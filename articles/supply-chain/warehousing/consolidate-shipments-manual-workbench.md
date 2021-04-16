---
title: 出荷連結ワークベンチを使用して出荷を連結する
description: このトピックでは、複数の注文が倉庫にリリースされ、出荷連結ワークベンチを使用して出荷に連結するシナリオを示します。
author: GarmMSFT
ms.date: 05/12/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: WHSShipConsolidationPolicy, WHSShipConsolidationWorkbench, WHSShipConsolidationSetShipment
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: kamaybac
ms.search.validFrom: 2020-05-01
ms.dyn365.ops.version: 10.0.6
ms.openlocfilehash: 29dd403ce2378beb6f4ba71a0b3c0836eed7566a
ms.sourcegitcommit: 0e8db169c3f90bd750826af76709ef5d621fd377
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/01/2021
ms.locfileid: "5838421"
---
# <a name="consolidate-shipments-by-using-the-shipment-consolidation-workbench"></a><span data-ttu-id="97985-103">出荷連結ワークベンチを使用して出荷を連結する</span><span class="sxs-lookup"><span data-stu-id="97985-103">Consolidate shipments by using the shipment consolidation workbench</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="97985-104">このトピックでは、複数の注文が倉庫にリリースされ、出荷連結ワークベンチを使用して出荷に連結するシナリオを示します。</span><span class="sxs-lookup"><span data-stu-id="97985-104">This topic presents a scenario where multiple orders are released to the warehouse and then consolidated into shipments later by using the shipment consolidation workbench.</span></span>

## <a name="make-demo-data-available"></a><span data-ttu-id="97985-105">デモ データを有効化する</span><span class="sxs-lookup"><span data-stu-id="97985-105">Make demo data available</span></span>

<span data-ttu-id="97985-106">このトピックのシナリオでは、Microsoft Dynamics 365 Supply Chain Management にて用意されている標準のデモデータに含まれる値とレコードを参照し ます。</span><span class="sxs-lookup"><span data-stu-id="97985-106">The scenario in this topic references values and records that are included in the standard demo data that is provided for Microsoft Dynamics 365 Supply Chain Management.</span></span> <span data-ttu-id="97985-107">ここで提供されている値を使用するには、デモデータがインストールされている環境で作業し、開始する前に法人を **usmf** に設定します。</span><span class="sxs-lookup"><span data-stu-id="97985-107">If you want to use the values that are provided here as you do the exercises, be sure to work in an environment where the demo data is installed, and set the legal entity to **USMF** before you begin.</span></span>

## <a name="set-up-shipment-consolidation-policies-and-product-filters"></a><span data-ttu-id="97985-108">出荷連結ポリシーおよび製品フィルタの設定</span><span class="sxs-lookup"><span data-stu-id="97985-108">Set up shipment consolidation policies and product filters</span></span>

<span data-ttu-id="97985-109">このシナリオでは、既にこの機能を有効にし、[出荷連結ポリシーの構成](configure-shipment-consolidation-policies.md)内の実習を完了しており、同ページ内に記述されているポリシーとその他のレコードを作成していることを前提としています。</span><span class="sxs-lookup"><span data-stu-id="97985-109">The scenario that is described here assumes that you've already turned on the feature, done the exercises in [Configure shipment consolidation policies](configure-shipment-consolidation-policies.md), and created the policies and other records that are described there.</span></span> <span data-ttu-id="97985-110">このシナリオを続行する前に、この演習を行っている必要があります。</span><span class="sxs-lookup"><span data-stu-id="97985-110">Be sure to do those exercises before you continue with this scenario.</span></span>

## <a name="turn-on-the-manual-shipment-consolidation-feature"></a><span data-ttu-id="97985-111">手動での出荷連結機能を有効化する</span><span class="sxs-lookup"><span data-stu-id="97985-111">Turn on the manual shipment consolidation feature</span></span>

<span data-ttu-id="97985-112">*手動出荷連結* 機能を使用する前に 、システムでこの機能を有効にしておく必要があります。</span><span class="sxs-lookup"><span data-stu-id="97985-112">Before you can use the *Manual shipment consolidation* feature, you must turn it on in your system.</span></span> <span data-ttu-id="97985-113">管理者は、[機能管理](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) 設定を使用して、機能の状態を確認し、有効にすることができます。</span><span class="sxs-lookup"><span data-stu-id="97985-113">Admins can use the [feature management](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) settings to check the status of the feature and turn it on.</span></span> <span data-ttu-id="97985-114">**機能管理** ワークスペースで、この機能は次のようにリストされています。</span><span class="sxs-lookup"><span data-stu-id="97985-114">In the **Feature management** workspace, the feature is listed in the following way:</span></span>

- <span data-ttu-id="97985-115">**モジュール:** *倉庫管理*</span><span class="sxs-lookup"><span data-stu-id="97985-115">**Module:** *Warehouse management*</span></span>
- <span data-ttu-id="97985-116">**機能名:** *手動出荷連結*</span><span class="sxs-lookup"><span data-stu-id="97985-116">**Feature name:** *Manual shipment consolidation*</span></span>

<span data-ttu-id="97985-117">[出荷連結ポリシーの構成](configure-shipment-consolidation-policies.md)に記載されているように、ポリシーを作成する前に *出荷の連結* 機能を有効にしておく必要があります。</span><span class="sxs-lookup"><span data-stu-id="97985-117">As was mentioned in [Configure shipment consolidation policies](configure-shipment-consolidation-policies.md), you must also turn on the *Consolidate shipment* feature before you can create policies.</span></span> <span data-ttu-id="97985-118">この手順は既に完了している前提で進めます。</span><span class="sxs-lookup"><span data-stu-id="97985-118">However, you should already have completed that step.</span></span>

## <a name="create-the-sales-orders-for-this-scenario"></a><span data-ttu-id="97985-119">このシナリオで使用する販売注文の作成</span><span class="sxs-lookup"><span data-stu-id="97985-119">Create the sales orders for this scenario</span></span>

<span data-ttu-id="97985-120">シナリオで使用する一連の販売注文を作成することから始めます。</span><span class="sxs-lookup"><span data-stu-id="97985-120">Start by creating a collection of sales orders that you can work with.</span></span> <span data-ttu-id="97985-121">高度な倉庫 (WMS) プロセスが利用できる倉庫を使用する必要があります。</span><span class="sxs-lookup"><span data-stu-id="97985-121">You must work with a warehouse that is enabled for advanced warehouse (WMS) processes.</span></span> <span data-ttu-id="97985-122">他の倉庫を明示的に指定していない場合は、次の注文セットのそれぞれに対して同じ倉庫が使用されなければなりません。</span><span class="sxs-lookup"><span data-stu-id="97985-122">Unless a different warehouse is explicitly mentioned, that same warehouse must be used for each of the following sets of orders.</span></span>

<span data-ttu-id="97985-123">**売掛金勘定  \> 注文 \> すべての販売注文** に移動し、次のサブセクションで説明されている設定を含む販売注文のコレクションを作成します。</span><span class="sxs-lookup"><span data-stu-id="97985-123">Go to **Accounts receivable \> Orders \> All sales orders**, and create a collection of sales orders that have the settings that are described in the following subsections.</span></span>

### <a name="create-order-set-1"></a><span data-ttu-id="97985-124">注文セット 1 を作成する</span><span class="sxs-lookup"><span data-stu-id="97985-124">Create order set 1</span></span>

#### <a name="sales-orders-1-1-and-1-2"></a><span data-ttu-id="97985-125">販売注文 1-1 と 1-2</span><span class="sxs-lookup"><span data-stu-id="97985-125">Sales orders 1-1 and 1-2</span></span>

1. <span data-ttu-id="97985-126">以下の設定で 2 つの同一の販売注文を作成します:</span><span class="sxs-lookup"><span data-stu-id="97985-126">Create two identical sales orders that have the following settings:</span></span>

    - <span data-ttu-id="97985-127">**顧客アカウント:** *US-001*</span><span class="sxs-lookup"><span data-stu-id="97985-127">**Customer account:** *US-001*</span></span>
    - <span data-ttu-id="97985-128">**荷渡方法:** *Airwa-Air*</span><span class="sxs-lookup"><span data-stu-id="97985-128">**Mode of delivery:** *Airwa-Air*</span></span>

1. <span data-ttu-id="97985-129">以下の設定で注文明細行を追加します:</span><span class="sxs-lookup"><span data-stu-id="97985-129">Add an order line that has the following settings:</span></span>

    - <span data-ttu-id="97985-130">**品目番号 :** *A0001* (**コード 4** フィルタが割り当てられていない品目)</span><span class="sxs-lookup"><span data-stu-id="97985-130">**Item number:** *A0001* (an item that no **Code 4** filter is assigned to)</span></span>
    - <span data-ttu-id="97985-131">**数量:** *1.00*</span><span class="sxs-lookup"><span data-stu-id="97985-131">**Quantity:** *1.00*</span></span>

1. <span data-ttu-id="97985-132">**在庫 \> 引当** を選択し、アクションウ ィンドウで **ロットの引当** を選択して、注文明細行を引当します。</span><span class="sxs-lookup"><span data-stu-id="97985-132">Select **Inventory \> Reservation**, and then, on the Action Pane, select **Reserve lot** to reserve the order line.</span></span>

#### <a name="sales-order-1-3"></a><span data-ttu-id="97985-133">販売注文 1-3</span><span class="sxs-lookup"><span data-stu-id="97985-133">Sales order 1-3</span></span>

1. <span data-ttu-id="97985-134">以下の設定で販売注文を作成します:</span><span class="sxs-lookup"><span data-stu-id="97985-134">Create a sales order that has the following settings:</span></span>

    - <span data-ttu-id="97985-135">**顧客アカウント:** *US-001*</span><span class="sxs-lookup"><span data-stu-id="97985-135">**Customer account:** *US-001*</span></span>
    - <span data-ttu-id="97985-136">**荷渡方法:** *10*</span><span class="sxs-lookup"><span data-stu-id="97985-136">**Mode of delivery:** *10*</span></span>

1. <span data-ttu-id="97985-137">以下の設定で注文明細行を追加します:</span><span class="sxs-lookup"><span data-stu-id="97985-137">Add an order line that has the following settings:</span></span>

    - <span data-ttu-id="97985-138">**品目番号 :** *A0001* (**コード 4** フィルタが割り当てられていない品目)</span><span class="sxs-lookup"><span data-stu-id="97985-138">**Item number:** *A0001* (an item that no **Code 4** filter is assigned to)</span></span>
    - <span data-ttu-id="97985-139">**数量:** *1.00*</span><span class="sxs-lookup"><span data-stu-id="97985-139">**Quantity:** *1.00*</span></span>

1. <span data-ttu-id="97985-140">**在庫 \> 引当** を選択し、アクションウ ィンドウで **ロットの引当** を選択して、注文明細行を引当します。</span><span class="sxs-lookup"><span data-stu-id="97985-140">Select **Inventory \> Reservation**, and then, on the Action Pane, select **Reserve lot** to reserve the order line.</span></span>
1. <span data-ttu-id="97985-141">以下の設定で 2 つ目の販売注文を作成します:</span><span class="sxs-lookup"><span data-stu-id="97985-141">Add a second order line that has the following settings:</span></span>

    - <span data-ttu-id="97985-142">**品目番号 :** *A0002* ( **コード 4** フィルタが割り当てられていない品目)</span><span class="sxs-lookup"><span data-stu-id="97985-142">**Item number:** *A0002* (an item that no **Code 4** filter is assigned to)</span></span>
    - <span data-ttu-id="97985-143">**数量:** *1.00*</span><span class="sxs-lookup"><span data-stu-id="97985-143">**Quantity:** *1.00*</span></span>
    - <span data-ttu-id="97985-144">**荷渡方法:** *Airwa-Air*</span><span class="sxs-lookup"><span data-stu-id="97985-144">**Mode of delivery:** *Airwa-Air*</span></span>

1. <span data-ttu-id="97985-145">**在庫 \> 引当** を選択し、アクションウ ィンドウで **ロットの引当** を選択して、2 つ目の注文明細行を引当します。</span><span class="sxs-lookup"><span data-stu-id="97985-145">Select **Inventory \> Reservation**, and then, on the Action Pane, select **Reserve lot** to reserve the second order line.</span></span>

### <a name="create-order-set-2"></a><span data-ttu-id="97985-146">注文セット 2 を作成する</span><span class="sxs-lookup"><span data-stu-id="97985-146">Create order set 2</span></span>

#### <a name="sales-orders-2-1-and-2-2"></a><span data-ttu-id="97985-147">販売注文 2-1 と 2-2</span><span class="sxs-lookup"><span data-stu-id="97985-147">Sales orders 2-1 and 2-2</span></span>

1. <span data-ttu-id="97985-148">以下の設定で 2 つの同一の販売注文を作成します:</span><span class="sxs-lookup"><span data-stu-id="97985-148">Create two identical sales orders that have the following settings:</span></span>

    - <span data-ttu-id="97985-149">**顧客アカウント:** *US-002*</span><span class="sxs-lookup"><span data-stu-id="97985-149">**Customer account:** *US-002*</span></span>
    - <span data-ttu-id="97985-150">**荷渡方法:** *Airwa-Air*</span><span class="sxs-lookup"><span data-stu-id="97985-150">**Mode of delivery:** *Airwa-Air*</span></span>

1. <span data-ttu-id="97985-151">以下の設定で注文明細行を追加します:</span><span class="sxs-lookup"><span data-stu-id="97985-151">Add an order line that has the following settings:</span></span>

    - <span data-ttu-id="97985-152">**品目番号 :** *M9200* (**コード 4** のフィルタが *可燃性* に設定されている品目)</span><span class="sxs-lookup"><span data-stu-id="97985-152">**Item number:** *M9200* (an item where the **Code 4** filter is set to *Flammable*)</span></span>
    - <span data-ttu-id="97985-153">**数量:** *1.00*</span><span class="sxs-lookup"><span data-stu-id="97985-153">**Quantity:** *1.00*</span></span>

1. <span data-ttu-id="97985-154">**在庫 \> 引当** を選択し、アクションウ ィンドウで **ロットの引当** を選択して、注文明細行を引当します。</span><span class="sxs-lookup"><span data-stu-id="97985-154">Select **Inventory \> Reservation**, and then, on the Action Pane, select **Reserve lot** to reserve the order line.</span></span>
1. <span data-ttu-id="97985-155">以下の設定で 2 つ目の販売注文を作成します:</span><span class="sxs-lookup"><span data-stu-id="97985-155">Add a second order line that has the following settings:</span></span>

    - <span data-ttu-id="97985-156">**品目番号 :** *M9201*( **コード 4** のフィルタが *爆発物* に設定されている品目)</span><span class="sxs-lookup"><span data-stu-id="97985-156">**Item number:** *M9201* (an item where the **Code 4** filter is set to *Explosive*)</span></span>
    - <span data-ttu-id="97985-157">**数量:** *1.00*</span><span class="sxs-lookup"><span data-stu-id="97985-157">**Quantity:** *1.00*</span></span>
    - <span data-ttu-id="97985-158">**荷渡方法:** *Airwa-Air*</span><span class="sxs-lookup"><span data-stu-id="97985-158">**Mode of delivery:** *Airwa-Air*</span></span>

1. <span data-ttu-id="97985-159">**在庫 \> 引当** を選択し、アクションウ ィンドウで **ロットの引当** を選択して、2 つ目の注文明細行を引当します。</span><span class="sxs-lookup"><span data-stu-id="97985-159">Select **Inventory \> Reservation**, and then, on the Action Pane, select **Reserve lot** to reserve the second order line.</span></span>

### <a name="create-order-set-3"></a><span data-ttu-id="97985-160">注文セット 3 を作成する</span><span class="sxs-lookup"><span data-stu-id="97985-160">Create order set 3</span></span>

#### <a name="sales-orders-3-1-and-3-2"></a><span data-ttu-id="97985-161">販売注文 3-1 と 3-2</span><span class="sxs-lookup"><span data-stu-id="97985-161">Sales orders 3-1 and 3-2</span></span>

1. <span data-ttu-id="97985-162">以下の設定で 2 つの同一の販売注文を作成します:</span><span class="sxs-lookup"><span data-stu-id="97985-162">Create two identical sales orders that have the following settings:</span></span>

    - <span data-ttu-id="97985-163">**顧客アカウント:** *US-001*</span><span class="sxs-lookup"><span data-stu-id="97985-163">**Customer account:** *US-001*</span></span>
    - <span data-ttu-id="97985-164">**顧客の要求:** *1*</span><span class="sxs-lookup"><span data-stu-id="97985-164">**Customer requisition:** *1*</span></span>

1. <span data-ttu-id="97985-165">以下の設定で注文明細行を追加します:</span><span class="sxs-lookup"><span data-stu-id="97985-165">Add an order line that has the following settings:</span></span>

    - <span data-ttu-id="97985-166">**品目番号 :** *A0001* (**コード 4** フィルタが割り当てられていない品目)</span><span class="sxs-lookup"><span data-stu-id="97985-166">**Item number:** *A0001* (an item that no **Code 4** filter is assigned to)</span></span>
    - <span data-ttu-id="97985-167">**数量:** *1.00*</span><span class="sxs-lookup"><span data-stu-id="97985-167">**Quantity:** *1.00*</span></span>

1. <span data-ttu-id="97985-168">**在庫 \> 引当** を選択し、アクションウ ィンドウで **ロットの引当** を選択して、注文明細行を引当します。</span><span class="sxs-lookup"><span data-stu-id="97985-168">Select **Inventory \> Reservation**, and then, on the Action Pane, select **Reserve lot** to reserve the order line.</span></span>

#### <a name="sales-orders-3-3-and-3-4"></a><span data-ttu-id="97985-169">販売注文 3-3 と 3-4</span><span class="sxs-lookup"><span data-stu-id="97985-169">Sales orders 3-3 and 3-4</span></span>

1. <span data-ttu-id="97985-170">以下の設定で 2 つの同一の販売注文を作成します:</span><span class="sxs-lookup"><span data-stu-id="97985-170">Create two identical sales orders that have the following settings:</span></span>

    - <span data-ttu-id="97985-171">**顧客アカウント:** *US-001*</span><span class="sxs-lookup"><span data-stu-id="97985-171">**Customer account:** *US-001*</span></span>
    - <span data-ttu-id="97985-172">**顧客の要求:** *2*</span><span class="sxs-lookup"><span data-stu-id="97985-172">**Customer requisition:** *2*</span></span>

1. <span data-ttu-id="97985-173">以下の設定で注文明細行を追加します:</span><span class="sxs-lookup"><span data-stu-id="97985-173">Add an order line that has the following settings:</span></span>

    - <span data-ttu-id="97985-174">**品目番号 :** *A0001* (**コード 4** フィルタが割り当てられていない品目)</span><span class="sxs-lookup"><span data-stu-id="97985-174">**Item number:** *A0001* (an item that no **Code 4** filter is assigned to)</span></span>
    - <span data-ttu-id="97985-175">**数量:** *1.00*</span><span class="sxs-lookup"><span data-stu-id="97985-175">**Quantity:** *1.00*</span></span>

1. <span data-ttu-id="97985-176">**在庫 \> 引当** を選択し、アクションウ ィンドウで **ロットの引当** を選択して、注文明細行を引当します。</span><span class="sxs-lookup"><span data-stu-id="97985-176">Select **Inventory \> Reservation**, and then, on the Action Pane, select **Reserve lot** to reserve the order line.</span></span>

### <a name="create-order-set-4"></a><span data-ttu-id="97985-177">注文セット 4 を作成する</span><span class="sxs-lookup"><span data-stu-id="97985-177">Create order set 4</span></span>

#### <a name="sales-orders-4-1-and-4-2"></a><span data-ttu-id="97985-178">販売注文 4-1 と 4-2</span><span class="sxs-lookup"><span data-stu-id="97985-178">Sales orders 4-1 and 4-2</span></span>

1. <span data-ttu-id="97985-179">以下の設定で 2 つの同一の販売注文を作成します:</span><span class="sxs-lookup"><span data-stu-id="97985-179">Create two identical sales orders that have the following settings:</span></span>

    - <span data-ttu-id="97985-180">**顧客アカウント:** *US-003*</span><span class="sxs-lookup"><span data-stu-id="97985-180">**Customer account:** *US-003*</span></span>

1. <span data-ttu-id="97985-181">以下の設定で注文明細行を追加します:</span><span class="sxs-lookup"><span data-stu-id="97985-181">Add an order line that has the following settings:</span></span>

    - <span data-ttu-id="97985-182">**品目番号 :** *A0001* (**コード 4** フィルタが割り当てられていない品目)</span><span class="sxs-lookup"><span data-stu-id="97985-182">**Item number:** *A0001* (an item that no **Code 4** filter is assigned to)</span></span>
    - <span data-ttu-id="97985-183">**数量:** *1.00*</span><span class="sxs-lookup"><span data-stu-id="97985-183">**Quantity:** *1.00*</span></span>

1. <span data-ttu-id="97985-184">**在庫 \> 引当** を選択し、アクションウ ィンドウで **ロットの引当** を選択して、注文明細行を引当します。</span><span class="sxs-lookup"><span data-stu-id="97985-184">Select **Inventory \> Reservation**, and then, on the Action Pane, select **Reserve lot** to reserve the order line.</span></span>

#### <a name="sales-orders-4-3-and-4-4"></a><span data-ttu-id="97985-185">販売注文 4-3 と 4-4</span><span class="sxs-lookup"><span data-stu-id="97985-185">Sales orders 4-3 and 4-4</span></span>

1. <span data-ttu-id="97985-186">以下の設定で 2 つの同一の販売注文を作成します:</span><span class="sxs-lookup"><span data-stu-id="97985-186">Create two identical sales orders that have the following settings:</span></span>

    - <span data-ttu-id="97985-187">**顧客アカウント:** *US-004*</span><span class="sxs-lookup"><span data-stu-id="97985-187">**Customer account:** *US-004*</span></span>

1. <span data-ttu-id="97985-188">以下の設定で注文明細行を追加します:</span><span class="sxs-lookup"><span data-stu-id="97985-188">Add an order line that has the following settings:</span></span>

    - <span data-ttu-id="97985-189">**品目番号 :** *A0001* (**コード 4** フィルタが割り当てられていない品目)</span><span class="sxs-lookup"><span data-stu-id="97985-189">**Item number:** *A0001* (an item that no **Code 4** filter is assigned to)</span></span>
    - <span data-ttu-id="97985-190">**数量:** *1.00*</span><span class="sxs-lookup"><span data-stu-id="97985-190">**Quantity:** *1.00*</span></span>

1. <span data-ttu-id="97985-191">**在庫 \> 引当** を選択し、アクションウ ィンドウで **ロットの引当** を選択して、注文明細行を引当します。</span><span class="sxs-lookup"><span data-stu-id="97985-191">Select **Inventory \> Reservation**, and then, on the Action Pane, select **Reserve lot** to reserve the order line.</span></span>

#### <a name="sales-orders-4-5-and-4-6"></a><span data-ttu-id="97985-192">販売注文 4-5 と 4-6</span><span class="sxs-lookup"><span data-stu-id="97985-192">Sales orders 4-5 and 4-6</span></span>

1. <span data-ttu-id="97985-193">以下の設定で 2 つの同一の販売注文を作成します:</span><span class="sxs-lookup"><span data-stu-id="97985-193">Create two identical sales orders that have the following settings:</span></span>

    - <span data-ttu-id="97985-194">**顧客アカウント:** *US-007*</span><span class="sxs-lookup"><span data-stu-id="97985-194">**Customer account:** *US-007*</span></span>
    - <span data-ttu-id="97985-195">**サイト:** *6*</span><span class="sxs-lookup"><span data-stu-id="97985-195">**Site:** *6*</span></span>
    - <span data-ttu-id="97985-196">**倉庫:** *61*</span><span class="sxs-lookup"><span data-stu-id="97985-196">**Warehouse:** *61*</span></span>
    - <span data-ttu-id="97985-197">**プール :** *ShipCons*</span><span class="sxs-lookup"><span data-stu-id="97985-197">**Pool:** *ShipCons*</span></span>

1. <span data-ttu-id="97985-198">以下の設定で注文明細行を追加します:</span><span class="sxs-lookup"><span data-stu-id="97985-198">Add an order line that has the following settings:</span></span>

    - <span data-ttu-id="97985-199">**品目番号 :** *A0001* (**コード 4** フィルタが割り当てられていない品目)</span><span class="sxs-lookup"><span data-stu-id="97985-199">**Item number:** *A0001* (an item that no **Code 4** filter is assigned to)</span></span>
    - <span data-ttu-id="97985-200">**数量:** *1.00*</span><span class="sxs-lookup"><span data-stu-id="97985-200">**Quantity:** *1.00*</span></span>

1. <span data-ttu-id="97985-201">**在庫 \> 引当** を選択し、アクションウ ィンドウで **ロットの引当** を選択して、注文明細行を引当します。</span><span class="sxs-lookup"><span data-stu-id="97985-201">Select **Inventory \> Reservation**, and then, on the Action Pane, select **Reserve lot** to reserve the order line.</span></span>

#### <a name="sales-orders-4-7-and-4-8"></a><span data-ttu-id="97985-202">販売注文 4-7 と 4-8</span><span class="sxs-lookup"><span data-stu-id="97985-202">Sales orders 4-7 and 4-8</span></span>

1. <span data-ttu-id="97985-203">以下の設定で 2 つの同一の販売注文を作成します:</span><span class="sxs-lookup"><span data-stu-id="97985-203">Create two identical sales orders that have the following settings:</span></span>

    - <span data-ttu-id="97985-204">**顧客アカウント:** *US-007*</span><span class="sxs-lookup"><span data-stu-id="97985-204">**Customer account:** *US-007*</span></span>
    - <span data-ttu-id="97985-205">**サイト:** *6*</span><span class="sxs-lookup"><span data-stu-id="97985-205">**Site:** *6*</span></span>
    - <span data-ttu-id="97985-206">**倉庫:** *61*</span><span class="sxs-lookup"><span data-stu-id="97985-206">**Warehouse:** *61*</span></span>
    - <span data-ttu-id="97985-207">**プール :** このフィールドは空白のままにします。</span><span class="sxs-lookup"><span data-stu-id="97985-207">**Pool:** Leave this field blank.</span></span>

1. <span data-ttu-id="97985-208">以下の設定で注文明細行を追加します:</span><span class="sxs-lookup"><span data-stu-id="97985-208">Add an order line that has the following settings:</span></span>

    - <span data-ttu-id="97985-209">**品目番号 :** *A0001* (**コード 4** フィルタが割り当てられていない品目)</span><span class="sxs-lookup"><span data-stu-id="97985-209">**Item number:** *A0001* (an item that no **Code 4** filter is assigned to)</span></span>
    - <span data-ttu-id="97985-210">**数量:** *1.00*</span><span class="sxs-lookup"><span data-stu-id="97985-210">**Quantity:** *1.00*</span></span>

1. <span data-ttu-id="97985-211">**在庫 \> 引当** を選択し、アクションウ ィンドウで **ロットの引当** を選択して、注文明細行を引当します。</span><span class="sxs-lookup"><span data-stu-id="97985-211">Select **Inventory \> Reservation**, and then, on the Action Pane, select **Reserve lot** to reserve the order line.</span></span>

## <a name="release-the-orders-to-the-warehouse"></a><span data-ttu-id="97985-212">注文を倉庫にリリースする</span><span class="sxs-lookup"><span data-stu-id="97985-212">Release the orders to the warehouse</span></span>

<span data-ttu-id="97985-213">このシナリオで作成した各販売注文のリリースをするには、次の手順に従ってください。</span><span class="sxs-lookup"><span data-stu-id="97985-213">Follow these steps to release each sales order that you created for this scenario to the warehouse.</span></span>

1. <span data-ttu-id="97985-214">**売掛金勘定 \> 注文 \> すべての販売注文** に移動します。</span><span class="sxs-lookup"><span data-stu-id="97985-214">Go to **Accounts receivable \> Orders \> All sales orders**.</span></span>
1. <span data-ttu-id="97985-215">リリースする販売注文を検索して選択します。</span><span class="sxs-lookup"><span data-stu-id="97985-215">Find and select the sales order to release.</span></span>
1. <span data-ttu-id="97985-216">アクション ウィンドウの、**倉庫** タブにて、**アクション\> 倉庫へのリリース** を選択して、選択された販売注文をリリースします。</span><span class="sxs-lookup"><span data-stu-id="97985-216">On the Action Pane, on the **Warehouse** tab, select **Actions \> Release to warehouse** to release the selected sales order.</span></span>
1. <span data-ttu-id="97985-217">このシナリオで作成したそれぞれの販売注文に対して、この手順を繰り返します。</span><span class="sxs-lookup"><span data-stu-id="97985-217">Repeat this procedure for every other sales order that you created for this scenario.</span></span>

## <a name="consolidate-the-shipments-by-using-the-shipment-consolidation-workbench"></a><span data-ttu-id="97985-218">出荷連結ワークベンチを使用して出荷を連結する</span><span class="sxs-lookup"><span data-stu-id="97985-218">Consolidate the shipments by using the shipment consolidation workbench</span></span>

1. <span data-ttu-id="97985-219">**倉庫管理 \> 倉庫へのリリース \> 出荷統合ワークベンチ** に移動します。</span><span class="sxs-lookup"><span data-stu-id="97985-219">Go to **Warehouse management \> Release to warehouse \> Shipment consolidation workbench**.</span></span>
1. <span data-ttu-id="97985-220">アクション ウィンドウで、**クエリの編集** を選択します。</span><span class="sxs-lookup"><span data-stu-id="97985-220">On the Action Pane, select **Edit query**.</span></span>
1. <span data-ttu-id="97985-221">[クエリの編集] ダイアログ ボックスの **範囲** タブで、**追加** を選択して、グリッドに次の設定を持つ行を追加します:</span><span class="sxs-lookup"><span data-stu-id="97985-221">In the query editor dialog box, on the **Range** tab, select **Add** to add a row that has the following settings to the grid:</span></span>

    - <span data-ttu-id="97985-222">**テーブル:** *販売注文*</span><span class="sxs-lookup"><span data-stu-id="97985-222">**Table:** *Sales orders*</span></span>
    - <span data-ttu-id="97985-223">**フィールド:** *販売注文*</span><span class="sxs-lookup"><span data-stu-id="97985-223">**Field:** *Sales order*</span></span>
    - <span data-ttu-id="97985-224">**基準:** このシナリオで作成した各注文セットの販売注文番号をコンマで区切った一覧を入力します。</span><span class="sxs-lookup"><span data-stu-id="97985-224">**Criteria:** Enter a comma-separated list of the sales order numbers for each order set that you created for this scenario.</span></span>

1. <span data-ttu-id="97985-225">**OK** を選択してクエリを保存し、ダイアログ ボックスを閉じます。</span><span class="sxs-lookup"><span data-stu-id="97985-225">Select **OK** to save your query and close the dialog box.</span></span>
1. <span data-ttu-id="97985-226">アクション ウィンドウで、**出荷の連結** を選択します。</span><span class="sxs-lookup"><span data-stu-id="97985-226">On the Action Pane, select **Consolidate shipments**.</span></span>
1. <span data-ttu-id="97985-227">すべての出荷を選択し、アクション ウィンドウで **連結** をを選択します。</span><span class="sxs-lookup"><span data-stu-id="97985-227">Select all the shipments, and then, on the Action Pane, select **Consolidate**.</span></span>

## <a name="verify-the-shipments"></a><span data-ttu-id="97985-228">出荷の確認</span><span class="sxs-lookup"><span data-stu-id="97985-228">Verify the shipments</span></span>

<span data-ttu-id="97985-229">次の手順では、出荷連結の結果として作成、更新された出荷を確認できます。</span><span class="sxs-lookup"><span data-stu-id="97985-229">The following procedure lets you verify the shipments that have been created or updated as a result of shipment consolidation.</span></span> <span data-ttu-id="97985-230">これを使用して、このシナリオで作成した各注文セットを確認します。続いてその結果が得られるかどうかを確認するには、次のセクションを確認します。</span><span class="sxs-lookup"><span data-stu-id="97985-230">Use it to review each order set that you created for this scenario, and then review the subsections that follow to make sure that you've obtained the expected results.</span></span>

1. <span data-ttu-id="97985-231">**倉庫管理 \> 出荷 \> すべての出荷** に移動します。</span><span class="sxs-lookup"><span data-stu-id="97985-231">Go to **Warehouse management \> Shipments \> All shipments**.</span></span>
1. <span data-ttu-id="97985-232">必要な出荷を検索して選択します。</span><span class="sxs-lookup"><span data-stu-id="97985-232">Find and select the required shipment.</span></span>
1. <span data-ttu-id="97985-233">出荷の作成時または更新時に連結ポリシーが使用されていた場合は、**出荷連結ポリシー** フィールドに表示する必要があります。</span><span class="sxs-lookup"><span data-stu-id="97985-233">If a consolidation policy was used when the shipment was created or updated, you should see it in the **Shipment consolidation policy** field.</span></span>

### <a name="related-shipments-for-order-set-1"></a><span data-ttu-id="97985-234">注文セット 1 に関連する出荷</span><span class="sxs-lookup"><span data-stu-id="97985-234">Related shipments for order set 1</span></span>

<span data-ttu-id="97985-235">次の 2 つの出荷が作成されている必要があります:</span><span class="sxs-lookup"><span data-stu-id="97985-235">Two shipments should have been created:</span></span>

- <span data-ttu-id="97985-236">最初の出荷は、*顧客モード* の出荷連結ポリシーを使用して作成された 3 つの行で構成されます。</span><span class="sxs-lookup"><span data-stu-id="97985-236">The first shipment contains three lines and was created by using the *CustomerMode* shipment consolidation policy.</span></span>
- <span data-ttu-id="97985-237">2 つ目の出荷は、*航空運賃* 輸送モードの荷渡方法を使用しないもので、顧客注文の *CustomerOrderNo* 連結ポリシーを使用して作成されてい ます。</span><span class="sxs-lookup"><span data-stu-id="97985-237">The second shipment, which doesn't use the *Airways* transportation mode of delivery, was created by using the *CustomerOrderNo* shipment consolidation policy.</span></span>

### <a name="related-shipments-for-order-set-2"></a><span data-ttu-id="97985-238">注文セット 2 に関連する出荷</span><span class="sxs-lookup"><span data-stu-id="97985-238">Related shipments for order set 2</span></span>

<span data-ttu-id="97985-239">次の 3 つの出荷が作成されている必要があります:</span><span class="sxs-lookup"><span data-stu-id="97985-239">Three shipments should have been created:</span></span>

- <span data-ttu-id="97985-240">最初の出荷には、 *可燃性* の品目が含まれています。</span><span class="sxs-lookup"><span data-stu-id="97985-240">The first shipment contains *Flammable* items.</span></span>
- <span data-ttu-id="97985-241">他の 2 つの出荷には、*爆発性* の品目を含む 1 つの行が含まれてい ます。</span><span class="sxs-lookup"><span data-stu-id="97985-241">Each of the other two shipments contains one line that has the *Explosive* item.</span></span>

### <a name="related-shipments-for-order-set-3"></a><span data-ttu-id="97985-242">注文セット 3 に関連する出荷</span><span class="sxs-lookup"><span data-stu-id="97985-242">Related shipments for order set 3</span></span>

<span data-ttu-id="97985-243">次の 2 つの出荷が作成されている必要があります:</span><span class="sxs-lookup"><span data-stu-id="97985-243">Two shipments should have been created:</span></span>

- <span data-ttu-id="97985-244">1つ目の出荷には、**顧客要求** フィールドが *1* に設定されている販売注文の注文明細行が含まれます。</span><span class="sxs-lookup"><span data-stu-id="97985-244">The first shipment contains order lines from the sales order where the **Customer requisition** field is set to *1*.</span></span>
- <span data-ttu-id="97985-245">2つ目の出荷には、**顧客要求** フィールドが *2* に設定されている販売注文の注文明細行が含まれます。</span><span class="sxs-lookup"><span data-stu-id="97985-245">The second shipment contains order lines from sales order where the **Customer requisition** field is set to *2*.</span></span>

### <a name="related-shipments-for-order-set-4"></a><span data-ttu-id="97985-246">注文セット 4 に関連する出荷</span><span class="sxs-lookup"><span data-stu-id="97985-246">Related shipments for order set 4</span></span>

<span data-ttu-id="97985-247">次の 4 つの出荷が作成されている必要があります:</span><span class="sxs-lookup"><span data-stu-id="97985-247">Four shipments should have been created:</span></span>

- <span data-ttu-id="97985-248">顧客アカウント *US-003* の 2 件の販売注文の明細行は、*注文プール* の出荷連結ポリシーを使用して 1 つの出荷にグループ化されています。</span><span class="sxs-lookup"><span data-stu-id="97985-248">Lines from two orders for customer *US-003* were grouped into one shipment by using the *Order pool* shipment consolidation policy.</span></span>
- <span data-ttu-id="97985-249">顧客アカウント *US-004* の 2 件の販売注文の明細行は、*注文プール* の出荷連結ポリシーを使用して 1 つの出荷にグループ化されています。</span><span class="sxs-lookup"><span data-stu-id="97985-249">Lines from two orders for customer *US-004* were grouped into one shipment by using the *Order pool* shipment consolidation policy.</span></span>
- <span data-ttu-id="97985-250">顧客 *007* の販売注文 4-5 および 4-6 の明細行は、*注文プール* の出荷連結ポリシーを使用して1つの出荷にグループ化されています。</span><span class="sxs-lookup"><span data-stu-id="97985-250">Lines from sales orders 4-5 and 4-6 for customer *US-007* were grouped into one shipment by using the *Order pool* shipment consolidation policy.</span></span>
- <span data-ttu-id="97985-251">顧客 *007* の販売注文 4-7 および 4-8 の明細行は、*クロスオーダー* の出荷連結ポリシーを使用して1つの出荷にグループ化されています。</span><span class="sxs-lookup"><span data-stu-id="97985-251">Lines from sales orders 4-7 and 4-8 for customer *US-007* were grouped into one shipment by using the *CrossOrder* shipment consolidation policy.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="97985-252">追加リソース</span><span class="sxs-lookup"><span data-stu-id="97985-252">Additional resources</span></span>

- [<span data-ttu-id="97985-253">出荷連結ポリシー</span><span class="sxs-lookup"><span data-stu-id="97985-253">Shipment consolidation policies</span></span>](about-shipment-consolidation-policies.md)
- [<span data-ttu-id="97985-254">出荷連結ポリシーを構成する</span><span class="sxs-lookup"><span data-stu-id="97985-254">Configure shipment consolidation policies</span></span>](configure-shipment-consolidation-policies.md)


[!INCLUDE[footer-include](../../includes/footer-banner.md)]