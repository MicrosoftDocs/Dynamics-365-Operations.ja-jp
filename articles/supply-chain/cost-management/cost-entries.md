---
title: 原価エントリ
description: この記事は、原価エントリおよびその作成時に関する情報を提供します。 原価エントリは、特定のイベントの数量と原価を登録するレコードです。
author: AndersGirke
manager: tfehr
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: InventCostOnhandItem
audience: Application User
ms.reviewer: kamaybac
ms.custom: 19131
ms.assetid: dd2663d8-bcc0-47b1-b36d-57433143487c
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: kamaybac
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 12ff771cf44595420ca721605daabaa6b071a4ff
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 01/15/2021
ms.locfileid: "4967817"
---
# <a name="cost-entries"></a><span data-ttu-id="708f7-104">原価エントリ</span><span class="sxs-lookup"><span data-stu-id="708f7-104">Cost entries</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="708f7-105">この記事は、原価エントリおよびその作成時に関する情報を提供します。</span><span class="sxs-lookup"><span data-stu-id="708f7-105">This article provides information about cost entries and when they are created.</span></span> <span data-ttu-id="708f7-106">原価エントリは、特定のイベントの数量と原価を登録するレコードです。</span><span class="sxs-lookup"><span data-stu-id="708f7-106">A cost entry is a record that registers the quantity and cost of a given event.</span></span>

<span data-ttu-id="708f7-107">原価エントリは、有効な資産在庫分析コードに記録される在庫トランザクションの集計です。</span><span class="sxs-lookup"><span data-stu-id="708f7-107">Cost entries are aggregations of inventory transactions that are recorded on active financial inventory dimensions.</span></span>

## <a name="examples"></a><span data-ttu-id="708f7-108">例</span><span class="sxs-lookup"><span data-stu-id="708f7-108">Examples</span></span>
### <a name="example-1-no-cost-entries-are-created"></a><span data-ttu-id="708f7-109">例 1 : 原価エントリは作成されません</span><span class="sxs-lookup"><span data-stu-id="708f7-109">Example 1: No cost entries are created</span></span>

<span data-ttu-id="708f7-110">振替仕訳帳イベントが登録されます。</span><span class="sxs-lookup"><span data-stu-id="708f7-110">A transfer journal event is registered.</span></span> <span data-ttu-id="708f7-111">このイベントは、場所 A から場所 B に品目 A を 1 個転送します。場所の在庫分析コードは、原価オブジェクトの一部としては考慮されません。</span><span class="sxs-lookup"><span data-stu-id="708f7-111">The event transfers one piece of item A from location A to location B. The Location inventory dimension isn't considered part of the cost object.</span></span> <span data-ttu-id="708f7-112">したがって、イベントは 2 個の在庫トランザクションを作成しますが、原価エントリを作成しません。</span><span class="sxs-lookup"><span data-stu-id="708f7-112">Therefore, the event creates two inventory transactions and no cost entries.</span></span>

### <a name="example-2-cost-entries-are-created"></a><span data-ttu-id="708f7-113">例 2 : 原価エントリは作成されます</span><span class="sxs-lookup"><span data-stu-id="708f7-113">Example 2: Cost entries are created</span></span>

<span data-ttu-id="708f7-114">振替仕訳帳イベントが登録されます。</span><span class="sxs-lookup"><span data-stu-id="708f7-114">A transfer journal event is registered.</span></span> <span data-ttu-id="708f7-115">このイベントは、サイト 1 からサイト 2 に品目 A を 1 個転送します。</span><span class="sxs-lookup"><span data-stu-id="708f7-115">The event transfers one piece of item A from site 1 to site 2.</span></span> <span data-ttu-id="708f7-116">サイトの在庫分析コードは、原価オブジェクトの一部として考慮されます。</span><span class="sxs-lookup"><span data-stu-id="708f7-116">The Site inventory dimension is considered part of the cost object.</span></span> <span data-ttu-id="708f7-117">したがって、イベントは 2 個の在庫トランザクションを作成し、2 個の原価エントリを作成します。</span><span class="sxs-lookup"><span data-stu-id="708f7-117">Therefore, the event creates two inventory transactions and two cost entries.</span></span>

### <a name="example-3-one-cost-entry-is-created"></a><span data-ttu-id="708f7-118">例 3 : 1 個の原価エントリが作成されます</span><span class="sxs-lookup"><span data-stu-id="708f7-118">Example 3: One cost entry is created</span></span>

<span data-ttu-id="708f7-119">製品受領書イベントが発注書に登録されます。</span><span class="sxs-lookup"><span data-stu-id="708f7-119">A product receipt event is registered for a purchase order.</span></span> <span data-ttu-id="708f7-120">このイベントは、10.00 米国ドル (USD) の単位原価で品目 A を100 個登録します。</span><span class="sxs-lookup"><span data-stu-id="708f7-120">The event registers 100 pieces of item A at a unit cost of 10.00 U.S. dollars (USD).</span></span> <span data-ttu-id="708f7-121">品目 A は在庫管理の目的を追跡するためにシリアル番号を使用するため、入庫した品目ごとに固有のシリアル番号が作成されます。</span><span class="sxs-lookup"><span data-stu-id="708f7-121">Because item A uses a serial number to track the purpose of inventory management, a unique serial number is created for each item that is received.</span></span> <span data-ttu-id="708f7-122">したがって、イベントは 100 個の在庫トランザクションを作成し、原価エントリを 1 個作成します。</span><span class="sxs-lookup"><span data-stu-id="708f7-122">Therefore, the event creates 100 inventory transactions and one cost entry.</span></span>

## <a name="cost-entries-page"></a><span data-ttu-id="708f7-123">[原価エントリ] ページ</span><span class="sxs-lookup"><span data-stu-id="708f7-123">Cost entries page</span></span>
<span data-ttu-id="708f7-124">新しい **原価エントリ** ページでは、数量と原価の登録を表示および管理することができます。</span><span class="sxs-lookup"><span data-stu-id="708f7-124">The new **Cost entries** page lets you view and control registrations of quantities and costs.</span></span> <span data-ttu-id="708f7-125">このページは、**在庫トランザクション** ページと **在庫決済** ページを提供します。</span><span class="sxs-lookup"><span data-stu-id="708f7-125">This page complements the **Inventory transaction** and **Inventory settlement** pages.</span></span> <span data-ttu-id="708f7-126">レコードは、イベントに年代順に登録されます。</span><span class="sxs-lookup"><span data-stu-id="708f7-126">Records are registered in chronological order for an event.</span></span> <span data-ttu-id="708f7-127">したがって、ドキュメントに関連付けられる特定のイベントやすべてのイベントの累計コストをすばやく検索し、管理できます。</span><span class="sxs-lookup"><span data-stu-id="708f7-127">Therefore, you can quickly find and control the accumulated costs of a specific event or all events that are related to a document.</span></span> <span data-ttu-id="708f7-128">次に例を示します。</span><span class="sxs-lookup"><span data-stu-id="708f7-128">Here is an example:</span></span>

-   <span data-ttu-id="708f7-129">製品受領書イベントは、品目 A に登録されています。10.00 USD の単位原価で 100 個入庫します。</span><span class="sxs-lookup"><span data-stu-id="708f7-129">A product receipt event is registered for item A. One hundred pieces are received at a unit cost of 10.00 USD.</span></span>
-   <span data-ttu-id="708f7-130">請求書イベントが登録された数日後に、原価が 11.00 USD に増加します。</span><span class="sxs-lookup"><span data-stu-id="708f7-130">A few days after the invoice event is registered, the cost increases to 11.00 USD.</span></span> <span data-ttu-id="708f7-131">そのため、合計金額は 1,100 USD になります。</span><span class="sxs-lookup"><span data-stu-id="708f7-131">Therefore, the total amount is 1,100 USD.</span></span> <span data-ttu-id="708f7-132">2 番目の伝票が 100 USD の差額を示すために作成されます。</span><span class="sxs-lookup"><span data-stu-id="708f7-132">A second voucher is created to account for the difference of 100 USD.</span></span>
-   <span data-ttu-id="708f7-133">数日後に、輸送コストを含めるための 15.00 USD の雑費が発注書に登録されます。</span><span class="sxs-lookup"><span data-stu-id="708f7-133">A few days later, a miscellaneous charge of 15.00 USD to cover the transportation cost is registered on the purchase order.</span></span>

| <span data-ttu-id="708f7-134">伝票</span><span class="sxs-lookup"><span data-stu-id="708f7-134">Voucher</span></span> | <span data-ttu-id="708f7-135">日</span><span class="sxs-lookup"><span data-stu-id="708f7-135">Date</span></span>       | <span data-ttu-id="708f7-136">参照</span><span class="sxs-lookup"><span data-stu-id="708f7-136">Reference</span></span>      | <span data-ttu-id="708f7-137">数値</span><span class="sxs-lookup"><span data-stu-id="708f7-137">Number</span></span> | <span data-ttu-id="708f7-138">ロット ID</span><span class="sxs-lookup"><span data-stu-id="708f7-138">Lot ID</span></span>  | <span data-ttu-id="708f7-139">件数</span><span class="sxs-lookup"><span data-stu-id="708f7-139">Quantity</span></span> | <span data-ttu-id="708f7-140">金額</span><span class="sxs-lookup"><span data-stu-id="708f7-140">Amount</span></span>  |
|---------|------------|----------------|--------|---------|---------------|----|
| <span data-ttu-id="708f7-141">00001</span><span class="sxs-lookup"><span data-stu-id="708f7-141">00001</span></span>   | <span data-ttu-id="708f7-142">2015 年 1 月 1 日</span><span class="sxs-lookup"><span data-stu-id="708f7-142">01-01-2015</span></span> | <span data-ttu-id="708f7-143">発注書</span><span class="sxs-lookup"><span data-stu-id="708f7-143">Purchase order</span></span> | <span data-ttu-id="708f7-144">100001</span><span class="sxs-lookup"><span data-stu-id="708f7-144">100001</span></span> | <span data-ttu-id="708f7-145">0000101</span><span class="sxs-lookup"><span data-stu-id="708f7-145">0000101</span></span> | <span data-ttu-id="708f7-146">100.00</span><span class="sxs-lookup"><span data-stu-id="708f7-146">100.00</span></span>   | <span data-ttu-id="708f7-147">1000.00</span><span class="sxs-lookup"><span data-stu-id="708f7-147">1000.00</span></span> |
| <span data-ttu-id="708f7-148">00002</span><span class="sxs-lookup"><span data-stu-id="708f7-148">00002</span></span>   | <span data-ttu-id="708f7-149">2015 年 1 月 20 日</span><span class="sxs-lookup"><span data-stu-id="708f7-149">20-01-2015</span></span> | <span data-ttu-id="708f7-150">発注書</span><span class="sxs-lookup"><span data-stu-id="708f7-150">Purchase order</span></span> | <span data-ttu-id="708f7-151">100001</span><span class="sxs-lookup"><span data-stu-id="708f7-151">100001</span></span> | <span data-ttu-id="708f7-152">0000101</span><span class="sxs-lookup"><span data-stu-id="708f7-152">0000101</span></span> |          | <span data-ttu-id="708f7-153">100.00</span><span class="sxs-lookup"><span data-stu-id="708f7-153">100.00</span></span>  |
| <span data-ttu-id="708f7-154">00003</span><span class="sxs-lookup"><span data-stu-id="708f7-154">00003</span></span>   | <span data-ttu-id="708f7-155">2015 年 1 月 31 日</span><span class="sxs-lookup"><span data-stu-id="708f7-155">31-01-2015</span></span> | <span data-ttu-id="708f7-156">調整</span><span class="sxs-lookup"><span data-stu-id="708f7-156">Adjustment</span></span>     | <span data-ttu-id="708f7-157">100001</span><span class="sxs-lookup"><span data-stu-id="708f7-157">100001</span></span> | <span data-ttu-id="708f7-158">0000101</span><span class="sxs-lookup"><span data-stu-id="708f7-158">0000101</span></span> |          | <span data-ttu-id="708f7-159">15.00</span><span class="sxs-lookup"><span data-stu-id="708f7-159">15.00</span></span>   |

<span data-ttu-id="708f7-160">**原価エントリ** ページは、ドキュメント ID とドキュメントの日付によるフィルター処理を有効にします。</span><span class="sxs-lookup"><span data-stu-id="708f7-160">The **Cost entries** page enables filtering by document ID and document date.</span></span> 

> [!NOTE]
> <span data-ttu-id="708f7-161">原価エントリは、[原価オブジェクト](cost-object.md) またはリリースされた製品でのみ使用できます。</span><span class="sxs-lookup"><span data-stu-id="708f7-161">Cost entries are available only for [cost objects](cost-object.md) or released products.</span></span>

<a name="additional-resources"></a><span data-ttu-id="708f7-162">その他のリソース</span><span class="sxs-lookup"><span data-stu-id="708f7-162">Additional resources</span></span>
--------

[<span data-ttu-id="708f7-163">原価オブジェクト</span><span class="sxs-lookup"><span data-stu-id="708f7-163">Cost objects</span></span>](cost-object.md)



