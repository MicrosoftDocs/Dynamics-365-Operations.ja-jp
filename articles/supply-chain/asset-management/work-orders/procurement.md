---
title: 調達
description: このトピックでは、資産管理の調達について説明します。
author: josaw1
manager: tfehr
ms.date: 10/15/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: EntAssetWorkOrderPurchaseListPagePreviewPane, EntAssetWorkOrderPurchaseListPage, EntAssetWorkOrderPurchaseLineAmountInfoPart, EntAssetWorkOrderPurchReqListPage
audience: Application User
ms.reviewer: kamaybac
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: riluan
ms.search.validFrom: 2019-09-30
ms.dyn365.ops.version: 10.0.5
ms.openlocfilehash: fce60f6ac2ac0dabe1c0ecd804a1dec1e7e373a2
ms.sourcegitcommit: deac22ba5377a912d93fe408c5ae875706378c2d
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 01/16/2021
ms.locfileid: "5020207"
---
# <a name="procurement"></a><span data-ttu-id="b18ce-103">調達</span><span class="sxs-lookup"><span data-stu-id="b18ce-103">Procurement</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="b18ce-104">資産管理では、作業指示書に関連する購買要求および発注書の概要を取得できます。</span><span class="sxs-lookup"><span data-stu-id="b18ce-104">In Asset Management, you can get an overview of purchase requisitions and purchase orders that are related to work orders.</span></span> <span data-ttu-id="b18ce-105">また、作業指示書から発注書または購買要求を作成することもできます。</span><span class="sxs-lookup"><span data-stu-id="b18ce-105">You can also create a purchase order or a purchase requisition from a work order.</span></span>

<span data-ttu-id="b18ce-106">**作業指示購買要求** の一覧ページ (**資産管理** > **共通** > **調達** > **作業指示購買要求**) で、作業指示書に関連する購買要求の一覧を表示します。</span><span class="sxs-lookup"><span data-stu-id="b18ce-106">The **Work order purchase requisition** list page (**Asset management** > **Common** > **Procurement** > **Work order purchase requisition**) shows a list of purchase requisitions that are related to work orders.</span></span> <span data-ttu-id="b18ce-107">このページで作業指示書のジョブを選択すると、**作業指示書の購買要求** Action Pane タブの **表示** グループにあるボタンを使い、様々なアクションを実行できます。</span><span class="sxs-lookup"><span data-stu-id="b18ce-107">When you select a work order job on this page, you can use the buttons in the **Show** group on the **Work order purchase requisition** Action Pane tab to perform various actions:</span></span>

- <span data-ttu-id="b18ce-108">関連する購買要求を開くには、**購買要求** を選択します。</span><span class="sxs-lookup"><span data-stu-id="b18ce-108">To open the related purchase requisition, select **Purchase requisition**.</span></span> 
- <span data-ttu-id="b18ce-109">関連する作業指示書を開くには、**作業指示書** を選択します。</span><span class="sxs-lookup"><span data-stu-id="b18ce-109">To open the related work order, select **Work order**.</span></span>
- <span data-ttu-id="b18ce-110">資産管理で資産、メンテナンス ジョブ タイプの既定値、予備部品、および作業指示書に関連して、選択した明細行の品目が使用されている場所を示す概要を取得するには、**品目の使用場所** を選択します。</span><span class="sxs-lookup"><span data-stu-id="b18ce-110">To get an overview that shows where the item on the selected line is used in relation to assets, maintenance job type defaults, spare parts, and work orders in Asset Management, select **Item where used**.</span></span> <span data-ttu-id="b18ce-111">この概要の詳細については、[品目の使用場所](../controlling-and-reporting/item-where-used.md) を参照してください。</span><span class="sxs-lookup"><span data-stu-id="b18ce-111">For more information about this overview, see [Item where used](../controlling-and-reporting/item-where-used.md).</span></span>

<span data-ttu-id="b18ce-112">次の図は、**作業指示書の購買要求** の一覧ページの例を示しています。</span><span class="sxs-lookup"><span data-stu-id="b18ce-112">The illustration below shows an example of the **Work order purchase requisition** list page.</span></span>

![図 1](media/08-work-orders.png)


<span data-ttu-id="b18ce-114">**作業指示書の購買** の一覧ページ (**資産管理** > **共通** > **調達** > **作業指示購買要求**) で、作業指示書に関連する発注書の一覧を表示します。</span><span class="sxs-lookup"><span data-stu-id="b18ce-114">The **Work order purchase** list page (**Asset management** > **Common** > **Procurement** > **Work order purchase**) shows a list of purchase orders that are related to work orders.</span></span> <span data-ttu-id="b18ce-115">このページで作業指示書のジョブを選択すると、Action Pane **作業指示書の購買** タブにある **表示** グループのボタンを使い、様々なアクションを実行できます。</span><span class="sxs-lookup"><span data-stu-id="b18ce-115">When you select a work order job on this page, you can use the buttons in the **Show** group on the **Work order purchase** tab of the Action Pane to perform various actions:</span></span>

- <span data-ttu-id="b18ce-116">関連する発注書を開くには、**発注書** を選択します。</span><span class="sxs-lookup"><span data-stu-id="b18ce-116">To open the related purchase order, select **Purchase order**.</span></span> 
- <span data-ttu-id="b18ce-117">関連する作業指示書を開くには、**作業指示書** を選択します。</span><span class="sxs-lookup"><span data-stu-id="b18ce-117">To open the related work order, select **Work order**.</span></span>
- <span data-ttu-id="b18ce-118">資産管理で資産、メンテナンス ジョブ タイプの既定値、予備部品、および作業指示書に関連して、選択した明細行の品目が使用されている場所を示す概要を取得するには、**品目の使用場所** を選択します。</span><span class="sxs-lookup"><span data-stu-id="b18ce-118">To get an overview that shows where the item on the selected line is used in relation to assets, maintenance job type defaults, spare parts, and work orders in Asset Management, select **Item where used**.</span></span> <span data-ttu-id="b18ce-119">この概要の詳細については、[品目の使用場所](../controlling-and-reporting/item-where-used.md) を参照してください。</span><span class="sxs-lookup"><span data-stu-id="b18ce-119">For more information about this overview, see [Item where used](../controlling-and-reporting/item-where-used.md).</span></span>

<span data-ttu-id="b18ce-120">次の図は、**作業指示書の購買** の一覧ページの例を示しています。</span><span class="sxs-lookup"><span data-stu-id="b18ce-120">The illustration below shows an example of the **Work order purchase** list page.</span></span>

![図 2](media/09-work-orders.png)


<span data-ttu-id="b18ce-122">**作業指示書の購買** の一覧 ページと **作業指示書の購買要求** の一覧ページの両方で、配送日の管理に関する記号が各行の右側に表示されます。</span><span class="sxs-lookup"><span data-stu-id="b18ce-122">On both the **Work order purchase** list page and the **Work order purchase requisition** list page, a symbol that is related to delivery date control appears on the right side of each line.</span></span> <span data-ttu-id="b18ce-123">記号に赤い丸の感嘆符が表示されている場合、関連する発注書または購買要求の配送が遅延する可能性があります。</span><span class="sxs-lookup"><span data-stu-id="b18ce-123">If the symbol is an exclamation point in a red circle, delivery of the related purchase order or purchase requisition might be delayed.</span></span>

<span data-ttu-id="b18ce-124">発注書の場合、発注書の明細行に関連する日付を使用して、予想される遅延を計算します。</span><span class="sxs-lookup"><span data-stu-id="b18ce-124">For a purchase order, the date that is related to the purchase order line is used to calculate a possible delay.</span></span> <span data-ttu-id="b18ce-125">この日付を表示するには、**発注書** ページで、発注書の明細行を選択します。</span><span class="sxs-lookup"><span data-stu-id="b18ce-125">To view this date, on the **Purchase order** page, select the purchase order line.</span></span> <span data-ttu-id="b18ce-126">その日付は、**明細行の詳細** クイックタブの **設定** タブにある **出荷日の確認** フィールドに表示されます。</span><span class="sxs-lookup"><span data-stu-id="b18ce-126">The date is shown in the **Confirmed delivery date** field on the **Setup** tab of the **Line details** FastTab.</span></span> <span data-ttu-id="b18ce-127">**出荷日の確認** フィールドが設定されていない場合、**発注書のヘッダー** クイックタブにある **出荷日** フィールドの日付が計算に使用されます。</span><span class="sxs-lookup"><span data-stu-id="b18ce-127">If the **Confirmed delivery date** field isn't set, the date in the **Delivery date** field on the **Purchase order header** FastTab is used for the calculation.</span></span> <span data-ttu-id="b18ce-128">それらの日付の 1 つは、次の順序で、作業指示書または作業指示書のジョブで利用可能な日付と比較されます。</span><span class="sxs-lookup"><span data-stu-id="b18ce-128">One of those dates is compared to the available date on the work order or work order job, in the following order:</span></span>

1. <span data-ttu-id="b18ce-129">作業指示書の実際の開始日</span><span class="sxs-lookup"><span data-stu-id="b18ce-129">Actual start date on the work order</span></span>  

2. <span data-ttu-id="b18ce-130">関連する作業指示ジョブの開始予定日</span><span class="sxs-lookup"><span data-stu-id="b18ce-130">Scheduled start date on the related work order job</span></span> 

3. <span data-ttu-id="b18ce-131">作業指示書の開始予定日</span><span class="sxs-lookup"><span data-stu-id="b18ce-131">Scheduled start date on the work order</span></span> 

4. <span data-ttu-id="b18ce-132">作業指示書の開始予測日</span><span class="sxs-lookup"><span data-stu-id="b18ce-132">Expected start date on the work order</span></span> 

<span data-ttu-id="b18ce-133">購買要求では、**購買要求** ページの **購買要求のヘッダー** クイックタブにある **要求日** フィールドの日付は、起こり得る遅延の計算に使用されます。</span><span class="sxs-lookup"><span data-stu-id="b18ce-133">For a purchase requisition, the date in the **Requested date** field on the **Purchase requisition header** FastTab of the **Purchase requisitions** page is used to calculate a possible delay.</span></span> <span data-ttu-id="b18ce-134">フィールドの日付は、発注書に使用された同じ注文で、作業指示書または作業指示書ジョブで利用可能な日付と比較されます。</span><span class="sxs-lookup"><span data-stu-id="b18ce-134">The date in that field is compared to the available date on the work order or work order job, in the same order that is used for a purchase order.</span></span>


## <a name="create-a-purchase-order-from-a-work-order"></a><span data-ttu-id="b18ce-135">作業指示書から発注書を作成</span><span class="sxs-lookup"><span data-stu-id="b18ce-135">Create a purchase order from a work order</span></span>

<span data-ttu-id="b18ce-136">**すべての作業指示書** の一覧ページで、作業指示書のジョブを選択し、関連する発注書または購買要求を作成できます。</span><span class="sxs-lookup"><span data-stu-id="b18ce-136">On the **All work orders** list page, you can select a work order job, and then create a related purchase order or a related purchase requisition.</span></span> <span data-ttu-id="b18ce-137">この方法は、プロジェクト関係が発注書または購買要求と作業指示書の間に存在していることを保証します。</span><span class="sxs-lookup"><span data-stu-id="b18ce-137">In this way, you help guarantee that project relations exist between the purchase order or purchase requisition and the work order.</span></span>

1. <span data-ttu-id="b18ce-138">**資産管理** > **共通** > **作業指示書** > **すべての作業指示書** または **有効な作業指示書** の順に選択します。</span><span class="sxs-lookup"><span data-stu-id="b18ce-138">Select **Asset management** > **Common** > **Work orders** > **All work orders** or **Active work orders**.</span></span>

2. <span data-ttu-id="b18ce-139">作業指示書を選び、発注書を作成し **編集** を選択します。</span><span class="sxs-lookup"><span data-stu-id="b18ce-139">Select the work order to create a purchase order for, and then select **Edit**.</span></span>

3. <span data-ttu-id="b18ce-140">**作業指示書のメンテナンス作業** クイックタブで、作業指示書ジョブを選び、その発注書を作成します。</span><span class="sxs-lookup"><span data-stu-id="b18ce-140">On the **Work order maintenance jobs** FastTab, select the work order job to create the purchase order for.</span></span>

4. <span data-ttu-id="b18ce-141">**品目作業** > **作業指示書ジョブから発注書** を選択します。</span><span class="sxs-lookup"><span data-stu-id="b18ce-141">Select **Item tasks** > **Purchase order from work order job**.</span></span>

5. <span data-ttu-id="b18ce-142">**プロジェクト発注書** 一覧ページで、**新規** をクリックします。</span><span class="sxs-lookup"><span data-stu-id="b18ce-142">On the **Project purchase orders** list page, click **New**.</span></span>

6. <span data-ttu-id="b18ce-143">発注書を作成します。</span><span class="sxs-lookup"><span data-stu-id="b18ce-143">Create the purchase order.</span></span>

>[!NOTE]
><span data-ttu-id="b18ce-144">関連する購買要求を作成するには、同じ手順を実行します。</span><span class="sxs-lookup"><span data-stu-id="b18ce-144">To create a related purchase requisition, follow the same steps.</span></span> <span data-ttu-id="b18ce-145">ただし、手順 4 で **品目作業** > **作業指示書ジョブから購買要求** を選択します。</span><span class="sxs-lookup"><span data-stu-id="b18ce-145">However, select **Item tasks** > **Purchase requisition from work order job** in step 4.</span></span>


## <a name="project-relation-between-work-order-and-purchase-order-or-purchase-requisition"></a><span data-ttu-id="b18ce-146">作業指示書と購買注文または購買要求間のプロジェクト関係</span><span class="sxs-lookup"><span data-stu-id="b18ce-146">Project relation between work order and purchase order or purchase requisition</span></span>

<span data-ttu-id="b18ce-147">発注書明細行または購買要求明細行は、作業指示プロジェクトおよび関連するプロジェクト活動番号を介して、作業指示ジョブに関連付けられます。</span><span class="sxs-lookup"><span data-stu-id="b18ce-147">A purchase order line or purchase requisition line is related to a work order job via the work order project and the related project activity number.</span></span> <span data-ttu-id="b18ce-148">発注書または購買要求を作業指示ジョブから作成する場合、関連するプロジェクト活動番号が必須になります。</span><span class="sxs-lookup"><span data-stu-id="b18ce-148">When you create a purchase order or purchase requisition from a work order job, the related project activity number is mandatory.</span></span> <span data-ttu-id="b18ce-149">関連する作業指示書のすべての作業指示書ジョブが同じメンテナンス作業タイプを含む場合、プロジェクト活動番号は発注書または購買要求に自動的に入力されます。</span><span class="sxs-lookup"><span data-stu-id="b18ce-149">If all the work order jobs in the related work order have the same maintenance job type, the project activity number is automatically entered on the purchase order or purchase requisition.</span></span> <span data-ttu-id="b18ce-150">作業指示書ジョブが異なるメンテナンス作業タイプを含む場合、プロジェクト活動番号を発注書または購買要求に手動で入力する必要があります。</span><span class="sxs-lookup"><span data-stu-id="b18ce-150">If the work order jobs have different maintenance job types, you must manually enter the project activity number on the purchase order or purchase requisition.</span></span>

<span data-ttu-id="b18ce-151">発注書の明細行に関連付けられている活動番号を表示または入力するには、**作業指示書の購買** 一覧ページで発注書の記録を選び、**発注書** の列で発注書のリンクを選択します。</span><span class="sxs-lookup"><span data-stu-id="b18ce-151">To view or enter the activity number that is related to a purchase order line, on the **Work order purchase** list page, select the purchase order record, and then, in the **Purchase order** column, select the link for the purchase order.</span></span> <span data-ttu-id="b18ce-152">**明細行の詳細** クイックタブの **プロジェクト** タブで、**活動番号** フィールドを参照してください。</span><span class="sxs-lookup"><span data-stu-id="b18ce-152">You can find the **Activity number** field on the **Project** tab of the **Line details** FastTab.</span></span>

<span data-ttu-id="b18ce-153">次の図では **発注書** ページの例を示しており、**活動番号** に焦点を合わせています。</span><span class="sxs-lookup"><span data-stu-id="b18ce-153">The illustration below shows an example of the **Purchase order** page, with focus on the **Activity number**.</span></span>

![図 3](media/10-work-orders.png)

<span data-ttu-id="b18ce-155">同様に、作業指示書における購買要求の明細行に関連付けられている活動番号を表示または入力するには、**作業指示書の購買要求** 一覧ページで購買要求の記録を選び、**購買要求** の列で購買要求のリンクを選択します。</span><span class="sxs-lookup"><span data-stu-id="b18ce-155">Likewise, to view or enter the activity number that is related to a work order purchase requisition line, on the **Work order purchase requisition** list page, select the purchase requisition record, and then, in the **Purchase requisition** column, select the link for the purchase requisition.</span></span> <span data-ttu-id="b18ce-156">**明細行の詳細** クイックタブの **プロジェクト** タブで、**活動番号** フィールドを参照してください。</span><span class="sxs-lookup"><span data-stu-id="b18ce-156">You can find the **Activity number** field on the **Project** tab of the **Line details** FastTab.</span></span>

