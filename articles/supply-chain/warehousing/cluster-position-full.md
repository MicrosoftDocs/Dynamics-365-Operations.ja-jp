---
title: クラスター位置フル
description: このトピックでは、クラスター位置フル機能について説明します。 この機能により、クラスター ピッキングが使用されているときに、コンテナやトートの容量制限においてより大きな誤差を許容できるため、作業の中断に関するルールをより厳格に適用することができます。
author: Mirzaab
manager: tfehr
ms.date: 08/25/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: mirzaab
ms.search.validFrom: 2020-07-08
ms.dyn365.ops.version: Release 10.0.8
ms.openlocfilehash: 8d030afb568b158e6caf48b0044d595d6ec024f6
ms.sourcegitcommit: 06f64550b2043582de4018bdd3924fcc1fd5d310
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 09/14/2020
ms.locfileid: "3802217"
---
# <a name="cluster-position-full"></a><span data-ttu-id="a05db-104">クラスター位置フル</span><span class="sxs-lookup"><span data-stu-id="a05db-104">Cluster position full</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="a05db-105">*クラスター位置フル* 機能を使用することで、クラスター ピッキングが使用されているときに、コンテナやトートの容量制限において、より大きな誤差を許容できるため、作業の中断に関するルールをより厳格に適用することができます。</span><span class="sxs-lookup"><span data-stu-id="a05db-105">The *Cluster position full* feature offers an alternative to more rigid enforcement of work break rules when cluster picking is used, because it enables a larger margin of error in the volumetric constraints of containers or totes.</span></span> <span data-ttu-id="a05db-106">一般的なシナリオでは、選択されたコンテナーには作業指示書のすべての品目が適合するわけではありません。</span><span class="sxs-lookup"><span data-stu-id="a05db-106">In a common scenario, not all items on a work order fit into a selected container.</span></span> <span data-ttu-id="a05db-107">クラスター ピッキングの対象となる倉庫の作業者は、このシナリオに対するオプションがほとんどないため、より大きなコンテナサイズに変更するか、上司と協力して別の解決策を考えなければなりません。</span><span class="sxs-lookup"><span data-stu-id="a05db-107">Warehouse workers who are cluster picking have few options in this scenario: they must either change to a larger container size or work with their supervisor to come up with a different solution.</span></span>

<span data-ttu-id="a05db-108">この機能により、クラスター内の作業単位のいずれかで **フル** ボタンを実行する機能が導入されます。</span><span class="sxs-lookup"><span data-stu-id="a05db-108">This feature introduces the ability to run the **Full** button on one of the work units in a cluster.</span></span> <span data-ttu-id="a05db-109">以前のバージョンでは、このオプションは、通常の注文のピッキングに対してのみ使用でき、クラスター ピッキングには使用できませんでした。</span><span class="sxs-lookup"><span data-stu-id="a05db-109">In older versions, this option was available only for regular order picking, not for cluster picking.</span></span> <span data-ttu-id="a05db-110">ただし、この機能は、残りの作業をキャンセルするという点で、標準の **フル** ボタンとは異なります。</span><span class="sxs-lookup"><span data-stu-id="a05db-110">However, this feature differs from the standard **Full** button in that it cancels the remaining work.</span></span> <span data-ttu-id="a05db-111">ユーザーが同じクラスタに別の在庫置場を追加することを推奨するものでも、自動的に新しい作業を作成するものでもありません。</span><span class="sxs-lookup"><span data-stu-id="a05db-111">It doesn't suggest that the user add another bin to the same cluster, and it doesn't automatically create new work.</span></span>

## <a name="turn-on-the-cluster-position-full-feature"></a><span data-ttu-id="a05db-112">クラスター位置フルの機能をオンにする</span><span class="sxs-lookup"><span data-stu-id="a05db-112">Turn on the Cluster position full feature</span></span>

<span data-ttu-id="a05db-113">この機能を使用するには、システム上で有効にする必要があります。</span><span class="sxs-lookup"><span data-stu-id="a05db-113">Before you can use this feature, it must be turned on in your system.</span></span> <span data-ttu-id="a05db-114">管理者は、[機能管理](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) 設定を使用して、機能の状態を確認し、有効にすることができます。</span><span class="sxs-lookup"><span data-stu-id="a05db-114">Admins can use the [feature management](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) settings to check the status of the feature and turn it on.</span></span> <span data-ttu-id="a05db-115">**機能管理** ワークスペースで、この機能は次のようにリストされています。</span><span class="sxs-lookup"><span data-stu-id="a05db-115">In the **Feature management** workspace, the feature is listed in the following way:</span></span>

- <span data-ttu-id="a05db-116">**モジュール:** *倉庫管理*</span><span class="sxs-lookup"><span data-stu-id="a05db-116">**Module:** *Warehouse management*</span></span>
- <span data-ttu-id="a05db-117">**クラスター名称 :** *クラスター位置フル*</span><span class="sxs-lookup"><span data-stu-id="a05db-117">**Feature name:** *Cluster position full*</span></span>

## <a name="setup"></a><span data-ttu-id="a05db-118">段取り</span><span class="sxs-lookup"><span data-stu-id="a05db-118">Setup</span></span>

<span data-ttu-id="a05db-119">このセクションでは、*クラスター位置フル*の機能を設定および使用する際のガイドラインと例を示します。</span><span class="sxs-lookup"><span data-stu-id="a05db-119">This section provides guidelines, and an example that shows how to set up and use the *Cluster position full* feature.</span></span>

### <a name="make-sample-data-available"></a><span data-ttu-id="a05db-120">サンプル データを有効化する</span><span class="sxs-lookup"><span data-stu-id="a05db-120">Make sample data available</span></span>

<span data-ttu-id="a05db-121">ここで指定されたサンプル レコードと値を使用して [シナリオ例](#example-scenario) を実行するには、標準の [デモ データ](../../fin-ops-core/dev-itpro/deployment/deploy-demo-environment.md) がインストールされているシステムを使用する必要があります。</span><span class="sxs-lookup"><span data-stu-id="a05db-121">To work through the [example scenario](#example-scenario) by using the sample records and values that are specified here, you must be on a system where the standard [demo data](../../fin-ops-core/dev-itpro/deployment/deploy-demo-environment.md) is installed.</span></span> <span data-ttu-id="a05db-122">また、開始する前に **USMF** 法人を選択する必要があります。</span><span class="sxs-lookup"><span data-stu-id="a05db-122">Additionally, you must select the **USMF** legal entity before you begin.</span></span>

<span data-ttu-id="a05db-123">このシナリオは、実稼働システムで作業する際の機能ガイダンスとして使用することもできます。</span><span class="sxs-lookup"><span data-stu-id="a05db-123">You can also use the example scenario as guidance for working with this feature on a production system.</span></span> <span data-ttu-id="a05db-124">ただし、その場合はここで説明した設定を独自の値に置き換える必要があります。</span><span class="sxs-lookup"><span data-stu-id="a05db-124">However, in that case, you must substitute your own values for the settings that are described here.</span></span>

### <a name="cluster-profiles"></a><span data-ttu-id="a05db-125">クラスター プロファイル</span><span class="sxs-lookup"><span data-stu-id="a05db-125">Cluster profiles</span></span>

<span data-ttu-id="a05db-126">クラスター ID を自動的に生成するかどうか、使用するポジション数、クラスターを分割する場合、ピッキング作業の順序付けと検証方法を指定する必要があります。</span><span class="sxs-lookup"><span data-stu-id="a05db-126">You must specify whether cluster IDs are automatically generated, how many positions are used, when clusters are broken, and how the picking work is sequenced and verified.</span></span>

1. <span data-ttu-id="a05db-127">**倉庫管理 \> 設定 \> モバイル デバイス \> クラスター プロファイル**の順に移動します。</span><span class="sxs-lookup"><span data-stu-id="a05db-127">Go to **Warehouse management \> Setup \> Mobile device \> Cluster profiles**.</span></span>
1. <span data-ttu-id="a05db-128">リスト ペインで、クラスター**レコードの作成**を選択します。</span><span class="sxs-lookup"><span data-stu-id="a05db-128">In the list pane, select the **Create Cluster** record.</span></span>
1. <span data-ttu-id="a05db-129">**一般** クイック タブで、次の値を検証します :</span><span class="sxs-lookup"><span data-stu-id="a05db-129">On the **General** FastTab, verify the following values:</span></span>

    - <span data-ttu-id="a05db-130">**クラスターID の生成 :** *はい*</span><span class="sxs-lookup"><span data-stu-id="a05db-130">**Generate cluster ID:** *Yes*</span></span>
    - <span data-ttu-id="a05db-131">**位置をアクティブ化する :** *はい*</span><span class="sxs-lookup"><span data-stu-id="a05db-131">**Activate positions:** *Yes*</span></span>
    - <span data-ttu-id="a05db-132">**位置の数 :** *2*</span><span class="sxs-lookup"><span data-stu-id="a05db-132">**Number of positions:** *2*</span></span>
    - <span data-ttu-id="a05db-133">**位置の名前 :** *数値*</span><span class="sxs-lookup"><span data-stu-id="a05db-133">**Position name:** *Numeric*</span></span>
    - <span data-ttu-id="a05db-134">**クラスターの分割位置 :**  *プット*</span><span class="sxs-lookup"><span data-stu-id="a05db-134">**Break cluster at:** *Put*</span></span>
    - <span data-ttu-id="a05db-135">**検証タイプのソート :** *位置スキャン*</span><span class="sxs-lookup"><span data-stu-id="a05db-135">**Sort verification type:** *Position scan*</span></span>

1. <span data-ttu-id="a05db-136">**クラスターの並べ替え** クイックタブを選択します。</span><span class="sxs-lookup"><span data-stu-id="a05db-136">In the **Cluster sorting** FastTab.</span></span> <span data-ttu-id="a05db-137">グリッドは空白にする必要があります (ここには行が含まれていない必要があります)。</span><span class="sxs-lookup"><span data-stu-id="a05db-137">The grid should be blank (that is, it should contain no lines).</span></span>

### <a name="work-templates"></a><span data-ttu-id="a05db-138">作業テンプレート</span><span class="sxs-lookup"><span data-stu-id="a05db-138">Work templates</span></span>

<span data-ttu-id="a05db-139">クラスター ピッキングに使用するピッキング作業がどのように作成されるかを定義する必要があります。</span><span class="sxs-lookup"><span data-stu-id="a05db-139">You must define how the picking work for cluster picking is created.</span></span>

1. <span data-ttu-id="a05db-140">**倉庫管理 \> 設定 \> 作業 \> 作業テンプレート**の順に移動します。</span><span class="sxs-lookup"><span data-stu-id="a05db-140">Go to **Warehouse management \> Setup \> Work \> Work templates**.</span></span>
1. <span data-ttu-id="a05db-141">ページ上部で、**作業指示書の種類** フィールドを *販売注文* に設定します。</span><span class="sxs-lookup"><span data-stu-id="a05db-141">At the top of the page, set the **Work order type** field to *Sales orders*.</span></span>
1. <span data-ttu-id="a05db-142">デモデータの中で、以下の作業テンプレートがリストされていることを確認してください。</span><span class="sxs-lookup"><span data-stu-id="a05db-142">Make sure that the following work templates from the demo data are listed.</span></span> <span data-ttu-id="a05db-143">これらが使用できない場合は、このシナリオを完了できません。</span><span class="sxs-lookup"><span data-stu-id="a05db-143">If they aren't available, you won't be able to complete the scenario.</span></span>

    - <span data-ttu-id="a05db-144">61 SO ステージ</span><span class="sxs-lookup"><span data-stu-id="a05db-144">61 SO Stage</span></span>
    - <span data-ttu-id="a05db-145">61 SO クラスター ピッキング</span><span class="sxs-lookup"><span data-stu-id="a05db-145">61 SO Cluster pick</span></span>

### <a name="location-directives"></a><span data-ttu-id="a05db-146">場所のディレクティブ</span><span class="sxs-lookup"><span data-stu-id="a05db-146">Location directives</span></span>

<span data-ttu-id="a05db-147">品目をピッキングする場所とプットする場所を指定する必要があります。</span><span class="sxs-lookup"><span data-stu-id="a05db-147">You must specify where items are picked from and where they are put.</span></span>

1. <span data-ttu-id="a05db-148">**倉庫管理 \> 設定 \> 場所のディレクティブ** に移動します。</span><span class="sxs-lookup"><span data-stu-id="a05db-148">Go to **Warehouse management \> Setup \> Location directives**.</span></span>
1. <span data-ttu-id="a05db-149">リスト ヘッダーでは、**作業指示書のタイプ** フィールドを *販売注文* に設定します。</span><span class="sxs-lookup"><span data-stu-id="a05db-149">In the list header, set the **Work order type** field to *Sales orders*.</span></span>
1. <span data-ttu-id="a05db-150">デモ データの中で、以下の販売注文ディレクティブがリストされていることを確認してください。</span><span class="sxs-lookup"><span data-stu-id="a05db-150">Make sure that the following sales order directives from the demo data are listed.</span></span> <span data-ttu-id="a05db-151">これらが使用できない場合は、このシナリオを完了できません。</span><span class="sxs-lookup"><span data-stu-id="a05db-151">If they aren't available, you won't be able to complete the scenario.</span></span>

    - <span data-ttu-id="a05db-152">61 クラスター ピッキング</span><span class="sxs-lookup"><span data-stu-id="a05db-152">61 Cluster pick</span></span>
    - <span data-ttu-id="a05db-153">61 SO 注文のピッキング</span><span class="sxs-lookup"><span data-stu-id="a05db-153">61 SO Pick order</span></span>

### <a name="mobile-device-menu-items"></a><span data-ttu-id="a05db-154">モバイル デバイスのメニュー品目</span><span class="sxs-lookup"><span data-stu-id="a05db-154">Mobile device menu items</span></span>

<span data-ttu-id="a05db-155">クラスター ピッキングで指示された既存の作業を利用するには、モバイルデバイスのメニュー項目を構成する必要があります。</span><span class="sxs-lookup"><span data-stu-id="a05db-155">You must configure a mobile device menu item to use existing work that is directed by cluster picking.</span></span> <span data-ttu-id="a05db-156">クラスターピッキングのモバイル デバイス メニュー項目で、 **作業の分割を許可** のパラメータをオンにして、*SO ピッキング*の作業クラスを追加する必要があります。</span><span class="sxs-lookup"><span data-stu-id="a05db-156">In the mobile device menu item for cluster picking, the **Allow splitting of work** parameter must be turned on, and the *SO Pick* work class must be added.</span></span>

1. <span data-ttu-id="a05db-157">**倉庫管理 \> 設定 \> モバイル デバイス \> モバイル デバイスのメニュー品目**の順に移動します。</span><span class="sxs-lookup"><span data-stu-id="a05db-157">Go to **Warehouse management \> Setup \> Mobile device \> Mobile device menu items**.</span></span>
1. <span data-ttu-id="a05db-158">リスト ペインで、**クラスター ピッキングの作成** レコードを選択します。</span><span class="sxs-lookup"><span data-stu-id="a05db-158">In the list pane, select the **Cluster Pick Create** record.</span></span>
1. <span data-ttu-id="a05db-159">アクション ペインで、**編集**を選択します。</span><span class="sxs-lookup"><span data-stu-id="a05db-159">Select **Edit** in the Action pane.</span></span>
1. <span data-ttu-id="a05db-160">**一般**クイック タブで、次の値を設定します。</span><span class="sxs-lookup"><span data-stu-id="a05db-160">On the **General** FastTab, set the following values:</span></span>

    - <span data-ttu-id="a05db-161">**作業指示 :** *クラスター ピッキング*</span><span class="sxs-lookup"><span data-stu-id="a05db-161">**Directed by:** *Cluster picking*</span></span>
    - <span data-ttu-id="a05db-162">**ライセンスプレートの生成:** *はい*</span><span class="sxs-lookup"><span data-stu-id="a05db-162">**Generate license plate:** *Yes*</span></span>
    - <span data-ttu-id="a05db-163">**作業の分割を許可する :** *はい*</span><span class="sxs-lookup"><span data-stu-id="a05db-163">**Allow splitting of work:** *Yes*</span></span>
    - <span data-ttu-id="a05db-164">**クラスタープロファイル ID :** *クラスターの作成*</span><span class="sxs-lookup"><span data-stu-id="a05db-164">**Cluster profile ID:** *Create Cluster*</span></span>

    <span data-ttu-id="a05db-165">他のすべてのフィールドの既定値を受け入れます。</span><span class="sxs-lookup"><span data-stu-id="a05db-165">Accept the default values for all other fields.</span></span>

1. <span data-ttu-id="a05db-166">**作業クラス** クイックタブで、必要に応じて次の2行を追加します :</span><span class="sxs-lookup"><span data-stu-id="a05db-166">On the **Work classes** FastTab, add the following two lines, as required:</span></span>

    - <span data-ttu-id="a05db-167">1行目 (通常はデモデータに含まれています) :</span><span class="sxs-lookup"><span data-stu-id="a05db-167">Line 1 (usually present in demo data):</span></span>

        - <span data-ttu-id="a05db-168">**作業クラス ID :** *営業*</span><span class="sxs-lookup"><span data-stu-id="a05db-168">**Work class ID:** *Sales*</span></span> 
        - <span data-ttu-id="a05db-169">**作業指示のタイプ :** *販売注文*</span><span class="sxs-lookup"><span data-stu-id="a05db-169">**Work order type:** *Sales orders*</span></span>

    - <span data-ttu-id="a05db-170">2行目 (通常はデモデータに含まれません) :</span><span class="sxs-lookup"><span data-stu-id="a05db-170">Line 2 (probably not present in demo data):</span></span>

        - <span data-ttu-id="a05db-171">**作業クラス ID:** *SO ピック*</span><span class="sxs-lookup"><span data-stu-id="a05db-171">**Work class ID:** *SO Pick*</span></span>
        - <span data-ttu-id="a05db-172">**作業指示のタイプ :** *販売注文*</span><span class="sxs-lookup"><span data-stu-id="a05db-172">**Work order type:** *Sales orders*</span></span>

1. <span data-ttu-id="a05db-173">アクション ペインの **作業確認の設定** の設定に移動します。</span><span class="sxs-lookup"><span data-stu-id="a05db-173">Go to **Work confirmation setup** in the Action pane.</span></span>
1. <span data-ttu-id="a05db-174">**編集**を選択します。</span><span class="sxs-lookup"><span data-stu-id="a05db-174">Select **Edit**.</span></span>
1. <span data-ttu-id="a05db-175">グリッド内の行に以下の値を入力します。</span><span class="sxs-lookup"><span data-stu-id="a05db-175">Enter the following values on the line in grid.</span></span>
    - <span data-ttu-id="a05db-176">**作業タイプ** - *ピック*</span><span class="sxs-lookup"><span data-stu-id="a05db-176">**Work type** - *Pick*</span></span>
    - <span data-ttu-id="a05db-177">**製品確認** - *チェックボックスを確認する*</span><span class="sxs-lookup"><span data-stu-id="a05db-177">**Product confirmation** - *Select the check box*</span></span>

1. <span data-ttu-id="a05db-178">アクション ペインで**保存**を選択し、ページを閉じます。</span><span class="sxs-lookup"><span data-stu-id="a05db-178">Select **Save** in the Action pane and close the page.</span></span>

## <a name="create-picking-work"></a><span data-ttu-id="a05db-179">ピッキング作業の作成</span><span class="sxs-lookup"><span data-stu-id="a05db-179">Create picking work</span></span>

<span data-ttu-id="a05db-180">クラスター ピッキングを開始する前に、いくつかの出荷作業を作成する必要があります。</span><span class="sxs-lookup"><span data-stu-id="a05db-180">Before you can start cluster picking, you must create some outbound work.</span></span> <span data-ttu-id="a05db-181">前に作成したクラスター プロファイルは、2 つのクラスターのポジションを指定します。</span><span class="sxs-lookup"><span data-stu-id="a05db-181">The cluster profile that you created earlier specifies two cluster positions.</span></span> <span data-ttu-id="a05db-182">したがって、販売注文ピッキングは少なくとも 2 つの作業 ID を作成する必要があります。</span><span class="sxs-lookup"><span data-stu-id="a05db-182">Therefore, at least two work IDs must be created for sales order picking.</span></span> <span data-ttu-id="a05db-183">このシナリオでは、トランザクションが倉庫 *61* で発生し、品目 *L0101* と *T0100* が使用されます。</span><span class="sxs-lookup"><span data-stu-id="a05db-183">For this scenario, transactions will occur in warehouse *61*, and they will use items *L0101* and *T0100*.</span></span> <span data-ttu-id="a05db-184">デモデータには、これら品目の手持在庫が十分にある必要があります。</span><span class="sxs-lookup"><span data-stu-id="a05db-184">The demo data should have enough on-hand inventory of these items.</span></span> <span data-ttu-id="a05db-185">トランザクションを完了するために十分な在庫があることを確認してください。</span><span class="sxs-lookup"><span data-stu-id="a05db-185">Make sure that you have enough inventory to complete the transactions.</span></span>

### <a name="create-sales-order-1"></a><span data-ttu-id="a05db-186">販売注文の作成 1</span><span class="sxs-lookup"><span data-stu-id="a05db-186">Create sales order 1</span></span>

1. <span data-ttu-id="a05db-187">**販売とマーケティング \> 販売注文 \> すべての販売注文**の順に移動します。</span><span class="sxs-lookup"><span data-stu-id="a05db-187">Go to **Sales and Marketing \> Sales orders \> All sales orders**.</span></span>
1. <span data-ttu-id="a05db-188">**新規**を選択して新たに販売注文 1 を作成します。</span><span class="sxs-lookup"><span data-stu-id="a05db-188">Select **New** to create sales order 1.</span></span>
1. <span data-ttu-id="a05db-189">**販売注文の作成**ダイアログ ボックスでは、次の値を設定します。</span><span class="sxs-lookup"><span data-stu-id="a05db-189">In the **Create sales order** dialog box, set the following values:</span></span>

    - <span data-ttu-id="a05db-190">**顧客アカウント:** *US-010*</span><span class="sxs-lookup"><span data-stu-id="a05db-190">**Customer account:** *US-010*</span></span>
    - <span data-ttu-id="a05db-191">**倉庫:** *61*</span><span class="sxs-lookup"><span data-stu-id="a05db-191">**Warehouse:** *61*</span></span>

1. <span data-ttu-id="a05db-192">**OK** を選択します。</span><span class="sxs-lookup"><span data-stu-id="a05db-192">Select **OK**.</span></span>
1. <span data-ttu-id="a05db-193">新しい販売注文が開かれます。</span><span class="sxs-lookup"><span data-stu-id="a05db-193">The new sales order is opened.</span></span> <span data-ttu-id="a05db-194">**販売注文明細行**クイックタブで、次の設定で明細行を追加します :</span><span class="sxs-lookup"><span data-stu-id="a05db-194">On the **Sales order lines** FastTab, add a line that has the following settings:</span></span>

    - <span data-ttu-id="a05db-195">**品目番号:** *T0100*</span><span class="sxs-lookup"><span data-stu-id="a05db-195">**Item number:** *T0100*</span></span>
    - <span data-ttu-id="a05db-196">**数量:** *5*</span><span class="sxs-lookup"><span data-stu-id="a05db-196">**Quantity:** *5*</span></span>

1. <span data-ttu-id="a05db-197">**明細行の詳細**クイックタブの**配送**タブで、**出荷日の確認**フィールドが今日の日付に設定されます。</span><span class="sxs-lookup"><span data-stu-id="a05db-197">On the **Line details** FastTab, on the **Delivery** tab, set the **Confirmed ship date** field to today's date.</span></span>
1. <span data-ttu-id="a05db-198">**販売注文明細行**クイックタブで、次の設定を持つ 2 つ目の明細行を追加します :</span><span class="sxs-lookup"><span data-stu-id="a05db-198">On the **Sales order lines** FastTab, add a second line that has the following settings:</span></span>

    - <span data-ttu-id="a05db-199">**品目番号:** *L0101*</span><span class="sxs-lookup"><span data-stu-id="a05db-199">**Item number:** *L0101*</span></span>
    - <span data-ttu-id="a05db-200">**数量:** *20*</span><span class="sxs-lookup"><span data-stu-id="a05db-200">**Quantity:** *20*</span></span>

1. <span data-ttu-id="a05db-201">**明細行の詳細**クイックタブの**配送**タブで、**出荷日の確認**フィールドが今日の日付に設定されます。</span><span class="sxs-lookup"><span data-stu-id="a05db-201">On the **Line details** FastTab, on the **Delivery** tab, set the **Confirmed ship date** field to today's date.</span></span>
1. <span data-ttu-id="a05db-202">追加した各行に対して、次の手順に従って在庫を引当します :</span><span class="sxs-lookup"><span data-stu-id="a05db-202">For each line that you just added, follow these steps to reserve inventory:</span></span>

    1. <span data-ttu-id="a05db-203">引当する行を選択します。</span><span class="sxs-lookup"><span data-stu-id="a05db-203">Select the line to reserve.</span></span>
    2. <span data-ttu-id="a05db-204">**販売注文行** クイック タブで、**在庫 \> 予約** を選択します。</span><span class="sxs-lookup"><span data-stu-id="a05db-204">On the **Sales order lines** FastTab, select **Inventory \> Reservation**.</span></span>
    3. <span data-ttu-id="a05db-205">**引当** ページの、アクション ウィンドウで**ロットの引当**を選択して、在庫を引当てします。</span><span class="sxs-lookup"><span data-stu-id="a05db-205">On the **Reservation** page, on the Action Pane, select **Reserve lot** to reserve the inventory.</span></span>
    4. <span data-ttu-id="a05db-206">**引当**ページを閉じます。</span><span class="sxs-lookup"><span data-stu-id="a05db-206">Close the **Reservation** page.</span></span>

1. <span data-ttu-id="a05db-207">アクション ウィンドウの**倉庫**タブで、**倉庫へのリリース**を選択します。</span><span class="sxs-lookup"><span data-stu-id="a05db-207">On the Action Pane, on the **Warehouse** tab, select **Release to warehouse**.</span></span>

    <span data-ttu-id="a05db-208">リリースが完了すると、作成されたウェーブ ID と出荷 ID を示す情報メッセージが表示されます。</span><span class="sxs-lookup"><span data-stu-id="a05db-208">When the release is completed, you receive informational messages that show the wave and load IDs that were created.</span></span>

### <a name="create-sales-order-2"></a><span data-ttu-id="a05db-209">販売注文の作成 2</span><span class="sxs-lookup"><span data-stu-id="a05db-209">Create sales order 2</span></span>

1. <span data-ttu-id="a05db-210">**販売とマーケティング \> 販売注文 \> すべての販売注文**の順に移動します。</span><span class="sxs-lookup"><span data-stu-id="a05db-210">Go to **Sales and Marketing \> Sales orders \> All sales orders**.</span></span>
1. <span data-ttu-id="a05db-211">**新規**を選択して新たに販売注文 2 を作成します。</span><span class="sxs-lookup"><span data-stu-id="a05db-211">Select **New** to create sales order 2.</span></span>
1. <span data-ttu-id="a05db-212">**販売注文の作成**ダイアログ ボックスでは、次の値を設定します。</span><span class="sxs-lookup"><span data-stu-id="a05db-212">In the **Create sales order** dialog box, set the following values:</span></span>

    - <span data-ttu-id="a05db-213">**顧客アカウント:** *US-011*</span><span class="sxs-lookup"><span data-stu-id="a05db-213">**Customer account:** *US-011*</span></span>
    - <span data-ttu-id="a05db-214">**倉庫:** *61*</span><span class="sxs-lookup"><span data-stu-id="a05db-214">**Warehouse:** *61*</span></span>

1. <span data-ttu-id="a05db-215">**OK** を選択します。</span><span class="sxs-lookup"><span data-stu-id="a05db-215">Select **OK**.</span></span>
1. <span data-ttu-id="a05db-216">新しい販売注文が開かれます。</span><span class="sxs-lookup"><span data-stu-id="a05db-216">The new sales order is opened.</span></span> <span data-ttu-id="a05db-217">**販売注文明細行**クイックタブで、次の設定で明細行を追加します :</span><span class="sxs-lookup"><span data-stu-id="a05db-217">On the **Sales order lines** FastTab, add a line that has the following settings:</span></span>

    - <span data-ttu-id="a05db-218">**品目番号:** *L0101*</span><span class="sxs-lookup"><span data-stu-id="a05db-218">**Item number:** *L0101*</span></span>
    - <span data-ttu-id="a05db-219">**数量:** *20*</span><span class="sxs-lookup"><span data-stu-id="a05db-219">**Quantity:** *20*</span></span>

1. <span data-ttu-id="a05db-220">**明細行の詳細**クイックタブの**配送**タブで、**出荷日の確認**フィールドが今日の日付に設定されます。</span><span class="sxs-lookup"><span data-stu-id="a05db-220">On the **Line details** FastTab, on the **Delivery** tab, set the **Confirmed ship date** field to today's date.</span></span>
1. <span data-ttu-id="a05db-221">**販売注文明細行**クイックタブで、次の設定を持つ 2 つ目の明細行を追加します :</span><span class="sxs-lookup"><span data-stu-id="a05db-221">On the **Sales order lines** FastTab, add a second line that has the following settings:</span></span>

    - <span data-ttu-id="a05db-222">**品目番号:** *T0100*</span><span class="sxs-lookup"><span data-stu-id="a05db-222">**Item number:** *T0100*</span></span>
    - <span data-ttu-id="a05db-223">**数量:** *2*</span><span class="sxs-lookup"><span data-stu-id="a05db-223">**Quantity:** *2*</span></span>

1. <span data-ttu-id="a05db-224">**明細行の詳細**クイックタブの**配送**タブで、**出荷日の確認**フィールドが今日の日付に設定されます。</span><span class="sxs-lookup"><span data-stu-id="a05db-224">On the **Line details** FastTab, on the **Delivery** tab, set the **Confirmed ship date** field to today's date.</span></span>
1. <span data-ttu-id="a05db-225">追加した各行に対して、次の手順に従って在庫を引当します :</span><span class="sxs-lookup"><span data-stu-id="a05db-225">For each line that you just added, follow these steps to reserve inventory:</span></span>

    1. <span data-ttu-id="a05db-226">引当する行を選択します。</span><span class="sxs-lookup"><span data-stu-id="a05db-226">Select the line to reserve.</span></span>
    2. <span data-ttu-id="a05db-227">**販売注文行** クイック タブで、**在庫 \> 予約** を選択します。</span><span class="sxs-lookup"><span data-stu-id="a05db-227">On the **Sales order lines** FastTab, select **Inventory \> Reservation**.</span></span>
    3. <span data-ttu-id="a05db-228">**引当** ページの、アクション ウィンドウで**ロットの引当**を選択して、在庫を引当てします。</span><span class="sxs-lookup"><span data-stu-id="a05db-228">On the **Reservation** page, on the Action Pane, select **Reserve lot** to reserve the inventory.</span></span>
    4. <span data-ttu-id="a05db-229">**引当**ページを閉じます。</span><span class="sxs-lookup"><span data-stu-id="a05db-229">Close the **Reservation** page.</span></span>

1. <span data-ttu-id="a05db-230">アクション ウィンドウの**倉庫**タブで、**倉庫へのリリース**を選択します。</span><span class="sxs-lookup"><span data-stu-id="a05db-230">On the Action Pane, on the **Warehouse** tab, select **Release to warehouse**.</span></span>

    <span data-ttu-id="a05db-231">リリースが完了すると、作成されたウェーブ ID と出荷 ID を示す情報メッセージが表示されます。</span><span class="sxs-lookup"><span data-stu-id="a05db-231">When the release is completed, you receive informational messages that show the wave and load IDs that were created.</span></span>

### <a name="get-work-ids-and-license-plate-numbers"></a><span data-ttu-id="a05db-232">作業 ID とライセンスプレート番号の取得</span><span class="sxs-lookup"><span data-stu-id="a05db-232">Get work IDs and license plate numbers</span></span>

<span data-ttu-id="a05db-233">2つのピッキングラインを持つ2つの作業 ID が作成されている必要があります。</span><span class="sxs-lookup"><span data-stu-id="a05db-233">Two work IDs should have been created, each of which has two pick lines.</span></span> <span data-ttu-id="a05db-234">次の手順に従って、作業 ID とライセンス プレート の割り当てを検索します。</span><span class="sxs-lookup"><span data-stu-id="a05db-234">Follow these steps to find the work IDs and license plate assignments.</span></span>

1. <span data-ttu-id="a05db-235">**倉庫管理 \> 作業 \> 作業の詳細**の順に移動します。</span><span class="sxs-lookup"><span data-stu-id="a05db-235">Go to **Warehouse management \> Work \> Work details**.</span></span>
1. <span data-ttu-id="a05db-236">**概要**グリッドで、今作成した 2つの販売注文の **注文番号** 列を検索します。</span><span class="sxs-lookup"><span data-stu-id="a05db-236">In the **Overview** grid, search the **Order number** column for the two sales orders that you just created.</span></span> <span data-ttu-id="a05db-237">各販売注文については、対応する作業 ID をメモしておいてください。</span><span class="sxs-lookup"><span data-stu-id="a05db-237">For each sales order, make a note of the corresponding work ID.</span></span>
1. <span data-ttu-id="a05db-238">販売注文ごとに行を選択して、**明細行**グリッドに関連情報を表示します。</span><span class="sxs-lookup"><span data-stu-id="a05db-238">Select the row for each sales order to show related information in the **Lines** grid.</span></span> <span data-ttu-id="a05db-239">各品目がピッキングされる場所をメモします。</span><span class="sxs-lookup"><span data-stu-id="a05db-239">Make a note of the location that each item will be picked from.</span></span>
1. <span data-ttu-id="a05db-240">**在庫管理 \> 照会およびレポート \> 手持在庫リスト** の順に移動します。</span><span class="sxs-lookup"><span data-stu-id="a05db-240">Go to **Inventory management \> Inquiries and reports \> On-hand list**.</span></span>
1. <span data-ttu-id="a05db-241">アクション ペインで**寸法**を選択して、**寸法の表示**ダイアログ ボックスを開きます。</span><span class="sxs-lookup"><span data-stu-id="a05db-241">On the Action Pane, select **Dimensions** to open the **Dimension display** dialog box.</span></span>
1. <span data-ttu-id="a05db-242">**ライセンス プレート**、**倉庫**、**品目番号** の各チェックボックスがオンになっていることを確認し、 **OK** を選択します。</span><span class="sxs-lookup"><span data-stu-id="a05db-242">Make sure that the **License plate**, **Warehouse**, and **Item number** check boxes are selected, and then select **OK**.</span></span>
1. <span data-ttu-id="a05db-243">**フィルター**ペインで、次のフィルタを設定します :</span><span class="sxs-lookup"><span data-stu-id="a05db-243">In the **Filter** pane, set the following filters:</span></span>

    - <span data-ttu-id="a05db-244">**品目番号** – *L0101*と *T100* の**いずれか**である</span><span class="sxs-lookup"><span data-stu-id="a05db-244">**Item number** – **is one of** – *L0101* and *T100*</span></span>
    - <span data-ttu-id="a05db-245">**倉庫** – **61** – *で始まる*</span><span class="sxs-lookup"><span data-stu-id="a05db-245">**Warehouse** – **begins with** – *61*</span></span>

1. <span data-ttu-id="a05db-246">表示された**ライセンス プレート** の値をメモします。</span><span class="sxs-lookup"><span data-stu-id="a05db-246">Make a note of the **License plate** values that are shown.</span></span>

## <a name="example-scenario"></a><a name="example-scenario"></a><span data-ttu-id="a05db-247">シナリオ例</span><span class="sxs-lookup"><span data-stu-id="a05db-247">Example scenario</span></span>

### <a name="mobile-device-flow-execution--work-confirmation-setup-for-the-product"></a><span data-ttu-id="a05db-248">モバイル デバイスフローの実行 – 製品に使用する作業確認の設定</span><span class="sxs-lookup"><span data-stu-id="a05db-248">Mobile device flow execution – Work confirmation setup for the product</span></span>

1. <span data-ttu-id="a05db-249">倉庫 *61* でユーザーとして倉庫アプリにサインインします。</span><span class="sxs-lookup"><span data-stu-id="a05db-249">Sign in to the warehouse app as a user in warehouse *61*.</span></span>
1. <span data-ttu-id="a05db-250">**アウトバウンド \> クラスター ピッキングの作成** に移動します。</span><span class="sxs-lookup"><span data-stu-id="a05db-250">Go to **Outbound \> Cluster pick create**.</span></span>

    <span data-ttu-id="a05db-251">**タスク : 作業をクラスターに割り当てる** ページが表示されます。</span><span class="sxs-lookup"><span data-stu-id="a05db-251">The **TASK: Assign work to Cluster** page appears.</span></span>

1. <span data-ttu-id="a05db-252">販売注文 1 に作業 ID を入力し、クラスター位置 1 に割り当てます。</span><span class="sxs-lookup"><span data-stu-id="a05db-252">Enter the work ID for sales order 1 to assign it to cluster position 1.</span></span>
1. <span data-ttu-id="a05db-253">**OK** (チェックマーク記号) を選択します。</span><span class="sxs-lookup"><span data-stu-id="a05db-253">Select **OK** (check mark symbol).</span></span>
1. <span data-ttu-id="a05db-254">販売注文 2 に作業 ID を入力し、クラスター位置 2 に割り当てます。</span><span class="sxs-lookup"><span data-stu-id="a05db-254">Enter the work ID for sales order 2 to assign it to cluster position 2.</span></span>
1. <span data-ttu-id="a05db-255">**OK** (チェックマーク記号) を選択します。</span><span class="sxs-lookup"><span data-stu-id="a05db-255">Select **OK** (check mark symbol).</span></span>

    <span data-ttu-id="a05db-256">**タスク : クラスター ピッキングの作成 : ピック** ページが表示され、*品目 L0101 2 PL*が表示されます。</span><span class="sxs-lookup"><span data-stu-id="a05db-256">The **TASK: Cluster Pick Create: Pick** page appears and shows *Item L0101 2 PL*.</span></span>

<span data-ttu-id="a05db-257">クラスター プロファイルでは、[ポジションの数] が 2 に設定されているため、最初の [統合ピッキング] に自動的に次の指示が表示されます : 品目*L0101* を含む 2 つのパレット</span><span class="sxs-lookup"><span data-stu-id="a05db-257">Because the cluster profile set the number of positions to 2, the system automatically directs you to the first consolidate pick: two pallets (PL) of item *L0101*.</span></span>

<span data-ttu-id="a05db-258">次のステップの過程においてはいつでも、**詳細** タブを選択して、ピッキング場所などのタスクに関する追加情報を表示することができます。</span><span class="sxs-lookup"><span data-stu-id="a05db-258">At any time during the following steps, you can select the **Details** tab to view additional information about the task, such as the picking location.</span></span>

1. <span data-ttu-id="a05db-259">**品目**フィールドを *L0101* に設定します。</span><span class="sxs-lookup"><span data-stu-id="a05db-259">Set the **ITEM** field to *L0101*.</span></span> <span data-ttu-id="a05db-260">これにより、このメニュー項目に必要な品目番号が確認されます (このメニュー項目を作成した際に **モバイル デバイス メニュー品目**  ページの **作業確認の設定** を選択して設定したものです)。</span><span class="sxs-lookup"><span data-stu-id="a05db-260">This confirms the item number, which is required for this menu item (you configured this earlier by selecting **Work confirmation setup**  from the **Mobile device menu item** page when you created this menu item).</span></span>
1. <span data-ttu-id="a05db-261">ピッキングされる場所の品目に関連付けられているライセンス プレート番号を入力します。</span><span class="sxs-lookup"><span data-stu-id="a05db-261">Enter the license plate number that is associated with the item in the location that is being picked.</span></span> <span data-ttu-id="a05db-262">2 つのパレットを選択します。</span><span class="sxs-lookup"><span data-stu-id="a05db-262">You will pick two pallets.</span></span>
1. <span data-ttu-id="a05db-263">**LP** フィールドを *LP\_PICK\_01* に設定します。</span><span class="sxs-lookup"><span data-stu-id="a05db-263">Set the **LP** field to *LP\_PICK\_01*.</span></span>
1. <span data-ttu-id="a05db-264">**OK** (チェックマーク記号) を選択します。</span><span class="sxs-lookup"><span data-stu-id="a05db-264">Select **OK** (check mark symbol).</span></span>

    <span data-ttu-id="a05db-265">**タスク : 並べ替え : クラスター ピッキングの作成** ページが表示されます。</span><span class="sxs-lookup"><span data-stu-id="a05db-265">The **TASK: Sort: Cluster Pick Create** page appears.</span></span> <span data-ttu-id="a05db-266">ここでは、2つのピッキング済パレットをピックのポジションに並べ替えます。</span><span class="sxs-lookup"><span data-stu-id="a05db-266">Here, you will sort the two picked pallets into a pick position.</span></span> <span data-ttu-id="a05db-267">このポジションは、ピッキングされた在庫を販売注文と区別するトートやコンテナになる可能性があります。</span><span class="sxs-lookup"><span data-stu-id="a05db-267">This position might be a tote or container that is used to separate the picked inventory by sales order.</span></span>

1. <span data-ttu-id="a05db-268">ポシション 1 (販売注文 1 に使用する) の位置にソートされる品目 (*L0101*) と数量 (*20*ea) の詳細を表示します。</span><span class="sxs-lookup"><span data-stu-id="a05db-268">View the details that are shown for the item (*L0101*) and quantity (*20* ea) that will be sorted into position 1 (for sales order 1).</span></span>
1. <span data-ttu-id="a05db-269">**POSITION NA** フィールドを *1* に設定します。</span><span class="sxs-lookup"><span data-stu-id="a05db-269">Set the **POSITION NA** field to *1*.</span></span>
1. <span data-ttu-id="a05db-270">**OK** (チェックマーク記号) を選択します。</span><span class="sxs-lookup"><span data-stu-id="a05db-270">Select **OK** (check mark symbol).</span></span>
1. <span data-ttu-id="a05db-271">ポシション 2 (販売注文 2 に使用する) の位置にソートされる品目 (*L0101*) と数量 (*20*ea) の詳細を表示します。</span><span class="sxs-lookup"><span data-stu-id="a05db-271">View the details that are shown for the item (*L0101*) and quantity (*20* ea) that will be sorted into position 2 (for sales order 2).</span></span>
1. <span data-ttu-id="a05db-272">**POSITION NA** フィールドを *2* に設定します。</span><span class="sxs-lookup"><span data-stu-id="a05db-272">Set the **POSITION NA** field to *2*.</span></span>
1. <span data-ttu-id="a05db-273">**OK** (チェックマーク記号) を選択します。</span><span class="sxs-lookup"><span data-stu-id="a05db-273">Select **OK** (check mark symbol).</span></span>

    <span data-ttu-id="a05db-274">**タスク : クラスター ピッキングの作成 : ピック** ページが表示され、*品目 T0100 7 ea* が表示されます。</span><span class="sxs-lookup"><span data-stu-id="a05db-274">The **TASK: Cluster Pick Create: Pick** page appears and shows *Item T0100 7 ea*.</span></span>

<span data-ttu-id="a05db-275">このシナリオでは、ポシション 1 は、販売注文 1 を処理するにあたってピッキングする必要がある品目の数量全体を受け入れることができません。</span><span class="sxs-lookup"><span data-stu-id="a05db-275">In this scenario, position 1 can't accept the full quantity of items that must be picked to fulfill sales order 1.</span></span> <span data-ttu-id="a05db-276">ポシションは、"満杯" とマークする必要があります。</span><span class="sxs-lookup"><span data-stu-id="a05db-276">A position must be marked as full.</span></span> <span data-ttu-id="a05db-277">このシナリオでは、2つ目の品目の部分的なピッキングを行います。</span><span class="sxs-lookup"><span data-stu-id="a05db-277">In this scenario, you will do a partial pick of the second item.</span></span> <span data-ttu-id="a05db-278">2つ目の品目はポシション 1 のために部分的にピッキングし、注文を処理するにあたって残数量をピッキングするために新規作業を作成します。</span><span class="sxs-lookup"><span data-stu-id="a05db-278">The second item will be partially picked for position 1, and new work will be created to pick the remaining quantity to fulfill the order.</span></span>

1. <span data-ttu-id="a05db-279">メニュー ボタン (ハンバーガーまたはハンバーガー ボタンと呼ばれる場合もあります) を選択し、続いて**満杯のポジション**を選択します。</span><span class="sxs-lookup"><span data-stu-id="a05db-279">Select the Menu button (sometimes referred to as the hamburger or the hamburger button), and then select **Position full**.</span></span>
1. <span data-ttu-id="a05db-280">満杯になっているポジションを特定し、*1*を選択します。</span><span class="sxs-lookup"><span data-stu-id="a05db-280">Identify the position that is full, and select *1*.</span></span>
1. <span data-ttu-id="a05db-281">**OK** (チェックマーク記号) を選択します。</span><span class="sxs-lookup"><span data-stu-id="a05db-281">Select **OK** (check mark symbol).</span></span>
1. <span data-ttu-id="a05db-282">1 のポジションにピック可能なピック量を入力します。</span><span class="sxs-lookup"><span data-stu-id="a05db-282">Enter the pick quantity that can still be picked into position 1.</span></span> <span data-ttu-id="a05db-283">ピッキングされる品目番号は、システムによって決定可能です。</span><span class="sxs-lookup"><span data-stu-id="a05db-283">The system can determine which item number is being picked.</span></span>
1. <span data-ttu-id="a05db-284">*2* と入力します。</span><span class="sxs-lookup"><span data-stu-id="a05db-284">Enter *2*.</span></span>
1. <span data-ttu-id="a05db-285">**OK** (チェックマーク記号) を選択します。</span><span class="sxs-lookup"><span data-stu-id="a05db-285">Select **OK** (check mark symbol).</span></span>
1. <span data-ttu-id="a05db-286">品目番号を確認して、残りの品目のピッキングを 2 のポジションに対して完了します。</span><span class="sxs-lookup"><span data-stu-id="a05db-286">Confirm the item number to complete the pick of the remaining item into position 2.</span></span>
1. <span data-ttu-id="a05db-287">**品目**フィールドを *T0100* に設定します。</span><span class="sxs-lookup"><span data-stu-id="a05db-287">Set the **ITEM** field to *T0100*.</span></span>
1. <span data-ttu-id="a05db-288">**OK** (チェックマーク記号) を選択します。</span><span class="sxs-lookup"><span data-stu-id="a05db-288">Select **OK** (check mark symbol).</span></span>
1. <span data-ttu-id="a05db-289">**LP** フィールドを *LPREPL04* に設定して、品目がピッキングされるライセンス プレートを入力します。</span><span class="sxs-lookup"><span data-stu-id="a05db-289">Enter the license plate that the item is being picked from by setting the **LP** field to *LPREPL04*.</span></span>
1. <span data-ttu-id="a05db-290">**OK** (チェックマーク記号) を選択します。</span><span class="sxs-lookup"><span data-stu-id="a05db-290">Select **OK** (check mark symbol).</span></span>
1. <span data-ttu-id="a05db-291">ポシション 2 (販売注文 2 に使用する) の位置にソートされる品目 (*T0100*) と数量 (*2*ea) の詳細を表示します。</span><span class="sxs-lookup"><span data-stu-id="a05db-291">View the details that are shown for the item (*T0100*) and quantity (*2* ea) that will be sorted into position 2 (for sales order 2).</span></span>
1. <span data-ttu-id="a05db-292">**POSITION NA** フィールドを *2* に設定します。</span><span class="sxs-lookup"><span data-stu-id="a05db-292">Set the **POSITION NA** field to *2*.</span></span>
1. <span data-ttu-id="a05db-293">**OK** (チェックマーク記号) を選択します。</span><span class="sxs-lookup"><span data-stu-id="a05db-293">Select **OK** (check mark symbol).</span></span>
1. <span data-ttu-id="a05db-294">ポシション 1 (販売注文 1 に使用する) の位置にソートされる品目 (*T0100*) と数量 (*2*ea) の詳細を表示します。</span><span class="sxs-lookup"><span data-stu-id="a05db-294">View the details that are shown for the item (*T0100*) and quantity (*2* ea) that will be sorted into position 1 (for sales order 1).</span></span>
1. <span data-ttu-id="a05db-295">**POSITION NA** フィールドを *1* に設定します。</span><span class="sxs-lookup"><span data-stu-id="a05db-295">Set the **POSITION NA** field to *1*.</span></span>
1. <span data-ttu-id="a05db-296">**OK** (チェックマーク記号) を選択します。</span><span class="sxs-lookup"><span data-stu-id="a05db-296">Select **OK** (check mark symbol).</span></span>

    <span data-ttu-id="a05db-297">**タスク : クラスター ピッキングの作成 : プット** ページが表示されます。</span><span class="sxs-lookup"><span data-stu-id="a05db-297">The **TASK: Cluster Pick Create: Put** page appears.</span></span>

<span data-ttu-id="a05db-298">このシナリオでは、クラスターピッキングが完了しており、ユーザーは、ポジション 1とポジション 2からステージング場所である *STAGE01* にピック済品目を入れるように指示されています。</span><span class="sxs-lookup"><span data-stu-id="a05db-298">In this scenario, the cluster pick has been completed, and the user is directed to put away the picked items from position 1 and position 2 into staging location *STAGE01*.</span></span>

1. <span data-ttu-id="a05db-299">ページの情報を確認します。</span><span class="sxs-lookup"><span data-stu-id="a05db-299">Review the information on the page.</span></span> <span data-ttu-id="a05db-300">総数である *44* がステージング場所にプットされることを示しています。</span><span class="sxs-lookup"><span data-stu-id="a05db-300">It shows that a total quantity of *44* will be put to the staging location.</span></span>
1. <span data-ttu-id="a05db-301">**OK** (チェックマーク記号) を選択します。</span><span class="sxs-lookup"><span data-stu-id="a05db-301">Select **OK** (check mark symbol).</span></span>

    <span data-ttu-id="a05db-302">「クラスターが完了」しましたというメッセージが表示されます。</span><span class="sxs-lookup"><span data-stu-id="a05db-302">You receive a "Cluster Completed" message.</span></span>

<span data-ttu-id="a05db-303">以上で、**売上のピッキング**メニューの品目を使用して残余数量を選択できるようになります。</span><span class="sxs-lookup"><span data-stu-id="a05db-303">You can now use the **Sales Picking** menu item to pick the remaining quantity.</span></span> <span data-ttu-id="a05db-304">その後、**売上の荷積** メニュー品目を使用して、ステージング場所から荷積ドックに品目を移動することができます。</span><span class="sxs-lookup"><span data-stu-id="a05db-304">You can then use the **Sales loading** menu item to move the items from the staging location to the loading dock.</span></span>
