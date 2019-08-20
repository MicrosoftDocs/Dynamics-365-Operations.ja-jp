---
title: 運営リソースの作成
description: プロジェクト活動または生産プロセスを実行する運営リソース。
author: sorenva
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: WrkCtrTable
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: sorenand
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 91f5498bf5a5570c9d3b3f63e0a01b788fa00f35
ms.sourcegitcommit: 8b4b6a9226d4e5f66498ab2a5b4160e26dd112af
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 08/01/2019
ms.locfileid: "1838634"
---
# <a name="create-an-operations-resource"></a><span data-ttu-id="eea72-103">運営リソースの作成</span><span class="sxs-lookup"><span data-stu-id="eea72-103">Create an operations resource</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="eea72-104">プロジェクト活動または生産プロセスを実行する運営リソース。</span><span class="sxs-lookup"><span data-stu-id="eea72-104">An operations resource performs the activities of a project or a production process.</span></span> <span data-ttu-id="eea72-105">この手順では、運営リソースを定義する方法について説明します。</span><span class="sxs-lookup"><span data-stu-id="eea72-105">This procedures shows you how to define an operations resource.</span></span> <span data-ttu-id="eea72-106">デモ データ会社 USMF または独自のデータを使用してこの手順の説明を見ることができます。</span><span class="sxs-lookup"><span data-stu-id="eea72-106">You can walk through this procedure in demo data company USMF, or using your own data.</span></span>

1. <span data-ttu-id="eea72-107">[リソース] に移動します。</span><span class="sxs-lookup"><span data-stu-id="eea72-107">Go to Resources.</span></span>
2. <span data-ttu-id="eea72-108">[新規] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="eea72-108">Click New.</span></span>
3. <span data-ttu-id="eea72-109">[リソース] フィールドに値を入力します。</span><span class="sxs-lookup"><span data-stu-id="eea72-109">In the Resource field, type a value.</span></span>
4. <span data-ttu-id="eea72-110">[説明] フィールドに値を入力します。</span><span class="sxs-lookup"><span data-stu-id="eea72-110">In the Description field, type a value.</span></span>

## <a name="define-capacity-and-consumption-parameters"></a><span data-ttu-id="eea72-111">能力と消費パラメータの定義</span><span class="sxs-lookup"><span data-stu-id="eea72-111">Define capacity and consumption parameters</span></span>
1. <span data-ttu-id="eea72-112">[操作] セクションを展開します。</span><span class="sxs-lookup"><span data-stu-id="eea72-112">Expand the Operation section.</span></span>
2. <span data-ttu-id="eea72-113">[仕損率] フィールドに数値を入力します。</span><span class="sxs-lookup"><span data-stu-id="eea72-113">In the Scrap percentage field, enter a number.</span></span>
3. <span data-ttu-id="eea72-114">[段取りカテゴリ] フィールドで、値を入力または選択します。</span><span class="sxs-lookup"><span data-stu-id="eea72-114">In the Setup category field, enter or select a value.</span></span>
    * <span data-ttu-id="eea72-115">設定の原価を計算する方法を定義する原価カテゴリを指定します。</span><span class="sxs-lookup"><span data-stu-id="eea72-115">Specify the cost category that defines how to account for the cost of setup.</span></span>  
4. <span data-ttu-id="eea72-116">[実行時間カテゴリ] フィールドで、値を入力または選択します。</span><span class="sxs-lookup"><span data-stu-id="eea72-116">In the Run time category field, enter or select a value.</span></span>
    * <span data-ttu-id="eea72-117">実行時間の原価を計算する方法を定義する原価カテゴリを指定します。</span><span class="sxs-lookup"><span data-stu-id="eea72-117">Specify the cost category that defines how to account for the cost of run time.</span></span>  
5. <span data-ttu-id="eea72-118">[数量カテゴリ] フィールドで、値を入力または選択します。</span><span class="sxs-lookup"><span data-stu-id="eea72-118">In the Quantity category field, enter or select a value.</span></span>
    * <span data-ttu-id="eea72-119">出来高数量に基づいてリソース コストを説明する方法を定義する原価カテゴリを指定します。</span><span class="sxs-lookup"><span data-stu-id="eea72-119">Specify the cost category that defines how to account for the resource cost based on the output quantity.</span></span>  
6. <span data-ttu-id="eea72-120">[能力単位] フィールドで、オプションを選択します。</span><span class="sxs-lookup"><span data-stu-id="eea72-120">In the Capacity unit field, select an option.</span></span>
    * <span data-ttu-id="eea72-121">運営リソース能力の表示単位を指定します。</span><span class="sxs-lookup"><span data-stu-id="eea72-121">Specify the unit in which to express the capacity of the operations resource.</span></span>  
7. <span data-ttu-id="eea72-122">[能力] フィールドに数値を入力します。</span><span class="sxs-lookup"><span data-stu-id="eea72-122">In the Capacity field, enter a number.</span></span>
8. <span data-ttu-id="eea72-123">[効率] フィールドに、数値を入力します。</span><span class="sxs-lookup"><span data-stu-id="eea72-123">In the Efficiency percentage field, enter a number.</span></span>
    * <span data-ttu-id="eea72-124">その運営リソースから期待される効率を指定します。</span><span class="sxs-lookup"><span data-stu-id="eea72-124">Specify the efficiency that you expect from the operations resource.</span></span> <span data-ttu-id="eea72-125">効率はリソースのスループットを調整します。これにより、運営リソースに対して予約される時間に影響を与えます。</span><span class="sxs-lookup"><span data-stu-id="eea72-125">The efficiency percentage adjusts the throughput of the operations resource and affects the time that is reserved for the resource.</span></span>  
9. <span data-ttu-id="eea72-126">[工程のスケジューリング率] フィールドに数値を入力します。</span><span class="sxs-lookup"><span data-stu-id="eea72-126">In the Operations scheduling percentage field, enter a number.</span></span>
    * <span data-ttu-id="eea72-127">工程のスケジューリングで使用する運営リソース能力の最大割合を指定します。</span><span class="sxs-lookup"><span data-stu-id="eea72-127">Specify the maximum percentage of capacity of the operations resource that you want to use in operations scheduling.</span></span>  
10. <span data-ttu-id="eea72-128">[有限能力] フィールドで [はい] を選択します。</span><span class="sxs-lookup"><span data-stu-id="eea72-128">Select Yes in the Finite capacity field.</span></span>
    * <span data-ttu-id="eea72-129">利用可能な実際の能力に基づいてスケジュールを立てる場合、かつ既存の確保済能力を考慮する場合は、このオプションを [はい] にします。</span><span class="sxs-lookup"><span data-stu-id="eea72-129">Set this option to Yes if the operations resource should be scheduled based on the actual capacity that is available, and if existing capacity reservations should be considered.</span></span> <span data-ttu-id="eea72-130">このオプションが [いいえ] に設定されている場合、運営リソースには無限の能力があるとされ、リソースが予約超過になることがあります。</span><span class="sxs-lookup"><span data-stu-id="eea72-130">If this option is set to No, the operations resource is assumed to have infinite capacity, and the resource might be overbooked.</span></span>  
11. <span data-ttu-id="eea72-131">[ボトルネック リソース] フィールドで、[はい] を選択します。</span><span class="sxs-lookup"><span data-stu-id="eea72-131">Select Yes in the Bottleneck resource field.</span></span>

## <a name="define-working-times"></a><span data-ttu-id="eea72-132">作業時間の定義</span><span class="sxs-lookup"><span data-stu-id="eea72-132">Define working times</span></span>
1. <span data-ttu-id="eea72-133">[カレンダー] セクションを展開します。</span><span class="sxs-lookup"><span data-stu-id="eea72-133">Expand the Calendars section.</span></span>
2. <span data-ttu-id="eea72-134">[追加] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="eea72-134">Click Add.</span></span>
3. <span data-ttu-id="eea72-135">[カレンダー] フィールドで値を入力または選択します。</span><span class="sxs-lookup"><span data-stu-id="eea72-135">In the Calendar field, enter or select a value.</span></span>
    * <span data-ttu-id="eea72-136">リソースの能力 (時間) で定義した作業時間カレンダーを指定します。</span><span class="sxs-lookup"><span data-stu-id="eea72-136">Specify the working time calendar that defines the capacity (in hours) of the resource.</span></span>  
4. <span data-ttu-id="eea72-137">一覧で、目的のレコードを見つけ、選択します。</span><span class="sxs-lookup"><span data-stu-id="eea72-137">In the list, find and select the desired record.</span></span>
5. <span data-ttu-id="eea72-138">一覧で、選択された行のリンクをクリックします。</span><span class="sxs-lookup"><span data-stu-id="eea72-138">In the list, click the link in the selected row.</span></span>

## <a name="define-resource-capabilities"></a><span data-ttu-id="eea72-139">リソース能力の定義</span><span class="sxs-lookup"><span data-stu-id="eea72-139">Define resource capabilities</span></span>
1. <span data-ttu-id="eea72-140">[処理能力] セクションを展開します。</span><span class="sxs-lookup"><span data-stu-id="eea72-140">Expand the Capabilities section.</span></span>
2. <span data-ttu-id="eea72-141">[追加] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="eea72-141">Click Add.</span></span>
    * <span data-ttu-id="eea72-142">能力とは、運営リソースが特定の活動を実行する能力です。</span><span class="sxs-lookup"><span data-stu-id="eea72-142">A capability is the ability of an operations resource to perform a particular activity.</span></span> <span data-ttu-id="eea72-143">スケジューリング エンジンは、運営リソースの利用可能な能力と各活動のリソース要件が一致するようにリソースを割り当てます。</span><span class="sxs-lookup"><span data-stu-id="eea72-143">The scheduling engine allocates resources by matching the resource requirements of each activity to the capabilities of the available operations resources.</span></span>  
3. <span data-ttu-id="eea72-144">[能力] フィールドで、値を入力または選択します。</span><span class="sxs-lookup"><span data-stu-id="eea72-144">In the Capability field, enter or select a value.</span></span>
4. <span data-ttu-id="eea72-145">[レベル] フィールドに数値を入力します。</span><span class="sxs-lookup"><span data-stu-id="eea72-145">In the Level field, enter a number.</span></span>
    * <span data-ttu-id="eea72-146">リソースが能力を処理する実力レベルを指定します。</span><span class="sxs-lookup"><span data-stu-id="eea72-146">Specify the level of proficiency by which the resource processes the capability.</span></span>  
5. <span data-ttu-id="eea72-147">[優先順位] フィールドに数値を入力します。</span><span class="sxs-lookup"><span data-stu-id="eea72-147">In the Priority field, enter a number.</span></span>
    * <span data-ttu-id="eea72-148">能力に基づいて、運営リソースの優先順位を指定します。</span><span class="sxs-lookup"><span data-stu-id="eea72-148">Specify the priority of the operations resource with respect to the capability.</span></span> <span data-ttu-id="eea72-149">優先順位のスケジューリングの際は、最も優先順位の高い運営リソース (最小の数字) が最初に選択されます。</span><span class="sxs-lookup"><span data-stu-id="eea72-149">When scheduling by priority, the operations resource with the highest priority (lowest numeric value) is selected first.</span></span>  

## <a name="assign-resource-to-resource-group"></a><span data-ttu-id="eea72-150">リソース グループへのリソース割り当て</span><span class="sxs-lookup"><span data-stu-id="eea72-150">Assign resource to resource group</span></span>
1. <span data-ttu-id="eea72-151">[リソース グループ] セクションを展開します。</span><span class="sxs-lookup"><span data-stu-id="eea72-151">Expand the Resource groups section.</span></span>
2. <span data-ttu-id="eea72-152">[追加] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="eea72-152">Click Add.</span></span>
    * <span data-ttu-id="eea72-153">リソース グループとは、運営リソースのサイト、生産単位、および倉庫の環境です。</span><span class="sxs-lookup"><span data-stu-id="eea72-153">The resource group defines the site, production unit, and warehouse context for operations resources.</span></span> <span data-ttu-id="eea72-154">運営リソースは、リソース グループに割り当てられている時、かつそのリソース グループが置かれているサイトでのみスケジューリングできます。</span><span class="sxs-lookup"><span data-stu-id="eea72-154">The operations resource can only be scheduled when assigned to a resource group, and only on the site where the resource group is located.</span></span>  
3. <span data-ttu-id="eea72-155">[リソース グループ] フィールドで、値を入力または選択します。</span><span class="sxs-lookup"><span data-stu-id="eea72-155">In the Resource group field, enter or select a value.</span></span>
4. <span data-ttu-id="eea72-156">[入庫場所] フィールドで、値を入力または選択します。</span><span class="sxs-lookup"><span data-stu-id="eea72-156">In the Input location field, enter or select a value.</span></span>
    * <span data-ttu-id="eea72-157">運営リソースが消費する材料を格納している倉庫の場所を指定します。</span><span class="sxs-lookup"><span data-stu-id="eea72-157">Specify the warehouse location from where the operations resource is consuming materials.</span></span>  

