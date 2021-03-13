---
title: 職務候補者の採用
description: このトピックでは、Dynamics 365 Human Resources でどのように候補者を採用するかを説明します。
author: andreabichsel
manager: tfehr
ms.date: 12/03/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-human-resources
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Human Resources
ms.custom: 7521
ms.assetid: ''
ms.search.region: Global
ms.author: anbichse
ms.search.validFrom: 2020-12-03
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: f615584785ba48a140e4e97991a4594047fea8ee
ms.sourcegitcommit: ea2d652867b9b83ce6e5e8d6a97d2f9460a84c52
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 02/03/2021
ms.locfileid: "5113185"
---
# <a name="recruit-job-candidates"></a><span data-ttu-id="32af5-103">職務候補者の採用</span><span class="sxs-lookup"><span data-stu-id="32af5-103">Recruit job candidates</span></span>

[!include [banner](includes/preview-feature.md)]

<span data-ttu-id="32af5-104">Dynamics 365 Human Resources を使用すると、採用要求の管理が簡単になります。</span><span class="sxs-lookup"><span data-stu-id="32af5-104">Dynamics 365 Human Resources helps you to manage recruiting requests.</span></span> <span data-ttu-id="32af5-105">また、職務の候補者が従業員になるまでの移行をシームレスに実行することもできます。</span><span class="sxs-lookup"><span data-stu-id="32af5-105">It also helps you seamlessly transition job candidates to employees.</span></span> <span data-ttu-id="32af5-106">組織で別の採用アプリケーションを使用している場合、採用プロセスには次の手順が含まれる場合があります。</span><span class="sxs-lookup"><span data-stu-id="32af5-106">If your organization uses a separate recruiting application, your recruiting process might include the following steps:</span></span>

- <span data-ttu-id="32af5-107">採用要求を Human Resources に入力する。</span><span class="sxs-lookup"><span data-stu-id="32af5-107">Enter your recruiting request in Human Resources.</span></span>
- <span data-ttu-id="32af5-108">採用アプリケーションから候補者の推薦状を Human Resources で受け取る。</span><span class="sxs-lookup"><span data-stu-id="32af5-108">Receive candidate referrals in Human Resources from the recruiting application.</span></span>
- <span data-ttu-id="32af5-109">Human Resources で候補者の承認プロセスを完了する。</span><span class="sxs-lookup"><span data-stu-id="32af5-109">Complete the candidate approval process in Human Resources.</span></span>

<span data-ttu-id="32af5-110">別の採用アプリケーションを使用していない場合は、Human Resources で手動で候補者を管理することもできます。</span><span class="sxs-lookup"><span data-stu-id="32af5-110">If you aren't using a separate recruiting application, you can also manually manage candidates in Human Resources.</span></span>

>[!NOTE]
><span data-ttu-id="32af5-111">管理者または開発者が Human Resources とサードパーティの採用アプリケーションを統合する場合は、[Dataverse 統合の構成](hr-admin-integration-common-data-service.md) および [Dataverse 仮想エンティティの構成](hr-admin-integration-common-data-service-virtual-entities.md) を参照してください</span><span class="sxs-lookup"><span data-stu-id="32af5-111">If you're an admin or developer and want to integrate Human Resources with a third-party recruiting application, see [Configure Dataverse integration](hr-admin-integration-common-data-service.md) and [Configure Dataverse virtual tables](hr-admin-integration-common-data-service-virtual-entities.md)</span></span>
>
> <span data-ttu-id="32af5-112">[AppSource](https://appsource.microsoft.com/marketplace/apps?search=recruiting%20dynamics) からも採用統合アプリを利用できます。</span><span class="sxs-lookup"><span data-stu-id="32af5-112">You can also find recruiting integration apps on [AppSource](https://appsource.microsoft.com/marketplace/apps?search=recruiting%20dynamics).</span></span>
>
> <span data-ttu-id="32af5-113">LinkedIn Talent Hub との統合で使用するプレビュー機能を試すには、[LinkedIn Talent Hub との統合](hr-admin-integration-linkedin.md)を参照してください。</span><span class="sxs-lookup"><span data-stu-id="32af5-113">To try out our preview feature for integrating with LinkedIn Talent Hub, see [Integrate with LinkedIn Talent Hub](hr-admin-integration-linkedin.md).</span></span>

## <a name="enable-recruiting-requests"></a><span data-ttu-id="32af5-114">採用要求を有効にする</span><span class="sxs-lookup"><span data-stu-id="32af5-114">Enable recruiting requests</span></span>

<span data-ttu-id="32af5-115">Human Resources に採用要求を送信する場合は、まず **Human Resources 共有パラメーター** で機能を有効にする必要があります。</span><span class="sxs-lookup"><span data-stu-id="32af5-115">If you want to submit recruiting requests in Human Resources, you must first enable the functionality in **Human resources shared parameters**.</span></span>

1. <span data-ttu-id="32af5-116">**人事管理** ワークスペースで、**リンク** を選択します。</span><span class="sxs-lookup"><span data-stu-id="32af5-116">In the **Personnel management** workspace, select **Links**.</span></span>

2. <span data-ttu-id="32af5-117">**設定** で、**人事管理共有パラメーター** を選択します。</span><span class="sxs-lookup"><span data-stu-id="32af5-117">Under **Setup**, select **Human resources shared parameters**.</span></span>

3. <span data-ttu-id="32af5-118">**採用** の **採用** タブで、 **採用要求の有効化** を **はい** に設定します。</span><span class="sxs-lookup"><span data-stu-id="32af5-118">On the **Recruitment** tab, under **RECRUITING**, set **Enable recruiting requests** to **Yes**.</span></span>

## <a name="add-a-recruiting-request-location"></a><span data-ttu-id="32af5-119">採用要求の勤務場所の追加</span><span class="sxs-lookup"><span data-stu-id="32af5-119">Add a recruiting request location</span></span>

<span data-ttu-id="32af5-120">組織に勤務場所が複数ある場合は、勤務場所を追加して、要求者が新しい採用がある勤務場所を選択できるようにできます。</span><span class="sxs-lookup"><span data-stu-id="32af5-120">If your organization has multiple locations, you can add them so requestors can select a location where the new recruit will be working.</span></span> <span data-ttu-id="32af5-121">勤務場所は求人情報に記載されます。</span><span class="sxs-lookup"><span data-stu-id="32af5-121">The location will be included in the job posting.</span></span>

1. <span data-ttu-id="32af5-122">検索バーで **採用要求の勤務場所** を入力します。</span><span class="sxs-lookup"><span data-stu-id="32af5-122">In the search bar, enter **recruiting request location**.</span></span>

2. <span data-ttu-id="32af5-123">**新規** を選択します。</span><span class="sxs-lookup"><span data-stu-id="32af5-123">Select **New**.</span></span>

3. <span data-ttu-id="32af5-124">**採用要求の勤務場所** フィールドに、勤務場所の名前を入力します。</span><span class="sxs-lookup"><span data-stu-id="32af5-124">In the **Recruiting request location** field, enter the location name.</span></span>

   ![採用要求の勤務場所の追加](./media/hr-recruit-0a-add-location.png)

4. <span data-ttu-id="32af5-126">**説明** フィールドに、勤務場所の説明を入力します。</span><span class="sxs-lookup"><span data-stu-id="32af5-126">In the **Description**, enter a description for the location.</span></span>

5. <span data-ttu-id="32af5-127">**勤務場所** で、**追加** を選択します。</span><span class="sxs-lookup"><span data-stu-id="32af5-127">Under **Location**, select **Add**.</span></span> <span data-ttu-id="32af5-128">**新しい住所** と表示された場合は、その勤務場所の住所を入力します。</span><span class="sxs-lookup"><span data-stu-id="32af5-128">If the **New address** popout appears, enter the address for the location.</span></span>

   ![住所の入力](./media/hr-recruit-0b-address.png)

6. <span data-ttu-id="32af5-130">**連絡先情報** で、勤務場所の連絡先の情報を入力します。</span><span class="sxs-lookup"><span data-stu-id="32af5-130">Under **Contact information**, enter the information for the location's contact.</span></span>

7. <span data-ttu-id="32af5-131">**保存** を選択します。</span><span class="sxs-lookup"><span data-stu-id="32af5-131">Select **Save**.</span></span>

## <a name="add-a-recruiting-request"></a><span data-ttu-id="32af5-132">採用要求の追加</span><span class="sxs-lookup"><span data-stu-id="32af5-132">Add a recruiting request</span></span>

<span data-ttu-id="32af5-133">管理者は、Human Resources に採用要求を送信できます。</span><span class="sxs-lookup"><span data-stu-id="32af5-133">Managers can submit recruiting requests in Human Resources.</span></span> <span data-ttu-id="32af5-134">別の採用アプリケーションを使用する場合は、これらの手順を完了すると採用要求が送信され、そのアプリケーションで採用プロセスが開始されます。</span><span class="sxs-lookup"><span data-stu-id="32af5-134">If you use a separate recruiting application, completing these steps will send a recruiting request and start the recruiting process in that application.</span></span> <span data-ttu-id="32af5-135">それ以外の場合は、この手順を実行して、社内採用プロセスのワークフローを開始します。</span><span class="sxs-lookup"><span data-stu-id="32af5-135">Otherwise, complete this procedure to begin the workflow for your own internal recruiting process.</span></span>

1. <span data-ttu-id="32af5-136">**従業員セルフ サービス** を選択します。</span><span class="sxs-lookup"><span data-stu-id="32af5-136">Select **Employee self service**.</span></span>

2. <span data-ttu-id="32af5-137">**自分のチーム** タブを選択します。</span><span class="sxs-lookup"><span data-stu-id="32af5-137">Select the **My team** tab.</span></span>

3. <span data-ttu-id="32af5-138">**採用を要求** を選択します。</span><span class="sxs-lookup"><span data-stu-id="32af5-138">Select  **Request to recruit**.</span></span>

   ![採用要求の開始](./media/hr-recruit-1-request-to-recruit.png)

4. <span data-ttu-id="32af5-140">**説明**、**職務**、および **予想開始日** フィールドに入力します。</span><span class="sxs-lookup"><span data-stu-id="32af5-140">Complete the **Description**, **Job**, and **Estimated start date** fields.</span></span>

   ![採用要求の完了](./media/hr-recruit-2-request-to-recruit.png)

5. <span data-ttu-id="32af5-142">**続行** を選択します。</span><span class="sxs-lookup"><span data-stu-id="32af5-142">Select **Continue**.</span></span> <span data-ttu-id="32af5-143">希望する職務の採用要求が表示されます。</span><span class="sxs-lookup"><span data-stu-id="32af5-143">The recruiting request for your position appears.</span></span>

6. <span data-ttu-id="32af5-144">**一般** で、**採用担当者** ドロップダウンから採用担当者を選択し、**採用要求の勤務場所** ドロップダウンから勤務場所を選択します。</span><span class="sxs-lookup"><span data-stu-id="32af5-144">Under **General**, select a recruiter from the **Recruiter** dropdown, and then select a location from the **Recruiting request location** dropdown.</span></span>

7. <span data-ttu-id="32af5-145">**職務** で、必要に応じて情報を変更し、**職務から詳細を作成** を選択します。</span><span class="sxs-lookup"><span data-stu-id="32af5-145">Under **Job**, change any information as needed, and then select **Create details from job**.</span></span>

   ![職務から詳細を作成](./media/hr-recruit-3-create-details-from-job.png)

   <span data-ttu-id="32af5-147">採用要求の残りの部分には、入力した職務の既定の情報が入力されます。</span><span class="sxs-lookup"><span data-stu-id="32af5-147">The rest of the recruiting request will populate with the default information for the job you entered.</span></span>

8. <span data-ttu-id="32af5-148">**外部説明** で、外部向け職務明細書を入力します。</span><span class="sxs-lookup"><span data-stu-id="32af5-148">Under **External description**, enter an external-facing job description.</span></span>

9. <span data-ttu-id="32af5-149">**職位** で **追加** を選択してから、この採用要求の職位を選択します。</span><span class="sxs-lookup"><span data-stu-id="32af5-149">Under **Positions**, select **Add**, and then select a position for this recruiting request.</span></span>

   ![職位の追加](./media/hr-recruit-4-select-position.png)

10. <span data-ttu-id="32af5-151">**スキル** で **追加** を選択してからスキルを選択します。</span><span class="sxs-lookup"><span data-stu-id="32af5-151">Under **Skills**, select **Add**, and then select a skill.</span></span>

11. <span data-ttu-id="32af5-152">**学歴要件** で **追加** を選択してから、**学歴** および **最終学歴** ドロップダウンから学歴を選択します。</span><span class="sxs-lookup"><span data-stu-id="32af5-152">Under **Educational requirements**, select **Add**, and then select values from the **Education** and **Level of education** dropdowns.</span></span>

   ![学歴要件の追加](./media/hr-recruit-5-select-educational-requirements.png)

12. <span data-ttu-id="32af5-154">**コメント** で、必要に応じてコメントを追加します。</span><span class="sxs-lookup"><span data-stu-id="32af5-154">Under **Comment**, add comments as necessary.</span></span>

13. <span data-ttu-id="32af5-155">**報酬** で **レベル** からレベルを選択してから、必要に応じて **低しきい値**、**制御ポイント**、**高しきい値** を調整します。</span><span class="sxs-lookup"><span data-stu-id="32af5-155">Under **Compensation**, select a level from the **Level** dropdown, and then adjust **Low threshold**, **Control point**, and **High threshold** as necessary.</span></span>

14. <span data-ttu-id="32af5-156">採用要求が完了し採用プロセスを開始する準備ができたら、メニュー バーの **有効化** を選択します。</span><span class="sxs-lookup"><span data-stu-id="32af5-156">When your recruiting request is complete and you're ready to start the recruiting process, select **Activate** in the menu bar.</span></span>

   ![採用要求の有効化](./media/hr-recruit-6-activate-recruit-request.png)

15. <span data-ttu-id="32af5-158">**保存** を選択します。</span><span class="sxs-lookup"><span data-stu-id="32af5-158">Select **Save**.</span></span>

## <a name="view-and-edit-your-recruiting-requests"></a><span data-ttu-id="32af5-159">採用要求の表示と編集</span><span class="sxs-lookup"><span data-stu-id="32af5-159">View and edit your recruiting requests</span></span>

<span data-ttu-id="32af5-160">マネージャーに要求を表示する場合は、次の操作を行います。</span><span class="sxs-lookup"><span data-stu-id="32af5-160">If you're a manager and want to view your own requests:</span></span>

1. <span data-ttu-id="32af5-161">**従業員セルフ サービス** を選択します。</span><span class="sxs-lookup"><span data-stu-id="32af5-161">Select **Employee self service**.</span></span>

2. <span data-ttu-id="32af5-162">**自分のチーム** タブを選択します。</span><span class="sxs-lookup"><span data-stu-id="32af5-162">Select the **My team** tab.</span></span>

3. <span data-ttu-id="32af5-163">**自分のチームの情報** で、**採用要求** タブを選択します。</span><span class="sxs-lookup"><span data-stu-id="32af5-163">Under **My team information**, select the **Recruiting requests** tab.</span></span>

   ![[採用要求] タブの選択](./media/hr-recruit-7-recruiting-requests.png)

4. <span data-ttu-id="32af5-165">採用要求を表示または編集するには、グリッドで選択します。</span><span class="sxs-lookup"><span data-stu-id="32af5-165">To view or edit a recruiting request, select it in the grid.</span></span>

<span data-ttu-id="32af5-166">HR のプロフェッショナルにすべての採用要求を表示するには、次の操作を行います。</span><span class="sxs-lookup"><span data-stu-id="32af5-166">If you're an HR pro and want to view all recruiting requests:</span></span>

1. <span data-ttu-id="32af5-167">**人事管理** を選択する。</span><span class="sxs-lookup"><span data-stu-id="32af5-167">Select **Personnel management**.</span></span>

2. <span data-ttu-id="32af5-168">**採用要求** を選択する。</span><span class="sxs-lookup"><span data-stu-id="32af5-168">Select **Recruiting requests**.</span></span>

   ![人事管理で採用要求を表示する](./media/hr-recruit-8-recruiting-requests-personnel-management.png)

3. <span data-ttu-id="32af5-170">採用要求を表示または編集するには、グリッドで選択します。</span><span class="sxs-lookup"><span data-stu-id="32af5-170">To view or edit a recruiting request, select it in the grid.</span></span>

## <a name="add-or-edit-a-candidate-profile"></a><span data-ttu-id="32af5-171">候補者プロファイルの追加または編集</span><span class="sxs-lookup"><span data-stu-id="32af5-171">Add or edit a candidate profile</span></span>

<span data-ttu-id="32af5-172">採用要求を管理するために組織が別のアプリケーションと統合している場合、採用要求はそのアプリケーションに転送されます。</span><span class="sxs-lookup"><span data-stu-id="32af5-172">If your organization has integrated with another application to manage recruiting requests, recruiting requests are forwarded to that application.</span></span> <span data-ttu-id="32af5-173">その後、採用アプリケーションが候補者の情報を Human Resources に送り返します。</span><span class="sxs-lookup"><span data-stu-id="32af5-173">The recruiting application then sends candidate information back to Human Resources.</span></span> <span data-ttu-id="32af5-174">それ以外の場合は、独自の内部採用プロセスに従って、候補者の情報を手動で入力できます。</span><span class="sxs-lookup"><span data-stu-id="32af5-174">Otherwise, you can follow your own internal recruiting processes and enter candidate information manually.</span></span>

1. <span data-ttu-id="32af5-175">**人事管理** を選択する。</span><span class="sxs-lookup"><span data-stu-id="32af5-175">Select **Personnel management**.</span></span>

2. <span data-ttu-id="32af5-176">**リンク** を選択します。</span><span class="sxs-lookup"><span data-stu-id="32af5-176">Select **Links**.</span></span>

3. <span data-ttu-id="32af5-177">**採用** で **候補者** を選択します。</span><span class="sxs-lookup"><span data-stu-id="32af5-177">Under **Recruiting**, select **Candidates**.</span></span>

   ![候補者の表示](./media/hr-recruit-9-candidates.png)

4. <span data-ttu-id="32af5-179">候補者を追加するには、**新規** を選択します。</span><span class="sxs-lookup"><span data-stu-id="32af5-179">To add a candidate, select **New**.</span></span> <span data-ttu-id="32af5-180">既存の候補者を編集するには、リストから候補者を選択し、**編集** を選択します。</span><span class="sxs-lookup"><span data-stu-id="32af5-180">To edit an existing candidate, select the candidate from the list and then select **Edit**.</span></span> <span data-ttu-id="32af5-181">候補者のプロファイルが表示されます。</span><span class="sxs-lookup"><span data-stu-id="32af5-181">The candidate profile appears.</span></span>

5. <span data-ttu-id="32af5-182">**候補者の概要** で、必要に応じて候補者情報を入力または編集します。</span><span class="sxs-lookup"><span data-stu-id="32af5-182">Under **Candidate summary**, enter or edit the candidate information as necessary.</span></span>

6. <span data-ttu-id="32af5-183">**採用要求** で、候補者にリンクする採用要求を選択します。</span><span class="sxs-lookup"><span data-stu-id="32af5-183">Under **Recruiting request**, select a recruiting request to link the candidate to.</span></span> <span data-ttu-id="32af5-184">**開始予定日**、**採用マネージャー**、**職位**、**フィールド説明** に適当な情報を入力します。</span><span class="sxs-lookup"><span data-stu-id="32af5-184">Then complete the **Estimated start date**, **Hiring manager**, **Position**, and **Description fields** as appropriate.</span></span>

   ![採用要求へのリンク](./media/hr-recruit-10-link-to-recruiting-request.png)

7. <span data-ttu-id="32af5-186">候補者のレコードに含める次の領域のすべての情報を入力します。</span><span class="sxs-lookup"><span data-stu-id="32af5-186">Complete all the information in the following areas that you want to include in the candidate's record:</span></span>
   - <span data-ttu-id="32af5-187">**備考**</span><span class="sxs-lookup"><span data-stu-id="32af5-187">**Comments**</span></span>
   - <span data-ttu-id="32af5-188">**職務経験**</span><span class="sxs-lookup"><span data-stu-id="32af5-188">**Professional experience**</span></span>
   - <span data-ttu-id="32af5-189">**連絡先情報**</span><span class="sxs-lookup"><span data-stu-id="32af5-189">**Contact information**</span></span>
   - <span data-ttu-id="32af5-190">**教育**</span><span class="sxs-lookup"><span data-stu-id="32af5-190">**Education**</span></span>
   - <span data-ttu-id="32af5-191">**スキル**</span><span class="sxs-lookup"><span data-stu-id="32af5-191">**Skills**</span></span>
   - <span data-ttu-id="32af5-192">**証明書**</span><span class="sxs-lookup"><span data-stu-id="32af5-192">**Certificates**</span></span>
   - <span data-ttu-id="32af5-193">**審査**</span><span class="sxs-lookup"><span data-stu-id="32af5-193">**Screenings**</span></span>

8. <span data-ttu-id="32af5-194">**保存** を選択します。</span><span class="sxs-lookup"><span data-stu-id="32af5-194">Select **Save**.</span></span>

## <a name="hire-a-candidate"></a><span data-ttu-id="32af5-195">候補者の採用</span><span class="sxs-lookup"><span data-stu-id="32af5-195">Hire a candidate</span></span>

<span data-ttu-id="32af5-196">候補者を採用する準備ができたら、次の手順に従って採用者から従業員へ移行します。</span><span class="sxs-lookup"><span data-stu-id="32af5-196">When you're ready to hire a candidate, follow this procedure to transition the candidate to an employee.</span></span>

1. <span data-ttu-id="32af5-197">候補者フォームで、**採用** を選択します。</span><span class="sxs-lookup"><span data-stu-id="32af5-197">On the candidate form, select **Hire**.</span></span>

   ![候補者の採用](./media/hr-recruit-11-hire.png)

2. <span data-ttu-id="32af5-199">**新規採用** フォームにある **詳細** で、すべてのフィールドに入力します。</span><span class="sxs-lookup"><span data-stu-id="32af5-199">On the **Hire new worker** form, under **Details**, complete all the fields.</span></span>

   ![新入社員の詳細の入力](./media/hr-recruit-12-hire-new-worker.png)

3. <span data-ttu-id="32af5-201">**職位の詳細** で、必要に応じて情報を確認および変更します。</span><span class="sxs-lookup"><span data-stu-id="32af5-201">Under **Position details**, verify and change information as necessary.</span></span>

4. <span data-ttu-id="32af5-202">**オンボード チェックリスト** で、この従業員に関連するオンボード チェックリストを選択します。</span><span class="sxs-lookup"><span data-stu-id="32af5-202">Under **Onboarding checklists**, select the relevant onboarding checklists for this employee.</span></span>

5. <span data-ttu-id="32af5-203">**続行** を選択して従業員レコードを作成します。</span><span class="sxs-lookup"><span data-stu-id="32af5-203">Select **Continue** to create the employee record.</span></span>

   >[!NOTE]
   ><span data-ttu-id="32af5-204">組織のワークフローによっては、候補者レコードが従業員レコードに移行する前に他の承認ステップが必要な場合があります。</span><span class="sxs-lookup"><span data-stu-id="32af5-204">Depending on your organization's workflows, the candidate record may go through additional approval steps before becoming an employee record.</span></span>

## <a name="decide-not-to-hire-a-candidate"></a><span data-ttu-id="32af5-205">候補者の不採用</span><span class="sxs-lookup"><span data-stu-id="32af5-205">Decide not to hire a candidate</span></span>

<span data-ttu-id="32af5-206">候補者を採用しない場合は、次の手順に従って、候補者を審査プロセスから削除します。</span><span class="sxs-lookup"><span data-stu-id="32af5-206">If you decide not to hire a candidate, follow this procedure to remove them from the vetting process.</span></span> 

1. <span data-ttu-id="32af5-207">候補者フォームで、**不採用** を選択します。</span><span class="sxs-lookup"><span data-stu-id="32af5-207">On the candidate form, select **Do not hire**.</span></span>

   ![候補者の不採用](./media/hr-recruit-13-do-not-hire.png)

2. <span data-ttu-id="32af5-209">**理由コード** を選択し、コメントを記入します。</span><span class="sxs-lookup"><span data-stu-id="32af5-209">Select a **Reason code** and include any comments.</span></span>

3. <span data-ttu-id="32af5-210">**OK** を選択します。</span><span class="sxs-lookup"><span data-stu-id="32af5-210">Select **OK**.</span></span>

## <a name="dismiss-a-candidate"></a><span data-ttu-id="32af5-211">候補の消去</span><span class="sxs-lookup"><span data-stu-id="32af5-211">Dismiss a candidate</span></span>

<span data-ttu-id="32af5-212">必要に応じて、採用後に候補を消去することができます。</span><span class="sxs-lookup"><span data-stu-id="32af5-212">If needed, you can dismiss a candidate after hiring them.</span></span> <span data-ttu-id="32af5-213">たとえば、候補者が採用を拒否したり、初日に出勤しなかったりする場合です。</span><span class="sxs-lookup"><span data-stu-id="32af5-213">For example, a candidate might reject your offer or not show up on their first day.</span></span>

- <span data-ttu-id="32af5-214">候補者フォームで、**候補を消去** を選択します。</span><span class="sxs-lookup"><span data-stu-id="32af5-214">On the candidate form, select **Dismiss candidate**.</span></span>

  ![候補の消去](./media/hr-recruit-14-dismiss-candidate.png)

## <a name="see-also"></a><span data-ttu-id="32af5-216">参照</span><span class="sxs-lookup"><span data-stu-id="32af5-216">See also</span></span>

[<span data-ttu-id="32af5-217">構成 Dataverse 仮想テーブル</span><span class="sxs-lookup"><span data-stu-id="32af5-217">Configure Dataverse virtual tables</span></span>](hr-admin-integration-common-data-service-virtual-entities.md)<br>
[<span data-ttu-id="32af5-218">従業員の編成</span><span class="sxs-lookup"><span data-stu-id="32af5-218">Organize your workforce</span></span>](hr-personnel-departments-jobs-positions.md)<br>
[<span data-ttu-id="32af5-219">職務のコンポーネントの設定</span><span class="sxs-lookup"><span data-stu-id="32af5-219">Set up the components of a job</span></span>](hr-personnel-jobs.md)
