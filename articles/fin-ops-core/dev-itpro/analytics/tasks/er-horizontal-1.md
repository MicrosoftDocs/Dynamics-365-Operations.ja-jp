---
title: ER 水平に拡張された範囲を使用して Excel のレポートに列を動的に追加する (第 1 部 - デザイン形式)
description: このトピックでは、OPENXML ワークシート (Excel) ファイルとしてレポートを生成するように電子申告 (ER) 形式を構成する方法について説明します。 (第 1 部)
author: NickSelin
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: ERSolutionTable, ERSolutionCreateDropDialog, EROperationDesigner, ERComponentTypeDropDialog
audience: Application User
ms.reviewer: kfend
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: a5119255b119a99f3809d2d75bbfdc7b3bad9932
ms.sourcegitcommit: 6cb174d1ec8b55946dca4db03d6a3c3f4c6fa2df
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 03/09/2021
ms.locfileid: "5569560"
---
# <a name="er-use-horizontally-expandable-ranges-to-dynamically-add-columns-in-excel-reports-part-1---design-format"></a><span data-ttu-id="28cca-104">ER 水平に拡張された範囲を使用して Excel のレポートに列を動的に追加する (第 1 部 - デザイン形式)</span><span class="sxs-lookup"><span data-stu-id="28cca-104">ER Use horizontally expandable ranges to dynamically add columns in Excel reports (Part 1 - Design format)</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="28cca-105">次の手順は、システム管理者または電子レポートのロールに割り当てられたユーザーが、 OPENXML ワークシート (Excel) ファイル（要求された列が水平に展開される範囲として動的に作成される）としてのレポートを生成する電子レポート（ER）フォーマットをどのように設定するのか説明します。</span><span class="sxs-lookup"><span data-stu-id="28cca-105">The following steps explain how a user assigned to the system administrator or electronic reporting developer role can configure an Electronic reporting (ER) format to generate reports as OPENXML worksheets (Excel) files in which the required columns can be created dynamically as horizontally expandable ranges.</span></span> <span data-ttu-id="28cca-106">これらの手順はどのタイプの企業でも実施できます。</span><span class="sxs-lookup"><span data-stu-id="28cca-106">These steps can be performed in any company.</span></span>

<span data-ttu-id="28cca-107">これらのステップを完了するには、まず次の 3 つのタスク ガイドを完了する必要があります。</span><span class="sxs-lookup"><span data-stu-id="28cca-107">To complete these steps, you must first complete these three task guides:</span></span> 

<span data-ttu-id="28cca-108">ER 構成プロバイダーを作成し、アクティブとしてマークする</span><span class="sxs-lookup"><span data-stu-id="28cca-108">"ER Create a configuration provider and mark it as active"</span></span>

<span data-ttu-id="28cca-109">ER 財務分析コードをデータ ソースとして使用する（第 1 部：データ モデルのデザイン）</span><span class="sxs-lookup"><span data-stu-id="28cca-109">"ER Use financial dimensions as a data source (Part 1: Design data model)"</span></span>

<span data-ttu-id="28cca-110">ER 財務分析コードをデータ ソースとして使用する（第 2 部：モデル マッピング）</span><span class="sxs-lookup"><span data-stu-id="28cca-110">"ER Use financial dimensions as a data source (Part 2: Model mapping)"</span></span>

<span data-ttu-id="28cca-111">[財務分析コードのサンプル Web サービス レポート](https://go.microsoft.com/fwlink/?linkid=862266) にあるサンプル レポートで、テンプレートのローカル コピーをダウンロードし、保存する必要があります。</span><span class="sxs-lookup"><span data-stu-id="28cca-111">You must also download and save a local copy of the template with a sample report found here, [Sample Financial Dimensions Web Service Report](https://go.microsoft.com/fwlink/?linkid=862266).</span></span>

<span data-ttu-id="28cca-112">この手順は Dynamics 365 for Operations バージョン 1611 に追加された機能です。</span><span class="sxs-lookup"><span data-stu-id="28cca-112">This procedure is for a feature that was added in Dynamics 365 for Operations version 1611.</span></span>


## <a name="create-a-new-report-configuration"></a><span data-ttu-id="28cca-113">新しいレポート設定を作成する</span><span class="sxs-lookup"><span data-stu-id="28cca-113">Create a new report configuration</span></span>
1. <span data-ttu-id="28cca-114">[組織管理] > [電子申告] > [コンフィギュレーション] に移動します。</span><span class="sxs-lookup"><span data-stu-id="28cca-114">Go to Organization administration > Electronic reporting > Configurations.</span></span>
2. <span data-ttu-id="28cca-115">[ツリー] フィールドで、「財務分析コード・サンプル モデル」を選択します。</span><span class="sxs-lookup"><span data-stu-id="28cca-115">In the tree, select 'Financial dimensions sample model'.</span></span>
3. <span data-ttu-id="28cca-116">[コンフィギュレーションの作成] をクリックすると、ドロップ ダイアログが開きます。</span><span class="sxs-lookup"><span data-stu-id="28cca-116">Click Create configuration to open the drop dialog.</span></span>
4. <span data-ttu-id="28cca-117">[新規] フィールドで、「財務分析コード・サンプルモデルに基づくフォーマット」を入力します。</span><span class="sxs-lookup"><span data-stu-id="28cca-117">In the New field, enter 'Format based on data model Financial dimensions sample model'.</span></span>
    * <span data-ttu-id="28cca-118">新規レポートのデータ ソースとして事前に作成されたモデルを使用します。</span><span class="sxs-lookup"><span data-stu-id="28cca-118">Use the model created in advance as the data source for your new report.</span></span>  
5. <span data-ttu-id="28cca-119">[名称] フィールドで、「水平に展開可能な範囲でのサンプルレポート」を入力します。</span><span class="sxs-lookup"><span data-stu-id="28cca-119">In the Name field, type 'Sample report with horizontally expandable ranges'.</span></span>
    * <span data-ttu-id="28cca-120">水平に展開可能な範囲でレポートを試します。</span><span class="sxs-lookup"><span data-stu-id="28cca-120">Sample report with horizontally expandable ranges</span></span>  
6. <span data-ttu-id="28cca-121">[説明] フィールドで、「列を動的に追加するExcelを出力」を入力します。</span><span class="sxs-lookup"><span data-stu-id="28cca-121">In the Description field, type 'To make Excel output with dynamically adding columns'.</span></span>
    * <span data-ttu-id="28cca-122">動的に列を追加するExcelを出力</span><span class="sxs-lookup"><span data-stu-id="28cca-122">To make Excel output with dynamically adding columns</span></span>  
7. <span data-ttu-id="28cca-123">[データモデル定義] フィールドで、「エントリ」を選択します。</span><span class="sxs-lookup"><span data-stu-id="28cca-123">In the Data model definition field, select Entry.</span></span>
8. <span data-ttu-id="28cca-124">[コンフィギュレーションの作成] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="28cca-124">Click Create configuration.</span></span>

## <a name="design-the-report-format"></a><span data-ttu-id="28cca-125">レポートフォーマットを デザインする</span><span class="sxs-lookup"><span data-stu-id="28cca-125">Design the report format</span></span>
1. <span data-ttu-id="28cca-126">[デザイナー] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="28cca-126">Click Designer.</span></span>
2. <span data-ttu-id="28cca-127">[詳細を表示] トグル ボタンをオンにします。</span><span class="sxs-lookup"><span data-stu-id="28cca-127">Turn on the 'Show details' toggle button.</span></span>
3. <span data-ttu-id="28cca-128">アクション ウィンドウで、[インポート] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="28cca-128">On the Action Pane, click Import.</span></span>
4. <span data-ttu-id="28cca-129">[Excel からインポート] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="28cca-129">Click Import from Excel.</span></span>
5. <span data-ttu-id="28cca-130">[添付ファイル] クリックします。</span><span class="sxs-lookup"><span data-stu-id="28cca-130">Click Attachments.</span></span>
    * <span data-ttu-id="28cca-131">レポートの テンプレートをインポートします。</span><span class="sxs-lookup"><span data-stu-id="28cca-131">Import the report's template.</span></span> <span data-ttu-id="28cca-132">そのためにダウンロードしたExcelファイルを使用します。</span><span class="sxs-lookup"><span data-stu-id="28cca-132">Use Excel file that you downloaded for that.</span></span>  
6. <span data-ttu-id="28cca-133">[新規] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="28cca-133">Click New.</span></span>
7. <span data-ttu-id="28cca-134">[ファイル] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="28cca-134">Click File.</span></span>
8. <span data-ttu-id="28cca-135">ページを閉じます。</span><span class="sxs-lookup"><span data-stu-id="28cca-135">Close the page.</span></span>
9. <span data-ttu-id="28cca-136">[テンプレート] フィールドで、値を入力または選択します。</span><span class="sxs-lookup"><span data-stu-id="28cca-136">In the Template field, enter or select a value.</span></span>
    * <span data-ttu-id="28cca-137">ダウンロードしたテンプレートを選択します。</span><span class="sxs-lookup"><span data-stu-id="28cca-137">Select the downloaded template.</span></span>  
10. <span data-ttu-id="28cca-138">[OK] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="28cca-138">Click OK.</span></span>
    * <span data-ttu-id="28cca-139">財務分析コードで（ユーザーダイアログ形式）選択した可能な限りの列を有するExcel出力を動的に作成するには新しい範囲を加えます。</span><span class="sxs-lookup"><span data-stu-id="28cca-139">Add a new range to dynamically create Excel output with as many columns as you selected (in the user dialog form) for financial dimensions.</span></span> <span data-ttu-id="28cca-140">それぞれの列のセルは単一の財務分析コードの名称を表します。</span><span class="sxs-lookup"><span data-stu-id="28cca-140">Each cell for every column will represent a single financial dimension's name.</span></span>  
11. <span data-ttu-id="28cca-141">[追加] をクリックしてドロップ ダイアログを開きます。</span><span class="sxs-lookup"><span data-stu-id="28cca-141">Click Add to open the drop dialog.</span></span>
12. <span data-ttu-id="28cca-142">ツリーで、[Excel\Range] を選択します。</span><span class="sxs-lookup"><span data-stu-id="28cca-142">In the tree, select 'Excel\Range'.</span></span>
13. <span data-ttu-id="28cca-143">[Excelの範囲] フィールドで、「DimNames 」を入力します。</span><span class="sxs-lookup"><span data-stu-id="28cca-143">In the Excel range field, type 'DimNames'.</span></span>
    * <span data-ttu-id="28cca-144">DimNames</span><span class="sxs-lookup"><span data-stu-id="28cca-144">DimNames</span></span>  
14. <span data-ttu-id="28cca-145">[レプリケーション方向] フィールドで、「水平」を選択します。</span><span class="sxs-lookup"><span data-stu-id="28cca-145">In the Replication direction field, select 'Horizontal'.</span></span>
15. <span data-ttu-id="28cca-146">[OK] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="28cca-146">Click OK.</span></span>
16. <span data-ttu-id="28cca-147">ツリーで、「Excel = "SampleFinDimWsReport"\Range<DimNames>: Horizontal」を選択します。</span><span class="sxs-lookup"><span data-stu-id="28cca-147">In the tree, select 'Excel = "SampleFinDimWsReport"\Range<DimNames>: Horizontal'.</span></span>
17. <span data-ttu-id="28cca-148">[上へ移動] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="28cca-148">Click Move up.</span></span>
18. <span data-ttu-id="28cca-149">ツリーで、「Excel = "SampleFinDimWsReport"\Cell<DimNames>」を選択します。</span><span class="sxs-lookup"><span data-stu-id="28cca-149">In the tree, select 'Excel = "SampleFinDimWsReport"\Cell<DimNames>'.</span></span>
19. <span data-ttu-id="28cca-150">[カット] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="28cca-150">Click Cut.</span></span>
20. <span data-ttu-id="28cca-151">ツリーで、「Excel = "SampleFinDimWsReport"\Range<DimNames>: Horizontal」を選択します。</span><span class="sxs-lookup"><span data-stu-id="28cca-151">In the tree, select 'Excel = "SampleFinDimWsReport"\Range<DimNames>: Horizontal'.</span></span>
21. <span data-ttu-id="28cca-152">[ペースト] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="28cca-152">Click Paste.</span></span>
22. <span data-ttu-id="28cca-153">ツリーで、「Excel = "SampleFinDimWsReport"\Range<DimNames>: Horizontal」を展開します。</span><span class="sxs-lookup"><span data-stu-id="28cca-153">In the tree, expand 'Excel = "SampleFinDimWsReport"\Range<DimNames>: Horizontal'.</span></span>
23. <span data-ttu-id="28cca-154">ツリーで、「Excel = "SampleFinDimWsReport"\Range<JournalLine>: Vertical」を展開します。</span><span class="sxs-lookup"><span data-stu-id="28cca-154">In the tree, expand 'Excel = "SampleFinDimWsReport"\Range<JournalLine>: Vertical'.</span></span>
24. <span data-ttu-id="28cca-155">ツリーで、「Excel = "SampleFinDimWsReport"\Range<JournalLine>: Vertical\Range<TransactionLine>: Vertical」を展開します。</span><span class="sxs-lookup"><span data-stu-id="28cca-155">In the tree, expand 'Excel = "SampleFinDimWsReport"\Range<JournalLine>: Vertical\Range<TransactionLine>: Vertical'.</span></span>
25. <span data-ttu-id="28cca-156">ツリーで、「Excel = "SampleFinDimWsReport"\Range<JournalLine>: Vertical\Range<TransactionLine>: Vertical」を選択します。</span><span class="sxs-lookup"><span data-stu-id="28cca-156">In the tree, select 'Excel = "SampleFinDimWsReport"\Range<JournalLine>: Vertical\Range<TransactionLine>: Vertical'.</span></span>
    * <span data-ttu-id="28cca-157">財務分析コードで（ユーザーダイアログ形式）選択した可能な限りの列を有するExcel出力を動的に作成するには新しい範囲を加えます。</span><span class="sxs-lookup"><span data-stu-id="28cca-157">Add a new range to dynamically create Excel output with as many columns as you selected (in the user dialog form) for financial dimensions.</span></span> <span data-ttu-id="28cca-158">それぞれの列のセルは、各レポート トランザクションの単一の財務分析コードの値を表します。</span><span class="sxs-lookup"><span data-stu-id="28cca-158">Each cell for every column will represent a single financial dimension's value for each reporting transaction.</span></span>  
26. <span data-ttu-id="28cca-159">[範囲を追加] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="28cca-159">Click Add Range.</span></span>
27. <span data-ttu-id="28cca-160">[Excelの範囲] フィールドで、「DimValues」を入力します。</span><span class="sxs-lookup"><span data-stu-id="28cca-160">In the Excel range field, type 'DimValues'.</span></span>
    * <span data-ttu-id="28cca-161">DimValues</span><span class="sxs-lookup"><span data-stu-id="28cca-161">DimValues</span></span>  
28. <span data-ttu-id="28cca-162">[レプリケーション方向] フィールドで、「水平」を選択します。</span><span class="sxs-lookup"><span data-stu-id="28cca-162">In the Replication direction field, select 'Horizontal'.</span></span>
29. <span data-ttu-id="28cca-163">[OK] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="28cca-163">Click OK.</span></span>
30. <span data-ttu-id="28cca-164">ツリーで、「Excel = "SampleFinDimWsReport"\Range<JournalLine>: Vertical\Range<TransactionLine>: Vertical\Cell<DimValues>」を選択します。</span><span class="sxs-lookup"><span data-stu-id="28cca-164">In the tree, select 'Excel = "SampleFinDimWsReport"\Range<JournalLine>: Vertical\Range<TransactionLine>: Vertical\Cell<DimValues>'.</span></span>
31. <span data-ttu-id="28cca-165">[カット] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="28cca-165">Click Cut.</span></span>
32. <span data-ttu-id="28cca-166">ツリーで、「Excel = "SampleFinDimWsReport"\Range<JournalLine>: Vertical\Range<TransactionLine>: Vertical\Range<DimValues>: Horizontal」を選択します。</span><span class="sxs-lookup"><span data-stu-id="28cca-166">In the tree, select 'Excel = "SampleFinDimWsReport"\Range<JournalLine>: Vertical\Range<TransactionLine>: Vertical\Range<DimValues>: Horizontal'.</span></span>
33. <span data-ttu-id="28cca-167">[ペースト] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="28cca-167">Click Paste.</span></span>
34. <span data-ttu-id="28cca-168">ツリーで、「Excel = "SampleFinDimWsReport"\Range<JournalLine>: Vertical\Range<TransactionLine>: Vertical\Range<DimValues>: Horizontal」を展開します。</span><span class="sxs-lookup"><span data-stu-id="28cca-168">In the tree, expand 'Excel = "SampleFinDimWsReport"\Range<JournalLine>: Vertical\Range<TransactionLine>: Vertical\Range<DimValues>: Horizontal'.</span></span>

## <a name="map-format-elements-to-data-sources"></a><span data-ttu-id="28cca-169">フォーマットエレメントをデータソースにマッピングする</span><span class="sxs-lookup"><span data-stu-id="28cca-169">Map format elements to data sources</span></span>
1. <span data-ttu-id="28cca-170">[マッピング] タブをクリックします。</span><span class="sxs-lookup"><span data-stu-id="28cca-170">Click the Mapping tab.</span></span>
2. <span data-ttu-id="28cca-171">ツリーで、「model: Data model Financial dimensions sample model」を展開します。</span><span class="sxs-lookup"><span data-stu-id="28cca-171">In the tree, expand 'model: Data model Financial dimensions sample model'.</span></span>
3. <span data-ttu-id="28cca-172">ツリーで、「model: Data model Financial dimensions sample model\Journal: Record list」を展開します。</span><span class="sxs-lookup"><span data-stu-id="28cca-172">In the tree, expand 'model: Data model Financial dimensions sample model\Journal: Record list'.</span></span>
4. <span data-ttu-id="28cca-173">ツリーで、「model: Data model Financial dimensions sample model\Journal: Record list\Transaction: Record list」を展開します。</span><span class="sxs-lookup"><span data-stu-id="28cca-173">In the tree, expand 'model: Data model Financial dimensions sample model\Journal: Record list\Transaction: Record list'.</span></span>
5. <span data-ttu-id="28cca-174">ツリーで、「model: Data model Financial dimensions sample model\Journal: Record list\Transaction: Record list\Dimensions data: Record list」を展開します。</span><span class="sxs-lookup"><span data-stu-id="28cca-174">In the tree, expand 'model: Data model Financial dimensions sample model\Journal: Record list\Transaction: Record list\Dimensions data: Record list'.</span></span>
6. <span data-ttu-id="28cca-175">ツリーで、「Excel = "SampleFinDimWsReport"\Range<JournalLine>: Vertical\Range<TransactionLine>: Vertical\Range<DimValues>: Horizontal\Cell<DimValues>」を選択します。</span><span class="sxs-lookup"><span data-stu-id="28cca-175">In the tree, select 'Excel = "SampleFinDimWsReport"\Range<JournalLine>: Vertical\Range<TransactionLine>: Vertical\Range<DimValues>: Horizontal\Cell<DimValues>'.</span></span>
7. <span data-ttu-id="28cca-176">ツリーで、「model: Data model Financial dimensions sample model\Journal: Record list\Transaction: Record list\Dimensions data: Record listt\Code: String」を選択します。</span><span class="sxs-lookup"><span data-stu-id="28cca-176">In the tree, select 'model: Data model Financial dimensions sample model\Journal: Record list\Transaction: Record list\Dimensions data: Record list\Code: String'.</span></span>
8. <span data-ttu-id="28cca-177">[バインド] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="28cca-177">Click Bind.</span></span>
9. <span data-ttu-id="28cca-178">ツリーで、「Excel = "SampleFinDimWsReport"\Range<JournalLine>: Vertical\Range<TransactionLine>: Vertical\Range<DimValues>: Horizontal」を選択します。</span><span class="sxs-lookup"><span data-stu-id="28cca-178">In the tree, select 'Excel = "SampleFinDimWsReport"\Range<JournalLine>: Vertical\Range<TransactionLine>: Vertical\Range<DimValues>: Horizontal'.</span></span>
10. <span data-ttu-id="28cca-179">ツリーで、「model: Data model Financial dimensions sample model\Journal: Record list\Transaction: Record list\Dimensions data: Record list」を展開します。</span><span class="sxs-lookup"><span data-stu-id="28cca-179">In the tree, select 'model: Data model Financial dimensions sample model\Journal: Record list\Transaction: Record list\Dimensions data: Record list'.</span></span>
11. <span data-ttu-id="28cca-180">[バインド] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="28cca-180">Click Bind.</span></span>
12. <span data-ttu-id="28cca-181">ツリーで、「Excel = "SampleFinDimWsReport"\Range<JournalLine>: Vertical\Range<TransactionLine>: Vertical\Cell<Credit>」を選択します。</span><span class="sxs-lookup"><span data-stu-id="28cca-181">In the tree, select 'Excel = "SampleFinDimWsReport"\Range<JournalLine>: Vertical\Range<TransactionLine>: Vertical\Cell<Credit>'.</span></span>
13. <span data-ttu-id="28cca-182">ツリーで、「model: Data model Financial dimensions sample model\Journal: Record list\Transaction: Record list\Credit: Real」を選択します。</span><span class="sxs-lookup"><span data-stu-id="28cca-182">In the tree, select 'model: Data model Financial dimensions sample model\Journal: Record list\Transaction: Record list\Credit: Real'.</span></span>
14. <span data-ttu-id="28cca-183">[バインド] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="28cca-183">Click Bind.</span></span>
15. <span data-ttu-id="28cca-184">ツリーで、「Excel = "SampleFinDimWsReport"\Range<JournalLine>: Vertical\Range<TransactionLine>: Vertical\Cell<Debit>」を選択します。</span><span class="sxs-lookup"><span data-stu-id="28cca-184">In the tree, select 'Excel = "SampleFinDimWsReport"\Range<JournalLine>: Vertical\Range<TransactionLine>: Vertical\Cell<Debit>'.</span></span>
16. <span data-ttu-id="28cca-185">ツリーで、「model: Data model Financial dimensions sample model\Journal: Record list\Transaction: Record list\Debit: Real」を選択します。</span><span class="sxs-lookup"><span data-stu-id="28cca-185">In the tree, select 'model: Data model Financial dimensions sample model\Journal: Record list\Transaction: Record list\Debit: Real'.</span></span>
17. <span data-ttu-id="28cca-186">[バインド] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="28cca-186">Click Bind.</span></span>
18. <span data-ttu-id="28cca-187">ツリーで、「Excel = "SampleFinDimWsReport"\Range<JournalLine>: Vertical\Range<TransactionLine>: Vertical\Cell<Currency>」を選択します。</span><span class="sxs-lookup"><span data-stu-id="28cca-187">In the tree, select 'Excel = "SampleFinDimWsReport"\Range<JournalLine>: Vertical\Range<TransactionLine>: Vertical\Cell<Currency>'.</span></span>
19. <span data-ttu-id="28cca-188">ツリーで、「model: Data model Financial dimensions sample model\Journal: Record list\Transaction: Record list\Currency: String」を選択します。</span><span class="sxs-lookup"><span data-stu-id="28cca-188">In the tree, select 'model: Data model Financial dimensions sample model\Journal: Record list\Transaction: Record list\Currency: String'.</span></span>
20. <span data-ttu-id="28cca-189">[バインド] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="28cca-189">Click Bind.</span></span>
21. <span data-ttu-id="28cca-190">ツリーで、「Excel = "SampleFinDimWsReport"\Range<JournalLine>: Vertical\Range<TransactionLine>: Vertical\Cell<TransDate>」を選択します。</span><span class="sxs-lookup"><span data-stu-id="28cca-190">In the tree, select 'Excel = "SampleFinDimWsReport"\Range<JournalLine>: Vertical\Range<TransactionLine>: Vertical\Cell<TransDate>'.</span></span>
22. <span data-ttu-id="28cca-191">ツリーで、「model: Data model Financial dimensions sample model\Journal: Record list\Transaction: Record list\Date: Date」を選択します。</span><span class="sxs-lookup"><span data-stu-id="28cca-191">In the tree, select 'model: Data model Financial dimensions sample model\Journal: Record list\Transaction: Record list\Date: Date'.</span></span>
23. <span data-ttu-id="28cca-192">[バインド] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="28cca-192">Click Bind.</span></span>
24. <span data-ttu-id="28cca-193">ツリーで、「Excel = "SampleFinDimWsReport"\Range<JournalLine>: Vertical\Range<TransactionLine>: Vertical\Cell<TransVoucher>」を選択します。</span><span class="sxs-lookup"><span data-stu-id="28cca-193">In the tree, select 'Excel = "SampleFinDimWsReport"\Range<JournalLine>: Vertical\Range<TransactionLine>: Vertical\Cell<TransVoucher>'.</span></span>
25. <span data-ttu-id="28cca-194">ツリーで、「model: Data model Financial dimensions sample model\Journal: Record list\Transaction: Record list\Currency: String」を選択します。</span><span class="sxs-lookup"><span data-stu-id="28cca-194">In the tree, select 'model: Data model Financial dimensions sample model\Journal: Record list\Transaction: Record list\Voucher: String'.</span></span>
26. <span data-ttu-id="28cca-195">[バインド] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="28cca-195">Click Bind.</span></span>
27. <span data-ttu-id="28cca-196">ツリーで、「Excel = "SampleFinDimWsReport"\Range<JournalLine>: Vertical\Range<TransactionLine>: Vertical\Cell<TransBatch>」を選択します。</span><span class="sxs-lookup"><span data-stu-id="28cca-196">In the tree, select 'Excel = "SampleFinDimWsReport"\Range<JournalLine>: Vertical\Range<TransactionLine>: Vertical\Cell<TransBatch>'.</span></span>
28. <span data-ttu-id="28cca-197">ツリーで、「model: Data model Financial dimensions sample model\Journal: Record list\Batch: String」を選択します。</span><span class="sxs-lookup"><span data-stu-id="28cca-197">In the tree, select 'model: Data model Financial dimensions sample model\Journal: Record list\Batch: String'.</span></span>
29. <span data-ttu-id="28cca-198">[バインド] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="28cca-198">Click Bind.</span></span>
30. <span data-ttu-id="28cca-199">ツリーで、「Excel = "SampleFinDimWsReport"\Range<JournalLine>: Vertical\Range<TransactionLine>: Vertical」を選択します。</span><span class="sxs-lookup"><span data-stu-id="28cca-199">In the tree, select 'Excel = "SampleFinDimWsReport"\Range<JournalLine>: Vertical\Range<TransactionLine>: Vertical'.</span></span>
31. <span data-ttu-id="28cca-200">ツリーで、「model: Data model Financial dimensions sample model\Journal: Record list\Transaction: Record list」を選択します。</span><span class="sxs-lookup"><span data-stu-id="28cca-200">In the tree, select 'model: Data model Financial dimensions sample model\Journal: Record list\Transaction: Record list'.</span></span>
32. <span data-ttu-id="28cca-201">[バインド] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="28cca-201">Click Bind.</span></span>
33. <span data-ttu-id="28cca-202">ツリーで、「Excel = "SampleFinDimWsReport"\Range<JournalLine>: Vertical\Cell<Batch>」を選択します。</span><span class="sxs-lookup"><span data-stu-id="28cca-202">In the tree, select 'Excel = "SampleFinDimWsReport"\Range<JournalLine>: Vertical\Cell<Batch>'.</span></span>
34. <span data-ttu-id="28cca-203">ツリーで、「model: Data model Financial dimensions sample model\Journal: Record list\Batch: String」を選択します。</span><span class="sxs-lookup"><span data-stu-id="28cca-203">In the tree, select 'model: Data model Financial dimensions sample model\Journal: Record list\Batch: String'.</span></span>
35. <span data-ttu-id="28cca-204">[バインド] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="28cca-204">Click Bind.</span></span>
36. <span data-ttu-id="28cca-205">ツリーで、「Excel = "SampleFinDimWsReport"\Range<JournalLine>: Vertical」を選択します。</span><span class="sxs-lookup"><span data-stu-id="28cca-205">In the tree, select 'Excel = "SampleFinDimWsReport"\Range<JournalLine>: Vertical'.</span></span>
37. <span data-ttu-id="28cca-206">ツリーで、「model: Data model Financial dimensions sample model\Journal: Record list」を選択します。</span><span class="sxs-lookup"><span data-stu-id="28cca-206">In the tree, select 'model: Data model Financial dimensions sample model\Journal: Record list'.</span></span>
38. <span data-ttu-id="28cca-207">[バインド] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="28cca-207">Click Bind.</span></span>
39. <span data-ttu-id="28cca-208">ツリーで、「model: Data model Financial dimensions sample model\Dimensions setting: Record list」を展開します。</span><span class="sxs-lookup"><span data-stu-id="28cca-208">In the tree, expand 'model: Data model Financial dimensions sample model\Dimensions setting: Record list'.</span></span>
40. <span data-ttu-id="28cca-209">ツリーで、「model: Data model Financial dimensions sample model\Dimensions setting: Record list\Code: String」を選択します。</span><span class="sxs-lookup"><span data-stu-id="28cca-209">In the tree, select 'model: Data model Financial dimensions sample model\Dimensions setting: Record list\Code: String'.</span></span>
41. <span data-ttu-id="28cca-210">ツリーで、「Excel = "SampleFinDimWsReport"\Range<DimNames>: Horizontal\Cell<DimNames>」を選択します。</span><span class="sxs-lookup"><span data-stu-id="28cca-210">In the tree, select 'Excel = "SampleFinDimWsReport"\Range<DimNames>: Horizontal\Cell<DimNames>'.</span></span>
42. <span data-ttu-id="28cca-211">[バインド] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="28cca-211">Click Bind.</span></span>
43. <span data-ttu-id="28cca-212">ツリーで、「model: Data model Financial dimensions sample model\Dimensions setting: Record list」を選択します。</span><span class="sxs-lookup"><span data-stu-id="28cca-212">In the tree, select 'model: Data model Financial dimensions sample model\Dimensions setting: Record list'.</span></span>
44. <span data-ttu-id="28cca-213">ツリーで、「Excel = "SampleFinDimWsReport"\Range<DimNames>: Horizontal」を選択します。</span><span class="sxs-lookup"><span data-stu-id="28cca-213">In the tree, select 'Excel = "SampleFinDimWsReport"\Range<DimNames>: Horizontal'.</span></span>
45. <span data-ttu-id="28cca-214">[バインド] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="28cca-214">Click Bind.</span></span>
46. <span data-ttu-id="28cca-215">ツリーで、「Excel = "SampleFinDimWsReport"\Cell<CompanyName>」を選択します。</span><span class="sxs-lookup"><span data-stu-id="28cca-215">In the tree, select 'Excel = "SampleFinDimWsReport"\Cell<CompanyName>'.</span></span>
47. <span data-ttu-id="28cca-216">ツリーで、「model: Data model Financial dimensions sample model\Company: String」を選択します。</span><span class="sxs-lookup"><span data-stu-id="28cca-216">In the tree, select 'model: Data model Financial dimensions sample model\Company: String'.</span></span>
48. <span data-ttu-id="28cca-217">[バインド] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="28cca-217">Click Bind.</span></span>
49. <span data-ttu-id="28cca-218">[保存] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="28cca-218">Click Save.</span></span>
50. <span data-ttu-id="28cca-219">ページを閉じます。</span><span class="sxs-lookup"><span data-stu-id="28cca-219">Close the page.</span></span>



[!INCLUDE[footer-include](../../../../includes/footer-banner.md)]