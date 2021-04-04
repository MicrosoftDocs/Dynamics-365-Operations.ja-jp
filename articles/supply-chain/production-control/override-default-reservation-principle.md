---
title: 生産材料の既定の予約原則の上書き
description: このトピックでは、生産部品表 (BOM) またはバッチ オーダー フォーミュラの一部である各品目に対して、異なる予約原則を自動的に適用できるよう、各品目モデル グループに対して既定の予約原則を設定する方法について説明します。
author: johanhoffmann
manager: tfehr
ms.date: 12/10/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: InventModelGroup
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: johanho
ms.search.validFrom: 2020-12-10
ms.dyn365.ops.version: 10.0.17
ms.openlocfilehash: 2391ec11bd497c69ddb19e29533f5441d7374877
ms.sourcegitcommit: 2b4809e60974e72df9476ffd62706b1bfc8da4a7
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 03/04/2021
ms.locfileid: "5501105"
---
# <a name="override-the-default-reservation-principle-for-materials-in-production"></a><span data-ttu-id="89548-103">生産材料の既定の予約原則の上書き</span><span class="sxs-lookup"><span data-stu-id="89548-103">Override the default reservation principle for materials in production</span></span>

[!include [banner](../includes/banner.md)]
[!include [preview banner](../includes/preview-banner.md)]

<span data-ttu-id="89548-104">*既定の生産予約の上書き* 機能を使用すると、各品目モデル グループに対して既定の予約原則を設定できます。</span><span class="sxs-lookup"><span data-stu-id="89548-104">The *Override default production reservation* feature lets you set a default reservation principle for each item model group.</span></span> <span data-ttu-id="89548-105">したがって、生産部品表 (BOM) またはバッチ オーダー フォーミュラの一部である各品目に対して、異なる予約原則を自動的に適用できます。</span><span class="sxs-lookup"><span data-stu-id="89548-105">Therefore, different reservation principles can automatically be applied for each item that is part of a production bill of materials (BOM) or batch order formula.</span></span> <span data-ttu-id="89548-106">各品目モデル グループが、注文に対して設定されている既定の予約原則を上書きするかどうか、および、代わりに使用する必要がある予約原則 (*手動*、*見積*、*スケジューリング*、*リリース*、または *開始*) を選択できます。</span><span class="sxs-lookup"><span data-stu-id="89548-106">You can select whether each item model group should override the default reservation principle that is set for an order, and what reservation principle should be used instead (*manual*, *estimation*, *scheduling*, *release*, or *start*).</span></span>

<span data-ttu-id="89548-107">新しい製造オーダーまたはバッチ オーダーを作成するときに、その注文とそのすべての BOM 明細行またはフォーミュラ明細行に適用する必要がある予約原則を選択するように求めるメッセージが表示されます。</span><span class="sxs-lookup"><span data-stu-id="89548-107">When you create a new production order or batch order, you're prompted to select the reservation principle that should be applied to that order and all its BOM lines or formula lines.</span></span> <span data-ttu-id="89548-108">*既定の生産予約の上書き* 機能を使用する場合は 、BOM明細行またはフォーミュラ明細行の一部またはすべてが、その予約原則を上書きし、代わりに関連する品目モデル グループに対して設定されている予約原則を使用できます。</span><span class="sxs-lookup"><span data-stu-id="89548-108">When the *Override default production reservation* feature is used, some or all of the BOM or formula lines can override that reservation principle and instead use the reservation principle that is set for the relevant item model group.</span></span>

<span data-ttu-id="89548-109">たとえば、それらの製品に対して作成される原材料または材料がピック作業を必要とする場合、BOM かフォーミュラ明細行の物理的な予約が必要になります。これは、倉庫作業の生成には物理的な予約が前提条件となります。</span><span class="sxs-lookup"><span data-stu-id="89548-109">For example, if you have raw materials or ingredients that require pick work, BOM or formula lines that are created for those products require a physical reservation, because physical reservation is a prerequisite for the generation of warehouse work.</span></span> <span data-ttu-id="89548-110">通常、予約を自動的に行う場合は、*見積*、*スケジューリング*、*リリース*、または *開始* のいずれかの予約原則を選択します。</span><span class="sxs-lookup"><span data-stu-id="89548-110">Typically, if you want the reservation to occur automatically, you select one of the following reservation principles: *estimation*, *scheduling*, *release*, or *start*.</span></span> <span data-ttu-id="89548-111">一方、ピック作業を必要としない材料または材料がある場合は、場所から直接消費されるのが一般的です。*手動* 予約原則は、物理的な引当を行わないか、ピック作業を生成しません。</span><span class="sxs-lookup"><span data-stu-id="89548-111">On the other hand, if you have materials or ingredients that don't require pick work, because they are consumed directly from a location, you typically select the *manual* reservation principle, which doesn't make any physical reservations or generate any pick work.</span></span>

## <a name="turn-on-the-feature"></a><span data-ttu-id="89548-112">機能をオンにする</span><span class="sxs-lookup"><span data-stu-id="89548-112">Turn on the feature</span></span>

<span data-ttu-id="89548-113">この機能を使用するには、システム上で有効化する必要があります。</span><span class="sxs-lookup"><span data-stu-id="89548-113">Before you can use the feature, it must be turned on in your system.</span></span> <span data-ttu-id="89548-114">管理者は、[機能管理](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) 設定を使用して、機能の状態を確認し、有効にすることができます。</span><span class="sxs-lookup"><span data-stu-id="89548-114">Admins can use the [feature management](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) settings to check the status of the feature and turn it on.</span></span> <span data-ttu-id="89548-115">**機能管理** ワークスペースで、この機能は次のようにリストされています。</span><span class="sxs-lookup"><span data-stu-id="89548-115">In the **Feature management** workspace, the feature is listed in the following way:</span></span>

- <span data-ttu-id="89548-116">**モジュール:** *生産制御*</span><span class="sxs-lookup"><span data-stu-id="89548-116">**Module:** *Production control*</span></span>
- <span data-ttu-id="89548-117">**機能名:** *(プレビュー) 規定の生産計画の上書き*</span><span class="sxs-lookup"><span data-stu-id="89548-117">**Feature name:** *(Preview) Override default production reservation*</span></span>

## <a name="assign-a-production-reservation-policy-to-an-item-model-group"></a><span data-ttu-id="89548-118">品目モデル グループへの生産予約ポリシーの割り当て</span><span class="sxs-lookup"><span data-stu-id="89548-118">Assign a production reservation policy to an item model group</span></span>

1. <span data-ttu-id="89548-119">**原価管理 \> 在庫会計ポリシー設定 \> 品目モデル グループ** に移動します。</span><span class="sxs-lookup"><span data-stu-id="89548-119">Go to **Cost management \> Inventory accounting policies setup \> Item model groups**.</span></span>
1. <span data-ttu-id="89548-120">品目モデル グループを作成または選択します。</span><span class="sxs-lookup"><span data-stu-id="89548-120">Create or select an item model group.</span></span>
1. <span data-ttu-id="89548-121">**在庫ポリシー** クイックタブで、**品目生産の予約の上書き** チェック ボックスをオンにします。</span><span class="sxs-lookup"><span data-stu-id="89548-121">On the **Inventory policies** FastTab, select the **Override item production reservation** check box.</span></span>
1. <span data-ttu-id="89548-122">**予約** フィールドで、選択したモデル グループに属する品目の予約原則を選択します。</span><span class="sxs-lookup"><span data-stu-id="89548-122">In the **Reservation** field, select the reservation principle for items that belong to the selected model group.</span></span> <span data-ttu-id="89548-123">(これらの品目には、BOM 明細行またはフォーミュラ明細行上の品目が含まれます。)</span><span class="sxs-lookup"><span data-stu-id="89548-123">(Those items include items that are on a BOM or formula line.)</span></span>

    - <span data-ttu-id="89548-124">**手動** - モデル グループの品目は、生産に対して物理的に予約されません。</span><span class="sxs-lookup"><span data-stu-id="89548-124">**Manual** – Items in the model group won't automatically be physically reserved for production.</span></span> <span data-ttu-id="89548-125">ただし、これらの引当は必要に応じて手動で行うことができます。</span><span class="sxs-lookup"><span data-stu-id="89548-125">However, they can still be manually reserved as required.</span></span>
    - <span data-ttu-id="89548-126">**見積** -  製造オーダーの見積時に、モデル グループの品目が物理的に予約されます。</span><span class="sxs-lookup"><span data-stu-id="89548-126">**Estimation** – Items in the model group will be physically reserved during estimation of the production order.</span></span>
    - <span data-ttu-id="89548-127">**スケジュール** -  製造オーダーのスケジュール時に、モデル グループの品目が物理的に予約されます。</span><span class="sxs-lookup"><span data-stu-id="89548-127">**Scheduling** – Items in the model group will be physically reserved during scheduling of the production order.</span></span>
    - <span data-ttu-id="89548-128">**リリース** -  製造オーダーのリリース時に、モデル グループの品目が物理的に予約されます。</span><span class="sxs-lookup"><span data-stu-id="89548-128">**Release** – Items in the model group will be physically reserved when the production order is released.</span></span>
    - <span data-ttu-id="89548-129">**開始** -  製造オーダーの開始時に、モデル グループの品目が物理的に予約されます。</span><span class="sxs-lookup"><span data-stu-id="89548-129">**Start** – Items in the model group will be physically reserved at the start of the production order.</span></span>

## <a name="example-using-reservation-principles-in-a-bulkpack-scenario"></a><span data-ttu-id="89548-130">例: バルク/梱包のシナリオでの予約原則の使用</span><span class="sxs-lookup"><span data-stu-id="89548-130">Example: Using reservation principles in a bulk/pack scenario</span></span>

<span data-ttu-id="89548-131">バルク潤滑剤は、1,000リットルのミキサーで生産されます。</span><span class="sxs-lookup"><span data-stu-id="89548-131">A bulk lubricant material is produced in a 1,000-liter mixer.</span></span> <span data-ttu-id="89548-132">バルク材料の準備が整った後、さまざまなサイズのびんが満たされた複数の充填操作によって取り出されます。</span><span class="sxs-lookup"><span data-stu-id="89548-132">After the bulk material is ready, it's pumped out to several filling stations, where bottles of different sizes are filled.</span></span> <span data-ttu-id="89548-133">満たされた後、びんはボックスに梱包されます。</span><span class="sxs-lookup"><span data-stu-id="89548-133">After filling is completed, the bottles are packed into boxes.</span></span> <span data-ttu-id="89548-134">これらのボックスは、パレットに梱包されます。</span><span class="sxs-lookup"><span data-stu-id="89548-134">Those boxes are then packed onto pallets.</span></span>

<span data-ttu-id="89548-135">このシナリオでは、1,000 リットルのバルク材料を作成するバッチ オーダーが作成されます。</span><span class="sxs-lookup"><span data-stu-id="89548-135">In this scenario, a batch order to make 1,000 liters of bulk material is created.</span></span> <span data-ttu-id="89548-136">(この注文はバルク オーダーです。) このバッチ オーダーが完了すると、そのバッチ オーダーが入力された場所に完了済と報告されます。</span><span class="sxs-lookup"><span data-stu-id="89548-136">(This order is the bulk order.) When this batch order is completed, it's reported as finished to the material input location of the filling stations.</span></span> <span data-ttu-id="89548-137">その後、各びんのサイズを満たして梱包するバッチ オーダーが作成されます。</span><span class="sxs-lookup"><span data-stu-id="89548-137">A batch order to fill and pack each bottle size is then created.</span></span> <span data-ttu-id="89548-138">(これらのオーダーは梱包オーダーです。) 梱包オーダーには、バルク材料、空のびん、ラベル、他の梱包材から構成されるフォーミュラがあります。</span><span class="sxs-lookup"><span data-stu-id="89548-138">(These orders are the pack orders.) The pack orders have a formula that consists of the bulk material, an empty bottle, a label, and other packing materials.</span></span> <span data-ttu-id="89548-139">バルク材料は、入れ物の付け物に対して直接移動する機能なので、この材料をピックする倉庫作業は必要ありません。また、バルク材料は入庫場所から直接消費されます。</span><span class="sxs-lookup"><span data-stu-id="89548-139">Because the bulk material flows directly from the mixer tank to the filling stations, no warehouse work is required to pick this ingredient, and the bulk material is consumed directly from the input location.</span></span> <span data-ttu-id="89548-140">したがって、予約原則は *手動* に設定されます。</span><span class="sxs-lookup"><span data-stu-id="89548-140">Therefore, the reservation principle is set to *manual*.</span></span> <span data-ttu-id="89548-141">その他の材料は、ピック作業によって充填用のステーションにステージされます。</span><span class="sxs-lookup"><span data-stu-id="89548-141">The other materials are staged to the filling station by pick work.</span></span> <span data-ttu-id="89548-142">したがって、これらの明細行の予約原則は、たとえば、梱包オーダーがリリースされると自動的に予約が行われるため、*リリース* に設定されます。</span><span class="sxs-lookup"><span data-stu-id="89548-142">Therefore, the reservation principle for these lines is set to *release*, for example, so that the reservation automatically occurs when the pack order is released.</span></span>


[!INCLUDE[footer-include](../../includes/footer-banner.md)]