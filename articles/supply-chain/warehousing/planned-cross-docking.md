---
title: 計画済クロスドッキング
description: このトピックでは、注文に必要な在庫数量が受入または作成から正しい出荷ドックまたはステージング領域に直接送られる、高度な計画済クロスドッキングについて説明します。 元伝票からの残りのすべての在庫は、通常のプットアウェイ プロセスによって適切な保管場所に送られます。
author: Mirzaab
ms.date: 07/01/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: WHSCrossDockingTemplate, WHSLoadPostMethod, WHSWorkClass, WHSWorkTemplateTable, WHSLocDirTable, WHSPlannedCrossDocking
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: mirzaab
ms.search.validFrom: 2020-07-01
ms.dyn365.ops.version: Release 10.0.7
ms.openlocfilehash: 11e044e04e05c68af676bf97e6085e9975da5c1d
ms.sourcegitcommit: bef7bd2aac00d7eb837fd275d383b7a5c3f1c1ee
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/19/2021
ms.locfileid: "5911251"
---
# <a name="planned-cross-docking"></a><span data-ttu-id="2c75b-104">計画済クロスドッキング</span><span class="sxs-lookup"><span data-stu-id="2c75b-104">Planned cross-docking</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="2c75b-105">このトピックでは、高度な計画済クロスドッキングについて説明します。</span><span class="sxs-lookup"><span data-stu-id="2c75b-105">This topic describes advanced planned cross-docking.</span></span> <span data-ttu-id="2c75b-106">クロスドッキングは、注文に必要な在庫数量が受入または作成から正しい出荷ドックまたはステージング領域に直接送られる倉庫プロセスです。</span><span class="sxs-lookup"><span data-stu-id="2c75b-106">Cross-docking is a warehouse process where the inventory quantity that is required for an order is directed straight from receipt or creation to the correct outbound dock or staging area.</span></span> <span data-ttu-id="2c75b-107">元伝票からの残りのすべての在庫は、通常のプットアウェイ プロセスによって適切な保管場所に送られます。</span><span class="sxs-lookup"><span data-stu-id="2c75b-107">All remaining inventory from the inbound source is directed to the correct storage location through the regular put-away process.</span></span>

<span data-ttu-id="2c75b-108">クロスドッキングにより、作業者は既に出荷注文としてマークされている入荷プットアウェイと出荷ピッキングの手順を省略します。</span><span class="sxs-lookup"><span data-stu-id="2c75b-108">Cross-docking lets workers skip inbound put-away and outbound picking of inventory that is already marked for an outbound order.</span></span> <span data-ttu-id="2c75b-109">したがって、在庫の処理回数は可能な限り最小限に抑えられます。</span><span class="sxs-lookup"><span data-stu-id="2c75b-109">Therefore, the number of times that inventory is touched is minimized, where possible.</span></span> <span data-ttu-id="2c75b-110">さらに、システムとの相互作用が少ないため、倉庫の作業現場での時間とスペースの節約が増加します。</span><span class="sxs-lookup"><span data-stu-id="2c75b-110">Additionally, because there is less interaction with the system, time and space savings on the warehouse shop floor are increased.</span></span>

<span data-ttu-id="2c75b-111">クロスドッキングを実行する前に、ユーザーは新しいクロスドッキング テンプレートを構成する必要があります。このテンプレートでは、クロスドッキングの供給元とその他の要件セットを指定します。</span><span class="sxs-lookup"><span data-stu-id="2c75b-111">Before you can run cross-docking, you must configure a new cross-docking template, where the supply source and other sets of requirements for cross-docking are specified.</span></span> <span data-ttu-id="2c75b-112">出荷注文が作成されると、明細行は同じ品目を含む入荷注文に対してマークされる必要があります。</span><span class="sxs-lookup"><span data-stu-id="2c75b-112">As the outbound order is created, the line must be marked against an inbound order that contains the same item.</span></span> <span data-ttu-id="2c75b-113">補充および発注書を設定する方法と同様に、クロスドッキング テンプレートのディレクティブ コード フィールドを選択できます。</span><span class="sxs-lookup"><span data-stu-id="2c75b-113">You can select the directive code field on the cross-docking template, similar to the way you set up replenishment and purchase orders.</span></span>

<span data-ttu-id="2c75b-114">入荷注文の受取時に、クロスドッキング設定によってクロスドッキングの必要性が自動的に識別され、場所ディレクティブの設定に基づいて、必要な数量の移動作業が自動的に作成されます。</span><span class="sxs-lookup"><span data-stu-id="2c75b-114">At the time of inbound order receiving, the cross-docking setup automatically identifies the need for cross-docking and creates the movement work for the required quantity, based on the setup of the location directive.</span></span>

> [!NOTE]
> <span data-ttu-id="2c75b-115">倉庫管理パラメーターでこの機能の設定が有効になっている場合でも、クロスドッキング作業がキャンセルされると、在庫トランザクションは登録解除 *されません*。</span><span class="sxs-lookup"><span data-stu-id="2c75b-115">Inventory transactions are *not* unregistered when crossing-dock work is canceled, even if the setting for this capability is turned on in Warehouse management parameters.</span></span>

## <a name="turn-on-the-planned-cross-docking-features"></a><span data-ttu-id="2c75b-116">計画済クロスドッキング機能を有効にする</span><span class="sxs-lookup"><span data-stu-id="2c75b-116">Turn on the planned cross docking features</span></span>

<span data-ttu-id="2c75b-117">このトピックで説明する機能がシステムにまだ含まれていない場合は、[機能管理](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) に移動して、次の機能を次の順序でオンにします:</span><span class="sxs-lookup"><span data-stu-id="2c75b-117">If your system doesn't already include the features described in this topic, go to [Feature management](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) and turn on the following features in the following order:</span></span>

1. <span data-ttu-id="2c75b-118">*計画済クロスドッキング*</span><span class="sxs-lookup"><span data-stu-id="2c75b-118">*Planned cross docking*</span></span>
1. <span data-ttu-id="2c75b-119">*クロスドッキング テンプレートと場所ディレクティブ*</span><span class="sxs-lookup"><span data-stu-id="2c75b-119">*Cross docking templates with location directives*</span></span>
    > [!NOTE]
    > <span data-ttu-id="2c75b-120">この機能により、補充テンプレートを設定するのと同じように、クロスドッキング テンプレートで **ディレクティブ コード** フィールドを指定できます。</span><span class="sxs-lookup"><span data-stu-id="2c75b-120">This feature enables the **Directive code** field to be specified on the cross-docking template, similar to the way you set up replenishment templates.</span></span> <span data-ttu-id="2c75b-121">この機能を有効にすると、最後の *プット* 明細行のクロスドッキング作業テンプレート行にディレクティブ コードを追加できなくなります。</span><span class="sxs-lookup"><span data-stu-id="2c75b-121">Enabling this feature prevents you from adding a directive code on the cross-docking work template lines for the final *Put* line.</span></span> <span data-ttu-id="2c75b-122">これにより、作業テンプレートを検討する前に、作業の作成中に最終的な配置場所を決定できます。</span><span class="sxs-lookup"><span data-stu-id="2c75b-122">This ensures that the final put location can be determined during work creation before considering work templates.</span></span>

## <a name="setup"></a><span data-ttu-id="2c75b-123">段取り</span><span class="sxs-lookup"><span data-stu-id="2c75b-123">Setup</span></span>

### <a name="regenerate-load-posting-methods"></a><span data-ttu-id="2c75b-124">積荷の転記メソッドの再生成</span><span class="sxs-lookup"><span data-stu-id="2c75b-124">Regenerate load posting methods</span></span>

<span data-ttu-id="2c75b-125">計画済クロスドッキングは、積荷の転記メソッドとして実装されています。</span><span class="sxs-lookup"><span data-stu-id="2c75b-125">Planned cross-docking is implemented as a load posting method.</span></span> <span data-ttu-id="2c75b-126">機能を有効にした後で、方法を再生成する必要があります。</span><span class="sxs-lookup"><span data-stu-id="2c75b-126">After you turn on the feature, you must regenerate the methods.</span></span>

1. <span data-ttu-id="2c75b-127">**倉庫管理 \> 設定 \> 積荷の転記メソッド** の順に移動します。</span><span class="sxs-lookup"><span data-stu-id="2c75b-127">Go to **Warehouse management \> Setup \> Load posting methods**.</span></span>
1. <span data-ttu-id="2c75b-128">アクション ウィンドウで、**方法の再生成** を選択します。</span><span class="sxs-lookup"><span data-stu-id="2c75b-128">On the Action Pane, select **Regenerate methods**.</span></span>

    <span data-ttu-id="2c75b-129">再生成が完了すると、**メソッド名** の値が *planCrossDocking* のメソッドが表示されます。</span><span class="sxs-lookup"><span data-stu-id="2c75b-129">When regeneration is completed, you should see a method that has a **Method name** value of *planCrossDocking*.</span></span>

1. <span data-ttu-id="2c75b-130">ページを閉じます。</span><span class="sxs-lookup"><span data-stu-id="2c75b-130">Close the page.</span></span>

### <a name="create-a-cross-docking-template"></a><span data-ttu-id="2c75b-131">クロスドッキング テンプレートの作成</span><span class="sxs-lookup"><span data-stu-id="2c75b-131">Create a cross-docking template</span></span>

1. <span data-ttu-id="2c75b-132">**倉庫管理 \> 設定 \> 作業 \> クロスドッキング テンプレート** の順に移動します。</span><span class="sxs-lookup"><span data-stu-id="2c75b-132">Go to **Warehouse management \> Setup \> Work \> Cross docking templates**.</span></span>
1. <span data-ttu-id="2c75b-133">アクション ウィンドウで **新規** を選択して、テンプレートを作成します。</span><span class="sxs-lookup"><span data-stu-id="2c75b-133">On the Action Pane, select **New** to create a template.</span></span>
1. <span data-ttu-id="2c75b-134">ヘッダーで、次の値を設定します。</span><span class="sxs-lookup"><span data-stu-id="2c75b-134">In the header, set the following values:</span></span>

    - <span data-ttu-id="2c75b-135">**シーケンス:** *1*</span><span class="sxs-lookup"><span data-stu-id="2c75b-135">**Sequence:** *1*</span></span>

        <span data-ttu-id="2c75b-136">このフィールドでは、でテンプレートが評価される順序を定義します。</span><span class="sxs-lookup"><span data-stu-id="2c75b-136">This field defines the order that templates are evaluated in.</span></span>

    - <span data-ttu-id="2c75b-137">**クロスドッキング テンプレート ID:** *51*</span><span class="sxs-lookup"><span data-stu-id="2c75b-137">**Cross docking template ID:** *51*</span></span>
    - <span data-ttu-id="2c75b-138">**説明 :** *倉庫 51*</span><span class="sxs-lookup"><span data-stu-id="2c75b-138">**Description:** *Warehouse 51*</span></span>
    - <span data-ttu-id="2c75b-139">**需要リリース ポリシー :** *供給受領前*</span><span class="sxs-lookup"><span data-stu-id="2c75b-139">**Demand release policy:** *Before supply receipt*</span></span>
    - <span data-ttu-id="2c75b-140">**倉庫:** *51*</span><span class="sxs-lookup"><span data-stu-id="2c75b-140">**Warehouse:** *51*</span></span>

1. <span data-ttu-id="2c75b-141">**計画** クイック タブでの設定は、テンプレートの動作を制御します。</span><span class="sxs-lookup"><span data-stu-id="2c75b-141">The setup on the **Planning** FastTab controls how the template works.</span></span> <span data-ttu-id="2c75b-142">次の値を設定します。</span><span class="sxs-lookup"><span data-stu-id="2c75b-142">Set the following values:</span></span>

    - <span data-ttu-id="2c75b-143">**需要の要件 :** *なし*</span><span class="sxs-lookup"><span data-stu-id="2c75b-143">**Demand requirements:** *None*</span></span>

        <span data-ttu-id="2c75b-144">このフィールドは、需要在庫の要件を定義します。</span><span class="sxs-lookup"><span data-stu-id="2c75b-144">This field defines the requirements of the demand inventory.</span></span> <span data-ttu-id="2c75b-145">リリース前に需要を供給にリンクする必要がある場合は、*マーキング* を選択します。</span><span class="sxs-lookup"><span data-stu-id="2c75b-145">If the demand must be linked to the supply before release, select *Marking*.</span></span> <span data-ttu-id="2c75b-146">リリース前に需要を供給に対して注文引当する必要がある場合は、*注文引当* を選択します。</span><span class="sxs-lookup"><span data-stu-id="2c75b-146">If the demand must be order-reserved against the supply before release, select *Order reservation*.</span></span>

    - <span data-ttu-id="2c75b-147">**検索タイプ :** *出荷場所*</span><span class="sxs-lookup"><span data-stu-id="2c75b-147">**Locating type:** *Shipment locations*</span></span>

        <span data-ttu-id="2c75b-148">このフィールドは、クロスドッキング作業でステージング / 積荷の場所を使用する必要があるかどうか、または、独自のステージング / 積荷の場所の検索に場所ディレクティブを使用するかどうかを定義します。</span><span class="sxs-lookup"><span data-stu-id="2c75b-148">This field defines whether the cross-docking work should use the staging/load locations from the shipment, or whether it should use location directives to find its own staging/load locations.</span></span>

    - <span data-ttu-id="2c75b-149">**作業テンプレート** このフィールドは空白のままにしておきます。</span><span class="sxs-lookup"><span data-stu-id="2c75b-149">**Work template:** Leave this field blank.</span></span>

        <span data-ttu-id="2c75b-150">このフィールドでは、クロスドッキング作業を作成するときに使用する作業テンプレートを定義します。</span><span class="sxs-lookup"><span data-stu-id="2c75b-150">This field defines the work template that should be used when cross-docking work is created.</span></span>

    - <span data-ttu-id="2c75b-151">**供給受領の再検証 :** *いいえ*</span><span class="sxs-lookup"><span data-stu-id="2c75b-151">**Revalidate on supply receipt:** *No*</span></span>

        <span data-ttu-id="2c75b-152">このオプションは、受領時に供給を再検証するかどうかを定義します。</span><span class="sxs-lookup"><span data-stu-id="2c75b-152">This option defines whether the supply should be revalidated during receipt.</span></span> <span data-ttu-id="2c75b-153">このオプションが *はい* に設定されている場合は、最大時間ウィンドウと有効期限の日付範囲の両方がチェックされます。</span><span class="sxs-lookup"><span data-stu-id="2c75b-153">If this option is set to *Yes*, both the maximum time window and the expiration days range are checked.</span></span>

    - <span data-ttu-id="2c75b-154">**ディレクティブ コード:** このフィールドは空白のままにします</span><span class="sxs-lookup"><span data-stu-id="2c75b-154">**Directive code:** Leave this field blank</span></span>

        <span data-ttu-id="2c75b-155">このオプションは、*場所ディレクティブ付きのクロスドッキング テンプレート* 機能によって有効になります。</span><span class="sxs-lookup"><span data-stu-id="2c75b-155">This option is enabled by the *Cross docking templates with location directives* feature.</span></span> <span data-ttu-id="2c75b-156">システムは、場所ディレクティブを使用して、クロスドッキング在庫の移動の最適な場所を決定できます。</span><span class="sxs-lookup"><span data-stu-id="2c75b-156">The system uses location directives to help determine the best location to move cross-docking inventory to.</span></span> <span data-ttu-id="2c75b-157">関連する各クロスドッキング テンプレートにディレクティブ コードを割り当てると、このコードを設定できます。</span><span class="sxs-lookup"><span data-stu-id="2c75b-157">You can set it up by assigning a directive code to each relevant cross-docking template.</span></span> <span data-ttu-id="2c75b-158">ディレクティブ コードが設定されている場合、作業が生成されるときに、システムはディレクティブ コードで場所ディレクティブを検索します。</span><span class="sxs-lookup"><span data-stu-id="2c75b-158">If a directive code is set, the system will search location directives by directive code when work is generated.</span></span> <span data-ttu-id="2c75b-159">これにより、特定のクロスドッキング テンプレートに使用される場所ディレクティブを制限できます。</span><span class="sxs-lookup"><span data-stu-id="2c75b-159">In this way, you can limit location directives that are used for a particular cross-docking template.</span></span>

    - <span data-ttu-id="2c75b-160">**時間ウィンドウの検証 :** *はい*</span><span class="sxs-lookup"><span data-stu-id="2c75b-160">**Validate time window:** *Yes*</span></span>

        <span data-ttu-id="2c75b-161">このオプションは、供給元を選択したときに最大時間ウィンドウを評価するかどうかを定義します。</span><span class="sxs-lookup"><span data-stu-id="2c75b-161">This option defines whether the maximum time window should be evaluated when a supply source is selected.</span></span> <span data-ttu-id="2c75b-162">このオプションが *はい* に設定されている場合は、最大および最小時間ウィンドウに関連するフィールドが使用可能になります。</span><span class="sxs-lookup"><span data-stu-id="2c75b-162">If this option is set to *Yes*, the fields that are related to the maximum and minimum time windows become available.</span></span>

    - <span data-ttu-id="2c75b-163">**最大時間ウィンドウ :** *5*</span><span class="sxs-lookup"><span data-stu-id="2c75b-163">**Maximum time window:** *5*</span></span>

        <span data-ttu-id="2c75b-164">このフィールドでは、供給到着から需要出発までの間で許可される最大期間を定義します。</span><span class="sxs-lookup"><span data-stu-id="2c75b-164">This field defines the maximum period that is allowed between supply arrival and demand departure.</span></span>

    - <span data-ttu-id="2c75b-165">**最大時間ウィンドウの単位 :** *日*</span><span class="sxs-lookup"><span data-stu-id="2c75b-165">**Maximum time window unit:** *Days*</span></span>
    - <span data-ttu-id="2c75b-166">**最小時間ウィンドウ :** *0*</span><span class="sxs-lookup"><span data-stu-id="2c75b-166">**Minimum time window:** *0*</span></span>

        <span data-ttu-id="2c75b-167">このフィールドでは、供給到着から需要出発までの間で許可される最小期間を定義します。</span><span class="sxs-lookup"><span data-stu-id="2c75b-167">This field defines the minimum period that is allowed between supply arrival and demand departure.</span></span>

    - <span data-ttu-id="2c75b-168">**最小時間ウィンドウの単位 :** *日*</span><span class="sxs-lookup"><span data-stu-id="2c75b-168">**Minimum time window unit:** *Days*</span></span>
    - <span data-ttu-id="2c75b-169">**有効期限の日付範囲 :** *0*</span><span class="sxs-lookup"><span data-stu-id="2c75b-169">**Expiration days range:** *0*</span></span>

        <span data-ttu-id="2c75b-170">*先入れ先出し (FEFO) 基準 :* このフィールドでは、現在倉庫にある最初に失効するバッチの有効期限から、受入中のバッチまでの最大日数を定義します。</span><span class="sxs-lookup"><span data-stu-id="2c75b-170">*First expiry first out (FEFO) criteria:* This field defines the maximum number of days between the expiration date of the first-expiring batch that is currently in the warehouse and the batch that is being received.</span></span>

1. <span data-ttu-id="2c75b-171">**供給元** クイック タブで、このテンプレートに対して有効な供給タイプを指定します。</span><span class="sxs-lookup"><span data-stu-id="2c75b-171">On the **Supply sources** FastTab, you specify the types of supply that are valid for this template.</span></span> <span data-ttu-id="2c75b-172">**新規** を選択して、次の値を設定します。</span><span class="sxs-lookup"><span data-stu-id="2c75b-172">Select **New**, and then set the following values:</span></span>

    - <span data-ttu-id="2c75b-173">**シーケンス番号:** *1*</span><span class="sxs-lookup"><span data-stu-id="2c75b-173">**Sequence number:** *1*</span></span>
    - <span data-ttu-id="2c75b-174">**供給元 :** *発注書*</span><span class="sxs-lookup"><span data-stu-id="2c75b-174">**Supply source:** *Purchase order*</span></span>

### <a name="create-a-work-class"></a><span data-ttu-id="2c75b-175">作業クラスの作成</span><span class="sxs-lookup"><span data-stu-id="2c75b-175">Create a work class</span></span>

1. <span data-ttu-id="2c75b-176">**倉庫管理 \> 設定 \> 作業 \> 作業クラス** の順に移動します。</span><span class="sxs-lookup"><span data-stu-id="2c75b-176">Go to **Warehouse management \> Setup \> Work \> Work classes**.</span></span>
1. <span data-ttu-id="2c75b-177">アクション ウィンドウで **新規** を選択し、作業クラスを作成します。</span><span class="sxs-lookup"><span data-stu-id="2c75b-177">On the Action Pane, select **New** to create a work class.</span></span>
1. <span data-ttu-id="2c75b-178">次の値を設定します。</span><span class="sxs-lookup"><span data-stu-id="2c75b-178">Set the following values:</span></span>

    - <span data-ttu-id="2c75b-179">**作業クラス ID:** *CrossDock*</span><span class="sxs-lookup"><span data-stu-id="2c75b-179">**Work class ID:** *CrossDock*</span></span>
    - <span data-ttu-id="2c75b-180">**説明 :** *クロスドッキング*</span><span class="sxs-lookup"><span data-stu-id="2c75b-180">**Description:** *Cross Dock*</span></span>
    - <span data-ttu-id="2c75b-181">**作業指示書タイプ :** *クロスドッキング*</span><span class="sxs-lookup"><span data-stu-id="2c75b-181">**Work order type:** *Cross docking*</span></span>

### <a name="create-a-work-template"></a><span data-ttu-id="2c75b-182">作業テンプレートの作成</span><span class="sxs-lookup"><span data-stu-id="2c75b-182">Create a work template</span></span>

1. <span data-ttu-id="2c75b-183">**倉庫管理 \> 設定 \> 作業 \> 作業テンプレート** の順に移動します。</span><span class="sxs-lookup"><span data-stu-id="2c75b-183">Go to **Warehouse management \> Setup \> Work \> Work templates**.</span></span>
1. <span data-ttu-id="2c75b-184">**作業指示書タイプ** フィールドを *クロスドッキング* に設定します。</span><span class="sxs-lookup"><span data-stu-id="2c75b-184">Set the **Work order type** field to *Cross docking*.</span></span>
1. <span data-ttu-id="2c75b-185">アクション ウィンドウで **新規** を選択して、明細行を **概要** タブに追加します。</span><span class="sxs-lookup"><span data-stu-id="2c75b-185">On the Action Pane, select **New** to add a line to the **Overview** tab.</span></span>
1. <span data-ttu-id="2c75b-186">新しい明細行で、次の値を設定します。</span><span class="sxs-lookup"><span data-stu-id="2c75b-186">On the new line, set the following values:</span></span>

    - <span data-ttu-id="2c75b-187">**シーケンス番号 :** *1*</span><span class="sxs-lookup"><span data-stu-id="2c75b-187">**Sequence number:** *1*</span></span>
    - <span data-ttu-id="2c75b-188">**作業テンプレート ID:** *51 クロスドッキング*</span><span class="sxs-lookup"><span data-stu-id="2c75b-188">**Work template:** *51 Cross Dock*</span></span>
    - <span data-ttu-id="2c75b-189">**作業テンプレートの説明 :** *51 クロスドッキング*</span><span class="sxs-lookup"><span data-stu-id="2c75b-189">**Work template description:** *51 Cross Dock*</span></span>

1. <span data-ttu-id="2c75b-190">**保存** を選択して、**作業テンプレートの詳細** クイック タブを使用できるようにします。</span><span class="sxs-lookup"><span data-stu-id="2c75b-190">Select **Save** to make the **Work Template Details** FastTab available.</span></span>
1. <span data-ttu-id="2c75b-191">**作業テンプレートの詳細** クイック タブで、**新規** を選択してグリッドに明細行を追加します。</span><span class="sxs-lookup"><span data-stu-id="2c75b-191">On the **Work Template Details** FastTab, select **New** to add a line to the grid.</span></span>
1. <span data-ttu-id="2c75b-192">新しい明細行で、次の値を設定します。</span><span class="sxs-lookup"><span data-stu-id="2c75b-192">On the new line, set the following values:</span></span>

    - <span data-ttu-id="2c75b-193">**作業タイプ:** *ピッキング*</span><span class="sxs-lookup"><span data-stu-id="2c75b-193">**Work type:** *Pick*</span></span>
    - <span data-ttu-id="2c75b-194">**作業クラス ID:** *CrossDock*</span><span class="sxs-lookup"><span data-stu-id="2c75b-194">**Work class ID:** *CrossDock*</span></span>

1. <span data-ttu-id="2c75b-195">**新規** を選択して別の明細行を追加し、次の値を設定します。</span><span class="sxs-lookup"><span data-stu-id="2c75b-195">Select **New** to add another line, and set the following values on it:</span></span>

    - <span data-ttu-id="2c75b-196">**作業タイプ:** *プット*</span><span class="sxs-lookup"><span data-stu-id="2c75b-196">**Work type:** *Put*</span></span>
    - <span data-ttu-id="2c75b-197">**作業クラス ID:** *CrossDock*</span><span class="sxs-lookup"><span data-stu-id="2c75b-197">**Work class ID:** *CrossDock*</span></span>

1. <span data-ttu-id="2c75b-198">**保存** を選択して、*51 クロスドッキング* テンプレートの **有効** チェック ボックスがオンになっていることを確認します。</span><span class="sxs-lookup"><span data-stu-id="2c75b-198">Select **Save**, and confirm that the **Valid** check box is selected for the *51 Cross Dock* template.</span></span>

> [!NOTE]
> <span data-ttu-id="2c75b-199">*ピッキング* と *プット* の作業タイプの作業クラス ID は同じである必要があります。</span><span class="sxs-lookup"><span data-stu-id="2c75b-199">The work class IDs for the *Pick* and *Put* work types must be the same.</span></span>

### <a name="create-location-directives"></a><span data-ttu-id="2c75b-200">場所ディレクティブを作成する</span><span class="sxs-lookup"><span data-stu-id="2c75b-200">Create location directives</span></span>

1. <span data-ttu-id="2c75b-201">**倉庫管理 \> 設定 \> 場所のディレクティブ** に移動します。</span><span class="sxs-lookup"><span data-stu-id="2c75b-201">Go to **Warehouse management \> Setup \> Location directives**.</span></span>
1. <span data-ttu-id="2c75b-202">左ウィンドウで、**作業指示書タイプ** フィールドを *クロスドッキング* に設定します。</span><span class="sxs-lookup"><span data-stu-id="2c75b-202">In the left pane, set the **Work order type** field to *Cross docking*.</span></span>
1. <span data-ttu-id="2c75b-203">アクション ウィンドウで、**新規** を選択し、次の値を設定します。</span><span class="sxs-lookup"><span data-stu-id="2c75b-203">On the Action Pane, select **New**, and set the following values:</span></span>

    - <span data-ttu-id="2c75b-204">**シーケンス番号 :** *1*</span><span class="sxs-lookup"><span data-stu-id="2c75b-204">**Sequence number:** *1*</span></span>
    - <span data-ttu-id="2c75b-205">**名前 :** *51 クロスドッキング プット*</span><span class="sxs-lookup"><span data-stu-id="2c75b-205">**Name:** *51 Cross Dock Put*</span></span>
    - <span data-ttu-id="2c75b-206">**作業タイプ:** *プット*</span><span class="sxs-lookup"><span data-stu-id="2c75b-206">**Work type:** *Put*</span></span>
    - <span data-ttu-id="2c75b-207">**サイト:** *5*</span><span class="sxs-lookup"><span data-stu-id="2c75b-207">**Site:** *5*</span></span>
    - <span data-ttu-id="2c75b-208">**倉庫:** *51*</span><span class="sxs-lookup"><span data-stu-id="2c75b-208">**Warehouse:** *51*</span></span>

1. <span data-ttu-id="2c75b-209">**保存** を選択して、**明細行** クイック タブを使用できるようにします。</span><span class="sxs-lookup"><span data-stu-id="2c75b-209">Select **Save** to make the **Lines** FastTab available.</span></span>
1. <span data-ttu-id="2c75b-210">**明細行** クイック タブで、**新規** を選択してグリッドに明細行を追加します。</span><span class="sxs-lookup"><span data-stu-id="2c75b-210">On the **Lines** FastTab, select **New** to add a line to the grid.</span></span>
1. <span data-ttu-id="2c75b-211">新しい明細行で、次の値を設定します。</span><span class="sxs-lookup"><span data-stu-id="2c75b-211">On the new line, set the following values:</span></span>

    - <span data-ttu-id="2c75b-212">**開始数量:** *1*</span><span class="sxs-lookup"><span data-stu-id="2c75b-212">**From quantity:** *1*</span></span>
    - <span data-ttu-id="2c75b-213">**上限数量:** *1000000*</span><span class="sxs-lookup"><span data-stu-id="2c75b-213">**To quantity:** *1,000,000*</span></span>

1. <span data-ttu-id="2c75b-214">**保存** を選択して、**場所ディレクティブ アクション** クイック タブを使用できるようにします。</span><span class="sxs-lookup"><span data-stu-id="2c75b-214">Select **Save** to make the **Location Directive Actions** FastTab available.</span></span>
1. <span data-ttu-id="2c75b-215">**場所ディレクティブ アクション** クイック タブで、**新規** を選択してグリッドに明細行を追加します。</span><span class="sxs-lookup"><span data-stu-id="2c75b-215">On the **Location Directive Actions** FastTab, select **New** to add a line to the grid.</span></span>
1. <span data-ttu-id="2c75b-216">新しい明細行で、次の値を設定します。</span><span class="sxs-lookup"><span data-stu-id="2c75b-216">On the new line, set the following values:</span></span>

    - <span data-ttu-id="2c75b-217">**名前 :** *ベイドア*</span><span class="sxs-lookup"><span data-stu-id="2c75b-217">**Name:** *Baydoor*</span></span>
    - <span data-ttu-id="2c75b-218">**固定の場所の使用 :** *固定の場所および固定されていない場所*</span><span class="sxs-lookup"><span data-stu-id="2c75b-218">**Fixed location usage:** *Fixed and non-fixed locations*</span></span>

1. <span data-ttu-id="2c75b-219">**保存** を選択すると、**場所ディレクティブ アクション** のツール バーにある **クエリの編集** ボタンが使用できるようになります。</span><span class="sxs-lookup"><span data-stu-id="2c75b-219">Select **Save** to make the **Edit query** button on the **Location Directive Actions** toolbar available.</span></span>
1. <span data-ttu-id="2c75b-220">**クエリの編集** を選択して、クエリ エディターを開きます。</span><span class="sxs-lookup"><span data-stu-id="2c75b-220">Select **Edit query** to open the query editor.</span></span>
1. <span data-ttu-id="2c75b-221">**範囲** タブで、次の 2 つの明細行が構成されていることを確認します。</span><span class="sxs-lookup"><span data-stu-id="2c75b-221">On the **Range** tab, make sure that the following two lines are configured:</span></span>

    - <span data-ttu-id="2c75b-222">明細行 1:</span><span class="sxs-lookup"><span data-stu-id="2c75b-222">Line 1:</span></span>

        - <span data-ttu-id="2c75b-223">**テーブル:** *場所*</span><span class="sxs-lookup"><span data-stu-id="2c75b-223">**Table:** *Locations*</span></span>
        - <span data-ttu-id="2c75b-224">**派生テーブル :** *場所*</span><span class="sxs-lookup"><span data-stu-id="2c75b-224">**Derived Table:** *Locations*</span></span>
        - <span data-ttu-id="2c75b-225">**フィールド :** *倉庫*</span><span class="sxs-lookup"><span data-stu-id="2c75b-225">**Field:** *Warehouse*</span></span>
        - <span data-ttu-id="2c75b-226">**基準 :** *51*</span><span class="sxs-lookup"><span data-stu-id="2c75b-226">**Criteria:** *51*</span></span>

    - <span data-ttu-id="2c75b-227">明細行 2:</span><span class="sxs-lookup"><span data-stu-id="2c75b-227">Line 2:</span></span>

        - <span data-ttu-id="2c75b-228">**テーブル:** *場所*</span><span class="sxs-lookup"><span data-stu-id="2c75b-228">**Table:** *Locations*</span></span>
        - <span data-ttu-id="2c75b-229">**派生テーブル :** *場所*</span><span class="sxs-lookup"><span data-stu-id="2c75b-229">**Derived Table:** *Locations*</span></span>
        - <span data-ttu-id="2c75b-230">**フィールド :** *場所*</span><span class="sxs-lookup"><span data-stu-id="2c75b-230">**Field:** *Location*</span></span>
        - <span data-ttu-id="2c75b-231">**基準 :** *ベイドア*</span><span class="sxs-lookup"><span data-stu-id="2c75b-231">**Criteria:** *Baydoor*</span></span>

1. <span data-ttu-id="2c75b-232">**OK** を選択してクエリ エディターを閉じます。</span><span class="sxs-lookup"><span data-stu-id="2c75b-232">Select **OK** to close the query editor.</span></span>

### <a name="create-a-mobile-device-menu-item"></a><span data-ttu-id="2c75b-233">品目のモバイル デバイス メニューの作成</span><span class="sxs-lookup"><span data-stu-id="2c75b-233">Create a mobile device menu item</span></span>

1. <span data-ttu-id="2c75b-234">**倉庫管理 \> 設定 \> モバイル デバイス \> モバイル デバイスのメニュー品目** の順に移動します。</span><span class="sxs-lookup"><span data-stu-id="2c75b-234">Go to **Warehouse management \> Setup \> Mobile device \> Mobile device menu items**.</span></span>
1. <span data-ttu-id="2c75b-235">左ウィンドウのメニュー項目の一覧で、**購入品のプットアウェイ** を選択します。</span><span class="sxs-lookup"><span data-stu-id="2c75b-235">In the list of menu items in the left pane, select **Purchase Put-away**.</span></span>
1. <span data-ttu-id="2c75b-236">**編集** を選択します。</span><span class="sxs-lookup"><span data-stu-id="2c75b-236">Select **Edit**.</span></span>
1. <span data-ttu-id="2c75b-237">**作業クラス** クイック タブで、**新規** を選択してグリッドに明細行を追加します。</span><span class="sxs-lookup"><span data-stu-id="2c75b-237">On the **Work classes** FastTab, select **New** to add a line to the grid.</span></span>
1. <span data-ttu-id="2c75b-238">新しい明細行で、次の値を設定します。</span><span class="sxs-lookup"><span data-stu-id="2c75b-238">On the new line, set the following values:</span></span>

    - <span data-ttu-id="2c75b-239">**作業クラス ID:** *CrossDock*</span><span class="sxs-lookup"><span data-stu-id="2c75b-239">**Work class ID:** *CrossDock*</span></span>
    - <span data-ttu-id="2c75b-240">**作業指示書タイプ :** *クロスドッキング*</span><span class="sxs-lookup"><span data-stu-id="2c75b-240">**Work order type:** *Cross docking*</span></span>

1. <span data-ttu-id="2c75b-241">**保存** を選択します。</span><span class="sxs-lookup"><span data-stu-id="2c75b-241">Select **Save**.</span></span>

## <a name="scenario"></a><span data-ttu-id="2c75b-242">シナリオ</span><span class="sxs-lookup"><span data-stu-id="2c75b-242">Scenario</span></span>

### <a name="create-a-purchase-order"></a><span data-ttu-id="2c75b-243">発注書の作成</span><span class="sxs-lookup"><span data-stu-id="2c75b-243">Create a purchase order</span></span>

<span data-ttu-id="2c75b-244">発注書を供給元として作成するには、次の手順に従います。</span><span class="sxs-lookup"><span data-stu-id="2c75b-244">Follow these steps to create a purchase order as a source of supply.</span></span>

1. <span data-ttu-id="2c75b-245">**調達 \> 発注書 \> すべての発注書** に移動します。</span><span class="sxs-lookup"><span data-stu-id="2c75b-245">Go to **Procurement and sourcing \> Purchase orders \> All purchase orders**.</span></span>
1. <span data-ttu-id="2c75b-246">アクション ウィンドウで、**新規** を選択します。</span><span class="sxs-lookup"><span data-stu-id="2c75b-246">On the Action Pane, select **New**.</span></span>
1. <span data-ttu-id="2c75b-247">**発注書の作成** ダイアログ ボックスで、次の値を設定します。</span><span class="sxs-lookup"><span data-stu-id="2c75b-247">In the **Create purchase order** dialog box, set the following values:</span></span>

    - <span data-ttu-id="2c75b-248">**仕入先勘定 :** *104*</span><span class="sxs-lookup"><span data-stu-id="2c75b-248">**Vendor account:** *104*</span></span>
    - <span data-ttu-id="2c75b-249">**倉庫:** *51*</span><span class="sxs-lookup"><span data-stu-id="2c75b-249">**Warehouse:** *51*</span></span>

1. <span data-ttu-id="2c75b-250">**OK** を選択し、注文番号をメモします。</span><span class="sxs-lookup"><span data-stu-id="2c75b-250">Select **OK**, and make a note of the order number.</span></span>
1. <span data-ttu-id="2c75b-251">新しい明細行が、**発注書明細行** クイック タブに追加されます。</span><span class="sxs-lookup"><span data-stu-id="2c75b-251">A new line is added to the **Purchase order lines** FastTab.</span></span> <span data-ttu-id="2c75b-252">この明細行で、次の値を設定します。</span><span class="sxs-lookup"><span data-stu-id="2c75b-252">On this line, set the following values:</span></span>

    - <span data-ttu-id="2c75b-253">**品目番号:** *A0001*</span><span class="sxs-lookup"><span data-stu-id="2c75b-253">**Item number:** *A0001*</span></span>
    - <span data-ttu-id="2c75b-254">**数量:** *5*</span><span class="sxs-lookup"><span data-stu-id="2c75b-254">**Quantity:** *5*</span></span>

### <a name="create-a-sales-order"></a><span data-ttu-id="2c75b-255">販売注文の作成</span><span class="sxs-lookup"><span data-stu-id="2c75b-255">Create a sales order</span></span>

<span data-ttu-id="2c75b-256">販売注文を需要元として作成するには、次の手順に従います。</span><span class="sxs-lookup"><span data-stu-id="2c75b-256">Follow these steps to create a sales order as a source of demand.</span></span>

1. <span data-ttu-id="2c75b-257">**販売とマーケティング \> 販売注文 \> すべての販売注文** の順に移動します。</span><span class="sxs-lookup"><span data-stu-id="2c75b-257">Go to **Sales and marketing \> Sales orders \> All sales orders**.</span></span>
1. <span data-ttu-id="2c75b-258">アクション ウィンドウで、**新規** を選択します。</span><span class="sxs-lookup"><span data-stu-id="2c75b-258">On the Action Pane, select **New**.</span></span>
1. <span data-ttu-id="2c75b-259">**販売注文の作成** ダイアログ ボックスでは、次の値を設定します。</span><span class="sxs-lookup"><span data-stu-id="2c75b-259">In the **Create sales order** dialog box, set the following values:</span></span>

    - <span data-ttu-id="2c75b-260">**顧客アカウント:** *US-002*</span><span class="sxs-lookup"><span data-stu-id="2c75b-260">**Customer account:** *US-002*</span></span>
    - <span data-ttu-id="2c75b-261">**倉庫:** *51*</span><span class="sxs-lookup"><span data-stu-id="2c75b-261">**Warehouse:** *51*</span></span>

1. <span data-ttu-id="2c75b-262">**OK** を選択します。</span><span class="sxs-lookup"><span data-stu-id="2c75b-262">Select **OK**.</span></span>
1. <span data-ttu-id="2c75b-263">新しい明細行が、**販売注文明細行** クイック タブに追加されます。</span><span class="sxs-lookup"><span data-stu-id="2c75b-263">A new line is added to the **Sales order lines** FastTab.</span></span> <span data-ttu-id="2c75b-264">この明細行で、次の値を設定します。</span><span class="sxs-lookup"><span data-stu-id="2c75b-264">On this line, set the following values:</span></span>

    - <span data-ttu-id="2c75b-265">**品目番号:** *A0001*</span><span class="sxs-lookup"><span data-stu-id="2c75b-265">**Item number:** *A0001*</span></span>
    - <span data-ttu-id="2c75b-266">**数量:** *3*</span><span class="sxs-lookup"><span data-stu-id="2c75b-266">**Quantity:** *3*</span></span>

### <a name="create-planned-cross-docking"></a><span data-ttu-id="2c75b-267">計画済クロスドッキングの作成</span><span class="sxs-lookup"><span data-stu-id="2c75b-267">Create planned cross-docking</span></span>

<span data-ttu-id="2c75b-268">販売注文から計画済クロスドッキングを作成するには、次の手順に従います。</span><span class="sxs-lookup"><span data-stu-id="2c75b-268">Follow these steps to create the planned cross-docking from the sales order.</span></span>

1. <span data-ttu-id="2c75b-269">作成した販売注文の **販売注文の詳細** ページのアクション ウィンドウにある、**倉庫** タブの **アクション** グループで、**倉庫へのリリース** を選択します。</span><span class="sxs-lookup"><span data-stu-id="2c75b-269">In the **Sales order details** page for the sales order that you just created, on the Action Pane, on the **Warehouse** tab, in the **Actions** group, select **Release to warehouse**.</span></span>

    <span data-ttu-id="2c75b-270">倉庫のリリース アクションによって、販売注文明細行の出荷と積荷明細行が作成され、在庫の配賦が試みられます。</span><span class="sxs-lookup"><span data-stu-id="2c75b-270">The release to warehouse action creates a shipment and load line for the sales order line, and tries to allocate inventory.</span></span>
    
    <span data-ttu-id="2c75b-271">情報メッセージが表示されます。</span><span class="sxs-lookup"><span data-stu-id="2c75b-271">You receive an informational message.</span></span> <span data-ttu-id="2c75b-272">また、「ウェーブ XXXX の作業は作成されませんでした。</span><span class="sxs-lookup"><span data-stu-id="2c75b-272">You also receive the following warning message: "No work was created for wave XXXX.</span></span> <span data-ttu-id="2c75b-273">詳細については、作業の作成履歴ログを参照してください。」という警告メッセージも表示されます。</span><span class="sxs-lookup"><span data-stu-id="2c75b-273">See the work creation history log for details."</span></span> <span data-ttu-id="2c75b-274">倉庫に在庫がないため、この動作が予想されます。</span><span class="sxs-lookup"><span data-stu-id="2c75b-274">This behavior is expected, because there is no inventory in the warehouse.</span></span>

1. <span data-ttu-id="2c75b-275">**販売注文明細行** クイック タブの **倉庫** メニューで、**出荷の詳細** を選択します。</span><span class="sxs-lookup"><span data-stu-id="2c75b-275">On the **Sales order lines** FastTab, on the **Warehouse** menu, select **Shipment details**.</span></span>

    <span data-ttu-id="2c75b-276">**出荷の詳細** ページが表示され、販売注文に対して作成された出荷が表示されます。</span><span class="sxs-lookup"><span data-stu-id="2c75b-276">The **Shipment details** page appears and shows the shipment that was created for the sales order.</span></span>

1. <span data-ttu-id="2c75b-277">**積荷明細行** クイック タブで、**計画済クロスドッキング数量** フィールドが *3* に設定されていることを確認します。</span><span class="sxs-lookup"><span data-stu-id="2c75b-277">On the **Load lines** FastTab, notice that the **Planned cross docking quantity** field is set to *3*.</span></span> <span data-ttu-id="2c75b-278">倉庫には在庫がなくても、有効な供給元がクロスドッキング テンプレートで定義されている時間ウィンドウ内に入庫するため、クロスドッキングの数量が作成されました。</span><span class="sxs-lookup"><span data-stu-id="2c75b-278">Because no inventory was available in the warehouse, but a valid supply source will arrive within the time window that is defined in the cross-docking template, the cross-docking quantity was created.</span></span>
1. <span data-ttu-id="2c75b-279">**積荷明細行** クイック タブで、**計画済クロスドッキング** を選択して、作成されたクロスドッキングの詳細を表示します。</span><span class="sxs-lookup"><span data-stu-id="2c75b-279">On the **Load lines** FastTab, select **Planned cross docking** to view the details of the cross-docking that was created.</span></span>

## <a name="process-the-cross-docking"></a><span data-ttu-id="2c75b-280">クロスドッキングのプロセス</span><span class="sxs-lookup"><span data-stu-id="2c75b-280">Process the cross-docking</span></span>

### <a name="purchase-order-receiving-on-the-warehousing-mobile-app"></a><span data-ttu-id="2c75b-281">倉庫管理モバイル アプリでの発注書の入庫</span><span class="sxs-lookup"><span data-stu-id="2c75b-281">Purchase order receiving on the warehousing mobile app</span></span>

<span data-ttu-id="2c75b-282">発注書から入庫場所に数量 5 が入庫し、2 つの作業がシステムによって作成されます。</span><span class="sxs-lookup"><span data-stu-id="2c75b-282">The system will receive the quantity of 5 from the purchase order into the receiving location and create two pieces of work.</span></span>

<span data-ttu-id="2c75b-283">作成された最初の作業 ID は、**作業指示タイプ** の値が *クロスドッキング* で、販売注文にリンクされています。</span><span class="sxs-lookup"><span data-stu-id="2c75b-283">The first work ID that is created has a **Work order type** value of *Cross docking* and is linked to the sales order.</span></span> <span data-ttu-id="2c75b-284">数量が 3 で、すぐに出荷できるように最終出荷場所に転送されます。</span><span class="sxs-lookup"><span data-stu-id="2c75b-284">It has a quantity of 3 and is directed to the final shipping location so that it can be shipped out immediately.</span></span>

<span data-ttu-id="2c75b-285">作成された 2 つ目の作業 ID は、**作業指示タイプ** の値が *発注書* で、発注書にリンクされています。</span><span class="sxs-lookup"><span data-stu-id="2c75b-285">The second work ID that is created has a **Work order type** value of *Purchase orders* and is linked to the purchase order.</span></span> <span data-ttu-id="2c75b-286">残りの 2 の数量はクロスドッキングされず、ストレージにプットアウェイされます。</span><span class="sxs-lookup"><span data-stu-id="2c75b-286">It has the remaining quantity of 2 that wasn't cross-docked and is directed to put-away to storage.</span></span>

1. <span data-ttu-id="2c75b-287">倉庫 *51* のユーザーとしてモバイル デバイスにサインインします。</span><span class="sxs-lookup"><span data-stu-id="2c75b-287">Sign in to the mobile device as a user in warehouse *51*.</span></span>
1. <span data-ttu-id="2c75b-288">**入庫 \> 購買の入庫** に移動します。</span><span class="sxs-lookup"><span data-stu-id="2c75b-288">Go to **Inbound \> Purchase Receive**.</span></span>
1. <span data-ttu-id="2c75b-289">**PONum** フィールドに発注書番号を入力します。</span><span class="sxs-lookup"><span data-stu-id="2c75b-289">In the **PONum** field, enter your purchase order number.</span></span>
1. <span data-ttu-id="2c75b-290">**数量** フィールドに、*5* と入力します。</span><span class="sxs-lookup"><span data-stu-id="2c75b-290">In the **Qty** field, enter *5*.</span></span>
1. <span data-ttu-id="2c75b-291">**OK** を選択します。</span><span class="sxs-lookup"><span data-stu-id="2c75b-291">Select **OK**.</span></span>
1. <span data-ttu-id="2c75b-292">次のページで、**品目** フィールドを *A0001* に設定します。</span><span class="sxs-lookup"><span data-stu-id="2c75b-292">On the next page, set the **Item** field to *A0001*.</span></span>
1. <span data-ttu-id="2c75b-293">**OK** を選択します。</span><span class="sxs-lookup"><span data-stu-id="2c75b-293">Select **OK**.</span></span>
1. <span data-ttu-id="2c75b-294">次のページで、**OK** を選択して、**PONum**、**品目**、および **数量** の値を確認します。</span><span class="sxs-lookup"><span data-stu-id="2c75b-294">On the next page, confirm the **PONum**, **Item**, and **Qty** values by selecting **OK**.</span></span>

    <span data-ttu-id="2c75b-295">「作業が完了しました」というメッセージが表示されます。</span><span class="sxs-lookup"><span data-stu-id="2c75b-295">You receive a "Work Completed" message.</span></span>

1. <span data-ttu-id="2c75b-296">**キャンセル** を選択して終了します。</span><span class="sxs-lookup"><span data-stu-id="2c75b-296">Select **Cancel** to exit.</span></span>

### <a name="put-away-to-cross-docking-and-bulk"></a><span data-ttu-id="2c75b-297">クロスドッキングおよびバルクへのプットアウェイ</span><span class="sxs-lookup"><span data-stu-id="2c75b-297">Put-away to cross-docking and bulk</span></span>

<span data-ttu-id="2c75b-298">現在、両方の作業 ID のターゲット ライセンス プレートは同じです。</span><span class="sxs-lookup"><span data-stu-id="2c75b-298">Currently, both work IDs have the same target license plate.</span></span> <span data-ttu-id="2c75b-299">次の手順を完了するには、作業 ID とターゲット ライセンス プレート ID を取得する必要があります。</span><span class="sxs-lookup"><span data-stu-id="2c75b-299">To complete the next steps, you must get the work ID and the target license plate ID.</span></span> <span data-ttu-id="2c75b-300">この情報は、注文書明細行および販売注文明細行の作業の詳細から取得できます。</span><span class="sxs-lookup"><span data-stu-id="2c75b-300">You can get this information from the work details for the purchase order line and the sales order line.</span></span> <span data-ttu-id="2c75b-301">または、**倉庫管理 \> 作業 \> 作業の詳細** に移動して、**倉庫** の値が *51* の作業をフィルター処理します。</span><span class="sxs-lookup"><span data-stu-id="2c75b-301">Alternately, you can go to **Warehouse management \> Work \> Work details** and filter for work where the **Warehouse** value is *51*.</span></span>

1. <span data-ttu-id="2c75b-302">モバイル デバイスでは、**入庫 \> 購入品のプットアウェイ** に移動して、作業からターゲット ライセンス プレートを入力します。</span><span class="sxs-lookup"><span data-stu-id="2c75b-302">On the mobile device, go to **Inbound \> Purchase put-away**, and enter the target license plate from the work.</span></span>
1. <span data-ttu-id="2c75b-303">**ID** フィールドに、作業の詳細からターゲット ライセンス プレート ID を入力します。</span><span class="sxs-lookup"><span data-stu-id="2c75b-303">In the **ID** field, enter the target license plate ID from the work details.</span></span>

    <span data-ttu-id="2c75b-304">クロスドッキングのピッキング ページには、ピッキング場所 (*RECV*)、ターゲット ライセンス プレート (*ライセンス プレート*)、品目 (*A0001*)、および数量 (*3*) が表示されます。</span><span class="sxs-lookup"><span data-stu-id="2c75b-304">The cross-docking pick page shows the picking location (*RECV*), target license plate (*license plate*), item (*A0001*), and quantity (*3*).</span></span>

1. <span data-ttu-id="2c75b-305">**OK** を選択します。</span><span class="sxs-lookup"><span data-stu-id="2c75b-305">Select **OK**.</span></span>
1. <span data-ttu-id="2c75b-306">**ターゲット LP** フィールドに、出荷場所にプット (クロスドッキング) するライセンス プレート ID のターゲット ライセンス プレートを入力します。</span><span class="sxs-lookup"><span data-stu-id="2c75b-306">In the **Target LP** field, enter a target license plate for the license plate ID that should be put (cross-docked) to the shipping location.</span></span> <span data-ttu-id="2c75b-307">選択した任意のライセンス プレート ID を選択できます。</span><span class="sxs-lookup"><span data-stu-id="2c75b-307">You can select any license plate ID of your choice.</span></span>
1. <span data-ttu-id="2c75b-308">**OK** を選択します。</span><span class="sxs-lookup"><span data-stu-id="2c75b-308">Select **OK**.</span></span>
1. <span data-ttu-id="2c75b-309">次のページの **ID** フィールドに、ターゲット ライセンス プレート ID を入力します。</span><span class="sxs-lookup"><span data-stu-id="2c75b-309">On the next page, in the **ID** field, enter the target license plate ID.</span></span>
1. <span data-ttu-id="2c75b-310">**OK** を選択します。</span><span class="sxs-lookup"><span data-stu-id="2c75b-310">Select **OK**.</span></span>
1. <span data-ttu-id="2c75b-311">残りの数量 2 をピッキングするための作業を確認し、**OK** を選択します。</span><span class="sxs-lookup"><span data-stu-id="2c75b-311">Confirm the work for picking the remaining quantity of 2, and then select **OK**.</span></span>
1. <span data-ttu-id="2c75b-312">次のページで、**完了** を選択してピッキング プロセスを終了し、プットアウェイ プロセスを開始します。</span><span class="sxs-lookup"><span data-stu-id="2c75b-312">On the next page, select **Done** to end the picking process and begin the put-away process.</span></span>

    <span data-ttu-id="2c75b-313">モバイル アプリでは、品目をプットする場所とライセンス プレートを提供します。</span><span class="sxs-lookup"><span data-stu-id="2c75b-313">The mobile app presents you with the location and license plate to put the item to.</span></span>

1. <span data-ttu-id="2c75b-314">**OK** を選択して、バルク ストレージの **プット** を確認します。</span><span class="sxs-lookup"><span data-stu-id="2c75b-314">Confirm the bulk storage **Put** by selecting **OK**.</span></span>
1. <span data-ttu-id="2c75b-315">次のページで、**OK** を選択して、クロスドッキングの **プット** を確認します。</span><span class="sxs-lookup"><span data-stu-id="2c75b-315">On the next page, confirm the cross-docking **Put** by selecting **OK**.</span></span>

    <span data-ttu-id="2c75b-316">「作業が完了しました」というメッセージが表示されます。</span><span class="sxs-lookup"><span data-stu-id="2c75b-316">You receive a "Work Completed" message.</span></span>

1. <span data-ttu-id="2c75b-317">**キャンセル** を選択して終了します。</span><span class="sxs-lookup"><span data-stu-id="2c75b-317">Select **Cancel** to exit.</span></span>

<span data-ttu-id="2c75b-318">次の図は、完了したクロスドッキング作業が Microsoft Dynamics 365 Supply Chain Management でどのように表示されるかを示しています。</span><span class="sxs-lookup"><span data-stu-id="2c75b-318">The following illustration shows how the completed cross-docking work might appear in Microsoft Dynamics 365 Supply Chain Management.</span></span>

<span data-ttu-id="2c75b-319">![クロスドッキング作業が完了しました](media/PlannedCrossDockingWork.png "クロスドッキング作業が完了しました")</span><span class="sxs-lookup"><span data-stu-id="2c75b-319">![Cross-docking work completed](media/PlannedCrossDockingWork.png "Cross-docking work completed")</span></span>


[!INCLUDE[footer-include](../../includes/footer-banner.md)]