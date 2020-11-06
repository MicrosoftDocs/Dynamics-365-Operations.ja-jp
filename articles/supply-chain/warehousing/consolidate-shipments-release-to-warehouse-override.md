---
title: 出荷連結ポリシーが [倉庫へのリリース] ページで無効になっている場合の出荷の連結
description: このトピックでは、1 つ以上の販売明細を、[倉庫へのリリース] ページから手動でリリースする必要がある場合で、かつリリース前にシステム定義の連結ポリシーを上書きする必要があるシナリオを示します。
author: GarmMSFT
manager: tfehr
ms.date: 05/12/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: WHSShipConsolidationPolicy, WHSShipConsolidationWorkbench, WHSFilterGroupTable, WHSShipConsolidationSetShipment, WHSShipmentConsolidation, WHSFilterGenerallyAvail, WHSReleaseToWarehouse
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: kamaybac
ms.search.validFrom: 2020-05-01
ms.dyn365.ops.version: 10.0.6
ms.openlocfilehash: 96f994e9f3440721105545f96d7d8475fcab2b6b
ms.sourcegitcommit: a36a4f9915ae3eb36bf8220111cf1486387713d9
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 10/16/2020
ms.locfileid: "4016796"
---
# <a name="consolidate-shipments-when-the-shipment-consolidation-policy-is-overridden-from-the-release-to-warehouse-page"></a><span data-ttu-id="d9f0e-103">出荷連結ポリシーが [倉庫へのリリース] ページで無効になっている場合の出荷の連結</span><span class="sxs-lookup"><span data-stu-id="d9f0e-103">Consolidate shipments when the shipment consolidation policy is overridden from the Release to warehouse page</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="d9f0e-104">このトピックでは、1 つ以上の販売明細を、 **倉庫へのリリース** ページから手動でリリースする必要がある場合で、かつリリース前にシステム定義の連結ポリシーを上書きする必要があるシナリオを示します。</span><span class="sxs-lookup"><span data-stu-id="d9f0e-104">This topic presents a scenario where one or more sales lines must be manually released to the warehouse from the **Release to warehouse** page, and the system-defined shipment consolidation policy must be overridden before the release.</span></span> <span data-ttu-id="d9f0e-105">例えば、通常はオープン出荷で連結されていない注文をオープン出荷で連結する必要がある場合など、出荷の連結ポリシーの上書きが必要になる場合があります。</span><span class="sxs-lookup"><span data-stu-id="d9f0e-105">An override of the shipment consolidation policy might be required if, for example, an order that isn't usually consolidated with open shipments must be consolidated with open shipments.</span></span>

<span data-ttu-id="d9f0e-106">このシナリオでは、一連の販売注文を作成してから、その注文を倉庫にリリースする前に既定の出荷連結ポリシーを上書きします。</span><span class="sxs-lookup"><span data-stu-id="d9f0e-106">During the scenario, you will create a set of sales orders and then override the default shipment consolidation policy before you release the orders to the warehouse.</span></span>

## <a name="make-demo-data-available"></a><span data-ttu-id="d9f0e-107">デモ データを有効化する</span><span class="sxs-lookup"><span data-stu-id="d9f0e-107">Make demo data available</span></span>

<span data-ttu-id="d9f0e-108">このトピックのシナリオでは、Microsoft Dynamics 365 Supply Chain Management にて用意されている標準のデモデータに含まれる値とレコードを参照し ます。</span><span class="sxs-lookup"><span data-stu-id="d9f0e-108">The scenario in this topic references values and records that are included in the standard demo data that is provided for Microsoft Dynamics 365 Supply Chain Management.</span></span> <span data-ttu-id="d9f0e-109">ここで提供されている値を使用するには、デモデータがインストールされている環境で作業し、開始する前に法人を **usmf** に設定します。</span><span class="sxs-lookup"><span data-stu-id="d9f0e-109">If you want to use the values that are provided here as you do the exercises, be sure to work in an environment where the demo data is installed, and set the legal entity to **USMF** before you begin.</span></span>

## <a name="set-up-shipment-consolidation-policies-and-product-filters"></a><span data-ttu-id="d9f0e-110">出荷連結ポリシーおよび製品フィルタの設定</span><span class="sxs-lookup"><span data-stu-id="d9f0e-110">Set up shipment consolidation policies and product filters</span></span>

<span data-ttu-id="d9f0e-111">このシナリオでは、既にこの機能を有効にし、[出荷連結ポリシーの構成](configure-shipment-consolidation-policies.md)内の実習を完了しており、同ページ内に記述されているポリシーとその他のレコードを作成していることを前提としています。</span><span class="sxs-lookup"><span data-stu-id="d9f0e-111">The scenario that is described here assumes that you've already turned on the feature, done the exercises in [Configure shipment consolidation policies](configure-shipment-consolidation-policies.md), and created the policies and other records that are described there.</span></span> <span data-ttu-id="d9f0e-112">このシナリオを続行する前に、この演習を行っている必要があります。</span><span class="sxs-lookup"><span data-stu-id="d9f0e-112">Be sure to do those exercises before you continue with this scenario.</span></span>

## <a name="create-the-sales-orders-for-this-scenario"></a><span data-ttu-id="d9f0e-113">このシナリオで使用する販売注文の作成</span><span class="sxs-lookup"><span data-stu-id="d9f0e-113">Create the sales orders for this scenario</span></span>

1. <span data-ttu-id="d9f0e-114">**売掛金勘定 \> 注文 \> すべての販売注文を** に移動し、次のような同一の販売注文を3つ作成します:</span><span class="sxs-lookup"><span data-stu-id="d9f0e-114">Go to **Accounts receivable \> Orders \> All sales orders** , and create three identical sales orders that have the following settings:</span></span>

    - <span data-ttu-id="d9f0e-115">**顧客アカウント:** *US-002*</span><span class="sxs-lookup"><span data-stu-id="d9f0e-115">**Customer account:** *US-002*</span></span>

1. <span data-ttu-id="d9f0e-116">以下の設定で注文明細行を追加します:</span><span class="sxs-lookup"><span data-stu-id="d9f0e-116">Add an order line that has the following settings:</span></span>

    - <span data-ttu-id="d9f0e-117">**品目番号 :** *A0001* ( **コード 4** フィルタが割り当てられていない品目)</span><span class="sxs-lookup"><span data-stu-id="d9f0e-117">**Item number:** *A0001* (an item that no **Code 4** filter is assigned to)</span></span>
    - <span data-ttu-id="d9f0e-118">**数量:** *1.00*</span><span class="sxs-lookup"><span data-stu-id="d9f0e-118">**Quantity:** *1.00*</span></span>

1. <span data-ttu-id="d9f0e-119">**在庫 \> 引当** を選択し、アクションウ ィンドウで **ロットの引当** を選択して、注文明細行を引当します。</span><span class="sxs-lookup"><span data-stu-id="d9f0e-119">Select **Inventory \> Reservation** , and then, on the Action Pane, select **Reserve lot** to reserve the order line.</span></span>

## <a name="release-the-sales-orders-from-the-release-to-warehouse-page"></a><span data-ttu-id="d9f0e-120">[倉庫へのリリース] ページから販売注文をリリースする</span><span class="sxs-lookup"><span data-stu-id="d9f0e-120">Release the sales orders from the Release to warehouse page</span></span>

<span data-ttu-id="d9f0e-121">倉庫へのリリース時に出荷の連結ポリシーを上書きするには、次の手順に従います。</span><span class="sxs-lookup"><span data-stu-id="d9f0e-121">Follow these steps to override the shipment consolidation policy during the release to the warehouse.</span></span>

1. <span data-ttu-id="d9f0e-122">**倉庫管理 \> 倉庫へのリリース \> 倉庫へのリリース** に移動します。</span><span class="sxs-lookup"><span data-stu-id="d9f0e-122">Go to **Warehouse management \> Release to warehouse \> Release to warehouse**.</span></span>
1. <span data-ttu-id="d9f0e-123">上部ウィンドウで、このシナリオで作成した最初の販売注文を選択します。</span><span class="sxs-lookup"><span data-stu-id="d9f0e-123">In the upper pane, select the first sales order that you created for this scenario.</span></span>
1. <span data-ttu-id="d9f0e-124">**追加** を選択して、倉庫へのリリースに明細行を追加します。</span><span class="sxs-lookup"><span data-stu-id="d9f0e-124">Select **Add** to add the line to the release to the warehouse.</span></span> <span data-ttu-id="d9f0e-125">*既定* の出荷連結ポリシーが下部ウィンドウに適用されていることを確認します。</span><span class="sxs-lookup"><span data-stu-id="d9f0e-125">Notice that the *Default* shipment consolidation policy is applied in the bottom pane.</span></span>
1. <span data-ttu-id="d9f0e-126">下部ウィンドウで、 **新規出荷連結ポリシーの選択** を選択します。</span><span class="sxs-lookup"><span data-stu-id="d9f0e-126">In the bottom pane, select **Select new shipment consolidation policy**.</span></span>
1. <span data-ttu-id="d9f0e-127">同一のポリシーを持つ、その他のオープンな出荷との連結を可能にするポリシーを選択します。</span><span class="sxs-lookup"><span data-stu-id="d9f0e-127">Select a policy that allows for consolidation with other open shipments of the same policy.</span></span> <span data-ttu-id="d9f0e-128">たとえば、 *CustomerOrderNo* ポリシーを選択します。</span><span class="sxs-lookup"><span data-stu-id="d9f0e-128">For example, select the *CustomerOrderNo* policy.</span></span>
1. <span data-ttu-id="d9f0e-129">**倉庫へのリリース** を選択します。</span><span class="sxs-lookup"><span data-stu-id="d9f0e-129">Select **Release to warehouse**.</span></span>
1. <span data-ttu-id="d9f0e-130">このシナリオで作成した、2番目と3番目の販売注文を選択します。</span><span class="sxs-lookup"><span data-stu-id="d9f0e-130">Select the second and third sales orders that you created for this scenario.</span></span>
1. <span data-ttu-id="d9f0e-131">**追加** を選択して、倉庫へのリリースに明細行を追加します。</span><span class="sxs-lookup"><span data-stu-id="d9f0e-131">Select **Add** to add the lines to the release to the warehouse.</span></span> <span data-ttu-id="d9f0e-132">*既定* の出荷連結ポリシーが下部ウィンドウに適用されていることを確認します。</span><span class="sxs-lookup"><span data-stu-id="d9f0e-132">Notice that the *Default* policy is applied in the bottom pane.</span></span>
1. <span data-ttu-id="d9f0e-133">2番目の明細行を選択し、 **新規出荷連結ポリシーの選択** フィールドで、 *CustomerOrderNo* ポリシーを選択します。</span><span class="sxs-lookup"><span data-stu-id="d9f0e-133">Select the second line, and then, in the **Select new shipment consolidation policy** field, select the *CustomerOrderNo* policy.</span></span>
1. <span data-ttu-id="d9f0e-134">両方の明細行で **倉庫へのリリース** を選択します。</span><span class="sxs-lookup"><span data-stu-id="d9f0e-134">Select **Release to warehouse** for both lines.</span></span>

## <a name="verify-the-shipments"></a><span data-ttu-id="d9f0e-135">出荷の確認</span><span class="sxs-lookup"><span data-stu-id="d9f0e-135">Verify the shipments</span></span>

<span data-ttu-id="d9f0e-136">次の 2 つの出荷が作成されている必要があります:</span><span class="sxs-lookup"><span data-stu-id="d9f0e-136">Two shipments should have been created:</span></span>

- <span data-ttu-id="d9f0e-137">1つ目の出荷は、 *CustomerOrderNo* の出荷連結ポリシーを使用して作成された 3 つの行で構成されます。</span><span class="sxs-lookup"><span data-stu-id="d9f0e-137">The first shipment contains two lines and was created by using the *CustomerOrderNo* shipment consolidation policy.</span></span>
- <span data-ttu-id="d9f0e-138">2つ目の出荷は、 *既定* の出荷連結ポリシーを使用して作成された 1 つの行で構成されます。</span><span class="sxs-lookup"><span data-stu-id="d9f0e-138">The second shipment contains one line and was created by using the *Default* shipment consolidation policy.</span></span>

<span data-ttu-id="d9f0e-139">作成された出荷を確認するには、次の手順に従います。</span><span class="sxs-lookup"><span data-stu-id="d9f0e-139">Follow these steps to review the shipments that were created.</span></span>

1. <span data-ttu-id="d9f0e-140">**倉庫管理 \> 出荷 \> すべての出荷** に移動します。</span><span class="sxs-lookup"><span data-stu-id="d9f0e-140">Go to **Warehouse management \> Shipments \> All shipments**.</span></span>
1. <span data-ttu-id="d9f0e-141">必要な出荷を検索して選択します。</span><span class="sxs-lookup"><span data-stu-id="d9f0e-141">Find and select the required shipment.</span></span>
1. <span data-ttu-id="d9f0e-142">**出荷連結ポリシー** フィールドで、出荷の作成時に使用された連結ポリシーを確認します。</span><span class="sxs-lookup"><span data-stu-id="d9f0e-142">In the **Shipment consolidation policy** field, review the consolidation policy that was used when the shipment was created.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="d9f0e-143">追加リソース</span><span class="sxs-lookup"><span data-stu-id="d9f0e-143">Additional resources</span></span>

- [<span data-ttu-id="d9f0e-144">出荷連結ポリシー</span><span class="sxs-lookup"><span data-stu-id="d9f0e-144">Shipment consolidation policies</span></span>](about-shipment-consolidation-policies.md)
- [<span data-ttu-id="d9f0e-145">出荷連結ポリシーを構成する</span><span class="sxs-lookup"><span data-stu-id="d9f0e-145">Configure shipment consolidation policies</span></span>](configure-shipment-consolidation-policies.md)
