---
title: 作業ラインの詳細
description: このトピックでは、システムの個々の作業ラインの包括的、並べ替え可能、フィルター処理可能な一覧を表示する作業ラインの詳細ページに関する情報を提供します。
author: mirzaab
manager: tfehr
ms.date: 07/01/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Retail, Core, Operations
ms.search.region: Global
ms.author: mirzaab
ms.search.validFrom: 2020-07-01
ms.dyn365.ops.version: Release 10.0.8
ms.openlocfilehash: 4f0952cc8778ffc509bed80b3a5038dbf4fb76c2
ms.sourcegitcommit: f64fce03ec52f844b05a9e8cac286cb201385002
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 07/16/2020
ms.locfileid: "3597195"
---
# <a name="work-line-details"></a><span data-ttu-id="7a6d3-103">作業ラインの詳細</span><span class="sxs-lookup"><span data-stu-id="7a6d3-103">Work line details</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="7a6d3-104">**作業ラインの詳細**ページには、システムの個々の作業ラインの包括的、並べ替え可能、フィルター処理可能な一覧が表示されます。</span><span class="sxs-lookup"><span data-stu-id="7a6d3-104">The **Work line details** page shows a comprehensive, sortable, and filterable list of the individual work lines in your system.</span></span> <span data-ttu-id="7a6d3-105">これにより、倉庫で計画および実行されている作業の完全な概要が表示されます。</span><span class="sxs-lookup"><span data-stu-id="7a6d3-105">It provides a complete overview of work that is being planned and executed in the warehouse.</span></span> <span data-ttu-id="7a6d3-106">すべての作業ラインの表示とオープン作業ラインのみの表示を簡単に切り替えることができます。</span><span class="sxs-lookup"><span data-stu-id="7a6d3-106">You can easily switch between viewing all work lines and viewing only open work lines.</span></span> <span data-ttu-id="7a6d3-107">各ラインに対して表示される詳細には、作業ステータス、品目番号、場所、作業数量、積荷 ID、および出荷 ID が含まれます。</span><span class="sxs-lookup"><span data-stu-id="7a6d3-107">Details that are provided for each line include the work status, item number, location, work quantity, load ID, and shipment ID.</span></span>

## <a name="turn-on-the-work-line-details-feature"></a><span data-ttu-id="7a6d3-108">作業ラインの詳細機能をオンにする</span><span class="sxs-lookup"><span data-stu-id="7a6d3-108">Turn on the work line details feature</span></span>

<span data-ttu-id="7a6d3-109">この機能を使用するには、システム上で有効にする必要があります。</span><span class="sxs-lookup"><span data-stu-id="7a6d3-109">Before you can use this feature, it must be turned on in your system.</span></span> <span data-ttu-id="7a6d3-110">管理者は、[機能の管理](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md)設定を使用して、機能の状態を確認し、必要に応じて有効にすることができます。</span><span class="sxs-lookup"><span data-stu-id="7a6d3-110">Admins can use the [feature management](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) settings to check the status of the feature and turn it on if it's required.</span></span> <span data-ttu-id="7a6d3-111">**機能管理** ワークスペースで、この機能は次のようにリストされています。</span><span class="sxs-lookup"><span data-stu-id="7a6d3-111">In the **Feature management** workspace, the feature is listed in the following way:</span></span>

- <span data-ttu-id="7a6d3-112">**モジュール:** *倉庫管理*</span><span class="sxs-lookup"><span data-stu-id="7a6d3-112">**Module:** *Warehouse management*</span></span>
- <span data-ttu-id="7a6d3-113">**機能名:** *作業ラインの詳細*</span><span class="sxs-lookup"><span data-stu-id="7a6d3-113">**Feature name:** *Work line details*</span></span>

## <a name="open-and-use-the-work-line-details-page"></a><span data-ttu-id="7a6d3-114">作業ラインの詳細ページを開いて使用する</span><span class="sxs-lookup"><span data-stu-id="7a6d3-114">Open and use the Work line details page</span></span>

<span data-ttu-id="7a6d3-115">作業ラインの詳細の一覧を表示するには、**倉庫管理 \> 作業 \> 作業ラインの詳細**の順に移動します。</span><span class="sxs-lookup"><span data-stu-id="7a6d3-115">To view the list of work line details, go to **Warehouse management \> Work \> Work line details**.</span></span> <span data-ttu-id="7a6d3-116">ここでは、実行できるアクションは次のとおりです。</span><span class="sxs-lookup"><span data-stu-id="7a6d3-116">From here, you can perform the following actions:</span></span>

- <span data-ttu-id="7a6d3-117">**フィルター** フィールドを使用して、使用可能なパラメーターに対して特定の値をとるラインを検索します。</span><span class="sxs-lookup"><span data-stu-id="7a6d3-117">Use the **Filter** field to search for lines that have a specific value for any available parameter.</span></span> <span data-ttu-id="7a6d3-118">(使用可能なパラメーターには、グリッドに列として表示されない多数のパラメーターが含まれています。)</span><span class="sxs-lookup"><span data-stu-id="7a6d3-118">(Available parameters include many parameters that aren't shown as columns in the grid.)</span></span>
- <span data-ttu-id="7a6d3-119">**クローズ済の表示**チェックボックスを使用して、閉じたラインを表示または非表示にできます。</span><span class="sxs-lookup"><span data-stu-id="7a6d3-119">Use the **Show closed** check box to show or hide closed lines.</span></span>
- <span data-ttu-id="7a6d3-120">**分析コードの表示**を選択して、**分析コード表示**ダイアログ ボックスを開きます。ここでは、グリッド内のさまざまな分析コード列を表示または非表示にすることができます。</span><span class="sxs-lookup"><span data-stu-id="7a6d3-120">Select **Display dimensions** to open the **Dimensions display** dialog box, where you can choose to show or hide various dimension columns in the grid.</span></span>
- <span data-ttu-id="7a6d3-121">任意の列見出しを選択してメニューを開き、その列の値によって一覧の並べ替え、またはフィルター処理を選択できます。</span><span class="sxs-lookup"><span data-stu-id="7a6d3-121">Select any column heading to open a menu where you can choose to sort or filter the list by values in that column.</span></span>
- <span data-ttu-id="7a6d3-122">作業ラインを選択し、**場所の変更**を選択して、その作業ラインの場所を変更できるダイアログ ボックスを開きます。</span><span class="sxs-lookup"><span data-stu-id="7a6d3-122">Select a work line, and then select **Change location** to open a dialog box where you can change the location for that work line.</span></span> <span data-ttu-id="7a6d3-123">指定した場所は、場所のディレクティブの設定を上書きします。</span><span class="sxs-lookup"><span data-stu-id="7a6d3-123">The location that you specify will override the setup of the location directive.</span></span>
- <span data-ttu-id="7a6d3-124">作業ラインを選択し、**作業ラインのキャンセル**を選択して、その作業ラインの数量を部分的または完全に減らすことができるダイアログ ボックスを開きます。</span><span class="sxs-lookup"><span data-stu-id="7a6d3-124">Select a work line, and then select **Cancel work line** to open a dialog box where you can partially or fully reduce the quantity of that work line.</span></span>
- <span data-ttu-id="7a6d3-125">数量を調整します。</span><span class="sxs-lookup"><span data-stu-id="7a6d3-125">Adjust quantities.</span></span>
- <span data-ttu-id="7a6d3-126">任意の作業ラインの背後にあるトランザクションを表示します。</span><span class="sxs-lookup"><span data-stu-id="7a6d3-126">View the transactions behind any work line.</span></span>

## <a name="try-out-the-feature"></a><span data-ttu-id="7a6d3-127">機能を試す</span><span class="sxs-lookup"><span data-stu-id="7a6d3-127">Try out the feature</span></span>

<span data-ttu-id="7a6d3-128">このセクションでは、作業ラインの詳細を操作する方法を示す 3 つの部分からなるデモについて説明します。</span><span class="sxs-lookup"><span data-stu-id="7a6d3-128">This section provides a three-part demo that shows how to work with work line details.</span></span>

### <a name="make-sample-data-available"></a><span data-ttu-id="7a6d3-129">サンプル データを有効化する</span><span class="sxs-lookup"><span data-stu-id="7a6d3-129">Make sample data available</span></span>

<span data-ttu-id="7a6d3-130">ここで指定されたサンプル レコードと値を使用してこのデモを実行するには、標準の [デモ データ](../../fin-ops-core/dev-itpro/deployment/deploy-demo-environment.md) がインストールされているシステムを使用する必要があります。</span><span class="sxs-lookup"><span data-stu-id="7a6d3-130">To work through this demo by using the sample records and values that are specified here, you must be on a system where the standard [demo data](../../fin-ops-core/dev-itpro/deployment/deploy-demo-environment.md) is installed.</span></span> <span data-ttu-id="7a6d3-131">また、開始する前に **USMF** 法人を選択する必要があります。</span><span class="sxs-lookup"><span data-stu-id="7a6d3-131">Additionally, you must select the **USMF** legal entity before you begin.</span></span>

<span data-ttu-id="7a6d3-132">このデモは、実稼働システムで作業するときのガイダンスとして使用することもできます。</span><span class="sxs-lookup"><span data-stu-id="7a6d3-132">You can also use this demo as guidance when you work on a production system.</span></span> <span data-ttu-id="7a6d3-133">ただし、独自の値に置き換える必要があり、標準のデモ データが提供するいくつかのタイプの必要なレコードが不足している可能性があります。</span><span class="sxs-lookup"><span data-stu-id="7a6d3-133">However, you must substitute your own values, and you might be missing some types of required records that the standard demo data provides.</span></span>

### <a name="verify-that-the-scenario-setup-includes-enough-available-inventory"></a><span data-ttu-id="7a6d3-134">シナリオの設定に十分な利用可能在庫があることの検証</span><span class="sxs-lookup"><span data-stu-id="7a6d3-134">Verify that the scenario setup includes enough available inventory</span></span>

<span data-ttu-id="7a6d3-135">**USMF** のデモ データを使用している場合は、まず、関連する各ピッキング場所に十分な在庫が利用できるようにシステムが設定されていることを確認する必要があります。</span><span class="sxs-lookup"><span data-stu-id="7a6d3-135">If you're working with the **USMF** demo data, you should first make sure that your system is set up so that enough inventory is available at each relevant pick location.</span></span> <span data-ttu-id="7a6d3-136">このデモでは、次の在庫があることが予想されます。</span><span class="sxs-lookup"><span data-stu-id="7a6d3-136">For this demo, the expectation is that you have the following inventory available:</span></span>

- <span data-ttu-id="7a6d3-137">**品目 M9200:** 45 個</span><span class="sxs-lookup"><span data-stu-id="7a6d3-137">**Item M9200:** 45 ea.</span></span> <span data-ttu-id="7a6d3-138">(または以上)</span><span class="sxs-lookup"><span data-stu-id="7a6d3-138">(or more)</span></span>
- <span data-ttu-id="7a6d3-139">**品目 M9202:** 10 個</span><span class="sxs-lookup"><span data-stu-id="7a6d3-139">**Item M9202:** 10 ea.</span></span> <span data-ttu-id="7a6d3-140">(または以上)</span><span class="sxs-lookup"><span data-stu-id="7a6d3-140">(or more)</span></span>

<span data-ttu-id="7a6d3-141">次の手順に従って、十分な在庫があることを確認し、必要な調整を行います。</span><span class="sxs-lookup"><span data-stu-id="7a6d3-141">Follow these steps to verify that enough inventory is available and to make any adjustments that are required.</span></span>

1. <span data-ttu-id="7a6d3-142">**倉庫管理 \> 設定 \> 場所のディレクティブ**の順に移動し、倉庫 51 で販売注文のピッキングに使用されるピッキング場所を決定します。</span><span class="sxs-lookup"><span data-stu-id="7a6d3-142">Go to **Warehouse management \> Setup \> Location directives**, and determine which picking locations are used for sales order picking at warehouse 51.</span></span> <span data-ttu-id="7a6d3-143">(詳細については、[作業テンプレートと場所ディレクティブを使い倉庫作業の制御](control-warehouse-location-directives.md) を参照してください。)</span><span class="sxs-lookup"><span data-stu-id="7a6d3-143">(For more information, see [Control warehouse work by using work templates and location directives](control-warehouse-location-directives.md).)</span></span>
1. <span data-ttu-id="7a6d3-144">関連する場所で在庫レベルを確認します。</span><span class="sxs-lookup"><span data-stu-id="7a6d3-144">Check the inventory levels at the relevant locations.</span></span>
1. <span data-ttu-id="7a6d3-145">必要に応じて在庫を調整します。</span><span class="sxs-lookup"><span data-stu-id="7a6d3-145">Adjust inventory as required.</span></span> <span data-ttu-id="7a6d3-146">手動による移動を作成したり、補充を使用したり、またはその他のフローを適用して在庫を調整したりできます。</span><span class="sxs-lookup"><span data-stu-id="7a6d3-146">You can create manual movements, use replenishment, or apply any other flow to adjust the inventory.</span></span>

### <a name="part-1-create-picking-work"></a><span data-ttu-id="7a6d3-147">パート 1: ピッキング作業の作成</span><span class="sxs-lookup"><span data-stu-id="7a6d3-147">Part 1: Create picking work</span></span>

<span data-ttu-id="7a6d3-148">作業の作成を開始する前に、予定した方法で作業要求に対応するように倉庫が設定されていることを確認してください。</span><span class="sxs-lookup"><span data-stu-id="7a6d3-148">Before you start to create work, make sure that your warehouse is set up to respond to work requests in the expected manner.</span></span>

<span data-ttu-id="7a6d3-149">これらの手順に従って、ピッキング作業を作成します。</span><span class="sxs-lookup"><span data-stu-id="7a6d3-149">Follow these steps to create some picking work.</span></span>

1. <span data-ttu-id="7a6d3-150">**販売とマーケティング \> 販売注文 \> すべての販売注文**の順に移動します。</span><span class="sxs-lookup"><span data-stu-id="7a6d3-150">Go to **Sales and marketing \> Sales orders \> All sales orders**.</span></span>
1. <span data-ttu-id="7a6d3-151">**新規**を選択して、**販売注文の作成**ダイアログ ボックスを開きます。</span><span class="sxs-lookup"><span data-stu-id="7a6d3-151">Select **New** to open the **Create sales order** dialog box.</span></span>
1. <span data-ttu-id="7a6d3-152">**販売注文の作成**ダイアログ ボックスでは、次の値を設定します。</span><span class="sxs-lookup"><span data-stu-id="7a6d3-152">In the **Create sales order** dialog box, set the following values:</span></span>

    - <span data-ttu-id="7a6d3-153">**顧客**クイック タブで、**顧客 ID** フィールドを _US-001_ に設定します。</span><span class="sxs-lookup"><span data-stu-id="7a6d3-153">On the **Customer** FastTab, set the **Customer account** field to _US-001_.</span></span>
    - <span data-ttu-id="7a6d3-154">**一般**クイック タブの**倉庫**フィールドを _51_ に設定します。</span><span class="sxs-lookup"><span data-stu-id="7a6d3-154">On the **General** FastTab, set the **Warehouse** field to _51_.</span></span>

1. <span data-ttu-id="7a6d3-155">**OK** を選択して販売注文を作成し、ダイアログ ボックスを閉じます。</span><span class="sxs-lookup"><span data-stu-id="7a6d3-155">Select **OK** to create the sales order and close the dialog box.</span></span>
1. <span data-ttu-id="7a6d3-156">新しい販売注文が開かれます。</span><span class="sxs-lookup"><span data-stu-id="7a6d3-156">Your new sales order is opened.</span></span> <span data-ttu-id="7a6d3-157">**販売注文行**グリッドに新しい空の行が含まれます。</span><span class="sxs-lookup"><span data-stu-id="7a6d3-157">It includes a new, empty row in the **Sales order lines** grid.</span></span> <span data-ttu-id="7a6d3-158">この注文明細行に次の値を設定します。</span><span class="sxs-lookup"><span data-stu-id="7a6d3-158">On this order line, set the following values:</span></span>

    - <span data-ttu-id="7a6d3-159">**品目番号:** _M9200_</span><span class="sxs-lookup"><span data-stu-id="7a6d3-159">**Item number:** _M9200_</span></span>
    - <span data-ttu-id="7a6d3-160">**数量:** _20_</span><span class="sxs-lookup"><span data-stu-id="7a6d3-160">**Quantity:** _20_</span></span>
    - <span data-ttu-id="7a6d3-161">**単位:** _個_</span><span class="sxs-lookup"><span data-stu-id="7a6d3-161">**Unit:** _ea_</span></span>

1. <span data-ttu-id="7a6d3-162">新しい注文明細行を選択し、**在庫**メニューで、**引当**を選択して**引当**ページを開きます。</span><span class="sxs-lookup"><span data-stu-id="7a6d3-162">Select the new order line, and then, on the **Inventory** menu, select **Reservation** to open the **Reservation** page.</span></span>
1. <span data-ttu-id="7a6d3-163">**引当**ページで、**引当ロット**を選択して、選択した明細行の全数量を倉庫に引当します。</span><span class="sxs-lookup"><span data-stu-id="7a6d3-163">On the **Reservation** page, select **Reserve lot** to reserve the selected line's full quantity in the warehouse.</span></span>
1. <span data-ttu-id="7a6d3-164">**引当**ページを閉じて、販売注文に戻ります。</span><span class="sxs-lookup"><span data-stu-id="7a6d3-164">Close the **Reservation** page to return to the sales order.</span></span>
1. <span data-ttu-id="7a6d3-165">アクション ウィンドウの**倉庫**タブで、**倉庫へのリリース**を選択します。</span><span class="sxs-lookup"><span data-stu-id="7a6d3-165">On the Action Pane, on the **Warehouse** tab, select **Release to warehouse**.</span></span> <span data-ttu-id="7a6d3-166">システムは出荷を作成し、それを新しい積荷に追加して、必要な作業を作成します。</span><span class="sxs-lookup"><span data-stu-id="7a6d3-166">The system creates a shipment, adds it to a new load, and creates the required work.</span></span>
1. <span data-ttu-id="7a6d3-167">最初の注文で使用したのと同じ顧客 ID と倉庫に対して 2 番目の販売注文を作成します。</span><span class="sxs-lookup"><span data-stu-id="7a6d3-167">Create a second sales order for the same customer account and warehouse that you used for the first order.</span></span> <span data-ttu-id="7a6d3-168">この注文に次の 2 つの注文明細行を追加します。</span><span class="sxs-lookup"><span data-stu-id="7a6d3-168">Add the following two order lines to this order:</span></span>

    - <span data-ttu-id="7a6d3-169">**行 1:** **品目番号**フィールドを _M9200_ に、**数量**フィールドを _25_ に、**単位**を_個_に設定します。</span><span class="sxs-lookup"><span data-stu-id="7a6d3-169">**Line 1:** Set the **Item number** field to _M9200_, the **Quantity** field to _25_, and the **Unit** field to _ea_.</span></span>
    - <span data-ttu-id="7a6d3-170">**行 2:** **品目番号**フィールドを _M9202_ に、**数量**フィールドを _10_ に、**単位**を_個_に設定します。</span><span class="sxs-lookup"><span data-stu-id="7a6d3-170">**Line 2:** Set the **Item number** field to _M9202_, the **Quantity** field to _10_, and the **Unit** field to _ea_.</span></span>

1. <span data-ttu-id="7a6d3-171">手順 6 ～ 8 を繰り返して、各注文明細行の在庫の引当を行い (一度に 1 つずつ)、手順 9 を繰り返して、注文を倉庫にリリースします。</span><span class="sxs-lookup"><span data-stu-id="7a6d3-171">Repeat steps 6 through 8 to reserve the inventory for each order line (one at a time), and then repeat step 9 to release the order to the warehouse.</span></span>

### <a name="part-2-change-the-location-for-a-work-line"></a><span data-ttu-id="7a6d3-172">手順 2: 作業ラインの場所を変更する</span><span class="sxs-lookup"><span data-stu-id="7a6d3-172">Part 2: Change the location for a work line</span></span>

1. <span data-ttu-id="7a6d3-173">**倉庫管理 \> 作業 \> 作業ラインの詳細**の順に移動します。</span><span class="sxs-lookup"><span data-stu-id="7a6d3-173">Go to **Warehouse management \> Work \> Work line details**.</span></span>
1. <span data-ttu-id="7a6d3-174">このデモ用に作成した作業ラインの 1 つを検索して選択します。</span><span class="sxs-lookup"><span data-stu-id="7a6d3-174">Find and select one of the work lines that you created for this demo.</span></span>
1. <span data-ttu-id="7a6d3-175">**場所の変更**を選択して、**新しい場所の選択**ダイアログ ボックスを開きます。</span><span class="sxs-lookup"><span data-stu-id="7a6d3-175">Select **Change location** to open the **Select new location** dialog box.</span></span>
1. <span data-ttu-id="7a6d3-176">**新しい場所の選択**ダイアログ ボックスの**場所**フィールドで、作業ラインの新しい場所を選択します。</span><span class="sxs-lookup"><span data-stu-id="7a6d3-176">In the **Select new location** dialog box, in the **Location** field, select a new location for the work line.</span></span>
1. <span data-ttu-id="7a6d3-177">**OK** を選択して変更を適用し、ダイアログ ボックスを閉じます。</span><span class="sxs-lookup"><span data-stu-id="7a6d3-177">Select **OK** to apply your change and close the dialog box.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="7a6d3-178">新しい保管場所に使用可能な十分の在庫がある場合 (ピッキングの場合)、または場所タイプの検証に合格した場合 (プットの場合) にのみ、場所の変更を送信できます。</span><span class="sxs-lookup"><span data-stu-id="7a6d3-178">You can submit location changes only if the new location has enough inventory available (for a pick), or if it passes location-type validation (for a put).</span></span>

### <a name="part-3-change-the-quantity-of-a-work-line-or-cancel-a-work-line"></a><span data-ttu-id="7a6d3-179">手順 3: 作業ラインの数量の変更または作業ラインのキャンセル</span><span class="sxs-lookup"><span data-stu-id="7a6d3-179">Part 3: Change the quantity of a work line or cancel a work line</span></span>

1. <span data-ttu-id="7a6d3-180">**倉庫管理 \> 作業 \> 作業ラインの詳細**の順に移動します。</span><span class="sxs-lookup"><span data-stu-id="7a6d3-180">Go to **Warehouse management \> Work \> Work line details**.</span></span>
1. <span data-ttu-id="7a6d3-181">このデモ用に作成した作業ラインの 1 つを検索して選択します。</span><span class="sxs-lookup"><span data-stu-id="7a6d3-181">Find and select one of the work lines that you created for this demo.</span></span> <span data-ttu-id="7a6d3-182">作業タイプが_ピッキング_である作業ラインについてのみ、数量をキャンセルまたは変更できることに注意してください。</span><span class="sxs-lookup"><span data-stu-id="7a6d3-182">Note that you can cancel or change quantities only for work lines where the work type is _pick_.</span></span>
1. <span data-ttu-id="7a6d3-183">**作業ラインのキャンセル**を選択して、**キャンセルする数量**ダイアログ ボックスを開きます。</span><span class="sxs-lookup"><span data-stu-id="7a6d3-183">Select **Cancel work line** to open the **Quantity to cancel** dialog box.</span></span>
1. <span data-ttu-id="7a6d3-184">**キャンセルする数量**ダイアログ ボックスで、**数量**フィールドの値を変更して、ラインに現在指定されている数量*から減算*される数量を指定します。</span><span class="sxs-lookup"><span data-stu-id="7a6d3-184">In the **Quantity to cancel** dialog box, change the value in the **Quantity** field to specify the quantity that should be *subtracted from* the quantity that is currently specified for the line.</span></span> <span data-ttu-id="7a6d3-185">既定では、**数量**フィールドには全数量が表示されます。</span><span class="sxs-lookup"><span data-stu-id="7a6d3-185">By default, the **Quantity** field shows the full quantity.</span></span>

    - <span data-ttu-id="7a6d3-186">全数量をキャンセルすると、**作業ステータス**値が_キャンセル済_に変更されますが、**作業数量**フィールドには、元の値が引き続き表示されます。</span><span class="sxs-lookup"><span data-stu-id="7a6d3-186">If you cancel the full quantity, the **Work status** value will be changed to _Canceled_, but the **Work quantity** field will still show the original value.</span></span>
    - <span data-ttu-id="7a6d3-187">数量の一部のみをキャンセルした場合、**作業数量**フィールドは更新されて新しい値が表示されますが、**作業ステータス**値は変更されません。</span><span class="sxs-lookup"><span data-stu-id="7a6d3-187">If you cancel just part of the quantity, the **Work quantity** field will be updated to show the new value, but the **Work status** value won't change.</span></span>

1. <span data-ttu-id="7a6d3-188">**OK** を選択して変更を適用し、ダイアログ ボックスを閉じます。</span><span class="sxs-lookup"><span data-stu-id="7a6d3-188">Select **OK** to apply your change and close the dialog box.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="7a6d3-189">作業ラインの数量の一部のみをキャンセルする場合は、積荷明細行から古い数量を削除する必要もあります。</span><span class="sxs-lookup"><span data-stu-id="7a6d3-189">If you cancel just part of the quantity for a work line, you must also remove the obsolete quantity from the load line.</span></span> <span data-ttu-id="7a6d3-190">それ以外の場合は、過少配送が正しく設定されていないと、積荷明細行は出荷確認できません。</span><span class="sxs-lookup"><span data-stu-id="7a6d3-190">Otherwise, unless under-delivery is set up correctly, the load line can't be ship-confirmed.</span></span>
