---
title: 発注書の作業テンプレートの設定
description: このトピックでは、入庫済品目のプット アウェイで使用する簡単な作業テンプレートの設定について説明します。
author: ShylaThompson
manager: tfehr
ms.date: 08/08/2019
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: WHSWorkTemplateTable, SysQueryForm
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.search.industry: Distribution
ms.author: kamaybac
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: e9acf6db9138a009527c6662f1cbb7e5fedc8778
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 01/15/2021
ms.locfileid: "4976866"
---
# <a name="set-up-a-work-template-for-purchase-orders"></a><span data-ttu-id="1a79a-103">発注書の作業テンプレートの設定</span><span class="sxs-lookup"><span data-stu-id="1a79a-103">Set up a work template for purchase orders</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="1a79a-104">このトピックでは、入庫済品目のプット アウェイで使用する簡単な作業テンプレートの設定について説明します。</span><span class="sxs-lookup"><span data-stu-id="1a79a-104">This topic describes how to set up a simple work template to be used when putting away received items.</span></span> <span data-ttu-id="1a79a-105">品目を入庫エリアから移動するときにモバイル デバイスで倉庫作業者に提示される一連の手順が、作業テンプレートによって決まります。</span><span class="sxs-lookup"><span data-stu-id="1a79a-105">Work templates determine the set of instructions presented to the warehouse worker on a mobile device when moving items from the receiving area.</span></span> <span data-ttu-id="1a79a-106">この手順は、デモ データの会社 USMF で前述のデータを使用して実施できます。</span><span class="sxs-lookup"><span data-stu-id="1a79a-106">You can use this procedure with the data mentioned in demo data company USMF.</span></span> <span data-ttu-id="1a79a-107">このガイドを開始する前に、作業プール ID を作成します。</span><span class="sxs-lookup"><span data-stu-id="1a79a-107">Before you start this guide, create a work pool ID.</span></span> <span data-ttu-id="1a79a-108">この例では、入庫で呼び出される作業プール ID を使用します。</span><span class="sxs-lookup"><span data-stu-id="1a79a-108">In this example, a work pool ID called in Inbound is used.</span></span> <span data-ttu-id="1a79a-109">この手順は、倉庫マネージャーを対象としています。</span><span class="sxs-lookup"><span data-stu-id="1a79a-109">This procedure is intended for the warehouse manager.</span></span>

1. <span data-ttu-id="1a79a-110">ナビゲーション ウィンドウで、**モジュール > 倉庫管理 > 設定 > 作業 > 作業テンプレート** の順に移動します。</span><span class="sxs-lookup"><span data-stu-id="1a79a-110">In the navigation pane, go to **Modules > Warehouse management > Setup > Work > Work templates**.</span></span>
2. <span data-ttu-id="1a79a-111">**ワーク オーダー タイプ** フィールドで **発注書** を選択します。</span><span class="sxs-lookup"><span data-stu-id="1a79a-111">In the **Work order type** field, select **Purchase orders**.</span></span>

## <a name="create-a-work-template-header"></a><span data-ttu-id="1a79a-112">作業テンプレート ヘッダーの作成</span><span class="sxs-lookup"><span data-stu-id="1a79a-112">Create a work template header</span></span>
1. <span data-ttu-id="1a79a-113">**新規** を選択します。</span><span class="sxs-lookup"><span data-stu-id="1a79a-113">Select **New**.</span></span>
2. <span data-ttu-id="1a79a-114">**順序番号** フィールドに番号を入力します。</span><span class="sxs-lookup"><span data-stu-id="1a79a-114">In the **Sequence number** field, enter a number.</span></span> <span data-ttu-id="1a79a-115">これは、作業のテンプレートが評価される順序です。</span><span class="sxs-lookup"><span data-stu-id="1a79a-115">This is the sequence in which the work templates are evaluated.</span></span> <span data-ttu-id="1a79a-116">この順序は、必要に応じて修正できます。</span><span class="sxs-lookup"><span data-stu-id="1a79a-116">You can modify the sequence, if needed.</span></span>  
3. <span data-ttu-id="1a79a-117">**作業テンプレート** フィールドに値を入力します。</span><span class="sxs-lookup"><span data-stu-id="1a79a-117">In the **Work template** field, type a value.</span></span> <span data-ttu-id="1a79a-118">これは、このテンプレートの固有識別子です。</span><span class="sxs-lookup"><span data-stu-id="1a79a-118">This is the unique identifier for this template.</span></span>  
4. <span data-ttu-id="1a79a-119">**作業テンプレートの説明** フィールドで、値を入力します。</span><span class="sxs-lookup"><span data-stu-id="1a79a-119">In the **Work template description** field, type a value.</span></span>
    - <span data-ttu-id="1a79a-120">**有効** オプションは、テンプレートに必要とされるすべての情報を入力され、**保存** が選択されるまでチェックマークがつきません。</span><span class="sxs-lookup"><span data-stu-id="1a79a-120">The **Valid** option will not be checked until you've completed all the information that's needed by the template and have then selected **Save**.</span></span>  
    - <span data-ttu-id="1a79a-121">**発注書** タイプのワーク オーダーは、自動的に処理することはできません。従って **自動的に処理** オプションは **いいえ** に設定しておきます。</span><span class="sxs-lookup"><span data-stu-id="1a79a-121">A work order of type **Purchase order** cannot be automatically processed, so leave the **Automatically process** option set to **No**.</span></span>  
5. <span data-ttu-id="1a79a-122">**作業プール ID** フィールドで、値を入力します。</span><span class="sxs-lookup"><span data-stu-id="1a79a-122">In the **Work pool ID** field, type a value.</span></span> <span data-ttu-id="1a79a-123">作業プール ID を使用して、作業をグループに整理できます。</span><span class="sxs-lookup"><span data-stu-id="1a79a-123">Work pool IDs allow you to organize work into groups.</span></span> <span data-ttu-id="1a79a-124">ここで設定する値は、このテンプレートを使用して作成されるすべての作業の既定値になります。</span><span class="sxs-lookup"><span data-stu-id="1a79a-124">The value that you set here will be the default value for any work that's created using this template.</span></span>  
6. <span data-ttu-id="1a79a-125">**作業の優先順位** フィールドに  `1` を入力します。</span><span class="sxs-lookup"><span data-stu-id="1a79a-125">In the **Work priority** field, enter `1`.</span></span> <span data-ttu-id="1a79a-126">これは作業の重要性を示し、ここで設定する値はこのテンプレートを使用して作成されるすべての作業の既定値になります。</span><span class="sxs-lookup"><span data-stu-id="1a79a-126">This indicates the importance of the work, and the value that you set here will be the default for any work created using this template.</span></span>  
7. <span data-ttu-id="1a79a-127">**保存** を選択します。</span><span class="sxs-lookup"><span data-stu-id="1a79a-127">Select **Save**.</span></span> <span data-ttu-id="1a79a-128">**クエリの編集** が使用できるようになるには、まず作業テンプレートのヘッダーを保存する必要があります。</span><span class="sxs-lookup"><span data-stu-id="1a79a-128">You must save the work template header before the **Edit Query** button becomes available.</span></span>  

## <a name="set-up-the-query-for-the-work-template"></a><span data-ttu-id="1a79a-129">作業テンプレート用クエリの設定</span><span class="sxs-lookup"><span data-stu-id="1a79a-129">Set up the query for the work template</span></span>
1. <span data-ttu-id="1a79a-130">**クエリの編集** を選択します。</span><span class="sxs-lookup"><span data-stu-id="1a79a-130">Select **Edit query**.</span></span> <span data-ttu-id="1a79a-131">特定の倉庫内でのみこのテンプレートを使用できるように制限を設定します。</span><span class="sxs-lookup"><span data-stu-id="1a79a-131">We'll set a limitation that the template can only be used within a specific warehouse.</span></span>  
2. <span data-ttu-id="1a79a-132">**追加** を選択します。</span><span class="sxs-lookup"><span data-stu-id="1a79a-132">Select **Add**.</span></span>
3. <span data-ttu-id="1a79a-133">新しい行の **フィールド** フィールドに、`warehouse` と入力します。</span><span class="sxs-lookup"><span data-stu-id="1a79a-133">In the **Field** field of the new row, type `warehouse`.</span></span>
4. <span data-ttu-id="1a79a-134">**基準** フィールドに値を入力します。</span><span class="sxs-lookup"><span data-stu-id="1a79a-134">In the **Criteria** field, type a value.</span></span>
5. <span data-ttu-id="1a79a-135">**OK** を選択します。</span><span class="sxs-lookup"><span data-stu-id="1a79a-135">Select **OK**.</span></span>
6. <span data-ttu-id="1a79a-136">**はい** を選択します。</span><span class="sxs-lookup"><span data-stu-id="1a79a-136">Select **Yes**.</span></span>

## <a name="set-work-template-details"></a><span data-ttu-id="1a79a-137">作業テンプレートの詳細を設定</span><span class="sxs-lookup"><span data-stu-id="1a79a-137">Set work template details</span></span>
1. <span data-ttu-id="1a79a-138">**新規** を選択します。</span><span class="sxs-lookup"><span data-stu-id="1a79a-138">Select **New**.</span></span>
2. <span data-ttu-id="1a79a-139">**作業タイプ** フィールドで **ピック** を選択します。</span><span class="sxs-lookup"><span data-stu-id="1a79a-139">In the **Work type** field, select **Pick**.</span></span>
3. <span data-ttu-id="1a79a-140">**作業クラス ID** フィールドに `purchase` と入力します。</span><span class="sxs-lookup"><span data-stu-id="1a79a-140">In the **Work class ID** field, type `purchase`.</span></span> <span data-ttu-id="1a79a-141">ここで設定する作業クラスは、このテンプレートを使用して作成されるピッキング タイプによるすべての作業明細行の既定になります。</span><span class="sxs-lookup"><span data-stu-id="1a79a-141">The work class that you set here will be the default on all work lines of type Pick that are created using this template.</span></span> <span data-ttu-id="1a79a-142">作業クラスは、ワーク オーダー明細行から上書きできません。</span><span class="sxs-lookup"><span data-stu-id="1a79a-142">The work class cannot be overridden from the work order lines.</span></span> <span data-ttu-id="1a79a-143">作業クラスは、倉庫作業者がモバイル デバイスで処理できる、ワーク オーダー明細行のタイプを指示または制限するために使用されます。</span><span class="sxs-lookup"><span data-stu-id="1a79a-143">Work classes are used to direct and/or limit the type of work order lines a warehouse worker can process on a mobile device.</span></span>  
4. <span data-ttu-id="1a79a-144">**新規** を選択します。</span><span class="sxs-lookup"><span data-stu-id="1a79a-144">Select **New**.</span></span>
5. <span data-ttu-id="1a79a-145">**作業タイプ** フィールドで **プット** を選択します。</span><span class="sxs-lookup"><span data-stu-id="1a79a-145">In the **Work type** field, select **Put**.</span></span>
6. <span data-ttu-id="1a79a-146">**作業クラス ID** フィールドで、値を入力します。</span><span class="sxs-lookup"><span data-stu-id="1a79a-146">In the **Work class ID** field, type a value.</span></span> <span data-ttu-id="1a79a-147">ピッキングとプットの手順は、セットです。</span><span class="sxs-lookup"><span data-stu-id="1a79a-147">The pick and put instructions are a set.</span></span> <span data-ttu-id="1a79a-148">各ピック/プット セットの作業クラスは同じである必要があります。</span><span class="sxs-lookup"><span data-stu-id="1a79a-148">Each pick/put set must have the same work class.</span></span> <span data-ttu-id="1a79a-149">ピッキング手順用に用意した同じ作業クラスを使用してください。</span><span class="sxs-lookup"><span data-stu-id="1a79a-149">Use the same work class that you provided for the pick instruction.</span></span>  
7. <span data-ttu-id="1a79a-150">**保存** を選択します。</span><span class="sxs-lookup"><span data-stu-id="1a79a-150">Select **Save**.</span></span> <span data-ttu-id="1a79a-151">**有効** チェック ボックスがオンになったことに注意してください。</span><span class="sxs-lookup"><span data-stu-id="1a79a-151">Note that the **Valid** checkbox is now checked.</span></span>  

