---
title: "在庫分析コード当たりの移動平均原価の追跡"
description: "在庫分析コード グループは各在庫品目に割り当てられています。 したがって、品目の移動平均原価価格は、財務的に追跡されている在庫分析コードの選択に基づいて計算されます。"
author: YuyuScheller
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: InventOnhandItem
audience: Application User
ms.reviewer: yuyus
ms.search.scope: Core, AX 7.0.0, Operations, UnifiedOperations, Retail
ms.custom: 75053
ms.assetid: 68cc00f4-0f7a-4a7d-be90-8f2e0d0563d3
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: mguada
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: Human Translation
ms.sourcegitcommit: 08c38aada355583c5a6872f75b57db95d9b81786
ms.openlocfilehash: a88ec380810a9a2d7048d5a8773ebb5960e4cf86
ms.contentlocale: ja-jp
ms.lasthandoff: 07/18/2017

---

# <a name="tracking-running-average-cost-per-inventory-dimension"></a><span data-ttu-id="ef57b-104">在庫分析コード当たりの移動平均原価の追跡</span><span class="sxs-lookup"><span data-stu-id="ef57b-104">Tracking running average cost per inventory dimension</span></span>

[!include[banner](../includes/banner.md)]

[!include[retail name](../includes/retail-name.md)]


<span data-ttu-id="ef57b-105">在庫分析コード グループは各在庫品目に割り当てられています。</span><span class="sxs-lookup"><span data-stu-id="ef57b-105">An inventory dimension group is attached to every inventory item.</span></span> <span data-ttu-id="ef57b-106">したがって、品目の移動平均原価価格は、財務的に追跡されている在庫分析コードの選択に基づいて計算されます。</span><span class="sxs-lookup"><span data-stu-id="ef57b-106">Therefore, the running average cost price of an item is calculated based on the selected inventory dimensions that are being tracked financially.</span></span>

<span data-ttu-id="ef57b-107">在庫分析コードは製品、保管、および追跡の 3 種類があります。</span><span class="sxs-lookup"><span data-stu-id="ef57b-107">There are three types of inventory dimensions: product, storage, and tracking.</span></span> <span data-ttu-id="ef57b-108">製品分析コードは、コンフィギュレーション、サイズ、および色が含まれます。</span><span class="sxs-lookup"><span data-stu-id="ef57b-108">Product dimensions include configuration, size, and color.</span></span> <span data-ttu-id="ef57b-109">製品分析コードは常に財務的に追跡されます。</span><span class="sxs-lookup"><span data-stu-id="ef57b-109">Product dimensions are always tracked financially.</span></span> <span data-ttu-id="ef57b-110">保管と追跡用分析コードは、サイト、倉庫、場所、在庫状態、ライセンス プレート、バッチ番号、シリアル番号を含みます。</span><span class="sxs-lookup"><span data-stu-id="ef57b-110">Storage and tracking dimensions include site, warehouse, location, inventory status, license plate, batch number, and serial number.</span></span> <span data-ttu-id="ef57b-111">どの保管と追跡用分析コードが財務的に追跡されるかを指定できます。</span><span class="sxs-lookup"><span data-stu-id="ef57b-111">You can decide which storage and tracking dimensions are tracked financially.</span></span> 

<span data-ttu-id="ef57b-112">**例 1**</span><span class="sxs-lookup"><span data-stu-id="ef57b-112">**Example 1**</span></span> 

<span data-ttu-id="ef57b-113">品目に添付されている保管分析コード グループが倉庫によって財務的に追跡されている場合、移動平均原価価格は倉庫ごとに計算されます。</span><span class="sxs-lookup"><span data-stu-id="ef57b-113">If the storage dimension group that is attached to the item is financially tracked by warehouse, the running average cost price is calculated per warehouse.</span></span> <span data-ttu-id="ef57b-114">次の購買注文が請求されています。</span><span class="sxs-lookup"><span data-stu-id="ef57b-114">The following purchase orders have been invoiced:</span></span>

-   <span data-ttu-id="ef57b-115">原価価格が USD 10.00 で数量が 2 の発注書が倉庫 GW に対して請求されています。</span><span class="sxs-lookup"><span data-stu-id="ef57b-115">A purchase order for a quantity of 2 at a cost price of USD 10.00 has been invoiced for warehouse GW.</span></span>
-   <span data-ttu-id="ef57b-116">原価価格が USD 12.00 で数量が 3 の発注書が倉庫 GW に対して請求されています。</span><span class="sxs-lookup"><span data-stu-id="ef57b-116">A purchase order for a quantity of 3 at a cost price of USD 12.00 has been invoiced for warehouse GW.</span></span>
-   <span data-ttu-id="ef57b-117">原価価格が USD 15.00 で数量が 5 の発注書が倉庫 MW に対して請求されています。</span><span class="sxs-lookup"><span data-stu-id="ef57b-117">A purchase order for a quantity of 5 at a cost price of USD 15.00 has been invoiced for warehouse MW.</span></span>

<span data-ttu-id="ef57b-118">倉庫 GW の移動平均原価価格は USD 11.20 で、倉庫 MW の移動平均原価価格は USD 15.00 です。</span><span class="sxs-lookup"><span data-stu-id="ef57b-118">The running average cost price for warehouse GW is USD 11.20, and the running average cost price for warehouse MW is USD 15.00.</span></span> <span data-ttu-id="ef57b-119">販売注文請求書が倉庫 GW に対して転記されます。</span><span class="sxs-lookup"><span data-stu-id="ef57b-119">A sales order invoice is posted for warehouse GW.</span></span> <span data-ttu-id="ef57b-120">在庫と売却済商品の原価の価値 (在庫決算が実行される前で、マークがない) は、USD 11.20 です。</span><span class="sxs-lookup"><span data-stu-id="ef57b-120">The value of the inventory and the cost of goods sold (before inventory close is run and without marking) is USD 11.20.</span></span> <span data-ttu-id="ef57b-121">別の販売注文が倉庫 MW に対して転記されます。</span><span class="sxs-lookup"><span data-stu-id="ef57b-121">Another sales order is posted for warehouse MW.</span></span> <span data-ttu-id="ef57b-122">在庫と売却済商品の原価の価値 (在庫決算が実行される前で、マークがない) は、USD 15.00 です。</span><span class="sxs-lookup"><span data-stu-id="ef57b-122">The value of the inventory and the cost of goods sold (before inventory close is run and without marking) is USD 15.00.</span></span> 

<span data-ttu-id="ef57b-123">**例 2** 品目に関連付けられている保管分析コード グループが倉庫によって財務的に追跡され、また追跡用分析コード グループがバッチ番号によって財務的に追跡されている場合、移動平均原価価格はバッチごとに計算されます。</span><span class="sxs-lookup"><span data-stu-id="ef57b-123">**Example 2** If the storage dimension group that is attached to the item is financially tracked by warehouse, and the tracking dimension group is financially tracked by batch number, the running average cost price is calculated for each batch.</span></span> 

<span data-ttu-id="ef57b-124">**注記:** すべての財務分析コードを追跡して、原価価格を常に表示することをお勧めします。</span><span class="sxs-lookup"><span data-stu-id="ef57b-124">**Note:** We recommend that you always view the cost price for all financial dimensions that are being tracked.</span></span> <span data-ttu-id="ef57b-125">次の購買注文が請求されています。</span><span class="sxs-lookup"><span data-stu-id="ef57b-125">The following purchase orders have been invoiced:</span></span>

-   <span data-ttu-id="ef57b-126">原価価格が USD 10.00 で数量が 2 の発注書が倉庫 GW およびバッチ AAA に対して請求されています。</span><span class="sxs-lookup"><span data-stu-id="ef57b-126">A purchase order for a quantity of 2 at a cost price of USD 10.00 has been invoiced for warehouse GW and batch AAA.</span></span>
-   <span data-ttu-id="ef57b-127">原価価格が USD 12.00 で数量が 3 の発注書が倉庫 GW およびバッチ AAA に対して請求されています。</span><span class="sxs-lookup"><span data-stu-id="ef57b-127">A purchase order for a quantity of 3 at a cost price of USD 12.00 has been invoiced for warehouse GW and batch AAA.</span></span>
-   <span data-ttu-id="ef57b-128">原価価格が USD 15.00 で数量が 2 の発注書が倉庫 GW およびバッチ BBB に対して請求されています。</span><span class="sxs-lookup"><span data-stu-id="ef57b-128">A purchase order for a quantity of 2 at a cost price of USD 15.00 has been invoiced for warehouse GW and batch BBB.</span></span>

<span data-ttu-id="ef57b-129">倉庫 GW とバッチ AAA の移動平均原価価格は USD 11.20 で、倉庫 GW とバッチ BBB の移動平均原価価格は USD 15.00 です。</span><span class="sxs-lookup"><span data-stu-id="ef57b-129">The running average cost price for warehouse GW and batch AAA is USD 11.20, and the running average cost price for warehouse GW and batch BBB is USD 15.00.</span></span>




