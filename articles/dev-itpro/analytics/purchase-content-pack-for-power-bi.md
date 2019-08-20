---
title: 購買支出の分析 Power BI コンテンツ
description: このトピックでは、購買支出の分析 Power BI コンテンツの内容について説明します。 コンテンツに含まれているレポートにアクセスする方法を説明し、コンテンツを作成するために使用するデータ モデルおよびエンティティについての情報を提供します。
author: FrankDahl
manager: AnnBe
ms.date: 04/24/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-platform
ms.technology: ''
ms.search.form: PurchaseSpendAnalysisPowerBI
audience: Application User, IT Pro
ms.reviewer: kfend
ms.search.scope: Core, Operations
ms.custom: 265434
ms.assetid: 3cd9dfce-2687-4303-bc78-349e7cb5ea75
ms.search.region: global
ms.author: fdahl
ms.search.validFrom: 2016-11-30
ms.dyn365.ops.version: Version 1611
ms.openlocfilehash: 571f443b02268cbee8fe787f25419e046ba99aeb
ms.sourcegitcommit: 16bfa0fd08feec1647829630401ce62ce2ffa1a4
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 08/02/2019
ms.locfileid: "1850022"
---
# <a name="purchase-spend-analysis-power-bi-content"></a><span data-ttu-id="aa0b2-104">購買支出の分析 Power BI コンテンツ</span><span class="sxs-lookup"><span data-stu-id="aa0b2-104">Purchase spend analysis Power BI content</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="aa0b2-105">このトピックでは、**購買支出の分析** Microsoft Power BI コンテンツの内容について説明します。</span><span class="sxs-lookup"><span data-stu-id="aa0b2-105">This topic describes what is included in the **Purchase spend analysis** Microsoft Power BI content.</span></span> <span data-ttu-id="aa0b2-106">Power BI レポートにアクセスする方法を説明し、コンテンツを作成するために使用するデータ モデルおよびエンティティについての情報を提供します。</span><span class="sxs-lookup"><span data-stu-id="aa0b2-106">It explains how to access the Power BI reports, and provides information about the data model and entities that are used to build the content.</span></span>

## <a name="overview"></a><span data-ttu-id="aa0b2-107">概要</span><span class="sxs-lookup"><span data-stu-id="aa0b2-107">Overview</span></span>

<span data-ttu-id="aa0b2-108">**購買支出の分析** Power BI コンテンツは、予算を担当する購買部門のマネージャーおよびマネージャーが購買支出を追跡できるように設計されています。</span><span class="sxs-lookup"><span data-stu-id="aa0b2-108">The **Purchase spend analysis** Power BI content was designed to help purchasing managers and managers who are responsible for budgets keep track of purchase spending.</span></span> <span data-ttu-id="aa0b2-109">マネージャーは、以下の方法で購買支出を分析できます:</span><span class="sxs-lookup"><span data-stu-id="aa0b2-109">Managers can analyze purchase spending in the following ways:</span></span>

- <span data-ttu-id="aa0b2-110">会計年度の購買 (仕入先グループと個々の仕入先、調達カテゴリと個々の製品、仕入先の場所)</span><span class="sxs-lookup"><span data-stu-id="aa0b2-110">Year-to-date purchase (by vendor group and individual vendors, procurement category and individual products, and vendor location)</span></span>
- <span data-ttu-id="aa0b2-111">前年比購買の変化 (仕入先グループと調達カテゴリ)</span><span class="sxs-lookup"><span data-stu-id="aa0b2-111">Year-over-year purchase change (by vendor group and procurement category)</span></span>

<span data-ttu-id="aa0b2-112">コンテンツは購買トランザクション データを使用して、会社全体の購買数の集計ビュー、仕入先および製品の購買先支出の内訳の両方を提供します。</span><span class="sxs-lookup"><span data-stu-id="aa0b2-112">The content uses purchase transactional data, and provides both an aggregate view of the company-wide purchase figures and a breakdown of purchase spending by vendor and product.</span></span> <span data-ttu-id="aa0b2-113">レポートでは時間経過に伴う購買支出の変化が強調表示されています。</span><span class="sxs-lookup"><span data-stu-id="aa0b2-113">Reports highlight changes in purchase spending over time.</span></span> <span data-ttu-id="aa0b2-114">そのため、このレポートは、個々の仕入先や製品の積極的および消極的な支出動向を管理者に警告するために使用することができます。</span><span class="sxs-lookup"><span data-stu-id="aa0b2-114">Therefore, the reports can be used to alert managers about positive and negative spending trends for individual vendors and products.</span></span> <span data-ttu-id="aa0b2-115">また、チャートは、様々な調達カテゴリおよび仕入先グループの購買支出を示します。</span><span class="sxs-lookup"><span data-stu-id="aa0b2-115">Additionally, charts show purchase spending for different procurement categories and vendor groups.</span></span> <span data-ttu-id="aa0b2-116">それゆえ、カテゴリおよび地域マネージャーは、チャートを使用して支出行動の変化を識別することができます。</span><span class="sxs-lookup"><span data-stu-id="aa0b2-116">Therefore, category and regional managers can use the charts to help identify changes in spending behavior.</span></span>

## <a name="accessing-the-power-bi-content"></a><span data-ttu-id="aa0b2-117">Power BI コンテンツへのアクセス</span><span class="sxs-lookup"><span data-stu-id="aa0b2-117">Accessing the Power BI content</span></span>
<span data-ttu-id="aa0b2-118">**購買支出の分析** Power BI コンテンツは**購買支出の分析**ページ (**調達** \> **照会およびレポート** \> **購買パフォーマンスの分析** \> **購買支出の分析**) に表示されます。</span><span class="sxs-lookup"><span data-stu-id="aa0b2-118">The **Purchase spend analysis** Power BI content is shown on the **Purchase and spend analysis** page (**Procurement and sourcing** \> **Inquiries and reports** \> **Purchase performance analysis** \> **Purchase and spend analysis**).</span></span>

## <a name="metrics-that-are-included-in-the-power-bi-content"></a><span data-ttu-id="aa0b2-119">Power BI コンテンツに含まれるメトリックス</span><span class="sxs-lookup"><span data-stu-id="aa0b2-119">Metrics that are included in the Power BI content</span></span>
<span data-ttu-id="aa0b2-120">**購買支出の分析** Power BI コンテンツには、一連のメトリックスで構成されるレポートが含まれます。</span><span class="sxs-lookup"><span data-stu-id="aa0b2-120">The **Purchase spend analysis** Power BI content includes a report that consists of a set of metrics.</span></span> <span data-ttu-id="aa0b2-121">これらのメトリックスはグラフ、タイル、表として視覚化されます。</span><span class="sxs-lookup"><span data-stu-id="aa0b2-121">These metrics are visualized as charts, tiles, and tables.</span></span> 

<span data-ttu-id="aa0b2-122">次の表は、視覚化の概要を示しています。</span><span class="sxs-lookup"><span data-stu-id="aa0b2-122">The following sections provide an overview of the visualizations.</span></span>

### <a name="purchase-by-vendor-report-page"></a><span data-ttu-id="aa0b2-123">仕入先別購入レポートページ</span><span class="sxs-lookup"><span data-stu-id="aa0b2-123">Purchase by vendor report page</span></span>
<span data-ttu-id="aa0b2-124">**グラフ**</span><span class="sxs-lookup"><span data-stu-id="aa0b2-124">**Charts**</span></span>
- <span data-ttu-id="aa0b2-125">購買別トップ 10 の仕入先 (積み上げ棒グラフ)</span><span class="sxs-lookup"><span data-stu-id="aa0b2-125">Top 10 vendors by purchase (stacked bar chart)</span></span>
- <span data-ttu-id="aa0b2-126">仕入先グループ、国、名前別購買合計 (円グラフ)</span><span class="sxs-lookup"><span data-stu-id="aa0b2-126">Total purchase by vendor group / country / name (pie chart)</span></span>
- <span data-ttu-id="aa0b2-127">仕入先グループ、国、名前別購買 (円柱グラフ)</span><span class="sxs-lookup"><span data-stu-id="aa0b2-127">Purchase by vendor group / country / name (column chart)</span></span>
- <span data-ttu-id="aa0b2-128">仕入先グループ、国、名前別平均購買 (円柱グラフ)</span><span class="sxs-lookup"><span data-stu-id="aa0b2-128">Average purchase by vendor group / country / name (column chart)</span></span>

<span data-ttu-id="aa0b2-129">**タイル**</span><span class="sxs-lookup"><span data-stu-id="aa0b2-129">**Tiles**</span></span>
- <span data-ttu-id="aa0b2-130">購買の合計</span><span class="sxs-lookup"><span data-stu-id="aa0b2-130">Total purchase</span></span>
- <span data-ttu-id="aa0b2-131">前年比購買成長</span><span class="sxs-lookup"><span data-stu-id="aa0b2-131">YOY purchase growth</span></span>
- <span data-ttu-id="aa0b2-132">合計仕入先数</span><span class="sxs-lookup"><span data-stu-id="aa0b2-132">Total # vendors</span></span>
- <span data-ttu-id="aa0b2-133">有効な仕入先合計数</span><span class="sxs-lookup"><span data-stu-id="aa0b2-133">Total # of active vendors</span></span>

<span data-ttu-id="aa0b2-134">**例**</span><span class="sxs-lookup"><span data-stu-id="aa0b2-134">**Example**</span></span>
<img src="media/spend1.PNG" alt="Purchase by vendor">

### <a name="purchase-by-product-report-page"></a><span data-ttu-id="aa0b2-135">製品別購買レポートページ</span><span class="sxs-lookup"><span data-stu-id="aa0b2-135">Purchase by product report page</span></span>

<span data-ttu-id="aa0b2-136">**グラフ**</span><span class="sxs-lookup"><span data-stu-id="aa0b2-136">**Charts**</span></span>
- <span data-ttu-id="aa0b2-137">調達カテゴリまたは製品名別購買 (円柱グラフ)</span><span class="sxs-lookup"><span data-stu-id="aa0b2-137">Purchase by procurement category / product name (column chart)</span></span>
- <span data-ttu-id="aa0b2-138">調達カテゴリまたは製品名 (円グラフ) 別購買合計</span><span class="sxs-lookup"><span data-stu-id="aa0b2-138">Total purchase by procurement category / product name (pie chart)</span></span>
- <span data-ttu-id="aa0b2-139">購買別トップ 10 製品 (積み上げ棒グラフ)</span><span class="sxs-lookup"><span data-stu-id="aa0b2-139">Top 10 products by purchase (stacked bar chart)</span></span>

<span data-ttu-id="aa0b2-140">**タイル**</span><span class="sxs-lookup"><span data-stu-id="aa0b2-140">**Tiles**</span></span>
- <span data-ttu-id="aa0b2-141">製品の合計数</span><span class="sxs-lookup"><span data-stu-id="aa0b2-141">Total # of products</span></span></li>
- <span data-ttu-id="aa0b2-142">製品合計数の有効な製品の合計割合</span><span class="sxs-lookup"><span data-stu-id="aa0b2-142">Total active products percentage of total # of products</span></span>
- <span data-ttu-id="aa0b2-143">購買の 80% を占める製品の数</span><span class="sxs-lookup"><span data-stu-id="aa0b2-143">Number of products accounting for 80% purchase</span></span>

<span data-ttu-id="aa0b2-144">**例**</span><span class="sxs-lookup"><span data-stu-id="aa0b2-144">**Example**</span></span>


<img src="media/purchaseByProduct.PNG" alt="Purchase by Product">

### <a name="purchase-by-period-report-page"></a><span data-ttu-id="aa0b2-145">期間別購買レポートページ</span><span class="sxs-lookup"><span data-stu-id="aa0b2-145">Purchase by period report page</span></span>
<span data-ttu-id="aa0b2-146">このページでは、今年度と昨年度の購買、および調達カテゴリによる成長が表示されます。</span><span class="sxs-lookup"><span data-stu-id="aa0b2-146">This page shows purchases this year and last year, and growth by procurement category.</span></span>

<span data-ttu-id="aa0b2-147">**グラフ**</span><span class="sxs-lookup"><span data-stu-id="aa0b2-147">**Charts**</span></span> 
- <span data-ttu-id="aa0b2-148">月/日別の購買 (円柱グラフ)</span><span class="sxs-lookup"><span data-stu-id="aa0b2-148">Purchase by month / day (column chart)</span></span>
- <span data-ttu-id="aa0b2-149">累計購買金額の前年比差異 (伝播)</span><span class="sxs-lookup"><span data-stu-id="aa0b2-149">Cumulative purchase YOY variance (waterfall chart)</span></span>
- <span data-ttu-id="aa0b2-150">合計購買金額の前年比成長 (円柱グラフ)</span><span class="sxs-lookup"><span data-stu-id="aa0b2-150">Total purchase YOY growth (column chart)</span></span>
- <span data-ttu-id="aa0b2-151">調達明細書 (マトリックス)</span><span class="sxs-lookup"><span data-stu-id="aa0b2-151">Procurement statement (matrix)</span></span>

<span data-ttu-id="aa0b2-152">**タイル**</span><span class="sxs-lookup"><span data-stu-id="aa0b2-152">**Tiles**</span></span>
- <span data-ttu-id="aa0b2-153">前年比購買成長</span><span class="sxs-lookup"><span data-stu-id="aa0b2-153">YOY purchase growth</span></span>
- <span data-ttu-id="aa0b2-154">前年比購買成長の割合 %</span><span class="sxs-lookup"><span data-stu-id="aa0b2-154">YOY purchase growth %</span></span>

<span data-ttu-id="aa0b2-155">**例**</span><span class="sxs-lookup"><span data-stu-id="aa0b2-155">**Example**</span></span>
<img src="media/purchaseByPeriod.PNG" alt="Purchase by Period">

### <a name="purchase-by-vendor-location-report-page"></a><span data-ttu-id="aa0b2-156">仕入先場所別購買レポートページ</span><span class="sxs-lookup"><span data-stu-id="aa0b2-156">Purchase by vendor location report page</span></span>

<span data-ttu-id="aa0b2-157">**グラフ**</span><span class="sxs-lookup"><span data-stu-id="aa0b2-157">**Charts**</span></span>
- <span data-ttu-id="aa0b2-158">市町村別の購買</span><span class="sxs-lookup"><span data-stu-id="aa0b2-158">Purchase by city</span></span>
- <span data-ttu-id="aa0b2-159">購買額の前年比成長の割合 %</span><span class="sxs-lookup"><span data-stu-id="aa0b2-159">Purchase YOY growth %</span></span>
- <span data-ttu-id="aa0b2-160">購買国</span><span class="sxs-lookup"><span data-stu-id="aa0b2-160">Purchase by country</span></span>

<span data-ttu-id="aa0b2-161">**例**</span><span class="sxs-lookup"><span data-stu-id="aa0b2-161">**Example**</span></span>
<img src="media/purchByVendorLocation.PNG" alt="Purchase by Vendor Location">

### <a name="purchase-spend-analysis-by-time-report-page"></a><span data-ttu-id="aa0b2-162">時間別購買先支出の分析レポートページ</span><span class="sxs-lookup"><span data-stu-id="aa0b2-162">Purchase spend analysis by time report page</span></span>

<span data-ttu-id="aa0b2-163">**グラフ**</span><span class="sxs-lookup"><span data-stu-id="aa0b2-163">**Charts**</span></span> 
- <span data-ttu-id="aa0b2-164">月/日別今年度の購買 (折れ線グラフ)</span><span class="sxs-lookup"><span data-stu-id="aa0b2-164">Purchase current year by month / day (line chart)</span></span>
- <span data-ttu-id="aa0b2-165">今年度および昨年度の購買 (線と円柱グラフ)</span><span class="sxs-lookup"><span data-stu-id="aa0b2-165">Purchase current and last year (line and column chart)</span></span>

<span data-ttu-id="aa0b2-166">**例**</span><span class="sxs-lookup"><span data-stu-id="aa0b2-166">**Example**</span></span>
<img src="media/PurchByTIme.PNG" alt="Purchase by Time">

### <a name="purchase-spend-analysis-by-vendor-report-page"></a><span data-ttu-id="aa0b2-167">仕入先別購買先支出の分析レポートページ</span><span class="sxs-lookup"><span data-stu-id="aa0b2-167">Purchase spend analysis by vendor report page</span></span>

<span data-ttu-id="aa0b2-168">**グラフ**</span><span class="sxs-lookup"><span data-stu-id="aa0b2-168">**Charts**</span></span> 
- <span data-ttu-id="aa0b2-169">トップ 10 の仕入先の購買割合 % (じょうご)</span><span class="sxs-lookup"><span data-stu-id="aa0b2-169">Top 10 vendor purchase % of purchase (funnel)</span></span>
- <span data-ttu-id="aa0b2-170">トップ 10 仕入先による増加支出額の前年比</span><span class="sxs-lookup"><span data-stu-id="aa0b2-170">Top 10 vendors with increased spending YOY</span></span>
- <span data-ttu-id="aa0b2-171">トップ 10 仕入先による減少支出額の前年比</span><span class="sxs-lookup"><span data-stu-id="aa0b2-171">Top 10 vendors with decreased spending YOY</span></span>

<span data-ttu-id="aa0b2-172">**例** 
</span><span class="sxs-lookup"><span data-stu-id="aa0b2-172">**Example** 
</span></span><img src="media/PurchSpendAnalysisByVendor.PNG" alt="Purchase spend by vendor">


## <a name="data-model-and-entities"></a><span data-ttu-id="aa0b2-173">データ モデルおよびエンティティ</span><span class="sxs-lookup"><span data-stu-id="aa0b2-173">Data model and entities</span></span>
<span data-ttu-id="aa0b2-174">次のデータは、**購買支出の分析** Power BI コンテンツのレポート ページに入力するために使用されます。</span><span class="sxs-lookup"><span data-stu-id="aa0b2-174">The following data is used to fill the report pages in the **Purchase spend analysis** Power BI content.</span></span> <span data-ttu-id="aa0b2-175">このデータは、エンティティ ストアで実施される集計の測定として表されます。</span><span class="sxs-lookup"><span data-stu-id="aa0b2-175">This data is represented as aggregate measurements that are staged in the Entity store.</span></span> <span data-ttu-id="aa0b2-176">エンティティ ストアは、分析に最適化された Microsoft SQL Server データベースです。</span><span class="sxs-lookup"><span data-stu-id="aa0b2-176">The Entity store is a Microsoft SQL Server database that is optimized for analytics.</span></span> <span data-ttu-id="aa0b2-177">詳細については、[エンティティ格納と Power BI の統合の概要](power-bi-integration-entity-store.md) を参照してください。</span><span class="sxs-lookup"><span data-stu-id="aa0b2-177">For more information, see [Overview of Power BI integration with Entity store](power-bi-integration-entity-store.md).</span></span>

<span data-ttu-id="aa0b2-178">このコンテンツの集計の測定は Microsoft Dynamics AX 2012 および Microsoft Dynamics AX 2012 R3 の購買キューブに使用できた集計の測定のサブセットです。</span><span class="sxs-lookup"><span data-stu-id="aa0b2-178">The aggregate measurements in this content are the subset of aggregate measurements that were available in the Purchase Cube in Microsoft Dynamics AX 2012 and Microsoft Dynamics AX 2012 R3.</span></span> <span data-ttu-id="aa0b2-179">エンティティ格納でキューブの集計の測定を公開するには、それらを配置可能にする必要があります。</span><span class="sxs-lookup"><span data-stu-id="aa0b2-179">To stage the cube's aggregate measurements in the Entity store, you must make them deployable.</span></span> <span data-ttu-id="aa0b2-180">詳細については、[エンティティ ストアと Power BI の統合の概要](power-bi-integration-entity-store.md) ブログ投稿で、集計の測定をエンティティ格納へ公開する手順を参照してください。</span><span class="sxs-lookup"><span data-stu-id="aa0b2-180">For more information, see the procedure for staging aggregate measurements in the Entity store in [Overview of Power BI integration with Entity store](power-bi-integration-entity-store.md).</span></span> <span data-ttu-id="aa0b2-181">次のキー集計の測定は、請求明細行エンティティから直接使用でき、コンテンツの基準として使用されます。</span><span class="sxs-lookup"><span data-stu-id="aa0b2-181">The following key aggregate measurements are available directly from the Invoice lines entity and are used as the basis of the content.</span></span>

| <span data-ttu-id="aa0b2-182">エンティティ</span><span class="sxs-lookup"><span data-stu-id="aa0b2-182">Entity</span></span>        | <span data-ttu-id="aa0b2-183">キー集計の測定</span><span class="sxs-lookup"><span data-stu-id="aa0b2-183">Key aggregate measurements</span></span> | <span data-ttu-id="aa0b2-184">データ ソース</span><span class="sxs-lookup"><span data-stu-id="aa0b2-184">Data source</span></span>                                 | <span data-ttu-id="aa0b2-185">フィールド</span><span class="sxs-lookup"><span data-stu-id="aa0b2-185">Field</span></span>              | <span data-ttu-id="aa0b2-186">説明</span><span class="sxs-lookup"><span data-stu-id="aa0b2-186">Description</span></span>                            |
|---------------|----------------------------|---------------------------------------------|--------------------|----------------------------------------|
| <span data-ttu-id="aa0b2-187">請求明細行</span><span class="sxs-lookup"><span data-stu-id="aa0b2-187">Invoice lines</span></span> | <span data-ttu-id="aa0b2-188">購買</span><span class="sxs-lookup"><span data-stu-id="aa0b2-188">Purchase</span></span>                   | <span data-ttu-id="aa0b2-189">VendInvoiceTrans</span><span class="sxs-lookup"><span data-stu-id="aa0b2-189">VendInvoiceTrans</span></span>                            | <span data-ttu-id="aa0b2-190">合計 (LineAmountMST)</span><span class="sxs-lookup"><span data-stu-id="aa0b2-190">SUM(LineAmountMST)</span></span> | <span data-ttu-id="aa0b2-191">会計通貨での金額。</span><span class="sxs-lookup"><span data-stu-id="aa0b2-191">The amount in the accounting currency.</span></span> |

<span data-ttu-id="aa0b2-192">次の表は、請求明細行のエンティティのコンテンツで計算される主要な測定単位を示します。</span><span class="sxs-lookup"><span data-stu-id="aa0b2-192">The following table shows the key measurements in the content that are calculated from the Invoice lines entity.</span></span>

| <span data-ttu-id="aa0b2-193">基準</span><span class="sxs-lookup"><span data-stu-id="aa0b2-193">Measure</span></span>               | <span data-ttu-id="aa0b2-194">計算</span><span class="sxs-lookup"><span data-stu-id="aa0b2-194">Calculation</span></span>                                                                                         |
|-----------------------|-----------------------------------------------------------------------------------------------------|
| <span data-ttu-id="aa0b2-195">今年度の購買</span><span class="sxs-lookup"><span data-stu-id="aa0b2-195">Purchase current year</span></span> | <span data-ttu-id="aa0b2-196">今年度の購買 = SUM('請求明細行'\[購買\])</span><span class="sxs-lookup"><span data-stu-id="aa0b2-196">Purchase current year = SUM('Invoice lines'\[Purchase\])</span></span>                                            |
| <span data-ttu-id="aa0b2-197">昨年度の購買</span><span class="sxs-lookup"><span data-stu-id="aa0b2-197">Purchase last year</span></span>    | <span data-ttu-id="aa0b2-198">昨年購買 = CALCULATE(合計 ('請求明細行'\[購買\]), SAMEPERIODLASTYEAR(日付\[日付\]))</span><span class="sxs-lookup"><span data-stu-id="aa0b2-198">Purchase last year = CALCULATE(SUM('Invoice lines'\[Purchase\]), SAMEPERIODLASTYEAR(Dates\[Date\]))</span></span> |
| <span data-ttu-id="aa0b2-199">前年比購買成長</span><span class="sxs-lookup"><span data-stu-id="aa0b2-199">YOY purchase growth</span></span>   | <span data-ttu-id="aa0b2-200">前年比購買成長 = \[今年度の購買\] – \[昨年度の購買\]</span><span class="sxs-lookup"><span data-stu-id="aa0b2-200">YOY purchase growth = \[Purchase current year\] – \[Purchase last year\]</span></span>                            |

<span data-ttu-id="aa0b2-201">コンテンツの以下のキー分析コードは、より高い粒度を達成し深い分析洞察を取得できるように、集計の測定をスライスするフィルターとして使用されます。</span><span class="sxs-lookup"><span data-stu-id="aa0b2-201">The following key dimensions in the content are used as filters to slice the aggregate measurements, so that you can achieve more granularity and gain deeper analytical insights.</span></span>

| <span data-ttu-id="aa0b2-202">エンティティ</span><span class="sxs-lookup"><span data-stu-id="aa0b2-202">Entity</span></span>                 | <span data-ttu-id="aa0b2-203">属性の例</span><span class="sxs-lookup"><span data-stu-id="aa0b2-203">Examples of attributes</span></span>                                |
|------------------------|-------------------------------------------------------|
| <span data-ttu-id="aa0b2-204">仕入先</span><span class="sxs-lookup"><span data-stu-id="aa0b2-204">Vendors</span></span>                | <span data-ttu-id="aa0b2-205">仕入先グループ、仕入先の国または地域、仕入先名</span><span class="sxs-lookup"><span data-stu-id="aa0b2-205">Vendor groups, Vendor country or regions, Vendor name</span></span> |
| <span data-ttu-id="aa0b2-206">製品</span><span class="sxs-lookup"><span data-stu-id="aa0b2-206">Products</span></span>               | <span data-ttu-id="aa0b2-207">製品番号、製品名、品目グループの名前</span><span class="sxs-lookup"><span data-stu-id="aa0b2-207">Product number, Product name, Item groups name</span></span>        |
| <span data-ttu-id="aa0b2-208">調達カテゴリ</span><span class="sxs-lookup"><span data-stu-id="aa0b2-208">Procurement categories</span></span> | <span data-ttu-id="aa0b2-209">調達カテゴリ、調達カテゴリの名前</span><span class="sxs-lookup"><span data-stu-id="aa0b2-209">Procurement category, Procurement category names</span></span>      |
| <span data-ttu-id="aa0b2-210">法人</span><span class="sxs-lookup"><span data-stu-id="aa0b2-210">Legal entities</span></span>         | <span data-ttu-id="aa0b2-211">法人名</span><span class="sxs-lookup"><span data-stu-id="aa0b2-211">Legal entity name</span></span>                                     |
| <span data-ttu-id="aa0b2-212">日付</span><span class="sxs-lookup"><span data-stu-id="aa0b2-212">Dates</span></span>                  | <span data-ttu-id="aa0b2-213">日付、年度相殺</span><span class="sxs-lookup"><span data-stu-id="aa0b2-213">Dates, Year offset</span></span>                                    |

<span data-ttu-id="aa0b2-214">既定では、コンテンツは、現在の暦年のデータが表示されます。</span><span class="sxs-lookup"><span data-stu-id="aa0b2-214">By default, the content shows data for the current calendar year.</span></span> <span data-ttu-id="aa0b2-215">ただし、レポートのフィルタ セクションの日付のフィルタを変更できます。</span><span class="sxs-lookup"><span data-stu-id="aa0b2-215">However, you can change the date filter in the report filters section.</span></span> <span data-ttu-id="aa0b2-216">会社フィルターを変更することもできます。</span><span class="sxs-lookup"><span data-stu-id="aa0b2-216">You can also change the company filter.</span></span>
