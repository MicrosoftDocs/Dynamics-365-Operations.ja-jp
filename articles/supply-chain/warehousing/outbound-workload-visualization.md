---
title: 出庫ワークロードの視覚化
description: このトピックは、ワークロードの視覚化に関する情報を提供します。 この機能により、倉庫管理者と監修者は、現在の作業の進捗状況と残っている金額を監視するために使用できるカスタム ワークロード グラフを作成できるようになります。 倉庫管理者は、複数のビューを作成し、必要に応じて自動更新を設定できます。
author: Mirzaab
manager: tfehr
ms.date: 08/28/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: mirzaab
ms.search.validFrom: 2020-08-28
ms.dyn365.ops.version: Release 10.0.13
ms.openlocfilehash: 6b7512ea6ad2e97db388bac6750482f7ed967140
ms.sourcegitcommit: eaf330dbee1db96c20d5ac479f007747bea079eb
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 02/15/2021
ms.locfileid: "5225933"
---
# <a name="outbound-workload-visualization"></a><span data-ttu-id="d1a65-105">出庫ワークロードの視覚化</span><span class="sxs-lookup"><span data-stu-id="d1a65-105">Outbound workload visualization</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="d1a65-106">**出庫ワークロードの視覚化** ページからアクセスできる高度な設定機能により、倉庫管理者と監修者は、現在の作業の進捗状況と残っている金額を監視するためのカスタム ワークロード グラフを作成できます。</span><span class="sxs-lookup"><span data-stu-id="d1a65-106">Advanced setup capabilities that are accessible from the **Outbound workload visualization** page let warehouse managers and supervisors create custom workload charts that can be used to monitor the progress of current work and the amount of it that remains.</span></span> <span data-ttu-id="d1a65-107">倉庫管理者は、複数のビューを作成し、必要に応じて自動更新を設定できます。</span><span class="sxs-lookup"><span data-stu-id="d1a65-107">Warehouse managers can create multiple views and set up automatic refresh as they require.</span></span> <span data-ttu-id="d1a65-108">出庫ワークロードの視覚化は、倉庫のパフォーマンス ページでの表示に適しています。</span><span class="sxs-lookup"><span data-stu-id="d1a65-108">Outbound workload visualizations are suitable for display on warehouse performance pages.</span></span>

<span data-ttu-id="d1a65-109">この機能は、集荷作業の進行状況を追跡するために使用できます。</span><span class="sxs-lookup"><span data-stu-id="d1a65-109">This functionality can be used to track the progress of picking work.</span></span> <span data-ttu-id="d1a65-110">この機能は労働管理に統合されており、労務管理が設定されている場合は、表示されている集荷作業の残りの時間数を計算して表示することができます (フィルター処理)。</span><span class="sxs-lookup"><span data-stu-id="d1a65-110">The feature is integrated with labor management, and if labor management is set up, outbound workload visualizations can show a calculation of the number of hours that remain for the picking work that is shown (filtered).</span></span>

## <a name="turn-on-the-outbound-workload-visualization-feature"></a><span data-ttu-id="d1a65-111">ワークロードの視覚化機能を有効にする</span><span class="sxs-lookup"><span data-stu-id="d1a65-111">Turn on the Outbound workload visualization feature</span></span>

<span data-ttu-id="d1a65-112">この機能を使用するには、システム上で有効にする必要があります。</span><span class="sxs-lookup"><span data-stu-id="d1a65-112">Before you can use this feature, it must be turned on in your system.</span></span> <span data-ttu-id="d1a65-113">管理者は、[機能管理](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) 設定を使用して、機能の状態を確認し、有効にすることができます。</span><span class="sxs-lookup"><span data-stu-id="d1a65-113">Admins can use the [Feature management](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) settings to check the status of the feature and turn it on.</span></span> <span data-ttu-id="d1a65-114">**機能管理** ワークスペースで、この機能は次のようにリストされています。</span><span class="sxs-lookup"><span data-stu-id="d1a65-114">In the **Feature management** workspace, the feature is listed in the following way:</span></span>

- <span data-ttu-id="d1a65-115">**モジュール:** *倉庫管理*</span><span class="sxs-lookup"><span data-stu-id="d1a65-115">**Module:** *Warehouse management*</span></span>
- <span data-ttu-id="d1a65-116">**機能名:** *ワークロードの視覚化機能を有効にする*</span><span class="sxs-lookup"><span data-stu-id="d1a65-116">**Feature name:** *Outbound workload visualization*</span></span>

## <a name="set-up-outbound-workload-visualizations"></a><span data-ttu-id="d1a65-117">出庫ワークロードの視覚化の設定</span><span class="sxs-lookup"><span data-stu-id="d1a65-117">Set up outbound workload visualizations</span></span>

<span data-ttu-id="d1a65-118">視覚化を設定するには、フィルター (ビュー) のコレクションを作成し、異なるタイプの分析を表示するように各フィルターを設計します。</span><span class="sxs-lookup"><span data-stu-id="d1a65-118">To set up your visualizations, you create a collection of filters (views) and design each filter so that it shows a different type of analysis.</span></span> <span data-ttu-id="d1a65-119">フィルターを設計するには、**フィルターの構成** ページを使用します。</span><span class="sxs-lookup"><span data-stu-id="d1a65-119">You use the **Configure filters** page to design the filters.</span></span>

<span data-ttu-id="d1a65-120">出庫ワークロードの視覚化を設定するには、次の手順を実行します。</span><span class="sxs-lookup"><span data-stu-id="d1a65-120">To set up an outbound workload visualization, follow these steps.</span></span>

1. <span data-ttu-id="d1a65-121">**倉庫管理 \> 倉庫の監視レポート \> 出庫ワークロードの視覚化** の順に移動します。</span><span class="sxs-lookup"><span data-stu-id="d1a65-121">Go to **Warehouse management \> Warehouse monitoring reports \> Outbound workload visualization**.</span></span>

    <span data-ttu-id="d1a65-122">**出庫ワークロードの視覚化** ページが表示されます。</span><span class="sxs-lookup"><span data-stu-id="d1a65-122">The **Outbound workload visualization** page appears.</span></span> <span data-ttu-id="d1a65-123">フィルターを作成すると、このページに視覚化が表示されます。</span><span class="sxs-lookup"><span data-stu-id="d1a65-123">After you create some filters, this page will show your visualization.</span></span> <span data-ttu-id="d1a65-124">必要な数のフィルターを作成することができます。</span><span class="sxs-lookup"><span data-stu-id="d1a65-124">You can create as many filters as you want.</span></span> <span data-ttu-id="d1a65-125">作成したすべてのフィルターは、ユーザー アカウントに保存されるため、後で使用することができます。</span><span class="sxs-lookup"><span data-stu-id="d1a65-125">All the filters that you create are saved under your user account, so that you can use them later.</span></span> <span data-ttu-id="d1a65-126">つまり、各ユーザーは作成された独自のフィルターのセットを持つことになります。</span><span class="sxs-lookup"><span data-stu-id="d1a65-126">In other words, each user will have their own set of filters that they created.</span></span> <span data-ttu-id="d1a65-127">これらのフィルターは、他のユーザーと共有されることはありません。</span><span class="sxs-lookup"><span data-stu-id="d1a65-127">Those filters won't be shared with other users.</span></span>

1. <span data-ttu-id="d1a65-128">**出庫ワークロードの視覚化** ページのアクション ウィンドウの **フィルター** タブで、**フィルターの構成** を選択します。</span><span class="sxs-lookup"><span data-stu-id="d1a65-128">On the **Outbound workload visualization** page, on the Action Pane, on the **Filters** tab, select **Configure filters**.</span></span>
1. <span data-ttu-id="d1a65-129">**フィルターの構成** ページのアクション ウィンドウで、**新規** を選択してフィルターを追加し、次のフィールドを設定します。</span><span class="sxs-lookup"><span data-stu-id="d1a65-129">On the **Configure filters** page, on the Action Pane, select **New** to add a filter, and then set the following fields for it:</span></span>

    - <span data-ttu-id="d1a65-130">**X 軸のグループ テーブル** – X 軸の値をグループ化するために使用するフィールドを含むテーブルを選択します。</span><span class="sxs-lookup"><span data-stu-id="d1a65-130">**X-axis group table** – Select the table that contains the field that should be used to group the X-axis values.</span></span>
    - <span data-ttu-id="d1a65-131">**X 軸のグループ フィールド** – **X 軸グループ テーブル** フィールドで選択したテーブルのフィールドの中から、X 軸の値をグループ化するために使用するフィールドを選択します。</span><span class="sxs-lookup"><span data-stu-id="d1a65-131">**X-axis group field** – From among the fields of the table that you selected in the **X-axis group table** field, select the field that should be used to group the X-axis values.</span></span>
    - <span data-ttu-id="d1a65-132">**X 軸値のテーブル** – グループをさらに分析するために使用する必要があるフィールドを含むテーブルを選択します。</span><span class="sxs-lookup"><span data-stu-id="d1a65-132">**X-axis value table** – Select the table that contains the field that should be used to further analyze the groups.</span></span>
    - <span data-ttu-id="d1a65-133">**X 軸値のフィールド** – **X 軸グループ テーブル** フィールドで選択したテーブルのフィールドの中から、グループごとに分析する必要のある値を提供するフィールドを選択します。</span><span class="sxs-lookup"><span data-stu-id="d1a65-133">**X-axis value field** – From among the fields of the table that you selected in the **X-axis value table** field, select the field that provides the values that should be analyzed for each group.</span></span>
    - <span data-ttu-id="d1a65-134">**自動更新** – 視覚化を自動的に更新するかどうかを選択します。</span><span class="sxs-lookup"><span data-stu-id="d1a65-134">**Auto-refresh** – Select whether the visualization should automatically be refreshed.</span></span>
    - <span data-ttu-id="d1a65-135">**更新間隔 (分)** – 自動更新の間隔を分単位で入力します。</span><span class="sxs-lookup"><span data-stu-id="d1a65-135">**Refresh interval (minutes)** – Enter the number of minutes between automatic refreshes.</span></span>
    - <span data-ttu-id="d1a65-136">**表示レベル** – グラフでオープン行とオープン ヘッダー カウントのどちらを表示するかを選択します。</span><span class="sxs-lookup"><span data-stu-id="d1a65-136">**Display level** – Select whether the chart should show open lines or open header counts.</span></span>
    - <span data-ttu-id="d1a65-137">**ピッキング タイプ** – **表示レベル** フィールドを _明細行を開く_ に設定した場合は、グラフの内の開いている作業明細行の数に、初期ピック、段階的ピック、または初期ピックと段階的ピックの両方を含めるかどうかを選択します。</span><span class="sxs-lookup"><span data-stu-id="d1a65-137">**Picking type** – If you set the **Display level** field to _Open lines_, select whether the count of open work lines in the chart should include initial picks, staged picks, or both initial picks and staged picks.</span></span>
    - <span data-ttu-id="d1a65-138">**サイト** – グラフを読み込むサイトを選択します。</span><span class="sxs-lookup"><span data-stu-id="d1a65-138">**Site** – Select the site to load the chart for.</span></span>
    - <span data-ttu-id="d1a65-139">**サイト** – グラフを読み込む倉庫を選択します。</span><span class="sxs-lookup"><span data-stu-id="d1a65-139">**Warehouse** – Select the warehouse to load the chart for.</span></span>
    - <span data-ttu-id="d1a65-140">**含める日数** – グラフを生成する過去の日数を入力します。</span><span class="sxs-lookup"><span data-stu-id="d1a65-140">**Days to include** – Enter the number of days in the past that the chart should be generated for.</span></span>
    - <span data-ttu-id="d1a65-141">**作業指示書タイプ** – フィルター処理する出庫作業指示書タイプを選択します。</span><span class="sxs-lookup"><span data-stu-id="d1a65-141">**Work order type** – Select the outbound work order types to filter on.</span></span>

    <span data-ttu-id="d1a65-142">![フィルターの構成ページ](media/work-viz-filters-1.png "フィルターの構成ページ")</span><span class="sxs-lookup"><span data-stu-id="d1a65-142">![Configure filters page](media/work-viz-filters-1.png "Configure filters page")</span></span>

1. <span data-ttu-id="d1a65-143">**フィルターの構成** ページを閉じて、**出庫ワークロードの視覚化** ページに戻ります。</span><span class="sxs-lookup"><span data-stu-id="d1a65-143">Close the **Configure filters** page to return to the **Outbound workload visualizations** page.</span></span>

    <span data-ttu-id="d1a65-144">新しいフィルター設定に基づいて、**出庫ワークロードの視覚化** ページにデータが表示されるようになりました。</span><span class="sxs-lookup"><span data-stu-id="d1a65-144">The **Outbound workload visualizations** page now shows data, based on your new filter settings.</span></span> <span data-ttu-id="d1a65-145">これで、新しいフィルターが使用可能になり、**フィルター** フィールドで選択されます。</span><span class="sxs-lookup"><span data-stu-id="d1a65-145">Your new filter is now available and is selected in the **Filter** field.</span></span> <span data-ttu-id="d1a65-146">グラフの最上部には、次のフィールドがあります:</span><span class="sxs-lookup"><span data-stu-id="d1a65-146">The following fields are available at the top of the chart:</span></span>

    - <span data-ttu-id="d1a65-147">**フィルター**: このフィールドには、これまでに作成したすべてのフィルターが含まれます。</span><span class="sxs-lookup"><span data-stu-id="d1a65-147">**Filter** – This field includes all the filters that you've created so far.</span></span> <span data-ttu-id="d1a65-148">データをグラフに表示するには、フィルターを選択します。</span><span class="sxs-lookup"><span data-stu-id="d1a65-148">Select a filter to view its data in the chart.</span></span>
    - <span data-ttu-id="d1a65-149">**最終更新日時** – このフィールドは、グラフの情報が最後に更新された日時を表示します。</span><span class="sxs-lookup"><span data-stu-id="d1a65-149">**Last refreshed** – This field shows the date and time when the information in the chart was last updated.</span></span>
    - <span data-ttu-id="d1a65-150">**見積済/実際の時間** – 労働基準がシステムで設定されている場合、このオプションを *はい* に設定すると、計算された集荷時間の累計がグラフの各列の上部に表示されます。</span><span class="sxs-lookup"><span data-stu-id="d1a65-150">**Estimated/actual time** – If labor standards are set up in your system, set this option to *Yes* to show accumulated estimated picking times at the top of each column in the chart.</span></span> <span data-ttu-id="d1a65-151">労働基準を使用していない場合、このオプションは使用できません。</span><span class="sxs-lookup"><span data-stu-id="d1a65-151">If you aren't using labor standards, this option is unavailable.</span></span>

    <span data-ttu-id="d1a65-152">![視覚化の例](media/work-viz-chart.png "視覚化の例")</span><span class="sxs-lookup"><span data-stu-id="d1a65-152">![Example visualization](media/work-viz-chart.png "Example visualization")</span></span>

1. <span data-ttu-id="d1a65-153">グラフ内の任意のバーを選択して、関連する作業明細行の詳細を表示します。</span><span class="sxs-lookup"><span data-stu-id="d1a65-153">Select any bar in the chart to view the associated work line details.</span></span>

    <span data-ttu-id="d1a65-154">![作業ラインの詳細](media/work-viz-work-details.png "作業ラインの詳細")</span><span class="sxs-lookup"><span data-stu-id="d1a65-154">![Work line details](media/work-viz-work-details.png "Work line details")</span></span>

## <a name="example-outbound-workload-visualization-for-zones"></a><span data-ttu-id="d1a65-155">例: ゾーンの出庫ワークロードの視覚化</span><span class="sxs-lookup"><span data-stu-id="d1a65-155">Example: Outbound workload visualization for zones</span></span>

<span data-ttu-id="d1a65-156">この例では、各ゾーンの作業明細行を表示する視覚化と、各作業項目のステータス (_未処理_、_終了_、または _キャンセル_) を設定します。</span><span class="sxs-lookup"><span data-stu-id="d1a65-156">For this example, you want to set up a visualization that shows work lines for each zone, and the status of each work line (_Open_, _Closed_, or _Canceled_).</span></span> <span data-ttu-id="d1a65-157">この場合は、次の設定を含むフィルターを設定できます。</span><span class="sxs-lookup"><span data-stu-id="d1a65-157">In this case, you can set up a filter that has the following settings:</span></span>

- <span data-ttu-id="d1a65-158">**フィルター名** – このフィルターの名前 (_ゾーンと作業ステータス_ など) を入力します。</span><span class="sxs-lookup"><span data-stu-id="d1a65-158">**Filter name** – Enter a name for this filter (such as _Zone vs. work status_).</span></span>
- <span data-ttu-id="d1a65-159">**説明** – このフィルターの簡単な説明 (_ゾーンと作業ステータス_ など) を入力します。</span><span class="sxs-lookup"><span data-stu-id="d1a65-159">**Description** – Enter a short description for this filter (such as _Zone vs. work status_).</span></span>
- <span data-ttu-id="d1a65-160">**X 軸のグループ テーブル** – _場所_ を選択します。</span><span class="sxs-lookup"><span data-stu-id="d1a65-160">**X-axis group table** – Select _Locations._</span></span>
- <span data-ttu-id="d1a65-161">**X 軸グループ** – _ゾーン ID_ を選択します。</span><span class="sxs-lookup"><span data-stu-id="d1a65-161">**X-axis group** – Select _Zone ID_.</span></span>
- <span data-ttu-id="d1a65-162">**X 軸の値テーブル** – ゾーンごとの作業を表示するので、_作業_ を選択します。</span><span class="sxs-lookup"><span data-stu-id="d1a65-162">**X-axis value table** – Select _Work_, because you want to view work per zone.</span></span>
- <span data-ttu-id="d1a65-163">**X 軸の値フィールド** – 作業の状態を表示するので、_作業状態_ を選択します。</span><span class="sxs-lookup"><span data-stu-id="d1a65-163">**X-axis value field** – Select _Work status_, because you want to view work status.</span></span>
- <span data-ttu-id="d1a65-164">**自動更新** – 視覚化を自動的に更新するかどうかを選択します。</span><span class="sxs-lookup"><span data-stu-id="d1a65-164">**Auto refresh** – Select whether the visualization should automatically be refreshed.</span></span>
- <span data-ttu-id="d1a65-165">**ピッキング タイプ** – ステージング場所からの最初のピックとピックの両方を含めるために、_初期ピックとステージピック_ を選択します。</span><span class="sxs-lookup"><span data-stu-id="d1a65-165">**Picking type** – Select _Initial picks and staged picks_, because you want to include both initial picks and picks from staging locations.</span></span> <span data-ttu-id="d1a65-166">つまり、基本的には、作成したすべてのピック作業行を含める必要があります。</span><span class="sxs-lookup"><span data-stu-id="d1a65-166">In other words, you essentially want to include all the pick work lines that you have.</span></span>
- <span data-ttu-id="d1a65-167">**表示レベル** – 作業ヘッダーごとではなく明細行ごとの情報を表示するために、_未処理の明細行_ を選択します。</span><span class="sxs-lookup"><span data-stu-id="d1a65-167">**Display level** – Select _Open lines_, because you want to view the information per line, not per work header.</span></span>

<span data-ttu-id="d1a65-168">以下の図は、結果としてのグラフの一例を表しています。</span><span class="sxs-lookup"><span data-stu-id="d1a65-168">The following illustration shows an example of the resulting chart.</span></span>

<span data-ttu-id="d1a65-169">![ゾーンと作業状態の視覚化](media/work-viz-chart.png "ゾーンと作業状態の視覚化")</span><span class="sxs-lookup"><span data-stu-id="d1a65-169">![Zone vs. work status visualization](media/work-viz-chart.png "Zone vs. work status visualization")</span></span>

<span data-ttu-id="d1a65-170">このグラフには、**FLOOR** および **BULK** という名前の 2 つのゾーンと **空白** のゾーンが示されています。</span><span class="sxs-lookup"><span data-stu-id="d1a65-170">This chart shows two zones that are named **FLOOR** and **BULK**, plus a zone that is named **Blank**.</span></span> <span data-ttu-id="d1a65-171">**空白** のゾーンは、ゾーンのメンバーではないすべての作業明細行を表します。</span><span class="sxs-lookup"><span data-stu-id="d1a65-171">The **Blank** zone represents all work lines that aren't members of any zones.</span></span> <span data-ttu-id="d1a65-172">グラフには、関係のないすべてのフィルター処理されたデータが常に **空白** として表示され、できるだけ視覚化できるようになっています。</span><span class="sxs-lookup"><span data-stu-id="d1a65-172">The chart always shows all unrelated filtered data as **Blank**, to provide as much visibility as possible.</span></span> <span data-ttu-id="d1a65-173">**FLOOR** ゾーンでは、グラフに 3 つの終了した明細行と 4 つの未処理の明細行が表示されています。</span><span class="sxs-lookup"><span data-stu-id="d1a65-173">In the **FLOOR** zone, the chart shows three closed lines and four open lines.</span></span> <span data-ttu-id="d1a65-174">**BULK** ゾーンでは、グラフに 4 つの終了した明細行と 1 つの未処理の明細行、24 のキャンセルされた明細行が表示されています。</span><span class="sxs-lookup"><span data-stu-id="d1a65-174">In the **BULK** zone, the chart shows four closed lines, one open line, and 24 canceled lines.</span></span> <span data-ttu-id="d1a65-175">最後に、ゾーンに含まれていない 8 つの終了した明細行がグラフに表示されるため、**空白** として一覧されます。</span><span class="sxs-lookup"><span data-stu-id="d1a65-175">Finally, the chart shows eight closed lines that aren't part of any zone and are therefore listed as **Blank**.</span></span>


[!INCLUDE[footer-include](../../includes/footer-banner.md)]