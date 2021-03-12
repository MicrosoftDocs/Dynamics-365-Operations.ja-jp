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
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: riluan
ms.search.validFrom: 2020-5-29
ms.dyn365.ops.version: ''
ms.openlocfilehash: b3822cf4c26d7ef9cd0d062d57fa909140d7e258
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 01/15/2021
ms.locfileid: "4983928"
---
# <a name="inventory-aging-report-examples-and-logic"></a><span data-ttu-id="bcce5-103">在庫エイジング レポートの例とロジック</span><span class="sxs-lookup"><span data-stu-id="bcce5-103">Inventory aging report examples and logic</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="bcce5-104">このトピックでは、**在庫のエイジング** レポートの結果を解釈する方法を示すいくつかの例を示します。</span><span class="sxs-lookup"><span data-stu-id="bcce5-104">This topic presents some examples that show how to interpret the results of an **Inventory aging** report.</span></span> <span data-ttu-id="bcce5-105">このレポートでは、選択された品目または品目グループの手持在庫の数量と在庫価値が、いくつかの期間バケットに分類されます。</span><span class="sxs-lookup"><span data-stu-id="bcce5-105">This report categorizes on-hand quantity and inventory values for a selected item or item group into several period buckets.</span></span> <span data-ttu-id="bcce5-106">このトピックでは、レポートの内部ロジックについても説明します。</span><span class="sxs-lookup"><span data-stu-id="bcce5-106">This topic also shows the internal logic of the report.</span></span>

<span data-ttu-id="bcce5-107">このトピックの例では、標準の **在庫エイジング レポート** で表示される結果を示します。</span><span class="sxs-lookup"><span data-stu-id="bcce5-107">The examples in this topic show results that are presented on a standard **Inventory aging** report.</span></span> <span data-ttu-id="bcce5-108">ただし、通常は、特に処理する必要がある品目と倉庫が多い場合は、このレポートの [在庫エイジング レポート ストレージ](inventory-aging-report-storage.md) バージョンを使用することをお勧めします。</span><span class="sxs-lookup"><span data-stu-id="bcce5-108">However, in general, we recommend that you use the [Inventory aging report storage](inventory-aging-report-storage.md) version of this report, especially when you have many items and warehouses that must be processed.</span></span> <span data-ttu-id="bcce5-109">在庫のエイジング レポートの保管では、生成された各レポートを保存し、結果をインタラクティブなページとグラフで表示して、レポートをエクスポートすることができます。</span><span class="sxs-lookup"><span data-stu-id="bcce5-109">Inventory aging report storage saves each report that you generate, shows the results as an interactive page and a chart, and lets you export any saved report.</span></span>

## <a name="sample-data-that-is-used-in-these-examples"></a><span data-ttu-id="bcce5-110">これらの例で使用されるサンプル データ</span><span class="sxs-lookup"><span data-stu-id="bcce5-110">Sample data that is used in these examples</span></span>

<span data-ttu-id="bcce5-111">このトピックの例は、このセクションで説明するサンプル在庫トランザクション データに基づいています。</span><span class="sxs-lookup"><span data-stu-id="bcce5-111">The examples in this topic are based on the sample inventory transaction data that is described in this section.</span></span>

### <a name="storage-dimension-setup"></a><span data-ttu-id="bcce5-112">保管分析コード セットアップ</span><span class="sxs-lookup"><span data-stu-id="bcce5-112">Storage dimension setup</span></span>

<span data-ttu-id="bcce5-113">この例のシステムには、次の保管分析コードの設定が含まれています。</span><span class="sxs-lookup"><span data-stu-id="bcce5-113">The example system contains the following setup of storage dimensions.</span></span>

| <span data-ttu-id="bcce5-114">氏名</span><span class="sxs-lookup"><span data-stu-id="bcce5-114">Name</span></span>      | <span data-ttu-id="bcce5-115">使用可能</span><span class="sxs-lookup"><span data-stu-id="bcce5-115">Active</span></span> | <span data-ttu-id="bcce5-116">現物在庫</span><span class="sxs-lookup"><span data-stu-id="bcce5-116">Physical inventory</span></span> | <span data-ttu-id="bcce5-117">資産在庫</span><span class="sxs-lookup"><span data-stu-id="bcce5-117">Financial inventory</span></span> |
|-----------|--------|--------------------|---------------------|
| <span data-ttu-id="bcce5-118">サイト</span><span class="sxs-lookup"><span data-stu-id="bcce5-118">Site</span></span>      | <span data-ttu-id="bcce5-119">有</span><span class="sxs-lookup"><span data-stu-id="bcce5-119">Yes</span></span>    | <span data-ttu-id="bcce5-120">有</span><span class="sxs-lookup"><span data-stu-id="bcce5-120">Yes</span></span>                | <span data-ttu-id="bcce5-121">有</span><span class="sxs-lookup"><span data-stu-id="bcce5-121">Yes</span></span>                 |
| <span data-ttu-id="bcce5-122">倉庫</span><span class="sxs-lookup"><span data-stu-id="bcce5-122">Warehouse</span></span> | <span data-ttu-id="bcce5-123">有</span><span class="sxs-lookup"><span data-stu-id="bcce5-123">Yes</span></span>    | <span data-ttu-id="bcce5-124">有</span><span class="sxs-lookup"><span data-stu-id="bcce5-124">Yes</span></span>                | <span data-ttu-id="bcce5-125">無</span><span class="sxs-lookup"><span data-stu-id="bcce5-125">No</span></span>                  |

### <a name="inventory-model"></a><span data-ttu-id="bcce5-126">在庫モデル</span><span class="sxs-lookup"><span data-stu-id="bcce5-126">Inventory model</span></span>

<span data-ttu-id="bcce5-127">この例のシステムでは、リリースされた製品の在庫モデルは *FIFO* で、在庫モデルの **原価価格** 設定には *現物価格* が含まれます。</span><span class="sxs-lookup"><span data-stu-id="bcce5-127">For the example system, the inventory model for the released products is *FIFO*, and the **Cost price** setting for the inventory model is *Include physical value*.</span></span>

### <a name="inventory-transactions"></a><span data-ttu-id="bcce5-128">在庫トランザクション</span><span class="sxs-lookup"><span data-stu-id="bcce5-128">Inventory transactions</span></span>

<span data-ttu-id="bcce5-129">この例のシステムには、品目番号 *1000* を持つリリース済製品についての、次の在庫トランザクションが含まれています。</span><span class="sxs-lookup"><span data-stu-id="bcce5-129">The example system contains the following inventory transactions for a released product that has the item number *1000*.</span></span>

| <span data-ttu-id="bcce5-130">参照</span><span class="sxs-lookup"><span data-stu-id="bcce5-130">Reference</span></span>      | <span data-ttu-id="bcce5-131">サイト</span><span class="sxs-lookup"><span data-stu-id="bcce5-131">Site</span></span> | <span data-ttu-id="bcce5-132">倉庫</span><span class="sxs-lookup"><span data-stu-id="bcce5-132">Warehouse</span></span> | <span data-ttu-id="bcce5-133">受信</span><span class="sxs-lookup"><span data-stu-id="bcce5-133">Receipt</span></span>   | <span data-ttu-id="bcce5-134">問題</span><span class="sxs-lookup"><span data-stu-id="bcce5-134">Issue</span></span> | <span data-ttu-id="bcce5-135">現物日付</span><span class="sxs-lookup"><span data-stu-id="bcce5-135">Physical date</span></span> | <span data-ttu-id="bcce5-136">財務日付</span><span class="sxs-lookup"><span data-stu-id="bcce5-136">Financial date</span></span> | <span data-ttu-id="bcce5-137">件数</span><span class="sxs-lookup"><span data-stu-id="bcce5-137">Quantity</span></span> | <span data-ttu-id="bcce5-138">原価金額</span><span class="sxs-lookup"><span data-stu-id="bcce5-138">Cost amount</span></span> | <span data-ttu-id="bcce5-139">現物原価金額</span><span class="sxs-lookup"><span data-stu-id="bcce5-139">Physical cost amount</span></span> |
|----------------|------|-----------|-----------|-------|---------------|----------------|----------|-------------|----------------------|
| <span data-ttu-id="bcce5-140">発注書</span><span class="sxs-lookup"><span data-stu-id="bcce5-140">Purchase order</span></span> | <span data-ttu-id="bcce5-141">1</span><span class="sxs-lookup"><span data-stu-id="bcce5-141">1</span></span>    | <span data-ttu-id="bcce5-142">11</span><span class="sxs-lookup"><span data-stu-id="bcce5-142">11</span></span>        | <span data-ttu-id="bcce5-143">購買済</span><span class="sxs-lookup"><span data-stu-id="bcce5-143">Purchased</span></span> |       | <span data-ttu-id="bcce5-144">3 月 15 日</span><span class="sxs-lookup"><span data-stu-id="bcce5-144">March 15</span></span>      | <span data-ttu-id="bcce5-145">3 月 15 日</span><span class="sxs-lookup"><span data-stu-id="bcce5-145">March 15</span></span>       | <span data-ttu-id="bcce5-146">10</span><span class="sxs-lookup"><span data-stu-id="bcce5-146">10</span></span>       | <span data-ttu-id="bcce5-147">1.000</span><span class="sxs-lookup"><span data-stu-id="bcce5-147">1,000</span></span>       | <span data-ttu-id="bcce5-148">1.000</span><span class="sxs-lookup"><span data-stu-id="bcce5-148">1,000</span></span>                |
| <span data-ttu-id="bcce5-149">発注書</span><span class="sxs-lookup"><span data-stu-id="bcce5-149">Purchase order</span></span> | <span data-ttu-id="bcce5-150">2</span><span class="sxs-lookup"><span data-stu-id="bcce5-150">2</span></span>    | <span data-ttu-id="bcce5-151">21</span><span class="sxs-lookup"><span data-stu-id="bcce5-151">21</span></span>        | <span data-ttu-id="bcce5-152">購買済</span><span class="sxs-lookup"><span data-stu-id="bcce5-152">Purchased</span></span> |       | <span data-ttu-id="bcce5-153">3 月 15 日</span><span class="sxs-lookup"><span data-stu-id="bcce5-153">March 15</span></span>      | <span data-ttu-id="bcce5-154">3 月 15 日</span><span class="sxs-lookup"><span data-stu-id="bcce5-154">March 15</span></span>       | <span data-ttu-id="bcce5-155">10</span><span class="sxs-lookup"><span data-stu-id="bcce5-155">10</span></span>       | <span data-ttu-id="bcce5-156">2,000</span><span class="sxs-lookup"><span data-stu-id="bcce5-156">2,000</span></span>       | <span data-ttu-id="bcce5-157">2,000</span><span class="sxs-lookup"><span data-stu-id="bcce5-157">2,000</span></span>                |
| <span data-ttu-id="bcce5-158">発注書</span><span class="sxs-lookup"><span data-stu-id="bcce5-158">Purchase order</span></span> | <span data-ttu-id="bcce5-159">1</span><span class="sxs-lookup"><span data-stu-id="bcce5-159">1</span></span>    | <span data-ttu-id="bcce5-160">11</span><span class="sxs-lookup"><span data-stu-id="bcce5-160">11</span></span>        | <span data-ttu-id="bcce5-161">受入済</span><span class="sxs-lookup"><span data-stu-id="bcce5-161">Received</span></span>  |       | <span data-ttu-id="bcce5-162">4 月 15 日</span><span class="sxs-lookup"><span data-stu-id="bcce5-162">April 15</span></span>      |                | <span data-ttu-id="bcce5-163">5</span><span class="sxs-lookup"><span data-stu-id="bcce5-163">5</span></span>        |             | <span data-ttu-id="bcce5-164">375</span><span class="sxs-lookup"><span data-stu-id="bcce5-164">375</span></span>                  |
| <span data-ttu-id="bcce5-165">移動オーダー</span><span class="sxs-lookup"><span data-stu-id="bcce5-165">Transfer order</span></span> | <span data-ttu-id="bcce5-166">1</span><span class="sxs-lookup"><span data-stu-id="bcce5-166">1</span></span>    | <span data-ttu-id="bcce5-167">11</span><span class="sxs-lookup"><span data-stu-id="bcce5-167">11</span></span>        |           | <span data-ttu-id="bcce5-168">売却</span><span class="sxs-lookup"><span data-stu-id="bcce5-168">Sold</span></span>  | <span data-ttu-id="bcce5-169">5 月 2 日</span><span class="sxs-lookup"><span data-stu-id="bcce5-169">May 2</span></span>         | <span data-ttu-id="bcce5-170">5 月 2 日</span><span class="sxs-lookup"><span data-stu-id="bcce5-170">May 2</span></span>          | <span data-ttu-id="bcce5-171">-5</span><span class="sxs-lookup"><span data-stu-id="bcce5-171">-5</span></span>       | <span data-ttu-id="bcce5-172">-458.33</span><span class="sxs-lookup"><span data-stu-id="bcce5-172">-458.33</span></span>     | <span data-ttu-id="bcce5-173">-458.33</span><span class="sxs-lookup"><span data-stu-id="bcce5-173">-458.33</span></span>              |
| <span data-ttu-id="bcce5-174">移動オーダー</span><span class="sxs-lookup"><span data-stu-id="bcce5-174">Transfer order</span></span> | <span data-ttu-id="bcce5-175">1</span><span class="sxs-lookup"><span data-stu-id="bcce5-175">1</span></span>    | <span data-ttu-id="bcce5-176">12</span><span class="sxs-lookup"><span data-stu-id="bcce5-176">12</span></span>        | <span data-ttu-id="bcce5-177">購買済</span><span class="sxs-lookup"><span data-stu-id="bcce5-177">Purchased</span></span> |       | <span data-ttu-id="bcce5-178">5 月 2 日</span><span class="sxs-lookup"><span data-stu-id="bcce5-178">May 2</span></span>         | <span data-ttu-id="bcce5-179">5 月 2 日</span><span class="sxs-lookup"><span data-stu-id="bcce5-179">May 2</span></span>          | <span data-ttu-id="bcce5-180">5</span><span class="sxs-lookup"><span data-stu-id="bcce5-180">5</span></span>        | <span data-ttu-id="bcce5-181">458.33</span><span class="sxs-lookup"><span data-stu-id="bcce5-181">458.33</span></span>      | <span data-ttu-id="bcce5-182">458.33</span><span class="sxs-lookup"><span data-stu-id="bcce5-182">458.33</span></span>               |
| <span data-ttu-id="bcce5-183">販売注文</span><span class="sxs-lookup"><span data-stu-id="bcce5-183">Sales order</span></span>    | <span data-ttu-id="bcce5-184">1</span><span class="sxs-lookup"><span data-stu-id="bcce5-184">1</span></span>    | <span data-ttu-id="bcce5-185">12</span><span class="sxs-lookup"><span data-stu-id="bcce5-185">12</span></span>        |           | <span data-ttu-id="bcce5-186">売却</span><span class="sxs-lookup"><span data-stu-id="bcce5-186">Sold</span></span>  | <span data-ttu-id="bcce5-187">5 月 3 日</span><span class="sxs-lookup"><span data-stu-id="bcce5-187">May 3</span></span>         | <span data-ttu-id="bcce5-188">5 月 3 日</span><span class="sxs-lookup"><span data-stu-id="bcce5-188">May 3</span></span>          | <span data-ttu-id="bcce5-189">-1</span><span class="sxs-lookup"><span data-stu-id="bcce5-189">-1</span></span>       | <span data-ttu-id="bcce5-190">-91.67</span><span class="sxs-lookup"><span data-stu-id="bcce5-190">-91.67</span></span>      | <span data-ttu-id="bcce5-191">-91.67</span><span class="sxs-lookup"><span data-stu-id="bcce5-191">-91.67</span></span>               |

## <a name="how-quantities-and-amounts-in-each-period-bucket-are-calculated"></a><span data-ttu-id="bcce5-192">各期間バケットの数量と金額の計算方法</span><span class="sxs-lookup"><span data-stu-id="bcce5-192">How quantities and amounts in each period bucket are calculated</span></span>

<span data-ttu-id="bcce5-193">前のセクションで説明したサンプルデータを使用して、次のような設定の **在庫エイジング** レポートを実行できます。</span><span class="sxs-lookup"><span data-stu-id="bcce5-193">By using the sample data that is described in the previous sections, you can run an **Inventory aging** report that has the following settings:</span></span>

- <span data-ttu-id="bcce5-194">**現在の日付:** *2020 年 5 月 9 日*</span><span class="sxs-lookup"><span data-stu-id="bcce5-194">**As of date:** *May 9, 2020*</span></span>
- <span data-ttu-id="bcce5-195">**サイト:** *表示*</span><span class="sxs-lookup"><span data-stu-id="bcce5-195">**Site:** *View*</span></span>
- <span data-ttu-id="bcce5-196">**倉庫:** *いいえ*</span><span class="sxs-lookup"><span data-stu-id="bcce5-196">**Warehouse:** *No*</span></span>
- <span data-ttu-id="bcce5-197">**品目番号:** *合計*</span><span class="sxs-lookup"><span data-stu-id="bcce5-197">**Item number:** *Total*</span></span>
- <span data-ttu-id="bcce5-198">**エイジング期間:** 月ごとのバケットを生成する場合にこのフィールドを設定します。</span><span class="sxs-lookup"><span data-stu-id="bcce5-198">**Aging period:** Set this field to generate monthly buckets.</span></span>

<span data-ttu-id="bcce5-199">この場合、生成されるレポートの内容は、次の例のようになります。</span><span class="sxs-lookup"><span data-stu-id="bcce5-199">In this case, the content of the report that is generated will resemble the following example.</span></span>

<table>
<thead>
<tr>
    <th rowspan="2"><span data-ttu-id="bcce5-200">品目番号</span><span class="sxs-lookup"><span data-stu-id="bcce5-200">Item number</span></span></th>
    <th rowspan="2"><span data-ttu-id="bcce5-201">サイト</span><span class="sxs-lookup"><span data-stu-id="bcce5-201">Site</span></span></th>
    <th rowspan="2"><span data-ttu-id="bcce5-202">手持在庫数量</span><span class="sxs-lookup"><span data-stu-id="bcce5-202">On-hand quantity</span></span></th>
    <th rowspan="2"><span data-ttu-id="bcce5-203">手持の金額</span><span class="sxs-lookup"><span data-stu-id="bcce5-203">On-hand value</span></span></th>
    <th rowspan="2"><span data-ttu-id="bcce5-204">在庫金額数量</span><span class="sxs-lookup"><span data-stu-id="bcce5-204">Inventory value quantity</span></span></th>
    <th rowspan="2"><span data-ttu-id="bcce5-205">在庫金額</span><span class="sxs-lookup"><span data-stu-id="bcce5-205">Inventory value</span></span></th>
    <th rowspan="2"><span data-ttu-id="bcce5-206">平均単位原価</span><span class="sxs-lookup"><span data-stu-id="bcce5-206">Average unit cost</span></span></th>
    <th colspan="2"><span data-ttu-id="bcce5-207">2020 年 5 月 8 日 - 2020 年 5 月 1 日</span><span class="sxs-lookup"><span data-stu-id="bcce5-207">5/8/2020 - 5/1/2020</span></span></th>
    <th colspan="2"><span data-ttu-id="bcce5-208">2020 年 4 月 30 日 - 2020 年 4 月 1 日</span><span class="sxs-lookup"><span data-stu-id="bcce5-208">4/30/2020 - 4/1/2020</span></span></th>
    <th colspan="2"><span data-ttu-id="bcce5-209">2020 年 3 月 31 日 - 2020 年 3 月 1 日</span><span class="sxs-lookup"><span data-stu-id="bcce5-209">3/31/2020 - 3/1/2020</span></span></th>
</tr>
<tr>
    <th><span data-ttu-id="bcce5-210">P1:数量</span><span class="sxs-lookup"><span data-stu-id="bcce5-210">P1:Quantity</span></span></th>
    <th><span data-ttu-id="bcce5-211">P1:額</span><span class="sxs-lookup"><span data-stu-id="bcce5-211">P1:Amount</span></span></th>
    <th><span data-ttu-id="bcce5-212">P2:数量</span><span class="sxs-lookup"><span data-stu-id="bcce5-212">P2:Quantity</span></span></th>
    <th><span data-ttu-id="bcce5-213">P2:額</span><span class="sxs-lookup"><span data-stu-id="bcce5-213">P2:Amount</span></span></th>
    <th><span data-ttu-id="bcce5-214">P3:数量</span><span class="sxs-lookup"><span data-stu-id="bcce5-214">P3:Quantity</span></span></th>
    <th><span data-ttu-id="bcce5-215">P3:額</span><span class="sxs-lookup"><span data-stu-id="bcce5-215">P3:Amount</span></span></th>
</tr>
</thead>
<tbody>
<tr>
    <td><span data-ttu-id="bcce5-216">1000</span><span class="sxs-lookup"><span data-stu-id="bcce5-216">1000</span></span></td>
    <td><span data-ttu-id="bcce5-217">1</span><span class="sxs-lookup"><span data-stu-id="bcce5-217">1</span></span></td>
    <td><span data-ttu-id="bcce5-218">14</span><span class="sxs-lookup"><span data-stu-id="bcce5-218">14</span></span></td>
    <td><span data-ttu-id="bcce5-219">1,283.33</span><span class="sxs-lookup"><span data-stu-id="bcce5-219">1,283.33</span></span></td>
    <td><span data-ttu-id="bcce5-220">14</span><span class="sxs-lookup"><span data-stu-id="bcce5-220">14</span></span></td>
    <td><span data-ttu-id="bcce5-221">1,283.33</span><span class="sxs-lookup"><span data-stu-id="bcce5-221">1,283.33</span></span></td>
    <td><span data-ttu-id="bcce5-222">91.67</span><span class="sxs-lookup"><span data-stu-id="bcce5-222">91.67</span></span></td>
    <td></td>
    <td></td>
    <td><span data-ttu-id="bcce5-223">5.00</span><span class="sxs-lookup"><span data-stu-id="bcce5-223">5.00</span></span></td>
    <td><span data-ttu-id="bcce5-224">458.33</span><span class="sxs-lookup"><span data-stu-id="bcce5-224">458.33</span></span></td>
    <td><span data-ttu-id="bcce5-225">9.00</span><span class="sxs-lookup"><span data-stu-id="bcce5-225">9.00</span></span></td>
    <td><span data-ttu-id="bcce5-226">825.00</span><span class="sxs-lookup"><span data-stu-id="bcce5-226">825.00</span></span></td>
</tr>
<tr>
    <td><span data-ttu-id="bcce5-227">1000</span><span class="sxs-lookup"><span data-stu-id="bcce5-227">1000</span></span></td>
    <td><span data-ttu-id="bcce5-228">2</span><span class="sxs-lookup"><span data-stu-id="bcce5-228">2</span></span></td>
    <td><span data-ttu-id="bcce5-229">10</span><span class="sxs-lookup"><span data-stu-id="bcce5-229">10</span></span></td>
    <td><span data-ttu-id="bcce5-230">2,000.00</span><span class="sxs-lookup"><span data-stu-id="bcce5-230">2,000.00</span></span></td>
    <td><span data-ttu-id="bcce5-231">10</span><span class="sxs-lookup"><span data-stu-id="bcce5-231">10</span></span></td>
    <td><span data-ttu-id="bcce5-232">2,000.00</span><span class="sxs-lookup"><span data-stu-id="bcce5-232">2,000.00</span></span></td>
    <td><span data-ttu-id="bcce5-233">200.00</span><span class="sxs-lookup"><span data-stu-id="bcce5-233">200.00</span></span></td>
    <td></td>
    <td></td>
    <td></td>
    <td></td>
    <td><span data-ttu-id="bcce5-234">10.00</span><span class="sxs-lookup"><span data-stu-id="bcce5-234">10.00</span></span></td>
    <td><span data-ttu-id="bcce5-235">2,000.00</span><span class="sxs-lookup"><span data-stu-id="bcce5-235">2,000.00</span></span></td>
</tr>
</tbody>
<tfoot>
<tr>
    <td><span data-ttu-id="bcce5-236"><strong>合計 1000</strong></span><span class="sxs-lookup"><span data-stu-id="bcce5-236"><strong>1000 Totals</strong></span></span></td>
    <td></td>
    <td><span data-ttu-id="bcce5-237"><strong>24.00</strong></span><span class="sxs-lookup"><span data-stu-id="bcce5-237"><strong>24.00</strong></span></span></td>
    <td><span data-ttu-id="bcce5-238"><strong>3,283.33</strong></span><span class="sxs-lookup"><span data-stu-id="bcce5-238"><strong>3,283.33</strong></span></span></td>
    <td></td>
    <td></td>
    <td></td>
    <td></td>
    <td></td>
    <td><span data-ttu-id="bcce5-239"><strong>5.00</strong></span><span class="sxs-lookup"><span data-stu-id="bcce5-239"><strong>5.00</strong></span></span></td>
    <td><span data-ttu-id="bcce5-240"><strong>458.33</strong></span><span class="sxs-lookup"><span data-stu-id="bcce5-240"><strong>458.33</strong></span></span></td>
    <td><span data-ttu-id="bcce5-241"><strong>19</strong></span><span class="sxs-lookup"><span data-stu-id="bcce5-241"><strong>19</strong></span></span></td>
    <td><span data-ttu-id="bcce5-242"><strong>2,825.00</strong></span><span class="sxs-lookup"><span data-stu-id="bcce5-242"><strong>2,825.00</strong></span></span></td>
</tr>
</tfoot>
</table>

<span data-ttu-id="bcce5-243">このサンプル レポートの詳細については、次を確認してください。</span><span class="sxs-lookup"><span data-stu-id="bcce5-243">Note the following details in this example report:</span></span>

- <span data-ttu-id="bcce5-244">レポートに表示される **在庫金額の数量**、**在庫金額**、**平均単位原価** の各値は、財務在庫分析コード (この場合は **サイト**) の値です。</span><span class="sxs-lookup"><span data-stu-id="bcce5-244">The **Inventory value quantity**, **Inventory value**, and **Average unit cost** values that are shown on the report are values for the financial inventory dimension (**Site**, in this case).</span></span>

    <span data-ttu-id="bcce5-245">たとえば、サイト 1の場合、レポートには次の情報が表示されます。</span><span class="sxs-lookup"><span data-stu-id="bcce5-245">For example, for site 1, the report shows the following information:</span></span>

    - <span data-ttu-id="bcce5-246">**在庫金額の数量** の値は、*14* (= 10 + 5 – 5 + 5 – 1) になります。</span><span class="sxs-lookup"><span data-stu-id="bcce5-246">The **Inventory value quantity** value is *14* (= 10 + 5 – 5 + 5 – 1).</span></span>
    - <span data-ttu-id="bcce5-247">**在庫金額の数量** の値は、*1,283.33* (= 1,000 + 375 – 458.33 + 458.33 – 91.67) になります。</span><span class="sxs-lookup"><span data-stu-id="bcce5-247">The **Inventory value** value is *1,283.33* (= 1,000 + 375 – 458.33 + 458.33 – 91.67).</span></span>
    - <span data-ttu-id="bcce5-248">**平均単位原価** の値は *91.67* です。</span><span class="sxs-lookup"><span data-stu-id="bcce5-248">The **Average unit cost** value is *91.67*.</span></span>
    - <span data-ttu-id="bcce5-249">各期間バケットの **手持在庫** の値と **金額** の値は、**平均単位原価** の値を使用して計算されます。</span><span class="sxs-lookup"><span data-stu-id="bcce5-249">The **On-hand value** value and the **Amount** value in each period bucket are calculated by using the **Average unit cost** value.</span></span>

- <span data-ttu-id="bcce5-250">このレポートでは、各期間バケットの入庫済在庫数量を集計することによって、各期間バケットの手持在庫数量を決定します。</span><span class="sxs-lookup"><span data-stu-id="bcce5-250">The report determines the on-hand quantity for each period bucket by summarizing the total received inventory quantity for each period bucket.</span></span> <span data-ttu-id="bcce5-251">次に、品目が使用している在庫モデルに関係なく、先入れ先出し (FIFO) 原則を適用して、合計出庫数量を差し引きます。</span><span class="sxs-lookup"><span data-stu-id="bcce5-251">It then applies the first in, first out (FIFO) principle to deduct the total issued quantity, regardless of the inventory model that the items use.</span></span>

<span data-ttu-id="bcce5-252">同じレポートを再度実行したときに、両方の **サイト** フィールドと **倉庫** フィールドを *表示する* ように設定した場合、新しいレポートは次の例のようになります。</span><span class="sxs-lookup"><span data-stu-id="bcce5-252">If you run the same report again, but this time you set both the **Site** and **Warehouse** fields to *View*, the new report will resemble the following example.</span></span>

<table>
<thead>
<tr>
    <th rowspan="2"><span data-ttu-id="bcce5-253">品目番号</span><span class="sxs-lookup"><span data-stu-id="bcce5-253">Item number</span></span></th>
    <th rowspan="2"><span data-ttu-id="bcce5-254">サイト</span><span class="sxs-lookup"><span data-stu-id="bcce5-254">Site</span></span></th>
    <th rowspan="2"><span data-ttu-id="bcce5-255">倉庫</span><span class="sxs-lookup"><span data-stu-id="bcce5-255">Warehouse</span></span></th>
    <th rowspan="2"><span data-ttu-id="bcce5-256">手持在庫数量</span><span class="sxs-lookup"><span data-stu-id="bcce5-256">On-hand quantity</span></span></th>
    <th rowspan="2"><span data-ttu-id="bcce5-257">手持の金額</span><span class="sxs-lookup"><span data-stu-id="bcce5-257">On-hand value</span></span></th>
    <th rowspan="2"><span data-ttu-id="bcce5-258">在庫金額数量</span><span class="sxs-lookup"><span data-stu-id="bcce5-258">Inventory value quantity</span></span></th>
    <th rowspan="2"><span data-ttu-id="bcce5-259">在庫金額</span><span class="sxs-lookup"><span data-stu-id="bcce5-259">Inventory value</span></span></th>
    <th rowspan="2"><span data-ttu-id="bcce5-260">平均単位原価</span><span class="sxs-lookup"><span data-stu-id="bcce5-260">Average unit cost</span></span></th>
    <th colspan="2"><span data-ttu-id="bcce5-261">2020 年 5 月 8 日 - 2020 年 5 月 1 日</span><span class="sxs-lookup"><span data-stu-id="bcce5-261">5/8/2020 - 5/1/2020</span></span></th>
    <th colspan="2"><span data-ttu-id="bcce5-262">2020 年 4 月 30 日 - 2020 年 4 月 1 日</span><span class="sxs-lookup"><span data-stu-id="bcce5-262">4/30/2020 - 4/1/2020</span></span></th>
    <th colspan="2"><span data-ttu-id="bcce5-263">2020 年 3 月 31 日 - 2020 年 3 月 1 日</span><span class="sxs-lookup"><span data-stu-id="bcce5-263">3/31/2020 - 3/1/2020</span></span></th>
</tr>
<tr>
    <th><span data-ttu-id="bcce5-264">P1:数量</span><span class="sxs-lookup"><span data-stu-id="bcce5-264">P1:Quantity</span></span></th>
    <th><span data-ttu-id="bcce5-265">P1:額</span><span class="sxs-lookup"><span data-stu-id="bcce5-265">P1:Amount</span></span></th>
    <th><span data-ttu-id="bcce5-266">P2:数量</span><span class="sxs-lookup"><span data-stu-id="bcce5-266">P2:Quantity</span></span></th>
    <th><span data-ttu-id="bcce5-267">P2:額</span><span class="sxs-lookup"><span data-stu-id="bcce5-267">P2:Amount</span></span></th>
    <th><span data-ttu-id="bcce5-268">P3:数量</span><span class="sxs-lookup"><span data-stu-id="bcce5-268">P3:Quantity</span></span></th>
    <th><span data-ttu-id="bcce5-269">P3:額</span><span class="sxs-lookup"><span data-stu-id="bcce5-269">P3:Amount</span></span></th>
</tr>
</thead>
<tbody>
<tr>
    <td><span data-ttu-id="bcce5-270">1000</span><span class="sxs-lookup"><span data-stu-id="bcce5-270">1000</span></span></td>
    <td><span data-ttu-id="bcce5-271">1</span><span class="sxs-lookup"><span data-stu-id="bcce5-271">1</span></span></td>
    <td><span data-ttu-id="bcce5-272">11</span><span class="sxs-lookup"><span data-stu-id="bcce5-272">11</span></span></td>
    <td><span data-ttu-id="bcce5-273">10</span><span class="sxs-lookup"><span data-stu-id="bcce5-273">10</span></span></td>
    <td><span data-ttu-id="bcce5-274">916.67</span><span class="sxs-lookup"><span data-stu-id="bcce5-274">916.67</span></span></td>
    <td><span data-ttu-id="bcce5-275">14</span><span class="sxs-lookup"><span data-stu-id="bcce5-275">14</span></span></td>
    <td><span data-ttu-id="bcce5-276">1,283.33</span><span class="sxs-lookup"><span data-stu-id="bcce5-276">1,283.33</span></span></td>
    <td><span data-ttu-id="bcce5-277">91.67</span><span class="sxs-lookup"><span data-stu-id="bcce5-277">91.67</span></span></td>
    <td></td>
    <td></td>
    <td><span data-ttu-id="bcce5-278">5.00</span><span class="sxs-lookup"><span data-stu-id="bcce5-278">5.00</span></span></td>
    <td><span data-ttu-id="bcce5-279">458.33</span><span class="sxs-lookup"><span data-stu-id="bcce5-279">458.33</span></span></td>
    <td><span data-ttu-id="bcce5-280">5.00</span><span class="sxs-lookup"><span data-stu-id="bcce5-280">5.00</span></span></td>
    <td><span data-ttu-id="bcce5-281">458.33</span><span class="sxs-lookup"><span data-stu-id="bcce5-281">458.33</span></span></td>
</tr>
<tr>
    <td><span data-ttu-id="bcce5-282">1000</span><span class="sxs-lookup"><span data-stu-id="bcce5-282">1000</span></span></td>
    <td><span data-ttu-id="bcce5-283">1</span><span class="sxs-lookup"><span data-stu-id="bcce5-283">1</span></span></td>
    <td><span data-ttu-id="bcce5-284">12</span><span class="sxs-lookup"><span data-stu-id="bcce5-284">12</span></span></td>
    <td><span data-ttu-id="bcce5-285">4</span><span class="sxs-lookup"><span data-stu-id="bcce5-285">4</span></span></td>
    <td><span data-ttu-id="bcce5-286">366.67</span><span class="sxs-lookup"><span data-stu-id="bcce5-286">366.67</span></span></td>
    <td><span data-ttu-id="bcce5-287">14</span><span class="sxs-lookup"><span data-stu-id="bcce5-287">14</span></span></td>
    <td><span data-ttu-id="bcce5-288">1,283.33</span><span class="sxs-lookup"><span data-stu-id="bcce5-288">1,283.33</span></span></td>
    <td><span data-ttu-id="bcce5-289">91.67</span><span class="sxs-lookup"><span data-stu-id="bcce5-289">91.67</span></span></td>
    <td><span data-ttu-id="bcce5-290">4.00</span><span class="sxs-lookup"><span data-stu-id="bcce5-290">4.00</span></span></td>
    <td><span data-ttu-id="bcce5-291">366.67</span><span class="sxs-lookup"><span data-stu-id="bcce5-291">366.67</span></span></td>
    <td></td>
    <td></td>
    <td></td>
    <td></td>
</tr>
<tr>
    <td><span data-ttu-id="bcce5-292">1000</span><span class="sxs-lookup"><span data-stu-id="bcce5-292">1000</span></span></td>
    <td><span data-ttu-id="bcce5-293">2</span><span class="sxs-lookup"><span data-stu-id="bcce5-293">2</span></span></td>
    <td></td>
    <td><span data-ttu-id="bcce5-294">10</span><span class="sxs-lookup"><span data-stu-id="bcce5-294">10</span></span></td>
    <td><span data-ttu-id="bcce5-295">2,000.00</span><span class="sxs-lookup"><span data-stu-id="bcce5-295">2,000.00</span></span></td>
    <td><span data-ttu-id="bcce5-296">10</span><span class="sxs-lookup"><span data-stu-id="bcce5-296">10</span></span></td>
    <td><span data-ttu-id="bcce5-297">2,000.00</span><span class="sxs-lookup"><span data-stu-id="bcce5-297">2,000.00</span></span></td>
    <td><span data-ttu-id="bcce5-298">200.00</span><span class="sxs-lookup"><span data-stu-id="bcce5-298">200.00</span></span></td>
    <td></td>
    <td></td>
    <td></td>
    <td></td>
    <td><span data-ttu-id="bcce5-299">10.00</span><span class="sxs-lookup"><span data-stu-id="bcce5-299">10.00</span></span></td>
    <td><span data-ttu-id="bcce5-300">2,000.00</span><span class="sxs-lookup"><span data-stu-id="bcce5-300">2,000.00</span></span></td>
</tr>
</tbody>
<tfoot>
<tr>
    <td><span data-ttu-id="bcce5-301"><strong>合計 1000</strong></span><span class="sxs-lookup"><span data-stu-id="bcce5-301"><strong>1000 Totals</strong></span></span></td>
    <td></td>
    <td></td>
    <td><span data-ttu-id="bcce5-302"><strong>24.00</strong></span><span class="sxs-lookup"><span data-stu-id="bcce5-302"><strong>24.00</strong></span></span></td>
    <td><span data-ttu-id="bcce5-303"><strong>3,283.33</strong></span><span class="sxs-lookup"><span data-stu-id="bcce5-303"><strong>3,283.33</strong></span></span></td>
    <td></td>
    <td></td>
    <td></td>
    <td><span data-ttu-id="bcce5-304"><strong>4.00</strong></span><span class="sxs-lookup"><span data-stu-id="bcce5-304"><strong>4.00</strong></span></span></td>
    <td><span data-ttu-id="bcce5-305"><strong>366.67</strong></span><span class="sxs-lookup"><span data-stu-id="bcce5-305"><strong>366.67</strong></span></span></td>
    <td><span data-ttu-id="bcce5-306"><strong>5.00</strong></span><span class="sxs-lookup"><span data-stu-id="bcce5-306"><strong>5.00</strong></span></span></td>
    <td><span data-ttu-id="bcce5-307"><strong>458.33</strong></span><span class="sxs-lookup"><span data-stu-id="bcce5-307"><strong>458.33</strong></span></span></td>
    <td><span data-ttu-id="bcce5-308"><strong>15</strong></span><span class="sxs-lookup"><span data-stu-id="bcce5-308"><strong>15</strong></span></span></td>
    <td><span data-ttu-id="bcce5-309"><strong>2,458.33</strong></span><span class="sxs-lookup"><span data-stu-id="bcce5-309"><strong>2,458.33</strong></span></span></td>
</tr>
</tfoot>
</table>

<span data-ttu-id="bcce5-310">この場合、サイト 1 は 2 つの行に分割され、1 つは倉庫 11、もう 1 つは倉庫 12 に対応します。</span><span class="sxs-lookup"><span data-stu-id="bcce5-310">This time, site 1 is split into two rows, one for warehouse 11 and one for warehouse 12.</span></span> <span data-ttu-id="bcce5-311">ただし、財務在庫分析コードではないので、**在庫金額の数量**、**在庫金額**、**平均単位原価** の各値は、**倉庫** は同じになります。</span><span class="sxs-lookup"><span data-stu-id="bcce5-311">However, the **Inventory value quantity**, **Inventory value**, and **Average unit cost** values are the same, because **Warehouse** isn't a financial inventory dimension.</span></span>

<span data-ttu-id="bcce5-312">また、サイト 1 の数量配分が異なることを確認します。</span><span class="sxs-lookup"><span data-stu-id="bcce5-312">Additionally, notice that the quantity distribution of site 1 is different.</span></span> <span data-ttu-id="bcce5-313">最初に実行したレポートでは、同じサイトで発生した移動オーダーが無視され、売上請求書の数量がサイト 1 の **3/31/2020 - 3/1/2020** の期間バケットから差し引かれます。</span><span class="sxs-lookup"><span data-stu-id="bcce5-313">In the first report that you ran, the system ignored the transfer order that occurred in the same site and deducted the quantity of the sales invoice from the **3/31/2020 - 3/1/2020** period bucket in site 1.</span></span> <span data-ttu-id="bcce5-314">ただし、新しいレポートでは、システムによって、倉庫 12 の **5/8/2020 - 5/1/2020** 期間バケットからの売上請求書の数量が差し引かれます。</span><span class="sxs-lookup"><span data-stu-id="bcce5-314">However, in the new report, the system deducts the quantity of the sales invoice from the **5/8/2020 - 5/1/2020** period bucket in warehouse 12.</span></span>

## <a name="effects-of-inventory-closing"></a><span data-ttu-id="bcce5-315">在庫決算の効果</span><span class="sxs-lookup"><span data-stu-id="bcce5-315">Effects of inventory closing</span></span>

<span data-ttu-id="bcce5-316">5 月の在庫決算を実行した後に、前のレポートを再度実行しても、**現在の日付** フィールドが *2020 年 5 月 31 日* に設定されている場合は、次のような結果が確認できます。</span><span class="sxs-lookup"><span data-stu-id="bcce5-316">If you run the inventory closing for May and then run the previous report again, but you set the **As of date** field to *May 31, 2020*, you will notice the following results:</span></span>

- <span data-ttu-id="bcce5-317">**在庫の値** と **平均単位原価** 価値が更新されます。</span><span class="sxs-lookup"><span data-stu-id="bcce5-317">The **Inventory value** and **Average unit cost** values are updated.</span></span>
- <span data-ttu-id="bcce5-318">**手持在庫の値** の値と、各区間バケットのすべての **金額** の値が、それに応じて更新されます。</span><span class="sxs-lookup"><span data-stu-id="bcce5-318">The **On-hand value** value and all the **Amount** values in every period bucket are updated accordingly.</span></span>

<span data-ttu-id="bcce5-319">新しいレポートは次の例のようになります。</span><span class="sxs-lookup"><span data-stu-id="bcce5-319">The new report will resemble the following example.</span></span>

<table>
<thead>
<tr>
    <th rowspan="2"><span data-ttu-id="bcce5-320">品目番号</span><span class="sxs-lookup"><span data-stu-id="bcce5-320">Item number</span></span></th>
    <th rowspan="2"><span data-ttu-id="bcce5-321">サイト</span><span class="sxs-lookup"><span data-stu-id="bcce5-321">Site</span></span></th>
    <th rowspan="2"><span data-ttu-id="bcce5-322">倉庫</span><span class="sxs-lookup"><span data-stu-id="bcce5-322">Warehouse</span></span></th>
    <th rowspan="2"><span data-ttu-id="bcce5-323">手持在庫数量</span><span class="sxs-lookup"><span data-stu-id="bcce5-323">On-hand quantity</span></span></th>
    <th rowspan="2"><span data-ttu-id="bcce5-324">手持の金額</span><span class="sxs-lookup"><span data-stu-id="bcce5-324">On-hand value</span></span></th>
    <th rowspan="2"><span data-ttu-id="bcce5-325">在庫金額数量</span><span class="sxs-lookup"><span data-stu-id="bcce5-325">Inventory value quantity</span></span></th>
    <th rowspan="2"><span data-ttu-id="bcce5-326">在庫金額</span><span class="sxs-lookup"><span data-stu-id="bcce5-326">Inventory value</span></span></th>
    <th rowspan="2"><span data-ttu-id="bcce5-327">平均単位原価</span><span class="sxs-lookup"><span data-stu-id="bcce5-327">Average unit cost</span></span></th>
    <th colspan="2"><span data-ttu-id="bcce5-328">2020 年 5 月 31 日 - 2020 年 5 月 1 日</span><span class="sxs-lookup"><span data-stu-id="bcce5-328">5/31/2020 - 5/1/2020</span></span></th>
    <th colspan="2"><span data-ttu-id="bcce5-329">2020 年 4 月 30 日 - 2020 年 4 月 1 日</span><span class="sxs-lookup"><span data-stu-id="bcce5-329">4/30/2020 - 4/1/2020</span></span></th>
    <th colspan="2"><span data-ttu-id="bcce5-330">2020 年 3 月 31 日 - 2020 年 3 月 1 日</span><span class="sxs-lookup"><span data-stu-id="bcce5-330">3/31/2020 - 3/1/2020</span></span></th>
</tr>
<tr>
    <th><span data-ttu-id="bcce5-331">P1:数量</span><span class="sxs-lookup"><span data-stu-id="bcce5-331">P1:Quantity</span></span></th>
    <th><span data-ttu-id="bcce5-332">P1:額</span><span class="sxs-lookup"><span data-stu-id="bcce5-332">P1:Amount</span></span></th>
    <th><span data-ttu-id="bcce5-333">P2:数量</span><span class="sxs-lookup"><span data-stu-id="bcce5-333">P2:Quantity</span></span></th>
    <th><span data-ttu-id="bcce5-334">P2:額</span><span class="sxs-lookup"><span data-stu-id="bcce5-334">P2:Amount</span></span></th>
    <th><span data-ttu-id="bcce5-335">P3:数量</span><span class="sxs-lookup"><span data-stu-id="bcce5-335">P3:Quantity</span></span></th>
    <th><span data-ttu-id="bcce5-336">P3:額</span><span class="sxs-lookup"><span data-stu-id="bcce5-336">P3:Amount</span></span></th>
</tr>
</thead>
<tbody>
<tr>
    <td><span data-ttu-id="bcce5-337">1000</span><span class="sxs-lookup"><span data-stu-id="bcce5-337">1000</span></span></td>
    <td><span data-ttu-id="bcce5-338">1</span><span class="sxs-lookup"><span data-stu-id="bcce5-338">1</span></span></td>
    <td><span data-ttu-id="bcce5-339">11</span><span class="sxs-lookup"><span data-stu-id="bcce5-339">11</span></span></td>
    <td><span data-ttu-id="bcce5-340">10</span><span class="sxs-lookup"><span data-stu-id="bcce5-340">10</span></span></td>
    <td><span data-ttu-id="bcce5-341">910.70</span><span class="sxs-lookup"><span data-stu-id="bcce5-341">910.70</span></span></td>
    <td><span data-ttu-id="bcce5-342">14</span><span class="sxs-lookup"><span data-stu-id="bcce5-342">14</span></span></td>
    <td><span data-ttu-id="bcce5-343">1,275.00</span><span class="sxs-lookup"><span data-stu-id="bcce5-343">1,275.00</span></span></td>
    <td><span data-ttu-id="bcce5-344">91.07</span><span class="sxs-lookup"><span data-stu-id="bcce5-344">91.07</span></span></td>
    <td><span data-ttu-id="bcce5-345">0.00</span><span class="sxs-lookup"><span data-stu-id="bcce5-345">0.00</span></span></td>
    <td></td>
    <td><span data-ttu-id="bcce5-346">5.00</span><span class="sxs-lookup"><span data-stu-id="bcce5-346">5.00</span></span></td>
    <td><span data-ttu-id="bcce5-347">455.36</span><span class="sxs-lookup"><span data-stu-id="bcce5-347">455.36</span></span></td>
    <td><span data-ttu-id="bcce5-348">5.00</span><span class="sxs-lookup"><span data-stu-id="bcce5-348">5.00</span></span></td>
    <td><span data-ttu-id="bcce5-349">455.36</span><span class="sxs-lookup"><span data-stu-id="bcce5-349">455.36</span></span></td>
</tr>
<tr>
    <td><span data-ttu-id="bcce5-350">1000</span><span class="sxs-lookup"><span data-stu-id="bcce5-350">1000</span></span></td>
    <td><span data-ttu-id="bcce5-351">1</span><span class="sxs-lookup"><span data-stu-id="bcce5-351">1</span></span></td>
    <td><span data-ttu-id="bcce5-352">12</span><span class="sxs-lookup"><span data-stu-id="bcce5-352">12</span></span></td>
    <td><span data-ttu-id="bcce5-353">4</span><span class="sxs-lookup"><span data-stu-id="bcce5-353">4</span></span></td>
    <td><span data-ttu-id="bcce5-354">364.29</span><span class="sxs-lookup"><span data-stu-id="bcce5-354">364.29</span></span></td>
    <td><span data-ttu-id="bcce5-355">14</span><span class="sxs-lookup"><span data-stu-id="bcce5-355">14</span></span></td>
    <td><span data-ttu-id="bcce5-356">1,275.00</span><span class="sxs-lookup"><span data-stu-id="bcce5-356">1,275.00</span></span></td>
    <td><span data-ttu-id="bcce5-357">91.07</span><span class="sxs-lookup"><span data-stu-id="bcce5-357">91.07</span></span></td>
    <td><span data-ttu-id="bcce5-358">4.00</span><span class="sxs-lookup"><span data-stu-id="bcce5-358">4.00</span></span></td>
    <td><span data-ttu-id="bcce5-359">364.29</span><span class="sxs-lookup"><span data-stu-id="bcce5-359">364.29</span></span></td>
    <td></td>
    <td></td>
    <td></td>
    <td></td>
</tr>
<tr>
    <td><span data-ttu-id="bcce5-360">1000</span><span class="sxs-lookup"><span data-stu-id="bcce5-360">1000</span></span></td>
    <td><span data-ttu-id="bcce5-361">2</span><span class="sxs-lookup"><span data-stu-id="bcce5-361">2</span></span></td>
    <td></td>
    <td><span data-ttu-id="bcce5-362">10</span><span class="sxs-lookup"><span data-stu-id="bcce5-362">10</span></span></td>
    <td><span data-ttu-id="bcce5-363">2,000.00</span><span class="sxs-lookup"><span data-stu-id="bcce5-363">2,000.00</span></span></td>
    <td><span data-ttu-id="bcce5-364">10</span><span class="sxs-lookup"><span data-stu-id="bcce5-364">10</span></span></td>
    <td><span data-ttu-id="bcce5-365">2,000.00</span><span class="sxs-lookup"><span data-stu-id="bcce5-365">2,000.00</span></span></td>
    <td><span data-ttu-id="bcce5-366">200.00</span><span class="sxs-lookup"><span data-stu-id="bcce5-366">200.00</span></span></td>
    <td></td>
    <td></td>
    <td></td>
    <td></td>
    <td><span data-ttu-id="bcce5-367">10.00</span><span class="sxs-lookup"><span data-stu-id="bcce5-367">10.00</span></span></td>
    <td><span data-ttu-id="bcce5-368">2,000.00</span><span class="sxs-lookup"><span data-stu-id="bcce5-368">2,000.00</span></span></td>
</tr>
</tbody>
<tfoot>
<tr>
    <td><span data-ttu-id="bcce5-369"><strong>合計 1000</strong></span><span class="sxs-lookup"><span data-stu-id="bcce5-369"><strong>1000 Totals</strong></span></span></td>
    <td></td>
    <td></td>
    <td><span data-ttu-id="bcce5-370"><strong>24.00</strong></span><span class="sxs-lookup"><span data-stu-id="bcce5-370"><strong>24.00</strong></span></span></td>
    <td><span data-ttu-id="bcce5-371"><strong>3,275.00</strong></span><span class="sxs-lookup"><span data-stu-id="bcce5-371"><strong>3,275.00</strong></span></span></td>
    <td></td>
    <td></td>
    <td></td>
    <td><span data-ttu-id="bcce5-372"><strong>4.00</strong></span><span class="sxs-lookup"><span data-stu-id="bcce5-372"><strong>4.00</strong></span></span></td>
    <td><span data-ttu-id="bcce5-373"><strong>364.29</strong></span><span class="sxs-lookup"><span data-stu-id="bcce5-373"><strong>364.29</strong></span></span></td>
    <td><span data-ttu-id="bcce5-374"><strong>5.00</strong></span><span class="sxs-lookup"><span data-stu-id="bcce5-374"><strong>5.00</strong></span></span></td>
    <td><span data-ttu-id="bcce5-375"><strong>455.36</strong></span><span class="sxs-lookup"><span data-stu-id="bcce5-375"><strong>455.36</strong></span></span></td>
    <td><span data-ttu-id="bcce5-376"><strong>15</strong></span><span class="sxs-lookup"><span data-stu-id="bcce5-376"><strong>15</strong></span></span></td>
    <td><span data-ttu-id="bcce5-377"><strong>2,455.36</strong></span><span class="sxs-lookup"><span data-stu-id="bcce5-377"><strong>2,455.36</strong></span></span></td>
</tr>
</tfoot>
</table>
