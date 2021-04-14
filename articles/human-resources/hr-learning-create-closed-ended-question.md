---
title: 選択式の質問の作成
description: 選択式の質問には、回答者が選択できるためのオプションが用意されます。
author: andreabichsel
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: KMAnswerCollection, KMAnswer, KMQuestion, HcmLearningWorkspace
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Human Resources
ms.search.region: Global
ms.author: anbichse
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 41e12e6f35237ea125756b502d5cebed58c6bf55
ms.sourcegitcommit: 3cdc42346bb653c13ab33a7142dbb7969f1f6dda
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 03/31/2021
ms.locfileid: "5790647"
---
# <a name="create-a-closed-ended-question"></a><span data-ttu-id="cf52f-103">選択式の質問の作成</span><span class="sxs-lookup"><span data-stu-id="cf52f-103">Create a closed ended question</span></span>

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]



<span data-ttu-id="cf52f-104">選択式の質問には、回答者が選択できるためのオプションが用意されます。</span><span class="sxs-lookup"><span data-stu-id="cf52f-104">Closed-ended questions allow you to provide options for the respondent to choose from.</span></span> <span data-ttu-id="cf52f-105">最初に、回答と回答グループを作成する必要があり、その後回答グループを使用する質問を作成します。</span><span class="sxs-lookup"><span data-stu-id="cf52f-105">First, you need to create the Answer group with the answers, then create the question that will use the answer group.</span></span> <span data-ttu-id="cf52f-106">この手順の作成に使用するデモ データの会社は USMF です。</span><span class="sxs-lookup"><span data-stu-id="cf52f-106">The demo data company used to create this procedure is USMF.</span></span>


## <a name="create-an-answer-group"></a><span data-ttu-id="cf52f-107">回答グループの作成</span><span class="sxs-lookup"><span data-stu-id="cf52f-107">Create an answer group</span></span>
1. <span data-ttu-id="cf52f-108">[アンケート] > [設計] > [回答グループ] の順に移動します。</span><span class="sxs-lookup"><span data-stu-id="cf52f-108">Go to Questionnaire > Design > Answer groups.</span></span>
2. <span data-ttu-id="cf52f-109">[新規] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="cf52f-109">Click New.</span></span>
3. <span data-ttu-id="cf52f-110">[回答グループ] フィールドに値を入力します。</span><span class="sxs-lookup"><span data-stu-id="cf52f-110">In the Answer group field, type a value.</span></span>
4. <span data-ttu-id="cf52f-111">[説明] フィールドに値を入力します。</span><span class="sxs-lookup"><span data-stu-id="cf52f-111">In the Description field, type a value.</span></span>
    * <span data-ttu-id="cf52f-112">回答グループが質問に使用されるたびに、必要に応じて別の順序で回答をランダムに設定するランダム化機能を使用します。</span><span class="sxs-lookup"><span data-stu-id="cf52f-112">Use the Randomize functionality to randomly place the answers in a different order each time the answer group is used for a question.</span></span>  
5. <span data-ttu-id="cf52f-113">[回答] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="cf52f-113">Click Answer.</span></span>
6. <span data-ttu-id="cf52f-114">[新規] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="cf52f-114">Click New.</span></span>
    * <span data-ttu-id="cf52f-115">ランダム化機能が回答グループに対して選択されている場合を除いて、番号順序は回答が表示される順序を制御します。</span><span class="sxs-lookup"><span data-stu-id="cf52f-115">Sequence number controls the order in which the answers are displayed, unless Randomize is selected for the Answer group.</span></span>  
    * <span data-ttu-id="cf52f-116">アンケートの採点に対して回答するために、ポイントは支給できます。</span><span class="sxs-lookup"><span data-stu-id="cf52f-116">Points can be awarded to answers for use in scoring the questionnaire.</span></span>  
7. <span data-ttu-id="cf52f-117">[点数] フィールドに数値を入力します。</span><span class="sxs-lookup"><span data-stu-id="cf52f-117">In the Points field, enter a number.</span></span>
    * <span data-ttu-id="cf52f-118">正解な回答をマークし、選択した回答が正しいものであることを表示できます。</span><span class="sxs-lookup"><span data-stu-id="cf52f-118">The correct answer can be marked to indicate that the selected answer is the correct one.</span></span> <span data-ttu-id="cf52f-119">これは、アンケートの採点に使用できます。</span><span class="sxs-lookup"><span data-stu-id="cf52f-119">This can be used for scoring the questionnaire.</span></span>  
8. <span data-ttu-id="cf52f-120">[回答] フィールドに値を入力します。</span><span class="sxs-lookup"><span data-stu-id="cf52f-120">In the Answer field, type a value.</span></span>
    * <span data-ttu-id="cf52f-121">回答グループに対して選択できる回答オプションを作成し続けます。</span><span class="sxs-lookup"><span data-stu-id="cf52f-121">Continue to create answer selection options for the answer group.</span></span>  
9. <span data-ttu-id="cf52f-122">[新規] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="cf52f-122">Click New.</span></span>
10. <span data-ttu-id="cf52f-123">[点数] フィールドに数値を入力します。</span><span class="sxs-lookup"><span data-stu-id="cf52f-123">In the Points field, enter a number.</span></span>
11. <span data-ttu-id="cf52f-124">[回答] フィールドに値を入力します。</span><span class="sxs-lookup"><span data-stu-id="cf52f-124">In the Answer field, type a value.</span></span>
12. <span data-ttu-id="cf52f-125">[新規] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="cf52f-125">Click New.</span></span>
13. <span data-ttu-id="cf52f-126">[点数] フィールドに数値を入力します。</span><span class="sxs-lookup"><span data-stu-id="cf52f-126">In the Points field, enter a number.</span></span>
14. <span data-ttu-id="cf52f-127">[回答] フィールドに値を入力します。</span><span class="sxs-lookup"><span data-stu-id="cf52f-127">In the Answer field, type a value.</span></span>
15. <span data-ttu-id="cf52f-128">[新規] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="cf52f-128">Click New.</span></span>
16. <span data-ttu-id="cf52f-129">[点数] フィールドに数値を入力します。</span><span class="sxs-lookup"><span data-stu-id="cf52f-129">In the Points field, enter a number.</span></span>
17. <span data-ttu-id="cf52f-130">[回答] フィールドに値を入力します。</span><span class="sxs-lookup"><span data-stu-id="cf52f-130">In the Answer field, type a value.</span></span>
18. <span data-ttu-id="cf52f-131">[新規] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="cf52f-131">Click New.</span></span>
19. <span data-ttu-id="cf52f-132">[点数] フィールドに数値を入力します。</span><span class="sxs-lookup"><span data-stu-id="cf52f-132">In the Points field, enter a number.</span></span>
20. <span data-ttu-id="cf52f-133">[回答] フィールドに値を入力します。</span><span class="sxs-lookup"><span data-stu-id="cf52f-133">In the Answer field, type a value.</span></span>
21. <span data-ttu-id="cf52f-134">ページを閉じます。</span><span class="sxs-lookup"><span data-stu-id="cf52f-134">Close the page.</span></span>
22. <span data-ttu-id="cf52f-135">ページを閉じます。</span><span class="sxs-lookup"><span data-stu-id="cf52f-135">Close the page.</span></span>

## <a name="create-the-question"></a><span data-ttu-id="cf52f-136">質問の作成</span><span class="sxs-lookup"><span data-stu-id="cf52f-136">Create the question</span></span>
1. <span data-ttu-id="cf52f-137">[アンケート] > [設計] > [質問] の順に移動します。</span><span class="sxs-lookup"><span data-stu-id="cf52f-137">Go to Questionnaire > Design > Questions.</span></span>
2. <span data-ttu-id="cf52f-138">[新規] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="cf52f-138">Click New.</span></span>
3. <span data-ttu-id="cf52f-139">[タイプ] フィールドを使用して、関連の質問をグループ化します。</span><span class="sxs-lookup"><span data-stu-id="cf52f-139">Use the Type field to group related questions together.</span></span>
    * <span data-ttu-id="cf52f-140">選択式の質問の場合は、チェック ボックス、代替ボタン、またはコンボ ボックスの入力タイプを使用できます。</span><span class="sxs-lookup"><span data-stu-id="cf52f-140">You can use input types of Check box, Alternative button, or Combo box for closed-ended questions.</span></span>  
4. <span data-ttu-id="cf52f-141">[入力タイプ] フィールドで、オプションを選択します。</span><span class="sxs-lookup"><span data-stu-id="cf52f-141">In the Input type field, select an option.</span></span>
5. <span data-ttu-id="cf52f-142">[回答グループ] フィールドで、値を入力または選択します。</span><span class="sxs-lookup"><span data-stu-id="cf52f-142">In the Answer group field, enter or select a value.</span></span>
6. <span data-ttu-id="cf52f-143">[テキスト] フィールドに値を入力します。</span><span class="sxs-lookup"><span data-stu-id="cf52f-143">In the Text field, type a value.</span></span>



[!INCLUDE[footer-include](../includes/footer-banner.md)]