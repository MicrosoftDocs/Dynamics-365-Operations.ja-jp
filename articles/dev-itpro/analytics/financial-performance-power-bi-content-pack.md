---
title: "財務パフォーマンス Power BI コンテンツ"
description: "このトピックでは、財務パフォーマンス Power BI コンテンツについて説明します。 含まれているダッシュボードおよびレポートについて説明し、コンテンツを作成するために使用したデータモデルとエンティティに関する情報を提供します。"
author: kweekley
manager: AnnBe
ms.date: 12/01/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-platform
ms.technology: 
audience: Application User, IT Pro
ms.reviewer: sericks
ms.search.scope: Core, Operations
ms.custom: 106233
ms.assetid: 517e6a88-e7a1-4398-9971-b22fa83306ba
ms.search.region: Global
ms.author: kweekley
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 6e64337f19600b18320550d91c134949c33af7b0
ms.openlocfilehash: 3638f5acf6a05ec419dc4308e861d95f0d7b2cea
ms.contentlocale: ja-jp
ms.lasthandoff: 12/01/2017

---

# <a name="financial-performance-power-bi-content"></a><span data-ttu-id="59066-104">財務パフォーマンス Power BI コンテンツ</span><span class="sxs-lookup"><span data-stu-id="59066-104">Financial performance Power BI content</span></span>

[!include[banner](../includes/banner.md)]

<span data-ttu-id="59066-105">このトピックでは、**財務パフォーマンス** Microsoft Power BI コンテンツについて説明します。</span><span class="sxs-lookup"><span data-stu-id="59066-105">This topic describes the **Financial performance** Microsoft Power BI content.</span></span> <span data-ttu-id="59066-106">含まれているダッシュボードおよびレポートについて説明し、コンテンツを作成するために使用したデータモデルとエンティティに関する情報を提供します。</span><span class="sxs-lookup"><span data-stu-id="59066-106">It describes the dashboard and reports that are included, and provides information about the data model and entities that were used to build the content.</span></span>

## <a name="accessing-the-power-bi-content"></a><span data-ttu-id="59066-107">Power BI コンテンツへのアクセス</span><span class="sxs-lookup"><span data-stu-id="59066-107">Accessing the Power BI content</span></span>

<span data-ttu-id="59066-108">**財務パフォーマンス** Power BIは、Microsoft Dynamics Lifecycle Services (LCS) および PowerBI.com からアクセスできます。</span><span class="sxs-lookup"><span data-stu-id="59066-108">You can access the **Financial performance** Power BI from Microsoft Dynamics Lifecycle Services (LCS) and from PowerBI.com.</span></span>

### <a name="available-from-lcs"></a><span data-ttu-id="59066-109">LCS から使用できます。</span><span class="sxs-lookup"><span data-stu-id="59066-109">Available from LCS</span></span>
<span data-ttu-id="59066-110">LCS から使用できる**財務パフォーマンス** Power BI コンテンツは、次のバージョンがサポートされています。</span><span class="sxs-lookup"><span data-stu-id="59066-110">The **Financial performance** Power BI content that is available from LCS supports the following versions:</span></span>

- <span data-ttu-id="59066-111">Microsoft Dynamics 365 for Finance and Operations、Enterprise Edition バージョン</span><span class="sxs-lookup"><span data-stu-id="59066-111">Microsoft Dynamics 365 for Finance and Operations, Enterprise edition versions</span></span>
- <span data-ttu-id="59066-112">Microsoft Dynamics 365 for Operations バージョン 1611</span><span class="sxs-lookup"><span data-stu-id="59066-112">Microsoft Dynamics 365 for Operations version 1611</span></span> 

<span data-ttu-id="59066-113">LCS の共有資産ライブラリに Power BI コンテンツがあります。</span><span class="sxs-lookup"><span data-stu-id="59066-113">You can find the Power BI content in the Shared asset library in LCS.</span></span> <span data-ttu-id="59066-114">コンテンツパックのダウンロード方法および組織で実装する方法の詳細については、「[Microsoft およびパートナーからの LCS での Power BI コンテンツ](power-bi-content-microsoft-partners.md)」を参照してください。</span><span class="sxs-lookup"><span data-stu-id="59066-114">For more information about how to download the content pack and implement it in your organization, see [Power BI content in LCS from Microsoft and your partners](power-bi-content-microsoft-partners.md).</span></span> <span data-ttu-id="59066-115">Power BI コンテンツの実装方法を示すデモを視聴するには、「[Microsoft の Power BI コンテンツおよび Dynamics Lifecycle Services のパートナー](https://mix.office.com/watch/9puyb1b2xs1w)」の Office Mix を参照してください。</span><span class="sxs-lookup"><span data-stu-id="59066-115">To watch a demo that shows how to implement the Power BI content, see the [Power BI content from Microsoft and your partners in Dynamics Lifecycle Services](https://mix.office.com/watch/9puyb1b2xs1w) Office Mix.</span></span>

### <a name="available-from-powerbicom"></a><span data-ttu-id="59066-116">PowerBI.com からアクセスできます。</span><span class="sxs-lookup"><span data-stu-id="59066-116">Available from PowerBI.com</span></span>
<span data-ttu-id="59066-117">**財務パフォーマンス** PowerBI.com から使用できる Power BI コンテンツは、Microsoft Dynamics AX バージョン 7.0 および 7.0.1 をサポートしています。</span><span class="sxs-lookup"><span data-stu-id="59066-117">The **Financial performance** Power BI content that is available from PowerBI.com supports Microsoft Dynamics AX versions 7.0 and 7.0.1.</span></span> <span data-ttu-id="59066-118">Dynamics AX データの接続および読み込み方法の詳細については、「[PowerBI.com からの Power BI コンテンツへのアクセス](power-bi-home-page.md)」を参照してください。</span><span class="sxs-lookup"><span data-stu-id="59066-118">For more information about how to connect and load your Dynamics AX data, see [Access Power BI content from PowerBI.com](power-bi-home-page.md).</span></span>

## <a name="main-account-setup"></a><span data-ttu-id="59066-119">主勘定の設定</span><span class="sxs-lookup"><span data-stu-id="59066-119">Main account setup</span></span>
<span data-ttu-id="59066-120">組織は負債と収益の勘定をレポートに正の金額として表示させるため、主勘定の設定が重要です。</span><span class="sxs-lookup"><span data-stu-id="59066-120">Because organizations want liabilities and revenue amounts to appear as positive amounts on reports, the setup of the main accounts is important.</span></span> <span data-ttu-id="59066-121">これらの主勘定を正の金額として表示するには、主勘定タイプを [**負債**] または [**収益**] に設定する必要があります。</span><span class="sxs-lookup"><span data-stu-id="59066-121">For these main accounts to appear as positive amounts, the main account type must be set to **Liability** or **Revenue**.</span></span> <span data-ttu-id="59066-122">これらの勘定タイプを使用すると、Power BI での報告は符号が逆になり、正として金額が表示されます。</span><span class="sxs-lookup"><span data-stu-id="59066-122">When these account types are used, reporting through Power BI will reverse the signs and show the amounts as positive.</span></span>

## <a name="dashboard-and-reports-that-are-included-in-the-power-bi-content"></a><span data-ttu-id="59066-123">Power BI コンテンツに含まれるダッシュボードおよびレポート</span><span class="sxs-lookup"><span data-stu-id="59066-123">Dashboard and reports that are included in the Power BI content</span></span>
<span data-ttu-id="59066-124">ダッシュボードには、基になるレポートに基づいて集計されたデータ タイルが含まれます。</span><span class="sxs-lookup"><span data-stu-id="59066-124">The dashboard contains summarized tiles of data that are based on underlying reports.</span></span> <span data-ttu-id="59066-125">各タイルには、組織のすべての会社間での今年度における集計情報が含まれます。</span><span class="sxs-lookup"><span data-stu-id="59066-125">Each tile contains summarized information for the current year across all companies in an organization.</span></span> <span data-ttu-id="59066-126">次にタイルの例を示します。</span><span class="sxs-lookup"><span data-stu-id="59066-126">Here are some of the tiles:</span></span>

- <span data-ttu-id="59066-127">現金</span><span class="sxs-lookup"><span data-stu-id="59066-127">Cash</span></span>
- <span data-ttu-id="59066-128">今年度の総収益</span><span class="sxs-lookup"><span data-stu-id="59066-128">Total Revenue this year</span></span>
- <span data-ttu-id="59066-129">今年度の経費合計</span><span class="sxs-lookup"><span data-stu-id="59066-129">Total Expenses this year</span></span>
- <span data-ttu-id="59066-130">今年度の純利益</span><span class="sxs-lookup"><span data-stu-id="59066-130">Net Income this year</span></span>
- <span data-ttu-id="59066-131">当座比率</span><span class="sxs-lookup"><span data-stu-id="59066-131">Quick Ratio</span></span>
- <span data-ttu-id="59066-132">勘定カテゴリごとの今年度合計経費</span><span class="sxs-lookup"><span data-stu-id="59066-132">Total Expenses this year by account category</span></span>
- <span data-ttu-id="59066-133">現在の比率</span><span class="sxs-lookup"><span data-stu-id="59066-133">Current Ratio</span></span>
- <span data-ttu-id="59066-134">[負債総資産比率]</span><span class="sxs-lookup"><span data-stu-id="59066-134">Debt to Total Assets</span></span>
- <span data-ttu-id="59066-135">実績対予測された収益</span><span class="sxs-lookup"><span data-stu-id="59066-135">Actual vs Forecasted Revenue</span></span>
- <span data-ttu-id="59066-136">今年度の請求収益</span><span class="sxs-lookup"><span data-stu-id="59066-136">Billed Revenue this Year</span></span>
- <span data-ttu-id="59066-137">今年度の営業経費の比率</span><span class="sxs-lookup"><span data-stu-id="59066-137">Operating expenses Ratio this year</span></span>
- <span data-ttu-id="59066-138">今年度利益率</span><span class="sxs-lookup"><span data-stu-id="59066-138">Profit Margin this year</span></span>
- <span data-ttu-id="59066-139">実績対予算の経費 – すべての会社</span><span class="sxs-lookup"><span data-stu-id="59066-139">Actual vs Budget Expenses – All companies</span></span>

<span data-ttu-id="59066-140">各タイルがサポート レポートによってサポートされます。</span><span class="sxs-lookup"><span data-stu-id="59066-140">Each tile is backed by a supporting report.</span></span> <span data-ttu-id="59066-141">これらのレポートには、詳細情報を提供するテーブルとグラフが含まれます。</span><span class="sxs-lookup"><span data-stu-id="59066-141">These reports contain both charts and tables that provide more information.</span></span> <span data-ttu-id="59066-142">次の表にレポートを示します。</span><span class="sxs-lookup"><span data-stu-id="59066-142">The following table describes the reports.</span></span>

| <span data-ttu-id="59066-143">レポート </span><span class="sxs-lookup"><span data-stu-id="59066-143">Report</span></span>                      | <span data-ttu-id="59066-144">レポートに含まれる情報</span><span class="sxs-lookup"><span data-stu-id="59066-144">Information that the report contains</span></span> |
|-----------------------------|--------------------------------------|
| <span data-ttu-id="59066-145">現金分析</span><span class="sxs-lookup"><span data-stu-id="59066-145">Cash Analysis</span></span>               | <span data-ttu-id="59066-146">法人による現金、四半期ごとの現金、合計現金および勘定ごとの現金</span><span class="sxs-lookup"><span data-stu-id="59066-146">Cash by legal entity, cash by quarter, total cash, and cash by account</span></span><blockquote>[!NOTE]<br><span data-ttu-id="59066-147">四半期ごとの現金は、第 1 四半期の合計の期首残高に含まれていません。</span><span class="sxs-lookup"><span data-stu-id="59066-147">The cash by quarter information doesn't include beginning balances in the total for the first quarter.</span></span> <span data-ttu-id="59066-148">これは四半期ごとに転記される新しいトランザクションの合計を表示します。</span><span class="sxs-lookup"><span data-stu-id="59066-148">It shows the total of new transactions that are posted in each quarter.</span></span></blockquote> |
| <span data-ttu-id="59066-149">現在の比率分析</span><span class="sxs-lookup"><span data-stu-id="59066-149">Current Ratio Analysis</span></span>      | <span data-ttu-id="59066-150">法人による現在の比率、四半期ごとの現在の比率、現在の流動資産および負債の残高</span><span class="sxs-lookup"><span data-stu-id="59066-150">Current ratio by legal entity, current ratio by quarter, and balances for current assets and current liabilities</span></span> |
| <span data-ttu-id="59066-151">当座比率の分析</span><span class="sxs-lookup"><span data-stu-id="59066-151">Quick Ratio Analysis</span></span>        | <span data-ttu-id="59066-152">法人による当座比率、四半期ごとの当座比率、現金残高、売掛金勘定および現在の負債</span><span class="sxs-lookup"><span data-stu-id="59066-152">Quick ratio by legal entity, quick ratio by quarter, and balances for cash, accounts receivable, and current liabilities</span></span> |
| <span data-ttu-id="59066-153">売却済商品の原価分析</span><span class="sxs-lookup"><span data-stu-id="59066-153">Cost of Goods Sold Analysis</span></span> | <span data-ttu-id="59066-154">法人による売却済商品の原価 (COGS)、四半期ごとの今年度および昨年度の COGS、法人による COGS から売上、COGS 合計、および売上に対する COGS の割合</span><span class="sxs-lookup"><span data-stu-id="59066-154">Cost of goods sold (COGS) by legal entity, COGS this year and last year by quarter, COGS to sales by legal entity, total COGS, and COGS to sales percentage</span></span> |
| <span data-ttu-id="59066-155">運営資金の分析</span><span class="sxs-lookup"><span data-stu-id="59066-155">Working Capital Analysis</span></span>    | <span data-ttu-id="59066-156">法人による運営資金、四半期ごとの運営資金、現在の流動資産、現在の負債、および総運営資金</span><span class="sxs-lookup"><span data-stu-id="59066-156">Working capital by legal entity, working capital by quarter, current assets, current liabilities, and total working capital</span></span> |
| <span data-ttu-id="59066-157">資産および負債の分析</span><span class="sxs-lookup"><span data-stu-id="59066-157">Asset and Debt Analysis</span></span>     | <span data-ttu-id="59066-158">総資産利益率および法人による負債総資産比率、負債総資産比率および四半期累計期間 (現時点までの) における総資産利益率、資産、および負債</span><span class="sxs-lookup"><span data-stu-id="59066-158">Return on total assets and debt to total assets by legal entity, debt to total assets and return on total assets quarter to date, assets, and liabilities</span></span> |
| <span data-ttu-id="59066-159">利益率の分析</span><span class="sxs-lookup"><span data-stu-id="59066-159">Profit Margin Analysis</span></span>      | <span data-ttu-id="59066-160">法人による実績および予算の利益率、四半期ごとの利益、利益率の割合、および利益率</span><span class="sxs-lookup"><span data-stu-id="59066-160">Actual and budget profit margin by legal entity, profit marking by quarter, profit margin percentage, and profit margin</span></span> |
| <span data-ttu-id="59066-161">純利益の分析</span><span class="sxs-lookup"><span data-stu-id="59066-161">Net Income Analysis</span></span>         | <span data-ttu-id="59066-162">法人による実績および予算純利益、今年度および昨年度の純利益、および純利益に対する経費の割合</span><span class="sxs-lookup"><span data-stu-id="59066-162">Actual and budget net income by legal entity, net income this year and last year, and expenses to net income percentage</span></span> |
| <span data-ttu-id="59066-163">収益の分析</span><span class="sxs-lookup"><span data-stu-id="59066-163">Earnings Analysis</span></span>           | <span data-ttu-id="59066-164">法人による実績と予算における金利税引き前利益 (EBIT)、今年度と昨年度の EBIT、収益に対する経費の割合、および実績および予算における収益に対する経費の割合</span><span class="sxs-lookup"><span data-stu-id="59066-164">Actual and budget earnings before interest and taxes (EBIT) by legal entity, EBIT this year and last year, expenses to revenue percentage, and actual and budget expenses to revenue</span></span> |
| <span data-ttu-id="59066-165">収益の分析</span><span class="sxs-lookup"><span data-stu-id="59066-165">Revenue Analysis</span></span>            | <span data-ttu-id="59066-166">総収益、法人による実績と予算の総収益、今年度および昨年度の総収益、法人による収益予算差異、この期間と最後の期間における総収益</span><span class="sxs-lookup"><span data-stu-id="59066-166">Total revenue, actual and budget total revenue by legal entity, total revenue this year and last year, revenue budget variance by legal entity, and total revenue this period and last period</span></span> |
| <span data-ttu-id="59066-167">経費の分析</span><span class="sxs-lookup"><span data-stu-id="59066-167">Expense Analysis</span></span>            | <span data-ttu-id="59066-168">経費の合計金額、法人による合計経費予算に対する実績金額、四半期ごとの合計経費予算、勘定カテゴリごとの合計経費、および営業経費の比率</span><span class="sxs-lookup"><span data-stu-id="59066-168">Total expenses, actual to budget total expenses by legal entity, actual and budget total expense by quarter, total expenses by account category, and operating expenses ratio</span></span> |
| <span data-ttu-id="59066-169">請求収益の分析</span><span class="sxs-lookup"><span data-stu-id="59066-169">Billed Revenue Analysis</span></span>     | <span data-ttu-id="59066-170">売掛金勘定の合計、法人による売掛金勘定の合計、四半期ごとの売掛金勘定の合計、売掛金勘定の勘定残高</span><span class="sxs-lookup"><span data-stu-id="59066-170">Total accounts receivable, total accounts receivable by legal entity, total accounts receivable by quarter, and balances for accounts receivable accounts</span></span><blockquote>[!NOTE]<br><span data-ttu-id="59066-171">第 1 四半期の売掛金勘定の勘定科目は、情報に含まれていません。</span><span class="sxs-lookup"><span data-stu-id="59066-171">The information doesn't include beginning balances for the accounts receivable ledger accounts.</span></span> <span data-ttu-id="59066-172">売掛金勘定に転記される新しいトランザクションの合計を表示します。</span><span class="sxs-lookup"><span data-stu-id="59066-172">It shows the total of new transactions that are posted to Accounts receivable.</span></span></blockquote> |

<span data-ttu-id="59066-173">これらすべてのレポートのグラフとタイルはフィルター処理し、ダッシュボードに固定することができます。</span><span class="sxs-lookup"><span data-stu-id="59066-173">The charts and tiles on all these reports can be filtered and pinned to the dashboard.</span></span> <span data-ttu-id="59066-174">Power BI のフィルター処理と固定方法の詳細については、[ダッシュボードの作成およびコンフィギュレーション](https://powerbi.microsoft.com/en-us/guided-learning/powerbi-learning-4-2-create-configure-dashboards) を参照してください。</span><span class="sxs-lookup"><span data-stu-id="59066-174">For more information about how to filter and pin in Power BI, see [Create and Configure a Dashboard](https://powerbi.microsoft.com/en-us/guided-learning/powerbi-learning-4-2-create-configure-dashboards).</span></span>

## <a name="understanding-the-data-model-and-entities"></a><span data-ttu-id="59066-175">データ モデルおよびエンティティの理解</span><span class="sxs-lookup"><span data-stu-id="59066-175">Understanding the data model and entities</span></span>
<span data-ttu-id="59066-176">次のエンティティは**財務パフォーマンス** Power BI コンテンツの基準として使用されていました。</span><span class="sxs-lookup"><span data-stu-id="59066-176">The following entities were used as the basis of the **Financial performance** Power BI content:</span></span>

<span data-ttu-id="59066-177">**データ エンティティの集計**</span><span class="sxs-lookup"><span data-stu-id="59066-177">**Aggregate data entities**</span></span>

- <span data-ttu-id="59066-178">**GeneralLedgerActivities** – このエンティティは、勘定カテゴリの総勘定元帳の残高を集計します。</span><span class="sxs-lookup"><span data-stu-id="59066-178">**GeneralLedgerActivities** – This entity aggregates general ledger balances by account category.</span></span>
- <span data-ttu-id="59066-179">**BudgetActivities** – このエンティティは、勘定カテゴリの予算残高を集計します。</span><span class="sxs-lookup"><span data-stu-id="59066-179">**BudgetActivities** – This entity aggregates budget balances by account category.</span></span>

<span data-ttu-id="59066-180">**データ エンティティ**</span><span class="sxs-lookup"><span data-stu-id="59066-180">**Data entities**</span></span>

- <span data-ttu-id="59066-181">FiscalCalendars</span><span class="sxs-lookup"><span data-stu-id="59066-181">FiscalCalendars</span></span>
- <span data-ttu-id="59066-182">MainAccounts</span><span class="sxs-lookup"><span data-stu-id="59066-182">MainAccounts</span></span>
- <span data-ttu-id="59066-183">LegalEntities</span><span class="sxs-lookup"><span data-stu-id="59066-183">LegalEntities</span></span>
- <span data-ttu-id="59066-184">元帳</span><span class="sxs-lookup"><span data-stu-id="59066-184">Ledgers</span></span>
- <span data-ttu-id="59066-185">ChartofAccounts</span><span class="sxs-lookup"><span data-stu-id="59066-185">ChartofAccounts</span></span>

<span data-ttu-id="59066-186">これらのエンティティは、データ モデルの計算メジャーを作成するために使用されました。</span><span class="sxs-lookup"><span data-stu-id="59066-186">These entities were used to create calculated measures in the data model.</span></span> <span data-ttu-id="59066-187">計算メジャーは、主要業績評価指標 (KPI) およびコンテンツで使用されるレポートを計算するために使用されます。</span><span class="sxs-lookup"><span data-stu-id="59066-187">The calculated measures are used to calculate the key performance indicators (KPIs) and reports that are used in the content.</span></span> <span data-ttu-id="59066-188">既定では、コンテンツにより、過去 3 年間および将来 1 年間のデータが取得されます。</span><span class="sxs-lookup"><span data-stu-id="59066-188">By default, the content brings in data for the last three years and one future year.</span></span> <span data-ttu-id="59066-189">追加の計算をレポートおよびダッシュボードに含めるには、[Microsoft Excel ワークブック](https://mbs.microsoft.com/customersource/global/AX/downloads/reports/msdaxfinpercontentpowerbi) を変更できます。</span><span class="sxs-lookup"><span data-stu-id="59066-189">To include additional calculations on your reports and dashboard, you can modify the [Microsoft Excel workbook](https://mbs.microsoft.com/customersource/global/AX/downloads/reports/msdaxfinpercontentpowerbi).</span></span> <span data-ttu-id="59066-190">このワークブックはコンテンツを作成するために使用された既定のデータ モデルです。</span><span class="sxs-lookup"><span data-stu-id="59066-190">This workbook is the default data model that was used to create the content.</span></span> <span data-ttu-id="59066-191">自分の変更が終了した後に、追加した情報を含む組織のコンテンツ パックとダッシュボードを作成できます。</span><span class="sxs-lookup"><span data-stu-id="59066-191">After you've finished making your modifications, you can create an organizational content pack and dashboard that contain the information that you’ve added.</span></span>

