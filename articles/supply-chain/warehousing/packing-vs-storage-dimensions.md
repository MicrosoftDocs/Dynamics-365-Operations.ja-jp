---
title: 梱包とストレージへのさまざまな分析コードの設定
description: このトピックでは、指定した各分析コードを使用するプロセス (梱包、ストレージ、または入れ子になった梱包) を指定する方法を示します。
author: mirzaab
manager: tfehr
ms.date: 01/28/2021
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: WHSPhysDimUOM
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: mirzaab
ms.search.validFrom: 2021-01-28
ms.dyn365.ops.version: Release 10.0.17
ms.openlocfilehash: 004d9b4522335b481b640ef0fe35f4db66e3c9f5
ms.sourcegitcommit: b7a7a14f8650913f6797ae1c4a82ad8adfe415fd
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 01/28/2021
ms.locfileid: "5078282"
---
# <a name="set-different-dimensions-for-packing-and-storage"></a><span data-ttu-id="206d8-103">梱包とストレージへのさまざまな分析コードの設定</span><span class="sxs-lookup"><span data-stu-id="206d8-103">Set different dimensions for packing and storage</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="206d8-104">一部の品目は、複数の異なるプロセスで物理的な分析コードをそれぞれ異なる方法で追跡する必要があるなどの方法で梱包または格納されます。</span><span class="sxs-lookup"><span data-stu-id="206d8-104">Some items are packed or stored in such a way that you may need to track physical dimensions differently for each of several different processes.</span></span> <span data-ttu-id="206d8-105">*梱包製品分析コード* 機能を使用すると、製品ごとに 1 つ以上のタイプの分析コードを設定できます。</span><span class="sxs-lookup"><span data-stu-id="206d8-105">The *Packaging product dimensions* feature lets you set up one or several types of dimensions for each product.</span></span> <span data-ttu-id="206d8-106">各分析コード タイプは、一連の物理的測定 (重量、幅、奥行、高さ) を提供し、これらの物理的測定値が適用されるプロセスを設定します。</span><span class="sxs-lookup"><span data-stu-id="206d8-106">Each dimension type provides a set of physical measurements (weight, width, depth, and height), and establishes the process where those physical measurement values apply.</span></span> <span data-ttu-id="206d8-107">この機能が有効な場合、システムは次のタイプの分析コードをサポートします。</span><span class="sxs-lookup"><span data-stu-id="206d8-107">When this feature is enabled, your system will support the following types of dimensions:</span></span>

- <span data-ttu-id="206d8-108">*ストレージ* - 保管分析コードを場所の容積測定スペースと共に使用して、各品目をさまざまな倉庫の場所に保管できる数量を決定します。</span><span class="sxs-lookup"><span data-stu-id="206d8-108">*Storage* - Storage dimensions are used along with location volumetrics to determine how many of each item can be stored in various warehouse locations.</span></span>
- <span data-ttu-id="206d8-109">*梱包* - 梱包分析コードは、コンテナ詰めと手動梱包プロセスで使用され、各品目がさまざまなコンテナ タイプに収まる数を決定します。</span><span class="sxs-lookup"><span data-stu-id="206d8-109">*Packing* - Packing dimensions are used during containerization and the manual packing process to determine how many of each item will fit in various container types.</span></span>
- <span data-ttu-id="206d8-110">*入れ子になった梱包* - 入れ子になった梱包分析コードは、梱包プロセスに複数のレベルが含まれる場合に使用されます。</span><span class="sxs-lookup"><span data-stu-id="206d8-110">*Nested packing* - Nested packing dimensions are used when the packing process contains multiple levels.</span></span>

<span data-ttu-id="206d8-111">*梱包製品分析コード* 機能を無効 にした場合でも、*ストレージ* 分析コードがサポートされます。</span><span class="sxs-lookup"><span data-stu-id="206d8-111">*Storage* dimensions are supported even when the *Packaging product dimensions* feature isn't enabled.</span></span> <span data-ttu-id="206d8-112">これらは、Supply Chain Management の **物理分析コード** ページを使用して設定します。</span><span class="sxs-lookup"><span data-stu-id="206d8-112">You set these up using the **Physical dimension** page in Supply Chain Management.</span></span> <span data-ttu-id="206d8-113">これらの分析コードは、梱包と入れ子になった梱包分析コードが指定されていないすべてのプロセスで使用されます。</span><span class="sxs-lookup"><span data-stu-id="206d8-113">These dimensions are used by all processes where the packing and nested packing dimensions aren't specified.</span></span>

<span data-ttu-id="206d8-114">*梱包* と *入れ子になった梱包* 分析コードは、**梱包製品分析コード** 機能を有効にした場合に追加される *物理的な製品分析コード* ページを使用 して設定されます。</span><span class="sxs-lookup"><span data-stu-id="206d8-114">*Packing* and *nested packing* dimensions are set up using the **Physical product dimensions** page, which is added when you enable the *Packaging product dimensions* feature.</span></span>
<span data-ttu-id="206d8-115">このトピックでは、この機能の使い方を説明するシナリオを示します。</span><span class="sxs-lookup"><span data-stu-id="206d8-115">This topic provides a scenario that illustrates how to use this feature.</span></span>

## <a name="turn-on-the-packaging-product-dimensions-feature"></a><span data-ttu-id="206d8-116">梱包製品分析コード機能をオンにする</span><span class="sxs-lookup"><span data-stu-id="206d8-116">Turn on the packaging product dimensions feature</span></span>

<span data-ttu-id="206d8-117">この機能を使用するには、システム上で有効にする必要があります。</span><span class="sxs-lookup"><span data-stu-id="206d8-117">Before you can use this feature, it must be turned on in your system.</span></span> <span data-ttu-id="206d8-118">管理者は、[機能の管理](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) ワークスペースを使用して、機能の状態を確認し、必要に応じて有効にすることができます。</span><span class="sxs-lookup"><span data-stu-id="206d8-118">Admins can use the [Feature management](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) workspace to check the status of the feature and turn it on if it's required.</span></span> <span data-ttu-id="206d8-119">この機能は、次のようにして表示されます。</span><span class="sxs-lookup"><span data-stu-id="206d8-119">There, the feature is listed in the following way:</span></span>

- <span data-ttu-id="206d8-120">**モジュール:** *倉庫管理*</span><span class="sxs-lookup"><span data-stu-id="206d8-120">**Module:** *Warehouse management*</span></span>
- <span data-ttu-id="206d8-121">**機能名:** *梱包製品分析コード*</span><span class="sxs-lookup"><span data-stu-id="206d8-121">**Feature name:** *Packaging product dimensions*</span></span>

## <a name="example-scenario"></a><span data-ttu-id="206d8-122">シナリオ例</span><span class="sxs-lookup"><span data-stu-id="206d8-122">Example scenario</span></span>

### <a name="set-up-the-scenario"></a><span data-ttu-id="206d8-123">シナリオを設定する</span><span class="sxs-lookup"><span data-stu-id="206d8-123">Set up the scenario</span></span>

<span data-ttu-id="206d8-124">シナリオ例を実行する前に、このセクションの説明に従ってシステムを準備する必要があります。</span><span class="sxs-lookup"><span data-stu-id="206d8-124">Before you can run the example scenario, you must prepare your system as described in this section.</span></span>

#### <a name="enable-demo-data"></a><span data-ttu-id="206d8-125">デモ データを有効にする</span><span class="sxs-lookup"><span data-stu-id="206d8-125">Enable demo data</span></span>

<span data-ttu-id="206d8-126">ここで指定されたデモ レコードと値を使用してシナリオを実行するには、標準 [デモ データ](../../fin-ops-core/dev-itpro/deployment/deploy-demo-environment.md) がインストールされているシステムを使用する必要があります。</span><span class="sxs-lookup"><span data-stu-id="206d8-126">To work through this scenario using the demo records and values that are specified here, you must be on a system where the standard [demo data](../../fin-ops-core/dev-itpro/deployment/deploy-demo-environment.md) is installed.</span></span> <span data-ttu-id="206d8-127">また、開始する前に *USMF* 法人を選択する必要があります。</span><span class="sxs-lookup"><span data-stu-id="206d8-127">Additionally, you must select the *USMF* legal entity before you begin.</span></span>

#### <a name="add-a-new-physical-dimension-to-a-product"></a><span data-ttu-id="206d8-128">製品への新しい物理的分析コードの追加</span><span class="sxs-lookup"><span data-stu-id="206d8-128">Add a new physical dimension to a product</span></span>

<span data-ttu-id="206d8-129">次の手順に従って、製品の新しい物理的分析コードを追加します。</span><span class="sxs-lookup"><span data-stu-id="206d8-129">Add a new physical dimension for a product by doing the following:</span></span>

1. <span data-ttu-id="206d8-130">**製品管理情報 \> 製品 \> リリースされた製品** の順に移動します。</span><span class="sxs-lookup"><span data-stu-id="206d8-130">Go to **Product information management \> Products \> Released products**.</span></span>
1. <span data-ttu-id="206d8-131">製品を **品目番号** *A0001* で選択します。</span><span class="sxs-lookup"><span data-stu-id="206d8-131">Select the product with **Item number** *A0001*.</span></span>
1. <span data-ttu-id="206d8-132">アクション ペインの **在庫の管理** タブを開いて、**倉庫** グループから、**現物製品分析コード** を選択します。</span><span class="sxs-lookup"><span data-stu-id="206d8-132">On the Action Pane, open the **Manage inventory** tab and, from the **Warehouse** group, select **Physical product dimensions**.</span></span>
1. <span data-ttu-id="206d8-133">**現物製品分析コード** ページが開きます。</span><span class="sxs-lookup"><span data-stu-id="206d8-133">The **Physical product dimensions** page opens.</span></span> <span data-ttu-id="206d8-134">アクション ペインで、**新規** を選択して新規分析コードをグリッドに追加して、次のフィールドを設定します。</span><span class="sxs-lookup"><span data-stu-id="206d8-134">On the Action Pane, select **New** to add a new dimension to the grid with the following settings:</span></span>
    - <span data-ttu-id="206d8-135">**現物分析コードの種類** - *梱包*</span><span class="sxs-lookup"><span data-stu-id="206d8-135">**Physical dimension type** - *Packing*</span></span>
    - <span data-ttu-id="206d8-136">**物理単位** - *個数*</span><span class="sxs-lookup"><span data-stu-id="206d8-136">**Physical unit** - *pcs*</span></span>
    - <span data-ttu-id="206d8-137">**重量** - *4*</span><span class="sxs-lookup"><span data-stu-id="206d8-137">**Weight** - *4*</span></span>
    - <span data-ttu-id="206d8-138">**重量単位** - *kg*</span><span class="sxs-lookup"><span data-stu-id="206d8-138">**Weight unit** - *kg*</span></span>
    - <span data-ttu-id="206d8-139">**Depth** - *3*</span><span class="sxs-lookup"><span data-stu-id="206d8-139">**Depth** - *3*</span></span>
    - <span data-ttu-id="206d8-140">**高さ** - *4*</span><span class="sxs-lookup"><span data-stu-id="206d8-140">**Height** - *4*</span></span>
    - <span data-ttu-id="206d8-141">**幅** - *3*</span><span class="sxs-lookup"><span data-stu-id="206d8-141">**Width** - *3*</span></span>
    - <span data-ttu-id="206d8-142">**長さ** - *cm*</span><span class="sxs-lookup"><span data-stu-id="206d8-142">**Length** - *cm*</span></span>
    - <span data-ttu-id="206d8-143">**容積単位** - *cm3*</span><span class="sxs-lookup"><span data-stu-id="206d8-143">**Volume unit** - *cm3*</span></span>

<span data-ttu-id="206d8-144">**容積** フィールドは、**奥行き**、**高さ**、および **幅** の設定に基づいて自動的に計算されます。</span><span class="sxs-lookup"><span data-stu-id="206d8-144">The **Volume** field is automatically calculated based on your **Depth**, **Height**, and **Width** settings.</span></span>

#### <a name="create-a-new-container-type"></a><span data-ttu-id="206d8-145">新規コンテナー タイプの作成</span><span class="sxs-lookup"><span data-stu-id="206d8-145">Create a new container type</span></span>

<span data-ttu-id="206d8-146">**倉庫管理 \>設定 \>コンテナー \>コンテナー タイプ** の順に移動して、次の設定を使用して新規レコードを作成します。</span><span class="sxs-lookup"><span data-stu-id="206d8-146">Go to **Warehouse management \> Setup \> Containers \> Container types** and create a new record with the following settings:</span></span>

- <span data-ttu-id="206d8-147">**コンテナー タイプ コード** - *短いボックス*</span><span class="sxs-lookup"><span data-stu-id="206d8-147">**Container type code** - *Short Box*</span></span>
- <span data-ttu-id="206d8-148">**説明** - *短いボックス*</span><span class="sxs-lookup"><span data-stu-id="206d8-148">**Description** - *Short Box*</span></span>
- <span data-ttu-id="206d8-149">**最大正味重量** - *50*</span><span class="sxs-lookup"><span data-stu-id="206d8-149">**Maximum net weight** - *50*</span></span>
- <span data-ttu-id="206d8-150">**容量** - *144*</span><span class="sxs-lookup"><span data-stu-id="206d8-150">**Volume** - *144*</span></span>
- <span data-ttu-id="206d8-151">**長さ** - *6*</span><span class="sxs-lookup"><span data-stu-id="206d8-151">**Length** - *6*</span></span>
- <span data-ttu-id="206d8-152">**幅** - *6*</span><span class="sxs-lookup"><span data-stu-id="206d8-152">**Width** - *6*</span></span>
- <span data-ttu-id="206d8-153">**高さ** - *4*</span><span class="sxs-lookup"><span data-stu-id="206d8-153">**Height** - *4*</span></span>

#### <a name="create-a-container-group"></a><span data-ttu-id="206d8-154">コンテナーグループの作成</span><span class="sxs-lookup"><span data-stu-id="206d8-154">Create a container group</span></span>

<span data-ttu-id="206d8-155">**倉庫管理 \>設定 \>コンテナー \>コンテナー グループ** の順に移動して、次の設定を使用して新規レコードを作成します。</span><span class="sxs-lookup"><span data-stu-id="206d8-155">Go to **Warehouse management \> Setup \> Containers \> Container groups** and create a new record with the following settings:</span></span>

- <span data-ttu-id="206d8-156">**コンテナー グループ ID** - *短いボックス*</span><span class="sxs-lookup"><span data-stu-id="206d8-156">**Container group ID** - *Short Box*</span></span>
- <span data-ttu-id="206d8-157">**説明** - *短いボックス*</span><span class="sxs-lookup"><span data-stu-id="206d8-157">**Description** - *Short Box*</span></span>

<span data-ttu-id="206d8-158">**詳細** セクションをクリックして、新しい行を追加します。</span><span class="sxs-lookup"><span data-stu-id="206d8-158">Add a new line to the **Details** section.</span></span> <span data-ttu-id="206d8-159">**コンテナタイプ** を *短いボックス* に設定します。</span><span class="sxs-lookup"><span data-stu-id="206d8-159">Set the **Container type** to *Short Box*.</span></span>

#### <a name="set-up-a-container-build-template"></a><span data-ttu-id="206d8-160">コンテナー構築テンプレートのセットアップ</span><span class="sxs-lookup"><span data-stu-id="206d8-160">Set up a container build template</span></span>

<span data-ttu-id="206d8-161">**倉庫管理 \> 設定 \> コンテナー \> コンテナー ビルド テンプレート** の順に移動して、**箱** を選択します。</span><span class="sxs-lookup"><span data-stu-id="206d8-161">Go to **Warehouse management \> Setup \> Containers \> Container build templates** and select **Boxes**.</span></span> <span data-ttu-id="206d8-162">**コンテナ グループ ID** を *短いボックス* に変更します。</span><span class="sxs-lookup"><span data-stu-id="206d8-162">Change the **Container group ID** to *Short Box*.</span></span>

### <a name="run-the-scenario"></a><span data-ttu-id="206d8-163">シナリオの実行</span><span class="sxs-lookup"><span data-stu-id="206d8-163">Run the scenario</span></span>

<span data-ttu-id="206d8-164">前のセクションの説明に従ってシステムを準備できたら、次のセクションの説明に従ってシナリオを実行できます。</span><span class="sxs-lookup"><span data-stu-id="206d8-164">After you have prepared your system as described in the previous section, you are ready to run the scenario as described in the next section.</span></span>

#### <a name="create-a-sales-order-and-create-a-shipment"></a><span data-ttu-id="206d8-165">販売注文の作成と出荷の作成</span><span class="sxs-lookup"><span data-stu-id="206d8-165">Create a sales order and create a shipment</span></span>

<span data-ttu-id="206d8-166">このプロセスでは、高さが 3 未満の品目 *梱包* 分析コードに基づいて出荷を作成します。</span><span class="sxs-lookup"><span data-stu-id="206d8-166">In this process you will create a shipment based on the item *packing* dimensions, for which the height is less than 3.</span></span>

1. <span data-ttu-id="206d8-167">**販売とマーケティング \> 販売注文 \> すべての販売注文** の順に移動します。</span><span class="sxs-lookup"><span data-stu-id="206d8-167">Go to **Sales and marketing \> Sales orders \> All sales orders**.</span></span>
1. <span data-ttu-id="206d8-168">アクション ウィンドウで、**新規** を選択します。</span><span class="sxs-lookup"><span data-stu-id="206d8-168">On the Action Pane, select **New**.</span></span>
1. <span data-ttu-id="206d8-169">**販売注文の作成** ダイアログ ボックスでは、次の値を設定します。</span><span class="sxs-lookup"><span data-stu-id="206d8-169">In the **Create sales order** dialog box, set the following values:</span></span>

    - <span data-ttu-id="206d8-170">**顧客アカウント:** *US-001*</span><span class="sxs-lookup"><span data-stu-id="206d8-170">**Customer account:** *US-001*</span></span>
    - <span data-ttu-id="206d8-171">**倉庫:** *63*</span><span class="sxs-lookup"><span data-stu-id="206d8-171">**Warehouse:** *63*</span></span>

1. <span data-ttu-id="206d8-172">**OK** を選択して販売注文を作成し、ダイアログ ボックスを閉じます。</span><span class="sxs-lookup"><span data-stu-id="206d8-172">Select **OK** to create the sales order and close the dialog box.</span></span>
1. <span data-ttu-id="206d8-173">新しい販売注文が開かれます。</span><span class="sxs-lookup"><span data-stu-id="206d8-173">The new sales order is opened.</span></span> <span data-ttu-id="206d8-174">**販売注文明細行** クイック タブのグリッドに、新しい空の明細行を含める必要があります。</span><span class="sxs-lookup"><span data-stu-id="206d8-174">It should include a new, empty line in the grid on the **Sales order lines** FastTab.</span></span> <span data-ttu-id="206d8-175">この明細行で、次の値を設定します。</span><span class="sxs-lookup"><span data-stu-id="206d8-175">On this line, set the following values:</span></span>

    - <span data-ttu-id="206d8-176">**品目番号:** *A0001*</span><span class="sxs-lookup"><span data-stu-id="206d8-176">**Item number:** *A0001*</span></span>
    - <span data-ttu-id="206d8-177">**数量:** *5*</span><span class="sxs-lookup"><span data-stu-id="206d8-177">**Quantity:** *5*</span></span>

1. <span data-ttu-id="206d8-178">**販売注文行** クイック タブで、**在庫 \> 予約** を選択します。</span><span class="sxs-lookup"><span data-stu-id="206d8-178">On the **Sales order lines** FastTab, select **Inventory \> Reservation**.</span></span>
1. <span data-ttu-id="206d8-179">**引当** ページの、アクション ウィンドウで **ロットの引当** を選択して、在庫を引当てします。</span><span class="sxs-lookup"><span data-stu-id="206d8-179">On the **Reservation** page, on the Action Pane, select **Reserve lot** to reserve the inventory.</span></span>
1. <span data-ttu-id="206d8-180">ページを閉じます。</span><span class="sxs-lookup"><span data-stu-id="206d8-180">Close the page.</span></span>
1. <span data-ttu-id="206d8-181">アクション ペインの **倉庫** タブで、**倉庫へのリリース** を選択して、倉庫の作業を作成します。</span><span class="sxs-lookup"><span data-stu-id="206d8-181">On the Action Pane, open the **Warehouse** tab and select **Release to warehouse** to create work for the warehouse.</span></span>
1. <span data-ttu-id="206d8-182">**販売注文明細行** クイック タブで、**倉庫 \> 出荷の詳細** を選択します。</span><span class="sxs-lookup"><span data-stu-id="206d8-182">On the **Sales order lines** FastTab, select **Warehouse \> Shipment details**.</span></span>
1. <span data-ttu-id="206d8-183">アクション ペインで、**輸送** タブを開き、**コンテナーの表示** を選択します。</span><span class="sxs-lookup"><span data-stu-id="206d8-183">On the Action Pane, open the **Transportation** tab and select **View containers**.</span></span> <span data-ttu-id="206d8-184">2 つの *短いボックス* コンテナに品目がコンテナ化されたのを確認します。</span><span class="sxs-lookup"><span data-stu-id="206d8-184">Confirm that the item was containerized into the two *Short Box* containers.</span></span>

#### <a name="place-an-item-into-storage"></a><span data-ttu-id="206d8-185">品目をストレージに配置する</span><span class="sxs-lookup"><span data-stu-id="206d8-185">Place an item into storage</span></span>

1. <span data-ttu-id="206d8-186">モバイル デバイスを開き、倉庫 63 にログインして **在庫 \>調整** に移動します。</span><span class="sxs-lookup"><span data-stu-id="206d8-186">Open the mobile device, sign in to warehouse 63 and go to **Inventory \> Adjust In**.</span></span>
1. <span data-ttu-id="206d8-187">**Loc** = *SHORT-01* と入力します。</span><span class="sxs-lookup"><span data-stu-id="206d8-187">Enter **Loc** = *SHORT-01*.</span></span> <span data-ttu-id="206d8-188">新規ライセンス プレートを **品目** = *A0001* と **数量** = *1 個* で作成します。</span><span class="sxs-lookup"><span data-stu-id="206d8-188">Make a new license plate with **Item** = *A0001* and **Quantity** = *1 pcs*.</span></span>
1. <span data-ttu-id="206d8-189">**OK** を選択します。</span><span class="sxs-lookup"><span data-stu-id="206d8-189">Select **OK**.</span></span> <span data-ttu-id="206d8-190">"品目 A0001 が場所の指定した分析コードに合わないため、場所 SHORT-01 に失敗しました" というエラーが表示されます。</span><span class="sxs-lookup"><span data-stu-id="206d8-190">You will receive the error "Location SHORT-01 failed because item A0001 does not fit in location's specified dimensions."</span></span> <span data-ttu-id="206d8-191">これは、製品の *ストレージ* タイプ分析コードが、場所プロファイルで指定された分析コードよりも大きいためです。</span><span class="sxs-lookup"><span data-stu-id="206d8-191">This is because the *Storage* type dimensions of the product are larger than the dimensions specified on the location profile.</span></span>
