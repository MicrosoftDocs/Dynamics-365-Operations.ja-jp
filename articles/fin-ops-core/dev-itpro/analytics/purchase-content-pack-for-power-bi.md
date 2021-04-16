---
title: 購買支出の分析 Power BI コンテンツ
description: このトピックでは、購買支出の分析 Power BI コンテンツの内容について説明します。
author: FrankDahl
ms.date: 04/24/2019
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: PurchaseSpendAnalysisPowerBI
audience: Application User, IT Pro
ms.reviewer: kfend
ms.custom: 265434
ms.assetid: 3cd9dfce-2687-4303-bc78-349e7cb5ea75
ms.search.region: global
ms.author: fdahl
ms.search.validFrom: 2016-11-30
ms.dyn365.ops.version: Version 1611
ms.openlocfilehash: f9741b5f30f5e62b9e80000953113377fe016253
ms.sourcegitcommit: 074b6e212d19dd5d84881d1cdd096611a18c207f
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 03/31/2021
ms.locfileid: "5749372"
---
# <a name="purchase-spend-analysis-power-bi-content"></a><span data-ttu-id="54add-103">購買支出の分析 Power BI コンテンツ</span><span class="sxs-lookup"><span data-stu-id="54add-103">Purchase spend analysis Power BI content</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="54add-104">このトピックでは、**購買支出の分析** Microsoft Power BI コンテンツの内容について説明します。</span><span class="sxs-lookup"><span data-stu-id="54add-104">This topic describes what is included in the **Purchase spend analysis** Microsoft Power BI content.</span></span> <span data-ttu-id="54add-105">Power BI レポートにアクセスする方法を説明し、コンテンツを作成するために使用するデータ モデルおよびエンティティについての情報を提供します。</span><span class="sxs-lookup"><span data-stu-id="54add-105">It explains how to access the Power BI reports, and provides information about the data model and entities that are used to build the content.</span></span>

## <a name="overview"></a><span data-ttu-id="54add-106">概要</span><span class="sxs-lookup"><span data-stu-id="54add-106">Overview</span></span>

<span data-ttu-id="54add-107">**購買支出の分析** Power BI コンテンツは、予算を担当する購買部門のマネージャーおよびマネージャーが購買支出を追跡できるように設計されています。</span><span class="sxs-lookup"><span data-stu-id="54add-107">The **Purchase spend analysis** Power BI content was designed to help purchasing managers and managers who are responsible for budgets keep track of purchase spending.</span></span> <span data-ttu-id="54add-108">マネージャーは、以下の方法で購買支出を分析できます:</span><span class="sxs-lookup"><span data-stu-id="54add-108">Managers can analyze purchase spending in the following ways:</span></span>

- <span data-ttu-id="54add-109">会計年度の購買 (仕入先グループと個々の仕入先、調達カテゴリと個々の製品、仕入先の場所)</span><span class="sxs-lookup"><span data-stu-id="54add-109">Year-to-date purchase (by vendor group and individual vendors, procurement category and individual products, and vendor location)</span></span>
- <span data-ttu-id="54add-110">前年比購買の変化 (仕入先グループと調達カテゴリ)</span><span class="sxs-lookup"><span data-stu-id="54add-110">Year-over-year purchase change (by vendor group and procurement category)</span></span>

<span data-ttu-id="54add-111">コンテンツは購買トランザクション データを使用して、会社全体の購買数の集計ビュー、仕入先および製品の購買先支出の内訳の両方を提供します。</span><span class="sxs-lookup"><span data-stu-id="54add-111">The content uses purchase transactional data, and provides both an aggregate view of the company-wide purchase figures and a breakdown of purchase spending by vendor and product.</span></span> <span data-ttu-id="54add-112">レポートでは時間経過に伴う購買支出の変化が強調表示されています。</span><span class="sxs-lookup"><span data-stu-id="54add-112">Reports highlight changes in purchase spending over time.</span></span> <span data-ttu-id="54add-113">そのため、このレポートは、個々の仕入先や製品の積極的および消極的な支出動向を管理者に警告するために使用することができます。</span><span class="sxs-lookup"><span data-stu-id="54add-113">Therefore, the reports can be used to alert managers about positive and negative spending trends for individual vendors and products.</span></span> <span data-ttu-id="54add-114">また、チャートは、様々な調達カテゴリおよび仕入先グループの購買支出を示します。</span><span class="sxs-lookup"><span data-stu-id="54add-114">Additionally, charts show purchase spending for different procurement categories and vendor groups.</span></span> <span data-ttu-id="54add-115">それゆえ、カテゴリおよび地域マネージャーは、チャートを使用して支出行動の変化を識別することができます。</span><span class="sxs-lookup"><span data-stu-id="54add-115">Therefore, category and regional managers can use the charts to help identify changes in spending behavior.</span></span>

## <a name="accessing-the-power-bi-content"></a><span data-ttu-id="54add-116">Power BI コンテンツへのアクセス</span><span class="sxs-lookup"><span data-stu-id="54add-116">Accessing the Power BI content</span></span>
<span data-ttu-id="54add-117">**購買支出の分析** Power BI コンテンツは **購買支出の分析** ページ (**調達** \> **照会およびレポート** \> **購買パフォーマンスの分析** \> **購買支出の分析**) に表示されます。</span><span class="sxs-lookup"><span data-stu-id="54add-117">The **Purchase spend analysis** Power BI content is shown on the **Purchase and spend analysis** page (**Procurement and sourcing** \> **Inquiries and reports** \> **Purchase performance analysis** \> **Purchase and spend analysis**).</span></span>

## <a name="metrics-that-are-included-in-the-power-bi-content"></a><span data-ttu-id="54add-118">Power BI コンテンツに含まれるメトリックス</span><span class="sxs-lookup"><span data-stu-id="54add-118">Metrics that are included in the Power BI content</span></span>
<span data-ttu-id="54add-119">**購買支出の分析** Power BI コンテンツには、一連のメトリックスで構成されるレポートが含まれます。</span><span class="sxs-lookup"><span data-stu-id="54add-119">The **Purchase spend analysis** Power BI content includes a report that consists of a set of metrics.</span></span> <span data-ttu-id="54add-120">これらのメトリックスはグラフ、タイル、表として視覚化されます。</span><span class="sxs-lookup"><span data-stu-id="54add-120">These metrics are visualized as charts, tiles, and tables.</span></span> 

<span data-ttu-id="54add-121">次の表は、視覚化の概要を示しています。</span><span class="sxs-lookup"><span data-stu-id="54add-121">The following sections provide an overview of the visualizations.</span></span>

### <a name="purchase-by-vendor-report-page"></a><span data-ttu-id="54add-122">仕入先別購入レポートページ</span><span class="sxs-lookup"><span data-stu-id="54add-122">Purchase by vendor report page</span></span>
<span data-ttu-id="54add-123">**グラフ**</span><span class="sxs-lookup"><span data-stu-id="54add-123">**Charts**</span></span>
- <span data-ttu-id="54add-124">購買別トップ 10 の仕入先 (積み上げ棒グラフ)</span><span class="sxs-lookup"><span data-stu-id="54add-124">Top 10 vendors by purchase (stacked bar chart)</span></span>
- <span data-ttu-id="54add-125">仕入先グループ、国、名前別購買合計 (円グラフ)</span><span class="sxs-lookup"><span data-stu-id="54add-125">Total purchase by vendor group / country / name (pie chart)</span></span>
- <span data-ttu-id="54add-126">仕入先グループ、国、名前別購買 (円柱グラフ)</span><span class="sxs-lookup"><span data-stu-id="54add-126">Purchase by vendor group / country / name (column chart)</span></span>
- <span data-ttu-id="54add-127">仕入先グループ、国、名前別平均購買 (円柱グラフ)</span><span class="sxs-lookup"><span data-stu-id="54add-127">Average purchase by vendor group / country / name (column chart)</span></span>

<span data-ttu-id="54add-128">**タイル**</span><span class="sxs-lookup"><span data-stu-id="54add-128">**Tiles**</span></span>
- <span data-ttu-id="54add-129">購買の合計</span><span class="sxs-lookup"><span data-stu-id="54add-129">Total purchase</span></span>
- <span data-ttu-id="54add-130">前年比購買成長</span><span class="sxs-lookup"><span data-stu-id="54add-130">YOY purchase growth</span></span>
- <span data-ttu-id="54add-131">合計仕入先数</span><span class="sxs-lookup"><span data-stu-id="54add-131">Total # vendors</span></span>
- <span data-ttu-id="54add-132">有効な仕入先合計数</span><span class="sxs-lookup"><span data-stu-id="54add-132">Total # of active vendors</span></span>

<span data-ttu-id="54add-133">**例**</span><span class="sxs-lookup"><span data-stu-id="54add-133">**Example**</span></span>
<img src="media/spend1.png" alt="Purchase by vendor">

### <a name="purchase-by-product-report-page"></a><span data-ttu-id="54add-134">製品別購買レポートページ</span><span class="sxs-lookup"><span data-stu-id="54add-134">Purchase by product report page</span></span>

<span data-ttu-id="54add-135">**グラフ**</span><span class="sxs-lookup"><span data-stu-id="54add-135">**Charts**</span></span>
- <span data-ttu-id="54add-136">調達カテゴリまたは製品名別購買 (円柱グラフ)</span><span class="sxs-lookup"><span data-stu-id="54add-136">Purchase by procurement category / product name (column chart)</span></span>
- <span data-ttu-id="54add-137">調達カテゴリまたは製品名 (円グラフ) 別購買合計</span><span class="sxs-lookup"><span data-stu-id="54add-137">Total purchase by procurement category / product name (pie chart)</span></span>
- <span data-ttu-id="54add-138">購買別トップ 10 製品 (積み上げ棒グラフ)</span><span class="sxs-lookup"><span data-stu-id="54add-138">Top 10 products by purchase (stacked bar chart)</span></span>

<span data-ttu-id="54add-139">**タイル**</span><span class="sxs-lookup"><span data-stu-id="54add-139">**Tiles**</span></span>
- <span data-ttu-id="54add-140">製品の合計数</span><span class="sxs-lookup"><span data-stu-id="54add-140">Total # of products</span></span></li>
- <span data-ttu-id="54add-141">製品合計数の有効な製品の合計割合</span><span class="sxs-lookup"><span data-stu-id="54add-141">Total active products percentage of total # of products</span></span>
- <span data-ttu-id="54add-142">購買の 80% を占める製品の数</span><span class="sxs-lookup"><span data-stu-id="54add-142">Number of products accounting for 80% purchase</span></span>

<span data-ttu-id="54add-143">**例**</span><span class="sxs-lookup"><span data-stu-id="54add-143">**Example**</span></span>


<img src="media/purchaseByProduct.png" alt="Purchase by Product">

### <a name="purchase-by-period-report-page"></a><span data-ttu-id="54add-144">期間別購買レポートページ</span><span class="sxs-lookup"><span data-stu-id="54add-144">Purchase by period report page</span></span>
<span data-ttu-id="54add-145">このページでは、今年度と昨年度の購買、および調達カテゴリによる成長が表示されます。</span><span class="sxs-lookup"><span data-stu-id="54add-145">This page shows purchases this year and last year, and growth by procurement category.</span></span>

<span data-ttu-id="54add-146">**グラフ**</span><span class="sxs-lookup"><span data-stu-id="54add-146">**Charts**</span></span> 
- <span data-ttu-id="54add-147">月/日別の購買 (円柱グラフ)</span><span class="sxs-lookup"><span data-stu-id="54add-147">Purchase by month / day (column chart)</span></span>
- <span data-ttu-id="54add-148">累計購買金額の前年比差異 (伝播)</span><span class="sxs-lookup"><span data-stu-id="54add-148">Cumulative purchase YOY variance (waterfall chart)</span></span>
- <span data-ttu-id="54add-149">合計購買金額の前年比成長 (円柱グラフ)</span><span class="sxs-lookup"><span data-stu-id="54add-149">Total purchase YOY growth (column chart)</span></span>
- <span data-ttu-id="54add-150">調達明細書 (マトリックス)</span><span class="sxs-lookup"><span data-stu-id="54add-150">Procurement statement (matrix)</span></span>

<span data-ttu-id="54add-151">**タイル**</span><span class="sxs-lookup"><span data-stu-id="54add-151">**Tiles**</span></span>
- <span data-ttu-id="54add-152">前年比購買成長</span><span class="sxs-lookup"><span data-stu-id="54add-152">YOY purchase growth</span></span>
- <span data-ttu-id="54add-153">前年比購買成長の割合 %</span><span class="sxs-lookup"><span data-stu-id="54add-153">YOY purchase growth %</span></span>

<span data-ttu-id="54add-154">**例**</span><span class="sxs-lookup"><span data-stu-id="54add-154">**Example**</span></span>
<img src="media/purchaseByPeriod.png" alt="Purchase by Period">

### <a name="purchase-by-vendor-location-report-page"></a><span data-ttu-id="54add-155">仕入先場所別購買レポートページ</span><span class="sxs-lookup"><span data-stu-id="54add-155">Purchase by vendor location report page</span></span>

<span data-ttu-id="54add-156">**グラフ**</span><span class="sxs-lookup"><span data-stu-id="54add-156">**Charts**</span></span>
- <span data-ttu-id="54add-157">市町村別の購買</span><span class="sxs-lookup"><span data-stu-id="54add-157">Purchase by city</span></span>
- <span data-ttu-id="54add-158">購買額の前年比成長の割合 %</span><span class="sxs-lookup"><span data-stu-id="54add-158">Purchase YOY growth %</span></span>
- <span data-ttu-id="54add-159">購買国</span><span class="sxs-lookup"><span data-stu-id="54add-159">Purchase by country</span></span>

<span data-ttu-id="54add-160">**例**</span><span class="sxs-lookup"><span data-stu-id="54add-160">**Example**</span></span>
<img src="media/purchByVendorLocation.png" alt="Purchase by Vendor Location">

### <a name="purchase-spend-analysis-by-time-report-page"></a><span data-ttu-id="54add-161">時間別購買先支出の分析レポートページ</span><span class="sxs-lookup"><span data-stu-id="54add-161">Purchase spend analysis by time report page</span></span>

<span data-ttu-id="54add-162">**グラフ**</span><span class="sxs-lookup"><span data-stu-id="54add-162">**Charts**</span></span> 
- <span data-ttu-id="54add-163">月/日別今年度の購買 (折れ線グラフ)</span><span class="sxs-lookup"><span data-stu-id="54add-163">Purchase current year by month / day (line chart)</span></span>
- <span data-ttu-id="54add-164">今年度および昨年度の購買 (線と円柱グラフ)</span><span class="sxs-lookup"><span data-stu-id="54add-164">Purchase current and last year (line and column chart)</span></span>

<span data-ttu-id="54add-165">**例**</span><span class="sxs-lookup"><span data-stu-id="54add-165">**Example**</span></span>
<img src="media/PurchByTIme.png" alt="Purchase by Time">

### <a name="purchase-spend-analysis-by-vendor-report-page"></a><span data-ttu-id="54add-166">仕入先別購買先支出の分析レポートページ</span><span class="sxs-lookup"><span data-stu-id="54add-166">Purchase spend analysis by vendor report page</span></span>

<span data-ttu-id="54add-167">**グラフ**</span><span class="sxs-lookup"><span data-stu-id="54add-167">**Charts**</span></span> 
- <span data-ttu-id="54add-168">トップ 10 の仕入先の購買割合 % (じょうご)</span><span class="sxs-lookup"><span data-stu-id="54add-168">Top 10 vendor purchase % of purchase (funnel)</span></span>
- <span data-ttu-id="54add-169">トップ 10 仕入先による増加支出額の前年比</span><span class="sxs-lookup"><span data-stu-id="54add-169">Top 10 vendors with increased spending YOY</span></span>
- <span data-ttu-id="54add-170">トップ 10 仕入先による減少支出額の前年比</span><span class="sxs-lookup"><span data-stu-id="54add-170">Top 10 vendors with decreased spending YOY</span></span>

<span data-ttu-id="54add-171">**例** 
</span><span class="sxs-lookup"><span data-stu-id="54add-171">**Example** 
</span></span><img src="media/PurchSpendAnalysisByVendor.png" alt="Purchase spend by vendor">


## <a name="data-model-and-entities"></a><span data-ttu-id="54add-172">データ モデルおよびエンティティ</span><span class="sxs-lookup"><span data-stu-id="54add-172">Data model and entities</span></span>
<span data-ttu-id="54add-173">次のデータは、**購買支出の分析** Power BI コンテンツのレポート ページに入力するために使用されます。</span><span class="sxs-lookup"><span data-stu-id="54add-173">The following data is used to fill the report pages in the **Purchase spend analysis** Power BI content.</span></span> <span data-ttu-id="54add-174">このデータは、エンティティ ストアで実施される集計の測定として表されます。</span><span class="sxs-lookup"><span data-stu-id="54add-174">This data is represented as aggregate measurements that are staged in the Entity store.</span></span> <span data-ttu-id="54add-175">エンティティ ストアは、分析に最適化された Microsoft SQL Server データベースです。</span><span class="sxs-lookup"><span data-stu-id="54add-175">The Entity store is a Microsoft SQL Server database that is optimized for analytics.</span></span> <span data-ttu-id="54add-176">詳細については、[エンティティ格納と Power BI の統合](power-bi-integration-entity-store.md) を参照してください。</span><span class="sxs-lookup"><span data-stu-id="54add-176">For more information, see [Power BI integration with Entity store](power-bi-integration-entity-store.md).</span></span>

<span data-ttu-id="54add-177">このコンテンツの集計の測定は Microsoft Dynamics AX 2012 および Microsoft Dynamics AX 2012 R3 の購買キューブに使用できた集計の測定のサブセットです。</span><span class="sxs-lookup"><span data-stu-id="54add-177">The aggregate measurements in this content are the subset of aggregate measurements that were available in the Purchase Cube in Microsoft Dynamics AX 2012 and Microsoft Dynamics AX 2012 R3.</span></span> <span data-ttu-id="54add-178">エンティティ格納でキューブの集計の測定を公開するには、それらを配置可能にする必要があります。</span><span class="sxs-lookup"><span data-stu-id="54add-178">To stage the cube's aggregate measurements in the Entity store, you must make them deployable.</span></span> <span data-ttu-id="54add-179">詳細については、[エンティティ ストアと Power BI の統合](power-bi-integration-entity-store.md) ブログ投稿で、集計の測定をエンティティ格納へ公開する手順を参照してください。</span><span class="sxs-lookup"><span data-stu-id="54add-179">For more information, see the procedure for staging aggregate measurements in the Entity store in [Power BI integration with Entity store](power-bi-integration-entity-store.md).</span></span> <span data-ttu-id="54add-180">次のキー集計の測定は、請求明細行エンティティから直接使用でき、コンテンツの基準として使用されます。</span><span class="sxs-lookup"><span data-stu-id="54add-180">The following key aggregate measurements are available directly from the Invoice lines entity and are used as the basis of the content.</span></span>

| <span data-ttu-id="54add-181">エンティティ</span><span class="sxs-lookup"><span data-stu-id="54add-181">Entity</span></span>        | <span data-ttu-id="54add-182">キー集計の測定</span><span class="sxs-lookup"><span data-stu-id="54add-182">Key aggregate measurements</span></span> | <span data-ttu-id="54add-183">データ ソース</span><span class="sxs-lookup"><span data-stu-id="54add-183">Data source</span></span>                                 | <span data-ttu-id="54add-184">フィールド</span><span class="sxs-lookup"><span data-stu-id="54add-184">Field</span></span>              | <span data-ttu-id="54add-185">説明</span><span class="sxs-lookup"><span data-stu-id="54add-185">Description</span></span>                            |
|---------------|----------------------------|---------------------------------------------|--------------------|----------------------------------------|
| <span data-ttu-id="54add-186">請求明細行</span><span class="sxs-lookup"><span data-stu-id="54add-186">Invoice lines</span></span> | <span data-ttu-id="54add-187">購買</span><span class="sxs-lookup"><span data-stu-id="54add-187">Purchase</span></span>                   | <span data-ttu-id="54add-188">VendInvoiceTrans</span><span class="sxs-lookup"><span data-stu-id="54add-188">VendInvoiceTrans</span></span>                            | <span data-ttu-id="54add-189">合計 (LineAmountMST)</span><span class="sxs-lookup"><span data-stu-id="54add-189">SUM(LineAmountMST)</span></span> | <span data-ttu-id="54add-190">会計通貨での金額。</span><span class="sxs-lookup"><span data-stu-id="54add-190">The amount in the accounting currency.</span></span> |

<span data-ttu-id="54add-191">次の表は、請求明細行のエンティティのコンテンツで計算される主要な測定単位を示します。</span><span class="sxs-lookup"><span data-stu-id="54add-191">The following table shows the key measurements in the content that are calculated from the Invoice lines entity.</span></span>

| <span data-ttu-id="54add-192">基準</span><span class="sxs-lookup"><span data-stu-id="54add-192">Measure</span></span>               | <span data-ttu-id="54add-193">計算</span><span class="sxs-lookup"><span data-stu-id="54add-193">Calculation</span></span>                                                                                         |
|-----------------------|-----------------------------------------------------------------------------------------------------|
| <span data-ttu-id="54add-194">今年度の購買</span><span class="sxs-lookup"><span data-stu-id="54add-194">Purchase current year</span></span> | <span data-ttu-id="54add-195">今年度の購買 = SUM('請求明細行'\[購買\])</span><span class="sxs-lookup"><span data-stu-id="54add-195">Purchase current year = SUM('Invoice lines'\[Purchase\])</span></span>                                            |
| <span data-ttu-id="54add-196">昨年度の購買</span><span class="sxs-lookup"><span data-stu-id="54add-196">Purchase last year</span></span>    | <span data-ttu-id="54add-197">昨年購買 = CALCULATE(合計 ('請求明細行'\[購買\]), SAMEPERIODLASTYEAR(日付\[日付\]))</span><span class="sxs-lookup"><span data-stu-id="54add-197">Purchase last year = CALCULATE(SUM('Invoice lines'\[Purchase\]), SAMEPERIODLASTYEAR(Dates\[Date\]))</span></span> |
| <span data-ttu-id="54add-198">前年比購買成長</span><span class="sxs-lookup"><span data-stu-id="54add-198">YOY purchase growth</span></span>   | <span data-ttu-id="54add-199">前年比購買成長 = \[今年度の購買\] – \[昨年度の購買\]</span><span class="sxs-lookup"><span data-stu-id="54add-199">YOY purchase growth = \[Purchase current year\] – \[Purchase last year\]</span></span>                            |

<span data-ttu-id="54add-200">コンテンツの以下のキー分析コードは、より高い粒度を達成し深い分析洞察を取得できるように、集計の測定をスライスするフィルターとして使用されます。</span><span class="sxs-lookup"><span data-stu-id="54add-200">The following key dimensions in the content are used as filters to slice the aggregate measurements, so that you can achieve more granularity and gain deeper analytical insights.</span></span>

| <span data-ttu-id="54add-201">エンティティ</span><span class="sxs-lookup"><span data-stu-id="54add-201">Entity</span></span>                 | <span data-ttu-id="54add-202">属性の例</span><span class="sxs-lookup"><span data-stu-id="54add-202">Examples of attributes</span></span>                                |
|------------------------|-------------------------------------------------------|
| <span data-ttu-id="54add-203">仕入先</span><span class="sxs-lookup"><span data-stu-id="54add-203">Vendors</span></span>                | <span data-ttu-id="54add-204">仕入先グループ、仕入先の国または地域、仕入先名</span><span class="sxs-lookup"><span data-stu-id="54add-204">Vendor groups, Vendor country or regions, Vendor name</span></span> |
| <span data-ttu-id="54add-205">製品</span><span class="sxs-lookup"><span data-stu-id="54add-205">Products</span></span>               | <span data-ttu-id="54add-206">製品番号、製品名、品目グループの名前</span><span class="sxs-lookup"><span data-stu-id="54add-206">Product number, Product name, Item groups name</span></span>        |
| <span data-ttu-id="54add-207">調達カテゴリ</span><span class="sxs-lookup"><span data-stu-id="54add-207">Procurement categories</span></span> | <span data-ttu-id="54add-208">調達カテゴリ、調達カテゴリの名前</span><span class="sxs-lookup"><span data-stu-id="54add-208">Procurement category, Procurement category names</span></span>      |
| <span data-ttu-id="54add-209">法人</span><span class="sxs-lookup"><span data-stu-id="54add-209">Legal entities</span></span>         | <span data-ttu-id="54add-210">法人名</span><span class="sxs-lookup"><span data-stu-id="54add-210">Legal entity name</span></span>                                     |
| <span data-ttu-id="54add-211">日付</span><span class="sxs-lookup"><span data-stu-id="54add-211">Dates</span></span>                  | <span data-ttu-id="54add-212">日付、年度相殺</span><span class="sxs-lookup"><span data-stu-id="54add-212">Dates, Year offset</span></span>                                    |

<span data-ttu-id="54add-213">既定では、コンテンツは、現在の暦年のデータが表示されます。</span><span class="sxs-lookup"><span data-stu-id="54add-213">By default, the content shows data for the current calendar year.</span></span> <span data-ttu-id="54add-214">ただし、レポートのフィルタ セクションの日付のフィルタを変更できます。</span><span class="sxs-lookup"><span data-stu-id="54add-214">However, you can change the date filter in the report filters section.</span></span> <span data-ttu-id="54add-215">会社フィルターを変更することもできます。</span><span class="sxs-lookup"><span data-stu-id="54add-215">You can also change the company filter.</span></span>


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]