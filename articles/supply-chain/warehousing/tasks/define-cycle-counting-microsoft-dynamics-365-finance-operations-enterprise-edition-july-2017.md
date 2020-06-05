---
title: 循環棚卸の定義
description: 循環棚卸は、手持在庫品目を監査するために使用できる倉庫プロセスです。
author: MarkusFogelberg
manager: tfehr
ms.date: 08/12/2019
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Operations
ms.search.region: Global
ms.author: mafoge
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 1503ef3646657a4b7bb7e240144af2ac559a62d0
ms.sourcegitcommit: 8a2127c5af6cdbda30ccc1f9bef9bd4ab61e9e50
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 05/18/2020
ms.locfileid: "3383024"
---
# <a name="define-cycle-counting"></a><span data-ttu-id="ae7b1-103">循環棚卸の定義</span><span class="sxs-lookup"><span data-stu-id="ae7b1-103">Define cycle counting</span></span> 

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="ae7b1-104">循環棚卸は、手持在庫品目を監査するために使用できる倉庫プロセスです。</span><span class="sxs-lookup"><span data-stu-id="ae7b1-104">Cycle counting is a warehouse process that you can use to audit on-hand inventory items.</span></span> <span data-ttu-id="ae7b1-105">このタスク記録では、次の作業を実施する方法を説明します。棚卸作業の既定の優先順位を設定する。モバイル デバイス メニュー項目でピッキングと棚卸の両方の工程を処理できるようにする。場所が空になったときに棚卸のしきい値をトリガーできるようにする。および特定の倉庫にある特定の品目の循環棚卸計画を有効にする。</span><span class="sxs-lookup"><span data-stu-id="ae7b1-105">This task recording shows how to set up the default counting work priority, enable a mobile device menu item to process both picking and counting operations, enable a counting threshold trigger when a location becomes empty, and enable a cycle counting plan for a specific item in a specific warehouse.</span></span> <span data-ttu-id="ae7b1-106">通常、これらのタスクは、倉庫マネージャーが実行します。</span><span class="sxs-lookup"><span data-stu-id="ae7b1-106">Typically, these tasks are performed by a warehouse manager.</span></span> <span data-ttu-id="ae7b1-107">USMF デモ データ会社または独自のデータを使用して、この手順を踏むことができます。</span><span class="sxs-lookup"><span data-stu-id="ae7b1-107">You can go through this procedure in the USMF demo data company or in your own data.</span></span>


## <a name="set-the-priority-of-counting-work"></a><span data-ttu-id="ae7b1-108">棚卸作業の優先順位を設定する</span><span class="sxs-lookup"><span data-stu-id="ae7b1-108">Set the priority of counting work</span></span>
1. <span data-ttu-id="ae7b1-109">**ナビゲーション ウィンドウ**で、**モジュール > 倉庫管理 > 設定 > 倉庫管理パラメーター**の順に移動します。</span><span class="sxs-lookup"><span data-stu-id="ae7b1-109">In the **Navigation pane**, go to **Modules > Warehouse management > Setup > Warehouse management parameters**.</span></span>
2. <span data-ttu-id="ae7b1-110">**循環棚卸**タブをクリックします。</span><span class="sxs-lookup"><span data-stu-id="ae7b1-110">Click the **Cycle counting** tab.</span></span>
3. <span data-ttu-id="ae7b1-111">**既定の循環棚卸作業優先順位**フィールドで、数値を入力します。</span><span class="sxs-lookup"><span data-stu-id="ae7b1-111">In the **Default cycle count work priority** field, enter a number.</span></span> <span data-ttu-id="ae7b1-112">この手順では、倉庫内での他の種類の作業と比較して、循環棚卸作業の優先順位を変更します。</span><span class="sxs-lookup"><span data-stu-id="ae7b1-112">This step changes the priority of cycle counting work compared to other types of work in the warehouse.</span></span> <span data-ttu-id="ae7b1-113">他の種類の作業よりも小さい番号を入力すると、循環棚卸作業の優先順位が上がります。</span><span class="sxs-lookup"><span data-stu-id="ae7b1-113">By entering a number that is lower than the number for other types of work, you raise the priority of the cycle counting work.</span></span>  
4. <span data-ttu-id="ae7b1-114">**保存**をクリックします。</span><span class="sxs-lookup"><span data-stu-id="ae7b1-114">Click **Save**.</span></span>
5. <span data-ttu-id="ae7b1-115">ページを閉じます。</span><span class="sxs-lookup"><span data-stu-id="ae7b1-115">Close the page.</span></span>

## <a name="enable-the-mobile-device"></a><span data-ttu-id="ae7b1-116">モバイル デバイスを有効にする</span><span class="sxs-lookup"><span data-stu-id="ae7b1-116">Enable the mobile device</span></span>
1. <span data-ttu-id="ae7b1-117">**ナビゲーション ウィンドウ**で、**モジュール > 倉庫管理 > 設定 > モバイル デバイス > モバイル デバイスのメニュー品目**の順に移動します。</span><span class="sxs-lookup"><span data-stu-id="ae7b1-117">In the **Navigation pane**, go to **Modules > Warehouse management > Setup > Mobile device > Mobile device menu items**.</span></span>
2. <span data-ttu-id="ae7b1-118">**新規** をクリックします。</span><span class="sxs-lookup"><span data-stu-id="ae7b1-118">Click **New**.</span></span>
3. <span data-ttu-id="ae7b1-119">**メニュー項目名**フィールドで、値を入力します。</span><span class="sxs-lookup"><span data-stu-id="ae7b1-119">In the **Menu item name** field, type a value.</span></span>
4. <span data-ttu-id="ae7b1-120">**タイトル** フィールドに値を入力します。</span><span class="sxs-lookup"><span data-stu-id="ae7b1-120">In the **Title** field, type a value.</span></span>
5. <span data-ttu-id="ae7b1-121">**モード** フィールドで '作業' を選択します。</span><span class="sxs-lookup"><span data-stu-id="ae7b1-121">In the **Mode** field, select 'Work'.</span></span>
6. <span data-ttu-id="ae7b1-122">**既存の作業を使用**オプションをはいに設定します。</span><span class="sxs-lookup"><span data-stu-id="ae7b1-122">Set the **Use existing work** option to Yes.</span></span> <span data-ttu-id="ae7b1-123">このオプション [はい] に設定する場合、モバイル デバイスのメニュー項目を使用すると、システムは既存の作業を検索します。</span><span class="sxs-lookup"><span data-stu-id="ae7b1-123">When you set this option to Yes, the system will look for existing work when the mobile device menu item is used.</span></span>  
7. <span data-ttu-id="ae7b1-124">**指示者**フィールドで 'システム主導' を選択します。</span><span class="sxs-lookup"><span data-stu-id="ae7b1-124">In the **Directed by** field, select 'System directed'.</span></span> <span data-ttu-id="ae7b1-125">「システム主導」が選択される場合、定義された作業クラスにある作業を開くため、倉庫作業員が指示されます。</span><span class="sxs-lookup"><span data-stu-id="ae7b1-125">When "System directed" is selected, the warehouse worker will be directed to open work that is in defined work classes.</span></span> <span data-ttu-id="ae7b1-126">(次にこれらの作業クラスを作成します。)</span><span class="sxs-lookup"><span data-stu-id="ae7b1-126">(We will create these work classes next.)</span></span>  
8. <span data-ttu-id="ae7b1-127">**作業クラス** クイック タブを展開します。</span><span class="sxs-lookup"><span data-stu-id="ae7b1-127">Expand the **Work classes** fastTab.</span></span> <span data-ttu-id="ae7b1-128">次に、このモバイル デバイスのメニュー項目で使用する 2 個の作業クラスを作成します。</span><span class="sxs-lookup"><span data-stu-id="ae7b1-128">Next, we will create two work classes that will be used with this mobile device menu item.</span></span> <span data-ttu-id="ae7b1-129">このメニュー項目が使用されると、これらの作業クラスが照会されて、最も優先順位の高い作業がユーザーに表示されることになります。</span><span class="sxs-lookup"><span data-stu-id="ae7b1-129">When the menu item is used, these work classes will be queried, and the work that has the highest priority will be shown to the user.</span></span>  
9. <span data-ttu-id="ae7b1-130">**新規** をクリックします。</span><span class="sxs-lookup"><span data-stu-id="ae7b1-130">Click **New**.</span></span>
10. <span data-ttu-id="ae7b1-131">**作業クラス ID** フィールドで、値を選択します。</span><span class="sxs-lookup"><span data-stu-id="ae7b1-131">In the**Work class ID** field, select a value.</span></span>
11. <span data-ttu-id="ae7b1-132">**新規** をクリックします。</span><span class="sxs-lookup"><span data-stu-id="ae7b1-132">Click **New**.</span></span>
12. <span data-ttu-id="ae7b1-133">**作業クラス ID** フィールドで、値を選択します。</span><span class="sxs-lookup"><span data-stu-id="ae7b1-133">In the **Work class ID** field, select a value.</span></span>
13. <span data-ttu-id="ae7b1-134">**アクション ウィンドウ**で、**保存** をクリックします。</span><span class="sxs-lookup"><span data-stu-id="ae7b1-134">In the **Action Pane**, click **Save**.</span></span>
14. <span data-ttu-id="ae7b1-135">ページを閉じます。</span><span class="sxs-lookup"><span data-stu-id="ae7b1-135">Close the page.</span></span>
15. <span data-ttu-id="ae7b1-136">**ナビゲーション ウィンドウ**で、**モジュール > 倉庫管理 > 設定 > モバイル デバイス > モバイル デバイスのメニュー**の順に移動します。</span><span class="sxs-lookup"><span data-stu-id="ae7b1-136">In the **Navigation pane**, go to **Modules > Warehouse management > Setup > Mobile device > Mobile device menu**.</span></span>
16. <span data-ttu-id="ae7b1-137">一覧で、目的のレコードを見つけ、選択します。</span><span class="sxs-lookup"><span data-stu-id="ae7b1-137">In the list, find and select the desired record.</span></span>
17. <span data-ttu-id="ae7b1-138">ツリーで、「作成したメニュー項目」を選択します。</span><span class="sxs-lookup"><span data-stu-id="ae7b1-138">In the tree, select 'the menu item that you just created'.</span></span>
18. <span data-ttu-id="ae7b1-139">**編集** をクリックします。</span><span class="sxs-lookup"><span data-stu-id="ae7b1-139">Click **Edit**.</span></span>
19. <span data-ttu-id="ae7b1-140">矢印をクリックしてメニュー項目をメニューに追加します。</span><span class="sxs-lookup"><span data-stu-id="ae7b1-140">Click the arrow to add the menu item to the menu.</span></span>
20. <span data-ttu-id="ae7b1-141">**保存**をクリックします。</span><span class="sxs-lookup"><span data-stu-id="ae7b1-141">Click **Save**.</span></span>

## <a name="create-a-counting-threshold"></a><span data-ttu-id="ae7b1-142">棚卸のしきい値を作成する</span><span class="sxs-lookup"><span data-stu-id="ae7b1-142">Create a counting threshold</span></span>
1. <span data-ttu-id="ae7b1-143">**ナビゲーション ウィンドウ**で、**モジュール > 倉庫管理 > 設定 > 循環棚卸 > 循環棚卸のしきい値**の順に移動します。</span><span class="sxs-lookup"><span data-stu-id="ae7b1-143">In the **Navigation pane**, go to **Modules > Warehouse management > Setup > Cycle counting > Cycle count thresholds**.</span></span>
2. <span data-ttu-id="ae7b1-144">**新規** をクリックします。</span><span class="sxs-lookup"><span data-stu-id="ae7b1-144">Click **New**.</span></span>
3. <span data-ttu-id="ae7b1-145">**循環棚卸のしきい値 ID** フィールドに、値を入力します。</span><span class="sxs-lookup"><span data-stu-id="ae7b1-145">In the **Cycle counting threshold ID** field, type a value.</span></span>
4. <span data-ttu-id="ae7b1-146">**循環棚卸をすぐに処理する**オプションをはいに設定します。</span><span class="sxs-lookup"><span data-stu-id="ae7b1-146">Set the **Process cycle counting immediately** option to Yes.</span></span>
5. <span data-ttu-id="ae7b1-147">**説明**フィールドで、値を入力します。</span><span class="sxs-lookup"><span data-stu-id="ae7b1-147">In the **Description** field, type a value.</span></span>
6. <span data-ttu-id="ae7b1-148">**保存**をクリックします。</span><span class="sxs-lookup"><span data-stu-id="ae7b1-148">Click **Save**.</span></span>
7. <span data-ttu-id="ae7b1-149">**場所の選択**をクリックします。</span><span class="sxs-lookup"><span data-stu-id="ae7b1-149">Click **Select locations**.</span></span>
8. <span data-ttu-id="ae7b1-150">一覧で、選択された行をマークします。</span><span class="sxs-lookup"><span data-stu-id="ae7b1-150">In the list, mark the selected row.</span></span>
9. <span data-ttu-id="ae7b1-151">**基準**フィールドで値を選択します。</span><span class="sxs-lookup"><span data-stu-id="ae7b1-151">In the **Criteria** field, select a value.</span></span>
10. <span data-ttu-id="ae7b1-152">**OK**をクリックします。</span><span class="sxs-lookup"><span data-stu-id="ae7b1-152">Click **OK**.</span></span>
11. <span data-ttu-id="ae7b1-153">ページを閉じます。</span><span class="sxs-lookup"><span data-stu-id="ae7b1-153">Close the page.</span></span>

## <a name="create-a-cycle-count-plan"></a><span data-ttu-id="ae7b1-154">循環棚卸計画を作成する</span><span class="sxs-lookup"><span data-stu-id="ae7b1-154">Create a cycle count plan</span></span>
1. <span data-ttu-id="ae7b1-155">**ナビゲーション ウィンドウ**で、**モジュール > 倉庫管理 > 設定 > 循環棚卸 > 循環棚卸計画**の順に移動します。</span><span class="sxs-lookup"><span data-stu-id="ae7b1-155">In the **Navigation pane**, go to **Modules > Warehouse management > Setup > Cycle counting > Cycle count plans**.</span></span>
2. <span data-ttu-id="ae7b1-156">**新規** をクリックします。</span><span class="sxs-lookup"><span data-stu-id="ae7b1-156">Click **New**.</span></span>
3. <span data-ttu-id="ae7b1-157">**循環棚卸計画 ID** フィールドに値を入力します。</span><span class="sxs-lookup"><span data-stu-id="ae7b1-157">In the **Cycle counting plan ID** field, type a value.</span></span>
4. <span data-ttu-id="ae7b1-158">**説明**フィールドで、値を入力します。</span><span class="sxs-lookup"><span data-stu-id="ae7b1-158">In the **Description** field, type a value.</span></span>
5. <span data-ttu-id="ae7b1-159">**循環棚卸の最大数**フィールドに、数値を入力します。</span><span class="sxs-lookup"><span data-stu-id="ae7b1-159">In the **Maximum number of cycle counts** field, enter a number.</span></span>
6. <span data-ttu-id="ae7b1-160">**保存**をクリックします。</span><span class="sxs-lookup"><span data-stu-id="ae7b1-160">Click **Save**.</span></span>
7. <span data-ttu-id="ae7b1-161">**場所の選択**をクリックします。</span><span class="sxs-lookup"><span data-stu-id="ae7b1-161">Click **Select locations**.</span></span>
8. <span data-ttu-id="ae7b1-162">一覧で、選択された行をマークします。</span><span class="sxs-lookup"><span data-stu-id="ae7b1-162">In the list, mark the selected row.</span></span>
9. <span data-ttu-id="ae7b1-163">**基準**フィールドで値を選択します。</span><span class="sxs-lookup"><span data-stu-id="ae7b1-163">In the **Criteria** field, select a value.</span></span>
10. <span data-ttu-id="ae7b1-164">**OK**をクリックします。</span><span class="sxs-lookup"><span data-stu-id="ae7b1-164">Click **OK**.</span></span>
11. <span data-ttu-id="ae7b1-165">**次回の循環棚卸までの日数**フィールドに、数値を入力します。</span><span class="sxs-lookup"><span data-stu-id="ae7b1-165">In the **Days between cycle counting** field, enter a number.</span></span> <span data-ttu-id="ae7b1-166">たとえば、**次回の循環棚卸までの日数**フィールドを 5 に設定すると、循環棚卸作業は 5 日ごとに作成されます。</span><span class="sxs-lookup"><span data-stu-id="ae7b1-166">For example, if the **Days between cycle counting** field is set to 5, cycle counting work will be created every five days.</span></span> <span data-ttu-id="ae7b1-167">ただし、循環棚卸作業が 3 日目に処理される場合は、次の循環棚卸作業は、最後の循環棚卸処理の 5 日後の 8 日目に作成されます。</span><span class="sxs-lookup"><span data-stu-id="ae7b1-167">However, if cycle counting work is processed on day three, the next cycle counting work will be created five days after the last cycle counting was processed, on day 8.</span></span>  
12. <span data-ttu-id="ae7b1-168">**保存**をクリックします。</span><span class="sxs-lookup"><span data-stu-id="ae7b1-168">Click **Save**.</span></span>
13. <span data-ttu-id="ae7b1-169">**新規** をクリックします。</span><span class="sxs-lookup"><span data-stu-id="ae7b1-169">Click **New**.</span></span>
14. <span data-ttu-id="ae7b1-170">**順序番号**フィールドに番号を入力します。</span><span class="sxs-lookup"><span data-stu-id="ae7b1-170">In the **Sequence number** field, enter a number.</span></span> <span data-ttu-id="ae7b1-171">並べ替えは、最小番号から最大番号です。</span><span class="sxs-lookup"><span data-stu-id="ae7b1-171">The sort is from the smallest number to the largest number.</span></span> <span data-ttu-id="ae7b1-172">値は 0 (ゼロ) より大きい値に設定する必要があります。</span><span class="sxs-lookup"><span data-stu-id="ae7b1-172">The value must be more than 0 (zero).</span></span>  
15. <span data-ttu-id="ae7b1-173">一覧で、選択された行をマークします。</span><span class="sxs-lookup"><span data-stu-id="ae7b1-173">In the list, mark the selected row.</span></span>
16. <span data-ttu-id="ae7b1-174">**説明**フィールドで、値を入力します。</span><span class="sxs-lookup"><span data-stu-id="ae7b1-174">In the **Description** field, type a value.</span></span>
17. <span data-ttu-id="ae7b1-175">**保存**をクリックします。</span><span class="sxs-lookup"><span data-stu-id="ae7b1-175">Click **Save**.</span></span>
18. <span data-ttu-id="ae7b1-176">**製品の定義**クエリをクリックします。</span><span class="sxs-lookup"><span data-stu-id="ae7b1-176">Click **Define product** query.</span></span>
19. <span data-ttu-id="ae7b1-177">一覧で、選択された行をマークします。</span><span class="sxs-lookup"><span data-stu-id="ae7b1-177">In the list, mark the selected row.</span></span>
20. <span data-ttu-id="ae7b1-178">**基準**フィールドで、値を入力または選択します。</span><span class="sxs-lookup"><span data-stu-id="ae7b1-178">In the **Criteria** field, enter or select a value.</span></span>
21. <span data-ttu-id="ae7b1-179">**OK**をクリックします。</span><span class="sxs-lookup"><span data-stu-id="ae7b1-179">Click **OK**.</span></span>
22. <span data-ttu-id="ae7b1-180">ページを閉じます。</span><span class="sxs-lookup"><span data-stu-id="ae7b1-180">Close the page.</span></span>

