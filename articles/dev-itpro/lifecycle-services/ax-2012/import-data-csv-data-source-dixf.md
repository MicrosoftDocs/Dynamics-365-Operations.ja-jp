---
title: "CSV データ ソースからのデータのインポート"
description: "Microsoft Dynamics AX 2012 のデータのインポート/エクスポート フレームワークを使用すると、CSV ファイルからのデータを Microsoft Dynamics AX にインポートすることができます。"
author: kfend
manager: AnnBe
ms.date: 11/13/2017
ms.topic: article
ms.prod: dynamics-ax-2012
ms.service: 
ms.technology: 
audience: Developer, IT Pro
ms.reviewer: kfend
ms.search.scope: AX 2012
ms.custom: 18801
ms.assetid: f358a897-31c0-46fe-a554-3798afa2f65d
ms.search.region: Global
ms.author: kfend
ms.search.validFrom: 
ms.dyn365.ops.version: 2012
ms.translationtype: HT
ms.sourcegitcommit: e782d33f3748524491dace28008cd9148ae70529
ms.openlocfilehash: 079164dbee2ae22da220b6bbd941876a201abad7
ms.contentlocale: ja-jp
ms.lasthandoff: 08/09/2018

---

# <a name="import-data-from-csv-data-sources"></a><span data-ttu-id="3b72f-103">CSV データ ソースからのデータのインポート</span><span class="sxs-lookup"><span data-stu-id="3b72f-103">Import data from CSV data sources</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="3b72f-104">Microsoft Dynamics AX 2012 のデータのインポート/エクスポート フレームワークを使用すると、CSV ファイルからのデータを Microsoft Dynamics AX にインポートすることができます。</span><span class="sxs-lookup"><span data-stu-id="3b72f-104">You can use the Microsoft Dynamics AX 2012 Data Import/Export Framework to import data from a CSV file into Microsoft Dynamics AX.</span></span>

<span data-ttu-id="3b72f-105">このチュートリアルでは、次のタスクを説明する例を示します。</span><span class="sxs-lookup"><span data-stu-id="3b72f-105">This walkthrough provides examples to illustrate the following tasks:</span></span>

-   <span data-ttu-id="3b72f-106">ソースとして使用する CSV ファイルを検索します</span><span class="sxs-lookup"><span data-stu-id="3b72f-106">Find a CSV file to use as a source</span></span>
-   <span data-ttu-id="3b72f-107">ソース データのフォーマットを形式する</span><span class="sxs-lookup"><span data-stu-id="3b72f-107">Define the format of your source data</span></span>
-   <span data-ttu-id="3b72f-108">処理グループの定義</span><span class="sxs-lookup"><span data-stu-id="3b72f-108">Define a processing group</span></span>
-   <span data-ttu-id="3b72f-109">ソースからステージングにデータを処理</span><span class="sxs-lookup"><span data-stu-id="3b72f-109">Process data from source to staging</span></span>
-   <span data-ttu-id="3b72f-110">ステージングのデータの検証</span><span class="sxs-lookup"><span data-stu-id="3b72f-110">Validate the data in staging</span></span>
-   <span data-ttu-id="3b72f-111">ステージングからターゲットにデータを処理</span><span class="sxs-lookup"><span data-stu-id="3b72f-111">Process data from staging to target</span></span>
-   <span data-ttu-id="3b72f-112">ターゲットのデータの検証</span><span class="sxs-lookup"><span data-stu-id="3b72f-112">Validate the data in target</span></span>

## <a name="prerequisites"></a><span data-ttu-id="3b72f-113">前提条件</span><span class="sxs-lookup"><span data-stu-id="3b72f-113">Prerequisites</span></span>
<span data-ttu-id="3b72f-114">このチュートリアルを完了するには、次のものが必要です。</span><span class="sxs-lookup"><span data-stu-id="3b72f-114">To complete this walkthrough you will need:</span></span>

-   <span data-ttu-id="3b72f-115">Microsoft Dynamics AX 2012、Microsoft Dynamics AX 2012 R2、または Microsoft Dynamics AX 2012 R3</span><span class="sxs-lookup"><span data-stu-id="3b72f-115">Microsoft Dynamics AX 2012, Microsoft Dynamics AX 2012 R2, or Microsoft Dynamics AX 2012 R3</span></span>
-   <span data-ttu-id="3b72f-116">データのインポート/エクスポート フレームワーク</span><span class="sxs-lookup"><span data-stu-id="3b72f-116">Data Import/Export Framework</span></span>

## <a name="find-a-csv-file-to-use-as-a-source"></a><span data-ttu-id="3b72f-117">ソースとして使用する CSV ファイルを検索します</span><span class="sxs-lookup"><span data-stu-id="3b72f-117">Find a CSV file to use as a source</span></span>
<span data-ttu-id="3b72f-118">この例を実行するには、データ インポート/エクスポート フレームワークに同梱されている区切りデモ ファイルのいずれかを使用します。</span><span class="sxs-lookup"><span data-stu-id="3b72f-118">To work through this example, use any of the delimited demo files that are shipped with the Data Import/Export Framework.</span></span> <span data-ttu-id="3b72f-119">デモ ファイルでの詳細については、[データのインポート/エクスポート フレームワークのデモ ファイル (DIXF、DMF)](demo-files-dixf.md) を参照してください。</span><span class="sxs-lookup"><span data-stu-id="3b72f-119">For more information on the demo files, see [Demo files for the Data import/export framework (DIXF, DMF)](demo-files-dixf.md).</span></span>

## <a name="define-the-format-of-your-source-data"></a><span data-ttu-id="3b72f-120">ソース データのフォーマットを形式する</span><span class="sxs-lookup"><span data-stu-id="3b72f-120">Define the format of your source data</span></span>
1.  <span data-ttu-id="3b72f-121">**データのインポート/エクスポート フレームワーク**を開き、**設定** &gt; **ソース データ形式**をクリックします。</span><span class="sxs-lookup"><span data-stu-id="3b72f-121">Open **Data Import/Export Framework**, and then click **Setup** &gt; **Source data formats**.</span></span>
2.  <span data-ttu-id="3b72f-122">**新規**をクリックし、ソースの名前 CSV を入力します。</span><span class="sxs-lookup"><span data-stu-id="3b72f-122">Click **New** and enter the name CSV for the source.</span></span>
3.  <span data-ttu-id="3b72f-123">ソース タイプが **ファイル** であることを確認します。</span><span class="sxs-lookup"><span data-stu-id="3b72f-123">Verify that the source type is **File**.</span></span>
4.  <span data-ttu-id="3b72f-124">次のオプションをコンフィギュレーションします。</span><span class="sxs-lookup"><span data-stu-id="3b72f-124">Configure the following options:</span></span>

    | <span data-ttu-id="3b72f-125">**設定**</span><span class="sxs-lookup"><span data-stu-id="3b72f-125">**Setting**</span></span>                     | <span data-ttu-id="3b72f-126">**値**</span><span class="sxs-lookup"><span data-stu-id="3b72f-126">**Value**</span></span>                                                                                    |
    |---------------------------------|----------------------------------------------------------------------------------------------|
    | <span data-ttu-id="3b72f-127">**ファイル形式**</span><span class="sxs-lookup"><span data-stu-id="3b72f-127">**File format**</span></span>                 | <span data-ttu-id="3b72f-128">区切り</span><span class="sxs-lookup"><span data-stu-id="3b72f-128">Delimited</span></span>                                                                                    |
    | <span data-ttu-id="3b72f-129">**先頭行のヘッダー**</span><span class="sxs-lookup"><span data-stu-id="3b72f-129">**First row header**</span></span>            | <span data-ttu-id="3b72f-130">選択済</span><span class="sxs-lookup"><span data-stu-id="3b72f-130">Selected</span></span>                                                                                     |
    | <span data-ttu-id="3b72f-131">**行区切り**</span><span class="sxs-lookup"><span data-stu-id="3b72f-131">**Row delimiter**</span></span>               | <span data-ttu-id="3b72f-132">{CR}{LF}</span><span class="sxs-lookup"><span data-stu-id="3b72f-132">{CR}{LF}</span></span>                                                                                     |
    | <span data-ttu-id="3b72f-133">**列区切り**</span><span class="sxs-lookup"><span data-stu-id="3b72f-133">**Column delimiter**</span></span>            | <span data-ttu-id="3b72f-134">コンマ {,}</span><span class="sxs-lookup"><span data-stu-id="3b72f-134">Comma {,}</span></span>                                                                                    |
    | <span data-ttu-id="3b72f-135">**テキスト修飾子**</span><span class="sxs-lookup"><span data-stu-id="3b72f-135">**Text qualifier**</span></span>              | <span data-ttu-id="3b72f-136">"</span><span class="sxs-lookup"><span data-stu-id="3b72f-136">"</span></span>                                                                                            |
    | <span data-ttu-id="3b72f-137">**コード ページ**</span><span class="sxs-lookup"><span data-stu-id="3b72f-137">**Code page**</span></span>                   | <span data-ttu-id="3b72f-138">1252 西ヨーロッパ (Windows)</span><span class="sxs-lookup"><span data-stu-id="3b72f-138">1252 Western European (Windows)</span></span>                                                              |
    | <span data-ttu-id="3b72f-139">**Unicode**</span><span class="sxs-lookup"><span data-stu-id="3b72f-139">**Unicode**</span></span>                     | <span data-ttu-id="3b72f-140">未選択</span><span class="sxs-lookup"><span data-stu-id="3b72f-140">Not selected</span></span>                                                                                 |
    | <span data-ttu-id="3b72f-141">**言語ロケール**</span><span class="sxs-lookup"><span data-stu-id="3b72f-141">**Language locale**</span></span>             | <span data-ttu-id="3b72f-142">ja</span><span class="sxs-lookup"><span data-stu-id="3b72f-142">en-us</span></span>                                                                                        |
    | <span data-ttu-id="3b72f-143">**分析コード**</span><span class="sxs-lookup"><span data-stu-id="3b72f-143">**Dimension code**</span></span>              | <span data-ttu-id="3b72f-144">選択した分析コードは、インポートするデモ ファイルに基づいて異なります。</span><span class="sxs-lookup"><span data-stu-id="3b72f-144">The dimension code you choose will vary, based on which demo file you have chosen to import.</span></span> |
    | <span data-ttu-id="3b72f-145">**勘定科目表の区切り記号**</span><span class="sxs-lookup"><span data-stu-id="3b72f-145">**Chart of accounts delimiter**</span></span> | -                                                                                            |

## <a name="define-a-processing-group"></a><span data-ttu-id="3b72f-146">処理グループの定義</span><span class="sxs-lookup"><span data-stu-id="3b72f-146">Define a processing group</span></span>
1.  <span data-ttu-id="3b72f-147">**データのインポート/エクスポート フレームワーク**で、&gt; **共通** &gt; **処理グループ**とクリックしてから、**新規**をクリックして新しい処理グループを作成します。</span><span class="sxs-lookup"><span data-stu-id="3b72f-147">In **Data Import/Export Framework**, click &gt; **Common** &gt; **Processing group**, and then click **New** to create a new processing group.</span></span>
2.  <span data-ttu-id="3b72f-148">グループの名前と説明を設定します。</span><span class="sxs-lookup"><span data-stu-id="3b72f-148">Set the group name and description.</span></span>
3.  <span data-ttu-id="3b72f-149">処理グループに含めるエンティティを選択するには、**エンティティ**をクリックし、次の情報を入力します。</span><span class="sxs-lookup"><span data-stu-id="3b72f-149">Click **Entities** to select the entities to include in the processing group, and enter the following information.</span></span>
    1.  <span data-ttu-id="3b72f-150">**処理グループのエンティティの選択**フォームで、**新規**をクリックしてから、**エンティティ名**に名前を入力します。</span><span class="sxs-lookup"><span data-stu-id="3b72f-150">In the **Select entities for processing group** form, click **New**, and then, for **Entity name**, enter a name.</span></span>
    2.  <span data-ttu-id="3b72f-151">**ソース データ形式** を CSV に設定します。</span><span class="sxs-lookup"><span data-stu-id="3b72f-151">Set the **Source data format** to CSV.</span></span>
    3.  <span data-ttu-id="3b72f-152">**サンプル ファイルのパス フィールド**で、次の場所にあるデモ ファイルからインポートするファイルを見つけます。Program Files/Microsoft Dynamics AX 2012/データのインポート/エクスポート フレームワーク クライアントのコンポーネント&lt;バージョン&gt;DemoFilesDelimited。</span><span class="sxs-lookup"><span data-stu-id="3b72f-152">In the **Sample file path field**, locate the file to import from the demo files at the following location: Program Files/Microsoft Dynamics AX 2012/Data Import/Export Framework Client Component&lt;version&gt;DemoFilesDelimited.</span></span>
    4.  <span data-ttu-id="3b72f-153">**ソース マッピングの生成**をクリックします。</span><span class="sxs-lookup"><span data-stu-id="3b72f-153">Click **Generate source mapping**.</span></span>
    5.  <span data-ttu-id="3b72f-154">ソース マッピングを表示するには、**ソース マッピングを変更** をクリックします。</span><span class="sxs-lookup"><span data-stu-id="3b72f-154">To view the source mapping, click **Modify source mapping**.</span></span> <span data-ttu-id="3b72f-155">**ソースをステージングにマップ** フォームを閉じます。</span><span class="sxs-lookup"><span data-stu-id="3b72f-155">Close the **Map source to staging** form.</span></span>
    6.  <span data-ttu-id="3b72f-156">**検証**をクリックします。</span><span class="sxs-lookup"><span data-stu-id="3b72f-156">Click **Validate**.</span></span>
    7.  <span data-ttu-id="3b72f-157">**ソース ファイルのプレビュー**をクリックし、**処理グループのエンティティの選択**フォームを閉じます。</span><span class="sxs-lookup"><span data-stu-id="3b72f-157">Click **Preview source file**, and then close the **Select entities for processing group** form.</span></span>

## <a name="process-data-from-source-to-staging"></a><span data-ttu-id="3b72f-158">ソースからステージングにデータを処理</span><span class="sxs-lookup"><span data-stu-id="3b72f-158">Process data from source to staging</span></span>
1.  <span data-ttu-id="3b72f-159">**処理グループ** フォームで、作成したグループを選択して**ステージング データの取得**をクリックします。</span><span class="sxs-lookup"><span data-stu-id="3b72f-159">In the **Processing group** form, select the group that you created, and click **Get staging data**.</span></span> <span data-ttu-id="3b72f-160">**ステージング データ ジョブに対するジョブ ID の作成** フォームが開きます。</span><span class="sxs-lookup"><span data-stu-id="3b72f-160">The **Create a job ID for the staging data job** form opens.</span></span>
2.  <span data-ttu-id="3b72f-161">既定では、ジョブの ID が生成されます。</span><span class="sxs-lookup"><span data-stu-id="3b72f-161">By default, an ID for the job is generated.</span></span> <span data-ttu-id="3b72f-162">必要に応じて、IDを変更して説明を追加することができます。</span><span class="sxs-lookup"><span data-stu-id="3b72f-162">You can optionally modify the ID and add a description.</span></span> <span data-ttu-id="3b72f-163">**OK** をクリックします。</span><span class="sxs-lookup"><span data-stu-id="3b72f-163">Click **OK**.</span></span> <span data-ttu-id="3b72f-164">**ステージング データ実行** フォームが開きます。</span><span class="sxs-lookup"><span data-stu-id="3b72f-164">The **Staging data execution** form opens.</span></span>
3.  <span data-ttu-id="3b72f-165">**エンティティの詳細** で、すべてのソース データを含むファイルのパスを入力し、**実行** をクリックします。します。</span><span class="sxs-lookup"><span data-stu-id="3b72f-165">Under **Entity details**, enter the path of the file that contains all of your source data, and then click **Run**.</span></span> <span data-ttu-id="3b72f-166">**注記:** サンプル ファイルと完全なソース ファイルが異なる場合、この時点で完全なソース ファイルに変更されます。</span><span class="sxs-lookup"><span data-stu-id="3b72f-166">**Note:** If your sample file and full source file are different from each other, you would change to your full source file at this point.</span></span>
4.  <span data-ttu-id="3b72f-167">**ソースからステージングにデータを取得**フォームで、**OK** をクリックしてすぐに実行します。</span><span class="sxs-lookup"><span data-stu-id="3b72f-167">In the **Get data from source to staging** form, click **OK** to run immediately.</span></span> <span data-ttu-id="3b72f-168">ソース データはステージング テーブルにコピーされます。</span><span class="sxs-lookup"><span data-stu-id="3b72f-168">The source data is copied to the staging tables.</span></span>

## <a name="validate-the-data-in-staging"></a><span data-ttu-id="3b72f-169">ステージングのデータの検証</span><span class="sxs-lookup"><span data-stu-id="3b72f-169">Validate the data in staging</span></span>
1.  <span data-ttu-id="3b72f-170">**データのインポート/エクスポート フレームワーク**で、**共通** &gt; **処理グループ** &gt; **実行履歴**とクリックしてから実行したジョブを選択します。</span><span class="sxs-lookup"><span data-stu-id="3b72f-170">In **Data Import/Export Framework**, click **Common** &gt; **Processing group** &gt; **Execution history**, and then select the job that ran.</span></span>
2.  <span data-ttu-id="3b72f-171">**ステージング データの表示**をクリックします。</span><span class="sxs-lookup"><span data-stu-id="3b72f-171">Click **View staging data**.</span></span>
3.  <span data-ttu-id="3b72f-172">ソース ファイルと一致することを検証するステージング データを確認します。</span><span class="sxs-lookup"><span data-stu-id="3b72f-172">Review the staging data to validate that it matches the source file.</span></span>
4.  <span data-ttu-id="3b72f-173">**すべて検証**をクリックして、関連するすべての参照データが正しくシステムに存在することを確認します。</span><span class="sxs-lookup"><span data-stu-id="3b72f-173">Click **Validate all** to verify that all the related reference data is correct and present in the system.</span></span>

## <a name="process-data-from-staging-to-target"></a><span data-ttu-id="3b72f-174">ステージングからターゲットにデータを処理</span><span class="sxs-lookup"><span data-stu-id="3b72f-174">Process data from staging to target</span></span>
1.  <span data-ttu-id="3b72f-175">**データのインポート/エクスポート フレームワーク**で、**共通** &gt; **処理グループ**とクリックしてから、操作する処理グループを選択します。</span><span class="sxs-lookup"><span data-stu-id="3b72f-175">In **Data Import/Export Framework**, click **Common** &gt; **Processing group**, and then select the processing group to work with.</span></span>
2.  <span data-ttu-id="3b72f-176">**データをターゲットにコピー**をクリックします。</span><span class="sxs-lookup"><span data-stu-id="3b72f-176">Click **Copy data to target**.</span></span> <span data-ttu-id="3b72f-177">**実行するジョブ ID を選択** ダイアログ ボックスが開きます。</span><span class="sxs-lookup"><span data-stu-id="3b72f-177">The **Select a job ID to run** dialog box opens.</span></span>
3.  <span data-ttu-id="3b72f-178">前の手順で作成したジョブを選択し、**OK** をクリックします。</span><span class="sxs-lookup"><span data-stu-id="3b72f-178">Select the job that you created in the previous procedure, and click **OK**.</span></span> <span data-ttu-id="3b72f-179">**ターゲット データ実行** ダイアログ ボックスが開きます。</span><span class="sxs-lookup"><span data-stu-id="3b72f-179">The **Target data execution** dialog box opens.</span></span>
4.  <span data-ttu-id="3b72f-180">**実行**をクリックし、**OK** をクリックします。</span><span class="sxs-lookup"><span data-stu-id="3b72f-180">Click **Run**, and then click **OK**.</span></span> <span data-ttu-id="3b72f-181">データはターゲット エンティティにコピーされます。</span><span class="sxs-lookup"><span data-stu-id="3b72f-181">The data is copied to the target entities.</span></span>

## <a name="validate-the-data-in-target"></a><span data-ttu-id="3b72f-182">ターゲットのデータの検証</span><span class="sxs-lookup"><span data-stu-id="3b72f-182">Validate the data in target</span></span>
<span data-ttu-id="3b72f-183">ステージング データの表示:</span><span class="sxs-lookup"><span data-stu-id="3b72f-183">View staging data:</span></span>

1.  <span data-ttu-id="3b72f-184">**データのインポート/エクスポート フレームワーク**で、**共通** &gt; **処理グループ** &gt; **実行履歴** &gt; **ステージング データの表示**とクリックしてから実行したジョブを選択します。</span><span class="sxs-lookup"><span data-stu-id="3b72f-184">In **Data Import/Export Framework**, click **Common** &gt; **Processing group** &gt; **Execution history** &gt; **View staging data**, and then select the job that ran.</span></span>
2.  <span data-ttu-id="3b72f-185">**ターゲット**をクリックします。</span><span class="sxs-lookup"><span data-stu-id="3b72f-185">Click **Target**.</span></span>
3.  <span data-ttu-id="3b72f-186">データが正しいことを確認します。</span><span class="sxs-lookup"><span data-stu-id="3b72f-186">Verify that the data is correct.</span></span>





