---
title: メンテナンス予測
description: このトピックでは、資産管理におけるメンテナンス予測について説明します。
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
ms.openlocfilehash: 383c910b40199f2da863144c6dc85a579d0091e9
ms.sourcegitcommit: f87de0f949b5d60993b19e0f61297f02d42b5bef
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 09/24/2019
ms.locfileid: "2024502"
---
# <a name="maintenance-forecasts"></a><span data-ttu-id="16c4b-103">メンテナンス予測</span><span class="sxs-lookup"><span data-stu-id="16c4b-103">Maintenance forecasts</span></span>

[!include [banner](../../includes/banner.md)]

[!include [banner](../../includes/preview-banner.md)]


<span data-ttu-id="16c4b-104">作業指示書を作成すると、関連する資産とメンテナンス作業タイプを含む作業指示書ジョブが作成されます。</span><span class="sxs-lookup"><span data-stu-id="16c4b-104">When you create a work order, you create work order jobs with related assets and maintenance job types.</span></span> <span data-ttu-id="16c4b-105">メンテナンス予測を含むメンテナンス作業タイプを選択すると、予測が自動的に作業指示書にコピーされます。</span><span class="sxs-lookup"><span data-stu-id="16c4b-105">When you select a maintenance job type containing maintenance forecasts, the forecasts are automatically copied to the work order.</span></span>

<span data-ttu-id="16c4b-106">作業指示書の予測明細行を追加または削除できる場合があります。</span><span class="sxs-lookup"><span data-stu-id="16c4b-106">You may be able to add or delete forecast lines on a work order.</span></span> <span data-ttu-id="16c4b-107">作業指示書のライフサイクルの状態の設定、関連するプロジェクト タイプ、およびプロジェクト タイプに関連するステージ ルールにより、予測明細行を追加または編集できるかどうかが決まります。</span><span class="sxs-lookup"><span data-stu-id="16c4b-107">The setup of a work order lifecycle state, the related project type, and the stage rules related to the project type determines if you are able to add or edit forecast lines.</span></span> 

1. <span data-ttu-id="16c4b-108">**資産管理** > **共通** > **作業指示書** > **すべての作業指示書**または**有効な作業指示書**の順にクリックします。</span><span class="sxs-lookup"><span data-stu-id="16c4b-108">Click **Asset management** > **Common** > **Work orders** > **All work orders** or **Active work orders**.</span></span>

2. <span data-ttu-id="16c4b-109">リストから作業指示書を選択し、**予測**をクリックします。</span><span class="sxs-lookup"><span data-stu-id="16c4b-109">Select the work order in the list, and click **Forecast**.</span></span> <span data-ttu-id="16c4b-110">**作業指示書のメンテナンス予測**では、作業指示書ジョブで選択したメンテナンス作業タイプからの予測明細行が表示されます。</span><span class="sxs-lookup"><span data-stu-id="16c4b-110">In **Work order maintenance forecast**, forecast lines from the maintenance job type selected on the work order job are displayed.</span></span>


## <a name="add-hours-forecast-to-a-work-order"></a><span data-ttu-id="16c4b-111">作業指示書への時間予測の追加</span><span class="sxs-lookup"><span data-stu-id="16c4b-111">Add hours forecast to a work order</span></span>

1. <span data-ttu-id="16c4b-112">予測追加する作業指示書ジョブを選択します。</span><span class="sxs-lookup"><span data-stu-id="16c4b-112">Select the work order job to which you want to add a forecast.</span></span>

2. <span data-ttu-id="16c4b-113">**時間**クイック タブで、**追加**をクリックして明細行を新規作成します。</span><span class="sxs-lookup"><span data-stu-id="16c4b-113">On the **Hours** FastTab, click **Add** to create a new line.</span></span>

3. <span data-ttu-id="16c4b-114">**カテゴリ** フィールドで、カテゴリを選択します。</span><span class="sxs-lookup"><span data-stu-id="16c4b-114">Select a category in the **Category** field.</span></span>

4. <span data-ttu-id="16c4b-115">**時間**フィールドに予測時間数を挿入します。</span><span class="sxs-lookup"><span data-stu-id="16c4b-115">Insert number of forecasted hours in the **Hours** field.</span></span>

5. <span data-ttu-id="16c4b-116">**明細行プロパティ** フィールドで、明細行に使用する雑費タイプを選択します。</span><span class="sxs-lookup"><span data-stu-id="16c4b-116">In the **Line property** field, select the charge type to be used on the line.</span></span>


## <a name="add-items-forecast-to-a-work-order"></a><span data-ttu-id="16c4b-117">作業指示書への品目予測の追加</span><span class="sxs-lookup"><span data-stu-id="16c4b-117">Add items forecast to a work order</span></span>

<span data-ttu-id="16c4b-118">作業指示書のメンテナンス予測に品目を追加するには、次の 3 つの方法があります。予備部品リストまたは資産 BOM に含まれない品目 (予備部品) の明細行を作成します。承認済みの予備部品リストから予備部品を選択します。資産 BOM から品目を選択します。</span><span class="sxs-lookup"><span data-stu-id="16c4b-118">There are three ways to add items to a work order maintenance forecast: You can create lines for items (spare parts) that are not included in the spare parts list or asset BOM, you can select spare parts from the approved spare parts list, and you can select items from the asset BOM.</span></span>

1. <span data-ttu-id="16c4b-119">予測追加する作業指示書ジョブを選択します。</span><span class="sxs-lookup"><span data-stu-id="16c4b-119">Select the work order job to which you want to add a forecast.</span></span>

2. <span data-ttu-id="16c4b-120">**品目**クイック タブを選択します。</span><span class="sxs-lookup"><span data-stu-id="16c4b-120">Select the **Items** FastTab.</span></span>

3. <span data-ttu-id="16c4b-121">**追加**をクリックして、予備部品リストまたは資産 BOM リストにない予備部品に対して新しい明細行を作成します。</span><span class="sxs-lookup"><span data-stu-id="16c4b-121">Click **Add** to create a new line for a spare part that is not on the spare parts list or the asset BOM list.</span></span>

4. <span data-ttu-id="16c4b-122">**品目番号**フィールドで、品目を選択します。</span><span class="sxs-lookup"><span data-stu-id="16c4b-122">Select the item in the **Item number** field.</span></span>

5. <span data-ttu-id="16c4b-123">**販売数量**フィールドに数量を挿入し、**単位**フィールドで数量単位を選択します。</span><span class="sxs-lookup"><span data-stu-id="16c4b-123">Insert quantity in the **Sales quantity** field, and select a quantity unit in the **Unit** field.</span></span>

6. <span data-ttu-id="16c4b-124">関連するフィールドに原価価格と通貨を挿入し、**明細行プロパティ**を選択します。</span><span class="sxs-lookup"><span data-stu-id="16c4b-124">Insert cost price and currency in the relevant fields, and select a **Line property**.</span></span>

7. <span data-ttu-id="16c4b-125">品目明細行に表示される分析コードの一覧を変更する場合は、**在庫** > **分析コードの表示**をクリックし、分析コードを選択して、**設定の保存**トグル ボタンで「はい」を選択します。</span><span class="sxs-lookup"><span data-stu-id="16c4b-125">If you want to change the list of dimensions displayed on the item lines, click **Inventory** > **Display dimensions**, select the dimensions, and select "Yes" on the **Save setup** toggle button.</span></span>

8. <span data-ttu-id="16c4b-126">承認済み予備部品をメンテナンス予測に追加する場合は、**予備部品の追加**をクリックし、予備部品を選択し、必要に応じて関連情報を編集して **OK** をクリックします。</span><span class="sxs-lookup"><span data-stu-id="16c4b-126">If you want to add an approved spare part to the maintenance forecast, click **Add spare parts**, select the spare part, edit related information if required, and click **OK**.</span></span>

9. <span data-ttu-id="16c4b-127">予測に資産 BOM 品目を追加する場合は、**BOM 品目の追加**をクリックし、品目を選択し、必要に応じて関連情報を編集して **OK** をクリックします。</span><span class="sxs-lookup"><span data-stu-id="16c4b-127">If you want to add asset BOM items to the forecast, click **Add BOM items**, select the item, edit related information if required, and click **OK**.</span></span>

10. <span data-ttu-id="16c4b-128">選択した明細行の品目が資産管理において、資産、メンテナンス作業タイプの既定、予備部品、および作業指示書に関連して使用される場所の概要を取得する場合は、**品目の使用場所**をクリックします。</span><span class="sxs-lookup"><span data-stu-id="16c4b-128">Click **Item where used** if you want to get an overview of where the item on the selected line is used in Asset Management in relation to assets, maintenance job type defaults, spare parts, and work orders.</span></span> 



## <a name="add-expense-forecast-to-a-work-order"></a><span data-ttu-id="16c4b-129">作業指示書への経費予測の追加</span><span class="sxs-lookup"><span data-stu-id="16c4b-129">Add expense forecast to a work order</span></span>

1. <span data-ttu-id="16c4b-130">このトピックでは、作業指示書に経費予測を追加する方法について説明します。</span><span class="sxs-lookup"><span data-stu-id="16c4b-130">This topic explains how to add an expense forecast to a work order.</span></span> <span data-ttu-id="16c4b-131">フォームの左側で、予測を追加する作業指示書ジョブを選択します。</span><span class="sxs-lookup"><span data-stu-id="16c4b-131">In the left-hand side of the form, select the work order job to which you want to add a forecast.</span></span>

2. <span data-ttu-id="16c4b-132">**経費**クイック タブを選択します。</span><span class="sxs-lookup"><span data-stu-id="16c4b-132">Select the **Expense** FastTab.</span></span>

3. <span data-ttu-id="16c4b-133">新しい明細行を作成するには、**追加**をクリックします。</span><span class="sxs-lookup"><span data-stu-id="16c4b-133">Click **Add** to create a new line.</span></span>

4. <span data-ttu-id="16c4b-134">**カテゴリ** フィールドで、カテゴリを選択します。</span><span class="sxs-lookup"><span data-stu-id="16c4b-134">Select a category in the **Category** field.</span></span>

5. <span data-ttu-id="16c4b-135">**数量**フィールドに数量を挿入します。</span><span class="sxs-lookup"><span data-stu-id="16c4b-135">Insert quantity in the **Quantity** field.</span></span>

6. <span data-ttu-id="16c4b-136">関連するフィールドに、原価価格、販売通貨、および販売価格を挿入します。</span><span class="sxs-lookup"><span data-stu-id="16c4b-136">Insert cost price, sales currency, and sales price in the relevant fields.</span></span>

7. <span data-ttu-id="16c4b-137">**明細行プロパティ** フィールドで、明細行に使用する雑費タイプを選択します。</span><span class="sxs-lookup"><span data-stu-id="16c4b-137">In the **Line property** field, select the charge type to be used on the line.</span></span>

>[!NOTE]
><span data-ttu-id="16c4b-138">**メンテナンス予測の合計**クイック タブでは、選択した作業指示書ジョブと作業指示書について、各タブに作成された行数の概要を表示できます。</span><span class="sxs-lookup"><span data-stu-id="16c4b-138">On the **Maintenance forecast totals** FastTab, you can see an overview of the number of lines created on each tab, for the selected work order job and for the work order.</span></span> <span data-ttu-id="16c4b-139">また、作業指示書ジョブおよび作業指示書の予測作業時間の合計を表示することもできます。</span><span class="sxs-lookup"><span data-stu-id="16c4b-139">Also, you can see a sum of forecasted work hours for the work order job and for the work order.</span></span>

![図 1](media/06-work-orders.png)


## <a name="automatic-update-of-work-order-forecasts"></a><span data-ttu-id="16c4b-141">作業指示書予測の自動更新</span><span class="sxs-lookup"><span data-stu-id="16c4b-141">Automatic update of work order forecasts</span></span>

<span data-ttu-id="16c4b-142">資産管理では、他のモジュールで更新された時間原価、品目原価、および経費に関するいて、作業指示書予測の変更を自動的に更新できます。</span><span class="sxs-lookup"><span data-stu-id="16c4b-142">In Asset Management, you can automatically update any changes in work order forecasts regarding hour costs, item costs, and expenses, which have been updated in other modules.</span></span> <span data-ttu-id="16c4b-143">これは、最新の原価価格が常に作業指示書予測に使用されるようにするために行われます。</span><span class="sxs-lookup"><span data-stu-id="16c4b-143">This is done to ensure that the latest cost prices are always used in your work order forecasts.</span></span> <span data-ttu-id="16c4b-144">[メンテナンス作業タイプの予測](../setup-for-work-orders/job-groups-and-job-types-variants-trades-and-checklists.md) についても、同様の更新を行うことができます。</span><span class="sxs-lookup"><span data-stu-id="16c4b-144">It is also possible to make similar updates for [maintenance job type forecasts](../setup-for-work-orders/job-groups-and-job-types-variants-trades-and-checklists.md).</span></span>

1. <span data-ttu-id="16c4b-145">**資産管理** > **定期処理** > **予測** > **作業指示書予測の更新**をクリックします。</span><span class="sxs-lookup"><span data-stu-id="16c4b-145">Click **Asset management** > **Periodic** > **Forecast** > **Update work order forecast**.</span></span>

2. <span data-ttu-id="16c4b-146">**作業指示書予測の更新**ドロップダウン ダイアログでは、特定の作業指示書または作業指示書ジョブに関する選択を必要に応じて追加できます。</span><span class="sxs-lookup"><span data-stu-id="16c4b-146">In the **Update work order forecast** drop-down dialog, you can add selections regarding specific work orders or work order jobs, if required.</span></span> <span data-ttu-id="16c4b-147">**フィルター**をクリックして、これらの選択を行います。</span><span class="sxs-lookup"><span data-stu-id="16c4b-147">Click **Filter** to make those selections.</span></span>

3. <span data-ttu-id="16c4b-148">**バックグラウンドで実行**クイック タブで、必要に応じて自動更新をバッチ ジョブとして設定できます。</span><span class="sxs-lookup"><span data-stu-id="16c4b-148">If required, you can set up the automatic update as a batch job on the **Run in the background** FastTab.</span></span>

4. <span data-ttu-id="16c4b-149">**OK** をクリックして、予測の更新を開始します。</span><span class="sxs-lookup"><span data-stu-id="16c4b-149">Click **OK** to start the forecast update.</span></span>


![図 2](media/07-work-orders.png)

