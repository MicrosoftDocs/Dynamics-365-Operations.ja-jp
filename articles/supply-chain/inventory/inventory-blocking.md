---
title: "在庫ブロック"
description: "この記事は、Microsoft Dynamics 365 for Finance and Operations の品質検査プロセスの一部である在庫ブロックの概要を示します。 在庫ブロックは、品目が処理または消費されるのを防ぐために使用できます。"
author: perlynne
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: InventBlocking, InventQualityOrderTable
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.custom: 2094
ms.assetid: 1968e32f-eff9-4c17-8f7f-a870f0c38fbc
ms.search.region: Global
ms.search.industry: Distribution
ms.author: perlynne
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: d9747ba144d56c9410846769e5465372c89ea111
ms.openlocfilehash: eb6291e2f012f148b247b747f84155b96cf09677
ms.contentlocale: ja-jp
ms.lasthandoff: 08/07/2018

---

# <a name="inventory-blocking"></a><span data-ttu-id="9d0a6-104">在庫ブロック</span><span class="sxs-lookup"><span data-stu-id="9d0a6-104">Inventory blocking</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="9d0a6-105">この記事は、Microsoft Dynamics 365 for Finance and Operations の品質検査プロセスの一部である在庫ブロックの概要を示します。</span><span class="sxs-lookup"><span data-stu-id="9d0a6-105">This article provides an overview of inventory blocking, which is part of the quality inspection process in Microsoft Dynamics 365 for Finance and Operations.</span></span> <span data-ttu-id="9d0a6-106">在庫ブロックは、品目が処理または消費されるのを防ぐために使用できます。</span><span class="sxs-lookup"><span data-stu-id="9d0a6-106">You can use inventory blocking to prevent items from being processed or consumed.</span></span>

<span data-ttu-id="9d0a6-107">在庫品目は、次の方法でブロックできます。</span><span class="sxs-lookup"><span data-stu-id="9d0a6-107">You can block inventory items in the following ways:</span></span>
-   <span data-ttu-id="9d0a6-108">手動</span><span class="sxs-lookup"><span data-stu-id="9d0a6-108">Manually</span></span>
-   <span data-ttu-id="9d0a6-109">品質指示を作成して</span><span class="sxs-lookup"><span data-stu-id="9d0a6-109">By creating a quality order</span></span>
-   <span data-ttu-id="9d0a6-110">品質指示を生成するプロセスを使用して</span><span class="sxs-lookup"><span data-stu-id="9d0a6-110">By using a process that generates a quality order</span></span>
-   <span data-ttu-id="9d0a6-111">在庫状態ブロックを使用</span><span class="sxs-lookup"><span data-stu-id="9d0a6-111">By using inventory status blocking</span></span>

## <a name="blocking-items-manually"></a><span data-ttu-id="9d0a6-112">手動での品目のブロック</span><span class="sxs-lookup"><span data-stu-id="9d0a6-112">Blocking items manually</span></span>
<span data-ttu-id="9d0a6-113">**在庫ブロック** ページでトランザクションを作成することで、品目の数量をブロックできます。</span><span class="sxs-lookup"><span data-stu-id="9d0a6-113">You can block a quantity of an item by creating a transaction on the **Inventory blocking** page.</span></span> <span data-ttu-id="9d0a6-114">手動でブロックできるのは、手持在庫として使用可能な品目のみです。</span><span class="sxs-lookup"><span data-stu-id="9d0a6-114">Only items that are available as on-hand inventory can be blocked manually.</span></span> <span data-ttu-id="9d0a6-115">数量を手動でブロックする場合は、計画を行う際に、入庫予定を予定手持数量として含めるかどうか決める必要があります。</span><span class="sxs-lookup"><span data-stu-id="9d0a6-115">For manually blocked quantities, you must decide whether planning activities include expected receipts as an expected on-hand quantity.</span></span> <span data-ttu-id="9d0a6-116">入庫予定とは、検査の完了後に手持在庫として使用可能になる予定の、ブロックされた品目です。</span><span class="sxs-lookup"><span data-stu-id="9d0a6-116">Expected receipts are blocked items that you expect to be available as on-hand inventory after inspection is completed.</span></span> <span data-ttu-id="9d0a6-117">予定日は変更できます。</span><span class="sxs-lookup"><span data-stu-id="9d0a6-117">You can maintain the expected date.</span></span> <span data-ttu-id="9d0a6-118">既定では、品質指示によってブロックされている品目について、**入庫予定**オプションが選択されます。</span><span class="sxs-lookup"><span data-stu-id="9d0a6-118">By default, the **Expected receipts** option is selected for items that are blocked through a quality order.</span></span> <span data-ttu-id="9d0a6-119">手動でブロックした数量は、**在庫ブロック** ページでトランザクションを削除することにより、キャンセルできます。</span><span class="sxs-lookup"><span data-stu-id="9d0a6-119">You can cancel a manual block on a quantity by deleting the transaction on the **Inventory blocking** page.</span></span>

## <a name="blocking-items-by-creating-a-quality-order"></a><span data-ttu-id="9d0a6-120">品質指示の作成による品目のブロック</span><span class="sxs-lookup"><span data-stu-id="9d0a6-120">Blocking items by creating a quality order</span></span>
<span data-ttu-id="9d0a6-121">**品質指示**ページの品質指示の作成によって確認する必要がある品目を指定できます。</span><span class="sxs-lookup"><span data-stu-id="9d0a6-121">You can specify items that must be inspected by creating a quality order on the **Quality orders** page.</span></span> <span data-ttu-id="9d0a6-122">品質指示を作成すると、指定する品目の数量がブロックされます。</span><span class="sxs-lookup"><span data-stu-id="9d0a6-122">When you create a quality order, the quantity that you specify for an item is blocked.</span></span> <span data-ttu-id="9d0a6-123">品質指示に関連付けられるサンプリング計画は、検査する必要のある項目の数量のみを制御します。ブロックする数量ではありません。</span><span class="sxs-lookup"><span data-stu-id="9d0a6-123">The sampling plan that is associated with a quality order controls only the quantity of items that must be inspected, not the quantity that is blocked.</span></span> <span data-ttu-id="9d0a6-124">品質指示に入力される品目の数量は、ブロックされる数量になります。サンプリング計画で検査に送るように指定する数量とは無関係です。</span><span class="sxs-lookup"><span data-stu-id="9d0a6-124">The quantity that is entered on the quality order is the quantity that is blocked, regardless of the quantity that the sampling plan specifies should be sent for inspection.</span></span>

## <a name="blocking-items-by-using-a-process-that-generates-a-quality-order"></a><span data-ttu-id="9d0a6-125">品質指示を生成するプロセスによる品目のブロック</span><span class="sxs-lookup"><span data-stu-id="9d0a6-125">Blocking items by using a process that generates a quality order</span></span>
<span data-ttu-id="9d0a6-126">品質プロセス中で品目が検査必要となっている場合、その品目の数量が自動的にブロックされます。</span><span class="sxs-lookup"><span data-stu-id="9d0a6-126">If a quality process specifies that an item must be inspected, a quantity of the item is blocked automatically.</span></span> <span data-ttu-id="9d0a6-127">したがって、品質指示が自動的に生成されると、品質指示に関連付けられている品目サンプリング計画によって、ブロックする品目の数量と、検査する品目の数量の両方が制御されます。</span><span class="sxs-lookup"><span data-stu-id="9d0a6-127">Therefore, when a quality order is generated automatically, the item sampling plan that is associated with the quality order controls the both quantity of items that is blocked and the quantity that must be inspected.</span></span> <span data-ttu-id="9d0a6-128">**品目サンプリング** ページの**完全ブロック** オプションがオンの場合は、たとえば、購買注文明細行について、その全数量が検査中にブロックされます。品目のサンプリング数量には関係しません。</span><span class="sxs-lookup"><span data-stu-id="9d0a6-128">If the **Full blocking** option on the **Item sampling** page is selected, the full quantity of, for example, a purchase order line is blocked during inspection, regardless of the item sampling quantity.</span></span>
### <a name="example"></a><span data-ttu-id="9d0a6-129">例</span><span class="sxs-lookup"><span data-stu-id="9d0a6-129">Example</span></span>

<span data-ttu-id="9d0a6-130">次の例では、発注書の梱包明細が転記されると、品質指示が生成されます。</span><span class="sxs-lookup"><span data-stu-id="9d0a6-130">In the following example, a quality order is generated when a purchase order packing slip is posted.</span></span> <span data-ttu-id="9d0a6-131">**品質関連**ページでは、発注書の梱包明細の転記処理が、品質指示を有効にするプロセスとして指定してあります。</span><span class="sxs-lookup"><span data-stu-id="9d0a6-131">On the **Quality associations** page, you specified that posting of a purchase order packing slip is the process that activates a quality order.</span></span>

|<span data-ttu-id="9d0a6-132">段取り</span><span class="sxs-lookup"><span data-stu-id="9d0a6-132">Setup</span></span>                                                                     |<span data-ttu-id="9d0a6-133">ユーザー アクション</span><span class="sxs-lookup"><span data-stu-id="9d0a6-133">User action</span></span>                 |<span data-ttu-id="9d0a6-134">結果</span><span class="sxs-lookup"><span data-stu-id="9d0a6-134">Result</span></span>             |
|--------------------------------------------------------------------------|----------------------------|-------------------|
| <span data-ttu-id="9d0a6-135">品質関連によって、発注書の梱包明細が転記されたときに、品質指示が生成される必要のあることが指定されます。</span><span class="sxs-lookup"><span data-stu-id="9d0a6-135">A quality association specifies that a quality order must be generated when a purchase order packing slip is posted.</span></span> <span data-ttu-id="9d0a6-136">品質指示の品目サンプリング設定によって、購買注文明細行の数量の 10% を検査しなければならないことが指定されます。</span><span class="sxs-lookup"><span data-stu-id="9d0a6-136">The item sampling setup of the quality order specifies that 10 percent of the quantity on the purchase order line must be inspected.</span></span> <span data-ttu-id="9d0a6-137">さらに、品目サンプリング設定で**完全ブロック** オプションが選択されているため、検査に送られる数量とは関係なく、購買注文明細行の全数量を検査中にブロックする必要があります。</span><span class="sxs-lookup"><span data-stu-id="9d0a6-137">Furthermore, because the **Full blocking** option selected in the item sampling setup, the full quantity of the purchase order line must be blocked during inspection, regardless of the quantity that is sent for inspection.</span></span> | <span data-ttu-id="9d0a6-138">梱包明細を転記します。</span><span class="sxs-lookup"><span data-stu-id="9d0a6-138">The packing slip is posted.</span></span> | <span data-ttu-id="9d0a6-139">品質指示が生成されます。</span><span class="sxs-lookup"><span data-stu-id="9d0a6-139">A quality order is generated.</span></span> <span data-ttu-id="9d0a6-140">品目の発注書数量の 10% が検査に送られます。</span><span class="sxs-lookup"><span data-stu-id="9d0a6-140">Ten percent of the purchase order quantity for the item is sent to inspection.</span></span> <span data-ttu-id="9d0a6-141">購買注文明細行の全数量がブロックされます。</span><span class="sxs-lookup"><span data-stu-id="9d0a6-141">The full quantity of the purchase order line is blocked.</span></span> |

## <a name="blocking-items-by-using-inventory-status-blocking"></a><span data-ttu-id="9d0a6-142">在庫状態ブロックを使用した品目のブロック</span><span class="sxs-lookup"><span data-stu-id="9d0a6-142">Blocking items by using inventory status blocking</span></span>
<span data-ttu-id="9d0a6-143">**在庫状態**ページの**在庫ブロック**パラメータを使用すると、どの在庫状態をブロック状態にするか指定できます。</span><span class="sxs-lookup"><span data-stu-id="9d0a6-143">You can specify which inventory statuses are blocking statuses by using the **Inventory blocking** parameter on the **Inventory statuses** page.</span></span> <span data-ttu-id="9d0a6-144">在庫ステータスは、製造オーダー、販売注文、移動オーダー、出荷トランザクション、およびプロジェクト統合のブロック状態としては使用できません。</span><span class="sxs-lookup"><span data-stu-id="9d0a6-144">You can't use inventory statuses as blocking statuses for production orders, sales orders, transfer orders, outbound transactions, or project integrations.</span></span> <span data-ttu-id="9d0a6-145">出荷作業の場合、使用可能な在庫状態の品目を使用します。</span><span class="sxs-lookup"><span data-stu-id="9d0a6-145">For outbound work, use items that have an available inventory status.</span></span> <span data-ttu-id="9d0a6-146">**破損**の状態の品目があり、マスター プランがこれらの品目で実行している場合、品目は存在しない見なされ、棚卸資産は自動的に補充されます。</span><span class="sxs-lookup"><span data-stu-id="9d0a6-146">If items have a status of **Broken**, and master planning is run on those items, the items are considered missing, and inventory is automatically replenished.</span></span>



<a name="additional-resources"></a><span data-ttu-id="9d0a6-147">その他のリソース</span><span class="sxs-lookup"><span data-stu-id="9d0a6-147">Additional resources</span></span>
--------

[<span data-ttu-id="9d0a6-148">在庫ブロックの作成および管理</span><span class="sxs-lookup"><span data-stu-id="9d0a6-148">Create and maintain an inventory blocking</span></span>](tasks/create-maintain-inventory-blocking.md)

[<span data-ttu-id="9d0a6-149">品質管理プロセス</span><span class="sxs-lookup"><span data-stu-id="9d0a6-149">Quality management processes</span></span>](quality-management-processes.md)

[<span data-ttu-id="9d0a6-150">商品の品質の調査 (タスク ガイド)</span><span class="sxs-lookup"><span data-stu-id="9d0a6-150">Inspect the quality of goods (Task guide)</span></span>](tasks/inspect-quality-goods.md)

