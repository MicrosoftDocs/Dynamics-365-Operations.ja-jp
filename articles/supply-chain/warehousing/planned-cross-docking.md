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
ms.search.region: Global
ms.author: mirzaab
ms.search.validFrom: 2020-07-01
ms.dyn365.ops.version: Release 10.0.7
ms.openlocfilehash: 722b004e607cb2e6b7de292d92b67b18c2024696
ms.sourcegitcommit: 70b1567d316f19c15a4b032b4897f15c8dcdca09
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 03/08/2021
ms.locfileid: "5556269"
---
# <a name="planned-cross-docking"></a><span data-ttu-id="eaeb9-104">計画済クロスドッキング</span><span class="sxs-lookup"><span data-stu-id="eaeb9-104">Planned cross-docking</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="eaeb9-105">このトピックでは、高度な計画済クロスドッキングについて説明します。</span><span class="sxs-lookup"><span data-stu-id="eaeb9-105">This topic describes advanced planned cross-docking.</span></span> <span data-ttu-id="eaeb9-106">クロスドッキングは、注文に必要な在庫数量が受入または作成から正しい出荷ドックまたはステージング領域に直接送られる倉庫プロセスです。</span><span class="sxs-lookup"><span data-stu-id="eaeb9-106">Cross-docking is a warehouse process where the inventory quantity that is required for an order is directed straight from receipt or creation to the correct outbound dock or staging area.</span></span> <span data-ttu-id="eaeb9-107">元伝票からの残りのすべての在庫は、通常のプットアウェイ プロセスによって適切な保管場所に送られます。</span><span class="sxs-lookup"><span data-stu-id="eaeb9-107">All remaining inventory from the inbound source is directed to the correct storage location through the regular put-away process.</span></span>

<span data-ttu-id="eaeb9-108">クロスドッキングにより、作業者は既に出荷注文としてマークされている入荷プットアウェイと出荷ピッキングの手順を省略します。</span><span class="sxs-lookup"><span data-stu-id="eaeb9-108">Cross-docking lets workers skip inbound put-away and outbound picking of inventory that is already marked for an outbound order.</span></span> <span data-ttu-id="eaeb9-109">したがって、在庫の処理回数は可能な限り最小限に抑えられます。</span><span class="sxs-lookup"><span data-stu-id="eaeb9-109">Therefore, the number of times that inventory is touched is minimized, where possible.</span></span> <span data-ttu-id="eaeb9-110">さらに、システムとの相互作用が少ないため、倉庫の作業現場での時間とスペースの節約が増加します。</span><span class="sxs-lookup"><span data-stu-id="eaeb9-110">Additionally, because there is less interaction with the system, time and space savings on the warehouse shop floor are increased.</span></span>

<span data-ttu-id="eaeb9-111">クロスドッキングを実行する前に、ユーザーは新しいクロスドッキング テンプレートを構成する必要があります。このテンプレートでは、クロスドッキングの供給元とその他の要件セットを指定します。</span><span class="sxs-lookup"><span data-stu-id="eaeb9-111">Before cross-docking can be run, the user must configure a new cross-docking template, where the supply source and other sets of requirements for cross-docking are specified.</span></span> <span data-ttu-id="eaeb9-112">出荷注文が作成されると、明細行は同じ品目を含む入荷注文に対してマークされる必要があります。</span><span class="sxs-lookup"><span data-stu-id="eaeb9-112">As the outbound order is created, the line must be marked against an inbound order that contains the same item.</span></span>

<span data-ttu-id="eaeb9-113">入荷注文の受取時に、クロスドッキング設定によってクロスドッキングの必要性が自動的に識別され、場所ディレクティブの設定に基づいて、必要な数量の移動作業が自動的に作成されます。</span><span class="sxs-lookup"><span data-stu-id="eaeb9-113">At the time of inbound order receiving, the cross-docking setup automatically identifies the need for cross-docking and creates the movement work for the required quantity, based on the setup of the location directive.</span></span>

> [!NOTE]
> <span data-ttu-id="eaeb9-114">倉庫管理パラメーターでこの機能の設定が有効になっている場合でも、クロスドッキング作業がキャンセルされると、在庫トランザクションは登録解除 **されません**。</span><span class="sxs-lookup"><span data-stu-id="eaeb9-114">Inventory transactions are **not** unregistered when crossing-dock work is canceled, even if the setting for this capability is turned on in Warehouse management parameters.</span></span>

## <a name="turn-on-the-planned-cross-docking-features"></a><span data-ttu-id="eaeb9-115">計画済クロスドッキング機能を有効にする</span><span class="sxs-lookup"><span data-stu-id="eaeb9-115">Turn on the planned cross docking features</span></span>

<span data-ttu-id="eaeb9-116">このトピックで説明する機能がシステムにまだ含まれていない場合は、[機能管理](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) に移動して、次の機能を次の順序でオンにします:</span><span class="sxs-lookup"><span data-stu-id="eaeb9-116">If your system doesn't already include the features described in this topic, go to [Feature management](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) and turn on the following features in the following order:</span></span>

1. <span data-ttu-id="eaeb9-117">*計画済クロスドッキング*</span><span class="sxs-lookup"><span data-stu-id="eaeb9-117">*Planned cross docking*</span></span>
2. <span data-ttu-id="eaeb9-118">*クロスドッキング テンプレートと場所ディレクティブ*</span><span class="sxs-lookup"><span data-stu-id="eaeb9-118">*Cross docking templates with location directives*</span></span>

## <a name="setup"></a><span data-ttu-id="eaeb9-119">段取り</span><span class="sxs-lookup"><span data-stu-id="eaeb9-119">Setup</span></span>

### <a name="regenerate-load-posting-methods"></a><span data-ttu-id="eaeb9-120">積荷の転記メソッドの再生成</span><span class="sxs-lookup"><span data-stu-id="eaeb9-120">Regenerate load posting methods</span></span>

<span data-ttu-id="eaeb9-121">計画済クロスドッキングは、積荷の転記メソッドとして実装されています。</span><span class="sxs-lookup"><span data-stu-id="eaeb9-121">Planned cross-docking is implemented as a load posting method.</span></span> <span data-ttu-id="eaeb9-122">機能を有効にした後で、方法を再生成する必要があります。</span><span class="sxs-lookup"><span data-stu-id="eaeb9-122">After you turn on the feature, you must regenerate the methods.</span></span>

1. <span data-ttu-id="eaeb9-123">**倉庫管理 \> 設定 \> 積荷の転記メソッド** の順に移動します。</span><span class="sxs-lookup"><span data-stu-id="eaeb9-123">Go to **Warehouse management \> Setup \> Load posting methods**.</span></span>
1. <span data-ttu-id="eaeb9-124">アクション ウィンドウで、**方法の再生成** を選択します。</span><span class="sxs-lookup"><span data-stu-id="eaeb9-124">On the Action Pane, select **Regenerate methods**.</span></span>

    <span data-ttu-id="eaeb9-125">再生成が完了すると、**メソッド名** の値が *planCrossDocking* のメソッドが表示されます。</span><span class="sxs-lookup"><span data-stu-id="eaeb9-125">When regeneration is completed, you should see a method that has a **Method name** value of *planCrossDocking*.</span></span>

1. <span data-ttu-id="eaeb9-126">ページを閉じます。</span><span class="sxs-lookup"><span data-stu-id="eaeb9-126">Close the page.</span></span>

### <a name="create-a-cross-docking-template"></a><span data-ttu-id="eaeb9-127">クロスドッキング テンプレートの作成</span><span class="sxs-lookup"><span data-stu-id="eaeb9-127">Create a cross-docking template</span></span>

1. <span data-ttu-id="eaeb9-128">**倉庫管理 \> 設定 \> 作業 \> クロスドッキング テンプレート** の順に移動します。</span><span class="sxs-lookup"><span data-stu-id="eaeb9-128">Go to **Warehouse management \> Setup \> Work \> Cross docking templates**.</span></span>
1. <span data-ttu-id="eaeb9-129">アクション ウィンドウで **新規** を選択して、テンプレートを作成します。</span><span class="sxs-lookup"><span data-stu-id="eaeb9-129">On the Action Pane, select **New** to create a template.</span></span>
1. <span data-ttu-id="eaeb9-130">ヘッダーで、次の値を設定します。</span><span class="sxs-lookup"><span data-stu-id="eaeb9-130">In the header, set the following values:</span></span>

    - <span data-ttu-id="eaeb9-131">**シーケンス:** *1*</span><span class="sxs-lookup"><span data-stu-id="eaeb9-131">**Sequence:** *1*</span></span>

        <span data-ttu-id="eaeb9-132">このフィールドでは、でテンプレートが評価される順序を定義します。</span><span class="sxs-lookup"><span data-stu-id="eaeb9-132">This field defines the order that templates are evaluated in.</span></span>

    - <span data-ttu-id="eaeb9-133">**クロスドッキング テンプレート ID:** *51*</span><span class="sxs-lookup"><span data-stu-id="eaeb9-133">**Cross docking template ID:** *51*</span></span>
    - <span data-ttu-id="eaeb9-134">**説明 :** *倉庫 51*</span><span class="sxs-lookup"><span data-stu-id="eaeb9-134">**Description:** *Warehouse 51*</span></span>
    - <span data-ttu-id="eaeb9-135">**需要リリース ポリシー :** *供給受領前*</span><span class="sxs-lookup"><span data-stu-id="eaeb9-135">**Demand release policy:** *Before supply receipt*</span></span>
    - <span data-ttu-id="eaeb9-136">**倉庫:** *51*</span><span class="sxs-lookup"><span data-stu-id="eaeb9-136">**Warehouse:** *51*</span></span>

1. <span data-ttu-id="eaeb9-137">**計画** クイック タブでの設定は、テンプレートの動作を制御します。</span><span class="sxs-lookup"><span data-stu-id="eaeb9-137">The setup on the **Planning** FastTab controls how the template works.</span></span> <span data-ttu-id="eaeb9-138">次の値を設定します。</span><span class="sxs-lookup"><span data-stu-id="eaeb9-138">Set the following values:</span></span>

    - <span data-ttu-id="eaeb9-139">**需要の要件 :** *なし*</span><span class="sxs-lookup"><span data-stu-id="eaeb9-139">**Demand requirements:** *None*</span></span>

        <span data-ttu-id="eaeb9-140">このフィールドは、需要在庫の要件を定義します。</span><span class="sxs-lookup"><span data-stu-id="eaeb9-140">This field defines the requirements of the demand inventory.</span></span> <span data-ttu-id="eaeb9-141">リリース前に需要を供給にリンクする必要がある場合は、*マーキング* を選択します。</span><span class="sxs-lookup"><span data-stu-id="eaeb9-141">If the demand must be linked to the supply before release, select *Marking*.</span></span> <span data-ttu-id="eaeb9-142">リリース前に需要を供給に対して注文引当する必要がある場合は、*注文引当* を選択します。</span><span class="sxs-lookup"><span data-stu-id="eaeb9-142">If the demand must be order-reserved against the supply before release, select *Order reservation*.</span></span>

    - <span data-ttu-id="eaeb9-143">**検索タイプ :** *出荷場所*</span><span class="sxs-lookup"><span data-stu-id="eaeb9-143">**Locating type:** *Shipment locations*</span></span>

        <span data-ttu-id="eaeb9-144">このフィールドは、クロスドッキング作業でステージング / 積荷の場所を使用する必要があるかどうか、または、独自のステージング / 積荷の場所の検索に場所ディレクティブを使用するかどうかを定義します。</span><span class="sxs-lookup"><span data-stu-id="eaeb9-144">This field defines whether the cross-docking work should use the staging/load locations from the shipment, or whether it should use location directives to find its own staging/load locations.</span></span>

    - <span data-ttu-id="eaeb9-145">**作業テンプレート** このフィールドは空白のままにしておきます。</span><span class="sxs-lookup"><span data-stu-id="eaeb9-145">**Work template:** Leave this field blank.</span></span>

        <span data-ttu-id="eaeb9-146">このフィールドでは、クロスドッキング作業を作成するときに使用する作業テンプレートを定義します。</span><span class="sxs-lookup"><span data-stu-id="eaeb9-146">This field defines the work template that should be used when cross-docking work is created.</span></span>

    - <span data-ttu-id="eaeb9-147">**供給受領の再検証 :** *いいえ*</span><span class="sxs-lookup"><span data-stu-id="eaeb9-147">**Revalidate on supply receipt:** *No*</span></span>

        <span data-ttu-id="eaeb9-148">このオプションは、受領時に供給を再検証するかどうかを定義します。</span><span class="sxs-lookup"><span data-stu-id="eaeb9-148">This option defines whether the supply should be revalidated during receipt.</span></span> <span data-ttu-id="eaeb9-149">このオプションが *はい* に設定されている場合は、最大時間ウィンドウと有効期限の日付範囲の両方がチェックされます。</span><span class="sxs-lookup"><span data-stu-id="eaeb9-149">If this option is set to *Yes*, both the maximum time window and the expiration days range are checked.</span></span>

    - <span data-ttu-id="eaeb9-150">**ディレクティブ コード** このフィールドは空白のままにします</span><span class="sxs-lookup"><span data-stu-id="eaeb9-150">**Directive code** Leave this field blank</span></span>

        <span data-ttu-id="eaeb9-151">このオプションを選択すると、場所ディレクティブを使用することで、クロスドッキング在庫の移動の最適な場所を決定できます。</span><span class="sxs-lookup"><span data-stu-id="eaeb9-151">This option enables the system to use location directives to help determine the best location to move cross-docking inventory to.</span></span> <span data-ttu-id="eaeb9-152">関連する各クロスドッキング テンプレートにディレクティブ コードを割り当てると、このコードを設定できます。</span><span class="sxs-lookup"><span data-stu-id="eaeb9-152">You can set it up by assigning a directive code to each relevant cross-docking template.</span></span> <span data-ttu-id="eaeb9-153">各ディレクティブ コードは、一意の場所のディレクティブを識別します。</span><span class="sxs-lookup"><span data-stu-id="eaeb9-153">Each directive code identifies a unique location directive.</span></span>

    - <span data-ttu-id="eaeb9-154">**時間ウィンドウの検証 :** *はい*</span><span class="sxs-lookup"><span data-stu-id="eaeb9-154">**Validate time window:** *Yes*</span></span>

        <span data-ttu-id="eaeb9-155">このオプションは、供給元を選択したときに最大時間ウィンドウを評価するかどうかを定義します。</span><span class="sxs-lookup"><span data-stu-id="eaeb9-155">This option defines whether the maximum time window should be evaluated when a supply source is selected.</span></span> <span data-ttu-id="eaeb9-156">このオプションが *はい* に設定されている場合は、最大および最小時間ウィンドウに関連するフィールドが使用可能になります。</span><span class="sxs-lookup"><span data-stu-id="eaeb9-156">If this option is set to *Yes*, the fields that are related to the maximum and minimum time windows become available.</span></span>

    - <span data-ttu-id="eaeb9-157">**最大時間ウィンドウ :** *5*</span><span class="sxs-lookup"><span data-stu-id="eaeb9-157">**Maximum time window:** *5*</span></span>

        <span data-ttu-id="eaeb9-158">このフィールドでは、供給到着から需要出発までの間で許可される最大期間を定義します。</span><span class="sxs-lookup"><span data-stu-id="eaeb9-158">This field defines the maximum period that is allowed between supply arrival and demand departure.</span></span>

    - <span data-ttu-id="eaeb9-159">**最大時間ウィンドウの単位 :** *日*</span><span class="sxs-lookup"><span data-stu-id="eaeb9-159">**Maximum time window unit:** *Days*</span></span>
    - <span data-ttu-id="eaeb9-160">**最小時間ウィンドウ :** *0*</span><span class="sxs-lookup"><span data-stu-id="eaeb9-160">**Minimum time window:** *0*</span></span>

        <span data-ttu-id="eaeb9-161">このフィールドでは、供給到着から需要出発までの間で許可される最小期間を定義します。</span><span class="sxs-lookup"><span data-stu-id="eaeb9-161">This field defines the minimum period that is allowed between supply arrival and demand departure.</span></span>

    - <span data-ttu-id="eaeb9-162">**最小時間ウィンドウの単位 :** *日*</span><span class="sxs-lookup"><span data-stu-id="eaeb9-162">**Minimum time window unit:** *Days*</span></span>
    - <span data-ttu-id="eaeb9-163">**有効期限の日付範囲 :** *0*</span><span class="sxs-lookup"><span data-stu-id="eaeb9-163">**Expiration days range:** *0*</span></span>

        <span data-ttu-id="eaeb9-164">*先入れ先出し (FEFO) 基準 :* このフィールドでは、現在倉庫にある最初に失効するバッチの有効期限から、受入中のバッチまでの最大日数を定義します。</span><span class="sxs-lookup"><span data-stu-id="eaeb9-164">*First expiry first out (FEFO) criteria:* This field defines the maximum number of days between the expiration date of the first-expiring batch that is currently in the warehouse and the batch that is being received.</span></span>

1. <span data-ttu-id="eaeb9-165">**供給元** クイック タブで、このテンプレートに対して有効な供給タイプを指定します。</span><span class="sxs-lookup"><span data-stu-id="eaeb9-165">On the **Supply sources** FastTab, you specify the types of supply that are valid for this template.</span></span> <span data-ttu-id="eaeb9-166">**新規** を選択して、次の値を設定します。</span><span class="sxs-lookup"><span data-stu-id="eaeb9-166">Select **New**, and then set the following values:</span></span>

    - <span data-ttu-id="eaeb9-167">**シーケンス番号:** *1*</span><span class="sxs-lookup"><span data-stu-id="eaeb9-167">**Sequence number:** *1*</span></span>
    - <span data-ttu-id="eaeb9-168">**供給元 :** *発注書*</span><span class="sxs-lookup"><span data-stu-id="eaeb9-168">**Supply source:** *Purchase order*</span></span>

### <a name="create-a-work-class"></a><span data-ttu-id="eaeb9-169">作業クラスの作成</span><span class="sxs-lookup"><span data-stu-id="eaeb9-169">Create a work class</span></span>

1. <span data-ttu-id="eaeb9-170">**倉庫管理 \> 設定 \> 作業 \> 作業クラス** の順に移動します。</span><span class="sxs-lookup"><span data-stu-id="eaeb9-170">Go to **Warehouse management \> Setup \> Work \> Work classes**.</span></span>
1. <span data-ttu-id="eaeb9-171">アクション ウィンドウで **新規** を選択し、作業クラスを作成します。</span><span class="sxs-lookup"><span data-stu-id="eaeb9-171">On the Action Pane, select **New** to create a work class.</span></span>
1. <span data-ttu-id="eaeb9-172">次の値を設定します。</span><span class="sxs-lookup"><span data-stu-id="eaeb9-172">Set the following values:</span></span>

    - <span data-ttu-id="eaeb9-173">**作業クラス ID:** *CrossDock*</span><span class="sxs-lookup"><span data-stu-id="eaeb9-173">**Work class ID:** *CrossDock*</span></span>
    - <span data-ttu-id="eaeb9-174">**説明 :** *クロスドッキング*</span><span class="sxs-lookup"><span data-stu-id="eaeb9-174">**Description:** *Cross Dock*</span></span>
    - <span data-ttu-id="eaeb9-175">**作業指示書タイプ :** *クロスドッキング*</span><span class="sxs-lookup"><span data-stu-id="eaeb9-175">**Work order type:** *Cross docking*</span></span>

### <a name="create-a-work-template"></a><span data-ttu-id="eaeb9-176">作業テンプレートの作成</span><span class="sxs-lookup"><span data-stu-id="eaeb9-176">Create a work template</span></span>

1. <span data-ttu-id="eaeb9-177">**倉庫管理 \> 設定 \> 作業 \> 作業テンプレート** の順に移動します。</span><span class="sxs-lookup"><span data-stu-id="eaeb9-177">Go to **Warehouse management \> Setup \> Work \> Work templates**.</span></span>
1. <span data-ttu-id="eaeb9-178">**作業指示書タイプ** フィールドを *クロスドッキング* に設定します。</span><span class="sxs-lookup"><span data-stu-id="eaeb9-178">Set the **Work order type** field to *Cross docking*.</span></span>
1. <span data-ttu-id="eaeb9-179">アクション ウィンドウで **新規** を選択して、明細行を **概要** タブに追加します。</span><span class="sxs-lookup"><span data-stu-id="eaeb9-179">On the Action Pane, select **New** to add a line to the **Overview** tab.</span></span>
1. <span data-ttu-id="eaeb9-180">新しい明細行で、次の値を設定します。</span><span class="sxs-lookup"><span data-stu-id="eaeb9-180">On the new line, set the following values:</span></span>

    - <span data-ttu-id="eaeb9-181">**シーケンス番号 :** *1*</span><span class="sxs-lookup"><span data-stu-id="eaeb9-181">**Sequence number:** *1*</span></span>
    - <span data-ttu-id="eaeb9-182">**作業テンプレート ID:** *51 クロスドッキング*</span><span class="sxs-lookup"><span data-stu-id="eaeb9-182">**Work template:** *51 Cross Dock*</span></span>
    - <span data-ttu-id="eaeb9-183">**作業テンプレートの説明 :** *51 クロスドッキング*</span><span class="sxs-lookup"><span data-stu-id="eaeb9-183">**Work template description:** *51 Cross Dock*</span></span>

1. <span data-ttu-id="eaeb9-184">**保存** を選択して、**作業テンプレートの詳細** クイック タブを使用できるようにします。</span><span class="sxs-lookup"><span data-stu-id="eaeb9-184">Select **Save** to make the **Work Template Details** FastTab available.</span></span>
1. <span data-ttu-id="eaeb9-185">**作業テンプレートの詳細** クイック タブで、**新規** を選択してグリッドに明細行を追加します。</span><span class="sxs-lookup"><span data-stu-id="eaeb9-185">On the **Work Template Details** FastTab, select **New** to add a line to the grid.</span></span>
1. <span data-ttu-id="eaeb9-186">新しい明細行で、次の値を設定します。</span><span class="sxs-lookup"><span data-stu-id="eaeb9-186">On the new line, set the following values:</span></span>

    - <span data-ttu-id="eaeb9-187">**作業タイプ:** *ピッキング*</span><span class="sxs-lookup"><span data-stu-id="eaeb9-187">**Work type:** *Pick*</span></span>
    - <span data-ttu-id="eaeb9-188">**作業クラス ID:** *CrossDock*</span><span class="sxs-lookup"><span data-stu-id="eaeb9-188">**Work class ID:** *CrossDock*</span></span>

1. <span data-ttu-id="eaeb9-189">**新規** を選択して別の明細行を追加し、次の値を設定します。</span><span class="sxs-lookup"><span data-stu-id="eaeb9-189">Select **New** to add another line, and set the following values on it:</span></span>

    - <span data-ttu-id="eaeb9-190">**作業タイプ:** *プット*</span><span class="sxs-lookup"><span data-stu-id="eaeb9-190">**Work type:** *Put*</span></span>
    - <span data-ttu-id="eaeb9-191">**作業クラス ID:** *CrossDock*</span><span class="sxs-lookup"><span data-stu-id="eaeb9-191">**Work class ID:** *CrossDock*</span></span>

1. <span data-ttu-id="eaeb9-192">**保存** を選択して、*51 クロスドッキング* テンプレートの **有効** チェック ボックスがオンになっていることを確認します。</span><span class="sxs-lookup"><span data-stu-id="eaeb9-192">Select **Save**, and confirm that the **Valid** check box is selected for the *51 Cross Dock* template.</span></span>

> [!NOTE]
> <span data-ttu-id="eaeb9-193">*ピッキング* と *プット* の作業タイプの作業クラス ID は同じである必要があります。</span><span class="sxs-lookup"><span data-stu-id="eaeb9-193">The work class IDs for the *Pick* and *Put* work types must be the same.</span></span>

### <a name="create-location-directives"></a><span data-ttu-id="eaeb9-194">場所ディレクティブを作成する</span><span class="sxs-lookup"><span data-stu-id="eaeb9-194">Create location directives</span></span>

1. <span data-ttu-id="eaeb9-195">**倉庫管理 \> 設定 \> 場所のディレクティブ** に移動します。</span><span class="sxs-lookup"><span data-stu-id="eaeb9-195">Go to **Warehouse management \> Setup \> Location directives**.</span></span>
1. <span data-ttu-id="eaeb9-196">左ウィンドウで、**作業指示書タイプ** フィールドを *クロスドッキング* に設定します。</span><span class="sxs-lookup"><span data-stu-id="eaeb9-196">In the left pane, set the **Work order type** field to *Cross docking*.</span></span>
1. <span data-ttu-id="eaeb9-197">アクション ウィンドウで、**新規** を選択し、次の値を設定します。</span><span class="sxs-lookup"><span data-stu-id="eaeb9-197">On the Action Pane, select **New**, and set the following values:</span></span>

    - <span data-ttu-id="eaeb9-198">**シーケンス番号 :** *1*</span><span class="sxs-lookup"><span data-stu-id="eaeb9-198">**Sequence number:** *1*</span></span>
    - <span data-ttu-id="eaeb9-199">**名前 :** *51 クロスドッキング プット*</span><span class="sxs-lookup"><span data-stu-id="eaeb9-199">**Name:** *51 Cross Dock Put*</span></span>
    - <span data-ttu-id="eaeb9-200">**作業タイプ:** *プット*</span><span class="sxs-lookup"><span data-stu-id="eaeb9-200">**Work type:** *Put*</span></span>
    - <span data-ttu-id="eaeb9-201">**サイト:** *5*</span><span class="sxs-lookup"><span data-stu-id="eaeb9-201">**Site:** *5*</span></span>
    - <span data-ttu-id="eaeb9-202">**倉庫:** *51*</span><span class="sxs-lookup"><span data-stu-id="eaeb9-202">**Warehouse:** *51*</span></span>

1. <span data-ttu-id="eaeb9-203">**保存** を選択して、**明細行** クイック タブを使用できるようにします。</span><span class="sxs-lookup"><span data-stu-id="eaeb9-203">Select **Save** to make the **Lines** FastTab available.</span></span>
1. <span data-ttu-id="eaeb9-204">**明細行** クイック タブで、**新規** を選択してグリッドに明細行を追加します。</span><span class="sxs-lookup"><span data-stu-id="eaeb9-204">On the **Lines** FastTab, select **New** to add a line to the grid.</span></span>
1. <span data-ttu-id="eaeb9-205">新しい明細行で、次の値を設定します。</span><span class="sxs-lookup"><span data-stu-id="eaeb9-205">On the new line, set the following values:</span></span>

    - <span data-ttu-id="eaeb9-206">**開始数量:** *1*</span><span class="sxs-lookup"><span data-stu-id="eaeb9-206">**From quantity:** *1*</span></span>
    - <span data-ttu-id="eaeb9-207">**上限数量:** *1000000*</span><span class="sxs-lookup"><span data-stu-id="eaeb9-207">**To quantity:** *1,000,000*</span></span>

1. <span data-ttu-id="eaeb9-208">**保存** を選択して、**場所ディレクティブ アクション** クイック タブを使用できるようにします。</span><span class="sxs-lookup"><span data-stu-id="eaeb9-208">Select **Save** to make the **Location Directive Actions** FastTab available.</span></span>
1. <span data-ttu-id="eaeb9-209">**場所ディレクティブ アクション** クイック タブで、**新規** を選択してグリッドに明細行を追加します。</span><span class="sxs-lookup"><span data-stu-id="eaeb9-209">On the **Location Directive Actions** FastTab, select **New** to add a line to the grid.</span></span>
1. <span data-ttu-id="eaeb9-210">新しい明細行で、次の値を設定します。</span><span class="sxs-lookup"><span data-stu-id="eaeb9-210">On the new line, set the following values:</span></span>

    - <span data-ttu-id="eaeb9-211">**名前 :** *ベイドア*</span><span class="sxs-lookup"><span data-stu-id="eaeb9-211">**Name:** *Baydoor*</span></span>
    - <span data-ttu-id="eaeb9-212">**固定の場所の使用 :** *固定の場所および固定されていない場所*</span><span class="sxs-lookup"><span data-stu-id="eaeb9-212">**Fixed location usage:** *Fixed and non-fixed locations*</span></span>

1. <span data-ttu-id="eaeb9-213">**保存** を選択すると、**場所ディレクティブ アクション** のツール バーにある **クエリの編集** ボタンが使用できるようになります。</span><span class="sxs-lookup"><span data-stu-id="eaeb9-213">Select **Save** to make the **Edit query** button on the **Location Directive Actions** toolbar available.</span></span>
1. <span data-ttu-id="eaeb9-214">**クエリの編集** を選択して、クエリ エディターを開きます。</span><span class="sxs-lookup"><span data-stu-id="eaeb9-214">Select **Edit query** to open the query editor.</span></span>
1. <span data-ttu-id="eaeb9-215">**範囲** タブで、次の 2 つの明細行が構成されていることを確認します。</span><span class="sxs-lookup"><span data-stu-id="eaeb9-215">On the **Range** tab, make sure that the following two lines are configured:</span></span>

    - <span data-ttu-id="eaeb9-216">明細行 1:</span><span class="sxs-lookup"><span data-stu-id="eaeb9-216">Line 1:</span></span>

        - <span data-ttu-id="eaeb9-217">**テーブル:** *場所*</span><span class="sxs-lookup"><span data-stu-id="eaeb9-217">**Table:** *Locations*</span></span>
        - <span data-ttu-id="eaeb9-218">**派生テーブル :** *場所*</span><span class="sxs-lookup"><span data-stu-id="eaeb9-218">**Derived Table:** *Locations*</span></span>
        - <span data-ttu-id="eaeb9-219">**フィールド :** *倉庫*</span><span class="sxs-lookup"><span data-stu-id="eaeb9-219">**Field:** *Warehouse*</span></span>
        - <span data-ttu-id="eaeb9-220">**基準 :** *51*</span><span class="sxs-lookup"><span data-stu-id="eaeb9-220">**Criteria:** *51*</span></span>

    - <span data-ttu-id="eaeb9-221">明細行 2:</span><span class="sxs-lookup"><span data-stu-id="eaeb9-221">Line 2:</span></span>

        - <span data-ttu-id="eaeb9-222">**テーブル:** *場所*</span><span class="sxs-lookup"><span data-stu-id="eaeb9-222">**Table:** *Locations*</span></span>
        - <span data-ttu-id="eaeb9-223">**派生テーブル :** *場所*</span><span class="sxs-lookup"><span data-stu-id="eaeb9-223">**Derived Table:** *Locations*</span></span>
        - <span data-ttu-id="eaeb9-224">**フィールド :** *場所*</span><span class="sxs-lookup"><span data-stu-id="eaeb9-224">**Field:** *Location*</span></span>
        - <span data-ttu-id="eaeb9-225">**基準 :** *ベイドア*</span><span class="sxs-lookup"><span data-stu-id="eaeb9-225">**Criteria:** *Baydoor*</span></span>

1. <span data-ttu-id="eaeb9-226">**OK** を選択してクエリ エディターを閉じます。</span><span class="sxs-lookup"><span data-stu-id="eaeb9-226">Select **OK** to close the query editor.</span></span>

### <a name="create-a-mobile-device-menu-item"></a><span data-ttu-id="eaeb9-227">品目のモバイル デバイス メニューの作成</span><span class="sxs-lookup"><span data-stu-id="eaeb9-227">Create a mobile device menu item</span></span>

1. <span data-ttu-id="eaeb9-228">**倉庫管理 \> 設定 \> モバイル デバイス \> モバイル デバイスのメニュー品目** の順に移動します。</span><span class="sxs-lookup"><span data-stu-id="eaeb9-228">Go to **Warehouse management \> Setup \> Mobile device \> Mobile device menu items**.</span></span>
1. <span data-ttu-id="eaeb9-229">左ウィンドウのメニュー項目の一覧で、**購入品のプットアウェイ** を選択します。</span><span class="sxs-lookup"><span data-stu-id="eaeb9-229">In the list of menu items in the left pane, select **Purchase Put-away**.</span></span>
1. <span data-ttu-id="eaeb9-230">**編集** を選択します。</span><span class="sxs-lookup"><span data-stu-id="eaeb9-230">Select **Edit**.</span></span>
1. <span data-ttu-id="eaeb9-231">**作業クラス** クイック タブで、**新規** を選択してグリッドに明細行を追加します。</span><span class="sxs-lookup"><span data-stu-id="eaeb9-231">On the **Work classes** FastTab, select **New** to add a line to the grid.</span></span>
1. <span data-ttu-id="eaeb9-232">新しい明細行で、次の値を設定します。</span><span class="sxs-lookup"><span data-stu-id="eaeb9-232">On the new line, set the following values:</span></span>

    - <span data-ttu-id="eaeb9-233">**作業クラス ID:** *CrossDock*</span><span class="sxs-lookup"><span data-stu-id="eaeb9-233">**Work class ID:** *CrossDock*</span></span>
    - <span data-ttu-id="eaeb9-234">**作業指示書タイプ :** *クロスドッキング*</span><span class="sxs-lookup"><span data-stu-id="eaeb9-234">**Work order type:** *Cross docking*</span></span>

1. <span data-ttu-id="eaeb9-235">**保存** を選択します。</span><span class="sxs-lookup"><span data-stu-id="eaeb9-235">Select **Save**.</span></span>

## <a name="scenario"></a><span data-ttu-id="eaeb9-236">シナリオ</span><span class="sxs-lookup"><span data-stu-id="eaeb9-236">Scenario</span></span>

### <a name="create-a-purchase-order"></a><span data-ttu-id="eaeb9-237">発注書の作成</span><span class="sxs-lookup"><span data-stu-id="eaeb9-237">Create a purchase order</span></span>

<span data-ttu-id="eaeb9-238">発注書を供給元として作成するには、次の手順に従います。</span><span class="sxs-lookup"><span data-stu-id="eaeb9-238">Follow these steps to create a purchase order as a source of supply.</span></span>

1. <span data-ttu-id="eaeb9-239">**調達 \> 発注書 \> すべての発注書** に移動します。</span><span class="sxs-lookup"><span data-stu-id="eaeb9-239">Go to **Procurement and sourcing \> Purchase orders \> All purchase orders**.</span></span>
1. <span data-ttu-id="eaeb9-240">アクション ウィンドウで、**新規** を選択します。</span><span class="sxs-lookup"><span data-stu-id="eaeb9-240">On the Action Pane, select **New**.</span></span>
1. <span data-ttu-id="eaeb9-241">**発注書の作成** ダイアログ ボックスで、次の値を設定します。</span><span class="sxs-lookup"><span data-stu-id="eaeb9-241">In the **Create purchase order** dialog box, set the following values:</span></span>

    - <span data-ttu-id="eaeb9-242">**仕入先勘定 :** *104*</span><span class="sxs-lookup"><span data-stu-id="eaeb9-242">**Vendor account:** *104*</span></span>
    - <span data-ttu-id="eaeb9-243">**倉庫:** *51*</span><span class="sxs-lookup"><span data-stu-id="eaeb9-243">**Warehouse:** *51*</span></span>

1. <span data-ttu-id="eaeb9-244">**OK** を選択し、注文番号をメモします。</span><span class="sxs-lookup"><span data-stu-id="eaeb9-244">Select **OK**, and make a note of the order number.</span></span>
1. <span data-ttu-id="eaeb9-245">新しい明細行が、**発注書明細行** クイック タブに追加されます。</span><span class="sxs-lookup"><span data-stu-id="eaeb9-245">A new line is added to the **Purchase order lines** FastTab.</span></span> <span data-ttu-id="eaeb9-246">この明細行で、次の値を設定します。</span><span class="sxs-lookup"><span data-stu-id="eaeb9-246">On this line, set the following values:</span></span>

    - <span data-ttu-id="eaeb9-247">**品目番号:** *A0001*</span><span class="sxs-lookup"><span data-stu-id="eaeb9-247">**Item number:** *A0001*</span></span>
    - <span data-ttu-id="eaeb9-248">**数量:** *5*</span><span class="sxs-lookup"><span data-stu-id="eaeb9-248">**Quantity:** *5*</span></span>

### <a name="create-a-sales-order"></a><span data-ttu-id="eaeb9-249">販売注文の作成</span><span class="sxs-lookup"><span data-stu-id="eaeb9-249">Create a sales order</span></span>

<span data-ttu-id="eaeb9-250">販売注文を需要元として作成するには、次の手順に従います。</span><span class="sxs-lookup"><span data-stu-id="eaeb9-250">Follow these steps to create a sales order as a source of demand.</span></span>

1. <span data-ttu-id="eaeb9-251">**販売とマーケティング \> 販売注文 \> すべての販売注文** の順に移動します。</span><span class="sxs-lookup"><span data-stu-id="eaeb9-251">Go to **Sales and marketing \> Sales orders \> All sales orders**.</span></span>
1. <span data-ttu-id="eaeb9-252">アクション ウィンドウで、**新規** を選択します。</span><span class="sxs-lookup"><span data-stu-id="eaeb9-252">On the Action Pane, select **New**.</span></span>
1. <span data-ttu-id="eaeb9-253">**販売注文の作成** ダイアログ ボックスでは、次の値を設定します。</span><span class="sxs-lookup"><span data-stu-id="eaeb9-253">In the **Create sales order** dialog box, set the following values:</span></span>

    - <span data-ttu-id="eaeb9-254">**顧客アカウント:** *US-002*</span><span class="sxs-lookup"><span data-stu-id="eaeb9-254">**Customer account:** *US-002*</span></span>
    - <span data-ttu-id="eaeb9-255">**倉庫:** *51*</span><span class="sxs-lookup"><span data-stu-id="eaeb9-255">**Warehouse:** *51*</span></span>

1. <span data-ttu-id="eaeb9-256">**OK** を選択します。</span><span class="sxs-lookup"><span data-stu-id="eaeb9-256">Select **OK**.</span></span>
1. <span data-ttu-id="eaeb9-257">新しい明細行が、**販売注文明細行** クイック タブに追加されます。</span><span class="sxs-lookup"><span data-stu-id="eaeb9-257">A new line is added to the **Sales order lines** FastTab.</span></span> <span data-ttu-id="eaeb9-258">この明細行で、次の値を設定します。</span><span class="sxs-lookup"><span data-stu-id="eaeb9-258">On this line, set the following values:</span></span>

    - <span data-ttu-id="eaeb9-259">**品目番号:** *A0001*</span><span class="sxs-lookup"><span data-stu-id="eaeb9-259">**Item number:** *A0001*</span></span>
    - <span data-ttu-id="eaeb9-260">**数量:** *3*</span><span class="sxs-lookup"><span data-stu-id="eaeb9-260">**Quantity:** *3*</span></span>

### <a name="create-planned-cross-docking"></a><span data-ttu-id="eaeb9-261">計画済クロスドッキングの作成</span><span class="sxs-lookup"><span data-stu-id="eaeb9-261">Create planned cross-docking</span></span>

<span data-ttu-id="eaeb9-262">販売注文から計画済クロスドッキングを作成するには、次の手順に従います。</span><span class="sxs-lookup"><span data-stu-id="eaeb9-262">Follow these steps to create the planned cross-docking from the sales order.</span></span>

1. <span data-ttu-id="eaeb9-263">作成した販売注文の **販売注文の詳細** ページのアクション ウィンドウにある、**倉庫** タブの **アクション** グループで、**倉庫へのリリース** を選択します。</span><span class="sxs-lookup"><span data-stu-id="eaeb9-263">In the **Sales order details** page for the sales order that you just created, on the Action Pane, on the **Warehouse** tab, in the **Actions** group, select **Release to warehouse**.</span></span>

    <span data-ttu-id="eaeb9-264">倉庫のリリース アクションによって、販売注文明細行の出荷と積荷明細行が作成され、在庫の配賦が試みられます。</span><span class="sxs-lookup"><span data-stu-id="eaeb9-264">The release to warehouse action creates a shipment and load line for the sales order line, and tries to allocate inventory.</span></span>
    
    <span data-ttu-id="eaeb9-265">情報メッセージが表示されます。</span><span class="sxs-lookup"><span data-stu-id="eaeb9-265">You receive an informational message.</span></span> <span data-ttu-id="eaeb9-266">また、「ウェーブ XXXX の作業は作成されませんでした。</span><span class="sxs-lookup"><span data-stu-id="eaeb9-266">You also receive the following warning message: "No work was created for wave XXXX.</span></span> <span data-ttu-id="eaeb9-267">詳細については、作業の作成履歴ログを参照してください。」という警告メッセージも表示されます。</span><span class="sxs-lookup"><span data-stu-id="eaeb9-267">See the work creation history log for details."</span></span> <span data-ttu-id="eaeb9-268">倉庫に在庫がないため、この動作が予想されます。</span><span class="sxs-lookup"><span data-stu-id="eaeb9-268">This behavior is expected, because there is no inventory in the warehouse.</span></span>

1. <span data-ttu-id="eaeb9-269">**販売注文明細行** クイック タブの **倉庫** メニューで、**出荷の詳細** を選択します。</span><span class="sxs-lookup"><span data-stu-id="eaeb9-269">On the **Sales order lines** FastTab, on the **Warehouse** menu, select **Shipment details**.</span></span>

    <span data-ttu-id="eaeb9-270">**出荷の詳細** ページが表示され、販売注文に対して作成された出荷が表示されます。</span><span class="sxs-lookup"><span data-stu-id="eaeb9-270">The **Shipment details** page appears and shows the shipment that was created for the sales order.</span></span>

1. <span data-ttu-id="eaeb9-271">**積荷明細行** クイック タブで、**計画済クロスドッキング数量** フィールドが *3* に設定されていることを確認します。</span><span class="sxs-lookup"><span data-stu-id="eaeb9-271">On the **Load lines** FastTab, notice that the **Planned cross docking quantity** field is set to *3*.</span></span> <span data-ttu-id="eaeb9-272">倉庫には在庫がなくても、有効な供給元がクロスドッキング テンプレートで定義されている時間ウィンドウ内に入庫するため、クロスドッキングの数量が作成されました。</span><span class="sxs-lookup"><span data-stu-id="eaeb9-272">Because no inventory was available in the warehouse, but a valid supply source will arrive within the time window that is defined in the cross-docking template, the cross-docking quantity was created.</span></span>
1. <span data-ttu-id="eaeb9-273">**積荷明細行** クイック タブで、**計画済クロスドッキング** を選択して、作成されたクロスドッキングの詳細を表示します。</span><span class="sxs-lookup"><span data-stu-id="eaeb9-273">On the **Load lines** FastTab, select **Planned cross docking** to view the details of the cross-docking that was created.</span></span>

## <a name="process-the-cross-docking"></a><span data-ttu-id="eaeb9-274">クロスドッキングのプロセス</span><span class="sxs-lookup"><span data-stu-id="eaeb9-274">Process the cross-docking</span></span>

### <a name="purchase-order-receiving-on-the-warehousing-mobile-app"></a><span data-ttu-id="eaeb9-275">倉庫管理モバイル アプリでの発注書の入庫</span><span class="sxs-lookup"><span data-stu-id="eaeb9-275">Purchase order receiving on the warehousing mobile app</span></span>

<span data-ttu-id="eaeb9-276">発注書から入庫場所に数量 5 が入庫し、2 つの作業がシステムによって作成されます。</span><span class="sxs-lookup"><span data-stu-id="eaeb9-276">The system will receive the quantity of 5 from the purchase order into the receiving location and create two pieces of work.</span></span>

<span data-ttu-id="eaeb9-277">作成された最初の作業 ID は、**作業指示タイプ** の値が *クロスドッキング* で、販売注文にリンクされています。</span><span class="sxs-lookup"><span data-stu-id="eaeb9-277">The first work ID that is created has a **Work order type** value of *Cross docking* and is linked to the sales order.</span></span> <span data-ttu-id="eaeb9-278">数量が 3 で、すぐに出荷できるように最終出荷場所に転送されます。</span><span class="sxs-lookup"><span data-stu-id="eaeb9-278">It has a quantity of 3 and is directed to the final shipping location so that it can be shipped out immediately.</span></span>

<span data-ttu-id="eaeb9-279">作成された 2 つ目の作業 ID は、**作業指示タイプ** の値が *発注書* で、発注書にリンクされています。</span><span class="sxs-lookup"><span data-stu-id="eaeb9-279">The second work ID that is created has a **Work order type** value of *Purchase orders* and is linked to the purchase order.</span></span> <span data-ttu-id="eaeb9-280">残りの 2 の数量はクロスドッキングされず、ストレージにプットアウェイされます。</span><span class="sxs-lookup"><span data-stu-id="eaeb9-280">It has the remaining quantity of 2 that wasn't cross-docked and is directed to put-away to storage.</span></span>

1. <span data-ttu-id="eaeb9-281">倉庫 *51* のユーザーとしてモバイル デバイスにサインインします。</span><span class="sxs-lookup"><span data-stu-id="eaeb9-281">Sign in to the mobile device as a user in warehouse *51*.</span></span>
1. <span data-ttu-id="eaeb9-282">**入庫 \> 購買の入庫** に移動します。</span><span class="sxs-lookup"><span data-stu-id="eaeb9-282">Go to **Inbound \> Purchase Receive**.</span></span>
1. <span data-ttu-id="eaeb9-283">**PONum** フィールドに発注書番号を入力します。</span><span class="sxs-lookup"><span data-stu-id="eaeb9-283">In the **PONum** field, enter your purchase order number.</span></span>
1. <span data-ttu-id="eaeb9-284">**数量** フィールドに、*5* と入力します。</span><span class="sxs-lookup"><span data-stu-id="eaeb9-284">In the **Qty** field, enter *5*.</span></span>
1. <span data-ttu-id="eaeb9-285">**OK** を選択します。</span><span class="sxs-lookup"><span data-stu-id="eaeb9-285">Select **OK**.</span></span>
1. <span data-ttu-id="eaeb9-286">次のページで、**品目** フィールドを *A0001* に設定します。</span><span class="sxs-lookup"><span data-stu-id="eaeb9-286">On the next page, set the **Item** field to *A0001*.</span></span>
1. <span data-ttu-id="eaeb9-287">**OK** を選択します。</span><span class="sxs-lookup"><span data-stu-id="eaeb9-287">Select **OK**.</span></span>
1. <span data-ttu-id="eaeb9-288">次のページで、**OK** を選択して、**PONum**、**品目**、および **数量** の値を確認します。</span><span class="sxs-lookup"><span data-stu-id="eaeb9-288">On the next page, confirm the **PONum**, **Item**, and **Qty** values by selecting **OK**.</span></span>

    <span data-ttu-id="eaeb9-289">「作業が完了しました」というメッセージが表示されます。</span><span class="sxs-lookup"><span data-stu-id="eaeb9-289">You receive a "Work Completed" message.</span></span>

1. <span data-ttu-id="eaeb9-290">**キャンセル** を選択して終了します。</span><span class="sxs-lookup"><span data-stu-id="eaeb9-290">Select **Cancel** to exit.</span></span>

### <a name="put-away-to-cross-docking-and-bulk"></a><span data-ttu-id="eaeb9-291">クロスドッキングおよびバルクへのプットアウェイ</span><span class="sxs-lookup"><span data-stu-id="eaeb9-291">Put-away to cross-docking and bulk</span></span>

<span data-ttu-id="eaeb9-292">現在、両方の作業 ID のターゲット ライセンス プレートは同じです。</span><span class="sxs-lookup"><span data-stu-id="eaeb9-292">Currently, both work IDs have the same target license plate.</span></span> <span data-ttu-id="eaeb9-293">次の手順を完了するには、作業 ID とターゲット ライセンス プレート ID を取得する必要があります。</span><span class="sxs-lookup"><span data-stu-id="eaeb9-293">To complete the next steps, you must get the work ID and the target license plate ID.</span></span> <span data-ttu-id="eaeb9-294">この情報は、注文書明細行および販売注文明細行の作業の詳細から取得できます。</span><span class="sxs-lookup"><span data-stu-id="eaeb9-294">You can get this information from the work details for the purchase order line and the sales order line.</span></span> <span data-ttu-id="eaeb9-295">または、**倉庫管理 \> 作業 \> 作業の詳細** に移動して、**倉庫** の値が *51* の作業をフィルター処理します。</span><span class="sxs-lookup"><span data-stu-id="eaeb9-295">Alternately, you can go to **Warehouse management \> Work \> Work details** and filter for work where the **Warehouse** value is *51*.</span></span>

1. <span data-ttu-id="eaeb9-296">モバイル デバイスでは、**入庫 \> 購入品のプットアウェイ** に移動して、作業からターゲット ライセンス プレートを入力します。</span><span class="sxs-lookup"><span data-stu-id="eaeb9-296">On the mobile device, go to **Inbound \> Purchase put-away**, and enter the target license plate from the work.</span></span>
1. <span data-ttu-id="eaeb9-297">**ID** フィールドに、作業の詳細からターゲット ライセンス プレート ID を入力します。</span><span class="sxs-lookup"><span data-stu-id="eaeb9-297">In the **ID** field, enter the target license plate ID from the work details.</span></span>

    <span data-ttu-id="eaeb9-298">クロスドッキングのピッキング ページには、ピッキング場所 (*RECV*)、ターゲット ライセンス プレート (*ライセンス プレート*)、品目 (*A0001*)、および数量 (*3*) が表示されます。</span><span class="sxs-lookup"><span data-stu-id="eaeb9-298">The cross-docking pick page shows the picking location (*RECV*), target license plate (*license plate*), item (*A0001*), and quantity (*3*).</span></span>

1. <span data-ttu-id="eaeb9-299">**OK** を選択します。</span><span class="sxs-lookup"><span data-stu-id="eaeb9-299">Select **OK**.</span></span>
1. <span data-ttu-id="eaeb9-300">**ターゲット LP** フィールドに、出荷場所にプット (クロスドッキング) するライセンス プレート ID のターゲット ライセンス プレートを入力します。</span><span class="sxs-lookup"><span data-stu-id="eaeb9-300">In the **Target LP** field, enter a target license plate for the license plate ID that should be put (cross-docked) to the shipping location.</span></span> <span data-ttu-id="eaeb9-301">選択した任意のライセンス プレート ID を選択できます。</span><span class="sxs-lookup"><span data-stu-id="eaeb9-301">You can select any license plate ID of your choice.</span></span>
1. <span data-ttu-id="eaeb9-302">**OK** を選択します。</span><span class="sxs-lookup"><span data-stu-id="eaeb9-302">Select **OK**.</span></span>
1. <span data-ttu-id="eaeb9-303">次のページの **ID** フィールドに、ターゲット ライセンス プレート ID を入力します。</span><span class="sxs-lookup"><span data-stu-id="eaeb9-303">On the next page, in the **ID** field, enter the target license plate ID.</span></span>
1. <span data-ttu-id="eaeb9-304">**OK** を選択します。</span><span class="sxs-lookup"><span data-stu-id="eaeb9-304">Select **OK**.</span></span>
1. <span data-ttu-id="eaeb9-305">残りの数量 2 をピッキングするための作業を確認し、**OK** を選択します。</span><span class="sxs-lookup"><span data-stu-id="eaeb9-305">Confirm the work for picking the remaining quantity of 2, and then select **OK**.</span></span>
1. <span data-ttu-id="eaeb9-306">次のページで、**完了** を選択してピッキング プロセスを終了し、プットアウェイ プロセスを開始します。</span><span class="sxs-lookup"><span data-stu-id="eaeb9-306">On the next page, select **Done** to end the picking process and begin the put-away process.</span></span>

    <span data-ttu-id="eaeb9-307">モバイル アプリでは、品目をプットする場所とライセンス プレートを提供します。</span><span class="sxs-lookup"><span data-stu-id="eaeb9-307">The mobile app presents you with the location and license plate to put the item to.</span></span>

1. <span data-ttu-id="eaeb9-308">**OK** を選択して、バルク ストレージの **プット** を確認します。</span><span class="sxs-lookup"><span data-stu-id="eaeb9-308">Confirm the bulk storage **Put** by selecting **OK**.</span></span>
1. <span data-ttu-id="eaeb9-309">次のページで、**OK** を選択して、クロスドッキングの **プット** を確認します。</span><span class="sxs-lookup"><span data-stu-id="eaeb9-309">On the next page, confirm the cross-docking **Put** by selecting **OK**.</span></span>

    <span data-ttu-id="eaeb9-310">「作業が完了しました」というメッセージが表示されます。</span><span class="sxs-lookup"><span data-stu-id="eaeb9-310">You receive a "Work Completed" message.</span></span>

1. <span data-ttu-id="eaeb9-311">**キャンセル** を選択して終了します。</span><span class="sxs-lookup"><span data-stu-id="eaeb9-311">Select **Cancel** to exit.</span></span>

<span data-ttu-id="eaeb9-312">次の図は、完了したクロスドッキング作業が Microsoft Dynamics 365 Supply Chain Management でどのように表示されるかを示しています。</span><span class="sxs-lookup"><span data-stu-id="eaeb9-312">The following illustration shows how the completed cross-docking work might appear in Microsoft Dynamics 365 Supply Chain Management.</span></span>

<span data-ttu-id="eaeb9-313">![クロスドッキング作業が完了しました](media/PlannedCrossDockingWork.png "クロスドッキング作業が完了しました")</span><span class="sxs-lookup"><span data-stu-id="eaeb9-313">![Cross-docking work completed](media/PlannedCrossDockingWork.png "Cross-docking work completed")</span></span>


[!INCLUDE[footer-include](../../includes/footer-banner.md)]