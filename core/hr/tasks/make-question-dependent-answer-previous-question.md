--- 
title: "前の質問の回答に応じた質問の作成"
description: "条件付き質問は、前の質問に対する回答に基づいて、回答者に提供するフォローアップの質問を指定することを可能にします。"
author: twheeloc
manager: AnnBe
ms.date: 02/12/2016
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: rschloma
ms.search.scope: Operations
ms.search.region: Global
ms.author: twheeloc
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 663da58ef01b705c0c984fbfd3fce8bc31be04c6
ms.openlocfilehash: 05f7af94813934c1d77d6a509587280395f0e8bd
ms.contentlocale: ja-jp
ms.lasthandoff: 08/29/2017

---
# <a name="make-a-question-dependent-on-the-answer-of-the-previous-question"></a><span data-ttu-id="29c89-103">前の質問の回答に応じた質問の作成</span><span class="sxs-lookup"><span data-stu-id="29c89-103">Make a question dependent on the answer of the previous question</span></span>

[!include[task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="29c89-104">条件付き質問は、前の質問に対する回答に基づいて、回答者に提供するフォローアップの質問を指定することを可能にします。</span><span class="sxs-lookup"><span data-stu-id="29c89-104">Conditional questions allow you to specify what follow-up question will be presented to a respondent, based on the answer to the preceding question.</span></span> <span data-ttu-id="29c89-105">たとえば、「コーヒーまたは紅茶を選択するか」と質問する場合、回答者がコーヒーまたは紅茶のどちらを回答に選ぶかによって、論理的なフォローアップ質問が特定されます。</span><span class="sxs-lookup"><span data-stu-id="29c89-105">For example, if you ask "Do you prefer coffee or tea," a logical follow-up question can be determined depending on whether the respondent selects coffee or tea as their answer.</span></span> <span data-ttu-id="29c89-106">この手順の作成に使用するデモ データの会社は USMF です。</span><span class="sxs-lookup"><span data-stu-id="29c89-106">The demo data company used to create this procedure is USMF.</span></span>


## <a name="find-the-existing-questionnaire"></a><span data-ttu-id="29c89-107">現在のアンケートを見つけます。</span><span class="sxs-lookup"><span data-stu-id="29c89-107">Find the existing questionnaire</span></span>
1. <span data-ttu-id="29c89-108">[アンケート] > [設計] > [アンケート] の順に移動します。</span><span class="sxs-lookup"><span data-stu-id="29c89-108">Go to Questionnaire > Design > Questionnaires.</span></span>
2. <span data-ttu-id="29c89-109">一覧で、「WorkFH questionnaire」を選択します。</span><span class="sxs-lookup"><span data-stu-id="29c89-109">In the list, select the WorkFH questionnaire.</span></span>

## <a name="add-all-questions-and-sub-questions-to-the-questionnaire"></a><span data-ttu-id="29c89-110">すべての質問と副質問をアンケートに追加する</span><span class="sxs-lookup"><span data-stu-id="29c89-110">Add all questions and sub-questions to the Questionnaire</span></span>
1. <span data-ttu-id="29c89-111">[質問] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="29c89-111">Click Questions.</span></span>
2. <span data-ttu-id="29c89-112">[新規] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="29c89-112">Click New.</span></span>
3. <span data-ttu-id="29c89-113">[質問] フィールドで、質問番号「00016」を選択します。</span><span class="sxs-lookup"><span data-stu-id="29c89-113">In the Question field, select question number 00016.</span></span>
4. <span data-ttu-id="29c89-114">一覧で、目的のレコードを見つけ、選択します。</span><span class="sxs-lookup"><span data-stu-id="29c89-114">In the list, find and select the desired record.</span></span>
5. <span data-ttu-id="29c89-115">一覧で、選択された行のリンクをクリックします。</span><span class="sxs-lookup"><span data-stu-id="29c89-115">In the list, click the link in the selected row.</span></span>
6. <span data-ttu-id="29c89-116">[保存] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="29c89-116">Click Save.</span></span>
7. <span data-ttu-id="29c89-117">ページを閉じます。</span><span class="sxs-lookup"><span data-stu-id="29c89-117">Close the page.</span></span>

## <a name="set-the-questionnaire-sequence-to-conditional-and-make-the-question-dependent-on-the-appropriate-question"></a><span data-ttu-id="29c89-118">アンケート順序を条件に設定し、適切な質問を要求する質問を作成します。</span><span class="sxs-lookup"><span data-stu-id="29c89-118">Set the Questionnaire Sequence to Conditional and make the question dependent on the appropriate question</span></span>
1. <span data-ttu-id="29c89-119">[編集] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="29c89-119">Click Edit.</span></span>
2. <span data-ttu-id="29c89-120">[設定] セクションを展開します。</span><span class="sxs-lookup"><span data-stu-id="29c89-120">Expand the Setup section.</span></span>
3. <span data-ttu-id="29c89-121">[質問の順序] フィールドで、「00016」を選択します。</span><span class="sxs-lookup"><span data-stu-id="29c89-121">In the Question order field, select 'Conditional'.</span></span>
4. <span data-ttu-id="29c89-122">[条件付き質問] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="29c89-122">Click Conditional question.</span></span>
5. <span data-ttu-id="29c89-123">ツリーで、「質問\以前の質問に対してなぜそのように回答したかを説明してください。」を選択します。</span><span class="sxs-lookup"><span data-stu-id="29c89-123">In the tree, select 'Questions\Explain why you answered the previous question the way you did?'.</span></span>
6. <span data-ttu-id="29c89-124">主質問フィールドで、質問「00009」を選択する</span><span class="sxs-lookup"><span data-stu-id="29c89-124">In the Primary question field, select question 00009</span></span>
7. <span data-ttu-id="29c89-125">一覧で、選択された行のリンクをクリックします。</span><span class="sxs-lookup"><span data-stu-id="29c89-125">In the list, click the link in the selected row.</span></span>
8. <span data-ttu-id="29c89-126">[回答] フィールドに、質問が依存する回答オプションの回答順序 ID を入力します。</span><span class="sxs-lookup"><span data-stu-id="29c89-126">In the Answer field, enter the answer sequence ID of the answer option you want to make the question dependent on.</span></span> <span data-ttu-id="29c89-127">たとえば、最初の回答オプションについて、「1」を入力します。</span><span class="sxs-lookup"><span data-stu-id="29c89-127">For example, enter 1 for the first answer option.</span></span>
9. <span data-ttu-id="29c89-128">[保存] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="29c89-128">Click Save.</span></span>
10. <span data-ttu-id="29c89-129">ツリーで、「質問\自分の作業に対して公正な給料をもらっている」を選択します。</span><span class="sxs-lookup"><span data-stu-id="29c89-129">In the tree, select 'Questions\I am paid fairly for the work I do.'.</span></span>
    * <span data-ttu-id="29c89-130">依存関係を表示する更新された質問ツリーに注意します。</span><span class="sxs-lookup"><span data-stu-id="29c89-130">Note that the question tree updated to show the dependency.</span></span>  

