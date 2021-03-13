---
title: ER 棚卸および集計を行うための形式のコンフィギュレーション (第 3 部 - 出力を作成するための計算の使用)
description: このトピックでは、既に生成されたテキスト出力のデータに基づいて棚卸および集計を行うために電子レポート形式を構成する方法について説明します。 (第 3 部)
author: NickSelin
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ERWorkspace, ERSolutionTable, EROperationDesigner, ERDataSourceAddDropDialog, ERExpressionDesignerFormula, ERComponentTypeDropDialog
audience: Application User
ms.reviewer: kfend
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 4a69dd28051d8e98643eb95c663525075bed8dec
ms.sourcegitcommit: 5192cfaedfd861faea63d8954d7bcc500608a225
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 01/30/2021
ms.locfileid: "5092975"
---
# <a name="er-configure-format-to-do-counting-and-summing-part-3---use-computations-to-make-the-output"></a><span data-ttu-id="d9df5-104">ER 棚卸および集計を行うための形式のコンフィギュレーション (第 3 部 - 出力を作成するための計算の使用)</span><span class="sxs-lookup"><span data-stu-id="d9df5-104">ER Configure format to do counting and summing (Part 3 - Use computations to make the output)</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="d9df5-105">次の手順では、システム管理者または電子レポート開発者のロールに指定されたユーザーが、生成済みのテキスト出力に基づく計算と集計の電子レポート（ER）フォーマットをどのように環境設定するのかについて示します。</span><span class="sxs-lookup"><span data-stu-id="d9df5-105">The following steps explain how a user assigned to the system administrator or electronic reporting developer role can configure an Electronic reporting (ER) format to do counting and summing based on data of the already generated text output.</span></span> <span data-ttu-id="d9df5-106">これらの手順はどのタイプの企業でも実施できます。</span><span class="sxs-lookup"><span data-stu-id="d9df5-106">These steps can be performed in any company.</span></span>

<span data-ttu-id="d9df5-107">これらの手順を完了するには、まず 「計算と集計を行うER設定フォーマット（パート2：計算の環境設定）」に記載の手順を完了する必要があります。</span><span class="sxs-lookup"><span data-stu-id="d9df5-107">To complete these steps, you must first complete the steps in the "ER Configure format to do counting and summing (Part 2: Configure computations)" procedure.</span></span>

<span data-ttu-id="d9df5-108">この手順は Dynamics 365 for Operations バージョン 1611 に追加された機能です。</span><span class="sxs-lookup"><span data-stu-id="d9df5-108">This procedure is for a feature that was added in Dynamics 365 for Operations version 1611.</span></span>


## <a name="configure-this-report-to-use-counting-and-summing-info"></a><span data-ttu-id="d9df5-109">計算と集計の情報を使用するには、このレポートを設定します。</span><span class="sxs-lookup"><span data-stu-id="d9df5-109">Configure this report to use counting and summing info</span></span>
1. <span data-ttu-id="d9df5-110">[組織管理] > [ワークスペース] > [電子申告] の順に移動します。</span><span class="sxs-lookup"><span data-stu-id="d9df5-110">Go to Organization administration > Workspaces > Electronic reporting.</span></span>
2. <span data-ttu-id="d9df5-111">[コンフィギュレーションをレポートする] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="d9df5-111">Click Reporting configurations.</span></span>
3. <span data-ttu-id="d9df5-112">ツリーで、「Intrastat model」を展開します。</span><span class="sxs-lookup"><span data-stu-id="d9df5-112">In the tree, expand 'Intrastat model'.</span></span>
4. <span data-ttu-id="d9df5-113">ツリーで、「Intrastat model\Intrastat (DE)」を選択します。</span><span class="sxs-lookup"><span data-stu-id="d9df5-113">In the tree, expand 'Intrastat model\Intrastat (DE)'.</span></span>
5. <span data-ttu-id="d9df5-114">ツリーで、「Intrastat model\Intrastat (DE)\Intrastat (DE) with counting & summing'」を選択します。</span><span class="sxs-lookup"><span data-stu-id="d9df5-114">In the tree, select 'Intrastat model\Intrastat (DE)\Intrastat (DE) with counting & summing'.</span></span>
6. <span data-ttu-id="d9df5-115">[デザイナー] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="d9df5-115">Click Designer.</span></span>
7. <span data-ttu-id="d9df5-116">[マッピング] タブをクリックします。</span><span class="sxs-lookup"><span data-stu-id="d9df5-116">Click the Mapping tab.</span></span>
8. <span data-ttu-id="d9df5-117">[ルートの追加] をクリックして、ドロップ ダイアログを開きます。</span><span class="sxs-lookup"><span data-stu-id="d9df5-117">Click Add root to open the drop dialog.</span></span>
    * <span data-ttu-id="d9df5-118">新規データソースを加えて、記憶されたブロックのリストを取得します。</span><span class="sxs-lookup"><span data-stu-id="d9df5-118">Add a new data source to get the list of memorized blocks.</span></span>  
9. <span data-ttu-id="d9df5-119">ツリーで、[Functions\Calculated field] を選択します。</span><span class="sxs-lookup"><span data-stu-id="d9df5-119">In the tree, select 'Functions\Calculated field'.</span></span>
10. <span data-ttu-id="d9df5-120">[名称] フィールドに、「$BlocksList」を入力します。</span><span class="sxs-lookup"><span data-stu-id="d9df5-120">In the Name field, type '$BlocksList'.</span></span>
    * <span data-ttu-id="d9df5-121">$BlocksList</span><span class="sxs-lookup"><span data-stu-id="d9df5-121">$BlocksList</span></span>  
11. <span data-ttu-id="d9df5-122">[式の編集] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="d9df5-122">Click Edit formula.</span></span>
12. <span data-ttu-id="d9df5-123">ツリーで、「Data collection functions\COLLECTEDLIST」を選択します。</span><span class="sxs-lookup"><span data-stu-id="d9df5-123">In the tree, select 'Data collection functions\COLLECTEDLIST'.</span></span>
13. <span data-ttu-id="d9df5-124">[機能の追加] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="d9df5-124">Click Add function.</span></span>
14. <span data-ttu-id="d9df5-125">[データ ソースの追加] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="d9df5-125">Click Add data source.</span></span>
15. <span data-ttu-id="d9df5-126">[式] フィールドに、「COLLECTEDLIST('$BlockName', '」を入力します。</span><span class="sxs-lookup"><span data-stu-id="d9df5-126">In the Formula field, enter 'COLLECTEDLIST('$BlockName', '.</span></span>
    * <span data-ttu-id="d9df5-127">COLLECTEDLIST('$BlockName',</span><span class="sxs-lookup"><span data-stu-id="d9df5-127">COLLECTEDLIST('$BlockName',</span></span>  
16. <span data-ttu-id="d9df5-128">[式] フィールドに、「COLLECTEDLIST('$BlockName', "\*")」を入力します。</span><span class="sxs-lookup"><span data-stu-id="d9df5-128">In the Formula field, enter 'COLLECTEDLIST('$BlockName', "\*")'.</span></span>
    * <span data-ttu-id="d9df5-129">COLLECTEDLIST('$BlockName', "\*")</span><span class="sxs-lookup"><span data-stu-id="d9df5-129">COLLECTEDLIST('$BlockName', "\*")</span></span>  
17. <span data-ttu-id="d9df5-130">[保存] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="d9df5-130">Click Save.</span></span>
    * <span data-ttu-id="d9df5-131">パターン 「\*」 は、すべてのブロックがこの記録のリストに含まれることを意味します。</span><span class="sxs-lookup"><span data-stu-id="d9df5-131">The pattern "\*" means that all blocks will be included to the list for this record.</span></span>  
18. <span data-ttu-id="d9df5-132">ページを閉じます。</span><span class="sxs-lookup"><span data-stu-id="d9df5-132">Close the page.</span></span>
19. <span data-ttu-id="d9df5-133">[OK] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="d9df5-133">Click OK.</span></span>
20. <span data-ttu-id="d9df5-134">[フォーマット] タブをクリックします。</span><span class="sxs-lookup"><span data-stu-id="d9df5-134">Click the Format tab.</span></span>
21. <span data-ttu-id="d9df5-135">ツリーで、「Intrastat\Data」を選択します。</span><span class="sxs-lookup"><span data-stu-id="d9df5-135">In the tree, select 'Intrastat\Data'.</span></span>
22. <span data-ttu-id="d9df5-136">[追加] をクリックしてドロップ ダイアログを開きます。</span><span class="sxs-lookup"><span data-stu-id="d9df5-136">Click Add to open the drop dialog.</span></span>
23. <span data-ttu-id="d9df5-137">ツリーで、「Text\Sequence」を選択します。</span><span class="sxs-lookup"><span data-stu-id="d9df5-137">In the tree, select 'Text\Sequence'.</span></span>
24. <span data-ttu-id="d9df5-138">[名称] フィールドに、「Totals by blocks」を入力します。</span><span class="sxs-lookup"><span data-stu-id="d9df5-138">In the Name field, type 'Totals by blocks'.</span></span>
    * <span data-ttu-id="d9df5-139">ブロック別の合計</span><span class="sxs-lookup"><span data-stu-id="d9df5-139">Totals by blocks</span></span>  
25. <span data-ttu-id="d9df5-140">[特殊文字] フィールドでは、「New line - Windows (CR LF)」を選択します。</span><span class="sxs-lookup"><span data-stu-id="d9df5-140">In the Special characters field, select 'New line - Windows (CR LF)'.</span></span>
26. <span data-ttu-id="d9df5-141">[OK] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="d9df5-141">Click OK.</span></span>
27. <span data-ttu-id="d9df5-142">ツリーで、「Intrastat\Data\Totals by blocks」を選択します。</span><span class="sxs-lookup"><span data-stu-id="d9df5-142">In the tree, select 'Intrastat\Data\Totals by blocks'.</span></span>
28. <span data-ttu-id="d9df5-143">[追加] をクリックしてドロップ ダイアログを開きます。</span><span class="sxs-lookup"><span data-stu-id="d9df5-143">Click Add to open the drop dialog.</span></span>
29. <span data-ttu-id="d9df5-144">ツリーで、[Text\String] を選択します。</span><span class="sxs-lookup"><span data-stu-id="d9df5-144">In the tree, select 'Text\String'.</span></span>
30. <span data-ttu-id="d9df5-145">[名称] フィールドで、「ブロックコード」と入力します。</span><span class="sxs-lookup"><span data-stu-id="d9df5-145">In the Name field, type 'Block code'.</span></span>
    * <span data-ttu-id="d9df5-146">ブロック コード</span><span class="sxs-lookup"><span data-stu-id="d9df5-146">Block code</span></span>  
31. <span data-ttu-id="d9df5-147">[OK] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="d9df5-147">Click OK.</span></span>
32. <span data-ttu-id="d9df5-148">[ストリングの追加] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="d9df5-148">Click Add String.</span></span>
33. <span data-ttu-id="d9df5-149">[名称] フィールドに、「Lines counting」と入力します。</span><span class="sxs-lookup"><span data-stu-id="d9df5-149">In the Name field, type 'Lines counting'.</span></span>
    * <span data-ttu-id="d9df5-150">計算の明細行</span><span class="sxs-lookup"><span data-stu-id="d9df5-150">Lines counting</span></span>  
34. <span data-ttu-id="d9df5-151">[OK] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="d9df5-151">Click OK.</span></span>
35. <span data-ttu-id="d9df5-152">[ストリングの追加] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="d9df5-152">Click Add String.</span></span>
36. <span data-ttu-id="d9df5-153">[名前] フィールドに、「Total amount」を入力します。</span><span class="sxs-lookup"><span data-stu-id="d9df5-153">In the Name field, type 'Total amount'.</span></span>
    * <span data-ttu-id="d9df5-154">合計時間</span><span class="sxs-lookup"><span data-stu-id="d9df5-154">Total amount</span></span>  
37. <span data-ttu-id="d9df5-155">[OK] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="d9df5-155">Click OK.</span></span>
38. <span data-ttu-id="d9df5-156">[マッピング] タブをクリックします。</span><span class="sxs-lookup"><span data-stu-id="d9df5-156">Click the Mapping tab.</span></span>
39. <span data-ttu-id="d9df5-157">ツリーで、「$BlocksList」を選択します。</span><span class="sxs-lookup"><span data-stu-id="d9df5-157">In the tree, select '$BlocksList'.</span></span>
40. <span data-ttu-id="d9df5-158">[バインド] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="d9df5-158">Click Bind.</span></span>
    * <span data-ttu-id="d9df5-159">記憶された各ブロックの集計行を作成します。</span><span class="sxs-lookup"><span data-stu-id="d9df5-159">Create a summary line for each memorized block.</span></span>  
41. <span data-ttu-id="d9df5-160">[フォーマット] タブをクリックします。</span><span class="sxs-lookup"><span data-stu-id="d9df5-160">Click the Format tab.</span></span>
42. <span data-ttu-id="d9df5-161">ツリーで、「Intrastat\Data\Totals by blocks\Block code」を選択します。</span><span class="sxs-lookup"><span data-stu-id="d9df5-161">In the tree, select 'Intrastat\Data\Totals by blocks\Block code'.</span></span>
43. <span data-ttu-id="d9df5-162">[マッピング] タブをクリックします。</span><span class="sxs-lookup"><span data-stu-id="d9df5-162">Click the Mapping tab.</span></span>
44. <span data-ttu-id="d9df5-163">[式の編集] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="d9df5-163">Click Edit formula.</span></span>
45. <span data-ttu-id="d9df5-164">[式] フィールドに、「"Block id: " & 」を入力します。</span><span class="sxs-lookup"><span data-stu-id="d9df5-164">In the Formula field, enter '"Block id: " & '.</span></span>
    * <span data-ttu-id="d9df5-165">"ブロック id: " &</span><span class="sxs-lookup"><span data-stu-id="d9df5-165">"Block id: " &</span></span>  
46. <span data-ttu-id="d9df5-166">ツリーで、「$BlocksList」を展開します。</span><span class="sxs-lookup"><span data-stu-id="d9df5-166">In the tree, expand '$BlocksList'.</span></span>
47. <span data-ttu-id="d9df5-167">ツリーで、「$BlocksList\Value」を選択します</span><span class="sxs-lookup"><span data-stu-id="d9df5-167">In the tree, select '$BlocksList\Value'.</span></span>
48. <span data-ttu-id="d9df5-168">[データ ソースの追加] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="d9df5-168">Click Add data source.</span></span>
49. <span data-ttu-id="d9df5-169">[保存] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="d9df5-169">Click Save.</span></span>
50. <span data-ttu-id="d9df5-170">ページを閉じます。</span><span class="sxs-lookup"><span data-stu-id="d9df5-170">Close the page.</span></span>
51. <span data-ttu-id="d9df5-171">[フォーマット] タブをクリックします。</span><span class="sxs-lookup"><span data-stu-id="d9df5-171">Click the Format tab.</span></span>
52. <span data-ttu-id="d9df5-172">ツリーで、「Intrastat\Data\Totals by blocks\Lines counting」を選択します。</span><span class="sxs-lookup"><span data-stu-id="d9df5-172">In the tree, select 'Intrastat\Data\Totals by blocks\Lines counting'.</span></span>
53. <span data-ttu-id="d9df5-173">[マッピング] タブをクリックします。</span><span class="sxs-lookup"><span data-stu-id="d9df5-173">Click the Mapping tab.</span></span>
54. <span data-ttu-id="d9df5-174">[式の編集] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="d9df5-174">Click Edit formula.</span></span>
    * <span data-ttu-id="d9df5-175">このレポートに表示される各ブロックの行数の出荷を作成します。</span><span class="sxs-lookup"><span data-stu-id="d9df5-175">Create output for the number of lines for each block presented in this report.</span></span>  
55. <span data-ttu-id="d9df5-176">[式] フィールドで、「"このブロックの行数： " & 」を入力します。</span><span class="sxs-lookup"><span data-stu-id="d9df5-176">In the Formula field, enter '"Number of lines in this block: " & '.</span></span>
    * <span data-ttu-id="d9df5-177">"このブロックの行数: " &</span><span class="sxs-lookup"><span data-stu-id="d9df5-177">"Number of lines in this block: " &</span></span>  
56. <span data-ttu-id="d9df5-178">[式] フィールドで、「"このブロックの行数： " & TEXT(」を入力します。</span><span class="sxs-lookup"><span data-stu-id="d9df5-178">In the Formula field, enter '"Number of lines in this block: " & TEXT('.</span></span>
    * <span data-ttu-id="d9df5-179">"このブロックの行数: " & TEXT(</span><span class="sxs-lookup"><span data-stu-id="d9df5-179">"Number of lines in this block: " & TEXT(</span></span>  
57. <span data-ttu-id="d9df5-180">ツリーで、「Data collection functions\COUNTIFS」を選択します。</span><span class="sxs-lookup"><span data-stu-id="d9df5-180">In the tree, select 'Data collection functions\COUNTIFS'.</span></span>
58. <span data-ttu-id="d9df5-181">[機能の追加] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="d9df5-181">Click Add function.</span></span>
59. <span data-ttu-id="d9df5-182">[データ ソースの追加] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="d9df5-182">Click Add data source.</span></span>
60. <span data-ttu-id="d9df5-183">[式] フィールドで、「"このブロックの行数: " & TEXT(COUNTIFS('$BlockName', 」を入力します。</span><span class="sxs-lookup"><span data-stu-id="d9df5-183">In the Formula field, enter '"Number of lines in this block: " & TEXT(COUNTIFS('$BlockName', '.</span></span>
    * <span data-ttu-id="d9df5-184">"このブロックの行数: " & TEXT(COUNTIFS('$BlockName',</span><span class="sxs-lookup"><span data-stu-id="d9df5-184">"Number of lines in this block: " & TEXT(COUNTIFS('$BlockName',</span></span>  
61. <span data-ttu-id="d9df5-185">ツリーで、「$BlocksList」を展開します。</span><span class="sxs-lookup"><span data-stu-id="d9df5-185">In the tree, expand '$BlocksList'.</span></span>
62. <span data-ttu-id="d9df5-186">ツリーで、「$BlocksList\Value」を選択します</span><span class="sxs-lookup"><span data-stu-id="d9df5-186">In the tree, select '$BlocksList\Value'.</span></span>
63. <span data-ttu-id="d9df5-187">[データ ソースの追加] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="d9df5-187">Click Add data source.</span></span>
64. <span data-ttu-id="d9df5-188">[式] フィールドで、「"このブロックの行数: " & TEXT(COUNTIFS('$BlockName', '$BlocksList'.Value, 」を入力します。</span><span class="sxs-lookup"><span data-stu-id="d9df5-188">In the Formula field, enter '"Number of lines in this block: " & TEXT(COUNTIFS('$BlockName', '$BlocksList'.Value, '.</span></span>
    * <span data-ttu-id="d9df5-189">"このブロックの行数: " & TEXT(COUNTIFS('$BlockName', '$BlocksList'.Value,</span><span class="sxs-lookup"><span data-stu-id="d9df5-189">"Number of lines in this block: " & TEXT(COUNTIFS('$BlockName', '$BlocksList'.Value,</span></span>  
65. <span data-ttu-id="d9df5-190">ツリーで、「$RecName」を選択します。</span><span class="sxs-lookup"><span data-stu-id="d9df5-190">In the tree, select '$RecName'.</span></span>
66. <span data-ttu-id="d9df5-191">[データ ソースの追加] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="d9df5-191">Click Add data source.</span></span>
67. <span data-ttu-id="d9df5-192">[式] フィールドで、「"このブロックの行数: " & TEXT(COUNTIFS('$BlockName', '$BlocksList'.Value, '$RecName', "\*"))」を入力します。</span><span class="sxs-lookup"><span data-stu-id="d9df5-192">In the Formula field, enter '"Number of lines in this block: " & TEXT(COUNTIFS('$BlockName', '$BlocksList'.Value, '$RecName', "\*"))'.</span></span>
    * <span data-ttu-id="d9df5-193">"このブロックの行数: " & TEXT(COUNTIFS('$BlockName', '$BlocksList'.Value, '$RecName', "\*"))</span><span class="sxs-lookup"><span data-stu-id="d9df5-193">"Number of lines in this block: " & TEXT(COUNTIFS('$BlockName', '$BlocksList'.Value, '$RecName', "\*"))</span></span>  
68. <span data-ttu-id="d9df5-194">[保存] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="d9df5-194">Click Save.</span></span>
69. <span data-ttu-id="d9df5-195">ページを閉じます。</span><span class="sxs-lookup"><span data-stu-id="d9df5-195">Close the page.</span></span>
70. <span data-ttu-id="d9df5-196">[フォーマット] タブをクリックします。</span><span class="sxs-lookup"><span data-stu-id="d9df5-196">Click the Format tab.</span></span>
71. <span data-ttu-id="d9df5-197">ツリーで、「Intrastat\Data\Totals by blocks\Total amount」を選択します。</span><span class="sxs-lookup"><span data-stu-id="d9df5-197">In the tree, select 'Intrastat\Data\Totals by blocks\Total amount'.</span></span>
72. <span data-ttu-id="d9df5-198">[マッピング] タブをクリックします。</span><span class="sxs-lookup"><span data-stu-id="d9df5-198">Click the Mapping tab.</span></span>
73. <span data-ttu-id="d9df5-199">[式の編集] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="d9df5-199">Click Edit formula.</span></span>
    * <span data-ttu-id="d9df5-200">このレポートで指定された各ブロックの合計請求金額となる出荷を作成します。</span><span class="sxs-lookup"><span data-stu-id="d9df5-200">Create output that will be the total of the invoiced amount for each block presented in this report.</span></span>  
74. <span data-ttu-id="d9df5-201">[式] フィールドで、「"合計請求金額: " & TEXT(SUMIFS('$InvName', '$BlockName', '$BlocksList'.Value, '$RecName', "\*"))」を入力します。</span><span class="sxs-lookup"><span data-stu-id="d9df5-201">In the Formula field, enter '"Sum of invoiced amount: " & TEXT(SUMIFS('$InvName', '$BlockName', '$BlocksList'.Value, '$RecName', "\*"))'.</span></span>
    * <span data-ttu-id="d9df5-202">"合計請求金額: " & TEXT(SUMIFS('$InvName', '$BlockName', '$BlocksList'.Value, '$RecName', "\*"))</span><span class="sxs-lookup"><span data-stu-id="d9df5-202">"Sum of invoiced amount: " & TEXT(SUMIFS('$InvName', '$BlockName', '$BlocksList'.Value, '$RecName', "\*"))</span></span>  
75. <span data-ttu-id="d9df5-203">[保存] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="d9df5-203">Click Save.</span></span>
76. <span data-ttu-id="d9df5-204">ページを閉じます。</span><span class="sxs-lookup"><span data-stu-id="d9df5-204">Close the page.</span></span>
77. <span data-ttu-id="d9df5-205">[保存] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="d9df5-205">Click Save.</span></span>
78. <span data-ttu-id="d9df5-206">ページを閉じます。</span><span class="sxs-lookup"><span data-stu-id="d9df5-206">Close the page.</span></span>

