---
title: ER 棚卸および集計を行うための形式のコンフィギュレーション (第 2 部 - 計算のコンフィギュレーション)
description: このトピックでは、既に生成されたテキスト出力のデータに基づいて棚卸および集計を行うために電子レポート形式を構成する方法について説明します。 (第 2 部)
author: NickSelin
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: ERWorkspace, ERSolutionTable, ERSolutionCreateDropDialog, EROperationDesigner, ERDataSourceAddDropDialog, ERExpressionDesignerFormula
audience: Application User
ms.reviewer: kfend
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: d6eb3d686e8f60de51001deffb4c2460c181a4ab
ms.sourcegitcommit: 6cb174d1ec8b55946dca4db03d6a3c3f4c6fa2df
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 03/09/2021
ms.locfileid: "5565169"
---
# <a name="er-configure-format-to-do-counting-and-summing-part-2---configure-computations"></a><span data-ttu-id="e1070-104">ER 棚卸および集計を行うための形式のコンフィギュレーション (第 2 部 - 計算のコンフィギュレーション)</span><span class="sxs-lookup"><span data-stu-id="e1070-104">ER Configure format to do counting and summing (Part 2 - Configure computations)</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="e1070-105">次の手順では、システム管理者または電子レポート開発者のロールに指定されたユーザーが、生成済みのテキスト出力に基づく計算と集計の電子レポート（ER）フォーマットをどのように環境設定するのかについて示します。</span><span class="sxs-lookup"><span data-stu-id="e1070-105">The following steps explain how a user assigned to the system administrator or electronic reporting developer role can configure an Electronic reporting (ER) format to do counting and summing based on data of the already generated text output.</span></span> <span data-ttu-id="e1070-106">これらの手順はどのタイプの企業でも実施できます。</span><span class="sxs-lookup"><span data-stu-id="e1070-106">These steps can be performed in any company.</span></span>

<span data-ttu-id="e1070-107">これらの手順を完了するには、まず「計算と集計を行う ER 設定フォーマット（パート1：フォーマットの作成）」に記載の手順を完了する必要があります。</span><span class="sxs-lookup"><span data-stu-id="e1070-107">To complete these steps, you must first complete the steps in the "ER Configure format to do counting and summing (Part 1: Create format)" procedure.</span></span>

<span data-ttu-id="e1070-108">この手順は Dynamics 365 for Operations バージョン 1611 に追加された機能です。</span><span class="sxs-lookup"><span data-stu-id="e1070-108">This procedure is for a feature that was added in Dynamics 365 for Operations version 1611.</span></span>


## <a name="create-a-format-configuration-to-add-counting-and-summing-details"></a><span data-ttu-id="e1070-109">フォーマット設定を作成し、計算と集計の情報を加えます。</span><span class="sxs-lookup"><span data-stu-id="e1070-109">Create a format configuration to add counting and summing details</span></span>
1. <span data-ttu-id="e1070-110">[組織管理] > [ワークスペース] > [電子申告] の順に移動します。</span><span class="sxs-lookup"><span data-stu-id="e1070-110">Go to Organization administration > Workspaces > Electronic reporting.</span></span>
2. <span data-ttu-id="e1070-111">[コンフィギュレーションをレポートする] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="e1070-111">Click Reporting configurations.</span></span>
3. <span data-ttu-id="e1070-112">ツリーで、「Intrastat model」を展開します。</span><span class="sxs-lookup"><span data-stu-id="e1070-112">In the tree, expand 'Intrastat model'.</span></span>
4. <span data-ttu-id="e1070-113">ツリーで、「イントラスタットmodel\Intrastat (DE)を選択します。</span><span class="sxs-lookup"><span data-stu-id="e1070-113">In the tree, select 'Intrastat model\Intrastat (DE)'.</span></span>
    * <span data-ttu-id="e1070-114">イントラスタット レポートの最後に集計詳細を含む明細行を追加して、Microsoft 提供のフォーマットをカスタマイズする必要があります。</span><span class="sxs-lookup"><span data-stu-id="e1070-114">Assume that you need to customize the format provided by Microsoft by adding lines with summary details at the end of the Intrastat report.</span></span> <span data-ttu-id="e1070-115">そのためには、変更を行うMicrosoftのインスタンスからイントラスタット コンフィギュレーションのインスタンスを取得する必要があります。</span><span class="sxs-lookup"><span data-stu-id="e1070-115">You need to do that by deriving our own instance of the Intrastat configuration from the Microsoft instance to make modifications.</span></span>  
5. <span data-ttu-id="e1070-116">[コンフィギュレーションの作成] をクリックすると、ドロップ ダイアログが開きます。</span><span class="sxs-lookup"><span data-stu-id="e1070-116">Click Create configuration to open the drop dialog.</span></span>
6. <span data-ttu-id="e1070-117">[新規] フィールドで、「名称から取得: Intrastat (DE), Microsoft」を選択します。</span><span class="sxs-lookup"><span data-stu-id="e1070-117">In the New field, enter 'Derive from Name: Intrastat (DE), Microsoft'.</span></span>
7. <span data-ttu-id="e1070-118">[名称] フィールドに、「計算 & 集計を含Intrastat (DE)」と入力します。</span><span class="sxs-lookup"><span data-stu-id="e1070-118">In the Name field, type 'Intrastat (DE) with counting & summing'.</span></span>
8. <span data-ttu-id="e1070-119">[コンフィギュレーションの作成] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="e1070-119">Click Create configuration.</span></span>

## <a name="configure-this-report-to-do-counting-and-summation-based-on-output-details"></a><span data-ttu-id="e1070-120">出荷詳細に基づく計算と集計を行うには、このレポートを設定します。</span><span class="sxs-lookup"><span data-stu-id="e1070-120">Configure this report to do counting and summation based on output details</span></span>
1. <span data-ttu-id="e1070-121">[デザイナー] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="e1070-121">Click Designer.</span></span>
2. <span data-ttu-id="e1070-122">[出荷情報] フィールドで、[はい] を選択します。</span><span class="sxs-lookup"><span data-stu-id="e1070-122">Select Yes in the Collect output details field.</span></span>
    * <span data-ttu-id="e1070-123">このフラグは、イントラスタット ファイル生成に必要な出力情報を収集するプロセスを実行時にアクティブ化します。</span><span class="sxs-lookup"><span data-stu-id="e1070-123">This flag will activate at run-time the process of collecting output details for generating the Intrastat file.</span></span>  
    * <span data-ttu-id="e1070-124">異なる イントラスタット 方向をカウントする必要があるので、このフォーマット構成のデータソースのリストには専用のモデル列挙を追加します。</span><span class="sxs-lookup"><span data-stu-id="e1070-124">You need to do counting for different Intrastat directions, so add a dedicated model enumeration to the data sources' list of this format configuration.</span></span>  
3. <span data-ttu-id="e1070-125">[マッピング] タブをクリックします。</span><span class="sxs-lookup"><span data-stu-id="e1070-125">Click the Mapping tab.</span></span>
4. <span data-ttu-id="e1070-126">[ルートの追加] をクリックして、ドロップ ダイアログを開きます。</span><span class="sxs-lookup"><span data-stu-id="e1070-126">Click Add root to open the drop dialog.</span></span>
5. <span data-ttu-id="e1070-127">ツリーで、「Data model\Enumeration」を選択します。</span><span class="sxs-lookup"><span data-stu-id="e1070-127">In the tree, select 'Data model\Enumeration '.</span></span>
6. <span data-ttu-id="e1070-128">[名称] フィールドに、「指示」を入力します。</span><span class="sxs-lookup"><span data-stu-id="e1070-128">In the Name field, type 'Direction'.</span></span>
7. <span data-ttu-id="e1070-129">[モデル リスト] フィールドで、値を入力または選択します。</span><span class="sxs-lookup"><span data-stu-id="e1070-129">In the Model enumeration field, enter or select a value.</span></span>
    * <span data-ttu-id="e1070-130">値の「指示」を選択します。</span><span class="sxs-lookup"><span data-stu-id="e1070-130">Select the value Direction.</span></span>  
8. <span data-ttu-id="e1070-131">[OK] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="e1070-131">Click OK.</span></span>
9. <span data-ttu-id="e1070-132">[ルートの追加] をクリックして、ドロップ ダイアログを開きます。</span><span class="sxs-lookup"><span data-stu-id="e1070-132">Click Add root to open the drop dialog.</span></span>
10. <span data-ttu-id="e1070-133">ツリーで、[Functions\Calculated field] を選択します。</span><span class="sxs-lookup"><span data-stu-id="e1070-133">In the tree, select 'Functions\Calculated field'.</span></span>
11. <span data-ttu-id="e1070-134">[名称] フィールドに、[$BlockName] を入力します。</span><span class="sxs-lookup"><span data-stu-id="e1070-134">In the Name field, type '$BlockName'.</span></span>
12. <span data-ttu-id="e1070-135">[式の編集] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="e1070-135">Click Edit formula.</span></span>
13. <span data-ttu-id="e1070-136">[式] フィールドに、[ブロック] を入力します。</span><span class="sxs-lookup"><span data-stu-id="e1070-136">In the Formula field, enter '"block"'.</span></span>
14. <span data-ttu-id="e1070-137">[保存] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="e1070-137">Click Save.</span></span>
15. <span data-ttu-id="e1070-138">ページを閉じます。</span><span class="sxs-lookup"><span data-stu-id="e1070-138">Close the page.</span></span>
16. <span data-ttu-id="e1070-139">[OK] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="e1070-139">Click OK.</span></span>
17. <span data-ttu-id="e1070-140">[ルートの追加] をクリックして、ドロップ ダイアログを開きます。</span><span class="sxs-lookup"><span data-stu-id="e1070-140">Click Add root to open the drop dialog.</span></span>
18. <span data-ttu-id="e1070-141">ツリーで、[Functions\Calculated field] を選択します。</span><span class="sxs-lookup"><span data-stu-id="e1070-141">In the tree, select 'Functions\Calculated field'.</span></span>
19. <span data-ttu-id="e1070-142">[名称] フィールドに、[$RecName] を入力します。</span><span class="sxs-lookup"><span data-stu-id="e1070-142">In the Name field, type '$RecName'.</span></span>
20. <span data-ttu-id="e1070-143">[式の編集] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="e1070-143">Click Edit formula.</span></span>
21. <span data-ttu-id="e1070-144">[式] フィールドに、[記録] を入力します。</span><span class="sxs-lookup"><span data-stu-id="e1070-144">In the Formula field, enter '"record"'.</span></span>
22. <span data-ttu-id="e1070-145">[保存] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="e1070-145">Click Save.</span></span>
23. <span data-ttu-id="e1070-146">ページを閉じます。</span><span class="sxs-lookup"><span data-stu-id="e1070-146">Close the page.</span></span>
24. <span data-ttu-id="e1070-147">[OK] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="e1070-147">Click OK.</span></span>
25. <span data-ttu-id="e1070-148">[ルートの追加] をクリックして、ドロップ ダイアログを開きます。</span><span class="sxs-lookup"><span data-stu-id="e1070-148">Click Add root to open the drop dialog.</span></span>
26. <span data-ttu-id="e1070-149">ツリーで、[Functions\Calculated field] を選択します。</span><span class="sxs-lookup"><span data-stu-id="e1070-149">In the tree, select 'Functions\Calculated field'.</span></span>
27. <span data-ttu-id="e1070-150">[名称] フィールドに、[$InvName] を入力します。</span><span class="sxs-lookup"><span data-stu-id="e1070-150">In the Name field, type '$InvName'.</span></span>
28. <span data-ttu-id="e1070-151">[式の編集] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="e1070-151">Click Edit formula.</span></span>
29. <span data-ttu-id="e1070-152">[式] フィールドに、[InvoicedAmountEUR] を入力します。</span><span class="sxs-lookup"><span data-stu-id="e1070-152">In the Formula field, enter '"InvoicedAmountEUR"'.</span></span>
30. <span data-ttu-id="e1070-153">[保存] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="e1070-153">Click Save.</span></span>
31. <span data-ttu-id="e1070-154">ページを閉じます。</span><span class="sxs-lookup"><span data-stu-id="e1070-154">Close the page.</span></span>
32. <span data-ttu-id="e1070-155">[OK] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="e1070-155">Click OK.</span></span>
33. <span data-ttu-id="e1070-156">ツリーで、「Intrastat\Data」を選択します。</span><span class="sxs-lookup"><span data-stu-id="e1070-156">In the tree, select 'Intrastat\Data'.</span></span>
34. <span data-ttu-id="e1070-157">「収集したデータ キー名称」フィールドの編集ボタンをクリックします</span><span class="sxs-lookup"><span data-stu-id="e1070-157">Click Edit button for the 'Collected data key name' field</span></span>
35. <span data-ttu-id="e1070-158">[データ ソースの追加] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="e1070-158">Click Add data source.</span></span>
    * <span data-ttu-id="e1070-159">$BlockName</span><span class="sxs-lookup"><span data-stu-id="e1070-159">$BlockName</span></span>  
36. <span data-ttu-id="e1070-160">[保存] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="e1070-160">Click Save.</span></span>
37. <span data-ttu-id="e1070-161">ページを閉じます。</span><span class="sxs-lookup"><span data-stu-id="e1070-161">Close the page.</span></span>
38. <span data-ttu-id="e1070-162">「収集したデータ キー値」のフィールドの編集のボタンをクリックします。</span><span class="sxs-lookup"><span data-stu-id="e1070-162">Click the Edit button for the Collected data key value field.</span></span>
39. <span data-ttu-id="e1070-163">[式] フィールドに、「IF(Intrastat.CommodityRecord.Direction=Direction.Import, "Import", "Export")」を入力します。</span><span class="sxs-lookup"><span data-stu-id="e1070-163">In the Formula field, enter 'IF(Intrastat.CommodityRecord.Direction=Direction.Import, "Import", "Export")'.</span></span>
    * <span data-ttu-id="e1070-164">IF(Intrastat.CommodityRecord.Direction=Direction.Import, "Import", "Export")</span><span class="sxs-lookup"><span data-stu-id="e1070-164">IF(Intrastat.CommodityRecord.Direction=Direction.Import, "Import", "Export")</span></span>  
40. <span data-ttu-id="e1070-165">[保存] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="e1070-165">Click Save.</span></span>
41. <span data-ttu-id="e1070-166">ページを閉じます。</span><span class="sxs-lookup"><span data-stu-id="e1070-166">Close the page.</span></span>
    * <span data-ttu-id="e1070-167">このシーケンスの明細行をカウントします。</span><span class="sxs-lookup"><span data-stu-id="e1070-167">Count the lines of this sequence.</span></span> <span data-ttu-id="e1070-168">結果は 「ブロック」 という名称で方向性ごとに分けて使用されます。</span><span class="sxs-lookup"><span data-stu-id="e1070-168">The results will be used with the name "block" separately for different directions.</span></span> <span data-ttu-id="e1070-169">値 「インポートは」 、すべての到着イントラスタット トランザクションに使用されます。</span><span class="sxs-lookup"><span data-stu-id="e1070-169">Value "Import" will be used for any arrivals Intrastat transactions.</span></span> <span data-ttu-id="e1070-170">値「エクスポートは」、すべての発送イントラスタット トランザクションに使用されます。</span><span class="sxs-lookup"><span data-stu-id="e1070-170">The value "Export" will be used for any Intrastat dispatches transactions.</span></span> <span data-ttu-id="e1070-171">これが仮想のExcelワークシートの有効であるとみなします。</span><span class="sxs-lookup"><span data-stu-id="e1070-171">Consider this to be a virtual Excel spreadsheet.</span></span> <span data-ttu-id="e1070-172">それぞれのトランザクションでは、最初の列 「ブロック」 には 「インポート」 と 「エクスポート」 が入ります。</span><span class="sxs-lookup"><span data-stu-id="e1070-172">For each transaction a row where the first column "block" is filled with the values "Import" and "Export" accordingly.</span></span>  
42. <span data-ttu-id="e1070-173">ツリーで、「Intrastat\Data: Sequence」を展開します。</span><span class="sxs-lookup"><span data-stu-id="e1070-173">In the tree, expand 'Intrastat\Data: Sequence'.</span></span>
43. <span data-ttu-id="e1070-174">ツリーで、「Intrastat\Data: Sequence\Arrivals?」を選択します。</span><span class="sxs-lookup"><span data-stu-id="e1070-174">In the tree, select 'Intrastat\Data: Sequence\Arrivals?'.</span></span>
44. <span data-ttu-id="e1070-175">「収集したデータ キー名称」フィールドの編集ボタンをクリックします。</span><span class="sxs-lookup"><span data-stu-id="e1070-175">Click Edit button for the 'Collected data key name' field.</span></span>
    * <span data-ttu-id="e1070-176">このシーケンスの明細行をカウントします。</span><span class="sxs-lookup"><span data-stu-id="e1070-176">Count the lines of this sequence.</span></span> <span data-ttu-id="e1070-177">結果は、「レコード」 という名称を使用して記憶されます。</span><span class="sxs-lookup"><span data-stu-id="e1070-177">The results will be memorized using the name "record".</span></span>  
45. <span data-ttu-id="e1070-178">ツリーで、「$RecName」を選択します。</span><span class="sxs-lookup"><span data-stu-id="e1070-178">In the tree, select '$RecName'.</span></span>
46. <span data-ttu-id="e1070-179">[データ ソースの追加] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="e1070-179">Click Add data source.</span></span>
47. <span data-ttu-id="e1070-180">[保存] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="e1070-180">Click Save.</span></span>
48. <span data-ttu-id="e1070-181">ページを閉じます。</span><span class="sxs-lookup"><span data-stu-id="e1070-181">Close the page.</span></span>
49. <span data-ttu-id="e1070-182">「収集したデータ キー値」 フィールドの編集ボタンをクリックします</span><span class="sxs-lookup"><span data-stu-id="e1070-182">Click Edit button for the 'Collected data key value' field</span></span>
50. <span data-ttu-id="e1070-183">[式] フィールドで、「Intrastat.CommodityRecord.CommodityCode」を入力します。</span><span class="sxs-lookup"><span data-stu-id="e1070-183">In the Formula field, enter 'Intrastat.CommodityRecord.CommodityCode'.</span></span>
51. <span data-ttu-id="e1070-184">[保存] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="e1070-184">Click Save.</span></span>
52. <span data-ttu-id="e1070-185">ページを閉じます。</span><span class="sxs-lookup"><span data-stu-id="e1070-185">Close the page.</span></span>
    * <span data-ttu-id="e1070-186">このシーケンスの明細行をカウントします。</span><span class="sxs-lookup"><span data-stu-id="e1070-186">Count the lines of this sequence.</span></span> <span data-ttu-id="e1070-187">結果は、異なる商品コードごとに「レコード」という名前で使用されます。</span><span class="sxs-lookup"><span data-stu-id="e1070-187">The results will be used with the name "record" separately for different commodity codes.</span></span> <span data-ttu-id="e1070-188">これが仮想のExcelワークシートの有効であるとみなします。</span><span class="sxs-lookup"><span data-stu-id="e1070-188">Consider this to be a virtual Excel spreadsheet.</span></span> <span data-ttu-id="e1070-189">それぞれのトランザクションでは、最初の列 「ブロック」 には 「インポート」 と 「エクスポート」 が入り、2 番目のブロック 「レコード」 には商品コードの値が入ります。</span><span class="sxs-lookup"><span data-stu-id="e1070-189">For each transaction a row where the first column "block" is filled with the values "Import" and "Export" accordingly and the second block "record" is filled with the commodity code value.</span></span>  
53. <span data-ttu-id="e1070-190">ツリーで、「Intrastat\Data: Sequence\Dispatches?」を選択します。</span><span class="sxs-lookup"><span data-stu-id="e1070-190">In the tree, select 'Intrastat\Data: Sequence\Dispatches?'.</span></span>
54. <span data-ttu-id="e1070-191">「収集したデータ キー名称」フィールドの編集ボタンをクリックします</span><span class="sxs-lookup"><span data-stu-id="e1070-191">Click Edit button for the 'Collected data key name' field</span></span>
55. <span data-ttu-id="e1070-192">ツリーで、「$RecName」を選択します。</span><span class="sxs-lookup"><span data-stu-id="e1070-192">In the tree, select '$RecName'.</span></span>
56. <span data-ttu-id="e1070-193">[データ ソースの追加] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="e1070-193">Click Add data source.</span></span>
57. <span data-ttu-id="e1070-194">[保存] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="e1070-194">Click Save.</span></span>
58. <span data-ttu-id="e1070-195">ページを閉じます。</span><span class="sxs-lookup"><span data-stu-id="e1070-195">Close the page.</span></span>
59. <span data-ttu-id="e1070-196">「収集したデータ キー値」フィールドの編集ボタンをクリックします。</span><span class="sxs-lookup"><span data-stu-id="e1070-196">Click the Edit button for the 'Collected data key value' field.</span></span>
60. <span data-ttu-id="e1070-197">[式] フィールドで、「Intrastat.CommodityRecord.CommodityCode」を入力します。</span><span class="sxs-lookup"><span data-stu-id="e1070-197">In the Formula field, enter 'Intrastat.CommodityRecord.CommodityCode'.</span></span>
61. <span data-ttu-id="e1070-198">[保存] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="e1070-198">Click Save.</span></span>
62. <span data-ttu-id="e1070-199">ページを閉じます。</span><span class="sxs-lookup"><span data-stu-id="e1070-199">Close the page.</span></span>
63. <span data-ttu-id="e1070-200">ツリーで、「Intrastat\Data: Sequence\Dispatches: Sequence?」を展開します。</span><span class="sxs-lookup"><span data-stu-id="e1070-200">In the tree, expand 'Intrastat\Data: Sequence\Dispatches: Sequence?'.</span></span>
64. <span data-ttu-id="e1070-201">ツリーで、「Intrastat\Data: Sequence\Dispatches: Sequence?\Record =  Intrastat.CommodityRecord」を展開します。</span><span class="sxs-lookup"><span data-stu-id="e1070-201">In the tree, expand 'Intrastat\Data: Sequence\Dispatches: Sequence?\Record =  Intrastat.CommodityRecord'.</span></span>
65. <span data-ttu-id="e1070-202">[フォーマット] タブをクリックします。</span><span class="sxs-lookup"><span data-stu-id="e1070-202">Click the Format tab.</span></span>
66. <span data-ttu-id="e1070-203">ツリーで、「Intrastat\Data\Dispatches\Record\Invoice amount EUR」を選択します。</span><span class="sxs-lookup"><span data-stu-id="e1070-203">In the tree, select 'Intrastat\Data\Dispatches\Record\Invoice amount EUR'.</span></span>
67. <span data-ttu-id="e1070-204">[マッピング] タブをクリックします。</span><span class="sxs-lookup"><span data-stu-id="e1070-204">Click the Mapping tab.</span></span>
68. <span data-ttu-id="e1070-205">「収集したデータ キー名」フィールドの編集ボタンをクリックします。</span><span class="sxs-lookup"><span data-stu-id="e1070-205">Click the Edit button for the 'Collected data key name' field.</span></span>
69. <span data-ttu-id="e1070-206">ツリーで、「$InvName」を選択します。</span><span class="sxs-lookup"><span data-stu-id="e1070-206">In the tree, select '$InvName'.</span></span>
70. <span data-ttu-id="e1070-207">[データ ソースの追加] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="e1070-207">Click Add data source.</span></span>
71. <span data-ttu-id="e1070-208">[保存] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="e1070-208">Click Save.</span></span>
72. <span data-ttu-id="e1070-209">ページを閉じます。</span><span class="sxs-lookup"><span data-stu-id="e1070-209">Close the page.</span></span>
    * <span data-ttu-id="e1070-210">このシーケンスの明細行について、請求額を集計します。</span><span class="sxs-lookup"><span data-stu-id="e1070-210">Summarize the invoiced amount values for lines of this sequence.</span></span> <span data-ttu-id="e1070-211">結果のイントラスタットの方向性や商品コードが異なる場合は、別途 「InvoicedAmountEUR」 という名称で使用されます。</span><span class="sxs-lookup"><span data-stu-id="e1070-211">The results will be used with the name "InvoicedAmountEUR" separately for different Intrastat directions and commodity codes.</span></span> <span data-ttu-id="e1070-212">これが仮想のExcelスプレッドシートであるとみなします。</span><span class="sxs-lookup"><span data-stu-id="e1070-212">Consider this to be a virtual creation in Excel spreadsheet.</span></span> <span data-ttu-id="e1070-213">それぞれのトランザクションでは、最初の列 「ブロック」 には 「インポート」 と 「エクスポート」 が入ります。</span><span class="sxs-lookup"><span data-stu-id="e1070-213">For each transaction a row where the first column "block" is filled with the values "Import" and "Export" accordingly.</span></span> <span data-ttu-id="e1070-214">2 番目のブロック 「記録」 には商品コードの値が入り、3 番目の列 「InvoicedAmountEUR値」 には請求金額が入ります。</span><span class="sxs-lookup"><span data-stu-id="e1070-214">The second block "record" is filled with the commodity code value, and the third column "InvoicedAmountEUR" is filled with the invoice amount value.</span></span>  
73. <span data-ttu-id="e1070-215">ツリーで、「Intrastat\Data\Arrivals?」を展開します。</span><span class="sxs-lookup"><span data-stu-id="e1070-215">In the tree, expand 'Intrastat\Data\Arrivals?'.</span></span>
74. <span data-ttu-id="e1070-216">ツリーで、「Intrastat\Data\Arrivals?\Record =  Intrastat.CommodityRecord」を展開します。</span><span class="sxs-lookup"><span data-stu-id="e1070-216">In the tree, expand 'Intrastat\Data\Arrivals?\Record =  Intrastat.CommodityRecord'.</span></span>
75. <span data-ttu-id="e1070-217">[フォーマット] タブをクリックします。</span><span class="sxs-lookup"><span data-stu-id="e1070-217">Click the Format tab.</span></span>
76. <span data-ttu-id="e1070-218">ツリーで、「Intrastat\Data\Dispatches\Record\Invoice amount EUR」を選択します。</span><span class="sxs-lookup"><span data-stu-id="e1070-218">In the tree, select 'Intrastat\Data\Arrivals\Record\Invoice amount EUR'.</span></span>
77. <span data-ttu-id="e1070-219">[マッピング] タブをクリックします。</span><span class="sxs-lookup"><span data-stu-id="e1070-219">Click the Mapping tab.</span></span>
78. <span data-ttu-id="e1070-220">「収集したデータ キー名」フィールドの編集ボタンをクリックします。</span><span class="sxs-lookup"><span data-stu-id="e1070-220">Click the Edit button for the 'Collected data key name' field.</span></span>
79. <span data-ttu-id="e1070-221">ツリーで、「$InvName」を選択します。</span><span class="sxs-lookup"><span data-stu-id="e1070-221">In the tree, select '$InvName'.</span></span>
80. <span data-ttu-id="e1070-222">[データ ソースの追加] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="e1070-222">Click Add data source.</span></span>
81. <span data-ttu-id="e1070-223">[保存] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="e1070-223">Click Save.</span></span>
82. <span data-ttu-id="e1070-224">ページを閉じます。</span><span class="sxs-lookup"><span data-stu-id="e1070-224">Close the page.</span></span>
83. <span data-ttu-id="e1070-225">[保存] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="e1070-225">Click Save.</span></span>
84. <span data-ttu-id="e1070-226">ページを閉じます。</span><span class="sxs-lookup"><span data-stu-id="e1070-226">Close the page.</span></span>



[!INCLUDE[footer-include](../../../../includes/footer-banner.md)]