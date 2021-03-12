---
title: ピッキング行のグループ化
description: このトピックでは、ピッキング行のグループ化の概要を示します。
author: Mirzaab
manager: tfehr
ms.date: 12/15/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: WHSRFMenuItem,WHSWorkTemplateTable
audience: Application User
ms.reviewer: kamaybac
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: perlynne
ms.search.validFrom: 2019-12-31
ms.dyn365.ops.version: 10.0.1
ms.openlocfilehash: e70244d46ec2787fefdb097d0354af7910b55e9c
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 01/15/2021
ms.locfileid: "4989721"
---
# <a name="pick-line-grouping"></a><span data-ttu-id="87adf-103">ピッキング行のグループ化</span><span class="sxs-lookup"><span data-stu-id="87adf-103">Pick line grouping</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="87adf-104">ピッキング行のグループでは、品目と場所が同じ複数の作業明細行を結合して、モバイル デバイスでユーザーに提示される 1 つのピッキングを作成できます。</span><span class="sxs-lookup"><span data-stu-id="87adf-104">Pick line grouping enables multiple work lines that have the same item and location to be combined into a single pick that is presented to the user on the mobile device.</span></span> <span data-ttu-id="87adf-105">したがって、倉庫の作業者は、可能な限り効率的な指示を受け取ることができますが、システムに必要な作業明細行の分割 (たとえば、異なるコンテナや注文など) も維持されます。</span><span class="sxs-lookup"><span data-stu-id="87adf-105">Therefore, warehouse workers can receive the most efficient instructions, but required work line separation (for different containers, orders, and so on) can still be maintained in the system.</span></span>

## <a name="turn-on-the-pick-line-grouping-feature"></a><span data-ttu-id="87adf-106">ピッキング行のグループ機能をオンにする</span><span class="sxs-lookup"><span data-stu-id="87adf-106">Turn on the pick line grouping feature</span></span>

<span data-ttu-id="87adf-107">この機能を使用するには、システム上で有効にする必要があります。</span><span class="sxs-lookup"><span data-stu-id="87adf-107">Before you can use this feature, it must be turned on in your system.</span></span> <span data-ttu-id="87adf-108">管理者は、[機能の管理](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) ワークスペースを使用して、この機能の状態を確認し、必要に応じて有効にすることができます。</span><span class="sxs-lookup"><span data-stu-id="87adf-108">Administrators can use the [Feature management](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) workspace to check the status of the feature and turn it on if it's required.</span></span> <span data-ttu-id="87adf-109">この機能は、次のようにして表示されます。</span><span class="sxs-lookup"><span data-stu-id="87adf-109">There, the feature is listed in the following way:</span></span>

- <span data-ttu-id="87adf-110">**モジュール:** *倉庫管理*</span><span class="sxs-lookup"><span data-stu-id="87adf-110">**Module:** *Warehouse management*</span></span>
- <span data-ttu-id="87adf-111">**機能名:** *ピッキング行のグループ*</span><span class="sxs-lookup"><span data-stu-id="87adf-111">**Feature name:** *Pick line grouping*</span></span>

## <a name="set-up-pick-line-grouping"></a><span data-ttu-id="87adf-112">ピッキング行のグループ化の設定</span><span class="sxs-lookup"><span data-stu-id="87adf-112">Set up pick line grouping</span></span>

### <a name="create-a-mobile-device-menu-item"></a><span data-ttu-id="87adf-113">品目のモバイル デバイス メニューの作成</span><span class="sxs-lookup"><span data-stu-id="87adf-113">Create a mobile device menu item</span></span>

1. <span data-ttu-id="87adf-114">**倉庫管理 \> 設定 \> モバイル デバイス \> モバイル デバイスのメニュー品目** の順に移動します。</span><span class="sxs-lookup"><span data-stu-id="87adf-114">Go to **Warehouse management \> Setup \> Mobile device \> Mobile device menu items**.</span></span>
1. <span data-ttu-id="87adf-115">アクション ウィンドウで、**新規** を選択します。</span><span class="sxs-lookup"><span data-stu-id="87adf-115">On the Action Pane, select **New**.</span></span>
1. <span data-ttu-id="87adf-116">**メニュー項目名** フィールドに、*販売グループ行のピッキング* と入力します。</span><span class="sxs-lookup"><span data-stu-id="87adf-116">In the **Menu item name** field, enter *Sales group line picking*.</span></span>
1. <span data-ttu-id="87adf-117">**タイトル** フィールドに、*販売グループ行ピッキング* と入力します。</span><span class="sxs-lookup"><span data-stu-id="87adf-117">In the **Title** field, enter *Sales group line picking*.</span></span> <span data-ttu-id="87adf-118">このタイトルはモバイル デバイス メニューに表示されます。</span><span class="sxs-lookup"><span data-stu-id="87adf-118">This title will be shown on the mobile device menu.</span></span>
1. <span data-ttu-id="87adf-119">**モード** フィールドで、*作業* を選択します。</span><span class="sxs-lookup"><span data-stu-id="87adf-119">In the **Mode** field, select *Work*.</span></span>
1. <span data-ttu-id="87adf-120">**既存の作業を使用** オプションを *はい* に設定します。</span><span class="sxs-lookup"><span data-stu-id="87adf-120">Set the **Use existing work** option to *Yes*.</span></span>
1. <span data-ttu-id="87adf-121">**一般** クイック タブで、次の値を設定します。</span><span class="sxs-lookup"><span data-stu-id="87adf-121">On the **General** FastTab, set the following values:</span></span>

    - <span data-ttu-id="87adf-122">**指示者** フィールドで、*ユーザー主導* を選択します。</span><span class="sxs-lookup"><span data-stu-id="87adf-122">In the **Directed by** field, select *User directed*.</span></span>
    - <span data-ttu-id="87adf-123">**ライセンス プレートの生成** オプションを *はい* に設定します。</span><span class="sxs-lookup"><span data-stu-id="87adf-123">Set the **Generate license plate** option to *Yes*.</span></span>
    - <span data-ttu-id="87adf-124">**グループ ピック** オプションを *はい* に設定します。</span><span class="sxs-lookup"><span data-stu-id="87adf-124">Set the **Group pick** option to *Yes*.</span></span>
    - <span data-ttu-id="87adf-125">残りのオプションに対しては規定値を受け入れます。</span><span class="sxs-lookup"><span data-stu-id="87adf-125">Accept the default values for the remaining options.</span></span>

1. <span data-ttu-id="87adf-126">次の手順に従って、モバイル デバイスのメニュー項目に対して有効な作業クラスを構成します。</span><span class="sxs-lookup"><span data-stu-id="87adf-126">Follow these steps to configure the valid work classes for the mobile device menu item:</span></span>

    1. <span data-ttu-id="87adf-127">**作業クラス** クイック タブで、**新規** を選択します。</span><span class="sxs-lookup"><span data-stu-id="87adf-127">On the **Work classes** FastTab, elect **New**.</span></span>
    2. <span data-ttu-id="87adf-128">**作業クラス ID** フィールドで、使用する倉庫に応じて *販売* または *SO ピッキング* のいずれかを選択できます。</span><span class="sxs-lookup"><span data-stu-id="87adf-128">In the **Work class ID** field, you can select either *Sales* or *SO Pick*, depending on the warehouse that you will use.</span></span> <span data-ttu-id="87adf-129">このシナリオでは *SO ピッキング* を選択します。</span><span class="sxs-lookup"><span data-stu-id="87adf-129">For this scenario, select *SO Pick*.</span></span>

        <span data-ttu-id="87adf-130">**作業指示書のタイプ** フィールドは自動的に *発注書* に設定されます。</span><span class="sxs-lookup"><span data-stu-id="87adf-130">The **Work order type** field is automatically set to *Sales orders*.</span></span>

### <a name="set-up-a-mobile-device-menu"></a><span data-ttu-id="87adf-131">モバイル デバイス メニューを設定する</span><span class="sxs-lookup"><span data-stu-id="87adf-131">Set up a mobile device menu</span></span>

<span data-ttu-id="87adf-132">次の手順に従って、作成したメニュー項目を **出荷** メニューに追加します。</span><span class="sxs-lookup"><span data-stu-id="87adf-132">Follow these steps to add the menu item that you just created to the **Outbound** menu.</span></span>

1. <span data-ttu-id="87adf-133">**倉庫管理 \> 設定 \> モバイル デバイス \> モバイル デバイス メニュー** の順に移動します。</span><span class="sxs-lookup"><span data-stu-id="87adf-133">Go to **Warehouse management \> Setup \> Mobile device \> Mobile device menu**.</span></span>
1. <span data-ttu-id="87adf-134">アクション ウィンドウで、**編集** を選択します。</span><span class="sxs-lookup"><span data-stu-id="87adf-134">On the Action Pane, select **Edit**.</span></span>
1. <span data-ttu-id="87adf-135">リスト ペインには、既存のすべてのモバイル デバイス メニューが表示されます。</span><span class="sxs-lookup"><span data-stu-id="87adf-135">The list pane shows all existing mobile device menus.</span></span> <span data-ttu-id="87adf-136">リストで、*出荷* を選択します。</span><span class="sxs-lookup"><span data-stu-id="87adf-136">Select *Outbound* in the list.</span></span>
1. <span data-ttu-id="87adf-137">**使用可能なメニューとメニュー項目** のリストで、作成した *販売グループ列のピッキング* メニュー項目を検索して選択します。</span><span class="sxs-lookup"><span data-stu-id="87adf-137">In the **Available menus and menu items** list, find and select the *Sales group line picking* menu item that you created.</span></span>
1. <span data-ttu-id="87adf-138">右矢印ボタンを選択して、*販売グループ列のピッキング* メニュー項目を **メニュー構造** の一覧に移動します。</span><span class="sxs-lookup"><span data-stu-id="87adf-138">Select the right arrow button to move the *Sales group line picking* menu item to the **Menu structure** list.</span></span>
1. <span data-ttu-id="87adf-139">上向き矢印ボタンと下向き矢印ボタンを使用して、メニュー構造をメニューの目的の位置に移動します。</span><span class="sxs-lookup"><span data-stu-id="87adf-139">Use the up arrow and down arrow buttons to move the menu item into the desired position in the menu structure.</span></span>
1. <span data-ttu-id="87adf-140">アクション ウィンドウで、**保存** を選択します。</span><span class="sxs-lookup"><span data-stu-id="87adf-140">On the Action Pane, select **Save**.</span></span>

### <a name="set-up-a-work-template"></a><span data-ttu-id="87adf-141">作業テンプレートを設定する</span><span class="sxs-lookup"><span data-stu-id="87adf-141">Set up a work template</span></span>

1. <span data-ttu-id="87adf-142">**倉庫管理 \> 設定 \> 作業 \> 作業テンプレート** の順に移動します。</span><span class="sxs-lookup"><span data-stu-id="87adf-142">Go to **Warehouse management \> Setup \> Work \> Work templates**.</span></span>
1. <span data-ttu-id="87adf-143">**ワーク オーダー タイプ** フィールドで、*販売注文* を選択します。</span><span class="sxs-lookup"><span data-stu-id="87adf-143">In the **Work order type** field, select *Sales orders*.</span></span>
1. <span data-ttu-id="87adf-144">**概要** グリッドで、この機能で使用する作業テンプレートを検索および選択します。</span><span class="sxs-lookup"><span data-stu-id="87adf-144">In the **Overview** grid, find and select the work template that should be used with this function.</span></span> <span data-ttu-id="87adf-145">このシナリオについては *51 ピッキングからステージ* を選択します。</span><span class="sxs-lookup"><span data-stu-id="87adf-145">For this scenario, select the *51 Pick to stage* template.</span></span>
1. <span data-ttu-id="87adf-146">アクション ウィンドウで、**クエリの編集** を選択します。</span><span class="sxs-lookup"><span data-stu-id="87adf-146">On the Action Pane, select **Edit query**.</span></span>
1. <span data-ttu-id="87adf-147">このクエリの編集ダイアログ ボックスの、**ソーティング** タブで、**追加** を選択して、新しい行を追加し、次の値を設定します。</span><span class="sxs-lookup"><span data-stu-id="87adf-147">In the query editor dialog box, on the **Sorting** tab, select **Add**, and then set the following values for the new row:</span></span>

    - <span data-ttu-id="87adf-148">**テーブル** 列で、*一時的な作業トランザクション* を選択します。</span><span class="sxs-lookup"><span data-stu-id="87adf-148">In the **Table** column, select *Temporary work transactions*.</span></span>
    - <span data-ttu-id="87adf-149">**派生テーブル** 列で、*一時的な作業トランザクション* を選択します。</span><span class="sxs-lookup"><span data-stu-id="87adf-149">In the **Derived table** column, select *Temporary work transactions*.</span></span>
    - <span data-ttu-id="87adf-150">**フィールド** 列で、*品目番号* を選択します。</span><span class="sxs-lookup"><span data-stu-id="87adf-150">In the **Field** column, select *Item number*.</span></span>
    - <span data-ttu-id="87adf-151">**検索の方向** 列で、*昇順* を選択します。</span><span class="sxs-lookup"><span data-stu-id="87adf-151">In the **Search direction** column, select *Ascending*.</span></span>

1. <span data-ttu-id="87adf-152">**OK** を選択してダイアログ ボックスを閉じて、選択項目を保存します。</span><span class="sxs-lookup"><span data-stu-id="87adf-152">Select **OK** to close the dialog box and save your selection.</span></span>
1. <span data-ttu-id="87adf-153">次のメッセージが表示されます: "グループはリセットされますが、続行しますか?"</span><span class="sxs-lookup"><span data-stu-id="87adf-153">You receive the following message: "Grouping will be reset, continue?"</span></span> <span data-ttu-id="87adf-154">**はい** を選択して続行します。</span><span class="sxs-lookup"><span data-stu-id="87adf-154">Select **Yes** to continue.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="87adf-155">ピッキング行のグループ化機能を機能させるには、作業明細行を品目 ID で並べ替える必要があります。</span><span class="sxs-lookup"><span data-stu-id="87adf-155">For the pick line grouping functionality to work, the work lines must be sorted by item ID.</span></span> <span data-ttu-id="87adf-156">同じ品目を含む行が順序付けされない場合は、グループ化されません。</span><span class="sxs-lookup"><span data-stu-id="87adf-156">If lines that have the same items aren't sequenced one after another, they won't be grouped.</span></span>

## <a name="example"></a><span data-ttu-id="87adf-157">例</span><span class="sxs-lookup"><span data-stu-id="87adf-157">Example</span></span>

### <a name="create-picking-work"></a><span data-ttu-id="87adf-158">ピッキング作業の作成</span><span class="sxs-lookup"><span data-stu-id="87adf-158">Create picking work</span></span>

<span data-ttu-id="87adf-159">ピッキング行のグループ化を設定する前に、適格な出荷作業をいくつか作成する必要があります。</span><span class="sxs-lookup"><span data-stu-id="87adf-159">Before you can set up pick line grouping, you must create some eligible outbound work.</span></span>

1. <span data-ttu-id="87adf-160">**販売とマーケティング \> 販売注文 \> すべての販売注文** の順に移動します。</span><span class="sxs-lookup"><span data-stu-id="87adf-160">Go to **Sales and marketing \> Sales orders \> All sales orders**.</span></span>
1. <span data-ttu-id="87adf-161">**新規** を選択して新しい販売注文を作成します。</span><span class="sxs-lookup"><span data-stu-id="87adf-161">Select **New** to create a sales order.</span></span>
1. <span data-ttu-id="87adf-162">**顧客口座** フィールドで、*US-004* を選択します。</span><span class="sxs-lookup"><span data-stu-id="87adf-162">In the **Customer account** field, select *US-004*.</span></span>
1. <span data-ttu-id="87adf-163">**一般** クイック タブの **倉庫** フィールドで、 *51* を選択します。</span><span class="sxs-lookup"><span data-stu-id="87adf-163">On the **General** FastTab, in the **Warehouse** field, select *51*.</span></span>
1. <span data-ttu-id="87adf-164">**OK** を選択します。</span><span class="sxs-lookup"><span data-stu-id="87adf-164">Select **OK**.</span></span>
1. <span data-ttu-id="87adf-165">**販売注文明細行** クイックタブで、次の 6 行を追加します。</span><span class="sxs-lookup"><span data-stu-id="87adf-165">On the **Sales order lines** FastTab, add the following six lines:</span></span>

    - <span data-ttu-id="87adf-166">**明細行 1:** **品目番号** フィールドで、*M9200* を選択します。</span><span class="sxs-lookup"><span data-stu-id="87adf-166">**Line 1:** In the **Item number** field, select *M9200*.</span></span> <span data-ttu-id="87adf-167">**数量** フィールドに *3* と入力します。</span><span class="sxs-lookup"><span data-stu-id="87adf-167">In the **Quantity** field, enter *3*.</span></span>
    - <span data-ttu-id="87adf-168">**明細行 2:** **品目番号** フィールドで、*M9201* を選択します。</span><span class="sxs-lookup"><span data-stu-id="87adf-168">**Line 2:** In the **Item number** field, select *M9201*.</span></span> <span data-ttu-id="87adf-169">**数量** フィールドに *3* と入力します。</span><span class="sxs-lookup"><span data-stu-id="87adf-169">In the **Quantity** field, enter *3*.</span></span>
    - <span data-ttu-id="87adf-170">**明細行 3:** **品目番号** フィールドで、*M9202* を選択します。</span><span class="sxs-lookup"><span data-stu-id="87adf-170">**Line 3:** In the **Item number** field, select *M9202*.</span></span> <span data-ttu-id="87adf-171">**数量** フィールドに *2* と入力します。</span><span class="sxs-lookup"><span data-stu-id="87adf-171">In the **Quantity** field, enter *2*.</span></span>
    - <span data-ttu-id="87adf-172">**明細行 4:** **品目番号** フィールドで、*M9200* を選択します。</span><span class="sxs-lookup"><span data-stu-id="87adf-172">**Line 4:** In the **Item number** field, select *M9200*.</span></span> <span data-ttu-id="87adf-173">**数量** フィールドに *1* と入力します。</span><span class="sxs-lookup"><span data-stu-id="87adf-173">In the **Quantity** field, enter *1*.</span></span>
    - <span data-ttu-id="87adf-174">**明細行 5:** **品目番号** フィールドで、*M9200* を選択します。</span><span class="sxs-lookup"><span data-stu-id="87adf-174">**Line 5:** In the **Item number** field, select *M9200*.</span></span> <span data-ttu-id="87adf-175">**数量** フィールドに *3* と入力します。</span><span class="sxs-lookup"><span data-stu-id="87adf-175">In the **Quantity** field, enter *3*.</span></span>
    - <span data-ttu-id="87adf-176">**明細行 6:** **品目番号** フィールドで、*M9202* を選択します。</span><span class="sxs-lookup"><span data-stu-id="87adf-176">**Line 6:** In the **Item number** field, select *M9202*.</span></span> <span data-ttu-id="87adf-177">**数量** フィールドに *7* と入力します。</span><span class="sxs-lookup"><span data-stu-id="87adf-177">In the **Quantity** field, enter *7*.</span></span>

    <span data-ttu-id="87adf-178">各品目の合計数量の概要を次に示します。</span><span class="sxs-lookup"><span data-stu-id="87adf-178">Here is a summary of the total quantities for each item:</span></span>

    - <span data-ttu-id="87adf-179">**品目 M9200:** 各 *7* 個</span><span class="sxs-lookup"><span data-stu-id="87adf-179">**Item M9200:** *7* each</span></span>
    - <span data-ttu-id="87adf-180">**品目 M9201:** 各 *3* 個</span><span class="sxs-lookup"><span data-stu-id="87adf-180">**Item M9201:** *3* each</span></span>
    - <span data-ttu-id="87adf-181">**品目 M9202:** 各 *9* 個</span><span class="sxs-lookup"><span data-stu-id="87adf-181">**Item M9202:** *9* each</span></span>

1. <span data-ttu-id="87adf-182">注文を倉庫にリリースする前に、ピッキング場所にすべての注文のすべての品目に十分な在庫があることを確認する必要があります。</span><span class="sxs-lookup"><span data-stu-id="87adf-182">Before you release the orders to the warehouse, you must make sure that the pick locations have enough inventory for all the items on all the orders.</span></span> <span data-ttu-id="87adf-183">**場所のディレクティブ** の設定を確認して、販売注文のピッキングに使用されるピッキング場所を決定します。</span><span class="sxs-lookup"><span data-stu-id="87adf-183">Review the **Location directive** setting to determine which picking locations are used for sales order picking.</span></span> <span data-ttu-id="87adf-184">倉庫 *51* に Contoso のデモ データ環境を使用している場合は、利用可能な在庫が必要です。</span><span class="sxs-lookup"><span data-stu-id="87adf-184">If you're using the Contoso demo data environment for warehouse *51*, confirm that there is available inventory.</span></span>

    <span data-ttu-id="87adf-185">行ごとに在庫の予約を行う必要があります。</span><span class="sxs-lookup"><span data-stu-id="87adf-185">You must now reserve the inventory for each line.</span></span>

1. <span data-ttu-id="87adf-186">**販売注文明細行** クイック タブで、予約する必要がある明細行を 1 つ選択します。</span><span class="sxs-lookup"><span data-stu-id="87adf-186">On the **Sales order lines** FastTab, select one of the lines that must be reserved.</span></span>
1. <span data-ttu-id="87adf-187">グリッドの上部にある **在庫** メニューで、**引当** を選択します。</span><span class="sxs-lookup"><span data-stu-id="87adf-187">On the **Inventory** menu above the grid, select **Reservation**.</span></span>
1. <span data-ttu-id="87adf-188">**引当** ページの、アクション ペインで **ロットの引当** を選択して、予約を適用します。</span><span class="sxs-lookup"><span data-stu-id="87adf-188">On the **Reservation** page, on the Action Pane, select **Reserve lot** to apply the reservation.</span></span> <span data-ttu-id="87adf-189">その後、ページを閉じます。</span><span class="sxs-lookup"><span data-stu-id="87adf-189">Then close the page.</span></span>
1. <span data-ttu-id="87adf-190">引当する必要がある残りの行に対して、手順 8 ~ 10 を繰り返します。</span><span class="sxs-lookup"><span data-stu-id="87adf-190">Repeat steps 8 through 10 for the remaining lines that must be reserved.</span></span>

    <span data-ttu-id="87adf-191">倉庫にリリースした販売注文を選択します。</span><span class="sxs-lookup"><span data-stu-id="87adf-191">You must now release the sales order to the warehouse.</span></span>

1. <span data-ttu-id="87adf-192">アクション ウィンドウの **倉庫** タブで、**倉庫へのリリース** を選択します。</span><span class="sxs-lookup"><span data-stu-id="87adf-192">On the Action Pane, on the **Warehouse** tab, select **Release to warehouse**.</span></span>

    <span data-ttu-id="87adf-193">出荷とジョブが作成されたというメッセージと、バッチで実行するためにそのシステムが送信されたというメッセージが表示されます。</span><span class="sxs-lookup"><span data-stu-id="87adf-193">You receive a message that states that a shipment and a wave have been created, and that the wave has been submitted to run in a batch.</span></span>

    <span data-ttu-id="87adf-194">6 行の作業に対して作業 ID が作成され、そのジョブと一部のジョブが終了すると、その作業 ID が作成されます。</span><span class="sxs-lookup"><span data-stu-id="87adf-194">When the wave and all downstream jobs have been completed, a work ID is created for work that has six lines.</span></span> <span data-ttu-id="87adf-195">行は品目番号順に並べ替えられます。</span><span class="sxs-lookup"><span data-stu-id="87adf-195">The lines are sorted by item number.</span></span>

1. <span data-ttu-id="87adf-196">**倉庫管理 \> 作業 \> すべての作業** の順に移動して、作成した作業を表示します。</span><span class="sxs-lookup"><span data-stu-id="87adf-196">Go to **Warehouse management \> Work \> All work** to view the work that was created.</span></span> <span data-ttu-id="87adf-197">次の手順で必要になるので、**作業 ID** の値をメモしておきます。</span><span class="sxs-lookup"><span data-stu-id="87adf-197">Make a note of the **Work ID** value, because you will need it in the next procedure.</span></span>

### <a name="initiate-picking-from-the-mobile-device"></a><span data-ttu-id="87adf-198">モバイル デバイスからのピッキングの開始</span><span class="sxs-lookup"><span data-stu-id="87adf-198">Initiate picking from the mobile device</span></span>

1. <span data-ttu-id="87adf-199">倉庫 *51* に設定されているユーザーとして、モバイル デバイスにサインインします。</span><span class="sxs-lookup"><span data-stu-id="87adf-199">Sign in to the mobile device as a user who is set up for warehouse *51*.</span></span>
1. <span data-ttu-id="87adf-200">モバイル デバイスで、モバイル デバイス メニュー品目を含むメニューを選択します。</span><span class="sxs-lookup"><span data-stu-id="87adf-200">On the mobile device, select the menu that includes the new mobile device menu item.</span></span> <span data-ttu-id="87adf-201">このシナリオでは **出荷** を選択します。</span><span class="sxs-lookup"><span data-stu-id="87adf-201">For this scenario, select **Outbound**.</span></span>
1. <span data-ttu-id="87adf-202">**販売グループ行ピッキング** メニュー品目を選択して、ピッキングを開始します。</span><span class="sxs-lookup"><span data-stu-id="87adf-202">Select the **Sales group line picking** menu item to initiate the pick.</span></span>
1. <span data-ttu-id="87adf-203">前の手順でメモした **作業 ID** 値を入力します。</span><span class="sxs-lookup"><span data-stu-id="87adf-203">Enter the **Work ID** value that you made a note of in the previous procedure.</span></span>

    <span data-ttu-id="87adf-204">品目 *M9200* のすべてのピック明細行がグループ化されるピック ステップが表示され、各品目 *M9200を* の *7* つをピックする指示が表示される必要があります。</span><span class="sxs-lookup"><span data-stu-id="87adf-204">You should see a pick step where all pick lines for item *M9200* are grouped, and you should receive an instruction to pick *7* each of item *M9200*.</span></span>

    > [!IMPORTANT]
    > <span data-ttu-id="87adf-205">モバイル デバイスでは、3 つのピッキング作業明細行のピッキング作業が、ユーザーの 1 つのピッキング ステップに集計されています。</span><span class="sxs-lookup"><span data-stu-id="87adf-205">On the mobile device, the pick work for the three pick work lines has been aggregated into one picking step for the user.</span></span>

1. <span data-ttu-id="87adf-206">ピッキング ステップを確定します。</span><span class="sxs-lookup"><span data-stu-id="87adf-206">Confirm the pick step.</span></span>
1. <span data-ttu-id="87adf-207">作業 ID の作業頁に移動して、品目 *M9200* の 3 つのピッキング明細行がすべて同時に閉じられていることを確認します。</span><span class="sxs-lookup"><span data-stu-id="87adf-207">Go to the work page for the work ID, and notice that all three pick lines for item *M9200* were closed simultaneously.</span></span>
1. <span data-ttu-id="87adf-208">モバイル デバイスに戻り、ピックを続行します。</span><span class="sxs-lookup"><span data-stu-id="87adf-208">Go back to the mobile device, and continue to pick.</span></span> <span data-ttu-id="87adf-209">品目 *M9201* の作業行 4 が表示されます。</span><span class="sxs-lookup"><span data-stu-id="87adf-209">Work line 4 for item *M9201* should be presented.</span></span> <span data-ttu-id="87adf-210">注文には作業行が 1 行しかないので、集計する必要は何もありません。</span><span class="sxs-lookup"><span data-stu-id="87adf-210">Because there was only one work line on the order, there is nothing to aggregate.</span></span>
1. <span data-ttu-id="87adf-211">ピッキング ステップを確定します。</span><span class="sxs-lookup"><span data-stu-id="87adf-211">Confirm the pick step.</span></span>
1. <span data-ttu-id="87adf-212">モバイル デバイスの最後のピッキング ステップでは、ワーク オーダーから最後の 2 つのピッキング明細行を集計します。</span><span class="sxs-lookup"><span data-stu-id="87adf-212">The last pick step on the mobile device aggregates the last two pick lines from the work order.</span></span>
1. <span data-ttu-id="87adf-213">品目 *M9202* の各 *9* 個のピッキング ステップを完了します。</span><span class="sxs-lookup"><span data-stu-id="87adf-213">Complete the pick step for *9* each of item *M9202*.</span></span>
1. <span data-ttu-id="87adf-214">作業を完了するには、プット ステップと、追加のピック / プットのペアを確認します。</span><span class="sxs-lookup"><span data-stu-id="87adf-214">Confirm the put step and any additional pick/put pairs to complete the work.</span></span>

> [!IMPORTANT]
>
> - <span data-ttu-id="87adf-215">作業明細行は、順序が正しい場合にのみグループ化できます。</span><span class="sxs-lookup"><span data-stu-id="87adf-215">Work lines can be grouped only if they are in sequence.</span></span>
> - <span data-ttu-id="87adf-216">次の機能はサポートされていません。</span><span class="sxs-lookup"><span data-stu-id="87adf-216">The following functionality isn't supported:</span></span>
>
>   - <span data-ttu-id="87adf-217">CW 品目</span><span class="sxs-lookup"><span data-stu-id="87adf-217">Catch-weight items</span></span>
>
>    <span data-ttu-id="87adf-218">作業に CW 品目がある場合は、ピッキングを開始する前にエラー メッセージが表示されます。</span><span class="sxs-lookup"><span data-stu-id="87adf-218">If there are any catch-weight items on the work, you receive an error message before you start to pick.</span></span>
>
>   - <span data-ttu-id="87adf-219">ピース ピッキング</span><span class="sxs-lookup"><span data-stu-id="87adf-219">Piece picking</span></span>
>   - <span data-ttu-id="87adf-220">未完了の補充作業がある作業明細行</span><span class="sxs-lookup"><span data-stu-id="87adf-220">Work lines that have unfinished replenishment work</span></span>
>   - <span data-ttu-id="87adf-221">超過ピッキング</span><span class="sxs-lookup"><span data-stu-id="87adf-221">Over-picking</span></span>
>   - <span data-ttu-id="87adf-222">品目再配賦の未処理ピッキング</span><span class="sxs-lookup"><span data-stu-id="87adf-222">Short picking with item reallocation</span></span>
