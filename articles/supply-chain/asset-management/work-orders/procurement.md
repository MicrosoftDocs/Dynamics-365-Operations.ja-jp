---
title: 調達
description: このトピックでは、資産管理の調達について説明します。
author: josaw1
manager: AnnBe
ms.date: 08/15/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: mkirknel
ms.search.validFrom: 2019-08-15
ms.dyn365.ops.version: 10.0.5
ms.openlocfilehash: 1678dbe2432e4be46aebb40a12e73dfd695c3e77
ms.sourcegitcommit: f5bfa3212bc3ef7d944a358ef08fe8863fd93b91
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 08/16/2019
ms.locfileid: "1875754"
---
# <a name="procurement"></a><span data-ttu-id="d1386-103">調達</span><span class="sxs-lookup"><span data-stu-id="d1386-103">Procurement</span></span>


[!include [banner](../../includes/banner.md)]

[!include [banner](../../includes/preview-banner.md)]

<span data-ttu-id="d1386-104">資産管理では、作業指示書に関連する購買要求および発注書の概要を取得できます。</span><span class="sxs-lookup"><span data-stu-id="d1386-104">In Asset Management, you can get an overview of purchase requisitions and purchase orders related to work orders.</span></span> <span data-ttu-id="d1386-105">また、作業指示書から発注書または購買要求を作成することもできます。</span><span class="sxs-lookup"><span data-stu-id="d1386-105">It is also possible to create a purchase order or a purchase requisition from a work order.</span></span>

<span data-ttu-id="d1386-106">**作業指示購買要求**の一覧 (**資産管理** > **共通** > **調達** > **作業指示購買要求**) で、作業指示に関連する購買要求の一覧を表示します。</span><span class="sxs-lookup"><span data-stu-id="d1386-106">In the **Work order purchase requisition** list (**Asset management** > **Common** > **Procurement** > **Work order purchase requisition**), you see a list of purchase requisitions related to work orders.</span></span>

- <span data-ttu-id="d1386-107">**作業指示購買要求**の一覧で作業指示ジョブを選択し、**購買要求**ボタンをクリックして、関連する購買要求を開きます。</span><span class="sxs-lookup"><span data-stu-id="d1386-107">Select a work order job in the **Work order purchase requisition** list, and click the **Purchase requisition** button to open the related purchase requisition.</span></span>  
- <span data-ttu-id="d1386-108">**作業指示購買要求**の一覧で作業指示ジョブを選択し、**作業指示**ボタンをクリックして、関連する作業指示書を開きます。</span><span class="sxs-lookup"><span data-stu-id="d1386-108">Select a work order job in the **Work order purchase requisition** list, and click the **Work order** button to open the related work order.</span></span>  
- <span data-ttu-id="d1386-109">選択した明細行の品目が資産管理において、資産、既定のメンテナンス作業タイプ、予備部品、および作業指示書に関連して使用される場所の概要を取得する場合は、**作業指示購買要求**の一覧で作業指示ジョブを選択し、**品目の使用場所**ボタンをクリックします。</span><span class="sxs-lookup"><span data-stu-id="d1386-109">Select a work order job in the **Work order purchase requisition** list, and click the **Item where used** button if you want to get an overview of where the item on the selected line is used in Asset Management in relation to assets, maintenance job type defaults, spare parts, and work orders.</span></span> 

![図 1](media/08-work-orders.png)


<span data-ttu-id="d1386-111">**作業指示購買**の一覧 (**エンタープライズ資産管理** > **共通** > **調達** > **作業指示購買**) で、作業指示書に関連する発注書の一覧を表示できます。</span><span class="sxs-lookup"><span data-stu-id="d1386-111">In the **Work order purchase** list (**Enterprise asset management** > **Common** > **Procurement** > **Work order purchase**), you can see a list of purchase orders related to work orders.</span></span>

- <span data-ttu-id="d1386-112">**作業指示購買**の一覧で作業指示ジョブを選択し、**発注書**ボタンをクリックして、関連する発注書を開きます。</span><span class="sxs-lookup"><span data-stu-id="d1386-112">Select a work order job in the **Work order purchase** list, and click the **Purchase order** button to open the related purchase order.</span></span>  
- <span data-ttu-id="d1386-113">**作業指示購買**の一覧で作業指示ジョブを選択し、**作業指示**ボタンをクリックして、関連する作業指示書を開きます。</span><span class="sxs-lookup"><span data-stu-id="d1386-113">Select a work order job in the **Work order purchase** list, and click the **Work order** button to open the related work order.</span></span>  
- <span data-ttu-id="d1386-114">選択した明細行の品目が資産管理において、資産、既定のメンテナンス作業タイプ、予備部品、および作業指示書に関連して使用される場所の概要を取得する場合は、**作業指示書**の購買一覧で作業指示ジョブを選択し、**品目の使用場所**ボタンをクリックします。</span><span class="sxs-lookup"><span data-stu-id="d1386-114">Select a work order job in the **Work order** purchase list, and click the **Item where used** button if you want to get an overview of where the item on the selected line is used in Asset Management in relation to assets, maintenance job type defaults, spare parts, and work orders.</span></span> 

![図 2](media/09-work-orders.png)


<span data-ttu-id="d1386-116">上記の一覧では、配送日管理に関するアイコンが各行の右側に配置されます。</span><span class="sxs-lookup"><span data-stu-id="d1386-116">In the lists shown above, an icon regarding delivery date control is placed to the right on each line.</span></span> <span data-ttu-id="d1386-117">アイコンに赤い丸の感嘆符が表示されている場合、関連する購買要求または発注書の配送が遅延する可能性を意味します。</span><span class="sxs-lookup"><span data-stu-id="d1386-117">If the icon shows an exclamation mark in a red circle, it means that delivery on the related purchase requisition or purchase order may be delayed.</span></span>

<span data-ttu-id="d1386-118">購買要求では、起こり得る遅延の計算に使用される日付は**購買要求**フォーム > **購買要求ヘッダー** クイック タブ > **要求日**フィールドで検出されます。</span><span class="sxs-lookup"><span data-stu-id="d1386-118">On a purchase requisition, the date used to calculate possible delay is found in the **Purchase requisitions** form > **Purchase requisition header** FastTab > **Requested date** field.</span></span> <span data-ttu-id="d1386-119">この日付は、発注書の日付と同じ方法で、作業指示書または作業指示ジョブで利用可能な日付と比較されます。</span><span class="sxs-lookup"><span data-stu-id="d1386-119">That date is compared to the available date on the work order or work order job in the same way as the purchase order date.</span></span>

<span data-ttu-id="d1386-120">発注書では、起こり得る遅延の計算に使用された日付は発注書明細行に関連付けられた日付となり、**発注書**フォーム > 発注書明細行の選択 > **明細行の詳細**クイック タブ > **設定**タブ >**確認済配送日**フィールドで表示されます。</span><span class="sxs-lookup"><span data-stu-id="d1386-120">On a purchase order, the date used to calculate possible delay is the date related to the purchase order line, which shown in the **Purchase order** form > select purchase order line > **Line details** FastTab > **Setup** tab > **Confirmed delivery date** field.</span></span> <span data-ttu-id="d1386-121">このフィールドが入力されていない場合は、**発注書ヘッダー** クイック タブの**配送日**フィールドの日付が使用されます。</span><span class="sxs-lookup"><span data-stu-id="d1386-121">If that field is not filled out, the date in the **Delivery date** field on the **Purchase order header** FastTab is used.</span></span> <span data-ttu-id="d1386-122">それらの日付の 1 つは、次の順序で、作業指示書または作業指示ジョブで利用可能な日付と比較されます。</span><span class="sxs-lookup"><span data-stu-id="d1386-122">One of those dates is compared to the available date on the work order or work order job in the following order:</span></span>

- <span data-ttu-id="d1386-123">作業指示書の実際の開始日、または</span><span class="sxs-lookup"><span data-stu-id="d1386-123">Actual start date on the work order, or</span></span>  

- <span data-ttu-id="d1386-124">関連する作業指示ジョブの開始予定日、または</span><span class="sxs-lookup"><span data-stu-id="d1386-124">Scheduled start date on the related work order job, or</span></span>  

- <span data-ttu-id="d1386-125">作業指示書の開始予定日、または</span><span class="sxs-lookup"><span data-stu-id="d1386-125">Scheduled start date on the work order, or</span></span>  

- <span data-ttu-id="d1386-126">作業指示書の開始予測日</span><span class="sxs-lookup"><span data-stu-id="d1386-126">Expected start date on the work order</span></span>  


## <a name="create-purchase-order-from-a-work-order"></a><span data-ttu-id="d1386-127">作業指示書から発注書の作成</span><span class="sxs-lookup"><span data-stu-id="d1386-127">Create purchase order from a work order</span></span>

<span data-ttu-id="d1386-128">**すべての作業指示書**で、作業指示ジョブを選択し、関連する発注書または購買要求を作成します。</span><span class="sxs-lookup"><span data-stu-id="d1386-128">In **All Work orders**, you select a work order job and create a related purchase order or a purchase requisition.</span></span> <span data-ttu-id="d1386-129">これは、発注書または購買要求および作業指示書との間のプロジェクト関係を確認するために行われます。</span><span class="sxs-lookup"><span data-stu-id="d1386-129">This is done to ensure project relations between the purchase order or purchase requisition and the work order.</span></span>

1. <span data-ttu-id="d1386-130">**資産管理** > **共通** > **作業指示書** > **すべての作業指示書**または**有効な作業指示書**の順にクリックします。</span><span class="sxs-lookup"><span data-stu-id="d1386-130">Click **Asset management** > **Common** > **Work orders** > **All work orders** or **Active work orders**.</span></span>

2. <span data-ttu-id="d1386-131">**すべての作業指示書**または**有効な作業指示書**の一覧で、発注書を作成する作業指示書を選択し、**編集**をクリックします。</span><span class="sxs-lookup"><span data-stu-id="d1386-131">In the **All work orders** or **Active work orders** list, select the work order for which you want to create a purchase order, and click **Edit**.</span></span>

3. <span data-ttu-id="d1386-132">**作業指示書**フォーム > **作業指示書メンテナンス ジョブ** クイックタブで、発注書を作成する作業指示ジョブを選択します。</span><span class="sxs-lookup"><span data-stu-id="d1386-132">In the **Work order** form > **Work order maintenance jobs** FastTab, select the work order job for which you want to create the purchase order.</span></span>

4. <span data-ttu-id="d1386-133">**品目作業** > **作業指示ジョブから発注書**をクリックします。</span><span class="sxs-lookup"><span data-stu-id="d1386-133">Click **Item tasks** > **Purchase order from work order job**.</span></span>

5. <span data-ttu-id="d1386-134">**プロジェクト発注書**リスト ページで、**新規**をクリックします。</span><span class="sxs-lookup"><span data-stu-id="d1386-134">In the **Project purchase orders** list page, click **New**.</span></span>

6. <span data-ttu-id="d1386-135">発注書を作成します。</span><span class="sxs-lookup"><span data-stu-id="d1386-135">Create the purchase order.</span></span>

>[!NOTE]
><span data-ttu-id="d1386-136">購買要求の作成は、発注書の作成とほぼ同じです。</span><span class="sxs-lookup"><span data-stu-id="d1386-136">Creating a purchase requisition is almost identical to creating a purchase order.</span></span> <span data-ttu-id="d1386-137">上の手順で唯一の違いは、手順 2 で**品目作業** > **作業指示ジョブから発注書**をクリックすることです。</span><span class="sxs-lookup"><span data-stu-id="d1386-137">The only difference is that in the above procedure, you click **Item tasks** > **Purchase requisition from work order job** in step 2.</span></span>

## <a name="project-relation-between-work-order-and-purchase-order-or-purchase-requisition"></a><span data-ttu-id="d1386-138">作業指示書と購買注文または購買要求間のプロジェクト関係</span><span class="sxs-lookup"><span data-stu-id="d1386-138">Project relation between work order and purchase order or purchase requisition</span></span>

<span data-ttu-id="d1386-139">発注書明細行または購買要求明細行は、作業指示プロジェクトおよび関連するプロジェクト活動番号を介して、作業指示ジョブに関連付けられます。</span><span class="sxs-lookup"><span data-stu-id="d1386-139">A purchase order line or purchase requisition line is related to a work order job via the work order project and the related project activity number.</span></span> <span data-ttu-id="d1386-140">発注書または購買要求を作業指示ジョブから作成する場合、関連するプロジェクト活動番号が必須になります。</span><span class="sxs-lookup"><span data-stu-id="d1386-140">When you create a purchase order or purchase requisition from a work order job, the related project activity number is mandatory.</span></span> <span data-ttu-id="d1386-141">関連する作業指示書にすべて同じメンテナンス作業タイプを使用する作業指示ジョブが含まれている場合、プロジェクト活動番号は発注書または購買要求に自動的に挿入されます。</span><span class="sxs-lookup"><span data-stu-id="d1386-141">The project activity number is automatically inserted on a purchase order or purchase requisition if the related work order contains work order jobs that all use the same maintenance job type.</span></span> <span data-ttu-id="d1386-142">作業指示ジョブに異なるメンテナンス作業タイプが含まれている場合、プロジェクト活動番号を手動で挿入する必要があります。</span><span class="sxs-lookup"><span data-stu-id="d1386-142">If the work order jobs contain different maintenance job types, the project activity number must be inserted manually.</span></span>

<span data-ttu-id="d1386-143">発注書明細行に関連する活動番号を表示または挿入するには、**作業指示購買** > 発注書レコードを選択 > **発注書**列で発注書をクリック > **明細行の詳細**クイック タブ > **プロジェクト** タブ > **活動番号**フィールドを開きます。</span><span class="sxs-lookup"><span data-stu-id="d1386-143">To see or insert the activity number related to a purchase order line, open **Work order purchase** > select the purchase order record > click on the purchase order in the **Purchase order** column > **Line details** FastTab > **Project** tab > **Activity number** field.</span></span>


![図 3](media/10-work-orders.png)


<span data-ttu-id="d1386-145">同様に、作業指示購買要求の明細行に関連する活動番号を表示または挿入するには、**作業指示購買要求** > 購買要求レコードを選択 > **購買要求**列で購買要求をクリック > **明細行の詳細**クイック タブ > **プロジェクト** タブ > **活動番号**フィールドを開きます。</span><span class="sxs-lookup"><span data-stu-id="d1386-145">Likewise, to see or insert the activity number related to a work order purchase requisition line, open **Work order purchase requisition** > select the purchase requisition record > click on the purchase requisition in the **Purchase requisition** column > **Line details** FastTab > **Project** tab > **Activity number** field.</span></span>

