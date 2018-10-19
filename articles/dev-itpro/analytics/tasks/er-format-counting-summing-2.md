--- 
title: "ER 棚卸および集計を行うための形式のコンフィギュレーション (第 2 部 - 計算のコンフィギュレーション)"
description: "次の手順では、システム管理者または電子レポート開発者のロールに指定されたユーザーが、生成済みのテキスト出力に基づく計算と集計の電子レポート（ER）フォーマットをどのように環境設定するのかについて示します。"
author: NickSelin
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: ERWorkspace, ERSolutionTable, ERSolutionCreateDropDialog, EROperationDesigner, ERDataSourceAddDropDialog, ERExpressionDesignerFormula
audience: Application User
ms.reviewer: kfend
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 0312b8cfadd45f8e59225e9daba78b9e216cff51
ms.openlocfilehash: 4ef657b13bc1f7f4a84676821e4175ace32c069a
ms.contentlocale: ja-jp
ms.lasthandoff: 10/16/2018

---
# <a name="er-configure-format-to-do-counting-and-summing-part-2-configure-computations"></a><span data-ttu-id="075b3-103">ER 棚卸および集計を行うための形式のコンフィギュレーション (パート 2: コンフィギュレーションの計算)</span><span class="sxs-lookup"><span data-stu-id="075b3-103">ER Configure format to do counting and summing (Part 2: Configure computations)</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="075b3-104">次の手順では、システム管理者または電子レポート開発者のロールに指定されたユーザーが、生成済みのテキスト出力に基づく計算と集計の電子レポート（ER）フォーマットをどのように環境設定するのかについて示します。</span><span class="sxs-lookup"><span data-stu-id="075b3-104">The following steps explain how a user assigned to the system administrator or electronic reporting developer role can configure an Electronic reporting (ER) format to do counting and summing based on data of the already generated text output.</span></span> <span data-ttu-id="075b3-105">これらの手順はどのタイプの企業でも実施できます。</span><span class="sxs-lookup"><span data-stu-id="075b3-105">These steps can be performed in any company.</span></span>

<span data-ttu-id="075b3-106">これらの手順を完了するには、まず「計算と集計を行うER設定フォーマット（パート1：フォーマットの作成）」の手順を完了する必要があります。</span><span class="sxs-lookup"><span data-stu-id="075b3-106">To complete these steps, you must first complete the steps in the “ER Configure format to do counting and summing (Part 1: Create format)” procedure.</span></span>

<span data-ttu-id="075b3-107">この手順は、Dynamics 365 for Operations、バージョン 1611 に追加された機能です。</span><span class="sxs-lookup"><span data-stu-id="075b3-107">This procedure is for a feature that was added in Dynamics 365 for Operations version 1611.</span></span>


## <a name="create-a-format-configuration-to-add-counting-and-summing-details"></a><span data-ttu-id="075b3-108">フォーマット設定を作成し、計算と集計の情報を加えます。</span><span class="sxs-lookup"><span data-stu-id="075b3-108">Create a format configuration to add counting and summing details</span></span>
1. <span data-ttu-id="075b3-109">[組織管理] > [ワークスペース] > [電子申告] の順に移動します。</span><span class="sxs-lookup"><span data-stu-id="075b3-109">Go to Organization administration > Workspaces > Electronic reporting.</span></span>
2. <span data-ttu-id="075b3-110">[コンフィギュレーションをレポートする] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="075b3-110">Click Reporting configurations.</span></span>
3. <span data-ttu-id="075b3-111">ツリーで、「Intrastat model」を展開します。</span><span class="sxs-lookup"><span data-stu-id="075b3-111">In the tree, expand 'Intrastat model'.</span></span>
4. <span data-ttu-id="075b3-112">ツリーで、「イントラスタットmodel\Intrastat (DE)を選択します。</span><span class="sxs-lookup"><span data-stu-id="075b3-112">In the tree, select 'Intrastat model\Intrastat (DE)'.</span></span>
    * <span data-ttu-id="075b3-113">イントラスタット レポートの最後に集計詳細を含む明細行を追加して、Microsoft 提供のフォーマットをカスタマイズする必要があります。</span><span class="sxs-lookup"><span data-stu-id="075b3-113">Assume that you need to customize the format provided by Microsoft by adding lines with summary details at the end of the Intrastat report.</span></span> <span data-ttu-id="075b3-114">そのためには、変更を行うMicrosoftのインスタンスからイントラスタット コンフィギュレーションのインスタンスを取得する必要があります。</span><span class="sxs-lookup"><span data-stu-id="075b3-114">You need to do that by deriving our own instance of the Intrastat configuration from the Microsoft instance to make modifications.</span></span>  
5. <span data-ttu-id="075b3-115">[コンフィギュレーションの作成] をクリックすると、ドロップ ダイアログが開きます。</span><span class="sxs-lookup"><span data-stu-id="075b3-115">Click Create configuration to open the drop dialog.</span></span>
6. <span data-ttu-id="075b3-116">[新規] フィールドで、「名称から取得: Intrastat (DE), Microsoft」を選択します。</span><span class="sxs-lookup"><span data-stu-id="075b3-116">In the New field, enter 'Derive from Name: Intrastat (DE), Microsoft'.</span></span>
7. <span data-ttu-id="075b3-117">[名称] フィールドに、「計算 & 集計を含Intrastat (DE)」と入力します。</span><span class="sxs-lookup"><span data-stu-id="075b3-117">In the Name field, type 'Intrastat (DE) with counting & summing'.</span></span>
8. <span data-ttu-id="075b3-118">[コンフィギュレーションの作成] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="075b3-118">Click Create configuration.</span></span>

## <a name="configure-this-report-to-do-counting-and-summation-based-on-output-details"></a><span data-ttu-id="075b3-119">出荷詳細に基づく計算と集計を行うには、このレポートを設定します。</span><span class="sxs-lookup"><span data-stu-id="075b3-119">Configure this report to do counting and summation based on output details</span></span>
1. <span data-ttu-id="075b3-120">[デザイナー] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="075b3-120">Click Designer.</span></span>
2. <span data-ttu-id="075b3-121">[出荷情報] フィールドで、[はい] を選択します。</span><span class="sxs-lookup"><span data-stu-id="075b3-121">Select Yes in the Collect output details field.</span></span>
    * <span data-ttu-id="075b3-122">このフラグは、イントラスタット ファイル生成に必要な出力情報を収集するプロセスを実行時にアクティブ化します。</span><span class="sxs-lookup"><span data-stu-id="075b3-122">This flag will activate at run-time the process of collecting output details for generating the Intrastat file.</span></span>  
    * <span data-ttu-id="075b3-123">イントラスタットのさまざまな指示について計算をする必要があるため、このフォーマットのコンフィグレーションのデータソースリストに専用モデルリストを追加します。</span><span class="sxs-lookup"><span data-stu-id="075b3-123">You need to do counting for different Intrastat directions, so add a dedicated model enumeration to the data sources’ list of this format configuration.</span></span>  
3. <span data-ttu-id="075b3-124">[マッピング] タブをクリックします。</span><span class="sxs-lookup"><span data-stu-id="075b3-124">Click the Mapping tab.</span></span>
4. <span data-ttu-id="075b3-125">[ルートの追加] をクリックして、ドロップ ダイアログを開きます。</span><span class="sxs-lookup"><span data-stu-id="075b3-125">Click Add root to open the drop dialog.</span></span>
5. <span data-ttu-id="075b3-126">ツリーで、「Data model\Enumeration」を選択します。</span><span class="sxs-lookup"><span data-stu-id="075b3-126">In the tree, select 'Data model\Enumeration '.</span></span>
6. <span data-ttu-id="075b3-127">[名称] フィールドに、「指示」を入力します。</span><span class="sxs-lookup"><span data-stu-id="075b3-127">In the Name field, type 'Direction'.</span></span>
7. <span data-ttu-id="075b3-128">[モデル リスト] フィールドで、値を入力または選択します。</span><span class="sxs-lookup"><span data-stu-id="075b3-128">In the Model enumeration field, enter or select a value.</span></span>
    * <span data-ttu-id="075b3-129">値の「指示」を選択します。</span><span class="sxs-lookup"><span data-stu-id="075b3-129">Select the value Direction.</span></span>  
8. <span data-ttu-id="075b3-130">[OK] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="075b3-130">Click OK.</span></span>
9. <span data-ttu-id="075b3-131">[ルートの追加] をクリックして、ドロップ ダイアログを開きます。</span><span class="sxs-lookup"><span data-stu-id="075b3-131">Click Add root to open the drop dialog.</span></span>
10. <span data-ttu-id="075b3-132">ツリーで、[Functions\Calculated field] を選択します。</span><span class="sxs-lookup"><span data-stu-id="075b3-132">In the tree, select 'Functions\Calculated field'.</span></span>
11. <span data-ttu-id="075b3-133">[名称] フィールドに、[$BlockName] を入力します。</span><span class="sxs-lookup"><span data-stu-id="075b3-133">In the Name field, type '$BlockName'.</span></span>
12. <span data-ttu-id="075b3-134">[式の編集] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="075b3-134">Click Edit formula.</span></span>
13. <span data-ttu-id="075b3-135">[式] フィールドに、[ブロック] を入力します。</span><span class="sxs-lookup"><span data-stu-id="075b3-135">In the Formula field, enter '"block"'.</span></span>
14. <span data-ttu-id="075b3-136">[保存] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="075b3-136">Click Save.</span></span>
15. <span data-ttu-id="075b3-137">ページを閉じます。</span><span class="sxs-lookup"><span data-stu-id="075b3-137">Close the page.</span></span>
16. <span data-ttu-id="075b3-138">[OK] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="075b3-138">Click OK.</span></span>
17. <span data-ttu-id="075b3-139">[ルートの追加] をクリックして、ドロップ ダイアログを開きます。</span><span class="sxs-lookup"><span data-stu-id="075b3-139">Click Add root to open the drop dialog.</span></span>
18. <span data-ttu-id="075b3-140">ツリーで、[Functions\Calculated field] を選択します。</span><span class="sxs-lookup"><span data-stu-id="075b3-140">In the tree, select 'Functions\Calculated field'.</span></span>
19. <span data-ttu-id="075b3-141">[名称] フィールドに、[$RecName] を入力します。</span><span class="sxs-lookup"><span data-stu-id="075b3-141">In the Name field, type '$RecName'.</span></span>
20. <span data-ttu-id="075b3-142">[式の編集] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="075b3-142">Click Edit formula.</span></span>
21. <span data-ttu-id="075b3-143">[式] フィールドに、[記録] を入力します。</span><span class="sxs-lookup"><span data-stu-id="075b3-143">In the Formula field, enter '"record"'.</span></span>
22. <span data-ttu-id="075b3-144">[保存] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="075b3-144">Click Save.</span></span>
23. <span data-ttu-id="075b3-145">ページを閉じます。</span><span class="sxs-lookup"><span data-stu-id="075b3-145">Close the page.</span></span>
24. <span data-ttu-id="075b3-146">[OK] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="075b3-146">Click OK.</span></span>
25. <span data-ttu-id="075b3-147">[ルートの追加] をクリックして、ドロップ ダイアログを開きます。</span><span class="sxs-lookup"><span data-stu-id="075b3-147">Click Add root to open the drop dialog.</span></span>
26. <span data-ttu-id="075b3-148">ツリーで、[Functions\Calculated field] を選択します。</span><span class="sxs-lookup"><span data-stu-id="075b3-148">In the tree, select 'Functions\Calculated field'.</span></span>
27. <span data-ttu-id="075b3-149">[名称] フィールドに、[$InvName] を入力します。</span><span class="sxs-lookup"><span data-stu-id="075b3-149">In the Name field, type '$InvName'.</span></span>
28. <span data-ttu-id="075b3-150">[式の編集] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="075b3-150">Click Edit formula.</span></span>
29. <span data-ttu-id="075b3-151">[式] フィールドに、[InvoicedAmountEUR] を入力します。</span><span class="sxs-lookup"><span data-stu-id="075b3-151">In the Formula field, enter '"InvoicedAmountEUR"'.</span></span>
30. <span data-ttu-id="075b3-152">[保存] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="075b3-152">Click Save.</span></span>
31. <span data-ttu-id="075b3-153">ページを閉じます。</span><span class="sxs-lookup"><span data-stu-id="075b3-153">Close the page.</span></span>
32. <span data-ttu-id="075b3-154">[OK] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="075b3-154">Click OK.</span></span>
33. <span data-ttu-id="075b3-155">ツリーで、「Intrastat\Data」を選択します。</span><span class="sxs-lookup"><span data-stu-id="075b3-155">In the tree, select 'Intrastat\Data'.</span></span>
34. <span data-ttu-id="075b3-156">「収集したデータ キー名」のフィールドの編集のボタンをクリックします。</span><span class="sxs-lookup"><span data-stu-id="075b3-156">Click Edit button for the ‘Collected data key name’ field</span></span>
35. <span data-ttu-id="075b3-157">[データ ソースの追加] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="075b3-157">Click Add data source.</span></span>
    * <span data-ttu-id="075b3-158">$BlockName</span><span class="sxs-lookup"><span data-stu-id="075b3-158">$BlockName</span></span>  
36. <span data-ttu-id="075b3-159">[保存] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="075b3-159">Click Save.</span></span>
37. <span data-ttu-id="075b3-160">ページを閉じます。</span><span class="sxs-lookup"><span data-stu-id="075b3-160">Close the page.</span></span>
38. <span data-ttu-id="075b3-161">「収集したデータ キー値」のフィールドの編集のボタンをクリックします。</span><span class="sxs-lookup"><span data-stu-id="075b3-161">Click the Edit button for the Collected data key value field.</span></span>
39. <span data-ttu-id="075b3-162">[式] フィールドに、「IF(Intrastat.CommodityRecord.Direction=Direction.Import, "Import", "Export")」を入力します。</span><span class="sxs-lookup"><span data-stu-id="075b3-162">In the Formula field, enter 'IF(Intrastat.CommodityRecord.Direction=Direction.Import, "Import", "Export")'.</span></span>
    * <span data-ttu-id="075b3-163">IF(Intrastat.CommodityRecord.Direction=Direction.Import, "Import", "Export")</span><span class="sxs-lookup"><span data-stu-id="075b3-163">IF(Intrastat.CommodityRecord.Direction=Direction.Import, "Import", "Export")</span></span>  
40. <span data-ttu-id="075b3-164">[保存] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="075b3-164">Click Save.</span></span>
41. <span data-ttu-id="075b3-165">ページを閉じます。</span><span class="sxs-lookup"><span data-stu-id="075b3-165">Close the page.</span></span>
    * <span data-ttu-id="075b3-166">このシーケンスの明細行をカウントします。</span><span class="sxs-lookup"><span data-stu-id="075b3-166">Count the lines of this sequence.</span></span> <span data-ttu-id="075b3-167">結果は、別途さまざまな方向の名称「ブロック」で使用されます。</span><span class="sxs-lookup"><span data-stu-id="075b3-167">The results will be used with the name “block” separately for different directions.</span></span> <span data-ttu-id="075b3-168">値「インポートは」、着荷のイントラスタット トランザクションに使用されます。</span><span class="sxs-lookup"><span data-stu-id="075b3-168">Value “Import” will be used for any arrivals Intrastat transactions.</span></span> <span data-ttu-id="075b3-169">値「エクスポートは」、発送のイントラスタット トランザクションに使用されます。</span><span class="sxs-lookup"><span data-stu-id="075b3-169">The value “Export” will be used for any Intrastat dispatches transactions.</span></span> <span data-ttu-id="075b3-170">これが仮想のExcelワークシートの有効であるとみなします。</span><span class="sxs-lookup"><span data-stu-id="075b3-170">Consider this to be a virtual Excel spreadsheet.</span></span> <span data-ttu-id="075b3-171">各トランザクションについて、最初の列「ブロック」は「インポート」と「エクスポート」が入ります。</span><span class="sxs-lookup"><span data-stu-id="075b3-171">For each transaction a row where the first column “block” is filled with the values “Import” and “Export” accordingly.</span></span>  
42. <span data-ttu-id="075b3-172">ツリーで、「Intrastat\Data: Sequence」を展開します。</span><span class="sxs-lookup"><span data-stu-id="075b3-172">In the tree, expand 'Intrastat\Data: Sequence'.</span></span>
43. <span data-ttu-id="075b3-173">ツリーで、「Intrastat\Data: Sequence\Arrivals?」を選択します。</span><span class="sxs-lookup"><span data-stu-id="075b3-173">In the tree, select 'Intrastat\Data: Sequence\Arrivals?'.</span></span>
44. <span data-ttu-id="075b3-174">「収集したデータ キー名」のフィールドの編集のボタンをクリックします。</span><span class="sxs-lookup"><span data-stu-id="075b3-174">Click Edit button for the ‘Collected data key name’ field.</span></span>
    * <span data-ttu-id="075b3-175">このシーケンスの明細行をカウントします。</span><span class="sxs-lookup"><span data-stu-id="075b3-175">Count the lines of this sequence.</span></span> <span data-ttu-id="075b3-176">結果は、名称「記録」を使用して記憶されます。</span><span class="sxs-lookup"><span data-stu-id="075b3-176">The results will be memorized using the name “record”.</span></span>  
45. <span data-ttu-id="075b3-177">ツリーで、「$RecName」を選択します。</span><span class="sxs-lookup"><span data-stu-id="075b3-177">In the tree, select '$RecName'.</span></span>
46. <span data-ttu-id="075b3-178">[データ ソースの追加] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="075b3-178">Click Add data source.</span></span>
47. <span data-ttu-id="075b3-179">[保存] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="075b3-179">Click Save.</span></span>
48. <span data-ttu-id="075b3-180">ページを閉じます。</span><span class="sxs-lookup"><span data-stu-id="075b3-180">Close the page.</span></span>
49. <span data-ttu-id="075b3-181">「収集したデータ キー値」のフィールドの編集のボタンをクリックします。</span><span class="sxs-lookup"><span data-stu-id="075b3-181">Click Edit button for the ‘Collected data key value’ field</span></span>
50. <span data-ttu-id="075b3-182">[式] フィールドで、「Intrastat.CommodityRecord.CommodityCode」を入力します。</span><span class="sxs-lookup"><span data-stu-id="075b3-182">In the Formula field, enter 'Intrastat.CommodityRecord.CommodityCode'.</span></span>
51. <span data-ttu-id="075b3-183">[保存] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="075b3-183">Click Save.</span></span>
52. <span data-ttu-id="075b3-184">ページを閉じます。</span><span class="sxs-lookup"><span data-stu-id="075b3-184">Close the page.</span></span>
    * <span data-ttu-id="075b3-185">このシーケンスの明細行をカウントします。</span><span class="sxs-lookup"><span data-stu-id="075b3-185">Count the lines of this sequence.</span></span> <span data-ttu-id="075b3-186">結果は、別途さまざまな商品コードについて名称「記録」で使用されます。</span><span class="sxs-lookup"><span data-stu-id="075b3-186">The results will be used with the name “record” separately for different commodity codes.</span></span> <span data-ttu-id="075b3-187">これが仮想のExcelワークシートの有効であるとみなします。</span><span class="sxs-lookup"><span data-stu-id="075b3-187">Consider this to be a virtual Excel spreadsheet.</span></span> <span data-ttu-id="075b3-188">各トランザクションについて、最初の列「ブロック」は「インポート」と「エクスポート」が入り、2番目のブロック「記録」は商品コード値が入ります。</span><span class="sxs-lookup"><span data-stu-id="075b3-188">For each transaction a row where the first column “block” is filled with the values “Import” and “Export” accordingly and the second block “record” is filled with the commodity code value.</span></span>  
53. <span data-ttu-id="075b3-189">ツリーで、「Intrastat\Data: Sequence\Dispatches?」を選択します。</span><span class="sxs-lookup"><span data-stu-id="075b3-189">In the tree, select 'Intrastat\Data: Sequence\Dispatches?'.</span></span>
54. <span data-ttu-id="075b3-190">「収集したデータ キー名」のフィールドの編集のボタンをクリックします。</span><span class="sxs-lookup"><span data-stu-id="075b3-190">Click Edit button for the ‘Collected data key name’ field</span></span>
55. <span data-ttu-id="075b3-191">ツリーで、「$RecName」を選択します。</span><span class="sxs-lookup"><span data-stu-id="075b3-191">In the tree, select '$RecName'.</span></span>
56. <span data-ttu-id="075b3-192">[データ ソースの追加] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="075b3-192">Click Add data source.</span></span>
57. <span data-ttu-id="075b3-193">[保存] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="075b3-193">Click Save.</span></span>
58. <span data-ttu-id="075b3-194">ページを閉じます。</span><span class="sxs-lookup"><span data-stu-id="075b3-194">Close the page.</span></span>
59. <span data-ttu-id="075b3-195">「収集したデータ キー値」のフィールドの編集のボタンをクリックします。</span><span class="sxs-lookup"><span data-stu-id="075b3-195">Click the Edit button for the ‘Collected data key value’ field.</span></span>
60. <span data-ttu-id="075b3-196">[式] フィールドで、「Intrastat.CommodityRecord.CommodityCode」を入力します。</span><span class="sxs-lookup"><span data-stu-id="075b3-196">In the Formula field, enter 'Intrastat.CommodityRecord.CommodityCode'.</span></span>
61. <span data-ttu-id="075b3-197">[保存] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="075b3-197">Click Save.</span></span>
62. <span data-ttu-id="075b3-198">ページを閉じます。</span><span class="sxs-lookup"><span data-stu-id="075b3-198">Close the page.</span></span>
63. <span data-ttu-id="075b3-199">ツリーで、「Intrastat\Data: Sequence\Dispatches: Sequence?」を展開します。</span><span class="sxs-lookup"><span data-stu-id="075b3-199">In the tree, expand 'Intrastat\Data: Sequence\Dispatches: Sequence?'.</span></span>
64. <span data-ttu-id="075b3-200">ツリーで、「Intrastat\Data: Sequence\Dispatches: Sequence?\Record =  Intrastat.CommodityRecord」を展開します。</span><span class="sxs-lookup"><span data-stu-id="075b3-200">In the tree, expand 'Intrastat\Data: Sequence\Dispatches: Sequence?\Record =  Intrastat.CommodityRecord'.</span></span>
65. <span data-ttu-id="075b3-201">[フォーマット] タブをクリックします。</span><span class="sxs-lookup"><span data-stu-id="075b3-201">Click the Format tab.</span></span>
66. <span data-ttu-id="075b3-202">ツリーで、「Intrastat\Data\Dispatches\Record\Invoice amount EUR」を選択します。</span><span class="sxs-lookup"><span data-stu-id="075b3-202">In the tree, select 'Intrastat\Data\Dispatches\Record\Invoice amount EUR'.</span></span>
67. <span data-ttu-id="075b3-203">[マッピング] タブをクリックします。</span><span class="sxs-lookup"><span data-stu-id="075b3-203">Click the Mapping tab.</span></span>
68. <span data-ttu-id="075b3-204">「収集したデータ キー名」のフィールドの編集のボタンをクリックします。</span><span class="sxs-lookup"><span data-stu-id="075b3-204">Click the Edit button for the ‘Collected data key name’ field.</span></span>
69. <span data-ttu-id="075b3-205">ツリーで、「$InvName」を選択します。</span><span class="sxs-lookup"><span data-stu-id="075b3-205">In the tree, select '$InvName'.</span></span>
70. <span data-ttu-id="075b3-206">[データ ソースの追加] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="075b3-206">Click Add data source.</span></span>
71. <span data-ttu-id="075b3-207">[保存] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="075b3-207">Click Save.</span></span>
72. <span data-ttu-id="075b3-208">ページを閉じます。</span><span class="sxs-lookup"><span data-stu-id="075b3-208">Close the page.</span></span>
    * <span data-ttu-id="075b3-209">このシーケンスの明細行について、請求額を集計します。</span><span class="sxs-lookup"><span data-stu-id="075b3-209">Summarize the invoiced amount values for lines of this sequence.</span></span> <span data-ttu-id="075b3-210">結果は、別途さまざまなイントラスタットの指示と商品コードについて名称「記録」で使用されます。</span><span class="sxs-lookup"><span data-stu-id="075b3-210">The results will be used with the name “InvoicedAmountEUR” separately for different Intrastat directions and commodity codes.</span></span> <span data-ttu-id="075b3-211">これが仮想のExcelスプレッドシートであるとみなします。</span><span class="sxs-lookup"><span data-stu-id="075b3-211">Consider this to be a virtual creation in Excel spreadsheet.</span></span> <span data-ttu-id="075b3-212">各トランザクションについて、最初の列「ブロック」は「インポート」と「エクスポート」が入ります。</span><span class="sxs-lookup"><span data-stu-id="075b3-212">For each transaction a row where the first column “block” is filled with the values “Import” and “Export” accordingly.</span></span> <span data-ttu-id="075b3-213">2番目のブロック「記録」は商品コードの値が入り、3番目の列「InvoicedAmountEUR値」は請求金額が入ります。</span><span class="sxs-lookup"><span data-stu-id="075b3-213">The second block “record” is filled with the commodity code value, and the third column “InvoicedAmountEUR” is filled with the invoice amount value.</span></span>  
73. <span data-ttu-id="075b3-214">ツリーで、「Intrastat\Data\Arrivals?」を展開します。</span><span class="sxs-lookup"><span data-stu-id="075b3-214">In the tree, expand 'Intrastat\Data\Arrivals?'.</span></span>
74. <span data-ttu-id="075b3-215">ツリーで、「Intrastat\Data\Arrivals?\Record =  Intrastat.CommodityRecord」を展開します。</span><span class="sxs-lookup"><span data-stu-id="075b3-215">In the tree, expand 'Intrastat\Data\Arrivals?\Record =  Intrastat.CommodityRecord'.</span></span>
75. <span data-ttu-id="075b3-216">[フォーマット] タブをクリックします。</span><span class="sxs-lookup"><span data-stu-id="075b3-216">Click the Format tab.</span></span>
76. <span data-ttu-id="075b3-217">ツリーで、「Intrastat\Data\Dispatches\Record\Invoice amount EUR」を選択します。</span><span class="sxs-lookup"><span data-stu-id="075b3-217">In the tree, select 'Intrastat\Data\Arrivals\Record\Invoice amount EUR'.</span></span>
77. <span data-ttu-id="075b3-218">[マッピング] タブをクリックします。</span><span class="sxs-lookup"><span data-stu-id="075b3-218">Click the Mapping tab.</span></span>
78. <span data-ttu-id="075b3-219">「収集したデータ キー名」のフィールドの編集のボタンをクリックします。</span><span class="sxs-lookup"><span data-stu-id="075b3-219">Click the Edit button for the ‘Collected data key name’ field.</span></span>
79. <span data-ttu-id="075b3-220">ツリーで、「$InvName」を選択します。</span><span class="sxs-lookup"><span data-stu-id="075b3-220">In the tree, select '$InvName'.</span></span>
80. <span data-ttu-id="075b3-221">[データ ソースの追加] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="075b3-221">Click Add data source.</span></span>
81. <span data-ttu-id="075b3-222">[保存] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="075b3-222">Click Save.</span></span>
82. <span data-ttu-id="075b3-223">ページを閉じます。</span><span class="sxs-lookup"><span data-stu-id="075b3-223">Close the page.</span></span>
83. <span data-ttu-id="075b3-224">[保存] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="075b3-224">Click Save.</span></span>
84. <span data-ttu-id="075b3-225">ページを閉じます。</span><span class="sxs-lookup"><span data-stu-id="075b3-225">Close the page.</span></span>


