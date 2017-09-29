--- 
title: "コンテナー詰めの設定"
description: "この手順では、倉庫管理での積荷のコンテナー詰めを自動化する方法について説明します。"
author: YuyuScheller
manager: AnnBe
ms.date: 06/07/2016
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: bis
ms.search.scope: Operations
ms.search.region: Global
ms.search.industry: Distribution
ms.author: mirzaab
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 663da58ef01b705c0c984fbfd3fce8bc31be04c6
ms.openlocfilehash: aeb7d956560c513c08d5e20dcf20989b49137a52
ms.contentlocale: ja-jp
ms.lasthandoff: 08/29/2017

---
# <a name="set-up-containerization"></a><span data-ttu-id="31d50-103">コンテナー詰めの設定</span><span class="sxs-lookup"><span data-stu-id="31d50-103">Set up containerization</span></span>

[!include[task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="31d50-104">この手順では、倉庫管理での積荷のコンテナー詰めを自動化する方法について説明します。</span><span class="sxs-lookup"><span data-stu-id="31d50-104">This procedure describes how to automate the containerization of loads in Warehouse management.</span></span> <span data-ttu-id="31d50-105">自動化されたコンテナー詰めは、ウェーブが処理される際に、出荷のためのコンテナーとピッキングの作業を作成し、作業ラインがコンテナーに合った数量に分割されます。</span><span class="sxs-lookup"><span data-stu-id="31d50-105">Automated containerization creates containers and the picking work for shipments when a wave is processed and work lines can be split into quantities that fit the containers.</span></span> <span data-ttu-id="31d50-106">これにより、倉庫作業者は選択したコンテナーに品目を直接ピッキングすることができます。</span><span class="sxs-lookup"><span data-stu-id="31d50-106">This helps warehouse workers to pick the items directly into the chosen container.</span></span> <span data-ttu-id="31d50-107">手動梱包プロセスと比べて、コンテナーの作成、品目の割り当て、コンテナーの終了などのタスクがシステムによって自動化されます。</span><span class="sxs-lookup"><span data-stu-id="31d50-107">Compared to the manual packing process, tasks such as creating containers, assigning items, and closing containers are automated by the system.</span></span> <span data-ttu-id="31d50-108">この手順は、USMF というデモ会社を使用し、倉庫マネージャーによって行われます。</span><span class="sxs-lookup"><span data-stu-id="31d50-108">This procedure uses the USMF demo company and is performed by a Warehouse manager.</span></span>


## <a name="set-up-a-wave-template"></a><span data-ttu-id="31d50-109">ウェーブ テンプレートの設定</span><span class="sxs-lookup"><span data-stu-id="31d50-109">Set up a wave template</span></span>
1. <span data-ttu-id="31d50-110">[倉庫管理] > [設定] > [ウェーブ] > [ウェーブ テンプレート] の順に移動します。</span><span class="sxs-lookup"><span data-stu-id="31d50-110">Go to Warehouse management > Setup > Waves > Wave templates.</span></span>
2. <span data-ttu-id="31d50-111">[新規] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="31d50-111">Click New.</span></span>
3. <span data-ttu-id="31d50-112">[ウェーブ テンプレート名] フィールドで、値を入力します。</span><span class="sxs-lookup"><span data-stu-id="31d50-112">In the Wave template name field, type a value.</span></span>
4. <span data-ttu-id="31d50-113">[ウェーブ テンプレートの説明] フィールドで、値を入力します。</span><span class="sxs-lookup"><span data-stu-id="31d50-113">In the Wave template description field, type a value.</span></span>
5. <span data-ttu-id="31d50-114">[サイト] フィールドで値を入力または選択します。</span><span class="sxs-lookup"><span data-stu-id="31d50-114">In the Site field, enter or select a value.</span></span>
6. <span data-ttu-id="31d50-115">[倉庫] フィールドで、値を入力または選択します。</span><span class="sxs-lookup"><span data-stu-id="31d50-115">In the Warehouse field, enter or select a value.</span></span>
7. <span data-ttu-id="31d50-116">[メソッド] セクションを展開します。</span><span class="sxs-lookup"><span data-stu-id="31d50-116">Expand the Methods section.</span></span>
    * <span data-ttu-id="31d50-117">[選択されたメソッド] ウィンドウは、選択したウェーブ テンプレート タイプのメソッドを一覧表示します。</span><span class="sxs-lookup"><span data-stu-id="31d50-117">The Selected methods pane lists the methods for the selected wave template type.</span></span> <span data-ttu-id="31d50-118">ウェーブ テンプレートには、[コンテナー] メソッドを含める必要があります。</span><span class="sxs-lookup"><span data-stu-id="31d50-118">The wave template must include the containerize method.</span></span>  
8. <span data-ttu-id="31d50-119">一覧で、目的のレコードを見つけ、選択します。</span><span class="sxs-lookup"><span data-stu-id="31d50-119">In the list, find and select the desired record.</span></span>
9. <span data-ttu-id="31d50-120">[ウェーブ ステップ コード] フィールドに値を入力します。</span><span class="sxs-lookup"><span data-stu-id="31d50-120">In the Wave step code field, type a value.</span></span>
    * <span data-ttu-id="31d50-121">追加したメソッドの任意のウェーブ ステップ コードを入力します。</span><span class="sxs-lookup"><span data-stu-id="31d50-121">Enter a Wave step code for the added method, which can be any code.</span></span> <span data-ttu-id="31d50-122">メソッドを何度も追加して、異なるウェーブ ステップ コードを割り当てることができます。</span><span class="sxs-lookup"><span data-stu-id="31d50-122">It’s possible to add the method more than once and assign different wave step codes.</span></span> <span data-ttu-id="31d50-123">これを行うには、ウェーブのプロセス方法のページでこのメソッドの反復可能を選択します。</span><span class="sxs-lookup"><span data-stu-id="31d50-123">To do this, select Repeatable for this method in the Wave process methods page.</span></span>  
10. <span data-ttu-id="31d50-124">[保存] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="31d50-124">Click Save.</span></span>
11. <span data-ttu-id="31d50-125">ページを閉じます。</span><span class="sxs-lookup"><span data-stu-id="31d50-125">Close the page.</span></span>

## <a name="set-up-a-container-type"></a><span data-ttu-id="31d50-126">コンテナー タイプを設定する</span><span class="sxs-lookup"><span data-stu-id="31d50-126">Set up a container type</span></span>
1. <span data-ttu-id="31d50-127">[倉庫管理] > [設定] > [コンテナー] > [コンテナー タイプ] の順に移動します。</span><span class="sxs-lookup"><span data-stu-id="31d50-127">Go to Warehouse management > Setup > Containers > Container types.</span></span>
    * <span data-ttu-id="31d50-128">[コンテナー タイプ] ページでコンテナーを定義できます。</span><span class="sxs-lookup"><span data-stu-id="31d50-128">You can define your containers in the Container types page.</span></span> <span data-ttu-id="31d50-129">風袋重量、最大重量、最大容積、長さ、幅と高さを含むコンテナーの現物分析コードをコンフィギュレーションできます。</span><span class="sxs-lookup"><span data-stu-id="31d50-129">You can configure the physical dimensions of containers including tare weight, maximum weight, maximum volume, length, width, and height.</span></span> <span data-ttu-id="31d50-130">この例では、3 つのサイズのボックスがあります。</span><span class="sxs-lookup"><span data-stu-id="31d50-130">In this example, we have three different sizes of boxes.</span></span>  
2. <span data-ttu-id="31d50-131">[新規] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="31d50-131">Click New.</span></span>
3. <span data-ttu-id="31d50-132">[コンテナー タイプ コード] フィールドに値を入力します。</span><span class="sxs-lookup"><span data-stu-id="31d50-132">In the Container type code field, type a value.</span></span>
4. <span data-ttu-id="31d50-133">[風袋重量] フィールドに数値を入力します。</span><span class="sxs-lookup"><span data-stu-id="31d50-133">In the Tare weight field, enter a number.</span></span>
5. <span data-ttu-id="31d50-134">[最大重量] フィールドに数値を入力します。</span><span class="sxs-lookup"><span data-stu-id="31d50-134">In the Maximum weight field, enter a number.</span></span>
6. <span data-ttu-id="31d50-135">[容積] フィールドに数値を入力します。</span><span class="sxs-lookup"><span data-stu-id="31d50-135">In the Volume field, enter a number.</span></span>
7. <span data-ttu-id="31d50-136">[長さ] フィールドに数値を入力します。</span><span class="sxs-lookup"><span data-stu-id="31d50-136">In the Length field, enter a number.</span></span>
8. <span data-ttu-id="31d50-137">[幅] フィールドに数値を入力します。</span><span class="sxs-lookup"><span data-stu-id="31d50-137">In the Width field, enter a number.</span></span>
9. <span data-ttu-id="31d50-138">[高さ] フィールドに数値を入力します。</span><span class="sxs-lookup"><span data-stu-id="31d50-138">In the Height field, enter a number.</span></span>
10. <span data-ttu-id="31d50-139">[説明] フィールドに値を入力します。</span><span class="sxs-lookup"><span data-stu-id="31d50-139">In the Description field, type a value.</span></span>
11. <span data-ttu-id="31d50-140">[保存] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="31d50-140">Click Save.</span></span>
12. <span data-ttu-id="31d50-141">[新規] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="31d50-141">Click New.</span></span>
13. <span data-ttu-id="31d50-142">[コンテナー タイプ コード] フィールドに値を入力します。</span><span class="sxs-lookup"><span data-stu-id="31d50-142">In the Container type code field, type a value.</span></span>
14. <span data-ttu-id="31d50-143">[説明] フィールドに値を入力します。</span><span class="sxs-lookup"><span data-stu-id="31d50-143">In the Description field, type a value.</span></span>
15. <span data-ttu-id="31d50-144">[風袋重量] フィールドに数値を入力します。</span><span class="sxs-lookup"><span data-stu-id="31d50-144">In the Tare weight field, enter a number.</span></span>
16. <span data-ttu-id="31d50-145">[最大重量] フィールドに数値を入力します。</span><span class="sxs-lookup"><span data-stu-id="31d50-145">In the Maximum weight field, enter a number.</span></span>
17. <span data-ttu-id="31d50-146">[容積] フィールドに数値を入力します。</span><span class="sxs-lookup"><span data-stu-id="31d50-146">In the Volume field, enter a number.</span></span>
18. <span data-ttu-id="31d50-147">[長さ] フィールドに数値を入力します。</span><span class="sxs-lookup"><span data-stu-id="31d50-147">In the Length field, enter a number.</span></span>
19. <span data-ttu-id="31d50-148">[幅] フィールドに数値を入力します。</span><span class="sxs-lookup"><span data-stu-id="31d50-148">In the Width field, enter a number.</span></span>
20. <span data-ttu-id="31d50-149">[高さ] フィールドに数値を入力します。</span><span class="sxs-lookup"><span data-stu-id="31d50-149">In the Height field, enter a number.</span></span>
21. <span data-ttu-id="31d50-150">[保存] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="31d50-150">Click Save.</span></span>
22. <span data-ttu-id="31d50-151">[新規] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="31d50-151">Click New.</span></span>
23. <span data-ttu-id="31d50-152">[コンテナー タイプ コード] フィールドに値を入力します。</span><span class="sxs-lookup"><span data-stu-id="31d50-152">In the Container type code field, type a value.</span></span>
24. <span data-ttu-id="31d50-153">[説明] フィールドに値を入力します。</span><span class="sxs-lookup"><span data-stu-id="31d50-153">In the Description field, type a value.</span></span>
25. <span data-ttu-id="31d50-154">[風袋重量] フィールドに数値を入力します。</span><span class="sxs-lookup"><span data-stu-id="31d50-154">In the Tare weight field, enter a number.</span></span>
26. <span data-ttu-id="31d50-155">[最大重量] フィールドに数値を入力します。</span><span class="sxs-lookup"><span data-stu-id="31d50-155">In the Maximum weight field, enter a number.</span></span>
27. <span data-ttu-id="31d50-156">[容積] フィールドに数値を入力します。</span><span class="sxs-lookup"><span data-stu-id="31d50-156">In the Volume field, enter a number.</span></span>
28. <span data-ttu-id="31d50-157">[長さ] フィールドに数値を入力します。</span><span class="sxs-lookup"><span data-stu-id="31d50-157">In the Length field, enter a number.</span></span>
29. <span data-ttu-id="31d50-158">[幅] フィールドに数値を入力します。</span><span class="sxs-lookup"><span data-stu-id="31d50-158">In the Width field, enter a number.</span></span>
30. <span data-ttu-id="31d50-159">[高さ] フィールドに数値を入力します。</span><span class="sxs-lookup"><span data-stu-id="31d50-159">In the Height field, enter a number.</span></span>
31. <span data-ttu-id="31d50-160">[保存] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="31d50-160">Click Save.</span></span>
32. <span data-ttu-id="31d50-161">ページを閉じます。</span><span class="sxs-lookup"><span data-stu-id="31d50-161">Close the page.</span></span>

## <a name="set-up-a-container-group"></a><span data-ttu-id="31d50-162">コンテナー グループを設定する</span><span class="sxs-lookup"><span data-stu-id="31d50-162">Set up a container group</span></span>
1. <span data-ttu-id="31d50-163">[倉庫管理] > [設定] > [コンテナー] > [コンテナー グループ] の順に移動します。</span><span class="sxs-lookup"><span data-stu-id="31d50-163">Go to Warehouse management > Setup > Containers > Container groups.</span></span>
2. <span data-ttu-id="31d50-164">[新規] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="31d50-164">Click New.</span></span>
    * <span data-ttu-id="31d50-165">コンテナーのタイプの論理グループを設定できます。</span><span class="sxs-lookup"><span data-stu-id="31d50-165">You can set up logical groups of container types.</span></span> <span data-ttu-id="31d50-166">グループごとに、コンテナーを梱包する順番と、コンテナーに詰める割合を指定できます。コンテナーに適合するどうかを決定するために、品目のサイズ分析コードが使用されます。</span><span class="sxs-lookup"><span data-stu-id="31d50-166">For each group, you can specify the sequence in which to pack the containers and the percentage of the containers to fill.The size dimensions of the item is used to determine whether it will fit in a container.</span></span> <span data-ttu-id="31d50-167">品目のサイズ分析コードに最も近いコンテナーが使用されます。</span><span class="sxs-lookup"><span data-stu-id="31d50-167">The container that is closest to the size dimensions of the item is used.</span></span> <span data-ttu-id="31d50-168">グループにコンテナーが複数ある場合は、最大のコンテナーが 1 番目、最小のコンテナーが最後になるようにサイズで順番を並べるようにお勧めします。</span><span class="sxs-lookup"><span data-stu-id="31d50-168">If you have multiple container types in a group, we recommend that you arrange the sequence by size, so that the largest container is first, number 1 in the sequence, and the smallest container is last.</span></span>    
3. <span data-ttu-id="31d50-169">[コンテナー グループ ID] フィールドに値を入力します。</span><span class="sxs-lookup"><span data-stu-id="31d50-169">In the Container group ID field, type a value.</span></span>
4. <span data-ttu-id="31d50-170">[説明] フィールドに値を入力します。</span><span class="sxs-lookup"><span data-stu-id="31d50-170">In the Description field, type a value.</span></span>
5. <span data-ttu-id="31d50-171">[新規] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="31d50-171">Click New.</span></span>
6. <span data-ttu-id="31d50-172">一覧で、選択された行をマークします。</span><span class="sxs-lookup"><span data-stu-id="31d50-172">In the list, mark the selected row.</span></span>
7. <span data-ttu-id="31d50-173">[コンテナー タイプ] フィールドで、値を入力または選択します。</span><span class="sxs-lookup"><span data-stu-id="31d50-173">In the Container type field, enter or select a value.</span></span>
8. <span data-ttu-id="31d50-174">[新規] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="31d50-174">Click New.</span></span>
9. <span data-ttu-id="31d50-175">一覧で、選択された行をマークします。</span><span class="sxs-lookup"><span data-stu-id="31d50-175">In the list, mark the selected row.</span></span>
10. <span data-ttu-id="31d50-176">[コンテナー タイプ] フィールドで、値を入力または選択します。</span><span class="sxs-lookup"><span data-stu-id="31d50-176">In the Container type field, enter or select a value.</span></span>
11. <span data-ttu-id="31d50-177">[新規] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="31d50-177">Click New.</span></span>
12. <span data-ttu-id="31d50-178">一覧で、選択された行をマークします。</span><span class="sxs-lookup"><span data-stu-id="31d50-178">In the list, mark the selected row.</span></span>
13. <span data-ttu-id="31d50-179">[コンテナー タイプ] フィールドで、値を入力または選択します。</span><span class="sxs-lookup"><span data-stu-id="31d50-179">In the Container type field, enter or select a value.</span></span>
14. <span data-ttu-id="31d50-180">[保存] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="31d50-180">Click Save.</span></span>
15. <span data-ttu-id="31d50-181">ページを閉じます。</span><span class="sxs-lookup"><span data-stu-id="31d50-181">Close the page.</span></span>

## <a name="set-up-a-container-build-template"></a><span data-ttu-id="31d50-182">コンテナー構築テンプレートのセットアップ</span><span class="sxs-lookup"><span data-stu-id="31d50-182">Set up a container build template</span></span>
1. <span data-ttu-id="31d50-183">[倉庫管理] > [設定] > [コンテナー] > [コンテナー構築テンプレート] の順に移動します。</span><span class="sxs-lookup"><span data-stu-id="31d50-183">Go to Warehouse management > Setup > Containers > Container build templates.</span></span>
2. <span data-ttu-id="31d50-184">[新規] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="31d50-184">Click New.</span></span>
    * <span data-ttu-id="31d50-185">コンテナー構築テンプレートは、どのコンテナー詰めのプロセスが実行されるかに基づきます。</span><span class="sxs-lookup"><span data-stu-id="31d50-185">The container build template is based on which of the containerization processes are performed.</span></span> <span data-ttu-id="31d50-186">各コンテナー構築テンプレートは、ウェーブ テンプレートで使用されるコンテナー詰めのプロセスを定義します。</span><span class="sxs-lookup"><span data-stu-id="31d50-186">Each container build template defines one containerization process that will be used by a wave template.</span></span> <span data-ttu-id="31d50-187">[クエリの編集] オプションで、選択したテンプレートを処理する条件を定義することができます。</span><span class="sxs-lookup"><span data-stu-id="31d50-187">The Edit query option allows you to define the conditions on which the selected template will be processed.</span></span> <span data-ttu-id="31d50-188">たとえば、特定の顧客、製品、または倉庫のコンテナー詰めのみ実行したり、テンプレートに対応するクエリの範囲を追加したりできます。</span><span class="sxs-lookup"><span data-stu-id="31d50-188">For example, you may want to only run containerization for specific customers, products, or warehouses or you can add the corresponding query ranges to the template.</span></span> <span data-ttu-id="31d50-189">[ウェーブ ステップ コード] フィールドは、コンテナー構築テンプレートをウェーブ テンプレートの手順にリンクする方法です。</span><span class="sxs-lookup"><span data-stu-id="31d50-189">The Wave step code field is how a container build template is linked to steps in a wave template.</span></span> <span data-ttu-id="31d50-190">ウェーブが実行されると、コンテナー詰めの開始に使用されるコンテナー構築テンプレートが決まります。</span><span class="sxs-lookup"><span data-stu-id="31d50-190">When a wave is executed, it determines which container build template(s) are used to initiate containerization.</span></span> <span data-ttu-id="31d50-191">[基準クエリのタイプ] フィールドで、梱包内容やフィルターがクエリする基準を決定します。</span><span class="sxs-lookup"><span data-stu-id="31d50-191">The Base query type field determines what to pack and what to base the filter query on.</span></span>  
3. <span data-ttu-id="31d50-192">一覧で、選択された行をマークします。</span><span class="sxs-lookup"><span data-stu-id="31d50-192">In the list, mark the selected row.</span></span>
4. <span data-ttu-id="31d50-193">[コンテナー テンプレート ID] フィールドに値を入力します。</span><span class="sxs-lookup"><span data-stu-id="31d50-193">In the Container template ID field, type a value.</span></span>
5. <span data-ttu-id="31d50-194">[コンテナー グループ ID] フィールドで、値を入力または選択します。</span><span class="sxs-lookup"><span data-stu-id="31d50-194">In the Container group ID field, enter or select a value.</span></span>
6. <span data-ttu-id="31d50-195">[ウェーブ ステップ コード] フィールドに値を入力します。</span><span class="sxs-lookup"><span data-stu-id="31d50-195">In the Wave step code field, type a value.</span></span>
7. <span data-ttu-id="31d50-196">[分割ピッキングを許可する] チェック ボックスをオンにします。</span><span class="sxs-lookup"><span data-stu-id="31d50-196">Select the Allow split picks check box.</span></span>
8. <span data-ttu-id="31d50-197">[保存] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="31d50-197">Click Save.</span></span>
9. <span data-ttu-id="31d50-198">[コンテナー混合制約] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="31d50-198">Click Containier mixing constraints.</span></span>
    * <span data-ttu-id="31d50-199">混合ロジック ブレークで、コンテナーに配賦ラインを梱包するルールを設定できます。</span><span class="sxs-lookup"><span data-stu-id="31d50-199">Mixing logic breaks allows you to set up rules for packing allocation lines in containers.</span></span> <span data-ttu-id="31d50-200">たとえば、品目をコンテナーに割り当てる際に [品目番号] フィールドを追加する場合、新しい品目番号があると新しいコンテナーが作成されます。</span><span class="sxs-lookup"><span data-stu-id="31d50-200">For example, if you add the Item number field, when items are assigned to containers, a new container will be created when there is a new item number.</span></span> <span data-ttu-id="31d50-201">これにより、作業者が同じコンテナーの 2 人の異なる顧客に配賦ラインを梱包することを防ぎます。</span><span class="sxs-lookup"><span data-stu-id="31d50-201">This is will prevent workers from packing allocations lines for two different customers in the same container.</span></span>  
10. <span data-ttu-id="31d50-202">[新規] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="31d50-202">Click New.</span></span>
11. <span data-ttu-id="31d50-203">[テーブル] フィールドで、オプションを選択します。</span><span class="sxs-lookup"><span data-stu-id="31d50-203">In the Table field, select an option.</span></span>
12. <span data-ttu-id="31d50-204">[フィールドの選択] フィールドで、値を入力または選択します。</span><span class="sxs-lookup"><span data-stu-id="31d50-204">In the Field Select field, enter or select a value.</span></span>
13. <span data-ttu-id="31d50-205">[OK] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="31d50-205">Click OK.</span></span>


