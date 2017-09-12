---
title: "購買先支出分析 Power BI コンテンツ"
description: "このトピックでは、購買と支出の分析 Power BI コンテンツの内容について説明します。 コンテンツに含まれているレポートにアクセスする方法を説明し、コンテンツを作成するために使用するデータ モデルおよびエンティティについての情報を提供します。"
author: FrankDahl
manager: AnnBe
ms.date: 06/16/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-platform
ms.technology: 
audience: Application User, IT Pro
ms.reviewer: sericks
ms.search.scope: Core, Operations, UnifiedOperations
ms.custom: 265434
ms.assetid: 3cd9dfce-2687-4303-bc78-349e7cb5ea75
ms.search.region: global
ms.author: fdahl
ms.search.validFrom: 2016-11-30
ms.dyn365.ops.version: Version 1611
ms.translationtype: Human Translation
ms.sourcegitcommit: 08c38aada355583c5a6872f75b57db95d9b81786
ms.openlocfilehash: 4e60a6c7d79f59382b3958b849d78aac18550bc3
ms.contentlocale: ja-jp
ms.lasthandoff: 07/18/2017

---

# <a name="purchase-spend-analysis-power-bi-content"></a><span data-ttu-id="cd097-104">購買先支出分析 Power BI コンテンツ</span><span class="sxs-lookup"><span data-stu-id="cd097-104">Purchase spend analysis Power BI content</span></span>

[!include[banner](../includes/banner.md)]

<span data-ttu-id="cd097-105">このトピックでは、[**購買と支出の分析**] Microsoft Power BI コンテンツの内容について説明します。</span><span class="sxs-lookup"><span data-stu-id="cd097-105">This topic describes what is included in the **Purchase spend analysis** Microsoft Power BI content.</span></span> <span data-ttu-id="cd097-106">Power BI レポートにアクセスする方法を説明し、コンテンツを作成するために使用するデータ モデルおよびエンティティについての情報を提供します。</span><span class="sxs-lookup"><span data-stu-id="cd097-106">It explains how to access the Power BI reports, and provides information about the data model and entities that are used to build the content.</span></span>

## <a name="overview"></a><span data-ttu-id="cd097-107">概要</span><span class="sxs-lookup"><span data-stu-id="cd097-107">Overview</span></span>

<span data-ttu-id="cd097-108">[**購買支出の分析**] Power BI コンテンツは、予算を担当する購買部門のマネージャーおよびマネージャーが購買支出に留意するように設計されています。</span><span class="sxs-lookup"><span data-stu-id="cd097-108">The **Purchase spend analysis** Power BI content was designed to help purchasing managers and managers who are responsible for budgets keep an eye on purchase spending.</span></span> <span data-ttu-id="cd097-109">マネージャーは、以下の方法で購買支出を分析できます:</span><span class="sxs-lookup"><span data-stu-id="cd097-109">Managers can analyze purchase spending in the following ways:</span></span>

-   <span data-ttu-id="cd097-110">会計年度の購買 (仕入先グループと個々の仕入先、調達カテゴリと個々の製品、仕入先の場所)</span><span class="sxs-lookup"><span data-stu-id="cd097-110">Year-to-date purchase (by vendor group and individual vendors, procurement category and individual products, and vendor location)</span></span>
-   <span data-ttu-id="cd097-111">前年比購買の変化 (仕入先グループと調達カテゴリ)</span><span class="sxs-lookup"><span data-stu-id="cd097-111">Year-over-year purchase change (by vendor group and procurement category)</span></span>

<span data-ttu-id="cd097-112">コンテンツは購買トランザクション データを使用して、会社全体の購買数の集計ビュー、仕入先および製品の購買先支出の内訳の両方を提供します。</span><span class="sxs-lookup"><span data-stu-id="cd097-112">The content uses purchase transactional data, and provides both an aggregate view of the company-wide purchase figures and a breakdown of purchase spending by vendor and product.</span></span> <span data-ttu-id="cd097-113">レポートでは時間経過に伴う購買支出の変化が強調表示されています。</span><span class="sxs-lookup"><span data-stu-id="cd097-113">Reports highlight changes in purchase spending over time.</span></span> <span data-ttu-id="cd097-114">そのため、このレポートは、個々の仕入先や製品の積極的および消極的な支出動向を管理者に警告するために使用することができます。</span><span class="sxs-lookup"><span data-stu-id="cd097-114">Therefore, the reports can be used to alert managers about positive and negative spending trends for individual vendors and products.</span></span> <span data-ttu-id="cd097-115">また、チャートは、様々な調達カテゴリおよび仕入先グループの購買支出を示します。</span><span class="sxs-lookup"><span data-stu-id="cd097-115">Additionally, charts show purchase spending for different procurement categories and vendor groups.</span></span> <span data-ttu-id="cd097-116">それゆえ、カテゴリおよび地域マネージャーは、チャートを使用して支出行動の変化を識別することができます。</span><span class="sxs-lookup"><span data-stu-id="cd097-116">Therefore, category and regional managers can use the charts to help identify changes in spending behavior.</span></span>

## <a name="accessing-the-power-bi-content"></a><span data-ttu-id="cd097-117">Power BI コンテンツへのアクセス</span><span class="sxs-lookup"><span data-stu-id="cd097-117">Accessing the Power BI content</span></span>
<span data-ttu-id="cd097-118">Microsoft Dynamics 365 for Finance and Operations Enterprise エディション (2017 年 7 月) を使用している場合は、[**購買支出の分析**] Power BI コンテンツは、[**購買支出の分析**]ページ ([**調達**] > [**照会およびレポート**] > [**購買パフォーマンスの分析**] > [**購買支出の分析**]) に表示されます。</span><span class="sxs-lookup"><span data-stu-id="cd097-118">If you're using Microsoft Dynamics 365 for Finance and Operations, Enterprise edition July 2017 update, the **Purchase spend analysis** Power BI content is shown on the **Purchase and spend analysis** page (**Procurement and sourcing** > **Inquiries and reports** > **Purchase performance analysis** > **Purchase and spend analysis**).</span></span> 

## <a name="metrics-that-are-included-in-the-power-bi-content"></a><span data-ttu-id="cd097-119">Power BI コンテンツに含まれるメトリックス</span><span class="sxs-lookup"><span data-stu-id="cd097-119">Metrics that are included in the Power BI content</span></span>
<span data-ttu-id="cd097-120">[**購買と支出の分析**] Power BI コンテンツには、一連のメトリックスで構成されるレポートが含まれます。</span><span class="sxs-lookup"><span data-stu-id="cd097-120">The **Purchase spend analysis** Power BI content includes a report that consists of a set of metrics.</span></span> <span data-ttu-id="cd097-121">これらのメトリックスはグラフ、タイル、表として視覚化されます。</span><span class="sxs-lookup"><span data-stu-id="cd097-121">These metrics are visualized as charts, tiles, and tables.</span></span> <span data-ttu-id="cd097-122">次の表は、視覚エフェクトの概要を示します。</span><span class="sxs-lookup"><span data-stu-id="cd097-122">The following table provides an overview of the visualizations.</span></span>

<table>
<colgroup>
<col width="33%" />
<col width="33%" />
<col width="33%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="cd097-123">レポート ページ</span><span class="sxs-lookup"><span data-stu-id="cd097-123">Report page</span></span></th>
<th><span data-ttu-id="cd097-124">グラフ</span><span class="sxs-lookup"><span data-stu-id="cd097-124">Charts</span></span></th>
<th><span data-ttu-id="cd097-125">タイル</span><span class="sxs-lookup"><span data-stu-id="cd097-125">Tiles</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="cd097-126">仕入先別購買</span><span class="sxs-lookup"><span data-stu-id="cd097-126">Purchase by vendor</span></span></td>
<td><ul>
<li><span data-ttu-id="cd097-127">購買別トップ 10 の仕入先 (積み上げ棒グラフ)</span><span class="sxs-lookup"><span data-stu-id="cd097-127">Top 10 vendors by purchase (stacked bar chart)</span></span></li>
<li><span data-ttu-id="cd097-128">仕入先グループ、国、名前別購買合計 (円グラフ)</span><span class="sxs-lookup"><span data-stu-id="cd097-128">Total purchase by vendor group / country / name (pie chart)</span></span></li>
<li><span data-ttu-id="cd097-129">仕入先グループ、国、名前別購買 (円柱グラフ)</span><span class="sxs-lookup"><span data-stu-id="cd097-129">Purchase by vendor group / country / name (column chart)</span></span></li>
<li><span data-ttu-id="cd097-130">仕入先グループ、国、名前別平均購買 (円柱グラフ)</span><span class="sxs-lookup"><span data-stu-id="cd097-130">Average purchase by vendor group / country / name (column chart)</span></span></li>
</ul></td>
<td><ul>
<li><span data-ttu-id="cd097-131">購買の合計</span><span class="sxs-lookup"><span data-stu-id="cd097-131">Total purchase</span></span></li>
<li><span data-ttu-id="cd097-132">前年比購買成長</span><span class="sxs-lookup"><span data-stu-id="cd097-132">YOY purchase growth</span></span></li>
<li><span data-ttu-id="cd097-133">合計仕入先数</span><span class="sxs-lookup"><span data-stu-id="cd097-133">Total # vendors</span></span></li>
<li><span data-ttu-id="cd097-134">有効な仕入先合計数</span><span class="sxs-lookup"><span data-stu-id="cd097-134">Total # of active vendors</span></span></li>
</ul></td>
</tr>
<tr class="even">
<td><span data-ttu-id="cd097-135">製品別購買</span><span class="sxs-lookup"><span data-stu-id="cd097-135">Purchase by product</span></span></td>
<td><ul>
<li><span data-ttu-id="cd097-136">調達カテゴリまたは製品名別購買 (円柱グラフ)</span><span class="sxs-lookup"><span data-stu-id="cd097-136">Purchase by procurement category / product name (column chart)</span></span></li>
<li><span data-ttu-id="cd097-137">調達カテゴリまたは製品名 (円グラフ) 別購買合計</span><span class="sxs-lookup"><span data-stu-id="cd097-137">Total purchase by procurement category / product name (pie chart)</span></span></li>
<li><span data-ttu-id="cd097-138">購買別トップ 10 製品 (積み上げ棒グラフ)</span><span class="sxs-lookup"><span data-stu-id="cd097-138">Top 10 products by purchase (stacked bar chart)</span></span></li>
</ul></td>
<td><ul>
<li><span data-ttu-id="cd097-139">製品の合計数</span><span class="sxs-lookup"><span data-stu-id="cd097-139">Total # of products</span></span></li>
<li><span data-ttu-id="cd097-140">製品合計数の有効な製品の合計割合</span><span class="sxs-lookup"><span data-stu-id="cd097-140">Total active products percentage of total # of products</span></span></li>
<li><span data-ttu-id="cd097-141">購買の 80% を占める製品の数</span><span class="sxs-lookup"><span data-stu-id="cd097-141">Number of products accounting for 80% purchase</span></span></li>
</ul></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="cd097-142">期間別購買*</span><span class="sxs-lookup"><span data-stu-id="cd097-142">Purchase by period*</span></span></td>
<td><ul>
<li><span data-ttu-id="cd097-143">月/日別の購買 (円柱グラフ)</span><span class="sxs-lookup"><span data-stu-id="cd097-143">Purchase by month / day (column chart)</span></span></li>
<li><span data-ttu-id="cd097-144">累計購買金額の前年比差異 (伝播)</span><span class="sxs-lookup"><span data-stu-id="cd097-144">Cumulative purchase YOY variance (waterfall chart)</span></span></li>
<li><span data-ttu-id="cd097-145">合計購買金額の前年比成長 (円柱グラフ)</span><span class="sxs-lookup"><span data-stu-id="cd097-145">Total purchase YOY growth (column chart)</span></span></li>
<li><span data-ttu-id="cd097-146">調達明細書 (マトリックス)</span><span class="sxs-lookup"><span data-stu-id="cd097-146">Procurement statement (matrix)</span></span></li>
</ul></td>
<td><ul>
<li><span data-ttu-id="cd097-147">前年比購買成長</span><span class="sxs-lookup"><span data-stu-id="cd097-147">YOY purchase growth</span></span></li>
<li><span data-ttu-id="cd097-148">前年比購買成長の割合 %</span><span class="sxs-lookup"><span data-stu-id="cd097-148">YOY purchase growth %</span></span></li>
</ul></td>
</tr>
<tr class="even">
<td><span data-ttu-id="cd097-149">仕入先の場所別購買</span><span class="sxs-lookup"><span data-stu-id="cd097-149">Purchase by vendor location</span></span></td>
<td><ul>
<li><span data-ttu-id="cd097-150">市町村別の購買</span><span class="sxs-lookup"><span data-stu-id="cd097-150">Purchase by city</span></span></li>
<li><span data-ttu-id="cd097-151">購買額の前年比成長の割合 %</span><span class="sxs-lookup"><span data-stu-id="cd097-151">Purchase YOY growth %</span></span></li>
<li><span data-ttu-id="cd097-152">購買国</span><span class="sxs-lookup"><span data-stu-id="cd097-152">Purchase by country</span></span></li>
</ul></td>
<td></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="cd097-153">時間別購買先支出の分析</span><span class="sxs-lookup"><span data-stu-id="cd097-153">Purchase spend analysis by time</span></span></td>
<td><ul>
<li><span data-ttu-id="cd097-154">月/日別今年度の購買 (折れ線グラフ)</span><span class="sxs-lookup"><span data-stu-id="cd097-154">Purchase current year by month / day (line chart)</span></span></li>
<li><span data-ttu-id="cd097-155">今年度および昨年度の購買 (線と円柱グラフ)</span><span class="sxs-lookup"><span data-stu-id="cd097-155">Purchase current and last year (line and column chart)</span></span></li>
</ul></td>
<td></td>
</tr>
<tr class="even">
<td><span data-ttu-id="cd097-156">仕入先別購買先支出の分析</span><span class="sxs-lookup"><span data-stu-id="cd097-156">Purchase spend analysis by vendor</span></span></td>
<td><ul>
<li><span data-ttu-id="cd097-157">トップ 10 の仕入先の購買割合 % (じょうご)</span><span class="sxs-lookup"><span data-stu-id="cd097-157">Top 10 vendor purchase % of purchase (funnel)</span></span></li>
<li><span data-ttu-id="cd097-158">トップ 10 仕入先による増加支出額の前年比</span><span class="sxs-lookup"><span data-stu-id="cd097-158">Top 10 vendors with increased spending YOY</span></span></li>
<li><span data-ttu-id="cd097-159">トップ 10 仕入先による減少支出額の前年比</span><span class="sxs-lookup"><span data-stu-id="cd097-159">Top 10 vendors with decreased spending YOY</span></span></li>
</ul></td>
<td></td>
</tr>
</tbody>
</table>

<span data-ttu-id="cd097-160">\* 今年度と昨年度の購買、調達カテゴリによる成長</span><span class="sxs-lookup"><span data-stu-id="cd097-160">\* Purchase this year and last year, and growth by procurement category</span></span>

## <a name="extending-the-power-bi-content"></a><span data-ttu-id="cd097-161">Power BI コンテンツの拡張</span><span class="sxs-lookup"><span data-stu-id="cd097-161">Extending the Power BI content</span></span>
<span data-ttu-id="cd097-162">Microsoft Dynamics Lifecycle Services (LCS) で利用できるコンテンツ パックを使用すると、Microsoft Dynamics 365 にログインしない人々に関する優れた分析ができます。</span><span class="sxs-lookup"><span data-stu-id="cd097-162">By using the content packs that are available in Microsoft Dynamics Lifecycle Services (LCS), you can provide great analytics to people who don't sign in to Microsoft Dynamics 365.</span></span> <span data-ttu-id="cd097-163">ほかのレポートまたはビジュアルを含めるよう、これらのコンテンツ パックを変更できます。次いで分析のためにコンテンツ パックを Power BI.com テナントに発行します。</span><span class="sxs-lookup"><span data-stu-id="cd097-163">You can modify these content packs so that they include other reports or visuals, and then publish the content packs to your Power BI.com tenant for analysis.</span></span> 

<span data-ttu-id="cd097-164">LCS の共有資産ライブラリに [**購買と支出の分析**] Power BI コンテンツがあります。</span><span class="sxs-lookup"><span data-stu-id="cd097-164">You can find the **Purchase spend analysis** Power BI content in the Shared assets library in LCS.</span></span> <span data-ttu-id="cd097-165">コンテンツのダウンロード方法および組織で実装する方法の詳細については、「[Microsoft およびパートナーからの LCS での Power BI コンテンツ](power-bi-content-microsoft-partners.md)」を参照してください。</span><span class="sxs-lookup"><span data-stu-id="cd097-165">For more information about how to download the content and implement it in your organization, see [Power BI content in LCS from Microsoft and your partners](power-bi-content-microsoft-partners.md).</span></span> <span data-ttu-id="cd097-166">Power BI コンテンツの実装方法を示すデモを視聴するには、「[Microsoft の Power BI コンテンツおよび Dynamics Lifecycle Services のパートナー](https://mix.office.com/watch/9puyb1b2xs1w)」の Office Mix を参照してください。</span><span class="sxs-lookup"><span data-stu-id="cd097-166">To watch a demo that shows how to implement the Power BI content, see the [Power BI content from Microsoft and your partners in Dynamics Lifecycle Services](https://mix.office.com/watch/9puyb1b2xs1w) Office Mix.</span></span>

<span data-ttu-id="cd097-167">ご使用のバージョンの Microsoft Dynamics 365 に適用する [**購買と支出の分析**] コンテンツをダウンロードしてください。</span><span class="sxs-lookup"><span data-stu-id="cd097-167">Be sure to download the **Purchase spend analysis** content that applies to the version of Dynamics 365 that you're using.</span></span>

> [!NOTE]
> <span data-ttu-id="cd097-168">Microsoft Dynamics 365 for Operations バージョン 1611 を使用している場合、この Power BI コンテンツの前提条件はサポート技術情報 4011327 です。</span><span class="sxs-lookup"><span data-stu-id="cd097-168">If you're using Microsoft Dynamics 365 for Operations version 1611, KB 4011327 is a prerequisite for this Power BI content.</span></span> <span data-ttu-id="cd097-169">LCS にサインインすると、https://fix.lcs.dynamics.com/issue/results/?q=kb4011327 でサポート技術情報にアクセスできます。</span><span class="sxs-lookup"><span data-stu-id="cd097-169">After you sign in to LCS, you can access the KB at https://fix.lcs.dynamics.com/issue/results/?q=kb4011327.</span></span>

## <a name="data-model-and-entities"></a><span data-ttu-id="cd097-170">データ モデルおよびエンティティ</span><span class="sxs-lookup"><span data-stu-id="cd097-170">Data model and entities</span></span>
<span data-ttu-id="cd097-171">次のデータは、[**購買と支出の分析**] Power BI コンテンツのレポート ページに入力するために使用されます。</span><span class="sxs-lookup"><span data-stu-id="cd097-171">The following data is used to fill the report pages in the **Purchase spend analysis** Power BI content.</span></span> <span data-ttu-id="cd097-172">このデータは、エンティティ ストアで実施される集計の測定として表されます。</span><span class="sxs-lookup"><span data-stu-id="cd097-172">This data is represented as aggregate measurements that are staged in the Entity store.</span></span> <span data-ttu-id="cd097-173">エンティティ ストアは、分析に最適化された Microsoft SQL Server データベースです。</span><span class="sxs-lookup"><span data-stu-id="cd097-173">The Entity store is a Microsoft SQL Server database that is optimized for analytics.</span></span> <span data-ttu-id="cd097-174">詳細については、「[エンティティ ストアとの Power BI の統合](power-bi-integration-entity-store.md)」を参照してください。</span><span class="sxs-lookup"><span data-stu-id="cd097-174">For more information, see [Overview of Power BI integration with Entity store](power-bi-integration-entity-store.md).</span></span>

<span data-ttu-id="cd097-175">このコンテンツの集計の測定は Microsoft Dynamics AX 2012 および Microsoft Dynamics AX 2012 R3 の購買キューブに使用できた集計の測定のサブセットです。</span><span class="sxs-lookup"><span data-stu-id="cd097-175">The aggregate measurements in this content are the subset of aggregate measurements that were available in the Purchase Cube in Microsoft Dynamics AX 2012 and Microsoft Dynamics AX 2012 R3.</span></span> <span data-ttu-id="cd097-176">エンティティ格納でキューブの集計の測定を公開するには、それらを配置可能にする必要があります。</span><span class="sxs-lookup"><span data-stu-id="cd097-176">To stage the cube’s aggregate measurements in the Entity store, you must make them deployable.</span></span> <span data-ttu-id="cd097-177">詳細については、「[エンティティ ストアとの Power BI の統合](power-bi-integration-entity-store.md) ブログ投稿で、集計の測定をエンティティ格納へ公開する手順」を参照してください。</span><span class="sxs-lookup"><span data-stu-id="cd097-177">For more information, see the procedure for staging aggregate measurements in the Entity store in [Overview of Power BI integration with Entity store](power-bi-integration-entity-store.md).</span></span> <span data-ttu-id="cd097-178">次のキー集計の測定は、請求明細行エンティティから直接使用でき、コンテンツの基準として使用されます。</span><span class="sxs-lookup"><span data-stu-id="cd097-178">The following key aggregate measurements are available directly from the Invoice lines entity and are used as the basis of the content.</span></span>

| <span data-ttu-id="cd097-179">エンティティ</span><span class="sxs-lookup"><span data-stu-id="cd097-179">Entity</span></span>        | <span data-ttu-id="cd097-180">キー集計の測定</span><span class="sxs-lookup"><span data-stu-id="cd097-180">Key aggregate measurements</span></span> | <span data-ttu-id="cd097-181">データ ソース</span><span class="sxs-lookup"><span data-stu-id="cd097-181">Data source</span></span>                                 | <span data-ttu-id="cd097-182">フィールド</span><span class="sxs-lookup"><span data-stu-id="cd097-182">Field</span></span>              | <span data-ttu-id="cd097-183">説明</span><span class="sxs-lookup"><span data-stu-id="cd097-183">Description</span></span>                            |
|---------------|----------------------------|---------------------------------------------|--------------------|----------------------------------------|
| <span data-ttu-id="cd097-184">請求明細行</span><span class="sxs-lookup"><span data-stu-id="cd097-184">Invoice lines</span></span> | <span data-ttu-id="cd097-185">購買</span><span class="sxs-lookup"><span data-stu-id="cd097-185">Purchase</span></span>                   | <span data-ttu-id="cd097-186">VendInvoiceTrans</span><span class="sxs-lookup"><span data-stu-id="cd097-186">VendInvoiceTrans</span></span>                            | <span data-ttu-id="cd097-187">合計 (LineAmountMST) </span><span class="sxs-lookup"><span data-stu-id="cd097-187">SUM(LineAmountMST)</span></span> | <span data-ttu-id="cd097-188">会計通貨での金額。</span><span class="sxs-lookup"><span data-stu-id="cd097-188">The amount in the accounting currency.</span></span> |

<span data-ttu-id="cd097-189">次の表は、請求明細行のエンティティのコンテンツで計算される主要な測定単位を示します。</span><span class="sxs-lookup"><span data-stu-id="cd097-189">The following table shows the key measurements in the content that are calculated from the Invoice lines entity.</span></span>

| <span data-ttu-id="cd097-190">基準</span><span class="sxs-lookup"><span data-stu-id="cd097-190">Measure</span></span>               | <span data-ttu-id="cd097-191">計算</span><span class="sxs-lookup"><span data-stu-id="cd097-191">Calculation</span></span>                                                                                         |
|-----------------------|-----------------------------------------------------------------------------------------------------|
| <span data-ttu-id="cd097-192">今年度の購買</span><span class="sxs-lookup"><span data-stu-id="cd097-192">Purchase current year</span></span> | <span data-ttu-id="cd097-193">今年度の購買 = SUM('請求明細行'\[購買\])</span><span class="sxs-lookup"><span data-stu-id="cd097-193">Purchase current year = SUM('Invoice lines'\[Purchase\])</span></span>                                            |
| <span data-ttu-id="cd097-194">昨年度の購買</span><span class="sxs-lookup"><span data-stu-id="cd097-194">Purchase last year</span></span>    | <span data-ttu-id="cd097-195">昨年購買 = CALCULATE(合計 ('請求明細行'\[購買\]), SAMEPERIODLASTYEAR(日付\[日付\]))</span><span class="sxs-lookup"><span data-stu-id="cd097-195">Purchase last year = CALCULATE(SUM('Invoice lines'\[Purchase\]), SAMEPERIODLASTYEAR(Dates\[Date\]))</span></span> |
| <span data-ttu-id="cd097-196">前年比購買成長</span><span class="sxs-lookup"><span data-stu-id="cd097-196">YOY purchase growth</span></span>   | <span data-ttu-id="cd097-197">前年比購買成長 = \[今年度の購買\] – \[昨年度の購買\]</span><span class="sxs-lookup"><span data-stu-id="cd097-197">YOY purchase growth = \[Purchase current year\] – \[Purchase last year\]</span></span>                            |

<span data-ttu-id="cd097-198">コンテンツの以下のキー分析コードは、より高い粒度を達成し深い分析洞察を取得できるように、集計の測定をスライスするフィルターとして使用されます。</span><span class="sxs-lookup"><span data-stu-id="cd097-198">The following key dimensions in the content are used as filters to slice the aggregate measurements, so that you can achieve more granularity and gain deeper analytical insights.</span></span>

| <span data-ttu-id="cd097-199">エンティティ</span><span class="sxs-lookup"><span data-stu-id="cd097-199">Entity</span></span>                 | <span data-ttu-id="cd097-200">属性の例</span><span class="sxs-lookup"><span data-stu-id="cd097-200">Examples of attributes</span></span>                                |
|------------------------|-------------------------------------------------------|
| <span data-ttu-id="cd097-201">仕入先</span><span class="sxs-lookup"><span data-stu-id="cd097-201">Vendors</span></span>                | <span data-ttu-id="cd097-202">仕入先グループ、仕入先の国または地域、仕入先名</span><span class="sxs-lookup"><span data-stu-id="cd097-202">Vendor groups, Vendor country or regions, Vendor name</span></span> |
| <span data-ttu-id="cd097-203">製品</span><span class="sxs-lookup"><span data-stu-id="cd097-203">Products</span></span>               | <span data-ttu-id="cd097-204">製品番号、製品名、品目グループの名前</span><span class="sxs-lookup"><span data-stu-id="cd097-204">Product number, Product name, Item groups name</span></span>        |
| <span data-ttu-id="cd097-205">調達カテゴリ</span><span class="sxs-lookup"><span data-stu-id="cd097-205">Procurement categories</span></span> | <span data-ttu-id="cd097-206">調達カテゴリ、調達カテゴリの名前</span><span class="sxs-lookup"><span data-stu-id="cd097-206">Procurement category, Procurement category names</span></span>      |
| <span data-ttu-id="cd097-207">法人</span><span class="sxs-lookup"><span data-stu-id="cd097-207">Legal entities</span></span>         | <span data-ttu-id="cd097-208">法人名</span><span class="sxs-lookup"><span data-stu-id="cd097-208">Legal entity name</span></span>                                     |
| <span data-ttu-id="cd097-209">日付</span><span class="sxs-lookup"><span data-stu-id="cd097-209">Dates</span></span>                  | <span data-ttu-id="cd097-210">日付、年度相殺</span><span class="sxs-lookup"><span data-stu-id="cd097-210">Dates, Year offset</span></span>                                    |

<span data-ttu-id="cd097-211">既定では、コンテンツは、現在の暦年のデータが表示されます。</span><span class="sxs-lookup"><span data-stu-id="cd097-211">By default, the content shows data for the current calendar year.</span></span> <span data-ttu-id="cd097-212">ただし、レポートのフィルタ セクションの日付のフィルタを変更できます。</span><span class="sxs-lookup"><span data-stu-id="cd097-212">However, you can change the date filter in the report filters section.</span></span> <span data-ttu-id="cd097-213">会社フィルターを変更することもできます。</span><span class="sxs-lookup"><span data-stu-id="cd097-213">You can also change the company filter.</span></span>

