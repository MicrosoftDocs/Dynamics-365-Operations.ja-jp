---
title: スケジューリングを使用したアンケートの配布
description: アンケートのスケジューリングによって、複数の回答者に対するアンケートを計画して配布することができます。
author: andreabichsel
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: KMKnowledgeCollectorPlanningTable, KMKnowledgeCollectorPlanningMulti, SysQueryForm, HcmPersonLookup, KMKnowledgeCollectorPlanning
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: anbichse
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: a6887deb01ade2c5b8cef88294eace65e9300eb9
ms.sourcegitcommit: 2b890cd7a801055ab0ca24398efc8e4e777d4d8c
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 05/07/2019
ms.locfileid: "1510546"
---
# <a name="distribute-questionnaires-using-scheduling"></a><span data-ttu-id="fd4a4-103">スケジューリングを使用したアンケートの配布</span><span class="sxs-lookup"><span data-stu-id="fd4a4-103">Distribute questionnaires using scheduling</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="fd4a4-104">アンケートのスケジューリングによって、複数の回答者に対するアンケートを計画して配布することができます。</span><span class="sxs-lookup"><span data-stu-id="fd4a4-104">Questionnaire scheduling allows you to plan and distribute questionnaires to multiple respondents.</span></span> <span data-ttu-id="fd4a4-105">この手順の作成に使用するデモ データの会社は USMF です。</span><span class="sxs-lookup"><span data-stu-id="fd4a4-105">The demo data company used to create this procedure is USMF.</span></span>


## <a name="create-a-questionnaire-schedule"></a><span data-ttu-id="fd4a4-106">アンケートのスケジューリングの作成</span><span class="sxs-lookup"><span data-stu-id="fd4a4-106">Create a questionnaire schedule</span></span>
1. <span data-ttu-id="fd4a4-107">[アンケート] > [配分] > [アンケートのスケジュール] の順に移動します。</span><span class="sxs-lookup"><span data-stu-id="fd4a4-107">Go to Questionnaire > Distribute > Questionnaire schedules.</span></span>
2. <span data-ttu-id="fd4a4-108">[新規] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="fd4a4-108">Click New.</span></span>
3. <span data-ttu-id="fd4a4-109">[スケジューリング] フィールドに値を入力します。</span><span class="sxs-lookup"><span data-stu-id="fd4a4-109">In the Scheduling field, type a value.</span></span>
4. <span data-ttu-id="fd4a4-110">[説明] フィールドに値を入力します。</span><span class="sxs-lookup"><span data-stu-id="fd4a4-110">In the Description field, type a value.</span></span>
    * <span data-ttu-id="fd4a4-111">応答に関連付けられた名前を使わずに応答を記録する場合、スケジュールを [匿名] に設定します。</span><span class="sxs-lookup"><span data-stu-id="fd4a4-111">Set the schedule to Anonymous if the responses should be recorded without names associated to the response.</span></span>  
    * <span data-ttu-id="fd4a4-112">匿名結果を許可するには、最初に HR パラメータで設定する必要があります。</span><span class="sxs-lookup"><span data-stu-id="fd4a4-112">Allowing anonymous results must be set up in the HR parameters first.</span></span>  
5. <span data-ttu-id="fd4a4-113">[タイプ] フィールドで、計画タイプを選択します。</span><span class="sxs-lookup"><span data-stu-id="fd4a4-113">In the Type field, select the planning type.</span></span>  <span data-ttu-id="fd4a4-114">この例では、Satisfaction タイプを使用します。</span><span class="sxs-lookup"><span data-stu-id="fd4a4-114">In this example we will use the Satisfaction type.</span></span>
6. <span data-ttu-id="fd4a4-115">一覧で、目的のレコードを見つけ、選択します。</span><span class="sxs-lookup"><span data-stu-id="fd4a4-115">In the list, find and select the desired record.</span></span>
7. <span data-ttu-id="fd4a4-116">一覧で、選択された行のリンクをクリックします。</span><span class="sxs-lookup"><span data-stu-id="fd4a4-116">In the list, click the link in the selected row.</span></span>
8. <span data-ttu-id="fd4a4-117">[日付] フィールドに日付を入力します。</span><span class="sxs-lookup"><span data-stu-id="fd4a4-117">In the Date field, enter a date.</span></span>
9. <span data-ttu-id="fd4a4-118">従業員セルフサービス セクションの電子メールを展開します。</span><span class="sxs-lookup"><span data-stu-id="fd4a4-118">Expand the Email for employee self service section.</span></span>
10. <span data-ttu-id="fd4a4-119">[件名] フィールドに値を入力します。</span><span class="sxs-lookup"><span data-stu-id="fd4a4-119">In the Subject field, type a value.</span></span>
    * <span data-ttu-id="fd4a4-120">例: アンケートの対象</span><span class="sxs-lookup"><span data-stu-id="fd4a4-120">Example: Questionnaire available</span></span>  
11. <span data-ttu-id="fd4a4-121">[テキスト] フィールドで、電子メールメッセージの本文を入力します。</span><span class="sxs-lookup"><span data-stu-id="fd4a4-121">In the Text field, type the body of your email message.</span></span> <span data-ttu-id="fd4a4-122">変数は、システム内の値を置換するために使用できることに注意してください。</span><span class="sxs-lookup"><span data-stu-id="fd4a4-122">Note, the variable can be used to substitue values in the system.</span></span>
    * <span data-ttu-id="fd4a4-123">例:   %P% 様、従業員セルフサービスにログインして、従業員の健康アンケートを完了してください。</span><span class="sxs-lookup"><span data-stu-id="fd4a4-123">Example:   Dear %P%,  Please log in to Employee Self Service to complete the Workforce Health questionnaire.</span></span>  <span data-ttu-id="fd4a4-124">Contoso</span><span class="sxs-lookup"><span data-stu-id="fd4a4-124">Contoso</span></span>  
12. <span data-ttu-id="fd4a4-125">[保存] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="fd4a4-125">Click Save.</span></span>

## <a name="use-the-setup-details-to-select-the-questionnaires-to-be-answered-as-well-as-any-queries-to-use-to-select-respondents"></a><span data-ttu-id="fd4a4-126">[設定の詳細] を使用して、回答対象のアンケートと回答者を選択するために使用するクエリを選択します。</span><span class="sxs-lookup"><span data-stu-id="fd4a4-126">Use the Setup details to select the questionnaire(s) to be answered as well as any queries to use to select respondents.</span></span>
1. <span data-ttu-id="fd4a4-127">[設定の詳細] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="fd4a4-127">Click Setup details.</span></span>
2. <span data-ttu-id="fd4a4-128">リストから、アンケートの回答者を検索するのに使用するクエリを選択します。</span><span class="sxs-lookup"><span data-stu-id="fd4a4-128">In the list, select a query to use to search the system for respondents for the questionnaire.</span></span>
    * <span data-ttu-id="fd4a4-129">例: 作業者</span><span class="sxs-lookup"><span data-stu-id="fd4a4-129">Example: Workers</span></span>  
3. <span data-ttu-id="fd4a4-130">[表示] をクリックするか、クエリを変更して特定のユーザーを選択するか、クエリを調整して特定の基準に一致する従業員を検索します。</span><span class="sxs-lookup"><span data-stu-id="fd4a4-130">Click View or modify query to select specific people or adjust the query to find people who match specific criteria.</span></span>
    * <span data-ttu-id="fd4a4-131">すべての回答者が、システム内のユーザーである必要があることに注意してください。</span><span class="sxs-lookup"><span data-stu-id="fd4a4-131">Note that all respondents must also be users in the system.</span></span>  
4. <span data-ttu-id="fd4a4-132">一覧で、Person の行をマークします。</span><span class="sxs-lookup"><span data-stu-id="fd4a4-132">In the list, mark the row for Person</span></span>
5. <span data-ttu-id="fd4a4-133">[基準] フィールドで、値を入力または選択します。</span><span class="sxs-lookup"><span data-stu-id="fd4a4-133">In the Criteria field, enter or select a value.</span></span>
    * <span data-ttu-id="fd4a4-134">Julia Funderburk を選択</span><span class="sxs-lookup"><span data-stu-id="fd4a4-134">Select Julia Funderburk</span></span>  
6. <span data-ttu-id="fd4a4-135">リストで、Julia Funderburk を選択</span><span class="sxs-lookup"><span data-stu-id="fd4a4-135">In the list, select Julia Funderburk</span></span>
7. <span data-ttu-id="fd4a4-136">[OK] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="fd4a4-136">Click OK.</span></span>
8. <span data-ttu-id="fd4a4-137">[アンケート] タブをクリックします。</span><span class="sxs-lookup"><span data-stu-id="fd4a4-137">Click the Questionnaires tab.</span></span>
9. <span data-ttu-id="fd4a4-138">ツリーで、「アンケート タイプ Satisfaction Survey のノード」を展開します。</span><span class="sxs-lookup"><span data-stu-id="fd4a4-138">In the tree, expand 'the node for the questionnaire type Satisfaction Survey'.</span></span>
10. <span data-ttu-id="fd4a4-139">ツリーで、「従業員の健康評価」をチェックします。</span><span class="sxs-lookup"><span data-stu-id="fd4a4-139">In the tree, check 'Workforce Health Assessment'.</span></span>
11. <span data-ttu-id="fd4a4-140">[OK] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="fd4a4-140">Click OK.</span></span>
12. <span data-ttu-id="fd4a4-141">[計画済回答セッション] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="fd4a4-141">Click Planned answer session.</span></span>
    * <span data-ttu-id="fd4a4-142">[計画済回答セッション] が、それぞれの選択または質問されたユーザーに対して作成されたことに注意してください。</span><span class="sxs-lookup"><span data-stu-id="fd4a4-142">Note that Planned answer sessions have been created for each selected/queried user.</span></span>  
13. <span data-ttu-id="fd4a4-143">ページを閉じます。</span><span class="sxs-lookup"><span data-stu-id="fd4a4-143">Close the page.</span></span>

## <a name="start-the-questionnaire-schedule-in-order-to-make-the-questionnaire-available-for-respondents-to-complete"></a><span data-ttu-id="fd4a4-144">アンケートのスケジュールを開始して、回答者がアンケートを完了できるようにします。</span><span class="sxs-lookup"><span data-stu-id="fd4a4-144">Start the questionnaire schedule in order to make the questionnaire available for respondents to complete.</span></span>
1. <span data-ttu-id="fd4a4-145">[機能] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="fd4a4-145">Click Functions.</span></span>
2. <span data-ttu-id="fd4a4-146">[開始] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="fd4a4-146">Click Start.</span></span>
3. <span data-ttu-id="fd4a4-147">[OK] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="fd4a4-147">Click OK.</span></span>

## <a name="send-the-email-to-inform-respondents-of-the-available-questionnaire"></a><span data-ttu-id="fd4a4-148">使用できるアンケートを回答者に通知する電子メールを送信します。</span><span class="sxs-lookup"><span data-stu-id="fd4a4-148">Send the email to inform respondents of the available questionnaire.</span></span>
1. <span data-ttu-id="fd4a4-149">[機能] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="fd4a4-149">Click Functions.</span></span>
2. <span data-ttu-id="fd4a4-150">[電子メールの送信] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="fd4a4-150">Click Send email.</span></span>
3. <span data-ttu-id="fd4a4-151">[キャンセル] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="fd4a4-151">Click Cancel.</span></span>

## <a name="use-planned-answer-sessions-to-monitor-who-needs-to-complete-the-questionnaire"></a><span data-ttu-id="fd4a4-152">[計画済回答セッション] を使用して、アンケートを完了する必要がある人を監視します。</span><span class="sxs-lookup"><span data-stu-id="fd4a4-152">Use Planned answer sessions to monitor who needs to complete the questionnaire.</span></span>
1. <span data-ttu-id="fd4a4-153">[計画済回答セッション] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="fd4a4-153">Click Planned answer session.</span></span>
    * <span data-ttu-id="fd4a4-154">予定セッションを終了する準備ができたら、残りの計画済回答セッションを削除します。</span><span class="sxs-lookup"><span data-stu-id="fd4a4-154">Delete any remaining planned answer session when you're ready to end the scheduled session.</span></span>  
2. <span data-ttu-id="fd4a4-155">[削除] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="fd4a4-155">Click Delete.</span></span>
3. <span data-ttu-id="fd4a4-156">[はい] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="fd4a4-156">Click Yes.</span></span>
4. <span data-ttu-id="fd4a4-157">ページを閉じます。</span><span class="sxs-lookup"><span data-stu-id="fd4a4-157">Close the page.</span></span>

## <a name="end-the-schedule-when-all-respondents-have-completed-the-questionnaire-andor-all-remaining-planned-answer-sessions-have-been-deleted"></a><span data-ttu-id="fd4a4-158">すべての回答者がアンケートを完了し、および/または残りのすべての計画済回答セッションが削除されたときに、スケジュールを終了します。</span><span class="sxs-lookup"><span data-stu-id="fd4a4-158">End the schedule when all respondents have completed the questionnaire and/or all remaining Planned answer sessions have been deleted.</span></span>
1. <span data-ttu-id="fd4a4-159">[機能] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="fd4a4-159">Click Functions.</span></span>
2. <span data-ttu-id="fd4a4-160">[終了] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="fd4a4-160">Click End.</span></span>
3. <span data-ttu-id="fd4a4-161">[OK] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="fd4a4-161">Click OK.</span></span>

