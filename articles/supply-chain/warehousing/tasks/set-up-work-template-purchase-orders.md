---
title: 発注書の作業テンプレートの設定
description: このトピックでは、入庫済品目のプット アウェイで使用する簡単な作業テンプレートの設定について説明します。
author: ShylaThompson
manager: AnnBe
ms.date: 08/08/2019
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: WHSWorkTemplateTable, SysQueryForm
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.search.region: Global
ms.search.industry: Distribution
ms.author: shylaw
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 227a6865df826caf8ce154f9c44ebe082acd76a5
ms.sourcegitcommit: cbcf344b3b552acca56c3e27606eac7f2f124afe
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 08/22/2019
ms.locfileid: "1916742"
---
# <a name="set-up-a-work-template-for-purchase-orders"></a><span data-ttu-id="31fac-103">発注書の作業テンプレートの設定</span><span class="sxs-lookup"><span data-stu-id="31fac-103">Set up a work template for purchase orders</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="31fac-104">このトピックでは、入庫済品目のプット アウェイで使用する簡単な作業テンプレートの設定について説明します。</span><span class="sxs-lookup"><span data-stu-id="31fac-104">This topic describes how to set up a simple work template to be used when putting away received items.</span></span> <span data-ttu-id="31fac-105">品目を入庫エリアから移動するときにモバイル デバイスで倉庫作業者に提示される一連の手順が、作業テンプレートによって決まります。</span><span class="sxs-lookup"><span data-stu-id="31fac-105">Work templates determine the set of instructions presented to the warehouse worker on a mobile device when moving items from the receiving area.</span></span> <span data-ttu-id="31fac-106">この手順は、デモ データの会社 USMF で前述のデータを使用して実施できます。</span><span class="sxs-lookup"><span data-stu-id="31fac-106">You can use this procedure with the data mentioned in demo data company USMF.</span></span> <span data-ttu-id="31fac-107">このガイドを開始する前に、作業プール ID を作成します。</span><span class="sxs-lookup"><span data-stu-id="31fac-107">Before you start this guide, create a work pool ID.</span></span> <span data-ttu-id="31fac-108">この例では、入庫で呼び出される作業プール ID を使用します。</span><span class="sxs-lookup"><span data-stu-id="31fac-108">In this example, a work pool ID called in Inbound is used.</span></span> <span data-ttu-id="31fac-109">この手順は、倉庫マネージャーを対象としています。</span><span class="sxs-lookup"><span data-stu-id="31fac-109">This procedure is intended for the warehouse manager.</span></span>

1. <span data-ttu-id="31fac-110">ナビゲーション ウィンドウで、**モジュール > 倉庫管理 > 設定 > 作業 > 作業テンプレート**の順に移動します。</span><span class="sxs-lookup"><span data-stu-id="31fac-110">In the navigation pane, go to **Modules > Warehouse management > Setup > Work > Work templates**.</span></span>
2. <span data-ttu-id="31fac-111">**ワーク オーダー タイプ** フィールドで**発注書**を選択します。</span><span class="sxs-lookup"><span data-stu-id="31fac-111">In the **Work order type** field, select **Purchase orders**.</span></span>

## <a name="create-a-work-template-header"></a><span data-ttu-id="31fac-112">作業テンプレート ヘッダーの作成</span><span class="sxs-lookup"><span data-stu-id="31fac-112">Create a work template header</span></span>
1. <span data-ttu-id="31fac-113">**新規** を選択します。</span><span class="sxs-lookup"><span data-stu-id="31fac-113">Select **New**.</span></span>
2. <span data-ttu-id="31fac-114">**順序番号**フィールドに番号を入力します。</span><span class="sxs-lookup"><span data-stu-id="31fac-114">In the **Sequence number** field, enter a number.</span></span> <span data-ttu-id="31fac-115">これは、作業のテンプレートが評価される順序です。</span><span class="sxs-lookup"><span data-stu-id="31fac-115">This is the sequence in which the work templates are evaluated.</span></span> <span data-ttu-id="31fac-116">この順序は、必要に応じて修正できます。</span><span class="sxs-lookup"><span data-stu-id="31fac-116">You can modify the sequence, if needed.</span></span>  
3. <span data-ttu-id="31fac-117">**作業テンプレート** フィールドに値を入力します。</span><span class="sxs-lookup"><span data-stu-id="31fac-117">In the **Work template** field, type a value.</span></span> <span data-ttu-id="31fac-118">これは、このテンプレートの固有識別子です。</span><span class="sxs-lookup"><span data-stu-id="31fac-118">This is the unique identifier for this template.</span></span>  
4. <span data-ttu-id="31fac-119">**作業テンプレートの説明**フィールドで、値を入力します。</span><span class="sxs-lookup"><span data-stu-id="31fac-119">In the **Work template description** field, type a value.</span></span>
    - <span data-ttu-id="31fac-120">**有効**オプションは、テンプレートに必要とされるすべての情報を入力してから**保存**を選択するとオンになります。</span><span class="sxs-lookup"><span data-stu-id="31fac-120">The **Valid** option will not be checked until you’ve completed all the information that's needed by the template and have then selected **Save**.</span></span>  
    - <span data-ttu-id="31fac-121">**発注書**タイプのワーク オーダーは、自動的に処理することはできません。従って**自動的に処理**オプションは**いいえ**に設定しておきます。</span><span class="sxs-lookup"><span data-stu-id="31fac-121">A work order of type **Purchase order** cannot be automatically processed, so leave the **Automatically process** option set to **No**.</span></span>  
5. <span data-ttu-id="31fac-122">**作業プール ID** フィールドで、値を入力します。</span><span class="sxs-lookup"><span data-stu-id="31fac-122">In the **Work pool ID** field, type a value.</span></span> <span data-ttu-id="31fac-123">作業プール ID を使用して、作業をグループに整理できます。</span><span class="sxs-lookup"><span data-stu-id="31fac-123">Work pool IDs allow you to organize work into groups.</span></span> <span data-ttu-id="31fac-124">ここで設定する値は、このテンプレートを使用して作成されるすべての作業の既定値になります。</span><span class="sxs-lookup"><span data-stu-id="31fac-124">The value that you set here will be the default value for any work that’s created using this template.</span></span>  
6. <span data-ttu-id="31fac-125">**作業の優先順位**フィールドに  `1` を入力します。</span><span class="sxs-lookup"><span data-stu-id="31fac-125">In the **Work priority** field, enter `1`.</span></span> <span data-ttu-id="31fac-126">これは作業の重要性を示し、ここで設定する値はこのテンプレートを使用して作成されるすべての作業の既定値になります。</span><span class="sxs-lookup"><span data-stu-id="31fac-126">This indicates the importance of the work, and the value that you set here will be the default for any work created using this template.</span></span>  
7. <span data-ttu-id="31fac-127">**保存** を選択します。</span><span class="sxs-lookup"><span data-stu-id="31fac-127">Select **Save**.</span></span> <span data-ttu-id="31fac-128">**クエリの編集**が使用できるようになるには、まず作業テンプレートのヘッダーを保存する必要があります。</span><span class="sxs-lookup"><span data-stu-id="31fac-128">You must save the work template header before the **Edit Query** button becomes available.</span></span>  

## <a name="set-up-the-query-for-the-work-template"></a><span data-ttu-id="31fac-129">作業テンプレート用クエリの設定</span><span class="sxs-lookup"><span data-stu-id="31fac-129">Set up the query for the work template</span></span>
1. <span data-ttu-id="31fac-130">**クエリの編集**を選択します。</span><span class="sxs-lookup"><span data-stu-id="31fac-130">Select **Edit query**.</span></span> <span data-ttu-id="31fac-131">特定の倉庫内でのみこのテンプレートを使用できるように制限を設定します。</span><span class="sxs-lookup"><span data-stu-id="31fac-131">We’ll set a limitation that the template can only be used within a specific warehouse.</span></span>  
2. <span data-ttu-id="31fac-132">**追加**を選択します。</span><span class="sxs-lookup"><span data-stu-id="31fac-132">Select **Add**.</span></span>
3. <span data-ttu-id="31fac-133">新しい行の**フィールド** フィールドに、`warehouse` と入力します。</span><span class="sxs-lookup"><span data-stu-id="31fac-133">In the **Field** field of the new row, type `warehouse`.</span></span>
4. <span data-ttu-id="31fac-134">**基準**フィールドに値を入力します。</span><span class="sxs-lookup"><span data-stu-id="31fac-134">In the **Criteria** field, type a value.</span></span>
5. <span data-ttu-id="31fac-135">**OK** を選択します。</span><span class="sxs-lookup"><span data-stu-id="31fac-135">Select **OK**.</span></span>
6. <span data-ttu-id="31fac-136">**はい**を選択します。</span><span class="sxs-lookup"><span data-stu-id="31fac-136">Select **Yes**.</span></span>

## <a name="set-work-template-details"></a><span data-ttu-id="31fac-137">作業テンプレートの詳細を設定</span><span class="sxs-lookup"><span data-stu-id="31fac-137">Set work template details</span></span>
1. <span data-ttu-id="31fac-138">**新規** を選択します。</span><span class="sxs-lookup"><span data-stu-id="31fac-138">Select **New**.</span></span>
2. <span data-ttu-id="31fac-139">**作業タイプ** フィールドで**ピック**を選択します。</span><span class="sxs-lookup"><span data-stu-id="31fac-139">In the **Work type** field, select **Pick**.</span></span>
3. <span data-ttu-id="31fac-140">**作業クラス ID** フィールドに `purchase` と入力します。</span><span class="sxs-lookup"><span data-stu-id="31fac-140">In the **Work class ID** field, type `purchase`.</span></span> <span data-ttu-id="31fac-141">ここで設定する作業クラスは、このテンプレートを使用して作成されるピッキング タイプによるすべての作業明細行の既定になります。</span><span class="sxs-lookup"><span data-stu-id="31fac-141">The work class that you set here will be the default on all work lines of type Pick that are created using this template.</span></span> <span data-ttu-id="31fac-142">作業クラスは、ワーク オーダー明細行から上書きできません。</span><span class="sxs-lookup"><span data-stu-id="31fac-142">The work class cannot be overridden from the work order lines.</span></span> <span data-ttu-id="31fac-143">作業クラスは、倉庫作業者がモバイル デバイスで処理できる、ワーク オーダー明細行のタイプを指示または制限するために使用されます。</span><span class="sxs-lookup"><span data-stu-id="31fac-143">Work classes are used to direct and/or limit the type of work order lines a warehouse worker can process on a mobile device.</span></span>  
4. <span data-ttu-id="31fac-144">**新規** を選択します。</span><span class="sxs-lookup"><span data-stu-id="31fac-144">Select **New**.</span></span>
5. <span data-ttu-id="31fac-145">**作業タイプ** フィールドで**プット**を選択します。</span><span class="sxs-lookup"><span data-stu-id="31fac-145">In the **Work type** field, select **Put**.</span></span>
6. <span data-ttu-id="31fac-146">**作業クラス ID** フィールドで、値を入力します。</span><span class="sxs-lookup"><span data-stu-id="31fac-146">In the **Work class ID** field, type a value.</span></span> <span data-ttu-id="31fac-147">ピッキングとプットの手順は、セットです。</span><span class="sxs-lookup"><span data-stu-id="31fac-147">The pick and put instructions are a set.</span></span> <span data-ttu-id="31fac-148">各ピック/プット セットの作業クラスは同じである必要があります。</span><span class="sxs-lookup"><span data-stu-id="31fac-148">Each pick/put set must have the same work class.</span></span> <span data-ttu-id="31fac-149">ピッキング手順用に用意した同じ作業クラスを使用してください。</span><span class="sxs-lookup"><span data-stu-id="31fac-149">Use the same work class that you provided for the pick instruction.</span></span>  
7. <span data-ttu-id="31fac-150">**保存** を選択します。</span><span class="sxs-lookup"><span data-stu-id="31fac-150">Select **Save**.</span></span> <span data-ttu-id="31fac-151">**有効**チェック ボックスがオンになったことに注意してください。</span><span class="sxs-lookup"><span data-stu-id="31fac-151">Note that the **Valid** checkbox is now checked.</span></span>  

