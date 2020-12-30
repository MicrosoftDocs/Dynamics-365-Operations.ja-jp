---
title: 計画済クロスドッキング
description: このトピックでは、注文に必要な在庫数量が受入または作成から正しい出荷ドックまたはステージング領域に直接送られる、高度な計画済クロスドッキングについて説明します。 元伝票からの残りのすべての在庫は、通常のプットアウェイ プロセスによって適切な保管場所に送られます。
author: Mirzaab
manager: tfehr
ms.date: 07/01/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: WHSCrossDockingTemplate, WHSLoadPostMethod, WHSWorkClass, WHSWorkTemplateTable, WHSLocDirTable, WHSPlannedCrossDocking
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: mirzaab
ms.search.validFrom: 2020-07-01
ms.dyn365.ops.version: Release 10.0.7
ms.openlocfilehash: cc217f21a5fa70feb9ef9161f3ef2e2b6a333f35
ms.sourcegitcommit: 827d77c638555396b32d36af5d22d1b61dafb0e8
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 10/16/2020
ms.locfileid: "4432363"
---
# <a name="planned-cross-docking"></a><span data-ttu-id="6c1a6-104">計画済クロスドッキング</span><span class="sxs-lookup"><span data-stu-id="6c1a6-104">Planned cross-docking</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="6c1a6-105">このトピックでは、高度な計画済クロスドッキングについて説明します。</span><span class="sxs-lookup"><span data-stu-id="6c1a6-105">This topic describes advanced planned cross-docking.</span></span> <span data-ttu-id="6c1a6-106">クロスドッキングは、注文に必要な在庫数量が受入または作成から正しい出荷ドックまたはステージング領域に直接送られる倉庫プロセスです。</span><span class="sxs-lookup"><span data-stu-id="6c1a6-106">Cross-docking is a warehouse process where the inventory quantity that is required for an order is directed straight from receipt or creation to the correct outbound dock or staging area.</span></span> <span data-ttu-id="6c1a6-107">元伝票からの残りのすべての在庫は、通常のプットアウェイ プロセスによって適切な保管場所に送られます。</span><span class="sxs-lookup"><span data-stu-id="6c1a6-107">All remaining inventory from the inbound source is directed to the correct storage location through the regular put-away process.</span></span>

<span data-ttu-id="6c1a6-108">クロスドッキングにより、作業者は既に出荷注文としてマークされている入荷プットアウェイと出荷ピッキングの手順を省略します。</span><span class="sxs-lookup"><span data-stu-id="6c1a6-108">Cross-docking lets workers skip inbound put-away and outbound picking of inventory that is already marked for an outbound order.</span></span> <span data-ttu-id="6c1a6-109">したがって、在庫の処理回数は可能な限り最小限に抑えられます。</span><span class="sxs-lookup"><span data-stu-id="6c1a6-109">Therefore, the number of times that inventory is touched is minimized, where possible.</span></span> <span data-ttu-id="6c1a6-110">さらに、システムとの相互作用が少ないため、倉庫の作業現場での時間とスペースの節約が増加します。</span><span class="sxs-lookup"><span data-stu-id="6c1a6-110">Additionally, because there is less interaction with the system, time and space savings on the warehouse shop floor are increased.</span></span>

<span data-ttu-id="6c1a6-111">クロスドッキングを実行する前に、ユーザーは新しいクロスドッキング テンプレートを構成する必要があります。このテンプレートでは、クロスドッキングの供給元とその他の要件セットを指定します。</span><span class="sxs-lookup"><span data-stu-id="6c1a6-111">Before cross-docking can be run, the user must configure a new cross-docking template, where the supply source and other sets of requirements for cross-docking are specified.</span></span> <span data-ttu-id="6c1a6-112">出荷注文が作成されると、明細行は同じ品目を含む入荷注文に対してマークされる必要があります。</span><span class="sxs-lookup"><span data-stu-id="6c1a6-112">As the outbound order is created, the line must be marked against an inbound order that contains the same item.</span></span>

<span data-ttu-id="6c1a6-113">入荷注文の受取時に、クロスドッキング設定によってクロスドッキングの必要性が自動的に識別され、場所ディレクティブの設定に基づいて、必要な数量の移動作業が自動的に作成されます。</span><span class="sxs-lookup"><span data-stu-id="6c1a6-113">At the time of inbound order receiving, the cross-docking setup automatically identifies the need for cross-docking and creates the movement work for the required quantity, based on the setup of the location directive.</span></span>

> [!NOTE]
> <span data-ttu-id="6c1a6-114">倉庫管理パラメーターでこの機能の設定が有効になっている場合でも、クロスドッキング作業がキャンセルされると、在庫トランザクションは登録解除 **されません**。</span><span class="sxs-lookup"><span data-stu-id="6c1a6-114">Inventory transactions are **not** unregistered when crossing-dock work is canceled, even if the setting for this capability is turned on in Warehouse management parameters.</span></span>

## <a name="turn-on-the-planned-cross-docking-feature"></a><span data-ttu-id="6c1a6-115">計画済クロスドッキング機能を有効にする</span><span class="sxs-lookup"><span data-stu-id="6c1a6-115">Turn on the Planned cross docking feature</span></span>

<span data-ttu-id="6c1a6-116">高度な計画済クロスドッキングを使用するには、システム上で有効にする必要があります。</span><span class="sxs-lookup"><span data-stu-id="6c1a6-116">Before you can use advanced planned cross-docking, the feature must be turned on in your system.</span></span> <span data-ttu-id="6c1a6-117">管理者は、[機能の管理](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) ワークスペースを使用して、機能の状態を確認し、必要に応じて有効にすることができます。</span><span class="sxs-lookup"><span data-stu-id="6c1a6-117">Admins can use the [Feature management](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) workspace to check the status of the feature and turn it on if it's required.</span></span> <span data-ttu-id="6c1a6-118">この機能は、次のようにして表示されます。</span><span class="sxs-lookup"><span data-stu-id="6c1a6-118">There, the feature is listed in the following way:</span></span>

- <span data-ttu-id="6c1a6-119">**モジュール:** *倉庫管理*</span><span class="sxs-lookup"><span data-stu-id="6c1a6-119">**Module:** *Warehouse management*</span></span>
- <span data-ttu-id="6c1a6-120">**機能名 :** *計画済クロスドッキング*</span><span class="sxs-lookup"><span data-stu-id="6c1a6-120">**Feature name:** *Planned cross docking*</span></span>

## <a name="setup"></a><span data-ttu-id="6c1a6-121">セットアップ</span><span class="sxs-lookup"><span data-stu-id="6c1a6-121">Setup</span></span>

### <a name="regenerate-load-posting-methods"></a><span data-ttu-id="6c1a6-122">積荷の転記メソッドの再生成</span><span class="sxs-lookup"><span data-stu-id="6c1a6-122">Regenerate load posting methods</span></span>

<span data-ttu-id="6c1a6-123">計画済クロスドッキングは、積荷の転記メソッドとして実装されています。</span><span class="sxs-lookup"><span data-stu-id="6c1a6-123">Planned cross-docking is implemented as a load posting method.</span></span> <span data-ttu-id="6c1a6-124">機能を有効にした後で、方法を再生成する必要があります。</span><span class="sxs-lookup"><span data-stu-id="6c1a6-124">After you turn on the feature, you must regenerate the methods.</span></span>

1. <span data-ttu-id="6c1a6-125">**倉庫管理 \> 設定 \> 積荷の転記メソッド** の順に移動します。</span><span class="sxs-lookup"><span data-stu-id="6c1a6-125">Go to **Warehouse management \> Setup \> Load posting methods**.</span></span>
1. <span data-ttu-id="6c1a6-126">アクション ウィンドウで、**方法の再生成** を選択します。</span><span class="sxs-lookup"><span data-stu-id="6c1a6-126">On the Action Pane, select **Regenerate methods**.</span></span>

    <span data-ttu-id="6c1a6-127">再生成が完了すると、**メソッド名** の値が *planCrossDocking* のメソッドが表示されます。</span><span class="sxs-lookup"><span data-stu-id="6c1a6-127">When regeneration is completed, you should see a method that has a **Method name** value of *planCrossDocking*.</span></span>

1. <span data-ttu-id="6c1a6-128">ページを閉じます。</span><span class="sxs-lookup"><span data-stu-id="6c1a6-128">Close the page.</span></span>

### <a name="create-a-cross-docking-template"></a><span data-ttu-id="6c1a6-129">クロスドッキング テンプレートの作成</span><span class="sxs-lookup"><span data-stu-id="6c1a6-129">Create a cross-docking template</span></span>

1. <span data-ttu-id="6c1a6-130">**倉庫管理 \> 設定 \> 作業 \> クロスドッキング テンプレート** の順に移動します。</span><span class="sxs-lookup"><span data-stu-id="6c1a6-130">Go to **Warehouse management \> Setup \> Work \> Cross docking templates**.</span></span>
1. <span data-ttu-id="6c1a6-131">アクション ウィンドウで **新規** を選択して、テンプレートを作成します。</span><span class="sxs-lookup"><span data-stu-id="6c1a6-131">On the Action Pane, select **New** to create a template.</span></span>
1. <span data-ttu-id="6c1a6-132">ヘッダーで、次の値を設定します。</span><span class="sxs-lookup"><span data-stu-id="6c1a6-132">In the header, set the following values:</span></span>

    - <span data-ttu-id="6c1a6-133">**シーケンス:** *1*</span><span class="sxs-lookup"><span data-stu-id="6c1a6-133">**Sequence:** *1*</span></span>

        <span data-ttu-id="6c1a6-134">このフィールドでは、でテンプレートが評価される順序を定義します。</span><span class="sxs-lookup"><span data-stu-id="6c1a6-134">This field defines the order that templates are evaluated in.</span></span>

    - <span data-ttu-id="6c1a6-135">**クロスドッキング テンプレート ID:** *51*</span><span class="sxs-lookup"><span data-stu-id="6c1a6-135">**Cross docking template ID:** *51*</span></span>
    - <span data-ttu-id="6c1a6-136">**説明 :** *倉庫 51*</span><span class="sxs-lookup"><span data-stu-id="6c1a6-136">**Description:** *Warehouse 51*</span></span>
    - <span data-ttu-id="6c1a6-137">**需要リリース ポリシー :** *供給受領前*</span><span class="sxs-lookup"><span data-stu-id="6c1a6-137">**Demand release policy:** *Before supply receipt*</span></span>
    - <span data-ttu-id="6c1a6-138">**倉庫:** *51*</span><span class="sxs-lookup"><span data-stu-id="6c1a6-138">**Warehouse:** *51*</span></span>

1. <span data-ttu-id="6c1a6-139">**計画** クイック タブでの設定は、テンプレートの動作を制御します。</span><span class="sxs-lookup"><span data-stu-id="6c1a6-139">The setup on the **Planning** FastTab controls how the template works.</span></span> <span data-ttu-id="6c1a6-140">次の値を設定します。</span><span class="sxs-lookup"><span data-stu-id="6c1a6-140">Set the following values:</span></span>

    - <span data-ttu-id="6c1a6-141">**需要の要件 :** *なし*</span><span class="sxs-lookup"><span data-stu-id="6c1a6-141">**Demand requirements:** *None*</span></span>

        <span data-ttu-id="6c1a6-142">このフィールドは、需要在庫の要件を定義します。</span><span class="sxs-lookup"><span data-stu-id="6c1a6-142">This field defines the requirements of the demand inventory.</span></span> <span data-ttu-id="6c1a6-143">リリース前に需要を供給にリンクする必要がある場合は、*マーキング* を選択します。</span><span class="sxs-lookup"><span data-stu-id="6c1a6-143">If the demand must be linked to the supply before release, select *Marking*.</span></span> <span data-ttu-id="6c1a6-144">リリース前に需要を供給に対して注文引当する必要がある場合は、*注文引当* を選択します。</span><span class="sxs-lookup"><span data-stu-id="6c1a6-144">If the demand must be order-reserved against the supply before release, select *Order reservation*.</span></span>

    - <span data-ttu-id="6c1a6-145">**検索タイプ :** *出荷場所*</span><span class="sxs-lookup"><span data-stu-id="6c1a6-145">**Locating type:** *Shipment locations*</span></span>

        <span data-ttu-id="6c1a6-146">このフィールドは、クロスドッキング作業でステージング / 積荷の場所を使用する必要があるかどうか、または、独自のステージング / 積荷の場所の検索に場所ディレクティブを使用するかどうかを定義します。</span><span class="sxs-lookup"><span data-stu-id="6c1a6-146">This field defines whether the cross-docking work should use the staging/load locations from the shipment, or whether it should use location directives to find its own staging/load locations.</span></span>

    - <span data-ttu-id="6c1a6-147">**作業テンプレート** このフィールドは空白のままにしておきます。</span><span class="sxs-lookup"><span data-stu-id="6c1a6-147">**Work template:** Leave this field blank.</span></span>

        <span data-ttu-id="6c1a6-148">このフィールドでは、クロスドッキング作業を作成するときに使用する作業テンプレートを定義します。</span><span class="sxs-lookup"><span data-stu-id="6c1a6-148">This field defines the work template that should be used when cross-docking work is created.</span></span>

    - <span data-ttu-id="6c1a6-149">**供給受領の再検証 :** *いいえ*</span><span class="sxs-lookup"><span data-stu-id="6c1a6-149">**Revalidate on supply receipt:** *No*</span></span>

        <span data-ttu-id="6c1a6-150">このオプションは、受領時に供給を再検証するかどうかを定義します。</span><span class="sxs-lookup"><span data-stu-id="6c1a6-150">This option defines whether the supply should be revalidated during receipt.</span></span> <span data-ttu-id="6c1a6-151">このオプションが *はい* に設定されている場合は、最大時間ウィンドウと有効期限の日付範囲の両方がチェックされます。</span><span class="sxs-lookup"><span data-stu-id="6c1a6-151">If this option is set to *Yes*, both the maximum time window and the expiration days range are checked.</span></span>

    - <span data-ttu-id="6c1a6-152">**時間ウィンドウの検証 :** *はい*</span><span class="sxs-lookup"><span data-stu-id="6c1a6-152">**Validate time window:** *Yes*</span></span>

        <span data-ttu-id="6c1a6-153">このオプションは、供給元を選択したときに最大時間ウィンドウを評価するかどうかを定義します。</span><span class="sxs-lookup"><span data-stu-id="6c1a6-153">This option defines whether the maximum time window should be evaluated when a supply source is selected.</span></span> <span data-ttu-id="6c1a6-154">このオプションが *はい* に設定されている場合は、最大および最小時間ウィンドウに関連するフィールドが使用可能になります。</span><span class="sxs-lookup"><span data-stu-id="6c1a6-154">If this option is set to *Yes*, the fields that are related to the maximum and minimum time windows become available.</span></span>

    - <span data-ttu-id="6c1a6-155">**最大時間ウィンドウ :** *5*</span><span class="sxs-lookup"><span data-stu-id="6c1a6-155">**Maximum time window:** *5*</span></span>

        <span data-ttu-id="6c1a6-156">このフィールドでは、供給到着から需要出発までの間で許可される最大期間を定義します。</span><span class="sxs-lookup"><span data-stu-id="6c1a6-156">This field defines the maximum period that is allowed between supply arrival and demand departure.</span></span>

    - <span data-ttu-id="6c1a6-157">**最大時間ウィンドウの単位 :** *日*</span><span class="sxs-lookup"><span data-stu-id="6c1a6-157">**Maximum time window unit:** *Days*</span></span>
    - <span data-ttu-id="6c1a6-158">**最小時間ウィンドウ :** *0*</span><span class="sxs-lookup"><span data-stu-id="6c1a6-158">**Minimum time window:** *0*</span></span>

        <span data-ttu-id="6c1a6-159">このフィールドでは、供給到着から需要出発までの間で許可される最小期間を定義します。</span><span class="sxs-lookup"><span data-stu-id="6c1a6-159">This field defines the minimum period that is allowed between supply arrival and demand departure.</span></span>

    - <span data-ttu-id="6c1a6-160">**最小時間ウィンドウの単位 :** *日*</span><span class="sxs-lookup"><span data-stu-id="6c1a6-160">**Minimum time window unit:** *Days*</span></span>
    - <span data-ttu-id="6c1a6-161">**有効期限の日付範囲 :** *0*</span><span class="sxs-lookup"><span data-stu-id="6c1a6-161">**Expiration days range:** *0*</span></span>

        <span data-ttu-id="6c1a6-162">*先入れ先出し (FEFO) 基準 :* このフィールドでは、現在倉庫にある最初に失効するバッチの有効期限から、受入中のバッチまでの最大日数を定義します。</span><span class="sxs-lookup"><span data-stu-id="6c1a6-162">*First expiry first out (FEFO) criteria:* This field defines the maximum number of days between the expiration date of the first-expiring batch that is currently in the warehouse and the batch that is being received.</span></span>

1. <span data-ttu-id="6c1a6-163">**供給元** クイック タブで、このテンプレートに対して有効な供給タイプを指定します。</span><span class="sxs-lookup"><span data-stu-id="6c1a6-163">On the **Supply sources** FastTab, you specify the types of supply that are valid for this template.</span></span> <span data-ttu-id="6c1a6-164">**新規** を選択して、次の値を設定します。</span><span class="sxs-lookup"><span data-stu-id="6c1a6-164">Select **New**, and then set the following values:</span></span>

    - <span data-ttu-id="6c1a6-165">**シーケンス番号:** *1*</span><span class="sxs-lookup"><span data-stu-id="6c1a6-165">**Sequence number:** *1*</span></span>
    - <span data-ttu-id="6c1a6-166">**供給元 :** *発注書*</span><span class="sxs-lookup"><span data-stu-id="6c1a6-166">**Supply source:** *Purchase order*</span></span>

### <a name="create-a-work-class"></a><span data-ttu-id="6c1a6-167">作業クラスの作成</span><span class="sxs-lookup"><span data-stu-id="6c1a6-167">Create a work class</span></span>

1. <span data-ttu-id="6c1a6-168">**倉庫管理 \> 設定 \> 作業 \> 作業クラス** の順に移動します。</span><span class="sxs-lookup"><span data-stu-id="6c1a6-168">Go to **Warehouse management \> Setup \> Work \> Work classes**.</span></span>
1. <span data-ttu-id="6c1a6-169">アクション ウィンドウで **新規** を選択し、作業クラスを作成します。</span><span class="sxs-lookup"><span data-stu-id="6c1a6-169">On the Action Pane, select **New** to create a work class.</span></span>
1. <span data-ttu-id="6c1a6-170">次の値を設定します。</span><span class="sxs-lookup"><span data-stu-id="6c1a6-170">Set the following values:</span></span>

    - <span data-ttu-id="6c1a6-171">**作業クラス ID:** *CrossDock*</span><span class="sxs-lookup"><span data-stu-id="6c1a6-171">**Work class ID:** *CrossDock*</span></span>
    - <span data-ttu-id="6c1a6-172">**説明 :** *クロスドッキング*</span><span class="sxs-lookup"><span data-stu-id="6c1a6-172">**Description:** *Cross Dock*</span></span>
    - <span data-ttu-id="6c1a6-173">**作業指示書タイプ :** *クロスドッキング*</span><span class="sxs-lookup"><span data-stu-id="6c1a6-173">**Work order type:** *Cross docking*</span></span>

### <a name="create-a-work-template"></a><span data-ttu-id="6c1a6-174">作業テンプレートの作成</span><span class="sxs-lookup"><span data-stu-id="6c1a6-174">Create a work template</span></span>

1. <span data-ttu-id="6c1a6-175">**倉庫管理 \> 設定 \> 作業 \> 作業テンプレート** の順に移動します。</span><span class="sxs-lookup"><span data-stu-id="6c1a6-175">Go to **Warehouse management \> Setup \> Work \> Work templates**.</span></span>
1. <span data-ttu-id="6c1a6-176">**作業指示書タイプ** フィールドを *クロスドッキング* に設定します。</span><span class="sxs-lookup"><span data-stu-id="6c1a6-176">Set the **Work order type** field to *Cross docking*.</span></span>
1. <span data-ttu-id="6c1a6-177">アクション ウィンドウで **新規** を選択して、明細行を **概要** タブに追加します。</span><span class="sxs-lookup"><span data-stu-id="6c1a6-177">On the Action Pane, select **New** to add a line to the **Overview** tab.</span></span>
1. <span data-ttu-id="6c1a6-178">新しい明細行で、次の値を設定します。</span><span class="sxs-lookup"><span data-stu-id="6c1a6-178">On the new line, set the following values:</span></span>

    - <span data-ttu-id="6c1a6-179">**シーケンス番号 :** *1*</span><span class="sxs-lookup"><span data-stu-id="6c1a6-179">**Sequence number:** *1*</span></span>
    - <span data-ttu-id="6c1a6-180">**作業テンプレート ID:** *51 クロスドッキング*</span><span class="sxs-lookup"><span data-stu-id="6c1a6-180">**Work template:** *51 Cross Dock*</span></span>
    - <span data-ttu-id="6c1a6-181">**作業テンプレートの説明 :** *51 クロスドッキング*</span><span class="sxs-lookup"><span data-stu-id="6c1a6-181">**Work template description:** *51 Cross Dock*</span></span>

1. <span data-ttu-id="6c1a6-182">**保存** を選択して、**作業テンプレートの詳細** クイック タブを使用できるようにします。</span><span class="sxs-lookup"><span data-stu-id="6c1a6-182">Select **Save** to make the **Work Template Details** FastTab available.</span></span>
1. <span data-ttu-id="6c1a6-183">**作業テンプレートの詳細** クイック タブで、**新規** を選択してグリッドに明細行を追加します。</span><span class="sxs-lookup"><span data-stu-id="6c1a6-183">On the **Work Template Details** FastTab, select **New** to add a line to the grid.</span></span>
1. <span data-ttu-id="6c1a6-184">新しい明細行で、次の値を設定します。</span><span class="sxs-lookup"><span data-stu-id="6c1a6-184">On the new line, set the following values:</span></span>

    - <span data-ttu-id="6c1a6-185">**作業タイプ:** *ピッキング*</span><span class="sxs-lookup"><span data-stu-id="6c1a6-185">**Work type:** *Pick*</span></span>
    - <span data-ttu-id="6c1a6-186">**作業クラス ID:** *CrossDock*</span><span class="sxs-lookup"><span data-stu-id="6c1a6-186">**Work class ID:** *CrossDock*</span></span>

1. <span data-ttu-id="6c1a6-187">**新規** を選択して別の明細行を追加し、次の値を設定します。</span><span class="sxs-lookup"><span data-stu-id="6c1a6-187">Select **New** to add another line, and set the following values on it:</span></span>

    - <span data-ttu-id="6c1a6-188">**作業タイプ:** *プット*</span><span class="sxs-lookup"><span data-stu-id="6c1a6-188">**Work type:** *Put*</span></span>
    - <span data-ttu-id="6c1a6-189">**作業クラス ID:** *CrossDock*</span><span class="sxs-lookup"><span data-stu-id="6c1a6-189">**Work class ID:** *CrossDock*</span></span>

1. <span data-ttu-id="6c1a6-190">**保存** を選択して、*51 クロスドッキング* テンプレートの **有効** チェック ボックスがオンになっていることを確認します。</span><span class="sxs-lookup"><span data-stu-id="6c1a6-190">Select **Save**, and confirm that the **Valid** check box is selected for the *51 Cross Dock* template.</span></span>

> [!NOTE]
> <span data-ttu-id="6c1a6-191">*ピッキング* と *プット* の作業タイプの作業クラス ID は同じである必要があります。</span><span class="sxs-lookup"><span data-stu-id="6c1a6-191">The work class IDs for the *Pick* and *Put* work types must be the same.</span></span>

### <a name="create-location-directives"></a><span data-ttu-id="6c1a6-192">場所ディレクティブを作成する</span><span class="sxs-lookup"><span data-stu-id="6c1a6-192">Create location directives</span></span>

1. <span data-ttu-id="6c1a6-193">**倉庫管理 \> 設定 \> 場所のディレクティブ** に移動します。</span><span class="sxs-lookup"><span data-stu-id="6c1a6-193">Go to **Warehouse management \> Setup \> Location directives**.</span></span>
1. <span data-ttu-id="6c1a6-194">左ウィンドウで、**作業指示書タイプ** フィールドを *クロスドッキング* に設定します。</span><span class="sxs-lookup"><span data-stu-id="6c1a6-194">In the left pane, set the **Work order type** field to *Cross docking*.</span></span>
1. <span data-ttu-id="6c1a6-195">アクション ウィンドウで、**新規** を選択し、次の値を設定します。</span><span class="sxs-lookup"><span data-stu-id="6c1a6-195">On the Action Pane, select **New**, and set the following values:</span></span>

    - <span data-ttu-id="6c1a6-196">**シーケンス番号 :** *1*</span><span class="sxs-lookup"><span data-stu-id="6c1a6-196">**Sequence number:** *1*</span></span>
    - <span data-ttu-id="6c1a6-197">**名前 :** *51 クロスドッキング プット*</span><span class="sxs-lookup"><span data-stu-id="6c1a6-197">**Name:** *51 Cross Dock Put*</span></span>
    - <span data-ttu-id="6c1a6-198">**作業タイプ:** *プット*</span><span class="sxs-lookup"><span data-stu-id="6c1a6-198">**Work type:** *Put*</span></span>
    - <span data-ttu-id="6c1a6-199">**サイト:** *5*</span><span class="sxs-lookup"><span data-stu-id="6c1a6-199">**Site:** *5*</span></span>
    - <span data-ttu-id="6c1a6-200">**倉庫:** *51*</span><span class="sxs-lookup"><span data-stu-id="6c1a6-200">**Warehouse:** *51*</span></span>

1. <span data-ttu-id="6c1a6-201">**保存** を選択して、**明細行** クイック タブを使用できるようにします。</span><span class="sxs-lookup"><span data-stu-id="6c1a6-201">Select **Save** to make the **Lines** FastTab available.</span></span>
1. <span data-ttu-id="6c1a6-202">**明細行** クイック タブで、**新規** を選択してグリッドに明細行を追加します。</span><span class="sxs-lookup"><span data-stu-id="6c1a6-202">On the **Lines** FastTab, select **New** to add a line to the grid.</span></span>
1. <span data-ttu-id="6c1a6-203">新しい明細行で、次の値を設定します。</span><span class="sxs-lookup"><span data-stu-id="6c1a6-203">On the new line, set the following values:</span></span>

    - <span data-ttu-id="6c1a6-204">**開始数量:** *1*</span><span class="sxs-lookup"><span data-stu-id="6c1a6-204">**From quantity:** *1*</span></span>
    - <span data-ttu-id="6c1a6-205">**上限数量:** *1000000*</span><span class="sxs-lookup"><span data-stu-id="6c1a6-205">**To quantity:** *1,000,000*</span></span>

1. <span data-ttu-id="6c1a6-206">**保存** を選択して、**場所ディレクティブ アクション** クイック タブを使用できるようにします。</span><span class="sxs-lookup"><span data-stu-id="6c1a6-206">Select **Save** to make the **Location Directive Actions** FastTab available.</span></span>
1. <span data-ttu-id="6c1a6-207">**場所ディレクティブ アクション** クイック タブで、**新規** を選択してグリッドに明細行を追加します。</span><span class="sxs-lookup"><span data-stu-id="6c1a6-207">On the **Location Directive Actions** FastTab, select **New** to add a line to the grid.</span></span>
1. <span data-ttu-id="6c1a6-208">新しい明細行で、次の値を設定します。</span><span class="sxs-lookup"><span data-stu-id="6c1a6-208">On the new line, set the following values:</span></span>

    - <span data-ttu-id="6c1a6-209">**名前 :** *ベイドア*</span><span class="sxs-lookup"><span data-stu-id="6c1a6-209">**Name:** *Baydoor*</span></span>
    - <span data-ttu-id="6c1a6-210">**固定の場所の使用 :** *固定の場所および固定されていない場所*</span><span class="sxs-lookup"><span data-stu-id="6c1a6-210">**Fixed location usage:** *Fixed and non-fixed locations*</span></span>

1. <span data-ttu-id="6c1a6-211">**保存** を選択すると、**場所ディレクティブ アクション** のツール バーにある **クエリの編集** ボタンが使用できるようになります。</span><span class="sxs-lookup"><span data-stu-id="6c1a6-211">Select **Save** to make the **Edit query** button on the **Location Directive Actions** toolbar available.</span></span>
1. <span data-ttu-id="6c1a6-212">**クエリの編集** を選択して、クエリ エディターを開きます。</span><span class="sxs-lookup"><span data-stu-id="6c1a6-212">Select **Edit query** to open the query editor.</span></span>
1. <span data-ttu-id="6c1a6-213">**範囲** タブで、次の 2 つの明細行が構成されていることを確認します。</span><span class="sxs-lookup"><span data-stu-id="6c1a6-213">On the **Range** tab, make sure that the following two lines are configured:</span></span>

    - <span data-ttu-id="6c1a6-214">明細行 1:</span><span class="sxs-lookup"><span data-stu-id="6c1a6-214">Line 1:</span></span>

        - <span data-ttu-id="6c1a6-215">**テーブル:** *場所*</span><span class="sxs-lookup"><span data-stu-id="6c1a6-215">**Table:** *Locations*</span></span>
        - <span data-ttu-id="6c1a6-216">**派生テーブル :** *場所*</span><span class="sxs-lookup"><span data-stu-id="6c1a6-216">**Derived Table:** *Locations*</span></span>
        - <span data-ttu-id="6c1a6-217">**フィールド :** *倉庫*</span><span class="sxs-lookup"><span data-stu-id="6c1a6-217">**Field:** *Warehouse*</span></span>
        - <span data-ttu-id="6c1a6-218">**基準 :** *51*</span><span class="sxs-lookup"><span data-stu-id="6c1a6-218">**Criteria:** *51*</span></span>

    - <span data-ttu-id="6c1a6-219">明細行 2:</span><span class="sxs-lookup"><span data-stu-id="6c1a6-219">Line 2:</span></span>

        - <span data-ttu-id="6c1a6-220">**テーブル:** *場所*</span><span class="sxs-lookup"><span data-stu-id="6c1a6-220">**Table:** *Locations*</span></span>
        - <span data-ttu-id="6c1a6-221">**派生テーブル :** *場所*</span><span class="sxs-lookup"><span data-stu-id="6c1a6-221">**Derived Table:** *Locations*</span></span>
        - <span data-ttu-id="6c1a6-222">**フィールド :** *場所*</span><span class="sxs-lookup"><span data-stu-id="6c1a6-222">**Field:** *Location*</span></span>
        - <span data-ttu-id="6c1a6-223">**基準 :** *ベイドア*</span><span class="sxs-lookup"><span data-stu-id="6c1a6-223">**Criteria:** *Baydoor*</span></span>

1. <span data-ttu-id="6c1a6-224">**OK** を選択してクエリ エディターを閉じます。</span><span class="sxs-lookup"><span data-stu-id="6c1a6-224">Select **OK** to close the query editor.</span></span>

### <a name="create-a-mobile-device-menu-item"></a><span data-ttu-id="6c1a6-225">品目のモバイル デバイス メニューの作成</span><span class="sxs-lookup"><span data-stu-id="6c1a6-225">Create a mobile device menu item</span></span>

1. <span data-ttu-id="6c1a6-226">**倉庫管理 \> 設定 \> モバイル デバイス \> モバイル デバイスのメニュー品目** の順に移動します。</span><span class="sxs-lookup"><span data-stu-id="6c1a6-226">Go to **Warehouse management \> Setup \> Mobile device \> Mobile device menu items**.</span></span>
1. <span data-ttu-id="6c1a6-227">左ウィンドウのメニュー項目の一覧で、**購入品のプットアウェイ** を選択します。</span><span class="sxs-lookup"><span data-stu-id="6c1a6-227">In the list of menu items in the left pane, select **Purchase Put-away**.</span></span>
1. <span data-ttu-id="6c1a6-228">**編集** を選択します。</span><span class="sxs-lookup"><span data-stu-id="6c1a6-228">Select **Edit**.</span></span>
1. <span data-ttu-id="6c1a6-229">**作業クラス** クイック タブで、**新規** を選択してグリッドに明細行を追加します。</span><span class="sxs-lookup"><span data-stu-id="6c1a6-229">On the **Work classes** FastTab, select **New** to add a line to the grid.</span></span>
1. <span data-ttu-id="6c1a6-230">新しい明細行で、次の値を設定します。</span><span class="sxs-lookup"><span data-stu-id="6c1a6-230">On the new line, set the following values:</span></span>

    - <span data-ttu-id="6c1a6-231">**作業クラス ID:** *CrossDock*</span><span class="sxs-lookup"><span data-stu-id="6c1a6-231">**Work class ID:** *CrossDock*</span></span>
    - <span data-ttu-id="6c1a6-232">**作業指示書タイプ :** *クロスドッキング*</span><span class="sxs-lookup"><span data-stu-id="6c1a6-232">**Work order type:** *Cross docking*</span></span>

1. <span data-ttu-id="6c1a6-233">**保存** を選択します。</span><span class="sxs-lookup"><span data-stu-id="6c1a6-233">Select **Save**.</span></span>

## <a name="scenario"></a><span data-ttu-id="6c1a6-234">シナリオ</span><span class="sxs-lookup"><span data-stu-id="6c1a6-234">Scenario</span></span>

### <a name="create-a-purchase-order"></a><span data-ttu-id="6c1a6-235">発注書の作成</span><span class="sxs-lookup"><span data-stu-id="6c1a6-235">Create a purchase order</span></span>

<span data-ttu-id="6c1a6-236">発注書を供給元として作成するには、次の手順に従います。</span><span class="sxs-lookup"><span data-stu-id="6c1a6-236">Follow these steps to create a purchase order as a source of supply.</span></span>

1. <span data-ttu-id="6c1a6-237">**調達 \> 発注書 \> すべての発注書** に移動します。</span><span class="sxs-lookup"><span data-stu-id="6c1a6-237">Go to **Procurement and sourcing \> Purchase orders \> All purchase orders**.</span></span>
1. <span data-ttu-id="6c1a6-238">アクション ウィンドウで、**新規** を選択します。</span><span class="sxs-lookup"><span data-stu-id="6c1a6-238">On the Action Pane, select **New**.</span></span>
1. <span data-ttu-id="6c1a6-239">**発注書の作成** ダイアログ ボックスで、次の値を設定します。</span><span class="sxs-lookup"><span data-stu-id="6c1a6-239">In the **Create purchase order** dialog box, set the following values:</span></span>

    - <span data-ttu-id="6c1a6-240">**仕入先勘定 :** *104*</span><span class="sxs-lookup"><span data-stu-id="6c1a6-240">**Vendor account:** *104*</span></span>
    - <span data-ttu-id="6c1a6-241">**倉庫:** *51*</span><span class="sxs-lookup"><span data-stu-id="6c1a6-241">**Warehouse:** *51*</span></span>

1. <span data-ttu-id="6c1a6-242">**OK** を選択し、注文番号をメモします。</span><span class="sxs-lookup"><span data-stu-id="6c1a6-242">Select **OK**, and make a note of the order number.</span></span>
1. <span data-ttu-id="6c1a6-243">新しい明細行が、**発注書明細行** クイック タブに追加されます。</span><span class="sxs-lookup"><span data-stu-id="6c1a6-243">A new line is added to the **Purchase order lines** FastTab.</span></span> <span data-ttu-id="6c1a6-244">この明細行で、次の値を設定します。</span><span class="sxs-lookup"><span data-stu-id="6c1a6-244">On this line, set the following values:</span></span>

    - <span data-ttu-id="6c1a6-245">**品目番号:** *A0001*</span><span class="sxs-lookup"><span data-stu-id="6c1a6-245">**Item number:** *A0001*</span></span>
    - <span data-ttu-id="6c1a6-246">**数量:** *5*</span><span class="sxs-lookup"><span data-stu-id="6c1a6-246">**Quantity:** *5*</span></span>

### <a name="create-a-sales-order"></a><span data-ttu-id="6c1a6-247">販売注文の作成</span><span class="sxs-lookup"><span data-stu-id="6c1a6-247">Create a sales order</span></span>

<span data-ttu-id="6c1a6-248">販売注文を需要元として作成するには、次の手順に従います。</span><span class="sxs-lookup"><span data-stu-id="6c1a6-248">Follow these steps to create a sales order as a source of demand.</span></span>

1. <span data-ttu-id="6c1a6-249">**販売とマーケティング \> 販売注文 \> すべての販売注文** の順に移動します。</span><span class="sxs-lookup"><span data-stu-id="6c1a6-249">Go to **Sales and marketing \> Sales orders \> All sales orders**.</span></span>
1. <span data-ttu-id="6c1a6-250">アクション ウィンドウで、**新規** を選択します。</span><span class="sxs-lookup"><span data-stu-id="6c1a6-250">On the Action Pane, select **New**.</span></span>
1. <span data-ttu-id="6c1a6-251">**販売注文の作成** ダイアログ ボックスでは、次の値を設定します。</span><span class="sxs-lookup"><span data-stu-id="6c1a6-251">In the **Create sales order** dialog box, set the following values:</span></span>

    - <span data-ttu-id="6c1a6-252">**顧客アカウント:** *US-002*</span><span class="sxs-lookup"><span data-stu-id="6c1a6-252">**Customer account:** *US-002*</span></span>
    - <span data-ttu-id="6c1a6-253">**倉庫:** *51*</span><span class="sxs-lookup"><span data-stu-id="6c1a6-253">**Warehouse:** *51*</span></span>

1. <span data-ttu-id="6c1a6-254">**OK** を選択します。</span><span class="sxs-lookup"><span data-stu-id="6c1a6-254">Select **OK**.</span></span>
1. <span data-ttu-id="6c1a6-255">新しい明細行が、**販売注文明細行** クイック タブに追加されます。</span><span class="sxs-lookup"><span data-stu-id="6c1a6-255">A new line is added to the **Sales order lines** FastTab.</span></span> <span data-ttu-id="6c1a6-256">この明細行で、次の値を設定します。</span><span class="sxs-lookup"><span data-stu-id="6c1a6-256">On this line, set the following values:</span></span>

    - <span data-ttu-id="6c1a6-257">**品目番号:** *A0001*</span><span class="sxs-lookup"><span data-stu-id="6c1a6-257">**Item number:** *A0001*</span></span>
    - <span data-ttu-id="6c1a6-258">**数量:** *3*</span><span class="sxs-lookup"><span data-stu-id="6c1a6-258">**Quantity:** *3*</span></span>

### <a name="create-planned-cross-docking"></a><span data-ttu-id="6c1a6-259">計画済クロスドッキングの作成</span><span class="sxs-lookup"><span data-stu-id="6c1a6-259">Create planned cross-docking</span></span>

<span data-ttu-id="6c1a6-260">販売注文から計画済クロスドッキングを作成するには、次の手順に従います。</span><span class="sxs-lookup"><span data-stu-id="6c1a6-260">Follow these steps to create the planned cross-docking from the sales order.</span></span>

1. <span data-ttu-id="6c1a6-261">作成した販売注文の **販売注文の詳細** ページのアクション ウィンドウにある、**倉庫** タブの **アクション** グループで、**倉庫へのリリース** を選択します。</span><span class="sxs-lookup"><span data-stu-id="6c1a6-261">In the **Sales order details** page for the sales order that you just created, on the Action Pane, on the **Warehouse** tab, in the **Actions** group, select **Release to warehouse**.</span></span>

    <span data-ttu-id="6c1a6-262">倉庫のリリース アクションによって、販売注文明細行の出荷と積荷明細行が作成され、在庫の配賦が試みられます。</span><span class="sxs-lookup"><span data-stu-id="6c1a6-262">The release to warehouse action creates a shipment and load line for the sales order line, and tries to allocate inventory.</span></span>
    
    <span data-ttu-id="6c1a6-263">情報メッセージが表示されます。</span><span class="sxs-lookup"><span data-stu-id="6c1a6-263">You receive an informational message.</span></span> <span data-ttu-id="6c1a6-264">また、「ウェーブ XXXX の作業は作成されませんでした。</span><span class="sxs-lookup"><span data-stu-id="6c1a6-264">You also receive the following warning message: "No work was created for wave XXXX.</span></span> <span data-ttu-id="6c1a6-265">詳細については、作業の作成履歴ログを参照してください。」という警告メッセージも表示されます。</span><span class="sxs-lookup"><span data-stu-id="6c1a6-265">See the work creation history log for details."</span></span> <span data-ttu-id="6c1a6-266">倉庫に在庫がないため、この動作が予想されます。</span><span class="sxs-lookup"><span data-stu-id="6c1a6-266">This behavior is expected, because there is no inventory in the warehouse.</span></span>

1. <span data-ttu-id="6c1a6-267">**販売注文明細行** クイック タブの **倉庫** メニューで、**出荷の詳細** を選択します。</span><span class="sxs-lookup"><span data-stu-id="6c1a6-267">On the **Sales order lines** FastTab, on the **Warehouse** menu, select **Shipment details**.</span></span>

    <span data-ttu-id="6c1a6-268">**出荷の詳細** ページが表示され、販売注文に対して作成された出荷が表示されます。</span><span class="sxs-lookup"><span data-stu-id="6c1a6-268">The **Shipment details** page appears and shows the shipment that was created for the sales order.</span></span>

1. <span data-ttu-id="6c1a6-269">**積荷明細行** クイック タブで、**計画済クロスドッキング数量** フィールドが *3* に設定されていることを確認します。</span><span class="sxs-lookup"><span data-stu-id="6c1a6-269">On the **Load lines** FastTab, notice that the **Planned cross docking quantity** field is set to *3*.</span></span> <span data-ttu-id="6c1a6-270">倉庫には在庫がなくても、有効な供給元がクロスドッキング テンプレートで定義されている時間ウィンドウ内に入庫するため、クロスドッキングの数量が作成されました。</span><span class="sxs-lookup"><span data-stu-id="6c1a6-270">Because no inventory was available in the warehouse, but a valid supply source will arrive within the time window that is defined in the cross-docking template, the cross-docking quantity was created.</span></span>
1. <span data-ttu-id="6c1a6-271">**積荷明細行** クイック タブで、**計画済クロスドッキング** を選択して、作成されたクロスドッキングの詳細を表示します。</span><span class="sxs-lookup"><span data-stu-id="6c1a6-271">On the **Load lines** FastTab, select **Planned cross docking** to view the details of the cross-docking that was created.</span></span>

## <a name="process-the-cross-docking"></a><span data-ttu-id="6c1a6-272">クロスドッキングのプロセス</span><span class="sxs-lookup"><span data-stu-id="6c1a6-272">Process the cross-docking</span></span>

### <a name="purchase-order-receiving-on-the-warehousing-mobile-app"></a><span data-ttu-id="6c1a6-273">倉庫管理モバイル アプリでの発注書の入庫</span><span class="sxs-lookup"><span data-stu-id="6c1a6-273">Purchase order receiving on the warehousing mobile app</span></span>

<span data-ttu-id="6c1a6-274">発注書から入庫場所に数量 5 が入庫し、2 つの作業がシステムによって作成されます。</span><span class="sxs-lookup"><span data-stu-id="6c1a6-274">The system will receive the quantity of 5 from the purchase order into the receiving location and create two pieces of work.</span></span>

<span data-ttu-id="6c1a6-275">作成された最初の作業 ID は、**作業指示タイプ** の値が *クロスドッキング* で、販売注文にリンクされています。</span><span class="sxs-lookup"><span data-stu-id="6c1a6-275">The first work ID that is created has a **Work order type** value of *Cross docking* and is linked to the sales order.</span></span> <span data-ttu-id="6c1a6-276">数量が 3 で、すぐに出荷できるように最終出荷場所に転送されます。</span><span class="sxs-lookup"><span data-stu-id="6c1a6-276">It has a quantity of 3 and is directed to the final shipping location so that it can be shipped out immediately.</span></span>

<span data-ttu-id="6c1a6-277">作成された 2 つ目の作業 ID は、**作業指示タイプ** の値が *発注書* で、発注書にリンクされています。</span><span class="sxs-lookup"><span data-stu-id="6c1a6-277">The second work ID that is created has a **Work order type** value of *Purchase orders* and is linked to the purchase order.</span></span> <span data-ttu-id="6c1a6-278">残りの 2 の数量はクロスドッキングされず、ストレージにプットアウェイされます。</span><span class="sxs-lookup"><span data-stu-id="6c1a6-278">It has the remaining quantity of 2 that wasn't cross-docked and is directed to put-away to storage.</span></span>

1. <span data-ttu-id="6c1a6-279">倉庫 *51* のユーザーとしてモバイル デバイスにサインインします。</span><span class="sxs-lookup"><span data-stu-id="6c1a6-279">Sign in to the mobile device as a user in warehouse *51*.</span></span>
1. <span data-ttu-id="6c1a6-280">**入庫 \> 購買の入庫** に移動します。</span><span class="sxs-lookup"><span data-stu-id="6c1a6-280">Go to **Inbound \> Purchase Receive**.</span></span>
1. <span data-ttu-id="6c1a6-281">**PONum** フィールドに発注書番号を入力します。</span><span class="sxs-lookup"><span data-stu-id="6c1a6-281">In the **PONum** field, enter your purchase order number.</span></span>
1. <span data-ttu-id="6c1a6-282">**数量** フィールドに、*5* と入力します。</span><span class="sxs-lookup"><span data-stu-id="6c1a6-282">In the **Qty** field, enter *5*.</span></span>
1. <span data-ttu-id="6c1a6-283">**OK** を選択します。</span><span class="sxs-lookup"><span data-stu-id="6c1a6-283">Select **OK**.</span></span>
1. <span data-ttu-id="6c1a6-284">次のページで、**品目** フィールドを *A0001* に設定します。</span><span class="sxs-lookup"><span data-stu-id="6c1a6-284">On the next page, set the **Item** field to *A0001*.</span></span>
1. <span data-ttu-id="6c1a6-285">**OK** を選択します。</span><span class="sxs-lookup"><span data-stu-id="6c1a6-285">Select **OK**.</span></span>
1. <span data-ttu-id="6c1a6-286">次のページで、**OK** を選択して、**PONum**、**品目**、および **数量** の値を確認します。</span><span class="sxs-lookup"><span data-stu-id="6c1a6-286">On the next page, confirm the **PONum**, **Item**, and **Qty** values by selecting **OK**.</span></span>

    <span data-ttu-id="6c1a6-287">「作業が完了しました」というメッセージが表示されます。</span><span class="sxs-lookup"><span data-stu-id="6c1a6-287">You receive a "Work Completed" message.</span></span>

1. <span data-ttu-id="6c1a6-288">**キャンセル** を選択して終了します。</span><span class="sxs-lookup"><span data-stu-id="6c1a6-288">Select **Cancel** to exit.</span></span>

### <a name="put-away-to-cross-docking-and-bulk"></a><span data-ttu-id="6c1a6-289">クロスドッキングおよびバルクへのプットアウェイ</span><span class="sxs-lookup"><span data-stu-id="6c1a6-289">Put-away to cross-docking and bulk</span></span>

<span data-ttu-id="6c1a6-290">現在、両方の作業 ID のターゲット ライセンス プレートは同じです。</span><span class="sxs-lookup"><span data-stu-id="6c1a6-290">Currently, both work IDs have the same target license plate.</span></span> <span data-ttu-id="6c1a6-291">次の手順を完了するには、作業 ID とターゲット ライセンス プレート ID を取得する必要があります。</span><span class="sxs-lookup"><span data-stu-id="6c1a6-291">To complete the next steps, you must get the work ID and the target license plate ID.</span></span> <span data-ttu-id="6c1a6-292">この情報は、注文書明細行および販売注文明細行の作業の詳細から取得できます。</span><span class="sxs-lookup"><span data-stu-id="6c1a6-292">You can get this information from the work details for the purchase order line and the sales order line.</span></span> <span data-ttu-id="6c1a6-293">または、**倉庫管理 \> 作業 \> 作業の詳細** に移動して、**倉庫** の値が *51* の作業をフィルター処理します。</span><span class="sxs-lookup"><span data-stu-id="6c1a6-293">Alternately, you can go to **Warehouse management \> Work \> Work details** and filter for work where the **Warehouse** value is *51*.</span></span>

1. <span data-ttu-id="6c1a6-294">モバイル デバイスでは、**入庫 \> 購入品のプットアウェイ** に移動して、作業からターゲット ライセンス プレートを入力します。</span><span class="sxs-lookup"><span data-stu-id="6c1a6-294">On the mobile device, go to **Inbound \> Purchase put-away**, and enter the target license plate from the work.</span></span>
1. <span data-ttu-id="6c1a6-295">**ID** フィールドに、作業の詳細からターゲット ライセンス プレート ID を入力します。</span><span class="sxs-lookup"><span data-stu-id="6c1a6-295">In the **ID** field, enter the target license plate ID from the work details.</span></span>

    <span data-ttu-id="6c1a6-296">クロスドッキングのピッキング ページには、ピッキング場所 (*RECV*)、ターゲット ライセンス プレート (*ライセンス プレート*)、品目 (*A0001*)、および数量 (*3*) が表示されます。</span><span class="sxs-lookup"><span data-stu-id="6c1a6-296">The cross-docking pick page shows the picking location (*RECV*), target license plate (*license plate*), item (*A0001*), and quantity (*3*).</span></span>

1. <span data-ttu-id="6c1a6-297">**OK** を選択します。</span><span class="sxs-lookup"><span data-stu-id="6c1a6-297">Select **OK**.</span></span>
1. <span data-ttu-id="6c1a6-298">**ターゲット LP** フィールドに、出荷場所にプット (クロスドッキング) するライセンス プレート ID のターゲット ライセンス プレートを入力します。</span><span class="sxs-lookup"><span data-stu-id="6c1a6-298">In the **Target LP** field, enter a target license plate for the license plate ID that should be put (cross-docked) to the shipping location.</span></span> <span data-ttu-id="6c1a6-299">選択した任意のライセンス プレート ID を選択できます。</span><span class="sxs-lookup"><span data-stu-id="6c1a6-299">You can select any license plate ID of your choice.</span></span>
1. <span data-ttu-id="6c1a6-300">**OK** を選択します。</span><span class="sxs-lookup"><span data-stu-id="6c1a6-300">Select **OK**.</span></span>
1. <span data-ttu-id="6c1a6-301">次のページの **ID** フィールドに、ターゲット ライセンス プレート ID を入力します。</span><span class="sxs-lookup"><span data-stu-id="6c1a6-301">On the next page, in the **ID** field, enter the target license plate ID.</span></span>
1. <span data-ttu-id="6c1a6-302">**OK** を選択します。</span><span class="sxs-lookup"><span data-stu-id="6c1a6-302">Select **OK**.</span></span>
1. <span data-ttu-id="6c1a6-303">残りの数量 2 をピッキングするための作業を確認し、**OK** を選択します。</span><span class="sxs-lookup"><span data-stu-id="6c1a6-303">Confirm the work for picking the remaining quantity of 2, and then select **OK**.</span></span>
1. <span data-ttu-id="6c1a6-304">次のページで、**完了** を選択してピッキング プロセスを終了し、プットアウェイ プロセスを開始します。</span><span class="sxs-lookup"><span data-stu-id="6c1a6-304">On the next page, select **Done** to end the picking process and begin the put-away process.</span></span>

    <span data-ttu-id="6c1a6-305">モバイル アプリでは、品目をプットする場所とライセンス プレートを提供します。</span><span class="sxs-lookup"><span data-stu-id="6c1a6-305">The mobile app presents you with the location and license plate to put the item to.</span></span>

1. <span data-ttu-id="6c1a6-306">**OK** を選択して、バルク ストレージの **プット** を確認します。</span><span class="sxs-lookup"><span data-stu-id="6c1a6-306">Confirm the bulk storage **Put** by selecting **OK**.</span></span>
1. <span data-ttu-id="6c1a6-307">次のページで、**OK** を選択して、クロスドッキングの **プット** を確認します。</span><span class="sxs-lookup"><span data-stu-id="6c1a6-307">On the next page, confirm the cross-docking **Put** by selecting **OK**.</span></span>

    <span data-ttu-id="6c1a6-308">「作業が完了しました」というメッセージが表示されます。</span><span class="sxs-lookup"><span data-stu-id="6c1a6-308">You receive a "Work Completed" message.</span></span>

1. <span data-ttu-id="6c1a6-309">**キャンセル** を選択して終了します。</span><span class="sxs-lookup"><span data-stu-id="6c1a6-309">Select **Cancel** to exit.</span></span>

<span data-ttu-id="6c1a6-310">次の図は、完了したクロスドッキング作業が Microsoft Dynamics 365 Supply Chain Management でどのように表示されるかを示しています。</span><span class="sxs-lookup"><span data-stu-id="6c1a6-310">The following illustration shows how the completed cross-docking work might appear in Microsoft Dynamics 365 Supply Chain Management.</span></span>

<span data-ttu-id="6c1a6-311">![クロスドッキング作業が完了しました](media/PlannedCrossDockingWork.png "クロスドッキング作業が完了しました")</span><span class="sxs-lookup"><span data-stu-id="6c1a6-311">![Cross-docking work completed](media/PlannedCrossDockingWork.png "Cross-docking work completed")</span></span>
