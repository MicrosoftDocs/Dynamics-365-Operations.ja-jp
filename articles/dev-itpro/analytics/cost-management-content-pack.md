---
title: "原価管理 Power BI コンテンツ"
description: "このトピックでは、原価管理 Power BI コンテンツの内容について説明します。"
author: YuyuScheller
manager: AnnBe
ms.date: 03/16/2018
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-platform
ms.technology: 
ms.search.form: CostAdminWorkspace, CostAnalysisWorkspace
audience: Application User, IT Pro
ms.reviewer: sericks
ms.search.scope: Operations
ms.custom: 270314
ms.assetid: 9680d977-43c8-47a7-966d-2280ba21402a
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: yuyus
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: a8b5a5af5108744406a3d2fb84d7151baea2481b
ms.openlocfilehash: a4eacafdf9b9e0eabe7fe599e679fca18c749733
ms.contentlocale: ja-jp
ms.lasthandoff: 04/13/2018

---

# <a name="cost-management-power-bi-content"></a><span data-ttu-id="7e823-103">原価管理 Power BI コンテンツ</span><span class="sxs-lookup"><span data-stu-id="7e823-103">Cost management Power BI content</span></span>

[!INCLUDE [banner](../includes/banner.md)]

## <a name="overview"></a><span data-ttu-id="7e823-104">概要</span><span class="sxs-lookup"><span data-stu-id="7e823-104">Overview</span></span>

<span data-ttu-id="7e823-105">**原価管理** Microsoft Power BI コンテンツは、在庫経理担当者または在庫や進行中の作業 (WIP) を担当、または関心を持つ組織の担当者、または標準的な原価差異の分析を担当、または関心を持つ組織の担当者を対象としています。</span><span class="sxs-lookup"><span data-stu-id="7e823-105">The **Cost management** Microsoft Power BI content is intended for inventory accountants or individuals in the organization who are responsible for or interested in the status of inventory or work in progress (WIP), or who are responsible for or interested in analyzing standard cost variances.</span></span>

> [!Note]
> <span data-ttu-id="7e823-106">このトピックで説明する**原価管理** Power BIコンテンツは Dynamics 365 for Finance and Operations 8.0 に適用されます。</span><span class="sxs-lookup"><span data-stu-id="7e823-106">The **Cost management** Power BI content described in this this topic applies to Dynamics 365 for Finance and Operations 8.0.</span></span>
> 
> <span data-ttu-id="7e823-107">PowerBI.com サイトに公開された**原価管理** Power BI コンテンツ パックの使用は推奨されていません。</span><span class="sxs-lookup"><span data-stu-id="7e823-107">The **Cost management** Power BI content pack, published to the PowerBI.com site has been deprecated.</span></span> <span data-ttu-id="7e823-108">非推奨に関しての詳細については [Power BI コンテンツ パックは PowerBI.com に公開します](../migration-upgrade/deprecated-features.md#power-bi-content-packs-published-to-powerbicom) の記事を参照してください。</span><span class="sxs-lookup"><span data-stu-id="7e823-108">For more information about that deprecation, see [Power BI content packs published to PowerBI.com](../migration-upgrade/deprecated-features.md#power-bi-content-packs-published-to-powerbicom).</span></span>


<span data-ttu-id="7e823-109">この Power BI コンテンツは、在庫のパフォーマンスを監視し、原価の流れを視覚化するのに役立つカテゴリ化された形式を提供します。</span><span class="sxs-lookup"><span data-stu-id="7e823-109">This Power BI content provides a categorized format that helps you monitor the performance of inventories and visualize how cost flows through them.</span></span> <span data-ttu-id="7e823-110">回転資本率、在庫を保持している日数、精度、「ABC分類」などの経営洞察力を、望ましい集計レベル (会社、品目、品目グループ、またはサイト) で得ることができます。</span><span class="sxs-lookup"><span data-stu-id="7e823-110">You can gain managerial insights such as the turnover ratio, number of days that inventory is on hand, accuracy, and "ABC classification" at your preferred aggregated level (company, item, item group, or site).</span></span> <span data-ttu-id="7e823-111">利用可能になった情報は、財務諸表の詳細な補足情報として使用できます。</span><span class="sxs-lookup"><span data-stu-id="7e823-111">The information that is made available can also be used as a detailed supplement to the financial statement.</span></span>

<span data-ttu-id="7e823-112">The Power BI コンテンツは **CostObjectStatementCacheMonthly** 集計測定に基づいて作成されます。これには、主なデータソースとして **CostObjectStatementCache** テーブルがあります。</span><span class="sxs-lookup"><span data-stu-id="7e823-112">The Power BI content is built on the **CostObjectStatementCacheMonthly** aggregated measurement, which has the **CostObjectStatementCache** table as its primary data source.</span></span> <span data-ttu-id="7e823-113">この表は、データ セット キャッシュ フレームワークで管理されます。</span><span class="sxs-lookup"><span data-stu-id="7e823-113">This table is managed by the Data set cache framework.</span></span> <span data-ttu-id="7e823-114">既定では、テーブルは 24 時間ごとに更新されますが、データ セット キャッシュの構成で更新頻度を変更したり、手動更新を有効にすることができます。</span><span class="sxs-lookup"><span data-stu-id="7e823-114">By default, the table is updated every 24 hours, but you can change the update frequency or enable manual updates in the configuration of the data set cache.</span></span> <span data-ttu-id="7e823-115">手動更新は、**原価管理**ワークスペースまたは**原価分析**ワークスペースのどちらでも実行することができます。</span><span class="sxs-lookup"><span data-stu-id="7e823-115">Manual updates can be run in either the **Cost administration** workspace or the **Cost analysis** workspace.</span></span>

<span data-ttu-id="7e823-116">**CostObjectStatementCache** テーブルを更新するたびに、Power BI ビジュアル化内のデータを更新する前に **CostObjectStatementCacheMonthly** 集計測定を更新する必要があります。</span><span class="sxs-lookup"><span data-stu-id="7e823-116">After every update of the **CostObjectStatementCache** table, the **CostObjectStatementCacheMonthly** aggregated measurement must updated before data in the Power BI visualizations is updated.</span></span>

## <a name="accessing-the-power-bi-content"></a><span data-ttu-id="7e823-117">Power BI コンテンツへのアクセス</span><span class="sxs-lookup"><span data-stu-id="7e823-117">Accessing the Power BI content</span></span>

<span data-ttu-id="7e823-118">**原価管理** Power BI コンテンツは、**原価管理**および**コスト分析**ワークスペースで表示されます。</span><span class="sxs-lookup"><span data-stu-id="7e823-118">The **Cost management** Power BI content is shown in the **Cost administration** and **Cost analysis** workspaces.</span></span>

<span data-ttu-id="7e823-119">**原価管理**ワークスペースには、次のタブが含まれています。</span><span class="sxs-lookup"><span data-stu-id="7e823-119">The **Cost administration** workspace contains the following tabs:</span></span>

- <span data-ttu-id="7e823-120">**概要** – このタブは、アプリケーション データを表示します。</span><span class="sxs-lookup"><span data-stu-id="7e823-120">**Overview** – This tab shows application data.</span></span>
- <span data-ttu-id="7e823-121">**在庫会計ステータス** – このタブでは、Power BI コンテンツが表示されます。</span><span class="sxs-lookup"><span data-stu-id="7e823-121">**Inventory accounting status** – This tab shows Power BI content.</span></span>
- <span data-ttu-id="7e823-122">**製造会計ステータス** – このタブでは、Power BI コンテンツが表示されます。</span><span class="sxs-lookup"><span data-stu-id="7e823-122">**Manufacturing accounting status** – This tab shows Power BI content.</span></span>

<span data-ttu-id="7e823-123">**コスト分析**ワークスペースには、次のタブが含まれています。</span><span class="sxs-lookup"><span data-stu-id="7e823-123">The **Cost analysis** workspace contains the following tabs:</span></span>

- <span data-ttu-id="7e823-124">**概要** – このタブは、アプリケーション データを表示します。</span><span class="sxs-lookup"><span data-stu-id="7e823-124">**Overview** – This tab shows application data.</span></span>
- <span data-ttu-id="7e823-125">**在庫会計分析** – このタブでは、Power BI コンテンツが表示されます。</span><span class="sxs-lookup"><span data-stu-id="7e823-125">**Inventory accounting analysis** – This tab shows Power BI content.</span></span>
- <span data-ttu-id="7e823-126">**製造会計分析** – このタブでは、Power BI コンテンツが表示されます。</span><span class="sxs-lookup"><span data-stu-id="7e823-126">**Manufacturing accounting analysis** – This tab shows Power BI content.</span></span>
- <span data-ttu-id="7e823-127">**標準原価差異分析** – このタブでは、Power BI コンテンツが表示されます。</span><span class="sxs-lookup"><span data-stu-id="7e823-127">**Std. cost variance analysis** – This tab shows Power BI content.</span></span>

## <a name="report-pages-that-are-included-in-the-power-bi-content"></a><span data-ttu-id="7e823-128">Power BI コンテンツに含まれるレポート ページ</span><span class="sxs-lookup"><span data-stu-id="7e823-128">Report pages that are included in the Power BI content</span></span>

<span data-ttu-id="7e823-129">**原価管理** Power BI コンテンツには、一連のメトリックスで構成されるレポート ページのセットが含まれています。</span><span class="sxs-lookup"><span data-stu-id="7e823-129">The **Cost management** Power BI content includes a set of report pages that consist of a set of metrics.</span></span> <span data-ttu-id="7e823-130">これらのメトリックスはグラフ、タイル、表として視覚化されます。</span><span class="sxs-lookup"><span data-stu-id="7e823-130">These metrics are visualized as charts, tiles, and tables.</span></span> 

<span data-ttu-id="7e823-131">次の表に、**原価管理** Power BI コンテンツの表示の概要を示します。</span><span class="sxs-lookup"><span data-stu-id="7e823-131">The following tables provide an overview of the visualizations in the **Cost management** Power BI content.</span></span>

### <a name="inventory-accounting-status"></a><span data-ttu-id="7e823-132">在庫会計ステータス</span><span class="sxs-lookup"><span data-stu-id="7e823-132">Inventory accounting status</span></span>

| <span data-ttu-id="7e823-133">レポート ページ</span><span class="sxs-lookup"><span data-stu-id="7e823-133">Report page</span></span>                               | <span data-ttu-id="7e823-134">視覚化</span><span class="sxs-lookup"><span data-stu-id="7e823-134">Visualization</span></span>                                   |
|-------------------------------------------|-------------------------------------------------|
| <span data-ttu-id="7e823-135">在庫の概要</span><span class="sxs-lookup"><span data-stu-id="7e823-135">Inventory overview</span></span>                        | <span data-ttu-id="7e823-136">期首残高</span><span class="sxs-lookup"><span data-stu-id="7e823-136">Beginning balance</span></span>                               |
|                                           | <span data-ttu-id="7e823-137">差分変更</span><span class="sxs-lookup"><span data-stu-id="7e823-137">Net change</span></span>                                      |
|                                           | <span data-ttu-id="7e823-138">差分変更 %</span><span class="sxs-lookup"><span data-stu-id="7e823-138">Net change %</span></span>                                    |
|                                           | <span data-ttu-id="7e823-139">期末残高</span><span class="sxs-lookup"><span data-stu-id="7e823-139">Ending balance</span></span>                                  |
|                                           | <span data-ttu-id="7e823-140">在庫の正確性</span><span class="sxs-lookup"><span data-stu-id="7e823-140">Inventory accuracy</span></span>                              |
|                                           | <span data-ttu-id="7e823-141">在庫回転率</span><span class="sxs-lookup"><span data-stu-id="7e823-141">Inventory turnover ratio</span></span>                        |
|                                           | <span data-ttu-id="7e823-142">手持在庫日数</span><span class="sxs-lookup"><span data-stu-id="7e823-142">Days inventory on-hand</span></span>                          |
|                                           | <span data-ttu-id="7e823-143">期間内の有効な製品</span><span class="sxs-lookup"><span data-stu-id="7e823-143">Active product in period</span></span>                        |
|                                           | <span data-ttu-id="7e823-144">期間内の有効な原価オブジェクト</span><span class="sxs-lookup"><span data-stu-id="7e823-144">Active cost objects in period</span></span>                   |
|                                           | <span data-ttu-id="7e823-145">品目グループ別残高</span><span class="sxs-lookup"><span data-stu-id="7e823-145">Balance by item group</span></span>                           |
|                                           | <span data-ttu-id="7e823-146">サイト別の残高</span><span class="sxs-lookup"><span data-stu-id="7e823-146">Balance by site</span></span>                                 |
|                                           | <span data-ttu-id="7e823-147">カテゴリ別の明細書</span><span class="sxs-lookup"><span data-stu-id="7e823-147">Statement by category</span></span>                           |
|                                           | <span data-ttu-id="7e823-148">四半期ごとの差分変更</span><span class="sxs-lookup"><span data-stu-id="7e823-148">Net change by quarter</span></span>                           |
| <span data-ttu-id="7e823-149">サイトおよび品目グループ別在庫の概要</span><span class="sxs-lookup"><span data-stu-id="7e823-149">Inventory overview by site and item group</span></span> | <span data-ttu-id="7e823-150">サイト別の在庫の正確性</span><span class="sxs-lookup"><span data-stu-id="7e823-150">Inventory accuracy by site</span></span>                      |
|                                           | <span data-ttu-id="7e823-151">サイト別の在庫回転率</span><span class="sxs-lookup"><span data-stu-id="7e823-151">Inventory turnover ratio by site</span></span>                |
|                                           | <span data-ttu-id="7e823-152">サイト別の在庫期末残高</span><span class="sxs-lookup"><span data-stu-id="7e823-152">Inventory ending balance by site</span></span>                |
|                                           | <span data-ttu-id="7e823-153">品目グループ別の在庫の正確性</span><span class="sxs-lookup"><span data-stu-id="7e823-153">Inventory accuracy by item group</span></span>                |
|                                           | <span data-ttu-id="7e823-154">品目グループ別の在庫回転率</span><span class="sxs-lookup"><span data-stu-id="7e823-154">Inventory turnover ratio by item group</span></span>          |
|                                           | <span data-ttu-id="7e823-155">サイトおよび品目グループ別の在庫期末残高</span><span class="sxs-lookup"><span data-stu-id="7e823-155">Inventory ending balance by site and item group</span></span> |
| <span data-ttu-id="7e823-156">在庫明細書</span><span class="sxs-lookup"><span data-stu-id="7e823-156">Inventory statement</span></span>                       | <span data-ttu-id="7e823-157">在庫明細書</span><span class="sxs-lookup"><span data-stu-id="7e823-157">Inventory statement</span></span>                             |
| <span data-ttu-id="7e823-158">サイトごとの在庫明細書</span><span class="sxs-lookup"><span data-stu-id="7e823-158">Inventory statement by site</span></span>               | <span data-ttu-id="7e823-159">サイトごとの在庫明細書</span><span class="sxs-lookup"><span data-stu-id="7e823-159">Inventory statement by site</span></span>                     |
| <span data-ttu-id="7e823-160">製品階層別の在庫明細書</span><span class="sxs-lookup"><span data-stu-id="7e823-160">Inventory statement by product hierarchy</span></span>  | <span data-ttu-id="7e823-161">在庫明細書</span><span class="sxs-lookup"><span data-stu-id="7e823-161">Inventory statement</span></span>                             |
| <span data-ttu-id="7e823-162">製品階層別の在庫明細書</span><span class="sxs-lookup"><span data-stu-id="7e823-162">Inventory statement by product hierarchy</span></span>  | <span data-ttu-id="7e823-163">サイトごとの在庫明細書</span><span class="sxs-lookup"><span data-stu-id="7e823-163">Inventory statement by site</span></span>                     |

### <a name="manufacturing-accounting-status"></a><span data-ttu-id="7e823-164">製造会計ステータス</span><span class="sxs-lookup"><span data-stu-id="7e823-164">Manufacturing accounting status</span></span>

| <span data-ttu-id="7e823-165">レポート ページ</span><span class="sxs-lookup"><span data-stu-id="7e823-165">Report page</span></span>                | <span data-ttu-id="7e823-166">視覚化</span><span class="sxs-lookup"><span data-stu-id="7e823-166">Visualization</span></span>                       |
|----------------------------|-------------------------------------|
| <span data-ttu-id="7e823-167">仕掛品の概要 YTD</span><span class="sxs-lookup"><span data-stu-id="7e823-167">WIP overview YTD</span></span>           | <span data-ttu-id="7e823-168">期首残高</span><span class="sxs-lookup"><span data-stu-id="7e823-168">Beginning balance</span></span>                   |
|                            | <span data-ttu-id="7e823-169">差分変更</span><span class="sxs-lookup"><span data-stu-id="7e823-169">Net change</span></span>                          |
|                            | <span data-ttu-id="7e823-170">差分変更 %</span><span class="sxs-lookup"><span data-stu-id="7e823-170">Net change %</span></span>                        |
|                            | <span data-ttu-id="7e823-171">期末残高</span><span class="sxs-lookup"><span data-stu-id="7e823-171">Ending balance</span></span>                      |
|                            | <span data-ttu-id="7e823-172">仕掛品回転資本率</span><span class="sxs-lookup"><span data-stu-id="7e823-172">WIP turnover ratio</span></span>                  |
|                            | <span data-ttu-id="7e823-173">手持仕掛品日数</span><span class="sxs-lookup"><span data-stu-id="7e823-173">Days WIP on-hand</span></span>                    |
|                            | <span data-ttu-id="7e823-174">期間内の有効な原価オブジェクト</span><span class="sxs-lookup"><span data-stu-id="7e823-174">Active cost object in period</span></span>        |
|                            | <span data-ttu-id="7e823-175">リソース グループ別の差分変更</span><span class="sxs-lookup"><span data-stu-id="7e823-175">Net change by resource group</span></span>        |
|                            | <span data-ttu-id="7e823-176">サイト別の残高</span><span class="sxs-lookup"><span data-stu-id="7e823-176">Balance by site</span></span>                     |
|                            | <span data-ttu-id="7e823-177">カテゴリ別の明細書</span><span class="sxs-lookup"><span data-stu-id="7e823-177">Statement by category</span></span>               |
|                            | <span data-ttu-id="7e823-178">四半期ごとの差分変更</span><span class="sxs-lookup"><span data-stu-id="7e823-178">Net change by quarter</span></span>               |
| <span data-ttu-id="7e823-179">仕掛報告書</span><span class="sxs-lookup"><span data-stu-id="7e823-179">WIP statement</span></span>              | <span data-ttu-id="7e823-180">期首残高</span><span class="sxs-lookup"><span data-stu-id="7e823-180">Beginning balance</span></span>                   |
|                            | <span data-ttu-id="7e823-181">期末残高</span><span class="sxs-lookup"><span data-stu-id="7e823-181">Ending balance</span></span>                      |
|                            | <span data-ttu-id="7e823-182">カテゴリ別の仕掛品明細書</span><span class="sxs-lookup"><span data-stu-id="7e823-182">WIP statement by category</span></span>           |
| <span data-ttu-id="7e823-183">サイト別の仕掛品明細書</span><span class="sxs-lookup"><span data-stu-id="7e823-183">WIP statement by site</span></span>      | <span data-ttu-id="7e823-184">期首残高</span><span class="sxs-lookup"><span data-stu-id="7e823-184">Beginning balance</span></span>                   |
|                            | <span data-ttu-id="7e823-185">期末残高</span><span class="sxs-lookup"><span data-stu-id="7e823-185">Ending balance</span></span>                      |
|                            | <span data-ttu-id="7e823-186">カテゴリおよびサイト別の仕掛品明細書</span><span class="sxs-lookup"><span data-stu-id="7e823-186">WIP statement by category and site</span></span>  |
| <span data-ttu-id="7e823-187">カテゴリ階層別の仕掛品明細書</span><span class="sxs-lookup"><span data-stu-id="7e823-187">WIP statement by hierarchy</span></span> | <span data-ttu-id="7e823-188">期首残高</span><span class="sxs-lookup"><span data-stu-id="7e823-188">Beginning balance</span></span>                   |
|                            | <span data-ttu-id="7e823-189">期末残高</span><span class="sxs-lookup"><span data-stu-id="7e823-189">Ending balance</span></span>                      |
|                            | <span data-ttu-id="7e823-190">カテゴリ階層別の仕掛品明細書</span><span class="sxs-lookup"><span data-stu-id="7e823-190">WIP statement by category hierarchy</span></span> |

### <a name="inventory-accounting-analysis"></a><span data-ttu-id="7e823-191">在庫会計分析</span><span class="sxs-lookup"><span data-stu-id="7e823-191">Inventory accounting analysis</span></span>

| <span data-ttu-id="7e823-192">レポート ページ</span><span class="sxs-lookup"><span data-stu-id="7e823-192">Report page</span></span>        | <span data-ttu-id="7e823-193">視覚化</span><span class="sxs-lookup"><span data-stu-id="7e823-193">Visualization</span></span>                                                                |
|--------------------|------------------------------------------------------------------------------|
| <span data-ttu-id="7e823-194">在庫の詳細</span><span class="sxs-lookup"><span data-stu-id="7e823-194">Inventory details</span></span>  | <span data-ttu-id="7e823-195">期末残高別の上位 10 リソース</span><span class="sxs-lookup"><span data-stu-id="7e823-195">Top 10 resources by ending balance</span></span>                                           |
|                    | <span data-ttu-id="7e823-196">差分変更増加別の上位 10 リソース</span><span class="sxs-lookup"><span data-stu-id="7e823-196">Top 10 resources by net change increase</span></span>                                      |
|                    | <span data-ttu-id="7e823-197">差分変更減少別の上位 10 リソース</span><span class="sxs-lookup"><span data-stu-id="7e823-197">Top 10 resources by net change decrease</span></span>                                      |
|                    | <span data-ttu-id="7e823-198">在庫回転率別の上位 10 リソース</span><span class="sxs-lookup"><span data-stu-id="7e823-198">Top 10 resources by inventory turnover ratio</span></span>                                 |
|                    | <span data-ttu-id="7e823-199">低在庫回転率と期末残高がしきい値以上のリソース</span><span class="sxs-lookup"><span data-stu-id="7e823-199">Resources by low inventory turnover ratio and ending balance above threshold</span></span> |
|                    | <span data-ttu-id="7e823-200">低精度の上位 10 リソース</span><span class="sxs-lookup"><span data-stu-id="7e823-200">Top 10 resources by low accuracy</span></span>                                             |
| <span data-ttu-id="7e823-201">ABC 分類</span><span class="sxs-lookup"><span data-stu-id="7e823-201">ABC classification</span></span> | <span data-ttu-id="7e823-202">在庫期末残高</span><span class="sxs-lookup"><span data-stu-id="7e823-202">Inventory ending balance</span></span>                                                     |
|                    | <span data-ttu-id="7e823-203">消費された材料</span><span class="sxs-lookup"><span data-stu-id="7e823-203">Consumed material</span></span>                                                            |
|                    | <span data-ttu-id="7e823-204">売却 (COGS)</span><span class="sxs-lookup"><span data-stu-id="7e823-204">Sold (COGS)</span></span>                                                                  |
| <span data-ttu-id="7e823-205">在庫のトレンド</span><span class="sxs-lookup"><span data-stu-id="7e823-205">Inventory trends</span></span>   | <span data-ttu-id="7e823-206">在庫期末残高</span><span class="sxs-lookup"><span data-stu-id="7e823-206">Inventory ending balance</span></span>                                                     |
|                    | <span data-ttu-id="7e823-207">在庫差分変更</span><span class="sxs-lookup"><span data-stu-id="7e823-207">Inventory net change</span></span>                                                         |
|                    | <span data-ttu-id="7e823-208">在庫回転率</span><span class="sxs-lookup"><span data-stu-id="7e823-208">Inventory turnover ratio</span></span>                                                     |
|                    | <span data-ttu-id="7e823-209">在庫の正確性</span><span class="sxs-lookup"><span data-stu-id="7e823-209">Inventory accuracy</span></span>                                                           |

### <a name="manufacturing-accounting-analysis"></a><span data-ttu-id="7e823-210">製造会計分析</span><span class="sxs-lookup"><span data-stu-id="7e823-210">Manufacturing accounting analysis</span></span>

| <span data-ttu-id="7e823-211">レポート ページ</span><span class="sxs-lookup"><span data-stu-id="7e823-211">Report page</span></span> | <span data-ttu-id="7e823-212">視覚化</span><span class="sxs-lookup"><span data-stu-id="7e823-212">Visualization</span></span>      |
|-------------|--------------------|
| <span data-ttu-id="7e823-213">仕掛品のトレンド</span><span class="sxs-lookup"><span data-stu-id="7e823-213">WIP trends</span></span>  | <span data-ttu-id="7e823-214">仕掛品期末残高</span><span class="sxs-lookup"><span data-stu-id="7e823-214">WIP ending balance</span></span> |
|             | <span data-ttu-id="7e823-215">仕掛品差分変更</span><span class="sxs-lookup"><span data-stu-id="7e823-215">WIP net change</span></span>     |
|             | <span data-ttu-id="7e823-216">仕掛品回転資本率</span><span class="sxs-lookup"><span data-stu-id="7e823-216">WIP turnover ratio</span></span> |

### <a name="std-cost-variance-analysis"></a><span data-ttu-id="7e823-217">標準原価差異分析</span><span class="sxs-lookup"><span data-stu-id="7e823-217">Std. cost variance analysis</span></span>

| <span data-ttu-id="7e823-218">レポート ページ</span><span class="sxs-lookup"><span data-stu-id="7e823-218">Report page</span></span>                             | <span data-ttu-id="7e823-219">視覚化</span><span class="sxs-lookup"><span data-stu-id="7e823-219">Visualization</span></span>                                        |
|-----------------------------------------|------------------------------------------------------|
| <span data-ttu-id="7e823-220">購買価格差異 (標準原価) YTD</span><span class="sxs-lookup"><span data-stu-id="7e823-220">Purchase price variance (Std. cost) YTD</span></span> | <span data-ttu-id="7e823-221">調達済み残高</span><span class="sxs-lookup"><span data-stu-id="7e823-221">Procured balance</span></span>                                     |
|                                         | <span data-ttu-id="7e823-222">購買価格差異</span><span class="sxs-lookup"><span data-stu-id="7e823-222">Purchase price variance</span></span>                              |
|                                         | <span data-ttu-id="7e823-223">購買価格差異比率</span><span class="sxs-lookup"><span data-stu-id="7e823-223">Purchase price variance ratio</span></span>                        |
|                                         | <span data-ttu-id="7e823-224">品目グループ別の差異</span><span class="sxs-lookup"><span data-stu-id="7e823-224">Variance by item group</span></span>                               |
|                                         | <span data-ttu-id="7e823-225">サイト別の差異</span><span class="sxs-lookup"><span data-stu-id="7e823-225">Variance by site</span></span>                                     |
|                                         | <span data-ttu-id="7e823-226">四半期ごとの購買価格</span><span class="sxs-lookup"><span data-stu-id="7e823-226">Purchase price by quarter</span></span>                            |
|                                         | <span data-ttu-id="7e823-227">四半期および品目グループごとの購買価格</span><span class="sxs-lookup"><span data-stu-id="7e823-227">Purchase price by quarter and Item group</span></span>             |
|                                         | <span data-ttu-id="7e823-228">好ましくない購買価格比率の上位 10 リソース</span><span class="sxs-lookup"><span data-stu-id="7e823-228">Top 10 resources by unfavorable purchase price ratio</span></span> |
|                                         | <span data-ttu-id="7e823-229">有利な購買価格比率の上位 10 リソース</span><span class="sxs-lookup"><span data-stu-id="7e823-229">Top 10 resources by favorable purchase price ratio</span></span>   |
| <span data-ttu-id="7e823-230">製造差異 (標準原価) YTD</span><span class="sxs-lookup"><span data-stu-id="7e823-230">Production variance (Std. cost) YTD</span></span>     | <span data-ttu-id="7e823-231">製造原価</span><span class="sxs-lookup"><span data-stu-id="7e823-231">Manufactured cost</span></span>                                    |
|                                         | <span data-ttu-id="7e823-232">製造差異</span><span class="sxs-lookup"><span data-stu-id="7e823-232">Production variance</span></span>                                  |
|                                         | <span data-ttu-id="7e823-233">製造差異比率</span><span class="sxs-lookup"><span data-stu-id="7e823-233">Production variance ratio</span></span>                            |
|                                         | <span data-ttu-id="7e823-234">品目グループ別の差異</span><span class="sxs-lookup"><span data-stu-id="7e823-234">Variance by item group</span></span>                               |
|                                         | <span data-ttu-id="7e823-235">サイト別の差異</span><span class="sxs-lookup"><span data-stu-id="7e823-235">Variance by site</span></span>                                     |
|                                         | <span data-ttu-id="7e823-236">四半期ごとの製造差異</span><span class="sxs-lookup"><span data-stu-id="7e823-236">Production variance by quarter</span></span>                       |
|                                         | <span data-ttu-id="7e823-237">四半期および差異タイプによる製造差異</span><span class="sxs-lookup"><span data-stu-id="7e823-237">Production variance by quarter and variance type</span></span>     |
|                                         | <span data-ttu-id="7e823-238">好ましくない製造差異の上位 10 リソース</span><span class="sxs-lookup"><span data-stu-id="7e823-238">Top 10 resources by unfavorable production variance</span></span>  |
|                                         | <span data-ttu-id="7e823-239">有利な製造差異の上位 10 リソース</span><span class="sxs-lookup"><span data-stu-id="7e823-239">Top 10 resources by favorable production variance</span></span>    |

### <a name="understanding-the-data-model-and-entities"></a><span data-ttu-id="7e823-240">データ モデルおよびエンティティの理解</span><span class="sxs-lookup"><span data-stu-id="7e823-240">Understanding the data model and entities</span></span>

<span data-ttu-id="7e823-241">Microsoft Dynamics 365 for Finance and Operations からのデータは、**原価管理** Power BI コンテンツのレポート ページを入力するために使用されます。</span><span class="sxs-lookup"><span data-stu-id="7e823-241">Data from Microsoft Dynamics 365 for Finance and Operations is used to fill the report pages in the **Cost management** Power BI content.</span></span> <span data-ttu-id="7e823-242">このデータは、分析用に最適化された Microsoft SQL Server データベースであるエンティティ格納でステージ完了である集計の測定として表されます。</span><span class="sxs-lookup"><span data-stu-id="7e823-242">This data is represented as aggregate measurements that are staged in the entity store, which is a Microsoft SQL Server database that is optimized for analytics.</span></span> <span data-ttu-id="7e823-243">詳細については、[エンティティ ストアとの Power BI の統合](power-bi-integration-entity-store.md) を参照してください。</span><span class="sxs-lookup"><span data-stu-id="7e823-243">For more information, see [Power BI integration with entity store](power-bi-integration-entity-store.md).</span></span>

<span data-ttu-id="7e823-244">次のオブジェクトのキー集計の測定は、Power BI コンテンツの基準として使用されます。</span><span class="sxs-lookup"><span data-stu-id="7e823-244">The key aggregate measurements of the following objects are used as the basis of the Power BI content.</span></span>

| <span data-ttu-id="7e823-245">オブジェクト</span><span class="sxs-lookup"><span data-stu-id="7e823-245">Object</span></span>                          | <span data-ttu-id="7e823-246">キー集計の測定</span><span class="sxs-lookup"><span data-stu-id="7e823-246">Key aggregate measurements</span></span> | <span data-ttu-id="7e823-247">Finance and Operations のデータ ソース</span><span class="sxs-lookup"><span data-stu-id="7e823-247">Data source for Finance and Operations</span></span> | <span data-ttu-id="7e823-248">フィールド</span><span class="sxs-lookup"><span data-stu-id="7e823-248">Field</span></span>               |
|---------------------------------|----------------------------|----------------------------------------|---------------------|
| <span data-ttu-id="7e823-249">CostObjectStatementCacheMonthly</span><span class="sxs-lookup"><span data-stu-id="7e823-249">CostObjectStatementCacheMonthly</span></span> | <span data-ttu-id="7e823-250">量</span><span class="sxs-lookup"><span data-stu-id="7e823-250">Amount</span></span>                     | <span data-ttu-id="7e823-251">CostObjectStatementCache</span><span class="sxs-lookup"><span data-stu-id="7e823-251">CostObjectStatementCache</span></span>               | <span data-ttu-id="7e823-252">量</span><span class="sxs-lookup"><span data-stu-id="7e823-252">Amount</span></span>              |
| <span data-ttu-id="7e823-253">CostObjectStatementCacheMonthly</span><span class="sxs-lookup"><span data-stu-id="7e823-253">CostObjectStatementCacheMonthly</span></span> | <span data-ttu-id="7e823-254">件数</span><span class="sxs-lookup"><span data-stu-id="7e823-254">Quantity</span></span>                   | <span data-ttu-id="7e823-255">CostObjectStatementCache</span><span class="sxs-lookup"><span data-stu-id="7e823-255">CostObjectStatementCache</span></span>               | <span data-ttu-id="7e823-256">数量</span><span class="sxs-lookup"><span data-stu-id="7e823-256">Qty</span></span>                 |
| <span data-ttu-id="7e823-257">CostInventoryAccountingKPIGoal</span><span class="sxs-lookup"><span data-stu-id="7e823-257">CostInventoryAccountingKPIGoal</span></span>  | <span data-ttu-id="7e823-258">AnnualInventoryTurn</span><span class="sxs-lookup"><span data-stu-id="7e823-258">AnnualInventoryTurn</span></span>        | <span data-ttu-id="7e823-259">CostInventoryAccountingKPIGoal</span><span class="sxs-lookup"><span data-stu-id="7e823-259">CostInventoryAccountingKPIGoal</span></span>         | <span data-ttu-id="7e823-260">AnnualInventoryTurn</span><span class="sxs-lookup"><span data-stu-id="7e823-260">AnnualInventoryTurn</span></span> |
| <span data-ttu-id="7e823-261">CostInventoryAccountingKPIGoal</span><span class="sxs-lookup"><span data-stu-id="7e823-261">CostInventoryAccountingKPIGoal</span></span>  | <span data-ttu-id="7e823-262">InventoryAccuracy</span><span class="sxs-lookup"><span data-stu-id="7e823-262">InventoryAccuracy</span></span>          | <span data-ttu-id="7e823-263">CostInventoryAccountingKPIGoal</span><span class="sxs-lookup"><span data-stu-id="7e823-263">CostInventoryAccountingKPIGoal</span></span>         | <span data-ttu-id="7e823-264">InventoryAccuracy</span><span class="sxs-lookup"><span data-stu-id="7e823-264">InventoryAccuracy</span></span>   |

<span data-ttu-id="7e823-265">次の表は、Power BI コンテンツでキー計算された測定値を示しています。</span><span class="sxs-lookup"><span data-stu-id="7e823-265">The following table shows the key calculated measurements in the Power BI content.</span></span>

| <span data-ttu-id="7e823-266">基準</span><span class="sxs-lookup"><span data-stu-id="7e823-266">Measure</span></span>                            | <span data-ttu-id="7e823-267">計算</span><span class="sxs-lookup"><span data-stu-id="7e823-267">Calculation</span></span> |
|------------------------------------|-------------|
| <span data-ttu-id="7e823-268">期首残高</span><span class="sxs-lookup"><span data-stu-id="7e823-268">Beginning balance</span></span>                  | <span data-ttu-id="7e823-269">期首残高 = [期末残高]-[差分変更]</span><span class="sxs-lookup"><span data-stu-id="7e823-269">Beginning balance = [Ending balance]-[Net change]</span></span> |
| <span data-ttu-id="7e823-270">期首残高数量</span><span class="sxs-lookup"><span data-stu-id="7e823-270">Beginning balance qty.</span></span>             | <span data-ttu-id="7e823-271">期首残高数量 = [期末残高数量]-[差分変更数量]</span><span class="sxs-lookup"><span data-stu-id="7e823-271">Beginning balance qty. = [Ending balance qty.]-[Net change qty.]</span></span> |
| <span data-ttu-id="7e823-272">期末残高</span><span class="sxs-lookup"><span data-stu-id="7e823-272">Ending balance</span></span>                     | <span data-ttu-id="7e823-273">期末残高 = (CALCULATE(SUM([Amount]), FILTER(ALL(FiscalCalendar) ,FiscalCalendar[MONTHSTARTDATE] \<= MAX(FiscalCalendar[MONTHSTARTDATE]))))</span><span class="sxs-lookup"><span data-stu-id="7e823-273">Ending balance = (CALCULATE(SUM([Amount]), FILTER(ALL(FiscalCalendar) ,FiscalCalendar[MONTHSTARTDATE] \<= MAX(FiscalCalendar[MONTHSTARTDATE]))))</span></span> |
| <span data-ttu-id="7e823-274">期末残高数量</span><span class="sxs-lookup"><span data-stu-id="7e823-274">Ending balance qty.</span></span>                | <span data-ttu-id="7e823-275">期末残高数量 = CALCULATE(SUM([QTY]), FILTER(ALL(FiscalCalendar),FiscalCalendar[MONTHSTARTDATE] \<= MAX(FiscalCalendar[MONTHSTARTDATE])))</span><span class="sxs-lookup"><span data-stu-id="7e823-275">Ending balance qty. = CALCULATE(SUM([QTY]), FILTER(ALL(FiscalCalendar),FiscalCalendar[MONTHSTARTDATE] \<= MAX(FiscalCalendar[MONTHSTARTDATE])))</span></span> |
| <span data-ttu-id="7e823-276">差分変更</span><span class="sxs-lookup"><span data-stu-id="7e823-276">Net change</span></span>                         | <span data-ttu-id="7e823-277">差分変更 = SUM([AMOUNT])</span><span class="sxs-lookup"><span data-stu-id="7e823-277">Net change = SUM([AMOUNT])</span></span> |
| <span data-ttu-id="7e823-278">差分変更数量</span><span class="sxs-lookup"><span data-stu-id="7e823-278">Net change qty.</span></span>                    | <span data-ttu-id="7e823-279">差分変更数量 = SUM([QTY])</span><span class="sxs-lookup"><span data-stu-id="7e823-279">Net change qty. = SUM([QTY])</span></span> |
| <span data-ttu-id="7e823-280">金額別の在庫回転率</span><span class="sxs-lookup"><span data-stu-id="7e823-280">Inventory turnover ratio by amount</span></span> | <span data-ttu-id="7e823-281">金額別の在庫回転率 = if(OR([在庫平均残高] \<= 0, [販売在庫または消費の払出] \>= 0), 0, ABS([販売在庫または消費の払出])/[在庫平均残高])</span><span class="sxs-lookup"><span data-stu-id="7e823-281">Inventory turnover ratio by amount = if(OR([Inventory average balance] \<= 0, [Inventory sold or consumed issues] \>= 0), 0, ABS([Inventory sold or consumed issues])/[Inventory average balance])</span></span> |
| <span data-ttu-id="7e823-282">在庫平均残高</span><span class="sxs-lookup"><span data-stu-id="7e823-282">Inventory average balance</span></span>          | <span data-ttu-id="7e823-283">I在庫平均残高 = (([期末残高] + [期首残高]) / 2)</span><span class="sxs-lookup"><span data-stu-id="7e823-283">Inventory average balance = (([Ending balance] + [Beginning balance]) / 2)</span></span> |
| <span data-ttu-id="7e823-284">手持在庫日数</span><span class="sxs-lookup"><span data-stu-id="7e823-284">Days inventory on-hand</span></span>             | <span data-ttu-id="7e823-285">手持在庫日数 = 365 / CostObjectStatementEntries[金額別の在庫回転率]</span><span class="sxs-lookup"><span data-stu-id="7e823-285">Days inventory onhand = 365 / CostObjectStatementEntries[Inventory turnover ratio by amount]</span></span> |
| <span data-ttu-id="7e823-286">在庫の正確性</span><span class="sxs-lookup"><span data-stu-id="7e823-286">Inventory accuracy</span></span>                 | <span data-ttu-id="7e823-287">金額ごとの在庫の正確性 = IF([期末残高] \<= 0, IF(OR([在庫棚卸金額] \<\> 0, [期末残高] \< 0), 0, 1), MAX(0, ([期末残高] - ABS([在庫棚卸金額]))/[期末残高]))</span><span class="sxs-lookup"><span data-stu-id="7e823-287">Inventory accuracy by amount = IF([Ending balance] \<= 0, IF(OR([Inventory counted amount] \<\> 0, [Ending balance] \< 0), 0, 1), MAX(0, ([Ending balance] - ABS([Inventory counted amount]))/[Ending balance]))</span></span> |

<span data-ttu-id="7e823-288">以下のキー分析コードは、より高い粒度を達成し深い分析洞察を取得できるように、集計の測定をスライスするフィルターとして使用されます。</span><span class="sxs-lookup"><span data-stu-id="7e823-288">The following key dimensions are used as filters to slice the aggregate measurements, so that you can achieve greater granularity and gain deeper analytical insights.</span></span>


|                         <span data-ttu-id="7e823-289">エンティティ</span><span class="sxs-lookup"><span data-stu-id="7e823-289">Entity</span></span>                          |             <span data-ttu-id="7e823-290">属性の例</span><span class="sxs-lookup"><span data-stu-id="7e823-290">Examples of attributes</span></span>              |
|---------------------------------------------------------|-------------------------------------------------|
|                        <span data-ttu-id="7e823-291">製品</span><span class="sxs-lookup"><span data-stu-id="7e823-291">Products</span></span>                         | <span data-ttu-id="7e823-292">製品番号、製品名、単位、品目グループ</span><span class="sxs-lookup"><span data-stu-id="7e823-292">Product number, Product name, Unit, Item groups</span></span> |
| <span data-ttu-id="7e823-293">カテゴリ階層 (原価管理のロールに割り当て)</span><span class="sxs-lookup"><span data-stu-id="7e823-293">Category hierarchies (Assigned to role Cost management)</span></span> |       <span data-ttu-id="7e823-294">カテゴリ階層、カテゴリ レベル</span><span class="sxs-lookup"><span data-stu-id="7e823-294">Category hierarchy, Category level</span></span>        |
|                     <span data-ttu-id="7e823-295">法人</span><span class="sxs-lookup"><span data-stu-id="7e823-295">Legal entities</span></span>                      |               <span data-ttu-id="7e823-296">法人名</span><span class="sxs-lookup"><span data-stu-id="7e823-296">Legal entity names</span></span>                |
|                    <span data-ttu-id="7e823-297">会計カレンダー</span><span class="sxs-lookup"><span data-stu-id="7e823-297">Fiscal calendars</span></span>                     |  <span data-ttu-id="7e823-298">会計カレンダー、年、四半期、期間、月</span><span class="sxs-lookup"><span data-stu-id="7e823-298">Fiscal calendar, Year, Quarter, Period, Month</span></span>  |
|                          <span data-ttu-id="7e823-299">サイト</span><span class="sxs-lookup"><span data-stu-id="7e823-299">Site</span></span>                           |        <span data-ttu-id="7e823-300">ID、名前、住所、都道府県、国</span><span class="sxs-lookup"><span data-stu-id="7e823-300">ID, Name, Address, State, Country</span></span>        |


