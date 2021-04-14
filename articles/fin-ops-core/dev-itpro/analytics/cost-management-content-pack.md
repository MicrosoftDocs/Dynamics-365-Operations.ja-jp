---
title: 原価管理 Power BI コンテンツ
description: このトピックでは、原価管理 Power BI コンテンツの内容について説明します。
author: ShylaThompson
ms.date: 03/16/2018
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: CostAdminWorkspace, CostAnalysisWorkspace, CostObjectWithLowestAccuracy, CostVarianceChart, CostObjectWithLowestTurn
audience: Application User, IT Pro
ms.reviewer: kfend
ms.custom: 270314
ms.assetid: 9680d977-43c8-47a7-966d-2280ba21402a
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: kfend
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: fc033e41d17c8bb4c187db60faeefab453b6057a
ms.sourcegitcommit: 074b6e212d19dd5d84881d1cdd096611a18c207f
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 03/31/2021
ms.locfileid: "5755479"
---
# <a name="cost-management-power-bi-content"></a><span data-ttu-id="54884-103">原価管理 Power BI コンテンツ</span><span class="sxs-lookup"><span data-stu-id="54884-103">Cost management Power BI content</span></span>

[!include [banner](../includes/banner.md)]

## <a name="overview"></a><span data-ttu-id="54884-104">概要</span><span class="sxs-lookup"><span data-stu-id="54884-104">Overview</span></span>

<span data-ttu-id="54884-105">**原価管理** Microsoft Power BI コンテンツは、在庫経理担当者または在庫や進行中の作業 (WIP) を担当、または関心を持つ組織の担当者、または標準的な原価差異の分析を担当、または関心を持つ組織の担当者を対象としています。</span><span class="sxs-lookup"><span data-stu-id="54884-105">The **Cost management** Microsoft Power BI content is intended for inventory accountants or individuals in the organization who are responsible for or interested in the status of inventory or work in progress (WIP), or who are responsible for or interested in analyzing standard cost variances.</span></span>

> [!NOTE]
> <span data-ttu-id="54884-106">このトピックで説明する **原価管理** Power BI コンテンツは、Dynamics 365 Finance and Operations 8.0 に適用されます。</span><span class="sxs-lookup"><span data-stu-id="54884-106">The **Cost management** Power BI content described in this this topic applies to Dynamics 365 Finance and Operations 8.0.</span></span>
> 
> <span data-ttu-id="54884-107">AppSource サイトで利用可能な **原価管理** Power BI コンテンツ パックの使用は推奨されていません。</span><span class="sxs-lookup"><span data-stu-id="54884-107">The **Cost management** Power BI content pack, available on the AppSource site, has been deprecated.</span></span> <span data-ttu-id="54884-108">この廃止の詳細については、[Finance and Operations の削除済みまたは非推奨の機能](../migration-upgrade/deprecated-features.md#power-bi-content-packs-available-on-appsource)を参照してください。</span><span class="sxs-lookup"><span data-stu-id="54884-108">For more information about that deprecation, see [Removed or deprecated features for Finance and Operations](../migration-upgrade/deprecated-features.md#power-bi-content-packs-available-on-appsource).</span></span>

<span data-ttu-id="54884-109">この Power BI コンテンツは、在庫のパフォーマンスを監視し、原価の流れを視覚化するのに役立つカテゴリ化された形式を提供します。</span><span class="sxs-lookup"><span data-stu-id="54884-109">This Power BI content provides a categorized format that helps you monitor the performance of inventories and visualize how cost flows through them.</span></span> <span data-ttu-id="54884-110">回転資本率、在庫を保持している日数、精度、「ABC分類」などの経営洞察力を、望ましい集計レベル (会社、品目、品目グループ、またはサイト) で得ることができます。</span><span class="sxs-lookup"><span data-stu-id="54884-110">You can gain managerial insights such as the turnover ratio, number of days that inventory is on hand, accuracy, and "ABC classification" at your preferred aggregated level (company, item, item group, or site).</span></span> <span data-ttu-id="54884-111">利用可能になった情報は、財務諸表の詳細な補足情報として使用できます。</span><span class="sxs-lookup"><span data-stu-id="54884-111">The information that is made available can also be used as a detailed supplement to the financial statement.</span></span>

<span data-ttu-id="54884-112">Power BI コンテンツは **CostObjectStatementCacheMonthly** 集計測定に基づいて作成されます。これには、主なデータ ソースとして **CostObjectStatementCache** テーブルがあります。</span><span class="sxs-lookup"><span data-stu-id="54884-112">The Power BI content is built on the **CostObjectStatementCacheMonthly** aggregated measurement, which has the **CostObjectStatementCache** table as its primary data source.</span></span> <span data-ttu-id="54884-113">この表は、データ セット キャッシュ フレームワークで管理されます。</span><span class="sxs-lookup"><span data-stu-id="54884-113">This table is managed by the Data set cache framework.</span></span> <span data-ttu-id="54884-114">既定では、テーブルは 24 時間ごとに更新されますが、データ セット キャッシュの構成で更新頻度を変更したり、手動更新を有効にすることができます。</span><span class="sxs-lookup"><span data-stu-id="54884-114">By default, the table is updated every 24 hours, but you can change the update frequency or enable manual updates in the configuration of the data set cache.</span></span> <span data-ttu-id="54884-115">手動更新は、**原価管理** ワークスペースまたは **原価分析** ワークスペースのどちらでも実行することができます。</span><span class="sxs-lookup"><span data-stu-id="54884-115">Manual updates can be run in either the **Cost administration** workspace or the **Cost analysis** workspace.</span></span>

<span data-ttu-id="54884-116">**CostObjectStatementCache** テーブルを更新するたびに、Power BI ビジュアル化内のデータを更新する前に **CostObjectStatementCacheMonthly** 集計測定を更新する必要があります。</span><span class="sxs-lookup"><span data-stu-id="54884-116">After every update of the **CostObjectStatementCache** table, the **CostObjectStatementCacheMonthly** aggregated measurement must updated before data in the Power BI visualizations is updated.</span></span>

## <a name="accessing-the-power-bi-content"></a><span data-ttu-id="54884-117">Power BI コンテンツへのアクセス</span><span class="sxs-lookup"><span data-stu-id="54884-117">Accessing the Power BI content</span></span>

<span data-ttu-id="54884-118">**原価管理** Power BI コンテンツは、**原価管理** および **コスト分析** ワークスペースで表示されます。</span><span class="sxs-lookup"><span data-stu-id="54884-118">The **Cost management** Power BI content is shown in the **Cost administration** and **Cost analysis** workspaces.</span></span>

<span data-ttu-id="54884-119">**原価管理** ワークスペースには、次のタブが含まれています。</span><span class="sxs-lookup"><span data-stu-id="54884-119">The **Cost administration** workspace contains the following tabs:</span></span>

- <span data-ttu-id="54884-120">**概要** – このタブは、アプリケーション データを表示します。</span><span class="sxs-lookup"><span data-stu-id="54884-120">**Overview** – This tab shows application data.</span></span>
- <span data-ttu-id="54884-121">**在庫会計ステータス** – このタブでは、Power BI コンテンツが表示されます。</span><span class="sxs-lookup"><span data-stu-id="54884-121">**Inventory accounting status** – This tab shows Power BI content.</span></span>
- <span data-ttu-id="54884-122">**製造会計ステータス** – このタブでは、Power BI コンテンツが表示されます。</span><span class="sxs-lookup"><span data-stu-id="54884-122">**Manufacturing accounting status** – This tab shows Power BI content.</span></span>

<span data-ttu-id="54884-123">**コスト分析** ワークスペースには、次のタブが含まれています。</span><span class="sxs-lookup"><span data-stu-id="54884-123">The **Cost analysis** workspace contains the following tabs:</span></span>

- <span data-ttu-id="54884-124">**概要** – このタブは、アプリケーション データを表示します。</span><span class="sxs-lookup"><span data-stu-id="54884-124">**Overview** – This tab shows application data.</span></span>
- <span data-ttu-id="54884-125">**在庫会計分析** – このタブでは、Power BI コンテンツが表示されます。</span><span class="sxs-lookup"><span data-stu-id="54884-125">**Inventory accounting analysis** – This tab shows Power BI content.</span></span>
- <span data-ttu-id="54884-126">**製造会計分析** – このタブでは、Power BI コンテンツが表示されます。</span><span class="sxs-lookup"><span data-stu-id="54884-126">**Manufacturing accounting analysis** – This tab shows Power BI content.</span></span>
- <span data-ttu-id="54884-127">**標準原価差異分析** – このタブでは、Power BI コンテンツが表示されます。</span><span class="sxs-lookup"><span data-stu-id="54884-127">**Std. cost variance analysis** – This tab shows Power BI content.</span></span>

## <a name="report-pages-that-are-included-in-the-power-bi-content"></a><span data-ttu-id="54884-128">Power BIコンテンツに含まれるレポート ページ</span><span class="sxs-lookup"><span data-stu-id="54884-128">Report pages that are included in the Power BI content</span></span>

<span data-ttu-id="54884-129">**原価管理** Power BI コンテンツには、一連のメトリックスで構成されるレポート ページのセットが含まれています。</span><span class="sxs-lookup"><span data-stu-id="54884-129">The **Cost management** Power BI content includes a set of report pages that consist of a set of metrics.</span></span> <span data-ttu-id="54884-130">これらのメトリックスはグラフ、タイル、表として視覚化されます。</span><span class="sxs-lookup"><span data-stu-id="54884-130">These metrics are visualized as charts, tiles, and tables.</span></span> 

<span data-ttu-id="54884-131">次の表に、**原価管理** Power BI コンテンツの視覚化の概要を示します。</span><span class="sxs-lookup"><span data-stu-id="54884-131">The following tables provide an overview of the visualizations in the **Cost management** Power BI content.</span></span>

### <a name="inventory-accounting-status"></a><span data-ttu-id="54884-132">在庫会計ステータス</span><span class="sxs-lookup"><span data-stu-id="54884-132">Inventory accounting status</span></span>

| <span data-ttu-id="54884-133">レポート ページ</span><span class="sxs-lookup"><span data-stu-id="54884-133">Report page</span></span>                               | <span data-ttu-id="54884-134">視覚化</span><span class="sxs-lookup"><span data-stu-id="54884-134">Visualization</span></span>                                   |
|-------------------------------------------|-------------------------------------------------|
| <span data-ttu-id="54884-135">在庫の概要</span><span class="sxs-lookup"><span data-stu-id="54884-135">Inventory overview</span></span>                        | <span data-ttu-id="54884-136">期首残高</span><span class="sxs-lookup"><span data-stu-id="54884-136">Beginning balance</span></span>                               |
|                                           | <span data-ttu-id="54884-137">差分変更</span><span class="sxs-lookup"><span data-stu-id="54884-137">Net change</span></span>                                      |
|                                           | <span data-ttu-id="54884-138">差分変更 %</span><span class="sxs-lookup"><span data-stu-id="54884-138">Net change %</span></span>                                    |
|                                           | <span data-ttu-id="54884-139">期末残高</span><span class="sxs-lookup"><span data-stu-id="54884-139">Ending balance</span></span>                                  |
|                                           | <span data-ttu-id="54884-140">在庫の正確性</span><span class="sxs-lookup"><span data-stu-id="54884-140">Inventory accuracy</span></span>                              |
|                                           | <span data-ttu-id="54884-141">在庫回転率</span><span class="sxs-lookup"><span data-stu-id="54884-141">Inventory turnover ratio</span></span>                        |
|                                           | <span data-ttu-id="54884-142">手持在庫日数</span><span class="sxs-lookup"><span data-stu-id="54884-142">Days inventory on-hand</span></span>                          |
|                                           | <span data-ttu-id="54884-143">期間内の有効な製品</span><span class="sxs-lookup"><span data-stu-id="54884-143">Active product in period</span></span>                        |
|                                           | <span data-ttu-id="54884-144">期間内の有効な原価オブジェクト</span><span class="sxs-lookup"><span data-stu-id="54884-144">Active cost objects in period</span></span>                   |
|                                           | <span data-ttu-id="54884-145">品目グループ別残高</span><span class="sxs-lookup"><span data-stu-id="54884-145">Balance by item group</span></span>                           |
|                                           | <span data-ttu-id="54884-146">サイト別の残高</span><span class="sxs-lookup"><span data-stu-id="54884-146">Balance by site</span></span>                                 |
|                                           | <span data-ttu-id="54884-147">カテゴリ別の明細書</span><span class="sxs-lookup"><span data-stu-id="54884-147">Statement by category</span></span>                           |
|                                           | <span data-ttu-id="54884-148">四半期ごとの差分変更</span><span class="sxs-lookup"><span data-stu-id="54884-148">Net change by quarter</span></span>                           |
| <span data-ttu-id="54884-149">サイトおよび品目グループ別在庫の概要</span><span class="sxs-lookup"><span data-stu-id="54884-149">Inventory overview by site and item group</span></span> | <span data-ttu-id="54884-150">サイト別の在庫の正確性</span><span class="sxs-lookup"><span data-stu-id="54884-150">Inventory accuracy by site</span></span>                      |
|                                           | <span data-ttu-id="54884-151">サイト別の在庫回転率</span><span class="sxs-lookup"><span data-stu-id="54884-151">Inventory turnover ratio by site</span></span>                |
|                                           | <span data-ttu-id="54884-152">サイト別の在庫期末残高</span><span class="sxs-lookup"><span data-stu-id="54884-152">Inventory ending balance by site</span></span>                |
|                                           | <span data-ttu-id="54884-153">品目グループ別の在庫の正確性</span><span class="sxs-lookup"><span data-stu-id="54884-153">Inventory accuracy by item group</span></span>                |
|                                           | <span data-ttu-id="54884-154">品目グループ別の在庫回転率</span><span class="sxs-lookup"><span data-stu-id="54884-154">Inventory turnover ratio by item group</span></span>          |
|                                           | <span data-ttu-id="54884-155">サイトおよび品目グループ別の在庫期末残高</span><span class="sxs-lookup"><span data-stu-id="54884-155">Inventory ending balance by site and item group</span></span> |
| <span data-ttu-id="54884-156">在庫明細書</span><span class="sxs-lookup"><span data-stu-id="54884-156">Inventory statement</span></span>                       | <span data-ttu-id="54884-157">在庫明細書</span><span class="sxs-lookup"><span data-stu-id="54884-157">Inventory statement</span></span>                             |
| <span data-ttu-id="54884-158">サイトごとの在庫明細書</span><span class="sxs-lookup"><span data-stu-id="54884-158">Inventory statement by site</span></span>               | <span data-ttu-id="54884-159">サイトごとの在庫明細書</span><span class="sxs-lookup"><span data-stu-id="54884-159">Inventory statement by site</span></span>                     |
| <span data-ttu-id="54884-160">製品階層別の在庫明細書</span><span class="sxs-lookup"><span data-stu-id="54884-160">Inventory statement by product hierarchy</span></span>  | <span data-ttu-id="54884-161">在庫明細書</span><span class="sxs-lookup"><span data-stu-id="54884-161">Inventory statement</span></span>                             |
| <span data-ttu-id="54884-162">製品階層別の在庫明細書</span><span class="sxs-lookup"><span data-stu-id="54884-162">Inventory statement by product hierarchy</span></span>  | <span data-ttu-id="54884-163">サイトごとの在庫明細書</span><span class="sxs-lookup"><span data-stu-id="54884-163">Inventory statement by site</span></span>                     |

### <a name="manufacturing-accounting-status"></a><span data-ttu-id="54884-164">製造会計ステータス</span><span class="sxs-lookup"><span data-stu-id="54884-164">Manufacturing accounting status</span></span>

| <span data-ttu-id="54884-165">レポート ページ</span><span class="sxs-lookup"><span data-stu-id="54884-165">Report page</span></span>                | <span data-ttu-id="54884-166">視覚化</span><span class="sxs-lookup"><span data-stu-id="54884-166">Visualization</span></span>                       |
|----------------------------|-------------------------------------|
| <span data-ttu-id="54884-167">仕掛品の概要 YTD</span><span class="sxs-lookup"><span data-stu-id="54884-167">WIP overview YTD</span></span>           | <span data-ttu-id="54884-168">期首残高</span><span class="sxs-lookup"><span data-stu-id="54884-168">Beginning balance</span></span>                   |
|                            | <span data-ttu-id="54884-169">差分変更</span><span class="sxs-lookup"><span data-stu-id="54884-169">Net change</span></span>                          |
|                            | <span data-ttu-id="54884-170">差分変更 %</span><span class="sxs-lookup"><span data-stu-id="54884-170">Net change %</span></span>                        |
|                            | <span data-ttu-id="54884-171">期末残高</span><span class="sxs-lookup"><span data-stu-id="54884-171">Ending balance</span></span>                      |
|                            | <span data-ttu-id="54884-172">仕掛品回転資本率</span><span class="sxs-lookup"><span data-stu-id="54884-172">WIP turnover ratio</span></span>                  |
|                            | <span data-ttu-id="54884-173">手持仕掛品日数</span><span class="sxs-lookup"><span data-stu-id="54884-173">Days WIP on-hand</span></span>                    |
|                            | <span data-ttu-id="54884-174">期間内の有効な原価オブジェクト</span><span class="sxs-lookup"><span data-stu-id="54884-174">Active cost object in period</span></span>        |
|                            | <span data-ttu-id="54884-175">リソース グループ別の差分変更</span><span class="sxs-lookup"><span data-stu-id="54884-175">Net change by resource group</span></span>        |
|                            | <span data-ttu-id="54884-176">サイト別の残高</span><span class="sxs-lookup"><span data-stu-id="54884-176">Balance by site</span></span>                     |
|                            | <span data-ttu-id="54884-177">カテゴリ別の明細書</span><span class="sxs-lookup"><span data-stu-id="54884-177">Statement by category</span></span>               |
|                            | <span data-ttu-id="54884-178">四半期ごとの差分変更</span><span class="sxs-lookup"><span data-stu-id="54884-178">Net change by quarter</span></span>               |
| <span data-ttu-id="54884-179">仕掛報告書</span><span class="sxs-lookup"><span data-stu-id="54884-179">WIP statement</span></span>              | <span data-ttu-id="54884-180">期首残高</span><span class="sxs-lookup"><span data-stu-id="54884-180">Beginning balance</span></span>                   |
|                            | <span data-ttu-id="54884-181">期末残高</span><span class="sxs-lookup"><span data-stu-id="54884-181">Ending balance</span></span>                      |
|                            | <span data-ttu-id="54884-182">カテゴリ別の仕掛品明細書</span><span class="sxs-lookup"><span data-stu-id="54884-182">WIP statement by category</span></span>           |
| <span data-ttu-id="54884-183">サイト別の仕掛品明細書</span><span class="sxs-lookup"><span data-stu-id="54884-183">WIP statement by site</span></span>      | <span data-ttu-id="54884-184">期首残高</span><span class="sxs-lookup"><span data-stu-id="54884-184">Beginning balance</span></span>                   |
|                            | <span data-ttu-id="54884-185">期末残高</span><span class="sxs-lookup"><span data-stu-id="54884-185">Ending balance</span></span>                      |
|                            | <span data-ttu-id="54884-186">カテゴリおよびサイト別の仕掛品明細書</span><span class="sxs-lookup"><span data-stu-id="54884-186">WIP statement by category and site</span></span>  |
| <span data-ttu-id="54884-187">カテゴリ階層別の仕掛品明細書</span><span class="sxs-lookup"><span data-stu-id="54884-187">WIP statement by hierarchy</span></span> | <span data-ttu-id="54884-188">期首残高</span><span class="sxs-lookup"><span data-stu-id="54884-188">Beginning balance</span></span>                   |
|                            | <span data-ttu-id="54884-189">期末残高</span><span class="sxs-lookup"><span data-stu-id="54884-189">Ending balance</span></span>                      |
|                            | <span data-ttu-id="54884-190">カテゴリ階層別の仕掛品明細書</span><span class="sxs-lookup"><span data-stu-id="54884-190">WIP statement by category hierarchy</span></span> |

### <a name="inventory-accounting-analysis"></a><span data-ttu-id="54884-191">在庫会計分析</span><span class="sxs-lookup"><span data-stu-id="54884-191">Inventory accounting analysis</span></span>

| <span data-ttu-id="54884-192">レポート ページ</span><span class="sxs-lookup"><span data-stu-id="54884-192">Report page</span></span>        | <span data-ttu-id="54884-193">視覚化</span><span class="sxs-lookup"><span data-stu-id="54884-193">Visualization</span></span>                                                                |
|--------------------|------------------------------------------------------------------------------|
| <span data-ttu-id="54884-194">在庫の詳細</span><span class="sxs-lookup"><span data-stu-id="54884-194">Inventory details</span></span>  | <span data-ttu-id="54884-195">期末残高別の上位 10 リソース</span><span class="sxs-lookup"><span data-stu-id="54884-195">Top 10 resources by ending balance</span></span>                                           |
|                    | <span data-ttu-id="54884-196">差分変更増加別の上位 10 リソース</span><span class="sxs-lookup"><span data-stu-id="54884-196">Top 10 resources by net change increase</span></span>                                      |
|                    | <span data-ttu-id="54884-197">差分変更減少別の上位 10 リソース</span><span class="sxs-lookup"><span data-stu-id="54884-197">Top 10 resources by net change decrease</span></span>                                      |
|                    | <span data-ttu-id="54884-198">在庫回転率別の上位 10 リソース</span><span class="sxs-lookup"><span data-stu-id="54884-198">Top 10 resources by inventory turnover ratio</span></span>                                 |
|                    | <span data-ttu-id="54884-199">低在庫回転率と期末残高がしきい値以上のリソース</span><span class="sxs-lookup"><span data-stu-id="54884-199">Resources by low inventory turnover ratio and ending balance above threshold</span></span> |
|                    | <span data-ttu-id="54884-200">低精度の上位 10 リソース</span><span class="sxs-lookup"><span data-stu-id="54884-200">Top 10 resources by low accuracy</span></span>                                             |
| <span data-ttu-id="54884-201">ABC 分類</span><span class="sxs-lookup"><span data-stu-id="54884-201">ABC classification</span></span> | <span data-ttu-id="54884-202">在庫期末残高</span><span class="sxs-lookup"><span data-stu-id="54884-202">Inventory ending balance</span></span>                                                     |
|                    | <span data-ttu-id="54884-203">消費された材料</span><span class="sxs-lookup"><span data-stu-id="54884-203">Consumed material</span></span>                                                            |
|                    | <span data-ttu-id="54884-204">売却 (COGS)</span><span class="sxs-lookup"><span data-stu-id="54884-204">Sold (COGS)</span></span>                                                                  |
| <span data-ttu-id="54884-205">在庫のトレンド</span><span class="sxs-lookup"><span data-stu-id="54884-205">Inventory trends</span></span>   | <span data-ttu-id="54884-206">在庫期末残高</span><span class="sxs-lookup"><span data-stu-id="54884-206">Inventory ending balance</span></span>                                                     |
|                    | <span data-ttu-id="54884-207">在庫差分変更</span><span class="sxs-lookup"><span data-stu-id="54884-207">Inventory net change</span></span>                                                         |
|                    | <span data-ttu-id="54884-208">在庫回転率</span><span class="sxs-lookup"><span data-stu-id="54884-208">Inventory turnover ratio</span></span>                                                     |
|                    | <span data-ttu-id="54884-209">在庫の正確性</span><span class="sxs-lookup"><span data-stu-id="54884-209">Inventory accuracy</span></span>                                                           |

### <a name="manufacturing-accounting-analysis"></a><span data-ttu-id="54884-210">製造会計分析</span><span class="sxs-lookup"><span data-stu-id="54884-210">Manufacturing accounting analysis</span></span>

| <span data-ttu-id="54884-211">レポート ページ</span><span class="sxs-lookup"><span data-stu-id="54884-211">Report page</span></span> | <span data-ttu-id="54884-212">視覚化</span><span class="sxs-lookup"><span data-stu-id="54884-212">Visualization</span></span>      |
|-------------|--------------------|
| <span data-ttu-id="54884-213">仕掛品のトレンド</span><span class="sxs-lookup"><span data-stu-id="54884-213">WIP trends</span></span>  | <span data-ttu-id="54884-214">仕掛品期末残高</span><span class="sxs-lookup"><span data-stu-id="54884-214">WIP ending balance</span></span> |
|             | <span data-ttu-id="54884-215">仕掛品差分変更</span><span class="sxs-lookup"><span data-stu-id="54884-215">WIP net change</span></span>     |
|             | <span data-ttu-id="54884-216">仕掛品回転資本率</span><span class="sxs-lookup"><span data-stu-id="54884-216">WIP turnover ratio</span></span> |

### <a name="std-cost-variance-analysis"></a><span data-ttu-id="54884-217">標準原価差異分析</span><span class="sxs-lookup"><span data-stu-id="54884-217">Std. cost variance analysis</span></span>

| <span data-ttu-id="54884-218">レポート ページ</span><span class="sxs-lookup"><span data-stu-id="54884-218">Report page</span></span>                             | <span data-ttu-id="54884-219">視覚化</span><span class="sxs-lookup"><span data-stu-id="54884-219">Visualization</span></span>                                        |
|-----------------------------------------|------------------------------------------------------|
| <span data-ttu-id="54884-220">購買価格差異 (標準原価) YTD</span><span class="sxs-lookup"><span data-stu-id="54884-220">Purchase price variance (Std. cost) YTD</span></span> | <span data-ttu-id="54884-221">調達済み残高</span><span class="sxs-lookup"><span data-stu-id="54884-221">Procured balance</span></span>                                     |
|                                         | <span data-ttu-id="54884-222">購買価格差異</span><span class="sxs-lookup"><span data-stu-id="54884-222">Purchase price variance</span></span>                              |
|                                         | <span data-ttu-id="54884-223">購買価格差異比率</span><span class="sxs-lookup"><span data-stu-id="54884-223">Purchase price variance ratio</span></span>                        |
|                                         | <span data-ttu-id="54884-224">品目グループ別の差異</span><span class="sxs-lookup"><span data-stu-id="54884-224">Variance by item group</span></span>                               |
|                                         | <span data-ttu-id="54884-225">サイト別の差異</span><span class="sxs-lookup"><span data-stu-id="54884-225">Variance by site</span></span>                                     |
|                                         | <span data-ttu-id="54884-226">四半期ごとの購買価格</span><span class="sxs-lookup"><span data-stu-id="54884-226">Purchase price by quarter</span></span>                            |
|                                         | <span data-ttu-id="54884-227">四半期および品目グループごとの購買価格</span><span class="sxs-lookup"><span data-stu-id="54884-227">Purchase price by quarter and Item group</span></span>             |
|                                         | <span data-ttu-id="54884-228">好ましくない購買価格比率の上位 10 リソース</span><span class="sxs-lookup"><span data-stu-id="54884-228">Top 10 resources by unfavorable purchase price ratio</span></span> |
|                                         | <span data-ttu-id="54884-229">有利な購買価格比率の上位 10 リソース</span><span class="sxs-lookup"><span data-stu-id="54884-229">Top 10 resources by favorable purchase price ratio</span></span>   |
| <span data-ttu-id="54884-230">製造差異 (標準原価) YTD</span><span class="sxs-lookup"><span data-stu-id="54884-230">Production variance (Std. cost) YTD</span></span>     | <span data-ttu-id="54884-231">製造原価</span><span class="sxs-lookup"><span data-stu-id="54884-231">Manufactured cost</span></span>                                    |
|                                         | <span data-ttu-id="54884-232">製造差異</span><span class="sxs-lookup"><span data-stu-id="54884-232">Production variance</span></span>                                  |
|                                         | <span data-ttu-id="54884-233">製造差異比率</span><span class="sxs-lookup"><span data-stu-id="54884-233">Production variance ratio</span></span>                            |
|                                         | <span data-ttu-id="54884-234">品目グループ別の差異</span><span class="sxs-lookup"><span data-stu-id="54884-234">Variance by item group</span></span>                               |
|                                         | <span data-ttu-id="54884-235">サイト別の差異</span><span class="sxs-lookup"><span data-stu-id="54884-235">Variance by site</span></span>                                     |
|                                         | <span data-ttu-id="54884-236">四半期ごとの製造差異</span><span class="sxs-lookup"><span data-stu-id="54884-236">Production variance by quarter</span></span>                       |
|                                         | <span data-ttu-id="54884-237">四半期および差異タイプによる製造差異</span><span class="sxs-lookup"><span data-stu-id="54884-237">Production variance by quarter and variance type</span></span>     |
|                                         | <span data-ttu-id="54884-238">好ましくない製造差異の上位 10 リソース</span><span class="sxs-lookup"><span data-stu-id="54884-238">Top 10 resources by unfavorable production variance</span></span>  |
|                                         | <span data-ttu-id="54884-239">有利な製造差異の上位 10 リソース</span><span class="sxs-lookup"><span data-stu-id="54884-239">Top 10 resources by favorable production variance</span></span>    |

## <a name="understanding-the-data-model-and-entities"></a><span data-ttu-id="54884-240">データ モデルおよびエンティティの理解</span><span class="sxs-lookup"><span data-stu-id="54884-240">Understanding the data model and entities</span></span>

<span data-ttu-id="54884-241">アプリケーションからのデータは、**原価管理** Power BI コンテンツのレポート ページに入力するために使用されます。</span><span class="sxs-lookup"><span data-stu-id="54884-241">Data from the application is used to fill the report pages in the **Cost management** Power BI content.</span></span> <span data-ttu-id="54884-242">このデータは、分析用に最適化された Microsoft SQL Server データベースであるエンティティ格納でステージ完了である集計の測定として表されます。</span><span class="sxs-lookup"><span data-stu-id="54884-242">This data is represented as aggregate measurements that are staged in the entity store, which is a Microsoft SQL Server database that is optimized for analytics.</span></span> <span data-ttu-id="54884-243">詳細については、[エンティティ格納と Power BI の統合](power-bi-integration-entity-store.md) を参照してください。</span><span class="sxs-lookup"><span data-stu-id="54884-243">For more information, see [Power BI integration with Entity store](power-bi-integration-entity-store.md).</span></span>

<span data-ttu-id="54884-244">次のオブジェクトのキー集計の測定は、Power BI コンテンツの基準として使用されます。</span><span class="sxs-lookup"><span data-stu-id="54884-244">The key aggregate measurements of the following objects are used as the basis of the Power BI content.</span></span>

| <span data-ttu-id="54884-245">オブジェクト</span><span class="sxs-lookup"><span data-stu-id="54884-245">Object</span></span>                          | <span data-ttu-id="54884-246">キー集計の測定</span><span class="sxs-lookup"><span data-stu-id="54884-246">Key aggregate measurements</span></span> | <span data-ttu-id="54884-247">Finance and Operations のデータ ソース</span><span class="sxs-lookup"><span data-stu-id="54884-247">Data source for Finance and Operations</span></span> | <span data-ttu-id="54884-248">フィールド</span><span class="sxs-lookup"><span data-stu-id="54884-248">Field</span></span>               |
|---------------------------------|----------------------------|----------------------------------------|---------------------|
| <span data-ttu-id="54884-249">CostObjectStatementCacheMonthly</span><span class="sxs-lookup"><span data-stu-id="54884-249">CostObjectStatementCacheMonthly</span></span> | <span data-ttu-id="54884-250">日数</span><span class="sxs-lookup"><span data-stu-id="54884-250">Amount</span></span>                     | <span data-ttu-id="54884-251">CostObjectStatementCache</span><span class="sxs-lookup"><span data-stu-id="54884-251">CostObjectStatementCache</span></span>               | <span data-ttu-id="54884-252">量</span><span class="sxs-lookup"><span data-stu-id="54884-252">Amount</span></span>              |
| <span data-ttu-id="54884-253">CostObjectStatementCacheMonthly</span><span class="sxs-lookup"><span data-stu-id="54884-253">CostObjectStatementCacheMonthly</span></span> | <span data-ttu-id="54884-254">件数</span><span class="sxs-lookup"><span data-stu-id="54884-254">Quantity</span></span>                   | <span data-ttu-id="54884-255">CostObjectStatementCache</span><span class="sxs-lookup"><span data-stu-id="54884-255">CostObjectStatementCache</span></span>               | <span data-ttu-id="54884-256">数量</span><span class="sxs-lookup"><span data-stu-id="54884-256">Qty</span></span>                 |
| <span data-ttu-id="54884-257">CostInventoryAccountingKPIGoal</span><span class="sxs-lookup"><span data-stu-id="54884-257">CostInventoryAccountingKPIGoal</span></span>  | <span data-ttu-id="54884-258">AnnualInventoryTurn</span><span class="sxs-lookup"><span data-stu-id="54884-258">AnnualInventoryTurn</span></span>        | <span data-ttu-id="54884-259">CostInventoryAccountingKPIGoal</span><span class="sxs-lookup"><span data-stu-id="54884-259">CostInventoryAccountingKPIGoal</span></span>         | <span data-ttu-id="54884-260">AnnualInventoryTurn</span><span class="sxs-lookup"><span data-stu-id="54884-260">AnnualInventoryTurn</span></span> |
| <span data-ttu-id="54884-261">CostInventoryAccountingKPIGoal</span><span class="sxs-lookup"><span data-stu-id="54884-261">CostInventoryAccountingKPIGoal</span></span>  | <span data-ttu-id="54884-262">InventoryAccuracy</span><span class="sxs-lookup"><span data-stu-id="54884-262">InventoryAccuracy</span></span>          | <span data-ttu-id="54884-263">CostInventoryAccountingKPIGoal</span><span class="sxs-lookup"><span data-stu-id="54884-263">CostInventoryAccountingKPIGoal</span></span>         | <span data-ttu-id="54884-264">InventoryAccuracy</span><span class="sxs-lookup"><span data-stu-id="54884-264">InventoryAccuracy</span></span>   |

<span data-ttu-id="54884-265">次の表は、Power BI コンテンツでキー計算された測定値を示しています。</span><span class="sxs-lookup"><span data-stu-id="54884-265">The following table shows the key calculated measurements in the Power BI content.</span></span>

| <span data-ttu-id="54884-266">測定</span><span class="sxs-lookup"><span data-stu-id="54884-266">Measure</span></span>                            | <span data-ttu-id="54884-267">計算</span><span class="sxs-lookup"><span data-stu-id="54884-267">Calculation</span></span> |
|------------------------------------|-------------|
| <span data-ttu-id="54884-268">期首残高</span><span class="sxs-lookup"><span data-stu-id="54884-268">Beginning balance</span></span>                  | <span data-ttu-id="54884-269">期首残高 = \[期末残高\]-\[差分変更\]</span><span class="sxs-lookup"><span data-stu-id="54884-269">Beginning balance = \[Ending balance\]-\[Net change\]</span></span> |
| <span data-ttu-id="54884-270">期首残高数量</span><span class="sxs-lookup"><span data-stu-id="54884-270">Beginning balance qty.</span></span>             | <span data-ttu-id="54884-271">期首残高数量 = \[期末残高数量\]-\[差分変更数量\]</span><span class="sxs-lookup"><span data-stu-id="54884-271">Beginning balance qty. = \[Ending balance qty.\]-\[Net change qty.\]</span></span> |
| <span data-ttu-id="54884-272">期末残高</span><span class="sxs-lookup"><span data-stu-id="54884-272">Ending balance</span></span>                     | <span data-ttu-id="54884-273">期末残高 = (CALCULATE(SUM(\[Amount\]), FILTER(ALL(FiscalCalendar) ,FiscalCalendar\[MONTHSTARTDATE\] \<= MAX(FiscalCalendar\[MONTHSTARTDATE\]))))</span><span class="sxs-lookup"><span data-stu-id="54884-273">Ending balance = (CALCULATE(SUM(\[Amount\]), FILTER(ALL(FiscalCalendar) ,FiscalCalendar\[MONTHSTARTDATE\] \<= MAX(FiscalCalendar\[MONTHSTARTDATE\]))))</span></span> |
| <span data-ttu-id="54884-274">期末残高数量</span><span class="sxs-lookup"><span data-stu-id="54884-274">Ending balance qty.</span></span>                | <span data-ttu-id="54884-275">期末残高数量 = CALCULATE(SUM(\[QTY\]), FILTER(ALL(FiscalCalendar),FiscalCalendar\[MONTHSTARTDATE\] \<= MAX(FiscalCalendar\[MONTHSTARTDATE\])))</span><span class="sxs-lookup"><span data-stu-id="54884-275">Ending balance qty. = CALCULATE(SUM(\[QTY\]), FILTER(ALL(FiscalCalendar),FiscalCalendar\[MONTHSTARTDATE\] \<= MAX(FiscalCalendar\[MONTHSTARTDATE\])))</span></span> |
| <span data-ttu-id="54884-276">差分変更</span><span class="sxs-lookup"><span data-stu-id="54884-276">Net change</span></span>                         | <span data-ttu-id="54884-277">差分変更 = SUM(\[AMOUNT\])</span><span class="sxs-lookup"><span data-stu-id="54884-277">Net change = SUM(\[AMOUNT\])</span></span> |
| <span data-ttu-id="54884-278">差分変更数量</span><span class="sxs-lookup"><span data-stu-id="54884-278">Net change qty.</span></span>                    | <span data-ttu-id="54884-279">差分変更数量 = SUM(\[QTY\])</span><span class="sxs-lookup"><span data-stu-id="54884-279">Net change qty. = SUM(\[QTY\])</span></span> |
| <span data-ttu-id="54884-280">金額別の在庫回転率</span><span class="sxs-lookup"><span data-stu-id="54884-280">Inventory turnover ratio by amount</span></span> | <span data-ttu-id="54884-281">金額別の在庫回転率 = if(OR(\[在庫平均残数\] \<= 0, \[Inventory sold or consumed issues\] \> = 0), 0, ABS(\[販売在庫または消費の払出\])/\[在庫平均残数\])</span><span class="sxs-lookup"><span data-stu-id="54884-281">Inventory turnover ratio by amount = if(OR(\[Inventory average balance\] \<= 0, \[Inventory sold or consumed issues\] \>= 0), 0, ABS(\[Inventory sold or consumed issues\])/\[Inventory average balance\])</span></span> |
| <span data-ttu-id="54884-282">在庫平均残高</span><span class="sxs-lookup"><span data-stu-id="54884-282">Inventory average balance</span></span>          | <span data-ttu-id="54884-283">在庫平均残高 = ((\[期末残高\] + \[期首残高\]) / 2)</span><span class="sxs-lookup"><span data-stu-id="54884-283">Inventory average balance = ((\[Ending balance\] + \[Beginning balance\]) / 2)</span></span> |
| <span data-ttu-id="54884-284">手持在庫日数</span><span class="sxs-lookup"><span data-stu-id="54884-284">Days inventory on-hand</span></span>             | <span data-ttu-id="54884-285">手持在庫日数 = 365 / CostObjectStatementEntries\[金額別の在庫回転率\]</span><span class="sxs-lookup"><span data-stu-id="54884-285">Days inventory onhand = 365 / CostObjectStatementEntries\[Inventory turnover ratio by amount\]</span></span> |
| <span data-ttu-id="54884-286">在庫の正確性</span><span class="sxs-lookup"><span data-stu-id="54884-286">Inventory accuracy</span></span>                 | <span data-ttu-id="54884-287">金額による在庫の正確度 = IF ( \[終了残数\] \<= 0, IF(OR(\[Inventory counted amount\] \<\> 0、\[終了残数 \] \< 0)、0、1)、MAX (0, (\[終了残数\] - ABS (\[在庫棚卸\]))/\[終了残数\]))</span><span class="sxs-lookup"><span data-stu-id="54884-287">Inventory accuracy by amount = IF(\[Ending balance\] \<= 0, IF(OR(\[Inventory counted amount\] \<\> 0, \[Ending balance\] \< 0), 0, 1), MAX(0, (\[Ending balance\] - ABS(\[Inventory counted amount\]))/\[Ending balance\]))</span></span> |

<span data-ttu-id="54884-288">以下のキー分析コードは、より高い粒度を達成し深い分析洞察を取得できるように、集計の測定をスライスするフィルターとして使用されます。</span><span class="sxs-lookup"><span data-stu-id="54884-288">The following key dimensions are used as filters to slice the aggregate measurements, so that you can achieve greater granularity and gain deeper analytical insights.</span></span>


| <span data-ttu-id="54884-289">エンティティ</span><span class="sxs-lookup"><span data-stu-id="54884-289">Entity</span></span>                                                  | <span data-ttu-id="54884-290">属性の例</span><span class="sxs-lookup"><span data-stu-id="54884-290">Examples of attributes</span></span>                          |
|---------------------------------------------------------|-------------------------------------------------|
| <span data-ttu-id="54884-291">製品</span><span class="sxs-lookup"><span data-stu-id="54884-291">Products</span></span>                                                | <span data-ttu-id="54884-292">製品番号、製品名、単位、品目グループ</span><span class="sxs-lookup"><span data-stu-id="54884-292">Product number, Product name, Unit, Item groups</span></span> |
| <span data-ttu-id="54884-293">カテゴリ階層 (原価管理のロールに割り当て)</span><span class="sxs-lookup"><span data-stu-id="54884-293">Category hierarchies (Assigned to role Cost management)</span></span> | <span data-ttu-id="54884-294">カテゴリ階層、カテゴリ レベル</span><span class="sxs-lookup"><span data-stu-id="54884-294">Category hierarchy, Category level</span></span>              |
| <span data-ttu-id="54884-295">法人</span><span class="sxs-lookup"><span data-stu-id="54884-295">Legal entities</span></span>                                          | <span data-ttu-id="54884-296">法人名</span><span class="sxs-lookup"><span data-stu-id="54884-296">Legal entity names</span></span>                              |
| <span data-ttu-id="54884-297">会計カレンダー</span><span class="sxs-lookup"><span data-stu-id="54884-297">Fiscal calendars</span></span>                                        | <span data-ttu-id="54884-298">会計カレンダー、年、四半期、期間、月</span><span class="sxs-lookup"><span data-stu-id="54884-298">Fiscal calendar, Year, Quarter, Period, Month</span></span>   |
| <span data-ttu-id="54884-299">サイト</span><span class="sxs-lookup"><span data-stu-id="54884-299">Site</span></span>                                                    | <span data-ttu-id="54884-300">ID、名前、住所、都道府県、国</span><span class="sxs-lookup"><span data-stu-id="54884-300">ID, Name, Address, State, Country</span></span>               |


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]