---
title: 発注書に基づいた資産の作成
description: このトピックでは、資産管理でメンテナンス ジョブの資産を作成するための基礎として使用できる資産品目の一覧を作成する方法について説明します。
author: josaw1
manager: tfehr
ms.date: 06/26/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: CatProcureCatalogEdit, CatProcureCatalogListPage, EntAssetObjectItem, EntAssetPendingAssets
audience: Application User
ms.reviewer: kamaybac
ms.custom: 2214
ms.assetid: 2f3e0441-414d-402b-b28b-7ab0d650d658
ms.search.region: Global
ms.author: riluan
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 83419fa5c6b6aee0b321c526565c3518deaf4bd0
ms.sourcegitcommit: deac22ba5377a912d93fe408c5ae875706378c2d
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 01/16/2021
ms.locfileid: "5016987"
---
# <a name="create-assets-based-on-purchase-orders"></a><span data-ttu-id="0d005-103">発注書に基づいた資産の作成</span><span class="sxs-lookup"><span data-stu-id="0d005-103">Create assets based on purchase orders</span></span>

[!include [banner](../../includes/banner.md)]

 

<span data-ttu-id="0d005-104">このトピックでは、資産管理でメンテナンス ジョブの資産を作成するための基礎として使用できる資産品目の一覧を作成する方法について説明します。</span><span class="sxs-lookup"><span data-stu-id="0d005-104">This topic explains how you can create a list of asset items that can be used as a basis for creating assets for maintenance jobs in Asset Management.</span></span> <span data-ttu-id="0d005-105">資産品目に基づいて、それらの品目で作成された発注書明細行の一覧を表示できます。</span><span class="sxs-lookup"><span data-stu-id="0d005-105">Based on the asset items, you are able to view a list of the purchase order lines that have been created on those items.</span></span> <span data-ttu-id="0d005-106">この機能の目的は、発注書に基づいて資産管理で資産を簡単に作成することです。</span><span class="sxs-lookup"><span data-stu-id="0d005-106">The purpose of this functionality is to easily create an asset in Asset Management based on a purchase order.</span></span>

<span data-ttu-id="0d005-107">まず、**資産品目** の発注書から、資産を作成するために使用する品目を設定します。</span><span class="sxs-lookup"><span data-stu-id="0d005-107">First, you set up the items to be used for creating assets from a purchase order in **Asset items**.</span></span> <span data-ttu-id="0d005-108">発注書明細行を作成した後、**保留中の資産** で資産を作成します。</span><span class="sxs-lookup"><span data-stu-id="0d005-108">After creating a purchase order line, you create the assets in **Pending assets**.</span></span> <span data-ttu-id="0d005-109">資産を作成する必要のある発注書のステージを決定できます。</span><span class="sxs-lookup"><span data-stu-id="0d005-109">It is possible to decide at which stage of the purchase order the asset should be created.</span></span>


## <a name="select-asset-items"></a><span data-ttu-id="0d005-110">資産品目を選択する</span><span class="sxs-lookup"><span data-stu-id="0d005-110">Select asset items</span></span>

1. <span data-ttu-id="0d005-111">**資産管理** > **設定** > **資産** > **品目** の順にクリックします。</span><span class="sxs-lookup"><span data-stu-id="0d005-111">Click **Asset management** > **Setup** > **Assets** > **Items**.</span></span>
2. <span data-ttu-id="0d005-112">**新規** をクリックして、新しい資産品目を作成します。</span><span class="sxs-lookup"><span data-stu-id="0d005-112">Click **New** to create a new asset item.</span></span>
3. <span data-ttu-id="0d005-113">**品目番号** フィールドで、品目を選択します。</span><span class="sxs-lookup"><span data-stu-id="0d005-113">Select the item in the **Item number** field.</span></span> <span data-ttu-id="0d005-114">そのフィールドを離れると、品目名が **製品名** フィールドに自動的に挿入されます。</span><span class="sxs-lookup"><span data-stu-id="0d005-114">When you leave that field, the item name is automatically inserted in the **Product name** field.</span></span>
4. <span data-ttu-id="0d005-115">**一般** クイック タブで、品目の資産タイプを選択します。</span><span class="sxs-lookup"><span data-stu-id="0d005-115">On the **General** FastTab, select an asset type for the item.</span></span>
5. <span data-ttu-id="0d005-116">品目に対する資産メーカーとモデルを選択します。</span><span class="sxs-lookup"><span data-stu-id="0d005-116">Select asset manufacturer and model for the item.</span></span>
6. <span data-ttu-id="0d005-117">品目の保存</span><span class="sxs-lookup"><span data-stu-id="0d005-117">Save the item.</span></span>


## <a name="create-assets-from-pending-assets"></a><span data-ttu-id="0d005-118">保留中の資産から資産を作成する</span><span class="sxs-lookup"><span data-stu-id="0d005-118">Create assets from pending assets</span></span>

1. <span data-ttu-id="0d005-119">**資産管理** > **共通** > **資産** > **保留中の資産** の順にクリックします。</span><span class="sxs-lookup"><span data-stu-id="0d005-119">Click **Asset management** > **Common** > **Assets** > **Pending Assets**.</span></span>
2. <span data-ttu-id="0d005-120">**資産品目** で選択した品目に基づいて、発注書の更新された一覧が表示されます。</span><span class="sxs-lookup"><span data-stu-id="0d005-120">You will see an updated list of the purchase orders based on the items selected in **Asset items**.</span></span>
3. <span data-ttu-id="0d005-121">発注書の状態をフィルター処理して、資産を作成するライフサイクル状態を選択できます。</span><span class="sxs-lookup"><span data-stu-id="0d005-121">You can filter the status of purchase orders to select at which lifecycle state the asset should be created.</span></span> <span data-ttu-id="0d005-122">たとえば、製品入庫が発注書に転記されている場合にのみ資産を作成できます。</span><span class="sxs-lookup"><span data-stu-id="0d005-122">For example, you may only want to create assets when a product receipt has been posted on a purchase order.</span></span>
4. <span data-ttu-id="0d005-123">品目に関する詳細情報を表示するには、発注書明細行の **参照番号** リンクを選択します。</span><span class="sxs-lookup"><span data-stu-id="0d005-123">Select the **Reference number** link on a purchase order line to view detailed information about the item.</span></span>
5. <span data-ttu-id="0d005-124">**在庫分析コード** クイック タブに表示される分析コードを編集する場合は、**分析コードの表示** ボタンをクリックしてから、選択を行います。</span><span class="sxs-lookup"><span data-stu-id="0d005-124">If you want to edit which dimensions are displayed on the **Inventory dimensions** FastTab, click the **Display Dimensions** button, and make your selections.</span></span>
6. <span data-ttu-id="0d005-125">発注書明細行に基づいて資産を作成する場合は、リスト ページでその明細行に対する **マーク** 列のチェック ボックスを選択してから、**資産の作成** をクリックします。</span><span class="sxs-lookup"><span data-stu-id="0d005-125">If you want to create an asset based on a purchase order line, select the check box in the **Mark** column for that line on the list page, and click **Create assets**.</span></span> <span data-ttu-id="0d005-126">資産 ID を通知するメッセージが表示されます。</span><span class="sxs-lookup"><span data-stu-id="0d005-126">A message will be displayed informing you of the asset ID.</span></span>
7. <span data-ttu-id="0d005-127">**全資産** リストで資産を選択し、**編集** をクリックして資産に詳細情報を追加します。</span><span class="sxs-lookup"><span data-stu-id="0d005-127">Select the asset in the **All assets** list and click **Edit** to add more information to the asset.</span></span>
8. <span data-ttu-id="0d005-128">**保留中の資産** で、資産を作成しないため明細行を削除する場合は、その明細行に対する **マーク** 列のチェック ボックスを選択してから、**保留中の資産を破棄** をクリックします。</span><span class="sxs-lookup"><span data-stu-id="0d005-128">In **Pending assets**, if you want to delete a line because you don't want to create an asset, select the check box in the **Mark** column for that line, and click **Discard pending assets**.</span></span> <span data-ttu-id="0d005-129">資産 ID を通知するメッセージが表示されます。</span><span class="sxs-lookup"><span data-stu-id="0d005-129">A message will be displayed informing you of the asset ID.</span></span> <span data-ttu-id="0d005-130">発注書または販売注文を削除するのではなく、**資産管理** で資産を作成できたレコードだけを削除します。</span><span class="sxs-lookup"><span data-stu-id="0d005-130">You are not deleting the purchase order or sales order, just the record from which you could have created an asset in **Asset Management**.</span></span>

>[!NOTE]
><span data-ttu-id="0d005-131">すべての製品分析コード (サイズ、色、コンフィギュレーションなど) が資産属性に自動的に転送されます。</span><span class="sxs-lookup"><span data-stu-id="0d005-131">All product dimensions (size, color, configuration etc.) are automatically transferred to the asset attributes.</span></span> <span data-ttu-id="0d005-132">追跡用分析コード (シリアル番号) は、資産の作成時に資産に直接保存されます。</span><span class="sxs-lookup"><span data-stu-id="0d005-132">Tracking dimensions (serial number) are stored directly on the asset when the asset is created.</span></span>


## <a name="find-pending-assets"></a><span data-ttu-id="0d005-133">保留中の資産を検索する</span><span class="sxs-lookup"><span data-stu-id="0d005-133">Find pending assets</span></span>

<span data-ttu-id="0d005-134">**保留中の資産数** を実行して、保留中の資産を確認できます。</span><span class="sxs-lookup"><span data-stu-id="0d005-134">You can run a **Pending asset count** to check for pending assets.</span></span> <span data-ttu-id="0d005-135">たとえば、この機能は、保留中の資産を資産として作成する準備が整うたびに通知を受け取るのに使用できます。</span><span class="sxs-lookup"><span data-stu-id="0d005-135">For example, this function can be used for receiving a notification each time a pending asset is ready to be created as an asset.</span></span>

1. <span data-ttu-id="0d005-136">**資産管理** > **定期処理** > **資産** > **保留中の資産数** の順にクリックします。</span><span class="sxs-lookup"><span data-stu-id="0d005-136">Click **Asset management** > **Periodic** > **Assets** > **Pending asset count**.</span></span>
2. <span data-ttu-id="0d005-137">**OK** をクリックしてジョブを実行し、**保留中の資産** で一覧を更新します。</span><span class="sxs-lookup"><span data-stu-id="0d005-137">Click **OK** to run the job and update the list in **Pending assets**.</span></span>
3. <span data-ttu-id="0d005-138">たとえば、1 日 1 回、このジョブをバッチ ジョブとして実行するように設定できます。</span><span class="sxs-lookup"><span data-stu-id="0d005-138">You can set up this job to run as a batch job, for example, once each day.</span></span>

<span data-ttu-id="0d005-139">**注意:** 関連品目に基づいて資産を作成した *後* に発注書でデータが変更される場合、それらの変更は資産に反映されません。</span><span class="sxs-lookup"><span data-stu-id="0d005-139">**Caution:** If data is changed on a purchase order *after* you have created an asset based on the appertaining item, those changes will not be reflected on the asset.</span></span>
