---
title: 二重書き込みでの在庫状況
description: このトピックでは、二重書き込みでの在庫状況の確認方法について説明します。
author: RamaKrishnamoorthy
ms.date: 05/26/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User, IT Pro
ms.reviewer: rhaertle
ms.custom: ''
ms.assetid: ''
ms.search.region: global
ms.search.industry: ''
ms.author: ramasri
ms.dyn365.ops.version: ''
ms.search.validFrom: 2020-05-26
ms.openlocfilehash: 0fded78134b1427e6faea9656e1d3b02b467ae91
ms.sourcegitcommit: 74e47075eab2b0b28f82b0d57f439719847ecb01
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/07/2021
ms.locfileid: "6193410"
---
# <a name="inventory-availability-in-dual-write"></a><span data-ttu-id="a2c68-103">二重書き込みでの在庫状況</span><span class="sxs-lookup"><span data-stu-id="a2c68-103">Inventory availability in dual-write</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="a2c68-104">在庫状況を使用すると、Microsoft Dynamics 365 Sales の **見積**、**注文**、または **請求書** ページに製品を追加する前に、在庫を確認できます。</span><span class="sxs-lookup"><span data-stu-id="a2c68-104">By using inventory availability, you can check your inventory before you add a product to the **Quotations**, **Orders**, or **Invoices** page in Microsoft Dynamics 365 Sales.</span></span> <span data-ttu-id="a2c68-105">たとえば、[見込顧客から現金](dual-write-prospect-to-cash.md) の一つの重要なタスクとして在庫の確認と履行日の決定をおこないます。</span><span class="sxs-lookup"><span data-stu-id="a2c68-105">For example, you check inventory and determine a fulfillment date as one key task in the [prospect-to-cash](dual-write-prospect-to-cash.md) process.</span></span>

<span data-ttu-id="a2c68-106">十分な在庫がない場合は、予想在庫の入庫および払出に基づいて出荷日を見積もることができます。</span><span class="sxs-lookup"><span data-stu-id="a2c68-106">If you don't have enough inventory, you can estimate a delivery date, based on projected inventory receipts and issues.</span></span> <span data-ttu-id="a2c68-107">また、製品の納期回答可能在庫 (ATP) 情報を確認して、事前に定義されたタイム フェンスで ATP 数量を検索することもできます。</span><span class="sxs-lookup"><span data-stu-id="a2c68-107">You can also check the product's available-to-promise (ATP) information, where you can find the ATP quantity in the predefined time fence.</span></span>

## <a name="on-hand-inventory"></a><span data-ttu-id="a2c68-108">手持在庫</span><span class="sxs-lookup"><span data-stu-id="a2c68-108">On-hand inventory</span></span>

<span data-ttu-id="a2c68-109">Dynamics 365 Sales で、**見積**、**注文**、**請求書** の各ページのヘッダーに、新規の **手持在庫** ボタンが追加されました。</span><span class="sxs-lookup"><span data-stu-id="a2c68-109">In Dynamics 365 Sales, a new **On-hand Inventory** button has been added to the header of the **Quotes**, **Orders**, and **Invoices** pages.</span></span> <span data-ttu-id="a2c68-110">このボタンをクリックすると、ダイアログ ボックスが表示され、手持在庫を確認する会社と製品を指定できます。</span><span class="sxs-lookup"><span data-stu-id="a2c68-110">When you select this button, a dialog box appears, where you can specify the company and the product that you want to check the on-hand inventory for.</span></span> <span data-ttu-id="a2c68-111">このダイアログボックスには、[手持在庫](../../../../supply-chain/inventory/tasks/check-availability-stock.md) と同じ情報が表示されます。</span><span class="sxs-lookup"><span data-stu-id="a2c68-111">This dialog box shows the same information as [On-hand inventory](../../../../supply-chain/inventory/tasks/check-availability-stock.md).</span></span>

<span data-ttu-id="a2c68-112">このダイアログ ボックスでは、Dynamics 365 Supply Chain Management からの在庫情報が返されます。</span><span class="sxs-lookup"><span data-stu-id="a2c68-112">The dialog box returns the inventory information from Dynamics 365 Supply Chain Management.</span></span> <span data-ttu-id="a2c68-113">この情報には、次の数量が含まれています。</span><span class="sxs-lookup"><span data-stu-id="a2c68-113">This information includes the following quantities:</span></span>

- <span data-ttu-id="a2c68-114">手持在庫数量</span><span class="sxs-lookup"><span data-stu-id="a2c68-114">On-hand quantity</span></span>
- <span data-ttu-id="a2c68-115">予約済み手持数量</span><span class="sxs-lookup"><span data-stu-id="a2c68-115">Reserved on-hand quantity</span></span>
- <span data-ttu-id="a2c68-116">使用可能な手持数量</span><span class="sxs-lookup"><span data-stu-id="a2c68-116">Available on-hand quantity</span></span>
- <span data-ttu-id="a2c68-117">注文済数量</span><span class="sxs-lookup"><span data-stu-id="a2c68-117">Ordered quantity</span></span>
- <span data-ttu-id="a2c68-118">注文中数量</span><span class="sxs-lookup"><span data-stu-id="a2c68-118">On-order quantity</span></span>
- <span data-ttu-id="a2c68-119">引当済の注文済数量</span><span class="sxs-lookup"><span data-stu-id="a2c68-119">Reserved ordered quantity</span></span>
- <span data-ttu-id="a2c68-120">利用可能な合計数量</span><span class="sxs-lookup"><span data-stu-id="a2c68-120">Total available quantity</span></span>

## <a name="atp-information"></a><span data-ttu-id="a2c68-121">ATP 情報</span><span class="sxs-lookup"><span data-stu-id="a2c68-121">ATP information</span></span>

<span data-ttu-id="a2c68-122">Sales では、**ATP情報** ボタンが **見積**、**注文**、**請求書** の各ページの品目に追加されました。</span><span class="sxs-lookup"><span data-stu-id="a2c68-122">In Sales, a new **ATP Information** button has been added to line items on the **Quotes**, **Orders**, and **Invoices** pages.</span></span> <span data-ttu-id="a2c68-123">このボタンを選択すると、ダイアログ ボックスが表示され、会社、製品、在庫サイト、在庫倉庫、注文数量を指定できます。</span><span class="sxs-lookup"><span data-stu-id="a2c68-123">When you select this button, a dialog box appears, where you can specify the company, product, inventory site, inventory warehouse, and order quantity.</span></span> <span data-ttu-id="a2c68-124">このダイアログボックスの設定は、[注文-受注](../../../../supply-chain/sales-marketing/delivery-dates-available-promise-calculations.md#atp-calculations) に記述されている設定と同じです。</span><span class="sxs-lookup"><span data-stu-id="a2c68-124">This dialog box has the same settings that are described in [Order promising](../../../../supply-chain/sales-marketing/delivery-dates-available-promise-calculations.md#atp-calculations).</span></span>

<span data-ttu-id="a2c68-125">このダイアログ ボックスでは、Supply Chain Management からの ATP 情報が返されます。</span><span class="sxs-lookup"><span data-stu-id="a2c68-125">The dialog box returns the ATP information from Supply Chain Management.</span></span> <span data-ttu-id="a2c68-126">この情報には、次の数量が含まれています。</span><span class="sxs-lookup"><span data-stu-id="a2c68-126">This information includes the following quantities:</span></span>

- <span data-ttu-id="a2c68-127">ATP 数量</span><span class="sxs-lookup"><span data-stu-id="a2c68-127">ATP quantity</span></span>
- <span data-ttu-id="a2c68-128">受入数量</span><span class="sxs-lookup"><span data-stu-id="a2c68-128">Receipt quantity</span></span>
- <span data-ttu-id="a2c68-129">払出数量</span><span class="sxs-lookup"><span data-stu-id="a2c68-129">Issue quantity</span></span>
- <span data-ttu-id="a2c68-130">手持在庫数量</span><span class="sxs-lookup"><span data-stu-id="a2c68-130">On-hand quantity</span></span>

## <a name="how-it-works"></a><span data-ttu-id="a2c68-131">この機能の動作</span><span class="sxs-lookup"><span data-stu-id="a2c68-131">How it works</span></span>

<span data-ttu-id="a2c68-132">**見積書**、**注文**、または **請求書** ページの **手持在庫** ボタンを選択すると、デュアル書き込み呼び出しが **手持在庫** API につくられます。</span><span class="sxs-lookup"><span data-stu-id="a2c68-132">When you select the **On-hand Inventory** button on the **Quotes**, **Orders**, or **Invoices** page, a live dual-write call is made to the **Onhand inventory** API.</span></span> <span data-ttu-id="a2c68-133">API によって、特定の製品の在庫が計算されます。</span><span class="sxs-lookup"><span data-stu-id="a2c68-133">The API calculates the on-hand inventory for the given product.</span></span> <span data-ttu-id="a2c68-134">この結果は、**InventCDSInventoryOnHandRequestEntity** と **InventCDSInventoryOnHandEntryEntity** テーブルに格納された後、デュアル書き込みによって Dataverse に書き込まれます。</span><span class="sxs-lookup"><span data-stu-id="a2c68-134">The result is stored in the **InventCDSInventoryOnHandRequestEntity** and **InventCDSInventoryOnHandEntryEntity** tables, and then is written to Dataverse by dual-write.</span></span> <span data-ttu-id="a2c68-135">この機能を使用するには、次のデュアル 書き込みマップを実行する必要があります。</span><span class="sxs-lookup"><span data-stu-id="a2c68-135">To use this functionality, you need to run the following dual-write maps.</span></span> <span data-ttu-id="a2c68-136">マップの実行時に初期同期をスキップします。</span><span class="sxs-lookup"><span data-stu-id="a2c68-136">Skip initial synchronization when you run the maps.</span></span>

- <span data-ttu-id="a2c68-137">CDS 在庫の手持在庫エントリー (msdyn_inventoryonhandentries)</span><span class="sxs-lookup"><span data-stu-id="a2c68-137">CDS inventory on-hand entries (msdyn_inventoryonhandentries)</span></span>
- <span data-ttu-id="a2c68-138">CDS 在庫の手持在庫要求 (msdyn_inventoryonhandrequests)</span><span class="sxs-lookup"><span data-stu-id="a2c68-138">CDS inventory on-hand requests (msdyn_inventoryonhandrequests)</span></span>

## <a name="templates"></a><span data-ttu-id="a2c68-139">テンプレート</span><span class="sxs-lookup"><span data-stu-id="a2c68-139">Templates</span></span>
<span data-ttu-id="a2c68-140">次のテンプレートを使用して、手持在庫の在庫データを公開します。</span><span class="sxs-lookup"><span data-stu-id="a2c68-140">The following templates are available for the exposing the onhand inventory data.</span></span>

<span data-ttu-id="a2c68-141">Finance and Operations アプリ</span><span class="sxs-lookup"><span data-stu-id="a2c68-141">Finance and Operations apps</span></span> | <span data-ttu-id="a2c68-142">Customer Engagement アプリ</span><span class="sxs-lookup"><span data-stu-id="a2c68-142">Customer engagement app</span></span> | <span data-ttu-id="a2c68-143">説明</span><span class="sxs-lookup"><span data-stu-id="a2c68-143">Description</span></span> 
---|---|---
[<span data-ttu-id="a2c68-144">CDS 手持在庫エントリ</span><span class="sxs-lookup"><span data-stu-id="a2c68-144">CDS inventory on-hand entries</span></span>](#145) | <span data-ttu-id="a2c68-145">msdyn_inventoryonhandentries</span><span class="sxs-lookup"><span data-stu-id="a2c68-145">msdyn_inventoryonhandentries</span></span> |
[<span data-ttu-id="a2c68-146">CDS 手持在庫要求</span><span class="sxs-lookup"><span data-stu-id="a2c68-146">CDS inventory on-hand requests</span></span>](#147) | <span data-ttu-id="a2c68-147">msdyn_inventoryonhandrequests</span><span class="sxs-lookup"><span data-stu-id="a2c68-147">msdyn_inventoryonhandrequests</span></span> |

[!include [banner](../../includes/dual-write-symbols.md)]

###  <a name="cds-inventory-on-hand-entries-msdyn_inventoryonhandentries"></a><a name="145"></a><span data-ttu-id="a2c68-148">CDS 在庫の手持在庫エントリー (msdyn_inventoryonhandentries)</span><span class="sxs-lookup"><span data-stu-id="a2c68-148">CDS inventory on-hand entries (msdyn_inventoryonhandentries)</span></span>

<span data-ttu-id="a2c68-149">このテンプレートは、Finance and Operations アプリと Dataverse 間でデータを同期します。</span><span class="sxs-lookup"><span data-stu-id="a2c68-149">This template synchronizes data between Finance and Operations apps and Dataverse.</span></span>

<span data-ttu-id="a2c68-150">Finance and Operations フィールド</span><span class="sxs-lookup"><span data-stu-id="a2c68-150">Finance and Operations field</span></span> | <span data-ttu-id="a2c68-151">タイプのマッピング</span><span class="sxs-lookup"><span data-stu-id="a2c68-151">Map type</span></span> | <span data-ttu-id="a2c68-152">Customer Engagement フィールド</span><span class="sxs-lookup"><span data-stu-id="a2c68-152">Customer engagement field</span></span> | <span data-ttu-id="a2c68-153">既定値</span><span class="sxs-lookup"><span data-stu-id="a2c68-153">Default value</span></span>
---|---|---|---
`REQUESTID` | = | `msdyn_request.msdyn_requestid` |
`INVENTORYSITEID` | = | `msdyn_inventorysite.msdyn_siteid` |
`INVENTORYWAREHOUSEID` | = | `msdyn_inventorywarehouse.msdyn_warehouseidentifier` |
`AVAILABLEONHANDQUANTITY` | > | `msdyn_availableonhandquantity` |
`AVAILABLEORDEREDQUANTITY` | > | `msdyn_availableorderedquantity` |
`ONHANDQUANTITY` | > | `msdyn_onhandquantity` |
`ONORDERQUANTITY` | > | `msdyn_onorderquantity` |
`ORDEREDQUANTITY` | > | `msdyn_orderedquantity` |
`RESERVEDONHANDQUANTITY` | > | `msdyn_reservedonhandquantity` |
`RESERVEDORDEREDQUANTITY` | > | `msdyn_reservedorderedquantity` |
`TOTALAVAILABLEQUANTITY` | > | `msdyn_totalavailablequantity` |
`ATPDATE` | = | `msdyn_atpdate` |
`ATPQUANTITY` | > | `msdyn_atpquantity` |
`PROJECTEDISSUEQUANTITY` | > | `msdyn_projectedissuequantity` |
`PROJECTEDONHANDQUANTITY` | > | `msdyn_projectedonhandquantity` |
`PROJECTEDRECEIPTQUANTITY` | > | `msdyn_projectedreceiptquantity` |
`ORDERQUANTITY` | > | `msdyn_orderquantity` |
`UNAVAILABLEONHANDQUANTITY` | > | `msdyn_unavailableonhandquantity` |

###  <a name="cds-inventory-on-hand-requests-msdyn_inventoryonhandrequests"></a><a name="147"></a><span data-ttu-id="a2c68-154">CDS 在庫の手持在庫要求 (msdyn_inventoryonhandrequests)</span><span class="sxs-lookup"><span data-stu-id="a2c68-154">CDS inventory on-hand requests (msdyn_inventoryonhandrequests)</span></span>

<span data-ttu-id="a2c68-155">このテンプレートは、Finance and Operations アプリと Dataverse 間でデータを同期します。</span><span class="sxs-lookup"><span data-stu-id="a2c68-155">This template synchronizes data between Finance and Operations apps and Dataverse.</span></span>

<span data-ttu-id="a2c68-156">Finance and Operations フィールド</span><span class="sxs-lookup"><span data-stu-id="a2c68-156">Finance and Operations field</span></span> | <span data-ttu-id="a2c68-157">タイプのマッピング</span><span class="sxs-lookup"><span data-stu-id="a2c68-157">Map type</span></span> | <span data-ttu-id="a2c68-158">Customer Engagement フィールド</span><span class="sxs-lookup"><span data-stu-id="a2c68-158">Customer engagement field</span></span> | <span data-ttu-id="a2c68-159">既定値</span><span class="sxs-lookup"><span data-stu-id="a2c68-159">Default value</span></span>
---|---|---|---
`REQUESTID` | = | `msdyn_requestid` |
`PRODUCTNUMBER` | < | `msdyn_product.msdyn_productnumber` |
`ISATPCALCULATION` | << | `msdyn_isatpcalculation` |
`ORDERQUANTITY` | < | `msdyn_orderquantity` |
`INVENTORYSITEID` | < | `msdyn_inventorysite.msdyn_siteid` |
`INVENTORYWAREHOUSEID` | < | `msdyn_inventorywarehouse.msdyn_warehouseidentifier` |
`REFERENCENUMBER` | < | `msdyn_referencenumber` |
`LINECREATIONSEQUENCENUMBER` | < | `msdyn_linecreationsequencenumber` |






[!INCLUDE[footer-include](../../../../includes/footer-banner.md)]