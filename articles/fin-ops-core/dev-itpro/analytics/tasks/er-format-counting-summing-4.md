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
ms.openlocfilehash: b89d08d8f6a4223eb592ffa2b918504839e5287b
ms.sourcegitcommit: 57e1dafa186fec77ddd8ba9425d238e36e0f0998
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 03/18/2020
ms.locfileid: "3142412"
---
# <a name="er-configure-format-to-do-counting-and-summing-part-4---run-format"></a><span data-ttu-id="8b855-103">ER 棚卸および集計を行うための形式のコンフィギュレーション (第 4 部 - 形式の実行)</span><span class="sxs-lookup"><span data-stu-id="8b855-103">ER Configure format to do counting and summing (Part 4 - Run format)</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="8b855-104">次の手順では、システム管理者または電子レポート開発者のロールに指定されたユーザーが、生成済みのテキスト出力に基づく計算と集計の電子レポート（ER）フォーマットをどのように環境設定するのかについて示します。</span><span class="sxs-lookup"><span data-stu-id="8b855-104">The following steps explain how a user assigned to the system administrator or electronic reporting developer role can configure an Electronic reporting (ER) format to do counting and summing based on data of the already generated text output.</span></span> <span data-ttu-id="8b855-105">これらのステップは DEMF 会社で実行できます。</span><span class="sxs-lookup"><span data-stu-id="8b855-105">These steps can be performed in the DEMF company.</span></span>

<span data-ttu-id="8b855-106">これらの手順を完了するには、まず「計算と集計を行う ER コンフィギュレーション フォーマット (パート3: 出力を行う計算を使用する)」の手順を完了する必要があります。</span><span class="sxs-lookup"><span data-stu-id="8b855-106">To complete these steps, you must first complete the steps in the "ER Configure format to do counting and summing (Part 3: Use computations to make the output)" procedure.</span></span>

<span data-ttu-id="8b855-107">この手順は Dynamics 365 for Operations バージョン 1611 に追加された機能です。</span><span class="sxs-lookup"><span data-stu-id="8b855-107">This procedure is for a feature that was added in Dynamics 365 for Operations version 1611.</span></span>


## <a name="test-this-configuration-for-generation-of-the-intrastat-reports"></a><span data-ttu-id="8b855-108">イントラスタット レポートの生成にあたり、この設定をテストします。</span><span class="sxs-lookup"><span data-stu-id="8b855-108">Test this configuration for generation of the Intrastat reports</span></span>
1. <span data-ttu-id="8b855-109">[組織管理] > [ワークスペース] > [電子申告] の順に移動します。</span><span class="sxs-lookup"><span data-stu-id="8b855-109">Go to Organization administration > Workspaces > Electronic reporting.</span></span>
2. <span data-ttu-id="8b855-110">[コンフィギュレーションをレポートする] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="8b855-110">Click Reporting configurations.</span></span>
3. <span data-ttu-id="8b855-111">ツリーで、「Intrastat model」を展開します。</span><span class="sxs-lookup"><span data-stu-id="8b855-111">In the tree, expand 'Intrastat model'.</span></span>
4. <span data-ttu-id="8b855-112">ツリーで、「Intrastat model\Intrastat (DE)」を選択します。</span><span class="sxs-lookup"><span data-stu-id="8b855-112">In the tree, expand 'Intrastat model\Intrastat (DE)'.</span></span>
5. <span data-ttu-id="8b855-113">ツリーで、「Intrastat model\Intrastat (DE)\Intrastat (DE) with counting & summing'」を選択します。</span><span class="sxs-lookup"><span data-stu-id="8b855-113">In the tree, select 'Intrastat model\Intrastat (DE)\Intrastat (DE) with counting & summing'.</span></span>
6. <span data-ttu-id="8b855-114">アクション ウィンドウで、[設定] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="8b855-114">On the Action Pane, click Configurations.</span></span>
7. <span data-ttu-id="8b855-115">[ユーザー パラメーター] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="8b855-115">Click User parameters.</span></span>
8. <span data-ttu-id="8b855-116">[設定の実行] フィールドで、[はい] を選択します。</span><span class="sxs-lookup"><span data-stu-id="8b855-116">Select Yes in the Run settings field.</span></span>
9. <span data-ttu-id="8b855-117">[OK] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="8b855-117">Click OK.</span></span>
10. <span data-ttu-id="8b855-118">[編集] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="8b855-118">Click Edit.</span></span>
11. <span data-ttu-id="8b855-119">[ドラフトの実行] フィールドで、[はい] を選択します。</span><span class="sxs-lookup"><span data-stu-id="8b855-119">Select Yes in the Run Draft field.</span></span>
12. <span data-ttu-id="8b855-120">[保存] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="8b855-120">Click Save.</span></span>
13. <span data-ttu-id="8b855-121">[税] > [設定] > [対外貿易] > [対外貿易パラメーター] の順に移動します。</span><span class="sxs-lookup"><span data-stu-id="8b855-121">Go to Tax > Setup > Foreign trade > Foreign trade parameters.</span></span>
14. <span data-ttu-id="8b855-122">[電子申告] セクションを展開します。</span><span class="sxs-lookup"><span data-stu-id="8b855-122">Expand the Electronic reporting section.</span></span>
15. <span data-ttu-id="8b855-123">[計算と集計のイントラスタット (DE)] コンフィギュレーションを選択します。</span><span class="sxs-lookup"><span data-stu-id="8b855-123">Select the "Intrastat (DE) with counting & summing" configuration.</span></span>
16. <span data-ttu-id="8b855-124">[計算と集計のイントラスタット (DE)] コンフィギュレーションを選択します。</span><span class="sxs-lookup"><span data-stu-id="8b855-124">Select the "Intrastat (DE) with counting & summing" configuration.</span></span>
17. <span data-ttu-id="8b855-125">[保存] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="8b855-125">Click Save.</span></span>
18. <span data-ttu-id="8b855-126">ページを閉じます。</span><span class="sxs-lookup"><span data-stu-id="8b855-126">Close the page.</span></span>
19. <span data-ttu-id="8b855-127">[税] > [申告] > [対外貿易] > [イントラスタット] の順に移動します。</span><span class="sxs-lookup"><span data-stu-id="8b855-127">Go to Tax > Declarations > Foreign trade > Intrastat.</span></span>
20. <span data-ttu-id="8b855-128">[出力] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="8b855-128">Click Output.</span></span>
21. <span data-ttu-id="8b855-129">[レポート] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="8b855-129">Click Report.</span></span>
    * <span data-ttu-id="8b855-130">イントラスタット レポートの生成処理を実行します。</span><span class="sxs-lookup"><span data-stu-id="8b855-130">Run the Intrastat report generation process.</span></span>  
22. <span data-ttu-id="8b855-131">[開始日] フィールドで、日付を「2000-01-01」に設定します。</span><span class="sxs-lookup"><span data-stu-id="8b855-131">In the From date field, set the date to '2000-01-01'.</span></span>
    * <span data-ttu-id="8b855-132">トランザクションのフォームで既存のレポートを含むレポート期間の開始日と終了日を定義します。</span><span class="sxs-lookup"><span data-stu-id="8b855-132">Define start and end dates for the reporting period that include the existing on the form transactions.</span></span>  
23. <span data-ttu-id="8b855-133">[終了日] フィールドで、日付を「2022-12-31」に設定します。</span><span class="sxs-lookup"><span data-stu-id="8b855-133">In the To date field, set the date to '2022-12-31'.</span></span>
    * <span data-ttu-id="8b855-134">トランザクションのフォームで既存のレポートを含むレポート期間の開始日と終了日を定義します。</span><span class="sxs-lookup"><span data-stu-id="8b855-134">Define start and end dates for the reporting period that include the existing on the form transactions.</span></span>  
24. <span data-ttu-id="8b855-135">[指示] フィールドで、「着荷」を選択します。</span><span class="sxs-lookup"><span data-stu-id="8b855-135">In the Direction field, select 'Arrivals'.</span></span>
25. <span data-ttu-id="8b855-136">[ファイルの生成] フィールドで、[はい] を選択します。</span><span class="sxs-lookup"><span data-stu-id="8b855-136">Select Yes in the Generate file field.</span></span>
26. <span data-ttu-id="8b855-137">[OK] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="8b855-137">Click OK.</span></span>
    * <span data-ttu-id="8b855-138">最終的な集計明細行を含む作成済みの出荷を確認します。</span><span class="sxs-lookup"><span data-stu-id="8b855-138">Review the created output with the summary lines in the end.</span></span>  
27. <span data-ttu-id="8b855-139">[新規] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="8b855-139">Click New.</span></span>
28. <span data-ttu-id="8b855-140">一覧で、選択された行をマークします。</span><span class="sxs-lookup"><span data-stu-id="8b855-140">In the list, mark the selected row.</span></span>
29. <span data-ttu-id="8b855-141">[指示] フィールドで、「発送」を選択します。</span><span class="sxs-lookup"><span data-stu-id="8b855-141">In the Direction field, select 'Dispatches'.</span></span>
30. <span data-ttu-id="8b855-142">[品目番号] フィールドで、値を入力または選択します。</span><span class="sxs-lookup"><span data-stu-id="8b855-142">In the Item number field, enter or select a value.</span></span>
31. <span data-ttu-id="8b855-143">[商品] フィールドで値を入力または選択します。</span><span class="sxs-lookup"><span data-stu-id="8b855-143">In the Commodity field, enter or select a value.</span></span>
32. <span data-ttu-id="8b855-144">受領を「10」に設定します。</span><span class="sxs-lookup"><span data-stu-id="8b855-144">Set Weight to '10'.</span></span>
33. <span data-ttu-id="8b855-145">請求金額を「10000」に設定します。</span><span class="sxs-lookup"><span data-stu-id="8b855-145">Set Invoice amount to '10000'.</span></span>
34. <span data-ttu-id="8b855-146">統計金額を「10000」に設定します。</span><span class="sxs-lookup"><span data-stu-id="8b855-146">Set Statistical amount to '10000'.</span></span>
35. <span data-ttu-id="8b855-147">[出力] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="8b855-147">Click Output.</span></span>
36. <span data-ttu-id="8b855-148">[レポート] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="8b855-148">Click Report.</span></span>
37. <span data-ttu-id="8b855-149">[指示] フィールドで、「発送」を選択します。</span><span class="sxs-lookup"><span data-stu-id="8b855-149">In the Direction field, select 'Dispatches'.</span></span>
38. <span data-ttu-id="8b855-150">[OK] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="8b855-150">Click OK.</span></span>
    * <span data-ttu-id="8b855-151">最終的な集計明細行を含む作成済みの出荷を確認します。</span><span class="sxs-lookup"><span data-stu-id="8b855-151">Review the created output with the summary lines in the end.</span></span> <span data-ttu-id="8b855-152">最初の実行時と比較すると変更されていることに注意してください。</span><span class="sxs-lookup"><span data-stu-id="8b855-152">Note that it has been changed in comparison to the first run.</span></span>  

## <a name="run-this-configuration-in-debug-mode-to-review-the-collected-counting--summing-data"></a><span data-ttu-id="8b855-153">デバッグモードでこの設定を実行し、収集した計算 & 集計データを確認します。</span><span class="sxs-lookup"><span data-stu-id="8b855-153">Run this configuration in debug mode to review the collected counting & summing data</span></span>
1. <span data-ttu-id="8b855-154">[組織管理] > [電子申告] > [コンフィギュレーション] に移動します。</span><span class="sxs-lookup"><span data-stu-id="8b855-154">Go to Organization administration > Electronic reporting > Configurations.</span></span>
2. <span data-ttu-id="8b855-155">ツリーで、「Intrastat model」を展開します。</span><span class="sxs-lookup"><span data-stu-id="8b855-155">In the tree, expand 'Intrastat model'.</span></span>
3. <span data-ttu-id="8b855-156">ツリーで、「Intrastat model\Intrastat (DE)」を選択します。</span><span class="sxs-lookup"><span data-stu-id="8b855-156">In the tree, expand 'Intrastat model\Intrastat (DE)'.</span></span>
4. <span data-ttu-id="8b855-157">ツリーで、「Intrastat model\Intrastat (DE)\Intrastat (DE) with counting & summing'」を選択します。</span><span class="sxs-lookup"><span data-stu-id="8b855-157">In the tree, select 'Intrastat model\Intrastat (DE)\Intrastat (DE) with counting & summing'.</span></span>
5. <span data-ttu-id="8b855-158">アクション ウィンドウで、[設定] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="8b855-158">On the Action Pane, click Configurations.</span></span>
6. <span data-ttu-id="8b855-159">[ユーザー パラメーター] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="8b855-159">Click User parameters.</span></span>
7. <span data-ttu-id="8b855-160">[デバッグモードの実行] フィールドで、[はい] を選択します。</span><span class="sxs-lookup"><span data-stu-id="8b855-160">Select Yes in the Run in debug mode field.</span></span>
8. <span data-ttu-id="8b855-161">[OK] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="8b855-161">Click OK.</span></span>
9. <span data-ttu-id="8b855-162">ページを閉じます。</span><span class="sxs-lookup"><span data-stu-id="8b855-162">Close the page.</span></span>
10. <span data-ttu-id="8b855-163">[税] > [申告] > [対外貿易] > [イントラスタット] の順に移動します。</span><span class="sxs-lookup"><span data-stu-id="8b855-163">Go to Tax > Declarations > Foreign trade > Intrastat.</span></span>
11. <span data-ttu-id="8b855-164">[出力] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="8b855-164">Click Output.</span></span>
12. <span data-ttu-id="8b855-165">[レポート] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="8b855-165">Click Report.</span></span>
13. <span data-ttu-id="8b855-166">[OK] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="8b855-166">Click OK.</span></span>
14. <span data-ttu-id="8b855-167">ページを閉じます。</span><span class="sxs-lookup"><span data-stu-id="8b855-167">Close the page.</span></span>
15. <span data-ttu-id="8b855-168">[組織管理] > [電子申告] > [コンフィギュレーション] に移動します。</span><span class="sxs-lookup"><span data-stu-id="8b855-168">Go to Organization administration > Electronic reporting > Configurations.</span></span>
16. <span data-ttu-id="8b855-169">ツリーで、「Intrastat model」を展開します。</span><span class="sxs-lookup"><span data-stu-id="8b855-169">In the tree, expand 'Intrastat model'.</span></span>
17. <span data-ttu-id="8b855-170">ツリーで、「Intrastat model\Intrastat (DE)」を選択します。</span><span class="sxs-lookup"><span data-stu-id="8b855-170">In the tree, expand 'Intrastat model\Intrastat (DE)'.</span></span>
18. <span data-ttu-id="8b855-171">ツリーで、「Intrastat model\Intrastat (DE)\Intrastat (DE) with counting & summing'」を選択します。</span><span class="sxs-lookup"><span data-stu-id="8b855-171">In the tree, select 'Intrastat model\Intrastat (DE)\Intrastat (DE) with counting & summing'.</span></span>
19. <span data-ttu-id="8b855-172">[デバッグ ログ] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="8b855-172">Click Debug logs.</span></span>
    * <span data-ttu-id="8b855-173">選択した設定の実行に際して、デバッグのログ記録が作成されていることに注意してください。</span><span class="sxs-lookup"><span data-stu-id="8b855-173">Note that a debug log record has been created for the execution process of the selected configuration.</span></span>  
20. <span data-ttu-id="8b855-174">[添付] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="8b855-174">Click Attach.</span></span>
21. <span data-ttu-id="8b855-175">[開く] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="8b855-175">Click Open.</span></span>
    * <span data-ttu-id="8b855-176">選択した設定の実行中に収集された計算と集計の情報を含む作成済みのXMLファイルを確認します。</span><span class="sxs-lookup"><span data-stu-id="8b855-176">Review the created XML file that contains counting and summing details that were collected during the execution of the selected configuration.</span></span>  

