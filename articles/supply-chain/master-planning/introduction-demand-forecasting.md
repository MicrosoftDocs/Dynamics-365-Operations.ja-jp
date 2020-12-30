---
title: 需要予測の概要
description: 需要予測は、販売注文からの独立要求および顧客注文のすべての減結合ポイントで依存要求を予測する場合に使用されます。 拡張された需要予測の削減ルールは、大量のカスタマイズに理想的なソリューションを提供します。
author: roxanadiaconu
manager: tfehr
ms.date: 07/07/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ReqDemPlanCreateForecastDialog
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.custom: 72004
ms.assetid: 916707c9-1333-460f-a0fa-4e95f6fda2ad
ms.search.region: global
ms.search.industry: Manufacturing
ms.author: kamaybac
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 62ee31b7931c6e7d8f54c1efb556a2ba01eb7746
ms.sourcegitcommit: 199848e78df5cb7c439b001bdbe1ece963593cdb
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 10/13/2020
ms.locfileid: "4432205"
---
# <a name="demand-forecasting-overview"></a><span data-ttu-id="67e87-104">需要予測の概要</span><span class="sxs-lookup"><span data-stu-id="67e87-104">Demand forecasting overview</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="67e87-105">需要予測は、販売注文からの独立要求および顧客注文のすべての減結合ポイントで依存要求を予測する場合に使用されます。</span><span class="sxs-lookup"><span data-stu-id="67e87-105">Demand forecasting is used to predict independent demand from sales orders and dependent demand at any decoupling point for customer orders.</span></span> <span data-ttu-id="67e87-106">拡張された需要予測の削減ルールは、大量のカスタマイズに理想的なソリューションを提供します。</span><span class="sxs-lookup"><span data-stu-id="67e87-106">The enhanced demand forecast reduction rules provide an ideal solution for mass customization.</span></span>

<span data-ttu-id="67e87-107">ベースラインの予測を生成するには、履歴トランザクション集計が Azure でホストされている Microsoft Azure Machine Learning に転送されます。</span><span class="sxs-lookup"><span data-stu-id="67e87-107">To generate the baseline forecast, a summary of historical transactions is passed to Microsoft Azure Machine Learning hosted on Azure.</span></span> <span data-ttu-id="67e87-108">このサービスはユーザー間で共有されないため、業界固有の要件に合わせて、簡単にカスタマイズできます。</span><span class="sxs-lookup"><span data-stu-id="67e87-108">Because this service isn't shared among users, it can easily be customized to meet industry-specific requirements.</span></span> <span data-ttu-id="67e87-109">Supply Chain Management を使用して、予測を視覚化し、予測を調整し、予測精度に関する主要業績評価指標 (KPI) を表示することができます。</span><span class="sxs-lookup"><span data-stu-id="67e87-109">You can use Supply Chain Management to visualize the forecast, adjust the forecast, and view key performance indicators (KPIs) about forecast accuracy.</span></span>

## <a name="key-features-of-demand-forecasting"></a><span data-ttu-id="67e87-110">需要予測の主な機能</span><span class="sxs-lookup"><span data-stu-id="67e87-110">Key features of demand forecasting</span></span>
<span data-ttu-id="67e87-111">需要予測の主な特長を次に示します。</span><span class="sxs-lookup"><span data-stu-id="67e87-111">Here are some of the main features of demand forecasting:</span></span>

-   <span data-ttu-id="67e87-112">履歴データに基づいて統計ベースライン予測を生成します。</span><span class="sxs-lookup"><span data-stu-id="67e87-112">Generate a statistical baseline forecast that is based on historical data.</span></span>
-   <span data-ttu-id="67e87-113">動的セットの予測分析コードを使用します。</span><span class="sxs-lookup"><span data-stu-id="67e87-113">Use a dynamic set of forecast dimensions.</span></span>
-   <span data-ttu-id="67e87-114">需要傾向、信頼区間と予測調整を視覚化します。</span><span class="sxs-lookup"><span data-stu-id="67e87-114">Visualize demand trends, confidence intervals, and adjustments of the forecast.</span></span>
-   <span data-ttu-id="67e87-115">計画プロセスで使用する調整された予測を承認します。</span><span class="sxs-lookup"><span data-stu-id="67e87-115">Authorize the adjusted forecast to be used in planning processes.</span></span>
-   <span data-ttu-id="67e87-116">異常値を削除します。</span><span class="sxs-lookup"><span data-stu-id="67e87-116">Remove outliers.</span></span>
-   <span data-ttu-id="67e87-117">予測精度の測定を作成します。</span><span class="sxs-lookup"><span data-stu-id="67e87-117">Create measurements of forecast accuracy.</span></span>

## <a name="major-themes-in-demand-forecasting"></a><span data-ttu-id="67e87-118">需要予測の主要テーマ</span><span class="sxs-lookup"><span data-stu-id="67e87-118">Major themes in demand forecasting</span></span>
<span data-ttu-id="67e87-119">3 つの主要なテーマの需要予測が実装できます。</span><span class="sxs-lookup"><span data-stu-id="67e87-119">Three major themes are implemented in demand forecasting:</span></span>

-   <span data-ttu-id="67e87-120">**モジュール性** – 需要予測はモジュールおよびコンフィギュレーションが簡単にできます。</span><span class="sxs-lookup"><span data-stu-id="67e87-120">**Modularity** – Demand forecasting is modular and easy to configure.</span></span> <span data-ttu-id="67e87-121">**販売** &gt; **在庫予測** &gt; **需要予測** で構成キーの機能をオン/オフに変更できます。</span><span class="sxs-lookup"><span data-stu-id="67e87-121">You can turn the functionality on and off by changing the configuration key at **Trade** &gt; **Inventory forecast** &gt; **Demand forecasting**.</span></span>
-   <span data-ttu-id="67e87-122">**Microsoft Stack の再利用** – Microsoft Cortana Analytics Suite の一部である Machine Learning を使用すると、アルゴリズム R または Python プログラミング言語、およびシンプルなドラッグ アンド ドロップ インターフェースを使用して、需要見積もりの試算などの予測分析実験をすばやく簡単に作成できます。</span><span class="sxs-lookup"><span data-stu-id="67e87-122">**Reuse of the Microsoft stack** – Machine Learning, which is part of the Microsoft Cortana Analytics Suite, lets you quickly and easily create predictive analysis experiments, such as demand estimation experiments, by using algorithms R or Python programming languages and a simple drag-and-drop interface.</span></span>
    -   <span data-ttu-id="67e87-123">需要予測実験をダウンロードし、業務要件に合わせて変更し、Azure の Web サービスとして公開し、需要予測の生成にそれらを使用することができます。</span><span class="sxs-lookup"><span data-stu-id="67e87-123">You can download the Demand forecasting experiments, change them to meet your business requirements, publish them as a web service on Azure, and use them to generate demand forecasts.</span></span> <span data-ttu-id="67e87-124">エンタープライズ レベルのユーザーとして、生産計画担当者向けに Supply Chain Management サブスクリプションを購入した場合は、この実験をダウンロードできます。</span><span class="sxs-lookup"><span data-stu-id="67e87-124">The experiments are available for download if you've purchased a Supply Chain Management subscription for a production planner as enterprise level user.</span></span>
    -   <span data-ttu-id="67e87-125">[Cortana Analytics Gallery](https://gallery.cortanaanalytics.com/) から現在有効な需要予測実験をダウンロードできます。</span><span class="sxs-lookup"><span data-stu-id="67e87-125">You can download any of the currently available demand prediction experiments from the [Cortana Analytics Gallery](https://gallery.cortanaanalytics.com/).</span></span> <span data-ttu-id="67e87-126">需要予測実験は Supply Chain Management と自動的に統合されるので、顧客およびパートナーは [Cortana Analytics Gallery](https://gallery.cortanaanalytics.com/) からダウンロードした実験の統合を処理する必要があります。</span><span class="sxs-lookup"><span data-stu-id="67e87-126">Whereas the Demand forecasting experiments are automatically integrated with Supply Chain Management, customers and partners must handle the integration of experiments that they download from the [Cortana Analytics Gallery](https://gallery.cortanaanalytics.com/).</span></span> <span data-ttu-id="67e87-127">したがって、[Cortana Analytics Gallery](https://gallery.cortanaanalytics.com/) の実験が Finance and Operations の需要予測実験として使用できるわけではありません。</span><span class="sxs-lookup"><span data-stu-id="67e87-127">Therefore, experiments from the [Cortana Analytics Gallery](https://gallery.cortanaanalytics.com/) aren't as straightforward to use as the Finance and Operations Demand forecasting experiments.</span></span> <span data-ttu-id="67e87-128">Finance and Operations アプリケーション プログラミング インターフェイス (API) を使用するための実験コードを変更する必要があります。</span><span class="sxs-lookup"><span data-stu-id="67e87-128">You must modify the code of the experiments so that they use the Finance and Operations application programming interface (API).</span></span>
    -   <span data-ttu-id="67e87-129">Microsoft Azure Machine Learning Studio (クラシック) で独自の実験を作成し、Azure のサービスとして発行、そして需要予測の生成に使用することができます。</span><span class="sxs-lookup"><span data-stu-id="67e87-129">You can create your own experiments in Microsoft Azure Machine Learning Studio (classic), publish them as services on Azure, and use them to generate demand forecasts.</span></span>
    -   <span data-ttu-id="67e87-130">高パフォーマンスが必要でない場合、または大量のデータの処理が要求されていない場合に、Machine Learning 無料レベルを使用できます。</span><span class="sxs-lookup"><span data-stu-id="67e87-130">If you don’t require high performance, or if you don't require that a large amount of data be processed, you can use the Machine Learning free tier.</span></span> <span data-ttu-id="67e87-131">特に実装およびテスト フェーズの際には、このレベルから常に開始することをお勧めします。</span><span class="sxs-lookup"><span data-stu-id="67e87-131">We recommend that you always start from this tier, especially during implementation and testing phases.</span></span> <span data-ttu-id="67e87-132">高パフォーマンスと追加のストレージが必要な場合、Machine Learning 標準レベルを使用できます。</span><span class="sxs-lookup"><span data-stu-id="67e87-132">If you require higher performance and additional storage, you can use the Machine Learning standard tier.</span></span> <span data-ttu-id="67e87-133">この層には、Azure のサブスクリプションが要求され、追加費用が含まれます。</span><span class="sxs-lookup"><span data-stu-id="67e87-133">This tier requires an Azure subscription and involves additional costs.</span></span> <span data-ttu-id="67e87-134">Machine Learning 価格設定の詳細については、[Machine Learning Studio の価格](https://aka.ms/machine-learning-price-info)を参照ください。</span><span class="sxs-lookup"><span data-stu-id="67e87-134">For details about Machine Learning pricing, see [Machine Learning Studio pricing](https://aka.ms/machine-learning-price-info).</span></span>
-   <span data-ttu-id="67e87-135">**減結合ポイントの予測下方修正** - すべての減結合ポイントで依存要求と独立要求の両方を予測するこの機能で、ビルドでの需要予測を作成します。</span><span class="sxs-lookup"><span data-stu-id="67e87-135">**Forecast reduction at any decoupling point** – Demand forecasting in builds on this functionality, which lets you forecast both dependent and independent demand at any decoupling point.</span></span>

## <a name="basic-flow-in-demand-forecasting"></a><span data-ttu-id="67e87-136">需要予測の基本フロー</span><span class="sxs-lookup"><span data-stu-id="67e87-136">Basic flow in demand forecasting</span></span>
<span data-ttu-id="67e87-137">次の図は、需要予測の基本フローを表示します。</span><span class="sxs-lookup"><span data-stu-id="67e87-137">The following diagram shows the basic flow in demand forecasting.</span></span> 

<span data-ttu-id="67e87-138">[![需要予測の導入図](./media/demand-forecasting-introduction.png)](./media/demand-forecasting-introduction.png)</span><span class="sxs-lookup"><span data-stu-id="67e87-138">[![demand forecasting introduction diagram](./media/demand-forecasting-introduction.png)](./media/demand-forecasting-introduction.png)</span></span>

<span data-ttu-id="67e87-139">需要予測の生成は、Supply Chain Management で開始されます。</span><span class="sxs-lookup"><span data-stu-id="67e87-139">Demand forecast generation starts in Supply Chain Management.</span></span> <span data-ttu-id="67e87-140">Supply Chain Management トランザクション データベースからの履歴トランザクション データが収集され、ステージング テーブルに値が入力されます。</span><span class="sxs-lookup"><span data-stu-id="67e87-140">Historical transactional data from the Supply Chain Management transactional database is gathered and populates a staging table.</span></span> <span data-ttu-id="67e87-141">このステージング テーブルが Machine Learning サービスに後ほど提供されます。</span><span class="sxs-lookup"><span data-stu-id="67e87-141">This staging table is later fed to a Machine Learning service.</span></span> <span data-ttu-id="67e87-142">最低限のカスタマイズで、さまざまなデータ ソースをステージング テーブルにプラグできます。</span><span class="sxs-lookup"><span data-stu-id="67e87-142">By performing minimal customization, you can plug various data sources into the staging table.</span></span> <span data-ttu-id="67e87-143">データ ソースには、Microsoft Excel ファイル、コンマ区切り値 (CSV) ファイル、および Microsoft Dynamics AX 2009 と Microsoft Dynamics AX 2012 からのデータが含まれます。</span><span class="sxs-lookup"><span data-stu-id="67e87-143">The data sources can include Microsoft Excel files, comma-separated value (CSV) files, and data from Microsoft Dynamics AX 2009 and Microsoft Dynamics AX 2012.</span></span> <span data-ttu-id="67e87-144">したがって、複数のシステムにまたがった履歴データを考慮する需要予測を生成できます。</span><span class="sxs-lookup"><span data-stu-id="67e87-144">Therefore, you can generate demand forecasts that consider historical data that is spread among multiple systems.</span></span> <span data-ttu-id="67e87-145">ただし、品目名、販売単位などのマスター データは、さまざまなデータ ソース間でも同じである必要があります。</span><span class="sxs-lookup"><span data-stu-id="67e87-145">However, the master data, such as item names and units of measure, must be the same across the various data sources.</span></span>

<span data-ttu-id="67e87-146">需要予測 Machine Learning 実験を使用すると、ベースライン予測を計算するための 5 つのタイム シリーズ の予測方法の中から最も適切なものを検索します。</span><span class="sxs-lookup"><span data-stu-id="67e87-146">If you use the Demand forecasting Machine Learning experiments, they look for a best fit among five time series forecasting methods to calculate a baseline forecast.</span></span> <span data-ttu-id="67e87-147">予測方法のパラメーターは Supply Chain Management で管理されます。</span><span class="sxs-lookup"><span data-stu-id="67e87-147">The parameters for these forecasting methods are managed in Supply Chain Management.</span></span> 

<span data-ttu-id="67e87-148">以前の項目での、予測、履歴データ、および変更点などの需要予測が Supply Chain Management で次に利用可能です。</span><span class="sxs-lookup"><span data-stu-id="67e87-148">The forecasts, historical data, and any changes that were made to the demand forecasts in previous iterations are then available in Supply Chain Management.</span></span> 

<span data-ttu-id="67e87-149">Supply Chain Management を使用してベースラインの予測を視覚化し修正できます。</span><span class="sxs-lookup"><span data-stu-id="67e87-149">You can use Supply Chain Management to visualize and modify the baseline forecasts.</span></span> <span data-ttu-id="67e87-150">手動調整は、予測計画で使用する前に承認する必要があります。</span><span class="sxs-lookup"><span data-stu-id="67e87-150">Manual adjustments must be authorized before the forecasts can be used for planning.</span></span>

## <a name="limitations"></a><span data-ttu-id="67e87-151">制限</span><span class="sxs-lookup"><span data-stu-id="67e87-151">Limitations</span></span>
<span data-ttu-id="67e87-152">需要予測は、予測プロセスを作成する製造業界の顧客を支援するツールです。</span><span class="sxs-lookup"><span data-stu-id="67e87-152">Demand forecasting is a tool that helps customers in the manufacturing industry create forecasting processes.</span></span> <span data-ttu-id="67e87-153">需要予測ソリューションの核となる機能を提供し、簡単に拡張できるように設計されています。</span><span class="sxs-lookup"><span data-stu-id="67e87-153">It offers the core functionality of a demand forecasting solution and is designed so that it can easily be extended.</span></span> <span data-ttu-id="67e87-154">需要予測は、商業、卸売業、倉庫保管、輸送業、または他の専門的なサービス産業の顧客には最適ではない場合があります。</span><span class="sxs-lookup"><span data-stu-id="67e87-154">Demand forecasting might not be the best fit for customers in industries such as commerce, wholesale, warehousing, transportation, or other professional services.</span></span>

### <a name="demand-forecast-variant-conversion-limitation"></a><span data-ttu-id="67e87-155">需要予測バリアント変換の制限</span><span class="sxs-lookup"><span data-stu-id="67e87-155">Demand forecast variant conversion limitation</span></span>

<span data-ttu-id="67e87-156">バリアント変換ごとの測定単位 (UOM) は、在庫単位が需要予測単位と異なる場合、需要予測の生成時に完全にはサポートされません。</span><span class="sxs-lookup"><span data-stu-id="67e87-156">Unit of measure (UOM) per variant conversion is not fully supported when generating demand forecast if inventory UOM is different than the demand forecast UOM.</span></span>

<span data-ttu-id="67e87-157">予測の生成 ( **在庫単位 > 需要予測単位**) では、製品単位の変換を使用します。</span><span class="sxs-lookup"><span data-stu-id="67e87-157">Generating forecast (**Inventory UOM > Demand forecast UOM**) uses product UOM conversion.</span></span> <span data-ttu-id="67e87-158">需要予測生成の履歴データを読み込む場合、バリアント レベルで変換が定義されていても、在庫単位から需要予測単位に変換するときは製品レベルの単位変換が常に使用されます。</span><span class="sxs-lookup"><span data-stu-id="67e87-158">When loading historical data for the demand forecast generation, the product level UOM conversion will be always used when converting from inventory UOM to the demand forecast UOM, even if there are conversions defined on the variant level.</span></span>

<span data-ttu-id="67e87-159">予測の承認の最初の部分 (**需要予測単位 > 在庫単位**) では、製品単位の変換を使用します。</span><span class="sxs-lookup"><span data-stu-id="67e87-159">The first part of authorizing forecast (**Demand forecast UOM > Inventory UOM**) uses product UOM conversion.</span></span> <span data-ttu-id="67e87-160">予測の承認の 2 番目の部分 (**在庫単位 > 販売単位**) では、バリアント単位の変換を使用します。</span><span class="sxs-lookup"><span data-stu-id="67e87-160">The second part of authorizing forecast (**Inventory UOM > Sales UOM**) uses the variant UOM conversion.</span></span> <span data-ttu-id="67e87-161">生成された需要予測が承認されると、需要予測単位から在庫単位への変換は、製品レベルの単位の変換を使用して行われます。</span><span class="sxs-lookup"><span data-stu-id="67e87-161">When the generated demand forecast is authorized, the conversion to inventory UOM from demand forecast UOM will be done using product level UOM conversion.</span></span> <span data-ttu-id="67e87-162">同時に、在庫単位と販売単位の間の変換では、バリアント レベルで定義された変換が考慮されます。</span><span class="sxs-lookup"><span data-stu-id="67e87-162">At the same time, conversion between the inventory unit and the sales UOM will respect the variant level defined conversions.</span></span>

<span data-ttu-id="67e87-163">需要予測単位は特定の意味を持つ必要はないことに注意してください。</span><span class="sxs-lookup"><span data-stu-id="67e87-163">Note that the demand forecast UOM does not have to have any specific meaning.</span></span> <span data-ttu-id="67e87-164">"需要予測単位" と定義できます。</span><span class="sxs-lookup"><span data-stu-id="67e87-164">It can be defined as “Demand forecast unit”.</span></span> <span data-ttu-id="67e87-165">各製品について、在庫単位を使用して変換を 1:1 に定義できます。</span><span class="sxs-lookup"><span data-stu-id="67e87-165">For each of the products, you can define the conversion to be 1:1 with the inventory UOM.</span></span>

<a name="additional-resources"></a><span data-ttu-id="67e87-166">追加リソース</span><span class="sxs-lookup"><span data-stu-id="67e87-166">Additional resources</span></span>
--------

[<span data-ttu-id="67e87-167">需要予測の設定</span><span class="sxs-lookup"><span data-stu-id="67e87-167">Demand forecasting setup</span></span>](demand-forecasting-setup.md)

[<span data-ttu-id="67e87-168">統計ベースライン予測の生成</span><span class="sxs-lookup"><span data-stu-id="67e87-168">Generate a statistical baseline forecast</span></span>](generate-statistical-baseline-forecast.md)

[<span data-ttu-id="67e87-169">ベースライン予測に対して手動調整を行う</span><span class="sxs-lookup"><span data-stu-id="67e87-169">Make manual adjustments to the baseline forecast</span></span>](manual-adjustments-baseline-forecast.md)

[<span data-ttu-id="67e87-170">調整された需要予測の承認</span><span class="sxs-lookup"><span data-stu-id="67e87-170">Authorize an adjusted forecast</span></span>](authorize-adjusted-forecast.md)

[<span data-ttu-id="67e87-171">予測精度の監視</span><span class="sxs-lookup"><span data-stu-id="67e87-171">Monitor forecast accuracy</span></span>](monitor-forecast-accuracy.md)

[<span data-ttu-id="67e87-172">需要予測を計算するときに、トランザクション履歴データから異常値を削除</span><span class="sxs-lookup"><span data-stu-id="67e87-172">Remove outliers from historical transaction data when calculating a demand forecast</span></span>](remove-historical-outliers-calculating-demand-forecast.md)

[<span data-ttu-id="67e87-173">Extend the demand forecasting functionality (需要予測機能の拡張)</span><span class="sxs-lookup"><span data-stu-id="67e87-173">Extend the demand forecasting functionality</span></span>](https://www.youtube.com/watch?v=4OIKIXLiNjI&feature=youtu.be)



