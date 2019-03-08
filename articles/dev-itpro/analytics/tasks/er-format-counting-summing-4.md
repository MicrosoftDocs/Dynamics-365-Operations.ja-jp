---
title: ER 棚卸および集計を行うための形式のコンフィギュレーション (第 4 部 - 形式の実行)
description: 次の手順では、システム管理者または電子レポート開発者のロールに指定されたユーザーが、生成済みのテキスト出力に基づく計算と集計の電子レポート（ER）フォーマットをどのように環境設定するのかについて示します。
author: NickSelin
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ERWorkspace, ERSolutionTable, IntrastatParameters, Intrastat, InventItemIdLookupSimple, IntrastatCommodityLookup, ERFormatMappingRunLogTable, DocuView
audience: Application User
ms.reviewer: kfend
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 17989b7fa2baf14472ec19a041cb5ce7e5c0380d
ms.sourcegitcommit: 0f530e5f72a40f383868957a6b5cb0e446e4c795
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 01/29/2019
ms.locfileid: "336201"
---
# <a name="er-configure-format-to-do-counting-and-summing-part-4-run-format"></a><span data-ttu-id="f8872-103">ER 棚卸および集計を行うための形式のコンフィギュレーション (パート 4: 形式の実行)</span><span class="sxs-lookup"><span data-stu-id="f8872-103">ER Configure format to do counting and summing (Part 4: Run format)</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="f8872-104">次の手順では、システム管理者または電子レポート開発者のロールに指定されたユーザーが、生成済みのテキスト出力に基づく計算と集計の電子レポート（ER）フォーマットをどのように環境設定するのかについて示します。</span><span class="sxs-lookup"><span data-stu-id="f8872-104">The following steps explain how a user assigned to the system administrator or electronic reporting developer role can configure an Electronic reporting (ER) format to do counting and summing based on data of the already generated text output.</span></span> <span data-ttu-id="f8872-105">これらのステップは DEMF 会社で実行できます。</span><span class="sxs-lookup"><span data-stu-id="f8872-105">These steps can be performed in the DEMF company.</span></span>

<span data-ttu-id="f8872-106">これらの手順を完了するには、まず「計算と集計を行うER設定フォーマット（パート3：出荷のための計算）」の手順を完了する必要があります。</span><span class="sxs-lookup"><span data-stu-id="f8872-106">To complete these steps, you must first complete the steps in the “ER Configure format to do counting and summing (Part 3: Use computations to make the output)” procedure.</span></span>

<span data-ttu-id="f8872-107">この手順は Dynamics 365 for Operations バージョン 1611 に追加された機能です。</span><span class="sxs-lookup"><span data-stu-id="f8872-107">This procedure is for a feature that was added in Dynamics 365 for Operations version 1611.</span></span>


## <a name="test-this-configuration-for-generation-of-the-intrastat-reports"></a><span data-ttu-id="f8872-108">イントラスタット レポートの生成にあたり、この設定をテストします。</span><span class="sxs-lookup"><span data-stu-id="f8872-108">Test this configuration for generation of the Intrastat reports</span></span>
1. <span data-ttu-id="f8872-109">[組織管理] > [ワークスペース] > [電子申告] の順に移動します。</span><span class="sxs-lookup"><span data-stu-id="f8872-109">Go to Organization administration > Workspaces > Electronic reporting.</span></span>
2. <span data-ttu-id="f8872-110">[コンフィギュレーションをレポートする] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="f8872-110">Click Reporting configurations.</span></span>
3. <span data-ttu-id="f8872-111">ツリーで、「Intrastat model」を展開します。</span><span class="sxs-lookup"><span data-stu-id="f8872-111">In the tree, expand 'Intrastat model'.</span></span>
4. <span data-ttu-id="f8872-112">ツリーで、「Intrastat model\Intrastat (DE)」を選択します。</span><span class="sxs-lookup"><span data-stu-id="f8872-112">In the tree, expand 'Intrastat model\Intrastat (DE)'.</span></span>
5. <span data-ttu-id="f8872-113">ツリーで、「Intrastat model\Intrastat (DE)\Intrastat (DE) with counting & summing'」を選択します。</span><span class="sxs-lookup"><span data-stu-id="f8872-113">In the tree, select 'Intrastat model\Intrastat (DE)\Intrastat (DE) with counting & summing'.</span></span>
6. <span data-ttu-id="f8872-114">アクション ウィンドウで、[設定] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="f8872-114">On the Action Pane, click Configurations.</span></span>
7. <span data-ttu-id="f8872-115">[ユーザー パラメーター] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="f8872-115">Click User parameters.</span></span>
8. <span data-ttu-id="f8872-116">[設定の実行] フィールドで、[はい] を選択します。</span><span class="sxs-lookup"><span data-stu-id="f8872-116">Select Yes in the Run settings field.</span></span>
9. <span data-ttu-id="f8872-117">[OK] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="f8872-117">Click OK.</span></span>
10. <span data-ttu-id="f8872-118">[編集] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="f8872-118">Click Edit.</span></span>
11. <span data-ttu-id="f8872-119">[ドラフトの実行] フィールドで、[はい] を選択します。</span><span class="sxs-lookup"><span data-stu-id="f8872-119">Select Yes in the Run Draft field.</span></span>
12. <span data-ttu-id="f8872-120">[保存] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="f8872-120">Click Save.</span></span>
13. <span data-ttu-id="f8872-121">[税] > [設定] > [対外貿易] > [対外貿易パラメーター] の順に移動します。</span><span class="sxs-lookup"><span data-stu-id="f8872-121">Go to Tax > Setup > Foreign trade > Foreign trade parameters.</span></span>
14. <span data-ttu-id="f8872-122">[電子申告] セクションを展開します。</span><span class="sxs-lookup"><span data-stu-id="f8872-122">Expand the Electronic reporting section.</span></span>
15. <span data-ttu-id="f8872-123">[計算 & 集計を含むイントラスタット (DE)] の設定を選択します。</span><span class="sxs-lookup"><span data-stu-id="f8872-123">Select the “Intrastat (DE) with counting & summing” configuration.</span></span>
16. <span data-ttu-id="f8872-124">[計算 & 集計を含むイントラスタット (DE)] の設定を選択します。</span><span class="sxs-lookup"><span data-stu-id="f8872-124">Select the “Intrastat (DE) with counting & summing” configuration.</span></span>
17. <span data-ttu-id="f8872-125">[保存] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="f8872-125">Click Save.</span></span>
18. <span data-ttu-id="f8872-126">ページを閉じます。</span><span class="sxs-lookup"><span data-stu-id="f8872-126">Close the page.</span></span>
19. <span data-ttu-id="f8872-127">[税] > [申告] > [対外貿易] > [イントラスタット] の順に移動します。</span><span class="sxs-lookup"><span data-stu-id="f8872-127">Go to Tax > Declarations > Foreign trade > Intrastat.</span></span>
20. <span data-ttu-id="f8872-128">[出力] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="f8872-128">Click Output.</span></span>
21. <span data-ttu-id="f8872-129">[レポート] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="f8872-129">Click Report.</span></span>
    * <span data-ttu-id="f8872-130">イントラスタット レポートの生成処理を実行します。</span><span class="sxs-lookup"><span data-stu-id="f8872-130">Run the Intrastat report generation process.</span></span>  
22. <span data-ttu-id="f8872-131">[開始日] フィールドで、日付を「2000-01-01」に設定します。</span><span class="sxs-lookup"><span data-stu-id="f8872-131">In the From date field, set the date to '2000-01-01'.</span></span>
    * <span data-ttu-id="f8872-132">トランザクションのフォームで既存のレポートを含むレポート期間の開始日と終了日を定義します。</span><span class="sxs-lookup"><span data-stu-id="f8872-132">Define start and end dates for the reporting period that include the existing on the form transactions.</span></span>  
23. <span data-ttu-id="f8872-133">[終了日] フィールドで、日付を「2022-12-31」に設定します。</span><span class="sxs-lookup"><span data-stu-id="f8872-133">In the To date field, set the date to '2022-12-31'.</span></span>
    * <span data-ttu-id="f8872-134">トランザクションのフォームで既存のレポートを含むレポート期間の開始日と終了日を定義します。</span><span class="sxs-lookup"><span data-stu-id="f8872-134">Define start and end dates for the reporting period that include the existing on the form transactions.</span></span>  
24. <span data-ttu-id="f8872-135">[指示] フィールドで、「着荷」を選択します。</span><span class="sxs-lookup"><span data-stu-id="f8872-135">In the Direction field, select 'Arrivals'.</span></span>
25. <span data-ttu-id="f8872-136">[ファイルの生成] フィールドで、[はい] を選択します。</span><span class="sxs-lookup"><span data-stu-id="f8872-136">Select Yes in the Generate file field.</span></span>
26. <span data-ttu-id="f8872-137">[OK] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="f8872-137">Click OK.</span></span>
    * <span data-ttu-id="f8872-138">最終的な集計明細行を含む作成済みの出荷を確認します。</span><span class="sxs-lookup"><span data-stu-id="f8872-138">Review the created output with the summary lines in the end.</span></span>  
27. <span data-ttu-id="f8872-139">[新規] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="f8872-139">Click New.</span></span>
28. <span data-ttu-id="f8872-140">一覧で、選択された行をマークします。</span><span class="sxs-lookup"><span data-stu-id="f8872-140">In the list, mark the selected row.</span></span>
29. <span data-ttu-id="f8872-141">[指示] フィールドで、「発送」を選択します。</span><span class="sxs-lookup"><span data-stu-id="f8872-141">In the Direction field, select 'Dispatches'.</span></span>
30. <span data-ttu-id="f8872-142">[品目番号] フィールドで、値を入力または選択します。</span><span class="sxs-lookup"><span data-stu-id="f8872-142">In the Item number field, enter or select a value.</span></span>
31. <span data-ttu-id="f8872-143">[商品] フィールドで値を入力または選択します。</span><span class="sxs-lookup"><span data-stu-id="f8872-143">In the Commodity field, enter or select a value.</span></span>
32. <span data-ttu-id="f8872-144">受領を「10」に設定します。</span><span class="sxs-lookup"><span data-stu-id="f8872-144">Set Weight to '10'.</span></span>
33. <span data-ttu-id="f8872-145">請求金額を「10000」に設定します。</span><span class="sxs-lookup"><span data-stu-id="f8872-145">Set Invoice amount to '10000'.</span></span>
34. <span data-ttu-id="f8872-146">統計金額を「10000」に設定します。</span><span class="sxs-lookup"><span data-stu-id="f8872-146">Set Statistical amount to '10000'.</span></span>
35. <span data-ttu-id="f8872-147">[出力] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="f8872-147">Click Output.</span></span>
36. <span data-ttu-id="f8872-148">[レポート] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="f8872-148">Click Report.</span></span>
37. <span data-ttu-id="f8872-149">[指示] フィールドで、「発送」を選択します。</span><span class="sxs-lookup"><span data-stu-id="f8872-149">In the Direction field, select 'Dispatches'.</span></span>
38. <span data-ttu-id="f8872-150">[OK] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="f8872-150">Click OK.</span></span>
    * <span data-ttu-id="f8872-151">最終的な集計明細行を含む作成済みの出荷を確認します。</span><span class="sxs-lookup"><span data-stu-id="f8872-151">Review the created output with the summary lines in the end.</span></span> <span data-ttu-id="f8872-152">最初の実行時と比較すると変更されていることに注意してください。</span><span class="sxs-lookup"><span data-stu-id="f8872-152">Note that it has been changed in comparison to the first run.</span></span>  

## <a name="run-this-configuration-in-debug-mode-to-review-the-collected-counting--summing-data"></a><span data-ttu-id="f8872-153">デバッグモードでこの設定を実行し、収集した計算 & 集計データを確認します。</span><span class="sxs-lookup"><span data-stu-id="f8872-153">Run this configuration in debug mode to review the collected counting & summing data</span></span>
1. <span data-ttu-id="f8872-154">[組織管理] > [電子申告] > [コンフィギュレーション] に移動します。</span><span class="sxs-lookup"><span data-stu-id="f8872-154">Go to Organization administration > Electronic reporting > Configurations.</span></span>
2. <span data-ttu-id="f8872-155">ツリーで、「Intrastat model」を展開します。</span><span class="sxs-lookup"><span data-stu-id="f8872-155">In the tree, expand 'Intrastat model'.</span></span>
3. <span data-ttu-id="f8872-156">ツリーで、「Intrastat model\Intrastat (DE)」を選択します。</span><span class="sxs-lookup"><span data-stu-id="f8872-156">In the tree, expand 'Intrastat model\Intrastat (DE)'.</span></span>
4. <span data-ttu-id="f8872-157">ツリーで、「Intrastat model\Intrastat (DE)\Intrastat (DE) with counting & summing'」を選択します。</span><span class="sxs-lookup"><span data-stu-id="f8872-157">In the tree, select 'Intrastat model\Intrastat (DE)\Intrastat (DE) with counting & summing'.</span></span>
5. <span data-ttu-id="f8872-158">アクション ウィンドウで、[設定] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="f8872-158">On the Action Pane, click Configurations.</span></span>
6. <span data-ttu-id="f8872-159">[ユーザー パラメーター] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="f8872-159">Click User parameters.</span></span>
7. <span data-ttu-id="f8872-160">[デバッグモードの実行] フィールドで、[はい] を選択します。</span><span class="sxs-lookup"><span data-stu-id="f8872-160">Select Yes in the Run in debug mode field.</span></span>
8. <span data-ttu-id="f8872-161">[OK] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="f8872-161">Click OK.</span></span>
9. <span data-ttu-id="f8872-162">ページを閉じます。</span><span class="sxs-lookup"><span data-stu-id="f8872-162">Close the page.</span></span>
10. <span data-ttu-id="f8872-163">[税] > [申告] > [対外貿易] > [イントラスタット] の順に移動します。</span><span class="sxs-lookup"><span data-stu-id="f8872-163">Go to Tax > Declarations > Foreign trade > Intrastat.</span></span>
11. <span data-ttu-id="f8872-164">[出力] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="f8872-164">Click Output.</span></span>
12. <span data-ttu-id="f8872-165">[レポート] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="f8872-165">Click Report.</span></span>
13. <span data-ttu-id="f8872-166">[OK] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="f8872-166">Click OK.</span></span>
14. <span data-ttu-id="f8872-167">ページを閉じます。</span><span class="sxs-lookup"><span data-stu-id="f8872-167">Close the page.</span></span>
15. <span data-ttu-id="f8872-168">[組織管理] > [電子申告] > [コンフィギュレーション] に移動します。</span><span class="sxs-lookup"><span data-stu-id="f8872-168">Go to Organization administration > Electronic reporting > Configurations.</span></span>
16. <span data-ttu-id="f8872-169">ツリーで、「Intrastat model」を展開します。</span><span class="sxs-lookup"><span data-stu-id="f8872-169">In the tree, expand 'Intrastat model'.</span></span>
17. <span data-ttu-id="f8872-170">ツリーで、「Intrastat model\Intrastat (DE)」を選択します。</span><span class="sxs-lookup"><span data-stu-id="f8872-170">In the tree, expand 'Intrastat model\Intrastat (DE)'.</span></span>
18. <span data-ttu-id="f8872-171">ツリーで、「Intrastat model\Intrastat (DE)\Intrastat (DE) with counting & summing'」を選択します。</span><span class="sxs-lookup"><span data-stu-id="f8872-171">In the tree, select 'Intrastat model\Intrastat (DE)\Intrastat (DE) with counting & summing'.</span></span>
19. <span data-ttu-id="f8872-172">[デバッグ ログ] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="f8872-172">Click Debug logs.</span></span>
    * <span data-ttu-id="f8872-173">選択した設定の実行に際して、デバッグのログ記録が作成されていることに注意してください。</span><span class="sxs-lookup"><span data-stu-id="f8872-173">Note that a debug log record has been created for the execution process of the selected configuration.</span></span>  
20. <span data-ttu-id="f8872-174">[添付] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="f8872-174">Click Attach.</span></span>
21. <span data-ttu-id="f8872-175">[開く] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="f8872-175">Click Open.</span></span>
    * <span data-ttu-id="f8872-176">選択した設定の実行中に収集された計算と集計の情報を含む作成済みのXMLファイルを確認します。</span><span class="sxs-lookup"><span data-stu-id="f8872-176">Review the created XML file that contains counting and summing details that were collected during the execution of the selected configuration.</span></span>  

