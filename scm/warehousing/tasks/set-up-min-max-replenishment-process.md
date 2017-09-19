--- 
title: "最小/最大の補充プロセスの設定"
description: "この手順では、最小/最大の補充方法を使用する新しい補充プロセスを設定する方法を示します。"
author: perlynne
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
ms.author: perlynne
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 663da58ef01b705c0c984fbfd3fce8bc31be04c6
ms.openlocfilehash: 02af5d1beb2d4eb6a7162b47c42854725fbdbec2
ms.contentlocale: ja-jp
ms.lasthandoff: 08/29/2017

---
# <a name="set-up-a-min-max-replenishment-process"></a><span data-ttu-id="068ae-103">最小/最大の補充プロセスの設定</span><span class="sxs-lookup"><span data-stu-id="068ae-103">Set up a min-max replenishment process</span></span>

[!include[task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="068ae-104">この手順では、最小/最大の補充方法を使用する新しい補充プロセスを設定する方法を示します。</span><span class="sxs-lookup"><span data-stu-id="068ae-104">This procedure shows you how to set up a new replenishment process which uses the minimum/maximum replenishment strategy.</span></span> <span data-ttu-id="068ae-105">在庫が最小レベルを下回った場合、場所を補充するために作業が作成されます。</span><span class="sxs-lookup"><span data-stu-id="068ae-105">When inventory falls below the minimum level, work will be created to replenish the location.</span></span> <span data-ttu-id="068ae-106">手順では、在庫が最小レベルを下回った場合でも補充を許可する固定のピッキング場所の使用方法や、バッチ ジョブを使用して定期的に補充プロセスを実行できるようにする方法も示します。</span><span class="sxs-lookup"><span data-stu-id="068ae-106">The procedure also shows how to use fixed picking locations to allow restocking even if inventory falls below the minimum level, and how to enable the replenishment process to run regularly using a batch job.</span></span> <span data-ttu-id="068ae-107">通常、これらのタスクを実施するのは、倉庫マネージャーです。</span><span class="sxs-lookup"><span data-stu-id="068ae-107">These tasks would typically be carried out by a warehouse manager.</span></span> <span data-ttu-id="068ae-108">メモの例の値を使用するデモ データの会社 USMF でこの手順を実行したり、独自のデータで実行したりできます。</span><span class="sxs-lookup"><span data-stu-id="068ae-108">You can run this procedure in the USMF demo data company using the example values in the notes, or can run it on your own data.</span></span> <span data-ttu-id="068ae-109">独自のデータを使用している場合、倉庫管理プロセスに有効な倉庫があることを確認します。</span><span class="sxs-lookup"><span data-stu-id="068ae-109">If you’re using your own data, make sure that you have a warehouse that’s enabled for Warehouse management processes.</span></span>


## <a name="create-a-fixed-picking-location"></a><span data-ttu-id="068ae-110">固定のピッキング場所の作成</span><span class="sxs-lookup"><span data-stu-id="068ae-110">Create a fixed picking location</span></span>
1. <span data-ttu-id="068ae-111">[倉庫管理] > [設定] > [倉庫] > [固定の場所] の順に移動します。</span><span class="sxs-lookup"><span data-stu-id="068ae-111">Go to Warehouse management > Setup > Warehouse > Fixed locations.</span></span>
    * <span data-ttu-id="068ae-112">これは、最小/最大の補充のためのオプションのタスクですが、固定のピッキング場所を使用する場合、システムは残りがなくてもどの品目を補充する必要があるか判断できるため、最小レベルを下回っていても在庫を補充できます。</span><span class="sxs-lookup"><span data-stu-id="068ae-112">This is an optional task for min-max replenishment, but if you use fixed picking location, this allows stock to be replenished even if it falls below the minimum level, because the system can determine which items need to be replenished, even if there aren't any left.</span></span>  
2. <span data-ttu-id="068ae-113">[新規] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="068ae-113">Click New.</span></span>
3. <span data-ttu-id="068ae-114">[品目番号] フィールドで、値を入力または選択します。</span><span class="sxs-lookup"><span data-stu-id="068ae-114">In the Item number field, enter or select a value.</span></span>
    * <span data-ttu-id="068ae-115">USMF を使用すると、品目 A0001 を選択できます。</span><span class="sxs-lookup"><span data-stu-id="068ae-115">If you’re using USMF, you can select item A0001.</span></span>  
4. <span data-ttu-id="068ae-116">[サイト] フィールドで値を入力または選択します。</span><span class="sxs-lookup"><span data-stu-id="068ae-116">In the Site field, enter or select a value.</span></span>
    * <span data-ttu-id="068ae-117">USMF を使用している場合はサイト 2 を選択できます。</span><span class="sxs-lookup"><span data-stu-id="068ae-117">If you’re using USMF, you can select site 2.</span></span>  
5. <span data-ttu-id="068ae-118">[倉庫] フィールドで、値を入力または選択します。</span><span class="sxs-lookup"><span data-stu-id="068ae-118">In the Warehouse field, enter or select a value.</span></span>
    * <span data-ttu-id="068ae-119">USMF を使用している場合は倉庫 24 を選択できます。</span><span class="sxs-lookup"><span data-stu-id="068ae-119">If you’re using USMF, you can select warehouse 24.</span></span>  
6. <span data-ttu-id="068ae-120">[場所] フィールドで値を入力または選択します。</span><span class="sxs-lookup"><span data-stu-id="068ae-120">In the Location field, enter or select a value.</span></span>
    * <span data-ttu-id="068ae-121">USMF を使用している場合、CP-003 を選択できます。</span><span class="sxs-lookup"><span data-stu-id="068ae-121">If you’re using USMF, you can select CP-003.</span></span>  
7. <span data-ttu-id="068ae-122">ページを閉じます。</span><span class="sxs-lookup"><span data-stu-id="068ae-122">Close the page.</span></span>

## <a name="create-a-replenishment-location-directive"></a><span data-ttu-id="068ae-123">補充場所のディレクティブの作成</span><span class="sxs-lookup"><span data-stu-id="068ae-123">Create a replenishment location directive</span></span>
1. <span data-ttu-id="068ae-124">[倉庫管理] > [設定] > [場所のディレクティブ] の順に移動します。</span><span class="sxs-lookup"><span data-stu-id="068ae-124">Go to Warehouse management > Setup > Location directives.</span></span>
    * <span data-ttu-id="068ae-125">場所のディレクティブは、品目がピッキングされる場所を特定するために補充プロセスで使用されます。</span><span class="sxs-lookup"><span data-stu-id="068ae-125">Location directives are used to determine where items should be picked from in the replenishment process.</span></span>  
2. <span data-ttu-id="068ae-126">[ワーク オーダー タイプ] フィールドで、[補充] を選択します。</span><span class="sxs-lookup"><span data-stu-id="068ae-126">In the Work order type field, select 'Replenishment'.</span></span>
3. <span data-ttu-id="068ae-127">[新規] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="068ae-127">Click New.</span></span>
4. <span data-ttu-id="068ae-128">[名前] フィールドに値を入力します。</span><span class="sxs-lookup"><span data-stu-id="068ae-128">In the Name field, type a value.</span></span>
5. <span data-ttu-id="068ae-129">[作業タイプ] フィールドで [ピック] を選択します。</span><span class="sxs-lookup"><span data-stu-id="068ae-129">In the Work type field, select 'Pick'.</span></span>
6. <span data-ttu-id="068ae-130">[サイト] フィールドで値を入力または選択します。</span><span class="sxs-lookup"><span data-stu-id="068ae-130">In the Site field, enter or select a value.</span></span>
    * <span data-ttu-id="068ae-131">USMF を使用している場合はサイト 2 を選択できます。</span><span class="sxs-lookup"><span data-stu-id="068ae-131">If you’re using USMF, you can select site 2.</span></span>  
7. <span data-ttu-id="068ae-132">[倉庫] フィールドで、値を入力または選択します。</span><span class="sxs-lookup"><span data-stu-id="068ae-132">In the Warehouse field, enter or select a value.</span></span>
    * <span data-ttu-id="068ae-133">USMF を使用している場合は倉庫 24 を選択できます。</span><span class="sxs-lookup"><span data-stu-id="068ae-133">If you’re using USMF, you can select warehouse 24.</span></span>  
8. <span data-ttu-id="068ae-134">[保存] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="068ae-134">Click Save.</span></span>
9. <span data-ttu-id="068ae-135">[新規] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="068ae-135">Click New.</span></span>
10. <span data-ttu-id="068ae-136">一覧で、選択された行をマークします。</span><span class="sxs-lookup"><span data-stu-id="068ae-136">In the list, mark the selected row.</span></span>
11. <span data-ttu-id="068ae-137">[上限数量] フィールドに数値を入力します。</span><span class="sxs-lookup"><span data-stu-id="068ae-137">In the To quantity field, enter a number.</span></span>
    * <span data-ttu-id="068ae-138">たとえば、9999 に設定できます。</span><span class="sxs-lookup"><span data-stu-id="068ae-138">For example, you can set it to 9999.</span></span>  
12. <span data-ttu-id="068ae-139">[分割を許可] チェック ボックスをオンにします。</span><span class="sxs-lookup"><span data-stu-id="068ae-139">Select the Allow split check box.</span></span>
    * <span data-ttu-id="068ae-140">このオプションを選択すると、作業作成プロセスによって作業ラインの数量を複数の場所に分割できます。</span><span class="sxs-lookup"><span data-stu-id="068ae-140">If you select this option, the work creation process will allow work line quantities to be split across multiple locations.</span></span>  
13. <span data-ttu-id="068ae-141">[保存] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="068ae-141">Click Save.</span></span>
14. <span data-ttu-id="068ae-142">[新規] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="068ae-142">Click New.</span></span>
15. <span data-ttu-id="068ae-143">一覧で、選択された行をマークします。</span><span class="sxs-lookup"><span data-stu-id="068ae-143">In the list, mark the selected row.</span></span>
16. <span data-ttu-id="068ae-144">[名前] フィールドに値を入力します。</span><span class="sxs-lookup"><span data-stu-id="068ae-144">In the Name field, type a value.</span></span>
17. <span data-ttu-id="068ae-145">[保存] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="068ae-145">Click Save.</span></span>
18. <span data-ttu-id="068ae-146">[クエリの編集] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="068ae-146">Click Edit query.</span></span>
    * <span data-ttu-id="068ae-147">このクエリを編集して在庫が補充プロセスで選択できる制限を追加できます。</span><span class="sxs-lookup"><span data-stu-id="068ae-147">You can edit this query to add restrictions where inventory can be selected from in the replenishment process.</span></span> <span data-ttu-id="068ae-148">たとえば、在庫を倉庫のバルク領域からのみ使用する必要がある場合が考えられます。</span><span class="sxs-lookup"><span data-stu-id="068ae-148">For example, it could be that inventory should only be used from the Bulk area of the warehouse.</span></span>  
19. <span data-ttu-id="068ae-149">[OK] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="068ae-149">Click OK.</span></span>
20. <span data-ttu-id="068ae-150">ページを閉じます。</span><span class="sxs-lookup"><span data-stu-id="068ae-150">Close the page.</span></span>

## <a name="create-a-replenishment-work-template"></a><span data-ttu-id="068ae-151">補充作業テンプレートの作成</span><span class="sxs-lookup"><span data-stu-id="068ae-151">Create a replenishment work template</span></span>
1. <span data-ttu-id="068ae-152">[倉庫管理] > [設定] > [作業] > [作業テンプレート] の順に移動します。</span><span class="sxs-lookup"><span data-stu-id="068ae-152">Go to Warehouse management > Setup > Work > Work templates.</span></span>
    * <span data-ttu-id="068ae-153">作業テンプレートは、最小/最大の補充作業に必要な作成方法についてシステムをガイドするために使用されます。</span><span class="sxs-lookup"><span data-stu-id="068ae-153">The work template is use to guide the system as to how the min/max replenishment work must be created.</span></span> <span data-ttu-id="068ae-154">最小として、ピッキングとプットの作業テンプレート行が必要です。</span><span class="sxs-lookup"><span data-stu-id="068ae-154">As a minimum, there must be a work template line for a pick and a put.</span></span> <span data-ttu-id="068ae-155">作業テンプレートは、必要なすべての情報が入力されるまで無効であることを示します。</span><span class="sxs-lookup"><span data-stu-id="068ae-155">The work template will say that it’s Invalid until all the necessary information has been filled in.</span></span>  
2. <span data-ttu-id="068ae-156">[ワーク オーダー タイプ] フィールドで、[補充] を選択します。</span><span class="sxs-lookup"><span data-stu-id="068ae-156">In the Work order type field, select 'Replenishment'.</span></span>
3. <span data-ttu-id="068ae-157">[新規] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="068ae-157">Click New.</span></span>
4. <span data-ttu-id="068ae-158">[作業テンプレート] フィールドに値を入力します。</span><span class="sxs-lookup"><span data-stu-id="068ae-158">In the Work template field, type a value.</span></span>
5. <span data-ttu-id="068ae-159">[保存] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="068ae-159">Click Save.</span></span>
6. <span data-ttu-id="068ae-160">[新規] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="068ae-160">Click New.</span></span>
7. <span data-ttu-id="068ae-161">[作業タイプ] フィールドで [ピック] を選択します。</span><span class="sxs-lookup"><span data-stu-id="068ae-161">In the Work type field, select 'Pick'.</span></span>
8. <span data-ttu-id="068ae-162">[作業クラス ID] フィールドで、値を入力または選択します。</span><span class="sxs-lookup"><span data-stu-id="068ae-162">In the Work class ID field, enter or select a value.</span></span>
    * <span data-ttu-id="068ae-163">これは、補充に関連付けられた作業クラスである必要があります。</span><span class="sxs-lookup"><span data-stu-id="068ae-163">This should be a work class related to replenishment.</span></span> <span data-ttu-id="068ae-164">USMF を使用している場合は、[補充] を選択します。</span><span class="sxs-lookup"><span data-stu-id="068ae-164">If you’re using USMF, select Replenish.</span></span>  
9. <span data-ttu-id="068ae-165">[新規] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="068ae-165">Click New.</span></span>
10. <span data-ttu-id="068ae-166">一覧で、選択された行をマークします。</span><span class="sxs-lookup"><span data-stu-id="068ae-166">In the list, mark the selected row.</span></span>
11. <span data-ttu-id="068ae-167">[ワーク タイプ] フィールドで [プット] を選択します。</span><span class="sxs-lookup"><span data-stu-id="068ae-167">In the Work type field, select 'Put'.</span></span>
12. <span data-ttu-id="068ae-168">[作業クラス ID] フィールドで、値を入力または選択します。</span><span class="sxs-lookup"><span data-stu-id="068ae-168">In the Work class ID field, enter or select a value.</span></span>
13. <span data-ttu-id="068ae-169">[保存] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="068ae-169">Click Save.</span></span>
14. <span data-ttu-id="068ae-170">ページを閉じます。</span><span class="sxs-lookup"><span data-stu-id="068ae-170">Close the page.</span></span>

## <a name="create-a-new-replenishment-template"></a><span data-ttu-id="068ae-171">新しい補充テンプレートの作成</span><span class="sxs-lookup"><span data-stu-id="068ae-171">Create a new replenishment template</span></span>
1. <span data-ttu-id="068ae-172">[倉庫管理] > [設定] > [補充] > [補充テンプレート] の順に移動します。</span><span class="sxs-lookup"><span data-stu-id="068ae-172">Go to Warehouse management > Setup > Replenishment > Replenishment templates.</span></span>
    * <span data-ttu-id="068ae-173">補充テンプレートは補充する品目と数量、および場所の定義に使用されます。</span><span class="sxs-lookup"><span data-stu-id="068ae-173">The replenishment template is used to define the items and quantities, and the location to replenish.</span></span>  
2. <span data-ttu-id="068ae-174">[新規] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="068ae-174">Click New.</span></span>
3. <span data-ttu-id="068ae-175">[補充テンプレート] フィールドに値を入力します。</span><span class="sxs-lookup"><span data-stu-id="068ae-175">In the Replenish template field, type a value.</span></span>
    * <span data-ttu-id="068ae-176">最小/最大の補充のためであることを示すためにテンプレートに名前を指定します。</span><span class="sxs-lookup"><span data-stu-id="068ae-176">Give the template a name to indicate that it’s for min/max replenishment.</span></span>  
4. <span data-ttu-id="068ae-177">[説明] フィールドに値を入力します。</span><span class="sxs-lookup"><span data-stu-id="068ae-177">In the Description field, type a value.</span></span>
5. <span data-ttu-id="068ae-178">[ウェーブ需要に未引当数量の使用を許可する] チェック ボックスをオンにします。</span><span class="sxs-lookup"><span data-stu-id="068ae-178">Select the Allow wave demand to use unreserved quantities check box.</span></span>
    * <span data-ttu-id="068ae-179">このオプションを選択した場合、ウェーブ要求補充が最小/最大の補充に関連付けられる数量を消費できます。</span><span class="sxs-lookup"><span data-stu-id="068ae-179">If you select this option, it enables wave demand replenishment to consume quantities that are related to min/max replenishment.</span></span> <span data-ttu-id="068ae-180">たとえば、最小/最大の補充作業がすぐに処理されない場合、不要な要求補充作業の作成を回避するのに役立ちます。</span><span class="sxs-lookup"><span data-stu-id="068ae-180">For example, this might be useful if the min/max replenishment work isn’t processed immediately, to avoid unnecessary demand replenishment work from being created.</span></span>  
6. <span data-ttu-id="068ae-181">[新規] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="068ae-181">Click New.</span></span>
7. <span data-ttu-id="068ae-182">[順序番号] フィールドに番号を入力します。</span><span class="sxs-lookup"><span data-stu-id="068ae-182">In the Sequence number field, enter a number.</span></span>
8. <span data-ttu-id="068ae-183">[説明] フィールドに値を入力します。</span><span class="sxs-lookup"><span data-stu-id="068ae-183">In the Description field, type a value.</span></span>
9. <span data-ttu-id="068ae-184">一覧で、選択された行をマークします。</span><span class="sxs-lookup"><span data-stu-id="068ae-184">In the list, mark the selected row.</span></span>
10. <span data-ttu-id="068ae-185">[補充単位] フィールドで値を入力または選択します。</span><span class="sxs-lookup"><span data-stu-id="068ae-185">In the Replenishment unit field, enter or select a value.</span></span>
    * <span data-ttu-id="068ae-186">例えば、pcs を選択します。</span><span class="sxs-lookup"><span data-stu-id="068ae-186">For example, select pcs.</span></span> <span data-ttu-id="068ae-187">この設定は必須です。</span><span class="sxs-lookup"><span data-stu-id="068ae-187">This setting is mandatory.</span></span> <span data-ttu-id="068ae-188">このテンプレートで最小および最大在庫レベルに指定された単位と比較した補充作業の別の測定単位を指定することができます。</span><span class="sxs-lookup"><span data-stu-id="068ae-188">It allows you to specify a different unit of measurement for replenishment work compared to the unit specified for the minimum and maximum stock levels in this template.</span></span>  
11. <span data-ttu-id="068ae-189">[作業テンプレート] フィールドで、値を入力または選択します。</span><span class="sxs-lookup"><span data-stu-id="068ae-189">In the Work template field, enter or select a value.</span></span>
    * <span data-ttu-id="068ae-190">先ほど作成した作業テンプレートを選択します。</span><span class="sxs-lookup"><span data-stu-id="068ae-190">Choose the work template that you created earlier.</span></span>  
12. <span data-ttu-id="068ae-191">[最小数量] フィールドに番号を入力します。</span><span class="sxs-lookup"><span data-stu-id="068ae-191">In the Minimum quantity field, enter a number.</span></span>
    * <span data-ttu-id="068ae-192">補充をトリガーする最小数量を選択します。</span><span class="sxs-lookup"><span data-stu-id="068ae-192">Select the minimum quantity that should trigger the replenishment.</span></span> <span data-ttu-id="068ae-193">たとえば、これを 50 に設定します。</span><span class="sxs-lookup"><span data-stu-id="068ae-193">For example, set this to 50.</span></span> <span data-ttu-id="068ae-194">固定の場所を補充しており、[空の固定の場所を補充する] オプションが [はい] に設定されている場合、この設定をゼロのままにできます。</span><span class="sxs-lookup"><span data-stu-id="068ae-194">It is possible to leave this set to zero, if you’re replenishing a fixed location and the Replenish empty fixed locations option is set to Yes.</span></span> <span data-ttu-id="068ae-195">また、パフォーマンス上の理由から [固定の場所のみを補充する] オプションを選択することををお勧めします。</span><span class="sxs-lookup"><span data-stu-id="068ae-195">We also recommend that you select the Replenish only fixed locations option for performance reasons.</span></span>  
13. <span data-ttu-id="068ae-196">[最大数量] フィールドに番号を入力します。</span><span class="sxs-lookup"><span data-stu-id="068ae-196">In the Maximum quantity field, enter a number.</span></span>
    * <span data-ttu-id="068ae-197">たとえば、これを 100 に設定します。</span><span class="sxs-lookup"><span data-stu-id="068ae-197">For example, set this to 100.</span></span>  
14. <span data-ttu-id="068ae-198">[単位] フィールドで、値を入力または選択します。</span><span class="sxs-lookup"><span data-stu-id="068ae-198">In the Unit field, enter or select a value.</span></span>
    * <span data-ttu-id="068ae-199">最小および最大数量の単位を割り当てます。</span><span class="sxs-lookup"><span data-stu-id="068ae-199">Assign the unit for the minimum and maximum quantities.</span></span> <span data-ttu-id="068ae-200">たとえば、これを pcs に設定します。</span><span class="sxs-lookup"><span data-stu-id="068ae-200">For example, set this to pcs.</span></span>  
15. <span data-ttu-id="068ae-201">[空の固定の場所を補充する] チェック ボックスをオンにします。</span><span class="sxs-lookup"><span data-stu-id="068ae-201">Select the Replenish empty fixed locations check box.</span></span>
    * <span data-ttu-id="068ae-202">空になったとき固定の場所を補充するには、このチェック ボックスをオンにします。</span><span class="sxs-lookup"><span data-stu-id="068ae-202">Select this check box to replenish fixed locations when they are empty.</span></span> <span data-ttu-id="068ae-203">それ以外の場合、手持の数量を持つ場所のみが補充されます。</span><span class="sxs-lookup"><span data-stu-id="068ae-203">Otherwise, only the locations where there is a quantity on hand will be replenished.</span></span>  
16. <span data-ttu-id="068ae-204">[固定の場所のみを補充する] チェック ボックスをオンにします。</span><span class="sxs-lookup"><span data-stu-id="068ae-204">Select the Replenish only fixed locations check box.</span></span>
17. <span data-ttu-id="068ae-205">[製品の選択] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="068ae-205">Click Select products.</span></span>
    * <span data-ttu-id="068ae-206">これは、補充する必要のある製品を定義する場所です。</span><span class="sxs-lookup"><span data-stu-id="068ae-206">This is the place to define which products should be replenished.</span></span> <span data-ttu-id="068ae-207">[固定のピッキング場所] オプションを選択している場合、このクエリの場所も定義する必要があります。</span><span class="sxs-lookup"><span data-stu-id="068ae-207">If the Fixed picking locations option is selected, you also need to define the locations in this query.</span></span> <span data-ttu-id="068ae-208">バリアント固有のクエリが、製品固有のクエリと同様に使用できます。</span><span class="sxs-lookup"><span data-stu-id="068ae-208">Variant-specific queries are available as well product-specific queries.</span></span>  
18. <span data-ttu-id="068ae-209">[品目] の行を選択します。</span><span class="sxs-lookup"><span data-stu-id="068ae-209">Select the Items row.</span></span>
19. <span data-ttu-id="068ae-210">[基準] フィールドに値を入力します。</span><span class="sxs-lookup"><span data-stu-id="068ae-210">In the Criteria field, type a value.</span></span>
    * <span data-ttu-id="068ae-211">固定の場所で補充する必要がある品目を選択します。</span><span class="sxs-lookup"><span data-stu-id="068ae-211">Select the items that should be replenished at the fixed locations.</span></span> <span data-ttu-id="068ae-212">たとえば、A で始まるすべての品目番号を選択するには、A* を入力します。</span><span class="sxs-lookup"><span data-stu-id="068ae-212">For example, type A* to select all item numbers beginning with A.</span></span>  
20. <span data-ttu-id="068ae-213">[追加] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="068ae-213">Click Add.</span></span>
    * <span data-ttu-id="068ae-214">場所エンティティ (存在しない場合) を追加して、倉庫の特定の領域内の固定ピッキング場所への補充作業を制限することができます。</span><span class="sxs-lookup"><span data-stu-id="068ae-214">Add the Location entity (unless it already exists) to be able to restrict the replenishment work to the fixed picking locations within a specific area of the warehouse.</span></span>  
21. <span data-ttu-id="068ae-215">一覧で、選択された行をマークします。</span><span class="sxs-lookup"><span data-stu-id="068ae-215">In the list, mark the selected row.</span></span>
22. <span data-ttu-id="068ae-216">テーブル フィールドを [場所] に設定します。</span><span class="sxs-lookup"><span data-stu-id="068ae-216">Set the Table field to Locations.</span></span>
23. <span data-ttu-id="068ae-217">[フィールド] フィールドで、場所プロファイル ID を選択します。</span><span class="sxs-lookup"><span data-stu-id="068ae-217">In the Field field, select Location profile ID.</span></span>
24. <span data-ttu-id="068ae-218">[基準] フィールドで、値を入力または選択します。</span><span class="sxs-lookup"><span data-stu-id="068ae-218">In the Criteria field, enter or select a value.</span></span>
25. <span data-ttu-id="068ae-219">[OK] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="068ae-219">Click OK.</span></span>
26. <span data-ttu-id="068ae-220">ページを閉じます。</span><span class="sxs-lookup"><span data-stu-id="068ae-220">Close the page.</span></span>

## <a name="set-the-replenishment-process-to-run-as-a-batch-job"></a><span data-ttu-id="068ae-221">バッチ ジョブとして実行する補充プロセスの設定</span><span class="sxs-lookup"><span data-stu-id="068ae-221">Set the replenishment process to run as a batch job</span></span>
1. <span data-ttu-id="068ae-222">[倉庫管理] > [補充] > [補充] の順に移動します。</span><span class="sxs-lookup"><span data-stu-id="068ae-222">Go to Warehouse management > Replenishment > Replenishments.</span></span>
    * <span data-ttu-id="068ae-223">補充ページでバッチ ジョブとして実行したり、手動で開始するように要求したりする補充を設定できます。</span><span class="sxs-lookup"><span data-stu-id="068ae-223">The Replenishments page allows you to set up replenishment to run as a batch job, or to require that it’s started manually.</span></span>  
2. <span data-ttu-id="068ae-224">[フィルター] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="068ae-224">Click Filter.</span></span>
3. <span data-ttu-id="068ae-225">一覧で、選択された行をマークします。</span><span class="sxs-lookup"><span data-stu-id="068ae-225">In the list, mark the selected row.</span></span>
4. <span data-ttu-id="068ae-226">[基準] フィールドで、値を入力または選択します。</span><span class="sxs-lookup"><span data-stu-id="068ae-226">In the Criteria field, enter or select a value.</span></span>
5. <span data-ttu-id="068ae-227">[OK] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="068ae-227">Click OK.</span></span>
6. <span data-ttu-id="068ae-228">[バックグラウンドで実行] セクションを展開します。</span><span class="sxs-lookup"><span data-stu-id="068ae-228">Expand the Run in the background section.</span></span>
7. <span data-ttu-id="068ae-229">[バッチ処理] オプションを [はい] に設定します。</span><span class="sxs-lookup"><span data-stu-id="068ae-229">Set the Batch processing option to Yes.</span></span>
8. <span data-ttu-id="068ae-230">[再実行] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="068ae-230">Click Recurrence.</span></span>
9. <span data-ttu-id="068ae-231">[終了日なし] のオプションを選択します。</span><span class="sxs-lookup"><span data-stu-id="068ae-231">Select the No end date option.</span></span>
10. <span data-ttu-id="068ae-232">定期的なアイテムのパターンを設定します。</span><span class="sxs-lookup"><span data-stu-id="068ae-232">Set the Recurrance pattern.</span></span>
    * <span data-ttu-id="068ae-233">たとえば、日数を選択します。</span><span class="sxs-lookup"><span data-stu-id="068ae-233">For example, select Days.</span></span>  
11. <span data-ttu-id="068ae-234">[OK] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="068ae-234">Click OK.</span></span>
12. <span data-ttu-id="068ae-235">[OK] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="068ae-235">Click OK.</span></span>

