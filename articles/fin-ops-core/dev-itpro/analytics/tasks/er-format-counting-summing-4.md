---
title: ER 棚卸および集計を行うための形式のコンフィギュレーション (第 4 部 - 形式の実行)
description: このトピックでは、既に生成されたテキスト出力のデータに基づいて棚卸および集計を行うために電子レポート形式を構成する方法について説明します。 (第 4 部)
author: NickSelin
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: ERWorkspace, ERSolutionTable, IntrastatParameters, Intrastat, InventItemIdLookupSimple, IntrastatCommodityLookup, ERFormatMappingRunLogTable, DocuView
audience: Application User
ms.reviewer: kfend
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 2ca8449581edc06016b6e387880aad91087b67f1
ms.sourcegitcommit: 6cb174d1ec8b55946dca4db03d6a3c3f4c6fa2df
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 03/09/2021
ms.locfileid: "5565420"
---
# <a name="er-configure-format-to-do-counting-and-summing-part-4---run-format"></a><span data-ttu-id="c23a8-104">ER 棚卸および集計を行うための形式のコンフィギュレーション (第 4 部 - 形式の実行)</span><span class="sxs-lookup"><span data-stu-id="c23a8-104">ER Configure format to do counting and summing (Part 4 - Run format)</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="c23a8-105">次の手順では、システム管理者または電子レポート開発者のロールに指定されたユーザーが、生成済みのテキスト出力に基づく計算と集計の電子レポート（ER）フォーマットをどのように環境設定するのかについて示します。</span><span class="sxs-lookup"><span data-stu-id="c23a8-105">The following steps explain how a user assigned to the system administrator or electronic reporting developer role can configure an Electronic reporting (ER) format to do counting and summing based on data of the already generated text output.</span></span> <span data-ttu-id="c23a8-106">これらのステップは DEMF 会社で実行できます。</span><span class="sxs-lookup"><span data-stu-id="c23a8-106">These steps can be performed in the DEMF company.</span></span>

<span data-ttu-id="c23a8-107">これらの手順を完了するには、まず「計算と集計を行う ER コンフィギュレーション フォーマット (パート3: 出力を行う計算を使用する)」の手順を完了する必要があります。</span><span class="sxs-lookup"><span data-stu-id="c23a8-107">To complete these steps, you must first complete the steps in the "ER Configure format to do counting and summing (Part 3: Use computations to make the output)" procedure.</span></span>

<span data-ttu-id="c23a8-108">この手順は Dynamics 365 for Operations バージョン 1611 に追加された機能です。</span><span class="sxs-lookup"><span data-stu-id="c23a8-108">This procedure is for a feature that was added in Dynamics 365 for Operations version 1611.</span></span>


## <a name="test-this-configuration-for-generation-of-the-intrastat-reports"></a><span data-ttu-id="c23a8-109">イントラスタット レポートの生成にあたり、この設定をテストします。</span><span class="sxs-lookup"><span data-stu-id="c23a8-109">Test this configuration for generation of the Intrastat reports</span></span>
1. <span data-ttu-id="c23a8-110">[組織管理] > [ワークスペース] > [電子申告] の順に移動します。</span><span class="sxs-lookup"><span data-stu-id="c23a8-110">Go to Organization administration > Workspaces > Electronic reporting.</span></span>
2. <span data-ttu-id="c23a8-111">[コンフィギュレーションをレポートする] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="c23a8-111">Click Reporting configurations.</span></span>
3. <span data-ttu-id="c23a8-112">ツリーで、「Intrastat model」を展開します。</span><span class="sxs-lookup"><span data-stu-id="c23a8-112">In the tree, expand 'Intrastat model'.</span></span>
4. <span data-ttu-id="c23a8-113">ツリーで、「Intrastat model\Intrastat (DE)」を選択します。</span><span class="sxs-lookup"><span data-stu-id="c23a8-113">In the tree, expand 'Intrastat model\Intrastat (DE)'.</span></span>
5. <span data-ttu-id="c23a8-114">ツリーで、「Intrastat model\Intrastat (DE)\Intrastat (DE) with counting & summing'」を選択します。</span><span class="sxs-lookup"><span data-stu-id="c23a8-114">In the tree, select 'Intrastat model\Intrastat (DE)\Intrastat (DE) with counting & summing'.</span></span>
6. <span data-ttu-id="c23a8-115">アクション ウィンドウで、[設定] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="c23a8-115">On the Action Pane, click Configurations.</span></span>
7. <span data-ttu-id="c23a8-116">[ユーザー パラメーター] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="c23a8-116">Click User parameters.</span></span>
8. <span data-ttu-id="c23a8-117">[設定の実行] フィールドで、[はい] を選択します。</span><span class="sxs-lookup"><span data-stu-id="c23a8-117">Select Yes in the Run settings field.</span></span>
9. <span data-ttu-id="c23a8-118">[OK] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="c23a8-118">Click OK.</span></span>
10. <span data-ttu-id="c23a8-119">[編集] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="c23a8-119">Click Edit.</span></span>
11. <span data-ttu-id="c23a8-120">[ドラフトの実行] フィールドで、[はい] を選択します。</span><span class="sxs-lookup"><span data-stu-id="c23a8-120">Select Yes in the Run Draft field.</span></span>
12. <span data-ttu-id="c23a8-121">[保存] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="c23a8-121">Click Save.</span></span>
13. <span data-ttu-id="c23a8-122">[税] > [設定] > [対外貿易] > [対外貿易パラメーター] の順に移動します。</span><span class="sxs-lookup"><span data-stu-id="c23a8-122">Go to Tax > Setup > Foreign trade > Foreign trade parameters.</span></span>
14. <span data-ttu-id="c23a8-123">[電子申告] セクションを展開します。</span><span class="sxs-lookup"><span data-stu-id="c23a8-123">Expand the Electronic reporting section.</span></span>
15. <span data-ttu-id="c23a8-124">[計算と集計のイントラスタット (DE)] コンフィギュレーションを選択します。</span><span class="sxs-lookup"><span data-stu-id="c23a8-124">Select the "Intrastat (DE) with counting & summing" configuration.</span></span>
16. <span data-ttu-id="c23a8-125">[計算と集計のイントラスタット (DE)] コンフィギュレーションを選択します。</span><span class="sxs-lookup"><span data-stu-id="c23a8-125">Select the "Intrastat (DE) with counting & summing" configuration.</span></span>
17. <span data-ttu-id="c23a8-126">[保存] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="c23a8-126">Click Save.</span></span>
18. <span data-ttu-id="c23a8-127">ページを閉じます。</span><span class="sxs-lookup"><span data-stu-id="c23a8-127">Close the page.</span></span>
19. <span data-ttu-id="c23a8-128">[税] > [申告] > [対外貿易] > [イントラスタット] の順に移動します。</span><span class="sxs-lookup"><span data-stu-id="c23a8-128">Go to Tax > Declarations > Foreign trade > Intrastat.</span></span>
20. <span data-ttu-id="c23a8-129">[出力] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="c23a8-129">Click Output.</span></span>
21. <span data-ttu-id="c23a8-130">[レポート] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="c23a8-130">Click Report.</span></span>
    * <span data-ttu-id="c23a8-131">イントラスタット レポートの生成処理を実行します。</span><span class="sxs-lookup"><span data-stu-id="c23a8-131">Run the Intrastat report generation process.</span></span>  
22. <span data-ttu-id="c23a8-132">[開始日] フィールドで、日付を「2000-01-01」に設定します。</span><span class="sxs-lookup"><span data-stu-id="c23a8-132">In the From date field, set the date to '2000-01-01'.</span></span>
    * <span data-ttu-id="c23a8-133">トランザクションのフォームで既存のレポートを含むレポート期間の開始日と終了日を定義します。</span><span class="sxs-lookup"><span data-stu-id="c23a8-133">Define start and end dates for the reporting period that include the existing on the form transactions.</span></span>  
23. <span data-ttu-id="c23a8-134">[終了日] フィールドで、日付を「2022-12-31」に設定します。</span><span class="sxs-lookup"><span data-stu-id="c23a8-134">In the To date field, set the date to '2022-12-31'.</span></span>
    * <span data-ttu-id="c23a8-135">トランザクションのフォームで既存のレポートを含むレポート期間の開始日と終了日を定義します。</span><span class="sxs-lookup"><span data-stu-id="c23a8-135">Define start and end dates for the reporting period that include the existing on the form transactions.</span></span>  
24. <span data-ttu-id="c23a8-136">[指示] フィールドで、「着荷」を選択します。</span><span class="sxs-lookup"><span data-stu-id="c23a8-136">In the Direction field, select 'Arrivals'.</span></span>
25. <span data-ttu-id="c23a8-137">[ファイルの生成] フィールドで、[はい] を選択します。</span><span class="sxs-lookup"><span data-stu-id="c23a8-137">Select Yes in the Generate file field.</span></span>
26. <span data-ttu-id="c23a8-138">[OK] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="c23a8-138">Click OK.</span></span>
    * <span data-ttu-id="c23a8-139">最終的な集計明細行を含む作成済みの出荷を確認します。</span><span class="sxs-lookup"><span data-stu-id="c23a8-139">Review the created output with the summary lines in the end.</span></span>  
27. <span data-ttu-id="c23a8-140">[新規] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="c23a8-140">Click New.</span></span>
28. <span data-ttu-id="c23a8-141">一覧で、選択された行をマークします。</span><span class="sxs-lookup"><span data-stu-id="c23a8-141">In the list, mark the selected row.</span></span>
29. <span data-ttu-id="c23a8-142">[指示] フィールドで、「発送」を選択します。</span><span class="sxs-lookup"><span data-stu-id="c23a8-142">In the Direction field, select 'Dispatches'.</span></span>
30. <span data-ttu-id="c23a8-143">[品目番号] フィールドで、値を入力または選択します。</span><span class="sxs-lookup"><span data-stu-id="c23a8-143">In the Item number field, enter or select a value.</span></span>
31. <span data-ttu-id="c23a8-144">[商品] フィールドで値を入力または選択します。</span><span class="sxs-lookup"><span data-stu-id="c23a8-144">In the Commodity field, enter or select a value.</span></span>
32. <span data-ttu-id="c23a8-145">受領を「10」に設定します。</span><span class="sxs-lookup"><span data-stu-id="c23a8-145">Set Weight to '10'.</span></span>
33. <span data-ttu-id="c23a8-146">請求金額を「10000」に設定します。</span><span class="sxs-lookup"><span data-stu-id="c23a8-146">Set Invoice amount to '10000'.</span></span>
34. <span data-ttu-id="c23a8-147">統計金額を「10000」に設定します。</span><span class="sxs-lookup"><span data-stu-id="c23a8-147">Set Statistical amount to '10000'.</span></span>
35. <span data-ttu-id="c23a8-148">[出力] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="c23a8-148">Click Output.</span></span>
36. <span data-ttu-id="c23a8-149">[レポート] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="c23a8-149">Click Report.</span></span>
37. <span data-ttu-id="c23a8-150">[指示] フィールドで、「発送」を選択します。</span><span class="sxs-lookup"><span data-stu-id="c23a8-150">In the Direction field, select 'Dispatches'.</span></span>
38. <span data-ttu-id="c23a8-151">[OK] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="c23a8-151">Click OK.</span></span>
    * <span data-ttu-id="c23a8-152">最終的な集計明細行を含む作成済みの出荷を確認します。</span><span class="sxs-lookup"><span data-stu-id="c23a8-152">Review the created output with the summary lines in the end.</span></span> <span data-ttu-id="c23a8-153">最初の実行時と比較すると変更されていることに注意してください。</span><span class="sxs-lookup"><span data-stu-id="c23a8-153">Note that it has been changed in comparison to the first run.</span></span>  

## <a name="run-this-configuration-in-debug-mode-to-review-the-collected-counting--summing-data"></a><span data-ttu-id="c23a8-154">デバッグモードでこの設定を実行し、収集した計算 & 集計データを確認します。</span><span class="sxs-lookup"><span data-stu-id="c23a8-154">Run this configuration in debug mode to review the collected counting & summing data</span></span>
1. <span data-ttu-id="c23a8-155">[組織管理] > [電子申告] > [コンフィギュレーション] に移動します。</span><span class="sxs-lookup"><span data-stu-id="c23a8-155">Go to Organization administration > Electronic reporting > Configurations.</span></span>
2. <span data-ttu-id="c23a8-156">ツリーで、「Intrastat model」を展開します。</span><span class="sxs-lookup"><span data-stu-id="c23a8-156">In the tree, expand 'Intrastat model'.</span></span>
3. <span data-ttu-id="c23a8-157">ツリーで、「Intrastat model\Intrastat (DE)」を選択します。</span><span class="sxs-lookup"><span data-stu-id="c23a8-157">In the tree, expand 'Intrastat model\Intrastat (DE)'.</span></span>
4. <span data-ttu-id="c23a8-158">ツリーで、「Intrastat model\Intrastat (DE)\Intrastat (DE) with counting & summing'」を選択します。</span><span class="sxs-lookup"><span data-stu-id="c23a8-158">In the tree, select 'Intrastat model\Intrastat (DE)\Intrastat (DE) with counting & summing'.</span></span>
5. <span data-ttu-id="c23a8-159">アクション ウィンドウで、[設定] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="c23a8-159">On the Action Pane, click Configurations.</span></span>
6. <span data-ttu-id="c23a8-160">[ユーザー パラメーター] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="c23a8-160">Click User parameters.</span></span>
7. <span data-ttu-id="c23a8-161">[デバッグモードの実行] フィールドで、[はい] を選択します。</span><span class="sxs-lookup"><span data-stu-id="c23a8-161">Select Yes in the Run in debug mode field.</span></span>
8. <span data-ttu-id="c23a8-162">[OK] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="c23a8-162">Click OK.</span></span>
9. <span data-ttu-id="c23a8-163">ページを閉じます。</span><span class="sxs-lookup"><span data-stu-id="c23a8-163">Close the page.</span></span>
10. <span data-ttu-id="c23a8-164">[税] > [申告] > [対外貿易] > [イントラスタット] の順に移動します。</span><span class="sxs-lookup"><span data-stu-id="c23a8-164">Go to Tax > Declarations > Foreign trade > Intrastat.</span></span>
11. <span data-ttu-id="c23a8-165">[出力] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="c23a8-165">Click Output.</span></span>
12. <span data-ttu-id="c23a8-166">[レポート] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="c23a8-166">Click Report.</span></span>
13. <span data-ttu-id="c23a8-167">[OK] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="c23a8-167">Click OK.</span></span>
14. <span data-ttu-id="c23a8-168">ページを閉じます。</span><span class="sxs-lookup"><span data-stu-id="c23a8-168">Close the page.</span></span>
15. <span data-ttu-id="c23a8-169">[組織管理] > [電子申告] > [コンフィギュレーション] に移動します。</span><span class="sxs-lookup"><span data-stu-id="c23a8-169">Go to Organization administration > Electronic reporting > Configurations.</span></span>
16. <span data-ttu-id="c23a8-170">ツリーで、「Intrastat model」を展開します。</span><span class="sxs-lookup"><span data-stu-id="c23a8-170">In the tree, expand 'Intrastat model'.</span></span>
17. <span data-ttu-id="c23a8-171">ツリーで、「Intrastat model\Intrastat (DE)」を選択します。</span><span class="sxs-lookup"><span data-stu-id="c23a8-171">In the tree, expand 'Intrastat model\Intrastat (DE)'.</span></span>
18. <span data-ttu-id="c23a8-172">ツリーで、「Intrastat model\Intrastat (DE)\Intrastat (DE) with counting & summing'」を選択します。</span><span class="sxs-lookup"><span data-stu-id="c23a8-172">In the tree, select 'Intrastat model\Intrastat (DE)\Intrastat (DE) with counting & summing'.</span></span>
19. <span data-ttu-id="c23a8-173">[デバッグ ログ] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="c23a8-173">Click Debug logs.</span></span>
    * <span data-ttu-id="c23a8-174">選択した設定の実行に際して、デバッグのログ記録が作成されていることに注意してください。</span><span class="sxs-lookup"><span data-stu-id="c23a8-174">Note that a debug log record has been created for the execution process of the selected configuration.</span></span>  
20. <span data-ttu-id="c23a8-175">[添付] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="c23a8-175">Click Attach.</span></span>
21. <span data-ttu-id="c23a8-176">[開く] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="c23a8-176">Click Open.</span></span>
    * <span data-ttu-id="c23a8-177">選択した設定の実行中に収集された計算と集計の情報を含む作成済みのXMLファイルを確認します。</span><span class="sxs-lookup"><span data-stu-id="c23a8-177">Review the created XML file that contains counting and summing details that were collected during the execution of the selected configuration.</span></span>  



[!INCLUDE[footer-include](../../../../includes/footer-banner.md)]