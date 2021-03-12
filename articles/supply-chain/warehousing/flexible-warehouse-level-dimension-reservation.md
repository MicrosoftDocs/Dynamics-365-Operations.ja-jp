---
title: 変動倉庫レベルの分析引当ポリシー
description: このトピックでは、製品に関連付けられている引当階層が特定のバッチの予約を許可していない場合でも、バッチ追跡製品を販売し、WMS 対応工程としてロジスティクスを実行する企業が顧客の販売注文に対して特定のバッチを予約できるようにする在庫引当のポリシーについて説明します。
author: perlynne
manager: tfehr
ms.date: 07/31/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: WHSReservationHierarchy, WHSWorkTrans, WHSWorkInventTrans, WHSInventTableReservationHierarchy, WHSReservationHierarchyCreate, WHSInventTableReservationHierarchy
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: perlynne
ms.search.validFrom: 2020-01-15
ms.dyn365.ops.version: 10.0.13
ms.openlocfilehash: bf50b0b8da2859caab4db2394f2d56f7b76793ca
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 01/15/2021
ms.locfileid: "5004805"
---
# <a name="flexible-warehouse-level-dimension-reservation-policy"></a><span data-ttu-id="6f8a2-103">変動倉庫レベルの分析引当ポリシー</span><span class="sxs-lookup"><span data-stu-id="6f8a2-103">Flexible warehouse-level dimension reservation policy</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="6f8a2-104">「バッチ非優先\[ロケーション\]」タイプの在庫引当階層が製品に関連付けられている場合は、バッチ追跡製品を販売し、Microsoft Dynamics 365 Warehouse Management System (WMS) で有効になっている工程で物流を実行する企業は、顧客の販売注文に対して特定のバッチを引当することはできません。</span><span class="sxs-lookup"><span data-stu-id="6f8a2-104">When an inventory reservation hierarchy of the "Batch-below\[location\]" type is associated with products, businesses that sell batch-tracked products and run their logistics as operations that are enabled for the Microsoft Dynamics 365 Warehouse Management System (WMS) can't reserve specific batches of those products for customer sales orders.</span></span>

<span data-ttu-id="6f8a2-105">また、特定のライセンス プレートは、製品が既定の引当階層に関連付けられている場合、販売注文の製品に対して引当することはできません。</span><span class="sxs-lookup"><span data-stu-id="6f8a2-105">In a similar way, specific license plates can't be reserved for products on sales orders when those products are associated with the default reservation hierarchy.</span></span>

<span data-ttu-id="6f8a2-106">このトピックでは、製品が引当階層 「バッチ非優先\[ロケーション\]」 に関連付けられている場合でも、特定のバッチやライセンス プレートを引当可能となる、在庫の引き当てポリシーについて説明します。</span><span class="sxs-lookup"><span data-stu-id="6f8a2-106">This topic describes the inventory reservation policy that lets these businesses reserve specific batches or license plates, even when the products are associated with a "Batch-below\[location\]" reservation hierarchy.</span></span>

## <a name="inventory-reservation-hierarchy"></a><span data-ttu-id="6f8a2-107">在庫引当階層</span><span class="sxs-lookup"><span data-stu-id="6f8a2-107">Inventory reservation hierarchy</span></span>

<span data-ttu-id="6f8a2-108">このセクションでは、既存の在庫引当階層の要約します。</span><span class="sxs-lookup"><span data-stu-id="6f8a2-108">This section summarizes the existing inventory reservation hierarchy.</span></span>

<span data-ttu-id="6f8a2-109">在庫引当階層では、保管分析コードに関する限り、需要オーダーはサイト、倉庫、在庫ステータスの必須分析コードを保持し、倉庫ロジックはロケーションを要求された数量に割り当て、ロケーションを引当する責任があります。</span><span class="sxs-lookup"><span data-stu-id="6f8a2-109">The inventory reservation hierarchy dictates that, as far as storage dimensions are concerned, the demand order carries the mandatory dimensions of site, warehouse, and inventory status, whereas the warehouse logic is responsible for assigning a location to the requested quantities and reserving the location.</span></span> <span data-ttu-id="6f8a2-110">つまり、需要オーダーと倉庫工程の間の相互作用において、注文の出荷元 (つまり、サイトと倉庫) を示すように需要オーダーが求められます。</span><span class="sxs-lookup"><span data-stu-id="6f8a2-110">In other words, in the interactions between the demand order and the warehouse operations, the demand order is expected to indicate where the order must be shipped from (that is, what site and warehouse).</span></span> <span data-ttu-id="6f8a2-111">倉庫では、倉庫の施設内で必要な数量を見つけるためにロジックに依存します。</span><span class="sxs-lookup"><span data-stu-id="6f8a2-111">The warehouse then relies on its logic to find the required quantity in the warehouse premises.</span></span>

<span data-ttu-id="6f8a2-112">ただし、ビジネスの運用モデルを反映するために、追跡用分析コード (バッチ番号とシリアル番号) の方が柔軟性があります。</span><span class="sxs-lookup"><span data-stu-id="6f8a2-112">However, to reflect the operational model of the business, tracking dimensions (batch and serial numbers) are subject to more flexibility.</span></span> <span data-ttu-id="6f8a2-113">在庫引当階層は、次の条件が適用されるシナリオに対応できます。</span><span class="sxs-lookup"><span data-stu-id="6f8a2-113">An inventory reservation hierarchy can accommodate scenarios where the following conditions apply:</span></span>

- <span data-ttu-id="6f8a2-114">業務は、倉庫保管スペースで数量が検出された後、バッチまたはシリアル番号を持つ数量のピッキングを管理するために倉庫工程に依存しています。</span><span class="sxs-lookup"><span data-stu-id="6f8a2-114">The business relies on its warehouse operations to manage picking of quantities that have batch or serial numbers after the quantities have been found in the warehousing storage space.</span></span> <span data-ttu-id="6f8a2-115">このモデルは、多くの場合 *バッチ非優先\[ロケーション\]* と呼ばれます。</span><span class="sxs-lookup"><span data-stu-id="6f8a2-115">This model is often referred to as *Batch-below\[location\]*.</span></span> <span data-ttu-id="6f8a2-116">これは通常、製品のバッチまたはシリアル番号の ID が、販売会社に需要のある顧客にとって重要ではない場合に使用されます。</span><span class="sxs-lookup"><span data-stu-id="6f8a2-116">It's typically used when a product's batch or serial number identification isn't important to the customers who place the demand with the selling company.</span></span>
- <span data-ttu-id="6f8a2-117">バッチ番号またはシリアル番号が顧客の注文仕様の一部であり、それらが需要オーダーに記録されている場合、倉庫内の数量を見つける倉庫操作は、特定の要求された番号によって制約され、それらを変更することはできません。</span><span class="sxs-lookup"><span data-stu-id="6f8a2-117">If batch or serial numbers are part of a customer's order specification, and they are recorded on the demand order, the warehouse operations that find the quantities in the warehouse are constrained by the specific requested numbers and aren't allowed to change them.</span></span> <span data-ttu-id="6f8a2-118">このモデルは、*バッチ優先\[ロケーション\]* と呼ばれます。</span><span class="sxs-lookup"><span data-stu-id="6f8a2-118">This model is referred to as *Batch-above\[location\]*.</span></span>

<span data-ttu-id="6f8a2-119">これらのシナリオでは、各リリース製品に割り当て可能な在庫引当階層は 1 つだけであるという課題があります。</span><span class="sxs-lookup"><span data-stu-id="6f8a2-119">In these scenarios, the challenge is that only one inventory reservation hierarchy can be assigned to each released product.</span></span> <span data-ttu-id="6f8a2-120">したがって、WMS が追跡対象の品目を処理するために、階層の割り当てがバッチまたはシリアル番号を予約する時期を決定した後 (需要オーダーを取得したとき、または倉庫ピッキング作業中)、このタイミングをアドホック基準で変更することはできません。</span><span class="sxs-lookup"><span data-stu-id="6f8a2-120">Therefore, for the WMS to handle tracked items, after the hierarchy assignment determines when the batch or serial number should be reserved (either when the demand order is taken or during the warehouse picking work), this timing can't be changed on an ad-hoc basis.</span></span>

## <a name="flexible-reservation-for-batch-tracked-items"></a><span data-ttu-id="6f8a2-121">バッチ追跡品目の変動引当</span><span class="sxs-lookup"><span data-stu-id="6f8a2-121">Flexible reservation for batch-tracked items</span></span>

### <a name="business-scenario"></a><span data-ttu-id="6f8a2-122">ビジネス シナリオ</span><span class="sxs-lookup"><span data-stu-id="6f8a2-122">Business scenario</span></span>

<span data-ttu-id="6f8a2-123">このシナリオでは、会社は完成品をバッチ番号で追跡する在庫戦略を使用しています。</span><span class="sxs-lookup"><span data-stu-id="6f8a2-123">In this scenario, a company uses an inventory strategy where finished goods are tracked by batch numbers.</span></span> <span data-ttu-id="6f8a2-124">この会社は、WMS ワークロードも使用します。</span><span class="sxs-lookup"><span data-stu-id="6f8a2-124">This company also uses the WMS workload.</span></span> <span data-ttu-id="6f8a2-125">このワークロードには、バッチ対応アイテムの倉庫ピッキングおよび出荷操作を計画および実行するための十分に装備されたロジックがあるため、完成したアイテムのほとんどは「バッチ非優先\[ロケーション\]」在庫引当階層に関連付けられます。</span><span class="sxs-lookup"><span data-stu-id="6f8a2-125">Because this workload has well-equipped logic for planning and running warehouse picking and shipping operations for batch-enabled items, most of the finished items are associated with a "Batch-below\[location\]" inventory reservation hierarchy.</span></span> <span data-ttu-id="6f8a2-126">このタイプの運用設定の利点は、ピッキングするバッチや倉庫内での配置ロケーションを決定する意思決定 (効果的な引当を決定すること) が、倉庫のピッキング工程を開始するまで延期されるという点です。</span><span class="sxs-lookup"><span data-stu-id="6f8a2-126">The advantage of this type of operational setup is that decisions (which are effectively reservation decisions) about which batches to pick and where to put them in the warehouse are postponed until the warehouse picking operations start.</span></span> <span data-ttu-id="6f8a2-127">顧客の注文が行われたときに作成されません。</span><span class="sxs-lookup"><span data-stu-id="6f8a2-127">They aren't made when the customer's order is placed.</span></span>

<span data-ttu-id="6f8a2-128">「バッチ非優先\[ロケーション\]」の引当階層は、会社のビジネス目標にも対応していますが、会社が獲得した顧客の多くは、製品の再注文時に以前に購入したものと同じバッチを必要とします。</span><span class="sxs-lookup"><span data-stu-id="6f8a2-128">Although the "Batch-below\[location\]" reservation hierarchy serves the company's business goals well, many of the company's established customers require the same batch that they previously purchased when they reorder products.</span></span> <span data-ttu-id="6f8a2-129">したがって、この会社では、バッチ引当ルールの処理方法に関する柔軟性を模索しているため、同じ品目に対する顧客の需要に応じて次のような動作が発生します。</span><span class="sxs-lookup"><span data-stu-id="6f8a2-129">Therefore, the company is looking for flexibility in the way that the batch reservation rules are handled, so that, depending on the customers' demand for the same item, the following behaviors occur:</span></span>

- <span data-ttu-id="6f8a2-130">バッチ番号は、注文が販売プロセッサによって取得されるときに記録および予約することができ、倉庫行程中に変更したり、他の需要によって取得したりすることはできません。</span><span class="sxs-lookup"><span data-stu-id="6f8a2-130">A batch number can be recorded and reserved when the order is taken by the sales processor, and it can't be changed during warehouse operations and/or taken by other demands.</span></span> <span data-ttu-id="6f8a2-131">この動作により、注文されたバッチ番号が顧客に出荷されることが保証されます。</span><span class="sxs-lookup"><span data-stu-id="6f8a2-131">This behavior helps guarantee that the batch number that was ordered is shipped to the customer.</span></span>
- <span data-ttu-id="6f8a2-132">顧客にとってバッチ番号が重要ではない場合、倉庫行程でピッキング作業中に、販売注文の登録と予約が完了した後、バッチ番号を決定できます。</span><span class="sxs-lookup"><span data-stu-id="6f8a2-132">If the batch number isn't important to the customer, the warehouse operations can determine a batch number during picking work, after sales order registration and reservation have been done.</span></span>

### <a name="allowing-reservation-of-a-specific-batch-on-the-sales-order"></a><span data-ttu-id="6f8a2-133">販売注文の特定のバッチの引当許可</span><span class="sxs-lookup"><span data-stu-id="6f8a2-133">Allowing reservation of a specific batch on the sales order</span></span>

<span data-ttu-id="6f8a2-134">「バッチ非優先\[ロケーション\]」在庫引当階層に関連付けられている品目のバッチ引当動作に必要な柔軟性を提供するには、在庫マネージャーは、**在庫引当階層** ページで **バッチ番号** レベルの **需要の引当オーダーを許可** チェック ボックスを選択する必要があります。</span><span class="sxs-lookup"><span data-stu-id="6f8a2-134">To accommodate the desired flexibility in the batch reservation behavior for items that are associated with a "Batch-below\[location\]" inventory reservation hierarchy, inventory managers must select the **Allow reservation on demand order** check box for the **Batch number** level on the **Inventory reservation hierarchies** page.</span></span>

![在庫引当階層を柔軟にする](media/Flexible-inventory-reservation-hierarchy.png)

<span data-ttu-id="6f8a2-136">階層内の **バッチ番号** レベルが選択されている場合は、そのレベルより上で **ロケーション** レベルまでのすべての分析コードが自動的に選択されます。</span><span class="sxs-lookup"><span data-stu-id="6f8a2-136">When the **Batch number** level in the hierarchy is selected, all dimensions above that level and up through the **Location** level will be automatically selected.</span></span> <span data-ttu-id="6f8a2-137">(既定では、**ロケーション** レベルの上のすべての分析コードが事前に設定されています。) この動作は、注文明細行で特定のバッチ番号を予約した後、バッチ番号とロケーションの間の範囲のすべての分析コードも自動的に予約されるロジックを反映しています。</span><span class="sxs-lookup"><span data-stu-id="6f8a2-137">(By default, all dimensions above the **Location** level are preselected.) This behavior reflects the logic where all dimensions in the range between the batch number and location are also automatically reserved after you reserve a specific batch number on the order line.</span></span>

> [!NOTE]
> <span data-ttu-id="6f8a2-138">**需要の引当オーダーを許可** チェックボックスは、倉庫のロケーション分析コードより下にある引当階層レベルにのみ適用されます。</span><span class="sxs-lookup"><span data-stu-id="6f8a2-138">The **Allow reservation on demand order** check box applies only to reservation hierarchy levels that are below the warehouse location dimension.</span></span>
>
> <span data-ttu-id="6f8a2-139">**バッチ番号** および **ライセンス プレート** は、柔軟な予約ポリシーで使用するためにオープンされている階層内のレベルのみを指定します。</span><span class="sxs-lookup"><span data-stu-id="6f8a2-139">**Batch number** and **License plate** are the only levels in the hierarchy that are open for the flexible reservation policy.</span></span> <span data-ttu-id="6f8a2-140">つまり、**オンデマンド引当を許可する** のチェックボックスを **ロケーション** または **シリアル番号** レベルで選択することはできません。</span><span class="sxs-lookup"><span data-stu-id="6f8a2-140">In other words, you can't select the **Allow reservation on demand order** check box for the **Location** or **Serial number** level.</span></span>
>
> <span data-ttu-id="6f8a2-141">引当階層にシリアル番号分析コード (常に **バッチ番号** レベル未満でなければならない) が含まれていて、バッチ番号のバッチ固有の予約をオンにした場合、システムは、「シリアル非優先\[ロケーション\]」引当ポリシーに適用されるルールに基づいて、シリアル番号の予約およびピッキング操作を引き続き処理します。</span><span class="sxs-lookup"><span data-stu-id="6f8a2-141">If your reservation hierarchy includes the serial number dimension (which must always be below the **Batch number** level), and if you've turned on batch-specific reservation for the batch number, the system will continue to handle serial number reservation and picking operations, based on the rules that apply to the "Serial-below\[location\]" reservation policy.</span></span>

<span data-ttu-id="6f8a2-142">いつでも、展開内の既存の「バッチ非優先\[ロケーション\]」引当階層にバッチ固有の予約を許可できます。</span><span class="sxs-lookup"><span data-stu-id="6f8a2-142">At any point, you can allow batch-specific reservation for an existing "Batch-below\[location\]" reservation hierarchy in your deployment.</span></span> <span data-ttu-id="6f8a2-143">この変更は、変更が発生する前に作成された引当および未処理の倉庫の作業には影響しません。</span><span class="sxs-lookup"><span data-stu-id="6f8a2-143">This change won't affect any reservations and open warehouse work that were created before the change occurred.</span></span> <span data-ttu-id="6f8a2-144">ただし、引当階層に関連付けられている 1 つ以上の品目に対して **引当済注文**、**引当済現物**、または **注文済** 払出タイプの在庫トランザクションが存在する場合は、**需要の引当オーダーを許可** チェックボックスをオフにすることはできません。</span><span class="sxs-lookup"><span data-stu-id="6f8a2-144">However, the **Allow reservation on demand order** check box can't be cleared if inventory transactions of the **Reserved ordered**, **Reserved physical**, or **Ordered** issue type exist for one or more items that are associated with that reservation hierarchy.</span></span>

> [!NOTE]
> <span data-ttu-id="6f8a2-145">品目の既存の引当階層で、注文のバッチ指定が許可されていない場合は、両方の階層で階層レベル構造が同じであることを条件として、バッチの指定が可能な引当階層に再割り当てすることができます。</span><span class="sxs-lookup"><span data-stu-id="6f8a2-145">If an item's existing reservation hierarchy doesn't allow batch specification on the order, you can reassign it to a reservation hierarchy that does allow batch specification, provided that the hierarchy level structure is the same in both hierarchies.</span></span> <span data-ttu-id="6f8a2-146">**品目の引当階層を変更** 機能を使用して、再割り当てを行います。</span><span class="sxs-lookup"><span data-stu-id="6f8a2-146">Use the **Change reservation hierarchy for items** function to do the reassignment.</span></span> <span data-ttu-id="6f8a2-147">この変更は、バッチ追跡された品目のサブセットに対する変動バッチ引当を防止し、その他の製品ポートフォリオに対して許可する場合に関連します。</span><span class="sxs-lookup"><span data-stu-id="6f8a2-147">This change might be relevant when you want to prevent flexible batch reservation for a subset of batch-tracked items but allow it for the rest of the product portfolio.</span></span>

<span data-ttu-id="6f8a2-148">**需要の引当オーダーを許可** チェックボックスを選択したかどうかにかかわらず、注文明細行のアイテムに特定のバッチ番号を引き当てない場合は、「バッチ非優先\[ロケーション\]」引当階層に有効な既定の倉庫行程ロジックが引き続き適用されます。</span><span class="sxs-lookup"><span data-stu-id="6f8a2-148">Regardless of whether you've selected the **Allow reservation on demand order** check box, if you don't want to reserve a specific batch number for the item on an order line, default warehouse operations logic that is valid for a "Batch-below\[location\]" reservation hierarchy will still apply.</span></span>

### <a name="reserve-a-specific-batch-number-for-a-customer-order"></a><span data-ttu-id="6f8a2-149">顧客注文の特定のバッチ番号の引当</span><span class="sxs-lookup"><span data-stu-id="6f8a2-149">Reserve a specific batch number for a customer order</span></span>

<span data-ttu-id="6f8a2-150">バッチ追跡された品目の「バッチ非優先\[ロケーション\]」在庫引当階層が設定された後、注文の特定のバッチ番号を予約できるようになり、販売注文プロセッサは、顧客の要求に応じて、次のいずれかの方法で同じアイテムの顧客注文を受け取ることができます。</span><span class="sxs-lookup"><span data-stu-id="6f8a2-150">After a batch-tracked item's "Batch-below\[location\]" inventory reservation hierarchy is set up to allow reservation of specific batch numbers on sales orders, sales order processors can take customer orders for the same item in one of the following ways, depending on the customer's request:</span></span>

- <span data-ttu-id="6f8a2-151">**バッチ番号を指定せずに注文の詳細を入力します** - このアプローチは、製品のバッチの仕様が顧客にとって重要ではない場合に使用します。</span><span class="sxs-lookup"><span data-stu-id="6f8a2-151">**Enter order details without specifying a batch number** – This approach should be used when the product's batch specification isn't important to the customer.</span></span> <span data-ttu-id="6f8a2-152">このタイプの注文の処理に関連付けられているすべての既存のプロセスは、システムに変更されずに残ります。</span><span class="sxs-lookup"><span data-stu-id="6f8a2-152">All existing processes that are associated with handling an order of this type in the system remain unchanged.</span></span> <span data-ttu-id="6f8a2-153">ユーザー側で追加の考慮事項は必要ありません。</span><span class="sxs-lookup"><span data-stu-id="6f8a2-153">No additional considerations are required on the part of users.</span></span>
- <span data-ttu-id="6f8a2-154">**注文の詳細を入力し、特定のバッチ番号を引当** - 顧客が特定のバッチを要求する場合は、この方法を使用する必要があります。</span><span class="sxs-lookup"><span data-stu-id="6f8a2-154">**Enter order details and reserve a specific batch number** – This approach should be used when the customer requests a specific batch.</span></span> <span data-ttu-id="6f8a2-155">通常、顧客は以前に購入した製品を再注文するときに特定のバッチを要求します。</span><span class="sxs-lookup"><span data-stu-id="6f8a2-155">Typically, customers will request a specific batch when they are reordering a product that they previously purchased.</span></span> <span data-ttu-id="6f8a2-156">このタイプのバッチ固有の引当は、*確定済み引当* と呼ばれます。</span><span class="sxs-lookup"><span data-stu-id="6f8a2-156">This type of batch-specific reservation is referred to as *order-committed reservation*.</span></span>

<span data-ttu-id="6f8a2-157">次の一連のルールは、数量が処理されるときに有効になり、バッチ番号は特定の注文にコミットされます。</span><span class="sxs-lookup"><span data-stu-id="6f8a2-157">The following set of rules is valid when quantities are processed, and a batch number is committed to a specific order:</span></span>

- <span data-ttu-id="6f8a2-158">「バッチ非優先\[ロケーション\]」引当ポリシーの下で品目の特定のバッチ番号の引当を許可するには、システムはロケーションまですべての分析コードを引当する必要があります。</span><span class="sxs-lookup"><span data-stu-id="6f8a2-158">To allow reservation of a specific batch number for an item under the "Batch-below\[location\]" reservation policy, the system must reserve all dimensions up through location.</span></span> <span data-ttu-id="6f8a2-159">通常、この範囲には、ライセンス プレート分析コードが含まれます。</span><span class="sxs-lookup"><span data-stu-id="6f8a2-159">This range typically includes the license plate dimension.</span></span>
- <span data-ttu-id="6f8a2-160">注文が確定したバッチ引当を使用する販売明細行に対してピッキング作業が作成される場合、ロケーションの指示は使用されません。</span><span class="sxs-lookup"><span data-stu-id="6f8a2-160">Location directives aren't used when picking work is created for a sales line that uses order-committed batch reservation.</span></span>
- <span data-ttu-id="6f8a2-161">注文が確定したバッチの作業倉庫処理では、ユーザーもシステムもバッチ番号を変更することはできません。</span><span class="sxs-lookup"><span data-stu-id="6f8a2-161">During warehouse processing of work for order-committed batches, neither the user nor the system is allowed to change the batch number.</span></span> <span data-ttu-id="6f8a2-162">(この処理には例外処理が含まれています。)</span><span class="sxs-lookup"><span data-stu-id="6f8a2-162">(This processing includes exception handling.)</span></span>

<span data-ttu-id="6f8a2-163">次の例は、エンド ツー エンド フローの例を示しています。</span><span class="sxs-lookup"><span data-stu-id="6f8a2-163">The following example shows the end-to-end flow.</span></span>

## <a name="example-scenario-batch-number-allocation"></a><span data-ttu-id="6f8a2-164">シナリオ例 : バッチ番号の配賦</span><span class="sxs-lookup"><span data-stu-id="6f8a2-164">Example scenario: Batch number allocation</span></span>

<span data-ttu-id="6f8a2-165">この例では、**USMF** デモ データの会社を使用して、デモ データをインストールする必要があります。</span><span class="sxs-lookup"><span data-stu-id="6f8a2-165">For this example, demo data must be installed, and you must use the **USMF** demo data company.</span></span>

### <a name="set-up-an-inventory-reservation-hierarchy-to-allow-batch-specific-reservation"></a><a name="Example-batch-allocation"></a><span data-ttu-id="6f8a2-166">在庫引当階層を設定して、バッチ固有の引当を許可する</span><span class="sxs-lookup"><span data-stu-id="6f8a2-166">Set up an inventory reservation hierarchy to allow batch-specific reservation</span></span>

1. <span data-ttu-id="6f8a2-167">**倉庫管理** \> **設定** \> **在庫 \> 引当階層** に移動します。</span><span class="sxs-lookup"><span data-stu-id="6f8a2-167">Go to **Warehouse management** \> **Setup** \> **Inventory \> Reservation hierarchy**.</span></span>
2. <span data-ttu-id="6f8a2-168">**新規** を選択します。</span><span class="sxs-lookup"><span data-stu-id="6f8a2-168">Select **New**.</span></span>
3. <span data-ttu-id="6f8a2-169">**名前** フィールドに、名前を入力します (たとえば、**BatchFlex**)。</span><span class="sxs-lookup"><span data-stu-id="6f8a2-169">In the **Name** field, enter a name (for example, **BatchFlex**).</span></span>
4. <span data-ttu-id="6f8a2-170">**説明** フィールドに、説明を入力します (たとえば、**下の変動バッチ** など)。</span><span class="sxs-lookup"><span data-stu-id="6f8a2-170">In the **Description** field, enter a description (for example, **Batch below flexible**).</span></span>
5. <span data-ttu-id="6f8a2-171">**選択済** フィールドで、**シリアル番号** および **所有者** を選択し、左矢印ボタンを選択して **使用可能** フィールドに移動します。</span><span class="sxs-lookup"><span data-stu-id="6f8a2-171">In the **Selected** field, select **Serial number** and **Owner**, and then select the left arrow button to move them to the **Available** field.</span></span>
6. <span data-ttu-id="6f8a2-172">**OK** を選択します。</span><span class="sxs-lookup"><span data-stu-id="6f8a2-172">Select **OK**.</span></span>
7. <span data-ttu-id="6f8a2-173">**バッチ番号** 分析コード レベルの行で、**需要の引当オーダーを許可** チェックボックスを選択します。</span><span class="sxs-lookup"><span data-stu-id="6f8a2-173">In the row for the **Batch number** dimension level, select the **Allow reservation on demand order** check box.</span></span> <span data-ttu-id="6f8a2-174">**ライセンス プレート** と **ロケーション** のレベルは自動的に選択され、それらのチェックボックスをオフにすることはできません。</span><span class="sxs-lookup"><span data-stu-id="6f8a2-174">The **License plate** and **Location** levels are automatically selected, and you can't clear the check boxes for them.</span></span>
8. <span data-ttu-id="6f8a2-175">**保存** を選択します。</span><span class="sxs-lookup"><span data-stu-id="6f8a2-175">Select **Save**.</span></span>

### <a name="create-a-new-released-product"></a><span data-ttu-id="6f8a2-176">新しくリリースされた製品の作成</span><span class="sxs-lookup"><span data-stu-id="6f8a2-176">Create a new released product</span></span>

1. <span data-ttu-id="6f8a2-177">次の値を使用して、製品の 3 つのマスター データ パラメータを設定します。</span><span class="sxs-lookup"><span data-stu-id="6f8a2-177">Set the product's three master data parameters by using these values:</span></span>

    - <span data-ttu-id="6f8a2-178">**保管分析コード グループ** フィールドで、**Ware** を選択します。</span><span class="sxs-lookup"><span data-stu-id="6f8a2-178">In the **Storage dimension group** field, select **Ware**.</span></span>
    - <span data-ttu-id="6f8a2-179">**追跡用分析コード グループ** フィールドで、**Batch-Phy** を選択します。</span><span class="sxs-lookup"><span data-stu-id="6f8a2-179">In the **Tracking dimension group** field, select **Batch-Phy**.</span></span>
    - <span data-ttu-id="6f8a2-180">**引当階層** フィールドで、**BatchFlex** を選択します。</span><span class="sxs-lookup"><span data-stu-id="6f8a2-180">In the **Reservation hierarchy** field, select **BatchFlex**.</span></span>

2. <span data-ttu-id="6f8a2-181">**B11** や **B22** などの 2 つのバッチ番号を作成します。</span><span class="sxs-lookup"><span data-stu-id="6f8a2-181">Create two batch numbers, such as **B11** and **B22**.</span></span>
3. <span data-ttu-id="6f8a2-182">次の値を使用して、品目の数量を手持在庫に追加します。</span><span class="sxs-lookup"><span data-stu-id="6f8a2-182">Add item quantities to on-hand stock by using the following values.</span></span>

    | <span data-ttu-id="6f8a2-183">倉庫</span><span class="sxs-lookup"><span data-stu-id="6f8a2-183">Warehouse</span></span> | <span data-ttu-id="6f8a2-184">バッチ番号</span><span class="sxs-lookup"><span data-stu-id="6f8a2-184">Batch number</span></span> | <span data-ttu-id="6f8a2-185">ロケーション</span><span class="sxs-lookup"><span data-stu-id="6f8a2-185">Location</span></span> | <span data-ttu-id="6f8a2-186">ライセンス プレート</span><span class="sxs-lookup"><span data-stu-id="6f8a2-186">License plate</span></span> | <span data-ttu-id="6f8a2-187">件数</span><span class="sxs-lookup"><span data-stu-id="6f8a2-187">Quantity</span></span> |
    |-----------|--------------|----------|---------------|----------|
    | <span data-ttu-id="6f8a2-188">24</span><span class="sxs-lookup"><span data-stu-id="6f8a2-188">24</span></span>        | <span data-ttu-id="6f8a2-189">B11</span><span class="sxs-lookup"><span data-stu-id="6f8a2-189">B11</span></span>          | <span data-ttu-id="6f8a2-190">BULK-001</span><span class="sxs-lookup"><span data-stu-id="6f8a2-190">BULK-001</span></span> | <span data-ttu-id="6f8a2-191">なし</span><span class="sxs-lookup"><span data-stu-id="6f8a2-191">None</span></span>          | <span data-ttu-id="6f8a2-192">10</span><span class="sxs-lookup"><span data-stu-id="6f8a2-192">10</span></span>       |
    | <span data-ttu-id="6f8a2-193">24</span><span class="sxs-lookup"><span data-stu-id="6f8a2-193">24</span></span>        | <span data-ttu-id="6f8a2-194">B11</span><span class="sxs-lookup"><span data-stu-id="6f8a2-194">B11</span></span>          | <span data-ttu-id="6f8a2-195">FL-001</span><span class="sxs-lookup"><span data-stu-id="6f8a2-195">FL-001</span></span>   | <span data-ttu-id="6f8a2-196">LP11</span><span class="sxs-lookup"><span data-stu-id="6f8a2-196">LP11</span></span>          | <span data-ttu-id="6f8a2-197">10</span><span class="sxs-lookup"><span data-stu-id="6f8a2-197">10</span></span>       |
    | <span data-ttu-id="6f8a2-198">24</span><span class="sxs-lookup"><span data-stu-id="6f8a2-198">24</span></span>        | <span data-ttu-id="6f8a2-199">B22</span><span class="sxs-lookup"><span data-stu-id="6f8a2-199">B22</span></span>          | <span data-ttu-id="6f8a2-200">FL-002</span><span class="sxs-lookup"><span data-stu-id="6f8a2-200">FL-002</span></span>   | <span data-ttu-id="6f8a2-201">LP22</span><span class="sxs-lookup"><span data-stu-id="6f8a2-201">LP22</span></span>          | <span data-ttu-id="6f8a2-202">10</span><span class="sxs-lookup"><span data-stu-id="6f8a2-202">10</span></span>       |

### <a name="enter-sales-order-details"></a><a name="sales-order-details"></a><span data-ttu-id="6f8a2-203">販売注文詳細の入力</span><span class="sxs-lookup"><span data-stu-id="6f8a2-203">Enter sales order details</span></span>

1. <span data-ttu-id="6f8a2-204">**販売とマーケティング** \> **販売注文** \> **すべての販売注文** の順に移動します。</span><span class="sxs-lookup"><span data-stu-id="6f8a2-204">Go to **Sales and marketing** \> **Sales orders** \> **All sales orders**.</span></span>
2. <span data-ttu-id="6f8a2-205">**新規** を選択します。</span><span class="sxs-lookup"><span data-stu-id="6f8a2-205">Select **New**.</span></span>
3. <span data-ttu-id="6f8a2-206">販売注文ヘッダーの **顧客 ID** フィールドに、**US-003** と入力します。</span><span class="sxs-lookup"><span data-stu-id="6f8a2-206">On the sales order header, in the **Customer account** field, enter **US-003**.</span></span>
4. <span data-ttu-id="6f8a2-207">新規の品目の明細行を追加し、数量として **10** を入力します。</span><span class="sxs-lookup"><span data-stu-id="6f8a2-207">Add a line for the new item, and enter **10** as the quantity.</span></span> <span data-ttu-id="6f8a2-208">**倉庫** フィールドが **24** に設定されていることを確認してください。</span><span class="sxs-lookup"><span data-stu-id="6f8a2-208">Make sure that the **Warehouse** field is set to **24**.</span></span>
5. <span data-ttu-id="6f8a2-209">**販売注文明細行** クイック タブで **在庫** を選択し、**管理** グループで **バッチ引当** を選択します。</span><span class="sxs-lookup"><span data-stu-id="6f8a2-209">On the **Sales order lines** FastTab, select **Inventory**, and then, in the **Maintain** group, select **Batch reservation**.</span></span> <span data-ttu-id="6f8a2-210">**バッチ引当** ページに、注文明細行の引当に使用できるバッチのリストが表示されます。</span><span class="sxs-lookup"><span data-stu-id="6f8a2-210">The **Batch reservation** page shows a list of batches that are available for reservation for the order line.</span></span> <span data-ttu-id="6f8a2-211">この例では、バッチ番号 **B11** の場合は **20** の数量、バッチ番号 **B22** の場合は **10** の数量が表示されます。</span><span class="sxs-lookup"><span data-stu-id="6f8a2-211">For this example, it shows a quantity of **20** for batch number **B11** and a quantity of **10** for batch number **B22**.</span></span> <span data-ttu-id="6f8a2-212">バッチ固有の引当を許可するように設定されていない限り、その行の品目が「バッチ非優先\[ロケーション\]」引当階層に関連付けられている場合、**バッチ引当** ページにアクセスできないことに注意してください。</span><span class="sxs-lookup"><span data-stu-id="6f8a2-212">Note that the **Batch reservation** page cannot be accessed from a line if the item on that line is associated with "Batch-below\[location\]" reservation hierarchy unless it is set up to allow batch-specific reservation.</span></span>

    > [!NOTE]
    > <span data-ttu-id="6f8a2-213">販売注文の特定のバッチを引当するには、**バッチ引当** ページを使用する必要があります。</span><span class="sxs-lookup"><span data-stu-id="6f8a2-213">To reserve a specific batch for a sales order, you must use the **Batch reservation** page.</span></span>
    >
    > <span data-ttu-id="6f8a2-214">販売注文明細行にバッチ番号を直接入力すると、「バッチ非優先\[ロケーション\]」の引当ポリシーの対象となる品目に対して特定のバッチ値を入力した場合と同じようにシステムが動作します。</span><span class="sxs-lookup"><span data-stu-id="6f8a2-214">If you enter the batch number directly on the sales order line, the system will behave as though you entered a specific batch value for an item that is subject to the "Batch-below\[location\]" reservation policy.</span></span> <span data-ttu-id="6f8a2-215">明細行を保存すると、警告メッセージが表示されます。</span><span class="sxs-lookup"><span data-stu-id="6f8a2-215">When you save the line, you will receive a warning message.</span></span> <span data-ttu-id="6f8a2-216">バッチ番号が注文明細行に直接指定されていることを確認した場合、その明細行は、通常の倉庫管理ロジックで処理されることはありません。</span><span class="sxs-lookup"><span data-stu-id="6f8a2-216">If you confirm that the batch number should be specified directly on the order line, the line won't be handled by the regular warehouse management logic.</span></span>
    >
    > <span data-ttu-id="6f8a2-217">**引当** ページの数量を引当すると、特定のバッチは引当されず、その行の倉庫操作の実行は、「バッチ非優先\[ロケーション\]」の引当ポリシーの下で適用されるルールに従います。</span><span class="sxs-lookup"><span data-stu-id="6f8a2-217">If you reserve the quantity from the **Reservation** page, no specific batch will be reserved, and the execution of warehouse operations for the line will follow the rules that are applicable under the "Batch-below\[location\]" reservation policy.</span></span>

    <span data-ttu-id="6f8a2-218">一般に、このページは「バッチ優先\[ロケーション\]」タイプの引当階層が関連付けられている品目に対して機能し、同じ方法で連携されます。</span><span class="sxs-lookup"><span data-stu-id="6f8a2-218">In general, this page works and is interacted with in the same way that it works and is interacted with for items that have an associated reservation hierarchy of the "Batch-above\[location\]" type.</span></span> <span data-ttu-id="6f8a2-219">ただし、次の例外が適用されます。</span><span class="sxs-lookup"><span data-stu-id="6f8a2-219">However, the following exceptions apply:</span></span>

    - <span data-ttu-id="6f8a2-220">**ソース明細行に確定済みのバッチ番号** クイック タブには、注文明細行に対して引き当てられているバッチ番号が表示されます。</span><span class="sxs-lookup"><span data-stu-id="6f8a2-220">The **Batch numbers committed to source line** FastTab shows the batch numbers that are reserved for the order line.</span></span> <span data-ttu-id="6f8a2-221">グリッドのバッチ値は、倉庫処理ステージを含む注文明細行のフルフィルメント サイクル全体で表示されます。</span><span class="sxs-lookup"><span data-stu-id="6f8a2-221">The batch values in the grid will be shown throughout the fulfillment cycle of the order line, including the warehouse processing stages.</span></span> <span data-ttu-id="6f8a2-222">対照的に、**概要** クイックタブでは、通常の注文明細行の引当 (**ロケーション** レベルの上にある分析コードに対して実行される引当) は、倉庫作業が作成される時点までグリッドに表示されます。</span><span class="sxs-lookup"><span data-stu-id="6f8a2-222">By contrast, on the **Overview** FastTab, regular order line reservation (that is, reservation that is done for the dimensions above the **Location** level) is shown in the grid up to the point when warehouse work is created.</span></span> <span data-ttu-id="6f8a2-223">その後、作業エンティティは明細行の引当を引き継ぎ、明細行の引当はページに表示されなくなります。</span><span class="sxs-lookup"><span data-stu-id="6f8a2-223">The work entity then takes over the line reservation, and the line reservation no longer appears on the page.</span></span> <span data-ttu-id="6f8a2-224">**ソース明細行に確定済みのバッチ番号** クイック タブは、販売注文プロセッサが、請求まで、ライフサイクルの任意の時点で顧客の注文に対して確定されたバッチ番号を表示できるようにするために役立ちます。</span><span class="sxs-lookup"><span data-stu-id="6f8a2-224">The **Batch numbers committed to source line** FastTab helps guarantee that the sales order processor can view the batch numbers that were committed to the customer's order at any point during its lifecycle, up through invoicing.</span></span>
    - <span data-ttu-id="6f8a2-225">特定のバッチの引当に加えて、ユーザーはシステムによって自動的に選択させる代わりに、バッチの特定のロケーションとライセンス プレートを手動で選択できます。</span><span class="sxs-lookup"><span data-stu-id="6f8a2-225">In addition to reserving a specific batch, a user can manually select the batch's specific location and license plate instead of letting the system automatically select them.</span></span> <span data-ttu-id="6f8a2-226">この機能は、注文が確定したバッチ引当メカニズムの設計に関連しています。</span><span class="sxs-lookup"><span data-stu-id="6f8a2-226">This capability is related to the design of the order-committed batch reservation mechanism.</span></span> <span data-ttu-id="6f8a2-227">前述のように、バッチ番号が「バッチ非優先\[ロケーション\]」引当ポリシーの品目で引当されている場合、システムはすべての分析コードをロケーションまで引当てる必要があります。</span><span class="sxs-lookup"><span data-stu-id="6f8a2-227">As was mentioned earlier, when a batch number is reserved for an item under the "Batch-below\[location\]" reservation policy, the system must reserve all dimensions up through location.</span></span> <span data-ttu-id="6f8a2-228">したがって、倉庫作業では、注文を処理したユーザーによって予約されたものと同じ保管分析コードが使用され、ピッキング行程に便利な、または可能な品目の保管ロケーションを常に表すとは限りません。</span><span class="sxs-lookup"><span data-stu-id="6f8a2-228">Therefore, warehouse work will carry the same storage dimensions that were reserved by the users who worked with the orders, and it might not always represent the item storage placement that is convenient, or even possible, for picking operations.</span></span> <span data-ttu-id="6f8a2-229">注文処理担当者が倉庫の制約を認識している場合、バッチを予約する際に特定のロケーションとライセンス プレートを手動で選択することができます。</span><span class="sxs-lookup"><span data-stu-id="6f8a2-229">If order processors are aware of the warehouse constraints, they might want to manually select the specific locations and license plates when they reserve a batch.</span></span> <span data-ttu-id="6f8a2-230">この場合、ユーザーはページ ヘッダーの **分析コードの表示** 機能を使用し、**概要** クイック タブのグリッドにロケーションとライセンス プレートを追加する必要があります。</span><span class="sxs-lookup"><span data-stu-id="6f8a2-230">In this case, the user must use the **Display dimensions** functionality on the page header, and must add the location and license plate in the grid on the **Overview** FastTab.</span></span>

6. <span data-ttu-id="6f8a2-231">**バッチ引当** ページで、バッチ **B11** の明細行を選択し、**引当行** を選択します。</span><span class="sxs-lookup"><span data-stu-id="6f8a2-231">On the **Batch reservation** page, select the line for batch **B11**, and then select **Reserve line**.</span></span> <span data-ttu-id="6f8a2-232">自動引当中にロケーションとライセンス プレートを割り当てるための指定されたロジックはありません。</span><span class="sxs-lookup"><span data-stu-id="6f8a2-232">There is no designated logic for assigning locations and license plates during automatic reservation.</span></span> <span data-ttu-id="6f8a2-233">**引当** フィールドに手動で数量を入力できます。</span><span class="sxs-lookup"><span data-stu-id="6f8a2-233">You can manually enter the quantity in the **Reservation** field.</span></span> <span data-ttu-id="6f8a2-234">**ソース明細行に確定済みのバッチ番号** クイック タブでは、バッチ **B11** が **確定済み** として表示されることに注意してください。</span><span class="sxs-lookup"><span data-stu-id="6f8a2-234">Notice that, on the **Batch numbers committed to source line** FastTab, batch **B11** is shown as **Committed**.</span></span>

    ![バッチ引当ページの特定のバッチ番号を販売注文明細行にコミットする](media/Batch-reservation-form-with-order-committed-reservation.png)

    > [!NOTE]
    > <span data-ttu-id="6f8a2-236">販売注文明細行の数量の引当は、複数のバッチ間で行うことができます。</span><span class="sxs-lookup"><span data-stu-id="6f8a2-236">Reservation of the quantity on a sales order line can be done across multiple batches.</span></span> <span data-ttu-id="6f8a2-237">同様に、複数のロケーションおよびライセンス プレートに対して同じバッチの引当を行うことができます (そのロケーションでライセンス プレートが有効になっている場合)。</span><span class="sxs-lookup"><span data-stu-id="6f8a2-237">Likewise, reservation of the same batch can be done against multiple locations and license plates (if license plates are enabled for the locations).</span></span>
    >
    > <span data-ttu-id="6f8a2-238">販売注文明細行の数量に対する特定のバッチの引当も部分的に設定することもできます。</span><span class="sxs-lookup"><span data-stu-id="6f8a2-238">Reservation of a specific batch for the quantity on a sales order line can also be partial.</span></span> <span data-ttu-id="6f8a2-239">たとえば、100 単位の合計数量を引当して、特定のバッチを 20 単位にコミットし、80 単位を使用可能なバッチのサイトおよび倉庫レベルで引当できます。</span><span class="sxs-lookup"><span data-stu-id="6f8a2-239">For example, the total quantity of 100 units can be reserved so that a specific batch is committed to 20 units, whereas 80 units are reserved at the site and warehouse levels for any available batch.</span></span> <span data-ttu-id="6f8a2-240">この場合、WMS は 2 つの異なる作業明細行を使用してピッキング工程を処理します。</span><span class="sxs-lookup"><span data-stu-id="6f8a2-240">In this case, the WMS will handle picking operations by using two separate work lines.</span></span>

7. <span data-ttu-id="6f8a2-241">**製品情報管理** \> **製品** \> **リリース済製品** の順に移動します。</span><span class="sxs-lookup"><span data-stu-id="6f8a2-241">Go to **Product information management** \> **Products** \> **Released products**.</span></span> <span data-ttu-id="6f8a2-242">品目を選択し、**在庫の管理** \> **表示** \> **トランザクション** を選択します。</span><span class="sxs-lookup"><span data-stu-id="6f8a2-242">Select your item, and then select **Manage inventory** \> **View** \> **Transactions**.</span></span>

    ![在庫トランザクション タイプとして確定済み引当](media/Inventory-transactions-for-order-committed-reservation.png)

8. <span data-ttu-id="6f8a2-244">販売注文明細行の引当に関連する品目の在庫トランザクションを確認します。</span><span class="sxs-lookup"><span data-stu-id="6f8a2-244">Review the item's inventory transactions that are related to the sales order line reservation.</span></span>

    - <span data-ttu-id="6f8a2-245">**参照** フィールドが **販売注文** に設定され、**払出** フィールドが **引当済現物** に設定されているトランザクションは、**ロケーション** レベルよりも上の在庫分析コードの注文明細行の引当を表します。</span><span class="sxs-lookup"><span data-stu-id="6f8a2-245">A transaction where the **Reference** field is set to **Sales order** and the **Issue** field is set to **Reserved physical** represents the order line reservation for the inventory dimensions above the **Location** level.</span></span> <span data-ttu-id="6f8a2-246">品目の在庫引当階層に従って、これらの分析コードは、サイト、倉庫、および在庫状態になります。</span><span class="sxs-lookup"><span data-stu-id="6f8a2-246">According to the item's inventory reservation hierarchy, those dimensions are site, warehouse, and inventory status.</span></span>
    - <span data-ttu-id="6f8a2-247">**参照** フィールドが **確定済み引当** に設定され、**払出** フィールドが **引当済現物** に設定されているトランザクションは、特定のバッチおよびその上のすべての在庫分析コードの注文明細行の引当を表します。</span><span class="sxs-lookup"><span data-stu-id="6f8a2-247">A transaction where the **Reference** field is set to **Order-committed reservation** and the **Issue** field is set to **Reserved physical** represents the order line reservation for the specific batch and all inventory dimensions above it.</span></span> <span data-ttu-id="6f8a2-248">品目の在庫引当階層に従って、これらの分析コードは、バッチ番号およびロケーションになります。</span><span class="sxs-lookup"><span data-stu-id="6f8a2-248">According to the item's inventory reservation hierarchy, those dimensions are batch number and location.</span></span> <span data-ttu-id="6f8a2-249">この例では、このロケーションは **Bulk-001** です。</span><span class="sxs-lookup"><span data-stu-id="6f8a2-249">In this example, the location is **Bulk-001**.</span></span>

9. <span data-ttu-id="6f8a2-250">販売注文ヘッダーで、**倉庫** \> **アクション** \> **倉庫にリリース** を選択します。</span><span class="sxs-lookup"><span data-stu-id="6f8a2-250">On the sales order header, select **Warehouse** \> **Actions** \> **Release to warehouse**.</span></span> <span data-ttu-id="6f8a2-251">注文明細行がウェーブ処理され、積荷と作業が作成されます。</span><span class="sxs-lookup"><span data-stu-id="6f8a2-251">The order line is now waved, and a load and work are created.</span></span>

### <a name="review-and-process-warehouse-work-that-has-order-committed-batch-numbers"></a><span data-ttu-id="6f8a2-252">注文が確定したバッチ番号を持つ倉庫作業の確認および処理</span><span class="sxs-lookup"><span data-stu-id="6f8a2-252">Review and process warehouse work that has order-committed batch numbers</span></span>

1. <span data-ttu-id="6f8a2-253">**販売注文明細行** クイック タブで、**倉庫** \> **作業の詳細** を選択します。</span><span class="sxs-lookup"><span data-stu-id="6f8a2-253">On the **Sales order lines** FastTab, select **Warehouse** \> **Work details**.</span></span>

    <span data-ttu-id="6f8a2-254">販売注文明細行に確定されているバッチの数量のピッキング工程を処理する作業には、次のような特性があります。</span><span class="sxs-lookup"><span data-stu-id="6f8a2-254">The work that handles the picking operation for batch quantities that are committed to the sales order line has the following characteristics:</span></span>

    - <span data-ttu-id="6f8a2-255">作業を作成するには、作業テンプレートを使用しますが、ロケーションの指示は使用しません。</span><span class="sxs-lookup"><span data-stu-id="6f8a2-255">To create work, the system uses work templates but not location directives.</span></span> <span data-ttu-id="6f8a2-256">いつ新しい作業を作成するかを決定するために、ピッキング明細行の最大数や特定の測定単位など、作業テンプレートに定義されているすべての標準設定が適用されます。</span><span class="sxs-lookup"><span data-stu-id="6f8a2-256">All the standard settings that are defined for work templates, such as a maximum number of pick lines or a specific unit of measure, will be applied to determine when new work should be created.</span></span> <span data-ttu-id="6f8a2-257">ただし、確定済み引当ではすべての在庫分析コードが既に指定されているため、ピッキングロケーションを識別するためのロケーションの指示に関連付けられているルールは考慮されません。</span><span class="sxs-lookup"><span data-stu-id="6f8a2-257">However, the rules that are associated with location directives for identifying pick locations aren't considered, because the order-committed reservation already specifies all the inventory dimensions.</span></span> <span data-ttu-id="6f8a2-258">これらの在庫分析コードには、倉庫の保管レベルの分析コードが含まれます。</span><span class="sxs-lookup"><span data-stu-id="6f8a2-258">Those inventory dimensions include the dimensions at the warehouse storage level.</span></span> <span data-ttu-id="6f8a2-259">したがって、作業では、ロケーションの指示を参照することなく、これらの分析コードが継承されます。</span><span class="sxs-lookup"><span data-stu-id="6f8a2-259">Therefore, the work inherits those dimensions without having to consult location directives.</span></span>
    - <span data-ttu-id="6f8a2-260">バッチ番号は、ピッキング行には表示されません。(「バッチ優先\[ロケーション\]」の引当階層が関連付けられている品目に対して作成される作業明細行と同様です) 代わりに、「開始」バッチ番号と他のすべての保管分析コードが、関連付けられている在庫トランザクションから参照されている作業明細行の作業在庫トランザクションに表示されます。</span><span class="sxs-lookup"><span data-stu-id="6f8a2-260">The batch number isn't shown on the pick line (as is the case for the work line that is created for an item that has an associated "Batch-above\[location\]" reservation hierarchy.) Instead, the "from" batch number and all other storage dimensions are shown on the work line's work inventory transaction that is referenced from the associated inventory transactions.</span></span>

        ![注文が確定した引当によって発生した作業の倉庫在庫トランザクション](media/Work-inventory-transactions-for-order-committed-reservation.png)

    - <span data-ttu-id="6f8a2-262">作業が作成されると、**参照** フィールドが **確定済み引当** に設定されている品目の在庫トランザクションが削除されます。</span><span class="sxs-lookup"><span data-stu-id="6f8a2-262">After work is created, the item's inventory transaction where the **Reference** field is set to **Order-committed reservation** is removed.</span></span> <span data-ttu-id="6f8a2-263">**参照** フィールドが **作業** に設定されている在庫トランザクションは、すべての数量の在庫分析コードに対して現物引当を保持するようになりました。</span><span class="sxs-lookup"><span data-stu-id="6f8a2-263">The inventory transaction where the **Reference** field is set to **Work** now holds the physical reservation on all the quantity's inventory dimensions.</span></span>

        <span data-ttu-id="6f8a2-264">倉庫工程は、作業の実行を通常の方法で処理することができます。</span><span class="sxs-lookup"><span data-stu-id="6f8a2-264">Warehouse operations can proceed to handle execution of the work in the usual manner.</span></span> <span data-ttu-id="6f8a2-265">ただし、モバイル デバイスの指示では、特定のバッチ番号を選択するよう作業者に指示します。</span><span class="sxs-lookup"><span data-stu-id="6f8a2-265">However, the instructions on the mobile device will instruct the worker to pick a specific batch number.</span></span> <span data-ttu-id="6f8a2-266">ロケーションがライセンス プレートにより制御されている倉庫環境では、複数のライセンス プレートで同じバッチが保管されているロケーションに作業者が到達した後、まだ引当されていないライセンス プレートから選択できます (たとえば、別の確定済み引当またはそのタイプの引当から発生する作業による)。</span><span class="sxs-lookup"><span data-stu-id="6f8a2-266">In warehouse environments where locations are license plate–controlled, after a worker reaches a location that stores the same batch on multiple license plates, he or she can pick from any license plate that isn't already reserved (for example, by another order-committed reservation or work that originates from a reservation of that type.)</span></span>

        <span data-ttu-id="6f8a2-267">作業明細行で指定されたロケーションからのピッキングが実際的ではない場合、倉庫オペレーターは次のいずれかのアクションを使用して、特定のバッチのピッキングをより便利なロケーションからリダイレクトできます。</span><span class="sxs-lookup"><span data-stu-id="6f8a2-267">If it turns out to be impractical to pick from the location that is specified on the work line, the warehouse operators can use one of the following actions to redirect picking of the specific batch from a more convenient location:</span></span>

        - <span data-ttu-id="6f8a2-268">モバイル デバイスでの標準の **ロケーションの上書き** アクション (倉庫作業者の **ピッキング ロケーションの上書きを許可** 設定が有効になっている場合)</span><span class="sxs-lookup"><span data-stu-id="6f8a2-268">The standard **Override location** action on a mobile device (provided that the warehouse worker's **Allow pick location override** setting is enabled)</span></span>
        - <span data-ttu-id="6f8a2-269">**作業一覧詳細** ページでの **ロケーションの変更** アクション。</span><span class="sxs-lookup"><span data-stu-id="6f8a2-269">The **Change location** action on the **Work list details** page.</span></span> 

2. <span data-ttu-id="6f8a2-270">モバイル デバイスで、ピッキングと作業の配置を完了します。</span><span class="sxs-lookup"><span data-stu-id="6f8a2-270">On the mobile device, finish picking and putting the work.</span></span>

    <span data-ttu-id="6f8a2-271">バッチ番号 **B11** の数量 **10** が販売注文明細行に対してピッキングされ、**Baydoor** のロケーションに配置されます。</span><span class="sxs-lookup"><span data-stu-id="6f8a2-271">The quantity of **10** for batch number **B11** is now picked for the sales order line and put in the **Baydoor** location.</span></span> <span data-ttu-id="6f8a2-272">この時点で、トラックに積載して、顧客の住所に出荷する準備が整いました。</span><span class="sxs-lookup"><span data-stu-id="6f8a2-272">At this point, it's ready to be loaded onto the truck and dispatched to the customer's address.</span></span>

## <a name="flexible-license-plate-reservation"></a><span data-ttu-id="6f8a2-273">柔軟なライセンス プレートの引当</span><span class="sxs-lookup"><span data-stu-id="6f8a2-273">Flexible license plate reservation</span></span>

### <a name="business-scenario"></a><span data-ttu-id="6f8a2-274">ビジネス シナリオ</span><span class="sxs-lookup"><span data-stu-id="6f8a2-274">Business scenario</span></span>

<span data-ttu-id="6f8a2-275">このシナリオでは、倉庫管理や作業処理を行い、作業が発生する前に Supply Chain Management の外部にある個々のパレット/コンテナーのレベルでの積荷計画を処理します。</span><span class="sxs-lookup"><span data-stu-id="6f8a2-275">In this scenario, a company uses warehouse management and work processing, and handles load planning at the level of individual pallets/containers outside Supply Chain Management before work is created.</span></span> <span data-ttu-id="6f8a2-276">これらのコンテナーは、在庫分析コードのライセンス プレートで表されます。</span><span class="sxs-lookup"><span data-stu-id="6f8a2-276">These containers are represented by license plates in the inventory dimensions.</span></span> <span data-ttu-id="6f8a2-277">そのため、この方法ではピッキング作業を行う前に、特定のライセンス プレートを事前に販売注文明細行に割り当てる必要があります。</span><span class="sxs-lookup"><span data-stu-id="6f8a2-277">Therefore, for this approach, specific license plates must be pre-assigned to sales order lines before picking work is done.</span></span> <span data-ttu-id="6f8a2-278">ライセンス プレートの引当ルールの扱いに柔軟性を求めているため、次のような事象が発生します :</span><span class="sxs-lookup"><span data-stu-id="6f8a2-278">The company is looking for flexibility in the way that the license plate reservation rules are handled, so that the following behaviors occur:</span></span>

- <span data-ttu-id="6f8a2-279">ライセンス プレートは、販売処理者が注文を受けた際に記録して引当することができ、他の用途では取得できません。</span><span class="sxs-lookup"><span data-stu-id="6f8a2-279">A license plate can be recorded and reserved when the order is taken by the sales processor, and it can't be taken by other demands.</span></span> <span data-ttu-id="6f8a2-280">この動作により、計画されたライセンス プレートが顧客に出荷されることが保証されます。</span><span class="sxs-lookup"><span data-stu-id="6f8a2-280">This behavior helps guarantee that the license plate that was planned is shipped to the customer.</span></span>
- <span data-ttu-id="6f8a2-281">ライセンス プレートが販売注文明細行に割り当てられていない場合は、販売注文の登録および引当が完了した後、倉庫の担当者がピッキング作業中にライセンス プレートを選択することができます。</span><span class="sxs-lookup"><span data-stu-id="6f8a2-281">If the license plate isn't already assigned to a sales order line, warehouse personnel can select a license plate during picking work, after sales order registration and reservation are completed.</span></span>

### <a name="turn-on-flexible-license-plate-reservation"></a><span data-ttu-id="6f8a2-282">柔軟なライセンス プレートの引当を有効化する</span><span class="sxs-lookup"><span data-stu-id="6f8a2-282">Turn on flexible license plate reservation</span></span>

<span data-ttu-id="6f8a2-283">柔軟なライセンス プレートの引当を利用する前に、システムで2つの機能を有効化しておく必要があります。</span><span class="sxs-lookup"><span data-stu-id="6f8a2-283">Before you can use flexible license plate reservation, two features must be turned on in your system.</span></span> <span data-ttu-id="6f8a2-284">管理者は、[機能の管理](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md)設定を使用して、機能の状態を確認し、必要に応じて有効化することができます。</span><span class="sxs-lookup"><span data-stu-id="6f8a2-284">Admins can use the [feature management](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) settings to check the status of the features and turn them on if they are required.</span></span> <span data-ttu-id="6f8a2-285">これら機能は、次の順序で有効にする必要があります :</span><span class="sxs-lookup"><span data-stu-id="6f8a2-285">You must turn on the features in the following order:</span></span>

1. <span data-ttu-id="6f8a2-286">**機能名 :** *柔軟な倉庫レベル分析コードの引当ポリシー*</span><span class="sxs-lookup"><span data-stu-id="6f8a2-286">**Feature name:** *Flexible warehouse-level dimension reservation*</span></span>
1. <span data-ttu-id="6f8a2-287">**機能名 :** *柔軟な注文 - コミットされたライセンス プレートの引当*</span><span class="sxs-lookup"><span data-stu-id="6f8a2-287">**Feature name:** *Flexible order-committed license plate reservation*</span></span>

### <a name="reserve-a-specific-license-plate-on-the-sales-order"></a><span data-ttu-id="6f8a2-288">販売注文に基づく特定のライセンス プレートの引当</span><span class="sxs-lookup"><span data-stu-id="6f8a2-288">Reserve a specific license plate on the sales order</span></span>

<span data-ttu-id="6f8a2-289">注文に基づくライセンス プレートの引当を有効にするには、関連するアイテムに関連付けられている階層の **在庫引当階層** ページで、**ライセンスプレート** レベルの **オンデマンド引当を許可する** チェック ボックスを選択する必要があります。</span><span class="sxs-lookup"><span data-stu-id="6f8a2-289">To enable license plate reservation on an order, you must select the **Allow reservation on demand order** check box for the **License plate** level on the **Inventory reservation hierarchies** page for the hierarchy that is associated with the relevant item.</span></span>

![柔軟なライセンス プレートの引当階層で使用する在庫引当階層ページ](media/Flexible-LP-reservation-hierarchy.png)

<span data-ttu-id="6f8a2-291">デプロイのどの時点であっても、注文時にライセンス プレートの引当を有効化できます。</span><span class="sxs-lookup"><span data-stu-id="6f8a2-291">You can enable license plate reservation on the order at any point in your deployment.</span></span> <span data-ttu-id="6f8a2-292">この変更は、変更が発生する前に作成された引当や未処理の倉庫作業には影響しません。</span><span class="sxs-lookup"><span data-stu-id="6f8a2-292">This change won't affect any reservations or open warehouse work that were created before the change occurred.</span></span> <span data-ttu-id="6f8a2-293">ただし、その予約階層に関連付けられている1つ以上のアイテムに対して、*注文中*、*引当済注文*、または *引当済現物* の発行ステータスを持つ、処理中の在庫出荷トランザクションが存在する場合は、**オンデマンド引当を許可する** チェック ボックスをクリアすることはできません。</span><span class="sxs-lookup"><span data-stu-id="6f8a2-293">However, you can't clear the **Allow reservation on demand order** check box if open outbound inventory transactions that have an issue status of *On order*, *Reserved ordered*, or *Reserved physical* exist for one or more items that are associated with that reservation hierarchy.</span></span>

<span data-ttu-id="6f8a2-294">**ライセンス プレート** レベルで **オンデマンド引当を許可する** のチェックボックスがオンの場合であっても、注文に対して特定のライセンス プレートを引当 *しない* ことは可能です。</span><span class="sxs-lookup"><span data-stu-id="6f8a2-294">Even if the **Allow reservation on demand order** check box is selected for the **License plate** level, it's still possible *not* to reserve a specific license plate on the order.</span></span> <span data-ttu-id="6f8a2-295">この場合、引当階層に対して有効な既定の倉庫の運用ロジックが適用されます。</span><span class="sxs-lookup"><span data-stu-id="6f8a2-295">In this case, the default warehouse operations logic that is valid for the reservation hierarchy applies.</span></span>

<span data-ttu-id="6f8a2-296">特定のライセンス プレートを予約するには、[Open Data Protocol (OData)](../../fin-ops-core/dev-itpro/data-entities/odata.md)プロセスを使用する必要があります。アプリケーションでは、**Excelで開く** コマンドの **ライセンス プレートごとの注文コミット引当** オプションを使用して、販売注文から直接的に引当を行うことができます。</span><span class="sxs-lookup"><span data-stu-id="6f8a2-296">To reserve a specific license plate, you must use an [Open Data Protocol (OData)](../../fin-ops-core/dev-itpro/data-entities/odata.md) process.In the application, you can do this reservation directly from a sales order by using the **Order-committed reservations per license plate** option of the **Open in Excel** command.</span></span> <span data-ttu-id="6f8a2-297">Excel アドインで開いたエンティティ データでは、次の引当に関連するデータを入力し、**発行** を選択して、Supply Chain Managementにデータを返送する必要があります :</span><span class="sxs-lookup"><span data-stu-id="6f8a2-297">In the entity data that is opened in the Excel add-in, you must enter the following reservation-related data and then select **Publish** to send the data back to Supply Chain Management:</span></span>

- <span data-ttu-id="6f8a2-298">参照 (*販売注文* の値のみに対応しています)</span><span class="sxs-lookup"><span data-stu-id="6f8a2-298">Reference (Only the *Sales order* value is supported.)</span></span>
- <span data-ttu-id="6f8a2-299">注文番号 (値はロットから派生させることができます)</span><span class="sxs-lookup"><span data-stu-id="6f8a2-299">Order number (The value can be derived from the lot.)</span></span>
- <span data-ttu-id="6f8a2-300">ロット ID</span><span class="sxs-lookup"><span data-stu-id="6f8a2-300">Lot ID</span></span>
- <span data-ttu-id="6f8a2-301">ライセンス プレート</span><span class="sxs-lookup"><span data-stu-id="6f8a2-301">License plate</span></span>
- <span data-ttu-id="6f8a2-302">件数</span><span class="sxs-lookup"><span data-stu-id="6f8a2-302">Quantity</span></span>

<span data-ttu-id="6f8a2-303">一括追跡された特定のライセンス プレートを引当する必要がある場合は、[販売注文の詳細を入力する](#sales-order-details)の項目に記載されているように、**バッチ引当** ページを使用してください。</span><span class="sxs-lookup"><span data-stu-id="6f8a2-303">If you must reserve a specific license plate for a batch-tracked item, use the **Batch reservation** page, as described in the [Enter sales order details](#sales-order-details) section.</span></span>

<span data-ttu-id="6f8a2-304">倉庫業務で注文でコミットされたライセンス プレートの引当を使用した販売注文明細行が処理されている場合、ロケーションの指示は使用されません。</span><span class="sxs-lookup"><span data-stu-id="6f8a2-304">When the sales order line that uses an order-committed license plate reservation is processed by warehouse operations, location directives aren't used.</span></span>

<span data-ttu-id="6f8a2-305">倉庫の作業項目が完全なパレットと同じラインで構成されており、ライセンス プレートがコミットされた数量である場合、モバイル デバイスのメニュー項目を使用して、**ライセンス プレートで処理する** オプションが *はい* に設定することで、ピッキング プロセスを最適化できます。</span><span class="sxs-lookup"><span data-stu-id="6f8a2-305">If a warehouse work item consists of lines that equal a complete pallet and have license plate–committed quantities, you can optimize the picking process by using a mobile device menu item where the **Handle by license plate** option is set to *Yes*.</span></span> <span data-ttu-id="6f8a2-306">その後、倉庫の作業員は、作業中の品目をつずつスキャンする代わりに、ライセンス プレートをスキャンしてピック作業を完了させることができます。</span><span class="sxs-lookup"><span data-stu-id="6f8a2-306">A warehouse worker can then scan a license plate to complete a pick instead of having to scan the items from the work one by one.</span></span>

![[ライセンス プレートで処理する]オプションが「はい」に設定されているモバイル デバイスのメニュー項目](media/Handle-by-LP-menu-item.png)

<span data-ttu-id="6f8a2-308">**ライセンス プレートで処理する** 機能では複数のパレットを対象とする作業に対応していないため、ライセンス プレートごとに別の作業項目を用意することをお勧めします。</span><span class="sxs-lookup"><span data-stu-id="6f8a2-308">Because the **Handle by license plate** functionality doesn't support work that covers multiple pallets, it's better to have a separate work item for different license plates.</span></span> <span data-ttu-id="6f8a2-309">この方法を使用するには、**作業テンプレート** ページの作業ヘッダーの区切りに、**注文がコミットされたライセンス プレートの ID** のフィールドを追加します。</span><span class="sxs-lookup"><span data-stu-id="6f8a2-309">To use this approach, add the **Order-committed license plate ID** field as a work header break on the **Work template** page.</span></span>

> [!NOTE]
> <span data-ttu-id="6f8a2-310">注文がコミットされた作業作成プロセスでは、"注文がコミットされた在庫分析コード" 値はピッキング作業明細行に割り当てられ、ライセンス プレート値を直接表示することはできません。</span><span class="sxs-lookup"><span data-stu-id="6f8a2-310">For the order-committed work creation process, an "order-committed inventory dimension" value will be assigned to the picking work lines, and it won't be possible to view the license plate value directly.</span></span> <span data-ttu-id="6f8a2-311">モバイル デバイスのメニュー項目を設定する場合は、*ユーザー主導* プロセスのみがサポートされます。</span><span class="sxs-lookup"><span data-stu-id="6f8a2-311">Only the *User directed* process is supported when setting up a mobile device menu item.</span></span>

## <a name="example-scenario-set-up-and-process-an-order-committed-license-plate-reservation"></a><span data-ttu-id="6f8a2-312">シナリオ例 : 注文をコミットしてライセンス プレートの引当を設定して処理する</span><span class="sxs-lookup"><span data-stu-id="6f8a2-312">Example scenario: Set up and process an order-committed license plate reservation</span></span>

<span data-ttu-id="6f8a2-313">このシナリオでは、注文がコミットされたライセンス プレートの引当を設定して処理する方法を説明します。</span><span class="sxs-lookup"><span data-stu-id="6f8a2-313">This scenario shows how to set up and process an order-committed license plate reservation.</span></span>

### <a name="make-demo-data-available"></a><span data-ttu-id="6f8a2-314">デモ データを有効化する</span><span class="sxs-lookup"><span data-stu-id="6f8a2-314">Make demo data available</span></span>

<span data-ttu-id="6f8a2-315">このシナリオでは、Supply Chain Management に向けて提供されている標準のデモデータに含まれる値とレコードを参照しています。</span><span class="sxs-lookup"><span data-stu-id="6f8a2-315">This scenario refers to values and records that are included in the standard demo data that is provided for Supply Chain Management.</span></span> <span data-ttu-id="6f8a2-316">ここで提供されている値を使ってシナリオを進める場合は、必ずデモ データがインストールされている環境で作業を行ってください。</span><span class="sxs-lookup"><span data-stu-id="6f8a2-316">If you want to work through the scenario by using the values that are provided here, be sure to work on an environment where the demo data is installed.</span></span> <span data-ttu-id="6f8a2-317">また、開始する前に法人を **USMF** に設定しておく必要があります。</span><span class="sxs-lookup"><span data-stu-id="6f8a2-317">Additionally, set the legal entity to **USMF** before you begin.</span></span>

### <a name="create-an-inventory-reservation-hierarchy-that-allows-for-license-plate-reservation"></a><span data-ttu-id="6f8a2-318">ライセンス プレートの引当を許可する在庫引当の階層を作成する</span><span class="sxs-lookup"><span data-stu-id="6f8a2-318">Create an inventory reservation hierarchy that allows for license plate reservation</span></span>

1. <span data-ttu-id="6f8a2-319">**倉庫管理 \> 設定 \> 在庫 \> 引当階層** に移動します。</span><span class="sxs-lookup"><span data-stu-id="6f8a2-319">Go to **Warehouse management \> Setup \> Inventory \> Reservation hierarchy**.</span></span>
1. <span data-ttu-id="6f8a2-320">**新規** を選択します。</span><span class="sxs-lookup"><span data-stu-id="6f8a2-320">Select **New**.</span></span>
1. <span data-ttu-id="6f8a2-321">**名前** フィールドに、値を入力します (例 : *FlexibleLP*)。</span><span class="sxs-lookup"><span data-stu-id="6f8a2-321">In the **Name** field, enter a value (for example, *FlexibleLP*).</span></span>
1. <span data-ttu-id="6f8a2-322">**説明** フィールドに、値を入力します (例 : *柔軟な LP 引当*)。</span><span class="sxs-lookup"><span data-stu-id="6f8a2-322">In the **Description** field, enter a value (for example, *Flexible LP reservation*).</span></span>
1. <span data-ttu-id="6f8a2-323">**選択済** 一覧で、 **バッチ番号**、**シリアル番号**、**所有者** を選択します。</span><span class="sxs-lookup"><span data-stu-id="6f8a2-323">In the **Selected** list, select **Batch number**, **Serial number**, and **Owner**.</span></span>
1. <span data-ttu-id="6f8a2-324">**削除** ボタン![後向き矢印](media/backward-button.png) を選択して、フィールドを **利用可能** 一覧に移動します。</span><span class="sxs-lookup"><span data-stu-id="6f8a2-324">Select the **Remove** button ![backward arrow](media/backward-button.png) to move the selected records to the **Available** list.</span></span>
1. <span data-ttu-id="6f8a2-325">**OK** を選択します。</span><span class="sxs-lookup"><span data-stu-id="6f8a2-325">Select **OK**.</span></span>
1. <span data-ttu-id="6f8a2-326">**ライセンス プレート** 分析コード レベルの行で、**オンデマンド引当を許可する** チェック ボックスを選択します。</span><span class="sxs-lookup"><span data-stu-id="6f8a2-326">In the row for the **License plate** dimension level, select the **Allow reservation on demand order** check box.</span></span> <span data-ttu-id="6f8a2-327">**ロケーション** レベルは自動的に選択されるため、チェック ボックスをクリアすることはできません。</span><span class="sxs-lookup"><span data-stu-id="6f8a2-327">The **Location** level is automatically selected, and you can't clear the check box for it.</span></span>
1. <span data-ttu-id="6f8a2-328">**保存** を選択します。</span><span class="sxs-lookup"><span data-stu-id="6f8a2-328">Select **Save**.</span></span>

### <a name="create-two-released-products"></a><span data-ttu-id="6f8a2-329">リリース済製品を2つ作成する</span><span class="sxs-lookup"><span data-stu-id="6f8a2-329">Create two released products</span></span>

1. <span data-ttu-id="6f8a2-330">**製品管理情報 \> 製品 \> リリースされた製品** の順に移動します。</span><span class="sxs-lookup"><span data-stu-id="6f8a2-330">Go to **Product information management \> Products \> Released products**.</span></span>
1. <span data-ttu-id="6f8a2-331">アクション ウィンドウで、**新規** を選択します。</span><span class="sxs-lookup"><span data-stu-id="6f8a2-331">On the Action Pane, select **New**.</span></span>
1. <span data-ttu-id="6f8a2-332">**新製品** ダイアログ ボックスに次の値を設定します :</span><span class="sxs-lookup"><span data-stu-id="6f8a2-332">In the **New released product** dialog box, set the following values:</span></span>

    - <span data-ttu-id="6f8a2-333">**製品番号 :** *Item1*</span><span class="sxs-lookup"><span data-stu-id="6f8a2-333">**Product number:** *Item1*</span></span>
    - <span data-ttu-id="6f8a2-334">**品目番号:** *Item1*</span><span class="sxs-lookup"><span data-stu-id="6f8a2-334">**Item number:** *Item1*</span></span>
    - <span data-ttu-id="6f8a2-335">**品目モデル グループ :** *FIFO*</span><span class="sxs-lookup"><span data-stu-id="6f8a2-335">**Item model group:** *FIFO*</span></span>
    - <span data-ttu-id="6f8a2-336">**品目グループ :** *Audio*</span><span class="sxs-lookup"><span data-stu-id="6f8a2-336">**Item group:** *Audio*</span></span>
    - <span data-ttu-id="6f8a2-337">**保管分析コード グループ :** *Ware*</span><span class="sxs-lookup"><span data-stu-id="6f8a2-337">**Storage dimension group:** *Ware*</span></span>
    - <span data-ttu-id="6f8a2-338">**追跡用分析コード グループ :** *なし*</span><span class="sxs-lookup"><span data-stu-id="6f8a2-338">**Tracking dimension group:** *None*</span></span>
    - <span data-ttu-id="6f8a2-339">**引当階層:** *FlexibleLP*</span><span class="sxs-lookup"><span data-stu-id="6f8a2-339">**Reservation hierarchy:** *FlexibleLP*</span></span>

1. <span data-ttu-id="6f8a2-340">**OK** を選択して製品を作成し、ダイアログ ボックスを閉じます。</span><span class="sxs-lookup"><span data-stu-id="6f8a2-340">Select **OK** to create the product and close the dialog box.</span></span>
1. <span data-ttu-id="6f8a2-341">新製品が開きます。</span><span class="sxs-lookup"><span data-stu-id="6f8a2-341">The new product is opened.</span></span> <span data-ttu-id="6f8a2-342">**倉庫** クイック タブの **単位の順序グループ ID** フィールドに、*ea* と入力します。</span><span class="sxs-lookup"><span data-stu-id="6f8a2-342">On the **Warehouse** FastTab, set the **Unit sequence group ID** field to *ea*.</span></span>
1. <span data-ttu-id="6f8a2-343">前述の手順を繰り返して、2つ目の製品を同じ設定で作成し、**製品番号** と **品目番号** フィールドを *Item2* に設定します。</span><span class="sxs-lookup"><span data-stu-id="6f8a2-343">Repeat the previous steps to create a second product that has the same settings, but set the **Product number** and **Item number** fields to *Item2*.</span></span>
1. <span data-ttu-id="6f8a2-344">アクション ペインの **在庫の管理** タブの **表示** グループで、**手持ち在庫** を選択します。</span><span class="sxs-lookup"><span data-stu-id="6f8a2-344">On the Action Pane, on the **Manage inventory** tab, in the **View** group, select **On-hand inventory**.</span></span> <span data-ttu-id="6f8a2-345">続いて、**数量調整** を選択します。</span><span class="sxs-lookup"><span data-stu-id="6f8a2-345">Then select **Quantity adjustment**.</span></span>
1. <span data-ttu-id="6f8a2-346">以下の表で指定しているように、新しい品目の手持在庫を調整します。</span><span class="sxs-lookup"><span data-stu-id="6f8a2-346">Adjust the on-hand inventory of the new items as specified in the following table.</span></span>

    | <span data-ttu-id="6f8a2-347">項目</span><span class="sxs-lookup"><span data-stu-id="6f8a2-347">Item</span></span>  | <span data-ttu-id="6f8a2-348">倉庫</span><span class="sxs-lookup"><span data-stu-id="6f8a2-348">Warehouse</span></span> | <span data-ttu-id="6f8a2-349">ロケーション</span><span class="sxs-lookup"><span data-stu-id="6f8a2-349">Location</span></span> | <span data-ttu-id="6f8a2-350">ライセンス プレート</span><span class="sxs-lookup"><span data-stu-id="6f8a2-350">License plate</span></span> | <span data-ttu-id="6f8a2-351">件数</span><span class="sxs-lookup"><span data-stu-id="6f8a2-351">Quantity</span></span> |
    |-------|-----------|----------|---------------|----------|
    | <span data-ttu-id="6f8a2-352">Item1</span><span class="sxs-lookup"><span data-stu-id="6f8a2-352">Item1</span></span> | <span data-ttu-id="6f8a2-353">24</span><span class="sxs-lookup"><span data-stu-id="6f8a2-353">24</span></span>        | <span data-ttu-id="6f8a2-354">FL-010</span><span class="sxs-lookup"><span data-stu-id="6f8a2-354">FL-010</span></span>   | <span data-ttu-id="6f8a2-355">LP01</span><span class="sxs-lookup"><span data-stu-id="6f8a2-355">LP01</span></span>          | <span data-ttu-id="6f8a2-356">10</span><span class="sxs-lookup"><span data-stu-id="6f8a2-356">10</span></span>       |
    | <span data-ttu-id="6f8a2-357">Item1</span><span class="sxs-lookup"><span data-stu-id="6f8a2-357">Item1</span></span> | <span data-ttu-id="6f8a2-358">24</span><span class="sxs-lookup"><span data-stu-id="6f8a2-358">24</span></span>        | <span data-ttu-id="6f8a2-359">FL-011</span><span class="sxs-lookup"><span data-stu-id="6f8a2-359">FL-011</span></span>   | <span data-ttu-id="6f8a2-360">LP02</span><span class="sxs-lookup"><span data-stu-id="6f8a2-360">LP02</span></span>          | <span data-ttu-id="6f8a2-361">10</span><span class="sxs-lookup"><span data-stu-id="6f8a2-361">10</span></span>       |
    | <span data-ttu-id="6f8a2-362">Item2</span><span class="sxs-lookup"><span data-stu-id="6f8a2-362">Item2</span></span> | <span data-ttu-id="6f8a2-363">24</span><span class="sxs-lookup"><span data-stu-id="6f8a2-363">24</span></span>        | <span data-ttu-id="6f8a2-364">FL-010</span><span class="sxs-lookup"><span data-stu-id="6f8a2-364">FL-010</span></span>   | <span data-ttu-id="6f8a2-365">LP01</span><span class="sxs-lookup"><span data-stu-id="6f8a2-365">LP01</span></span>          | <span data-ttu-id="6f8a2-366">5</span><span class="sxs-lookup"><span data-stu-id="6f8a2-366">5</span></span>        |
    | <span data-ttu-id="6f8a2-367">Item2</span><span class="sxs-lookup"><span data-stu-id="6f8a2-367">Item2</span></span> | <span data-ttu-id="6f8a2-368">24</span><span class="sxs-lookup"><span data-stu-id="6f8a2-368">24</span></span>        | <span data-ttu-id="6f8a2-369">FL-011</span><span class="sxs-lookup"><span data-stu-id="6f8a2-369">FL-011</span></span>   | <span data-ttu-id="6f8a2-370">LP02</span><span class="sxs-lookup"><span data-stu-id="6f8a2-370">LP02</span></span>          | <span data-ttu-id="6f8a2-371">5</span><span class="sxs-lookup"><span data-stu-id="6f8a2-371">5</span></span>        |

    > [!NOTE]
    > <span data-ttu-id="6f8a2-372">2つのライセンス プレートを作成し、*FL-010* や *FL-011* などの混合品目を許容するロケーションを使用する必要があり ます。</span><span class="sxs-lookup"><span data-stu-id="6f8a2-372">You must create the two license plates and use locations that allow for mixed items, such as *FL-010* and *FL-011*.</span></span>

### <a name="create-a-sales-order-and-reserve-a-specific-license-plate"></a><span data-ttu-id="6f8a2-373">販売注文を作成して特定のライセンス プレートを引当する</span><span class="sxs-lookup"><span data-stu-id="6f8a2-373">Create a sales order and reserve a specific license plate</span></span>

1. <span data-ttu-id="6f8a2-374">**販売とマーケティング \> 販売注文 \> すべての販売注文** の順に移動します。</span><span class="sxs-lookup"><span data-stu-id="6f8a2-374">Go to **Sales and marketing \> Sales orders \> All sales orders**.</span></span>
1. <span data-ttu-id="6f8a2-375">**新規** を選択します。</span><span class="sxs-lookup"><span data-stu-id="6f8a2-375">Select **New**.</span></span>
1. <span data-ttu-id="6f8a2-376">**販売注文の作成** ダイアログ ボックスでは、次の値を設定します。</span><span class="sxs-lookup"><span data-stu-id="6f8a2-376">In the **Create sales order** dialog box, set the following values:</span></span>

    - <span data-ttu-id="6f8a2-377">**顧客アカウント:** *US-001*</span><span class="sxs-lookup"><span data-stu-id="6f8a2-377">**Customer account:** *US-001*</span></span>
    - <span data-ttu-id="6f8a2-378">**倉庫:** *24*</span><span class="sxs-lookup"><span data-stu-id="6f8a2-378">**Warehouse:** *24*</span></span>

1. <span data-ttu-id="6f8a2-379">**OK** を選択して **販売注文の作成** ダイアログ ボックスを閉じ、新規販売注文を開きます。</span><span class="sxs-lookup"><span data-stu-id="6f8a2-379">Select **OK** to close the **Create sales order** dialog box and open the new sales order.</span></span>
1. <span data-ttu-id="6f8a2-380">**販売注文明細行** クイックタブで、次の設定で明細行を追加します :</span><span class="sxs-lookup"><span data-stu-id="6f8a2-380">On the **Sales order lines** FastTab, add a line that has the following settings:</span></span>

    - <span data-ttu-id="6f8a2-381">**品目番号:** *Item1*</span><span class="sxs-lookup"><span data-stu-id="6f8a2-381">**Item number:** *Item1*</span></span>
    - <span data-ttu-id="6f8a2-382">**数量:** *10*</span><span class="sxs-lookup"><span data-stu-id="6f8a2-382">**Quantity:** *10*</span></span>

1. <span data-ttu-id="6f8a2-383">以下の設定で 2 つ目の販売注文明細行を作成します :</span><span class="sxs-lookup"><span data-stu-id="6f8a2-383">Add a second sales order line that has the following settings:</span></span>

    - <span data-ttu-id="6f8a2-384">**品目番号:** *Item2*</span><span class="sxs-lookup"><span data-stu-id="6f8a2-384">**Item number:** *Item2*</span></span>
    - <span data-ttu-id="6f8a2-385">**数量:** *5*</span><span class="sxs-lookup"><span data-stu-id="6f8a2-385">**Quantity:** *5*</span></span>

1. <span data-ttu-id="6f8a2-386">**保存** を選択します。</span><span class="sxs-lookup"><span data-stu-id="6f8a2-386">Select **Save**.</span></span>
1. <span data-ttu-id="6f8a2-387">**明細行の詳細** クイックタブの **設定** タブで、各行の **ロット ID** の値をメモします。</span><span class="sxs-lookup"><span data-stu-id="6f8a2-387">On the **Line details** FastTab, on the **Setup** tab, make a note of the **Lot ID** value for each line.</span></span> <span data-ttu-id="6f8a2-388">これらの値は、該当するライセンス プレートの引当時に必要になります。</span><span class="sxs-lookup"><span data-stu-id="6f8a2-388">These values will be required during reservation of specific license plates.</span></span>

    > [!NOTE]
    > <span data-ttu-id="6f8a2-389">特定のライセンス プレートを引当するには、**ライセンス プレートごとに注文がコミットされた引当** のデータエンティティを使用する必要があり ます。</span><span class="sxs-lookup"><span data-stu-id="6f8a2-389">To reserve a specific license plate, you must use the **Order-committed reservations per license plate** data entity.</span></span> <span data-ttu-id="6f8a2-390">特定のライセンス  プレートでバッチ引当をするには、[販売注文の詳細を入力する](#sales-order-details)セクションで説明されているとおり、**バッチ引当** ページを利用することもできます。</span><span class="sxs-lookup"><span data-stu-id="6f8a2-390">To reserve a batch-tracked item on a specific license plate, you can also use the **Batch reservation** page, as described in the [Enter sales order details](#sales-order-details) section.</span></span>
    >
    > <span data-ttu-id="6f8a2-391">ライセンス プレートを販売注文明細行に直接入力してシステムに確認した場合、その明細行には倉庫管理の処理は使用されません。</span><span class="sxs-lookup"><span data-stu-id="6f8a2-391">If you enter the license plate directly on the sales order line and confirm it to the system, warehouse management processing won't be used for the line.</span></span>

1. <span data-ttu-id="6f8a2-392">**Microsoft Office で開く** を選択し、**ライセンス プレートごとに注文がコミットされた引当** を選択し、ファイルをダウンロードします。</span><span class="sxs-lookup"><span data-stu-id="6f8a2-392">Select **Open in Microsoft Office**, select **Order-committed reservations per license plate**, and download the file.</span></span>
1. <span data-ttu-id="6f8a2-393">ファイルをダウンロードして Excel で開き、**編集機能を有効にする** を選択し、Excel アドインが実行されるようにします。</span><span class="sxs-lookup"><span data-stu-id="6f8a2-393">Open the downloaded file in Excel, and select **Enable editing** to enable the Excel add-in to run.</span></span>
1. <span data-ttu-id="6f8a2-394">初めて Excel アドインを実行する場合は、**このアドインを信頼します** を選択します。</span><span class="sxs-lookup"><span data-stu-id="6f8a2-394">If you're running the Excel add-in for the first time, select **Trust this Add-in**.</span></span>
1. <span data-ttu-id="6f8a2-395">サインインを促すメッセージが表示されたら、**サインイン** を選択し、Supply Chain Management へのサインインで使用しているものと同じ資格情報を用いてサインインします。</span><span class="sxs-lookup"><span data-stu-id="6f8a2-395">If you're prompted to sign in, select **Sign in**, and then sign in by using the same credentials that you used to sign in to Supply Chain Management.</span></span>
1. <span data-ttu-id="6f8a2-396">特定のライセンスプレートで品目を引当するには、Excelアドインで、**新規** を選択して引当明細行を追加し、次の値を設定します :</span><span class="sxs-lookup"><span data-stu-id="6f8a2-396">To reserve an item on a specific license plate, in the Excel add-in, select **New** to add a reservation line, and then set the following values:</span></span>

    - <span data-ttu-id="6f8a2-397">**ロット ID :** *Item1* の販売注文明細行の **ロット ID** の値を入力します。</span><span class="sxs-lookup"><span data-stu-id="6f8a2-397">**Lot ID:** Enter the **Lot ID** value that you found for the sales order line for *Item1*.</span></span>
    - <span data-ttu-id="6f8a2-398">**ライセンス プレート :** *LP02*</span><span class="sxs-lookup"><span data-stu-id="6f8a2-398">**License plate:** *LP02*</span></span>
    - <span data-ttu-id="6f8a2-399">**ReservedInventoryQuantity:** *10*</span><span class="sxs-lookup"><span data-stu-id="6f8a2-399">**ReservedInventoryQuantity:** *10*</span></span>

1. <span data-ttu-id="6f8a2-400">**新規** を選択して別の引当明細行を追加し、次の値を設定します :</span><span class="sxs-lookup"><span data-stu-id="6f8a2-400">Select **New** to add another reservation line, and set the following values:</span></span>

    - <span data-ttu-id="6f8a2-401">**ロット ID :** *Item2* の販売注文明細行の **ロット ID** の値を入力します。</span><span class="sxs-lookup"><span data-stu-id="6f8a2-401">**Lot ID:** Enter the **Lot ID** value you found for the sales order line for *Item2*.</span></span>
    - <span data-ttu-id="6f8a2-402">**ライセンス プレート :** *LP02*</span><span class="sxs-lookup"><span data-stu-id="6f8a2-402">**License plate:** *LP02*</span></span>
    - <span data-ttu-id="6f8a2-403">**ReservedInventoryQuantity:** *5*</span><span class="sxs-lookup"><span data-stu-id="6f8a2-403">**ReservedInventoryQuantity:** *5*</span></span>

1. <span data-ttu-id="6f8a2-404">Excel アドインで Supply Chain Management にデータを返送するには、**発行** を選択します。</span><span class="sxs-lookup"><span data-stu-id="6f8a2-404">In the Excel add-in, select **Publish** to send the data back to Supply Chain Management.</span></span>

    > [!NOTE]
    > <span data-ttu-id="6f8a2-405">引当明細行は、エラーなく発行が完了した場合にのみ、システムに表示されます。</span><span class="sxs-lookup"><span data-stu-id="6f8a2-405">The reservation line will appear in the system only if publishing is completed without errors.</span></span>

1. <span data-ttu-id="6f8a2-406">Supply Chain Management に戻ります。</span><span class="sxs-lookup"><span data-stu-id="6f8a2-406">Go back to Supply Chain Management.</span></span> 
1. <span data-ttu-id="6f8a2-407">品目の引当を確認するには、**販売注文明細行** クイックタブの、**在庫** メニューで、**管理 \> 引当** を選択します。</span><span class="sxs-lookup"><span data-stu-id="6f8a2-407">To review the item's reservation, on the **Sales order lines** FastTab, on the **Inventory** menu, select **Maintain \> Reservation**.</span></span> <span data-ttu-id="6f8a2-408">*Item1* の販売注文明細行では、在庫のうち *10* が引当されており、*Item2* の販売注文明細行では、在庫のうち *5* が引当されていることに注意してください。</span><span class="sxs-lookup"><span data-stu-id="6f8a2-408">Notice that, for the sales order line for *Item1*, inventory of *10* is reserved, and for the sales order line for *Item2*, inventory of *5* is reserved.</span></span>
1. <span data-ttu-id="6f8a2-409">販売注文明細行の引当に関連する在庫トランザクションを確認するには、**販売注文明細行** クイックタブの **在庫** メニューで **表示 \> トランザクション** を選択します。</span><span class="sxs-lookup"><span data-stu-id="6f8a2-409">To review inventory transactions that are related to the sales order line reservation, on the **Sales order lines** FastTab, on the **Inventory** menu, select **View \> Transactions**.</span></span> <span data-ttu-id="6f8a2-410">引当に関連する2つのトランザクションが存在することに注目してください : ひとつは **参照** フィールドが *販売注文* に設定されているもので、もうひとつは **参照** フィールドが *注文がコミットされた引当* に設定されているものです。</span><span class="sxs-lookup"><span data-stu-id="6f8a2-410">Notice that there are two transactions that are related to the reservation: one where the **Reference** field is set to *Sales order* and one where the **Reference** field is set to *Order-committed reservation*.</span></span>

    > [!NOTE]
    > <span data-ttu-id="6f8a2-411">**参照** フィールドが *販売注文* に設定されているトランザクションは、**ロケーション** レベル (サイト、倉庫、在庫状況) 以上の在庫分析コードの注文明細行の引当を表しています。</span><span class="sxs-lookup"><span data-stu-id="6f8a2-411">A transaction where the **Reference** field is set to *Sales order* represents the order line reservation for inventory dimensions that are above the **Location** level (site, warehouse, and inventory status).</span></span> <span data-ttu-id="6f8a2-412">**参照** フィールドが、*注文がコミットされた引当* に設定されているトランザクションは、特定のライセンス プレートとロケーションに対する注文明細行の引当を表しています。</span><span class="sxs-lookup"><span data-stu-id="6f8a2-412">A transaction where the **Reference** field is set to *Order-committed reservation* represents the order line reservation for the specific license plate and location.</span></span>

1. <span data-ttu-id="6f8a2-413">販売注文をリリースするには、**アクション** グループ内の **倉庫** タブのアクション ペインで、**倉庫へのリリース** を選択します。</span><span class="sxs-lookup"><span data-stu-id="6f8a2-413">To release the sales order, on the Action Pane, on the **Warehouse** tab, in the **Actions** group, select **Release to warehouse**.</span></span>

### <a name="review-and-process-warehouse-work-with-order-committed-license-plates-assigned"></a><span data-ttu-id="6f8a2-414">注文がコミットされたライセンス プレートを割り当てられた倉庫作業の確認とプロセス</span><span class="sxs-lookup"><span data-stu-id="6f8a2-414">Review and process warehouse work with order-committed license plates assigned</span></span>

1. <span data-ttu-id="6f8a2-415">**販売注文明細行** クイック タブの **倉庫** メニューで、**作業詳細** を選択します。</span><span class="sxs-lookup"><span data-stu-id="6f8a2-415">On the **Sales order lines** FastTab, on the **Warehouse** menu, select **Work details**.</span></span>

    <span data-ttu-id="6f8a2-416">特定のバッチ引当の場合、ライセンス プレートの引当を利用した販売注文の作業を作成する際に、システムはロケーションの指示を利用しません。</span><span class="sxs-lookup"><span data-stu-id="6f8a2-416">As when reservation is done for a specific batch, the system doesn't use location directives when it creates the work for the sales order that uses license plate reservation.</span></span> <span data-ttu-id="6f8a2-417">注文がコミットされた引当では、ロケーションを含むすべての在庫の分析コードが指定されているため、ロケーションの指示を利用する必要はありません。</span><span class="sxs-lookup"><span data-stu-id="6f8a2-417">Because the order-committed reservation specifies all the inventory dimensions, including the location, location directives don't have to be used, because those inventory dimensions are just entered in the work.</span></span> <span data-ttu-id="6f8a2-418">これらは、**作業在庫取引** ページの **在庫分析コード** のセクションに表示されています。</span><span class="sxs-lookup"><span data-stu-id="6f8a2-418">They are shown in the **From inventory dimensions** section on the **Work inventory transactions** page.</span></span>

    > [!NOTE]
    > <span data-ttu-id="6f8a2-419">作業の作成後は、**参照** フィールドが *注文がコミットされた引当* に設定されている品目の在庫トランザクションが削除されます。</span><span class="sxs-lookup"><span data-stu-id="6f8a2-419">After the work is created, the item's inventory transaction where the **Reference** field is set to *Order-committed reservation* is removed.</span></span> <span data-ttu-id="6f8a2-420">**参照** フィールドが *作業* に設定されている在庫トランザクションは、すべての数量の在庫分析コードに対して現物引当を保持するようになります。</span><span class="sxs-lookup"><span data-stu-id="6f8a2-420">The inventory transaction where the **Reference** field is set to *Work* now holds the physical reservation for all the quantity's inventory dimensions.</span></span>

1. <span data-ttu-id="6f8a2-421">モバイル デバイスで、**ライセンス プレートで処理する** チェック ボックスがオンになっているメニュー項目を使用してピッキングと作業を完了します。</span><span class="sxs-lookup"><span data-stu-id="6f8a2-421">On the mobile device, finish picking and putting the work by using a menu item where the **Handle by license plate** check box is selected.</span></span>

    > [!NOTE]
    > <span data-ttu-id="6f8a2-422">**ライセンス プレートで処理する** 機能は、ライセンス プレート全体を処理する場合に役立ちます。</span><span class="sxs-lookup"><span data-stu-id="6f8a2-422">The **Handle by license plate** functionality helps you process the whole license plate.</span></span> <span data-ttu-id="6f8a2-423">ライセンスプレートの一部のみを処理する必要がある場合は、この機能を使用できません。</span><span class="sxs-lookup"><span data-stu-id="6f8a2-423">If you must process part of the license plate, you can't use this functionality.</span></span>
    >
    > <span data-ttu-id="6f8a2-424">ライセンス プレートごとに徳利手下の作業を生成することを推奨します。</span><span class="sxs-lookup"><span data-stu-id="6f8a2-424">We recommend that you have separate work generated for each license plate.</span></span> <span data-ttu-id="6f8a2-425">この結果を得るには、**作業テンプレート** ページの **作業用ヘッダーの区切り** 機能を使用し ます。</span><span class="sxs-lookup"><span data-stu-id="6f8a2-425">To achieve this result, use the **Work header breaks** feature on the **Work template** page.</span></span>

    <span data-ttu-id="6f8a2-426">ライセン スプレート *LP02* は、販売注文明細行でピッキングされ、ロケーション *Baydoor* に配置されます。</span><span class="sxs-lookup"><span data-stu-id="6f8a2-426">License plate *LP02* is now picked for sales order lines and put to the *Baydoor* location.</span></span> <span data-ttu-id="6f8a2-427">以上で積み込み準備と顧客への出荷準備が整いました。</span><span class="sxs-lookup"><span data-stu-id="6f8a2-427">At this point, it's ready to be loaded and dispatched to the customer.</span></span>

## <a name="exception-handling-of-warehouse-work-that-has-order-committed-batch-numbers"></a><span data-ttu-id="6f8a2-428">注文が確定したバッチ番号を持つ倉庫作業の例外処理</span><span class="sxs-lookup"><span data-stu-id="6f8a2-428">Exception handling of warehouse work that has order-committed batch numbers</span></span>

<span data-ttu-id="6f8a2-429">注文が確定したバッチ番号をピッキングする倉庫作業には、通常の作業と同じ標準の倉庫例外処理とアクションが適用されます。</span><span class="sxs-lookup"><span data-stu-id="6f8a2-429">Warehouse work for picking order-committed batch numbers is subject to the same standard warehouse exception handling and actions as regular work.</span></span> <span data-ttu-id="6f8a2-430">一般に、オープン作業または作業明細行はキャンセルされたり、ユーザーのロケーションがいっぱいになったために中断されたり、ショート ピッキングされたり、移動のために更新される可能性があります。</span><span class="sxs-lookup"><span data-stu-id="6f8a2-430">In general, the open work or work line can be canceled, it can be interrupted because a user location is full, it can be short-picked, and it can be updated because of a movement.</span></span> <span data-ttu-id="6f8a2-431">同様に、既に完了した作業のピッキング済数量を減らすことも、または作業を取り消すこともできます。</span><span class="sxs-lookup"><span data-stu-id="6f8a2-431">Likewise, the picked quantity of work that has already been completed can be reduced, or the work can be reversed.</span></span>

<span data-ttu-id="6f8a2-432">これらのすべての例外処理アクションに次の主要なルールが適用されます。顧客に対して引当されているバッチ番号を別のバッチ番号に置き換えられることはありませんが、保管分析コード　(ロケーションおよびライセン スプレート) は、ユーザーによる手動更新またはシステムによる自動更新によって変更できます。</span><span class="sxs-lookup"><span data-stu-id="6f8a2-432">The following key rule is applied to all these exception handling actions: the batch number that was reserved for the customer can never be replaced with a different batch number, but its storage dimensions (location and license plate) can be changed through either a manual update by the user or an automatic update by the system.</span></span> <span data-ttu-id="6f8a2-433">自動更新は、特定のバッチが自動的に引当され、保管分析コードが指定されていない場合に適用される保管分析コードのランダムな割り当てに基づいています。</span><span class="sxs-lookup"><span data-stu-id="6f8a2-433">The automatic update is based on the same random assignment of storage dimensions that applied when a specific batch was automatically reserved but no storage dimensions were specified.</span></span>

### <a name="example-scenario"></a><span data-ttu-id="6f8a2-434">シナリオ例</span><span class="sxs-lookup"><span data-stu-id="6f8a2-434">Example scenario</span></span>

<span data-ttu-id="6f8a2-435">このシナリオの例としては、**ピッキング済数量の削減** 機能を使用して、以前に完了した作業を解除している状況です。</span><span class="sxs-lookup"><span data-stu-id="6f8a2-435">An example of this scenario is a situation where previously completed work is being unpicked by using the **Reduce picked quantity** function.</span></span> <span data-ttu-id="6f8a2-436">この例は、[シナリオ例 : バッチ番号の割り当て](#Example-batch-allocation)で説明されている手順が既に完了していることを前提としています。</span><span class="sxs-lookup"><span data-stu-id="6f8a2-436">This example assumes that you've already completed the steps that are described in [Example scenario: Batch number allocation](#Example-batch-allocation).</span></span> <span data-ttu-id="6f8a2-437">ここでは、そのシナリオ例の続きを行います。</span><span class="sxs-lookup"><span data-stu-id="6f8a2-437">It continues from that example.</span></span>

1. <span data-ttu-id="6f8a2-438">**倉庫管理** \> **積荷** \> **有効な積荷** に移動します。</span><span class="sxs-lookup"><span data-stu-id="6f8a2-438">Go to **Warehouse management** \> **Loads** \> **Active loads**.</span></span>
2. <span data-ttu-id="6f8a2-439">販売注文の出荷に関連して作成された積荷を選択します。</span><span class="sxs-lookup"><span data-stu-id="6f8a2-439">Select the load that was created in connection with the shipment of your sales order.</span></span>
3. <span data-ttu-id="6f8a2-440">**積荷注文明細行数** クイック タブから、**ピッキング済数量の削減** を選択します。</span><span class="sxs-lookup"><span data-stu-id="6f8a2-440">From the **Load order lines** FastTab, select **Reduce picked quantity**.</span></span>
4. <span data-ttu-id="6f8a2-441">**ピッキング済数量の削減** ページの **ロケーションに移動する** フィールドで、**FL-001** を選択します。</span><span class="sxs-lookup"><span data-stu-id="6f8a2-441">On the **Reduce picked quantity** page, in the **Move to location** field, select **FL-001**.</span></span>
5. <span data-ttu-id="6f8a2-442">**ライセンス プレートに移動する** フィールドで、**LP33** を選択します。</span><span class="sxs-lookup"><span data-stu-id="6f8a2-442">In the **Move to license plate** field, select **LP33**.</span></span>
6. <span data-ttu-id="6f8a2-443">グリッドで、**ピッキングを解除する在庫数量** フィールドに **10** と入力します。</span><span class="sxs-lookup"><span data-stu-id="6f8a2-443">In the grid, in the **Inventory quantity to unpick** field, enter **10**.</span></span>
7. <span data-ttu-id="6f8a2-444">**OK** を選択します。</span><span class="sxs-lookup"><span data-stu-id="6f8a2-444">Select **OK**.</span></span>

<span data-ttu-id="6f8a2-445">ピッキング解除アクションの実行結果は次のようになります。</span><span class="sxs-lookup"><span data-stu-id="6f8a2-445">Here are the results of the unpicking action:</span></span>

- <span data-ttu-id="6f8a2-446">以前に終了した作業のステータスは、**キャンセル済** に設定されます。</span><span class="sxs-lookup"><span data-stu-id="6f8a2-446">The status of the previously closed work is set to **Canceled**.</span></span>
- <span data-ttu-id="6f8a2-447">バッチ番号 **B11** の **10** のピッキング済ではない数量に対して、**在庫移動** タイプの新しい作業が作成されます。</span><span class="sxs-lookup"><span data-stu-id="6f8a2-447">New work of the **Inventory movement** type is created for the unpicked quantity of **10** for batch number **B11**.</span></span> <span data-ttu-id="6f8a2-448">この作業は、**ベイドア** のロケーションから、**FL-001** のロケーションのライセンス プレート **LP33** への移動を表しています。</span><span class="sxs-lookup"><span data-stu-id="6f8a2-448">This work represents the movement from the **Baydoor** location to license plate **LP33** in location **FL-001**.</span></span> <span data-ttu-id="6f8a2-449">ステータスは **終了済** に設定されます。</span><span class="sxs-lookup"><span data-stu-id="6f8a2-449">The status is set to **Closed**.</span></span>
- <span data-ttu-id="6f8a2-450">システムは、元の注文バッチ番号を再度準備し、ロケーションとライセンス プレート ID を割り当てます。</span><span class="sxs-lookup"><span data-stu-id="6f8a2-450">The system re-reserves the batch number that was originally ordered, and assigns the location and license plate IDs.</span></span> <span data-ttu-id="6f8a2-451">(このプロセスは、指定されたバッチ番号の注文明細行に対して **引当行** 機能を実行することと同じです)。</span><span class="sxs-lookup"><span data-stu-id="6f8a2-451">(This process is equivalent to running the **Reserve line** function for the order line for a given batch number).</span></span> <span data-ttu-id="6f8a2-452">その結果、バッチ **B11** は、**バッチ引当** ページの **ソース明細行に確定済みのバッチ番号** クイック タブに確定済みとして表示され、**引当** フィールドには、バッチ番号 **B11** の数量 **10** が含まれています。</span><span class="sxs-lookup"><span data-stu-id="6f8a2-452">As a result, batch **B11** is shown as committed on the **Batch numbers committed to source line** FastTab of the **Batch reservation** page, and the **Reservation** field contains a quantity of **10** for batch number **B11**.</span></span> <span data-ttu-id="6f8a2-453">さらに、**ロケーション** フィールドは **FL-001** に設定され、**ライセンス プレート** フィールドは **LP11** に設定されます。</span><span class="sxs-lookup"><span data-stu-id="6f8a2-453">Additionally, the **Location** field is set to **FL-001**, and the **License plate** field is set to **LP11**.</span></span> <span data-ttu-id="6f8a2-454">(これらのフィールドが表示されていない場合は、グリッドに追加できます。)</span><span class="sxs-lookup"><span data-stu-id="6f8a2-454">(You can add these fields to the grid if they aren't visible.)</span></span>

<span data-ttu-id="6f8a2-455">次の表は、特定の倉庫アクションの注文が確定したバッチ引当をシステムが処理する方法を示す概要を示しています。</span><span class="sxs-lookup"><span data-stu-id="6f8a2-455">The following tables provide an overview that shows how the system handles order-committed batch reservation for specific warehouse actions.</span></span> <span data-ttu-id="6f8a2-456">テーブルのコンテンツを解釈するには、各倉庫アクションが注文が確定したバッチ引当から発生する既存の倉庫作業のコンテキストで実行されるか、各倉庫アクションの実行がそのタイプの作業に影響すると仮定します。</span><span class="sxs-lookup"><span data-stu-id="6f8a2-456">To interpret the content in the tables, assume that each warehouse action is run in the context of existing warehouse work that originates from an order-committed batch reservation, or that execution of each warehouse action affects work of that type.</span></span>

> [!NOTE]
> <span data-ttu-id="6f8a2-457">これらの表の「バッチ数量が利用可能」列は、現在の注文が確定した引当に対して既に引当されている数量、またはそのタイプの引当から発生する倉庫作業によって既に引当されている数量に加えて、バッチ数量が利用可能かどうかを示します。</span><span class="sxs-lookup"><span data-stu-id="6f8a2-457">In these tables, the "Batch quantity is available" column indicates whether a batch quantity is available in addition to the quantity that is either already reserved for the current order-committed reservations or already reserved by the warehouse work that originates from reservations of that type.</span></span>

#### <a name="override-the-pick-location-on-the-open-work"></a><span data-ttu-id="6f8a2-458">オープン作業のピッキングロケーションを上書きする</span><span class="sxs-lookup"><span data-stu-id="6f8a2-458">Override the pick location on the open work</span></span>

<table>
<thead>
<tr>
<th><span data-ttu-id="6f8a2-459">キー設定パラメーター</span><span class="sxs-lookup"><span data-stu-id="6f8a2-459">Key setup parameter</span></span></th>
<th><span data-ttu-id="6f8a2-460">バッチ数量が利用可能</span><span class="sxs-lookup"><span data-stu-id="6f8a2-460">Batch quantity is available</span></span></th>
<th><span data-ttu-id="6f8a2-461">主要なユーザーの手順</span><span class="sxs-lookup"><span data-stu-id="6f8a2-461">Key user steps</span></span></th>
<th><span data-ttu-id="6f8a2-462">倉庫作業</span><span class="sxs-lookup"><span data-stu-id="6f8a2-462">Warehouse work</span></span></th>
<th><span data-ttu-id="6f8a2-463">注文が確定したバッチ引当</span><span class="sxs-lookup"><span data-stu-id="6f8a2-463">Order-committed batch reservation</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td rowspan='2'><span data-ttu-id="6f8a2-464">作業者で<strong>ピッキングロケーションの上書きを許可</strong>オプションが有効になっている。</span><span class="sxs-lookup"><span data-stu-id="6f8a2-464">The <strong>Allow pick location override</strong> option is enabled on the worker.</span></span></td>
<td><span data-ttu-id="6f8a2-465">有</span><span class="sxs-lookup"><span data-stu-id="6f8a2-465">Yes</span></span></td>
<td>
<ol>
<li><span data-ttu-id="6f8a2-466">ピッキング作業開始時に、倉庫アプリの<strong>ロケーションの上書き</strong>メニュー項目を選択します。</span><span class="sxs-lookup"><span data-stu-id="6f8a2-466">Select the <strong>Override location</strong> menu item on the warehouse app when you start picking work.</span></span></li>
<li><span data-ttu-id="6f8a2-467"><strong>提案</strong>を選択します。</span><span class="sxs-lookup"><span data-stu-id="6f8a2-467">Select <strong>Suggest</strong>.</span></span></li>
<li><span data-ttu-id="6f8a2-468">バッチ数量の使用可能性に基づいて提案される新しいロケーションを確認します。</span><span class="sxs-lookup"><span data-stu-id="6f8a2-468">Confirm the new location that is suggested based on batch quantity availability.</span></span></li>
</ol>
</td>
<td><span data-ttu-id="6f8a2-469">現在の作業では、次のアクションが発生します。</span><span class="sxs-lookup"><span data-stu-id="6f8a2-469">On the current work, the following actions occur:</span></span>
<ul>
<li><span data-ttu-id="6f8a2-470">ピッキング行のロケーションが新しいロケーションに更新されます。</span><span class="sxs-lookup"><span data-stu-id="6f8a2-470">The location on the pick line is updated to the new location.</span></span> <span data-ttu-id="6f8a2-471">(ロケーションがライセンス プレートにより制御されている場合、ランダムなライセンス プレートが作業在庫トランザクションに割り当てられ、作業者は使用可能な数量があるライセンス プレートからピッキングできます。)</span><span class="sxs-lookup"><span data-stu-id="6f8a2-471">(If the location is license plate–controlled, a random license plate is assigned to the work inventory transaction, and the worker can pick from any license plate that has available quantity.)</span></span></li>
<li><span data-ttu-id="6f8a2-472">新しいロケーションで複数のライセンス プレートに数量が見つかった場合、元のピッキング行を複数の行に分割して、各ライセンス プレートに一致させることができます。</span><span class="sxs-lookup"><span data-stu-id="6f8a2-472">If the quantity is found on more than one license plate in the new location, the original pick line is split into multiple lines to match each license plate.</span></span></li>
</ul>
</td>
<td><span data-ttu-id="6f8a2-473">該当なし</span><span class="sxs-lookup"><span data-stu-id="6f8a2-473">Not applicable</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="6f8a2-474">無</span><span class="sxs-lookup"><span data-stu-id="6f8a2-474">No</span></span></td>
<td>
<ol>
<li><span data-ttu-id="6f8a2-475">ピッキング作業開始時に、倉庫アプリの<strong>ロケーションの上書き</strong>メニュー項目を選択します。</span><span class="sxs-lookup"><span data-stu-id="6f8a2-475">Select the <strong>Override location</strong> menu item on the warehouse app when you start picking work.</span></span></li>
<li><span data-ttu-id="6f8a2-476">ロケーションを手動で入力します。</span><span class="sxs-lookup"><span data-stu-id="6f8a2-476">Manually enter a location.</span></span></li>
</ol>
</td>
<td><span data-ttu-id="6f8a2-477"><strong>ロケーションの上書き</strong>アクションは実行できません。</span><span class="sxs-lookup"><span data-stu-id="6f8a2-477">The <strong>Override location</strong> action isn't possible.</span></span> <span data-ttu-id="6f8a2-478">失敗すると、エラーがスローされます。</span><span class="sxs-lookup"><span data-stu-id="6f8a2-478">It fails, and an error is thrown.</span></span></td>
<td><span data-ttu-id="6f8a2-479">適用できません</span><span class="sxs-lookup"><span data-stu-id="6f8a2-479">Not applicable</span></span></td>
</tr>
</tbody>
</table>

#### <a name="full-button--split-a-work-line-because-of-overflow-on-the-user-location"></a><span data-ttu-id="6f8a2-480">フル ボタン - ユーザーのロケーションでオーバーフローしたために作業ラインを分割します</span><span class="sxs-lookup"><span data-stu-id="6f8a2-480">Full button – Split a work line because of overflow on the user location</span></span>

<table>
<thead>
<tr>
<th><span data-ttu-id="6f8a2-481">キー設定パラメーター</span><span class="sxs-lookup"><span data-stu-id="6f8a2-481">Key setup parameter</span></span></th>
<th><span data-ttu-id="6f8a2-482">バッチ数量が利用可能</span><span class="sxs-lookup"><span data-stu-id="6f8a2-482">Batch quantity is available</span></span></th>
<th><span data-ttu-id="6f8a2-483">主要なユーザーの手順</span><span class="sxs-lookup"><span data-stu-id="6f8a2-483">Key user steps</span></span></th>
<th><span data-ttu-id="6f8a2-484">倉庫作業</span><span class="sxs-lookup"><span data-stu-id="6f8a2-484">Warehouse work</span></span></th>
<th><span data-ttu-id="6f8a2-485">注文が確定したバッチ引当</span><span class="sxs-lookup"><span data-stu-id="6f8a2-485">Order-committed batch reservation</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="6f8a2-486">モバイル デバイスのメニュー項目で<strong>作業の分割を許可</strong>オプションが有効になっています。</span><span class="sxs-lookup"><span data-stu-id="6f8a2-486">The <strong>Allow splitting of work</strong> option is enabled on the mobile device menu item.</span></span></td>
<td><span data-ttu-id="6f8a2-487">該当なし</span><span class="sxs-lookup"><span data-stu-id="6f8a2-487">Not applicable</span></span></td>
<td>
<ol>
<li><span data-ttu-id="6f8a2-488">ピッキング作業プロセス時に、倉庫アプリのメニュー項目<strong>フル</strong>を選択します。</span><span class="sxs-lookup"><span data-stu-id="6f8a2-488">Select the <strong>Full</strong> menu item on the warehouse app when you process picking work.</span></span></li>
<li><span data-ttu-id="6f8a2-489"><strong>ピッキング数量</strong>フィールドに、必要なピッキングの一部の数量を入力して、全能力を示します。</span><span class="sxs-lookup"><span data-stu-id="6f8a2-489">In the <strong>Pick Qty</strong> field, enter a partial quantity of the required pick to indicate the full capacity.</span></span></li>
</ol>
</td>
<td>
<ul>
<li><span data-ttu-id="6f8a2-490">現在の作業では、数量はピッキングが必要な残余数量に更新されます。</span><span class="sxs-lookup"><span data-stu-id="6f8a2-490">On the current work, the quantity is updated to the remaining quantity that must be picked.</span></span></li>
<li><span data-ttu-id="6f8a2-491">選択した数量の新しい作業が作成され、決済されます。</span><span class="sxs-lookup"><span data-stu-id="6f8a2-491">New work for the picked quantity is created and closed.</span></span></li>
</ul></td>
<td><span data-ttu-id="6f8a2-492">適用できません</span><span class="sxs-lookup"><span data-stu-id="6f8a2-492">Not applicable</span></span></td>
</tr>
</tbody>
</table>

#### <a name="reduce-the-picked-quantity-of-completed-work-from-a-load"></a><span data-ttu-id="6f8a2-493">完了した作業のピッキング済数量をする (積荷から)</span><span class="sxs-lookup"><span data-stu-id="6f8a2-493">Reduce the picked quantity of completed work (from a load)</span></span>

<table>
<thead>
<tr>
<th><span data-ttu-id="6f8a2-494">キー設定パラメーター</span><span class="sxs-lookup"><span data-stu-id="6f8a2-494">Key setup parameter</span></span></th>
<th><span data-ttu-id="6f8a2-495">バッチ数量が利用可能</span><span class="sxs-lookup"><span data-stu-id="6f8a2-495">Batch quantity is available</span></span></th>
<th><span data-ttu-id="6f8a2-496">主要なユーザーの手順</span><span class="sxs-lookup"><span data-stu-id="6f8a2-496">Key user steps</span></span></th>
<th><span data-ttu-id="6f8a2-497">倉庫作業</span><span class="sxs-lookup"><span data-stu-id="6f8a2-497">Warehouse work</span></span></th>
<th><span data-ttu-id="6f8a2-498">注文が確定したバッチ引当</span><span class="sxs-lookup"><span data-stu-id="6f8a2-498">Order-committed batch reservation</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td rowspan='2'><span data-ttu-id="6f8a2-499">適用できません</span><span class="sxs-lookup"><span data-stu-id="6f8a2-499">Not applicable</span></span></td>
<td><span data-ttu-id="6f8a2-500">はい</span><span class="sxs-lookup"><span data-stu-id="6f8a2-500">Yes</span></span></td>
<td>
<ol>
<li><span data-ttu-id="6f8a2-501">積荷明細行から<strong>ピッキング済数量の削減</strong>ページを開きます。</span><span class="sxs-lookup"><span data-stu-id="6f8a2-501">Open the <strong>Reduce picked quantity</strong> page from the load line.</span></span></li>
<li><span data-ttu-id="6f8a2-502">ピッキングを解除する全数量を入力します。</span><span class="sxs-lookup"><span data-stu-id="6f8a2-502">Enter the full quantity to unpick.</span></span></li>
<li><span data-ttu-id="6f8a2-503">「移動先」のロケーション / ライセンス プレートを選択します。</span><span class="sxs-lookup"><span data-stu-id="6f8a2-503">Select a "move to" location/license plate.</span></span></li>
</ol>
</td>
<td>
<ul> 
<li><span data-ttu-id="6f8a2-504">積荷明細行に関連付けられている作業はキャンセルされます。</span><span class="sxs-lookup"><span data-stu-id="6f8a2-504">Work that is associated with the load line is canceled.</span></span></li>
<li><span data-ttu-id="6f8a2-505">在庫移動の新しい作業が作成され、決済されます。</span><span class="sxs-lookup"><span data-stu-id="6f8a2-505">New work for the inventory movement is created and closed.</span></span></li>
</ul>
</td>
<td><span data-ttu-id="6f8a2-506">この数量は、同じバッチに対して再引当されます。</span><span class="sxs-lookup"><span data-stu-id="6f8a2-506">The quantity is re-reserved for the same batch.</span></span> <span data-ttu-id="6f8a2-507">システムは、数量が使用可能なロケーションとライセンス プレート (ロケーションがライセンス プレートで制御されている場合) をランダムに割り当てます。</span><span class="sxs-lookup"><span data-stu-id="6f8a2-507">The system randomly assigns a location and license plate (if the location is license plate–controlled) where the quantity is available.</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="6f8a2-508">いいえ</span><span class="sxs-lookup"><span data-stu-id="6f8a2-508">No</span></span></td>
<td><span data-ttu-id="6f8a2-509">前の行を参照してください。</span><span class="sxs-lookup"><span data-stu-id="6f8a2-509">See the previous row.</span></span></td>
<td><span data-ttu-id="6f8a2-510">前の行を参照してください。</span><span class="sxs-lookup"><span data-stu-id="6f8a2-510">See the previous row.</span></span></td>
<td><span data-ttu-id="6f8a2-511">数量は、ピッキング中に入力された同じバッチ、および同じロケーション、およびライセンス プレート (ロケーションがライセンス プレートで制御されている場合) に対して再引当されます。</span><span class="sxs-lookup"><span data-stu-id="6f8a2-511">The quantity is re-reserved for the same batch, and for the same location and license plate (if the location is license plate–controlled) that were entered during unpicking.</span></span></td>
</tr>
</tbody>
</table>

#### <a name="move-an-item-within-a-warehouse"></a><span data-ttu-id="6f8a2-512">倉庫内の品目を移動する</span><span class="sxs-lookup"><span data-stu-id="6f8a2-512">Move an item within a warehouse</span></span>

> [!NOTE]
> <span data-ttu-id="6f8a2-513">この倉庫アクションは、**作業作成プロセス** タイプの移動にのみ適用され、テンプレートによる移動には適用されません。</span><span class="sxs-lookup"><span data-stu-id="6f8a2-513">This warehouse action is applicable only to movement of the **Work creation process** type, not to movement by template.</span></span>

<table>
<thead>
<tr>
<th><span data-ttu-id="6f8a2-514">キー設定パラメーター</span><span class="sxs-lookup"><span data-stu-id="6f8a2-514">Key setup parameter</span></span></th>
<th><span data-ttu-id="6f8a2-515">バッチ数量が利用可能</span><span class="sxs-lookup"><span data-stu-id="6f8a2-515">Batch quantity is available</span></span></th>
<th><span data-ttu-id="6f8a2-516">主要なユーザーの手順</span><span class="sxs-lookup"><span data-stu-id="6f8a2-516">Key user steps</span></span></th>
<th><span data-ttu-id="6f8a2-517">倉庫作業</span><span class="sxs-lookup"><span data-stu-id="6f8a2-517">Warehouse work</span></span></th>
<th><span data-ttu-id="6f8a2-518">注文が確定したバッチ引当</span><span class="sxs-lookup"><span data-stu-id="6f8a2-518">Order-committed batch reservation</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td rowspan='2'><span data-ttu-id="6f8a2-519">作業者で、<strong>作業が関連付けられている在庫の移動を許可</strong>オプションが有効になっています。</span><span class="sxs-lookup"><span data-stu-id="6f8a2-519">The <strong>Allow movement of inventory with associated work</strong> option is enabled on the worker.</span></span></td>
<td><span data-ttu-id="6f8a2-520">有</span><span class="sxs-lookup"><span data-stu-id="6f8a2-520">Yes</span></span></td>
<td>
<ol>
<li><span data-ttu-id="6f8a2-521">倉庫アプリで移動を開始します。</span><span class="sxs-lookup"><span data-stu-id="6f8a2-521">Start a movement on the warehouse app.</span></span></li>
<li><span data-ttu-id="6f8a2-522">「移動元」および「移動先」のロケーションを入力します。</span><span class="sxs-lookup"><span data-stu-id="6f8a2-522">Enter "from" and "to" locations.</span></span></li>
</ol></td>
<td>
<ul>
<li><span data-ttu-id="6f8a2-523">移動によって影響を受けるすべての既存の作業について、ピッキングロケーションが新しい「移動先」のロケーションに更新されます。</span><span class="sxs-lookup"><span data-stu-id="6f8a2-523">On all existing work that is affected by the move, the pick location is updated to the new "to" location.</span></span></li>
<li><span data-ttu-id="6f8a2-524">在庫移動の新しい作業が作成され、決済されます。</span><span class="sxs-lookup"><span data-stu-id="6f8a2-524">New work for the inventory movement is created and closed.</span></span></li>
</ul>
</td>
<td><span data-ttu-id="6f8a2-525">特定のロケーションからの数量の移動によって影響を受けるすべての既存の引当は、同じバッチに対して再引当されます。</span><span class="sxs-lookup"><span data-stu-id="6f8a2-525">All existing reservations that are affected by the quantity movement from the given location are re-reserved for the same batch.</span></span> <span data-ttu-id="6f8a2-526">システムは、数量が使用可能なロケーションとライセンス プレート (ロケーションがライセンス プレートで制御されている場合) をランダムに割り当てます。</span><span class="sxs-lookup"><span data-stu-id="6f8a2-526">The system randomly assigns a location and license plate (if the location is license plate–controlled) where the quantity is available.</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="6f8a2-527">いいえ</span><span class="sxs-lookup"><span data-stu-id="6f8a2-527">No</span></span></td>
<td><span data-ttu-id="6f8a2-528">前の行を参照してください。</span><span class="sxs-lookup"><span data-stu-id="6f8a2-528">See the previous row.</span></span></td>
<td><span data-ttu-id="6f8a2-529">前の行を参照してください。</span><span class="sxs-lookup"><span data-stu-id="6f8a2-529">See the previous row.</span></span></td>
<td><span data-ttu-id="6f8a2-530">特定のロケーションからの数量の移動によって影響を受けるすべての既存の引当は、同じバッチ、および新しい「移動先」ロケーションとライセンス プレートに対して再引当されます (ロケーションがライセンス プレートで制御されている場合)。</span><span class="sxs-lookup"><span data-stu-id="6f8a2-530">All existing reservations that are affected by the quantity movement from the given location are re-reserved for the same batch, and for the new "to" location and license plate (if the location is license plate–controlled).</span></span></td>
</tr>
</tbody>
</table>

#### <a name="reverse-the-picked-quantity-of-completed-work-from-a-load-or-a-wave"></a><span data-ttu-id="6f8a2-531">完了した作業のピッキング済数量を取り消す (積荷もしくはウェーブから)</span><span class="sxs-lookup"><span data-stu-id="6f8a2-531">Reverse the picked quantity of completed work (from a load or a wave)</span></span>

<table>
<thead>
<tr>
<th><span data-ttu-id="6f8a2-532">キー設定パラメーター</span><span class="sxs-lookup"><span data-stu-id="6f8a2-532">Key setup parameter</span></span></th>
<th><span data-ttu-id="6f8a2-533">バッチ数量が利用可能</span><span class="sxs-lookup"><span data-stu-id="6f8a2-533">Batch quantity is available</span></span></th>
<th><span data-ttu-id="6f8a2-534">主要なユーザーの手順</span><span class="sxs-lookup"><span data-stu-id="6f8a2-534">Key user steps</span></span></th>
<th><span data-ttu-id="6f8a2-535">倉庫作業</span><span class="sxs-lookup"><span data-stu-id="6f8a2-535">Warehouse work</span></span></th>
<th><span data-ttu-id="6f8a2-536">注文が確定したバッチ引当</span><span class="sxs-lookup"><span data-stu-id="6f8a2-536">Order-committed batch reservation</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td rowspan='6'><span data-ttu-id="6f8a2-537">適用できません</span><span class="sxs-lookup"><span data-stu-id="6f8a2-537">Not applicable</span></span></td>
<td><span data-ttu-id="6f8a2-538">はい</span><span class="sxs-lookup"><span data-stu-id="6f8a2-538">Yes</span></span></td>
<td>
<ol>
<li><span data-ttu-id="6f8a2-539"><strong>作業を取消</strong>ページを開きます。</span><span class="sxs-lookup"><span data-stu-id="6f8a2-539">Open the <strong>Reverse work</strong> page.</span></span></li>
<li><span data-ttu-id="6f8a2-540">要求ページで、<strong>品目を現在のロケーションに配置したままにする</strong>オプションを選択します。</span><span class="sxs-lookup"><span data-stu-id="6f8a2-540">On the request page, select the <strong>Leave items at current location</strong> option.</span></span></li>
</ol>
</td>
<td><span data-ttu-id="6f8a2-541">積荷に関連付けられているすべての作業はキャンセルされます。</span><span class="sxs-lookup"><span data-stu-id="6f8a2-541">All work that is associated with the load is canceled.</span></span></td>
<td><span data-ttu-id="6f8a2-542">この数量は、同じバッチに対して再引当されます。</span><span class="sxs-lookup"><span data-stu-id="6f8a2-542">The quantity is re-reserved for the same batch.</span></span> <span data-ttu-id="6f8a2-543">システムは、数量が使用可能なロケーションとライセンス プレート (ロケーションがライセンス プレートで制御されている場合) をランダムに割り当てます。</span><span class="sxs-lookup"><span data-stu-id="6f8a2-543">The system randomly assigns a location and license plate (if the location is license plate–controlled) where the quantity is available.</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="6f8a2-544">いいえ</span><span class="sxs-lookup"><span data-stu-id="6f8a2-544">No</span></span></td>
<td><span data-ttu-id="6f8a2-545">前の行を参照してください。</span><span class="sxs-lookup"><span data-stu-id="6f8a2-545">See the previous row.</span></span></td>
<td><span data-ttu-id="6f8a2-546">前の行を参照してください。</span><span class="sxs-lookup"><span data-stu-id="6f8a2-546">See the previous row.</span></span></td>
<td><span data-ttu-id="6f8a2-547">数量は、同じバッチ、および取消時に数量が残されたロケーションとライセンス プレートに対して再引当されます。</span><span class="sxs-lookup"><span data-stu-id="6f8a2-547">The quantity is re-reserved for the same batch, and for the location and license plate where the quantity was left upon reversal.</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="6f8a2-548">はい</span><span class="sxs-lookup"><span data-stu-id="6f8a2-548">Yes</span></span></td>
<td>
<ol>
<li><span data-ttu-id="6f8a2-549"><strong>作業を取消</strong>ページを開きます。</span><span class="sxs-lookup"><span data-stu-id="6f8a2-549">Open the <strong>Reverse work</strong> page.</span></span></li>
<li><span data-ttu-id="6f8a2-550">要求ページで、<strong>品目をこのロケーションに割り当てる</strong>オプションを選択します。</span><span class="sxs-lookup"><span data-stu-id="6f8a2-550">On the request page, select the <strong>Assign items to this location</strong> option.</span></span></li>
</ol>
</td>
<td>
<ul>
<li><span data-ttu-id="6f8a2-551">現在の作業はキャンセルされました。</span><span class="sxs-lookup"><span data-stu-id="6f8a2-551">The current work is canceled.</span></span></li>
<li><span data-ttu-id="6f8a2-552">在庫移動の新しい作業が作成され、決済されます。</span><span class="sxs-lookup"><span data-stu-id="6f8a2-552">New work for the inventory movement is created and closed.</span></span></li>
</ul>
</td>
<td><span data-ttu-id="6f8a2-553">この数量は、同じバッチに対して再引当されます。</span><span class="sxs-lookup"><span data-stu-id="6f8a2-553">The quantity is re-reserved for the same batch.</span></span> <span data-ttu-id="6f8a2-554">システムは、数量が使用可能なロケーションとライセンス プレート (ロケーションがライセンス プレートで制御されている場合) をランダムに割り当てます。</span><span class="sxs-lookup"><span data-stu-id="6f8a2-554">The system randomly assigns a location and license plate (if the location is license plate–controlled) where the quantity is available.</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="6f8a2-555">いいえ</span><span class="sxs-lookup"><span data-stu-id="6f8a2-555">No</span></span></td>
<td><span data-ttu-id="6f8a2-556">前の行を参照してください。</span><span class="sxs-lookup"><span data-stu-id="6f8a2-556">See the previous row.</span></span></td>
<td><span data-ttu-id="6f8a2-557">前の行を参照してください。</span><span class="sxs-lookup"><span data-stu-id="6f8a2-557">See the previous row.</span></span></td>
<td><span data-ttu-id="6f8a2-558">数量は、同じバッチ、および取消時に数量が割り当てられたロケーションとライセンス プレートに対して再引当されます。</span><span class="sxs-lookup"><span data-stu-id="6f8a2-558">The quantity is re-reserved for the same batch, and for the location and license plate that the quantity was assigned to upon reversal.</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="6f8a2-559">はい/いいえ</span><span class="sxs-lookup"><span data-stu-id="6f8a2-559">Yes/No</span></span></td>
<td>
<ol>
<li><span data-ttu-id="6f8a2-560"><strong>作業を取消</strong>ページを開きます。</span><span class="sxs-lookup"><span data-stu-id="6f8a2-560">Open the <strong>Reverse work</strong> page.</span></span></li>
<li><span data-ttu-id="6f8a2-561">要求ページで、<strong>品目をこのロケーションに移動する</strong>オプションを選択します。</span><span class="sxs-lookup"><span data-stu-id="6f8a2-561">On the request page, select the <strong>Move items to this location</strong> option.</span></span></li>
</ol>
</td>
<td><span data-ttu-id="6f8a2-562">取消はサポートされていません。</span><span class="sxs-lookup"><span data-stu-id="6f8a2-562">Reversal isn't supported.</span></span></td>
<td><span data-ttu-id="6f8a2-563">適用できません</span><span class="sxs-lookup"><span data-stu-id="6f8a2-563">Not applicable</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="6f8a2-564">はい/いいえ</span><span class="sxs-lookup"><span data-stu-id="6f8a2-564">Yes/No</span></span></td>
<td>
<ol>
<li><span data-ttu-id="6f8a2-565"><strong>作業を取消</strong>ページを開きます。</span><span class="sxs-lookup"><span data-stu-id="6f8a2-565">Open the <strong>Reverse work</strong> page.</span></span></li>
<li><span data-ttu-id="6f8a2-566">要求ページで、<strong>ロケーションの指示に基づいて品目を移動する</strong>オプションを選択します。</span><span class="sxs-lookup"><span data-stu-id="6f8a2-566">On the request page, select the <strong>Move items based on location directives</strong> option.</span></span></li>
</ol>
</td>
<td><span data-ttu-id="6f8a2-567">取消はサポートされていません。</span><span class="sxs-lookup"><span data-stu-id="6f8a2-567">Reversal isn't supported.</span></span> </td>
<td><span data-ttu-id="6f8a2-568">適用できません</span><span class="sxs-lookup"><span data-stu-id="6f8a2-568">Not applicable</span></span></td>
</tr>
</tbody>
</table>

#### <a name="short-pick-a-quantity--register-the-quantity-as-physically-not-found-at-the-locationlicense-plate-while-you-perform-picking-work"></a><span data-ttu-id="6f8a2-569">数量の選択 - ピッキング作業の実行中に、ロケーション / ライセンス プレートでは見つからない数量を登録する</span><span class="sxs-lookup"><span data-stu-id="6f8a2-569">Short-pick a quantity – Register the quantity as physically not found at the location/license plate while you perform picking work</span></span>

<table>
<thead>
<tr>
<th><span data-ttu-id="6f8a2-570">キー設定パラメーター</span><span class="sxs-lookup"><span data-stu-id="6f8a2-570">Key setup parameter</span></span></th>
<th><span data-ttu-id="6f8a2-571">バッチ数量が利用可能</span><span class="sxs-lookup"><span data-stu-id="6f8a2-571">Batch quantity is available</span></span></th>
<th><span data-ttu-id="6f8a2-572">主要なユーザーの手順</span><span class="sxs-lookup"><span data-stu-id="6f8a2-572">Key user steps</span></span></th>
<th><span data-ttu-id="6f8a2-573">倉庫作業</span><span class="sxs-lookup"><span data-stu-id="6f8a2-573">Warehouse work</span></span></th>
<th><span data-ttu-id="6f8a2-574">注文が確定したバッチ引当</span><span class="sxs-lookup"><span data-stu-id="6f8a2-574">Order-committed batch reservation</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td rowspan='2'><span data-ttu-id="6f8a2-575"><strong>品目再配賦</strong> = <strong>なし</strong>、<strong>在庫の調整</strong> = <strong>はい</strong>、および<strong>引当の削除</strong> = <strong>いいえ</strong>で、<strong>ショートピック</strong> タイプの作業例外が設定されています。</span><span class="sxs-lookup"><span data-stu-id="6f8a2-575">A work exception of the <strong>Short pick</strong> type is set up, where <strong>Item reallocation</strong> = <strong>None</strong>, <strong>Adjust inventory</strong> = <strong>Yes</strong>, and <strong>Remove reservations</strong> = <strong>No</strong>.</span></span></td>
<td><span data-ttu-id="6f8a2-576">有</span><span class="sxs-lookup"><span data-stu-id="6f8a2-576">Yes</span></span></td>
<td>
<ol>
<li><span data-ttu-id="6f8a2-577">ピッキング作業のプロセス時に、倉庫アプリのメニュー項目<strong>ショート ピック</strong>を選択します。</span><span class="sxs-lookup"><span data-stu-id="6f8a2-577">Select the <strong>Shortpick</strong> menu item on the warehouse app when you run picking work.</span></span></li>
<li><span data-ttu-id="6f8a2-578"><strong>ピック数量</strong>フィールドに <strong>0</strong> (ゼロ) と入力します。</span><span class="sxs-lookup"><span data-stu-id="6f8a2-578">In the <strong>Pick Quantity</strong> field, enter <strong>0</strong> (zero).</span></span></li>
<li><span data-ttu-id="6f8a2-579"><strong>理由</strong>フィールドに、<strong>非再配賦</strong>と入力します。</span><span class="sxs-lookup"><span data-stu-id="6f8a2-579">In the <strong>Reason</strong> field, enter <strong>No reallocation</strong>.</span></span></li>
</ol>
</td>
<td>
<ul>
<li><span data-ttu-id="6f8a2-580">現在の作業は終了済で、ピッキング済数量は 0 (ゼロ) です。</span><span class="sxs-lookup"><span data-stu-id="6f8a2-580">The current work is closed, and the picked quantity is 0 (zero).</span></span></li>
<li><span data-ttu-id="6f8a2-581"><strong>棚卸</strong>タイプの在庫トランザクションおよび<strong>売却</strong>出庫タイプの在庫トランザクションが作成され、調整を表します。</span><span class="sxs-lookup"><span data-stu-id="6f8a2-581">An inventory transaction of the <strong>Counting</strong> type and the <strong>Sold</strong> issue type is created to represent the adjustment.</span></span></li>
</ul>
</td>
<td><span data-ttu-id="6f8a2-582">この数量は、同じバッチに対して再引当されます。</span><span class="sxs-lookup"><span data-stu-id="6f8a2-582">The quantity is re-reserved for the same batch.</span></span> <span data-ttu-id="6f8a2-583">システムは、数量が使用可能なロケーションとライセンス プレート (ロケーションがライセンス プレートで制御されている場合) をランダムに割り当てます。</span><span class="sxs-lookup"><span data-stu-id="6f8a2-583">The system randomly assigns a location and license plate (if the location is license plate–controlled) where the quantity is available.</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="6f8a2-584">いいえ</span><span class="sxs-lookup"><span data-stu-id="6f8a2-584">No</span></span></td>
<td><span data-ttu-id="6f8a2-585">前の行を参照してください。</span><span class="sxs-lookup"><span data-stu-id="6f8a2-585">See the previous row.</span></span></td>
<td>
<ul>
<li><span data-ttu-id="6f8a2-586">ショートピッキング アクションの実行に失敗し、エラーがスローされます。</span><span class="sxs-lookup"><span data-stu-id="6f8a2-586">The short-picking action fails, and an error is thrown.</span></span></li>
<li><span data-ttu-id="6f8a2-587">現在の作業は開いたままになります。</span><span class="sxs-lookup"><span data-stu-id="6f8a2-587">The current work remains open.</span></span></li>
</ul>
</td>
<td><span data-ttu-id="6f8a2-588">適用できません</span><span class="sxs-lookup"><span data-stu-id="6f8a2-588">Not applicable</span></span></td>
</tr>
<tr>
<td rowspan='2'><span data-ttu-id="6f8a2-589"><strong>品目再配賦</strong> = <strong>なし</strong>、<strong>在庫の調整</strong> = <strong>はい</strong>、および<strong>引当の削除</strong> = <strong>はい</strong>で、<strong>ショートピック</strong> タイプの作業例外が設定されています。</span><span class="sxs-lookup"><span data-stu-id="6f8a2-589">A work exception of the <strong>Short pick</strong> type is set up, where <strong>Item reallocation</strong> = <strong>None</strong>, <strong>Adjust inventory</strong> = <strong>Yes</strong>, and <strong>Remove reservations</strong> = <strong>Yes</strong>.</span></span></td>
<td><span data-ttu-id="6f8a2-590">有</span><span class="sxs-lookup"><span data-stu-id="6f8a2-590">Yes</span></span></td>
<td>
<ol>
<li><span data-ttu-id="6f8a2-591">ピッキング作業のプロセス時に、倉庫アプリのメニュー項目<strong>ショート ピック</strong>を選択します。</span><span class="sxs-lookup"><span data-stu-id="6f8a2-591">Select the <strong>Shortpick</strong> menu item on the warehouse app when you run picking work.</span></span></li>
<li><span data-ttu-id="6f8a2-592"><strong>ピック数量</strong>フィールドに <strong>0</strong> (ゼロ) と入力します。</span><span class="sxs-lookup"><span data-stu-id="6f8a2-592">In the <strong>Pick Quantity</strong> field, enter <strong>0</strong> (zero).</span></span></li>
<li><span data-ttu-id="6f8a2-593"><strong>理由</strong>フィールドに、<strong>非再配賦</strong>と入力します。</span><span class="sxs-lookup"><span data-stu-id="6f8a2-593">In the <strong>Reason</strong> field, enter <strong>No reallocation</strong>.</span></span></li>
</ol>
</td>
<td>
<ul>
<li><span data-ttu-id="6f8a2-594">現在の作業は終了済で、ピッキング済数量は 0 (ゼロ) です。</span><span class="sxs-lookup"><span data-stu-id="6f8a2-594">The current work is closed, and the picked quantity is 0 (zero).</span></span></li>
<li><span data-ttu-id="6f8a2-595"><strong>棚卸</strong>タイプの在庫トランザクションおよび<strong>売却</strong>出庫タイプの在庫トランザクションが作成され、調整を表します。</span><span class="sxs-lookup"><span data-stu-id="6f8a2-595">An inventory transaction of the <strong>Counting</strong> type and the <strong>Sold</strong> issue type is created to represent the adjustment.</span></span></li>
</ul>
</td>
<td><span data-ttu-id="6f8a2-596">簡単なピッキングロケーションからの数量の調整によって影響を受けるすべての既存の引当は、同じバッチに対して再引当されます。</span><span class="sxs-lookup"><span data-stu-id="6f8a2-596">All existing reservations that are affected by the quantity adjustment in the short-picked location are re-reserved for the same batch.</span></span> <span data-ttu-id="6f8a2-597">システムは、数量が使用可能なロケーションとライセンス プレート (ロケーションがライセンス プレートで制御されている場合) をランダムに割り当てます。</span><span class="sxs-lookup"><span data-stu-id="6f8a2-597">The system randomly assigns a location and license plate (if the location is license plate–controlled) where the quantity is available.</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="6f8a2-598">いいえ</span><span class="sxs-lookup"><span data-stu-id="6f8a2-598">No</span></span></td>
<td><span data-ttu-id="6f8a2-599">前の行を参照してください。</span><span class="sxs-lookup"><span data-stu-id="6f8a2-599">See the previous row.</span></span></td>
<td><span data-ttu-id="6f8a2-600">前の行を参照してください。</span><span class="sxs-lookup"><span data-stu-id="6f8a2-600">See the previous row.</span></span></td>
<td><span data-ttu-id="6f8a2-601">簡単なピッキングロケーションからの数量の調整によって影響を受けるすべての既存の引当は、削除されました。</span><span class="sxs-lookup"><span data-stu-id="6f8a2-601">All existing reservations that are affected by the quantity adjustment in the short-picked location are removed.</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="6f8a2-602"><strong>品目再配賦</strong> = <strong>手動</strong>、<strong>在庫の調整</strong> = <strong>はい</strong>、および<strong>引当の削除</strong> = <strong>いいえ / はい</strong>で、<strong>ショートピック</strong> タイプの作業例外が設定されています。</span><span class="sxs-lookup"><span data-stu-id="6f8a2-602">A work exception of the <strong>Short pick</strong> type is set up, where <strong>Item reallocation</strong> = <strong>Manual</strong>, <strong>Adjust inventory</strong> = <strong>Yes</strong>, and <strong>Remove reservations</strong> = <strong>No/Yes</strong>.</span></span> <span data-ttu-id="6f8a2-603">さらに、作業者で<strong>手動による再配置を許可</strong>オプションが有効になります。</span><span class="sxs-lookup"><span data-stu-id="6f8a2-603">Additionally, the <strong>Allow manual item reallocation</strong> option is enabled on the worker.</span></span></td>
<td><span data-ttu-id="6f8a2-604">有</span><span class="sxs-lookup"><span data-stu-id="6f8a2-604">Yes</span></span></td>
<td>
<ol>
<li><span data-ttu-id="6f8a2-605">ピッキング作業のプロセス時に、倉庫アプリのメニュー項目<strong>ショート ピック</strong>を選択します。</span><span class="sxs-lookup"><span data-stu-id="6f8a2-605">Select the <strong>Shortpick</strong> menu item on the warehouse app when you run picking work.</span></span></li>
<li><span data-ttu-id="6f8a2-606"><strong>ショートピック数量</strong>フィールドに <strong>0</strong> (ゼロ) と入力します。</span><span class="sxs-lookup"><span data-stu-id="6f8a2-606">In the <strong>Shortpick Quantity</strong> field, enter <strong>0</strong> (zero).</span></span></li>
<li><span data-ttu-id="6f8a2-607"><strong>理由</strong>フィールドで、<strong>手動での再配分を使用したショートピッキング</strong>を選択します。</span><span class="sxs-lookup"><span data-stu-id="6f8a2-607">In the <strong>Reason</strong> field, select <strong>Short Picking with manual reallocation</strong>.</span></span></li>
<li><span data-ttu-id="6f8a2-608">一覧からロケーション / ライセンス プレートを選択します。</span><span class="sxs-lookup"><span data-stu-id="6f8a2-608">Select the location/license plate in the list.</span></span></li>
</ol>
</td>
<td>
<ul>
<li><span data-ttu-id="6f8a2-609">現在の作業では、次のアクションが発生します。</span><span class="sxs-lookup"><span data-stu-id="6f8a2-609">On the current work, the following actions occur:</span></span>
<ul>
<li><span data-ttu-id="6f8a2-610">ピッキング行は終了済で、ピッキング済数量は 0 (ゼロ) です。</span><span class="sxs-lookup"><span data-stu-id="6f8a2-610">The pick line is closed, and the picked quantity is 0 (zero).</span></span></li>
<li><span data-ttu-id="6f8a2-611">プット明細行はキャンセルされました。</span><span class="sxs-lookup"><span data-stu-id="6f8a2-611">The put line is canceled.</span></span></li>
<li><span data-ttu-id="6f8a2-612">新しいピック行が作成されました。</span><span class="sxs-lookup"><span data-stu-id="6f8a2-612">A new pick line is created.</span></span> <span data-ttu-id="6f8a2-613">ユーザーによって選択されたロケーション / ライセンス プレートを使用します。</span><span class="sxs-lookup"><span data-stu-id="6f8a2-613">It uses the location/license plate that the user selected.</span></span></li>
<li><span data-ttu-id="6f8a2-614">新しいプット明細行が作成されました。</span><span class="sxs-lookup"><span data-stu-id="6f8a2-614">A new put line is created.</span></span></li>
</ul>
</li>
<li><span data-ttu-id="6f8a2-615"><strong>棚卸</strong>タイプの在庫トランザクションおよび<strong>売却</strong>出庫タイプの在庫トランザクションが作成され、調整を表します。</span><span class="sxs-lookup"><span data-stu-id="6f8a2-615">An inventory transaction of the <strong>Counting</strong> type and the <strong>Sold</strong> issue type is created to represent the adjustment.</span></span></li>
</ul>
</td>
<td><span data-ttu-id="6f8a2-616">適用できません</span><span class="sxs-lookup"><span data-stu-id="6f8a2-616">Not applicable</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="6f8a2-617"><strong>品目再配賦</strong> = <strong>手動</strong>、<strong>在庫の調整</strong> = <strong>はい</strong>、および<strong>引当の削除</strong> = <strong>いいえ</strong>で、<strong>ショートピック</strong> タイプの作業例外が設定されています。</span><span class="sxs-lookup"><span data-stu-id="6f8a2-617">A work exception of the <strong>Short pick</strong> type is set up, where <strong>Item reallocation</strong> = <strong>Manual</strong>, <strong>Adjust inventory</strong> = <strong>Yes</strong>, and <strong>Remove reservations</strong> = <strong>No</strong>.</span></span> <span data-ttu-id="6f8a2-618">さらに、作業者で<strong>手動による再配置を許可</strong>オプションが有効になります。</span><span class="sxs-lookup"><span data-stu-id="6f8a2-618">Additionally, the <strong>Allow manual item reallocation</strong> option is enabled on the worker.</span></span></td>
<td><span data-ttu-id="6f8a2-619">無</span><span class="sxs-lookup"><span data-stu-id="6f8a2-619">No</span></span></td>
<td>
<ol>
<li><span data-ttu-id="6f8a2-620">ピッキング作業のプロセス時に、倉庫アプリのメニュー項目<strong>ショート ピック</strong>を選択します。</span><span class="sxs-lookup"><span data-stu-id="6f8a2-620">Select the <strong>Shortpick</strong> menu item on the warehouse app when you run picking work.</span></span></li>
<li><span data-ttu-id="6f8a2-621"><strong>ショートピック数量</strong>フィールドに <strong>0</strong> (ゼロ) と入力します。</span><span class="sxs-lookup"><span data-stu-id="6f8a2-621">In the <strong>Shortpick Quantity</strong> field, enter <strong>0</strong> (zero).</span></span></li>
<li><span data-ttu-id="6f8a2-622"><strong>理由</strong>フィールドで、<strong>手動での再配分を使用したショートピッキング</strong>を選択します。</span><span class="sxs-lookup"><span data-stu-id="6f8a2-622">In the <strong>Reason</strong> field, select <strong>Short Picking with manual reallocation</strong>.</span></span></li>
</ol>
</td>
<td><span data-ttu-id="6f8a2-623">ショートピッキング アクションの実行に失敗し、エラーがスローされます。</span><span class="sxs-lookup"><span data-stu-id="6f8a2-623">The short-picking action fails, and an error is thrown.</span></span></td>
<td><span data-ttu-id="6f8a2-624">適用できません</span><span class="sxs-lookup"><span data-stu-id="6f8a2-624">Not applicable</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="6f8a2-625"><strong>品目再配賦</strong> = <strong>手動</strong>、<strong>在庫の調整</strong> = <strong>はい</strong>、および<strong>引当の削除</strong> = <strong>はい</strong>で、<strong>ショートピック</strong> タイプの作業例外が設定されています。</span><span class="sxs-lookup"><span data-stu-id="6f8a2-625">A work exception of the <strong>Short pick</strong> type is set up, where <strong>Item reallocation</strong> = <strong>Manual</strong>, <strong>Adjust inventory</strong> = <strong>Yes</strong>, and <strong>Remove reservations</strong> = <strong>Yes</strong>.</span></span> <span data-ttu-id="6f8a2-626">さらに、作業者で<strong>手動による再配置を許可</strong>オプションが有効になります。</span><span class="sxs-lookup"><span data-stu-id="6f8a2-626">Additionally, the <strong>Allow manual item reallocation</strong> option is enabled on the worker.</span></span></td>
<td><span data-ttu-id="6f8a2-627">無</span><span class="sxs-lookup"><span data-stu-id="6f8a2-627">No</span></span></td>
<td>
<ol>
<li><span data-ttu-id="6f8a2-628">ピッキング作業のプロセス時に、倉庫アプリのメニュー項目<strong>ショート ピック</strong>を選択します。</span><span class="sxs-lookup"><span data-stu-id="6f8a2-628">Select the <strong>Shortpick</strong> menu item on the warehouse app when you run picking work.</span></span></li>
<li><span data-ttu-id="6f8a2-629"><strong>ショートピック数量</strong>フィールドに <strong>0</strong> (ゼロ) と入力します。</span><span class="sxs-lookup"><span data-stu-id="6f8a2-629">In the <strong>Shortpick Quantity</strong> field, enter <strong>0</strong> (zero).</span></span></li>
<li><span data-ttu-id="6f8a2-630"><strong>理由</strong>フィールドで、<strong>手動での再配分を使用したショートピッキング</strong>を選択します。</span><span class="sxs-lookup"><span data-stu-id="6f8a2-630">In the <strong>Reason</strong> field, select <strong>Short Picking with manual reallocation</strong>.</span></span></li>
<li><span data-ttu-id="6f8a2-631">一覧からロケーション / ライセンス プレートを選択します。</span><span class="sxs-lookup"><span data-stu-id="6f8a2-631">Select the location/license plate in the list.</span></span></li>
</ol>
</td>
<td>
<ul>
<li><span data-ttu-id="6f8a2-632">現在の作業では、次のアクションが発生します。</span><span class="sxs-lookup"><span data-stu-id="6f8a2-632">On the current work, the following actions occur:</span></span>
<ul>
<li><span data-ttu-id="6f8a2-633">ピッキング行は終了済で、ピッキング済数量は 0 (ゼロ) です。</span><span class="sxs-lookup"><span data-stu-id="6f8a2-633">The pick line is closed, and the picked quantity is 0 (zero).</span></span></li>
<li><span data-ttu-id="6f8a2-634">プット明細行はキャンセルされました。</span><span class="sxs-lookup"><span data-stu-id="6f8a2-634">The put line is canceled.</span></span></li>
</ul>
</li>
<li><span data-ttu-id="6f8a2-635"><strong>棚卸</strong>タイプの在庫トランザクションおよび<strong>売却</strong>出庫タイプの在庫トランザクションが作成され、調整を表します。</span><span class="sxs-lookup"><span data-stu-id="6f8a2-635">An inventory transaction of the <strong>Counting</strong> type and the <strong>Sold</strong> issue type is created to represent the adjustment.</span></span></li>
</ul>
</td>
<td><span data-ttu-id="6f8a2-636">簡単なピッキング ロケーション / ライセンス プレートからの数量の調整によって影響を受けるすべての既存の引当は、削除されました。</span><span class="sxs-lookup"><span data-stu-id="6f8a2-636">All existing reservations that are affected by the quantity adjustment in the short-picked location/license plate are removed.</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="6f8a2-637"><strong>品目再配賦</strong> = <strong>自動</strong>、<strong>在庫の調整</strong> = <strong>はい / いいえ</strong>、および<strong>引当の削除</strong> = <strong>はい / いいえ</strong>で、<strong>ショートピック</strong> タイプの作業例外が設定されています。</span><span class="sxs-lookup"><span data-stu-id="6f8a2-637">A work exception of the <strong>Short pick</strong> type is set up, where <strong>Item reallocation</strong> = <strong>Automatic</strong>, <strong>Adjust inventory</strong> = <strong>Yes/No</strong>, and <strong>Remove reservations</strong> = <strong>Yes/No</strong>.</span></span></td>
<td><span data-ttu-id="6f8a2-638">該当なし</span><span class="sxs-lookup"><span data-stu-id="6f8a2-638">Not applicable</span></span></td>
<td>
<ol>
<li><span data-ttu-id="6f8a2-639">ピッキング作業のプロセス時に、倉庫アプリのメニュー項目<strong>ショート ピック</strong>を選択します。</span><span class="sxs-lookup"><span data-stu-id="6f8a2-639">Select the <strong>Shortpick</strong> menu item on the warehouse app when you run picking work.</span></span></li>
<li><span data-ttu-id="6f8a2-640"><strong>ショートピック数量</strong>フィールドに <strong>0</strong> (ゼロ) と入力します。</span><span class="sxs-lookup"><span data-stu-id="6f8a2-640">In the <strong>Shortpick Quantity</strong> field, enter <strong>0</strong> (zero).</span></span></li>
<li><span data-ttu-id="6f8a2-641"><strong>理由</strong>フィールドで、<strong>自動での再配分を使用したショートピッキング</strong>を選択します。</span><span class="sxs-lookup"><span data-stu-id="6f8a2-641">In the <strong>Reason</strong> field, select <strong>Short Picking with automatic reallocation</strong>.</span></span></li>
</ol>
</td>
<td><span data-ttu-id="6f8a2-642">自動再割り当てを含むショートピッキングはサポートされていません。</span><span class="sxs-lookup"><span data-stu-id="6f8a2-642">Short-picking that involves automatic reallocation isn't supported.</span></span></td>
<td><span data-ttu-id="6f8a2-643">自動再割り当てを含むショートピッキングはサポートされていません。</span><span class="sxs-lookup"><span data-stu-id="6f8a2-643">Short-picking that involves automatic reallocation isn't supported.</span></span></td>
</tr>
</tbody>
</table>

#### <a name="change-the-inventory-status"></a><span data-ttu-id="6f8a2-644">在庫状態の変更</span><span class="sxs-lookup"><span data-stu-id="6f8a2-644">Change the inventory status</span></span>

> [!NOTE]
> <span data-ttu-id="6f8a2-645">この倉庫アクションは複数のエントリ ポイントから実行できます。</span><span class="sxs-lookup"><span data-stu-id="6f8a2-645">This warehouse action can be performed from multiple entry points.</span></span> <span data-ttu-id="6f8a2-646">ここに表示されている例では、**ロケーションごとの手持在庫** ページで **在庫状態の変更** アクションを使用しています。</span><span class="sxs-lookup"><span data-stu-id="6f8a2-646">The example that is shown here uses **Inventory status change** action on the **On-hand by location** page.</span></span>

<table>
<thead>
<tr>
<th><span data-ttu-id="6f8a2-647">キー設定パラメーター</span><span class="sxs-lookup"><span data-stu-id="6f8a2-647">Key setup parameter</span></span></th>
<th><span data-ttu-id="6f8a2-648">バッチ数量が利用可能</span><span class="sxs-lookup"><span data-stu-id="6f8a2-648">Batch quantity is available</span></span></th>
<th><span data-ttu-id="6f8a2-649">主要なユーザーの手順</span><span class="sxs-lookup"><span data-stu-id="6f8a2-649">Key user steps</span></span></th>
<th><span data-ttu-id="6f8a2-650">倉庫作業</span><span class="sxs-lookup"><span data-stu-id="6f8a2-650">Warehouse work</span></span></th>
<th><span data-ttu-id="6f8a2-651">注文が確定したバッチ引当</span><span class="sxs-lookup"><span data-stu-id="6f8a2-651">Order-committed batch reservation</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td rowspan='2'><span data-ttu-id="6f8a2-652"><strong>倉庫</strong>タブの<strong>倉庫</strong>レコードで、<strong>引当とマーキングの削除</strong>フィールドが<strong>引当</strong>または<strong>マーキングと引当</strong>に設定されます。</span><span class="sxs-lookup"><span data-stu-id="6f8a2-652">On the <strong>Warehouse</strong> tab, in the <strong>Warehouse</strong> record, the <strong>Remove reservations and markings</strong> field is set to <strong>Reservations</strong> or <strong>Markings and reservations</strong>.</span></span></td>
<td><span data-ttu-id="6f8a2-653">はい</span><span class="sxs-lookup"><span data-stu-id="6f8a2-653">Yes</span></span></td>
<td>
<ol>
<li><span data-ttu-id="6f8a2-654">特定のロケーションを選択します。</span><span class="sxs-lookup"><span data-stu-id="6f8a2-654">Select a specific location.</span></span></li>
<li><span data-ttu-id="6f8a2-655">特定の品目、ロケーション、およびライセンス プレートがある明細行を選択します (ロケーションがライセンス プレートにより制御されている場合)。</span><span class="sxs-lookup"><span data-stu-id="6f8a2-655">Select a line that has a specific item, location, and license plate (if the location is license plate–controlled).</span></span></li>
<li><span data-ttu-id="6f8a2-656"><strong>在庫状態の変更</strong>を選択します。</span><span class="sxs-lookup"><span data-stu-id="6f8a2-656">Select <strong>Inventory status change</strong>.</span></span></li>
<li><span data-ttu-id="6f8a2-657"><strong>在庫状態</strong>フィールドを<strong>ブロック</strong>に設定します。</span><span class="sxs-lookup"><span data-stu-id="6f8a2-657">Set the <strong>Inventory status</strong> field to <strong>Blocking</strong>.</span></span></li>
</ol>
</td>
<td><span data-ttu-id="6f8a2-658">作業用に引き当てられている数量に対して、在庫状態の変更は許可されていません。</span><span class="sxs-lookup"><span data-stu-id="6f8a2-658">Inventory status changes aren't allowed for quantities that are reserved for work.</span></span></td>
<td>
<ul>
<li><span data-ttu-id="6f8a2-659">この数量は、同じバッチに対して再引当されます。</span><span class="sxs-lookup"><span data-stu-id="6f8a2-659">The quantity is re-reserved for the same batch.</span></span> <span data-ttu-id="6f8a2-660">システムは、数量が使用可能なロケーションとライセンス プレート (ロケーションがライセンス プレートで制御されている場合) をランダムに割り当てます。</span><span class="sxs-lookup"><span data-stu-id="6f8a2-660">The system randomly assigns a location and license plate (if the location is license plate–controlled) where the quantity is available.</span></span></li>
<li><span data-ttu-id="6f8a2-661"><strong>在庫状態の変更</strong>タイプの 2 つの在庫トランザクションを作成して、在庫状態分析コードの変更を表します。</span><span class="sxs-lookup"><span data-stu-id="6f8a2-661">Two inventory transactions of the <strong>Inventory status change</strong> type are created to represent the change in the inventory status dimension.</span></span></li>
<li><span data-ttu-id="6f8a2-662">ブロックされた数量の引き当てを表すために、<strong>在庫ブロック</strong>タイプおよび<strong>引当済現物</strong>払出タイプの在庫トランザクションが作成されます。</span><span class="sxs-lookup"><span data-stu-id="6f8a2-662">An inventory transaction of the <strong>Inventory blocking</strong> type and the <strong>Reserved physical</strong> issue type is created to represent the reservation of the blocked quantity.</span></span></li>
</ul>
</td>
</tr>
<tr>
<td><span data-ttu-id="6f8a2-663">いいえ</span><span class="sxs-lookup"><span data-stu-id="6f8a2-663">No</span></span></td>
<td><span data-ttu-id="6f8a2-664">前の行を参照してください。</span><span class="sxs-lookup"><span data-stu-id="6f8a2-664">See the previous row.</span></span></td>
<td><span data-ttu-id="6f8a2-665">作業用に引き当てられている数量に対して、在庫状態の変更は許可されていません。</span><span class="sxs-lookup"><span data-stu-id="6f8a2-665">Inventory status changes aren't allowed for quantities that are reserved for work.</span></span></td>
<td>
<ul>
<li><span data-ttu-id="6f8a2-666">引当が削除されます。</span><span class="sxs-lookup"><span data-stu-id="6f8a2-666">The reservation is removed.</span></span></li>
<li><span data-ttu-id="6f8a2-667"><strong>在庫状態の変更</strong>タイプの 2 つの在庫トランザクションを作成して、在庫状態分析コードの変更を表します。</span><span class="sxs-lookup"><span data-stu-id="6f8a2-667">Two inventory transactions of the <strong>Inventory status change</strong> type are created to represent the change in the inventory status dimension.</span></span></li>
<li><span data-ttu-id="6f8a2-668">ブロックされた数量の引き当てを表すために、<strong>在庫ブロック</strong>タイプおよび<strong>引当済現物</strong>払出タイプの在庫トランザクションが作成されます。</span><span class="sxs-lookup"><span data-stu-id="6f8a2-668">An inventory transaction of the <strong>Inventory blocking</strong> type and the <strong>Reserved physical</strong> issue type is created to represent the reservation of the blocked quantity.</span></span></li>
</ul>
</td>
</tr>
<tr>
<td rowspan='2'><span data-ttu-id="6f8a2-669"><strong>倉庫</strong>タブの<strong>倉庫</strong>レコードで、<strong>引当とマーキングの削除</strong>フィールドが<strong>なし</strong>に設定されます。</span><span class="sxs-lookup"><span data-stu-id="6f8a2-669">On the <strong>Warehouse</strong> tab, in the <strong>Warehouse</strong> record, the <strong>Remove reservations and markings</strong> field is set to <strong>None</strong>.</span></span></td>
<td><span data-ttu-id="6f8a2-670">はい</span><span class="sxs-lookup"><span data-stu-id="6f8a2-670">Yes</span></span></td>
<td>
<ol>
<li><span data-ttu-id="6f8a2-671">特定のロケーションを選択します。</span><span class="sxs-lookup"><span data-stu-id="6f8a2-671">Select a specific location.</span></span></li>
<li><span data-ttu-id="6f8a2-672">特定の品目、ロケーション、およびライセンス プレートがある明細行を選択します (ロケーションがライセンス プレートにより制御されている場合)。</span><span class="sxs-lookup"><span data-stu-id="6f8a2-672">Select a line that has a specific item, location, and license plate (if the location is license plate–controlled).</span></span></li>
<li><span data-ttu-id="6f8a2-673"><strong>在庫状態の変更</strong>を選択します。</span><span class="sxs-lookup"><span data-stu-id="6f8a2-673">Select <strong>Inventory status change</strong>.</span></span></li>
<li><span data-ttu-id="6f8a2-674"><strong>在庫状態</strong>フィールドを<strong>ブロック</strong>に設定します。</span><span class="sxs-lookup"><span data-stu-id="6f8a2-674">Set the <strong>Inventory status</strong> field to <strong>Blocking</strong>.</span></span></li>
</ol>
</td>
<td><span data-ttu-id="6f8a2-675">作業用に引き当てられている数量に対して、在庫状態の変更は許可されていません。</span><span class="sxs-lookup"><span data-stu-id="6f8a2-675">Inventory status changes aren't allowed for quantities that are reserved for work.</span></span></td>
<td><span data-ttu-id="6f8a2-676">この数量は、同じバッチに対して再引当されます。</span><span class="sxs-lookup"><span data-stu-id="6f8a2-676">The quantity is re-reserved for the same batch.</span></span> <span data-ttu-id="6f8a2-677">システムは、数量が使用可能なロケーションとライセンス プレート (ロケーションがライセンス プレートで制御されている場合) をランダムに割り当てます。</span><span class="sxs-lookup"><span data-stu-id="6f8a2-677">The system randomly assigns a location and license plate (if the location is license plate–controlled) where the quantity is available.</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="6f8a2-678">いいえ</span><span class="sxs-lookup"><span data-stu-id="6f8a2-678">No</span></span></td>
<td><span data-ttu-id="6f8a2-679">前の行を参照してください。</span><span class="sxs-lookup"><span data-stu-id="6f8a2-679">See the previous row.</span></span></td>
<td><span data-ttu-id="6f8a2-680">作業用に引き当てられている数量に対して、在庫状態の変更は許可されていません。</span><span class="sxs-lookup"><span data-stu-id="6f8a2-680">Inventory status changes aren't allowed for quantities that are reserved for work.</span></span></td>
<td><span data-ttu-id="6f8a2-681">在庫状態の変更は許可されません。</span><span class="sxs-lookup"><span data-stu-id="6f8a2-681">Inventory status changes aren't allowed.</span></span></td>
</tr>
</tbody>
</table>

## <a name="limitations"></a><span data-ttu-id="6f8a2-682">制限</span><span class="sxs-lookup"><span data-stu-id="6f8a2-682">Limitations</span></span>

- <span data-ttu-id="6f8a2-683">変動倉庫のレベルの分析コード引当機能では、次の機能はサポートされません。</span><span class="sxs-lookup"><span data-stu-id="6f8a2-683">The flexible warehouse-level dimension reservation functionality doesn't support the following features:</span></span>

    - <span data-ttu-id="6f8a2-684">CW 管理</span><span class="sxs-lookup"><span data-stu-id="6f8a2-684">Catch weight management</span></span>
    - <span data-ttu-id="6f8a2-685">現物マイナス在庫</span><span class="sxs-lookup"><span data-stu-id="6f8a2-685">Physical negative inventory</span></span>
    - <span data-ttu-id="6f8a2-686">注文供給に対する引当</span><span class="sxs-lookup"><span data-stu-id="6f8a2-686">Reservation against ordered supply</span></span>
    - <span data-ttu-id="6f8a2-687">移動オーダーおよび原材料のピッキング</span><span class="sxs-lookup"><span data-stu-id="6f8a2-687">Transfer orders and raw material picking</span></span>

- <span data-ttu-id="6f8a2-688">ディレクティブ単位での梱包のためのコンテナー連結ルールには、制限があります。</span><span class="sxs-lookup"><span data-stu-id="6f8a2-688">The container consolidation rule for packing by directive unit has limitations.</span></span> <span data-ttu-id="6f8a2-689">注文が確定された引当では、**ディレクティブ単位別の梱包** フィールドが有効になっているコンテナー構築テンプレートを使用しないことをお勧めします。</span><span class="sxs-lookup"><span data-stu-id="6f8a2-689">For order-committed reservations, we recommend that you not use container build templates where the **Pack by directive unit** field is enabled.</span></span> <span data-ttu-id="6f8a2-690">現在の設計では、倉庫作業の作成時にロケーションの指示は使用されません。</span><span class="sxs-lookup"><span data-stu-id="6f8a2-690">In the current design, location directives aren't used when warehouse work is created.</span></span> <span data-ttu-id="6f8a2-691">したがって、コンテナー詰めのウェーブ ステップ中には、単位順序グループ (在庫単位) の最小単位のみが適用されます。</span><span class="sxs-lookup"><span data-stu-id="6f8a2-691">Therefore, only the lowest unit in the unit sequence group (the inventory unit) is applied during the containerization wave step.</span></span>
