---
title: ゾーンしきい値の補充
description: ゾーンに基づいた補充では、最小/最大 (最小/最大) 補充方法が使用されますが、個々の場所ではなく、倉庫ゾーン全体が評価されます。 したがって、倉庫管理者はピッキング ゾーンで追加の在庫が必要になるタイミングをより迅速に知ることができます。
author: Mirzaab
manager: tfehr
ms.date: 07/01/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: mirzaab
ms.search.validFrom: 2020-07-01
ms.dyn365.ops.version: Release 10.0.8
ms.openlocfilehash: 7e9fdf0a546bf449f249eacdded1f4b4d1b4d1af
ms.sourcegitcommit: a7a7303004620d2e9cef0642b16d89163911dbb4
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 07/01/2020
ms.locfileid: "3530607"
---
# <a name="zone-threshold-replenishment"></a><span data-ttu-id="03f78-104">ゾーンしきい値の補充</span><span class="sxs-lookup"><span data-stu-id="03f78-104">Zone threshold replenishment</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="03f78-105">ゾーンに基づいた補充では、最小/最大 (最小/最大) [補充](replenishment.md) 方法が使用されますが、個々の場所ではなく、倉庫ゾーン全体が評価されます。</span><span class="sxs-lookup"><span data-stu-id="03f78-105">Zone-based replenishment uses a minimum/maximum (min/max) [replenishment](replenishment.md) strategy, but it evaluates whole warehouse zones instead of just individual locations.</span></span> <span data-ttu-id="03f78-106">したがって、倉庫管理者はピッキング ゾーンで追加の在庫が必要になるタイミングをより迅速に知ることができます。</span><span class="sxs-lookup"><span data-stu-id="03f78-106">Therefore, warehouse managers can more quickly learn when additional inventory is required in a picking zone.</span></span>

<span data-ttu-id="03f78-107">この機能の設定は、場所に基づく補充の設定に似ています。</span><span class="sxs-lookup"><span data-stu-id="03f78-107">The setup for this feature resembles the setup for location-based replenishment.</span></span> <span data-ttu-id="03f78-108">ただし、最小/最大補充用のテンプレートを設定する場合は、しきい値を場所ごとに評価するかゾーンごとに評価するかを指定することもできます。</span><span class="sxs-lookup"><span data-stu-id="03f78-108">However, when you set up a template for min/max replenishment, you can also specify whether the threshold should be evaluated per location or per zone.</span></span> <span data-ttu-id="03f78-109">ゾーンに基づく評価を設定する場合は、ゾーン選択クエリに特定のゾーンを追加する必要があります。</span><span class="sxs-lookup"><span data-stu-id="03f78-109">If you set up evaluation that is based on zones, you must add specific zones to the zone selection query.</span></span>

<span data-ttu-id="03f78-110">場所に基づく最小/最大の補充と同様に、ゾーンに基づく最小/最大の補充とは、選択された品目の補充作業の作成をトリガーする最小在庫しきい値の設定を基にしています。</span><span class="sxs-lookup"><span data-stu-id="03f78-110">Like location-based min/max replenishment, zone-based min/max replenishment is based the setup of a minimum inventory threshold that triggers the creation of replenishment work for selected items.</span></span> <span data-ttu-id="03f78-111">この補充作業により、在庫がゾーンの指定された最大しきい値まで増加します。</span><span class="sxs-lookup"><span data-stu-id="03f78-111">This replenishment work will increase inventory up to the specified maximum threshold for the zone.</span></span>

> [!NOTE]
> <span data-ttu-id="03f78-112">製品バリアントのゾーンの補充プロセスは、現在のリリースではサポートされていません。</span><span class="sxs-lookup"><span data-stu-id="03f78-112">Zone replenishment processes for product variants aren't supported in the current release.</span></span>


<span data-ttu-id="03f78-113">場所に基づく最小/最大補充とは異なり、ゾーンに基づく最小/最大補充では、場所が特定の品目を格納するかどうかを評価するために固定の場所を必要としません。</span><span class="sxs-lookup"><span data-stu-id="03f78-113">Unlike location-based min/max replenishment, zone-based min/max replenishment doesn't require fixed locations to evaluate whether locations should store a specific item.</span></span> <span data-ttu-id="03f78-114">したがって、ゾーンに基づく補充では、倉庫内の各品目または品目バリアントに対して固定の場所がない場合でも、最小/最大補充を使用できます。</span><span class="sxs-lookup"><span data-stu-id="03f78-114">Therefore, zone-based replenishment lets you use min/max replenishment even if you don't have fixed locations for each item or item variant in the warehouse.</span></span> <span data-ttu-id="03f78-115">ゾーンの数量が指定された最小しきい値を下回ると、補充作業が作成されます。</span><span class="sxs-lookup"><span data-stu-id="03f78-115">When a quantity in the zone falls below the specified minimum threshold, replenishment work is created.</span></span> <span data-ttu-id="03f78-116">場所のディレクティブによって、在庫が配置される特定の場所が決定されます。</span><span class="sxs-lookup"><span data-stu-id="03f78-116">Location directives will determine which specific location the inventory should be put into.</span></span>

## <a name="turn-on-the-zone-threshold-replenishment-feature"></a><span data-ttu-id="03f78-117">ゾーンしきい値の補充機能を有効にする</span><span class="sxs-lookup"><span data-stu-id="03f78-117">Turn on the Zone threshold replenishment feature</span></span>

<span data-ttu-id="03f78-118">*ゾーンしきい値の補充*機能を使用するには、システム上で有効にする必要があります。</span><span class="sxs-lookup"><span data-stu-id="03f78-118">Before you can use the *Zone threshold replenishment* feature, it must be turned on in your system.</span></span> <span data-ttu-id="03f78-119">管理者は、[機能の管理](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md)設定を使用して、機能の状態を確認し、必要に応じて有効にすることができます。</span><span class="sxs-lookup"><span data-stu-id="03f78-119">Admins can use the [feature management](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) settings to check the status of the feature and turn it on if it's required.</span></span> <span data-ttu-id="03f78-120">**機能管理** ワークスペースで、この機能は次のようにリストされています。</span><span class="sxs-lookup"><span data-stu-id="03f78-120">In the **Feature management** workspace, the feature is listed in the following way:</span></span>

- <span data-ttu-id="03f78-121">**モジュール:** *倉庫管理*</span><span class="sxs-lookup"><span data-stu-id="03f78-121">**Module:** *Warehouse management*</span></span>
- <span data-ttu-id="03f78-122">**機能名:** *ゾーンしきい値の補充*</span><span class="sxs-lookup"><span data-stu-id="03f78-122">**Feature name:** *Zone threshold replenishment*</span></span>

## <a name="set-up-zone-based-replenishment"></a><a name="setup"></a><span data-ttu-id="03f78-123">ゾーンに基づく補充の設定</span><span class="sxs-lookup"><span data-stu-id="03f78-123">Set up zone-based replenishment</span></span>

<span data-ttu-id="03f78-124">ゾーンに基づく補充を設定するには、システムのいくつかの部分をコンフィギュレーションする必要があります。</span><span class="sxs-lookup"><span data-stu-id="03f78-124">To set up zone-based replenishment, you must configure several parts of the system.</span></span> <span data-ttu-id="03f78-125">このセクションでは、さまざまな設定を紹介し、このトピックの最後にシナリオを実行する場合に入力できるデモ データの値を示します。</span><span class="sxs-lookup"><span data-stu-id="03f78-125">This section introduces the various settings and provides demo data values that you can enter if you want to work through the scenario at the end of this topic.</span></span>

### <a name="set-up-directive-codes"></a><span data-ttu-id="03f78-126">ディレクティブ コードの設定</span><span class="sxs-lookup"><span data-stu-id="03f78-126">Set up directive codes</span></span>

<span data-ttu-id="03f78-127">[ディレクティブ コード](control-warehouse-location-directives.md)では、作業テンプレートで使用する場所テンプレートを定義する際に、より具体的に指定することができます。</span><span class="sxs-lookup"><span data-stu-id="03f78-127">[Directive codes](control-warehouse-location-directives.md) let you be more specific when you define the location template that is used in a work template.</span></span> <span data-ttu-id="03f78-128">各コードでは、各タイプのテンプレートをコンフィギュレーションする際に参照できる共通の値を設定します。</span><span class="sxs-lookup"><span data-stu-id="03f78-128">Each code establishes a common value that you can refer to when you configure each type of template.</span></span>

#### <a name="view-and-edit-directive-codes"></a><span data-ttu-id="03f78-129">ディレクティブ コードの表示と編集</span><span class="sxs-lookup"><span data-stu-id="03f78-129">View and edit directive codes</span></span>

<span data-ttu-id="03f78-130">ディレクティブ コードを表示または編集するには、**倉庫管理\>設定\>ディレクティブ コード**に移動します。</span><span class="sxs-lookup"><span data-stu-id="03f78-130">To view or edit your directive codes, go to **Warehouse management \> Setup \> Directive codes**.</span></span>

#### <a name="prepare-demo-data-directive-codes"></a><span data-ttu-id="03f78-131">デモ データのディレクティブ コードの準備</span><span class="sxs-lookup"><span data-stu-id="03f78-131">Prepare demo data directive codes</span></span>

<span data-ttu-id="03f78-132">この例では、ディレクティブ コードを準備する方法を示します。</span><span class="sxs-lookup"><span data-stu-id="03f78-132">This example shows how to prepare a directive code.</span></span> <span data-ttu-id="03f78-133">このトピックの最後にあるシナリオを実行する場合は、ここで提供されているデモ データの値を使用します。</span><span class="sxs-lookup"><span data-stu-id="03f78-133">If you're planning to work through the scenario at the end of this topic, use the demo data values that are provided here.</span></span> <span data-ttu-id="03f78-134">それ以外の場合は、独自の値を使用します。</span><span class="sxs-lookup"><span data-stu-id="03f78-134">Otherwise, use your own values.</span></span>

1. <span data-ttu-id="03f78-135">**USMF** 法人を選択して、デモ データを操作します。</span><span class="sxs-lookup"><span data-stu-id="03f78-135">Select the **USMF** legal entity to work with the demo data.</span></span>
1. <span data-ttu-id="03f78-136">**倉庫管理 \> 設定 \> ディレクティブ コード**に移動します。</span><span class="sxs-lookup"><span data-stu-id="03f78-136">Go to **Warehouse management \> Setup \> Directive codes**.</span></span>
1. <span data-ttu-id="03f78-137">アクション ウィンドウで**新規**を選択して、行をグリッドに追加します。</span><span class="sxs-lookup"><span data-stu-id="03f78-137">On the Action Pane, select **New** to add a row to the grid.</span></span>
1. <span data-ttu-id="03f78-138">新しい行で、次の値を設定します。</span><span class="sxs-lookup"><span data-stu-id="03f78-138">In the new row, set the following values:</span></span>

    - <span data-ttu-id="03f78-139">**ディレクティブ コード:** _Zone replen_</span><span class="sxs-lookup"><span data-stu-id="03f78-139">**Directive code:** _Zone replen_</span></span>
    - <span data-ttu-id="03f78-140">**ディレクティブの説明:** _ゾーンの補充_</span><span class="sxs-lookup"><span data-stu-id="03f78-140">**Directive description:** _Zone replenishment_</span></span>

1. <span data-ttu-id="03f78-141">**保存**を選択して新しいコードを保存します。</span><span class="sxs-lookup"><span data-stu-id="03f78-141">Select **Save** to save the new code.</span></span>

### <a name="set-up-replenishment-templates"></a><span data-ttu-id="03f78-142">補充テンプレートを設定します</span><span class="sxs-lookup"><span data-stu-id="03f78-142">Set up replenishment templates</span></span>

<span data-ttu-id="03f78-143">[最小/最大補充のテンプレート](tasks/set-up-min-max-replenishment-process.md)は、ピッキング場所で最適なレベルを維持する上での主要なメカニズムです。</span><span class="sxs-lookup"><span data-stu-id="03f78-143">[Min/max replenishment templates](tasks/set-up-min-max-replenishment-process.md) are the primary mechanism for maintaining optimal levels in picking locations.</span></span> <span data-ttu-id="03f78-144">これらのテンプレートでは、倉庫での在庫の補充に使用されるルールを設定する必要があります。</span><span class="sxs-lookup"><span data-stu-id="03f78-144">In these templates, you must set up the rules that will be used to replenish inventory in the warehouse.</span></span> <span data-ttu-id="03f78-145">テンプレートを使用できる補充には、ゾーンに基づく補充が含まれます。</span><span class="sxs-lookup"><span data-stu-id="03f78-145">The replenishment that the templates can be used for includes zone-based replenishment.</span></span>

#### <a name="view-and-edit-replenishment-templates"></a><span data-ttu-id="03f78-146">補充テンプレートの表示と編集</span><span class="sxs-lookup"><span data-stu-id="03f78-146">View and edit replenishment templates</span></span>

<span data-ttu-id="03f78-147">補充テンプレートは、場所が補充されるタイミングと方法を制御するルールのセットです。</span><span class="sxs-lookup"><span data-stu-id="03f78-147">A replenishment template is a set of rules that control when and how a location is replenished.</span></span> <span data-ttu-id="03f78-148">テンプレートを選択して、補充を実行するタイミングと方法を制御します。</span><span class="sxs-lookup"><span data-stu-id="03f78-148">You select a template to control when and how replenishment is done.</span></span> <span data-ttu-id="03f78-149">補充テンプレートを表示または編集するには、**倉庫管理\>設定\>補充\>補充テンプレート**の順に移動します。</span><span class="sxs-lookup"><span data-stu-id="03f78-149">To view or edit your replenishment templates, go to **Warehouse management \> Setup \> Replenishment \> Replenishment templates**.</span></span>

#### <a name="prepare-a-demo-data-replenishment-template"></a><span data-ttu-id="03f78-150">デモ データの補充テンプレートの準備</span><span class="sxs-lookup"><span data-stu-id="03f78-150">Prepare a demo data replenishment template</span></span>

<span data-ttu-id="03f78-151">この例では、補充テンプレートを準備する方法を示します。</span><span class="sxs-lookup"><span data-stu-id="03f78-151">This example shows how to prepare a replenishment template.</span></span> <span data-ttu-id="03f78-152">このトピックの最後にあるシナリオを実行する場合は、ここで提供されているデモ データの値を使用します。</span><span class="sxs-lookup"><span data-stu-id="03f78-152">If you're planning to work through the scenario at the end of this topic, use the demo data values that are provided here.</span></span> <span data-ttu-id="03f78-153">それ以外の場合は、独自の値を使用します。</span><span class="sxs-lookup"><span data-stu-id="03f78-153">Otherwise, use your own values.</span></span>

1. <span data-ttu-id="03f78-154">**USMF** 法人を選択して、デモ データを操作します。</span><span class="sxs-lookup"><span data-stu-id="03f78-154">Select the **USMF** legal entity to work with the demo data.</span></span>
1. <span data-ttu-id="03f78-155">**倉庫管理\>設定\>補充\>補充テンプレート**の順に移動します。</span><span class="sxs-lookup"><span data-stu-id="03f78-155">Go to **Warehouse management \> Setup \> Replenishment \> Replenishment templates**.</span></span>
1. <span data-ttu-id="03f78-156">**編集**を選択し、ページを編集モードにします。</span><span class="sxs-lookup"><span data-stu-id="03f78-156">Select **Edit** to put the page into edit mode.</span></span>
1. <span data-ttu-id="03f78-157">アクション ペインで**新規**を選択して、行を**概要**グリッドに追加します。</span><span class="sxs-lookup"><span data-stu-id="03f78-157">On the Action Pane, select **New** to add a row to the **Overview** grid.</span></span>
1. <span data-ttu-id="03f78-158">新しい行で、次の値を設定します。</span><span class="sxs-lookup"><span data-stu-id="03f78-158">In the new row, set the following values.</span></span> <span data-ttu-id="03f78-159">他のすべてのフィールドの既定値を受け入れます。</span><span class="sxs-lookup"><span data-stu-id="03f78-159">Accept the default values for all other fields.</span></span>

    - <span data-ttu-id="03f78-160">**補充テンプレート:** _Zone min/max replen_</span><span class="sxs-lookup"><span data-stu-id="03f78-160">**Replenish template:** _Zone min/max replen_</span></span>
    - <span data-ttu-id="03f78-161">**説明:** _ゾーンの最小/最大補充_</span><span class="sxs-lookup"><span data-stu-id="03f78-161">**Description:** _Zone min/max replenishment_</span></span>
    - <span data-ttu-id="03f78-162">**補充タイプ:** _最小または最大_</span><span class="sxs-lookup"><span data-stu-id="03f78-162">**Replenishment type:** _Minimum or maximum_</span></span>

1. <span data-ttu-id="03f78-163">**保存** を選択します。</span><span class="sxs-lookup"><span data-stu-id="03f78-163">Select **Save**.</span></span>
1. <span data-ttu-id="03f78-164">**概要**グリッドで新しい行が選択されている状態で、**補充テンプレートの詳細**グリッドの上にある**新規**を選択し、作成した *Zone Min/Max replen* 補充テンプレートに関連付けられている行を追加します。</span><span class="sxs-lookup"><span data-stu-id="03f78-164">While the new row is still selected in the **Overview** grid, select **New** above the **Replenishment Template Details** grid to add a row that is associated with the *Zone Min/Max replen* replenishment template that you just created.</span></span>
1. <span data-ttu-id="03f78-165">新しい行で、次の値を設定します。</span><span class="sxs-lookup"><span data-stu-id="03f78-165">In the new row, set the following values:</span></span>

    - <span data-ttu-id="03f78-166">**シーケンス番号:** _1_ を入力します。</span><span class="sxs-lookup"><span data-stu-id="03f78-166">**Sequence number:** Enter _1_.</span></span>
    - <span data-ttu-id="03f78-167">**説明:** _ゾーン補充をピック_と入力します。</span><span class="sxs-lookup"><span data-stu-id="03f78-167">**Description:** Enter _Pick zone replenishment_.</span></span>
    - <span data-ttu-id="03f78-168">**補充単位:** _ea_ を選択します。</span><span class="sxs-lookup"><span data-stu-id="03f78-168">**Replenishment unit:** Select _ea_.</span></span>
    - <span data-ttu-id="03f78-169">**要求タイプ:** このフィールドは空白のままにします。</span><span class="sxs-lookup"><span data-stu-id="03f78-169">**Request type:** Leave this field blank.</span></span>
    - <span data-ttu-id="03f78-170">**ディレクティブ コード:** このフィールドは、補充テンプレートを場所のディレクティブにリンクします。</span><span class="sxs-lookup"><span data-stu-id="03f78-170">**Directive code:** This field links the replenishment template with a location directive.</span></span> <span data-ttu-id="03f78-171">作成済みのデモ データのディレクティブ コード (_Zone replen)_ を選択します。</span><span class="sxs-lookup"><span data-stu-id="03f78-171">Select the demo data directive code that you created earlier (_Zone replen_).</span></span>
    - <span data-ttu-id="03f78-172">**作業テンプレート** このフィールドは空白のままにしておきます。</span><span class="sxs-lookup"><span data-stu-id="03f78-172">**Work template:** Leave this field blank.</span></span>
    - <span data-ttu-id="03f78-173">**最小数量:** このフィールドは、補充がトリガーされる数量を設定します。</span><span class="sxs-lookup"><span data-stu-id="03f78-173">**Minimum quantity:** This field sets the quantity that replenishment will be triggered at.</span></span> <span data-ttu-id="03f78-174">_50_ と入力します。</span><span class="sxs-lookup"><span data-stu-id="03f78-174">Enter _50_.</span></span>
    - <span data-ttu-id="03f78-175">**最大数量:** このフィールドは、ゾーンに存在できる品目の最大数量を設定します。</span><span class="sxs-lookup"><span data-stu-id="03f78-175">**Maximum quantity:** This field sets the maximum quantity of an item that can be present in a zone.</span></span> <span data-ttu-id="03f78-176">生成された補充作業により、在庫がこの数量まで増加します。</span><span class="sxs-lookup"><span data-stu-id="03f78-176">Generated replenishment work will increase inventory to this quantity.</span></span> <span data-ttu-id="03f78-177">_150_ と入力します。</span><span class="sxs-lookup"><span data-stu-id="03f78-177">Enter _150_.</span></span>
    - <span data-ttu-id="03f78-178">**単位:** このフィールドでは、最小値と最大値の単位が設定されます。</span><span class="sxs-lookup"><span data-stu-id="03f78-178">**Unit:** This field sets the unit for the minimum and maximum values.</span></span> <span data-ttu-id="03f78-179">_ea_ を選択します。</span><span class="sxs-lookup"><span data-stu-id="03f78-179">Select _ea_.</span></span>
    - <span data-ttu-id="03f78-180">**需要の増加:**_切り上げ_を選択します。</span><span class="sxs-lookup"><span data-stu-id="03f78-180">**Demand increment:** Select _Round up_.</span></span>
    - <span data-ttu-id="03f78-181">**空の固定の場所を補充する:** このチェック ボックスをオンにします。</span><span class="sxs-lookup"><span data-stu-id="03f78-181">**Replenish empty fixed locations:** Select this check box.</span></span>
    - <span data-ttu-id="03f78-182">**固定の場所のみを補充する:** このチェック ボックスをオフにします。</span><span class="sxs-lookup"><span data-stu-id="03f78-182">**Replenish only fixed locations:** Clear this check box.</span></span>
    - <span data-ttu-id="03f78-183">**製品クエリ モード:** _製品クエリ_を選択します。</span><span class="sxs-lookup"><span data-stu-id="03f78-183">**Product query mode:** Select _Product query_.</span></span>
    - <span data-ttu-id="03f78-184">**補充のしきい値のスコープ:** このフィールドは、テンプレートをゾーン別に評価するか、特定の場所別に評価するかを定義します。</span><span class="sxs-lookup"><span data-stu-id="03f78-184">**Replenishment threshold scope:** This field defines whether the template should evaluate by zone or by specific location.</span></span> <span data-ttu-id="03f78-185">_ゾーン_を選択します。</span><span class="sxs-lookup"><span data-stu-id="03f78-185">Select _Zone_.</span></span>
    - <span data-ttu-id="03f78-186">**倉庫:** _61_ を選択します。</span><span class="sxs-lookup"><span data-stu-id="03f78-186">**Warehouse:** Select _61_.</span></span>

1. <span data-ttu-id="03f78-187">**補充テンプレートの詳細**グリッドの上にある**製品の選択**を選択します。</span><span class="sxs-lookup"><span data-stu-id="03f78-187">Select **Select products** above the **Replenishment Template Details** grid.</span></span>
1. <span data-ttu-id="03f78-188">**製品クエリ**ダイアログ ボックスの**範囲**タブで**追加**を選択して、グリッドに行を追加します。</span><span class="sxs-lookup"><span data-stu-id="03f78-188">In the **Product query** dialog box, on the **Range** tab, select **Add** to add a row to the grid.</span></span>
1. <span data-ttu-id="03f78-189">新しい行で、次の値を設定します。</span><span class="sxs-lookup"><span data-stu-id="03f78-189">In the new row, set the following values:</span></span>

    - <span data-ttu-id="03f78-190">**テーブル:** _品目_</span><span class="sxs-lookup"><span data-stu-id="03f78-190">**Table:** _Items_</span></span>
    - <span data-ttu-id="03f78-191">**派生テーブル:** _品目_</span><span class="sxs-lookup"><span data-stu-id="03f78-191">**Derived table:** _Items_</span></span>
    - <span data-ttu-id="03f78-192">**フィールド:** _品目番号_</span><span class="sxs-lookup"><span data-stu-id="03f78-192">**Field:** _Item number_</span></span>
    - <span data-ttu-id="03f78-193">**基準:** _A0001_</span><span class="sxs-lookup"><span data-stu-id="03f78-193">**Criteria:** _A0001_</span></span>

1. <span data-ttu-id="03f78-194">**OK** を選択してクエリを保存し、ダイアログ ボックスを閉じます。</span><span class="sxs-lookup"><span data-stu-id="03f78-194">Select **OK** to save your query and close the dialog box.</span></span>
1. <span data-ttu-id="03f78-195">**補充テンプレートの詳細**グリッドの上にある**補充するゾーンの選択**を選択します。</span><span class="sxs-lookup"><span data-stu-id="03f78-195">Select **Select zones to replenish** above the **Replenishment Template Details** grid.</span></span>
1. <span data-ttu-id="03f78-196">**ゾーン クエリ**ダイアログ ボックスの**範囲**タブで、グリッドに行を追加します。</span><span class="sxs-lookup"><span data-stu-id="03f78-196">In the **Zone query** dialog box, on the **Range** tab, add a row to the grid.</span></span>
1. <span data-ttu-id="03f78-197">新しい行で、次の値を設定します。</span><span class="sxs-lookup"><span data-stu-id="03f78-197">In the new row, set the following values:</span></span>

    - <span data-ttu-id="03f78-198">**テーブル:** _倉庫ゾーン_</span><span class="sxs-lookup"><span data-stu-id="03f78-198">**Table:** _Warehouse zone_</span></span>
    - <span data-ttu-id="03f78-199">**派生テーブル:** _倉庫ゾーン_</span><span class="sxs-lookup"><span data-stu-id="03f78-199">**Derived table:** _Warehouse zone_</span></span>
    - <span data-ttu-id="03f78-200">**フィールド:** _ゾーン ID_</span><span class="sxs-lookup"><span data-stu-id="03f78-200">**Field:** _Zone ID_</span></span>
    - <span data-ttu-id="03f78-201">**基準:** _FLOOR_</span><span class="sxs-lookup"><span data-stu-id="03f78-201">**Criteria:** _FLOOR_</span></span>

1. <span data-ttu-id="03f78-202">**OK** を選択してクエリを保存し、ダイアログ ボックスを閉じます。</span><span class="sxs-lookup"><span data-stu-id="03f78-202">Select **OK** to save your query and close the dialog box.</span></span>

### <a name="set-up-location-directives"></a><span data-ttu-id="03f78-203">場所ディレクティブを設定します</span><span class="sxs-lookup"><span data-stu-id="03f78-203">Set up location directives</span></span>

<span data-ttu-id="03f78-204">場所に基づく最小/最大補充とは異なり、ゾーンに基づく最小/最大補充では、システムが出荷作業のピック場所だけでなくゾーン全体を評価するため、ピック場所ディレクティブとプット場所ディレクティブの両方を設定する必要があります。</span><span class="sxs-lookup"><span data-stu-id="03f78-204">Unlike location-based min/max replenishment, zone-based min/max replenishment requires that you set up both pick location directives and put location directives, because the system evaluates the whole zone instead of just the pick location for outbound work.</span></span>

#### <a name="view-and-edit-location-directives"></a><span data-ttu-id="03f78-205">場所ディレクティブの表示と編集</span><span class="sxs-lookup"><span data-stu-id="03f78-205">View and edit location directives</span></span>

<span data-ttu-id="03f78-206">場所ディレクティブを表示または編集するには、**倉庫管理\>設定\>場所ディレクティブ**に移動します。</span><span class="sxs-lookup"><span data-stu-id="03f78-206">To view or edit your location directives, go to **Warehouse management \> Setup \> Location directives**.</span></span>

<span data-ttu-id="03f78-207">設定を使用して、必要なピック場所ディレクティブとプット場所ディレクティブを作成する方法の例については、次のセクションを参照してください。</span><span class="sxs-lookup"><span data-stu-id="03f78-207">For examples that show how to use the settings to create the required pick location directives and put location directives, see the next section.</span></span>

#### <a name="prepare-demo-data-location-directives"></a><span data-ttu-id="03f78-208">デモ データの場所ディレクティブの準備</span><span class="sxs-lookup"><span data-stu-id="03f78-208">Prepare demo data location directives</span></span>

<span data-ttu-id="03f78-209">デモ データを準備して、このトピックの最後にあるシナリオで使用できるようにするには、ピック用とプット用の 2 つの場所ディレクティブを作成する必要があります。</span><span class="sxs-lookup"><span data-stu-id="03f78-209">To prepare demo data so that it can be used in the scenario at the end of this topic, you must create two location directives: one for pick and one for put.</span></span>

##### <a name="create-a-replenishment-pick-directive"></a><span data-ttu-id="03f78-210">補充ピック ディレクティブの作成</span><span class="sxs-lookup"><span data-stu-id="03f78-210">Create a replenishment pick directive</span></span>

1. <span data-ttu-id="03f78-211">**USMF** 法人を選択して、デモ データを操作します。</span><span class="sxs-lookup"><span data-stu-id="03f78-211">Select the **USMF** legal entity to work with the demo data.</span></span>
1. <span data-ttu-id="03f78-212">**倉庫管理 \> 設定 \> 場所のディレクティブ** に移動します。</span><span class="sxs-lookup"><span data-stu-id="03f78-212">Go to **Warehouse management \> Setup \> Location directives**.</span></span>
1. <span data-ttu-id="03f78-213">左ウィンドウで、**作業指示のタイプ** フィールドを_補充_に設定します。</span><span class="sxs-lookup"><span data-stu-id="03f78-213">In the left pane, set the **Work order type** field to _Replenishment_.</span></span>
1. <span data-ttu-id="03f78-214">アクション ペインで、**新規**を選択して新しいディレクティブを作成します。</span><span class="sxs-lookup"><span data-stu-id="03f78-214">On the Action Pane, select **New** to create a new directive.</span></span>
1. <span data-ttu-id="03f78-215">次の値を設定します。</span><span class="sxs-lookup"><span data-stu-id="03f78-215">Set the following values:</span></span>

    - <span data-ttu-id="03f78-216">**シーケンス番号:** 規定値を受け入れます。</span><span class="sxs-lookup"><span data-stu-id="03f78-216">**Sequence number:** Accept the default value.</span></span>
    - <span data-ttu-id="03f78-217">**名前:** _ゾーン ピック_と入力します。</span><span class="sxs-lookup"><span data-stu-id="03f78-217">**Name:** Enter _Zone pick_.</span></span>
    - <span data-ttu-id="03f78-218">**作業タイプ:** _ピック_を選択します。</span><span class="sxs-lookup"><span data-stu-id="03f78-218">**Work type:** Select _Pick_.</span></span>
    - <span data-ttu-id="03f78-219">**サイト:** _6_ を選択します。</span><span class="sxs-lookup"><span data-stu-id="03f78-219">**Site:** Select _6_.</span></span>
    - <span data-ttu-id="03f78-220">**倉庫:** _61_ を選択します。</span><span class="sxs-lookup"><span data-stu-id="03f78-220">**Warehouse:** Select _61_.</span></span>
    - <span data-ttu-id="03f78-221">**ディレクティブ コード:** このフィールドは空白のままにします。</span><span class="sxs-lookup"><span data-stu-id="03f78-221">**Directive code:** Leave this field blank.</span></span>
    - <span data-ttu-id="03f78-222">**マルチ SKU:** このオプションを_いいえ_に設定します。</span><span class="sxs-lookup"><span data-stu-id="03f78-222">**Multi SKU:** Set this option to _No_.</span></span>

1. <span data-ttu-id="03f78-223">Select **保存**を選択して、これまでにコンフィギュレーションした設定を持つディレクティブを作成します。</span><span class="sxs-lookup"><span data-stu-id="03f78-223">Select **Save** to create a directive that has the settings that you've configured so far.</span></span>
1. <span data-ttu-id="03f78-224">**明細行**クイック タブで、**新規**を選択してグリッドに明細行を追加します。</span><span class="sxs-lookup"><span data-stu-id="03f78-224">On the **Lines** FastTab, select **New** to add a line to the grid.</span></span>
1. <span data-ttu-id="03f78-225">新しい明細行で、次の値を設定します。</span><span class="sxs-lookup"><span data-stu-id="03f78-225">On the new line, set the following values:</span></span>

    - <span data-ttu-id="03f78-226">**シーケンス番号:** _1_ を入力します。</span><span class="sxs-lookup"><span data-stu-id="03f78-226">**Sequence number:** Enter _1_.</span></span>
    - <span data-ttu-id="03f78-227">**開始数量:** _0_ と入力します。</span><span class="sxs-lookup"><span data-stu-id="03f78-227">**From quantity:** Enter _0_.</span></span>
    - <span data-ttu-id="03f78-228">**上限数量:** _10000000_ と入力します。</span><span class="sxs-lookup"><span data-stu-id="03f78-228">**To quantity:** Enter _10000000_.</span></span>
    - <span data-ttu-id="03f78-229">**ユニット:** このフィールドは空白のままにします。</span><span class="sxs-lookup"><span data-stu-id="03f78-229">**Unit:** Leave this field blank.</span></span>
    - <span data-ttu-id="03f78-230">**数量の検索:** _なし_を選択します。</span><span class="sxs-lookup"><span data-stu-id="03f78-230">**Locate quantity:** Select _None_.</span></span>
    - <span data-ttu-id="03f78-231">**単位ごとに制限:** このチェック ボックスをオフにします。</span><span class="sxs-lookup"><span data-stu-id="03f78-231">**Restrict by unit:** Clear this check box.</span></span>
    - <span data-ttu-id="03f78-232">**単位に切り上げ:** このチェックボックスをオフにします。</span><span class="sxs-lookup"><span data-stu-id="03f78-232">**Round up to unit:** Clear this check box.</span></span>
    - <span data-ttu-id="03f78-233">**梱包数量の検索:** このチェックボックスをオフにします。</span><span class="sxs-lookup"><span data-stu-id="03f78-233">**Locate packing quantity:** Clear this check box.</span></span>
    - <span data-ttu-id="03f78-234">**分割を許可** このチェック ボックスをオンにします。</span><span class="sxs-lookup"><span data-stu-id="03f78-234">**Allow split:** Select this check box.</span></span>

1. <span data-ttu-id="03f78-235">**保存**を選択して新しい行を保存します。</span><span class="sxs-lookup"><span data-stu-id="03f78-235">Select **Save** to save the new line.</span></span>
1. <span data-ttu-id="03f78-236">**行**グリッドで新しい行がまだ選択されている間に、**場所ディレクティブ アクション** クイック タブで**新規**を選択し、グリッドに行を追加します。</span><span class="sxs-lookup"><span data-stu-id="03f78-236">While your new line is still selected in the **Lines** grid, select **New** on the **Location Directive Actions** FastTab to add a row to the grid.</span></span>
1. <span data-ttu-id="03f78-237">新しい行で、次の値を設定します。</span><span class="sxs-lookup"><span data-stu-id="03f78-237">In the new row, set the following values:</span></span>

    - <span data-ttu-id="03f78-238">**シーケンス番号:** _1_ を入力します。</span><span class="sxs-lookup"><span data-stu-id="03f78-238">**Sequence number:** Enter _1_.</span></span>
    - <span data-ttu-id="03f78-239">**名前:** _バルクからピック_と入力します。</span><span class="sxs-lookup"><span data-stu-id="03f78-239">**Name:** Enter _Pick from bulk_.</span></span>
    - <span data-ttu-id="03f78-240">**固定の場所の使用:** _固定の場所および固定されていない場所_を選択します。</span><span class="sxs-lookup"><span data-stu-id="03f78-240">**Fixed location usage:** Select _Fixed and non-fixed locations_.</span></span>
    - <span data-ttu-id="03f78-241">**マイナス在庫を許可:** このチェックボックスをオフにします。</span><span class="sxs-lookup"><span data-stu-id="03f78-241">**Allow negative inventory:** Clear this check box.</span></span>
    - <span data-ttu-id="03f78-242">**バッチが有効:** このチェックボックスをオフにします。</span><span class="sxs-lookup"><span data-stu-id="03f78-242">**Batch enabled:** Clear this check box.</span></span>
    - <span data-ttu-id="03f78-243">**戦略:** _なし_を選択します。</span><span class="sxs-lookup"><span data-stu-id="03f78-243">**Strategy:** Select _None_.</span></span>

1. <span data-ttu-id="03f78-244">**保存**を選択して新しいアクションを保存します。</span><span class="sxs-lookup"><span data-stu-id="03f78-244">Select **Save** to save the new action.</span></span>
1. <span data-ttu-id="03f78-245">新しいアクションがまだ選択されている間に、**場所ディレクティブ アクション** グリッドの上にある**クエリの編集**を選択します。</span><span class="sxs-lookup"><span data-stu-id="03f78-245">While your new action still selected, select **Edit query** above the **Location Directive Actions** grid.</span></span>
1. <span data-ttu-id="03f78-246">クエリ ダイアログ ボックスが表示され、補充する場所を選択できます。</span><span class="sxs-lookup"><span data-stu-id="03f78-246">A query dialog box appears, where you can select the locations to replenish from.</span></span> <span data-ttu-id="03f78-247">**範囲**タブで、**追加**を選択してグリッドに新しい行を追加します。</span><span class="sxs-lookup"><span data-stu-id="03f78-247">On the **Range** tab, select **Add** to add a row to the grid.</span></span>
1. <span data-ttu-id="03f78-248">新しい行で、次の値を設定します。</span><span class="sxs-lookup"><span data-stu-id="03f78-248">In the new row, set the following values:</span></span>

    - <span data-ttu-id="03f78-249">**テーブル:** _場所_</span><span class="sxs-lookup"><span data-stu-id="03f78-249">**Table:** _Locations_</span></span>
    - <span data-ttu-id="03f78-250">**派生テーブル:** _場所_</span><span class="sxs-lookup"><span data-stu-id="03f78-250">**Derived table:** _Locations_</span></span>
    - <span data-ttu-id="03f78-251">**フィールド:** _ゾーン ID_</span><span class="sxs-lookup"><span data-stu-id="03f78-251">**Field:** _Zone ID_</span></span>
    - <span data-ttu-id="03f78-252">**基準:** _BULK_</span><span class="sxs-lookup"><span data-stu-id="03f78-252">**Criteria:** _BULK_</span></span>

1. <span data-ttu-id="03f78-253">**OK** を選択してクエリを保存し、ダイアログ ボックスを閉じます。</span><span class="sxs-lookup"><span data-stu-id="03f78-253">Select **OK** to save your query and close the dialog box.</span></span>
1. <span data-ttu-id="03f78-254">**保存**を選択し、場所のディレクティブを保存します。</span><span class="sxs-lookup"><span data-stu-id="03f78-254">Select **Save** to save your location directive.</span></span>

##### <a name="create-a-replenishment-put-directive"></a><span data-ttu-id="03f78-255">補充プット ディレクティブの作成</span><span class="sxs-lookup"><span data-stu-id="03f78-255">Create a replenishment put directive</span></span>

1. <span data-ttu-id="03f78-256">**場所ディレクティブ** ページの左ウィンドウで、**作業指示のタイプ** フィールドがまだ_補充_に設定されていることを確認します。</span><span class="sxs-lookup"><span data-stu-id="03f78-256">On the **Location directives** page, in the left pane, make sure that the **Work order type** field is still set to _Replenishment_.</span></span>
1. <span data-ttu-id="03f78-257">アクション ペインで、**新規**を選択して別の新しいディレクティブを作成します。</span><span class="sxs-lookup"><span data-stu-id="03f78-257">On the Action Pane, select **New** to create another new directive.</span></span>
1. <span data-ttu-id="03f78-258">次の値を設定します。</span><span class="sxs-lookup"><span data-stu-id="03f78-258">Set the following values:</span></span>

    - <span data-ttu-id="03f78-259">**シーケンス番号:** 規定値を受け入れます。</span><span class="sxs-lookup"><span data-stu-id="03f78-259">**Sequence number:** Accept the default value.</span></span>
    - <span data-ttu-id="03f78-260">**名前:** _ゾーン プット_と入力します。</span><span class="sxs-lookup"><span data-stu-id="03f78-260">**Name:** Enter _Zone put_.</span></span>
    - <span data-ttu-id="03f78-261">**作業指示のタイプ:** _プット_を選択します。</span><span class="sxs-lookup"><span data-stu-id="03f78-261">**Work order type:** Select _Put_.</span></span>
    - <span data-ttu-id="03f78-262">**サイト:** _6_ を選択します。</span><span class="sxs-lookup"><span data-stu-id="03f78-262">**Site:** Select _6_.</span></span>
    - <span data-ttu-id="03f78-263">**倉庫:** _61_ を選択します。</span><span class="sxs-lookup"><span data-stu-id="03f78-263">**Warehouse:** Select _61_.</span></span>
    - <span data-ttu-id="03f78-264">**ディレクティブ コード:** _Zone replen_ を選択して、この場所ディレクティブを以前作成したコードを使用して作成した補充テンプレートにリンクします。</span><span class="sxs-lookup"><span data-stu-id="03f78-264">**Directive code:** Select _Zone replen_ to link this location directive with the replenishment template that you created earlier by using the code that you created earlier.</span></span>
    - <span data-ttu-id="03f78-265">**マルチ SKU:** このオプションを_いいえ_に設定します。</span><span class="sxs-lookup"><span data-stu-id="03f78-265">**Multi SKU:** Set this option to _No_.</span></span>

1. <span data-ttu-id="03f78-266">Select **保存**を選択して、これまでにコンフィギュレーションした設定を持つディレクティブを作成します。</span><span class="sxs-lookup"><span data-stu-id="03f78-266">Select **Save** to create a directive that has the settings that you've configured so far.</span></span>
1. <span data-ttu-id="03f78-267">**明細行**クイック タブで、**新規**を選択してグリッドに明細行を追加します。</span><span class="sxs-lookup"><span data-stu-id="03f78-267">On the **Lines** FastTab, select **New** to add a line to the grid.</span></span>
1. <span data-ttu-id="03f78-268">新しい明細行で、次の値を設定します。</span><span class="sxs-lookup"><span data-stu-id="03f78-268">On the new line, set the following values:</span></span>

    - <span data-ttu-id="03f78-269">**シーケンス番号:** _1_ を入力します。</span><span class="sxs-lookup"><span data-stu-id="03f78-269">**Sequence number:** Enter _1_.</span></span>
    - <span data-ttu-id="03f78-270">**開始数量:** _0_ と入力します。</span><span class="sxs-lookup"><span data-stu-id="03f78-270">**From quantity:** Enter _0_.</span></span>
    - <span data-ttu-id="03f78-271">**上限数量:** _10000000_ と入力します。</span><span class="sxs-lookup"><span data-stu-id="03f78-271">**To quantity:** Enter _10000000_.</span></span>
    - <span data-ttu-id="03f78-272">**ユニット:** このフィールドは空白のままにします。</span><span class="sxs-lookup"><span data-stu-id="03f78-272">**Unit:** Leave this field blank.</span></span>
    - <span data-ttu-id="03f78-273">**数量の検索:** _なし_を選択します。</span><span class="sxs-lookup"><span data-stu-id="03f78-273">**Locate quantity:** Select _None_.</span></span>
    - <span data-ttu-id="03f78-274">**単位ごとに制限:** このチェック ボックスをオフにします。</span><span class="sxs-lookup"><span data-stu-id="03f78-274">**Restrict by unit:** Clear this check box.</span></span>
    - <span data-ttu-id="03f78-275">**単位に切り上げ:** このチェックボックスをオフにします。</span><span class="sxs-lookup"><span data-stu-id="03f78-275">**Round up to unit:** Clear this check box.</span></span>
    - <span data-ttu-id="03f78-276">**梱包数量の検索:** このチェックボックスをオフにします。</span><span class="sxs-lookup"><span data-stu-id="03f78-276">**Locate packing quantity:** Clear this check box.</span></span>
    - <span data-ttu-id="03f78-277">**分割を許可** このチェック ボックスをオンにします。</span><span class="sxs-lookup"><span data-stu-id="03f78-277">**Allow split:** Select this check box.</span></span>

1. <span data-ttu-id="03f78-278">**保存**を選択して新しい行を保存します。</span><span class="sxs-lookup"><span data-stu-id="03f78-278">Select **Save** to save the new line.</span></span>
1. <span data-ttu-id="03f78-279">**行**グリッドで新しい行がまだ選択されている間に、**場所ディレクティブ アクション** クイック タブで**新規**を選択し、グリッドに行を追加します。</span><span class="sxs-lookup"><span data-stu-id="03f78-279">While your new line is still selected in the **Lines** grid, select **New** on the **Location Directive Actions** FastTab to add a row to the grid.</span></span>
1. <span data-ttu-id="03f78-280">新しい行で、次の値を設定します。</span><span class="sxs-lookup"><span data-stu-id="03f78-280">In the new row, set the following values:</span></span>

    - <span data-ttu-id="03f78-281">**シーケンス番号:** _1_ を入力します。</span><span class="sxs-lookup"><span data-stu-id="03f78-281">**Sequence number:** Enter _1_.</span></span>
    - <span data-ttu-id="03f78-282">**名前:** _ゾーン プット_と入力します。</span><span class="sxs-lookup"><span data-stu-id="03f78-282">**Name:** Enter _Zone put_.</span></span>
    - <span data-ttu-id="03f78-283">**固定の場所の使用:** _固定の場所および固定されていない場所_を選択します。</span><span class="sxs-lookup"><span data-stu-id="03f78-283">**Fixed location usage:** Select _Fixed and non-fixed locations_.</span></span>
    - <span data-ttu-id="03f78-284">**マイナス在庫を許可:** このチェックボックスをオフにします。</span><span class="sxs-lookup"><span data-stu-id="03f78-284">**Allow negative inventory:** Clear this check box.</span></span>
    - <span data-ttu-id="03f78-285">**バッチが有効:** このチェックボックスをオフにします。</span><span class="sxs-lookup"><span data-stu-id="03f78-285">**Batch enabled:** Clear this check box.</span></span>
    - <span data-ttu-id="03f78-286">**戦略:** _連結_を選択します。</span><span class="sxs-lookup"><span data-stu-id="03f78-286">**Strategy:** Select _Consolidate_.</span></span>

1. <span data-ttu-id="03f78-287">**保存**を選択して新しいアクションを保存します。</span><span class="sxs-lookup"><span data-stu-id="03f78-287">Select **Save** to save the new action.</span></span>
1. <span data-ttu-id="03f78-288">新しいアクションがまだ選択されている間に、**場所ディレクティブ アクション** グリッドの上にある**クエリの編集**を選択します。</span><span class="sxs-lookup"><span data-stu-id="03f78-288">While your new action is still selected, select **Edit query** above the **Location Directive Actions** grid.</span></span>
1. <span data-ttu-id="03f78-289">クエリ ダイアログ ボックスが表示され、補充するゾーンを選択できます。</span><span class="sxs-lookup"><span data-stu-id="03f78-289">A query dialog box appears, where you can select the zone to replenish to.</span></span> <span data-ttu-id="03f78-290">このゾーンは、補充テンプレートで指定されているものと同じゾーンである必要があります。</span><span class="sxs-lookup"><span data-stu-id="03f78-290">This zone should be the same zone that is specified in the replenishment template.</span></span> <span data-ttu-id="03f78-291">**範囲**タブで、**追加**を選択してグリッドに新しい行を追加します。</span><span class="sxs-lookup"><span data-stu-id="03f78-291">On the **Range** tab, select **Add** to add a row to the grid.</span></span>
1. <span data-ttu-id="03f78-292">新しい行で、次の値を設定します。</span><span class="sxs-lookup"><span data-stu-id="03f78-292">In the new row, set the following values:</span></span>

    - <span data-ttu-id="03f78-293">**テーブル:** _場所_</span><span class="sxs-lookup"><span data-stu-id="03f78-293">**Table:** _Locations_</span></span>
    - <span data-ttu-id="03f78-294">**派生テーブル:** _場所_</span><span class="sxs-lookup"><span data-stu-id="03f78-294">**Derived table:** _Locations_</span></span>
    - <span data-ttu-id="03f78-295">**フィールド:** _ゾーン ID_</span><span class="sxs-lookup"><span data-stu-id="03f78-295">**Field:** _Zone ID_</span></span>
    - <span data-ttu-id="03f78-296">**基準:** _FLOOR_</span><span class="sxs-lookup"><span data-stu-id="03f78-296">**Criteria:** _FLOOR_</span></span>

1. <span data-ttu-id="03f78-297">**OK** を選択してクエリを保存し、ダイアログ ボックスを閉じます。</span><span class="sxs-lookup"><span data-stu-id="03f78-297">Select **OK** to save your query and close the dialog box.</span></span>
1. <span data-ttu-id="03f78-298">**保存**を選択し、場所のディレクティブを保存します。</span><span class="sxs-lookup"><span data-stu-id="03f78-298">Select **Save** to save your location directive.</span></span>

## <a name="scenario"></a><span data-ttu-id="03f78-299">シナリオ</span><span class="sxs-lookup"><span data-stu-id="03f78-299">Scenario</span></span>

<span data-ttu-id="03f78-300">このセクションでは、機能の使用方法を示すサンプル シナリオを提供します。</span><span class="sxs-lookup"><span data-stu-id="03f78-300">This section provides a sample scenario that shows how to work with the feature.</span></span>

### <a name="prepare-the-sample-data-that-is-required-for-the-sample-scenario"></a><span data-ttu-id="03f78-301">サンプル シナリオに必要なサンプル データの準備</span><span class="sxs-lookup"><span data-stu-id="03f78-301">Prepare the sample data that is required for the sample scenario</span></span>

<span data-ttu-id="03f78-302">シナリオの作業を開始する前に、サンプル データを有効にして、このトピックのこのセクションおよび前のセクションの説明に従って機能を設定する必要があります。</span><span class="sxs-lookup"><span data-stu-id="03f78-302">Before you start to work through the scenario, you must activate sample data and set up the feature as described in this section and in the previous sections of this topic.</span></span>

#### <a name="use-the-usmf-legal-entity"></a><span data-ttu-id="03f78-303">USMF 法人を使用します</span><span class="sxs-lookup"><span data-stu-id="03f78-303">Use the USMF legal entity</span></span>

<span data-ttu-id="03f78-304">指定されたサンプル レコードと値を使用してシナリオを実行するには、標準の [デモデータ](../../fin-ops-core/dev-itpro/deployment/deploy-demo-environment.md) がインストールされているシステムを使用する必要があります。</span><span class="sxs-lookup"><span data-stu-id="03f78-304">To work through the scenario by using the sample records and values that are specified here, you must be on a system where the standard [demo data](../../fin-ops-core/dev-itpro/deployment/deploy-demo-environment.md) is installed.</span></span> <span data-ttu-id="03f78-305">また、開始する前に **USMF** 法人を選択する必要があります。</span><span class="sxs-lookup"><span data-stu-id="03f78-305">Additionally, you must select the **USMF** legal entity before you begin.</span></span>

#### <a name="prepare-additional-sample-data"></a><span data-ttu-id="03f78-306">追加のサンプル データの準備</span><span class="sxs-lookup"><span data-stu-id="03f78-306">Prepare additional sample data</span></span>

<span data-ttu-id="03f78-307">**USMF** 法人を選択したら、このトピックの前の[ゾーンに基づく補充の設定](#setup) で説明しているように、必要な追加のサンプル データを追加し ます。</span><span class="sxs-lookup"><span data-stu-id="03f78-307">After you've selected the **USMF** legal entity, add the additional sample data that is required, as described in the [Set up zone-based replenishment](#setup) section earlier in this topic.</span></span>

#### <a name="check-your-on-hand-inventory"></a><span data-ttu-id="03f78-308">手持在庫の確認</span><span class="sxs-lookup"><span data-stu-id="03f78-308">Check your on-hand inventory</span></span>

<span data-ttu-id="03f78-309">このサンプル シナリオをサポートするのに十分な在庫がシステムに含まれていることを確認するには、次の手順を実行します。</span><span class="sxs-lookup"><span data-stu-id="03f78-309">Follow these steps to make sure that your system includes enough inventory to support the sample scenario.</span></span>

1. <span data-ttu-id="03f78-310">品目 *A0001* の手持在庫が、補充テンプレートで指定されているピック ゾーン (*FLOOR*) の 2 つの異なる場所にあることを確認します。</span><span class="sxs-lookup"><span data-stu-id="03f78-310">Make sure that there is on-hand inventory for item *A0001* at two different locations in the pick zone (*FLOOR*) that is specified in the replenishment template.</span></span> <span data-ttu-id="03f78-311">ただし、合計在庫は、補充テンプレートで指定された最小数量 (*50*) より小さくする必要があります。</span><span class="sxs-lookup"><span data-stu-id="03f78-311">However, the total inventory should be less than the required minimum quantity (*50*) that is specified on the replenishment template.</span></span> <span data-ttu-id="03f78-312">これにより、1 つの場所だけでなく、ゾーン全体の計算がどのように行われるかをシミュレートすることができます。</span><span class="sxs-lookup"><span data-stu-id="03f78-312">In this way, you can simulate how the calculation occurs for the whole zone instead of just for a single location.</span></span> <span data-ttu-id="03f78-313">**必要に応じて、いずれかの倉庫プロセスを使用して在庫を調整します。**</span><span class="sxs-lookup"><span data-stu-id="03f78-313">**Use any of the warehouse processes to adjust inventory as required.**</span></span>
1. <span data-ttu-id="03f78-314">補充作業がゾーン ID *BULK* から品目をピックする必要があるゾーン ピック場所ディレクティブで指定されたバルクの場所に、品目 *A0001* の十分な在庫があることを確認します。</span><span class="sxs-lookup"><span data-stu-id="03f78-314">Make sure that there is enough inventory for item *A0001* at a bulk location that is specified in the zone pick location directive where the replenishment work should pick the items from zone ID *BULK*.</span></span> <span data-ttu-id="03f78-315">合計在庫は、補充テンプレートで指定された最大数量 (*150*) より大きくする必要があります。</span><span class="sxs-lookup"><span data-stu-id="03f78-315">The total inventory must be more than the required maximum quantity (*150*) that is specified in the replenishment template.</span></span>
1. <span data-ttu-id="03f78-316">次はオプションですが、推奨されます。以下の手順に従って在庫調整仕訳帳を作成します。</span><span class="sxs-lookup"><span data-stu-id="03f78-316">Optional but recommended: Follow these steps to create an inventory adjustment journal:</span></span>

    1. <span data-ttu-id="03f78-317">**在庫管理\>仕訳入力\>品目\>在庫調整**の順に移動します。</span><span class="sxs-lookup"><span data-stu-id="03f78-317">Go to **Inventory management \> Journal entries \> Items \> Inventory adjustment**.</span></span>
    1. <span data-ttu-id="03f78-318">**新規** を選択します。</span><span class="sxs-lookup"><span data-stu-id="03f78-318">Select **New**.</span></span>
    1. <span data-ttu-id="03f78-319">**在庫仕訳帳の作成**ダイアログ ボックスの**倉庫**フィールドで、*61* を選択します。</span><span class="sxs-lookup"><span data-stu-id="03f78-319">In the **Create inventory journal** dialog box, in the **Warehouse** field, select *61*.</span></span>
    1. <span data-ttu-id="03f78-320">**OK** を選択します。</span><span class="sxs-lookup"><span data-stu-id="03f78-320">Select **OK**.</span></span>
    1. <span data-ttu-id="03f78-321">**仕訳帳明細行**クイック タブで、**新規**ボタンを使用して、グリッドに 3 行を追加し、次の値を設定します。</span><span class="sxs-lookup"><span data-stu-id="03f78-321">On the **Journal lines** FastTab, use the **New** button to add three lines to the grid, and set the following values.</span></span> <span data-ttu-id="03f78-322">各行の設定が完了したら、**保存**を選択します。</span><span class="sxs-lookup"><span data-stu-id="03f78-322">After you've finished setting up each line, select **Save**.</span></span>

        - <span data-ttu-id="03f78-323">**行 1:**</span><span class="sxs-lookup"><span data-stu-id="03f78-323">**Line 1:**</span></span>

            - <span data-ttu-id="03f78-324">**品目番号:** *A0001*</span><span class="sxs-lookup"><span data-stu-id="03f78-324">**Item number:** *A0001*</span></span>
            - <span data-ttu-id="03f78-325">**サイト:** *6*</span><span class="sxs-lookup"><span data-stu-id="03f78-325">**Site:** *6*</span></span>
            - <span data-ttu-id="03f78-326">**倉庫:** *61*</span><span class="sxs-lookup"><span data-stu-id="03f78-326">**Warehouse:** *61*</span></span>
            - <span data-ttu-id="03f78-327">**場所:** *02A01R1S1B*</span><span class="sxs-lookup"><span data-stu-id="03f78-327">**Location:** *02A01R1S1B*</span></span>
            - <span data-ttu-id="03f78-328">**ライセンス プレート:** 一覧で既存のライセンス プレートを選択するか、新しいライセンス プレートを作成します。</span><span class="sxs-lookup"><span data-stu-id="03f78-328">**License plate:** Select an existing license plate in the list, or create a new license plate.</span></span>
            - <span data-ttu-id="03f78-329">**数量:** *1000*</span><span class="sxs-lookup"><span data-stu-id="03f78-329">**Quantity:** *1000*</span></span>

        - <span data-ttu-id="03f78-330">**行 2:**</span><span class="sxs-lookup"><span data-stu-id="03f78-330">**Line 2:**</span></span>

            - <span data-ttu-id="03f78-331">**品目番号:** *A0001*</span><span class="sxs-lookup"><span data-stu-id="03f78-331">**Item number:** *A0001*</span></span>
            - <span data-ttu-id="03f78-332">**サイト:** *6*</span><span class="sxs-lookup"><span data-stu-id="03f78-332">**Site:** *6*</span></span>
            - <span data-ttu-id="03f78-333">**倉庫:** *61*</span><span class="sxs-lookup"><span data-stu-id="03f78-333">**Warehouse:** *61*</span></span>
            - <span data-ttu-id="03f78-334">**場所:** *07A01R2S1B*</span><span class="sxs-lookup"><span data-stu-id="03f78-334">**Location:** *07A01R2S1B*</span></span>
            - <span data-ttu-id="03f78-335">**ライセンス プレート:** 一覧で既存のライセンス プレートを選択するか、新しいライセンス プレートを作成します。</span><span class="sxs-lookup"><span data-stu-id="03f78-335">**License plate:** Select an existing license plate in the list, or create a new license plate.</span></span>
            - <span data-ttu-id="03f78-336">**数量:** *15*</span><span class="sxs-lookup"><span data-stu-id="03f78-336">**Quantity:** *15*</span></span>

        - <span data-ttu-id="03f78-337">**行 3:**</span><span class="sxs-lookup"><span data-stu-id="03f78-337">**Line 3:**</span></span>

            - <span data-ttu-id="03f78-338">**品目番号:** *A0001*</span><span class="sxs-lookup"><span data-stu-id="03f78-338">**Item number:** *A0001*</span></span>
            - <span data-ttu-id="03f78-339">**サイト:** *6*</span><span class="sxs-lookup"><span data-stu-id="03f78-339">**Site:** *6*</span></span>
            - <span data-ttu-id="03f78-340">**倉庫:** *61*</span><span class="sxs-lookup"><span data-stu-id="03f78-340">**Warehouse:** *61*</span></span>
            - <span data-ttu-id="03f78-341">**場所:** *07A01R1S1B*</span><span class="sxs-lookup"><span data-stu-id="03f78-341">**Location:** *07A01R1S1B*</span></span>
            - <span data-ttu-id="03f78-342">**ライセンス プレート:** 一覧で既存のライセンス プレートを選択するか、新しいライセンス プレートを作成します。</span><span class="sxs-lookup"><span data-stu-id="03f78-342">**License plate:** Select an existing license plate in the list, or create a new license plate.</span></span>
            - <span data-ttu-id="03f78-343">**数量:** *10*</span><span class="sxs-lookup"><span data-stu-id="03f78-343">**Quantity:** *10*</span></span>

    1. <span data-ttu-id="03f78-344">アクション ペインで、**検証**を選択します。</span><span class="sxs-lookup"><span data-stu-id="03f78-344">On the Action Pane, select **Validate**.</span></span> <span data-ttu-id="03f78-345">次のステップに進む前に検出されたエラーに対処します。</span><span class="sxs-lookup"><span data-stu-id="03f78-345">Address any errors that are found before you move on to the next step.</span></span>
    1. <span data-ttu-id="03f78-346">アクション ペインで**転記**を選択して、在庫を倉庫に転記します。</span><span class="sxs-lookup"><span data-stu-id="03f78-346">On the Action Pane, select **Post** to post the inventory to the warehouse.</span></span>

### <a name="sample-scenario-run-zone-based-minmax-replenishment"></a><span data-ttu-id="03f78-347">サンプル シナリオ: ゾーンに基づく最小/最大補充の実行</span><span class="sxs-lookup"><span data-stu-id="03f78-347">Sample scenario: Run zone-based min/max replenishment</span></span>

<span data-ttu-id="03f78-348">前提条件のサンプル データをすべて設定したら、次の手順に従って補充をトリガーできます。</span><span class="sxs-lookup"><span data-stu-id="03f78-348">After all the prerequisite sample data is in place, you can trigger replenishment by following these steps.</span></span>

1. <span data-ttu-id="03f78-349">**倉庫管理\>補充\>補充**の順に移動します。</span><span class="sxs-lookup"><span data-stu-id="03f78-349">Go to **Warehouse management \> Replenishment \> Replenishments**.</span></span>
1. <span data-ttu-id="03f78-350">**補充**ダイアログ ボックスの**対象に含めるレコード** クイック タブで、**フィルター**を選択します。</span><span class="sxs-lookup"><span data-stu-id="03f78-350">In the **Replenishment** dialog box, on the **Records to include** FastTab, select **Filter**.</span></span>
1. <span data-ttu-id="03f78-351">**照会**ダイアログ ボックスの**範囲**タブで、既定のテーブル行を次のように編集します。</span><span class="sxs-lookup"><span data-stu-id="03f78-351">In the **Inquiry** dialog box, on the **Range** tab, edit the default table row in the following way:</span></span>

    - <span data-ttu-id="03f78-352">**テーブル:** _補充テンプレート_を選択します。</span><span class="sxs-lookup"><span data-stu-id="03f78-352">**Table:** Select _Replenishment templates_.</span></span>
    - <span data-ttu-id="03f78-353">**派生テーブル:** _補充テンプレート_を選択します。</span><span class="sxs-lookup"><span data-stu-id="03f78-353">**Derived table:** Select _Replenishment templates_.</span></span>
    - <span data-ttu-id="03f78-354">**フィールド:** _補充テンプレート_を選択します。</span><span class="sxs-lookup"><span data-stu-id="03f78-354">**Field:** Select _Replenishment template_.</span></span>
    - <span data-ttu-id="03f78-355">**基準:** _Zone min/max replen_ を選択します。</span><span class="sxs-lookup"><span data-stu-id="03f78-355">**Criteria:** Select _Zone min/max replen_.</span></span> <span data-ttu-id="03f78-356">この補充テンプレートは、このシナリオのデモ データを準備している間に作成した補充テンプレートです。</span><span class="sxs-lookup"><span data-stu-id="03f78-356">This replenishment template is the replenishment template that you created while you were preparing the demo data for this scenario.</span></span>

1. <span data-ttu-id="03f78-357">**OK** を選択してクエリを保存し、**補充**ダイアログ ボックスに戻ります。</span><span class="sxs-lookup"><span data-stu-id="03f78-357">Select **OK** to save the query and go back to the **Replenishment** dialog box.</span></span>
1. <span data-ttu-id="03f78-358">**OK** を選択して、補充テンプレートを実行します。</span><span class="sxs-lookup"><span data-stu-id="03f78-358">Select **OK** to run the replenishment template.</span></span>

<span data-ttu-id="03f78-359">これで、補充作業が作成されて *BULK* ゾーンから在庫をピックし、*FLOOR* ゾーンに補充します。</span><span class="sxs-lookup"><span data-stu-id="03f78-359">Replenishment work is now created to pick inventory from the *BULK* zone and replenish it to the *FLOOR* zone.</span></span>

## <a name="notes-and-tips"></a><span data-ttu-id="03f78-360">メモとヒント</span><span class="sxs-lookup"><span data-stu-id="03f78-360">Notes and tips</span></span>

<span data-ttu-id="03f78-361">この機能を使用するためのメモとヒントを次に示します。</span><span class="sxs-lookup"><span data-stu-id="03f78-361">Here are a few notes and tips for working with the feature:</span></span>

- <span data-ttu-id="03f78-362">目的のゾーンに移動する補充作業を設定するには、次のいずれかの方法で補充テンプレートの行と場所ディレクティブをリンクできます。</span><span class="sxs-lookup"><span data-stu-id="03f78-362">To set up replenishment work that goes to the desired zone, you can link the replenishment template lines and location directives in either of the following ways:</span></span>

    - <span data-ttu-id="03f78-363">場所ディレクティブ ヘッダー クエリを編集し、選択した補充テンプレートの行をフィルタ処理します。</span><span class="sxs-lookup"><span data-stu-id="03f78-363">Edit the location directive header query, and filter the selected replenishment template lines.</span></span>
    - <span data-ttu-id="03f78-364">補充テンプレートの行でディレクティブ コードを使用し、それをプット場所ディレクティブと一致させます。</span><span class="sxs-lookup"><span data-stu-id="03f78-364">Use a directive code on the replenishment template line, and match it to the put location directive.</span></span>

- <span data-ttu-id="03f78-365">動的な場所を使用している場合、場所ディレクティブ アクションが**連結**戦略を使用するように設定されている場合は、最初に使用可能な場所または在庫が含まれている場所に対して補充作業が作成されます。</span><span class="sxs-lookup"><span data-stu-id="03f78-365">If you're using dynamic locations, replenishment work will be created either for the first available location or for a location that already contains inventory, if the location directive action is set up to use the **Consolidate** strategy.</span></span>
- <span data-ttu-id="03f78-366">ゾーンではなく固定の場所を使用する場合は、[標準の最小/最大補充](tasks/set-up-min-max-replenishment-process.md)を使用する必要があります。</span><span class="sxs-lookup"><span data-stu-id="03f78-366">If you're using fixed locations instead of zones, you should use [standard min/max replenishment](tasks/set-up-min-max-replenishment-process.md).</span></span>
