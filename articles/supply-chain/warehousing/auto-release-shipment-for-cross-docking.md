---
title: クロスドッキングの自動リリース出荷
description: このトピックでは、数量が生産出荷の場所から出庫場所に直接移動されるようにするために、需要数量を供給する製造オーダーが完了済として報告されたときに、需要オーダーを倉庫に自動的にリリースできるクロスドッキング戦略について説明します。
author: omulvad
manager: tfehr
ms.date: 10/15/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: WHSCrossDockingTemplate
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: kamaybac
ms.search.validFrom: 2019-10-1
ms.dyn365.ops.version: 10.0.6
ms.openlocfilehash: bcae977ede91dcaf4e455353f023e9eee4fcb2b1
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 01/15/2021
ms.locfileid: "4977491"
---
# <a name="auto-release-shipment-for-cross-docking"></a><span data-ttu-id="82a51-103">クロスドッキングの自動リリース出荷</span><span class="sxs-lookup"><span data-stu-id="82a51-103">Auto-release shipment for cross-docking</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="82a51-104">このトピックでは、需要数量を供給する製造オーダーが完了済として報告されたときに、需要オーダーを倉庫に自動的にリリースできるようにする、クロスドッキング戦略について説明します。</span><span class="sxs-lookup"><span data-stu-id="82a51-104">This topic describes a cross-docking strategy that lets you automatically release a demand order to the warehouse when the production order that supplies the demand quantity is reported as finished.</span></span> <span data-ttu-id="82a51-105">このようにして、需要オーダーのフルフィルメントに必要な数量は、生産出荷場所から出庫場所に直接移動されます。</span><span class="sxs-lookup"><span data-stu-id="82a51-105">In this way, the quantity that is required for fulfillment of the demand order is moved directly from the production output location to the outbound location.</span></span>

<span data-ttu-id="82a51-106">クロスドッキングは、出庫注文のフルフィルメントに必要な数量が、入庫注文を受け取った場所からの注文の出庫ドックまたはステージング領域に送られる倉庫処理フローです。</span><span class="sxs-lookup"><span data-stu-id="82a51-106">Cross-docking is a warehouse handling flow where the quantity that is required to fulfill an outbound order is directed to the order's outbound dock or staging area from the location where the inbound order was received.</span></span> <span data-ttu-id="82a51-107">(入庫注文は、発注書、移動オーダー、または製造オーダーのいずれかにすることができます。) 高度なクロスドッキング機能は、すべての供給と需要オーダーをサポートし、クロスドッキングの営業案件が識別される前に出庫需要がリリースされるようにする必要があるのに対し、自動リリース出荷機能には次の特性があります。</span><span class="sxs-lookup"><span data-stu-id="82a51-107">(The inbound order can be a purchase order, a transfer order, or a production order.) Whereas the Advanced cross-docking feature supports all supply and demand orders, and it requires that the outbound demand be released before the cross-dock opportunity is identified, the Auto-release shipment feature has these characteristics:</span></span>

- <span data-ttu-id="82a51-108">この機能では、供給としては製造オーダーのみ、需要としては販売注文と移動オーダーのみがサポートされます。</span><span class="sxs-lookup"><span data-stu-id="82a51-108">It supports only production orders as supply, and only sales orders and transfer orders as demand.</span></span>
- <span data-ttu-id="82a51-109">供給受領書が登録される前 (つまり、生産が完了済として報告される前) に、需要オーダーが倉庫にリリースされていない場合でも、クロスドッキング操作を開始できます。</span><span class="sxs-lookup"><span data-stu-id="82a51-109">The cross-docking operation can be started even if the demand order wasn't released to the warehouse before the supply receipt was registered (that is, before the production was reported as finished).</span></span>

<span data-ttu-id="82a51-110">このクロスドッキング機能には 2 つの利点があります。</span><span class="sxs-lookup"><span data-stu-id="82a51-110">This cross-docking functionality has two advantages:</span></span>

- <span data-ttu-id="82a51-111">この倉庫工程では、これらの数量が出庫注文をフルフィルメントするために再び集荷される場合、完成品の数量を通常の倉庫の保管エリアに戻すステップを省略できます。</span><span class="sxs-lookup"><span data-stu-id="82a51-111">The warehouse operations can skip the step of putting away quantities of finished goods to the regular warehouse storage area if those quantities will just be picked up again to fulfill the outbound order.</span></span> <span data-ttu-id="82a51-112">代わりに、出荷の場所から梱包/出荷場所に、数量を 1 回移動できます。</span><span class="sxs-lookup"><span data-stu-id="82a51-112">Instead, the quantities can be moved one time, from the output location to a packing/shipping location.</span></span> <span data-ttu-id="82a51-113">この機能により、在庫の処理回数を最小限に抑えることができ、最終的に倉庫の作業現場で時間とスペースを最大限に節約できます。</span><span class="sxs-lookup"><span data-stu-id="82a51-113">In this way, the functionality helps minimize the number of times that stock is handled and, ultimately, helps maximize time and space savings on the warehouse shop floor.</span></span>
- <span data-ttu-id="82a51-114">倉庫工程では、関連付けられている製造オーダーの完成品の出荷が完了済として報告されるまで、販売注文のリリースと倉庫への移動オーダーを延期できます。</span><span class="sxs-lookup"><span data-stu-id="82a51-114">The warehouse operations can postpone the release of sales orders and transfer orders to the warehouse until the output of finished goods for the associated production order is reported as finished.</span></span> <span data-ttu-id="82a51-115">この利点は、製造リード タイムが見込み生産環境のリード タイムより長くなる傾向があるような、受注生産環境においては特に関係があります。</span><span class="sxs-lookup"><span data-stu-id="82a51-115">This advantage might be especially relevant in make-to-order production environments, where manufacturing lead times tend to be longer than the lead times in make-to-stock environments.</span></span>

## <a name="prerequisites"></a><span data-ttu-id="82a51-116">必要条件</span><span class="sxs-lookup"><span data-stu-id="82a51-116">Prerequisites</span></span>

| <span data-ttu-id="82a51-117">前提条件</span><span class="sxs-lookup"><span data-stu-id="82a51-117">Prerequisite</span></span> | <span data-ttu-id="82a51-118">説明</span><span class="sxs-lookup"><span data-stu-id="82a51-118">Description</span></span> |
|---|---|
| <span data-ttu-id="82a51-119">項目</span><span class="sxs-lookup"><span data-stu-id="82a51-119">Item</span></span> | <span data-ttu-id="82a51-120">品目は倉庫管理プロセスで有効にする必要があります。</span><span class="sxs-lookup"><span data-stu-id="82a51-120">The item must be enabled for warehouse management processes.</span></span><p><span data-ttu-id="82a51-121">**注:** CW が有効な品目は、クロスドッキング プロセスに含めることはできません。</span><span class="sxs-lookup"><span data-stu-id="82a51-121">**Note:** Catch-weight-enabled items can't be included in the cross-docking processes.</span></span></p> |
| <span data-ttu-id="82a51-122">倉庫</span><span class="sxs-lookup"><span data-stu-id="82a51-122">Warehouse</span></span> | <span data-ttu-id="82a51-123">倉庫は倉庫管理プロセスで有効にする必要があります。</span><span class="sxs-lookup"><span data-stu-id="82a51-123">The warehouse must be enabled for warehouse management processes.</span></span> |
| <span data-ttu-id="82a51-124">クロスドッキング テンプレート</span><span class="sxs-lookup"><span data-stu-id="82a51-124">Cross-docking templates</span></span> | <span data-ttu-id="82a51-125">特定の倉庫に対して、**供給受領時** の需要リリース ポリシーを使用する少なくとも 1 つのクロスドッキング テンプレートを設定する必要があります。</span><span class="sxs-lookup"><span data-stu-id="82a51-125">At least one cross-docking template that uses the **At supply receipt** demand release policy must be set up for a given warehouse.</span></span> |
| <span data-ttu-id="82a51-126">作業クラス</span><span class="sxs-lookup"><span data-stu-id="82a51-126">Work class</span></span> | <span data-ttu-id="82a51-127">**クロスドッキング** 作業指示書タイプには、クロスドッキング作業クラス ID を作成する必要があります。</span><span class="sxs-lookup"><span data-stu-id="82a51-127">A cross-docking work class ID must be created for the **Cross docking** work order type.</span></span> |
| <span data-ttu-id="82a51-128">作業テンプレート</span><span class="sxs-lookup"><span data-stu-id="82a51-128">Work templates</span></span> | <span data-ttu-id="82a51-129">**クロスドッキング** 作業指示書タイプの作業テンプレートは、クロスドッキングのピッキングとプット作業を作成するために必要です。</span><span class="sxs-lookup"><span data-stu-id="82a51-129">Work templates of the **Cross docking** work order type are required to create cross-docking pick and put work.</span></span> |
| <span data-ttu-id="82a51-130">場所のディレクティブ</span><span class="sxs-lookup"><span data-stu-id="82a51-130">Location directives</span></span> | <span data-ttu-id="82a51-131">**クロスドッキング** 作業指示書タイプの場所のディレクティブは、販売注文の数量が梱包および出荷される場所でのプット作業をガイドするために必要です。</span><span class="sxs-lookup"><span data-stu-id="82a51-131">Location directives of the **Cross docking** work order type are required to guide put work in the locations where sales order quantities will be packed and shipped.</span></span> |
| <span data-ttu-id="82a51-132">需要オーダーと製造オーダーとの間のマーキング</span><span class="sxs-lookup"><span data-stu-id="82a51-132">Marking between a demand order and a production order</span></span> | <span data-ttu-id="82a51-133">倉庫システムは、出庫注文の出荷の自動リリースをトリガーしたり、販売注文と移動オーダーが製造オーダーに対して引当およびマークされている場合にのみ、完了済アクションの場所からのクロスドッキング作業を作成したりできます。</span><span class="sxs-lookup"><span data-stu-id="82a51-133">The warehouse system can trigger automatic release of the outbound order shipment and create cross-docking work from the output location at the report-as-finished action only if sales orders and transfer orders are reserved and marked against a production order.</span></span> |

## <a name="example-cross-docking-flow"></a><span data-ttu-id="82a51-134">クロスドッキング フローの例</span><span class="sxs-lookup"><span data-stu-id="82a51-134">Example cross-docking flow</span></span>

<span data-ttu-id="82a51-135">一般的なクロスドッキング フローは、次の主要なステップで構成されます。</span><span class="sxs-lookup"><span data-stu-id="82a51-135">A typical cross-docking flow consists of the following main steps.</span></span>

1. <span data-ttu-id="82a51-136">受注管理者は、受注生産製品の販売注文を作成します。</span><span class="sxs-lookup"><span data-stu-id="82a51-136">A sales order taker creates a sales order for a make-to-order product.</span></span> <span data-ttu-id="82a51-137">通常、要求された数量は手持ちではないため、最初に生産する必要があります。</span><span class="sxs-lookup"><span data-stu-id="82a51-137">Typically, the requested quantity isn't on hand and must first be produced.</span></span>
2. <span data-ttu-id="82a51-138">受注管理者は、販売注文明細行から製造オーダーを直接作成します。</span><span class="sxs-lookup"><span data-stu-id="82a51-138">The sales order taker creates a production order directly from the sales order line.</span></span> <span data-ttu-id="82a51-139">このように、受注管理者は、販売注文の数量を製造オーダーの数量に対して引当およびマークします。</span><span class="sxs-lookup"><span data-stu-id="82a51-139">In this way, the sales order taker reserves and marks the sales order quantity against the production order quantity.</span></span> 

    <span data-ttu-id="82a51-140">または、生産計画者が、計画オーダーが確定されたときにマーキングを更新する必要があることを指定します。</span><span class="sxs-lookup"><span data-stu-id="82a51-140">Alternatively, a production planner specifies that the marking must be updated when planned orders are being firmed.</span></span>

3. <span data-ttu-id="82a51-141">製造オーダーには、次の手順が実行されます。</span><span class="sxs-lookup"><span data-stu-id="82a51-141">The production order goes through the following steps:</span></span>

    1. <span data-ttu-id="82a51-142">生産計画担当者は、製造オーダーを見積してリリースします。</span><span class="sxs-lookup"><span data-stu-id="82a51-142">A production planner estimates and releases the production order.</span></span> <span data-ttu-id="82a51-143">(見積には原材料の引当が含まれており、リリースには倉庫へのリリースが含まれています)。</span><span class="sxs-lookup"><span data-stu-id="82a51-143">(Estimation includes raw material reservation, and the release includes the release to a warehouse.)</span></span>
    2. <span data-ttu-id="82a51-144">倉庫の作業者は、生産ピッキング作業に応じて、保管場所から生産入庫の場所までの原材料のピッキングを開始および完了します。</span><span class="sxs-lookup"><span data-stu-id="82a51-144">A warehouse worker starts and completes raw material picking from the storage location to the production input location, according to the production pick work.</span></span>
    3. <span data-ttu-id="82a51-145">作業現場のオペレーターが製造オーダーを開始します。</span><span class="sxs-lookup"><span data-stu-id="82a51-145">A shop floor operator starts the production order.</span></span>
    4. <span data-ttu-id="82a51-146">最後の工程では、機械オペレーターがモバイル デバイスを使用して製造オーダーを完了済として報告します。</span><span class="sxs-lookup"><span data-stu-id="82a51-146">In the last operation, a machine operator uses the mobile device to report the production order as finished.</span></span>

4. <span data-ttu-id="82a51-147">システムは、設定を使用して 2 つのリンクされた注文のクロスドッキング イベントを識別し、これらのタスクを完了します。</span><span class="sxs-lookup"><span data-stu-id="82a51-147">The system uses the setup to identify the cross-docking event for the two linked orders and then completes these tasks:</span></span>

    1. <span data-ttu-id="82a51-148">関連付けられている販売注文を自動的に倉庫にリリースして出荷を作成します。</span><span class="sxs-lookup"><span data-stu-id="82a51-148">Automatically release the associated sales order to a warehouse to create a shipment.</span></span>
    2. <span data-ttu-id="82a51-149">出荷場所から完成品をピッキングし、クロスドッキング場所ディレクティブが、販売注文に割り当てられている出庫場所にそれらを移動するよう指示するクロスドッキング作業を自動的に作成します。</span><span class="sxs-lookup"><span data-stu-id="82a51-149">Automatically create cross-docking work that has instructions to pick the finished goods from the output location and move them to the outbound location that the cross-docking location directives assigned to the sales order.</span></span>
    3. <span data-ttu-id="82a51-150">製造オーダーが完了済と報告された直後にクロスドッキング作業を完了するように機械オペレーターに指示します。</span><span class="sxs-lookup"><span data-stu-id="82a51-150">Prompt a machine operator to complete the cross-docking work immediately after the production order is reported as finished.</span></span>

5. <span data-ttu-id="82a51-151">クロスドッキング作業が完了し、数量が車両に読み込まれると、出庫倉庫プランナーで販売出荷が確認されます。</span><span class="sxs-lookup"><span data-stu-id="82a51-151">After the cross-docking work is completed, and quantities are loaded onto the vehicle, an outbound warehouse planner confirms the sales shipment.</span></span>

## <a name="example-scenario"></a><span data-ttu-id="82a51-152">シナリオ例</span><span class="sxs-lookup"><span data-stu-id="82a51-152">Example scenario</span></span>

<span data-ttu-id="82a51-153">このシナリオでは、デモ データをインストールして、**USMF** デモ データの会社を使用する必要があります。</span><span class="sxs-lookup"><span data-stu-id="82a51-153">For this scenario, you must have demo data installed, and you must use the **USMF** demo data company.</span></span>

### <a name="set-up-cross-docking-that-uses-the-auto-release-shipment-feature"></a><span data-ttu-id="82a51-154">自動リリース出荷機能を使用するクロスドッキングの設定</span><span class="sxs-lookup"><span data-stu-id="82a51-154">Set up cross-docking that uses the auto-release shipment feature</span></span>

#### <a name="cross-docking-template"></a><span data-ttu-id="82a51-155">クロスドッキング テンプレート</span><span class="sxs-lookup"><span data-stu-id="82a51-155">Cross-docking template</span></span>

1. <span data-ttu-id="82a51-156">**倉庫管理** \> **設定** \> **作業** \> **クロスドッキング テンプレート** の順に移動します。</span><span class="sxs-lookup"><span data-stu-id="82a51-156">Go to **Warehouse management** \> **Setup** \> **Work** \> **Cross docking templates**.</span></span>
2. <span data-ttu-id="82a51-157">**新規** を選択します。</span><span class="sxs-lookup"><span data-stu-id="82a51-157">Select **New**.</span></span>
3. <span data-ttu-id="82a51-158">**シーケンス番号** フィールドに **1** を入力します。</span><span class="sxs-lookup"><span data-stu-id="82a51-158">In the **Sequence number** field, enter **1**.</span></span>
4. <span data-ttu-id="82a51-159">**クロスドッキング テンプレート ID** フィールドに、**XDock\_RAF** などの名前を入力します。</span><span class="sxs-lookup"><span data-stu-id="82a51-159">In the **Cross docking template ID** field, enter a name, such as **XDock\_RAF**.</span></span>
5. <span data-ttu-id="82a51-160">**需要リリース ポリシー** フィールドで、**供給受領時** を選択します。</span><span class="sxs-lookup"><span data-stu-id="82a51-160">In the **Demand release policy** field, select **At supply receipt**.</span></span>
6. <span data-ttu-id="82a51-161">**倉庫** フィールドに、クロスドッキング プロセスを設定する倉庫の番号を入力します。</span><span class="sxs-lookup"><span data-stu-id="82a51-161">In the **Warehouse** field, enter the number of the warehouse where you want to set up the cross-docking process.</span></span> <span data-ttu-id="82a51-162">この例では、**51** を選択します。</span><span class="sxs-lookup"><span data-stu-id="82a51-162">For this example, select **51**.</span></span>

    > [!NOTE]
    > <span data-ttu-id="82a51-163">テンプレートの需要リリース ポリシーとして **供給受領時** を選択すると、ページ上の他のすべてのフィールドが使用できなくなります。</span><span class="sxs-lookup"><span data-stu-id="82a51-163">As soon as you select **At supply receipt** as the demand release policy for the template, all other fields on the page become unavailable.</span></span> <span data-ttu-id="82a51-164">同様に、供給元を定義することはできません。</span><span class="sxs-lookup"><span data-stu-id="82a51-164">Likewise, you can't define any supply sources.</span></span> <span data-ttu-id="82a51-165">この現象は、自動リリース出荷機能を使用するクロスドッキングが、製造オーダーのみを供給元としてサポートし、販売注文と製造オーダーの間にマーキングが存在することを要求するために発生します。</span><span class="sxs-lookup"><span data-stu-id="82a51-165">This behavior occurs because cross-docking that uses the auto-release shipment feature supports only production orders as supply sources, and it requires that a marking exist between sales orders and production orders.</span></span> <span data-ttu-id="82a51-166">需要リリース ポリシーとして **供給受領前** を選択した場合、**計画** および **供給元** タブのフィールドが使用可能になり、編集できるようになります。</span><span class="sxs-lookup"><span data-stu-id="82a51-166">If you select **Before supply receipt** as the demand release policy, the fields on the **Planning** and **Supply sources** tabs are available and can be edited.</span></span>

#### <a name="work-classes"></a><span data-ttu-id="82a51-167">作業クラス</span><span class="sxs-lookup"><span data-stu-id="82a51-167">Work classes</span></span>

1. <span data-ttu-id="82a51-168">**倉庫管理** \> **設定** \> **作業** \> **作業クラス** の順に移動します。</span><span class="sxs-lookup"><span data-stu-id="82a51-168">Go to **Warehouse management** \> **Setup** \> **Work** \> **Work classes**.</span></span>
2. <span data-ttu-id="82a51-169">**新規** を選択します。</span><span class="sxs-lookup"><span data-stu-id="82a51-169">Select **New**.</span></span>
3. <span data-ttu-id="82a51-170">**作業クラス ID** フィールドに、**CrossDock** などの名前を入力します。</span><span class="sxs-lookup"><span data-stu-id="82a51-170">In the **Work class ID** field, enter a name, such as **CrossDock**.</span></span>
4. <span data-ttu-id="82a51-171">**作業指示書タイプ** フィールドで **クロスドッキング** を選択します。</span><span class="sxs-lookup"><span data-stu-id="82a51-171">In the **Work order type** field, select **Cross docking**.</span></span>

<span data-ttu-id="82a51-172">クロスドッキングされた完成品をプットできる場所のタイプを制限するには、有効な場所のタイプを 1 つ以上指定します。</span><span class="sxs-lookup"><span data-stu-id="82a51-172">To limit the types of locations where cross-docked finished goods can be put, you can specify one or more valid location types.</span></span>

#### <a name="work-templates"></a><span data-ttu-id="82a51-173">作業テンプレート</span><span class="sxs-lookup"><span data-stu-id="82a51-173">Work templates</span></span>

1. <span data-ttu-id="82a51-174">**倉庫管理** \> **設定** \> **作業** \> **作業テンプレート** の順に移動します。</span><span class="sxs-lookup"><span data-stu-id="82a51-174">Go to **Warehouse management** \> **Setup** \> **Work** \> **Work templates**.</span></span>
2. <span data-ttu-id="82a51-175">**作業指示書タイプ** フィールドで **クロスドッキング** を選択します。</span><span class="sxs-lookup"><span data-stu-id="82a51-175">In the **Work order type** field, select **Cross docking**.</span></span>
3. <span data-ttu-id="82a51-176">**新規** を選択します。</span><span class="sxs-lookup"><span data-stu-id="82a51-176">Select **New**.</span></span>
4. <span data-ttu-id="82a51-177">**シーケンス番号** フィールドに **1** を入力します。</span><span class="sxs-lookup"><span data-stu-id="82a51-177">In the **Sequence number** field, enter **1**.</span></span>
5. <span data-ttu-id="82a51-178">**作業テンプレート** フィールドに、**CrossDock\_51** などの名前を入力します。</span><span class="sxs-lookup"><span data-stu-id="82a51-178">In the **Work template** field, enter a name, such as **CrossDock\_51**.</span></span>
6. <span data-ttu-id="82a51-179">**保存** を選択します。</span><span class="sxs-lookup"><span data-stu-id="82a51-179">Select **Save**.</span></span>
7. <span data-ttu-id="82a51-180">**作業テンプレートの詳細** セクションで、**新規** を選択します。</span><span class="sxs-lookup"><span data-stu-id="82a51-180">In the **Work Template Details** section, select **New**.</span></span>
8. <span data-ttu-id="82a51-181">新しい行の **作業タイプ** フィールドで、**ピッキング** を選択します。</span><span class="sxs-lookup"><span data-stu-id="82a51-181">For the new line, in the **Work type** field, select **Pick**.</span></span> <span data-ttu-id="82a51-182">**作業クラス ID** フィールドで **CrossDock** を選択します。</span><span class="sxs-lookup"><span data-stu-id="82a51-182">In the **Work class ID** field, select **CrossDock**.</span></span>
9. <span data-ttu-id="82a51-183">**新規** を選択します。</span><span class="sxs-lookup"><span data-stu-id="82a51-183">Select **New**.</span></span>
10. <span data-ttu-id="82a51-184">新しい行の **作業タイプ** フィールドで、**プット** を選択します。</span><span class="sxs-lookup"><span data-stu-id="82a51-184">For the new line, in the **Work type** field, select **Put**.</span></span> <span data-ttu-id="82a51-185">**作業クラス ID** フィールドで **CrossDock** を選択します。</span><span class="sxs-lookup"><span data-stu-id="82a51-185">In the **Work class ID** field, select **CrossDock**.</span></span>

#### <a name="location-directives"></a><span data-ttu-id="82a51-186">場所のディレクティブ</span><span class="sxs-lookup"><span data-stu-id="82a51-186">Location directives</span></span>

<span data-ttu-id="82a51-187">完成品の標準のプット アウェイのプロセスでは、ピッキング済の生産数量の通常の保管スペースへの移動をガイドする **プット** 場所ディレクティブが必要です。</span><span class="sxs-lookup"><span data-stu-id="82a51-187">A standard put-away process for finished goods requires a **Put** location directive to guide the movement of picked production quantities to a regular storage space.</span></span> <span data-ttu-id="82a51-188">同様に、クロスドッキング **プット** 場所ディレクティブを設定して、関連する販売注文の出荷を処理する指定された出庫場所に完了済数量をプットするように作業に指示する必要があります。</span><span class="sxs-lookup"><span data-stu-id="82a51-188">Likewise, you must set up a cross-docking **Put** location directive to instruct the work to put the finished quantity in a designated outbound location that services the shipment of the associated sales order.</span></span>

<span data-ttu-id="82a51-189">クロスドッキングの場合、完成品の通常のプット アウェイに関しては、出荷場所が指定されているため、ピッキング作業アクションの場所ディレクティブを作成する必要はありません。</span><span class="sxs-lookup"><span data-stu-id="82a51-189">For cross-docking, as for regular put-away of finished goods, you don't have to create a location directive for the pick work action, because the output location is given.</span></span> <span data-ttu-id="82a51-190">さらに、この出荷場所は、リソース関連レコードの既定の出荷場所 (つまり、リソース、リソース グループの関係、またはリソース グループ) として、または倉庫の既定の生産完成品の場所として設定する必要があります。</span><span class="sxs-lookup"><span data-stu-id="82a51-190">Additionally, this output location is expected to be set up either as the default output location on one of the resource-related records (that is, the resource, resource group relation, or resource group) or as a default production finished goods location for a warehouse.</span></span>

1. <span data-ttu-id="82a51-191">**倉庫管理** \> **設定** \> **場所ディレクティブ** の順に移動します。</span><span class="sxs-lookup"><span data-stu-id="82a51-191">Go to **Warehouse management** \> **Setup** \> **Location directives**.</span></span>
2. <span data-ttu-id="82a51-192">**作業指示書タイプ** フィールドで **クロスドッキング** を選択します。</span><span class="sxs-lookup"><span data-stu-id="82a51-192">In the **Work order type** field, select **Cross docking**.</span></span>
3. <span data-ttu-id="82a51-193">**新規** を選択します。</span><span class="sxs-lookup"><span data-stu-id="82a51-193">Select **New**.</span></span>
4. <span data-ttu-id="82a51-194">**シーケンス番号** フィールドに **1** を入力します。</span><span class="sxs-lookup"><span data-stu-id="82a51-194">In the **Sequence number** field, enter **1**.</span></span>
5. <span data-ttu-id="82a51-195">**名前** フィールドに、**Baydoor** のような名前を入力します。</span><span class="sxs-lookup"><span data-stu-id="82a51-195">In the **Name** field, enter a name, such as **Baydoor**.</span></span>
6. <span data-ttu-id="82a51-196">**作業タイプ** フィールドで **プット** を選択します。</span><span class="sxs-lookup"><span data-stu-id="82a51-196">In the **Work type** field, select **Put**.</span></span>
7. <span data-ttu-id="82a51-197">**サイト** フィールドで、**5** を選択します。</span><span class="sxs-lookup"><span data-stu-id="82a51-197">In the **Site** field, select **5**.</span></span>
8. <span data-ttu-id="82a51-198">**倉庫** フィールドで、**51** を選択します。</span><span class="sxs-lookup"><span data-stu-id="82a51-198">In the **Warehouse** field, select **51**.</span></span>
9. <span data-ttu-id="82a51-199">**明細行** クイック タブで、**新規** を選択します。</span><span class="sxs-lookup"><span data-stu-id="82a51-199">On the **Lines** FastTab, select **New**.</span></span>
10. <span data-ttu-id="82a51-200">**上限数量** フィールドに、範囲の最大数量 (**1000000** など) を入力します。</span><span class="sxs-lookup"><span data-stu-id="82a51-200">In the **To quantity** field, enter the maximum quantity of the range, such as **1000000**.</span></span>
11. <span data-ttu-id="82a51-201">**保存** を選択します。</span><span class="sxs-lookup"><span data-stu-id="82a51-201">Select **Save**.</span></span>
12. <span data-ttu-id="82a51-202">**場所ディレクティブ アクション** クイック タブで、**新規** を選択します。</span><span class="sxs-lookup"><span data-stu-id="82a51-202">On the **Location Directives Actions** FastTab, select **New**.</span></span>
13. <span data-ttu-id="82a51-203">**名前** フィールドに、**Baydoor** のような名前を入力します。</span><span class="sxs-lookup"><span data-stu-id="82a51-203">In the **Name** field, enter a name, such as **Baydoor**.</span></span>
14. <span data-ttu-id="82a51-204">**保存** を選択します。</span><span class="sxs-lookup"><span data-stu-id="82a51-204">Select **Save**.</span></span>
15. <span data-ttu-id="82a51-205">標準クエリ機能を使用すると、1 つ以上の特定の場所にプット場所を制限することができます。</span><span class="sxs-lookup"><span data-stu-id="82a51-205">You can use the standard query facility to limit put locations to one or more specific locations.</span></span> <span data-ttu-id="82a51-206"> **クエリの編集** を選択してから、**場所** テーブルの **倉庫** フィールドの基準として **51** を選択します。</span><span class="sxs-lookup"><span data-stu-id="82a51-206">Select **Edit query**, and select **51** as the criterion for the **Warehouse** field in the **Locations** table.</span></span>

### <a name="cross-dock-finished-goods-to-the-outbound-location"></a><span data-ttu-id="82a51-207">出庫場所への完成品のクロスドッキング</span><span class="sxs-lookup"><span data-stu-id="82a51-207">Cross-dock finished goods to the outbound location</span></span>

<span data-ttu-id="82a51-208">完成品の数量を、関連付けられている販売注文の出庫場所にクロスドッキングするには、次の手順に従います。</span><span class="sxs-lookup"><span data-stu-id="82a51-208">To cross-dock the quantity of finished goods to the outbound location of the associated sales order, follow these steps.</span></span>

1. <span data-ttu-id="82a51-209">**販売とマーケティング** \> **販売注文** \> **すべての販売注文** の順に移動します。</span><span class="sxs-lookup"><span data-stu-id="82a51-209">Go to **Sales and marketing** \> **Sales orders** \> **All sales orders**.</span></span>
2. <span data-ttu-id="82a51-210">**新規** を選択します。</span><span class="sxs-lookup"><span data-stu-id="82a51-210">Select **New**.</span></span>
3. <span data-ttu-id="82a51-211">販売注文ヘッダーでは、顧客 ID **US-001** および自動リリース出荷機能を使用するクロスドッキング用に設定されている倉庫を選択します。</span><span class="sxs-lookup"><span data-stu-id="82a51-211">For the sales order header, select customer account **US-001** and a warehouse that is set up for cross-docking that uses the auto-release shipment feature.</span></span>
4. <span data-ttu-id="82a51-212">完成品の明細行を追加し、数量として **10** を入力します。</span><span class="sxs-lookup"><span data-stu-id="82a51-212">Add a line for a finished product, and enter **10** as the quantity.</span></span>
5. <span data-ttu-id="82a51-213">**販売注文明細行** セクションで、**製品と供給** \> **製造オーダー** を選択します。</span><span class="sxs-lookup"><span data-stu-id="82a51-213">In the **Sales order lines** section, select **Product and supply** \> **Production order**.</span></span>
6. <span data-ttu-id="82a51-214">**製造オーダーの作成** ダイアログ ボックスで既定値を確認し、**作成** を選択します。</span><span class="sxs-lookup"><span data-stu-id="82a51-214">In the **Create production order** dialog box, review the default values, and then select **Create**.</span></span> <span data-ttu-id="82a51-215">新しい製造オーダーが作成され、販売注文にリンクされます (つまり、引当およびマークされます)。</span><span class="sxs-lookup"><span data-stu-id="82a51-215">A new production order is created and linked to the sales order (that is, it's reserved and marked).</span></span>
7. <span data-ttu-id="82a51-216">オプション: **数量** フィールドの値を変更して、販売注文のフルフィルメントに必要な値を超えないようにします。</span><span class="sxs-lookup"><span data-stu-id="82a51-216">Optional: Change the value of the **Quantity** field so that it's more than the value that is required to fulfill the sales order.</span></span> <span data-ttu-id="82a51-217">生産数量が完了済として報告されると、完成品をプット アウェイするための通常の手順に従って、システムによってマーク済の数量に対してクロスドッキング作業および残りの数量に対してプット アウェイ作業が作成されます。</span><span class="sxs-lookup"><span data-stu-id="82a51-217">When the production quantity is reported as finished, the system will create cross-docking work for the marked quantity and put-away work for the remaining quantity, according to the regular procedure for handling the put-away of finished goods.</span></span>

    <span data-ttu-id="82a51-218">既述のように、販売注文と製造オーダーの間にマーキングが必要です。</span><span class="sxs-lookup"><span data-stu-id="82a51-218">As was mentioned earlier, a marking must exist between the sales order and the production order.</span></span> <span data-ttu-id="82a51-219">そうでない場合、クロスドッキングは機能しません。</span><span class="sxs-lookup"><span data-stu-id="82a51-219">Otherwise, the cross-docking won't work.</span></span> <span data-ttu-id="82a51-220">マーキングは、複数の方法で作成できます。</span><span class="sxs-lookup"><span data-stu-id="82a51-220">A marking can be created in the multiple ways:</span></span>

    - <span data-ttu-id="82a51-221">システムは、次のような状況でマーキングを自動的に作成できます。</span><span class="sxs-lookup"><span data-stu-id="82a51-221">The system can automatically create the marking in the following situations:</span></span>

        - <span data-ttu-id="82a51-222">製造オーダーが販売注文明細行から手動で直接作成されます (ステップ 6 を参照してください)。</span><span class="sxs-lookup"><span data-stu-id="82a51-222">The production order is manually created directly from the sales order line (see step 6).</span></span>
        - <span data-ttu-id="82a51-223">計画製造オーダーが確定され、**マーキングの更新** フィールドが **標準** に設定されます。</span><span class="sxs-lookup"><span data-stu-id="82a51-223">Planned production orders are firmed, and the **Update marking** field is set to **Standard**.</span></span>

    - <span data-ttu-id="82a51-224">ユーザーは、需要オーダー明細行から **マーキング** ページを開くことで、手動でマーキングを作成できます。</span><span class="sxs-lookup"><span data-stu-id="82a51-224">The user can manually create the marking by opening the **Marking** page from the demand order line.</span></span>

    > [!NOTE]
    > <span data-ttu-id="82a51-225">標準および加重平均を在庫モデルとして使用するように設定されている品目に対して、マーキングを手動で作成することはできません。</span><span class="sxs-lookup"><span data-stu-id="82a51-225">A marking can't be manually created for items that are set up to use standard and weighted average as inventory models.</span></span>

8. <span data-ttu-id="82a51-226">**製造オーダー** ページのアクション ウィンドウの **製造オーダー** タブの、**プロセス** グループで **見積** を選択してから、**OK** を選択します。</span><span class="sxs-lookup"><span data-stu-id="82a51-226">On the **Production order** page, on the Action Pane, on the **Production order** tab, in the **Process** group, select **Estimate**, and then select **OK**.</span></span> <span data-ttu-id="82a51-227">オーダーが見積され、原材料の数量が生産に対して引当されます。</span><span class="sxs-lookup"><span data-stu-id="82a51-227">The order is estimated, and the raw material quantity is reserved for the production.</span></span>
9. <span data-ttu-id="82a51-228">アクション ウィンドウの **製造オーダー** タブの **プロセス** グループで、**リリース** を選択してから、**OK** を選択します。</span><span class="sxs-lookup"><span data-stu-id="82a51-228">On the Action Pane, on the **Production order** tab, in the **Process** group, select **Release**, and then select **OK**.</span></span> <span data-ttu-id="82a51-229">原材料に対して倉庫ピッキング作業が作成されます。</span><span class="sxs-lookup"><span data-stu-id="82a51-229">Warehouse pick work is created for the raw materials.</span></span>
10. <span data-ttu-id="82a51-230">作業を開いて確認します。</span><span class="sxs-lookup"><span data-stu-id="82a51-230">Open and review the work.</span></span> <span data-ttu-id="82a51-231">アクション ウィンドウの **倉庫** タブの、**一般** グループで、**作業詳細** を選択します。</span><span class="sxs-lookup"><span data-stu-id="82a51-231">On the Action Pane, on the **Warehouse** tab, in the **General** group, select **Work details**.</span></span> <span data-ttu-id="82a51-232">作業 ID をメモします。</span><span class="sxs-lookup"><span data-stu-id="82a51-232">Make a note of the work ID.</span></span>
11. <span data-ttu-id="82a51-233">倉庫 51 で作業を実行するには、倉庫アプリを開いてサインインします。</span><span class="sxs-lookup"><span data-stu-id="82a51-233">Sign in to the warehouse app to run work in warehouse 51.</span></span>
12. <span data-ttu-id="82a51-234">**生産** \> **生産ピッキング** の順に移動します。</span><span class="sxs-lookup"><span data-stu-id="82a51-234">Go to **Production** \> **Production pick**.</span></span>
13. <span data-ttu-id="82a51-235">作業 ID を入力して、原材料ピッキングを開始および完了します。</span><span class="sxs-lookup"><span data-stu-id="82a51-235">Enter the work ID to start and complete the raw material picking.</span></span> 

    <span data-ttu-id="82a51-236">作業が完了済として報告されると、原材料の数量が生産入庫の場所 (USMF データで **005**) で使用可能になり、製造オーダーの実行を開始できるようになります。</span><span class="sxs-lookup"><span data-stu-id="82a51-236">After the work is reported as finished, the quantity of raw materials is available in the production input location (**005** in USMF demo data), and execution of the production order can start.</span></span>

14. <span data-ttu-id="82a51-237">**製造オーダー** ページのアクション ウィンドウの **製造オーダー** タブの、**プロセス** グループで、**開始** を選択してから、**OK** を選択します。</span><span class="sxs-lookup"><span data-stu-id="82a51-237">On the **Production order** page, on the Action Pane, on the **Production order** tab, in the **Process** group, select **Start**, and then select **OK**.</span></span>
15. <span data-ttu-id="82a51-238">アプリで、**生産** \> **RAF およびプット アウェイ** の順に移動します。</span><span class="sxs-lookup"><span data-stu-id="82a51-238">In the app, go to **Production** \> **RAF and put away**.</span></span>
16. <span data-ttu-id="82a51-239">**製品 ID** フィールドに、製造オーダー番号およびその他の必須の詳細を入力して、**OK** を選択します。</span><span class="sxs-lookup"><span data-stu-id="82a51-239">In the **Prod ID** field, enter the production order number and other mandatory details, and then select **OK**.</span></span>

<span data-ttu-id="82a51-240">次のイベントが発生することにご注意ください。</span><span class="sxs-lookup"><span data-stu-id="82a51-240">Notice that the following events occur:</span></span>

- <span data-ttu-id="82a51-241">リンクされた販売注文に対して、倉庫にリリースが発生します。</span><span class="sxs-lookup"><span data-stu-id="82a51-241">The release to a warehouse is triggered for the linked sales order.</span></span>
- <span data-ttu-id="82a51-242">リリースに基づいて、出荷とクロスドッキングの作業が作成されます。</span><span class="sxs-lookup"><span data-stu-id="82a51-242">Based on the release, shipment and cross-docking work is created.</span></span> <span data-ttu-id="82a51-243">この作業では、倉庫オペレーターに対して、販売注文明細行をフルフィルメントするために必要な数量をピッキングし、クロスドッキング場所ディレクティブで指定された出庫場所にプットするように指示します。</span><span class="sxs-lookup"><span data-stu-id="82a51-243">This work instructs the warehouse operator to pick the quantities that are required to fulfill the sales order line and put them in the outbound location that specified in the cross-docking location directive.</span></span>
- <span data-ttu-id="82a51-244">製造オーダーの数量が販売注文で要求される数量を超える場合は、通常のプット アウェイ作業が作成されます。</span><span class="sxs-lookup"><span data-stu-id="82a51-244">If the production order quantity is more than the quantity that is required by the sales order, regular put-away work is created.</span></span> <span data-ttu-id="82a51-245">この作業では、場所ディレクティブに従って、クロスドッキング後に残っている完成品の数量をピッキングし、通常の保管場所に移動するよう倉庫オペレーターに指示します。</span><span class="sxs-lookup"><span data-stu-id="82a51-245">This work instructs the warehouse operator to pick the quantity of finished goods that remains after cross-docking and move it to regular storage, according to the location directive.</span></span>
