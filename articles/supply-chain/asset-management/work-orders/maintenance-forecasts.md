---
title: メンテナンス予測
description: このトピックでは、資産管理におけるメンテナンス予測について説明します。
author: josaw1
manager: AnnBe
ms.date: 10/15/2019
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
ms.search.validFrom: 2019-09-30
ms.dyn365.ops.version: 10.0.5
ms.openlocfilehash: a1596b283c3eaffca25ff7f03c722a2bcce109fb
ms.sourcegitcommit: deb87e518a151d8bb084891851a39758938a96e4
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 10/15/2019
ms.locfileid: "2626296"
---
# <a name="maintenance-forecasts"></a><span data-ttu-id="246b0-103">メンテナンス予測</span><span class="sxs-lookup"><span data-stu-id="246b0-103">Maintenance forecasts</span></span>

[!include [banner](../../includes/banner.md)]



<span data-ttu-id="246b0-104">作業指示書を作成すると、関連する資産とメンテナンス作業タイプを含む作業指示書ジョブが作成されます。</span><span class="sxs-lookup"><span data-stu-id="246b0-104">When you create a work order, you create work order jobs that have related assets and maintenance job types.</span></span> <span data-ttu-id="246b0-105">メンテナンス予測を含むメンテナンス作業タイプを選択すると、予測が自動的に作業指示書にコピーされます。</span><span class="sxs-lookup"><span data-stu-id="246b0-105">When you select a maintenance job type that contains maintenance forecasts, the forecasts are automatically copied to the work order.</span></span>

<span data-ttu-id="246b0-106">作業指示書に予測明細行を追加したり削除したりすることができる場合があります。</span><span class="sxs-lookup"><span data-stu-id="246b0-106">You might be able to add forecast lines to a work order or delete them from a work order.</span></span> <span data-ttu-id="246b0-107">作業指示書ライフサイクル状態の設定、関連するプロジェクト タイプ、およびプロジェクト タイプに関連するステージ ルールにより、予測明細行を追加または編集できるかどうかが決まります。</span><span class="sxs-lookup"><span data-stu-id="246b0-107">The setup of the work order lifecycle state, the related project type, and the stage rules that are related to the project type determine whether you can add or edit forecast lines.</span></span> <span data-ttu-id="246b0-108">作業指示書ライフサイクルの状態と関連するプロジェクト ステージの詳細については、[予測、作業指示書、およびプロジェクト](../integration-to-project-management-and-accounting/forecasts-work-orders-and-projects.md) を参照してください。</span><span class="sxs-lookup"><span data-stu-id="246b0-108">For more information about work order lifecycle states and related project stages, see [Forecasts, work orders, and projects](../integration-to-project-management-and-accounting/forecasts-work-orders-and-projects.md).</span></span>

1. <span data-ttu-id="246b0-109">**資産管理** > **共通** > **作業指示書** > **すべての作業指示書**または**有効な作業指示書**の順に選択します。</span><span class="sxs-lookup"><span data-stu-id="246b0-109">Select **Asset management** > **Common** > **Work orders** > **All work orders** or **Active work orders**.</span></span>

2. <span data-ttu-id="246b0-110">一覧で作業指示書を選択してから、アクション ペインで > **作業指示書**タブ > **プロジェクト**グループ > **予測**を選択します。</span><span class="sxs-lookup"><span data-stu-id="246b0-110">Select the work order in the list, and then, on the Action Pane > **Work order** tab > the **Project** group, select **Forecast**.</span></span> <span data-ttu-id="246b0-111">**作業指示書のメンテナンス予測**ページでは、作業指示書ジョブで選択したメンテナンス作業タイプからの予測明細行が表示されます。</span><span class="sxs-lookup"><span data-stu-id="246b0-111">The **Work order maintenance forecast** page shows forecast lines from the maintenance job type that is selected on the work order job.</span></span>


## <a name="add-an-hours-forecast-to-a-work-order"></a><span data-ttu-id="246b0-112">作業指示書への時間予測の追加</span><span class="sxs-lookup"><span data-stu-id="246b0-112">Add an hours forecast to a work order</span></span>

1. <span data-ttu-id="246b0-113">**作業指示書のメンテナンス予測**ページで、予測を追加する作業指示書ジョブを選択します。</span><span class="sxs-lookup"><span data-stu-id="246b0-113">On the **Work order maintenance forecast** page, select the work order job to add a forecast to.</span></span>

2. <span data-ttu-id="246b0-114">**時間**クイック タブで、**追加**を選択して明細行を新規作成します。</span><span class="sxs-lookup"><span data-stu-id="246b0-114">On the **Hours** FastTab, select **Add** to create a new line.</span></span>

3. <span data-ttu-id="246b0-115">**カテゴリ**フィールドで、カテゴリを選択します。</span><span class="sxs-lookup"><span data-stu-id="246b0-115">In the **Category** field, select a category.</span></span>

4. <span data-ttu-id="246b0-116">**時間**フィールドに予測時間数を入力します。</span><span class="sxs-lookup"><span data-stu-id="246b0-116">In the **Hours** field, enter the number of forecasted hours.</span></span>

5. <span data-ttu-id="246b0-117">**明細行プロパティ** フィールドで、明細行に使用する費用のタイプを選択します。</span><span class="sxs-lookup"><span data-stu-id="246b0-117">In the **Line property** field, select the type of charge that should be used on the line.</span></span>


## <a name="add-an-items-forecast-to-a-work-order"></a><span data-ttu-id="246b0-118">作業指示書への品目予測の追加</span><span class="sxs-lookup"><span data-stu-id="246b0-118">Add an items forecast to a work order</span></span>

<span data-ttu-id="246b0-119">作業指示書のメンテナンス予測に品目を追加するには、3 つの方法があります。</span><span class="sxs-lookup"><span data-stu-id="246b0-119">There are three ways to add items to a work order maintenance forecast.</span></span> <span data-ttu-id="246b0-120">予備部品リストまたは資産の部品表 (BOM) に含まれない品目 (予備部品) に対する明細行を作成します。承認済みの予備部品リストから予備部品を選択します。資産の BOM から品目を選択します。</span><span class="sxs-lookup"><span data-stu-id="246b0-120">You can create lines for items (spare parts) that aren't included on the spare parts list or the asset bill of materials (BOM), you can select spare parts from the approved spare parts list, or you can select items from the asset BOM.</span></span>

- <span data-ttu-id="246b0-121">**作業指示書のメンテナンス予測**ページで、予測を追加する作業指示書ジョブを選択します。</span><span class="sxs-lookup"><span data-stu-id="246b0-121">On the **Work order maintenance forecast** page, select the work order job to to add a forecast to.</span></span>

- <span data-ttu-id="246b0-122">**品目**クイック タブで、適切なメソッドを使用して、メンテナンス予測に品目を追加します。</span><span class="sxs-lookup"><span data-stu-id="246b0-122">On the **Items** FastTab, add items to the maintenance forecast by using the appropriate method.</span></span>

<span data-ttu-id="246b0-123">予備部品リストまたは資産の BOM にない予備部品に対して新しい明細行を作成するには、これらのステップに従います。</span><span class="sxs-lookup"><span data-stu-id="246b0-123">To create a line for a spare part that isn't on the spare parts list or the asset BOM, follow these steps:</span></span>

1. <span data-ttu-id="246b0-124">**追加**を選択します。</span><span class="sxs-lookup"><span data-stu-id="246b0-124">Select **Add**.</span></span>
2. <span data-ttu-id="246b0-125">**品目番号** フィールドで、品目を選択します。</span><span class="sxs-lookup"><span data-stu-id="246b0-125">In the **Item number** field, select the item.</span></span>
3. <span data-ttu-id="246b0-126">**販売数量**フィールドで、数量を入力します。</span><span class="sxs-lookup"><span data-stu-id="246b0-126">In the **Sales quantity** field, enter the quantity.</span></span>
4. <span data-ttu-id="246b0-127">**単位**フィールドで、数量の測定単位を選択します。</span><span class="sxs-lookup"><span data-stu-id="246b0-127">In the **Unit** field, select the unit of measure for the quantity.</span></span>
5. <span data-ttu-id="246b0-128">**原価価格**および**通貨**フィールドに、適切な値を入力します。</span><span class="sxs-lookup"><span data-stu-id="246b0-128">In the **Cost price** and **Currency** fields, enter appropriate values.</span></span>
6. <span data-ttu-id="246b0-129">**明細行プロパティ**フィールドで、明細行プロパティを選択します。</span><span class="sxs-lookup"><span data-stu-id="246b0-129">In the **Line property** field, select a line property.</span></span>
7. <span data-ttu-id="246b0-130">品目明細行に表示される分析コードの一覧を変更するには、**在庫** > **分析コードの表示**で分析コードを選択してから、**設定の保存**オプションで**はい**を選択します。</span><span class="sxs-lookup"><span data-stu-id="246b0-130">To change the list of dimensions that is shown on the item lines, select **Inventory** > **Display dimensions**, select the dimensions, and then set the **Save setup** option to **Yes**.</span></span>

<span data-ttu-id="246b0-131">承認済み予備部品リストから予備部品を追加するには、次の手順に従います。</span><span class="sxs-lookup"><span data-stu-id="246b0-131">To add a spare part from an approved spare parts list, follow these steps:</span></span>

1. <span data-ttu-id="246b0-132">**予備部品の追加**を選択します。</span><span class="sxs-lookup"><span data-stu-id="246b0-132">Select **Add spare parts**.</span></span>
2. <span data-ttu-id="246b0-133">予備部品を選択し、必要に応じて関連情報を編集します。</span><span class="sxs-lookup"><span data-stu-id="246b0-133">Select the spare part, and edit the related information as you require.</span></span>
3. <span data-ttu-id="246b0-134">**OK** を選択します。</span><span class="sxs-lookup"><span data-stu-id="246b0-134">Select **OK**.</span></span>

<span data-ttu-id="246b0-135">資産の BOM から品目を追加するには、次の手順に従います。</span><span class="sxs-lookup"><span data-stu-id="246b0-135">To add an item from the asset BOM, follow these steps:</span></span>

1. <span data-ttu-id="246b0-136">**BOM 品目の追加**を選択します。</span><span class="sxs-lookup"><span data-stu-id="246b0-136">Select **Add BOM items**.</span></span>
2. <span data-ttu-id="246b0-137">品目を選択し、必要に応じて関連情報を編集します。</span><span class="sxs-lookup"><span data-stu-id="246b0-137">Select the item, and edit the related information as you require.</span></span>
3. <span data-ttu-id="246b0-138">**OK** を選択します。</span><span class="sxs-lookup"><span data-stu-id="246b0-138">Select **OK**.</span></span>

<span data-ttu-id="246b0-139">資産管理で資産、メンテナンス ジョブ タイプの既定値、予備部品、および作業指示書に関連して、選択した明細行の品目が使用されている場所を示す概要を取得するには、**品目の使用場所**を選択します。</span><span class="sxs-lookup"><span data-stu-id="246b0-139">To get an overview that shows where the item on the selected line is used in relation to assets, maintenance job type defaults, spare parts, and work orders in Asset Management, select **Item where used**.</span></span> <span data-ttu-id="246b0-140">この概要の詳細については、[品目の使用場所](../controlling-and-reporting/item-where-used.md) を参照してください。</span><span class="sxs-lookup"><span data-stu-id="246b0-140">For more information about this overview, see [Item where used](../controlling-and-reporting/item-where-used.md).</span></span>


## <a name="add-an-expense-forecast-to-a-work-order"></a><span data-ttu-id="246b0-141">作業指示書への経費予測の追加</span><span class="sxs-lookup"><span data-stu-id="246b0-141">Add an expense forecast to a work order</span></span>

1. <span data-ttu-id="246b0-142">**作業指示書のメンテナンス予測**ページで、予測を追加する作業指示書ジョブを選択します。</span><span class="sxs-lookup"><span data-stu-id="246b0-142">On the **Work order maintenance forecast** page, select the work order job to add a forecast to.</span></span>

2. <span data-ttu-id="246b0-143">**経費**クイック タブで、**追加**を選択して明細行を作成します。</span><span class="sxs-lookup"><span data-stu-id="246b0-143">On the **Expense** FastTab, select **Add** to create a line.</span></span>

3. <span data-ttu-id="246b0-144">**カテゴリ**フィールドで、カテゴリを選択します。</span><span class="sxs-lookup"><span data-stu-id="246b0-144">In the **Category** field, select a category.</span></span>

4. <span data-ttu-id="246b0-145">**数量** フィールドで、数量を入力します。</span><span class="sxs-lookup"><span data-stu-id="246b0-145">In the **Quantity** field, enter the quantity.</span></span>

5. <span data-ttu-id="246b0-146">**原価価格**、**販売通貨**、および**販売価格**フィールドに適切な値を入力します。</span><span class="sxs-lookup"><span data-stu-id="246b0-146">In the **Cost price**, **Sales currency**, and **Sales price** fields, enter appropriate values.</span></span>

6. <span data-ttu-id="246b0-147">**明細行プロパティ** フィールドで、明細行に使用する費用のタイプを選択します。</span><span class="sxs-lookup"><span data-stu-id="246b0-147">In the **Line property** field, select the type of charge that should be used on the line.</span></span>

>[!NOTE]
><span data-ttu-id="246b0-148">**メンテナンス予測の合計**クイック タブでは、各クイック タブで選択した作業指示書ジョブと作業指示書について、作成された行数の概要を表示できます。</span><span class="sxs-lookup"><span data-stu-id="246b0-148">The **Maintenance forecast totals** FastTab shows an overview of the number of lines that have been created, for the selected work order job and for the work order, on each FastTab.</span></span> <span data-ttu-id="246b0-149">また、作業指示書ジョブおよび作業指示書の予測作業時間の合計を表示することもできます。</span><span class="sxs-lookup"><span data-stu-id="246b0-149">It also shows the total forecasted work hours for the work order job and the work order.</span></span>

<span data-ttu-id="246b0-150">下の図は、**作業指示書のメンテナンス予測**ページの例を示しています。</span><span class="sxs-lookup"><span data-stu-id="246b0-150">The illustration below shows an example of the **Work order maintenance forecast** page.</span></span>

![図 1](media/06-work-orders.png)


## <a name="automatic-update-of-work-order-forecasts"></a><span data-ttu-id="246b0-152">作業指示書予測の自動更新</span><span class="sxs-lookup"><span data-stu-id="246b0-152">Automatic update of work order forecasts</span></span>

<span data-ttu-id="246b0-153">時間原価、品目原価、および経費が、Microsoft Dynamics 365 for Finance and Operations の他のモジュールで更新された場合、資産管理での作業指示書予測は変更を反映するように自動的に更新されます。</span><span class="sxs-lookup"><span data-stu-id="246b0-153">If hour costs, item costs, and expenses are updated in other modules in Microsoft Dynamics 365 for Finance and Operations, work order forecasts in Asset Management can automatically be updated to reflect those changes.</span></span> <span data-ttu-id="246b0-154">この能力によって、最新の原価価格が常に作業指示書予測に使用されることが保証されます。</span><span class="sxs-lookup"><span data-stu-id="246b0-154">This capability helps guarantee that the latest cost prices are always used in your work order forecasts.</span></span> <span data-ttu-id="246b0-155">[メンテナンス作業タイプの予測](../setup-for-work-orders/job-groups-and-job-types-variants-trades-and-checklists.md) についても、同様の更新を行うことができます。</span><span class="sxs-lookup"><span data-stu-id="246b0-155">You can also do similar updates for [maintenance job type forecasts](../setup-for-work-orders/job-groups-and-job-types-variants-trades-and-checklists.md).</span></span>

1. <span data-ttu-id="246b0-156">**資産管理** > **定期処理** > **予測** > **作業指示書予測の更新**を選択します。</span><span class="sxs-lookup"><span data-stu-id="246b0-156">Select **Asset management** > **Periodic** > **Forecast** > **Update work order forecast**.</span></span>

2. <span data-ttu-id="246b0-157">**作業指示書予測の更新**ダイアログ (**対象に含めるレコード**クイックタブ) では、特定の作業指示書または作業指示書ジョブに関する選択を必要に応じて追加できます。</span><span class="sxs-lookup"><span data-stu-id="246b0-157">In the **Update work order forecast** dialog, on the **Records to include** FastTab, you can add selections regarding specific work orders or work order jobs, as you require.</span></span> <span data-ttu-id="246b0-158">**フィルター**をクリックして、関連する選択を行います。</span><span class="sxs-lookup"><span data-stu-id="246b0-158">Click **Filter** to make the relevant selections.</span></span>

3. <span data-ttu-id="246b0-159">**バックグラウンドで実行**クイック タブでは、必要に応じて自動更新をバッチ ジョブとして設定できます。</span><span class="sxs-lookup"><span data-stu-id="246b0-159">On the **Run in the background** FastTab, you can set up the automatic update as a batch job, as you require.</span></span>

4. <span data-ttu-id="246b0-160">**OK** を選択し、予測の更新を開始します。</span><span class="sxs-lookup"><span data-stu-id="246b0-160">Select **OK** to start the forecast update.</span></span>


<span data-ttu-id="246b0-161">次の図は、**作業指示書予測の更新**ダイアログの例を示しています。</span><span class="sxs-lookup"><span data-stu-id="246b0-161">The illustration below shows an example of the **Update work order forecast** dialog.</span></span>

![図 2](media/07-work-orders.png)
