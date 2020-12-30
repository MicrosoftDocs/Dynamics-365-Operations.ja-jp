---
title: アウトバウンド ソーティング
description: このトピックは、アウトバウンド ソーティングに関する情報を提供します。 この機能を使用すると、小さなコンテナーの処理が容易になり、倉庫の従業員がトラックのパレット容量をより効率的に計画および整理できるようになります。
author: Mirzaab
manager: tfehr
ms.date: 07/15/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: WHSPack, WHSOutboundSortTemplate, WHSOutboundSortPositionAssignments, WHSLocationType, WHSLoactionProfile
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: mirzaab
ms.search.validFrom: 2020-07-15
ms.dyn365.ops.version: Release 10.0.9
ms.openlocfilehash: 84c4ec83ed16762e6c3c1a22425cf60e5b3ae8da
ms.sourcegitcommit: 827d77c638555396b32d36af5d22d1b61dafb0e8
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 10/16/2020
ms.locfileid: "4432383"
---
# <a name="outbound-sorting"></a><span data-ttu-id="eafbb-104">アウトバウンド ソーティング</span><span class="sxs-lookup"><span data-stu-id="eafbb-104">Outbound sorting</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="eafbb-105">この機能を使用すると、小さなコンテナーの処理が容易になり、倉庫の従業員がトラックのパレット容量をより効率的に計画および整理できるようになります。</span><span class="sxs-lookup"><span data-stu-id="eafbb-105">This functionality makes it easier to handle small containers and helps warehouse workers better plan and organize pallet capacity in the truck.</span></span> <span data-ttu-id="eafbb-106">アウトバウンド ソーティングを使用すると、梱包コンテナーを梱包ステーションに置いた後に、梱包コンテナーを正しいパレットにソートすることができます。</span><span class="sxs-lookup"><span data-stu-id="eafbb-106">When you use outbound sorting, you can sort packed containers to the correct pallet after they have been at a packing station.</span></span> <span data-ttu-id="eafbb-107">また、梱包階層を構築することもできます。</span><span class="sxs-lookup"><span data-stu-id="eafbb-107">You can also build a packing hierarchy.</span></span>

<span data-ttu-id="eafbb-108">この機能を使用すると、梱包機能を通じて梱包されているコンテナーからパレットを構築できます。</span><span class="sxs-lookup"><span data-stu-id="eafbb-108">This functionality lets you build pallets from containers that are packed through the packing functionality.</span></span> <span data-ttu-id="eafbb-109">このコンテナーは、元の梱包フローに含まれているため、最終出荷場所には送られません。</span><span class="sxs-lookup"><span data-stu-id="eafbb-109">The container isn't sent to the final shipping location as it is in the original packing flow.</span></span> <span data-ttu-id="eafbb-110">代わりに、作業者はコンテナーを閉じて、ソート タイプの場所に移動することができます。</span><span class="sxs-lookup"><span data-stu-id="eafbb-110">Instead, workers can close the container and move it to a sort type location.</span></span> <span data-ttu-id="eafbb-111">これにより、コンテナーをソートして配置でき、そのそれぞれがライセンス プレート (LP) を保持します。</span><span class="sxs-lookup"><span data-stu-id="eafbb-111">They can then sort containers to positions, each of which has a license plate (LP).</span></span> <span data-ttu-id="eafbb-112">コンテナーがソートされたら、作業を作成して、場所のディレクティブまたは独自の要件に基づいて、LP 全体を最終的な出荷ドックまたはステージの場所に送ることができます。</span><span class="sxs-lookup"><span data-stu-id="eafbb-112">After the containers have been sorted, work can be created to send the whole LP to the final shipping dock or stage locations, based on location directives or your own requirements.</span></span> <span data-ttu-id="eafbb-113">さらに、ソート位置を閉じるアクションおこなうと、即座位に在庫を最終的な出荷場所に移動し、注文をピッキングすることができます。</span><span class="sxs-lookup"><span data-stu-id="eafbb-113">Additionally, the action of closing of the sort position can immediately move the inventory to the final shipping location and pick it to the order.</span></span>

## <a name="turn-on-the-outbound-sorting-feature"></a><span data-ttu-id="eafbb-114">アウトバウンド ソーティング機能を有効にする</span><span class="sxs-lookup"><span data-stu-id="eafbb-114">Turn on the Outbound sorting feature</span></span>

<span data-ttu-id="eafbb-115">この機能を使用するには、システム上で有効化する必要があります。</span><span class="sxs-lookup"><span data-stu-id="eafbb-115">Before you can use the feature, it must be turned on in your system.</span></span> <span data-ttu-id="eafbb-116">管理者は、[機能の管理](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) ワークスペースを使用して、機能の状態を確認し、必要に応じて有効にすることができます。</span><span class="sxs-lookup"><span data-stu-id="eafbb-116">Admins can use the [Feature management](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) workspace to check the status of the feature and turn it on if it's required.</span></span> <span data-ttu-id="eafbb-117">この機能は、次のようにして表示されます。</span><span class="sxs-lookup"><span data-stu-id="eafbb-117">There, the feature is listed in the following way:</span></span>

- <span data-ttu-id="eafbb-118">**モジュール:** *倉庫管理*</span><span class="sxs-lookup"><span data-stu-id="eafbb-118">**Module:** *Warehouse management*</span></span>
- <span data-ttu-id="eafbb-119">**機能名:** *アウトバウンド ソーティング*</span><span class="sxs-lookup"><span data-stu-id="eafbb-119">**Feature name:** *Outbound sorting*</span></span>

## <a name="setup"></a><span data-ttu-id="eafbb-120">セットアップ</span><span class="sxs-lookup"><span data-stu-id="eafbb-120">Setup</span></span>

<span data-ttu-id="eafbb-121">このシナリオでは、標準の **USMF** デモ データと倉庫 *62* を使用する必要があります。</span><span class="sxs-lookup"><span data-stu-id="eafbb-121">For this scenario, you must use standard **USMF** demo data and warehouse *62*.</span></span> <span data-ttu-id="eafbb-122">また、次のサブセクションで説明する設定を完了する必要があります。</span><span class="sxs-lookup"><span data-stu-id="eafbb-122">You must also complete the setup that is described in the following subsections.</span></span>

### <a name="set-up-a-wave-template"></a><span data-ttu-id="eafbb-123">ウェーブ テンプレートの設定</span><span class="sxs-lookup"><span data-stu-id="eafbb-123">Set up a wave template</span></span>

<span data-ttu-id="eafbb-124">この設定は、明細行がその倉庫にリリースされると自動的にウェーブをプロセス処理し作業を作成します。</span><span class="sxs-lookup"><span data-stu-id="eafbb-124">This setup automatically processes the wave and creates work when a line is released to the warehouse.</span></span>

1. <span data-ttu-id="eafbb-125">**倉庫管理 \> 設定 \> ウェーブ \> ウェーブ テンプレート** の順に移動します。</span><span class="sxs-lookup"><span data-stu-id="eafbb-125">Go to **Warehouse management \> Setup \> Waves \> Wave templates**.</span></span>
1. <span data-ttu-id="eafbb-126">テンプレート リストで、**倉庫 62** を選択します。</span><span class="sxs-lookup"><span data-stu-id="eafbb-126">In the template list, select **Warehouse 62**.</span></span>
1. <span data-ttu-id="eafbb-127">**一般** クイック タブで、**倉庫へのリリース時点でウェーブを処理する** オプションが *はい* に設定されていることを確認します。</span><span class="sxs-lookup"><span data-stu-id="eafbb-127">On the **General** FastTab, make sure that the **Process wave at release to warehouse** option is set to *Yes*.</span></span>

### <a name="set-up-a-worker"></a><span data-ttu-id="eafbb-128">作業者の設定</span><span class="sxs-lookup"><span data-stu-id="eafbb-128">Set up a worker</span></span>

<span data-ttu-id="eafbb-129">梱包ステーションは 1 つの場所と見なされます。</span><span class="sxs-lookup"><span data-stu-id="eafbb-129">The packing station is considered a location.</span></span> <span data-ttu-id="eafbb-130">梱包ステーションにログインする倉庫作業者は、特定の梱包場所で計画されている出荷とコンテナーのみを表示して作業します。</span><span class="sxs-lookup"><span data-stu-id="eafbb-130">Warehouse workers who sign in at the packing station see and work on only shipments and containers that are planned at that specific packing location.</span></span> <span data-ttu-id="eafbb-131">Microsoft Dynamics 365 にサインインするユーザーは、倉庫管理で作業者として設定されていなければなりません。</span><span class="sxs-lookup"><span data-stu-id="eafbb-131">A user who signs in to Microsoft Dynamics 365 must be set up as a worker in Warehouse management.</span></span> <span data-ttu-id="eafbb-132">ユーザーの名前が作業ユーザーの一覧に表示されない場合は、次の手順で追加します。</span><span class="sxs-lookup"><span data-stu-id="eafbb-132">If the user's name doesn't appear in the list of work users, use the following procedure to add it.</span></span>

> [!NOTE]
> <span data-ttu-id="eafbb-133">次の手順では、ユーザーが既にシステム内に存在し、**Human Resources** モジュールで従業員または作業者として関連付けられていると推定します。</span><span class="sxs-lookup"><span data-stu-id="eafbb-133">These steps assume that the user already exists in the system and has been associated as an employee or worker in the **Human Resources** module.</span></span>

1. <span data-ttu-id="eafbb-134">**倉庫管理 \> 設定 \> 作業者** の順に移動します。</span><span class="sxs-lookup"><span data-stu-id="eafbb-134">Go to **Warehouse management \> Setup \> Worker**.</span></span>
1. <span data-ttu-id="eafbb-135">**新規** を選択します。</span><span class="sxs-lookup"><span data-stu-id="eafbb-135">Select **New**.</span></span>
1. <span data-ttu-id="eafbb-136">**作業者** フィールドで、従業員の一覧から対象ユーザーを選択します。</span><span class="sxs-lookup"><span data-stu-id="eafbb-136">In the **Worker** field, select the target user in the list of employees.</span></span>
1. <span data-ttu-id="eafbb-137">**選択** を選択します。</span><span class="sxs-lookup"><span data-stu-id="eafbb-137">Select **Select**.</span></span>
1. <span data-ttu-id="eafbb-138">アクション ウィンドウで、**保存** を選択します。</span><span class="sxs-lookup"><span data-stu-id="eafbb-138">On the Action Pane, select **Save**.</span></span>
1. <span data-ttu-id="eafbb-139">**ユーザー** クイックタブで、**新規** を選択して、モバイル デバイス アカウントを作成し、次の値を設定します。</span><span class="sxs-lookup"><span data-stu-id="eafbb-139">On the **Users** FastTab, select **New** to create a mobile device account, and set the following values for it:</span></span>

    - <span data-ttu-id="eafbb-140">**ユーザー ID:** 一意の ID を入力します。</span><span class="sxs-lookup"><span data-stu-id="eafbb-140">**User ID:** Enter a unique ID.</span></span>
    - <span data-ttu-id="eafbb-141">**ユーザー名:** ID の名前を入力します。</span><span class="sxs-lookup"><span data-stu-id="eafbb-141">**User name:** Enter a name for the ID.</span></span>
    - <span data-ttu-id="eafbb-142">**既定の倉庫:** *62*</span><span class="sxs-lookup"><span data-stu-id="eafbb-142">**Default warehouse:** *62*</span></span>
    - <span data-ttu-id="eafbb-143">**メニュー名:** *メイン*</span><span class="sxs-lookup"><span data-stu-id="eafbb-143">**Menu name:** *Main*</span></span>

1. <span data-ttu-id="eafbb-144">アクション ウィンドウで、**保存** を選択します。</span><span class="sxs-lookup"><span data-stu-id="eafbb-144">On the Action Pane, select **Save**.</span></span>
1. <span data-ttu-id="eafbb-145">**パスワードの設定** ダイアログ ボックスが表示され、ユーザーがモバイル アプリにログインするために使用できる簡易パスワードを作成できます。</span><span class="sxs-lookup"><span data-stu-id="eafbb-145">The **Set password** dialog box appears, where you can create a simple password that the user can use to sign in to the mobile app.</span></span> <span data-ttu-id="eafbb-146">次の値を設定します。</span><span class="sxs-lookup"><span data-stu-id="eafbb-146">Set the following values:</span></span>

    - <span data-ttu-id="eafbb-147">**パスワード:** 簡易パスワードを入力します。</span><span class="sxs-lookup"><span data-stu-id="eafbb-147">**Password:** Enter a simple password.</span></span>
    - <span data-ttu-id="eafbb-148">**パスワードの確認:** 同じパスワードを再度入力します。</span><span class="sxs-lookup"><span data-stu-id="eafbb-148">**Confirm password:** Enter the same password again.</span></span>

1. <span data-ttu-id="eafbb-149">**パスワードの設定** を選択します。</span><span class="sxs-lookup"><span data-stu-id="eafbb-149">Select **Set password**.</span></span>

    <span data-ttu-id="eafbb-150">作成したユーザーに対してパスワードが設定されていることを知らせる通知がアクション センターに表示されます。</span><span class="sxs-lookup"><span data-stu-id="eafbb-150">A notification in the Action Center informs you that the password has been set for the user that you created.</span></span>

### <a name="create-a-location-type"></a><span data-ttu-id="eafbb-151">場所タイプの作成</span><span class="sxs-lookup"><span data-stu-id="eafbb-151">Create a location type</span></span>

1. <span data-ttu-id="eafbb-152">**倉庫管理 \> 設定 \> 倉庫 \> 場所タイプ** の順に移動します。</span><span class="sxs-lookup"><span data-stu-id="eafbb-152">Go to **Warehouse management \> Setup \> Warehouse \> Location types**.</span></span>
1. <span data-ttu-id="eafbb-153">アクション ウィンドウで、場所タイプを作成するために **新規** を選択して、次の値を設定します。</span><span class="sxs-lookup"><span data-stu-id="eafbb-153">On the Action Pane, select **New** to create a location type, and set the following values for it:</span></span>

    - <span data-ttu-id="eafbb-154">**場所タイプ:** *SORT*</span><span class="sxs-lookup"><span data-stu-id="eafbb-154">**Location type:** *SORT*</span></span>
    - <span data-ttu-id="eafbb-155">**説明:** *ソート*</span><span class="sxs-lookup"><span data-stu-id="eafbb-155">**Description:** *Sort*</span></span>

1. <span data-ttu-id="eafbb-156">アクション ウィンドウで、**保存** を選択します。</span><span class="sxs-lookup"><span data-stu-id="eafbb-156">On the Action Pane, select **Save**.</span></span>

### <a name="set-up-warehouse-management-parameters"></a><span data-ttu-id="eafbb-157">倉庫管理パラメーターの設定</span><span class="sxs-lookup"><span data-stu-id="eafbb-157">Set up Warehouse management parameters</span></span>

1. <span data-ttu-id="eafbb-158">**倉庫管理 \> 設定 \> 倉庫管理パラメーター** の順に移動します。</span><span class="sxs-lookup"><span data-stu-id="eafbb-158">Go to **Warehouse management \> Setup \> Warehouse management parameters**.</span></span>
1. <span data-ttu-id="eafbb-159">**全般** タブの **場所タイプ** クイック タブで、**ソーティング場所のタイプ** フィールドを *SORT* に設定します。</span><span class="sxs-lookup"><span data-stu-id="eafbb-159">On the **General** tab, on the **Location types** FastTab, set the **Sorting location type** field to *SORT*.</span></span>
1. <span data-ttu-id="eafbb-160">アクション ウィンドウで、**保存** を選択します。</span><span class="sxs-lookup"><span data-stu-id="eafbb-160">On the Action Pane, select **Save**.</span></span>

### <a name="set-up-a-location-profile"></a><span data-ttu-id="eafbb-161">場所プロファイルの設定</span><span class="sxs-lookup"><span data-stu-id="eafbb-161">Set up a location profile</span></span>

1. <span data-ttu-id="eafbb-162">**倉庫管理 \> 設定 \> 倉庫 \> 場所プロファイル** に移動します。</span><span class="sxs-lookup"><span data-stu-id="eafbb-162">Go to **Warehouse management \> Setup \> Warehouse \> Location profiles**.</span></span>
1. <span data-ttu-id="eafbb-163">アクション ウィンドウで、**新規** を選択します。</span><span class="sxs-lookup"><span data-stu-id="eafbb-163">On the Action Pane, select **New**.</span></span>
1. <span data-ttu-id="eafbb-164">ヘッダーで、次の値を設定します。</span><span class="sxs-lookup"><span data-stu-id="eafbb-164">In the header, set the following values:</span></span>

    - <span data-ttu-id="eafbb-165">**場所プロファイル ID:** *ソーティング*</span><span class="sxs-lookup"><span data-stu-id="eafbb-165">**Location profile ID:** *Sorting*</span></span>
    - <span data-ttu-id="eafbb-166">**名前:** *ソーティング*</span><span class="sxs-lookup"><span data-stu-id="eafbb-166">**Name:** *Sorting*</span></span>

1. <span data-ttu-id="eafbb-167">**一般** クイック タブで、次の値を設定します。</span><span class="sxs-lookup"><span data-stu-id="eafbb-167">On the **General** FastTab, set the following values:</span></span>

    - <span data-ttu-id="eafbb-168">**場所の形式:** *ASRB* (通路-ラック-棚-トレイ)</span><span class="sxs-lookup"><span data-stu-id="eafbb-168">**Location format:** *ASRB* (Aisle-Rack-Shelf-Bin)</span></span>
    - <span data-ttu-id="eafbb-169">**場所タイプ:** *SORT*</span><span class="sxs-lookup"><span data-stu-id="eafbb-169">**Location type:** *SORT*</span></span>
    - <span data-ttu-id="eafbb-170">**ライセンス プレート追跡を使用:** *はい*</span><span class="sxs-lookup"><span data-stu-id="eafbb-170">**Use license plate tracking:** *Yes*</span></span>
    - <span data-ttu-id="eafbb-171">**混合品目を許可** *はい* (このオプションを *はい* に設定する場合、**在庫バッチの混在を許可する** オプションが自動的に *はい* に設定され、個別に変更することはできなくなります。)</span><span class="sxs-lookup"><span data-stu-id="eafbb-171">**Allow mixed items:** *Yes* (When you set this option to *Yes*, the **Allow mixed inventory batches** option is automatically set to *Yes* and can't be changed independently.)</span></span>

1. <span data-ttu-id="eafbb-172">**保存** を選択します。</span><span class="sxs-lookup"><span data-stu-id="eafbb-172">Select **Save**.</span></span>

### <a name="set-up-a-location"></a><span data-ttu-id="eafbb-173">場所の設定</span><span class="sxs-lookup"><span data-stu-id="eafbb-173">Set up a location</span></span>

1. <span data-ttu-id="eafbb-174">**倉庫管理 \> 設定 \> 倉庫 \> 場所** に移動します。</span><span class="sxs-lookup"><span data-stu-id="eafbb-174">Go to **Warehouse management \> Setup \> Warehouse \> Locations**.</span></span>
1. <span data-ttu-id="eafbb-175">ヘッダーで、**場所のチェック ディジットを生成する** チェック ボックスをオフにします。</span><span class="sxs-lookup"><span data-stu-id="eafbb-175">In the header, clear the **Generate check digits for location** check box.</span></span>
1. <span data-ttu-id="eafbb-176">アクション ウィンドウで、**新規** を選択して場所タイプを作成し、次の値を設定します。</span><span class="sxs-lookup"><span data-stu-id="eafbb-176">On the Action Pane, select **New** to create a location, and set the following values for it:</span></span>

    - <span data-ttu-id="eafbb-177">**倉庫:** *62*</span><span class="sxs-lookup"><span data-stu-id="eafbb-177">**Warehouse:** *62*</span></span>
    - <span data-ttu-id="eafbb-178">**場所:** *SORT*</span><span class="sxs-lookup"><span data-stu-id="eafbb-178">**Location:** *SORT*</span></span>
    - <span data-ttu-id="eafbb-179">**場所プロファイル ID:** *SORTING*</span><span class="sxs-lookup"><span data-stu-id="eafbb-179">**Location profile ID:** *SORTING*</span></span>

1. <span data-ttu-id="eafbb-180">**保存** を選択します。</span><span class="sxs-lookup"><span data-stu-id="eafbb-180">Select **Save**.</span></span>

### <a name="set-up-an-outbound-sorting-template"></a><span data-ttu-id="eafbb-181">アウトバウンド ソーティング テンプレートの設定</span><span class="sxs-lookup"><span data-stu-id="eafbb-181">Set up an outbound sorting template</span></span>

<span data-ttu-id="eafbb-182">アウトバウンド ソーティング テンプレートでは、作業をソート場所から作成するかどうか、ソーティングを手動で行うか自動的に行うかを指定します。</span><span class="sxs-lookup"><span data-stu-id="eafbb-182">The outbound sorting template determines whether work is created out of the sort location, and whether sorting is done manually or automatically.</span></span>

<span data-ttu-id="eafbb-183">このシナリオでは、アウトバウンド ソーティング テンプレートを作成して、梱包ステーションの後にパレットを構築します。</span><span class="sxs-lookup"><span data-stu-id="eafbb-183">For this scenario, you will create an outbound sorting template to build pallets after the packing station.</span></span>

1. <span data-ttu-id="eafbb-184">**倉庫管理 \> 設定 \> 梱包 \> アウトバウンド ソーティング テンプレート** の順に移動します。</span><span class="sxs-lookup"><span data-stu-id="eafbb-184">Go to **Warehouse Management \> Setup \> Packing \> Outbound sorting template**.</span></span>
1. <span data-ttu-id="eafbb-185">アクション ウィンドウで、**新規** を選択します。</span><span class="sxs-lookup"><span data-stu-id="eafbb-185">On the Action Pane, select **New**.</span></span>
1. <span data-ttu-id="eafbb-186">新規テンプレートのヘッダーで、次の値を設定します。</span><span class="sxs-lookup"><span data-stu-id="eafbb-186">In the header of the new template, set the following values:</span></span>

    - <span data-ttu-id="eafbb-187">**アウトバウンド ソーティング テンプレート ID:** *AutoWork*</span><span class="sxs-lookup"><span data-stu-id="eafbb-187">**Outbound sorting template ID:** *AutoWork*</span></span>
    - <span data-ttu-id="eafbb-188">**説明:** *自動作業の作成*</span><span class="sxs-lookup"><span data-stu-id="eafbb-188">**Description:** *Auto Work Creation*</span></span>
    - <span data-ttu-id="eafbb-189">**アウトバウンド ソーティング テンプレートの種類:** *コンテナー*</span><span class="sxs-lookup"><span data-stu-id="eafbb-189">**Outbound sorting template type:** *Container*</span></span>
    - <span data-ttu-id="eafbb-190">**倉庫:** *62*</span><span class="sxs-lookup"><span data-stu-id="eafbb-190">**Warehouse:** *62*</span></span>
    - <span data-ttu-id="eafbb-191">**場所:** *SORT*</span><span class="sxs-lookup"><span data-stu-id="eafbb-191">**Location:** *SORT*</span></span>

1. <span data-ttu-id="eafbb-192">**一般** クイック タブで、次の値を設定します。</span><span class="sxs-lookup"><span data-stu-id="eafbb-192">On the **General** FastTab, set the following values:</span></span>

    - <span data-ttu-id="eafbb-193">**ソートの検証:** *位置スキャン*</span><span class="sxs-lookup"><span data-stu-id="eafbb-193">**Sort verification:** *Position scan*</span></span>
    - <span data-ttu-id="eafbb-194">**位置がクローズしたら作業を作成する:** *はい*</span><span class="sxs-lookup"><span data-stu-id="eafbb-194">**Create work on position close:** *Yes*</span></span>

        <span data-ttu-id="eafbb-195">このオプションを *はい* に設定すると、その位置がクローズしたときに、最終出荷場所に在庫を移動する作業が作成されます。</span><span class="sxs-lookup"><span data-stu-id="eafbb-195">If this option is set to *Yes*, when the position is closed, work will be created to move inventory to the final shipping location.</span></span> <span data-ttu-id="eafbb-196">これを *いいえ* に設定すると、その位置がクローズすると、直ちに在庫が注文に対してピッキングされます。</span><span class="sxs-lookup"><span data-stu-id="eafbb-196">If it's set to *No*, inventory will immediately be picked to the order when the position is closed.</span></span>

    - <span data-ttu-id="eafbb-197">**位置の割り当て:** *自動*</span><span class="sxs-lookup"><span data-stu-id="eafbb-197">**Position assignment:** *Automatic*</span></span>

        <span data-ttu-id="eafbb-198">このフィールドが *手動* に設定されている場合、ユーザーは常に、在庫がソートされるべき位置を指定する必要があります。</span><span class="sxs-lookup"><span data-stu-id="eafbb-198">If this field is set to *Manual*, the user must always indicate which position the inventory should be sorted to.</span></span> <span data-ttu-id="eafbb-199">これが *自動* に設定されている場合、システムは可能な場合はソート テンプレートの分割に基づいて自動的に在庫をある位置にガイドします。</span><span class="sxs-lookup"><span data-stu-id="eafbb-199">If it's set to *Automatic*, the system will automatically guide the inventory to a position whenever it can, based on the sort template breaks.</span></span>

1. <span data-ttu-id="eafbb-200">**保存** を選択して、アクション ウィンドウで **クエリの編集** ボタンが使用できるようにします。</span><span class="sxs-lookup"><span data-stu-id="eafbb-200">Select **Save** to make the **Edit query** button on the Action Pane available.</span></span>
1. <span data-ttu-id="eafbb-201">アクション ウィンドウで、**クエリの編集** を選択します。</span><span class="sxs-lookup"><span data-stu-id="eafbb-201">On the Action Pane, select **Edit Query**.</span></span>
1. <span data-ttu-id="eafbb-202">クエリ エディターの **ソーティング** タブで、以下の値を持つ行を追加します。</span><span class="sxs-lookup"><span data-stu-id="eafbb-202">In the query editor, on the **Sorting** tab, add a line that has the following values:</span></span>

    - <span data-ttu-id="eafbb-203">**テーブル:** *出荷*</span><span class="sxs-lookup"><span data-stu-id="eafbb-203">**Table:** *Shipments*</span></span>
    - <span data-ttu-id="eafbb-204">**派生テーブル:** *出荷*</span><span class="sxs-lookup"><span data-stu-id="eafbb-204">**Derived table:** *Shipments*</span></span>
    - <span data-ttu-id="eafbb-205">**フィールド:** *配送サービス*</span><span class="sxs-lookup"><span data-stu-id="eafbb-205">**Field:** *Carrier service*</span></span>

        <span data-ttu-id="eafbb-206">この値を選択すると、次のメッセージが表示されることがあります: "フィールド配送業者のサービスはインデックス フィールドではありません。</span><span class="sxs-lookup"><span data-stu-id="eafbb-206">When you select this value, you might receive the following message: "Field Carrier service is not an index field.</span></span> <span data-ttu-id="eafbb-207">並べ替えを追加しますか ?"</span><span class="sxs-lookup"><span data-stu-id="eafbb-207">Do you want to add sorting on this?"</span></span> <span data-ttu-id="eafbb-208">**はい** を選択します。</span><span class="sxs-lookup"><span data-stu-id="eafbb-208">Select **Yes**.</span></span>

    - <span data-ttu-id="eafbb-209">**検索の方法:** *昇順*</span><span class="sxs-lookup"><span data-stu-id="eafbb-209">**Search direction:** *Ascending*</span></span>

1. <span data-ttu-id="eafbb-210">**OK** を選択します。</span><span class="sxs-lookup"><span data-stu-id="eafbb-210">Select **OK**.</span></span>
1. <span data-ttu-id="eafbb-211">次のメッセージが表示される場合があります: "グループはリセットされますが、続行しますか?"</span><span class="sxs-lookup"><span data-stu-id="eafbb-211">You might receive the following message: "Grouping will be reset, continue?"</span></span> <span data-ttu-id="eafbb-212">**はい** を選択します。</span><span class="sxs-lookup"><span data-stu-id="eafbb-212">Select **Yes**.</span></span>

    <span data-ttu-id="eafbb-213">アクション ウィンドウの **アウトバウンド ソーティング テンプレート分割** ボタンが使用可能になります。</span><span class="sxs-lookup"><span data-stu-id="eafbb-213">The **Outbound sorting template breaks** button on the Action Pane becomes available.</span></span>

1. <span data-ttu-id="eafbb-214">アクション ウィンドウで、**アウトバウンド ソーティング テンプレート分割** を選択します。</span><span class="sxs-lookup"><span data-stu-id="eafbb-214">On the Action Pane, select **Outbound sorting template breaks**.</span></span>
1. <span data-ttu-id="eafbb-215">**アウトバウンド ソーティング 基準** ダイアログ ボックスで、次の値を設定します。</span><span class="sxs-lookup"><span data-stu-id="eafbb-215">In the **Outbound sorting criteria** dialog box, set the following values:</span></span>

    - <span data-ttu-id="eafbb-216">**参照テーブル名:** *出荷*</span><span class="sxs-lookup"><span data-stu-id="eafbb-216">**Reference table name:** *Shipments*</span></span>
    - <span data-ttu-id="eafbb-217">**参照フィールド名:** *配送業者サービス*</span><span class="sxs-lookup"><span data-stu-id="eafbb-217">**Reference field name:** *Carrier service*</span></span>
    - <span data-ttu-id="eafbb-218">**フィールドでグループ化:** 配送業者サービス別に出荷をグループ化するには、このチェック ボックスを選択します。</span><span class="sxs-lookup"><span data-stu-id="eafbb-218">**Group by field:** Select this check box to group shipments by carrier service.</span></span>

1. <span data-ttu-id="eafbb-219">**OK** を選択して設定を保存し、ダイアログ ボックスを閉じます。</span><span class="sxs-lookup"><span data-stu-id="eafbb-219">Select **OK** to save your settings and close the dialog box.</span></span>

### <a name="set-up-container-packing-policies"></a><span data-ttu-id="eafbb-220">コンテナー梱包ポリシーの設定</span><span class="sxs-lookup"><span data-stu-id="eafbb-220">Set up container packing policies</span></span>

1. <span data-ttu-id="eafbb-221">**倉庫管理 \> 設定 \> コンテナ― \> コンテナ―梱包ポリシー** の順に移動します。</span><span class="sxs-lookup"><span data-stu-id="eafbb-221">Go to **Warehouse management \> Setup \> Containers \> Container packing policies**.</span></span>
1. <span data-ttu-id="eafbb-222">アクション ウィンドウで、**新規** を選択します。</span><span class="sxs-lookup"><span data-stu-id="eafbb-222">On the Action Pane, select **New**.</span></span>
1. <span data-ttu-id="eafbb-223">新規ポリシーのヘッダーで、次の値を設定します。</span><span class="sxs-lookup"><span data-stu-id="eafbb-223">In the header of the new policy, set the following values:</span></span>

    - <span data-ttu-id="eafbb-224">**コンテナー梱包ポリシー:** *ソート*</span><span class="sxs-lookup"><span data-stu-id="eafbb-224">**Container packing policy:** *Sort*</span></span>
    - <span data-ttu-id="eafbb-225">**説明:** *ソート*</span><span class="sxs-lookup"><span data-stu-id="eafbb-225">**Description:** *Sort*</span></span>

1. <span data-ttu-id="eafbb-226">**概要** クイック タブで、次の値を設定します。</span><span class="sxs-lookup"><span data-stu-id="eafbb-226">On the **Overview** FastTab, set the following values:</span></span>

    - <span data-ttu-id="eafbb-227">**倉庫:** *62*</span><span class="sxs-lookup"><span data-stu-id="eafbb-227">**Warehouse:** *62*</span></span>
    - <span data-ttu-id="eafbb-228">**ソーティングの規定の場所:** *SORT*</span><span class="sxs-lookup"><span data-stu-id="eafbb-228">**Default location for sorting:** *SORT*</span></span>
    - <span data-ttu-id="eafbb-229">**重量単位:** *kg*</span><span class="sxs-lookup"><span data-stu-id="eafbb-229">**Weight unit:** *kg*</span></span>
    - <span data-ttu-id="eafbb-230">**コンテナーのクロージング ポリシー:** *自動リリース*</span><span class="sxs-lookup"><span data-stu-id="eafbb-230">**Container closing policy:** *Automatic release*</span></span>
    - <span data-ttu-id="eafbb-231">**コンテナーのリリース ポリシー:** *アウトバウンド ソーティング位置にコンテナーを割り当てる*</span><span class="sxs-lookup"><span data-stu-id="eafbb-231">**Container release policy:** *Assign container to outbound sorting position*</span></span>

1. <span data-ttu-id="eafbb-232">**保存** を選択します。</span><span class="sxs-lookup"><span data-stu-id="eafbb-232">Select **Save**.</span></span>

### <a name="set-up-packing-profiles"></a><span data-ttu-id="eafbb-233">梱包プロファイルの設定</span><span class="sxs-lookup"><span data-stu-id="eafbb-233">Set up packing profiles</span></span>

<span data-ttu-id="eafbb-234">ソーティング機能と共に使用される新しい梱包プロファイルを作成します。</span><span class="sxs-lookup"><span data-stu-id="eafbb-234">Create a new packing profile that will be used together with the sorting functionality.</span></span>

1. <span data-ttu-id="eafbb-235">**倉庫管理 \> 設定 \> 梱包 \> 梱包プロファイル** の順に移動します。</span><span class="sxs-lookup"><span data-stu-id="eafbb-235">Go to **Warehouse management \> Setup \> Packing \> Packing profiles**.</span></span>
1. <span data-ttu-id="eafbb-236">アクション ウィンドウで、**新規** を選択して明細行を作成し、次の値を設定します。</span><span class="sxs-lookup"><span data-stu-id="eafbb-236">On the Action Pane, select **New** to create a line, and set the following values for it:</span></span>

    - <span data-ttu-id="eafbb-237">**梱包プロファイル ID:** *ソート*</span><span class="sxs-lookup"><span data-stu-id="eafbb-237">**Packing profile ID:** *Sort*</span></span>
    - <span data-ttu-id="eafbb-238">**説明:** *ソート*</span><span class="sxs-lookup"><span data-stu-id="eafbb-238">**Description:** *Sort*</span></span>
    - <span data-ttu-id="eafbb-239">**コンテナー梱包ポリシー:** *ソート*</span><span class="sxs-lookup"><span data-stu-id="eafbb-239">**Container packing policy:** *Sort*</span></span>
    - <span data-ttu-id="eafbb-240">**コンテナー ID モード:** *自動*</span><span class="sxs-lookup"><span data-stu-id="eafbb-240">**Container ID mode:** *Auto*</span></span>
    - <span data-ttu-id="eafbb-241">**コンテナー タイプ:** *ボックス-大*</span><span class="sxs-lookup"><span data-stu-id="eafbb-241">**Container type:** *Box-Large*</span></span>
    - <span data-ttu-id="eafbb-242">**コンテナーのクローズ時にコンテナーを自動作成する:** オフ (= *いいえ*)</span><span class="sxs-lookup"><span data-stu-id="eafbb-242">**Auto create container at container close:** Cleared (= *No*)</span></span>

1. <span data-ttu-id="eafbb-243">**保存** を選択します。</span><span class="sxs-lookup"><span data-stu-id="eafbb-243">Select **Save**.</span></span>

### <a name="set-up-work-classes"></a><span data-ttu-id="eafbb-244">作業クラスの設定</span><span class="sxs-lookup"><span data-stu-id="eafbb-244">Set up work classes</span></span>

<span data-ttu-id="eafbb-245">ソーティングと共に使用される作業クラスを設定します。</span><span class="sxs-lookup"><span data-stu-id="eafbb-245">Set up a work class that will be used together with sorting.</span></span>

1. <span data-ttu-id="eafbb-246">**倉庫管理 \> 設定 \> 作業 \> 作業クラス** の順に移動します。</span><span class="sxs-lookup"><span data-stu-id="eafbb-246">Go to **Warehouse management \> Setup \> Work \> Work classes**.</span></span>
1. <span data-ttu-id="eafbb-247">アクション ウィンドウで、ソーティングの作業クラスを作成するために **新規** を選択して、次の値を設定します。</span><span class="sxs-lookup"><span data-stu-id="eafbb-247">On the Action Pane, select **New** to create a work class for sorting, and set the following values for it:</span></span>

    - <span data-ttu-id="eafbb-248">**作業クラス ID:** *ソート*</span><span class="sxs-lookup"><span data-stu-id="eafbb-248">**Work class ID:** *Sort*</span></span>
    - <span data-ttu-id="eafbb-249">**説明:** *ソート*</span><span class="sxs-lookup"><span data-stu-id="eafbb-249">**Description:** *Sort*</span></span>
    - <span data-ttu-id="eafbb-250">**作業指示のタイプ:** *ソート済み在庫のピッキング*</span><span class="sxs-lookup"><span data-stu-id="eafbb-250">**Work order type:** *Sorted inventory picking*</span></span>

1. <span data-ttu-id="eafbb-251">**保存** を選択します。</span><span class="sxs-lookup"><span data-stu-id="eafbb-251">Select **Save**.</span></span>

### <a name="set-up-mobile-device-menu-items"></a><span data-ttu-id="eafbb-252">モバイル デバイス メニュー項目を設定する</span><span class="sxs-lookup"><span data-stu-id="eafbb-252">Set up mobile device menu items</span></span>

#### <a name="set-up-a-new-pallet-menu-item"></a><span data-ttu-id="eafbb-253">新規パレットのメニュー項目を設定する</span><span class="sxs-lookup"><span data-stu-id="eafbb-253">Set up a new pallet menu item</span></span>

<span data-ttu-id="eafbb-254">ソーティング中にパレットを構築するためのモバイル デバイス メニュー項目を作成します。</span><span class="sxs-lookup"><span data-stu-id="eafbb-254">Create a mobile device menu item to build pallets during sorting.</span></span>

1. <span data-ttu-id="eafbb-255">**倉庫管理 \> 設定 \> モバイル デバイス \> モバイル デバイスのメニュー品目** の順に移動します。</span><span class="sxs-lookup"><span data-stu-id="eafbb-255">Go to **Warehouse management \> Setup \> Mobile device \> Mobile device menu items**.</span></span>
1. <span data-ttu-id="eafbb-256">アクション ウィンドウで、**新規** を選択します。</span><span class="sxs-lookup"><span data-stu-id="eafbb-256">On the Action Pane, select **New**.</span></span>
1. <span data-ttu-id="eafbb-257">ヘッダーで、次の値を設定します。</span><span class="sxs-lookup"><span data-stu-id="eafbb-257">In the header, set the following values:</span></span>

    - <span data-ttu-id="eafbb-258">**メニュー項目名:** *パレット構築*</span><span class="sxs-lookup"><span data-stu-id="eafbb-258">**Menu item name:** *Pallet build*</span></span>
    - <span data-ttu-id="eafbb-259">**タイトル:** *パレット構築*</span><span class="sxs-lookup"><span data-stu-id="eafbb-259">**Title:** *Pallet build*</span></span>
    - <span data-ttu-id="eafbb-260">**モード:** *間接*</span><span class="sxs-lookup"><span data-stu-id="eafbb-260">**Mode:** *Indirect*</span></span>
    - <span data-ttu-id="eafbb-261">**既存の作業を使用する :** *いいえ*</span><span class="sxs-lookup"><span data-stu-id="eafbb-261">**Use existing work:** *No*</span></span>

1. <span data-ttu-id="eafbb-262">**一般** クイック タブで、次の値を設定します。</span><span class="sxs-lookup"><span data-stu-id="eafbb-262">On the **General** FastTab, set the following values:</span></span>

    - <span data-ttu-id="eafbb-263">**アクティビティ コード:** *アウトバウンド ソーティング*</span><span class="sxs-lookup"><span data-stu-id="eafbb-263">**Activity code:** *Outbound sorting*</span></span>

        <span data-ttu-id="eafbb-264">このフィールドが *アウトバウンド ソーティング* に設定されている場合は、**アウトバウンド ソーティング テンプレート ID** フィールドが表示されます。</span><span class="sxs-lookup"><span data-stu-id="eafbb-264">When this field is set to *Outbound sorting*, the **Outbound sorting template ID** field is shown.</span></span>

    - <span data-ttu-id="eafbb-265">**プロセスガイドの使用:** *はい*</span><span class="sxs-lookup"><span data-stu-id="eafbb-265">**Use process guide:** *Yes*</span></span>

        <span data-ttu-id="eafbb-266">**アクティビティ コード** フィールドを *アウトバウンド ソーティング* に設定すると、このオプションは自動的に *はい* に設定されます。</span><span class="sxs-lookup"><span data-stu-id="eafbb-266">When the **Activity code** field is set to *Outbound sorting*, this option is automatically set to *Yes*.</span></span>

    - <span data-ttu-id="eafbb-267">**アウトバウンド ソーティング テンプレート ID:** *AutoWork*</span><span class="sxs-lookup"><span data-stu-id="eafbb-267">**Outbound sorting template ID:** *AutoWork*</span></span>

1. <span data-ttu-id="eafbb-268">**保存** を選択します。</span><span class="sxs-lookup"><span data-stu-id="eafbb-268">Select **Save**.</span></span>

#### <a name="set-up-a-new-loading-menu-item"></a><span data-ttu-id="eafbb-269">新規積荷メニュー項目を設定する</span><span class="sxs-lookup"><span data-stu-id="eafbb-269">Set up a new loading menu item</span></span>

<span data-ttu-id="eafbb-270">次に、ユーザーがソートされた在庫品目を出荷場所に移動できるメニュー項目を作成します。</span><span class="sxs-lookup"><span data-stu-id="eafbb-270">Next, create a menu item that lets users move the sorted inventory items to the shipping location.</span></span>

1. <span data-ttu-id="eafbb-271">**倉庫管理 \> 設定 \> モバイル デバイス \> モバイル デバイスのメニュー品目** の順に移動します。</span><span class="sxs-lookup"><span data-stu-id="eafbb-271">Go to **Warehouse management \> Setup \> Mobile device \> Mobile device menu items**.</span></span>
1. <span data-ttu-id="eafbb-272">アクション ウィンドウで、**新規** を選択します。</span><span class="sxs-lookup"><span data-stu-id="eafbb-272">On the Action Pane, select **New**.</span></span>
1. <span data-ttu-id="eafbb-273">ヘッダーで、次の値を設定します。</span><span class="sxs-lookup"><span data-stu-id="eafbb-273">In the header, set the following values:</span></span>

    - <span data-ttu-id="eafbb-274">**メニュー項目名:** *ソーティングからの積荷*</span><span class="sxs-lookup"><span data-stu-id="eafbb-274">**Menu item name:** *Load from Sorting*</span></span>
    - <span data-ttu-id="eafbb-275">**タイトル:** *ソーティングからの積荷*</span><span class="sxs-lookup"><span data-stu-id="eafbb-275">**Title:** *Load from Sorting*</span></span>
    - <span data-ttu-id="eafbb-276">**モード:** *作業*</span><span class="sxs-lookup"><span data-stu-id="eafbb-276">**Mode:** *Work*</span></span>
    - <span data-ttu-id="eafbb-277">**既存の作業を使用:** *はい*</span><span class="sxs-lookup"><span data-stu-id="eafbb-277">**Use existing work:** *Yes*</span></span>

1. <span data-ttu-id="eafbb-278">**一般** クイック タブで、**指示者** フィールドを *ユーザー主導* に設定します。</span><span class="sxs-lookup"><span data-stu-id="eafbb-278">On the **General** FastTab, set the **Directed by** field to *User directed*.</span></span>
1. <span data-ttu-id="eafbb-279">**作業クラス** クイック タブで、**新規** を選択して、次の値を設定します。</span><span class="sxs-lookup"><span data-stu-id="eafbb-279">On the **Work classes** FastTab, select **New**, and then set the following values:</span></span>

    - <span data-ttu-id="eafbb-280">**作業クラス ID:** *SORT*</span><span class="sxs-lookup"><span data-stu-id="eafbb-280">**Work class ID:** *SORT*</span></span>
    - <span data-ttu-id="eafbb-281">**作業指示のタイプ:** *ソート済み在庫のピッキング*</span><span class="sxs-lookup"><span data-stu-id="eafbb-281">**Work order type:** *Sorted inventory picking*</span></span>

1. <span data-ttu-id="eafbb-282">**保存** を選択します。</span><span class="sxs-lookup"><span data-stu-id="eafbb-282">Select **Save**.</span></span>

### <a name="set-up-the-mobile-device-menu"></a><span data-ttu-id="eafbb-283">モバイル デバイス メニューを設定する</span><span class="sxs-lookup"><span data-stu-id="eafbb-283">Set up the mobile device menu</span></span>

<span data-ttu-id="eafbb-284">ここで、新しいメニュー項目をモバイル デバイス メニューに追加する必要があります。</span><span class="sxs-lookup"><span data-stu-id="eafbb-284">You must now add the new menu items to the mobile device menu.</span></span>

1. <span data-ttu-id="eafbb-285">**倉庫管理 \> 設定 \> モバイル デバイス \> モバイル デバイス メニュー** の順に移動します。</span><span class="sxs-lookup"><span data-stu-id="eafbb-285">Go to **Warehouse management \> Setup \> Mobile device \> Mobile device menu**.</span></span>
1. <span data-ttu-id="eafbb-286">**出荷** メニューを選択します。</span><span class="sxs-lookup"><span data-stu-id="eafbb-286">Select the **Outbound** menu.</span></span>
1. <span data-ttu-id="eafbb-287">アクション ウィンドウで、**編集** を選択します。</span><span class="sxs-lookup"><span data-stu-id="eafbb-287">On the Action Pane, select **Edit**.</span></span>
1. <span data-ttu-id="eafbb-288">**使用可能なメニューとメニュー項目** 列で、**パレット構築** を検索して選択します。</span><span class="sxs-lookup"><span data-stu-id="eafbb-288">In the **Available menus and menu items** column, find and select **Pallet build**.</span></span>
1. <span data-ttu-id="eafbb-289">右矢印ボタンを選択して、**調整** を **メニュー構造** 列の一覧に移動します。</span><span class="sxs-lookup"><span data-stu-id="eafbb-289">Select the right arrow button to move **Pallet build** to the **Menu structure** column.</span></span>
1. <span data-ttu-id="eafbb-290">上矢印ボタンと下矢印ボタンを使用して、モバイル デバイス メニューの目的の位置にある **パレット構築** メニュー項目に行きます。</span><span class="sxs-lookup"><span data-stu-id="eafbb-290">Use the up arrow and down arrow buttons to put the **Pallet build** menu item in the desired position on the mobile device menu.</span></span>
1. <span data-ttu-id="eafbb-291">**保存** を選択します。</span><span class="sxs-lookup"><span data-stu-id="eafbb-291">Select **Save**.</span></span>
1. <span data-ttu-id="eafbb-292">この手順を繰り返して、**ソーティングからの積荷** メニュー項目を **アウトバウンド** メニューに追加します。</span><span class="sxs-lookup"><span data-stu-id="eafbb-292">Repeat this procedure to add the **Load from Sorting** menu item to the **Outbound** menu.</span></span>

### <a name="set-up-location-directives"></a><span data-ttu-id="eafbb-293">場所ディレクティブを設定します</span><span class="sxs-lookup"><span data-stu-id="eafbb-293">Set up location directives</span></span>

<span data-ttu-id="eafbb-294">*場所ディレクティブ* は、在庫移動のピッキングとプットの場所を識別するのにに役立つルールです。</span><span class="sxs-lookup"><span data-stu-id="eafbb-294">*Location directives* are rules that help identify pick and put locations for inventory movement.</span></span> <span data-ttu-id="eafbb-295">次に、ソーティング作業を管理するルールを作成する必要があります。</span><span class="sxs-lookup"><span data-stu-id="eafbb-295">You must now create a rule to manage the sorting work.</span></span>

#### <a name="set-up-a-single-sku-directive"></a><span data-ttu-id="eafbb-296">(SKU) ディレクティブの設定</span><span class="sxs-lookup"><span data-stu-id="eafbb-296">Set up a single-SKU directive</span></span>

1. <span data-ttu-id="eafbb-297">**倉庫管理 \> 設定 \> 場所のディレクティブ** に移動します。</span><span class="sxs-lookup"><span data-stu-id="eafbb-297">Go to **Warehouse management \> Setup \> Location directives**.</span></span>
1. <span data-ttu-id="eafbb-298">左ウィンドウで、**作業指示タイプ** フィールドの値を *ソート済み在庫ピッキング* に変更します。</span><span class="sxs-lookup"><span data-stu-id="eafbb-298">In the left pane, change the value of the **Work order type** field to *Sorted inventory picking*.</span></span>
1. <span data-ttu-id="eafbb-299">アクション ウィンドウで、**新規** を選択します。</span><span class="sxs-lookup"><span data-stu-id="eafbb-299">On the Action Pane, select **New**.</span></span>
1. <span data-ttu-id="eafbb-300">ヘッダーで、次の値を設定します。</span><span class="sxs-lookup"><span data-stu-id="eafbb-300">In the header, set the following values:</span></span>

    - <span data-ttu-id="eafbb-301">**シーケンス:** *1*</span><span class="sxs-lookup"><span data-stu-id="eafbb-301">**Sequence:** *1*</span></span>
    - <span data-ttu-id="eafbb-302">**名前 :** *ベイドア*</span><span class="sxs-lookup"><span data-stu-id="eafbb-302">**Name:** *Baydoor*</span></span>

1. <span data-ttu-id="eafbb-303">**場所のディレクティブ** クイック タブで、次の値を設定します。</span><span class="sxs-lookup"><span data-stu-id="eafbb-303">On the **Location directives** FastTab, set the following values:</span></span>

    - <span data-ttu-id="eafbb-304">**作業タイプ:** *プット*</span><span class="sxs-lookup"><span data-stu-id="eafbb-304">**Work type:** *Put*</span></span>
    - <span data-ttu-id="eafbb-305">**サイト:** *6*</span><span class="sxs-lookup"><span data-stu-id="eafbb-305">**Site:** *6*</span></span>
    - <span data-ttu-id="eafbb-306">**倉庫:** *62*</span><span class="sxs-lookup"><span data-stu-id="eafbb-306">**Warehouse:** *62*</span></span>
    - <span data-ttu-id="eafbb-307">**複数の SKU:** *いいえ*</span><span class="sxs-lookup"><span data-stu-id="eafbb-307">**Multiple SKU:** *No*</span></span>

1. <span data-ttu-id="eafbb-308">**保存** を選択して、**明細行** クイック タブでツール バーを使用できるようにします。</span><span class="sxs-lookup"><span data-stu-id="eafbb-308">Select **Save** to make the toolbar on the **Lines** FastTab available.</span></span>
1. <span data-ttu-id="eafbb-309">**明細行** クイック タブで、**新規** を選択して、新規明細行で次の値を設定します。</span><span class="sxs-lookup"><span data-stu-id="eafbb-309">On the **Lines** FastTab, select **New**, and then set the following values on the new line.</span></span> <span data-ttu-id="eafbb-310">その他のすべてのフィールドの規定値を受け入れます。</span><span class="sxs-lookup"><span data-stu-id="eafbb-310">Accept the default values for all the other fields.</span></span>

    - <span data-ttu-id="eafbb-311">**シーケンス:** *1*</span><span class="sxs-lookup"><span data-stu-id="eafbb-311">**Sequence:** *1*</span></span>
    - <span data-ttu-id="eafbb-312">**開始:** *0*</span><span class="sxs-lookup"><span data-stu-id="eafbb-312">**From:** *0*</span></span>
    - <span data-ttu-id="eafbb-313">**終了:** *1,000,000*</span><span class="sxs-lookup"><span data-stu-id="eafbb-313">**To:** *1,000,000*</span></span>

1. <span data-ttu-id="eafbb-314">**保存** を選択して、**場所ディレクティブ アクション** クイック タブでツールバーを使用できるようにします。</span><span class="sxs-lookup"><span data-stu-id="eafbb-314">Select **Save** to make the toolbar on the **Location Directive Actions** FastTab available.</span></span>
1. <span data-ttu-id="eafbb-315">**場所ディレクティブ アクション** クイック タブで、**新規** を選択して、新規明細行で次の値を設定します。</span><span class="sxs-lookup"><span data-stu-id="eafbb-315">On the **Location Directive Actions** FastTab, select **New**, and then set the following values on the new line.</span></span> <span data-ttu-id="eafbb-316">その他のすべてのフィールドの規定値を受け入れます。</span><span class="sxs-lookup"><span data-stu-id="eafbb-316">Accept the default values for all the other fields.</span></span>

    - <span data-ttu-id="eafbb-317">**シーケンス:** *1*</span><span class="sxs-lookup"><span data-stu-id="eafbb-317">**Sequence:** *1*</span></span>
    - <span data-ttu-id="eafbb-318">**名前 :** *ベイドア*</span><span class="sxs-lookup"><span data-stu-id="eafbb-318">**Name:** *Baydoor*</span></span>

1. <span data-ttu-id="eafbb-319">**保存** を選択します。</span><span class="sxs-lookup"><span data-stu-id="eafbb-319">Select **Save**.</span></span>
1. <span data-ttu-id="eafbb-320">**場所ディレクティブ アクション** クイック タブで、**クエリの編集** を選択します。</span><span class="sxs-lookup"><span data-stu-id="eafbb-320">On the **Location Directive Actions** FastTab, select **Edit query**.</span></span>
1. <span data-ttu-id="eafbb-321">**範囲** タブのクエリ エディターで、**フィールド** フィールドが *場所* に設定されている行を検索します。</span><span class="sxs-lookup"><span data-stu-id="eafbb-321">In the query editor, on the **Range** tab, find the row where the **Field** field is set to *Location*.</span></span> <span data-ttu-id="eafbb-322">この行の **基準** フィールドを *Baydoor* に設定します。</span><span class="sxs-lookup"><span data-stu-id="eafbb-322">Set the **Criteria** field for this row to *Baydoor*.</span></span>
1. <span data-ttu-id="eafbb-323">**OK** を選択して設定を保存し、クエリ エディターを閉じます。</span><span class="sxs-lookup"><span data-stu-id="eafbb-323">Select **OK** to save your settings and close the query editor.</span></span>

#### <a name="set-up-a-multiple-sku-directive"></a><span data-ttu-id="eafbb-324">複数の (SKU) ディレクティブの設定</span><span class="sxs-lookup"><span data-stu-id="eafbb-324">Set up a multiple-SKU directive</span></span>

1. <span data-ttu-id="eafbb-325">**倉庫管理 \> 設定 \> 場所のディレクティブ** に移動します。</span><span class="sxs-lookup"><span data-stu-id="eafbb-325">Go to **Warehouse management \> Setup \> Location directives**.</span></span>
1. <span data-ttu-id="eafbb-326">左ウィンドウで、**作業指示タイプ** フィールドの値を *ソート済み在庫ピッキング* に変更します。</span><span class="sxs-lookup"><span data-stu-id="eafbb-326">In the left pane, change the value of the **Work order type** field to *Sorted inventory picking*.</span></span>
1. <span data-ttu-id="eafbb-327">アクション ウィンドウで、**新規** を選択します。</span><span class="sxs-lookup"><span data-stu-id="eafbb-327">On the Action Pane, select **New**.</span></span>
1. <span data-ttu-id="eafbb-328">ヘッダーで、次の値を設定します。</span><span class="sxs-lookup"><span data-stu-id="eafbb-328">In the header, set the following values:</span></span>

    - <span data-ttu-id="eafbb-329">**シーケンス:** *2*</span><span class="sxs-lookup"><span data-stu-id="eafbb-329">**Sequence:** *2*</span></span>
    - <span data-ttu-id="eafbb-330">**名前:** *Baydoor Multi*</span><span class="sxs-lookup"><span data-stu-id="eafbb-330">**Name:** *Baydoor Multi*</span></span>

1. <span data-ttu-id="eafbb-331">**場所のディレクティブ** クイック タブで、次の値を設定します。</span><span class="sxs-lookup"><span data-stu-id="eafbb-331">On the **Location directives** FastTab, set the following values:</span></span>

    - <span data-ttu-id="eafbb-332">**作業タイプ:** *プット*</span><span class="sxs-lookup"><span data-stu-id="eafbb-332">**Work type:** *Put*</span></span>
    - <span data-ttu-id="eafbb-333">**サイト:** *6*</span><span class="sxs-lookup"><span data-stu-id="eafbb-333">**Site:** *6*</span></span>
    - <span data-ttu-id="eafbb-334">**倉庫:** *62*</span><span class="sxs-lookup"><span data-stu-id="eafbb-334">**Warehouse:** *62*</span></span>
    - <span data-ttu-id="eafbb-335">**複数のSKU:** *はい*</span><span class="sxs-lookup"><span data-stu-id="eafbb-335">**Multiple SKU:** *Yes*</span></span>

1. <span data-ttu-id="eafbb-336">**保存** を選択して、**明細行** クイック タブでツール バーを使用できるようにします。</span><span class="sxs-lookup"><span data-stu-id="eafbb-336">Select **Save** to make the toolbar on the **Lines** FastTab available.</span></span>
1. <span data-ttu-id="eafbb-337">**明細行** クイック タブで、**新規** を選択して、新規明細行で次の値を設定します。</span><span class="sxs-lookup"><span data-stu-id="eafbb-337">On the **Lines** FastTab, select **New**, and then set the following values on the new line.</span></span> <span data-ttu-id="eafbb-338">その他のすべてのフィールドの規定値を受け入れます。</span><span class="sxs-lookup"><span data-stu-id="eafbb-338">Accept the default values for all the other fields.</span></span>

    - <span data-ttu-id="eafbb-339">**シーケンス:** *1*</span><span class="sxs-lookup"><span data-stu-id="eafbb-339">**Sequence:** *1*</span></span>
    - <span data-ttu-id="eafbb-340">**開始:** *0*</span><span class="sxs-lookup"><span data-stu-id="eafbb-340">**From:** *0*</span></span>
    - <span data-ttu-id="eafbb-341">**終了:** *1,000,000*</span><span class="sxs-lookup"><span data-stu-id="eafbb-341">**To:** *1,000,000*</span></span>

1. <span data-ttu-id="eafbb-342">**保存** を選択して、**場所ディレクティブ アクション** クイック タブでツールバーを使用できるようにします。</span><span class="sxs-lookup"><span data-stu-id="eafbb-342">Select **Save** to make the toolbar on the **Location Directive Actions** FastTab available.</span></span>
1. <span data-ttu-id="eafbb-343">**場所ディレクティブ アクション** クイック タブで、**新規** を選択して、新規明細行で次の値を設定します。</span><span class="sxs-lookup"><span data-stu-id="eafbb-343">On the **Location Directive Actions** FastTab, select **New**, and then set the following values on the new line.</span></span> <span data-ttu-id="eafbb-344">その他のすべてのフィールドの規定値を受け入れます。</span><span class="sxs-lookup"><span data-stu-id="eafbb-344">Accept the default values for all the other fields.</span></span>

    - <span data-ttu-id="eafbb-345">**シーケンス:** *1*</span><span class="sxs-lookup"><span data-stu-id="eafbb-345">**Sequence:** *1*</span></span>
    - <span data-ttu-id="eafbb-346">**名前:** *Baydoor Multi*</span><span class="sxs-lookup"><span data-stu-id="eafbb-346">**Name:** *Baydoor Multi*</span></span>

1. <span data-ttu-id="eafbb-347">**保存** を選択します。</span><span class="sxs-lookup"><span data-stu-id="eafbb-347">Select **Save**.</span></span>
1. <span data-ttu-id="eafbb-348">**場所ディレクティブ アクション** クイック タブで、**クエリの編集** を選択します。</span><span class="sxs-lookup"><span data-stu-id="eafbb-348">On the **Location Directive Actions** FastTab, select **Edit query**.</span></span>
1. <span data-ttu-id="eafbb-349">**範囲** タブのクエリ エディターで、**フィールド** フィールドが *場所* に設定されている行を検索します。</span><span class="sxs-lookup"><span data-stu-id="eafbb-349">In the query editor, on the **Range** tab, find the row where the **Field** field is set to *Location*.</span></span> <span data-ttu-id="eafbb-350">この行の **基準** フィールドを *Baydoor* に設定します。</span><span class="sxs-lookup"><span data-stu-id="eafbb-350">Set the **Criteria** field for this row to *Baydoor*.</span></span>
1. <span data-ttu-id="eafbb-351">**OK** を選択して設定を保存し、クエリ エディターを閉じます。</span><span class="sxs-lookup"><span data-stu-id="eafbb-351">Select **OK** to save your settings and close the query editor.</span></span>

### <a name="set-up-work-templates"></a><span data-ttu-id="eafbb-352">作業テンプレートを設定します</span><span class="sxs-lookup"><span data-stu-id="eafbb-352">Set up work templates</span></span>

1. <span data-ttu-id="eafbb-353">**倉庫管理 \> 設定 \> 作業 \> 作業テンプレート** の順に移動します。</span><span class="sxs-lookup"><span data-stu-id="eafbb-353">Go to **Warehouse management \> Setup \> Work \> Work templates**.</span></span>
1. <span data-ttu-id="eafbb-354">**作業指示タイプ** フィールドの値を *ソート済み在庫ピッキング* に変更します。</span><span class="sxs-lookup"><span data-stu-id="eafbb-354">Change the value of the **Work order type** field to *Sorted inventory picking*.</span></span>
1. <span data-ttu-id="eafbb-355">アクション ウィンドウで **新規** を選択し、作業テンプレートを作成します。</span><span class="sxs-lookup"><span data-stu-id="eafbb-355">On the Action Pane, select **New** to create a work template.</span></span>
1. <span data-ttu-id="eafbb-356">**概要** タブで、次の値を設定します。</span><span class="sxs-lookup"><span data-stu-id="eafbb-356">On the **Overview** tab, set the following values:</span></span>

    - <span data-ttu-id="eafbb-357">**シーケンス:** *1*</span><span class="sxs-lookup"><span data-stu-id="eafbb-357">**Sequence:** *1*</span></span>
    - <span data-ttu-id="eafbb-358">**作業テンプレート:** *Sort*</span><span class="sxs-lookup"><span data-stu-id="eafbb-358">**Work template:** *Sort*</span></span>
    - <span data-ttu-id="eafbb-359">**作業テンプレートの説明:** *Sort*</span><span class="sxs-lookup"><span data-stu-id="eafbb-359">**Work template description:** *Sort*</span></span>

1. <span data-ttu-id="eafbb-360">**保存** を選択して、**作業テンプレートの詳細** クイック タブを使用できるようにします。</span><span class="sxs-lookup"><span data-stu-id="eafbb-360">Select **Save** to make the **Work Template Details** FastTab available.</span></span>
1. <span data-ttu-id="eafbb-361">**作業テンプレートの詳細** クイック タブで、**新規** を選択して明細行を追加し、次の値を設定します。</span><span class="sxs-lookup"><span data-stu-id="eafbb-361">On the **Work Template Details** FastTab, select **New** to add a line, and then set the following values for it:</span></span>

    - <span data-ttu-id="eafbb-362">**作業タイプ:** *ピッキング*</span><span class="sxs-lookup"><span data-stu-id="eafbb-362">**Work type:** *Pick*</span></span>
    - <span data-ttu-id="eafbb-363">**作業クラス ID:** *SORT*</span><span class="sxs-lookup"><span data-stu-id="eafbb-363">**Work class ID:** *SORT*</span></span>

1. <span data-ttu-id="eafbb-364">**新規** を再度選択して 2 行目を追加し、それに次の値を設定します。</span><span class="sxs-lookup"><span data-stu-id="eafbb-364">Select **New** again to add a second line, and then set the following values for it:</span></span>

    - <span data-ttu-id="eafbb-365">**作業タイプ:** *プット*</span><span class="sxs-lookup"><span data-stu-id="eafbb-365">**Work type:** *Put*</span></span>
    - <span data-ttu-id="eafbb-366">**作業クラス ID:** *SORT*</span><span class="sxs-lookup"><span data-stu-id="eafbb-366">**Work class ID:** *SORT*</span></span>

1. <span data-ttu-id="eafbb-367">**保存** を選択します。</span><span class="sxs-lookup"><span data-stu-id="eafbb-367">Select **Save**.</span></span>

## <a name="scenario"></a><span data-ttu-id="eafbb-368">シナリオ</span><span class="sxs-lookup"><span data-stu-id="eafbb-368">Scenario</span></span>

<span data-ttu-id="eafbb-369">このシナリオでは、出荷の配送業者サービスに応じて、梱包済みコンテナーを梱包ステーションの後の異なる位置 (パレット) に自動的にソートされる状況をシミュレートします。</span><span class="sxs-lookup"><span data-stu-id="eafbb-369">This scenario simulates a situation where packed containers should automatically be sorted to different positions (pallets) after the packing station, depending on the shipping carrier service.</span></span> <span data-ttu-id="eafbb-370">積荷からのすべての品目を梱包して住所でソートした後、パレットはベイのドアに移動します。</span><span class="sxs-lookup"><span data-stu-id="eafbb-370">After all items from the load are packed and sorted by address, the pallets will be moved to the bay door.</span></span>

### <a name="create-sales-orders-and-picking-work"></a><span data-ttu-id="eafbb-371">販売注文とピッキング作業の作成</span><span class="sxs-lookup"><span data-stu-id="eafbb-371">Create sales orders and picking work</span></span>

#### <a name="create-sales-order-1"></a><span data-ttu-id="eafbb-372">販売注文の作成 1</span><span class="sxs-lookup"><span data-stu-id="eafbb-372">Create sales order 1</span></span>

1. <span data-ttu-id="eafbb-373">**販売とマーケティング \> 販売注文 \> すべての販売注文** の順に移動します。</span><span class="sxs-lookup"><span data-stu-id="eafbb-373">Go to **Sales and marketing \> Sales orders \> All sales orders**.</span></span>
1. <span data-ttu-id="eafbb-374">アクション ウィンドウで、**新規** を選択します。</span><span class="sxs-lookup"><span data-stu-id="eafbb-374">On the Action Pane, select **New**.</span></span>
1. <span data-ttu-id="eafbb-375">**販売注文の作成** ダイアログ ボックスでは、次の値を設定します。</span><span class="sxs-lookup"><span data-stu-id="eafbb-375">In the **Create sales order** dialog box, set the following values:</span></span>

    - <span data-ttu-id="eafbb-376">**顧客アカウント:** *US-005*</span><span class="sxs-lookup"><span data-stu-id="eafbb-376">**Customer account:** *US-005*</span></span>
    - <span data-ttu-id="eafbb-377">**倉庫:** *62*</span><span class="sxs-lookup"><span data-stu-id="eafbb-377">**Warehouse:** *62*</span></span>

1. <span data-ttu-id="eafbb-378">**OK** を選択してダイアログ ボックスを閉じます。</span><span class="sxs-lookup"><span data-stu-id="eafbb-378">Select **OK** to close the dialog box.</span></span>

    <span data-ttu-id="eafbb-379">新しい販売注文が開かれます。</span><span class="sxs-lookup"><span data-stu-id="eafbb-379">The new sales order is opened.</span></span>

1. <span data-ttu-id="eafbb-380">**ヘッダー** 表示に切り替えます。</span><span class="sxs-lookup"><span data-stu-id="eafbb-380">Switch to the **Header** view.</span></span>
1. <span data-ttu-id="eafbb-381">**配送** クイック タブの **輸送** セクションで、次の値を設定します。</span><span class="sxs-lookup"><span data-stu-id="eafbb-381">On the **Delivery** FastTab, in the **Transportation** section, set the following values:</span></span>

    - <span data-ttu-id="eafbb-382">**配送業者:** *航空貨物*</span><span class="sxs-lookup"><span data-stu-id="eafbb-382">**Shipping carrier:** *Air cargo*</span></span>
    - <span data-ttu-id="eafbb-383">**配送サービス :** *Air*</span><span class="sxs-lookup"><span data-stu-id="eafbb-383">**Carrier service:** *Air*</span></span>

1. <span data-ttu-id="eafbb-384">**明細行** ビューに切り替えます。</span><span class="sxs-lookup"><span data-stu-id="eafbb-384">Switch to the **Lines** view.</span></span>
1. <span data-ttu-id="eafbb-385">新規の空欄明細行が自動的に **販売注文の明細行** クイックタブに追加されない場合は、**行の追加** を選択して 1 つ追加します。</span><span class="sxs-lookup"><span data-stu-id="eafbb-385">If a new, empty line isn't automatically added to the grid on the **Sales order lines** FastTab, select **Add line** to add one.</span></span>
1. <span data-ttu-id="eafbb-386">この新規注文明細行に次の値を設定します。</span><span class="sxs-lookup"><span data-stu-id="eafbb-386">On the new order line, set the following values:</span></span>

    - <span data-ttu-id="eafbb-387">**品目番号:** *A0001*</span><span class="sxs-lookup"><span data-stu-id="eafbb-387">**Item number:** *A0001*</span></span>
    - <span data-ttu-id="eafbb-388">**数量:** *2*</span><span class="sxs-lookup"><span data-stu-id="eafbb-388">**Quantity:** *2*</span></span>

1. <span data-ttu-id="eafbb-389">新しい注文明細行が **販売注文明細行** クイック タブで選択されている間に、グリッドの上部にある **在庫** メニューで **予約** を選択します。</span><span class="sxs-lookup"><span data-stu-id="eafbb-389">While the new order line is still selected on the **Sales order lines** FastTab, on the **Inventory** menu above the grid, select **Reservation**.</span></span>
1. <span data-ttu-id="eafbb-390">**引当** ページで、**引当ロット** を選択して、選択した明細行の全数量を倉庫に引当てます。</span><span class="sxs-lookup"><span data-stu-id="eafbb-390">On the **Reservation** page, select **Reserve lot** to reserve the full quantity of the selected line in the warehouse.</span></span>
1. <span data-ttu-id="eafbb-391">**引当** ページを閉じて、販売注文に戻ります。</span><span class="sxs-lookup"><span data-stu-id="eafbb-391">Close the **Reservation** page to return to the sales order.</span></span>
1. <span data-ttu-id="eafbb-392">アクション ペインの、**倉庫** タブにある **アクション** グループで、**倉庫にリリース** を選択します。</span><span class="sxs-lookup"><span data-stu-id="eafbb-392">On the Action Pane, on the **Warehouse** tab, in the **Actions** group, select **Release to warehouse**.</span></span>
1. <span data-ttu-id="eafbb-393">この注文の出荷とウェーブを示す情報メッセージが表示されます。</span><span class="sxs-lookup"><span data-stu-id="eafbb-393">You receive an informational message that shows the shipment and wave for this order.</span></span> <span data-ttu-id="eafbb-394">ウェーブ ID 番号と出荷 ID 番号をメモします。</span><span class="sxs-lookup"><span data-stu-id="eafbb-394">Make a note of the wave ID and shipment ID numbers.</span></span>

#### <a name="sales-order-2"></a><span data-ttu-id="eafbb-395">販売注文 2</span><span class="sxs-lookup"><span data-stu-id="eafbb-395">Sales order 2</span></span>

1. <span data-ttu-id="eafbb-396">**販売とマーケティング \> 販売注文 \> すべての販売注文** の順に移動します。</span><span class="sxs-lookup"><span data-stu-id="eafbb-396">Go to **Sales and marketing \> Sales orders \> All sales orders**.</span></span>
1. <span data-ttu-id="eafbb-397">アクション ウィンドウで、**新規** を選択します。</span><span class="sxs-lookup"><span data-stu-id="eafbb-397">On the Action Pane, select **New**.</span></span>
1. <span data-ttu-id="eafbb-398">**販売注文の作成** ダイアログ ボックスでは、次の値を設定します。</span><span class="sxs-lookup"><span data-stu-id="eafbb-398">In the **Create sales order** dialog box, set the following values:</span></span>

    - <span data-ttu-id="eafbb-399">**顧客アカウント:** *US-006*</span><span class="sxs-lookup"><span data-stu-id="eafbb-399">**Customer account:** *US-006*</span></span>
    - <span data-ttu-id="eafbb-400">**倉庫:** *62*</span><span class="sxs-lookup"><span data-stu-id="eafbb-400">**Warehouse:** *62*</span></span>

1. <span data-ttu-id="eafbb-401">**OK** を選択してダイアログ ボックスを閉じます。</span><span class="sxs-lookup"><span data-stu-id="eafbb-401">Select **OK** to close the dialog box.</span></span>
1. <span data-ttu-id="eafbb-402">新しい販売注文が開かれます。</span><span class="sxs-lookup"><span data-stu-id="eafbb-402">The new sales order is opened.</span></span> <span data-ttu-id="eafbb-403">**販売注文明細行** クイック タブのグリッドに、新しい空の明細行を含める必要があります。</span><span class="sxs-lookup"><span data-stu-id="eafbb-403">It should include a new, empty line in the grid on the **Sales order lines** FastTab.</span></span> <span data-ttu-id="eafbb-404">この注文明細行に次の値を設定します。</span><span class="sxs-lookup"><span data-stu-id="eafbb-404">Set the following values on this order line:</span></span>

    - <span data-ttu-id="eafbb-405">**品目:** *A0001*</span><span class="sxs-lookup"><span data-stu-id="eafbb-405">**Item:** *A0001*</span></span>
    - <span data-ttu-id="eafbb-406">**数量:** *1*</span><span class="sxs-lookup"><span data-stu-id="eafbb-406">**Quantity:** *1*</span></span>

1. <span data-ttu-id="eafbb-407">**明細行の詳細** クイック タブ の **配送** タブで、**配送のモード** フィールド を *Flowe-STD* に設定します。</span><span class="sxs-lookup"><span data-stu-id="eafbb-407">On the **Line details** FastTab, on the **Delivery** tab, set the **Mode of delivery** field to *Flowe-STD*.</span></span>
1. <span data-ttu-id="eafbb-408">**販売注文明細行** クイック タブで、**明細行を追加** を選択して、2 番目の注文明細行で次の値を設定します。</span><span class="sxs-lookup"><span data-stu-id="eafbb-408">On the **Sales order lines** FastTab, select **Add line**, and then set the following values on the second order line:</span></span>

    - <span data-ttu-id="eafbb-409">**品目:** *A0002*</span><span class="sxs-lookup"><span data-stu-id="eafbb-409">**Item:** *A0002*</span></span>
    - <span data-ttu-id="eafbb-410">**数量:** *1*</span><span class="sxs-lookup"><span data-stu-id="eafbb-410">**Quantity:** *1*</span></span>

1. <span data-ttu-id="eafbb-411">**明細行の詳細** クイック タブ の **配送** タブで、**配送のモード** フィールドの値を *Air C-Air* に変更します。</span><span class="sxs-lookup"><span data-stu-id="eafbb-411">On the **Line details** FastTab, on the **Delivery** tab, change the value of the **Mode of delivery** field to *Air C-Air*.</span></span>
1. <span data-ttu-id="eafbb-412">**販売注文明細行** クイックタブで、最初の販売注文明細行を選択します。</span><span class="sxs-lookup"><span data-stu-id="eafbb-412">On the **Sales order lines** FastTab, select the first order line.</span></span> <span data-ttu-id="eafbb-413">その後、グリッドの上部にある **在庫** メニューで、**引当** を選択します。</span><span class="sxs-lookup"><span data-stu-id="eafbb-413">Then, on the **Inventory** menu above the grid, select **Reservation**.</span></span>
1. <span data-ttu-id="eafbb-414">**引当** ページで、**引当ロット** を選択して、選択した明細行の全数量を倉庫に引当てます。</span><span class="sxs-lookup"><span data-stu-id="eafbb-414">On the **Reservation** page, select **Reserve lot** to reserve the full quantity of the selected line in the warehouse.</span></span>
1. <span data-ttu-id="eafbb-415">**引当** ページを閉じて、販売注文に戻ります。</span><span class="sxs-lookup"><span data-stu-id="eafbb-415">Close the **Reservation** page to return to the sales order.</span></span>
1. <span data-ttu-id="eafbb-416">**販売注文明細行** クイックタブで、2 番目の注文明細行を選択します。</span><span class="sxs-lookup"><span data-stu-id="eafbb-416">On the **Sales order lines** FastTab, select the second order line.</span></span> <span data-ttu-id="eafbb-417">その後、グリッドの上部にある **在庫** メニューで、**引当** を選択します。</span><span class="sxs-lookup"><span data-stu-id="eafbb-417">Then, on the **Inventory** menu above the grid, select **Reservation**.</span></span>
1. <span data-ttu-id="eafbb-418">**引当** ページで、**引当ロット** を選択して、選択した明細行の全数量を倉庫に引当てます。</span><span class="sxs-lookup"><span data-stu-id="eafbb-418">On the **Reservation** page, select **Reserve lot** to reserve the full quantity of the selected line in the warehouse.</span></span>
1. <span data-ttu-id="eafbb-419">**引当** ページを閉じて、販売注文に戻ります。</span><span class="sxs-lookup"><span data-stu-id="eafbb-419">Close the **Reservation** page to return to the sales order.</span></span>
1. <span data-ttu-id="eafbb-420">アクション ペインの、**倉庫** タブにある **アクション** グループで、**倉庫にリリース** を選択します。</span><span class="sxs-lookup"><span data-stu-id="eafbb-420">On the Action Pane, on the **Warehouse** tab, in the **Actions** group, select **Release to warehouse**.</span></span>
1. <span data-ttu-id="eafbb-421">この注文の出荷とウェーブを示す情報メッセージが表示されます。</span><span class="sxs-lookup"><span data-stu-id="eafbb-421">You receive an informational message that shows the shipment and wave for this order.</span></span> <span data-ttu-id="eafbb-422">2 つのウェーブ ID 番号と 2 つの出荷 ID 番号 (販売注文明細行の配送モードに対して各 1 つ) が作成されていることに注意してください。</span><span class="sxs-lookup"><span data-stu-id="eafbb-422">Notice that two wave ID numbers and two shipment ID numbers have been created, one for each mode of delivery for the sales order lines.</span></span>

#### <a name="get-the-work-ids-from-the-work-details"></a><span data-ttu-id="eafbb-423">作業詳細から作業 ID を取得する</span><span class="sxs-lookup"><span data-stu-id="eafbb-423">Get the work IDs from the work details</span></span>

1. <span data-ttu-id="eafbb-424">**倉庫管理 \> 作業 \> 作業の詳細** の順に移動します。</span><span class="sxs-lookup"><span data-stu-id="eafbb-424">Go to **Warehouse management \> Work \> Work details**.</span></span>
1. <span data-ttu-id="eafbb-425">このページには、販売注文から作成された作業 ID が表示されます。</span><span class="sxs-lookup"><span data-stu-id="eafbb-425">The page shows the work IDs that have been created from sales orders.</span></span> <span data-ttu-id="eafbb-426">作成した販売注文のウェーブ ID と出荷 ID を使用して、各ウェーブと出荷の作業 ID を検索します。</span><span class="sxs-lookup"><span data-stu-id="eafbb-426">Use the wave IDs and shipment IDs from the sales orders that you created to find the work ID for each wave and shipment.</span></span> <span data-ttu-id="eafbb-427">これらの作業 ID は次の手順で必要になるため、メモしておきます。</span><span class="sxs-lookup"><span data-stu-id="eafbb-427">Make a note of those work IDs, because you will need them in the next steps.</span></span> <span data-ttu-id="eafbb-428">2 つ目の販売注文に対して 2 つの作業 ID が作成されていることを確認します。</span><span class="sxs-lookup"><span data-stu-id="eafbb-428">Notice that two work IDs were created for the second sales order.</span></span> <span data-ttu-id="eafbb-429">異なる場所からピッキングされた品目がある場合は、個々のワード ID が生成されます。</span><span class="sxs-lookup"><span data-stu-id="eafbb-429">If different items are picked from different locations, separate word IDs are generated.</span></span>

### <a name="pick-items-for-the-sales-orders"></a><span data-ttu-id="eafbb-430">販売注文のピッキング品目</span><span class="sxs-lookup"><span data-stu-id="eafbb-430">Pick items for the sales orders</span></span>

<span data-ttu-id="eafbb-431">モバイル デバイスを使用して、パック ステーションに品目を移動することによって、作成された作業を完了します。</span><span class="sxs-lookup"><span data-stu-id="eafbb-431">Complete the created work by using the mobile device to move the items to the pack station.</span></span>

1. <span data-ttu-id="eafbb-432">モバイル デバイスで、このシナリオに対して作成したユーザー ID (既存のデモ データ ユーザーのユーザー ID) を使用して、倉庫 *62* にログインします。</span><span class="sxs-lookup"><span data-stu-id="eafbb-432">On the mobile device, sign in to warehouse *62* by using the user ID that you created for this scenario (or the user ID of an existing demo data user).</span></span>
1. <span data-ttu-id="eafbb-433">メイン メニューで、**アウトバウンド** を選択します。</span><span class="sxs-lookup"><span data-stu-id="eafbb-433">On the main menu, select **Outbound**.</span></span>
1. <span data-ttu-id="eafbb-434">**アウトバウンド** メニューで、**営業ピッキング** を選択します。</span><span class="sxs-lookup"><span data-stu-id="eafbb-434">On the **Outbound** menu, select **Sales Picking**.</span></span>
1. <span data-ttu-id="eafbb-435">**ID** フィールドに、販売注文 1 に対して作成された作業 ID を入力します。</span><span class="sxs-lookup"><span data-stu-id="eafbb-435">In the **ID** field, enter the work ID that was created for sales order 1.</span></span>
1. <span data-ttu-id="eafbb-436">**OK** を選択します。</span><span class="sxs-lookup"><span data-stu-id="eafbb-436">Select **OK**.</span></span>
1. <span data-ttu-id="eafbb-437">**販売注文-ピッキング** ページで、販売注文 1 に対して作成されたターゲット LP を入力します。</span><span class="sxs-lookup"><span data-stu-id="eafbb-437">On the **Sales orders - Pick** page, enter a target LP that was created for sales order 1.</span></span> <span data-ttu-id="eafbb-438">ピッキング場所 (*ulk-001*)、品目 (*A0001*)、および数量 (*2 個*) 表示されます。</span><span class="sxs-lookup"><span data-stu-id="eafbb-438">Notice that the picking location (*bulk-001*), item (*A0001*), and quantity (*2 pcs*) are shown.</span></span>
1. <span data-ttu-id="eafbb-439">**OK** を選択します。</span><span class="sxs-lookup"><span data-stu-id="eafbb-439">Select **OK**.</span></span>
1. <span data-ttu-id="eafbb-440">**販売注文 - 配置** ページの情報をレビューします。</span><span class="sxs-lookup"><span data-stu-id="eafbb-440">Review the information on the **Sales orders - Put** page.</span></span> <span data-ttu-id="eafbb-441">**Loc** フィールドは、ピッキングされた品目が *梱包* 場所に移動していることを示します。</span><span class="sxs-lookup"><span data-stu-id="eafbb-441">The **Loc** field should indicate that the picked items are going to the *Pack* location.</span></span>
1. <span data-ttu-id="eafbb-442">**OK** を選択します。</span><span class="sxs-lookup"><span data-stu-id="eafbb-442">Select **OK**.</span></span>

    <span data-ttu-id="eafbb-443">**作業 ID / ライセンス プレート ID** ページ上で、販売注文 1 の作業 ID が完了していることを示す、”作業が完了しました” というメッセージを受信します。</span><span class="sxs-lookup"><span data-stu-id="eafbb-443">On the **Scan a work ID / license plate ID** page, you receive a "Work Completed" message, which indicates that the work ID from sales order 1 has been completed.</span></span>

    <span data-ttu-id="eafbb-444">次に、販売注文 2 を選択します。</span><span class="sxs-lookup"><span data-stu-id="eafbb-444">You will now pick sales order 2.</span></span>

1. <span data-ttu-id="eafbb-445">**ID** フィールドで、1 行目が項目 *A0001* となっている販売注文 2 に対して作成された作業 ID を入力します。</span><span class="sxs-lookup"><span data-stu-id="eafbb-445">In the **ID** field, enter the work ID that was created for sales order 2, where line 1 has item *A0001*.</span></span>
1. <span data-ttu-id="eafbb-446">**OK** を選択します。</span><span class="sxs-lookup"><span data-stu-id="eafbb-446">Select **OK**.</span></span>
1. <span data-ttu-id="eafbb-447">**販売注文 - ピッキング** ページで、ターゲット LP を入力します。</span><span class="sxs-lookup"><span data-stu-id="eafbb-447">On the **Sales orders - Pick** page, enter a target LP.</span></span> <span data-ttu-id="eafbb-448">ピッキング場所 (*ulk-001*)、品目 (*A0001*)、および数量 (*1 個*) が表示されていることに注意して下さい。</span><span class="sxs-lookup"><span data-stu-id="eafbb-448">Notice that the picking location (*bulk-001*), item (*A0001*), and quantity (*1 pcs*) are shown.</span></span>
1. <span data-ttu-id="eafbb-449">**OK** を選択します。</span><span class="sxs-lookup"><span data-stu-id="eafbb-449">Select **OK**.</span></span>
1. <span data-ttu-id="eafbb-450">**販売注文 - 配置** ページの情報をレビューします。</span><span class="sxs-lookup"><span data-stu-id="eafbb-450">Review the information on the **Sales orders - Put** page.</span></span> <span data-ttu-id="eafbb-451">**Loc** フィールドは、ピッキングされた品目が *梱包* 場所に移動していることを示します。</span><span class="sxs-lookup"><span data-stu-id="eafbb-451">The **Loc** field should indicate that the picked items are going to the *Pack* location.</span></span>
1. <span data-ttu-id="eafbb-452">**OK** を選択します。</span><span class="sxs-lookup"><span data-stu-id="eafbb-452">Select **OK**.</span></span>

    <span data-ttu-id="eafbb-453">**作業 ID / ライセンス プレート ID のスキャン** ページで、"作業が完了しました" というメッセージが表示されます。</span><span class="sxs-lookup"><span data-stu-id="eafbb-453">On the **Scan a work ID / license plate ID** page, you receive a "Work Completed" message.</span></span> <span data-ttu-id="eafbb-454">このメッセージは、販売注文 2 の 1 行目の作業 ID が完了したことを示しています。</span><span class="sxs-lookup"><span data-stu-id="eafbb-454">This message indicates that the work ID from line 1 of sales order 2 has been completed.</span></span>

1. <span data-ttu-id="eafbb-455">**ID** フィールドで、2 行目が項目 *A0002* となる販売注文 2 に対して作成された作業 ID を入力します。</span><span class="sxs-lookup"><span data-stu-id="eafbb-455">In the **ID** field, enter the work ID that was created for sales order 2, where line 2 has item *A0002*.</span></span>
1. <span data-ttu-id="eafbb-456">**OK** を選択します。</span><span class="sxs-lookup"><span data-stu-id="eafbb-456">Select **OK**.</span></span>
1. <span data-ttu-id="eafbb-457">**販売注文 - ピッキング** ページで、ターゲット LP を入力します。</span><span class="sxs-lookup"><span data-stu-id="eafbb-457">On the **Sales orders - Pick** page, enter a target LP.</span></span> <span data-ttu-id="eafbb-458">ピッキング場所 (*ulk-002*)、品目 (*A0001*)、および数量 (*1 個*) が表示されていることに注意して下さい。</span><span class="sxs-lookup"><span data-stu-id="eafbb-458">Notice that the picking location (*bulk-002*), item (*A0001*), and quantity (*1 pcs*) are shown.</span></span>
1. <span data-ttu-id="eafbb-459">**OK** を選択します。</span><span class="sxs-lookup"><span data-stu-id="eafbb-459">Select **OK**.</span></span>
1. <span data-ttu-id="eafbb-460">**販売注文 - 配置** ページの情報をレビューします。</span><span class="sxs-lookup"><span data-stu-id="eafbb-460">Review the information on the **Sales orders - Put** page.</span></span> <span data-ttu-id="eafbb-461">**Loc** フィールドは、ピッキングされた品目が *梱包* 場所に移動していることを示します。</span><span class="sxs-lookup"><span data-stu-id="eafbb-461">The **Loc** field should indicate that the picked items are going to the *Pack* location.</span></span>
1. <span data-ttu-id="eafbb-462">**OK** を選択します。</span><span class="sxs-lookup"><span data-stu-id="eafbb-462">Select **OK**.</span></span>

    <span data-ttu-id="eafbb-463">**作業 ID / ライセンス プレート ID のスキャン** ページで、"作業が完了しました" というメッセージが表示されます。</span><span class="sxs-lookup"><span data-stu-id="eafbb-463">On the **Scan a work ID / license plate ID** page, you receive a "Work Completed" message.</span></span> <span data-ttu-id="eafbb-464">このメッセージは、販売注文 2 の 2 行目の作業 ID が完了したことを示しています。</span><span class="sxs-lookup"><span data-stu-id="eafbb-464">This message indicates that the work ID from line 2 of sales order 2 has been completed.</span></span>

### <a name="pack-sales-orders-into-containers"></a><span data-ttu-id="eafbb-465">販売注文をコンテナーに梱包する</span><span class="sxs-lookup"><span data-stu-id="eafbb-465">Pack sales orders into containers</span></span>

#### <a name="pack-sales-order-1-into-containers"></a><span data-ttu-id="eafbb-466">販売注文 1 をコンテナーに梱包する</span><span class="sxs-lookup"><span data-stu-id="eafbb-466">Pack sales order 1 into containers</span></span>

1. <span data-ttu-id="eafbb-467">**倉庫管理 \> 梱包とパックとコンテナー詰め \> 梱包** の順に移動します。</span><span class="sxs-lookup"><span data-stu-id="eafbb-467">Go to **Warehouse management \> Packing and containerization \> Pack**.</span></span>

    <span data-ttu-id="eafbb-468">**梱包ステーションの選択** ダイアログ ボックスが表示されます。</span><span class="sxs-lookup"><span data-stu-id="eafbb-468">The **Select packing station** dialog box appears.</span></span> <span data-ttu-id="eafbb-469">既定では、**作業者** フィールドは以前に設定した作業者の名前に設定する必要があります。</span><span class="sxs-lookup"><span data-stu-id="eafbb-469">By default, the **Worker** field should be set to the name of the worker that you set up earlier.</span></span>

1. <span data-ttu-id="eafbb-470">特定の梱包ステーションで計画されている出荷およびコンテナーを表示し作業するために次の値を設定します。</span><span class="sxs-lookup"><span data-stu-id="eafbb-470">Set the following values to view and work on shipments and containers that are planned at the specific packing location:</span></span>

    - <span data-ttu-id="eafbb-471">**サイト:** *6*</span><span class="sxs-lookup"><span data-stu-id="eafbb-471">**Site:** *6*</span></span>
    - <span data-ttu-id="eafbb-472">**倉庫:** *62*</span><span class="sxs-lookup"><span data-stu-id="eafbb-472">**Warehouse:** *62*</span></span>
    - <span data-ttu-id="eafbb-473">**場所:** *梱包*</span><span class="sxs-lookup"><span data-stu-id="eafbb-473">**Location:** *Pack*</span></span>
    - <span data-ttu-id="eafbb-474">**梱包プロファイル ID:** *ソート*</span><span class="sxs-lookup"><span data-stu-id="eafbb-474">**Packing profile ID:** *Sort*</span></span>

1. <span data-ttu-id="eafbb-475">**OK** を選択してダイアログ ボックスを閉じます。</span><span class="sxs-lookup"><span data-stu-id="eafbb-475">Select **OK** to close the dialog box.</span></span>
1. <span data-ttu-id="eafbb-476">**梱包** ページの **ライセンス プレートまたは出荷** フィールドに、販売注文 1 のターゲット LP を入力します。</span><span class="sxs-lookup"><span data-stu-id="eafbb-476">On the **Pack** page, in the **License plate or shipment** field, enter the target LP for sales order 1.</span></span> <span data-ttu-id="eafbb-477">次に、キーボードの **タブ** または **Enter** キーを選択して、フィールドの外に移動します。</span><span class="sxs-lookup"><span data-stu-id="eafbb-477">Then select the **Tab** or **Enter** key on your keyboard to move out of the field.</span></span>
1. <span data-ttu-id="eafbb-478">アクション ウィンドウで、**新規コンテナ―** を選択します。</span><span class="sxs-lookup"><span data-stu-id="eafbb-478">On the Action Pane, select **New container**.</span></span>
1. <span data-ttu-id="eafbb-479">既定の設定をすべて受け入れ、**OK** をクリックします。</span><span class="sxs-lookup"><span data-stu-id="eafbb-479">Accept all the default settings, and select **OK**.</span></span> <span data-ttu-id="eafbb-480">コンテナ― ID をメモします。</span><span class="sxs-lookup"><span data-stu-id="eafbb-480">Make a note of the container ID.</span></span>
1. <span data-ttu-id="eafbb-481">**品目の梱包** クイック タブで、次の値を設定します:</span><span class="sxs-lookup"><span data-stu-id="eafbb-481">On the **Item packing** FastTab, set the following values:</span></span>

    - <span data-ttu-id="eafbb-482">**数量:** *1*</span><span class="sxs-lookup"><span data-stu-id="eafbb-482">**Quantity:** *1*</span></span>
    - <span data-ttu-id="eafbb-483">**識別子:** 品目 *A0001*</span><span class="sxs-lookup"><span data-stu-id="eafbb-483">**Identifier:** Item *A0001*</span></span>

1. <span data-ttu-id="eafbb-484">アクション ウィンドウで、**コンテナ―を閉じる** を選択します。</span><span class="sxs-lookup"><span data-stu-id="eafbb-484">On the Action Pane, select **Close container**.</span></span>
1. <span data-ttu-id="eafbb-485">**コンテナを閉じる** ダイアログ ボックスで、**システム重量を取得** を選択して、**総重量** フィールドを更新します。</span><span class="sxs-lookup"><span data-stu-id="eafbb-485">In the **Close container** dialog box, select **Get system weight** to have the system update the **Gross weight** field.</span></span>
1. <span data-ttu-id="eafbb-486">**OK** を選択します。</span><span class="sxs-lookup"><span data-stu-id="eafbb-486">Select **OK**.</span></span> <span data-ttu-id="eafbb-487">コンテナーが *SPRT* 場所に移動され、ソーティングできるようになります。</span><span class="sxs-lookup"><span data-stu-id="eafbb-487">The container is moved to the *SORT* location and is ready for sorting.</span></span>
1. <span data-ttu-id="eafbb-488">2 番目のコンテナーを作成して、販売注文 1 のLP からの 2 番目の品目を新規コンテナーに追加します。</span><span class="sxs-lookup"><span data-stu-id="eafbb-488">Create a second container to add the second item from the LP for sales order 1 to a new container.</span></span>
1. <span data-ttu-id="eafbb-489">アクション ウィンドウで、**新規コンテナ―** を選択します。</span><span class="sxs-lookup"><span data-stu-id="eafbb-489">On the Action Pane, select **New container**.</span></span>
1. <span data-ttu-id="eafbb-490">既定の設定をすべて受け入れ、**OK** をクリックします。</span><span class="sxs-lookup"><span data-stu-id="eafbb-490">Accept all the default settings, and select **OK**.</span></span> <span data-ttu-id="eafbb-491">コンテナ― ID をメモします。</span><span class="sxs-lookup"><span data-stu-id="eafbb-491">Make a note of the container ID.</span></span>
1. <span data-ttu-id="eafbb-492">**品目の梱包** クイック タブで、次の値を設定します:</span><span class="sxs-lookup"><span data-stu-id="eafbb-492">On the **Item packing** FastTab, set the following values:</span></span>

    - <span data-ttu-id="eafbb-493">**数量:** *1*</span><span class="sxs-lookup"><span data-stu-id="eafbb-493">**Quantity:** *1*</span></span>
    - <span data-ttu-id="eafbb-494">**識別子:** 品目 *A0001*</span><span class="sxs-lookup"><span data-stu-id="eafbb-494">**Identifier:** Item *A0001*</span></span>

1. <span data-ttu-id="eafbb-495">アクション ウィンドウで、**コンテナ―を閉じる** を選択します。</span><span class="sxs-lookup"><span data-stu-id="eafbb-495">On the Action Pane, select **Close container**.</span></span>
1. <span data-ttu-id="eafbb-496">**コンテナを閉じる** ダイアログ ボックスで、**システム重量を取得** を選択して、**総重量** フィールドを更新します。</span><span class="sxs-lookup"><span data-stu-id="eafbb-496">In the **Close container** dialog box, select **Get system weight** to have the system update the **Gross weight** field.</span></span>
1. <span data-ttu-id="eafbb-497">**OK** を選択します。</span><span class="sxs-lookup"><span data-stu-id="eafbb-497">Select **OK**.</span></span> <span data-ttu-id="eafbb-498">コンテナーが *SPRT* 場所に移動され、ソーティングできるようになります。</span><span class="sxs-lookup"><span data-stu-id="eafbb-498">The container is moved to the *SORT* location and is ready for sorting.</span></span>

#### <a name="pack-sales-order-2-into-containers"></a><span data-ttu-id="eafbb-499">販売注文 2 をコンテナーに梱包する</span><span class="sxs-lookup"><span data-stu-id="eafbb-499">Pack sales order 2 into containers</span></span>

1. <span data-ttu-id="eafbb-500">**梱包** ページの **ライセンス プレートまたは出荷** フィールドで、販売注文 2 の明細行 1 にターゲット LP を入力します。</span><span class="sxs-lookup"><span data-stu-id="eafbb-500">On the **Pack** page, in the **License plate or shipment** field, enter the target LP for line 1 of sales order 2.</span></span> <span data-ttu-id="eafbb-501">次に、キーボードの **タブ** または **Enter** キーを選択して、フィールドの外に移動します。</span><span class="sxs-lookup"><span data-stu-id="eafbb-501">Then select the **Tab** or **Enter** key on your keyboard to move out of the field.</span></span>
1. <span data-ttu-id="eafbb-502">アクション ウィンドウで、**新規コンテナ―** を選択します。</span><span class="sxs-lookup"><span data-stu-id="eafbb-502">On the Action Pane, select **New container**.</span></span>
1. <span data-ttu-id="eafbb-503">既定の設定をすべて受け入れ、**OK** をクリックします。</span><span class="sxs-lookup"><span data-stu-id="eafbb-503">Accept all the default settings, and select **OK**.</span></span> <span data-ttu-id="eafbb-504">コンテナ― ID をメモします。</span><span class="sxs-lookup"><span data-stu-id="eafbb-504">Make a note of the container ID.</span></span>
1. <span data-ttu-id="eafbb-505">**品目の梱包** クイック タブで、次の値を設定します:</span><span class="sxs-lookup"><span data-stu-id="eafbb-505">On the **Item packing** FastTab, set the following values:</span></span>

    - <span data-ttu-id="eafbb-506">**数量:** *1*</span><span class="sxs-lookup"><span data-stu-id="eafbb-506">**Quantity:** *1*</span></span>
    - <span data-ttu-id="eafbb-507">**識別子:** 品目 *A0001*</span><span class="sxs-lookup"><span data-stu-id="eafbb-507">**Identifier:** Item *A0001*</span></span>

1. <span data-ttu-id="eafbb-508">アクション ウィンドウで、**コンテナ―を閉じる** を選択します。</span><span class="sxs-lookup"><span data-stu-id="eafbb-508">On the Action Pane, select **Close container**.</span></span>
1. <span data-ttu-id="eafbb-509">**コンテナを閉じる** ダイアログ ボックスで、**システム重量を取得** を選択して、**総重量** フィールドを更新します。</span><span class="sxs-lookup"><span data-stu-id="eafbb-509">In the **Close container** dialog box, select **Get system weight** to have the system update the **Gross weight** field.</span></span>
1. <span data-ttu-id="eafbb-510">**OK** を選択します。</span><span class="sxs-lookup"><span data-stu-id="eafbb-510">Select **OK**.</span></span> <span data-ttu-id="eafbb-511">コンテナーが *SPRT* 場所に移動され、ソーティングできるようになります。</span><span class="sxs-lookup"><span data-stu-id="eafbb-511">The container is moved to the *SORT* location and is ready for sorting.</span></span>
1. <span data-ttu-id="eafbb-512">**ライセンス プレートまたは出荷** フィールドで、販売注文 2 の明細行 2 にターゲット LP を入力します。</span><span class="sxs-lookup"><span data-stu-id="eafbb-512">In the **License plate or shipment** field, enter the target LP for line 2 of the sales order 2.</span></span> <span data-ttu-id="eafbb-513">次に、キーボードの **タブ** または **Enter** キーを選択して、フィールドの外に移動します。</span><span class="sxs-lookup"><span data-stu-id="eafbb-513">Then select the **Tab** or **Enter** key on your keyboard to move out of the field.</span></span>
1. <span data-ttu-id="eafbb-514">アクション ウィンドウで、**新規コンテナ―** を選択します。</span><span class="sxs-lookup"><span data-stu-id="eafbb-514">On the Action Pane, select **New container**.</span></span>
1. <span data-ttu-id="eafbb-515">既定の設定をすべて受け入れ、**OK** をクリックします。</span><span class="sxs-lookup"><span data-stu-id="eafbb-515">Accept all the default settings, and select **OK**.</span></span> <span data-ttu-id="eafbb-516">コンテナ― ID をメモします。</span><span class="sxs-lookup"><span data-stu-id="eafbb-516">Make a note of the container ID.</span></span>
1. <span data-ttu-id="eafbb-517">**品目の梱包** クイック タブで、次の値を設定します:</span><span class="sxs-lookup"><span data-stu-id="eafbb-517">On the **Item packing** FastTab, set the following values:</span></span>

    - <span data-ttu-id="eafbb-518">**数量:** *1*</span><span class="sxs-lookup"><span data-stu-id="eafbb-518">**Quantity:** *1*</span></span>
    - <span data-ttu-id="eafbb-519">**識別子フィールド:** 品目 *A0002*</span><span class="sxs-lookup"><span data-stu-id="eafbb-519">**Identifier field:** Item *A0002*</span></span>

1. <span data-ttu-id="eafbb-520">アクション ウィンドウで、**コンテナ―を閉じる** を選択します。</span><span class="sxs-lookup"><span data-stu-id="eafbb-520">On the Action Pane, select **Close container**.</span></span>
1. <span data-ttu-id="eafbb-521">**コンテナを閉じる** ダイアログ ボックスで、**システム重量を取得** を選択して、**総重量** フィールドを更新します。</span><span class="sxs-lookup"><span data-stu-id="eafbb-521">In the **Close container** dialog box, select **Get system weight** to have the system update the **Gross weight** field.</span></span>
1. <span data-ttu-id="eafbb-522">**OK** を選択します。</span><span class="sxs-lookup"><span data-stu-id="eafbb-522">Select **OK**.</span></span> <span data-ttu-id="eafbb-523">コンテナーが *SPRT* 場所に移動され、ソーティングできるようになります。</span><span class="sxs-lookup"><span data-stu-id="eafbb-523">The container is moved to the *SORT* location and is ready for sorting.</span></span>

<span data-ttu-id="eafbb-524">コンテナーの詳細を表示するには、**倉庫管理 \>梱包とコンテナ―詰め \>** の順に移動して、梱包中に作成されたコンテナー ID を検索します。</span><span class="sxs-lookup"><span data-stu-id="eafbb-524">To view the container details, go to **Warehouse management \> Packing and containerization \> Containers**, and search for the container IDs that were created during packing.</span></span>

### <a name="sort-the-containers"></a><span data-ttu-id="eafbb-525">コンテナーのソート</span><span class="sxs-lookup"><span data-stu-id="eafbb-525">Sort the containers</span></span>

> [!IMPORTANT]
> <span data-ttu-id="eafbb-526">アウトバウンド ソーティングをおこなうためにモバイル アプリの **パレット構築** メニュー項目にアクセスすると、**フル** というラベルの付いたボタンが表示されます。</span><span class="sxs-lookup"><span data-stu-id="eafbb-526">When you access the **Pallet build** menu item on the mobile app to do outbound sorting, you will see a button that is labeled **Full**.</span></span> <span data-ttu-id="eafbb-527">*ソートや位置をクローズするために **フル** ボタンを使用しないでください。*</span><span class="sxs-lookup"><span data-stu-id="eafbb-527">*Don't use the **Full** button to sort or close the position.*</span></span>
>
> <span data-ttu-id="eafbb-528">**フル** ボタンは既定で提供されており、無効にしたり、ページから削除したりすることはできません。</span><span class="sxs-lookup"><span data-stu-id="eafbb-528">The **Full** button is provided by default and can't be disabled or removed from the page.</span></span> <span data-ttu-id="eafbb-529">この *アウトバウンド ソーティング* 機能に使用されません。</span><span class="sxs-lookup"><span data-stu-id="eafbb-529">It isn't used for the *Outbound sorting* feature.</span></span>

#### <a name="sort-the-first-container"></a><span data-ttu-id="eafbb-530">最初のコンテナーのソート</span><span class="sxs-lookup"><span data-stu-id="eafbb-530">Sort the first container</span></span>

1. <span data-ttu-id="eafbb-531">モバイル デバイスで、このシナリオに対して作成したユーザー ID (既存のデモ データ ユーザーのユーザー ID) を使用して、倉庫 *62* にログインします。</span><span class="sxs-lookup"><span data-stu-id="eafbb-531">On the mobile device, sign in to warehouse *62* by using the user ID that you created for this scenario (or the user ID of an existing demo data user).</span></span>
1. <span data-ttu-id="eafbb-532">メイン メニューで、**アウトバウンド** を選択します。</span><span class="sxs-lookup"><span data-stu-id="eafbb-532">On the main menu, select **Outbound**.</span></span>
1. <span data-ttu-id="eafbb-533">**アウトバウンド** メニューで、**パレット構築** を選択します。</span><span class="sxs-lookup"><span data-stu-id="eafbb-533">On the **Outbound** menu, select **Pallet build**.</span></span>
1. <span data-ttu-id="eafbb-534">**LP/Con** フィールドで、販売注文 1 に関連付けられている最初のコンテナー ID を入力します。</span><span class="sxs-lookup"><span data-stu-id="eafbb-534">In the **LP/Con** field, enter the first container ID that is associated with sales order 1.</span></span>
1. <span data-ttu-id="eafbb-535">**OK** を選択します。</span><span class="sxs-lookup"><span data-stu-id="eafbb-535">Select **OK**.</span></span>
1. <span data-ttu-id="eafbb-536">現在存在する並べ替え位置がないため、並べ替えの対象を指定する必要があります。</span><span class="sxs-lookup"><span data-stu-id="eafbb-536">Because no sort positions currently exist, you must specify one.</span></span> <span data-ttu-id="eafbb-537">**位置 ID のソート** フィールドに、*SP01* と入力します。</span><span class="sxs-lookup"><span data-stu-id="eafbb-537">In the **Sort position ID** field, enter *SP01*.</span></span>
1. <span data-ttu-id="eafbb-538">現在、ソート位置 *SP01* に関連付けられている LP がありませんので、指定する必要があります。</span><span class="sxs-lookup"><span data-stu-id="eafbb-538">Because no LP is currently associated with sort position *SP01*, you must specify one.</span></span> <span data-ttu-id="eafbb-539">**LP** フィールドに、*PLP01* と入力します。</span><span class="sxs-lookup"><span data-stu-id="eafbb-539">In the **LP** field, enter *PLP01*.</span></span>
1. <span data-ttu-id="eafbb-540">**OK** を選択します。</span><span class="sxs-lookup"><span data-stu-id="eafbb-540">Select **OK**.</span></span>
1. <span data-ttu-id="eafbb-541">ソート位置の検証が有効になっているため、ソート位置 ID を再度入力する必要があります。</span><span class="sxs-lookup"><span data-stu-id="eafbb-541">Because sort position validation is turned on, you must enter the sort position ID again.</span></span> <span data-ttu-id="eafbb-542">**ソート位置 ID** フィールドに、*SP01* と入力します。</span><span class="sxs-lookup"><span data-stu-id="eafbb-542">In the **Sort Position ID** field, enter *SP01*.</span></span>
1. <span data-ttu-id="eafbb-543">**OK** を選択します。</span><span class="sxs-lookup"><span data-stu-id="eafbb-543">Select **OK**.</span></span>

    <span data-ttu-id="eafbb-544">"作業が完了しました" というメッセージを受信します。</span><span class="sxs-lookup"><span data-stu-id="eafbb-544">You receive a "Work completed" message.</span></span>

> [!TIP]
> <span data-ttu-id="eafbb-545">ソート位置と LP を表示するには、**倉庫管理 \> 梱包とコンテナー詰め \> アウトバウンド ソーティング 位置の割り当て** の順に移動します。</span><span class="sxs-lookup"><span data-stu-id="eafbb-545">To view the sort position and the LP in it, go to **Warehouse management \> Packing and containerization \> Outbound sorting position assignments**.</span></span>
>
> <span data-ttu-id="eafbb-546"> **アウトバウンド ソーティング位置の割り当て** ページには、現在有効なすべてのソート位置が表示されます。</span><span class="sxs-lookup"><span data-stu-id="eafbb-546">The **Outbound sorting position assignments** page shows all the sort positions that are currently active.</span></span> <span data-ttu-id="eafbb-547">**ソート位置のトランザクション** フィールドには、各ソート位置に関連付けられている LP と、ソート位置にあるコンテナーが表示されます。</span><span class="sxs-lookup"><span data-stu-id="eafbb-547">The **Sort position transactions** field shows the LP that is associated with each sort position, and the containers that are in the sort position.</span></span> <span data-ttu-id="eafbb-548">現在は 1 つの並べ替え位置が存在し、**ソート位置の基準** クイック タブの **出荷 - 配送業者サービス - 空路** の基準を示します。</span><span class="sxs-lookup"><span data-stu-id="eafbb-548">Notice that one sort position currently exists, and that the **Sort position criteria** FastTab shows a criterion of **Shipment – Carrier service - Air**.</span></span>

#### <a name="sort-the-remaining-containers"></a><span data-ttu-id="eafbb-549">残存コンテナーのソート</span><span class="sxs-lookup"><span data-stu-id="eafbb-549">Sort the remaining containers</span></span>

1. <span data-ttu-id="eafbb-550">モバイル デバイスで、このシナリオに対して作成したユーザー ID (既存のデモ データ ユーザーのユーザー ID) を使用して、倉庫 *62* にログインします。</span><span class="sxs-lookup"><span data-stu-id="eafbb-550">On the mobile device, sign in to warehouse *62* by using the user ID that you created for this scenario (or the user ID of an existing demo data user).</span></span>
1. <span data-ttu-id="eafbb-551">メイン メニューで、**アウトバウンド** を選択します。</span><span class="sxs-lookup"><span data-stu-id="eafbb-551">On the main menu, select **Outbound**.</span></span>
1. <span data-ttu-id="eafbb-552">**アウトバウンド** メニューで、**パレット構築** を選択します。</span><span class="sxs-lookup"><span data-stu-id="eafbb-552">On the **Outbound** menu, select **Pallet build**.</span></span>
1. <span data-ttu-id="eafbb-553">**LP/Con** フィールドで、販売注文 1 に関連付けられている 2 番目のコンテナー ID を入力します。</span><span class="sxs-lookup"><span data-stu-id="eafbb-553">In the **LP/Con** field, enter the second container ID that is associated with sales order 1.</span></span>
1. <span data-ttu-id="eafbb-554">**OK** を選択します。</span><span class="sxs-lookup"><span data-stu-id="eafbb-554">Select **OK**.</span></span> <span data-ttu-id="eafbb-555">ソーティング テンプレートは自動的にソートするように設定されており、基準に一致するソート位置が既に存在するため、自動的に正しいソート位置へとダイレクトされます。</span><span class="sxs-lookup"><span data-stu-id="eafbb-555">Because the sorting template is set up to sort automatically, and a sort position that has matching criteria already exists, you're automatically directed to the correct sort position.</span></span>
1. <span data-ttu-id="eafbb-556">**OK** を選択します。</span><span class="sxs-lookup"><span data-stu-id="eafbb-556">Select **OK**.</span></span>
1. <span data-ttu-id="eafbb-557">ソート位置 ID を確認して、在庫が正しい場所にあることを示します。</span><span class="sxs-lookup"><span data-stu-id="eafbb-557">Confirm the sort position ID to indicate that the inventory is in the correct place.</span></span> <span data-ttu-id="eafbb-558">**ソート位置 ID** フィールドに、*SP01* と入力します。</span><span class="sxs-lookup"><span data-stu-id="eafbb-558">In the **Sort Position ID** field, enter *SP01*.</span></span>
1. <span data-ttu-id="eafbb-559">**OK** を選択します。</span><span class="sxs-lookup"><span data-stu-id="eafbb-559">Select **OK**.</span></span>

    <span data-ttu-id="eafbb-560">作業は、販売注文 1 の 2 番目のコンテナーで完了します。</span><span class="sxs-lookup"><span data-stu-id="eafbb-560">Work is completed on the second container from sales order 1.</span></span> <span data-ttu-id="eafbb-561">次に、残りのコンテナーを販売注文 2 からソートします。</span><span class="sxs-lookup"><span data-stu-id="eafbb-561">You will now sort the remaining containers from sales order 2.</span></span>

1. <span data-ttu-id="eafbb-562">**LP/Con** フィールドに、品目 *A0001* を保持する販売注文 2 からのコンテナーのコンテナー ID を入力します。</span><span class="sxs-lookup"><span data-stu-id="eafbb-562">In the **LP/Con** field, enter the container ID of the container from sales order 2 that holds item *A0001*.</span></span> <span data-ttu-id="eafbb-563">配送業者サービスは異なることから、新規ソート位置を入力し、その位置に LP を割り当てるように求められます。</span><span class="sxs-lookup"><span data-stu-id="eafbb-563">Because the carrier service differs, you're prompted to enter a new sort position and assign an LP to that position.</span></span> <span data-ttu-id="eafbb-564">ソート位置 *SP02* とLP *PLP02* を使用します。</span><span class="sxs-lookup"><span data-stu-id="eafbb-564">Use sort position *SP02* and LP *PLP02*.</span></span>
1. <span data-ttu-id="eafbb-565">**OK** を選択します。</span><span class="sxs-lookup"><span data-stu-id="eafbb-565">Select **OK**.</span></span>
1. <span data-ttu-id="eafbb-566">**ソート位置 ID** フィールドに *SP02* と入力してソート位置を確認します。</span><span class="sxs-lookup"><span data-stu-id="eafbb-566">Confirm the sort position by entering *SP02* in the **Sort Position ID** field.</span></span>
1. <span data-ttu-id="eafbb-567">**OK** を選択します。</span><span class="sxs-lookup"><span data-stu-id="eafbb-567">Select **OK**.</span></span>

    <span data-ttu-id="eafbb-568">作業はこのコンテナーで完了します。</span><span class="sxs-lookup"><span data-stu-id="eafbb-568">Work is completed on the container.</span></span>

1. <span data-ttu-id="eafbb-569">**LP/Con** フィールドに、品目 *A0002* を保持する販売注文 2 からの残存コンテナーのコンテナー ID を入力します。</span><span class="sxs-lookup"><span data-stu-id="eafbb-569">In the **LP/Con** field, enter the container ID for the remaining container from sales order 2 that holds item *A0002*.</span></span> <span data-ttu-id="eafbb-570">配送業者サービスは、販売注文 1 の配送業者サービスと同じであるため、一致条件を持つ既存のソート位置が表示されます。</span><span class="sxs-lookup"><span data-stu-id="eafbb-570">Because the carrier service is the same as the carrier service for sales order 1, the system shows the existing sort position that has matching criteria.</span></span>
1. <span data-ttu-id="eafbb-571">**OK** を選択します。</span><span class="sxs-lookup"><span data-stu-id="eafbb-571">Select **OK**.</span></span>
1. <span data-ttu-id="eafbb-572">**ソート位置 ID** フィールドに *SP01* と入力してソート位置を確認します。</span><span class="sxs-lookup"><span data-stu-id="eafbb-572">Confirm the sort position by entering *SP01* in the **Sort Position ID** field.</span></span>
1. <span data-ttu-id="eafbb-573">**OK** を選択します。</span><span class="sxs-lookup"><span data-stu-id="eafbb-573">Select **OK**.</span></span>

    <span data-ttu-id="eafbb-574">作業はこのコンテナーで完了します。</span><span class="sxs-lookup"><span data-stu-id="eafbb-574">Work is completed on the container.</span></span>

### <a name="close-the-outbound-sorting-positions"></a><span data-ttu-id="eafbb-575">アウトバウンド ソーティング位置を閉じる</span><span class="sxs-lookup"><span data-stu-id="eafbb-575">Close the outbound sorting positions</span></span>

<span data-ttu-id="eafbb-576">すべての在庫がソートされたら、作業を作成する前にその位置を閉じる必要があります。</span><span class="sxs-lookup"><span data-stu-id="eafbb-576">When all inventory has been sorted, the position must be closed before work can be created.</span></span> <span data-ttu-id="eafbb-577">在庫をベイのドアに移動するために、ソート済みの在庫ピッキング作業が作成されます。</span><span class="sxs-lookup"><span data-stu-id="eafbb-577">Sorted inventory picking work will be created to take the inventory to the bay door.</span></span>

#### <a name="close-a-position-from-the-mobile-device"></a><span data-ttu-id="eafbb-578">モバイル デバイスからの位置のクローズ</span><span class="sxs-lookup"><span data-stu-id="eafbb-578">Close a position from the mobile device</span></span>

1. <span data-ttu-id="eafbb-579">モバイル デバイスで、このシナリオに対して作成したユーザー ID (既存のデモ データ ユーザーのユーザー ID) を使用して、倉庫 *62* にログインします。</span><span class="sxs-lookup"><span data-stu-id="eafbb-579">On the mobile device, sign in to warehouse *62* by using the user ID that you created for this scenario (or the user ID of an existing demo data user).</span></span>
1. <span data-ttu-id="eafbb-580">メイン メニューで、**アウトバウンド** を選択します。</span><span class="sxs-lookup"><span data-stu-id="eafbb-580">On the main menu, select **Outbound**.</span></span>
1. <span data-ttu-id="eafbb-581">**アウトバウンド** メニューで、**パレット構築** を選択します。</span><span class="sxs-lookup"><span data-stu-id="eafbb-581">On the **Outbound** menu, select **Pallet build**.</span></span>
1. <span data-ttu-id="eafbb-582">**LP/Con** フィールドで、位置 *SP01* をソートするためにソートされたコンテナー ID を入力します。</span><span class="sxs-lookup"><span data-stu-id="eafbb-582">In the **LP/Con** field, enter a container ID that was sorted to sort position *SP01*.</span></span>
1. <span data-ttu-id="eafbb-583">**OK** を選択します。</span><span class="sxs-lookup"><span data-stu-id="eafbb-583">Select **OK**.</span></span>
1. <span data-ttu-id="eafbb-584">次のメッセージが表示されます: "このコンテナーは既に SP01 位置にソートされています。</span><span class="sxs-lookup"><span data-stu-id="eafbb-584">You receive the following message: "The container is already sorted to position SP01.</span></span> <span data-ttu-id="eafbb-585">この位置を閉じますか?"</span><span class="sxs-lookup"><span data-stu-id="eafbb-585">Close the position?"</span></span> <span data-ttu-id="eafbb-586">**閉じる** を選択します。</span><span class="sxs-lookup"><span data-stu-id="eafbb-586">Select **Close**.</span></span>

    <span data-ttu-id="eafbb-587">作業が完了しました。</span><span class="sxs-lookup"><span data-stu-id="eafbb-587">Work is completed.</span></span>

#### <a name="close-a-position-from-outbound-sorting-position-assignments"></a><span data-ttu-id="eafbb-588">アウトバウンド ソーティング位置割り当てから位置をクローズする</span><span class="sxs-lookup"><span data-stu-id="eafbb-588">Close a position from outbound sorting position assignments</span></span>

1. <span data-ttu-id="eafbb-589">**倉庫管理 \> 梱包とコンテナー詰め \> アウトバウンド ソーティング位置割り当て** の順に移動します。</span><span class="sxs-lookup"><span data-stu-id="eafbb-589">Go to **Warehouse management \> Packing and containerization \> Outbound sorting position assignments**.</span></span>
1. <span data-ttu-id="eafbb-590">左の列で、**SP02** を選択します。</span><span class="sxs-lookup"><span data-stu-id="eafbb-590">In the left column, select **SP02**.</span></span> <span data-ttu-id="eafbb-591">このアウトバウンド ソーティング位置の行は、ユーザーが終了することになります。</span><span class="sxs-lookup"><span data-stu-id="eafbb-591">This outbound sorting position row is the one that you will close.</span></span>
1. <span data-ttu-id="eafbb-592">アクション ウィンドウで、**コンテナー位置** を選択します。</span><span class="sxs-lookup"><span data-stu-id="eafbb-592">On the Action Pane, select **Close position**.</span></span> <span data-ttu-id="eafbb-593">このソーティング位置のレコードが閉じられ、表示されなくなります。</span><span class="sxs-lookup"><span data-stu-id="eafbb-593">The sorting position record is closed and is no longer shown.</span></span>

    > [!TIP]
    > <span data-ttu-id="eafbb-594">すべての終了した位置レコードを表示するには、**終了したものを表示する** チェックボックスをオンにします。</span><span class="sxs-lookup"><span data-stu-id="eafbb-594">To show all closed position records, select the **Show closed** check box.</span></span>

### <a name="sorted-inventory-picking"></a><span data-ttu-id="eafbb-595">並べ替え在庫ピッキング</span><span class="sxs-lookup"><span data-stu-id="eafbb-595">Sorted inventory picking</span></span>

<span data-ttu-id="eafbb-596">ソート済みの在庫のピッキング作業を完了する必要があります。</span><span class="sxs-lookup"><span data-stu-id="eafbb-596">You must complete the sorted inventory picking work.</span></span> <span data-ttu-id="eafbb-597">完了すると、その在庫は販売注文にピッキングされます。</span><span class="sxs-lookup"><span data-stu-id="eafbb-597">When it's completed, the inventory will be picked to the sales order.</span></span> <span data-ttu-id="eafbb-598">その時点で、その他のすべての倉庫プロセスが適用されます。</span><span class="sxs-lookup"><span data-stu-id="eafbb-598">At that point, all other warehouse processes apply.</span></span>

1. <span data-ttu-id="eafbb-599">モバイル デバイスで、このシナリオに対して作成したユーザー ID (既存のデモ データ ユーザーのユーザー ID) を使用して、倉庫 *62* にログインします。</span><span class="sxs-lookup"><span data-stu-id="eafbb-599">On the mobile device, sign in to warehouse *62* by using the user ID that you created for this scenario (or the user ID of an existing demo data user).</span></span>
1. <span data-ttu-id="eafbb-600">メイン メニューで、**アウトバウンド** を選択します。</span><span class="sxs-lookup"><span data-stu-id="eafbb-600">On the main menu, select **Outbound**.</span></span>
1. <span data-ttu-id="eafbb-601">**アウトバウンド** メニューで、**ソートから積荷** を選択します。</span><span class="sxs-lookup"><span data-stu-id="eafbb-601">On the **Outbound** menu, select **Load from Sorting**.</span></span>
1. <span data-ttu-id="eafbb-602">最初のソート位置 *SP01* からターゲット LP の ID を入力します。</span><span class="sxs-lookup"><span data-stu-id="eafbb-602">Enter the target LP ID from the first sort position, *SP01*.</span></span> <span data-ttu-id="eafbb-603">**ID** フィールドを *PLP01* に設定します。</span><span class="sxs-lookup"><span data-stu-id="eafbb-603">Set the **ID** field to *PLP01*.</span></span>
1. <span data-ttu-id="eafbb-604">**OK** を選択します。</span><span class="sxs-lookup"><span data-stu-id="eafbb-604">Select **OK**.</span></span>
1. <span data-ttu-id="eafbb-605">**ソートされた在庫ピッキング: ピッキング** ページには、完了しなければならないピッキング作業が表示されます。</span><span class="sxs-lookup"><span data-stu-id="eafbb-605">The **Sorted inventory picking: Pick** page shows the pick work that must be done.</span></span> <span data-ttu-id="eafbb-606">*SORT* 位置とターゲット LP の *PLP01* からピッキングします。これは、複数の品目が数量 *3* となっています。</span><span class="sxs-lookup"><span data-stu-id="eafbb-606">Pick from the *SORT* location and target LP *PLP01*, which has multiple items and a quantity of *3*.</span></span>
1. <span data-ttu-id="eafbb-607">**OK** を選択します。</span><span class="sxs-lookup"><span data-stu-id="eafbb-607">Select **OK**.</span></span>
1. <span data-ttu-id="eafbb-608">**ソート済み庫のピッキング: プット** ページには、完了しなければならないプット作業が表示されます。</span><span class="sxs-lookup"><span data-stu-id="eafbb-608">The **Sorted inventory picking: Put** page shows the put work that must be done.</span></span> <span data-ttu-id="eafbb-609">*Baydoor* 位置とターゲット LP の *PLP01* にプットします。これは、複数の品目が数量 *3* となっています。</span><span class="sxs-lookup"><span data-stu-id="eafbb-609">Put to the *Baydoor* location and target LP *PLP01*, which has multiple items and a quantity of *3*.</span></span>
1. <span data-ttu-id="eafbb-610">**OK** を選択します。</span><span class="sxs-lookup"><span data-stu-id="eafbb-610">Select **OK**.</span></span>

    <span data-ttu-id="eafbb-611">作業が完了しました。</span><span class="sxs-lookup"><span data-stu-id="eafbb-611">Work is completed.</span></span>

1. <span data-ttu-id="eafbb-612">2 番目のソート位置 *SP02* からターゲット ライセンス プレート の ID を入力します。</span><span class="sxs-lookup"><span data-stu-id="eafbb-612">Enter the target license plate ID from the second sort position, *SP02*.</span></span> <span data-ttu-id="eafbb-613">**ID** フィールドを *PLP02* に設定します。</span><span class="sxs-lookup"><span data-stu-id="eafbb-613">Set the **ID** field to *PLP02*.</span></span>
1. <span data-ttu-id="eafbb-614">**OK** を選択します。</span><span class="sxs-lookup"><span data-stu-id="eafbb-614">Select **OK**.</span></span>
1. <span data-ttu-id="eafbb-615">**ソートされた在庫ピッキング: ピッキング** ページには、完了しなければならないピッキング作業が表示されます。</span><span class="sxs-lookup"><span data-stu-id="eafbb-615">The **Sorted inventory picking: Pick** page shows the pick work that must be done.</span></span> <span data-ttu-id="eafbb-616">*SORT* 位置とターゲット LP の *PLP02* からピッキングします。これは、複数の品目が数量 *1* となっています。</span><span class="sxs-lookup"><span data-stu-id="eafbb-616">Pick from the *SORT* location and target LP *PLP02*, which has multiple items and a quantity of *1*.</span></span>
1. <span data-ttu-id="eafbb-617">**OK** を選択します。</span><span class="sxs-lookup"><span data-stu-id="eafbb-617">Select **OK**.</span></span>
1. <span data-ttu-id="eafbb-618">**ソート済み庫のピッキング: プット** ページには、完了しなければならないプット作業が表示されます。</span><span class="sxs-lookup"><span data-stu-id="eafbb-618">The **Sorted inventory picking: Put** page shows the put work that must be done.</span></span> <span data-ttu-id="eafbb-619">*Baydoor* 位置とターゲット LP の *PLP02* にプットします。これは、複数の品目が数量 *1* となっています。</span><span class="sxs-lookup"><span data-stu-id="eafbb-619">Put to the *Baydoor* location and target LP *PLP02*, which has multiple items and a quantity of *1*.</span></span>
1. <span data-ttu-id="eafbb-620">**OK** を選択します。</span><span class="sxs-lookup"><span data-stu-id="eafbb-620">Select **OK**.</span></span>

    <span data-ttu-id="eafbb-621">作業が完了しました。</span><span class="sxs-lookup"><span data-stu-id="eafbb-621">Work is completed.</span></span>

<span data-ttu-id="eafbb-622">この時点から先は、その他のすべての倉庫プロセスが適用されます。</span><span class="sxs-lookup"><span data-stu-id="eafbb-622">From this point forward, all other warehouse processes apply.</span></span>
