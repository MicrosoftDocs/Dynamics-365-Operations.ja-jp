---
title: メンテナンス要求のライフサイクルの状態
description: このトピックでは、資産管理でメンテナンス要求のライフサイクルの状態を設定する方法について説明します。
author: josaw1
manager: tfehr
ms.date: 04/20/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: EntAssetRequestLifecycleState, EntAssetRequestLifecycleModel
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: mkirknel
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 5849e3a8c3c619916c718032579d4fe6444fa49b
ms.sourcegitcommit: c986d5234b81d31cc6d054298be6f6ec92c1754c
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 09/25/2020
ms.locfileid: "3889124"
---
# <a name="maintenance-request-lifecycle-states"></a><span data-ttu-id="cdc20-103">メンテナンス要求のライフサイクルの状態</span><span class="sxs-lookup"><span data-stu-id="cdc20-103">Maintenance request lifecycle states</span></span>

[!include [banner](../../includes/banner.md)]

 


<span data-ttu-id="cdc20-104">メンテナンス要求のイフサイクルの状態は、要求を実施できるステージを定義します。</span><span class="sxs-lookup"><span data-stu-id="cdc20-104">Maintenance request lifecycle states define the stages that a request can go through.</span></span> <span data-ttu-id="cdc20-105">**作成済**、**有効**、および**終了**などがその例です。</span><span class="sxs-lookup"><span data-stu-id="cdc20-105">Examples include **Created**, **Active**, and **Ended**.</span></span> <span data-ttu-id="cdc20-106">メンテナンス要求が作業指示書に変換される場合、メンテナンス要求のライフサイクルの状態を**終了**または**終了済**に更新して、メンテナンス要求がアクティブでなくなったことを示す必要があります。</span><span class="sxs-lookup"><span data-stu-id="cdc20-106">When a maintenance request is converted to a work order, the maintenance request lifecycle state should be updated to **Ended** or **Closed** to indicate that the maintenance request is no longer active.</span></span> <span data-ttu-id="cdc20-107">**すべてのメンテナンス要求**リスト ページで、ライフサイクルの状態に関係なく、すべてのメンテナンス要求を表示できます。</span><span class="sxs-lookup"><span data-stu-id="cdc20-107">On the **All maintenance requests** list page, you can view all maintenance requests, regardless of their lifecycle state.</span></span>

## <a name="set-up-maintenance-request-lifecycle-states"></a><span data-ttu-id="cdc20-108">メンテナンス要求のライフサイクルの状態の設定</span><span class="sxs-lookup"><span data-stu-id="cdc20-108">Set up maintenance request lifecycle states</span></span>

1. <span data-ttu-id="cdc20-109">**資産管理** \> **設定** \> **メンテナンス要求** \> **ライフサイクル状態**を選択します。</span><span class="sxs-lookup"><span data-stu-id="cdc20-109">Select **Asset management** \> **Setup** \> **Maintenance requests** \> **Lifecycle states**.</span></span>
2. <span data-ttu-id="cdc20-110">**新規**を選択して、メンテナンス要求のライフサイクルの状態を作成します。</span><span class="sxs-lookup"><span data-stu-id="cdc20-110">Select **New** to create a maintenance request lifecycle state.</span></span>
3. <span data-ttu-id="cdc20-111">**ライフサイクルの状態**フィールドに、ライフサイクルの状態 ID を入力します。</span><span class="sxs-lookup"><span data-stu-id="cdc20-111">In the **Lifecycle state** field, enter an ID for the lifecycle state.</span></span>
4. <span data-ttu-id="cdc20-112">**名前**フィールドに、名前を入力します。</span><span class="sxs-lookup"><span data-stu-id="cdc20-112">In the **Name** field, enter a name.</span></span>

    <span data-ttu-id="cdc20-113">**詳細**クイック タブで、**ライフサイクル モデル** フィールドには、このライフサイクルの状態を使用するメンテナンス要求のライフサイクル モデルの数が表示されます。</span><span class="sxs-lookup"><span data-stu-id="cdc20-113">On the **Details** FastTab, the **Lifecycle models** field shows the number of maintenance request lifecycle models that use this lifecycle state.</span></span>

5. <span data-ttu-id="cdc20-114">**一般**クイック タブで、このライフサイクルの状態にある間にメンテナンス要求を有効にする必要がある場合は、**有効**オプションを**はい**に設定します。</span><span class="sxs-lookup"><span data-stu-id="cdc20-114">On the **General** FastTab, set the **Active** option to **Yes** if a maintenance request should be active while it's in this lifecycle state.</span></span>
6. <span data-ttu-id="cdc20-115">このライフサイクルの状態のメンテナンス要求で実際の終了日時を自動的に入力する必要がある場合は、**実際の終了を設定** オプションを **はい** に設定します。</span><span class="sxs-lookup"><span data-stu-id="cdc20-115">Set the **Set actual end** option to **Yes** if an actual end date and time should automatically be entered on a maintenance request that is in this lifecycle state.</span></span>
7. <span data-ttu-id="cdc20-116">このライフサイクルの状態にあるメンテナンス要求からワーク オーダーを作成できる場合は、**ワーク オーダーの作成**オプションを**はい**に設定します。</span><span class="sxs-lookup"><span data-stu-id="cdc20-116">Set the **Create work order** option to **Yes** if a work order can be created from a maintenance request that is in this lifecycle state.</span></span>
8. <span data-ttu-id="cdc20-117">このライフサイクルの状態にある間にメンテナンス要求を削除できる場合は、**削除**オプションを**はい**に設定します。</span><span class="sxs-lookup"><span data-stu-id="cdc20-117">Set the **Delete** option to **Yes** if a maintenance request can be deleted while it's in this lifecycle state.</span></span>
9. <span data-ttu-id="cdc20-118">**更新** クイック タブの、**資産** セクションの **受信** および **送信** オプションは、引き取り修理修復を使用する場合に関連しています。</span><span class="sxs-lookup"><span data-stu-id="cdc20-118">On the **Update** FastTab, the **Inbound** and **Outbound** options in the **Asset** section are relevant if you use depot repair.</span></span> <span data-ttu-id="cdc20-119">保守要求で選択されている資産の資産ライフサイクルの状態が、**受信** または **送信** に設定されている場合に、その保守要求のメンテナンス要求ライフサイクルの状態が自動的に **受信** または **送信** に設定されている場合は、適切なオプションを **はい** に設定します。</span><span class="sxs-lookup"><span data-stu-id="cdc20-119">Set the appropriate option to **Yes** if the asset lifecycle state of assets that are selected on a maintenance request should automatically be updated to **Inbound** or **Outbound** when the maintenance request lifecycle state of that maintenance request is set to **Inbound** or **Outbound**.</span></span>

<span data-ttu-id="cdc20-120">次の図は、**メンテナンス要求のライフサイクルの状態**ページの例を示しています。</span><span class="sxs-lookup"><span data-stu-id="cdc20-120">The follow illustration shows an example of the **Maintenance request lifecycle states** page.</span></span>

![メンテナンス要求のライフサイクルの状態のページ](media/02-setup-for-requests.png)

> [!NOTE]
> <span data-ttu-id="cdc20-122">メンテナンス要求のライフサイクルの状態、ライフサイクルの状態グループ、およびタイプは、ワーク オーダー ライフサイクルの状態、ライフサイクルの状態グループ、およびタイプに関連し、同じように使用されます。</span><span class="sxs-lookup"><span data-stu-id="cdc20-122">Maintenance request lifecycle states, lifecycle state groups, and types are related to, and used in the same way as, work order lifecycle states, lifecycle state groups, and types.</span></span> 

## <a name="set-up-maintenance-request-lifecycle-models"></a><span data-ttu-id="cdc20-123">メンテナンス要求のライフサイクル モデルの設定</span><span class="sxs-lookup"><span data-stu-id="cdc20-123">Set up maintenance request lifecycle models</span></span>

<span data-ttu-id="cdc20-124">メンテナンス要求に必要なライフサイクル状態を作成したら、ライフサイクル状態グループまたはライフサイクル モデルに分割できます。</span><span class="sxs-lookup"><span data-stu-id="cdc20-124">After you've created the lifecycle states that are required for your maintenance requests, they can be divided into lifecycle state groups, or lifecycle models.</span></span> <span data-ttu-id="cdc20-125">メンテナンス要求のライフサイクル モデルは、さまざまなタイプのメンテナンス要求に使用できるフローを作成するために使用されます。</span><span class="sxs-lookup"><span data-stu-id="cdc20-125">Maintenance request lifecycle models are used to create the flow that can be used for different types of maintenance requests.</span></span> <span data-ttu-id="cdc20-126">少なくとも、1 つの標準のメンテナンス要求のライフサイクル モデルを作成する必要があります。</span><span class="sxs-lookup"><span data-stu-id="cdc20-126">At a minimum, one standard maintenance request lifecycle model should be created.</span></span>

1. <span data-ttu-id="cdc20-127">**資産管理** \> **設定** \> **メンテナンス要求** \> **ライフサイクル モデル**を選択します。</span><span class="sxs-lookup"><span data-stu-id="cdc20-127">Select **Asset management** \> **Setup** \> **Maintenance requests** \> **Lifecycle models**.</span></span>
2. <span data-ttu-id="cdc20-128">**新規**を選択して、メンテナンス要求のライフサイクル モデルの状態を作成します。</span><span class="sxs-lookup"><span data-stu-id="cdc20-128">Select **New** to create a maintenance request lifecycle model.</span></span>
3. <span data-ttu-id="cdc20-129">**ライフサイクル モデル**フィールドに、ライフサイクル モデルの ID を入力します。</span><span class="sxs-lookup"><span data-stu-id="cdc20-129">In the **Lifecycle model** field, enter an ID for the lifecycle model.</span></span>
4. <span data-ttu-id="cdc20-130">**名前**フィールドに、名前を入力します。</span><span class="sxs-lookup"><span data-stu-id="cdc20-130">In the **Name** field, enter a name.</span></span>

    <span data-ttu-id="cdc20-131">**詳細**クイック タブで、 **ライフサイクルの状態**には、ライフサイクル モデルで選択されているライフサイクルの状態の数が表示されます。</span><span class="sxs-lookup"><span data-stu-id="cdc20-131">On the **Details** FastTab, the **Lifecycle states** shows the number of lifecycle states that are selected in this lifecycle model.</span></span> <span data-ttu-id="cdc20-132">**メンテナンス要求タイプ**フィールドには、ライフサイクル モデルを使用するメンテナンス要求タイプの数が表示されます。</span><span class="sxs-lookup"><span data-stu-id="cdc20-132">The **Maintenance request types** field shows the number of maintenance request types that use this lifecycle model.</span></span>

5. <span data-ttu-id="cdc20-133">**ライフサイクルの状態**クイック タブで、ライフサイクル モデルに含める必要があるライフサイクル状態を選択します。</span><span class="sxs-lookup"><span data-stu-id="cdc20-133">On the **Lifecycle states** FastTab, select the lifecycle states that should be included in the lifecycle model:</span></span>

    - <span data-ttu-id="cdc20-134">ライフサイクル モデルにライフサイクルの状態を含めるには、**残りのライフサイクル状態**セクションでそれを選択し、右矢印ボタン![右矢印](media/03-setup-for-requests.png) を選択して**選択されたライフサイクルの状態**セクションに移動します。</span><span class="sxs-lookup"><span data-stu-id="cdc20-134">To include a lifecycle state in the lifecycle model, select it in the **Lifecycle states remaining** section, and then select the right arrow button ![Right arrow](media/03-setup-for-requests.png) to move it to the **Lifecycle states selected** section.</span></span>
    - <span data-ttu-id="cdc20-135">ライフサイクル モデルに使用可能なすべてのライフサイクルの状態を含めるには、**使用可能なすべての状態を選択**ボタン![使用可能なすべての状態を選択](media/04-setup-for-requests.png) を選択します。</span><span class="sxs-lookup"><span data-stu-id="cdc20-135">To include all the available lifecycle states in the lifecycle model, select the **Select all available states** button ![Select all available states](media/04-setup-for-requests.png).</span></span> <span data-ttu-id="cdc20-136">すべてのライフサイクルの状態は、**選択されたライフサイクルの状態**セクションに移動されます。</span><span class="sxs-lookup"><span data-stu-id="cdc20-136">All lifecycle states are moved to the **Lifecycle states selected** section.</span></span>
    - <span data-ttu-id="cdc20-137">ライフサイクル モデルからライフサイクルの状態を削除するには、**選択されたライフサイクルの状態**セクションでそれを選択し、左矢印ボタン![左矢印](media/05-setup-for-requests.png) を選択して**残りのライフサイクルの状態**セクションに移動します。</span><span class="sxs-lookup"><span data-stu-id="cdc20-137">To remove a lifecycle state from the lifecycle model, select it in the **Lifecycle states selected** section, and then select the left arrow button ![Left arrow](media/05-setup-for-requests.png) to move it to the **Lifecycle states remaining** section.</span></span>

6. <span data-ttu-id="cdc20-138">**一般**クイック タブでは、Depot 修復を使用する場合、**更新**セクションのフィールドが関連します。</span><span class="sxs-lookup"><span data-stu-id="cdc20-138">On the **General** FastTab, the fields in the **Updates** section are relevant if you use depot repair.</span></span>

    - <span data-ttu-id="cdc20-139">**受入済資産のライフサイクルの状態**フィールドで、メンテナンス要求で選択された資産が Depot 修復のために受け取る場合に自動的に更新される資産ライフサイクルの状態を選択します。</span><span class="sxs-lookup"><span data-stu-id="cdc20-139">In the **Lifecycle state for asset received** field, select the asset lifecycle state that assets that are selected on a maintenance request should automatically be updated to when they are received for depot repair.</span></span>
    - <span data-ttu-id="cdc20-140">**出荷済資産のライフサイクルの状態**フィールドで、メンテナンス要求で選択された資産が修復後に返品される場合に自動的に更新される資産ライフサイクルの状態を選択します。</span><span class="sxs-lookup"><span data-stu-id="cdc20-140">In the **Lifecycle state for asset delivered** field, select the lifecycle state that assets that are selected on a maintenance request should automatically be updated to when they are returned after repair.</span></span>

<span data-ttu-id="cdc20-141">次の図は、**メンテナンス要求のライフサイクル モデル** ページの例を示しています。</span><span class="sxs-lookup"><span data-stu-id="cdc20-141">The following illustration shows an example of the **Maintenance request lifecycle models** page.</span></span>

![メンテナンス要求のライフサイクル モデルのページ](media/06-setup-for-requests.png)
