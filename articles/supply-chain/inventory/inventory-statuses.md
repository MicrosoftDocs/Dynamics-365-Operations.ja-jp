---
title: 在庫状態
description: この記事は、在庫を分類し、追跡する在庫状態を使用する方法について説明します。
author: MarkusFogelberg
manager: tfehr
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: EcoResStorageDimensionGroup, WHSInventStatus, WHSWarehouseStatusChange
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.custom: 21331
ms.assetid: b35f495f-de4f-48a0-9d09-4d06781d7650
ms.search.region: Global
ms.author: mafoge
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: eca9d3e4e15d11d2a9a1b531028de230ffc43913
ms.sourcegitcommit: 597476103bb695e3cbe6d9ffcd7a466400346636
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 11/20/2020
ms.locfileid: "4594605"
---
# <a name="inventory-statuses"></a><span data-ttu-id="a0c19-103">在庫状態</span><span class="sxs-lookup"><span data-stu-id="a0c19-103">Inventory statuses</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="a0c19-104">この記事は、在庫を分類し、追跡する在庫状態を使用する方法について説明します。</span><span class="sxs-lookup"><span data-stu-id="a0c19-104">This article describes how you can use inventory statuses to categorize and keep track of inventory.</span></span>

## <a name="set-up-and-use-inventory-statuses"></a><span data-ttu-id="a0c19-105">在庫状態の設定および使用</span><span class="sxs-lookup"><span data-stu-id="a0c19-105">Set up and use inventory statuses</span></span>

<span data-ttu-id="a0c19-106">在庫を分類するために在庫状態を使用できます。</span><span class="sxs-lookup"><span data-stu-id="a0c19-106">You can use inventory statuses to categorize inventory.</span></span> <span data-ttu-id="a0c19-107">これにより、補充またはプット アウェイ作業などの適切なアクションを開始できます。</span><span class="sxs-lookup"><span data-stu-id="a0c19-107">You can then initiate appropriate actions, such as replenishment or put-away work.</span></span>

<span data-ttu-id="a0c19-108">在庫状態の使用方法の例を次に示します。</span><span class="sxs-lookup"><span data-stu-id="a0c19-108">Here are some examples of ways that you can use inventory statuses:</span></span>

- <span data-ttu-id="a0c19-109">手持在庫、入庫トランザクション、および出荷トランザクションの在庫状態を作成します。</span><span class="sxs-lookup"><span data-stu-id="a0c19-109">Create inventory statuses for on-hand inventory, inbound transactions, and outbound transactions.</span></span>
- <span data-ttu-id="a0c19-110">倉庫トランザクションの既定の在庫状態を指定します。</span><span class="sxs-lookup"><span data-stu-id="a0c19-110">Specify a default inventory status for warehouse transactions.</span></span>
- <span data-ttu-id="a0c19-111">着荷前、着荷時、または品目が棚卸資産移動中にプット アウェイされる場合に品目の棚卸資産の状態を変更します。</span><span class="sxs-lookup"><span data-stu-id="a0c19-111">Change an inventory status for items before arrival, during arrival, or when the items are put away during inventory movement.</span></span>
- <span data-ttu-id="a0c19-112">返品された品目の価格決定およびマスタ プラン中の品目補充の計画のために在庫状態を使用します。</span><span class="sxs-lookup"><span data-stu-id="a0c19-112">Use an inventory status to price items that are returned and to plan item coverage during master planning.</span></span>

<span data-ttu-id="a0c19-113">棚卸資産の状態は保管分析コード グループの分析コードの 1 つです。</span><span class="sxs-lookup"><span data-stu-id="a0c19-113">An inventory status is one of the dimensions in the storage dimension group.</span></span> <span data-ttu-id="a0c19-114">在庫状態が使用できるか使用できないかを分類できます。また、**在庫ブロック** パラメーターを使用して、使用できない在庫状態の品目をブロックできます。</span><span class="sxs-lookup"><span data-stu-id="a0c19-114">Inventory statuses can be categorized as available or unavailable, and you can use the **Inventory blocking** parameter to block items that have an unavailable inventory status.</span></span> <span data-ttu-id="a0c19-115">ブロックされた状態の品目は現物在庫と見なされ、製造オーダー、販売注文、移動オーダー、または出荷トランザクションで使用できません。</span><span class="sxs-lookup"><span data-stu-id="a0c19-115">Items that have a blocked status are considered physical inventory, and they can't be used on a production order, sales order, transfer order, or outbound transaction.</span></span>

<span data-ttu-id="a0c19-116">入荷作業のために使用できるか、使用できないかいずれかの在庫状態の倉庫品目を使用できます。</span><span class="sxs-lookup"><span data-stu-id="a0c19-116">You can use warehouse items that have either available or unavailable inventory statuses for inbound work.</span></span> <span data-ttu-id="a0c19-117">たとえば、*準備完了* という名前の使用可能な状態、*破損* という名前の使用できない状態、*ブロック* という名前のブロックされた状態を作成します。</span><span class="sxs-lookup"><span data-stu-id="a0c19-117">For example, you create an available status that is named *Ready*, an unavailable status that is named *Damaged*, and a blocked status that is named *Blocked*.</span></span> <span data-ttu-id="a0c19-118">入庫品目または返品品目の発注書を作成するときに、品目が破損したり、または壊れていれば、購買注文明細行の *破損* で、これらの品目の在庫状態を変更できます。</span><span class="sxs-lookup"><span data-stu-id="a0c19-118">When you create a purchase order for received or returned items, if any items are damaged or broken, you can change the inventory status of those items to *Damaged* on the purchase order line.</span></span> <span data-ttu-id="a0c19-119">これらの品目を受領したら、状態が自動的に *ブロック* に設定されます。</span><span class="sxs-lookup"><span data-stu-id="a0c19-119">After these items are received, the status is automatically set to *Blocked*.</span></span> <span data-ttu-id="a0c19-120">モバイル デバイスを使用して破損した品目をスキャンすると、Supply Chain Management は、場所ディレクティブおよび作業テンプレートを使用し、これらの品目をプット アウェイするための適切な場所または場所の範囲に関する情報を表示します。</span><span class="sxs-lookup"><span data-stu-id="a0c19-120">If you scan the damaged items by using a mobile device, Supply Chain Management can use location directives and work templates to show information about an appropriate location or range of locations where you can put away those items.</span></span> <span data-ttu-id="a0c19-121">返品品目の場合、**在庫トランザクション** ページで *引当* 払出タイプが作成されます。</span><span class="sxs-lookup"><span data-stu-id="a0c19-121">For returned items, an issue type of *Reservation* is created on the **Inventory transactions** page.</span></span>

<span data-ttu-id="a0c19-122">出荷作業の場合、使用可能な在庫状態の品目を使用します。</span><span class="sxs-lookup"><span data-stu-id="a0c19-122">For outbound work, use items that have an available inventory status.</span></span> <span data-ttu-id="a0c19-123">状態が *破損* の品目で、これらの品目にマスタ プランが実行されている場合、品目は存在しないと見なされ、在庫が自動的に補充されます。</span><span class="sxs-lookup"><span data-stu-id="a0c19-123">If you have items that have a status of *Broken*, and master planning is run on these items, the items are considered missing, and inventory is automatically replenished.</span></span>

<span data-ttu-id="a0c19-124">在庫状態を設定したら、サイト、品目、および倉庫の既定の在庫状態を設定できます。</span><span class="sxs-lookup"><span data-stu-id="a0c19-124">After you set up inventory statuses, you can set the default inventory status for a site, item, and warehouse.</span></span> <span data-ttu-id="a0c19-125">また、販売、移動、発注書の既定のステータスを設定できます。</span><span class="sxs-lookup"><span data-stu-id="a0c19-125">You can also set a default status for sales, transfer, and purchase orders.</span></span> <span data-ttu-id="a0c19-126">販売注文および出荷の移動オーダーの既定のステータスでは、**在庫ブロック** オプションは *はい* に設定できません。</span><span class="sxs-lookup"><span data-stu-id="a0c19-126">The default status for sales orders and outbound transfer order can't have the **Inventory blocking** option set to *Yes*.</span></span> <span data-ttu-id="a0c19-127">サイト、倉庫、品目、発注書、移動オーダー、または販売注文の既定の設定に基づく在庫状態は、モバイル デバイスを使用して、発注書、販売注文、または在庫移動指示明細行で変更できます。</span><span class="sxs-lookup"><span data-stu-id="a0c19-127">The inventory status that is inherited from the default settings on a site, warehouse, item, purchase order, transfer order or sales order can be changed by using the mobile device, or on the purchase order, sales order, or transfer order line.</span></span>

<span data-ttu-id="a0c19-128">利用可能な在庫状態を持つ品目の補充を計画するには、**保管分析コード グループ** ページで、保管分析コードの **分析コード別補充計画** オプションを選択します。</span><span class="sxs-lookup"><span data-stu-id="a0c19-128">To plan coverage for items that have an available inventory status, select the **Coverage plan by dimension** option for a storage dimension on the **Storage dimension groups** page.</span></span> <span data-ttu-id="a0c19-129">**品目の補充** ウィザードを開くと、使用可能な状態の品目が **ステータス** ページに表示されます。</span><span class="sxs-lookup"><span data-stu-id="a0c19-129">When you open the **Item Coverage** wizard, items that have an available status appear on the **Status** page.</span></span> <span data-ttu-id="a0c19-130">これらの品目の補充設定を作成するには、利用可能な棚卸資産の状態の棚卸資産の状態 ID を選択します。</span><span class="sxs-lookup"><span data-stu-id="a0c19-130">To create coverage settings for these items, select the inventory status ID for the available inventory statuses.</span></span> <span data-ttu-id="a0c19-131">補充設定に基づいて、品目要件を計算し、マスタ プラン中に利用できる品目の供給と需要を予測できます。</span><span class="sxs-lookup"><span data-stu-id="a0c19-131">Based on the coverage settings, you can calculate the item requirements and forecast the supply and demand of available items during master planning.</span></span> <span data-ttu-id="a0c19-132">ブロックされた在庫状態の品目補充設定を作成することはできません。</span><span class="sxs-lookup"><span data-stu-id="a0c19-132">You can't create an item coverage setup that has a blocked inventory status.</span></span> <span data-ttu-id="a0c19-133">代わりに、**品目補充** ページを使用して、品目補充パラメータを作成または変更します。</span><span class="sxs-lookup"><span data-stu-id="a0c19-133">Alternatively, use the **Item coverage** page to create or modify the item coverage parameters.</span></span>

## <a name="change-inventory-statuses"></a><span data-ttu-id="a0c19-134">在庫状態の変更</span><span class="sxs-lookup"><span data-stu-id="a0c19-134">Change inventory statuses</span></span>

<span data-ttu-id="a0c19-135">在庫状態を変更するには、**場所別手持在庫** ページか *在庫状態の変更* 定期処理タスクを使用します。</span><span class="sxs-lookup"><span data-stu-id="a0c19-135">You can change inventory statuses either by using the **On-hand by location** page or by using the *Inventory status change* periodic task.</span></span>

- <span data-ttu-id="a0c19-136">*在庫状態変更* の定期処理タスクを使用する場合は、含めるレコードを選択し、希望する間隔でそのタスクをバッチで実行するように設定できます。</span><span class="sxs-lookup"><span data-stu-id="a0c19-136">When using the *Inventory status change* periodic task, you can select which records to include and set the task to run in the batch at the desired interval.</span></span>
- <span data-ttu-id="a0c19-137">在庫状態をアドホック プロセスとして変更するには、**場所別手持在庫** ページに移動して、関連するレコードを選択し、**在庫状態の変更** を選択します。</span><span class="sxs-lookup"><span data-stu-id="a0c19-137">To change inventory status as an ad-hoc process, go to **On-hand by location** page, select the relevant records, and then select the **Inventory status change** button.</span></span>

> [!NOTE]
> <span data-ttu-id="a0c19-138">*追跡分析コードが制御する品目の在庫状態の変更* 機能を使用すると、選択したレコードのみを更新する機能を含めて、追跡分析コードが制御する品目の在庫状態を変更できます。</span><span class="sxs-lookup"><span data-stu-id="a0c19-138">The *Change the inventory status of items controlled by tracking dimensions* feature allows you to change the inventory status of items controlled by tracking dimensions, including the ability to update only selected records.</span></span> <span data-ttu-id="a0c19-139">[機能管理](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) を使用して、必要な機能を有効化します。</span><span class="sxs-lookup"><span data-stu-id="a0c19-139">Use [feature management](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) to enable the feature as needed.</span></span> <span data-ttu-id="a0c19-140">機能を有効にすると、次の操作を実行できるようになります。</span><span class="sxs-lookup"><span data-stu-id="a0c19-140">When the feature is enabled, you'll be able to do the following:</span></span>
>
> - <span data-ttu-id="a0c19-141">**場所別手持在庫** ページで、**分析コードの表示** ボタンを使用して表示されている分析コードに基づいて明細行をグループ化し、選択した明細行の状態を変更することができます。</span><span class="sxs-lookup"><span data-stu-id="a0c19-141">On the **On-hand by location** page, you can group lines based on shown dimensions using the **Display dimensions** button and change the status for the selected lines.</span></span>
> - <span data-ttu-id="a0c19-142">**場所別手持在庫** ページで、複数のレコードを選択してから **在庫状態の変更** ボタンを使用して一度に変更できます。</span><span class="sxs-lookup"><span data-stu-id="a0c19-142">On the **On-hand by location** page, you can select multiple records and then use the **Inventory status change** button to change all of them at once.</span></span>
> - <span data-ttu-id="a0c19-143">**在庫状態の変更** の定期処理タスクでは、追跡分析コードを使用してフィルター処理をすることができます。</span><span class="sxs-lookup"><span data-stu-id="a0c19-143">On the **Inventory status change** periodic task you will be able to filter by tracking dimensions.</span></span>
