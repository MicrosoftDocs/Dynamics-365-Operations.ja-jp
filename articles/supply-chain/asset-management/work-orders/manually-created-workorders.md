---
title: 手動で作成された作業指示書
description: このトピックでは、資産管理で作業指示書を手動で作成する方法について説明します。
author: josaw1
manager: tfehr
ms.date: 10/15/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: EntAssetWorkOrderTableCreateRelated, EntAssetWorkOrderTableCreate, EntAssetWorkOrderTableCopy
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: mkirknel
ms.search.validFrom: 2019-09-30
ms.dyn365.ops.version: 10.0.5
ms.openlocfilehash: 4a4b148d9ac5d032d2caa5fcea0398a5a3726f0e
ms.sourcegitcommit: 199848e78df5cb7c439b001bdbe1ece963593cdb
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 10/13/2020
ms.locfileid: "4431780"
---
# <a name="manually-created-work-orders"></a><span data-ttu-id="c9e9d-103">手動で作成された作業指示書</span><span class="sxs-lookup"><span data-stu-id="c9e9d-103">Manually created work orders</span></span>

[!include [banner](../../includes/banner.md)]


<span data-ttu-id="c9e9d-104">作業指示書は 2 つの方法で手動で作成することができます。</span><span class="sxs-lookup"><span data-stu-id="c9e9d-104">You can create work orders manually in two ways:</span></span>

- <span data-ttu-id="c9e9d-105">**すべての作業指示書** または **有効な作業指示書** ページで</span><span class="sxs-lookup"><span data-stu-id="c9e9d-105">On the **All work orders** or **Active work orders** page</span></span> 
- <span data-ttu-id="c9e9d-106">**すべてのメンテナンス要求** または **有効なメンテナンス要求** または **個人用の機能の場所のメンテナンス要求** ページで</span><span class="sxs-lookup"><span data-stu-id="c9e9d-106">On the **All maintenance requests** or **Active maintenance requests** or **My functional location maintenance requests** page</span></span> 

## <a name="create-work-order"></a><span data-ttu-id="c9e9d-107">作業指示書の作成</span><span class="sxs-lookup"><span data-stu-id="c9e9d-107">Create work order</span></span>

1. <span data-ttu-id="c9e9d-108">**資産管理** > **共通** > **作業指示書** > **すべての作業指示書** または **有効な作業指示書** の順に選択します。</span><span class="sxs-lookup"><span data-stu-id="c9e9d-108">Selece **Asset management** > **Common** > **Work orders** > **All work orders** or **Active work orders**.</span></span>

2. <span data-ttu-id="c9e9d-109">**新規** を選択します。</span><span class="sxs-lookup"><span data-stu-id="c9e9d-109">Select **New**.</span></span>

3. <span data-ttu-id="c9e9d-110">**作業指示書の作成** ダイアログで、**作業指示書のタイプ** フィールドを選択します。</span><span class="sxs-lookup"><span data-stu-id="c9e9d-110">In the **Create work order** dialog, select a work order type in the **Work order type** field.</span></span>

4. <span data-ttu-id="c9e9d-111">必要に応じて、**説明** を選択します。</span><span class="sxs-lookup"><span data-stu-id="c9e9d-111">If required, select a **Description**.</span></span>

5. <span data-ttu-id="c9e9d-112">**資産** フィールドで、資産を選択します。</span><span class="sxs-lookup"><span data-stu-id="c9e9d-112">In the **Asset** field, select the asset.</span></span>

>[!NOTE]
><span data-ttu-id="c9e9d-113">資産を選択すると、**資産** ドロップダウンに 3 つのタブが利用可能になる場合があります。</span><span class="sxs-lookup"><span data-stu-id="c9e9d-113">When you select an asset, three tabs might be available in the **Asset** drop-down:</span></span> 

- <span data-ttu-id="c9e9d-114">**有効な資産** - このタブには、資産ライフサイクル状態が「有効」であるすべての資産の一覧が含まれます。</span><span class="sxs-lookup"><span data-stu-id="c9e9d-114">**Active assets** - This tab contains a list of all assets that have an "Active" asset lifecycle state.</span></span> 
- <span data-ttu-id="c9e9d-115">**資産表示** - このタブには、機能の場所とそれらにインストールされている資産のツリー ビューが表示されます。</span><span class="sxs-lookup"><span data-stu-id="c9e9d-115">**Asset view** - This tab displays a tree view of functional locations and the assets installed on them.</span></span>
- <span data-ttu-id="c9e9d-116">**個人用資産** - このタブには、ユーザーが割り当てられる機能の場所 (システムにサイン インしている作業者) に関連する資産が含まれています。</span><span class="sxs-lookup"><span data-stu-id="c9e9d-116">**My assets** - This tab contains assets that are related to the functional locations that you (the worker who is signed in to the system) may be allocated to.</span></span> <span data-ttu-id="c9e9d-117">(設定の詳細については、[メンテナンス作業者と作業者グループ](../setup-for-objects/workers-and-worker-groups.md)を参照してください。) [メンテナンス作業者と作業者グループ](../setup-for-objects/workers-and-worker-groups.md)の作業者に設定されている機能の場所がない場合、**個人用資産** タブは使用できません。</span><span class="sxs-lookup"><span data-stu-id="c9e9d-117">(For information about the setup, see [Maintenance workers and worker groups](../setup-for-objects/workers-and-worker-groups.md).) If no functional locations are set up on a worker in [Maintenance workers and worker groups](../setup-for-objects/workers-and-worker-groups.md), the **My assets** tab isn't available.</span></span> 

6. <span data-ttu-id="c9e9d-118">**メンテナンス作業タイプ** フィールドで、作業指示書のメンテナンス作業タイプを選択します。</span><span class="sxs-lookup"><span data-stu-id="c9e9d-118">In the **Maintenance job type** field, select a maintenance job type for the work order.</span></span>

7. <span data-ttu-id="c9e9d-119">必要に応じて、**メンテナンス作業タイプ バリアント** および **取引** を選択します。</span><span class="sxs-lookup"><span data-stu-id="c9e9d-119">If required, select **Maintenance job type variant** and **Trade**.</span></span>

8. <span data-ttu-id="c9e9d-120">必要に応じて、**サービス レベル** フィールドで作業指示書のサービス レベルを変更することができます。</span><span class="sxs-lookup"><span data-stu-id="c9e9d-120">If required, you can change the work order service level in the **Service level** field.</span></span>

9. <span data-ttu-id="c9e9d-121">関連フィールドで、**開始予定** 日と **終了予定** 日を選択します。</span><span class="sxs-lookup"><span data-stu-id="c9e9d-121">Select **Expected start** and **Expected end** dates in the related fields.</span></span>

10. <span data-ttu-id="c9e9d-122">**OK** をクリックして、作業指示書を作成します。</span><span class="sxs-lookup"><span data-stu-id="c9e9d-122">Click **OK** to create the work order.</span></span>

11. <span data-ttu-id="c9e9d-123">**すべての作業指示書** リスト ページで、必要に応じて作業指示書を編集できます。</span><span class="sxs-lookup"><span data-stu-id="c9e9d-123">On the **All work orders** list page, you can edit the work order as you require.</span></span>

<span data-ttu-id="c9e9d-124">次のポイントに注意します。</span><span class="sxs-lookup"><span data-stu-id="c9e9d-124">Note the following points:</span></span>

- <span data-ttu-id="c9e9d-125">**すべての作業指示書** リスト ページの詳細表示で、**作業指示書のメンテナンス作業** クイック タブで明細行を追加することにより、作業指示書に複数の資産を追加することができます。</span><span class="sxs-lookup"><span data-stu-id="c9e9d-125">In the details view on the **All work orders** list page, you can add several assets to a work order by adding lines on the **Work order maintenance jobs** FastTab.</span></span> <span data-ttu-id="c9e9d-126">資産で、資産に対して選択されている資産タイプに定義されているメンテナンス作業タイプのみを選択することができます。</span><span class="sxs-lookup"><span data-stu-id="c9e9d-126">On an asset, you can select only the maintenance job types that are defined on the asset type that is selected on the asset.</span></span>  

- <span data-ttu-id="c9e9d-127">作業指示書で資産を既に使用した後に、資産サービス レベルまたは資産の重要度を変更した場合、作業指示書のサービス レベルまたは重要度はそれに応じて更新されません。</span><span class="sxs-lookup"><span data-stu-id="c9e9d-127">If you change an asset service level or an asset criticality after you've used the asset on a work order, the service level or criticality on the work order isn't updated accordingly.</span></span> <span data-ttu-id="c9e9d-128">サービス レベルと重要度の詳細については、[資産サービス レベル](../setup-for-objects/object-priorities.md) および[資産の重要度タイプ](../setup-for-objects/object-criticalities.md) を参照してください。</span><span class="sxs-lookup"><span data-stu-id="c9e9d-128">For more information about service levels and criticalities, see [Asset service levels](../setup-for-objects/object-priorities.md) and [Asset criticality types](../setup-for-objects/object-criticalities.md).</span></span>

- <span data-ttu-id="c9e9d-129">作業指示書の重要度は、作業指示書ジョブが作業指示書に追加または削除されるたびに再計算されます。</span><span class="sxs-lookup"><span data-stu-id="c9e9d-129">Criticality on a work order is recalculated every time a work order job is added to or deleted from the work order.</span></span>

- <span data-ttu-id="c9e9d-130">**すべての作業指示書** の詳細表示 > **ヘッダー** タブ > **スケジュール** クイック タブで、**担当グループ** または **担当者** フィールドで担当メンテナンス作業者グループまたは担当メンテナンス作業者を選択することができます。</span><span class="sxs-lookup"><span data-stu-id="c9e9d-130">In the **All work orders** details view > **Header** tab > **Schedule** FastTab, in the **Responsible group** or **Responsible** field, you can select a responsible maintenance worker group or a responsible maintenance worker.</span></span> <span data-ttu-id="c9e9d-131">これらの設定は、作業指示書が有効な間に変更できます。</span><span class="sxs-lookup"><span data-stu-id="c9e9d-131">These settings can be changed while the work order is active.</span></span> <span data-ttu-id="c9e9d-132">たとえば、作業指示書ライフサイクルの状態が変化したときに、それらを変更することができます。</span><span class="sxs-lookup"><span data-stu-id="c9e9d-132">For example, they can be changed when the work order lifecycle state changes.</span></span> <span data-ttu-id="c9e9d-133">作業指示書の作成中に行われる自動選択は、**担当メンテナンス作業者** ページでの設定に基づきます。</span><span class="sxs-lookup"><span data-stu-id="c9e9d-133">The automatic selection that is made during work order creation is based on the setup on the **Responsible maintenance workers** page.</span></span> <span data-ttu-id="c9e9d-134">作業指示書を作成した後に作業指示書のジョブを追加または削除し、作業指示書を更新した時に **担当グループ** フィールドおよび **担当者** フィールドが空白だった場合、資産管理は担当メンテナンス作業者グループまたは担当メンテナンス作業者について、設定ページで一致の可能性を検索しようとします。</span><span class="sxs-lookup"><span data-stu-id="c9e9d-134">If you add or remove work order jobs after you've created a work order, and if the **Responsible group** and **Responsible** fields are blank when you update the work order, Asset Management tries to find a responsible maintenance worker group or a responsible maintenance worker for a possible match on the setup page.</span></span> <span data-ttu-id="c9e9d-135">作業指示書を更新した時、**担当グループ** フィールドまたは **担当者** フィールドがすでに設定されている場合、変更は行われません。</span><span class="sxs-lookup"><span data-stu-id="c9e9d-135">If the **Responsible group** or **Responsible** field is already set when you update the work order, no changes are made.</span></span> <span data-ttu-id="c9e9d-136">担当メンテナンス作業者および担当メンテナンス作業者グループの詳細については、[担当メンテナンス作業者](../setup-for-maintenance-requests/responsible-workers.md) を参照してください。</span><span class="sxs-lookup"><span data-stu-id="c9e9d-136">For more information about responsible maintenance workers and worker groups, see [Responsible maintenance workers](../setup-for-maintenance-requests/responsible-workers.md).</span></span>

- <span data-ttu-id="c9e9d-137">[メンテナンスの状態](../controlling-and-reporting/maintenance-status.md) ページで、計算を実行し、受信および完了した作業指示書に関するワークロードの概要を取得することができます。</span><span class="sxs-lookup"><span data-stu-id="c9e9d-137">From the [Maintenance status](../controlling-and-reporting/maintenance-status.md) page, you can do a calculation to get an overview of the workload for incoming and completed work orders.</span></span>  

- <span data-ttu-id="c9e9d-138">**すべての作業指示書** ページの詳細表示にある **明細行の詳細** クイック タブで、**緯度** と **経度** フィールドを使用して、作業指示書ジョブで選択された資産の地理座標を追加できます。</span><span class="sxs-lookup"><span data-stu-id="c9e9d-138">In the details view of the **All work orders** page, on the **Line details** FastTab, you can use the **Latitude** and **Longitude** fields to add geographic coordinates for the asset that is selected on the work order job.</span></span>  


## <a name="create-related-work-order"></a><span data-ttu-id="c9e9d-139">関連作業指示書の作成</span><span class="sxs-lookup"><span data-stu-id="c9e9d-139">Create related work order</span></span>

<span data-ttu-id="c9e9d-140">既存の作業指示書に関連する作業指示書を作成することができます。</span><span class="sxs-lookup"><span data-stu-id="c9e9d-140">You can create a work order that is related to an existing work order.</span></span> <span data-ttu-id="c9e9d-141">この機能は、たとえば、基本および副次の作業指示書を作業する場合に便利です。</span><span class="sxs-lookup"><span data-stu-id="c9e9d-141">This capability is useful if, for example, you want to work with primary and secondary work orders.</span></span> <span data-ttu-id="c9e9d-142">新しい作業指示書は、既存の作業指示書からの作業指示ジョブに基づいています。</span><span class="sxs-lookup"><span data-stu-id="c9e9d-142">A new work order is based on a work order job from an existing work order.</span></span>

1. <span data-ttu-id="c9e9d-143">**資産管理** > **共通** > **作業指示書** > **すべての作業指示書** または **有効な作業指示書** の順に選択します。</span><span class="sxs-lookup"><span data-stu-id="c9e9d-143">Select **Asset management** > **Common** > **Work orders** > **All work orders** or **Active work orders**.</span></span>

2. <span data-ttu-id="c9e9d-144">関連する作業指示書を作成する作業指示書を選択します。</span><span class="sxs-lookup"><span data-stu-id="c9e9d-144">Select the work order to create a related work order for.</span></span>

3. <span data-ttu-id="c9e9d-145">アクション ペインの、**作業指示書** タブの、**新規** グループで、**関連する作業指示書** を選択します。</span><span class="sxs-lookup"><span data-stu-id="c9e9d-145">On the Action Pane, on the **Work order** tab, in the **New** group, select **Related work order**.</span></span>

4. <span data-ttu-id="c9e9d-146">**関連する作業指示書の作成** ダイアログ内の、**作業指示書ジョブ** フィールドで、関連する作業指示書を作成する作業指示書ジョブを選択します。</span><span class="sxs-lookup"><span data-stu-id="c9e9d-146">In the **Create related work order** dialog, in the **Work order job** field, select the work order job to create a related work order for.</span></span>

5. <span data-ttu-id="c9e9d-147">**メンテナンス作業タイプ** フィールドで、メンテナンス作業タイプを選択します。</span><span class="sxs-lookup"><span data-stu-id="c9e9d-147">Select a maintenance job type in the **Maintenance job type** field.</span></span>

6. <span data-ttu-id="c9e9d-148">**メンテナンス作業タイプ バリアント** および **取引** フィールドで、必要に応じて、関連するメンテナンス作業タイプ バリアントおよび取引を選択します。</span><span class="sxs-lookup"><span data-stu-id="c9e9d-148">Select a related maintenance job type variant and trade in the **Maintenance job type variant** and **Trade** fields, as you require.</span></span>

7. <span data-ttu-id="c9e9d-149">この作業指示書が、選択した作業指示書に対して作成された最初の関連する作業指示書である場合は、次の手順を実行します。</span><span class="sxs-lookup"><span data-stu-id="c9e9d-149">If this work order is the first related work order that has been created for the selected work order, follow these steps:</span></span>
    1. <span data-ttu-id="c9e9d-150">**新しい作業指示書** オプションを選択します。</span><span class="sxs-lookup"><span data-stu-id="c9e9d-150">Select the **New work order** option.</span></span>
    2. <span data-ttu-id="c9e9d-151">**作業指示書タイプ** フィールドで、作業指示書タイプを選択します。</span><span class="sxs-lookup"><span data-stu-id="c9e9d-151">In  the **Work order type** field, select a work order type.</span></span>
    3. <span data-ttu-id="c9e9d-152">**説明** に、説明を入力します。</span><span class="sxs-lookup"><span data-stu-id="c9e9d-152">In the **Description**, enter a description.</span></span>
    4. <span data-ttu-id="c9e9d-153">必要に応じて、**サービス レベル** フィールドで作業指示書のサービス レベルを変更します。</span><span class="sxs-lookup"><span data-stu-id="c9e9d-153">In the **Service level** field, change the work order service level as you require.</span></span>
    5. <span data-ttu-id="c9e9d-154">**開始予定** と **終了予定** フィールドで、開始予定日と終了予定日を選択します。</span><span class="sxs-lookup"><span data-stu-id="c9e9d-154">In the **Expected start** and **Expected end** fields, select the expected start and end dates.</span></span>
    6. <span data-ttu-id="c9e9d-155">**OK** を選択します。</span><span class="sxs-lookup"><span data-stu-id="c9e9d-155">Select **OK**.</span></span> <span data-ttu-id="c9e9d-156">新しい関連する作業指示書は、**すべての作業指示書** リスト ページに表示されます。</span><span class="sxs-lookup"><span data-stu-id="c9e9d-156">The new related work order is shown on the **All work orders** list page.</span></span>  

8. <span data-ttu-id="c9e9d-157">この関連する作業指示書を作成する作業指示書に既に関連する作業指示書がある場合、以下の手順に従って、新しい作業指示書ジョブを既存の関連する作業指示書に追加します。</span><span class="sxs-lookup"><span data-stu-id="c9e9d-157">If the work order that you're creating this related work order for already has related work orders, follow these steps to add a new work order job to an existing related work order:</span></span>
    1. <span data-ttu-id="c9e9d-158">**関連する作業指示書に追加** オプションを選択します。</span><span class="sxs-lookup"><span data-stu-id="c9e9d-158">Select the **Add to related work order** option.</span></span>
    2. <span data-ttu-id="c9e9d-159">**作業指示書** フィールドで、関連する作業指示書を選択して、新しい作業指示書ジョブを追加します。</span><span class="sxs-lookup"><span data-stu-id="c9e9d-159">In the **Work order** field, select the related work order to add a new work order job to.</span></span>
    3. <span data-ttu-id="c9e9d-160">必要に応じて、**サービス レベル** フィールドで作業指示書のサービス レベルを変更します。</span><span class="sxs-lookup"><span data-stu-id="c9e9d-160">In the **Service level** field, change the work order service level as you require.</span></span>
    4. <span data-ttu-id="c9e9d-161">**開始予定** と **終了予定** フィールドで、必要に応じて、開始予定日と終了予定日を変更します。</span><span class="sxs-lookup"><span data-stu-id="c9e9d-161">In the **Expected start** and **Expected end** fields, change the expected start and end dates as you require.</span></span>
    5. <span data-ttu-id="c9e9d-162">**OK** を選択します。</span><span class="sxs-lookup"><span data-stu-id="c9e9d-162">Select **OK**.</span></span> <span data-ttu-id="c9e9d-163">作業指示ジョブが既存の関連する作業指示書に追加されます。</span><span class="sxs-lookup"><span data-stu-id="c9e9d-163">The work order job is added to the existing related work order.</span></span>

<span data-ttu-id="c9e9d-164">次の図は、**関連する作業指示書の作成** ダイアログの例を示しています。</span><span class="sxs-lookup"><span data-stu-id="c9e9d-164">The illustration below shows an example of the **Create related work order** dialog.</span></span>

![図 1](media/03-work-orders.png)

>[!NOTE]
><span data-ttu-id="c9e9d-166">**資産管理パラメーター** > **作業指示書** タブ > **関連する作業指示書のマスク** フィールドで関連する作業指示書のマスクを設定している場合、作業指示書 ID はマスクの設定に基づいて作成されます。</span><span class="sxs-lookup"><span data-stu-id="c9e9d-166">If you've set up a related work order mask in **Asset management parameters** > **Work orders** tab > **Related work order mask** field, work order IDs are created according to the mask setup.</span></span> <span data-ttu-id="c9e9d-167">関連する作業指示書のマスクが設定されていない場合は、次に使用可能な作業指示書 ID が関連する作業指示書に対して使用されます。</span><span class="sxs-lookup"><span data-stu-id="c9e9d-167">If no related work order mask is set up, the next available work order ID is used for related work orders.</span></span>

## <a name="copy-a-work-order"></a><span data-ttu-id="c9e9d-168">作業指示書のコピー</span><span class="sxs-lookup"><span data-stu-id="c9e9d-168">Copy a work order</span></span>

<span data-ttu-id="c9e9d-169">既存の作業指示書から新しい作業指示書をすばやく作成することができます。</span><span class="sxs-lookup"><span data-stu-id="c9e9d-169">You can quickly create a new work order from an existing work order.</span></span> <span data-ttu-id="c9e9d-170">この作業指示書の操作方法は、[メンテナンス計画](../preventive-and-reactive-maintenance/maintenance-plans.md) に基づく作業指示書の作成とは異なります</span><span class="sxs-lookup"><span data-stu-id="c9e9d-170">This way of working with work orders differs from the creation of work orders based on [maintenance plans](../preventive-and-reactive-maintenance/maintenance-plans.md).</span></span> <span data-ttu-id="c9e9d-171">この機能は、たとえば、作業指示書に多くの作業指示書ジョブが含まれており、さまざまなジョブが異なる資産で定期的に完了する必要がある場合に役立ちます。</span><span class="sxs-lookup"><span data-stu-id="c9e9d-171">It's useful if, for example, a work order contains many work order jobs, and the various jobs should be completed on different assets at regular intervals.</span></span>

1. <span data-ttu-id="c9e9d-172">**資産管理** > **共通** > **作業指示書** > **すべての作業指示書** または **有効な作業指示書** の順に選択します。</span><span class="sxs-lookup"><span data-stu-id="c9e9d-172">Select **Asset management** > **Common** > **Work orders** > **All work orders** or **Active work orders**.</span></span>

2. <span data-ttu-id="c9e9d-173">コンテンツをコピーする作業指示書を選択します。</span><span class="sxs-lookup"><span data-stu-id="c9e9d-173">Select the work order to copy content from.</span></span>

3. <span data-ttu-id="c9e9d-174">アクション ペイン > **作業指示書** タブ > **新規** グループで、**作業指示書のコピー** を選択します。</span><span class="sxs-lookup"><span data-stu-id="c9e9d-174">On the Action Pane > **Work order** tab > **New** group, select **Copy work order**.</span></span>

4. <span data-ttu-id="c9e9d-175">選択した作業指示書から作業指示書の設定が表示されます。</span><span class="sxs-lookup"><span data-stu-id="c9e9d-175">The work order setup from the selected work order is shown.</span></span> <span data-ttu-id="c9e9d-176">必要に応じて、一部のフィールドを編集することができます。</span><span class="sxs-lookup"><span data-stu-id="c9e9d-176">You can edit some of the fields as you require.</span></span>

5. <span data-ttu-id="c9e9d-177">**OK** を選択して、新しい作業指示書を作成します。</span><span class="sxs-lookup"><span data-stu-id="c9e9d-177">Select **OK** to create the new work order.</span></span>

6. <span data-ttu-id="c9e9d-178">**すべての作業指示書** リスト ページで、必要に応じて作業指示書を編集できます。</span><span class="sxs-lookup"><span data-stu-id="c9e9d-178">On the **All work orders** list page, you can edit the work order as you require.</span></span>

>[!NOTE]
><span data-ttu-id="c9e9d-179">新しい作業指示書が作成されると、一部の情報が既存の作業指示書から直接コピーされます。</span><span class="sxs-lookup"><span data-stu-id="c9e9d-179">When the new work order is created, some information is copied directly from the existing work order.</span></span> <span data-ttu-id="c9e9d-180">予測、ツール、メンテナンス チェックリスト、機能の場所、住所、およびスケジューリングに関する情報は、コピーされません。</span><span class="sxs-lookup"><span data-stu-id="c9e9d-180">Information about forecasts, tools, maintenance checklists, functional location, addresses, and scheduling isn't copied.</span></span> <span data-ttu-id="c9e9d-181">代わりに、資産管理の現在の設定から初期化されます。</span><span class="sxs-lookup"><span data-stu-id="c9e9d-181">Instead, it's initialized from the current setup in Asset Management.</span></span> <span data-ttu-id="c9e9d-182">したがって、最初の作業指示書が作成された時点から、作業指示書のコピーを作成した時点までの情報が変更された場合、変更は新しい作業指示書に含まれます。</span><span class="sxs-lookup"><span data-stu-id="c9e9d-182">Therefore, if that information was changed between the time when the first work order was created and the time when you made a copy of the work order, the changes are included in the new work order.</span></span> <span data-ttu-id="c9e9d-183">例には、予測または更新されたメンテナンス チェックリストの変更が含まれます。</span><span class="sxs-lookup"><span data-stu-id="c9e9d-183">Examples include changes to forecasts and updates to maintenance checklists.</span></span>

<span data-ttu-id="c9e9d-184">次の図は、**作業指示書のコピー** ダイアログの例を示しています。</span><span class="sxs-lookup"><span data-stu-id="c9e9d-184">The illustration below shows an example of the **Copy work order** dialog.</span></span>

![図 2](media/04-work-orders.png)


## <a name="create-a-work-order-based-on-a-maintenance-request"></a><span data-ttu-id="c9e9d-186">メンテナンス要求に基づく作業指示書の作成</span><span class="sxs-lookup"><span data-stu-id="c9e9d-186">Create a work order based on a maintenance request</span></span>

1. <span data-ttu-id="c9e9d-187">**資産管理** > **共通** > **メンテナンス要求** > **すべてのメンテナンス要求** または **有効なメンテナンス要求** を選択します。</span><span class="sxs-lookup"><span data-stu-id="c9e9d-187">Select **Asset management** > **Common** > **Maintenance requests** > **All maintenance requests** or **Active maintenance requests**.</span></span>

2. <span data-ttu-id="c9e9d-188">作業指示書を作成するメンテナンス要求を選択し、**編集** をクリックします。</span><span class="sxs-lookup"><span data-stu-id="c9e9d-188">Select the maintenance request to create a work order for, and click **Edit**.</span></span>

3. <span data-ttu-id="c9e9d-189">アクション ペイン > **メンテナンス要求** タブ > **新規** グループで、**作業指示書** を選択します。</span><span class="sxs-lookup"><span data-stu-id="c9e9d-189">On the Action Pane > **Maintenance request** tab > **New** group, select **Work order**.</span></span>

4. <span data-ttu-id="c9e9d-190">**作業指示書** ダイアログで、フィールドを設定します。</span><span class="sxs-lookup"><span data-stu-id="c9e9d-190">In the **Work order** dialog, set the fields.</span></span> <span data-ttu-id="c9e9d-191">メンテナンス要求でメンテナンス ジョブ タイプが選択されている場合、必要に応じて、作業指示書の作成時に別のメンテナンス ジョブ タイプを選択することができます。</span><span class="sxs-lookup"><span data-stu-id="c9e9d-191">If a maintenance job type has been selected in the maintenance request, you can select a different maintenance job type when you create the work order, as you require.</span></span>

5. <span data-ttu-id="c9e9d-192">**OK** を選択します。</span><span class="sxs-lookup"><span data-stu-id="c9e9d-192">Select **OK**.</span></span> <span data-ttu-id="c9e9d-193">メッセージは、作業指示書が作成されたことを通知します。</span><span class="sxs-lookup"><span data-stu-id="c9e9d-193">A message notifies you that the work order has been created.</span></span>

6. <span data-ttu-id="c9e9d-194">メンテナンス要求に関連付けられている作業指示書を確認する場合、**すべてのメンテナンス要求** または **有効なメンテナンス要求** リスト ページで、メンテナンス要求を選択します。</span><span class="sxs-lookup"><span data-stu-id="c9e9d-194">To view the work orders that are connected to a maintenance request, on the **All maintenance requests** or **Active maintenance requests** list page, select the maintenance request.</span></span> <span data-ttu-id="c9e9d-195">その後、アクション ペインの **メンテナンス要求** タブの **新規** グループで、**作業指示書** を選択します。</span><span class="sxs-lookup"><span data-stu-id="c9e9d-195">Then, on the Action Pane, on the **Maintenance request** tab, in the **View** group, select **Work orders**.</span></span>


<span data-ttu-id="c9e9d-196">次の図は、**作業指示書の作成** ダイアログの例を示しています。</span><span class="sxs-lookup"><span data-stu-id="c9e9d-196">The illustration below shows an example of the **Create work order** dialog.</span></span>

![図 3](media/05-work-orders.png)


>[!NOTE]
><span data-ttu-id="c9e9d-198">作業指示書を自動的に作成する場合は、メンテナンス計画ジョブをスケジュールしたり、資産に対して、"自動作成" [メンテナンス計画](../preventive-and-reactive-maintenance/maintenance-plans.md) または [メンテナンス ラウンド](../preventive-and-reactive-maintenance/maintenance-rounds.md) を設定できます。</span><span class="sxs-lookup"><span data-stu-id="c9e9d-198">If you want work orders to be created automatically, you can schedule maintenance plan jobs, or you can set up "Auto create" [maintenance plans](../preventive-and-reactive-maintenance/maintenance-plans.md) or [maintenance rounds](../preventive-and-reactive-maintenance/maintenance-rounds.md) on an asset.</span></span> <span data-ttu-id="c9e9d-199">**すべてのメンテナンススケジュール** リスト ページのメンテナンス要求から作成された作業指示書には、メンテナンス要求で選択されたメンテナンス ジョブ タイプがあります。</span><span class="sxs-lookup"><span data-stu-id="c9e9d-199">Work orders that are created from maintenance requests on the **All maintenance schedule** list page have the maintenance job types that are selected on the maintenance requests.</span></span>

