---
title: コンテナー詰めの設定
description: このトピックでは、倉庫管理での積荷のコンテナー詰めを自動化する方法について説明します。
author: ShylaThompson
manager: AnnBe
ms.date: 07/22/19
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: WHSWaveTemplateTable, InventLocationIdLookup, WHSContainerType, WHSContainerGroup, WHSContainerizationTable, WHSContainerizationBreak, WHSCreateContainerBreak
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.search.region: Global
ms.search.industry: Distribution
ms.author: mirzaab
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: f9dbf62e1c518b0cd77da693127588a04f17d622
ms.sourcegitcommit: fcb27d6a46cd544feef34f6ec7607bdd46b0c12b
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 03/18/2020
ms.locfileid: "3148265"
---
# <a name="set-up-containerization"></a><span data-ttu-id="e9e2e-103">コンテナー詰めの設定</span><span class="sxs-lookup"><span data-stu-id="e9e2e-103">Set up containerization</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="e9e2e-104">このトピックでは、倉庫管理での積荷のコンテナー詰めを自動化する方法について説明します。</span><span class="sxs-lookup"><span data-stu-id="e9e2e-104">This topic describes how to automate the containerization of loads in Warehouse management.</span></span> <span data-ttu-id="e9e2e-105">自動化されたコンテナー詰めは、ウェーブが処理される際に、出荷のためのコンテナーとピッキングの作業を作成し、作業ラインがコンテナーに合った数量に分割されます。</span><span class="sxs-lookup"><span data-stu-id="e9e2e-105">Automated containerization creates containers and the picking work for shipments when a wave is processed and work lines can be split into quantities that fit the containers.</span></span> <span data-ttu-id="e9e2e-106">これにより、倉庫作業者は選択したコンテナーに品目を直接ピッキングすることができます。</span><span class="sxs-lookup"><span data-stu-id="e9e2e-106">This helps warehouse workers to pick the items directly into the chosen container.</span></span> <span data-ttu-id="e9e2e-107">手動梱包プロセスと比べて、コンテナーの作成、品目の割り当て、コンテナーの終了などのタスクがシステムによって自動化されます。</span><span class="sxs-lookup"><span data-stu-id="e9e2e-107">Compared to the manual packing process, tasks such as creating containers, assigning items, and closing containers are automated by the system.</span></span> <span data-ttu-id="e9e2e-108">この手順は、USMF というデモ会社を使用し、倉庫マネージャーによって行われます。</span><span class="sxs-lookup"><span data-stu-id="e9e2e-108">This procedure uses the USMF demo company and is performed by a Warehouse manager.</span></span>


## <a name="set-up-a-wave-template"></a><span data-ttu-id="e9e2e-109">ウェーブ テンプレートの設定</span><span class="sxs-lookup"><span data-stu-id="e9e2e-109">Set up a wave template</span></span>
1. <span data-ttu-id="e9e2e-110">ナビゲーション ウィンドウで、**モジュール > 倉庫管理 > 設定 > ウェーブ > ウェーブ テンプレート**の順に移動します。</span><span class="sxs-lookup"><span data-stu-id="e9e2e-110">In the navigation pane, go to **Modules > Warehouse management > Setup > Waves > Wave templates**.</span></span>
2. <span data-ttu-id="e9e2e-111">**新規** を選択します。</span><span class="sxs-lookup"><span data-stu-id="e9e2e-111">Select **New**.</span></span>
3. <span data-ttu-id="e9e2e-112">**ウェーブ テンプレート名**フィールドで、値を入力します。</span><span class="sxs-lookup"><span data-stu-id="e9e2e-112">In the **Wave template name** field, type a value.</span></span>
4. <span data-ttu-id="e9e2e-113">**ウェーブ テンプレートの説明**フィールドで、値を入力します。</span><span class="sxs-lookup"><span data-stu-id="e9e2e-113">In the **Wave template description** field, type a value.</span></span>
5. <span data-ttu-id="e9e2e-114">**サイト** フィールドで値を入力または選択します。</span><span class="sxs-lookup"><span data-stu-id="e9e2e-114">In the **Site** field, enter or select a value.</span></span>
6. <span data-ttu-id="e9e2e-115">**倉庫**フィールドで、値を入力または選択します。</span><span class="sxs-lookup"><span data-stu-id="e9e2e-115">In the **Warehouse** field, enter or select a value.</span></span>
7. <span data-ttu-id="e9e2e-116">**メソッド** セクションを展開します。</span><span class="sxs-lookup"><span data-stu-id="e9e2e-116">Expand the **Methods** section.</span></span> <span data-ttu-id="e9e2e-117">**選択されたメソッド**ウィンドウは、選択したウェーブ テンプレート タイプのメソッドを一覧表示します。</span><span class="sxs-lookup"><span data-stu-id="e9e2e-117">The **Selected methods** pane lists the methods for the selected wave template type.</span></span> <span data-ttu-id="e9e2e-118">ウェーブ テンプレートには、[コンテナー] メソッドを含める必要があります。</span><span class="sxs-lookup"><span data-stu-id="e9e2e-118">The wave template must include the containerize method.</span></span>  
8. <span data-ttu-id="e9e2e-119">**ウェーブ ステップ コード** フィールドに値を入力します。</span><span class="sxs-lookup"><span data-stu-id="e9e2e-119">In the **Wave step code** field, type a value.</span></span> <span data-ttu-id="e9e2e-120">追加したメソッドの任意のウェーブ ステップ コードを入力します。</span><span class="sxs-lookup"><span data-stu-id="e9e2e-120">Enter a Wave step code for the added method, which can be any code.</span></span> <span data-ttu-id="e9e2e-121">メソッドを複数回追加して、異なるウェーブ ステップ コードを割り当てることができます。</span><span class="sxs-lookup"><span data-stu-id="e9e2e-121">It's possible to add the method more than once and assign different wave step codes.</span></span> <span data-ttu-id="e9e2e-122">これを行うには、**ウェーブのプロセス方法**ページで**このメソッドの反復可能**を選択します。</span><span class="sxs-lookup"><span data-stu-id="e9e2e-122">To do this, select **Repeatable for this method** in the **Wave process methods** page.</span></span>  
9. <span data-ttu-id="e9e2e-123">**保存** を選択します。</span><span class="sxs-lookup"><span data-stu-id="e9e2e-123">Select **Save**.</span></span>
10. <span data-ttu-id="e9e2e-124">ページを閉じます。</span><span class="sxs-lookup"><span data-stu-id="e9e2e-124">Close the page.</span></span>

## <a name="set-up-a-container-type"></a><span data-ttu-id="e9e2e-125">コンテナー タイプを設定する</span><span class="sxs-lookup"><span data-stu-id="e9e2e-125">Set up a container type</span></span>
1. <span data-ttu-id="e9e2e-126">ナビゲーション ウィンドウで、**モジュール > 倉庫管理 > 設定 > コンテナー > コンテナー タイプ**の順に移動します。</span><span class="sxs-lookup"><span data-stu-id="e9e2e-126">In the navigation pane, go to **Modules > Warehouse management > Setup > Containers > Container types**.</span></span> <span data-ttu-id="e9e2e-127">**コンテナー タイプ** ページでコンテナーを定義できます。</span><span class="sxs-lookup"><span data-stu-id="e9e2e-127">You can define your containers in the **Container types** page.</span></span> <span data-ttu-id="e9e2e-128">風袋重量、最大重量、最大容積、長さ、幅と高さを含むコンテナーの現物分析コードをコンフィギュレーションできます。</span><span class="sxs-lookup"><span data-stu-id="e9e2e-128">You can configure the physical dimensions of containers including tare weight, maximum weight, maximum volume, length, width, and height.</span></span> <span data-ttu-id="e9e2e-129">この例では、3 つのサイズのボックスがあります。</span><span class="sxs-lookup"><span data-stu-id="e9e2e-129">In this example, we have three different sizes of boxes.</span></span>  
2. <span data-ttu-id="e9e2e-130">**新規** を選択します。</span><span class="sxs-lookup"><span data-stu-id="e9e2e-130">Select **New**.</span></span>
3. <span data-ttu-id="e9e2e-131">**コンテナー タイプ コード** フィールドに値を入力します。</span><span class="sxs-lookup"><span data-stu-id="e9e2e-131">In the **Container type code** field, type a value.</span></span>
4. <span data-ttu-id="e9e2e-132">**風袋重量**フィールドに数値を入力します。</span><span class="sxs-lookup"><span data-stu-id="e9e2e-132">In the **Tare weight** field, enter a number.</span></span>
5. <span data-ttu-id="e9e2e-133">**最大重量**フィールドに数値を入力します。</span><span class="sxs-lookup"><span data-stu-id="e9e2e-133">In the **Maximum weight** field, enter a number.</span></span>
6. <span data-ttu-id="e9e2e-134">**容積**フィールドに数値を入力します。</span><span class="sxs-lookup"><span data-stu-id="e9e2e-134">In the **Volume** field, enter a number.</span></span>
7. <span data-ttu-id="e9e2e-135">**長さ**フィールドに数値を入力します。</span><span class="sxs-lookup"><span data-stu-id="e9e2e-135">In the **Length** field, enter a number.</span></span>
8. <span data-ttu-id="e9e2e-136">**幅**フィールドに数値を入力します。</span><span class="sxs-lookup"><span data-stu-id="e9e2e-136">In the **Width** field, enter a number.</span></span>
9. <span data-ttu-id="e9e2e-137">**高さ**フィールドに数値を入力します。</span><span class="sxs-lookup"><span data-stu-id="e9e2e-137">In the **Height** field, enter a number.</span></span>
10. <span data-ttu-id="e9e2e-138">**説明**フィールドで、値を入力します。</span><span class="sxs-lookup"><span data-stu-id="e9e2e-138">In the **Description** field, type a value.</span></span>
11. <span data-ttu-id="e9e2e-139">**保存** を選択します。</span><span class="sxs-lookup"><span data-stu-id="e9e2e-139">Select **Save**.</span></span>
13. <span data-ttu-id="e9e2e-140">手順 2～11 をさらに 2 回繰り返して、3 つの合計コンテナー タイプを作成します。</span><span class="sxs-lookup"><span data-stu-id="e9e2e-140">Repeat steps 2-11 two more times to make three total container types.</span></span>
14. <span data-ttu-id="e9e2e-141">ページを閉じます。</span><span class="sxs-lookup"><span data-stu-id="e9e2e-141">Close the page.</span></span>

## <a name="set-up-a-container-group"></a><span data-ttu-id="e9e2e-142">コンテナー グループを設定する</span><span class="sxs-lookup"><span data-stu-id="e9e2e-142">Set up a container group</span></span>
1. <span data-ttu-id="e9e2e-143">ナビゲーション ウィンドウで、**モジュール > 倉庫管理 > 設定 > コンテナー > コンテナー グループ**の順に移動します。</span><span class="sxs-lookup"><span data-stu-id="e9e2e-143">In the navigation pane, go to **Modules > Warehouse management > Setup > Containers > Container groups**.</span></span>
2. <span data-ttu-id="e9e2e-144">アクション ウィンドウで、**新規**を選択します。</span><span class="sxs-lookup"><span data-stu-id="e9e2e-144">In the action pane, select **New**.</span></span> <span data-ttu-id="e9e2e-145">コンテナーのタイプの論理グループを設定できます。</span><span class="sxs-lookup"><span data-stu-id="e9e2e-145">You can set up logical groups of container types.</span></span> <span data-ttu-id="e9e2e-146">グループごとに、コンテナーを梱包する順番と、コンテナーに詰める割合を指定できます。コンテナーに適合するどうかを決定するために、品目のサイズ分析コードが使用されます。</span><span class="sxs-lookup"><span data-stu-id="e9e2e-146">For each group, you can specify the sequence in which to pack the containers and the percentage of the containers to fill.The size dimensions of the item is used to determine whether it will fit in a container.</span></span> <span data-ttu-id="e9e2e-147">品目のサイズ分析コードに最も近いコンテナーが使用されます。</span><span class="sxs-lookup"><span data-stu-id="e9e2e-147">The container that is closest to the size dimensions of the item is used.</span></span> <span data-ttu-id="e9e2e-148">グループにコンテナーが複数ある場合は、最大のコンテナーが 1 番目、最小のコンテナーが最後になるようにサイズで順番を並べるようにお勧めします。</span><span class="sxs-lookup"><span data-stu-id="e9e2e-148">If you have multiple container types in a group, we recommend that you arrange the sequence by size, so that the largest container is first, number 1 in the sequence, and the smallest container is last.</span></span>    
3. <span data-ttu-id="e9e2e-149">**コンテナー グループ ID** フィールドに、前に作成した値を入力します。</span><span class="sxs-lookup"><span data-stu-id="e9e2e-149">In the **Container group ID** field, type a value that you created earlier.</span></span>
4. <span data-ttu-id="e9e2e-150">**説明フィールド**で、値を入力します。</span><span class="sxs-lookup"><span data-stu-id="e9e2e-150">In the **Description field**, type a value.</span></span>
5. <span data-ttu-id="e9e2e-151">前に作成した 3 つのコンテナー タイプすべてに対して、手順 2～4 を繰り返します。</span><span class="sxs-lookup"><span data-stu-id="e9e2e-151">Repeat steps 2-4 for all three container types you created earlier.</span></span>
6. <span data-ttu-id="e9e2e-152">**保存** を選択します。</span><span class="sxs-lookup"><span data-stu-id="e9e2e-152">Select **Save**.</span></span>
7. <span data-ttu-id="e9e2e-153">ページを閉じます。</span><span class="sxs-lookup"><span data-stu-id="e9e2e-153">Close the page.</span></span>

## <a name="set-up-a-container-build-template"></a><span data-ttu-id="e9e2e-154">コンテナー構築テンプレートのセットアップ</span><span class="sxs-lookup"><span data-stu-id="e9e2e-154">Set up a container build template</span></span>
1. <span data-ttu-id="e9e2e-155">ナビゲーション ウィンドウで、**モジュール > 倉庫管理 > 設定 > コンテナー > コンテナー構築テンプレート**の順に移動します。</span><span class="sxs-lookup"><span data-stu-id="e9e2e-155">In the navigation pane, go to **Modules > Warehouse management > Setup > Containers > Container build templates**.</span></span>
2. <span data-ttu-id="e9e2e-156">**新規** を選択します。</span><span class="sxs-lookup"><span data-stu-id="e9e2e-156">Select **New**.</span></span> <span data-ttu-id="e9e2e-157">コンテナー構築テンプレートは、どのコンテナー詰めのプロセスが実行されるかに基づきます。</span><span class="sxs-lookup"><span data-stu-id="e9e2e-157">The container build template is based on which of the containerization processes are performed.</span></span> <span data-ttu-id="e9e2e-158">各コンテナー構築テンプレートは、ウェーブ テンプレートで使用されるコンテナー詰めのプロセスを定義します。</span><span class="sxs-lookup"><span data-stu-id="e9e2e-158">Each container build template defines one containerization process that will be used by a wave template.</span></span> <span data-ttu-id="e9e2e-159">**クエリの編集**オプションで、選択したテンプレートを処理する条件を定義することができます。</span><span class="sxs-lookup"><span data-stu-id="e9e2e-159">The **Edit query** option allows you to define the conditions on which the selected template will be processed.</span></span> <span data-ttu-id="e9e2e-160">たとえば、特定の顧客、製品、または倉庫のコンテナー詰めのみ実行したり、テンプレートに対応するクエリの範囲を追加したりできます。</span><span class="sxs-lookup"><span data-stu-id="e9e2e-160">For example, you may want to only run containerization for specific customers, products, or warehouses or you can add the corresponding query ranges to the template.</span></span> <span data-ttu-id="e9e2e-161">**ウェーブ ステップ コード** フィールドは、コンテナー構築テンプレートをウェーブ テンプレートの手順にリンクする方法です。</span><span class="sxs-lookup"><span data-stu-id="e9e2e-161">The **Wave step code** field is how a container build template is linked to steps in a wave template.</span></span> <span data-ttu-id="e9e2e-162">ウェーブが実行されると、コンテナー詰めの開始に使用されるコンテナー構築テンプレートが決まります。</span><span class="sxs-lookup"><span data-stu-id="e9e2e-162">When a wave is executed, it determines which container build template(s) are used to initiate containerization.</span></span> <span data-ttu-id="e9e2e-163">[基準クエリのタイプ] フィールドで、梱包内容やフィルターがクエリする基準を決定します。</span><span class="sxs-lookup"><span data-stu-id="e9e2e-163">The Base query type field determines what to pack and what to base the filter query on.</span></span> 
3. <span data-ttu-id="e9e2e-164">**コンテナー テンプレート ID** フィールドに値を入力します。</span><span class="sxs-lookup"><span data-stu-id="e9e2e-164">In the **Container template ID** field, type a value.</span></span>
4. <span data-ttu-id="e9e2e-165">**コンテナー グループ ID** フィールドで、値を入力または選択します。</span><span class="sxs-lookup"><span data-stu-id="e9e2e-165">In the **Container group ID** field, enter or select a value.</span></span>
5. <span data-ttu-id="e9e2e-166">**ウェーブ ステップ コード** フィールドに値を入力します。</span><span class="sxs-lookup"><span data-stu-id="e9e2e-166">In the **Wave step code** field, type a value.</span></span>
6. <span data-ttu-id="e9e2e-167">**分割ピッキングを許可する**チェック ボックスを選択します。</span><span class="sxs-lookup"><span data-stu-id="e9e2e-167">Select the **Allow split picks** check box.</span></span>
7. <span data-ttu-id="e9e2e-168">**保存** を選択します。</span><span class="sxs-lookup"><span data-stu-id="e9e2e-168">Select **Save**.</span></span>
8. <span data-ttu-id="e9e2e-169">**コンテナー混合制約**を選択します。</span><span class="sxs-lookup"><span data-stu-id="e9e2e-169">Select **Containier mixing constraints**.</span></span> <span data-ttu-id="e9e2e-170">混合ロジック ブレークで、コンテナーに配賦ラインを梱包するルールを設定できます。</span><span class="sxs-lookup"><span data-stu-id="e9e2e-170">Mixing logic breaks allows you to set up rules for packing allocation lines in containers.</span></span> <span data-ttu-id="e9e2e-171">たとえば、品目をコンテナーに割り当てる際に **品目番号フィールド**を追加する場合、新しい品目番号があると新しいコンテナーが作成されます。</span><span class="sxs-lookup"><span data-stu-id="e9e2e-171">For example, if you add the **Item number field**, when items are assigned to containers, a new container will be created when there is a new item number.</span></span> <span data-ttu-id="e9e2e-172">これにより、作業者が同じコンテナーの 2 人の異なる顧客に配賦ラインを梱包することを防ぎます。</span><span class="sxs-lookup"><span data-stu-id="e9e2e-172">This is will prevent workers from packing allocations lines for two different customers in the same container.</span></span>  
9. <span data-ttu-id="e9e2e-173">**新規** を選択します。</span><span class="sxs-lookup"><span data-stu-id="e9e2e-173">Select **New**.</span></span>
10. <span data-ttu-id="e9e2e-174">**テーブル** フィールドで、オプションを選択します。</span><span class="sxs-lookup"><span data-stu-id="e9e2e-174">In the **Table** field, select an option.</span></span>
11. <span data-ttu-id="e9e2e-175">**フィールドの選択**フィールドで、値を入力または選択します。</span><span class="sxs-lookup"><span data-stu-id="e9e2e-175">In the **Field Select** field, enter or select a value.</span></span>
12. <span data-ttu-id="e9e2e-176">**OK** を選択します。</span><span class="sxs-lookup"><span data-stu-id="e9e2e-176">Select **OK**.</span></span>

