---
title: 場所ライセンス プレートの配置
description: ライセンス プレートの場所の配置を使用すると、ライセンス プレートが複数パレットの場所 (たとえば、2つの深いパレットのラック配置を使用する場所など) を表示できます。
author: Mirzaab
manager: tfehr
ms.date: 07/01/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: WHSLicensePlate, WHSLocationProfile, WHSLocDirTable
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: mirzaab
ms.search.validFrom: 2020-07-01
ms.dyn365.ops.version: Release 10.0.7
ms.openlocfilehash: cfab8c36adb08f799305a153589926bfc1ae31fe
ms.sourcegitcommit: eaf330dbee1db96c20d5ac479f007747bea079eb
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 02/15/2021
ms.locfileid: "5217104"
---
# <a name="location-license-plate-positioning"></a><span data-ttu-id="b75ac-103">場所ライセンス プレートの配置</span><span class="sxs-lookup"><span data-stu-id="b75ac-103">Location license plate positioning</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="b75ac-104">ライセンス プレートの場所の配置を使用すると、ライセンス プレートが複数パレットの場所 (たとえば、2つの深いパレットのラック配置を使用する場所など) を表示できます。</span><span class="sxs-lookup"><span data-stu-id="b75ac-104">License plate location positioning lets you see where a license plate is located in a multi-pallet location, such as a location that uses double-deep pallet racking.</span></span>

<span data-ttu-id="b75ac-105">この機能により、保管場所に格納されている各ライセンス プレートにシーケンス番号が追加されます。</span><span class="sxs-lookup"><span data-stu-id="b75ac-105">The feature adds a sequence number to each license plate that is put into a storage location.</span></span> <span data-ttu-id="b75ac-106">このシーケンス番号は、保存場所でライセンス プレートを順序付けるために使用されます。</span><span class="sxs-lookup"><span data-stu-id="b75ac-106">This sequence number is used to order the license plates in the storage location.</span></span> <span data-ttu-id="b75ac-107">したがって、この機能は、顧客が重力ラッキング システムを使用していて、どのライセンス プレートが前面にあるかを把握しておく必要があるシナリオをインテリジェントにサポートします。</span><span class="sxs-lookup"><span data-stu-id="b75ac-107">Therefore, the feature intelligently supports scenarios where customers are using a gravity racking system and must know, for picking purposes, which license plate is front-facing.</span></span>

<span data-ttu-id="b75ac-108">このトピックでは、機能を設定および使用する方法を示すシナリオを示します。</span><span class="sxs-lookup"><span data-stu-id="b75ac-108">This topic presents a scenario that shows how to set up and use the feature.</span></span>

## <a name="turn-on-the-location-license-plate-positioning-feature"></a><span data-ttu-id="b75ac-109">場所ライセンス プレートの配置機能を有効にする</span><span class="sxs-lookup"><span data-stu-id="b75ac-109">Turn on the Location license plate positioning feature</span></span>

<span data-ttu-id="b75ac-110">ライセンス プレートの場所の配置機能を使用するには、システム上で有効にする必要があります。</span><span class="sxs-lookup"><span data-stu-id="b75ac-110">Before you can use license plate location positioning, the feature must be turned on in your system.</span></span> <span data-ttu-id="b75ac-111">管理者は、[機能の管理](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) ワークスペースを使用して、機能の状態を確認し、必要に応じて有効にすることができます。</span><span class="sxs-lookup"><span data-stu-id="b75ac-111">Admins can use the [Feature management](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) workspace to check the status of the feature and turn it on if it's required.</span></span> <span data-ttu-id="b75ac-112">この機能は、次のようにして表示されます。</span><span class="sxs-lookup"><span data-stu-id="b75ac-112">There, the feature is listed in the following way:</span></span>

- <span data-ttu-id="b75ac-113">**モジュール:** *倉庫管理*</span><span class="sxs-lookup"><span data-stu-id="b75ac-113">**Module:** *Warehouse management*</span></span>
- <span data-ttu-id="b75ac-114">**機能名 :** *場所ライセンス プレートの配置*</span><span class="sxs-lookup"><span data-stu-id="b75ac-114">**Feature name:** *Location license plate positioning*</span></span>

## <a name="example-scenario"></a><span data-ttu-id="b75ac-115">シナリオ例</span><span class="sxs-lookup"><span data-stu-id="b75ac-115">Example scenario</span></span>

### <a name="make-sample-data-available"></a><span data-ttu-id="b75ac-116">サンプル データを有効化する</span><span class="sxs-lookup"><span data-stu-id="b75ac-116">Make sample data available</span></span>

<span data-ttu-id="b75ac-117">ここで推奨されている値を使用してこのシナリオを実行するには、サンプル データがインストールされているシステム上で作業する必要があります。</span><span class="sxs-lookup"><span data-stu-id="b75ac-117">To work through this scenario by using the values that are suggested here, you must work on a system where sample data is installed.</span></span> <span data-ttu-id="b75ac-118">また、開始する前に **USMF** 法人を選択する必要があります。</span><span class="sxs-lookup"><span data-stu-id="b75ac-118">Additionally, you must select the **USMF** legal entity before you start.</span></span>

### <a name="set-up-the-feature-for-this-scenario"></a><span data-ttu-id="b75ac-119">このシナリオの機能の設定</span><span class="sxs-lookup"><span data-stu-id="b75ac-119">Set up the feature for this scenario</span></span>

<span data-ttu-id="b75ac-120">次の手順を完了して、このトピックに示されているシナリオの *場所ライセンス プレートの配置* 機能を設定します。</span><span class="sxs-lookup"><span data-stu-id="b75ac-120">Complete the following procedures to set up the *Location license plate positioning* feature for the scenario that is presented in this topic.</span></span>

#### <a name="location-profiles"></a><span data-ttu-id="b75ac-121">場所プロファイル</span><span class="sxs-lookup"><span data-stu-id="b75ac-121">Location profiles</span></span>

<span data-ttu-id="b75ac-122">この機能は、使用するすべての場所の場所プロファイルでオンになっている必要があります。</span><span class="sxs-lookup"><span data-stu-id="b75ac-122">The feature must be turned on in the location profile for every location where it will be used.</span></span>

1. <span data-ttu-id="b75ac-123">**倉庫管理 \> 設定 \> 倉庫 \> 場所プロファイル** に移動します。</span><span class="sxs-lookup"><span data-stu-id="b75ac-123">Go to **Warehouse management \> Setup \> Warehouse \> Location profiles**.</span></span>
1. <span data-ttu-id="b75ac-124">左ウィンドウの場所プロファイルの一覧で、**バルク-06** を選択します。</span><span class="sxs-lookup"><span data-stu-id="b75ac-124">In the list of location profiles in the left pane, select **BULK-06**.</span></span>
1. <span data-ttu-id="b75ac-125">**一般** クイック タブに、この機能によって 2 つの新しいオプションが追加されています。</span><span class="sxs-lookup"><span data-stu-id="b75ac-125">On the **General** FastTab, two new options have been added by the feature.</span></span> <span data-ttu-id="b75ac-126">次の値を設定します。</span><span class="sxs-lookup"><span data-stu-id="b75ac-126">Set the following values:</span></span>

    - <span data-ttu-id="b75ac-127">**ライセンス プレートの位置の有効化 :** *はい*</span><span class="sxs-lookup"><span data-stu-id="b75ac-127">**Enable license plate position:** *Yes*</span></span>

        <span data-ttu-id="b75ac-128">このオプションを *はい* に設定すると、その場所のライセンス プレートに対して、ライセンス プレートの位置が維持されます。</span><span class="sxs-lookup"><span data-stu-id="b75ac-128">When this option is set to *Yes*, the license plate position will be maintained for license plates in the location.</span></span>

    - <span data-ttu-id="b75ac-129">**モバイル デバイスの LP の位置を表示する :** *はい*</span><span class="sxs-lookup"><span data-stu-id="b75ac-129">**Display mobile device LP position:** *Yes*</span></span>

        <span data-ttu-id="b75ac-130">このオプションを *はい* に設定すると、調整および棚卸時にモバイル デバイスのユーザーに対してライセンス プレートの位置が表示されます。</span><span class="sxs-lookup"><span data-stu-id="b75ac-130">When this option is set to *Yes*, the license plate position will be shown to mobile device users during adjustment and counting.</span></span> <span data-ttu-id="b75ac-131">このオプションの設定を変更できるのは、機能が有効になっている場合に限られます。</span><span class="sxs-lookup"><span data-stu-id="b75ac-131">You can change the setting of this option only when the feature is turned on.</span></span>

1. <span data-ttu-id="b75ac-132">**保存** を選択します。</span><span class="sxs-lookup"><span data-stu-id="b75ac-132">Select **Save**.</span></span>

#### <a name="location-directives"></a><span data-ttu-id="b75ac-133">場所のディレクティブ</span><span class="sxs-lookup"><span data-stu-id="b75ac-133">Location directives</span></span>

1. <span data-ttu-id="b75ac-134">**倉庫管理 \> 設定 \> 場所のディレクティブ** に移動します。</span><span class="sxs-lookup"><span data-stu-id="b75ac-134">Go to **Warehouse management \> Setup \> Location directives**.</span></span>
1. <span data-ttu-id="b75ac-135">左ウィンドウで、**作業指示書の種類** フィールドが *販売注文* に設定されていることを確認します。</span><span class="sxs-lookup"><span data-stu-id="b75ac-135">In the left pane, make sure that the **Work order type** field is set to *Sales orders*.</span></span>
1. <span data-ttu-id="b75ac-136">場所ディレクティブの一覧で、**61 SO ピッキング オーダー** を選択します。</span><span class="sxs-lookup"><span data-stu-id="b75ac-136">In the list of location directives, select **61 SO Pick order**.</span></span>
1. <span data-ttu-id="b75ac-137">アクション ウィンドウで、**編集** を選択します。</span><span class="sxs-lookup"><span data-stu-id="b75ac-137">On the Action Pane, select **Edit**.</span></span>
1. <span data-ttu-id="b75ac-138">**明細行** クイック タブで、**シーケンス番号** の値が *2* の明細行を選択します。</span><span class="sxs-lookup"><span data-stu-id="b75ac-138">On the **Lines** FastTab, select the line that has a **Sequence number** value of *2*.</span></span>
1. <span data-ttu-id="b75ac-139">**場所ディレクティブ アクション** クイック タブで、**名前** の値が *パレットよりも少なくピッキング* に設定された明細行 (唯一の明細行である必要があります) を選択し、その **シーケンス番号** の値を *2* に変更します。</span><span class="sxs-lookup"><span data-stu-id="b75ac-139">On the **Location Directive Actions** FastTab, select the line that has a **Name** value of *Pick for less than pallet* (it should be the only line), and change its **Sequence number** value to *2*.</span></span>
1. <span data-ttu-id="b75ac-140">新しい場所ディレクティブ アクションの行を追加するには、グリッドの上で **新規** を選択します。</span><span class="sxs-lookup"><span data-stu-id="b75ac-140">Select **New** above the grid to add a line for a new location directive action.</span></span>
1. <span data-ttu-id="b75ac-141">新しい明細行で、次の値を設定します。</span><span class="sxs-lookup"><span data-stu-id="b75ac-141">On the new line, set the following values:</span></span>

    - <span data-ttu-id="b75ac-142">**シーケンス番号 :** *1*</span><span class="sxs-lookup"><span data-stu-id="b75ac-142">**Sequence number:** *1*</span></span>
    - <span data-ttu-id="b75ac-143">**名前 :** *ピッキング位置 1*</span><span class="sxs-lookup"><span data-stu-id="b75ac-143">**Name:** *Pick position 1*</span></span>

1. <span data-ttu-id="b75ac-144">新しい明細行が選択されたままの状態で、グリッドの上にある **クエリの編集** を選択します。</span><span class="sxs-lookup"><span data-stu-id="b75ac-144">While the new line is still selected, select **Edit query** above the grid.</span></span>
1. <span data-ttu-id="b75ac-145">クエリ エディターで、**結合** タブを選択します。</span><span class="sxs-lookup"><span data-stu-id="b75ac-145">In the query editor, select the **Joins** tab.</span></span>
1. <span data-ttu-id="b75ac-146">**場所** テーブル結合を展開して、**在庫分析コード** テーブルへの結合を表示します。</span><span class="sxs-lookup"><span data-stu-id="b75ac-146">Expand the **Locations** table join to show the join to the **Inventory dimensions** table.</span></span>
1. <span data-ttu-id="b75ac-147">**在庫分析コード** テーブル結合を展開して、**手持在庫** テーブルへの結合を表示します。</span><span class="sxs-lookup"><span data-stu-id="b75ac-147">Expand the **Inventory dimensions** table join to show the join to the **On-hand inventory** table.</span></span>
1. <span data-ttu-id="b75ac-148">**在庫分析コード** を選択して、**テーブル結合の追加** を選択します。</span><span class="sxs-lookup"><span data-stu-id="b75ac-148">Select **Inventory dimensions**, and then select **Add table join**.</span></span>
1. <span data-ttu-id="b75ac-149">表示されるテーブルの一覧で、**関係** 列の **ライセンス プレート (ライセンス プレート)** を選択します。</span><span class="sxs-lookup"><span data-stu-id="b75ac-149">In the list of tables that appears, in the **Relation** column, select **License plate (License plate)**.</span></span> <span data-ttu-id="b75ac-150">次に、**選択** を選択して、**ライセンス プレート** を **在庫分析コード** テーブル結合に追加します。</span><span class="sxs-lookup"><span data-stu-id="b75ac-150">Then select **Select** to add **License plate** to the **Inventory dimensions** table join.</span></span>
1. <span data-ttu-id="b75ac-151">**ライセンス プレート** を選択したままで、**テーブル結合の追加** を選択します。</span><span class="sxs-lookup"><span data-stu-id="b75ac-151">While **License plate** is still selected, select **Add table join**.</span></span>
1. <span data-ttu-id="b75ac-152">表示されるテーブルの一覧で、**関係** 列の **場所ライセンス プレートの配置 (ライセンス プレート)** を選択します。</span><span class="sxs-lookup"><span data-stu-id="b75ac-152">In the list of tables that appears, in the **Relation** column, select **Location license plate positioning (License plate)**.</span></span> <span data-ttu-id="b75ac-153">次に、**選択** を選択して、**場所ライセンス プレートの配置** を **在庫分析コード** テーブル結合に追加します。</span><span class="sxs-lookup"><span data-stu-id="b75ac-153">Then select **Select** to add **Location license plate positioning** to the **Inventory dimensions** table join.</span></span>

    <span data-ttu-id="b75ac-154">![テーブル結合](media/LpTableJoin.png "テーブル結合")</span><span class="sxs-lookup"><span data-stu-id="b75ac-154">![Table joins](media/LpTableJoin.png "Table joins")</span></span>

1. <span data-ttu-id="b75ac-155">**OK** を選択して 、更新された結合テーブルを確認し、クエリ エディターを閉じます。</span><span class="sxs-lookup"><span data-stu-id="b75ac-155">Select **OK** to confirm the updated joined tables and close the query editor.</span></span>
1. <span data-ttu-id="b75ac-156">**場所ディレクティブ アクション** クイック タブで、**クエリの編集** を再度選択してクエリ エディターを開きます。</span><span class="sxs-lookup"><span data-stu-id="b75ac-156">On the **Location Directive Actions** FastTab, select **Edit query** again to reopen to the query editor.</span></span>
1. <span data-ttu-id="b75ac-157">**範囲** タブで、**追加** を選択してグリッドに新しい行を追加します。</span><span class="sxs-lookup"><span data-stu-id="b75ac-157">On the **Range** tab, select **Add** to add a line to the grid.</span></span>
1. <span data-ttu-id="b75ac-158">新しい明細行で、次の値を設定します。</span><span class="sxs-lookup"><span data-stu-id="b75ac-158">On the new line, set the following values:</span></span>

    - <span data-ttu-id="b75ac-159">**テーブル :** *場所ライセンス プレートの配置*</span><span class="sxs-lookup"><span data-stu-id="b75ac-159">**Table:** *Location license plate positioning*</span></span>
    - <span data-ttu-id="b75ac-160">**派生テーブル :** *場所ライセンス プレートの配置*</span><span class="sxs-lookup"><span data-stu-id="b75ac-160">**Derived table:** *Location license plate positioning*</span></span>
    - <span data-ttu-id="b75ac-161">**フィールド :** *LP の位置*</span><span class="sxs-lookup"><span data-stu-id="b75ac-161">**Field:** *LP Position*</span></span>
    - <span data-ttu-id="b75ac-162">**基準 :** *1*</span><span class="sxs-lookup"><span data-stu-id="b75ac-162">**Criteria:** *1*</span></span>

    <span data-ttu-id="b75ac-163">![新しい範囲](media/LpPositionCriteria.png "新しい範囲")</span><span class="sxs-lookup"><span data-stu-id="b75ac-163">![New range](media/LpPositionCriteria.png "New range")</span></span>

1. <span data-ttu-id="b75ac-164">**OK** を選択して変更を確認し、クエリ エディターを閉じます。</span><span class="sxs-lookup"><span data-stu-id="b75ac-164">Select **OK** to confirm your changes and close the query editor.</span></span>

### <a name="set-up-sample-data-for-this-scenario"></a><span data-ttu-id="b75ac-165">このシナリオにサンプル データを設定する</span><span class="sxs-lookup"><span data-stu-id="b75ac-165">Set up sample data for this scenario</span></span>

<span data-ttu-id="b75ac-166">このシナリオでは、ユーザーは倉庫 *61* 用に設定された作業者を使用して、倉庫管理モバイル アプリにサインインして作業を行う必要があります。</span><span class="sxs-lookup"><span data-stu-id="b75ac-166">For this scenario, the user must sign in to the warehousing mobile app by using a worker who is set up for warehouse *61* to perform work.</span></span> <span data-ttu-id="b75ac-167">また、ユーザーはトランザクションを完了する必要があります。</span><span class="sxs-lookup"><span data-stu-id="b75ac-167">The user must also complete transactions.</span></span>

<span data-ttu-id="b75ac-168">*場所ライセンス プレートの配置* 機能は、場所ライセンス プレートの位置に新しい識別子を追加するため、最初にこのシナリオをサポートするデータを作成する必要があります。</span><span class="sxs-lookup"><span data-stu-id="b75ac-168">Because the *Location license plate positioning* feature adds a new identifier for license plate positions in a location, you must first create some data to support the scenario.</span></span>

#### <a name="spot-count-the-first-location"></a><span data-ttu-id="b75ac-169">最初の場所のスポット棚卸</span><span class="sxs-lookup"><span data-stu-id="b75ac-169">Spot-count the first location</span></span>

1. <span data-ttu-id="b75ac-170">倉庫管理アプリを開いて、倉庫 *61* にサインインします。</span><span class="sxs-lookup"><span data-stu-id="b75ac-170">Open the warehousing mobile app, and sign in to warehouse *61*.</span></span>
1. <span data-ttu-id="b75ac-171">**在庫 \> スポット棚卸** に移動します。</span><span class="sxs-lookup"><span data-stu-id="b75ac-171">Go to **Inventory \> Spot Counting**.</span></span>
1. <span data-ttu-id="b75ac-172">**スポット棚卸** ページで、**場所** フィールドを *01A01R1S1B* に設定します。</span><span class="sxs-lookup"><span data-stu-id="b75ac-172">On the **Spot Counting** page, set the **Location** field to *01A01R1S1B*.</span></span>
1. <span data-ttu-id="b75ac-173">**OK** を選択します。</span><span class="sxs-lookup"><span data-stu-id="b75ac-173">Select **OK**.</span></span>

    <span data-ttu-id="b75ac-174">ページには、入力した場所が表示されます。</span><span class="sxs-lookup"><span data-stu-id="b75ac-174">The page shows the location that you entered.</span></span> <span data-ttu-id="b75ac-175">また、「場所が完了しました。新しい LP または品目を追加しますか?」というメッセージが表示されます。</span><span class="sxs-lookup"><span data-stu-id="b75ac-175">It also shows the following message: "Location complete, add new LP or Item?"</span></span>

1. <span data-ttu-id="b75ac-176">**最新の情報に更新** を選択して、場所に棚卸を追加します。</span><span class="sxs-lookup"><span data-stu-id="b75ac-176">Select **Refresh** to add a count in the location.</span></span>
1. <span data-ttu-id="b75ac-177">**循環棚卸 : 新しい LP または品目の追加** ページで、**品目** フィールドを選択し、値 *A0001* を入力します。</span><span class="sxs-lookup"><span data-stu-id="b75ac-177">On the **Cycle Count: Add New LP or Item** page, select the **Item** field, and then enter the value *A0001*.</span></span>
1. <span data-ttu-id="b75ac-178">**OK** を選択します。</span><span class="sxs-lookup"><span data-stu-id="b75ac-178">Select **OK**.</span></span>
1. <span data-ttu-id="b75ac-179">**循環棚卸 : 新しい LP または品目の追加** ページで、**LP** フィールドを選択し、値 *LP1001* (またはその他の任意のライセンス プレート番号) を入力します。</span><span class="sxs-lookup"><span data-stu-id="b75ac-179">On the **Cycle Count: Add New LP or Item** page, select the **LP** field, and then enter the value *LP1001* (or any other license plate number of your choice).</span></span>

    <span data-ttu-id="b75ac-180">**循環棚卸 : 新しい LP または品目の追加** ページに **ライセンス プレートの位置 1** が表示されます。</span><span class="sxs-lookup"><span data-stu-id="b75ac-180">The **Cycle Count: Add New LP or Item** page shows **License Plate Position 1**.</span></span>

1. <span data-ttu-id="b75ac-181">**OK** を選択します。</span><span class="sxs-lookup"><span data-stu-id="b75ac-181">Select **OK**.</span></span>

    <span data-ttu-id="b75ac-182">ここで、ライセンス プレートで棚卸する品目の数量を指定する必要があります。</span><span class="sxs-lookup"><span data-stu-id="b75ac-182">You must now specify the quantity of the item that is counted on the license plate.</span></span>

1. <span data-ttu-id="b75ac-183">**数量** フィールドを *10* に設定します。</span><span class="sxs-lookup"><span data-stu-id="b75ac-183">Set the **Qty** field to *10*.</span></span>
1. <span data-ttu-id="b75ac-184">**OK** を選択します。</span><span class="sxs-lookup"><span data-stu-id="b75ac-184">Select **OK**.</span></span>

    <span data-ttu-id="b75ac-185">ページには、入力した場所が表示されます。</span><span class="sxs-lookup"><span data-stu-id="b75ac-185">The page shows the location that you entered.</span></span> <span data-ttu-id="b75ac-186">また、「場所が完了しました。新しい LP または品目を追加しますか?」というメッセージが表示されます。</span><span class="sxs-lookup"><span data-stu-id="b75ac-186">It also shows the following message: "Location complete, add new LP or Item?"</span></span>

1. <span data-ttu-id="b75ac-187">**最新の情報に更新** を選択して、場所に別の棚卸を追加します。</span><span class="sxs-lookup"><span data-stu-id="b75ac-187">Select **Refresh** to add another count in the location.</span></span>
1. <span data-ttu-id="b75ac-188">**循環棚卸 : 新しい LP または品目の追加** ページで、**品目** フィールドを選択し、値 *A0002* を入力します。</span><span class="sxs-lookup"><span data-stu-id="b75ac-188">On the **Cycle Count: Add New LP or Item** page, select the **Item** field, and then enter the value *A0002*.</span></span>
1. <span data-ttu-id="b75ac-189">**OK** を選択します。</span><span class="sxs-lookup"><span data-stu-id="b75ac-189">Select **OK**.</span></span>
1. <span data-ttu-id="b75ac-190">**循環棚卸 : 新しい LP または品目の追加** ページで、**LP** フィールドを選択し、値 *LP1002* (先に指定したライセンス プレート番号と異なる場合は、選択したその他のライセンス プレート番号) を入力します。</span><span class="sxs-lookup"><span data-stu-id="b75ac-190">On the **Cycle Count: Add New LP or Item** page, select the **LP** field, and then enter the value *LP1002* (or any other license plate number of your choice, provided that it differs from the license plate number that you specified earlier).</span></span>
1. <span data-ttu-id="b75ac-191">**LP の位置** フィールドを *2* に設定して、ライセンス プレートの位置を変更します。</span><span class="sxs-lookup"><span data-stu-id="b75ac-191">Change the license plate position by setting the **LP Position** field to *2*.</span></span>
1. <span data-ttu-id="b75ac-192">**OK** を選択します。</span><span class="sxs-lookup"><span data-stu-id="b75ac-192">Select **OK**.</span></span>
1. <span data-ttu-id="b75ac-193">**数量** フィールドを *10* に設定することにより、ライセンス プレートで棚卸する品目の数量を指定します。</span><span class="sxs-lookup"><span data-stu-id="b75ac-193">Specify the quantity of the item that is counted on the license plate by setting the **Qty** field to *10*.</span></span>
1. <span data-ttu-id="b75ac-194">**OK** を選択します。</span><span class="sxs-lookup"><span data-stu-id="b75ac-194">Select **OK**.</span></span>

    <span data-ttu-id="b75ac-195">ページには、入力した場所が表示されます。</span><span class="sxs-lookup"><span data-stu-id="b75ac-195">The page shows the location that you entered.</span></span> <span data-ttu-id="b75ac-196">また、「場所が完了しました。新しい LP または品目を追加しますか?」というメッセージが表示されます。</span><span class="sxs-lookup"><span data-stu-id="b75ac-196">It also shows the following message: "Location complete, add new LP or Item?"</span></span>

1. <span data-ttu-id="b75ac-197">**OK** を選択します。</span><span class="sxs-lookup"><span data-stu-id="b75ac-197">Select **OK**.</span></span>

<span data-ttu-id="b75ac-198">作業が完了しました。</span><span class="sxs-lookup"><span data-stu-id="b75ac-198">Work is now completed.</span></span>

#### <a name="spot-count-the-second-location"></a><span data-ttu-id="b75ac-199">2 つ目の場所のスポット棚卸</span><span class="sxs-lookup"><span data-stu-id="b75ac-199">Spot-count the second location</span></span>

1. <span data-ttu-id="b75ac-200">**スポット棚卸** ページで、**場所** フィールドを *01A01R1S2B* に設定します。</span><span class="sxs-lookup"><span data-stu-id="b75ac-200">On the **Spot Counting** page, set the **Location** field to *01A01R1S2B*.</span></span>
1. <span data-ttu-id="b75ac-201">**OK** を選択します。</span><span class="sxs-lookup"><span data-stu-id="b75ac-201">Select **OK**.</span></span>

    <span data-ttu-id="b75ac-202">ページには、入力した場所が表示されます。</span><span class="sxs-lookup"><span data-stu-id="b75ac-202">The page shows the location that you entered.</span></span> <span data-ttu-id="b75ac-203">また、「場所が完了しました。新しい LP または品目を追加しますか?」というメッセージが表示されます。</span><span class="sxs-lookup"><span data-stu-id="b75ac-203">It also shows the following message: "Location complete, add new LP or Item?"</span></span>

1. <span data-ttu-id="b75ac-204">**最新の情報に更新** を選択して、場所に棚卸を追加します。</span><span class="sxs-lookup"><span data-stu-id="b75ac-204">Select **Refresh** to add a count in the location.</span></span>
1. <span data-ttu-id="b75ac-205">**循環棚卸 : 新しい LP または品目の追加** ページで、**品目** フィールドを選択し、値 *A0002* を入力します。</span><span class="sxs-lookup"><span data-stu-id="b75ac-205">On the **Cycle Count: Add New LP or Item** page, select the **Item** field, and then enter the value *A0002*.</span></span>
1. <span data-ttu-id="b75ac-206">**OK** を選択します。</span><span class="sxs-lookup"><span data-stu-id="b75ac-206">Select **OK**.</span></span>
1. <span data-ttu-id="b75ac-207">**循環棚卸 : 新しい LP または品目の追加** ページで、**LP** フィールドを選択し、値 *LP1003* (前の手順で指定した両方のライセンス プレート番号と異なる場合は、選択したその他のライセンス プレート番号) を入力します。</span><span class="sxs-lookup"><span data-stu-id="b75ac-207">On the **Cycle Count: Add New LP or Item** page, select the **LP** field, and then enter the value *LP1003* (or any other license plate number of your choice, provided that it differs from the both the license plate numbers that you specified in the previous procedure).</span></span>

    <span data-ttu-id="b75ac-208">**循環棚卸 : 新しい LP または品目の追加** ページに **ライセンス プレートの位置 1** が表示されます。</span><span class="sxs-lookup"><span data-stu-id="b75ac-208">The **Cycle Count: Add New LP or Item** page shows **License Plate Position 1**.</span></span>

1. <span data-ttu-id="b75ac-209">**OK** を選択します。</span><span class="sxs-lookup"><span data-stu-id="b75ac-209">Select **OK**.</span></span>
1. <span data-ttu-id="b75ac-210">**数量** フィールドを *10* に設定することにより、ライセンス プレートで棚卸する品目の数量を指定します。</span><span class="sxs-lookup"><span data-stu-id="b75ac-210">Specify the quantity of the item that is counted on the license plate by setting the **Qty** field to *10*.</span></span>
1. <span data-ttu-id="b75ac-211">**OK** を選択します。</span><span class="sxs-lookup"><span data-stu-id="b75ac-211">Select **OK**.</span></span>

    <span data-ttu-id="b75ac-212">ページには、入力した場所が表示されます。</span><span class="sxs-lookup"><span data-stu-id="b75ac-212">The page shows the location that you entered.</span></span> <span data-ttu-id="b75ac-213">また、「場所が完了しました。新しい LP または品目を追加しますか?」というメッセージが表示されます。</span><span class="sxs-lookup"><span data-stu-id="b75ac-213">It also shows the following message: "Location complete, add new LP or Item?"</span></span>

1. <span data-ttu-id="b75ac-214">**OK** を選択します。</span><span class="sxs-lookup"><span data-stu-id="b75ac-214">Select **OK**.</span></span>

<span data-ttu-id="b75ac-215">作業が完了しました。</span><span class="sxs-lookup"><span data-stu-id="b75ac-215">Work is now completed.</span></span>

#### <a name="work-details"></a><span data-ttu-id="b75ac-216">作業の詳細</span><span class="sxs-lookup"><span data-stu-id="b75ac-216">Work details</span></span>

> [!NOTE]
> <span data-ttu-id="b75ac-217">モバイル アプリからのスポット棚卸は、Microsoft Dynamics 365 に循環棚卸作業を作成します。</span><span class="sxs-lookup"><span data-stu-id="b75ac-217">Spot counts from the mobile app create cycle counting work in Microsoft Dynamics 365.</span></span> <span data-ttu-id="b75ac-218">この作業では、在庫に転記する前に棚卸を承認する必要があります。</span><span class="sxs-lookup"><span data-stu-id="b75ac-218">The work requires that the counts be accepted before they are posted to inventory.</span></span>

1. <span data-ttu-id="b75ac-219">Dynamics 365 Supply Chain Management へサインインします。</span><span class="sxs-lookup"><span data-stu-id="b75ac-219">Sign in to Dynamics 365 Supply Chain Management.</span></span>
1. <span data-ttu-id="b75ac-220">**倉庫管理 \> 作業 \> 作業の詳細** の順に移動します。</span><span class="sxs-lookup"><span data-stu-id="b75ac-220">Go to **Warehouse management \> Work \> Work details**.</span></span>
1. <span data-ttu-id="b75ac-221">**概要** タブで、次の値を含む行を探します。</span><span class="sxs-lookup"><span data-stu-id="b75ac-221">On the **Overview** tab, look for the lines that have the following values:</span></span>

    - <span data-ttu-id="b75ac-222">**作業指示書のタイプ :** *循環棚卸*</span><span class="sxs-lookup"><span data-stu-id="b75ac-222">**Work order type:** *Cycle counting*</span></span>
    - <span data-ttu-id="b75ac-223">**倉庫:** *61*</span><span class="sxs-lookup"><span data-stu-id="b75ac-223">**Warehouse:** *61*</span></span>
    - <span data-ttu-id="b75ac-224">**作業状態 :** *検討保留*</span><span class="sxs-lookup"><span data-stu-id="b75ac-224">**Work status:** *Pending review*</span></span>

    <span data-ttu-id="b75ac-225">これらの明細行に対して 2 つの作業 ID が作成されている必要があります。</span><span class="sxs-lookup"><span data-stu-id="b75ac-225">Two work IDs should have been created for these lines.</span></span> <span data-ttu-id="b75ac-226">これらの両方の作業 ID の棚卸を承認する必要があります。</span><span class="sxs-lookup"><span data-stu-id="b75ac-226">The counts for both these work IDs must be accepted.</span></span>

1. <span data-ttu-id="b75ac-227">グリッドで、*循環棚卸* 作業指示書タイプの最初の作業 ID を選択します。</span><span class="sxs-lookup"><span data-stu-id="b75ac-227">In the grid, select the first work ID for the *Cycle counting* work order type.</span></span>
1. <span data-ttu-id="b75ac-228">アクション ウィンドウの **作業** タブの、**作業** グループで、**循環棚卸** を選択します。</span><span class="sxs-lookup"><span data-stu-id="b75ac-228">On the Action Pane, on **Work** tab, in the **Work** group, select **Cycle counting**.</span></span>

    <span data-ttu-id="b75ac-229">品目ごと、およびライセンス プレートごとに 1 つずつ、合計 2 つの明細行が表示されます。</span><span class="sxs-lookup"><span data-stu-id="b75ac-229">Two lines are shown, one for each item and license plate.</span></span> <span data-ttu-id="b75ac-230">**棚卸数**、**場所**、**ライセンス プレート**、**品目** フィールドの値は、モバイル デバイスで作成した棚卸エントリと一致する必要があります。</span><span class="sxs-lookup"><span data-stu-id="b75ac-230">The values in the **Counted quantity**, **Location**, **License plate**, and **Item** fields should match the count entries that you created on the mobile device.</span></span> <span data-ttu-id="b75ac-231">これらのフィールドが表示されていない場合は、 アクション ウィンドウで **分析コードの表示** を選択して、グリッドに追加します。</span><span class="sxs-lookup"><span data-stu-id="b75ac-231">If any of these fields aren't visible, select **Display dimensions** on the Action Pane to add them to the grid.</span></span>

1. <span data-ttu-id="b75ac-232">両方の明細行を選択します。</span><span class="sxs-lookup"><span data-stu-id="b75ac-232">Select both lines.</span></span>
1. <span data-ttu-id="b75ac-233">アクション ウィンドウで、**受け入れ数量** を選択します。</span><span class="sxs-lookup"><span data-stu-id="b75ac-233">On the Action Pane, select **Accept count**.</span></span>
1. <span data-ttu-id="b75ac-234">「転記 - 仕訳帳」というメッセージが表示されます。</span><span class="sxs-lookup"><span data-stu-id="b75ac-234">You receive a "Posting - Journal" message.</span></span> <span data-ttu-id="b75ac-235">転記済仕訳帳番号を表示するには、**メッセージの詳細** を選択します。</span><span class="sxs-lookup"><span data-stu-id="b75ac-235">Select **Message details** to view the posted journal number.</span></span>
1. <span data-ttu-id="b75ac-236">メッセージの詳細を閉じます。</span><span class="sxs-lookup"><span data-stu-id="b75ac-236">Close the message details.</span></span>
1. <span data-ttu-id="b75ac-237">**作業** ページを最新の情報に更新します。</span><span class="sxs-lookup"><span data-stu-id="b75ac-237">Refresh the **Work** page.</span></span>

    <span data-ttu-id="b75ac-238">最初の作業 ID は既にクローズされているため、表示されません。</span><span class="sxs-lookup"><span data-stu-id="b75ac-238">The first work ID has been closed and is no longer shown.</span></span>

    > [!TIP]
    > <span data-ttu-id="b75ac-239">クローズした作業を表示するには、グリッド上部の **クローズ済の表示** チェック ボックスをオンにします。</span><span class="sxs-lookup"><span data-stu-id="b75ac-239">To view closed work, select the **Show closed** check box above the grid.</span></span>

    <span data-ttu-id="b75ac-240">ここでは、*01A01R1S2B* の場所にあるライセンス プレートの作業を受け入れます。</span><span class="sxs-lookup"><span data-stu-id="b75ac-240">You will now accept the work for the license plate in the *01A01R1S2B* location.</span></span>

1. <span data-ttu-id="b75ac-241">**概要** タブで、*循環棚卸* 作業指示書タイプの 2 つ目の作業 ID を選択します。</span><span class="sxs-lookup"><span data-stu-id="b75ac-241">On the **Overview** tab, select the second work ID for the *Cycle counting* work order type.</span></span>
1. <span data-ttu-id="b75ac-242">アクション ウィンドウの **作業** タブの、**作業** グループで、**循環棚卸** を選択します。</span><span class="sxs-lookup"><span data-stu-id="b75ac-242">On the Action Pane, on **Work** tab, in the **Work** group, select **Cycle counting**.</span></span>

    <span data-ttu-id="b75ac-243">品目とライセンス プレートに、1 つの明細行が表示されます。</span><span class="sxs-lookup"><span data-stu-id="b75ac-243">One line is shown, for the item and license plate.</span></span> <span data-ttu-id="b75ac-244">**棚卸数**、**場所**、**ライセンス プレート**、**品目** フィールドの値は、モバイル デバイスで作成した棚卸エントリと一致する必要があります。</span><span class="sxs-lookup"><span data-stu-id="b75ac-244">The values in the **Counted quantity**, **Location**, **License plate**, and **Item** fields should match the count entries that you created on the mobile device.</span></span>

1. <span data-ttu-id="b75ac-245">明細行を選択します。</span><span class="sxs-lookup"><span data-stu-id="b75ac-245">Select the line.</span></span>
1. <span data-ttu-id="b75ac-246">アクション ウィンドウで、**受け入れ数量** を選択します。</span><span class="sxs-lookup"><span data-stu-id="b75ac-246">On the Action Pane, select **Accept count**.</span></span>
1. <span data-ttu-id="b75ac-247">「転記 - 仕訳帳」というメッセージが表示されます。</span><span class="sxs-lookup"><span data-stu-id="b75ac-247">You receive a "Posting - Journal" message.</span></span> <span data-ttu-id="b75ac-248">転記済仕訳帳番号を表示するには、**メッセージの詳細** を選択します。</span><span class="sxs-lookup"><span data-stu-id="b75ac-248">Select **Message details** to view the posted journal number.</span></span>
1. <span data-ttu-id="b75ac-249">メッセージの詳細を閉じます。</span><span class="sxs-lookup"><span data-stu-id="b75ac-249">Close the message details.</span></span>
1. <span data-ttu-id="b75ac-250">**作業** ページを最新の情報に更新します。</span><span class="sxs-lookup"><span data-stu-id="b75ac-250">Refresh the **Work** page.</span></span>

    <span data-ttu-id="b75ac-251">2 つ目の作業 ID は既にクローズされているため、表示されません。</span><span class="sxs-lookup"><span data-stu-id="b75ac-251">The second work ID has been closed and is no longer shown.</span></span>

    > [!TIP]
    > <span data-ttu-id="b75ac-252">クローズした作業を表示するには、グリッド上部の **クローズ済の表示** チェック ボックスをオンにします。</span><span class="sxs-lookup"><span data-stu-id="b75ac-252">To view closed work, select the **Show closed** check box above the grid.</span></span>

#### <a name="on-hand-by-location"></a><span data-ttu-id="b75ac-253">保管場所ごとの手持在庫</span><span class="sxs-lookup"><span data-stu-id="b75ac-253">On-hand by location</span></span>

1. <span data-ttu-id="b75ac-254">**倉庫管理 \> 照会およびレポート \> 保管場所ごとの手持在庫** の順に移動します。</span><span class="sxs-lookup"><span data-stu-id="b75ac-254">Go to **Warehouse management \> Inquiries and reports \> On-hand by location**.</span></span>
1. <span data-ttu-id="b75ac-255">次の値を設定します。</span><span class="sxs-lookup"><span data-stu-id="b75ac-255">Set the following values:</span></span>

    - <span data-ttu-id="b75ac-256">**サイト:** *6*</span><span class="sxs-lookup"><span data-stu-id="b75ac-256">**Site:** *6*</span></span>
    - <span data-ttu-id="b75ac-257">**倉庫:** *61*</span><span class="sxs-lookup"><span data-stu-id="b75ac-257">**Warehouse:** *61*</span></span>
    - <span data-ttu-id="b75ac-258">**場所を越えて最新の情報に更新する :** *はい*</span><span class="sxs-lookup"><span data-stu-id="b75ac-258">**Refresh across locations:** *Yes*</span></span>

1. <span data-ttu-id="b75ac-259">場所 *01A01R1S1B* には 2 つのライセンス プレートがあることに注意してください。</span><span class="sxs-lookup"><span data-stu-id="b75ac-259">Notice that location *01A01R1S1B* has two license plates:</span></span>

    - <span data-ttu-id="b75ac-260">**LP の位置** フィールドが *1* に設定されている **A0001**</span><span class="sxs-lookup"><span data-stu-id="b75ac-260">**A0001**, where the **LP Position** field is set to *1*</span></span>
    - <span data-ttu-id="b75ac-261">**LP の位置** フィールドが *2* に設定されている **A0002**</span><span class="sxs-lookup"><span data-stu-id="b75ac-261">**A0002**, where the **LP Position** field is set to *2*</span></span>

1. <span data-ttu-id="b75ac-262">場所 *01A01R1S2B* には 1 つのライセンス プレートがあることに注意してください。</span><span class="sxs-lookup"><span data-stu-id="b75ac-262">Notice that location *01A01R1S2B* has one license plate:</span></span>

    - <span data-ttu-id="b75ac-263">**LP の位置** フィールドが *1* に設定されている **A0002**</span><span class="sxs-lookup"><span data-stu-id="b75ac-263">**A0002**, where the **LP Position** field is set to *1*</span></span>

### <a name="sales-order-scenario"></a><span data-ttu-id="b75ac-264">販売注文のシナリオ</span><span class="sxs-lookup"><span data-stu-id="b75ac-264">Sales order scenario</span></span>

<span data-ttu-id="b75ac-265">これで、*場所ライセンス プレートの配置* 機能が設定され、在庫のステージングが完了したので、販売注文を作成してピッキング作業を生成し、パレット ID が位置 *1* にある在庫場所から倉庫作業者に品目 *A0002* をピッキングさせる必要があります。</span><span class="sxs-lookup"><span data-stu-id="b75ac-265">Now that the *Location license plate positioning* feature has been set up, and the inventory has been staged, you must create a sales order to generate picking work that will direct the warehouse worker to pick item *A0002* from the inventory location where the pallet ID is in position *1*.</span></span>

1. <span data-ttu-id="b75ac-266">**販売とマーケティング \> 販売注文 \> すべての販売注文** の順に移動します。</span><span class="sxs-lookup"><span data-stu-id="b75ac-266">Go to **Sales and marketing \> Sales orders \> All sales orders**.</span></span>
1. <span data-ttu-id="b75ac-267">アクション ウィンドウで、**新規** を選択します。</span><span class="sxs-lookup"><span data-stu-id="b75ac-267">On the Action Pane, select **New**.</span></span>
1. <span data-ttu-id="b75ac-268">**販売注文の作成** ダイアログ ボックスでは、次の値を設定します。</span><span class="sxs-lookup"><span data-stu-id="b75ac-268">In the **Create sales order** dialog box, set the following values:</span></span>

    - <span data-ttu-id="b75ac-269">**顧客アカウント:** *US-004*</span><span class="sxs-lookup"><span data-stu-id="b75ac-269">**Customer account:** *US-004*</span></span>
    - <span data-ttu-id="b75ac-270">**倉庫:** *61*</span><span class="sxs-lookup"><span data-stu-id="b75ac-270">**Warehouse:** *61*</span></span>

1. <span data-ttu-id="b75ac-271">**OK** を選択します。</span><span class="sxs-lookup"><span data-stu-id="b75ac-271">Select **OK**.</span></span>
1. <span data-ttu-id="b75ac-272">新しい明細行が、**販売注文明細行** クイック タブのグリッドに追加されます。</span><span class="sxs-lookup"><span data-stu-id="b75ac-272">A new line is added to the grid on the **Sales order lines** FastTab.</span></span> <span data-ttu-id="b75ac-273">この新しい明細行で、次の値を設定します。</span><span class="sxs-lookup"><span data-stu-id="b75ac-273">On this new line, set the following values:</span></span>

    - <span data-ttu-id="b75ac-274">**品目番号:** *A0002*</span><span class="sxs-lookup"><span data-stu-id="b75ac-274">**Item number:** *A0002*</span></span>
    - <span data-ttu-id="b75ac-275">**数量:** *1*</span><span class="sxs-lookup"><span data-stu-id="b75ac-275">**Quantity:** *1*</span></span>

1. <span data-ttu-id="b75ac-276">グリッドの上部にある **在庫** メニューで、**引当** を選択します。</span><span class="sxs-lookup"><span data-stu-id="b75ac-276">On the **Inventory** menu above the grid, select **Reservation**.</span></span>
1. <span data-ttu-id="b75ac-277">**引当** ページの、アクション ウィンドウで **ロットの引当** を選択して、注文明細行に在庫を引当します。</span><span class="sxs-lookup"><span data-stu-id="b75ac-277">On the **Reservation** page, on the Action Pane, select **Reserve lot** to reserve inventory for the order line.</span></span>
1. <span data-ttu-id="b75ac-278">**引当** ページを閉じます。</span><span class="sxs-lookup"><span data-stu-id="b75ac-278">Close the **Reservation** page.</span></span>
1. <span data-ttu-id="b75ac-279">アクション ペインの、**倉庫** タブにある **アクション** グループで、**倉庫にリリース** を選択します。</span><span class="sxs-lookup"><span data-stu-id="b75ac-279">On the Action Pane, on the **Warehouse** tab, in the **Actions** group, select **Release to warehouse**.</span></span>

    <span data-ttu-id="b75ac-280">この注文に対して作成されたウェーブ ID および出荷 ID を示す情報メッセージが表示されます。</span><span class="sxs-lookup"><span data-stu-id="b75ac-280">You receive an informational message that indicates the wave ID and shipment ID that were created for the order.</span></span>

1. <span data-ttu-id="b75ac-281">グリッドの上部の **販売注文明細行** クイック タブにある **倉庫** メニューで、**作業の詳細** を選択します。</span><span class="sxs-lookup"><span data-stu-id="b75ac-281">On the **Sales order lines** FastTab, on the **Warehouse** menu above the grid, select **Work details**.</span></span>
1. <span data-ttu-id="b75ac-282">**作業** ページが表示され、販売明細行に対して作成された作業が表示されます。</span><span class="sxs-lookup"><span data-stu-id="b75ac-282">The **Work** page appears and shows the work that was created for the sales line.</span></span> <span data-ttu-id="b75ac-283">表示されている作業 ID をメモします。</span><span class="sxs-lookup"><span data-stu-id="b75ac-283">Make a note of the work ID that is shown.</span></span>

### <a name="sales-picking-scenario"></a><span data-ttu-id="b75ac-284">販売ピッキングのシナリオ</span><span class="sxs-lookup"><span data-stu-id="b75ac-284">Sales picking scenario</span></span>

1. <span data-ttu-id="b75ac-285">モバイル アプリを開いて、倉庫 *61* にサインインします。</span><span class="sxs-lookup"><span data-stu-id="b75ac-285">Open the mobile app, and sign in to warehouse *61*.</span></span>
1. <span data-ttu-id="b75ac-286">**出荷 \> 販売ピッキング** に移動します。</span><span class="sxs-lookup"><span data-stu-id="b75ac-286">Go to **Outbound \> Sales picking**.</span></span>
1. <span data-ttu-id="b75ac-287">**作業 ID のスキャン / ライセンス プレート ID** ページで、**ID** フィールドを選択して、販売明細行から作業 ID を入力します。</span><span class="sxs-lookup"><span data-stu-id="b75ac-287">On the **Scan a work ID / license plate ID** page, select the **ID** field, and then enter the work ID from the sales line.</span></span>
1. <span data-ttu-id="b75ac-288">このピッキング作業では、品目 *A0002* を場所 *01A01R1S2B* からピッキングするように指示されます。</span><span class="sxs-lookup"><span data-stu-id="b75ac-288">Notice that the picking work directs you to pick item *A0002* from location *01A01R1S2B*.</span></span> <span data-ttu-id="b75ac-289">この指示は、品目 *A0002* が その場所の位置 *1* のライセンス プレート上にあるために表示されます。</span><span class="sxs-lookup"><span data-stu-id="b75ac-289">You receive this instruction because item *A0002* is on a license plate that is in position *1* in that location.</span></span>

    <span data-ttu-id="b75ac-290">![位置 1 の場所](media/LocationLicensePlatePositioning.png "位置 1 の場所")</span><span class="sxs-lookup"><span data-stu-id="b75ac-290">![Position 1 location](media/LocationLicensePlatePositioning.png "Position 1 location")</span></span>

1. <span data-ttu-id="b75ac-291">場所に対して作成したライセンス プレートの ID を入力し、プロンプトに従って販売注文を選択します。</span><span class="sxs-lookup"><span data-stu-id="b75ac-291">Enter the license plate ID that you created for the location, and then follow the prompts to pick the sales order.</span></span>


[!INCLUDE[footer-include](../../includes/footer-banner.md)]