---
title: 在庫評価額ストレージ レポート
description: このトピックでは、在庫評価額ストレージ レポートを実行し、Microsoft Dynamics 365 Supply Chain Management で対話型ページとして、または複数の形式でエクスポートされたドキュメントとして、出力をデジタルで使用可能にする方法について説明します。
author: AndersGirke
manager: tfehr
ms.date: 04/17/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: InventValueProcess, InventValueReportSetup
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: aevengir
ms.search.validFrom: 2020-04-17
ms.dyn365.ops.version: Release 10.0.9
ms.openlocfilehash: f50318e0a955d8244ba854aa1fd73ad7532b9198
ms.sourcegitcommit: 199848e78df5cb7c439b001bdbe1ece963593cdb
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 10/13/2020
ms.locfileid: "4431937"
---
# <a name="inventory-value-storage-report"></a><span data-ttu-id="d3d05-103">在庫評価額ストレージ レポート</span><span class="sxs-lookup"><span data-stu-id="d3d05-103">Inventory value storage report</span></span>

<span data-ttu-id="d3d05-104">このトピックでは、**在庫評価額ストレージ** レポートを実行し、 Microsoft Dynamics 365 Supply Chain Management で対話型ページとして、または複数の形式でエクスポートされたドキュメントとして、出力をデジタルで使用可能にする方法について説明します。</span><span class="sxs-lookup"><span data-stu-id="d3d05-104">This topic explains how to run an **Inventory value storage** report and make the output available digitally, either as an interactive page in Microsoft Dynamics 365 Supply Chain Management or as an exported document in any of several formats.</span></span>

<span data-ttu-id="d3d05-105">ブラウザでレポートを表示すると、列と集計残高は、構成したレイアウトに応じて動的に調整されます。</span><span class="sxs-lookup"><span data-stu-id="d3d05-105">When you view the report in your browser, columns and aggregate balances are dynamically adjusted, depending on the layout that you've configured.</span></span> <span data-ttu-id="d3d05-106">結果の並べ替え、フィルター処理、データのドリル ダウンなどを行うことができます。</span><span class="sxs-lookup"><span data-stu-id="d3d05-106">You can sort the results, filter them, drill down into the data, and more.</span></span>

<span data-ttu-id="d3d05-107">レポートの結果は、**在庫評価額** データ エンティティに格納されます。</span><span class="sxs-lookup"><span data-stu-id="d3d05-107">Report results are stored in the **Inventory value** data entity.</span></span> <span data-ttu-id="d3d05-108">したがって、結果をフィルタ処理し、その結果をコンマ区切り値 (CSV) または Microsoft Excel 形式などにエクスポートできます。</span><span class="sxs-lookup"><span data-stu-id="d3d05-108">Therefore, you can filter and export the results to a format such as comma-separated values (CSV) or Microsoft Excel format.</span></span>

<span data-ttu-id="d3d05-109">**在庫評価額ストレージ** レポートは、出力に多数の行が含まれている場合に役立ちます。</span><span class="sxs-lookup"><span data-stu-id="d3d05-109">The **Inventory value storage** report is helpful when the output contains many lines.</span></span> <span data-ttu-id="d3d05-110">たとえば、5 万の品目があり、倉庫として 300 店舗を作ったとします。</span><span class="sxs-lookup"><span data-stu-id="d3d05-110">For example, you have 50,000 items, and 300 stores have been created as warehouses.</span></span> <span data-ttu-id="d3d05-111">この場合、品目別、拠点別、倉庫別に在庫期末残高を要求すると、出力に多数の明細が含まれます。</span><span class="sxs-lookup"><span data-stu-id="d3d05-111">In this case, if you request inventory ending balances by item, site, and warehouse, the output will contain many lines.</span></span>

> [!NOTE]
> <span data-ttu-id="d3d05-112">レポートには、レポート レイアウトで定義されている小計は含まれません。</span><span class="sxs-lookup"><span data-stu-id="d3d05-112">The report won't include subtotals that are defined in the report layout.</span></span> <span data-ttu-id="d3d05-113">一般会計残高は、レポートレイアウトで定義されている場合でも、含まれません。</span><span class="sxs-lookup"><span data-stu-id="d3d05-113">It also won't include general ledger balances, even when they are defined in the report layout.</span></span> <span data-ttu-id="d3d05-114">一般会計への調整は、試算表を使用して行う必要があります。</span><span class="sxs-lookup"><span data-stu-id="d3d05-114">Reconciliation to the general ledger must be done by using trial balances.</span></span>

## <a name="turn-on-the-inventory-value-storage-feature"></a><span data-ttu-id="d3d05-115">在庫評価額ストレージ機能を有効にします</span><span class="sxs-lookup"><span data-stu-id="d3d05-115">Turn on the Inventory value storage feature</span></span>

<span data-ttu-id="d3d05-116">**在庫評価額** レポートを生成する前に、システムでこの機能を有効にしておく必要があります。</span><span class="sxs-lookup"><span data-stu-id="d3d05-116">Before you can generate an **Inventory value storage** report, you must turn on the feature in your system.</span></span> <span data-ttu-id="d3d05-117">管理者は、[機能の管理](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) 設定を使用して、機能の状態を確認し、必要に応じて有効にすることができます。</span><span class="sxs-lookup"><span data-stu-id="d3d05-117">Administrators can use the [feature management](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) settings to check the status of the feature and turn it on if it's required.</span></span> <span data-ttu-id="d3d05-118">**機能管理** ワークスペースで、この機能は次のようにリストされています。</span><span class="sxs-lookup"><span data-stu-id="d3d05-118">In the **Feature management** workspace, the feature is listed in the following way:</span></span>

- <span data-ttu-id="d3d05-119">**モジュール** - 原価管理</span><span class="sxs-lookup"><span data-stu-id="d3d05-119">**Module** – Cost management</span></span>
- <span data-ttu-id="d3d05-120">**機能名** 在庫評価額ストレージ</span><span class="sxs-lookup"><span data-stu-id="d3d05-120">**Feature name** – Inventory value storage</span></span>

## <a name="generate-an-inventory-value-storage-report"></a><span data-ttu-id="d3d05-121">在庫評価額ストレージ レポートを生成します</span><span class="sxs-lookup"><span data-stu-id="d3d05-121">Generate an Inventory value storage report</span></span>

<span data-ttu-id="d3d05-122">次の手順に従って、**在庫評価額ストレージ** レポートを生成して保存します。</span><span class="sxs-lookup"><span data-stu-id="d3d05-122">Follow these steps to generate and store an **Inventory value storage** report.</span></span>

1. <span data-ttu-id="d3d05-123">**原価管理 \> 照会とレポート \> 在庫評価額レポートストレージ** の順に移動します。</span><span class="sxs-lookup"><span data-stu-id="d3d05-123">Go to **Cost management \> Inquiries and reports \> Inventory value report storage**.</span></span>
1. <span data-ttu-id="d3d05-124">**新規** を選択します。</span><span class="sxs-lookup"><span data-stu-id="d3d05-124">Select **New**.</span></span>
1. <span data-ttu-id="d3d05-125">**在庫評価額** ダイアログ ボックスで、次の値を設定してレポートに含めるレコードを定義します：</span><span class="sxs-lookup"><span data-stu-id="d3d05-125">In the **Inventory value** dialog box that appears, set the following values to define which records are included in your report:</span></span>

    - <span data-ttu-id="d3d05-126">**パラメータ** クイックタブで、レポートの一意の名前を入力し、**日付間隔** セクションのフィールドを使用して、レポートに含めるレコードを定義します。</span><span class="sxs-lookup"><span data-stu-id="d3d05-126">On the **Parameters** FastTab, enter a unique name for the report, and use the fields in the **Date interval** section to define which records are included in the report.</span></span> <span data-ttu-id="d3d05-127">日付の間隔を定義するには、**日付間隔コード** フィールドで事前に設定された (レポートの生成日を基準とした) 範囲を選択するか、 **開始日** フィールドと **終了日** フィールドで特定の日付を選択します。</span><span class="sxs-lookup"><span data-stu-id="d3d05-127">To define the date interval, you can either select a preset range (relative to the report generation date) in the **Date interval code** field, or select specific dates in the **From date** and **To date** fields.</span></span>
    - <span data-ttu-id="d3d05-128">**対象に含めるレコード** クイックタブで、フィルタと制約を設定して、レポートに含めるデータを定義します。</span><span class="sxs-lookup"><span data-stu-id="d3d05-128">On the **Records to include** FastTab, set up filters and constraints to define which data is included in the report.</span></span>
    - <span data-ttu-id="d3d05-129">**バックグラウンドで実行** クイックタブで、レポートの生成方法、タイミング、および頻度を指定します。</span><span class="sxs-lookup"><span data-stu-id="d3d05-129">On the **Run in the background** FastTab, specify how, when, and how often the report is generated.</span></span>

    > [!NOTE]
    > <span data-ttu-id="d3d05-130">このレポートは、常にバッチ ジョブの一部として実行されます。</span><span class="sxs-lookup"><span data-stu-id="d3d05-130">This report is always run as part of a batch job.</span></span>

1. <span data-ttu-id="d3d05-131">**OK** を選択して設定を適用し、ダイアログ ボックスを閉じます。</span><span class="sxs-lookup"><span data-stu-id="d3d05-131">Select **OK** to apply your settings and close the dialog box.</span></span>

<span data-ttu-id="d3d05-132">バッチ ジョブが完了すると、レポートは **在庫評価額 レポート ストレージ** ページに表示されます。</span><span class="sxs-lookup"><span data-stu-id="d3d05-132">After the batch job is completed, the report will be listed on the **Inventory value report storage** page.</span></span> <span data-ttu-id="d3d05-133">レポートを表示するにあたって、ページの更新が必要となる場合があります。</span><span class="sxs-lookup"><span data-stu-id="d3d05-133">You might have to refresh the page to see the report.</span></span>

## <a name="explore-an-inventory-value-storage-report"></a><span data-ttu-id="d3d05-134">在庫評価額ストレージ レポートを確認します</span><span class="sxs-lookup"><span data-stu-id="d3d05-134">Explore an Inventory value storage report</span></span>

<span data-ttu-id="d3d05-135">レポートを生成した後は、いつでも次の手順で表示および調査できます。</span><span class="sxs-lookup"><span data-stu-id="d3d05-135">After you've generated a report, you can view and explore it at any time by following these steps.</span></span>

1. <span data-ttu-id="d3d05-136">**原価管理 \> 照会とレポート \> 在庫評価額レポートストレージ** の順に移動します。</span><span class="sxs-lookup"><span data-stu-id="d3d05-136">Go to **Cost management \> Inquiries and reports \> Inventory value report storage**.</span></span>
1. <span data-ttu-id="d3d05-137">一覧で、レポートを選択します。</span><span class="sxs-lookup"><span data-stu-id="d3d05-137">Select a report in the list.</span></span>
1. <span data-ttu-id="d3d05-138">レポートの内容を表示するには、**詳細の表示** を選択します。</span><span class="sxs-lookup"><span data-stu-id="d3d05-138">Select **View details** to show the report content.</span></span>
1. <span data-ttu-id="d3d05-139">次の手順のいずれかを実行してレポートを探索します。</span><span class="sxs-lookup"><span data-stu-id="d3d05-139">Explore the report by following any of these steps:</span></span>

    - <span data-ttu-id="d3d05-140">Supply Chain Management のほとんどの標準フォームと同様に、ほとんどの列の見出しを選択して、その列の値でグリッドをソートしたり、フィルタリングしたりすることができます。</span><span class="sxs-lookup"><span data-stu-id="d3d05-140">As for most standard pages in Supply Chain Management, you can select almost any column heading to sort or filter the grid by the values in that column.</span></span>
    - <span data-ttu-id="d3d05-141">**フィルタ** フィールドを使用して、使用可能な複数の列のいずれかの値でレポートをフィルタ処理します。</span><span class="sxs-lookup"><span data-stu-id="d3d05-141">Use the **Filter** field to filter the report by any value in any of several available columns.</span></span>
    - <span data-ttu-id="d3d05-142">並べ替えとフィルタのオプションの好みの組み合わせを保存して読み込むには、**フィルタ** フィールドの上部にある [表示] メニューを使用します。</span><span class="sxs-lookup"><span data-stu-id="d3d05-142">Use the view menu (above the **Filter** field) to save and load your favorite combinations of sort and filter options.</span></span>

## <a name="export-an-inventory-value-storage-report"></a><span data-ttu-id="d3d05-143">在庫評価額ストレージ レポートをエクスポートします</span><span class="sxs-lookup"><span data-stu-id="d3d05-143">Export an Inventory value storage report</span></span>

<span data-ttu-id="d3d05-144">生成した各レポートは、**在庫評価額** データ エンティティに保存されます。</span><span class="sxs-lookup"><span data-stu-id="d3d05-144">Every report that you generate is stored in the **Inventory value** data entity.</span></span> <span data-ttu-id="d3d05-145">Supply Chain Management の標準データ管理機能を使用して、データをこのエンティティから CSV または Excel を含むサポートされているデータ形式にエクスポートします。</span><span class="sxs-lookup"><span data-stu-id="d3d05-145">You can use the standard data management features of Supply Chain Management to export data from this entity to any supported data format, such as CSV or Excel format.</span></span>

<span data-ttu-id="d3d05-146">次の例では、**在庫評価額レポート** をエクスポートする方法を示します。</span><span class="sxs-lookup"><span data-stu-id="d3d05-146">The following example shows how to export an **Inventory value report** report.</span></span>

1. <span data-ttu-id="d3d05-147">**システム管理 \> ワークスペース \> データ管理** の順に移動します。</span><span class="sxs-lookup"><span data-stu-id="d3d05-147">Go to **System administration \> Workspaces \> Data management**.</span></span>
1. <span data-ttu-id="d3d05-148">**インポート/エクスポート** セクションで、**エクスポート** タイルを選択します。</span><span class="sxs-lookup"><span data-stu-id="d3d05-148">In the **Import / Export** section, select the **Export** tile.</span></span> 
1. <span data-ttu-id="d3d05-149">表示された **エクスポート** ページで、エクスポート ジョブを設定します。</span><span class="sxs-lookup"><span data-stu-id="d3d05-149">On the **Export** page that appears, you will set up the export job.</span></span> <span data-ttu-id="d3d05-150">まず、ジョブのグループ名を入力します。</span><span class="sxs-lookup"><span data-stu-id="d3d05-150">First enter a group name for the job.</span></span>
1. <span data-ttu-id="d3d05-151">**選択したエンティティ** セクションで、 **エンティティの追加** を選択します。</span><span class="sxs-lookup"><span data-stu-id="d3d05-151">In the **Selected entities** section, select **Add entity**.</span></span>
1. <span data-ttu-id="d3d05-152">表示されたダイアログ ボックスで、次のフィールドを設定します。</span><span class="sxs-lookup"><span data-stu-id="d3d05-152">In the dialog box that appears, set the following fields:</span></span>

    - <span data-ttu-id="d3d05-153">**エンティティ名** –  **在庫評価額** を選択します。</span><span class="sxs-lookup"><span data-stu-id="d3d05-153">**Entity name** – Select **Inventory value**.</span></span>
    - <span data-ttu-id="d3d05-154">**ターゲット データ形式** – データのエクスポート先の形式を選択します。</span><span class="sxs-lookup"><span data-stu-id="d3d05-154">**Target data format** – Select the format to export data to.</span></span>

1. <span data-ttu-id="d3d05-155">**追加** を選択して新しい行を追加し、**閉じる** を選択してダイアログ ボックスを閉じます。</span><span class="sxs-lookup"><span data-stu-id="d3d05-155">Select **Add** to add the new row, and then select **Close** to close the dialog box.</span></span>
1. <span data-ttu-id="d3d05-156">通常は、一度にレポート 1 件をエクスポートします。</span><span class="sxs-lookup"><span data-stu-id="d3d05-156">Usually, you will export one report at a time.</span></span> <span data-ttu-id="d3d05-157">1 つのレポートをエクスポートするには、**照会** ダイアログボックスに追加した行に対してフィルタを設定します。</span><span class="sxs-lookup"><span data-stu-id="d3d05-157">To export a single report, set up a filter for the row that you just added to the **Inquiry** dialog box.</span></span> <span data-ttu-id="d3d05-158">このようにして、**在庫金額** エンティティからのレポートをエクスポートに含めるように定義できます。</span><span class="sxs-lookup"><span data-stu-id="d3d05-158">In this way, you can define which report from the **Inventory value** entity is included in your export.</span></span> <span data-ttu-id="d3d05-159">以下の手順に従って、単一のレポートをエクスポートするには、以下のフィルタ オプションを設定します：</span><span class="sxs-lookup"><span data-stu-id="d3d05-159">Follow these steps to set the following filter options to export a single report:</span></span>

    1. <span data-ttu-id="d3d05-160">**範囲** タブで、**追加** を選択して新しい列を追加します。</span><span class="sxs-lookup"><span data-stu-id="d3d05-160">On the **Range** tab, select **Add** to add a row.</span></span>
    2. <span data-ttu-id="d3d05-161">**テーブル** フィールドを **在庫評価額** に設定します。</span><span class="sxs-lookup"><span data-stu-id="d3d05-161">Set the **Table** field to **Inventory value**.</span></span>
    3. <span data-ttu-id="d3d05-162">**派生テーブル** フィールドを **在庫評価額** に設定します。</span><span class="sxs-lookup"><span data-stu-id="d3d05-162">Set the **Derived table** field to **Inventory value**.</span></span>
    4. <span data-ttu-id="d3d05-163">フィルター処理の対象となる **フィールド** を設定します。</span><span class="sxs-lookup"><span data-stu-id="d3d05-163">Set the **Field** field to the field that you want to filter by.</span></span> <span data-ttu-id="d3d05-164">通常は、**実行名** フィールドと **実行時間** フィールドのいずれか、または両方を使用します。</span><span class="sxs-lookup"><span data-stu-id="d3d05-164">Usually, you will use the **Execution name** field and/or the **Execution time** field.</span></span>
    5. <span data-ttu-id="d3d05-165">**基準** フィールドを、選択したフィールドで検索する値に変更します。</span><span class="sxs-lookup"><span data-stu-id="d3d05-165">Set the **Criteria** field to the value that you want to look for in the selected field.</span></span> <span data-ttu-id="d3d05-166">(前の手順で **実行名** フィールドを選択している場合、この値はレポートの名前になります。</span><span class="sxs-lookup"><span data-stu-id="d3d05-166">(If you selected the **Execution name** field in the previous step, this value will be the name of the report.</span></span> <span data-ttu-id="d3d05-167">**実行時間** フィールドを選択した場合は、レポートが生成された時刻になります）</span><span class="sxs-lookup"><span data-stu-id="d3d05-167">If you selected the **Execution time** field, it will be the time when the report was generated.)</span></span>
    6. <span data-ttu-id="d3d05-168">必要に応じて、探しているレポートが一意に識別されるまで、 **範囲** タブにさらに行を追加します。</span><span class="sxs-lookup"><span data-stu-id="d3d05-168">Add more rows to the **Range** tab as you require, until you've uniquely identified the report that you're looking for.</span></span>

1. <span data-ttu-id="d3d05-169">**OK** を選択して設定を保存し、ダイアログ ボックスを閉じます。</span><span class="sxs-lookup"><span data-stu-id="d3d05-169">Select **OK** to save your settings and close the dialog box.</span></span>
1. <span data-ttu-id="d3d05-170">**保存** を選択し、エクスポート設定を保存します。</span><span class="sxs-lookup"><span data-stu-id="d3d05-170">Select **Save** to save your export setup.</span></span>
1. <span data-ttu-id="d3d05-171">**エクスポート オプション** タブをで、**今すぐエクスポート** を選択して、エクスポート ファイルを生成します。</span><span class="sxs-lookup"><span data-stu-id="d3d05-171">On the **Export options** tab, select **Export now** to generate the export file.</span></span>
1. <span data-ttu-id="d3d05-172">**実行の概要** ページが表示され、エクスポートジョブの状態とエクスポートされたエンティティのリストを表示することができます。</span><span class="sxs-lookup"><span data-stu-id="d3d05-172">On the **Execution summary** page that appears, you can view the status of your export job and a list of the entities that were exported.</span></span> <span data-ttu-id="d3d05-173">**エンティティ処理の状態** セクションで、一覧表示されている **在庫評価額** エンティティを選択し、**ファイルのダウンロード** を選び、エンティティからエクスポートされたデータをダウンロードします。</span><span class="sxs-lookup"><span data-stu-id="d3d05-173">In the **Entity processing status** section, select the **Inventory value** entity in the list, and then select **Download file** to download the data that was exported from that entity.</span></span>

<span data-ttu-id="d3d05-174">データをエクスポートするためのデータ管理の使用方法については、[データ インポートとエクスポートのジョブ概要](../../fin-ops-core/dev-itpro/data-entities/data-import-export-job.md) を参照してください。</span><span class="sxs-lookup"><span data-stu-id="d3d05-174">For more information about how to use data management to export data, see [Data import and export jobs overview](../../fin-ops-core/dev-itpro/data-entities/data-import-export-job.md).</span></span>
