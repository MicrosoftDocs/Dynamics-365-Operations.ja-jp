---
title: 壁にプット - 店舗にプット
description: このトピックでは、壁にプット - 店舗にプット機能について説明します。 この機能を使用すると、コンフィギュレーション可能な基準に基づいて、製品をパッケージ品目のステージング エリアに統合する必要があるシナリオを処理できます。 これにより、単一のターゲット ライセンス プレートへのピッキングが可能となり、クラスター ピッキングよりも多くのプット位置を使用できるようになるので、ピッキング時間を減らすことができます。
author: Mirzaab
manager: tfehr
ms.date: 07/16/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: WHSLocationType, WHSLocationProfile, WHSLocation, WHSPackProfile, WHSWaveStepCode, WHSOutboundSortTemplate, WHSPostMethod, WHSWaveTemplateTable, WHSLocDirTable, WHSWorkClass, WHSWorkTemplateTable
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: mirzaab
ms.search.validFrom: 2020-07-16
ms.dyn365.ops.version: Release 10.0.9
ms.openlocfilehash: 12501b90e4b31ec11e3c59784ace9fd9a8b7d934
ms.sourcegitcommit: a36a4f9915ae3eb36bf8220111cf1486387713d9
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 10/16/2020
ms.locfileid: "4017831"
---
# <a name="put-to-wall---put-to-store"></a><span data-ttu-id="57413-105">壁にプット - 店舗にプット</span><span class="sxs-lookup"><span data-stu-id="57413-105">Put to wall - put to store</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="57413-106">*壁にプット - 店舗にプット* 機能を使用すると、コンフィギュレーション可能な基準に基づいて、製品をパッケージ品目のステージング エリアに統合する必要があるシナリオを処理できます。</span><span class="sxs-lookup"><span data-stu-id="57413-106">The *Put to wall - put to store* functionality lets you handle scenarios where you must consolidate a product to a prepack staging area, based on configurable criteria.</span></span> <span data-ttu-id="57413-107">この機能を使用すると、単一のターゲット ライセンス プレートへのピッキングが可能になり、クラスター ピッキングよりも多くのプット位置を使用できるようになるので、店舗へ出荷または小型品目を取り扱う企業はピッキング時間を減らすというメリットを得ることができます。</span><span class="sxs-lookup"><span data-stu-id="57413-107">Because this functionality allows for picking to a single target license plate and can use more put positions than cluster picking, companies that ship to stores or handle small items will benefit from decreased picking time.</span></span>

<span data-ttu-id="57413-108">この機能のワークフローは、さまざまな種類のコンテナーに配布するために、ピックされた製品をソーティング場所に送ります。</span><span class="sxs-lookup"><span data-stu-id="57413-108">The workflow for this functionality directs picked product to a sorting location for distribution into various types of containers.</span></span> <span data-ttu-id="57413-109">一般に、ソーティング場所には、複数のソート位置があります。</span><span class="sxs-lookup"><span data-stu-id="57413-109">Generally, each sorting location includes multiple sort positions.</span></span> <span data-ttu-id="57413-110">各ソート位置は、業務プロセスによって設定された基準に従って割り当てられます。</span><span class="sxs-lookup"><span data-stu-id="57413-110">Each sort position is assigned according to the criteria that are set by the business process.</span></span> <span data-ttu-id="57413-111">一般的な基準としては、最終出荷先、出荷、積荷があります。</span><span class="sxs-lookup"><span data-stu-id="57413-111">Typical criteria are the final destination, shipment, or load.</span></span> <span data-ttu-id="57413-112">商品が到着した後、注文、出荷先、出荷、または積荷に関連付けられている数量に基づいて、各ソート位置に配送されます。</span><span class="sxs-lookup"><span data-stu-id="57413-112">After a product arrives, it's distributed to each sort position, based on the quantity that is associated with the order, destination, shipment, or load.</span></span> <span data-ttu-id="57413-113">コンテナーが一杯であったり完全した場合は、業務プロセスに応じて、ステージング場所や出荷場所に移動され、さらなる処理が行なわれます。</span><span class="sxs-lookup"><span data-stu-id="57413-113">When a container is full or complete, it's moved to a staging location or a shipping location for further handling, depending on the business process.</span></span>

<span data-ttu-id="57413-114">この倉庫管理機能は、Put-to-light や Break Open などのその他の名前でも呼ばれています。</span><span class="sxs-lookup"><span data-stu-id="57413-114">This warehousing functionality is also referred to by other names, such as put-to-light and break opens.</span></span>

## <a name="turn-on-the-outbound-sorting-feature"></a><span data-ttu-id="57413-115">アウトバウンド ソーティング機能を有効にする</span><span class="sxs-lookup"><span data-stu-id="57413-115">Turn on the Outbound sorting feature</span></span>

<span data-ttu-id="57413-116">*壁にプット - 店舗にプット* 機能を使用する前に、 *オンボーディング ソーティング* 機能は自分のシステムでオンにしておく必要があります。</span><span class="sxs-lookup"><span data-stu-id="57413-116">Before you can use the *Put to wall - put to store* functionality, the *Outbound sorting* feature must be turned on in your system.</span></span> <span data-ttu-id="57413-117">管理者は、[機能の管理](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) ワークスペースを使用して、機能の状態を確認し、必要に応じて有効にすることができます。</span><span class="sxs-lookup"><span data-stu-id="57413-117">Admins can use the [Feature management](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) workspace to check the status of the feature and turn it on if it's required.</span></span> <span data-ttu-id="57413-118">この機能は、次のようにして表示されます。</span><span class="sxs-lookup"><span data-stu-id="57413-118">There, the feature is listed in the following way:</span></span>

- <span data-ttu-id="57413-119">**モジュール:** *倉庫管理*</span><span class="sxs-lookup"><span data-stu-id="57413-119">**Module:** *Warehouse management*</span></span>
- <span data-ttu-id="57413-120">**機能名:** *アウトバウンド ソーティング*</span><span class="sxs-lookup"><span data-stu-id="57413-120">**Feature name:** *Outbound sorting*</span></span>

<span data-ttu-id="57413-121">この機能が有効になっている場合は、 *アウトバウンド ソーティング* 機能を *組織全体のウェーブ ステップ コード* 機能と組み合わせて使用することができます。</span><span class="sxs-lookup"><span data-stu-id="57413-121">The *Outbound sorting* feature can be used in conjunction with the *Organization wide wave step code* feature if it's turned on.</span></span> <span data-ttu-id="57413-122">また、ウェーブ ステップ コードで設定された事前定義済のコードを使用する場合は、この機能もオンにする必要もあります。</span><span class="sxs-lookup"><span data-stu-id="57413-122">You must also turn on this feature if you will use predefined codes that are set up in wave step codes.</span></span> <span data-ttu-id="57413-123">**機能管理** ワークスペースで、この機能は次のようにリストされています:</span><span class="sxs-lookup"><span data-stu-id="57413-123">In the **Feature management** workspace, this feature is listed in the following way:</span></span>

- <span data-ttu-id="57413-124">**モジュール:** *倉庫管理*</span><span class="sxs-lookup"><span data-stu-id="57413-124">**Module:** *Warehouse management*</span></span>
- <span data-ttu-id="57413-125">**機能名:** *機能全体のウェーブ ステップ コード*</span><span class="sxs-lookup"><span data-stu-id="57413-125">**Feature name:** *Organization wide wave step code*</span></span>

## <a name="setup"></a><span data-ttu-id="57413-126">セットアップ</span><span class="sxs-lookup"><span data-stu-id="57413-126">Setup</span></span>

<span data-ttu-id="57413-127">このデモでは、標準の Contoso データと倉庫 *62* が使用されます。</span><span class="sxs-lookup"><span data-stu-id="57413-127">For this demo, standard Contoso data and warehouse *62* are used.</span></span> <span data-ttu-id="57413-128">また、後で説明する追加機能も使用されます。</span><span class="sxs-lookup"><span data-stu-id="57413-128">Some additions that are noted later are also used.</span></span>

### <a name="location-type"></a><span data-ttu-id="57413-129">場所のタイプ</span><span class="sxs-lookup"><span data-stu-id="57413-129">Location type</span></span>

1. <span data-ttu-id="57413-130">**倉庫管理 \> 設定 \> 倉庫 \> 場所タイプ** の順に移動します。</span><span class="sxs-lookup"><span data-stu-id="57413-130">Go to **Warehouse management \> Setup \> Warehouse \> Location types**.</span></span>
1. <span data-ttu-id="57413-131">アクション ウィンドウで、 **新規** を選択して、ソーティング用の場所タイプを作成します。</span><span class="sxs-lookup"><span data-stu-id="57413-131">On the Action Pane, select **New** to create a location type for sorting.</span></span>
1. <span data-ttu-id="57413-132">次の値を設定します。</span><span class="sxs-lookup"><span data-stu-id="57413-132">Set the following values:</span></span>

    - <span data-ttu-id="57413-133">**場所タイプ:** *SORT*</span><span class="sxs-lookup"><span data-stu-id="57413-133">**Location type:** *SORT*</span></span>
    - <span data-ttu-id="57413-134">**説明:** *ソート*</span><span class="sxs-lookup"><span data-stu-id="57413-134">**Description:** *Sort*</span></span>

1. <span data-ttu-id="57413-135">**保存** を選択します。</span><span class="sxs-lookup"><span data-stu-id="57413-135">Select **Save**.</span></span>

### <a name="warehouse-management-parameters"></a><span data-ttu-id="57413-136">倉庫管理パラメーター</span><span class="sxs-lookup"><span data-stu-id="57413-136">Warehouse management parameters</span></span>

1. <span data-ttu-id="57413-137">**倉庫管理 \> 設定 \> 倉庫管理パラメーター** の順に移動します。</span><span class="sxs-lookup"><span data-stu-id="57413-137">Go to **Warehouse management \> Setup \> Warehouse management parameters**.</span></span>
1. <span data-ttu-id="57413-138">**全般** タブの **場所タイプ** クイック タブ、 **ソーティング場所のタイプ** フィールドで、 *SORT* と入力します。</span><span class="sxs-lookup"><span data-stu-id="57413-138">On the **General** tab, on the **Location types** FastTab, in the **Sorting location type** field, enter *SORT*.</span></span>
1. <span data-ttu-id="57413-139">**保存** を選択します。</span><span class="sxs-lookup"><span data-stu-id="57413-139">Select **Save**.</span></span>

### <a name="location-profile"></a><span data-ttu-id="57413-140">場所プロファイル</span><span class="sxs-lookup"><span data-stu-id="57413-140">Location profile</span></span>

1. <span data-ttu-id="57413-141">**倉庫管理 \> 設定 \> 倉庫 \> 場所プロファイル** に移動します。</span><span class="sxs-lookup"><span data-stu-id="57413-141">Go to **Warehouse management \> Setup \> Warehouse \> Location profiles**.</span></span>
1. <span data-ttu-id="57413-142">アクション ウィンドウで、 **新規** を選択して、ソーティング場所の場所プロファイルを作成します。</span><span class="sxs-lookup"><span data-stu-id="57413-142">On the Action Pane, select **New** to create a location profile for the sorting location.</span></span>
1. <span data-ttu-id="57413-143">ヘッダーで、次の値を設定します。</span><span class="sxs-lookup"><span data-stu-id="57413-143">In the header, set the following values:</span></span>

    - <span data-ttu-id="57413-144">**場所プロファイル ID:** *ソート*</span><span class="sxs-lookup"><span data-stu-id="57413-144">**Location profile ID:** *Sort*</span></span>
    - <span data-ttu-id="57413-145">**名前:** *ソート*</span><span class="sxs-lookup"><span data-stu-id="57413-145">**Name:** *Sort*</span></span>

1. <span data-ttu-id="57413-146">**一般** クイック タブで、次の値を設定します。</span><span class="sxs-lookup"><span data-stu-id="57413-146">On the **General** FastTab, set the following values:</span></span>

    - <span data-ttu-id="57413-147">**場所フォーマット:** *PACK*</span><span class="sxs-lookup"><span data-stu-id="57413-147">**Location format:** *PACK*</span></span>
    - <span data-ttu-id="57413-148">**場所タイプ:** *SORT*</span><span class="sxs-lookup"><span data-stu-id="57413-148">**Location type:** *SORT*</span></span>
    - <span data-ttu-id="57413-149">**ライセンス プレート追跡を使用:** *はい*</span><span class="sxs-lookup"><span data-stu-id="57413-149">**Use license plate tracking:** *Yes*</span></span>
    - <span data-ttu-id="57413-150">**混合品目を許可:** *はい*</span><span class="sxs-lookup"><span data-stu-id="57413-150">**Allow mixed items:** *Yes*</span></span>
    - <span data-ttu-id="57413-151">**混合在庫ステータスを許可:** *はい*</span><span class="sxs-lookup"><span data-stu-id="57413-151">**Allow mixed inventory statuses:** *Yes*</span></span>

1. <span data-ttu-id="57413-152">**保存** を選択します。</span><span class="sxs-lookup"><span data-stu-id="57413-152">Select **Save**.</span></span>

### <a name="locations"></a><span data-ttu-id="57413-153">場所</span><span class="sxs-lookup"><span data-stu-id="57413-153">Locations</span></span>

1. <span data-ttu-id="57413-154">**倉庫管理 \> 設定 \> 倉庫 \> 場所** に移動します。</span><span class="sxs-lookup"><span data-stu-id="57413-154">Go to **Warehouse management \> Setup \> Warehouse \> Locations**.</span></span>
1. <span data-ttu-id="57413-155">**場所のチェック ディジットを生成する** チェック ボックスをクリアします。</span><span class="sxs-lookup"><span data-stu-id="57413-155">Clear the **Generate check digits for location** check box.</span></span>
1. <span data-ttu-id="57413-156">アクション ウィンドウで、 **新規** を選択し、次の値を設定します。</span><span class="sxs-lookup"><span data-stu-id="57413-156">On the Action Pane, select **New** , and then set the following values:</span></span>

    - <span data-ttu-id="57413-157">**倉庫:** *62*</span><span class="sxs-lookup"><span data-stu-id="57413-157">**Warehouse:** *62*</span></span>
    - <span data-ttu-id="57413-158">**場所:** *ソート*</span><span class="sxs-lookup"><span data-stu-id="57413-158">**Location:** *Sort*</span></span>
    - <span data-ttu-id="57413-159">**場所プロファイル ID:** *ソート*</span><span class="sxs-lookup"><span data-stu-id="57413-159">**Location profile ID:** *Sort*</span></span>

1. <span data-ttu-id="57413-160">**保存** を選択します。</span><span class="sxs-lookup"><span data-stu-id="57413-160">Select **Save**.</span></span>

### <a name="packing-profiles"></a><span data-ttu-id="57413-161">梱包プロファイル</span><span class="sxs-lookup"><span data-stu-id="57413-161">Packing profiles</span></span>

1. <span data-ttu-id="57413-162">**倉庫管理 \> 設定 \> 梱包 \> 梱包プロファイル** の順に移動します。</span><span class="sxs-lookup"><span data-stu-id="57413-162">Go to **Warehouse management \> Setup \> Packing \> Packing profiles**.</span></span>
1. <span data-ttu-id="57413-163">アクション ウィンドウで、 **新規** を選択し、次の値を設定します。</span><span class="sxs-lookup"><span data-stu-id="57413-163">On the Action Pane, select **New** , and then set the following values:</span></span>

    - <span data-ttu-id="57413-164">**梱包プロファイル ID:** *ソート*</span><span class="sxs-lookup"><span data-stu-id="57413-164">**Packing profile ID:** *Sort*</span></span>
    - <span data-ttu-id="57413-165">**説明:** *ソート*</span><span class="sxs-lookup"><span data-stu-id="57413-165">**Description:** *Sort*</span></span>
    - <span data-ttu-id="57413-166">**コンテナー梱包ポリシー:** このフィールドは空白のままにします。</span><span class="sxs-lookup"><span data-stu-id="57413-166">**Container packing policy:** Leave this field blank.</span></span>
    - <span data-ttu-id="57413-167">**コンテナー ID モード:** *自動*</span><span class="sxs-lookup"><span data-stu-id="57413-167">**Container ID mode:** *Auto*</span></span>
    - <span data-ttu-id="57413-168">**コンテナー タイプ:** *パレット 48X48*</span><span class="sxs-lookup"><span data-stu-id="57413-168">**Container type:** *PALLET 48X48*</span></span>
    - <span data-ttu-id="57413-169">**コンテナーを閉じる際コンテナーを自動作成する:** このフィールドは空白のままにします。</span><span class="sxs-lookup"><span data-stu-id="57413-169">**Autocreate container at container close:** Leave this field blank.</span></span>

1. <span data-ttu-id="57413-170">**保存** を選択します。</span><span class="sxs-lookup"><span data-stu-id="57413-170">Select **Save**.</span></span>

### <a name="wave-step-codes"></a><span data-ttu-id="57413-171">ウェーブ ステップ コード</span><span class="sxs-lookup"><span data-stu-id="57413-171">Wave step codes</span></span>

<span data-ttu-id="57413-172">*組織全体のウェーブステップコード* 機能を有効にしている場合は、次のコードを設定します。</span><span class="sxs-lookup"><span data-stu-id="57413-172">If you turned on the *Organization wide wave step code* feature, set up the following code.</span></span>

1. <span data-ttu-id="57413-173">**倉庫管理 \> 設定 \> ウェーブ \> ウェーブ ステップ コード** の順に移動します。</span><span class="sxs-lookup"><span data-stu-id="57413-173">Go to **Warehouse management \> Setup \> Waves \> Wave step codes**.</span></span>
1. <span data-ttu-id="57413-174">アクション ウィンドウで、 **新規** を選択し、次の値を設定します。</span><span class="sxs-lookup"><span data-stu-id="57413-174">On the Action Pane, select **New** , and then set the following values:</span></span>

    - <span data-ttu-id="57413-175">**ウェーブ ステップ コード:** *ソート*</span><span class="sxs-lookup"><span data-stu-id="57413-175">**Wave step code:** *Sort*</span></span>
    - <span data-ttu-id="57413-176">**ウェーブ ステップ詳細:** *ソート*</span><span class="sxs-lookup"><span data-stu-id="57413-176">**Wave step description:** *Sort*</span></span>
    - <span data-ttu-id="57413-177">**ウェーブ ステップ タイプ:** *ソート テンプレート*</span><span class="sxs-lookup"><span data-stu-id="57413-177">**Wave step type:** *Sort template*</span></span>

1. <span data-ttu-id="57413-178">**保存** を選択します。</span><span class="sxs-lookup"><span data-stu-id="57413-178">Select **Save**.</span></span>

### <a name="outbound-sorting-template"></a><span data-ttu-id="57413-179">出庫並べ替えテンプレート</span><span class="sxs-lookup"><span data-stu-id="57413-179">Outbound sorting template</span></span>

<span data-ttu-id="57413-180">ソート テンプレートは、ソート位置を作成するかどうか、使用される基準、ソート プロセスのその他の属性をコントロールします。</span><span class="sxs-lookup"><span data-stu-id="57413-180">The sorting template controls whether sort positions are created, what criteria are used, and other attributes of the sorting process.</span></span>

1. <span data-ttu-id="57413-181">**倉庫管理 \> 設定 \> 梱包 \> アウトバウンド ソーティング テンプレート** の順に移動します。</span><span class="sxs-lookup"><span data-stu-id="57413-181">Go to **Warehouse management \> Setup \> Packing \> Outbound sorting template**.</span></span>
1. <span data-ttu-id="57413-182">アクション ウィンドウで、 **新規** を選択して、ソート テンプレートを作成します。</span><span class="sxs-lookup"><span data-stu-id="57413-182">On the Action Pane, select **New** to create a sorting template.</span></span>
1. <span data-ttu-id="57413-183">新規テンプレートのヘッダーで、次の値を設定します。</span><span class="sxs-lookup"><span data-stu-id="57413-183">In the header of the new template, set the following values:</span></span>

    - <span data-ttu-id="57413-184">**アウトバウンド ソーティング テンプレート ID:** *ウェーブ ソート*</span><span class="sxs-lookup"><span data-stu-id="57413-184">**Outbound sorting template ID:** *Wave Sort*</span></span>
    - <span data-ttu-id="57413-185">**説明:** *ウェーブ ソート*</span><span class="sxs-lookup"><span data-stu-id="57413-185">**Description:** *Wave sort*</span></span>
    - <span data-ttu-id="57413-186">**ソート テンプレート タイプ:** *ウェーブ需要*</span><span class="sxs-lookup"><span data-stu-id="57413-186">**Sort template type:** *Wave demand*</span></span>

        <span data-ttu-id="57413-187">このフィールドでは、ソーティング テンプレートが使用されるプロセスを定義します。</span><span class="sxs-lookup"><span data-stu-id="57413-187">This field defines the process that the sorting template is used for.</span></span> <span data-ttu-id="57413-188">使用可能な値は次のとおりです。</span><span class="sxs-lookup"><span data-stu-id="57413-188">The following values are available:</span></span>

        - <span data-ttu-id="57413-189">**ウェーブ 需要** - ソート テンプレートは、 *Put to wall* プロセスに使用されます。</span><span class="sxs-lookup"><span data-stu-id="57413-189">**Wave demand** – The sorting template is used for the *Put to wall* process.</span></span> <span data-ttu-id="57413-190">このテンプレート タイプは、パック ステーションをバイパスして、在庫をウェーブから直接処理するのに使用されます。</span><span class="sxs-lookup"><span data-stu-id="57413-190">This template type is used to bypass the pack station and process inventory directly out of the wave.</span></span> <span data-ttu-id="57413-191">このタイプを使用するのは、 **ソーティング** ウェーブ プロセス メソッドがウェーブ テンプレートに含まれている場合のみです。</span><span class="sxs-lookup"><span data-stu-id="57413-191">You can use this type only if the **sorting** wave process method is included in the wave template.</span></span>
        - <span data-ttu-id="57413-192">**コンテナー** - ソーティング テンプレートは、 *梱包後にパレットを構築* プロセスに使用されます。</span><span class="sxs-lookup"><span data-stu-id="57413-192">**Container** – The sorting template is used for the *Pallet building after packing* process.</span></span> <span data-ttu-id="57413-193">このテンプレート タイプは、そのパック ステーションが閉じられ、パレットでソートされる必要があるコンテナーの処理に使用されます。</span><span class="sxs-lookup"><span data-stu-id="57413-193">This template type is used to process containers that are closed at the pack station and must be sorted onto pallets.</span></span>

    - <span data-ttu-id="57413-194">**倉庫:** *62*</span><span class="sxs-lookup"><span data-stu-id="57413-194">**Warehouse:** *62*</span></span>
    - <span data-ttu-id="57413-195">**場所:** *ソート*</span><span class="sxs-lookup"><span data-stu-id="57413-195">**Location:** *Sort*</span></span>

1. <span data-ttu-id="57413-196">**一般** クイック タブで、次の値を設定します。</span><span class="sxs-lookup"><span data-stu-id="57413-196">On the **General** FastTab, set the following values:</span></span>

    - <span data-ttu-id="57413-197">**ソートの検証:** *位置スキャン*</span><span class="sxs-lookup"><span data-stu-id="57413-197">**Sort verification:** *Position scan*</span></span>

        <span data-ttu-id="57413-198">このフィールドは、ソーティング中に必要な検証を定義します。</span><span class="sxs-lookup"><span data-stu-id="57413-198">This field defines the verification that is required during sorting.</span></span> <span data-ttu-id="57413-199">使用可能な値は次のとおりです。</span><span class="sxs-lookup"><span data-stu-id="57413-199">The following values are available:</span></span>

        - <span data-ttu-id="57413-200">None</span><span class="sxs-lookup"><span data-stu-id="57413-200">None</span></span>
        - <span data-ttu-id="57413-201">ライセンス プレートのスキャン</span><span class="sxs-lookup"><span data-stu-id="57413-201">License plate scan</span></span>
        - <span data-ttu-id="57413-202">位置のスキャン</span><span class="sxs-lookup"><span data-stu-id="57413-202">Position scan</span></span>

    - <span data-ttu-id="57413-203">**位置がクローズしたら作業を作成する:** *はい*</span><span class="sxs-lookup"><span data-stu-id="57413-203">**Create work on position close:** *Yes*</span></span>

        <span data-ttu-id="57413-204">このオプションを *はい* に設定すると、その位置がクローズしたときに、最終出荷場所に在庫を移動する作業が作成されます。</span><span class="sxs-lookup"><span data-stu-id="57413-204">If this option is set to *Yes* , when the position is closed, work will be created to move inventory to the final shipping location.</span></span> <span data-ttu-id="57413-205">これを *いいえ* に設定すると、その位置がクローズすると、直ちに在庫が注文に対してピッキングされます。</span><span class="sxs-lookup"><span data-stu-id="57413-205">If it's set to *No* , inventory will immediately be picked to the order when the position is closed.</span></span>

    - <span data-ttu-id="57413-206">**位置の割り当て:** *手動*</span><span class="sxs-lookup"><span data-stu-id="57413-206">**Position assignment:** *Manual*</span></span>

        <span data-ttu-id="57413-207">このフィールドは、位置割り当てのタイプを定義します。</span><span class="sxs-lookup"><span data-stu-id="57413-207">This field defines the type of position assignment.</span></span> <span data-ttu-id="57413-208">使用可能な値は次のとおりです。</span><span class="sxs-lookup"><span data-stu-id="57413-208">The following values are available:</span></span>

        - <span data-ttu-id="57413-209">**手動** - ユーザーは常に、在庫がソートされるべき位置を指定する必要があります。</span><span class="sxs-lookup"><span data-stu-id="57413-209">**Manual** – The user must always indicate which position the inventory should be sorted to.</span></span>
        - <span data-ttu-id="57413-210">**自動** - システムは可能な場合はソート テンプレートの分割に基づいて自動的に在庫をある位置にガイドします。</span><span class="sxs-lookup"><span data-stu-id="57413-210">**Automatic** – The system will automatically guide the inventory to a position whenever it can, based on the sort template breaks.</span></span>

    - <span data-ttu-id="57413-211">**ソート位置の割り当て基準:** *空の位置のみ使用*</span><span class="sxs-lookup"><span data-stu-id="57413-211">**Assign sort position criteria:** *Only use empty position*</span></span>

        <span data-ttu-id="57413-212">このフィールドは、位置が需要に割り当てられる場合に、ソート位置に既に存在する在庫を考慮するかどうかを制御します。</span><span class="sxs-lookup"><span data-stu-id="57413-212">This field controls whether inventory that is already present on sort positions is taken into account when a position is assigned for the demand.</span></span> <span data-ttu-id="57413-213">使用可能な値は次のとおりです。</span><span class="sxs-lookup"><span data-stu-id="57413-213">The following values are available:</span></span>

        - <span data-ttu-id="57413-214">**空欄の位置のみを使用** - 既に在庫が関連付けられている位置が考慮されます。</span><span class="sxs-lookup"><span data-stu-id="57413-214">**Only use empty position** – Positions that already have inventory associated with them will be taken into account</span></span>
        - <span data-ttu-id="57413-215">**位置が空と仮定する** - 位置に既に存在する在庫は、割り当て中に無視されます。</span><span class="sxs-lookup"><span data-stu-id="57413-215">**Assume position empty** – Any inventory that is already on the position will be disregarded during assignment.</span></span> <span data-ttu-id="57413-216">使用可能なすべての位置が使用されます。</span><span class="sxs-lookup"><span data-stu-id="57413-216">All available positions will be used.</span></span>

    - <span data-ttu-id="57413-217">**ウェーブ ステップ コード:** *ソート*</span><span class="sxs-lookup"><span data-stu-id="57413-217">**Wave step code:** *Sort*</span></span>

        <span data-ttu-id="57413-218">*組織全体のウェーブ ステップ コード* 機能がオンになっている場合は、 *ソート* のウェーブ ステップ コードもウェーブ ステップ コードで設定する必要があります。</span><span class="sxs-lookup"><span data-stu-id="57413-218">If the *Organization wide wave step code* feature is turned on, the *Sort* wave step code must also be set up in wave step codes.</span></span>

    - <span data-ttu-id="57413-219">**ソート位置を自動的に閉じる:** *はい*</span><span class="sxs-lookup"><span data-stu-id="57413-219">**Auto close sort position:** *Yes*</span></span>

        <span data-ttu-id="57413-220">このオプションを *はい* に設定すると、その位置に来るすべての作業が完了したときに、ソート位置は自動的に閉じられます。</span><span class="sxs-lookup"><span data-stu-id="57413-220">If this option is set to *Yes* , the sort position will automatically be closed when all work that comes to the position has been completed.</span></span>

    - <span data-ttu-id="57413-221">**ソート位置の数:** *3*</span><span class="sxs-lookup"><span data-stu-id="57413-221">**Number of sort positions:** *3*</span></span>

        <span data-ttu-id="57413-222">このフィールドは、システムが作成しりソート位置の最大数を定義します。</span><span class="sxs-lookup"><span data-stu-id="57413-222">This field defines the maximum number of sort positions that the system will create.</span></span>

    - <span data-ttu-id="57413-223">**ソート位置のプレフィックス:** *SP-*</span><span class="sxs-lookup"><span data-stu-id="57413-223">**Sort position prefix:** *SP-*</span></span>

        <span data-ttu-id="57413-224">このフィールドでは、システムが位置番号の前に割り当てる接頭語を定義します。</span><span class="sxs-lookup"><span data-stu-id="57413-224">This field defines the prefix that the system assigns before the position number.</span></span>

    - <span data-ttu-id="57413-225">**ソート位置を自動的にパックする:** *はい*</span><span class="sxs-lookup"><span data-stu-id="57413-225">**Auto pack sort position:** *Yes*</span></span>

        <span data-ttu-id="57413-226">このオプションを *はい* も設定すると、ソート位置の在庫は位置がクローズされた時にコンテナーに梱包されます。</span><span class="sxs-lookup"><span data-stu-id="57413-226">If this option is set to *Yes* , the inventory on the sort position will be packed into a container when the position is closed.</span></span>

    - <span data-ttu-id="57413-227">**梱包プロファイル ID:** *ソート*</span><span class="sxs-lookup"><span data-stu-id="57413-227">**Packing profile ID:** *Sort*</span></span>

        <span data-ttu-id="57413-228">このフィールドはソート位置がコンテナーに格納されるときに使用される梱包プロファイルを定義します。</span><span class="sxs-lookup"><span data-stu-id="57413-228">This field defines the packing profile that will be used when the sort position is packed into a container.</span></span>

1. <span data-ttu-id="57413-229">アクション ウィンドウで、 **クエリの編集** を選択して、このソーティング テンプレートに使用する基準を指定します。</span><span class="sxs-lookup"><span data-stu-id="57413-229">On the Action Pane, select **Edit query** to specify the criteria that are used for this sorting template.</span></span>
1. <span data-ttu-id="57413-230">このクエリのダイアログ ボックスに、 **ソーティング** タブで、 **新規** を選択して、明細行を追加し、次の値を設定します:</span><span class="sxs-lookup"><span data-stu-id="57413-230">In the query dialog box, on the **Sorting** tab, select **New** to add a line, and then set the following values:</span></span>

    - <span data-ttu-id="57413-231">**テーブル:** *積荷の詳細*</span><span class="sxs-lookup"><span data-stu-id="57413-231">**Table:** *Load details*</span></span>
    - <span data-ttu-id="57413-232">**派生テーブル:** *積荷の詳細*</span><span class="sxs-lookup"><span data-stu-id="57413-232">**Derived table:** *Load details*</span></span>
    - <span data-ttu-id="57413-233">**フィールド:** *出荷 ID*</span><span class="sxs-lookup"><span data-stu-id="57413-233">**Field:** *Shipment ID*</span></span>
    - <span data-ttu-id="57413-234">**検索の方法:** *昇順*</span><span class="sxs-lookup"><span data-stu-id="57413-234">**Search direction:** *Ascending*</span></span>

1. <span data-ttu-id="57413-235">**OK** を選択します。</span><span class="sxs-lookup"><span data-stu-id="57413-235">Select **OK**.</span></span>
1. <span data-ttu-id="57413-236">次のメッセージが表示される場合があります: "グループはリセットされますが、続行しますか?"</span><span class="sxs-lookup"><span data-stu-id="57413-236">You might receive the following message: "Grouping will be reset, continue?"</span></span> <span data-ttu-id="57413-237">**はい** を選択します。</span><span class="sxs-lookup"><span data-stu-id="57413-237">Select **Yes**.</span></span>

    <span data-ttu-id="57413-238">アクション ウィンドウの **アウトバウンド ソーティング テンプレート分割** ボタンが使用可能になります。</span><span class="sxs-lookup"><span data-stu-id="57413-238">The **Outbound sorting template breaks** button on the Action Pane becomes available.</span></span>

1. <span data-ttu-id="57413-239">アクション ウィンドウで、 **アウトバウンド ソーティング テンプレート分割** を選択します。</span><span class="sxs-lookup"><span data-stu-id="57413-239">On the Action Pane, select **Outbound sorting template breaks**.</span></span>
1. <span data-ttu-id="57413-240">**フィールドでグループ化** チェック ボックスを選択して、出荷 ID 別にグループ化します。</span><span class="sxs-lookup"><span data-stu-id="57413-240">Select the **Group by field** check box to group by shipment ID.</span></span>

    <span data-ttu-id="57413-241">この設定により、ウェーブのコンテナーである出荷ごとにソート位置が 1 つ作成されます。</span><span class="sxs-lookup"><span data-stu-id="57413-241">This setting will create one sort position per shipment that is a container in the wave.</span></span>

1. <span data-ttu-id="57413-242">**OK** を選択します。</span><span class="sxs-lookup"><span data-stu-id="57413-242">Select **OK**.</span></span>

### <a name="wave-process-methods"></a><span data-ttu-id="57413-243">ウェーブのプロセス方法</span><span class="sxs-lookup"><span data-stu-id="57413-243">Wave process methods</span></span>

1. <span data-ttu-id="57413-244">**倉庫管理 \> 設定 \> ウェーブ \> ウェーブのプロセス メソッド** に移動します。</span><span class="sxs-lookup"><span data-stu-id="57413-244">Go to **Warehouse management \> Setup \> Waves \> Wave process methods**.</span></span>
1. <span data-ttu-id="57413-245">アクション ウィンドウで、 **方法の再生成** を選択します。</span><span class="sxs-lookup"><span data-stu-id="57413-245">On the Action Pane, select **Regenerate methods**.</span></span>

    <span data-ttu-id="57413-246">**ソーティング** メソッドは、利用可能なメソッドのリストに追加され、 *出荷* ウェーブ テンプレート タイプがそれに対して選択されます。</span><span class="sxs-lookup"><span data-stu-id="57413-246">The **sorting** method is added to the list of available methods, and the *Shipping* wave template type is selected for it.</span></span>

### <a name="wave-templates"></a><span data-ttu-id="57413-247">ウェーブ テンプレート</span><span class="sxs-lookup"><span data-stu-id="57413-247">Wave templates</span></span>

<span data-ttu-id="57413-248">ウェーブ需要のソーティングに使用されるウェーブ テンプレートを編集します。</span><span class="sxs-lookup"><span data-stu-id="57413-248">Edit the wave template that is used for wave demand sorting.</span></span>

1. <span data-ttu-id="57413-249">**倉庫管理 \> 設定 \> ウェーブ \> ウェーブ テンプレート** の順に移動します。</span><span class="sxs-lookup"><span data-stu-id="57413-249">Go to **Warehouse management \> Setup \> Waves \> Wave templates**.</span></span>
1. <span data-ttu-id="57413-250">**ウェーブ テンプレート タイプ** フィールドで、 *出荷* を選択します。</span><span class="sxs-lookup"><span data-stu-id="57413-250">In the **Wave template type** field, select *Shipping*.</span></span>
1. <span data-ttu-id="57413-251">既存の **62 出荷の規定** テンプレートを選択します。</span><span class="sxs-lookup"><span data-stu-id="57413-251">Select the existing **62 Shipping default** template.</span></span>
1. <span data-ttu-id="57413-252">アクション ウィンドウで、 **編集** を選択します。</span><span class="sxs-lookup"><span data-stu-id="57413-252">On the Action Pane, select **Edit**.</span></span>
1. <span data-ttu-id="57413-253">**一般** クイック タブで、次の変更を加えます。</span><span class="sxs-lookup"><span data-stu-id="57413-253">On the **General** FastTab, make the following changes:</span></span>

    - <span data-ttu-id="57413-254">**倉庫へのリリース時にウェーブを処理する** オプションを *いいえ* に設定します。</span><span class="sxs-lookup"><span data-stu-id="57413-254">Set the **Process wave at release to warehouse** option to *No*.</span></span>
    - <span data-ttu-id="57413-255">**ウェーブを開くように割り当てる** オプションを *はい* に設定します。</span><span class="sxs-lookup"><span data-stu-id="57413-255">Set the **Assign to open waves** option to *Yes*.</span></span>

1. <span data-ttu-id="57413-256">**メソッド** クイック タブで、 **ソーティング** メソッドを設定します。</span><span class="sxs-lookup"><span data-stu-id="57413-256">On the **Methods** FastTab, set up the **sorting** method:</span></span>

    1. <span data-ttu-id="57413-257">**残りのメソッド** で、 **ソーティング** を選択します。</span><span class="sxs-lookup"><span data-stu-id="57413-257">In the **Remaining Methods** grid, select **sorting**.</span></span>
    2. <span data-ttu-id="57413-258">右矢印ボタンを選択して、 **ソーティング** を **選択したメソッド** グリッドに移動します。</span><span class="sxs-lookup"><span data-stu-id="57413-258">Select the right arrow button to move **sorting** to the **Selected Methods** grid.</span></span>
    3. <span data-ttu-id="57413-259">**選択したメソッド** グリッドで、 **ソーティング** を選択します。</span><span class="sxs-lookup"><span data-stu-id="57413-259">In the **Selected Methods** grid, select **sorting**.</span></span>
    4. <span data-ttu-id="57413-260">**ウェーブ ステップ コード** フィールドを *ソート* に設定します。</span><span class="sxs-lookup"><span data-stu-id="57413-260">Set the **Wave step code** field to *Sort*.</span></span>

1. <span data-ttu-id="57413-261">**保存** を選択します。</span><span class="sxs-lookup"><span data-stu-id="57413-261">Select **Save**.</span></span>

### <a name="mobile-device-menu-items"></a><span data-ttu-id="57413-262">モバイル デバイスのメニュー品目</span><span class="sxs-lookup"><span data-stu-id="57413-262">Mobile device menu items</span></span>

1. <span data-ttu-id="57413-263">**倉庫管理 \> 設定 \> モバイル デバイス \> モバイル デバイスのメニュー品目** の順に移動します。</span><span class="sxs-lookup"><span data-stu-id="57413-263">Go to **Warehouse management \> Setup \> Mobile device \> Mobile device menu items**.</span></span>
1. <span data-ttu-id="57413-264">アクション ウィンドウで、 **新規** を選択します。</span><span class="sxs-lookup"><span data-stu-id="57413-264">On the Action Pane, select **New**.</span></span>
1. <span data-ttu-id="57413-265">ヘッダーで、次の値を設定します。</span><span class="sxs-lookup"><span data-stu-id="57413-265">In the header, set the following values:</span></span>

    - <span data-ttu-id="57413-266">**メニュー項目名:** *ソート*</span><span class="sxs-lookup"><span data-stu-id="57413-266">**Menu item name:** *Sort*</span></span>
    - <span data-ttu-id="57413-267">**タイトル:** *ソート*</span><span class="sxs-lookup"><span data-stu-id="57413-267">**Title:** *Sort*</span></span>
    - <span data-ttu-id="57413-268">**モード:** *間接*</span><span class="sxs-lookup"><span data-stu-id="57413-268">**Mode:** *Indirect*</span></span>
    - <span data-ttu-id="57413-269">**既存の作業を使用する :** *いいえ*</span><span class="sxs-lookup"><span data-stu-id="57413-269">**Use existing work:** *No*</span></span>

1. <span data-ttu-id="57413-270">**一般** クイック タブで、次の値を設定します。</span><span class="sxs-lookup"><span data-stu-id="57413-270">On the **General** FastTab, set the following values:</span></span>

    - <span data-ttu-id="57413-271">**アクティビティ コード:** *アウトバウンド ソーティング*</span><span class="sxs-lookup"><span data-stu-id="57413-271">**Activity code:** *Outbound sorting*</span></span>
    - <span data-ttu-id="57413-272">**プロセス ガイドの使用:** *はい* (既定値)</span><span class="sxs-lookup"><span data-stu-id="57413-272">**Use process guide:** *Yes* (default value)</span></span>
    - <span data-ttu-id="57413-273">**アウトバウンド ソーティング テンプレート ID:** *ウェーブ ソート*</span><span class="sxs-lookup"><span data-stu-id="57413-273">**Outbound sorting template ID:** *Wave Sort*</span></span>

1. <span data-ttu-id="57413-274">**保存** を選択します。</span><span class="sxs-lookup"><span data-stu-id="57413-274">Select **Save**.</span></span>

### <a name="mobile-device-menu"></a><span data-ttu-id="57413-275">モバイル デバイスのメニュー</span><span class="sxs-lookup"><span data-stu-id="57413-275">Mobile device menu</span></span>

1. <span data-ttu-id="57413-276">**倉庫管理 \> 設定 \> モバイル デバイス \> モバイル デバイス メニュー** の順に移動します。</span><span class="sxs-lookup"><span data-stu-id="57413-276">Go to **Warehouse management \> Setup \> Mobile device \> Mobile device menu**.</span></span>
1. <span data-ttu-id="57413-277">メニューの一覧で **アウトバウンド** を選択します。</span><span class="sxs-lookup"><span data-stu-id="57413-277">In the list of menus, select **Outbound**.</span></span>
1. <span data-ttu-id="57413-278">アクション ウィンドウで、 **編集** を選択します。</span><span class="sxs-lookup"><span data-stu-id="57413-278">On the Action Pane, select **Edit**.</span></span>
1. <span data-ttu-id="57413-279">**使用可能なメニューとメニュー項目** のグリッドで、作成した **ソート** メニュー項目を検索して選択します。</span><span class="sxs-lookup"><span data-stu-id="57413-279">In the **Available Menus And Menu Items** grid, find and select the **Sort** menu item that you just created.</span></span>
1. <span data-ttu-id="57413-280">右矢印ボタンを選択して、 **ソート** を **メニュー構造** グリッドに移動します。</span><span class="sxs-lookup"><span data-stu-id="57413-280">Select the right arrow button to move **Sort** to the **Menu Structure** grid.</span></span> <span data-ttu-id="57413-281">このようにして、メニュー項目に **アウトバウンド** メニューを追加します。</span><span class="sxs-lookup"><span data-stu-id="57413-281">In this way, you add the menu item to the **Outbound** menu.</span></span>
1. <span data-ttu-id="57413-282">**保存** を選択します。</span><span class="sxs-lookup"><span data-stu-id="57413-282">Select **Save**.</span></span>

### <a name="location-directives"></a><span data-ttu-id="57413-283">場所のディレクティブ</span><span class="sxs-lookup"><span data-stu-id="57413-283">Location directives</span></span>

<span data-ttu-id="57413-284">ソーティングが完了した後に作成された作業をガイドするための場所ディレクティブを作成する必要があります。</span><span class="sxs-lookup"><span data-stu-id="57413-284">You must create location directives to guide the work that is created after the sorting is completed.</span></span>

1. <span data-ttu-id="57413-285">**倉庫管理 \> 設定 \> 場所のディレクティブ** に移動します。</span><span class="sxs-lookup"><span data-stu-id="57413-285">Go to **Warehouse management \> Setup \> Location directives**.</span></span>
1. <span data-ttu-id="57413-286">**作業指示書タイプ** フィールドで *ソート済み在庫ピッキング* を選択します。</span><span class="sxs-lookup"><span data-stu-id="57413-286">In the **Work order type** field, select *Sorted inventory picking*.</span></span>
1. <span data-ttu-id="57413-287">アクション ウィンドウで、 **新規** を選択します。</span><span class="sxs-lookup"><span data-stu-id="57413-287">On the Action Pane, select **New**.</span></span>
1. <span data-ttu-id="57413-288">ヘッダーで、次の値を設定します。</span><span class="sxs-lookup"><span data-stu-id="57413-288">In the header, set the following values:</span></span>

    - <span data-ttu-id="57413-289">**シーケンス:** *1*</span><span class="sxs-lookup"><span data-stu-id="57413-289">**Sequence:** *1*</span></span>
    - <span data-ttu-id="57413-290">**名前:** *Baydoor にプット*</span><span class="sxs-lookup"><span data-stu-id="57413-290">**Name:** *Put to Baydoor*</span></span>

1. <span data-ttu-id="57413-291">**場所のディレクティブ** クイック タブで、次の値を設定します。</span><span class="sxs-lookup"><span data-stu-id="57413-291">On the **Location directives** FastTab, set the following values:</span></span>

    - <span data-ttu-id="57413-292">**作業タイプ:** *プット*</span><span class="sxs-lookup"><span data-stu-id="57413-292">**Work type:** *Put*</span></span>
    - <span data-ttu-id="57413-293">**サイト:** *6*</span><span class="sxs-lookup"><span data-stu-id="57413-293">**Site:** *6*</span></span>
    - <span data-ttu-id="57413-294">**倉庫:** *62*</span><span class="sxs-lookup"><span data-stu-id="57413-294">**Warehouse:** *62*</span></span>
    - <span data-ttu-id="57413-295">**ディレクティブ コード:** このフィールドは空白のままにします。</span><span class="sxs-lookup"><span data-stu-id="57413-295">**Directive code:** Leave this field blank.</span></span>
    - <span data-ttu-id="57413-296">**複数の SKU:** *いいえ*</span><span class="sxs-lookup"><span data-stu-id="57413-296">**Multiple SKU:** *No*</span></span>

1. <span data-ttu-id="57413-297">**保存** を選択して、 **明細行** クイック タブを使用できるようにします。</span><span class="sxs-lookup"><span data-stu-id="57413-297">Select **Save** to make the **Lines** FastTab available.</span></span>
1. <span data-ttu-id="57413-298">**明細行** クイック タブで、 **新規** を選択して、次の値を設定します。</span><span class="sxs-lookup"><span data-stu-id="57413-298">On the **Lines** FastTab, select **New** , and then set the following values.</span></span> <span data-ttu-id="57413-299">その他のすべてのフィールドの規定値を受け入れます。</span><span class="sxs-lookup"><span data-stu-id="57413-299">Accept the default values for all the other fields.</span></span>

    - <span data-ttu-id="57413-300">**シーケンス番号:** *1*</span><span class="sxs-lookup"><span data-stu-id="57413-300">**Sequence number:** *1*</span></span>
    - <span data-ttu-id="57413-301">**開始数量:** *0*</span><span class="sxs-lookup"><span data-stu-id="57413-301">**From quantity:** *0*</span></span>
    - <span data-ttu-id="57413-302">**上限数量:** *1000000*</span><span class="sxs-lookup"><span data-stu-id="57413-302">**To quantity:** *1000000*</span></span>

1. <span data-ttu-id="57413-303">**保存** を選択して、 **場所ディレクティブ アクション** クイック タブを使用できるようにします。</span><span class="sxs-lookup"><span data-stu-id="57413-303">Select **Save** to make the **Location Directive Actions** FastTab available.</span></span>
1. <span data-ttu-id="57413-304">**場所ディレクティブ アクション** クイック タブで、 **新規** を選択して、次の値を設定します。</span><span class="sxs-lookup"><span data-stu-id="57413-304">On the **Location Directive Actions** FastTab, select **New** , and then set the following values.</span></span> <span data-ttu-id="57413-305">その他のすべてのフィールドの規定値を受け入れます。</span><span class="sxs-lookup"><span data-stu-id="57413-305">Accept the default values for all the other fields.</span></span>

    - <span data-ttu-id="57413-306">**シーケンス番号:** *1*</span><span class="sxs-lookup"><span data-stu-id="57413-306">**Sequence number:** *1*</span></span>
    - <span data-ttu-id="57413-307">**名前 :** *ベイドア*</span><span class="sxs-lookup"><span data-stu-id="57413-307">**Name:** *Baydoor*</span></span>

1. <span data-ttu-id="57413-308">**保存** を選択すると、 **場所ディレクティブ アクション** のファスト タブにある **クエリの編集** ボタンが使用できるようになります。</span><span class="sxs-lookup"><span data-stu-id="57413-308">Select **Save** to make the **Edit query** button on the **Location Directive Actions** FastTab available.</span></span>
1. <span data-ttu-id="57413-309">**場所ディレクティブ アクション** クイック タブで、 **クエリの編集** を選択します。</span><span class="sxs-lookup"><span data-stu-id="57413-309">On the **Location Directive Actions** FastTab, select **Edit query**.</span></span>
1. <span data-ttu-id="57413-310">**範囲** タブのクエリ ダイアログ ボックスで、 **フィールド** フィールドが *場所* に設定されている行を検索します。</span><span class="sxs-lookup"><span data-stu-id="57413-310">In the query dialog box, on the **Range** tab, find the row where the **Field** field is set to *Location*.</span></span> <span data-ttu-id="57413-311">この行の **基準** フィールドを *Baydoor* に設定します。</span><span class="sxs-lookup"><span data-stu-id="57413-311">Set the **Criteria** field for this row to *Baydoor*.</span></span>
1. <span data-ttu-id="57413-312">**OK** を選択して編集を確定します。</span><span class="sxs-lookup"><span data-stu-id="57413-312">Select **OK** to confirm the edit.</span></span>

### <a name="work-classes"></a><span data-ttu-id="57413-313">作業クラス</span><span class="sxs-lookup"><span data-stu-id="57413-313">Work classes</span></span>

1. <span data-ttu-id="57413-314">**倉庫管理 \> 設定 \> 作業 \> 作業クラス** の順に移動します。</span><span class="sxs-lookup"><span data-stu-id="57413-314">Go to **Warehouse management \> Setup \> Work \> Work classes**.</span></span>
1. <span data-ttu-id="57413-315">アクション ウィンドウで、 **新規** を選択します。</span><span class="sxs-lookup"><span data-stu-id="57413-315">On the Action Pane, select **New**.</span></span>
1. <span data-ttu-id="57413-316">ヘッダーで、次の値を設定します。</span><span class="sxs-lookup"><span data-stu-id="57413-316">In the header, set the following values:</span></span>

    - <span data-ttu-id="57413-317">**作業クラス ID:** *ソーティング*</span><span class="sxs-lookup"><span data-stu-id="57413-317">**Work class ID:** *Sorting*</span></span>
    - <span data-ttu-id="57413-318">**説明:** *ソーティング*</span><span class="sxs-lookup"><span data-stu-id="57413-318">**Description:** *Sorting*</span></span>
    - <span data-ttu-id="57413-319">**作業指示のタイプ:** *ソート済み在庫のピッキング*</span><span class="sxs-lookup"><span data-stu-id="57413-319">**Work order type:** *Sorted inventory picking*</span></span>

1. <span data-ttu-id="57413-320">**保存** を選択します。</span><span class="sxs-lookup"><span data-stu-id="57413-320">Select **Save**.</span></span>

### <a name="work-templates"></a><span data-ttu-id="57413-321">作業テンプレート</span><span class="sxs-lookup"><span data-stu-id="57413-321">Work templates</span></span>

1. <span data-ttu-id="57413-322">**倉庫管理 \> 作業 \> 作業テンプレート** の順に移動します。</span><span class="sxs-lookup"><span data-stu-id="57413-322">Go to **Warehouse management \> Work \> Work templates**.</span></span>
1. <span data-ttu-id="57413-323">**ワーク オーダー タイプ** フィールドで、 *販売注文* を選択します。</span><span class="sxs-lookup"><span data-stu-id="57413-323">In the **Work order type** field, select *Sales orders*.</span></span>
1. <span data-ttu-id="57413-324">グリッドで、 **62 を梱包にピッキングする** 作業テンプレートを選択します。</span><span class="sxs-lookup"><span data-stu-id="57413-324">In the grid, select the **62 Pick to pack** work template.</span></span>
1. <span data-ttu-id="57413-325">アクション ウィンドウで、 **作業ヘッダーの分割** を選択します。</span><span class="sxs-lookup"><span data-stu-id="57413-325">On the Action Pane, select **Work header breaks**.</span></span>
1. <span data-ttu-id="57413-326">アクション ウィンドウで、 **編集** を選択します。</span><span class="sxs-lookup"><span data-stu-id="57413-326">On the Action Pane, select **Edit**.</span></span>
1. <span data-ttu-id="57413-327">**フィールド名** フィールドが *出荷ID* に設定されている行で、 **このフィールドでグループ化** チェック ボックスをオフにします。</span><span class="sxs-lookup"><span data-stu-id="57413-327">On the line where the **Field name** field is set to *Shipment ID* , clear the **Group by this field** check box.</span></span>
1. <span data-ttu-id="57413-328">**保存** をクリックし、 **ワーク ヘッダーの区切り** ダイアログ ボックスを閉じます。</span><span class="sxs-lookup"><span data-stu-id="57413-328">Select **Save** , and then close the **Work header breaks** dialog box.</span></span>
1. <span data-ttu-id="57413-329">**作業指示書タイプ** フィールドで *ソート済み在庫ピッキング* を選択します。</span><span class="sxs-lookup"><span data-stu-id="57413-329">In the **Work order type** field, select *Sorted inventory picking*.</span></span>
1. <span data-ttu-id="57413-330">**新規** を選択して、作業テンプレートを作成します。</span><span class="sxs-lookup"><span data-stu-id="57413-330">Select **New** to create a work template.</span></span>
1. <span data-ttu-id="57413-331">**概要** セクションで、次の値を設定します。</span><span class="sxs-lookup"><span data-stu-id="57413-331">In the **Overview** section, set the following values.</span></span> <span data-ttu-id="57413-332">その他のすべてのフィールドの規定値を受け入れます。</span><span class="sxs-lookup"><span data-stu-id="57413-332">Accept the default values for all the other fields.</span></span>

    - <span data-ttu-id="57413-333">**作業テンプレート:** *ソート済みピッキング*</span><span class="sxs-lookup"><span data-stu-id="57413-333">**Work template:** *Sorted picking*</span></span>
    - <span data-ttu-id="57413-334">**作業テンプレートの説明:** *ソート済みピッキング*</span><span class="sxs-lookup"><span data-stu-id="57413-334">**Work template description:** *Sorted picking*</span></span>

1. <span data-ttu-id="57413-335">**保存** を選択して、 **作業テンプレートの詳細** セクションを使用できるようにします。</span><span class="sxs-lookup"><span data-stu-id="57413-335">Select **Save** to make the **Work Template Details** section available.</span></span>
1. <span data-ttu-id="57413-336">**作業テンプレートの詳細** セクションでは、2 つの行を作成します。</span><span class="sxs-lookup"><span data-stu-id="57413-336">In the **Work Template Details** section, you will create two lines.</span></span> <span data-ttu-id="57413-337">**新規** を選択して、明細行 1 に次の値を設定します。</span><span class="sxs-lookup"><span data-stu-id="57413-337">Select **New** , and then set the following values for line 1:</span></span>

    - <span data-ttu-id="57413-338">**作業タイプ:** *ピッキング*</span><span class="sxs-lookup"><span data-stu-id="57413-338">**Work type:** *Pick*</span></span>
    - <span data-ttu-id="57413-339">**必須:** 選択済 (= *はい* )</span><span class="sxs-lookup"><span data-stu-id="57413-339">**Mandatory:** Selected (= *Yes* )</span></span>
    - <span data-ttu-id="57413-340">**作業クラス ID:** *ソーティング*</span><span class="sxs-lookup"><span data-stu-id="57413-340">**Work class ID:** *Sorting*</span></span>

1. <span data-ttu-id="57413-341">**新規** を再度選択して、明細行 2 に次の値を設定します。</span><span class="sxs-lookup"><span data-stu-id="57413-341">Select **New** again, and then set the following values for line 2:</span></span>

    - <span data-ttu-id="57413-342">**作業タイプ:** *プット*</span><span class="sxs-lookup"><span data-stu-id="57413-342">**Work type:** *Put*</span></span>
    - <span data-ttu-id="57413-343">**必須:** 選択済 (= *はい* )</span><span class="sxs-lookup"><span data-stu-id="57413-343">**Mandatory:** Selected (= *Yes* )</span></span>
    - <span data-ttu-id="57413-344">**作業クラス ID:** *ソーティング*</span><span class="sxs-lookup"><span data-stu-id="57413-344">**Work class ID:** *Sorting*</span></span>

1. <span data-ttu-id="57413-345">**保存** を選択します。</span><span class="sxs-lookup"><span data-stu-id="57413-345">Select **Save**.</span></span>

## <a name="example-scenario"></a><span data-ttu-id="57413-346">シナリオ例</span><span class="sxs-lookup"><span data-stu-id="57413-346">Example scenario</span></span>

<span data-ttu-id="57413-347">このシナリオでは、倉庫には小品目が複数場所に保管されていて出荷前に梱包する必要があり、梱包ステーション機能が実際は適していない場合に、シミュレーションを行います。</span><span class="sxs-lookup"><span data-stu-id="57413-347">This scenario simulates a situation where the warehouse stores small items in locations and must pack them into boxes before they are shipped, and where packing station functionality isn't really suitable.</span></span> <span data-ttu-id="57413-348">作業者は、ピッキング速度を高めるために、複数の顧客や異なる住所に対して同時に注文をピックします。</span><span class="sxs-lookup"><span data-stu-id="57413-348">Workers pick orders for multiple customers and different addresses at the same time to increase the picking speed.</span></span> <span data-ttu-id="57413-349">ピッキングが完了した後は、必要な基準に基づいて、ピッキングされた品目を適切なボックスにソートできるソーティング場所に作業者が到着します。</span><span class="sxs-lookup"><span data-stu-id="57413-349">After picking has been completed, the workers arrive at the sorting location, where the picked items can be sorted to the correct box, based on required criteria.</span></span> <span data-ttu-id="57413-350">この例では、各出荷ごとに異なる住所があるので、出荷 ID を使用して適切なボックスを決定します。</span><span class="sxs-lookup"><span data-stu-id="57413-350">In this example, the shipment ID will be used to determine the correct box, because each shipment has a different address.</span></span> <span data-ttu-id="57413-351">積荷からすべての品目を梱包して出荷別にソートした後、このボックスはステージング エリアに移動され、最終的にトラックに積み込まれます。</span><span class="sxs-lookup"><span data-stu-id="57413-351">After all items from the load are packed and sorted by shipment, the boxes will be moved to the staging area and eventually loaded onto a truck.</span></span>

<span data-ttu-id="57413-352">このシナリオを始める前に、すべての標準倉庫機能が自分の倉庫に対して正しく設定されていることを確認してください。</span><span class="sxs-lookup"><span data-stu-id="57413-352">Before you start the scenario, make sure that all standard warehouse functionality is set up correctly for your warehouse.</span></span> <span data-ttu-id="57413-353">標準 Contoso 倉庫 *62* はこの目的のために使用されます。</span><span class="sxs-lookup"><span data-stu-id="57413-353">Standard Contoso warehouse *62* is used for this purpose.</span></span> <span data-ttu-id="57413-354">標準コンフィギュレーションは変更されていないので、これ以外のこの設定について説明します。</span><span class="sxs-lookup"><span data-stu-id="57413-354">Standard configurations haven't been changed, besides what is described in the setup.</span></span>

### <a name="create-demand"></a><span data-ttu-id="57413-355">需要の作成</span><span class="sxs-lookup"><span data-stu-id="57413-355">Create demand</span></span>

<span data-ttu-id="57413-356">この機能を説明する前に、いくつかの要求を作成する必要があります。</span><span class="sxs-lookup"><span data-stu-id="57413-356">Before the functionality can be demonstrated, you must create some demand.</span></span> <span data-ttu-id="57413-357">このシナリオでは、3 つの異なる顧客に対して 3 つの販売注文を作成して、さまざまな配送先住所をシミュレーションします。</span><span class="sxs-lookup"><span data-stu-id="57413-357">For this scenario, you will create three sales orders for three different customers to simulate different delivery addresses.</span></span> <span data-ttu-id="57413-358">この方法では、3 つの個別の出荷を作成します。</span><span class="sxs-lookup"><span data-stu-id="57413-358">In this way, you will create three separate shipments.</span></span>

<span data-ttu-id="57413-359">販売注文と出荷を作成する前に、ピッキング場所に、注文のすべての品目に対して十分な在庫があることを確認する必要もあります。</span><span class="sxs-lookup"><span data-stu-id="57413-359">Before you create sales orders and shipments, make sure that the pick locations have enough inventory for all the items on the orders.</span></span> <span data-ttu-id="57413-360">場所ディレクティブの設定を確認して、販売注文のピッキングに使用されるピッキング場所を確認します。</span><span class="sxs-lookup"><span data-stu-id="57413-360">Review the location directive settings to confirm the picking locations that are used for sales order picking.</span></span> <span data-ttu-id="57413-361">在庫を調整する必要がある場合には、手動によって移動を作成したり、補充を使用したり、またはその他のフローを使用したりできます。</span><span class="sxs-lookup"><span data-stu-id="57413-361">If you must adjust the inventory, you can create manual movements, use replenishment, or use any other flow.</span></span> <span data-ttu-id="57413-362">その後在庫を予約します。</span><span class="sxs-lookup"><span data-stu-id="57413-362">Then reserve the inventory.</span></span>

1. <span data-ttu-id="57413-363">**販売とマーケティング \> 販売注文 \> すべての販売注文** の順に移動します。</span><span class="sxs-lookup"><span data-stu-id="57413-363">Go to **Sales and marketing \> Sales orders \> All sales orders**.</span></span>
1. <span data-ttu-id="57413-364">**新規** を選択して注文 1 の販売注文を作成します。</span><span class="sxs-lookup"><span data-stu-id="57413-364">Select **New** to create a sales order for order 1.</span></span>
1. <span data-ttu-id="57413-365">**販売注文の作成** ダイアログ ボックスでは、次の値を設定します。</span><span class="sxs-lookup"><span data-stu-id="57413-365">In the **Create sales order** dialog box, set the following values:</span></span>

    - <span data-ttu-id="57413-366">**顧客:** *US-001*</span><span class="sxs-lookup"><span data-stu-id="57413-366">**Customer:** *US-001*</span></span>
    - <span data-ttu-id="57413-367">**倉庫:** *62*</span><span class="sxs-lookup"><span data-stu-id="57413-367">**Warehouse:** *62*</span></span>

1. <span data-ttu-id="57413-368">**OK** を選択します。</span><span class="sxs-lookup"><span data-stu-id="57413-368">Select **OK**.</span></span>
1. <span data-ttu-id="57413-369">新しい明細行が、 **販売注文明細行** クイック タブに追加されます。</span><span class="sxs-lookup"><span data-stu-id="57413-369">A new line is added to the **Sales order lines** FastTab.</span></span> <span data-ttu-id="57413-370">次の値を設定します。</span><span class="sxs-lookup"><span data-stu-id="57413-370">Set the following values:</span></span>

    - <span data-ttu-id="57413-371">**品目番号:** *A0001*</span><span class="sxs-lookup"><span data-stu-id="57413-371">**Item number:** *A0001*</span></span>
    - <span data-ttu-id="57413-372">**数量:** *5*</span><span class="sxs-lookup"><span data-stu-id="57413-372">**Quantity:** *5*</span></span>

1. <span data-ttu-id="57413-373">**明細行の追加** を選択して、2 行目を追加し、次の値を設定します。</span><span class="sxs-lookup"><span data-stu-id="57413-373">Select **Add line** to add a second line, and set the following values:</span></span>

    - <span data-ttu-id="57413-374">**品目番号:** *A0002*</span><span class="sxs-lookup"><span data-stu-id="57413-374">**Item number:** *A0002*</span></span>
    - <span data-ttu-id="57413-375">**数量:** *10*</span><span class="sxs-lookup"><span data-stu-id="57413-375">**Quantity:** *10*</span></span>

1. <span data-ttu-id="57413-376">在庫引当のために、注文の各販売明細行について、次の手順を繰り返します。</span><span class="sxs-lookup"><span data-stu-id="57413-376">Repeat the following steps for each sales line on the order to reserve inventory for it:</span></span>

    1. <span data-ttu-id="57413-377">**販売注文行** クイック タブの **在庫** メニューで、 **予約** を選択します。</span><span class="sxs-lookup"><span data-stu-id="57413-377">On the **Sales order lines** FastTab, on the **Inventory** menu, select **Reservation**.</span></span>
    1. <span data-ttu-id="57413-378">**予約** ページの、 **ロットの予約** を選択して、ページを閉じます。</span><span class="sxs-lookup"><span data-stu-id="57413-378">On the **Reservation** page, select **Reserve lot** , and then close the page.</span></span>
    1. <span data-ttu-id="57413-379">**保存** を選択します。</span><span class="sxs-lookup"><span data-stu-id="57413-379">Select **Save**.</span></span>

1. <span data-ttu-id="57413-380">**新規** を選択して注文 2 の販売注文を作成します。</span><span class="sxs-lookup"><span data-stu-id="57413-380">Select **New** to create a sales order for order 2.</span></span>
1. <span data-ttu-id="57413-381">**販売注文の作成** ダイアログ ボックスでは、次の値を設定します。</span><span class="sxs-lookup"><span data-stu-id="57413-381">In the **Create sales order** dialog box, set the following values:</span></span>

    - <span data-ttu-id="57413-382">**顧客:** *US-004*</span><span class="sxs-lookup"><span data-stu-id="57413-382">**Customer:** *US-004*</span></span>
    - <span data-ttu-id="57413-383">**倉庫:** *62*</span><span class="sxs-lookup"><span data-stu-id="57413-383">**Warehouse:** *62*</span></span>

1. <span data-ttu-id="57413-384">**OK** を選択します。</span><span class="sxs-lookup"><span data-stu-id="57413-384">Select **OK**.</span></span>
1. <span data-ttu-id="57413-385">新しい明細行が、 **販売注文明細行** クイック タブに追加されます。</span><span class="sxs-lookup"><span data-stu-id="57413-385">A new line is added to the **Sales order lines** FastTab.</span></span> <span data-ttu-id="57413-386">次の値を設定します。</span><span class="sxs-lookup"><span data-stu-id="57413-386">Set the following values:</span></span>

    - <span data-ttu-id="57413-387">**品目番号:** *A0001*</span><span class="sxs-lookup"><span data-stu-id="57413-387">**Item number:** *A0001*</span></span>
    - <span data-ttu-id="57413-388">**数量:** *7*</span><span class="sxs-lookup"><span data-stu-id="57413-388">**Quantity:** *7*</span></span>

1. <span data-ttu-id="57413-389">**明細行の追加** を選択して、2 行目を追加し、次の値を設定します。</span><span class="sxs-lookup"><span data-stu-id="57413-389">Select **Add line** to add a second line, and set the following values:</span></span>

    - <span data-ttu-id="57413-390">**品目番号:** *A0002*</span><span class="sxs-lookup"><span data-stu-id="57413-390">**Item number:** *A0002*</span></span>
    - <span data-ttu-id="57413-391">**数量:** *3*</span><span class="sxs-lookup"><span data-stu-id="57413-391">**Quantity:** *3*</span></span>

1. <span data-ttu-id="57413-392">在庫引当のために、注文の各販売明細行について、次の手順を繰り返します。</span><span class="sxs-lookup"><span data-stu-id="57413-392">Repeat the following steps for each sales line on the order to reserve inventory for it:</span></span>

    1. <span data-ttu-id="57413-393">**販売注文行** クイック タブの **在庫** メニューで、 **予約** を選択します。</span><span class="sxs-lookup"><span data-stu-id="57413-393">On the **Sales order lines** FastTab, on the **Inventory** menu, select **Reservation**.</span></span>
    1. <span data-ttu-id="57413-394">**予約** ページの、 **ロットの予約** を選択して、ページを閉じます。</span><span class="sxs-lookup"><span data-stu-id="57413-394">On the **Reservation** page, select **Reserve lot** , and then close the page.</span></span>
    1. <span data-ttu-id="57413-395">**保存** を選択します。</span><span class="sxs-lookup"><span data-stu-id="57413-395">Select **Save**.</span></span>

1. <span data-ttu-id="57413-396">**新規** を選択して注文 3 の販売注文を作成します。</span><span class="sxs-lookup"><span data-stu-id="57413-396">Select **New** to create a sales order for order 3.</span></span>
1. <span data-ttu-id="57413-397">**販売注文の作成** ダイアログ ボックスでは、次の値を設定します。</span><span class="sxs-lookup"><span data-stu-id="57413-397">In the **Create sales order** dialog box, set the following values:</span></span>

    - <span data-ttu-id="57413-398">**顧客:** *US-007*</span><span class="sxs-lookup"><span data-stu-id="57413-398">**Customer:** *US-007*</span></span>
    - <span data-ttu-id="57413-399">**倉庫:** *62*</span><span class="sxs-lookup"><span data-stu-id="57413-399">**Warehouse:** *62*</span></span>

1. <span data-ttu-id="57413-400">**OK** を選択します。</span><span class="sxs-lookup"><span data-stu-id="57413-400">Select **OK**.</span></span>
1. <span data-ttu-id="57413-401">新しい明細行が、 **販売注文明細行** クイック タブに追加されます。</span><span class="sxs-lookup"><span data-stu-id="57413-401">A new line is added to the **Sales order lines** FastTab.</span></span> <span data-ttu-id="57413-402">次の値を設定します。</span><span class="sxs-lookup"><span data-stu-id="57413-402">Set the following values:</span></span>

    - <span data-ttu-id="57413-403">**品目番号:** *A0001*</span><span class="sxs-lookup"><span data-stu-id="57413-403">**Item number:** *A0001*</span></span>
    - <span data-ttu-id="57413-404">**数量:** *8*</span><span class="sxs-lookup"><span data-stu-id="57413-404">**Quantity:** *8*</span></span>

1. <span data-ttu-id="57413-405">販売明細行のために在庫を予約するには、次の手順に従います。</span><span class="sxs-lookup"><span data-stu-id="57413-405">Follow these steps to reserve inventory for the sales line:</span></span>

    1. <span data-ttu-id="57413-406">**販売注文行** クイック タブの **在庫** メニューで、 **予約** を選択します。</span><span class="sxs-lookup"><span data-stu-id="57413-406">On the **Sales order lines** FastTab, on the **Inventory** menu, select **Reservation**.</span></span>
    1. <span data-ttu-id="57413-407">**予約** ページの、 **ロットの予約** を選択して、ページを閉じます。</span><span class="sxs-lookup"><span data-stu-id="57413-407">On the **Reservation** page, select **Reserve lot** , and then close the page.</span></span>
    1. <span data-ttu-id="57413-408">**保存** を選択します。</span><span class="sxs-lookup"><span data-stu-id="57413-408">Select **Save**.</span></span>

<span data-ttu-id="57413-409">各販売注文ごとに倉庫にリリースするには、次の手順を実行します。</span><span class="sxs-lookup"><span data-stu-id="57413-409">Complete the following procedure to release each sales order to the warehouse.</span></span> <span data-ttu-id="57413-410">3 つの異なる出荷が作成されます。</span><span class="sxs-lookup"><span data-stu-id="57413-410">Three different shipments will be created.</span></span> <span data-ttu-id="57413-411">その後、この 3 つの出荷をすべて 1 つの新規ウェーブに追加します。</span><span class="sxs-lookup"><span data-stu-id="57413-411">You will then add all three shipments to one new wave.</span></span>

1. <span data-ttu-id="57413-412">**販売とマーケティング \> 販売注文 \> すべての販売注文** の順に移動します。</span><span class="sxs-lookup"><span data-stu-id="57413-412">Go to **Sales and marketing \> Sales orders \> All sales orders**.</span></span>
1. <span data-ttu-id="57413-413">グリッドで、作成した最初の販売注文を選択します。</span><span class="sxs-lookup"><span data-stu-id="57413-413">In the grid, select the first sales order that you created.</span></span>
1. <span data-ttu-id="57413-414">アクション ウィンドウの **倉庫** タブで、 **倉庫へのリリース** を選択します。</span><span class="sxs-lookup"><span data-stu-id="57413-414">On the Action Pane, on the **Warehouse** tab, select **Release to warehouse**.</span></span>

    <span data-ttu-id="57413-415">作成したウェーブ ID と出荷 ID を示す情報メッセージを受信します。</span><span class="sxs-lookup"><span data-stu-id="57413-415">You receive an informational message that shows the wave ID and shipment ID that were created.</span></span>

1. <span data-ttu-id="57413-416">前の手順を繰り返して、販売注文 2 と 3 を倉庫にリリースします。</span><span class="sxs-lookup"><span data-stu-id="57413-416">Repeat the previous steps to release sales orders 2 and 3 to the warehouse.</span></span> <span data-ttu-id="57413-417">表示される情報メッセージは、販売注文 1 をリリースしたときに作成されたウェーブに出荷が追加されたことを示しています。</span><span class="sxs-lookup"><span data-stu-id="57413-417">Notice that the informational message that you receive indicates that a shipment has been added to the wave that was created when you released sales order 1.</span></span>
1. <span data-ttu-id="57413-418">**倉庫管理 \> 出庫ウェーブ \> 出荷ウェーブ \> すべてのウェーブ** の順に移動します。</span><span class="sxs-lookup"><span data-stu-id="57413-418">Go to **Warehouse management \> Outbound waves \> Shipment waves \> All waves**.</span></span>
1. <span data-ttu-id="57413-419">販売注文のリリースから作成されたウェーブ ID を選択して、 **ウェーブ** ページを開きます。</span><span class="sxs-lookup"><span data-stu-id="57413-419">Select the wave ID that was created from the release of the sales orders to open the **Waves** page.</span></span> <span data-ttu-id="57413-420">このページには、ウェーブの詳細が表示されます。</span><span class="sxs-lookup"><span data-stu-id="57413-420">This page shows the wave details.</span></span> <span data-ttu-id="57413-421">**ウェーブ 明細行** クイック タブには、作成された出荷が表示されます。</span><span class="sxs-lookup"><span data-stu-id="57413-421">The **Wave lines** FastTab shows the shipments that were created.</span></span>

    <span data-ttu-id="57413-422">ここで、ピッキング場所からソート場所に品目を取り込むための作業を作成する必要があります。</span><span class="sxs-lookup"><span data-stu-id="57413-422">You must now create work to bring items from the picking locations to the sorting location.</span></span>

1. <span data-ttu-id="57413-423">アクション ウィンドウで、 **プロセス** を選択します。</span><span class="sxs-lookup"><span data-stu-id="57413-423">On the Action Pane, select **Process**.</span></span>

    <span data-ttu-id="57413-424">ソート方法では、ウェーブ処理中に、ソーティング テンプレートを使用して、ソート位置に在庫を割り当てます。</span><span class="sxs-lookup"><span data-stu-id="57413-424">During wave processing, the sorting method will use the sorting template to assign the inventory to sort positions.</span></span> <span data-ttu-id="57413-425">ウェーブが完了したときに、作業が作成され、ウェーブが転記されたことを示す情報メッセージを受信します。</span><span class="sxs-lookup"><span data-stu-id="57413-425">When wave processing is completed, you receive an informational message that states that the wave has been posted and work has been created.</span></span>

1. <span data-ttu-id="57413-426">アクション ウィンドウの、 **ウェーブ** タブの **関連情報** グループで、 **作業** を選択して作成された作業を表示します。</span><span class="sxs-lookup"><span data-stu-id="57413-426">On the Action Pane, on the **Wave** tab, in the **Related information** group, select **Work** to view the work that was created.</span></span> <span data-ttu-id="57413-427">作業 ID をメモします。</span><span class="sxs-lookup"><span data-stu-id="57413-427">Make a note of the work ID.</span></span>
1. <span data-ttu-id="57413-428">**倉庫管理 \> 梱包とコンテナー詰め \> アウトバウンド ソーティング位置割り当て** の順に移動します。</span><span class="sxs-lookup"><span data-stu-id="57413-428">Go to **Warehouse management \> Packing and containerization \> Outbound sorting position assignments**.</span></span>
1. <span data-ttu-id="57413-429">左の列では、出荷ごとに作成されたアウトバウンド ソーティング位置を表示できます。</span><span class="sxs-lookup"><span data-stu-id="57413-429">In the left column, you can view the outbound sorting position that was created for each shipment.</span></span>
1. <span data-ttu-id="57413-430">**ソート位置の基準** クイック タブには、その位置の出荷 ID が表示されます。</span><span class="sxs-lookup"><span data-stu-id="57413-430">On the **Sort position criteria** FastTab, you can view the shipment ID for that position.</span></span>

<span data-ttu-id="57413-431">作業 ID が 1 つ作成され、ピッキング場所からソート場所に在庫を運びます。</span><span class="sxs-lookup"><span data-stu-id="57413-431">One work ID has been created to bring inventory from the picking locations to the sorting location.</span></span> <span data-ttu-id="57413-432">この作業を完了するには、ウェーブ処理中に作成された作業 ID が必要になります。</span><span class="sxs-lookup"><span data-stu-id="57413-432">To complete the work, you will need the work ID that was created during wave processing.</span></span>

### <a name="sales-order-picking-to-the-sorting-location"></a><span data-ttu-id="57413-433">ソーティング場所に対する販売注文のピッキング</span><span class="sxs-lookup"><span data-stu-id="57413-433">Sales order picking to the sorting location</span></span>

1. <span data-ttu-id="57413-434">倉庫 *62* の作業者としてモバイル アプリにサインインします。</span><span class="sxs-lookup"><span data-stu-id="57413-434">Sign in to the mobile app as a worker in warehouse *62*.</span></span>
1. <span data-ttu-id="57413-435">メイン メニューで、 **アウトバウンド** を選択します。</span><span class="sxs-lookup"><span data-stu-id="57413-435">On the main menu, select **Outbound**.</span></span>
1. <span data-ttu-id="57413-436">**アウトバウンド** メニューで、 **営業ピッキング** を選択します。</span><span class="sxs-lookup"><span data-stu-id="57413-436">On the **Outbound** menu, select **Sales Picking**.</span></span>
1. <span data-ttu-id="57413-437">**ID** フィールドを選択し、ウェーブ処理から作業 ID を入力します。</span><span class="sxs-lookup"><span data-stu-id="57413-437">Select the **ID** field, and then enter the work ID from the wave processing.</span></span>
1. <span data-ttu-id="57413-438">入力内容を確認します。</span><span class="sxs-lookup"><span data-stu-id="57413-438">Confirm your entry.</span></span>

    <span data-ttu-id="57413-439">次に、ターゲットのライセンス プレート (LP) を入力するように求められます。</span><span class="sxs-lookup"><span data-stu-id="57413-439">Next, you're prompted to enter a target license plate (LP).</span></span> <span data-ttu-id="57413-440">販売注文 1 の明細行 1 は、ピッキングしてターゲットのライセンス プレートに追加する必要があることに注意してください。</span><span class="sxs-lookup"><span data-stu-id="57413-440">Notice that line 1 from sales order 1 is what must be picked and added to the target license plate.</span></span> <span data-ttu-id="57413-441">品目番号、数量、品目の説明、およびピッキング場所が表示されます。</span><span class="sxs-lookup"><span data-stu-id="57413-441">The item number, quantity, item description, and pick location are shown.</span></span>

1. <span data-ttu-id="57413-442">**ターゲット LP** フィールドに、ライセンス プレート番号を入力します。</span><span class="sxs-lookup"><span data-stu-id="57413-442">In the **Target LP** field, enter a license plate number.</span></span>

    <span data-ttu-id="57413-443">処理済みのウェーブから作成されたすべての明細行を、同じターゲットのライセンス プレートにピッキングします。</span><span class="sxs-lookup"><span data-stu-id="57413-443">You will pick all lines that were created from the processed wave onto the same target license plate.</span></span>

1. <span data-ttu-id="57413-444">入力内容を確認します。</span><span class="sxs-lookup"><span data-stu-id="57413-444">Confirm your entry.</span></span>

    <span data-ttu-id="57413-445">モバイル アプリには、ピッキング場所と、ピッキングする必要がある品目および数量を示す一連の **ピッキング** ページが今すぐ表示されます。</span><span class="sxs-lookup"><span data-stu-id="57413-445">The mobile app now presents a series of **Pick** pages that point you to the picking location, and to the item and quantity that must be picked.</span></span> <span data-ttu-id="57413-446">ピッキングされた品目をライセンス プレートに追加したら、ピッキング作業を確認します。</span><span class="sxs-lookup"><span data-stu-id="57413-446">After the picked item is added to the license plate, you will confirm the pick work.</span></span> <span data-ttu-id="57413-447">最後のページは、ピッキングされた品目をソーティング場所にプットするための作業になります。</span><span class="sxs-lookup"><span data-stu-id="57413-447">The last page will be the work to put the picked items into the sorting location.</span></span>

1. <span data-ttu-id="57413-448">最初のピッキング作業を確認します。</span><span class="sxs-lookup"><span data-stu-id="57413-448">Confirm the first pick work.</span></span>
1. <span data-ttu-id="57413-449">次のピッキング作業が表示されます。</span><span class="sxs-lookup"><span data-stu-id="57413-449">The next pick work is shown.</span></span> <span data-ttu-id="57413-450">ピッキングを確定します。</span><span class="sxs-lookup"><span data-stu-id="57413-450">Confirm the pick.</span></span>
1. <span data-ttu-id="57413-451">残りのピッキング作業の確認に進みます。</span><span class="sxs-lookup"><span data-stu-id="57413-451">Continue to confirm the remaining pick work.</span></span>
1. <span data-ttu-id="57413-452">最後の手順は、プット作業を完了することです。</span><span class="sxs-lookup"><span data-stu-id="57413-452">The last step is to complete the put work.</span></span> <span data-ttu-id="57413-453">ソーティング場所へのプット アウェイを確認します。</span><span class="sxs-lookup"><span data-stu-id="57413-453">Confirm the put-away to the sorting location.</span></span>

    <span data-ttu-id="57413-454">"作業が完了しました" というメッセージを受信します。</span><span class="sxs-lookup"><span data-stu-id="57413-454">You receive a "Work completed" message.</span></span>

1. <span data-ttu-id="57413-455">モバイルアプリの **販売ピッキング** を終了します。</span><span class="sxs-lookup"><span data-stu-id="57413-455">Exit **Sales Picking** on the mobile app.</span></span>

### <a name="sortingput-to-wall"></a><span data-ttu-id="57413-456">ソーティング/put-to-wall</span><span class="sxs-lookup"><span data-stu-id="57413-456">Sorting/put-to-wall</span></span>

<span data-ttu-id="57413-457">すべての在庫がソーティング場所に配置されたので、適切なソート位置にソートされる必要があります。</span><span class="sxs-lookup"><span data-stu-id="57413-457">Now that all inventory has been put to the sorting location, it must be sorted to the correct sort position.</span></span>

1. <span data-ttu-id="57413-458">モバイル アプリにサインインします。</span><span class="sxs-lookup"><span data-stu-id="57413-458">Sign in to the mobile app.</span></span>
1. <span data-ttu-id="57413-459">メイン メニューで、 **アウトバウンド** を選択します。</span><span class="sxs-lookup"><span data-stu-id="57413-459">On the main menu, select **Outbound**.</span></span>
1. <span data-ttu-id="57413-460">**アウトバウンド** メニューで、 **ソート** を選択して品目のソートを開始します。</span><span class="sxs-lookup"><span data-stu-id="57413-460">On the **Outbound** menu, select **Sort** to start to sort the items.</span></span>
1. <span data-ttu-id="57413-461">**LP/CON** フィールドで、ピッキングされた販売注文作業のターゲット ライセンス プレートを入力します。</span><span class="sxs-lookup"><span data-stu-id="57413-461">In the **LP/CON** field, enter the target license plate of the picked sales order work.</span></span>
1. <span data-ttu-id="57413-462">入力内容を確認します。</span><span class="sxs-lookup"><span data-stu-id="57413-462">Confirm your entry.</span></span>
1. <span data-ttu-id="57413-463">最初にソートする品目番号を入力します。</span><span class="sxs-lookup"><span data-stu-id="57413-463">Enter the item number to sort first.</span></span>
1. <span data-ttu-id="57413-464">表示する必要のある最初のソート位置はシステムが決定します。</span><span class="sxs-lookup"><span data-stu-id="57413-464">The system determines the first sort position that should be shown.</span></span> <span data-ttu-id="57413-465">ソート位置を確認します。</span><span class="sxs-lookup"><span data-stu-id="57413-465">Confirm the sort position.</span></span>
1. <span data-ttu-id="57413-466">ソート位置にライセンス プレートを割り当てるかどうかを求められます。</span><span class="sxs-lookup"><span data-stu-id="57413-466">You're prompted to assign a license plate to the sort position.</span></span> <span data-ttu-id="57413-467">**LP** フィールドを選択し、ライセンス プレート番号を入力して、入力内容を確認します。</span><span class="sxs-lookup"><span data-stu-id="57413-467">Select the **LP** field, enter a license plate number, and then confirm your entry.</span></span>

    <span data-ttu-id="57413-468">ソート位置は、出荷 ID に関連しているので、ピッキングされた品目を、アウトバウンド出荷および販売注文に固有であるライセンス プレートにソートします。</span><span class="sxs-lookup"><span data-stu-id="57413-468">Because the sort position is related to the shipment ID, you will sort the picked items into a license plate that is specific to the outbound shipment and sales order.</span></span>

    <span data-ttu-id="57413-469">次のページには、品目 ID、数量、ソート位置 ID、"開始" (ピッキング) と "終了" (ソーティング) のライセンス プレート ID を示します。</span><span class="sxs-lookup"><span data-stu-id="57413-469">The next page shows the item ID, quantity, sort position ID, and the "from" (picking) and "to" (sorting) license plate IDs.</span></span> <span data-ttu-id="57413-470">このページの情報は、ピッキング ライセンス プレートから指定された品目と数量をソーティングライセンス プレートにソートするためのガイドです。</span><span class="sxs-lookup"><span data-stu-id="57413-470">The information on this page instructs you to sort the specified item and quantities from the picking license plate into the sorting license plate.</span></span>

1. <span data-ttu-id="57413-471">ソート位置を確認します。</span><span class="sxs-lookup"><span data-stu-id="57413-471">Confirm the sort position.</span></span>
1. <span data-ttu-id="57413-472">最初のソート位置の品目をソートします。</span><span class="sxs-lookup"><span data-stu-id="57413-472">Sort the items in the first sort position.</span></span> <span data-ttu-id="57413-473">入力が完了すると、システムは次のソート位置に指示します。</span><span class="sxs-lookup"><span data-stu-id="57413-473">When you've finished, the system directs you to the next sort position.</span></span>
1. <span data-ttu-id="57413-474">このプロセスを、作業指示書上でピッキングされたすべての明細行に対して繰り返します。</span><span class="sxs-lookup"><span data-stu-id="57413-474">Repeat this process for all picked lines on the work order.</span></span> <span data-ttu-id="57413-475">このプロセスは、品目番号が同じピッキング明細行が複数ある場合にも使用してください。</span><span class="sxs-lookup"><span data-stu-id="57413-475">You should also use this process when there are multiple pick lines that have the same item number.</span></span>

    <span data-ttu-id="57413-476">すべての品目に対してこのプロセスを繰り返すと、次のスキャンされた品目 (作業明細行) からの基準が評価され、どのソーティング位置に配置するかが決定されます。</span><span class="sxs-lookup"><span data-stu-id="57413-476">As you repeat this process for all items, the system evaluates the criteria from the next scanned item (work line) and determines which sorting position it should be put to.</span></span> <span data-ttu-id="57413-477">品目を適切なソート位置に配置するように自動的に指示されます。</span><span class="sxs-lookup"><span data-stu-id="57413-477">You're automatically directed to put the item to the correct sort position.</span></span> <span data-ttu-id="57413-478">確認の設定によっては、位置番号またはライセンス プレート ID を入力して、このアクションを確認するように指示することもできます。</span><span class="sxs-lookup"><span data-stu-id="57413-478">Depending on the confirmation setup, you're also directed to confirm this action by entering the position number or license plate ID.</span></span>

    > [!NOTE]
    > <span data-ttu-id="57413-479">自動ソーティングが有効になっている場合、手動での上書きは使用できません。</span><span class="sxs-lookup"><span data-stu-id="57413-479">If automatic sorting is turned on, manual override isn't available.</span></span>

1. <span data-ttu-id="57413-480">完了したら、Microsoft Dynamics 365 Supply Chain Management で **アウトバウンド ソーティング位置の割り当て** ページを開いて、位置のステータスを確認します。</span><span class="sxs-lookup"><span data-stu-id="57413-480">When you've finished, in Microsoft Dynamics 365 Supply Chain Management, open the **Outbound sorting position assignments** page to review the status of the positions.</span></span>

    - <span data-ttu-id="57413-481">位置が自動的にクローズされた場合は、 **終了と表示** を選択して、終了した位置を表示します。</span><span class="sxs-lookup"><span data-stu-id="57413-481">If positions are closed automatically, select **Show closed** to show the closed positions.</span></span>
    - <span data-ttu-id="57413-482">ソート位置のトランザクションが表示されますので注意して下さい。</span><span class="sxs-lookup"><span data-stu-id="57413-482">Notice that sort position transactions are shown.</span></span> <span data-ttu-id="57413-483">この位置を通じて処理された品目と数量が表示されます。</span><span class="sxs-lookup"><span data-stu-id="57413-483">The item and quantity that were processed through the position are shown.</span></span>

    <span data-ttu-id="57413-484">アウトバウンド ソーティング テンプレートを設定する場合は、 **ソート位置の自動終了** オプションを *はい* に設定します。</span><span class="sxs-lookup"><span data-stu-id="57413-484">When you set up the outbound sorting template, you set the **Auto close sort position** option to *Yes*.</span></span> <span data-ttu-id="57413-485">したがって、最後に予想された在庫が配置された後に、その位置は自動的に終了します。</span><span class="sxs-lookup"><span data-stu-id="57413-485">Therefore, the position is automatically closed after the last expected inventory is put to it.</span></span> <span data-ttu-id="57413-486">並べ替え位置は **終了** になり、ソートされた在庫を *Baydoor* 場所に移動する作業が作成されます。</span><span class="sxs-lookup"><span data-stu-id="57413-486">The sort positions are in **Closed** status, and work has been created to move the sorted inventory to *Baydoor* location.</span></span>

1. <span data-ttu-id="57413-487">ソートされた在庫ピッキング作業を完了して、在庫を出荷場所に移動します。</span><span class="sxs-lookup"><span data-stu-id="57413-487">Complete the sorted inventory picking work to move the inventory to the shipping location.</span></span> <span data-ttu-id="57413-488">在庫の準備ができたら、出荷確定をします。</span><span class="sxs-lookup"><span data-stu-id="57413-488">When the inventory is ready, ship-confirm it.</span></span>

> [!NOTE]
> <span data-ttu-id="57413-489">ソートされた在庫ピッキング作業を正しく処理するには、 **作業指示タイプ** フィールドが *ソート済み在庫ピッキング* に設定されている作業クラス ID を持つモバイル デバイス メニュー項目を、移動や積荷プロセスで使用する必要があります。</span><span class="sxs-lookup"><span data-stu-id="57413-489">For sorted inventory picking work to be processed correctly, a mobile device menu item that has a work class ID where the **Work order type** field is set to *Sorted inventory picking* should be used for the movement and loading process.</span></span>

### <a name="manually-close-a-position-optional"></a><span data-ttu-id="57413-490">位置の手動による終了 (オプション)</span><span class="sxs-lookup"><span data-stu-id="57413-490">Manually close a position (optional)</span></span>

<span data-ttu-id="57413-491">ソート位置を手動で終了する必要がある場合は、アウトバウンド ソーティング テンプレートの **ソート位置の自動終了** オプションを *いいえ* に設定し、ベイのドア エリアに移動する前に決算を実行する必要があります。</span><span class="sxs-lookup"><span data-stu-id="57413-491">If sort positions should be closed manually, the **Auto close sort position** option for the outbound sorting template must be set to *No* , and closing must be done before inventory can be moved to the bay door area.</span></span> <span data-ttu-id="57413-492">位置はさまざまな方法で終了できます。</span><span class="sxs-lookup"><span data-stu-id="57413-492">Positions can be closed in various ways:</span></span>

- <span data-ttu-id="57413-493">倉庫アプリを介して:</span><span class="sxs-lookup"><span data-stu-id="57413-493">Via the warehouse app:</span></span>

    - <span data-ttu-id="57413-494">ユーザーは、その位置に既に存在する品目の 1 つをスキャンして、 **閉じる** を選択してその位置を閉じます。</span><span class="sxs-lookup"><span data-stu-id="57413-494">The user can scan one of the items that are already on the position and then select **Close** to close the position.</span></span>
    - <span data-ttu-id="57413-495">ユーザーが既にソートされたコンテナーを含むコンテナーをスキャンすると、エラーメッセージが表示されます。</span><span class="sxs-lookup"><span data-stu-id="57413-495">If the user scans a container that has already been sorted container, an error message is shown.</span></span> <span data-ttu-id="57413-496">ただし、この時点では、ユーザーはその位置を引き続き終了できます。</span><span class="sxs-lookup"><span data-stu-id="57413-496">However, the user can still continue to close the position.</span></span>

- <span data-ttu-id="57413-497">Microsoft Dynamics 365 Supply Chain Management **アウトバウンド ソーティング位置の割り当て** ページから、</span><span class="sxs-lookup"><span data-stu-id="57413-497">From the Microsoft Dynamics 365 Supply Chain Management **Outbound sorting position assignments** page:</span></span>

    - <span data-ttu-id="57413-498">ユーザーは、アウトバウンド ソーティング位置レコードを選択し、アクション ウィンドウで **位置を終了する** を選択します。</span><span class="sxs-lookup"><span data-stu-id="57413-498">The user can select the outbound sorting position record and then select **Close position** on the Action Pane.</span></span>

## <a name="tips"></a><span data-ttu-id="57413-499">ヒント</span><span class="sxs-lookup"><span data-stu-id="57413-499">Tips</span></span>

- <span data-ttu-id="57413-500">品目が割り当てられている場合、その位置間で品目を移動することはできません。</span><span class="sxs-lookup"><span data-stu-id="57413-500">Items can't be moved between positions after they have been assigned to one.</span></span> <span data-ttu-id="57413-501">システムによって、各品目が特定の位置にどの程度移動する必要があるかが評価されます。</span><span class="sxs-lookup"><span data-stu-id="57413-501">The system evaluates how many of each item should go to a specific position.</span></span>
- <span data-ttu-id="57413-502">ソート テンプレートをコンフィギュレーションして、位置を終了したときに自動的にコンテナーが作成されるようにすることができます。</span><span class="sxs-lookup"><span data-stu-id="57413-502">Sorts template can be configured to automatically create containers when positions are closed.</span></span> <span data-ttu-id="57413-503">このアプローチでは、指定した梱包プロファイルに基づいて、標準のコンテナー ID 構造が作成されます。</span><span class="sxs-lookup"><span data-stu-id="57413-503">This approach will create standard container ID structure that is based on the specified packing profile.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="57413-504">ソーティング位置から移動作業が作成された後、その作業をキャンセルしないでください。</span><span class="sxs-lookup"><span data-stu-id="57413-504">After movement work has been created from the sorting location, you must not cancel the work.</span></span> <span data-ttu-id="57413-505">それ以外の場合は、その中の位置とコンテナーがシステムから削除され、それ以上の処理に使用できなくなります。</span><span class="sxs-lookup"><span data-stu-id="57413-505">Otherwise, the position and the containers in it will be deleted from the system and unavailable for further processing.</span></span> <span data-ttu-id="57413-506">在庫も削除されます。</span><span class="sxs-lookup"><span data-stu-id="57413-506">The inventory will also be removed.</span></span>
