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
ms.sourcegitcommit: 3ba95d50b8262fa0f43d4faad76adac4d05eb3ea
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 09/27/2019
ms.locfileid: "2178762"
---
# <a name="distribute-questionnaires-using-scheduling"></a><span data-ttu-id="afdbe-103">スケジューリングを使用したアンケートの配布</span><span class="sxs-lookup"><span data-stu-id="afdbe-103">Distribute questionnaires using scheduling</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="afdbe-104">アンケートのスケジューリングによって、複数の回答者に対するアンケートを計画して配布することができます。</span><span class="sxs-lookup"><span data-stu-id="afdbe-104">Questionnaire scheduling allows you to plan and distribute questionnaires to multiple respondents.</span></span> <span data-ttu-id="afdbe-105">この手順の作成に使用するデモ データの会社は USMF です。</span><span class="sxs-lookup"><span data-stu-id="afdbe-105">The demo data company used to create this procedure is USMF.</span></span>


## <a name="create-a-questionnaire-schedule"></a><span data-ttu-id="afdbe-106">アンケートのスケジューリングの作成</span><span class="sxs-lookup"><span data-stu-id="afdbe-106">Create a questionnaire schedule</span></span>
1. <span data-ttu-id="afdbe-107">[アンケート] > [配分] > [アンケートのスケジュール] の順に移動します。</span><span class="sxs-lookup"><span data-stu-id="afdbe-107">Go to Questionnaire > Distribute > Questionnaire schedules.</span></span>
2. <span data-ttu-id="afdbe-108">[新規] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="afdbe-108">Click New.</span></span>
3. <span data-ttu-id="afdbe-109">[スケジューリング] フィールドに値を入力します。</span><span class="sxs-lookup"><span data-stu-id="afdbe-109">In the Scheduling field, type a value.</span></span>
4. <span data-ttu-id="afdbe-110">[説明] フィールドに値を入力します。</span><span class="sxs-lookup"><span data-stu-id="afdbe-110">In the Description field, type a value.</span></span>
    * <span data-ttu-id="afdbe-111">応答に関連付けられた名前を使わずに応答を記録する場合、スケジュールを [匿名] に設定します。</span><span class="sxs-lookup"><span data-stu-id="afdbe-111">Set the schedule to Anonymous if the responses should be recorded without names associated to the response.</span></span>  
    * <span data-ttu-id="afdbe-112">匿名結果を許可するには、最初に HR パラメータで設定する必要があります。</span><span class="sxs-lookup"><span data-stu-id="afdbe-112">Allowing anonymous results must be set up in the HR parameters first.</span></span>  
5. <span data-ttu-id="afdbe-113">[タイプ] フィールドで、計画タイプを選択します。</span><span class="sxs-lookup"><span data-stu-id="afdbe-113">In the Type field, select the planning type.</span></span>  <span data-ttu-id="afdbe-114">この例では、Satisfaction タイプを使用します。</span><span class="sxs-lookup"><span data-stu-id="afdbe-114">In this example we will use the Satisfaction type.</span></span>
6. <span data-ttu-id="afdbe-115">一覧で、目的のレコードを見つけ、選択します。</span><span class="sxs-lookup"><span data-stu-id="afdbe-115">In the list, find and select the desired record.</span></span>
7. <span data-ttu-id="afdbe-116">一覧で、選択された行のリンクをクリックします。</span><span class="sxs-lookup"><span data-stu-id="afdbe-116">In the list, click the link in the selected row.</span></span>
8. <span data-ttu-id="afdbe-117">[日付] フィールドに日付を入力します。</span><span class="sxs-lookup"><span data-stu-id="afdbe-117">In the Date field, enter a date.</span></span>
9. <span data-ttu-id="afdbe-118">従業員セルフサービス セクションの電子メールを展開します。</span><span class="sxs-lookup"><span data-stu-id="afdbe-118">Expand the Email for employee self service section.</span></span>
10. <span data-ttu-id="afdbe-119">[件名] フィールドに値を入力します。</span><span class="sxs-lookup"><span data-stu-id="afdbe-119">In the Subject field, type a value.</span></span>
    * <span data-ttu-id="afdbe-120">例: アンケートの対象</span><span class="sxs-lookup"><span data-stu-id="afdbe-120">Example: Questionnaire available</span></span>  
11. <span data-ttu-id="afdbe-121">[テキスト] フィールドで、電子メールメッセージの本文を入力します。</span><span class="sxs-lookup"><span data-stu-id="afdbe-121">In the Text field, type the body of your email message.</span></span> <span data-ttu-id="afdbe-122">変数は、システム内の値を置換するために使用できることに注意してください。</span><span class="sxs-lookup"><span data-stu-id="afdbe-122">Note, the variable can be used to substitue values in the system.</span></span>
    * <span data-ttu-id="afdbe-123">例:   %P% 様、従業員セルフサービスにログインして、従業員の健康アンケートを完了してください。</span><span class="sxs-lookup"><span data-stu-id="afdbe-123">Example:   Dear %P%,  Please log in to Employee Self Service to complete the Workforce Health questionnaire.</span></span>  <span data-ttu-id="afdbe-124">Contoso</span><span class="sxs-lookup"><span data-stu-id="afdbe-124">Contoso</span></span>  
12. <span data-ttu-id="afdbe-125">[保存] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="afdbe-125">Click Save.</span></span>

## <a name="use-the-setup-details-to-select-the-questionnaires-to-be-answered-as-well-as-any-queries-to-use-to-select-respondents"></a><span data-ttu-id="afdbe-126">[設定の詳細] を使用して、回答対象のアンケートと回答者を選択するために使用するクエリを選択します。</span><span class="sxs-lookup"><span data-stu-id="afdbe-126">Use the Setup details to select the questionnaire(s) to be answered as well as any queries to use to select respondents.</span></span>
1. <span data-ttu-id="afdbe-127">[設定の詳細] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="afdbe-127">Click Setup details.</span></span>
2. <span data-ttu-id="afdbe-128">リストから、アンケートの回答者を検索するのに使用するクエリを選択します。</span><span class="sxs-lookup"><span data-stu-id="afdbe-128">In the list, select a query to use to search the system for respondents for the questionnaire.</span></span>
    * <span data-ttu-id="afdbe-129">例: 作業者</span><span class="sxs-lookup"><span data-stu-id="afdbe-129">Example: Workers</span></span>  
3. <span data-ttu-id="afdbe-130">[表示] をクリックするか、クエリを変更して特定のユーザーを選択するか、クエリを調整して特定の基準に一致する従業員を検索します。</span><span class="sxs-lookup"><span data-stu-id="afdbe-130">Click View or modify query to select specific people or adjust the query to find people who match specific criteria.</span></span>
    * <span data-ttu-id="afdbe-131">すべての回答者が、システム内のユーザーである必要があることに注意してください。</span><span class="sxs-lookup"><span data-stu-id="afdbe-131">Note that all respondents must also be users in the system.</span></span>  
4. <span data-ttu-id="afdbe-132">一覧で、Person の行をマークします。</span><span class="sxs-lookup"><span data-stu-id="afdbe-132">In the list, mark the row for Person</span></span>
5. <span data-ttu-id="afdbe-133">[基準] フィールドで、値を入力または選択します。</span><span class="sxs-lookup"><span data-stu-id="afdbe-133">In the Criteria field, enter or select a value.</span></span>
    * <span data-ttu-id="afdbe-134">Julia Funderburk を選択</span><span class="sxs-lookup"><span data-stu-id="afdbe-134">Select Julia Funderburk</span></span>  
6. <span data-ttu-id="afdbe-135">リストで、Julia Funderburk を選択</span><span class="sxs-lookup"><span data-stu-id="afdbe-135">In the list, select Julia Funderburk</span></span>
7. <span data-ttu-id="afdbe-136">[OK] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="afdbe-136">Click OK.</span></span>
8. <span data-ttu-id="afdbe-137">[アンケート] タブをクリックします。</span><span class="sxs-lookup"><span data-stu-id="afdbe-137">Click the Questionnaires tab.</span></span>
9. <span data-ttu-id="afdbe-138">ツリーで、「アンケート タイプ Satisfaction Survey のノード」を展開します。</span><span class="sxs-lookup"><span data-stu-id="afdbe-138">In the tree, expand 'the node for the questionnaire type Satisfaction Survey'.</span></span>
10. <span data-ttu-id="afdbe-139">ツリーで、「従業員の健康評価」をチェックします。</span><span class="sxs-lookup"><span data-stu-id="afdbe-139">In the tree, check 'Workforce Health Assessment'.</span></span>
11. <span data-ttu-id="afdbe-140">[OK] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="afdbe-140">Click OK.</span></span>
12. <span data-ttu-id="afdbe-141">[計画済回答セッション] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="afdbe-141">Click Planned answer session.</span></span>
    * <span data-ttu-id="afdbe-142">[計画済回答セッション] が、それぞれの選択または質問されたユーザーに対して作成されたことに注意してください。</span><span class="sxs-lookup"><span data-stu-id="afdbe-142">Note that Planned answer sessions have been created for each selected/queried user.</span></span>  
13. <span data-ttu-id="afdbe-143">ページを閉じます。</span><span class="sxs-lookup"><span data-stu-id="afdbe-143">Close the page.</span></span>

## <a name="start-the-questionnaire-schedule-in-order-to-make-the-questionnaire-available-for-respondents-to-complete"></a><span data-ttu-id="afdbe-144">アンケートのスケジュールを開始して、回答者がアンケートを完了できるようにします。</span><span class="sxs-lookup"><span data-stu-id="afdbe-144">Start the questionnaire schedule in order to make the questionnaire available for respondents to complete.</span></span>
1. <span data-ttu-id="afdbe-145">[機能] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="afdbe-145">Click Functions.</span></span>
2. <span data-ttu-id="afdbe-146">[開始] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="afdbe-146">Click Start.</span></span>
3. <span data-ttu-id="afdbe-147">[OK] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="afdbe-147">Click OK.</span></span>

## <a name="send-the-email-to-inform-respondents-of-the-available-questionnaire"></a><span data-ttu-id="afdbe-148">使用できるアンケートを回答者に通知する電子メールを送信します。</span><span class="sxs-lookup"><span data-stu-id="afdbe-148">Send the email to inform respondents of the available questionnaire.</span></span>
1. <span data-ttu-id="afdbe-149">[機能] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="afdbe-149">Click Functions.</span></span>
2. <span data-ttu-id="afdbe-150">[電子メールの送信] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="afdbe-150">Click Send email.</span></span>
3. <span data-ttu-id="afdbe-151">[キャンセル] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="afdbe-151">Click Cancel.</span></span>

## <a name="use-planned-answer-sessions-to-monitor-who-needs-to-complete-the-questionnaire"></a><span data-ttu-id="afdbe-152">[計画済回答セッション] を使用して、アンケートを完了する必要がある人を監視します。</span><span class="sxs-lookup"><span data-stu-id="afdbe-152">Use Planned answer sessions to monitor who needs to complete the questionnaire.</span></span>
1. <span data-ttu-id="afdbe-153">[計画済回答セッション] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="afdbe-153">Click Planned answer session.</span></span>
    * <span data-ttu-id="afdbe-154">予定セッションを終了する準備ができたら、残りの計画済回答セッションを削除します。</span><span class="sxs-lookup"><span data-stu-id="afdbe-154">Delete any remaining planned answer session when you're ready to end the scheduled session.</span></span>  
2. <span data-ttu-id="afdbe-155">[削除] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="afdbe-155">Click Delete.</span></span>
3. <span data-ttu-id="afdbe-156">[はい] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="afdbe-156">Click Yes.</span></span>
4. <span data-ttu-id="afdbe-157">ページを閉じます。</span><span class="sxs-lookup"><span data-stu-id="afdbe-157">Close the page.</span></span>

## <a name="end-the-schedule-when-all-respondents-have-completed-the-questionnaire-andor-all-remaining-planned-answer-sessions-have-been-deleted"></a><span data-ttu-id="afdbe-158">すべての回答者がアンケートを完了し、および/または残りのすべての計画済回答セッションが削除されたときに、スケジュールを終了します。</span><span class="sxs-lookup"><span data-stu-id="afdbe-158">End the schedule when all respondents have completed the questionnaire and/or all remaining Planned answer sessions have been deleted.</span></span>
1. <span data-ttu-id="afdbe-159">[機能] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="afdbe-159">Click Functions.</span></span>
2. <span data-ttu-id="afdbe-160">[終了] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="afdbe-160">Click End.</span></span>
3. <span data-ttu-id="afdbe-161">[OK] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="afdbe-161">Click OK.</span></span>
