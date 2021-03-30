---
title: 出荷の連結ページを使用して出荷を手動で連結する
description: このトピックでは、複数の注文が倉庫にリリースされ、出荷の連結ページを使用して連結するシナリオを示します。
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
ms.search.region: Global
ms.author: kamaybac
ms.search.validFrom: 2020-05-01
ms.dyn365.ops.version: 10.0.3
ms.openlocfilehash: 6d9186fe242fa56b6a360d6a4e4284c0c3eac141
ms.sourcegitcommit: eaf330dbee1db96c20d5ac479f007747bea079eb
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 02/15/2021
ms.locfileid: "5242208"
---
# <a name="consolidate-shipments-manually-by-using-the-consolidate-shipments-page"></a><span data-ttu-id="6b699-103">出荷の連結ページを使用して出荷を手動で連結する</span><span class="sxs-lookup"><span data-stu-id="6b699-103">Consolidate shipments manually by using the Consolidate shipments page</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="6b699-104">このトピックでは、複数の注文が倉庫にリリースされ、**出荷の連結** ページを使用して連結するシナリオを示します。</span><span class="sxs-lookup"><span data-stu-id="6b699-104">This topic presents a scenario where multiple orders are released to the warehouse and then consolidated later by using the **Consolidate shipments** page.</span></span>

## <a name="make-demo-data-available"></a><span data-ttu-id="6b699-105">デモ データを有効化する</span><span class="sxs-lookup"><span data-stu-id="6b699-105">Make demo data available</span></span>

<span data-ttu-id="6b699-106">このトピックのシナリオでは、Microsoft Dynamics 365 Supply Chain Management にて用意されている標準のデモデータに含まれる値とレコードを参照し ます。</span><span class="sxs-lookup"><span data-stu-id="6b699-106">The scenario in this topic references values and records that are included in the standard demo data that is provided for Microsoft Dynamics 365 Supply Chain Management.</span></span> <span data-ttu-id="6b699-107">ここで提供されている値を使用するには、デモデータがインストールされている環境で作業し、開始する前に法人を **usmf** に設定します。</span><span class="sxs-lookup"><span data-stu-id="6b699-107">If you want to use the values that are provided here as you do the exercises, be sure to work in an environment where the demo data is installed, and set the legal entity to **USMF** before you begin.</span></span>

## <a name="set-up-shipment-consolidation-policies-and-product-filters"></a><span data-ttu-id="6b699-108">出荷連結ポリシーおよび製品フィルタの設定</span><span class="sxs-lookup"><span data-stu-id="6b699-108">Set up shipment consolidation policies and product filters</span></span>

<span data-ttu-id="6b699-109">このシナリオでは、既にこの機能を有効にし、[出荷連結ポリシーの構成](configure-shipment-consolidation-policies.md)内の実習を完了しており、同ページ内に記述されているポリシーとその他のレコードを作成していることを前提としています。</span><span class="sxs-lookup"><span data-stu-id="6b699-109">The scenario that is described here assumes that you've already turned on the feature, done the exercises in [Configure shipment consolidation policies](configure-shipment-consolidation-policies.md), and created the policies and other records that are described there.</span></span> <span data-ttu-id="6b699-110">このシナリオを続行する前に、この演習を行っている必要があります。</span><span class="sxs-lookup"><span data-stu-id="6b699-110">Be sure to do those exercises before you continue with this scenario.</span></span>

## <a name="create-the-sales-orders-for-this-scenario"></a><span data-ttu-id="6b699-111">このシナリオで使用する販売注文の作成</span><span class="sxs-lookup"><span data-stu-id="6b699-111">Create the sales orders for this scenario</span></span>

<span data-ttu-id="6b699-112">シナリオで使用する一連の販売注文を作成することから始めます。</span><span class="sxs-lookup"><span data-stu-id="6b699-112">Start by creating a collection of sales orders that you can work with.</span></span> <span data-ttu-id="6b699-113">高度な倉庫 (WMS) プロセスが利用できる倉庫を使用する必要があります。</span><span class="sxs-lookup"><span data-stu-id="6b699-113">You must work with a warehouse that is enabled for advanced warehouse (WMS) processes.</span></span> <span data-ttu-id="6b699-114">他の倉庫を明示的に指定していない場合は、次の注文セットのそれぞれに対して同じ倉庫が使用されなければなりません。</span><span class="sxs-lookup"><span data-stu-id="6b699-114">Unless a different warehouse is explicitly mentioned, that same warehouse must be used for each of the following sets of orders.</span></span>

<span data-ttu-id="6b699-115">**売掛金勘定  \> 注文 \> すべての販売注文** に移動し、次のサブセクションで説明されている設定を含む販売注文のコレクションを作成します。</span><span class="sxs-lookup"><span data-stu-id="6b699-115">Go to **Accounts receivable \> Orders \> All sales orders**, and create a collection of sales orders that have the settings that are described in the following subsections.</span></span>

### <a name="create-sales-orders-1-and-2"></a><span data-ttu-id="6b699-116">販売注文 1 と 2 の作成</span><span class="sxs-lookup"><span data-stu-id="6b699-116">Create sales orders 1 and 2</span></span>

1. <span data-ttu-id="6b699-117">以下の設定で 2 つの同一の販売注文を作成します:</span><span class="sxs-lookup"><span data-stu-id="6b699-117">Create two identical sales orders that have the following settings:</span></span>

    - <span data-ttu-id="6b699-118">**顧客アカウント:** *US-007*</span><span class="sxs-lookup"><span data-stu-id="6b699-118">**Customer account:** *US-007*</span></span>
    - <span data-ttu-id="6b699-119">**プール :** *ShipCons*</span><span class="sxs-lookup"><span data-stu-id="6b699-119">**Pool:** *ShipCons*</span></span>

1. <span data-ttu-id="6b699-120">以下の設定で注文明細行を追加します:</span><span class="sxs-lookup"><span data-stu-id="6b699-120">Add an order line that has the following settings:</span></span>

    - <span data-ttu-id="6b699-121">**品目番号 :** *A0001* (**コード 4** フィルタが割り当てられていない品目)</span><span class="sxs-lookup"><span data-stu-id="6b699-121">**Item number:** *A0001* (an item that no **Code 4** filter is assigned to)</span></span>
    - <span data-ttu-id="6b699-122">**数量:** *1.00*</span><span class="sxs-lookup"><span data-stu-id="6b699-122">**Quantity:** *1.00*</span></span>

1. <span data-ttu-id="6b699-123">**在庫 \> 引当** を選択し、アクションウ ィンドウで **ロットの引当** を選択して、注文明細行を引当します。</span><span class="sxs-lookup"><span data-stu-id="6b699-123">Select **Inventory \> Reservation**, and then, on the Action Pane, select **Reserve lot** to reserve the order line.</span></span>

### <a name="create-sales-orders-3-and-4"></a><span data-ttu-id="6b699-124">販売注文 3 と 4 の作成</span><span class="sxs-lookup"><span data-stu-id="6b699-124">Create sales orders 3 and 4</span></span>

1. <span data-ttu-id="6b699-125">以下の設定で 2 つの同一の販売注文を作成します:</span><span class="sxs-lookup"><span data-stu-id="6b699-125">Create two identical sales orders that have the following settings:</span></span>

    - <span data-ttu-id="6b699-126">**顧客アカウント:** *US-007*</span><span class="sxs-lookup"><span data-stu-id="6b699-126">**Customer account:** *US-007*</span></span>
    - <span data-ttu-id="6b699-127">**プール :** このフィールドは空白のままにします。</span><span class="sxs-lookup"><span data-stu-id="6b699-127">**Pool:** Leave this field blank.</span></span>

1. <span data-ttu-id="6b699-128">以下の設定で注文明細行を追加します:</span><span class="sxs-lookup"><span data-stu-id="6b699-128">Add an order line that has the following settings:</span></span>

    - <span data-ttu-id="6b699-129">**品目番号 :** *A0001* (**コード 4** フィルタが割り当てられていない品目)</span><span class="sxs-lookup"><span data-stu-id="6b699-129">**Item number:** *A0001* (an item that no **Code 4** filter is assigned to)</span></span>
    - <span data-ttu-id="6b699-130">**数量:** *1.00*</span><span class="sxs-lookup"><span data-stu-id="6b699-130">**Quantity:** *1.00*</span></span>

1. <span data-ttu-id="6b699-131">**在庫 \> 引当** を選択し、アクションウ ィンドウで **ロットの引当** を選択して、注文明細行を引当します。</span><span class="sxs-lookup"><span data-stu-id="6b699-131">Select **Inventory \> Reservation**, and then, on the Action Pane, select **Reserve lot** to reserve the order line.</span></span>

## <a name="release-the-orders-to-the-warehouse"></a><span data-ttu-id="6b699-132">注文を倉庫にリリースする</span><span class="sxs-lookup"><span data-stu-id="6b699-132">Release the orders to the warehouse</span></span>

<span data-ttu-id="6b699-133">このシナリオで作成した各販売注文のリリースをするには、次の手順に従ってください。</span><span class="sxs-lookup"><span data-stu-id="6b699-133">Follow these steps to release each sales order that you created for this scenario to the warehouse.</span></span>

1. <span data-ttu-id="6b699-134">**売掛金勘定 \> 注文 \> すべての販売注文** に移動します。</span><span class="sxs-lookup"><span data-stu-id="6b699-134">Go to **Accounts receivable \> Orders \> All sales orders**.</span></span>
1. <span data-ttu-id="6b699-135">リリースする販売注文を検索して選択します。</span><span class="sxs-lookup"><span data-stu-id="6b699-135">Find and select the sales order to release.</span></span>
1. <span data-ttu-id="6b699-136">アクション ウィンドウの、**倉庫** タブにて、**アクション\> 倉庫へのリリース** を選択して、選択された販売注文をリリースします。</span><span class="sxs-lookup"><span data-stu-id="6b699-136">On the Action Pane, on the **Warehouse** tab, select **Actions \> Release to warehouse** to release the selected sales order.</span></span>
1. <span data-ttu-id="6b699-137">このシナリオで作成したそれぞれの販売注文に対して、この手順を繰り返します。</span><span class="sxs-lookup"><span data-stu-id="6b699-137">Repeat this procedure for every other sales order that you created for this scenario.</span></span>

## <a name="consolidate-shipments"></a><span data-ttu-id="6b699-138">出荷の連結</span><span class="sxs-lookup"><span data-stu-id="6b699-138">Consolidate shipments</span></span>

1. <span data-ttu-id="6b699-139">**倉庫管理 \> 出荷 \> すべての出荷** に移動します。</span><span class="sxs-lookup"><span data-stu-id="6b699-139">Go to **Warehouse management \> Shipments \> All shipments**.</span></span>
1. <span data-ttu-id="6b699-140">販売注文 1 が倉庫にリリースされた際に作成された出荷を検索して選択します。</span><span class="sxs-lookup"><span data-stu-id="6b699-140">Find and select a shipment that was created when sales order 1 was released to the warehouse.</span></span> <span data-ttu-id="6b699-141">(それぞれの **出荷連結ポリシー** フィールドには、*注文管理プール* を設定する必要があります。)</span><span class="sxs-lookup"><span data-stu-id="6b699-141">(Its **Shipment consolidation policy** field should be set to *Order pool*.)</span></span>
1. <span data-ttu-id="6b699-142">アクション ウィンドウの **出荷** タブで、**出荷 \> 出荷の連結** を選択します。</span><span class="sxs-lookup"><span data-stu-id="6b699-142">On the Action Pane, on the **Shipments** tab, select **Shipments \> Consolidate shipments**.</span></span>
1. <span data-ttu-id="6b699-143">連結の提案がされている出荷を確認します。</span><span class="sxs-lookup"><span data-stu-id="6b699-143">Verify the shipments that are suggested for consolidation.</span></span> <span data-ttu-id="6b699-144">連結に提案は、同一のポリシーが設定された出荷を1つだけ設定する必要があります。</span><span class="sxs-lookup"><span data-stu-id="6b699-144">Only one shipment that has the same policy should be suggested for consolidation.</span></span>
1. <span data-ttu-id="6b699-145">**出荷の連結** ページを閉じます。</span><span class="sxs-lookup"><span data-stu-id="6b699-145">Close the **Shipment consolidation** page.</span></span>
1. <span data-ttu-id="6b699-146">販売注文 3 が倉庫にリリースされた際に作成された出荷を検索して選択します。</span><span class="sxs-lookup"><span data-stu-id="6b699-146">Find and select a shipment that was created when sales order 3 was released to the warehouse.</span></span> <span data-ttu-id="6b699-147">(それぞれの **出荷連結ポリシー** フィールドには、*既定* を設定する必要があります。)</span><span class="sxs-lookup"><span data-stu-id="6b699-147">(Its **Shipment consolidation policy** field should be set to *Default*.)</span></span>
1. <span data-ttu-id="6b699-148">アクション ウィンドウの **出荷** タブで、**出荷 \> 出荷の連結** を選択します。</span><span class="sxs-lookup"><span data-stu-id="6b699-148">On the Action Pane, on the **Shipments** tab, select **Shipments \> Consolidate shipments**.</span></span>
1. <span data-ttu-id="6b699-149">連結の提案がされている出荷がないことを確認します。</span><span class="sxs-lookup"><span data-stu-id="6b699-149">Verify that no shipments are suggested for consolidation.</span></span>
1. <span data-ttu-id="6b699-150">**フィルタの表示** を選択します。</span><span class="sxs-lookup"><span data-stu-id="6b699-150">Select **Show filters**.</span></span>
1. <span data-ttu-id="6b699-151">**フィルタ** ウィンドウで、**注文番号** フィルタを削除し、 **適用** を選択します。</span><span class="sxs-lookup"><span data-stu-id="6b699-151">In the **Filters** pane, remove the **Order number** filter, and then select **Apply**.</span></span>
1. <span data-ttu-id="6b699-152">連結の提案がされている出荷を確認します。</span><span class="sxs-lookup"><span data-stu-id="6b699-152">Verify the shipments that are suggested for consolidation.</span></span> <span data-ttu-id="6b699-153">連結に提案は、同一のポリシーが設定された出荷を1つだけ設定する必要があります。</span><span class="sxs-lookup"><span data-stu-id="6b699-153">Only one shipment that has the same policy should be suggested for consolidation.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="6b699-154">追加リソース</span><span class="sxs-lookup"><span data-stu-id="6b699-154">Additional resources</span></span>

- [<span data-ttu-id="6b699-155">出荷連結ポリシー</span><span class="sxs-lookup"><span data-stu-id="6b699-155">Shipment consolidation policies</span></span>](about-shipment-consolidation-policies.md)
- [<span data-ttu-id="6b699-156">出荷連結ポリシーを構成する</span><span class="sxs-lookup"><span data-stu-id="6b699-156">Configure shipment consolidation policies</span></span>](configure-shipment-consolidation-policies.md)

[!INCLUDE[footer-include](../../includes/footer-banner.md)]