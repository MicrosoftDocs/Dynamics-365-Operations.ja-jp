---
title: 作業指示書プール
description: このトピックでは資産管理でワーク オーダー プールを操作する方法について説明します。
author: josaw1
manager: tfehr
ms.date: 10/15/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: EntAssetWorkOrderTablePoolPart, EntAssetWorkOrderPoolReferenceInfoPart, EntAssetWorkOrderPool, EntAssetWorkOrderPoolPreviewPart
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: mkirknel
ms.search.validFrom: 2019-09-30
ms.dyn365.ops.version: 10.0.5
ms.openlocfilehash: 3e95a4fdfaf4817867f3d2df7774df6a27ee6599
ms.sourcegitcommit: c986d5234b81d31cc6d054298be6f6ec92c1754c
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 09/25/2020
ms.locfileid: "3889508"
---
# <a name="work-order-pools"></a><span data-ttu-id="8a1e4-103">作業指示書プール</span><span class="sxs-lookup"><span data-stu-id="8a1e4-103">Work order pools</span></span>

[!include [banner](../../includes/banner.md)]


<span data-ttu-id="8a1e4-104">ワーク オーダー プールを使用して、共通点があるワーク オーダーをグループ化できます。</span><span class="sxs-lookup"><span data-stu-id="8a1e4-104">You can use work order pools to group work orders that have something in common.</span></span> <span data-ttu-id="8a1e4-105">ワーク オーダー プールを作成できる要素の例を以下に示します。</span><span class="sxs-lookup"><span data-stu-id="8a1e4-105">Here are some examples of things that you can create  work order pools for:</span></span>

- <span data-ttu-id="8a1e4-106">メンテナンス作業者 A またはメンテナンス作業者 B、などの作業者</span><span class="sxs-lookup"><span data-stu-id="8a1e4-106">Work crews, for example, Maintenance Crew A or Maintenance Crew B</span></span>  

- <span data-ttu-id="8a1e4-107">電気技師または配管工などの専門的なスキル</span><span class="sxs-lookup"><span data-stu-id="8a1e4-107">Professional skills, such as electricians or plumbers</span></span>  

- <span data-ttu-id="8a1e4-108">物理的場所</span><span class="sxs-lookup"><span data-stu-id="8a1e4-108">Physical locations</span></span>  

- <span data-ttu-id="8a1e4-109">週またはその他の期間などのタイム スケジュール</span><span class="sxs-lookup"><span data-stu-id="8a1e4-109">Time schedules, such as weeks or other periods</span></span>  

<span data-ttu-id="8a1e4-110">必要に応じて、1 つのワーク オーダーを複数のワーク オーダー プールに追加できます。</span><span class="sxs-lookup"><span data-stu-id="8a1e4-110">As you require, you can put one work order in multiple work order pools.</span></span>


## <a name="create-a-work-order-pool"></a><span data-ttu-id="8a1e4-111">ワーク オーダー プールの作成</span><span class="sxs-lookup"><span data-stu-id="8a1e4-111">Create a work order pool</span></span>

<span data-ttu-id="8a1e4-112">**すべてのワーク オーダー プール**または**有効なワーク オーダー プール** リスト ページでは、ワーク オーダー プールの概要を取得し、新しいプールを作成できます。</span><span class="sxs-lookup"><span data-stu-id="8a1e4-112">On the **All work order pools** or **Active work order pools** list page, you can get an overview of your work order pools and create new pools.</span></span>

1. <span data-ttu-id="8a1e4-113">**資産管理** > **共通** > **ワーク オーダー プール** > **すべてのワーク オーダー プール**または**有効なワーク オーダー プール**の順に選択します。</span><span class="sxs-lookup"><span data-stu-id="8a1e4-113">Select **Asset management** > **Common** > **Work order pools** > **All work order pools** or **Active work order pools**.</span></span>

2. <span data-ttu-id="8a1e4-114">**新規** を選択します。</span><span class="sxs-lookup"><span data-stu-id="8a1e4-114">Select **New**.</span></span>

3. <span data-ttu-id="8a1e4-115">**プール** フィールドに、ワーク オーダー プールの ID を入力します。</span><span class="sxs-lookup"><span data-stu-id="8a1e4-115">In the **Pool** field, enter an ID for the work order pool.</span></span>

4. <span data-ttu-id="8a1e4-116">**名前**フィールドに、名前を入力します。</span><span class="sxs-lookup"><span data-stu-id="8a1e4-116">the **Name** field, enter a name.</span></span>

5. <span data-ttu-id="8a1e4-117">**有効**オプションを**はい**に設定して、ワーク オーダー プールが有効であることを示します。</span><span class="sxs-lookup"><span data-stu-id="8a1e4-117">Set the **Active** option to **Yes** to indicate that the work order pool is active.</span></span>

6. <span data-ttu-id="8a1e4-118">ワーク オーダーをワーク オーダー プールから自動的に削除する場合は、**ワーク オーダー リレーションの削除**オプションを**はい**に設定します。</span><span class="sxs-lookup"><span data-stu-id="8a1e4-118">Set the **Delete work order relations** option to **Yes** if work orders should automatically be removed from the work order pool.</span></span>

7. <span data-ttu-id="8a1e4-119">**ライフサイクル状態の削除**フィールドで、ワーク オーダーのライフサイクル状態を選択します。</span><span class="sxs-lookup"><span data-stu-id="8a1e4-119">In the **Delete lifecycle state** field, select the work order lifecycle state.</span></span> <span data-ttu-id="8a1e4-120">たとえば、ワーク オーダーを完了するためのワーク オーダー ライフサイクル状態は、ワーク オーダー プールへのリレーションを自動的に削除するように設定できます。</span><span class="sxs-lookup"><span data-stu-id="8a1e4-120">For example, the work order lifecycle state for completing a work order could be set to automatically delete relations to work order pools.</span></span>

    <span data-ttu-id="8a1e4-121">ワーク オーダーをワーク オーダー プールにすぐに追加できます。</span><span class="sxs-lookup"><span data-stu-id="8a1e4-121">You can start adding work orders to your work order pool right away.</span></span>

8. <span data-ttu-id="8a1e4-122">**ワーク オーダー** クイック タブの、**明細行の追加**を選択します。</span><span class="sxs-lookup"><span data-stu-id="8a1e4-122">On the **Work orders** FastTab, select **Add line**.</span></span>

9. <span data-ttu-id="8a1e4-123">**ワーク オーダー** フィールドで、ワーク オーダーを選択します。</span><span class="sxs-lookup"><span data-stu-id="8a1e4-123">In the **Work order** field, select a work order.</span></span> <span data-ttu-id="8a1e4-124">関連フィールドは、自動的に更新されます。</span><span class="sxs-lookup"><span data-stu-id="8a1e4-124">The related fields are automatically updated.</span></span>

10. <span data-ttu-id="8a1e4-125">手順 8～9 を繰り返してワーク オーダーを追加します。</span><span class="sxs-lookup"><span data-stu-id="8a1e4-125">Repeat steps 8 through 9 to add more work orders.</span></span>

11. <span data-ttu-id="8a1e4-126">追加したワーク オーダーを特定の順序で実行する必要がある場合は、**並べ替え順序**フィールドで、**1**、**2**、**3** などの番号を入力して、順序を指定できます。</span><span class="sxs-lookup"><span data-stu-id="8a1e4-126">If the work orders that you added should be done in a specific order, in the **Sort order** field, you can enter the numbers **1**, **2**, **3**, and so on, to specify that order.</span></span>

12. <span data-ttu-id="8a1e4-127">ワーク オーダー プールに含まれるすべてのワーク オーダーの一覧を表示するには、**関連するワーク オーダー プールの表示**グループの、**ワーク オーダー プール** タブの、アクション ウィンドウで、**ワーク オーダー**を選択して、**すべてのワーク オーダー**一覧ページを開きます。</span><span class="sxs-lookup"><span data-stu-id="8a1e4-127">To view a list of all the work orders that are included in the work order pool, on the Action Pane, on the **Work order pool** tab, in the **View work order pool related** group, select **Work orders** to open the **All work orders** list page.</span></span>

13. <span data-ttu-id="8a1e4-128">メンテナンス スケジュール、スケジュールされていないワーク オーダーおよびスケジュールされたワーク オーダーの最大能力負荷を計算および表示するには、**関連するワーク オーダー プールの表示**グループの、**ワーク オーダー プール** タブの、アクション ウィンドウで、**最大能力負荷**を選択して、**最大能力負荷の計算**ダイアログを開きます。</span><span class="sxs-lookup"><span data-stu-id="8a1e4-128">To calculate and view capacity load for the maintenance schedule, unscheduled work orders, and scheduled work orders, on the Action Pane, on the **Work order pool** tab, in the **View work order pool related** group, select **Capacity load** to open the **Calculate capacity load** dialog.</span></span>

14. <span data-ttu-id="8a1e4-129">メンテナンス スケジュール、スケジュールされていないワーク オーダーおよびスケジュールされたワーク オーダーに関連する品目 (予備部品やその他必要な品目) の予測を計算および表示するには、**関連するワーク オーダー プールの表示**グループの、**ワーク オーダー プール** タブの、アクション ウィンドウで、**品目予測**を選択して、**品目予測の計算**ダイアログを開きます。</span><span class="sxs-lookup"><span data-stu-id="8a1e4-129">To calculate and view forecasts for items (spare parts and other required items) that are related to maintenance schedule, unscheduled work orders, and scheduled work orders, on the Action Pane, on the **Work order pool** tab, in the **View work order pool related** group, select **Item forecast** to open the **Calculate item forecast** dialog.</span></span>

15. <span data-ttu-id="8a1e4-130">ワーク オーダー プールのワーク オーダーに関連する購買要求の一覧を表示するには、**調達**グループの、**ワーク オーダー プール** タブの、アクション ウィンドウで、**ワーク オーダー購買要求**を選択して、**ワーク オーダー購買要求**一覧ページを開きます。</span><span class="sxs-lookup"><span data-stu-id="8a1e4-130">To view a list of purchase requisitions that are related to the work orders in the work order pool, on the Action Pane, on the **Work order pool** tab, in the **Procurement** group, select **Work order purchase requisition** to open the **Work order purchase requisition** list page.</span></span>

16. <span data-ttu-id="8a1e4-131">ワーク オーダー プールのワーク オーダーに関連する発注書の一覧を表示するには、**調達**グループの、**ワーク オーダー プール** タブの、アクション ウィンドウで、**ワーク オーダー購買**を選択して、**ワーク オーダー購買**一覧ページを開きます。</span><span class="sxs-lookup"><span data-stu-id="8a1e4-131">To view a list of purchase orders that are related to the work orders in the work order pool, on the Action Pane, on the **Work order pool** tab, in the **Procurement** group, select **Work order purchase** to open the **Work order purchase** list page.</span></span>

>[!NOTE]
><span data-ttu-id="8a1e4-132">作業計画がワーク オーダー プールに関連しなくなった場合は、**ワーク オーダー プール**ページのリスト ビューで、そのプールの**有効**オプションを、**いいえ**に設定します。</span><span class="sxs-lookup"><span data-stu-id="8a1e4-132">When a work order pool is no longer relevant to your work planning, set the **Active** option for that pool to **No** in the list view of the **Work order pool** page.</span></span>

<span data-ttu-id="8a1e4-133">すべてのワーク オーダー明細行を削除するには、**ワーク オーダー リレーションの削除**オプションを**はい**に設定します。</span><span class="sxs-lookup"><span data-stu-id="8a1e4-133">To delete all worker order lines, set the **Delete work order relations** option to **Yes**.</span></span> <span data-ttu-id="8a1e4-134">このオプションは、後で他のワーク オーダーに使用できる空のプールを作成する場合などに役立ちます。</span><span class="sxs-lookup"><span data-stu-id="8a1e4-134">This option is useful if, for example, you want to create an empty pool that you can use later for other work orders.</span></span> <span data-ttu-id="8a1e4-135">ワーク オーダー プールを使用して、後で新しいワーク オーダー リレーションを作成する場合は、**ワーク オーダー リレーションの削除**オプションを**いいえ**に設定する必要があります。</span><span class="sxs-lookup"><span data-stu-id="8a1e4-135">When you're ready to use the work order pool to create new work order relations later, remember to set the **Delete work order relations** option to **No**.</span></span>

<span data-ttu-id="8a1e4-136">次の図は、**ワーク オーダー プール**の一覧ページの例を示しています。</span><span class="sxs-lookup"><span data-stu-id="8a1e4-136">The illustration below shows an example of the **Work order pool** list page.</span></span>

![図 1](media/22-work-orders.png)


## <a name="add-a-work-order-to-a-work-order-pool"></a><span data-ttu-id="8a1e4-138">ワーク オーダーをワーク オーダー プールに追加する</span><span class="sxs-lookup"><span data-stu-id="8a1e4-138">Add a work order to a work order pool</span></span>

<span data-ttu-id="8a1e4-139">前のセクションで説明したように、プールを作成するときに、ワーク オーダーをワーク オーダー プールに追加できます。</span><span class="sxs-lookup"><span data-stu-id="8a1e4-139">As described in the previous section, you can add work orders to a work order pool when you create that pool.</span></span> <span data-ttu-id="8a1e4-140">**すべてのワーク オーダー**または**有効なワーク オーダー**一覧ページで、ワーク オーダーをワーク オーダー プールに追加することもできます。</span><span class="sxs-lookup"><span data-stu-id="8a1e4-140">You can also add work orders to a work order pool on the **All work orders** or **Active work orders** list page.</span></span>

1. <span data-ttu-id="8a1e4-141">ワーク オーダーを選択してから、アクション ウィンドウで**ワーク オーダー**タブ (**管理**グループ内) で、**ワーク オーダー プール**を選択します。</span><span class="sxs-lookup"><span data-stu-id="8a1e4-141">Select the work order, and then, on the Action Pane, on the **Work order** tab, in the **Maintain** group, select **Work order pool**.</span></span>

2. <span data-ttu-id="8a1e4-142">リストからワーク オーダーを選択し、**ワーク オーダー プール**をクリックします。</span><span class="sxs-lookup"><span data-stu-id="8a1e4-142">Select the work order in the list, and click **Work order pool**.</span></span>

3. <span data-ttu-id="8a1e4-143">**ワーク オーダー プールの管理**ダイアログの、**追加/削除**フィールドで、**追加**を選択します。</span><span class="sxs-lookup"><span data-stu-id="8a1e4-143">In the **Maintain work order pool** dialog, in the **Add/remove** field, select **Add**.</span></span>

4. <span data-ttu-id="8a1e4-144">**プール** フィールドで、ワーク オーダー プールを選択します。</span><span class="sxs-lookup"><span data-stu-id="8a1e4-144">In the **Pool** field, select the work order pool.</span></span>

5. <span data-ttu-id="8a1e4-145">**OK** を選択します。</span><span class="sxs-lookup"><span data-stu-id="8a1e4-145">Select **OK**.</span></span>

6. <span data-ttu-id="8a1e4-146">ワーク オーダー プールに特定の順序で追加したワーク オーダーを追加するには、**すべてのワーク オーダー プール**または**有効なワーク オーダー プール**一覧ページで、そのプールを選択してから**編集**を選択します。</span><span class="sxs-lookup"><span data-stu-id="8a1e4-146">To put the work order that you added in a specific order in the work order pool, on the **All work order pools** or **Active work order pools** list page, select the pool, and then select **Edit**.</span></span> <span data-ttu-id="8a1e4-147">その後、**ワーク オーダー** クイック タブの**ワーク オーダー プール** ページで、**並べ替え順序**フィールドを試用して、プールに含まれるワーク オーダーの並べ替え順序を調整します。</span><span class="sxs-lookup"><span data-stu-id="8a1e4-147">Then, on the **Work order pool** page, on the **Work orders** FastTab, use the **Sort order** field to adjust the sort order of the work orders that are included in pool.</span></span>

<span data-ttu-id="8a1e4-148">ワーク オーダーをワーク オーダー プールから削除する場合は、これらの手順を繰り返して、手順 3 で**削除**を選択します。</span><span class="sxs-lookup"><span data-stu-id="8a1e4-148">To remove a work order from a work order pool, repeat these steps, but select **Remove** in step 3.</span></span>

