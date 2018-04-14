--- 
title: "手動の梱包の設定 (2016 年 2 月および 5 月のみ)"
description: "梱包プロセスで、製品を検証してコンテナーに梱包できます。"
author: BibiSp
manager: AnnBe
ms.date: 11/04/2016
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: bis
ms.search.scope: Operations
ms.search.region: Global
ms.search.industry: Distribution
ms.author: bis
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: a8b5a5af5108744406a3d2fb84d7151baea2481b
ms.openlocfilehash: 31b689b6c31563f24892525eed5911af3a35bd51
ms.contentlocale: ja-jp
ms.lasthandoff: 04/13/2018

---
# <a name="set-up-manual-packing-february--may-2016-only"></a><span data-ttu-id="3d70d-103">手動の梱包の設定 (2016 年 2 月および 5 月のみ)</span><span class="sxs-lookup"><span data-stu-id="3d70d-103">Set up manual packing (February & May 2016 only)</span></span>

[!INCLUDE [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="3d70d-104">梱包プロセスで、製品を検証してコンテナーに梱包できます。</span><span class="sxs-lookup"><span data-stu-id="3d70d-104">The packing process allows you to validate and pack products into containers.</span></span> <span data-ttu-id="3d70d-105">このプロセスでは、倉庫作業者が製品を保管場所から集荷し、品目の数量および種類をチェックする梱包ステーションに移動して、適切なコンテナーに割り当てます。</span><span class="sxs-lookup"><span data-stu-id="3d70d-105">In this process, warehouse workers pick products from the storage locations and move them to a packing station where they check the item quantities and types, and assign them to appropriate containers.</span></span> <span data-ttu-id="3d70d-106">コンテナーが完全に梱包され、閉じてから出荷ドックに移動されると、製品を出荷する準備が整います。</span><span class="sxs-lookup"><span data-stu-id="3d70d-106">When a container is fully packed, they can close it and move it to the outbound docks, and the products are ready to ship.</span></span> <span data-ttu-id="3d70d-107">この手順では、USMF というデモ会社を使用します。</span><span class="sxs-lookup"><span data-stu-id="3d70d-107">This procedure uses the USMF demo company.</span></span>


## <a name="set-up-location-profiles"></a><span data-ttu-id="3d70d-108">場所プロファイルを設定します</span><span class="sxs-lookup"><span data-stu-id="3d70d-108">Set up location profiles</span></span>
1. <span data-ttu-id="3d70d-109">[倉庫管理] > [設定] > [倉庫] > [場所プロファイル] の順に移動します。</span><span class="sxs-lookup"><span data-stu-id="3d70d-109">Go to Warehouse management > Setup > Warehouse > Location profiles.</span></span>
2. <span data-ttu-id="3d70d-110">[新規] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="3d70d-110">Click New.</span></span>
    * <span data-ttu-id="3d70d-111">場所プロファイルは梱包ステーションに使用され、場所の情報およびルールが含まれます。</span><span class="sxs-lookup"><span data-stu-id="3d70d-111">The location profile is used for packing stations and contains information and rules for a location.</span></span>  
3. <span data-ttu-id="3d70d-112">[場所プロファイル ID] フィールドに値を入力します。</span><span class="sxs-lookup"><span data-stu-id="3d70d-112">In the Location profile ID field, type a value.</span></span>
4. <span data-ttu-id="3d70d-113">[名前] フィールドに値を入力します。</span><span class="sxs-lookup"><span data-stu-id="3d70d-113">In the Name field, type a value.</span></span>
5. <span data-ttu-id="3d70d-114">[場所形式] フィールドで、値を入力または選択します。</span><span class="sxs-lookup"><span data-stu-id="3d70d-114">In the Location format field, enter or select a value.</span></span>
6. <span data-ttu-id="3d70d-115">[場所タイプ] フィールドで、値を入力または選択します。</span><span class="sxs-lookup"><span data-stu-id="3d70d-115">In the Location type field, enter or select a value.</span></span>
7. <span data-ttu-id="3d70d-116">[混合保管を許可] フィールドで [はい] を選択します。</span><span class="sxs-lookup"><span data-stu-id="3d70d-116">Select Yes in the Allow mixed items field.</span></span>
8. <span data-ttu-id="3d70d-117">[混合在庫状態を許可] フィールドで [はい] を選択します。</span><span class="sxs-lookup"><span data-stu-id="3d70d-117">Select Yes in the Allow mixed  inventory statuses field.</span></span>
9. <span data-ttu-id="3d70d-118">[バッチ日数ルールの上書き] フィールドで [はい] を選択します。</span><span class="sxs-lookup"><span data-stu-id="3d70d-118">Select Yes in the Override rules for batch days field.</span></span>
10. <span data-ttu-id="3d70d-119">ページを閉じます。</span><span class="sxs-lookup"><span data-stu-id="3d70d-119">Close the page.</span></span>

## <a name="set-up-warehouse-management-parameters"></a><span data-ttu-id="3d70d-120">倉庫管理パラメーターの設定</span><span class="sxs-lookup"><span data-stu-id="3d70d-120">Set up warehouse management parameters</span></span> 
1. <span data-ttu-id="3d70d-121">[倉庫管理] > [設定] > [倉庫管理パラメーター] の順に移動します。</span><span class="sxs-lookup"><span data-stu-id="3d70d-121">Go to Warehouse management > Setup > Warehouse management parameters.</span></span>
2. <span data-ttu-id="3d70d-122">[梱包] タブをクリックします</span><span class="sxs-lookup"><span data-stu-id="3d70d-122">Click the Packing tab.</span></span>
3. <span data-ttu-id="3d70d-123">[梱包場所のプロファイル ID] フィールドで値を入力するか選択します。</span><span class="sxs-lookup"><span data-stu-id="3d70d-123">In the Profile ID for packing location field, enter or select a value.</span></span>
    * <span data-ttu-id="3d70d-124">梱包に使用する場所プロファイルを選択します。</span><span class="sxs-lookup"><span data-stu-id="3d70d-124">Select the location profile that you want to use for packing.</span></span>  
4. <span data-ttu-id="3d70d-125">ページを閉じます。</span><span class="sxs-lookup"><span data-stu-id="3d70d-125">Close the page.</span></span>

## <a name="set-up-container-types"></a><span data-ttu-id="3d70d-126">コンテナー タイプの設定</span><span class="sxs-lookup"><span data-stu-id="3d70d-126">Set up container types</span></span>
1. <span data-ttu-id="3d70d-127">[倉庫管理] > [設定] > [コンテナー] > [コンテナー タイプ] の順に移動します。</span><span class="sxs-lookup"><span data-stu-id="3d70d-127">Go to Warehouse management > Setup > Containers > Container types.</span></span>
2. <span data-ttu-id="3d70d-128">[新規] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="3d70d-128">Click New.</span></span>
    * <span data-ttu-id="3d70d-129">使用するコンテナー タイプを定義することができます。</span><span class="sxs-lookup"><span data-stu-id="3d70d-129">You can define the types of containers to use.</span></span> <span data-ttu-id="3d70d-130">風袋重量、最大重量、最大容積、長さ、幅と重量を含むコンテナーの現物分析コードを指定できます。</span><span class="sxs-lookup"><span data-stu-id="3d70d-130">You can specify the physical dimensions of the container, including tare weight, maximum weight, maximum volume, length, width, and weight.</span></span>  <span data-ttu-id="3d70d-131">属性はコンテナー タイプの予備の分析コードを追加できるようにカスタマイズされたフィールドです。</span><span class="sxs-lookup"><span data-stu-id="3d70d-131">The Attributes are customized fields that allow you to add extra dimensions on the container type.</span></span>     
3. <span data-ttu-id="3d70d-132">[コンテナー タイプ コード] フィールドに値を入力します。</span><span class="sxs-lookup"><span data-stu-id="3d70d-132">In the Container type code field, type a value.</span></span>
4. <span data-ttu-id="3d70d-133">[説明] フィールドに値を入力します。</span><span class="sxs-lookup"><span data-stu-id="3d70d-133">In the Description field, type a value.</span></span>
5. <span data-ttu-id="3d70d-134">[風袋重量] フィールドに数値を入力します。</span><span class="sxs-lookup"><span data-stu-id="3d70d-134">In the Tare weight field, enter a number.</span></span>
6. <span data-ttu-id="3d70d-135">[最大重量] フィールドに数値を入力します。</span><span class="sxs-lookup"><span data-stu-id="3d70d-135">In the Maximum weight field, enter a number.</span></span>
7. <span data-ttu-id="3d70d-136">[容積] フィールドに数値を入力します。</span><span class="sxs-lookup"><span data-stu-id="3d70d-136">In the Volume field, enter a number.</span></span>
8. <span data-ttu-id="3d70d-137">[長さ] フィールドに数値を入力します。</span><span class="sxs-lookup"><span data-stu-id="3d70d-137">In the Length field, enter a number.</span></span>
9. <span data-ttu-id="3d70d-138">[幅] フィールドに数値を入力します。</span><span class="sxs-lookup"><span data-stu-id="3d70d-138">In the Width field, enter a number.</span></span>
10. <span data-ttu-id="3d70d-139">[高さ] フィールドに数値を入力します。</span><span class="sxs-lookup"><span data-stu-id="3d70d-139">In the Height field, enter a number.</span></span>
11. <span data-ttu-id="3d70d-140">[保存] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="3d70d-140">Click Save.</span></span>
12. <span data-ttu-id="3d70d-141">ページを閉じます。</span><span class="sxs-lookup"><span data-stu-id="3d70d-141">Close the page.</span></span>

## <a name="set-up-packing-profiles"></a><span data-ttu-id="3d70d-142">梱包プロファイルの設定</span><span class="sxs-lookup"><span data-stu-id="3d70d-142">Set up packing profiles</span></span>
1. <span data-ttu-id="3d70d-143">[倉庫管理] > [設定] > [梱包] > [梱包プロファイル] の順に移動します。</span><span class="sxs-lookup"><span data-stu-id="3d70d-143">Go to Warehouse management > Setup > Packing > Packing profiles.</span></span>
2. <span data-ttu-id="3d70d-144">[新規] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="3d70d-144">Click New.</span></span>
3. <span data-ttu-id="3d70d-145">[梱包プロファイル ID] フィールドに値を入力します。</span><span class="sxs-lookup"><span data-stu-id="3d70d-145">In the Packing profile ID field, type a value.</span></span>
4. <span data-ttu-id="3d70d-146">[説明] フィールドに値を入力します。</span><span class="sxs-lookup"><span data-stu-id="3d70d-146">In the Description field, type a value.</span></span>
5. <span data-ttu-id="3d70d-147">[コンテナーを閉じるプロファイル ID] フィールドで値を入力するか選択します。</span><span class="sxs-lookup"><span data-stu-id="3d70d-147">In the Container closing profile ID field, enter or select a value.</span></span>
    * <span data-ttu-id="3d70d-148">コンテナーを閉じるプロファイル ID はオプションで、この梱包プロファイルの既定の終了コンテナー プロファイルです。</span><span class="sxs-lookup"><span data-stu-id="3d70d-148">A container closing profile ID is optional and is the default close container profile for this packing profile.</span></span>  
6. <span data-ttu-id="3d70d-149">[コンテナー ID モード] フィールドで、オプションを選択します。</span><span class="sxs-lookup"><span data-stu-id="3d70d-149">In the Container ID mode field, select an option.</span></span>
    * <span data-ttu-id="3d70d-150">このオプションにより、コンテナーの作成時またはコンテナー ID を手動で作成した場合に、コンテナー ID が自動的に生成されるかどうかが決まります。</span><span class="sxs-lookup"><span data-stu-id="3d70d-150">This option determines whether a container ID will be automatically generated when a container is created or if a container ID will be created manually.</span></span>  
7. <span data-ttu-id="3d70d-151">[コンテナー タイプ] フィールドで、値を入力または選択します。</span><span class="sxs-lookup"><span data-stu-id="3d70d-151">In the Container type field, enter or select a value.</span></span>
    * <span data-ttu-id="3d70d-152">コンテナー タイプは、新しいコンテナーの作成時に既定で使用されます。</span><span class="sxs-lookup"><span data-stu-id="3d70d-152">The container type will be used by default when a new container is created.</span></span>  
8. <span data-ttu-id="3d70d-153">[コンテナーを閉じる時にコンテナーを自動作成] チェック ボックスをオンにします。</span><span class="sxs-lookup"><span data-stu-id="3d70d-153">Select the Autocreate container at container close check box.</span></span>
9. <span data-ttu-id="3d70d-154">[保存] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="3d70d-154">Click Save.</span></span>
10. <span data-ttu-id="3d70d-155">ページを閉じます。</span><span class="sxs-lookup"><span data-stu-id="3d70d-155">Close the page.</span></span>

## <a name="set-up-container-closing-profiles"></a><span data-ttu-id="3d70d-156">コンテナー終了プロファイルの設定</span><span class="sxs-lookup"><span data-stu-id="3d70d-156">Set up container closing profiles</span></span>
1. <span data-ttu-id="3d70d-157">[倉庫管理] > [設定] > [コンテナー] > [コンテナー終了プロファイル] の順に移動します。</span><span class="sxs-lookup"><span data-stu-id="3d70d-157">Go to Warehouse management > Setup > Containers > Container closing profiles.</span></span>
    * <span data-ttu-id="3d70d-158">コンテナーを閉じるプロファイルは、コンテナーを締める際の処理を定義します。</span><span class="sxs-lookup"><span data-stu-id="3d70d-158">Container closing profiles define what happens when a container is closed.</span></span> <span data-ttu-id="3d70d-159">複数の終了コンテナー プロファイルを設定できます。</span><span class="sxs-lookup"><span data-stu-id="3d70d-159">You can set up multiple close container profiles.</span></span>       
2. <span data-ttu-id="3d70d-160">[新規] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="3d70d-160">Click New.</span></span>
3. <span data-ttu-id="3d70d-161">[コンテナーを閉じるプロファイル ID] フィールドで値を入力します。</span><span class="sxs-lookup"><span data-stu-id="3d70d-161">In the Container closing profile ID field, type a value.</span></span>
4. <span data-ttu-id="3d70d-162">[説明] フィールドに値を入力します。</span><span class="sxs-lookup"><span data-stu-id="3d70d-162">In the Description field, type a value.</span></span>
5. <span data-ttu-id="3d70d-163">[マニフェスト予定日時] フィールドで、オプションを選択します。</span><span class="sxs-lookup"><span data-stu-id="3d70d-163">In the Manifest at field, select an option.</span></span>
    * <span data-ttu-id="3d70d-164">コンテナー終了時や出荷の確認時にマニフェストを行うかどうかを指定します。</span><span class="sxs-lookup"><span data-stu-id="3d70d-164">Specify whether manifesting will occur when closing containers or when confirming the shipment.</span></span> <span data-ttu-id="3d70d-165">マニフェストには輸送管理が必要であることに注意してください。</span><span class="sxs-lookup"><span data-stu-id="3d70d-165">Note that manifesting requires Transportation management.</span></span> <span data-ttu-id="3d70d-166">マニフェストを動作させるためには輸送エンジンに実装する必要があります。</span><span class="sxs-lookup"><span data-stu-id="3d70d-166">Manifesting must be implemented in the transportation engines in order for it work.</span></span>  
6. <span data-ttu-id="3d70d-167">[倉庫] フィールドで、値を入力または選択します。</span><span class="sxs-lookup"><span data-stu-id="3d70d-167">In the Warehouse field, enter or select a value.</span></span>
7. <span data-ttu-id="3d70d-168">[最終出荷の既定の場所] フィールドで値を入力するか選択します。</span><span class="sxs-lookup"><span data-stu-id="3d70d-168">In the Default location for final shipment field, enter or select a value.</span></span>
    * <span data-ttu-id="3d70d-169">これは、コンテナーを閉じた後に移動する場所です。</span><span class="sxs-lookup"><span data-stu-id="3d70d-169">This will be location to which products will be moved after the containers are closed.</span></span> <span data-ttu-id="3d70d-170">この場所には、倉庫パラメーターで定義された場所プロファイルが必要です。</span><span class="sxs-lookup"><span data-stu-id="3d70d-170">This location must have a location profile defined on Warehouse parameters.</span></span>  
8. <span data-ttu-id="3d70d-171">[重量単位] フィールドで、値を入力または選択します。</span><span class="sxs-lookup"><span data-stu-id="3d70d-171">In the Weight unit field, enter or select a value.</span></span>
9. <span data-ttu-id="3d70d-172">[保存] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="3d70d-172">Click Save.</span></span>


