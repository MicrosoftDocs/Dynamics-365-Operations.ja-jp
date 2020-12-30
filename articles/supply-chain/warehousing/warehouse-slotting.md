---
title: 倉庫のスロッティング
description: このトピックでは、倉庫のスロッティングについて説明します。 倉庫のスロッティングでは、注文済、予約済、またはリリース済のステータスである注文から、品目および測定単位別に需要を連結できます。 これにより、倉庫管理者は、注文を倉庫にリリースしてピッキング作業を作成する前に、ピッキング場所をインテリジェントに計画できます。
author: mirzaab
manager: tfehr
ms.date: 11/13/2020
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
ms.openlocfilehash: 31b86837735ca16610a1d304eab611b12a6aceeb
ms.sourcegitcommit: be4b9d557511bbb43e71a93f2c3b23b5f1a4669d
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 11/24/2020
ms.locfileid: "4627752"
---
# <a name="warehouse-slotting"></a><span data-ttu-id="d1fc5-105">倉庫のスロッティング</span><span class="sxs-lookup"><span data-stu-id="d1fc5-105">Warehouse slotting</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="d1fc5-106">倉庫管理者が、注文を倉庫にリリースしてピッキング作業を作成する前に、ピッキング場所をインテリジェントに計画できるよう、複数の倉庫スロッティング機能が用意されています。</span><span class="sxs-lookup"><span data-stu-id="d1fc5-106">Several warehouse slotting features are available to help warehouse managers intelligently plan picking locations before they release orders to the warehouse and create picking work.</span></span>

<span data-ttu-id="d1fc5-107">*倉庫のスロッティング機能* では、*注文済*、*予約済*、または *リリース済* のステータスである注文から、品目および測定単位別に需要を連結できます。</span><span class="sxs-lookup"><span data-stu-id="d1fc5-107">The *Warehouse slotting feature* lets you consolidate demand by item and unit of measure from orders that have a status of *Ordered*, *Reserved*, or *Released*.</span></span> <span data-ttu-id="d1fc5-108">生成された需要は、数量、単位、物理的分析コード、固定の場所などに基づいてピッキングに使用される場所を適用できます。</span><span class="sxs-lookup"><span data-stu-id="d1fc5-108">Generated demand can then be applied to locations that will be used for picking, based on quantity, unit, physical dimensions, fixed locations, and more.</span></span> <span data-ttu-id="d1fc5-109">スロッティングの計画が確立された後に、補充作業を作成して、各場所に適切な量の在庫を取り込むことができます。</span><span class="sxs-lookup"><span data-stu-id="d1fc5-109">After the slotting plan has been established, replenishment work can be created to bring the appropriate amount of inventory to each location.</span></span>

<span data-ttu-id="d1fc5-110">*移動オーダーの倉庫スロッティング* 機能により、倉庫管理者は、まだ倉庫にリリースされていない移動オーダーからの需要に基づいてピッキング場所を補充できます。</span><span class="sxs-lookup"><span data-stu-id="d1fc5-110">The *Warehouse slotting for transfer orders* feature lets warehouse managers replenish picking locations, based on demand from transfer orders that aren't yet released to the warehouse.</span></span> <span data-ttu-id="d1fc5-111">これにより、倉庫へのリリース後に移動オーダーに必要なすべての品目がピッキング場所に含まれるようになります。</span><span class="sxs-lookup"><span data-stu-id="d1fc5-111">It ensures that picking locations will include all the items that are required for the transfer orders after they are released to warehouse.</span></span> <span data-ttu-id="d1fc5-112">この機能を有効にするには、*倉庫スロッティング機能* も有効にする必要があります。</span><span class="sxs-lookup"><span data-stu-id="d1fc5-112">This feature requires that you also turn on the *Warehouse slotting feature* feature.</span></span>

<span data-ttu-id="d1fc5-113">*倉庫スロッティングの割り当て拡張* 機能により、*倉庫スロッティング機能* によって使用されるテンプレート行のオプションが追加されます。</span><span class="sxs-lookup"><span data-stu-id="d1fc5-113">The *Warehouse slotting allocation enhancements* feature adds an option for the template lines that are used by the *Warehouse slotting feature* feature.</span></span> <span data-ttu-id="d1fc5-114">このオプションを選択すると、システムは既存の手持在庫をターゲットの場所で考慮できます。</span><span class="sxs-lookup"><span data-stu-id="d1fc5-114">The option enables the system to consider existing on-hand inventory at a target location.</span></span> <span data-ttu-id="d1fc5-115">したがって、スロッティングに対して生成される補充の数は少なくなる可能性があります。</span><span class="sxs-lookup"><span data-stu-id="d1fc5-115">Therefore, fewer replenishments might be generated for slotting.</span></span> <span data-ttu-id="d1fc5-116">*倉庫スロッティングの割り当て拡張* 機能を使用するには、*倉庫スロッティング機能* も有効にする必要があります。</span><span class="sxs-lookup"><span data-stu-id="d1fc5-116">The *Warehouse slotting allocation enhancements* feature requires that you also turn on the *Warehouse slotting feature* feature.</span></span> <span data-ttu-id="d1fc5-117">必要に応じて、*移動オーダーの倉庫スロッティング* 機能と組み合わせて使用することもできます。</span><span class="sxs-lookup"><span data-stu-id="d1fc5-117">It can optionally be used together with the *Warehouse slotting for transfer orders* feature.</span></span>

## <a name="turn-on-the-warehouse-slotting-features"></a><span data-ttu-id="d1fc5-118">倉庫のスロッティング機能をオンにする</span><span class="sxs-lookup"><span data-stu-id="d1fc5-118">Turn on the warehouse slotting features</span></span>

<span data-ttu-id="d1fc5-119">これらの機能を使用するには、システム上で有効化する必要があります。</span><span class="sxs-lookup"><span data-stu-id="d1fc5-119">Before you can use these features, they must be turned on in your system.</span></span> <span data-ttu-id="d1fc5-120">管理者は、[機能の管理](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md)設定を使用して、機能の状態を確認し、必要に応じて有効化することができます。</span><span class="sxs-lookup"><span data-stu-id="d1fc5-120">Admins can use the [feature management](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) settings to check the status of the features and turn them on if they are required.</span></span> <span data-ttu-id="d1fc5-121">必要に応じて、次の機能を有効にします。</span><span class="sxs-lookup"><span data-stu-id="d1fc5-121">Turn on the following features as required:</span></span>

- <span data-ttu-id="d1fc5-122">倉庫スロット機能</span><span class="sxs-lookup"><span data-stu-id="d1fc5-122">Warehouse slotting feature</span></span>
- <span data-ttu-id="d1fc5-123">移動オーダー用の倉庫のスロッティング</span><span class="sxs-lookup"><span data-stu-id="d1fc5-123">Warehouse slotting for transfer orders</span></span>

    > [!IMPORTANT]
    > <span data-ttu-id="d1fc5-124">この機能を有効にするには、*倉庫スロッティング機能* を有効にする必要があります。</span><span class="sxs-lookup"><span data-stu-id="d1fc5-124">The *Warehouse slotting feature* feature must be turned on before this feature.</span></span>

- <span data-ttu-id="d1fc5-125">倉庫のスロッティングの割り当て拡張</span><span class="sxs-lookup"><span data-stu-id="d1fc5-125">Warehouse slotting allocation enhancements</span></span>

    > [!IMPORTANT]
    > <span data-ttu-id="d1fc5-126">この機能を有効にするには、*倉庫スロッティング機能* を有効にする必要があります。</span><span class="sxs-lookup"><span data-stu-id="d1fc5-126">The *Warehouse slotting feature* feature must be turned on before this feature.</span></span>

## <a name="set-up-warehouse-slotting"></a><span data-ttu-id="d1fc5-127">倉庫のスロッティングの設定</span><span class="sxs-lookup"><span data-stu-id="d1fc5-127">Set up warehouse slotting</span></span>

<span data-ttu-id="d1fc5-128">倉庫のスロッティングを使用するには、次の要素をシステムで設定する必要があります。</span><span class="sxs-lookup"><span data-stu-id="d1fc5-128">To use warehouse slotting, you must set up the following elements in your system:</span></span>

- <span data-ttu-id="d1fc5-129">スロッティングの測定単位階層</span><span class="sxs-lookup"><span data-stu-id="d1fc5-129">Slotting unit of measure tiers</span></span>
- <span data-ttu-id="d1fc5-130">ディレクティブ コード</span><span class="sxs-lookup"><span data-stu-id="d1fc5-130">Directive codes</span></span>
- <span data-ttu-id="d1fc5-131">スロッティング テンプレート</span><span class="sxs-lookup"><span data-stu-id="d1fc5-131">Slotting templates</span></span>
- <span data-ttu-id="d1fc5-132">場所のディレクティブ</span><span class="sxs-lookup"><span data-stu-id="d1fc5-132">Location directives</span></span>

### <a name="create-unit-of-measure-tiers-for-slotting"></a><a name="unit-tiers"></a><span data-ttu-id="d1fc5-133">スロッティングの測定単位層の作成</span><span class="sxs-lookup"><span data-stu-id="d1fc5-133">Create unit-of-measure tiers for slotting</span></span>

<span data-ttu-id="d1fc5-134">測定単位層は、スロッティング目的で複数の測定単位をグループ化できます。</span><span class="sxs-lookup"><span data-stu-id="d1fc5-134">Unit-of-measure tiers enable multiple units of measure to be grouped together for the purposes of slotting.</span></span> <span data-ttu-id="d1fc5-135">たとえば、同じボックスのピッキング エリアから複数のボックスがすべてピッキングされた場合、すべてのサイズに対して 1 つの層を作成することができます。</span><span class="sxs-lookup"><span data-stu-id="d1fc5-135">For example, if multiple sizes of boxes are all picked from the same box picking area, one tier can be created for all the sizes.</span></span> <span data-ttu-id="d1fc5-136">**各層に含まれる測定単位ごとに明細行を作成する必要があります。**</span><span class="sxs-lookup"><span data-stu-id="d1fc5-136">**A line must be created for each unit of measure that should be part of the tier.**</span></span>

1. <span data-ttu-id="d1fc5-137">**倉庫管理 \> 設定 \> 補充 \> 測定単位層のスロッティング** に移動します。</span><span class="sxs-lookup"><span data-stu-id="d1fc5-137">Go to **Warehouse management \> Setup \> Replenishment \> Slotting unit of measure tiers**.</span></span>
1. <span data-ttu-id="d1fc5-138">**新規** を選択します。</span><span class="sxs-lookup"><span data-stu-id="d1fc5-138">Select **New**.</span></span>
1. <span data-ttu-id="d1fc5-139">ヘッダーで、次の値を設定します。</span><span class="sxs-lookup"><span data-stu-id="d1fc5-139">In the header, set the following values:</span></span>

    - <span data-ttu-id="d1fc5-140">**測定単位層:** *EaBoxPl*</span><span class="sxs-lookup"><span data-stu-id="d1fc5-140">**Unit of measure tier:** *EaBoxPl*</span></span>
    - <span data-ttu-id="d1fc5-141">**説明:** *各ボックス パレット*</span><span class="sxs-lookup"><span data-stu-id="d1fc5-141">**Description:** *Each box pallet*</span></span>

1. <span data-ttu-id="d1fc5-142">**保存** を選択します。</span><span class="sxs-lookup"><span data-stu-id="d1fc5-142">Select **Save**.</span></span>
1. <span data-ttu-id="d1fc5-143">**測定単位** クイック タブで、**新規** を選択してグリッドに行を追加します。</span><span class="sxs-lookup"><span data-stu-id="d1fc5-143">On the **Units of measure** FastTab, select **New** to add a line to the grid.</span></span>
1. <span data-ttu-id="d1fc5-144">新しい明細行で、次の値を設定します。</span><span class="sxs-lookup"><span data-stu-id="d1fc5-144">On the new line, set the following values:</span></span>

    - <span data-ttu-id="d1fc5-145">**単位:** *ボックス*</span><span class="sxs-lookup"><span data-stu-id="d1fc5-145">**Unit:** *Box*</span></span>
    - <span data-ttu-id="d1fc5-146">**説明:** このフィールドは空白のままにしておきます。</span><span class="sxs-lookup"><span data-stu-id="d1fc5-146">**Description:** Leave this field blank.</span></span> <span data-ttu-id="d1fc5-147">変更を保存すると、自動的に入力されます。</span><span class="sxs-lookup"><span data-stu-id="d1fc5-147">It will be filled in automatically when you save your changes.</span></span>
    - <span data-ttu-id="d1fc5-148">**単位クラス:** *数量*</span><span class="sxs-lookup"><span data-stu-id="d1fc5-148">**Unit class:** *Quantity*</span></span>

1. <span data-ttu-id="d1fc5-149">**新規** を選択して、グリッドの 2 行目を追加します。</span><span class="sxs-lookup"><span data-stu-id="d1fc5-149">Select **New** to add a second line to the grid.</span></span>
1. <span data-ttu-id="d1fc5-150">新しい明細行で、次の値を設定します。</span><span class="sxs-lookup"><span data-stu-id="d1fc5-150">On the new line, set the following values:</span></span>

    - <span data-ttu-id="d1fc5-151">**単位:** *個*</span><span class="sxs-lookup"><span data-stu-id="d1fc5-151">**Unit:** *ea*</span></span>
    - <span data-ttu-id="d1fc5-152">**説明:** このフィールドは空白のままにしておきます。</span><span class="sxs-lookup"><span data-stu-id="d1fc5-152">**Description:** Leave this field blank.</span></span> <span data-ttu-id="d1fc5-153">変更を保存すると、自動的に入力されます。</span><span class="sxs-lookup"><span data-stu-id="d1fc5-153">It will be filled in automatically when you save your changes.</span></span>
    - <span data-ttu-id="d1fc5-154">**単位クラス:** *数量*</span><span class="sxs-lookup"><span data-stu-id="d1fc5-154">**Unit class:** *Quantity*</span></span>

1. <span data-ttu-id="d1fc5-155">**新規** を選択して、グリッドの 3 行目を追加します。</span><span class="sxs-lookup"><span data-stu-id="d1fc5-155">Select **New** to add a third line to the grid.</span></span>
1. <span data-ttu-id="d1fc5-156">新しい明細行で、次の値を設定します。</span><span class="sxs-lookup"><span data-stu-id="d1fc5-156">On the new line, set the following values:</span></span>

    - <span data-ttu-id="d1fc5-157">**ユニット:** *PL*</span><span class="sxs-lookup"><span data-stu-id="d1fc5-157">**Unit:** *PL*</span></span>
    - <span data-ttu-id="d1fc5-158">**説明:** このフィールドは空白のままにしておきます。</span><span class="sxs-lookup"><span data-stu-id="d1fc5-158">**Description:** Leave this field blank.</span></span> <span data-ttu-id="d1fc5-159">変更を保存すると、自動的に入力されます。</span><span class="sxs-lookup"><span data-stu-id="d1fc5-159">It will be filled in automatically when you save your changes.</span></span>
    - <span data-ttu-id="d1fc5-160">**単位クラス:** *数量*</span><span class="sxs-lookup"><span data-stu-id="d1fc5-160">**Unit class:** *Quantity*</span></span>

1. <span data-ttu-id="d1fc5-161">**保存** を選択して階層に保存します。</span><span class="sxs-lookup"><span data-stu-id="d1fc5-161">Select **Save** to save the tier.</span></span>

### <a name="create-a-directive-code-for-slotting"></a><span data-ttu-id="d1fc5-162">スロッティング用のディレクティブ コードの作成</span><span class="sxs-lookup"><span data-stu-id="d1fc5-162">Create a directive code for slotting</span></span>

<span data-ttu-id="d1fc5-163">テンプレートに関連付けるディレクティブ コードを選択する必要があります。</span><span class="sxs-lookup"><span data-stu-id="d1fc5-163">You must select the directive code that should be associated with a template.</span></span>

1. <span data-ttu-id="d1fc5-164">**倉庫管理 \> 設定 \> ディレクティブ コード** に移動します。</span><span class="sxs-lookup"><span data-stu-id="d1fc5-164">Go to **Warehouse management \> Setup \> Directive codes**.</span></span>
1. <span data-ttu-id="d1fc5-165">アクション ウィンドウで、**新規** を選択します。</span><span class="sxs-lookup"><span data-stu-id="d1fc5-165">On the Action Pane, select **New**.</span></span>
1. <span data-ttu-id="d1fc5-166">**ディレクティブ コード** フィールドに、*スロッティング* と入力します。</span><span class="sxs-lookup"><span data-stu-id="d1fc5-166">In the **Directive code** field, enter *Slotting*.</span></span>
1. <span data-ttu-id="d1fc5-167">**ディレクティブの説明** フィールドに、*スロッティング* と入力します。</span><span class="sxs-lookup"><span data-stu-id="d1fc5-167">In the **Directive description** field, enter *Slotting*.</span></span>

### <a name="set-up-slotting-templates"></a><span data-ttu-id="d1fc5-168">スロッティング テンプレートの設定</span><span class="sxs-lookup"><span data-stu-id="d1fc5-168">Set up slotting templates</span></span>

<span data-ttu-id="d1fc5-169">各スロッティング テンプレートは、在庫を特定の倉庫の場所に割り当てる方法を制御します。</span><span class="sxs-lookup"><span data-stu-id="d1fc5-169">Each slotting template controls how inventory is assigned to locations for a specific warehouse.</span></span> <span data-ttu-id="d1fc5-170">各テンプレートには、スロッティングの仕様ごとに 1 行を含める必要があります。</span><span class="sxs-lookup"><span data-stu-id="d1fc5-170">Each template must include a line for each slotting specification.</span></span> <span data-ttu-id="d1fc5-171">スロッティング テンプレートを設定するには、このセクションの手順を使用します。</span><span class="sxs-lookup"><span data-stu-id="d1fc5-171">Use the procedures in this section to set up slotting templates.</span></span>

1. <span data-ttu-id="d1fc5-172">**倉庫管理 \> 設定 \> 補充 \> スロッティング テンプレート** の順に移動します。</span><span class="sxs-lookup"><span data-stu-id="d1fc5-172">Go to **Warehouse management \> Setup \> Replenishment \> Slotting templates**.</span></span>
1. <span data-ttu-id="d1fc5-173">**新規作成** を選択してテンプレートを作成します。</span><span class="sxs-lookup"><span data-stu-id="d1fc5-173">Select **New** to create a template.</span></span>

<span data-ttu-id="d1fc5-174">次に、以下のサブセクションで説明するように、テンプレート ヘッダー、スロッティングの仕様、および場所ディレクティブを設定する必要があります。</span><span class="sxs-lookup"><span data-stu-id="d1fc5-174">Next, you must set up the template header, slotting specifications, and location directives, as explained in the following subsections.</span></span> <span data-ttu-id="d1fc5-175">移動オーダーのスロッティングの設定は、販売注文のスロッティングの設定に似ていますが、**需要タイプ** フィールドは、*販売注文* ではなく *移動オーダー* に設定します。</span><span class="sxs-lookup"><span data-stu-id="d1fc5-175">The setup for slotting for transfer orders resembles the setup for slotting for sales orders, but the **Demand type** field is set *Transfer orders* instead of *Sales order*.</span></span>

#### <a name="set-up-the-header-for-a-sales-order-slotting-template"></a><span data-ttu-id="d1fc5-176">販売注文のスロッティング テンプレートのヘッダーの設定</span><span class="sxs-lookup"><span data-stu-id="d1fc5-176">Set up the header for a sales order slotting template</span></span>

1. <span data-ttu-id="d1fc5-177">テンプレートのヘッダーで、次の値を設定します。</span><span class="sxs-lookup"><span data-stu-id="d1fc5-177">In the header for the template, set the following values:</span></span>

    - <span data-ttu-id="d1fc5-178">**スロッティング テンプレート:** _61_</span><span class="sxs-lookup"><span data-stu-id="d1fc5-178">**Slotting template:** _61_</span></span>
    - <span data-ttu-id="d1fc5-179">**説明:** _61_</span><span class="sxs-lookup"><span data-stu-id="d1fc5-179">**Description:** _61_</span></span>
    - <span data-ttu-id="d1fc5-180">**需要タイプ:** *販売注文*</span><span class="sxs-lookup"><span data-stu-id="d1fc5-180">**Demand type:** *Sales order*</span></span>

        > [!NOTE]
        > <span data-ttu-id="d1fc5-181">現在、*販売注文* と *移動オーダー* は、サポートされている唯一の需要タイプです。</span><span class="sxs-lookup"><span data-stu-id="d1fc5-181">Currently, *Sales orders* and *Transfer orders* are the only demand types that are supported.</span></span> <span data-ttu-id="d1fc5-182">*移動オーダー* を選択できるのは、*移動オーダーの倉庫スロッティング* 機能がオンになっている場合のみです。</span><span class="sxs-lookup"><span data-stu-id="d1fc5-182">You can select *Transfer orders* only if the *Warehouse Slotting for transfer orders* feature is turned on.</span></span>

    - <span data-ttu-id="d1fc5-183">**需要戦略:** _注文済_</span><span class="sxs-lookup"><span data-stu-id="d1fc5-183">**Demand strategy:** _Ordered_</span></span>

        <span data-ttu-id="d1fc5-184">以下の値は、このフィールドで使用できます。</span><span class="sxs-lookup"><span data-stu-id="d1fc5-184">The following values are available in this field:</span></span>

        - <span data-ttu-id="d1fc5-185">**注文済** – 販売注文の注文済数量すべてを需要と見なされます。</span><span class="sxs-lookup"><span data-stu-id="d1fc5-185">**Ordered** – The full ordered quantity on the sales order should be considered demand.</span></span>
        - <span data-ttu-id="d1fc5-186">**予約済** – 予約済 (現物と注文済の両方) である販売注文明細行数量のみを要求と見なされます。</span><span class="sxs-lookup"><span data-stu-id="d1fc5-186">**Reserved** – Only the sales order line quantities that are reserved (physical and ordered) should be considered demand.</span></span>
        - <span data-ttu-id="d1fc5-187">**リリース済**: リリース済数量は需要と見なす必要があります。</span><span class="sxs-lookup"><span data-stu-id="d1fc5-187">**Released** – The released quantity should be considered demand.</span></span>

    - <span data-ttu-id="d1fc5-188">**倉庫:** _61_</span><span class="sxs-lookup"><span data-stu-id="d1fc5-188">**Warehouse:** _61_</span></span>
    - <span data-ttu-id="d1fc5-189">**ウェーブ要素に未引当数量の使用を許可する:** _はい_</span><span class="sxs-lookup"><span data-stu-id="d1fc5-189">**Allow wave demand to use unreserved quantities:** _Yes_</span></span>

<span data-ttu-id="d1fc5-190">評価する需要の範囲を絞り込むためのクエリを指定することもできます。</span><span class="sxs-lookup"><span data-stu-id="d1fc5-190">You can also specify a query to narrow the scope of the demand that is evaluated.</span></span>

#### <a name="set-up-slotting-specifications-for-each-template"></a><span data-ttu-id="d1fc5-191">スロッティングの仕様の各テンプレートを設定します</span><span class="sxs-lookup"><span data-stu-id="d1fc5-191">Set up slotting specifications for each template</span></span>

<span data-ttu-id="d1fc5-192">作成する販売注文テンプレートごとに、次の手順に従ってスロッティングの仕様ごとに行を追加します。</span><span class="sxs-lookup"><span data-stu-id="d1fc5-192">For each sales order template that you create, follow these steps to add a line for each slotting specification.</span></span>

1. <span data-ttu-id="d1fc5-193">**スロッティングのテンプレート詳細** クイック タブで、**新規** を選択してテンプレート行を作成します。</span><span class="sxs-lookup"><span data-stu-id="d1fc5-193">On the **Slotting template details** FastTab, select **New** to create a template line.</span></span>
1. <span data-ttu-id="d1fc5-194">新しい明細行で、次の値を設定します。</span><span class="sxs-lookup"><span data-stu-id="d1fc5-194">On the new line, set the following values:</span></span>

    - <span data-ttu-id="d1fc5-195">**シーケンス:** _1_</span><span class="sxs-lookup"><span data-stu-id="d1fc5-195">**Sequence:** _1_</span></span>
    - <span data-ttu-id="d1fc5-196">**説明:** _固定の場所_</span><span class="sxs-lookup"><span data-stu-id="d1fc5-196">**Description:** _Fixed location_</span></span>
    - <span data-ttu-id="d1fc5-197">**最小数量:** _1_</span><span class="sxs-lookup"><span data-stu-id="d1fc5-197">**Minimum quantity:** _1_</span></span>

        <span data-ttu-id="d1fc5-198">このフィールドでは、明細行に必要な最小需要数量を定義します。</span><span class="sxs-lookup"><span data-stu-id="d1fc5-198">This field defines the minimum quantity of demand that is required for the line.</span></span>

    - <span data-ttu-id="d1fc5-199">**最大数量:** _1000000_</span><span class="sxs-lookup"><span data-stu-id="d1fc5-199">**Maximum quantity:** _1000000_</span></span>

        <span data-ttu-id="d1fc5-200">このフィールドでは、明細行に有効な最大需要数量を定義します。</span><span class="sxs-lookup"><span data-stu-id="d1fc5-200">This field defines the maximum quantity of demand that is valid for the line.</span></span>

    - <span data-ttu-id="d1fc5-201">**ユニット:** このフィールドは空白のままにします。</span><span class="sxs-lookup"><span data-stu-id="d1fc5-201">**Unit:** Leave this field blank.</span></span>

        <span data-ttu-id="d1fc5-202">このフィールドは、最小数量と最大数量が参照する測定単位を定義します。</span><span class="sxs-lookup"><span data-stu-id="d1fc5-202">This field defines the unit of measure that the minimum and maximum quantities refer to.</span></span>

    - <span data-ttu-id="d1fc5-203">**測定単位層:** _EaBoxPl_</span><span class="sxs-lookup"><span data-stu-id="d1fc5-203">**Unit of Measure Tier:** _EaBoxPl_</span></span>

        <span data-ttu-id="d1fc5-204">このフィールドでは、明細行有効な測定単位を定義します。</span><span class="sxs-lookup"><span data-stu-id="d1fc5-204">This field defines the units of measure of demand that are valid for the line.</span></span> <span data-ttu-id="d1fc5-205">(詳細については、このトピックの前の[スロッティングの測定単位層の設定](#unit-tiers) セクションを参照してください。)</span><span class="sxs-lookup"><span data-stu-id="d1fc5-205">(For more information, see the [Set up unit-of-measure tiers for slotting](#unit-tiers) section earlier in this topic.)</span></span>

    - <span data-ttu-id="d1fc5-206">**スロット基準の割り当て:** _数量を考慮_</span><span class="sxs-lookup"><span data-stu-id="d1fc5-206">**Assign slot criteria:** _Consider qty_</span></span>

        <span data-ttu-id="d1fc5-207">以下の値は、このフィールドで使用できます。</span><span class="sxs-lookup"><span data-stu-id="d1fc5-207">The following values are available in this field:</span></span>

        - <span data-ttu-id="d1fc5-208">**空白であると仮定** – このシステムでは、ピッキングエリア内のすべての場所が空であると想定し、在庫の場所を確認しないようにします。</span><span class="sxs-lookup"><span data-stu-id="d1fc5-208">**Assume empty** – This system should assume that all locations in the picking area are empty and should not check those locations for inventory.</span></span>
        - <span data-ttu-id="d1fc5-209">**数量を考慮** – このシステムでは、ピッキングエリア内の場所で在庫を確認し、空でない場所はスキップするようにします。</span><span class="sxs-lookup"><span data-stu-id="d1fc5-209">**Consider qty** – The system should check the locations in the picking area for inventory and should skip any locations that aren't empty.</span></span>
        - <span data-ttu-id="d1fc5-210">**手持在庫を考慮する**: ターゲットの場所に需要明細行の品目の未引き当て数量が含まれているかどうかをシステムが確認します。</span><span class="sxs-lookup"><span data-stu-id="d1fc5-210">**Consider on-hand** – The system should check whether any target location contains unreserved quantities for the item on the demand line.</span></span> <span data-ttu-id="d1fc5-211">需要明細行の少なくとも 1 つの単位を満たすのに十分な量がある場合は、生成されたスロッティング計画レコードが利用可能な数量分減少します。</span><span class="sxs-lookup"><span data-stu-id="d1fc5-211">If the quantity is large enough to satisfy at least one unit of the demand line, the generated slotting plan record is reduced by the available amount.</span></span> <span data-ttu-id="d1fc5-212">たとえば、需要が 10 ケースで、1 つのケースが手元にある場合、検出された需要は 9 つのケースになります。</span><span class="sxs-lookup"><span data-stu-id="d1fc5-212">For example, if the demand is 10 cases, and one case is on hand, the located demand will be nine cases.</span></span> <span data-ttu-id="d1fc5-213">需要が 10 ケースで、1 個ずつ手元にある場合、検出された需要は 10 ケースになります。</span><span class="sxs-lookup"><span data-stu-id="d1fc5-213">If the demand is 10 cases, and one each is on hand, the located demand will be 10 cases.</span></span> <span data-ttu-id="d1fc5-214">この値は、*倉庫スロッティング割り当て拡張* 機能がオンになっている場合にのみ使用できます。</span><span class="sxs-lookup"><span data-stu-id="d1fc5-214">This value is available only when the *Warehouse slotting allocation enhancements* feature is turned on.</span></span>

    - <span data-ttu-id="d1fc5-215">**ディレクティブ コード:** _スロッティング_</span><span class="sxs-lookup"><span data-stu-id="d1fc5-215">**Directive code:** _Slotting_</span></span>

        <span data-ttu-id="d1fc5-216">このフィールドでは、補充作業のピッキング場所を検索する際に使用される場所のディレクティブを定義します。</span><span class="sxs-lookup"><span data-stu-id="d1fc5-216">This field defines the location directive that is used to find the picking location of the replenishment work.</span></span>

    - <span data-ttu-id="d1fc5-217">**オーバーフローの場所:** このフィールドは空白のままにします。</span><span class="sxs-lookup"><span data-stu-id="d1fc5-217">**Overflow location:** Leave this field blank.</span></span>

        <span data-ttu-id="d1fc5-218">このフィールドは、明細行が処理されたときに在庫が数量の場所が検出されない場合に、在庫が置かれる場所を定義します。</span><span class="sxs-lookup"><span data-stu-id="d1fc5-218">This field defines the location that inventory that is put to if a location can't be found for the quantity when the line is processed.</span></span>

    - <span data-ttu-id="d1fc5-219">**停止の許可:** _はい_</span><span class="sxs-lookup"><span data-stu-id="d1fc5-219">**Allow let up:** _Yes_</span></span>

        <span data-ttu-id="d1fc5-220">このオプションを *はい* に設定すると、スロット化できない需要がある場合、在庫があっても、スロット化されていない場所から在庫を取り出す振替作業が作成されます。</span><span class="sxs-lookup"><span data-stu-id="d1fc5-220">When this option is set to *Yes*, if any demand can't be slotted, movement work will be created to take inventory out of locations where there is inventory, but where nothing was slotted.</span></span> <span data-ttu-id="d1fc5-221">その後、テンプレートが再度実行されます。</span><span class="sxs-lookup"><span data-stu-id="d1fc5-221">The template is then run again.</span></span> <span data-ttu-id="d1fc5-222">今回は、場所の在庫が無視されます。</span><span class="sxs-lookup"><span data-stu-id="d1fc5-222">This time, it ignores the inventory in the locations.</span></span> <span data-ttu-id="d1fc5-223">この機能は、**スロット基準の割り当て** フィールドが _数量を考慮_ に設定されている場合に最も有効です。</span><span class="sxs-lookup"><span data-stu-id="d1fc5-223">This functionality works best when the **Assign slot criteria** field is set to _Consider qty_.</span></span>

    - <span data-ttu-id="d1fc5-224">**固定の場所の使用:** _製品の固定された場所のみ_</span><span class="sxs-lookup"><span data-stu-id="d1fc5-224">**Fixed location usage:** _Only fixed locations for the product_</span></span>

        <span data-ttu-id="d1fc5-225">以下の値は、このフィールドで使用できます。</span><span class="sxs-lookup"><span data-stu-id="d1fc5-225">The following values are available in this field:</span></span>

        - <span data-ttu-id="d1fc5-226">**固定の場所および固定されていない場所** –システムは、固定場所のみを使用するように制限することはできません。</span><span class="sxs-lookup"><span data-stu-id="d1fc5-226">**Fixed and non-fixed locations** – The system should not be limited to using only fixed locations.</span></span>
        - <span data-ttu-id="d1fc5-227">**製品の固定された場所のみ** – システムは、製品の固定された場所である場所に対してのみスロットを使用する必要があります。</span><span class="sxs-lookup"><span data-stu-id="d1fc5-227">**Only fixed locations for the product** – The system should slot only to locations that are fixed locations for the product.</span></span>
        - <span data-ttu-id="d1fc5-228">**製品バリアントの固定された場所のみ** – システムは、製品バリアントの固定された場所である場所に対してのみスロットを使用する必要があります。</span><span class="sxs-lookup"><span data-stu-id="d1fc5-228">**Only fixed locations for the product variant** – The system should slot only to locations that are fixed locations for the product variant.</span></span>

> [!NOTE]
> <span data-ttu-id="d1fc5-229">スロッティング テンプレートに 1 つ以上の行が含まれていて、**スロット基準の割り当て** フィールドが *手持在庫を考慮* に設定されている場合、テンプレートのどの行に対しても緩和は使用できなくなります。</span><span class="sxs-lookup"><span data-stu-id="d1fc5-229">If the slotting template contains at least one line where the **Assign slot criteria** field is set to *Consider on-hand*, let-ups are no longer allowed for any line in the template.</span></span>

1. <span data-ttu-id="d1fc5-230">**保存** を選択します。</span><span class="sxs-lookup"><span data-stu-id="d1fc5-230">Select **Save**.</span></span>
1. <span data-ttu-id="d1fc5-231">**新規** を選択して、テンプレートの 2 行目を追加します。</span><span class="sxs-lookup"><span data-stu-id="d1fc5-231">Select **New** to create a second template line.</span></span>
1. <span data-ttu-id="d1fc5-232">新しい明細行で、次の値を設定します。</span><span class="sxs-lookup"><span data-stu-id="d1fc5-232">On the new line, set the following values:</span></span>

    - <span data-ttu-id="d1fc5-233">**シーケンス:** _2_</span><span class="sxs-lookup"><span data-stu-id="d1fc5-233">**Sequence:** _2_</span></span>
    - <span data-ttu-id="d1fc5-234">**説明:** _その他_</span><span class="sxs-lookup"><span data-stu-id="d1fc5-234">**Description:** _Other_</span></span>
    - <span data-ttu-id="d1fc5-235">**最小数量:** _1_</span><span class="sxs-lookup"><span data-stu-id="d1fc5-235">**Minimum Qty:** _1_</span></span>
    - <span data-ttu-id="d1fc5-236">**最大数量:** _1000000_</span><span class="sxs-lookup"><span data-stu-id="d1fc5-236">**Maximum Qty:** _1000000_</span></span>
    - <span data-ttu-id="d1fc5-237">**ユニット:** このフィールドは空白のままにします。</span><span class="sxs-lookup"><span data-stu-id="d1fc5-237">**Unit:** Leave this field blank.</span></span>
    - <span data-ttu-id="d1fc5-238">**測定単位層:** _EaBoxPl_</span><span class="sxs-lookup"><span data-stu-id="d1fc5-238">**Unit of measure tier:** _EaBoxPl_</span></span>
    - <span data-ttu-id="d1fc5-239">**スロット基準の割り当て:** _数量を考慮_</span><span class="sxs-lookup"><span data-stu-id="d1fc5-239">**Assign slot criteria:** _Consider qty_</span></span>
    - <span data-ttu-id="d1fc5-240">**ディレクティブ コード:** _スロッティング_</span><span class="sxs-lookup"><span data-stu-id="d1fc5-240">**Directive code:** _Slotting_</span></span>
    - <span data-ttu-id="d1fc5-241">**オーバーフローの場所:** このフィールドは空白のままにします。</span><span class="sxs-lookup"><span data-stu-id="d1fc5-241">**Overflow location:** Leave this field blank.</span></span>
    - <span data-ttu-id="d1fc5-242">**停止の許可:** _はい_</span><span class="sxs-lookup"><span data-stu-id="d1fc5-242">**Allow let up:** _Yes_</span></span>
    - <span data-ttu-id="d1fc5-243">**固定の場所の使用:** _固定の場所および固定されていない場所_</span><span class="sxs-lookup"><span data-stu-id="d1fc5-243">**Use fixed locations:** _Fixed and non-fixed locations_</span></span>

    <span data-ttu-id="d1fc5-244">2 行目のクエリでは、この行の需要をスロット化できる場所を決定するために使用される基準を指定できるようになりました。</span><span class="sxs-lookup"><span data-stu-id="d1fc5-244">In the query for the second line, you will now specify the criteria that are used to determine what locations the demand for that line can be slotted to.</span></span>

1. <span data-ttu-id="d1fc5-245">**シーケンス** フィールドが *2* に設定されている行を選択します。</span><span class="sxs-lookup"><span data-stu-id="d1fc5-245">Select the line where the **Sequence** field is set to *2*.</span></span>
1. <span data-ttu-id="d1fc5-246">**クエリの編集** を選択します。</span><span class="sxs-lookup"><span data-stu-id="d1fc5-246">Select **Edit query**.</span></span>
1. <span data-ttu-id="d1fc5-247">**範囲** タブで、**追加** を選択してグリッドに新しい行を追加します。</span><span class="sxs-lookup"><span data-stu-id="d1fc5-247">On the **Range** tab, select **Add** to add a line to the grid.</span></span>
1. <span data-ttu-id="d1fc5-248">新しい明細行で、次の値を設定します。</span><span class="sxs-lookup"><span data-stu-id="d1fc5-248">On the new line, set the following values:</span></span>

    - <span data-ttu-id="d1fc5-249">**テーブル:** *場所*</span><span class="sxs-lookup"><span data-stu-id="d1fc5-249">**Table:** *Locations*</span></span>
    - <span data-ttu-id="d1fc5-250">**派生テーブル:** *場所*</span><span class="sxs-lookup"><span data-stu-id="d1fc5-250">**Derived table:** *Locations*</span></span>
    - <span data-ttu-id="d1fc5-251">\**フィールド:\*\*\*場所のプロファイル ID*</span><span class="sxs-lookup"><span data-stu-id="d1fc5-251">**Field:** *Location profile ID*</span></span>
    - <span data-ttu-id="d1fc5-252">**基準:** *Pick-06* (フィールドでダブル プラス記号 \[**++**\] を選択して一覧を展開し、*Pick-06* - *ピッキング サイト 6* を選択します。)</span><span class="sxs-lookup"><span data-stu-id="d1fc5-252">**Criteria:** *Pick-06* (Select the double plus sign \[**++**\] in the field to expand the list, and then select *Pick-06* - *Picking Site 6*.)</span></span>

1. <span data-ttu-id="d1fc5-253">**OK** を選択します。</span><span class="sxs-lookup"><span data-stu-id="d1fc5-253">Select **OK**.</span></span>

#### <a name="set-up-location-directives"></a><span data-ttu-id="d1fc5-254">場所ディレクティブを設定します</span><span class="sxs-lookup"><span data-stu-id="d1fc5-254">Set up location directives</span></span>

<span data-ttu-id="d1fc5-255">スロッティング ピックをサポートするには、少なくとも 1 つの場所のディレクティブを設定する必要があります。</span><span class="sxs-lookup"><span data-stu-id="d1fc5-255">At least one location directive must be set up to support slotting picks.</span></span> <span data-ttu-id="d1fc5-256">スロッティング ピックの新しい *補充場所のディレクティブ* を設定するには、このセクションの手順を使用します。</span><span class="sxs-lookup"><span data-stu-id="d1fc5-256">Use the procedures in this section to set up a new *replenishment location directive* for slotting picks.</span></span>

1. <span data-ttu-id="d1fc5-257">**倉庫管理 \> 設定 \> 場所のディレクティブ** に移動します。</span><span class="sxs-lookup"><span data-stu-id="d1fc5-257">Go to **Warehouse management \> Setup \> Location directives**.</span></span>
1. <span data-ttu-id="d1fc5-258">左ウィンドウで、**作業指示タイプ** フィールドを *補充* に設定します。</span><span class="sxs-lookup"><span data-stu-id="d1fc5-258">In the left pane, in the **Work order type** field, select *Replenishment*.</span></span>
1. <span data-ttu-id="d1fc5-259">アクション ウィンドウで、**新規** を選択します。</span><span class="sxs-lookup"><span data-stu-id="d1fc5-259">On the Action Pane, select **New**.</span></span>
1. <span data-ttu-id="d1fc5-260">新しい場所のヘッダーで、**名前** フィールドに *61 スロッティング ピック* と入力します。</span><span class="sxs-lookup"><span data-stu-id="d1fc5-260">In the header for the new location directive, in the **Name** field, enter *61 Slotting pick*.</span></span>
1. <span data-ttu-id="d1fc5-261">**シーケンス番号** フィールドで、既定値を受け入れます。</span><span class="sxs-lookup"><span data-stu-id="d1fc5-261">In the **Sequence number** field, accept the default value.</span></span>

##### <a name="configure-the-location-directives-fasttab"></a><span data-ttu-id="d1fc5-262">場所のディレクティブ クイック タブのコンフィギュレーション</span><span class="sxs-lookup"><span data-stu-id="d1fc5-262">Configure the Location directives FastTab</span></span>

1. <span data-ttu-id="d1fc5-263">**場所のディレクティブ** クイック タブで、次の値を設定します。</span><span class="sxs-lookup"><span data-stu-id="d1fc5-263">On the **Location directives** FastTab, set the following values.</span></span> <span data-ttu-id="d1fc5-264">他のすべてのフィールドの既定値を受け入れます。</span><span class="sxs-lookup"><span data-stu-id="d1fc5-264">Accept the default values for all other fields.</span></span>

    - <span data-ttu-id="d1fc5-265">**作業タイプ:** _ピッキング_</span><span class="sxs-lookup"><span data-stu-id="d1fc5-265">**Work type:** _Pick_</span></span>
    - <span data-ttu-id="d1fc5-266">**サイト:** _6_</span><span class="sxs-lookup"><span data-stu-id="d1fc5-266">**Site:** _6_</span></span>
    - <span data-ttu-id="d1fc5-267">**倉庫:** _61_</span><span class="sxs-lookup"><span data-stu-id="d1fc5-267">**Warehouse:** _61_</span></span>
    - <span data-ttu-id="d1fc5-268">**ディレクティブ コード:** _スロッティング_</span><span class="sxs-lookup"><span data-stu-id="d1fc5-268">**Directive code:** _Slotting_</span></span>

1. <span data-ttu-id="d1fc5-269">**保存** を選択して、**明細行** クイック タブを使用できるようにします。</span><span class="sxs-lookup"><span data-stu-id="d1fc5-269">Select **Save** to make the **Lines** FastTab available.</span></span>

##### <a name="configure-the-lines-fasttab"></a><span data-ttu-id="d1fc5-270">明細行クイック タブのコンフィギュレーション</span><span class="sxs-lookup"><span data-stu-id="d1fc5-270">Configure the Lines FastTab</span></span>

1. <span data-ttu-id="d1fc5-271">**明細行** クイック タブで、**新規** をクリックして明細行を作成します。</span><span class="sxs-lookup"><span data-stu-id="d1fc5-271">On the **Lines** FastTab, select **New** to create a line.</span></span>
1. <span data-ttu-id="d1fc5-272">新しい行で、次の値を設定します。</span><span class="sxs-lookup"><span data-stu-id="d1fc5-272">On the new line, set the following values.</span></span>

    - <span data-ttu-id="d1fc5-273">**開始数量:** _0_</span><span class="sxs-lookup"><span data-stu-id="d1fc5-273">**From quantity:** _0_</span></span>
    - <span data-ttu-id="d1fc5-274">**上限数量:** _1000000_</span><span class="sxs-lookup"><span data-stu-id="d1fc5-274">**To quantity:** _1000000_</span></span>

1. <span data-ttu-id="d1fc5-275">残りのフィールドに対しては規定値を受け入れます。</span><span class="sxs-lookup"><span data-stu-id="d1fc5-275">Accept the default values for the remaining fields.</span></span>
1. <span data-ttu-id="d1fc5-276">**保存** を選択して、**場所ディレクティブ アクション** クイック タブを使用できるようにします。</span><span class="sxs-lookup"><span data-stu-id="d1fc5-276">Select **Save** to make the **Location Directive Actions** FastTab available.</span></span>

##### <a name="configure-the-location-directive-actions-fasttab"></a><span data-ttu-id="d1fc5-277">場所ディレクティブ アクション クイック タブのコンフィギュレーション</span><span class="sxs-lookup"><span data-stu-id="d1fc5-277">Configure the Location Directive Actions FastTab</span></span>

1. <span data-ttu-id="d1fc5-278">**場所ディレクティブ アクション** クイック タブで、**新規** を選択して明細行を作成します。</span><span class="sxs-lookup"><span data-stu-id="d1fc5-278">On the **Location Directive Actions** FastTab, select **New** to create a line.</span></span>
1. <span data-ttu-id="d1fc5-279">新しい行で、次の値を設定します。</span><span class="sxs-lookup"><span data-stu-id="d1fc5-279">On the new line, set the following values.</span></span> <span data-ttu-id="d1fc5-280">他のすべてのフィールドの既定値を受け入れます。</span><span class="sxs-lookup"><span data-stu-id="d1fc5-280">Accept the default values for all other fields.</span></span>

    - <span data-ttu-id="d1fc5-281">**シーケンス番号:** 規定値を受け入れます。</span><span class="sxs-lookup"><span data-stu-id="d1fc5-281">**Sequence number:** Accept the default value.</span></span>
    - <span data-ttu-id="d1fc5-282">**名前:** _バルク_</span><span class="sxs-lookup"><span data-stu-id="d1fc5-282">**Name:** _Bulk_</span></span>
    - <span data-ttu-id="d1fc5-283">**戦略:** _なし_</span><span class="sxs-lookup"><span data-stu-id="d1fc5-283">**Strategy:** _None_</span></span>

1. <span data-ttu-id="d1fc5-284">残りのフィールドに対しては規定値を受け入れます。</span><span class="sxs-lookup"><span data-stu-id="d1fc5-284">Accept the default values for the remaining fields.</span></span>
1. <span data-ttu-id="d1fc5-285">**保存** を選択すると、**クエリの編集** ボタンが使用できるようになります。</span><span class="sxs-lookup"><span data-stu-id="d1fc5-285">Select **Save** to make the **Edit query** button available.</span></span>

##### <a name="edit-the-query"></a><span data-ttu-id="d1fc5-286">クエリを編集します</span><span class="sxs-lookup"><span data-stu-id="d1fc5-286">Edit the query</span></span>

1. <span data-ttu-id="d1fc5-287">**場所ディレクティブ アクション** クイック タブで、**クエリの編集** を選択します。</span><span class="sxs-lookup"><span data-stu-id="d1fc5-287">On the **Location Directive Actions** FastTab, select **Edit query**.</span></span>
1. <span data-ttu-id="d1fc5-288">**範囲** タブで、**追加** を選択してグリッドに新しい行を追加します。</span><span class="sxs-lookup"><span data-stu-id="d1fc5-288">On the **Range** tab, select **Add** to add a line to the grid.</span></span>
1. <span data-ttu-id="d1fc5-289">新しい明細行で、次の値を設定します。</span><span class="sxs-lookup"><span data-stu-id="d1fc5-289">On the new line, set the following values:</span></span>

    - <span data-ttu-id="d1fc5-290">**テーブル:** *場所*</span><span class="sxs-lookup"><span data-stu-id="d1fc5-290">**Table:** *Locations*</span></span>
    - <span data-ttu-id="d1fc5-291">**派生テーブル:** *場所*</span><span class="sxs-lookup"><span data-stu-id="d1fc5-291">**Derived table:** *Locations*</span></span>
    - <span data-ttu-id="d1fc5-292">**フィールド:** *ゾーン ID*</span><span class="sxs-lookup"><span data-stu-id="d1fc5-292">**Field:** *Zone ID*</span></span>
    - <span data-ttu-id="d1fc5-293">**基準:** *バルク* (フィールドでダブルプラス記号 \[**++**\] を選択して一覧を展開し、*バルク* を選択します。)</span><span class="sxs-lookup"><span data-stu-id="d1fc5-293">**Criteria:** *Bulk* (Select the double plus sign \[**++**\] in the field to expand the list, and then select *Bulk*.)</span></span>

1. <span data-ttu-id="d1fc5-294">**OK** を選択します。</span><span class="sxs-lookup"><span data-stu-id="d1fc5-294">Select **OK**.</span></span>

## <a name="scenario"></a><span data-ttu-id="d1fc5-295">シナリオ</span><span class="sxs-lookup"><span data-stu-id="d1fc5-295">Scenario</span></span>

### <a name="set-up-the-scenario"></a><span data-ttu-id="d1fc5-296">シナリオを設定する</span><span class="sxs-lookup"><span data-stu-id="d1fc5-296">Set up the scenario</span></span>

<span data-ttu-id="d1fc5-297">このシナリオでは、組み込みのサンプル データを使用して、このセクションで説明されているレコードを作成します。</span><span class="sxs-lookup"><span data-stu-id="d1fc5-297">For this scenario, use the built-in sample data, and create the records that are described in this section.</span></span>

#### <a name="use-the-usmf-sample-data"></a><span data-ttu-id="d1fc5-298">USMF サンプル データの使用</span><span class="sxs-lookup"><span data-stu-id="d1fc5-298">Use the USMF sample data</span></span>

<span data-ttu-id="d1fc5-299">ここで指定されたサンプル レコードと値を使用してシナリオを実行するには、標準[デモ データ](../../fin-ops-core/dev-itpro/deployment/deploy-demo-environment.md) がインストールされているシステムを使用する必要があります。</span><span class="sxs-lookup"><span data-stu-id="d1fc5-299">To work through this scenario by using the sample records and values that are specified here, you must be on a system where the standard [demo data](../../fin-ops-core/dev-itpro/deployment/deploy-demo-environment.md) is installed.</span></span> <span data-ttu-id="d1fc5-300">また、開始する前に **USMF** 法人を選択する必要があります。</span><span class="sxs-lookup"><span data-stu-id="d1fc5-300">Additionally, you must select the **USMF** legal entity before you begin.</span></span>

#### <a name="create-demand"></a><span data-ttu-id="d1fc5-301">需要の作成</span><span class="sxs-lookup"><span data-stu-id="d1fc5-301">Create demand</span></span>

<span data-ttu-id="d1fc5-302">スロッティングに適用する需要を作成するには、次の手順に従います。</span><span class="sxs-lookup"><span data-stu-id="d1fc5-302">Follow these steps to create the demand that you will apply slotting to.</span></span>

1. <span data-ttu-id="d1fc5-303">**販売とマーケティング \> 販売注文 \> すべての販売注文** の順に移動します。</span><span class="sxs-lookup"><span data-stu-id="d1fc5-303">Go to **Sales and marketing \> Sales orders \> All sales order**.</span></span>
1. <span data-ttu-id="d1fc5-304">**新規** を選択して新しい販売注文を作成します。</span><span class="sxs-lookup"><span data-stu-id="d1fc5-304">Select **New** to create a sales order.</span></span>
1. <span data-ttu-id="d1fc5-305">**販売注文の作成** ダイアログ ボックスの **顧客 ID** フィールドで、_US-007_ を選択します。</span><span class="sxs-lookup"><span data-stu-id="d1fc5-305">In the **Create sales order** dialog box, in the **Customer account** field, select _US-007_.</span></span>
1. <span data-ttu-id="d1fc5-306">**倉庫** フィールドで、_61_ を選択します。</span><span class="sxs-lookup"><span data-stu-id="d1fc5-306">In the **Warehouse** field, select _61_.</span></span>
1. <span data-ttu-id="d1fc5-307">**OK** を選択します。</span><span class="sxs-lookup"><span data-stu-id="d1fc5-307">Select **OK**.</span></span>
1. <span data-ttu-id="d1fc5-308">新しい販売注文が開かれます。</span><span class="sxs-lookup"><span data-stu-id="d1fc5-308">The new sales order is opened.</span></span> <span data-ttu-id="d1fc5-309">**販売注文行** クイック タブに空の明細行が含まれています。</span><span class="sxs-lookup"><span data-stu-id="d1fc5-309">It includes an empty line on the **Sales order lines** FastTab.</span></span> <span data-ttu-id="d1fc5-310">この明細行で、次の値を設定します。</span><span class="sxs-lookup"><span data-stu-id="d1fc5-310">On this line, set the following values:</span></span>

    - <span data-ttu-id="d1fc5-311">**品目:** _L0101_</span><span class="sxs-lookup"><span data-stu-id="d1fc5-311">**Item:** _L0101_</span></span>
    - <span data-ttu-id="d1fc5-312">**数量:** _20_</span><span class="sxs-lookup"><span data-stu-id="d1fc5-312">**Quantity:** _20_</span></span>

1. <span data-ttu-id="d1fc5-313">**行の追加** を選択して新しい行を追加し、次の値を設定します。</span><span class="sxs-lookup"><span data-stu-id="d1fc5-313">Select **Add line** to add a new line, and set the following values:</span></span>

    - <span data-ttu-id="d1fc5-314">**品目:** _T0100_</span><span class="sxs-lookup"><span data-stu-id="d1fc5-314">**Item:** _T0100_</span></span>
    - <span data-ttu-id="d1fc5-315">**数量:** _8_</span><span class="sxs-lookup"><span data-stu-id="d1fc5-315">**Quantity:** _8_</span></span>

1. <span data-ttu-id="d1fc5-316">**保存** を選択します。</span><span class="sxs-lookup"><span data-stu-id="d1fc5-316">Select **Save**.</span></span>
1. <span data-ttu-id="d1fc5-317">**新規** を選択して 2 番目の販売注文を作成します。</span><span class="sxs-lookup"><span data-stu-id="d1fc5-317">Select **New** to create a second sales order.</span></span>
1. <span data-ttu-id="d1fc5-318">**販売注文の作成** ダイアログ ボックスの **顧客 ID** フィールドで、_US-008_ を選択します。</span><span class="sxs-lookup"><span data-stu-id="d1fc5-318">In the **Create sales order** dialog box, in the **Customer account** field, select _US-008_.</span></span>
1. <span data-ttu-id="d1fc5-319">**倉庫** フィールドで、_61_ を選択します。</span><span class="sxs-lookup"><span data-stu-id="d1fc5-319">In the **Warehouse** field, select _61_.</span></span>
1. <span data-ttu-id="d1fc5-320">新しい販売注文が開かれます。</span><span class="sxs-lookup"><span data-stu-id="d1fc5-320">The new sales order is opened.</span></span> <span data-ttu-id="d1fc5-321">**販売注文行** クイック タブに空の明細行が含まれています。</span><span class="sxs-lookup"><span data-stu-id="d1fc5-321">It includes an empty line on the **Sales order lines** FastTab.</span></span> <span data-ttu-id="d1fc5-322">この明細行で、次の値を設定します。</span><span class="sxs-lookup"><span data-stu-id="d1fc5-322">On this line, set the following values:</span></span>

    - <span data-ttu-id="d1fc5-323">**品目:** _T0100_</span><span class="sxs-lookup"><span data-stu-id="d1fc5-323">**Item:** _T0100_</span></span>
    - <span data-ttu-id="d1fc5-324">**数量:** _1_</span><span class="sxs-lookup"><span data-stu-id="d1fc5-324">**Quantity:** _1_</span></span>

1. <span data-ttu-id="d1fc5-325">**保存** を選択します。</span><span class="sxs-lookup"><span data-stu-id="d1fc5-325">Select **Save**.</span></span>

### <a name="walk-through-a-typical-slotting-scenario"></a><span data-ttu-id="d1fc5-326">標準的なスロッティングのシナリオを説明していきます</span><span class="sxs-lookup"><span data-stu-id="d1fc5-326">Walk through a typical slotting scenario</span></span>

<span data-ttu-id="d1fc5-327">前のセクションで説明したように、すべての前提条件要素が満たされた後、このセクションの各練習を通じて、この機能を試すことができるようになります。</span><span class="sxs-lookup"><span data-stu-id="d1fc5-327">After all the prerequisite elements are in place, as described in the previous section, you're ready to try out the feature by working through each exercise in this section.</span></span>

#### <a name="generate-demand"></a><span data-ttu-id="d1fc5-328">要求の生成</span><span class="sxs-lookup"><span data-stu-id="d1fc5-328">Generate demand</span></span>

1. <span data-ttu-id="d1fc5-329">**倉庫管理 \> 設定 \> 補充 \> スロッティング テンプレート** の順に移動し、先ほど作成したスロッティング テンプレートを選択します。</span><span class="sxs-lookup"><span data-stu-id="d1fc5-329">Go to **Warehouse management \> Setup \> Replenishment \> Slotting templates**, and select the slotting template that you created earlier.</span></span>
1. <span data-ttu-id="d1fc5-330">アクション ウィンドウで、**需要の生成** を選択します。</span><span class="sxs-lookup"><span data-stu-id="d1fc5-330">On the Action Pane, select **Generate demand**.</span></span> <span data-ttu-id="d1fc5-331">このコマンドは、システム内のすべての需要の中で、スロッティング テンプレートのクエリに一致する需要を評価します。</span><span class="sxs-lookup"><span data-stu-id="d1fc5-331">This command evaluates all demand that is in the system, and that matches the slotting template query.</span></span> <span data-ttu-id="d1fc5-332">すべての注文の合計需要が、数量/測定単位ごとに 1 つの行に連結されます。</span><span class="sxs-lookup"><span data-stu-id="d1fc5-332">The total demand across all orders is then consolidated onto one line per quantity/unit of measure.</span></span> <span data-ttu-id="d1fc5-333">プロセスが完了すると、情報メッセージが表示されます。</span><span class="sxs-lookup"><span data-stu-id="d1fc5-333">An informational message appears when the process is completed.</span></span>

#### <a name="slotting-demand"></a><span data-ttu-id="d1fc5-334">スロッティングの要求</span><span class="sxs-lookup"><span data-stu-id="d1fc5-334">Slotting demand</span></span>

<span data-ttu-id="d1fc5-335">*スロッティングの需要* はスロッティング テンプレートの設定に基づいて、需要生成の結果を示します。</span><span class="sxs-lookup"><span data-stu-id="d1fc5-335">The *slotting demand* shows the results of demand generation, based on the setup of the slotting template.</span></span>

- <span data-ttu-id="d1fc5-336">アクション ウィンドウで、**スロッティングの需要** を選択して、**需要生成** コマンドの結果を表示します。</span><span class="sxs-lookup"><span data-stu-id="d1fc5-336">On the Action Pane, select **Slotting demand** to view the results from the **Generate demand** command.</span></span> <span data-ttu-id="d1fc5-337">スロッティングの需要の明細行は編集できます。</span><span class="sxs-lookup"><span data-stu-id="d1fc5-337">The lines in the slotting demand can be edited.</span></span> <span data-ttu-id="d1fc5-338">明細行を削除したり、新しい明細行を追加したり、行の詳細を編集したりすることができます。</span><span class="sxs-lookup"><span data-stu-id="d1fc5-338">You can delete a line, add a new line, or edit the line details.</span></span>

> [!NOTE]
> <span data-ttu-id="d1fc5-339">需要を手動で編集したり、データ管理を使用して外部システムからインポートしたりすることができます。</span><span class="sxs-lookup"><span data-stu-id="d1fc5-339">You can edit demand manually, or you can import it from an external system by using data management.</span></span> <span data-ttu-id="d1fc5-340">スロッティングの需要については、どこから入手したかにかかわらず、次の手順で使用されます。</span><span class="sxs-lookup"><span data-stu-id="d1fc5-340">Whatever is in the slotting demand will be used in the next step, regardless of where it came from.</span></span>

#### <a name="locate-demand"></a><span data-ttu-id="d1fc5-341">要求の特定</span><span class="sxs-lookup"><span data-stu-id="d1fc5-341">Locate demand</span></span>

<span data-ttu-id="d1fc5-342">需要が生成された後に、**需要の検索** コマンドを使用して *スロッティングの計画* を生成する必要があります。</span><span class="sxs-lookup"><span data-stu-id="d1fc5-342">After demand has been generated, you must use the **Locate demand** command to generate the *slotting plan*.</span></span>

- <span data-ttu-id="d1fc5-343">アクション ウィンドウで、**需要の検索** を選択します。</span><span class="sxs-lookup"><span data-stu-id="d1fc5-343">On the Action Pane, select **Locate demand**.</span></span> <span data-ttu-id="d1fc5-344">スロッティングのプロセスが実行されます。</span><span class="sxs-lookup"><span data-stu-id="d1fc5-344">The slotting process runs.</span></span> <span data-ttu-id="d1fc5-345">プロセスが完了すると、情報メッセージが表示されます。</span><span class="sxs-lookup"><span data-stu-id="d1fc5-345">An informational message appears when the process is completed.</span></span>

#### <a name="slotting-plan"></a><span data-ttu-id="d1fc5-346">スロッティングの計画</span><span class="sxs-lookup"><span data-stu-id="d1fc5-346">Slotting plan</span></span>

<span data-ttu-id="d1fc5-347">スロッティングの計画には、各品目または数量が割り当てられた場所、オーバーフローが使用されたかどうか、停止作業が作成されたかどうか、および使用されたテンプレート行が示されます。</span><span class="sxs-lookup"><span data-stu-id="d1fc5-347">The slotting plan shows the location that each item/quantity was assigned to, whether overflow was used, whether let-up work was created, and the template line that was used.</span></span> <span data-ttu-id="d1fc5-348">*スロット化できなかった需要は、赤で強調表示されます。*</span><span class="sxs-lookup"><span data-stu-id="d1fc5-348">*Any demand that could not be slotted is highlighted in red.*</span></span>

- <span data-ttu-id="d1fc5-349">アクション ウィンドウで、**スロッティングの計画** を選択して結果を表示します。</span><span class="sxs-lookup"><span data-stu-id="d1fc5-349">On the Action Pane, select **Slotting plan** to view the results.</span></span>

> [!NOTE]
> - <span data-ttu-id="d1fc5-350">これで、**需要の生成**、**需要の特定**、**補充の実行** プロセスがサンドボックスで実行されるようになります。</span><span class="sxs-lookup"><span data-stu-id="d1fc5-350">The **Generate demand**, **Locate demand**, and **Run replenishment** processes are now run in a sandbox.</span></span> <span data-ttu-id="d1fc5-351">(これらのプロセスは、**スロッティング テンプレート** ページのアクション ウィンドウから使用できます)。</span><span class="sxs-lookup"><span data-stu-id="d1fc5-351">(These processes are available from the Action Pane on the **Slotting templates** page.)</span></span>
> - <span data-ttu-id="d1fc5-352">**需要の生成**、**需要の特定**、および **補充の実行** プロセスには、それらが同時にトリガーされないようにするためのロックが設定されています。</span><span class="sxs-lookup"><span data-stu-id="d1fc5-352">The **Generate demand**, **Locate demand**, and **Run replenishment** processes have a lock to ensure that they can't be triggered at the same time.</span></span> <span data-ttu-id="d1fc5-353">そうしないと、使用されたデータは削除される可能性があります。</span><span class="sxs-lookup"><span data-stu-id="d1fc5-353">Otherwise, the data that is used could be deleted.</span></span>
> - <span data-ttu-id="d1fc5-354">実行でレコードが生成されなかった場合、またはレコードの情報が欠落している場合、**需要の生成** プロセスと **需要の特定** プロセスにより警告が表示されます。</span><span class="sxs-lookup"><span data-stu-id="d1fc5-354">The **Generate demand** and **Locate demand** processes show a warning if the run didn't generate records, or if the records are missing information.</span></span>
> - <span data-ttu-id="d1fc5-355">**スロッティング計画** を選択すると、データ ソースを編集できないので、ページのアクション ウィンドウに **新規**、**編集**、または **削除** ボタンはありません。</span><span class="sxs-lookup"><span data-stu-id="d1fc5-355">When you select **Slotting plan**, the page doesn't have **New**, **Edit**, or **Delete** buttons on the Action Pane, because the data source can't be edited.</span></span>
> - <span data-ttu-id="d1fc5-356">**補充の実行** を選択すると、選択したスロット テンプレートおよびプロセスがシステムによって検証されます。</span><span class="sxs-lookup"><span data-stu-id="d1fc5-356">When you select **Run replenishment**, the system validates the selected slot template and processes.</span></span>

#### <a name="create-replenishment"></a><span data-ttu-id="d1fc5-357">補充を作成する</span><span class="sxs-lookup"><span data-stu-id="d1fc5-357">Create replenishment</span></span>

<span data-ttu-id="d1fc5-358">スロッティングの計画を作成した後、計画に基づいて *補充作業* を作成する必要があります。</span><span class="sxs-lookup"><span data-stu-id="d1fc5-358">After the slotting plan has been created, you must create *replenishment work*, based on the plan.</span></span>

- <span data-ttu-id="d1fc5-359">アクション ウィンドウで、**補充の実行** を選択します。</span><span class="sxs-lookup"><span data-stu-id="d1fc5-359">On the Action Pane, select **Run replenishment**.</span></span> <span data-ttu-id="d1fc5-360">プロセスが完了すると、情報メッセージが表示されます。</span><span class="sxs-lookup"><span data-stu-id="d1fc5-360">An informational message appears when the process is completed.</span></span> <span data-ttu-id="d1fc5-361">このメッセージは、作業ビルド ID に対して作成されたヘッダーの数を示します。</span><span class="sxs-lookup"><span data-stu-id="d1fc5-361">This message indicates the number of headers that were created for the work build ID.</span></span>

<span data-ttu-id="d1fc5-362">使用されるロケーション ディレクティブは、各テンプレート行に指定されているディレクティブ コードに基づいて識別されます。</span><span class="sxs-lookup"><span data-stu-id="d1fc5-362">Location directives that will be used are identified based on the directive code that is specified on each template line.</span></span>

## <a name="tips"></a><span data-ttu-id="d1fc5-363">ヒント</span><span class="sxs-lookup"><span data-stu-id="d1fc5-363">Tips</span></span>

### <a name="set-up-automatic-slotting"></a><span data-ttu-id="d1fc5-364">自動スロッティングの設定</span><span class="sxs-lookup"><span data-stu-id="d1fc5-364">Set up automatic slotting</span></span>

<span data-ttu-id="d1fc5-365">必要な要素すべてを満たした後、次の手順に従って自動的に実行されるようにスロッティングを設定できます。</span><span class="sxs-lookup"><span data-stu-id="d1fc5-365">After all the required elements are in place, you can set up slotting to run automatically by following these steps.</span></span>

1. <span data-ttu-id="d1fc5-366">**倉庫管理 \> 補充 \> スロッティングの実行** の順に移動します。</span><span class="sxs-lookup"><span data-stu-id="d1fc5-366">Go to **Warehouse management \> Replenishment \> Run slotting**.</span></span>
1. <span data-ttu-id="d1fc5-367">実行するスロッティングの手順を指定します。</span><span class="sxs-lookup"><span data-stu-id="d1fc5-367">Specify the slotting steps to run.</span></span> <span data-ttu-id="d1fc5-368">1 つ以上の以下のスロッティングの手順を選択します。</span><span class="sxs-lookup"><span data-stu-id="d1fc5-368">Select one or more of the following slotting steps:</span></span>

    - <span data-ttu-id="d1fc5-369">要求の生成</span><span class="sxs-lookup"><span data-stu-id="d1fc5-369">Generate demand</span></span>
    - <span data-ttu-id="d1fc5-370">要求の特定</span><span class="sxs-lookup"><span data-stu-id="d1fc5-370">Locate demand</span></span>
    - <span data-ttu-id="d1fc5-371">補充作業の作成</span><span class="sxs-lookup"><span data-stu-id="d1fc5-371">Create replenishment work</span></span>

    > [!NOTE]
    > <span data-ttu-id="d1fc5-372">スロッティングの手順はプログレッシブです。</span><span class="sxs-lookup"><span data-stu-id="d1fc5-372">The slotting steps are progressive.</span></span> <span data-ttu-id="d1fc5-373">*需要の検索* を選択するには、最初に *需要の生成* を選択する必要があります。</span><span class="sxs-lookup"><span data-stu-id="d1fc5-373">If you want to select *Locate demand*, you must first select *Generate demand*.</span></span>

1. <span data-ttu-id="d1fc5-374">使用するスロッティングのテンプレートを指定します。</span><span class="sxs-lookup"><span data-stu-id="d1fc5-374">Specify the slotting template to use.</span></span>
1. <span data-ttu-id="d1fc5-375">必要に応じて繰り返し自動的に実行されるように設定します。</span><span class="sxs-lookup"><span data-stu-id="d1fc5-375">Set the recurrence to run automatically, if you want.</span></span>

<span data-ttu-id="d1fc5-376">シナリオの演習では、自動スロッティングを **しない** に設定してください。</span><span class="sxs-lookup"><span data-stu-id="d1fc5-376">For the exercises in the scenario, do **not** set up automatic slotting.</span></span>
