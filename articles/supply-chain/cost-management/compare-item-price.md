---
title: 品目価格の保管レポートの比較
description: 比較商品価格の保存レポートを生成し、結果を参照および/またはエクスポートする方法について説明します。
author: AndersGirke
manager: tfehr
ms.date: 01/30/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: CostAdminWorkspace, CostAnalysisWorkspace, InventItemPriceCompareStorage, InventItemPriceCompareStorageDetailsChart, InventItemPriceCompareStorageDetails
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: aevengir
ms.search.validFrom: 2020-03-01
ms.dyn365.ops.version: Release 10.0.9
ms.openlocfilehash: 73e43a685f390fd718028de6add0370dfcd6cf3b
ms.sourcegitcommit: 199848e78df5cb7c439b001bdbe1ece963593cdb
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 10/13/2020
ms.locfileid: "4432163"
---
# <a name="compare-item-prices-storage-report"></a><span data-ttu-id="6f915-103">品目価格の保管レポートの比較</span><span class="sxs-lookup"><span data-stu-id="6f915-103">Compare item prices storage report</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="6f915-104">このトピックでは、Dynamics 365 Supply Chain Management の対話型ページまたはいくつかの形式のいずれかのエクスポートされたドキュメントとして、**品目価格保管の比較** レポートの実行方法とデジタルで利用可能な出力の作成方法を説明します。</span><span class="sxs-lookup"><span data-stu-id="6f915-104">This topic explains how to run a **Compare item prices storage** report and make the output available digitally, either as an interactive page in Dynamics 365 Supply Chain Management, or as an exported document in any of several formats.</span></span>

<span data-ttu-id="6f915-105">ブラウザーのレポートを表示する際、コンフィギュレーションされているレイアウトに応じて、列と集計残高が動的に調整されます。</span><span class="sxs-lookup"><span data-stu-id="6f915-105">When you view the report in your browser, columns and aggregate balances are dynamically adjusted, depending on your configured layout.</span></span> <span data-ttu-id="6f915-106">結果の並べ替え、フィルター処理、データのドリル ダウンなどを行うことができます。</span><span class="sxs-lookup"><span data-stu-id="6f915-106">You can sort the results, filter them, drill down into the data, and more.</span></span>

<span data-ttu-id="6f915-107">レポートの結果は、**品目価格の比較** データ エンティティに保存され、CSV または Microsoft Excel などの形式で結果をフィルター処理またはエクスポートできます。</span><span class="sxs-lookup"><span data-stu-id="6f915-107">Report results are stored in the **Compare item prices** data entity, which lets you filter and export the results to a format such as CSV or Microsoft Excel.</span></span>

<span data-ttu-id="6f915-108">**品目価格保存の比較** レポートでは、出力に多数の行が含まれている場合に便利です。</span><span class="sxs-lookup"><span data-stu-id="6f915-108">The **Compare item prices storage** report is helpful in cases where the output contains many lines.</span></span> <span data-ttu-id="6f915-109">たとえば、原価バージョンに保留中の品目価格を 4 万品目以上保持している場合、この出力には多くの明細行が含まれます。</span><span class="sxs-lookup"><span data-stu-id="6f915-109">For example, the output will contain many lines if you have more than 40,000 items holding a pending item price in the costing version.</span></span>

## <a name="enable-compare-item-prices-storage"></a><span data-ttu-id="6f915-110">品目価格保管の比較を有効化</span><span class="sxs-lookup"><span data-stu-id="6f915-110">Enable compare item prices storage</span></span>

<span data-ttu-id="6f915-111">この機能を使用するには、事前にシステム上で有効にする必要があります。</span><span class="sxs-lookup"><span data-stu-id="6f915-111">Before you can use this feature, you must enable it on your system.</span></span> <span data-ttu-id="6f915-112">管理者は、[機能管理](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) 設定を使用して機能状態を確認し、必要に応じてそれを有効にすることができます。</span><span class="sxs-lookup"><span data-stu-id="6f915-112">Administrators can use the [feature management](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) settings to check the feature status and enable it if needed.</span></span> <span data-ttu-id="6f915-113">この機能は次のように一覧表示されます。</span><span class="sxs-lookup"><span data-stu-id="6f915-113">Here, the feature is listed as:</span></span>

- <span data-ttu-id="6f915-114">**モジュール** - 原価管理</span><span class="sxs-lookup"><span data-stu-id="6f915-114">**Module** - Cost management</span></span>
- <span data-ttu-id="6f915-115">**機能名** - 品目価格保管の比較</span><span class="sxs-lookup"><span data-stu-id="6f915-115">**Feature name** - Compare item price storage</span></span>

## <a name="generate-a-compare-item-prices-storage-report"></a><span data-ttu-id="6f915-116">品目価格保管のレポートの比較を生成</span><span class="sxs-lookup"><span data-stu-id="6f915-116">Generate a Compare item prices storage report</span></span>

<span data-ttu-id="6f915-117">次の手順に従って、**品目価格保管の比較** レポートを生成して保存します。</span><span class="sxs-lookup"><span data-stu-id="6f915-117">Follow these steps to generate and store a **Compare item prices storage** report:</span></span>

1. <span data-ttu-id="6f915-118">**原価管理 > 照会およびレポート > あらかじめ設定された原価レポート > 品目価格保管の比較** の順に移動します。</span><span class="sxs-lookup"><span data-stu-id="6f915-118">Go to **Cost management > Inquiries and reports > Predetermined cost reports > Compare item prices storage**.</span></span>

1. <span data-ttu-id="6f915-119">**新規** を選択し、**品目価格の比較** ウィンドウを開きます。</span><span class="sxs-lookup"><span data-stu-id="6f915-119">Select **New** to open the **Compare item prices** pane.</span></span> <span data-ttu-id="6f915-120">次のオプションを設定して、レポートで比較する価格を定義します。</span><span class="sxs-lookup"><span data-stu-id="6f915-120">Set the following options to define which prices to compare in your report:</span></span>

    - <span data-ttu-id="6f915-121">**パラメータ** クイックタブで、レポートに固有の **名前** を付け、**比較する保留中の価格** と **比較に使用した価格** セクションのフィールドを使用し、比較する価格と日付を定義します。</span><span class="sxs-lookup"><span data-stu-id="6f915-121">On the **Parameters** FastTab, give the report a unique **Name** and use the fields in the **Pending prices to compare** and **Prices used for comparison** sections to define which prices and dates to compare.</span></span>
    - <span data-ttu-id="6f915-122">**対象に含めるレコード** クイックタブで、フィルターと制約を設定し、レポートに含めるデータを定義します。</span><span class="sxs-lookup"><span data-stu-id="6f915-122">On the **Records to include** FastTab, set up filters and constraints to define which data to include in the report.</span></span>
    - <span data-ttu-id="6f915-123">**バックグラウンドで実行** クイックタブで、レポートを生成する方法、タイミング、および頻度を設定します。</span><span class="sxs-lookup"><span data-stu-id="6f915-123">On the **Run in the background** FastTab, set up how, when, and the frequency at which you want to generate the report.</span></span>
    > [!NOTE]
    > <span data-ttu-id="6f915-124">このレポートは、常にバッチ ジョブの一部として実行されます。</span><span class="sxs-lookup"><span data-stu-id="6f915-124">This report is always executed as part of a batch job.</span></span>

1. <span data-ttu-id="6f915-125">**一致** を選択して設定を適用し、ウィンドウを閉じます。</span><span class="sxs-lookup"><span data-stu-id="6f915-125">Select **OK** to apply your settings and close the pane.</span></span>

1. <span data-ttu-id="6f915-126">バッチジョブが完了すると、**品目価格保管の比較** ページに一覧表示されます。</span><span class="sxs-lookup"><span data-stu-id="6f915-126">After the batch job is completed, it will be listed on the **Compare item prices storage** page.</span></span> <span data-ttu-id="6f915-127">レポートを表示するには、ページを更新する必要があります。</span><span class="sxs-lookup"><span data-stu-id="6f915-127">You may need to refresh the page to see the report.</span></span>

## <a name="explore-the-compare-item-prices-storage-report"></a><span data-ttu-id="6f915-128">品目価格の保管レポートの確認</span><span class="sxs-lookup"><span data-stu-id="6f915-128">Explore the Compare item prices storage report</span></span>

<span data-ttu-id="6f915-129">レポートを生成した後は、いつでも次の方法で表示および調査できます。</span><span class="sxs-lookup"><span data-stu-id="6f915-129">After you've generated a report, you can view and explore it at any time as follows:</span></span>

1. <span data-ttu-id="6f915-130">**原価管理 > 照会およびレポート > あらかじめ設定された原価レポート > 品目価格保管の比較** の順に移動します。</span><span class="sxs-lookup"><span data-stu-id="6f915-130">Go to **Cost management > Inquiries and reports > Predetermined cost reports > Compare item prices storage**.</span></span>

1. <span data-ttu-id="6f915-131">一覧からレポートを選択します。</span><span class="sxs-lookup"><span data-stu-id="6f915-131">Select a report from the list.</span></span>

1. <span data-ttu-id="6f915-132">次のどちらかを実行します。</span><span class="sxs-lookup"><span data-stu-id="6f915-132">Do one of the following:</span></span>

    - <span data-ttu-id="6f915-133">**概要** を選択して、レポート結果の概要を取得します。</span><span class="sxs-lookup"><span data-stu-id="6f915-133">Select **Overview** to get an overview of your report results.</span></span>
    - <span data-ttu-id="6f915-134">**詳細の表示** を選択して、レポートのより詳しい内容表示を取得</span><span class="sxs-lookup"><span data-stu-id="6f915-134">Select **View details** to get a more detailed view of your report</span></span>

1. <span data-ttu-id="6f915-135">選択された表示を開くと、次の事が実行できます。</span><span class="sxs-lookup"><span data-stu-id="6f915-135">After the selected view opens, you can do the following:</span></span>

    - <span data-ttu-id="6f915-136">Supply Chain Management のほとんどの標準フォームと同様に、ほとんどすべての列見出しを選択し、列の値でテーブルを並べ替えたりフィルター処理を行います。</span><span class="sxs-lookup"><span data-stu-id="6f915-136">Select almost any column heading to sort or filter the table by values in that column, just as with most standard forms in Supply Chain Management.</span></span> <span data-ttu-id="6f915-137">注記: 計算フィールドであるため、**差分変更価格 %** 列を並べ替えたりフィルター処理したりすることはできません。</span><span class="sxs-lookup"><span data-stu-id="6f915-137">Note, you can't sort or filter the **Net change price %** column because it's a calculated field.</span></span>
    - <span data-ttu-id="6f915-138">**分析コード表示** を選択してウィンドウが開くと、フォームに含める分析コード列を選択できます。</span><span class="sxs-lookup"><span data-stu-id="6f915-138">Select **Dimension display** to open a pane where you can choose which dimension column to include on the form.</span></span> <span data-ttu-id="6f915-139">**設定の保存** で **はい** とすると、次回レポートを開いたときに保存されるように、これらの設定が保存されます。</span><span class="sxs-lookup"><span data-stu-id="6f915-139">Set **Save setup** to **Yes** if you'd like to save these settings so they will be preserved the next time you open the report.</span></span> <span data-ttu-id="6f915-140">**一致** を選択して、設定を適用し閉じます。</span><span class="sxs-lookup"><span data-stu-id="6f915-140">Select **OK** to apply your settings and close.</span></span>
    - <span data-ttu-id="6f915-141">フォーム内の任意の行を選び、**詳細を表示** を選択すると、選択した品目に関する詳細情報が表示されます。</span><span class="sxs-lookup"><span data-stu-id="6f915-141">Select any row in the form and then select **View details** to see more information about the selected item.</span></span> <span data-ttu-id="6f915-142">ここからデータにドリル ダウンできます。</span><span class="sxs-lookup"><span data-stu-id="6f915-142">You'll be able to drill down into the data from here.</span></span>
    - <span data-ttu-id="6f915-143">フォームの任意の行を選び **比較グラフの表示** を選択して、選択した品目に関連する結果をグラフィカルに表示します。</span><span class="sxs-lookup"><span data-stu-id="6f915-143">Select any row in the form and then select **View comparison chart** to see an interactive graphical representation of your results as they relate to your selected item.</span></span> <span data-ttu-id="6f915-144">グラフとグラフの凡例からさまざまなグラフィック要素を選択することにより、これらの結果を確認することができます。</span><span class="sxs-lookup"><span data-stu-id="6f915-144">You can explore these results by selecting various graphical elements in the chart and chart legend.</span></span>
    - <span data-ttu-id="6f915-145">フォーム内の任意の行を選び、**計算詳細を表示** を選択すると、選択した品目に関する計算情報が表示されます。</span><span class="sxs-lookup"><span data-stu-id="6f915-145">Select any row in the form and then select **View calculation details** to see more information about calculations related to the selected item.</span></span> <span data-ttu-id="6f915-146">ここからデータにドリル ダウンできます。</span><span class="sxs-lookup"><span data-stu-id="6f915-146">You'll be able to drill down into the data from here.</span></span>

## <a name="export-the-compare-item-prices-storage-report"></a><span data-ttu-id="6f915-147">品目価格の保管レポートのエクスポート</span><span class="sxs-lookup"><span data-stu-id="6f915-147">Export the Compare item prices storage report</span></span>

<span data-ttu-id="6f915-148">生成した各レポートは、**品目価格の比較** データ エンティティに保存されます。</span><span class="sxs-lookup"><span data-stu-id="6f915-148">Each report that you generate is stored in the **Compare item prices** data entity.</span></span> <span data-ttu-id="6f915-149">Supply Chain Management の標準データ管理機能を使用して、データをこのエンティティから CSV または Microsoft Excel を含むサポートされているデータ形式にエクスポートします。　</span><span class="sxs-lookup"><span data-stu-id="6f915-149">You can use the standard data management features of Supply Chain Management to export data from this entity to any supported data format, including CSV or Microsoft Excel.</span></span>

<span data-ttu-id="6f915-150">次に示すのは、**品目価格保管の比較** レポートのエクスポート方法の例です。</span><span class="sxs-lookup"><span data-stu-id="6f915-150">The following is an example of how to export a **Compare item prices storage** report:</span></span>

1. <span data-ttu-id="6f915-151">**システム管理 > ワークスペース > データ管理** の順に移動します。</span><span class="sxs-lookup"><span data-stu-id="6f915-151">Go to **System administration > Workspaces > Data management**.</span></span>

1. <span data-ttu-id="6f915-152">**データ管理** セクションの **エクスポート** ボタンを選択します。</span><span class="sxs-lookup"><span data-stu-id="6f915-152">Select the **Export** button in the **Data management** section.</span></span>

1. <span data-ttu-id="6f915-153">**エクスポート** ページを開き、エクスポート ジョブの設定に使用します。</span><span class="sxs-lookup"><span data-stu-id="6f915-153">The **Export** page opens, which you'll use to set up your export job.</span></span> <span data-ttu-id="6f915-154">まず、ジョブに **グループ名** をつけます。</span><span class="sxs-lookup"><span data-stu-id="6f915-154">Start by giving your job a **Group name**.</span></span>

1. <span data-ttu-id="6f915-155">**選択したエンティティ** セクションで **エンティティの追加** をクリックして、次のオプションを設定するダイアログ ボックスを開きます。</span><span class="sxs-lookup"><span data-stu-id="6f915-155">In the **Selected entities** section, select **Add entity** to open a dialog box where you can set the following options:</span></span>

    - <span data-ttu-id="6f915-156">**エンティティ名** - **品目価格の比較** を選択します。</span><span class="sxs-lookup"><span data-stu-id="6f915-156">**Entity name** - Select **Compare item prices**.</span></span>
    - <span data-ttu-id="6f915-157">**ターゲット データ形式** - エクスポート先の形式を選択します。</span><span class="sxs-lookup"><span data-stu-id="6f915-157">**Target data format** - Choose the format that you want to export to.</span></span>

1. <span data-ttu-id="6f915-158">**追加** を選択して新しい行を追加し、**閉じる** を選択してダイアログボックスを閉じます。</span><span class="sxs-lookup"><span data-stu-id="6f915-158">Select **Add** to add the new row and then select **Close** to close the dialog box.</span></span>

1. <span data-ttu-id="6f915-159">通常は、一度にレポート 1 件をエクスポートします。</span><span class="sxs-lookup"><span data-stu-id="6f915-159">Usually you'll export one report at a time.</span></span> <span data-ttu-id="6f915-160">これを行うには、**照会** ウィンドウに追加した行の **フィルター** を設定します。</span><span class="sxs-lookup"><span data-stu-id="6f915-160">To do this, set up a **Filter** for the row you just added to the **Inquiry** pane.</span></span> <span data-ttu-id="6f915-161">これにより、エクスポートに含める **品目価格の比較** エンティティからのレポートを定義できるようになります。</span><span class="sxs-lookup"><span data-stu-id="6f915-161">This will let you define which reports from the **Compare item prices** entity that you want to include in your export.</span></span> <span data-ttu-id="6f915-162">1 件のレポートをエクスポートするには、次のフィルター オプションを設定します。</span><span class="sxs-lookup"><span data-stu-id="6f915-162">Set the following filter options to export a single report:</span></span>

    - <span data-ttu-id="6f915-163">**範囲** タブで、**追加** を選択して新しい列を追加します。</span><span class="sxs-lookup"><span data-stu-id="6f915-163">On the **Range** tab, select **Add** to add a new row.</span></span>
    - <span data-ttu-id="6f915-164">**品目価格の比較** に **テーブル** を設定します。</span><span class="sxs-lookup"><span data-stu-id="6f915-164">Set **Table** to **Compare item prices**.</span></span>
    - <span data-ttu-id="6f915-165">**品目価格の比較** に **派生テーブル** を設定します。</span><span class="sxs-lookup"><span data-stu-id="6f915-165">Set **Derived table** to **Compare item prices**.</span></span>
    - <span data-ttu-id="6f915-166">フィルター処理の対象となる **フィールド** を設定します。</span><span class="sxs-lookup"><span data-stu-id="6f915-166">Set **Field** to the field that you want to filter by.</span></span> <span data-ttu-id="6f915-167">通常は、**実行名** または **実行時間** を使用します。</span><span class="sxs-lookup"><span data-stu-id="6f915-167">Usually you'll use **Execution name** or **Execution time**.</span></span>
    - <span data-ttu-id="6f915-168">**基準** を検索したい選択フィールドから値に設定します (レポートの名前またはレポートが生成された時刻)。</span><span class="sxs-lookup"><span data-stu-id="6f915-168">Set **Criteria** to the value from your selected field that you want to look for (either the name of the report or the time the report was generated).</span></span>
    - <span data-ttu-id="6f915-169">必要に応じて、検索しているレポートを一意に識別するまで、**範囲** テーブルに行をさらに追加します。</span><span class="sxs-lookup"><span data-stu-id="6f915-169">If necessary, add more rows to the **Range** table until you have uniquely identified the report that you're looking for.</span></span>

1. <span data-ttu-id="6f915-170">**一致** を選択して、設定を保存し閉じます。</span><span class="sxs-lookup"><span data-stu-id="6f915-170">Select **OK** to save your settings and close.</span></span>

1. <span data-ttu-id="6f915-171">**保存** を選択し、エクスポート設定を保存します。</span><span class="sxs-lookup"><span data-stu-id="6f915-171">Select **Save** to save your export setup.</span></span>

1. <span data-ttu-id="6f915-172">**エクスポート オプション** タブを開き、**今すぐエクスポート** を選択して、エクスポート ファイルを生成します。</span><span class="sxs-lookup"><span data-stu-id="6f915-172">Open the **Export options** tab and select **Export now** to generate the export file.</span></span>

1. <span data-ttu-id="6f915-173">**実行の概要** ページが開き、エクスポート ジョブの状態とエクスポートされたエンティティの一覧が表示されます。</span><span class="sxs-lookup"><span data-stu-id="6f915-173">The **Execution summary** page opens, where you can see the status of your export job and a list of entities that were exported.</span></span> <span data-ttu-id="6f915-174">**エンティティ処理の状態** エリアで一覧表示されている **品目価格の比較** エンティティを選択し、**ファイルのダウンロード** を選び、エンティティからエクスポートされたデータをダウンロードします。</span><span class="sxs-lookup"><span data-stu-id="6f915-174">Select the **Compare item prices** entity listed in the **Entity processing status** area and then select **Download file** to download the data exported from that entity.</span></span>

<span data-ttu-id="6f915-175">データをエクスポートするためのデータ管理の使用方法については、[データ インポートとエクスポートのジョブ概要](../../fin-ops-core/dev-itpro/data-entities/data-import-export-job.md) を参照してください。</span><span class="sxs-lookup"><span data-stu-id="6f915-175">For more information about how to use data management to export data, see [Data import and export jobs overview](../../fin-ops-core/dev-itpro/data-entities/data-import-export-job.md).</span></span>
