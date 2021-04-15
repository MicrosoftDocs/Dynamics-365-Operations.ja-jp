---
title: 資産ライフサイクル状態
description: このトピックでは、資産管理の資産ライフサイクル状態とライフサイクル モデルについて説明します。
author: johanhoffmann
ms.date: 06/26/2019
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: CatProcureCatalogEdit, CatProcureCatalogListPage, EntAssetLifecycleModelStateNext, EntAssetObjectLifecycleState, EntAssetLifecycleStateUpdate, EntAssetObjectLifecycleModel
audience: Application User
ms.reviewer: kamaybac
ms.custom: 2214
ms.assetid: 2f3e0441-414d-402b-b28b-7ab0d650d658
ms.search.region: Global
ms.author: johanho
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 985fedc13e28caee90c9db27b145e415d256208d
ms.sourcegitcommit: 0e8db169c3f90bd750826af76709ef5d621fd377
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/01/2021
ms.locfileid: "5808297"
---
# <a name="asset-lifecycle-states"></a><span data-ttu-id="e28eb-103">資産ライフサイクル状態</span><span class="sxs-lookup"><span data-stu-id="e28eb-103">Asset lifecycle states</span></span>

[!include [banner](../../includes/banner.md)]

 

<span data-ttu-id="e28eb-104">このトピックでは、資産管理の資産ライフサイクル状態とライフサイクル モデルについて説明します。</span><span class="sxs-lookup"><span data-stu-id="e28eb-104">This topic explains asset lifecycle states and lifecycle models in Asset Management.</span></span> <span data-ttu-id="e28eb-105">資産ライフサイクル状態は、資産が有効か無効かを定義するために使用されます。</span><span class="sxs-lookup"><span data-stu-id="e28eb-105">Asset lifecycle states are used to define whether an asset is active or inactive.</span></span> <span data-ttu-id="e28eb-106">たとえば、**作成済み**、**有効**、および **終了** などの資産ライフサイクル状態を設定できます。</span><span class="sxs-lookup"><span data-stu-id="e28eb-106">For example, you can set up asset lifecycle states such as **Created**, **Active**, and **Terminated**.</span></span>

> [!NOTE]
> - <span data-ttu-id="e28eb-107">要求ライフサイクル状態は、資産ライフサイクル状態にリンクされます。</span><span class="sxs-lookup"><span data-stu-id="e28eb-107">Request lifecycle states are linked to asset lifecycle states.</span></span> <span data-ttu-id="e28eb-108">したがって、要求が新しい要求ライフサイクル状態に変更されると、要求に添付された資産が新しい資産ライフサイクル状態に変更されます。</span><span class="sxs-lookup"><span data-stu-id="e28eb-108">Therefore, when a request is changed to a new request lifecycle state, the asset that is attached to the request is changed to a new asset lifecycle state.</span></span> <span data-ttu-id="e28eb-109">たとえば、要求のライフサイクル状態が、**受信** に変更された場合、添付された資産のライフサイクル状態は、**資産ライフサイクル状態モデル** ページの **資産ライフサイクル状態** クイック タブの **受信ライフサイクル状態** フィールドで選択されたライフサイクル状態に変更されます。</span><span class="sxs-lookup"><span data-stu-id="e28eb-109">For example, if the lifecycle state of a request is changed to **Inbound**, the lifecycle state of the attached asset is changed to the lifecycle state that is selected in the **Inbound lifecycle state** field on the **Asset lifecycle state** FastTab of the **Asset lifecycle state models** page.</span></span> 


<span data-ttu-id="e28eb-110">資産ライフサイクル状態は、資産ライフサイクル モデルで設定でき、さまざまなタイプの資産に必要なライフサイクル状態を定義できます。</span><span class="sxs-lookup"><span data-stu-id="e28eb-110">Asset lifecycle states can be set up in asset lifecycle models, where you can define the required lifecycle states for various types of assets.</span></span> <span data-ttu-id="e28eb-111">最初にライフサイクル状態を設定します。</span><span class="sxs-lookup"><span data-stu-id="e28eb-111">You first set up lifecycle states.</span></span> <span data-ttu-id="e28eb-112">次に、ライフサイクル モデルを作成し、そのライフサイクル状態を選択します。</span><span class="sxs-lookup"><span data-stu-id="e28eb-112">You then create a lifecycle model and select lifecycle states for it.</span></span>

1. <span data-ttu-id="e28eb-113">**資産管理** \> **設定** \> **資産** \> **ライフサイクル状態** を選択します。</span><span class="sxs-lookup"><span data-stu-id="e28eb-113">Select **Asset management** \> **Setup** \> **Assets** \> **Lifecycle states**.</span></span>
2. <span data-ttu-id="e28eb-114">**新規** を選択して、新しい資産ライフサイクル状態を作成します。</span><span class="sxs-lookup"><span data-stu-id="e28eb-114">Select **New** to create a new asset lifecycle state.</span></span>
3. <span data-ttu-id="e28eb-115">**ライフサイクル状態** フィールドに、ライフサイクル状態 ID を入力します。</span><span class="sxs-lookup"><span data-stu-id="e28eb-115">In the **Lifecycle state** field, enter the lifecycle state ID.</span></span>
4. <span data-ttu-id="e28eb-116">**名前** フィールドに、説明を入力します。</span><span class="sxs-lookup"><span data-stu-id="e28eb-116">In the **Name** field, enter a description.</span></span>

    <span data-ttu-id="e28eb-117">**ライフサイクル モデル** フィールドには、資産ライフサイクル状態を使用する資産ライフサイクル モデルの数が表示されます。</span><span class="sxs-lookup"><span data-stu-id="e28eb-117">The **Lifecycle models** field shows the number of asset lifecycle models that use the asset lifecycle state.</span></span>

5. <span data-ttu-id="e28eb-118">このライフサイクル状態を有効なライフサイクル状態にする必要がある場合は、**有効** オプションを **はい** に設定します (つまり、このライフサイクル状態の資産に対してワーク オーダーを作成できる場合)。</span><span class="sxs-lookup"><span data-stu-id="e28eb-118">Set the **Active** option to **Yes** if this lifecycle state should be an active lifecycle state (in other words, if work orders can be created for assets that are in this lifecycle state).</span></span>
6. <span data-ttu-id="e28eb-119">**作成済** の資産ライフサイクル状態で開いている資産カレンダー明細行を、このライフサイクル状態にあるときに削除する必要がある場合は、**開いているカレンダー明細行を削除** オプションを **はい** に設定します。</span><span class="sxs-lookup"><span data-stu-id="e28eb-119">Set the **Delete open calendar lines** option to **Yes** if open asset calendar lines that have an asset lifecycle state of **Created** should be deleted when they are in this lifecycle state.</span></span> <span data-ttu-id="e28eb-120">この設定は、資産に関連しなくなったオープン メンテナンス スケジュールをクリーンアップする場合に役立ちます (たとえば、資産が有効でなくなった場合)。</span><span class="sxs-lookup"><span data-stu-id="e28eb-120">This setting is useful if you want to clean up any open maintenance schedules that are no longer relevant for the asset (for example, if the asset is no longer active).</span></span>

> [!NOTE]
> <span data-ttu-id="e28eb-121">資産ライフサイクル状態、資産ライフサイクル モデル、および資産タイプが関連しています。</span><span class="sxs-lookup"><span data-stu-id="e28eb-121">Asset lifecycle states, asset lifecycle models, and asset types are related.</span></span> <span data-ttu-id="e28eb-122">これらは、ワーク オーダーのライフサイクル状態、ワーク オーダーのライフサイクル モデル、およびワーク オーダー タイプと同じ方法で使用されます。</span><span class="sxs-lookup"><span data-stu-id="e28eb-122">They are used in the same way as work order lifecycle states, work order lifecycle models, and work order types.</span></span> 


<span data-ttu-id="e28eb-123">必要な資産ライフサイクル状態を作成した後、資産ライフサイクル モデルでライフサイクル状態を設定できます。</span><span class="sxs-lookup"><span data-stu-id="e28eb-123">After you've created the required asset lifecycle states, you can set up lifecycle states in asset lifecycle models.</span></span>

1. <span data-ttu-id="e28eb-124">**資産管理** \> **設定** \> **資産** \> **ライフサイクル モデル** を選択します。</span><span class="sxs-lookup"><span data-stu-id="e28eb-124">Select **Asset management** \> **Setup** \> **assets** \> **lifecycle models**.</span></span>
2. <span data-ttu-id="e28eb-125">**新規** を選択して、新しい資産ライフサイクル モデルを作成します。</span><span class="sxs-lookup"><span data-stu-id="e28eb-125">Select **New** to create a new asset lifecycle model.</span></span>
3. <span data-ttu-id="e28eb-126">**ライフサイクル モデル** フィールドに、ライフサイクル モデル ID を入力します。</span><span class="sxs-lookup"><span data-stu-id="e28eb-126">In the **Lifecycle model** field, enter the lifecycle model ID.</span></span>
4. <span data-ttu-id="e28eb-127">**名前** フィールドに、説明を入力します。</span><span class="sxs-lookup"><span data-stu-id="e28eb-127">In the **Name** field, enter a description.</span></span>

    <span data-ttu-id="e28eb-128">**ライフサイクル状態** フィールドには、資産ライフサイクル モデルで選択されている資産ライフサイクル状態の数が表示されます。</span><span class="sxs-lookup"><span data-stu-id="e28eb-128">The **Lifecycle states** field shows the number of asset lifecycle states that are selected in the asset lifecycle model.</span></span> <span data-ttu-id="e28eb-129">**資産タイプ** フィールドには、ライフサイクル モデルを使用する資産タイプの数が表示されます。</span><span class="sxs-lookup"><span data-stu-id="e28eb-129">The **Asset types** field shows the number of asset types that use the lifecycle model.</span></span>

5. <span data-ttu-id="e28eb-130">**ライフサイクル状態** クイック タブで、資産ライフサイクル モデルに含める必要がある資産ライフサイクル状態を選択します。</span><span class="sxs-lookup"><span data-stu-id="e28eb-130">On the **Lifecycle states** FastTab, select the asset lifecycle states that should be included in the asset lifecycle model:</span></span>

    - <span data-ttu-id="e28eb-131">モデルのライフサイクル状態を使用するには、**残りのライフサイクル状態** セクションでそれを選択し、右矢印ボタン![右矢印](media/15-setup-for-objects.png)を選択して **選択されたライフサイクル状態** セクションに移動します。</span><span class="sxs-lookup"><span data-stu-id="e28eb-131">To use a lifecycle state for the model, select it in the **Lifecycle states remaining** section, and then select the right arrow button ![Right arrow](media/15-setup-for-objects.png) to move it to the **Lifecycle states selected** section.</span></span>
    - <span data-ttu-id="e28eb-132">モデルで使用可能なすべてのライフサイクル状態を使用するには、**使用可能なすべてのライフサイクル状態** ボタン![使用可能なすべてのライフサイクル状態](media/20-setup-for-objects.png)を選択します。</span><span class="sxs-lookup"><span data-stu-id="e28eb-132">To use all the available lifecycle states for the model, select the **All available lifecycle states** button ![All available lifecycle states](media/20-setup-for-objects.png).</span></span> <span data-ttu-id="e28eb-133">すべてのライフサイクル状態は、**選択されたライフサイクル状態** セクションに転送されます。</span><span class="sxs-lookup"><span data-stu-id="e28eb-133">All lifecycle states are transferred to the **Lifecycle states selected** section.</span></span>
    - <span data-ttu-id="e28eb-134">モデルからライフサイクル状態を削除するには、**選択されたライフサイクル状態** セクションでそれを選択し、左矢印ボタン![左矢印](media/16-setup-for-objects.png)を選択して **残りのライフサイクル状態** セクションに移動します。</span><span class="sxs-lookup"><span data-stu-id="e28eb-134">To remove a lifecycle state from the model, select it in the **lifecycle states selected** section, and then select the left arrow button ![Left arrow](media/16-setup-for-objects.png) to move it to the **Lifecycle states remaining** section.</span></span>

6. <span data-ttu-id="e28eb-135">**ライフサイクル状態の更新プログラム** を選択して、選択したライフサイクル状態に従うことができる資産ライフサイクル状態を定義します。</span><span class="sxs-lookup"><span data-stu-id="e28eb-135">Select **Lifecycle state updates** to define the asset lifecycle states that can follow a selected lifecycle state.</span></span>
7. <span data-ttu-id="e28eb-136">修復のために受け取った資産を処理する場合は、**資産状態** クイック タブを使用します。</span><span class="sxs-lookup"><span data-stu-id="e28eb-136">You use the **Asset state** FastTab if you handle assets that you receive for repair.</span></span> <span data-ttu-id="e28eb-137">**受信/送信** セクションで、資産ライフサイクル状態を選択して、修理のために受け取る資産のワークフローを示すことができます。</span><span class="sxs-lookup"><span data-stu-id="e28eb-137">In the **Inbound/outbound** section, you can select asset lifecycle states to indicate the workflow of an asset that you receive for repair.</span></span> <span data-ttu-id="e28eb-138">顧客または部門にローン資産を提供する場合は、**ローン** セクションで、ローン資産のライフサイクル状態を選択できます。</span><span class="sxs-lookup"><span data-stu-id="e28eb-138">If you offer loan assets to customers or departments, in the **Loan** section, you can select lifecycle states for loan assets.</span></span>


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]