---
title: 循環棚卸の定義
description: 循環棚卸は、手持在庫品目を監査するために使用できる倉庫プロセスです。
author: MarkusFogelberg
manager: AnnBe
ms.date: 06/23/2017
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User
ms.reviewer: josaw
ms.search.scope: Operations
ms.search.region: Global
ms.author: mafoge
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 2832547f81b0153d42ac4664184f18bd66f1acdd
ms.sourcegitcommit: 0f530e5f72a40f383868957a6b5cb0e446e4c795
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 01/29/2019
ms.locfileid: "337305"
---
# <a name="define-cycle-counting"></a><span data-ttu-id="84b23-103">循環棚卸の定義</span><span class="sxs-lookup"><span data-stu-id="84b23-103">Define cycle counting</span></span> 

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="84b23-104">循環棚卸は、手持在庫品目を監査するために使用できる倉庫プロセスです。</span><span class="sxs-lookup"><span data-stu-id="84b23-104">Cycle counting is a warehouse process that you can use to audit on-hand inventory items.</span></span> <span data-ttu-id="84b23-105">このタスク記録では、次の作業を実施する方法を説明します。棚卸作業の既定の優先順位を設定する。モバイル デバイス メニュー項目でピッキングと棚卸の両方の工程を処理できるようにする。場所が空になったときに棚卸のしきい値をトリガーできるようにする。および特定の倉庫にある特定の品目の循環棚卸計画を有効にする。</span><span class="sxs-lookup"><span data-stu-id="84b23-105">This task recording shows how to set up the default counting work priority, enable a mobile device menu item to process both picking and counting operations, enable a counting threshold trigger when a location becomes empty, and enable a cycle counting plan for a specific item in a specific warehouse.</span></span> <span data-ttu-id="84b23-106">通常、これらのタスクは、倉庫マネージャーが実行します。</span><span class="sxs-lookup"><span data-stu-id="84b23-106">Typically, these tasks are performed by a warehouse manager.</span></span> <span data-ttu-id="84b23-107">USMF デモ データ会社または独自のデータを使用して、この手順を踏むことができます。</span><span class="sxs-lookup"><span data-stu-id="84b23-107">You can go through this procedure in the USMF demo data company or in your own data.</span></span>


## <a name="set-the-priority-of-counting-work"></a><span data-ttu-id="84b23-108">棚卸作業の優先順位を設定する</span><span class="sxs-lookup"><span data-stu-id="84b23-108">Set the priority of counting work</span></span>
1. <span data-ttu-id="84b23-109">[倉庫管理] > [設定] > [倉庫管理パラメーター] の順に移動します。</span><span class="sxs-lookup"><span data-stu-id="84b23-109">Go to Warehouse management > Setup > Warehouse management parameters.</span></span>
2. <span data-ttu-id="84b23-110">[循環棚卸] タブをクリックします。</span><span class="sxs-lookup"><span data-stu-id="84b23-110">Click the Cycle counting tab.</span></span>
3. <span data-ttu-id="84b23-111">[既定の循環棚卸作業優先順位] フィールドで、数値を入力します。</span><span class="sxs-lookup"><span data-stu-id="84b23-111">In the Default cycle count work priority field, enter a number.</span></span>
    * <span data-ttu-id="84b23-112">この手順では、倉庫内での他の種類の作業と比較して、循環棚卸作業の優先順位を変更します。</span><span class="sxs-lookup"><span data-stu-id="84b23-112">This step changes the priority of cycle counting work compared to other types of work in the warehouse.</span></span> <span data-ttu-id="84b23-113">他の種類の作業よりも小さい番号を入力すると、循環棚卸作業の優先順位が上がります。</span><span class="sxs-lookup"><span data-stu-id="84b23-113">By entering a number that is lower than the number for other types of work, you raise the priority of the cycle counting work.</span></span>  
4. <span data-ttu-id="84b23-114">[保存] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="84b23-114">Click Save.</span></span>
5. <span data-ttu-id="84b23-115">ページを閉じます。</span><span class="sxs-lookup"><span data-stu-id="84b23-115">Close the page.</span></span>

## <a name="enable-the-mobile-device"></a><span data-ttu-id="84b23-116">モバイル デバイスを有効にする</span><span class="sxs-lookup"><span data-stu-id="84b23-116">Enable the mobile device</span></span>
1. <span data-ttu-id="84b23-117">[倉庫管理] > [設定] > [モバイル デバイス] > [モバイル デバイスのメニュー品目] の順に移動します。</span><span class="sxs-lookup"><span data-stu-id="84b23-117">Go to Warehouse management > Setup > Mobile device > Mobile device menu items.</span></span>
2. <span data-ttu-id="84b23-118">[新規] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="84b23-118">Click New.</span></span>
3. <span data-ttu-id="84b23-119">[メニュー項目名] フィールドで、値を入力します。</span><span class="sxs-lookup"><span data-stu-id="84b23-119">In the Menu item name field, type a value.</span></span>
4. <span data-ttu-id="84b23-120">[タイトル] フィールドに値を入力します。</span><span class="sxs-lookup"><span data-stu-id="84b23-120">In the Title field, type a value.</span></span>
5. <span data-ttu-id="84b23-121">[モード] フィールドで [作業] を選択します。</span><span class="sxs-lookup"><span data-stu-id="84b23-121">In the Mode field, select 'Work'.</span></span>
6. <span data-ttu-id="84b23-122">[既存の作業を使用] オプションを [はい] に設定します。</span><span class="sxs-lookup"><span data-stu-id="84b23-122">Set the Use existing work option to Yes.</span></span>
    * <span data-ttu-id="84b23-123">このオプション [はい] に設定する場合、モバイル デバイスのメニュー項目を使用すると、システムは既存の作業を検索します。</span><span class="sxs-lookup"><span data-stu-id="84b23-123">When you set this option to Yes, the system will look for existing work when the mobile device menu item is used.</span></span>  
7. <span data-ttu-id="84b23-124">[指示者] フィールドで [システム主導] を選択します。</span><span class="sxs-lookup"><span data-stu-id="84b23-124">In the Directed by field, select 'System directed'.</span></span>
    * <span data-ttu-id="84b23-125">「システム主導」が選択される場合、定義された作業クラスにある作業を開くため、倉庫作業員が指示されます。</span><span class="sxs-lookup"><span data-stu-id="84b23-125">When "System directed" is selected, the warehouse worker will be directed to open work that is in defined work classes.</span></span> <span data-ttu-id="84b23-126">(次にこれらの作業クラスを作成します。)</span><span class="sxs-lookup"><span data-stu-id="84b23-126">(We will create these work classes next.)</span></span>  
8. <span data-ttu-id="84b23-127">[作業クラス] セクションを展開または折りたたみます。</span><span class="sxs-lookup"><span data-stu-id="84b23-127">Expand or collapse the Work classes section.</span></span>
    * <span data-ttu-id="84b23-128">次に、このモバイル デバイスのメニュー項目で使用する 2 個の作業クラスを作成します。</span><span class="sxs-lookup"><span data-stu-id="84b23-128">Next, we will create two work classes that will be used with this mobile device menu item.</span></span> <span data-ttu-id="84b23-129">このメニュー項目が使用されると、これらの作業クラスが照会されて、最も優先順位の高い作業がユーザーに表示されることになります。</span><span class="sxs-lookup"><span data-stu-id="84b23-129">When the menu item is used, these work classes will be queried, and the work that has the highest priority will be shown to the user.</span></span>  
9. <span data-ttu-id="84b23-130">[新規] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="84b23-130">Click New.</span></span>
10. <span data-ttu-id="84b23-131">[作業クラス ID] フィールドで値を選択します。</span><span class="sxs-lookup"><span data-stu-id="84b23-131">In the Work class ID field, select a value.</span></span>
11. <span data-ttu-id="84b23-132">[新規] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="84b23-132">Click New.</span></span>
12. <span data-ttu-id="84b23-133">[作業クラス ID] フィールドで値を選択します。</span><span class="sxs-lookup"><span data-stu-id="84b23-133">In the Work class ID field, select a value.</span></span>
13. <span data-ttu-id="84b23-134">[保存] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="84b23-134">Click Save.</span></span>
14. <span data-ttu-id="84b23-135">ページを閉じます。</span><span class="sxs-lookup"><span data-stu-id="84b23-135">Close the page.</span></span>
15. <span data-ttu-id="84b23-136">[倉庫管理] > [設定] > [モバイル デバイス] > [モバイル デバイスのメニュー] の順に移動します。</span><span class="sxs-lookup"><span data-stu-id="84b23-136">Go to Warehouse management > Setup > Mobile device > Mobile device menu.</span></span>
16. <span data-ttu-id="84b23-137">一覧で、目的のレコードを見つけ、選択します。</span><span class="sxs-lookup"><span data-stu-id="84b23-137">In the list, find and select the desired record.</span></span>
17. <span data-ttu-id="84b23-138">ツリーで、「作成したメニュー項目」を選択します。</span><span class="sxs-lookup"><span data-stu-id="84b23-138">In the tree, select 'the menu item that you just created'.</span></span>
18. <span data-ttu-id="84b23-139">[編集] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="84b23-139">Click Edit.</span></span>
19. <span data-ttu-id="84b23-140">矢印をクリックしてメニュー項目をメニューに追加します。</span><span class="sxs-lookup"><span data-stu-id="84b23-140">Click the arrow to add the menu item to the menu.</span></span>
20. <span data-ttu-id="84b23-141">[保存] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="84b23-141">Click Save.</span></span>

## <a name="create-a-counting-threshold"></a><span data-ttu-id="84b23-142">棚卸のしきい値を作成する</span><span class="sxs-lookup"><span data-stu-id="84b23-142">Create a counting threshold</span></span>
1. <span data-ttu-id="84b23-143">[倉庫管理] > [設定] > [循環棚卸] > [循環棚卸のしきい値] の順に移動します。</span><span class="sxs-lookup"><span data-stu-id="84b23-143">Go to Warehouse management > Setup > Cycle counting > Cycle count thresholds.</span></span>
2. <span data-ttu-id="84b23-144">[新規] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="84b23-144">Click New.</span></span>
3. <span data-ttu-id="84b23-145">[循環棚卸のしきい値 ID] フィールドに値を入力します。</span><span class="sxs-lookup"><span data-stu-id="84b23-145">In the Cycle counting threshold ID field, type a value.</span></span>
4. <span data-ttu-id="84b23-146">[循環棚卸をすぐに処理する] オプションを [はい] に設定します。</span><span class="sxs-lookup"><span data-stu-id="84b23-146">Set the Process cycle counting immediately option to Yes.</span></span>
5. <span data-ttu-id="84b23-147">[説明] フィールドに値を入力します。</span><span class="sxs-lookup"><span data-stu-id="84b23-147">In the Description field, type a value.</span></span>
6. <span data-ttu-id="84b23-148">[保存] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="84b23-148">Click Save.</span></span>
7. <span data-ttu-id="84b23-149">[場所の選択] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="84b23-149">Click Select locations.</span></span>
8. <span data-ttu-id="84b23-150">一覧で、選択された行をマークします。</span><span class="sxs-lookup"><span data-stu-id="84b23-150">In the list, mark the selected row.</span></span>
9. <span data-ttu-id="84b23-151">[基準] フィールドで値を選択します。</span><span class="sxs-lookup"><span data-stu-id="84b23-151">In the Criteria field, select a value.</span></span>
10. <span data-ttu-id="84b23-152">[OK] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="84b23-152">Click OK.</span></span>
11. <span data-ttu-id="84b23-153">ページを閉じます。</span><span class="sxs-lookup"><span data-stu-id="84b23-153">Close the page.</span></span>

## <a name="create-a-cycle-count-plan"></a><span data-ttu-id="84b23-154">循環棚卸計画を作成する</span><span class="sxs-lookup"><span data-stu-id="84b23-154">Create a cycle count plan</span></span>
1. <span data-ttu-id="84b23-155">[倉庫管理] > [設定] > [循環棚卸] > [循環棚卸計画] の順に移動します。</span><span class="sxs-lookup"><span data-stu-id="84b23-155">Go to Warehouse management > Setup > Cycle counting > Cycle count plans.</span></span>
2. <span data-ttu-id="84b23-156">[新規] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="84b23-156">Click New.</span></span>
3. <span data-ttu-id="84b23-157">[循環棚卸計画 ID] フィールドに値を入力します。</span><span class="sxs-lookup"><span data-stu-id="84b23-157">In the Cycle counting plan ID field, type a value.</span></span>
4. <span data-ttu-id="84b23-158">[説明] フィールドで値を入力します。</span><span class="sxs-lookup"><span data-stu-id="84b23-158">In the Description field, type a value.</span></span>
5. <span data-ttu-id="84b23-159">[循環棚卸の最大数] フィールドに数値を入力します。</span><span class="sxs-lookup"><span data-stu-id="84b23-159">In the Maximum number of cycle counts field, enter a number.</span></span>
6. <span data-ttu-id="84b23-160">[保存] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="84b23-160">Click Save.</span></span>
7. <span data-ttu-id="84b23-161">[場所の選択] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="84b23-161">Click Select locations.</span></span>
8. <span data-ttu-id="84b23-162">一覧で、選択された行をマークします。</span><span class="sxs-lookup"><span data-stu-id="84b23-162">In the list, mark the selected row.</span></span>
9. <span data-ttu-id="84b23-163">[基準] フィールドで値を選択します。</span><span class="sxs-lookup"><span data-stu-id="84b23-163">In the Criteria field, select a value.</span></span>
10. <span data-ttu-id="84b23-164">[OK] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="84b23-164">Click OK.</span></span>
11. <span data-ttu-id="84b23-165">[次回の循環棚卸までの日数] フィールドに数値を入力します。</span><span class="sxs-lookup"><span data-stu-id="84b23-165">In the Days between cycle counting field, enter a number.</span></span>
    * <span data-ttu-id="84b23-166">たとえば、[次回の循環棚卸までの日数] フィールドを 5 に設定すると、循環棚卸作業は 5 日ごとに作成されます。</span><span class="sxs-lookup"><span data-stu-id="84b23-166">For example, if the Days between cycle counting field is set to 5, cycle counting work will be created every five days.</span></span> <span data-ttu-id="84b23-167">ただし、循環棚卸作業が 3 日目に処理される場合は、次の循環棚卸作業は、最後の循環棚卸処理の 5 日後の 8 日目に作成されます。</span><span class="sxs-lookup"><span data-stu-id="84b23-167">However, if cycle counting work is processed on day three, the next cycle counting work will be created five days after the last cycle counting was processed, on day 8.</span></span>  
12. <span data-ttu-id="84b23-168">[保存] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="84b23-168">Click Save.</span></span>
13. <span data-ttu-id="84b23-169">[新規] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="84b23-169">Click New.</span></span>
14. <span data-ttu-id="84b23-170">[順序番号] フィールドに番号を入力します。</span><span class="sxs-lookup"><span data-stu-id="84b23-170">In the Sequence number field, enter a number.</span></span>
    * <span data-ttu-id="84b23-171">並べ替えは、最小番号から最大番号です。</span><span class="sxs-lookup"><span data-stu-id="84b23-171">The sort is from the smallest number to the largest number.</span></span> <span data-ttu-id="84b23-172">値は 0 (ゼロ) より大きい値に設定する必要があります。</span><span class="sxs-lookup"><span data-stu-id="84b23-172">The value must be more than 0 (zero).</span></span>  
15. <span data-ttu-id="84b23-173">一覧で、選択された行をマークします。</span><span class="sxs-lookup"><span data-stu-id="84b23-173">In the list, mark the selected row.</span></span>
16. <span data-ttu-id="84b23-174">[説明] フィールドに値を入力します。</span><span class="sxs-lookup"><span data-stu-id="84b23-174">In the Description field, type a value.</span></span>
17. <span data-ttu-id="84b23-175">[保存] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="84b23-175">Click Save.</span></span>
18. <span data-ttu-id="84b23-176">[製品クエリの定義] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="84b23-176">Click Define product query.</span></span>
19. <span data-ttu-id="84b23-177">一覧で、選択された行をマークします。</span><span class="sxs-lookup"><span data-stu-id="84b23-177">In the list, mark the selected row.</span></span>
20. <span data-ttu-id="84b23-178">[基準] フィールドで、値を入力または選択します。</span><span class="sxs-lookup"><span data-stu-id="84b23-178">In the Criteria field, enter or select a value.</span></span>
21. <span data-ttu-id="84b23-179">[OK] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="84b23-179">Click OK.</span></span>
22. <span data-ttu-id="84b23-180">ページを閉じます。</span><span class="sxs-lookup"><span data-stu-id="84b23-180">Close the page.</span></span>

