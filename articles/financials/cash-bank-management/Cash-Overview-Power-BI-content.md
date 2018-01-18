---
title: "キャッシュの概要 Power BI コンテンツ"
description: "このトピックでは、キャッシュの概要 Microsoft Power BI コンテンツについて説明します。 コンテンツに含まれているレポートにアクセスする方法を説明し、コンテンツを作成するために使用したデータ モデルおよびエンティティについての情報を提供します。"
author: saraschi2
manager: AnnBe
ms.date: 12/19/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: BankTreasurerWorkspace
audience: Application User
ms.reviewer: sericks
ms.search.scope: Operations, Core
ms.search.region: Global
ms.author: saraschi
ms.search.validFrom: 2017-06-30
ms.dyn365.ops.version: July 2017 update
ms.translationtype: HT
ms.sourcegitcommit: 029511634e56aec7fdd91bad9441cd12951fbd8d
ms.openlocfilehash: a5ac80af2f00aba0a63b4c773f437d3ac7a0e8f6
ms.contentlocale: ja-jp
ms.lasthandoff: 01/17/2018

---

# <a name="cash-overview-power-bi-content"></a><span data-ttu-id="99376-104">キャッシュの概要 Power BI コンテンツ</span><span class="sxs-lookup"><span data-stu-id="99376-104">Cash overview Power BI content</span></span>

[!include[banner](../includes/banner.md)]

<span data-ttu-id="99376-105">このトピックでは、**キャッシュの概要** Microsoft Power BI content について説明します。</span><span class="sxs-lookup"><span data-stu-id="99376-105">This topic describes the **Cash overview** Microsoft Power BI content.</span></span> <span data-ttu-id="99376-106">コンテンツに含まれているレポートにアクセスする方法を説明し、コンテンツを作成するために使用したデータ モデルおよびエンティティについての情報を提供します。</span><span class="sxs-lookup"><span data-stu-id="99376-106">It explains how to access the reports that are included in the content, and provides information about the data model and entities that were used to build the content.</span></span>

## <a name="overview"></a><span data-ttu-id="99376-107">概要</span><span class="sxs-lookup"><span data-stu-id="99376-107">Overview</span></span>

<span data-ttu-id="99376-108">**キャッシュの概要** Power BI コンテンツは、組織内で現金を担当する方のために作成されました。</span><span class="sxs-lookup"><span data-stu-id="99376-108">The **Cash overview** Power BI content was created for individuals who are responsible for cash in their organization.</span></span> <span data-ttu-id="99376-109">**キャッシュの概要** Power BI コンテンツは、キャッシュ フローの可視性を提供します。</span><span class="sxs-lookup"><span data-stu-id="99376-109">The **Cash overview** Power BI content provides visibility into your cash flow.</span></span> <span data-ttu-id="99376-110">適切な意志決定を支援するための予測も提供し、キャッシュ フローの正常性が向上します。</span><span class="sxs-lookup"><span data-stu-id="99376-110">It also provides forecasts that can help you make better decisions and therefore improve the health of your cash flow.</span></span> <span data-ttu-id="99376-111">黒字額と不足分を把握するために、法人、通貨、および銀行口座ごとにキャッシュを分析できます。</span><span class="sxs-lookup"><span data-stu-id="99376-111">You can analyze cash by legal entity, currency, and bank account to get a better understanding of surpluses and shortfalls.</span></span>

## <a name="accessing-the-power-bi-content"></a><span data-ttu-id="99376-112">Power BI コンテンツへのアクセス</span><span class="sxs-lookup"><span data-stu-id="99376-112">Accessing the Power BI content</span></span>

<span data-ttu-id="99376-113">**現金の概要** Power BI コンテンツからのレポートが、**現金の概要** および **銀行管理** ワークスペースで表示されます。</span><span class="sxs-lookup"><span data-stu-id="99376-113">Reports from the **Cash overview** Power BI content are displayed in the **Cash overview** and **Bank management** workspaces.</span></span>

<span data-ttu-id="99376-114">データでキャッシュ フロー予測レポートを表示するには、まず、現金および銀行管理領域から**キャッシュ フロー予測の計算** 機能を使用して、予測計算プロセスを実行する必要があります。</span><span class="sxs-lookup"><span data-stu-id="99376-114">To view the Cash flow forecasting reports with data, you must first run the forecast calculation process using the **Calculate cash flow forecasts** function from the Cash and bank management area.</span></span>  <span data-ttu-id="99376-115">これは、予測に含める会社ごとに完了する必要があります。</span><span class="sxs-lookup"><span data-stu-id="99376-115">This needs to be completed for each company included in the forecast.</span></span>  <span data-ttu-id="99376-116">[**エンティティ格納**] ページで [LedgerCovLiquidityMeasurement] 集計の測定を更新する必要があります。</span><span class="sxs-lookup"><span data-stu-id="99376-116">You then need to refresh the LedgerCovLiquidityMeasurement aggregate measurement on the **Entity Store** page.</span></span>  

<span data-ttu-id="99376-117">説明するには、[**データの生成**] ページをデモ データ モジュールから使用し、キャッシュ フロー予測デモ データを追加できます。</span><span class="sxs-lookup"><span data-stu-id="99376-117">For demonstration purposes, you can add cash flow forecasting demo data using the **Generate data** page from the Demo data module.</span></span>  <span data-ttu-id="99376-118">このスクリプトは、キャッシュ フロー予測テーブルにデータを挿入して、レポートに必要な情報をすばやく入力します。</span><span class="sxs-lookup"><span data-stu-id="99376-118">This script will insert data into the cash flow forecasting tables to quickly populate information necessary for reports.</span></span>  <span data-ttu-id="99376-119">このモジュールは、デモ データ スイート モデルが環境に展開されている場合にのみ使用できます。</span><span class="sxs-lookup"><span data-stu-id="99376-119">This module is only available if you have the Demo data suite model deployed on the environment.</span></span> 

## <a name="reports-that-are-included-in-the-power-bi-content"></a><span data-ttu-id="99376-120">Power BI コンテンツに含まれるレポート</span><span class="sxs-lookup"><span data-stu-id="99376-120">Reports that are included in the Power BI content</span></span>
<span data-ttu-id="99376-121">次の表は、**キャッシュの概要** Power BI コンテンツの各レポート ページに表示されるメトリックスの詳細について説明しています。</span><span class="sxs-lookup"><span data-stu-id="99376-121">The following table provides details about the metrics that are found on each report page in the **Cash overview** Power BI content.</span></span>

| <span data-ttu-id="99376-122">レポート</span><span class="sxs-lookup"><span data-stu-id="99376-122">Report</span></span>                                | <span data-ttu-id="99376-123">コンテンツ</span><span class="sxs-lookup"><span data-stu-id="99376-123">Contents</span></span> |
|---------------------------------------|----------|
| <span data-ttu-id="99376-124">現金の概要 – すべての会社</span><span class="sxs-lookup"><span data-stu-id="99376-124">Cash overview – all companies</span></span>         | <ul><li><span data-ttu-id="99376-125">システム通貨の現金収支</span><span class="sxs-lookup"><span data-stu-id="99376-125">Inflows and outflows in system currency</span></span></li><li><span data-ttu-id="99376-126">予測される通貨残高</span><span class="sxs-lookup"><span data-stu-id="99376-126">Forecasted currency balances</span></span></li><li><span data-ttu-id="99376-127">システム通貨での銀行預金残高の合計</span><span class="sxs-lookup"><span data-stu-id="99376-127">Total bank balance in system currency</span></span></li><li><span data-ttu-id="99376-128">法人ごとの残高</span><span class="sxs-lookup"><span data-stu-id="99376-128">Balance by legal entity</span></span></li><li><span data-ttu-id="99376-129">銀行口座通貨での、現在の実績対予測残高</span><span class="sxs-lookup"><span data-stu-id="99376-129">Today’s actual vs forecasted balance in bank account currency</span></span></li></ul> |
| <span data-ttu-id="99376-130">現金の概要 – 現在の会社</span><span class="sxs-lookup"><span data-stu-id="99376-130">Cash overview – current company</span></span>       | <ul><li><span data-ttu-id="99376-131">会計通貨の現金収支</span><span class="sxs-lookup"><span data-stu-id="99376-131">Inflows and outflows in accounting currency</span></span></li><li><span data-ttu-id="99376-132">予測される通貨残高</span><span class="sxs-lookup"><span data-stu-id="99376-132">Forecasted currency balances</span></span></li><li><span data-ttu-id="99376-133">会計通貨での銀行預金残高の合計</span><span class="sxs-lookup"><span data-stu-id="99376-133">Total bank balance in accounting currency</span></span></li><li><span data-ttu-id="99376-134">銀行口座通貨での、現在の実績対予測残高</span><span class="sxs-lookup"><span data-stu-id="99376-134">Today’s actual vs forecasted balance in bank account currency</span></span></li></ul> |
| <span data-ttu-id="99376-135">予測されるキャッシュ フロー – すべての会社</span><span class="sxs-lookup"><span data-stu-id="99376-135">Cash flow forecast – all companies</span></span>    | <ul><li><span data-ttu-id="99376-136">システム通貨の現金収支</span><span class="sxs-lookup"><span data-stu-id="99376-136">Inflows and outflows in system currency</span></span></li><li><span data-ttu-id="99376-137">日次予測の集計</span><span class="sxs-lookup"><span data-stu-id="99376-137">Daily forecast summary</span></span></li><li><span data-ttu-id="99376-138">予測の詳細</span><span class="sxs-lookup"><span data-stu-id="99376-138">Forecast details</span></span></li></ul> |
| <span data-ttu-id="99376-139">キャッシュ フロー予測 – 会社通貨</span><span class="sxs-lookup"><span data-stu-id="99376-139">Cash flow forecast – currency company</span></span> | <ul><li><span data-ttu-id="99376-140">会計通貨の現金収支</span><span class="sxs-lookup"><span data-stu-id="99376-140">Inflows and outflows in accounting currency</span></span></li><li><span data-ttu-id="99376-141">日次予測の集計</span><span class="sxs-lookup"><span data-stu-id="99376-141">Daily forecast summary</span></span></li><li><span data-ttu-id="99376-142">予測の詳細</span><span class="sxs-lookup"><span data-stu-id="99376-142">Forecast details</span></span></li></ul> |
| <span data-ttu-id="99376-143">通貨予測</span><span class="sxs-lookup"><span data-stu-id="99376-143">Currency forecast</span></span>                     | <ul><li><span data-ttu-id="99376-144">予測される通貨残高</span><span class="sxs-lookup"><span data-stu-id="99376-144">Forecasted currency balances</span></span></li><li><span data-ttu-id="99376-145">日次通貨集計</span><span class="sxs-lookup"><span data-stu-id="99376-145">Daily currency summary</span></span></li><li><span data-ttu-id="99376-146">予測の詳細</span><span class="sxs-lookup"><span data-stu-id="99376-146">Forecast details</span></span></li></ul> |
| <span data-ttu-id="99376-147">銀行預金残高</span><span class="sxs-lookup"><span data-stu-id="99376-147">Bank balances</span></span>                         | <ul><li><span data-ttu-id="99376-148">システム通貨での銀行預金残高の合計</span><span class="sxs-lookup"><span data-stu-id="99376-148">Total bank balance in system currency</span></span></li><li><span data-ttu-id="99376-149">法人ごとの残高</span><span class="sxs-lookup"><span data-stu-id="99376-149">Balance by legal entity</span></span></li><li><span data-ttu-id="99376-150">銀行口座通貨での、現在の実績対予測残高</span><span class="sxs-lookup"><span data-stu-id="99376-150">Today’s actual vs forecasted balance in bank account currency</span></span></li><li><span data-ttu-id="99376-151">銀行口座ごとの残高</span><span class="sxs-lookup"><span data-stu-id="99376-151">Balance by bank account</span></span></li><li><span data-ttu-id="99376-152">通貨別残高</span><span class="sxs-lookup"><span data-stu-id="99376-152">Balance by currency</span></span></li></ul> |


## <a name="understanding-the-data-model-and-entities"></a><span data-ttu-id="99376-153">データ モデルおよびエンティティの理解</span><span class="sxs-lookup"><span data-stu-id="99376-153">Understanding the data model and entities</span></span>

<span data-ttu-id="99376-154">次の表に、**現金の概要** Power BI コンテンツが基づいているエンティティを示します。</span><span class="sxs-lookup"><span data-stu-id="99376-154">The following table shows the entities that the **Cash overview** Power BI content is based on.</span></span>

| <span data-ttu-id="99376-155">エンティティ</span><span class="sxs-lookup"><span data-stu-id="99376-155">Entity</span></span>                                                                          | <span data-ttu-id="99376-156">コンテンツ</span><span class="sxs-lookup"><span data-stu-id="99376-156">Contents</span></span> |
|---------------------------------------------------------------------------------|----------|
| <span data-ttu-id="99376-157">LedgerCovLiquidityMeasurement\_Company</span><span class="sxs-lookup"><span data-stu-id="99376-157">LedgerCovLiquidityMeasurement\_Company</span></span>                                          | <span data-ttu-id="99376-158">レポートをフィルター処理する会社</span><span class="sxs-lookup"><span data-stu-id="99376-158">Companies to filter reports by</span></span> |
| <span data-ttu-id="99376-159">LedgerCovLiquidityMeasurement\_Date</span><span class="sxs-lookup"><span data-stu-id="99376-159">LedgerCovLiquidityMeasurement\_Date</span></span>                                             | <span data-ttu-id="99376-160">レポートをフィルター処理する日付</span><span class="sxs-lookup"><span data-stu-id="99376-160">Dates to filter reports by</span></span> |
| <span data-ttu-id="99376-161">LedgerCovLiquidityMeasurement\_LedgerCovForecastActual</span><span class="sxs-lookup"><span data-stu-id="99376-161">LedgerCovLiquidityMeasurement\_LedgerCovForecastActual</span></span>                          | <span data-ttu-id="99376-162">実際の口座残高対最後に予測した銀行預金残高</span><span class="sxs-lookup"><span data-stu-id="99376-162">Actual bank balance vs last forecasted bank balance</span></span> |
| <span data-ttu-id="99376-163">LedgerCovLiquidityMeasurement\_LedgerCovLiquidity</span><span class="sxs-lookup"><span data-stu-id="99376-163">LedgerCovLiquidityMeasurement\_LedgerCovLiquidity</span></span>                               | <span data-ttu-id="99376-164">予測トランザクションの詳細</span><span class="sxs-lookup"><span data-stu-id="99376-164">Forecasted transaction details</span></span> |
| <span data-ttu-id="99376-165">LedgerCovLiquidityMeasurement\_LedgerCovLiquidityInflowOutflowBalanceCompany</span><span class="sxs-lookup"><span data-stu-id="99376-165">LedgerCovLiquidityMeasurement\_LedgerCovLiquidityInflowOutflowBalanceCompany</span></span>    | <span data-ttu-id="99376-166">各会社の会計通貨を使用したキャッシュ インフロー、アウトフロー、および残高</span><span class="sxs-lookup"><span data-stu-id="99376-166">Summarized cash inflows, outflows, and balance using each company’s accounting currency</span></span> |
| <span data-ttu-id="99376-167">LedgerCovLiquidityMeasurement\_LedgerCovLiquidityInflowOutflowBalanceEnterprise</span><span class="sxs-lookup"><span data-stu-id="99376-167">LedgerCovLiquidityMeasurement\_LedgerCovLiquidityInflowOutflowBalanceEnterprise</span></span> | <span data-ttu-id="99376-168">全ての会社に関して、システム通貨を使用したキャッシュ インフロー、アウトフロー、および残高</span><span class="sxs-lookup"><span data-stu-id="99376-168">Summarized cash inflows, outflows, and balance using the system currency for all companies</span></span> |
| <span data-ttu-id="99376-169">LedgerCovLiquidityMeasurement\_LedgerCovLiquidityTransactionCurrency</span><span class="sxs-lookup"><span data-stu-id="99376-169">LedgerCovLiquidityMeasurement\_LedgerCovLiquidityTransactionCurrency</span></span>            | <span data-ttu-id="99376-170">トランザクション通貨を使用した、トランザクション正味金額および通貨残高の集計</span><span class="sxs-lookup"><span data-stu-id="99376-170">Summarized net transaction amount and balance of currencies using the transaction currency</span></span> |



