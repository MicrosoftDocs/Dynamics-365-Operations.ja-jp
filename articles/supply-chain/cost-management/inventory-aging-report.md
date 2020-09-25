---
title: 在庫エイジング レポートの例とロジック
description: このトピックでは、在庫のエイジング レポートの結果を解釈する方法を示すいくつかの例を示します。
author: RichardLuan
manager: tfehr
ms.date: 5/29/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: InventAgingStorage, InventAgingStorageChart, InventAgingStorageDetails
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: riluan
ms.search.validFrom: 2020-5-29
ms.dyn365.ops.version: ''
ms.openlocfilehash: a6e708e4dc818f20fc8d835053da75c2fe9c98f6
ms.sourcegitcommit: cd339f48066b1d0fc740b513cb72ea19015acd16
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 09/02/2020
ms.locfileid: "3759547"
---
# <a name="inventory-aging-report-examples-and-logic"></a><span data-ttu-id="8593b-103">在庫エイジング レポートの例とロジック</span><span class="sxs-lookup"><span data-stu-id="8593b-103">Inventory aging report examples and logic</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="8593b-104">このトピックでは、**在庫のエイジング** レポートの結果を解釈する方法を示すいくつかの例を示します。</span><span class="sxs-lookup"><span data-stu-id="8593b-104">This topic presents some examples that show how to interpret the results of an **Inventory aging** report.</span></span> <span data-ttu-id="8593b-105">このレポートでは、選択された品目または品目グループの手持在庫の数量と在庫価値が、いくつかの期間バケットに分類されます。</span><span class="sxs-lookup"><span data-stu-id="8593b-105">This report categorizes on-hand quantity and inventory values for a selected item or item group into several period buckets.</span></span> <span data-ttu-id="8593b-106">このトピックでは、レポートの内部ロジックについても説明します。</span><span class="sxs-lookup"><span data-stu-id="8593b-106">This topic also shows the internal logic of the report.</span></span>

<span data-ttu-id="8593b-107">このトピックの例では、標準の **在庫エイジング レポート** で表示される結果を示します。</span><span class="sxs-lookup"><span data-stu-id="8593b-107">The examples in this topic show results that are presented on a standard **Inventory aging** report.</span></span> <span data-ttu-id="8593b-108">ただし、通常は、特に処理する必要がある品目と倉庫が多い場合は、このレポートの [在庫エイジング レポート ストレージ](inventory-aging-report-storage.md) バージョンを使用することをお勧めします。</span><span class="sxs-lookup"><span data-stu-id="8593b-108">However, in general, we recommend that you use the [Inventory aging report storage](inventory-aging-report-storage.md) version of this report, especially when you have many items and warehouses that must be processed.</span></span> <span data-ttu-id="8593b-109">在庫のエイジング レポートの保管では、生成された各レポートを保存し、結果をインタラクティブなページとグラフで表示して、レポートをエクスポートすることができます。</span><span class="sxs-lookup"><span data-stu-id="8593b-109">Inventory aging report storage saves each report that you generate, shows the results as an interactive page and a chart, and lets you export any saved report.</span></span>

## <a name="sample-data-that-is-used-in-these-examples"></a><span data-ttu-id="8593b-110">これらの例で使用されるサンプル データ</span><span class="sxs-lookup"><span data-stu-id="8593b-110">Sample data that is used in these examples</span></span>

<span data-ttu-id="8593b-111">このトピックの例は、このセクションで説明するサンプル在庫トランザクション データに基づいています。</span><span class="sxs-lookup"><span data-stu-id="8593b-111">The examples in this topic are based on the sample inventory transaction data that is described in this section.</span></span>

### <a name="storage-dimension-setup"></a><span data-ttu-id="8593b-112">保管分析コード セットアップ</span><span class="sxs-lookup"><span data-stu-id="8593b-112">Storage dimension setup</span></span>

<span data-ttu-id="8593b-113">この例のシステムには、次の保管分析コードの設定が含まれています。</span><span class="sxs-lookup"><span data-stu-id="8593b-113">The example system contains the following setup of storage dimensions.</span></span>

| <span data-ttu-id="8593b-114">氏名</span><span class="sxs-lookup"><span data-stu-id="8593b-114">Name</span></span>      | <span data-ttu-id="8593b-115">使用可能</span><span class="sxs-lookup"><span data-stu-id="8593b-115">Active</span></span> | <span data-ttu-id="8593b-116">現物在庫</span><span class="sxs-lookup"><span data-stu-id="8593b-116">Physical inventory</span></span> | <span data-ttu-id="8593b-117">資産在庫</span><span class="sxs-lookup"><span data-stu-id="8593b-117">Financial inventory</span></span> |
|-----------|--------|--------------------|---------------------|
| <span data-ttu-id="8593b-118">サイト</span><span class="sxs-lookup"><span data-stu-id="8593b-118">Site</span></span>      | <span data-ttu-id="8593b-119">有</span><span class="sxs-lookup"><span data-stu-id="8593b-119">Yes</span></span>    | <span data-ttu-id="8593b-120">有</span><span class="sxs-lookup"><span data-stu-id="8593b-120">Yes</span></span>                | <span data-ttu-id="8593b-121">有</span><span class="sxs-lookup"><span data-stu-id="8593b-121">Yes</span></span>                 |
| <span data-ttu-id="8593b-122">倉庫</span><span class="sxs-lookup"><span data-stu-id="8593b-122">Warehouse</span></span> | <span data-ttu-id="8593b-123">有</span><span class="sxs-lookup"><span data-stu-id="8593b-123">Yes</span></span>    | <span data-ttu-id="8593b-124">有</span><span class="sxs-lookup"><span data-stu-id="8593b-124">Yes</span></span>                | <span data-ttu-id="8593b-125">無</span><span class="sxs-lookup"><span data-stu-id="8593b-125">No</span></span>                  |

### <a name="inventory-model"></a><span data-ttu-id="8593b-126">在庫モデル</span><span class="sxs-lookup"><span data-stu-id="8593b-126">Inventory model</span></span>

<span data-ttu-id="8593b-127">この例のシステムでは、リリースされた製品の在庫モデルは *FIFO* で、在庫モデルの **原価価格** 設定には *現物価格* が含まれます。</span><span class="sxs-lookup"><span data-stu-id="8593b-127">For the example system, the inventory model for the released products is *FIFO*, and the **Cost price** setting for the inventory model is *Include physical value*.</span></span>

### <a name="inventory-transactions"></a><span data-ttu-id="8593b-128">在庫トランザクション</span><span class="sxs-lookup"><span data-stu-id="8593b-128">Inventory transactions</span></span>

<span data-ttu-id="8593b-129">この例のシステムには、品目番号 *1000* を持つリリース済製品についての、次の在庫トランザクションが含まれています。</span><span class="sxs-lookup"><span data-stu-id="8593b-129">The example system contains the following inventory transactions for a released product that has the item number *1000*.</span></span>

| <span data-ttu-id="8593b-130">参照</span><span class="sxs-lookup"><span data-stu-id="8593b-130">Reference</span></span>      | <span data-ttu-id="8593b-131">サイト</span><span class="sxs-lookup"><span data-stu-id="8593b-131">Site</span></span> | <span data-ttu-id="8593b-132">倉庫</span><span class="sxs-lookup"><span data-stu-id="8593b-132">Warehouse</span></span> | <span data-ttu-id="8593b-133">受信</span><span class="sxs-lookup"><span data-stu-id="8593b-133">Receipt</span></span>   | <span data-ttu-id="8593b-134">問題</span><span class="sxs-lookup"><span data-stu-id="8593b-134">Issue</span></span> | <span data-ttu-id="8593b-135">現物日付</span><span class="sxs-lookup"><span data-stu-id="8593b-135">Physical date</span></span> | <span data-ttu-id="8593b-136">財務日付</span><span class="sxs-lookup"><span data-stu-id="8593b-136">Financial date</span></span> | <span data-ttu-id="8593b-137">件数</span><span class="sxs-lookup"><span data-stu-id="8593b-137">Quantity</span></span> | <span data-ttu-id="8593b-138">原価金額</span><span class="sxs-lookup"><span data-stu-id="8593b-138">Cost amount</span></span> | <span data-ttu-id="8593b-139">現物原価金額</span><span class="sxs-lookup"><span data-stu-id="8593b-139">Physical cost amount</span></span> |
|----------------|------|-----------|-----------|-------|---------------|----------------|----------|-------------|----------------------|
| <span data-ttu-id="8593b-140">発注書</span><span class="sxs-lookup"><span data-stu-id="8593b-140">Purchase order</span></span> | <span data-ttu-id="8593b-141">1</span><span class="sxs-lookup"><span data-stu-id="8593b-141">1</span></span>    | <span data-ttu-id="8593b-142">11</span><span class="sxs-lookup"><span data-stu-id="8593b-142">11</span></span>        | <span data-ttu-id="8593b-143">購買済</span><span class="sxs-lookup"><span data-stu-id="8593b-143">Purchased</span></span> |       | <span data-ttu-id="8593b-144">3 月 15 日</span><span class="sxs-lookup"><span data-stu-id="8593b-144">March 15</span></span>      | <span data-ttu-id="8593b-145">3 月 15 日</span><span class="sxs-lookup"><span data-stu-id="8593b-145">March 15</span></span>       | <span data-ttu-id="8593b-146">10</span><span class="sxs-lookup"><span data-stu-id="8593b-146">10</span></span>       | <span data-ttu-id="8593b-147">1.000</span><span class="sxs-lookup"><span data-stu-id="8593b-147">1,000</span></span>       | <span data-ttu-id="8593b-148">1.000</span><span class="sxs-lookup"><span data-stu-id="8593b-148">1,000</span></span>                |
| <span data-ttu-id="8593b-149">発注書</span><span class="sxs-lookup"><span data-stu-id="8593b-149">Purchase order</span></span> | <span data-ttu-id="8593b-150">2</span><span class="sxs-lookup"><span data-stu-id="8593b-150">2</span></span>    | <span data-ttu-id="8593b-151">21</span><span class="sxs-lookup"><span data-stu-id="8593b-151">21</span></span>        | <span data-ttu-id="8593b-152">購買済</span><span class="sxs-lookup"><span data-stu-id="8593b-152">Purchased</span></span> |       | <span data-ttu-id="8593b-153">3 月 15 日</span><span class="sxs-lookup"><span data-stu-id="8593b-153">March 15</span></span>      | <span data-ttu-id="8593b-154">3 月 15 日</span><span class="sxs-lookup"><span data-stu-id="8593b-154">March 15</span></span>       | <span data-ttu-id="8593b-155">10</span><span class="sxs-lookup"><span data-stu-id="8593b-155">10</span></span>       | <span data-ttu-id="8593b-156">2,000</span><span class="sxs-lookup"><span data-stu-id="8593b-156">2,000</span></span>       | <span data-ttu-id="8593b-157">2,000</span><span class="sxs-lookup"><span data-stu-id="8593b-157">2,000</span></span>                |
| <span data-ttu-id="8593b-158">発注書</span><span class="sxs-lookup"><span data-stu-id="8593b-158">Purchase order</span></span> | <span data-ttu-id="8593b-159">1</span><span class="sxs-lookup"><span data-stu-id="8593b-159">1</span></span>    | <span data-ttu-id="8593b-160">11</span><span class="sxs-lookup"><span data-stu-id="8593b-160">11</span></span>        | <span data-ttu-id="8593b-161">受入済</span><span class="sxs-lookup"><span data-stu-id="8593b-161">Received</span></span>  |       | <span data-ttu-id="8593b-162">4 月 15 日</span><span class="sxs-lookup"><span data-stu-id="8593b-162">April 15</span></span>      |                | <span data-ttu-id="8593b-163">5</span><span class="sxs-lookup"><span data-stu-id="8593b-163">5</span></span>        |             | <span data-ttu-id="8593b-164">375</span><span class="sxs-lookup"><span data-stu-id="8593b-164">375</span></span>                  |
| <span data-ttu-id="8593b-165">移動オーダー</span><span class="sxs-lookup"><span data-stu-id="8593b-165">Transfer order</span></span> | <span data-ttu-id="8593b-166">1</span><span class="sxs-lookup"><span data-stu-id="8593b-166">1</span></span>    | <span data-ttu-id="8593b-167">11</span><span class="sxs-lookup"><span data-stu-id="8593b-167">11</span></span>        |           | <span data-ttu-id="8593b-168">売却</span><span class="sxs-lookup"><span data-stu-id="8593b-168">Sold</span></span>  | <span data-ttu-id="8593b-169">5 月 2 日</span><span class="sxs-lookup"><span data-stu-id="8593b-169">May 2</span></span>         | <span data-ttu-id="8593b-170">5 月 2 日</span><span class="sxs-lookup"><span data-stu-id="8593b-170">May 2</span></span>          | <span data-ttu-id="8593b-171">-5</span><span class="sxs-lookup"><span data-stu-id="8593b-171">-5</span></span>       | <span data-ttu-id="8593b-172">-458.33</span><span class="sxs-lookup"><span data-stu-id="8593b-172">-458.33</span></span>     | <span data-ttu-id="8593b-173">-458.33</span><span class="sxs-lookup"><span data-stu-id="8593b-173">-458.33</span></span>              |
| <span data-ttu-id="8593b-174">移動オーダー</span><span class="sxs-lookup"><span data-stu-id="8593b-174">Transfer order</span></span> | <span data-ttu-id="8593b-175">1</span><span class="sxs-lookup"><span data-stu-id="8593b-175">1</span></span>    | <span data-ttu-id="8593b-176">12</span><span class="sxs-lookup"><span data-stu-id="8593b-176">12</span></span>        | <span data-ttu-id="8593b-177">購買済</span><span class="sxs-lookup"><span data-stu-id="8593b-177">Purchased</span></span> |       | <span data-ttu-id="8593b-178">5 月 2 日</span><span class="sxs-lookup"><span data-stu-id="8593b-178">May 2</span></span>         | <span data-ttu-id="8593b-179">5 月 2 日</span><span class="sxs-lookup"><span data-stu-id="8593b-179">May 2</span></span>          | <span data-ttu-id="8593b-180">5</span><span class="sxs-lookup"><span data-stu-id="8593b-180">5</span></span>        | <span data-ttu-id="8593b-181">458.33</span><span class="sxs-lookup"><span data-stu-id="8593b-181">458.33</span></span>      | <span data-ttu-id="8593b-182">458.33</span><span class="sxs-lookup"><span data-stu-id="8593b-182">458.33</span></span>               |
| <span data-ttu-id="8593b-183">販売注文</span><span class="sxs-lookup"><span data-stu-id="8593b-183">Sales order</span></span>    | <span data-ttu-id="8593b-184">1</span><span class="sxs-lookup"><span data-stu-id="8593b-184">1</span></span>    | <span data-ttu-id="8593b-185">12</span><span class="sxs-lookup"><span data-stu-id="8593b-185">12</span></span>        |           | <span data-ttu-id="8593b-186">売却</span><span class="sxs-lookup"><span data-stu-id="8593b-186">Sold</span></span>  | <span data-ttu-id="8593b-187">5 月 3 日</span><span class="sxs-lookup"><span data-stu-id="8593b-187">May 3</span></span>         | <span data-ttu-id="8593b-188">5 月 3 日</span><span class="sxs-lookup"><span data-stu-id="8593b-188">May 3</span></span>          | <span data-ttu-id="8593b-189">-1</span><span class="sxs-lookup"><span data-stu-id="8593b-189">-1</span></span>       | <span data-ttu-id="8593b-190">-91.67</span><span class="sxs-lookup"><span data-stu-id="8593b-190">-91.67</span></span>      | <span data-ttu-id="8593b-191">-91.67</span><span class="sxs-lookup"><span data-stu-id="8593b-191">-91.67</span></span>               |

## <a name="how-quantities-and-amounts-in-each-period-bucket-are-calculated"></a><span data-ttu-id="8593b-192">各期間バケットの数量と金額の計算方法</span><span class="sxs-lookup"><span data-stu-id="8593b-192">How quantities and amounts in each period bucket are calculated</span></span>

<span data-ttu-id="8593b-193">前のセクションで説明したサンプルデータを使用して、次のような設定の **在庫エイジング** レポートを実行できます。</span><span class="sxs-lookup"><span data-stu-id="8593b-193">By using the sample data that is described in the previous sections, you can run an **Inventory aging** report that has the following settings:</span></span>

- <span data-ttu-id="8593b-194">**現在の日付:** *2020 年 5 月 9 日*</span><span class="sxs-lookup"><span data-stu-id="8593b-194">**As of date:** *May 9, 2020*</span></span>
- <span data-ttu-id="8593b-195">**サイト:** *表示*</span><span class="sxs-lookup"><span data-stu-id="8593b-195">**Site:** *View*</span></span>
- <span data-ttu-id="8593b-196">**倉庫:** *いいえ*</span><span class="sxs-lookup"><span data-stu-id="8593b-196">**Warehouse:** *No*</span></span>
- <span data-ttu-id="8593b-197">**品目番号:** *合計*</span><span class="sxs-lookup"><span data-stu-id="8593b-197">**Item number:** *Total*</span></span>
- <span data-ttu-id="8593b-198">**エイジング期間:** 月ごとのバケットを生成する場合にこのフィールドを設定します。</span><span class="sxs-lookup"><span data-stu-id="8593b-198">**Aging period:** Set this field to generate monthly buckets.</span></span>

<span data-ttu-id="8593b-199">この場合、生成されるレポートの内容は、次の例のようになります。</span><span class="sxs-lookup"><span data-stu-id="8593b-199">In this case, the content of the report that is generated will resemble the following example.</span></span>

<table>
<thead>
<tr>
    <th rowspan="2"><span data-ttu-id="8593b-200">品目番号</span><span class="sxs-lookup"><span data-stu-id="8593b-200">Item number</span></span></th>
    <th rowspan="2"><span data-ttu-id="8593b-201">サイト</span><span class="sxs-lookup"><span data-stu-id="8593b-201">Site</span></span></th>
    <th rowspan="2"><span data-ttu-id="8593b-202">手持在庫数量</span><span class="sxs-lookup"><span data-stu-id="8593b-202">On-hand quantity</span></span></th>
    <th rowspan="2"><span data-ttu-id="8593b-203">手持の金額</span><span class="sxs-lookup"><span data-stu-id="8593b-203">On-hand value</span></span></th>
    <th rowspan="2"><span data-ttu-id="8593b-204">在庫金額数量</span><span class="sxs-lookup"><span data-stu-id="8593b-204">Inventory value quantity</span></span></th>
    <th rowspan="2"><span data-ttu-id="8593b-205">在庫金額</span><span class="sxs-lookup"><span data-stu-id="8593b-205">Inventory value</span></span></th>
    <th rowspan="2"><span data-ttu-id="8593b-206">平均単位原価</span><span class="sxs-lookup"><span data-stu-id="8593b-206">Average unit cost</span></span></th>
    <th colspan="2"><span data-ttu-id="8593b-207">2020 年 5 月 8 日 - 2020 年 5 月 1 日</span><span class="sxs-lookup"><span data-stu-id="8593b-207">5/8/2020 - 5/1/2020</span></span></th>
    <th colspan="2"><span data-ttu-id="8593b-208">2020 年 4 月 30 日 - 2020 年 4 月 1 日</span><span class="sxs-lookup"><span data-stu-id="8593b-208">4/30/2020 - 4/1/2020</span></span></th>
    <th colspan="2"><span data-ttu-id="8593b-209">2020 年 3 月 31 日 - 2020 年 3 月 1 日</span><span class="sxs-lookup"><span data-stu-id="8593b-209">3/31/2020 - 3/1/2020</span></span></th>
</tr>
<tr>
    <th><span data-ttu-id="8593b-210">P1:数量</span><span class="sxs-lookup"><span data-stu-id="8593b-210">P1:Quantity</span></span></th>
    <th><span data-ttu-id="8593b-211">P1:額</span><span class="sxs-lookup"><span data-stu-id="8593b-211">P1:Amount</span></span></th>
    <th><span data-ttu-id="8593b-212">P2:数量</span><span class="sxs-lookup"><span data-stu-id="8593b-212">P2:Quantity</span></span></th>
    <th><span data-ttu-id="8593b-213">P2:額</span><span class="sxs-lookup"><span data-stu-id="8593b-213">P2:Amount</span></span></th>
    <th><span data-ttu-id="8593b-214">P3:数量</span><span class="sxs-lookup"><span data-stu-id="8593b-214">P3:Quantity</span></span></th>
    <th><span data-ttu-id="8593b-215">P3:額</span><span class="sxs-lookup"><span data-stu-id="8593b-215">P3:Amount</span></span></th>
</tr>
</thead>
<tbody>
<tr>
    <td><span data-ttu-id="8593b-216">1000</span><span class="sxs-lookup"><span data-stu-id="8593b-216">1000</span></span></td>
    <td><span data-ttu-id="8593b-217">1</span><span class="sxs-lookup"><span data-stu-id="8593b-217">1</span></span></td>
    <td><span data-ttu-id="8593b-218">14</span><span class="sxs-lookup"><span data-stu-id="8593b-218">14</span></span></td>
    <td><span data-ttu-id="8593b-219">1,283.33</span><span class="sxs-lookup"><span data-stu-id="8593b-219">1,283.33</span></span></td>
    <td><span data-ttu-id="8593b-220">14</span><span class="sxs-lookup"><span data-stu-id="8593b-220">14</span></span></td>
    <td><span data-ttu-id="8593b-221">1,283.33</span><span class="sxs-lookup"><span data-stu-id="8593b-221">1,283.33</span></span></td>
    <td><span data-ttu-id="8593b-222">91.67</span><span class="sxs-lookup"><span data-stu-id="8593b-222">91.67</span></span></td>
    <td></td>
    <td></td>
    <td><span data-ttu-id="8593b-223">5.00</span><span class="sxs-lookup"><span data-stu-id="8593b-223">5.00</span></span></td>
    <td><span data-ttu-id="8593b-224">458.33</span><span class="sxs-lookup"><span data-stu-id="8593b-224">458.33</span></span></td>
    <td><span data-ttu-id="8593b-225">9.00</span><span class="sxs-lookup"><span data-stu-id="8593b-225">9.00</span></span></td>
    <td><span data-ttu-id="8593b-226">825.00</span><span class="sxs-lookup"><span data-stu-id="8593b-226">825.00</span></span></td>
</tr>
<tr>
    <td><span data-ttu-id="8593b-227">1000</span><span class="sxs-lookup"><span data-stu-id="8593b-227">1000</span></span></td>
    <td><span data-ttu-id="8593b-228">2</span><span class="sxs-lookup"><span data-stu-id="8593b-228">2</span></span></td>
    <td><span data-ttu-id="8593b-229">10</span><span class="sxs-lookup"><span data-stu-id="8593b-229">10</span></span></td>
    <td><span data-ttu-id="8593b-230">2,000.00</span><span class="sxs-lookup"><span data-stu-id="8593b-230">2,000.00</span></span></td>
    <td><span data-ttu-id="8593b-231">10</span><span class="sxs-lookup"><span data-stu-id="8593b-231">10</span></span></td>
    <td><span data-ttu-id="8593b-232">2,000.00</span><span class="sxs-lookup"><span data-stu-id="8593b-232">2,000.00</span></span></td>
    <td><span data-ttu-id="8593b-233">200.00</span><span class="sxs-lookup"><span data-stu-id="8593b-233">200.00</span></span></td>
    <td></td>
    <td></td>
    <td></td>
    <td></td>
    <td><span data-ttu-id="8593b-234">10.00</span><span class="sxs-lookup"><span data-stu-id="8593b-234">10.00</span></span></td>
    <td><span data-ttu-id="8593b-235">2,000.00</span><span class="sxs-lookup"><span data-stu-id="8593b-235">2,000.00</span></span></td>
</tr>
</tbody>
<tfoot>
<tr>
    <td><span data-ttu-id="8593b-236"><strong>合計 1000</strong></span><span class="sxs-lookup"><span data-stu-id="8593b-236"><strong>1000 Totals</strong></span></span></td>
    <td></td>
    <td><span data-ttu-id="8593b-237"><strong>24.00</strong></span><span class="sxs-lookup"><span data-stu-id="8593b-237"><strong>24.00</strong></span></span></td>
    <td><span data-ttu-id="8593b-238"><strong>3,283.33</strong></span><span class="sxs-lookup"><span data-stu-id="8593b-238"><strong>3,283.33</strong></span></span></td>
    <td></td>
    <td></td>
    <td></td>
    <td></td>
    <td></td>
    <td><span data-ttu-id="8593b-239"><strong>5.00</strong></span><span class="sxs-lookup"><span data-stu-id="8593b-239"><strong>5.00</strong></span></span></td>
    <td><span data-ttu-id="8593b-240"><strong>458.33</strong></span><span class="sxs-lookup"><span data-stu-id="8593b-240"><strong>458.33</strong></span></span></td>
    <td><span data-ttu-id="8593b-241"><strong>19</strong></span><span class="sxs-lookup"><span data-stu-id="8593b-241"><strong>19</strong></span></span></td>
    <td><span data-ttu-id="8593b-242"><strong>2,825.00</strong></span><span class="sxs-lookup"><span data-stu-id="8593b-242"><strong>2,825.00</strong></span></span></td>
</tr>
</tfoot>
</table>

<span data-ttu-id="8593b-243">このサンプル レポートの詳細については、次を確認してください。</span><span class="sxs-lookup"><span data-stu-id="8593b-243">Note the following details in this example report:</span></span>

- <span data-ttu-id="8593b-244">レポートに表示される **在庫金額の数量**、**在庫金額**、**平均単位原価** の各値は、財務在庫分析コード (この場合は **サイト**) の値です。</span><span class="sxs-lookup"><span data-stu-id="8593b-244">The **Inventory value quantity**, **Inventory value**, and **Average unit cost** values that are shown on the report are values for the financial inventory dimension (**Site**, in this case).</span></span>

    <span data-ttu-id="8593b-245">たとえば、サイト 1の場合、レポートには次の情報が表示されます。</span><span class="sxs-lookup"><span data-stu-id="8593b-245">For example, for site 1, the report shows the following information:</span></span>

    - <span data-ttu-id="8593b-246">**在庫金額の数量** の値は、*14* (= 10 + 5 – 5 + 5 – 1) になります。</span><span class="sxs-lookup"><span data-stu-id="8593b-246">The **Inventory value quantity** value is *14* (= 10 + 5 – 5 + 5 – 1).</span></span>
    - <span data-ttu-id="8593b-247">**在庫金額の数量** の値は、*1,283.33* (= 1,000 + 375 – 458.33 + 458.33 – 91.67) になります。</span><span class="sxs-lookup"><span data-stu-id="8593b-247">The **Inventory value** value is *1,283.33* (= 1,000 + 375 – 458.33 + 458.33 – 91.67).</span></span>
    - <span data-ttu-id="8593b-248">**平均単位原価** の値は *91.67* です。</span><span class="sxs-lookup"><span data-stu-id="8593b-248">The **Average unit cost** value is *91.67*.</span></span>
    - <span data-ttu-id="8593b-249">各期間バケットの **手持在庫** の値と **金額** の値は、**平均単位原価** の値を使用して計算されます。</span><span class="sxs-lookup"><span data-stu-id="8593b-249">The **On-hand value** value and the **Amount** value in each period bucket are calculated by using the **Average unit cost** value.</span></span>

- <span data-ttu-id="8593b-250">このレポートでは、各期間バケットの入庫済在庫数量を集計することによって、各期間バケットの手持在庫数量を決定します。</span><span class="sxs-lookup"><span data-stu-id="8593b-250">The report determines the on-hand quantity for each period bucket by summarizing the total received inventory quantity for each period bucket.</span></span> <span data-ttu-id="8593b-251">次に、品目が使用している在庫モデルに関係なく、先入れ先出し (FIFO) 原則を適用して、合計出庫数量を差し引きます。</span><span class="sxs-lookup"><span data-stu-id="8593b-251">It then applies the first in, first out (FIFO) principle to deduct the total issued quantity, regardless of the inventory model that the items use.</span></span>

<span data-ttu-id="8593b-252">同じレポートを再度実行したときに、両方の **サイト** フィールドと **倉庫** フィールドを *表示する* ように設定した場合、新しいレポートは次の例のようになります。</span><span class="sxs-lookup"><span data-stu-id="8593b-252">If you run the same report again, but this time you set both the **Site** and **Warehouse** fields to *View*, the new report will resemble the following example.</span></span>

<table>
<thead>
<tr>
    <th rowspan="2"><span data-ttu-id="8593b-253">品目番号</span><span class="sxs-lookup"><span data-stu-id="8593b-253">Item number</span></span></th>
    <th rowspan="2"><span data-ttu-id="8593b-254">サイト</span><span class="sxs-lookup"><span data-stu-id="8593b-254">Site</span></span></th>
    <th rowspan="2"><span data-ttu-id="8593b-255">倉庫</span><span class="sxs-lookup"><span data-stu-id="8593b-255">Warehouse</span></span></th>
    <th rowspan="2"><span data-ttu-id="8593b-256">手持在庫数量</span><span class="sxs-lookup"><span data-stu-id="8593b-256">On-hand quantity</span></span></th>
    <th rowspan="2"><span data-ttu-id="8593b-257">手持の金額</span><span class="sxs-lookup"><span data-stu-id="8593b-257">On-hand value</span></span></th>
    <th rowspan="2"><span data-ttu-id="8593b-258">在庫金額数量</span><span class="sxs-lookup"><span data-stu-id="8593b-258">Inventory value quantity</span></span></th>
    <th rowspan="2"><span data-ttu-id="8593b-259">在庫金額</span><span class="sxs-lookup"><span data-stu-id="8593b-259">Inventory value</span></span></th>
    <th rowspan="2"><span data-ttu-id="8593b-260">平均単位原価</span><span class="sxs-lookup"><span data-stu-id="8593b-260">Average unit cost</span></span></th>
    <th colspan="2"><span data-ttu-id="8593b-261">2020 年 5 月 8 日 - 2020 年 5 月 1 日</span><span class="sxs-lookup"><span data-stu-id="8593b-261">5/8/2020 - 5/1/2020</span></span></th>
    <th colspan="2"><span data-ttu-id="8593b-262">2020 年 4 月 30 日 - 2020 年 4 月 1 日</span><span class="sxs-lookup"><span data-stu-id="8593b-262">4/30/2020 - 4/1/2020</span></span></th>
    <th colspan="2"><span data-ttu-id="8593b-263">2020 年 3 月 31 日 - 2020 年 3 月 1 日</span><span class="sxs-lookup"><span data-stu-id="8593b-263">3/31/2020 - 3/1/2020</span></span></th>
</tr>
<tr>
    <th><span data-ttu-id="8593b-264">P1:数量</span><span class="sxs-lookup"><span data-stu-id="8593b-264">P1:Quantity</span></span></th>
    <th><span data-ttu-id="8593b-265">P1:額</span><span class="sxs-lookup"><span data-stu-id="8593b-265">P1:Amount</span></span></th>
    <th><span data-ttu-id="8593b-266">P2:数量</span><span class="sxs-lookup"><span data-stu-id="8593b-266">P2:Quantity</span></span></th>
    <th><span data-ttu-id="8593b-267">P2:額</span><span class="sxs-lookup"><span data-stu-id="8593b-267">P2:Amount</span></span></th>
    <th><span data-ttu-id="8593b-268">P3:数量</span><span class="sxs-lookup"><span data-stu-id="8593b-268">P3:Quantity</span></span></th>
    <th><span data-ttu-id="8593b-269">P3:額</span><span class="sxs-lookup"><span data-stu-id="8593b-269">P3:Amount</span></span></th>
</tr>
</thead>
<tbody>
<tr>
    <td><span data-ttu-id="8593b-270">1000</span><span class="sxs-lookup"><span data-stu-id="8593b-270">1000</span></span></td>
    <td><span data-ttu-id="8593b-271">1</span><span class="sxs-lookup"><span data-stu-id="8593b-271">1</span></span></td>
    <td><span data-ttu-id="8593b-272">11</span><span class="sxs-lookup"><span data-stu-id="8593b-272">11</span></span></td>
    <td><span data-ttu-id="8593b-273">10</span><span class="sxs-lookup"><span data-stu-id="8593b-273">10</span></span></td>
    <td><span data-ttu-id="8593b-274">916.67</span><span class="sxs-lookup"><span data-stu-id="8593b-274">916.67</span></span></td>
    <td><span data-ttu-id="8593b-275">14</span><span class="sxs-lookup"><span data-stu-id="8593b-275">14</span></span></td>
    <td><span data-ttu-id="8593b-276">1,283.33</span><span class="sxs-lookup"><span data-stu-id="8593b-276">1,283.33</span></span></td>
    <td><span data-ttu-id="8593b-277">91.67</span><span class="sxs-lookup"><span data-stu-id="8593b-277">91.67</span></span></td>
    <td></td>
    <td></td>
    <td><span data-ttu-id="8593b-278">5.00</span><span class="sxs-lookup"><span data-stu-id="8593b-278">5.00</span></span></td>
    <td><span data-ttu-id="8593b-279">458.33</span><span class="sxs-lookup"><span data-stu-id="8593b-279">458.33</span></span></td>
    <td><span data-ttu-id="8593b-280">5.00</span><span class="sxs-lookup"><span data-stu-id="8593b-280">5.00</span></span></td>
    <td><span data-ttu-id="8593b-281">458.33</span><span class="sxs-lookup"><span data-stu-id="8593b-281">458.33</span></span></td>
</tr>
<tr>
    <td><span data-ttu-id="8593b-282">1000</span><span class="sxs-lookup"><span data-stu-id="8593b-282">1000</span></span></td>
    <td><span data-ttu-id="8593b-283">1</span><span class="sxs-lookup"><span data-stu-id="8593b-283">1</span></span></td>
    <td><span data-ttu-id="8593b-284">12</span><span class="sxs-lookup"><span data-stu-id="8593b-284">12</span></span></td>
    <td><span data-ttu-id="8593b-285">4</span><span class="sxs-lookup"><span data-stu-id="8593b-285">4</span></span></td>
    <td><span data-ttu-id="8593b-286">366.67</span><span class="sxs-lookup"><span data-stu-id="8593b-286">366.67</span></span></td>
    <td><span data-ttu-id="8593b-287">14</span><span class="sxs-lookup"><span data-stu-id="8593b-287">14</span></span></td>
    <td><span data-ttu-id="8593b-288">1,283.33</span><span class="sxs-lookup"><span data-stu-id="8593b-288">1,283.33</span></span></td>
    <td><span data-ttu-id="8593b-289">91.67</span><span class="sxs-lookup"><span data-stu-id="8593b-289">91.67</span></span></td>
    <td><span data-ttu-id="8593b-290">4.00</span><span class="sxs-lookup"><span data-stu-id="8593b-290">4.00</span></span></td>
    <td><span data-ttu-id="8593b-291">366.67</span><span class="sxs-lookup"><span data-stu-id="8593b-291">366.67</span></span></td>
    <td></td>
    <td></td>
    <td></td>
    <td></td>
</tr>
<tr>
    <td><span data-ttu-id="8593b-292">1000</span><span class="sxs-lookup"><span data-stu-id="8593b-292">1000</span></span></td>
    <td><span data-ttu-id="8593b-293">2</span><span class="sxs-lookup"><span data-stu-id="8593b-293">2</span></span></td>
    <td></td>
    <td><span data-ttu-id="8593b-294">10</span><span class="sxs-lookup"><span data-stu-id="8593b-294">10</span></span></td>
    <td><span data-ttu-id="8593b-295">2,000.00</span><span class="sxs-lookup"><span data-stu-id="8593b-295">2,000.00</span></span></td>
    <td><span data-ttu-id="8593b-296">10</span><span class="sxs-lookup"><span data-stu-id="8593b-296">10</span></span></td>
    <td><span data-ttu-id="8593b-297">2,000.00</span><span class="sxs-lookup"><span data-stu-id="8593b-297">2,000.00</span></span></td>
    <td><span data-ttu-id="8593b-298">200.00</span><span class="sxs-lookup"><span data-stu-id="8593b-298">200.00</span></span></td>
    <td></td>
    <td></td>
    <td></td>
    <td></td>
    <td><span data-ttu-id="8593b-299">10.00</span><span class="sxs-lookup"><span data-stu-id="8593b-299">10.00</span></span></td>
    <td><span data-ttu-id="8593b-300">2,000.00</span><span class="sxs-lookup"><span data-stu-id="8593b-300">2,000.00</span></span></td>
</tr>
</tbody>
<tfoot>
<tr>
    <td><span data-ttu-id="8593b-301"><strong>合計 1000</strong></span><span class="sxs-lookup"><span data-stu-id="8593b-301"><strong>1000 Totals</strong></span></span></td>
    <td></td>
    <td></td>
    <td><span data-ttu-id="8593b-302"><strong>24.00</strong></span><span class="sxs-lookup"><span data-stu-id="8593b-302"><strong>24.00</strong></span></span></td>
    <td><span data-ttu-id="8593b-303"><strong>3,283.33</strong></span><span class="sxs-lookup"><span data-stu-id="8593b-303"><strong>3,283.33</strong></span></span></td>
    <td></td>
    <td></td>
    <td></td>
    <td><span data-ttu-id="8593b-304"><strong>4.00</strong></span><span class="sxs-lookup"><span data-stu-id="8593b-304"><strong>4.00</strong></span></span></td>
    <td><span data-ttu-id="8593b-305"><strong>366.67</strong></span><span class="sxs-lookup"><span data-stu-id="8593b-305"><strong>366.67</strong></span></span></td>
    <td><span data-ttu-id="8593b-306"><strong>5.00</strong></span><span class="sxs-lookup"><span data-stu-id="8593b-306"><strong>5.00</strong></span></span></td>
    <td><span data-ttu-id="8593b-307"><strong>458.33</strong></span><span class="sxs-lookup"><span data-stu-id="8593b-307"><strong>458.33</strong></span></span></td>
    <td><span data-ttu-id="8593b-308"><strong>15</strong></span><span class="sxs-lookup"><span data-stu-id="8593b-308"><strong>15</strong></span></span></td>
    <td><span data-ttu-id="8593b-309"><strong>2,458.33</strong></span><span class="sxs-lookup"><span data-stu-id="8593b-309"><strong>2,458.33</strong></span></span></td>
</tr>
</tfoot>
</table>

<span data-ttu-id="8593b-310">この場合、サイト 1 は 2 つの行に分割され、1 つは倉庫 11、もう 1 つは倉庫 12 に対応します。</span><span class="sxs-lookup"><span data-stu-id="8593b-310">This time, site 1 is split into two rows, one for warehouse 11 and one for warehouse 12.</span></span> <span data-ttu-id="8593b-311">ただし、財務在庫分析コードではないので、**在庫金額の数量**、**在庫金額**、**平均単位原価** の各値は、**倉庫** は同じになります。</span><span class="sxs-lookup"><span data-stu-id="8593b-311">However, the **Inventory value quantity**, **Inventory value**, and **Average unit cost** values are the same, because **Warehouse** isn't a financial inventory dimension.</span></span>

<span data-ttu-id="8593b-312">また、サイト 1 の数量配分が異なることを確認します。</span><span class="sxs-lookup"><span data-stu-id="8593b-312">Additionally, notice that the quantity distribution of site 1 is different.</span></span> <span data-ttu-id="8593b-313">最初に実行したレポートでは、同じサイトで発生した移動オーダーが無視され、売上請求書の数量がサイト 1 の **3/31/2020 - 3/1/2020** の期間バケットから差し引かれます。</span><span class="sxs-lookup"><span data-stu-id="8593b-313">In the first report that you ran, the system ignored the transfer order that occurred in the same site and deducted the quantity of the sales invoice from the **3/31/2020 - 3/1/2020** period bucket in site 1.</span></span> <span data-ttu-id="8593b-314">ただし、新しいレポートでは、システムによって、倉庫 12 の **5/8/2020 - 5/1/2020** 期間バケットからの売上請求書の数量が差し引かれます。</span><span class="sxs-lookup"><span data-stu-id="8593b-314">However, in the new report, the system deducts the quantity of the sales invoice from the **5/8/2020 - 5/1/2020** period bucket in warehouse 12.</span></span>

## <a name="effects-of-inventory-closing"></a><span data-ttu-id="8593b-315">在庫決算の効果</span><span class="sxs-lookup"><span data-stu-id="8593b-315">Effects of inventory closing</span></span>

<span data-ttu-id="8593b-316">5 月の在庫決算を実行した後に、前のレポートを再度実行しても、**現在の日付** フィールドが *2020 年 5 月 31 日* に設定されている場合は、次のような結果が確認できます。</span><span class="sxs-lookup"><span data-stu-id="8593b-316">If you run the inventory closing for May and then run the previous report again, but you set the **As of date** field to *May 31, 2020*, you will notice the following results:</span></span>

- <span data-ttu-id="8593b-317">**在庫の値** と **平均単位原価** 価値が更新されます。</span><span class="sxs-lookup"><span data-stu-id="8593b-317">The **Inventory value** and **Average unit cost** values are updated.</span></span>
- <span data-ttu-id="8593b-318">**手持在庫の値** の値と、各区間バケットのすべての **金額** の値が、それに応じて更新されます。</span><span class="sxs-lookup"><span data-stu-id="8593b-318">The **On-hand value** value and all the **Amount** values in every period bucket are updated accordingly.</span></span>

<span data-ttu-id="8593b-319">新しいレポートは次の例のようになります。</span><span class="sxs-lookup"><span data-stu-id="8593b-319">The new report will resemble the following example.</span></span>

<table>
<thead>
<tr>
    <th rowspan="2"><span data-ttu-id="8593b-320">品目番号</span><span class="sxs-lookup"><span data-stu-id="8593b-320">Item number</span></span></th>
    <th rowspan="2"><span data-ttu-id="8593b-321">サイト</span><span class="sxs-lookup"><span data-stu-id="8593b-321">Site</span></span></th>
    <th rowspan="2"><span data-ttu-id="8593b-322">倉庫</span><span class="sxs-lookup"><span data-stu-id="8593b-322">Warehouse</span></span></th>
    <th rowspan="2"><span data-ttu-id="8593b-323">手持在庫数量</span><span class="sxs-lookup"><span data-stu-id="8593b-323">On-hand quantity</span></span></th>
    <th rowspan="2"><span data-ttu-id="8593b-324">手持の金額</span><span class="sxs-lookup"><span data-stu-id="8593b-324">On-hand value</span></span></th>
    <th rowspan="2"><span data-ttu-id="8593b-325">在庫金額数量</span><span class="sxs-lookup"><span data-stu-id="8593b-325">Inventory value quantity</span></span></th>
    <th rowspan="2"><span data-ttu-id="8593b-326">在庫金額</span><span class="sxs-lookup"><span data-stu-id="8593b-326">Inventory value</span></span></th>
    <th rowspan="2"><span data-ttu-id="8593b-327">平均単位原価</span><span class="sxs-lookup"><span data-stu-id="8593b-327">Average unit cost</span></span></th>
    <th colspan="2"><span data-ttu-id="8593b-328">2020 年 5 月 31 日 - 2020 年 5 月 1 日</span><span class="sxs-lookup"><span data-stu-id="8593b-328">5/31/2020 - 5/1/2020</span></span></th>
    <th colspan="2"><span data-ttu-id="8593b-329">2020 年 4 月 30 日 - 2020 年 4 月 1 日</span><span class="sxs-lookup"><span data-stu-id="8593b-329">4/30/2020 - 4/1/2020</span></span></th>
    <th colspan="2"><span data-ttu-id="8593b-330">2020 年 3 月 31 日 - 2020 年 3 月 1 日</span><span class="sxs-lookup"><span data-stu-id="8593b-330">3/31/2020 - 3/1/2020</span></span></th>
</tr>
<tr>
    <th><span data-ttu-id="8593b-331">P1:数量</span><span class="sxs-lookup"><span data-stu-id="8593b-331">P1:Quantity</span></span></th>
    <th><span data-ttu-id="8593b-332">P1:額</span><span class="sxs-lookup"><span data-stu-id="8593b-332">P1:Amount</span></span></th>
    <th><span data-ttu-id="8593b-333">P2:数量</span><span class="sxs-lookup"><span data-stu-id="8593b-333">P2:Quantity</span></span></th>
    <th><span data-ttu-id="8593b-334">P2:額</span><span class="sxs-lookup"><span data-stu-id="8593b-334">P2:Amount</span></span></th>
    <th><span data-ttu-id="8593b-335">P3:数量</span><span class="sxs-lookup"><span data-stu-id="8593b-335">P3:Quantity</span></span></th>
    <th><span data-ttu-id="8593b-336">P3:額</span><span class="sxs-lookup"><span data-stu-id="8593b-336">P3:Amount</span></span></th>
</tr>
</thead>
<tbody>
<tr>
    <td><span data-ttu-id="8593b-337">1000</span><span class="sxs-lookup"><span data-stu-id="8593b-337">1000</span></span></td>
    <td><span data-ttu-id="8593b-338">1</span><span class="sxs-lookup"><span data-stu-id="8593b-338">1</span></span></td>
    <td><span data-ttu-id="8593b-339">11</span><span class="sxs-lookup"><span data-stu-id="8593b-339">11</span></span></td>
    <td><span data-ttu-id="8593b-340">10</span><span class="sxs-lookup"><span data-stu-id="8593b-340">10</span></span></td>
    <td><span data-ttu-id="8593b-341">910.70</span><span class="sxs-lookup"><span data-stu-id="8593b-341">910.70</span></span></td>
    <td><span data-ttu-id="8593b-342">14</span><span class="sxs-lookup"><span data-stu-id="8593b-342">14</span></span></td>
    <td><span data-ttu-id="8593b-343">1,275.00</span><span class="sxs-lookup"><span data-stu-id="8593b-343">1,275.00</span></span></td>
    <td><span data-ttu-id="8593b-344">91.07</span><span class="sxs-lookup"><span data-stu-id="8593b-344">91.07</span></span></td>
    <td><span data-ttu-id="8593b-345">0.00</span><span class="sxs-lookup"><span data-stu-id="8593b-345">0.00</span></span></td>
    <td></td>
    <td><span data-ttu-id="8593b-346">5.00</span><span class="sxs-lookup"><span data-stu-id="8593b-346">5.00</span></span></td>
    <td><span data-ttu-id="8593b-347">455.36</span><span class="sxs-lookup"><span data-stu-id="8593b-347">455.36</span></span></td>
    <td><span data-ttu-id="8593b-348">5.00</span><span class="sxs-lookup"><span data-stu-id="8593b-348">5.00</span></span></td>
    <td><span data-ttu-id="8593b-349">455.36</span><span class="sxs-lookup"><span data-stu-id="8593b-349">455.36</span></span></td>
</tr>
<tr>
    <td><span data-ttu-id="8593b-350">1000</span><span class="sxs-lookup"><span data-stu-id="8593b-350">1000</span></span></td>
    <td><span data-ttu-id="8593b-351">1</span><span class="sxs-lookup"><span data-stu-id="8593b-351">1</span></span></td>
    <td><span data-ttu-id="8593b-352">12</span><span class="sxs-lookup"><span data-stu-id="8593b-352">12</span></span></td>
    <td><span data-ttu-id="8593b-353">4</span><span class="sxs-lookup"><span data-stu-id="8593b-353">4</span></span></td>
    <td><span data-ttu-id="8593b-354">364.29</span><span class="sxs-lookup"><span data-stu-id="8593b-354">364.29</span></span></td>
    <td><span data-ttu-id="8593b-355">14</span><span class="sxs-lookup"><span data-stu-id="8593b-355">14</span></span></td>
    <td><span data-ttu-id="8593b-356">1,275.00</span><span class="sxs-lookup"><span data-stu-id="8593b-356">1,275.00</span></span></td>
    <td><span data-ttu-id="8593b-357">91.07</span><span class="sxs-lookup"><span data-stu-id="8593b-357">91.07</span></span></td>
    <td><span data-ttu-id="8593b-358">4.00</span><span class="sxs-lookup"><span data-stu-id="8593b-358">4.00</span></span></td>
    <td><span data-ttu-id="8593b-359">364.29</span><span class="sxs-lookup"><span data-stu-id="8593b-359">364.29</span></span></td>
    <td></td>
    <td></td>
    <td></td>
    <td></td>
</tr>
<tr>
    <td><span data-ttu-id="8593b-360">1000</span><span class="sxs-lookup"><span data-stu-id="8593b-360">1000</span></span></td>
    <td><span data-ttu-id="8593b-361">2</span><span class="sxs-lookup"><span data-stu-id="8593b-361">2</span></span></td>
    <td></td>
    <td><span data-ttu-id="8593b-362">10</span><span class="sxs-lookup"><span data-stu-id="8593b-362">10</span></span></td>
    <td><span data-ttu-id="8593b-363">2,000.00</span><span class="sxs-lookup"><span data-stu-id="8593b-363">2,000.00</span></span></td>
    <td><span data-ttu-id="8593b-364">10</span><span class="sxs-lookup"><span data-stu-id="8593b-364">10</span></span></td>
    <td><span data-ttu-id="8593b-365">2,000.00</span><span class="sxs-lookup"><span data-stu-id="8593b-365">2,000.00</span></span></td>
    <td><span data-ttu-id="8593b-366">200.00</span><span class="sxs-lookup"><span data-stu-id="8593b-366">200.00</span></span></td>
    <td></td>
    <td></td>
    <td></td>
    <td></td>
    <td><span data-ttu-id="8593b-367">10.00</span><span class="sxs-lookup"><span data-stu-id="8593b-367">10.00</span></span></td>
    <td><span data-ttu-id="8593b-368">2,000.00</span><span class="sxs-lookup"><span data-stu-id="8593b-368">2,000.00</span></span></td>
</tr>
</tbody>
<tfoot>
<tr>
    <td><span data-ttu-id="8593b-369"><strong>合計 1000</strong></span><span class="sxs-lookup"><span data-stu-id="8593b-369"><strong>1000 Totals</strong></span></span></td>
    <td></td>
    <td></td>
    <td><span data-ttu-id="8593b-370"><strong>24.00</strong></span><span class="sxs-lookup"><span data-stu-id="8593b-370"><strong>24.00</strong></span></span></td>
    <td><span data-ttu-id="8593b-371"><strong>3,275.00</strong></span><span class="sxs-lookup"><span data-stu-id="8593b-371"><strong>3,275.00</strong></span></span></td>
    <td></td>
    <td></td>
    <td></td>
    <td><span data-ttu-id="8593b-372"><strong>4.00</strong></span><span class="sxs-lookup"><span data-stu-id="8593b-372"><strong>4.00</strong></span></span></td>
    <td><span data-ttu-id="8593b-373"><strong>364.29</strong></span><span class="sxs-lookup"><span data-stu-id="8593b-373"><strong>364.29</strong></span></span></td>
    <td><span data-ttu-id="8593b-374"><strong>5.00</strong></span><span class="sxs-lookup"><span data-stu-id="8593b-374"><strong>5.00</strong></span></span></td>
    <td><span data-ttu-id="8593b-375"><strong>455.36</strong></span><span class="sxs-lookup"><span data-stu-id="8593b-375"><strong>455.36</strong></span></span></td>
    <td><span data-ttu-id="8593b-376"><strong>15</strong></span><span class="sxs-lookup"><span data-stu-id="8593b-376"><strong>15</strong></span></span></td>
    <td><span data-ttu-id="8593b-377"><strong>2,455.36</strong></span><span class="sxs-lookup"><span data-stu-id="8593b-377"><strong>2,455.36</strong></span></span></td>
</tr>
</tfoot>
</table>
