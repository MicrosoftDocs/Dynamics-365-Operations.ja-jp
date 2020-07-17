---
title: システム主導の作業優先順位
description: このトピックでは、システム主導の作業優先順位について説明します。 この機能により、システムが実行のためにユーザーに提示する作業指示書の並べ替えとフィルター処理を行うことができます。 これは、倉庫ピッキング プロセスを促進するための追加の基準が必要なシナリオで役立ちます。
author: Mirzaab
manager: tfehr
ms.date: 07/03/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: mirzaab
ms.search.validFrom: 2020-07-03
ms.dyn365.ops.version: Release 10.0.7
ms.openlocfilehash: 2884c480d20090266f7cffb5e7d0aca58c1174f0
ms.sourcegitcommit: edb46dce498df42b09e8f5ad6de00f86c8022dfa
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 07/03/2020
ms.locfileid: "3534853"
---
# <a name="system-directed-work-sequencing"></a><span data-ttu-id="94c09-105">システム主導の作業優先順位</span><span class="sxs-lookup"><span data-stu-id="94c09-105">System-directed work sequencing</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="94c09-106">システム主導の作業優先順位により、システムが実行のためにユーザーに提示する作業指示書の並べ替えとフィルター処理を行うことができます。</span><span class="sxs-lookup"><span data-stu-id="94c09-106">System-directed work sequencing lets you sort and filter the work orders that the system presents to users for execution.</span></span> <span data-ttu-id="94c09-107">これは、倉庫のピッキングプロセスを実行するために追加の基準 (出荷の時間、ピッキング ゾーン、場所プロファイル、またはさまざまな基準の組み合わせなど) が必要となるシナリオで役立ちます。</span><span class="sxs-lookup"><span data-stu-id="94c09-107">It's helpful in scenarios where additional criteria (such as the time of shipping, the picking zone, the location profile, or a combination of various criteria) are required to drive the warehouse picking process.</span></span>

<span data-ttu-id="94c09-108">この機能は、現在のシステム主導のピッキング機能をシステム主導のクエリ順序を追加することにより拡張します。ユーザーは、作成されたすべての作業指示書を評価する優先順位と 1 つ以上のクエリを設定できます。</span><span class="sxs-lookup"><span data-stu-id="94c09-108">This functionality extends the current system-directed picking functionality by adding a system-directed query order, where users can set up a sequence and one or more queries that will evaluate all work orders that are created.</span></span> <span data-ttu-id="94c09-109">モバイル デバイス メニュー項目の設定で指定された基準を満たす作業指示書のみがキャプチャされ、表示されます。</span><span class="sxs-lookup"><span data-stu-id="94c09-109">Only work orders that meet the criteria that are specified in the setup of the mobile device menu item will be captured and presented.</span></span>

<span data-ttu-id="94c09-110">したがって、この機能により、定義された基準に一致する作業指示書を識別し、それらを適切なモバイル デバイス メニュー項目に割り当て、特定のスキル セット、ピッキング機器、またはその他の要件に基づいて作業者に提示するので、倉庫のピッキング プロセスをさらに最適化できます。</span><span class="sxs-lookup"><span data-stu-id="94c09-110">Therefore, this functionality allows for further optimization of warehouse picking processes as it identifies work orders that match the specified criteria, assigns them to the correct mobile device menu item, and then presents them to a worker, based on a specific skill set, picking equipment, or other requirement.</span></span>

> [!NOTE]
> <span data-ttu-id="94c09-111">異なる基準が必要な場合は、複数のモバイル デバイス メニュー項目を使用する必要があります。</span><span class="sxs-lookup"><span data-stu-id="94c09-111">If different criteria are needed, multiple mobile device menu items must be used.</span></span>

## <a name="turn-on-the-organization-wide-system-directed-work-sequencing-feature"></a><span data-ttu-id="94c09-112">組織全体のシステム主導の作業優先順位機能を有効にする</span><span class="sxs-lookup"><span data-stu-id="94c09-112">Turn on the Organization-wide system directed work sequencing feature</span></span>

<span data-ttu-id="94c09-113">システム主導の作業優先順位を使用するには、システム上でこの機能を有効にする必要があります。</span><span class="sxs-lookup"><span data-stu-id="94c09-113">Before you can use system-directed work sequencing, the feature must be turned on in your system.</span></span> <span data-ttu-id="94c09-114">管理者は、[機能の管理](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) ワークスペースを使用して、機能の状態を確認し、必要に応じて有効にすることができます。</span><span class="sxs-lookup"><span data-stu-id="94c09-114">Admins can use the [Feature management](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) workspace to check the status of the feature and turn it on if it's required.</span></span> <span data-ttu-id="94c09-115">この機能は、次のようにして表示されます。</span><span class="sxs-lookup"><span data-stu-id="94c09-115">There, the feature is listed in the following way:</span></span>

- <span data-ttu-id="94c09-116">**モジュール:** *倉庫管理*</span><span class="sxs-lookup"><span data-stu-id="94c09-116">**Module:** *Warehouse management*</span></span>
- <span data-ttu-id="94c09-117">**機能名:** *組織全体のシステム主導の作業優先順位*</span><span class="sxs-lookup"><span data-stu-id="94c09-117">**Feature name:** *Organization-wide system directed work sequencing*</span></span>

## <a name="setup"></a><span data-ttu-id="94c09-118">セットアップ</span><span class="sxs-lookup"><span data-stu-id="94c09-118">Setup</span></span>

### <a name="make-demo-data-available"></a><span data-ttu-id="94c09-119">デモ データを有効化する</span><span class="sxs-lookup"><span data-stu-id="94c09-119">Make demo data available</span></span>

<span data-ttu-id="94c09-120">このトピックで示されている値を使用してシナリオを実行するには、標準のデモ データがインストールされているシステムで作業する必要があります。</span><span class="sxs-lookup"><span data-stu-id="94c09-120">To work through the scenario by using the values that are presented in this topic, you must work on a system where the standard demo data is installed.</span></span> <span data-ttu-id="94c09-121">また、**USMF** 法人を選択する必要があります。</span><span class="sxs-lookup"><span data-stu-id="94c09-121">Additionally, you must select the **USMF** legal entity.</span></span> <span data-ttu-id="94c09-122">このシナリオでは、デモ データの倉庫 *51* を使用します。</span><span class="sxs-lookup"><span data-stu-id="94c09-122">The scenario uses warehouse *51* from the demo data.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="94c09-123">注文を倉庫にリリースする前に、ピッキング場所に注文のすべての品目に十分な在庫があることを確認してください。</span><span class="sxs-lookup"><span data-stu-id="94c09-123">Before you release the orders to the warehouse, make sure that the pick locations have enough inventory for all the items on the orders.</span></span>
>
> <span data-ttu-id="94c09-124">既定の USMF のデータは、このシナリオをサポートする必要があります。</span><span class="sxs-lookup"><span data-stu-id="94c09-124">Default USMF data should support this scenario.</span></span> <span data-ttu-id="94c09-125">デモ データを使用していない場合は、**場所のディレクティブ**の設定を確認して、どのピッキング場所が販売注文のピッキングに使用されるかを確認します。</span><span class="sxs-lookup"><span data-stu-id="94c09-125">If you aren't using demo data, review the **Location directive** setting to learn which picking locations are used for sales order picking.</span></span> <span data-ttu-id="94c09-126">在庫を調整する必要がある場合には、手動によって移動を作成したり、補充を使用したり、またはその他のフローを使用したりできます。</span><span class="sxs-lookup"><span data-stu-id="94c09-126">If you must adjust the inventory, you can create manual movements, use replenishment, or use any other flow.</span></span>

### <a name="set-up-a-mobile-device-menu-item"></a><span data-ttu-id="94c09-127">モバイル デバイス メニュー項目を設定する</span><span class="sxs-lookup"><span data-stu-id="94c09-127">Set up a mobile device menu item</span></span>

1. <span data-ttu-id="94c09-128">**倉庫管理 \> 設定 \> モバイル デバイス \> モバイル デバイスのメニュー品目**の順に移動します。</span><span class="sxs-lookup"><span data-stu-id="94c09-128">Go to **Warehouse management \> Setup \> Mobile device \> Mobile device menu items**.</span></span>
1. <span data-ttu-id="94c09-129">モバイル デバイス メニュー項目の一覧で、**販売ピッキング – システム**を選択します。</span><span class="sxs-lookup"><span data-stu-id="94c09-129">In the list of mobile device menu items, select **Sales Picking – System**.</span></span> <span data-ttu-id="94c09-130">必須のメニュー項目が既に存在している必要があります。</span><span class="sxs-lookup"><span data-stu-id="94c09-130">The required menu item should already exist.</span></span> 
1. <span data-ttu-id="94c09-131">次の設定を確認します。</span><span class="sxs-lookup"><span data-stu-id="94c09-131">Confirm the following settings:</span></span>

    - <span data-ttu-id="94c09-132">**一般**クイックタブで、**指示者**フィールドを*システム主導*に設定する必要があります。</span><span class="sxs-lookup"><span data-stu-id="94c09-132">On the **General** FastTab, the **Directed by** field should be set to *System directed*.</span></span>
    - <span data-ttu-id="94c09-133">**作業クラス** クイックタブには、次の設定を表示する必要があります。</span><span class="sxs-lookup"><span data-stu-id="94c09-133">The **Work classes** FastTab should show the following settings.</span></span>

        | <span data-ttu-id="94c09-134">作業クラス ID</span><span class="sxs-lookup"><span data-stu-id="94c09-134">Work class ID</span></span> | <span data-ttu-id="94c09-135">ワーク オーダー タイプ</span><span class="sxs-lookup"><span data-stu-id="94c09-135">Work order type</span></span> |
        |---|---|
        | <span data-ttu-id="94c09-136">Sales</span><span class="sxs-lookup"><span data-stu-id="94c09-136">Sales</span></span> | <span data-ttu-id="94c09-137">販売注文</span><span class="sxs-lookup"><span data-stu-id="94c09-137">Sales orders</span></span> |
        | <span data-ttu-id="94c09-138">SO ピッキング</span><span class="sxs-lookup"><span data-stu-id="94c09-138">SO Pick</span></span> | <span data-ttu-id="94c09-139">販売注文</span><span class="sxs-lookup"><span data-stu-id="94c09-139">Sales orders</span></span> |

1. <span data-ttu-id="94c09-140">アクション ウィンドウで、**システム主導の作業シーケンス クエリ**を選択します。</span><span class="sxs-lookup"><span data-stu-id="94c09-140">On the Action Pane, select **System directed work sequence queries**.</span></span>
1. <span data-ttu-id="94c09-141">**編集**を選択します。</span><span class="sxs-lookup"><span data-stu-id="94c09-141">Select **Edit**.</span></span>
1. <span data-ttu-id="94c09-142">既存の明細行を削除し、**はい**を選択してアクションを確認します。</span><span class="sxs-lookup"><span data-stu-id="94c09-142">Delete the existing line, and then confirm the action by selecting **Yes**.</span></span>
1. <span data-ttu-id="94c09-143">アクション ウィンドウで**新規**を選択して、明細行を作成します。</span><span class="sxs-lookup"><span data-stu-id="94c09-143">On the Action Pane, select **New** to create a line.</span></span>
1. <span data-ttu-id="94c09-144">新しい明細行で、次の値を設定します。</span><span class="sxs-lookup"><span data-stu-id="94c09-144">On the new line, set the following values:</span></span>

    - <span data-ttu-id="94c09-145">**シーケンス番号:** *1*</span><span class="sxs-lookup"><span data-stu-id="94c09-145">**Sequence number:** *1*</span></span>
    - <span data-ttu-id="94c09-146">**説明フィールド:** *20 未満の作業数量と降順*</span><span class="sxs-lookup"><span data-stu-id="94c09-146">**Description field:** *Work quantity less than 20 and Descending*</span></span>

1. <span data-ttu-id="94c09-147">**保存** を選択します。</span><span class="sxs-lookup"><span data-stu-id="94c09-147">Select **Save**.</span></span>
1. <span data-ttu-id="94c09-148">アクション ウィンドウで、**クエリの編集**を選択します。</span><span class="sxs-lookup"><span data-stu-id="94c09-148">On the Action Pane, select **Edit Query**.</span></span>
1. <span data-ttu-id="94c09-149">**結合**タブで、結合階層を展開して、**作業明細行**テーブルを表示します。</span><span class="sxs-lookup"><span data-stu-id="94c09-149">On the **Joins** tab, expand the join hierarchy to show the **Work lines** table.</span></span>
1. <span data-ttu-id="94c09-150">**作業明細行**テーブルの結合を選択します。</span><span class="sxs-lookup"><span data-stu-id="94c09-150">Select the **Work lines** table join.</span></span>
1. <span data-ttu-id="94c09-151">**結合するテーブルの追加** を選択します。</span><span class="sxs-lookup"><span data-stu-id="94c09-151">Select **Add table join**.</span></span>
1. <span data-ttu-id="94c09-152">表示される一覧で、次の設定を含む行を検索して選択します。</span><span class="sxs-lookup"><span data-stu-id="94c09-152">In the list that appears, find and select the row that has the following settings:</span></span>

    - <span data-ttu-id="94c09-153">**結合モード:** *n:1*</span><span class="sxs-lookup"><span data-stu-id="94c09-153">**Join mode:** *n:1*</span></span>
    - <span data-ttu-id="94c09-154">**リレーション:** *場所 (保管場所)*</span><span class="sxs-lookup"><span data-stu-id="94c09-154">**Relation:** *Locations (Location)*</span></span>

1. <span data-ttu-id="94c09-155">**選択** を選択します。</span><span class="sxs-lookup"><span data-stu-id="94c09-155">Select **Select**.</span></span>

    <span data-ttu-id="94c09-156">場所はテーブル結合に追加されます。</span><span class="sxs-lookup"><span data-stu-id="94c09-156">Locations are added to the table join.</span></span>

1. <span data-ttu-id="94c09-157">**並べ替え**タブで、**追加**を選択して新しい行を追加します。</span><span class="sxs-lookup"><span data-stu-id="94c09-157">On the **Sorting** tab, select **Add** to add a line.</span></span>
1. <span data-ttu-id="94c09-158">新しい明細行で、次の値を設定します。</span><span class="sxs-lookup"><span data-stu-id="94c09-158">On the new line, set the following values:</span></span>

    - <span data-ttu-id="94c09-159">**表:** *作業明細行*</span><span class="sxs-lookup"><span data-stu-id="94c09-159">**Table:** *Work lines*</span></span>
    - <span data-ttu-id="94c09-160">**派生テーブル:** *作業明細行*</span><span class="sxs-lookup"><span data-stu-id="94c09-160">**Derived table:** *Work lines*</span></span>
    - <span data-ttu-id="94c09-161">**フィールド:** *作業数量* (表示されるメッセージ ボックスで、**はい**を選択してこのフィールドに並べ替えを追加します。)</span><span class="sxs-lookup"><span data-stu-id="94c09-161">**Field:** *Work quantity* (In the message box that appears, select **Yes** to add sorting to this field.)</span></span>
    - <span data-ttu-id="94c09-162">**検索の方向:** *降順*</span><span class="sxs-lookup"><span data-stu-id="94c09-162">**Search direction:** *Descending*</span></span>

1. <span data-ttu-id="94c09-163">**範囲**タブを選択します。</span><span class="sxs-lookup"><span data-stu-id="94c09-163">Select the **Range** tab.</span></span>

    <span data-ttu-id="94c09-164">優先順位に特定の作業基準のみを含める必要がある場合は、**範囲**タブで指定できます。この例では、数量が 20 個 (最小の測定単位) 未満の作業のみを含めます。</span><span class="sxs-lookup"><span data-stu-id="94c09-164">If only specific work criteria should be included in the sequencing, you can specify them on the **Range** tab. In this example, you want to include only work where the quantity is less than 20 ea (the lowest unit of measure).</span></span>

    <span data-ttu-id="94c09-165">一部の明細行が既に含まれていることに注意してください。</span><span class="sxs-lookup"><span data-stu-id="94c09-165">Notice that some lines are already included.</span></span> <span data-ttu-id="94c09-166">これらの明細行は削除しないでください。</span><span class="sxs-lookup"><span data-stu-id="94c09-166">Those lines should not be removed.</span></span>

1. <span data-ttu-id="94c09-167">**追加**を選択して明細行を追加します。</span><span class="sxs-lookup"><span data-stu-id="94c09-167">Select **Add** to add a line.</span></span>
1. <span data-ttu-id="94c09-168">新しい明細行で、次の値を設定します。</span><span class="sxs-lookup"><span data-stu-id="94c09-168">On the new line, set the following values:</span></span>

    - <span data-ttu-id="94c09-169">**表:** *作業明細行*</span><span class="sxs-lookup"><span data-stu-id="94c09-169">**Table:** *Work lines*</span></span>
    - <span data-ttu-id="94c09-170">**派生テーブル:** *作業明細行*</span><span class="sxs-lookup"><span data-stu-id="94c09-170">**Derived table:** *Work lines*</span></span>
    - <span data-ttu-id="94c09-171">**フィールド:** *在庫作業数量*</span><span class="sxs-lookup"><span data-stu-id="94c09-171">**Field:** *Inventory work quantity*</span></span>
    - <span data-ttu-id="94c09-172">**基準:** *\<20* (20 未満)</span><span class="sxs-lookup"><span data-stu-id="94c09-172">**Criteria:** *\<20* (less than 20)</span></span>

1. <span data-ttu-id="94c09-173">**追加**を選択して別の明細行を追加します。</span><span class="sxs-lookup"><span data-stu-id="94c09-173">Select **Add** to add another line.</span></span>
1. <span data-ttu-id="94c09-174">新しい明細行で、次の値を設定します。</span><span class="sxs-lookup"><span data-stu-id="94c09-174">On the new line, set the following values:</span></span>

    - <span data-ttu-id="94c09-175">**表:** *作業明細行*</span><span class="sxs-lookup"><span data-stu-id="94c09-175">**Table:** *Work lines*</span></span>
    - <span data-ttu-id="94c09-176">**派生テーブル:** *作業明細行*</span><span class="sxs-lookup"><span data-stu-id="94c09-176">**Derived table:** *Work lines*</span></span>
    - <span data-ttu-id="94c09-177">**フィールド:** *作業タイプ*</span><span class="sxs-lookup"><span data-stu-id="94c09-177">**Field:** *Work type*</span></span>
    - <span data-ttu-id="94c09-178">**基準:** *ピッキング*</span><span class="sxs-lookup"><span data-stu-id="94c09-178">**Criteria:** *Pick*</span></span>

1. <span data-ttu-id="94c09-179">**追加**を選択して別の明細行を追加します。</span><span class="sxs-lookup"><span data-stu-id="94c09-179">Select **Add** to add another line.</span></span>
1. <span data-ttu-id="94c09-180">新しい明細行で、次の値を設定します。</span><span class="sxs-lookup"><span data-stu-id="94c09-180">On the new line, set the following values:</span></span>

    - <span data-ttu-id="94c09-181">**テーブル:** *場所*</span><span class="sxs-lookup"><span data-stu-id="94c09-181">**Table:** *Locations*</span></span>
    - <span data-ttu-id="94c09-182">**派生テーブル:** *場所*</span><span class="sxs-lookup"><span data-stu-id="94c09-182">**Derived table:** *Locations*</span></span>
    - <span data-ttu-id="94c09-183">\**フィールド:\*\*\*場所のプロファイル ID*</span><span class="sxs-lookup"><span data-stu-id="94c09-183">**Field:** *Location profile ID*</span></span>
    - <span data-ttu-id="94c09-184">**基準:** *!STAGE*</span><span class="sxs-lookup"><span data-stu-id="94c09-184">**Criteria:** *!STAGE*</span></span>

        > [!IMPORTANT]
        > <span data-ttu-id="94c09-185">*STAGE* の前に感嘆符 (*!*) を必ず含めてください。</span><span class="sxs-lookup"><span data-stu-id="94c09-185">Be sure to include the exclamation point (*!*) in front of *STAGE*.</span></span>

1. <span data-ttu-id="94c09-186">**OK** を選択して、クエリを保存して閉じます。</span><span class="sxs-lookup"><span data-stu-id="94c09-186">Select **OK** to save and close the query.</span></span>
1. <span data-ttu-id="94c09-187">**保存** を選択します。</span><span class="sxs-lookup"><span data-stu-id="94c09-187">Select **Save**.</span></span>
1. <span data-ttu-id="94c09-188">ページを閉じて、**モバイル デバイス メニュー項目**ページに戻ります。</span><span class="sxs-lookup"><span data-stu-id="94c09-188">Close the page to return to the **Mobile device menu items** page.</span></span>

> [!NOTE]
> <span data-ttu-id="94c09-189">この設定では、的確な作業をモバイル デバイス メニュー項目に適格な作業を供給するために使用される基準を定義します。</span><span class="sxs-lookup"><span data-stu-id="94c09-189">This setup defines the criteria that will be used to feed eligible work to the mobile device menu item.</span></span> <span data-ttu-id="94c09-190">クエリにさらに基準明細行を追加すると、システムは最初に最小の順序番号を持つクエリ明細行を使用します。</span><span class="sxs-lookup"><span data-stu-id="94c09-190">If you add more criteria lines to the query, the system will use the query line that has lowest sequence number first.</span></span> <span data-ttu-id="94c09-191">言い換えると、最初に順序番号 1 のすべての適格な作業がユーザーに表示され、次に番号順序 2 のすべての作業が表示されます。</span><span class="sxs-lookup"><span data-stu-id="94c09-191">In other words, all eligible work for sequence number 1 will be presented to the user first, and then all work for sequence number 2.</span></span> <span data-ttu-id="94c09-192">したがって、特定の範囲と並べ替えを一緒に使用する必要がある場合は、同じシステム主導の作業順序クエリで指定する必要があります。</span><span class="sxs-lookup"><span data-stu-id="94c09-192">Therefore, if a specific range and sorting must be used together, they should be specified in the same system-directed work sequence query.</span></span>
>
> <span data-ttu-id="94c09-193">この設定では、数量が 20 個未満である明細行が少なくとも 1 行あるすべての作業をキャプチャします。</span><span class="sxs-lookup"><span data-stu-id="94c09-193">This setup will capture any work that has at least one line where the quantity is less than 20 ea.</span></span> <span data-ttu-id="94c09-194">したがって、作業に数量がちょうど 20 個または 20 個より多い明細行がある場合、数量が 20 個未満の明細行も少なくとも 1 つあれば、それは有効になります。</span><span class="sxs-lookup"><span data-stu-id="94c09-194">Therefore, if the work has a line where the quantity is exactly 20 ea or more than 20 ea, it will be valid, provided that it also has at least one line where the quantity is less than 20 ea.</span></span>

### <a name="location-directives"></a><span data-ttu-id="94c09-195">場所のディレクティブ</span><span class="sxs-lookup"><span data-stu-id="94c09-195">Location directives</span></span>

<span data-ttu-id="94c09-196">既定の Contoso データを使用している場合、場所ディレクティブ アクションのクエリを変更する必要はありません。</span><span class="sxs-lookup"><span data-stu-id="94c09-196">If you're using default Contoso data, the query for the location directive action won't require changes.</span></span> <span data-ttu-id="94c09-197">ただし、Contoso 以外の環境でこの機能を適用するときに、場所ディレクティブが販売注文の品目を確実にキャプチャするようにするには、新しい場所ディレクティブを作成します。</span><span class="sxs-lookup"><span data-stu-id="94c09-197">However, to make sure that the location directives will capture the items on the sales orders when you apply the feature in a non-Contoso environment, create a new location directive.</span></span> <span data-ttu-id="94c09-198">デモ環境で設定を確認するには、次の手順を実行します。</span><span class="sxs-lookup"><span data-stu-id="94c09-198">To verify the settings in the demo environment, follow these steps.</span></span>

1. <span data-ttu-id="94c09-199">**倉庫管理** \> **設定** \> **場所ディレクティブ**の順に移動します。</span><span class="sxs-lookup"><span data-stu-id="94c09-199">Go to **Warehouse management** \> **Setup** \> **Location directives**.</span></span>
1. <span data-ttu-id="94c09-200">**ワーク オーダー タイプ** フィールドで、*販売注文*を選択します。</span><span class="sxs-lookup"><span data-stu-id="94c09-200">In the **Work order type** field, select *Sales orders*.</span></span>
1. <span data-ttu-id="94c09-201">*51 ピッキング*という名前の場所ディレクティブを選択します。</span><span class="sxs-lookup"><span data-stu-id="94c09-201">Select the location directive that is named *51 Pick*.</span></span>
1. <span data-ttu-id="94c09-202">**場所ディレクティブ アクション** クイックタブで、**ピッキング** アクションの行を選択します。</span><span class="sxs-lookup"><span data-stu-id="94c09-202">On the **Location Directive Actions** FastTab, select the line for the **Pick** action.</span></span>
1. <span data-ttu-id="94c09-203">グリッドの上にある**クエリの編集**を選択します。</span><span class="sxs-lookup"><span data-stu-id="94c09-203">Select **Edit query** above the grid.</span></span>
1. <span data-ttu-id="94c09-204">**範囲**クエリを確認します。</span><span class="sxs-lookup"><span data-stu-id="94c09-204">Review the **Range** query.</span></span>

    1. <span data-ttu-id="94c09-205">**フィールド** フィールドが*場所*に設定されている行を検索します。</span><span class="sxs-lookup"><span data-stu-id="94c09-205">Find the line where the **Field** field is set to *Location*.</span></span>
    2. <span data-ttu-id="94c09-206">**基準**フィールドが空白になっていることを確認します (つまり、制限はありません)。</span><span class="sxs-lookup"><span data-stu-id="94c09-206">Make sure that the **Criteria** field is blank (that is, there are no restrictions).</span></span>

## <a name="scenario"></a><span data-ttu-id="94c09-207">シナリオ</span><span class="sxs-lookup"><span data-stu-id="94c09-207">Scenario</span></span>

### <a name="create-sales-order-picking-work"></a><span data-ttu-id="94c09-208">販売注文のピッキング作業の作成</span><span class="sxs-lookup"><span data-stu-id="94c09-208">Create sales order picking work</span></span>

<span data-ttu-id="94c09-209">システム主導のピッキングを実行する前に、いくつかの出荷作業を作成する必要があります。</span><span class="sxs-lookup"><span data-stu-id="94c09-209">Before system-directed picking is run, some outbound work should be created.</span></span> <span data-ttu-id="94c09-210">このシナリオでは、指定されたシステム主導の作業順序クエリに基づく 4 つの販売注文を作成します。</span><span class="sxs-lookup"><span data-stu-id="94c09-210">For this scenario, you will create four sales orders that are based on the specified system-directed work sequence queries.</span></span>

<span data-ttu-id="94c09-211">販売注文ごとに在庫数量を引当します。</span><span class="sxs-lookup"><span data-stu-id="94c09-211">You will reserve inventory quantities for each sales order.</span></span> <span data-ttu-id="94c09-212">したがって、在庫引当または在庫引当の一部がキャンセルされない限り、引当済の在庫は他の注文のために倉庫から引き出すことはできません。</span><span class="sxs-lookup"><span data-stu-id="94c09-212">Therefore, reserved inventory can't be withdrawn from the warehouse for other orders unless the inventory reservation, or part of the inventory reservation, is canceled.</span></span>

<span data-ttu-id="94c09-213">次に、各販売注文を倉庫にリリースして、出荷作業を作成します。</span><span class="sxs-lookup"><span data-stu-id="94c09-213">You will then release each sales order to the warehouse to create the outbound work.</span></span>

#### <a name="sales-order-1"></a><span data-ttu-id="94c09-214">販売注文 1</span><span class="sxs-lookup"><span data-stu-id="94c09-214">Sales order 1</span></span>

1. <span data-ttu-id="94c09-215">**販売とマーケティング \> 販売注文 \> すべての販売注文**の順に移動します。</span><span class="sxs-lookup"><span data-stu-id="94c09-215">Go to **Sales and marketing \> Sales orders \> All sales orders**.</span></span>
1. <span data-ttu-id="94c09-216">アクション ウィンドウで、**新規**を選択して、販売注文 1 を作成します。</span><span class="sxs-lookup"><span data-stu-id="94c09-216">On the Action Pane, select **New** to create sales order 1.</span></span>
1. <span data-ttu-id="94c09-217">**販売注文の作成**ダイアログ ボックスでは、次の値を設定します。</span><span class="sxs-lookup"><span data-stu-id="94c09-217">In the **Create sales order** dialog box, set the following values:</span></span>

    - <span data-ttu-id="94c09-218">**顧客**セクションで、**顧客 ID** フィールドを *US-004* に設定します。</span><span class="sxs-lookup"><span data-stu-id="94c09-218">In the **Customer** section, set the **Customer account** field to *US-004*.</span></span>
    - <span data-ttu-id="94c09-219">**一般**セクションで、**倉庫**フィールドを *51* に設定します。</span><span class="sxs-lookup"><span data-stu-id="94c09-219">In the **General** section, set the **Warehouse** field to *51*.</span></span>

1. <span data-ttu-id="94c09-220">**OK** を選択してダイアログ ボックスを閉じます。</span><span class="sxs-lookup"><span data-stu-id="94c09-220">Select **OK** to close the dialog box.</span></span> <span data-ttu-id="94c09-221">販売注文番号をメモします。</span><span class="sxs-lookup"><span data-stu-id="94c09-221">Make a note of the sales order number.</span></span>
1. <span data-ttu-id="94c09-222">新しい販売注文に明細行を追加し、次の値を設定します。</span><span class="sxs-lookup"><span data-stu-id="94c09-222">Add a line to the new sales order, and set the following values:</span></span>

    - <span data-ttu-id="94c09-223">**品目番号:** *M9200*</span><span class="sxs-lookup"><span data-stu-id="94c09-223">**Item number:** *M9200*</span></span>
    - <span data-ttu-id="94c09-224">**数量:** *20*</span><span class="sxs-lookup"><span data-stu-id="94c09-224">**Quantity:** *20*</span></span>

1. <span data-ttu-id="94c09-225">グリッドの上部にある**在庫**メニューで、**引当**を選択します。</span><span class="sxs-lookup"><span data-stu-id="94c09-225">On the **Inventory** menu above the grid, select **Reservation**.</span></span>
1. <span data-ttu-id="94c09-226">**引当**ページで、**引当ロット**を選択して、在庫を引当します。</span><span class="sxs-lookup"><span data-stu-id="94c09-226">On the **Reservation** page, select **Reserve lot** to reserve the inventory.</span></span>
1. <span data-ttu-id="94c09-227">**引当**ページを閉じます。</span><span class="sxs-lookup"><span data-stu-id="94c09-227">Close the **Reservation** page.</span></span>
1. <span data-ttu-id="94c09-228">アクション ウィンドウの**倉庫**タブで、**倉庫へのリリース**を選択して、倉庫の作業を作成します。</span><span class="sxs-lookup"><span data-stu-id="94c09-228">On the Action Pane, on the **Warehouse** tab, select **Release to warehouse** to create work for the warehouse.</span></span>

    <span data-ttu-id="94c09-229">この販売注文に対して作成されたウェーブ ID および出荷 ID を示す情報メッセージが表示されます。</span><span class="sxs-lookup"><span data-stu-id="94c09-229">You receive informational messages that show the wave ID and shipment IDs that were created for the sales order.</span></span>

#### <a name="sales-order-2"></a><span data-ttu-id="94c09-230">販売注文 2</span><span class="sxs-lookup"><span data-stu-id="94c09-230">Sales order 2</span></span>

1. <span data-ttu-id="94c09-231">アクション ウィンドウで、**新規**を選択して、販売注文 2 を作成します。</span><span class="sxs-lookup"><span data-stu-id="94c09-231">On the Action Pane, select **New** to create sales order 2.</span></span>
1. <span data-ttu-id="94c09-232">**販売注文の作成**ダイアログ ボックスでは、次の値を設定します。</span><span class="sxs-lookup"><span data-stu-id="94c09-232">In the **Create sales order** dialog box, set the following values:</span></span>

    - <span data-ttu-id="94c09-233">**顧客アカウント:** *US-007*</span><span class="sxs-lookup"><span data-stu-id="94c09-233">**Customer account:** *US-007*</span></span>
    - <span data-ttu-id="94c09-234">**倉庫:** *51*</span><span class="sxs-lookup"><span data-stu-id="94c09-234">**Warehouse:** *51*</span></span>

1. <span data-ttu-id="94c09-235">**OK** を選択してダイアログ ボックスを閉じます。</span><span class="sxs-lookup"><span data-stu-id="94c09-235">Select **OK** to close the dialog box.</span></span> <span data-ttu-id="94c09-236">販売注文番号をメモします。</span><span class="sxs-lookup"><span data-stu-id="94c09-236">Make a note of the sales order number.</span></span>
1. <span data-ttu-id="94c09-237">新しい販売注文に明細行を追加し、次の値を設定します。</span><span class="sxs-lookup"><span data-stu-id="94c09-237">Add a line to the new sales order, and set the following values:</span></span>

    - <span data-ttu-id="94c09-238">**品目番号:** *M9200*</span><span class="sxs-lookup"><span data-stu-id="94c09-238">**Item number:** *M9200*</span></span>
    - <span data-ttu-id="94c09-239">**数量:** *5*</span><span class="sxs-lookup"><span data-stu-id="94c09-239">**Quantity:** *5*</span></span>

1. <span data-ttu-id="94c09-240">**明細行の追加**を選択して、2 行目を追加し、次の値を設定します。</span><span class="sxs-lookup"><span data-stu-id="94c09-240">Select **Add line** to add a second line, and set the following values:</span></span>

    - <span data-ttu-id="94c09-241">**品目番号:** *M9201*</span><span class="sxs-lookup"><span data-stu-id="94c09-241">**Item number:** *M9201*</span></span>
    - <span data-ttu-id="94c09-242">**数量:** *1*</span><span class="sxs-lookup"><span data-stu-id="94c09-242">**Quantity:** *1*</span></span>

1. <span data-ttu-id="94c09-243">両方の明細行の在庫を引当します。</span><span class="sxs-lookup"><span data-stu-id="94c09-243">Reserve inventory for both lines.</span></span>
1. <span data-ttu-id="94c09-244">注文を倉庫にリリースします。</span><span class="sxs-lookup"><span data-stu-id="94c09-244">Release the order to the warehouse.</span></span>

#### <a name="sales-order-3"></a><span data-ttu-id="94c09-245">販売注文 3</span><span class="sxs-lookup"><span data-stu-id="94c09-245">Sales order 3</span></span>

1. <span data-ttu-id="94c09-246">アクション ウィンドウで、**新規**を選択して、販売注文 3 を作成します。</span><span class="sxs-lookup"><span data-stu-id="94c09-246">On the Action Pane, select **New** to create sales order 3.</span></span>
1. <span data-ttu-id="94c09-247">**販売注文の作成**ダイアログ ボックスでは、次の値を設定します。</span><span class="sxs-lookup"><span data-stu-id="94c09-247">In the **Create sales order** dialog box, set the following values:</span></span>

    - <span data-ttu-id="94c09-248">**顧客アカウント:** *US-009*</span><span class="sxs-lookup"><span data-stu-id="94c09-248">**Customer account:** *US-009*</span></span>
    - <span data-ttu-id="94c09-249">**倉庫:** *51*</span><span class="sxs-lookup"><span data-stu-id="94c09-249">**Warehouse:** *51*</span></span>

1. <span data-ttu-id="94c09-250">**OK** を選択してダイアログ ボックスを閉じます。</span><span class="sxs-lookup"><span data-stu-id="94c09-250">Select **OK** to close the dialog box.</span></span> <span data-ttu-id="94c09-251">販売注文番号をメモします。</span><span class="sxs-lookup"><span data-stu-id="94c09-251">Make a note of the sales order number.</span></span>
1. <span data-ttu-id="94c09-252">新しい販売注文に明細行を追加し、次の値を設定します。</span><span class="sxs-lookup"><span data-stu-id="94c09-252">Add a line to the new sales order, and set the following values:</span></span>

    - <span data-ttu-id="94c09-253">**品目番号:** *M9200*</span><span class="sxs-lookup"><span data-stu-id="94c09-253">**Item number:** *M9200*</span></span>
    - <span data-ttu-id="94c09-254">**数量:** *7*</span><span class="sxs-lookup"><span data-stu-id="94c09-254">**Quantity:** *7*</span></span>

1. <span data-ttu-id="94c09-255">**明細行の追加**を選択して、2 行目を追加し、次の値を設定します。</span><span class="sxs-lookup"><span data-stu-id="94c09-255">Select **Add line** to add a second line, and set the following values:</span></span>

    - <span data-ttu-id="94c09-256">**品目番号:** *M9202*</span><span class="sxs-lookup"><span data-stu-id="94c09-256">**Item number:** *M9202*</span></span>
    - <span data-ttu-id="94c09-257">**数量:** *8*</span><span class="sxs-lookup"><span data-stu-id="94c09-257">**Quantity:** *8*</span></span>

1. <span data-ttu-id="94c09-258">両方の明細行の在庫を引当します。</span><span class="sxs-lookup"><span data-stu-id="94c09-258">Reserve inventory for both lines.</span></span>
1. <span data-ttu-id="94c09-259">注文を倉庫にリリースします。</span><span class="sxs-lookup"><span data-stu-id="94c09-259">Release the order to the warehouse.</span></span>

#### <a name="sales-order-4"></a><span data-ttu-id="94c09-260">販売注文 4</span><span class="sxs-lookup"><span data-stu-id="94c09-260">Sales order 4</span></span>

1. <span data-ttu-id="94c09-261">アクション ウィンドウで、**新規**を選択して、販売注文 4 を作成します。</span><span class="sxs-lookup"><span data-stu-id="94c09-261">On the Action Pane, select **New** to create sales order 4.</span></span>
1. <span data-ttu-id="94c09-262">**販売注文の作成**ダイアログ ボックスでは、次の値を設定します。</span><span class="sxs-lookup"><span data-stu-id="94c09-262">In the **Create sales order** dialog box, set the following values:</span></span>

    - <span data-ttu-id="94c09-263">**顧客アカウント:** *US-010*</span><span class="sxs-lookup"><span data-stu-id="94c09-263">**Customer account:** *US-010*</span></span>
    - <span data-ttu-id="94c09-264">**倉庫:** *51*</span><span class="sxs-lookup"><span data-stu-id="94c09-264">**Warehouse:** *51*</span></span>

1. <span data-ttu-id="94c09-265">**OK** を選択してダイアログ ボックスを閉じます。</span><span class="sxs-lookup"><span data-stu-id="94c09-265">Select **OK** to close the dialog box.</span></span> <span data-ttu-id="94c09-266">販売注文番号をメモします。</span><span class="sxs-lookup"><span data-stu-id="94c09-266">Make a note of the sales order number.</span></span>
1. <span data-ttu-id="94c09-267">新しい販売注文に明細行を追加し、次の値を設定します。</span><span class="sxs-lookup"><span data-stu-id="94c09-267">Add a line to the new sales order, and set the following values:</span></span>

    - <span data-ttu-id="94c09-268">**品目番号:** *M9200*</span><span class="sxs-lookup"><span data-stu-id="94c09-268">**Item number:** *M9200*</span></span>
    - <span data-ttu-id="94c09-269">**数量:** *25*</span><span class="sxs-lookup"><span data-stu-id="94c09-269">**Quantity:** *25*</span></span>

1. <span data-ttu-id="94c09-270">**明細行の追加**を選択して、2 行目を追加し、次の値を設定します。</span><span class="sxs-lookup"><span data-stu-id="94c09-270">Select **Add line** to add a second line, and set the following values:</span></span>

    - <span data-ttu-id="94c09-271">**品目番号:** *M9202*</span><span class="sxs-lookup"><span data-stu-id="94c09-271">**Item number:** *M9202*</span></span>
    - <span data-ttu-id="94c09-272">**数量:** *10*</span><span class="sxs-lookup"><span data-stu-id="94c09-272">**Quantity:** *10*</span></span>

1. <span data-ttu-id="94c09-273">両方の明細行の在庫を引当します。</span><span class="sxs-lookup"><span data-stu-id="94c09-273">Reserve inventory for both lines.</span></span>
1. <span data-ttu-id="94c09-274">注文を倉庫にリリースします。</span><span class="sxs-lookup"><span data-stu-id="94c09-274">Release the order to the warehouse.</span></span>

### <a name="get-work-ids-for-the-work-that-was-created"></a><span data-ttu-id="94c09-275">作成された作業の作業 ID を取得する</span><span class="sxs-lookup"><span data-stu-id="94c09-275">Get work IDs for the work that was created</span></span>

1. <span data-ttu-id="94c09-276">**倉庫管理 \> 作業 \> 作業の詳細**の順に移動します。</span><span class="sxs-lookup"><span data-stu-id="94c09-276">Go to **Warehouse management \> Work \> Work details**.</span></span>
1. <span data-ttu-id="94c09-277">**倉庫**フィールドでフィルター処理して、倉庫 *51* の作業のみが表示されるようにします。</span><span class="sxs-lookup"><span data-stu-id="94c09-277">Filter on the **Warehouse** field so that only work for warehouse *51* is shown.</span></span>
1. <span data-ttu-id="94c09-278">4 つの作業 ID が作成されている必要があります。</span><span class="sxs-lookup"><span data-stu-id="94c09-278">Four work IDs should have been created.</span></span> <span data-ttu-id="94c09-279">各販売注文の作業 ID をメモします。</span><span class="sxs-lookup"><span data-stu-id="94c09-279">Make a note of the work ID for each sales order.</span></span>

    | <span data-ttu-id="94c09-280">販売注文 ID</span><span class="sxs-lookup"><span data-stu-id="94c09-280">Sales order ID</span></span> | <span data-ttu-id="94c09-281">作業 ID</span><span class="sxs-lookup"><span data-stu-id="94c09-281">Work ID</span></span> | <span data-ttu-id="94c09-282">作業数量</span><span class="sxs-lookup"><span data-stu-id="94c09-282">Work quantity</span></span> |
    |---|---|---|
    | <span data-ttu-id="94c09-283">販売注文 1</span><span class="sxs-lookup"><span data-stu-id="94c09-283">Sales Order 1</span></span> | <span data-ttu-id="94c09-284">作業 ID 1</span><span class="sxs-lookup"><span data-stu-id="94c09-284">Work ID 1</span></span> | <span data-ttu-id="94c09-285">20 個体</span><span class="sxs-lookup"><span data-stu-id="94c09-285">20 ea</span></span> |
    | <span data-ttu-id="94c09-286">販売注文 2</span><span class="sxs-lookup"><span data-stu-id="94c09-286">Sales Order 2</span></span> | <span data-ttu-id="94c09-287">作業 ID 2</span><span class="sxs-lookup"><span data-stu-id="94c09-287">Work ID 2</span></span> | <span data-ttu-id="94c09-288">6 個 (両方の明細行の合計)</span><span class="sxs-lookup"><span data-stu-id="94c09-288">6 ea (sum of both lines)</span></span> |
    | <span data-ttu-id="94c09-289">販売注文 3</span><span class="sxs-lookup"><span data-stu-id="94c09-289">Sales Order 3</span></span> | <span data-ttu-id="94c09-290">作業 ID 3</span><span class="sxs-lookup"><span data-stu-id="94c09-290">Work ID 3</span></span> | <span data-ttu-id="94c09-291">15 個 (両方の明細行の合計)</span><span class="sxs-lookup"><span data-stu-id="94c09-291">15 ea (sum of both lines)</span></span> |
    | <span data-ttu-id="94c09-292">販売注文 4</span><span class="sxs-lookup"><span data-stu-id="94c09-292">Sales Order 4</span></span> | <span data-ttu-id="94c09-293">作業 ID 4</span><span class="sxs-lookup"><span data-stu-id="94c09-293">Work ID 4</span></span> | <span data-ttu-id="94c09-294">35 個 (両方の明細行の合計)</span><span class="sxs-lookup"><span data-stu-id="94c09-294">35 ea (sum of both lines)</span></span> |

<span data-ttu-id="94c09-295">モバイル デバイスでフローを実行する前に、作成したばかりの作業のみが、倉庫 *51* および*販売注文*の作業指示書タイプで*オープン*状態にあることを確認してください。</span><span class="sxs-lookup"><span data-stu-id="94c09-295">Before you run the flow on the mobile device, make sure that only the work that you just created is in *Open* status for warehouse *51* and the *Sales order* work order type.</span></span> <span data-ttu-id="94c09-296">それ以外の場合、システム主導のピッキングにはすべての適格な作業が含まれるため、テストの結果は異なる場合があります。</span><span class="sxs-lookup"><span data-stu-id="94c09-296">Otherwise, the results of the test might vary, because the system-direct picking will include all eligible work.</span></span>

1. <span data-ttu-id="94c09-297">**倉庫管理 \> 作業 \> 出荷 \> オープン販売作業**の順に移動します。</span><span class="sxs-lookup"><span data-stu-id="94c09-297">Go to **Warehouse management \> Work \> Outbound \> Open sales work**.</span></span>
1. <span data-ttu-id="94c09-298">**オープン販売作業**グリッドの**倉庫**フィールドでフィルター処理して、倉庫 *51* の作業のみが表示されるようにします。</span><span class="sxs-lookup"><span data-stu-id="94c09-298">In the **Open sales work** grid, filter on the **Warehouse** field so that only work for warehouse *51* is shown.</span></span>
1. <span data-ttu-id="94c09-299">先ほど作成した 4 つの作業 ID のみが表示されていることを確認します。</span><span class="sxs-lookup"><span data-stu-id="94c09-299">Confirm that only the four work IDs that you created earlier are shown.</span></span>
1. <span data-ttu-id="94c09-300">**作業**ページを閉じます。</span><span class="sxs-lookup"><span data-stu-id="94c09-300">Close the **Work** page.</span></span>

### <a name="mobile-device-flow-execution"></a><span data-ttu-id="94c09-301">モバイル デバイス フローの実行</span><span class="sxs-lookup"><span data-stu-id="94c09-301">Mobile device flow execution</span></span>

<span data-ttu-id="94c09-302">設定に基づいて、システムは、ユーザーの作業を作業明細行の数量が最も多いものから最も少ないものへと並べ替えて提供します。</span><span class="sxs-lookup"><span data-stu-id="94c09-302">Based on the setup, the system will feed the user work that is sorted from the highest work line quantity to the lowest.</span></span> <span data-ttu-id="94c09-303">各明細行の数量は、20 個未満になります。</span><span class="sxs-lookup"><span data-stu-id="94c09-303">The quantity on every line will be less than 20 ea.</span></span>

<span data-ttu-id="94c09-304">この設定では、数量が 20 個未満である明細行が少なくとも 1 行あるすべての作業がキャプチャされることに注意してください。</span><span class="sxs-lookup"><span data-stu-id="94c09-304">Remember that this setup will capture any work that has at least one line where the quantity is less than 20 ea.</span></span> <span data-ttu-id="94c09-305">したがって、作業に数量が 20 個または 20 個を超える別の明細行がある場合も、有効になります。</span><span class="sxs-lookup"><span data-stu-id="94c09-305">Therefore, if the work has another line where the quantity is exactly 20 ea or more than 20 ea, it will also be valid.</span></span>

#### <a name="mobile-app"></a><span data-ttu-id="94c09-306">モバイル アプリ</span><span class="sxs-lookup"><span data-stu-id="94c09-306">Mobile app</span></span>

1. <span data-ttu-id="94c09-307">倉庫 *51* にいるユーザーとして倉庫アプリにサインインします。</span><span class="sxs-lookup"><span data-stu-id="94c09-307">Sign in to the warehousing app as a user in warehouse *51*.</span></span>
1. <span data-ttu-id="94c09-308">**出荷 \> 販売ピッキング - システム**に移動します。</span><span class="sxs-lookup"><span data-stu-id="94c09-308">Go to **Outbound \> Sales Picking - System**.</span></span>

    <span data-ttu-id="94c09-309">作業 ID *4* のピッキング ステップが表示されます。</span><span class="sxs-lookup"><span data-stu-id="94c09-309">The pick step for work ID *4* is presented.</span></span> <span data-ttu-id="94c09-310">この作業 ID が最初に表示されるのは、システム主導のクエリ順序が設定されているためです。ここで、作業は降順の作業明細行の数量に基づいて順序付けする必要があると指定しました。</span><span class="sxs-lookup"><span data-stu-id="94c09-310">This work ID is presented first because of the setup of the system-directed query order, where you specified that work should be sequenced based on descending work line quantity.</span></span>

1. <span data-ttu-id="94c09-311">必要なピッキングを完了し、プットして作業 ID を閉じます。</span><span class="sxs-lookup"><span data-stu-id="94c09-311">Complete the required pick and put to close the work ID.</span></span>

    <span data-ttu-id="94c09-312">次に、作業 ID *3* が表示されます。</span><span class="sxs-lookup"><span data-stu-id="94c09-312">Next, work ID *3* is presented.</span></span> <span data-ttu-id="94c09-313">作業ラインの数量に基づいて、その作業ラインの 1 つは、順序で次になります。</span><span class="sxs-lookup"><span data-stu-id="94c09-313">One of its work lines is next in the sequence, based on the work line quantity.</span></span>

1. <span data-ttu-id="94c09-314">ピッキングを完了し、プットして作業 ID を閉じます。</span><span class="sxs-lookup"><span data-stu-id="94c09-314">Complete the pick and put to close the work ID.</span></span>

    <span data-ttu-id="94c09-315">次に、作業 ID *2* が表示されます。</span><span class="sxs-lookup"><span data-stu-id="94c09-315">Next, work ID *2* is presented.</span></span> <span data-ttu-id="94c09-316">この作業のピッキング行は順序で次になります。</span><span class="sxs-lookup"><span data-stu-id="94c09-316">This work's pick line is next in the sequence.</span></span>

1. <span data-ttu-id="94c09-317">ピッキングを完了し、プットして作業 ID を閉じます。</span><span class="sxs-lookup"><span data-stu-id="94c09-317">Complete the pick and put to close the work ID.</span></span>

    <span data-ttu-id="94c09-318">これ以上の作業は表示されません。</span><span class="sxs-lookup"><span data-stu-id="94c09-318">No further work should be presented to you.</span></span> <span data-ttu-id="94c09-319">作業 ID *1* は、このモバイル デバイス メニュー項目の対象となっていません。作業明細行の数量が 20 個未満の場合にのみ作業ヘッダーが考慮されることをクエリが指定しているためです。</span><span class="sxs-lookup"><span data-stu-id="94c09-319">Work ID *1* isn't eligible for this mobile device menu item, because the query specifies that work headers are considered only if the quantity on the work lines is less than 20 ea.</span></span>

## <a name="tips"></a><span data-ttu-id="94c09-320">ヒント</span><span class="sxs-lookup"><span data-stu-id="94c09-320">Tips</span></span>

<span data-ttu-id="94c09-321">システム主導の作業シーケンス クエリは*包括的*です。</span><span class="sxs-lookup"><span data-stu-id="94c09-321">The system-directed work sequence queries are *inclusive*.</span></span> <span data-ttu-id="94c09-322">一部の設定では、この事実を覚えておくことが重要です。</span><span class="sxs-lookup"><span data-stu-id="94c09-322">It's important that you remember this fact for some setups.</span></span> <span data-ttu-id="94c09-323">たとえば、特定のメニュー項目で、作業単位が*個*である作業のみを処理するとします。クエリの**範囲**タブでその制限を指定します。</span><span class="sxs-lookup"><span data-stu-id="94c09-323">For example, you want a specific menu item to process only work where the work unit is *ea*, and you specify that restriction on the **Range** tab of the query.</span></span> <span data-ttu-id="94c09-324">この場合、少なくとも 1 つの作業明細行で、作業単位が*個*に設定されているすべての作業は、作業者に提供されます。</span><span class="sxs-lookup"><span data-stu-id="94c09-324">In this case, all work where at least one work line has the work unit set to *ea* will be fed to the worker.</span></span> <span data-ttu-id="94c09-325">したがって、この作業には、作業明細行の*個*以外の作業単位 (*ボックス*や*パレット*など) が含まれる場合もあります。</span><span class="sxs-lookup"><span data-stu-id="94c09-325">Therefore, this work might also include work where work lines have a work unit other than *ea* (such as *box* or *pallet*).</span></span> <span data-ttu-id="94c09-326">クエリは、作業単位が*個*に設定されている作業ラインがない作業のみを除外します。</span><span class="sxs-lookup"><span data-stu-id="94c09-326">The query will exclude only work where no work line has the work unit set to *ea*.</span></span>

<span data-ttu-id="94c09-327">したがって、このシナリオの例では、作業ID *4* もクエリでキャプチャされていました。</span><span class="sxs-lookup"><span data-stu-id="94c09-327">Therefore, in the example from this scenario, work ID *4* was also captured by the query.</span></span> <span data-ttu-id="94c09-328">作成されたときに 2 つの明細行が追加されました。1 つは 25 個、もう 1 つは 10 個です。</span><span class="sxs-lookup"><span data-stu-id="94c09-328">When it was created, two lines were added: one for 25 ea and another for 10 ea.</span></span> <span data-ttu-id="94c09-329">少なくとも 1 つの作業ラインには、20 個未満の数量があるため、作業は引き続きユーザーに表示されました。</span><span class="sxs-lookup"><span data-stu-id="94c09-329">The work was still presented to the user, because at least one work line has a quantity of less than 20 ea.</span></span>

<span data-ttu-id="94c09-330">シナリオによっては、作業の分割を使用して、この動作を回避することができます。</span><span class="sxs-lookup"><span data-stu-id="94c09-330">Depending on the scenario, you can prevent this behavior by using work breaks.</span></span>
