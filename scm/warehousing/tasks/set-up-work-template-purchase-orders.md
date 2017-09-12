--- 
title: "発注書の作業テンプレートの設定"
description: "この手順では、入庫済品目のプット アウェイで使用する簡単な作業テンプレートの設定に集中して説明します。"
author: BibiSp
manager: AnnBe
ms.date: 11/14/2016
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
ms.sourcegitcommit: 663da58ef01b705c0c984fbfd3fce8bc31be04c6
ms.openlocfilehash: fbbe019bdca2d5182466a20370418a14032fe63d
ms.contentlocale: ja-jp
ms.lasthandoff: 08/29/2017

---
# <a name="set-up-a-work-template-for-purchase-orders"></a><span data-ttu-id="0067e-103">発注書の作業テンプレートの設定</span><span class="sxs-lookup"><span data-stu-id="0067e-103">Set up a work template for purchase orders</span></span>

[!include[task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="0067e-104">この手順では、入庫済品目のプット アウェイで使用する簡単な作業テンプレートの設定に集中して説明します。</span><span class="sxs-lookup"><span data-stu-id="0067e-104">This procedure focuses on the set up of a simple work template to be used when putting away received items.</span></span> <span data-ttu-id="0067e-105">品目を入庫エリアから移動するときにモバイル デバイスで倉庫作業者に提示される一連の手順が、作業テンプレートによって決まります。</span><span class="sxs-lookup"><span data-stu-id="0067e-105">Work templates determine the set of instructions presented to the warehouse worker on a mobile device when moving items from the receiving area.</span></span> <span data-ttu-id="0067e-106">この手順は、デモ データの会社 USMF で前述のデータを使用して実施できます。</span><span class="sxs-lookup"><span data-stu-id="0067e-106">You can use this procedure with the data mentioned in demo data company USMF.</span></span> <span data-ttu-id="0067e-107">このガイドを開始する前に、作業プール ID を作成します。</span><span class="sxs-lookup"><span data-stu-id="0067e-107">Before you start this guide, create a work pool ID.</span></span> <span data-ttu-id="0067e-108">この例では、入庫で呼び出される作業プール ID を使用します。</span><span class="sxs-lookup"><span data-stu-id="0067e-108">In this example, a work pool ID called in Inbound is used.</span></span> <span data-ttu-id="0067e-109">この手順は、倉庫マネージャーを対象としています。</span><span class="sxs-lookup"><span data-stu-id="0067e-109">This procedure is intended for the warehouse manager.</span></span>

1. <span data-ttu-id="0067e-110">[倉庫管理] > [設定] > [作業] > [作業テンプレート] の順に移動します。</span><span class="sxs-lookup"><span data-stu-id="0067e-110">Go to Warehouse management > Setup > Work > Work templates.</span></span>
2. <span data-ttu-id="0067e-111">[ワーク オーダー タイプ] フィールドで「発注書」を選択します。</span><span class="sxs-lookup"><span data-stu-id="0067e-111">In the Work order type field, select 'Purchase orders'.</span></span>

## <a name="create-a-work-template-header"></a><span data-ttu-id="0067e-112">作業テンプレート ヘッダーの作成</span><span class="sxs-lookup"><span data-stu-id="0067e-112">Create a work template header</span></span>
1. <span data-ttu-id="0067e-113">[新規] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="0067e-113">Click New.</span></span>
2. <span data-ttu-id="0067e-114">[順序番号] フィールドに番号を入力します。</span><span class="sxs-lookup"><span data-stu-id="0067e-114">In the Sequence number field, enter a number.</span></span>
    * <span data-ttu-id="0067e-115">これは、作業のテンプレートが評価される順序です。</span><span class="sxs-lookup"><span data-stu-id="0067e-115">This is the sequence in which the work templates are evaluated.</span></span> <span data-ttu-id="0067e-116">この順序は、必要に応じて修正できます。</span><span class="sxs-lookup"><span data-stu-id="0067e-116">You can modify the sequence, if needed.</span></span>  
3. <span data-ttu-id="0067e-117">[作業テンプレート] フィールドに値を入力します。</span><span class="sxs-lookup"><span data-stu-id="0067e-117">In the Work template field, type a value.</span></span>
    * <span data-ttu-id="0067e-118">これは、このテンプレートの固有識別子です。</span><span class="sxs-lookup"><span data-stu-id="0067e-118">This is the unique identifier for this template.</span></span>  
4. <span data-ttu-id="0067e-119">[作業テンプレートの説明] フィールドで、値を入力します。</span><span class="sxs-lookup"><span data-stu-id="0067e-119">In the Work template description field, type a value.</span></span>
    * <span data-ttu-id="0067e-120">[有効] オプションは、テンプレートに必要とされるすべての情報を入力してから [保存] をクリックするとオンになります。</span><span class="sxs-lookup"><span data-stu-id="0067e-120">The Valid option will not be checked until you’ve completed all the information that's needed by the template and have then clicked Save.</span></span>  
    * <span data-ttu-id="0067e-121">発注書タイプのワーク オーダーは、自動的に処理することはできません。従って [自動的に処理] オプションは [いいえ] に設定しておきます。</span><span class="sxs-lookup"><span data-stu-id="0067e-121">A work order of type Purchase order cannot be automatically processed, so leave the  Automatically process option set to No.</span></span>  
5. <span data-ttu-id="0067e-122">[作業プール ID] フィールドで、値を入力します。</span><span class="sxs-lookup"><span data-stu-id="0067e-122">In the Work pool ID field, type a value.</span></span>
    * <span data-ttu-id="0067e-123">作業プール ID を使用して、作業をグループに整理できます。</span><span class="sxs-lookup"><span data-stu-id="0067e-123">Work pool IDs allow you to organize work into groups.</span></span> <span data-ttu-id="0067e-124">ここで設定する値は、このテンプレートを使用して作成されるすべての作業の既定値になります。</span><span class="sxs-lookup"><span data-stu-id="0067e-124">The value that you set here will be the default value for any work that’s created using this template.</span></span>  
6. <span data-ttu-id="0067e-125">[作業の優先順位] フィールドに「1」を入力します。</span><span class="sxs-lookup"><span data-stu-id="0067e-125">In the Work priority field, enter '1'.</span></span>
    * <span data-ttu-id="0067e-126">これは作業の重要性を示し、ここで設定する値はこのテンプレートを使用して作成されるすべての作業の既定値になります。</span><span class="sxs-lookup"><span data-stu-id="0067e-126">This indicates the importance of the work, and the value that you set here will be the default for any work created using this template.</span></span>  
7. <span data-ttu-id="0067e-127">[保存] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="0067e-127">Click Save.</span></span>
    * <span data-ttu-id="0067e-128">[クエリの編集] が使用できるようになるには、まず作業テンプレートのヘッダーを保存する必要があります。</span><span class="sxs-lookup"><span data-stu-id="0067e-128">You must save the work template header before the Edit Query button becomes available.</span></span>  

## <a name="set-up-the-query-for-the-work-template"></a><span data-ttu-id="0067e-129">作業テンプレート用クエリの設定</span><span class="sxs-lookup"><span data-stu-id="0067e-129">Set up the query for the work template</span></span>
1. <span data-ttu-id="0067e-130">[クエリの編集] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="0067e-130">Click Edit query.</span></span>
    * <span data-ttu-id="0067e-131">特定の倉庫内でのみこのテンプレートを使用できるように制限を設定します。</span><span class="sxs-lookup"><span data-stu-id="0067e-131">We’ll set a limitation that the template can only be used within a specific warehouse.</span></span>  
2. <span data-ttu-id="0067e-132">[追加] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="0067e-132">Click Add.</span></span>
3. <span data-ttu-id="0067e-133">一覧で、選択された行をマークします。</span><span class="sxs-lookup"><span data-stu-id="0067e-133">In the list, mark the selected row.</span></span>
4. <span data-ttu-id="0067e-134">[フィールド] フィールドに「warehouse」と入力します。</span><span class="sxs-lookup"><span data-stu-id="0067e-134">In the Field field, type 'warehouse'.</span></span>
5. <span data-ttu-id="0067e-135">[基準] フィールドに値を入力します。</span><span class="sxs-lookup"><span data-stu-id="0067e-135">In the Criteria field, type a value.</span></span>
6. <span data-ttu-id="0067e-136">[OK] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="0067e-136">Click OK.</span></span>
7. <span data-ttu-id="0067e-137">[はい] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="0067e-137">Click Yes.</span></span>

## <a name="set-work-template-details"></a><span data-ttu-id="0067e-138">作業テンプレートの詳細を設定</span><span class="sxs-lookup"><span data-stu-id="0067e-138">Set work template details</span></span>
1. <span data-ttu-id="0067e-139">[新規] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="0067e-139">Click New.</span></span>
2. <span data-ttu-id="0067e-140">[作業タイプ] フィールドで [ピック] を選択します。</span><span class="sxs-lookup"><span data-stu-id="0067e-140">In the Work type field, select 'Pick'.</span></span>
3. <span data-ttu-id="0067e-141">[作業クラス ID] フィールドに「purchase」と入力します。</span><span class="sxs-lookup"><span data-stu-id="0067e-141">In the Work class ID field, type 'purchase'.</span></span>
    * <span data-ttu-id="0067e-142">ここで設定する作業クラスは、このテンプレートを使用して作成されるピッキング タイプによるすべての作業明細行の既定になります。</span><span class="sxs-lookup"><span data-stu-id="0067e-142">The work class that you set here will be the default on all work lines of type Pick that are created using this template.</span></span> <span data-ttu-id="0067e-143">作業クラスは、ワーク オーダー明細行から上書きできません。</span><span class="sxs-lookup"><span data-stu-id="0067e-143">The work class cannot be overridden from the work order lines.</span></span> <span data-ttu-id="0067e-144">作業クラスは、倉庫作業者がモバイル デバイスで処理できる、ワーク オーダー明細行のタイプを指示または制限するために使用されます。</span><span class="sxs-lookup"><span data-stu-id="0067e-144">Work classes are used to direct and/or limit the type of work order lines a warehouse worker can process on a mobile device.</span></span>  
4. <span data-ttu-id="0067e-145">[新規] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="0067e-145">Click New.</span></span>
5. <span data-ttu-id="0067e-146">[ワーク タイプ] フィールドで [プット] を選択します。</span><span class="sxs-lookup"><span data-stu-id="0067e-146">In the Work type field, select 'Put'.</span></span>
6. <span data-ttu-id="0067e-147">[作業クラス ID] フィールドで、値を入力します。</span><span class="sxs-lookup"><span data-stu-id="0067e-147">In the Work class ID field, type a value.</span></span>
    * <span data-ttu-id="0067e-148">ピッキングとプットの手順は、セットです。</span><span class="sxs-lookup"><span data-stu-id="0067e-148">The pick and put instructions are a set.</span></span> <span data-ttu-id="0067e-149">各ピック/プット セットの作業クラスは同じである必要があります。</span><span class="sxs-lookup"><span data-stu-id="0067e-149">Each pick/put set must have the same work class.</span></span> <span data-ttu-id="0067e-150">ピッキング手順用に用意した同じ作業クラスを使用してください。</span><span class="sxs-lookup"><span data-stu-id="0067e-150">Use the same work class that you provided for the pick instruction.</span></span>  
7. <span data-ttu-id="0067e-151">[保存] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="0067e-151">Click Save.</span></span>
    * <span data-ttu-id="0067e-152">[有効] チェック ボックスがオンになったことに注意してください。</span><span class="sxs-lookup"><span data-stu-id="0067e-152">Note that the Valid checkbox is now checked.</span></span>  


