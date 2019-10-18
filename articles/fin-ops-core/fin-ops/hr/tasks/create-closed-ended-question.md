---
title: 選択式の質問の作成
description: 選択式の質問には、回答者が選択できるためのオプションが用意されます。
author: andreabichsel
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: KMAnswerCollection, KMAnswer, KMQuestion
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: anbichse
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 92e4f9697fc00798d917db6f7f50d7e3b8739233
ms.sourcegitcommit: 3ba95d50b8262fa0f43d4faad76adac4d05eb3ea
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 09/27/2019
ms.locfileid: "2178769"
---
# <a name="create-a-closed-ended-question"></a><span data-ttu-id="7b471-103">選択式の質問の作成</span><span class="sxs-lookup"><span data-stu-id="7b471-103">Create a closed ended question</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="7b471-104">選択式の質問には、回答者が選択できるためのオプションが用意されます。</span><span class="sxs-lookup"><span data-stu-id="7b471-104">Closed-ended questions allow you to provide options for the respondent to choose from.</span></span> <span data-ttu-id="7b471-105">最初に、回答と回答グループを作成する必要があり、その後回答グループを使用する質問を作成します。</span><span class="sxs-lookup"><span data-stu-id="7b471-105">First, you need to create the Answer group with the answers, then create the question that will use the answer group.</span></span> <span data-ttu-id="7b471-106">この手順の作成に使用するデモ データの会社は USMF です。</span><span class="sxs-lookup"><span data-stu-id="7b471-106">The demo data company used to create this procedure is USMF.</span></span>


## <a name="create-an-answer-group"></a><span data-ttu-id="7b471-107">回答グループの作成</span><span class="sxs-lookup"><span data-stu-id="7b471-107">Create an answer group</span></span>
1. <span data-ttu-id="7b471-108">[アンケート] > [設計] > [回答グループ] の順に移動します。</span><span class="sxs-lookup"><span data-stu-id="7b471-108">Go to Questionnaire > Design > Answer groups.</span></span>
2. <span data-ttu-id="7b471-109">[新規] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="7b471-109">Click New.</span></span>
3. <span data-ttu-id="7b471-110">[回答グループ] フィールドに値を入力します。</span><span class="sxs-lookup"><span data-stu-id="7b471-110">In the Answer group field, type a value.</span></span>
4. <span data-ttu-id="7b471-111">[説明] フィールドに値を入力します。</span><span class="sxs-lookup"><span data-stu-id="7b471-111">In the Description field, type a value.</span></span>
    * <span data-ttu-id="7b471-112">回答グループが質問に使用されるたびに、必要に応じて別の順序で回答をランダムに設定するランダム化機能を使用します。</span><span class="sxs-lookup"><span data-stu-id="7b471-112">Use the Randomize functionality to randomly place the answers in a different order each time the answer group is used for a question.</span></span>  
5. <span data-ttu-id="7b471-113">[回答] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="7b471-113">Click Answer.</span></span>
6. <span data-ttu-id="7b471-114">[新規] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="7b471-114">Click New.</span></span>
    * <span data-ttu-id="7b471-115">ランダム化機能が回答グループに対して選択されている場合を除いて、番号順序は回答が表示される順序を制御します。</span><span class="sxs-lookup"><span data-stu-id="7b471-115">Sequence number controls the order in which the answers are displayed, unless Randomize is selected for the Answer group.</span></span>  
    * <span data-ttu-id="7b471-116">アンケートの採点に対して回答するために、ポイントは支給できます。</span><span class="sxs-lookup"><span data-stu-id="7b471-116">Points can be awarded to answers for use in scoring the questionnaire.</span></span>  
7. <span data-ttu-id="7b471-117">[点数] フィールドに数値を入力します。</span><span class="sxs-lookup"><span data-stu-id="7b471-117">In the Points field, enter a number.</span></span>
    * <span data-ttu-id="7b471-118">正解な回答をマークし、選択した回答が正しいものであることを表示できます。</span><span class="sxs-lookup"><span data-stu-id="7b471-118">The correct answer can be marked to indicate that the selected answer is the correct one.</span></span> <span data-ttu-id="7b471-119">これは、アンケートの採点に使用できます。</span><span class="sxs-lookup"><span data-stu-id="7b471-119">This can be used for scoring the questionnaire.</span></span>  
8. <span data-ttu-id="7b471-120">[回答] フィールドに値を入力します。</span><span class="sxs-lookup"><span data-stu-id="7b471-120">In the Answer field, type a value.</span></span>
    * <span data-ttu-id="7b471-121">回答グループに対して選択できる回答オプションを作成し続けます。</span><span class="sxs-lookup"><span data-stu-id="7b471-121">Continue to create answer selection options for the answer group.</span></span>  
9. <span data-ttu-id="7b471-122">[新規] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="7b471-122">Click New.</span></span>
10. <span data-ttu-id="7b471-123">[点数] フィールドに数値を入力します。</span><span class="sxs-lookup"><span data-stu-id="7b471-123">In the Points field, enter a number.</span></span>
11. <span data-ttu-id="7b471-124">[回答] フィールドに値を入力します。</span><span class="sxs-lookup"><span data-stu-id="7b471-124">In the Answer field, type a value.</span></span>
12. <span data-ttu-id="7b471-125">[新規] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="7b471-125">Click New.</span></span>
13. <span data-ttu-id="7b471-126">[点数] フィールドに数値を入力します。</span><span class="sxs-lookup"><span data-stu-id="7b471-126">In the Points field, enter a number.</span></span>
14. <span data-ttu-id="7b471-127">[回答] フィールドに値を入力します。</span><span class="sxs-lookup"><span data-stu-id="7b471-127">In the Answer field, type a value.</span></span>
15. <span data-ttu-id="7b471-128">[新規] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="7b471-128">Click New.</span></span>
16. <span data-ttu-id="7b471-129">[点数] フィールドに数値を入力します。</span><span class="sxs-lookup"><span data-stu-id="7b471-129">In the Points field, enter a number.</span></span>
17. <span data-ttu-id="7b471-130">[回答] フィールドに値を入力します。</span><span class="sxs-lookup"><span data-stu-id="7b471-130">In the Answer field, type a value.</span></span>
18. <span data-ttu-id="7b471-131">[新規] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="7b471-131">Click New.</span></span>
19. <span data-ttu-id="7b471-132">[点数] フィールドに数値を入力します。</span><span class="sxs-lookup"><span data-stu-id="7b471-132">In the Points field, enter a number.</span></span>
20. <span data-ttu-id="7b471-133">[回答] フィールドに値を入力します。</span><span class="sxs-lookup"><span data-stu-id="7b471-133">In the Answer field, type a value.</span></span>
21. <span data-ttu-id="7b471-134">ページを閉じます。</span><span class="sxs-lookup"><span data-stu-id="7b471-134">Close the page.</span></span>
22. <span data-ttu-id="7b471-135">ページを閉じます。</span><span class="sxs-lookup"><span data-stu-id="7b471-135">Close the page.</span></span>

## <a name="create-the-question"></a><span data-ttu-id="7b471-136">質問の作成</span><span class="sxs-lookup"><span data-stu-id="7b471-136">Create the question</span></span>
1. <span data-ttu-id="7b471-137">[アンケート] > [設計] > [質問] の順に移動します。</span><span class="sxs-lookup"><span data-stu-id="7b471-137">Go to Questionnaire > Design > Questions.</span></span>
2. <span data-ttu-id="7b471-138">[新規] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="7b471-138">Click New.</span></span>
3. <span data-ttu-id="7b471-139">[タイプ] フィールドを使用して、関連の質問をグループ化します。</span><span class="sxs-lookup"><span data-stu-id="7b471-139">Use the Type field to group related questions together.</span></span>
    * <span data-ttu-id="7b471-140">選択式の質問の場合は、チェック ボックス、代替ボタン、またはコンボ ボックスの入力タイプを使用できます。</span><span class="sxs-lookup"><span data-stu-id="7b471-140">You can use input types of Check box, Alternative button, or Combo box for closed-ended questions.</span></span>  
4. <span data-ttu-id="7b471-141">[入力タイプ] フィールドで、オプションを選択します。</span><span class="sxs-lookup"><span data-stu-id="7b471-141">In the Input type field, select an option.</span></span>
5. <span data-ttu-id="7b471-142">[回答グループ] フィールドで、値を入力または選択します。</span><span class="sxs-lookup"><span data-stu-id="7b471-142">In the Answer group field, enter or select a value.</span></span>
6. <span data-ttu-id="7b471-143">[テキスト] フィールドに値を入力します。</span><span class="sxs-lookup"><span data-stu-id="7b471-143">In the Text field, type a value.</span></span>

