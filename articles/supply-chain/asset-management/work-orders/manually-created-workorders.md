---
title: 手動で作成された作業指示書
description: このトピックでは、資産管理で作業指示書を手動で作成する方法について説明します。
author: josaw1
manager: AnnBe
ms.date: 08/15/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: mkirknel
ms.search.validFrom: 2019-08-15
ms.dyn365.ops.version: 10.0.5
ms.openlocfilehash: 261448a134a7c1aacfbb4ea6f954ce03a63c23e2
ms.sourcegitcommit: f5bfa3212bc3ef7d944a358ef08fe8863fd93b91
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 08/16/2019
ms.locfileid: "1875755"
---
# <a name="manually-created-work-orders"></a><span data-ttu-id="ee678-103">手動で作成された作業指示書</span><span class="sxs-lookup"><span data-stu-id="ee678-103">Manually created work orders</span></span>

[!include [banner](../../includes/banner.md)]

[!include [banner](../../includes/preview-banner.md)]


<span data-ttu-id="ee678-104">作業指示書は 2 つの方法で手動で作成することができます。</span><span class="sxs-lookup"><span data-stu-id="ee678-104">You can create work orders manually in two ways:</span></span>

- <span data-ttu-id="ee678-105">**すべての作業指示書**または**は有効な作業指示書**</span><span class="sxs-lookup"><span data-stu-id="ee678-105">in **All work orders** or **Active work orders**</span></span>  
- <span data-ttu-id="ee678-106">**すべてのメンテナンス要求**または**有効なメンテナンス要求**または**個人用の機能の場所のメンテナンス要求**</span><span class="sxs-lookup"><span data-stu-id="ee678-106">in **All maintenance requests** or **Active maintenance requests** or **My functional location maintenance requests**</span></span>  

## <a name="create-work-order"></a><span data-ttu-id="ee678-107">作業指示書の作成</span><span class="sxs-lookup"><span data-stu-id="ee678-107">Create work order</span></span>

1. <span data-ttu-id="ee678-108">**資産管理** > **共通** > **作業指示書** > **すべての作業指示書**または**有効な作業指示書**の順にクリックします。</span><span class="sxs-lookup"><span data-stu-id="ee678-108">Click **Asset management** > **Common** > **Work orders** > **All work orders** or **Active work orders**.</span></span>

2. <span data-ttu-id="ee678-109">**新規**ボタンをクリックします。</span><span class="sxs-lookup"><span data-stu-id="ee678-109">Click the **New** button.</span></span>

3. <span data-ttu-id="ee678-110">**作業指示書**ドロップダウンから、作業指示書のタイプを選択します。</span><span class="sxs-lookup"><span data-stu-id="ee678-110">In the **Create work order** drop-down, select a work order type.</span></span>

4. <span data-ttu-id="ee678-111">必要に応じて、説明を選択します。</span><span class="sxs-lookup"><span data-stu-id="ee678-111">If required, select a description.</span></span>

5. <span data-ttu-id="ee678-112">作業指示書の資産とメンテナンス作業タイプを選択します。</span><span class="sxs-lookup"><span data-stu-id="ee678-112">Select the asset for the work order as well as a maintenance job type.</span></span>

>[!NOTE]
><span data-ttu-id="ee678-113">資産を選択すると、3 つのタブが使用可能になります。**個人用資産**タブには、ユーザー (システムにログオンしている作業者) が割り当てられる機能の場所に関連する資産が含まれます ([メンテナンス作業者と作業者グループ](../setup-for-objects/workers-and-worker-groups.md) で設定)。</span><span class="sxs-lookup"><span data-stu-id="ee678-113">When you select an asset, three tabs may be available: The **My assets** tab contains assets related to the functional locations to which you (the worker who is logged on the system) may be allocated (set up in [Maintenance workers and worker groups](../setup-for-objects/workers-and-worker-groups.md)).</span></span> <span data-ttu-id="ee678-114">[メンテナンス作業者と作業者グループ](../setup-for-objects/workers-and-worker-groups.md) で作業者に機能の場所が設定されていない場合は、**個人用資産**タブは表示されません。</span><span class="sxs-lookup"><span data-stu-id="ee678-114">If no functional locations are set up on a worker in [Maintenance workers and worker groups](../setup-for-objects/workers-and-worker-groups.md), the **My assets** tab will not be visible.</span></span> <span data-ttu-id="ee678-115">**有効な資産**タブには、資産ライフサイクル状態が「有効」であるすべての資産の一覧が表示されます。</span><span class="sxs-lookup"><span data-stu-id="ee678-115">The **Active assets** tab contains a list of all assets with asset lifecycle state "Active".</span></span> <span data-ttu-id="ee678-116">**資産表示**タブには、それらの場所にインストールされている機能の場所と資産のツリー ビューが表示されます。</span><span class="sxs-lookup"><span data-stu-id="ee678-116">The **Asset view** tab displays a tree view of functional locations and assets installed on those locations.</span></span>

6. <span data-ttu-id="ee678-117">必要に応じて、**メンテナンス作業タイプ バリアント**および**取引**を選択します。</span><span class="sxs-lookup"><span data-stu-id="ee678-117">If required, select **Maintenance job type variant** and **Trade**.</span></span>

7. <span data-ttu-id="ee678-118">必要に応じて、**サービス レベル** フィールドで作業指示書のサービス レベルを変更することができます。</span><span class="sxs-lookup"><span data-stu-id="ee678-118">If required, you can change the work order service level in the **Service level** field.</span></span>

8. <span data-ttu-id="ee678-119">関連フィールドで、開始予定日と終了予定日を選択します。</span><span class="sxs-lookup"><span data-stu-id="ee678-119">Select expected start and end dates in the related fields.</span></span>

9. <span data-ttu-id="ee678-120">**OK** をクリックして新しい作業指示書を作成します。</span><span class="sxs-lookup"><span data-stu-id="ee678-120">Click **OK** to create a new work order.</span></span>

10. <span data-ttu-id="ee678-121">必要に応じて、**すべての作業指示書**で作業指示書を編集します。</span><span class="sxs-lookup"><span data-stu-id="ee678-121">Edit the work order in **All work orders**, if required.</span></span>

- <span data-ttu-id="ee678-122">**すべての作業指示書**で、**作業指示書のメンテナンス作業**クイック タブで明細行を追加することにより、詳細表示で作業指示書に複数の資産を追加することができます。</span><span class="sxs-lookup"><span data-stu-id="ee678-122">In **All work orders**, You can add several assets to a work order in Details view by adding lines on the **Work order maintenance jobs** FastTab.</span></span> <span data-ttu-id="ee678-123">資産について、資産に対して選択されている資産タイプに定義されているメンテナンス作業タイプのみを選択することができます。</span><span class="sxs-lookup"><span data-stu-id="ee678-123">On an asset, you can only select the maintenance job types that are defined on the asset type selected for the asset.</span></span>  
- <span data-ttu-id="ee678-124">作業指示書で使用した後、資産のサービス レベルまたは資産の重要度を変更した場合 ([資産のサービス レベル](../setup-for-objects/object-priorities.md) および [資産の重要度](../setup-for-objects/object-criticalities.md) を参照)、作業指示書のサービス レベルまたは重要度はそれに応じて更新されることはありません。</span><span class="sxs-lookup"><span data-stu-id="ee678-124">If you have changed an asset service level or an asset criticality after you have used them on a work order (refer to [Asset service levels](../setup-for-objects/object-priorities.md) and [Asset criticalities](../setup-for-objects/object-criticalities.md)), the service level or criticality on the work order is not updated accordingly.</span></span>
- <span data-ttu-id="ee678-125">作業指示書の重要度は、作業指示書に作業指示書明細行が追加または削除されるたびに再計算されます。</span><span class="sxs-lookup"><span data-stu-id="ee678-125">Criticality on a work order is re-calculated each time a work order line is added or deleted on the work order.</span></span>
- <span data-ttu-id="ee678-126">**すべての作業指示書**の詳細表示 > **ヘッダー**表示 > **スケジュール** クイック タブで、**担当グループ**または**担当者**フィールドで担当メンテナンス作業者グループまたは担当メンテナンス作業者を選択することができます。</span><span class="sxs-lookup"><span data-stu-id="ee678-126">In **All work orders** Details view > **Header** view > **Schedule** FastTab, you can select a responsible maintenance worker group or a responsible maintenance worker in the **Responsible group** or **Responsible** fields.</span></span> <span data-ttu-id="ee678-127">これらの設定は、作業指示書が有効である限り、作業指示書のライフサイクルの状態が変化した時などに変更することができます。</span><span class="sxs-lookup"><span data-stu-id="ee678-127">These settings can be changed as long as the work order is active, for example, when the work order lifecycle state changes.</span></span> <span data-ttu-id="ee678-128">作業指示書の作成中に行われる自動選択は、**担当メンテナンス作業者**での設定に基づきます。</span><span class="sxs-lookup"><span data-stu-id="ee678-128">The automatic selection made during work order creation is based on the setup in **Responsible maintenance workers**.</span></span> <span data-ttu-id="ee678-129">作業指示書を作成した後に作業指示書のジョブを追加または削除し、作業指示書を更新した時に**担当グループ** フィールドおよび**担当者**フィールドが空白だった場合、資産管理は担当メンテナンス作業者グループまたは担当メンテナンス作業者について、設定フォームで一致の可能性を検索します。</span><span class="sxs-lookup"><span data-stu-id="ee678-129">If you add or remove work order jobs after you have created a work order, and the **Responsible group** field and the **Responsible** field are blank when you update the work order, Asset Management searches for a possible match in the setup form for a responsible maintenance worker group or a responsible maintenance worker.</span></span> <span data-ttu-id="ee678-130">作業指示書を更新した時、**担当グループ** フィールドまたは**担当者** フィールドがすでに入力されている場合、変更は行われません。</span><span class="sxs-lookup"><span data-stu-id="ee678-130">If the **Responsible group** field or the **Responsible** field is already filled out when you update the work order, no changes are made.</span></span> 

- <span data-ttu-id="ee678-131">**メンテナンスの状態**で計算を実行し、受信および完了した作業指示書に関するワークロードの概要を取得することができます。</span><span class="sxs-lookup"><span data-stu-id="ee678-131">In **Maintenance status**, you can make a calculation to get an overview of workload regarding incoming and completed work orders.</span></span>  

- <span data-ttu-id="ee678-132">**明細行の詳細**クイック タブで、**緯度**および**経度**フィールドを使用して、作業指示書のジョブで選択した資産の地理座標を追加します。</span><span class="sxs-lookup"><span data-stu-id="ee678-132">On the **Line details** FastTab, use the **Latitude** and **Longitude** fields to add geographic coordinates for the asset selected on the work order job.</span></span>  

## <a name="create-related-work-order"></a><span data-ttu-id="ee678-133">関連作業指示書の作成</span><span class="sxs-lookup"><span data-stu-id="ee678-133">Create related work order</span></span>

<span data-ttu-id="ee678-134">たとえば、基本および副次の作業指示書を実行する場合に、既存の作業指示書に関連する作業指示書を作成できます。</span><span class="sxs-lookup"><span data-stu-id="ee678-134">You can create a related work order to an existing work order if, for example, you want to work with primary and secondary work orders.</span></span> <span data-ttu-id="ee678-135">新しい作業指示書は、既存の作業指示書からの作業指示ジョブに基づいています。</span><span class="sxs-lookup"><span data-stu-id="ee678-135">A new work order is based on a work order job from an existing work order.</span></span>

1. <span data-ttu-id="ee678-136">**資産管理** > **共通** > **作業指示書** > **すべての作業指示書**または**有効な作業指示書**の順にクリックします。</span><span class="sxs-lookup"><span data-stu-id="ee678-136">Click **Asset management** > **Common** > **Work orders** > **All work orders** or **Active work orders**.</span></span>

2. <span data-ttu-id="ee678-137">関連する作業指示書を作成する作業指示書を選択します。</span><span class="sxs-lookup"><span data-stu-id="ee678-137">Select the work order for which you want to make a related work order.</span></span>

3. <span data-ttu-id="ee678-138">**関連する作業指示書**をクリックします。</span><span class="sxs-lookup"><span data-stu-id="ee678-138">Click **Related work order**.</span></span>

4. <span data-ttu-id="ee678-139">**関連する作業指示書の作成**ドロップダウン ダイアログ内の、**作業指示ジョブ**フィールドで、関連する作業指示書を作成する作業指示ジョブを選択します。</span><span class="sxs-lookup"><span data-stu-id="ee678-139">In the **Create related work order** drop-down dialog, select the work order job for which you want to create a related work order in the **Work order job** field.</span></span>

5. <span data-ttu-id="ee678-140">**メンテナンス ジョブ タイプ** フィールドでメンテナンス ジョブ タイプを選択し、必要に応じて、**メンテナンス ジョブ タイプ バリアント**と**取引**フィールドで関連するメンテナンス ジョブ タイプ バリアントと取引を選択します。</span><span class="sxs-lookup"><span data-stu-id="ee678-140">Select a maintenance job type in the **Maintenance job type** field and, if required, a related maintenance job type variant and trade in the **Maintenance job type variant** and **Trade** fields.</span></span>

6. <span data-ttu-id="ee678-141">これが最初に関連する作業指示書である場合、**新しい作業指示書**オプション ボタンをクリックします。</span><span class="sxs-lookup"><span data-stu-id="ee678-141">If this is the first related work order you make, click the **New work order** radio button.</span></span>

7. <span data-ttu-id="ee678-142">関連するフィールドで、**作業指示書タイプ**および**説明**を選択します。</span><span class="sxs-lookup"><span data-stu-id="ee678-142">Select a **Work order type** and a **Description** in the related fields.</span></span>

8. <span data-ttu-id="ee678-143">必要に応じて、**サービス レベル** フィールドで作業指示書のサービス レベルを変更します。</span><span class="sxs-lookup"><span data-stu-id="ee678-143">If required, change the work order service level in the **Service level** field.</span></span>

9. <span data-ttu-id="ee678-144">関連フィールドで、開始予定日と終了予定日を挿入します。</span><span class="sxs-lookup"><span data-stu-id="ee678-144">Insert expected start and end dates in the related fields.</span></span>

10. <span data-ttu-id="ee678-145">**OK**をクリックします。</span><span class="sxs-lookup"><span data-stu-id="ee678-145">Click **OK**.</span></span> <span data-ttu-id="ee678-146">新しい関連作業指示書は、**すべての作業指示書**のリストに表示されます。</span><span class="sxs-lookup"><span data-stu-id="ee678-146">The new related work order is shown in the **All work orders** list.</span></span>

11. <span data-ttu-id="ee678-147">関連する作業指示書が既にある作業指示書に関連する作業指示を作成した場合、既に関連付けられている作業指示書に作業指示のジョブを追加することができます。</span><span class="sxs-lookup"><span data-stu-id="ee678-147">If you create a related work order on a work order that already has related work orders, you can add the work order job to an already related work order.</span></span> <span data-ttu-id="ee678-148">これを実行するには、手順 6 で**関連する作業指示に追加**ラジオ ボタンをクリックします。</span><span class="sxs-lookup"><span data-stu-id="ee678-148">This is done by clicking the **Add to related work order** radio button in step 6.</span></span> <span data-ttu-id="ee678-149">次に、新しい作業指示ジョブを追加する関連作業指示書を選択します。</span><span class="sxs-lookup"><span data-stu-id="ee678-149">Then you select the related work order to which you want to add a new work order job.</span></span> <span data-ttu-id="ee678-150">必要に応じて**サービス レベル**、**開始予定**、および**終了予定**フィールドを編集し、**OK** をクリックします。</span><span class="sxs-lookup"><span data-stu-id="ee678-150">Edit the **Service level**, **Expected start**, and **Expected end** fields, as required, and click **OK**.</span></span> <span data-ttu-id="ee678-151">作業指示ジョブが既存の関連する作業指示書に追加されます。</span><span class="sxs-lookup"><span data-stu-id="ee678-151">The work order job is added to the existing related work order.</span></span>


![図 1](media/03-work-orders.png)

<span data-ttu-id="ee678-153">**メモ:** **資産管理パラメータ** > **作業指示書**のリンク > **関連する作業指示書のマスク** フィールドで関連する作業指示書のマスクを設定している場合、作業指示 ID はマスク設定にしたがって作成されます。</span><span class="sxs-lookup"><span data-stu-id="ee678-153">**Note:** If you have set up a related work order mask in **Asset management parameters** > **Work orders** link > **Related work order mask** field, work order IDs will be created in accordance with the mask setup.</span></span> <span data-ttu-id="ee678-154">関連する作業指示書のマスクが設定されていない場合は、次に使用可能な作業指示 ID が関連する作業指示書に対して使用されます。</span><span class="sxs-lookup"><span data-stu-id="ee678-154">If no related work order mask is set up, the next available work order ID will be used for related work orders.</span></span>

## <a name="copy-work-order"></a><span data-ttu-id="ee678-155">作業指示書のコピー</span><span class="sxs-lookup"><span data-stu-id="ee678-155">Copy work order</span></span>

<span data-ttu-id="ee678-156">既存の作業指示書から新しい作業指示書をすばやく作成することができます。</span><span class="sxs-lookup"><span data-stu-id="ee678-156">It is possible to quickly create a new work order from an existing work order.</span></span> <span data-ttu-id="ee678-157">この作業指示書の作業方法は、メンテナンス計画に基づく作業指示書の作成とは異なります。</span><span class="sxs-lookup"><span data-stu-id="ee678-157">This way of working with work orders is different from creating work orders based on maintenance plans.</span></span> <span data-ttu-id="ee678-158">この機能は、たとえば、作業指示書に多くの作業指示ジョブと定期的に完了する必要のある異なる資産に対するさまざまなジョブが含まれている場合などに役に立ちます。</span><span class="sxs-lookup"><span data-stu-id="ee678-158">It is useful if, for example, you have a work order containing many work order jobs with various jobs on different assets that should be completed at regular intervals.</span></span>

1. <span data-ttu-id="ee678-159">**資産管理** > **共通** > **作業指示書** > **すべての作業指示書**または**有効な作業指示書**の順にクリックします。</span><span class="sxs-lookup"><span data-stu-id="ee678-159">Click **Asset management** > **Common** > **Work orders** > **All work orders** or **Active work orders**.</span></span>

2. <span data-ttu-id="ee678-160">コンテンツをコピーする作業順序書を選択します。</span><span class="sxs-lookup"><span data-stu-id="ee678-160">Select the work order from which you want to copy content.</span></span>

3. <span data-ttu-id="ee678-161">**作業指示書のコピー**をクリックします。</span><span class="sxs-lookup"><span data-stu-id="ee678-161">Click **Copy work order**.</span></span> <span data-ttu-id="ee678-162">選択した作業指示書から作業指示書の設定が表示されます。</span><span class="sxs-lookup"><span data-stu-id="ee678-162">The work order setup from the selected work order is shown.</span></span> <span data-ttu-id="ee678-163">必要に応じて、一部のフィールドを編集することができます。</span><span class="sxs-lookup"><span data-stu-id="ee678-163">If required, you can edit some of the fields.</span></span>

4. <span data-ttu-id="ee678-164">**OK** をクリックして、新しい作業指示書を作成します。</span><span class="sxs-lookup"><span data-stu-id="ee678-164">Click **OK** to create the new work order.</span></span>

5. <span data-ttu-id="ee678-165">必要に応じて、**すべての作業指示書**で作業指示書を編集します。</span><span class="sxs-lookup"><span data-stu-id="ee678-165">Edit the work order in **All work orders**, if required.</span></span>

>[!NOTE]
><span data-ttu-id="ee678-166">新しい作業指示書が作成されると、一部の情報が既存の作業指示書から直接コピーされます。</span><span class="sxs-lookup"><span data-stu-id="ee678-166">When the new work order is created, some information is copied directly from the existing work order.</span></span> <span data-ttu-id="ee678-167">予測、ツール、メンテナンス チェックリスト、機能の場所、住所、およびスケジューリングに関する情報はコピーされませんが、資産管理の現在の設定から初期化されます。</span><span class="sxs-lookup"><span data-stu-id="ee678-167">Information regarding forecasts, tools, maintenance checklists, functional location, addresses, and scheduling is not copied, but initialized from the current setup in Asset Management.</span></span> <span data-ttu-id="ee678-168">つまり、これらのデータに対して、最初の作業指示書を作成した時から作業指示書のコピーを作成した時までに変更を加えた場合、それら変更は作成した新しい作業指示書に含まれていることを意味します。</span><span class="sxs-lookup"><span data-stu-id="ee678-168">This means that if changes were made in those data from the time of creation of the first work order until the time you made a copy of the work order, those changes are included in the new work order you have created.</span></span> <span data-ttu-id="ee678-169">たとえば、予測または更新されたメンテナンス チェックリストの変更などです。</span><span class="sxs-lookup"><span data-stu-id="ee678-169">Examples are changes in forecasts or updated maintenance checklists.</span></span>


![図 2](media/04-work-orders.png)


## <a name="create-work-order-based-on-a-maintenance-request"></a><span data-ttu-id="ee678-171">メンテナンス要求に基づく作業指示書の作成</span><span class="sxs-lookup"><span data-stu-id="ee678-171">Create work order based on a maintenance request</span></span>

1. <span data-ttu-id="ee678-172">**資産管理** > **共通** > **メンテナンス要求** > **すべてのメンテナンス要求**または**有効なメンテナンス要求**をクリックします。</span><span class="sxs-lookup"><span data-stu-id="ee678-172">Click **Asset management** > **Common** > **Maintenance requests** > **All maintenance requests** or **Active maintenance requests**.</span></span>

2. <span data-ttu-id="ee678-173">作業指示書を作成するメンテナンス要求を選択し、**編集**をクリックします。</span><span class="sxs-lookup"><span data-stu-id="ee678-173">Select the maintenance request for which you want to create a work order, and click **Edit**.</span></span>

3. <span data-ttu-id="ee678-174">**すべての要求**で、**作業指示書**をクリックします。</span><span class="sxs-lookup"><span data-stu-id="ee678-174">In **All requests**, click **Work order**.</span></span>

4. <span data-ttu-id="ee678-175">**作業指示書**ドロップダウンに入力します。</span><span class="sxs-lookup"><span data-stu-id="ee678-175">Fill out the **Work order** drop-down.</span></span> <span data-ttu-id="ee678-176">メンテナンス要求でメンテナンス ジョブ タイプが選択されている場合、必要に応じて、作業指示書の作成時に別のメンテナンス ジョブ タイプを選択することができます。</span><span class="sxs-lookup"><span data-stu-id="ee678-176">If a maintenance job type has been selected in the maintenance request, you are able to select another maintenance job type, if required, when you create the work order.</span></span>

5. <span data-ttu-id="ee678-177">**OK**をクリックします。</span><span class="sxs-lookup"><span data-stu-id="ee678-177">Click **OK**.</span></span> <span data-ttu-id="ee678-178">作業指示書が作成されたことを知らせるメッセージが表示されます。</span><span class="sxs-lookup"><span data-stu-id="ee678-178">You will see a message informing you that the work order has been created.</span></span>

6. <span data-ttu-id="ee678-179">メンテナンス要求に関連付けられている作業指示書を確認する場合、**すべてのメンテナンス要求**または**有効なメンテナンス要求**リストのメンテナンス要求を選択し、**作業指示書**ボタンをクリックします。</span><span class="sxs-lookup"><span data-stu-id="ee678-179">If you want to see which work orders are connected to a maintenance request, select the maintenance request in the **All maintenance requests** or **Active maintenance requests** lists, and click the **Work orders** button.</span></span>


![図 3](media/05-work-orders.png)


>[!NOTE]
><span data-ttu-id="ee678-181">また、メンテナンス計画ジョブをスケジュールしたり、資産に対してメンテナンス プランまたはメンテナンス ラウンドの「自動作成」を設定することにより、作業指示書を自動的に作成することもできます。</span><span class="sxs-lookup"><span data-stu-id="ee678-181">Work orders can also be created automatically by scheduling maintenance plan jobs, or by setting up "Auto create" maintenance plans or maintenance rounds on an asset.</span></span> <span data-ttu-id="ee678-182">**メンテナンス スケジュール**のメンテナンス要求から作成された作業指示書は、メンテナンス要求で選択されたメンテナンス ジョブ タイプと共に作成されます。</span><span class="sxs-lookup"><span data-stu-id="ee678-182">Work orders created from maintenance requests in **Maintenance schedule** are created with the maintenance job types selected in the maintenance requests.</span></span>

