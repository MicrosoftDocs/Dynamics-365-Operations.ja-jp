---
title: 積荷計画ワークベンチから倉庫へのリリースを使用して出荷を連結する
description: このトピックでは、複数の注文が同一の積荷で倉庫にリリースされ、自動的に出荷に連結されるシナリオを示します。
author: GarmMSFT
manager: tfehr
ms.date: 05/12/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: WHSShipConsolidationPolicy, WHSShipConsolidationWorkbench
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: kamaybac
ms.search.validFrom: 2020-05-01
ms.dyn365.ops.version: 10.0.3
ms.openlocfilehash: 2f1dd5c743664e638c043b600ae7b0f6bce5ddcd
ms.sourcegitcommit: 199848e78df5cb7c439b001bdbe1ece963593cdb
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 10/13/2020
ms.locfileid: "4431727"
---
# <a name="consolidate-shipments-by-using-release-to-warehouse-from-the-load-planning-workbench"></a><span data-ttu-id="be0e2-103">積荷計画ワークベンチから倉庫へのリリースを使用して出荷を連結する</span><span class="sxs-lookup"><span data-stu-id="be0e2-103">Consolidate shipments by using Release to warehouse from the load planning workbench</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="be0e2-104">このトピックでは、複数の注文が同一の積荷で倉庫にリリースされ、自動的に出荷に連結されるシナリオを示します。</span><span class="sxs-lookup"><span data-stu-id="be0e2-104">This topic presents a scenario where multiple orders are released to the warehouse in the same load and are then automatically consolidated into shipments.</span></span>

## <a name="make-demo-data-available"></a><span data-ttu-id="be0e2-105">デモ データを有効化する</span><span class="sxs-lookup"><span data-stu-id="be0e2-105">Make demo data available</span></span>

<span data-ttu-id="be0e2-106">このトピックのシナリオでは、Microsoft Dynamics 365 Supply Chain Management にて用意されている標準のデモデータに含まれる値とレコードを参照し ます。</span><span class="sxs-lookup"><span data-stu-id="be0e2-106">The scenario in this topic references values and records that are included in the standard demo data that is provided for Microsoft Dynamics 365 Supply Chain Management.</span></span> <span data-ttu-id="be0e2-107">ここで提供されている値を使用するには、デモデータがインストールされている環境で作業し、開始する前に法人を **usmf** に設定します。</span><span class="sxs-lookup"><span data-stu-id="be0e2-107">If you want to use the values that are provided here as you do the exercises, be sure to work in an environment where the demo data is installed, and set the legal entity to **USMF** before you begin.</span></span>

## <a name="set-up-shipment-consolidation-policies-and-product-filters"></a><span data-ttu-id="be0e2-108">出荷連結ポリシーおよび製品フィルタの設定</span><span class="sxs-lookup"><span data-stu-id="be0e2-108">Set up shipment consolidation policies and product filters</span></span>

<span data-ttu-id="be0e2-109">このシナリオでは、既にこの機能を有効にし、[出荷連結ポリシーの構成](configure-shipment-consolidation-policies.md)内の実習を完了しており、同ページ内に記述されているポリシーとその他のレコードを作成していることを前提としています。</span><span class="sxs-lookup"><span data-stu-id="be0e2-109">The scenario that is described here assumes that you've already turned on the feature, done the exercises in [Configure shipment consolidation policies](configure-shipment-consolidation-policies.md), and created the policies and other records that are described there.</span></span> <span data-ttu-id="be0e2-110">このシナリオを続行する前に、この演習を行っている必要があります。</span><span class="sxs-lookup"><span data-stu-id="be0e2-110">Be sure to do those exercises before you continue with this scenario.</span></span>

## <a name="create-the-sales-orders-for-this-scenario"></a><span data-ttu-id="be0e2-111">このシナリオで使用する販売注文の作成</span><span class="sxs-lookup"><span data-stu-id="be0e2-111">Create the sales orders for this scenario</span></span>

<span data-ttu-id="be0e2-112">シナリオで使用する一連の販売注文を作成することから始めます。</span><span class="sxs-lookup"><span data-stu-id="be0e2-112">Start by creating a collection of sales orders that you can work with.</span></span> <span data-ttu-id="be0e2-113">高度な倉庫 (WMS) プロセスが利用できる倉庫を使用する必要があります。</span><span class="sxs-lookup"><span data-stu-id="be0e2-113">You must work with a warehouse that is enabled for advanced warehouse (WMS) processes.</span></span> <span data-ttu-id="be0e2-114">他の倉庫を明示的に指定していない場合は、次の注文セットのそれぞれに対して同じ倉庫が使用されなければなりません。</span><span class="sxs-lookup"><span data-stu-id="be0e2-114">Unless a different warehouse is explicitly mentioned, that same warehouse must be used for each of the following sets of orders.</span></span>

<span data-ttu-id="be0e2-115">**売掛金勘定  \> 注文 \> すべての販売注文** に移動し、次のサブセクションで説明されている設定を含む販売注文のコレクションを作成します。</span><span class="sxs-lookup"><span data-stu-id="be0e2-115">Go to **Accounts receivable \> Orders \> All sales orders**, and create a collection of sales orders that have the settings that are described in the following subsections.</span></span>

### <a name="create-order-set-1"></a><span data-ttu-id="be0e2-116">注文セット 1 を作成する</span><span class="sxs-lookup"><span data-stu-id="be0e2-116">Create order set 1</span></span>

#### <a name="sales-order-1-1"></a><span data-ttu-id="be0e2-117">販売注文 1-1</span><span class="sxs-lookup"><span data-stu-id="be0e2-117">Sales order 1-1</span></span>

1. <span data-ttu-id="be0e2-118">以下の設定で販売注文を作成します:</span><span class="sxs-lookup"><span data-stu-id="be0e2-118">Create a sales order that has the following settings:</span></span>

    - <span data-ttu-id="be0e2-119">**顧客アカウント:** *US-001*</span><span class="sxs-lookup"><span data-stu-id="be0e2-119">**Customer account:** *US-001*</span></span>
    - <span data-ttu-id="be0e2-120">**荷渡方法:** *Airwa-Air*</span><span class="sxs-lookup"><span data-stu-id="be0e2-120">**Mode of delivery:** *Airwa-Air*</span></span>

1. <span data-ttu-id="be0e2-121">以下の設定で注文明細行を追加します:</span><span class="sxs-lookup"><span data-stu-id="be0e2-121">Add an order line that has the following settings:</span></span>

    - <span data-ttu-id="be0e2-122">**品目番号 :** *A0001* (**コード 4** フィルタが割り当てられていない品目)</span><span class="sxs-lookup"><span data-stu-id="be0e2-122">**Item number:** *A0001* (an item that no **Code 4** filter is assigned to)</span></span>
    - <span data-ttu-id="be0e2-123">**数量:** *1.00*</span><span class="sxs-lookup"><span data-stu-id="be0e2-123">**Quantity:** *1.00*</span></span>

1. <span data-ttu-id="be0e2-124">**在庫 \> 引当** を選択し、アクションウ ィンドウで **ロットの引当** を選択して、注文明細行を引当します。</span><span class="sxs-lookup"><span data-stu-id="be0e2-124">Select **Inventory \> Reservation**, and then, on the Action Pane, select **Reserve lot** to reserve the order line.</span></span>

#### <a name="sales-order-1-2"></a><span data-ttu-id="be0e2-125">販売注文 1-2</span><span class="sxs-lookup"><span data-stu-id="be0e2-125">Sales order 1-2</span></span>

1. <span data-ttu-id="be0e2-126">以下の設定で販売注文を作成します:</span><span class="sxs-lookup"><span data-stu-id="be0e2-126">Create a sales order that has the following settings:</span></span>

    - <span data-ttu-id="be0e2-127">**顧客アカウント:** *US-001*</span><span class="sxs-lookup"><span data-stu-id="be0e2-127">**Customer account:** *US-001*</span></span>
    - <span data-ttu-id="be0e2-128">**荷渡方法:** *Airwa-Air*</span><span class="sxs-lookup"><span data-stu-id="be0e2-128">**Mode of delivery:** *Airwa-Air*</span></span>

1. <span data-ttu-id="be0e2-129">以下の設定で注文明細行を追加します:</span><span class="sxs-lookup"><span data-stu-id="be0e2-129">Add an order line that has the following settings:</span></span>

    - <span data-ttu-id="be0e2-130">**品目番号 :** *A0001* (**コード 4** フィルタが割り当てられていない品目)</span><span class="sxs-lookup"><span data-stu-id="be0e2-130">**Item number:** *A0001* (an item that no **Code 4** filter is assigned to)</span></span>
    - <span data-ttu-id="be0e2-131">**数量:** *1.00*</span><span class="sxs-lookup"><span data-stu-id="be0e2-131">**Quantity:** *1.00*</span></span>

1. <span data-ttu-id="be0e2-132">**在庫 \> 引当** を選択し、アクションウ ィンドウで **ロットの引当** を選択して、注文明細行を引当します。</span><span class="sxs-lookup"><span data-stu-id="be0e2-132">Select **Inventory \> Reservation**, and then, on the Action Pane, select **Reserve lot** to reserve the order line.</span></span>

#### <a name="sales-order-1-3"></a><span data-ttu-id="be0e2-133">販売注文 1-3</span><span class="sxs-lookup"><span data-stu-id="be0e2-133">Sales order 1-3</span></span>

1. <span data-ttu-id="be0e2-134">以下の設定で販売注文を作成します:</span><span class="sxs-lookup"><span data-stu-id="be0e2-134">Create a sales order that has the following settings:</span></span>

    - <span data-ttu-id="be0e2-135">**顧客アカウント:** *US-001*</span><span class="sxs-lookup"><span data-stu-id="be0e2-135">**Customer account:** *US-001*</span></span>
    - <span data-ttu-id="be0e2-136">**荷渡方法:** *10*</span><span class="sxs-lookup"><span data-stu-id="be0e2-136">**Mode of delivery:** *10*</span></span>

1. <span data-ttu-id="be0e2-137">以下の設定で注文明細行を追加します:</span><span class="sxs-lookup"><span data-stu-id="be0e2-137">Add an order line that has the following settings:</span></span>

    - <span data-ttu-id="be0e2-138">**品目番号 :** *A0001* (**コード 4** フィルタが割り当てられていない品目)</span><span class="sxs-lookup"><span data-stu-id="be0e2-138">**Item number:** *A0001* (an item that no **Code 4** filter is assigned to)</span></span>
    - <span data-ttu-id="be0e2-139">**数量:** *1.00*</span><span class="sxs-lookup"><span data-stu-id="be0e2-139">**Quantity:** *1.00*</span></span>

1. <span data-ttu-id="be0e2-140">**在庫 \> 引当** を選択し、アクションウ ィンドウで **ロットの引当** を選択して、注文明細行を引当します。</span><span class="sxs-lookup"><span data-stu-id="be0e2-140">Select **Inventory \> Reservation**, and then, on the Action Pane, select **Reserve lot** to reserve the order line.</span></span>
1. <span data-ttu-id="be0e2-141">以下の設定で 2 つ目の販売注文を作成します:</span><span class="sxs-lookup"><span data-stu-id="be0e2-141">Add a second order line that has the following settings:</span></span>

    - <span data-ttu-id="be0e2-142">**品目番号 :** *A0002* ( **コード 4** フィルタが割り当てられていない品目)</span><span class="sxs-lookup"><span data-stu-id="be0e2-142">**Item number:** *A0002* (an item that no **Code 4** filter is assigned to)</span></span>
    - <span data-ttu-id="be0e2-143">**数量:** *1.00*</span><span class="sxs-lookup"><span data-stu-id="be0e2-143">**Quantity:** *1.00*</span></span>
    - <span data-ttu-id="be0e2-144">**荷渡方法:** *Airwa-Air*</span><span class="sxs-lookup"><span data-stu-id="be0e2-144">**Mode of delivery:** *Airwa-Air*</span></span>

1. <span data-ttu-id="be0e2-145">**在庫 \> 引当** を選択し、アクションウ ィンドウで **ロットの引当** を選択して、2 つ目の注文明細行を引当します。</span><span class="sxs-lookup"><span data-stu-id="be0e2-145">Select **Inventory \> Reservation**, and then, on the Action Pane, select **Reserve lot** to reserve the second order line.</span></span>

### <a name="create-order-set-2"></a><span data-ttu-id="be0e2-146">注文セット 2 を作成する</span><span class="sxs-lookup"><span data-stu-id="be0e2-146">Create order set 2</span></span>

#### <a name="sales-orders-2-1-and-2-2"></a><span data-ttu-id="be0e2-147">販売注文 2-1 と 2-2</span><span class="sxs-lookup"><span data-stu-id="be0e2-147">Sales orders 2-1 and 2-2</span></span>

1. <span data-ttu-id="be0e2-148">以下の設定で 2 つの同一の販売注文を作成します:</span><span class="sxs-lookup"><span data-stu-id="be0e2-148">Create two identical sales orders that have the following settings:</span></span>

    - <span data-ttu-id="be0e2-149">**顧客アカウント:** *US-002*</span><span class="sxs-lookup"><span data-stu-id="be0e2-149">**Customer account:** *US-002*</span></span>

1. <span data-ttu-id="be0e2-150">以下の設定で注文明細行を追加します:</span><span class="sxs-lookup"><span data-stu-id="be0e2-150">Add an order line that has the following settings:</span></span>

    - <span data-ttu-id="be0e2-151">**品目番号 :** *M9200* (**コード 4** のフィルタが *可燃性* に設定されている品目)</span><span class="sxs-lookup"><span data-stu-id="be0e2-151">**Item number:** *M9200* (an item where the **Code 4** filter is set to *Flammable*)</span></span>
    - <span data-ttu-id="be0e2-152">**数量:** *1.00*</span><span class="sxs-lookup"><span data-stu-id="be0e2-152">**Quantity:** *1.00*</span></span>

1. <span data-ttu-id="be0e2-153">**在庫 \> 引当** を選択し、アクションウ ィンドウで **ロットの引当** を選択して、注文明細行を引当します。</span><span class="sxs-lookup"><span data-stu-id="be0e2-153">Select **Inventory \> Reservation**, and then, on the Action Pane, select **Reserve lot** to reserve the order line.</span></span>
1. <span data-ttu-id="be0e2-154">以下の設定で 2 つ目の販売注文を作成します:</span><span class="sxs-lookup"><span data-stu-id="be0e2-154">Add a second order line that has the following settings:</span></span>

    - <span data-ttu-id="be0e2-155">**品目番号 :** *M9201*( **コード 4** のフィルタが *爆発物* に設定されている品目)</span><span class="sxs-lookup"><span data-stu-id="be0e2-155">**Item number:** *M9201* (an item where the **Code 4** filter is set to *Explosive*)</span></span>
    - <span data-ttu-id="be0e2-156">**数量:** *1.00*</span><span class="sxs-lookup"><span data-stu-id="be0e2-156">**Quantity:** *1.00*</span></span>
    - <span data-ttu-id="be0e2-157">**荷渡方法:** *Airwa-Air*</span><span class="sxs-lookup"><span data-stu-id="be0e2-157">**Mode of delivery:** *Airwa-Air*</span></span>

1. <span data-ttu-id="be0e2-158">**在庫 \> 引当** を選択し、アクションウ ィンドウで **ロットの引当** を選択して、2 つ目の注文明細行を引当します。</span><span class="sxs-lookup"><span data-stu-id="be0e2-158">Select **Inventory \> Reservation**, and then, on the Action Pane, select **Reserve lot** to reserve the second order line.</span></span>

### <a name="create-order-set-3"></a><span data-ttu-id="be0e2-159">注文セット 3 を作成する</span><span class="sxs-lookup"><span data-stu-id="be0e2-159">Create order set 3</span></span>

#### <a name="sales-orders-3-1-and-3-2"></a><span data-ttu-id="be0e2-160">販売注文 3-1 と 3-2</span><span class="sxs-lookup"><span data-stu-id="be0e2-160">Sales orders 3-1 and 3-2</span></span>

1. <span data-ttu-id="be0e2-161">以下の設定で 2 つの同一の販売注文を作成します:</span><span class="sxs-lookup"><span data-stu-id="be0e2-161">Create two identical sales orders that have the following settings:</span></span>

    - <span data-ttu-id="be0e2-162">**顧客アカウント:** *US-001*</span><span class="sxs-lookup"><span data-stu-id="be0e2-162">**Customer account:** *US-001*</span></span>
    - <span data-ttu-id="be0e2-163">**顧客の要求:** *1*</span><span class="sxs-lookup"><span data-stu-id="be0e2-163">**Customer requisition:** *1*</span></span>

1. <span data-ttu-id="be0e2-164">以下の設定で注文明細行を追加します:</span><span class="sxs-lookup"><span data-stu-id="be0e2-164">Add an order line that has the following settings:</span></span>

    - <span data-ttu-id="be0e2-165">**品目番号 :** *A0001* (**コード 4** フィルタが割り当てられていない品目)</span><span class="sxs-lookup"><span data-stu-id="be0e2-165">**Item number:** *A0001* (an item that no **Code 4** filter is assigned to)</span></span>
    - <span data-ttu-id="be0e2-166">**数量:** *1.00*</span><span class="sxs-lookup"><span data-stu-id="be0e2-166">**Quantity:** *1.00*</span></span>

1. <span data-ttu-id="be0e2-167">**在庫 \> 引当** を選択し、アクションウ ィンドウで **ロットの引当** を選択して、注文明細行を引当します。</span><span class="sxs-lookup"><span data-stu-id="be0e2-167">Select **Inventory \> Reservation**, and then, on the Action Pane, select **Reserve lot** to reserve the order line.</span></span>

#### <a name="sales-orders-3-3-and-3-4"></a><span data-ttu-id="be0e2-168">販売注文 3-3 と 3-4</span><span class="sxs-lookup"><span data-stu-id="be0e2-168">Sales orders 3-3 and 3-4</span></span>

1. <span data-ttu-id="be0e2-169">以下の設定で 2 つの同一の販売注文を作成します:</span><span class="sxs-lookup"><span data-stu-id="be0e2-169">Create two identical sales orders that have the following settings:</span></span>

    - <span data-ttu-id="be0e2-170">**顧客アカウント:** *US-001*</span><span class="sxs-lookup"><span data-stu-id="be0e2-170">**Customer account:** *US-001*</span></span>
    - <span data-ttu-id="be0e2-171">**顧客の要求:** *2*</span><span class="sxs-lookup"><span data-stu-id="be0e2-171">**Customer requisition:** *2*</span></span>

1. <span data-ttu-id="be0e2-172">以下の設定で注文明細行を追加します:</span><span class="sxs-lookup"><span data-stu-id="be0e2-172">Add an order line that has the following settings:</span></span>

    - <span data-ttu-id="be0e2-173">**品目番号 :** *A0001* (**コード 4** フィルタが割り当てられていない品目)</span><span class="sxs-lookup"><span data-stu-id="be0e2-173">**Item number:** *A0001* (an item that no **Code 4** filter is assigned to)</span></span>
    - <span data-ttu-id="be0e2-174">**数量:** *1.00*</span><span class="sxs-lookup"><span data-stu-id="be0e2-174">**Quantity:** *1.00*</span></span>

1. <span data-ttu-id="be0e2-175">**在庫 \> 引当** を選択し、アクションウ ィンドウで **ロットの引当** を選択して、注文明細行を引当します。</span><span class="sxs-lookup"><span data-stu-id="be0e2-175">Select **Inventory \> Reservation**, and then, on the Action Pane, select **Reserve lot** to reserve the order line.</span></span>

### <a name="create-order-set-4"></a><span data-ttu-id="be0e2-176">注文セット 4 を作成する</span><span class="sxs-lookup"><span data-stu-id="be0e2-176">Create order set 4</span></span>

#### <a name="sales-orders-4-1-and-4-2"></a><span data-ttu-id="be0e2-177">販売注文 4-1 と 4-2</span><span class="sxs-lookup"><span data-stu-id="be0e2-177">Sales orders 4-1 and 4-2</span></span>

1. <span data-ttu-id="be0e2-178">以下の設定で 2 つの同一の販売注文を作成します:</span><span class="sxs-lookup"><span data-stu-id="be0e2-178">Create two identical sales orders that have the following settings:</span></span>

    - <span data-ttu-id="be0e2-179">**顧客アカウント:** *US-003*</span><span class="sxs-lookup"><span data-stu-id="be0e2-179">**Customer account:** *US-003*</span></span>

1. <span data-ttu-id="be0e2-180">以下の設定で注文明細行を追加します:</span><span class="sxs-lookup"><span data-stu-id="be0e2-180">Add an order line that has the following settings:</span></span>

    - <span data-ttu-id="be0e2-181">**品目番号 :** *A0001* (**コード 4** フィルタが割り当てられていない品目)</span><span class="sxs-lookup"><span data-stu-id="be0e2-181">**Item number:** *A0001* (an item that no **Code 4** filter is assigned to)</span></span>
    - <span data-ttu-id="be0e2-182">**数量:** *1.00*</span><span class="sxs-lookup"><span data-stu-id="be0e2-182">**Quantity:** *1.00*</span></span>

1. <span data-ttu-id="be0e2-183">**在庫 \> 引当** を選択し、アクションウ ィンドウで **ロットの引当** を選択して、注文明細行を引当します。</span><span class="sxs-lookup"><span data-stu-id="be0e2-183">Select **Inventory \> Reservation**, and then, on the Action Pane, select **Reserve lot** to reserve the order line.</span></span>

#### <a name="sales-orders-4-3-and-4-4"></a><span data-ttu-id="be0e2-184">販売注文 4-3 と 4-4</span><span class="sxs-lookup"><span data-stu-id="be0e2-184">Sales orders 4-3 and 4-4</span></span>

1. <span data-ttu-id="be0e2-185">以下の設定で 2 つの同一の販売注文を作成します:</span><span class="sxs-lookup"><span data-stu-id="be0e2-185">Create two identical sales orders that have the following settings:</span></span>

    - <span data-ttu-id="be0e2-186">**顧客アカウント:** *US-004*</span><span class="sxs-lookup"><span data-stu-id="be0e2-186">**Customer account:** *US-004*</span></span>

1. <span data-ttu-id="be0e2-187">以下の設定で注文明細行を追加します:</span><span class="sxs-lookup"><span data-stu-id="be0e2-187">Add an order line that has the following settings:</span></span>

    - <span data-ttu-id="be0e2-188">**品目番号 :** *A0001* (**コード 4** フィルタが割り当てられていない品目)</span><span class="sxs-lookup"><span data-stu-id="be0e2-188">**Item number:** *A0001* (an item that no **Code 4** filter is assigned to)</span></span>
    - <span data-ttu-id="be0e2-189">**数量:** *1.00*</span><span class="sxs-lookup"><span data-stu-id="be0e2-189">**Quantity:** *1.00*</span></span>

1. <span data-ttu-id="be0e2-190">**在庫 \> 引当** を選択し、アクションウ ィンドウで **ロットの引当** を選択して、注文明細行を引当します。</span><span class="sxs-lookup"><span data-stu-id="be0e2-190">Select **Inventory \> Reservation**, and then, on the Action Pane, select **Reserve lot** to reserve the order line.</span></span>

#### <a name="sales-orders-4-5-and-4-6"></a><span data-ttu-id="be0e2-191">販売注文 4-5 と 4-6</span><span class="sxs-lookup"><span data-stu-id="be0e2-191">Sales orders 4-5 and 4-6</span></span>

1. <span data-ttu-id="be0e2-192">以下の設定で 2 つの同一の販売注文を作成します:</span><span class="sxs-lookup"><span data-stu-id="be0e2-192">Create two identical sales orders that have the following settings:</span></span>

    - <span data-ttu-id="be0e2-193">**顧客アカウント:** *US-007*</span><span class="sxs-lookup"><span data-stu-id="be0e2-193">**Customer account:** *US-007*</span></span>
    - <span data-ttu-id="be0e2-194">**サイト:** *6*</span><span class="sxs-lookup"><span data-stu-id="be0e2-194">**Site:** *6*</span></span>
    - <span data-ttu-id="be0e2-195">**倉庫:** *61*</span><span class="sxs-lookup"><span data-stu-id="be0e2-195">**Warehouse:** *61*</span></span>
    - <span data-ttu-id="be0e2-196">**プール :** *ShipCons*</span><span class="sxs-lookup"><span data-stu-id="be0e2-196">**Pool:** *ShipCons*</span></span>

1. <span data-ttu-id="be0e2-197">以下の設定で注文明細行を追加します:</span><span class="sxs-lookup"><span data-stu-id="be0e2-197">Add an order line that has the following settings:</span></span>

    - <span data-ttu-id="be0e2-198">**品目番号 :** *A0001* (**コード 4** フィルタが割り当てられていない品目)</span><span class="sxs-lookup"><span data-stu-id="be0e2-198">**Item number:** *A0001* (an item that no **Code 4** filter is assigned to)</span></span>
    - <span data-ttu-id="be0e2-199">**数量:** *1.00*</span><span class="sxs-lookup"><span data-stu-id="be0e2-199">**Quantity:** *1.00*</span></span>

1. <span data-ttu-id="be0e2-200">**在庫 \> 引当** を選択し、アクションウ ィンドウで **ロットの引当** を選択して、注文明細行を引当します。</span><span class="sxs-lookup"><span data-stu-id="be0e2-200">Select **Inventory \> Reservation**, and then, on the Action Pane, select **Reserve lot** to reserve the order line.</span></span>

#### <a name="sales-orders-4-7-and-4-8"></a><span data-ttu-id="be0e2-201">販売注文 4-7 と 4-8</span><span class="sxs-lookup"><span data-stu-id="be0e2-201">Sales orders 4-7 and 4-8</span></span>

1. <span data-ttu-id="be0e2-202">以下の設定で 2 つの同一の販売注文を作成します:</span><span class="sxs-lookup"><span data-stu-id="be0e2-202">Create two identical sales orders that have the following settings:</span></span>

    - <span data-ttu-id="be0e2-203">**顧客アカウント:** *US-007*</span><span class="sxs-lookup"><span data-stu-id="be0e2-203">**Customer account:** *US-007*</span></span>
    - <span data-ttu-id="be0e2-204">**サイト:** *6*</span><span class="sxs-lookup"><span data-stu-id="be0e2-204">**Site:** *6*</span></span>
    - <span data-ttu-id="be0e2-205">**倉庫:** *61*</span><span class="sxs-lookup"><span data-stu-id="be0e2-205">**Warehouse:** *61*</span></span>
    - <span data-ttu-id="be0e2-206">**プール :** このフィールドは空白のままにします。</span><span class="sxs-lookup"><span data-stu-id="be0e2-206">**Pool:** Leave this field blank.</span></span>

1. <span data-ttu-id="be0e2-207">以下の設定で注文明細行を追加します:</span><span class="sxs-lookup"><span data-stu-id="be0e2-207">Add an order line that has the following settings:</span></span>

    - <span data-ttu-id="be0e2-208">**品目番号 :** *A0001* (**コード 4** フィルタが割り当てられていない品目)</span><span class="sxs-lookup"><span data-stu-id="be0e2-208">**Item number:** *A0001* (an item that no **Code 4** filter is assigned to)</span></span>
    - <span data-ttu-id="be0e2-209">**数量:** *1.00*</span><span class="sxs-lookup"><span data-stu-id="be0e2-209">**Quantity:** *1.00*</span></span>

1. <span data-ttu-id="be0e2-210">**在庫 \> 引当** を選択し、アクションウ ィンドウで **ロットの引当** を選択して、注文明細行を引当します。</span><span class="sxs-lookup"><span data-stu-id="be0e2-210">Select **Inventory \> Reservation**, and then, on the Action Pane, select **Reserve lot** to reserve the order line.</span></span>

## <a name="use-the-load-planning-workbench-to-create-loads-and-release-them-to-the-warehouse"></a><span data-ttu-id="be0e2-211">積荷計画ワークベンチを使用して積荷を作成し、倉庫にリリースする</span><span class="sxs-lookup"><span data-stu-id="be0e2-211">Use the load planning workbench to create loads and release them to the warehouse</span></span>

<span data-ttu-id="be0e2-212">このシナリオで作成した各注文セットに対して積荷を作成し、それを倉庫にリリースするには、次の手順に従います。</span><span class="sxs-lookup"><span data-stu-id="be0e2-212">Follow these steps to create a load for each order set that you created for this scenario and then release it to the warehouse.</span></span>

1. <span data-ttu-id="be0e2-213">**倉庫管理 \> 積荷 \> 積荷計画ワークベンチ** に移動します。</span><span class="sxs-lookup"><span data-stu-id="be0e2-213">Go to **Warehouse management \> Loads \> Load planning workbench**.</span></span>
1. <span data-ttu-id="be0e2-214">**販売明細** タブで、このシナリオに対して作成した注文セットの1つから、すべての販売注文明細行を検索して選択します。</span><span class="sxs-lookup"><span data-stu-id="be0e2-214">On the **Sales lines** tab, find and select all the sales order lines from one of the order sets that you created for this scenario.</span></span>
1. <span data-ttu-id="be0e2-215">アクション ウィンドウの **供給と需要** タブで、**追加 \> 新規積荷** を選択して、選択した注文明細行を新しい積荷に追加します。</span><span class="sxs-lookup"><span data-stu-id="be0e2-215">On the Action Pane, on the **Supply and demand** tab, select **Add \> To new load** to add the selected order lines to a new Load.</span></span>
1. <span data-ttu-id="be0e2-216">**積荷のテンプレート割り当て** ダイアログ ボックスの **積荷のテンプレート ID** フィールドで、*Stnd load template* などの積荷テンプレートを選択します。</span><span class="sxs-lookup"><span data-stu-id="be0e2-216">In the **Load template assignment** dialog box, in the **Load template ID** field, select a load template, such as *Stnd Load Template*.</span></span>
1. <span data-ttu-id="be0e2-217">**OK** を選択してダイアログ ボックスを閉じます。</span><span class="sxs-lookup"><span data-stu-id="be0e2-217">Select **OK** to close the dialog box.</span></span> 
1. <span data-ttu-id="be0e2-218">**積荷** セクションで、作成した積荷を見つけて選択します。</span><span class="sxs-lookup"><span data-stu-id="be0e2-218">In the **Loads** section, find and select the load that you just created.</span></span>
1. <span data-ttu-id="be0e2-219">**リリース \> 倉庫へのリリース** を選択し、選択した積荷を倉庫にリリースします。</span><span class="sxs-lookup"><span data-stu-id="be0e2-219">Select **Release \> Release to warehouse** to release the selected load to the warehouse.</span></span>
1. <span data-ttu-id="be0e2-220">このシナリオに対して作成した他の 3 つの注文セットに対して、この手順を繰り返します。</span><span class="sxs-lookup"><span data-stu-id="be0e2-220">Repeat this procedure for the other three order sets that you created for this scenario.</span></span>

## <a name="verify-the-shipments"></a><span data-ttu-id="be0e2-221">出荷の確認</span><span class="sxs-lookup"><span data-stu-id="be0e2-221">Verify the shipments</span></span>

<span data-ttu-id="be0e2-222">次の手順では、出荷連結の結果として作成、更新された出荷を確認できます。</span><span class="sxs-lookup"><span data-stu-id="be0e2-222">The following procedure lets you verify the shipments that have been created or updated as a result of shipment consolidation.</span></span> <span data-ttu-id="be0e2-223">これを使用して、このシナリオで作成した各注文セットを確認します。続いてその結果が得られるかどうかを確認するには、次のセクションを確認します。</span><span class="sxs-lookup"><span data-stu-id="be0e2-223">Use it to review each order set that you created for this scenario, and then review the subsections that follow to make sure that you've obtained the expected results.</span></span>

1. <span data-ttu-id="be0e2-224">**倉庫管理 \> 出荷 \> すべての出荷** に移動します。</span><span class="sxs-lookup"><span data-stu-id="be0e2-224">Go to **Warehouse management \> Shipments \> All shipments**.</span></span>
1. <span data-ttu-id="be0e2-225">必要な出荷を検索して選択します。</span><span class="sxs-lookup"><span data-stu-id="be0e2-225">Find and select the required shipment.</span></span>
1. <span data-ttu-id="be0e2-226">出荷の作成時または更新時に連結ポリシーが使用されていた場合は、**出荷連結ポリシー** フィールドに表示する必要があります。</span><span class="sxs-lookup"><span data-stu-id="be0e2-226">If a consolidation policy was used when the shipment was created or updated, you should see it in the **Shipment consolidation policy** field.</span></span>

### <a name="release-order-set-1-in-one-load"></a><span data-ttu-id="be0e2-227">ひとつの積荷で注文セット 1 をリリースする</span><span class="sxs-lookup"><span data-stu-id="be0e2-227">Release order set 1 in one load</span></span>

<span data-ttu-id="be0e2-228">次の 2 つの出荷が作成されている必要があります:</span><span class="sxs-lookup"><span data-stu-id="be0e2-228">Two shipments should have been created:</span></span>

- <span data-ttu-id="be0e2-229">最初の出荷は、*顧客モード* の出荷連結ポリシーを使用して作成された 3 つの行で構成されます。</span><span class="sxs-lookup"><span data-stu-id="be0e2-229">The first shipment contains three lines and was created by using the *CustomerMode* shipment consolidation policy.</span></span>
- <span data-ttu-id="be0e2-230">2 つ目の出荷は、*航空運賃* 輸送モードの荷渡方法を使用しないもので、顧客注文の *CustomerOrderNo* 連結ポリシーを使用して作成されてい ます。</span><span class="sxs-lookup"><span data-stu-id="be0e2-230">The second shipment, which doesn't use the *Airways* transportation mode of delivery, was created by using the *CustomerOrderNo* shipment consolidation policy.</span></span>

### <a name="release-order-set-2-in-one-load"></a><span data-ttu-id="be0e2-231">ひとつの積荷で注文セット 2 をリリースする</span><span class="sxs-lookup"><span data-stu-id="be0e2-231">Release order set 2 in one load</span></span>

<span data-ttu-id="be0e2-232">次の 3 つの出荷が作成されている必要があります:</span><span class="sxs-lookup"><span data-stu-id="be0e2-232">Three shipments should have been created:</span></span>

- <span data-ttu-id="be0e2-233">最初の出荷には、 *可燃性* の品目が含まれています。</span><span class="sxs-lookup"><span data-stu-id="be0e2-233">The first shipment contains the *Flammable* items.</span></span>
- <span data-ttu-id="be0e2-234">他の 2 つの出荷には、*爆発性* の品目を含む 1 つの行が含まれてい ます。</span><span class="sxs-lookup"><span data-stu-id="be0e2-234">Each of the other two shipments contains one line that has the *Explosive* item.</span></span>

### <a name="release-order-set-3-in-one-load"></a><span data-ttu-id="be0e2-235">ひとつの積荷で注文セット 3 をリリースする</span><span class="sxs-lookup"><span data-stu-id="be0e2-235">Release order set 3 in one load</span></span>

<span data-ttu-id="be0e2-236">次の 2 つの出荷が作成されている必要があります:</span><span class="sxs-lookup"><span data-stu-id="be0e2-236">Two shipments should have been created:</span></span>

- <span data-ttu-id="be0e2-237">1つ目の出荷には、**顧客要求** フィールドが *1* に設定されている販売注文の注文明細行が含まれます。</span><span class="sxs-lookup"><span data-stu-id="be0e2-237">The first shipment contains order lines from the sales order where the **Customer requisition** field is set to *1*.</span></span>
- <span data-ttu-id="be0e2-238">2つ目の出荷には、**顧客要求** フィールドが *2* に設定されている販売注文の注文明細行が含まれます。</span><span class="sxs-lookup"><span data-stu-id="be0e2-238">The second shipment contains order lines from sales order where the **Customer requisition** field is set to *2*.</span></span>

### <a name="release-order-set-4-in-one-load"></a><span data-ttu-id="be0e2-239">ひとつの積荷で注文セット 4 をリリースする</span><span class="sxs-lookup"><span data-stu-id="be0e2-239">Release order set 4 in one load</span></span>

<span data-ttu-id="be0e2-240">次の 4 つの出荷が作成されている必要があります:</span><span class="sxs-lookup"><span data-stu-id="be0e2-240">Four shipments should have been created:</span></span>

- <span data-ttu-id="be0e2-241">顧客アカウント *US-003* の 2 件の販売注文の明細行は、*注文プール* の出荷連結ポリシーを使用して 1 つの出荷にグループ化されています。</span><span class="sxs-lookup"><span data-stu-id="be0e2-241">Lines from two orders for customer account *US-003* were grouped into one shipment by using the *Order pool* shipment consolidation policy.</span></span>
- <span data-ttu-id="be0e2-242">顧客アカウント *US-004* の 2 件の販売注文の明細行は、*注文プール* の出荷連結ポリシーを使用して 1 つの出荷にグループ化されています。</span><span class="sxs-lookup"><span data-stu-id="be0e2-242">Lines from two orders for customer account *US-004* were grouped into one shipment by using the *Order pool* shipment consolidation policy.</span></span>
- <span data-ttu-id="be0e2-243">顧客アカウント *US-007* の販売注文 4-5 および 4-6 の明細行は、*注文プール* の出荷連結ポリシーを使用して1つの出荷にグループ化されています。</span><span class="sxs-lookup"><span data-stu-id="be0e2-243">Lines from sales orders 4-5 and 4-6 for customer account *US-007* were grouped into one shipment by using the *Order pool* shipment consolidation policy.</span></span>
- <span data-ttu-id="be0e2-244">顧客アカウント *US-007* の販売注文 4-7 および 4-8 の明細行は、*クロスオーダー* の出荷連結ポリシーを使用して1つの出荷にグループ化されています。</span><span class="sxs-lookup"><span data-stu-id="be0e2-244">Lines from sales orders 4-7 and 4-8 for customer account *US-007* were grouped into one shipment by using the *CrossOrder* shipment consolidation policy.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="be0e2-245">追加リソース</span><span class="sxs-lookup"><span data-stu-id="be0e2-245">Additional resources</span></span>

- [<span data-ttu-id="be0e2-246">出荷連結ポリシー</span><span class="sxs-lookup"><span data-stu-id="be0e2-246">Shipment consolidation policies</span></span>](about-shipment-consolidation-policies.md)
- [<span data-ttu-id="be0e2-247">出荷連結ポリシーを構成する</span><span class="sxs-lookup"><span data-stu-id="be0e2-247">Configure shipment consolidation policies</span></span>](configure-shipment-consolidation-policies.md)
