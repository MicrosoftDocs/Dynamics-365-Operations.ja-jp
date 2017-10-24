---
title: "アンケートのデザイン"
description: "このトピックは、アンケートを作成するプロセスについて説明します。 最初の手順では、アンケートを設計します。 アンケートを設計する場合は、質問と回答を書き込むだけでなく、回答を記録し、表にする構造を作成します。"
author: twheeloc
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: 
ms.service: Dynamics365Operations
ms.technology: 
ms.search.form: KCMCollectionType, KMAnswerCollection, KMCollection
audience: Application User
ms.reviewer: twheeloc
ms.search.scope: Core, AX 7.0.0, Operations, UnifiedOperations
ms.custom: 17341
ms.assetid: b27e2f12-c7a0-4a54-b8d8-17819f8a1c72
ms.search.region: Global
ms.author: twheeloc
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0, Talent July 2017 update
ms.translationtype: HT
ms.sourcegitcommit: f827b4787506cfdec8b9a91c4a68f3293190158a
ms.openlocfilehash: 65720297b43af49d8c8382ee2e3dde903d05ed14
ms.contentlocale: ja-jp
ms.lasthandoff: 09/29/2017

---

# <a name="design-a-questionnaire"></a><span data-ttu-id="90e7d-105">アンケートのデザイン</span><span class="sxs-lookup"><span data-stu-id="90e7d-105">Design a questionnaire</span></span>

<span data-ttu-id="90e7d-106">このトピックは、アンケートを作成するプロセスについて説明します。</span><span class="sxs-lookup"><span data-stu-id="90e7d-106">This topic describes the process for creating a questionnaire.</span></span> <span data-ttu-id="90e7d-107">最初の手順では、アンケートを設計します。</span><span class="sxs-lookup"><span data-stu-id="90e7d-107">The first step is to design the questionnaire.</span></span> <span data-ttu-id="90e7d-108">アンケートを設計する場合は、質問と回答を書き込むだけでなく、回答を記録し、表にする構造を作成します。</span><span class="sxs-lookup"><span data-stu-id="90e7d-108">When you design a questionnaire, you not only write the questions and answers, but also create the structure that enables answers to be recorded and tabulated.</span></span> 

<span data-ttu-id="90e7d-109">アンケートを入念に設計することは、収集するデータの質の向上につながります。</span><span class="sxs-lookup"><span data-stu-id="90e7d-109">A carefully designed questionnaire can help increase the quality of the data that you collect.</span></span> <span data-ttu-id="90e7d-110">デザインを入念に作成することで、適切な時点で、アンケートの適切なオプションをさらにうまく選択できます。</span><span class="sxs-lookup"><span data-stu-id="90e7d-110">Through careful design, you can better select the appropriate options at the appropriate time for a questionnaire.</span></span> <span data-ttu-id="90e7d-111">次の点が有効なアンケートを計画するのに役立ちます。</span><span class="sxs-lookup"><span data-stu-id="90e7d-111">The following points can help you plan an effective questionnaire:</span></span>

-   <span data-ttu-id="90e7d-112">質問が目的をサポートするのを保証するためにアンケートの目的を明確に定義します。</span><span class="sxs-lookup"><span data-stu-id="90e7d-112">Clearly define the purpose of the questionnaire to help guarantee that the questions support the purpose.</span></span>
-   <span data-ttu-id="90e7d-113">アンケートの対象となる個人やグループを決定します。</span><span class="sxs-lookup"><span data-stu-id="90e7d-113">Determine the individual person or the group of people who should complete the questionnaire.</span></span>
-   <span data-ttu-id="90e7d-114">アンケートに表示される質問を記述し、該当する場合は、回答の選択肢を含めます。</span><span class="sxs-lookup"><span data-stu-id="90e7d-114">Write questions that will appear on the questionnaire, and include answer choices, if applicable.</span></span>
-   <span data-ttu-id="90e7d-115">回答者が回答を続けるために、アンケートのフローが論理的であることを確認します。</span><span class="sxs-lookup"><span data-stu-id="90e7d-115">Be sure that the questionnaire flows logically, so that respondents remain engaged.</span></span>
-   <span data-ttu-id="90e7d-116">質問と回答は、回答者に提示する順序で並べ替えます。</span><span class="sxs-lookup"><span data-stu-id="90e7d-116">Arrange questions and answers in the order that they should be presented to respondents in.</span></span>
-   <span data-ttu-id="90e7d-117">該当する場合は、結果を評価する方法を指定します。</span><span class="sxs-lookup"><span data-stu-id="90e7d-117">Decide how the results should be evaluated, if applicable.</span></span>
-   <span data-ttu-id="90e7d-118">追加機能が必要かどうかを決定します。</span><span class="sxs-lookup"><span data-stu-id="90e7d-118">Decide whether you’ll need additional features.</span></span> <span data-ttu-id="90e7d-119">たとえば、結果を分類する必要があるかとその方法、時間制限が必要か、すべての質問を必須にするかどうかを決定します。</span><span class="sxs-lookup"><span data-stu-id="90e7d-119">For example, determine whether and how results should be categorized, whether a time limit is required, or whether all the questions will be mandatory.</span></span>

<span data-ttu-id="90e7d-120">設計フェーズには、次の順序で行う必要がある 4 つのタスクのカテゴリが含まれます。</span><span class="sxs-lookup"><span data-stu-id="90e7d-120">The design phase includes four categories of tasks that you must complete in this order:</span></span>

1.  <span data-ttu-id="90e7d-121">必要に応じて、前提条件を設定します。</span><span class="sxs-lookup"><span data-stu-id="90e7d-121">Set up prerequisites, as required.</span></span>
2.  <span data-ttu-id="90e7d-122">該当する場合は、回答グループと回答を設定します。</span><span class="sxs-lookup"><span data-stu-id="90e7d-122">Set up answer groups and answers, if applicable.</span></span>
3.  <span data-ttu-id="90e7d-123">質問および質問と回答グループの関連付けを設定します。</span><span class="sxs-lookup"><span data-stu-id="90e7d-123">Set up questions and their association with the answer groups.</span></span>
4.  <span data-ttu-id="90e7d-124">アンケート自体を設定し、それに質問を付属させます。</span><span class="sxs-lookup"><span data-stu-id="90e7d-124">Set up the questionnaire itself, and attach questions to it.</span></span>

## <a name="prerequisites"></a><span data-ttu-id="90e7d-125">必要条件</span><span class="sxs-lookup"><span data-stu-id="90e7d-125">Prerequisites</span></span>
<span data-ttu-id="90e7d-126">アンケート、回答、質問を作成する前に、前提条件を導入する必要があります。</span><span class="sxs-lookup"><span data-stu-id="90e7d-126">Some prerequisites must be in place before you can create questionnaires, answers, and questions.</span></span> <span data-ttu-id="90e7d-127">ただし、完全に機能させるのにすべての前提条件が必要ではありません。</span><span class="sxs-lookup"><span data-stu-id="90e7d-127">However, not all prerequisites are required for full functionality.</span></span>

### <a name="required"></a><span data-ttu-id="90e7d-128">必須</span><span class="sxs-lookup"><span data-stu-id="90e7d-128">Required</span></span>

| <span data-ttu-id="90e7d-129">前提条件</span><span class="sxs-lookup"><span data-stu-id="90e7d-129">Prerequisite</span></span>        | <span data-ttu-id="90e7d-130">説明</span><span class="sxs-lookup"><span data-stu-id="90e7d-130">Description</span></span>                |
|---------------------|----------------------------|
| <span data-ttu-id="90e7d-131">アンケートのタイプ</span><span class="sxs-lookup"><span data-stu-id="90e7d-131">Questionnaire types</span></span> | <span data-ttu-id="90e7d-132">アンケートを分類します。</span><span class="sxs-lookup"><span data-stu-id="90e7d-132">Categorize questionnaires.</span></span> |
| <span data-ttu-id="90e7d-133">質問タイプ</span><span class="sxs-lookup"><span data-stu-id="90e7d-133">Question types</span></span>      | <span data-ttu-id="90e7d-134">質問を分類します。</span><span class="sxs-lookup"><span data-stu-id="90e7d-134">Categorize questions.</span></span>      |

### <a name="optional"></a><span data-ttu-id="90e7d-135">オプション</span><span class="sxs-lookup"><span data-stu-id="90e7d-135">Optional</span></span>

| <span data-ttu-id="90e7d-136">前提条件</span><span class="sxs-lookup"><span data-stu-id="90e7d-136">Prerequisite</span></span>             | <span data-ttu-id="90e7d-137">説明</span><span class="sxs-lookup"><span data-stu-id="90e7d-137">Description</span></span>                                                    |
|--------------------------|----------------------------------------------------------------|
| <span data-ttu-id="90e7d-138">アンケート パラメーター</span><span class="sxs-lookup"><span data-stu-id="90e7d-138">Questionnaire parameters</span></span> | <span data-ttu-id="90e7d-139">アンケートの基本コントロールと既定の設定を変更します。</span><span class="sxs-lookup"><span data-stu-id="90e7d-139">Modify basic controls and default settings for questionnaires.</span></span> |

### <a name="questionnaire-types"></a><span data-ttu-id="90e7d-140">アンケートのタイプ</span><span class="sxs-lookup"><span data-stu-id="90e7d-140">Questionnaire types</span></span>

<span data-ttu-id="90e7d-141">アンケート タイプは必須で、アンケートを作成する際に割り当てる必要があります。</span><span class="sxs-lookup"><span data-stu-id="90e7d-141">Questionnaire types are required and must be assigned when you create a questionnaire.</span></span> <span data-ttu-id="90e7d-142">アンケートのタイプは、アンケートを容易に管理および分類するためにも使用できます。</span><span class="sxs-lookup"><span data-stu-id="90e7d-142">Questionnaire types help you manage and classify questionnaires more easily.</span></span> <span data-ttu-id="90e7d-143">アンケート タイプは、アンケートを分類して互いに区別するために使用します。</span><span class="sxs-lookup"><span data-stu-id="90e7d-143">Use questionnaire types to classify questionnaires and differentiate them from each other.</span></span> <span data-ttu-id="90e7d-144">たとえば、複数のアンケートから選択できる場合、特定のアンケートの検索を容易にするためにそれらをタイプでフィルタ処理できます。</span><span class="sxs-lookup"><span data-stu-id="90e7d-144">For example, if you have multiple questionnaires to select from, you can filter them by type to help make it easier to find a particular questionnaire.</span></span> <span data-ttu-id="90e7d-145">アンケートのタイプの例を次に示します。</span><span class="sxs-lookup"><span data-stu-id="90e7d-145">Here are some examples of questionnaire types:</span></span>

-   <span data-ttu-id="90e7d-146">人材開発</span><span class="sxs-lookup"><span data-stu-id="90e7d-146">Human resource development</span></span>
-   <span data-ttu-id="90e7d-147">顧客アンケート</span><span class="sxs-lookup"><span data-stu-id="90e7d-147">Customer surveys</span></span>
-   <span data-ttu-id="90e7d-148">確認プロセス</span><span class="sxs-lookup"><span data-stu-id="90e7d-148">Review process</span></span>

### <a name="question-types"></a><span data-ttu-id="90e7d-149">質問タイプ</span><span class="sxs-lookup"><span data-stu-id="90e7d-149">Question types</span></span>

<span data-ttu-id="90e7d-150">質問タイプは必須で、質問を作成する際に割り当てる必要があります。</span><span class="sxs-lookup"><span data-stu-id="90e7d-150">Question types are required and must be assigned when you create a question.</span></span> 

<span data-ttu-id="90e7d-151">レポートの質問を分類するには質問タイプを使用します。</span><span class="sxs-lookup"><span data-stu-id="90e7d-151">Use question types to categorize questions for reporting.</span></span> <span data-ttu-id="90e7d-152">[**質問**] ページのタイプをフィルタとして使用できるため、質問タイプは質問の検索を容易にします。</span><span class="sxs-lookup"><span data-stu-id="90e7d-152">Question types also make it easier to find questions, because you can use types as filters on the **Questions** page.</span></span> <span data-ttu-id="90e7d-153">質問タイプの例を次に示します。</span><span class="sxs-lookup"><span data-stu-id="90e7d-153">Here are some examples of question types:</span></span>

-   <span data-ttu-id="90e7d-154">人事リソース</span><span class="sxs-lookup"><span data-stu-id="90e7d-154">Human resource</span></span>
-   <span data-ttu-id="90e7d-155">業務の管理</span><span class="sxs-lookup"><span data-stu-id="90e7d-155">Managing business</span></span>
-   <span data-ttu-id="90e7d-156">コースの評価</span><span class="sxs-lookup"><span data-stu-id="90e7d-156">Course evaluation</span></span>

### <a name="questionnaire-parameters"></a><span data-ttu-id="90e7d-157">アンケート パラメーター</span><span class="sxs-lookup"><span data-stu-id="90e7d-157">Questionnaire parameters</span></span>

<span data-ttu-id="90e7d-158">アンケート パラメーターはオプションです。</span><span class="sxs-lookup"><span data-stu-id="90e7d-158">Questionnaire parameters are optional.</span></span> <span data-ttu-id="90e7d-159">会社の要件によって使用しない場合があります。</span><span class="sxs-lookup"><span data-stu-id="90e7d-159">You might not use them, depending on your company’s requirements.</span></span> 

<span data-ttu-id="90e7d-160">アンケート パラメータは、アンケートの匿名性別、番号順序コードおよび照会タイプを定義します。</span><span class="sxs-lookup"><span data-stu-id="90e7d-160">Questionnaire parameters define the anonymity, number sequence codes, and reference types of a questionnaire.</span></span> <span data-ttu-id="90e7d-161">組織がアンケートを配布すると、匿名の回答者を許可するオプションが問題になる場合があります。</span><span class="sxs-lookup"><span data-stu-id="90e7d-161">When an organization distributes a questionnaire, the option to allow respondents to remain anonymous might be of concern.</span></span> 

<span data-ttu-id="90e7d-162">番号順序コードは、質問と回答を整理するために使用されます。</span><span class="sxs-lookup"><span data-stu-id="90e7d-162">The number sequence codes are used to organize questions and answers.</span></span> <span data-ttu-id="90e7d-163">これらの番号順序コードに基づいて、値は品目に自動的に割り当てられます。</span><span class="sxs-lookup"><span data-stu-id="90e7d-163">Based on these number sequence codes, values are automatically assigned to items.</span></span> 

<span data-ttu-id="90e7d-164">データの作成を開始する前にすべてのパラメータを定義する必要があります。</span><span class="sxs-lookup"><span data-stu-id="90e7d-164">You should define all parameters before you begin to create your data.</span></span> <span data-ttu-id="90e7d-165">アンケート パラメータ設定はいつでも変更できます。</span><span class="sxs-lookup"><span data-stu-id="90e7d-165">You can modify the questionnaire parameter settings at any time.</span></span>

## <a name="questionnaire-components"></a><span data-ttu-id="90e7d-166">アンケート コンポーネント</span><span class="sxs-lookup"><span data-stu-id="90e7d-166">Questionnaire components</span></span>
<span data-ttu-id="90e7d-167">アンケートは 3 つの主要な要素から成り立ちます。多項選択の質問、質問、アンケート自体の回答を含んだ回答グループ。</span><span class="sxs-lookup"><span data-stu-id="90e7d-167">Questionnaires comprise three main elements: answer groups that contain the answers for multiple choice questions, questions, and the questionnaire itself.</span></span> <span data-ttu-id="90e7d-168">オプションでアンケートの質問を結果グループにグループ化できます。</span><span class="sxs-lookup"><span data-stu-id="90e7d-168">You can optionally group the questions on a questionnaire into result groups.</span></span> <span data-ttu-id="90e7d-169">結果グループは、質問を分類し、アンケートの更なる分析を提供します。</span><span class="sxs-lookup"><span data-stu-id="90e7d-169">Result groups let you categorize questions and provide further analysis on the questionnaire.</span></span> 

<span data-ttu-id="90e7d-170">[![QuestionnaireComponents](./media/questionnairecomponents-1024x615.png)](./media/questionnairecomponents.png)</span><span class="sxs-lookup"><span data-stu-id="90e7d-170">[![QuestionnaireComponents](./media/questionnairecomponents-1024x615.png)](./media/questionnairecomponents.png)</span></span>

### <a name="answer-groups-and-answers"></a><span data-ttu-id="90e7d-171">回答グループおよび回答</span><span class="sxs-lookup"><span data-stu-id="90e7d-171">Answer groups and answers</span></span>

<span data-ttu-id="90e7d-172">回答者が質問に回答するには次の 2 つの方法があり、どちらを使用するかは質問の目的によって決まります。</span><span class="sxs-lookup"><span data-stu-id="90e7d-172">Respondents can answer a question in two ways, depending on the subject of the question:</span></span>

-   <span data-ttu-id="90e7d-173">自由回答式の質問は、特定の形式の応答を必要としません。</span><span class="sxs-lookup"><span data-stu-id="90e7d-173">Open-ended questions don’t require responses in a specific format.</span></span> <span data-ttu-id="90e7d-174">回答者はテキスト、数、または日付か時刻で回答を入力します。</span><span class="sxs-lookup"><span data-stu-id="90e7d-174">Respondents can type a response as text, a number, a date, or a time.</span></span> <span data-ttu-id="90e7d-175">通常、これらの質問では、回答者は意見、説明、評価、予測などの主観的な情報を回答として入力する必要があります。</span><span class="sxs-lookup"><span data-stu-id="90e7d-175">These questions typically require that the respondents provide subjective information in their answers, such as an opinion, description, evaluation, or estimate.</span></span>
-   <span data-ttu-id="90e7d-176">選択式の質問は、回答者が回答の選択肢の一覧から回答を選択する必要があります。</span><span class="sxs-lookup"><span data-stu-id="90e7d-176">Closed-ended questions require that the respondent select an answer in a list of possible correct answers.</span></span>

<span data-ttu-id="90e7d-177">選択式の質問に回答の選択肢の一覧を提供するには、[**回答グループ**] ページで回答を作成します。</span><span class="sxs-lookup"><span data-stu-id="90e7d-177">To provide a list of possible answers for closed-ended questions, you can create answers on the **Answer groups** page.</span></span> 

<span data-ttu-id="90e7d-178">回答グループと回答は、質問が作成された情報元の本体を構成するコンポーネントです。</span><span class="sxs-lookup"><span data-stu-id="90e7d-178">Answer groups and answers are components that make up the main body of information that questions are created from.</span></span> <span data-ttu-id="90e7d-179">回答グループを作成した後に、[**質問**] ページの [**回答グループ**] フィールドでその回答グループを質問に関連付けることができます。</span><span class="sxs-lookup"><span data-stu-id="90e7d-179">After you create an answer group, you can associate the answer group with a question in the **Answer group** field on the **Questions** page.</span></span> 

<span data-ttu-id="90e7d-180">回答グループは、同じアンケートの複数の質問で使用できるほか、複数のアンケートにわたって使用することもできます。</span><span class="sxs-lookup"><span data-stu-id="90e7d-180">An answer group can be used for more than one question on the same questionnaire, and can also be used on more than one questionnaire.</span></span> 

<span data-ttu-id="90e7d-181">**メモ:** 完了したアンケートで既に使用されている回答グループの回答のテキストを変更すると、データが評価しにくくなり、アンケートの結果が無効になる場合があります。</span><span class="sxs-lookup"><span data-stu-id="90e7d-181">**Note:** If you modify answer text in answer groups that have already been used on completed questionnaires, data can become difficult to evaluate, and questionnaire results might no longer be valid.</span></span> <span data-ttu-id="90e7d-182">回答グループを変更する必要がある場合、既存の回答グループを変更するのではなく新しく作成することを検討してください。</span><span class="sxs-lookup"><span data-stu-id="90e7d-182">If you must change an answer group, consider creating a new answer group instead of changing an existing one.</span></span> <span data-ttu-id="90e7d-183">質問や回答に関連付けられている回答グループ、あるいは既に回答が行われた回答グループは削除できません。</span><span class="sxs-lookup"><span data-stu-id="90e7d-183">You can't delete answer groups that are attached to a question or answer, or that have been answered.</span></span>

### <a name="questions"></a><span data-ttu-id="90e7d-184">質問</span><span class="sxs-lookup"><span data-stu-id="90e7d-184">Questions</span></span>

<span data-ttu-id="90e7d-185">アンケートには質問が含まれている必要があります。</span><span class="sxs-lookup"><span data-stu-id="90e7d-185">A questionnaire must contain questions.</span></span> <span data-ttu-id="90e7d-186">質問は自由回答式または選択式のいずれかで行うことができます。</span><span class="sxs-lookup"><span data-stu-id="90e7d-186">Questions can be either open-ended or closed-ended.</span></span>

-   <span data-ttu-id="90e7d-187">自由回答式の質問に対する回答は管理されておらず、回答者が自分の回答を入力できます。</span><span class="sxs-lookup"><span data-stu-id="90e7d-187">The responses to open-ended questions aren't controlled, and respondents can type their answers.</span></span>
-   <span data-ttu-id="90e7d-188">選択式の質問では、定義された回答オプションの一覧が必要とされ、回答者が複数の回答を選択できるように質問を構築できます。</span><span class="sxs-lookup"><span data-stu-id="90e7d-188">Closed-ended questions require a list of predefined response options, and the questions can be structured to let a respondent select multiple responses.</span></span> <span data-ttu-id="90e7d-189">質問は、回答者から具体的な情報を引き出せるように意図して作成する必要があり、選択式の質問に回答オプションを提供する回答グループにリンクする必要があります。</span><span class="sxs-lookup"><span data-stu-id="90e7d-189">Questions should be designed to elicit specific information from a respondent and must be linked to an answer group that provides the response options for each closed-ended question.</span></span> 
     -  <span data-ttu-id="90e7d-190">**メモ:** 選択式の質問を設定する前に、回答グループと回答を作成する必要があります。</span><span class="sxs-lookup"><span data-stu-id="90e7d-190">**Note:** Before you can set up closed-ended questions, you must create answer groups and answers.</span></span>

<span data-ttu-id="90e7d-191">質問は、条件付き質問階層で整理することができ、それによって、副質問が前の質問に対する回答者が選択した回答に依存するようになります。</span><span class="sxs-lookup"><span data-stu-id="90e7d-191">Questions can be arranged in a conditional question hierarchy, so that secondary questions depend on the answer that the respondent selects for the previous question.</span></span> <span data-ttu-id="90e7d-192">最初に質問を記述し、後で階層に整理できます。</span><span class="sxs-lookup"><span data-stu-id="90e7d-192">You can write the questions first and then arrange them into a hierarchy later.</span></span>

## <a name="setting-up-questionnaires"></a><span data-ttu-id="90e7d-193">アンケートの設定</span><span class="sxs-lookup"><span data-stu-id="90e7d-193">Setting up questionnaires</span></span>
<span data-ttu-id="90e7d-194">**メモ:** アンケートを設定する前に、アンケートの回答、質問、および前提条件を設定する必要があります。</span><span class="sxs-lookup"><span data-stu-id="90e7d-194">**Note:** Before you can set up a questionnaire, you must set up answers, questions, and prerequisites.</span></span> 

<span data-ttu-id="90e7d-195">各アンケートに対し、次の情報を指定できます。</span><span class="sxs-lookup"><span data-stu-id="90e7d-195">For each questionnaire, you can specify the following information:</span></span>

-   <span data-ttu-id="90e7d-196">必須の質問に回答するための合計時間または時間制限。</span><span class="sxs-lookup"><span data-stu-id="90e7d-196">The total time or time limit to answer mandatory questions.</span></span>
-   <span data-ttu-id="90e7d-197">すべての質問が必須かどうか。</span><span class="sxs-lookup"><span data-stu-id="90e7d-197">Whether all questions are mandatory.</span></span>
-   <span data-ttu-id="90e7d-198">アンケートのポイントを計算するかどうか。</span><span class="sxs-lookup"><span data-stu-id="90e7d-198">Whether to calculate points on a questionnaire.</span></span>
-   <span data-ttu-id="90e7d-199">結果を分類する方法。</span><span class="sxs-lookup"><span data-stu-id="90e7d-199">How to categorize results.</span></span>
-   <span data-ttu-id="90e7d-200">アンケートは一連の限定された回答者が使用可能かどうか。</span><span class="sxs-lookup"><span data-stu-id="90e7d-200">Whether the questionnaire will be available to a restricted set of respondents.</span></span>
-   <span data-ttu-id="90e7d-201">フォーム テンプレートをアンケートの各ページのバックグラウンドとして表示するべきかどうか。</span><span class="sxs-lookup"><span data-stu-id="90e7d-201">Whether a form template should be displayed as a background behind each page of the questionnaire.</span></span>
-   <span data-ttu-id="90e7d-202">回答者にアンケートの目的を明らかにするための追加の注記が必要かどうか。</span><span class="sxs-lookup"><span data-stu-id="90e7d-202">Whether additional notes are required in order to clarify the intent of the questionnaire for the respondents.</span></span>
-   <span data-ttu-id="90e7d-203">質問を固定された順で表示するか、プールからランダムに選択するか。</span><span class="sxs-lookup"><span data-stu-id="90e7d-203">Whether to display questions in a fixed order or randomly select them from a pool.</span></span>
-   <span data-ttu-id="90e7d-204">前の回答に対して特定の回答がされた場合にのみ質問を出題するか。</span><span class="sxs-lookup"><span data-stu-id="90e7d-204">Whether questions will be asked only if specific responses are given for previous answers.</span></span>

### <a name="set-up-a-questionnaire"></a><span data-ttu-id="90e7d-205">アンケートの設定</span><span class="sxs-lookup"><span data-stu-id="90e7d-205">Set up a questionnaire</span></span>

<span data-ttu-id="90e7d-206">アンケートの設定に主に使用するページは [**アンケート**] ページです。</span><span class="sxs-lookup"><span data-stu-id="90e7d-206">The primary page that you use to set up a questionnaire is the **Questionnaires** page.</span></span> <span data-ttu-id="90e7d-207">アンケートを設定するには、次のタスクを順に実行します。</span><span class="sxs-lookup"><span data-stu-id="90e7d-207">To set up a questionnaire, complete the following tasks in order:</span></span>

1.  <span data-ttu-id="90e7d-208">アンケートを作成します。</span><span class="sxs-lookup"><span data-stu-id="90e7d-208">Create a questionnaire.</span></span>
2.  <span data-ttu-id="90e7d-209">アンケートに質問を関連付けるには、次の手順の 1 つを実行します。</span><span class="sxs-lookup"><span data-stu-id="90e7d-209">Follow one of these steps to attach questions to the questionnaire:</span></span>
    -   <span data-ttu-id="90e7d-210">結果グループを使用すると、結果グループを使用してアンケートに質問を関連付けることができます。</span><span class="sxs-lookup"><span data-stu-id="90e7d-210">If you're using result groups, you can attach questions to a questionnaire by using result groups.</span></span> <span data-ttu-id="90e7d-211">最初にアンケートの結果グループを設定し、後で結果グループに質問を追加します。</span><span class="sxs-lookup"><span data-stu-id="90e7d-211">First set up the result groups for the questionnaire, and then add questions to the result groups.</span></span>
    -   <span data-ttu-id="90e7d-212">結果グループを使用しない場合、質問をそのアンケートに直接関連付けることができます。</span><span class="sxs-lookup"><span data-stu-id="90e7d-212">If you aren't using result groups, you can attach questions directly to the questionnaire.</span></span>

3.  <span data-ttu-id="90e7d-213">必要な場合、条件付き質問階層を設定します。</span><span class="sxs-lookup"><span data-stu-id="90e7d-213">Set up a conditional question hierarchy, if it's required.</span></span>
4.  <span data-ttu-id="90e7d-214">アンケートをテストします。</span><span class="sxs-lookup"><span data-stu-id="90e7d-214">Test the questionnaire.</span></span>

<span data-ttu-id="90e7d-215">[**アンケート**] ページで [**検証**] をクリックすると、アンケートが正しく作成されているかどうかをテストできます。</span><span class="sxs-lookup"><span data-stu-id="90e7d-215">On the **Questionnaires** page, click **Validate** to test whether the questionnaire is assembled correctly.</span></span> <span data-ttu-id="90e7d-216">ただし、それを配分する前に、自分でアンケートを完了してテストすることは良い考えです。</span><span class="sxs-lookup"><span data-stu-id="90e7d-216">However, it's also a good idea to complete the questionnaire and test it yourself before you distribute it.</span></span>

### <a name="modify-a-questionnaire"></a><span data-ttu-id="90e7d-217">アンケートの変更</span><span class="sxs-lookup"><span data-stu-id="90e7d-217">Modify a questionnaire</span></span>

<span data-ttu-id="90e7d-218">[**アンケート**] ページで、次の作業を実行できます。</span><span class="sxs-lookup"><span data-stu-id="90e7d-218">You can complete the following tasks on the **Questionnaires** page:</span></span>

-   <span data-ttu-id="90e7d-219">結果グループや質問などの、アンケートの情報を編集します。</span><span class="sxs-lookup"><span data-stu-id="90e7d-219">Modify information in the questionnaire, such as the result groups and questions.</span></span>
-   <span data-ttu-id="90e7d-220">質問を削除および追加します。</span><span class="sxs-lookup"><span data-stu-id="90e7d-220">Delete and add questions.</span></span>
-   <span data-ttu-id="90e7d-221">結果グループおよびシーケンス番号に変更を加えることができます。</span><span class="sxs-lookup"><span data-stu-id="90e7d-221">Make changes in the result groups and sequence number.</span></span> 

<span data-ttu-id="90e7d-222">**注意:** 既に回答のあったアンケートに変更を加える場合は注意が必要です。</span><span class="sxs-lookup"><span data-stu-id="90e7d-222">**Caution:** Be careful when you change questionnaires that have already been answered.</span></span> <span data-ttu-id="90e7d-223">変更により統計の正確さが損なわれ、評価の基準として使用できなくなる可能性があります。</span><span class="sxs-lookup"><span data-stu-id="90e7d-223">Changes can reduce the accuracy of statistics and therefore make them a poor basis for evaluation.</span></span> <span data-ttu-id="90e7d-224">既に回答のあった質問を変更する代わりに、新しい質問を作成することを検討してください。</span><span class="sxs-lookup"><span data-stu-id="90e7d-224">Consider creating a new question instead of changing a question that has already been answered.</span></span>

<span data-ttu-id="90e7d-225">アンケートでは、次の質問のタイプは削除できません。</span><span class="sxs-lookup"><span data-stu-id="90e7d-225">In a questionnaire, you can't delete the following types of questions:</span></span>

-   <span data-ttu-id="90e7d-226">アンケートに関連付けられた質問</span><span class="sxs-lookup"><span data-stu-id="90e7d-226">Questions that are attached to a questionnaire</span></span>
-   <span data-ttu-id="90e7d-227">既に回答のあった質問で、[**回答**] ダイアログ ボックス内に表示されている質問。</span><span class="sxs-lookup"><span data-stu-id="90e7d-227">Questions that have already been answered and therefore appear in the **Answers** dialog box.</span></span>

### <a name="result-groups"></a><span data-ttu-id="90e7d-228">結果グループ</span><span class="sxs-lookup"><span data-stu-id="90e7d-228">Result groups</span></span>

<span data-ttu-id="90e7d-229">結果グループは、アンケートに質問を関連付けるときのオプションです。</span><span class="sxs-lookup"><span data-stu-id="90e7d-229">Result groups are optional when you attach questions to a questionnaire.</span></span> 

<span data-ttu-id="90e7d-230">結果グループは、ポイントを計算し、アンケートの結果を分類するために使用されます。</span><span class="sxs-lookup"><span data-stu-id="90e7d-230">A result group is used to calculate points and categorize the results of a questionnaire.</span></span> <span data-ttu-id="90e7d-231">結果グループを使用すると、次の作業を実行できます。</span><span class="sxs-lookup"><span data-stu-id="90e7d-231">If you use result groups, you can perform the following tasks:</span></span>

-   <span data-ttu-id="90e7d-232">ポイント統計に基づいてアンケートの結果を評価します。</span><span class="sxs-lookup"><span data-stu-id="90e7d-232">Evaluate questionnaire results, based on point statistics.</span></span>
-   <span data-ttu-id="90e7d-233">設定した各結果グループの回答者のスコアを評価します。</span><span class="sxs-lookup"><span data-stu-id="90e7d-233">Evaluate a respondent’s score for each result group that you set up.</span></span>
-   <span data-ttu-id="90e7d-234">結果の分析に役立つ結果グループごとの統計を生成します。</span><span class="sxs-lookup"><span data-stu-id="90e7d-234">Generate statistics for each result group to help you analyze results.</span></span>
-   <span data-ttu-id="90e7d-235">各結果グループの結果、および各結果グループ内で獲得したポイントに基づくオプション ポイント/テキストを示すレポートを印刷します。</span><span class="sxs-lookup"><span data-stu-id="90e7d-235">Print a report that shows results for each result group, and also optional points/texts that are based on points that are earned in each result group.</span></span>

<span data-ttu-id="90e7d-236">**メモ:** 結果グループを設定できるようにするには、その前に次のタスクを完了する必要があります。</span><span class="sxs-lookup"><span data-stu-id="90e7d-236">**Note:** Before you can set up result groups, you must complete the following tasks:</span></span>

-   <span data-ttu-id="90e7d-237">選択式の質問を設定します。</span><span class="sxs-lookup"><span data-stu-id="90e7d-237">Set up closed-ended questions.</span></span> <span data-ttu-id="90e7d-238">選択式の質問には、[**質問**] ページの入力タイプが [**チェック ボックス**]、[**代替ボタン**]、または [**コンボ ボックス**] である必要があります。</span><span class="sxs-lookup"><span data-stu-id="90e7d-238">For a closed-ended question, the input type on the **Questions** page must be **Check box**, **Alternative button**, or **Combo box**.</span></span>
-   <span data-ttu-id="90e7d-239">それぞれの質問に割り当てられた回答グループの回答に対してポイントを定義します。</span><span class="sxs-lookup"><span data-stu-id="90e7d-239">Define points for answers in the answer groups that are assigned to each question.</span></span>
-   <span data-ttu-id="90e7d-240">アンケートを設定します。</span><span class="sxs-lookup"><span data-stu-id="90e7d-240">Set up a questionnaire.</span></span>

<span data-ttu-id="90e7d-241">結果グループを使用してアンケートに質問を関連付けるには、アンケートの結果グループを設定し、結果グループに質問を追加します。</span><span class="sxs-lookup"><span data-stu-id="90e7d-241">To attach questions to a questionnaire by using result groups, first set up the result groups for the questionnaire, and then add questions to the result groups.</span></span> <span data-ttu-id="90e7d-242">結果グループを使用しない場合、質問をアンケートに直接関連付けることができます。</span><span class="sxs-lookup"><span data-stu-id="90e7d-242">If you don't use result groups, you can attach questions directly to a questionnaire.</span></span> 

<span data-ttu-id="90e7d-243">各カテゴリの回答者が獲得したポイントを評価するため、複数の結果グループを設定できます。</span><span class="sxs-lookup"><span data-stu-id="90e7d-243">You can set up multiple result groups to evaluate the points that a respondent earns in each category.</span></span> <span data-ttu-id="90e7d-244">アンケートの完了後に、各結果グループで獲得したポイントを表示できます。</span><span class="sxs-lookup"><span data-stu-id="90e7d-244">After a questionnaire is completed, you can view the points that have been achieved for each result group.</span></span> 

<span data-ttu-id="90e7d-245">**ヒント:** 別のカテゴリではなく、ポイントを使用してアンケートを評価するには、1 つの結果グループすべたの質問を加えることができます。</span><span class="sxs-lookup"><span data-stu-id="90e7d-245">**Tip:** To evaluate a questionnaire by using points but not separate categories, you can add all questions to a single result group.</span></span> 

<span data-ttu-id="90e7d-246">各結果グループでは、アンケート完了後に回答者が受け取るポイント ベース メッセージを 1 つ以上設定できます。</span><span class="sxs-lookup"><span data-stu-id="90e7d-246">For each result group, you can also set up one or more point-based messages that respondents receive after they complete a questionnaire.</span></span> <span data-ttu-id="90e7d-247">表示されるテキストは、回答者が結果グループ内で獲得するスコアによって異なる場合があります。</span><span class="sxs-lookup"><span data-stu-id="90e7d-247">The text that is shown can vary, depending on the score that a respondent achieves in a result group.</span></span> <span data-ttu-id="90e7d-248">ポイント ベース メッセージを使用するには、ポイントの間隔および各間隔の説明を定義する必要があります。</span><span class="sxs-lookup"><span data-stu-id="90e7d-248">To use point-based messages, you must define point intervals and a description of each interval.</span></span> <span data-ttu-id="90e7d-249">回答者が特定の間隔でスコアを獲得すると、その間隔のテキストが結果レポートに含まれます。</span><span class="sxs-lookup"><span data-stu-id="90e7d-249">When a respondent achieves a score in a specific interval, the text for that interval is included on the results report.</span></span> 

<span data-ttu-id="90e7d-250">結果グループはアンケートの特定の質問集に関連付けられている点数に関連するため、アンケートに対して特定の結果グループのみを使用できます。</span><span class="sxs-lookup"><span data-stu-id="90e7d-250">Because a result group is related to the points that are associated with specific sets of questions on a questionnaire, you can use only a specific result group for a questionnaire.</span></span>

#### <a name="example-pointstexts-for-result-group-3"></a><span data-ttu-id="90e7d-251">例: 結果グループ 3 のポイント/テキスト</span><span class="sxs-lookup"><span data-stu-id="90e7d-251">Example: Points/texts for result group 3</span></span>

<span data-ttu-id="90e7d-252">3 つのカテゴリに 15 の質問があるリーダーシップのテストに対してアンケートを使用します。</span><span class="sxs-lookup"><span data-stu-id="90e7d-252">You're using a questionnaire for a leadership test that has 15 questions in three categories.</span></span> <span data-ttu-id="90e7d-253">3 つの結果グループを作成し、各結果グループに 5 つの質問を追加します。</span><span class="sxs-lookup"><span data-stu-id="90e7d-253">You create three result groups and add five questions to each result group.</span></span> <span data-ttu-id="90e7d-254">3 つのグループのポイントが合計されます。</span><span class="sxs-lookup"><span data-stu-id="90e7d-254">Points are then totaled in the three groups.</span></span> <span data-ttu-id="90e7d-255">3 つの結果グループは次のとおりです。</span><span class="sxs-lookup"><span data-stu-id="90e7d-255">The three result groups are as follows:</span></span>

-   <span data-ttu-id="90e7d-256">創造力</span><span class="sxs-lookup"><span data-stu-id="90e7d-256">Creative abilities</span></span>
-   <span data-ttu-id="90e7d-257">指導力</span><span class="sxs-lookup"><span data-stu-id="90e7d-257">Leadership abilities</span></span>
-   <span data-ttu-id="90e7d-258">技術力</span><span class="sxs-lookup"><span data-stu-id="90e7d-258">Technical abilities</span></span>

<span data-ttu-id="90e7d-259">ポイント ベース メッセージを使用するには、各結果グループのテキスト間隔を設定できます。</span><span class="sxs-lookup"><span data-stu-id="90e7d-259">To use point-based messages, you set up text intervals for each result group.</span></span> <span data-ttu-id="90e7d-260">各質問に、2 ポイントが割り当てられます。</span><span class="sxs-lookup"><span data-stu-id="90e7d-260">Each question is assigned two points.</span></span> <span data-ttu-id="90e7d-261">したがって、各結果グループの最高ポイントの合計は、10 です。</span><span class="sxs-lookup"><span data-stu-id="90e7d-261">Therefore, the maximum point total in each result group is 10.</span></span> 

<span data-ttu-id="90e7d-262">次の表では、「指導能力」の結果グループに対して定義されるポイント ベースのメッセージが示されます。</span><span class="sxs-lookup"><span data-stu-id="90e7d-262">The following table shows the point-based messages that you define for the “leadership abilities” result group.</span></span>

| <span data-ttu-id="90e7d-263">ポイントの範囲</span><span class="sxs-lookup"><span data-stu-id="90e7d-263">Point interval</span></span> | <span data-ttu-id="90e7d-264">テキスト</span><span class="sxs-lookup"><span data-stu-id="90e7d-264">Text</span></span>                                       |
|----------------|--------------------------------------------|
| <span data-ttu-id="90e7d-265">1 ～ 3</span><span class="sxs-lookup"><span data-stu-id="90e7d-265">1 to 3</span></span>         | <span data-ttu-id="90e7d-266">平均的な指導力があります。</span><span class="sxs-lookup"><span data-stu-id="90e7d-266">You have average leadership abilities.</span></span>     |
| <span data-ttu-id="90e7d-267">4 ～ 7</span><span class="sxs-lookup"><span data-stu-id="90e7d-267">4 to 7</span></span>         | <span data-ttu-id="90e7d-268">優秀な指導力があります。</span><span class="sxs-lookup"><span data-stu-id="90e7d-268">You have good leadership abilities.</span></span>        |
| <span data-ttu-id="90e7d-269">8 ～ 10</span><span class="sxs-lookup"><span data-stu-id="90e7d-269">8 to 10</span></span>        | <span data-ttu-id="90e7d-270">きわめて優秀な指導力があります。</span><span class="sxs-lookup"><span data-stu-id="90e7d-270">You have outstanding leadership abilities.</span></span> |

<span data-ttu-id="90e7d-271">アンケートの各結果グループに、ポイント範囲およびテキストを設定できます。</span><span class="sxs-lookup"><span data-stu-id="90e7d-271">You can set up point intervals and texts for each result group on a questionnaire.</span></span> <span data-ttu-id="90e7d-272">各回答者のスコアに対応するテキストが、各結果グループに表示されます。</span><span class="sxs-lookup"><span data-stu-id="90e7d-272">Texts that correspond to each respondent’s score are displayed for each result group.</span></span> 

<span data-ttu-id="90e7d-273">**メモ:** 範囲やテキストは変更できます。</span><span class="sxs-lookup"><span data-stu-id="90e7d-273">**Note:** You can change intervals and texts.</span></span> <span data-ttu-id="90e7d-274">ただし、アンケートが完了した後に変更を加えると、先回の結果レポートと新しい結果レポートとの間で不一致が発生します。</span><span class="sxs-lookup"><span data-stu-id="90e7d-274">However, if a questionnaire has been completed, changes might cause differences between previous and new result reports.</span></span>

### <a name="conditional-question-hierarchies"></a><span data-ttu-id="90e7d-275">条件付き質問の階層</span><span class="sxs-lookup"><span data-stu-id="90e7d-275">Conditional question hierarchies</span></span>

<span data-ttu-id="90e7d-276">条件付き質問階層は、アンケート設定時のオプションです。</span><span class="sxs-lookup"><span data-stu-id="90e7d-276">Conditional question hierarchies are optional when you set up a questionnaire.</span></span> 

<span data-ttu-id="90e7d-277">**メモ:** 条件付き質問階層を設定するには、割り当てられている回答グループを伴う質問をアンケートに関連付けておく必要があります。</span><span class="sxs-lookup"><span data-stu-id="90e7d-277">**Note:** Before you can set up a conditional question hierarchy, you must attach questions that have assigned answer groups to the questionnaire.</span></span> 

<span data-ttu-id="90e7d-278">アンケートの質問階層を作成するために条件付き質問を使用するには、それぞれの質問に対して回答者が選択した回答に応じて提示される質問の順序を作成できます。</span><span class="sxs-lookup"><span data-stu-id="90e7d-278">To use conditional questions to create a question hierarchy in a questionnaire, you can make the sequence that questions are presented in depend on the answer that a respondent selects for each question.</span></span> <span data-ttu-id="90e7d-279">回答者の回答に基づいて質問の順序を決定することにより、回答者の回答中にアンケートを変更できます。</span><span class="sxs-lookup"><span data-stu-id="90e7d-279">By basing the question sequence on a respondent’s answer, you can modify the questionnaire as the respondent completes it.</span></span>

#### <a name="examples"></a><span data-ttu-id="90e7d-280">例</span><span class="sxs-lookup"><span data-stu-id="90e7d-280">Examples</span></span>

<span data-ttu-id="90e7d-281">法人が顧客に品目およびサービスの両方を提供します。</span><span class="sxs-lookup"><span data-stu-id="90e7d-281">A legal entity offers both items and services to its customers.</span></span> <span data-ttu-id="90e7d-282">この場合は通常、一部の顧客は品目のみやサービスのみを購入する場合もあれば、品目とサービスの両方を購入する場合もあります。</span><span class="sxs-lookup"><span data-stu-id="90e7d-282">As typically occurs in such cases, some customers purchase only items, some purchase only services, and some purchase both items and services.</span></span> <span data-ttu-id="90e7d-283">したがって、法人が顧客満足度調査を配布するときは、サービスだけを購入する顧客が品目に関する質問に回答しなくて済むように、アンケートに条件付き構造を適用できます。</span><span class="sxs-lookup"><span data-stu-id="90e7d-283">Therefore, when the legal entity distributes a customer satisfaction survey, it applies a conditional structure to the questionnaire, so that customers who purchase only services don't have to answer questions about items.</span></span> 

<span data-ttu-id="90e7d-284">または、回答者が質問 1 に対して回答 A を選択する場合には、質問 2 が次の質問の順序であるように、アンケートを設定できます。</span><span class="sxs-lookup"><span data-stu-id="90e7d-284">Alternatively, you set up a questionnaire so that if a respondent selects answer A for question 1, question 2 is next in the question sequence.</span></span> <span data-ttu-id="90e7d-285">ただし、回答者が質問 1 に対して回答 B を選択した場合には、質問 5 が次になります。</span><span class="sxs-lookup"><span data-stu-id="90e7d-285">However, if the respondent selects answer B for question 1, question 5 is next.</span></span>

<a name="see-also"></a><span data-ttu-id="90e7d-286">参照</span><span class="sxs-lookup"><span data-stu-id="90e7d-286">See also</span></span>
--------

[<span data-ttu-id="90e7d-287">アンケートの使用</span><span class="sxs-lookup"><span data-stu-id="90e7d-287">Using questionnaires</span></span>](questionnaires.md)

[<span data-ttu-id="90e7d-288">アンケートの配布および記入</span><span class="sxs-lookup"><span data-stu-id="90e7d-288">Distributing and completing questionnaires</span></span>](distribute-questionnaires.md)

[<span data-ttu-id="90e7d-289">アンケート結果を表示して評価する</span><span class="sxs-lookup"><span data-stu-id="90e7d-289">Viewing and evaluating the results of questionnaires</span></span>](evaluate-questionnaire-results.md)


