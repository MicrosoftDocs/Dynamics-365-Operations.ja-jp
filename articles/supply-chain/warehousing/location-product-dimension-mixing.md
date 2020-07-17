---
title: 場所の製品分析コードの混在
description: このトピックでは、場所の製品分析コードの混在に関する情報を提供します。 この場所プロファイルの機能は、ファッション業界などで、製品バリアントまたは分析コードを持つ製品を使用した場合に、場所の管理を改善するのに役立ちます。 特定の場所のプロファイルに対して、構成、色、スタイル、およびサイズを混在させることができるかどうか、またはこれらの分析コードのいずれかまたはそれらの組み合わせを同じ場所に配置できるかどうかを決定できます。
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
ms.dyn365.ops.version: Release 10.0.7
ms.openlocfilehash: 968777b918d59b810a189139fbf4d6fee1b5d3f5
ms.sourcegitcommit: a7a7303004620d2e9cef0642b16d89163911dbb4
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 07/01/2020
ms.locfileid: "3529986"
---
# <a name="location-product-dimension-mixing"></a><span data-ttu-id="59d11-105">場所の製品分析コードの混在</span><span class="sxs-lookup"><span data-stu-id="59d11-105">Location product dimension mixing</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="59d11-106">場所の製品分析コードの混合は、ファッション業界などで、製品バリアントまたは分析コードを持つ製品を使用した場合に、場所の管理を改善するのに役立つ場所プロファイルの機能です。</span><span class="sxs-lookup"><span data-stu-id="59d11-106">Location product dimension mixing is location profile functionality that helps improve location management when product variants or products that have dimensions are used, such as in the fashion industry.</span></span> <span data-ttu-id="59d11-107">特定の場所のプロファイルに対して、構成、色、スタイル、およびサイズを混在させることができるかどうか、またはこれらの分析コードのいずれかまたはそれらの組み合わせを同じ場所に配置できるかどうかを決定できます。</span><span class="sxs-lookup"><span data-stu-id="59d11-107">It lets you decide whether configurations, colors, styles, and sizes can be mixed for a specific location profile, or whether just one of these dimensions or a combination of them can be put to the same location.</span></span>

## <a name="turn-on-the-location-product-dimension-mixing-feature"></a><span data-ttu-id="59d11-108">場所の製品分析コードの混合機能を有効にする</span><span class="sxs-lookup"><span data-stu-id="59d11-108">Turn on the Location product dimension mixing feature</span></span>

<span data-ttu-id="59d11-109">場所の製品分析コードの混合機能を使用するには、システム上で有効にする必要があります。</span><span class="sxs-lookup"><span data-stu-id="59d11-109">Before you can use location product dimension mixing, the feature must be turned on in your system.</span></span> <span data-ttu-id="59d11-110">管理者は、[機能の管理](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) ワークスペースを使用して、機能の状態を確認し、必要に応じて有効にすることができます。</span><span class="sxs-lookup"><span data-stu-id="59d11-110">Admins can use the [Feature management](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) workspace to check the status of the feature and turn it on if it's required.</span></span> <span data-ttu-id="59d11-111">この機能は、次のようにして表示されます。</span><span class="sxs-lookup"><span data-stu-id="59d11-111">There, the feature is listed in the following way:</span></span>

- <span data-ttu-id="59d11-112">**モジュール:** *倉庫管理*</span><span class="sxs-lookup"><span data-stu-id="59d11-112">**Module:** *Warehouse management*</span></span>
- <span data-ttu-id="59d11-113">**機能名 :** *場所の製品分析コードの混合*</span><span class="sxs-lookup"><span data-stu-id="59d11-113">**Feature name:** *Location product dimension mixing*</span></span>

## <a name="setup"></a><span data-ttu-id="59d11-114">セットアップ</span><span class="sxs-lookup"><span data-stu-id="59d11-114">Setup</span></span>

<span data-ttu-id="59d11-115">倉庫の場所は、場所のプロパティに関連したプロファイルを有している必要があります。</span><span class="sxs-lookup"><span data-stu-id="59d11-115">Every location in the warehouse needs to have a location profile associated with it that describes the properties of the location.</span></span> <span data-ttu-id="59d11-116">そのため、同じ場所プロファイルを使用するすべての場所では、設定後に製品分析コードの混合を許可できます。</span><span class="sxs-lookup"><span data-stu-id="59d11-116">Therefore, all locations that use the same location profile will be able to allow product dimension mixing after it has been set up.</span></span>

### <a name="configure-location-profiles-to-allow-product-dimension-mixing"></a><span data-ttu-id="59d11-117">製品分析コードの混合を許可するための場所プロファイルの構成</span><span class="sxs-lookup"><span data-stu-id="59d11-117">Configure location profiles to allow product dimension mixing</span></span>

1. <span data-ttu-id="59d11-118">**倉庫管理 \> 設定 \> 倉庫 \> 場所プロファイル**に移動します。</span><span class="sxs-lookup"><span data-stu-id="59d11-118">Go to **Warehouse management \> Setup \> Warehouse \> Location profiles**.</span></span>
1. <span data-ttu-id="59d11-119">場所プロファイルの一覧で**バルク**を選択します。</span><span class="sxs-lookup"><span data-stu-id="59d11-119">In the list of location profiles, select **BULK**.</span></span>
1. <span data-ttu-id="59d11-120">アクション ウィンドウで、**編集**を選択します。</span><span class="sxs-lookup"><span data-stu-id="59d11-120">On the Action Pane, select **Edit**.</span></span>
1. <span data-ttu-id="59d11-121">**一般**クイック タブで、**場所の製品分析コード固有の混合を有効にする**オプションを*はい*に設定します。</span><span class="sxs-lookup"><span data-stu-id="59d11-121">On the **General** FastTab, set the **Enable location product dimension specific mixing** option to *Yes*.</span></span>

    > [!NOTE]
    > <span data-ttu-id="59d11-122">**品目の混合を許可する**オプションが*いいえ*に設定されている場合にのみ、このオプションを*はい*に設定できます。</span><span class="sxs-lookup"><span data-stu-id="59d11-122">You can set this option to *Yes* only if the **Allow mixed items** option is set to *No*.</span></span>

1. <span data-ttu-id="59d11-123">**許可された製品分析コードの混合**クイック タブで、**サイズ** オプションを*はい*に設定します。</span><span class="sxs-lookup"><span data-stu-id="59d11-123">On the **Allowed product dimension mixing** FastTab, set the **Size** option to *Yes*.</span></span> <span data-ttu-id="59d11-124">このトピックで説明するシナリオでは、異なる**サイズ**分析コードが設定されている製品に対してのみ混合を実行できます。</span><span class="sxs-lookup"><span data-stu-id="59d11-124">In the scenario that is described in this topic, mixing can be done only for products that have different **Size** dimensions.</span></span> <span data-ttu-id="59d11-125">ただし、他のオプションも使用可能です。</span><span class="sxs-lookup"><span data-stu-id="59d11-125">However, other options are also available.</span></span>
1. <span data-ttu-id="59d11-126">**保存** を選択します。</span><span class="sxs-lookup"><span data-stu-id="59d11-126">Select **Save**.</span></span>

### <a name="create-a-new-product-master-and-product-variants"></a><span data-ttu-id="59d11-127">新しい製品マスターおよび製品バリアントの作成</span><span class="sxs-lookup"><span data-stu-id="59d11-127">Create a new product master and product variants</span></span>

1. <span data-ttu-id="59d11-128">**製品情報管理 \> 製品 \> 製品マスター**に移動します。</span><span class="sxs-lookup"><span data-stu-id="59d11-128">Go to **Product information management \> Products \> Product masters**.</span></span>
1. <span data-ttu-id="59d11-129">アクション ウィンドウで、**新規**を選択して新しい製品マスターを作成します。</span><span class="sxs-lookup"><span data-stu-id="59d11-129">On the Action Pane, select **New** to create a product master.</span></span>
1. <span data-ttu-id="59d11-130">**新しい製品**ダイアログ ボックスに次の値を設定します。</span><span class="sxs-lookup"><span data-stu-id="59d11-130">In the **New product** dialog box, set the following values:</span></span>

    - <span data-ttu-id="59d11-131">**製品タイプ :** *品目*</span><span class="sxs-lookup"><span data-stu-id="59d11-131">**Product type:** *Item*</span></span>
    - <span data-ttu-id="59d11-132">**製品サブタイプ :** *製品マスター*</span><span class="sxs-lookup"><span data-stu-id="59d11-132">**Product subtype:** *Product master*</span></span>
    - <span data-ttu-id="59d11-133">**製品番号 :** *B0001*</span><span class="sxs-lookup"><span data-stu-id="59d11-133">**Product number:** *B0001*</span></span>
    - <span data-ttu-id="59d11-134">**製品名:** *B0001 サイズ*</span><span class="sxs-lookup"><span data-stu-id="59d11-134">**Product name:** *B0001 Size*</span></span>
    - <span data-ttu-id="59d11-135">**製品分析コード グループ :** *サイズ*</span><span class="sxs-lookup"><span data-stu-id="59d11-135">**Product dimension group:** *Size*</span></span>
    - <span data-ttu-id="59d11-136">**構成テクノロジ :** *事前に定義されたバリアント*</span><span class="sxs-lookup"><span data-stu-id="59d11-136">**Configuration technology:** *Predefined variant*</span></span>

1. <span data-ttu-id="59d11-137">**OK** を選択します。</span><span class="sxs-lookup"><span data-stu-id="59d11-137">Select **OK**.</span></span>
1. <span data-ttu-id="59d11-138">**製品の詳細**ページの、**一般**クイック タブで、次の値を設定します。</span><span class="sxs-lookup"><span data-stu-id="59d11-138">On the **Product details** page, on the **General** FastTab, set the following values:</span></span>

    - <span data-ttu-id="59d11-139">**バリアントの自動生成 :** *はい*</span><span class="sxs-lookup"><span data-stu-id="59d11-139">**Generate variants automatically:** *Yes*</span></span>
    - <span data-ttu-id="59d11-140">**サイズ グループ :** *CASUALDHIR*</span><span class="sxs-lookup"><span data-stu-id="59d11-140">**Size group:** *CASUALDHIR*</span></span>

1. <span data-ttu-id="59d11-141">事前に定義されたバリアントを表示するには、アクション ウィンドウで**製品バリアント**を選択します。</span><span class="sxs-lookup"><span data-stu-id="59d11-141">To view the predefined variants, on the Action Pane, select **Product variants**.</span></span>

    <span data-ttu-id="59d11-142">**製品バリアント** ページが表示され、サイズ グループの構成のバリアント一覧が表示されます。</span><span class="sxs-lookup"><span data-stu-id="59d11-142">The **Product variants** page appears and shows a list of variants from the configuration of the size group.</span></span>

### <a name="release-products-to-the-usmf-company"></a><span data-ttu-id="59d11-143">USMF 会社に製品をリリースする</span><span class="sxs-lookup"><span data-stu-id="59d11-143">Release products to the USMF company</span></span>

1. <span data-ttu-id="59d11-144">アクション ウィンドウで、**製品のリリース**を選択します。</span><span class="sxs-lookup"><span data-stu-id="59d11-144">On the Action Pane, select **Release products**.</span></span>
1. <span data-ttu-id="59d11-145">**リリースする製品の選択**ページで、製品番号 *B0001* が一覧に表示されていることを確認し、**次へ**を選択します。</span><span class="sxs-lookup"><span data-stu-id="59d11-145">On the **Select products to release** page, confirm that product number *B0001* is in the list, and then select **Next**.</span></span>
1. <span data-ttu-id="59d11-146">**次へ**を選択して、リリースする製品バリアントを確認します。</span><span class="sxs-lookup"><span data-stu-id="59d11-146">Select **Next** to confirm the product variants to release.</span></span>
1. <span data-ttu-id="59d11-147">**リリースする会社を選択**ページで *USMF* を選択し、**次へ**を選択して選択を確定します。</span><span class="sxs-lookup"><span data-stu-id="59d11-147">On the **Select companies to release to** page, select *USMF*, and then select **Next** to confirm the selection.</span></span>
1. <span data-ttu-id="59d11-148">**選択の確認**ページで、**完了**を選択してリリースを完了します。</span><span class="sxs-lookup"><span data-stu-id="59d11-148">On the **Confirm selection** page, select **Finish** to complete the release.</span></span>

    <span data-ttu-id="59d11-149">「処理が完了しました」というメッセージが表示されます。</span><span class="sxs-lookup"><span data-stu-id="59d11-149">You receive an "Operation completed" message.</span></span>

### <a name="update-a-released-product-in-the-usmf-company"></a><span data-ttu-id="59d11-150">USMF 会社のリリースされた製品を更新する</span><span class="sxs-lookup"><span data-stu-id="59d11-150">Update a released product in the USMF company</span></span>

1. <span data-ttu-id="59d11-151">**USMF** 会社にサイン インしていることを確認してください。</span><span class="sxs-lookup"><span data-stu-id="59d11-151">Make sure that you're signed in to the **USMF** company.</span></span>
1. <span data-ttu-id="59d11-152">**製品情報管理 \> 製品 \> リリース済製品** の順に選択して、リリース済の製品の作成を完了します。</span><span class="sxs-lookup"><span data-stu-id="59d11-152">Go to **Product information management \> Products \> Released products** to finish creating the released product.</span></span>
1. <span data-ttu-id="59d11-153">品目番号 *B0001* を検索して選択し、**リリース済製品の詳細**ページを開きます。</span><span class="sxs-lookup"><span data-stu-id="59d11-153">Find and select item number *B0001* to open the **Released product details** page.</span></span>
1. <span data-ttu-id="59d11-154">アクション ウィンドウで、**編集**を選択します。</span><span class="sxs-lookup"><span data-stu-id="59d11-154">On the Action Pane, select **Edit**.</span></span>
1. <span data-ttu-id="59d11-155">**一般**クイック タブで、**品目モデル グループ** フィールドが *FIFO* に設定されていることを確認します。</span><span class="sxs-lookup"><span data-stu-id="59d11-155">On the **General** FastTab, make sure that the **Item model group** field is set to *FIFO*.</span></span>
1. <span data-ttu-id="59d11-156">アクション ウィンドウで、**製品**タブの**設定**グループで、**分析コード グループ**を選択します。</span><span class="sxs-lookup"><span data-stu-id="59d11-156">On the Action Pane, on the **Product** tab, in the **Set up** group, select **Dimension groups**.</span></span>
1. <span data-ttu-id="59d11-157">次の値を設定します。</span><span class="sxs-lookup"><span data-stu-id="59d11-157">Set the following values:</span></span>

    - <span data-ttu-id="59d11-158">**保管分析コード グループ :** *Ware*</span><span class="sxs-lookup"><span data-stu-id="59d11-158">**Storage dimension group:** *Ware*</span></span>
    - <span data-ttu-id="59d11-159">**追跡用分析コード グループ :** *なし*</span><span class="sxs-lookup"><span data-stu-id="59d11-159">**Tracking dimension group:** *None*</span></span>

1. <span data-ttu-id="59d11-160">**OK** を選択します。</span><span class="sxs-lookup"><span data-stu-id="59d11-160">Select **OK**.</span></span>
1. <span data-ttu-id="59d11-161">アクション ウィンドウで、**製品**タブの**設定**グループで、**引当階層**を選択します。</span><span class="sxs-lookup"><span data-stu-id="59d11-161">On the Action Pane, on the **Product** tab, in the **Set up** group, select **Reservation hierarchy**.</span></span>
1. <span data-ttu-id="59d11-162">**引当階層**フィールドを*既定値*に設定し、**OK** を選択します。</span><span class="sxs-lookup"><span data-stu-id="59d11-162">Set the **Reservation hierarchy** field to *Default*, and then select **OK**.</span></span>
1. <span data-ttu-id="59d11-163">**一般**クイック タブの**管理**セクションで、選択内容が更新されていることを確認します。</span><span class="sxs-lookup"><span data-stu-id="59d11-163">On the **General** FastTab, in the **Administration** section, notice that your selections have been updated.</span></span>
1. <span data-ttu-id="59d11-164">**購入**クイック タブの**価格**フィールドに *10* と入力します。</span><span class="sxs-lookup"><span data-stu-id="59d11-164">On the **Purchase** FastTab, in the **Price** field, enter *10*.</span></span>
1. <span data-ttu-id="59d11-165">**品目グループ** フィールドの**原価の管理**クイック タブで、*オーディオ*と入力します。</span><span class="sxs-lookup"><span data-stu-id="59d11-165">On the **Manage costs** FastTab, in the **Item group** field, enter *Audio*.</span></span>
1. <span data-ttu-id="59d11-166">**購入**クイック タブの**価格**フィールドに *10* と入力します。</span><span class="sxs-lookup"><span data-stu-id="59d11-166">On the **Purchase** FastTab, in the **Price** field, enter *10*.</span></span>
1. <span data-ttu-id="59d11-167">**倉庫**クイック タブの**単位順序グループ ID** フィールドに、*ea* と入力します。</span><span class="sxs-lookup"><span data-stu-id="59d11-167">On the **Warehouse** FastTab, in the **Unit sequence group ID** field, enter *ea*.</span></span>
1. <span data-ttu-id="59d11-168">**保存** を選択します。</span><span class="sxs-lookup"><span data-stu-id="59d11-168">Select **Save**.</span></span>

### <a name="create-a-location-directive"></a><span data-ttu-id="59d11-169">場所のディレクティブを作成する</span><span class="sxs-lookup"><span data-stu-id="59d11-169">Create a location directive</span></span>

1. <span data-ttu-id="59d11-170">**倉庫管理 \> 設定 \> 場所のディレクティブ** に移動します。</span><span class="sxs-lookup"><span data-stu-id="59d11-170">Go to **Warehouse management \> Setup \> Location directives**.</span></span>
1. <span data-ttu-id="59d11-171">左ウィンドウの**作業指示書タイプ** フィールドで*発注書*を選択します。</span><span class="sxs-lookup"><span data-stu-id="59d11-171">In the left pane, in the **Work order type** field, select *Purchase orders*.</span></span>
1. <span data-ttu-id="59d11-172">一覧で、*24 PO Direct* という名前の場所ディレクティブを選択します。</span><span class="sxs-lookup"><span data-stu-id="59d11-172">In the list, select the location directive that is named *24 PO Direct*.</span></span>
1. <span data-ttu-id="59d11-173">**場所ディレクティブ アクション** クイック タブで、**新規**を選択してグリッドに明細行を追加します。</span><span class="sxs-lookup"><span data-stu-id="59d11-173">On the **Location Directive Actions** FastTab, select **New** to add a line to the grid.</span></span>
1. <span data-ttu-id="59d11-174">新しい明細行で、次の値を設定します。</span><span class="sxs-lookup"><span data-stu-id="59d11-174">On the new line, set the following values:</span></span>

    - <span data-ttu-id="59d11-175">**シーケンス番号 :** *1*</span><span class="sxs-lookup"><span data-stu-id="59d11-175">**Sequence number:** *1*</span></span>

        <span data-ttu-id="59d11-176">新しい明細行は、既に存在する明細行の前にある必要があります。</span><span class="sxs-lookup"><span data-stu-id="59d11-176">The new line should be in front of the previously existing line.</span></span> <span data-ttu-id="59d11-177">変更を加えるには、ツール バーの**上へ移動**または**下へ移動**ボタンを使用するか、既存の明細行の**シーケンス番号**値を *2* に変更します。</span><span class="sxs-lookup"><span data-stu-id="59d11-177">To make the change, use the **Move up** and **Move down** buttons on the toolbar, or change the existing line's **Sequence number** value to *2*.</span></span>

    - <span data-ttu-id="59d11-178">**名前 :** *バルク場所プロファイルに配置*</span><span class="sxs-lookup"><span data-stu-id="59d11-178">**Name:** *Put to BULK Location profile*</span></span>
    - <span data-ttu-id="59d11-179">**固定の場所の使用 :** *固定の場所および固定されていない場所*</span><span class="sxs-lookup"><span data-stu-id="59d11-179">**Fixed location usage:** *Fixed and non-fixed locations*</span></span>
    - <span data-ttu-id="59d11-180">**マイナス在庫を許可 :** *このチェック ボックスをオフにする (許可しない)*</span><span class="sxs-lookup"><span data-stu-id="59d11-180">**Allow negative inventory:** *Clear this check box (=No)*</span></span>
    - <span data-ttu-id="59d11-181">**バッチが有効 :** *このチェックボックスをオフにする (許可しない)*</span><span class="sxs-lookup"><span data-stu-id="59d11-181">**Batch enabled:** *Clear this check box (=No)*</span></span>
    - <span data-ttu-id="59d11-182">**戦略 :** *なし*</span><span class="sxs-lookup"><span data-stu-id="59d11-182">**Strategy:** *None*</span></span>

1. <span data-ttu-id="59d11-183">新しい明細行が選択されたままの状態で、グリッドの上にある**クエリの編集**を選択します。</span><span class="sxs-lookup"><span data-stu-id="59d11-183">While the new line is still selected, select **Edit query** above the grid.</span></span>
1. <span data-ttu-id="59d11-184">製品クエリ ダイアログ ボックスの**範囲**タブで**追加**を選択して、グリッドに明細行を追加します。</span><span class="sxs-lookup"><span data-stu-id="59d11-184">In the query dialog box, on the **Range** tab, select **Add** to add a line to the grid.</span></span>
1. <span data-ttu-id="59d11-185">新しい明細行で、次の値を設定します。</span><span class="sxs-lookup"><span data-stu-id="59d11-185">On the new line, set the following values:</span></span>

    - <span data-ttu-id="59d11-186">**テーブル:** *場所*</span><span class="sxs-lookup"><span data-stu-id="59d11-186">**Table:** *Locations*</span></span>
    - <span data-ttu-id="59d11-187">**派生テーブル :** *場所*</span><span class="sxs-lookup"><span data-stu-id="59d11-187">**Derived table:** *Locations*</span></span>
    - <span data-ttu-id="59d11-188">\**フィールド:\*\*\*場所のプロファイル ID*</span><span class="sxs-lookup"><span data-stu-id="59d11-188">**Field:** *Location profile ID*</span></span>
    - <span data-ttu-id="59d11-189">**基準:** *BULK*</span><span class="sxs-lookup"><span data-stu-id="59d11-189">**Criteria:** *BULK*</span></span>

1. <span data-ttu-id="59d11-190">**OK** を選択します。</span><span class="sxs-lookup"><span data-stu-id="59d11-190">Select **OK**.</span></span>
1. <span data-ttu-id="59d11-191">**場所ディレクティブ** ページで、**保存**を選択します。</span><span class="sxs-lookup"><span data-stu-id="59d11-191">On the **Location directives** page, on the Action Pane, select **Save**.</span></span>

> [!NOTE]
> <span data-ttu-id="59d11-192">**場所ディレクティブ アクション** クイック タブの**戦略**フィールドで、 *連結*場所戦略を使用すると、**場所のプロファイル**の**許可された製品分析コードの混合**の設定が上書きされ、この動作が設定で許可されていない場合でも、品目は同じ場所に配置されます。</span><span class="sxs-lookup"><span data-stu-id="59d11-192">On the **Location Directive Actions** FastTab **Strategy** field, if you use the *Consolidate* location strategy, the setup of the **Allowed product dimension mixing** FastTab on the **Location profiles** will be overridden, and items will be put to the same location even if this behavior isn't allowed by the setup.</span></span>

### <a name="create-a-mobile-device-menu-item"></a><span data-ttu-id="59d11-193">品目のモバイル デバイス メニューの作成</span><span class="sxs-lookup"><span data-stu-id="59d11-193">Create a mobile device menu item</span></span>

1. <span data-ttu-id="59d11-194">**倉庫管理 \> 設定 \> モバイル デバイス \> モバイル デバイスのメニュー品目**の順に移動します。</span><span class="sxs-lookup"><span data-stu-id="59d11-194">Go to **Warehouse management \> Setup \> Mobile device \> Mobile device menu items**.</span></span>
1. <span data-ttu-id="59d11-195">アクション ウィンドウで、**新規**を選択して、並べ替えに使用するメニュー項目を作成します。</span><span class="sxs-lookup"><span data-stu-id="59d11-195">On the Action Pane, select **New** to create a menu item to use for sorting.</span></span>
1. <span data-ttu-id="59d11-196">ヘッダーで、次の値を設定します。</span><span class="sxs-lookup"><span data-stu-id="59d11-196">In the header, set the following values:</span></span>

    - <span data-ttu-id="59d11-197">**メニュー項目名 :** *発注書明細行受取*</span><span class="sxs-lookup"><span data-stu-id="59d11-197">**Menu item name:** *PO line receiving*</span></span>
    - <span data-ttu-id="59d11-198">**タイトル :** *発注書明細行受取*</span><span class="sxs-lookup"><span data-stu-id="59d11-198">**Title:** *PO line receiving*</span></span>
    - <span data-ttu-id="59d11-199">**モード:** *作業*</span><span class="sxs-lookup"><span data-stu-id="59d11-199">**Mode:** *Work*</span></span>
    - <span data-ttu-id="59d11-200">**既存の作業を使用する :** *いいえ*</span><span class="sxs-lookup"><span data-stu-id="59d11-200">**Use existing work:** *No*</span></span>

1. <span data-ttu-id="59d11-201">**一般**クイック タブで、次の値を設定します。</span><span class="sxs-lookup"><span data-stu-id="59d11-201">On the **General** FastTab, set the following values:</span></span>

    - <span data-ttu-id="59d11-202">**作業の作成プロセス :** *購買注文明細行の受取とプットアウェイ*</span><span class="sxs-lookup"><span data-stu-id="59d11-202">**Work creation process:** *Purchase order line receiving and putaway*</span></span>
    - <span data-ttu-id="59d11-203">**ライセンスプレートの生成:** *はい*</span><span class="sxs-lookup"><span data-stu-id="59d11-203">**Generate license plate:** *Yes*</span></span>

1. <span data-ttu-id="59d11-204">**保存** を選択します。</span><span class="sxs-lookup"><span data-stu-id="59d11-204">Select **Save**.</span></span>

### <a name="configure-the-mobile-device-menu"></a><span data-ttu-id="59d11-205">モバイル デバイスのメニューの構成</span><span class="sxs-lookup"><span data-stu-id="59d11-205">Configure the mobile device menu</span></span>

1. <span data-ttu-id="59d11-206">**倉庫管理 \> 設定 \> モバイル デバイス \> モバイル デバイス メニュー**の順に移動します。</span><span class="sxs-lookup"><span data-stu-id="59d11-206">Go to **Warehouse management \> Setup \> Mobile device \> Mobile device menu**.</span></span>
1. <span data-ttu-id="59d11-207">メニューの一覧で**入庫**を選択します。</span><span class="sxs-lookup"><span data-stu-id="59d11-207">In the list of menus, select **Inbound**.</span></span>
1. <span data-ttu-id="59d11-208">アクション ウィンドウで、**編集**を選択します。</span><span class="sxs-lookup"><span data-stu-id="59d11-208">On the Action Pane, select **Edit**.</span></span>
1. <span data-ttu-id="59d11-209">**使用可能なメニューとメニュー項目**の一覧で、**発注書明細行受取**メニュー項目を検索して選択します。</span><span class="sxs-lookup"><span data-stu-id="59d11-209">In the **Available Menus And Menu Items** list, find and select the **PO line receiving** menu item.</span></span>
1. <span data-ttu-id="59d11-210">右矢印ボタンを選択して、**発注書明細行受取**メニュー項目を**メニュー構造**の一覧に移動します。</span><span class="sxs-lookup"><span data-stu-id="59d11-210">Select the right arrow button to move the **PO line receiving** menu item to the **Menu Structure** list.</span></span> <span data-ttu-id="59d11-211">このようにして、選択したメニューに新しいメニュー項目を追加します。</span><span class="sxs-lookup"><span data-stu-id="59d11-211">In this way, you add your new menu item to the selected menu.</span></span>
1. <span data-ttu-id="59d11-212">**保存** を選択します。</span><span class="sxs-lookup"><span data-stu-id="59d11-212">Select **Save**.</span></span>

## <a name="scenario"></a><span data-ttu-id="59d11-213">シナリオ</span><span class="sxs-lookup"><span data-stu-id="59d11-213">Scenario</span></span>

<span data-ttu-id="59d11-214">このデモ シナリオでは、場所プロファイルで品目の混合が許可されていない場合でも、 *場所の製品分析コードの混合*機能が有効になっている場合に、どのように 2 つの異なる製品バリアントを同じ場所に配置できるかについて説明します。</span><span class="sxs-lookup"><span data-stu-id="59d11-214">This demo scenario shows how two different product variants can be put to the same location when the location profile doesn't allow for mixed items, but the *Location product dimension mixing* feature is enabled.</span></span> <span data-ttu-id="59d11-215">この場合は、**サイズ** バリアントを基準として使用します。</span><span class="sxs-lookup"><span data-stu-id="59d11-215">In this case, you will use the **Size** variant as the criterion.</span></span>

<span data-ttu-id="59d11-216">開始する前に、*バルク*場所プロファイルを使用する空の場所が倉庫 *24* にあることを確認してください 。</span><span class="sxs-lookup"><span data-stu-id="59d11-216">Before you begin, make sure that there are empty locations in warehouse *24* that use the *BULK* location profile.</span></span>

### <a name="create-a-purchase-order"></a><span data-ttu-id="59d11-217">発注書の作成</span><span class="sxs-lookup"><span data-stu-id="59d11-217">Create a purchase order</span></span>

<span data-ttu-id="59d11-218">次の 3 つの明細行がある発注書を作成します。同じ製品番号で異なる**サイズ** バリアントの 2 つの明細行と、バリアントを持たない異なる製品の 3 番目の明細行です。</span><span class="sxs-lookup"><span data-stu-id="59d11-218">You will create a purchase order that has three lines: two lines for the same product number but different **Size** variants, and a third line for a different product that has no variants.</span></span>

1. <span data-ttu-id="59d11-219">**買掛金勘定 \> 発注書 \> すべての発注書**に移動します。</span><span class="sxs-lookup"><span data-stu-id="59d11-219">Go to **Accounts payable \> Purchase orders \> All purchase orders**.</span></span>
1. <span data-ttu-id="59d11-220">アクション ウィンドウで、**新規**を選択します。</span><span class="sxs-lookup"><span data-stu-id="59d11-220">On the Action Pane, select **New**.</span></span>
1. <span data-ttu-id="59d11-221">**発注書の作成**ダイアログ ボックスで、次の値を設定します。</span><span class="sxs-lookup"><span data-stu-id="59d11-221">In the **Create purchase order** dialog box, set the following values:</span></span>

    - <span data-ttu-id="59d11-222">**仕入先勘定 :** *1001*</span><span class="sxs-lookup"><span data-stu-id="59d11-222">**Vendor account:** *1001*</span></span>
    - <span data-ttu-id="59d11-223">**倉庫:** *24*</span><span class="sxs-lookup"><span data-stu-id="59d11-223">**Warehouse:** *24*</span></span>

1. <span data-ttu-id="59d11-224">**OK** を選択します。</span><span class="sxs-lookup"><span data-stu-id="59d11-224">Select **OK**.</span></span>
1. <span data-ttu-id="59d11-225">発注書が作成され、**発注書明細行**クイック タブに新しい明細行が追加されます。</span><span class="sxs-lookup"><span data-stu-id="59d11-225">The purchase order is created, and a new line is added on the **Purchase order lines** FastTab.</span></span> <span data-ttu-id="59d11-226">発注書番号をメモします。</span><span class="sxs-lookup"><span data-stu-id="59d11-226">Make a note of the purchase order number.</span></span>
1. <span data-ttu-id="59d11-227">新しい明細行で、次の値を設定します。</span><span class="sxs-lookup"><span data-stu-id="59d11-227">On the new line, set the following values:</span></span>

    - <span data-ttu-id="59d11-228">**品目番号:** *B0001*</span><span class="sxs-lookup"><span data-stu-id="59d11-228">**Item number:** *B0001*</span></span>
    - <span data-ttu-id="59d11-229">**サイズ** *L*</span><span class="sxs-lookup"><span data-stu-id="59d11-229">**Size** *L*</span></span>
    - <span data-ttu-id="59d11-230">**数量:** *2*</span><span class="sxs-lookup"><span data-stu-id="59d11-230">**Quantity:** *2*</span></span>

1. <span data-ttu-id="59d11-231">グリッドの上の**明細行の追加**を選択して、2 つ目の発注書明細行を追加し、次の値を設定します。</span><span class="sxs-lookup"><span data-stu-id="59d11-231">Select **Add line** above the grid to add a second purchase order line, and set the following values:</span></span>

    - <span data-ttu-id="59d11-232">**品目番号:** *B0001*</span><span class="sxs-lookup"><span data-stu-id="59d11-232">**Item number:** *B0001*</span></span>
    - <span data-ttu-id="59d11-233">**サイズ** *XL*</span><span class="sxs-lookup"><span data-stu-id="59d11-233">**Size** *XL*</span></span>
    - <span data-ttu-id="59d11-234">**数量:** *2*</span><span class="sxs-lookup"><span data-stu-id="59d11-234">**Quantity:** *2*</span></span>

1. <span data-ttu-id="59d11-235">**明細行の追加**を選択して、3 つ目の発注書明細行を追加し、次の値を設定します。</span><span class="sxs-lookup"><span data-stu-id="59d11-235">Select **Add line** to add a third purchase order line, and set the following values:</span></span>

    - <span data-ttu-id="59d11-236">**品目番号:** *A0001*</span><span class="sxs-lookup"><span data-stu-id="59d11-236">**Item number:** *A0001*</span></span>
    - <span data-ttu-id="59d11-237">**数量:** *1*</span><span class="sxs-lookup"><span data-stu-id="59d11-237">**Quantity:** *1*</span></span>

<span data-ttu-id="59d11-238">1. **保存** を選択します。</span><span class="sxs-lookup"><span data-stu-id="59d11-238">1.Select **Save**.</span></span>

### <a name="receive-purchase-order-lines-in-the-warehouse-app"></a><span data-ttu-id="59d11-239">倉庫アプリでの発注書明細行の受取</span><span class="sxs-lookup"><span data-stu-id="59d11-239">Receive purchase order lines in the warehouse app</span></span>

1. <span data-ttu-id="59d11-240">倉庫 *24* を有効にしたユーザーとして、倉庫アプリにログインします。</span><span class="sxs-lookup"><span data-stu-id="59d11-240">Sign in to the warehouse app as a user who is enabled for warehouse *24*.</span></span>
1. <span data-ttu-id="59d11-241">**入庫**メニューを選択します。</span><span class="sxs-lookup"><span data-stu-id="59d11-241">Select the **Inbound** menu.</span></span>
1. <span data-ttu-id="59d11-242">**発注書明細行受取**を選択します。</span><span class="sxs-lookup"><span data-stu-id="59d11-242">Select **PO Line receiving**.</span></span>
1. <span data-ttu-id="59d11-243">**PONUM** フィールドを選択してから、発注書番号を入力します。</span><span class="sxs-lookup"><span data-stu-id="59d11-243">Select the **PONUM** field, and then enter the purchase order number.</span></span>
1. <span data-ttu-id="59d11-244">入力を確認するには、ページの下部にある確認ボタン (✔) を選択します。</span><span class="sxs-lookup"><span data-stu-id="59d11-244">Confirm your entry by selecting the confirm button ( ✔ ) at the bottom of the page.</span></span>
1. <span data-ttu-id="59d11-245">入庫する発注書の明細行番号を入力します。</span><span class="sxs-lookup"><span data-stu-id="59d11-245">Enter the line number from the purchase order that is being received.</span></span> <span data-ttu-id="59d11-246">**LINENUM** フィールドを選択し、数字パッドを使用して *1* を入力します。</span><span class="sxs-lookup"><span data-stu-id="59d11-246">Select the **LINENUM** field, and then use the number pad to enter *1*.</span></span>
1. <span data-ttu-id="59d11-247">入力内容を確認します。</span><span class="sxs-lookup"><span data-stu-id="59d11-247">Confirm your entry.</span></span>
1. <span data-ttu-id="59d11-248">入庫する数量を入力します。</span><span class="sxs-lookup"><span data-stu-id="59d11-248">Enter the quantity to receive.</span></span> <span data-ttu-id="59d11-249">プラス記号 (**+**) ボタンを2回選択すると、**数量**フィールドの値が *2* に増加します。</span><span class="sxs-lookup"><span data-stu-id="59d11-249">Select the plus sign (**+**) button two times to increase the value in the **Qty** field to *2*.</span></span>
1. <span data-ttu-id="59d11-250">入力内容を登録するには、ページの下部にあるボタン (✔) を選択し、ボタン (✔) をもう一度選択して入力内容を確認します。</span><span class="sxs-lookup"><span data-stu-id="59d11-250">Register your entry by selecting the button ( ✔ ) at the bottom of the page, and then confirm your entry by selecting the button ( ✔ ) again.</span></span>
1. <span data-ttu-id="59d11-251">**発注書 : 配置**ページの情報を表示します。</span><span class="sxs-lookup"><span data-stu-id="59d11-251">View the information on the **Purchase orders: Put** page.</span></span> <span data-ttu-id="59d11-252">このページには、プットアウェイ (作業 1) のために作成された作業が表示されます。</span><span class="sxs-lookup"><span data-stu-id="59d11-252">This page shows the work that has been created for the put-away (Work 1).</span></span>

    <span data-ttu-id="59d11-253">入庫品目がプットアウェイされる場所、ライセンス プレート、品目、サイズ、および完了した**発注書明細行受取**の数量が表示されます。</span><span class="sxs-lookup"><span data-stu-id="59d11-253">The location where the received item will be put away, the license plate, the item, the size, and the quantity of the **PO Line receiving** task that you just completed are shown.</span></span>

1. <span data-ttu-id="59d11-254">プットアウェイ作業を確認します。</span><span class="sxs-lookup"><span data-stu-id="59d11-254">Confirm the put-away work.</span></span>
1. <span data-ttu-id="59d11-255">ステップ 4 ~ 11 を、発注書明細行 2 に対して繰り返します。</span><span class="sxs-lookup"><span data-stu-id="59d11-255">Repeat the steps 4 through 11 for the purchase order line 2.</span></span> <span data-ttu-id="59d11-256">ただし、手順 8 では *1* の数量を指定します。</span><span class="sxs-lookup"><span data-stu-id="59d11-256">However, in step 8, specify a quantity of *1*.</span></span>

    <span data-ttu-id="59d11-257">作業 1 と同じ場所に新しいプットアウェイ作業 (作業 2) が作成されます。</span><span class="sxs-lookup"><span data-stu-id="59d11-257">New put-away work (Work 2) is created for the same location as Work 1.</span></span>

1. <span data-ttu-id="59d11-258">ステップ 4 ~ 11 を、発注書明細行 2 に対して再度繰り返します。</span><span class="sxs-lookup"><span data-stu-id="59d11-258">Repeat the steps 4 through 11 again for purchase order line 2.</span></span> <span data-ttu-id="59d11-259">ただし、手順 8 では *1* の残りの数量を指定します。</span><span class="sxs-lookup"><span data-stu-id="59d11-259">In step 8, specify the remaining quantity of *1*.</span></span>

    <span data-ttu-id="59d11-260">作業 1 および 2 と同じ場所に新しいプットアウェイ作業 (作業 3) が作成されます。</span><span class="sxs-lookup"><span data-stu-id="59d11-260">New put-away work (Work 3) is created for the same location as Work 1 and Work 2.</span></span> <span data-ttu-id="59d11-261">この挙動の仕組みとしては、*連結*場所ディレクティブ戦略が使用されており、*バルク\***場所プロファイル**設定の**許可された製品分析コードの混合**クイック タブにより、\*\*サイズ*\* バリアントを 1 つの場所に混在させることができるためです。</span><span class="sxs-lookup"><span data-stu-id="59d11-261">This behavior occurs because the *Consolidate* location directive strategy is used, and the **Allowed product dimension mixing** FastTab on the *Bulk* **Location profiles** setup allows the **Size** variant to be mixed on a location.</span></span>

1. <span data-ttu-id="59d11-262">ステップ 4 ~ 11 を、発注書明細行 3 に対して繰り返します。</span><span class="sxs-lookup"><span data-stu-id="59d11-262">Repeat the steps 4 through 11 for purchase order line 3.</span></span> <span data-ttu-id="59d11-263">手順 8 では、品目番号 *A0001* に *1* の数量を指定します。</span><span class="sxs-lookup"><span data-stu-id="59d11-263">In step 8, specify a quantity of *1* for item number *A0001*.</span></span>

    <span data-ttu-id="59d11-264">新しいプットアウェイ作業 (作業 4) は、発注書明細行 1 および 2 に使用される場所とは別の場所に作成されます。</span><span class="sxs-lookup"><span data-stu-id="59d11-264">New put-away work (Work 4) is created for a different location than the location that is used for purchase order lines 1 and 2.</span></span> <span data-ttu-id="59d11-265">この挙動は、場所プロファイルでは製品の混合が許可されていませんが、同じ製品マスターの分析コードの混合は許可されているために発生します。</span><span class="sxs-lookup"><span data-stu-id="59d11-265">This behavior occurs because the location profile doesn't allow for mixed products, but it does allow for mixed dimensions of the same product master.</span></span>

1. <span data-ttu-id="59d11-266">ページの上部にあるメニュー ボタン (ハンバーガー またはハンバーガー ボタンと呼ばれることもあります) を選択し、**キャンセル**を選択して、**発注書明細行の受取**を終了します。</span><span class="sxs-lookup"><span data-stu-id="59d11-266">Select the Menu button at the top of the page (sometimes referred to as the hamburger or the hamburger button), and then select **Cancel** to exit **PO Line receiving**.</span></span>

> [!TIP]
> <span data-ttu-id="59d11-267">このシナリオを繰り返すことができますが、今回は、*バルク\***場所プロファイル**の、**製品分析コードの混合を許可する**クイック タブの下にある\*\*サイズ*\* - *いいえ*を設定して、どの製品分析コードも混合しないようにします。</span><span class="sxs-lookup"><span data-stu-id="59d11-267">You can repeat this scenario, but this time, set **Size** - *No* under the **Allow product dimension mixing** FastTab on the *BULK* **Location profiles**, so that none of the product dimensions can be mixed.</span></span> <span data-ttu-id="59d11-268">この場合、発注書の受取の際に、各製品バリアントが新しい場所に配置されます。</span><span class="sxs-lookup"><span data-stu-id="59d11-268">In this case, when you receive the purchase order, each product variant will be put to a new location.</span></span>
