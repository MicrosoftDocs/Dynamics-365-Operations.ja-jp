--- 
title: "手動梱包の設定 (2016 年 2 月 & 2016 年 5 月)"
description: "梱包プロセスで、製品を検証してコンテナーに梱包できます。"
author: ShylaThompson
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: WHSLocationProfile, WHSParameters, WHSContainerType, WHSPackProfile, WHSCloseContainerProfile, InventLocationIdLookup, UnitOfMeasureLookup
audience: Application User
ms.reviewer: shylaw
ms.search.scope: Core, Operations
ms.search.region: Global
ms.search.industry: Distribution
ms.author: shylaw
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 0312b8cfadd45f8e59225e9daba78b9e216cff51
ms.openlocfilehash: b90b4a71e2447e942dbb4a9645ef93064da630d3
ms.contentlocale: ja-jp
ms.lasthandoff: 10/16/2018

---
# <a name="set-up-manual-packing-february-2016--may-2016"></a><span data-ttu-id="2147f-103">手動梱包の設定 (2016 年 2 月 & 2016 年 5 月)</span><span class="sxs-lookup"><span data-stu-id="2147f-103">Set up manual packing (February 2016 & May 2016)</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="2147f-104">梱包プロセスで、製品を検証してコンテナーに梱包できます。</span><span class="sxs-lookup"><span data-stu-id="2147f-104">The packing process allows you to validate and pack products into containers.</span></span> <span data-ttu-id="2147f-105">このプロセスでは、倉庫作業者が製品を保管場所から集荷し、品目の数量および種類をチェックする梱包ステーションに移動して、適切なコンテナーに割り当てます。</span><span class="sxs-lookup"><span data-stu-id="2147f-105">In this process, warehouse workers pick products from the storage locations and move them to a packing station where they check the item quantities and types, and assign them to appropriate containers.</span></span> <span data-ttu-id="2147f-106">コンテナーが完全に梱包され、閉じてから出荷ドックに移動されると、製品を出荷する準備が整います。</span><span class="sxs-lookup"><span data-stu-id="2147f-106">When a container is fully packed, they can close it and move it to the outbound docks, and the products are ready to ship.</span></span> <span data-ttu-id="2147f-107">この手順では、USMF というデモ会社を使用します。</span><span class="sxs-lookup"><span data-stu-id="2147f-107">This procedure uses the USMF demo company.</span></span> <span data-ttu-id="2147f-108">この手順は、Dynamics 365 for Operations の2016 年 2 月と 2016 年 5 月のバージョンのみです。</span><span class="sxs-lookup"><span data-stu-id="2147f-108">This procedure is for the February 2016 & May 2016 versions of Dynamics 365 for Operations only.</span></span>


## <a name="set-up-location-profiles"></a><span data-ttu-id="2147f-109">場所プロファイルを設定します</span><span class="sxs-lookup"><span data-stu-id="2147f-109">Set up location profiles</span></span>
1. <span data-ttu-id="2147f-110">[倉庫管理] > [設定] > [倉庫] > [場所プロファイル] の順に移動します。</span><span class="sxs-lookup"><span data-stu-id="2147f-110">Go to Warehouse management > Setup > Warehouse > Location profiles.</span></span>
2. <span data-ttu-id="2147f-111">[新規] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="2147f-111">Click New.</span></span>
    * <span data-ttu-id="2147f-112">場所プロファイルは梱包ステーションに使用され、場所の情報およびルールが含まれます。</span><span class="sxs-lookup"><span data-stu-id="2147f-112">The location profile is used for packing stations and contains information and rules for a location.</span></span>  
3. <span data-ttu-id="2147f-113">[場所プロファイル ID] フィールドに値を入力します。</span><span class="sxs-lookup"><span data-stu-id="2147f-113">In the Location profile ID field, type a value.</span></span>
4. <span data-ttu-id="2147f-114">[名前] フィールドに値を入力します。</span><span class="sxs-lookup"><span data-stu-id="2147f-114">In the Name field, type a value.</span></span>
5. <span data-ttu-id="2147f-115">[場所形式] フィールドで、値を入力または選択します。</span><span class="sxs-lookup"><span data-stu-id="2147f-115">In the Location format field, enter or select a value.</span></span>
6. <span data-ttu-id="2147f-116">[場所タイプ] フィールドで、値を入力または選択します。</span><span class="sxs-lookup"><span data-stu-id="2147f-116">In the Location type field, enter or select a value.</span></span>
7. <span data-ttu-id="2147f-117">[混合保管を許可] フィールドで [はい] を選択します。</span><span class="sxs-lookup"><span data-stu-id="2147f-117">Select Yes in the Allow mixed items field.</span></span>
8. <span data-ttu-id="2147f-118">[混合在庫状態を許可] フィールドで [はい] を選択します。</span><span class="sxs-lookup"><span data-stu-id="2147f-118">Select Yes in the Allow mixed  inventory statuses field.</span></span>
9. <span data-ttu-id="2147f-119">[バッチ日数ルールの上書き] フィールドで [はい] を選択します。</span><span class="sxs-lookup"><span data-stu-id="2147f-119">Select Yes in the Override rules for batch days field.</span></span>
10. <span data-ttu-id="2147f-120">ページを閉じます。</span><span class="sxs-lookup"><span data-stu-id="2147f-120">Close the page.</span></span>

## <a name="set-up-warehouse-management-parameters"></a><span data-ttu-id="2147f-121">倉庫管理パラメーターの設定</span><span class="sxs-lookup"><span data-stu-id="2147f-121">Set up warehouse management parameters</span></span> 
1. <span data-ttu-id="2147f-122">[倉庫管理] > [設定] > [倉庫管理パラメーター] の順に移動します。</span><span class="sxs-lookup"><span data-stu-id="2147f-122">Go to Warehouse management > Setup > Warehouse management parameters.</span></span>
2. <span data-ttu-id="2147f-123">[梱包] タブをクリックします</span><span class="sxs-lookup"><span data-stu-id="2147f-123">Click the Packing tab.</span></span>
3. <span data-ttu-id="2147f-124">[梱包場所のプロファイル ID] フィールドで値を入力するか選択します。</span><span class="sxs-lookup"><span data-stu-id="2147f-124">In the Profile ID for packing location field, enter or select a value.</span></span>
    * <span data-ttu-id="2147f-125">梱包に使用する場所プロファイルを選択します。</span><span class="sxs-lookup"><span data-stu-id="2147f-125">Select the location profile that you want to use for packing.</span></span>  
4. <span data-ttu-id="2147f-126">ページを閉じます。</span><span class="sxs-lookup"><span data-stu-id="2147f-126">Close the page.</span></span>

## <a name="set-up-container-types"></a><span data-ttu-id="2147f-127">コンテナー タイプの設定</span><span class="sxs-lookup"><span data-stu-id="2147f-127">Set up container types</span></span>
1. <span data-ttu-id="2147f-128">[倉庫管理] > [設定] > [コンテナー] > [コンテナー タイプ] の順に移動します。</span><span class="sxs-lookup"><span data-stu-id="2147f-128">Go to Warehouse management > Setup > Containers > Container types.</span></span>
2. <span data-ttu-id="2147f-129">[新規] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="2147f-129">Click New.</span></span>
    * <span data-ttu-id="2147f-130">使用するコンテナー タイプを定義することができます。</span><span class="sxs-lookup"><span data-stu-id="2147f-130">You can define the types of containers to use.</span></span> <span data-ttu-id="2147f-131">風袋重量、最大重量、最大容積、長さ、幅と重量を含むコンテナーの現物分析コードを指定できます。</span><span class="sxs-lookup"><span data-stu-id="2147f-131">You can specify the physical dimensions of the container, including tare weight, maximum weight, maximum volume, length, width, and weight.</span></span>  <span data-ttu-id="2147f-132">属性はコンテナー タイプの予備の分析コードを追加できるようにカスタマイズされたフィールドです。</span><span class="sxs-lookup"><span data-stu-id="2147f-132">The Attributes are customized fields that allow you to add extra dimensions on the container type.</span></span>     
3. <span data-ttu-id="2147f-133">[コンテナー タイプ コード] フィールドに値を入力します。</span><span class="sxs-lookup"><span data-stu-id="2147f-133">In the Container type code field, type a value.</span></span>
4. <span data-ttu-id="2147f-134">[説明] フィールドに値を入力します。</span><span class="sxs-lookup"><span data-stu-id="2147f-134">In the Description field, type a value.</span></span>
5. <span data-ttu-id="2147f-135">[風袋重量] フィールドに数値を入力します。</span><span class="sxs-lookup"><span data-stu-id="2147f-135">In the Tare weight field, enter a number.</span></span>
6. <span data-ttu-id="2147f-136">[最大重量] フィールドに数値を入力します。</span><span class="sxs-lookup"><span data-stu-id="2147f-136">In the Maximum weight field, enter a number.</span></span>
7. <span data-ttu-id="2147f-137">[容積] フィールドに数値を入力します。</span><span class="sxs-lookup"><span data-stu-id="2147f-137">In the Volume field, enter a number.</span></span>
8. <span data-ttu-id="2147f-138">[長さ] フィールドに数値を入力します。</span><span class="sxs-lookup"><span data-stu-id="2147f-138">In the Length field, enter a number.</span></span>
9. <span data-ttu-id="2147f-139">[幅] フィールドに数値を入力します。</span><span class="sxs-lookup"><span data-stu-id="2147f-139">In the Width field, enter a number.</span></span>
10. <span data-ttu-id="2147f-140">[高さ] フィールドに数値を入力します。</span><span class="sxs-lookup"><span data-stu-id="2147f-140">In the Height field, enter a number.</span></span>
11. <span data-ttu-id="2147f-141">[保存] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="2147f-141">Click Save.</span></span>
12. <span data-ttu-id="2147f-142">ページを閉じます。</span><span class="sxs-lookup"><span data-stu-id="2147f-142">Close the page.</span></span>

## <a name="set-up-packing-profiles"></a><span data-ttu-id="2147f-143">梱包プロファイルの設定</span><span class="sxs-lookup"><span data-stu-id="2147f-143">Set up packing profiles</span></span>
1. <span data-ttu-id="2147f-144">[倉庫管理] > [設定] > [梱包] > [梱包プロファイル] の順に移動します。</span><span class="sxs-lookup"><span data-stu-id="2147f-144">Go to Warehouse management > Setup > Packing > Packing profiles.</span></span>
2. <span data-ttu-id="2147f-145">[新規] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="2147f-145">Click New.</span></span>
3. <span data-ttu-id="2147f-146">[梱包プロファイル ID] フィールドに値を入力します。</span><span class="sxs-lookup"><span data-stu-id="2147f-146">In the Packing profile ID field, type a value.</span></span>
4. <span data-ttu-id="2147f-147">[説明] フィールドに値を入力します。</span><span class="sxs-lookup"><span data-stu-id="2147f-147">In the Description field, type a value.</span></span>
5. <span data-ttu-id="2147f-148">[コンテナーを閉じるプロファイル ID] フィールドで値を入力するか選択します。</span><span class="sxs-lookup"><span data-stu-id="2147f-148">In the Container closing profile ID field, enter or select a value.</span></span>
    * <span data-ttu-id="2147f-149">コンテナーを閉じるプロファイル ID はオプションで、この梱包プロファイルの既定の終了コンテナー プロファイルです。</span><span class="sxs-lookup"><span data-stu-id="2147f-149">A container closing profile ID is optional and is the default close container profile for this packing profile.</span></span>  
6. <span data-ttu-id="2147f-150">[コンテナー ID モード] フィールドで、オプションを選択します。</span><span class="sxs-lookup"><span data-stu-id="2147f-150">In the Container ID mode field, select an option.</span></span>
    * <span data-ttu-id="2147f-151">このオプションにより、コンテナーの作成時またはコンテナー ID を手動で作成した場合に、コンテナー ID が自動的に生成されるかどうかが決まります。</span><span class="sxs-lookup"><span data-stu-id="2147f-151">This option determines whether a container ID will be automatically generated when a container is created or if a container ID will be created manually.</span></span>  
7. <span data-ttu-id="2147f-152">[コンテナー タイプ] フィールドで、値を入力または選択します。</span><span class="sxs-lookup"><span data-stu-id="2147f-152">In the Container type field, enter or select a value.</span></span>
    * <span data-ttu-id="2147f-153">コンテナー タイプは、新しいコンテナーの作成時に既定で使用されます。</span><span class="sxs-lookup"><span data-stu-id="2147f-153">The container type will be used by default when a new container is created.</span></span>  
8. <span data-ttu-id="2147f-154">[コンテナーを閉じる時にコンテナーを自動作成] チェック ボックスをオンにします。</span><span class="sxs-lookup"><span data-stu-id="2147f-154">Select the Autocreate container at container close check box.</span></span>
9. <span data-ttu-id="2147f-155">[保存] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="2147f-155">Click Save.</span></span>
10. <span data-ttu-id="2147f-156">ページを閉じます。</span><span class="sxs-lookup"><span data-stu-id="2147f-156">Close the page.</span></span>

## <a name="set-up-container-closing-profiles"></a><span data-ttu-id="2147f-157">コンテナー終了プロファイルの設定</span><span class="sxs-lookup"><span data-stu-id="2147f-157">Set up container closing profiles</span></span>
1. <span data-ttu-id="2147f-158">[倉庫管理] > [設定] > [コンテナー] > [コンテナー終了プロファイル] の順に移動します。</span><span class="sxs-lookup"><span data-stu-id="2147f-158">Go to Warehouse management > Setup > Containers > Container closing profiles.</span></span>
    * <span data-ttu-id="2147f-159">コンテナーを閉じるプロファイルは、コンテナーを締める際の処理を定義します。</span><span class="sxs-lookup"><span data-stu-id="2147f-159">Container closing profiles define what happens when a container is closed.</span></span> <span data-ttu-id="2147f-160">複数の終了コンテナー プロファイルを設定できます。</span><span class="sxs-lookup"><span data-stu-id="2147f-160">You can set up multiple close container profiles.</span></span>       
2. <span data-ttu-id="2147f-161">[新規] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="2147f-161">Click New.</span></span>
3. <span data-ttu-id="2147f-162">[コンテナーを閉じるプロファイル ID] フィールドで値を入力します。</span><span class="sxs-lookup"><span data-stu-id="2147f-162">In the Container closing profile ID field, type a value.</span></span>
4. <span data-ttu-id="2147f-163">[説明] フィールドに値を入力します。</span><span class="sxs-lookup"><span data-stu-id="2147f-163">In the Description field, type a value.</span></span>
5. <span data-ttu-id="2147f-164">[マニフェスト予定日時] フィールドで、オプションを選択します。</span><span class="sxs-lookup"><span data-stu-id="2147f-164">In the Manifest at field, select an option.</span></span>
    * <span data-ttu-id="2147f-165">コンテナー終了時や出荷の確認時にマニフェストを行うかどうかを指定します。</span><span class="sxs-lookup"><span data-stu-id="2147f-165">Specify whether manifesting will occur when closing containers or when confirming the shipment.</span></span> <span data-ttu-id="2147f-166">マニフェストには輸送管理が必要であることに注意してください。</span><span class="sxs-lookup"><span data-stu-id="2147f-166">Note that manifesting requires Transportation management.</span></span> <span data-ttu-id="2147f-167">マニフェストを動作させるためには輸送エンジンに実装する必要があります。</span><span class="sxs-lookup"><span data-stu-id="2147f-167">Manifesting must be implemented in the transportation engines in order for it work.</span></span>  
6. <span data-ttu-id="2147f-168">[倉庫] フィールドで、値を入力または選択します。</span><span class="sxs-lookup"><span data-stu-id="2147f-168">In the Warehouse field, enter or select a value.</span></span>
7. <span data-ttu-id="2147f-169">[最終出荷の既定の場所] フィールドで値を入力するか選択します。</span><span class="sxs-lookup"><span data-stu-id="2147f-169">In the Default location for final shipment field, enter or select a value.</span></span>
    * <span data-ttu-id="2147f-170">これは、コンテナーを閉じた後に移動する場所です。</span><span class="sxs-lookup"><span data-stu-id="2147f-170">This will be location to which products will be moved after the containers are closed.</span></span> <span data-ttu-id="2147f-171">この場所には、倉庫パラメーターで定義された場所プロファイルが必要です。</span><span class="sxs-lookup"><span data-stu-id="2147f-171">This location must have a location profile defined on Warehouse parameters.</span></span>  
8. <span data-ttu-id="2147f-172">[重量単位] フィールドで、値を入力または選択します。</span><span class="sxs-lookup"><span data-stu-id="2147f-172">In the Weight unit field, enter or select a value.</span></span>
9. <span data-ttu-id="2147f-173">[保存] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="2147f-173">Click Save.</span></span>


