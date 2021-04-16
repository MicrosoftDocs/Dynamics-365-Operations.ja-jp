---
title: 変動倉庫レベルの分析引当ポリシー
description: このトピックでは、製品に関連付けられている引当階層が特定のバッチの予約を許可していない場合でも、バッチ追跡製品を販売し、WMS 対応工程としてロジスティクスを実行する企業が顧客の販売注文に対して特定のバッチを予約できるようにする在庫引当のポリシーについて説明します。
author: perlynne
ms.date: 07/31/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: WHSReservationHierarchy, WHSWorkTrans, WHSWorkInventTrans, WHSInventTableReservationHierarchy, WHSReservationHierarchyCreate, WHSInventTableReservationHierarchy
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: perlynne
ms.search.validFrom: 2020-01-15
ms.dyn365.ops.version: 10.0.13
ms.openlocfilehash: 17ae3cc788c60917807acece2fc21f6c52d8ffe0
ms.sourcegitcommit: 0e8db169c3f90bd750826af76709ef5d621fd377
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/01/2021
ms.locfileid: "5835681"
---
# <a name="flexible-warehouse-level-dimension-reservation-policy"></a><span data-ttu-id="b2652-103">柔軟な倉庫レベル分析コードの引当ポリシー</span><span class="sxs-lookup"><span data-stu-id="b2652-103">Flexible warehouse-level dimension reservation policy</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="b2652-104">*以下のバッチ非優先\[ロケーション\]* タイプの在庫引当の階層が製品に関連付けられている場合、一括管理された製品を販売し、 Microsoft Dynamics 365 倉庫管理システム (WMS) が有効な業務として物流を運営している企業は、顧客の販売注文に対して特定のバッチを引当てできません。</span><span class="sxs-lookup"><span data-stu-id="b2652-104">When an inventory reservation hierarchy of the *Batch-below\[location\]* type is associated with products, businesses that sell batch-tracked products and run their logistics as operations that are enabled for the Microsoft Dynamics 365 Warehouse Management System (WMS) can't reserve specific batches of those products for customer sales orders.</span></span>

<span data-ttu-id="b2652-105">また、特定のライセンス プレートは、製品が既定の引当階層に関連付けられている場合、販売注文の製品に対して引当することはできません。</span><span class="sxs-lookup"><span data-stu-id="b2652-105">In a similar way, specific license plates can't be reserved for products on sales orders when those products are associated with the default reservation hierarchy.</span></span>

<span data-ttu-id="b2652-106">このトピックでは、製品が引当階層 *バッチ非優先\[ロケーション\]* に関連付けられている場合でも、特定のバッチやライセンス プレートを引当可能となる、在庫の引き当てポリシーについて説明します。</span><span class="sxs-lookup"><span data-stu-id="b2652-106">This topic describes the inventory reservation policy that lets these businesses reserve specific batches or license plates, even when the products are associated with a *Batch-below\[location\]* reservation hierarchy.</span></span>

## <a name="inventory-reservation-hierarchy"></a><span data-ttu-id="b2652-107">在庫引当階層</span><span class="sxs-lookup"><span data-stu-id="b2652-107">Inventory reservation hierarchy</span></span>

<span data-ttu-id="b2652-108">このセクションでは、既存の在庫引当階層の要約します。</span><span class="sxs-lookup"><span data-stu-id="b2652-108">This section summarizes the existing inventory reservation hierarchy.</span></span>

<span data-ttu-id="b2652-109">在庫の引当階層では、保管分析コードに関する限り需要注文にサイト、倉庫、在庫状況の必須の分析コードを含んでいます。</span><span class="sxs-lookup"><span data-stu-id="b2652-109">The inventory reservation hierarchy dictates that, as far as storage dimensions are concerned, the demand order carries the mandatory dimensions of site, warehouse, and inventory status.</span></span> <span data-ttu-id="b2652-110">つまり、必須分析コードとは、引当階層の中でロケーションの分析コードより上位の分析コードであり、倉庫ロジックは要求された数量にロケーションを割り当て、ロケーションを引当する役割を担っています。</span><span class="sxs-lookup"><span data-stu-id="b2652-110">In other words, the mandatory dimensions are all the dimensions above the location dimension in the reservation hierarchy, while the warehouse logic is responsible for assigning a location to the requested quantities and reserving the location.</span></span> <span data-ttu-id="b2652-111">需要オーダーと倉庫オペレーションの間の相互作用において、注文の出荷元 (つまり、サイトと倉庫) を示すように需要オーダーが求められます。</span><span class="sxs-lookup"><span data-stu-id="b2652-111">In the interactions between the demand order and the warehouse operations, the demand order is expected to indicate where the order must be shipped from (that is, what site and warehouse).</span></span> <span data-ttu-id="b2652-112">倉庫では、倉庫の施設内で必要な数量を見つけるためにロジックに依存します。</span><span class="sxs-lookup"><span data-stu-id="b2652-112">The warehouse then relies on its logic to find the required quantity in the warehouse premises.</span></span>

<span data-ttu-id="b2652-113">ただし、ビジネスの運用モデルを反映するために、追跡用分析コード (バッチ番号とシリアル番号) の方が柔軟性があります。</span><span class="sxs-lookup"><span data-stu-id="b2652-113">However, to reflect the operational model of the business, tracking dimensions (batch and serial numbers) are subject to more flexibility.</span></span> <span data-ttu-id="b2652-114">在庫引当階層は、次の条件が適用されるシナリオに対応できます。</span><span class="sxs-lookup"><span data-stu-id="b2652-114">An inventory reservation hierarchy can accommodate scenarios where the following conditions apply:</span></span>

- <span data-ttu-id="b2652-115">この業務では、バッチ番号やシリアル番号の付いた数量が倉庫の保管スペースに見つかった *後* のピッキング管理を倉庫業務に依存します。</span><span class="sxs-lookup"><span data-stu-id="b2652-115">The business relies on its warehouse operations to manage picking of quantities that have batch or serial numbers *after* the quantities have been found in the warehousing storage space.</span></span> <span data-ttu-id="b2652-116">このモデルは、多くの場合 *バッチ非優先\[ロケーション\]* または *シリアル非優先\[ロケーション\]* と呼ばれます。</span><span class="sxs-lookup"><span data-stu-id="b2652-116">This model is often referred to as *Batch-below\[location\]* or *Serial-below\[location\]*.</span></span> <span data-ttu-id="b2652-117">これは通常、製品のバッチまたはシリアル番号の ID が、販売会社に需要のある顧客にとって重要ではない場合に使用されます。</span><span class="sxs-lookup"><span data-stu-id="b2652-117">It's typically used when a product's batch or serial number identification isn't important to the customers who place the demand with the selling company.</span></span>
- <span data-ttu-id="b2652-118">この業務では、バッチ番号やシリアル番号の付いた数量が倉庫の保管スペースに見つかった *前* のピッキング管理を倉庫業務に依存します。</span><span class="sxs-lookup"><span data-stu-id="b2652-118">The business relies on its warehouse operations to manage picking of quantities that have batch or serial numbers *before* the quantities have been found in the warehousing storage space.</span></span> <span data-ttu-id="b2652-119">顧客の注文仕様の一部としてバッチ番号やシリアル番号が必要な場合、それらは要求オーダーに記録されます。また、倉庫内で数量を確認する倉庫作業では、それらを変更することはできません。</span><span class="sxs-lookup"><span data-stu-id="b2652-119">If batch or serial numbers are necessary as part of a customer's order specification, they are recorded on the demand order, and the warehouse operations that find the quantities in the warehouse aren't allowed to change them.</span></span> <span data-ttu-id="b2652-120">このモデルは、*バッチ優先\[ロケーション\]* または *シリアル優先\[ロケーション\]* と呼ばれます。</span><span class="sxs-lookup"><span data-stu-id="b2652-120">This model is referred to as *Batch-above\[location\]* or *Serial-above\[location\]*.</span></span> <span data-ttu-id="b2652-121">在庫ロケーション上の分析コードは、満たす必要がある要求に対する特定の要件であるため、倉庫ロジックでは在庫の割り当ては行されません。</span><span class="sxs-lookup"><span data-stu-id="b2652-121">Because the dimensions above location are the specific requirements for the demands that must be fulfilled, the warehouse logic won't allocate them.</span></span> <span data-ttu-id="b2652-122">これらの分析コード 、常に需要注文または関連する予約で指定する **必要があります**。</span><span class="sxs-lookup"><span data-stu-id="b2652-122">These dimensions **must** always be specified on the demand order or in the related reservations.</span></span>

<span data-ttu-id="b2652-123">これらのシナリオでは、各リリース製品に割り当て可能な在庫引当階層は 1 つだけであるという課題があります。</span><span class="sxs-lookup"><span data-stu-id="b2652-123">In these scenarios, the challenge is that only one inventory reservation hierarchy can be assigned to each released product.</span></span> <span data-ttu-id="b2652-124">したがって、WMS が追跡対象の品目を処理するために、階層の割り当てがバッチまたはシリアル番号を予約する時期を決定した後 (需要オーダーを取得したとき、または倉庫ピッキング作業中)、このタイミングをアドホック基準で変更することはできません。</span><span class="sxs-lookup"><span data-stu-id="b2652-124">Therefore, for the WMS to handle tracked items, after the hierarchy assignment determines when the batch or serial number should be reserved (either when the demand order is taken or during the warehouse picking work), this timing can't be changed on an ad-hoc basis.</span></span>

## <a name="flexible-reservation-for-batch-tracked-items"></a><span data-ttu-id="b2652-125">バッチ追跡品目の変動引当</span><span class="sxs-lookup"><span data-stu-id="b2652-125">Flexible reservation for batch-tracked items</span></span>

### <a name="business-scenario"></a><span data-ttu-id="b2652-126">ビジネス シナリオ</span><span class="sxs-lookup"><span data-stu-id="b2652-126">Business scenario</span></span>

<span data-ttu-id="b2652-127">このシナリオでは、会社は完成品をバッチ番号で追跡する在庫戦略を使用しています。</span><span class="sxs-lookup"><span data-stu-id="b2652-127">In this scenario, a company uses an inventory strategy where finished goods are tracked by batch numbers.</span></span> <span data-ttu-id="b2652-128">この会社は、WMS ワークロードも使用します。</span><span class="sxs-lookup"><span data-stu-id="b2652-128">This company also uses the WMS workload.</span></span> <span data-ttu-id="b2652-129">このワークロードには、バッチ対応アイテムの倉庫ピッキングおよび出荷操作を計画および実行するための十分に装備されたロジックがあるため、完成したアイテムのほとんどは *バッチ非優先\[ロケーション\]* 在庫引当階層に関連付けられます。</span><span class="sxs-lookup"><span data-stu-id="b2652-129">Because this workload has well-equipped logic for planning and running warehouse picking and shipping operations for batch-enabled items, most of the finished items are associated with a *Batch-below\[location\]* inventory reservation hierarchy.</span></span> <span data-ttu-id="b2652-130">このタイプの運用設定の利点は、ピッキングするバッチや倉庫内での配置ロケーションを決定する意思決定 (効果的な引当を決定すること) が、倉庫のピッキング工程を開始するまで延期されるという点です。</span><span class="sxs-lookup"><span data-stu-id="b2652-130">The advantage of this type of operational setup is that decisions (which are effectively reservation decisions) about which batches to pick and where to put them in the warehouse are postponed until the warehouse picking operations start.</span></span> <span data-ttu-id="b2652-131">顧客の注文が行われたときに作成されません。</span><span class="sxs-lookup"><span data-stu-id="b2652-131">They aren't made when the customer's order is placed.</span></span>

<span data-ttu-id="b2652-132">*バッチ非優先\[ロケーション\]* の引き当て階層は、会社のビジネス目標にも対応していますが、会社が獲得した顧客の多くは、製品の再注文時に以前に購入したものと同じバッチを必要とします。</span><span class="sxs-lookup"><span data-stu-id="b2652-132">Although the *Batch-below\[location\]* reservation hierarchy serves the company's business goals well, many of the company's established customers require the same batch that they previously purchased when they reorder products.</span></span> <span data-ttu-id="b2652-133">したがって、この会社では、バッチ引当ルールの処理方法に関する柔軟性を模索しているため、同じ品目に対する顧客の需要に応じて次のような動作が発生します。</span><span class="sxs-lookup"><span data-stu-id="b2652-133">Therefore, the company is looking for flexibility in the way that the batch reservation rules are handled, so that, depending on the customers' demand for the same item, the following behaviors occur:</span></span>

- <span data-ttu-id="b2652-134">バッチ番号は、注文が販売プロセッサによって取得されるときに記録および予約することができ、倉庫行程中に変更したり、他の需要によって取得したりすることはできません。</span><span class="sxs-lookup"><span data-stu-id="b2652-134">A batch number can be recorded and reserved when the order is taken by the sales processor, and it can't be changed during warehouse operations and/or taken by other demands.</span></span> <span data-ttu-id="b2652-135">この動作により、注文されたバッチ番号が顧客に出荷されることが保証されます。</span><span class="sxs-lookup"><span data-stu-id="b2652-135">This behavior helps guarantee that the batch number that was ordered is shipped to the customer.</span></span>
- <span data-ttu-id="b2652-136">顧客にとってバッチ番号が重要ではない場合、倉庫行程でピッキング作業中に、販売注文の登録と予約が完了した後、バッチ番号を決定できます。</span><span class="sxs-lookup"><span data-stu-id="b2652-136">If the batch number isn't important to the customer, the warehouse operations can determine a batch number during picking work, after sales order registration and reservation have been done.</span></span>

### <a name="allowing-reservation-of-a-specific-batch-on-the-sales-order"></a><span data-ttu-id="b2652-137">販売注文の特定のバッチの引当許可</span><span class="sxs-lookup"><span data-stu-id="b2652-137">Allowing reservation of a specific batch on the sales order</span></span>

<span data-ttu-id="b2652-138">*バッチ非優先\[ロケーション\]* 在庫引当階層に関連付けられている品目のバッチ引当動作に必要な柔軟性を提供するには、在庫マネージャーは、**在庫引当階層** ページで **バッチ番号** レベルの **需要の引当オーダーを許可** チェック ボックスを選択する必要があります。</span><span class="sxs-lookup"><span data-stu-id="b2652-138">To accommodate the desired flexibility in the batch reservation behavior for items that are associated with a *Batch-below\[location\]* inventory reservation hierarchy, inventory managers must select the **Allow reservation on demand order** check box for the **Batch number** level on the **Inventory reservation hierarchies** page.</span></span>

![在庫引当階層を柔軟にする](media/Flexible-inventory-reservation-hierarchy.png)

<span data-ttu-id="b2652-140">階層内の **バッチ番号** レベルが選択されている場合は、そのレベルより上で **ロケーション** レベルまでのすべての分析コードが自動的に選択されます。</span><span class="sxs-lookup"><span data-stu-id="b2652-140">When the **Batch number** level in the hierarchy is selected, all dimensions above that level and up through the **Location** level will be automatically selected.</span></span> <span data-ttu-id="b2652-141">(既定では、**ロケーション** レベルの上のすべての分析コードが事前に設定されています。) この動作は、注文明細行で特定のバッチ番号を予約した後、バッチ番号とロケーションの間の範囲のすべての分析コードも自動的に予約されるロジックを反映しています。</span><span class="sxs-lookup"><span data-stu-id="b2652-141">(By default, all dimensions above the **Location** level are preselected.) This behavior reflects the logic where all dimensions in the range between the batch number and location are also automatically reserved after you reserve a specific batch number on the order line.</span></span>

> [!NOTE]
> <span data-ttu-id="b2652-142">**需要の引当オーダーを許可** チェックボックスは、倉庫のロケーション分析コードより下にある引当階層レベルにのみ適用されます。</span><span class="sxs-lookup"><span data-stu-id="b2652-142">The **Allow reservation on demand order** check box applies only to reservation hierarchy levels that are below the warehouse location dimension.</span></span>
>
> <span data-ttu-id="b2652-143">**バッチ番号** および **ライセンス プレート** は、柔軟な予約ポリシーで使用するためにオープンされている階層内のレベルのみを指定します。</span><span class="sxs-lookup"><span data-stu-id="b2652-143">**Batch number** and **License plate** are the only levels in the hierarchy that are open for the flexible reservation policy.</span></span> <span data-ttu-id="b2652-144">つまり、**オンデマンド引当を許可する** のチェックボックスを **ロケーション** または **シリアル番号** レベルで選択することはできません。</span><span class="sxs-lookup"><span data-stu-id="b2652-144">In other words, you can't select the **Allow reservation on demand order** check box for the **Location** or **Serial number** level.</span></span>
>
> <span data-ttu-id="b2652-145">引当階層にシリアル番号分析コード (常に **バッチ番号r** レベル未満でなければならない) が含まれていて、バッチ番号のバッチ固有の予約をオンにした場合、システムは、*シリアル非優先\[ロケーション\]* 引当ポリシーに適用されるルールに基づいて、シリアル番号の予約およびピッキング操作を引き続き処理します。</span><span class="sxs-lookup"><span data-stu-id="b2652-145">If your reservation hierarchy includes the serial number dimension (which must always be below the **Batch number** level), and if you've turned on batch-specific reservation for the batch number, the system will continue to handle serial number reservation and picking operations, based on the rules that apply to the *Serial-below\[location\]* reservation policy.</span></span>

<span data-ttu-id="b2652-146">いつでも、展開内の既存の *バッチ非優先\[ロケーション\]* 引当階層にバッチ固有の予約を許可できます。</span><span class="sxs-lookup"><span data-stu-id="b2652-146">At any point, you can allow batch-specific reservation for an existing *Batch-below\[location\]* reservation hierarchy in your deployment.</span></span> <span data-ttu-id="b2652-147">この変更は、変更が発生する前に作成された引当および未処理の倉庫の作業には影響しません。</span><span class="sxs-lookup"><span data-stu-id="b2652-147">This change won't affect any reservations and open warehouse work that were created before the change occurred.</span></span> <span data-ttu-id="b2652-148">ただし、引当階層に関連付けられている 1 つ以上の品目に対して **引当済注文**、**引当済現物**、または **注文済** 払出タイプの在庫トランザクションが存在する場合は、**需要の引当オーダーを許可** チェックボックスをオフにすることはできません。</span><span class="sxs-lookup"><span data-stu-id="b2652-148">However, the **Allow reservation on demand order** check box can't be cleared if inventory transactions of the **Reserved ordered**, **Reserved physical**, or **Ordered** issue type exist for one or more items that are associated with that reservation hierarchy.</span></span>

> [!NOTE]
> <span data-ttu-id="b2652-149">品目の既存の引当階層で、注文のバッチ指定が許可されていない場合は、両方の階層で階層レベル構造が同じであることを条件として、バッチの指定が可能な引当階層に再割り当てすることができます。</span><span class="sxs-lookup"><span data-stu-id="b2652-149">If an item's existing reservation hierarchy doesn't allow batch specification on the order, you can reassign it to a reservation hierarchy that does allow batch specification, provided that the hierarchy level structure is the same in both hierarchies.</span></span> <span data-ttu-id="b2652-150">**品目の引当階層を変更** 機能を使用して、再割り当てを行います。</span><span class="sxs-lookup"><span data-stu-id="b2652-150">Use the **Change reservation hierarchy for items** function to do the reassignment.</span></span> <span data-ttu-id="b2652-151">この変更は、バッチ追跡された品目のサブセットに対する変動バッチ引当を防止し、その他の製品ポートフォリオに対して許可する場合に関連します。</span><span class="sxs-lookup"><span data-stu-id="b2652-151">This change might be relevant when you want to prevent flexible batch reservation for a subset of batch-tracked items but allow it for the rest of the product portfolio.</span></span>

<span data-ttu-id="b2652-152">**需要の引当オーダーを許可** チェックボックスを選択したかどうかにかかわらず、注文明細行のアイテムに特定のバッチ番号を引き当てない場合は、*バッチ非優先\[ロケーション\]* 引当階層に有効な既定の倉庫行程ロジックが引き続き適用されます。</span><span class="sxs-lookup"><span data-stu-id="b2652-152">Regardless of whether you've selected the **Allow reservation on demand order** check box, if you don't want to reserve a specific batch number for the item on an order line, default warehouse operations logic that is valid for a *Batch-below\[location\]* reservation hierarchy will still apply.</span></span>

### <a name="reserve-a-specific-batch-number-for-a-customer-order"></a><span data-ttu-id="b2652-153">顧客注文の特定のバッチ番号の引当</span><span class="sxs-lookup"><span data-stu-id="b2652-153">Reserve a specific batch number for a customer order</span></span>

<span data-ttu-id="b2652-154">バッチ追跡された品目の *バッチ非優先\[ロケーション\]* 在庫引当階層が設定された後、注文の特定のバッチ番号を予約できるようになり、販売注文プロセッサは、顧客の要求に応じて、次のいずれかの方法で同じアイテムの顧客注文を受け取ることができます。</span><span class="sxs-lookup"><span data-stu-id="b2652-154">After a batch-tracked item's *Batch-below\[location\]* inventory reservation hierarchy is set up to allow reservation of specific batch numbers on sales orders, sales order processors can take customer orders for the same item in one of the following ways, depending on the customer's request:</span></span>

- <span data-ttu-id="b2652-155">**バッチ番号を指定せずに注文の詳細を入力します** - このアプローチは、製品のバッチの仕様が顧客にとって重要ではない場合に使用します。</span><span class="sxs-lookup"><span data-stu-id="b2652-155">**Enter order details without specifying a batch number** – This approach should be used when the product's batch specification isn't important to the customer.</span></span> <span data-ttu-id="b2652-156">このタイプの注文の処理に関連付けられているすべての既存のプロセスは、システムに変更されずに残ります。</span><span class="sxs-lookup"><span data-stu-id="b2652-156">All existing processes that are associated with handling an order of this type in the system remain unchanged.</span></span> <span data-ttu-id="b2652-157">ユーザー側で追加の考慮事項は必要ありません。</span><span class="sxs-lookup"><span data-stu-id="b2652-157">No additional considerations are required on the part of users.</span></span>
- <span data-ttu-id="b2652-158">**注文の詳細を入力し、特定のバッチ番号を引当** - 顧客が特定のバッチを要求する場合は、この方法を使用する必要があります。</span><span class="sxs-lookup"><span data-stu-id="b2652-158">**Enter order details and reserve a specific batch number** – This approach should be used when the customer requests a specific batch.</span></span> <span data-ttu-id="b2652-159">通常、顧客は以前に購入した製品を再注文するときに特定のバッチを要求します。</span><span class="sxs-lookup"><span data-stu-id="b2652-159">Typically, customers will request a specific batch when they are reordering a product that they previously purchased.</span></span> <span data-ttu-id="b2652-160">このタイプのバッチ固有の引当は、*確定済み引当* と呼ばれます。</span><span class="sxs-lookup"><span data-stu-id="b2652-160">This type of batch-specific reservation is referred to as *order-committed reservation*.</span></span>

<span data-ttu-id="b2652-161">次の一連のルールは、数量が処理されるときに有効になり、バッチ番号は特定の注文にコミットされます。</span><span class="sxs-lookup"><span data-stu-id="b2652-161">The following set of rules is valid when quantities are processed, and a batch number is committed to a specific order:</span></span>

- <span data-ttu-id="b2652-162">*バッチ非優先\[ロケーション\]* 引当ポリシーの下で品目の特定のバッチ番号の引当を許可するには、システムはロケーションまですべての分析コードを引当する必要があります。</span><span class="sxs-lookup"><span data-stu-id="b2652-162">To allow reservation of a specific batch number for an item under the *Batch-below\[location\]* reservation policy, the system must reserve all dimensions up through location.</span></span> <span data-ttu-id="b2652-163">通常、この範囲には、ライセンス プレート分析コードが含まれます。</span><span class="sxs-lookup"><span data-stu-id="b2652-163">This range typically includes the license plate dimension.</span></span>
- <span data-ttu-id="b2652-164">注文が確定したバッチ引当を使用する販売明細行に対してピッキング作業が作成される場合、ロケーションの指示は使用されません。</span><span class="sxs-lookup"><span data-stu-id="b2652-164">Location directives aren't used when picking work is created for a sales line that uses order-committed batch reservation.</span></span>
- <span data-ttu-id="b2652-165">注文が確定したバッチの作業倉庫処理では、ユーザーもシステムもバッチ番号を変更することはできません。</span><span class="sxs-lookup"><span data-stu-id="b2652-165">During warehouse processing of work for order-committed batches, neither the user nor the system is allowed to change the batch number.</span></span> <span data-ttu-id="b2652-166">(この処理には例外処理が含まれています。)</span><span class="sxs-lookup"><span data-stu-id="b2652-166">(This processing includes exception handling.)</span></span>

<span data-ttu-id="b2652-167">次の例は、エンド ツー エンド フローの例を示しています。</span><span class="sxs-lookup"><span data-stu-id="b2652-167">The following example shows the end-to-end flow.</span></span>

## <a name="example-scenario-batch-number-allocation"></a><span data-ttu-id="b2652-168">シナリオ例 : バッチ番号の配賦</span><span class="sxs-lookup"><span data-stu-id="b2652-168">Example scenario: Batch number allocation</span></span>

<span data-ttu-id="b2652-169">この例では、**USMF** デモ データの会社を使用して、デモ データをインストールする必要があります。</span><span class="sxs-lookup"><span data-stu-id="b2652-169">For this example, demo data must be installed, and you must use the **USMF** demo data company.</span></span>

### <a name="set-up-an-inventory-reservation-hierarchy-to-allow-batch-specific-reservation"></a><a name="Example-batch-allocation"></a><span data-ttu-id="b2652-170">在庫引当階層を設定して、バッチ固有の引当を許可する</span><span class="sxs-lookup"><span data-stu-id="b2652-170">Set up an inventory reservation hierarchy to allow batch-specific reservation</span></span>

1. <span data-ttu-id="b2652-171">**倉庫管理** \> **設定** \> **在庫 \> 引当階層** に移動します。</span><span class="sxs-lookup"><span data-stu-id="b2652-171">Go to **Warehouse management** \> **Setup** \> **Inventory \> Reservation hierarchy**.</span></span>
2. <span data-ttu-id="b2652-172">**新規** を選択します。</span><span class="sxs-lookup"><span data-stu-id="b2652-172">Select **New**.</span></span>
3. <span data-ttu-id="b2652-173">**名前** フィールドに、名前を入力します (たとえば、**BatchFlex**)。</span><span class="sxs-lookup"><span data-stu-id="b2652-173">In the **Name** field, enter a name (for example, **BatchFlex**).</span></span>
4. <span data-ttu-id="b2652-174">**説明** フィールドに、説明を入力します (たとえば、**下の変動バッチ** など)。</span><span class="sxs-lookup"><span data-stu-id="b2652-174">In the **Description** field, enter a description (for example, **Batch below flexible**).</span></span>
5. <span data-ttu-id="b2652-175">**選択済** フィールドで、**シリアル番号** および **所有者** を選択し、左矢印ボタンを選択して **使用可能** フィールドに移動します。</span><span class="sxs-lookup"><span data-stu-id="b2652-175">In the **Selected** field, select **Serial number** and **Owner**, and then select the left arrow button to move them to the **Available** field.</span></span>
6. <span data-ttu-id="b2652-176">**OK** を選択します。</span><span class="sxs-lookup"><span data-stu-id="b2652-176">Select **OK**.</span></span>
7. <span data-ttu-id="b2652-177">**バッチ番号** 分析コード レベルの行で、**需要の引当オーダーを許可** チェックボックスを選択します。</span><span class="sxs-lookup"><span data-stu-id="b2652-177">In the row for the **Batch number** dimension level, select the **Allow reservation on demand order** check box.</span></span> <span data-ttu-id="b2652-178">**ライセンス プレート** と **ロケーション** のレベルは自動的に選択され、それらのチェックボックスをオフにすることはできません。</span><span class="sxs-lookup"><span data-stu-id="b2652-178">The **License plate** and **Location** levels are automatically selected, and you can't clear the check boxes for them.</span></span>
8. <span data-ttu-id="b2652-179">**保存** を選択します。</span><span class="sxs-lookup"><span data-stu-id="b2652-179">Select **Save**.</span></span>

### <a name="create-a-new-released-product"></a><span data-ttu-id="b2652-180">新しくリリースされた製品の作成</span><span class="sxs-lookup"><span data-stu-id="b2652-180">Create a new released product</span></span>

1. <span data-ttu-id="b2652-181">次の値を使用して、製品の 3 つのマスター データ パラメータを設定します。</span><span class="sxs-lookup"><span data-stu-id="b2652-181">Set the product's three master data parameters by using these values:</span></span>

    - <span data-ttu-id="b2652-182">**保管分析コード グループ** フィールドで、**Ware** を選択します。</span><span class="sxs-lookup"><span data-stu-id="b2652-182">In the **Storage dimension group** field, select **Ware**.</span></span>
    - <span data-ttu-id="b2652-183">**追跡用分析コード グループ** フィールドで、**Batch-Phy** を選択します。</span><span class="sxs-lookup"><span data-stu-id="b2652-183">In the **Tracking dimension group** field, select **Batch-Phy**.</span></span>
    - <span data-ttu-id="b2652-184">**引当階層** フィールドで、**BatchFlex** を選択します。</span><span class="sxs-lookup"><span data-stu-id="b2652-184">In the **Reservation hierarchy** field, select **BatchFlex**.</span></span>

2. <span data-ttu-id="b2652-185">**B11** や **B22** などの 2 つのバッチ番号を作成します。</span><span class="sxs-lookup"><span data-stu-id="b2652-185">Create two batch numbers, such as **B11** and **B22**.</span></span>
3. <span data-ttu-id="b2652-186">次の値を使用して、品目の数量を手持在庫に追加します。</span><span class="sxs-lookup"><span data-stu-id="b2652-186">Add item quantities to on-hand stock by using the following values.</span></span>

    | <span data-ttu-id="b2652-187">倉庫</span><span class="sxs-lookup"><span data-stu-id="b2652-187">Warehouse</span></span> | <span data-ttu-id="b2652-188">バッチ番号</span><span class="sxs-lookup"><span data-stu-id="b2652-188">Batch number</span></span> | <span data-ttu-id="b2652-189">ロケーション</span><span class="sxs-lookup"><span data-stu-id="b2652-189">Location</span></span> | <span data-ttu-id="b2652-190">ライセンス プレート</span><span class="sxs-lookup"><span data-stu-id="b2652-190">License plate</span></span> | <span data-ttu-id="b2652-191">件数</span><span class="sxs-lookup"><span data-stu-id="b2652-191">Quantity</span></span> |
    |-----------|--------------|----------|---------------|----------|
    | <span data-ttu-id="b2652-192">24</span><span class="sxs-lookup"><span data-stu-id="b2652-192">24</span></span>        | <span data-ttu-id="b2652-193">B11</span><span class="sxs-lookup"><span data-stu-id="b2652-193">B11</span></span>          | <span data-ttu-id="b2652-194">BULK-001</span><span class="sxs-lookup"><span data-stu-id="b2652-194">BULK-001</span></span> | <span data-ttu-id="b2652-195">なし</span><span class="sxs-lookup"><span data-stu-id="b2652-195">None</span></span>          | <span data-ttu-id="b2652-196">10</span><span class="sxs-lookup"><span data-stu-id="b2652-196">10</span></span>       |
    | <span data-ttu-id="b2652-197">24</span><span class="sxs-lookup"><span data-stu-id="b2652-197">24</span></span>        | <span data-ttu-id="b2652-198">B11</span><span class="sxs-lookup"><span data-stu-id="b2652-198">B11</span></span>          | <span data-ttu-id="b2652-199">FL-001</span><span class="sxs-lookup"><span data-stu-id="b2652-199">FL-001</span></span>   | <span data-ttu-id="b2652-200">LP11</span><span class="sxs-lookup"><span data-stu-id="b2652-200">LP11</span></span>          | <span data-ttu-id="b2652-201">10</span><span class="sxs-lookup"><span data-stu-id="b2652-201">10</span></span>       |
    | <span data-ttu-id="b2652-202">24</span><span class="sxs-lookup"><span data-stu-id="b2652-202">24</span></span>        | <span data-ttu-id="b2652-203">B22</span><span class="sxs-lookup"><span data-stu-id="b2652-203">B22</span></span>          | <span data-ttu-id="b2652-204">FL-002</span><span class="sxs-lookup"><span data-stu-id="b2652-204">FL-002</span></span>   | <span data-ttu-id="b2652-205">LP22</span><span class="sxs-lookup"><span data-stu-id="b2652-205">LP22</span></span>          | <span data-ttu-id="b2652-206">10</span><span class="sxs-lookup"><span data-stu-id="b2652-206">10</span></span>       |

### <a name="enter-sales-order-details"></a><a name="sales-order-details"></a><span data-ttu-id="b2652-207">販売注文詳細の入力</span><span class="sxs-lookup"><span data-stu-id="b2652-207">Enter sales order details</span></span>

1. <span data-ttu-id="b2652-208">**販売とマーケティング** \> **販売注文** \> **すべての販売注文** の順に移動します。</span><span class="sxs-lookup"><span data-stu-id="b2652-208">Go to **Sales and marketing** \> **Sales orders** \> **All sales orders**.</span></span>
2. <span data-ttu-id="b2652-209">**新規** を選択します。</span><span class="sxs-lookup"><span data-stu-id="b2652-209">Select **New**.</span></span>
3. <span data-ttu-id="b2652-210">販売注文ヘッダーの **顧客 ID** フィールドに、**US-003** と入力します。</span><span class="sxs-lookup"><span data-stu-id="b2652-210">On the sales order header, in the **Customer account** field, enter **US-003**.</span></span>
4. <span data-ttu-id="b2652-211">新規の品目の明細行を追加し、数量として **10** を入力します。</span><span class="sxs-lookup"><span data-stu-id="b2652-211">Add a line for the new item, and enter **10** as the quantity.</span></span> <span data-ttu-id="b2652-212">**倉庫** フィールドが **24** に設定されていることを確認してください。</span><span class="sxs-lookup"><span data-stu-id="b2652-212">Make sure that the **Warehouse** field is set to **24**.</span></span>
5. <span data-ttu-id="b2652-213">**販売注文明細行** クイック タブで **在庫** を選択し、**管理** グループで **バッチ引当** を選択します。</span><span class="sxs-lookup"><span data-stu-id="b2652-213">On the **Sales order lines** FastTab, select **Inventory**, and then, in the **Maintain** group, select **Batch reservation**.</span></span> <span data-ttu-id="b2652-214">**バッチ引当** ページに、注文明細行の引当に使用できるバッチのリストが表示されます。</span><span class="sxs-lookup"><span data-stu-id="b2652-214">The **Batch reservation** page shows a list of batches that are available for reservation for the order line.</span></span> <span data-ttu-id="b2652-215">この例では、バッチ番号 **B11** の場合は **20** の数量、バッチ番号 **B22** の場合は **10** の数量が表示されます。</span><span class="sxs-lookup"><span data-stu-id="b2652-215">For this example, it shows a quantity of **20** for batch number **B11** and a quantity of **10** for batch number **B22**.</span></span> <span data-ttu-id="b2652-216">バッチ固有の引当を許可するように設定されていない限り、その行の品目が *バッチ非優先\[ロケーション\]* 引当階層に関連付けられている場合、**バッチ引当** ページにアクセスできないことに注意してください。</span><span class="sxs-lookup"><span data-stu-id="b2652-216">Note that the **Batch reservation** page cannot be accessed from a line if the item on that line is associated with *Batch-below\[location\]* reservation hierarchy unless it is set up to allow batch-specific reservation.</span></span>

    > [!NOTE]
    > <span data-ttu-id="b2652-217">販売注文の特定のバッチを引当するには、**バッチ引当** ページを使用する必要があります。</span><span class="sxs-lookup"><span data-stu-id="b2652-217">To reserve a specific batch for a sales order, you must use the **Batch reservation** page.</span></span>
    >
    > <span data-ttu-id="b2652-218">販売注文明細行にバッチ番号を直接入力すると、*バッチ非優先\[ロケーション\]* の引当ポリシーの対象となる品目に対して特定のバッチ値を入力した場合と同じようにシステムが動作します。</span><span class="sxs-lookup"><span data-stu-id="b2652-218">If you enter the batch number directly on the sales order line, the system will behave as though you entered a specific batch value for an item that is subject to the *Batch-below\[location\]* reservation policy.</span></span> <span data-ttu-id="b2652-219">明細行を保存すると、警告メッセージが表示されます。</span><span class="sxs-lookup"><span data-stu-id="b2652-219">When you save the line, you will receive a warning message.</span></span> <span data-ttu-id="b2652-220">バッチ番号が注文明細行に直接指定されていることを確認した場合、その明細行は、通常の倉庫管理ロジックで処理されることはありません。</span><span class="sxs-lookup"><span data-stu-id="b2652-220">If you confirm that the batch number should be specified directly on the order line, the line won't be handled by the regular warehouse management logic.</span></span>
    >
    > <span data-ttu-id="b2652-221">**引当** ページの数量を引当すると、特定のバッチは引当されず、その行の倉庫操作の実行は、*バッチ非優先\[ロケーション\]* の引当ポリシーの下で適用されるルールに従います。</span><span class="sxs-lookup"><span data-stu-id="b2652-221">If you reserve the quantity from the **Reservation** page, no specific batch will be reserved, and the execution of warehouse operations for the line will follow the rules that are applicable under the *Batch-below\[location\]* reservation policy.</span></span>

    <span data-ttu-id="b2652-222">一般に、このページは *バッチ優先\[ロケーション\]* タイプの引当階層が関連付けられている品目に対して機能し、同じ方法で連携されます。</span><span class="sxs-lookup"><span data-stu-id="b2652-222">In general, this page works and is interacted with in the same way for items that have an associated reservation hierarchy of the *Batch-above\[location\]* type.</span></span> <span data-ttu-id="b2652-223">ただし、次の例外が適用されます。</span><span class="sxs-lookup"><span data-stu-id="b2652-223">However, the following exceptions apply:</span></span>

    - <span data-ttu-id="b2652-224">**ソース明細行に確定済みのバッチ番号** クイック タブには、注文明細行に対して引き当てられているバッチ番号が表示されます。</span><span class="sxs-lookup"><span data-stu-id="b2652-224">The **Batch numbers committed to source line** FastTab shows the batch numbers that are reserved for the order line.</span></span> <span data-ttu-id="b2652-225">グリッドのバッチ値は、倉庫処理ステージを含む注文明細行のフルフィルメント サイクル全体で表示されます。</span><span class="sxs-lookup"><span data-stu-id="b2652-225">The batch values in the grid will be shown throughout the fulfillment cycle of the order line, including the warehouse processing stages.</span></span> <span data-ttu-id="b2652-226">対照的に、**概要** クイックタブでは、通常の注文明細行の引当 (**ロケーション** レベルの上にある分析コードに対して実行される引当) は、倉庫作業が作成される時点までグリッドに表示されます。</span><span class="sxs-lookup"><span data-stu-id="b2652-226">By contrast, on the **Overview** FastTab, regular order line reservation (that is, reservation that is done for the dimensions above the **Location** level) is shown in the grid up to the point when warehouse work is created.</span></span> <span data-ttu-id="b2652-227">その後、作業エンティティは明細行の引当を引き継ぎ、明細行の引当はページに表示されなくなります。</span><span class="sxs-lookup"><span data-stu-id="b2652-227">The work entity then takes over the line reservation, and the line reservation no longer appears on the page.</span></span> <span data-ttu-id="b2652-228">**ソース明細行に確定済みのバッチ番号** クイック タブは、販売注文プロセッサが、請求まで、ライフサイクルの任意の時点で顧客の注文に対して確定されたバッチ番号を表示できるようにするために役立ちます。</span><span class="sxs-lookup"><span data-stu-id="b2652-228">The **Batch numbers committed to source line** FastTab helps guarantee that the sales order processor can view the batch numbers that were committed to the customer's order at any point during its lifecycle, up through invoicing.</span></span>
    - <span data-ttu-id="b2652-229">特定のバッチの引当に加えて、ユーザーはシステムによって自動的に選択させる代わりに、バッチの特定のロケーションとライセンス プレートを手動で選択できます。</span><span class="sxs-lookup"><span data-stu-id="b2652-229">In addition to reserving a specific batch, a user can manually select the batch's specific location and license plate instead of letting the system automatically select them.</span></span> <span data-ttu-id="b2652-230">この機能は、注文が確定したバッチ引当メカニズムの設計に関連しています。</span><span class="sxs-lookup"><span data-stu-id="b2652-230">This capability is related to the design of the order-committed batch reservation mechanism.</span></span> <span data-ttu-id="b2652-231">前述のように、バッチ番号が *バッチ非優先\[ロケーション\]* 引当ポリシーの品目で引当されている場合、システムはすべての分析コードをロケーションまで引当てる必要があります。</span><span class="sxs-lookup"><span data-stu-id="b2652-231">As was mentioned earlier, when a batch number is reserved for an item under the *Batch-below\[location\]* reservation policy, the system must reserve all dimensions up through location.</span></span> <span data-ttu-id="b2652-232">したがって、倉庫作業では、注文を処理したユーザーによって予約されたものと同じ保管分析コードが使用され、ピッキング行程に便利な、または可能な品目の保管ロケーションを常に表すとは限りません。</span><span class="sxs-lookup"><span data-stu-id="b2652-232">Therefore, warehouse work will carry the same storage dimensions that were reserved by the users who worked with the orders, and it might not always represent the item storage placement that is convenient, or even possible, for picking operations.</span></span> <span data-ttu-id="b2652-233">注文処理担当者が倉庫の制約を認識している場合、バッチを予約する際に特定のロケーションとライセンス プレートを手動で選択することができます。</span><span class="sxs-lookup"><span data-stu-id="b2652-233">If order processors are aware of the warehouse constraints, they might want to manually select the specific locations and license plates when they reserve a batch.</span></span> <span data-ttu-id="b2652-234">この場合、ユーザーはページ ヘッダーの **分析コードの表示** 機能を使用し、**概要** クイック タブのグリッドにロケーションとライセンス プレートを追加する必要があります。</span><span class="sxs-lookup"><span data-stu-id="b2652-234">In this case, the user must use the **Display dimensions** functionality on the page header, and must add the location and license plate in the grid on the **Overview** FastTab.</span></span>

6. <span data-ttu-id="b2652-235">**バッチ引当** ページで、バッチ **B11** の明細行を選択し、**引当行** を選択します。</span><span class="sxs-lookup"><span data-stu-id="b2652-235">On the **Batch reservation** page, select the line for batch **B11**, and then select **Reserve line**.</span></span> <span data-ttu-id="b2652-236">自動引当中にロケーションとライセンス プレートを割り当てるための指定されたロジックはありません。</span><span class="sxs-lookup"><span data-stu-id="b2652-236">There is no designated logic for assigning locations and license plates during automatic reservation.</span></span> <span data-ttu-id="b2652-237">**引当** フィールドに手動で数量を入力できます。</span><span class="sxs-lookup"><span data-stu-id="b2652-237">You can manually enter the quantity in the **Reservation** field.</span></span> <span data-ttu-id="b2652-238">**ソース明細行に確定済みのバッチ番号** クイック タブでは、バッチ **B11** が **確定済み** として表示されることに注意してください。</span><span class="sxs-lookup"><span data-stu-id="b2652-238">Notice that, on the **Batch numbers committed to source line** FastTab, batch **B11** is shown as **Committed**.</span></span>

    ![バッチ引当ページの特定のバッチ番号を販売注文明細行にコミットする](media/Batch-reservation-form-with-order-committed-reservation.png)

    > [!NOTE]
    > <span data-ttu-id="b2652-240">販売注文明細行の数量の引当は、複数のバッチ間で行うことができます。</span><span class="sxs-lookup"><span data-stu-id="b2652-240">Reservation of the quantity on a sales order line can be done across multiple batches.</span></span> <span data-ttu-id="b2652-241">同様に、複数のロケーションおよびライセンス プレートに対して同じバッチの引当を行うことができます (そのロケーションでライセンス プレートが有効になっている場合)。</span><span class="sxs-lookup"><span data-stu-id="b2652-241">Likewise, reservation of the same batch can be done against multiple locations and license plates (if license plates are enabled for the locations).</span></span>
    >
    > <span data-ttu-id="b2652-242">販売注文明細行の数量に対する特定のバッチの引当も部分的に設定することもできます。</span><span class="sxs-lookup"><span data-stu-id="b2652-242">Reservation of a specific batch for the quantity on a sales order line can also be partial.</span></span> <span data-ttu-id="b2652-243">たとえば、100 単位の合計数量を引当して、特定のバッチを 20 単位にコミットし、80 単位を使用可能なバッチのサイトおよび倉庫レベルで引当できます。</span><span class="sxs-lookup"><span data-stu-id="b2652-243">For example, the total quantity of 100 units can be reserved so that a specific batch is committed to 20 units, whereas 80 units are reserved at the site and warehouse levels for any available batch.</span></span> <span data-ttu-id="b2652-244">この場合、WMS は 2 つの異なる作業明細行を使用してピッキング工程を処理します。</span><span class="sxs-lookup"><span data-stu-id="b2652-244">In this case, the WMS will handle picking operations by using two separate work lines.</span></span>

7. <span data-ttu-id="b2652-245">**製品情報管理** \> **製品** \> **リリース済製品** の順に移動します。</span><span class="sxs-lookup"><span data-stu-id="b2652-245">Go to **Product information management** \> **Products** \> **Released products**.</span></span> <span data-ttu-id="b2652-246">品目を選択し、**在庫の管理** \> **表示** \> **トランザクション** を選択します。</span><span class="sxs-lookup"><span data-stu-id="b2652-246">Select your item, and then select **Manage inventory** \> **View** \> **Transactions**.</span></span>

    ![在庫トランザクション タイプとして確定済み引当](media/Inventory-transactions-for-order-committed-reservation.png)

8. <span data-ttu-id="b2652-248">販売注文明細行の引当に関連する品目の在庫トランザクションを確認します。</span><span class="sxs-lookup"><span data-stu-id="b2652-248">Review the item's inventory transactions that are related to the sales order line reservation.</span></span>

    - <span data-ttu-id="b2652-249">**参照** フィールドが **販売注文** に設定され、**払出** フィールドが **引当済現物** に設定されているトランザクションは、**ロケーション** レベルよりも上の在庫分析コードの注文明細行の引当を表します。</span><span class="sxs-lookup"><span data-stu-id="b2652-249">A transaction where the **Reference** field is set to **Sales order** and the **Issue** field is set to **Reserved physical** represents the order line reservation for the inventory dimensions above the **Location** level.</span></span> <span data-ttu-id="b2652-250">品目の在庫引当階層に従って、これらの分析コードは、サイト、倉庫、および在庫状態になります。</span><span class="sxs-lookup"><span data-stu-id="b2652-250">According to the item's inventory reservation hierarchy, those dimensions are site, warehouse, and inventory status.</span></span>
    - <span data-ttu-id="b2652-251">**参照** フィールドが **確定済み引当** に設定され、**払出** フィールドが **引当済現物** に設定されているトランザクションは、特定のバッチおよびその上のすべての在庫分析コードの注文明細行の引当を表します。</span><span class="sxs-lookup"><span data-stu-id="b2652-251">A transaction where the **Reference** field is set to **Order-committed reservation** and the **Issue** field is set to **Reserved physical** represents the order line reservation for the specific batch and all inventory dimensions above it.</span></span> <span data-ttu-id="b2652-252">品目の在庫引当階層に従って、これらの分析コードは、バッチ番号およびロケーションになります。</span><span class="sxs-lookup"><span data-stu-id="b2652-252">According to the item's inventory reservation hierarchy, those dimensions are batch number and location.</span></span> <span data-ttu-id="b2652-253">この例では、このロケーションは **Bulk-001** です。</span><span class="sxs-lookup"><span data-stu-id="b2652-253">In this example, the location is **Bulk-001**.</span></span>

9. <span data-ttu-id="b2652-254">販売注文ヘッダーで、**倉庫** \> **アクション** \> **倉庫にリリース** を選択します。</span><span class="sxs-lookup"><span data-stu-id="b2652-254">On the sales order header, select **Warehouse** \> **Actions** \> **Release to warehouse**.</span></span> <span data-ttu-id="b2652-255">注文明細行がウェーブ処理され、積荷と作業が作成されます。</span><span class="sxs-lookup"><span data-stu-id="b2652-255">The order line is now waved, and a load and work are created.</span></span>

### <a name="review-and-process-warehouse-work-that-has-order-committed-batch-numbers"></a><span data-ttu-id="b2652-256">注文が確定したバッチ番号を持つ倉庫作業の確認および処理</span><span class="sxs-lookup"><span data-stu-id="b2652-256">Review and process warehouse work that has order-committed batch numbers</span></span>

1. <span data-ttu-id="b2652-257">**販売注文明細行** クイック タブで、**倉庫** \> **作業の詳細** を選択します。</span><span class="sxs-lookup"><span data-stu-id="b2652-257">On the **Sales order lines** FastTab, select **Warehouse** \> **Work details**.</span></span>

    <span data-ttu-id="b2652-258">販売注文明細行に確定されているバッチの数量のピッキング工程を処理する作業には、次のような特性があります。</span><span class="sxs-lookup"><span data-stu-id="b2652-258">The work that handles the picking operation for batch quantities that are committed to the sales order line has the following characteristics:</span></span>

    - <span data-ttu-id="b2652-259">作業を作成するには、作業テンプレートを使用しますが、ロケーションの指示は使用しません。</span><span class="sxs-lookup"><span data-stu-id="b2652-259">To create work, the system uses work templates but not location directives.</span></span> <span data-ttu-id="b2652-260">いつ新しい作業を作成するかを決定するために、ピッキング明細行の最大数や特定の測定単位など、作業テンプレートに定義されているすべての標準設定が適用されます。</span><span class="sxs-lookup"><span data-stu-id="b2652-260">All the standard settings that are defined for work templates, such as a maximum number of pick lines or a specific unit of measure, will be applied to determine when new work should be created.</span></span> <span data-ttu-id="b2652-261">ただし、確定済み引当ではすべての在庫分析コードが既に指定されているため、ピッキングロケーションを識別するためのロケーションの指示に関連付けられているルールは考慮されません。</span><span class="sxs-lookup"><span data-stu-id="b2652-261">However, the rules that are associated with location directives for identifying pick locations aren't considered, because the order-committed reservation already specifies all the inventory dimensions.</span></span> <span data-ttu-id="b2652-262">これらの在庫分析コードには、倉庫の保管レベルの分析コードが含まれます。</span><span class="sxs-lookup"><span data-stu-id="b2652-262">Those inventory dimensions include the dimensions at the warehouse storage level.</span></span> <span data-ttu-id="b2652-263">したがって、作業では、ロケーションの指示を参照することなく、これらの分析コードが継承されます。</span><span class="sxs-lookup"><span data-stu-id="b2652-263">Therefore, the work inherits those dimensions without having to consult location directives.</span></span>
    - <span data-ttu-id="b2652-264">バッチ番号は、ピッキング行には表示されません。(*バッチ優先\[ロケーション\]* の引当階層が関連付けられている品目に対して作成される作業明細行と同様です) 代わりに、「開始」バッチ番号と他のすべての保管分析コードが、関連付けられている在庫トランザクションから参照されている作業明細行の作業在庫トランザクションに表示されます。</span><span class="sxs-lookup"><span data-stu-id="b2652-264">The batch number isn't shown on the pick line (as is the case for the work line that is created for an item that has an associated *Batch-above\[location\]* reservation hierarchy.) Instead, the "from" batch number and all other storage dimensions are shown on the work line's work inventory transaction that is referenced from the associated inventory transactions.</span></span>

        ![注文が確定した引当によって発生した作業の倉庫在庫トランザクション](media/Work-inventory-transactions-for-order-committed-reservation.png)

    - <span data-ttu-id="b2652-266">作業が作成されると、**参照** フィールドが **確定済み引当** に設定されている品目の在庫トランザクションが削除されます。</span><span class="sxs-lookup"><span data-stu-id="b2652-266">After work is created, the item's inventory transaction where the **Reference** field is set to **Order-committed reservation** is removed.</span></span> <span data-ttu-id="b2652-267">**参照** フィールドが **作業** に設定されている在庫トランザクションは、すべての数量の在庫分析コードに対して現物引当を保持するようになりました。</span><span class="sxs-lookup"><span data-stu-id="b2652-267">The inventory transaction where the **Reference** field is set to **Work** now holds the physical reservation on all the quantity's inventory dimensions.</span></span>

        <span data-ttu-id="b2652-268">倉庫工程は、作業の実行を通常の方法で処理することができます。</span><span class="sxs-lookup"><span data-stu-id="b2652-268">Warehouse operations can proceed to handle execution of the work in the usual manner.</span></span> <span data-ttu-id="b2652-269">ただし、モバイル デバイスの指示では、特定のバッチ番号を選択するよう作業者に指示します。</span><span class="sxs-lookup"><span data-stu-id="b2652-269">However, the instructions on the mobile device will instruct the worker to pick a specific batch number.</span></span> <span data-ttu-id="b2652-270">ロケーションがライセンス プレートにより制御されている倉庫環境では、複数のライセンス プレートで同じバッチが保管されているロケーションに作業者が到達した後、まだ引当されていないライセンス プレートから選択できます (たとえば、別の確定済み引当またはそのタイプの引当から発生する作業による)。</span><span class="sxs-lookup"><span data-stu-id="b2652-270">In warehouse environments where locations are license plate–controlled, after a worker reaches a location that stores the same batch on multiple license plates, he or she can pick from any license plate that isn't already reserved (for example, by another order-committed reservation or work that originates from a reservation of that type.)</span></span>

        <span data-ttu-id="b2652-271">作業明細行で指定されたロケーションからのピッキングが実際的ではない場合、倉庫オペレーターは次のいずれかのアクションを使用して、特定のバッチのピッキングをより便利なロケーションからリダイレクトできます。</span><span class="sxs-lookup"><span data-stu-id="b2652-271">If it turns out to be impractical to pick from the location that is specified on the work line, the warehouse operators can use one of the following actions to redirect picking of the specific batch from a more convenient location:</span></span>

        - <span data-ttu-id="b2652-272">モバイル デバイスでの標準の **ロケーションの上書き** アクション (倉庫作業者の **ピッキング ロケーションの上書きを許可** 設定が有効になっている場合)</span><span class="sxs-lookup"><span data-stu-id="b2652-272">The standard **Override location** action on a mobile device (provided that the warehouse worker's **Allow pick location override** setting is enabled)</span></span>
        - <span data-ttu-id="b2652-273">**作業一覧詳細** ページでの **ロケーションの変更** アクション。</span><span class="sxs-lookup"><span data-stu-id="b2652-273">The **Change location** action on the **Work list details** page.</span></span> 

2. <span data-ttu-id="b2652-274">モバイル デバイスで、ピッキングと作業の配置を完了します。</span><span class="sxs-lookup"><span data-stu-id="b2652-274">On the mobile device, finish picking and putting the work.</span></span>

    <span data-ttu-id="b2652-275">バッチ番号 **B11** の数量 **10** が販売注文明細行に対してピッキングされ、**Baydoor** のロケーションに配置されます。</span><span class="sxs-lookup"><span data-stu-id="b2652-275">The quantity of **10** for batch number **B11** is now picked for the sales order line and put in the **Baydoor** location.</span></span> <span data-ttu-id="b2652-276">この時点で、トラックに積載して、顧客の住所に出荷する準備が整いました。</span><span class="sxs-lookup"><span data-stu-id="b2652-276">At this point, it's ready to be loaded onto the truck and dispatched to the customer's address.</span></span>

## <a name="flexible-license-plate-reservation"></a><span data-ttu-id="b2652-277">柔軟なライセンス プレートの引当</span><span class="sxs-lookup"><span data-stu-id="b2652-277">Flexible license plate reservation</span></span>

### <a name="business-scenario"></a><span data-ttu-id="b2652-278">ビジネス シナリオ</span><span class="sxs-lookup"><span data-stu-id="b2652-278">Business scenario</span></span>

<span data-ttu-id="b2652-279">このシナリオでは、倉庫管理や作業処理を行い、作業が発生する前に Supply Chain Management の外部にある個々のパレット/コンテナーのレベルでの積荷計画を処理します。</span><span class="sxs-lookup"><span data-stu-id="b2652-279">In this scenario, a company uses warehouse management and work processing, and handles load planning at the level of individual pallets/containers outside Supply Chain Management before work is created.</span></span> <span data-ttu-id="b2652-280">これらのコンテナーは、在庫分析コードのライセンス プレートで表されます。</span><span class="sxs-lookup"><span data-stu-id="b2652-280">These containers are represented by license plates in the inventory dimensions.</span></span> <span data-ttu-id="b2652-281">そのため、この方法ではピッキング作業を行う前に、特定のライセンス プレートを事前に販売注文明細行に割り当てる必要があります。</span><span class="sxs-lookup"><span data-stu-id="b2652-281">Therefore, for this approach, specific license plates must be pre-assigned to sales order lines before picking work is done.</span></span> <span data-ttu-id="b2652-282">ライセンス プレートの引当ルールの扱いに柔軟性を求めているため、次のような事象が発生します :</span><span class="sxs-lookup"><span data-stu-id="b2652-282">The company is looking for flexibility in the way that the license plate reservation rules are handled, so that the following behaviors occur:</span></span>

- <span data-ttu-id="b2652-283">ライセンス プレートは、販売処理者が注文を受けた際に記録して引当することができ、他の用途では取得できません。</span><span class="sxs-lookup"><span data-stu-id="b2652-283">A license plate can be recorded and reserved when the order is taken by the sales processor, and it can't be taken by other demands.</span></span> <span data-ttu-id="b2652-284">この動作により、計画されたライセンス プレートが顧客に出荷されることが保証されます。</span><span class="sxs-lookup"><span data-stu-id="b2652-284">This behavior helps guarantee that the license plate that was planned is shipped to the customer.</span></span>
- <span data-ttu-id="b2652-285">ライセンス プレートが販売注文明細行に割り当てられていない場合は、販売注文の登録および引当が完了した後、倉庫の担当者がピッキング作業中にライセンス プレートを選択することができます。</span><span class="sxs-lookup"><span data-stu-id="b2652-285">If the license plate isn't already assigned to a sales order line, warehouse personnel can select a license plate during picking work, after sales order registration and reservation are completed.</span></span>

### <a name="turn-on-flexible-license-plate-reservation"></a><span data-ttu-id="b2652-286">柔軟なライセンス プレートの引当を有効化する</span><span class="sxs-lookup"><span data-stu-id="b2652-286">Turn on flexible license plate reservation</span></span>

<span data-ttu-id="b2652-287">柔軟なライセンス プレートの引当を利用する前に、システムで2つの機能を有効化しておく必要があります。</span><span class="sxs-lookup"><span data-stu-id="b2652-287">Before you can use flexible license plate reservation, two features must be turned on in your system.</span></span> <span data-ttu-id="b2652-288">管理者は、[機能の管理](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md)設定を使用して、機能の状態を確認し、必要に応じて有効化することができます。</span><span class="sxs-lookup"><span data-stu-id="b2652-288">Admins can use the [feature management](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) settings to check the status of the features and turn them on if they are required.</span></span> <span data-ttu-id="b2652-289">これら機能は、次の順序で有効にする必要があります :</span><span class="sxs-lookup"><span data-stu-id="b2652-289">You must turn on the features in the following order:</span></span>

1. <span data-ttu-id="b2652-290">**機能名 :** *柔軟な倉庫レベル分析コードの引当ポリシー*</span><span class="sxs-lookup"><span data-stu-id="b2652-290">**Feature name:** *Flexible warehouse-level dimension reservation*</span></span>
1. <span data-ttu-id="b2652-291">**機能名 :** *柔軟な注文 - コミットされたライセンス プレートの引当*</span><span class="sxs-lookup"><span data-stu-id="b2652-291">**Feature name:** *Flexible order-committed license plate reservation*</span></span>

### <a name="reserve-a-specific-license-plate-on-the-sales-order"></a><span data-ttu-id="b2652-292">販売注文に基づく特定のライセンス プレートの引当</span><span class="sxs-lookup"><span data-stu-id="b2652-292">Reserve a specific license plate on the sales order</span></span>

<span data-ttu-id="b2652-293">注文に基づくライセンス プレートの引当を有効にするには、関連するアイテムに関連付けられている階層の **在庫引当階層** ページで、**ライセンスプレート** レベルの **オンデマンド引当を許可する** チェック ボックスを選択する必要があります。</span><span class="sxs-lookup"><span data-stu-id="b2652-293">To enable license plate reservation on an order, you must select the **Allow reservation on demand order** check box for the **License plate** level on the **Inventory reservation hierarchies** page for the hierarchy that is associated with the relevant item.</span></span>

![柔軟なライセンス プレートの引当階層で使用する在庫引当階層ページ](media/Flexible-LP-reservation-hierarchy.png)

<span data-ttu-id="b2652-295">デプロイのどの時点であっても、注文時にライセンス プレートの引当を有効化できます。</span><span class="sxs-lookup"><span data-stu-id="b2652-295">You can enable license plate reservation on the order at any point in your deployment.</span></span> <span data-ttu-id="b2652-296">この変更は、変更が発生する前に作成された引当や未処理の倉庫作業には影響しません。</span><span class="sxs-lookup"><span data-stu-id="b2652-296">This change won't affect any reservations or open warehouse work that were created before the change occurred.</span></span> <span data-ttu-id="b2652-297">ただし、その予約階層に関連付けられている1つ以上のアイテムに対して、*注文中*、*引当済注文*、または *引当済現物* の発行ステータスを持つ、処理中の在庫出荷トランザクションが存在する場合は、**オンデマンド引当を許可する** チェック ボックスをクリアすることはできません。</span><span class="sxs-lookup"><span data-stu-id="b2652-297">However, you can't clear the **Allow reservation on demand order** check box if open outbound inventory transactions that have an issue status of *On order*, *Reserved ordered*, or *Reserved physical* exist for one or more items that are associated with that reservation hierarchy.</span></span>

<span data-ttu-id="b2652-298">**ライセンス プレート** レベルで **オンデマンド引当を許可する** のチェックボックスがオンの場合であっても、注文に対して特定のライセンス プレートを引当 *しない* ことは可能です。</span><span class="sxs-lookup"><span data-stu-id="b2652-298">Even if the **Allow reservation on demand order** check box is selected for the **License plate** level, it's still possible *not* to reserve a specific license plate on the order.</span></span> <span data-ttu-id="b2652-299">この場合、引当階層に対して有効な既定の倉庫の運用ロジックが適用されます。</span><span class="sxs-lookup"><span data-stu-id="b2652-299">In this case, the default warehouse operations logic that is valid for the reservation hierarchy applies.</span></span>

<span data-ttu-id="b2652-300">特定のライセンス契約を作成するために、[Open Data Protocol (OData)](../../fin-ops-core/dev-itpro/data-entities/odata.md) プロセスを使用する必要があります。</span><span class="sxs-lookup"><span data-stu-id="b2652-300">To reserve a specific license plate, you must use an [Open Data Protocol (OData)](../../fin-ops-core/dev-itpro/data-entities/odata.md) process.</span></span> <span data-ttu-id="b2652-301">アプリケーションでは、**Excelで開く** コマンドの **ライセンス 操作で使用する注文確定済引当て** オプションを使用して、販売注文から直接この引当を実行できます。</span><span class="sxs-lookup"><span data-stu-id="b2652-301">In the application, you can do this reservation directly from a sales order by using the **Order-committed reservations per license plate** option of the **Open in Excel** command.</span></span> <span data-ttu-id="b2652-302">Excel アドインで開いたエンティティ データでは、次の引当に関連するデータを入力し、**発行** を選択して、Supply Chain Managementにデータを返送する必要があります :</span><span class="sxs-lookup"><span data-stu-id="b2652-302">In the entity data that is opened in the Excel add-in, you must enter the following reservation-related data and then select **Publish** to send the data back to Supply Chain Management:</span></span>

- <span data-ttu-id="b2652-303">参照 (*販売注文* の値のみに対応しています)</span><span class="sxs-lookup"><span data-stu-id="b2652-303">Reference (Only the *Sales order* value is supported.)</span></span>
- <span data-ttu-id="b2652-304">注文番号 (値はロットから派生させることができます)</span><span class="sxs-lookup"><span data-stu-id="b2652-304">Order number (The value can be derived from the lot.)</span></span>
- <span data-ttu-id="b2652-305">ロット ID</span><span class="sxs-lookup"><span data-stu-id="b2652-305">Lot ID</span></span>
- <span data-ttu-id="b2652-306">ライセンス プレート</span><span class="sxs-lookup"><span data-stu-id="b2652-306">License plate</span></span>
- <span data-ttu-id="b2652-307">件数</span><span class="sxs-lookup"><span data-stu-id="b2652-307">Quantity</span></span>

<span data-ttu-id="b2652-308">一括追跡された特定のライセンス プレートを引当する必要がある場合は、[販売注文の詳細を入力する](#sales-order-details)の項目に記載されているように、**バッチ引当** ページを使用してください。</span><span class="sxs-lookup"><span data-stu-id="b2652-308">If you must reserve a specific license plate for a batch-tracked item, use the **Batch reservation** page, as described in the [Enter sales order details](#sales-order-details) section.</span></span>

<span data-ttu-id="b2652-309">倉庫業務で注文でコミットされたライセンス プレートの引当を使用した販売注文明細行が処理されている場合、ロケーションの指示は使用されません。</span><span class="sxs-lookup"><span data-stu-id="b2652-309">When the sales order line that uses an order-committed license plate reservation is processed by warehouse operations, location directives aren't used.</span></span>

<span data-ttu-id="b2652-310">倉庫の作業項目が完全なパレットと同じラインで構成されており、ライセンス プレートがコミットされた数量である場合、モバイル デバイスのメニュー項目を使用して、**ライセンス プレートで処理する** オプションが *はい* に設定することで、ピッキング プロセスを最適化できます。</span><span class="sxs-lookup"><span data-stu-id="b2652-310">If a warehouse work item consists of lines that equal a complete pallet and have license plate–committed quantities, you can optimize the picking process by using a mobile device menu item where the **Handle by license plate** option is set to *Yes*.</span></span> <span data-ttu-id="b2652-311">その後、倉庫の作業員は、作業中の品目をつずつスキャンする代わりに、ライセンス プレートをスキャンしてピック作業を完了させることができます。</span><span class="sxs-lookup"><span data-stu-id="b2652-311">A warehouse worker can then scan a license plate to complete a pick instead of having to scan the items from the work one by one.</span></span>

![[ライセンス プレートで処理する]オプションが「はい」に設定されているモバイル デバイスのメニュー項目](media/Handle-by-LP-menu-item.png)

<span data-ttu-id="b2652-313">**ライセンス プレートで処理する** 機能では複数のパレットを対象とする作業に対応していないため、ライセンス プレートごとに別の作業項目を用意することをお勧めします。</span><span class="sxs-lookup"><span data-stu-id="b2652-313">Because the **Handle by license plate** functionality doesn't support work that covers multiple pallets, it's better to have a separate work item for different license plates.</span></span> <span data-ttu-id="b2652-314">この方法を使用するには、**作業テンプレート** ページの作業ヘッダーの区切りに、**注文がコミットされたライセンス プレートの ID** のフィールドを追加します。</span><span class="sxs-lookup"><span data-stu-id="b2652-314">To use this approach, add the **Order-committed license plate ID** field as a work header break on the **Work template** page.</span></span>

> [!NOTE]
> <span data-ttu-id="b2652-315">注文がコミットされた作業作成プロセスでは、"注文がコミットされた在庫分析コード" 値はピッキング作業明細行に割り当てられ、ライセンス プレート値を直接表示することはできません。</span><span class="sxs-lookup"><span data-stu-id="b2652-315">For the order-committed work creation process, an "order-committed inventory dimension" value will be assigned to the picking work lines, and it won't be possible to view the license plate value directly.</span></span> <span data-ttu-id="b2652-316">モバイル デバイスのメニュー項目を設定する場合は、*ユーザー主導* プロセスのみがサポートされます。</span><span class="sxs-lookup"><span data-stu-id="b2652-316">Only the *User directed* process is supported when setting up a mobile device menu item.</span></span>

## <a name="example-scenario-set-up-and-process-an-order-committed-license-plate-reservation"></a><span data-ttu-id="b2652-317">シナリオ例 : 注文をコミットしてライセンス プレートの引当を設定して処理する</span><span class="sxs-lookup"><span data-stu-id="b2652-317">Example scenario: Set up and process an order-committed license plate reservation</span></span>

<span data-ttu-id="b2652-318">このシナリオでは、注文がコミットされたライセンス プレートの引当を設定して処理する方法を説明します。</span><span class="sxs-lookup"><span data-stu-id="b2652-318">This scenario shows how to set up and process an order-committed license plate reservation.</span></span>

### <a name="make-demo-data-available"></a><span data-ttu-id="b2652-319">デモ データを有効化する</span><span class="sxs-lookup"><span data-stu-id="b2652-319">Make demo data available</span></span>

<span data-ttu-id="b2652-320">このシナリオでは、Supply Chain Management に向けて提供されている標準のデモデータに含まれる値とレコードを参照しています。</span><span class="sxs-lookup"><span data-stu-id="b2652-320">This scenario refers to values and records that are included in the standard demo data that is provided for Supply Chain Management.</span></span> <span data-ttu-id="b2652-321">ここで提供されている値を使ってシナリオを進める場合は、必ずデモ データがインストールされている環境で作業を行ってください。</span><span class="sxs-lookup"><span data-stu-id="b2652-321">If you want to work through the scenario by using the values that are provided here, be sure to work on an environment where the demo data is installed.</span></span> <span data-ttu-id="b2652-322">また、開始する前に法人を **USMF** に設定しておく必要があります。</span><span class="sxs-lookup"><span data-stu-id="b2652-322">Additionally, set the legal entity to **USMF** before you begin.</span></span>

### <a name="create-an-inventory-reservation-hierarchy-that-allows-for-license-plate-reservation"></a><span data-ttu-id="b2652-323">ライセンス プレートの引当を許可する在庫引当の階層を作成する</span><span class="sxs-lookup"><span data-stu-id="b2652-323">Create an inventory reservation hierarchy that allows for license plate reservation</span></span>

1. <span data-ttu-id="b2652-324">**倉庫管理 \> 設定 \> 在庫 \> 引当階層** に移動します。</span><span class="sxs-lookup"><span data-stu-id="b2652-324">Go to **Warehouse management \> Setup \> Inventory \> Reservation hierarchy**.</span></span>
1. <span data-ttu-id="b2652-325">**新規** を選択します。</span><span class="sxs-lookup"><span data-stu-id="b2652-325">Select **New**.</span></span>
1. <span data-ttu-id="b2652-326">**名前** フィールドに、値を入力します (例 : *FlexibleLP*)。</span><span class="sxs-lookup"><span data-stu-id="b2652-326">In the **Name** field, enter a value (for example, *FlexibleLP*).</span></span>
1. <span data-ttu-id="b2652-327">**説明** フィールドに、値を入力します (例 : *柔軟な LP 引当*)。</span><span class="sxs-lookup"><span data-stu-id="b2652-327">In the **Description** field, enter a value (for example, *Flexible LP reservation*).</span></span>
1. <span data-ttu-id="b2652-328">**選択済** 一覧で、 **バッチ番号**、**シリアル番号**、**所有者** を選択します。</span><span class="sxs-lookup"><span data-stu-id="b2652-328">In the **Selected** list, select **Batch number**, **Serial number**, and **Owner**.</span></span>
1. <span data-ttu-id="b2652-329">**削除** ボタン![後向き矢印](media/backward-button.png) を選択して、フィールドを **利用可能** 一覧に移動します。</span><span class="sxs-lookup"><span data-stu-id="b2652-329">Select the **Remove** button ![backward arrow](media/backward-button.png) to move the selected records to the **Available** list.</span></span>
1. <span data-ttu-id="b2652-330">**OK** を選択します。</span><span class="sxs-lookup"><span data-stu-id="b2652-330">Select **OK**.</span></span>
1. <span data-ttu-id="b2652-331">**ライセンス プレート** 分析コード レベルの行で、**オンデマンド引当を許可する** チェック ボックスを選択します。</span><span class="sxs-lookup"><span data-stu-id="b2652-331">In the row for the **License plate** dimension level, select the **Allow reservation on demand order** check box.</span></span> <span data-ttu-id="b2652-332">**ロケーション** レベルは自動的に選択されるため、チェック ボックスをクリアすることはできません。</span><span class="sxs-lookup"><span data-stu-id="b2652-332">The **Location** level is automatically selected, and you can't clear the check box for it.</span></span>
1. <span data-ttu-id="b2652-333">**保存** を選択します。</span><span class="sxs-lookup"><span data-stu-id="b2652-333">Select **Save**.</span></span>

### <a name="create-two-released-products"></a><span data-ttu-id="b2652-334">リリース済製品を2つ作成する</span><span class="sxs-lookup"><span data-stu-id="b2652-334">Create two released products</span></span>

1. <span data-ttu-id="b2652-335">**製品管理情報 \> 製品 \> リリースされた製品** の順に移動します。</span><span class="sxs-lookup"><span data-stu-id="b2652-335">Go to **Product information management \> Products \> Released products**.</span></span>
1. <span data-ttu-id="b2652-336">アクション ウィンドウで、**新規** を選択します。</span><span class="sxs-lookup"><span data-stu-id="b2652-336">On the Action Pane, select **New**.</span></span>
1. <span data-ttu-id="b2652-337">**新製品** ダイアログ ボックスに次の値を設定します :</span><span class="sxs-lookup"><span data-stu-id="b2652-337">In the **New released product** dialog box, set the following values:</span></span>

    - <span data-ttu-id="b2652-338">**製品番号 :** *Item1*</span><span class="sxs-lookup"><span data-stu-id="b2652-338">**Product number:** *Item1*</span></span>
    - <span data-ttu-id="b2652-339">**品目番号:** *Item1*</span><span class="sxs-lookup"><span data-stu-id="b2652-339">**Item number:** *Item1*</span></span>
    - <span data-ttu-id="b2652-340">**品目モデル グループ :** *FIFO*</span><span class="sxs-lookup"><span data-stu-id="b2652-340">**Item model group:** *FIFO*</span></span>
    - <span data-ttu-id="b2652-341">**品目グループ :** *Audio*</span><span class="sxs-lookup"><span data-stu-id="b2652-341">**Item group:** *Audio*</span></span>
    - <span data-ttu-id="b2652-342">**保管分析コード グループ :** *Ware*</span><span class="sxs-lookup"><span data-stu-id="b2652-342">**Storage dimension group:** *Ware*</span></span>
    - <span data-ttu-id="b2652-343">**追跡用分析コード グループ :** *なし*</span><span class="sxs-lookup"><span data-stu-id="b2652-343">**Tracking dimension group:** *None*</span></span>
    - <span data-ttu-id="b2652-344">**引当階層:** *FlexibleLP*</span><span class="sxs-lookup"><span data-stu-id="b2652-344">**Reservation hierarchy:** *FlexibleLP*</span></span>

1. <span data-ttu-id="b2652-345">**OK** を選択して製品を作成し、ダイアログ ボックスを閉じます。</span><span class="sxs-lookup"><span data-stu-id="b2652-345">Select **OK** to create the product and close the dialog box.</span></span>
1. <span data-ttu-id="b2652-346">新製品が開きます。</span><span class="sxs-lookup"><span data-stu-id="b2652-346">The new product is opened.</span></span> <span data-ttu-id="b2652-347">**倉庫** クイック タブの **単位の順序グループ ID** フィールドに、*ea* と入力します。</span><span class="sxs-lookup"><span data-stu-id="b2652-347">On the **Warehouse** FastTab, set the **Unit sequence group ID** field to *ea*.</span></span>
1. <span data-ttu-id="b2652-348">前述の手順を繰り返して、2つ目の製品を同じ設定で作成し、**製品番号** と **品目番号** フィールドを *Item2* に設定します。</span><span class="sxs-lookup"><span data-stu-id="b2652-348">Repeat the previous steps to create a second product that has the same settings, but set the **Product number** and **Item number** fields to *Item2*.</span></span>
1. <span data-ttu-id="b2652-349">アクション ペインの **在庫の管理** タブの **表示** グループで、**手持ち在庫** を選択します。</span><span class="sxs-lookup"><span data-stu-id="b2652-349">On the Action Pane, on the **Manage inventory** tab, in the **View** group, select **On-hand inventory**.</span></span> <span data-ttu-id="b2652-350">続いて、**数量調整** を選択します。</span><span class="sxs-lookup"><span data-stu-id="b2652-350">Then select **Quantity adjustment**.</span></span>
1. <span data-ttu-id="b2652-351">以下の表で指定しているように、新しい品目の手持在庫を調整します。</span><span class="sxs-lookup"><span data-stu-id="b2652-351">Adjust the on-hand inventory of the new items as specified in the following table.</span></span>

    | <span data-ttu-id="b2652-352">項目</span><span class="sxs-lookup"><span data-stu-id="b2652-352">Item</span></span>  | <span data-ttu-id="b2652-353">倉庫</span><span class="sxs-lookup"><span data-stu-id="b2652-353">Warehouse</span></span> | <span data-ttu-id="b2652-354">ロケーション</span><span class="sxs-lookup"><span data-stu-id="b2652-354">Location</span></span> | <span data-ttu-id="b2652-355">ライセンス プレート</span><span class="sxs-lookup"><span data-stu-id="b2652-355">License plate</span></span> | <span data-ttu-id="b2652-356">件数</span><span class="sxs-lookup"><span data-stu-id="b2652-356">Quantity</span></span> |
    |-------|-----------|----------|---------------|----------|
    | <span data-ttu-id="b2652-357">Item1</span><span class="sxs-lookup"><span data-stu-id="b2652-357">Item1</span></span> | <span data-ttu-id="b2652-358">24</span><span class="sxs-lookup"><span data-stu-id="b2652-358">24</span></span>        | <span data-ttu-id="b2652-359">FL-010</span><span class="sxs-lookup"><span data-stu-id="b2652-359">FL-010</span></span>   | <span data-ttu-id="b2652-360">LP01</span><span class="sxs-lookup"><span data-stu-id="b2652-360">LP01</span></span>          | <span data-ttu-id="b2652-361">10</span><span class="sxs-lookup"><span data-stu-id="b2652-361">10</span></span>       |
    | <span data-ttu-id="b2652-362">Item1</span><span class="sxs-lookup"><span data-stu-id="b2652-362">Item1</span></span> | <span data-ttu-id="b2652-363">24</span><span class="sxs-lookup"><span data-stu-id="b2652-363">24</span></span>        | <span data-ttu-id="b2652-364">FL-011</span><span class="sxs-lookup"><span data-stu-id="b2652-364">FL-011</span></span>   | <span data-ttu-id="b2652-365">LP02</span><span class="sxs-lookup"><span data-stu-id="b2652-365">LP02</span></span>          | <span data-ttu-id="b2652-366">10</span><span class="sxs-lookup"><span data-stu-id="b2652-366">10</span></span>       |
    | <span data-ttu-id="b2652-367">Item2</span><span class="sxs-lookup"><span data-stu-id="b2652-367">Item2</span></span> | <span data-ttu-id="b2652-368">24</span><span class="sxs-lookup"><span data-stu-id="b2652-368">24</span></span>        | <span data-ttu-id="b2652-369">FL-010</span><span class="sxs-lookup"><span data-stu-id="b2652-369">FL-010</span></span>   | <span data-ttu-id="b2652-370">LP01</span><span class="sxs-lookup"><span data-stu-id="b2652-370">LP01</span></span>          | <span data-ttu-id="b2652-371">5</span><span class="sxs-lookup"><span data-stu-id="b2652-371">5</span></span>        |
    | <span data-ttu-id="b2652-372">Item2</span><span class="sxs-lookup"><span data-stu-id="b2652-372">Item2</span></span> | <span data-ttu-id="b2652-373">24</span><span class="sxs-lookup"><span data-stu-id="b2652-373">24</span></span>        | <span data-ttu-id="b2652-374">FL-011</span><span class="sxs-lookup"><span data-stu-id="b2652-374">FL-011</span></span>   | <span data-ttu-id="b2652-375">LP02</span><span class="sxs-lookup"><span data-stu-id="b2652-375">LP02</span></span>          | <span data-ttu-id="b2652-376">5</span><span class="sxs-lookup"><span data-stu-id="b2652-376">5</span></span>        |

    > [!NOTE]
    > <span data-ttu-id="b2652-377">2つのライセンス プレートを作成し、*FL-010* や *FL-011* などの混合品目を許容するロケーションを使用する必要があり ます。</span><span class="sxs-lookup"><span data-stu-id="b2652-377">You must create the two license plates and use locations that allow for mixed items, such as *FL-010* and *FL-011*.</span></span>

### <a name="create-a-sales-order-and-reserve-a-specific-license-plate"></a><span data-ttu-id="b2652-378">販売注文を作成して特定のライセンス プレートを引当する</span><span class="sxs-lookup"><span data-stu-id="b2652-378">Create a sales order and reserve a specific license plate</span></span>

1. <span data-ttu-id="b2652-379">**販売とマーケティング \> 販売注文 \> すべての販売注文** の順に移動します。</span><span class="sxs-lookup"><span data-stu-id="b2652-379">Go to **Sales and marketing \> Sales orders \> All sales orders**.</span></span>
1. <span data-ttu-id="b2652-380">**新規** を選択します。</span><span class="sxs-lookup"><span data-stu-id="b2652-380">Select **New**.</span></span>
1. <span data-ttu-id="b2652-381">**販売注文の作成** ダイアログ ボックスでは、次の値を設定します。</span><span class="sxs-lookup"><span data-stu-id="b2652-381">In the **Create sales order** dialog box, set the following values:</span></span>

    - <span data-ttu-id="b2652-382">**顧客アカウント:** *US-001*</span><span class="sxs-lookup"><span data-stu-id="b2652-382">**Customer account:** *US-001*</span></span>
    - <span data-ttu-id="b2652-383">**倉庫:** *24*</span><span class="sxs-lookup"><span data-stu-id="b2652-383">**Warehouse:** *24*</span></span>

1. <span data-ttu-id="b2652-384">**OK** を選択して **販売注文の作成** ダイアログ ボックスを閉じ、新規販売注文を開きます。</span><span class="sxs-lookup"><span data-stu-id="b2652-384">Select **OK** to close the **Create sales order** dialog box and open the new sales order.</span></span>
1. <span data-ttu-id="b2652-385">**販売注文明細行** クイックタブで、次の設定で明細行を追加します :</span><span class="sxs-lookup"><span data-stu-id="b2652-385">On the **Sales order lines** FastTab, add a line that has the following settings:</span></span>

    - <span data-ttu-id="b2652-386">**品目番号:** *Item1*</span><span class="sxs-lookup"><span data-stu-id="b2652-386">**Item number:** *Item1*</span></span>
    - <span data-ttu-id="b2652-387">**数量:** *10*</span><span class="sxs-lookup"><span data-stu-id="b2652-387">**Quantity:** *10*</span></span>

1. <span data-ttu-id="b2652-388">以下の設定で 2 つ目の販売注文明細行を作成します :</span><span class="sxs-lookup"><span data-stu-id="b2652-388">Add a second sales order line that has the following settings:</span></span>

    - <span data-ttu-id="b2652-389">**品目番号:** *Item2*</span><span class="sxs-lookup"><span data-stu-id="b2652-389">**Item number:** *Item2*</span></span>
    - <span data-ttu-id="b2652-390">**数量:** *5*</span><span class="sxs-lookup"><span data-stu-id="b2652-390">**Quantity:** *5*</span></span>

1. <span data-ttu-id="b2652-391">**保存** を選択します。</span><span class="sxs-lookup"><span data-stu-id="b2652-391">Select **Save**.</span></span>
1. <span data-ttu-id="b2652-392">**明細行の詳細** クイックタブの **設定** タブで、各行の **ロット ID** の値をメモします。</span><span class="sxs-lookup"><span data-stu-id="b2652-392">On the **Line details** FastTab, on the **Setup** tab, make a note of the **Lot ID** value for each line.</span></span> <span data-ttu-id="b2652-393">これらの値は、該当するライセンス プレートの引当時に必要になります。</span><span class="sxs-lookup"><span data-stu-id="b2652-393">These values will be required during reservation of specific license plates.</span></span>

    > [!NOTE]
    > <span data-ttu-id="b2652-394">特定のライセンス プレートを引当するには、**ライセンス プレートごとに注文がコミットされた引当** のデータエンティティを使用する必要があり ます。</span><span class="sxs-lookup"><span data-stu-id="b2652-394">To reserve a specific license plate, you must use the **Order-committed reservations per license plate** data entity.</span></span> <span data-ttu-id="b2652-395">特定のライセンス  プレートでバッチ引当をするには、[販売注文の詳細を入力する](#sales-order-details)セクションで説明されているとおり、**バッチ引当** ページを利用することもできます。</span><span class="sxs-lookup"><span data-stu-id="b2652-395">To reserve a batch-tracked item on a specific license plate, you can also use the **Batch reservation** page, as described in the [Enter sales order details](#sales-order-details) section.</span></span>
    >
    > <span data-ttu-id="b2652-396">ライセンス プレートを販売注文明細行に直接入力してシステムに確認した場合、その明細行には倉庫管理の処理は使用されません。</span><span class="sxs-lookup"><span data-stu-id="b2652-396">If you enter the license plate directly on the sales order line and confirm it to the system, warehouse management processing won't be used for the line.</span></span>

1. <span data-ttu-id="b2652-397">**Microsoft Office で開く** を選択し、**ライセンス プレートごとに注文がコミットされた引当** を選択し、ファイルをダウンロードします。</span><span class="sxs-lookup"><span data-stu-id="b2652-397">Select **Open in Microsoft Office**, select **Order-committed reservations per license plate**, and download the file.</span></span>
1. <span data-ttu-id="b2652-398">ファイルをダウンロードして Excel で開き、**編集機能を有効にする** を選択し、Excel アドインが実行されるようにします。</span><span class="sxs-lookup"><span data-stu-id="b2652-398">Open the downloaded file in Excel, and select **Enable editing** to enable the Excel add-in to run.</span></span>
1. <span data-ttu-id="b2652-399">初めて Excel アドインを実行する場合は、**このアドインを信頼します** を選択します。</span><span class="sxs-lookup"><span data-stu-id="b2652-399">If you're running the Excel add-in for the first time, select **Trust this Add-in**.</span></span>
1. <span data-ttu-id="b2652-400">サインインを促すメッセージが表示されたら、**サインイン** を選択し、Supply Chain Management へのサインインで使用しているものと同じ資格情報を用いてサインインします。</span><span class="sxs-lookup"><span data-stu-id="b2652-400">If you're prompted to sign in, select **Sign in**, and then sign in by using the same credentials that you used to sign in to Supply Chain Management.</span></span>
1. <span data-ttu-id="b2652-401">特定のライセンスプレートで品目を引当するには、Excelアドインで、**新規** を選択して引当明細行を追加し、次の値を設定します :</span><span class="sxs-lookup"><span data-stu-id="b2652-401">To reserve an item on a specific license plate, in the Excel add-in, select **New** to add a reservation line, and then set the following values:</span></span>

    - <span data-ttu-id="b2652-402">**ロット ID :** *Item1* の販売注文明細行の **ロット ID** の値を入力します。</span><span class="sxs-lookup"><span data-stu-id="b2652-402">**Lot ID:** Enter the **Lot ID** value that you found for the sales order line for *Item1*.</span></span>
    - <span data-ttu-id="b2652-403">**ライセンス プレート :** *LP02*</span><span class="sxs-lookup"><span data-stu-id="b2652-403">**License plate:** *LP02*</span></span>
    - <span data-ttu-id="b2652-404">**ReservedInventoryQuantity:** *10*</span><span class="sxs-lookup"><span data-stu-id="b2652-404">**ReservedInventoryQuantity:** *10*</span></span>

1. <span data-ttu-id="b2652-405">**新規** を選択して別の引当明細行を追加し、次の値を設定します :</span><span class="sxs-lookup"><span data-stu-id="b2652-405">Select **New** to add another reservation line, and set the following values:</span></span>

    - <span data-ttu-id="b2652-406">**ロット ID :** *Item2* の販売注文明細行の **ロット ID** の値を入力します。</span><span class="sxs-lookup"><span data-stu-id="b2652-406">**Lot ID:** Enter the **Lot ID** value you found for the sales order line for *Item2*.</span></span>
    - <span data-ttu-id="b2652-407">**ライセンス プレート :** *LP02*</span><span class="sxs-lookup"><span data-stu-id="b2652-407">**License plate:** *LP02*</span></span>
    - <span data-ttu-id="b2652-408">**ReservedInventoryQuantity:** *5*</span><span class="sxs-lookup"><span data-stu-id="b2652-408">**ReservedInventoryQuantity:** *5*</span></span>

1. <span data-ttu-id="b2652-409">Excel アドインで Supply Chain Management にデータを返送するには、**発行** を選択します。</span><span class="sxs-lookup"><span data-stu-id="b2652-409">In the Excel add-in, select **Publish** to send the data back to Supply Chain Management.</span></span>

    > [!NOTE]
    > <span data-ttu-id="b2652-410">引当明細行は、エラーなく発行が完了した場合にのみ、システムに表示されます。</span><span class="sxs-lookup"><span data-stu-id="b2652-410">The reservation line will appear in the system only if publishing is completed without errors.</span></span>

1. <span data-ttu-id="b2652-411">Supply Chain Management に戻ります。</span><span class="sxs-lookup"><span data-stu-id="b2652-411">Go back to Supply Chain Management.</span></span> 
1. <span data-ttu-id="b2652-412">品目の引当を確認するには、**販売注文明細行** クイックタブの、**在庫** メニューで、**管理 \> 引当** を選択します。</span><span class="sxs-lookup"><span data-stu-id="b2652-412">To review the item's reservation, on the **Sales order lines** FastTab, on the **Inventory** menu, select **Maintain \> Reservation**.</span></span> <span data-ttu-id="b2652-413">*Item1* の販売注文明細行では、在庫のうち *10* が引当されており、*Item2* の販売注文明細行では、在庫のうち *5* が引当されていることに注意してください。</span><span class="sxs-lookup"><span data-stu-id="b2652-413">Notice that, for the sales order line for *Item1*, inventory of *10* is reserved, and for the sales order line for *Item2*, inventory of *5* is reserved.</span></span>
1. <span data-ttu-id="b2652-414">販売注文明細行の引当に関連する在庫トランザクションを確認するには、**販売注文明細行** クイックタブの **在庫** メニューで **表示 \> トランザクション** を選択します。</span><span class="sxs-lookup"><span data-stu-id="b2652-414">To review inventory transactions that are related to the sales order line reservation, on the **Sales order lines** FastTab, on the **Inventory** menu, select **View \> Transactions**.</span></span> <span data-ttu-id="b2652-415">引当に関連する2つのトランザクションが存在することに注目してください : ひとつは **参照** フィールドが *販売注文* に設定されているもので、もうひとつは **参照** フィールドが *注文がコミットされた引当* に設定されているものです。</span><span class="sxs-lookup"><span data-stu-id="b2652-415">Notice that there are two transactions that are related to the reservation: one where the **Reference** field is set to *Sales order* and one where the **Reference** field is set to *Order-committed reservation*.</span></span>

    > [!NOTE]
    > <span data-ttu-id="b2652-416">**参照** フィールドが *販売注文* に設定されているトランザクションは、**ロケーション** レベル (サイト、倉庫、在庫状況) 以上の在庫分析コードの注文明細行の引当を表しています。</span><span class="sxs-lookup"><span data-stu-id="b2652-416">A transaction where the **Reference** field is set to *Sales order* represents the order line reservation for inventory dimensions that are above the **Location** level (site, warehouse, and inventory status).</span></span> <span data-ttu-id="b2652-417">**参照** フィールドが、*注文がコミットされた引当* に設定されているトランザクションは、特定のライセンス プレートとロケーションに対する注文明細行の引当を表しています。</span><span class="sxs-lookup"><span data-stu-id="b2652-417">A transaction where the **Reference** field is set to *Order-committed reservation* represents the order line reservation for the specific license plate and location.</span></span>

1. <span data-ttu-id="b2652-418">販売注文をリリースするには、**アクション** グループ内の **倉庫** タブのアクション ペインで、**倉庫へのリリース** を選択します。</span><span class="sxs-lookup"><span data-stu-id="b2652-418">To release the sales order, on the Action Pane, on the **Warehouse** tab, in the **Actions** group, select **Release to warehouse**.</span></span>

### <a name="review-and-process-warehouse-work-with-order-committed-license-plates-assigned"></a><span data-ttu-id="b2652-419">注文がコミットされたライセンス プレートを割り当てられた倉庫作業の確認とプロセス</span><span class="sxs-lookup"><span data-stu-id="b2652-419">Review and process warehouse work with order-committed license plates assigned</span></span>

1. <span data-ttu-id="b2652-420">**販売注文明細行** クイック タブの **倉庫** メニューで、**作業詳細** を選択します。</span><span class="sxs-lookup"><span data-stu-id="b2652-420">On the **Sales order lines** FastTab, on the **Warehouse** menu, select **Work details**.</span></span>

    <span data-ttu-id="b2652-421">特定のバッチ引当の場合、ライセンス プレートの引当を利用した販売注文の作業を作成する際に、システムはロケーションの指示を利用しません。</span><span class="sxs-lookup"><span data-stu-id="b2652-421">As when reservation is done for a specific batch, the system doesn't use location directives when it creates the work for the sales order that uses license plate reservation.</span></span> <span data-ttu-id="b2652-422">注文がコミットされた引当では、ロケーションを含むすべての在庫の分析コードが指定されているため、ロケーションの指示を利用する必要はありません。</span><span class="sxs-lookup"><span data-stu-id="b2652-422">Because the order-committed reservation specifies all the inventory dimensions, including the location, location directives don't have to be used, because those inventory dimensions are just entered in the work.</span></span> <span data-ttu-id="b2652-423">これらは、**作業在庫取引** ページの **在庫分析コード** のセクションに表示されています。</span><span class="sxs-lookup"><span data-stu-id="b2652-423">They are shown in the **From inventory dimensions** section on the **Work inventory transactions** page.</span></span>

    > [!NOTE]
    > <span data-ttu-id="b2652-424">作業の作成後は、**参照** フィールドが *注文がコミットされた引当* に設定されている品目の在庫トランザクションが削除されます。</span><span class="sxs-lookup"><span data-stu-id="b2652-424">After the work is created, the item's inventory transaction where the **Reference** field is set to *Order-committed reservation* is removed.</span></span> <span data-ttu-id="b2652-425">**参照** フィールドが *作業* に設定されている在庫トランザクションは、すべての数量の在庫分析コードに対して現物引当を保持するようになります。</span><span class="sxs-lookup"><span data-stu-id="b2652-425">The inventory transaction where the **Reference** field is set to *Work* now holds the physical reservation for all the quantity's inventory dimensions.</span></span>

1. <span data-ttu-id="b2652-426">モバイル デバイスで、**ライセンス プレートで処理する** チェック ボックスがオンになっているメニュー項目を使用してピッキングと作業を完了します。</span><span class="sxs-lookup"><span data-stu-id="b2652-426">On the mobile device, finish picking and putting the work by using a menu item where the **Handle by license plate** check box is selected.</span></span>

    > [!NOTE]
    > <span data-ttu-id="b2652-427">**ライセンス プレートで処理する** 機能は、ライセンス プレート全体を処理する場合に役立ちます。</span><span class="sxs-lookup"><span data-stu-id="b2652-427">The **Handle by license plate** functionality helps you process the whole license plate.</span></span> <span data-ttu-id="b2652-428">ライセンスプレートの一部のみを処理する必要がある場合は、この機能を使用できません。</span><span class="sxs-lookup"><span data-stu-id="b2652-428">If you must process part of the license plate, you can't use this functionality.</span></span>
    >
    > <span data-ttu-id="b2652-429">ライセンス プレートごとに徳利手下の作業を生成することを推奨します。</span><span class="sxs-lookup"><span data-stu-id="b2652-429">We recommend that you have separate work generated for each license plate.</span></span> <span data-ttu-id="b2652-430">この結果を得るには、**作業テンプレート** ページの **作業用ヘッダーの区切り** 機能を使用し ます。</span><span class="sxs-lookup"><span data-stu-id="b2652-430">To achieve this result, use the **Work header breaks** feature on the **Work template** page.</span></span>

    <span data-ttu-id="b2652-431">ライセン スプレート *LP02* は、販売注文明細行でピッキングされ、ロケーション *Baydoor* に配置されます。</span><span class="sxs-lookup"><span data-stu-id="b2652-431">License plate *LP02* is now picked for sales order lines and put to the *Baydoor* location.</span></span> <span data-ttu-id="b2652-432">以上で積み込み準備と顧客への出荷準備が整いました。</span><span class="sxs-lookup"><span data-stu-id="b2652-432">At this point, it's ready to be loaded and dispatched to the customer.</span></span>

## <a name="exception-handling-of-warehouse-work-that-has-order-committed-batch-numbers"></a><span data-ttu-id="b2652-433">注文が確定したバッチ番号を持つ倉庫作業の例外処理</span><span class="sxs-lookup"><span data-stu-id="b2652-433">Exception handling of warehouse work that has order-committed batch numbers</span></span>

<span data-ttu-id="b2652-434">注文が確定したバッチ番号をピッキングする倉庫作業には、通常の作業と同じ標準の倉庫例外処理とアクションが適用されます。</span><span class="sxs-lookup"><span data-stu-id="b2652-434">Warehouse work for picking order-committed batch numbers is subject to the same standard warehouse exception handling and actions as regular work.</span></span> <span data-ttu-id="b2652-435">一般に、オープン作業または作業明細行はキャンセルされたり、ユーザーのロケーションがいっぱいになったために中断されたり、ショート ピッキングされたり、移動のために更新される可能性があります。</span><span class="sxs-lookup"><span data-stu-id="b2652-435">In general, the open work or work line can be canceled, it can be interrupted because a user location is full, it can be short-picked, and it can be updated because of a movement.</span></span> <span data-ttu-id="b2652-436">同様に、既に完了した作業のピッキング済数量を減らすことも、または作業を取り消すこともできます。</span><span class="sxs-lookup"><span data-stu-id="b2652-436">Likewise, the picked quantity of work that has already been completed can be reduced, or the work can be reversed.</span></span>

<span data-ttu-id="b2652-437">これらのすべての例外処理アクションに次の主要なルールが適用されます。顧客に対して引当されているバッチ番号を別のバッチ番号に置き換えられることはありませんが、保管分析コード　(ロケーションおよびライセン スプレート) は、ユーザーによる手動更新またはシステムによる自動更新によって変更できます。</span><span class="sxs-lookup"><span data-stu-id="b2652-437">The following key rule is applied to all these exception handling actions: the batch number that was reserved for the customer can never be replaced with a different batch number, but its storage dimensions (location and license plate) can be changed through either a manual update by the user or an automatic update by the system.</span></span> <span data-ttu-id="b2652-438">自動更新は、特定のバッチが自動的に引当され、保管分析コードが指定されていない場合に適用される保管分析コードのランダムな割り当てに基づいています。</span><span class="sxs-lookup"><span data-stu-id="b2652-438">The automatic update is based on the same random assignment of storage dimensions that applied when a specific batch was automatically reserved but no storage dimensions were specified.</span></span>

### <a name="example-scenario"></a><span data-ttu-id="b2652-439">シナリオ例</span><span class="sxs-lookup"><span data-stu-id="b2652-439">Example scenario</span></span>

<span data-ttu-id="b2652-440">このシナリオの例としては、**ピッキング済数量の削減** 機能を使用して、以前に完了した作業を解除している状況です。</span><span class="sxs-lookup"><span data-stu-id="b2652-440">An example of this scenario is a situation where previously completed work is being unpicked by using the **Reduce picked quantity** function.</span></span> <span data-ttu-id="b2652-441">この例は、[シナリオ例 : バッチ番号の割り当て](#Example-batch-allocation)で説明されている手順が既に完了していることを前提としています。</span><span class="sxs-lookup"><span data-stu-id="b2652-441">This example assumes that you've already completed the steps that are described in [Example scenario: Batch number allocation](#Example-batch-allocation).</span></span> <span data-ttu-id="b2652-442">ここでは、そのシナリオ例の続きを行います。</span><span class="sxs-lookup"><span data-stu-id="b2652-442">It continues from that example.</span></span>

1. <span data-ttu-id="b2652-443">**倉庫管理** \> **積荷** \> **有効な積荷** に移動します。</span><span class="sxs-lookup"><span data-stu-id="b2652-443">Go to **Warehouse management** \> **Loads** \> **Active loads**.</span></span>
2. <span data-ttu-id="b2652-444">販売注文の出荷に関連して作成された積荷を選択します。</span><span class="sxs-lookup"><span data-stu-id="b2652-444">Select the load that was created in connection with the shipment of your sales order.</span></span>
3. <span data-ttu-id="b2652-445">**積荷注文明細行数** クイック タブから、**ピッキング済数量の削減** を選択します。</span><span class="sxs-lookup"><span data-stu-id="b2652-445">From the **Load order lines** FastTab, select **Reduce picked quantity**.</span></span>
4. <span data-ttu-id="b2652-446">**ピッキング済数量の削減** ページの **ロケーションに移動する** フィールドで、**FL-001** を選択します。</span><span class="sxs-lookup"><span data-stu-id="b2652-446">On the **Reduce picked quantity** page, in the **Move to location** field, select **FL-001**.</span></span>
5. <span data-ttu-id="b2652-447">**ライセンス プレートに移動する** フィールドで、**LP33** を選択します。</span><span class="sxs-lookup"><span data-stu-id="b2652-447">In the **Move to license plate** field, select **LP33**.</span></span>
6. <span data-ttu-id="b2652-448">グリッドで、**ピッキングを解除する在庫数量** フィールドに **10** と入力します。</span><span class="sxs-lookup"><span data-stu-id="b2652-448">In the grid, in the **Inventory quantity to unpick** field, enter **10**.</span></span>
7. <span data-ttu-id="b2652-449">**OK** を選択します。</span><span class="sxs-lookup"><span data-stu-id="b2652-449">Select **OK**.</span></span>

<span data-ttu-id="b2652-450">ピッキング解除アクションの実行結果は次のようになります。</span><span class="sxs-lookup"><span data-stu-id="b2652-450">Here are the results of the unpicking action:</span></span>

- <span data-ttu-id="b2652-451">以前に終了した作業のステータスは、**キャンセル済** に設定されます。</span><span class="sxs-lookup"><span data-stu-id="b2652-451">The status of the previously closed work is set to **Canceled**.</span></span>
- <span data-ttu-id="b2652-452">バッチ番号 **B11** の **10** のピッキング済ではない数量に対して、**在庫移動** タイプの新しい作業が作成されます。</span><span class="sxs-lookup"><span data-stu-id="b2652-452">New work of the **Inventory movement** type is created for the unpicked quantity of **10** for batch number **B11**.</span></span> <span data-ttu-id="b2652-453">この作業は、**ベイドア** のロケーションから、**FL-001** のロケーションのライセンス プレート **LP33** への移動を表しています。</span><span class="sxs-lookup"><span data-stu-id="b2652-453">This work represents the movement from the **Baydoor** location to license plate **LP33** in location **FL-001**.</span></span> <span data-ttu-id="b2652-454">ステータスは **終了済** に設定されます。</span><span class="sxs-lookup"><span data-stu-id="b2652-454">The status is set to **Closed**.</span></span>
- <span data-ttu-id="b2652-455">システムは、元の注文バッチ番号を再度準備し、ロケーションとライセンス プレート ID を割り当てます。</span><span class="sxs-lookup"><span data-stu-id="b2652-455">The system re-reserves the batch number that was originally ordered, and assigns the location and license plate IDs.</span></span> <span data-ttu-id="b2652-456">(このプロセスは、指定されたバッチ番号の注文明細行に対して **引当行** 機能を実行することと同じです)。</span><span class="sxs-lookup"><span data-stu-id="b2652-456">(This process is equivalent to running the **Reserve line** function for the order line for a given batch number).</span></span> <span data-ttu-id="b2652-457">その結果、バッチ **B11** は、**バッチ引当** ページの **ソース明細行に確定済みのバッチ番号** クイック タブに確定済みとして表示され、**引当** フィールドには、バッチ番号 **B11** の数量 **10** が含まれています。</span><span class="sxs-lookup"><span data-stu-id="b2652-457">As a result, batch **B11** is shown as committed on the **Batch numbers committed to source line** FastTab of the **Batch reservation** page, and the **Reservation** field contains a quantity of **10** for batch number **B11**.</span></span> <span data-ttu-id="b2652-458">さらに、**ロケーション** フィールドは **FL-001** に設定され、**ライセンス プレート** フィールドは **LP11** に設定されます。</span><span class="sxs-lookup"><span data-stu-id="b2652-458">Additionally, the **Location** field is set to **FL-001**, and the **License plate** field is set to **LP11**.</span></span> <span data-ttu-id="b2652-459">(これらのフィールドが表示されていない場合は、グリッドに追加できます。)</span><span class="sxs-lookup"><span data-stu-id="b2652-459">(You can add these fields to the grid if they aren't visible.)</span></span>

<span data-ttu-id="b2652-460">次の表は、特定の倉庫アクションの注文が確定したバッチ引当をシステムが処理する方法を示す概要を示しています。</span><span class="sxs-lookup"><span data-stu-id="b2652-460">The following tables provide an overview that shows how the system handles order-committed batch reservation for specific warehouse actions.</span></span> <span data-ttu-id="b2652-461">テーブルのコンテンツを解釈するには、各倉庫アクションが注文が確定したバッチ引当から発生する既存の倉庫作業のコンテキストで実行されるか、各倉庫アクションの実行がそのタイプの作業に影響すると仮定します。</span><span class="sxs-lookup"><span data-stu-id="b2652-461">To interpret the content in the tables, assume that each warehouse action is run in the context of existing warehouse work that originates from an order-committed batch reservation, or that execution of each warehouse action affects work of that type.</span></span>

> [!NOTE]
> <span data-ttu-id="b2652-462">これらの表の「バッチ数量が利用可能」列は、現在の注文が確定した引当に対して既に引当されている数量、またはそのタイプの引当から発生する倉庫作業によって既に引当されている数量に加えて、バッチ数量が利用可能かどうかを示します。</span><span class="sxs-lookup"><span data-stu-id="b2652-462">In these tables, the "Batch quantity is available" column indicates whether a batch quantity is available in addition to the quantity that is either already reserved for the current order-committed reservations or already reserved by the warehouse work that originates from reservations of that type.</span></span>

#### <a name="override-the-pick-location-on-the-open-work"></a><span data-ttu-id="b2652-463">オープン作業のピッキングロケーションを上書きする</span><span class="sxs-lookup"><span data-stu-id="b2652-463">Override the pick location on the open work</span></span>

<table>
<thead>
<tr>
<th><span data-ttu-id="b2652-464">キー設定パラメーター</span><span class="sxs-lookup"><span data-stu-id="b2652-464">Key setup parameter</span></span></th>
<th><span data-ttu-id="b2652-465">バッチ数量が利用可能</span><span class="sxs-lookup"><span data-stu-id="b2652-465">Batch quantity is available</span></span></th>
<th><span data-ttu-id="b2652-466">主要なユーザーの手順</span><span class="sxs-lookup"><span data-stu-id="b2652-466">Key user steps</span></span></th>
<th><span data-ttu-id="b2652-467">倉庫作業</span><span class="sxs-lookup"><span data-stu-id="b2652-467">Warehouse work</span></span></th>
<th><span data-ttu-id="b2652-468">注文が確定したバッチ引当</span><span class="sxs-lookup"><span data-stu-id="b2652-468">Order-committed batch reservation</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td rowspan='2'><span data-ttu-id="b2652-469">作業者で<strong>ピッキング場所の上書きを許可</strong>オプションが有効になっている。</span><span class="sxs-lookup"><span data-stu-id="b2652-469">The <strong>Allow pick location override</strong> option is enabled on the worker.</span></span></td>
<td><span data-ttu-id="b2652-470">あり</span><span class="sxs-lookup"><span data-stu-id="b2652-470">Yes</span></span></td>
<td>
<ol>
<li><span data-ttu-id="b2652-471">ピッキング作業開始時に、倉庫管理 モバイルアプリの<strong>ロケーションの上書き</strong>メニュー項目を選択します。</span><span class="sxs-lookup"><span data-stu-id="b2652-471">Select the <strong>Override location</strong> menu item on the Warehouse Management mobile app when you start picking work.</span></span></li>
<li><span data-ttu-id="b2652-472"><strong>提案</strong>を選択します。</span><span class="sxs-lookup"><span data-stu-id="b2652-472">Select <strong>Suggest</strong>.</span></span></li>
<li><span data-ttu-id="b2652-473">バッチ数量の使用可能性に基づいて提案される新しいロケーションを確認します。</span><span class="sxs-lookup"><span data-stu-id="b2652-473">Confirm the new location that is suggested based on batch quantity availability.</span></span></li>
</ol>
</td>
<td><span data-ttu-id="b2652-474">現在の作業では、次のアクションが発生します。</span><span class="sxs-lookup"><span data-stu-id="b2652-474">On the current work, the following actions occur:</span></span>
<ul>
<li><span data-ttu-id="b2652-475">ピッキング行のロケーションが新しいロケーションに更新されます。</span><span class="sxs-lookup"><span data-stu-id="b2652-475">The location on the pick line is updated to the new location.</span></span> <span data-ttu-id="b2652-476">(ロケーションがライセンス プレートにより制御されている場合、ランダムなライセンス プレートが作業在庫トランザクションに割り当てられ、作業者は使用可能な数量があるライセンス プレートからピッキングできます。)</span><span class="sxs-lookup"><span data-stu-id="b2652-476">(If the location is license plate–controlled, a random license plate is assigned to the work inventory transaction, and the worker can pick from any license plate that has available quantity.)</span></span></li>
<li><span data-ttu-id="b2652-477">新しいロケーションで複数のライセンス プレートに数量が見つかった場合、元のピッキング行を複数の行に分割して、各ライセンス プレートに一致させることができます。</span><span class="sxs-lookup"><span data-stu-id="b2652-477">If the quantity is found on more than one license plate in the new location, the original pick line is split into multiple lines to match each license plate.</span></span></li>
</ul>
</td>
<td><span data-ttu-id="b2652-478">適用できません</span><span class="sxs-lookup"><span data-stu-id="b2652-478">Not applicable</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="b2652-479">なし</span><span class="sxs-lookup"><span data-stu-id="b2652-479">No</span></span></td>
<td>
<ol>
<li><span data-ttu-id="b2652-480">ピッキング作業開始時に、倉庫管理 モバイルアプリの<strong>ロケーションの上書き</strong>メニュー項目を選択します。</span><span class="sxs-lookup"><span data-stu-id="b2652-480">Select the <strong>Override location</strong> menu item on the Warehouse Management mobile app when you start picking work.</span></span></li>
<li><span data-ttu-id="b2652-481">ロケーションを手動で入力します。</span><span class="sxs-lookup"><span data-stu-id="b2652-481">Manually enter a location.</span></span></li>
</ol>
</td>
<td><span data-ttu-id="b2652-482"><strong>ロケーションの上書き</strong>アクションは実行できません。</span><span class="sxs-lookup"><span data-stu-id="b2652-482">The <strong>Override location</strong> action isn't possible.</span></span> <span data-ttu-id="b2652-483">失敗すると、エラーがスローされます。</span><span class="sxs-lookup"><span data-stu-id="b2652-483">It fails, and an error is thrown.</span></span></td>
<td><span data-ttu-id="b2652-484">適用できません</span><span class="sxs-lookup"><span data-stu-id="b2652-484">Not applicable</span></span></td>
</tr>
</tbody>
</table>

#### <a name="full-button--split-a-work-line-because-of-overflow-on-the-user-location"></a><span data-ttu-id="b2652-485">フル ボタン - ユーザーのロケーションでオーバーフローしたために作業ラインを分割します</span><span class="sxs-lookup"><span data-stu-id="b2652-485">Full button – Split a work line because of overflow on the user location</span></span>

<table>
<thead>
<tr>
<th><span data-ttu-id="b2652-486">キー設定パラメーター</span><span class="sxs-lookup"><span data-stu-id="b2652-486">Key setup parameter</span></span></th>
<th><span data-ttu-id="b2652-487">バッチ数量が利用可能</span><span class="sxs-lookup"><span data-stu-id="b2652-487">Batch quantity is available</span></span></th>
<th><span data-ttu-id="b2652-488">主要なユーザーの手順</span><span class="sxs-lookup"><span data-stu-id="b2652-488">Key user steps</span></span></th>
<th><span data-ttu-id="b2652-489">倉庫作業</span><span class="sxs-lookup"><span data-stu-id="b2652-489">Warehouse work</span></span></th>
<th><span data-ttu-id="b2652-490">注文が確定したバッチ引当</span><span class="sxs-lookup"><span data-stu-id="b2652-490">Order-committed batch reservation</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="b2652-491">モバイル デバイスのメニュー項目で<strong>作業の分割を許可</strong>オプションが有効になっています。</span><span class="sxs-lookup"><span data-stu-id="b2652-491">The <strong>Allow splitting of work</strong> option is enabled on the mobile device menu item.</span></span></td>
<td><span data-ttu-id="b2652-492">適用できません</span><span class="sxs-lookup"><span data-stu-id="b2652-492">Not applicable</span></span></td>
<td>
<ol>
<li><span data-ttu-id="b2652-493">ピッキング作業プロセス時に、倉庫管理モバイル アプリのメニュー項目に<strong>フル</strong>を選択します。</span><span class="sxs-lookup"><span data-stu-id="b2652-493">Select the <strong>Full</strong> menu item on the Warehouse Management mobile app when you process picking work.</span></span></li>
<li><span data-ttu-id="b2652-494"><strong>ピッキング数量</strong>フィールドに、必要なピッキングの一部の数量を入力して、全能力を示します。</span><span class="sxs-lookup"><span data-stu-id="b2652-494">In the <strong>Pick Qty</strong> field, enter a partial quantity of the required pick to indicate the full capacity.</span></span></li>
</ol>
</td>
<td>
<ul>
<li><span data-ttu-id="b2652-495">現在の作業では、数量はピッキングが必要な残余数量に更新されます。</span><span class="sxs-lookup"><span data-stu-id="b2652-495">On the current work, the quantity is updated to the remaining quantity that must be picked.</span></span></li>
<li><span data-ttu-id="b2652-496">選択した数量の新しい作業が作成され、決済されます。</span><span class="sxs-lookup"><span data-stu-id="b2652-496">New work for the picked quantity is created and closed.</span></span></li>
</ul></td>
<td><span data-ttu-id="b2652-497">適用できません</span><span class="sxs-lookup"><span data-stu-id="b2652-497">Not applicable</span></span></td>
</tr>
</tbody>
</table>

#### <a name="reduce-the-picked-quantity-of-completed-work-from-a-load"></a><span data-ttu-id="b2652-498">完了した作業のピッキング済数量をする (積荷から)</span><span class="sxs-lookup"><span data-stu-id="b2652-498">Reduce the picked quantity of completed work (from a load)</span></span>

<table>
<thead>
<tr>
<th><span data-ttu-id="b2652-499">キー設定パラメーター</span><span class="sxs-lookup"><span data-stu-id="b2652-499">Key setup parameter</span></span></th>
<th><span data-ttu-id="b2652-500">バッチ数量が利用可能</span><span class="sxs-lookup"><span data-stu-id="b2652-500">Batch quantity is available</span></span></th>
<th><span data-ttu-id="b2652-501">主要なユーザーの手順</span><span class="sxs-lookup"><span data-stu-id="b2652-501">Key user steps</span></span></th>
<th><span data-ttu-id="b2652-502">倉庫作業</span><span class="sxs-lookup"><span data-stu-id="b2652-502">Warehouse work</span></span></th>
<th><span data-ttu-id="b2652-503">注文が確定したバッチ引当</span><span class="sxs-lookup"><span data-stu-id="b2652-503">Order-committed batch reservation</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td rowspan='2'><span data-ttu-id="b2652-504">適用できません</span><span class="sxs-lookup"><span data-stu-id="b2652-504">Not applicable</span></span></td>
<td><span data-ttu-id="b2652-505">はい</span><span class="sxs-lookup"><span data-stu-id="b2652-505">Yes</span></span></td>
<td>
<ol>
<li><span data-ttu-id="b2652-506">積荷明細行から<strong>ピッキング済数量の削減</strong>ページを開きます。</span><span class="sxs-lookup"><span data-stu-id="b2652-506">Open the <strong>Reduce picked quantity</strong> page from the load line.</span></span></li>
<li><span data-ttu-id="b2652-507">ピッキングを解除する全数量を入力します。</span><span class="sxs-lookup"><span data-stu-id="b2652-507">Enter the full quantity to unpick.</span></span></li>
<li><span data-ttu-id="b2652-508">「移動先」のロケーション / ライセンス プレートを選択します。</span><span class="sxs-lookup"><span data-stu-id="b2652-508">Select a "move to" location/license plate.</span></span></li>
</ol>
</td>
<td>
<ul> 
<li><span data-ttu-id="b2652-509">積荷明細行に関連付けられている作業はキャンセルされます。</span><span class="sxs-lookup"><span data-stu-id="b2652-509">Work that is associated with the load line is canceled.</span></span></li>
<li><span data-ttu-id="b2652-510">在庫移動の新しい作業が作成され、決済されます。</span><span class="sxs-lookup"><span data-stu-id="b2652-510">New work for the inventory movement is created and closed.</span></span></li>
</ul>
</td>
<td><span data-ttu-id="b2652-511">この数量は、同じバッチに対して再引当されます。</span><span class="sxs-lookup"><span data-stu-id="b2652-511">The quantity is re-reserved for the same batch.</span></span> <span data-ttu-id="b2652-512">システムは、数量が使用可能なロケーションとライセンス プレート (ロケーションがライセンス プレートで制御されている場合) をランダムに割り当てます。</span><span class="sxs-lookup"><span data-stu-id="b2652-512">The system randomly assigns a location and license plate (if the location is license plate–controlled) where the quantity is available.</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="b2652-513">いいえ</span><span class="sxs-lookup"><span data-stu-id="b2652-513">No</span></span></td>
<td><span data-ttu-id="b2652-514">前の行を参照してください。</span><span class="sxs-lookup"><span data-stu-id="b2652-514">See the previous row.</span></span></td>
<td><span data-ttu-id="b2652-515">前の行を参照してください。</span><span class="sxs-lookup"><span data-stu-id="b2652-515">See the previous row.</span></span></td>
<td><span data-ttu-id="b2652-516">数量は、ピッキング中に入力された同じバッチ、および同じロケーション、およびライセンス プレート (ロケーションがライセンス プレートで制御されている場合) に対して再引当されます。</span><span class="sxs-lookup"><span data-stu-id="b2652-516">The quantity is re-reserved for the same batch, and for the same location and license plate (if the location is license plate–controlled) that were entered during unpicking.</span></span></td>
</tr>
</tbody>
</table>

#### <a name="move-an-item-within-a-warehouse"></a><span data-ttu-id="b2652-517">倉庫内の品目を移動する</span><span class="sxs-lookup"><span data-stu-id="b2652-517">Move an item within a warehouse</span></span>

> [!NOTE]
> <span data-ttu-id="b2652-518">この倉庫アクションは、**作業作成プロセス** タイプの移動にのみ適用され、テンプレートによる移動には適用されません。</span><span class="sxs-lookup"><span data-stu-id="b2652-518">This warehouse action is applicable only to movement of the **Work creation process** type, not to movement by template.</span></span>

<table>
<thead>
<tr>
<th><span data-ttu-id="b2652-519">キー設定パラメーター</span><span class="sxs-lookup"><span data-stu-id="b2652-519">Key setup parameter</span></span></th>
<th><span data-ttu-id="b2652-520">バッチ数量が利用可能</span><span class="sxs-lookup"><span data-stu-id="b2652-520">Batch quantity is available</span></span></th>
<th><span data-ttu-id="b2652-521">主要なユーザーの手順</span><span class="sxs-lookup"><span data-stu-id="b2652-521">Key user steps</span></span></th>
<th><span data-ttu-id="b2652-522">倉庫作業</span><span class="sxs-lookup"><span data-stu-id="b2652-522">Warehouse work</span></span></th>
<th><span data-ttu-id="b2652-523">注文が確定したバッチ引当</span><span class="sxs-lookup"><span data-stu-id="b2652-523">Order-committed batch reservation</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td rowspan='2'><span data-ttu-id="b2652-524">作業者で、<strong>作業が関連付けられている在庫の移動を許可</strong>オプションが有効になっています。</span><span class="sxs-lookup"><span data-stu-id="b2652-524">The <strong>Allow movement of inventory with associated work</strong> option is enabled on the worker.</span></span></td>
<td><span data-ttu-id="b2652-525">あり</span><span class="sxs-lookup"><span data-stu-id="b2652-525">Yes</span></span></td>
<td>
<ol>
<li><span data-ttu-id="b2652-526">倉庫管理モバイル アプリで移動処理を開始する。</span><span class="sxs-lookup"><span data-stu-id="b2652-526">Start a movement on the Warehouse Management mobile app.</span></span></li>
<li><span data-ttu-id="b2652-527">「移動元」および「移動先」のロケーションを入力します。</span><span class="sxs-lookup"><span data-stu-id="b2652-527">Enter "from" and "to" locations.</span></span></li>
</ol></td>
<td>
<ul>
<li><span data-ttu-id="b2652-528">移動によって影響を受けるすべての既存の作業について、ピッキングロケーションが新しい「移動先」のロケーションに更新されます。</span><span class="sxs-lookup"><span data-stu-id="b2652-528">On all existing work that is affected by the move, the pick location is updated to the new "to" location.</span></span></li>
<li><span data-ttu-id="b2652-529">在庫移動の新しい作業が作成され、決済されます。</span><span class="sxs-lookup"><span data-stu-id="b2652-529">New work for the inventory movement is created and closed.</span></span></li>
</ul>
</td>
<td><span data-ttu-id="b2652-530">特定のロケーションからの数量の移動によって影響を受けるすべての既存の引当は、同じバッチに対して再引当されます。</span><span class="sxs-lookup"><span data-stu-id="b2652-530">All existing reservations that are affected by the quantity movement from the given location are re-reserved for the same batch.</span></span> <span data-ttu-id="b2652-531">システムは、数量が使用可能なロケーションとライセンス プレート (ロケーションがライセンス プレートで制御されている場合) をランダムに割り当てます。</span><span class="sxs-lookup"><span data-stu-id="b2652-531">The system randomly assigns a location and license plate (if the location is license plate–controlled) where the quantity is available.</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="b2652-532">いいえ</span><span class="sxs-lookup"><span data-stu-id="b2652-532">No</span></span></td>
<td><span data-ttu-id="b2652-533">前の行を参照してください。</span><span class="sxs-lookup"><span data-stu-id="b2652-533">See the previous row.</span></span></td>
<td><span data-ttu-id="b2652-534">前の行を参照してください。</span><span class="sxs-lookup"><span data-stu-id="b2652-534">See the previous row.</span></span></td>
<td><span data-ttu-id="b2652-535">特定のロケーションからの数量の移動によって影響を受けるすべての既存の引当は、同じバッチ、および新しい「移動先」ロケーションとライセンス プレートに対して再引当されます (ロケーションがライセンス プレートで制御されている場合)。</span><span class="sxs-lookup"><span data-stu-id="b2652-535">All existing reservations that are affected by the quantity movement from the given location are re-reserved for the same batch, and for the new "to" location and license plate (if the location is license plate–controlled).</span></span></td>
</tr>
</tbody>
</table>

#### <a name="reverse-the-picked-quantity-of-completed-work-from-a-load-or-a-wave"></a><span data-ttu-id="b2652-536">完了した作業のピッキング済数量を取り消す (積荷もしくはウェーブから)</span><span class="sxs-lookup"><span data-stu-id="b2652-536">Reverse the picked quantity of completed work (from a load or a wave)</span></span>

<table>
<thead>
<tr>
<th><span data-ttu-id="b2652-537">キー設定パラメーター</span><span class="sxs-lookup"><span data-stu-id="b2652-537">Key setup parameter</span></span></th>
<th><span data-ttu-id="b2652-538">バッチ数量が利用可能</span><span class="sxs-lookup"><span data-stu-id="b2652-538">Batch quantity is available</span></span></th>
<th><span data-ttu-id="b2652-539">主要なユーザーの手順</span><span class="sxs-lookup"><span data-stu-id="b2652-539">Key user steps</span></span></th>
<th><span data-ttu-id="b2652-540">倉庫作業</span><span class="sxs-lookup"><span data-stu-id="b2652-540">Warehouse work</span></span></th>
<th><span data-ttu-id="b2652-541">注文が確定したバッチ引当</span><span class="sxs-lookup"><span data-stu-id="b2652-541">Order-committed batch reservation</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td rowspan='6'><span data-ttu-id="b2652-542">適用できません</span><span class="sxs-lookup"><span data-stu-id="b2652-542">Not applicable</span></span></td>
<td><span data-ttu-id="b2652-543">はい</span><span class="sxs-lookup"><span data-stu-id="b2652-543">Yes</span></span></td>
<td>
<ol>
<li><span data-ttu-id="b2652-544"><strong>作業を取消</strong>ページを開きます。</span><span class="sxs-lookup"><span data-stu-id="b2652-544">Open the <strong>Reverse work</strong> page.</span></span></li>
<li><span data-ttu-id="b2652-545">要求ページで、<strong>品目を現在のロケーションに配置したままにする</strong>オプションを選択します。</span><span class="sxs-lookup"><span data-stu-id="b2652-545">On the request page, select the <strong>Leave items at current location</strong> option.</span></span></li>
</ol>
</td>
<td><span data-ttu-id="b2652-546">積荷に関連付けられているすべての作業はキャンセルされます。</span><span class="sxs-lookup"><span data-stu-id="b2652-546">All work that is associated with the load is canceled.</span></span></td>
<td><span data-ttu-id="b2652-547">この数量は、同じバッチに対して再引当されます。</span><span class="sxs-lookup"><span data-stu-id="b2652-547">The quantity is re-reserved for the same batch.</span></span> <span data-ttu-id="b2652-548">システムは、数量が使用可能なロケーションとライセンス プレート (ロケーションがライセンス プレートで制御されている場合) をランダムに割り当てます。</span><span class="sxs-lookup"><span data-stu-id="b2652-548">The system randomly assigns a location and license plate (if the location is license plate–controlled) where the quantity is available.</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="b2652-549">いいえ</span><span class="sxs-lookup"><span data-stu-id="b2652-549">No</span></span></td>
<td><span data-ttu-id="b2652-550">前の行を参照してください。</span><span class="sxs-lookup"><span data-stu-id="b2652-550">See the previous row.</span></span></td>
<td><span data-ttu-id="b2652-551">前の行を参照してください。</span><span class="sxs-lookup"><span data-stu-id="b2652-551">See the previous row.</span></span></td>
<td><span data-ttu-id="b2652-552">数量は、同じバッチ、および取消時に数量が残されたロケーションとライセンス プレートに対して再引当されます。</span><span class="sxs-lookup"><span data-stu-id="b2652-552">The quantity is re-reserved for the same batch, and for the location and license plate where the quantity was left upon reversal.</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="b2652-553">はい</span><span class="sxs-lookup"><span data-stu-id="b2652-553">Yes</span></span></td>
<td>
<ol>
<li><span data-ttu-id="b2652-554"><strong>作業を取消</strong>ページを開きます。</span><span class="sxs-lookup"><span data-stu-id="b2652-554">Open the <strong>Reverse work</strong> page.</span></span></li>
<li><span data-ttu-id="b2652-555">要求ページで、<strong>品目をこのロケーションに割り当てる</strong>オプションを選択します。</span><span class="sxs-lookup"><span data-stu-id="b2652-555">On the request page, select the <strong>Assign items to this location</strong> option.</span></span></li>
</ol>
</td>
<td>
<ul>
<li><span data-ttu-id="b2652-556">現在の作業はキャンセルされました。</span><span class="sxs-lookup"><span data-stu-id="b2652-556">The current work is canceled.</span></span></li>
<li><span data-ttu-id="b2652-557">在庫移動の新しい作業が作成され、決済されます。</span><span class="sxs-lookup"><span data-stu-id="b2652-557">New work for the inventory movement is created and closed.</span></span></li>
</ul>
</td>
<td><span data-ttu-id="b2652-558">この数量は、同じバッチに対して再引当されます。</span><span class="sxs-lookup"><span data-stu-id="b2652-558">The quantity is re-reserved for the same batch.</span></span> <span data-ttu-id="b2652-559">システムは、数量が使用可能なロケーションとライセンス プレート (ロケーションがライセンス プレートで制御されている場合) をランダムに割り当てます。</span><span class="sxs-lookup"><span data-stu-id="b2652-559">The system randomly assigns a location and license plate (if the location is license plate–controlled) where the quantity is available.</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="b2652-560">いいえ</span><span class="sxs-lookup"><span data-stu-id="b2652-560">No</span></span></td>
<td><span data-ttu-id="b2652-561">前の行を参照してください。</span><span class="sxs-lookup"><span data-stu-id="b2652-561">See the previous row.</span></span></td>
<td><span data-ttu-id="b2652-562">前の行を参照してください。</span><span class="sxs-lookup"><span data-stu-id="b2652-562">See the previous row.</span></span></td>
<td><span data-ttu-id="b2652-563">数量は、同じバッチ、および取消時に数量が割り当てられたロケーションとライセンス プレートに対して再引当されます。</span><span class="sxs-lookup"><span data-stu-id="b2652-563">The quantity is re-reserved for the same batch, and for the location and license plate that the quantity was assigned to upon reversal.</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="b2652-564">はい/いいえ</span><span class="sxs-lookup"><span data-stu-id="b2652-564">Yes/No</span></span></td>
<td>
<ol>
<li><span data-ttu-id="b2652-565"><strong>作業を取消</strong>ページを開きます。</span><span class="sxs-lookup"><span data-stu-id="b2652-565">Open the <strong>Reverse work</strong> page.</span></span></li>
<li><span data-ttu-id="b2652-566">要求ページで、<strong>品目をこのロケーションに移動する</strong>オプションを選択します。</span><span class="sxs-lookup"><span data-stu-id="b2652-566">On the request page, select the <strong>Move items to this location</strong> option.</span></span></li>
</ol>
</td>
<td><span data-ttu-id="b2652-567">取消はサポートされていません。</span><span class="sxs-lookup"><span data-stu-id="b2652-567">Reversal isn't supported.</span></span></td>
<td><span data-ttu-id="b2652-568">適用できません</span><span class="sxs-lookup"><span data-stu-id="b2652-568">Not applicable</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="b2652-569">はい/いいえ</span><span class="sxs-lookup"><span data-stu-id="b2652-569">Yes/No</span></span></td>
<td>
<ol>
<li><span data-ttu-id="b2652-570"><strong>作業を取消</strong>ページを開きます。</span><span class="sxs-lookup"><span data-stu-id="b2652-570">Open the <strong>Reverse work</strong> page.</span></span></li>
<li><span data-ttu-id="b2652-571">要求ページで、<strong>ロケーションの指示に基づいて品目を移動する</strong>オプションを選択します。</span><span class="sxs-lookup"><span data-stu-id="b2652-571">On the request page, select the <strong>Move items based on location directives</strong> option.</span></span></li>
</ol>
</td>
<td><span data-ttu-id="b2652-572">取消はサポートされていません。</span><span class="sxs-lookup"><span data-stu-id="b2652-572">Reversal isn't supported.</span></span> </td>
<td><span data-ttu-id="b2652-573">適用できません</span><span class="sxs-lookup"><span data-stu-id="b2652-573">Not applicable</span></span></td>
</tr>
</tbody>
</table>

#### <a name="short-pick-a-quantity--register-the-quantity-as-physically-not-found-at-the-locationlicense-plate-while-you-perform-picking-work"></a><span data-ttu-id="b2652-574">数量の選択 - ピッキング作業の実行中に、ロケーション / ライセンス プレートでは見つからない数量を登録する</span><span class="sxs-lookup"><span data-stu-id="b2652-574">Short-pick a quantity – Register the quantity as physically not found at the location/license plate while you perform picking work</span></span>

<table>
<thead>
<tr>
<th><span data-ttu-id="b2652-575">キー設定パラメーター</span><span class="sxs-lookup"><span data-stu-id="b2652-575">Key setup parameter</span></span></th>
<th><span data-ttu-id="b2652-576">バッチ数量が利用可能</span><span class="sxs-lookup"><span data-stu-id="b2652-576">Batch quantity is available</span></span></th>
<th><span data-ttu-id="b2652-577">主要なユーザーの手順</span><span class="sxs-lookup"><span data-stu-id="b2652-577">Key user steps</span></span></th>
<th><span data-ttu-id="b2652-578">倉庫作業</span><span class="sxs-lookup"><span data-stu-id="b2652-578">Warehouse work</span></span></th>
<th><span data-ttu-id="b2652-579">注文が確定したバッチ引当</span><span class="sxs-lookup"><span data-stu-id="b2652-579">Order-committed batch reservation</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td rowspan='2'><span data-ttu-id="b2652-580"><strong>品目再配賦</strong> = <strong>なし</strong>、<strong>在庫の調整</strong> = <strong>はい</strong>、および<strong>引当の削除</strong> = <strong>いいえ</strong>で、<strong>ショートピック</strong> タイプの作業例外が設定されています。</span><span class="sxs-lookup"><span data-stu-id="b2652-580">A work exception of the <strong>Short pick</strong> type is set up, where <strong>Item reallocation</strong> = <strong>None</strong>, <strong>Adjust inventory</strong> = <strong>Yes</strong>, and <strong>Remove reservations</strong> = <strong>No</strong>.</span></span></td>
<td><span data-ttu-id="b2652-581">あり</span><span class="sxs-lookup"><span data-stu-id="b2652-581">Yes</span></span></td>
<td>
<ol>
<li><span data-ttu-id="b2652-582">ピッキング作業のプロセス時に、倉庫管理モバイル アプリのメニュー項目に<strong>ショートピック</strong>を選択します。</span><span class="sxs-lookup"><span data-stu-id="b2652-582">Select the <strong>Shortpick</strong> menu item on the Warehouse Management mobile app when you run picking work.</span></span></li>
<li><span data-ttu-id="b2652-583"><strong>ピック数量</strong>フィールドに <strong>0</strong> (ゼロ) と入力します。</span><span class="sxs-lookup"><span data-stu-id="b2652-583">In the <strong>Pick Quantity</strong> field, enter <strong>0</strong> (zero).</span></span></li>
<li><span data-ttu-id="b2652-584"><strong>理由</strong>フィールドに、<strong>非再配賦</strong>と入力します。</span><span class="sxs-lookup"><span data-stu-id="b2652-584">In the <strong>Reason</strong> field, enter <strong>No reallocation</strong>.</span></span></li>
</ol>
</td>
<td>
<ul>
<li><span data-ttu-id="b2652-585">現在の作業は終了済で、ピッキング済数量は 0 (ゼロ) です。</span><span class="sxs-lookup"><span data-stu-id="b2652-585">The current work is closed, and the picked quantity is 0 (zero).</span></span></li>
<li><span data-ttu-id="b2652-586"><strong>棚卸</strong>タイプの在庫トランザクションおよび<strong>売却</strong>出庫タイプの在庫トランザクションが作成され、調整を表します。</span><span class="sxs-lookup"><span data-stu-id="b2652-586">An inventory transaction of the <strong>Counting</strong> type and the <strong>Sold</strong> issue type is created to represent the adjustment.</span></span></li>
</ul>
</td>
<td><span data-ttu-id="b2652-587">この数量は、同じバッチに対して再引当されます。</span><span class="sxs-lookup"><span data-stu-id="b2652-587">The quantity is re-reserved for the same batch.</span></span> <span data-ttu-id="b2652-588">システムは、数量が使用可能なロケーションとライセンス プレート (ロケーションがライセンス プレートで制御されている場合) をランダムに割り当てます。</span><span class="sxs-lookup"><span data-stu-id="b2652-588">The system randomly assigns a location and license plate (if the location is license plate–controlled) where the quantity is available.</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="b2652-589">いいえ</span><span class="sxs-lookup"><span data-stu-id="b2652-589">No</span></span></td>
<td><span data-ttu-id="b2652-590">前の行を参照してください。</span><span class="sxs-lookup"><span data-stu-id="b2652-590">See the previous row.</span></span></td>
<td>
<ul>
<li><span data-ttu-id="b2652-591">ショートピッキング アクションの実行に失敗し、エラーがスローされます。</span><span class="sxs-lookup"><span data-stu-id="b2652-591">The short-picking action fails, and an error is thrown.</span></span></li>
<li><span data-ttu-id="b2652-592">現在の作業は開いたままになります。</span><span class="sxs-lookup"><span data-stu-id="b2652-592">The current work remains open.</span></span></li>
</ul>
</td>
<td><span data-ttu-id="b2652-593">適用できません</span><span class="sxs-lookup"><span data-stu-id="b2652-593">Not applicable</span></span></td>
</tr>
<tr>
<td rowspan='2'><span data-ttu-id="b2652-594"><strong>品目再配賦</strong> = <strong>なし</strong>、<strong>在庫の調整</strong> = <strong>はい</strong>、および<strong>引当の削除</strong> = <strong>はい</strong>で、<strong>ショートピック</strong> タイプの作業例外が設定されています。</span><span class="sxs-lookup"><span data-stu-id="b2652-594">A work exception of the <strong>Short pick</strong> type is set up, where <strong>Item reallocation</strong> = <strong>None</strong>, <strong>Adjust inventory</strong> = <strong>Yes</strong>, and <strong>Remove reservations</strong> = <strong>Yes</strong>.</span></span></td>
<td><span data-ttu-id="b2652-595">あり</span><span class="sxs-lookup"><span data-stu-id="b2652-595">Yes</span></span></td>
<td>
<ol>
<li><span data-ttu-id="b2652-596">ピッキング作業のプロセス時に、倉庫管理モバイル アプリのメニュー項目に<strong>ショートピック</strong>を選択します。</span><span class="sxs-lookup"><span data-stu-id="b2652-596">Select the <strong>Shortpick</strong> menu item on the Warehouse Management mobile app when you run picking work.</span></span></li>
<li><span data-ttu-id="b2652-597"><strong>ピック数量</strong>フィールドに <strong>0</strong> (ゼロ) と入力します。</span><span class="sxs-lookup"><span data-stu-id="b2652-597">In the <strong>Pick Quantity</strong> field, enter <strong>0</strong> (zero).</span></span></li>
<li><span data-ttu-id="b2652-598"><strong>理由</strong>フィールドに、<strong>非再配賦</strong>と入力します。</span><span class="sxs-lookup"><span data-stu-id="b2652-598">In the <strong>Reason</strong> field, enter <strong>No reallocation</strong>.</span></span></li>
</ol>
</td>
<td>
<ul>
<li><span data-ttu-id="b2652-599">現在の作業は終了済で、ピッキング済数量は 0 (ゼロ) です。</span><span class="sxs-lookup"><span data-stu-id="b2652-599">The current work is closed, and the picked quantity is 0 (zero).</span></span></li>
<li><span data-ttu-id="b2652-600"><strong>棚卸</strong>タイプの在庫トランザクションおよび<strong>売却</strong>出庫タイプの在庫トランザクションが作成され、調整を表します。</span><span class="sxs-lookup"><span data-stu-id="b2652-600">An inventory transaction of the <strong>Counting</strong> type and the <strong>Sold</strong> issue type is created to represent the adjustment.</span></span></li>
</ul>
</td>
<td><span data-ttu-id="b2652-601">簡単なピッキングロケーションからの数量の調整によって影響を受けるすべての既存の引当は、同じバッチに対して再引当されます。</span><span class="sxs-lookup"><span data-stu-id="b2652-601">All existing reservations that are affected by the quantity adjustment in the short-picked location are re-reserved for the same batch.</span></span> <span data-ttu-id="b2652-602">システムは、数量が使用可能なロケーションとライセンス プレート (ロケーションがライセンス プレートで制御されている場合) をランダムに割り当てます。</span><span class="sxs-lookup"><span data-stu-id="b2652-602">The system randomly assigns a location and license plate (if the location is license plate–controlled) where the quantity is available.</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="b2652-603">いいえ</span><span class="sxs-lookup"><span data-stu-id="b2652-603">No</span></span></td>
<td><span data-ttu-id="b2652-604">前の行を参照してください。</span><span class="sxs-lookup"><span data-stu-id="b2652-604">See the previous row.</span></span></td>
<td><span data-ttu-id="b2652-605">前の行を参照してください。</span><span class="sxs-lookup"><span data-stu-id="b2652-605">See the previous row.</span></span></td>
<td><span data-ttu-id="b2652-606">簡単なピッキングロケーションからの数量の調整によって影響を受けるすべての既存の引当は、削除されました。</span><span class="sxs-lookup"><span data-stu-id="b2652-606">All existing reservations that are affected by the quantity adjustment in the short-picked location are removed.</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="b2652-607"><strong>品目再配賦</strong> = <strong>手動</strong>、<strong>在庫の調整</strong> = <strong>はい</strong>、および<strong>引当の削除</strong> = <strong>いいえ / はい</strong>で、<strong>ショートピック</strong> タイプの作業例外が設定されています。</span><span class="sxs-lookup"><span data-stu-id="b2652-607">A work exception of the <strong>Short pick</strong> type is set up, where <strong>Item reallocation</strong> = <strong>Manual</strong>, <strong>Adjust inventory</strong> = <strong>Yes</strong>, and <strong>Remove reservations</strong> = <strong>No/Yes</strong>.</span></span> <span data-ttu-id="b2652-608">さらに、作業者で<strong>手動による再配置を許可</strong>オプションが有効になります。</span><span class="sxs-lookup"><span data-stu-id="b2652-608">Additionally, the <strong>Allow manual item reallocation</strong> option is enabled on the worker.</span></span></td>
<td><span data-ttu-id="b2652-609">あり</span><span class="sxs-lookup"><span data-stu-id="b2652-609">Yes</span></span></td>
<td>
<ol>
<li><span data-ttu-id="b2652-610">ピッキング作業のプロセス時に、倉庫管理モバイル アプリのメニュー項目に<strong>ショートピック</strong>を選択します。</span><span class="sxs-lookup"><span data-stu-id="b2652-610">Select the <strong>Shortpick</strong> menu item on the Warehouse Management mobile app when you run picking work.</span></span></li>
<li><span data-ttu-id="b2652-611"><strong>ショートピック数量</strong>フィールドに <strong>0</strong> (ゼロ) と入力します。</span><span class="sxs-lookup"><span data-stu-id="b2652-611">In the <strong>Shortpick Quantity</strong> field, enter <strong>0</strong> (zero).</span></span></li>
<li><span data-ttu-id="b2652-612"><strong>理由</strong>フィールドで、<strong>手動での再配分を使用したショートピッキング</strong>を選択します。</span><span class="sxs-lookup"><span data-stu-id="b2652-612">In the <strong>Reason</strong> field, select <strong>Short Picking with manual reallocation</strong>.</span></span></li>
<li><span data-ttu-id="b2652-613">一覧からロケーション / ライセンス プレートを選択します。</span><span class="sxs-lookup"><span data-stu-id="b2652-613">Select the location/license plate in the list.</span></span></li>
</ol>
</td>
<td>
<ul>
<li><span data-ttu-id="b2652-614">現在の作業では、次のアクションが発生します。</span><span class="sxs-lookup"><span data-stu-id="b2652-614">On the current work, the following actions occur:</span></span>
<ul>
<li><span data-ttu-id="b2652-615">ピッキング行は終了済で、ピッキング済数量は 0 (ゼロ) です。</span><span class="sxs-lookup"><span data-stu-id="b2652-615">The pick line is closed, and the picked quantity is 0 (zero).</span></span></li>
<li><span data-ttu-id="b2652-616">プット明細行はキャンセルされました。</span><span class="sxs-lookup"><span data-stu-id="b2652-616">The put line is canceled.</span></span></li>
<li><span data-ttu-id="b2652-617">新しいピック行が作成されました。</span><span class="sxs-lookup"><span data-stu-id="b2652-617">A new pick line is created.</span></span> <span data-ttu-id="b2652-618">ユーザーによって選択されたロケーション / ライセンス プレートを使用します。</span><span class="sxs-lookup"><span data-stu-id="b2652-618">It uses the location/license plate that the user selected.</span></span></li>
<li><span data-ttu-id="b2652-619">新しいプット明細行が作成されました。</span><span class="sxs-lookup"><span data-stu-id="b2652-619">A new put line is created.</span></span></li>
</ul>
</li>
<li><span data-ttu-id="b2652-620"><strong>棚卸</strong>タイプの在庫トランザクションおよび<strong>売却</strong>出庫タイプの在庫トランザクションが作成され、調整を表します。</span><span class="sxs-lookup"><span data-stu-id="b2652-620">An inventory transaction of the <strong>Counting</strong> type and the <strong>Sold</strong> issue type is created to represent the adjustment.</span></span></li>
</ul>
</td>
<td><span data-ttu-id="b2652-621">適用できません</span><span class="sxs-lookup"><span data-stu-id="b2652-621">Not applicable</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="b2652-622"><strong>品目再配賦</strong> = <strong>手動</strong>、<strong>在庫の調整</strong> = <strong>はい</strong>、および<strong>引当の削除</strong> = <strong>いいえ</strong>で、<strong>ショートピック</strong> タイプの作業例外が設定されています。</span><span class="sxs-lookup"><span data-stu-id="b2652-622">A work exception of the <strong>Short pick</strong> type is set up, where <strong>Item reallocation</strong> = <strong>Manual</strong>, <strong>Adjust inventory</strong> = <strong>Yes</strong>, and <strong>Remove reservations</strong> = <strong>No</strong>.</span></span> <span data-ttu-id="b2652-623">さらに、作業者で<strong>手動による再配置を許可</strong>オプションが有効になります。</span><span class="sxs-lookup"><span data-stu-id="b2652-623">Additionally, the <strong>Allow manual item reallocation</strong> option is enabled on the worker.</span></span></td>
<td><span data-ttu-id="b2652-624">なし</span><span class="sxs-lookup"><span data-stu-id="b2652-624">No</span></span></td>
<td>
<ol>
<li><span data-ttu-id="b2652-625">ピッキング作業のプロセス時に、倉庫管理モバイル アプリのメニュー項目に<strong>ショートピック</strong>を選択します。</span><span class="sxs-lookup"><span data-stu-id="b2652-625">Select the <strong>Shortpick</strong> menu item on the Warehouse Management mobile app when you run picking work.</span></span></li>
<li><span data-ttu-id="b2652-626"><strong>ショートピック数量</strong>フィールドに <strong>0</strong> (ゼロ) と入力します。</span><span class="sxs-lookup"><span data-stu-id="b2652-626">In the <strong>Shortpick Quantity</strong> field, enter <strong>0</strong> (zero).</span></span></li>
<li><span data-ttu-id="b2652-627"><strong>理由</strong>フィールドで、<strong>手動での再配分を使用したショートピッキング</strong>を選択します。</span><span class="sxs-lookup"><span data-stu-id="b2652-627">In the <strong>Reason</strong> field, select <strong>Short Picking with manual reallocation</strong>.</span></span></li>
</ol>
</td>
<td><span data-ttu-id="b2652-628">ショートピッキング アクションの実行に失敗し、エラーがスローされます。</span><span class="sxs-lookup"><span data-stu-id="b2652-628">The short-picking action fails, and an error is thrown.</span></span></td>
<td><span data-ttu-id="b2652-629">適用できません</span><span class="sxs-lookup"><span data-stu-id="b2652-629">Not applicable</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="b2652-630"><strong>品目再配賦</strong> = <strong>手動</strong>、<strong>在庫の調整</strong> = <strong>はい</strong>、および<strong>引当の削除</strong> = <strong>はい</strong>で、<strong>ショートピック</strong> タイプの作業例外が設定されています。</span><span class="sxs-lookup"><span data-stu-id="b2652-630">A work exception of the <strong>Short pick</strong> type is set up, where <strong>Item reallocation</strong> = <strong>Manual</strong>, <strong>Adjust inventory</strong> = <strong>Yes</strong>, and <strong>Remove reservations</strong> = <strong>Yes</strong>.</span></span> <span data-ttu-id="b2652-631">さらに、作業者で<strong>手動による再配置を許可</strong>オプションが有効になります。</span><span class="sxs-lookup"><span data-stu-id="b2652-631">Additionally, the <strong>Allow manual item reallocation</strong> option is enabled on the worker.</span></span></td>
<td><span data-ttu-id="b2652-632">なし</span><span class="sxs-lookup"><span data-stu-id="b2652-632">No</span></span></td>
<td>
<ol>
<li><span data-ttu-id="b2652-633">ピッキング作業のプロセス時に、倉庫管理モバイル アプリのメニュー項目に<strong>ショートピック</strong>を選択します。</span><span class="sxs-lookup"><span data-stu-id="b2652-633">Select the <strong>Shortpick</strong> menu item on the Warehouse Management mobile app when you run picking work.</span></span></li>
<li><span data-ttu-id="b2652-634"><strong>ショートピック数量</strong>フィールドに <strong>0</strong> (ゼロ) と入力します。</span><span class="sxs-lookup"><span data-stu-id="b2652-634">In the <strong>Shortpick Quantity</strong> field, enter <strong>0</strong> (zero).</span></span></li>
<li><span data-ttu-id="b2652-635"><strong>理由</strong>フィールドで、<strong>手動での再配分を使用したショートピッキング</strong>を選択します。</span><span class="sxs-lookup"><span data-stu-id="b2652-635">In the <strong>Reason</strong> field, select <strong>Short Picking with manual reallocation</strong>.</span></span></li>
<li><span data-ttu-id="b2652-636">一覧からロケーション / ライセンス プレートを選択します。</span><span class="sxs-lookup"><span data-stu-id="b2652-636">Select the location/license plate in the list.</span></span></li>
</ol>
</td>
<td>
<ul>
<li><span data-ttu-id="b2652-637">現在の作業では、次のアクションが発生します。</span><span class="sxs-lookup"><span data-stu-id="b2652-637">On the current work, the following actions occur:</span></span>
<ul>
<li><span data-ttu-id="b2652-638">ピッキング行は終了済で、ピッキング済数量は 0 (ゼロ) です。</span><span class="sxs-lookup"><span data-stu-id="b2652-638">The pick line is closed, and the picked quantity is 0 (zero).</span></span></li>
<li><span data-ttu-id="b2652-639">プット明細行はキャンセルされました。</span><span class="sxs-lookup"><span data-stu-id="b2652-639">The put line is canceled.</span></span></li>
</ul>
</li>
<li><span data-ttu-id="b2652-640"><strong>棚卸</strong>タイプの在庫トランザクションおよび<strong>売却</strong>出庫タイプの在庫トランザクションが作成され、調整を表します。</span><span class="sxs-lookup"><span data-stu-id="b2652-640">An inventory transaction of the <strong>Counting</strong> type and the <strong>Sold</strong> issue type is created to represent the adjustment.</span></span></li>
</ul>
</td>
<td><span data-ttu-id="b2652-641">簡単なピッキング ロケーション / ライセンス プレートからの数量の調整によって影響を受けるすべての既存の引当は、削除されました。</span><span class="sxs-lookup"><span data-stu-id="b2652-641">All existing reservations that are affected by the quantity adjustment in the short-picked location/license plate are removed.</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="b2652-642"><strong>品目再配賦</strong> = <strong>自動</strong>、<strong>在庫の調整</strong> = <strong>はい / いいえ</strong>、および<strong>引当の削除</strong> = <strong>はい / いいえ</strong>で、<strong>ショートピック</strong> タイプの作業例外が設定されています。</span><span class="sxs-lookup"><span data-stu-id="b2652-642">A work exception of the <strong>Short pick</strong> type is set up, where <strong>Item reallocation</strong> = <strong>Automatic</strong>, <strong>Adjust inventory</strong> = <strong>Yes/No</strong>, and <strong>Remove reservations</strong> = <strong>Yes/No</strong>.</span></span></td>
<td><span data-ttu-id="b2652-643">適用できません</span><span class="sxs-lookup"><span data-stu-id="b2652-643">Not applicable</span></span></td>
<td>
<ol>
<li><span data-ttu-id="b2652-644">ピッキング作業のプロセス時に、倉庫管理モバイル アプリのメニュー項目に<strong>ショートピック</strong>を選択します。</span><span class="sxs-lookup"><span data-stu-id="b2652-644">Select the <strong>Shortpick</strong> menu item on the Warehouse Management mobile app when you run picking work.</span></span></li>
<li><span data-ttu-id="b2652-645"><strong>ショートピック数量</strong>フィールドに <strong>0</strong> (ゼロ) と入力します。</span><span class="sxs-lookup"><span data-stu-id="b2652-645">In the <strong>Shortpick Quantity</strong> field, enter <strong>0</strong> (zero).</span></span></li>
<li><span data-ttu-id="b2652-646"><strong>理由</strong>フィールドで、<strong>自動での再配分を使用したショートピッキング</strong>を選択します。</span><span class="sxs-lookup"><span data-stu-id="b2652-646">In the <strong>Reason</strong> field, select <strong>Short Picking with automatic reallocation</strong>.</span></span></li>
</ol>
</td>
<td><span data-ttu-id="b2652-647">自動再割り当てを含むショートピッキングはサポートされていません。</span><span class="sxs-lookup"><span data-stu-id="b2652-647">Short-picking that involves automatic reallocation isn't supported.</span></span></td>
<td><span data-ttu-id="b2652-648">自動再割り当てを含むショートピッキングはサポートされていません。</span><span class="sxs-lookup"><span data-stu-id="b2652-648">Short-picking that involves automatic reallocation isn't supported.</span></span></td>
</tr>
</tbody>
</table>

#### <a name="change-the-inventory-status"></a><span data-ttu-id="b2652-649">在庫状態の変更</span><span class="sxs-lookup"><span data-stu-id="b2652-649">Change the inventory status</span></span>

> [!NOTE]
> <span data-ttu-id="b2652-650">この倉庫アクションは複数のエントリ ポイントから実行できます。</span><span class="sxs-lookup"><span data-stu-id="b2652-650">This warehouse action can be performed from multiple entry points.</span></span> <span data-ttu-id="b2652-651">ここに表示されている例では、**ロケーションごとの手持在庫** ページで **在庫状態の変更** アクションを使用しています。</span><span class="sxs-lookup"><span data-stu-id="b2652-651">The example that is shown here uses **Inventory status change** action on the **On-hand by location** page.</span></span>

<table>
<thead>
<tr>
<th><span data-ttu-id="b2652-652">キー設定パラメーター</span><span class="sxs-lookup"><span data-stu-id="b2652-652">Key setup parameter</span></span></th>
<th><span data-ttu-id="b2652-653">バッチ数量が利用可能</span><span class="sxs-lookup"><span data-stu-id="b2652-653">Batch quantity is available</span></span></th>
<th><span data-ttu-id="b2652-654">主要なユーザーの手順</span><span class="sxs-lookup"><span data-stu-id="b2652-654">Key user steps</span></span></th>
<th><span data-ttu-id="b2652-655">倉庫作業</span><span class="sxs-lookup"><span data-stu-id="b2652-655">Warehouse work</span></span></th>
<th><span data-ttu-id="b2652-656">注文が確定したバッチ引当</span><span class="sxs-lookup"><span data-stu-id="b2652-656">Order-committed batch reservation</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td rowspan='2'><span data-ttu-id="b2652-657"><strong>倉庫</strong>タブの<strong>倉庫</strong>レコードで、<strong>引当とマーキングの削除</strong>フィールドが<strong>引当</strong>または<strong>マーキングと引当</strong>に設定されます。</span><span class="sxs-lookup"><span data-stu-id="b2652-657">On the <strong>Warehouse</strong> tab, in the <strong>Warehouse</strong> record, the <strong>Remove reservations and markings</strong> field is set to <strong>Reservations</strong> or <strong>Markings and reservations</strong>.</span></span></td>
<td><span data-ttu-id="b2652-658">はい</span><span class="sxs-lookup"><span data-stu-id="b2652-658">Yes</span></span></td>
<td>
<ol>
<li><span data-ttu-id="b2652-659">特定のロケーションを選択します。</span><span class="sxs-lookup"><span data-stu-id="b2652-659">Select a specific location.</span></span></li>
<li><span data-ttu-id="b2652-660">特定の品目、ロケーション、およびライセンス プレートがある明細行を選択します (ロケーションがライセンス プレートにより制御されている場合)。</span><span class="sxs-lookup"><span data-stu-id="b2652-660">Select a line that has a specific item, location, and license plate (if the location is license plate–controlled).</span></span></li>
<li><span data-ttu-id="b2652-661"><strong>在庫状態の変更</strong>を選択します。</span><span class="sxs-lookup"><span data-stu-id="b2652-661">Select <strong>Inventory status change</strong>.</span></span></li>
<li><span data-ttu-id="b2652-662"><strong>在庫状態</strong>フィールドを<strong>ブロック</strong>に設定します。</span><span class="sxs-lookup"><span data-stu-id="b2652-662">Set the <strong>Inventory status</strong> field to <strong>Blocking</strong>.</span></span></li>
</ol>
</td>
<td><span data-ttu-id="b2652-663">作業用に引き当てられている数量に対して、在庫状態の変更は許可されていません。</span><span class="sxs-lookup"><span data-stu-id="b2652-663">Inventory status changes aren't allowed for quantities that are reserved for work.</span></span></td>
<td>
<ul>
<li><span data-ttu-id="b2652-664">この数量は、同じバッチに対して再引当されます。</span><span class="sxs-lookup"><span data-stu-id="b2652-664">The quantity is re-reserved for the same batch.</span></span> <span data-ttu-id="b2652-665">システムは、数量が使用可能なロケーションとライセンス プレート (ロケーションがライセンス プレートで制御されている場合) をランダムに割り当てます。</span><span class="sxs-lookup"><span data-stu-id="b2652-665">The system randomly assigns a location and license plate (if the location is license plate–controlled) where the quantity is available.</span></span></li>
<li><span data-ttu-id="b2652-666"><strong>在庫状態の変更</strong>タイプの 2 つの在庫トランザクションを作成して、在庫状態分析コードの変更を表します。</span><span class="sxs-lookup"><span data-stu-id="b2652-666">Two inventory transactions of the <strong>Inventory status change</strong> type are created to represent the change in the inventory status dimension.</span></span></li>
<li><span data-ttu-id="b2652-667">ブロックされた数量の引き当てを表すために、<strong>在庫ブロック</strong>タイプおよび<strong>引当済現物</strong>払出タイプの在庫トランザクションが作成されます。</span><span class="sxs-lookup"><span data-stu-id="b2652-667">An inventory transaction of the <strong>Inventory blocking</strong> type and the <strong>Reserved physical</strong> issue type is created to represent the reservation of the blocked quantity.</span></span></li>
</ul>
</td>
</tr>
<tr>
<td><span data-ttu-id="b2652-668">いいえ</span><span class="sxs-lookup"><span data-stu-id="b2652-668">No</span></span></td>
<td><span data-ttu-id="b2652-669">前の行を参照してください。</span><span class="sxs-lookup"><span data-stu-id="b2652-669">See the previous row.</span></span></td>
<td><span data-ttu-id="b2652-670">作業用に引き当てられている数量に対して、在庫状態の変更は許可されていません。</span><span class="sxs-lookup"><span data-stu-id="b2652-670">Inventory status changes aren't allowed for quantities that are reserved for work.</span></span></td>
<td>
<ul>
<li><span data-ttu-id="b2652-671">引当が削除されます。</span><span class="sxs-lookup"><span data-stu-id="b2652-671">The reservation is removed.</span></span></li>
<li><span data-ttu-id="b2652-672"><strong>在庫状態の変更</strong>タイプの 2 つの在庫トランザクションを作成して、在庫状態分析コードの変更を表します。</span><span class="sxs-lookup"><span data-stu-id="b2652-672">Two inventory transactions of the <strong>Inventory status change</strong> type are created to represent the change in the inventory status dimension.</span></span></li>
<li><span data-ttu-id="b2652-673">ブロックされた数量の引き当てを表すために、<strong>在庫ブロック</strong>タイプおよび<strong>引当済現物</strong>払出タイプの在庫トランザクションが作成されます。</span><span class="sxs-lookup"><span data-stu-id="b2652-673">An inventory transaction of the <strong>Inventory blocking</strong> type and the <strong>Reserved physical</strong> issue type is created to represent the reservation of the blocked quantity.</span></span></li>
</ul>
</td>
</tr>
<tr>
<td rowspan='2'><span data-ttu-id="b2652-674"><strong>倉庫</strong>タブの<strong>倉庫</strong>レコードで、<strong>引当とマーキングの削除</strong>フィールドが<strong>なし</strong>に設定されます。</span><span class="sxs-lookup"><span data-stu-id="b2652-674">On the <strong>Warehouse</strong> tab, in the <strong>Warehouse</strong> record, the <strong>Remove reservations and markings</strong> field is set to <strong>None</strong>.</span></span></td>
<td><span data-ttu-id="b2652-675">はい</span><span class="sxs-lookup"><span data-stu-id="b2652-675">Yes</span></span></td>
<td>
<ol>
<li><span data-ttu-id="b2652-676">特定のロケーションを選択します。</span><span class="sxs-lookup"><span data-stu-id="b2652-676">Select a specific location.</span></span></li>
<li><span data-ttu-id="b2652-677">特定の品目、ロケーション、およびライセンス プレートがある明細行を選択します (ロケーションがライセンス プレートにより制御されている場合)。</span><span class="sxs-lookup"><span data-stu-id="b2652-677">Select a line that has a specific item, location, and license plate (if the location is license plate–controlled).</span></span></li>
<li><span data-ttu-id="b2652-678"><strong>在庫状態の変更</strong>を選択します。</span><span class="sxs-lookup"><span data-stu-id="b2652-678">Select <strong>Inventory status change</strong>.</span></span></li>
<li><span data-ttu-id="b2652-679"><strong>在庫状態</strong>フィールドを<strong>ブロック</strong>に設定します。</span><span class="sxs-lookup"><span data-stu-id="b2652-679">Set the <strong>Inventory status</strong> field to <strong>Blocking</strong>.</span></span></li>
</ol>
</td>
<td><span data-ttu-id="b2652-680">作業用に引き当てられている数量に対して、在庫状態の変更は許可されていません。</span><span class="sxs-lookup"><span data-stu-id="b2652-680">Inventory status changes aren't allowed for quantities that are reserved for work.</span></span></td>
<td><span data-ttu-id="b2652-681">この数量は、同じバッチに対して再引当されます。</span><span class="sxs-lookup"><span data-stu-id="b2652-681">The quantity is re-reserved for the same batch.</span></span> <span data-ttu-id="b2652-682">システムは、数量が使用可能なロケーションとライセンス プレート (ロケーションがライセンス プレートで制御されている場合) をランダムに割り当てます。</span><span class="sxs-lookup"><span data-stu-id="b2652-682">The system randomly assigns a location and license plate (if the location is license plate–controlled) where the quantity is available.</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="b2652-683">いいえ</span><span class="sxs-lookup"><span data-stu-id="b2652-683">No</span></span></td>
<td><span data-ttu-id="b2652-684">前の行を参照してください。</span><span class="sxs-lookup"><span data-stu-id="b2652-684">See the previous row.</span></span></td>
<td><span data-ttu-id="b2652-685">作業用に引き当てられている数量に対して、在庫状態の変更は許可されていません。</span><span class="sxs-lookup"><span data-stu-id="b2652-685">Inventory status changes aren't allowed for quantities that are reserved for work.</span></span></td>
<td><span data-ttu-id="b2652-686">在庫状態の変更は許可されません。</span><span class="sxs-lookup"><span data-stu-id="b2652-686">Inventory status changes aren't allowed.</span></span></td>
</tr>
</tbody>
</table>

## <a name="limitations"></a><span data-ttu-id="b2652-687">制限</span><span class="sxs-lookup"><span data-stu-id="b2652-687">Limitations</span></span>

- <span data-ttu-id="b2652-688">変動倉庫のレベルの分析コード引当機能では、次の機能はサポートされません。</span><span class="sxs-lookup"><span data-stu-id="b2652-688">The flexible warehouse-level dimension reservation functionality doesn't support the following features:</span></span>

    - <span data-ttu-id="b2652-689">CW 管理</span><span class="sxs-lookup"><span data-stu-id="b2652-689">Catch weight management</span></span>
    - <span data-ttu-id="b2652-690">現物マイナス在庫</span><span class="sxs-lookup"><span data-stu-id="b2652-690">Physical negative inventory</span></span>
    - <span data-ttu-id="b2652-691">注文供給に対する引当</span><span class="sxs-lookup"><span data-stu-id="b2652-691">Reservation against ordered supply</span></span>
    - <span data-ttu-id="b2652-692">移動オーダーおよび原材料のピッキング</span><span class="sxs-lookup"><span data-stu-id="b2652-692">Transfer orders and raw material picking</span></span>

- <span data-ttu-id="b2652-693">ディレクティブ単位での梱包のためのコンテナー連結ルールには、制限があります。</span><span class="sxs-lookup"><span data-stu-id="b2652-693">The container consolidation rule for packing by directive unit has limitations.</span></span> <span data-ttu-id="b2652-694">注文が確定された引当では、**ディレクティブ単位別の梱包** フィールドが有効になっているコンテナー構築テンプレートを使用しないことをお勧めします。</span><span class="sxs-lookup"><span data-stu-id="b2652-694">For order-committed reservations, we recommend that you not use container build templates where the **Pack by directive unit** field is enabled.</span></span> <span data-ttu-id="b2652-695">現在の設計では、倉庫作業の作成時にロケーションの指示は使用されません。</span><span class="sxs-lookup"><span data-stu-id="b2652-695">In the current design, location directives aren't used when warehouse work is created.</span></span> <span data-ttu-id="b2652-696">したがって、コンテナー詰めのウェーブ ステップ中には、単位順序グループ (在庫単位) の最小単位のみが適用されます。</span><span class="sxs-lookup"><span data-stu-id="b2652-696">Therefore, only the lowest unit in the unit sequence group (the inventory unit) is applied during the containerization wave step.</span></span>

## <a name="see-also"></a><span data-ttu-id="b2652-697">参照</span><span class="sxs-lookup"><span data-stu-id="b2652-697">See also</span></span>

- [<span data-ttu-id="b2652-698">倉庫管理のバッチ番号</span><span class="sxs-lookup"><span data-stu-id="b2652-698">Batch numbers in Warehouse management</span></span>](https://docs.microsoft.com/dynamicsax-2012/appuser-itpro/batch-numbers-in-warehouse-management)
- [<span data-ttu-id="b2652-699">販売注文に対する同じバッチの引当</span><span class="sxs-lookup"><span data-stu-id="b2652-699">Reserve the same batch for a sales order</span></span>](../sales-marketing/reserve-same-batch-sales-order.md)
- [<span data-ttu-id="b2652-700">モバイル デバイスで最も古いバッチをピッキング</span><span class="sxs-lookup"><span data-stu-id="b2652-700">Pick oldest batch on a mobile device</span></span>](pick-oldest-batch.md)
- [<span data-ttu-id="b2652-701">バッチおよびライセンス プレートの確認</span><span class="sxs-lookup"><span data-stu-id="b2652-701">Batch and license plate confirmation</span></span>](batch-and-license-plate-confirmation.md)
- [<span data-ttu-id="b2652-702">倉庫管理での引当のトラブルシューティング</span><span class="sxs-lookup"><span data-stu-id="b2652-702">Troubleshoot reservations in warehouse management</span></span>](troubleshoot-warehouse-reservations.md)


[!INCLUDE[footer-include](../../includes/footer-banner.md)]
