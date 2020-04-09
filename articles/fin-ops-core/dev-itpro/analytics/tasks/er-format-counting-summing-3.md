---
title: ER 棚卸および集計を行うための形式のコンフィギュレーション (第 3 部 - 出力を作成するための計算の使用)
description: 次の手順では、システム管理者または電子レポート開発者のロールに指定されたユーザーが、生成済みのテキスト出力に基づく計算と集計の電子レポート（ER）フォーマットをどのように環境設定するのかについて示します。
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
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: e8a4965c07c5a084b21da40667747db36530284c
ms.sourcegitcommit: 57e1dafa186fec77ddd8ba9425d238e36e0f0998
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 03/18/2020
ms.locfileid: "3141955"
---
# <a name="er-configure-format-to-do-counting-and-summing-part-3---use-computations-to-make-the-output"></a><span data-ttu-id="0747c-103">ER 棚卸および集計を行うための形式のコンフィギュレーション (第 3 部 - 出力を作成するための計算の使用)</span><span class="sxs-lookup"><span data-stu-id="0747c-103">ER Configure format to do counting and summing (Part 3 - Use computations to make the output)</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="0747c-104">次の手順では、システム管理者または電子レポート開発者のロールに指定されたユーザーが、生成済みのテキスト出力に基づく計算と集計の電子レポート（ER）フォーマットをどのように環境設定するのかについて示します。</span><span class="sxs-lookup"><span data-stu-id="0747c-104">The following steps explain how a user assigned to the system administrator or electronic reporting developer role can configure an Electronic reporting (ER) format to do counting and summing based on data of the already generated text output.</span></span> <span data-ttu-id="0747c-105">これらの手順はどのタイプの企業でも実施できます。</span><span class="sxs-lookup"><span data-stu-id="0747c-105">These steps can be performed in any company.</span></span>

<span data-ttu-id="0747c-106">これらの手順を完了するには、まず 「計算と集計を行うER設定フォーマット（パート2：計算の環境設定）」に記載の手順を完了する必要があります。</span><span class="sxs-lookup"><span data-stu-id="0747c-106">To complete these steps, you must first complete the steps in the "ER Configure format to do counting and summing (Part 2: Configure computations)" procedure.</span></span>

<span data-ttu-id="0747c-107">この手順は Dynamics 365 for Operations バージョン 1611 に追加された機能です。</span><span class="sxs-lookup"><span data-stu-id="0747c-107">This procedure is for a feature that was added in Dynamics 365 for Operations version 1611.</span></span>


## <a name="configure-this-report-to-use-counting-and-summing-info"></a><span data-ttu-id="0747c-108">計算と集計の情報を使用するには、このレポートを設定します。</span><span class="sxs-lookup"><span data-stu-id="0747c-108">Configure this report to use counting and summing info</span></span>
1. <span data-ttu-id="0747c-109">[組織管理] > [ワークスペース] > [電子申告] の順に移動します。</span><span class="sxs-lookup"><span data-stu-id="0747c-109">Go to Organization administration > Workspaces > Electronic reporting.</span></span>
2. <span data-ttu-id="0747c-110">[コンフィギュレーションをレポートする] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="0747c-110">Click Reporting configurations.</span></span>
3. <span data-ttu-id="0747c-111">ツリーで、「Intrastat model」を展開します。</span><span class="sxs-lookup"><span data-stu-id="0747c-111">In the tree, expand 'Intrastat model'.</span></span>
4. <span data-ttu-id="0747c-112">ツリーで、「Intrastat model\Intrastat (DE)」を選択します。</span><span class="sxs-lookup"><span data-stu-id="0747c-112">In the tree, expand 'Intrastat model\Intrastat (DE)'.</span></span>
5. <span data-ttu-id="0747c-113">ツリーで、「Intrastat model\Intrastat (DE)\Intrastat (DE) with counting & summing'」を選択します。</span><span class="sxs-lookup"><span data-stu-id="0747c-113">In the tree, select 'Intrastat model\Intrastat (DE)\Intrastat (DE) with counting & summing'.</span></span>
6. <span data-ttu-id="0747c-114">[デザイナー] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="0747c-114">Click Designer.</span></span>
7. <span data-ttu-id="0747c-115">[マッピング] タブをクリックします。</span><span class="sxs-lookup"><span data-stu-id="0747c-115">Click the Mapping tab.</span></span>
8. <span data-ttu-id="0747c-116">[ルートの追加] をクリックして、ドロップ ダイアログを開きます。</span><span class="sxs-lookup"><span data-stu-id="0747c-116">Click Add root to open the drop dialog.</span></span>
    * <span data-ttu-id="0747c-117">新規データソースを加えて、記憶されたブロックのリストを取得します。</span><span class="sxs-lookup"><span data-stu-id="0747c-117">Add a new data source to get the list of memorized blocks.</span></span>  
9. <span data-ttu-id="0747c-118">ツリーで、[Functions\Calculated field] を選択します。</span><span class="sxs-lookup"><span data-stu-id="0747c-118">In the tree, select 'Functions\Calculated field'.</span></span>
10. <span data-ttu-id="0747c-119">[名称] フィールドに、「$BlocksList」を入力します。</span><span class="sxs-lookup"><span data-stu-id="0747c-119">In the Name field, type '$BlocksList'.</span></span>
    * <span data-ttu-id="0747c-120">$BlocksList</span><span class="sxs-lookup"><span data-stu-id="0747c-120">$BlocksList</span></span>  
11. <span data-ttu-id="0747c-121">[式の編集] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="0747c-121">Click Edit formula.</span></span>
12. <span data-ttu-id="0747c-122">ツリーで、「Data collection functions\COLLECTEDLIST」を選択します。</span><span class="sxs-lookup"><span data-stu-id="0747c-122">In the tree, select 'Data collection functions\COLLECTEDLIST'.</span></span>
13. <span data-ttu-id="0747c-123">[機能の追加] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="0747c-123">Click Add function.</span></span>
14. <span data-ttu-id="0747c-124">[データ ソースの追加] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="0747c-124">Click Add data source.</span></span>
15. <span data-ttu-id="0747c-125">[式] フィールドに、「COLLECTEDLIST('$BlockName', '」を入力します。</span><span class="sxs-lookup"><span data-stu-id="0747c-125">In the Formula field, enter 'COLLECTEDLIST('$BlockName', '.</span></span>
    * <span data-ttu-id="0747c-126">COLLECTEDLIST('$BlockName',</span><span class="sxs-lookup"><span data-stu-id="0747c-126">COLLECTEDLIST('$BlockName',</span></span>  
16. <span data-ttu-id="0747c-127">[式] フィールドに、「COLLECTEDLIST('$BlockName', "\*")」を入力します。</span><span class="sxs-lookup"><span data-stu-id="0747c-127">In the Formula field, enter 'COLLECTEDLIST('$BlockName', "\*")'.</span></span>
    * <span data-ttu-id="0747c-128">COLLECTEDLIST('$BlockName', "\*")</span><span class="sxs-lookup"><span data-stu-id="0747c-128">COLLECTEDLIST('$BlockName', "\*")</span></span>  
17. <span data-ttu-id="0747c-129">[保存] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="0747c-129">Click Save.</span></span>
    * <span data-ttu-id="0747c-130">パターン 「\*」 は、すべてのブロックがこの記録のリストに含まれることを意味します。</span><span class="sxs-lookup"><span data-stu-id="0747c-130">The pattern "\*" means that all blocks will be included to the list for this record.</span></span>  
18. <span data-ttu-id="0747c-131">ページを閉じます。</span><span class="sxs-lookup"><span data-stu-id="0747c-131">Close the page.</span></span>
19. <span data-ttu-id="0747c-132">[OK] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="0747c-132">Click OK.</span></span>
20. <span data-ttu-id="0747c-133">[フォーマット] タブをクリックします。</span><span class="sxs-lookup"><span data-stu-id="0747c-133">Click the Format tab.</span></span>
21. <span data-ttu-id="0747c-134">ツリーで、「Intrastat\Data」を選択します。</span><span class="sxs-lookup"><span data-stu-id="0747c-134">In the tree, select 'Intrastat\Data'.</span></span>
22. <span data-ttu-id="0747c-135">[追加] をクリックしてドロップ ダイアログを開きます。</span><span class="sxs-lookup"><span data-stu-id="0747c-135">Click Add to open the drop dialog.</span></span>
23. <span data-ttu-id="0747c-136">ツリーで、「Text\Sequence」を選択します。</span><span class="sxs-lookup"><span data-stu-id="0747c-136">In the tree, select 'Text\Sequence'.</span></span>
24. <span data-ttu-id="0747c-137">[名称] フィールドに、「Totals by blocks」を入力します。</span><span class="sxs-lookup"><span data-stu-id="0747c-137">In the Name field, type 'Totals by blocks'.</span></span>
    * <span data-ttu-id="0747c-138">ブロック別の合計</span><span class="sxs-lookup"><span data-stu-id="0747c-138">Totals by blocks</span></span>  
25. <span data-ttu-id="0747c-139">[特殊文字] フィールドでは、「New line - Windows (CR LF)」を選択します。</span><span class="sxs-lookup"><span data-stu-id="0747c-139">In the Special characters field, select 'New line - Windows (CR LF)'.</span></span>
26. <span data-ttu-id="0747c-140">[OK] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="0747c-140">Click OK.</span></span>
27. <span data-ttu-id="0747c-141">ツリーで、「Intrastat\Data\Totals by blocks」を選択します。</span><span class="sxs-lookup"><span data-stu-id="0747c-141">In the tree, select 'Intrastat\Data\Totals by blocks'.</span></span>
28. <span data-ttu-id="0747c-142">[追加] をクリックしてドロップ ダイアログを開きます。</span><span class="sxs-lookup"><span data-stu-id="0747c-142">Click Add to open the drop dialog.</span></span>
29. <span data-ttu-id="0747c-143">ツリーで、[Text\String] を選択します。</span><span class="sxs-lookup"><span data-stu-id="0747c-143">In the tree, select 'Text\String'.</span></span>
30. <span data-ttu-id="0747c-144">[名称] フィールドで、「ブロックコード」と入力します。</span><span class="sxs-lookup"><span data-stu-id="0747c-144">In the Name field, type 'Block code'.</span></span>
    * <span data-ttu-id="0747c-145">ブロック コード</span><span class="sxs-lookup"><span data-stu-id="0747c-145">Block code</span></span>  
31. <span data-ttu-id="0747c-146">[OK] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="0747c-146">Click OK.</span></span>
32. <span data-ttu-id="0747c-147">[ストリングの追加」をクリックします。</span><span class="sxs-lookup"><span data-stu-id="0747c-147">Click Add String.</span></span>
33. <span data-ttu-id="0747c-148">[名称] フィールドに、「Lines counting」と入力します。</span><span class="sxs-lookup"><span data-stu-id="0747c-148">In the Name field, type 'Lines counting'.</span></span>
    * <span data-ttu-id="0747c-149">計算の明細行</span><span class="sxs-lookup"><span data-stu-id="0747c-149">Lines counting</span></span>  
34. <span data-ttu-id="0747c-150">[OK] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="0747c-150">Click OK.</span></span>
35. <span data-ttu-id="0747c-151">[ストリングの追加」をクリックします。</span><span class="sxs-lookup"><span data-stu-id="0747c-151">Click Add String.</span></span>
36. <span data-ttu-id="0747c-152">[名前] フィールドに、「Total amount」を入力します。</span><span class="sxs-lookup"><span data-stu-id="0747c-152">In the Name field, type 'Total amount'.</span></span>
    * <span data-ttu-id="0747c-153">合計時間</span><span class="sxs-lookup"><span data-stu-id="0747c-153">Total amount</span></span>  
37. <span data-ttu-id="0747c-154">[OK] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="0747c-154">Click OK.</span></span>
38. <span data-ttu-id="0747c-155">[マッピング] タブをクリックします。</span><span class="sxs-lookup"><span data-stu-id="0747c-155">Click the Mapping tab.</span></span>
39. <span data-ttu-id="0747c-156">ツリーで、「$BlocksList」を選択します。</span><span class="sxs-lookup"><span data-stu-id="0747c-156">In the tree, select '$BlocksList'.</span></span>
40. <span data-ttu-id="0747c-157">[バインド] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="0747c-157">Click Bind.</span></span>
    * <span data-ttu-id="0747c-158">記憶された各ブロックの集計行を作成します。</span><span class="sxs-lookup"><span data-stu-id="0747c-158">Create a summary line for each memorized block.</span></span>  
41. <span data-ttu-id="0747c-159">[フォーマット] タブをクリックします。</span><span class="sxs-lookup"><span data-stu-id="0747c-159">Click the Format tab.</span></span>
42. <span data-ttu-id="0747c-160">ツリーで、「Intrastat\Data\Totals by blocks\Block code」を選択します。</span><span class="sxs-lookup"><span data-stu-id="0747c-160">In the tree, select 'Intrastat\Data\Totals by blocks\Block code'.</span></span>
43. <span data-ttu-id="0747c-161">[マッピング] タブをクリックします。</span><span class="sxs-lookup"><span data-stu-id="0747c-161">Click the Mapping tab.</span></span>
44. <span data-ttu-id="0747c-162">[式の編集] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="0747c-162">Click Edit formula.</span></span>
45. <span data-ttu-id="0747c-163">[式] フィールドに、「"Block id: " & 」を入力します。</span><span class="sxs-lookup"><span data-stu-id="0747c-163">In the Formula field, enter '"Block id: " & '.</span></span>
    * <span data-ttu-id="0747c-164">"ブロック id: " &</span><span class="sxs-lookup"><span data-stu-id="0747c-164">"Block id: " &</span></span>  
46. <span data-ttu-id="0747c-165">ツリーで、「$BlocksList」を展開します。</span><span class="sxs-lookup"><span data-stu-id="0747c-165">In the tree, expand '$BlocksList'.</span></span>
47. <span data-ttu-id="0747c-166">ツリーで、「$BlocksList\Value」を選択します</span><span class="sxs-lookup"><span data-stu-id="0747c-166">In the tree, select '$BlocksList\Value'.</span></span>
48. <span data-ttu-id="0747c-167">[データ ソースの追加] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="0747c-167">Click Add data source.</span></span>
49. <span data-ttu-id="0747c-168">[保存] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="0747c-168">Click Save.</span></span>
50. <span data-ttu-id="0747c-169">ページを閉じます。</span><span class="sxs-lookup"><span data-stu-id="0747c-169">Close the page.</span></span>
51. <span data-ttu-id="0747c-170">[フォーマット] タブをクリックします。</span><span class="sxs-lookup"><span data-stu-id="0747c-170">Click the Format tab.</span></span>
52. <span data-ttu-id="0747c-171">ツリーで、「Intrastat\Data\Totals by blocks\Lines counting」を選択します。</span><span class="sxs-lookup"><span data-stu-id="0747c-171">In the tree, select 'Intrastat\Data\Totals by blocks\Lines counting'.</span></span>
53. <span data-ttu-id="0747c-172">[マッピング] タブをクリックします。</span><span class="sxs-lookup"><span data-stu-id="0747c-172">Click the Mapping tab.</span></span>
54. <span data-ttu-id="0747c-173">[式の編集] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="0747c-173">Click Edit formula.</span></span>
    * <span data-ttu-id="0747c-174">このレポートに表示される各ブロックの行数の出荷を作成します。</span><span class="sxs-lookup"><span data-stu-id="0747c-174">Create output for the number of lines for each block presented in this report.</span></span>  
55. <span data-ttu-id="0747c-175">[式] フィールドで、「"このブロックの行数： " & 」を入力します。</span><span class="sxs-lookup"><span data-stu-id="0747c-175">In the Formula field, enter '"Number of lines in this block: " & '.</span></span>
    * <span data-ttu-id="0747c-176">"このブロックの行数: " &</span><span class="sxs-lookup"><span data-stu-id="0747c-176">"Number of lines in this block: " &</span></span>  
56. <span data-ttu-id="0747c-177">[式] フィールドで、「"このブロックの行数： " & TEXT(」を入力します。</span><span class="sxs-lookup"><span data-stu-id="0747c-177">In the Formula field, enter '"Number of lines in this block: " & TEXT('.</span></span>
    * <span data-ttu-id="0747c-178">"このブロックの行数: " & TEXT(</span><span class="sxs-lookup"><span data-stu-id="0747c-178">"Number of lines in this block: " & TEXT(</span></span>  
57. <span data-ttu-id="0747c-179">ツリーで、「Data collection functions\COUNTIFS」を選択します。</span><span class="sxs-lookup"><span data-stu-id="0747c-179">In the tree, select 'Data collection functions\COUNTIFS'.</span></span>
58. <span data-ttu-id="0747c-180">[機能の追加] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="0747c-180">Click Add function.</span></span>
59. <span data-ttu-id="0747c-181">[データ ソースの追加] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="0747c-181">Click Add data source.</span></span>
60. <span data-ttu-id="0747c-182">[式] フィールドで、「"このブロックの行数: " & TEXT(COUNTIFS('$BlockName', 」を入力します。</span><span class="sxs-lookup"><span data-stu-id="0747c-182">In the Formula field, enter '"Number of lines in this block: " & TEXT(COUNTIFS('$BlockName', '.</span></span>
    * <span data-ttu-id="0747c-183">"このブロックの行数: " & TEXT(COUNTIFS('$BlockName',</span><span class="sxs-lookup"><span data-stu-id="0747c-183">"Number of lines in this block: " & TEXT(COUNTIFS('$BlockName',</span></span>  
61. <span data-ttu-id="0747c-184">ツリーで、「$BlocksList」を展開します。</span><span class="sxs-lookup"><span data-stu-id="0747c-184">In the tree, expand '$BlocksList'.</span></span>
62. <span data-ttu-id="0747c-185">ツリーで、「$BlocksList\Value」を選択します</span><span class="sxs-lookup"><span data-stu-id="0747c-185">In the tree, select '$BlocksList\Value'.</span></span>
63. <span data-ttu-id="0747c-186">[データ ソースの追加] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="0747c-186">Click Add data source.</span></span>
64. <span data-ttu-id="0747c-187">[式] フィールドで、「"このブロックの行数: " & TEXT(COUNTIFS('$BlockName', '$BlocksList'.Value, 」を入力します。</span><span class="sxs-lookup"><span data-stu-id="0747c-187">In the Formula field, enter '"Number of lines in this block: " & TEXT(COUNTIFS('$BlockName', '$BlocksList'.Value, '.</span></span>
    * <span data-ttu-id="0747c-188">"このブロックの行数: " & TEXT(COUNTIFS('$BlockName', '$BlocksList'.Value,</span><span class="sxs-lookup"><span data-stu-id="0747c-188">"Number of lines in this block: " & TEXT(COUNTIFS('$BlockName', '$BlocksList'.Value,</span></span>  
65. <span data-ttu-id="0747c-189">ツリーで、「$RecName」を選択します。</span><span class="sxs-lookup"><span data-stu-id="0747c-189">In the tree, select '$RecName'.</span></span>
66. <span data-ttu-id="0747c-190">[データ ソースの追加] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="0747c-190">Click Add data source.</span></span>
67. <span data-ttu-id="0747c-191">[式] フィールドで、「"このブロックの行数: " & TEXT(COUNTIFS('$BlockName', '$BlocksList'.Value, '$RecName', "\*"))」を入力します。</span><span class="sxs-lookup"><span data-stu-id="0747c-191">In the Formula field, enter '"Number of lines in this block: " & TEXT(COUNTIFS('$BlockName', '$BlocksList'.Value, '$RecName', "\*"))'.</span></span>
    * <span data-ttu-id="0747c-192">"このブロックの行数: " & TEXT(COUNTIFS('$BlockName', '$BlocksList'.Value, '$RecName', "\*"))</span><span class="sxs-lookup"><span data-stu-id="0747c-192">"Number of lines in this block: " & TEXT(COUNTIFS('$BlockName', '$BlocksList'.Value, '$RecName', "\*"))</span></span>  
68. <span data-ttu-id="0747c-193">[保存] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="0747c-193">Click Save.</span></span>
69. <span data-ttu-id="0747c-194">ページを閉じます。</span><span class="sxs-lookup"><span data-stu-id="0747c-194">Close the page.</span></span>
70. <span data-ttu-id="0747c-195">[フォーマット] タブをクリックします。</span><span class="sxs-lookup"><span data-stu-id="0747c-195">Click the Format tab.</span></span>
71. <span data-ttu-id="0747c-196">ツリーで、「Intrastat\Data\Totals by blocks\Total amount」を選択します。</span><span class="sxs-lookup"><span data-stu-id="0747c-196">In the tree, select 'Intrastat\Data\Totals by blocks\Total amount'.</span></span>
72. <span data-ttu-id="0747c-197">[マッピング] タブをクリックします。</span><span class="sxs-lookup"><span data-stu-id="0747c-197">Click the Mapping tab.</span></span>
73. <span data-ttu-id="0747c-198">[式の編集] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="0747c-198">Click Edit formula.</span></span>
    * <span data-ttu-id="0747c-199">このレポートで指定された各ブロックの合計請求金額となる出荷を作成します。</span><span class="sxs-lookup"><span data-stu-id="0747c-199">Create output that will be the total of the invoiced amount for each block presented in this report.</span></span>  
74. <span data-ttu-id="0747c-200">[式] フィールドで、「"合計請求金額: " & TEXT(SUMIFS('$InvName', '$BlockName', '$BlocksList'.Value, '$RecName', "\*"))」を入力します。</span><span class="sxs-lookup"><span data-stu-id="0747c-200">In the Formula field, enter '"Sum of invoiced amount: " & TEXT(SUMIFS('$InvName', '$BlockName', '$BlocksList'.Value, '$RecName', "\*"))'.</span></span>
    * <span data-ttu-id="0747c-201">"合計請求金額: " & TEXT(SUMIFS('$InvName', '$BlockName', '$BlocksList'.Value, '$RecName', "\*"))</span><span class="sxs-lookup"><span data-stu-id="0747c-201">"Sum of invoiced amount: " & TEXT(SUMIFS('$InvName', '$BlockName', '$BlocksList'.Value, '$RecName', "\*"))</span></span>  
75. <span data-ttu-id="0747c-202">[保存] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="0747c-202">Click Save.</span></span>
76. <span data-ttu-id="0747c-203">ページを閉じます。</span><span class="sxs-lookup"><span data-stu-id="0747c-203">Close the page.</span></span>
77. <span data-ttu-id="0747c-204">[保存] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="0747c-204">Click Save.</span></span>
78. <span data-ttu-id="0747c-205">ページを閉じます。</span><span class="sxs-lookup"><span data-stu-id="0747c-205">Close the page.</span></span>

