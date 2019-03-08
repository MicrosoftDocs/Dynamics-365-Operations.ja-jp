---
title: 需要予測の概要
description: 需要予測は、販売注文からの独立要求および顧客注文のすべての減結合ポイントで依存要求を予測する場合に使用されます。 拡張された需要予測の削減ルールは、大量のカスタマイズに理想的なソリューションを提供します。
author: roxanadiaconu
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ReqDemPlanCreateForecastDialog
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.custom: 72004
ms.assetid: 916707c9-1333-460f-a0fa-4e95f6fda2ad
ms.search.region: global
ms.search.industry: Manufacturing
ms.author: roxanad
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: a645ee6f7e6085abc6e872d490b078f512c15aa1
ms.sourcegitcommit: 0f530e5f72a40f383868957a6b5cb0e446e4c795
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 01/29/2019
ms.locfileid: "310004"
---
# <a name="demand-forecasting-overview"></a><span data-ttu-id="b8294-104">需要予測の概要</span><span class="sxs-lookup"><span data-stu-id="b8294-104">Demand forecasting overview</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="b8294-105">需要予測は、販売注文からの独立要求および顧客注文のすべての減結合ポイントで依存要求を予測する場合に使用されます。</span><span class="sxs-lookup"><span data-stu-id="b8294-105">Demand forecasting is used to predict independent demand from sales orders and dependent demand at any decoupling point for customer orders.</span></span> <span data-ttu-id="b8294-106">拡張された需要予測の削減ルールは、大量のカスタマイズに理想的なソリューションを提供します。</span><span class="sxs-lookup"><span data-stu-id="b8294-106">The enhanced demand forecast reduction rules provide an ideal solution for mass customization.</span></span>

<span data-ttu-id="b8294-107">ベースラインの予測を生成するには、履歴トランザクション集計が Azure でホストされている Microsoft Azure Machine Learning サービスに転送されます。</span><span class="sxs-lookup"><span data-stu-id="b8294-107">To generate the baseline forecast, a summary of historical transactions is passed to a Microsoft Azure Machine Learning service that is hosted on Azure.</span></span> <span data-ttu-id="b8294-108">このサービスはユーザー間で共有されないため、業界固有の要件に合わせて、簡単にカスタマイズできます。</span><span class="sxs-lookup"><span data-stu-id="b8294-108">Because this service isn't shared among users, it can easily be customized to meet industry-specific requirements.</span></span> <span data-ttu-id="b8294-109">Finance and Operations を使用して、予測を視覚化し、予測を調整し、予測精度に関する主要業績評価指標 (KPI) を表示することができます。</span><span class="sxs-lookup"><span data-stu-id="b8294-109">You can use Finance and Operations to visualize the forecast, adjust the forecast, and view key performance indicators (KPIs) about forecast accuracy.</span></span>

## <a name="key-features-of-demand-forecasting"></a><span data-ttu-id="b8294-110">需要予測の主な機能</span><span class="sxs-lookup"><span data-stu-id="b8294-110">Key features of demand forecasting</span></span>
<span data-ttu-id="b8294-111">需要予測の主な特長を次に示します。</span><span class="sxs-lookup"><span data-stu-id="b8294-111">Here are some of the main features of demand forecasting:</span></span>

-   <span data-ttu-id="b8294-112">履歴データに基づいて統計ベースライン予測を生成します。</span><span class="sxs-lookup"><span data-stu-id="b8294-112">Generate a statistical baseline forecast that is based on historical data.</span></span>
-   <span data-ttu-id="b8294-113">動的セットの予測分析コードを使用します。</span><span class="sxs-lookup"><span data-stu-id="b8294-113">Use a dynamic set of forecast dimensions.</span></span>
-   <span data-ttu-id="b8294-114">需要傾向、信頼区間と予測調整を視覚化します。</span><span class="sxs-lookup"><span data-stu-id="b8294-114">Visualize demand trends, confidence intervals, and adjustments of the forecast.</span></span>
-   <span data-ttu-id="b8294-115">計画プロセスで使用する調整された予測を承認します。</span><span class="sxs-lookup"><span data-stu-id="b8294-115">Authorize the adjusted forecast to be used in planning processes.</span></span>
-   <span data-ttu-id="b8294-116">異常値を削除します。</span><span class="sxs-lookup"><span data-stu-id="b8294-116">Remove outliers.</span></span>
-   <span data-ttu-id="b8294-117">予測精度の測定を作成します。</span><span class="sxs-lookup"><span data-stu-id="b8294-117">Create measurements of forecast accuracy.</span></span>

## <a name="major-themes-in-demand-forecasting"></a><span data-ttu-id="b8294-118">需要予測の主要テーマ</span><span class="sxs-lookup"><span data-stu-id="b8294-118">Major themes in demand forecasting</span></span>
<span data-ttu-id="b8294-119">3 つの主要なテーマの需要予測が実装できます。</span><span class="sxs-lookup"><span data-stu-id="b8294-119">Three major themes are implemented in demand forecasting:</span></span>

-   <span data-ttu-id="b8294-120">**モジュール性** – 需要予測はモジュールおよびコンフィギュレーションが簡単にできます。</span><span class="sxs-lookup"><span data-stu-id="b8294-120">**Modularity** – Demand forecasting is modular and easy to configure.</span></span> <span data-ttu-id="b8294-121">**販売** &gt; **在庫予測** &gt; **需要予測** で構成キーの機能をオン/オフに変更できます。</span><span class="sxs-lookup"><span data-stu-id="b8294-121">You can turn the functionality on and off by changing the configuration key at **Trade** &gt; **Inventory forecast** &gt; **Demand forecasting**.</span></span>
-   <span data-ttu-id="b8294-122">**Microsoft Stack の再利用** – Microsoft は 2015 年 2 月に Machine Learning プラットフォームを開始しました。</span><span class="sxs-lookup"><span data-stu-id="b8294-122">**Reuse of the Microsoft stack** – Microsoft launched the Machine Learning platform in February 2015.</span></span> <span data-ttu-id="b8294-123">Microsoft Cortana Analytics Suite の一部である Machine Learning を使用すると、需要見積もりの試算、アルゴリズム R または Python プログラミング言語、およびシンプルなドラッグ アンド ドロップ インターフェースなど、予測分析実験をすばやく簡単に作成できます。</span><span class="sxs-lookup"><span data-stu-id="b8294-123">Machine Learning, which is now part of the Microsoft Cortana Analytics Suite, lets you quickly and easily create predictive analysis experiments, such as demand estimation experiments, by using algorithms R or Python programming languages and a simple drag-and-drop interface.</span></span>
    -   <span data-ttu-id="b8294-124">Finance and Operations Demand forecasting experiments をダウンロードして、ビジネス要件に適合するように変更し、Azure の Web サービスとして公開し、需要予測を生成するために使用できます。</span><span class="sxs-lookup"><span data-stu-id="b8294-124">You can download the Finance and Operations Demand forecasting experiments, change them to meet your business requirements, publish them as a web service on Azure, and use them to generate demand forecasts.</span></span> <span data-ttu-id="b8294-125">エンタープライズ レベルのユーザーとして、生産計画担当者向けに Finance and Operations サブスクリプションを購入した場合は、この実験をダウンロードできます。</span><span class="sxs-lookup"><span data-stu-id="b8294-125">The experiments are available for download if you've purchased a Finance and Operations subscription for a production planner as enterprise level user.</span></span>
    -   <span data-ttu-id="b8294-126">[Cortana Analytics Gallery](https://gallery.cortanaanalytics.com/) から現在有効な需要予測実験をダウンロードできます。</span><span class="sxs-lookup"><span data-stu-id="b8294-126">You can download any of the currently available demand prediction experiments from the [Cortana Analytics Gallery](https://gallery.cortanaanalytics.com/).</span></span> <span data-ttu-id="b8294-127">Finance and Operations Demand forecasting experiments は Finance and Operations と自動的に統合されるので、顧客およびパートナーは [Cortana Analytics Gallery](https://gallery.cortanaanalytics.com/) からダウンロードした experiments の統合を処理する必要があります。</span><span class="sxs-lookup"><span data-stu-id="b8294-127">Whereas the Finance and Operations Demand forecasting experiments are automatically integrated with Finance and Operations, customers and partners must handle the integration of experiments that they download from the [Cortana Analytics Gallery](https://gallery.cortanaanalytics.com/).</span></span> <span data-ttu-id="b8294-128">したがって、[Cortana Analytics Gallery](https://gallery.cortanaanalytics.com/) の実験は Finance and Operations の需要予測実験として使用できるほど単純ではありません。</span><span class="sxs-lookup"><span data-stu-id="b8294-128">Therefore, experiments from the [Cortana Analytics Gallery](https://gallery.cortanaanalytics.com/) aren't as straightforward to use as the Finance and Operations Demand forecasting experiments.</span></span> <span data-ttu-id="b8294-129">Finance and Operations アプリケーション プログラム インターフェイス (API) を使用するように experiments のコードを修正する必要があります。</span><span class="sxs-lookup"><span data-stu-id="b8294-129">You must modify the code of the experiments so that they use the Finance and Operations application programming interface (API).</span></span>
    -   <span data-ttu-id="b8294-130">Microsoft Azure Machine Learning Studio で独自の実験を作成し、Azure のサービスとして発行、そして需要予測の生成に使用することができます。</span><span class="sxs-lookup"><span data-stu-id="b8294-130">You can create your own experiments in Microsoft Azure Machine Learning Studio, publish them as services on Azure, and use them to generate demand forecasts.</span></span>
    -   <span data-ttu-id="b8294-131">高パフォーマンスが必要でない場合、または大量のデータの処理が要求されていない場合に、Machine Learning 無料レベルを使用できます。</span><span class="sxs-lookup"><span data-stu-id="b8294-131">If you don’t require high performance, or if you don't require that a large amount of data be processed, you can use the Machine Learning free tier.</span></span> <span data-ttu-id="b8294-132">特に実装およびテスト フェーズの際には、このレベルから常に開始することをお勧めします。</span><span class="sxs-lookup"><span data-stu-id="b8294-132">We recommend that you always start from this tier, especially during implementation and testing phases.</span></span> <span data-ttu-id="b8294-133">高パフォーマンスと追加のストレージが必要な場合、Machine Learning 標準レベルを使用できます。</span><span class="sxs-lookup"><span data-stu-id="b8294-133">If you require higher performance and additional storage, you can use the Machine Learning standard tier.</span></span> <span data-ttu-id="b8294-134">この層には、Azure のサブスクリプションが要求され、追加費用が含まれます。</span><span class="sxs-lookup"><span data-stu-id="b8294-134">This tier requires an Azure subscription and involves additional costs.</span></span> <span data-ttu-id="b8294-135">Machine Learning 価格設定の詳細については、<http://aka.ms/machine-learning-price-info>を参照してください。</span><span class="sxs-lookup"><span data-stu-id="b8294-135">For details about Machine Learning pricing, see <http://aka.ms/machine-learning-price-info>.</span></span>
-   <span data-ttu-id="b8294-136">**すべてのデカップリング ポイントでの予測の減少** – Finance and Operations の需要予測はこの機能に基づいて作成されるので、すべてのデカップリング ポイントで需要に依存する、または依存しない予測が可能です。</span><span class="sxs-lookup"><span data-stu-id="b8294-136">**Forecast reduction at any decoupling point** – Demand forecasting in Finance and Operations builds on this functionality, which lets you forecast both dependent and independent demand at any decoupling point.</span></span>

## <a name="basic-flow-in-demand-forecasting"></a><span data-ttu-id="b8294-137">需要予測の基本フロー</span><span class="sxs-lookup"><span data-stu-id="b8294-137">Basic flow in demand forecasting</span></span>
<span data-ttu-id="b8294-138">次の図は、需要予測の基本フローを表示します。</span><span class="sxs-lookup"><span data-stu-id="b8294-138">The following diagram shows the basic flow in demand forecasting.</span></span> 

<span data-ttu-id="b8294-139">[![需要予測の導入図](./media/demand-forecasting-introduction.png)](./media/demand-forecasting-introduction.png)</span><span class="sxs-lookup"><span data-stu-id="b8294-139">[![demand forecasting introduction diagram](./media/demand-forecasting-introduction.png)](./media/demand-forecasting-introduction.png)</span></span>

<span data-ttu-id="b8294-140">需要予測の生成は、Finance and Operations で開始されます。</span><span class="sxs-lookup"><span data-stu-id="b8294-140">Demand forecast generation starts in Finance and Operations.</span></span> <span data-ttu-id="b8294-141">Finance and Operations トランザクション データベースからの履歴トランザクション データが収集され、ステージング テーブルに値が入力されます。</span><span class="sxs-lookup"><span data-stu-id="b8294-141">Historical transactional data from the Finance and Operations transactional database is gathered and populates a staging table.</span></span> <span data-ttu-id="b8294-142">このステージング テーブルが Machine Learning サービスに後ほど提供されます。</span><span class="sxs-lookup"><span data-stu-id="b8294-142">This staging table is later fed to a Machine Learning service.</span></span> <span data-ttu-id="b8294-143">最低限のカスタマイズで、さまざまなデータ ソースをステージング テーブルにプラグできます。</span><span class="sxs-lookup"><span data-stu-id="b8294-143">By performing minimal customization, you can plug various data sources into the staging table.</span></span> <span data-ttu-id="b8294-144">データ ソースには、Microsoft Excel ファイル、コンマ区切り値 (CSV) ファイル、および Microsoft Dynamics AX 2009 と Microsoft Dynamics AX 2012 からのデータが含まれます。</span><span class="sxs-lookup"><span data-stu-id="b8294-144">The data sources can include Microsoft Excel files, comma-separated value (CSV) files, and data from Microsoft Dynamics AX 2009 and Microsoft Dynamics AX 2012.</span></span> <span data-ttu-id="b8294-145">したがって、複数のシステムにまたがった履歴データを考慮する需要予測を生成できます。</span><span class="sxs-lookup"><span data-stu-id="b8294-145">Therefore, you can generate demand forecasts that consider historical data that is spread among multiple systems.</span></span> <span data-ttu-id="b8294-146">ただし、品目名、販売単位などのマスター データは、さまざまなデータ ソース間でも同じである必要があります。</span><span class="sxs-lookup"><span data-stu-id="b8294-146">However, the master data, such as item names and units of measure, must be the same across the various data sources.</span></span>

<span data-ttu-id="b8294-147">Finance and Operations Demand forecasting Machine Learning experiments を使用する場合、ベースラインの予測を計算する 5 つの予測方法から一番最適な予測を検索します。</span><span class="sxs-lookup"><span data-stu-id="b8294-147">If you use the Finance and Operations Demand forecasting Machine Learning experiments, they look for a best fit among five time series forecasting methods to calculate a baseline forecast.</span></span> <span data-ttu-id="b8294-148">予測方法のパラメーターは Finance and Operations に統合されます。</span><span class="sxs-lookup"><span data-stu-id="b8294-148">The parameters for these forecasting methods are managed in Finance and Operations.</span></span> 

<span data-ttu-id="b8294-149">以前の項目での、予測、履歴データ、および変更点などの需要予測が Finance and Operations で次に利用可能です。</span><span class="sxs-lookup"><span data-stu-id="b8294-149">The forecasts, historical data, and any changes that were made to the demand forecasts in previous iterations are then available in Finance and Operations.</span></span> 

<span data-ttu-id="b8294-150">Finance and Operations を使用してベースラインの予測を視覚化し修正できます。</span><span class="sxs-lookup"><span data-stu-id="b8294-150">You can use Finance and Operations to visualize and modify the baseline forecasts.</span></span> <span data-ttu-id="b8294-151">手動調整は、予測計画で使用する前に承認する必要があります。</span><span class="sxs-lookup"><span data-stu-id="b8294-151">Manual adjustments must be authorized before the forecasts can be used for planning.</span></span>

## <a name="limitations"></a><span data-ttu-id="b8294-152">制限</span><span class="sxs-lookup"><span data-stu-id="b8294-152">Limitations</span></span>
<span data-ttu-id="b8294-153">Finance and Operations での需要予測は、製造業界の顧客が予測プロセスを作成する助けとなるツールです。</span><span class="sxs-lookup"><span data-stu-id="b8294-153">Demand forecasting in Finance and Operations is a tool that helps customers in the manufacturing industry create forecasting processes.</span></span> <span data-ttu-id="b8294-154">需要予測ソリューションの核となる機能を提供し、簡単に拡張できるように設計されています。</span><span class="sxs-lookup"><span data-stu-id="b8294-154">It offers the core functionality of a demand forecasting solution and is designed so that it can easily be extended.</span></span> <span data-ttu-id="b8294-155">需要予測は、小売業、卸売業、倉庫保管、輸送業、または他の専門的なサービス産業の顧客には最適ではない場合があります。</span><span class="sxs-lookup"><span data-stu-id="b8294-155">Demand forecasting might not be the best fit for customers in industries such as retail, wholesale, warehousing, transportation, or other professional services.</span></span>

<a name="additional-resources"></a><span data-ttu-id="b8294-156">その他のリソース</span><span class="sxs-lookup"><span data-stu-id="b8294-156">Additional resources</span></span>
--------

[<span data-ttu-id="b8294-157">需要予測の設定</span><span class="sxs-lookup"><span data-stu-id="b8294-157">Demand forecasting setup</span></span>](demand-forecasting-setup.md)

[<span data-ttu-id="b8294-158">統計ベースライン予測の生成</span><span class="sxs-lookup"><span data-stu-id="b8294-158">Generating a statistical baseline forecast</span></span>](generate-statistical-baseline-forecast.md)

[<span data-ttu-id="b8294-159">ベースライン予測の手動調整の実施</span><span class="sxs-lookup"><span data-stu-id="b8294-159">Making manual adjustments to the baseline forecast</span></span>](manual-adjustments-baseline-forecast.md)

[<span data-ttu-id="b8294-160">調整された予測の承認</span><span class="sxs-lookup"><span data-stu-id="b8294-160">Authorizing the adjusted forecast</span></span>](authorize-adjusted-forecast.md)

[<span data-ttu-id="b8294-161">予測精度の監視</span><span class="sxs-lookup"><span data-stu-id="b8294-161">Monitoring forecast accuracy</span></span>](monitor-forecast-accuracy.md)

[<span data-ttu-id="b8294-162">需要予測を計算するときにトランザクション履歴データから異常値を削除する</span><span class="sxs-lookup"><span data-stu-id="b8294-162">Remove outliers from historical transaction data when calculating a demand forecast</span></span>](remove-historical-outliers-calculating-demand-forecast.md)

[<span data-ttu-id="b8294-163">Extend the demand forecasting functionality (需要予測機能の拡張)</span><span class="sxs-lookup"><span data-stu-id="b8294-163">Extend the demand forecasting functionality</span></span>](https://www.youtube.com/watch?v=4OIKIXLiNjI&feature=youtu.be)



