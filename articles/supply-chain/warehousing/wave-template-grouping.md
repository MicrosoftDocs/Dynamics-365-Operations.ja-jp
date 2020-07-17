---
title: ウェーブ テンプレートのグループ化
description: ウェーブ テンプレートのグループ化を使用すると、システムはウェーブ テンプレートの設定を使用して、定義した基準に基づいて、リリース済み明細行を分割して新規または既存のウェーブに割り当てる方法を決定することができます。 この機能は、特定の基準に基づいてウェーブが作成される倉庫で役立ちますが、マネージャーは手動ではなく自動的にウェーブを作成するすることもできます。
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
ms.dyn365.ops.version: Release 10.0.8
ms.openlocfilehash: 4dd188cbd17cfed372283ecb3389633b0c0021eb
ms.sourcegitcommit: a7a7303004620d2e9cef0642b16d89163911dbb4
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 07/01/2020
ms.locfileid: "3530469"
---
# <a name="wave-template-grouping"></a><span data-ttu-id="03486-104">ウェーブ テンプレートのグループ化</span><span class="sxs-lookup"><span data-stu-id="03486-104">Wave template grouping</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="03486-105">ウェーブ テンプレートのグループ化を使用すると、システムは [ウェーブ テンプレート](tasks/configure-wave-processing.md) の設定を使用して、定義した基準に基づいて、リリース済み明細行を分割して新規または既存のウェーブに割り当てる方法を決定することができます。</span><span class="sxs-lookup"><span data-stu-id="03486-105">Wave template grouping enables the system to use [wave template](tasks/configure-wave-processing.md) setups to determine, based on criteria that you define, how it should split released lines and assign them to new or existing waves.</span></span> <span data-ttu-id="03486-106">この機能は、特定の基準に基づいてウェーブが作成される倉庫で役立ちますが、マネージャーは手動ではなく自動的にウェーブを作成するすることもできます。</span><span class="sxs-lookup"><span data-stu-id="03486-106">This feature can be useful in warehouses where waves are created based on specific criteria, but where managers prefer to create waves automatically instead of manually.</span></span> <span data-ttu-id="03486-107">この機能を使用すると、システムはグループ化フィールドの値が一致する検出した最初のウェーブに、新しくリリースされた各出荷を追加することができます。</span><span class="sxs-lookup"><span data-stu-id="03486-107">It enables the system to add each newly released shipment to the first wave that it finds that has matching grouping field values.</span></span> <span data-ttu-id="03486-108">一致するものが見つからない場合は、新しい出荷に対して新しいウェーブが作成されます。</span><span class="sxs-lookup"><span data-stu-id="03486-108">If no match is found, the system creates a new wave for the new shipment.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="03486-109">ウェーブ テンプレートのグループ化は、作業タイプが*生産原材料ピッキング*または*かんばんピッキング*の場合はサポートされていません。</span><span class="sxs-lookup"><span data-stu-id="03486-109">Wave template grouping isn't supported for the work types *production raw material picking* or *Kanban picking*.</span></span> <span data-ttu-id="03486-110">これは、ウェーブ グループ化は出荷に基づいており、これらの作業タイプでは出荷を使用しないためです。</span><span class="sxs-lookup"><span data-stu-id="03486-110">This is because wave grouping is based on shipments and these work types don't use shipments.</span></span>

## <a name="turn-on-the-wave-template-grouping-feature"></a><span data-ttu-id="03486-111">ウェーブ テンプレートのグループ化機能を有効にする</span><span class="sxs-lookup"><span data-stu-id="03486-111">Turn on the Wave template grouping feature</span></span>

<span data-ttu-id="03486-112">*ウェーブ テンプレートのグループ化*機能を使用するには、システム上で有効にする必要があります。</span><span class="sxs-lookup"><span data-stu-id="03486-112">Before you can use the *Wave template grouping* feature, it must be turned on in your system.</span></span> <span data-ttu-id="03486-113">管理者は、[機能の管理](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md)設定を使用して、機能の状態を確認し、必要に応じて有効にすることができます。</span><span class="sxs-lookup"><span data-stu-id="03486-113">Admins can use the [feature management](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) settings to check the status of the feature and turn it on if it's required.</span></span> <span data-ttu-id="03486-114">**機能管理** ワークスペースで、この機能は次のようにリストされています。</span><span class="sxs-lookup"><span data-stu-id="03486-114">In the **Feature management** workspace, the feature is listed in the following way:</span></span>

- <span data-ttu-id="03486-115">**モジュール:** *倉庫管理*</span><span class="sxs-lookup"><span data-stu-id="03486-115">**Module:** *Warehouse management*</span></span>
- <span data-ttu-id="03486-116">**機能名:** *ウェーブ テンプレートのグループ化*</span><span class="sxs-lookup"><span data-stu-id="03486-116">**Feature name:** *Wave template grouping*</span></span>

## <a name="set-a-wave-template-to-use-wave-template-grouping"></a><a name="set-up-template"></a> <span data-ttu-id="03486-117">ウェーブ テンプレートのグループ化を使用するためのウェーブ テンプレートの設定</span><span class="sxs-lookup"><span data-stu-id="03486-117">Set a wave template to use wave template grouping</span></span>

<span data-ttu-id="03486-118">ウェーブ テンプレートのグループ化を使用可能にするには、次の手順に従って、[ウェーブ テンプレート](tasks/configure-wave-processing.md) を設定します。</span><span class="sxs-lookup"><span data-stu-id="03486-118">To make wave template grouping available, follow these steps to set up your [wave template](tasks/configure-wave-processing.md).</span></span>

1. <span data-ttu-id="03486-119">**倉庫管理 \> 設定 \> ウェーブ \> ウェーブ テンプレート**の順に移動します。</span><span class="sxs-lookup"><span data-stu-id="03486-119">Go to **Warehouse management \> Setup \> Waves \> Wave templates**.</span></span>
1. <span data-ttu-id="03486-120">左ウィンドウで、設定するウェーブ テンプレートを選択します。</span><span class="sxs-lookup"><span data-stu-id="03486-120">In the left pane, select the wave template to set up.</span></span> <span data-ttu-id="03486-121">このトピックの後半でデモ データを使用してシナリオを実行する準備をしている場合は、**62 出荷の規定**テンプレートを選択します。</span><span class="sxs-lookup"><span data-stu-id="03486-121">If you're preparing to work through the scenario later in this topic by using demo data, select the **62 Shipping default** template.</span></span>
1. <span data-ttu-id="03486-122">**編集**を選択し、ページを編集モードにします。</span><span class="sxs-lookup"><span data-stu-id="03486-122">Select **Edit** to put the page into edit mode.</span></span>
1. <span data-ttu-id="03486-123">**一般**クイック タブで、次の値を設定します。</span><span class="sxs-lookup"><span data-stu-id="03486-123">On the **General** FastTab, set the following values:</span></span>

    - <span data-ttu-id="03486-124">**ウェーブの作成を自動化:** *はい*</span><span class="sxs-lookup"><span data-stu-id="03486-124">**Automate wave creation:** *Yes*</span></span>
    - <span data-ttu-id="03486-125">**未処理のウェーブへの割り当て:** *はい*</span><span class="sxs-lookup"><span data-stu-id="03486-125">**Assign to open waves:** *Yes*</span></span>
    - <span data-ttu-id="03486-126">**倉庫へのリリース時にウェーブを処理する:** *いいえ*</span><span class="sxs-lookup"><span data-stu-id="03486-126">**Process wave at release to warehouse:** *No*</span></span>

1. <span data-ttu-id="03486-127">アクション ウィンドウで、**クエリの編集**を選択してクエリのダイアログ ボックスを開きます。</span><span class="sxs-lookup"><span data-stu-id="03486-127">On the Action Pane, select **Edit query** to open the query dialog box.</span></span>
1. <span data-ttu-id="03486-128">クエリのダイアログ ボックスの**並べ替え**タブで、並べ替え基準を確認し、ウェーブをグループ化するために使用するフィールドを含むルールがあることを確認します。</span><span class="sxs-lookup"><span data-stu-id="03486-128">In the query dialog box, on the **Sorting** tab, review the sorting criteria, and make sure that there is a rule that includes the field that you want to use to group your waves.</span></span>

    <span data-ttu-id="03486-129">デモ データを使用してシナリオを実行するための準備をしている場合は、次の値を含む行を追加します :</span><span class="sxs-lookup"><span data-stu-id="03486-129">If you're preparing to work through the scenario by using demo data, add a row that has the following values:</span></span>

    - <span data-ttu-id="03486-130">**テーブル:** *出荷*</span><span class="sxs-lookup"><span data-stu-id="03486-130">**Table:** *Shipments*</span></span>
    - <span data-ttu-id="03486-131">**派生テーブル:** *出荷*</span><span class="sxs-lookup"><span data-stu-id="03486-131">**Derived table:** *Shipments*</span></span>
    - <span data-ttu-id="03486-132">**フィールド:** *配送サービス*</span><span class="sxs-lookup"><span data-stu-id="03486-132">**Field:** *Carrier service*</span></span>

        > [!NOTE]
        > <span data-ttu-id="03486-133">この値を選択すると、次のメッセージが表示される場合があります: "フィールド配送サービスはインデックス フィールドではありません。</span><span class="sxs-lookup"><span data-stu-id="03486-133">After you select this value, you might receive the following message: "Field Carrier service is not an index field.</span></span> <span data-ttu-id="03486-134">並べ替えを追加しますか ?"</span><span class="sxs-lookup"><span data-stu-id="03486-134">Do you want to add sorting on this?"</span></span> <span data-ttu-id="03486-135">**はい**を選択し並べ替えを追加します。</span><span class="sxs-lookup"><span data-stu-id="03486-135">Select **Yes** to add sorting.</span></span>

    - <span data-ttu-id="03486-136">**検索の方向:** *昇順*</span><span class="sxs-lookup"><span data-stu-id="03486-136">**Search direction:** *Ascending*</span></span>

1. <span data-ttu-id="03486-137">**OK** を選択して変更を保存し、クエリのダイアログ ボックスを閉じます。</span><span class="sxs-lookup"><span data-stu-id="03486-137">Select **OK** to save your changes and close the query dialog box.</span></span>
1. <span data-ttu-id="03486-138">アクション ウィンドウで、**ウェーブ テンプレートのグループ化**を選択します。</span><span class="sxs-lookup"><span data-stu-id="03486-138">On the Action Pane, select **Wave template grouping**.</span></span>
1. <span data-ttu-id="03486-139">**ウェーブ テンプレートのグループ化**ページで、必要に応じて、注文明細行をウェーブにグループ化するために使用する各行の**グループ化**チェック ボックスを選択します。</span><span class="sxs-lookup"><span data-stu-id="03486-139">On the **Wave template grouping** page, select the **Group by** check box for each row that you want to use to group your order lines into waves, as required.</span></span> <span data-ttu-id="03486-140">デモ データを使用してシナリオを実行する準備をしている場合は、*配送サービス*行の**グループ化**チェック ボックスを選択します。</span><span class="sxs-lookup"><span data-stu-id="03486-140">If you're preparing to work through the scenario by using demo data, select the **Group by** check box for the *Carrier service* row.</span></span>
1. <span data-ttu-id="03486-141">**保存** を選択します。</span><span class="sxs-lookup"><span data-stu-id="03486-141">Select **Save**.</span></span>
1. <span data-ttu-id="03486-142">**ウェーブ テンプレートのグループ化**ページを閉じます。</span><span class="sxs-lookup"><span data-stu-id="03486-142">Close the **Wave template grouping** page.</span></span>
1. <span data-ttu-id="03486-143">**保存**を選択して、テンプレートを保存します。</span><span class="sxs-lookup"><span data-stu-id="03486-143">Select **Save** to save your template.</span></span>

## <a name="scenario"></a><span data-ttu-id="03486-144">シナリオ</span><span class="sxs-lookup"><span data-stu-id="03486-144">Scenario</span></span>

<span data-ttu-id="03486-145">このセクションでは、この機能の動作と作業方法を学ぶためのスクリプトを説明します。</span><span class="sxs-lookup"><span data-stu-id="03486-145">This section provides a script that you can work through to learn what this feature does and how to work with it.</span></span>

### <a name="make-sample-data-available"></a><span data-ttu-id="03486-146">サンプル データを有効化する</span><span class="sxs-lookup"><span data-stu-id="03486-146">Make sample data available</span></span>

<span data-ttu-id="03486-147">ここで指定されたサンプル レコードと値を使用してシナリオを実行するには、標準[デモ データ](../../fin-ops-core/dev-itpro/deployment/deploy-demo-environment.md) がインストールされているシステムを使用する必要があります。</span><span class="sxs-lookup"><span data-stu-id="03486-147">To work through this scenario by using the sample records and values that are specified here, you must be on a system where the standard [demo data](../../fin-ops-core/dev-itpro/deployment/deploy-demo-environment.md) is installed.</span></span> <span data-ttu-id="03486-148">また、開始する前に **USMF** 法人を選択する必要があります。</span><span class="sxs-lookup"><span data-stu-id="03486-148">Additionally, you must select the **USMF** legal entity before you begin.</span></span>

<span data-ttu-id="03486-149">このシナリオは、実稼働システムで作業するときにこの機能を使用するためのガイダンスとして使用することもできます。</span><span class="sxs-lookup"><span data-stu-id="03486-149">You can also use this scenario as guidance for using the feature when you work on a production system.</span></span> <span data-ttu-id="03486-150">ただし、その場合は、独自の値に置き換える必要があり、標準のデモ データが提供するいくつかのタイプの必要なレコードが不足している可能性があります。</span><span class="sxs-lookup"><span data-stu-id="03486-150">However, in that case, you must substitute your own values, and you might be missing some types of required records that the standard demo data provides.</span></span>

### <a name="scenario-wave-template-grouping"></a><span data-ttu-id="03486-151">シナリオ: ウェーブ テンプレートのグループ化</span><span class="sxs-lookup"><span data-stu-id="03486-151">Scenario: Wave template grouping</span></span>

<span data-ttu-id="03486-152">このシナリオでは、ウェーブ テンプレートのグループ化を使用して、ウェーブ テンプレートで定義されたグループ化基準に基づいて複数のウェーブを自動的に作成する方法を示します。</span><span class="sxs-lookup"><span data-stu-id="03486-152">This scenario shows how to use wave template grouping to automatically create multiple waves, based on grouping criteria that are defined in a wave template.</span></span> <span data-ttu-id="03486-153">このシナリオでは、ウェーブ テンプレートをシステムで設定して、配送サービスごとにウェーブを 1 つ作成します。</span><span class="sxs-lookup"><span data-stu-id="03486-153">In this scenario, the wave template is set up in the system to create one wave per carrier service.</span></span>

<span data-ttu-id="03486-154">開始する前に、このトピックの前の [ウェーブ テンプレートのグループ化を使用するためのウェーブ テンプレートの設定](#set-up-template) セクションの説明に従って、ウェーブ テンプレートを準備します。</span><span class="sxs-lookup"><span data-stu-id="03486-154">Before you begin, prepare your wave template as described in the [Set a wave template to use wave template grouping](#set-up-template) section earlier in this topic.</span></span> <span data-ttu-id="03486-155">このシナリオのデモ データを使用する場合は、必ずその手順で提案されるデモ データの値を使用してください。</span><span class="sxs-lookup"><span data-stu-id="03486-155">If you will be working with demo data for this scenario, be sure to use the demo data values that are suggested in that procedure.</span></span> <span data-ttu-id="03486-156">この設定により、各販売注文に対して設定されている配送サービスに従ってウェーブがグループ化されます。</span><span class="sxs-lookup"><span data-stu-id="03486-156">This setup will group your waves according to the carrier service that is set for each sales order.</span></span>

#### <a name="create-sales-order-1"></a><span data-ttu-id="03486-157">販売注文の作成 1</span><span class="sxs-lookup"><span data-stu-id="03486-157">Create sales order 1</span></span>

1. <span data-ttu-id="03486-158">**販売とマーケティング \> 販売注文 \> すべての販売注文**の順に移動します。</span><span class="sxs-lookup"><span data-stu-id="03486-158">Go to **Sales and marketing \> Sales orders \> All sales orders**.</span></span>
1. <span data-ttu-id="03486-159">**新規**を選択して新しい販売注文を作成します。</span><span class="sxs-lookup"><span data-stu-id="03486-159">Select **New** to create a sales order.</span></span>
1. <span data-ttu-id="03486-160">**販売注文の作成**ダイアログ ボックスでは、次の値を設定します。</span><span class="sxs-lookup"><span data-stu-id="03486-160">In the **Create sales order** dialog box, set the following values:</span></span>

    - <span data-ttu-id="03486-161">**顧客**クイック タブで、**顧客 ID** フィールドを *US-004* に設定します。</span><span class="sxs-lookup"><span data-stu-id="03486-161">On the **Customer** FastTab, set the **Customer account** field to *US-004*.</span></span>
    - <span data-ttu-id="03486-162">**一般**クイック タブの**倉庫**フィールドを *62* に設定します。</span><span class="sxs-lookup"><span data-stu-id="03486-162">On the **General** FastTab, set the **Warehouse** field to *62*.</span></span>

1. <span data-ttu-id="03486-163">**OK** を選択し販売注文を作成し、**販売注文の作成**ダイアログ ボックスを閉じます。</span><span class="sxs-lookup"><span data-stu-id="03486-163">Select **OK** to create the sales order and close the **Create sales order** dialog box.</span></span>
1. <span data-ttu-id="03486-164">新しい販売注文は、**明細行**ビューで開かれます。</span><span class="sxs-lookup"><span data-stu-id="03486-164">The new sales order is opened in the **Lines** view.</span></span> <span data-ttu-id="03486-165">販売注文番号をメモします。</span><span class="sxs-lookup"><span data-stu-id="03486-165">Make a note of the sales order number.</span></span>
1. <span data-ttu-id="03486-166">**ヘッダー**表示に切り替えます。</span><span class="sxs-lookup"><span data-stu-id="03486-166">Switch to the **Header** view.</span></span>
1. <span data-ttu-id="03486-167">**配送**クイック タブの**輸送**セクションで、次の値を設定します。</span><span class="sxs-lookup"><span data-stu-id="03486-167">On the **Delivery** FastTab, in the **Transportation** section, set the following values:</span></span>

    - <span data-ttu-id="03486-168">**配送業者:** *航空貨物*</span><span class="sxs-lookup"><span data-stu-id="03486-168">**Shipping carrier:** *Air cargo*</span></span>
    - <span data-ttu-id="03486-169">**配送サービス :** *Air*</span><span class="sxs-lookup"><span data-stu-id="03486-169">**Carrier service:** *Air*</span></span>

1. <span data-ttu-id="03486-170">**明細行**ビューに戻ります。</span><span class="sxs-lookup"><span data-stu-id="03486-170">Switch back to the **Lines** view.</span></span>
1. <span data-ttu-id="03486-171">**販売注文明細行**セクションで、**明細行の追加**を選択し、行をグリッドに追加します。</span><span class="sxs-lookup"><span data-stu-id="03486-171">In the **Sales order lines** section, select **Add line** to add a line to the grid.</span></span>
1. <span data-ttu-id="03486-172">新しい明細行で、次の値を設定します。</span><span class="sxs-lookup"><span data-stu-id="03486-172">On the new line, set the following values:</span></span>

    - <span data-ttu-id="03486-173">**品目番号:** *A0002*</span><span class="sxs-lookup"><span data-stu-id="03486-173">**Item number:** *A0002*</span></span>
    - <span data-ttu-id="03486-174">**数量:** *2*</span><span class="sxs-lookup"><span data-stu-id="03486-174">**Quantity:** *2*</span></span>

1. <span data-ttu-id="03486-175">新しい注文明細行を選択し、グリッドの上にある**在庫**メニューで、**引当**を選択します。</span><span class="sxs-lookup"><span data-stu-id="03486-175">Select the new order line, and then, on the **Inventory** menu above the grid, select **Reservation**.</span></span>
1. <span data-ttu-id="03486-176">**引当**ページのアクション ウィンドウで、**引当ロット**を選択して、選択した明細行の全数量を倉庫に引当します。</span><span class="sxs-lookup"><span data-stu-id="03486-176">On the **Reservation** page, on the Action Pane, select **Reserve lot** to reserve the full quantity of the selected line in the warehouse.</span></span>
1. <span data-ttu-id="03486-177">**引当**ページを閉じて、販売注文に戻ります。</span><span class="sxs-lookup"><span data-stu-id="03486-177">Close the **Reservation** page to return to the sales order.</span></span>
1. <span data-ttu-id="03486-178">アクション ペインの、**倉庫**タブにある**アクション**グループで、**倉庫にリリース**を選択します。</span><span class="sxs-lookup"><span data-stu-id="03486-178">On the Action Pane, on the **Warehouse** tab, in the **Actions** group, select **Release to warehouse**.</span></span>
1. <span data-ttu-id="03486-179">この注文の出荷とウェーブを示す情報メッセージが表示されます。</span><span class="sxs-lookup"><span data-stu-id="03486-179">You receive an informational message that shows the shipment and wave for this order.</span></span> <span data-ttu-id="03486-180">ウェーブ ID 番号と出荷 ID 番号をメモします。</span><span class="sxs-lookup"><span data-stu-id="03486-180">Make a note of the wave ID number and the shipment ID numbers.</span></span>

#### <a name="view-the-wave-that-was-created-from-sales-order-1"></a><span data-ttu-id="03486-181">販売注文 1 から作成されたウェーブの表示</span><span class="sxs-lookup"><span data-stu-id="03486-181">View the wave that was created from sales order 1</span></span>

1. <span data-ttu-id="03486-182">**倉庫管理 \> 出庫ウェーブ \> 出荷ウェーブ \> すべてのウェーブ**の順に移動します。</span><span class="sxs-lookup"><span data-stu-id="03486-182">Go to **Warehouse management \> Outbound waves \> Shipment waves \> All waves**.</span></span>
1. <span data-ttu-id="03486-183">販売注文から作成されたウェーブ ID を選択します。</span><span class="sxs-lookup"><span data-stu-id="03486-183">Select the wave ID that was created from the sales order.</span></span>
1. <span data-ttu-id="03486-184">ウェーブ ID のリンクを選択して、ウェーブ詳細ページを開きます。</span><span class="sxs-lookup"><span data-stu-id="03486-184">Select the wave ID link to open the wave details page.</span></span>
1. <span data-ttu-id="03486-185">**ウェーブ明細行**クイック タブに出荷が追加されていることを確認します。</span><span class="sxs-lookup"><span data-stu-id="03486-185">Notice that the shipment has been added to the **Wave lines** FastTab.</span></span>

#### <a name="create-sales-order-2"></a><span data-ttu-id="03486-186">販売注文の作成 2</span><span class="sxs-lookup"><span data-stu-id="03486-186">Create sales order 2</span></span>

1. <span data-ttu-id="03486-187">**販売とマーケティング \> 販売注文 \> すべての販売注文**の順に移動します。</span><span class="sxs-lookup"><span data-stu-id="03486-187">Go to **Sales and marketing \> Sales orders \> All sales orders**.</span></span>
1. <span data-ttu-id="03486-188">**新規**を選択して新しい販売注文を作成します。</span><span class="sxs-lookup"><span data-stu-id="03486-188">Select **New** to create a sales order.</span></span>
1. <span data-ttu-id="03486-189">**販売注文の作成**ダイアログ ボックスでは、次の値を設定します。</span><span class="sxs-lookup"><span data-stu-id="03486-189">In the **Create sales order** dialog box, set the following values:</span></span>

    - <span data-ttu-id="03486-190">**顧客**クイック タブで、**顧客 ID** フィールドを *US-005* に設定します。</span><span class="sxs-lookup"><span data-stu-id="03486-190">On the **Customer** FastTab, set the **Customer account** field to *US-005*.</span></span>
    - <span data-ttu-id="03486-191">**一般**クイック タブの**倉庫**フィールドを *62* に設定します。</span><span class="sxs-lookup"><span data-stu-id="03486-191">On the **General** FastTab, set the **Warehouse** field to *62*.</span></span>

1. <span data-ttu-id="03486-192">**OK** を選択し販売注文を作成し、**販売注文の作成**ダイアログ ボックスを閉じます。</span><span class="sxs-lookup"><span data-stu-id="03486-192">Select **OK** to create the sales order and close the **Create sales order** dialog box.</span></span>
1. <span data-ttu-id="03486-193">新しい販売注文は、**明細行**ビューで開かれます。</span><span class="sxs-lookup"><span data-stu-id="03486-193">The new sales order is opened in the **Lines** view.</span></span> <span data-ttu-id="03486-194">販売注文番号をメモします。</span><span class="sxs-lookup"><span data-stu-id="03486-194">Make a note of the sales order number.</span></span>
1. <span data-ttu-id="03486-195">**ヘッダー**表示に切り替えます。</span><span class="sxs-lookup"><span data-stu-id="03486-195">Switch to the **Header** view.</span></span>
1. <span data-ttu-id="03486-196">**配送**クイック タブの**輸送**セクションで、次の値を設定します。</span><span class="sxs-lookup"><span data-stu-id="03486-196">On the **Delivery** FastTab, in the **Transportation** section, set the following values:</span></span>

    - <span data-ttu-id="03486-197">**配送業者:** *花の移動*</span><span class="sxs-lookup"><span data-stu-id="03486-197">**Shipping carrier:** *Flower moving*</span></span>
    - <span data-ttu-id="03486-198">**配送サービス:** *Std*</span><span class="sxs-lookup"><span data-stu-id="03486-198">**Carrier service:** *Std*</span></span>

1. <span data-ttu-id="03486-199">**明細行**ビューに戻ります。</span><span class="sxs-lookup"><span data-stu-id="03486-199">Switch back to the **Lines** view.</span></span>
1. <span data-ttu-id="03486-200">**販売注文明細行**セクションで、**明細行の追加**を選択し、行をグリッドに追加します。</span><span class="sxs-lookup"><span data-stu-id="03486-200">In the **Sales order lines** section, select **Add line** to add a line to the grid.</span></span>
1. <span data-ttu-id="03486-201">新しい明細行で、次の値を設定します。</span><span class="sxs-lookup"><span data-stu-id="03486-201">On the new line, set the following values:</span></span>

    - <span data-ttu-id="03486-202">**品目番号:** *A0001*</span><span class="sxs-lookup"><span data-stu-id="03486-202">**Item number:** *A0001*</span></span>
    - <span data-ttu-id="03486-203">**数量:** *1*</span><span class="sxs-lookup"><span data-stu-id="03486-203">**Quantity:** *1*</span></span>

1. <span data-ttu-id="03486-204">新しい注文明細行を選択し、グリッドの上にある**在庫**メニューで、**引当**を選択します。</span><span class="sxs-lookup"><span data-stu-id="03486-204">Select the new order line, and then, on the **Inventory** menu above the grid, select **Reservation**.</span></span>
1. <span data-ttu-id="03486-205">**引当**ページのアクション ウィンドウで、**引当ロット**を選択して、選択した明細行の全数量を倉庫に引当します。</span><span class="sxs-lookup"><span data-stu-id="03486-205">On the **Reservation** page, on the Action Pane, select **Reserve lot** to reserve the full quantity of the selected line in the warehouse.</span></span>
1. <span data-ttu-id="03486-206">**引当**ページを閉じて、販売注文に戻ります。</span><span class="sxs-lookup"><span data-stu-id="03486-206">Close the **Reservation** page to return to the sales order.</span></span>
1. <span data-ttu-id="03486-207">アクション ペインの、**倉庫**タブにある**アクション**グループで、**倉庫にリリース**を選択します。</span><span class="sxs-lookup"><span data-stu-id="03486-207">On the Action Pane, on the **Warehouse** tab, in the **Actions** group, select **Release to warehouse**.</span></span>
1. <span data-ttu-id="03486-208">この注文の出荷とウェーブを示す情報メッセージが表示されます。</span><span class="sxs-lookup"><span data-stu-id="03486-208">You receive an informational message that shows the shipment and wave for this order.</span></span> <span data-ttu-id="03486-209">ウェーブ ID 番号と出荷 ID 番号をメモします。</span><span class="sxs-lookup"><span data-stu-id="03486-209">Make a note of the wave ID number and the shipment ID numbers.</span></span> <span data-ttu-id="03486-210">ウェーブ ID は、最初の販売注文のウェーブ ID と異なることに注意してください。</span><span class="sxs-lookup"><span data-stu-id="03486-210">Notice that the wave ID differs from the wave ID of the first sales order.</span></span>

#### <a name="view-the-wave-that-was-created-from-sales-order-2"></a><span data-ttu-id="03486-211">販売注文 2 から作成されたウェーブの表示</span><span class="sxs-lookup"><span data-stu-id="03486-211">View the wave that was created from sales order 2</span></span>

1. <span data-ttu-id="03486-212">**倉庫管理 \> 出庫ウェーブ \> 出荷ウェーブ \> すべてのウェーブ**の順に移動します。</span><span class="sxs-lookup"><span data-stu-id="03486-212">Go to **Warehouse management \> Outbound waves \> Shipment waves \> All waves**.</span></span>
1. <span data-ttu-id="03486-213">2 番目の販売注文から作成されたウェーブ ID を選択します。</span><span class="sxs-lookup"><span data-stu-id="03486-213">Select the wave ID that was created from the second sales order.</span></span>
1. <span data-ttu-id="03486-214">ウェーブ ID のリンクを選択して、ウェーブ詳細ページを開きます。</span><span class="sxs-lookup"><span data-stu-id="03486-214">Select the wave ID link to open the wave details page.</span></span>
1. <span data-ttu-id="03486-215">**ウェーブ明細行**クイック タブに出荷が追加されていることを確認します。</span><span class="sxs-lookup"><span data-stu-id="03486-215">Notice that the shipment has been added to the **Wave lines** FastTab.</span></span>

<span data-ttu-id="03486-216">この出荷に対して作成された新しいウェーブは、最初の販売注文とは異なる配送サービスを使用しているためです。</span><span class="sxs-lookup"><span data-stu-id="03486-216">A new wave was created for this shipment, because it uses a different carrier service than the first sales order.</span></span>

#### <a name="create-sales-order-3"></a><span data-ttu-id="03486-217">販売注文の作成 3</span><span class="sxs-lookup"><span data-stu-id="03486-217">Create sales order 3</span></span>

1. <span data-ttu-id="03486-218">**販売とマーケティング \> 販売注文 \> すべての販売注文**の順に移動します。</span><span class="sxs-lookup"><span data-stu-id="03486-218">Go to **Sales and marketing \> Sales orders \> All sales orders**.</span></span>
1. <span data-ttu-id="03486-219">**新規**を選択して新しい販売注文を作成します。</span><span class="sxs-lookup"><span data-stu-id="03486-219">Select **New** to create a sales order.</span></span>
1. <span data-ttu-id="03486-220">**販売注文の作成**ダイアログ ボックスでは、次の値を設定します。</span><span class="sxs-lookup"><span data-stu-id="03486-220">In the **Create sales order** dialog box, set the following values:</span></span>

    - <span data-ttu-id="03486-221">**顧客**クイック タブで、**顧客 ID** フィールドを *US-006* に設定します。</span><span class="sxs-lookup"><span data-stu-id="03486-221">On the **Customer** FastTab, set the **Customer account** field to *US-006*.</span></span>
    - <span data-ttu-id="03486-222">**一般**クイック タブの**倉庫**フィールドを *62* に設定します。</span><span class="sxs-lookup"><span data-stu-id="03486-222">On the **General** FastTab, set the **Warehouse** field to *62*.</span></span>

1. <span data-ttu-id="03486-223">**OK** を選択し販売注文を作成し、**販売注文の作成**ダイアログ ボックスを閉じます。</span><span class="sxs-lookup"><span data-stu-id="03486-223">Select **OK** to create the sales order and close the **Create sales order** dialog box.</span></span>
1. <span data-ttu-id="03486-224">新しい販売注文は、**明細行**ビューで開かれます。</span><span class="sxs-lookup"><span data-stu-id="03486-224">The new sales order is opened in the **Lines** view.</span></span> <span data-ttu-id="03486-225">販売注文番号をメモします。</span><span class="sxs-lookup"><span data-stu-id="03486-225">Make a note of the sales order number.</span></span>
1. <span data-ttu-id="03486-226">**ヘッダー**表示に切り替えます。</span><span class="sxs-lookup"><span data-stu-id="03486-226">Switch to the **Header** view.</span></span>
1. <span data-ttu-id="03486-227">**配送**クイック タブの**輸送**セクションで、次の値を設定します。</span><span class="sxs-lookup"><span data-stu-id="03486-227">On the **Delivery** FastTab, in the **Transportation** section, set the following values:</span></span>

    - <span data-ttu-id="03486-228">**配送業者:** *航空貨物*</span><span class="sxs-lookup"><span data-stu-id="03486-228">**Shipping carrier:** *Air Cargo*</span></span>
    - <span data-ttu-id="03486-229">**配送サービス :** *Air*</span><span class="sxs-lookup"><span data-stu-id="03486-229">**Carrier service:** *Air*</span></span>

1. <span data-ttu-id="03486-230">**明細行**ビューに戻ります。</span><span class="sxs-lookup"><span data-stu-id="03486-230">Switch back to the **Lines** view.</span></span>
1. <span data-ttu-id="03486-231">**販売注文明細行**セクションで、**明細行の追加**を選択し、行をグリッドに追加します。</span><span class="sxs-lookup"><span data-stu-id="03486-231">In the **Sales order lines** section, select **Add line** to add a line to the grid.</span></span>
1. <span data-ttu-id="03486-232">新しい明細行で、次の値を設定します。</span><span class="sxs-lookup"><span data-stu-id="03486-232">On the new line, set the following values:</span></span>

    - <span data-ttu-id="03486-233">**品目番号:** *A0001*</span><span class="sxs-lookup"><span data-stu-id="03486-233">**Item number:** *A0001*</span></span>
    - <span data-ttu-id="03486-234">**数量:** *1*</span><span class="sxs-lookup"><span data-stu-id="03486-234">**Quantity:** *1*</span></span>

1. <span data-ttu-id="03486-235">新しい注文明細行を選択し、グリッドの上にある**在庫**メニューで、**引当**を選択します。</span><span class="sxs-lookup"><span data-stu-id="03486-235">Select the new order line, and then, on the **Inventory** menu above the grid, select **Reservation**.</span></span>
1. <span data-ttu-id="03486-236">**引当**ページのアクション ウィンドウで、**引当ロット**を選択して、選択した明細行の全数量を倉庫に引当します。</span><span class="sxs-lookup"><span data-stu-id="03486-236">On the **Reservation** page, on the Action Pane, select **Reserve lot** to reserve the full quantity of the selected line in the warehouse.</span></span>
1. <span data-ttu-id="03486-237">**引当**ページを閉じて、販売注文に戻ります。</span><span class="sxs-lookup"><span data-stu-id="03486-237">Close the **Reservation** page to return to the sales order.</span></span>
1. <span data-ttu-id="03486-238">アクション ペインの、**倉庫**タブにある**アクション**グループで、**倉庫にリリース**を選択します。</span><span class="sxs-lookup"><span data-stu-id="03486-238">On the Action Pane, on the **Warehouse** tab, in the **Actions** group, select **Release to warehouse**.</span></span>
1. <span data-ttu-id="03486-239">この注文の出荷とウェーブを示す情報メッセージが表示されます。</span><span class="sxs-lookup"><span data-stu-id="03486-239">You receive an informational message that shows the shipment and wave for this order.</span></span> <span data-ttu-id="03486-240">ウェーブ ID 番号と出荷 ID 番号をメモします。</span><span class="sxs-lookup"><span data-stu-id="03486-240">Make a note of the wave ID number and the shipment ID numbers.</span></span> <span data-ttu-id="03486-241">この出荷は、最初の販売注文からの既存のウェーブに割り当てられています。</span><span class="sxs-lookup"><span data-stu-id="03486-241">The shipment has been assigned to the existing wave from the first sales order.</span></span>

#### <a name="view-the-wave-for-sales-orders-1-and-3"></a><span data-ttu-id="03486-242">販売注文 1 および 3 のウェーブの表示</span><span class="sxs-lookup"><span data-stu-id="03486-242">View the wave for sales orders 1 and 3</span></span>

1. <span data-ttu-id="03486-243">**倉庫管理 \> 出庫ウェーブ \> 出荷ウェーブ \> すべてのウェーブ**の順に移動します。</span><span class="sxs-lookup"><span data-stu-id="03486-243">Go to **Warehouse management \> Outbound waves \> Shipment waves \> All waves**.</span></span>
1. <span data-ttu-id="03486-244">3 番目の販売注文から作成されたウェーブ ID を選択します。</span><span class="sxs-lookup"><span data-stu-id="03486-244">Select the wave ID that was created from the third sales order.</span></span>
1. <span data-ttu-id="03486-245">ウェーブ ID のリンクを選択して、ウェーブ詳細ページを開きます。</span><span class="sxs-lookup"><span data-stu-id="03486-245">Select the wave ID link to open the wave details page.</span></span>
1. <span data-ttu-id="03486-246">最初の販売注文の出荷と共に、**ウェーブ明細行**クイック タブに出荷が追加されていることを確認します。</span><span class="sxs-lookup"><span data-stu-id="03486-246">Notice that the shipment has been added to the **Wave lines** FastTab, together with the shipment for the first sales order.</span></span>
