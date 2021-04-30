---
title: 財務パフォーマンス PowerBI.com ソリューション
description: このトピックでは、財務パフォーマンス PowerBI.com ソリューションについて説明します。
author: kweekley
ms.date: 05/09/2018
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User, IT Pro
ms.reviewer: kfend
ms.custom: 106233
ms.assetid: 517e6a88-e7a1-4398-9971-b22fa83306ba
ms.search.region: Global
ms.author: kweekley
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 953f477e7e00cde7f814ff28d3dfd8ed7075dafc
ms.sourcegitcommit: 951393b05bf409333cb3c7ad977bcaa804aa801b
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/13/2021
ms.locfileid: "5893229"
---
# <a name="financial-performance-powerbicom-solution"></a><span data-ttu-id="02a26-103">財務パフォーマンス PowerBI.com ソリューション</span><span class="sxs-lookup"><span data-stu-id="02a26-103">Financial performance PowerBI.com solution</span></span>

[!include [banner](../includes/banner.md)]

> [!NOTE]
> <span data-ttu-id="02a26-104">この PowerBI.com ソリューションは、[Finance and Operations の削除済みまたは非推奨の機能](../migration-upgrade/deprecated-features.md#power-bi-content-packs-available-on-appsource) に記載されている通り非推奨となっています。.</span><span class="sxs-lookup"><span data-stu-id="02a26-104">This PowerBI.com solution has been deprecated as documented in [Removed or deprecated features for Finance and Operations](../migration-upgrade/deprecated-features.md#power-bi-content-packs-available-on-appsource).</span></span>

<span data-ttu-id="02a26-105">このトピックでは、**財務パフォーマンス** PowerBI.com ソリューションについて説明します。</span><span class="sxs-lookup"><span data-stu-id="02a26-105">This topic describes the **Financial performance** PowerBI.com solution.</span></span> <span data-ttu-id="02a26-106">含まれているダッシュボードおよびレポートについて説明し、ソリューションを作成するために使用したデータ モデルとエンティティに関する情報を提供します。</span><span class="sxs-lookup"><span data-stu-id="02a26-106">It describes the dashboard and reports that are included, and provides information about the data model and entities that were used to build the solution.</span></span>

## <a name="main-account-setup"></a><span data-ttu-id="02a26-107">主勘定の設定</span><span class="sxs-lookup"><span data-stu-id="02a26-107">Main account setup</span></span>
<span data-ttu-id="02a26-108">組織は負債と収益の勘定をレポートに正の金額として表示させるため、主勘定の設定が重要です。</span><span class="sxs-lookup"><span data-stu-id="02a26-108">Because organizations want liabilities and revenue amounts to appear as positive amounts on reports, the setup of the main accounts is important.</span></span> <span data-ttu-id="02a26-109">これらの主勘定を正の金額として表示するには、主勘定タイプを **負債** または **収益** に設定する必要があります。</span><span class="sxs-lookup"><span data-stu-id="02a26-109">For these main accounts to appear as positive amounts, the main account type must be set to **Liability** or **Revenue**.</span></span> <span data-ttu-id="02a26-110">これらの勘定タイプを使用すると、Power BI での報告は符号が逆になり、正として金額が表示されます。</span><span class="sxs-lookup"><span data-stu-id="02a26-110">When these account types are used, reporting through Power BI will reverse the signs and show the amounts as positive.</span></span>

## <a name="dashboard-and-reports-that-are-included-in-the-powerbicom-solution"></a><span data-ttu-id="02a26-111">PowerBI.com ソリューションに含まれるダッシュボードおよびレポート</span><span class="sxs-lookup"><span data-stu-id="02a26-111">Dashboard and reports that are included in the PowerBI.com solution</span></span>
<span data-ttu-id="02a26-112">ダッシュボードには、基になるレポートに基づいて集計されたデータ タイルが含まれます。</span><span class="sxs-lookup"><span data-stu-id="02a26-112">The dashboard contains summarized tiles of data that are based on underlying reports.</span></span> <span data-ttu-id="02a26-113">各タイルには、組織のすべての会社間での今年度における集計情報が含まれます。</span><span class="sxs-lookup"><span data-stu-id="02a26-113">Each tile contains summarized information for the current year across all companies in an organization.</span></span> <span data-ttu-id="02a26-114">次にタイルの例を示します。</span><span class="sxs-lookup"><span data-stu-id="02a26-114">Here are some of the tiles:</span></span>

- <span data-ttu-id="02a26-115">現金</span><span class="sxs-lookup"><span data-stu-id="02a26-115">Cash</span></span>
- <span data-ttu-id="02a26-116">今年度の総収益</span><span class="sxs-lookup"><span data-stu-id="02a26-116">Total Revenue this year</span></span>
- <span data-ttu-id="02a26-117">今年度の経費合計</span><span class="sxs-lookup"><span data-stu-id="02a26-117">Total Expenses this year</span></span>
- <span data-ttu-id="02a26-118">今年度の純利益</span><span class="sxs-lookup"><span data-stu-id="02a26-118">Net Income this year</span></span>
- <span data-ttu-id="02a26-119">当座比率</span><span class="sxs-lookup"><span data-stu-id="02a26-119">Quick Ratio</span></span>
- <span data-ttu-id="02a26-120">勘定カテゴリごとの今年度合計経費</span><span class="sxs-lookup"><span data-stu-id="02a26-120">Total Expenses this year by account category</span></span>
- <span data-ttu-id="02a26-121">現在の比率</span><span class="sxs-lookup"><span data-stu-id="02a26-121">Current Ratio</span></span>
- <span data-ttu-id="02a26-122">[負債総資産比率]</span><span class="sxs-lookup"><span data-stu-id="02a26-122">Debt to Total Assets</span></span>
- <span data-ttu-id="02a26-123">実績対予測された収益</span><span class="sxs-lookup"><span data-stu-id="02a26-123">Actual vs Forecasted Revenue</span></span>
- <span data-ttu-id="02a26-124">今年度の請求収益</span><span class="sxs-lookup"><span data-stu-id="02a26-124">Billed Revenue this Year</span></span>
- <span data-ttu-id="02a26-125">今年度の営業経費の比率</span><span class="sxs-lookup"><span data-stu-id="02a26-125">Operating expenses Ratio this year</span></span>
- <span data-ttu-id="02a26-126">今年度利益率</span><span class="sxs-lookup"><span data-stu-id="02a26-126">Profit Margin this year</span></span>
- <span data-ttu-id="02a26-127">実績対予算の経費 – すべての会社</span><span class="sxs-lookup"><span data-stu-id="02a26-127">Actual vs Budget Expenses – All companies</span></span>

<span data-ttu-id="02a26-128">各タイルがサポート レポートによってサポートされます。</span><span class="sxs-lookup"><span data-stu-id="02a26-128">Each tile is backed by a supporting report.</span></span> <span data-ttu-id="02a26-129">これらのレポートには、詳細情報を提供するテーブルとグラフが含まれます。</span><span class="sxs-lookup"><span data-stu-id="02a26-129">These reports contain both charts and tables that provide more information.</span></span> <span data-ttu-id="02a26-130">次の表にレポートを示します。</span><span class="sxs-lookup"><span data-stu-id="02a26-130">The following table describes the reports.</span></span>

| <span data-ttu-id="02a26-131">レポート </span><span class="sxs-lookup"><span data-stu-id="02a26-131">Report</span></span>                      | <span data-ttu-id="02a26-132">レポートに含まれる情報</span><span class="sxs-lookup"><span data-stu-id="02a26-132">Information that the report contains</span></span> |
|-----------------------------|--------------------------------------|
| <span data-ttu-id="02a26-133">現金分析</span><span class="sxs-lookup"><span data-stu-id="02a26-133">Cash Analysis</span></span>               | <span data-ttu-id="02a26-134">法人による現金、四半期ごとの現金、合計現金および勘定ごとの現金</span><span class="sxs-lookup"><span data-stu-id="02a26-134">Cash by legal entity, cash by quarter, total cash, and cash by account</span></span><blockquote>[!NOTE] <span data-ttu-id="02a26-135">四半期ごとの現金は、第 1 四半期の合計の期首残高に含まれていません。</span><span class="sxs-lookup"><span data-stu-id="02a26-135">The cash by quarter information doesn't include beginning balances in the total for the first quarter.</span></span> <span data-ttu-id="02a26-136">これは四半期ごとに転記される新しいトランザクションの合計を表示します。</span><span class="sxs-lookup"><span data-stu-id="02a26-136">It shows the total of new transactions that are posted in each quarter.</span></span></blockquote> |
| <span data-ttu-id="02a26-137">現在の比率分析</span><span class="sxs-lookup"><span data-stu-id="02a26-137">Current Ratio Analysis</span></span>      | <span data-ttu-id="02a26-138">法人による現在の比率、四半期ごとの現在の比率、現在の流動資産および負債の残高</span><span class="sxs-lookup"><span data-stu-id="02a26-138">Current ratio by legal entity, current ratio by quarter, and balances for current assets and current liabilities</span></span> |
| <span data-ttu-id="02a26-139">当座比率の分析</span><span class="sxs-lookup"><span data-stu-id="02a26-139">Quick Ratio Analysis</span></span>        | <span data-ttu-id="02a26-140">法人による当座比率、四半期ごとの当座比率、現金残高、売掛金勘定および現在の負債</span><span class="sxs-lookup"><span data-stu-id="02a26-140">Quick ratio by legal entity, quick ratio by quarter, and balances for cash, accounts receivable, and current liabilities</span></span> |
| <span data-ttu-id="02a26-141">売却済商品の原価分析</span><span class="sxs-lookup"><span data-stu-id="02a26-141">Cost of Goods Sold Analysis</span></span> | <span data-ttu-id="02a26-142">法人による売却済商品の原価 (COGS)、四半期ごとの今年度および昨年度の COGS、法人による COGS から売上、COGS 合計、および売上に対する COGS の割合</span><span class="sxs-lookup"><span data-stu-id="02a26-142">Cost of goods sold (COGS) by legal entity, COGS this year and last year by quarter, COGS to sales by legal entity, total COGS, and COGS to sales percentage</span></span> |
| <span data-ttu-id="02a26-143">運営資金の分析</span><span class="sxs-lookup"><span data-stu-id="02a26-143">Working Capital Analysis</span></span>    | <span data-ttu-id="02a26-144">法人による運営資金、四半期ごとの運営資金、現在の流動資産、現在の負債、および総運営資金</span><span class="sxs-lookup"><span data-stu-id="02a26-144">Working capital by legal entity, working capital by quarter, current assets, current liabilities, and total working capital</span></span> |
| <span data-ttu-id="02a26-145">資産および負債の分析</span><span class="sxs-lookup"><span data-stu-id="02a26-145">Asset and Debt Analysis</span></span>     | <span data-ttu-id="02a26-146">総資産利益率および法人による負債総資産比率、負債総資産比率および四半期累計期間 (現時点までの) における総資産利益率、資産、および負債</span><span class="sxs-lookup"><span data-stu-id="02a26-146">Return on total assets and debt to total assets by legal entity, debt to total assets and return on total assets quarter to date, assets, and liabilities</span></span> |
| <span data-ttu-id="02a26-147">利益率の分析</span><span class="sxs-lookup"><span data-stu-id="02a26-147">Profit Margin Analysis</span></span>      | <span data-ttu-id="02a26-148">法人による実績および予算の利益率、四半期ごとの利益、利益率の割合、および利益率</span><span class="sxs-lookup"><span data-stu-id="02a26-148">Actual and budget profit margin by legal entity, profit marking by quarter, profit margin percentage, and profit margin</span></span> |
| <span data-ttu-id="02a26-149">純利益の分析</span><span class="sxs-lookup"><span data-stu-id="02a26-149">Net Income Analysis</span></span>         | <span data-ttu-id="02a26-150">法人による実績および予算純利益、今年度および昨年度の純利益、および純利益に対する経費の割合</span><span class="sxs-lookup"><span data-stu-id="02a26-150">Actual and budget net income by legal entity, net income this year and last year, and expenses to net income percentage</span></span> |
| <span data-ttu-id="02a26-151">収益の分析</span><span class="sxs-lookup"><span data-stu-id="02a26-151">Earnings Analysis</span></span>           | <span data-ttu-id="02a26-152">法人による実績と予算における金利税引き前利益 (EBIT)、今年度と昨年度の EBIT、収益に対する経費の割合、および実績および予算における収益に対する経費の割合</span><span class="sxs-lookup"><span data-stu-id="02a26-152">Actual and budget earnings before interest and taxes (EBIT) by legal entity, EBIT this year and last year, expenses to revenue percentage, and actual and budget expenses to revenue</span></span> |
| <span data-ttu-id="02a26-153">収益の分析</span><span class="sxs-lookup"><span data-stu-id="02a26-153">Revenue Analysis</span></span>            | <span data-ttu-id="02a26-154">総収益、法人による実績と予算の総収益、今年度および昨年度の総収益、法人による収益予算差異、この期間と最後の期間における総収益</span><span class="sxs-lookup"><span data-stu-id="02a26-154">Total revenue, actual and budget total revenue by legal entity, total revenue this year and last year, revenue budget variance by legal entity, and total revenue this period and last period</span></span> |
| <span data-ttu-id="02a26-155">経費の分析</span><span class="sxs-lookup"><span data-stu-id="02a26-155">Expense Analysis</span></span>            | <span data-ttu-id="02a26-156">経費の合計金額、法人による合計経費予算に対する実績金額、四半期ごとの合計経費予算、勘定カテゴリごとの合計経費、および営業経費の比率</span><span class="sxs-lookup"><span data-stu-id="02a26-156">Total expenses, actual to budget total expenses by legal entity, actual and budget total expense by quarter, total expenses by account category, and operating expenses ratio</span></span> |
| <span data-ttu-id="02a26-157">請求収益の分析</span><span class="sxs-lookup"><span data-stu-id="02a26-157">Billed Revenue Analysis</span></span>     | <span data-ttu-id="02a26-158">売掛金勘定の合計、法人による売掛金勘定の合計、四半期ごとの売掛金勘定の合計、売掛金勘定の勘定残高</span><span class="sxs-lookup"><span data-stu-id="02a26-158">Total accounts receivable, total accounts receivable by legal entity, total accounts receivable by quarter, and balances for accounts receivable accounts</span></span><blockquote>[!NOTE] <span data-ttu-id="02a26-159">第 1 四半期の売掛金勘定の勘定科目は、情報に含まれていません。</span><span class="sxs-lookup"><span data-stu-id="02a26-159">The information doesn't include beginning balances for the accounts receivable ledger accounts.</span></span> <span data-ttu-id="02a26-160">売掛金勘定に転記される新しいトランザクションの合計を表示します。</span><span class="sxs-lookup"><span data-stu-id="02a26-160">It shows the total of new transactions that are posted to Accounts receivable.</span></span></blockquote> |

<span data-ttu-id="02a26-161">これらすべてのレポートのグラフとタイルはフィルター処理し、ダッシュボードに固定することができます。</span><span class="sxs-lookup"><span data-stu-id="02a26-161">The charts and tiles on all these reports can be filtered and pinned to the dashboard.</span></span> <span data-ttu-id="02a26-162">Power BI のフィルター処理と固定方法の詳細については、[ダッシュボードの作成およびコンフィギュレーション](https://powerbi.microsoft.com/guided-learning/powerbi-learning-4-2-create-configure-dashboards) を参照してください。</span><span class="sxs-lookup"><span data-stu-id="02a26-162">For more information about how to filter and pin in Power BI, see [Create and Configure a Dashboard](https://powerbi.microsoft.com/guided-learning/powerbi-learning-4-2-create-configure-dashboards).</span></span>

## <a name="understanding-the-data-model-and-entities"></a><span data-ttu-id="02a26-163">データ モデルおよびエンティティの理解</span><span class="sxs-lookup"><span data-stu-id="02a26-163">Understanding the data model and entities</span></span>
<span data-ttu-id="02a26-164">次のエンティティは **財務パフォーマンス** PowerBI.com ソリューションの基準として使用されていました。</span><span class="sxs-lookup"><span data-stu-id="02a26-164">The following entities were used as the basis of the **Financial performance** PowerBI.com solution:</span></span>

<span data-ttu-id="02a26-165">**データ エンティティの集計**</span><span class="sxs-lookup"><span data-stu-id="02a26-165">**Aggregate data entities**</span></span>

- <span data-ttu-id="02a26-166">**GeneralLedgerActivities** – このエンティティは、勘定カテゴリの総勘定元帳の残高を集計します。</span><span class="sxs-lookup"><span data-stu-id="02a26-166">**GeneralLedgerActivities** – This entity aggregates general ledger balances by account category.</span></span>
- <span data-ttu-id="02a26-167">**BudgetActivities** – このエンティティは、勘定カテゴリの予算残高を集計します。</span><span class="sxs-lookup"><span data-stu-id="02a26-167">**BudgetActivities** – This entity aggregates budget balances by account category.</span></span>

<span data-ttu-id="02a26-168">**データ エンティティ**</span><span class="sxs-lookup"><span data-stu-id="02a26-168">**Data entities**</span></span>

- <span data-ttu-id="02a26-169">FiscalCalendars</span><span class="sxs-lookup"><span data-stu-id="02a26-169">FiscalCalendars</span></span>
- <span data-ttu-id="02a26-170">MainAccounts</span><span class="sxs-lookup"><span data-stu-id="02a26-170">MainAccounts</span></span>
- <span data-ttu-id="02a26-171">LegalEntities</span><span class="sxs-lookup"><span data-stu-id="02a26-171">LegalEntities</span></span>
- <span data-ttu-id="02a26-172">元帳</span><span class="sxs-lookup"><span data-stu-id="02a26-172">Ledgers</span></span>
- <span data-ttu-id="02a26-173">ChartofAccounts</span><span class="sxs-lookup"><span data-stu-id="02a26-173">ChartofAccounts</span></span>

<span data-ttu-id="02a26-174">これらのエンティティは、データ モデルの計算メジャーを作成するために使用されました。</span><span class="sxs-lookup"><span data-stu-id="02a26-174">These entities were used to create calculated measures in the data model.</span></span> <span data-ttu-id="02a26-175">計算メジャーは、主要業績評価指標 (KPI) およびコンテンツで使用されるレポートを計算するために使用されます。</span><span class="sxs-lookup"><span data-stu-id="02a26-175">The calculated measures are used to calculate the key performance indicators (KPIs) and reports that are used in the content.</span></span> <span data-ttu-id="02a26-176">既定では、コンテンツにより、過去 3 年間および将来 1 年間のデータが取得されます。</span><span class="sxs-lookup"><span data-stu-id="02a26-176">By default, the content brings in data for the last three years and one future year.</span></span> <span data-ttu-id="02a26-177">追加の計算をレポートおよびダッシュボードに含めるには、[Microsoft Excel ワークブック](/dynamics/s-e/) を変更できます。</span><span class="sxs-lookup"><span data-stu-id="02a26-177">To include additional calculations on your reports and dashboard, you can modify the [Microsoft Excel workbook](/dynamics/s-e/).</span></span> <span data-ttu-id="02a26-178">このワークブックはコンテンツを作成するために使用された既定のデータ モデルです。</span><span class="sxs-lookup"><span data-stu-id="02a26-178">This workbook is the default data model that was used to create the content.</span></span>


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]