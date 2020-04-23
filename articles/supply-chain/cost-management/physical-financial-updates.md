---
title: 現物更新と財務更新
description: このトピックでは、在庫数量を増減させるトランザクションのタイプについて、その概要を説明します。
author: AndersGirke
manager: tfehr
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: InventTrans, InventTransVoucher
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.custom: 75023
ms.assetid: 128340e1-c573-48e6-b835-6c350d8dd0fb
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: mguada
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 5ea79bd9c6561c4e4f6fad2c177f44fe62bdea5b
ms.sourcegitcommit: 4f9912439ff78acf0c754d5bff972c4b85763093
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/02/2020
ms.locfileid: "3214645"
---
# <a name="physical-and-financial-updates"></a><span data-ttu-id="51b0f-103">現物更新と財務更新</span><span class="sxs-lookup"><span data-stu-id="51b0f-103">Physical and financial updates</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="51b0f-104">このトピックでは、在庫数量を増減させるトランザクションのタイプについて、その概要を説明します。</span><span class="sxs-lookup"><span data-stu-id="51b0f-104">This topic provides an overview of which types of transactions increase or decrease inventory quantities.</span></span> 

<span data-ttu-id="51b0f-105">在庫トランザクションは、Dynamics 365 Supply Chain Management で現物更新および財務更新できます。</span><span class="sxs-lookup"><span data-stu-id="51b0f-105">Inventory transactions can be physically updated and financially updated in Dynamics 365 Supply Chain Management.</span></span> <span data-ttu-id="51b0f-106">現物トランザクションと財務トランザクションによっては、在庫数量を増加または減少させるものがあります。</span><span class="sxs-lookup"><span data-stu-id="51b0f-106">Some types of physical and financial transactions increase inventory quantities, whereas others decrease the quantity.</span></span>

## <a name="physical-increases"></a><span data-ttu-id="51b0f-107">現物の増加</span><span class="sxs-lookup"><span data-stu-id="51b0f-107">Physical increases</span></span>
<span data-ttu-id="51b0f-108">現物トランザクションが転記されると、トランザクション レコードのステータスは **入庫済** になります。</span><span class="sxs-lookup"><span data-stu-id="51b0f-108">When a physical transaction is posted, the status of the transaction record is **Received**.</span></span> <span data-ttu-id="51b0f-109">次のトランザクションは現物の増加と見なされます。</span><span class="sxs-lookup"><span data-stu-id="51b0f-109">The following transactions are considered physical increases:</span></span>

-   <span data-ttu-id="51b0f-110">発注書入庫</span><span class="sxs-lookup"><span data-stu-id="51b0f-110">Purchase order receipt</span></span>
-   <span data-ttu-id="51b0f-111">販売注文梱包明細票返品</span><span class="sxs-lookup"><span data-stu-id="51b0f-111">Sales order packing slip return</span></span>
-   <span data-ttu-id="51b0f-112">製造オーダーの終了を報告</span><span class="sxs-lookup"><span data-stu-id="51b0f-112">Reporting a production order as finished</span></span>
-   <span data-ttu-id="51b0f-113">製造オーダー ピッキング リストの副産物</span><span class="sxs-lookup"><span data-stu-id="51b0f-113">By-product on a production order picking list</span></span>

## <a name="financial-increases"></a><span data-ttu-id="51b0f-114">財務上の増加</span><span class="sxs-lookup"><span data-stu-id="51b0f-114">Financial increases</span></span>
<span data-ttu-id="51b0f-115">財務入庫トランザクションが転記されると、数量を増加させるトランザクション レコードのステータスは **購買済** になります。</span><span class="sxs-lookup"><span data-stu-id="51b0f-115">When a financial receipt transaction is posted, the status of the transaction record that increases the quantity is **Purchased**.</span></span> <span data-ttu-id="51b0f-116">次のトランザクションは、財務上の増加と見なされます。</span><span class="sxs-lookup"><span data-stu-id="51b0f-116">The following transactions are considered financial increases:</span></span>

-   <span data-ttu-id="51b0f-117">仕入先請求書</span><span class="sxs-lookup"><span data-stu-id="51b0f-117">Vendor invoice</span></span>
-   <span data-ttu-id="51b0f-118">返品用販売注文請求書</span><span class="sxs-lookup"><span data-stu-id="51b0f-118">Sales order invoice for a return</span></span>
-   <span data-ttu-id="51b0f-119">製造オーダー原価計算</span><span class="sxs-lookup"><span data-stu-id="51b0f-119">Production order costing</span></span>
-   <span data-ttu-id="51b0f-120">振替、損益、棚卸、部品表、移動などの正の数量の在庫仕訳帳</span><span class="sxs-lookup"><span data-stu-id="51b0f-120">Positive quantity inventory journals, such as movement, profit and loss, counting, bill of materials, and transfer</span></span>

## <a name="transactions-that-increase-quantity"></a><span data-ttu-id="51b0f-121">数量を増加させるトランザクション</span><span class="sxs-lookup"><span data-stu-id="51b0f-121">Transactions that increase quantity</span></span>
<span data-ttu-id="51b0f-122">数量を増加させるトランザクションは移動平均原価価格で転記されます。</span><span class="sxs-lookup"><span data-stu-id="51b0f-122">Transactions that increase quantity are posted at the running average cost price.</span></span> <span data-ttu-id="51b0f-123">計算済の移動平均原価価格は、財務的に追跡される在庫分析コードごとに、各トランザクションの原価を基準とします。</span><span class="sxs-lookup"><span data-stu-id="51b0f-123">The calculated running average cost price is based on the cost of each of these transactions for each inventory dimension that is being tracked financially.</span></span> <span data-ttu-id="51b0f-124">移動平均原価価格については、[[移動平均原価価格](running-average-cost-price.md)] を参照ください。</span><span class="sxs-lookup"><span data-stu-id="51b0f-124">For information about running average cost prices, see [Running average cost price](running-average-cost-price.md).</span></span>

## <a name="transactions-that-decrease-quantity"></a><span data-ttu-id="51b0f-125">数量を減少させるトランザクション</span><span class="sxs-lookup"><span data-stu-id="51b0f-125">Transactions that decrease quantity</span></span>
<span data-ttu-id="51b0f-126">計算済の移動平均原価価格は、在庫にどの在庫モデルが関連付けられているかに関係なく、数量を減少させるトランザクションが転記される際に使用されます。</span><span class="sxs-lookup"><span data-stu-id="51b0f-126">The calculated running average cost price is used  when a transaction that decreases quantity is posted, regardless of the inventory model that is associated with that inventory.</span></span> <span data-ttu-id="51b0f-127">転記される前に、数量を減少させるトランザクションが別のトランザクションにすでにマークされていてはいけません。</span><span class="sxs-lookup"><span data-stu-id="51b0f-127">The transaction that decreases quantity must not have been marked to another transaction before it was posted.</span></span> <span data-ttu-id="51b0f-128">現物手持在庫がマイナスになる場合、**品目**ページで品目に対して定義されている在庫原価を使用します。</span><span class="sxs-lookup"><span data-stu-id="51b0f-128">If the physical on-hand inventory becomes negative, the inventory cost that is defined for the item on the **Item** page is used.</span></span> 

> [!NOTE]
> <span data-ttu-id="51b0f-129">マルチサイト機能が有効になっている場合、この原価は**既定の注文設定**ページでサイトに対して定義されている在庫原価になります。</span><span class="sxs-lookup"><span data-stu-id="51b0f-129">If multisite functionality is enabled, this cost will instead be the inventory cost that is defined for a site on the **Default order settings** page.</span></span>

## <a name="physical-issues-vs-financial-issues"></a><span data-ttu-id="51b0f-130">現物払出と財務払出</span><span class="sxs-lookup"><span data-stu-id="51b0f-130">Physical issues vs. financial issues</span></span>
<span data-ttu-id="51b0f-131">現物払出トランザクションが転記されると、トランザクション レコードのステータスは **控除済** になります。</span><span class="sxs-lookup"><span data-stu-id="51b0f-131">When a physical issue transaction is posted, the status of the transaction record is **Deducted**.</span></span> <span data-ttu-id="51b0f-132">次のトランザクションは現物払出と見なされます。</span><span class="sxs-lookup"><span data-stu-id="51b0f-132">The following transactions are considered physical issues:</span></span>

-   <span data-ttu-id="51b0f-133">製造オーダー ピッキング リスト仕訳帳</span><span class="sxs-lookup"><span data-stu-id="51b0f-133">Production order picking list journal</span></span>
-   <span data-ttu-id="51b0f-134">販売注文梱包明細票</span><span class="sxs-lookup"><span data-stu-id="51b0f-134">Sales order packing slip</span></span>
-   <span data-ttu-id="51b0f-135">発注書梱包明細返品</span><span class="sxs-lookup"><span data-stu-id="51b0f-135">Purchase order packing slip return</span></span>

<span data-ttu-id="51b0f-136">財務トランザクションを転記すると、トランザクション レコードのステータスが **売却済** になります。</span><span class="sxs-lookup"><span data-stu-id="51b0f-136">When a financial transaction is posted, the status of the transaction record is **Sold**.</span></span> <span data-ttu-id="51b0f-137">次のトランザクションは財務払出と見なされます。</span><span class="sxs-lookup"><span data-stu-id="51b0f-137">The following transactions are considered financial issues:</span></span>

-   <span data-ttu-id="51b0f-138">製造オーダーの終了</span><span class="sxs-lookup"><span data-stu-id="51b0f-138">Ending a production order</span></span>
-   <span data-ttu-id="51b0f-139">販売注文請求書</span><span class="sxs-lookup"><span data-stu-id="51b0f-139">Sales order invoice</span></span>
-   <span data-ttu-id="51b0f-140">仕入先請求書返品</span><span class="sxs-lookup"><span data-stu-id="51b0f-140">Vendor invoice return</span></span>
-   <span data-ttu-id="51b0f-141">振替、損益、棚卸、部品表、移動などの負の数量の在庫仕訳帳</span><span class="sxs-lookup"><span data-stu-id="51b0f-141">Negative quantity inventory journals, such as movement, profit and loss, counting, bill of materials, and transfer</span></span>

<span data-ttu-id="51b0f-142">数量を減少させるトランザクションは移動平均原価価格で転記されます。</span><span class="sxs-lookup"><span data-stu-id="51b0f-142">Transactions that decrease quantity are posted at the running average cost price.</span></span> <span data-ttu-id="51b0f-143">したがって、各品目に割り当てられている在庫モデルに基づいて、出庫トランザクションが入庫トランザクションに対して決済されるために、在庫原価計算手順が必要です。</span><span class="sxs-lookup"><span data-stu-id="51b0f-143">Therefore, the inventory close procedure is required in order to settle issue transactions to receipt transactions, based on the inventory model that is assigned to each item.</span></span>
