---
title: 作業指示書プール
description: このトピックでは資産管理でワーク オーダー プールを操作する方法について説明します。
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
ms.openlocfilehash: 069fa02073808fd7bbaac9bc1603e49ce4d450eb
ms.sourcegitcommit: f5bfa3212bc3ef7d944a358ef08fe8863fd93b91
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 08/16/2019
ms.locfileid: "1875757"
---
# <a name="work-order-pools"></a><span data-ttu-id="dd9cc-103">作業指示書プール</span><span class="sxs-lookup"><span data-stu-id="dd9cc-103">Work order pools</span></span>


[!include [banner](../../includes/banner.md)]

[!include [banner](../../includes/preview-banner.md)]


<span data-ttu-id="dd9cc-104">ワーク オーダー プールを使用して、共通点があるワーク オーダーをグループ化できます。</span><span class="sxs-lookup"><span data-stu-id="dd9cc-104">You can use work order pools to group work orders that have something in common.</span></span> <span data-ttu-id="dd9cc-105">たとえば、次のようなワーク オーダー プールを作成できます。</span><span class="sxs-lookup"><span data-stu-id="dd9cc-105">For example, you can create work order pools for</span></span>

- <span data-ttu-id="dd9cc-106">メンテナンス作業者 A、メンテナンス作業者 B、などの作業者</span><span class="sxs-lookup"><span data-stu-id="dd9cc-106">work crews, for example, Maintenance Crew A, Maintenance Crew B</span></span>  

- <span data-ttu-id="dd9cc-107">電気技師または配管工などの専門的なスキル</span><span class="sxs-lookup"><span data-stu-id="dd9cc-107">professional skills, for example, electricians or plumbers</span></span>  

- <span data-ttu-id="dd9cc-108">物理的場所</span><span class="sxs-lookup"><span data-stu-id="dd9cc-108">physical locations</span></span>  

- <span data-ttu-id="dd9cc-109">週またはその他の期間などのタイム スケジュール</span><span class="sxs-lookup"><span data-stu-id="dd9cc-109">time schedules, for example, weeks or other periods</span></span>  


<span data-ttu-id="dd9cc-110">必要に応じて、1 つのワーク オーダーを複数のワーク オーダー プールに配置できます。</span><span class="sxs-lookup"><span data-stu-id="dd9cc-110">If required, one work order can be placed in many work order pools.</span></span>


## <a name="create-work-order-pool"></a><span data-ttu-id="dd9cc-111">ワーク オーダー プールの作成</span><span class="sxs-lookup"><span data-stu-id="dd9cc-111">Create work order pool</span></span>

<span data-ttu-id="dd9cc-112">**すべてのワーク オーダー プール**または**有効なワーク オーダー プール**では、ワーク オーダー プールの概要を取得し、新しいプールを作成できます。</span><span class="sxs-lookup"><span data-stu-id="dd9cc-112">In **All work order pools** or **Active work order pools**, you can get an overview of your work order pools and create new pools.</span></span>

1. <span data-ttu-id="dd9cc-113">**資産管理** > **共通** > **ワーク オーダー プール** > **すべてのワーク オーダー プール**または**有効なワーク オーダー プール**の順にクリックします。</span><span class="sxs-lookup"><span data-stu-id="dd9cc-113">Click **Asset management** > **Common** > **Work order pools** > **All work order pools** or **Active work order pools**.</span></span>

2. <span data-ttu-id="dd9cc-114">**新規** をクリックします。</span><span class="sxs-lookup"><span data-stu-id="dd9cc-114">Click **New**.</span></span>

3. <span data-ttu-id="dd9cc-115">**プール** フィールドにワーク オーダー プール ID を、**名前**フィールドに名前を挿入します。</span><span class="sxs-lookup"><span data-stu-id="dd9cc-115">Insert a work order pool ID in the **Pool** field and a name in the **Name** field.</span></span>

4. <span data-ttu-id="dd9cc-116">**有効**なトグル ボタンで「はい」を選択して、ワーク オーダー プールが有効であることを示します。</span><span class="sxs-lookup"><span data-stu-id="dd9cc-116">Select "Yes" on the **Active** toggle button to indicate that the work order pool is active.</span></span>

5. <span data-ttu-id="dd9cc-117">ワーク オーダーをワーク オーダー プールから自動的に削除する場合は、**ワーク オーダー リレーションの削除**トグル ボタンで「はい」を選択します。</span><span class="sxs-lookup"><span data-stu-id="dd9cc-117">Select "Yes" on the **Delete work order relations** toggle button if you want work orders to be automatically removed from the work order pool.</span></span>

6. <span data-ttu-id="dd9cc-118">**ライフサイクル状態の削除**フィールドで、ワーク オーダーのライフサイクル状態を選択します。</span><span class="sxs-lookup"><span data-stu-id="dd9cc-118">In the **Delete lifecycle state** field, select the work order lifecycle state.</span></span> <span data-ttu-id="dd9cc-119">たとえば、ワーク オーダーを完了するためのワーク オーダー ライフサイクル状態は、ワーク オーダー プールへのリレーションを自動的に削除するように設定できます。</span><span class="sxs-lookup"><span data-stu-id="dd9cc-119">For example, the work order lifecycle state for completing a work order could be set to automatically delete relations to work order pools.</span></span>

7. <span data-ttu-id="dd9cc-120">ワーク オーダーをワーク オーダー プールにすぐに追加できます。</span><span class="sxs-lookup"><span data-stu-id="dd9cc-120">You can start adding work orders to your work order pool right away.</span></span> <span data-ttu-id="dd9cc-121">**ワーク オーダー** クイック タブの、**明細行の追加**をクリックします。</span><span class="sxs-lookup"><span data-stu-id="dd9cc-121">On the **Work orders** FastTab, click **Add line**.</span></span>

8. <span data-ttu-id="dd9cc-122">**ワーク オーダー** フィールドで、ワーク オーダーを選択します。</span><span class="sxs-lookup"><span data-stu-id="dd9cc-122">Select a work order in the **Work order** field.</span></span> <span data-ttu-id="dd9cc-123">関連フィールドは、自動的に更新されます。</span><span class="sxs-lookup"><span data-stu-id="dd9cc-123">The related fields are automatically updated.</span></span>

9. <span data-ttu-id="dd9cc-124">ワーク オーダーをさらに追加する場合は、手順 7-8 を繰り返します。</span><span class="sxs-lookup"><span data-stu-id="dd9cc-124">Repeat steps 7-8 if you want to add more work orders.</span></span>

10. <span data-ttu-id="dd9cc-125">**並べ替え順序**フィールドで、ワーク オーダーを特定の順序で実行するかどうかを指定できます。</span><span class="sxs-lookup"><span data-stu-id="dd9cc-125">In the **Sort order** field, you can indicate if the work orders should be carried out in a certain order.</span></span> <span data-ttu-id="dd9cc-126">1、2、3 などの番号を挿入して、選択したワーク オーダーの特定の順序を示します。</span><span class="sxs-lookup"><span data-stu-id="dd9cc-126">Insert numbers 1, 2, 3, and so on to indicate a specific sequence for the selected work orders.</span></span>

11. <span data-ttu-id="dd9cc-127">**ワーク オーダー** ボタンをクリックして、ワーク オーダー プールに含まれているすべてのワーク オーダーの一覧を表示します。</span><span class="sxs-lookup"><span data-stu-id="dd9cc-127">Click the **Work orders** button to see a list of all the work orders included in the work order pool.</span></span>

12. <span data-ttu-id="dd9cc-128">**最大能力負荷**ボタンをクリックして、**最大能力負荷**を開き、メンテナンス スケジュール、スケジュールされていないワーク オーダー、スケジュールされたワーク オーダーの最大能力負荷を計算して表示します。</span><span class="sxs-lookup"><span data-stu-id="dd9cc-128">Click the **Capacity load** button to open **Capacity load** to calculate and view capacity load for maintenance schedule, not-scheduled work orders, and scheduled work orders.</span></span>

13. <span data-ttu-id="dd9cc-129">**品目予測**ボタンをクリックして**品目予測**を開き、メンテナンス スケジュール、スケジュールされていないワーク オーダー、およびスケジュールされたワーク オーダーに関連する品目 (予備部品やその他の必要な品目) の予測を計算して表示します。</span><span class="sxs-lookup"><span data-stu-id="dd9cc-129">Click the **Item forecast** button to open **Item forecast** to calculate and view forecasts for items (spare parts and other required items) related to maintenance schedule, not-scheduled work orders, and scheduled work orders.</span></span>

14. <span data-ttu-id="dd9cc-130">**ワーク オーダー購買要求**ボタンをクリックして**ワーク オーダー購買要求**の一覧を開き、ワーク オーダー プールのワーク オーダーに関連する購買要求の一覧を表示します。</span><span class="sxs-lookup"><span data-stu-id="dd9cc-130">Click the **Work order purchase requisition** button to open the **Work order purchase requisition** list to see a list of purchase requisitions related to the work orders in the work order pool.</span></span>

15. <span data-ttu-id="dd9cc-131">**ワーク オーダー購買**ボタンをクリックして**ワーク オーダー購買**の一覧を開き、ワーク オーダー プールのワーク オーダーに関連する発注書の一覧を表示します。</span><span class="sxs-lookup"><span data-stu-id="dd9cc-131">Click the **Work order purchase** button to open the **Work order purchase** list to see a list of purchase orders related to the work orders in the work order pool.</span></span>

>[!NOTE]
><span data-ttu-id="dd9cc-132">作業計画がワーク オーダー プールに関連しなくなった場合は、**ワーク オーダー プール**のリスト ビューで、そのプールの**有効**チェック ボックスを、「いいえ」に設定します。</span><span class="sxs-lookup"><span data-stu-id="dd9cc-132">When a work order pool is no longer relevant for your work planning, set the **Active** check box for that pool to "No" in the **Work order pool** list view.</span></span>

<span data-ttu-id="dd9cc-133">たとえば、後で他のワーク オーダーに使用できる空のプールを作成するために、すべてのワーク オーダー明細行を削除する場合は、**ワーク オーダー リレーションの削除**のチェック ボックスをオンにします。</span><span class="sxs-lookup"><span data-stu-id="dd9cc-133">Select the **Delete work order relations** check box if you want to delete all work order lines, for example to create an empty pool that you can later use for other work orders.</span></span> <span data-ttu-id="dd9cc-134">ワーク オーダー プールを使用して、後で新しいワーク オーダー リレーションを作成する場合は、**ワーク オーダー リレーションの削除**チェック ボックスをオフにします。</span><span class="sxs-lookup"><span data-stu-id="dd9cc-134">Remember to clear the **Delete work order relations** check box if you want to use the work order pool to create new work order relations later.</span></span>


![図 1](media/22-work-orders.png)


## <a name="add-work-order-to-a-work-order-pool"></a><span data-ttu-id="dd9cc-136">ワーク オーダーをワーク オーダー プールに追加する</span><span class="sxs-lookup"><span data-stu-id="dd9cc-136">Add work order to a work order pool</span></span>

<span data-ttu-id="dd9cc-137">上のセクションで説明したように、ワーク オーダーは、プールを作成するときにワーク オーダー プールに追加できます。</span><span class="sxs-lookup"><span data-stu-id="dd9cc-137">As described in the section above, you can add work orders to a work order pool when you create the pool.</span></span> <span data-ttu-id="dd9cc-138">また、**すべてのワーク オーダー**のリストのいずれかから、ワーク オーダーをワーク オーダー プールに追加することもできます。</span><span class="sxs-lookup"><span data-stu-id="dd9cc-138">You can also add a work order to a work order pool from one of the **All work orders** list.</span></span>

1. <span data-ttu-id="dd9cc-139">**資産管理** > **共通** > **作業指示書** > **すべての作業指示書**または**有効な作業指示書**の順にクリックします。</span><span class="sxs-lookup"><span data-stu-id="dd9cc-139">Click **Asset management** > **Common** > **Work orders** > **All work orders** or **Active work orders**.</span></span>

2. <span data-ttu-id="dd9cc-140">リストからワーク オーダーを選択し、**ワーク オーダー プール**をクリックします。</span><span class="sxs-lookup"><span data-stu-id="dd9cc-140">Select the work order in the list, and click **Work order pool**.</span></span>

3. <span data-ttu-id="dd9cc-141">**追加/削除**フィールドで、「追加」を選択します。</span><span class="sxs-lookup"><span data-stu-id="dd9cc-141">Select "Add" in the **Add/remove** field.</span></span>

4. <span data-ttu-id="dd9cc-142">**プール** フィールドで、ワーク オーダー プールを選択します。</span><span class="sxs-lookup"><span data-stu-id="dd9cc-142">Select the work order pool in the **Pool** field.</span></span>

5. <span data-ttu-id="dd9cc-143">**OK**をクリックします。</span><span class="sxs-lookup"><span data-stu-id="dd9cc-143">Click **OK**.</span></span>

6. <span data-ttu-id="dd9cc-144">ワーク オーダーをワーク オーダー プールに追加した後、ワーク オーダーをプール内で特定の順序で配置する場合は、**編集**をクリックします。そして**ワーク オーダー プール** フォーム > **ワーク オーダー** クイック タブ > **並べ替え順序**のフィールドにあるプールに含まれているワークオーダーの並べ替え順序を調整します。</span><span class="sxs-lookup"><span data-stu-id="dd9cc-144">After you have added a work order to a work order pool, if you want to place the work order in a specific sequence in the pool: Open one of the work order pools list pages, select the pool and click **Edit**, and adjust the sort order of the work orders included in pool in the **Work order pool** form > **Work orders** FastTab > **Sort order** field.</span></span>

<span data-ttu-id="dd9cc-145">選択したワーク オーダーをワーク オーダー プールから削除する場合は、手順 3 で「削除」を選択します。</span><span class="sxs-lookup"><span data-stu-id="dd9cc-145">If you want to remove the selected work order from a work order pool, select "Remove" in step 3.</span></span>

