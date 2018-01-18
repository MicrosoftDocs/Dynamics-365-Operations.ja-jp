---
title: "アンケートの配布および記入"
description: "このトピックは、設計したアンケートを、それらを実行するユーザーまたはユーザー グループが記入できるように配布する方法を説明します。"
author: kherr75
manager: AnnBe
ms.date: 04/04/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-talent
ms.technology: 
ms.search.form: KMConnectionType, KMKnowledgeCollectorPlanningTabel, SysEmailParameters
audience: Application User
ms.reviewer: rschloma
ms.search.scope: Operations, Core
ms.custom: 17424
ms.assetid: fd8d867a-2446-400a-b91f-ad4085427470
ms.search.region: Global
ms.author: kherr
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: d9b080ff46a0fbc73ed4f8fa3f03d71e9d758cc2
ms.openlocfilehash: 514de5296ee1fe955cd9ee2ea0d45f74b7c21f70
ms.contentlocale: ja-jp
ms.lasthandoff: 01/17/2018

---

# <a name="distribute-and-complete-a-questionnaire"></a><span data-ttu-id="c12e2-103">アンケートの配布および記入</span><span class="sxs-lookup"><span data-stu-id="c12e2-103">Distribute and complete a questionnaire</span></span>

[!include[banner](includes/banner.md)]


<span data-ttu-id="c12e2-104">このトピックは、設計したアンケートを、それらを実行するユーザーまたはユーザー グループが記入できるように配布する方法を説明します。</span><span class="sxs-lookup"><span data-stu-id="c12e2-104">This topic explains how distribute the questionnaires that you design, so that they are available to the person or group of people who will complete them.</span></span> 

<span data-ttu-id="c12e2-105">アンケートを配布する複数の方法があります。</span><span class="sxs-lookup"><span data-stu-id="c12e2-105">There are multiple ways to distribute a questionnaire:</span></span>

-   <span data-ttu-id="c12e2-106">アンケートを有効としてマークします。</span><span class="sxs-lookup"><span data-stu-id="c12e2-106">Mark the questionnaire as active.</span></span> <span data-ttu-id="c12e2-107">アクセスを制限するようにアンケート グループが設定されていない限り、すべての従業員がアンケートを使用できます。</span><span class="sxs-lookup"><span data-stu-id="c12e2-107">The questionnaire is then available to all employees, unless a questionnaire group is set up to restrict access to it.</span></span>
-   <span data-ttu-id="c12e2-108">アンケート グループへ権限を割り当てます。</span><span class="sxs-lookup"><span data-stu-id="c12e2-108">Assign rights to a questionnaire group.</span></span> <span data-ttu-id="c12e2-109">その後、アンケートは選択したグループのすべてのメンバーが使用できます。</span><span class="sxs-lookup"><span data-stu-id="c12e2-109">The questionnaire is then available to all members of the selected group.</span></span>
-   <span data-ttu-id="c12e2-110">計画済回答セッションを作成します。</span><span class="sxs-lookup"><span data-stu-id="c12e2-110">Create planned answer sessions.</span></span> <span data-ttu-id="c12e2-111">その後、特定の人だけがアンケートを使用できます。</span><span class="sxs-lookup"><span data-stu-id="c12e2-111">The questionnaire is then available only to a particular person.</span></span>
-   <span data-ttu-id="c12e2-112">スケジュールを作成する。</span><span class="sxs-lookup"><span data-stu-id="c12e2-112">Create a schedule.</span></span> <span data-ttu-id="c12e2-113">その後、アンケートは複数のユーザーが使用できます。</span><span class="sxs-lookup"><span data-stu-id="c12e2-113">The questionnaire can then be available to multiple people.</span></span>

## <a name="marking-a-questionnaire-as-active"></a><span data-ttu-id="c12e2-114">アンケートを有効としてマーク</span><span class="sxs-lookup"><span data-stu-id="c12e2-114">Marking a questionnaire as active</span></span>
<span data-ttu-id="c12e2-115">[アンケート] ページの [有効] フィールドで [はい] を選択すると、すべての従業員がアンケートを記入できるようになります。</span><span class="sxs-lookup"><span data-stu-id="c12e2-115">By setting the **Active** field to **Yes** on the **Questionnaires** page, you make the questionnaire available for all employees to complete.</span></span> <span data-ttu-id="c12e2-116">回答者はアンケートを複数回を記入できます。</span><span class="sxs-lookup"><span data-stu-id="c12e2-116">Respondents can complete the questionnaire multiple times.</span></span> <span data-ttu-id="c12e2-117">この機能は、年間を通して絶え間なくフィードバック集める場合に便利です。</span><span class="sxs-lookup"><span data-stu-id="c12e2-117">This functionality is useful if you want to gather continual feedback throughout the year.</span></span> <span data-ttu-id="c12e2-118">たとえば、カフェテリアの昼食サービスに関するフィードバックを提供するために従業員が使用するアンケートを作成することができます。</span><span class="sxs-lookup"><span data-stu-id="c12e2-118">For example, you can make a questionnaire that employees use to give feedback about the lunch service in the cafeteria.</span></span>

## <a name="questionnaire-groups"></a><span data-ttu-id="c12e2-119">アンケート グループ</span><span class="sxs-lookup"><span data-stu-id="c12e2-119">Questionnaire groups</span></span>
<span data-ttu-id="c12e2-120">アンケート グループを設定し、アンケートを配布する必要のある回答者を含めることができます。</span><span class="sxs-lookup"><span data-stu-id="c12e2-120">You can set up questionnaire groups and then include the respondents that a questionnaire should be distributed to.</span></span> 

<span data-ttu-id="c12e2-121">次のページからアンケート グループを作成できます。</span><span class="sxs-lookup"><span data-stu-id="c12e2-121">You can create questionnaire groups from the following pages:</span></span>

-   <span data-ttu-id="c12e2-122">**アンケート グループ** – アンケート グループのユーザーのみが、選択されたアンケートを実行できます。</span><span class="sxs-lookup"><span data-stu-id="c12e2-122">**Questionnaire groups** – Only individuals in a questionnaire group can complete a selected questionnaire.</span></span> <span data-ttu-id="c12e2-123">たとえば、対象ユーザーが契約社員のため、それらの回答者に固有のアンケート グループを作成する場合もあります。</span><span class="sxs-lookup"><span data-stu-id="c12e2-123">For example, your intended audience is contractors, so you create a questionnaire group that is specific to those respondents.</span></span>
-   <span data-ttu-id="c12e2-124">**アンケート グループのメンバー** – アンケート グループに人を追加できます。</span><span class="sxs-lookup"><span data-stu-id="c12e2-124">**Questionnaire group members** – You can add people to the questionnaire groups.</span></span>

<span data-ttu-id="c12e2-125">アンケートにアンケート グループを割り当てるには、[アンケート] ページで [ユーザーの権限] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="c12e2-125">To assign a questionnaire group to a questionnaire, on the **Questionnaires** page, click **User rights**.</span></span> <span data-ttu-id="c12e2-126">アンケートが有効として保存された後、アンケート グループのメンバーは、アンケートを記入できます。</span><span class="sxs-lookup"><span data-stu-id="c12e2-126">After the questionnaire is saved as active, the members of the questionnaire group can complete the questionnaire.</span></span> <span data-ttu-id="c12e2-127">この機能は、大きなグループに発行する前に選択したユーザー グループにアンケートをテストする場合や、極めて特殊なユーザーをアンケートの対象とする場合に便利です。</span><span class="sxs-lookup"><span data-stu-id="c12e2-127">This functionality is helpful if you want to test a questionnaire on a select group of people before you roll it out to a larger group, or if you want to target a questionnaire to a very specific audience.</span></span>

## <a name="planned-answer-sessions-in-a-questionnaire"></a><span data-ttu-id="c12e2-128">アンケートの計画済回答セッション</span><span class="sxs-lookup"><span data-stu-id="c12e2-128">Planned answer sessions in a questionnaire</span></span>
<span data-ttu-id="c12e2-129">計画済回答セッションは、回答者をデザインおよび選択したアンケートです。</span><span class="sxs-lookup"><span data-stu-id="c12e2-129">Planned answer sessions are questionnaires that you've designed and selected the respondents for.</span></span> 

> <span data-ttu-id="c12e2-130">**メモ:** 計画済回答セッションを設定する前に、アンケートをデザインする必要があります。</span><span class="sxs-lookup"><span data-stu-id="c12e2-130">**Note** Before you can set up planned answer sessions, you must design a questionnaire.</span></span> 

<span data-ttu-id="c12e2-131">[計画済回答セッション] ページで、個々の従業員に対して計画済回答セッションを作成できます。</span><span class="sxs-lookup"><span data-stu-id="c12e2-131">On the **Planned answer session** page, you can create a planned answer session for an individual employee.</span></span> <span data-ttu-id="c12e2-132">ページの一覧には、計画されたすべてのアンケートが表示されます。</span><span class="sxs-lookup"><span data-stu-id="c12e2-132">The list on the page displays all planned questionnaires.</span></span> 

<span data-ttu-id="c12e2-133">計画済回答セッションは [アンケートのスケジュール] ページでも使用され、そこで複数の人に対してアンケートを計画できます。</span><span class="sxs-lookup"><span data-stu-id="c12e2-133">Planned answer sessions are also used on the **Questionnaire schedules** page, where you can plan questionnaires for multiple people:</span></span>

-   <span data-ttu-id="c12e2-134">従業員</span><span class="sxs-lookup"><span data-stu-id="c12e2-134">Employees</span></span>
-   <span data-ttu-id="c12e2-135">コース参加者</span><span class="sxs-lookup"><span data-stu-id="c12e2-135">Course participants</span></span>
-   <span data-ttu-id="c12e2-136">組織ユニット</span><span class="sxs-lookup"><span data-stu-id="c12e2-136">Organizational units</span></span>

<span data-ttu-id="c12e2-137">各人は、アンケートに 1 回だけ回答できます。</span><span class="sxs-lookup"><span data-stu-id="c12e2-137">Each person can answer the questionnaire only one time.</span></span>

## <a name="scheduling-a-questionnaire"></a><span data-ttu-id="c12e2-138">アンケートのスケジューリング</span><span class="sxs-lookup"><span data-stu-id="c12e2-138">Scheduling a questionnaire</span></span>
<span data-ttu-id="c12e2-139">オプションで、複数の回答者に対して 1 つのアンケートをスケジュールできます。</span><span class="sxs-lookup"><span data-stu-id="c12e2-139">You can optionally schedule a questionnaire for multiple respondents.</span></span>

### <a name="planning-types"></a><span data-ttu-id="c12e2-140">計画タイプ</span><span class="sxs-lookup"><span data-stu-id="c12e2-140">Planning types</span></span>

<span data-ttu-id="c12e2-141">複数の回答者に対する計画済回答セッションをスケジュールする場合、計画タイプが必要になります。</span><span class="sxs-lookup"><span data-stu-id="c12e2-141">Planning types are required if you want to schedule planned answer sessions for multiple respondents.</span></span> <span data-ttu-id="c12e2-142">計画タイプがアンケート スケジュールを分類するために使用されます。</span><span class="sxs-lookup"><span data-stu-id="c12e2-142">Planning types are used to classify questionnaire schedules.</span></span> <span data-ttu-id="c12e2-143">たとえば、次の目的のためにアンケートをスケジュールできます。</span><span class="sxs-lookup"><span data-stu-id="c12e2-143">For example, you can schedule questionnaires for the following purposes:</span></span>

-   <span data-ttu-id="c12e2-144">評価</span><span class="sxs-lookup"><span data-stu-id="c12e2-144">Evaluation</span></span>
-   <span data-ttu-id="c12e2-145">調査</span><span class="sxs-lookup"><span data-stu-id="c12e2-145">Survey</span></span>
-   <span data-ttu-id="c12e2-146">テスト</span><span class="sxs-lookup"><span data-stu-id="c12e2-146">Testing</span></span>

<span data-ttu-id="c12e2-147">[アンケートのスケジュール] ページで、アンケート スケジュールの計画タイプを指定できます。</span><span class="sxs-lookup"><span data-stu-id="c12e2-147">You can specify planning types for a questionnaire schedule on the **Questionnaire schedules** page.</span></span>

### <a name="reference-types-for-questionnaire"></a><span data-ttu-id="c12e2-148">アンケートの参照タイプ</span><span class="sxs-lookup"><span data-stu-id="c12e2-148">Reference types for questionnaire</span></span>

<span data-ttu-id="c12e2-149">参照タイプを使用して、アンケートをいつスケジューリングするかを選択できる回答者の条件を入力できます。</span><span class="sxs-lookup"><span data-stu-id="c12e2-149">You can use reference types to enter criteria for the respondents that you might select when you schedule a questionnaire.</span></span> 

<span data-ttu-id="c12e2-150">[参照タイプ] ページを使用してアンケートの参照タイプを設定します。</span><span class="sxs-lookup"><span data-stu-id="c12e2-150">Use the **Reference types** page to set up reference types for a questionnaire.</span></span> <span data-ttu-id="c12e2-151">各参照タイプは Microsoft Dynamics 365 for Finance and Operations のテーブルに対応します。</span><span class="sxs-lookup"><span data-stu-id="c12e2-151">Each reference type corresponds to a table in Microsoft Dynamics 365 for Finance and Operations.</span></span> <span data-ttu-id="c12e2-152">アンケート スケジュールを作成すると、テーブル内の個々のレコードや、アンケートが関連付けられるレコードの範囲を指定できます。</span><span class="sxs-lookup"><span data-stu-id="c12e2-152">When you create questionnaire schedules, you can specify individual records in the table or a range of records that the questionnaire will be associated with.</span></span> 

<span data-ttu-id="c12e2-153">たとえば、コース テーブルを選択した場合、アンケートが使用される特定のコースを決定できます。</span><span class="sxs-lookup"><span data-stu-id="c12e2-153">For example, if you select the Courses table, you can decide which specific course the questionnaire will be for.</span></span> <span data-ttu-id="c12e2-154">コース テーブルの参照を設定すると、[コース] ページの一部のフィールドおよびボタンが使用できるようになります。</span><span class="sxs-lookup"><span data-stu-id="c12e2-154">When you set up a reference for the Courses table, some fields and buttons on the **Courses** page become available.</span></span>

### <a name="questionnaire-schedules"></a><span data-ttu-id="c12e2-155">アンケートのスケジュール</span><span class="sxs-lookup"><span data-stu-id="c12e2-155">Questionnaire schedules</span></span>

<span data-ttu-id="c12e2-156">参照タイプに基づいて、ユーザー グループの 1 つに複数の計画済回答セッションを生成するためにアンケート スケジュールを使用できます。</span><span class="sxs-lookup"><span data-stu-id="c12e2-156">You can use questionnaire schedules to generate multiple planned answer sessions for a group of users, based on a reference type.</span></span> <span data-ttu-id="c12e2-157">[アンケートのスケジュール] ページでスケジュールを作成します。</span><span class="sxs-lookup"><span data-stu-id="c12e2-157">Create a schedule on the **Questionnaire schedules** page.</span></span> <span data-ttu-id="c12e2-158">スケジュールを分類する計画タイプを選択し、特定のユーザーのシステムをクエリするのに使用する参照タイプを選択します。</span><span class="sxs-lookup"><span data-stu-id="c12e2-158">Select the planning type to categorize the schedule, and also select the reference type that should be used to query the system for specific users.</span></span> <span data-ttu-id="c12e2-159">たとえば、参照タイプをコース テーブルに設定すると、[参照] フィールドで特定のコースを選択できます。</span><span class="sxs-lookup"><span data-stu-id="c12e2-159">For example, if you set the reference type to the Courses table, you can select a specific course in the **Reference** field.</span></span> 

<span data-ttu-id="c12e2-160">アンケートおよびそのほかの基準を選択するには、[設定の詳細] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="c12e2-160">Click **Setup details** to select the questionnaire and other criteria.</span></span> <span data-ttu-id="c12e2-161">たとえば、アンケートが講師の評価の場合、講師名を基準として指定します。</span><span class="sxs-lookup"><span data-stu-id="c12e2-161">For example, specify the instructor's name as a criterion if the questionnaire is an evaluation of the instructor.</span></span> <span data-ttu-id="c12e2-162">設定の詳細の入力が完了したら、システムはクエリに含まれているユーザーの計画済回答セッションを生成します。</span><span class="sxs-lookup"><span data-stu-id="c12e2-162">After you've finished entering the setup details, the system generates planned answer sessions for the users that are included in the query.</span></span> 

<span data-ttu-id="c12e2-163">スケジュールの回答セッションを表示するには、[計画済回答セッション] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="c12e2-163">Click **Planned answer sessions** to view the answer sessions for the schedule.</span></span> <span data-ttu-id="c12e2-164">その後、追加の計画済回答セッションを手動で作成するか、回答されていない計画済回答セッションを削除できます。</span><span class="sxs-lookup"><span data-stu-id="c12e2-164">You can then manually create additional planned answer sessions or delete planned answer sessions that haven't been answered.</span></span> 

<span data-ttu-id="c12e2-165">アンケートを関連する計画済回答セッションのユーザーが利用できるようにするには、[機能] &gt; [開始] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="c12e2-165">Click **Functions** &gt; **Start** to make the questionnaire available to the users in related planned answer sessions.</span></span> <span data-ttu-id="c12e2-166">アンケートに記入された回答を表示するには、[回答] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="c12e2-166">Click **Answers** to view the completed responses to the questionnaire.</span></span> <span data-ttu-id="c12e2-167">オプションでアンケート スケジュールの設定、計画済回答セッションおよび回答を新しいアンケート スケジュールにコピーできます。</span><span class="sxs-lookup"><span data-stu-id="c12e2-167">You can optionally copy the questionnaire schedule settings, planned answer sessions, and answers to a new questionnaire schedule.</span></span>

## <a name="notifying-respondents-about-questionnaires-that-are-available-to-them"></a><span data-ttu-id="c12e2-168">回答者へ使用できるアンケートの通知</span><span class="sxs-lookup"><span data-stu-id="c12e2-168">Notifying respondents about questionnaires that are available to them</span></span>
<span data-ttu-id="c12e2-169">アンケートを配布するとき、アンケートを使用できることを回答者に通知する必要があります。</span><span class="sxs-lookup"><span data-stu-id="c12e2-169">When you distribute a questionnaire, you must notify respondents that questionnaires are available to them.</span></span> 

### <a name="notifying-respondents-about-a-planned-answer-session"></a><span data-ttu-id="c12e2-170">計画済回答セッションの回答者への通知</span><span class="sxs-lookup"><span data-stu-id="c12e2-170">Notifying respondents about a planned answer session</span></span>

<span data-ttu-id="c12e2-171">計画済回答セッションを使用する場合、電話または電子メールなどで個人に直接通知する必要があります。</span><span class="sxs-lookup"><span data-stu-id="c12e2-171">If you use a planned answer session, you must notify the person directly, such as by telephone or email.</span></span>

### <a name="notifying-respondents-about-a-scheduling"></a><span data-ttu-id="c12e2-172">スケジューリングの回答者への通知</span><span class="sxs-lookup"><span data-stu-id="c12e2-172">Notifying respondents about a scheduling</span></span>

<span data-ttu-id="c12e2-173">アンケートに割り当てられたすべての回答者に電子メールを準備および送信するには、[アンケートのスケジュール] ページを使用します。</span><span class="sxs-lookup"><span data-stu-id="c12e2-173">Use the **Questionnaire schedules** page to prepare and send email to all respondents who are assigned to the questionnaire.</span></span> <span data-ttu-id="c12e2-174">[従業員セルフ サービス用の電子メール] タブで電子メール テキストを入力します。スケジュールが開始された後、[機能] &gt; [電子メールの送信] をクリックして、電子メールを生成し回答者に送信します。</span><span class="sxs-lookup"><span data-stu-id="c12e2-174">Enter the email text on the **E-mail for employee self service** tab. After the schedule has been started, click **Functions** &gt; **Send e-mail** to generate and send the email to the respondents.</span></span> <span data-ttu-id="c12e2-175">その後、回答者は Web サイトにサインインしてアンケートを記入できます。</span><span class="sxs-lookup"><span data-stu-id="c12e2-175">Respondents can then sign in to the website and complete the questionnaire.</span></span> 

> <span data-ttu-id="c12e2-176">**メモ** 電子メール機能を使用する前に、IT 管理者は [電子メール パラメーター] ページに電子メール設定を入力する必要があります。</span><span class="sxs-lookup"><span data-stu-id="c12e2-176">**Note** Before you can use the email functionality, your IT administrator must enter the email settings on the **E-mail parameters** page.</span></span>

## <a name="ending-a-scheduled-questionnaire"></a><span data-ttu-id="c12e2-177">スケジュール済アンケートの終了</span><span class="sxs-lookup"><span data-stu-id="c12e2-177">Ending a scheduled questionnaire</span></span>
<span data-ttu-id="c12e2-178">すべての回答者が割り当てられた回答セッションを完了した後に、スケジュール済アンケートを終了できます。</span><span class="sxs-lookup"><span data-stu-id="c12e2-178">You can end a scheduled questionnaire after all respondents have completed their assigned answer sessions.</span></span> <span data-ttu-id="c12e2-179">予定のアンケートが終了すると、その設定は新しいスケジューリングにコピーできません。</span><span class="sxs-lookup"><span data-stu-id="c12e2-179">After a scheduled questionnaire is ended, you can't copy its settings to a new schedule.</span></span> 

> <span data-ttu-id="c12e2-180">**メモ** 1 人以上の回答者がアンケートを記入していない状態で、スケジューリングを完了する場合は、まず [計画済回答セッション] ページの一覧から関係ある回答者を削除してください。</span><span class="sxs-lookup"><span data-stu-id="c12e2-180">**Note** If one or more respondents haven't completed the questionnaire, but you still want to end the scheduling, you must first delete those respondents from the list on the **Planned answer session** page.</span></span> <span data-ttu-id="c12e2-181">その後、スケジューリングを終了できます。</span><span class="sxs-lookup"><span data-stu-id="c12e2-181">You can then end the schedule.</span></span>

## <a name="completing-questionnaires"></a><span data-ttu-id="c12e2-182">アンケートの記入</span><span class="sxs-lookup"><span data-stu-id="c12e2-182">Completing questionnaires</span></span>
<span data-ttu-id="c12e2-183">アンケートを作成し、配布した後、アンケートは選択した回答者が回答することができます。</span><span class="sxs-lookup"><span data-stu-id="c12e2-183">After you've designed and distributed a questionnaire, the questionnaire can be completed by selected respondents.</span></span> <span data-ttu-id="c12e2-184">アクセスが許可されているアンケートには、次の 2 か所から記入できます。</span><span class="sxs-lookup"><span data-stu-id="c12e2-184">You can complete the questionnaires that are available to you from two locations:</span></span>

-   <span data-ttu-id="c12e2-185">ナビゲーション ウィンドウで、[アンケート] &gt; [配布] &gt; [アンケートの記入] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="c12e2-185">In the navigation pane, click **Questionnaires** &gt; **Distribute** &gt; **Complete a questionnaire**.</span></span>
-   <span data-ttu-id="c12e2-186">[従業員セルフ サービス] で、[記入するアンケート] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="c12e2-186">In Employee self-service, click **Questionnaires to complete**.</span></span>

<span data-ttu-id="c12e2-187">アンケートへのアクセス許可は、特定のユーザーまたはユーザー グループに限定する場合と、ネットワーク内のすべてのユーザーに与える場合があります。</span><span class="sxs-lookup"><span data-stu-id="c12e2-187">Questionnaires can made be available to specific users or groups of users, or to all users in a network.</span></span>

<a name="see-also"></a><span data-ttu-id="c12e2-188">参照</span><span class="sxs-lookup"><span data-stu-id="c12e2-188">See also</span></span>
--------

[<span data-ttu-id="c12e2-189">アンケートのデザイン</span><span class="sxs-lookup"><span data-stu-id="c12e2-189">Designing questionnaires</span></span>](design-questionnaires.md)

[<span data-ttu-id="c12e2-190">アンケートの使用</span><span class="sxs-lookup"><span data-stu-id="c12e2-190">Using questionnaires</span></span>](questionnaires.md)

[<span data-ttu-id="c12e2-191">アンケート結果を表示して評価する</span><span class="sxs-lookup"><span data-stu-id="c12e2-191">Viewing and evaluating the results of questionnaires</span></span>](evaluate-questionnaire-results.md)



