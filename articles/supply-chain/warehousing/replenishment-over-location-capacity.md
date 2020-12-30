---
title: 場所の能力を超える補充
description: このトピックでは、場所の能力を超える補充機能に関する情報を提供します。 この機能によって、その日の作成に必要な補充作業がすべて有効になり、ピッキング場所の在庫がなくなったり、容量を超えたりしないことを保証するためにその補充作業の利用可能性を管理できるようになります。
author: mirzaab
manager: tfehr
ms.date: 07/16/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: WHSReplenishmentTemplates, WHSLocationLimit
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: mirzaab
ms.search.validFrom: 2020-07-16
ms.dyn365.ops.version: Release 10.0.7
ms.openlocfilehash: 8e9ae16fea892d1d6b6a6b5d06137576623e7f5b
ms.sourcegitcommit: 827d77c638555396b32d36af5d22d1b61dafb0e8
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 10/16/2020
ms.locfileid: "4432353"
---
# <a name="replenishment-over-location-capacity"></a><span data-ttu-id="27681-104">場所の能力を超える補充</span><span class="sxs-lookup"><span data-stu-id="27681-104">Replenishment over location capacity</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="27681-105">大規模な、または空間上制約のある倉庫の中には、ピッキング場所に収まるよりも多くの数量を 1 日に出荷する必要があるものがあります。</span><span class="sxs-lookup"><span data-stu-id="27681-105">Some high-volume or space-constrained warehouses must ship more quantity of an item in a day than will fit in the picking location.</span></span> <span data-ttu-id="27681-106">*場所の能力を超える補充* 機能によって、その日の作成に必要な補充作業がすべて有効になり、ピッキング場所の在庫がなくなったり、容量を超えたりしないことを保証するためにその補充作業の利用可能性を管理できるようになります。</span><span class="sxs-lookup"><span data-stu-id="27681-106">The *Replenishment over location capacity* feature enables all replenishment work that will be required for the day to be created and manages availability of that replenishment work to ensure that the picking location neither runs out of inventory nor goes above capacity.</span></span>

<span data-ttu-id="27681-107">この機能を使用すると、場所に収めるのではなく補充作業を作成することができます。また、保管場所がいっぱいになったときに補充作業が完了するのをブロックします。</span><span class="sxs-lookup"><span data-stu-id="27681-107">The feature enables more replenishment work to be created than will fit in a location, and it blocks replenishment work from being completed when the location is full.</span></span> <span data-ttu-id="27681-108">ピッキング場所の在庫がコンフィギュレーション可能なしきい値を下回った場合は、より多くの補充作業を使用できます。</span><span class="sxs-lookup"><span data-stu-id="27681-108">As inventory in the picking location drops below a configurable threshold, more replenishment work is made available.</span></span>

## <a name="turn-on-the-replenishment-over-location-capacity-feature"></a><span data-ttu-id="27681-109">場所の能力を超える補充機能をオンにする</span><span class="sxs-lookup"><span data-stu-id="27681-109">Turn on the Replenishment over location capacity feature</span></span>

<span data-ttu-id="27681-110">この機能を使用できるようにするには、[機能管理](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md)で次の機能を順にオンにします。</span><span class="sxs-lookup"><span data-stu-id="27681-110">To make this feature available, turn on the following features in [feature management](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) (in this order):</span></span>

1. <span data-ttu-id="27681-111">組織全体の作業のブロック</span><span class="sxs-lookup"><span data-stu-id="27681-111">Organization-wide work blocking</span></span>
1. <span data-ttu-id="27681-112">場所の能力を超える補充</span><span class="sxs-lookup"><span data-stu-id="27681-112">Replenishment over location capacity</span></span>

## <a name="set-up-the-feature-for-the-example-scenario"></a><span data-ttu-id="27681-113">シナリオ例の機能の設定</span><span class="sxs-lookup"><span data-stu-id="27681-113">Set up the feature for the example scenario</span></span>

<span data-ttu-id="27681-114">このセクションでは、この機能の設定方法と、本トピックの後で紹介するシナリオ例にサンプル データを準備する方法を示すガイドラインと例を説明します。</span><span class="sxs-lookup"><span data-stu-id="27681-114">This section provides guidelines and an example that shows how to set up this feature and prepare sample data for the example scenario that is provided later in this topic.</span></span>

### <a name="enable-sample-data"></a><span data-ttu-id="27681-115">サンプルデータの有効化</span><span class="sxs-lookup"><span data-stu-id="27681-115">Enable sample data</span></span>

<span data-ttu-id="27681-116">ここで指定されたサンプル レコードと値を使用して [シナリオ例](#example-scenario) を実行するには、標準の [デモ データ](../../fin-ops-core/dev-itpro/deployment/deploy-demo-environment.md) がインストールされているシステムを使用する必要があります。</span><span class="sxs-lookup"><span data-stu-id="27681-116">To work through the [example scenario](#example-scenario) by using the sample records and values that are specified here, you must be on a system where the standard [demo data](../../fin-ops-core/dev-itpro/deployment/deploy-demo-environment.md) is installed.</span></span> <span data-ttu-id="27681-117">また、開始する前に **USMF** 法人を選択する必要があります。</span><span class="sxs-lookup"><span data-stu-id="27681-117">Additionally, you must select the **USMF** legal entity before you begin.</span></span>

### <a name="location-profile"></a><span data-ttu-id="27681-118">場所プロファイル</span><span class="sxs-lookup"><span data-stu-id="27681-118">Location profile</span></span>

<span data-ttu-id="27681-119">場所のプロファイルで能力を超えた補充を有効にします。</span><span class="sxs-lookup"><span data-stu-id="27681-119">Enable the replenish over capacity functionality on the location profile.</span></span>

1. <span data-ttu-id="27681-120">**倉庫管理 \> 設定 \> 倉庫 \> 場所プロファイル** に移動します。</span><span class="sxs-lookup"><span data-stu-id="27681-120">Go to **Warehouse management \> Setup \> Warehouse \> Locations profiles**.</span></span>
1. <span data-ttu-id="27681-121">左のウィンドウで、**PICK-06** を選択します。</span><span class="sxs-lookup"><span data-stu-id="27681-121">In the left pane, select **PICK-06**.</span></span>
1. <span data-ttu-id="27681-122">アクション ウィンドウで、**編集** を選択します。</span><span class="sxs-lookup"><span data-stu-id="27681-122">On the Action Pane, select **Edit**.</span></span>
1. <span data-ttu-id="27681-123">**補充** クイック タブで、次の値を設定します:</span><span class="sxs-lookup"><span data-stu-id="27681-123">On the **Replenishment** FastTab, set the following values:</span></span>

    - <span data-ttu-id="27681-124">**場所の能力を超える:** *はい*</span><span class="sxs-lookup"><span data-stu-id="27681-124">**Exceed Location Capacity:** *Yes*</span></span>

        <span data-ttu-id="27681-125">有効な場合、その場所の最大キャパシティは補充作業によって超過できます。</span><span class="sxs-lookup"><span data-stu-id="27681-125">When enabled, the maximum capacity of the location will be allowed to be exceeded by replenishment work.</span></span> <span data-ttu-id="27681-126">これにより、**補充** クイック タブの他のフィールドも有効になり ます。</span><span class="sxs-lookup"><span data-stu-id="27681-126">This also enables other fields on the **Replenishment** FastTab.</span></span>

    - <span data-ttu-id="27681-127">**利用可能時間のしきい値のタイプ:** *数量*</span><span class="sxs-lookup"><span data-stu-id="27681-127">**Work availability threshold type:** *Quantity*</span></span>

        <span data-ttu-id="27681-128">このフィールドは、より多くの作業をリリースするタイミングを決定するために使用される方法を定義します。</span><span class="sxs-lookup"><span data-stu-id="27681-128">This field defines the method that is used to determine when more work should be released.</span></span> <span data-ttu-id="27681-129">数量または割合によりリリースできます。</span><span class="sxs-lookup"><span data-stu-id="27681-129">You can release by either quantity or a percentage:</span></span>

        - <span data-ttu-id="27681-130">*割合*: このオプションは、在庫限度または容積測定に基づく能力の割合を使用する場合に選択します。</span><span class="sxs-lookup"><span data-stu-id="27681-130">*Percent* – Select this option to use percentage capacity that is based on stocking limits or volumetrics.</span></span> <span data-ttu-id="27681-131">このオプションを選択すると、**オーバーフローの割合** フィールドが有効になり、2 つの数量関連フィールド (**オーバーフロー数量** と **オーバーフロー単位**) が無効になります。</span><span class="sxs-lookup"><span data-stu-id="27681-131">Selecting this option enables the **Overflow percentage** field, and disables the two quantity related fields,  **Overflow quantity** and **Overflow unit**.</span></span>

            <span data-ttu-id="27681-132">このオプションは、ピッキング場所で容積測定を使用する場合に使用できます。</span><span class="sxs-lookup"><span data-stu-id="27681-132">You can use this option if the picking locations use volumetrics.</span></span>

            <span data-ttu-id="27681-133">このオプションを選択した場合は、**オーバーフローの割合** フィールドを、使用可能な補充作業がさらにある割合に設定します。</span><span class="sxs-lookup"><span data-stu-id="27681-133">If this option is selected, set the **Overflow percentage** field to the percentage at which more replenishment work will be made available.</span></span>

        - <span data-ttu-id="27681-134">*数量*: 特定の数量の値を使用するには、このオプションを選択します。</span><span class="sxs-lookup"><span data-stu-id="27681-134">*Quantity* – Select this option to use a specific quantity value.</span></span> <span data-ttu-id="27681-135">このオプションを選択すると、**オーバーフローの割合** フィールドが無効になり、**オーバーフロー数量** と **オーバーフロー単位** フィールドが有効になります。</span><span class="sxs-lookup"><span data-stu-id="27681-135">Selecting this option disables the **Overflow percentage** field and enables **Overflow quantity** and **Overflow unit** fields.</span></span>

            <span data-ttu-id="27681-136">補充される場所に対して容積測定を使用していない場合、または場所に持ち込む在庫数を増やす必要がある一貫した数量を持っている場合は、このオプションを使用します。</span><span class="sxs-lookup"><span data-stu-id="27681-136">Use this option when you aren't using volumetrics for the locations that are being replenished, or when you have consistent quantities at which you want more inventory to be brought to the location.</span></span>

           <span data-ttu-id="27681-137">このオプションが選択されている場合は、**オーバーフロー数量** フィールドと **オーバーフロー単位** フィールドを、より多くの補充作業を実行できる数量と単位に設定します。</span><span class="sxs-lookup"><span data-stu-id="27681-137">If this option is selected, set the **Overflow quantity** and **Overflow unit** fields to the quantity and unit at which more replenishment work will be made available.</span></span>

    - <span data-ttu-id="27681-138">**オーバーフロー数量:** *0.65*</span><span class="sxs-lookup"><span data-stu-id="27681-138">**Overflow quantity:** *0.65*</span></span>

        <span data-ttu-id="27681-139">このフィールドでは、その場所がオーバーフローする数量を定義します。</span><span class="sxs-lookup"><span data-stu-id="27681-139">This field defines the quantity at which the location overflows.</span></span>

        <span data-ttu-id="27681-140">場所における手持数量と作業数量がこの値を下回るたびに作業が可能になります。</span><span class="sxs-lookup"><span data-stu-id="27681-140">Work will be available whenever the sum of the on-hand quantity in the location and the work quantity is below this value.</span></span> <span data-ttu-id="27681-141">この値以上の補充作業はブロックされるため、手動でブロックを解除する必要があります。</span><span class="sxs-lookup"><span data-stu-id="27681-141">Any replenishment work above this value will be blocked and must be manually unblocked.</span></span>

        <span data-ttu-id="27681-142">作業数量を計算するときに場所別在庫限度が考慮されます。</span><span class="sxs-lookup"><span data-stu-id="27681-142">Location stocking limits are considered when the work quantity is calculated.</span></span>

    - <span data-ttu-id="27681-143">**オーバーフロー単位:** *PL*</span><span class="sxs-lookup"><span data-stu-id="27681-143">**Overflow unit:** *PL*</span></span>

        <span data-ttu-id="27681-144">このフィールドは、オーバーフロー数量に関連付けられている単位を定義します。</span><span class="sxs-lookup"><span data-stu-id="27681-144">This field defines the unit that is associated with the overflow quantity.</span></span>

        <span data-ttu-id="27681-145">この場合、その場所が 0.65 パレット (PL) までダウンしたときに、より多くの補充作業が可能になります。</span><span class="sxs-lookup"><span data-stu-id="27681-145">In this case, more replenishment work will be made available when the location gets down to 0.65 pallet (PL).</span></span>

    - <span data-ttu-id="27681-146">**オーバーフロー率**</span><span class="sxs-lookup"><span data-stu-id="27681-146">**Overflow percentage**</span></span>

        <span data-ttu-id="27681-147">このフィールドでは、その場所がオーバーフローする割合を定義します。</span><span class="sxs-lookup"><span data-stu-id="27681-147">This field defines the percentage at which the location overflows.</span></span>

        <span data-ttu-id="27681-148">場所における手持数量と作業数量がこの割合を下回るたびに作業が可能になります。</span><span class="sxs-lookup"><span data-stu-id="27681-148">Work will be available whenever the sum of the on-hand quantity in the location and the work quantity is below this percentage.</span></span> <span data-ttu-id="27681-149">この値以上の補充作業量の割合はブロックされるため、手動でブロックを解除する必要があります。</span><span class="sxs-lookup"><span data-stu-id="27681-149">Any replenishment work quantity percentage above this value will be blocked and must be manually unblocked.</span></span>

        <span data-ttu-id="27681-150">作業数量割合を計算するときに場所別在庫限度が考慮されます。</span><span class="sxs-lookup"><span data-stu-id="27681-150">Location stocking limits are considered when the work quantity percentage is calculated.</span></span> <span data-ttu-id="27681-151">保管場所の在庫上限が定義されていない場合で、場所のプロファイルにボリュームの制約が定義されている場合は、作業量の割合がボリューム別に計算されます。</span><span class="sxs-lookup"><span data-stu-id="27681-151">If no location stocking limits are defined, the work quantity percentage is calculated by volume if volume constraints are defined for the location profile.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="27681-152">**USMF** 法人のデモ データを使用していて、*場所ライセンス プレートの配置* 機能をオンにしている場合は、サンプル シナリオでモバイル ステップを完了するために、場所プロファイル **BULK-06** の **場所ライセンス プレートの配置の有効化** をオフにする必要があります。</span><span class="sxs-lookup"><span data-stu-id="27681-152">If you're using the demo data for the **USMF** legal entity and previously turned on the *Location license plate positioning* feature, you must turn off the **Enable license plate positioning** setting for the **BULK-06** location profile to complete the mobile steps in the example scenario.</span></span>

### <a name="wave-step-code"></a><span data-ttu-id="27681-153">ウェーブ ステップ コード</span><span class="sxs-lookup"><span data-stu-id="27681-153">Wave step code</span></span>

> [!NOTE]
> <span data-ttu-id="27681-154">ここでの説明に従ってウェーブ ステップ コードを設定するには、まず、[機能管理](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md)を使用して、*組織全体のウェーブ ステップ コード* と呼ばれる機能を有効にする必要があります。</span><span class="sxs-lookup"><span data-stu-id="27681-154">To set up a wave step code as described here, you might first have to use [feature management](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) to turn on the feature that is named *Organization wide wave step code*.</span></span>

1. <span data-ttu-id="27681-155">**倉庫管理 \> 設定 \> ウェーブ \> ウェーブ ステップ コード** の順に移動します。</span><span class="sxs-lookup"><span data-stu-id="27681-155">Go to **Warehouse Management \> Setup \> Waves \> Wave step codes**.</span></span>
1. <span data-ttu-id="27681-156">**新規** を選択して、次の値を設定します。</span><span class="sxs-lookup"><span data-stu-id="27681-156">Select **New**, and set the following values:</span></span>

    - <span data-ttu-id="27681-157">**ウェーブ ステップ コード :** *補充*</span><span class="sxs-lookup"><span data-stu-id="27681-157">**Wave step code:** *Replen*</span></span>
    - <span data-ttu-id="27681-158">**ウェーブ ステップ詳細:** *補充*</span><span class="sxs-lookup"><span data-stu-id="27681-158">**Wave step description:** *Replenishment*</span></span>
    - <span data-ttu-id="27681-159">**ウェーブ ステップ タイプ:** *補充*</span><span class="sxs-lookup"><span data-stu-id="27681-159">**Wave step type:** *Replenishment*</span></span>

1. <span data-ttu-id="27681-160">**保存** を選択します。</span><span class="sxs-lookup"><span data-stu-id="27681-160">Select **Save**.</span></span>

### <a name="replenishment-template"></a><span data-ttu-id="27681-161">補充テンプレート</span><span class="sxs-lookup"><span data-stu-id="27681-161">Replenishment template</span></span>

<span data-ttu-id="27681-162">補充テンプレートは、場所が補充されるタイミングと方法を制御するルールのセットです。</span><span class="sxs-lookup"><span data-stu-id="27681-162">Replenishment templates are a set of rules that control when and how a location is replenished.</span></span>

1. <span data-ttu-id="27681-163">**倉庫管理\>設定\>補充\>補充テンプレート** の順に移動します。</span><span class="sxs-lookup"><span data-stu-id="27681-163">Go to **Warehouse management \> Setup \> Replenishment \> Replenishment templates**.</span></span>
1. <span data-ttu-id="27681-164">アクション ウィンドウで、**編集** を選択します。</span><span class="sxs-lookup"><span data-stu-id="27681-164">On the Action Pane, select **Edit**.</span></span>
1. <span data-ttu-id="27681-165">**概要** セクションで、**補充テンプレート** フィールドが *補充を要求* に設定されている明細行を選択します。</span><span class="sxs-lookup"><span data-stu-id="27681-165">In the **Overview** section, select the line where the **Replenish template** field is set to *Demand replenish*.</span></span>
1. <span data-ttu-id="27681-166">次の値を設定します。</span><span class="sxs-lookup"><span data-stu-id="27681-166">Set the following values:</span></span>

    - <span data-ttu-id="27681-167">**ウェーブ ステップ コード :** *補充*</span><span class="sxs-lookup"><span data-stu-id="27681-167">**Wave step code:** *Replen*</span></span>
    - <span data-ttu-id="27681-168">**ウェーブ要素に未引当数量の使用を許可する:** *はい*</span><span class="sxs-lookup"><span data-stu-id="27681-168">**Allow wave demand to use unreserved quantities:** *Yes*</span></span>

1. <span data-ttu-id="27681-169">**保存** を選択します。</span><span class="sxs-lookup"><span data-stu-id="27681-169">Select **Save**.</span></span>

### <a name="wave-template"></a><span data-ttu-id="27681-170">ウェーブ テンプレート</span><span class="sxs-lookup"><span data-stu-id="27681-170">Wave template</span></span>

1. <span data-ttu-id="27681-171">**倉庫管理 \> 設定 \> ウェーブ \> ウェーブ テンプレート** の順に移動します。</span><span class="sxs-lookup"><span data-stu-id="27681-171">Go to **Warehouse management \> Setup \> Waves \> Wave templates**.</span></span>
1. <span data-ttu-id="27681-172">左ウィンドウで、**ウェーブ テンプレート タイプ** フィールドを *出荷* に設定します。</span><span class="sxs-lookup"><span data-stu-id="27681-172">In the left pane, set the **Wave template type** field to *Shipping*.</span></span>
1. <span data-ttu-id="27681-173">リストでテンプレート **61 出荷** を選択します。</span><span class="sxs-lookup"><span data-stu-id="27681-173">Select template **61 Shipping** in the list.</span></span>
1. <span data-ttu-id="27681-174">アクション ウィンドウで、**編集** を選択します。</span><span class="sxs-lookup"><span data-stu-id="27681-174">On the Action Pane, select **Edit**.</span></span>
1. <span data-ttu-id="27681-175">**一般** クイック タブで、**補充作業のリリースの自動化** オプションを *はい* に設定します。</span><span class="sxs-lookup"><span data-stu-id="27681-175">On the **General** FastTab, set the **Automate replenishment work release** option to *Yes*.</span></span>

    <span data-ttu-id="27681-176">要求ベースの補充作業を作成して自動的にリリースするには、このオプションを *はい* に設定します。</span><span class="sxs-lookup"><span data-stu-id="27681-176">Set this option to *Yes* to create demand-based replenishment work and release it automatically.</span></span> <span data-ttu-id="27681-177">ウェーブ テンプレートに補充ウェーブ メソッドを追加し、**ウェーブ需要** タイプの補充テンプレートを作成する必要があります。</span><span class="sxs-lookup"><span data-stu-id="27681-177">You must add the replenishment wave method to the wave template and create a replenishment template of the **Wave demand** type.</span></span> <span data-ttu-id="27681-178">**補充テンプレート** ページで補充テンプレートを設定します。</span><span class="sxs-lookup"><span data-stu-id="27681-178">Set up a replenishment template on the **Replenishment templates** page.</span></span> <span data-ttu-id="27681-179">補充テンプレートを設定するには、補充方法をウェーブ テンプレートに追加する必要があります。</span><span class="sxs-lookup"><span data-stu-id="27681-179">To set up a replenishment template, you must add the replenish method to the wave template.</span></span>

1. <span data-ttu-id="27681-180">**メソッド** クイックタブの **選択したメソッド** 列で、次の行を確認します。</span><span class="sxs-lookup"><span data-stu-id="27681-180">On the **Methods** FastTab, in the **Selected methods** column, find the following line:</span></span>

    - <span data-ttu-id="27681-181">**メソッド名:** *補充*</span><span class="sxs-lookup"><span data-stu-id="27681-181">**Method name:** *replenish*</span></span>
    - <span data-ttu-id="27681-182">**名前:** *補充*</span><span class="sxs-lookup"><span data-stu-id="27681-182">**Name:** *Replenishment*</span></span>

1. <span data-ttu-id="27681-183">この行の **ウェーブ ステップ コード** フィールドを *補充* に設定します。</span><span class="sxs-lookup"><span data-stu-id="27681-183">Set the **Wave step code** field for this line to *Replen*.</span></span>
1. <span data-ttu-id="27681-184">**保存** を選択します。</span><span class="sxs-lookup"><span data-stu-id="27681-184">Select **Save**.</span></span>

## <a name="example-scenario"></a><span data-ttu-id="27681-185">シナリオ例</span><span class="sxs-lookup"><span data-stu-id="27681-185">Example scenario</span></span>

<span data-ttu-id="27681-186">上記で説明したサンプル データをすべて入手して設定したら、このシナリオを使用して *場所の能力を超える補充* 機能を試すことができます。</span><span class="sxs-lookup"><span data-stu-id="27681-186">After you've made all the previously described sample data available and set it up, you can work through this scenario to try out the *Replenishment over location capacity* feature.</span></span> <span data-ttu-id="27681-187">このシナリオに示されている値は、標準のデモデータで作業していて、**USMF** 法人を選択し、このトピックで既に説明したサンプル レコードを準備していることを前提としています。</span><span class="sxs-lookup"><span data-stu-id="27681-187">The values that are shown in this scenario assume that you're working with the standard demo data, that you selected the **USMF** legal entity, and that you prepared the sample records that are described earlier in this topic.</span></span> <span data-ttu-id="27681-188">このシナリオは、製品の設定で機能を使用する方法を示す例としても使用されます。</span><span class="sxs-lookup"><span data-stu-id="27681-188">This scenario also serves as an example that shows how the feature can be used in a production setting.</span></span>

### <a name="create-replenishment-work"></a><span data-ttu-id="27681-189">補充作業の作成</span><span class="sxs-lookup"><span data-stu-id="27681-189">Create replenishment work</span></span>

#### <a name="create-sales-order-1"></a><span data-ttu-id="27681-190">販売注文の作成 1</span><span class="sxs-lookup"><span data-stu-id="27681-190">Create sales order 1</span></span>

1. <span data-ttu-id="27681-191">**販売とマーケティング \> 販売注文 \> すべての販売注文** の順に移動します。</span><span class="sxs-lookup"><span data-stu-id="27681-191">Go to **Sales and marketing \> Sales orders \> All sales orders**.</span></span>
1. <span data-ttu-id="27681-192">アクション ウィンドウで **新規** を選択して、新しい販売注文を作成するダイアログ ボックスを開きます。</span><span class="sxs-lookup"><span data-stu-id="27681-192">On the Action Pane, select **New** to open a dialog box for creating a new sales order.</span></span>
1. <span data-ttu-id="27681-193">ダイアログ ボックスに次の値を設定します。</span><span class="sxs-lookup"><span data-stu-id="27681-193">In the dialog box, set the following values:</span></span>

    - <span data-ttu-id="27681-194">**顧客アカウント:** *US-007*</span><span class="sxs-lookup"><span data-stu-id="27681-194">**Customer account:** *US-007*</span></span>
    - <span data-ttu-id="27681-195">**倉庫:** *61*</span><span class="sxs-lookup"><span data-stu-id="27681-195">**Warehouse:** *61*</span></span>

1. <span data-ttu-id="27681-196">**OK** を選択して販売注文を作成し、ダイアログ ボックスを閉じます。</span><span class="sxs-lookup"><span data-stu-id="27681-196">Select **OK** to create the sales order and close the dialog box.</span></span>
1. <span data-ttu-id="27681-197">新しい販売注文が開かれます。</span><span class="sxs-lookup"><span data-stu-id="27681-197">The new sales order is opened.</span></span> <span data-ttu-id="27681-198">**販売注文行** クイック タブに新しい空の明細行が含まれています。</span><span class="sxs-lookup"><span data-stu-id="27681-198">It includes a new, empty line on the **Sales order lines** FastTab.</span></span> <span data-ttu-id="27681-199">この明細行で、次の値を設定します。</span><span class="sxs-lookup"><span data-stu-id="27681-199">On this line, set the following values:</span></span>

    - <span data-ttu-id="27681-200">**品目番号:** *T0100*</span><span class="sxs-lookup"><span data-stu-id="27681-200">**Item number:** *T0100*</span></span>
    - <span data-ttu-id="27681-201">**数量:** *40*</span><span class="sxs-lookup"><span data-stu-id="27681-201">**Quantity:** *40*</span></span>

1. <span data-ttu-id="27681-202">**販売注文行** クイック タブで、**在庫 \> 予約** を選択します。</span><span class="sxs-lookup"><span data-stu-id="27681-202">On the **Sales order lines** FastTab, select **Inventory \> Reservation**.</span></span>
1. <span data-ttu-id="27681-203">**予約** ページで、**ロットの予約** を選択します。</span><span class="sxs-lookup"><span data-stu-id="27681-203">On the **Reservation** page, select **Reserve lot**.</span></span>
1. <span data-ttu-id="27681-204">ページを閉じます。</span><span class="sxs-lookup"><span data-stu-id="27681-204">Close the page.</span></span>
1. <span data-ttu-id="27681-205">アクション ウィンドウの **倉庫** タブで、**倉庫へのリリース** を選択します。</span><span class="sxs-lookup"><span data-stu-id="27681-205">On the Action Pane, on the **Warehouse** tab, select **Release to warehouse**.</span></span>

    <span data-ttu-id="27681-206">作成したウェーブ ID と出荷 ID を示す情報メッセージを受信します。</span><span class="sxs-lookup"><span data-stu-id="27681-206">You receive informational messages that show the wave and shipment IDs that were created.</span></span> <span data-ttu-id="27681-207">補充ウェーブも作成されます。</span><span class="sxs-lookup"><span data-stu-id="27681-207">A replenishment wave is also created.</span></span>

    <span data-ttu-id="27681-208">また、"完了していない補充作業があるために業務 ID XXXX をブロック解除できません" という警告メッセージも表示されます。</span><span class="sxs-lookup"><span data-stu-id="27681-208">You also receive a warning message that states, "Work ID XXXX cannot be unblocked because it has unfinished replenishment work."</span></span>

#### <a name="create-sales-order-2"></a><span data-ttu-id="27681-209">販売注文の作成 2</span><span class="sxs-lookup"><span data-stu-id="27681-209">Create sales order 2</span></span>

1. <span data-ttu-id="27681-210">**すべての販売注文** ページのアクション ウィンドウで **新規** を選択して、新しい販売注文を作成するダイアログ ボックスを開きます。</span><span class="sxs-lookup"><span data-stu-id="27681-210">On the **All sales orders**, page, on the Action Pane, select **New** to open a dialog box for creating a new sales order.</span></span>
1. <span data-ttu-id="27681-211">ダイアログ ボックスに次の値を設定します。</span><span class="sxs-lookup"><span data-stu-id="27681-211">In the dialog box, set the following value:</span></span>

    - <span data-ttu-id="27681-212">**顧客アカウント:** *US-001*</span><span class="sxs-lookup"><span data-stu-id="27681-212">**Customer account:** *US-001*</span></span>
    - <span data-ttu-id="27681-213">**倉庫:** *61*</span><span class="sxs-lookup"><span data-stu-id="27681-213">**Warehouse:** *61*</span></span>

1. <span data-ttu-id="27681-214">**OK** を選択して販売注文を作成し、ダイアログ ボックスを閉じます。</span><span class="sxs-lookup"><span data-stu-id="27681-214">Select **OK** to create the sales order and close the dialog box.</span></span>
1. <span data-ttu-id="27681-215">新しい販売注文が開かれます。</span><span class="sxs-lookup"><span data-stu-id="27681-215">The new sales order is opened.</span></span> <span data-ttu-id="27681-216">**販売注文行** クイック タブに新しい空の明細行が含まれています。</span><span class="sxs-lookup"><span data-stu-id="27681-216">It includes a new, empty line on the **Sales order lines** FastTab.</span></span> <span data-ttu-id="27681-217">この明細行で、次の値を設定します。</span><span class="sxs-lookup"><span data-stu-id="27681-217">On this line, set the following values:</span></span>

    - <span data-ttu-id="27681-218">**品目番号:** *T0100*</span><span class="sxs-lookup"><span data-stu-id="27681-218">**Item number:** *T0100*</span></span>
    - <span data-ttu-id="27681-219">**数量:** *60*</span><span class="sxs-lookup"><span data-stu-id="27681-219">**Quantity:** *60*</span></span>

1. <span data-ttu-id="27681-220">**販売注文行** クイック タブで、**在庫 \> 予約** を選択します。</span><span class="sxs-lookup"><span data-stu-id="27681-220">On the **Sales order lines** FastTab, select **Inventory \> Reservation**.</span></span>
1. <span data-ttu-id="27681-221">**予約** ページで、**ロットの予約** を選択します。</span><span class="sxs-lookup"><span data-stu-id="27681-221">On the **Reservation** page, select **Reserve lot**.</span></span>
1. <span data-ttu-id="27681-222">ページを閉じます。</span><span class="sxs-lookup"><span data-stu-id="27681-222">Close the page.</span></span>
1. <span data-ttu-id="27681-223">アクション ウィンドウの **倉庫** タブで、**倉庫へのリリース** を選択します。</span><span class="sxs-lookup"><span data-stu-id="27681-223">On the Action Pane, on the **Warehouse** tab, select **Release to warehouse**.</span></span>

    <span data-ttu-id="27681-224">作成したウェーブ ID と出荷 ID を示す情報メッセージを受信します。</span><span class="sxs-lookup"><span data-stu-id="27681-224">You receive informational messages that show the wave and shipment IDs that were created.</span></span> <span data-ttu-id="27681-225">補充ウェーブも作成されます。</span><span class="sxs-lookup"><span data-stu-id="27681-225">A replenishment wave is also created.</span></span>

    <span data-ttu-id="27681-226">また、"完了していない補充作業があるために業務 ID XXXX をブロック解除できません" という警告メッセージも表示されます。</span><span class="sxs-lookup"><span data-stu-id="27681-226">You also receive a warning message that states, "Work ID XXXX cannot be unblocked because it has unfinished replenishment work."</span></span>

#### <a name="create-sales-order-3"></a><span data-ttu-id="27681-227">販売注文の作成 3</span><span class="sxs-lookup"><span data-stu-id="27681-227">Create sales order 3</span></span>

1. <span data-ttu-id="27681-228">**すべての販売注文** ページのアクション ウィンドウで **新規** を選択して、新しい販売注文を作成するダイアログ ボックスを開きます。</span><span class="sxs-lookup"><span data-stu-id="27681-228">On the **All sales orders** page, on the Action Pane, select **New** to open a dialog box for creating a new sales order.</span></span>
1. <span data-ttu-id="27681-229">ダイアログ ボックスに次の値を設定します。</span><span class="sxs-lookup"><span data-stu-id="27681-229">In the dialog box, set the following values:</span></span>

    - <span data-ttu-id="27681-230">**顧客アカウント:** *US-004*</span><span class="sxs-lookup"><span data-stu-id="27681-230">**Customer account:** *US-004*</span></span>
    - <span data-ttu-id="27681-231">**倉庫:** *61*</span><span class="sxs-lookup"><span data-stu-id="27681-231">**Warehouse:** *61*</span></span>

1. <span data-ttu-id="27681-232">**OK** を選択して販売注文を作成し、ダイアログ ボックスを閉じます。</span><span class="sxs-lookup"><span data-stu-id="27681-232">Select **OK** to create the sales order and close the dialog box.</span></span>
1. <span data-ttu-id="27681-233">新しい販売注文が開かれます。</span><span class="sxs-lookup"><span data-stu-id="27681-233">The new sales order is opened.</span></span> <span data-ttu-id="27681-234">**販売注文行** クイック タブに新しい空の明細行が含まれています。</span><span class="sxs-lookup"><span data-stu-id="27681-234">It includes a new, empty line on the **Sales order lines** FastTab.</span></span> <span data-ttu-id="27681-235">この明細行で、次の値を設定します。</span><span class="sxs-lookup"><span data-stu-id="27681-235">On this line, set the following values:</span></span>

    - <span data-ttu-id="27681-236">**品目番号:** *T0100*</span><span class="sxs-lookup"><span data-stu-id="27681-236">**Item number:** *T0100*</span></span>
    - <span data-ttu-id="27681-237">**数量:** *30*</span><span class="sxs-lookup"><span data-stu-id="27681-237">**Quantity:** *30*</span></span>

1. <span data-ttu-id="27681-238">**販売注文行** クイック タブで、**在庫 \> 予約** を選択します。</span><span class="sxs-lookup"><span data-stu-id="27681-238">On the **Sales order lines** FastTab, select **Inventory \> Reservation**.</span></span>
1. <span data-ttu-id="27681-239">**予約** ページで、**ロットの予約** を選択します。</span><span class="sxs-lookup"><span data-stu-id="27681-239">On the **Reservation** page, select **Reserve lot**.</span></span>
1. <span data-ttu-id="27681-240">ページを閉じます。</span><span class="sxs-lookup"><span data-stu-id="27681-240">Close the page.</span></span>
1. <span data-ttu-id="27681-241">アクション ウィンドウの **倉庫** タブで、**倉庫へのリリース** を選択します。</span><span class="sxs-lookup"><span data-stu-id="27681-241">On the Action Pane, on the **Warehouse** tab, select **Release to warehouse**.</span></span>

    <span data-ttu-id="27681-242">作成したウェーブ ID と出荷 ID を示す情報メッセージを受信します。</span><span class="sxs-lookup"><span data-stu-id="27681-242">You receive informational messages that show the wave and shipment IDs that were created.</span></span> <span data-ttu-id="27681-243">補充ウェーブも作成されます。</span><span class="sxs-lookup"><span data-stu-id="27681-243">A replenishment wave is also created.</span></span>

    <span data-ttu-id="27681-244">また、"完了していない補充作業があるために業務 ID XXXX をブロック解除できません" という警告メッセージも表示されます。</span><span class="sxs-lookup"><span data-stu-id="27681-244">You also receive a warning message that states, "Work ID XXXX cannot be unblocked because it has unfinished replenishment work."</span></span>

#### <a name="view-work-details"></a><span data-ttu-id="27681-245">作業の詳細を表示する</span><span class="sxs-lookup"><span data-stu-id="27681-245">View work details</span></span>

1. <span data-ttu-id="27681-246">**倉庫管理 \> 作業 \> 作業の詳細** の順に移動します。</span><span class="sxs-lookup"><span data-stu-id="27681-246">Go to **Warehouse management \> Work \> Work details**.</span></span>
1. <span data-ttu-id="27681-247">**概要** セクションで、倉庫 *61* の **倉庫** 列をフィルタリングします。</span><span class="sxs-lookup"><span data-stu-id="27681-247">In the **Overview** section, filter the **Warehouse** column for warehouse *61*.</span></span>
1. <span data-ttu-id="27681-248">3 つの需要販売注文に対して 7 つの作業 ID が作成されたことを確認します。</span><span class="sxs-lookup"><span data-stu-id="27681-248">You should see that seven work IDs were created for the three demand sales orders.</span></span>

    - <span data-ttu-id="27681-249">7 つの作業 ID のうち 3 つには、**作業指示タイプ** 値 *補充* があり、4 つには **作業指示タイプ** 値が *販売注文* があります。</span><span class="sxs-lookup"><span data-stu-id="27681-249">Three of the seven work IDs have a **Work order type** value of *Replenishment*, and four have a **Work order type** value of *Sales orders*.</span></span>
    - <span data-ttu-id="27681-250">**作業指示タイプ** 値が *補充* である 3 つのすべての作業 ID は、**明細行** セクションで同じ *ピッキング* 場所と *プット* 場所になります。</span><span class="sxs-lookup"><span data-stu-id="27681-250">All three work IDs that have a **Work order type** value of *Replenishment* have the same *Pick* and *Put* locations in the **Lines** section:</span></span>

        - <span data-ttu-id="27681-251">**ピッキング:** *02A01R5S1B*</span><span class="sxs-lookup"><span data-stu-id="27681-251">**Pick:** *02A01R5S1B*</span></span>
        - <span data-ttu-id="27681-252">**プット:** *06A01R2S1B*</span><span class="sxs-lookup"><span data-stu-id="27681-252">**Put:** *06A01R2S1B*</span></span>

    - <span data-ttu-id="27681-253">販売注文 1 に対して 2 つの作業 ID が作成されました。</span><span class="sxs-lookup"><span data-stu-id="27681-253">Two work IDs were created for sales order 1.</span></span>

1. <span data-ttu-id="27681-254">販売注文の作業 ID をメモします。</span><span class="sxs-lookup"><span data-stu-id="27681-254">Make a note of the work IDs for the sales orders.</span></span>

<span data-ttu-id="27681-255">手持在庫の数量に応じて、作成される作業数量は多少異なる場合があります。</span><span class="sxs-lookup"><span data-stu-id="27681-255">Depending on your on-hand quantities, the work quantities that are created might vary slightly.</span></span> <span data-ttu-id="27681-256">ただし、全体として、作成される作業ヘッダーは、このシナリオの例と一致している必要があります。</span><span class="sxs-lookup"><span data-stu-id="27681-256">However, overall, the work headers that are created should match this scenario example.</span></span>

#### <a name="on-hand-inventory-license-plate-id"></a><span data-ttu-id="27681-257">手持在庫のライセンス プレート ID</span><span class="sxs-lookup"><span data-stu-id="27681-257">On-hand inventory license plate ID</span></span>

<span data-ttu-id="27681-258">このシナリオの後半で、倉庫アプリ (またはエミュレーター) を使用して、ピッキングおよび補充のシナリオを完了するためのライセンス プレートを指定する必要があります。</span><span class="sxs-lookup"><span data-stu-id="27681-258">Later in this scenario, you will use the warehouse app (or an emulator), where you must identify the license plate to complete the picking and replenishment scenarios.</span></span>

<span data-ttu-id="27681-259">後で必要になるライセンス版 ID を検索するには、次の手順に従います。</span><span class="sxs-lookup"><span data-stu-id="27681-259">To find the license plate IDs that you will need later, follow these steps.</span></span>

1. <span data-ttu-id="27681-260">**在庫管理 \> 照会およびレポート \> 手持在庫リスト** の順に移動します。</span><span class="sxs-lookup"><span data-stu-id="27681-260">Go to **Inventory management \> Inquiries and reports \> On-hand list**.</span></span>
1. <span data-ttu-id="27681-261">フィルタ ウィンドウを開くには、**フィルタを表示** ボタンを選択します。</span><span class="sxs-lookup"><span data-stu-id="27681-261">Select the **Show filters** button to open the filter pane.</span></span>
1. <span data-ttu-id="27681-262">シナリオのライセンス プレートを取得するには、次のフィルタ条件を入力します。</span><span class="sxs-lookup"><span data-stu-id="27681-262">Enter the following filtering criteria to get the license plates for the scenario.</span></span> <span data-ttu-id="27681-263">*で始まる* フィルターを使用します。</span><span class="sxs-lookup"><span data-stu-id="27681-263">Use the *begins with* filter.</span></span>

    - <span data-ttu-id="27681-264">**品目番号:** *T0100*</span><span class="sxs-lookup"><span data-stu-id="27681-264">**Item number:** *T0100*</span></span>
    - <span data-ttu-id="27681-265">**倉庫:** *61*</span><span class="sxs-lookup"><span data-stu-id="27681-265">**Warehouse:** *61*</span></span>

1. <span data-ttu-id="27681-266">**適用** を選択します。</span><span class="sxs-lookup"><span data-stu-id="27681-266">Select **Apply**.</span></span>
1. <span data-ttu-id="27681-267">アクション ペインで、**分析コード** を選択します。</span><span class="sxs-lookup"><span data-stu-id="27681-267">On the Action Pane, select **Dimensions**.</span></span>
1. <span data-ttu-id="27681-268">**分析コード表示** ダイアログ ボックスの **保管分析コード** セクションで、すべての値を選択します。</span><span class="sxs-lookup"><span data-stu-id="27681-268">In the **Dimensions display** dialog box, in the **Storage Dimensions** section, select all the values.</span></span>
1. <span data-ttu-id="27681-269">**トランザクション** セクションで、**品目番号** と **数量 \<\> 0** を選択します。</span><span class="sxs-lookup"><span data-stu-id="27681-269">In the **Transactions** section, select **Item number** and **Quantity \<\> 0**.</span></span>
1. <span data-ttu-id="27681-270">完了後は、**OK** を選択して、ダイアログ ボックスを閉じます。</span><span class="sxs-lookup"><span data-stu-id="27681-270">When you've finished, select **OK** to close the dialog box.</span></span>
1. <span data-ttu-id="27681-271">**手持在庫** グリッドには、各場所にある品目 *T0100* のライセンス プレート番号が表示され ます。</span><span class="sxs-lookup"><span data-stu-id="27681-271">The **On-hand** grid shows the license plate numbers for item *T0100* in each location.</span></span> <span data-ttu-id="27681-272">後でこの情報を必要とするため、各場所にあるライセンス プレートを書き留めておきます。</span><span class="sxs-lookup"><span data-stu-id="27681-272">Make a note of the license plate that is in each location, because you will need this information later.</span></span>
1. <span data-ttu-id="27681-273">ページを閉じます。</span><span class="sxs-lookup"><span data-stu-id="27681-273">Close the page.</span></span>

### <a name="process-steps"></a><span data-ttu-id="27681-274">プロセスの手順</span><span class="sxs-lookup"><span data-stu-id="27681-274">Process steps</span></span>

<span data-ttu-id="27681-275">最初の 2 つの作業 ID に対して倉庫の場所の補充を実行します。</span><span class="sxs-lookup"><span data-stu-id="27681-275">You will perform the warehouse location replenishment for the first two work IDs.</span></span> <span data-ttu-id="27681-276">3 つ目の補充作業は、ピッキング場所の在庫レベルがしきい値を下回るまでブロックされます。</span><span class="sxs-lookup"><span data-stu-id="27681-276">Work on the third replenishment work will be blocked until the inventory level in the picking location falls below the threshold.</span></span>

#### <a name="replenishment"></a><span data-ttu-id="27681-277">補充</span><span class="sxs-lookup"><span data-stu-id="27681-277">Replenishment</span></span>

1. <span data-ttu-id="27681-278">倉庫 *61* でユーザーとして倉庫アプリにサインインします。</span><span class="sxs-lookup"><span data-stu-id="27681-278">Sign in to the warehouse app as a user in warehouse *61*.</span></span> <span data-ttu-id="27681-279">(ユーザー ID として *61* を、パスワードとして *1* を入力します。)</span><span class="sxs-lookup"><span data-stu-id="27681-279">(Enter *61* as the user ID and *1* as the password.)</span></span>
1. <span data-ttu-id="27681-280">**在庫 \> 補充** に移動します。</span><span class="sxs-lookup"><span data-stu-id="27681-280">Go to **Inventory \> Replenishment**.</span></span>

    <span data-ttu-id="27681-281">最初の補充作業を完了するように求めるメッセージが表示されます。</span><span class="sxs-lookup"><span data-stu-id="27681-281">You're prompted to complete the first replenishment work.</span></span> <span data-ttu-id="27681-282">品目番号、数量、ピッキング元の場所が表示されます。</span><span class="sxs-lookup"><span data-stu-id="27681-282">The item number, quantity, and location to pick from are shown.</span></span>

1. <span data-ttu-id="27681-283">**LP** フィールドに、表示される場所における品目のライセンス プレート番号を入力します。</span><span class="sxs-lookup"><span data-stu-id="27681-283">In the **LP** field, enter the license plate number for the item in the location that is shown.</span></span>
1. <span data-ttu-id="27681-284">**OK** ボタン (チェックマーク記号) を選択します。</span><span class="sxs-lookup"><span data-stu-id="27681-284">Select the **OK** button (check mark symbol).</span></span>

    <span data-ttu-id="27681-285">ピッキングされた品目の新しいライセンス プレートに対して、ターゲットのライセンス プレート番号が生成されます。</span><span class="sxs-lookup"><span data-stu-id="27681-285">The system generates a target license plate number for the new license plate for the picked item.</span></span>

1. <span data-ttu-id="27681-286">**OK** を選択して値を確定します。</span><span class="sxs-lookup"><span data-stu-id="27681-286">Select **OK** to confirm the value.</span></span>

    <span data-ttu-id="27681-287">ターゲットのライセンス プレートを補充場所にプットするようにユーザーに指示するプット作業を表示します。</span><span class="sxs-lookup"><span data-stu-id="27681-287">Put work is shown that instructs the user to put the target license plate into the replenishment location.</span></span> <span data-ttu-id="27681-288">*プット* の場所は **06A01R2S1B** である必要があります。</span><span class="sxs-lookup"><span data-stu-id="27681-288">The *Put* location should be **06A01R2S1B**.</span></span>

1. <span data-ttu-id="27681-289">プットの詳細を確認し、**OK** を選択します。</span><span class="sxs-lookup"><span data-stu-id="27681-289">Confirm the put details, and select **OK**.</span></span>

    <span data-ttu-id="27681-290">"作業が完了しました" というメッセージが表示され、次の補充ピック タスクの詳細が表示されます (品目番号、数量、およびピッキング元の場所)。</span><span class="sxs-lookup"><span data-stu-id="27681-290">You receive a "Work Completed" message, and the details of the next replenishment pick task are shown: the item number, quantity, and location to pick from.</span></span> <span data-ttu-id="27681-291">ピッキング場所は、最初の補充場所と同じになります。</span><span class="sxs-lookup"><span data-stu-id="27681-291">The picking location will be the same as the first replenishment location.</span></span> <span data-ttu-id="27681-292">したがって、ライセンス プレートには、最初の補充作業タスクで使用されたものと同じライセンス プレート ID が使用されます。</span><span class="sxs-lookup"><span data-stu-id="27681-292">Therefore, the license plate will have the same license plate ID that was used for the first replenishment work task.</span></span>

1. <span data-ttu-id="27681-293">前の手順を繰り返して、2 番目の作業タスクの補充作業を完了します。</span><span class="sxs-lookup"><span data-stu-id="27681-293">Repeat the preceding steps to complete the replenishment work for the second work task.</span></span> <span data-ttu-id="27681-294">数量およびターゲットのライセンス プレートは、最初の作業タスクの数量およびターゲット ライセンス プレートとは異なります。</span><span class="sxs-lookup"><span data-stu-id="27681-294">The quantity and target license plate will differ from the quantity and target license plate for the first work task.</span></span>

<span data-ttu-id="27681-295">2 つ目の補充作業が完了すると、"作業が完了しました" というメッセージが表示されます。</span><span class="sxs-lookup"><span data-stu-id="27681-295">After the second replenishment work is completed, you receive a "Work Completed" message.</span></span> <span data-ttu-id="27681-296">また、補充作業が残っている場合でも、利用可能な作業がないことがモバイル デバイスから通知されます。</span><span class="sxs-lookup"><span data-stu-id="27681-296">The mobile device also informs you that there is no work available, even though some replenishment work remains.</span></span> <span data-ttu-id="27681-297">この現象は、補充作業のステータスが *保留中* になっているため、**ブロック済** としてマークされていることが原因です。</span><span class="sxs-lookup"><span data-stu-id="27681-297">This behavior occurs because the replenishment work has an availability status of *Held* and is therefore marked as **Blocked**.</span></span>

<span data-ttu-id="27681-298">この *保留* ス テータスが発生するのは、作業が割り当てられているピッキング場所の場所プロファイルの **オーバーフロー数量** 値が *0.65 PL* であるためです。</span><span class="sxs-lookup"><span data-stu-id="27681-298">The *Held* status was triggered because the location profile for the picking location that the work is being assigned to has an **Overflow quantity** value of *0.65 PL*.</span></span> <span data-ttu-id="27681-299">以前の 2 つの補充作業タスクにより、この場所は、品目 *T0100* のオーバーフロー制限数に近くなります。</span><span class="sxs-lookup"><span data-stu-id="27681-299">The two previous replenishment work tasks filled the location almost to its overflow limit for item *T0100*.</span></span> <span data-ttu-id="27681-300">(品目の単位換算は *1 PL = 100 ea*)。したがって、残りの補充作業によって、場所のオーバーフロー制限を超えていることになります。</span><span class="sxs-lookup"><span data-stu-id="27681-300">(The unit conversion for the item is *1 PL = 100 ea*.) Therefore, the remaining replenishment work would cause the location to exceed its overflow limit.</span></span>

<span data-ttu-id="27681-301">モバイル デバイス メニュー項目の作業リリースしきい値を下回る十分な在庫が保管場所からピッキングされるまで、この補充作業はブロックされたままになります。</span><span class="sxs-lookup"><span data-stu-id="27681-301">Until enough inventory is picked from the location to bring it below the work release threshold on the mobile device menu item, this replenishment work will remain blocked.</span></span>

#### <a name="sales-order-pick"></a><span data-ttu-id="27681-302">販売注文のピッキング</span><span class="sxs-lookup"><span data-stu-id="27681-302">Sales order pick</span></span>

<span data-ttu-id="27681-303">残りの補充作業タスクを完了する前に、ピッキング場所の在庫を消費して、残りの補充作業のブロックを解除できるレベルにする必要があります。</span><span class="sxs-lookup"><span data-stu-id="27681-303">Before the remaining replenishment work task can be completed, the picking location must be depleted of inventory to a level where the remaining replenishment work can be unblocked.</span></span> <span data-ttu-id="27681-304">つまり、保管場所の手持在庫の数量と補充数量の合計が、**オーバーフロー数量** 値を超えることはできません。</span><span class="sxs-lookup"><span data-stu-id="27681-304">In other words, the sum of the quantity of on-hand inventory in the location and the replenishment quantity can't exceed the **Overflow quantity** value.</span></span> <span data-ttu-id="27681-305">この合計がオーバーフロー数量を下回ると、残りの補充作業のブロックが解除されます。</span><span class="sxs-lookup"><span data-stu-id="27681-305">When this sum is less than the overflow quantity, the remaining replenishment work will be unblocked.</span></span>

1. <span data-ttu-id="27681-306">倉庫 *61* でユーザーとして倉庫アプリにサインインします。</span><span class="sxs-lookup"><span data-stu-id="27681-306">Sign in to the warehouse app as a user in warehouse *61*.</span></span> <span data-ttu-id="27681-307">(ユーザー ID として *61* を、パスワードとして *1* を入力します。)</span><span class="sxs-lookup"><span data-stu-id="27681-307">(Enter *61* as the user ID and *1* as the password.)</span></span>
1. <span data-ttu-id="27681-308">**出荷 \> 販売ピッキング** に移動します。</span><span class="sxs-lookup"><span data-stu-id="27681-308">Go to **Outbound \> Sales Picking**.</span></span>
1. <span data-ttu-id="27681-309">販売注文 1 の最初の作業 ID を入力します。</span><span class="sxs-lookup"><span data-stu-id="27681-309">Enter the first work ID for sales order 1.</span></span>

    <span data-ttu-id="27681-310">**作業の詳細** ページで、前にメモした販売注文の作業 ID を参照します。</span><span class="sxs-lookup"><span data-stu-id="27681-310">Refer to the work IDs for sales orders that you made a note of earlier, on the **Work details** page.</span></span> <span data-ttu-id="27681-311">ここに入力した作業 ID は、2 つの異なる場所から 10 個の数量のピッキング作業を生成します。</span><span class="sxs-lookup"><span data-stu-id="27681-311">The work ID that you enter here will generate pick work for a quantity of 10 ea from two separate locations.</span></span>

1. <span data-ttu-id="27681-312">**OK** を選択します。</span><span class="sxs-lookup"><span data-stu-id="27681-312">Select **OK**.</span></span>

    <span data-ttu-id="27681-313">**販売注文: ピッキング** タスク ページには、最初の保管場所に対してピッキングする品目番号、数量、および場所が表示されます。</span><span class="sxs-lookup"><span data-stu-id="27681-313">The **Sales orders: Pick** task page shows the item number, quantity, and location to pick from for the first location.</span></span>

1. <span data-ttu-id="27681-314">**LP** フィールドに、表示される場所における品目のライセンス プレート番号を入力します。</span><span class="sxs-lookup"><span data-stu-id="27681-314">In the **LP** field, enter the license plate number for the item in the location that is shown.</span></span>
1. <span data-ttu-id="27681-315">**OK** ボタン (チェックマーク記号) を選択します。</span><span class="sxs-lookup"><span data-stu-id="27681-315">Select the **OK** button (check mark symbol).</span></span>

    <span data-ttu-id="27681-316">**販売注文: ピッキング** タスク ページには、次の保管場所に対してピッキングする品目番号、数量、および場所が表示されます。</span><span class="sxs-lookup"><span data-stu-id="27681-316">The **Sales orders: Pick** task page shows the item number, quantity, and location to pick from for the next location.</span></span>

1. <span data-ttu-id="27681-317">**LP** フィールドに、表示される場所における品目のライセンス プレート番号を入力します。</span><span class="sxs-lookup"><span data-stu-id="27681-317">In the **LP** field, enter the license plate number for the item in the location that is shown.</span></span>
1. <span data-ttu-id="27681-318">**OK** ボタン (チェックマーク記号) を選択します。</span><span class="sxs-lookup"><span data-stu-id="27681-318">Select the **OK** button (check mark symbol).</span></span>

    <span data-ttu-id="27681-319">**販売注文: プット** ページでは、完了した両方のピッキング作業を送信側のステージングの場所にプットするように指示されます。</span><span class="sxs-lookup"><span data-stu-id="27681-319">The **Sales orders: Put** page instructs you to put away both the completed picking works to the outbound staging location.</span></span>

1. <span data-ttu-id="27681-320">**OK** を選択します。</span><span class="sxs-lookup"><span data-stu-id="27681-320">Select **OK**.</span></span>

    <span data-ttu-id="27681-321">「作業が完了しました」というメッセージが表示されます。</span><span class="sxs-lookup"><span data-stu-id="27681-321">You receive a "Work Completed" message.</span></span>

1. <span data-ttu-id="27681-322">販売注文 1 の 2 番目の作業 ID を入力します。</span><span class="sxs-lookup"><span data-stu-id="27681-322">Enter the second work ID for sales order 1.</span></span>

    <span data-ttu-id="27681-323">この作業 ID に対してピック タスクは 1 つしかありません。</span><span class="sxs-lookup"><span data-stu-id="27681-323">There is only one pick task for this work ID.</span></span>

1. <span data-ttu-id="27681-324">**OK** を選択します。</span><span class="sxs-lookup"><span data-stu-id="27681-324">Select **OK**.</span></span>

    <span data-ttu-id="27681-325">**販売注文: ピッキング** タスク ページには、ピッキング元の品目番号、数量、および場所が表示されます。</span><span class="sxs-lookup"><span data-stu-id="27681-325">The **Sales orders: Pick** task page shows the item number, quantity, and location to pick from.</span></span>

1. <span data-ttu-id="27681-326">**LP** フィールドに、表示される場所における品目のライセンス プレート番号を入力します。</span><span class="sxs-lookup"><span data-stu-id="27681-326">In the **LP** field, enter the license plate number for the item in the location that is shown.</span></span>

    <span data-ttu-id="27681-327">指定したライセンス プレートは、補充作業タスクのシステム生成のライセンス プレートのいずれかになります。</span><span class="sxs-lookup"><span data-stu-id="27681-327">The license plate that you specify will be one of the system-generated license plates from the replenishment work tasks.</span></span> <span data-ttu-id="27681-328">適切なライセンス プレート ID を取り込んでいることを確認するには、**手持在庫リスト** ページで、品目、場所、および数量の在庫を確認します。</span><span class="sxs-lookup"><span data-stu-id="27681-328">To make sure that you capture the correct license plate ID, check the inventory on the **On-hand list** page for the item, location, and quantity.</span></span>

1. <span data-ttu-id="27681-329">**OK** ボタン (チェックマーク記号) を選択します。</span><span class="sxs-lookup"><span data-stu-id="27681-329">Select the **OK** button (check mark symbol).</span></span>
1. <span data-ttu-id="27681-330">送信側のステージング場所に対するプット タスクの指示を確認します。</span><span class="sxs-lookup"><span data-stu-id="27681-330">Confirm the instructions for the put task to the outbound staging location.</span></span>
1. <span data-ttu-id="27681-331">**OK** を選択します。</span><span class="sxs-lookup"><span data-stu-id="27681-331">Select **OK**.</span></span>

    <span data-ttu-id="27681-332">「作業が完了しました」というメッセージが表示されます。</span><span class="sxs-lookup"><span data-stu-id="27681-332">You receive a "Work Completed" message.</span></span>

<span data-ttu-id="27681-333">販売注文 2 は、リンク先の補充タスクが完了していないので、ピッキングをブロックされます。</span><span class="sxs-lookup"><span data-stu-id="27681-333">Sales order 2 is blocked from picking because the replenishment task that it's linked to isn't completed.</span></span> <span data-ttu-id="27681-334">現時点では、ピッキング場所に 30 個の数量があり、さらに販売注文 2 の補充数量が 60 個になっています。</span><span class="sxs-lookup"><span data-stu-id="27681-334">Currently, there is still a quantity of 30 ea in the picking location, and the replenishment quantity for sales order 2 is 60 ea.</span></span> <span data-ttu-id="27681-335">手持在庫と補充在庫の合計 (90 個) が、0.65 PL (つまり 65 個) のオーバーフロー数量を超えています。</span><span class="sxs-lookup"><span data-stu-id="27681-335">The sum of the on-hand inventory and the replenishment inventory (90 ea) exceeds the overflow quantity of 0.65 PL (or 65 ea).</span></span> <span data-ttu-id="27681-336">補充作業を完了する前に、販売注文 3 をピッキングする必要があります。</span><span class="sxs-lookup"><span data-stu-id="27681-336">Before the replenishment work can be completed, sales order 3 must be picked.</span></span>

1. <span data-ttu-id="27681-337">販売注文 3 の作業 ID を入力します。</span><span class="sxs-lookup"><span data-stu-id="27681-337">Enter the work ID for sales order 3.</span></span>

    <span data-ttu-id="27681-338">この作業 ID に対してピック タスクは 1 つしかありません。</span><span class="sxs-lookup"><span data-stu-id="27681-338">There is only one pick task for this work ID.</span></span>

1. <span data-ttu-id="27681-339">**OK** を選択します。</span><span class="sxs-lookup"><span data-stu-id="27681-339">Select **OK**.</span></span>

    <span data-ttu-id="27681-340">**販売注文: ピッキング** タスク ページには、ピッキング元の品目番号、数量、および場所が表示されます。</span><span class="sxs-lookup"><span data-stu-id="27681-340">The **Sales orders: Pick** task page shows the item number, quantity, and location to pick from.</span></span>

1. <span data-ttu-id="27681-341">**LP** フィールドに、表示される場所における品目のライセンス プレート番号を入力します。</span><span class="sxs-lookup"><span data-stu-id="27681-341">In the **LP** field, enter the license plate number for the item in the location that is shown.</span></span>

    <span data-ttu-id="27681-342">指定したライセンス プレートは、補充作業タスクのシステム生成のライセンス プレートのいずれかになります。</span><span class="sxs-lookup"><span data-stu-id="27681-342">The license plate that you specify will be one of the system-generated license plates from the replenishment work tasks.</span></span> <span data-ttu-id="27681-343">適切なライセンス プレート ID を取り込んでいることを確認するには、**手持在庫リスト** ページで、品目、場所、および数量の在庫を確認します。</span><span class="sxs-lookup"><span data-stu-id="27681-343">To make sure that you capture the correct license plate ID, check the inventory on the **On-hand list** page for the item, location, and quantity.</span></span>

1. <span data-ttu-id="27681-344">**OK** ボタン (チェックマーク記号) を選択します。</span><span class="sxs-lookup"><span data-stu-id="27681-344">Select the **OK** button (check mark symbol).</span></span>
1. <span data-ttu-id="27681-345">送信側のステージング場所に対するプット タスクの指示を確認します。</span><span class="sxs-lookup"><span data-stu-id="27681-345">Confirm the instructions for the put task to the outbound staging location.</span></span>
1. <span data-ttu-id="27681-346">**OK** を選択します。</span><span class="sxs-lookup"><span data-stu-id="27681-346">Select **OK**.</span></span>

    <span data-ttu-id="27681-347">「作業が完了しました」というメッセージが表示されます。</span><span class="sxs-lookup"><span data-stu-id="27681-347">You receive a "Work Completed" message.</span></span>

<span data-ttu-id="27681-348">ピッキング場所の手持在庫数量の合計と補充数量がしきい値を下回った時点で、残りの補充作業を処理できるようになります。</span><span class="sxs-lookup"><span data-stu-id="27681-348">As soon as the sum of the on-hand quantity in the picking location and the replenishment quantity is below the threshold, you will be able to process the remaining replenishment work.</span></span>

<span data-ttu-id="27681-349">**作業の詳細** ページに戻り、補充を受け入れるための十分な領域が確保されているため、最終の補充 (販売注文 2) の補充作業の利用可能性が *オープン* になっていることを確認します。</span><span class="sxs-lookup"><span data-stu-id="27681-349">Return to the **Work details** page, and notice that the replenishment work availability for the final piece of replenishment (for sales order 2) is *Open*, because there is now enough space in the location to accept the replenishment.</span></span>

<span data-ttu-id="27681-350">これで、この補充の作業をモバイル デバイス経由で処理できるようになります。</span><span class="sxs-lookup"><span data-stu-id="27681-350">You can now process this replenishment work via the mobile device.</span></span>

1. <span data-ttu-id="27681-351">**在庫 \> 補充** に移動します。</span><span class="sxs-lookup"><span data-stu-id="27681-351">Go to **Inventory \> Replenishment**.</span></span>

    <span data-ttu-id="27681-352">残りの補充作業を完了するように求めるメッセージが表示されます。</span><span class="sxs-lookup"><span data-stu-id="27681-352">You're prompted to complete the remaining replenishment work.</span></span> <span data-ttu-id="27681-353">品目番号、数量、ピッキング元の場所が表示されます。</span><span class="sxs-lookup"><span data-stu-id="27681-353">The item number, quantity, and location to pick from are shown.</span></span>

1. <span data-ttu-id="27681-354">**LP** フィールドに、表示される場所における品目のライセンス プレート番号を入力します。</span><span class="sxs-lookup"><span data-stu-id="27681-354">In the **LP** field, enter the license plate number for the item in the location that is shown.</span></span>
1. <span data-ttu-id="27681-355">**OK** ボタン (チェックマーク記号) を選択します。</span><span class="sxs-lookup"><span data-stu-id="27681-355">Select the **OK** button (check mark symbol).</span></span>

    <span data-ttu-id="27681-356">ピッキングされた品目の新しいライセンス プレートに対して、ターゲットのライセンス プレート番号が生成されます。</span><span class="sxs-lookup"><span data-stu-id="27681-356">The system generates a target license plate number for the new license plate for the picked item.</span></span>

1. <span data-ttu-id="27681-357">**OK** を選択して値を確定します。</span><span class="sxs-lookup"><span data-stu-id="27681-357">Select **OK** to confirm the value.</span></span>

    <span data-ttu-id="27681-358">ターゲットのライセンス プレートを補充場所にプットするようにユーザーに指示するプット作業を表示します。</span><span class="sxs-lookup"><span data-stu-id="27681-358">Put work is shown that instructs the user to put the target license plate into the replenishment location.</span></span> <span data-ttu-id="27681-359">*プット* の場所は **06A01R2S1B** である必要があります。</span><span class="sxs-lookup"><span data-stu-id="27681-359">The *Put* location should be **06A01R2S1B**.</span></span>

1. <span data-ttu-id="27681-360">プットの詳細を確認し、**OK** を選択します。</span><span class="sxs-lookup"><span data-stu-id="27681-360">Confirm the put details, and select **OK**.</span></span>

    <span data-ttu-id="27681-361">"作業が完了しました" と "利用できません" というメッセージが表示されます。</span><span class="sxs-lookup"><span data-stu-id="27681-361">You receive "Work Completed" and "No Work Available" messages.</span></span>

<span data-ttu-id="27681-362">販売注文 2 をピッキングできるようになりました。</span><span class="sxs-lookup"><span data-stu-id="27681-362">You can now pick sales order 2.</span></span> <span data-ttu-id="27681-363">販売注文に関連付けられている補充作業が完了したときにブロック解除されました。</span><span class="sxs-lookup"><span data-stu-id="27681-363">It became unblocked when the replenishment work that is linked to the sales order was completed.</span></span>

1. <span data-ttu-id="27681-364">販売注文 2 の作業 ID を入力します。</span><span class="sxs-lookup"><span data-stu-id="27681-364">Enter the work ID for sales order 2.</span></span>

    <span data-ttu-id="27681-365">この作業 ID に対してピック タスクは 1 つしかありません。</span><span class="sxs-lookup"><span data-stu-id="27681-365">There is only one pick task for this work ID.</span></span>

1. <span data-ttu-id="27681-366">**OK** を選択します。</span><span class="sxs-lookup"><span data-stu-id="27681-366">Select **OK**.</span></span>

    <span data-ttu-id="27681-367">**販売注文: ピッキング** タスク ページには、ピッキング元の品目番号、数量、および場所が表示されます。</span><span class="sxs-lookup"><span data-stu-id="27681-367">The **Sales orders: Pick** task page shows the item number, quantity, and location to pick from.</span></span>

1. <span data-ttu-id="27681-368">**LP** フィールドに、表示される場所における品目のライセンス プレート番号を入力します。</span><span class="sxs-lookup"><span data-stu-id="27681-368">In the **LP** field, enter the license plate number for the item in the location that is shown.</span></span>

    <span data-ttu-id="27681-369">指定したライセンス プレートは、補充作業タスクのシステム生成のライセンス プレートになります。</span><span class="sxs-lookup"><span data-stu-id="27681-369">The license plate that you specify will be the system-generated license plate from the replenishment work task.</span></span> <span data-ttu-id="27681-370">適切なライセンス プレート ID を取り込んでいることを確認するには、**手持在庫リスト** ページで、品目、場所、および数量の在庫を確認します。</span><span class="sxs-lookup"><span data-stu-id="27681-370">To make sure that you capture the correct license plate ID, check the inventory on the **On-hand list** page for the item, location, and quantity.</span></span>

1. <span data-ttu-id="27681-371">**OK** ボタン (チェックマーク記号) を選択します。</span><span class="sxs-lookup"><span data-stu-id="27681-371">Select the **OK** button (check mark symbol).</span></span>
1. <span data-ttu-id="27681-372">送信側のステージング場所に対するプット タスクの指示を確認します。</span><span class="sxs-lookup"><span data-stu-id="27681-372">Confirm the instructions for the put task to the outbound staging location.</span></span>
1. <span data-ttu-id="27681-373">**OK** を選択します。</span><span class="sxs-lookup"><span data-stu-id="27681-373">Select **OK**.</span></span>

    <span data-ttu-id="27681-374">「作業が完了しました」というメッセージが表示されます。</span><span class="sxs-lookup"><span data-stu-id="27681-374">You receive a "Work Completed" message.</span></span>

## <a name="notes-and-tips"></a><span data-ttu-id="27681-375">メモとヒント</span><span class="sxs-lookup"><span data-stu-id="27681-375">Notes and tips</span></span>

- <span data-ttu-id="27681-376">この機能は、すべてのタイプの補充 (ウェーブ受容、最小/最大、積荷需要、およびス六ティング) で機能します。</span><span class="sxs-lookup"><span data-stu-id="27681-376">This functionality works with all types of replenishment: wave demand, min/max, load demand, and slotting.</span></span>
- <span data-ttu-id="27681-377">必要に応じて、**作業の詳細** ページから、各作業ヘッダーの各作業時間の補充を手動で無効にすることができます。</span><span class="sxs-lookup"><span data-stu-id="27681-377">You can manually override the replenishment work availability for each work header from the **Work details** page if you want.</span></span>
- <span data-ttu-id="27681-378">補充作業の利用可能性がシステムによって設定されると、作業が完了する前にその場所に既に存在する在庫が考慮されます</span><span class="sxs-lookup"><span data-stu-id="27681-378">When the system sets the replenishment work availability, it considers any inventory that is already in the location before any work is completed</span></span>
- <span data-ttu-id="27681-379">各販売注文作業は、特定の補充作業にリンクされています。</span><span class="sxs-lookup"><span data-stu-id="27681-379">Each piece of sales order work is linked to a specific replenishment work.</span></span> <span data-ttu-id="27681-380">対応する販売作業の利用可能性機能はありません。</span><span class="sxs-lookup"><span data-stu-id="27681-380">There is no corresponding sales work availability functionality.</span></span>
