---
title: アンケート結果の表示と評価
description: このトピックは、回答者が完了したアンケートの結果を表示および評価する方法を説明します。
author: andreabichsel
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: KMCollection, KMKnowledgeCollectorCollection, KMKnowledgeCollectorUserResults
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Core, Operations, Talent
ms.custom: 17444
ms.assetid: 6570206a-b2c4-4025-8715-432fe6652b78
ms.search.region: Global
ms.author: anbichse
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0, Talent July 2017 update
ms.openlocfilehash: 38b694b6dd4b1b9a198452e409bd64d7934b4685
ms.sourcegitcommit: 608e68b603afef9eb98d8fb25e90109c2473ef87
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 03/19/2019
ms.locfileid: "859670"
---
# <a name="view-and-evaluate-the-results-of-questionnaires"></a><span data-ttu-id="ffb56-103">アンケート結果の表示と評価</span><span class="sxs-lookup"><span data-stu-id="ffb56-103">View and evaluate the results of questionnaires</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="ffb56-104">このトピックは、回答者が完了したアンケートの結果を表示および評価する方法を説明します。</span><span class="sxs-lookup"><span data-stu-id="ffb56-104">This topic explains how you can view and evaluate the results of questionnaires that respondents complete.</span></span> 

<span data-ttu-id="ffb56-105">回答者がアンケートを完了すると、次の方法でアンケートの結果を表示して評価できます。</span><span class="sxs-lookup"><span data-stu-id="ffb56-105">After respondents complete a questionnaire, you can view and evaluate the questionnaire results in the following ways:</span></span>

-   <span data-ttu-id="ffb56-106">**完了した回答セッション** – 回答者の完了したアンケートに関する詳細を表示し、回答および獲得した点数を集計するレポートを生成します。</span><span class="sxs-lookup"><span data-stu-id="ffb56-106">**Completed answer sessions** – View details about the questionnaires that respondents have completed, and generate reports to summarize answers and any points that were earned.</span></span>
-   <span data-ttu-id="ffb56-107">**結果グループ** – アンケートの結果グループの詳細および統計を表示します。</span><span class="sxs-lookup"><span data-stu-id="ffb56-107">**Result groups** – View result group details and statistics for questionnaires.</span></span> <span data-ttu-id="ffb56-108">結果グループの統計は、アンケートの 1 つの回答セッションまたはすべての回答セッションに生成できます。</span><span class="sxs-lookup"><span data-stu-id="ffb56-108">Result group statistics can be generated for either a single answer session  of a questionnaire or all answer sessions.</span></span>
-   <span data-ttu-id="ffb56-109">**アンケート統計** – 特定の回答者グループの統計を計算する基準を指定します。</span><span class="sxs-lookup"><span data-stu-id="ffb56-109">**Questionnaire statistics** – Specify criteria to calculate statistics for a specific group of respondents.</span></span>

<span data-ttu-id="ffb56-110">個人、回答セッション、または結果グループに分類された結果を表示する各種レポートを生成できます。</span><span class="sxs-lookup"><span data-stu-id="ffb56-110">You can also generate various reports to view results that are sorted by person, answer session, or result group.</span></span> <span data-ttu-id="ffb56-111">完了したアンケートに関連する次のレポートを使用できます。</span><span class="sxs-lookup"><span data-stu-id="ffb56-111">The following reports that are related to completed questionnaires are available:</span></span>

-   <span data-ttu-id="ffb56-112">回答</span><span class="sxs-lookup"><span data-stu-id="ffb56-112">Answers</span></span>
-   <span data-ttu-id="ffb56-113">アンケート別回答</span><span class="sxs-lookup"><span data-stu-id="ffb56-113">Answers per questionnaire</span></span>
-   <span data-ttu-id="ffb56-114">個人別回答</span><span class="sxs-lookup"><span data-stu-id="ffb56-114">Answers per person</span></span>
-   <span data-ttu-id="ffb56-115">フィードバック分析</span><span class="sxs-lookup"><span data-stu-id="ffb56-115">Feedback analysis</span></span>

## <a name="answer-session-results"></a><span data-ttu-id="ffb56-116">回答セッションの結果</span><span class="sxs-lookup"><span data-stu-id="ffb56-116">Answer session results</span></span>
<span data-ttu-id="ffb56-117">回答者がアンケートを実行後、完了した回答セッションの結果を表示できます。</span><span class="sxs-lookup"><span data-stu-id="ffb56-117">After respondents complete a questionnaire, you can view the results of the completed answer sessions.</span></span> <span data-ttu-id="ffb56-118">回答セッションは、アンケートに対する一人のユーザーの応答です。</span><span class="sxs-lookup"><span data-stu-id="ffb56-118">An answer session is one user’s response to a questionnaire.</span></span> <span data-ttu-id="ffb56-119">**回答**ページで、完了した回答セッションに関する詳細を表示できます。</span><span class="sxs-lookup"><span data-stu-id="ffb56-119">You can view details about completed answer sessions on the **Answers** page.</span></span> <span data-ttu-id="ffb56-120">**回答** ページに含まれている回答セッションは、ページを開いた方法によってさまざまな方法でフィルター処理されます。</span><span class="sxs-lookup"><span data-stu-id="ffb56-120">The answer sessions that are included on the **Answers** page are filtered in various ways, depending on how you open the page:</span></span>

-   <span data-ttu-id="ffb56-121">すべてのアンケート</span><span class="sxs-lookup"><span data-stu-id="ffb56-121">All questionnaires</span></span>
-   <span data-ttu-id="ffb56-122">特定のアンケート</span><span class="sxs-lookup"><span data-stu-id="ffb56-122">A specific questionnaire</span></span>
-   <span data-ttu-id="ffb56-123">特定の人物</span><span class="sxs-lookup"><span data-stu-id="ffb56-123">A specific person</span></span>

<span data-ttu-id="ffb56-124">**回答**ページから、各結果グループの回答、獲得された点数、回答者の応答、および選択したアンケートに質問階層が使用された場合はその詳細を表示できます。</span><span class="sxs-lookup"><span data-stu-id="ffb56-124">From the **Answers** page, you can view details about answers, points that were earned, a respondent’s responses in each result group, and the question hierarchy that was used on the selected questionnaire, if a question hierarchy was used.</span></span> <span data-ttu-id="ffb56-125">次のレポートの生成および印刷もできます。</span><span class="sxs-lookup"><span data-stu-id="ffb56-125">You can also generate and print the following reports:</span></span>

-   <span data-ttu-id="ffb56-126">**結果レポート** – このレポートには、選択された回答セッションの結果グループごとに取得したポイントをグラフィカル表示します。</span><span class="sxs-lookup"><span data-stu-id="ffb56-126">**Results report** – This report shows a graphical representation of the points that were earned per result group for the selected answer session.</span></span>
-   <span data-ttu-id="ffb56-127">**回答集計レポート** – このレポートには、回答者がアンケートの各質問に対して選択した回答を表示します。</span><span class="sxs-lookup"><span data-stu-id="ffb56-127">**Answer report** – This report shows the answers that the respondent selected for each question on the questionnaire.</span></span>
-   <span data-ttu-id="ffb56-128">**誤回答** – このレポートには、回答者が選択した誤回答に関連付けられる情報を表示します。</span><span class="sxs-lookup"><span data-stu-id="ffb56-128">**Incorrect answers** – This report shows information that is related to the incorrect answers that the respondent selected.</span></span>

<span data-ttu-id="ffb56-129">**メモ:** **結果**レポートは、アンケートの結果グループを使用し、**アンケート**ページで**結果ページ**を選択している場合にのみ使用できます。</span><span class="sxs-lookup"><span data-stu-id="ffb56-129">**Note:** The **Results** report is available only if you use results groups on the questionnaire, and if you selected **Results page** on the **Questionnaires** page.</span></span> <span data-ttu-id="ffb56-130">**回答集計**レポートと**誤回答**レポートは**アンケート**ページで**回答集計レポート**を選択している場合にのみ使用できます。</span><span class="sxs-lookup"><span data-stu-id="ffb56-130">The **Answer** report and the **Incorrect answers** report are available only if you selected **Answer report** on the **Questionnaires** page.</span></span>

## <a name="questionnaire-statistics"></a><span data-ttu-id="ffb56-131">アンケートの統計情報</span><span class="sxs-lookup"><span data-stu-id="ffb56-131">Questionnaire statistics</span></span>
<span data-ttu-id="ffb56-132">定義した計算が基にしたアンケート統計では、完了したアンケートの結果を分析できます。</span><span class="sxs-lookup"><span data-stu-id="ffb56-132">You can use questionnaire statistics to analyze the results of a completed questionnaire, based on calculations that you define.</span></span> <span data-ttu-id="ffb56-133">計算を定義するには、次の作業を行う必要があります。</span><span class="sxs-lookup"><span data-stu-id="ffb56-133">To define calculations, you must complete the following tasks:</span></span>

-   <span data-ttu-id="ffb56-134">統計を計算および表示する基準を選択します。</span><span class="sxs-lookup"><span data-stu-id="ffb56-134">Select criteria to calculate and display the statistics.</span></span>
    -   <span data-ttu-id="ffb56-135">アンケート、質問、質問行、または結果グループごとに統計を表示できます。</span><span class="sxs-lookup"><span data-stu-id="ffb56-135">You can show statistics by questionnaire, questions, question rows, or results groups.</span></span>
    -   <span data-ttu-id="ffb56-136">結果を表示するときに使用するグラフのタイプを選択します。</span><span class="sxs-lookup"><span data-stu-id="ffb56-136">Select the type of chart that will be used when you view results.</span></span>
    -   <span data-ttu-id="ffb56-137">回答を統計に含めるネットワーク上のユーザーのタイプ、従業員、連絡先担当者、または申請者などを選択します。</span><span class="sxs-lookup"><span data-stu-id="ffb56-137">Select the types of people from the network, such as employees, contact persons, or applicants, to include answers for.</span></span> <span data-ttu-id="ffb56-138">また、匿名で完了したアンケートの回答も含めることができます。</span><span class="sxs-lookup"><span data-stu-id="ffb56-138">You can also include answers from questionnaires that were completed anonymously.</span></span>
    -   <span data-ttu-id="ffb56-139">結果を分析するには、年齢または勤続に基づく期間を設定します。</span><span class="sxs-lookup"><span data-stu-id="ffb56-139">Set up intervals that are based on age or seniority to analyze results.</span></span>
-   <span data-ttu-id="ffb56-140">統計の対象範囲を調整する設定を選択または確認します。</span><span class="sxs-lookup"><span data-stu-id="ffb56-140">Select or verify settings that refine the subject of the statistics.</span></span> <span data-ttu-id="ffb56-141">たとえば、郵便番号を選択することにより、特定の地域のすべての回答者を対象として結果を分析できます。</span><span class="sxs-lookup"><span data-stu-id="ffb56-141">For example, by selecting a ZIP Code or postal code, you can analyze results for all respondents within a specific geographic area.</span></span>
-   <span data-ttu-id="ffb56-142">回答者またはアンケートの特性による結果を分析するための基準を選択または確認します。</span><span class="sxs-lookup"><span data-stu-id="ffb56-142">Select or verify criteria to analyze results by respondent or questionnaire characteristics.</span></span> <span data-ttu-id="ffb56-143">たとえば、**郵便番号**を選択して、回答者の場所と正解との相関関係を分析できます。</span><span class="sxs-lookup"><span data-stu-id="ffb56-143">For example, by selecting **ZIP/postal code**, you can analyze the correlation between a respondent’s location and correct answers.</span></span>

<span data-ttu-id="ffb56-144">定義した設定は保存され、定期的に結果を再計算するために使用されます。</span><span class="sxs-lookup"><span data-stu-id="ffb56-144">The settings that you define are saved and can be used to periodically recalculate results.</span></span>

<a name="additional-resources"></a><span data-ttu-id="ffb56-145">その他のリソース</span><span class="sxs-lookup"><span data-stu-id="ffb56-145">Additional resources</span></span>
--------

[<span data-ttu-id="ffb56-146">アンケートのデザイン</span><span class="sxs-lookup"><span data-stu-id="ffb56-146">Designing questionnaires</span></span>](design-questionnaires.md)

[<span data-ttu-id="ffb56-147">アンケートの使用</span><span class="sxs-lookup"><span data-stu-id="ffb56-147">Using questionnaires</span></span>](questionnaires.md)

[<span data-ttu-id="ffb56-148">アンケートの配布および記入</span><span class="sxs-lookup"><span data-stu-id="ffb56-148">Distributing and completing questionnaires</span></span>](distribute-questionnaires.md)

