---
title: 倉庫のスロッティング
description: このトピックでは、倉庫のスロッティングについて説明します。 倉庫のスロッティングでは、注文済、予約済、またはリリース済のステータスである注文から、品目および測定単位別に需要を連結できます。 これにより、倉庫管理者は、注文を倉庫にリリースしてピッキング作業を作成する前に、ピッキング場所をインテリジェントに計画できます。
author: mirzaab
manager: tfehr
ms.date: 07/01/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: WHSInventFixedLocation, WHSSlotDemandLocated, WHSSlotDemand, WHSSlotUOMTier, WHSSlotTemplate, WHSLocDirHint, WHSLocDirTable
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: mirzaab
ms.search.validFrom: 2020-07-01
ms.dyn365.ops.version: Release 10.0.9
ms.openlocfilehash: ed9e6eae2ecc8de8d5eeef4699678e93dd74f193
ms.sourcegitcommit: a36a4f9915ae3eb36bf8220111cf1486387713d9
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 10/16/2020
ms.locfileid: "4017417"
---
# <a name="warehouse-slotting"></a><span data-ttu-id="50c96-105">倉庫のスロッティング</span><span class="sxs-lookup"><span data-stu-id="50c96-105">Warehouse slotting</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="50c96-106">倉庫のスロッティングでは、 *注文済* 、 *予約済* 、または *リリース済* のステータスである注文から、品目および測定単位別に需要を連結できます。</span><span class="sxs-lookup"><span data-stu-id="50c96-106">Warehouse slotting lets you consolidate demand by item and unit of measure from orders that have a status of *Ordered* , *Reserved* , or *Released*.</span></span> <span data-ttu-id="50c96-107">生成された需要は、数量、単位、物理的分析コード、固定の場所などに基づいてピッキングに使用される場所を適用できます。</span><span class="sxs-lookup"><span data-stu-id="50c96-107">Generated demand can then be applied to locations that will be used for picking, based on quantity, unit, physical dimensions, fixed locations, and more.</span></span> <span data-ttu-id="50c96-108">スロッティングの計画が確立された後に、補充作業を作成して、各場所に適切な量の在庫を取り込むことができます。</span><span class="sxs-lookup"><span data-stu-id="50c96-108">After the slotting plan has been established, replenishment work can be created to bring the appropriate amount of inventory to each location.</span></span>

<span data-ttu-id="50c96-109">この機能により、倉庫管理者は、注文を倉庫にリリースしてピッキング作業を作成する前に、ピッキング場所をインテリジェントに計画できます。</span><span class="sxs-lookup"><span data-stu-id="50c96-109">This functionality helps warehouse managers intelligently plan picking locations before they release orders to the warehouse and create picking work.</span></span>

## <a name="turn-on-the-warehouse-slotting-feature"></a><span data-ttu-id="50c96-110">倉庫のスロッティング機能をオンにします</span><span class="sxs-lookup"><span data-stu-id="50c96-110">Turn on the warehouse slotting feature</span></span>

<span data-ttu-id="50c96-111">この機能を使用するには、システム上で有効にする必要があります。</span><span class="sxs-lookup"><span data-stu-id="50c96-111">Before you can use this feature, it must be turned on in your system.</span></span> <span data-ttu-id="50c96-112">管理者は、[機能の管理](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md)設定を使用して、機能の状態を確認し、必要に応じて有効にすることができます。</span><span class="sxs-lookup"><span data-stu-id="50c96-112">Admins can use the [feature management](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) settings to check the status of the feature and turn it on if it's required.</span></span> <span data-ttu-id="50c96-113">**機能管理** ワークスペースで、この機能は次のようにリストされています。</span><span class="sxs-lookup"><span data-stu-id="50c96-113">In the **Feature management** workspace, the feature is listed in the following way:</span></span>

- <span data-ttu-id="50c96-114">**モジュール:** *倉庫管理*</span><span class="sxs-lookup"><span data-stu-id="50c96-114">**Module:** *Warehouse management*</span></span>
- <span data-ttu-id="50c96-115">**機能名:** *倉庫スロッティング機能*</span><span class="sxs-lookup"><span data-stu-id="50c96-115">**Feature name:** *Warehouse slotting feature*</span></span>

## <a name="set-up-warehouse-slotting"></a><span data-ttu-id="50c96-116">倉庫のスロッティングの設定</span><span class="sxs-lookup"><span data-stu-id="50c96-116">Set up warehouse slotting</span></span>

<span data-ttu-id="50c96-117">倉庫のスロッティングを使用するには、次の要素をシステムに設定をする必要があります。</span><span class="sxs-lookup"><span data-stu-id="50c96-117">To use warehouse slotting, you must set up the following elements in your system.</span></span>

### <a name="create-unit-of-measure-tiers-for-slotting"></a><a name="unit-tiers"></a><span data-ttu-id="50c96-118">スロッティングの測定単位層の作成</span><span class="sxs-lookup"><span data-stu-id="50c96-118">Create unit-of-measure tiers for slotting</span></span>

<span data-ttu-id="50c96-119">測定単位層は、スロッティング目的で複数の測定単位をグループ化できます。</span><span class="sxs-lookup"><span data-stu-id="50c96-119">Unit-of-measure tiers enable multiple units of measure to be grouped together for the purposes of slotting.</span></span> <span data-ttu-id="50c96-120">たとえば、同じボックスのピッキング エリアから複数のボックスがすべてピッキングされた場合、すべてのサイズに対して 1 つの層を作成することができます。</span><span class="sxs-lookup"><span data-stu-id="50c96-120">For example, if multiple sizes of boxes are all picked from the same box picking area, one tier can be created for all the sizes.</span></span> <span data-ttu-id="50c96-121">**各層に含まれる測定単位ごとに明細行を作成する必要があります。**</span><span class="sxs-lookup"><span data-stu-id="50c96-121">**A line must be created for each unit of measure that should be part of the tier.**</span></span>

1. <span data-ttu-id="50c96-122">**倉庫管理 \> 設定 \> 補充 \> 測定単位層のスロッティング** に移動します。</span><span class="sxs-lookup"><span data-stu-id="50c96-122">Go to **Warehouse management \> Setup \> Replenishment \> Slotting unit of measure tiers**.</span></span>
1. <span data-ttu-id="50c96-123">**新規** を選択します。</span><span class="sxs-lookup"><span data-stu-id="50c96-123">Select **New**.</span></span>
1. <span data-ttu-id="50c96-124">ヘッダーで、次の値を設定します。</span><span class="sxs-lookup"><span data-stu-id="50c96-124">In the header, set the following values:</span></span>

    - <span data-ttu-id="50c96-125">**測定単位層:** *EaBoxPl*</span><span class="sxs-lookup"><span data-stu-id="50c96-125">**Unit of measure tier:** *EaBoxPl*</span></span>
    - <span data-ttu-id="50c96-126">**説明:** *各ボックス パレット*</span><span class="sxs-lookup"><span data-stu-id="50c96-126">**Description:** *Each box pallet*</span></span>

1. <span data-ttu-id="50c96-127">**保存** を選択します。</span><span class="sxs-lookup"><span data-stu-id="50c96-127">Select **Save**.</span></span>
1. <span data-ttu-id="50c96-128">**測定単位** クイック タブで、 **新規** を選択してグリッドに行を追加します。</span><span class="sxs-lookup"><span data-stu-id="50c96-128">On the **Units of measure** FastTab, select **New** to add a line to the grid.</span></span>
1. <span data-ttu-id="50c96-129">新しい明細行で、次の値を設定します。</span><span class="sxs-lookup"><span data-stu-id="50c96-129">On the new line, set the following values:</span></span>

    - <span data-ttu-id="50c96-130">**単位:** *ボックス*</span><span class="sxs-lookup"><span data-stu-id="50c96-130">**Unit:** *Box*</span></span>
    - <span data-ttu-id="50c96-131">**説明:** このフィールドは空白のままにしておきます。</span><span class="sxs-lookup"><span data-stu-id="50c96-131">**Description:** Leave this field blank.</span></span> <span data-ttu-id="50c96-132">変更を保存すると、自動的に入力されます。</span><span class="sxs-lookup"><span data-stu-id="50c96-132">It will be filled in automatically when you save your changes.</span></span>
    - <span data-ttu-id="50c96-133">**単位クラス:** *数量*</span><span class="sxs-lookup"><span data-stu-id="50c96-133">**Unit class:** *Quantity*</span></span>

1. <span data-ttu-id="50c96-134">**新規** を選択して、グリッドの 2 行目を追加します。</span><span class="sxs-lookup"><span data-stu-id="50c96-134">Select **New** to add a second line to the grid.</span></span>
1. <span data-ttu-id="50c96-135">新しい明細行で、次の値を設定します。</span><span class="sxs-lookup"><span data-stu-id="50c96-135">On the new line, set the following values:</span></span>

    - <span data-ttu-id="50c96-136">**単位:** *個*</span><span class="sxs-lookup"><span data-stu-id="50c96-136">**Unit:** *ea*</span></span>
    - <span data-ttu-id="50c96-137">**説明:** このフィールドは空白のままにしておきます。</span><span class="sxs-lookup"><span data-stu-id="50c96-137">**Description:** Leave this field blank.</span></span> <span data-ttu-id="50c96-138">変更を保存すると、自動的に入力されます。</span><span class="sxs-lookup"><span data-stu-id="50c96-138">It will be filled in automatically when you save your changes.</span></span>
    - <span data-ttu-id="50c96-139">**単位クラス:** *数量*</span><span class="sxs-lookup"><span data-stu-id="50c96-139">**Unit class:** *Quantity*</span></span>

1. <span data-ttu-id="50c96-140">**新規** を選択して、グリッドの 3 行目を追加します。</span><span class="sxs-lookup"><span data-stu-id="50c96-140">Select **New** to add a third line to the grid.</span></span>
1. <span data-ttu-id="50c96-141">新しい明細行で、次の値を設定します。</span><span class="sxs-lookup"><span data-stu-id="50c96-141">On the new line, set the following values:</span></span>

    - <span data-ttu-id="50c96-142">**ユニット:** *PL*</span><span class="sxs-lookup"><span data-stu-id="50c96-142">**Unit:** *PL*</span></span>
    - <span data-ttu-id="50c96-143">**説明:** このフィールドは空白のままにしておきます。</span><span class="sxs-lookup"><span data-stu-id="50c96-143">**Description:** Leave this field blank.</span></span> <span data-ttu-id="50c96-144">変更を保存すると、自動的に入力されます。</span><span class="sxs-lookup"><span data-stu-id="50c96-144">It will be filled in automatically when you save your changes.</span></span>
    - <span data-ttu-id="50c96-145">**単位クラス:** *数量*</span><span class="sxs-lookup"><span data-stu-id="50c96-145">**Unit class:** *Quantity*</span></span>

1. <span data-ttu-id="50c96-146">**保存** を選択して階層に保存します。</span><span class="sxs-lookup"><span data-stu-id="50c96-146">Select **Save** to save the tier.</span></span>

### <a name="create-a-directive-code-for-slotting"></a><span data-ttu-id="50c96-147">スロッティング用のディレクティブ コードの作成</span><span class="sxs-lookup"><span data-stu-id="50c96-147">Create a directive code for slotting</span></span>

<span data-ttu-id="50c96-148">テンプレートに関連付けるディレクティブ コードを選択する必要があります。</span><span class="sxs-lookup"><span data-stu-id="50c96-148">You must select the directive code that should be associated with a template.</span></span>

1. <span data-ttu-id="50c96-149">**倉庫管理 \> 設定 \> ディレクティブ コード** に移動します。</span><span class="sxs-lookup"><span data-stu-id="50c96-149">Go to **Warehouse management \> Setup \> Directive codes**.</span></span>
1. <span data-ttu-id="50c96-150">アクション ウィンドウで、 **新規** を選択します。</span><span class="sxs-lookup"><span data-stu-id="50c96-150">On the Action Pane, select **New**.</span></span>
1. <span data-ttu-id="50c96-151">**ディレクティブ コード** フィールドに、 *スロッティング* と入力します。</span><span class="sxs-lookup"><span data-stu-id="50c96-151">In the **Directive code** field, enter *Slotting*.</span></span>
1. <span data-ttu-id="50c96-152">**ディレクティブの説明** フィールドに、 *スロッティング* と入力します。</span><span class="sxs-lookup"><span data-stu-id="50c96-152">In the **Directive description** field, enter *Slotting*.</span></span>

### <a name="set-up-slotting-templates"></a><span data-ttu-id="50c96-153">スロッティング テンプレートの設定</span><span class="sxs-lookup"><span data-stu-id="50c96-153">Set up slotting templates</span></span>

<span data-ttu-id="50c96-154">各スロッティング テンプレートは、在庫を特定の倉庫の場所に割り当てる方法を制御します。</span><span class="sxs-lookup"><span data-stu-id="50c96-154">Each slotting template controls how inventory is assigned to locations for a specific warehouse.</span></span> <span data-ttu-id="50c96-155">各テンプレートには、スロッティングの仕様ごとに 1 行を含める必要があります。</span><span class="sxs-lookup"><span data-stu-id="50c96-155">Each template must include a line for each slotting specification.</span></span> <span data-ttu-id="50c96-156">スロッティング テンプレートを設定するには、このセクションの手順を使用します。</span><span class="sxs-lookup"><span data-stu-id="50c96-156">Use the procedures in this section to set up slotting templates.</span></span>

1. <span data-ttu-id="50c96-157">**倉庫管理 \> 設定 \> 補充 \> スロッティング テンプレート** の順に移動します。</span><span class="sxs-lookup"><span data-stu-id="50c96-157">Go to **Warehouse management \> Setup \> Replenishment \> Slotting templates**.</span></span>
1. <span data-ttu-id="50c96-158">**新規作成** を選択してテンプレートを作成します。</span><span class="sxs-lookup"><span data-stu-id="50c96-158">Select **New** to create a template.</span></span>

<span data-ttu-id="50c96-159">次に、以下のサブセクションで説明するように、テンプレート ヘッダー、スロッティングの仕様、および場所ディレクティブを設定する必要があります。</span><span class="sxs-lookup"><span data-stu-id="50c96-159">Next, you must set up the template header, slotting specifications, and location directives, as explained in the following subsections.</span></span>

#### <a name="set-up-a-slotting-template-header"></a><span data-ttu-id="50c96-160">スロッティングのテンプレート ヘッダーの設定</span><span class="sxs-lookup"><span data-stu-id="50c96-160">Set up a slotting template header</span></span>

1. <span data-ttu-id="50c96-161">テンプレートのヘッダーで、次の値を設定します。</span><span class="sxs-lookup"><span data-stu-id="50c96-161">In the header for the template, set the following values:</span></span>

    - <span data-ttu-id="50c96-162">**スロッティング テンプレート:** _61_</span><span class="sxs-lookup"><span data-stu-id="50c96-162">**Slotting template:** _61_</span></span>
    - <span data-ttu-id="50c96-163">**説明:** _61_</span><span class="sxs-lookup"><span data-stu-id="50c96-163">**Description:** _61_</span></span>
    - <span data-ttu-id="50c96-164">**需要タイプ:** *販売注文*</span><span class="sxs-lookup"><span data-stu-id="50c96-164">**Demand type:** *Sales order*</span></span>

        <span data-ttu-id="50c96-165">現在、 *販売注文* はサポートされている唯一の需要タイプです。</span><span class="sxs-lookup"><span data-stu-id="50c96-165">Currently, *Sales order* is the only demand type that is supported.</span></span>

    - <span data-ttu-id="50c96-166">**需要戦略:** _注文済_</span><span class="sxs-lookup"><span data-stu-id="50c96-166">**Demand strategy:** _Ordered_</span></span>

        <span data-ttu-id="50c96-167">以下の値は、このフィールドで使用できます。</span><span class="sxs-lookup"><span data-stu-id="50c96-167">The following values are available in this field:</span></span>

        - <span data-ttu-id="50c96-168">**注文済** – 販売注文の注文済数量すべてを需要と見なされます。</span><span class="sxs-lookup"><span data-stu-id="50c96-168">**Ordered** – The full ordered quantity on the sales order should be considered demand.</span></span>
        - <span data-ttu-id="50c96-169">**予約済** – 予約済 (現物と注文済の両方) である販売注文明細行数量のみを要求と見なされます。</span><span class="sxs-lookup"><span data-stu-id="50c96-169">**Reserved** – Only the sales order line quantities that are reserved (physical and ordered) should be considered demand.</span></span>

    - <span data-ttu-id="50c96-170">**倉庫:** _61_</span><span class="sxs-lookup"><span data-stu-id="50c96-170">**Warehouse:** _61_</span></span>
    - <span data-ttu-id="50c96-171">**ウェーブ要素に未引当数量の使用を許可する:** _はい_</span><span class="sxs-lookup"><span data-stu-id="50c96-171">**Allow wave demand to use unreserved quantities:** _Yes_</span></span>

<span data-ttu-id="50c96-172">評価する需要の範囲を絞り込むためのクエリを指定することもできます。</span><span class="sxs-lookup"><span data-stu-id="50c96-172">You can also specify a query to narrow the scope of the demand that is evaluated.</span></span>

#### <a name="set-up-slotting-specifications-for-each-template"></a><span data-ttu-id="50c96-173">スロッティングの仕様の各テンプレートを設定します</span><span class="sxs-lookup"><span data-stu-id="50c96-173">Set up slotting specifications for each template</span></span>

<span data-ttu-id="50c96-174">作成するテンプレートごとに、次の手順に従ってスロッティングの仕様ごとに行を追加します。</span><span class="sxs-lookup"><span data-stu-id="50c96-174">For each template that you create, follow these steps to add a line for each slotting specification.</span></span>

1. <span data-ttu-id="50c96-175">**スロッティングのテンプレート詳細** クイック タブで、 **新規** を選択してテンプレート行を作成します。</span><span class="sxs-lookup"><span data-stu-id="50c96-175">On the **Slotting template details** FastTab, select **New** to create a template line.</span></span>
1. <span data-ttu-id="50c96-176">新しい明細行で、次の値を設定します。</span><span class="sxs-lookup"><span data-stu-id="50c96-176">On the new line, set the following values:</span></span>

    - <span data-ttu-id="50c96-177">**シーケンス:** _1_</span><span class="sxs-lookup"><span data-stu-id="50c96-177">**Sequence:** _1_</span></span>
    - <span data-ttu-id="50c96-178">**説明:** _固定の場所_</span><span class="sxs-lookup"><span data-stu-id="50c96-178">**Description:** _Fixed location_</span></span>
    - <span data-ttu-id="50c96-179">**最小数量:** _1_</span><span class="sxs-lookup"><span data-stu-id="50c96-179">**Minimum quantity:** _1_</span></span>

        <span data-ttu-id="50c96-180">このフィールドでは、明細行に必要な最小需要数量を定義します。</span><span class="sxs-lookup"><span data-stu-id="50c96-180">This field defines the minimum quantity of demand that is required for the line.</span></span>

    - <span data-ttu-id="50c96-181">**最大数量:** _1000000_</span><span class="sxs-lookup"><span data-stu-id="50c96-181">**Maximum quantity:** _1000000_</span></span>

        <span data-ttu-id="50c96-182">このフィールドでは、明細行に有効な最大需要数量を定義します。</span><span class="sxs-lookup"><span data-stu-id="50c96-182">This field defines the maximum quantity of demand that is valid for the line.</span></span>

    - <span data-ttu-id="50c96-183">**ユニット:** このフィールドは空白のままにします。</span><span class="sxs-lookup"><span data-stu-id="50c96-183">**Unit:** Leave this field blank.</span></span>

        <span data-ttu-id="50c96-184">このフィールドは、最小数量と最大数量が参照する測定単位を定義します。</span><span class="sxs-lookup"><span data-stu-id="50c96-184">This field defines the unit of measure that the minimum and maximum quantities refer to.</span></span>

    - <span data-ttu-id="50c96-185">**測定単位層:** _EaBoxPl_</span><span class="sxs-lookup"><span data-stu-id="50c96-185">**Unit of Measure Tier:** _EaBoxPl_</span></span>

        <span data-ttu-id="50c96-186">このフィールドでは、明細行有効な測定単位を定義します。</span><span class="sxs-lookup"><span data-stu-id="50c96-186">This field defines the units of measure of demand that are valid for the line.</span></span> <span data-ttu-id="50c96-187">(詳細については、このトピックの前の[スロッティングの測定単位層の設定](#unit-tiers) セクションを参照してください。)</span><span class="sxs-lookup"><span data-stu-id="50c96-187">(For more information, see the [Set up unit-of-measure tiers for slotting](#unit-tiers) section earlier in this topic.)</span></span>

    - <span data-ttu-id="50c96-188">**スロット基準の割り当て:** _数量を考慮_</span><span class="sxs-lookup"><span data-stu-id="50c96-188">**Assign slot criteria:** _Consider qty_</span></span>

        <span data-ttu-id="50c96-189">以下の値は、このフィールドで使用できます。</span><span class="sxs-lookup"><span data-stu-id="50c96-189">The following values are available in this field:</span></span>

        - <span data-ttu-id="50c96-190">**空白であると仮定** – このシステムでは、ピッキングエリア内のすべての場所が空であると想定し、在庫の場所を確認しないようにします。</span><span class="sxs-lookup"><span data-stu-id="50c96-190">**Assume empty** – This system should assume that all locations in the picking area are empty and should not check those locations for inventory.</span></span>
        - <span data-ttu-id="50c96-191">**数量を考慮** – このシステムでは、ピッキングエリア内の場所で在庫を確認し、空でない場所はスキップするようにします。</span><span class="sxs-lookup"><span data-stu-id="50c96-191">**Consider qty** – The system should check the locations in the picking area for inventory and should skip any locations that aren't empty.</span></span>

    - <span data-ttu-id="50c96-192">**ディレクティブ コード:** _スロッティング_</span><span class="sxs-lookup"><span data-stu-id="50c96-192">**Directive code:** _Slotting_</span></span>

        <span data-ttu-id="50c96-193">このフィールドでは、補充作業のピッキング場所を検索する際に使用される場所のディレクティブを定義します。</span><span class="sxs-lookup"><span data-stu-id="50c96-193">This field defines the location directive that is used to find the picking location of the replenishment work.</span></span>

    - <span data-ttu-id="50c96-194">**オーバーフローの場所:** このフィールドは空白のままにします。</span><span class="sxs-lookup"><span data-stu-id="50c96-194">**Overflow location:** Leave this field blank.</span></span>

        <span data-ttu-id="50c96-195">このフィールドは、明細行が処理されたときに在庫が数量の場所が検出されない場合に、在庫が置かれる場所を定義します。</span><span class="sxs-lookup"><span data-stu-id="50c96-195">This field defines the location that inventory that is put to if a location can't be found for the quantity when the line is processed.</span></span>

    - <span data-ttu-id="50c96-196">**停止の許可:** _はい_</span><span class="sxs-lookup"><span data-stu-id="50c96-196">**Allow let up:** _Yes_</span></span>

        <span data-ttu-id="50c96-197">このオプションを *はい* に設定すると、スロット化できない需要がある場合、在庫があっても、スロット化されていない場所から在庫を取り出す振替作業が作成されます。</span><span class="sxs-lookup"><span data-stu-id="50c96-197">When this option is set to *Yes* , if any demand can't be slotted, movement work will be created to take inventory out of locations where there is inventory, but where nothing was slotted.</span></span> <span data-ttu-id="50c96-198">その後、テンプレートが再度実行されます。</span><span class="sxs-lookup"><span data-stu-id="50c96-198">The template is then run again.</span></span> <span data-ttu-id="50c96-199">今回は、場所の在庫が無視されます。</span><span class="sxs-lookup"><span data-stu-id="50c96-199">This time, it ignores the inventory in the locations.</span></span> <span data-ttu-id="50c96-200">この機能は、 **スロット基準の割り当て** フィールドが _数量を考慮_ に設定されている場合に最も有効です。</span><span class="sxs-lookup"><span data-stu-id="50c96-200">This functionality works best when the **Assign slot criteria** field is set to _Consider qty_.</span></span>

    - <span data-ttu-id="50c96-201">**固定の場所の使用:** _製品の固定された場所のみ_</span><span class="sxs-lookup"><span data-stu-id="50c96-201">**Fixed location usage:** _Only fixed locations for the product_</span></span>

        <span data-ttu-id="50c96-202">以下の値は、このフィールドで使用できます。</span><span class="sxs-lookup"><span data-stu-id="50c96-202">The following values are available in this field:</span></span>

        - <span data-ttu-id="50c96-203">**固定の場所および固定されていない場所** –システムは、固定場所のみを使用するように制限することはできません。</span><span class="sxs-lookup"><span data-stu-id="50c96-203">**Fixed and non-fixed locations** – The system should not be limited to using only fixed locations.</span></span>
        - <span data-ttu-id="50c96-204">**製品の固定された場所のみ** – システムは、製品の固定された場所である場所に対してのみスロットを使用する必要があります。</span><span class="sxs-lookup"><span data-stu-id="50c96-204">**Only fixed locations for the product** – The system should slot only to locations that are fixed locations for the product.</span></span>
        - <span data-ttu-id="50c96-205">**製品バリアントの固定された場所のみ** – システムは、製品バリアントの固定された場所である場所に対してのみスロットを使用する必要があります。</span><span class="sxs-lookup"><span data-stu-id="50c96-205">**Only fixed locations for the product variant** – The system should slot only to locations that are fixed locations for the product variant.</span></span>

1. <span data-ttu-id="50c96-206">**保存** を選択します。</span><span class="sxs-lookup"><span data-stu-id="50c96-206">Select **Save**.</span></span>
1. <span data-ttu-id="50c96-207">**新規** を選択して、テンプレートの 2 行目を追加します。</span><span class="sxs-lookup"><span data-stu-id="50c96-207">Select **New** to create a second template line.</span></span>
1. <span data-ttu-id="50c96-208">新しい明細行で、次の値を設定します。</span><span class="sxs-lookup"><span data-stu-id="50c96-208">On the new line, set the following values:</span></span>

    - <span data-ttu-id="50c96-209">**シーケンス:** _2_</span><span class="sxs-lookup"><span data-stu-id="50c96-209">**Sequence:** _2_</span></span>
    - <span data-ttu-id="50c96-210">**説明:** _その他_</span><span class="sxs-lookup"><span data-stu-id="50c96-210">**Description:** _Other_</span></span>
    - <span data-ttu-id="50c96-211">**最小数量:** _1_</span><span class="sxs-lookup"><span data-stu-id="50c96-211">**Minimum Qty:** _1_</span></span>
    - <span data-ttu-id="50c96-212">**最大数量:** _1000000_</span><span class="sxs-lookup"><span data-stu-id="50c96-212">**Maximum Qty:** _1000000_</span></span>
    - <span data-ttu-id="50c96-213">**ユニット:** このフィールドは空白のままにします。</span><span class="sxs-lookup"><span data-stu-id="50c96-213">**Unit:** Leave this field blank.</span></span>
    - <span data-ttu-id="50c96-214">**測定単位層:** _EaBoxPl_</span><span class="sxs-lookup"><span data-stu-id="50c96-214">**Unit of measure tier:** _EaBoxPl_</span></span>
    - <span data-ttu-id="50c96-215">**スロット基準の割り当て:** _数量を考慮_</span><span class="sxs-lookup"><span data-stu-id="50c96-215">**Assign slot criteria:** _Consider qty_</span></span>
    - <span data-ttu-id="50c96-216">**ディレクティブ コード:** _スロッティング_</span><span class="sxs-lookup"><span data-stu-id="50c96-216">**Directive code:** _Slotting_</span></span>
    - <span data-ttu-id="50c96-217">**オーバーフローの場所:** このフィールドは空白のままにします。</span><span class="sxs-lookup"><span data-stu-id="50c96-217">**Overflow location:** Leave this field blank.</span></span>
    - <span data-ttu-id="50c96-218">**停止の許可:** _はい_</span><span class="sxs-lookup"><span data-stu-id="50c96-218">**Allow let up:** _Yes_</span></span>
    - <span data-ttu-id="50c96-219">**固定の場所の使用:** _固定の場所および固定されていない場所_</span><span class="sxs-lookup"><span data-stu-id="50c96-219">**Use fixed locations:** _Fixed and non-fixed locations_</span></span>

    <span data-ttu-id="50c96-220">2 行目のクエリでは、この行の需要をスロット化できる場所を決定するために使用される基準を指定できるようになりました。</span><span class="sxs-lookup"><span data-stu-id="50c96-220">In the query for the second line, you will now specify the criteria that are used to determine what locations the demand for that line can be slotted to.</span></span>

1. <span data-ttu-id="50c96-221">**シーケンス** フィールドが *2* に設定されている行を選択します。</span><span class="sxs-lookup"><span data-stu-id="50c96-221">Select the line where the **Sequence** field is set to *2*.</span></span>
1. <span data-ttu-id="50c96-222">**クエリの編集** を選択します。</span><span class="sxs-lookup"><span data-stu-id="50c96-222">Select **Edit query**.</span></span>
1. <span data-ttu-id="50c96-223">**範囲** タブで、 **追加** を選択してグリッドに新しい行を追加します。</span><span class="sxs-lookup"><span data-stu-id="50c96-223">On the **Range** tab, select **Add** to add a line to the grid.</span></span>
1. <span data-ttu-id="50c96-224">新しい明細行で、次の値を設定します。</span><span class="sxs-lookup"><span data-stu-id="50c96-224">On the new line, set the following values:</span></span>

    - <span data-ttu-id="50c96-225">**テーブル:** *場所*</span><span class="sxs-lookup"><span data-stu-id="50c96-225">**Table:** *Locations*</span></span>
    - <span data-ttu-id="50c96-226">**派生テーブル:** *場所*</span><span class="sxs-lookup"><span data-stu-id="50c96-226">**Derived table:** *Locations*</span></span>
    - <span data-ttu-id="50c96-227">\**フィールド:\*\*\*場所のプロファイル ID*</span><span class="sxs-lookup"><span data-stu-id="50c96-227">**Field:** *Location profile ID*</span></span>
    - <span data-ttu-id="50c96-228">**基準:** *Pick-06* (フィールドでダブル プラス記号 \[**++**\] を選択して一覧を展開し、 *Pick-06* - *ピッキング サイト 6* を選択します。)</span><span class="sxs-lookup"><span data-stu-id="50c96-228">**Criteria:** *Pick-06* (Select the double plus sign \[**++**\] in the field to expand the list, and then select *Pick-06* - *Picking Site 6*.)</span></span>

1. <span data-ttu-id="50c96-229">**OK** を選択します。</span><span class="sxs-lookup"><span data-stu-id="50c96-229">Select **OK**.</span></span>

#### <a name="set-up-location-directives"></a><span data-ttu-id="50c96-230">場所ディレクティブを設定します</span><span class="sxs-lookup"><span data-stu-id="50c96-230">Set up location directives</span></span>

<span data-ttu-id="50c96-231">スロッティング ピックをサポートするには、少なくとも 1 つの場所のディレクティブを設定する必要があります。</span><span class="sxs-lookup"><span data-stu-id="50c96-231">At least one location directive must be set up to support slotting picks.</span></span> <span data-ttu-id="50c96-232">スロッティング ピックの新しい *補充場所のディレクティブ* を設定するには、このセクションの手順を使用します。</span><span class="sxs-lookup"><span data-stu-id="50c96-232">Use the procedures in this section to set up a new *replenishment location directive* for slotting picks.</span></span>

1. <span data-ttu-id="50c96-233">**倉庫管理 \> 設定 \> 場所のディレクティブ** に移動します。</span><span class="sxs-lookup"><span data-stu-id="50c96-233">Go to **Warehouse management \> Setup \> Location directives**.</span></span>
1. <span data-ttu-id="50c96-234">左ウィンドウで、 **作業指示タイプ** フィールドを *補充* に設定します。</span><span class="sxs-lookup"><span data-stu-id="50c96-234">In the left pane, in the **Work order type** field, select *Replenishment*.</span></span>
1. <span data-ttu-id="50c96-235">アクション ウィンドウで、 **新規** を選択します。</span><span class="sxs-lookup"><span data-stu-id="50c96-235">On the Action Pane, select **New**.</span></span>
1. <span data-ttu-id="50c96-236">新しい場所のヘッダーで、 **名前** フィールドに *61 スロッティング ピック* と入力します。</span><span class="sxs-lookup"><span data-stu-id="50c96-236">In the header for the new location directive, in the **Name** field, enter *61 Slotting pick*.</span></span>

##### <a name="configure-the-location-directives-fasttab"></a><span data-ttu-id="50c96-237">場所のディレクティブ クイック タブのコンフィギュレーション</span><span class="sxs-lookup"><span data-stu-id="50c96-237">Configure the Location directives FastTab</span></span>

1. <span data-ttu-id="50c96-238">**場所のディレクティブ** クイック タブで、次の値を設定します。</span><span class="sxs-lookup"><span data-stu-id="50c96-238">On the **Location directives** FastTab, set the following values.</span></span> <span data-ttu-id="50c96-239">他のすべてのフィールドの既定値を受け入れます。</span><span class="sxs-lookup"><span data-stu-id="50c96-239">Accept the default values for all other fields.</span></span>

    - <span data-ttu-id="50c96-240">**作業タイプ:** _ピッキング_</span><span class="sxs-lookup"><span data-stu-id="50c96-240">**Work type:** _Pick_</span></span>
    - <span data-ttu-id="50c96-241">**サイト:** _6_</span><span class="sxs-lookup"><span data-stu-id="50c96-241">**Site:** _6_</span></span>
    - <span data-ttu-id="50c96-242">**倉庫:** _61_</span><span class="sxs-lookup"><span data-stu-id="50c96-242">**Warehouse:** _61_</span></span>
    - <span data-ttu-id="50c96-243">**ディレクティブ コード:** _スロッティング_</span><span class="sxs-lookup"><span data-stu-id="50c96-243">**Directive code:** _Slotting_</span></span>

1. <span data-ttu-id="50c96-244">**保存** を選択して、 **明細行** クイック タブを使用できるようにします。</span><span class="sxs-lookup"><span data-stu-id="50c96-244">Select **Save** to make the **Lines** FastTab available.</span></span>

##### <a name="configure-the-lines-fasttab"></a><span data-ttu-id="50c96-245">明細行クイック タブのコンフィギュレーション</span><span class="sxs-lookup"><span data-stu-id="50c96-245">Configure the Lines FastTab</span></span>

1. <span data-ttu-id="50c96-246">**明細行** クイック タブで、 **新規** をクリックして明細行を作成します。</span><span class="sxs-lookup"><span data-stu-id="50c96-246">On the **Lines** FastTab, select **New** to create a line.</span></span>
1. <span data-ttu-id="50c96-247">新しい行で、次の値を設定します。</span><span class="sxs-lookup"><span data-stu-id="50c96-247">On the new line, set the following values.</span></span> <span data-ttu-id="50c96-248">他のすべてのフィールドの既定値を受け入れます。</span><span class="sxs-lookup"><span data-stu-id="50c96-248">Accept the default values for all other fields.</span></span>

    - <span data-ttu-id="50c96-249">**開始数量:** _0_</span><span class="sxs-lookup"><span data-stu-id="50c96-249">**From quantity:** _0_</span></span>
    - <span data-ttu-id="50c96-250">**上限数量:** _1000000_</span><span class="sxs-lookup"><span data-stu-id="50c96-250">**To quantity:** _1000000_</span></span>

1. <span data-ttu-id="50c96-251">**保存** を選択して、 **場所ディレクティブ アクション** クイック タブを使用できるようにします。</span><span class="sxs-lookup"><span data-stu-id="50c96-251">Select **Save** to make the **Location Directive Actions** FastTab available.</span></span>

##### <a name="configure-the-location-directive-actions-fasttab"></a><span data-ttu-id="50c96-252">場所ディレクティブ アクション クイック タブのコンフィギュレーション</span><span class="sxs-lookup"><span data-stu-id="50c96-252">Configure the Location Directive Actions FastTab</span></span>

1. <span data-ttu-id="50c96-253">**場所ディレクティブ アクション** クイック タブで、 **新規** を選択して明細行を作成します。</span><span class="sxs-lookup"><span data-stu-id="50c96-253">On the **Location Directive Actions** FastTab, select **New** to create a line.</span></span>
1. <span data-ttu-id="50c96-254">新しい行で、次の値を設定します。</span><span class="sxs-lookup"><span data-stu-id="50c96-254">On the new line, set the following values.</span></span> <span data-ttu-id="50c96-255">他のすべてのフィールドの既定値を受け入れます。</span><span class="sxs-lookup"><span data-stu-id="50c96-255">Accept the default values for all other fields.</span></span>

    - <span data-ttu-id="50c96-256">**名前:** _バルク_</span><span class="sxs-lookup"><span data-stu-id="50c96-256">**Name:** _Bulk_</span></span>
    - <span data-ttu-id="50c96-257">**戦略:** _なし_</span><span class="sxs-lookup"><span data-stu-id="50c96-257">**Strategy:** _None_</span></span>

1. <span data-ttu-id="50c96-258">**保存** を選択すると、 **クエリの編集** ボタンが使用できるようになります。</span><span class="sxs-lookup"><span data-stu-id="50c96-258">Select **Save** to make the **Edit query** button available.</span></span>

##### <a name="edit-the-query"></a><span data-ttu-id="50c96-259">クエリを編集します</span><span class="sxs-lookup"><span data-stu-id="50c96-259">Edit the query</span></span>

1. <span data-ttu-id="50c96-260">**場所ディレクティブ アクション** クイック タブで、 **クエリの編集** を選択します。</span><span class="sxs-lookup"><span data-stu-id="50c96-260">On the **Location Directive Actions** FastTab, select **Edit query**.</span></span>
1. <span data-ttu-id="50c96-261">**範囲** タブで、 **追加** を選択してグリッドに新しい行を追加します。</span><span class="sxs-lookup"><span data-stu-id="50c96-261">On the **Range** tab, select **Add** to add a line to the grid.</span></span>
1. <span data-ttu-id="50c96-262">新しい明細行で、次の値を設定します。</span><span class="sxs-lookup"><span data-stu-id="50c96-262">On the new line, set the following values:</span></span>

    - <span data-ttu-id="50c96-263">**テーブル:** *場所*</span><span class="sxs-lookup"><span data-stu-id="50c96-263">**Table:** *Locations*</span></span>
    - <span data-ttu-id="50c96-264">**派生テーブル:** *場所*</span><span class="sxs-lookup"><span data-stu-id="50c96-264">**Derived table:** *Locations*</span></span>
    - <span data-ttu-id="50c96-265">**フィールド:** *ゾーン ID*</span><span class="sxs-lookup"><span data-stu-id="50c96-265">**Field:** *Zone ID*</span></span>
    - <span data-ttu-id="50c96-266">**基準:** *バルク* (フィールドでダブルプラス記号 \[**++**\] を選択して一覧を展開し、 *バルク* を選択します。)</span><span class="sxs-lookup"><span data-stu-id="50c96-266">**Criteria:** *Bulk* (Select the double plus sign \[**++**\] in the field to expand the list, and then select *Bulk*.)</span></span>

1. <span data-ttu-id="50c96-267">**OK** を選択します。</span><span class="sxs-lookup"><span data-stu-id="50c96-267">Select **OK**.</span></span>

## <a name="scenario"></a><span data-ttu-id="50c96-268">シナリオ</span><span class="sxs-lookup"><span data-stu-id="50c96-268">Scenario</span></span>

### <a name="set-up-the-scenario"></a><span data-ttu-id="50c96-269">シナリオを設定する</span><span class="sxs-lookup"><span data-stu-id="50c96-269">Set up the scenario</span></span>

<span data-ttu-id="50c96-270">このシナリオでは、組み込みのサンプル データを使用して、このセクションで説明されているレコードを作成します。</span><span class="sxs-lookup"><span data-stu-id="50c96-270">For this scenario, use the built-in sample data, and create the records that are described in this section.</span></span>

#### <a name="use-the-usmf-sample-data"></a><span data-ttu-id="50c96-271">USMF サンプル データの使用</span><span class="sxs-lookup"><span data-stu-id="50c96-271">Use the USMF sample data</span></span>

<span data-ttu-id="50c96-272">ここで指定されたサンプル レコードと値を使用してシナリオを実行するには、標準[デモ データ](../../fin-ops-core/dev-itpro/deployment/deploy-demo-environment.md) がインストールされているシステムを使用する必要があります。</span><span class="sxs-lookup"><span data-stu-id="50c96-272">To work through this scenario by using the sample records and values that are specified here, you must be on a system where the standard [demo data](../../fin-ops-core/dev-itpro/deployment/deploy-demo-environment.md) is installed.</span></span> <span data-ttu-id="50c96-273">また、開始する前に **USMF** 法人を選択する必要があります。</span><span class="sxs-lookup"><span data-stu-id="50c96-273">Additionally, you must select the **USMF** legal entity before you begin.</span></span>

#### <a name="create-demand"></a><span data-ttu-id="50c96-274">需要の作成</span><span class="sxs-lookup"><span data-stu-id="50c96-274">Create demand</span></span>

<span data-ttu-id="50c96-275">スロッティングに適用する需要を作成するには、次の手順に従います。</span><span class="sxs-lookup"><span data-stu-id="50c96-275">Follow these steps to create the demand that you will apply slotting to.</span></span>

1. <span data-ttu-id="50c96-276">**販売とマーケティング \> 販売注文 \> すべての販売注文** の順に移動します。</span><span class="sxs-lookup"><span data-stu-id="50c96-276">Go to **Sales and marketing \> Sales orders \> All sales order**.</span></span>
1. <span data-ttu-id="50c96-277">**新規** を選択して新しい販売注文を作成します。</span><span class="sxs-lookup"><span data-stu-id="50c96-277">Select **New** to create a sales order.</span></span>
1. <span data-ttu-id="50c96-278">**販売注文の作成** ダイアログ ボックスの **顧客 ID** フィールドで、 _US-007_ を選択します。</span><span class="sxs-lookup"><span data-stu-id="50c96-278">In the **Create sales order** dialog box, in the **Customer account** field, select _US-007_.</span></span>
1. <span data-ttu-id="50c96-279">**倉庫** フィールドで、 _61_ を選択します。</span><span class="sxs-lookup"><span data-stu-id="50c96-279">In the **Warehouse** field, select _61_.</span></span>
1. <span data-ttu-id="50c96-280">**OK** を選択します。</span><span class="sxs-lookup"><span data-stu-id="50c96-280">Select **OK**.</span></span>
1. <span data-ttu-id="50c96-281">新しい販売注文が開かれます。</span><span class="sxs-lookup"><span data-stu-id="50c96-281">The new sales order is opened.</span></span> <span data-ttu-id="50c96-282">**販売注文行** クイック タブに空の明細行が含まれています。</span><span class="sxs-lookup"><span data-stu-id="50c96-282">It includes an empty line on the **Sales order lines** FastTab.</span></span> <span data-ttu-id="50c96-283">この明細行で、次の値を設定します。</span><span class="sxs-lookup"><span data-stu-id="50c96-283">On this line, set the following values:</span></span>

    - <span data-ttu-id="50c96-284">**品目:** _L0101_</span><span class="sxs-lookup"><span data-stu-id="50c96-284">**Item:** _L0101_</span></span>
    - <span data-ttu-id="50c96-285">**数量:** _20_</span><span class="sxs-lookup"><span data-stu-id="50c96-285">**Quantity:** _20_</span></span>

1. <span data-ttu-id="50c96-286">**行の追加** を選択して新しい行を追加し、次の値を設定します。</span><span class="sxs-lookup"><span data-stu-id="50c96-286">Select **Add line** to add a new line, and set the following values:</span></span>

    - <span data-ttu-id="50c96-287">**品目:** _T0100_</span><span class="sxs-lookup"><span data-stu-id="50c96-287">**Item:** _T0100_</span></span>
    - <span data-ttu-id="50c96-288">**数量:** _8_</span><span class="sxs-lookup"><span data-stu-id="50c96-288">**Quantity:** _8_</span></span>

1. <span data-ttu-id="50c96-289">**保存** を選択します。</span><span class="sxs-lookup"><span data-stu-id="50c96-289">Select **Save**.</span></span>
1. <span data-ttu-id="50c96-290">**新規** を選択して 2 番目の販売注文を作成します。</span><span class="sxs-lookup"><span data-stu-id="50c96-290">Select **New** to create a second sales order.</span></span>
1. <span data-ttu-id="50c96-291">**販売注文の作成** ダイアログ ボックスの **顧客 ID** フィールドで、 _US-008_ を選択します。</span><span class="sxs-lookup"><span data-stu-id="50c96-291">In the **Create sales order** dialog box, in the **Customer account** field, select _US-008_.</span></span>
1. <span data-ttu-id="50c96-292">**倉庫** フィールドで、 _61_ を選択します。</span><span class="sxs-lookup"><span data-stu-id="50c96-292">In the **Warehouse** field, select _61_.</span></span>
1. <span data-ttu-id="50c96-293">新しい販売注文が開かれます。</span><span class="sxs-lookup"><span data-stu-id="50c96-293">The new sales order is opened.</span></span> <span data-ttu-id="50c96-294">**販売注文行** クイック タブに空の明細行が含まれています。</span><span class="sxs-lookup"><span data-stu-id="50c96-294">It includes an empty line on the **Sales order lines** FastTab.</span></span> <span data-ttu-id="50c96-295">この明細行で、次の値を設定します。</span><span class="sxs-lookup"><span data-stu-id="50c96-295">On this line, set the following values:</span></span>

    - <span data-ttu-id="50c96-296">**品目:** _T0100_</span><span class="sxs-lookup"><span data-stu-id="50c96-296">**Item:** _T0100_</span></span>
    - <span data-ttu-id="50c96-297">**数量:** _1_</span><span class="sxs-lookup"><span data-stu-id="50c96-297">**Quantity:** _1_</span></span>

1. <span data-ttu-id="50c96-298">**保存** を選択します。</span><span class="sxs-lookup"><span data-stu-id="50c96-298">Select **Save**.</span></span>

### <a name="walk-through-a-typical-slotting-scenario"></a><span data-ttu-id="50c96-299">標準的なスロッティングのシナリオを説明していきます</span><span class="sxs-lookup"><span data-stu-id="50c96-299">Walk through a typical slotting scenario</span></span>

<span data-ttu-id="50c96-300">前のセクションで説明したように、すべての前提条件要素が満たされた後、このセクションの各練習を通じて、この機能を試すことができるようになります。</span><span class="sxs-lookup"><span data-stu-id="50c96-300">After all the prerequisite elements are in place, as described in the previous section, you're ready to try out the feature by working through each exercise in this section.</span></span>

#### <a name="generate-demand"></a><span data-ttu-id="50c96-301">要求の生成</span><span class="sxs-lookup"><span data-stu-id="50c96-301">Generate demand</span></span>

1. <span data-ttu-id="50c96-302">**倉庫管理 \> 設定 \> 補充 \> スロッティング テンプレート** の順に移動し、先ほど作成したスロッティング テンプレートを選択します。</span><span class="sxs-lookup"><span data-stu-id="50c96-302">Go to **Warehouse management \> Setup \> Replenishment \> Slotting templates** , and select the slotting template that you created earlier.</span></span>
1. <span data-ttu-id="50c96-303">アクション ウィンドウで、 **需要の生成** を選択します。</span><span class="sxs-lookup"><span data-stu-id="50c96-303">On the Action Pane, select **Generate demand**.</span></span> <span data-ttu-id="50c96-304">このコマンドは、システム内のすべての需要の中で、スロッティング テンプレートのクエリに一致する需要を評価します。</span><span class="sxs-lookup"><span data-stu-id="50c96-304">This command evaluates all demand that is in the system, and that matches the slotting template query.</span></span> <span data-ttu-id="50c96-305">すべての注文の合計需要が、数量/測定単位ごとに 1 つの行に連結されます。</span><span class="sxs-lookup"><span data-stu-id="50c96-305">The total demand across all orders is then consolidated onto one line per quantity/unit of measure.</span></span> <span data-ttu-id="50c96-306">プロセスが完了すると、情報メッセージが表示されます。</span><span class="sxs-lookup"><span data-stu-id="50c96-306">An informational message appears when the process is completed.</span></span>

#### <a name="slotting-demand"></a><span data-ttu-id="50c96-307">スロッティングの要求</span><span class="sxs-lookup"><span data-stu-id="50c96-307">Slotting demand</span></span>

<span data-ttu-id="50c96-308">*スロッティングの需要* はスロッティング テンプレートの設定に基づいて、需要生成の結果を示します。</span><span class="sxs-lookup"><span data-stu-id="50c96-308">The *slotting demand* shows the results of demand generation, based on the setup of the slotting template.</span></span>

- <span data-ttu-id="50c96-309">アクション ウィンドウで、 **スロッティングの需要** を選択して、 **需要生成** コマンドの結果を表示します。</span><span class="sxs-lookup"><span data-stu-id="50c96-309">On the Action Pane, select **Slotting demand** to view the results from the **Generate demand** command.</span></span> <span data-ttu-id="50c96-310">スロッティングの需要の明細行は編集できます。</span><span class="sxs-lookup"><span data-stu-id="50c96-310">The lines in the slotting demand can be edited.</span></span> <span data-ttu-id="50c96-311">明細行を削除したり、新しい明細行を追加したり、行の詳細を編集したりすることができます。</span><span class="sxs-lookup"><span data-stu-id="50c96-311">You can delete a line, add a new line, or edit the line details.</span></span>

> [!NOTE]
> <span data-ttu-id="50c96-312">需要を手動で編集したり、データ管理を使用して外部システムからインポートしたりすることができます。</span><span class="sxs-lookup"><span data-stu-id="50c96-312">You can edit demand manually, or you can import it from an external system by using data management.</span></span> <span data-ttu-id="50c96-313">スロッティングの需要については、どこから入手したかにかかわらず、次の手順で使用されます。</span><span class="sxs-lookup"><span data-stu-id="50c96-313">Whatever is in the slotting demand will be used in the next step, regardless of where it came from.</span></span>

#### <a name="locate-demand"></a><span data-ttu-id="50c96-314">要求の特定</span><span class="sxs-lookup"><span data-stu-id="50c96-314">Locate demand</span></span>

<span data-ttu-id="50c96-315">需要が生成された後に、 **需要の検索** コマンドを使用して *スロッティングの計画* を生成する必要があります。</span><span class="sxs-lookup"><span data-stu-id="50c96-315">After demand has been generated, you must use the **Locate demand** command to generate the *slotting plan*.</span></span>

- <span data-ttu-id="50c96-316">アクション ウィンドウで、 **需要の検索** を選択します。</span><span class="sxs-lookup"><span data-stu-id="50c96-316">On the Action Pane, select **Locate demand**.</span></span> <span data-ttu-id="50c96-317">スロッティングのプロセスが実行されます。</span><span class="sxs-lookup"><span data-stu-id="50c96-317">The slotting process runs.</span></span> <span data-ttu-id="50c96-318">プロセスが完了すると、情報メッセージが表示されます。</span><span class="sxs-lookup"><span data-stu-id="50c96-318">An informational message appears when the process is completed.</span></span>

#### <a name="slotting-plan"></a><span data-ttu-id="50c96-319">スロッティングの計画</span><span class="sxs-lookup"><span data-stu-id="50c96-319">Slotting plan</span></span>

<span data-ttu-id="50c96-320">スロッティングの計画には、各品目または数量が割り当てられた場所、オーバーフローが使用されたかどうか、停止作業が作成されたかどうか、および使用されたテンプレート行が示されます。</span><span class="sxs-lookup"><span data-stu-id="50c96-320">The slotting plan shows the location that each item/quantity was assigned to, whether overflow was used, whether let-up work was created, and the template line that was used.</span></span> <span data-ttu-id="50c96-321">**スロット化できなかった需要は、赤で強調表示されます。**</span><span class="sxs-lookup"><span data-stu-id="50c96-321">**Any demand that could not be slotted is highlighted in red.**</span></span>

- <span data-ttu-id="50c96-322">アクション ウィンドウで、 **スロッティングの計画** を選択して結果を表示します。</span><span class="sxs-lookup"><span data-stu-id="50c96-322">On the Action Pane, select **Slotting plan** to view the results.</span></span>

#### <a name="create-replenishment"></a><span data-ttu-id="50c96-323">補充を作成する</span><span class="sxs-lookup"><span data-stu-id="50c96-323">Create replenishment</span></span>

<span data-ttu-id="50c96-324">スロッティングの計画を作成した後、計画に基づいて *補充作業* を作成する必要があります。</span><span class="sxs-lookup"><span data-stu-id="50c96-324">After the slotting plan has been created, you must create *replenishment work* , based on the plan.</span></span>

- <span data-ttu-id="50c96-325">アクション ウィンドウで、 **補充の実行** を選択します。</span><span class="sxs-lookup"><span data-stu-id="50c96-325">On the Action Pane, select **Run replenishment**.</span></span> <span data-ttu-id="50c96-326">プロセスが完了すると、情報メッセージが表示されます。</span><span class="sxs-lookup"><span data-stu-id="50c96-326">An informational message appears when the process is completed.</span></span> <span data-ttu-id="50c96-327">このメッセージは、作業ビルド ID に対して作成されたヘッダーの数を示します。</span><span class="sxs-lookup"><span data-stu-id="50c96-327">This message indicates the number of headers that were created for the work build ID.</span></span>

<span data-ttu-id="50c96-328">使用されるロケーション ディレクティブは、各テンプレート行に指定されているディレクティブ コードに基づいて識別されます。</span><span class="sxs-lookup"><span data-stu-id="50c96-328">Location directives that will be used are identified based on the directive code that is specified on each template line.</span></span>

## <a name="tips"></a><span data-ttu-id="50c96-329">ヒント</span><span class="sxs-lookup"><span data-stu-id="50c96-329">Tips</span></span>

### <a name="set-up-automatic-slotting"></a><span data-ttu-id="50c96-330">自動スロッティングの設定</span><span class="sxs-lookup"><span data-stu-id="50c96-330">Set up automatic slotting</span></span>

<span data-ttu-id="50c96-331">必要な要素すべてを満たした後、次の手順に従って自動的に実行されるようにスロッティングを設定できます。</span><span class="sxs-lookup"><span data-stu-id="50c96-331">After all the required elements are in place, you can set up slotting to run automatically by following these steps.</span></span>

1. <span data-ttu-id="50c96-332">**倉庫管理 \> 補充 \> スロッティングの実行** の順に移動します。</span><span class="sxs-lookup"><span data-stu-id="50c96-332">Go to **Warehouse management \> Replenishment \> Run slotting**.</span></span>
1. <span data-ttu-id="50c96-333">実行するスロッティングの手順を指定します。</span><span class="sxs-lookup"><span data-stu-id="50c96-333">Specify the slotting steps to run.</span></span> <span data-ttu-id="50c96-334">1 つ以上の以下のスロッティングの手順を選択します。</span><span class="sxs-lookup"><span data-stu-id="50c96-334">Select one or more of the following slotting steps:</span></span>

    - <span data-ttu-id="50c96-335">要求の生成</span><span class="sxs-lookup"><span data-stu-id="50c96-335">Generate demand</span></span>
    - <span data-ttu-id="50c96-336">要求の特定</span><span class="sxs-lookup"><span data-stu-id="50c96-336">Locate demand</span></span>
    - <span data-ttu-id="50c96-337">補充作業の作成</span><span class="sxs-lookup"><span data-stu-id="50c96-337">Create replenishment work</span></span>

    > [!NOTE]
    > <span data-ttu-id="50c96-338">スロッティングの手順はプログレッシブです。</span><span class="sxs-lookup"><span data-stu-id="50c96-338">The slotting steps are progressive.</span></span> <span data-ttu-id="50c96-339">*需要の検索* を選択するには、最初に *需要の生成* を選択する必要があります。</span><span class="sxs-lookup"><span data-stu-id="50c96-339">If you want to select *Locate demand* , you must first select *Generate demand*.</span></span>

1. <span data-ttu-id="50c96-340">使用するスロッティングのテンプレートを指定します。</span><span class="sxs-lookup"><span data-stu-id="50c96-340">Specify the slotting template to use.</span></span>
1. <span data-ttu-id="50c96-341">必要に応じて繰り返し自動的に実行されるように設定します。</span><span class="sxs-lookup"><span data-stu-id="50c96-341">Set the recurrence to run automatically, if you want.</span></span>

<span data-ttu-id="50c96-342">シナリオの演習では、自動スロッティングを **しない** に設定してください。</span><span class="sxs-lookup"><span data-stu-id="50c96-342">For the exercises in the scenario, do **not** set up automatic slotting.</span></span>
