---
title: プットアウェイ クラスター
description: プットアウェイ クラスターには、複数のライセンス プレートを同時に選択し、異なる場所にある複数のライセンス プレートを使用する方法が用意されています。 プットアウェイ クラスターは、ライセンス プレートが在庫のパレット数が少ない小売業の場合に非常に役立ちます。
author: Mirzaab
manager: tfehr
ms.date: 10/19/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: mirzaab
ms.search.validFrom: 2020-10-19
ms.dyn365.ops.version: Release 10.0.7
ms.openlocfilehash: 6a330ddccbd17c92443232fc8488e36a59235773
ms.sourcegitcommit: cfd84321fba38e02e270d361df369a536a48efa3
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 11/11/2020
ms.locfileid: "4512333"
---
# <a name="putaway-clusters"></a><span data-ttu-id="9e9fa-104">プットアウェイ クラスター</span><span class="sxs-lookup"><span data-stu-id="9e9fa-104">Putaway clusters</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="9e9fa-105">プットアウェイ クラスターには、複数のライセンス プレートを同時に選択し、異なる場所にある複数のライセンス プレートを使用する方法が用意されています。</span><span class="sxs-lookup"><span data-stu-id="9e9fa-105">Putaway clusters offer a way to pick multiple license plates at the same time and then take them for putaway in different locations.</span></span> <span data-ttu-id="9e9fa-106">このプロセスは、*ミルク ラン* と呼ばれます。</span><span class="sxs-lookup"><span data-stu-id="9e9fa-106">This process is often referred to as a *milk run*.</span></span> <span data-ttu-id="9e9fa-107">プットアウェイ クラスターは、ライセンス プレートが在庫のパレット数が少ない小売業の場合に非常に役立ちます。</span><span class="sxs-lookup"><span data-stu-id="9e9fa-107">Putaway clusters can be very useful for retail businesses, where license plates typically aren't full pallets of inventory.</span></span> 

## <a name="turn-on-the-cluster-putaway-feature"></a><span data-ttu-id="9e9fa-108">クラスター プットアウェイ機能をオンにする</span><span class="sxs-lookup"><span data-stu-id="9e9fa-108">Turn on the cluster putaway feature</span></span>

<span data-ttu-id="9e9fa-109">この機能を使用するには、システム上で有効にする必要があります。</span><span class="sxs-lookup"><span data-stu-id="9e9fa-109">Before you can use this feature, it must be turned on in your system.</span></span> <span data-ttu-id="9e9fa-110">管理者は、[機能の管理](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) ワークスペースを使用して、機能の状態を確認し、必要に応じて有効にすることができます。</span><span class="sxs-lookup"><span data-stu-id="9e9fa-110">Admins can use the [Feature management](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) workspace to check the status of the feature and turn it on if it's required.</span></span> <span data-ttu-id="9e9fa-111">この機能は、次のようにして表示されます。</span><span class="sxs-lookup"><span data-stu-id="9e9fa-111">There, the feature is listed in the following way:</span></span>

- <span data-ttu-id="9e9fa-112">**モジュール:** *倉庫管理*</span><span class="sxs-lookup"><span data-stu-id="9e9fa-112">**Module:** *Warehouse management*</span></span>
- <span data-ttu-id="9e9fa-113">**機能名:** *クラスター プットアウェイ機能*</span><span class="sxs-lookup"><span data-stu-id="9e9fa-113">**Feature name:** *Cluster putaway feature*</span></span>

## <a name="setup-for-the-example-scenario"></a><span data-ttu-id="9e9fa-114">サンプル シナリオで設定する</span><span class="sxs-lookup"><span data-stu-id="9e9fa-114">Setup for the example scenario</span></span>

### <a name="cluster-profiles"></a><span data-ttu-id="9e9fa-115">クラスター プロファイル</span><span class="sxs-lookup"><span data-stu-id="9e9fa-115">Cluster profiles</span></span>

<span data-ttu-id="9e9fa-116">クラスター プロファイルは、入庫時に品目に割り当てられている場所に基づいて、品目の移動先を決定します。</span><span class="sxs-lookup"><span data-stu-id="9e9fa-116">The putaway cluster profile determines where an item will go, based on the location that is assigned to the item at the time of receipt.</span></span> <span data-ttu-id="9e9fa-117">異なるクラスターが必要な場合は、モバイル デバイスのメニュー項目ごとに異なるプットアウェイ クラスター機能を作成する必要があります。</span><span class="sxs-lookup"><span data-stu-id="9e9fa-117">If different clusters are required, different putaway clusters should be created, one for each mobile device menu item.</span></span>

1. <span data-ttu-id="9e9fa-118">**倉庫管理 \> 設定 \> モバイル デバイス \> クラスター プロファイル** の順に移動します。</span><span class="sxs-lookup"><span data-stu-id="9e9fa-118">Go to **Warehouse management \> Setup \> Mobile device \> Cluster profiles**.</span></span>
1. <span data-ttu-id="9e9fa-119">アクション ウィンドウで、**新規** を選択します。</span><span class="sxs-lookup"><span data-stu-id="9e9fa-119">On the Action Pane, select **New**.</span></span>
1. <span data-ttu-id="9e9fa-120">**ヘッダー** ビューで、次の値を設定します:</span><span class="sxs-lookup"><span data-stu-id="9e9fa-120">In the **Header** view, set the following values:</span></span>

    - <span data-ttu-id="9e9fa-121">**プットアウェイ クラスター プロファイル ID:** *クラスター プットアウェイ*</span><span class="sxs-lookup"><span data-stu-id="9e9fa-121">**Putaway cluster profile ID:** *Cluster putaway*</span></span>
    - <span data-ttu-id="9e9fa-122">**プットアウェイ クラスター プロファイル ID 名:** *クラスター プットアウェイ*</span><span class="sxs-lookup"><span data-stu-id="9e9fa-122">**Putaway cluster profile ID Name:** *Cluster putaway*</span></span>
    - <span data-ttu-id="9e9fa-123">**クラスター タイプ:** *プットアウェイ*</span><span class="sxs-lookup"><span data-stu-id="9e9fa-123">**Cluster type:** *Putaway*</span></span>
    - <span data-ttu-id="9e9fa-124">**シーケンス番号:** 規定値を受け入れます。</span><span class="sxs-lookup"><span data-stu-id="9e9fa-124">**Sequence number:** Accept the default value.</span></span>

1. <span data-ttu-id="9e9fa-125">**保存** を選択して、**全般** クイック タブで必要なフィールドを使用できるようにします。</span><span class="sxs-lookup"><span data-stu-id="9e9fa-125">Select **Save** to make the required fields on the **General** FastTab available.</span></span>
1. <span data-ttu-id="9e9fa-126">**一般** クイック タブで、次の値を設定します。</span><span class="sxs-lookup"><span data-stu-id="9e9fa-126">On the **General** FastTab, set the following values:</span></span>

    - <span data-ttu-id="9e9fa-127">**クラスターの割り当てのタイミング:** *入庫時*</span><span class="sxs-lookup"><span data-stu-id="9e9fa-127">**Cluster assignment timing:** *At receipt*</span></span>

        <span data-ttu-id="9e9fa-128">このフィールドでは、在庫の入庫時に直ちにこのクラスターを割り当てるか、後で並べ替えるかを定義します。</span><span class="sxs-lookup"><span data-stu-id="9e9fa-128">This field defines whether the putaway cluster should be assigned immediately when the inventory is received, or whether it should be sorted later.</span></span>

    - <span data-ttu-id="9e9fa-129">**クラスターの割り当てルール:** *手動*</span><span class="sxs-lookup"><span data-stu-id="9e9fa-129">**Cluster assignment rule:** *Manual*</span></span>

        <span data-ttu-id="9e9fa-130">このフィールドは、クラスターの割り当てをシステムが自動的に指定するか、ユーザーが手動で指定するかを定義します。</span><span class="sxs-lookup"><span data-stu-id="9e9fa-130">This field defines whether the cluster assignment should be determined automatically by the system or manually by the user.</span></span>

    - <span data-ttu-id="9e9fa-131">**ディレクティブ コード:** このフィールドは空白のままにします。</span><span class="sxs-lookup"><span data-stu-id="9e9fa-131">**Directive code:** Leave this field blank.</span></span>
    - <span data-ttu-id="9e9fa-132">**プットアウェイ クラスターの場所:** *入庫*</span><span class="sxs-lookup"><span data-stu-id="9e9fa-132">**Putaway cluster locate:** *Receipt*</span></span>

        <span data-ttu-id="9e9fa-133">使用可能な値は次のとおりです。</span><span class="sxs-lookup"><span data-stu-id="9e9fa-133">The following values are available:</span></span>

        - <span data-ttu-id="9e9fa-134">**入庫** – 場所は入庫時にすぐに検出されます。</span><span class="sxs-lookup"><span data-stu-id="9e9fa-134">**Receipt** – A location is found immediately during receipt.</span></span>
        - <span data-ttu-id="9e9fa-135">**クラスターの終了** – 場所はクラスターが終了するときに検出されます。</span><span class="sxs-lookup"><span data-stu-id="9e9fa-135">**Cluster close** – A location is found when the cluster is closed.</span></span>
        - <span data-ttu-id="9e9fa-136">**ユーザー主導** – ライセンス プレートがクラスターから選択されたときに、その場所が検出されます。</span><span class="sxs-lookup"><span data-stu-id="9e9fa-136">**User directed** – A location is found when the license plate is picked from the cluster for putaway.</span></span> <span data-ttu-id="9e9fa-137">この場合、プットアウェイ作業の作成時には場所が指定されません。</span><span class="sxs-lookup"><span data-stu-id="9e9fa-137">In this case, no location is specified when the putaway work is created.</span></span> <span data-ttu-id="9e9fa-138">プットアウェイの間に、ユーザーはナンバー プレートまたは作業 ID をスキャンしてプット ステップを開始する必要があります。</span><span class="sxs-lookup"><span data-stu-id="9e9fa-138">During the putaway itself, the user must scan the license plate or work ID to initiate the put step.</span></span> <span data-ttu-id="9e9fa-139">次に、プット場所が再度検索され、選択した数量のプット場所がユーザーに通知されます。</span><span class="sxs-lookup"><span data-stu-id="9e9fa-139">The system then finds the put location again and tells the user where to put the picked quantity.</span></span>

    - <span data-ttu-id="9e9fa-140">**ユーザーごとのプットアウェイ クラスター:** *いいえ*</span><span class="sxs-lookup"><span data-stu-id="9e9fa-140">**Putaway cluster per user:** *No*</span></span>

        <span data-ttu-id="9e9fa-141">このフィールドは、クラスターが自動的に割り当てられる場合に、各クラスターをユーザーごとに一意にするかどうかを定義します。</span><span class="sxs-lookup"><span data-stu-id="9e9fa-141">This field defines whether each cluster should be unique per user when clusters are automatically assigned.</span></span> <span data-ttu-id="9e9fa-142">**クラスター割り当てルール** フィールドが *自動* に設定されている場合にのみ使用できます。</span><span class="sxs-lookup"><span data-stu-id="9e9fa-142">It's available only when the **Cluster assignment rule** field is set to *Automatic*.</span></span>

    - <span data-ttu-id="9e9fa-143">**単位の制限:** このフィールドは空白のままにします。</span><span class="sxs-lookup"><span data-stu-id="9e9fa-143">**Unit restriction:** Leave this field blank.</span></span>

        <span data-ttu-id="9e9fa-144">このフィールドでは、プロファイルを有効にするために受け取る必要がある単位を定義します。</span><span class="sxs-lookup"><span data-stu-id="9e9fa-144">This field defines the unit that must be received for the profile to be valid.</span></span> <span data-ttu-id="9e9fa-145">空白のままにすると、すべての単位が有効になります。</span><span class="sxs-lookup"><span data-stu-id="9e9fa-145">If it's left blank, all units are valid.</span></span>

    - <span data-ttu-id="9e9fa-146">**作業単位ブレーク:** *個別*</span><span class="sxs-lookup"><span data-stu-id="9e9fa-146">**Work unit break:** *Individual*</span></span>

        <span data-ttu-id="9e9fa-147">このフィールドでは、クラスターを閉じたときにすべての在庫を 1 つのライセンス プレートに統合する (クラスター ID とライセンス プレートを使用) か、または、入庫したライセンスのプレートで 1 つのライセンス プレートとして、すべての在庫を個別にするか、または別にするかを定義します。</span><span class="sxs-lookup"><span data-stu-id="9e9fa-147">This field defines whether all inventory should be consolidated (by using the cluster ID and the license plate) onto one license plate when a cluster is closed, and whether it should be put away as a single license plate or separately on the license plates that were received.</span></span> <span data-ttu-id="9e9fa-148">このフィールドは、**プットアウェイ クラスターの場所** フィールドが *入庫* に設定されている場合は使用できません。</span><span class="sxs-lookup"><span data-stu-id="9e9fa-148">This field is unavailable when the **Putaway cluster locate** field is set to *Receipt*.</span></span>

    - <span data-ttu-id="9e9fa-149">**クラスターを親ライセンス プレートとして保持する:** *いいえ*</span><span class="sxs-lookup"><span data-stu-id="9e9fa-149">**Cluster persists as Parent License Plate:** *No*</span></span>

        <span data-ttu-id="9e9fa-150">このオプションが *はい* に設定されている場合は、プット手順が完了すると、クラスター ID が親ライセンス プレートになり、クラスター ID のすべての品目がその親ライセンス プレートにリンクされます。</span><span class="sxs-lookup"><span data-stu-id="9e9fa-150">If this option is set to *Yes*, when the put step is completed, the cluster ID will become a parent license plate, and all items on the cluster ID will be linked to that parent license plate.</span></span>

1. <span data-ttu-id="9e9fa-151">**クラスターの並べ替え** クイック タブでは、プットアウェイの並べ替え基準を定義できます。</span><span class="sxs-lookup"><span data-stu-id="9e9fa-151">On the **Cluster sorting** FastTab, you can define putaway sorting criteria.</span></span> <span data-ttu-id="9e9fa-152">ツールバーで **新規** を選択して明細行を追加し、それに次の値を設定します:</span><span class="sxs-lookup"><span data-stu-id="9e9fa-152">Select **New** on the toolbar to add a line, and then set the following values:</span></span>

    - <span data-ttu-id="9e9fa-153">**シーケンス番号:** 規定値を受け入れます。</span><span class="sxs-lookup"><span data-stu-id="9e9fa-153">**Sequence number:** Accept the default value.</span></span>
    - <span data-ttu-id="9e9fa-154">**フィールド名:** *WMSLocationId*</span><span class="sxs-lookup"><span data-stu-id="9e9fa-154">**Field name:** *WMSLocationId*</span></span>

        <span data-ttu-id="9e9fa-155">このフィールドは、この明細行で並べ替え基準として使用するフィールドを定義します。</span><span class="sxs-lookup"><span data-stu-id="9e9fa-155">This field defines the field that this line should use as a sorting criterion.</span></span>

    - <span data-ttu-id="9e9fa-156">**並べ替え:** *昇順*</span><span class="sxs-lookup"><span data-stu-id="9e9fa-156">**Sorting:** *Ascending*</span></span>

        <span data-ttu-id="9e9fa-157">このフィールドでは、並べ替えを昇順と降順のどちらで行うかを定義します。</span><span class="sxs-lookup"><span data-stu-id="9e9fa-157">This field defines whether sorting should be done in ascending or descending order.</span></span>

1. <span data-ttu-id="9e9fa-158">**クラスター作業テンプレート** クイック タブのツールバーで **新規** を選択して明細行を追加し、次の値を設定します:</span><span class="sxs-lookup"><span data-stu-id="9e9fa-158">On the **Cluster work template** FastTab, select **New** on the toolbar to add a line, and then set the following values:</span></span>

    - <span data-ttu-id="9e9fa-159">**作業指示タイプ:** *発注書*</span><span class="sxs-lookup"><span data-stu-id="9e9fa-159">**Work order type:** *Purchase orders*</span></span>
    - <span data-ttu-id="9e9fa-160">**作業テンプレート:** *61 PO Direct*</span><span class="sxs-lookup"><span data-stu-id="9e9fa-160">**Work template:** *61 PO Direct*</span></span>

1. <span data-ttu-id="9e9fa-161">アクション ペインで、**保存** を選択し、**クエリの編集** を選択します。</span><span class="sxs-lookup"><span data-stu-id="9e9fa-161">On the Action Pane, select **Save**, and then select **Edit query**.</span></span>
1. <span data-ttu-id="9e9fa-162">**クラスター プットアウェイ** ダイアログ ボックスの **範囲** タブで **追加** を選択して、2 番目の明細行にクエリを追加します。</span><span class="sxs-lookup"><span data-stu-id="9e9fa-162">In the **Cluster putaway** dialog box, on the **Range** tab, select **Add** to add a second line to the query.</span></span> <span data-ttu-id="9e9fa-163">次の表に示すように、クエリ行を更新します。</span><span class="sxs-lookup"><span data-stu-id="9e9fa-163">Then update the query lines as shown in the following table.</span></span>

    | <span data-ttu-id="9e9fa-164">テーブル</span><span class="sxs-lookup"><span data-stu-id="9e9fa-164">Table</span></span> | <span data-ttu-id="9e9fa-165">派生テーブル</span><span class="sxs-lookup"><span data-stu-id="9e9fa-165">Derived table</span></span> | <span data-ttu-id="9e9fa-166">フィールド</span><span class="sxs-lookup"><span data-stu-id="9e9fa-166">Field</span></span> | <span data-ttu-id="9e9fa-167">基準</span><span class="sxs-lookup"><span data-stu-id="9e9fa-167">Criteria</span></span> |
    |---|---|---|---|
    | <span data-ttu-id="9e9fa-168">作業</span><span class="sxs-lookup"><span data-stu-id="9e9fa-168">Work</span></span> | <span data-ttu-id="9e9fa-169">作業</span><span class="sxs-lookup"><span data-stu-id="9e9fa-169">Work</span></span> | <span data-ttu-id="9e9fa-170">倉庫</span><span class="sxs-lookup"><span data-stu-id="9e9fa-170">Warehouse</span></span> | <span data-ttu-id="9e9fa-171">*61*</span><span class="sxs-lookup"><span data-stu-id="9e9fa-171">*61*</span></span> |
    | <span data-ttu-id="9e9fa-172">作業</span><span class="sxs-lookup"><span data-stu-id="9e9fa-172">Work</span></span> | <span data-ttu-id="9e9fa-173">作業</span><span class="sxs-lookup"><span data-stu-id="9e9fa-173">Work</span></span> | <span data-ttu-id="9e9fa-174">作業 ID</span><span class="sxs-lookup"><span data-stu-id="9e9fa-174">Work ID</span></span> | <span data-ttu-id="9e9fa-175">このフィールドは空白のままにします。</span><span class="sxs-lookup"><span data-stu-id="9e9fa-175">Leave this field blank.</span></span> |

1. <span data-ttu-id="9e9fa-176">**OK** を選択してクエリを保存し、ダイアログ ボックスを閉じます。</span><span class="sxs-lookup"><span data-stu-id="9e9fa-176">Select **OK** to save the query and close the dialog box.</span></span>
1. <span data-ttu-id="9e9fa-177">アクション ペインで **保存** を選択し、ページを閉じます。</span><span class="sxs-lookup"><span data-stu-id="9e9fa-177">On the Action Pane, select **Save**, and close the page.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="9e9fa-178">**クラスター ID の生成** が *はい* に設定されている場合に淡色表示されているクラスター プロファイルのフィールドは、この機能が使用された場合には考慮されません。</span><span class="sxs-lookup"><span data-stu-id="9e9fa-178">Fields in the cluster profile that appear dimmed when **Generate cluster ID** is set to *Yes* are unavailable and won't be considered when this feature is used.</span></span>

### <a name="mobile-device-menu-items"></a><span data-ttu-id="9e9fa-179">モバイル デバイスのメニュー品目</span><span class="sxs-lookup"><span data-stu-id="9e9fa-179">Mobile device menu items</span></span>

<span data-ttu-id="9e9fa-180">この機能には、2 つの新しいモバイル デバイス メニュー項目が用意されています。</span><span class="sxs-lookup"><span data-stu-id="9e9fa-180">Two new mobile device menu items are available for this feature.</span></span> <span data-ttu-id="9e9fa-181">**クラスターの入庫と並べ替え** メニュー項目は、入庫時に受信した在庫をプットアウェイ クラスターに分類するために使用されます。</span><span class="sxs-lookup"><span data-stu-id="9e9fa-181">The **Receive and sort cluster** menu item is used to sort the received inventory into a putaway cluster upon receipt.</span></span> <span data-ttu-id="9e9fa-182">**クラスター プットアウェイ** メニュー項目は、割り当て後にクラスターを使用しないようにするために使用されます。</span><span class="sxs-lookup"><span data-stu-id="9e9fa-182">The **Cluster putaway** menu item is used to put the cluster away after it has been assigned.</span></span>

#### <a name="receive-and-sort-cluster"></a><span data-ttu-id="9e9fa-183">クラスターの入庫と並べ替え</span><span class="sxs-lookup"><span data-stu-id="9e9fa-183">Receive and sort cluster</span></span>

<span data-ttu-id="9e9fa-184">在庫を受け取ってクラスターに分類するための新しいモバイル デバイス メニュー項目を作成します。</span><span class="sxs-lookup"><span data-stu-id="9e9fa-184">Create a new mobile device menu item for receiving inventory and sorting into a cluster.</span></span> <span data-ttu-id="9e9fa-185">このメニュー項目は、在庫の受信後に入庫時の作業を作成します。これは、入庫メニュー項目がプットアウェイ クラスターで使用されることを示します。</span><span class="sxs-lookup"><span data-stu-id="9e9fa-185">This menu item will create inbound work after inventory is received, which indicates that the receiving menu item will be used for putaway clusters.</span></span>

> [!NOTE]
> <span data-ttu-id="9e9fa-186">**クラスターの入庫と並べ替え** メニュー項目は、次の入庫メニュー項目で使用できます:</span><span class="sxs-lookup"><span data-stu-id="9e9fa-186">The **Receive and sort cluster** menu item can be used with the following receiving menu items:</span></span>
>
> - <span data-ttu-id="9e9fa-187">発注書明細行受取</span><span class="sxs-lookup"><span data-stu-id="9e9fa-187">Purchase order line receiving</span></span>
> - <span data-ttu-id="9e9fa-188">発注書品目受取</span><span class="sxs-lookup"><span data-stu-id="9e9fa-188">Purchase order item receiving</span></span>
> - <span data-ttu-id="9e9fa-189">積荷品目入庫</span><span class="sxs-lookup"><span data-stu-id="9e9fa-189">Load item receiving</span></span>

1. <span data-ttu-id="9e9fa-190">**倉庫管理 \> 設定 \> モバイル デバイス \> モバイル デバイスのメニュー品目** の順に移動します。</span><span class="sxs-lookup"><span data-stu-id="9e9fa-190">Go to **Warehouse management \> Setup \> Mobile device \> Mobile device menu items**.</span></span>
1. <span data-ttu-id="9e9fa-191">アクション ウィンドウで、**新規** を選択します。</span><span class="sxs-lookup"><span data-stu-id="9e9fa-191">On the Action Pane, select **New**.</span></span>
1. <span data-ttu-id="9e9fa-192">**ヘッダー** ビューで、次の値を設定します:</span><span class="sxs-lookup"><span data-stu-id="9e9fa-192">In the **Header** view, set the following values:</span></span>

    - <span data-ttu-id="9e9fa-193">**メニュー項目名:** *クラスターの入庫と並べ替え*</span><span class="sxs-lookup"><span data-stu-id="9e9fa-193">**Menu item name:** *Receive and sort cluster*</span></span>
    - <span data-ttu-id="9e9fa-194">**タイトル:** *クラスターの入庫と並べ替え*</span><span class="sxs-lookup"><span data-stu-id="9e9fa-194">**Title:** *Receive and sort cluster*</span></span>
    - <span data-ttu-id="9e9fa-195">**モード:** *作業*</span><span class="sxs-lookup"><span data-stu-id="9e9fa-195">**Mode:** *Work*</span></span>
    - <span data-ttu-id="9e9fa-196">**既存の作業を使用する :** *いいえ*</span><span class="sxs-lookup"><span data-stu-id="9e9fa-196">**Use existing work:** *No*</span></span>

1. <span data-ttu-id="9e9fa-197">**一般** クイック タブで、次の値を設定します。</span><span class="sxs-lookup"><span data-stu-id="9e9fa-197">On the **General** FastTab, set the following values:</span></span>

    - <span data-ttu-id="9e9fa-198">**作業作成プロセス:** *発注書品目の入庫*</span><span class="sxs-lookup"><span data-stu-id="9e9fa-198">**Work creation process:** *Purchase order item receiving*</span></span>
    - <span data-ttu-id="9e9fa-199">**ライセンスプレートの生成:** *はい*</span><span class="sxs-lookup"><span data-stu-id="9e9fa-199">**Generate license plate:** *Yes*</span></span>
    - <span data-ttu-id="9e9fa-200">**プットアウェイ クラスターの割り当て:** *はい*</span><span class="sxs-lookup"><span data-stu-id="9e9fa-200">**Assign putaway cluster:** *Yes*</span></span>

        > [!NOTE]
        > <span data-ttu-id="9e9fa-201">**プットアウェイ クラスターを割り当てる** オプションは、1 回の手順の入庫 *作業の作成プロセス* にのみ使用でき ます。</span><span class="sxs-lookup"><span data-stu-id="9e9fa-201">The **Assign putaway cluster** option is available only for the one-step *Work creation process* activity for receiving.</span></span>

    <span data-ttu-id="9e9fa-202">残りのフィールドに対しては規定値を受け入れます。</span><span class="sxs-lookup"><span data-stu-id="9e9fa-202">Accept the default values for the remaining fields.</span></span>

1. <span data-ttu-id="9e9fa-203">アクション ウィンドウで、**保存** を選択します。</span><span class="sxs-lookup"><span data-stu-id="9e9fa-203">On the Action Pane, select **Save**.</span></span>

#### <a name="cluster-putaway"></a><span data-ttu-id="9e9fa-204">クラスター プットアウェイ</span><span class="sxs-lookup"><span data-stu-id="9e9fa-204">Cluster putaway</span></span>

<span data-ttu-id="9e9fa-205">割り当て後にクラスターを終了するための新しいモバイル デバイス メニュー項目を作成します。</span><span class="sxs-lookup"><span data-stu-id="9e9fa-205">Create a new mobile device menu item for putting the cluster away after it has been assigned.</span></span>

1. <span data-ttu-id="9e9fa-206">**倉庫管理 \> 設定 \> モバイル デバイス \> モバイル デバイスのメニュー品目** の順に移動します。</span><span class="sxs-lookup"><span data-stu-id="9e9fa-206">Go to **Warehouse management \> Setup \> Mobile device \> Mobile device menu items**.</span></span>
1. <span data-ttu-id="9e9fa-207">アクション ウィンドウで、**新規** を選択します。</span><span class="sxs-lookup"><span data-stu-id="9e9fa-207">On the Action Pane, select **New**.</span></span>
1. <span data-ttu-id="9e9fa-208">**ヘッダー** ビューで、次の値を設定します:</span><span class="sxs-lookup"><span data-stu-id="9e9fa-208">In the **Header** view, set the following values:</span></span>

    - <span data-ttu-id="9e9fa-209">**メニュー項目の名前:** *クラスター プットアウェイ*</span><span class="sxs-lookup"><span data-stu-id="9e9fa-209">**Menu item name:** *Cluster putaway*</span></span>
    - <span data-ttu-id="9e9fa-210">**タイトル:** *クラスター プットアウェイ*</span><span class="sxs-lookup"><span data-stu-id="9e9fa-210">**Title:** *Cluster putaway*</span></span>
    - <span data-ttu-id="9e9fa-211">**モード:** *作業*</span><span class="sxs-lookup"><span data-stu-id="9e9fa-211">**Mode:** *Work*</span></span>
    - <span data-ttu-id="9e9fa-212">**既存の作業を使用:** *はい*</span><span class="sxs-lookup"><span data-stu-id="9e9fa-212">**Use existing work:** *Yes*</span></span>

1. <span data-ttu-id="9e9fa-213">**全般** クイック タブで、**指示者** フィールドを *クラスター プットアウェイ* に設定します。</span><span class="sxs-lookup"><span data-stu-id="9e9fa-213">On the **General** FastTab, set the **Directed by** field to *Cluster putaway*.</span></span> <span data-ttu-id="9e9fa-214">残りのフィールドに対しては規定値を受け入れます。</span><span class="sxs-lookup"><span data-stu-id="9e9fa-214">Accept the default values for the remaining fields.</span></span>
1. <span data-ttu-id="9e9fa-215">**作業クラス** クイック タブで、このモバイル デバイスのメニュー品目に有効な作業クラスを設定します。</span><span class="sxs-lookup"><span data-stu-id="9e9fa-215">On the **Work classes** FastTab, set up the valid work class for this mobile device menu item:</span></span>

    - <span data-ttu-id="9e9fa-216">**作業クラス ID:** *購入*</span><span class="sxs-lookup"><span data-stu-id="9e9fa-216">**Work class ID:** *Purchase*</span></span>
    - <span data-ttu-id="9e9fa-217">**作業指示タイプ:** *発注書*</span><span class="sxs-lookup"><span data-stu-id="9e9fa-217">**Work order type:** *Purchase orders*</span></span>

1. <span data-ttu-id="9e9fa-218">アクション ウィンドウで、**保存** を選択します。</span><span class="sxs-lookup"><span data-stu-id="9e9fa-218">On the Action Pane, select **Save**.</span></span>

### <a name="mobile-device-menu"></a><span data-ttu-id="9e9fa-219">モバイル デバイスのメニュー</span><span class="sxs-lookup"><span data-stu-id="9e9fa-219">Mobile device menu</span></span>

<span data-ttu-id="9e9fa-220">作成したばかりのメニュー項目をモバイル アプリの入庫メニューに追加します。</span><span class="sxs-lookup"><span data-stu-id="9e9fa-220">Add the menu items that you just created to the inbound menu of the mobile app.</span></span>

1. <span data-ttu-id="9e9fa-221">**倉庫管理 \> 設定 \> モバイル デバイス \> モバイル デバイス メニュー** の順に移動します。</span><span class="sxs-lookup"><span data-stu-id="9e9fa-221">Go to **Warehouse management \> Setup \> Mobile device \> Mobile device menu**.</span></span>
1. <span data-ttu-id="9e9fa-222">アクション ウィンドウで、**編集** を選択します。</span><span class="sxs-lookup"><span data-stu-id="9e9fa-222">On the Action Pane, select **Edit**.</span></span>
1. <span data-ttu-id="9e9fa-223">メニューの一覧で **入庫** を選択します。</span><span class="sxs-lookup"><span data-stu-id="9e9fa-223">In the menu list, select **Inbound**.</span></span>
1. <span data-ttu-id="9e9fa-224">**使用可能なメニューとメニュー項目** の一覧で、**クラスターの入庫と並べ替え** を検索して選択します。</span><span class="sxs-lookup"><span data-stu-id="9e9fa-224">In the **Available menus and menu items** list, find and select **Receive and sort cluster**.</span></span>
1. <span data-ttu-id="9e9fa-225">右矢印ボタンを選択して、選択したメニュー項目を **メニュー構造** の一覧に移動します。</span><span class="sxs-lookup"><span data-stu-id="9e9fa-225">Select the right arrow button to move the selected menu item to the **Menu structure** list.</span></span>
1. <span data-ttu-id="9e9fa-226">上向き矢印ボタンまたは下向き矢印ボタンを使用して、メニュー項目をメニューの目的の位置に移動します。</span><span class="sxs-lookup"><span data-stu-id="9e9fa-226">Use the up arrow or down arrow button to move the menu item into the desired position in the menu.</span></span>
1. <span data-ttu-id="9e9fa-227">アクション ウィンドウで、**保存** を選択します。</span><span class="sxs-lookup"><span data-stu-id="9e9fa-227">On the Action Pane, select **Save**.</span></span>
1. <span data-ttu-id="9e9fa-228">手順 4 から 7 を繰り返して、残りのメニュー項目を追加します:</span><span class="sxs-lookup"><span data-stu-id="9e9fa-228">Repeat steps 4 through 7 to add the remaining menu items:</span></span>

    - <span data-ttu-id="9e9fa-229">クラスターの割り当て</span><span class="sxs-lookup"><span data-stu-id="9e9fa-229">Assign cluster</span></span>
    - <span data-ttu-id="9e9fa-230">クラスター プットアウェイ</span><span class="sxs-lookup"><span data-stu-id="9e9fa-230">Cluster putaway</span></span>

## <a name="example-scenario"></a><span data-ttu-id="9e9fa-231">シナリオ例</span><span class="sxs-lookup"><span data-stu-id="9e9fa-231">Example scenario</span></span>

<span data-ttu-id="9e9fa-232">このシナリオでは、プットアウェイ クラスターの処理をシミュレートします。</span><span class="sxs-lookup"><span data-stu-id="9e9fa-232">This scenario simulates putaway cluster processing.</span></span>

### <a name="create-a-purchase-order"></a><span data-ttu-id="9e9fa-233">発注書の作成</span><span class="sxs-lookup"><span data-stu-id="9e9fa-233">Create a purchase order</span></span>

1. <span data-ttu-id="9e9fa-234">**買掛金勘定 \> 発注書 \> すべての発注書** に移動します。</span><span class="sxs-lookup"><span data-stu-id="9e9fa-234">Go to **Accounts payable \> Purchase orders \> All purchase orders**.</span></span>
1. <span data-ttu-id="9e9fa-235">アクション ウィンドウで、**新規** を選択します。</span><span class="sxs-lookup"><span data-stu-id="9e9fa-235">On the Action Pane, select **New**.</span></span>
1. <span data-ttu-id="9e9fa-236">**発注書の作成** ダイアログ ボックスで、次の値を設定します。</span><span class="sxs-lookup"><span data-stu-id="9e9fa-236">In the **Create purchase order** dialog box, set the following values:</span></span>

    - <span data-ttu-id="9e9fa-237">**仕入先勘定 :** *1001*</span><span class="sxs-lookup"><span data-stu-id="9e9fa-237">**Vendor account:** *1001*</span></span>
    - <span data-ttu-id="9e9fa-238">**倉庫:** *61*</span><span class="sxs-lookup"><span data-stu-id="9e9fa-238">**Warehouse:** *61*</span></span>

1. <span data-ttu-id="9e9fa-239">**OK** を選択します。</span><span class="sxs-lookup"><span data-stu-id="9e9fa-239">Select **OK**.</span></span>

    <span data-ttu-id="9e9fa-240">**すべての発注書** ページが開きます。</span><span class="sxs-lookup"><span data-stu-id="9e9fa-240">The **All purchase orders** page appears.</span></span>

1. <span data-ttu-id="9e9fa-241">**すべての発注書** ページの **購買注文明細行** クイック タブで、**明細行の追加** ボタンを使用して次の行を追加します:</span><span class="sxs-lookup"><span data-stu-id="9e9fa-241">On the **All purchase orders** page, on the **Purchase order lines** FastTab, use the **Add line** button to add the following lines:</span></span>

    - <span data-ttu-id="9e9fa-242">発注書明細行 1:</span><span class="sxs-lookup"><span data-stu-id="9e9fa-242">Purchase order line 1:</span></span>

        - <span data-ttu-id="9e9fa-243">**品目番号:** *A0001*</span><span class="sxs-lookup"><span data-stu-id="9e9fa-243">**Item number:** *A0001*</span></span>
        - <span data-ttu-id="9e9fa-244">**数量:** *10*</span><span class="sxs-lookup"><span data-stu-id="9e9fa-244">**Quantity:** *10*</span></span>

    - <span data-ttu-id="9e9fa-245">発注書明細行 2:</span><span class="sxs-lookup"><span data-stu-id="9e9fa-245">Purchase order line 2:</span></span>

        - <span data-ttu-id="9e9fa-246">**品目番号:** *A0002*</span><span class="sxs-lookup"><span data-stu-id="9e9fa-246">**Item number:** *A0002*</span></span>
        - <span data-ttu-id="9e9fa-247">**数量:** *20*</span><span class="sxs-lookup"><span data-stu-id="9e9fa-247">**Quantity:** *20*</span></span>

    - <span data-ttu-id="9e9fa-248">発注書明細行 3:</span><span class="sxs-lookup"><span data-stu-id="9e9fa-248">Purchase order line 3:</span></span>

        - <span data-ttu-id="9e9fa-249">**品目番号:** *M9215*</span><span class="sxs-lookup"><span data-stu-id="9e9fa-249">**Item number:** *M9215*</span></span>
        - <span data-ttu-id="9e9fa-250">**数量:** *30*</span><span class="sxs-lookup"><span data-stu-id="9e9fa-250">**Quantity:** *30*</span></span>

1. <span data-ttu-id="9e9fa-251">アクション ウィンドウで、**保存** を選択します。</span><span class="sxs-lookup"><span data-stu-id="9e9fa-251">On the Action Pane, select **Save**.</span></span>
1. <span data-ttu-id="9e9fa-252">発注書番号をメモします。</span><span class="sxs-lookup"><span data-stu-id="9e9fa-252">Make a note of the purchase order number.</span></span>

### <a name="receive-inventory-and-put-it-away-from-the-mobile-device"></a><span data-ttu-id="9e9fa-253">在庫を受け取りモバイル デバイスにプットアウェイする</span><span class="sxs-lookup"><span data-stu-id="9e9fa-253">Receive inventory and put it away from the mobile device</span></span>

#### <a name="receive-and-sort-the-inventory-into-a-cluster"></a><span data-ttu-id="9e9fa-254">クラスターへの在庫の入庫と並べ替え</span><span class="sxs-lookup"><span data-stu-id="9e9fa-254">Receive and sort the inventory into a cluster</span></span>

1. <span data-ttu-id="9e9fa-255">倉庫 *61* を設定したユーザーとして、倉庫アプリにログインします。</span><span class="sxs-lookup"><span data-stu-id="9e9fa-255">Sign in to the warehouse app as a user who is set up for warehouse *61*.</span></span>
1. <span data-ttu-id="9e9fa-256">メイン メニューで、**入庫** を選択します。</span><span class="sxs-lookup"><span data-stu-id="9e9fa-256">On the main menu, select **Inbound**.</span></span>
1. <span data-ttu-id="9e9fa-257">**入庫** メニューで、**クラスターの入庫と並べ替え** を選択します。</span><span class="sxs-lookup"><span data-stu-id="9e9fa-257">On the **Inbound** menu, select **Receive and sort cluster**.</span></span>
1. <span data-ttu-id="9e9fa-258">**Ponum** フィールドに発注書番号を入力します。</span><span class="sxs-lookup"><span data-stu-id="9e9fa-258">In the **Ponum** field, enter the purchase order number.</span></span>
1. <span data-ttu-id="9e9fa-259">**OK** ボタン (チェック マーク ボタン) を選択します。</span><span class="sxs-lookup"><span data-stu-id="9e9fa-259">Select **OK** (the check mark button).</span></span>
1. <span data-ttu-id="9e9fa-260">**品目** フィールドを選択し、品目番号 *A0001* を入力して、**OK** を選択します。</span><span class="sxs-lookup"><span data-stu-id="9e9fa-260">Select the **Item** field, enter item number *A0001*, and then select **OK**.</span></span>
1. <span data-ttu-id="9e9fa-261">**数量** フィールドを選択し、数字パッドを使用して *10* を入力し、チェック マーク ボタンを選択します。</span><span class="sxs-lookup"><span data-stu-id="9e9fa-261">Select the **Qty** field, enter *10* by using the number pad, and then select the check mark button.</span></span>
1. <span data-ttu-id="9e9fa-262">**数量** タスク ページで、**OK** (チェック マーク ボタン) を選択して、入力した数量を確定します。</span><span class="sxs-lookup"><span data-stu-id="9e9fa-262">On the **Qty** task page, select **OK** (the check mark button) to confirm the quantity that you entered.</span></span>
1. <span data-ttu-id="9e9fa-263">**品目** タスク ページで、**OK** を選択して品目 *A0001* が入力されたことを確認します。</span><span class="sxs-lookup"><span data-stu-id="9e9fa-263">On the **Item** task page, select **OK** to confirm that item *A0001* was entered.</span></span>
1. <span data-ttu-id="9e9fa-264">**クラスター ID** フィールドを選択し、作成しているクラスターの ID を割り当てる値を入力します。</span><span class="sxs-lookup"><span data-stu-id="9e9fa-264">Select the **Cluster ID** field, and enter a value to assign an ID for the cluster that you're creating.</span></span>

    <span data-ttu-id="9e9fa-265">ここに入力する ID は、発注書の残りの 2 つの品目を受け取るときに使用されます。</span><span class="sxs-lookup"><span data-stu-id="9e9fa-265">The ID that you enter here will be used when the two remaining items on the purchase order are received.</span></span>

1. <span data-ttu-id="9e9fa-266">**OK** を選択します。</span><span class="sxs-lookup"><span data-stu-id="9e9fa-266">Select **OK**.</span></span>

    <span data-ttu-id="9e9fa-267">**Ponum** タスク ページが表示され、"作業が完了しました" というメッセージが表示されます。</span><span class="sxs-lookup"><span data-stu-id="9e9fa-267">The **Ponum** task page appears and shows a "Work completed" message.</span></span>

    <span data-ttu-id="9e9fa-268">これで、品目 *A0001* が *RECV* 場所に入り、手順 10 で入力したクラスター ID に割り当てられました。</span><span class="sxs-lookup"><span data-stu-id="9e9fa-268">Item *A0001* has now been received into the *RECV* location and assigned to the cluster ID that you entered in step 10.</span></span>

1. <span data-ttu-id="9e9fa-269">発注書の残り 2 つの品目を受け取り、それをクラスター ID に割り当てるには、手順 4 から 11 を繰り返します。</span><span class="sxs-lookup"><span data-stu-id="9e9fa-269">Repeat steps 4 through 11 to receive the remaining two items from the purchase order and assign them to the cluster ID:</span></span>

    - <span data-ttu-id="9e9fa-270">品目 *A0002* の数量 *20*</span><span class="sxs-lookup"><span data-stu-id="9e9fa-270">A quantity of *20* for item *A0002*</span></span>
    - <span data-ttu-id="9e9fa-271">品目 *M9215* の数量 *30*</span><span class="sxs-lookup"><span data-stu-id="9e9fa-271">A quantity of *30* for item *M9215*</span></span>

#### <a name="close-the-cluster"></a><span data-ttu-id="9e9fa-272">クラスターをクローズする</span><span class="sxs-lookup"><span data-stu-id="9e9fa-272">Close the cluster</span></span>

<span data-ttu-id="9e9fa-273">クラスター内の品目をプットアウェイする前に、クラスターをクローズする必要があります。</span><span class="sxs-lookup"><span data-stu-id="9e9fa-273">Before the items in the cluster can be put away, the cluster must be closed.</span></span>

1. <span data-ttu-id="9e9fa-274">Supply Chain Management で、**倉庫管理 \> 作業 \> 出庫 \> 作業クラスター** に移動します。</span><span class="sxs-lookup"><span data-stu-id="9e9fa-274">In Supply Chain Management, go to **Warehouse management \> Work \> Outbound \> Work clusters**.</span></span>
1. <span data-ttu-id="9e9fa-275">**作業クラスター** ページの **作業クラスター** セクションで、先ほど入力した **クラスター ID** フィールドを検索します。</span><span class="sxs-lookup"><span data-stu-id="9e9fa-275">On the **Work clusters** page, in the **Work cluster** section, search the **Cluster ID** field for the cluster ID that you entered earlier.</span></span>
1. <span data-ttu-id="9e9fa-276">クラスターが表示されない場合は、既に閉じている可能性があります。</span><span class="sxs-lookup"><span data-stu-id="9e9fa-276">If the cluster isn't shown, it might already have been closed.</span></span> <span data-ttu-id="9e9fa-277">クラスターが閉じているかどうかを確認するには、**クローズした作業を表示** チェックボックスを選択して、先ほど入力したクラスター ID を検索します。</span><span class="sxs-lookup"><span data-stu-id="9e9fa-277">To determine whether the cluster was closed, select the **Show closed work** check box, and search for the cluster ID that you entered earlier.</span></span> <span data-ttu-id="9e9fa-278">そして、次の手順のいずれかを実行します。</span><span class="sxs-lookup"><span data-stu-id="9e9fa-278">Then follow one of these steps:</span></span>

    - <span data-ttu-id="9e9fa-279">クラスターがクローズされている場合は、この手順の残りの手順は省略し、次の手順の[クラスター プットアウェイ](#put-the-cluster-away)に進みます。</span><span class="sxs-lookup"><span data-stu-id="9e9fa-279">If the cluster has been closed, skip the remaining steps of this procedure, and move on to the next procedure, [Put the cluster away](#put-the-cluster-away).</span></span>
    - <span data-ttu-id="9e9fa-280">クラスターがクローズされていない場合は、この手順の残りの手順を実行して、クラスターを手動でクローズします。</span><span class="sxs-lookup"><span data-stu-id="9e9fa-280">If the cluster hasn't been closed, follow the remaining steps of this procedure to manually close the cluster.</span></span> <span data-ttu-id="9e9fa-281">次に、次の手順に移動します。</span><span class="sxs-lookup"><span data-stu-id="9e9fa-281">Then move on to the next procedure.</span></span>

1. <span data-ttu-id="9e9fa-282">**作業クラスター** セクションで、先に入力したクラスター ID を選択します。</span><span class="sxs-lookup"><span data-stu-id="9e9fa-282">In the **Work cluster** section, select the cluster ID that you entered earlier.</span></span>
1. <span data-ttu-id="9e9fa-283">アクション ペインで、**クラスターのクローズ** を選択します。</span><span class="sxs-lookup"><span data-stu-id="9e9fa-283">On the Action Pane, select **Close cluster**.</span></span>

    <span data-ttu-id="9e9fa-284">クラスターをクローズした後は、**終了した作業を表示** チェック ボックスをオンにしない限り、このクラスターは **作業クラスター** セクションに表示されなくなります。</span><span class="sxs-lookup"><span data-stu-id="9e9fa-284">After the cluster has been closed, it's no longer shown in the **Work cluster** section (unless the **Show closed work** check box is selected).</span></span>

#### <a name="put-the-cluster-away"></a><span data-ttu-id="9e9fa-285">クラスター プットアウェイ</span><span class="sxs-lookup"><span data-stu-id="9e9fa-285">Put the cluster away</span></span>

1. <span data-ttu-id="9e9fa-286">倉庫 *61* を設定したユーザーとして、倉庫アプリにログインします。</span><span class="sxs-lookup"><span data-stu-id="9e9fa-286">Sign in to the warehouse app as a user who is set up for warehouse *61*.</span></span>
1. <span data-ttu-id="9e9fa-287">メイン メニューで、**入庫** を選択します。</span><span class="sxs-lookup"><span data-stu-id="9e9fa-287">On the main menu, select **Inbound**.</span></span>
1. <span data-ttu-id="9e9fa-288">**入庫** メニューで、**クラスター プットアウェイ** を選択します。</span><span class="sxs-lookup"><span data-stu-id="9e9fa-288">On the **Inbound** menu, select **Cluster putaway**.</span></span>
1. <span data-ttu-id="9e9fa-289">**クラスター ID** を選択し、以前にクローズしたクラスターに対して入力したクラスター ID を入力します。</span><span class="sxs-lookup"><span data-stu-id="9e9fa-289">Select **Cluster ID**, and enter the cluster ID that you entered earlier for the closed cluster.</span></span>
1. <span data-ttu-id="9e9fa-290">**OK** を選択します。</span><span class="sxs-lookup"><span data-stu-id="9e9fa-290">Select **OK**.</span></span>

    <span data-ttu-id="9e9fa-291">**クラスター プットアウェイ: ピック** ページが表示されます。</span><span class="sxs-lookup"><span data-stu-id="9e9fa-291">The **Cluster putaway: Pick** page appears.</span></span> <span data-ttu-id="9e9fa-292">ここには、クラスター ID、ピッキング場所、品目 (値 *複数* が表示されます)、ピッキングする必要があるクラスターの合計数量が表示されます。</span><span class="sxs-lookup"><span data-stu-id="9e9fa-292">It shows the cluster ID, the picking location, the items (the value *Multiple* will be shown), and the total quantity in the cluster that must be picked.</span></span>

1. <span data-ttu-id="9e9fa-293">**OK** を選択します。</span><span class="sxs-lookup"><span data-stu-id="9e9fa-293">Select **OK**.</span></span>

    <span data-ttu-id="9e9fa-294">**クラスター プットアウェイ: プット** ページが表示されます。</span><span class="sxs-lookup"><span data-stu-id="9e9fa-294">The **Cluster putaway: Put** page appears.</span></span> <span data-ttu-id="9e9fa-295">**プット** の指示は、クラスターで受け取った品目のクラスター ID、プット場所、品目、合計数量、およびライセンス プレート ID を識別します。</span><span class="sxs-lookup"><span data-stu-id="9e9fa-295">The **Put** instructions identify the cluster ID, the put location, the items, the total quantity, and the license plate IDs for the items that have been received on the cluster.</span></span>

    <span data-ttu-id="9e9fa-296">この手順を上書きまたは実行するための標準のオプションがあります。</span><span class="sxs-lookup"><span data-stu-id="9e9fa-296">You have the standard options to override or pass this step.</span></span>

    <span data-ttu-id="9e9fa-297">![クラスター プットアウェイ: プット ページ](media/Cluster_putaway-Put.png "クラスター プットアウェイ: プット ページ")</span><span class="sxs-lookup"><span data-stu-id="9e9fa-297">![Cluster putaway: Put page](media/Cluster_putaway-Put.png "Cluster putaway: Put page")</span></span>

1. <span data-ttu-id="9e9fa-298">**OK** を選択して、クラスター プットアウェイを確認します。</span><span class="sxs-lookup"><span data-stu-id="9e9fa-298">Select **OK** to confirm the putaway of the cluster.</span></span>

    <span data-ttu-id="9e9fa-299">"クラスターが完了" しましたというメッセージが表示されます。</span><span class="sxs-lookup"><span data-stu-id="9e9fa-299">A "Cluster completed" message is shown.</span></span>

## <a name="notes-and-tips"></a><span data-ttu-id="9e9fa-300">メモとヒント</span><span class="sxs-lookup"><span data-stu-id="9e9fa-300">Notes and tips</span></span>

<span data-ttu-id="9e9fa-301">クラスター ID がネストされたパレットの親ライセンス プレートとなる場合は、そのクラスター ID がスキャンされるときにプット場所が自動的に指定されます。</span><span class="sxs-lookup"><span data-stu-id="9e9fa-301">For cases where the cluster ID becomes the parent license plate for a nested pallet, the put position is automatically given when the cluster ID is scanned.</span></span> <span data-ttu-id="9e9fa-302">ライセンス プレートの生成が手動に設定されている場合でも、それ以上のライセンス プレートをスキャンする必要はありません。</span><span class="sxs-lookup"><span data-stu-id="9e9fa-302">No further license plate must be scanned, even if license plate generation is set to manual.</span></span>
