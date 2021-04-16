---
title: 販売注文の自動リリースを使用して倉庫にリリースされた出荷を連結する
description: このトピックでは、定期的に自動実行される [倉庫へのリリース] 手順内で、複数の注文が倉庫にリリースされたシナリオを示します。
author: GarmMSFT
ms.date: 05/12/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: WHSShipConsolidationPolicy, WHSShipConsolidationWorkbench, WHSFilterGroupTable, WHSShipmentConsolidation, WHSFilterGenerallyAvail
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: kamaybac
ms.search.validFrom: 2020-05-01
ms.dyn365.ops.version: 10.0.3
ms.openlocfilehash: 82a95ecf196ef7c33831da7f4d03df629b17fa53
ms.sourcegitcommit: 0e8db169c3f90bd750826af76709ef5d621fd377
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/01/2021
ms.locfileid: "5807563"
---
# <a name="consolidate-shipments-when-they-are-released-to-the-warehouse-by-using-automatic-release-of-sales-orders"></a><span data-ttu-id="9de5b-103">販売注文の自動リリースを使用して倉庫にリリースされた出荷を連結する</span><span class="sxs-lookup"><span data-stu-id="9de5b-103">Consolidate shipments when they are released to the warehouse by using Automatic release of sales orders</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="9de5b-104">このトピックでは、定期的に自動実行される [倉庫へのリリース] 手順内で、複数の注文が倉庫にリリースされたシナリオを示します。</span><span class="sxs-lookup"><span data-stu-id="9de5b-104">This topic presents a scenario where multiple orders are released to the warehouse in the same automated release-to-warehouse periodic procedure.</span></span> <span data-ttu-id="9de5b-105">注文は、出荷連結ポリシーとして定義されているルールに基づいて自動的に出荷に連結されます。</span><span class="sxs-lookup"><span data-stu-id="9de5b-105">The orders will automatically be consolidated into shipments, based on rules that are defined as shipment consolidation policies.</span></span>

<span data-ttu-id="9de5b-106">このシナリオでは、販売注文のセットを作成し、各セットを倉庫にリリースします。</span><span class="sxs-lookup"><span data-stu-id="9de5b-106">During the scenario, you will create sets of sales orders and release each set to the warehouse.</span></span> <span data-ttu-id="9de5b-107">次に、出荷連結の際に作成または更新された出荷を、構成されたポリシーに基づいて確認します。</span><span class="sxs-lookup"><span data-stu-id="9de5b-107">You will then review the shipments that are created or updated during shipment consolidation, based on the configured policies.</span></span>

## <a name="make-demo-data-available"></a><span data-ttu-id="9de5b-108">デモ データを有効化する</span><span class="sxs-lookup"><span data-stu-id="9de5b-108">Make demo data available</span></span>

<span data-ttu-id="9de5b-109">このトピックのシナリオでは、Microsoft Dynamics 365 Supply Chain Management にて用意されている標準のデモデータに含まれる値とレコードを参照し ます。</span><span class="sxs-lookup"><span data-stu-id="9de5b-109">The scenario in this topic references values and records that are included in the standard demo data that is provided for Microsoft Dynamics 365 Supply Chain Management.</span></span> <span data-ttu-id="9de5b-110">ここで提供されている値を使用するには、デモデータがインストールされている環境で作業し、開始する前に法人を **usmf** に設定します。</span><span class="sxs-lookup"><span data-stu-id="9de5b-110">If you want to use the values that are provided here as you do the exercises, be sure to work in an environment where the demo data is installed, and set the legal entity to **USMF** before you begin.</span></span>

## <a name="set-up-shipment-consolidation-policies-and-product-filters"></a><span data-ttu-id="9de5b-111">出荷連結ポリシーおよび製品フィルタの設定</span><span class="sxs-lookup"><span data-stu-id="9de5b-111">Set up shipment consolidation policies and product filters</span></span>

<span data-ttu-id="9de5b-112">このシナリオでは、既にこの機能を有効にし、[出荷連結ポリシーの構成](configure-shipment-consolidation-policies.md)内の実習を完了しており、同ページ内に記述されているポリシーとその他のレコードを作成していることを前提としています。</span><span class="sxs-lookup"><span data-stu-id="9de5b-112">The scenario that is described here assumes that you've already turned on the feature, done the exercises in [Configure shipment consolidation policies](configure-shipment-consolidation-policies.md), and created the policies and other records that are described there.</span></span> <span data-ttu-id="9de5b-113">このシナリオを続行する前に、この演習を行っている必要があります。</span><span class="sxs-lookup"><span data-stu-id="9de5b-113">Be sure to do those exercises before you continue with this scenario.</span></span>

## <a name="create-the-sales-orders-for-this-scenario"></a><span data-ttu-id="9de5b-114">このシナリオで使用する販売注文の作成</span><span class="sxs-lookup"><span data-stu-id="9de5b-114">Create the sales orders for this scenario</span></span>

<span data-ttu-id="9de5b-115">シナリオで使用する一連の販売注文を作成することから始めます。</span><span class="sxs-lookup"><span data-stu-id="9de5b-115">Start by creating a collection of sales orders that you can work with.</span></span> <span data-ttu-id="9de5b-116">高度な倉庫 (WMS) プロセスが利用できる倉庫を使用する必要があります。</span><span class="sxs-lookup"><span data-stu-id="9de5b-116">You must work with a warehouse that is enabled for advanced warehouse (WMS) processes.</span></span> <span data-ttu-id="9de5b-117">他の倉庫を明示的に指定していない場合は、次の注文セットのそれぞれに対して同じ倉庫が使用されなければなりません。</span><span class="sxs-lookup"><span data-stu-id="9de5b-117">Unless a different warehouse is explicitly mentioned, that same warehouse must be used for each of the following sets of orders.</span></span>

<span data-ttu-id="9de5b-118">**売掛金勘定  \> 注文 \> すべての販売注文** に移動し、次のサブセクションで説明されている設定を含む販売注文のコレクションを作成します。</span><span class="sxs-lookup"><span data-stu-id="9de5b-118">Go to **Accounts receivable \> Orders \> All sales orders**, and create a collection of sales orders that have the settings that are described in the following subsections.</span></span>

### <a name="create-order-set-1"></a><span data-ttu-id="9de5b-119">注文セット 1 を作成する</span><span class="sxs-lookup"><span data-stu-id="9de5b-119">Create order set 1</span></span>

#### <a name="sales-order-1-1"></a><span data-ttu-id="9de5b-120">販売注文 1-1</span><span class="sxs-lookup"><span data-stu-id="9de5b-120">Sales order 1-1</span></span>

1. <span data-ttu-id="9de5b-121">以下の設定で販売注文を作成します:</span><span class="sxs-lookup"><span data-stu-id="9de5b-121">Create a sales order that has the following settings:</span></span>

    - <span data-ttu-id="9de5b-122">**顧客アカウント:** *US-001*</span><span class="sxs-lookup"><span data-stu-id="9de5b-122">**Customer account:** *US-001*</span></span>
    - <span data-ttu-id="9de5b-123">**荷渡方法:** *Airwa-Air*</span><span class="sxs-lookup"><span data-stu-id="9de5b-123">**Mode of delivery:** *Airwa-Air*</span></span>

1. <span data-ttu-id="9de5b-124">以下の設定で注文明細行を追加します:</span><span class="sxs-lookup"><span data-stu-id="9de5b-124">Add an order line that has the following settings:</span></span>

    - <span data-ttu-id="9de5b-125">**品目番号 :** *A0001* (**コード 4** フィルタが割り当てられていない品目)</span><span class="sxs-lookup"><span data-stu-id="9de5b-125">**Item number:** *A0001* (an item that no **Code 4** filter is assigned to)</span></span>
    - <span data-ttu-id="9de5b-126">**数量:** *1.00*</span><span class="sxs-lookup"><span data-stu-id="9de5b-126">**Quantity:** *1.00*</span></span>

#### <a name="sales-order-1-2"></a><span data-ttu-id="9de5b-127">販売注文 1-2</span><span class="sxs-lookup"><span data-stu-id="9de5b-127">Sales order 1-2</span></span>

1. <span data-ttu-id="9de5b-128">以下の設定で販売注文を作成します:</span><span class="sxs-lookup"><span data-stu-id="9de5b-128">Create a sales order that has the following settings:</span></span>

    - <span data-ttu-id="9de5b-129">**顧客アカウント:** *US-001*</span><span class="sxs-lookup"><span data-stu-id="9de5b-129">**Customer account:** *US-001*</span></span>
    - <span data-ttu-id="9de5b-130">**荷渡方法:** *Airwa-Air*</span><span class="sxs-lookup"><span data-stu-id="9de5b-130">**Mode of delivery:** *Airwa-Air*</span></span>

1. <span data-ttu-id="9de5b-131">以下の設定で注文明細行を追加します:</span><span class="sxs-lookup"><span data-stu-id="9de5b-131">Add an order line that has the following settings:</span></span>

    - <span data-ttu-id="9de5b-132">**品目番号 :** *A0001* (**コード 4** フィルタが割り当てられていない品目)</span><span class="sxs-lookup"><span data-stu-id="9de5b-132">**Item number:** *A0001* (an item that no **Code 4** filter is assigned to)</span></span>
    - <span data-ttu-id="9de5b-133">**数量:** *1.00*</span><span class="sxs-lookup"><span data-stu-id="9de5b-133">**Quantity:** *1.00*</span></span>

#### <a name="sales-order-1-3"></a><span data-ttu-id="9de5b-134">販売注文 1-3</span><span class="sxs-lookup"><span data-stu-id="9de5b-134">Sales order 1-3</span></span>

1. <span data-ttu-id="9de5b-135">以下の設定で販売注文を作成します:</span><span class="sxs-lookup"><span data-stu-id="9de5b-135">Create a sales order that has the following settings:</span></span>

    - <span data-ttu-id="9de5b-136">**顧客アカウント:** *US-001*</span><span class="sxs-lookup"><span data-stu-id="9de5b-136">**Customer account:** *US-001*</span></span>
    - <span data-ttu-id="9de5b-137">**荷渡方法:** *10*</span><span class="sxs-lookup"><span data-stu-id="9de5b-137">**Mode of delivery:** *10*</span></span>

1. <span data-ttu-id="9de5b-138">以下の設定で注文明細行を追加します:</span><span class="sxs-lookup"><span data-stu-id="9de5b-138">Add an order line that has the following settings:</span></span>

    - <span data-ttu-id="9de5b-139">**品目番号 :** *A0001* (**コード 4** フィルタが割り当てられていない品目)</span><span class="sxs-lookup"><span data-stu-id="9de5b-139">**Item number:** *A0001* (an item that no **Code 4** filter is assigned to)</span></span>
    - <span data-ttu-id="9de5b-140">**数量:** *1.00*</span><span class="sxs-lookup"><span data-stu-id="9de5b-140">**Quantity:** *1.00*</span></span>

1. <span data-ttu-id="9de5b-141">以下の設定で 2 つ目の販売注文を作成します:</span><span class="sxs-lookup"><span data-stu-id="9de5b-141">Add a second order line that has the following settings:</span></span>

    - <span data-ttu-id="9de5b-142">**品目番号 :** *A0002* ( **コード 4** フィルタが割り当てられていない品目)</span><span class="sxs-lookup"><span data-stu-id="9de5b-142">**Item number:** *A0002* (an item that no **Code 4** filter is assigned to)</span></span>
    - <span data-ttu-id="9de5b-143">**数量:** *1.00*</span><span class="sxs-lookup"><span data-stu-id="9de5b-143">**Quantity:** *1.00*</span></span>
    - <span data-ttu-id="9de5b-144">**荷渡方法:** *Airwa-Air*</span><span class="sxs-lookup"><span data-stu-id="9de5b-144">**Mode of delivery:** *Airwa-Air*</span></span>

### <a name="create-order-set-2"></a><span data-ttu-id="9de5b-145">注文セット 2 を作成する</span><span class="sxs-lookup"><span data-stu-id="9de5b-145">Create order set 2</span></span>

#### <a name="sales-orders-2-1-and-2-2"></a><span data-ttu-id="9de5b-146">販売注文 2-1 と 2-2</span><span class="sxs-lookup"><span data-stu-id="9de5b-146">Sales orders 2-1 and 2-2</span></span>

1. <span data-ttu-id="9de5b-147">以下の設定で 2 つの同一の販売注文を作成します:</span><span class="sxs-lookup"><span data-stu-id="9de5b-147">Create two identical sales orders that have the following settings:</span></span>

    - <span data-ttu-id="9de5b-148">**顧客アカウント:** *US-002*</span><span class="sxs-lookup"><span data-stu-id="9de5b-148">**Customer account:** *US-002*</span></span>

1. <span data-ttu-id="9de5b-149">以下の設定で注文明細行を追加します:</span><span class="sxs-lookup"><span data-stu-id="9de5b-149">Add an order line that has the following settings:</span></span>

    - <span data-ttu-id="9de5b-150">**品目番号 :** *M9200* (**コード 4** のフィルタが *可燃性* に設定されている品目)</span><span class="sxs-lookup"><span data-stu-id="9de5b-150">**Item number:** *M9200* (an item where the **Code 4** filter is set to *Flammable*)</span></span>
    - <span data-ttu-id="9de5b-151">**数量:** *1.00*</span><span class="sxs-lookup"><span data-stu-id="9de5b-151">**Quantity:** *1.00*</span></span>

1. <span data-ttu-id="9de5b-152">以下の設定で 2 つ目の販売注文を作成します:</span><span class="sxs-lookup"><span data-stu-id="9de5b-152">Add a second order line that has the following settings:</span></span>

    - <span data-ttu-id="9de5b-153">**品目番号 :** *M9201*( **コード 4** のフィルタが *爆発物* に設定されている品目)</span><span class="sxs-lookup"><span data-stu-id="9de5b-153">**Item number:** *M9201* (an item where the **Code 4** filter is set to *Explosive*)</span></span>
    - <span data-ttu-id="9de5b-154">**数量:** *1.00*</span><span class="sxs-lookup"><span data-stu-id="9de5b-154">**Quantity:** *1.00*</span></span>
    - <span data-ttu-id="9de5b-155">**荷渡方法:** *Airwa-Air*</span><span class="sxs-lookup"><span data-stu-id="9de5b-155">**Mode of delivery:** *Airwa-Air*</span></span>

### <a name="create-order-set-3"></a><span data-ttu-id="9de5b-156">注文セット 3 を作成する</span><span class="sxs-lookup"><span data-stu-id="9de5b-156">Create order set 3</span></span>

#### <a name="sales-order-3-1"></a><span data-ttu-id="9de5b-157">販売注文 3-1</span><span class="sxs-lookup"><span data-stu-id="9de5b-157">Sales order 3-1</span></span>

1. <span data-ttu-id="9de5b-158">以下の設定で販売注文を作成します:</span><span class="sxs-lookup"><span data-stu-id="9de5b-158">Create a sales order that has the following settings:</span></span>

    - <span data-ttu-id="9de5b-159">**顧客アカウント:** *US-002*</span><span class="sxs-lookup"><span data-stu-id="9de5b-159">**Customer account:** *US-002*</span></span>

1. <span data-ttu-id="9de5b-160">以下の設定で注文明細行を追加します:</span><span class="sxs-lookup"><span data-stu-id="9de5b-160">Add an order line that has the following settings:</span></span>

    - <span data-ttu-id="9de5b-161">**品目番号 :** *M9200* (**コード 4** のフィルタが *可燃性* に設定されている品目)</span><span class="sxs-lookup"><span data-stu-id="9de5b-161">**Item number:** *M9200* (an item where the **Code 4** filter is set to *Flammable*)</span></span>
    - <span data-ttu-id="9de5b-162">**数量:** *1.00*</span><span class="sxs-lookup"><span data-stu-id="9de5b-162">**Quantity:** *1.00*</span></span>

1. <span data-ttu-id="9de5b-163">以下の設定で 2 つ目の販売注文を作成します:</span><span class="sxs-lookup"><span data-stu-id="9de5b-163">Add a second order line that has the following settings:</span></span>

    - <span data-ttu-id="9de5b-164">**品目番号 :** *M9201*( **コード 4** のフィルタが *爆発物* に設定されている品目)</span><span class="sxs-lookup"><span data-stu-id="9de5b-164">**Item number:** *M9201* (an item where the **Code 4** filter is set to *Explosive*)</span></span>
    - <span data-ttu-id="9de5b-165">**数量:** *1.00*</span><span class="sxs-lookup"><span data-stu-id="9de5b-165">**Quantity:** *1.00*</span></span>
    - <span data-ttu-id="9de5b-166">**荷渡方法:** *Airwa-Air*</span><span class="sxs-lookup"><span data-stu-id="9de5b-166">**Mode of delivery:** *Airwa-Air*</span></span>

> [!NOTE]
> <span data-ttu-id="9de5b-167">この注文は、注文セット 2 で作成した 2 つの注文と同じものです。</span><span class="sxs-lookup"><span data-stu-id="9de5b-167">This order is identical to the two orders that you created for order set 2.</span></span> <span data-ttu-id="9de5b-168">ただし、このシナリオでは後に別途リリースするため、独自のオーダー セットとして記載しています。</span><span class="sxs-lookup"><span data-stu-id="9de5b-168">However, it's listed as its own order set because you will release it separately later in this scenario.</span></span>

### <a name="create-order-set-4"></a><span data-ttu-id="9de5b-169">注文セット 4 を作成する</span><span class="sxs-lookup"><span data-stu-id="9de5b-169">Create order set 4</span></span>

#### <a name="sales-order-4-1"></a><span data-ttu-id="9de5b-170">販売注文 4-1</span><span class="sxs-lookup"><span data-stu-id="9de5b-170">Sales order 4-1</span></span>

1. <span data-ttu-id="9de5b-171">以下の設定で販売注文を作成します:</span><span class="sxs-lookup"><span data-stu-id="9de5b-171">Create a sales order that has the following settings:</span></span>

    - <span data-ttu-id="9de5b-172">**顧客アカウント:** *US-001*</span><span class="sxs-lookup"><span data-stu-id="9de5b-172">**Customer account:** *US-001*</span></span>
    - <span data-ttu-id="9de5b-173">**顧客の要求:** *1*</span><span class="sxs-lookup"><span data-stu-id="9de5b-173">**Customer requisition:** *1*</span></span>

1. <span data-ttu-id="9de5b-174">以下の設定で注文明細行を追加します:</span><span class="sxs-lookup"><span data-stu-id="9de5b-174">Add an order line that has the following settings:</span></span>

    - <span data-ttu-id="9de5b-175">**品目番号 :** *A0001* (**コード 4** フィルタが割り当てられていない品目)</span><span class="sxs-lookup"><span data-stu-id="9de5b-175">**Item number:** *A0001* (an item that no **Code 4** filter is assigned to)</span></span>
    - <span data-ttu-id="9de5b-176">**数量:** *1.00*</span><span class="sxs-lookup"><span data-stu-id="9de5b-176">**Quantity:** *1.00*</span></span>

### <a name="create-order-set-5"></a><span data-ttu-id="9de5b-177">注文セット 5 を作成する</span><span class="sxs-lookup"><span data-stu-id="9de5b-177">Create order set 5</span></span>

#### <a name="sales-orders-5-1-and-5-2"></a><span data-ttu-id="9de5b-178">販売注文 5-1 と 5-2</span><span class="sxs-lookup"><span data-stu-id="9de5b-178">Sales orders 5-1 and 5-2</span></span>

1. <span data-ttu-id="9de5b-179">以下の設定で 2 つの同一の販売注文を作成します:</span><span class="sxs-lookup"><span data-stu-id="9de5b-179">Create two identical sales orders that have the following settings:</span></span>

    - <span data-ttu-id="9de5b-180">**顧客アカウント:** *US-001*</span><span class="sxs-lookup"><span data-stu-id="9de5b-180">**Customer account:** *US-001*</span></span>
    - <span data-ttu-id="9de5b-181">**顧客の要求:** *2*</span><span class="sxs-lookup"><span data-stu-id="9de5b-181">**Customer requisition:** *2*</span></span>

1. <span data-ttu-id="9de5b-182">以下の設定で注文明細行を追加します:</span><span class="sxs-lookup"><span data-stu-id="9de5b-182">Add an order line that has the following settings:</span></span>

    - <span data-ttu-id="9de5b-183">**品目番号 :** *A0001* (**コード 4** フィルタが割り当てられていない品目)</span><span class="sxs-lookup"><span data-stu-id="9de5b-183">**Item number:** *A0001* (an item that no **Code 4** filter is assigned to)</span></span>
    - <span data-ttu-id="9de5b-184">**数量:** *1.00*</span><span class="sxs-lookup"><span data-stu-id="9de5b-184">**Quantity:** *1.00*</span></span>

#### <a name="sales-order-5-3"></a><span data-ttu-id="9de5b-185">販売注文 5-3</span><span class="sxs-lookup"><span data-stu-id="9de5b-185">Sales order 5-3</span></span>

1. <span data-ttu-id="9de5b-186">以下の設定で販売注文を作成します:</span><span class="sxs-lookup"><span data-stu-id="9de5b-186">Create a sales order that has the following settings:</span></span>

    - <span data-ttu-id="9de5b-187">**顧客アカウント:** *US-001*</span><span class="sxs-lookup"><span data-stu-id="9de5b-187">**Customer account:** *US-001*</span></span>
    - <span data-ttu-id="9de5b-188">**顧客の要求:** *1*</span><span class="sxs-lookup"><span data-stu-id="9de5b-188">**Customer requisition:** *1*</span></span>

1. <span data-ttu-id="9de5b-189">以下の設定で注文明細行を追加します:</span><span class="sxs-lookup"><span data-stu-id="9de5b-189">Add an order line that has the following settings:</span></span>

    - <span data-ttu-id="9de5b-190">**品目番号 :** *A0001* (**コード 4** フィルタが割り当てられていない品目)</span><span class="sxs-lookup"><span data-stu-id="9de5b-190">**Item number:** *A0001* (an item that no **Code 4** filter is assigned to)</span></span>
    - <span data-ttu-id="9de5b-191">**数量:** *1.00*</span><span class="sxs-lookup"><span data-stu-id="9de5b-191">**Quantity:** *1.00*</span></span>

### <a name="create-order-set-6"></a><span data-ttu-id="9de5b-192">注文セット 6 を作成する</span><span class="sxs-lookup"><span data-stu-id="9de5b-192">Create order set 6</span></span>

#### <a name="sales-orders-6-1-and-6-2"></a><span data-ttu-id="9de5b-193">販売注文 6-1 と 6-2</span><span class="sxs-lookup"><span data-stu-id="9de5b-193">Sales orders 6-1 and 6-2</span></span>

1. <span data-ttu-id="9de5b-194">以下の設定で 2 つの同一の販売注文を作成します:</span><span class="sxs-lookup"><span data-stu-id="9de5b-194">Create two identical sales orders that have the following settings:</span></span>

    - <span data-ttu-id="9de5b-195">**顧客アカウント:** *US-003*</span><span class="sxs-lookup"><span data-stu-id="9de5b-195">**Customer account:** *US-003*</span></span>
    - <span data-ttu-id="9de5b-196">**顧客の要求:** *2*</span><span class="sxs-lookup"><span data-stu-id="9de5b-196">**Customer requisition:** *2*</span></span>

1. <span data-ttu-id="9de5b-197">以下の設定で注文明細行を追加します:</span><span class="sxs-lookup"><span data-stu-id="9de5b-197">Add an order line that has the following settings:</span></span>

    - <span data-ttu-id="9de5b-198">**品目番号 :** *A0001* (**コード 4** フィルタが割り当てられていない品目)</span><span class="sxs-lookup"><span data-stu-id="9de5b-198">**Item number:** *A0001* (an item that no **Code 4** filter is assigned to)</span></span>
    - <span data-ttu-id="9de5b-199">**数量:** *1.00*</span><span class="sxs-lookup"><span data-stu-id="9de5b-199">**Quantity:** *1.00*</span></span>

#### <a name="sales-orders-6-3-and-6-4"></a><span data-ttu-id="9de5b-200">販売注文 6-3 と 6-4</span><span class="sxs-lookup"><span data-stu-id="9de5b-200">Sales orders 6-3 and 6-4</span></span>

1. <span data-ttu-id="9de5b-201">以下の設定で 2 つの同一の販売注文を作成します:</span><span class="sxs-lookup"><span data-stu-id="9de5b-201">Create two identical sales orders that have the following settings:</span></span>

    - <span data-ttu-id="9de5b-202">**顧客アカウント:** *US-004*</span><span class="sxs-lookup"><span data-stu-id="9de5b-202">**Customer account:** *US-004*</span></span>
    - <span data-ttu-id="9de5b-203">**顧客の要求:** *1*</span><span class="sxs-lookup"><span data-stu-id="9de5b-203">**Customer requisition:** *1*</span></span>

1. <span data-ttu-id="9de5b-204">以下の設定で注文明細行を追加します:</span><span class="sxs-lookup"><span data-stu-id="9de5b-204">Add an order line that has the following settings:</span></span>

    - <span data-ttu-id="9de5b-205">**品目番号 :** *A0001* (**コード 4** フィルタが割り当てられていない品目)</span><span class="sxs-lookup"><span data-stu-id="9de5b-205">**Item number:** *A0001* (an item that no **Code 4** filter is assigned to)</span></span>
    - <span data-ttu-id="9de5b-206">**数量:** *1.00*</span><span class="sxs-lookup"><span data-stu-id="9de5b-206">**Quantity:** *1.00*</span></span>

#### <a name="sales-orders-6-5-and-6-6"></a><span data-ttu-id="9de5b-207">販売注文 6-5 と 6-6</span><span class="sxs-lookup"><span data-stu-id="9de5b-207">Sales orders 6-5 and 6-6</span></span>

1. <span data-ttu-id="9de5b-208">以下の設定で 2 つの同一の販売注文を作成します:</span><span class="sxs-lookup"><span data-stu-id="9de5b-208">Create two identical sales orders that have the following settings:</span></span>

    - <span data-ttu-id="9de5b-209">**顧客アカウント:** *US-007*</span><span class="sxs-lookup"><span data-stu-id="9de5b-209">**Customer account:** *US-007*</span></span>
    - <span data-ttu-id="9de5b-210">**サイト:** *6*</span><span class="sxs-lookup"><span data-stu-id="9de5b-210">**Site:** *6*</span></span>
    - <span data-ttu-id="9de5b-211">**倉庫:** *61*</span><span class="sxs-lookup"><span data-stu-id="9de5b-211">**Warehouse:** *61*</span></span>
    - <span data-ttu-id="9de5b-212">**プール :** *ShipCons*</span><span class="sxs-lookup"><span data-stu-id="9de5b-212">**Pool:** *ShipCons*</span></span>

1. <span data-ttu-id="9de5b-213">以下の設定で注文明細行を追加します:</span><span class="sxs-lookup"><span data-stu-id="9de5b-213">Add an order line that has the following settings:</span></span>

    - <span data-ttu-id="9de5b-214">**品目番号 :** *A0001* (**コード 4** フィルタが割り当てられていない品目)</span><span class="sxs-lookup"><span data-stu-id="9de5b-214">**Item number:** *A0001* (an item that no **Code 4** filter is assigned to)</span></span>
    - <span data-ttu-id="9de5b-215">**数量:** *1.00*</span><span class="sxs-lookup"><span data-stu-id="9de5b-215">**Quantity:** *1.00*</span></span>

#### <a name="sales-orders-6-7-and-6-8"></a><span data-ttu-id="9de5b-216">販売注文 6-7 と 6-8</span><span class="sxs-lookup"><span data-stu-id="9de5b-216">Sales orders 6-7 and 6-8</span></span>

1. <span data-ttu-id="9de5b-217">以下の設定で 2 つの同一の販売注文を作成します:</span><span class="sxs-lookup"><span data-stu-id="9de5b-217">Create two identical sales orders that have the following settings:</span></span>

    - <span data-ttu-id="9de5b-218">**顧客アカウント:** *US-007*</span><span class="sxs-lookup"><span data-stu-id="9de5b-218">**Customer account:** *US-007*</span></span>
    - <span data-ttu-id="9de5b-219">**サイト:** *6*</span><span class="sxs-lookup"><span data-stu-id="9de5b-219">**Site:** *6*</span></span>
    - <span data-ttu-id="9de5b-220">**倉庫:** *61*</span><span class="sxs-lookup"><span data-stu-id="9de5b-220">**Warehouse:** *61*</span></span>
    - <span data-ttu-id="9de5b-221">**プール :** このフィールドは空白のままにします。</span><span class="sxs-lookup"><span data-stu-id="9de5b-221">**Pool:** Leave this field blank.</span></span>

1. <span data-ttu-id="9de5b-222">以下の設定で注文明細行を追加します:</span><span class="sxs-lookup"><span data-stu-id="9de5b-222">Add an order line that has the following settings:</span></span>

    - <span data-ttu-id="9de5b-223">**品目番号 :** *A0001* (**コード 4** フィルタが割り当てられていない品目)</span><span class="sxs-lookup"><span data-stu-id="9de5b-223">**Item number:** *A0001* (an item that no **Code 4** filter is assigned to)</span></span>
    - <span data-ttu-id="9de5b-224">**数量:** *1.00*</span><span class="sxs-lookup"><span data-stu-id="9de5b-224">**Quantity:** *1.00*</span></span>

## <a name="automatic-release-of-sales-orders-to-the-warehouse"></a><span data-ttu-id="9de5b-225">販売注文を倉庫に自動的にリリースする</span><span class="sxs-lookup"><span data-stu-id="9de5b-225">Automatic release of sales orders to the warehouse</span></span>

<span data-ttu-id="9de5b-226">既に作成した一連の販売注文に対して、自動的に倉庫にリリースする手順を実行します。</span><span class="sxs-lookup"><span data-stu-id="9de5b-226">For each set of sales orders that you created earlier, you will complete a procedure for automatic release to the warehouse.</span></span> <span data-ttu-id="9de5b-227">いずれの場合も、ここで提供されている[基本的な倉庫へのリリース手順](#release-procedure)に従って作業します。</span><span class="sxs-lookup"><span data-stu-id="9de5b-227">In each case, you will work through the [basic release-to-warehouse procedure](#release-procedure) that is provided here.</span></span>

### <a name="basic-release-to-warehouse-procedure"></a><a name="release-procedure"></a><span data-ttu-id="9de5b-228">基本的な倉庫へのリリース手順</span><span class="sxs-lookup"><span data-stu-id="9de5b-228">Basic release-to-warehouse procedure</span></span>

<span data-ttu-id="9de5b-229">作成済の連の販売注文ごとに、以下のサブセクションで説明する3つの手順を実行します。</span><span class="sxs-lookup"><span data-stu-id="9de5b-229">For each set of sales orders that you created earlier, you will complete the three procedures that are outlined in the following subsections.</span></span>

#### <a name="update-the-wave-template-that-will-be-used-during-release"></a><span data-ttu-id="9de5b-230">リリース時に使用されるウェーブのテンプレートを更新する</span><span class="sxs-lookup"><span data-stu-id="9de5b-230">Update the wave template that will be used during release</span></span>

1. <span data-ttu-id="9de5b-231">**倉庫管理 \> 設定 \> ウェーブ \> ウェーブ テンプレート** の順に移動します。</span><span class="sxs-lookup"><span data-stu-id="9de5b-231">Go to **Warehouse management \> Setup \> Waves \> Wave templates**.</span></span>
1. <span data-ttu-id="9de5b-232">**ウェーブ テンプレート タイプ** フィールドを *出荷* に設定 します。</span><span class="sxs-lookup"><span data-stu-id="9de5b-232">Set the **Wave template type** field to *Shipping*.</span></span>
1. <span data-ttu-id="9de5b-233">このシナリオで作成した注文セットで使用した倉庫に関連付けられているウェーブ テンプレートを検索して選択します。</span><span class="sxs-lookup"><span data-stu-id="9de5b-233">Find and select the wave template that is associated with the warehouse that you used in the order sets that you created for this scenario.</span></span> <span data-ttu-id="9de5b-234">たとえば、倉庫 *24* を使用した場合は、 **出荷時の既定のウェーブ テンプレートとして 24** を選択します。</span><span class="sxs-lookup"><span data-stu-id="9de5b-234">For example, if you used warehouse *24*, select the **24 Shipping Default** wave template.</span></span> <span data-ttu-id="9de5b-235">倉庫 *61* を使用した場合は、 **出荷時の既定のウェーブ テンプレートとして 61** を選択します。</span><span class="sxs-lookup"><span data-stu-id="9de5b-235">If you used warehouse *61*, select the **61 Shipping** wave template.</span></span>
1. <span data-ttu-id="9de5b-236">アクション ウィンドウで、**編集** を選択します。</span><span class="sxs-lookup"><span data-stu-id="9de5b-236">On the Action Pane, select **Edit**.</span></span>
1. <span data-ttu-id="9de5b-237">**倉庫へのリリース時にウェーブを処理する** オプションを *いいえ* に設定します。</span><span class="sxs-lookup"><span data-stu-id="9de5b-237">Set the **Process wave at release to warehouse** option to *No*.</span></span>

#### <a name="release-to-the-warehouse"></a><span data-ttu-id="9de5b-238">倉庫へのリリース</span><span class="sxs-lookup"><span data-stu-id="9de5b-238">Release to the warehouse</span></span>

1. <span data-ttu-id="9de5b-239">**倉庫管理 \> 倉庫へのリリース \> 販売注文の自動リリース** に移動します。</span><span class="sxs-lookup"><span data-stu-id="9de5b-239">Go to **Warehouse management \> Release to warehouse \> Automatic release of sales orders**.</span></span>
1. <span data-ttu-id="9de5b-240">**リリース数量** フィールドを *すべて* に設定します。</span><span class="sxs-lookup"><span data-stu-id="9de5b-240">Set the **Quantity to release** field to *All*.</span></span>
1. <span data-ttu-id="9de5b-241">**含めるレコード** クイックタブで、**フィルター** を選択してクエリのダイアログ ボックスを開きます。</span><span class="sxs-lookup"><span data-stu-id="9de5b-241">On the **Records to include** FastTab, select **Filter** to open the query dialog box.</span></span>
1. <span data-ttu-id="9de5b-242">**範囲** タブで、 **追加** を選択して、グリッドに以下の設定を持つ行を追加します:</span><span class="sxs-lookup"><span data-stu-id="9de5b-242">On the **Range** tab, select **Add** to add a row that has the following settings to the grid:</span></span>

    - <span data-ttu-id="9de5b-243">**テーブル:** *販売注文*</span><span class="sxs-lookup"><span data-stu-id="9de5b-243">**Table:** *Sales order*</span></span>
    - <span data-ttu-id="9de5b-244">**派生テーブル:** *販売注文*</span><span class="sxs-lookup"><span data-stu-id="9de5b-244">**Derived table:** *Sales order*</span></span>
    - <span data-ttu-id="9de5b-245">**フィールド:** *販売注文*</span><span class="sxs-lookup"><span data-stu-id="9de5b-245">**Field:** *Sales order*</span></span>
    - <span data-ttu-id="9de5b-246">**基準:** 希望する注文セットの販売注文番号をカンマ区切りで入力します。</span><span class="sxs-lookup"><span data-stu-id="9de5b-246">**Criteria:** Enter a comma-separated list of the sales order numbers from the desired order set.</span></span>

1. <span data-ttu-id="9de5b-247">**OK** を選択してクエリを保存します。</span><span class="sxs-lookup"><span data-stu-id="9de5b-247">Select **OK** to save your query.</span></span>
1. <span data-ttu-id="9de5b-248">**OK** を選択して、*倉庫への自動リリース* の手順を開始します。</span><span class="sxs-lookup"><span data-stu-id="9de5b-248">Select **OK** to start the *Automatic release to warehouse* procedure.</span></span>

#### <a name="review-the-shipment-that-is-created-or-updated"></a><span data-ttu-id="9de5b-249">作成または更新された出荷の確認</span><span class="sxs-lookup"><span data-stu-id="9de5b-249">Review the shipment that is created or updated</span></span>

1. <span data-ttu-id="9de5b-250">**倉庫管理 \> 出荷 \> すべての出荷** に移動します。</span><span class="sxs-lookup"><span data-stu-id="9de5b-250">Go to **Warehouse management \> Shipments \> All shipments**.</span></span>
1. <span data-ttu-id="9de5b-251">必要な出荷を検索して選択します。</span><span class="sxs-lookup"><span data-stu-id="9de5b-251">Find and select the required shipment.</span></span>
1. <span data-ttu-id="9de5b-252">出荷の作成時または更新時に連結ポリシーが使用されていた場合は、**出荷連結ポリシー** フィールドに表示する必要があります。</span><span class="sxs-lookup"><span data-stu-id="9de5b-252">If a consolidation policy was used when the shipment was created or updated, you should see it in the **Shipment consolidation policy** field.</span></span>

### <a name="release-sales-orders-from-order-set-1"></a><span data-ttu-id="9de5b-253">注文セット1から販売注文をリリースする</span><span class="sxs-lookup"><span data-stu-id="9de5b-253">Release sales orders from order set 1</span></span>

<span data-ttu-id="9de5b-254">[基本的な倉庫へのリリース手順](#release-procedure)に従って、注文セット1から販売注文をリリースします。</span><span class="sxs-lookup"><span data-stu-id="9de5b-254">Follow the [basic release-to-warehouse procedure](#release-procedure) to release the sales orders from order set 1.</span></span>

<span data-ttu-id="9de5b-255">完了すると、2つの出荷が作成されていることがわかります。</span><span class="sxs-lookup"><span data-stu-id="9de5b-255">When you've finished, you should see that two shipments were created:</span></span>

- <span data-ttu-id="9de5b-256">最初の出荷は、*顧客モード* の出荷連結ポリシーを使用して作成された 3 つの行で構成されます。</span><span class="sxs-lookup"><span data-stu-id="9de5b-256">The first shipment contains three lines and was created by using the *CustomerMode* shipment consolidation policy.</span></span>
- <span data-ttu-id="9de5b-257">2 つ目の出荷は、*航空運賃* 輸送モードの荷渡方法を使用しないもので、顧客注文の *CustomerOrderNo* 連結ポリシーを使用して作成されてい ます。</span><span class="sxs-lookup"><span data-stu-id="9de5b-257">The second shipment, which doesn't use the *Airways* transportation mode of delivery, was created by using the *CustomerOrderNo* shipment consolidation policy.</span></span>

### <a name="release-sales-orders-from-order-set-2"></a><span data-ttu-id="9de5b-258">注文セット2から販売注文をリリースする</span><span class="sxs-lookup"><span data-stu-id="9de5b-258">Release sales orders from order set 2</span></span>

<span data-ttu-id="9de5b-259">[基本的な倉庫へのリリース手順](#release-procedure)に従って、注文セット2から販売注文をリリースします。</span><span class="sxs-lookup"><span data-stu-id="9de5b-259">Follow the [basic release-to-warehouse procedure](#release-procedure) to release the sales orders from order set 2.</span></span>

<span data-ttu-id="9de5b-260">完了すると、3つの出荷が作成されていることがわかります。</span><span class="sxs-lookup"><span data-stu-id="9de5b-260">When you've finished, you should see that three shipments were created:</span></span>

- <span data-ttu-id="9de5b-261">最初の出荷には、 *可燃性* の品目が含まれています。</span><span class="sxs-lookup"><span data-stu-id="9de5b-261">The first shipment contains *Flammable* items.</span></span>
- <span data-ttu-id="9de5b-262">他の 2 つの出荷には、*爆発性* の品目を含む 1 つの行が含まれてい ます。</span><span class="sxs-lookup"><span data-stu-id="9de5b-262">Each of the other two shipments contains one line that has the *Explosive* item.</span></span>

### <a name="release-sales-orders-from-order-set-3"></a><span data-ttu-id="9de5b-263">注文セット3から販売注文をリリースする</span><span class="sxs-lookup"><span data-stu-id="9de5b-263">Release sales orders from order set 3</span></span>

<span data-ttu-id="9de5b-264">[基本的な倉庫へのリリース手順](#release-procedure)に従って、注文セット3から販売注文をリリースします。</span><span class="sxs-lookup"><span data-stu-id="9de5b-264">Follow the [basic release-to-warehouse procedure](#release-procedure) to release the sales orders from order set 3.</span></span>

<span data-ttu-id="9de5b-265">完了すると、以下のアクションが実行されることを確認します:</span><span class="sxs-lookup"><span data-stu-id="9de5b-265">When you've finished, you should see that the following actions occurred:</span></span>

- <span data-ttu-id="9de5b-266">既存の出荷 (注文セット2が倉庫にリリースされた際に作成された出荷) が1つ更新されました。</span><span class="sxs-lookup"><span data-stu-id="9de5b-266">One existing shipment (the shipment that was created when order set 2 was released to the warehouse) was updated.</span></span> <span data-ttu-id="9de5b-267">*可燃性* 品目を含む行が追加されました。</span><span class="sxs-lookup"><span data-stu-id="9de5b-267">A line that has the *Flammable* item was added.</span></span>
- <span data-ttu-id="9de5b-268">*爆発* 品目を新規出荷が1つ作成されました。</span><span class="sxs-lookup"><span data-stu-id="9de5b-268">One new shipment was created that contains the *Explosive* item.</span></span>

### <a name="release-sales-orders-from-order-set-4"></a><span data-ttu-id="9de5b-269">注文セット4から販売注文をリリースする</span><span class="sxs-lookup"><span data-stu-id="9de5b-269">Release sales orders from order set 4</span></span>

<span data-ttu-id="9de5b-270">[基本的な倉庫へのリリース手順](#release-procedure)に従って、注文セット4から販売注文をリリースします。</span><span class="sxs-lookup"><span data-stu-id="9de5b-270">Follow the [basic release-to-warehouse procedure](#release-procedure) to release the sales orders from order set 4.</span></span>

<span data-ttu-id="9de5b-271">完了すると、既存の出荷 (**顧客要求** フィールドが *1* に設定されているもの ) が更新されたことを確認できます。</span><span class="sxs-lookup"><span data-stu-id="9de5b-271">When you've finished, you should see that one existing shipment (where the **Customer requisition** field is set to *1*) was updated.</span></span> <span data-ttu-id="9de5b-272">新たな行が1つ追加されました。</span><span class="sxs-lookup"><span data-stu-id="9de5b-272">One new line was added to it.</span></span>

### <a name="release-sales-orders-from-order-set-5"></a><span data-ttu-id="9de5b-273">注文セット5から販売注文をリリースする</span><span class="sxs-lookup"><span data-stu-id="9de5b-273">Release sales orders from order set 5</span></span>

<span data-ttu-id="9de5b-274">[基本的な倉庫へのリリース手順](#release-procedure)に従って、注文セット5から販売注文をリリースします。</span><span class="sxs-lookup"><span data-stu-id="9de5b-274">Follow the [basic release-to-warehouse procedure](#release-procedure) to release the sales orders from order set 5.</span></span>

<span data-ttu-id="9de5b-275">完了すると、以下のアクションが実行されることを確認します:</span><span class="sxs-lookup"><span data-stu-id="9de5b-275">When you've finished, you should see that the following actions occurred:</span></span>

- <span data-ttu-id="9de5b-276">既存の出荷 ( **顧客要求** フィールドが *1* に設定されたもの) が更新されました。</span><span class="sxs-lookup"><span data-stu-id="9de5b-276">One existing shipment (where the **Customer requisition** field is set to *1*) was updated.</span></span> <span data-ttu-id="9de5b-277">販売注文 5-3 ( **顧客要求** フィールドが *1* に設定されたもの) の明細行が 追加されました。</span><span class="sxs-lookup"><span data-stu-id="9de5b-277">A line from sales order 5-3 (where the **Customer requisition** field is set to *1*) was added to it.</span></span>
- <span data-ttu-id="9de5b-278">販売注文 5-1 と 5-2 の明細行が1つの出荷にグループ化されている、新たな出荷が1つ作成されました。</span><span class="sxs-lookup"><span data-stu-id="9de5b-278">One new shipment was created, where lines from sales orders 5-1 and 5-2 are grouped into one shipment.</span></span>

### <a name="release-sales-orders-from-order-set-6"></a><span data-ttu-id="9de5b-279">注文セット6から販売注文をリリースする</span><span class="sxs-lookup"><span data-stu-id="9de5b-279">Release sales orders from order set 6</span></span>

<span data-ttu-id="9de5b-280">[基本的な倉庫へのリリース手順](#release-procedure)に従って、注文セット6から販売注文をリリースします。</span><span class="sxs-lookup"><span data-stu-id="9de5b-280">Follow the [basic release-to-warehouse procedure](#release-procedure) to release the sales orders from order set 6.</span></span>

<span data-ttu-id="9de5b-281">完了すると、4つの出荷が作成されていることがわかります。</span><span class="sxs-lookup"><span data-stu-id="9de5b-281">When you've finished, you should see that four shipments were created:</span></span>

- <span data-ttu-id="9de5b-282">顧客アカウント *US-003* の 2 件の販売注文の明細行は、*注文プール* の出荷連結ポリシーを使用して 1 つの出荷にグループ化されています。</span><span class="sxs-lookup"><span data-stu-id="9de5b-282">Lines from two orders for customer *US-003* were grouped into one shipment by using the *Order pool* shipment consolidation policy.</span></span>
- <span data-ttu-id="9de5b-283">顧客アカウント *US-004* の 2 件の販売注文の明細行は、*注文プール* の出荷連結ポリシーを使用して 1 つの出荷にグループ化されています。</span><span class="sxs-lookup"><span data-stu-id="9de5b-283">Lines from two orders for customer *US-004* were grouped into one shipment by using the *Order pool* shipment consolidation policy.</span></span>
- <span data-ttu-id="9de5b-284">顧客 *007* の販売注文 6-5 および 6-6 の明細行は、*注文プール* の出荷連結ポリシーを使用して1つの出荷にグループ化されています。</span><span class="sxs-lookup"><span data-stu-id="9de5b-284">Lines from sales orders 6-5 and 6-6 for customer *US-007* were grouped into one shipment by using the *Order pool* shipment consolidation policy.</span></span>
- <span data-ttu-id="9de5b-285">顧客 *007* の販売注文 6-7 および 6-8 の明細行は、*クロスオーダー* の出荷連結ポリシーを使用して1つの出荷にグループ化されています。</span><span class="sxs-lookup"><span data-stu-id="9de5b-285">Lines from sales orders 6-7 and 6-8 for customer *US-007* were grouped into one shipment by using the *CrossOrder* shipment consolidation policy.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="9de5b-286">追加リソース</span><span class="sxs-lookup"><span data-stu-id="9de5b-286">Additional resources</span></span>

- [<span data-ttu-id="9de5b-287">出荷連結ポリシー</span><span class="sxs-lookup"><span data-stu-id="9de5b-287">Shipment consolidation policies</span></span>](about-shipment-consolidation-policies.md)
- [<span data-ttu-id="9de5b-288">出荷連結ポリシーを構成する</span><span class="sxs-lookup"><span data-stu-id="9de5b-288">Configure shipment consolidation policies</span></span>](configure-shipment-consolidation-policies.md)


[!INCLUDE[footer-include](../../includes/footer-banner.md)]