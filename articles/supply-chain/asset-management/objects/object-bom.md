---
title: 資産 BOM
description: このトピックでは、資産管理の資産部品表 (BOM) について説明します。
author: josaw1
manager: tfehr
ms.date: 06/26/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: CatProcureCatalogEdit, CatProcureCatalogListPage, EntAssetStandardSparePartsItemGroup, EntAssetObjectBOM
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.custom: 2214
ms.assetid: 2f3e0441-414d-402b-b28b-7ab0d650d658
ms.search.region: Global
ms.author: mkirknel
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: f42646ae865cd530203c997fd10c8ccd59e7fa2b
ms.sourcegitcommit: c986d5234b81d31cc6d054298be6f6ec92c1754c
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 09/25/2020
ms.locfileid: "3890060"
---
# <a name="asset-boms"></a><span data-ttu-id="7b7f2-103">資産 BOM</span><span class="sxs-lookup"><span data-stu-id="7b7f2-103">Asset BOMs</span></span>

[!include [banner](../../includes/banner.md)]

 

<span data-ttu-id="7b7f2-104">このトピックでは、資産管理の資産部品表 (BOM) について説明します。</span><span class="sxs-lookup"><span data-stu-id="7b7f2-104">This topic describes asset bills of materials (BOMs) in Asset Management.</span></span> <span data-ttu-id="7b7f2-105">**資産 BOM** ページは、全有効期間中に使用される資産すべての品目の一覧 (予備部品およびその他の品目) を表示します。</span><span class="sxs-lookup"><span data-stu-id="7b7f2-105">The **Asset BOM** page shows a list of all items (spare parts and other items) that are used on an asset during its whole lifetime.</span></span> <span data-ttu-id="7b7f2-106">新しい資産を作成するときは、設定手順の一部として資産 BOM の設定を考慮する必要があります。</span><span class="sxs-lookup"><span data-stu-id="7b7f2-106">When you create a new asset, you should consider setting up an asset BOM as a part of the setup procedure.</span></span> <span data-ttu-id="7b7f2-107">これにより、作成日から資産の品目履歴を追跡することができます。</span><span class="sxs-lookup"><span data-stu-id="7b7f2-107">In this way, you can track item history for the asset from the creation date.</span></span>

<span data-ttu-id="7b7f2-108">メンテナンス ジョブが完了し、品目消費がワーク オーダーに登録され、資産で使用される予備部品およびその他の品目の消費を追跡できます。</span><span class="sxs-lookup"><span data-stu-id="7b7f2-108">After you've completed a maintenance job, and item consumption has been registered on a work order, you can track consumption of spare parts and other items that are used on the asset.</span></span> <span data-ttu-id="7b7f2-109">この機能により、すべての資産の品目消費レコードを完全に保管できます。</span><span class="sxs-lookup"><span data-stu-id="7b7f2-109">This functionality lets you keep a complete item consumption record for all your assets.</span></span> <span data-ttu-id="7b7f2-110">たとえば、レコードを使用して、特定の予備部品が頻繁に交換されるかどうかを監視、または資産で現在使用されている予備部品やその他の品目を追跡できます。</span><span class="sxs-lookup"><span data-stu-id="7b7f2-110">For example, you can use the record to monitor whether a specific spare part is often replaced, or to keep track of the spare parts or other items that are currently used on an asset.</span></span>

> [!NOTE]
> <span data-ttu-id="7b7f2-111">ワーク オーダーで、品目の消費には、予備部品および潤滑剤、ボルト、ガスケットなどのその他の追加品目の両方を含む場合があります。</span><span class="sxs-lookup"><span data-stu-id="7b7f2-111">On a work order, item consumption might include both spare parts and other, additional items, such as lubricants, bolts, and gaskets.</span></span>

<span data-ttu-id="7b7f2-112">資産 BOM は、資産管理の設定に基づいて自動的に更新できます。</span><span class="sxs-lookup"><span data-stu-id="7b7f2-112">An asset BOM can be automatically updated based on the setup in Asset Management.</span></span> <span data-ttu-id="7b7f2-113">ワーク オーダーのライフサイクル状態が終了または完了したワーク オーダーを処理するために作成された場合、ワーク オーダーのライフサイクル状態の**資産 BOM の更新**オプションが**ワーク オーダーのライフサイクル状態**ページで**はい**に設定されている場合、ワーク オーダーがそのライフサイクル状態に更新されると、ワーク オーダーで使用されるすべての品目が**資産 BOM** ページで自動的に更新されます。</span><span class="sxs-lookup"><span data-stu-id="7b7f2-113">If a work order lifecycle state has been created to handle finished or completed work orders, and if the **Update asset BOM** option for that work order lifecycle state is set to **Yes** on the **Work order lifecycle states** page, all items that are used on the work order will be automatically updated on the **Asset BOM** page when the work order is updated to that lifecycle state.</span></span> 


<span data-ttu-id="7b7f2-114">**資産 BOM** ページに新しい品目明細行を作成し、資産 BOM を手動で更新することもできます。</span><span class="sxs-lookup"><span data-stu-id="7b7f2-114">You can also manually update an asset BOM by creating new item lines on the **Asset BOM** page.</span></span>

<span data-ttu-id="7b7f2-115">**資産 BOM** ページで、品目の消費がワーク オーダーに登録された後、資産の予備部品履歴を追跡できます。</span><span class="sxs-lookup"><span data-stu-id="7b7f2-115">On the **Asset BOM** page, you can track spare parts history for assets after item consumption is registered on a work order.</span></span> <span data-ttu-id="7b7f2-116">この機能を使用するには、**予備部品品目グループ** ページで予備部品の登録に使用する品目グループを選択する必要があります。</span><span class="sxs-lookup"><span data-stu-id="7b7f2-116">To use this functionality, you must select the item groups that should be used for spare parts registration on the **Spare parts item groups** page.</span></span>

<span data-ttu-id="7b7f2-117">資産 BOM 機能を使用するには、まず必要な予備部品品目グループを設定する必要があります。</span><span class="sxs-lookup"><span data-stu-id="7b7f2-117">To use asset BOM functionality, you must first set up the required spare parts items groups.</span></span> <span data-ttu-id="7b7f2-118">その後、ワーク オーダーの完了時に資産 BOM を自動的に更新する場合は、その更新を処理するワーク オーダーのライフサイクル状態を設定できます。</span><span class="sxs-lookup"><span data-stu-id="7b7f2-118">Then, if you want the asset BOM to be automatically updated when a work order is completed, you can set up a work order lifecycle state to handle that update.</span></span> 


## <a name="set-up-spare-parts-item-groups"></a><span data-ttu-id="7b7f2-119">予備部品品目グループの設定</span><span class="sxs-lookup"><span data-stu-id="7b7f2-119">Set up spare parts item groups</span></span>

<span data-ttu-id="7b7f2-120">予備部品履歴の設定は、**在庫および倉庫管理**モジュールに作成された品目グループに基づいています。</span><span class="sxs-lookup"><span data-stu-id="7b7f2-120">The setup of spare parts history is based on item groups that are created in the **Inventory and warehouse management** module.</span></span> <span data-ttu-id="7b7f2-121">資産管理で、選択した品目グループ内の品目の予備部品履歴を追跡できるように品目グループを設定します。</span><span class="sxs-lookup"><span data-stu-id="7b7f2-121">In Asset Management, you set up item groups so that you can track spare parts history for the items in the selected item groups.</span></span>

1. <span data-ttu-id="7b7f2-122">**資産管理** \> **設定** \> **資産** \> **予備部品品目グループ**を選択します。</span><span class="sxs-lookup"><span data-stu-id="7b7f2-122">Select **Asset management** \> **Setup** \> **Asset** \> **Spare parts item groups**.</span></span>
2. <span data-ttu-id="7b7f2-123">品目グループを設定するには、**新規**を選択します。</span><span class="sxs-lookup"><span data-stu-id="7b7f2-123">Select **New** to set up an item group.</span></span>
3. <span data-ttu-id="7b7f2-124">**品目グループ** フィールドで、グループを選択します。</span><span class="sxs-lookup"><span data-stu-id="7b7f2-124">In the **Item group** field, select the group.</span></span> <span data-ttu-id="7b7f2-125">グループの名前は**名前**フィールドに自動的に入力されます。</span><span class="sxs-lookup"><span data-stu-id="7b7f2-125">The name of the group is automatically entered in the **Name** field.</span></span>

## <a name="view-and-update-asset-boms"></a><span data-ttu-id="7b7f2-126">資産 BOM の表示および更新</span><span class="sxs-lookup"><span data-stu-id="7b7f2-126">View and update asset BOMs</span></span>

<span data-ttu-id="7b7f2-127">ワーク オーダーに品目の消費を転記した後、**資産 BOM** ページで登録された品目の消費を表示できます。</span><span class="sxs-lookup"><span data-stu-id="7b7f2-127">After you post item consumption on a work order, you can view the registered item consumption on the **Asset BOM** page.</span></span>

1. <span data-ttu-id="7b7f2-128">**資産管理** \> **共通** \> **資産** \> **有効な資産**を選択します。</span><span class="sxs-lookup"><span data-stu-id="7b7f2-128">Select **Asset management** \> **Common** \> **Assets** \> **Active assets**.</span></span> <span data-ttu-id="7b7f2-129">一覧で資産を選択し、**資産 BOM** を選択します。</span><span class="sxs-lookup"><span data-stu-id="7b7f2-129">Select the asset in the list, and then select **Asset BOM**.</span></span>

    > [!NOTE]
    > <span data-ttu-id="7b7f2-130">すべての資産の全品目の消費登録を表示するには、**資産管理** \> **照会** \> **資産** \> **資産 BOM** を選択します。</span><span class="sxs-lookup"><span data-stu-id="7b7f2-130">To view all item consumption registrations on all assets, select **Asset management** \> **Inquiries** \> **Assets** \> **Asset BOM**.</span></span>

2. <span data-ttu-id="7b7f2-131">**資産 BOM の更新**を選択します。</span><span class="sxs-lookup"><span data-stu-id="7b7f2-131">Select **Update asset BOM**.</span></span> <span data-ttu-id="7b7f2-132">**選択**を選択すると、必要に応して更新に資産、資産タイプ、およびリソースを追加できます。</span><span class="sxs-lookup"><span data-stu-id="7b7f2-132">You can add assets, asset types, and resources to the update as you require by selecting **Select**.</span></span> <span data-ttu-id="7b7f2-133">**OK** を選択し、更新を開始します。</span><span class="sxs-lookup"><span data-stu-id="7b7f2-133">Select **OK** to start the update.</span></span> <span data-ttu-id="7b7f2-134">更新機能をバッチ ジョブとして設定することもできます。</span><span class="sxs-lookup"><span data-stu-id="7b7f2-134">You can also set up the Update function as a batch job.</span></span>
3. <span data-ttu-id="7b7f2-135">品目に関連する詳細情報を表示するには、在庫分析コードを追加できます。</span><span class="sxs-lookup"><span data-stu-id="7b7f2-135">If you want to see more information that is related to the items, you can add inventory dimensions.</span></span> <span data-ttu-id="7b7f2-136">**在庫** \> **分析コード表示**を選択し、表示する分析コードのチェック ボックスをオンにします。</span><span class="sxs-lookup"><span data-stu-id="7b7f2-136">Select **Inventory** \> **Dimensions display**, and then select the check boxes for the dimensions that you want to see.</span></span> <span data-ttu-id="7b7f2-137">**資産 BOM** ページのすべての資産に対してこの設定を維持するには、**設定の保存**オプションを**はい**に設定します。</span><span class="sxs-lookup"><span data-stu-id="7b7f2-137">To keep this setup for all assets on the **Asset BOM** page, set the **Save setup** option to **Yes**.</span></span>
4. <span data-ttu-id="7b7f2-138">資産管理で選択した明細行の品目が使用されている場所の概要を取得するには、資産、ジョブ タイプの既定値、予備部品、およびワーク オーダーに関連して、**品目の使用場所**を選択します。</span><span class="sxs-lookup"><span data-stu-id="7b7f2-138">To get an overview of where in Asset Management the item on the selected line is used, in relation to assets, job type defaults, spare parts, and work orders, select **Item where used**.</span></span> 
5. <span data-ttu-id="7b7f2-139">有効な品目明細行のみを表示する場合は、**表示** \> **現在**を選択します。</span><span class="sxs-lookup"><span data-stu-id="7b7f2-139">If you want to see only active item lines, select **View** \> **Current**.</span></span> <span data-ttu-id="7b7f2-140">有効期限が現在の日付より前の明細行を含むすべての明細行を表示するには、**表示** \> **すべて**を選択します。</span><span class="sxs-lookup"><span data-stu-id="7b7f2-140">To see all item lines, including lines where the expiration date is earlier than the current date, select **View** \> **All**.</span></span>

> [!NOTE]
> <span data-ttu-id="7b7f2-141">ワーク オーダーが完了したら、関連資産に関連のある一部の品目または予備部品の有効期限が切れている場合、または他の品目または予備部品に交換されている場合は、それに応じて資産 BOM を更新することをお勧めします。</span><span class="sxs-lookup"><span data-stu-id="7b7f2-141">When you've completed a work order, if some items or spare parts that are related to the related asset have expired or have been replaced by other items or spare parts, we recommend that you update the asset BOM accordingly.</span></span>

## <a name="create-a-new-item-line-in-an-asset-bom"></a><span data-ttu-id="7b7f2-142">資産 BOM で新しい品目明細行を作成する</span><span class="sxs-lookup"><span data-stu-id="7b7f2-142">Create a new item line in an asset BOM</span></span>

<span data-ttu-id="7b7f2-143">資産の品目明細行を手動で作成できます。</span><span class="sxs-lookup"><span data-stu-id="7b7f2-143">You can manually create item lines for assets.</span></span>

1. <span data-ttu-id="7b7f2-144">**資産 BOM** ページで、**新規**を選択します。</span><span class="sxs-lookup"><span data-stu-id="7b7f2-144">On the **Asset BOM** page, select **New**.</span></span>
2. <span data-ttu-id="7b7f2-145">**資産**フィールドで、品目明細行を追加する資産を選択します。</span><span class="sxs-lookup"><span data-stu-id="7b7f2-145">In the **Asset** field, select the asset to add an item line for.</span></span>
3. <span data-ttu-id="7b7f2-146">**行番号**フィールドに連続する明細行番号を入力します。</span><span class="sxs-lookup"><span data-stu-id="7b7f2-146">In the **Line number** field, enter a sequential line number.</span></span>
4. <span data-ttu-id="7b7f2-147">**有効開始**フィールドで、品目の開始日を入力します。</span><span class="sxs-lookup"><span data-stu-id="7b7f2-147">In the **Effective** field, enter a start date for the item.</span></span>
5. <span data-ttu-id="7b7f2-148">品目の有効期限が切れる場合**は、有効期限**フィールドに終了日を入力します。</span><span class="sxs-lookup"><span data-stu-id="7b7f2-148">If the item will expire, in the **Expiration** field, enter an end date.</span></span>
6. <span data-ttu-id="7b7f2-149">**品目番号** フィールドで、品目を選択します。</span><span class="sxs-lookup"><span data-stu-id="7b7f2-149">In the **Item number** field, select the item.</span></span> <span data-ttu-id="7b7f2-150">名前は**製品名**フィールドに自動的に入力されます。</span><span class="sxs-lookup"><span data-stu-id="7b7f2-150">The name is automatically entered in the **Product name** field.</span></span>
7. <span data-ttu-id="7b7f2-151">**数量**フィールドに、使用される数量を入力します。</span><span class="sxs-lookup"><span data-stu-id="7b7f2-151">In the **Quantity** field, enter the quantity that is used.</span></span> <span data-ttu-id="7b7f2-152">**単位**フィールドは自動的に更新されます。</span><span class="sxs-lookup"><span data-stu-id="7b7f2-152">The **Unit** field is automatically updated.</span></span>
