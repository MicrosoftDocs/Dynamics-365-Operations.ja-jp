---
title: アンケート結果の分析
description: アンケートの統計情報は、一連の統計データに基づいて平均、合計、割合を計算するために使用できます。
author: andreabichsel
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: KMQuestionnaireStatistics, KMQuestionnaireStatisticsLine, HcmLearningWorkspace
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: anbichse
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 0b8e4fd5d9fabd35de067ab61c1e64156ce4f0ec
ms.sourcegitcommit: ba340f836e472f13f263dec46a49847c788fca44
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/04/2020
ms.locfileid: "3429108"
---
# <a name="analyzing-questionnaire-results"></a><span data-ttu-id="371f8-103">アンケート結果の分析</span><span class="sxs-lookup"><span data-stu-id="371f8-103">Analyzing questionnaire results</span></span>



<span data-ttu-id="371f8-104">アンケートの統計情報は、一連の統計データに基づいて平均、合計、割合を計算するために使用できます。</span><span class="sxs-lookup"><span data-stu-id="371f8-104">Questionnaire statistics can be used to calculate averages, totals, and percentages based on a set of demographic data.</span></span> <span data-ttu-id="371f8-105">この手順を開始するには、[アンケート] > [結果の表示と分析] > [アンケート統計] の順に移動します。</span><span class="sxs-lookup"><span data-stu-id="371f8-105">To begin this procedure, go to Questionnaire > View and analyze results > Questionnaire statistics.</span></span> <span data-ttu-id="371f8-106">この手順の作成に使用するデモ データの会社は USMF です。</span><span class="sxs-lookup"><span data-stu-id="371f8-106">The demo data company used to create this procedure is USMF.</span></span>


## <a name="create-a-questionnaire-statistics-record"></a><span data-ttu-id="371f8-107">アンケート統計レコードの作成</span><span class="sxs-lookup"><span data-stu-id="371f8-107">Create a Questionnaire statistics record</span></span>
1. <span data-ttu-id="371f8-108">[アンケートの統計情報] に移動します。</span><span class="sxs-lookup"><span data-stu-id="371f8-108">Go to Questionnaire statistics.</span></span>
2. <span data-ttu-id="371f8-109">[新規] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="371f8-109">Click New.</span></span>
3. <span data-ttu-id="371f8-110">一覧で、選択された行をマークします。</span><span class="sxs-lookup"><span data-stu-id="371f8-110">In the list, mark the selected row.</span></span>
4. <span data-ttu-id="371f8-111">[統計] フィールドに値を入力します。</span><span class="sxs-lookup"><span data-stu-id="371f8-111">In the Statistics field, type a value.</span></span>
5. <span data-ttu-id="371f8-112">[説明] フィールドで値を入力します。</span><span class="sxs-lookup"><span data-stu-id="371f8-112">In the Description field, type a value.</span></span>
6. <span data-ttu-id="371f8-113">[アンケート] フィールドで、ドロップ ダウン ボタンをクリックし、ルックアップを開きます。</span><span class="sxs-lookup"><span data-stu-id="371f8-113">In the Questionnaire field, click the drop-down button to open the lookup.</span></span>
7. <span data-ttu-id="371f8-114">一覧で、選択された行のリンクをクリックします。</span><span class="sxs-lookup"><span data-stu-id="371f8-114">In the list, click the link in the selected row.</span></span>
8. <span data-ttu-id="371f8-115">[一般] タブをクリックします。</span><span class="sxs-lookup"><span data-stu-id="371f8-115">Click the General tab.</span></span>
    * <span data-ttu-id="371f8-116">匿名結果や作業者の結果、連絡担当者、および申請者を含める場合に選択します。</span><span class="sxs-lookup"><span data-stu-id="371f8-116">Select if you want to include anonymous results or results from workers, contacts, and applicants.</span></span>  
9. <span data-ttu-id="371f8-117">[作業者] チェック ボックスをオンまたはオフにします。</span><span class="sxs-lookup"><span data-stu-id="371f8-117">Select or clear the Worker check box.</span></span>
    * <span data-ttu-id="371f8-118">年齢または勤続年数別に結果を表示する場合、結果をグループ化するのに使用する範囲を指定します。</span><span class="sxs-lookup"><span data-stu-id="371f8-118">If you will be viewing the results by seniority or age, specify the intervals that you would like to use for grouping the results.</span></span>  
    * <span data-ttu-id="371f8-119">年齢間隔に 5 を入力すると、5 才ごとに結果をグループ化します。</span><span class="sxs-lookup"><span data-stu-id="371f8-119">Entering a 5 for the age interval will group the results based on five-year age intervals.</span></span>  
10. <span data-ttu-id="371f8-120">[年齢] フィールドに数値を入力します。</span><span class="sxs-lookup"><span data-stu-id="371f8-120">In the Age field, enter a number.</span></span>
    * <span data-ttu-id="371f8-121">各結果グループ、各質問、または各質問別に、全体のアンケートに対して計算を実行する場合に選択します。</span><span class="sxs-lookup"><span data-stu-id="371f8-121">Select if you want to run the calculation against the entire questionnaire, for each result group, for each question, or for each question row.</span></span>  
    * <span data-ttu-id="371f8-122">結果をグループ化する方法を選択します。</span><span class="sxs-lookup"><span data-stu-id="371f8-122">Select how you would like to group the results.</span></span>  
    * <span data-ttu-id="371f8-123">たとえば、質問ごとに平均ポイントを計算し、結果グループをグループ化することによって質問を表示することをお勧めします。</span><span class="sxs-lookup"><span data-stu-id="371f8-123">For example, if you calculate the average points per question, you may want to see the questions grouped by Result group.</span></span>  
    * <span data-ttu-id="371f8-124">計算の基になるデータを選択します。</span><span class="sxs-lookup"><span data-stu-id="371f8-124">Select the data to base the calculation on.</span></span>  
    * <span data-ttu-id="371f8-125">たとえば、作業者を対象に行ったアンケートの平均割合と作業者間で獲得した平均ポイント数を表示する場合です。</span><span class="sxs-lookup"><span data-stu-id="371f8-125">For example, if you want to see the average percent received on the questionnaire across your workers versus the average number of points achieved across your workers.</span></span>  
11. <span data-ttu-id="371f8-126">[範囲] タブをクリックします。</span><span class="sxs-lookup"><span data-stu-id="371f8-126">Click the Range tab.</span></span>
    * <span data-ttu-id="371f8-127">範囲の基準を満たすもののみに結果セットを制限して範囲を使用します。</span><span class="sxs-lookup"><span data-stu-id="371f8-127">Use ranges to limit your result set to only those meeting the Range criteria.</span></span>  
12. <span data-ttu-id="371f8-128">[グループ化] タブをクリックします。</span><span class="sxs-lookup"><span data-stu-id="371f8-128">Click the Grouping by tab.</span></span>
    * <span data-ttu-id="371f8-129">グループ化を使用すると、結果を表示する方法を変更できます。</span><span class="sxs-lookup"><span data-stu-id="371f8-129">Use Groupings to determine how the results should be displayed.</span></span>  
    * <span data-ttu-id="371f8-130">たとえば、最初に性別ごとに、その次に年齢ごとに結果をグループ化します。</span><span class="sxs-lookup"><span data-stu-id="371f8-130">For example, group the results first by gender, then by age.</span></span>  
13. <span data-ttu-id="371f8-131">一覧で、目的のレコードを見つけ、選択します。</span><span class="sxs-lookup"><span data-stu-id="371f8-131">In the list, find and select the desired record.</span></span>
    * <span data-ttu-id="371f8-132">グループを選択した側にに移動して、目的の順序に配置します。</span><span class="sxs-lookup"><span data-stu-id="371f8-132">Move the groupings into the Selected side and place them in the desired order.</span></span>  

## <a name="execute-the-statistics-calculation"></a><span data-ttu-id="371f8-133">統計計算の実行</span><span class="sxs-lookup"><span data-stu-id="371f8-133">Execute the statistics calculation</span></span>
1. <span data-ttu-id="371f8-134">[実行] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="371f8-134">Click Execute.</span></span>
    * <span data-ttu-id="371f8-135">結果に対して実行する計算機能を選択します。</span><span class="sxs-lookup"><span data-stu-id="371f8-135">Select which calculation function you would like to perform on the results.</span></span>  
    * <span data-ttu-id="371f8-136">たとえば、選択したグループ化について、アンケートの平均割合を計算するか、または結果グループのポイントを合計します。</span><span class="sxs-lookup"><span data-stu-id="371f8-136">For example, calculate the average percentages across the questionnaire for the selected groupings or total the points across the result groups for the selected groupings.</span></span>  
2. <span data-ttu-id="371f8-137">[以前の検索結果を削除] チェック ボックスをオンまたはオフにします。</span><span class="sxs-lookup"><span data-stu-id="371f8-137">Select or clear the Delete previous searches check box.</span></span>
3. <span data-ttu-id="371f8-138">[OK] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="371f8-138">Click OK.</span></span>

## <a name="view-the-results-of-the-questionnaire-statistics-run"></a><span data-ttu-id="371f8-139">アンケート統計の実行結果を表示します。</span><span class="sxs-lookup"><span data-stu-id="371f8-139">View the results of the questionnaire statistics run.</span></span>
1. <span data-ttu-id="371f8-140">[結果] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="371f8-140">Click Result.</span></span>
2. <span data-ttu-id="371f8-141">[結果] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="371f8-141">Click Result.</span></span>
3. <span data-ttu-id="371f8-142">ページを閉じます。</span><span class="sxs-lookup"><span data-stu-id="371f8-142">Close the page.</span></span>

