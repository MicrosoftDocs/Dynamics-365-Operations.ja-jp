---
title: 定期処理仕訳帳の転記
description: 定期処理仕訳帳は、繰返しの仕訳帳とも呼ばれ、定期処理仕訳帳を取得するたびに数量、テキスト、およびその他の情報が繰り返されます。
author: aprilolson
manager: AnnBe
ms.date: 06/26/2019
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: LedgerJournalTable, LedgerJournalTransPeriodic, LedgerJournalTransDaily
audience: Application User
ms.reviewer: roschlom
ms.search.region: Global
ms.author: aolson
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 99d157e82f8451e2c8f0bc7946ba30ca48e99add
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 01/15/2021
ms.locfileid: "4968507"
---
# <a name="post-periodic-journals"></a><span data-ttu-id="dd4e6-103">定期処理仕訳帳の転記</span><span class="sxs-lookup"><span data-stu-id="dd4e6-103">Post periodic journals</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="dd4e6-104">定期処理仕訳帳は、繰返しの仕訳帳とも呼ばれ、定期処理仕訳帳を取得するたびに数量、テキスト、およびその他の情報が繰り返されます。</span><span class="sxs-lookup"><span data-stu-id="dd4e6-104">Periodic journals are sometimes called recurring journals because the amount, text, and other information are repeated each time that the periodic journal is retrieved.</span></span> <span data-ttu-id="dd4e6-105">定期処理仕訳帳を作成する場合、日数または月数などの繰り返し間隔を指定します。</span><span class="sxs-lookup"><span data-stu-id="dd4e6-105">When you create the periodic journal, you specify the period interval for the recurrence, such as days or months.</span></span> <span data-ttu-id="dd4e6-106">このタスク ガイドでは、月間の繰り返しを持つ定期処理仕訳帳を作成します。</span><span class="sxs-lookup"><span data-stu-id="dd4e6-106">This task guide will create a periodic journal with a monthly recurrence.</span></span>

1. <span data-ttu-id="dd4e6-107">**ナビゲーション ウィンドウ > モジュール > 一般会計 > 定期処理タスク > 定期処理仕訳帳** の順に移動します。</span><span class="sxs-lookup"><span data-stu-id="dd4e6-107">Go to **Navigation pane > Modules > General ledger > Periodic tasks > Periodic journals**.</span></span>
2. <span data-ttu-id="dd4e6-108">**新規** をクリックします。</span><span class="sxs-lookup"><span data-stu-id="dd4e6-108">Click **New**.</span></span>
3. <span data-ttu-id="dd4e6-109">**名前** フィールドで値を入力または選択します。</span><span class="sxs-lookup"><span data-stu-id="dd4e6-109">In the **Name** field, enter or select a value.</span></span>
4. <span data-ttu-id="dd4e6-110">一覧で、選択された行のリンクをクリックします。</span><span class="sxs-lookup"><span data-stu-id="dd4e6-110">In the list, click the link in the selected row.</span></span>
5. <span data-ttu-id="dd4e6-111">**説明** フィールドで、値を入力します。</span><span class="sxs-lookup"><span data-stu-id="dd4e6-111">In the **Description** field, type a value.</span></span> <span data-ttu-id="dd4e6-112">説明は、後から取得する場合は定期処理仕訳帳の名前になるため、適切な名前を付けることをお勧めします。</span><span class="sxs-lookup"><span data-stu-id="dd4e6-112">The description will be the name of the Periodic journal when retrieved later so make sure to give it a relevant name.</span></span>
6. <span data-ttu-id="dd4e6-113">**アクション ウィンドウ** で、**明細行** をクリックします。</span><span class="sxs-lookup"><span data-stu-id="dd4e6-113">On the **Action pane**, click **Lines**.</span></span> <span data-ttu-id="dd4e6-114">定期処理仕訳帳には通常、複数の仕訳帳明細行が含まれます。</span><span class="sxs-lookup"><span data-stu-id="dd4e6-114">A periodic journal will typically include several journal lines.</span></span> <span data-ttu-id="dd4e6-115">ただし、このタスク ガイドでは 1 行のみ追加します。</span><span class="sxs-lookup"><span data-stu-id="dd4e6-115">this task guide will however only add one line.</span></span>
7. <span data-ttu-id="dd4e6-116">**日付** フィールドに日付を入力します。</span><span class="sxs-lookup"><span data-stu-id="dd4e6-116">In the **Date** field, enter a date.</span></span> <span data-ttu-id="dd4e6-117">**日付** フィールドには、次に日次仕訳帳への転送が行われる転記日付が含まれます。</span><span class="sxs-lookup"><span data-stu-id="dd4e6-117">The **Date** field contains the posting date for the next transfer to the daily journal.</span></span> <span data-ttu-id="dd4e6-118">毎月取得する仕訳帳については、転記を行う月内の日付を使用することをお勧めします。通常これは期間の最初または最後の日付です。</span><span class="sxs-lookup"><span data-stu-id="dd4e6-118">For journals that will be retrieved each month it is recommended to use the date in the month when it will be posted, typically the first or last date in the period.</span></span> <span data-ttu-id="dd4e6-119">[空の日付] フィールドを使用すると、[日付] フィールドを空のままにして、仕訳帳の取得時に日付を指定することができます。</span><span class="sxs-lookup"><span data-stu-id="dd4e6-119">It is possible to leave the Date field blank and to give a date when the journal is retrieved, using the Empty date field.</span></span> <span data-ttu-id="dd4e6-120">このフィールドは、トランザクションが取得される次の繰り返し日に自動的に更新されます。</span><span class="sxs-lookup"><span data-stu-id="dd4e6-120">The field is automatically updated to the next recurring date when transactions are retrieved.</span></span> 
8. <span data-ttu-id="dd4e6-121">**勘定** フィールドで、目的の値を指定します。</span><span class="sxs-lookup"><span data-stu-id="dd4e6-121">In the **Account** field, specify the desired values.</span></span>
9. <span data-ttu-id="dd4e6-122">**説明** フィールドで値を選択します。</span><span class="sxs-lookup"><span data-stu-id="dd4e6-122">In the **Description** field, select a value.</span></span>
10. <span data-ttu-id="dd4e6-123">ページを閉じます。</span><span class="sxs-lookup"><span data-stu-id="dd4e6-123">Close the page.</span></span>
11. <span data-ttu-id="dd4e6-124">**借方** フィールドに数値を入力します。</span><span class="sxs-lookup"><span data-stu-id="dd4e6-124">In the **Debit** field, enter a number.</span></span>
12. <span data-ttu-id="dd4e6-125">**相殺勘定** フィールドで、任意の値を指定します。</span><span class="sxs-lookup"><span data-stu-id="dd4e6-125">In the **Offset account** field, specify the desired values.</span></span>
13. <span data-ttu-id="dd4e6-126">**単位** フィールドで、月を選択します。</span><span class="sxs-lookup"><span data-stu-id="dd4e6-126">In the **Unit** field, select 'Months'.</span></span>
14. <span data-ttu-id="dd4e6-127">**単位数** フィールドに「1」を入力します。</span><span class="sxs-lookup"><span data-stu-id="dd4e6-127">In the **Number of units** field, enter '1'.</span></span>
15. <span data-ttu-id="dd4e6-128">**最終日付** フィールドに日付を入力します。</span><span class="sxs-lookup"><span data-stu-id="dd4e6-128">In the **Last date** field, enter a date.</span></span> <span data-ttu-id="dd4e6-129">前の期間内の最後の日付を入力すると、定期的な仕訳帳が誤った開始期間で作成されるのを防ぎます。</span><span class="sxs-lookup"><span data-stu-id="dd4e6-129">Entering last date in the preceding period will prevent that the recurring journal by mistake is created in the wrong starting period.</span></span> <span data-ttu-id="dd4e6-130">終了日は、後で定期処理仕訳帳が取得されるたびに更新されます。</span><span class="sxs-lookup"><span data-stu-id="dd4e6-130">Last date will later on be updated each time the periodic journal is retrieved.</span></span> 
16. <span data-ttu-id="dd4e6-131">**保存** をクリックします。</span><span class="sxs-lookup"><span data-stu-id="dd4e6-131">Click **Save**.</span></span>
17. <span data-ttu-id="dd4e6-132">**ナビゲーション ウィンドウ > モジュール > 総勘定元帳 > 仕訳入力 > 一般仕訳帳** の順に移動します。</span><span class="sxs-lookup"><span data-stu-id="dd4e6-132">Go to **Navigation pane > Modules > General ledger > Journal entries > General journals**.</span></span>
18. <span data-ttu-id="dd4e6-133">**新規** をクリックします。</span><span class="sxs-lookup"><span data-stu-id="dd4e6-133">Click **New**.</span></span>
19. <span data-ttu-id="dd4e6-134">**名前** フィールドで値を入力または選択します。</span><span class="sxs-lookup"><span data-stu-id="dd4e6-134">In the **Name** field, enter or select a value.</span></span>
20. <span data-ttu-id="dd4e6-135">一覧で、目的のレコードを見つけ、選択します。</span><span class="sxs-lookup"><span data-stu-id="dd4e6-135">In the list, find and select the desired record.</span></span>
21. <span data-ttu-id="dd4e6-136">一覧で、選択された行のリンクをクリックします。</span><span class="sxs-lookup"><span data-stu-id="dd4e6-136">In the list, click the link in the selected row.</span></span>
22. <span data-ttu-id="dd4e6-137">**説明** フィールドで、値を入力します。</span><span class="sxs-lookup"><span data-stu-id="dd4e6-137">In the **Description** field, type a value.</span></span>
23. <span data-ttu-id="dd4e6-138">**アクション ウィンドウ** で、**明細行** をクリックします。</span><span class="sxs-lookup"><span data-stu-id="dd4e6-138">On the **Action pane**, click **Lines**.</span></span>
24. <span data-ttu-id="dd4e6-139">**アクション ウィンドウ** で、**定期処理仕訳帳** をクリックします。</span><span class="sxs-lookup"><span data-stu-id="dd4e6-139">On the **Action pane**, click **Period journal**.</span></span>
25. <span data-ttu-id="dd4e6-140">**仕訳帳の取得** クリックします。</span><span class="sxs-lookup"><span data-stu-id="dd4e6-140">Click **Retrieve journal**.</span></span>
26. <span data-ttu-id="dd4e6-141">**終了日** フィールドに、日付を入力します。</span><span class="sxs-lookup"><span data-stu-id="dd4e6-141">In the **To date** field, enter a date.</span></span> <span data-ttu-id="dd4e6-142">**終了日** は、定期伝票明細行の締日として使用されます。</span><span class="sxs-lookup"><span data-stu-id="dd4e6-142">The **To date** serves as the cutoff date for the periodic voucher lines.</span></span> <span data-ttu-id="dd4e6-143">繰り返しの設定に基づいて、[最終日付] および [終了日] は、同じ行が仕訳帳に複数回含められる場合があります。</span><span class="sxs-lookup"><span data-stu-id="dd4e6-143">Based on the recurrence setting, the Last date and To date the same line might be included more than once in the resulting journal.</span></span> <span data-ttu-id="dd4e6-144">[終了日] は、定期行が仕訳帳に転送された前回のセッション日付に基づいて自動で更新されます。</span><span class="sxs-lookup"><span data-stu-id="dd4e6-144">To date is automatically updated based on  session date of the last time the periodic line was transferred to a journal.</span></span> 
27. <span data-ttu-id="dd4e6-145">**定期処理仕訳帳番号** フィールドで、値を入力または選択します。</span><span class="sxs-lookup"><span data-stu-id="dd4e6-145">In the **Periodic journal number** field, enter or select a value.</span></span>
28. <span data-ttu-id="dd4e6-146">一覧で、選択された行のリンクをクリックします。</span><span class="sxs-lookup"><span data-stu-id="dd4e6-146">In the list, click the link in the selected row.</span></span>
29. <span data-ttu-id="dd4e6-147">**OK** をクリックします。</span><span class="sxs-lookup"><span data-stu-id="dd4e6-147">Click **OK**.</span></span> <span data-ttu-id="dd4e6-148">定期処理仕訳帳は条件および設定に応じて、確認、承認、または転記できます。</span><span class="sxs-lookup"><span data-stu-id="dd4e6-148">The period journal can now be reviewed, approved or posted depending on requirement and setup.</span></span>   
