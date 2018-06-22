---
title: "CSV データ ソースからのデータのインポート (AX 2012)"
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
ms.sourcegitcommit: efcb77ff883b29a4bbaba27551e02311742afbbd
ms.openlocfilehash: 58226b27c2bf62df36eb5e9d67796888b5e0f945
ms.contentlocale: ja-jp
ms.lasthandoff: 05/08/2018

---

# <a name="import-data-from-a-csv-data-source-ax-2012"></a><span data-ttu-id="035ac-103">CSV データ ソースからのデータのインポート (AX 2012)</span><span class="sxs-lookup"><span data-stu-id="035ac-103">Import data from a CSV data source (AX 2012)</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="035ac-104">Microsoft Dynamics AX 2012 のデータのインポート/エクスポート フレームワークを使用すると、CSV ファイルからのデータを Microsoft Dynamics AX にインポートすることができます。</span><span class="sxs-lookup"><span data-stu-id="035ac-104">You can use the Microsoft Dynamics AX 2012 Data Import/Export Framework to import data from a CSV file into Microsoft Dynamics AX.</span></span>

<span data-ttu-id="035ac-105">このチュートリアルでは、次のタスクを説明する例を示します。</span><span class="sxs-lookup"><span data-stu-id="035ac-105">This walkthrough provides examples to illustrate the following tasks:</span></span>

-   <span data-ttu-id="035ac-106">ソースとして使用する CSV ファイルを検索します</span><span class="sxs-lookup"><span data-stu-id="035ac-106">Find a CSV file to use as a source</span></span>
-   <span data-ttu-id="035ac-107">ソース データのフォーマットを形式する</span><span class="sxs-lookup"><span data-stu-id="035ac-107">Define the format of your source data</span></span>
-   <span data-ttu-id="035ac-108">処理グループの定義</span><span class="sxs-lookup"><span data-stu-id="035ac-108">Define a processing group</span></span>
-   <span data-ttu-id="035ac-109">ソースからステージングにデータを処理</span><span class="sxs-lookup"><span data-stu-id="035ac-109">Process data from source to staging</span></span>
-   <span data-ttu-id="035ac-110">ステージングのデータの検証</span><span class="sxs-lookup"><span data-stu-id="035ac-110">Validate the data in staging</span></span>
-   <span data-ttu-id="035ac-111">ステージングからターゲットにデータを処理</span><span class="sxs-lookup"><span data-stu-id="035ac-111">Process data from staging to target</span></span>
-   <span data-ttu-id="035ac-112">ターゲットのデータの検証</span><span class="sxs-lookup"><span data-stu-id="035ac-112">Validate the data in target</span></span>

## <a name="prerequisites"></a><span data-ttu-id="035ac-113">前提条件</span><span class="sxs-lookup"><span data-stu-id="035ac-113">Prerequisites</span></span>
<span data-ttu-id="035ac-114">このチュートリアルを完了するには、次のものが必要です。</span><span class="sxs-lookup"><span data-stu-id="035ac-114">To complete this walkthrough you will need:</span></span>

-   <span data-ttu-id="035ac-115">Microsoft Dynamics AX 2012、Microsoft Dynamics AX 2012 R2、または Microsoft Dynamics AX 2012 R3</span><span class="sxs-lookup"><span data-stu-id="035ac-115">Microsoft Dynamics AX 2012, Microsoft Dynamics AX 2012 R2, or Microsoft Dynamics AX 2012 R3</span></span>
-   <span data-ttu-id="035ac-116">データのインポート/エクスポート フレームワーク</span><span class="sxs-lookup"><span data-stu-id="035ac-116">Data Import/Export Framework</span></span>

## <a name="find-a-csv-file-to-use-as-a-source"></a><span data-ttu-id="035ac-117">ソースとして使用する CSV ファイルを検索します</span><span class="sxs-lookup"><span data-stu-id="035ac-117">Find a CSV file to use as a source</span></span>
<span data-ttu-id="035ac-118">この例を実行するには、データ インポート/エクスポート フレームワークに同梱されている区切りデモ ファイルのいずれかを使用します。</span><span class="sxs-lookup"><span data-stu-id="035ac-118">To work through this example, use any of the delimited demo files that are shipped with the Data Import/Export Framework.</span></span> <span data-ttu-id="035ac-119">デモ ファイルでの詳細については、[データのインポート/エクスポート フレームワークのデモ ファイル (DIXF、DMF)](demo-files-dixf.md) を参照してください。</span><span class="sxs-lookup"><span data-stu-id="035ac-119">For more information on the demo files, see [Demo files for the Data import/export framework (DIXF, DMF)](demo-files-dixf.md).</span></span>

## <a name="define-the-format-of-your-source-data"></a><span data-ttu-id="035ac-120">ソース データのフォーマットを形式する</span><span class="sxs-lookup"><span data-stu-id="035ac-120">Define the format of your source data</span></span>
1.  <span data-ttu-id="035ac-121">**データのインポート/エクスポート フレームワーク**を開き、**設定** &gt; **ソース データ形式**をクリックします。</span><span class="sxs-lookup"><span data-stu-id="035ac-121">Open **Data Import/Export Framework**, and then click **Setup** &gt; **Source data formats**.</span></span>
2.  <span data-ttu-id="035ac-122">**新規**をクリックし、ソースの名前 CSV を入力します。</span><span class="sxs-lookup"><span data-stu-id="035ac-122">Click **New** and enter the name CSV for the source.</span></span>
3.  <span data-ttu-id="035ac-123">ソース タイプが **ファイル** であることを確認します。</span><span class="sxs-lookup"><span data-stu-id="035ac-123">Verify that the source type is **File**.</span></span>
4.  <span data-ttu-id="035ac-124">次のオプションをコンフィギュレーションします。</span><span class="sxs-lookup"><span data-stu-id="035ac-124">Configure the following options:</span></span>

    | <span data-ttu-id="035ac-125">**設定**</span><span class="sxs-lookup"><span data-stu-id="035ac-125">**Setting**</span></span>                     | <span data-ttu-id="035ac-126">**値**</span><span class="sxs-lookup"><span data-stu-id="035ac-126">**Value**</span></span>                                                                                    |
    |---------------------------------|----------------------------------------------------------------------------------------------|
    | <span data-ttu-id="035ac-127">**ファイル形式**</span><span class="sxs-lookup"><span data-stu-id="035ac-127">**File format**</span></span>                 | <span data-ttu-id="035ac-128">区切り</span><span class="sxs-lookup"><span data-stu-id="035ac-128">Delimited</span></span>                                                                                    |
    | <span data-ttu-id="035ac-129">**先頭行のヘッダー**</span><span class="sxs-lookup"><span data-stu-id="035ac-129">**First row header**</span></span>            | <span data-ttu-id="035ac-130">選択済</span><span class="sxs-lookup"><span data-stu-id="035ac-130">Selected</span></span>                                                                                     |
    | <span data-ttu-id="035ac-131">**行区切り**</span><span class="sxs-lookup"><span data-stu-id="035ac-131">**Row delimiter**</span></span>               | <span data-ttu-id="035ac-132">{CR}{LF}</span><span class="sxs-lookup"><span data-stu-id="035ac-132">{CR}{LF}</span></span>                                                                                     |
    | <span data-ttu-id="035ac-133">**列区切り**</span><span class="sxs-lookup"><span data-stu-id="035ac-133">**Column delimiter**</span></span>            | <span data-ttu-id="035ac-134">コンマ {,}</span><span class="sxs-lookup"><span data-stu-id="035ac-134">Comma {,}</span></span>                                                                                    |
    | <span data-ttu-id="035ac-135">**テキスト修飾子**</span><span class="sxs-lookup"><span data-stu-id="035ac-135">**Text qualifier**</span></span>              | <span data-ttu-id="035ac-136">"</span><span class="sxs-lookup"><span data-stu-id="035ac-136">"</span></span>                                                                                            |
    | <span data-ttu-id="035ac-137">**コード ページ**</span><span class="sxs-lookup"><span data-stu-id="035ac-137">**Code page**</span></span>                   | <span data-ttu-id="035ac-138">1252 西ヨーロッパ (Windows)</span><span class="sxs-lookup"><span data-stu-id="035ac-138">1252 Western European (Windows)</span></span>                                                              |
    | <span data-ttu-id="035ac-139">**Unicode**</span><span class="sxs-lookup"><span data-stu-id="035ac-139">**Unicode**</span></span>                     | <span data-ttu-id="035ac-140">未選択</span><span class="sxs-lookup"><span data-stu-id="035ac-140">Not selected</span></span>                                                                                 |
    | <span data-ttu-id="035ac-141">**言語ロケール**</span><span class="sxs-lookup"><span data-stu-id="035ac-141">**Language locale**</span></span>             | <span data-ttu-id="035ac-142">ja</span><span class="sxs-lookup"><span data-stu-id="035ac-142">en-us</span></span>                                                                                        |
    | <span data-ttu-id="035ac-143">**分析コード**</span><span class="sxs-lookup"><span data-stu-id="035ac-143">**Dimension code**</span></span>              | <span data-ttu-id="035ac-144">選択した分析コードは、インポートするデモ ファイルに基づいて異なります。</span><span class="sxs-lookup"><span data-stu-id="035ac-144">The dimension code you choose will vary, based on which demo file you have chosen to import.</span></span> |
    | <span data-ttu-id="035ac-145">**勘定科目表の区切り記号**</span><span class="sxs-lookup"><span data-stu-id="035ac-145">**Chart of accounts delimiter**</span></span> | -                                                                                            |

## <a name="define-a-processing-group"></a><span data-ttu-id="035ac-146">処理グループの定義</span><span class="sxs-lookup"><span data-stu-id="035ac-146">Define a processing group</span></span>
1.  <span data-ttu-id="035ac-147">**データのインポート/エクスポート フレームワーク**で、&gt; **共通** &gt; **処理グループ**とクリックしてから、**新規**をクリックして新しい処理グループを作成します。</span><span class="sxs-lookup"><span data-stu-id="035ac-147">In **Data Import/Export Framework**, click &gt; **Common** &gt; **Processing group**, and then click **New** to create a new processing group.</span></span>
2.  <span data-ttu-id="035ac-148">グループの名前と説明を設定します。</span><span class="sxs-lookup"><span data-stu-id="035ac-148">Set the group name and description.</span></span>
3.  <span data-ttu-id="035ac-149">処理グループに含めるエンティティを選択するには、**エンティティ**をクリックし、次の情報を入力します。</span><span class="sxs-lookup"><span data-stu-id="035ac-149">Click **Entities** to select the entities to include in the processing group, and enter the following information.</span></span>
    1.  <span data-ttu-id="035ac-150">**処理グループのエンティティの選択**フォームで、**新規**をクリックしてから、**エンティティ名**に名前を入力します。</span><span class="sxs-lookup"><span data-stu-id="035ac-150">In the **Select entities for processing group** form, click **New**, and then, for **Entity name**, enter a name.</span></span>
    2.  <span data-ttu-id="035ac-151">**ソース データ形式** を CSV に設定します。</span><span class="sxs-lookup"><span data-stu-id="035ac-151">Set the **Source data format** to CSV.</span></span>
    3.  <span data-ttu-id="035ac-152">**サンプル ファイルのパス フィールド**で、次の場所にあるデモ ファイルからインポートするファイルを見つけます。Program Files/Microsoft Dynamics AX 2012/データのインポート/エクスポート フレームワーク クライアントのコンポーネント&lt;バージョン&gt;DemoFilesDelimited。</span><span class="sxs-lookup"><span data-stu-id="035ac-152">In the **Sample file path field**, locate the file to import from the demo files at the following location: Program Files/Microsoft Dynamics AX 2012/Data Import/Export Framework Client Component&lt;version&gt;DemoFilesDelimited.</span></span>
    4.  <span data-ttu-id="035ac-153">**ソース マッピングの生成**をクリックします。</span><span class="sxs-lookup"><span data-stu-id="035ac-153">Click **Generate source mapping**.</span></span>
    5.  <span data-ttu-id="035ac-154">ソース マッピングを表示するには、**ソース マッピングを変更** をクリックします。</span><span class="sxs-lookup"><span data-stu-id="035ac-154">To view the source mapping, click **Modify source mapping**.</span></span> <span data-ttu-id="035ac-155">**ソースをステージングにマップ** フォームを閉じます。</span><span class="sxs-lookup"><span data-stu-id="035ac-155">Close the **Map source to staging** form.</span></span>
    6.  <span data-ttu-id="035ac-156">**検証**をクリックします。</span><span class="sxs-lookup"><span data-stu-id="035ac-156">Click **Validate**.</span></span>
    7.  <span data-ttu-id="035ac-157">**ソース ファイルのプレビュー**をクリックし、**処理グループのエンティティの選択**フォームを閉じます。</span><span class="sxs-lookup"><span data-stu-id="035ac-157">Click **Preview source file**, and then close the **Select entities for processing group** form.</span></span>

## <a name="process-data-from-source-to-staging"></a><span data-ttu-id="035ac-158">ソースからステージングにデータを処理</span><span class="sxs-lookup"><span data-stu-id="035ac-158">Process data from source to staging</span></span>
1.  <span data-ttu-id="035ac-159">**処理グループ** フォームで、作成したグループを選択して**ステージング データの取得**をクリックします。</span><span class="sxs-lookup"><span data-stu-id="035ac-159">In the **Processing group** form, select the group that you created, and click **Get staging data**.</span></span> <span data-ttu-id="035ac-160">**ステージング データ ジョブに対するジョブ ID の作成** フォームが開きます。</span><span class="sxs-lookup"><span data-stu-id="035ac-160">The **Create a job ID for the staging data job** form opens.</span></span>
2.  <span data-ttu-id="035ac-161">既定では、ジョブの ID が生成されます。</span><span class="sxs-lookup"><span data-stu-id="035ac-161">By default, an ID for the job is generated.</span></span> <span data-ttu-id="035ac-162">必要に応じて、IDを変更して説明を追加することができます。</span><span class="sxs-lookup"><span data-stu-id="035ac-162">You can optionally modify the ID and add a description.</span></span> <span data-ttu-id="035ac-163">**OK** をクリックします。</span><span class="sxs-lookup"><span data-stu-id="035ac-163">Click **OK**.</span></span> <span data-ttu-id="035ac-164">**ステージング データ実行** フォームが開きます。</span><span class="sxs-lookup"><span data-stu-id="035ac-164">The **Staging data execution** form opens.</span></span>
3.  <span data-ttu-id="035ac-165">**エンティティの詳細** で、すべてのソース データを含むファイルのパスを入力し、**実行** をクリックします。します。</span><span class="sxs-lookup"><span data-stu-id="035ac-165">Under **Entity details**, enter the path of the file that contains all of your source data, and then click **Run**.</span></span> <span data-ttu-id="035ac-166">**注記:** サンプル ファイルと完全なソース ファイルが異なる場合、この時点で完全なソース ファイルに変更されます。</span><span class="sxs-lookup"><span data-stu-id="035ac-166">**Note:** If your sample file and full source file are different from each other, you would change to your full source file at this point.</span></span>
4.  <span data-ttu-id="035ac-167">**ソースからステージングにデータを取得**フォームで、**OK** をクリックしてすぐに実行します。</span><span class="sxs-lookup"><span data-stu-id="035ac-167">In the **Get data from source to staging** form, click **OK** to run immediately.</span></span> <span data-ttu-id="035ac-168">ソース データはステージング テーブルにコピーされます。</span><span class="sxs-lookup"><span data-stu-id="035ac-168">The source data is copied to the staging tables.</span></span>

## <a name="validate-the-data-in-staging"></a><span data-ttu-id="035ac-169">ステージングのデータの検証</span><span class="sxs-lookup"><span data-stu-id="035ac-169">Validate the data in staging</span></span>
1.  <span data-ttu-id="035ac-170">**データのインポート/エクスポート フレームワーク**で、**共通** &gt; **処理グループ** &gt; **実行履歴**とクリックしてから実行したジョブを選択します。</span><span class="sxs-lookup"><span data-stu-id="035ac-170">In **Data Import/Export Framework**, click **Common** &gt; **Processing group** &gt; **Execution history**, and then select the job that ran.</span></span>
2.  <span data-ttu-id="035ac-171">**ステージング データの表示**をクリックします。</span><span class="sxs-lookup"><span data-stu-id="035ac-171">Click **View staging data**.</span></span>
3.  <span data-ttu-id="035ac-172">ソース ファイルと一致することを検証するステージング データを確認します。</span><span class="sxs-lookup"><span data-stu-id="035ac-172">Review the staging data to validate that it matches the source file.</span></span>
4.  <span data-ttu-id="035ac-173">**すべて検証**をクリックして、関連するすべての参照データが正しくシステムに存在することを確認します。</span><span class="sxs-lookup"><span data-stu-id="035ac-173">Click **Validate all** to verify that all the related reference data is correct and present in the system.</span></span>

## <a name="process-data-from-staging-to-target"></a><span data-ttu-id="035ac-174">ステージングからターゲットにデータを処理</span><span class="sxs-lookup"><span data-stu-id="035ac-174">Process data from staging to target</span></span>
1.  <span data-ttu-id="035ac-175">**データのインポート/エクスポート フレームワーク**で、**共通** &gt; **処理グループ**とクリックしてから、操作する処理グループを選択します。</span><span class="sxs-lookup"><span data-stu-id="035ac-175">In **Data Import/Export Framework**, click **Common** &gt; **Processing group**, and then select the processing group to work with.</span></span>
2.  <span data-ttu-id="035ac-176">**データをターゲットにコピー**をクリックします。</span><span class="sxs-lookup"><span data-stu-id="035ac-176">Click **Copy data to target**.</span></span> <span data-ttu-id="035ac-177">**実行するジョブ ID を選択** ダイアログ ボックスが開きます。</span><span class="sxs-lookup"><span data-stu-id="035ac-177">The **Select a job ID to run** dialog box opens.</span></span>
3.  <span data-ttu-id="035ac-178">前の手順で作成したジョブを選択し、**OK** をクリックします。</span><span class="sxs-lookup"><span data-stu-id="035ac-178">Select the job that you created in the previous procedure, and click **OK**.</span></span> <span data-ttu-id="035ac-179">**ターゲット データ実行** ダイアログ ボックスが開きます。</span><span class="sxs-lookup"><span data-stu-id="035ac-179">The **Target data execution** dialog box opens.</span></span>
4.  <span data-ttu-id="035ac-180">**実行**をクリックし、**OK** をクリックします。</span><span class="sxs-lookup"><span data-stu-id="035ac-180">Click **Run**, and then click **OK**.</span></span> <span data-ttu-id="035ac-181">データはターゲット エンティティにコピーされます。</span><span class="sxs-lookup"><span data-stu-id="035ac-181">The data is copied to the target entities.</span></span>

## <a name="validate-the-data-in-target"></a><span data-ttu-id="035ac-182">ターゲットのデータの検証</span><span class="sxs-lookup"><span data-stu-id="035ac-182">Validate the data in target</span></span>
<span data-ttu-id="035ac-183">ステージング データの表示:</span><span class="sxs-lookup"><span data-stu-id="035ac-183">View staging data:</span></span>

1.  <span data-ttu-id="035ac-184">**データのインポート/エクスポート フレームワーク**で、**共通** &gt; **処理グループ** &gt; **実行履歴** &gt; **ステージング データの表示**とクリックしてから実行したジョブを選択します。</span><span class="sxs-lookup"><span data-stu-id="035ac-184">In **Data Import/Export Framework**, click **Common** &gt; **Processing group** &gt; **Execution history** &gt; **View staging data**, and then select the job that ran.</span></span>
2.  <span data-ttu-id="035ac-185">**ターゲット**をクリックします。</span><span class="sxs-lookup"><span data-stu-id="035ac-185">Click **Target**.</span></span>
3.  <span data-ttu-id="035ac-186">データが正しいことを確認します。</span><span class="sxs-lookup"><span data-stu-id="035ac-186">Verify that the data is correct.</span></span>





