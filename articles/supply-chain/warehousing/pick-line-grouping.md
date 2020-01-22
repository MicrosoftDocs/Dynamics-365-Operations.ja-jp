---
title: ピッキング行のグループ化
description: このトピックでは、ピッキング行のグループ化の概要を示します。
author: Mirzaab
manager: AnnBe
ms.date: 12/10/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations, Supply Chain Management
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: perlynne
ms.search.validFrom: 2019-12-31
ms.dyn365.ops.version: 10.0.1
ms.openlocfilehash: 1b1d0135d450bc9be7b1303240a9ca70f95ae38e
ms.sourcegitcommit: 610d5c3efadbaf11752b46f24680af619bcd70a6
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 12/10/2019
ms.locfileid: "2906271"
---
# <a name="pick-line-grouping"></a><span data-ttu-id="a6241-103">ピッキング行のグループ化</span><span class="sxs-lookup"><span data-stu-id="a6241-103">Pick line grouping</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="a6241-104">ピッキング行のグループ化では、品目と場所が同じ複数の作業明細行を結合して、モバイル デバイスでユーザーに提示される 1 つのピッキングを作成できます。</span><span class="sxs-lookup"><span data-stu-id="a6241-104">In pick line grouping, multiple work lines that have the same item and location can be combined into a single pick that is presented to the user on a mobile device.</span></span> <span data-ttu-id="a6241-105">したがって、倉庫の作業者は、可能な限り効率的な指示を受け取ることができますが、システムに必要な作業明細行の分割 (たとえば、異なるコンテナや注文など) も維持されます。</span><span class="sxs-lookup"><span data-stu-id="a6241-105">Therefore, warehouse workers can receive the most efficient instructions that are possible, but the required separation of work lines in the system is also maintained (for example, for different containers and orders).</span></span>

## <a name="set-up-pick-line-grouping"></a><span data-ttu-id="a6241-106">ピッキング行のグループ化の設定</span><span class="sxs-lookup"><span data-stu-id="a6241-106">Set up pick line grouping</span></span>

### <a name="create-a-mobile-device-menu-item"></a><span data-ttu-id="a6241-107">品目のモバイル デバイス メニューの作成</span><span class="sxs-lookup"><span data-stu-id="a6241-107">Create a mobile device menu item</span></span>

1. <span data-ttu-id="a6241-108">**倉庫管理 \> 設定 \> モバイル デバイス \> モバイル デバイス メニュー項目**に移動して、**"販売グループ ライン ピッキング - ユーザー主導**という名前の新しいメニュー項目を作成します。</span><span class="sxs-lookup"><span data-stu-id="a6241-108">Go to **Warehouse management \> Setup \> Mobile device \> Mobile device menu items**, and create a new menu item that is named **Sales group line picking – User directed**.</span></span>
2. <span data-ttu-id="a6241-109">**モバイル デバイス メニュー項目**で、次の値を設定します。</span><span class="sxs-lookup"><span data-stu-id="a6241-109">Under **Mobile device menu items**, set the following values:</span></span>

    - <span data-ttu-id="a6241-110">**メニュー項目名**フィールドに、**販売ピッキング - グループ明細行**と入力します。</span><span class="sxs-lookup"><span data-stu-id="a6241-110">In the **Menu item name** field, enter **Sales Pick - Group line**.</span></span>
    - <span data-ttu-id="a6241-111">**タイトル** フィールドに、**販売ピッキング - グループ明細行**と入力します。</span><span class="sxs-lookup"><span data-stu-id="a6241-111">In the **Title** field, enter **Sales Pick - Group line**.</span></span>
    - <span data-ttu-id="a6241-112">**モード** フィールドで、**作業**を選択します。</span><span class="sxs-lookup"><span data-stu-id="a6241-112">In the **Mode** field, select **Work**.</span></span>
    - <span data-ttu-id="a6241-113">**既存の作業を使用** オプションを **はい** に設定します。</span><span class="sxs-lookup"><span data-stu-id="a6241-113">Set the **Use existing work** option to **Yes**.</span></span>

3. <span data-ttu-id="a6241-114">**一般**クイック タブで、次の値を設定します。</span><span class="sxs-lookup"><span data-stu-id="a6241-114">On the **General** FastTab, you can set the following values:</span></span>

    - <span data-ttu-id="a6241-115">**指示者**フィールドで、**ユーザー主導**を選択します。</span><span class="sxs-lookup"><span data-stu-id="a6241-115">In the **Directed by** field, select **User directed**.</span></span>
    - <span data-ttu-id="a6241-116">**ライセンス プレートの生成**オプションを**はい**に設定します。</span><span class="sxs-lookup"><span data-stu-id="a6241-116">Set the **Generate license plate** option to **Yes**.</span></span>
    - <span data-ttu-id="a6241-117">**グループ ピック** オプションを**はい**に設定します。</span><span class="sxs-lookup"><span data-stu-id="a6241-117">Set the **Group pick** option to **Yes**.</span></span>

4. <span data-ttu-id="a6241-118">**作業クラス** クイック タブで、次の手順に従って、モバイル デバイスのメニュー項目に対して有効な作業クラスを構成します。</span><span class="sxs-lookup"><span data-stu-id="a6241-118">On the **Work classes** FastTab, follow these steps to configure the valid work classes for the mobile device menu item:</span></span>

    1. <span data-ttu-id="a6241-119">**新規** を選択します。</span><span class="sxs-lookup"><span data-stu-id="a6241-119">Select **New**.</span></span>
    2. <span data-ttu-id="a6241-120">**作業クラス ID** フィールドで、使用する倉庫に応じて**販売**または **SO ピッキング**を選択します。</span><span class="sxs-lookup"><span data-stu-id="a6241-120">In the **Work class ID** field, select **Sales** or **SO Pick**, depending on the warehouse that you will use.</span></span>
    3. <span data-ttu-id="a6241-121">**ワーク オーダー タイプ** フィールドで、**販売注文**を選択します。</span><span class="sxs-lookup"><span data-stu-id="a6241-121">In the **Work order type** field, select **Sales orders**.</span></span>

### <a name="set-up-a-mobile-device-menu"></a><span data-ttu-id="a6241-122">モバイル デバイス メニューを設定する</span><span class="sxs-lookup"><span data-stu-id="a6241-122">Set up a mobile device menu</span></span>

1. <span data-ttu-id="a6241-123">**倉庫管理 \> 設定 \> モバイル デバイス \> モバイル デバイス メニュー**の順に移動します。</span><span class="sxs-lookup"><span data-stu-id="a6241-123">Go to **Warehouse management \> Setup \> Mobile device \> Mobile device menu**.</span></span> 
1. <span data-ttu-id="a6241-124">作成したメニュー項目を目的のメニューに追加します。</span><span class="sxs-lookup"><span data-stu-id="a6241-124">Add the menu item that you just created to the desired menu.</span></span>

### <a name="set-up-a-work-template"></a><span data-ttu-id="a6241-125">作業テンプレートを設定する</span><span class="sxs-lookup"><span data-stu-id="a6241-125">Set up a work template</span></span>

1. <span data-ttu-id="a6241-126">**倉庫管理 \> 設定 \> 作業 \> 作業テンプレート**の順に移動します。</span><span class="sxs-lookup"><span data-stu-id="a6241-126">Go to **Warehouse management \> Setup \> Work \> Work templates**.</span></span>
1. <span data-ttu-id="a6241-127">この機能で使用する必要がある作業テンプレートを検索します。</span><span class="sxs-lookup"><span data-stu-id="a6241-127">Find the work template that should be used with this function.</span></span> <span data-ttu-id="a6241-128">この例では、標準の **51 ステージにピック** Contoso 作業テンプレートを選択します。</span><span class="sxs-lookup"><span data-stu-id="a6241-128">For this example, select the standard **51 Pick to stage** Contoso work template.</span></span>
1. <span data-ttu-id="a6241-129">メニューで**クエリの編集**を選択します。</span><span class="sxs-lookup"><span data-stu-id="a6241-129">On the menu, select **Edit query**.</span></span>
1. <span data-ttu-id="a6241-130">**並べ替え**タブで**追加**を選択し、次の値を設定します。</span><span class="sxs-lookup"><span data-stu-id="a6241-130">On the **Sorting** tab, select **Add**, and then set the following values:</span></span>

    - <span data-ttu-id="a6241-131">**テーブル** フィールドで、**一時的な作業トランザクション**を選択します。</span><span class="sxs-lookup"><span data-stu-id="a6241-131">In the **Table** field, select **Temporary work transactions**.</span></span>
    - <span data-ttu-id="a6241-132">**派生テーブル** フィールドで、**一時的な作業トランザクション**を選択します。</span><span class="sxs-lookup"><span data-stu-id="a6241-132">In the **Derived table** field, select **Temporary work transactions**.</span></span>
    - <span data-ttu-id="a6241-133">**フィールド** フィールドで、**品目番号**を選択します。</span><span class="sxs-lookup"><span data-stu-id="a6241-133">In the **Field** field, select **Item number**.</span></span>
    - <span data-ttu-id="a6241-134">**検索の方向**フィールドで、**昇順**を選択します。</span><span class="sxs-lookup"><span data-stu-id="a6241-134">In the **Search direction** field, select **Ascending**.</span></span>

> [!NOTE]
> <span data-ttu-id="a6241-135">ピッキング行のグループ化機能を機能させるには、作業明細行を品目 ID で並べ替える必要があります。</span><span class="sxs-lookup"><span data-stu-id="a6241-135">For the pick line grouping functionality to work, the work lines must be sorted by item ID.</span></span> <span data-ttu-id="a6241-136">同じ品目を含む行が順序付けされない場合は、グループ化されません。</span><span class="sxs-lookup"><span data-stu-id="a6241-136">If lines that have the same items aren't sequenced one after another, they won't be grouped.</span></span>

## <a name="example"></a><span data-ttu-id="a6241-137">例</span><span class="sxs-lookup"><span data-stu-id="a6241-137">Example</span></span>

### <a name="create-picking-work"></a><span data-ttu-id="a6241-138">ピッキング作業の作成</span><span class="sxs-lookup"><span data-stu-id="a6241-138">Create picking work</span></span>

<span data-ttu-id="a6241-139">ピッキング行のグループ化を設定する前に、適格な出荷作業をいくつか作成する必要があります。</span><span class="sxs-lookup"><span data-stu-id="a6241-139">Before you can set up pick line grouping, you must create some eligible outbound work.</span></span>

1. <span data-ttu-id="a6241-140">**販売とマーケティング \> 販売注文 \> すべての販売注文**の順に移動します。</span><span class="sxs-lookup"><span data-stu-id="a6241-140">Go to **Sales and Marketing \> Sales orders \> All sales orders**.</span></span>
2. <span data-ttu-id="a6241-141">**新規**を選択して新しい販売注文を作成します。</span><span class="sxs-lookup"><span data-stu-id="a6241-141">Select **New** to create a sales order.</span></span> 
3. <span data-ttu-id="a6241-142">**顧客口座**フィールドで、顧客を選択します。</span><span class="sxs-lookup"><span data-stu-id="a6241-142">In the **Customer account** field, select any customer.</span></span> 
4. <span data-ttu-id="a6241-143">**一般** クイック タブの**倉庫**フィールドで、**51** を選択します。</span><span class="sxs-lookup"><span data-stu-id="a6241-143">On the **General** FastTab, in the **Warehouse** field, select **51**.</span></span> <span data-ttu-id="a6241-144">その後、**OK** を選択します。</span><span class="sxs-lookup"><span data-stu-id="a6241-144">Then select **OK**.</span></span>
5. <span data-ttu-id="a6241-145">**販売注文明細行**で、次の 6 行を追加します。</span><span class="sxs-lookup"><span data-stu-id="a6241-145">Under **Sales order lines**, add the following six lines:</span></span>

    - <span data-ttu-id="a6241-146">**明細行 1:** **品目番号**フィールドで、**M9200** を選択します。</span><span class="sxs-lookup"><span data-stu-id="a6241-146">**Line 1:** In the **Item number** field, select **M9200**.</span></span> <span data-ttu-id="a6241-147">**数量**フィールドに **3** と入力します。</span><span class="sxs-lookup"><span data-stu-id="a6241-147">In the **Quantity** field, enter **3**.</span></span>
    - <span data-ttu-id="a6241-148">**明細行 2:** **品目番号**フィールドで、**M9201** を選択します。</span><span class="sxs-lookup"><span data-stu-id="a6241-148">**Line 2:** In the **Item number** field, select **M9201**.</span></span> <span data-ttu-id="a6241-149">**数量**フィールドに **3** と入力します。</span><span class="sxs-lookup"><span data-stu-id="a6241-149">In the **Quantity** field, enter **3**.</span></span> 
    - <span data-ttu-id="a6241-150">**明細行 3:** **品目番号**フィールドで、**M9202** を選択します。</span><span class="sxs-lookup"><span data-stu-id="a6241-150">**Line 3:** In the **Item number** field, select **M9202**.</span></span> <span data-ttu-id="a6241-151">**数量**フィールドに **2** と入力します。</span><span class="sxs-lookup"><span data-stu-id="a6241-151">In the **Quantity** field, enter **2**.</span></span> 
    - <span data-ttu-id="a6241-152">**明細行 4:** **品目番号**フィールドで、**M9200** を選択します。</span><span class="sxs-lookup"><span data-stu-id="a6241-152">**Line 4:** In the **Item number** field, select **M9200**.</span></span> <span data-ttu-id="a6241-153">**数量**フィールドに **1** と入力します。</span><span class="sxs-lookup"><span data-stu-id="a6241-153">In the **Quantity** field, enter **1**.</span></span> 
    - <span data-ttu-id="a6241-154">**明細行 5:** **品目番号**フィールドで、**M9200** を選択します。</span><span class="sxs-lookup"><span data-stu-id="a6241-154">**Line 5:** In the **Item number** field, select **M9200**.</span></span> <span data-ttu-id="a6241-155">**数量**フィールドに **3** と入力します。</span><span class="sxs-lookup"><span data-stu-id="a6241-155">In the **Quantity** field, enter **3**.</span></span>
    - <span data-ttu-id="a6241-156">**明細行 6:** **品目番号**フィールドで、**M9202** を選択します。</span><span class="sxs-lookup"><span data-stu-id="a6241-156">**Line 6:** In the **Item number** field, select **M9202**.</span></span> <span data-ttu-id="a6241-157">**数量**フィールドに **7** と入力します。</span><span class="sxs-lookup"><span data-stu-id="a6241-157">In the **Quantity** field, enter **7**.</span></span> 

    <span data-ttu-id="a6241-158">各品目の合計数量の概要を次に示します。</span><span class="sxs-lookup"><span data-stu-id="a6241-158">Here is a summary of the total quantities for each item:</span></span>

    - <span data-ttu-id="a6241-159">**品目 M9200:** 各 7</span><span class="sxs-lookup"><span data-stu-id="a6241-159">**Item M9200:** 7 each</span></span>
    - <span data-ttu-id="a6241-160">**品目 M9201:** 各 3</span><span class="sxs-lookup"><span data-stu-id="a6241-160">**Item M9201:** 3 each</span></span>
    - <span data-ttu-id="a6241-161">**品目 M9202:** 各 9</span><span class="sxs-lookup"><span data-stu-id="a6241-161">**Item M9202:** 9 each</span></span>

6. <span data-ttu-id="a6241-162">注文を倉庫にリリースする前に、ピッキング場所にすべての注文のすべての品目に十分な在庫があることを確認する必要があります。</span><span class="sxs-lookup"><span data-stu-id="a6241-162">Before you release the orders to the warehouse, you must make sure that the pick locations have enough inventory for all the items on all the orders.</span></span> <span data-ttu-id="a6241-163">**場所のディレクティブ**の設定を確認して、販売注文のピッキングに使用されるピッキング場所を決定します。</span><span class="sxs-lookup"><span data-stu-id="a6241-163">Review the **Location directive** setting to determine which picking locations are used for sales order picking.</span></span>
7. <span data-ttu-id="a6241-164">在庫を引当し、倉庫にリリースします。</span><span class="sxs-lookup"><span data-stu-id="a6241-164">Reserve the inventory, and release it to the warehouse.</span></span> <span data-ttu-id="a6241-165">6 行の作業 ID が作成されます。</span><span class="sxs-lookup"><span data-stu-id="a6241-165">A work ID that has six lines is created.</span></span> <span data-ttu-id="a6241-166">行は品目番号順に並べ替えられます。</span><span class="sxs-lookup"><span data-stu-id="a6241-166">The lines are sorted by item number.</span></span>

### <a name="run-the-mobile-device-flow"></a><span data-ttu-id="a6241-167">モバイル デバイス フローを実行する</span><span class="sxs-lookup"><span data-stu-id="a6241-167">Run the mobile device flow</span></span>

1. <span data-ttu-id="a6241-168">モバイル デバイスで、モバイル デバイス メニュー品目を含むメニューを選択します。</span><span class="sxs-lookup"><span data-stu-id="a6241-168">On the mobile device, select the menu that includes the new mobile device menu item.</span></span>
1. <span data-ttu-id="a6241-169">**販売ピッキング - グループ明細行**メニュー品目を選択し、ピッキングを開始します。</span><span class="sxs-lookup"><span data-stu-id="a6241-169">Select the **Sales Pick – Group line** menu item, and initiate the pick.</span></span>

    <span data-ttu-id="a6241-170">メニューを選択して作業 ID を入力すると、品目 M9200 のすべてのピッキング明細行がグループ化されるピッキング ステップが表示されます。</span><span class="sxs-lookup"><span data-stu-id="a6241-170">After you select the menu and enter the work ID, you see the pick step where all pick lines for item M9200 are grouped.</span></span> <span data-ttu-id="a6241-171">品目 M9200を 7 つずつピッキングするように指示されます。</span><span class="sxs-lookup"><span data-stu-id="a6241-171">You receive an instruction to pick 7 each of item M9200.</span></span>

1. <span data-ttu-id="a6241-172">ピッキング ステップを確定します。</span><span class="sxs-lookup"><span data-stu-id="a6241-172">Confirm the pick step.</span></span> 
1. <span data-ttu-id="a6241-173">仕掛品のクライアント画面で、品目 M9200 の 3 つのピッキング明細行がすべて同時に閉じられていることを確認します。</span><span class="sxs-lookup"><span data-stu-id="a6241-173">Go to the client screen of the work in process, and notice that all three pick lines for item M9200 were closed simultaneously.</span></span>

    <span data-ttu-id="a6241-174">作業明細行 4 が表示されます。</span><span class="sxs-lookup"><span data-stu-id="a6241-174">Work line 4 is presented.</span></span>

1. <span data-ttu-id="a6241-175">ピッキング ステップを確定します。</span><span class="sxs-lookup"><span data-stu-id="a6241-175">Confirm the pick step.</span></span>

    <span data-ttu-id="a6241-176">モバイル デバイスの最後のピッキング ステップでは、ワーク オーダーから最後の 2 つのピッキング明細行を集計します。</span><span class="sxs-lookup"><span data-stu-id="a6241-176">The last pick step on the mobile device aggregates the last two pick lines from the work order.</span></span>

1. <span data-ttu-id="a6241-177">品目 M9202 の各 9 個のピッキング ステップを完了します。</span><span class="sxs-lookup"><span data-stu-id="a6241-177">Complete the pick step for 9 each of item M9202.</span></span>
1. <span data-ttu-id="a6241-178">作業を完了するには、プット ステップと、追加のピック / プットのペアを確認します。</span><span class="sxs-lookup"><span data-stu-id="a6241-178">Confirm the put step and any additional pick/put pairs to complete the work.</span></span>

> [!NOTE]
> - <span data-ttu-id="a6241-179">作業明細行は、順序が正しい場合にのみグループ化できます。</span><span class="sxs-lookup"><span data-stu-id="a6241-179">Work lines can be grouped only if they are in sequence.</span></span>
> - <span data-ttu-id="a6241-180">次の機能はサポートされていません。</span><span class="sxs-lookup"><span data-stu-id="a6241-180">The following functionality isn't supported:</span></span>
>
>    - <span data-ttu-id="a6241-181">CW 品目。</span><span class="sxs-lookup"><span data-stu-id="a6241-181">Catch-weight items.</span></span> <span data-ttu-id="a6241-182">作業に CW 品目がある場合は、ピッキングを開始する前にエラー メッセージが表示されます。</span><span class="sxs-lookup"><span data-stu-id="a6241-182">If there are any catch-weight items on the work, you receive an error message before you start to pick.</span></span>
>    - <span data-ttu-id="a6241-183">ピース ピッキング。</span><span class="sxs-lookup"><span data-stu-id="a6241-183">Piece picking.</span></span>
>    - <span data-ttu-id="a6241-184">未完了の補充作業がある作業明細行。</span><span class="sxs-lookup"><span data-stu-id="a6241-184">Work lines that have unfinished replenishment work.</span></span>
>    - <span data-ttu-id="a6241-185">超過ピッキング。</span><span class="sxs-lookup"><span data-stu-id="a6241-185">Over-picking.</span></span>
