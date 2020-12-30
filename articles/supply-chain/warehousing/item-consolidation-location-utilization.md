---
title: 品目の連結 - 場所の使用率
description: このトピックでは、倉庫管理者が倉庫全体の場所の容積使用率を容易に確認およびフィルター処理できる機能について説明します。 管理者は品目の連結ページから直接場所を選択して在庫移動作業を作成することで、品目を連結することができるため、倉庫空間をより有効に活用できます。
author: Mirzaab
manager: tfehr
ms.date: 07/16/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: WHSPhysDimUOM, WHSMovementType, WHSItemConsolidationForm, WHSRFMenu, WHSRFMenuItem
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: mirzaab
ms.search.validFrom: 2020-07-16
ms.dyn365.ops.version: Release 10.0.7
ms.openlocfilehash: 6a328b20c1cfb2fc376ab4656c64cf585a5aa015
ms.sourcegitcommit: 827d77c638555396b32d36af5d22d1b61dafb0e8
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 10/16/2020
ms.locfileid: "4432288"
---
# <a name="item-consolidation---location-utilization"></a><span data-ttu-id="fb868-104">品目の連結 - 場所の使用率</span><span class="sxs-lookup"><span data-stu-id="fb868-104">Item consolidation - location utilization</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="fb868-105">このトピックでは、倉庫管理者が倉庫全体の場所の容積使用率を容易に確認およびフィルター処理できる機能について説明します。</span><span class="sxs-lookup"><span data-stu-id="fb868-105">This topic provides information about functionality that makes it easy for warehouse managers to view and filter the volumetric utilization of locations across the warehouse.</span></span> <span data-ttu-id="fb868-106">管理者は **品目の連結** ページから直接場所を選択して在庫移動作業を作成することで、品目を連結することができるため、倉庫空間をより有効に活用できます。</span><span class="sxs-lookup"><span data-stu-id="fb868-106">Managers can select locations and create inventory movement work directly from the **Item Consolidation** page to consolidate items and therefore make better use of warehouse space.</span></span>

## <a name="turn-on-the-features"></a><span data-ttu-id="fb868-107">機能をオンにする</span><span class="sxs-lookup"><span data-stu-id="fb868-107">Turn on the features</span></span>

<span data-ttu-id="fb868-108">このトピックで説明されている機能を使用するには、システムでこれらの機能を有効にする必要があります。</span><span class="sxs-lookup"><span data-stu-id="fb868-108">Before you can use the features that are described in this topic, you must turn them on in your system.</span></span> <span data-ttu-id="fb868-109">管理者は、[機能管理](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) ワークスペースを使用して、機能の状態を確認し、必要に応じて有効にすることができます。</span><span class="sxs-lookup"><span data-stu-id="fb868-109">Admins can use the [Feature management](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) workspace to check the status of the features and turn them on if they are required.</span></span> <span data-ttu-id="fb868-110">次の両方の機能を、記載されている順序で有効にします。</span><span class="sxs-lookup"><span data-stu-id="fb868-110">Turn on both the following features, in the order that they are listed in.</span></span> <span data-ttu-id="fb868-111">(両方の機能は、**倉庫管理** モジュール用です。)</span><span class="sxs-lookup"><span data-stu-id="fb868-111">(Both features are for the **Warehouse management** module.)</span></span>

1. <span data-ttu-id="fb868-112">倉庫の場所の状態</span><span class="sxs-lookup"><span data-stu-id="fb868-112">Warehouse location status</span></span>
2. <span data-ttu-id="fb868-113">品目の連結場所の使用率</span><span class="sxs-lookup"><span data-stu-id="fb868-113">Item consolidation location utilization</span></span>

## <a name="warehouse-location-status"></a><span data-ttu-id="fb868-114">倉庫の場所の状態</span><span class="sxs-lookup"><span data-stu-id="fb868-114">Warehouse location status</span></span>

<span data-ttu-id="fb868-115">*倉庫の場所の状態* 機能では、場所の現在の状態に関する追加情報を追跡するために、**場所** ページに 4 つの新しいフィールドを追加します。</span><span class="sxs-lookup"><span data-stu-id="fb868-115">The *Warehouse location status* feature adds four new fields to the **Locations** page to track additional information about the current state of the location:</span></span>

- <span data-ttu-id="fb868-116">**品目番号** – 場所に現在含まれている品目。</span><span class="sxs-lookup"><span data-stu-id="fb868-116">**Item number** – The item that is currently in the location.</span></span> <span data-ttu-id="fb868-117">場所に複数の品目が含まれる場合、このフィールドは空白になります。</span><span class="sxs-lookup"><span data-stu-id="fb868-117">If the location contains multiple items, this field will be blank.</span></span>
- <span data-ttu-id="fb868-118">**最終活動日時** – 場所に対して実行された最後の倉庫トランザクションのタイムスタンプ。</span><span class="sxs-lookup"><span data-stu-id="fb868-118">**Last activity date and time** – The timestamp of the last warehouse transaction that was performed against the location.</span></span>
- <span data-ttu-id="fb868-119">**エイジング日付** – 場所の在庫が倉庫に取り込まれた日付。</span><span class="sxs-lookup"><span data-stu-id="fb868-119">**Aging date** – The date when the inventory in the location was brought into the warehouse.</span></span> <span data-ttu-id="fb868-120">この日付は、ライセンス プレートのエイジング日付に基づいて計算されます。</span><span class="sxs-lookup"><span data-stu-id="fb868-120">This date is calculated based on the license plate aging date.</span></span> <span data-ttu-id="fb868-121">この日付は、ライセンス プレートで追跡されている場所では正確ですが、ライセンス プレートで追跡されていない場所では正確ではない場合があります。</span><span class="sxs-lookup"><span data-stu-id="fb868-121">Although this date is accurate for license plate–tracked locations, it might not be accurate for locations that aren't license plate–tracked.</span></span>
- <span data-ttu-id="fb868-122">**位置情報** – 場所のステータス。</span><span class="sxs-lookup"><span data-stu-id="fb868-122">**Location status** – The status of the location.</span></span> <span data-ttu-id="fb868-123">次の 4 つの値が使用可能です:</span><span class="sxs-lookup"><span data-stu-id="fb868-123">Four values are available:</span></span>

    - <span data-ttu-id="fb868-124">**未定義** – 場所プロファイルはステータスを追跡しません。</span><span class="sxs-lookup"><span data-stu-id="fb868-124">**Undetermined** – The location profile doesn't track status.</span></span> <span data-ttu-id="fb868-125">したがって、現在のステータスは不明になります。</span><span class="sxs-lookup"><span data-stu-id="fb868-125">Therefore, the current status is unknown.</span></span>
    - <span data-ttu-id="fb868-126">**空** – 現在、この場所に在庫はありません。</span><span class="sxs-lookup"><span data-stu-id="fb868-126">**Empty** – No inventory is currently in the location.</span></span>
    - <span data-ttu-id="fb868-127">**ピッキング** – 最後に空になった後、その場所に対して出庫トランザクションが実行されました。</span><span class="sxs-lookup"><span data-stu-id="fb868-127">**Picking** – Outbound transactions have been performed against the location after it was last empty.</span></span>
    - <span data-ttu-id="fb868-128">**ストレージ** – 場所が最後に空になってから、入庫トランザクションのみが実行されました。</span><span class="sxs-lookup"><span data-stu-id="fb868-128">**Storage** – Only inbound transactions have been performed since the location was last empty.</span></span>

<span data-ttu-id="fb868-129">これらのフィールドにより、倉庫管理者は倉庫内の場所のステータスの概要をより適切に把握できます。</span><span class="sxs-lookup"><span data-stu-id="fb868-129">These fields let warehouse managers get a better overview of the status of the locations in the warehouse.</span></span> <span data-ttu-id="fb868-130">また、より詳細なレポートとフィルター処理も可能です。</span><span class="sxs-lookup"><span data-stu-id="fb868-130">They also allow for more advanced reporting and filtering.</span></span>

## <a name="set-up-item-consolidation-and-location-utilization"></a><span data-ttu-id="fb868-131">品目の連結と場所の使用率を設定する</span><span class="sxs-lookup"><span data-stu-id="fb868-131">Set up item consolidation and location utilization</span></span>

<span data-ttu-id="fb868-132">このセクションでは、品目の連結と場所の使用率を使用するためにシステムを準備する方法について説明します。</span><span class="sxs-lookup"><span data-stu-id="fb868-132">This section describes how to prepare your system to use item consolidation and location utilization.</span></span> <span data-ttu-id="fb868-133">この手順では、標準デモ データのサンプル値を使用します。</span><span class="sxs-lookup"><span data-stu-id="fb868-133">The procedures use sample values from the standard demo data.</span></span> <span data-ttu-id="fb868-134">このトピックで後述する例のシナリオに従って作業する場合は、**USMF** 法人 (標準デモ データを含む) を選択し、このセクションで説明されている各レコードを作成します。</span><span class="sxs-lookup"><span data-stu-id="fb868-134">If you plan to work through the example scenario that is provided later in this topic, select the **USMF** legal entity (which contains the standard demo data), and create each record that is described in this section.</span></span> <span data-ttu-id="fb868-135">この例のシナリオを実行する予定がない場合、ここで提供される値は、機能を使用するために完了しなければならない設定の種類の例と考えることができます。</span><span class="sxs-lookup"><span data-stu-id="fb868-135">If you don't plan to work through the example scenario, the values that are provided here can be considered examples of the types of setup that you must complete to use the features.</span></span>

### <a name="released-product"></a><span data-ttu-id="fb868-136">リリースされた製品</span><span class="sxs-lookup"><span data-stu-id="fb868-136">Released product</span></span>

1. <span data-ttu-id="fb868-137">**製品管理情報 \> 製品 \> リリースされた製品** の順に移動します。</span><span class="sxs-lookup"><span data-stu-id="fb868-137">Go to **Product information management \> Products \> Released products**.</span></span>
1. <span data-ttu-id="fb868-138">**品目番号** フィールドで、*M9201* を選択し、詳細ページを開きます。</span><span class="sxs-lookup"><span data-stu-id="fb868-138">In the **Item number** field, select *M9201*, and open the details page.</span></span>
1. <span data-ttu-id="fb868-139">アクション ペインの **在庫の管理** タブの **倉庫** グループで、**現物分析コード** を選択します。</span><span class="sxs-lookup"><span data-stu-id="fb868-139">On the Action Pane, on the **Manage inventory** tab, in the **Warehouse** group, select **Physical dimensions**.</span></span>
1. <span data-ttu-id="fb868-140">**現物分析コード** ページのアクション ペインで、**新規** を選択します。</span><span class="sxs-lookup"><span data-stu-id="fb868-140">On the **Physical dimension** page, on the Action Pane, select **New**.</span></span>

    <span data-ttu-id="fb868-141">新しい行がグリッドに追加されます。</span><span class="sxs-lookup"><span data-stu-id="fb868-141">A new line is added to the grid.</span></span> <span data-ttu-id="fb868-142">**品目番号** フィールドは事前設定されています。</span><span class="sxs-lookup"><span data-stu-id="fb868-142">The **Item number** field is preset.</span></span>

1. <span data-ttu-id="fb868-143">**単位** フィールドで、*ea* を選択します。</span><span class="sxs-lookup"><span data-stu-id="fb868-143">In the **Unit** field, select *ea*.</span></span> <span data-ttu-id="fb868-144">行の残りのフィールドは自動的に設定されます。</span><span class="sxs-lookup"><span data-stu-id="fb868-144">The remaining fields on the line are automatically set.</span></span>
1. <span data-ttu-id="fb868-145">**保存** を選択して、ページを閉じます。</span><span class="sxs-lookup"><span data-stu-id="fb868-145">Select **Save**, and close the page.</span></span>

### <a name="location-profile"></a><span data-ttu-id="fb868-146">場所プロファイル</span><span class="sxs-lookup"><span data-stu-id="fb868-146">Location profile</span></span>

1. <span data-ttu-id="fb868-147">**倉庫管理 \> 設定 \> 倉庫 \> 場所プロファイル** に移動します。</span><span class="sxs-lookup"><span data-stu-id="fb868-147">Go to **Warehouse management \> Setup \> Warehouse \> Location profiles**.</span></span>
1. <span data-ttu-id="fb868-148">場所プロファイルの一覧で、**FLOOR-05** を選択します。</span><span class="sxs-lookup"><span data-stu-id="fb868-148">In the list of location profiles, select **FLOOR-05**.</span></span>
1. <span data-ttu-id="fb868-149">アクション ウィンドウで、**編集** を選択します。</span><span class="sxs-lookup"><span data-stu-id="fb868-149">On the Action Pane, select **Edit**.</span></span>
1. <span data-ttu-id="fb868-150">**一般** クイックタブで、次の両方のオプションが *はい* に設定されていることを確認します:</span><span class="sxs-lookup"><span data-stu-id="fb868-150">On the **General** FastTab, make sure that both the following options are set to *Yes*:</span></span>

    - <span data-ttu-id="fb868-151">場所の品目の有効化</span><span class="sxs-lookup"><span data-stu-id="fb868-151">Enable item in location</span></span>
    - <span data-ttu-id="fb868-152">場所の状態の有効化</span><span class="sxs-lookup"><span data-stu-id="fb868-152">Enable location status</span></span>

1. <span data-ttu-id="fb868-153">**保存** を選択します。</span><span class="sxs-lookup"><span data-stu-id="fb868-153">Select **Save**.</span></span>

    > [!IMPORTANT]
    > <span data-ttu-id="fb868-154">**場所で品目の有効化** と **場所の状態の有効化** オプションが既に *はい* に設定されている場合は、ステップ 10 の **分析コード** クイック タブの設定手順に進みます。</span><span class="sxs-lookup"><span data-stu-id="fb868-154">If the **Enable item in location** and **Enable location status** options were already set to *Yes*, skip ahead to the instructions for setting up the **Dimensions** FastTab in step 10.</span></span> <span data-ttu-id="fb868-155">オプションが *はい* に設定されていない場合は 、手動で設定した後で、**倉庫管理** モジュールの整合性チェックを実行する必要があります。</span><span class="sxs-lookup"><span data-stu-id="fb868-155">If the options weren't already set to *Yes*, you must run a consistency check for the **Warehouse management** module after you manually set them.</span></span> <span data-ttu-id="fb868-156">この場合は、次のステップに進みます。</span><span class="sxs-lookup"><span data-stu-id="fb868-156">In this case, continue to the next step.</span></span>

1. <span data-ttu-id="fb868-157">整合性チェックを実行するには、**システム管理 \> 定期処理のタスク \> データベース \> 整合性チェック** に移動します。</span><span class="sxs-lookup"><span data-stu-id="fb868-157">To run the consistency check, go to **System administration \> Periodic tasks \> Database \> Consistency check**.</span></span>
1. <span data-ttu-id="fb868-158">**整合性チェック** ダイアログ ボックスに、次の値を設定します:</span><span class="sxs-lookup"><span data-stu-id="fb868-158">In the **Consistency check** dialog box, set the following values:</span></span>

    - <span data-ttu-id="fb868-159">**モジュール:** *倉庫管理*</span><span class="sxs-lookup"><span data-stu-id="fb868-159">**Module:** *Warehouse management*</span></span>
    - <span data-ttu-id="fb868-160">**確認/修正:** *確認*</span><span class="sxs-lookup"><span data-stu-id="fb868-160">**Check/Fix:** *Check*</span></span>
    - <span data-ttu-id="fb868-161">**開始日:** このフィールドは空白のままにしておきます。</span><span class="sxs-lookup"><span data-stu-id="fb868-161">**From date:** Leave this field blank.</span></span>
    - <span data-ttu-id="fb868-162">**倉庫の場所の状態の整合性チェック:** このチェック ボックスをオンにします。</span><span class="sxs-lookup"><span data-stu-id="fb868-162">**Warehouse location status consistency check:** Select this check box.</span></span>

1. <span data-ttu-id="fb868-163">**OK** を選択します。</span><span class="sxs-lookup"><span data-stu-id="fb868-163">Select **OK**.</span></span>

    > [!TIP]
    > <span data-ttu-id="fb868-164">整合性チェックが完了すると、通知を受け取ります。</span><span class="sxs-lookup"><span data-stu-id="fb868-164">When the consistency check is completed, you receive a notification.</span></span> <span data-ttu-id="fb868-165">[アクション センター](../../fin-ops-core/fin-ops/get-started/user-interface-elements.md#notifications) を開いて、メッセージを表示します。</span><span class="sxs-lookup"><span data-stu-id="fb868-165">Open the [Action Center](../../fin-ops-core/fin-ops/get-started/user-interface-elements.md#notifications) to view the message.</span></span> <span data-ttu-id="fb868-166">**メッセージの詳細** を選択すると、詳細が表示されます。</span><span class="sxs-lookup"><span data-stu-id="fb868-166">Select **Message details** to view the details.</span></span>
    >
    > <span data-ttu-id="fb868-167">整合性チェックのメッセージに 「倉庫 XX の場所 XXXX について誤った場所の状態情報が検出されました」 と記載されている場合は、再度整合性チェックを実行する必要があります。</span><span class="sxs-lookup"><span data-stu-id="fb868-167">If the message for the consistency check states, "Incorrect location status information found for location XXXX in warehouse XX," you must run the consistency check again.</span></span> <span data-ttu-id="fb868-168">今回は、**確認/修正** フィールドを *エラーの修正* に設定します。</span><span class="sxs-lookup"><span data-stu-id="fb868-168">This time, set the **Check/Fix** field to *Fix error*.</span></span> <span data-ttu-id="fb868-169">メッセージを表示して、エラーが検出されなかったことを確認します。</span><span class="sxs-lookup"><span data-stu-id="fb868-169">View the messages to make sure that no errors were found.</span></span>

1. <span data-ttu-id="fb868-170">ここで、場所プロファイルの設定を完了する必要があります。</span><span class="sxs-lookup"><span data-stu-id="fb868-170">You must now finish setting up the location profile.</span></span> <span data-ttu-id="fb868-171">**倉庫管理 \> 設定 \> 倉庫 \> 場所プロファイル** に戻り、場所プロファイル **FLOOR-05** を選択し、アクション ペインで **編集** を選択します。</span><span class="sxs-lookup"><span data-stu-id="fb868-171">Go back to **Warehouse management \> Setup \> Warehouse \> Location profiles**, select location profile **FLOOR-05**, and then, on the Action Pane, select **Edit**.</span></span>
1. <span data-ttu-id="fb868-172">**分析コード** クイック タブで、次の値を設定します:</span><span class="sxs-lookup"><span data-stu-id="fb868-172">On the **Dimensions** FastTab, set the following values:</span></span>

    - <span data-ttu-id="fb868-173">**容積使用率の割合:** *100*</span><span class="sxs-lookup"><span data-stu-id="fb868-173">**Volume utilization percentage:** *100*</span></span>
    - <span data-ttu-id="fb868-174">**在庫場所に対して使用される容積測定方法:** *場所の容積を使用*</span><span class="sxs-lookup"><span data-stu-id="fb868-174">**Volumetric method used for inventory location:** *Use location volume*</span></span>
    - <span data-ttu-id="fb868-175">**実際の場所の高さ:** *10*</span><span class="sxs-lookup"><span data-stu-id="fb868-175">**Actual location height:** *10*</span></span>
    - <span data-ttu-id="fb868-176">**実際の場所の幅:** *10*</span><span class="sxs-lookup"><span data-stu-id="fb868-176">**Actual location width:** *10*</span></span>
    - <span data-ttu-id="fb868-177">**実際の場所の奥行き:** *10*</span><span class="sxs-lookup"><span data-stu-id="fb868-177">**Actual location depth:** *10*</span></span>
    - <span data-ttu-id="fb868-178">**最大重量:** *100*</span><span class="sxs-lookup"><span data-stu-id="fb868-178">**Maximum weight:** *100*</span></span>

1. <span data-ttu-id="fb868-179">**保存** を選択します。</span><span class="sxs-lookup"><span data-stu-id="fb868-179">Select **Save**.</span></span>

### <a name="mobile-device-menu-items"></a><span data-ttu-id="fb868-180">モバイル デバイスのメニュー品目</span><span class="sxs-lookup"><span data-stu-id="fb868-180">Mobile device menu items</span></span>

1. <span data-ttu-id="fb868-181">**倉庫管理 \> 設定 \> モバイル デバイス \> モバイル デバイスのメニュー品目** の順に移動します。</span><span class="sxs-lookup"><span data-stu-id="fb868-181">Go to **Warehouse management \> Setup \> Mobile device \> Mobile device menu items**.</span></span>
1. <span data-ttu-id="fb868-182">アクション ペインで、**新規** を選択して、並べ替え用のメニュー項目を作成します。</span><span class="sxs-lookup"><span data-stu-id="fb868-182">On the Action Pane, select **New** to create a menu item for sorting.</span></span>
1. <span data-ttu-id="fb868-183">ヘッダーで、次の値を設定します。</span><span class="sxs-lookup"><span data-stu-id="fb868-183">In the header, set the following values:</span></span>

    - <span data-ttu-id="fb868-184">**メニュー項目名:** *調整*</span><span class="sxs-lookup"><span data-stu-id="fb868-184">**Menu item name:** *Adjust In*</span></span>
    - <span data-ttu-id="fb868-185">**タイトル:** *調整*</span><span class="sxs-lookup"><span data-stu-id="fb868-185">**Title:** *Adjust In*</span></span>
    - <span data-ttu-id="fb868-186">**モード:** *作業*</span><span class="sxs-lookup"><span data-stu-id="fb868-186">**Mode:** *Work*</span></span>
    - <span data-ttu-id="fb868-187">**既存の作業を使用する :** *いいえ*</span><span class="sxs-lookup"><span data-stu-id="fb868-187">**Use existing work:** *No*</span></span>

1. <span data-ttu-id="fb868-188">**一般** クイック タブで、次の値を設定します。</span><span class="sxs-lookup"><span data-stu-id="fb868-188">On the **General** FastTab, set the following values:</span></span>

    - <span data-ttu-id="fb868-189">**作業作成プロセス:** *調整内*</span><span class="sxs-lookup"><span data-stu-id="fb868-189">**Work creation process:** *Adjustment in*</span></span>
    - <span data-ttu-id="fb868-190">**在庫調整タイプ:** *調整*</span><span class="sxs-lookup"><span data-stu-id="fb868-190">**Inventory adjustment types:** *Adjust in*</span></span>

1. <span data-ttu-id="fb868-191">**保存** を選択します。</span><span class="sxs-lookup"><span data-stu-id="fb868-191">Select **Save**.</span></span>

### <a name="mobile-device-menu"></a><span data-ttu-id="fb868-192">モバイル デバイスのメニュー</span><span class="sxs-lookup"><span data-stu-id="fb868-192">Mobile device menu</span></span>

1. <span data-ttu-id="fb868-193">**倉庫管理 \> 設定 \> モバイル デバイス \> モバイル デバイス メニュー** の順に移動します。</span><span class="sxs-lookup"><span data-stu-id="fb868-193">Go to **Warehouse management \> Setup \> Mobile device \> Mobile device menu**.</span></span>
1. <span data-ttu-id="fb868-194">メニューの一覧で **在庫** を選択します。</span><span class="sxs-lookup"><span data-stu-id="fb868-194">In the list of menus, select **Inventory**.</span></span>
1. <span data-ttu-id="fb868-195">アクション ウィンドウで、**編集** を選択します。</span><span class="sxs-lookup"><span data-stu-id="fb868-195">On the Action Pane, select **Edit**.</span></span>
1. <span data-ttu-id="fb868-196">**使用可能なメニューとメニュー項目** の一覧で、**調整** メニュー項目を検索して選択します。</span><span class="sxs-lookup"><span data-stu-id="fb868-196">In the **Available Menus And Menu Items** list, find and select the **Adjust In** menu item.</span></span>
1. <span data-ttu-id="fb868-197">右矢印ボタンを選択して、**調整** を **メニュー構造** の一覧に移動します。</span><span class="sxs-lookup"><span data-stu-id="fb868-197">Select the right arrow button to move **Adjust In** to the **Menu Structure** list.</span></span> <span data-ttu-id="fb868-198">このようにして、選択したメニューに新しいメニュー項目を追加します。</span><span class="sxs-lookup"><span data-stu-id="fb868-198">In this way, you add the new menu item to the selected menu.</span></span>
1. <span data-ttu-id="fb868-199">**保存** を選択します。</span><span class="sxs-lookup"><span data-stu-id="fb868-199">Select **Save**.</span></span>

### <a name="movement-types"></a><span data-ttu-id="fb868-200">移動タイプ</span><span class="sxs-lookup"><span data-stu-id="fb868-200">Movement types</span></span>

1. <span data-ttu-id="fb868-201">**倉庫管理 \> 設定 \> 在庫 \> 移動タイプ** に移動します。</span><span class="sxs-lookup"><span data-stu-id="fb868-201">Go to **Warehouse management \> Setup \> Inventory \> Movement types**.</span></span>
1. <span data-ttu-id="fb868-202">アクション ウィンドウで、**新規** を選択し、次の値を設定します。</span><span class="sxs-lookup"><span data-stu-id="fb868-202">On the Action Pane, select **New**, and then set the following values:</span></span>

    - <span data-ttu-id="fb868-203">**移動タイプ コード:** *連結*</span><span class="sxs-lookup"><span data-stu-id="fb868-203">**Movement type code:** *CONSOLIDATE*</span></span>
    - <span data-ttu-id="fb868-204">**説明:** *場所の連結*</span><span class="sxs-lookup"><span data-stu-id="fb868-204">**Description:** *Consolidate locations*</span></span>
    - <span data-ttu-id="fb868-205">**作業クラス ID:** *InvMov*</span><span class="sxs-lookup"><span data-stu-id="fb868-205">**Work class ID:** *InvMov*</span></span>

1. <span data-ttu-id="fb868-206">**保存** を選択します。</span><span class="sxs-lookup"><span data-stu-id="fb868-206">Select **Save**.</span></span>

## <a name="example-scenario"></a><span data-ttu-id="fb868-207">シナリオ例</span><span class="sxs-lookup"><span data-stu-id="fb868-207">Example scenario</span></span>

<span data-ttu-id="fb868-208">次のシナリオでは、モバイル デバイスの倉庫アプリを使用して、倉庫内の 2 箇所に在庫を *調整* します。</span><span class="sxs-lookup"><span data-stu-id="fb868-208">The following scenario uses the warehouse app on a mobile device to make an inventory *adjustment in* to two locations in the warehouse.</span></span>

### <a name="add-inventory-to-locations"></a><span data-ttu-id="fb868-209">場所に在庫を追加する</span><span class="sxs-lookup"><span data-stu-id="fb868-209">Add inventory to locations</span></span>

1. <span data-ttu-id="fb868-210">倉庫 *51* に設定されているユーザーとして、モバイル デバイスにサインインします。</span><span class="sxs-lookup"><span data-stu-id="fb868-210">Sign in to the mobile device as a user who is set up for warehouse *51*.</span></span>
1. <span data-ttu-id="fb868-211">**在庫 \> 調整** に移動します。</span><span class="sxs-lookup"><span data-stu-id="fb868-211">Go to **Inventory \> Adjust In**.</span></span>

    <span data-ttu-id="fb868-212">次に、最初の場所調整を入力します。</span><span class="sxs-lookup"><span data-stu-id="fb868-212">You will now enter the first location adjustment.</span></span>

1. <span data-ttu-id="fb868-213">**調整内** タスクで、在庫調整を行う場所を選択します。</span><span class="sxs-lookup"><span data-stu-id="fb868-213">In the **Adjustment in** task, select the location to make the inventory adjustment for.</span></span> <span data-ttu-id="fb868-214">**LOC** フィールドで、*LP-001* を選択します。</span><span class="sxs-lookup"><span data-stu-id="fb868-214">In the **LOC** field, select *LP-001*.</span></span>
1. <span data-ttu-id="fb868-215">場所を確認します。</span><span class="sxs-lookup"><span data-stu-id="fb868-215">Confirm the location.</span></span>
1. <span data-ttu-id="fb868-216">場所に追加される品目のライセンス プレート ID を作成します。</span><span class="sxs-lookup"><span data-stu-id="fb868-216">Create a license plate ID for the item that will be added to the location.</span></span> <span data-ttu-id="fb868-217">**LP** フィールドに、*LP00101* を入力します。</span><span class="sxs-lookup"><span data-stu-id="fb868-217">In the **LP** field, enter *LP00101*.</span></span>
1. <span data-ttu-id="fb868-218">ライセンス プレートを確認します。</span><span class="sxs-lookup"><span data-stu-id="fb868-218">Confirm the license plate.</span></span>
1. <span data-ttu-id="fb868-219">ライセンス プレートに追加される品目を入力します。</span><span class="sxs-lookup"><span data-stu-id="fb868-219">Enter the item that will be added to the license plate.</span></span> <span data-ttu-id="fb868-220">**ITEM** フィールドで、*M9201* を入力します。</span><span class="sxs-lookup"><span data-stu-id="fb868-220">In the **ITEM** field, enter *M9201*.</span></span>
1. <span data-ttu-id="fb868-221">品目を確定します。</span><span class="sxs-lookup"><span data-stu-id="fb868-221">Confirm the item.</span></span>
1. <span data-ttu-id="fb868-222">追加する品目の数量を入力します。</span><span class="sxs-lookup"><span data-stu-id="fb868-222">Enter the quantity of the item that will be added.</span></span> <span data-ttu-id="fb868-223">**数量** フィールドに、*10* と入力します。</span><span class="sxs-lookup"><span data-stu-id="fb868-223">In the **QTY** field, enter *10*.</span></span>
1. <span data-ttu-id="fb868-224">数量を確認します。</span><span class="sxs-lookup"><span data-stu-id="fb868-224">Confirm the quantity.</span></span>

    <span data-ttu-id="fb868-225">「作業が完了しました」というメッセージが表示されます。</span><span class="sxs-lookup"><span data-stu-id="fb868-225">You receive a "Work Completed" message.</span></span> <span data-ttu-id="fb868-226">次に、2 番目の場所調整を入力します。</span><span class="sxs-lookup"><span data-stu-id="fb868-226">You will now enter the second location adjustment.</span></span>

1. <span data-ttu-id="fb868-227">**調整内** タスクで、在庫調整を行う場所を選択します。</span><span class="sxs-lookup"><span data-stu-id="fb868-227">In the **Adjustment in** task, select the location to make the inventory adjustment for.</span></span> <span data-ttu-id="fb868-228">**LOC** フィールドで、*LP-002* を選択します。</span><span class="sxs-lookup"><span data-stu-id="fb868-228">In the **LOC** field, select *LP-002*.</span></span>
1. <span data-ttu-id="fb868-229">場所を確認します。</span><span class="sxs-lookup"><span data-stu-id="fb868-229">Confirm the location.</span></span>
1. <span data-ttu-id="fb868-230">場所に追加される品目のライセンス プレート ID を作成します。</span><span class="sxs-lookup"><span data-stu-id="fb868-230">Create a license plate ID for the item that will be added to the location.</span></span> <span data-ttu-id="fb868-231">**LP** フィールドに、*LP00201* を入力します。</span><span class="sxs-lookup"><span data-stu-id="fb868-231">In the **LP** field, enter *LP00201*.</span></span>
1. <span data-ttu-id="fb868-232">ライセンス プレートを確認します。</span><span class="sxs-lookup"><span data-stu-id="fb868-232">Confirm the license plate.</span></span>
1. <span data-ttu-id="fb868-233">ライセンス プレートに追加される品目を入力します。</span><span class="sxs-lookup"><span data-stu-id="fb868-233">Enter the item that will be added to the license plate.</span></span> <span data-ttu-id="fb868-234">**ITEM** フィールドで、*M9201* を入力します。</span><span class="sxs-lookup"><span data-stu-id="fb868-234">In the **ITEM** field, enter *M9201*.</span></span>
1. <span data-ttu-id="fb868-235">品目を確定します。</span><span class="sxs-lookup"><span data-stu-id="fb868-235">Confirm the item.</span></span>
1. <span data-ttu-id="fb868-236">追加する品目の数量を入力します。</span><span class="sxs-lookup"><span data-stu-id="fb868-236">Enter the quantity of the item that will be added.</span></span> <span data-ttu-id="fb868-237">**数量** フィールドに、*15* と入力します。</span><span class="sxs-lookup"><span data-stu-id="fb868-237">In the **QTY** field, enter *15*.</span></span>
1. <span data-ttu-id="fb868-238">数量を確認します。</span><span class="sxs-lookup"><span data-stu-id="fb868-238">Confirm the quantity.</span></span>

    <span data-ttu-id="fb868-239">「作業が完了しました」というメッセージが表示されます。</span><span class="sxs-lookup"><span data-stu-id="fb868-239">You receive a "Work Completed" message.</span></span>

1. <span data-ttu-id="fb868-240">メニュー ボタン (ハンバーガーまたはハンバーガー ボタンと呼ばれることもあります) を選択し、**キャンセル** を選択して、**調整内** タスクを終了します。</span><span class="sxs-lookup"><span data-stu-id="fb868-240">Select the Menu button (sometimes referred to as the hamburger or the hamburger button), and then select **Cancel** to exit the **Adjustment in** task.</span></span>

### <a name="consolidate-locations"></a><span data-ttu-id="fb868-241">場所の連結</span><span class="sxs-lookup"><span data-stu-id="fb868-241">Consolidate locations</span></span>

1. <span data-ttu-id="fb868-242">**倉庫管理 \> 定期処理タスク \> 品目の連結** に移動します。</span><span class="sxs-lookup"><span data-stu-id="fb868-242">Go to **Warehouse management \> Periodic tasks \> Item consolidation**.</span></span>
1. <span data-ttu-id="fb868-243">ヘッダーで、連結を行う倉庫を選択します。</span><span class="sxs-lookup"><span data-stu-id="fb868-243">In the header, select a warehouse to do the consolidation for.</span></span> <span data-ttu-id="fb868-244">**倉庫** フィールドに、*51* と入力します。</span><span class="sxs-lookup"><span data-stu-id="fb868-244">In the **Warehouse** field, enter *51*.</span></span>

    <span data-ttu-id="fb868-245">品目 *M9201* が調整された場所ごとに、レコードが表示されます。</span><span class="sxs-lookup"><span data-stu-id="fb868-245">A record is shown for each location where item *M9201* was adjusted.</span></span> <span data-ttu-id="fb868-246">**使用率の割合** 列には、各場所の容積使用率が表示されます。</span><span class="sxs-lookup"><span data-stu-id="fb868-246">The **Utilization percentage** column shows the volumetric utilization of each location.</span></span>

1. <span data-ttu-id="fb868-247">在庫を連結するには、連結する必要のあるすべての場所を選択し、アクション ペインで **在庫の連結** を選択します。</span><span class="sxs-lookup"><span data-stu-id="fb868-247">To consolidate inventory, select all the locations that must be consolidated, and then, on the Action Pane, select **Consolidate Inventory**.</span></span>
1. <span data-ttu-id="fb868-248">**在庫の連結** ダイアログ ボックスで、在庫移動のための作業を作成するために使用する場所と移動タイプを指定します。</span><span class="sxs-lookup"><span data-stu-id="fb868-248">In the **Consolidate inventory** dialog box, specify the location and movement type that should be used to create the work for inventory movement.</span></span> <span data-ttu-id="fb868-249">次の値を設定します。</span><span class="sxs-lookup"><span data-stu-id="fb868-249">Set the following values:</span></span>

    - <span data-ttu-id="fb868-250">**場所:** *LP-001*</span><span class="sxs-lookup"><span data-stu-id="fb868-250">**Location:** *LP-001*</span></span>
    - <span data-ttu-id="fb868-251">**移動タイプ コード:** *連結*</span><span class="sxs-lookup"><span data-stu-id="fb868-251">**Movement type code:** *CONSOLIDATE*</span></span>

1. <span data-ttu-id="fb868-252">**OK** を選択します。</span><span class="sxs-lookup"><span data-stu-id="fb868-252">Select **OK**.</span></span>
1. <span data-ttu-id="fb868-253">作成された移動作業を示す情報メッセージが表示されます。</span><span class="sxs-lookup"><span data-stu-id="fb868-253">You receive an informational message that shows the movement work that was created.</span></span> <span data-ttu-id="fb868-254">移動作業 ID をメモします。</span><span class="sxs-lookup"><span data-stu-id="fb868-254">Make a note of the movement work ID.</span></span>

### <a name="view-movement-work"></a><span data-ttu-id="fb868-255">移動作業の表示</span><span class="sxs-lookup"><span data-stu-id="fb868-255">View movement work</span></span>

1. <span data-ttu-id="fb868-256">**倉庫管理 \> 作業 \> 作業の詳細** の順に移動します。</span><span class="sxs-lookup"><span data-stu-id="fb868-256">Go to **Warehouse management \> Work \> Work details**.</span></span>
1. <span data-ttu-id="fb868-257">作成された作業を表示します。</span><span class="sxs-lookup"><span data-stu-id="fb868-257">View the work that was created.</span></span> <span data-ttu-id="fb868-258">在庫連結の移動作業 ID を使用して、作業グリッドをフィルター処理または検索します。</span><span class="sxs-lookup"><span data-stu-id="fb868-258">Use the movement work ID from the inventory consolidation to filter or search the work grid.</span></span>

    <span data-ttu-id="fb868-259">このシナリオでは、在庫のある既存の場所を在庫の連結場所として使用しました。</span><span class="sxs-lookup"><span data-stu-id="fb868-259">In this scenario, an existing location that had inventory was used as the inventory consolidation location.</span></span> <span data-ttu-id="fb868-260">したがって、1 つの作業 ID しか作成されませんでした。</span><span class="sxs-lookup"><span data-stu-id="fb868-260">Therefore, only one work ID was created.</span></span>

    > [!NOTE]
   > <span data-ttu-id="fb868-261">システムは、完了する必要がある各移動に対して、1 つの作業 ID を作成します。</span><span class="sxs-lookup"><span data-stu-id="fb868-261">The system creates one work ID for each move that must be completed.</span></span> <span data-ttu-id="fb868-262">在庫が既に含まれている場所を指定した場合、1 つの作業 ID のみが作成されます。</span><span class="sxs-lookup"><span data-stu-id="fb868-262">If you specify a location that already contains inventory, only one work ID is created.</span></span> <span data-ttu-id="fb868-263">新しい場所を指定した場合は、2 つの作業 ID が作成されます。</span><span class="sxs-lookup"><span data-stu-id="fb868-263">If you specify a new location, two work IDs are created.</span></span>
