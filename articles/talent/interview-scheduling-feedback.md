---
title: 面接のスケジューリングおよびフィードバック
description: このトピックでは、Attract での面接のスケジューリングとフィードバック活動に関する情報を提供します。
author: ''
manager: AnnBe
ms.date: 02/01/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-talent
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: josaw
ms.search.scope: Talent, Core
ms.search.region: Global
ms.author: hasrivas
ms.openlocfilehash: 7bc5a66bb221cb0ab2c69fcb1013ed48a7c664a6
ms.sourcegitcommit: 1e32d78868098fd76124bb41363f15c4ec3ea15a
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 02/05/2019
ms.locfileid: "374933"
---
# <a name="interview-scheduling-and-feedback"></a><span data-ttu-id="1f674-103">面接のスケジューリングおよびフィードバック</span><span class="sxs-lookup"><span data-stu-id="1f674-103">Interview scheduling and feedback</span></span>

[!include[banner](../includes/banner.md)]

## <a name="scheduler-activity"></a><span data-ttu-id="1f674-104">スケジューラの活動</span><span class="sxs-lookup"><span data-stu-id="1f674-104">Scheduler activity</span></span>

<span data-ttu-id="1f674-105">スケジューラ活動はオプションであり、2 つのコンポーネントがあります: 候補者の面接可能日の要求およびスケジュールです。</span><span class="sxs-lookup"><span data-stu-id="1f674-105">The scheduler activity is optional and has two components: Candidate availability request and Schedule.</span></span> <span data-ttu-id="1f674-106">候補者の面接可能日コンポーネントにより、電子メールを使用して、候補者の面接可能日を要求することができます。</span><span class="sxs-lookup"><span data-stu-id="1f674-106">The Candidate availability component lets you use email to request a candidate's availability.</span></span> <span data-ttu-id="1f674-107">スケジュール コンポーネントでは、候補者と採用チームとの面接をスケジュールする機能を提供します。</span><span class="sxs-lookup"><span data-stu-id="1f674-107">The Schedule component provides the ability to schedule interviews with the candidate and the hiring team.</span></span>

### <a name="candidate-availability-request"></a><span data-ttu-id="1f674-108">候補者の面接可能日の要求</span><span class="sxs-lookup"><span data-stu-id="1f674-108">Candidate availability request</span></span>

<span data-ttu-id="1f674-109">候補者に面接可能日を要求する電子メールを送信するには、**候補者の面接可能日を要求**オプションをオンに設定します。</span><span class="sxs-lookup"><span data-stu-id="1f674-109">To send an email to candidates requesting their availability, select the **Request candidate availability** field.</span></span> <span data-ttu-id="1f674-110">フィールドが選択されていない場合、このステップはジョブの採用プロセスには表示されません。</span><span class="sxs-lookup"><span data-stu-id="1f674-110">If the field is not selected, this step won't be shown in the hiring process for the job.</span></span>

<span data-ttu-id="1f674-111">面接可能日の要求を送信するには、**要求の送信**をクリックして、利用可能な日付と電子メール テンプレートを選択し、メールを候補者に送信します。</span><span class="sxs-lookup"><span data-stu-id="1f674-111">To send the availability request, click **Send request**, choose the available dates and an email template, and then send the mail to the candidate.</span></span>

<span data-ttu-id="1f674-112">[![候補者の面接可能日の要求を送信する Attract 採用担当者ビュー](./media/scheduler-candidate-request.png)](./media/scheduler-candidate-request.png)</span><span class="sxs-lookup"><span data-stu-id="1f674-112">[![Attract recruiter view to send candidate availability request](./media/scheduler-candidate-request.png)](./media/scheduler-candidate-request.png)</span></span>

<span data-ttu-id="1f674-113">候補者は、要求に応答するための電子メールを受信すると、その候補者のポータルにサインインし、自分の都合に合う日付を選択し、**送信**をクリックします。</span><span class="sxs-lookup"><span data-stu-id="1f674-113">When the candidate receives an email to respond to the request, they can sign in to their candidate portal, choose the dates that match their availability, and click **Submit**.</span></span>

### <a name="schedule"></a><span data-ttu-id="1f674-114">スケジュール</span><span class="sxs-lookup"><span data-stu-id="1f674-114">Schedule</span></span>
<span data-ttu-id="1f674-115">面接スケジューラが面接ループを使用し、すばやく作成して面接者と候補者に送信するために使用できるコンフィギュレーションは複数あります。</span><span class="sxs-lookup"><span data-stu-id="1f674-115">There are multiple configurations available for the interview scheduler to use and quickly create and send the interview loop to the interviewers and the candidate.</span></span>

1. <span data-ttu-id="1f674-116">**スケジュールの作成**をクリックし、**面接を追加**ボックスで、面接ループの一部になる予定のすべての面接を一覧表示します。</span><span class="sxs-lookup"><span data-stu-id="1f674-116">Click **Create schedule**, and in the **Add interviewers** box, list all the interviewers that are going to be part of the interview loop.</span></span>
<span data-ttu-id="1f674-117">[![スケジューリングと面接ループを開始する Attract 採用担当者ビュー](./media/schedule-start-over.png)](./media/schedule-start-over.png) </span><span class="sxs-lookup"><span data-stu-id="1f674-117">[![Attract recruiter view to start scheduling an interview loop](./media/schedule-start-over.png)](./media/schedule-start-over.png) </span></span>  
    <span data-ttu-id="1f674-118">候補者が面接可能日の要求に応答した場合、**面接日**フィールドには、候補者の選択した内容があらかじめ設定されています。</span><span class="sxs-lookup"><span data-stu-id="1f674-118">If the candidate had responded to the interview request availability, the **Interview date** field will be pre-populated with their selection.</span></span> <span data-ttu-id="1f674-119">必要に応じて別の日付を選択できます。</span><span class="sxs-lookup"><span data-stu-id="1f674-119">You can select a different date if needed.</span></span>
    
    <span data-ttu-id="1f674-120">**これをパネル面接にする**フィールドを選択すると、左側の面接者のグループが単一のパネル ループに移動して面接を作成します。</span><span class="sxs-lookup"><span data-stu-id="1f674-120">If you select the **Make this a panel interview** field, the group of interviewers on the left are moved in to a single panel loop to create the interview.</span></span> <span data-ttu-id="1f674-121">その後、面接の特定の順序を定義する必要があります。</span><span class="sxs-lookup"><span data-stu-id="1f674-121">You will then need to define a specific sequence for the interviews.</span></span>
    
    <span data-ttu-id="1f674-122">面接のスケジュールは、参加者の都合に最も合うように調整する必要があります。</span><span class="sxs-lookup"><span data-stu-id="1f674-122">The interview schedule should be arranged to best match the participants’ availability.</span></span> <span data-ttu-id="1f674-123">内部候補者である場合は、スケジュールの推奨事項の一部としてそれらの都合を含めることができます。</span><span class="sxs-lookup"><span data-stu-id="1f674-123">If it’s an internal candidate, you can include their availability as part of the schedule recommendation.</span></span>
    
    <span data-ttu-id="1f674-124">オンライン会議を開くには、**Skype 会議の追加**フィールドを選択すると、各面接イベントに **Skype for Business** のリンクが表示されます。</span><span class="sxs-lookup"><span data-stu-id="1f674-124">To have an online meeting, select the **Add Skype meetings** field and each interview event will have a **Skype for Business** link available.</span></span>

2. <span data-ttu-id="1f674-125">各面接イベントに対する面接の期間を選択し、**OK** をクリックしてスケジュールの作成を開始します。</span><span class="sxs-lookup"><span data-stu-id="1f674-125">Select the interview duration for each interview event, and then click **OK** to start creating the schedule.</span></span>

    <span data-ttu-id="1f674-126">**推奨事項**を選択すると、提案が表示され、面接グリッドは自動的に入力されます。</span><span class="sxs-lookup"><span data-stu-id="1f674-126">If **Recommendations** are selected, suggestions will be shown and the interview grid will be pre-populated.</span></span> <span data-ttu-id="1f674-127">すべての選択された面接者の現在のカレンダーの面接可能日を見ることができます。</span><span class="sxs-lookup"><span data-stu-id="1f674-127">You will be able to see the current calendar availability of all the s elected interviewers.</span></span> <span data-ttu-id="1f674-128">内部候補者の場合は、候補者のカレンダーを表示することもできます。</span><span class="sxs-lookup"><span data-stu-id="1f674-128">You will also be able to view the candidate’s calendar if they're an internal candidate.</span></span>

3. <span data-ttu-id="1f674-129">利用可能な提案がない場合は、**面接**列で、タイム スロット内でクリックして、面接のタイトル、詳細、および必要に応じて場所の詳細を入力します。</span><span class="sxs-lookup"><span data-stu-id="1f674-129">If there are no suggestions available, in the **Interviewers** column, click in a time slot, provide the interview title, details, and populate the location details, as necessary.</span></span> <span data-ttu-id="1f674-130">面接に **Skype for Business** リンクを含めることを選択できます。</span><span class="sxs-lookup"><span data-stu-id="1f674-130">You can choose to include the **Skype for Business** link for the interview.</span></span>

4. <span data-ttu-id="1f674-131">追加の面接を含めるには、**面接の追加**グリッドの列をクリックして、1 つまたは複数の面接を選択します。</span><span class="sxs-lookup"><span data-stu-id="1f674-131">To include additional interviewers, click the **Add interview** grid column to select one or more interviewers.</span></span> <span data-ttu-id="1f674-132">ループから面接を削除するには、省略記号 (...) オプションを使用することができます。</span><span class="sxs-lookup"><span data-stu-id="1f674-132">You can use the ellipsis (...) option to remove an interview from the loop.</span></span>
    
5. <span data-ttu-id="1f674-133">面接が別のタイム ゾーンでスケジュールされている場合、右上のドロップダウン リストから必要な市区町村/タイムゾーンを選択します。</span><span class="sxs-lookup"><span data-stu-id="1f674-133">If the interviews are scheduled in a different time-zone, pick the required city/time-zone from the drop-down list in the upper right.</span></span> <span data-ttu-id="1f674-134">面接者の面接可能日グリッドは、新しいタイム ゾーンを反映するように更新されます。</span><span class="sxs-lookup"><span data-stu-id="1f674-134">The interviewer availability grid will be updated to reflect the new time zone.</span></span> <span data-ttu-id="1f674-135">このタイム ゾーンの選択は、**面接の概要**ビューにも表示されるようになり、面接者、および候補者に共有されます。</span><span class="sxs-lookup"><span data-stu-id="1f674-135">This time-zone selection will now also display in the **Interview summary** view, which will be shared with the interviewers and the candidate.</span></span> 

6. <span data-ttu-id="1f674-136">**面接者に送信**をクリックして、関係する面接者に会議への招待を送信します。</span><span class="sxs-lookup"><span data-stu-id="1f674-136">Click **Send to interviewers** to send the meeting invites to the interviewers involved.</span></span>

    <span data-ttu-id="1f674-137">面接の要求が面接者に送信された後は、受け取った電子メールの招待状から面接者が直接応答できるようになります。</span><span class="sxs-lookup"><span data-stu-id="1f674-137">After the interview requests have been sent to the interviewers, they can respond directly from the email invite that they receive.</span></span>

    >[!NOTE]
    > <span data-ttu-id="1f674-138">すべての 1 対 1 の面接で、面接者が面接要求に応答しなかった (承認または辞退した) 場合は、24 時間ごとにアラームが面接者に送信されます。</span><span class="sxs-lookup"><span data-stu-id="1f674-138">For all 1:1 interviews, reminders are sent to the interviewers every 24 hours if the interviewer has not responded (accepted or declined) to the interview request.</span></span>

    > <span data-ttu-id="1f674-139">すべてのパネル面接には、面接要求の自動アラームはありません。</span><span class="sxs-lookup"><span data-stu-id="1f674-139">For all panel interviews, there are no automated reminders for the interview request.</span></span> <span data-ttu-id="1f674-140">アラームを手動でトリガーするには、面接を編集し、**更新して送信**オプションを使用して面接者に要求を送り返します。</span><span class="sxs-lookup"><span data-stu-id="1f674-140">To trigger a reminder manually, edit the interview and use the **Update & Send** option to send the request back to the interviewers.</span></span>

    <span data-ttu-id="1f674-141">面接者の応答はキャプチャされ、Attract に表示されます。</span><span class="sxs-lookup"><span data-stu-id="1f674-141">Interviewer responses are captured and shown in Attract.</span></span> <span data-ttu-id="1f674-142">面接者が招待を辞退する場合は、変更を加えるよう通知されます。</span><span class="sxs-lookup"><span data-stu-id="1f674-142">If an interviewer declines the invite, you will be notified to make a change.</span></span> <span data-ttu-id="1f674-143">**スケジューラ**グリッド ビューで応答を表示するには、バブル アイコンをクリックします。</span><span class="sxs-lookup"><span data-stu-id="1f674-143">To view their response in the **Scheduler** grid view, click the bubble icon.</span></span>

<span data-ttu-id="1f674-144">[![面接者の応答の Attract 採用担当者ビュー](./media/schedule-interviewer-response.png)](./media/schedule-interviewer-response.png)</span><span class="sxs-lookup"><span data-stu-id="1f674-144">[![Attract recruiter view of an interviewer's response](./media/schedule-interviewer-response.png)](./media/schedule-interviewer-response.png)</span></span>

7. <span data-ttu-id="1f674-145">面接のスケジュールを候補者と共有する準備が完了したら、**候補者に送信**をクリックします。</span><span class="sxs-lookup"><span data-stu-id="1f674-145">After the interview schedule is ready to be shared with the candidate, click **Send to candidate**.</span></span> <span data-ttu-id="1f674-146">面接者の名前およびスロットを、候補者に対して表示または非表示にすることができます。</span><span class="sxs-lookup"><span data-stu-id="1f674-146">You can choose to hide or show the interviewer names and slots with the candidate.</span></span>

8. <span data-ttu-id="1f674-147">電子メール テンプレートを選択して、候補者に面接の概要を送信します。</span><span class="sxs-lookup"><span data-stu-id="1f674-147">Select an -mail template and send the interview summary to the candidate.</span></span> <span data-ttu-id="1f674-148">候補者は、自分の電子メールおよび自分の候補者ポータルで、この情報を確認できます。</span><span class="sxs-lookup"><span data-stu-id="1f674-148">The candidate can view this information in their email as well as on their candidate portal.</span></span>
    
>[!NOTE] 
> <span data-ttu-id="1f674-149">候補者のカレンダーの面接可能日は、内部候補者の場合のみ表示されます。</span><span class="sxs-lookup"><span data-stu-id="1f674-149">The calendar availability of a candidate is shown only if the candidate is internal.</span></span> <span data-ttu-id="1f674-150">同様に、面接スケジュールの推奨事項を強化するために使用できるのは、内部候補者のみです。</span><span class="sxs-lookup"><span data-stu-id="1f674-150">Similarly, only an internal candidates can be used to enhance interview schedule recommendations.</span></span> <span data-ttu-id="1f674-151">現時点では、候補者 (外部または内部) は会議への電子メールの招待を受信しない代わりに、面接の概要のみを受け取ります。</span><span class="sxs-lookup"><span data-stu-id="1f674-151">Currently, candidates (external or internal) don't receive an email meeting invite, instead the candidate receives only a summary of the interviews.</span></span>

## <a name="feedback-activity"></a><span data-ttu-id="1f674-152">フィードバック活動</span><span class="sxs-lookup"><span data-stu-id="1f674-152">Feedback activity</span></span>

<span data-ttu-id="1f674-153">フィードバック活動は、職務テンプレートではオプションです。</span><span class="sxs-lookup"><span data-stu-id="1f674-153">The feedback activity is optional in a job template.</span></span> <span data-ttu-id="1f674-154">この活動では、面接参加者が申請者に対する推奨事項またはフィードバック コメントを入力できます。</span><span class="sxs-lookup"><span data-stu-id="1f674-154">This activity lets interview participants enter recommendations or feedback comments for an applicant.</span></span> <span data-ttu-id="1f674-155">**採用チームからフィードバック参加者を継承**フィールドを選択すると、採用担当者、採用マネージャー、および面接者がフィードバック活動に自動的に入力されます。</span><span class="sxs-lookup"><span data-stu-id="1f674-155">If the **Inherit feedback participants from Hiring Team** field is selected, the recruiter, hiring manager, and interviewers are automatically entered in the feedback activity.</span></span> <span data-ttu-id="1f674-156">組織は、面接者が自分のフィードバックを送信する前に、他の人のフィードバックを表示することを許可することができます。</span><span class="sxs-lookup"><span data-stu-id="1f674-156">Organizations can allow interviewers to view the feedback of other people before they submit their own feedback.</span></span> <span data-ttu-id="1f674-157">組織は、面接者が提出した後に、そのフィードバックを編集するよう許可することもできます。</span><span class="sxs-lookup"><span data-stu-id="1f674-157">Organizations can also allow interviewers to edit their feedback after they submit it.</span></span> <span data-ttu-id="1f674-158">面接者は、職務テンプレートの一部として事前設定された設定に基づいて、最近行った面接についてのフィードバックを送信するように通知されます。</span><span class="sxs-lookup"><span data-stu-id="1f674-158">Interviewers are reminded to submit feedback for the interviews they have recently conducted based on the preset configuration as part of the job template.</span></span> <span data-ttu-id="1f674-159">職務の採用マネージャーや採用担当者は、面接者に手動でフィードバックを送信するよう通知することもできます。</span><span class="sxs-lookup"><span data-stu-id="1f674-159">The hiring manager or a recruiter on the job can also choose to manually remind an interviewer to submit feedback.</span></span>

## <a name="interview-activity"></a><span data-ttu-id="1f674-160">面接活動</span><span class="sxs-lookup"><span data-stu-id="1f674-160">Interview activity</span></span>

<span data-ttu-id="1f674-161">面接活動は 3 つのコンポーネントのあるオプションの活動です: 候補者の面接可能日の要求、スケジュール、およびフィードバックです。</span><span class="sxs-lookup"><span data-stu-id="1f674-161">The interview activity is an optional activity with three components: Candidate availability request, Schedule, and Feedback.</span></span> <span data-ttu-id="1f674-162">すべての候補者の面接可能日の要求、スケジュールが必要な場合は、職務テンプレートの面接活動を使用します。</span><span class="sxs-lookup"><span data-stu-id="1f674-162">Use the interview activity in the job template if you want all of the candidate’s availability request, schedule.</span></span> <span data-ttu-id="1f674-163">そして、採用プロセスの一部として個別にそれらを使用する代わりに、プロセスの一部としてのフィードバックします。</span><span class="sxs-lookup"><span data-stu-id="1f674-163">and feedback as part of the process instead using them individually as part of the hiring process.</span></span>
