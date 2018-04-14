--- 
title: "定期処理仕訳帳の転記"
description: "定期処理仕訳帳は、繰返しの仕訳帳とも呼ばれ、定期処理仕訳帳を取得するたびに数量、テキスト、およびその他の情報が繰り返されます。"
author: aprilolson
manager: AnnBe
ms.date: 02/24/2016
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: twheeloc
ms.search.scope: Operations
ms.search.region: Global
ms.author: aolson
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: a8b5a5af5108744406a3d2fb84d7151baea2481b
ms.openlocfilehash: 57b73c43be6ef4dda82cb919d4eb83eeae9c3633
ms.contentlocale: ja-jp
ms.lasthandoff: 04/13/2018

---
# <a name="post-periodic-journals"></a><span data-ttu-id="f9851-103">定期処理仕訳帳の転記</span><span class="sxs-lookup"><span data-stu-id="f9851-103">Post periodic journals</span></span>

[!INCLUDE [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="f9851-104">定期処理仕訳帳は、繰返しの仕訳帳とも呼ばれ、定期処理仕訳帳を取得するたびに数量、テキスト、およびその他の情報が繰り返されます。</span><span class="sxs-lookup"><span data-stu-id="f9851-104">Periodic journals are sometimes called recurring journals because the amount, text, and other information are repeated each time that the periodic journal is retrieved.</span></span> <span data-ttu-id="f9851-105">定期処理仕訳帳を作成する場合、日数または月数などの繰り返し間隔を指定します。</span><span class="sxs-lookup"><span data-stu-id="f9851-105">When you create the periodic journal, you specify the period interval for the recurrence, such as days or months.</span></span> <span data-ttu-id="f9851-106">このタスク ガイドでは、月間の繰り返しを持つ定期処理仕訳帳を作成します。</span><span class="sxs-lookup"><span data-stu-id="f9851-106">This task guide will create a periodic journal with a monthly recurrence.</span></span>



1. <span data-ttu-id="f9851-107">[総勘定元帳] > [定期処理タスク] > [定期処理仕訳帳] の順に移動します。</span><span class="sxs-lookup"><span data-stu-id="f9851-107">Go to General ledger > Periodic tasks > Periodic journals.</span></span>
2. <span data-ttu-id="f9851-108">[新規] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="f9851-108">Click New.</span></span>
3. <span data-ttu-id="f9851-109">[名前] フィールドで値を入力または選択します。</span><span class="sxs-lookup"><span data-stu-id="f9851-109">In the Name field, enter or select a value.</span></span>
4. <span data-ttu-id="f9851-110">一覧で、選択された行のリンクをクリックします。</span><span class="sxs-lookup"><span data-stu-id="f9851-110">In the list, click the link in the selected row.</span></span>
5. <span data-ttu-id="f9851-111">[説明] フィールドに値を入力します。</span><span class="sxs-lookup"><span data-stu-id="f9851-111">In the Description field, type a value.</span></span>
    * <span data-ttu-id="f9851-112">説明は、後から取得する場合は定期処理仕訳帳の名前になるため、適切な名前を付けることをお勧めします。</span><span class="sxs-lookup"><span data-stu-id="f9851-112">The description will be the name of the Periodic journal when retrieved later so make sure to give it a relevant name.</span></span>  
6. <span data-ttu-id="f9851-113">[明細行] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="f9851-113">Click Lines.</span></span>
    * <span data-ttu-id="f9851-114">定期処理仕訳帳には通常、複数の仕訳帳明細行が含まれます。</span><span class="sxs-lookup"><span data-stu-id="f9851-114">A periodic journal will typically include several journal lines.</span></span> <span data-ttu-id="f9851-115">ただし、このタスク ガイドでは 1 行のみ追加します。</span><span class="sxs-lookup"><span data-stu-id="f9851-115">this task guide will however only add one line.</span></span>  
7. <span data-ttu-id="f9851-116">[日付] フィールドに日付を入力します。</span><span class="sxs-lookup"><span data-stu-id="f9851-116">In the Date field, enter a date.</span></span>
    * <span data-ttu-id="f9851-117">[日付] フィールドには、次に日次仕訳帳への転送が行われる転記日付が含まれます。</span><span class="sxs-lookup"><span data-stu-id="f9851-117">The Date field contains the posting date for the next transfer to the daily journal.</span></span> <span data-ttu-id="f9851-118">毎月取得する仕訳帳については、転記を行う月内の日付を使用することをお勧めします。通常これは期間の最初または最後の日付です。</span><span class="sxs-lookup"><span data-stu-id="f9851-118">For journals that will be retrieved each month it is recommended to use the date in the month when it will be posted, typically the first or last date in the period.</span></span> <span data-ttu-id="f9851-119">[空の日付] フィールドを使用すると、[日付] フィールドを空のままにして、仕訳帳の取得時に日付を指定することができます。</span><span class="sxs-lookup"><span data-stu-id="f9851-119">It is possible to leave the Date field blank and to give a date when the journal is retrieved, using the Empty date field.</span></span>    <span data-ttu-id="f9851-120">このフィールドは、トランザクションが取得される次の繰り返し日に自動的に更新されます。</span><span class="sxs-lookup"><span data-stu-id="f9851-120">The field is automatically updated to the next recurring date when transactions are retrieved.</span></span>  
8. <span data-ttu-id="f9851-121">[勘定] フィールドで、任意の値を指定します。</span><span class="sxs-lookup"><span data-stu-id="f9851-121">In the Account field, specify the desired values.</span></span>
9. <span data-ttu-id="f9851-122">[説明] フィールドに値を入力します。</span><span class="sxs-lookup"><span data-stu-id="f9851-122">In the Description field, type a value.</span></span>
10. <span data-ttu-id="f9851-123">ページを閉じます。</span><span class="sxs-lookup"><span data-stu-id="f9851-123">Close the page.</span></span>
11. <span data-ttu-id="f9851-124">[借方] フィールドに数値を入力します。</span><span class="sxs-lookup"><span data-stu-id="f9851-124">In the Debit field, enter a number.</span></span>
12. <span data-ttu-id="f9851-125">[相殺勘定] フィールドで、任意の値を指定します。</span><span class="sxs-lookup"><span data-stu-id="f9851-125">In the Offset account field, specify the desired values.</span></span>
13. <span data-ttu-id="f9851-126">[単位] フィールドで、月を選択します。</span><span class="sxs-lookup"><span data-stu-id="f9851-126">In the Unit field, select 'Months'.</span></span>
14. <span data-ttu-id="f9851-127">[単位数] フィールドに「1」を入力します。</span><span class="sxs-lookup"><span data-stu-id="f9851-127">In the Number of units field, enter '1'.</span></span>
15. <span data-ttu-id="f9851-128">[最終日付] フィールドに日付を入力します。</span><span class="sxs-lookup"><span data-stu-id="f9851-128">In the Last date field, enter a date.</span></span>
    * <span data-ttu-id="f9851-129">前の期間内の最後の日付を入力すると、定期的な仕訳帳が誤った開始期間で作成されるのを防ぎます。</span><span class="sxs-lookup"><span data-stu-id="f9851-129">Entering last date in the preceding period will prevent that the recurring journal by mistake is created in the wrong starting period.</span></span> <span data-ttu-id="f9851-130">終了日は、後で定期処理仕訳帳が取得されるたびに更新されます。</span><span class="sxs-lookup"><span data-stu-id="f9851-130">Last date will later on be updated each time the periodic journal is retrieved.</span></span>  
16. <span data-ttu-id="f9851-131">[保存] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="f9851-131">Click Save.</span></span>
17. <span data-ttu-id="f9851-132">[既定のダッシュボード] に移動します。</span><span class="sxs-lookup"><span data-stu-id="f9851-132">Go to Default dashboard.</span></span>
18. <span data-ttu-id="f9851-133">[総勘定元帳] > [総勘定元帳] > [仕訳入力] > [一般仕訳帳] の順に移動します。</span><span class="sxs-lookup"><span data-stu-id="f9851-133">Go to General ledger > Journal entries > General journals.</span></span>
19. <span data-ttu-id="f9851-134">[新規] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="f9851-134">Click New.</span></span>
20. <span data-ttu-id="f9851-135">[名前] フィールドで値を入力または選択します。</span><span class="sxs-lookup"><span data-stu-id="f9851-135">In the Name field, enter or select a value.</span></span>
21. <span data-ttu-id="f9851-136">一覧で、目的のレコードを見つけ、選択します。</span><span class="sxs-lookup"><span data-stu-id="f9851-136">In the list, find and select the desired record.</span></span>
22. <span data-ttu-id="f9851-137">一覧で、選択された行のリンクをクリックします。</span><span class="sxs-lookup"><span data-stu-id="f9851-137">In the list, click the link in the selected row.</span></span>
23. <span data-ttu-id="f9851-138">[説明] フィールドに値を入力します。</span><span class="sxs-lookup"><span data-stu-id="f9851-138">In the Description field, type a value.</span></span>
24. <span data-ttu-id="f9851-139">[明細行] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="f9851-139">Click Lines.</span></span>
25. <span data-ttu-id="f9851-140">[定期処理仕訳帳] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="f9851-140">Click Period journal.</span></span>
26. <span data-ttu-id="f9851-141">[仕訳帳の取得] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="f9851-141">Click Retrieve journal.</span></span>
27. <span data-ttu-id="f9851-142">[終了日] フィールドで、日付を入力します。</span><span class="sxs-lookup"><span data-stu-id="f9851-142">In the To date field, enter a date.</span></span>
    * <span data-ttu-id="f9851-143">[終了日] は、定期伝票明細行の締日として使用されます。</span><span class="sxs-lookup"><span data-stu-id="f9851-143">The To date serves as the cutoff date for the periodic voucher lines.</span></span> <span data-ttu-id="f9851-144">繰り返しの設定に基づいて、[最終日付] および [終了日] は、同じ行が仕訳帳に複数回含められる場合があります。</span><span class="sxs-lookup"><span data-stu-id="f9851-144">Based on the recurrence setting, the Last date and To date the same line might be included more than once in the resulting journal.</span></span> <span data-ttu-id="f9851-145">[終了日] は、定期行が仕訳帳に転送された前回のセッション日付に基づいて自動で更新されます。</span><span class="sxs-lookup"><span data-stu-id="f9851-145">To date is automatically updated based on  session date of the last time the periodic line was transferred to a journal.</span></span>  
28. <span data-ttu-id="f9851-146">[定期処理仕訳帳番号] フィールドで、値を入力または選択します。</span><span class="sxs-lookup"><span data-stu-id="f9851-146">In the Periodic journal number field, enter or select a value.</span></span>
29. <span data-ttu-id="f9851-147">一覧で、選択された行のリンクをクリックします。</span><span class="sxs-lookup"><span data-stu-id="f9851-147">In the list, click the link in the selected row.</span></span>
30. <span data-ttu-id="f9851-148">[OK] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="f9851-148">Click OK.</span></span>
    * <span data-ttu-id="f9851-149">定期処理仕訳帳は条件および設定に応じて、確認、承認、または転記できます。</span><span class="sxs-lookup"><span data-stu-id="f9851-149">The period journal can now be reviewed, approved or posted depending on requirement and setup.</span></span>  


