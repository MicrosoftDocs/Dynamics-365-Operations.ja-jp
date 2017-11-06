--- 
title: "水平に拡張された範囲を使用して電子申告 (ER) の Excel のレポートに列を動的に追加するための形式の設計"
description: "次の手順は、システム管理者または電子レポートのロールに割り当てられたユーザーが、 OPENXML ワークシート (Excel) ファイル（要求された列が水平に展開される範囲として動的に作成される）としてのレポートを生成する電子レポート（ER）フォーマットをどのように設定するのか説明します。"
author: NickSelin
manager: AnnBe
ms.date: 10/28/2016
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: kfend
ms.search.scope: Operations
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: f827b4787506cfdec8b9a91c4a68f3293190158a
ms.openlocfilehash: 0cd1de95630d0f7c40c3b9948015892623a93686
ms.contentlocale: ja-jp
ms.lasthandoff: 09/29/2017

---
# <a name="design-a-format-to-use-horizontally-expandable-ranges-to-dynamically-add-columns-in-excel-reports-for-electronic-reporting-er"></a><span data-ttu-id="4be74-103">水平に拡張された範囲を使用して電子申告 (ER) の Excel のレポートに列を動的に追加するための形式の設計</span><span class="sxs-lookup"><span data-stu-id="4be74-103">Design a format to use horizontally-expandable ranges to dynamically add columns in Excel reports for electronic reporting (ER)</span></span>

[!include[task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="4be74-104">次の手順は、システム管理者または電子レポートのロールに割り当てられたユーザーが、 OPENXML ワークシート (Excel) ファイル（要求された列が水平に展開される範囲として動的に作成される）としてのレポートを生成する電子レポート（ER）フォーマットをどのように設定するのか説明します。</span><span class="sxs-lookup"><span data-stu-id="4be74-104">The following steps explain how a user assigned to the system administrator or electronic reporting developer role can configure an Electronic reporting (ER) format to generate reports as OPENXML worksheets (Excel) files in which the required columns can be created dynamically as horizontally expandable ranges.</span></span> <span data-ttu-id="4be74-105">これらの手順はどのタイプの企業でも実施できます。</span><span class="sxs-lookup"><span data-stu-id="4be74-105">These steps can be performed in any company.</span></span>

<span data-ttu-id="4be74-106">これらのステップを完了するには、まず次の 3 つのタスク ガイドを完了する必要があります。</span><span class="sxs-lookup"><span data-stu-id="4be74-106">To complete these steps, you must first complete these three task guides:</span></span> 

<span data-ttu-id="4be74-107">「ER コンフィギュレーション プロバイダーの作成および有効なプロバイダーとしてのマーク付け」</span><span class="sxs-lookup"><span data-stu-id="4be74-107">“ER Create a configuration provider and mark it as active”</span></span>

<span data-ttu-id="4be74-108">「ER データ ソースとしての財務分析コードの使用 (パート 1: データ モデルのデザイン)」</span><span class="sxs-lookup"><span data-stu-id="4be74-108">“ER Use financial dimensions as a data source (Part 1: Design data model)”</span></span>

<span data-ttu-id="4be74-109">「ER データ ソースとしての財務分析コードの使用 (パート 2: モデル マッピング)」</span><span class="sxs-lookup"><span data-stu-id="4be74-109">“ER Use financial dimensions as a data source (Part 2: Model mapping)”</span></span>

<span data-ttu-id="4be74-110">また、http://msdynamics.blob.core.windows.net/media/2016/09/SampleFinDimWsReport.xlsx にあるサンプル レポート付きのテンプレートのローカル コピーをダウンロードして保存する必要もあります。</span><span class="sxs-lookup"><span data-stu-id="4be74-110">You must also download and save a local copy of the template with a sample report found here: http://msdynamics.blob.core.windows.net/media/2016/09/SampleFinDimWsReport.xlsx</span></span>

<span data-ttu-id="4be74-111">この手順は、Dynamics 365 for Operations、バージョン 1611 に追加された機能です。</span><span class="sxs-lookup"><span data-stu-id="4be74-111">This procedure is for a feature that was added in Dynamics 365 for Operations version 1611.</span></span>


## <a name="create-a-new-report-configuration"></a><span data-ttu-id="4be74-112">新しいレポート設定を作成する</span><span class="sxs-lookup"><span data-stu-id="4be74-112">Create a new report configuration</span></span>
1. <span data-ttu-id="4be74-113">[組織管理] > [電子申告] > [コンフィギュレーション] に移動します。</span><span class="sxs-lookup"><span data-stu-id="4be74-113">Go to Organization administration > Electronic reporting > Configurations.</span></span>
2. <span data-ttu-id="4be74-114">[ツリー] フィールドで、「財務分析コード・サンプル モデル」を選択します。</span><span class="sxs-lookup"><span data-stu-id="4be74-114">In the tree, select 'Financial dimensions sample model'.</span></span>
3. <span data-ttu-id="4be74-115">[コンフィギュレーションの作成] をクリックすると、ドロップ ダイアログが開きます。</span><span class="sxs-lookup"><span data-stu-id="4be74-115">Click Create configuration to open the drop dialog.</span></span>
4. <span data-ttu-id="4be74-116">[新規] フィールドで、「財務分析コード・サンプルモデルに基づくフォーマット」を入力します。</span><span class="sxs-lookup"><span data-stu-id="4be74-116">In the New field, enter 'Format based on data model Financial dimensions sample model'.</span></span>
    * <span data-ttu-id="4be74-117">新規レポートのデータ ソースとして事前に作成されたモデルを使用します。</span><span class="sxs-lookup"><span data-stu-id="4be74-117">Use the model created in advance as the data source for your new report.</span></span>  
5. <span data-ttu-id="4be74-118">[名称] フィールドで、「水平に展開可能な範囲でのサンプルレポート」を入力します。</span><span class="sxs-lookup"><span data-stu-id="4be74-118">In the Name field, type 'Sample report with horizontally expandable ranges'.</span></span>
    * <span data-ttu-id="4be74-119">水平に展開可能な範囲でレポートを試します。</span><span class="sxs-lookup"><span data-stu-id="4be74-119">Sample report with horizontally expandable ranges</span></span>  
6. <span data-ttu-id="4be74-120">[説明] フィールドで、「列を動的に追加するExcelを出力」を入力します。</span><span class="sxs-lookup"><span data-stu-id="4be74-120">In the Description field, type 'To make Excel output with dynamically adding columns'.</span></span>
    * <span data-ttu-id="4be74-121">動的に列を追加するExcelを出力</span><span class="sxs-lookup"><span data-stu-id="4be74-121">To make Excel output with dynamically adding columns</span></span>  
7. <span data-ttu-id="4be74-122">[データモデル定義] フィールドで、「エントリ」を選択します。</span><span class="sxs-lookup"><span data-stu-id="4be74-122">In the Data model definition field, select Entry.</span></span>
8. <span data-ttu-id="4be74-123">[コンフィギュレーションの作成] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="4be74-123">Click Create configuration.</span></span>

## <a name="design-the-report-format"></a><span data-ttu-id="4be74-124">レポートフォーマットを デザインする</span><span class="sxs-lookup"><span data-stu-id="4be74-124">Design the report format</span></span>
1. <span data-ttu-id="4be74-125">[デザイナー] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="4be74-125">Click Designer.</span></span>
2. <span data-ttu-id="4be74-126">[詳細を表示] トグルボタンをオンします。</span><span class="sxs-lookup"><span data-stu-id="4be74-126">Turn on the ‘Show details’ toggle button.</span></span>
3. <span data-ttu-id="4be74-127">アクション ウィンドウで、[インポート] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="4be74-127">On the Action Pane, click Import.</span></span>
4. <span data-ttu-id="4be74-128">[Excel からインポート] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="4be74-128">Click Import from Excel.</span></span>
5. <span data-ttu-id="4be74-129">[添付ファイル] クリックします。</span><span class="sxs-lookup"><span data-stu-id="4be74-129">Click Attachments.</span></span>
    * <span data-ttu-id="4be74-130">レポートの テンプレートをインポートします。</span><span class="sxs-lookup"><span data-stu-id="4be74-130">Import the report’s template.</span></span> <span data-ttu-id="4be74-131">そのためにダウンロードしたExcelファイルを使用します。</span><span class="sxs-lookup"><span data-stu-id="4be74-131">Use Excel file that you downloaded for that.</span></span>  
6. <span data-ttu-id="4be74-132">[新規] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="4be74-132">Click New.</span></span>
7. <span data-ttu-id="4be74-133">[ファイル] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="4be74-133">Click File.</span></span>
8. <span data-ttu-id="4be74-134">ページを閉じます。</span><span class="sxs-lookup"><span data-stu-id="4be74-134">Close the page.</span></span>
9. <span data-ttu-id="4be74-135">[テンプレート] フィールドで、値を入力または選択します。</span><span class="sxs-lookup"><span data-stu-id="4be74-135">In the Template field, enter or select a value.</span></span>
    * <span data-ttu-id="4be74-136">ダウンロードしたテンプレートを選択します。</span><span class="sxs-lookup"><span data-stu-id="4be74-136">Select the downloaded template.</span></span>  
10. <span data-ttu-id="4be74-137">[OK] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="4be74-137">Click OK.</span></span>
    * <span data-ttu-id="4be74-138">財務分析コードで（ユーザーダイアログ形式）選択した可能な限りの列を有するExcel出力を動的に作成するには新しい範囲を加えます。</span><span class="sxs-lookup"><span data-stu-id="4be74-138">Add a new range to dynamically create Excel output with as many columns as you selected (in the user dialog form) for financial dimensions.</span></span> <span data-ttu-id="4be74-139">各列のセルは単一の財務分析コードの名称を表します。</span><span class="sxs-lookup"><span data-stu-id="4be74-139">Each cell for every column will represent a single financial dimension’s name.</span></span>  
11. <span data-ttu-id="4be74-140">[追加] をクリックしてドロップ ダイアログを開きます。</span><span class="sxs-lookup"><span data-stu-id="4be74-140">Click Add to open the drop dialog.</span></span>
12. <span data-ttu-id="4be74-141">ツリーで、[Excel\Range] を選択します。</span><span class="sxs-lookup"><span data-stu-id="4be74-141">In the tree, select 'Excel\Range'.</span></span>
13. <span data-ttu-id="4be74-142">[Excelの範囲] フィールドで、「DimNames 」を入力します。</span><span class="sxs-lookup"><span data-stu-id="4be74-142">In the Excel range field, type 'DimNames'.</span></span>
    * <span data-ttu-id="4be74-143">DimNames</span><span class="sxs-lookup"><span data-stu-id="4be74-143">DimNames</span></span>  
14. <span data-ttu-id="4be74-144">[レプリケーション方向] フィールドで、「水平」を選択します。</span><span class="sxs-lookup"><span data-stu-id="4be74-144">In the Replication direction field, select 'Horizontal'.</span></span>
15. <span data-ttu-id="4be74-145">[OK] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="4be74-145">Click OK.</span></span>
16. <span data-ttu-id="4be74-146">ツリーで、「Excel = "SampleFinDimWsReport"\Range<DimNames>: Horizontal」を選択します。</span><span class="sxs-lookup"><span data-stu-id="4be74-146">In the tree, select 'Excel = "SampleFinDimWsReport"\Range<DimNames>: Horizontal'.</span></span>
17. <span data-ttu-id="4be74-147">[上へ移動] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="4be74-147">Click Move up.</span></span>
18. <span data-ttu-id="4be74-148">ツリーで、「Excel = "SampleFinDimWsReport"\Cell<DimNames>」を選択します。</span><span class="sxs-lookup"><span data-stu-id="4be74-148">In the tree, select 'Excel = "SampleFinDimWsReport"\Cell<DimNames>'.</span></span>
19. <span data-ttu-id="4be74-149">[カット] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="4be74-149">Click Cut.</span></span>
20. <span data-ttu-id="4be74-150">ツリーで、「Excel = "SampleFinDimWsReport"\Range<DimNames>: Horizontal」を選択します。</span><span class="sxs-lookup"><span data-stu-id="4be74-150">In the tree, select 'Excel = "SampleFinDimWsReport"\Range<DimNames>: Horizontal'.</span></span>
21. <span data-ttu-id="4be74-151">[ペースト] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="4be74-151">Click Paste.</span></span>
22. <span data-ttu-id="4be74-152">ツリーで、「Excel = "SampleFinDimWsReport"\Range<DimNames>: Horizontal」を展開します。</span><span class="sxs-lookup"><span data-stu-id="4be74-152">In the tree, expand 'Excel = "SampleFinDimWsReport"\Range<DimNames>: Horizontal'.</span></span>
23. <span data-ttu-id="4be74-153">ツリーで、「Excel = "SampleFinDimWsReport"\Range<JournalLine>: Vertical」を展開します。</span><span class="sxs-lookup"><span data-stu-id="4be74-153">In the tree, expand 'Excel = "SampleFinDimWsReport"\Range<JournalLine>: Vertical'.</span></span>
24. <span data-ttu-id="4be74-154">ツリーで、「Excel = "SampleFinDimWsReport"\Range<JournalLine>: Vertical\Range<TransactionLine>: Vertical」を展開します。</span><span class="sxs-lookup"><span data-stu-id="4be74-154">In the tree, expand 'Excel = "SampleFinDimWsReport"\Range<JournalLine>: Vertical\Range<TransactionLine>: Vertical'.</span></span>
25. <span data-ttu-id="4be74-155">ツリーで、「Excel = "SampleFinDimWsReport"\Range<JournalLine>: Vertical\Range<TransactionLine>: Vertical」を選択します。</span><span class="sxs-lookup"><span data-stu-id="4be74-155">In the tree, select 'Excel = "SampleFinDimWsReport"\Range<JournalLine>: Vertical\Range<TransactionLine>: Vertical'.</span></span>
    * <span data-ttu-id="4be74-156">財務分析コードで（ユーザーダイアログ形式）選択した可能な限りの列を有するExcel出力を動的に作成するには新しい範囲を加えます。</span><span class="sxs-lookup"><span data-stu-id="4be74-156">Add a new range to dynamically create Excel output with as many columns as you selected (in the user dialog form) for financial dimensions.</span></span> <span data-ttu-id="4be74-157">各列のセルは、各報告トランザクションの単一の財務分析コードの値を表します。</span><span class="sxs-lookup"><span data-stu-id="4be74-157">Each cell for every column will represent a single financial dimension’s value for each reporting transaction.</span></span>  
26. <span data-ttu-id="4be74-158">[範囲を追加] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="4be74-158">Click Add Range.</span></span>
27. <span data-ttu-id="4be74-159">[Excelの範囲] フィールドで、「DimValues」を入力します。</span><span class="sxs-lookup"><span data-stu-id="4be74-159">In the Excel range field, type 'DimValues'.</span></span>
    * <span data-ttu-id="4be74-160">DimValues</span><span class="sxs-lookup"><span data-stu-id="4be74-160">DimValues</span></span>  
28. <span data-ttu-id="4be74-161">[レプリケーション方向] フィールドで、「水平」を選択します。</span><span class="sxs-lookup"><span data-stu-id="4be74-161">In the Replication direction field, select 'Horizontal'.</span></span>
29. <span data-ttu-id="4be74-162">[OK] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="4be74-162">Click OK.</span></span>
30. <span data-ttu-id="4be74-163">ツリーで、「Excel = "SampleFinDimWsReport"\Range<JournalLine>: Vertical\Range<TransactionLine>: Vertical\Cell<DimValues>」を選択します。</span><span class="sxs-lookup"><span data-stu-id="4be74-163">In the tree, select 'Excel = "SampleFinDimWsReport"\Range<JournalLine>: Vertical\Range<TransactionLine>: Vertical\Cell<DimValues>'.</span></span>
31. <span data-ttu-id="4be74-164">[カット] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="4be74-164">Click Cut.</span></span>
32. <span data-ttu-id="4be74-165">ツリーで、「Excel = "SampleFinDimWsReport"\Range<JournalLine>: Vertical\Range<TransactionLine>: Vertical\Range<DimValues>: Horizontal」を選択します。</span><span class="sxs-lookup"><span data-stu-id="4be74-165">In the tree, select 'Excel = "SampleFinDimWsReport"\Range<JournalLine>: Vertical\Range<TransactionLine>: Vertical\Range<DimValues>: Horizontal'.</span></span>
33. <span data-ttu-id="4be74-166">[ペースト] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="4be74-166">Click Paste.</span></span>
34. <span data-ttu-id="4be74-167">ツリーで、「Excel = "SampleFinDimWsReport"\Range<JournalLine>: Vertical\Range<TransactionLine>: Vertical\Range<DimValues>: Horizontal」を展開します。</span><span class="sxs-lookup"><span data-stu-id="4be74-167">In the tree, expand 'Excel = "SampleFinDimWsReport"\Range<JournalLine>: Vertical\Range<TransactionLine>: Vertical\Range<DimValues>: Horizontal'.</span></span>

## <a name="map-format-elements-to-data-sources"></a><span data-ttu-id="4be74-168">フォーマットエレメントをデータソースにマッピングする</span><span class="sxs-lookup"><span data-stu-id="4be74-168">Map format elements to data sources</span></span>
1. <span data-ttu-id="4be74-169">[マッピング] タブをクリックします。</span><span class="sxs-lookup"><span data-stu-id="4be74-169">Click the Mapping tab.</span></span>
2. <span data-ttu-id="4be74-170">ツリーで、「model: Data model Financial dimensions sample model」を展開します。</span><span class="sxs-lookup"><span data-stu-id="4be74-170">In the tree, expand 'model: Data model Financial dimensions sample model'.</span></span>
3. <span data-ttu-id="4be74-171">ツリーで、「model: Data model Financial dimensions sample model\Journal: Record list」を展開します。</span><span class="sxs-lookup"><span data-stu-id="4be74-171">In the tree, expand 'model: Data model Financial dimensions sample model\Journal: Record list'.</span></span>
4. <span data-ttu-id="4be74-172">ツリーで、「model: Data model Financial dimensions sample model\Journal: Record list\Transaction: Record list」を展開します。</span><span class="sxs-lookup"><span data-stu-id="4be74-172">In the tree, expand 'model: Data model Financial dimensions sample model\Journal: Record list\Transaction: Record list'.</span></span>
5. <span data-ttu-id="4be74-173">ツリーで、「model: Data model Financial dimensions sample model\Journal: Record list\Transaction: Record list\Dimensions data: Record list」を展開します。</span><span class="sxs-lookup"><span data-stu-id="4be74-173">In the tree, expand 'model: Data model Financial dimensions sample model\Journal: Record list\Transaction: Record list\Dimensions data: Record list'.</span></span>
6. <span data-ttu-id="4be74-174">ツリーで、「Excel = "SampleFinDimWsReport"\Range<JournalLine>: Vertical\Range<TransactionLine>: Vertical\Range<DimValues>: Horizontal\Cell<DimValues>」を選択します。</span><span class="sxs-lookup"><span data-stu-id="4be74-174">In the tree, select 'Excel = "SampleFinDimWsReport"\Range<JournalLine>: Vertical\Range<TransactionLine>: Vertical\Range<DimValues>: Horizontal\Cell<DimValues>'.</span></span>
7. <span data-ttu-id="4be74-175">ツリーで、「model: Data model Financial dimensions sample model\Journal: Record list\Transaction: Record list\Dimensions data: Record listt\Code: String」を選択します。</span><span class="sxs-lookup"><span data-stu-id="4be74-175">In the tree, select 'model: Data model Financial dimensions sample model\Journal: Record list\Transaction: Record list\Dimensions data: Record list\Code: String'.</span></span>
8. <span data-ttu-id="4be74-176">[バインド] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="4be74-176">Click Bind.</span></span>
9. <span data-ttu-id="4be74-177">ツリーで、「Excel = "SampleFinDimWsReport"\Range<JournalLine>: Vertical\Range<TransactionLine>: Vertical\Range<DimValues>: Horizontal」を選択します。</span><span class="sxs-lookup"><span data-stu-id="4be74-177">In the tree, select 'Excel = "SampleFinDimWsReport"\Range<JournalLine>: Vertical\Range<TransactionLine>: Vertical\Range<DimValues>: Horizontal'.</span></span>
10. <span data-ttu-id="4be74-178">ツリーで、「model: Data model Financial dimensions sample model\Journal: Record list\Transaction: Record list\Dimensions data: Record list」を展開します。</span><span class="sxs-lookup"><span data-stu-id="4be74-178">In the tree, select 'model: Data model Financial dimensions sample model\Journal: Record list\Transaction: Record list\Dimensions data: Record list'.</span></span>
11. <span data-ttu-id="4be74-179">[バインド] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="4be74-179">Click Bind.</span></span>
12. <span data-ttu-id="4be74-180">ツリーで、「Excel = "SampleFinDimWsReport"\Range<JournalLine>: Vertical\Range<TransactionLine>: Vertical\Cell<Credit>」を選択します。</span><span class="sxs-lookup"><span data-stu-id="4be74-180">In the tree, select 'Excel = "SampleFinDimWsReport"\Range<JournalLine>: Vertical\Range<TransactionLine>: Vertical\Cell<Credit>'.</span></span>
13. <span data-ttu-id="4be74-181">ツリーで、「model: Data model Financial dimensions sample model\Journal: Record list\Transaction: Record list\Credit: Real」を選択します。</span><span class="sxs-lookup"><span data-stu-id="4be74-181">In the tree, select 'model: Data model Financial dimensions sample model\Journal: Record list\Transaction: Record list\Credit: Real'.</span></span>
14. <span data-ttu-id="4be74-182">[バインド] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="4be74-182">Click Bind.</span></span>
15. <span data-ttu-id="4be74-183">ツリーで、「Excel = "SampleFinDimWsReport"\Range<JournalLine>: Vertical\Range<TransactionLine>: Vertical\Cell<Debit>」を選択します。</span><span class="sxs-lookup"><span data-stu-id="4be74-183">In the tree, select 'Excel = "SampleFinDimWsReport"\Range<JournalLine>: Vertical\Range<TransactionLine>: Vertical\Cell<Debit>'.</span></span>
16. <span data-ttu-id="4be74-184">ツリーで、「model: Data model Financial dimensions sample model\Journal: Record list\Transaction: Record list\Debit: Real」を選択します。</span><span class="sxs-lookup"><span data-stu-id="4be74-184">In the tree, select 'model: Data model Financial dimensions sample model\Journal: Record list\Transaction: Record list\Debit: Real'.</span></span>
17. <span data-ttu-id="4be74-185">[バインド] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="4be74-185">Click Bind.</span></span>
18. <span data-ttu-id="4be74-186">ツリーで、「Excel = "SampleFinDimWsReport"\Range<JournalLine>: Vertical\Range<TransactionLine>: Vertical\Cell<Currency>」を選択します。</span><span class="sxs-lookup"><span data-stu-id="4be74-186">In the tree, select 'Excel = "SampleFinDimWsReport"\Range<JournalLine>: Vertical\Range<TransactionLine>: Vertical\Cell<Currency>'.</span></span>
19. <span data-ttu-id="4be74-187">ツリーで、「model: Data model Financial dimensions sample model\Journal: Record list\Transaction: Record list\Currency: String」を選択します。</span><span class="sxs-lookup"><span data-stu-id="4be74-187">In the tree, select 'model: Data model Financial dimensions sample model\Journal: Record list\Transaction: Record list\Currency: String'.</span></span>
20. <span data-ttu-id="4be74-188">[バインド] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="4be74-188">Click Bind.</span></span>
21. <span data-ttu-id="4be74-189">ツリーで、「Excel = "SampleFinDimWsReport"\Range<JournalLine>: Vertical\Range<TransactionLine>: Vertical\Cell<TransDate>」を選択します。</span><span class="sxs-lookup"><span data-stu-id="4be74-189">In the tree, select 'Excel = "SampleFinDimWsReport"\Range<JournalLine>: Vertical\Range<TransactionLine>: Vertical\Cell<TransDate>'.</span></span>
22. <span data-ttu-id="4be74-190">ツリーで、「model: Data model Financial dimensions sample model\Journal: Record list\Transaction: Record list\Date: Date」を選択します。</span><span class="sxs-lookup"><span data-stu-id="4be74-190">In the tree, select 'model: Data model Financial dimensions sample model\Journal: Record list\Transaction: Record list\Date: Date'.</span></span>
23. <span data-ttu-id="4be74-191">[バインド] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="4be74-191">Click Bind.</span></span>
24. <span data-ttu-id="4be74-192">ツリーで、「Excel = "SampleFinDimWsReport"\Range<JournalLine>: Vertical\Range<TransactionLine>: Vertical\Cell<TransVoucher>」を選択します。</span><span class="sxs-lookup"><span data-stu-id="4be74-192">In the tree, select 'Excel = "SampleFinDimWsReport"\Range<JournalLine>: Vertical\Range<TransactionLine>: Vertical\Cell<TransVoucher>'.</span></span>
25. <span data-ttu-id="4be74-193">ツリーで、「model: Data model Financial dimensions sample model\Journal: Record list\Transaction: Record list\Currency: String」を選択します。</span><span class="sxs-lookup"><span data-stu-id="4be74-193">In the tree, select 'model: Data model Financial dimensions sample model\Journal: Record list\Transaction: Record list\Voucher: String'.</span></span>
26. <span data-ttu-id="4be74-194">[バインド] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="4be74-194">Click Bind.</span></span>
27. <span data-ttu-id="4be74-195">ツリーで、「Excel = "SampleFinDimWsReport"\Range<JournalLine>: Vertical\Range<TransactionLine>: Vertical\Cell<TransBatch>」を選択します。</span><span class="sxs-lookup"><span data-stu-id="4be74-195">In the tree, select 'Excel = "SampleFinDimWsReport"\Range<JournalLine>: Vertical\Range<TransactionLine>: Vertical\Cell<TransBatch>'.</span></span>
28. <span data-ttu-id="4be74-196">ツリーで、「model: Data model Financial dimensions sample model\Journal: Record list\Batch: String」を選択します。</span><span class="sxs-lookup"><span data-stu-id="4be74-196">In the tree, select 'model: Data model Financial dimensions sample model\Journal: Record list\Batch: String'.</span></span>
29. <span data-ttu-id="4be74-197">[バインド] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="4be74-197">Click Bind.</span></span>
30. <span data-ttu-id="4be74-198">ツリーで、「Excel = "SampleFinDimWsReport"\Range<JournalLine>: Vertical\Range<TransactionLine>: Vertical」を選択します。</span><span class="sxs-lookup"><span data-stu-id="4be74-198">In the tree, select 'Excel = "SampleFinDimWsReport"\Range<JournalLine>: Vertical\Range<TransactionLine>: Vertical'.</span></span>
31. <span data-ttu-id="4be74-199">ツリーで、「model: Data model Financial dimensions sample model\Journal: Record list\Transaction: Record list」を選択します。</span><span class="sxs-lookup"><span data-stu-id="4be74-199">In the tree, select 'model: Data model Financial dimensions sample model\Journal: Record list\Transaction: Record list'.</span></span>
32. <span data-ttu-id="4be74-200">[バインド] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="4be74-200">Click Bind.</span></span>
33. <span data-ttu-id="4be74-201">ツリーで、「Excel = "SampleFinDimWsReport"\Range<JournalLine>: Vertical\Cell<Batch>」を選択します。</span><span class="sxs-lookup"><span data-stu-id="4be74-201">In the tree, select 'Excel = "SampleFinDimWsReport"\Range<JournalLine>: Vertical\Cell<Batch>'.</span></span>
34. <span data-ttu-id="4be74-202">ツリーで、「model: Data model Financial dimensions sample model\Journal: Record list\Batch: String」を選択します。</span><span class="sxs-lookup"><span data-stu-id="4be74-202">In the tree, select 'model: Data model Financial dimensions sample model\Journal: Record list\Batch: String'.</span></span>
35. <span data-ttu-id="4be74-203">[バインド] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="4be74-203">Click Bind.</span></span>
36. <span data-ttu-id="4be74-204">ツリーで、「Excel = "SampleFinDimWsReport"\Range<JournalLine>: Vertical」を選択します。</span><span class="sxs-lookup"><span data-stu-id="4be74-204">In the tree, select 'Excel = "SampleFinDimWsReport"\Range<JournalLine>: Vertical'.</span></span>
37. <span data-ttu-id="4be74-205">ツリーで、「model: Data model Financial dimensions sample model\Journal: Record list」を選択します。</span><span class="sxs-lookup"><span data-stu-id="4be74-205">In the tree, select 'model: Data model Financial dimensions sample model\Journal: Record list'.</span></span>
38. <span data-ttu-id="4be74-206">[バインド] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="4be74-206">Click Bind.</span></span>
39. <span data-ttu-id="4be74-207">ツリーで、「model: Data model Financial dimensions sample model\Dimensions setting: Record list」を展開します。</span><span class="sxs-lookup"><span data-stu-id="4be74-207">In the tree, expand 'model: Data model Financial dimensions sample model\Dimensions setting: Record list'.</span></span>
40. <span data-ttu-id="4be74-208">ツリーで、「model: Data model Financial dimensions sample model\Dimensions setting: Record list\Code: String」を選択します。</span><span class="sxs-lookup"><span data-stu-id="4be74-208">In the tree, select 'model: Data model Financial dimensions sample model\Dimensions setting: Record list\Code: String'.</span></span>
41. <span data-ttu-id="4be74-209">ツリーで、「Excel = "SampleFinDimWsReport"\Range<DimNames>: Horizontal\Cell<DimNames>」を選択します。</span><span class="sxs-lookup"><span data-stu-id="4be74-209">In the tree, select 'Excel = "SampleFinDimWsReport"\Range<DimNames>: Horizontal\Cell<DimNames>'.</span></span>
42. <span data-ttu-id="4be74-210">[バインド] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="4be74-210">Click Bind.</span></span>
43. <span data-ttu-id="4be74-211">ツリーで、「model: Data model Financial dimensions sample model\Dimensions setting: Record list」を選択します。</span><span class="sxs-lookup"><span data-stu-id="4be74-211">In the tree, select 'model: Data model Financial dimensions sample model\Dimensions setting: Record list'.</span></span>
44. <span data-ttu-id="4be74-212">ツリーで、「Excel = "SampleFinDimWsReport"\Range<DimNames>: Horizontal」を選択します。</span><span class="sxs-lookup"><span data-stu-id="4be74-212">In the tree, select 'Excel = "SampleFinDimWsReport"\Range<DimNames>: Horizontal'.</span></span>
45. <span data-ttu-id="4be74-213">[バインド] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="4be74-213">Click Bind.</span></span>
46. <span data-ttu-id="4be74-214">ツリーで、「Excel = "SampleFinDimWsReport"\Cell<CompanyName>」を選択します。</span><span class="sxs-lookup"><span data-stu-id="4be74-214">In the tree, select 'Excel = "SampleFinDimWsReport"\Cell<CompanyName>'.</span></span>
47. <span data-ttu-id="4be74-215">ツリーで、「model: Data model Financial dimensions sample model\Company: String」を選択します。</span><span class="sxs-lookup"><span data-stu-id="4be74-215">In the tree, select 'model: Data model Financial dimensions sample model\Company: String'.</span></span>
48. <span data-ttu-id="4be74-216">[バインド] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="4be74-216">Click Bind.</span></span>
49. <span data-ttu-id="4be74-217">[保存] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="4be74-217">Click Save.</span></span>
50. <span data-ttu-id="4be74-218">ページを閉じます。</span><span class="sxs-lookup"><span data-stu-id="4be74-218">Close the page.</span></span>

