---
title: 積荷計画ワークベンチから倉庫にリリースすることで出荷を連結する
description: このトピックでは、複数の注文が同一の積荷で倉庫にリリースされ、自動的に出荷に連結されるシナリオを示します。
author: GarmMSFT
ms.date: 05/12/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: WHSShipConsolidationPolicy, WHSShipConsolidationWorkbench
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: kamaybac
ms.search.validFrom: 2020-05-01
ms.dyn365.ops.version: 10.0.3
ms.openlocfilehash: 30824bf1c8e84bab08b6885ee812ed5e3e9937bb
ms.sourcegitcommit: 53b797ff1b524f581046b48cdde42f50b37495bc
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 05/28/2021
ms.locfileid: "6117184"
---
# <a name="consolidate-shipments-by-releasing-to-warehouse-from-the-load-planning-workbench"></a><span data-ttu-id="250d4-103">積荷計画ワークベンチから倉庫にリリースすることで出荷を連結する</span><span class="sxs-lookup"><span data-stu-id="250d4-103">Consolidate shipments by releasing to warehouse from the load planning workbench</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="250d4-104">このトピックでは、複数の注文が同一の積荷で倉庫にリリースされ、自動的に出荷に連結されるシナリオを示します。</span><span class="sxs-lookup"><span data-stu-id="250d4-104">This topic presents a scenario where multiple orders are released to the warehouse in the same load and are then automatically consolidated into shipments.</span></span>

## <a name="make-demo-data-available"></a><span data-ttu-id="250d4-105">デモ データを有効化する</span><span class="sxs-lookup"><span data-stu-id="250d4-105">Make demo data available</span></span>

<span data-ttu-id="250d4-106">このトピックのシナリオでは、Microsoft Dynamics 365 Supply Chain Management にて用意されている標準のデモデータに含まれる値とレコードを参照し ます。</span><span class="sxs-lookup"><span data-stu-id="250d4-106">The scenario in this topic references values and records that are included in the standard demo data that is provided for Microsoft Dynamics 365 Supply Chain Management.</span></span> <span data-ttu-id="250d4-107">ここで提供されている値を使用するには、デモデータがインストールされている環境で作業し、開始する前に法人を **usmf** に設定します。</span><span class="sxs-lookup"><span data-stu-id="250d4-107">If you want to use the values that are provided here as you do the exercises, be sure to work in an environment where the demo data is installed, and set the legal entity to **USMF** before you begin.</span></span>

## <a name="set-up-shipment-consolidation-policies-and-product-filters"></a><span data-ttu-id="250d4-108">出荷連結ポリシーおよび製品フィルタの設定</span><span class="sxs-lookup"><span data-stu-id="250d4-108">Set up shipment consolidation policies and product filters</span></span>

<span data-ttu-id="250d4-109">このシナリオでは、既にこの機能を有効にし、[出荷連結ポリシーの構成](configure-shipment-consolidation-policies.md)内の実習を完了しており、同ページ内に記述されているポリシーとその他のレコードを作成していることを前提としています。</span><span class="sxs-lookup"><span data-stu-id="250d4-109">The scenario that is described here assumes that you've already turned on the feature, done the exercises in [Configure shipment consolidation policies](configure-shipment-consolidation-policies.md), and created the policies and other records that are described there.</span></span> <span data-ttu-id="250d4-110">このシナリオを続行する前に、この演習を行っている必要があります。</span><span class="sxs-lookup"><span data-stu-id="250d4-110">Be sure to do those exercises before you continue with this scenario.</span></span>

## <a name="create-the-sales-orders-for-this-scenario"></a><span data-ttu-id="250d4-111">このシナリオで使用する販売注文の作成</span><span class="sxs-lookup"><span data-stu-id="250d4-111">Create the sales orders for this scenario</span></span>

<span data-ttu-id="250d4-112">シナリオで使用する一連の販売注文を作成することから始めます。</span><span class="sxs-lookup"><span data-stu-id="250d4-112">Start by creating a collection of sales orders that you can work with.</span></span> <span data-ttu-id="250d4-113">高度な倉庫 (WMS) プロセスが利用できる倉庫を使用する必要があります。</span><span class="sxs-lookup"><span data-stu-id="250d4-113">You must work with a warehouse that is enabled for advanced warehouse (WMS) processes.</span></span> <span data-ttu-id="250d4-114">他の倉庫を明示的に指定していない場合は、次の注文セットのそれぞれに対して同じ倉庫が使用されなければなりません。</span><span class="sxs-lookup"><span data-stu-id="250d4-114">Unless a different warehouse is explicitly mentioned, that same warehouse must be used for each of the following sets of orders.</span></span>

<span data-ttu-id="250d4-115">**売掛金勘定  \> 注文 \> すべての販売注文** に移動し、次のサブセクションで説明されている設定を含む販売注文のコレクションを作成します。</span><span class="sxs-lookup"><span data-stu-id="250d4-115">Go to **Accounts receivable \> Orders \> All sales orders**, and create a collection of sales orders that have the settings that are described in the following subsections.</span></span>

### <a name="create-order-set-1"></a><span data-ttu-id="250d4-116">注文セット 1 を作成する</span><span class="sxs-lookup"><span data-stu-id="250d4-116">Create order set 1</span></span>

#### <a name="sales-order-1-1"></a><span data-ttu-id="250d4-117">販売注文 1-1</span><span class="sxs-lookup"><span data-stu-id="250d4-117">Sales order 1-1</span></span>

1. <span data-ttu-id="250d4-118">以下の設定で販売注文を作成します:</span><span class="sxs-lookup"><span data-stu-id="250d4-118">Create a sales order that has the following settings:</span></span>

    - <span data-ttu-id="250d4-119">**顧客アカウント:** *US-001*</span><span class="sxs-lookup"><span data-stu-id="250d4-119">**Customer account:** *US-001*</span></span>
    - <span data-ttu-id="250d4-120">**荷渡方法:** *Airwa-Air*</span><span class="sxs-lookup"><span data-stu-id="250d4-120">**Mode of delivery:** *Airwa-Air*</span></span>

1. <span data-ttu-id="250d4-121">以下の設定で注文明細行を追加します:</span><span class="sxs-lookup"><span data-stu-id="250d4-121">Add an order line that has the following settings:</span></span>

    - <span data-ttu-id="250d4-122">**品目番号 :** *A0001* (**コード 4** フィルタが割り当てられていない品目)</span><span class="sxs-lookup"><span data-stu-id="250d4-122">**Item number:** *A0001* (an item that no **Code 4** filter is assigned to)</span></span>
    - <span data-ttu-id="250d4-123">**数量:** *1.00*</span><span class="sxs-lookup"><span data-stu-id="250d4-123">**Quantity:** *1.00*</span></span>

1. <span data-ttu-id="250d4-124">**在庫 \> 引当** を選択し、アクションウ ィンドウで **ロットの引当** を選択して、注文明細行を引当します。</span><span class="sxs-lookup"><span data-stu-id="250d4-124">Select **Inventory \> Reservation**, and then, on the Action Pane, select **Reserve lot** to reserve the order line.</span></span>

#### <a name="sales-order-1-2"></a><span data-ttu-id="250d4-125">販売注文 1-2</span><span class="sxs-lookup"><span data-stu-id="250d4-125">Sales order 1-2</span></span>

1. <span data-ttu-id="250d4-126">以下の設定で販売注文を作成します:</span><span class="sxs-lookup"><span data-stu-id="250d4-126">Create a sales order that has the following settings:</span></span>

    - <span data-ttu-id="250d4-127">**顧客アカウント:** *US-001*</span><span class="sxs-lookup"><span data-stu-id="250d4-127">**Customer account:** *US-001*</span></span>
    - <span data-ttu-id="250d4-128">**荷渡方法:** *Airwa-Air*</span><span class="sxs-lookup"><span data-stu-id="250d4-128">**Mode of delivery:** *Airwa-Air*</span></span>

1. <span data-ttu-id="250d4-129">以下の設定で注文明細行を追加します:</span><span class="sxs-lookup"><span data-stu-id="250d4-129">Add an order line that has the following settings:</span></span>

    - <span data-ttu-id="250d4-130">**品目番号 :** *A0001* (**コード 4** フィルタが割り当てられていない品目)</span><span class="sxs-lookup"><span data-stu-id="250d4-130">**Item number:** *A0001* (an item that no **Code 4** filter is assigned to)</span></span>
    - <span data-ttu-id="250d4-131">**数量:** *1.00*</span><span class="sxs-lookup"><span data-stu-id="250d4-131">**Quantity:** *1.00*</span></span>

1. <span data-ttu-id="250d4-132">**在庫 \> 引当** を選択し、アクションウ ィンドウで **ロットの引当** を選択して、注文明細行を引当します。</span><span class="sxs-lookup"><span data-stu-id="250d4-132">Select **Inventory \> Reservation**, and then, on the Action Pane, select **Reserve lot** to reserve the order line.</span></span>

#### <a name="sales-order-1-3"></a><span data-ttu-id="250d4-133">販売注文 1-3</span><span class="sxs-lookup"><span data-stu-id="250d4-133">Sales order 1-3</span></span>

1. <span data-ttu-id="250d4-134">以下の設定で販売注文を作成します:</span><span class="sxs-lookup"><span data-stu-id="250d4-134">Create a sales order that has the following settings:</span></span>

    - <span data-ttu-id="250d4-135">**顧客アカウント:** *US-001*</span><span class="sxs-lookup"><span data-stu-id="250d4-135">**Customer account:** *US-001*</span></span>
    - <span data-ttu-id="250d4-136">**荷渡方法:** *10*</span><span class="sxs-lookup"><span data-stu-id="250d4-136">**Mode of delivery:** *10*</span></span>

1. <span data-ttu-id="250d4-137">以下の設定で注文明細行を追加します:</span><span class="sxs-lookup"><span data-stu-id="250d4-137">Add an order line that has the following settings:</span></span>

    - <span data-ttu-id="250d4-138">**品目番号 :** *A0001* (**コード 4** フィルタが割り当てられていない品目)</span><span class="sxs-lookup"><span data-stu-id="250d4-138">**Item number:** *A0001* (an item that no **Code 4** filter is assigned to)</span></span>
    - <span data-ttu-id="250d4-139">**数量:** *1.00*</span><span class="sxs-lookup"><span data-stu-id="250d4-139">**Quantity:** *1.00*</span></span>

1. <span data-ttu-id="250d4-140">**在庫 \> 引当** を選択し、アクションウ ィンドウで **ロットの引当** を選択して、注文明細行を引当します。</span><span class="sxs-lookup"><span data-stu-id="250d4-140">Select **Inventory \> Reservation**, and then, on the Action Pane, select **Reserve lot** to reserve the order line.</span></span>
1. <span data-ttu-id="250d4-141">以下の設定で 2 つ目の販売注文を作成します:</span><span class="sxs-lookup"><span data-stu-id="250d4-141">Add a second order line that has the following settings:</span></span>

    - <span data-ttu-id="250d4-142">**品目番号 :** *A0002* ( **コード 4** フィルタが割り当てられていない品目)</span><span class="sxs-lookup"><span data-stu-id="250d4-142">**Item number:** *A0002* (an item that no **Code 4** filter is assigned to)</span></span>
    - <span data-ttu-id="250d4-143">**数量:** *1.00*</span><span class="sxs-lookup"><span data-stu-id="250d4-143">**Quantity:** *1.00*</span></span>
    - <span data-ttu-id="250d4-144">**荷渡方法:** *Airwa-Air*</span><span class="sxs-lookup"><span data-stu-id="250d4-144">**Mode of delivery:** *Airwa-Air*</span></span>

1. <span data-ttu-id="250d4-145">**在庫 \> 引当** を選択し、アクションウ ィンドウで **ロットの引当** を選択して、2 つ目の注文明細行を引当します。</span><span class="sxs-lookup"><span data-stu-id="250d4-145">Select **Inventory \> Reservation**, and then, on the Action Pane, select **Reserve lot** to reserve the second order line.</span></span>

### <a name="create-order-set-2"></a><span data-ttu-id="250d4-146">注文セット 2 を作成する</span><span class="sxs-lookup"><span data-stu-id="250d4-146">Create order set 2</span></span>

#### <a name="sales-orders-2-1-and-2-2"></a><span data-ttu-id="250d4-147">販売注文 2-1 と 2-2</span><span class="sxs-lookup"><span data-stu-id="250d4-147">Sales orders 2-1 and 2-2</span></span>

1. <span data-ttu-id="250d4-148">以下の設定で 2 つの同一の販売注文を作成します:</span><span class="sxs-lookup"><span data-stu-id="250d4-148">Create two identical sales orders that have the following settings:</span></span>

    - <span data-ttu-id="250d4-149">**顧客アカウント:** *US-002*</span><span class="sxs-lookup"><span data-stu-id="250d4-149">**Customer account:** *US-002*</span></span>

1. <span data-ttu-id="250d4-150">以下の設定で注文明細行を追加します:</span><span class="sxs-lookup"><span data-stu-id="250d4-150">Add an order line that has the following settings:</span></span>

    - <span data-ttu-id="250d4-151">**品目番号 :** *M9200* (**コード 4** のフィルタが *可燃性* に設定されている品目)</span><span class="sxs-lookup"><span data-stu-id="250d4-151">**Item number:** *M9200* (an item where the **Code 4** filter is set to *Flammable*)</span></span>
    - <span data-ttu-id="250d4-152">**数量:** *1.00*</span><span class="sxs-lookup"><span data-stu-id="250d4-152">**Quantity:** *1.00*</span></span>

1. <span data-ttu-id="250d4-153">**在庫 \> 引当** を選択し、アクションウ ィンドウで **ロットの引当** を選択して、注文明細行を引当します。</span><span class="sxs-lookup"><span data-stu-id="250d4-153">Select **Inventory \> Reservation**, and then, on the Action Pane, select **Reserve lot** to reserve the order line.</span></span>
1. <span data-ttu-id="250d4-154">以下の設定で 2 つ目の販売注文を作成します:</span><span class="sxs-lookup"><span data-stu-id="250d4-154">Add a second order line that has the following settings:</span></span>

    - <span data-ttu-id="250d4-155">**品目番号 :** *M9201*( **コード 4** のフィルタが *爆発物* に設定されている品目)</span><span class="sxs-lookup"><span data-stu-id="250d4-155">**Item number:** *M9201* (an item where the **Code 4** filter is set to *Explosive*)</span></span>
    - <span data-ttu-id="250d4-156">**数量:** *1.00*</span><span class="sxs-lookup"><span data-stu-id="250d4-156">**Quantity:** *1.00*</span></span>
    - <span data-ttu-id="250d4-157">**荷渡方法:** *Airwa-Air*</span><span class="sxs-lookup"><span data-stu-id="250d4-157">**Mode of delivery:** *Airwa-Air*</span></span>

1. <span data-ttu-id="250d4-158">**在庫 \> 引当** を選択し、アクションウ ィンドウで **ロットの引当** を選択して、2 つ目の注文明細行を引当します。</span><span class="sxs-lookup"><span data-stu-id="250d4-158">Select **Inventory \> Reservation**, and then, on the Action Pane, select **Reserve lot** to reserve the second order line.</span></span>

### <a name="create-order-set-3"></a><span data-ttu-id="250d4-159">注文セット 3 を作成する</span><span class="sxs-lookup"><span data-stu-id="250d4-159">Create order set 3</span></span>

#### <a name="sales-orders-3-1-and-3-2"></a><span data-ttu-id="250d4-160">販売注文 3-1 と 3-2</span><span class="sxs-lookup"><span data-stu-id="250d4-160">Sales orders 3-1 and 3-2</span></span>

1. <span data-ttu-id="250d4-161">以下の設定で 2 つの同一の販売注文を作成します:</span><span class="sxs-lookup"><span data-stu-id="250d4-161">Create two identical sales orders that have the following settings:</span></span>

    - <span data-ttu-id="250d4-162">**顧客アカウント:** *US-001*</span><span class="sxs-lookup"><span data-stu-id="250d4-162">**Customer account:** *US-001*</span></span>
    - <span data-ttu-id="250d4-163">**顧客の要求:** *1*</span><span class="sxs-lookup"><span data-stu-id="250d4-163">**Customer requisition:** *1*</span></span>

1. <span data-ttu-id="250d4-164">以下の設定で注文明細行を追加します:</span><span class="sxs-lookup"><span data-stu-id="250d4-164">Add an order line that has the following settings:</span></span>

    - <span data-ttu-id="250d4-165">**品目番号 :** *A0001* (**コード 4** フィルタが割り当てられていない品目)</span><span class="sxs-lookup"><span data-stu-id="250d4-165">**Item number:** *A0001* (an item that no **Code 4** filter is assigned to)</span></span>
    - <span data-ttu-id="250d4-166">**数量:** *1.00*</span><span class="sxs-lookup"><span data-stu-id="250d4-166">**Quantity:** *1.00*</span></span>

1. <span data-ttu-id="250d4-167">**在庫 \> 引当** を選択し、アクションウ ィンドウで **ロットの引当** を選択して、注文明細行を引当します。</span><span class="sxs-lookup"><span data-stu-id="250d4-167">Select **Inventory \> Reservation**, and then, on the Action Pane, select **Reserve lot** to reserve the order line.</span></span>

#### <a name="sales-orders-3-3-and-3-4"></a><span data-ttu-id="250d4-168">販売注文 3-3 と 3-4</span><span class="sxs-lookup"><span data-stu-id="250d4-168">Sales orders 3-3 and 3-4</span></span>

1. <span data-ttu-id="250d4-169">以下の設定で 2 つの同一の販売注文を作成します:</span><span class="sxs-lookup"><span data-stu-id="250d4-169">Create two identical sales orders that have the following settings:</span></span>

    - <span data-ttu-id="250d4-170">**顧客アカウント:** *US-001*</span><span class="sxs-lookup"><span data-stu-id="250d4-170">**Customer account:** *US-001*</span></span>
    - <span data-ttu-id="250d4-171">**顧客の要求:** *2*</span><span class="sxs-lookup"><span data-stu-id="250d4-171">**Customer requisition:** *2*</span></span>

1. <span data-ttu-id="250d4-172">以下の設定で注文明細行を追加します:</span><span class="sxs-lookup"><span data-stu-id="250d4-172">Add an order line that has the following settings:</span></span>

    - <span data-ttu-id="250d4-173">**品目番号 :** *A0001* (**コード 4** フィルタが割り当てられていない品目)</span><span class="sxs-lookup"><span data-stu-id="250d4-173">**Item number:** *A0001* (an item that no **Code 4** filter is assigned to)</span></span>
    - <span data-ttu-id="250d4-174">**数量:** *1.00*</span><span class="sxs-lookup"><span data-stu-id="250d4-174">**Quantity:** *1.00*</span></span>

1. <span data-ttu-id="250d4-175">**在庫 \> 引当** を選択し、アクションウ ィンドウで **ロットの引当** を選択して、注文明細行を引当します。</span><span class="sxs-lookup"><span data-stu-id="250d4-175">Select **Inventory \> Reservation**, and then, on the Action Pane, select **Reserve lot** to reserve the order line.</span></span>

### <a name="create-order-set-4"></a><span data-ttu-id="250d4-176">注文セット 4 を作成する</span><span class="sxs-lookup"><span data-stu-id="250d4-176">Create order set 4</span></span>

#### <a name="sales-orders-4-1-and-4-2"></a><span data-ttu-id="250d4-177">販売注文 4-1 と 4-2</span><span class="sxs-lookup"><span data-stu-id="250d4-177">Sales orders 4-1 and 4-2</span></span>

1. <span data-ttu-id="250d4-178">以下の設定で 2 つの同一の販売注文を作成します:</span><span class="sxs-lookup"><span data-stu-id="250d4-178">Create two identical sales orders that have the following settings:</span></span>

    - <span data-ttu-id="250d4-179">**顧客アカウント:** *US-003*</span><span class="sxs-lookup"><span data-stu-id="250d4-179">**Customer account:** *US-003*</span></span>

1. <span data-ttu-id="250d4-180">以下の設定で注文明細行を追加します:</span><span class="sxs-lookup"><span data-stu-id="250d4-180">Add an order line that has the following settings:</span></span>

    - <span data-ttu-id="250d4-181">**品目番号 :** *A0001* (**コード 4** フィルタが割り当てられていない品目)</span><span class="sxs-lookup"><span data-stu-id="250d4-181">**Item number:** *A0001* (an item that no **Code 4** filter is assigned to)</span></span>
    - <span data-ttu-id="250d4-182">**数量:** *1.00*</span><span class="sxs-lookup"><span data-stu-id="250d4-182">**Quantity:** *1.00*</span></span>

1. <span data-ttu-id="250d4-183">**在庫 \> 引当** を選択し、アクションウ ィンドウで **ロットの引当** を選択して、注文明細行を引当します。</span><span class="sxs-lookup"><span data-stu-id="250d4-183">Select **Inventory \> Reservation**, and then, on the Action Pane, select **Reserve lot** to reserve the order line.</span></span>

#### <a name="sales-orders-4-3-and-4-4"></a><span data-ttu-id="250d4-184">販売注文 4-3 と 4-4</span><span class="sxs-lookup"><span data-stu-id="250d4-184">Sales orders 4-3 and 4-4</span></span>

1. <span data-ttu-id="250d4-185">以下の設定で 2 つの同一の販売注文を作成します:</span><span class="sxs-lookup"><span data-stu-id="250d4-185">Create two identical sales orders that have the following settings:</span></span>

    - <span data-ttu-id="250d4-186">**顧客アカウント:** *US-004*</span><span class="sxs-lookup"><span data-stu-id="250d4-186">**Customer account:** *US-004*</span></span>

1. <span data-ttu-id="250d4-187">以下の設定で注文明細行を追加します:</span><span class="sxs-lookup"><span data-stu-id="250d4-187">Add an order line that has the following settings:</span></span>

    - <span data-ttu-id="250d4-188">**品目番号 :** *A0001* (**コード 4** フィルタが割り当てられていない品目)</span><span class="sxs-lookup"><span data-stu-id="250d4-188">**Item number:** *A0001* (an item that no **Code 4** filter is assigned to)</span></span>
    - <span data-ttu-id="250d4-189">**数量:** *1.00*</span><span class="sxs-lookup"><span data-stu-id="250d4-189">**Quantity:** *1.00*</span></span>

1. <span data-ttu-id="250d4-190">**在庫 \> 引当** を選択し、アクションウ ィンドウで **ロットの引当** を選択して、注文明細行を引当します。</span><span class="sxs-lookup"><span data-stu-id="250d4-190">Select **Inventory \> Reservation**, and then, on the Action Pane, select **Reserve lot** to reserve the order line.</span></span>

#### <a name="sales-orders-4-5-and-4-6"></a><span data-ttu-id="250d4-191">販売注文 4-5 と 4-6</span><span class="sxs-lookup"><span data-stu-id="250d4-191">Sales orders 4-5 and 4-6</span></span>

1. <span data-ttu-id="250d4-192">以下の設定で 2 つの同一の販売注文を作成します:</span><span class="sxs-lookup"><span data-stu-id="250d4-192">Create two identical sales orders that have the following settings:</span></span>

    - <span data-ttu-id="250d4-193">**顧客アカウント:** *US-007*</span><span class="sxs-lookup"><span data-stu-id="250d4-193">**Customer account:** *US-007*</span></span>
    - <span data-ttu-id="250d4-194">**サイト:** *6*</span><span class="sxs-lookup"><span data-stu-id="250d4-194">**Site:** *6*</span></span>
    - <span data-ttu-id="250d4-195">**倉庫:** *61*</span><span class="sxs-lookup"><span data-stu-id="250d4-195">**Warehouse:** *61*</span></span>
    - <span data-ttu-id="250d4-196">**プール :** *ShipCons*</span><span class="sxs-lookup"><span data-stu-id="250d4-196">**Pool:** *ShipCons*</span></span>

1. <span data-ttu-id="250d4-197">以下の設定で注文明細行を追加します:</span><span class="sxs-lookup"><span data-stu-id="250d4-197">Add an order line that has the following settings:</span></span>

    - <span data-ttu-id="250d4-198">**品目番号 :** *A0001* (**コード 4** フィルタが割り当てられていない品目)</span><span class="sxs-lookup"><span data-stu-id="250d4-198">**Item number:** *A0001* (an item that no **Code 4** filter is assigned to)</span></span>
    - <span data-ttu-id="250d4-199">**数量:** *1.00*</span><span class="sxs-lookup"><span data-stu-id="250d4-199">**Quantity:** *1.00*</span></span>

1. <span data-ttu-id="250d4-200">**在庫 \> 引当** を選択し、アクションウ ィンドウで **ロットの引当** を選択して、注文明細行を引当します。</span><span class="sxs-lookup"><span data-stu-id="250d4-200">Select **Inventory \> Reservation**, and then, on the Action Pane, select **Reserve lot** to reserve the order line.</span></span>

#### <a name="sales-orders-4-7-and-4-8"></a><span data-ttu-id="250d4-201">販売注文 4-7 と 4-8</span><span class="sxs-lookup"><span data-stu-id="250d4-201">Sales orders 4-7 and 4-8</span></span>

1. <span data-ttu-id="250d4-202">以下の設定で 2 つの同一の販売注文を作成します:</span><span class="sxs-lookup"><span data-stu-id="250d4-202">Create two identical sales orders that have the following settings:</span></span>

    - <span data-ttu-id="250d4-203">**顧客アカウント:** *US-007*</span><span class="sxs-lookup"><span data-stu-id="250d4-203">**Customer account:** *US-007*</span></span>
    - <span data-ttu-id="250d4-204">**サイト:** *6*</span><span class="sxs-lookup"><span data-stu-id="250d4-204">**Site:** *6*</span></span>
    - <span data-ttu-id="250d4-205">**倉庫:** *61*</span><span class="sxs-lookup"><span data-stu-id="250d4-205">**Warehouse:** *61*</span></span>
    - <span data-ttu-id="250d4-206">**プール :** このフィールドは空白のままにします。</span><span class="sxs-lookup"><span data-stu-id="250d4-206">**Pool:** Leave this field blank.</span></span>

1. <span data-ttu-id="250d4-207">以下の設定で注文明細行を追加します:</span><span class="sxs-lookup"><span data-stu-id="250d4-207">Add an order line that has the following settings:</span></span>

    - <span data-ttu-id="250d4-208">**品目番号 :** *A0001* (**コード 4** フィルタが割り当てられていない品目)</span><span class="sxs-lookup"><span data-stu-id="250d4-208">**Item number:** *A0001* (an item that no **Code 4** filter is assigned to)</span></span>
    - <span data-ttu-id="250d4-209">**数量:** *1.00*</span><span class="sxs-lookup"><span data-stu-id="250d4-209">**Quantity:** *1.00*</span></span>

1. <span data-ttu-id="250d4-210">**在庫 \> 引当** を選択し、アクションウ ィンドウで **ロットの引当** を選択して、注文明細行を引当します。</span><span class="sxs-lookup"><span data-stu-id="250d4-210">Select **Inventory \> Reservation**, and then, on the Action Pane, select **Reserve lot** to reserve the order line.</span></span>

## <a name="use-the-load-planning-workbench-to-create-loads-and-release-them-to-the-warehouse"></a><span data-ttu-id="250d4-211">積荷計画ワークベンチを使用して積荷を作成し、倉庫にリリースする</span><span class="sxs-lookup"><span data-stu-id="250d4-211">Use the load planning workbench to create loads and release them to the warehouse</span></span>

<span data-ttu-id="250d4-212">このシナリオで作成した各注文セットに対して積荷を作成し、それを倉庫にリリースするには、次の手順に従います。</span><span class="sxs-lookup"><span data-stu-id="250d4-212">Follow these steps to create a load for each order set that you created for this scenario and then release it to the warehouse.</span></span>

1. <span data-ttu-id="250d4-213">**倉庫管理 \> 積荷 \> 積荷計画ワークベンチ** に移動します。</span><span class="sxs-lookup"><span data-stu-id="250d4-213">Go to **Warehouse management \> Loads \> Load planning workbench**.</span></span>
1. <span data-ttu-id="250d4-214">**販売明細** タブで、このシナリオに対して作成した注文セットの1つから、すべての販売注文明細行を検索して選択します。</span><span class="sxs-lookup"><span data-stu-id="250d4-214">On the **Sales lines** tab, find and select all the sales order lines from one of the order sets that you created for this scenario.</span></span>
1. <span data-ttu-id="250d4-215">アクション ウィンドウの **供給と需要** タブで、**追加 \> 新規積荷** を選択して、選択した注文明細行を新しい積荷に追加します。</span><span class="sxs-lookup"><span data-stu-id="250d4-215">On the Action Pane, on the **Supply and demand** tab, select **Add \> To new load** to add the selected order lines to a new Load.</span></span>
1. <span data-ttu-id="250d4-216">**積荷のテンプレート割り当て** ダイアログ ボックスの **積荷のテンプレート ID** フィールドで、*Stnd load template* などの積荷テンプレートを選択します。</span><span class="sxs-lookup"><span data-stu-id="250d4-216">In the **Load template assignment** dialog box, in the **Load template ID** field, select a load template, such as *Stnd Load Template*.</span></span>
1. <span data-ttu-id="250d4-217">**OK** を選択してダイアログ ボックスを閉じます。</span><span class="sxs-lookup"><span data-stu-id="250d4-217">Select **OK** to close the dialog box.</span></span> 
1. <span data-ttu-id="250d4-218">**積荷** セクションで、作成した積荷を見つけて選択します。</span><span class="sxs-lookup"><span data-stu-id="250d4-218">In the **Loads** section, find and select the load that you just created.</span></span>
1. <span data-ttu-id="250d4-219">**リリース \> 倉庫へのリリース** を選択し、選択した積荷を倉庫にリリースします。</span><span class="sxs-lookup"><span data-stu-id="250d4-219">Select **Release \> Release to warehouse** to release the selected load to the warehouse.</span></span>
1. <span data-ttu-id="250d4-220">このシナリオに対して作成した他の 3 つの注文セットに対して、この手順を繰り返します。</span><span class="sxs-lookup"><span data-stu-id="250d4-220">Repeat this procedure for the other three order sets that you created for this scenario.</span></span>

## <a name="verify-the-shipments"></a><span data-ttu-id="250d4-221">出荷の確認</span><span class="sxs-lookup"><span data-stu-id="250d4-221">Verify the shipments</span></span>

<span data-ttu-id="250d4-222">次の手順では、出荷連結の結果として作成、更新された出荷を確認できます。</span><span class="sxs-lookup"><span data-stu-id="250d4-222">The following procedure lets you verify the shipments that have been created or updated as a result of shipment consolidation.</span></span> <span data-ttu-id="250d4-223">これを使用して、このシナリオで作成した各注文セットを確認します。続いてその結果が得られるかどうかを確認するには、次のセクションを確認します。</span><span class="sxs-lookup"><span data-stu-id="250d4-223">Use it to review each order set that you created for this scenario, and then review the subsections that follow to make sure that you've obtained the expected results.</span></span>

1. <span data-ttu-id="250d4-224">**倉庫管理 \> 出荷 \> すべての出荷** に移動します。</span><span class="sxs-lookup"><span data-stu-id="250d4-224">Go to **Warehouse management \> Shipments \> All shipments**.</span></span>
1. <span data-ttu-id="250d4-225">必要な出荷を検索して選択します。</span><span class="sxs-lookup"><span data-stu-id="250d4-225">Find and select the required shipment.</span></span>
1. <span data-ttu-id="250d4-226">出荷の作成時または更新時に連結ポリシーが使用されていた場合は、**出荷連結ポリシー** フィールドに表示する必要があります。</span><span class="sxs-lookup"><span data-stu-id="250d4-226">If a consolidation policy was used when the shipment was created or updated, you should see it in the **Shipment consolidation policy** field.</span></span>

### <a name="release-order-set-1-in-one-load"></a><span data-ttu-id="250d4-227">ひとつの積荷で注文セット 1 をリリースする</span><span class="sxs-lookup"><span data-stu-id="250d4-227">Release order set 1 in one load</span></span>

<span data-ttu-id="250d4-228">次の 2 つの出荷が作成されている必要があります:</span><span class="sxs-lookup"><span data-stu-id="250d4-228">Two shipments should have been created:</span></span>

- <span data-ttu-id="250d4-229">最初の出荷は、*顧客モード* の出荷連結ポリシーを使用して作成された 3 つの行で構成されます。</span><span class="sxs-lookup"><span data-stu-id="250d4-229">The first shipment contains three lines and was created by using the *CustomerMode* shipment consolidation policy.</span></span>
- <span data-ttu-id="250d4-230">2 つ目の出荷は、*航空運賃* 輸送モードの荷渡方法を使用しないもので、顧客注文の *CustomerOrderNo* 連結ポリシーを使用して作成されてい ます。</span><span class="sxs-lookup"><span data-stu-id="250d4-230">The second shipment, which doesn't use the *Airways* transportation mode of delivery, was created by using the *CustomerOrderNo* shipment consolidation policy.</span></span>

### <a name="release-order-set-2-in-one-load"></a><span data-ttu-id="250d4-231">ひとつの積荷で注文セット 2 をリリースする</span><span class="sxs-lookup"><span data-stu-id="250d4-231">Release order set 2 in one load</span></span>

<span data-ttu-id="250d4-232">次の 3 つの出荷が作成されている必要があります:</span><span class="sxs-lookup"><span data-stu-id="250d4-232">Three shipments should have been created:</span></span>

- <span data-ttu-id="250d4-233">最初の出荷には、 *可燃性* の品目が含まれています。</span><span class="sxs-lookup"><span data-stu-id="250d4-233">The first shipment contains the *Flammable* items.</span></span>
- <span data-ttu-id="250d4-234">他の 2 つの出荷には、*爆発性* の品目を含む 1 つの行が含まれてい ます。</span><span class="sxs-lookup"><span data-stu-id="250d4-234">Each of the other two shipments contains one line that has the *Explosive* item.</span></span>

### <a name="release-order-set-3-in-one-load"></a><span data-ttu-id="250d4-235">ひとつの積荷で注文セット 3 をリリースする</span><span class="sxs-lookup"><span data-stu-id="250d4-235">Release order set 3 in one load</span></span>

<span data-ttu-id="250d4-236">次の 2 つの出荷が作成されている必要があります:</span><span class="sxs-lookup"><span data-stu-id="250d4-236">Two shipments should have been created:</span></span>

- <span data-ttu-id="250d4-237">1つ目の出荷には、**顧客要求** フィールドが *1* に設定されている販売注文の注文明細行が含まれます。</span><span class="sxs-lookup"><span data-stu-id="250d4-237">The first shipment contains order lines from the sales order where the **Customer requisition** field is set to *1*.</span></span>
- <span data-ttu-id="250d4-238">2つ目の出荷には、**顧客要求** フィールドが *2* に設定されている販売注文の注文明細行が含まれます。</span><span class="sxs-lookup"><span data-stu-id="250d4-238">The second shipment contains order lines from sales order where the **Customer requisition** field is set to *2*.</span></span>

### <a name="release-order-set-4-in-one-load"></a><span data-ttu-id="250d4-239">ひとつの積荷で注文セット 4 をリリースする</span><span class="sxs-lookup"><span data-stu-id="250d4-239">Release order set 4 in one load</span></span>

<span data-ttu-id="250d4-240">次の 4 つの出荷が作成されている必要があります:</span><span class="sxs-lookup"><span data-stu-id="250d4-240">Four shipments should have been created:</span></span>

- <span data-ttu-id="250d4-241">顧客アカウント *US-003* の 2 件の販売注文の明細行は、*注文プール* の出荷連結ポリシーを使用して 1 つの出荷にグループ化されています。</span><span class="sxs-lookup"><span data-stu-id="250d4-241">Lines from two orders for customer account *US-003* were grouped into one shipment by using the *Order pool* shipment consolidation policy.</span></span>
- <span data-ttu-id="250d4-242">顧客アカウント *US-004* の 2 件の販売注文の明細行は、*注文プール* の出荷連結ポリシーを使用して 1 つの出荷にグループ化されています。</span><span class="sxs-lookup"><span data-stu-id="250d4-242">Lines from two orders for customer account *US-004* were grouped into one shipment by using the *Order pool* shipment consolidation policy.</span></span>
- <span data-ttu-id="250d4-243">顧客アカウント *US-007* の販売注文 4-5 および 4-6 の明細行は、*注文プール* の出荷連結ポリシーを使用して1つの出荷にグループ化されています。</span><span class="sxs-lookup"><span data-stu-id="250d4-243">Lines from sales orders 4-5 and 4-6 for customer account *US-007* were grouped into one shipment by using the *Order pool* shipment consolidation policy.</span></span>
- <span data-ttu-id="250d4-244">顧客アカウント *US-007* の販売注文 4-7 および 4-8 の明細行は、*クロスオーダー* の出荷連結ポリシーを使用して1つの出荷にグループ化されています。</span><span class="sxs-lookup"><span data-stu-id="250d4-244">Lines from sales orders 4-7 and 4-8 for customer account *US-007* were grouped into one shipment by using the *CrossOrder* shipment consolidation policy.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="250d4-245">追加リソース</span><span class="sxs-lookup"><span data-stu-id="250d4-245">Additional resources</span></span>

- [<span data-ttu-id="250d4-246">出荷連結ポリシー</span><span class="sxs-lookup"><span data-stu-id="250d4-246">Shipment consolidation policies</span></span>](about-shipment-consolidation-policies.md)
- [<span data-ttu-id="250d4-247">出荷連結ポリシーを構成する</span><span class="sxs-lookup"><span data-stu-id="250d4-247">Configure shipment consolidation policies</span></span>](configure-shipment-consolidation-policies.md)


[!INCLUDE[footer-include](../../includes/footer-banner.md)]