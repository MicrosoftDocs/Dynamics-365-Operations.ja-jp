---
title: "プラクティス マネージャー Power BI コンテンツ"
description: "このトピックでは、プラクティス マネージャー Power BI コンテンツの内容について説明します。 コンテンツに含まれているレポートにアクセスする方法を説明し、コンテンツを作成するために使用するデータ モデルおよびエンティティについての情報を提供します。"
author: KimANelson
manager: AnnBe
ms.date: 06/16/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-platform
ms.technology: 
audience: Application User, IT Pro
ms.reviewer: sericks
ms.search.scope: Core, Operations
ms.assetid: 
ms.search.region: Global
ms.author: knelson
ms.search.validFrom: 2017-06-30
ms.dyn365.ops.version: July 2017 update
ms.translationtype: HT
ms.sourcegitcommit: 2771a31b5a4d418a27de0ebe1945d1fed2d8d6d6
ms.openlocfilehash: 3462ef1bbde9a98ac6a7bc9a5c54e58ff98559c8
ms.contentlocale: ja-jp
ms.lasthandoff: 11/03/2017

---

# <a name="practice-manager-power-bi-content"></a><span data-ttu-id="aadbd-104">プラクティス マネージャー Power BI コンテンツ</span><span class="sxs-lookup"><span data-stu-id="aadbd-104">Practice manager Power BI content</span></span>

[!include[banner](../includes/banner.md)]

<span data-ttu-id="aadbd-105">このトピックでは、**プラクティス マネージャー** Microsoft Power BI コンテンツの内容について説明します。</span><span class="sxs-lookup"><span data-stu-id="aadbd-105">This topic describes what is included in the **Practice manager** Microsoft Power BI content.</span></span> <span data-ttu-id="aadbd-106">Power BI レポートにアクセスする方法を説明し、コンテンツを作成するために使用するデータ モデルおよびエンティティについての情報を提供します。</span><span class="sxs-lookup"><span data-stu-id="aadbd-106">It explains how to access the Power BI reports, and provides information about the data model and entities that are used to build the content.</span></span>

## <a name="overview"></a><span data-ttu-id="aadbd-107">概要</span><span class="sxs-lookup"><span data-stu-id="aadbd-107">Overview</span></span>

<span data-ttu-id="aadbd-108">**プラクティス マネージャー** Power BI コンテンツは、プラクティス マネージャーおよびプロジェクト マネージャー用に作成されました。</span><span class="sxs-lookup"><span data-stu-id="aadbd-108">The **Practice manager** Power BI content was created for practice managers and project managers.</span></span> <span data-ttu-id="aadbd-109">組織が取り組んでいるプロジェクトに関連した主要メトリックスが提供されます。</span><span class="sxs-lookup"><span data-stu-id="aadbd-109">It provides key metrics that are related to the projects that the organization is working on.</span></span> <span data-ttu-id="aadbd-110">ダッシュ ボードでは、プロジェクトおよび関連する顧客の概要を示します。</span><span class="sxs-lookup"><span data-stu-id="aadbd-110">The dashboard gives an overview of the projects and related customers.</span></span> <span data-ttu-id="aadbd-111">レポート レベルのフィルターは、特定の法人のレポートに使用できます。</span><span class="sxs-lookup"><span data-stu-id="aadbd-111">A report-level filter can be used to report for specific legal entities.</span></span> <span data-ttu-id="aadbd-112">この Power BI コンテンツは、プロジェクト会計集計の測定からデータを取得します。</span><span class="sxs-lookup"><span data-stu-id="aadbd-112">This Power BI content pulls data from the project accounting aggregate measurements.</span></span>

<span data-ttu-id="aadbd-113">[**プラクティス マネージャー**] Power BI コンテンツには、5 つのレポート ページが含まれます。1 つの概要ページと、プロジェクト原価、収益、達成額管理、および時間測定値の詳細を示す 4 つのページで、さまざまな分析コードに分割されています。</span><span class="sxs-lookup"><span data-stu-id="aadbd-113">The **Practice manager** Power BI content contains five report pages: one overview page, and four pages that provide details about project costs, revenues, earned value management, and hour metrics that are broken down across various dimensions.</span></span>

<span data-ttu-id="aadbd-114">コンテンツ内のすべての金額はシステム通貨で表示されます。</span><span class="sxs-lookup"><span data-stu-id="aadbd-114">All the amounts in the content are shown in the system currency.</span></span> <span data-ttu-id="aadbd-115">システム通貨は、[**システム パラメーター**] ページで設定できます。</span><span class="sxs-lookup"><span data-stu-id="aadbd-115">You can set the system currency on the **System parameters** page.</span></span>

## <a name="accessing-the-power-bi-content"></a><span data-ttu-id="aadbd-116">Power BI コンテンツへのアクセス</span><span class="sxs-lookup"><span data-stu-id="aadbd-116">Accessing the Power BI content</span></span>
<span data-ttu-id="aadbd-117">Microsoft Dynamics 365 for Finance and Operations, Enterprise edition (2017 年 7 月) を使用している場合、[**プラクティス マネージャー**] Power BI コンテンツは [**プロジェクト管理**] ワークスペースで表示されます。</span><span class="sxs-lookup"><span data-stu-id="aadbd-117">If you're using Microsoft Dynamics 365 for Finance and Operations, Enterprise edition (July 2017), the **Practice manager** Power BI content is shown in the **Project management** workspace.</span></span>

## <a name="reports-that-are-included-in-the-power-bi-content"></a><span data-ttu-id="aadbd-118">Power BI コンテンツに含まれるレポート</span><span class="sxs-lookup"><span data-stu-id="aadbd-118">Reports that are included in the Power BI content</span></span>

<span data-ttu-id="aadbd-119">次の表は、**プラクティス マネージャー** Power BI コンテンツの各レポート ページに表示されるメトリックスの詳細について説明しています。</span><span class="sxs-lookup"><span data-stu-id="aadbd-119">The following table provides details about the metrics that are found on each report page in the **Practice manager** Power BI content.</span></span>

| <span data-ttu-id="aadbd-120">レポート ページ</span><span class="sxs-lookup"><span data-stu-id="aadbd-120">Report page</span></span>       | <span data-ttu-id="aadbd-121">メトリックス</span><span class="sxs-lookup"><span data-stu-id="aadbd-121">Metrics</span></span> |
|-------------------|---------|
| <span data-ttu-id="aadbd-122">プロジェクトの概要</span><span class="sxs-lookup"><span data-stu-id="aadbd-122">Projects overview</span></span> | <ul><li><span data-ttu-id="aadbd-123">作成済プロジェクト</span><span class="sxs-lookup"><span data-stu-id="aadbd-123">Created projects</span></span></li><li><span data-ttu-id="aadbd-124">見積済のプロジェクト</span><span class="sxs-lookup"><span data-stu-id="aadbd-124">Estimated projects</span></span></li><li><span data-ttu-id="aadbd-125">処理中のプロジェクト</span><span class="sxs-lookup"><span data-stu-id="aadbd-125">In-process projects</span></span></li><li><span data-ttu-id="aadbd-126">ステージ別のプロジェクト数</span><span class="sxs-lookup"><span data-stu-id="aadbd-126">Number of projects by stage</span></span></li><li><span data-ttu-id="aadbd-127">都市別のプロジェクト数</span><span class="sxs-lookup"><span data-stu-id="aadbd-127">Number of projects by city</span></span></li><li><span data-ttu-id="aadbd-128">顧客別の実績収益</span><span class="sxs-lookup"><span data-stu-id="aadbd-128">Actual revenue by customer</span></span></li><li><span data-ttu-id="aadbd-129">プロジェクト別の予算粗利</span><span class="sxs-lookup"><span data-stu-id="aadbd-129">Budget gross margin by project</span></span></li><li><span data-ttu-id="aadbd-130">達成額管理の概要</span><span class="sxs-lookup"><span data-stu-id="aadbd-130">Earned value management overview</span></span></li></ul> |
| <span data-ttu-id="aadbd-131">コスト</span><span class="sxs-lookup"><span data-stu-id="aadbd-131">Cost</span></span>              | <ul><li><span data-ttu-id="aadbd-132">月別の [実際] 対 [予算原価]</span><span class="sxs-lookup"><span data-stu-id="aadbd-132">Actual vs. budget cost by month</span></span></li><li><span data-ttu-id="aadbd-133">年別の [実際] 対 [予算原価]</span><span class="sxs-lookup"><span data-stu-id="aadbd-133">Actual vs. budget cost by year</span></span></li><li><span data-ttu-id="aadbd-134">カテゴリ別の [実際] 対 [予算原価]</span><span class="sxs-lookup"><span data-stu-id="aadbd-134">Actual vs. budget cost by category</span></span></li><li><span data-ttu-id="aadbd-135">トランザクション タイプ別の実際原価</span><span class="sxs-lookup"><span data-stu-id="aadbd-135">Actual cost by transaction type</span></span></li></ul> |
| <span data-ttu-id="aadbd-136">収益</span><span class="sxs-lookup"><span data-stu-id="aadbd-136">Revenue</span></span>           | <ul><li><span data-ttu-id="aadbd-137">月別の実績収益</span><span class="sxs-lookup"><span data-stu-id="aadbd-137">Actual revenue by month</span></span></li><li><span data-ttu-id="aadbd-138">郵便番号別の実績収益</span><span class="sxs-lookup"><span data-stu-id="aadbd-138">Actual revenue by postal code</span></span></li><li><span data-ttu-id="aadbd-139">カテゴリ別の [実際] 対 [予算収益]</span><span class="sxs-lookup"><span data-stu-id="aadbd-139">Actual vs. budget revenue by category</span></span></li><li><span data-ttu-id="aadbd-140">顧客の業種別の実績収益</span><span class="sxs-lookup"><span data-stu-id="aadbd-140">Actual revenue by customer industry</span></span></li></ul> |
| <span data-ttu-id="aadbd-141">EVM</span><span class="sxs-lookup"><span data-stu-id="aadbd-141">EVM</span></span>               | <span data-ttu-id="aadbd-142">プロジェクト別の原価とスケジュール業績インデックス</span><span class="sxs-lookup"><span data-stu-id="aadbd-142">Cost and schedule performance index by project</span></span> |
| <span data-ttu-id="aadbd-143">時間</span><span class="sxs-lookup"><span data-stu-id="aadbd-143">Hours</span></span>             | <ul><li><span data-ttu-id="aadbd-144">[支払い請求可能な実績稼働時間数] 対 [支払請求可能な実績非稼動時間数] 対 [予算時間]</span><span class="sxs-lookup"><span data-stu-id="aadbd-144">Actual billable utilized hours vs. actual billable burden hours vs. budget hours</span></span></li><li><span data-ttu-id="aadbd-145">プロジェクト別の [支払い請求可能な実績稼働時間数] 対 [支払請求可能な実績非稼動時間数]</span><span class="sxs-lookup"><span data-stu-id="aadbd-145">Actual billable utilized hours vs. actual billable burden hours by project</span></span></li><li><span data-ttu-id="aadbd-146">リソース別の [支払い請求可能な実績稼働時間数] 対 [支払請求可能な実績非稼動時間数]</span><span class="sxs-lookup"><span data-stu-id="aadbd-146">Actual billable utilized hours vs. actual billable burden hours by resource</span></span></li><li><span data-ttu-id="aadbd-147">プロジェクト別の請求可能な実績時間の比率</span><span class="sxs-lookup"><span data-stu-id="aadbd-147">Actual billable hours ratio by project</span></span></li><li><span data-ttu-id="aadbd-148">リソース別の請求可能な実績時間数の比率</span><span class="sxs-lookup"><span data-stu-id="aadbd-148">Actual billable hours ratio by resource</span></span></li></ul> |

<span data-ttu-id="aadbd-149">これらすべてのレポートのグラフとタイルはフィルター処理し、ダッシュボードに固定することができます。</span><span class="sxs-lookup"><span data-stu-id="aadbd-149">The charts and tiles on all these reports can be filtered and pinned to the dashboard.</span></span> <span data-ttu-id="aadbd-150">Power BI のフィルター処理と固定方法の詳細については、「[ダッシュボードの作成およびコンフィギュレーション](https://powerbi.microsoft.com/en-us/guided-learning/powerbi-learning-4-2-create-configure-dashboards/)」を参照してください。</span><span class="sxs-lookup"><span data-stu-id="aadbd-150">For more information about how to filter and pin in Power BI, see [Create and configure a dashboard](https://powerbi.microsoft.com/en-us/guided-learning/powerbi-learning-4-2-create-configure-dashboards/).</span></span> <span data-ttu-id="aadbd-151">また、基になるデータをエクスポートする機能を使用するなら、視覚化で要約されている基になるデータをエクスポートすることができます。</span><span class="sxs-lookup"><span data-stu-id="aadbd-151">You can also use the Export underlying data functionality to export the underlying data that is summarized in a visualization.</span></span>

## <a name="extending-the-power-bi-content"></a><span data-ttu-id="aadbd-152">Power BI コンテンツの拡張</span><span class="sxs-lookup"><span data-stu-id="aadbd-152">Extending the Power BI content</span></span>
<span data-ttu-id="aadbd-153">Microsoft Dynamics Lifecycle Services (LCS) で利用できるコンテンツ パックを使用すると、Microsoft Dynamics 365 にログインしない人々に関する優れた分析ができます。</span><span class="sxs-lookup"><span data-stu-id="aadbd-153">By using the content packs that are available in Microsoft Dynamics Lifecycle Services (LCS), you can provide great analytics to people who don't sign in to Microsoft Dynamics 365.</span></span> <span data-ttu-id="aadbd-154">ほかのレポートまたはビジュアルを含める場合、および、Power BI.com テナント分析のためにそれらを発行するために、これらのコンテンツ パックを変更できます。</span><span class="sxs-lookup"><span data-stu-id="aadbd-154">You can modify these content packs so that they include other reports or visuals, and then publish them to your Power BI.com tenant for analysis.</span></span> 

<span data-ttu-id="aadbd-155">LCS の共有資産ライブラリに [**プラクティス マネージャー**] Power BI コンテンツがあります。</span><span class="sxs-lookup"><span data-stu-id="aadbd-155">You can find the **Practice manager** Power BI content in the Shared assets library in LCS.</span></span> <span data-ttu-id="aadbd-156">コンテンツのダウンロード方法および組織で実装する方法の詳細については、「[Microsoft およびパートナーからの LCS での Power BI コンテンツ](power-bi-content-microsoft-partners.md)」を参照してください。</span><span class="sxs-lookup"><span data-stu-id="aadbd-156">For more information about how to download the content and implement it in your organization, see [Power BI content in LCS from Microsoft and your partners](power-bi-content-microsoft-partners.md).</span></span> <span data-ttu-id="aadbd-157">Power BI コンテンツの実装方法を示すデモを視聴するには、「[Microsoft の Power BI コンテンツおよび Dynamics Lifecycle Services のパートナー](https://mix.office.com/watch/9puyb1b2xs1w)」の Office Mix を参照してください。</span><span class="sxs-lookup"><span data-stu-id="aadbd-157">To watch a demo that shows how to implement the Power BI content, see the [Power BI content from Microsoft and your partners in Dynamics Lifecycle Services](https://mix.office.com/watch/9puyb1b2xs1w) Office Mix.</span></span>

<span data-ttu-id="aadbd-158">使用している Dynamics 365 バージョンに適用される [**プラクティス マネージャー**] コンテンツをダウンロードしてください。</span><span class="sxs-lookup"><span data-stu-id="aadbd-158">Be sure to download the **Practice manager** content that applies to the version of Dynamics 365 that you're using.</span></span>

## <a name="understanding-the-data-model-and-entities"></a><span data-ttu-id="aadbd-159">データ モデルおよびエンティティの理解</span><span class="sxs-lookup"><span data-stu-id="aadbd-159">Understanding the data model and entities</span></span>

<span data-ttu-id="aadbd-160">次のデータは、[**プラクティス マネージャー**] Power BI コンテンツのレポート ページに入力するために使用されます。</span><span class="sxs-lookup"><span data-stu-id="aadbd-160">The following data is used to fill the report pages in the **Practice manager** Power BI content.</span></span> <span data-ttu-id="aadbd-161">このデータは、エンティティ ストアで実施される集計の測定として表されます。</span><span class="sxs-lookup"><span data-stu-id="aadbd-161">This data is represented as aggregate measurements that are staged in the Entity store.</span></span> <span data-ttu-id="aadbd-162">エンティティ ストアは、分析に最適化された Microsoft SQL Server データベースです。</span><span class="sxs-lookup"><span data-stu-id="aadbd-162">The Entity store is a Microsoft SQL Server database that is optimized for analytics.</span></span> <span data-ttu-id="aadbd-163">詳細については、「[エンティティ ストアとの Power BI の統合](power-bi-integration-entity-store.md)」を参照してください。</span><span class="sxs-lookup"><span data-stu-id="aadbd-163">For more information, see [Overview of Power BI integration with Entity store](power-bi-integration-entity-store.md).</span></span>

<span data-ttu-id="aadbd-164">次のセクションでは、各エンティティで使用される集計の測定について説明します。</span><span class="sxs-lookup"><span data-stu-id="aadbd-164">The following sections describe the aggregate measurements that are used in each entity.</span></span>

### <a name="entity-projectaccountingcubeactualhourutilization"></a><span data-ttu-id="aadbd-165">エンティティ: ProjectAccountingCube_ActualHourUtilization</span><span class="sxs-lookup"><span data-stu-id="aadbd-165">Entity: ProjectAccountingCube_ActualHourUtilization</span></span>
<span data-ttu-id="aadbd-166">[**データ ソース:**] ProjEmplTrans</span><span class="sxs-lookup"><span data-stu-id="aadbd-166">**Data source:** ProjEmplTrans</span></span>

| <span data-ttu-id="aadbd-167">キー集計の測定</span><span class="sxs-lookup"><span data-stu-id="aadbd-167">Key aggregate measurement</span></span>      | <span data-ttu-id="aadbd-168">フィールド</span><span class="sxs-lookup"><span data-stu-id="aadbd-168">Field</span></span>                              | <span data-ttu-id="aadbd-169">説明</span><span class="sxs-lookup"><span data-stu-id="aadbd-169">Description</span></span> | 
|--------------------------------|------------------------------------|-------------|
| <span data-ttu-id="aadbd-170">支払い請求可能な実績稼働時間数</span><span class="sxs-lookup"><span data-stu-id="aadbd-170">Actual billable utilized hours</span></span> | <span data-ttu-id="aadbd-171">Sum(ActualUtilizationBillableRate)</span><span class="sxs-lookup"><span data-stu-id="aadbd-171">Sum(ActualUtilizationBillableRate)</span></span> | <span data-ttu-id="aadbd-172">支払い請求可能な実績稼働時間数の合計。</span><span class="sxs-lookup"><span data-stu-id="aadbd-172">The total of actual billable utilized hours.</span></span> |
| <span data-ttu-id="aadbd-173">支払請求可能な実績非稼動時間数</span><span class="sxs-lookup"><span data-stu-id="aadbd-173">Actual billable burden hours</span></span>   | <span data-ttu-id="aadbd-174">Sum(ActualBurdenBillableRate)</span><span class="sxs-lookup"><span data-stu-id="aadbd-174">Sum(ActualBurdenBillableRate)</span></span>      | <span data-ttu-id="aadbd-175">実績非稼動の比率の合計。</span><span class="sxs-lookup"><span data-stu-id="aadbd-175">The total of the actual burden rate.</span></span> |

### <a name="entity-projectaccountingcubeactuals"></a><span data-ttu-id="aadbd-176">エンティティ: ProjectAccountingCube_Actuals</span><span class="sxs-lookup"><span data-stu-id="aadbd-176">Entity: ProjectAccountingCube_Actuals</span></span>
<span data-ttu-id="aadbd-177">[**データ ソース:**] ProjTransPosting</span><span class="sxs-lookup"><span data-stu-id="aadbd-177">**Data source:** ProjTransPosting</span></span>

| <span data-ttu-id="aadbd-178">キー集計の測定</span><span class="sxs-lookup"><span data-stu-id="aadbd-178">Key aggregate measurement</span></span> | <span data-ttu-id="aadbd-179">フィールド</span><span class="sxs-lookup"><span data-stu-id="aadbd-179">Field</span></span>              | <span data-ttu-id="aadbd-180">説明</span><span class="sxs-lookup"><span data-stu-id="aadbd-180">Description</span></span> | 
|---------------------------|--------------------|-------------|
| <span data-ttu-id="aadbd-181">実績収益</span><span class="sxs-lookup"><span data-stu-id="aadbd-181">Actual revenue</span></span>            | <span data-ttu-id="aadbd-182">Sum(ActualRevenue)</span><span class="sxs-lookup"><span data-stu-id="aadbd-182">Sum(ActualRevenue)</span></span> | <span data-ttu-id="aadbd-183">全トランザクションの転記済収益の合計。</span><span class="sxs-lookup"><span data-stu-id="aadbd-183">The total of posted revenue for all transactions.</span></span> |   
| <span data-ttu-id="aadbd-184">実際原価</span><span class="sxs-lookup"><span data-stu-id="aadbd-184">Actual cost</span></span>               | <span data-ttu-id="aadbd-185">Sum(ActualCost)</span><span class="sxs-lookup"><span data-stu-id="aadbd-185">Sum(ActualCost)</span></span>    | <span data-ttu-id="aadbd-186">全トランザクション タイプの転記済原価の合計。</span><span class="sxs-lookup"><span data-stu-id="aadbd-186">The total of posted cost for all transaction types.</span></span> |

### <a name="entity-projectaccountingcubecustomer"></a><span data-ttu-id="aadbd-187">エンティティ: ProjectAccountingCube_Customer</span><span class="sxs-lookup"><span data-stu-id="aadbd-187">Entity: ProjectAccountingCube_Customer</span></span>
<span data-ttu-id="aadbd-188">[**データ ソース:**] CustTable</span><span class="sxs-lookup"><span data-stu-id="aadbd-188">**Data source:** CustTable</span></span>

| <span data-ttu-id="aadbd-189">キー集計の測定</span><span class="sxs-lookup"><span data-stu-id="aadbd-189">Key aggregate measurement</span></span> | <span data-ttu-id="aadbd-190">フィールド</span><span class="sxs-lookup"><span data-stu-id="aadbd-190">Field</span></span>                                            | <span data-ttu-id="aadbd-191">説明</span><span class="sxs-lookup"><span data-stu-id="aadbd-191">Description</span></span> | 
|---------------------------|--------------------------------------------------|-------------|
| <span data-ttu-id="aadbd-192">プロジェクト数</span><span class="sxs-lookup"><span data-stu-id="aadbd-192">Number of projects</span></span>        | <span data-ttu-id="aadbd-193">COUNTA(ProjectAccountingCube_Projects[PROJECTS])</span><span class="sxs-lookup"><span data-stu-id="aadbd-193">COUNTA(ProjectAccountingCube_Projects[PROJECTS])</span></span> | <span data-ttu-id="aadbd-194">使用可能なプロジェクトの数。</span><span class="sxs-lookup"><span data-stu-id="aadbd-194">The count of available projects.</span></span> |


### <a name="entity-projectaccountingcubeforecasts"></a><span data-ttu-id="aadbd-195">エンティティ: ProjectAccountingCube_Forecasts</span><span class="sxs-lookup"><span data-stu-id="aadbd-195">Entity: ProjectAccountingCube_Forecasts</span></span>
<span data-ttu-id="aadbd-196">[**データ ソース:**] ProjTransBudget</span><span class="sxs-lookup"><span data-stu-id="aadbd-196">**Data source:** ProjTransBudget</span></span>

| <span data-ttu-id="aadbd-197">キー集計の測定</span><span class="sxs-lookup"><span data-stu-id="aadbd-197">Key aggregate measurement</span></span> | <span data-ttu-id="aadbd-198">フィールド</span><span class="sxs-lookup"><span data-stu-id="aadbd-198">Field</span></span>                  | <span data-ttu-id="aadbd-199">説明</span><span class="sxs-lookup"><span data-stu-id="aadbd-199">Description</span></span> | 
|---------------------------|------------------------|-------------|
| <span data-ttu-id="aadbd-200">予算原価</span><span class="sxs-lookup"><span data-stu-id="aadbd-200">Budget cost</span></span>               | <span data-ttu-id="aadbd-201">Sum(BudgetCost)</span><span class="sxs-lookup"><span data-stu-id="aadbd-201">Sum(BudgetCost)</span></span>        | <span data-ttu-id="aadbd-202">全トランザクション タイプの予測原価の合計。</span><span class="sxs-lookup"><span data-stu-id="aadbd-202">The total of forecast cost for all transaction types.</span></span> |
| <span data-ttu-id="aadbd-203">予算収益</span><span class="sxs-lookup"><span data-stu-id="aadbd-203">Budget revenue</span></span>            | <span data-ttu-id="aadbd-204">Sum(BudgetRevenue)</span><span class="sxs-lookup"><span data-stu-id="aadbd-204">Sum(BudgetRevenue)</span></span>     | <span data-ttu-id="aadbd-205">未収 / 請求済み予測収益の合計。</span><span class="sxs-lookup"><span data-stu-id="aadbd-205">The total of forecast accrued/invoiced revenue.</span></span>  |
| <span data-ttu-id="aadbd-206">予算粗利</span><span class="sxs-lookup"><span data-stu-id="aadbd-206">Budget gross margin</span></span>       | <span data-ttu-id="aadbd-207">Sum(BudgetGrossMargin)</span><span class="sxs-lookup"><span data-stu-id="aadbd-207">Sum(BudgetGrossMargin)</span></span> | <span data-ttu-id="aadbd-208">全予測収益の合計と全予測原価の合計の差額。</span><span class="sxs-lookup"><span data-stu-id="aadbd-208">The difference between the sum of total forecast revenue and the sum of total forecast cost.</span></span> |

### <a name="entity-projectaccountingcubeprojectplancostsview"></a><span data-ttu-id="aadbd-209">エンティティ: ProjectAccountingCube_ProjectPlanCostsView</span><span class="sxs-lookup"><span data-stu-id="aadbd-209">Entity: ProjectAccountingCube_ProjectPlanCostsView</span></span>
<span data-ttu-id="aadbd-210">[**データ ソース:**] プロジェクト</span><span class="sxs-lookup"><span data-stu-id="aadbd-210">**Data source:** Project</span></span>

| <span data-ttu-id="aadbd-211">キー集計の測定</span><span class="sxs-lookup"><span data-stu-id="aadbd-211">Key aggregate measurement</span></span> | <span data-ttu-id="aadbd-212">フィールド</span><span class="sxs-lookup"><span data-stu-id="aadbd-212">Field</span></span>                    | <span data-ttu-id="aadbd-213">説明</span><span class="sxs-lookup"><span data-stu-id="aadbd-213">Description</span></span> | 
|---------------------------|--------------------------|-------------|
| <span data-ttu-id="aadbd-214">予定原価</span><span class="sxs-lookup"><span data-stu-id="aadbd-214">Planned cost</span></span>              | <span data-ttu-id="aadbd-215">Sum(SumOfTotalCostPrice)</span><span class="sxs-lookup"><span data-stu-id="aadbd-215">Sum(SumOfTotalCostPrice)</span></span> | <span data-ttu-id="aadbd-216">計画タスクのすべてのプロジェクト トランザクション タイプにおける合計原価価格の見積。</span><span class="sxs-lookup"><span data-stu-id="aadbd-216">The total cost price in estimates for all project transaction types that have planned tasks.</span></span> |

### <a name="entity-projectaccountingcubeprojects"></a><span data-ttu-id="aadbd-217">エンティティ: ProjectAccountingCube_Projects</span><span class="sxs-lookup"><span data-stu-id="aadbd-217">Entity: ProjectAccountingCube_Projects</span></span>
<span data-ttu-id="aadbd-218">[**データ ソース:**] プロジェクト</span><span class="sxs-lookup"><span data-stu-id="aadbd-218">**Data source:** Project</span></span>

| <span data-ttu-id="aadbd-219">キー集計の測定</span><span class="sxs-lookup"><span data-stu-id="aadbd-219">Key aggregate measurement</span></span>    | <span data-ttu-id="aadbd-220">フィールド</span><span class="sxs-lookup"><span data-stu-id="aadbd-220">Field</span></span> | <span data-ttu-id="aadbd-221">説明</span><span class="sxs-lookup"><span data-stu-id="aadbd-221">Description</span></span> | 
|------------------------------|-------|-------------|
| <span data-ttu-id="aadbd-222">コスト パフォーマンス インデックス</span><span class="sxs-lookup"><span data-stu-id="aadbd-222">Cost performance index</span></span>       | <span data-ttu-id="aadbd-223">ProjectAccountingCube_Projects[達成額] / ProjectAccountingCube_Projects[完了済みのタスクの合計実際原価]</span><span class="sxs-lookup"><span data-stu-id="aadbd-223">ProjectAccountingCube_Projects[Earned value] / ProjectAccountingCube_Projects[Total actual cost of completed tasks]</span></span> | <span data-ttu-id="aadbd-224">合計達成額を合計実際原価で除算した計算。</span><span class="sxs-lookup"><span data-stu-id="aadbd-224">The calculation of the total earned value divided by the total actual cost.</span></span> |
| <span data-ttu-id="aadbd-225">スケジュール業績インデックス</span><span class="sxs-lookup"><span data-stu-id="aadbd-225">Schedule performance index</span></span>   | <span data-ttu-id="aadbd-226">ProjectAccountingCube_Projects[達成額] / ProjectAccountingCube_Projects[完了済みのタスクの合計予定原価]</span><span class="sxs-lookup"><span data-stu-id="aadbd-226">ProjectAccountingCube_Projects[Earned value] / ProjectAccountingCube_Projects[Total planned cost of completed tasks]</span></span> | <span data-ttu-id="aadbd-227">合計達成額を合計予定原価で除算した計算。</span><span class="sxs-lookup"><span data-stu-id="aadbd-227">The calculation of the total earned value divided by the total planned cost.</span></span> |
| <span data-ttu-id="aadbd-228">作業の完了率</span><span class="sxs-lookup"><span data-stu-id="aadbd-228">Percentage of work completed</span></span> | <span data-ttu-id="aadbd-229">作業の完了率 = ProjectAccountingCube_Projects[完了済みのタスクの合計実際原価] / (ProjectAccountingCube_Projects[完了済みのタスクの合計実際原価] + ProjectAccountingCube_Projects[プロジェクトの合計予定原価] - ProjectAccountingCube_Projects[完了済みのタスクの合計予定原価])</span><span class="sxs-lookup"><span data-stu-id="aadbd-229">Percentage of work completed = ProjectAccountingCube_Projects[Total actual cost of completed tasks] / (ProjectAccountingCube_Projects[Total actual cost of completed tasks] + ProjectAccountingCube_Projects[Total planned cost of project] - ProjectAccountingCube_Projects[Total planned cost of completed tasks])</span></span> | <span data-ttu-id="aadbd-230">完了タスクの合計実際原価およびプロジェクトの予定原価に基づいた作業の合計完了率。</span><span class="sxs-lookup"><span data-stu-id="aadbd-230">The total percentage of completed work, based on the total actual cost of completed tasks and the planned cost of the project.</span></span> |
| <span data-ttu-id="aadbd-231">支払請求可能な実績時間数の比率</span><span class="sxs-lookup"><span data-stu-id="aadbd-231">Actual billable hours ratio</span></span>  | <span data-ttu-id="aadbd-232">ProjectAccountingCube_Projects[プロジェクトの支払い請求可能な実績稼働時間数の合計] / (ProjectAccountingCube_Projects[プロジェクトの支払い請求可能な実績稼働時間数の合計] + ProjectAccountingCube_Projects[プロジェクトの支払い請求可能な実績非稼動時間数])</span><span class="sxs-lookup"><span data-stu-id="aadbd-232">ProjectAccountingCube_Projects[Project total actual billable utilized hours] / (ProjectAccountingCube_Projects[Project total actual billable utilized hours] + ProjectAccountingCube_Projects[Project total actual billable burden hours])</span></span> | <span data-ttu-id="aadbd-233">実績稼働時間数と実績非稼動時間数に基づいた支払請求可能な実績時間数の合計。</span><span class="sxs-lookup"><span data-stu-id="aadbd-233">The total actual billable hours, based on the utilized hours and the burden hours.</span></span> |
| <span data-ttu-id="aadbd-234">達成額</span><span class="sxs-lookup"><span data-stu-id="aadbd-234">Earned value</span></span>                 | <span data-ttu-id="aadbd-235">ProjectAccountingCube_Projects[プロジェクトの合計予定原価] * ProjectAccountingCube_Projects[作業の完了率]</span><span class="sxs-lookup"><span data-stu-id="aadbd-235">ProjectAccountingCube_Projects[Total planned cost of project] * ProjectAccountingCube_Projects[Percentage of work completed]</span></span> | <span data-ttu-id="aadbd-236">合計予定原価と作業の完了率の乗算。</span><span class="sxs-lookup"><span data-stu-id="aadbd-236">The total planned cost multiplied by the percentage of completed work.</span></span> |

### <a name="entity-projectaccountingcubetotalestimatedcosts"></a><span data-ttu-id="aadbd-237">エンティティ: ProjectAccountingCube_TotalEstimatedCosts</span><span class="sxs-lookup"><span data-stu-id="aadbd-237">Entity: ProjectAccountingCube_TotalEstimatedCosts</span></span> 
<span data-ttu-id="aadbd-238">[**データ ソース:**] ProjTable</span><span class="sxs-lookup"><span data-stu-id="aadbd-238">**Data source:** ProjTable</span></span>

| <span data-ttu-id="aadbd-239">キー集計の測定</span><span class="sxs-lookup"><span data-stu-id="aadbd-239">Key aggregate measurement</span></span>       | <span data-ttu-id="aadbd-240">フィールド</span><span class="sxs-lookup"><span data-stu-id="aadbd-240">Field</span></span>               | <span data-ttu-id="aadbd-241">説明</span><span class="sxs-lookup"><span data-stu-id="aadbd-241">Description</span></span> | 
|---------------------------------|---------------------|-------------|
| <span data-ttu-id="aadbd-242">完了した活動の予定原価</span><span class="sxs-lookup"><span data-stu-id="aadbd-242">Completed activity planned cost</span></span> | <span data-ttu-id="aadbd-243">Sum(TotalCostPrice)</span><span class="sxs-lookup"><span data-stu-id="aadbd-243">Sum(TotalCostPrice)</span></span> | <span data-ttu-id="aadbd-244">完了タスクのすべてのプロジェクト トランザクション タイプにおける合計原価価格の見積。</span><span class="sxs-lookup"><span data-stu-id="aadbd-244">The total cost price in estimates for all project transaction types that have completed tasks.</span></span> |
