---
title: 倉庫バッチおよびシリアル予約階層のトラブルシューティング
description: このトピックでは、バッチ分析コードまたはシリアル分析コードを使って作業中に発生する可能性がある問題を修正する方法について説明します。
author: perlynne
ms.date: 3/12/2021
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Application user
ms.reviewer: kamaybac
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: perlynne
ms.search.validFrom: 3/12/2021
ms.openlocfilehash: a1abb6f8657484d43d434076e5ee38d1c63fe2ff
ms.sourcegitcommit: 0e8db169c3f90bd750826af76709ef5d621fd377
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/01/2021
ms.locfileid: "5838181"
---
# <a name="troubleshoot-warehouse-batch-and-serial-reservation-hierarchies"></a><span data-ttu-id="3d90a-103">倉庫バッチおよびシリアル予約階層のトラブルシューティング</span><span class="sxs-lookup"><span data-stu-id="3d90a-103">Troubleshoot warehouse batch and serial reservation hierarchies</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="3d90a-104">このトピックでは、バッチ分析コードまたはシリアル分析コードを使って作業中に発生する可能性がある問題を修正する方法について説明します。</span><span class="sxs-lookup"><span data-stu-id="3d90a-104">This topic describes how to fix common issues that you might encounter while you work with reservation hierarchies that use batch or serial dimensions.</span></span>

<span data-ttu-id="3d90a-105">詳細については、[柔軟な倉庫レベル分析コードの引当ポリシー](flexible-warehouse-level-dimension-reservation.md)を参照してください。</span><span class="sxs-lookup"><span data-stu-id="3d90a-105">For more information, see [Flexible warehouse-level dimension reservation policy](flexible-warehouse-level-dimension-reservation.md).</span></span>

<span data-ttu-id="3d90a-106">品目の予約階層によって、保管場所を需要注文に割り当てるには、保管分析コードの要件が満たされる必要があります。</span><span class="sxs-lookup"><span data-stu-id="3d90a-106">The reservation hierarchy of an item dictates the requirement of storage dimensions that must be fulfilled to assign a location to a demand order.</span></span> <span data-ttu-id="3d90a-107">これらの分析コードは、場所が需要注文に割り当てられた後に割り当て可能な分析コードについて、場所が割り当てられる前に満たす必要があるすべての分析コードと *場所の下の分析コード* にに対して、*場所の上の分析コード* として記述できます。</span><span class="sxs-lookup"><span data-stu-id="3d90a-107">These dimensions can be described as *dimensions above location*, for all the dimensions that must be fulfilled before a location is assigned, and *dimensions below location*, for dimensions that can be allocated after a location has been assigned to the demand order.</span></span> <span data-ttu-id="3d90a-108">これらの予約階層は、*バッチ-上* と *バッチ-下* の予約階層、または *シリアル-上* と *シリアル-下* の予約階層とも呼られています。</span><span class="sxs-lookup"><span data-stu-id="3d90a-108">These reservation hierarchies are also known as *batch-above* and *batch-below* reservation hierarchies, or *serial-above* and *serial-below* reservation hierarchies.</span></span>

<span data-ttu-id="3d90a-109">在庫の割り当ては、在庫場所の上の分析コードにすき間がない場合にのみ正常に割り当てできます。</span><span class="sxs-lookup"><span data-stu-id="3d90a-109">Inventory can be successfully allocated only if there are no gaps in the dimensions above location.</span></span> <span data-ttu-id="3d90a-110">たとえば、*バッチ-上* の予約階層では、**サイト**、**倉庫**、および **バッチ番号** の分析コードが需要注文に対して指定されている必要があります。</span><span class="sxs-lookup"><span data-stu-id="3d90a-110">For example, in a *batch-above* reservation hierarchy, you expect **Site,** **Warehouse,** and **Batch number** dimensions to be specified on the demand order.</span></span> <span data-ttu-id="3d90a-111">これらの分析コードが存在しない場合、配賦プロセスは失敗します。</span><span class="sxs-lookup"><span data-stu-id="3d90a-111">If any of these dimensions are missing, the allocation process will fail.</span></span> <span data-ttu-id="3d90a-112">一方、*下バッチ* または *下シリアル* の予約階層では、バッチ番号またはシリアル番号が需要注文に対して指定される場合がありますが、配賦プロセスでは必要 はありません。</span><span class="sxs-lookup"><span data-stu-id="3d90a-112">By contrast, in a *batch-below* or *serial-below* reservation hierarchy, a batch or serial number might be specified on the demand order, but the allocation process doesn't require it.</span></span>

## <a name="i-receive-the-following-error-message-to-be-assigned-to-wave-load-lines-must-specify-the-dimensions-above-the-location-to-assign-these-dimensions-reserve-and-recreate-the-load-line"></a><span data-ttu-id="3d90a-113">エラー メッセージ "ウェーブに割り当てるには、積荷明細行は、その場所より上の分析コードを指定する必要があります。</span><span class="sxs-lookup"><span data-stu-id="3d90a-113">I receive the following error message: "To be assigned to wave, load lines must specify the dimensions above the location.</span></span> <span data-ttu-id="3d90a-114">これらの分析コードを割り当てるには、積荷明細行を準備して再作成します" が表示されます。</span><span class="sxs-lookup"><span data-stu-id="3d90a-114">To assign these dimensions, reserve and recreate the load line."</span></span>

### <a name="issue-description"></a><span data-ttu-id="3d90a-115">問題の説明</span><span class="sxs-lookup"><span data-stu-id="3d90a-115">Issue description</span></span>

<span data-ttu-id="3d90a-116">*バッチ-上* 予約階層を持つ品目を使用する時、部分数量に対する積荷をリリースしようとする場合、**積荷計画ワークベンチ** ページの **倉庫にリリース** コマンドが機能しません。</span><span class="sxs-lookup"><span data-stu-id="3d90a-116">When you use an item that has a *batch-above* reservation hierarchy, the **Release to warehouse** command on the **Load planning workbench** page doesn't work if you try to release a load for a partial quantity.</span></span> <span data-ttu-id="3d90a-117">このエラー メッセージが表示され、部分数量に対して作業が作成されません。</span><span class="sxs-lookup"><span data-stu-id="3d90a-117">You receive this error message, and no work is created for the partial quantity.</span></span>

<span data-ttu-id="3d90a-118">ただし、*下バッチ* 予約階層を持つ品目を使用する時、部分数量に対する積荷を **計画ワークベンチの積荷** からをリリースできます。</span><span class="sxs-lookup"><span data-stu-id="3d90a-118">However, when you use an item that has a *batch-below* reservation hierarchy, you can release a load for a partial quantity from the **Load planning workbench** page.</span></span>

### <a name="issue-cause"></a><span data-ttu-id="3d90a-119">問題の原因</span><span class="sxs-lookup"><span data-stu-id="3d90a-119">Issue cause</span></span>

<span data-ttu-id="3d90a-120">予約階層で **場所** 分析コードの上に分析コードを配置する場合は、倉庫へのリリース前に指定する必要があります。</span><span class="sxs-lookup"><span data-stu-id="3d90a-120">When a dimension is above the **Location** dimension in the reservation hierarchy, it must be specified before the release to the warehouse.</span></span> <span data-ttu-id="3d90a-121">**場所** の上に 1 つ以上の分析コードが指定されていない場合、部分的な数量をリリースすることはできません。</span><span class="sxs-lookup"><span data-stu-id="3d90a-121">Partial quantities can't be released if one or more dimensions above **Location** aren't specified.</span></span>

## <a name="the-auto-reservation-prompt-for-a-batch-number-is-triggered-even-though-there-is-available-inventory"></a><span data-ttu-id="3d90a-122">利用可能な在庫がある場合でも、バッチ番号の自動引当プロンプトが発生します。</span><span class="sxs-lookup"><span data-stu-id="3d90a-122">The auto-reservation prompt for a batch number is triggered even though there is available inventory.</span></span>

### <a name="issue-description"></a><span data-ttu-id="3d90a-123">問題の説明</span><span class="sxs-lookup"><span data-stu-id="3d90a-123">Issue description</span></span>

<span data-ttu-id="3d90a-124">倉庫プロセスが有効になっていない倉庫で *バッチ-上* の予約階層を持つ品目を使用し、自動予約が有効になっている場合は、ピッキングに使用できるバッチが 1 つだけの場合でも、バッチ番号の自動予約プロンプトが表示されます。</span><span class="sxs-lookup"><span data-stu-id="3d90a-124">When you use an item that has a *batch-above* reservation hierarchy in a warehouse that hasn't enabled warehouse processes, and automatic reservation is enabled, the auto-reservation prompt for a batch number is shown even if only one batch is available for picking.</span></span>

<span data-ttu-id="3d90a-125">ただし、倉庫プロセスが有効になっている倉庫で同じ品目を使用した場合は、その倉庫に対する自動予約プロンプトは表示されません。</span><span class="sxs-lookup"><span data-stu-id="3d90a-125">However, when you use the same item in a warehouse where warehouse processes are enabled, the auto-reservation prompt isn't shown.</span></span>

### <a name="issue-cause"></a><span data-ttu-id="3d90a-126">問題の原因</span><span class="sxs-lookup"><span data-stu-id="3d90a-126">Issue cause</span></span>

<span data-ttu-id="3d90a-127">予約階層が *バッチ-上* または *シリアル-上* と定義されている場合、要求オーダーでは、常に参照される分析コード (**バッチ番号** または **シリアル番号**) を指定する必要があります。</span><span class="sxs-lookup"><span data-stu-id="3d90a-127">If a reservation hierarchy is defined as *batch-above* or *serial-above*, the referenced dimension (**Batch number** or **Serial number**) must always be specified on demand orders.</span></span> <span data-ttu-id="3d90a-128">単一のバッチ番号またはシリアル番号が利用可能な場合、倉庫プロセスで情報を完了できる場合があります。</span><span class="sxs-lookup"><span data-stu-id="3d90a-128">Warehouse processes might be able to complete the information if a single batch or serial number is available.</span></span> <span data-ttu-id="3d90a-129">ただし、倉庫の移動が倉庫プロセスに対して有効になっていないので、ユーザーは常に **場所** よりも上のすべての分析コードを指定する必要があります 。</span><span class="sxs-lookup"><span data-stu-id="3d90a-129">However, because the warehouse isn't enabled for warehouse processes, the user must always specify all the dimensions above **Location**.</span></span>

## <a name="slotting-templates-that-have-the-consider-on-hand-slot-criterion-dont-consider-current-on-hand-inventory-for-batch-enabled-items"></a><span data-ttu-id="3d90a-130">オンハンド を考慮するスロット基準を持つスロット テンプレートでは、バッチ対応品目の現在の在庫は考慮されません。</span><span class="sxs-lookup"><span data-stu-id="3d90a-130">Slotting templates that have the Consider on-hand slot criterion don't consider current on-hand inventory for batch-enabled items.</span></span>

<span data-ttu-id="3d90a-131">詳細については、[倉庫スロッティング](warehouse-slotting.md) を参照してください。</span><span class="sxs-lookup"><span data-stu-id="3d90a-131">For more information, see [Warehouse slotting](warehouse-slotting.md).</span></span>

### <a name="issue-description"></a><span data-ttu-id="3d90a-132">問題の説明</span><span class="sxs-lookup"><span data-stu-id="3d90a-132">Issue description</span></span>

<span data-ttu-id="3d90a-133">*オンハンドで考慮* のスロット基準を持つスロット テンプレートでは、*バッチ-上* 品目の現在のオンハンド在庫は考慮されません。</span><span class="sxs-lookup"><span data-stu-id="3d90a-133">Slotting templates that have the *Consider on-hand* slot criterion don't consider current on-hand inventory for *batch-above* items.</span></span> <span data-ttu-id="3d90a-134">販売注文書でバッチ番号が指定されている場合にのみ考慮されます。</span><span class="sxs-lookup"><span data-stu-id="3d90a-134">They consider it only if the batch number is specified on the sales order line.</span></span>

<span data-ttu-id="3d90a-135">ただし、*バッチ-下* 品目を使用する場合、現在の手持在庫は予定と見なされます。</span><span class="sxs-lookup"><span data-stu-id="3d90a-135">However, when you use *batch-below* items, the current on-hand inventory is considered as expected.</span></span>

### <a name="issue-cause"></a><span data-ttu-id="3d90a-136">問題の原因</span><span class="sxs-lookup"><span data-stu-id="3d90a-136">Issue cause</span></span>

<span data-ttu-id="3d90a-137">スロット テンプレート ヘッダーは、*注文済*、*予約済*、または *リリース済* の需要戦略に対して定義できます。</span><span class="sxs-lookup"><span data-stu-id="3d90a-137">The slotting template header can be defined for the *Ordered,* *Reserved*, or *Released* demand strategy.</span></span> <span data-ttu-id="3d90a-138">*注文済み* の需要戦略では、倉庫プロセスの予約またはリリースに適用される同じ在庫予約階層の要件が適用されます。</span><span class="sxs-lookup"><span data-stu-id="3d90a-138">For the *Ordered* demand strategy, the same reservation hierarchy requirements apply that apply to reservation or release to warehouse processes.</span></span> <span data-ttu-id="3d90a-139">したがって、*バッチ-上* および *シリアル-下* の予約階層を持つ品目については、需要注文 (販売または移動) にバッチ番号またはシリアル番号を指定 する必要があります。</span><span class="sxs-lookup"><span data-stu-id="3d90a-139">Therefore, for items that have *batch-above* and *serial-below* reservation hierarchies, the batch or serial number must be specified on the demand order (sales or transfer).</span></span> <span data-ttu-id="3d90a-140">または、倉庫のスロットへ需要が生成される前に、*予約済* 需要戦略を使用してバッチ番号またはシリアル番号 を選択できます。</span><span class="sxs-lookup"><span data-stu-id="3d90a-140">Alternatively, the *Reserved* demand strategy can be used to select the batch or serial number before the warehouse slotting demand is generated.</span></span>

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
