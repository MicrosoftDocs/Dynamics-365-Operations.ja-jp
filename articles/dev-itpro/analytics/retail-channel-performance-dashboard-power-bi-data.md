---
title: "販売チャネル パフォーマンス Power BI コンテンツ"
description: "このトピックでは、Dynamics AX 7.0 リリースの Retail チャネル パフォーマンス Power BI コンテンツに関する情報を提供します。 このコンテンツ パックを使用すると、チャネル パフォーマンス アナリティクスを迅速にビルドして、販売実績に基づいて傾向を予測し、洞察を得ることができます。"
author: ashishmsft
manager: AnnBe
ms.date: 02/02/2018
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-platform
ms.technology: 
audience: IT Pro
ms.reviewer: sericks
ms.search.scope: Operations
ms.custom: 105483
ms.assetid: cb5aff3b-5b29-44f7-9c6f-6b055c043996
ms.search.region: Global
ms.author: asharchw
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: efcb77ff883b29a4bbaba27551e02311742afbbd
ms.openlocfilehash: 9d1ed35f0886506024c93ebc2e5e763c99c1f8b2
ms.contentlocale: ja-jp
ms.lasthandoff: 05/08/2018

---

# <a name="retail-channel-performance-power-bi-content"></a><span data-ttu-id="331a2-104">販売チャネル パフォーマンス Power BI コンテンツ</span><span class="sxs-lookup"><span data-stu-id="331a2-104">Retail channel performance Power BI content</span></span>

[!include [banner](../includes/banner.md)]

> [!Note]
> <span data-ttu-id="331a2-105">このコンテンツ パックは [Power BI コンテンツ パックを PowerBI.com に公開する](https://docs.microsoft.com/en-us/dynamics365/unified-operations/dev-itpro/migration-upgrade/deprecated-features#power-bi-content-packs-published-to-powerbicom)で記載されたものとして非推奨になっています。</span><span class="sxs-lookup"><span data-stu-id="331a2-105">This content pack has been deprecated as documented in [Power BI content packs published to PowerBI.com](https://docs.microsoft.com/en-us/dynamics365/unified-operations/dev-itpro/migration-upgrade/deprecated-features#power-bi-content-packs-published-to-powerbicom).</span></span>

<span data-ttu-id="331a2-106">このトピックでは、Dynamics AX の Retail チャネル パフォーマンス Power BI コンテンツに関する情報を提供します。</span><span class="sxs-lookup"><span data-stu-id="331a2-106">This topic provides information about the Retail channel performance Power BI content for Dynamics AX.</span></span> <span data-ttu-id="331a2-107">このコンテンツ パックを使用すると、チャネル パフォーマンス アナリティクスを迅速にビルドして、販売実績に基づいて傾向を予測し、洞察を得ることができます。</span><span class="sxs-lookup"><span data-stu-id="331a2-107">This content pack lets channel managers quickly build channel performance analytics to predict trends and uncover insights, based on sales performance.</span></span>

<span data-ttu-id="331a2-108">Retail チャンネル パフォーマンス コンテンツ パックを使用すると、チャネル パフォーマンスの分析機能をすばやく作成することができます。</span><span class="sxs-lookup"><span data-stu-id="331a2-108">The Retail channel performance content pack lets you quickly build your channel performance analytics.</span></span> <span data-ttu-id="331a2-109">コンテンツ パックは、販売実績に焦点を当てて傾向を予測し、洞察を明らかにするチャネル マネージャー専用に設計されています。</span><span class="sxs-lookup"><span data-stu-id="331a2-109">The content pack is designed specifically for channel managers who focus on sales performance to predict trends and uncover insights.</span></span> <span data-ttu-id="331a2-110">そのコンポーネントは、Dynamics AX データベースで Retail と Commerce のデータから直接を取得し、従業員、カテゴリ、製品、ターミナル、チャネルなどによって地理的に世界中の組織全体の販売実績に関するドリルダウン レポートを提供します。</span><span class="sxs-lookup"><span data-stu-id="331a2-110">Its components draw directly from Retail and commerce data in the Dynamics AX database, and provide drill-down reports about organization-wide sales performance across global geography by employee, category, product, terminal, channel, and more.</span></span> <span data-ttu-id="331a2-111">Power BI は、小売およびコマース データを調査して分析するための良い出発点となる、レポートとダッシュボードに自動的に作成します。</span><span class="sxs-lookup"><span data-stu-id="331a2-111">Power BI automatically creates reports and dashboards that give you a great starting point for exploring and analyzing your Retail and commerce data.</span></span> <span data-ttu-id="331a2-112">この記事には、次の情報が含まれています。</span><span class="sxs-lookup"><span data-stu-id="331a2-112">This article includes the following information:</span></span>

-   <span data-ttu-id="331a2-113">Power BI の Retail チャネル パフォーマンス コンテンツ パックを Dynamics AX データ ソースに接続する方法について説明します。</span><span class="sxs-lookup"><span data-stu-id="331a2-113">Learn how to connect the Retail channel performance content pack in Power BI to a Dynamics AX data source.</span></span>
-   <span data-ttu-id="331a2-114">小売チャネルの実績に関する詳細情報を提供するレポートの一覧を表示します。</span><span class="sxs-lookup"><span data-stu-id="331a2-114">View a list of reports that provide insights into retail channel performance.</span></span>
-   <span data-ttu-id="331a2-115">コンテンツ パックの既存のレポートを変更して自分で作成する方法について説明します。</span><span class="sxs-lookup"><span data-stu-id="331a2-115">Learn how to modify an existing report in the content pack to make it self-authored.</span></span>
-   <span data-ttu-id="331a2-116">Power BI でのエクスペリエンス全体を有効にする実際のデータ モデルのほんの一部を取得します。</span><span class="sxs-lookup"><span data-stu-id="331a2-116">Get a glimpse of an actual data model that enables the whole experience in Power BI.</span></span>

## <a name="connect-the-retail-channel-performance-content-pack-in-power-bi-to-a-dynamics-ax-data-source"></a><span data-ttu-id="331a2-117">Power BI の小売チャネル パフォーマンス コンテンツ パックを Dynamics AX データ ソースに接続する</span><span class="sxs-lookup"><span data-stu-id="331a2-117">Connect the Retail channel performance content pack in Power BI to a Dynamics AX data source</span></span>
1.  <span data-ttu-id="331a2-118">https://www.powerbi.com に移動し、**サインイン**をクリックします。</span><span class="sxs-lookup"><span data-stu-id="331a2-118">Go to https://www.powerbi.com, and click **Sign in**.</span></span> <span data-ttu-id="331a2-119">アカウントがない場合は、サインアップし、新しい Power BI を無料でプレビューできます。</span><span class="sxs-lookup"><span data-stu-id="331a2-119">If you don't have an account, you can sign up to try the new Power BI Preview for free.</span></span>
2.  <span data-ttu-id="331a2-120">サインインするには、Power BI アカウントを持つ Microsoft Office 365 アカウントを入力します。</span><span class="sxs-lookup"><span data-stu-id="331a2-120">To sign in, enter a Microsoft Office 365 account that has a Power BI account.</span></span>
3.  <span data-ttu-id="331a2-121">ワークスペースが表示されたら、左のナビゲーション ウィンドウの下部にある**データの取得**をクリックします。</span><span class="sxs-lookup"><span data-stu-id="331a2-121">If your workspace appears, click **Get Data** at the bottom of the left navigation pane.</span></span>
4.  <span data-ttu-id="331a2-122">**サービス** セクションで、**取得**をクリックします。</span><span class="sxs-lookup"><span data-stu-id="331a2-122">In **Services** section, click **Get**.</span></span>
5.  <span data-ttu-id="331a2-123">スクロールするか検索して **Microsoft Dynamics AX Retail チャネル パフォーマンス** を見つけ、**今すぐ入手** をクリックします。</span><span class="sxs-lookup"><span data-stu-id="331a2-123">Scroll or search to find **Microsoft Dynamics AX Retail channel performance**, and then click **Get it now**.</span></span>
6.  <span data-ttu-id="331a2-124">次の形式に Dynamics AX の URL を入力します `https://<tenant>.cloudax.dynamics.com` (たとえば、`https://YourAOSTenant.cloudax.dynamics.com`)。</span><span class="sxs-lookup"><span data-stu-id="331a2-124">Enter your Dynamics AX URL in the following format: `https://<tenant>.cloudax.dynamics.com` (for example, `https://YourAOSTenant.cloudax.dynamics.com`).</span></span> <span data-ttu-id="331a2-125">次に、**Next** をクリックして Dynamics AX データ ストレージからこの Power BI ダッシュボードにデータをプルします。</span><span class="sxs-lookup"><span data-stu-id="331a2-125">Then click **Next** to pull data from Dynamics AX data storage into this Power BI dashboard.</span></span>
7.  <span data-ttu-id="331a2-126">認証方法として **oAuth2** を選択し、**署名する** をクリックします。</span><span class="sxs-lookup"><span data-stu-id="331a2-126">Select **oAuth2** as the authentication method, and then click **Sign in**.</span></span>
8.  <span data-ttu-id="331a2-127">サインインするには、Dynamics AX 環境にアクセスするアクセス許可を持つ Office 365 のアカウントを入力します。</span><span class="sxs-lookup"><span data-stu-id="331a2-127">To sign in, enter an Office 365 account that has permission to access your Dynamics AX environment.</span></span>
9.  <span data-ttu-id="331a2-128">データが Dynamics AX から Power BI に正常に引き込まれた後、左のナビゲーション ウィンドウで**小売チャネルの実績ダッシュボード**をクリックして、Power BI の個人の**小売チャネルの実績**を表示することができます。</span><span class="sxs-lookup"><span data-stu-id="331a2-128">After data is successfully pulled from Dynamics AX into Power BI, you can view your personal **Retail channel performance** dashboard in Power BI by clicking **Retail channel performance dashboard** in the left navigation pane.</span></span> <span data-ttu-id="331a2-129">[![小売チャンネル パフォーマンス ダッシュボード](./media/rcmpbidashboard-1024x679.png)](./media/rcmpbidashboard.png)</span><span class="sxs-lookup"><span data-stu-id="331a2-129">[![Retail channel performance dashboard](./media/rcmpbidashboard-1024x679.png)](./media/rcmpbidashboard.png)</span></span>
10. <span data-ttu-id="331a2-130">自然言語を使用することにより、Power BI 内の Q&A フィーチャーを活用して Dynamics AX の営業データをクエリすることができます。</span><span class="sxs-lookup"><span data-stu-id="331a2-130">You can then take advantage of the Q&A feature in Power BI to query your Dynamics AX sales data by using natural language.</span></span> <span data-ttu-id="331a2-131">[![Power BI にある Q&A 機能](./media/qnapbiretailchannelperformance.png)](./media/qnapbiretailchannelperformance.png)</span><span class="sxs-lookup"><span data-stu-id="331a2-131">[![Q&A feature in Power BI](./media/qnapbiretailchannelperformance.png)](./media/qnapbiretailchannelperformance.png)</span></span>

## <a name="view-a-list-of-reports"></a><span data-ttu-id="331a2-132">レポートの一覧の表示</span><span class="sxs-lookup"><span data-stu-id="331a2-132">View a list of reports</span></span>
<span data-ttu-id="331a2-133">ダッシュボードの固定されたタイルのいずれかをクリックすると、小売チャネルの実績に関する情報を提供する次の一覧に移動できます。</span><span class="sxs-lookup"><span data-stu-id="331a2-133">By clicking through any of the pinned tiles on the dashboard, you can navigate the following list of reports that provide insights into retail channel performance:</span></span>

-   <span data-ttu-id="331a2-134">地理的な販売配布</span><span class="sxs-lookup"><span data-stu-id="331a2-134">Geographical sales distribution</span></span>
-   <span data-ttu-id="331a2-135">カテゴリ販売実績</span><span class="sxs-lookup"><span data-stu-id="331a2-135">Category sales performance</span></span>
-   <span data-ttu-id="331a2-136">支払/入金タイプまたは支払方法ごとの売上集計</span><span class="sxs-lookup"><span data-stu-id="331a2-136">Sales summary by Tender type or payment method</span></span>
-   <span data-ttu-id="331a2-137">従業員の月次パフォーマンス</span><span class="sxs-lookup"><span data-stu-id="331a2-137">Employee monthly performance</span></span>
-   <span data-ttu-id="331a2-138">店舗の月次パフォーマンス</span><span class="sxs-lookup"><span data-stu-id="331a2-138">Store monthly performance</span></span>
-   <span data-ttu-id="331a2-139">特定の店舗での特定のカテゴリにおける製品の販売実績</span><span class="sxs-lookup"><span data-stu-id="331a2-139">Product sales performance for the given category in the given store</span></span>

<span data-ttu-id="331a2-140">たとえば、地理的な販売流通のより深い分析を実行する場合があります。</span><span class="sxs-lookup"><span data-stu-id="331a2-140">For example, you might want to do a deeper analysis of geographical sales distribution.</span></span> 

<span data-ttu-id="331a2-141">[![地理的販売配送レポート](./media/slicendicegeographicalsalesdata-1024x715.png)](./media/slicendicegeographicalsalesdata.png)</span><span class="sxs-lookup"><span data-stu-id="331a2-141">[![Geographical sales distribution report](./media/slicendicegeographicalsalesdata-1024x715.png)](./media/slicendicegeographicalsalesdata.png)</span></span>

## <a name="modify-an-existing-report-in-the-content-pack-to-make-it-self-authored"></a><span data-ttu-id="331a2-142">コンテンツ パックの既存のレポートを変更して自分で作成する</span><span class="sxs-lookup"><span data-stu-id="331a2-142">Modify an existing report in the content pack to make it self-authored</span></span>
<span data-ttu-id="331a2-143">コンテンツ パックの既存のレポートを変更して自己作成できるようにする簡単な例を次に示します。</span><span class="sxs-lookup"><span data-stu-id="331a2-143">Here's an example that shows how easy it is to modify an existing report in the content pack to make it self-authored.</span></span> <span data-ttu-id="331a2-144">この例では、**カテゴリおよび製品のパフォーマンス**という名前の既存のレポートを、そのレポートの**カテゴリ レベル 1** を**月 / 年ごとの合計金額**グラフに追加することで変更します。</span><span class="sxs-lookup"><span data-stu-id="331a2-144">In this example, we will modify an existing report that is named **Category & product performance** by adding **Category level 1** to the **Total amount by Month/Year** chart on that report.</span></span>

1.  <span data-ttu-id="331a2-145">ウィンドウの下部にある **CategoryProductPerformance** タブをクリックし、**カテゴリ、および製品のパフォーマンス** レポートを開きます。次に、**レポートの編集**をクリックします。</span><span class="sxs-lookup"><span data-stu-id="331a2-145">Click the **CategoryProductPerformance** tab at the bottom of the window to open the **Category & product performance** report, and then click **Edit report**.</span></span> <span data-ttu-id="331a2-146">[![レポートの編集](./media/editreport-1024x580.png)](./media/editreport.png)</span><span class="sxs-lookup"><span data-stu-id="331a2-146">[![Edit report](./media/editreport-1024x580.png)](./media/editreport.png)</span></span>
2.  <span data-ttu-id="331a2-147">**月/年ごとの合計金額** というグラフを選択します。</span><span class="sxs-lookup"><span data-stu-id="331a2-147">Select the chart that is named **Total amount by Month/Year**.</span></span> <span data-ttu-id="331a2-148">その後、ウィンドウの右側の **Fields** ウィンドウで、**既定小売品目カテゴリ階層** ノードを展開します。</span><span class="sxs-lookup"><span data-stu-id="331a2-148">Then, on the right side of the window, in the **Fields** pane, expand the **Default Retail Product Category Hierarchy** node.</span></span> <span data-ttu-id="331a2-149">[![月/年グラフによる合計金額の既定小売品目カテゴリ階層ノード](./media/editreportstep2-1024x624.png)](./media/editreportstep2.png)</span><span class="sxs-lookup"><span data-stu-id="331a2-149">[![Default Retail Product Category Hierarchy node for the Total amount by Month/Year chart](./media/editreportstep2-1024x624.png)](./media/editreportstep2.png)</span></span>
3.  <span data-ttu-id="331a2-150">この階層のカテゴリ レベルの一覧で**カテゴリ レベル 1** を選択します。</span><span class="sxs-lookup"><span data-stu-id="331a2-150">In the list of category levels for this hierarchy, select **Category Level 1**.</span></span> <span data-ttu-id="331a2-151">**月/年とカテゴリ レベル 1 グラフごとの合計金額** に変更するためにこの属性を選択したグラフの名前。このグラフでは、各カテゴリの売上シェアを毎月表示します。</span><span class="sxs-lookup"><span data-stu-id="331a2-151">The name of the chart that you selected this attribute for changes to **Total amount by Month/Year and Category level 1**, and the chart now shows the share of sales in each category for each month.</span></span> <span data-ttu-id="331a2-152">[![月 / 年とカテゴリレベル 1 グラフごとの合計金額](./media/editreportstep3-1024x625.png)](./media/editreportstep3.png)</span><span class="sxs-lookup"><span data-stu-id="331a2-152">[![Total amount by Month/Year and Category level 1 chart](./media/editreportstep3-1024x625.png)](./media/editreportstep3.png)</span></span>
4.  <span data-ttu-id="331a2-153">最後に、視覚化自体を変更するようにしてください。</span><span class="sxs-lookup"><span data-stu-id="331a2-153">Finally, try to change the visualization itself.</span></span> <span data-ttu-id="331a2-154">**月/年とカテゴリ レベル 1 ごとの合計金額** グラフを選択し、**ビジュアル化** ウィンドウで **面グラフ** または **積み上げ面グラフ** をクリックして結果を確認します。</span><span class="sxs-lookup"><span data-stu-id="331a2-154">Select the **Total amount by Month/Year and Category level 1** chart, and then, in the **Visualizations** pane, click **Area chart** or **Stacked area chart**, and see the effect.</span></span> <span data-ttu-id="331a2-155">[![月/年およびカテゴリレベル 1 のグラフによる合計金額の視覚化の変更](./media/editreportstep4-1024x630.png)](./media/editreportstep4.png)</span><span class="sxs-lookup"><span data-stu-id="331a2-155">[![Changing the visualization of the Total amount by Month/Year and Category level 1 chart](./media/editreportstep4-1024x630.png)](./media/editreportstep4.png)</span></span>

## <a name="get-a-glimpse-of-the-actual-data-model"></a><span data-ttu-id="331a2-156">実際のデータ モデルのほんの一部を取得します</span><span class="sxs-lookup"><span data-stu-id="331a2-156">Get a glimpse of the actual data model</span></span>
<span data-ttu-id="331a2-157">Dynamics AX データ エンティティおよび集約データ エンティティのコンテンツ パックに含まれているデータ モデルを使用すると、さまざまな分析コードを使用してさまざまな測定間でスライスおよびダイスすることができます。</span><span class="sxs-lookup"><span data-stu-id="331a2-157">The data model that is included in the content pack for the Dynamics AX data entities and aggregated data entities lets you slice and dice across various measures by using different dimensions.</span></span> <span data-ttu-id="331a2-158">[![データ モデル](./media/datamodeltomakeslicingndicingpossibleinrcm-1024x600.png)](./media/datamodeltomakeslicingndicingpossibleinrcm.png)</span><span class="sxs-lookup"><span data-stu-id="331a2-158">[![Data model](./media/datamodeltomakeslicingndicingpossibleinrcm-1024x600.png)](./media/datamodeltomakeslicingndicingpossibleinrcm.png)</span></span>

<a name="additional-resources"></a><span data-ttu-id="331a2-159">その他のリソース</span><span class="sxs-lookup"><span data-stu-id="331a2-159">Additional resources</span></span>
--------

[<span data-ttu-id="331a2-160">Power BI 統合</span><span class="sxs-lookup"><span data-stu-id="331a2-160">Power BI integration</span></span>](power-bi-integration.md)

[<span data-ttu-id="331a2-161">ワークスペースの Power BI 統合のコンフィギュレーション</span><span class="sxs-lookup"><span data-stu-id="331a2-161">Configuring Power BI integration for workspaces</span></span>](configure-power-bi-integration.md)



