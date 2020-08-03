---
title: 作業での作業プールの変更
description: このトピックでは、作業項目の [作業プールの変更] ボタンを使用して、既存の作業の作業プールを変更する方法について説明します。
author: mirzaab
manager: tfehr
ms.date: 07/16/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Retail, Core, Operations
ms.search.region: global
ms.author: mirzaab
ms.search.validFrom: 2020-07-16
ms.dyn365.ops.version: Release 10.0.8
ms.openlocfilehash: 33238b114f0939711163b19ae7af98be7c8d0744
ms.sourcegitcommit: f64fce03ec52f844b05a9e8cac286cb201385002
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 07/16/2020
ms.locfileid: "3597548"
---
# <a name="change-work-pool-on-work"></a><span data-ttu-id="badca-103">作業での作業プールの変更</span><span class="sxs-lookup"><span data-stu-id="badca-103">Change work pool on work</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="badca-104">作業プールを使用すると、作業をグループに整理することができます。</span><span class="sxs-lookup"><span data-stu-id="badca-104">You can use work pools to organize work into groups.</span></span> <span data-ttu-id="badca-105">たとえば、特定の倉庫の場所で発生する作業を分類する作業プールを作成できます。</span><span class="sxs-lookup"><span data-stu-id="badca-105">For example, you can create a work pool to classify work that occurs in a specific warehouse location.</span></span>

<span data-ttu-id="badca-106">*作業中の作業プールを変更する*機能を使用すると、作業項目のアクション ウィンドウに **作業プールの変更** ボタンが追加されます。</span><span class="sxs-lookup"><span data-stu-id="badca-106">The *Change work pool on work* feature adds a **Change work pool** button to the Action Pane for work items.</span></span> <span data-ttu-id="badca-107">したがって、倉庫管理者は、既存の作業の作業プールを簡単に変更できます。</span><span class="sxs-lookup"><span data-stu-id="badca-107">Therefore, warehouse managers can easily change the work pool of existing work.</span></span> <span data-ttu-id="badca-108">この機能により、倉庫の作業現場における変化に迅速に対応できるようになり、状況の変化に対する適応能力の改善や、作業を別の作業プールに移動する必要性が改善されるようになります。</span><span class="sxs-lookup"><span data-stu-id="badca-108">This feature lets managers react quickly to changes on the warehouse shop floor, and it helps improve their ability to adapt to changing situations and the need to transfer work to another work pool.</span></span>

## <a name="turn-on-the-change-work-pool-on-work-feature"></a><span data-ttu-id="badca-109">作業中の作業プールの変更機能を有効にします</span><span class="sxs-lookup"><span data-stu-id="badca-109">Turn on the Change work pool on work feature</span></span>

<span data-ttu-id="badca-110">この機能の設定、または使用を開始する前に、システムで使用可能な状態になっていることを確認する必要があります。</span><span class="sxs-lookup"><span data-stu-id="badca-110">Before you begin to set up or use this feature, you must make sure that it's available in your system.</span></span> <span data-ttu-id="badca-111">管理者は、[機能の管理](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md)設定を使用して、機能の状態を確認し、必要に応じて有効にすることができます。</span><span class="sxs-lookup"><span data-stu-id="badca-111">Admins can use the [feature management](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) settings to check the status of the feature and turn it on if it's required.</span></span> <span data-ttu-id="badca-112">**機能管理** ワークスペースで、この機能は次のようにリストされています。</span><span class="sxs-lookup"><span data-stu-id="badca-112">In the **Feature management** workspace, the feature is listed in the following way:</span></span>

- <span data-ttu-id="badca-113">**モジュール:** *倉庫管理*</span><span class="sxs-lookup"><span data-stu-id="badca-113">**Module:** *Warehouse management*</span></span>
- <span data-ttu-id="badca-114">**機能の名称 :** *作業中の作業プールの変更*</span><span class="sxs-lookup"><span data-stu-id="badca-114">**Feature name:** *Change work pool on work*</span></span>

## <a name="set-up-the-change-work-pool-on-work-feature"></a><span data-ttu-id="badca-115">作業中の作業プールの変更機能を設定する</span><span class="sxs-lookup"><span data-stu-id="badca-115">Set up the Change work pool on work feature</span></span>

<span data-ttu-id="badca-116">この機能を使用するには、いくつかの作業プールが設定されている必要があります。</span><span class="sxs-lookup"><span data-stu-id="badca-116">To use this feature, you must have some work pools set up.</span></span> <span data-ttu-id="badca-117">作業のテンプレートは、プールを自動的に割り当てられるように設定することもできます。</span><span class="sxs-lookup"><span data-stu-id="badca-117">You might also set up your work templates so that they automatically assign a pool.</span></span> <span data-ttu-id="badca-118">このトピックで後ほど説明するシナリオの例を使用する場合は、このセクションの説明に従ってシステムを設定します。</span><span class="sxs-lookup"><span data-stu-id="badca-118">If you want to work through the example scenario that is provided later in this topic, set up your system as described in this section.</span></span>

### <a name="set-up-work-pools"></a><span data-ttu-id="badca-119">作業プールの設定</span><span class="sxs-lookup"><span data-stu-id="badca-119">Set up work pools</span></span>

<span data-ttu-id="badca-120">作業プールを使用すると、作業項目をタイプ別に編成できます。</span><span class="sxs-lookup"><span data-stu-id="badca-120">Work pools let you organize work items by type.</span></span> <span data-ttu-id="badca-121">*作業中の作業プールの変更*機能を使用するには 、少なくとも2つの作業プールが使用可能な状態となっている必要があります。</span><span class="sxs-lookup"><span data-stu-id="badca-121">To work with the *Change work pool on work* feature, you must have at least two work pools available.</span></span> <span data-ttu-id="badca-122">作業プールの表示と追加をするには、以下の手順を実行します。</span><span class="sxs-lookup"><span data-stu-id="badca-122">To view and add work pools, follow these steps.</span></span>

1. <span data-ttu-id="badca-123">**倉庫管理 \> 設定 \> 作業 \> 作業プール** に移動します。</span><span class="sxs-lookup"><span data-stu-id="badca-123">Go to **Warehouse management \> Setup \> Work \> Work pools**.</span></span>
1. <span data-ttu-id="badca-124">**USMF**社のデモ データを使用して作業を行い、このトピックで後述するシナリオに従って作業する場合は、次のように設定された2つの作業プールを追加してください。</span><span class="sxs-lookup"><span data-stu-id="badca-124">If you're working with demo data from the **USMF** company and will work through the example scenario later in this topic, add two work pools that have the following settings:</span></span>

    - <span data-ttu-id="badca-125">作業プール 1:</span><span class="sxs-lookup"><span data-stu-id="badca-125">Work pool 1:</span></span>

        - <span data-ttu-id="badca-126">**作業プール ID:** *Webshop*</span><span class="sxs-lookup"><span data-stu-id="badca-126">**Work pool ID:** *Webshop*</span></span>
        - <span data-ttu-id="badca-127">**説明 :** *Web ショップ*</span><span class="sxs-lookup"><span data-stu-id="badca-127">**Description:** *Web Shop*</span></span>

    - <span data-ttu-id="badca-128">作業プール 2:</span><span class="sxs-lookup"><span data-stu-id="badca-128">Work pool 2:</span></span>

        - <span data-ttu-id="badca-129">**作業 プール ID:** *CallCenter*</span><span class="sxs-lookup"><span data-stu-id="badca-129">**Work pool ID:** *CallCenter*</span></span>
        - <span data-ttu-id="badca-130">**説明 :** *コールセンター*</span><span class="sxs-lookup"><span data-stu-id="badca-130">**Description:** *Call Center*</span></span>

1. <span data-ttu-id="badca-131">アクション ウィンドウで、**保存**を選択します。</span><span class="sxs-lookup"><span data-stu-id="badca-131">On the Action Pane, select **Save**.</span></span>

### <a name="set-up-work-templates"></a><span data-ttu-id="badca-132">作業テンプレートを設定します</span><span class="sxs-lookup"><span data-stu-id="badca-132">Set up work templates</span></span>

<span data-ttu-id="badca-133">作業テンプレートごとに、必要に応じて既定の作業プールを設定できます。</span><span class="sxs-lookup"><span data-stu-id="badca-133">For each of your work templates, you can set a default work pool, as you require.</span></span> <span data-ttu-id="badca-134">関連するテンプレートごとに、**作業プール ID** 列に作業プールを割り当てます。</span><span class="sxs-lookup"><span data-stu-id="badca-134">For each relevant template, you assign a work pool in the **Work pool ID** column.</span></span> <span data-ttu-id="badca-135">この場合、特定のテンプレートを使用して生成されるすべての作業項目は、割り当てられた作業プールを自動的に継承します。</span><span class="sxs-lookup"><span data-stu-id="badca-135">In this case, all work items that are generated by using a given template automatically inherit the assigned work pool.</span></span> <span data-ttu-id="badca-136">**USMF**社のデモ データを使用して作業を行い、このトピックで後述するシナリオに従って作業する場合は、次の設定に従ってください。</span><span class="sxs-lookup"><span data-stu-id="badca-136">If you're working with the demo data from the **USMF** company and will work through the example scenario later in this topic, follow these steps.</span></span>

1. <span data-ttu-id="badca-137">**倉庫管理 \> 設定 \> 作業 \> 作業テンプレート**の順に移動します。</span><span class="sxs-lookup"><span data-stu-id="badca-137">Go to **Warehouse management \> Setup \> Work \> Work templates**.</span></span>
1. <span data-ttu-id="badca-138">アクション ウィンドウで**編集**を選択し、ページを編集モードに変更します。</span><span class="sxs-lookup"><span data-stu-id="badca-138">On the Action Pane, select **Edit** to put the page into editing mode.</span></span>
1. <span data-ttu-id="badca-139">以下の値を設定してテンプレートを編集します。</span><span class="sxs-lookup"><span data-stu-id="badca-139">Edit the template by setting the following values:</span></span>

    - <span data-ttu-id="badca-140">**作業テンプレート :** *62 件のピッキングをして梱包する*</span><span class="sxs-lookup"><span data-stu-id="badca-140">**Work template:** *62 Pick to pack*</span></span>
    - <span data-ttu-id="badca-141">**作業プール ID:** *Webshop*</span><span class="sxs-lookup"><span data-stu-id="badca-141">**Work pool ID:** *Webshop*</span></span>

1. <span data-ttu-id="badca-142">**保存** を選択します。</span><span class="sxs-lookup"><span data-stu-id="badca-142">Select **Save**.</span></span>

## <a name="example-scenario"></a><span data-ttu-id="badca-143">シナリオ例</span><span class="sxs-lookup"><span data-stu-id="badca-143">Example scenario</span></span>

<span data-ttu-id="badca-144">このシナリオでは、既存の作業項目の作業プールを変更して処理の流れを変更する方法を説明します。</span><span class="sxs-lookup"><span data-stu-id="badca-144">This scenario shows how to change the stream of processing for an existing work item by changing its work pool.</span></span> <span data-ttu-id="badca-145">このトピックでは、**USMF** 社のデモデータと、このトピックで前述した設定を使用します。</span><span class="sxs-lookup"><span data-stu-id="badca-145">It uses demo data from the **USMF** company and the settings that were suggested earlier in this topic.</span></span>

### <a name="create-a-sales-order-and-release-it-to-the-warehouse"></a><span data-ttu-id="badca-146">販売注文を作成して倉庫にリリースする</span><span class="sxs-lookup"><span data-stu-id="badca-146">Create a sales order and release it to the warehouse</span></span>

1. <span data-ttu-id="badca-147">倉庫*62*の品目 *A0001* と *A0002* に十分な手持在庫があることを確認してください。</span><span class="sxs-lookup"><span data-stu-id="badca-147">Confirm that there is enough on-hand inventory for items *A0001* and *A0002* in warehouse *62*.</span></span> <span data-ttu-id="badca-148">**在庫管理 \> 照会とレポート \> 手持在庫一覧**に移動し、フィルターを次のように編集します。</span><span class="sxs-lookup"><span data-stu-id="badca-148">Go to **Inventory management \> Inquiries and reports \> On-hand list**, and edit the filters as shown here:</span></span>

    - <span data-ttu-id="badca-149">**倉庫**の値が、*62*で始まる。</span><span class="sxs-lookup"><span data-stu-id="badca-149">The **Warehouse** value begins with *62*.</span></span>
    - <span data-ttu-id="badca-150">**品目番号**の値が、*A001*、または *A002* のいずれかである。</span><span class="sxs-lookup"><span data-stu-id="badca-150">The **Item number** value is either *A001* or *A002*.</span></span>

    <span data-ttu-id="badca-151">デモデータの数量には、それぞれ 10 を設定する必要があります。</span><span class="sxs-lookup"><span data-stu-id="badca-151">Demo data should have a quantity of 10 each.</span></span>

    <span data-ttu-id="badca-152">続いて、販売注文を作成する必要があります。</span><span class="sxs-lookup"><span data-stu-id="badca-152">Next, you must create a sales order.</span></span>

1. <span data-ttu-id="badca-153">**販売とマーケティング \> 販売注文 \> すべての販売注文**の順に移動します。</span><span class="sxs-lookup"><span data-stu-id="badca-153">Go to **Sales and marketing \> Sales orders \> All sales orders**.</span></span>
1. <span data-ttu-id="badca-154">アクション ウィンドウで、**新規**を選択します。</span><span class="sxs-lookup"><span data-stu-id="badca-154">On the Action Pane, select **New**.</span></span>
1. <span data-ttu-id="badca-155">**販売注文の作成**ダイアログ ボックスでは、次の値を設定します。</span><span class="sxs-lookup"><span data-stu-id="badca-155">In the **Create sales order** dialog box, set the following values:</span></span>

    - <span data-ttu-id="badca-156">**顧客アカウント:** *US-007*</span><span class="sxs-lookup"><span data-stu-id="badca-156">**Customer account:** *US-007*</span></span>
    - <span data-ttu-id="badca-157">**倉庫:** *62*</span><span class="sxs-lookup"><span data-stu-id="badca-157">**Warehouse:** *62*</span></span>

1. <span data-ttu-id="badca-158">**OK** を選択して販売注文を作成し、ダイアログ ボックスを閉じます。</span><span class="sxs-lookup"><span data-stu-id="badca-158">Select **OK** to create the sales order and close the dialog box.</span></span>
1. <span data-ttu-id="badca-159">新しい販売注文が開かれます。</span><span class="sxs-lookup"><span data-stu-id="badca-159">The new sales order is opened.</span></span> <span data-ttu-id="badca-160">**販売注文明細行**クイック タブのグリッドに、新しい空の明細行を含める必要があります。</span><span class="sxs-lookup"><span data-stu-id="badca-160">It should include a new, empty line in the grid on the **Sales order lines** FastTab.</span></span> <span data-ttu-id="badca-161">この明細行で、次の値を設定します。</span><span class="sxs-lookup"><span data-stu-id="badca-161">On this line, set the following values:</span></span>

    - <span data-ttu-id="badca-162">**品目番号:** *A0001*</span><span class="sxs-lookup"><span data-stu-id="badca-162">**Item number:** *A0001*</span></span>
    - <span data-ttu-id="badca-163">**数量:** *2*</span><span class="sxs-lookup"><span data-stu-id="badca-163">**Quantity:** *2*</span></span>

1. <span data-ttu-id="badca-164">グリッドの上部にある**在庫**メニューで、**引当**を選択します。</span><span class="sxs-lookup"><span data-stu-id="badca-164">On the **Inventory** menu above the grid, select **Reservation**.</span></span>
1. <span data-ttu-id="badca-165">**引当** ページの、アクション ウィンドウで**ロットの引当**を選択して、在庫を引当てします。</span><span class="sxs-lookup"><span data-stu-id="badca-165">On the **Reservation** page, on the Action Pane, select **Reserve lot** to reserve the inventory.</span></span>
1. <span data-ttu-id="badca-166">ページを閉じます。</span><span class="sxs-lookup"><span data-stu-id="badca-166">Close the page.</span></span>
1. <span data-ttu-id="badca-167">**販売注文明細行**クイック タブで、**明細行の追加**を選択して、販売注文に新たな行を追加します。</span><span class="sxs-lookup"><span data-stu-id="badca-167">On the **Sales order lines** FastTab, select **Add line** to add another line to your sales order.</span></span> <span data-ttu-id="badca-168">この明細行で、次の値を設定します。</span><span class="sxs-lookup"><span data-stu-id="badca-168">On this line, set the following values:</span></span>

    - <span data-ttu-id="badca-169">**品目番号:** *A0002*</span><span class="sxs-lookup"><span data-stu-id="badca-169">**Item number:** *A0002*</span></span>
    - <span data-ttu-id="badca-170">**数量:** *2*</span><span class="sxs-lookup"><span data-stu-id="badca-170">**Quantity:** *2*</span></span>

1. <span data-ttu-id="badca-171">グリッドの上部にある**在庫**メニューで、**引当**を選択します。</span><span class="sxs-lookup"><span data-stu-id="badca-171">On the **Inventory** menu above the grid, select **Reservation**.</span></span>
1. <span data-ttu-id="badca-172">**引当** ページの、アクション ウィンドウで**ロットの引当**を選択して、在庫を引当てします。</span><span class="sxs-lookup"><span data-stu-id="badca-172">On the **Reservation** page, on the Action Pane, select **Reserve lot** to reserve the inventory.</span></span>
1. <span data-ttu-id="badca-173">ページを閉じます。</span><span class="sxs-lookup"><span data-stu-id="badca-173">Close the page.</span></span>
1. <span data-ttu-id="badca-174">アクション ウィンドウの**倉庫**タブで、**倉庫へのリリース**を選択します。</span><span class="sxs-lookup"><span data-stu-id="badca-174">On the Action Pane, on the **Warehouse** tab, select **Release to warehouse**.</span></span>
1. <span data-ttu-id="badca-175">このリリースに対して作成されたウェーブ ID と出荷 ID を示す情報のメッセージが表示されます。</span><span class="sxs-lookup"><span data-stu-id="badca-175">You receive informational messages that show the wave ID and shipment ID that were created from the release.</span></span> <span data-ttu-id="badca-176">ウェーブ ID をメモします。</span><span class="sxs-lookup"><span data-stu-id="badca-176">Make a note of the wave ID.</span></span>

### <a name="review-the-outbound-wave"></a><span data-ttu-id="badca-177">出荷のウェーブを確認する</span><span class="sxs-lookup"><span data-stu-id="badca-177">Review the outbound wave</span></span>

1. <span data-ttu-id="badca-178">**倉庫管理 \> 出庫ウェーブ \> 出荷ウェーブ \> すべてのウェーブ**の順に移動します。</span><span class="sxs-lookup"><span data-stu-id="badca-178">Go to **Warehouse management \> Outbound waves \> Shipment waves \> All waves**.</span></span>
1. <span data-ttu-id="badca-179">グリッドで、販売注文のリリースから作成されたウェーブ ID を検索します。</span><span class="sxs-lookup"><span data-stu-id="badca-179">In the grid, search for the wave ID that was created from the release of the sales order.</span></span>
1. <span data-ttu-id="badca-180">詳細情報を表示するウェーブ ID を選択します。</span><span class="sxs-lookup"><span data-stu-id="badca-180">Select the wave ID to view the details.</span></span>
1. <span data-ttu-id="badca-181">**ウェーブの明細** クイックタブで、販売注文の出荷 ID が表示されていることを確認します。</span><span class="sxs-lookup"><span data-stu-id="badca-181">On the **Wave lines** FastTab, make sure that a shipment ID is shown for the sales order.</span></span>

    > [!TIP]
    > <span data-ttu-id="badca-182">出荷ウェーブ テンプレートの設定で **倉庫へのリリース状態のウェーブを処理する**オプションが *いいえ* に設定されている場合は 、アクション ウィンドウの **ウェーブ**タブの **処理**を選択して手動で作業の作成処理をする必要があります。</span><span class="sxs-lookup"><span data-stu-id="badca-182">If the **Process wave at release to warehouse** option is set to *No* in the setup for the shipping wave template, you must manually process the wave by selecting **Process** from the **Wave** tab on the Action Pane to create work.</span></span>

1. <span data-ttu-id="badca-183">ウェーブが処理されたことを確認してください。</span><span class="sxs-lookup"><span data-stu-id="badca-183">Make sure that the wave has been processed.</span></span> <span data-ttu-id="badca-184">この処理では、必要となる作業が作成されます。</span><span class="sxs-lookup"><span data-stu-id="badca-184">This processing creates the required work.</span></span>

### <a name="view-work-details-and-change-the-work-pool"></a><span data-ttu-id="badca-185">作業の詳細を表示し、作業プールを変更します</span><span class="sxs-lookup"><span data-stu-id="badca-185">View work details and change the work pool</span></span>

<span data-ttu-id="badca-186">**作業の詳細** ページを使用して、作成された作業の表示や、作業プールを管理することができます。</span><span class="sxs-lookup"><span data-stu-id="badca-186">You can use the **Work details** page to view the work that was created and to manage the work pool.</span></span>

1. <span data-ttu-id="badca-187">**倉庫管理 \> 作業 \> 作業の詳細**の順に移動します。</span><span class="sxs-lookup"><span data-stu-id="badca-187">Go to **Warehouse management \> Work \> Work details**.</span></span>
1. <span data-ttu-id="badca-188">作成された作業の行を選択します。</span><span class="sxs-lookup"><span data-stu-id="badca-188">Select the row for the work that was just created.</span></span> <span data-ttu-id="badca-189">**注文番号** 列には販売注文番号が表示されます。</span><span class="sxs-lookup"><span data-stu-id="badca-189">The **Order number** column will show the sales order number.</span></span>

    <span data-ttu-id="badca-190">**作業プール ID** フィールドには、作業テンプレートで設定された作業プールの ID が設定されます。</span><span class="sxs-lookup"><span data-stu-id="badca-190">The **Work pool ID** field will be set to the work pool ID that was set up in the work template.</span></span>

    > [!TIP]
    > <span data-ttu-id="badca-191">**作業プール ID** フィールドが表示されない場合は、グリッドに列を追加し、ページを更新してください。</span><span class="sxs-lookup"><span data-stu-id="badca-191">If you don't see the **Work pool ID** field, add the column to the grid, and then refresh the page.</span></span>

1. <span data-ttu-id="badca-192">作業 ID に関連付けられている作業プールを変更するには、アクション ウィンドウの **作業** タブで、**作業プール ID の変更** を選択します。</span><span class="sxs-lookup"><span data-stu-id="badca-192">To change the work pool that is associated with the work ID, on the Action Pane, on the **Work** tab, select **Change Work pool ID**.</span></span>
1. <span data-ttu-id="badca-193">**パラメータ** クイックタブの **作業プールの変更** ダイアログ ボックス内の **作業プール ID**フィールドで、*CallCenter* を選択します。</span><span class="sxs-lookup"><span data-stu-id="badca-193">In the **Change work pool** dialog box, on the **Parameters** FastTab, in the **Work pool ID** field, select *CallCenter*.</span></span>
1. <span data-ttu-id="badca-194">**OK** を選択して変更を適用します。</span><span class="sxs-lookup"><span data-stu-id="badca-194">Select **OK** to apply your change.</span></span>
1. <span data-ttu-id="badca-195">**作業プール ID** フィールドの値が *CallCenter* に変更されていることを確認してください。</span><span class="sxs-lookup"><span data-stu-id="badca-195">Notice that the value of the **Work pool ID** field has now been changed to *CallCenter*.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="badca-196">**作業プールの変更** ダイアログ ボックスが表示された際に、既定で **作業プール ID** フィールドが空白になる場合があります。</span><span class="sxs-lookup"><span data-stu-id="badca-196">When the **Change work pool** dialog box appears, the **Work pool ID** field might be blank by default.</span></span> <span data-ttu-id="badca-197">このフィールドが空白になっている場合に **OK** を選択して変更を適用すると、作業プールが作業から完全に削除されます。</span><span class="sxs-lookup"><span data-stu-id="badca-197">If the field is blank when you select **OK** to apply changes, you will remove the work pool completely from the work.</span></span>
>
> <span data-ttu-id="badca-198">作業プールを切り替えるだけでなく、この手順を使用して、作業プールがない作業項目に作業プールを追加したり、作業プールがある作業項目から作業プールを削除したりすることもできます。</span><span class="sxs-lookup"><span data-stu-id="badca-198">In addition to switching work pools, you can use this procedure to add a work pool to any work item that doesn't have one, or to remove a work pool from any work item that does have one.</span></span>
