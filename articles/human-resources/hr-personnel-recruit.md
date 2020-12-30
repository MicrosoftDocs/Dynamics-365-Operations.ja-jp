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
ms.openlocfilehash: 9a35abcb8a2f6aa8031c8d84a44c2a8ad93883ac
ms.sourcegitcommit: 0354ca7e566fbd2eb0aabdd40000d4ac5c44ea78
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 12/04/2020
ms.locfileid: "4669177"
---
# <a name="recruit-job-candidates"></a><span data-ttu-id="a2786-103">職務候補者の採用</span><span class="sxs-lookup"><span data-stu-id="a2786-103">Recruit job candidates</span></span>

[!include [banner](includes/preview-feature.md)]

<span data-ttu-id="a2786-104">Dynamics 365 Human Resources を使用すると、採用要求の管理が簡単になります。</span><span class="sxs-lookup"><span data-stu-id="a2786-104">Dynamics 365 Human Resources helps you to manage recruiting requests.</span></span> <span data-ttu-id="a2786-105">また、職務の候補者が従業員になるまでの移行をシームレスに実行することもできます。</span><span class="sxs-lookup"><span data-stu-id="a2786-105">It also helps you seamlessly transition job candidates to employees.</span></span> <span data-ttu-id="a2786-106">組織で別の採用アプリケーションを使用している場合、採用プロセスには次の手順が含まれる場合があります。</span><span class="sxs-lookup"><span data-stu-id="a2786-106">If your organization uses a separate recruiting application, your recruiting process might include the following steps:</span></span>

- <span data-ttu-id="a2786-107">採用要求を Human Resources に入力する。</span><span class="sxs-lookup"><span data-stu-id="a2786-107">Enter your recruiting request in Human Resources.</span></span>
- <span data-ttu-id="a2786-108">採用アプリケーションから候補者の推薦状を Human Resources で受け取る。</span><span class="sxs-lookup"><span data-stu-id="a2786-108">Receive candidate referrals in Human Resources from the recruiting application.</span></span>
- <span data-ttu-id="a2786-109">Human Resources で候補者の承認プロセスを完了する。</span><span class="sxs-lookup"><span data-stu-id="a2786-109">Complete the candidate approval process in Human Resources.</span></span>

<span data-ttu-id="a2786-110">別の採用アプリケーションを使用していない場合は、Human Resources で手動で候補者を管理することもできます。</span><span class="sxs-lookup"><span data-stu-id="a2786-110">If you aren't using a separate recruiting application, you can also manually manage candidates in Human Resources.</span></span>

>[!NOTE]
><span data-ttu-id="a2786-111">管理者または開発者が Human Resources とサードパーティの採用アプリケーションを統合する場合は、[Common Data Service 統合の構成](hr-admin-integration-common-data-service.md) および [Common Data Service 仮想エンティティの構成](hr-admin-integration-common-data-service-virtual-entities.md) を参照してください</span><span class="sxs-lookup"><span data-stu-id="a2786-111">If you're an admin or developer and want to integrate Human Resources with a third-party recruiting application, see [Configure Common Data Service integration](hr-admin-integration-common-data-service.md) and [Configure Common Data Service virtual entities](hr-admin-integration-common-data-service-virtual-entities.md)</span></span>
>
> <span data-ttu-id="a2786-112">[AppSource](https://appsource.microsoft.com/marketplace/apps?search=recruiting%20dynamics) からも採用統合アプリを利用できます。</span><span class="sxs-lookup"><span data-stu-id="a2786-112">You can also find recruiting integration apps on [AppSource](https://appsource.microsoft.com/marketplace/apps?search=recruiting%20dynamics).</span></span>
>
> <span data-ttu-id="a2786-113">LinkedIn Talent Hub との統合で使用するプレビュー機能を試すには、[LinkedIn Talent Hub との統合](hr-admin-integration-linkedin.md)を参照してください。</span><span class="sxs-lookup"><span data-stu-id="a2786-113">To try out our preview feature for integrating with LinkedIn Talent Hub, see [Integrate with LinkedIn Talent Hub](hr-admin-integration-linkedin.md).</span></span>

## <a name="enable-recruiting-requests"></a><span data-ttu-id="a2786-114">採用要求を有効にする</span><span class="sxs-lookup"><span data-stu-id="a2786-114">Enable recruiting requests</span></span>

<span data-ttu-id="a2786-115">Human Resources に採用要求を送信する場合は、まず **人事管理パラメーター** で機能を有効にする必要があります。</span><span class="sxs-lookup"><span data-stu-id="a2786-115">If you want to submit recruiting requests in Human Resources, you must first enable the functionality in **Human resources parameters**.</span></span>

1. <span data-ttu-id="a2786-116">**人事管理** ワークスペースで、**リンク** を選択します。</span><span class="sxs-lookup"><span data-stu-id="a2786-116">In the **Personnel management** workspace, select **Links**.</span></span>

2. <span data-ttu-id="a2786-117">**設定** で、**人事管理パラメーター** を選択します。</span><span class="sxs-lookup"><span data-stu-id="a2786-117">Under **Setup**, select **Human resources parameters**.</span></span>

3. <span data-ttu-id="a2786-118">**一般** タブで、**採用** から **採用要求の有効化** を **はい** に設定します。</span><span class="sxs-lookup"><span data-stu-id="a2786-118">On the **General** tab, under **RECRUITING**, set **Enable recruiting requests** to **Yes**.</span></span>

   ![採用要求を有効にする](./media/hr-recruit-0-enable-requests.png)

## <a name="add-a-recruiting-request-location"></a><span data-ttu-id="a2786-120">採用要求の勤務場所の追加</span><span class="sxs-lookup"><span data-stu-id="a2786-120">Add a recruiting request location</span></span>

<span data-ttu-id="a2786-121">組織に勤務場所が複数ある場合は、勤務場所を追加して、要求者が新しい採用がある勤務場所を選択できるようにできます。</span><span class="sxs-lookup"><span data-stu-id="a2786-121">If your organization has multiple locations, you can add them so requestors can select a location where the new recruit will be working.</span></span> <span data-ttu-id="a2786-122">勤務場所は求人情報に記載されます。</span><span class="sxs-lookup"><span data-stu-id="a2786-122">The location will be included in the job posting.</span></span>

1. <span data-ttu-id="a2786-123">検索バーで **採用要求の勤務場所** を入力します。</span><span class="sxs-lookup"><span data-stu-id="a2786-123">In the search bar, enter **recruiting request location**.</span></span>

2. <span data-ttu-id="a2786-124">**新規** を選択します。</span><span class="sxs-lookup"><span data-stu-id="a2786-124">Select **New**.</span></span>

3. <span data-ttu-id="a2786-125">**採用要求の勤務場所** フィールドに、勤務場所の名前を入力します。</span><span class="sxs-lookup"><span data-stu-id="a2786-125">In the **Recruiting request location** field, enter the location name.</span></span>

   ![採用要求の勤務場所の追加](./media/hr-recruit-0a-add-location.png)

4. <span data-ttu-id="a2786-127">**説明** フィールドに、勤務場所の説明を入力します。</span><span class="sxs-lookup"><span data-stu-id="a2786-127">In the **Description**, enter a description for the location.</span></span>

5. <span data-ttu-id="a2786-128">**勤務場所** で、**追加** を選択します。</span><span class="sxs-lookup"><span data-stu-id="a2786-128">Under **Location**, select **Add**.</span></span> <span data-ttu-id="a2786-129">**新しい住所** と表示された場合は、その勤務場所の住所を入力します。</span><span class="sxs-lookup"><span data-stu-id="a2786-129">If the **New address** popout appears, enter the address for the location.</span></span>

   ![住所の入力](./media/hr-recruit-0b-address.png)

6. <span data-ttu-id="a2786-131">**連絡先情報** で、勤務場所の連絡先の情報を入力します。</span><span class="sxs-lookup"><span data-stu-id="a2786-131">Under **Contact information**, enter the information for the location's contact.</span></span>

7. <span data-ttu-id="a2786-132">**保存** を選択します。</span><span class="sxs-lookup"><span data-stu-id="a2786-132">Select **Save**.</span></span>

## <a name="add-a-recruiting-request"></a><span data-ttu-id="a2786-133">採用要求の追加</span><span class="sxs-lookup"><span data-stu-id="a2786-133">Add a recruiting request</span></span>

<span data-ttu-id="a2786-134">管理者は、Human Resources に採用要求を送信できます。</span><span class="sxs-lookup"><span data-stu-id="a2786-134">Managers can submit recruiting requests in Human Resources.</span></span> <span data-ttu-id="a2786-135">別の採用アプリケーションを使用する場合は、これらの手順を完了すると採用要求が送信され、そのアプリケーションで採用プロセスが開始されます。</span><span class="sxs-lookup"><span data-stu-id="a2786-135">If you use a separate recruiting application, completing these steps will send a recruiting request and start the recruiting process in that application.</span></span> <span data-ttu-id="a2786-136">それ以外の場合は、この手順を実行して、社内採用プロセスのワークフローを開始します。</span><span class="sxs-lookup"><span data-stu-id="a2786-136">Otherwise, complete this procedure to begin the workflow for your own internal recruiting process.</span></span>

1. <span data-ttu-id="a2786-137">**従業員セルフ サービス** を選択します。</span><span class="sxs-lookup"><span data-stu-id="a2786-137">Select **Employee self service**.</span></span>

2. <span data-ttu-id="a2786-138">**自分のチーム** タブを選択します。</span><span class="sxs-lookup"><span data-stu-id="a2786-138">Select the **My team** tab.</span></span>

3. <span data-ttu-id="a2786-139">**採用を要求** を選択します。</span><span class="sxs-lookup"><span data-stu-id="a2786-139">Select  **Request to recruit**.</span></span>

   ![採用要求の開始](./media/hr-recruit-1-request-to-recruit.png)

4. <span data-ttu-id="a2786-141">**説明**、**職務**、および **予想開始日** フィールドに入力します。</span><span class="sxs-lookup"><span data-stu-id="a2786-141">Complete the **Description**, **Job**, and **Estimated start date** fields.</span></span>

   ![採用要求の完了](./media/hr-recruit-2-request-to-recruit.png)

5. <span data-ttu-id="a2786-143">**続行** を選択します。</span><span class="sxs-lookup"><span data-stu-id="a2786-143">Select **Continue**.</span></span> <span data-ttu-id="a2786-144">希望する職務の採用要求が表示されます。</span><span class="sxs-lookup"><span data-stu-id="a2786-144">The recruiting request for your position appears.</span></span>

6. <span data-ttu-id="a2786-145">**一般** で、**採用担当者** ドロップダウンから採用担当者を選択し、**採用要求の勤務場所** ドロップダウンから勤務場所を選択します。</span><span class="sxs-lookup"><span data-stu-id="a2786-145">Under **General**, select a recruiter from the **Recruiter** dropdown, and then select a location from the **Recruiting request location** dropdown.</span></span>

7. <span data-ttu-id="a2786-146">**職務** で、必要に応じて情報を変更し、**職務から詳細を作成** を選択します。</span><span class="sxs-lookup"><span data-stu-id="a2786-146">Under **Job**, change any information as needed, and then select **Create details from job**.</span></span>

   ![職務から詳細を作成](./media/hr-recruit-3-create-details-from-job.png)

   <span data-ttu-id="a2786-148">採用要求の残りの部分には、入力した職務の既定の情報が入力されます。</span><span class="sxs-lookup"><span data-stu-id="a2786-148">The rest of the recruiting request will populate with the default information for the job you entered.</span></span>

8. <span data-ttu-id="a2786-149">**外部説明** で、外部向け職務明細書を入力します。</span><span class="sxs-lookup"><span data-stu-id="a2786-149">Under **External description**, enter an external-facing job description.</span></span>

9. <span data-ttu-id="a2786-150">**職位** で **追加** を選択してから、この採用要求の職位を選択します。</span><span class="sxs-lookup"><span data-stu-id="a2786-150">Under **Positions**, select **Add**, and then select a position for this recruiting request.</span></span>

   ![職位の追加](./media/hr-recruit-4-select-position.png)

10. <span data-ttu-id="a2786-152">**スキル** で **追加** を選択してからスキルを選択します。</span><span class="sxs-lookup"><span data-stu-id="a2786-152">Under **Skills**, select **Add**, and then select a skill.</span></span>

11. <span data-ttu-id="a2786-153">**学歴要件** で **追加** を選択してから、**学歴** および **最終学歴** ドロップダウンから学歴を選択します。</span><span class="sxs-lookup"><span data-stu-id="a2786-153">Under **Educational requirements**, select **Add**, and then select values from the **Education** and **Level of education** dropdowns.</span></span>

   ![学歴要件の追加](./media/hr-recruit-5-select-educational-requirements.png)

12. <span data-ttu-id="a2786-155">**コメント** で、必要に応じてコメントを追加します。</span><span class="sxs-lookup"><span data-stu-id="a2786-155">Under **Comment**, add comments as necessary.</span></span>

13. <span data-ttu-id="a2786-156">**報酬** で **レベル** からレベルを選択してから、必要に応じて **低しきい値**、**制御ポイント**、**高しきい値** を調整します。</span><span class="sxs-lookup"><span data-stu-id="a2786-156">Under **Compensation**, select a level from the **Level** dropdown, and then adjust **Low threshold**, **Control point**, and **High threshold** as necessary.</span></span>

14. <span data-ttu-id="a2786-157">採用要求が完了し採用プロセスを開始する準備ができたら、メニュー バーの **有効化** を選択します。</span><span class="sxs-lookup"><span data-stu-id="a2786-157">When your recruiting request is complete and you're ready to start the recruiting process, select **Activate** in the menu bar.</span></span>

   ![採用要求の有効化](./media/hr-recruit-6-activate-recruit-request.png)

15. <span data-ttu-id="a2786-159">**保存** を選択します。</span><span class="sxs-lookup"><span data-stu-id="a2786-159">Select **Save**.</span></span>

## <a name="view-and-edit-your-recruiting-requests"></a><span data-ttu-id="a2786-160">採用要求の表示と編集</span><span class="sxs-lookup"><span data-stu-id="a2786-160">View and edit your recruiting requests</span></span>

<span data-ttu-id="a2786-161">マネージャーに要求を表示する場合は、次の操作を行います。</span><span class="sxs-lookup"><span data-stu-id="a2786-161">If you're a manager and want to view your own requests:</span></span>

1. <span data-ttu-id="a2786-162">**従業員セルフ サービス** を選択します。</span><span class="sxs-lookup"><span data-stu-id="a2786-162">Select **Employee self service**.</span></span>

2. <span data-ttu-id="a2786-163">**自分のチーム** タブを選択します。</span><span class="sxs-lookup"><span data-stu-id="a2786-163">Select the **My team** tab.</span></span>

3. <span data-ttu-id="a2786-164">**自分のチームの情報** で、**採用要求** タブを選択します。</span><span class="sxs-lookup"><span data-stu-id="a2786-164">Under **My team information**, select the **Recruiting requests** tab.</span></span>

   ![[採用要求] タブの選択](./media/hr-recruit-7-recruiting-requests.png)

4. <span data-ttu-id="a2786-166">採用要求を表示または編集するには、グリッドで選択します。</span><span class="sxs-lookup"><span data-stu-id="a2786-166">To view or edit a recruiting request, select it in the grid.</span></span>

<span data-ttu-id="a2786-167">HR のプロフェッショナルにすべての採用要求を表示するには、次の操作を行います。</span><span class="sxs-lookup"><span data-stu-id="a2786-167">If you're an HR pro and want to view all recruiting requests:</span></span>

1. <span data-ttu-id="a2786-168">**人事管理** を選択する。</span><span class="sxs-lookup"><span data-stu-id="a2786-168">Select **Personnel management**.</span></span>

2. <span data-ttu-id="a2786-169">**採用要求** を選択する。</span><span class="sxs-lookup"><span data-stu-id="a2786-169">Select **Recruiting requests**.</span></span>

   ![人事管理で採用要求を表示する](./media/hr-recruit-8-recruiting-requests-personnel-management.png)

3. <span data-ttu-id="a2786-171">採用要求を表示または編集するには、グリッドで選択します。</span><span class="sxs-lookup"><span data-stu-id="a2786-171">To view or edit a recruiting request, select it in the grid.</span></span>

## <a name="add-or-edit-a-candidate-profile"></a><span data-ttu-id="a2786-172">候補者プロファイルの追加または編集</span><span class="sxs-lookup"><span data-stu-id="a2786-172">Add or edit a candidate profile</span></span>

<span data-ttu-id="a2786-173">採用要求を管理するために組織が別のアプリケーションと統合している場合、採用要求はそのアプリケーションに転送されます。</span><span class="sxs-lookup"><span data-stu-id="a2786-173">If your organization has integrated with another application to manage recruiting requests, recruiting requests are forwarded to that application.</span></span> <span data-ttu-id="a2786-174">その後、採用アプリケーションが候補者の情報を Human Resources に送り返します。</span><span class="sxs-lookup"><span data-stu-id="a2786-174">The recruiting application then sends candidate information back to Human Resources.</span></span> <span data-ttu-id="a2786-175">それ以外の場合は、独自の内部採用プロセスに従って、候補者の情報を手動で入力できます。</span><span class="sxs-lookup"><span data-stu-id="a2786-175">Otherwise, you can follow your own internal recruiting processes and enter candidate information manually.</span></span>

1. <span data-ttu-id="a2786-176">**人事管理** を選択する。</span><span class="sxs-lookup"><span data-stu-id="a2786-176">Select **Personnel management**.</span></span>

2. <span data-ttu-id="a2786-177">**リンク** を選択します。</span><span class="sxs-lookup"><span data-stu-id="a2786-177">Select **Links**.</span></span>

3. <span data-ttu-id="a2786-178">**採用** で **候補者** を選択します。</span><span class="sxs-lookup"><span data-stu-id="a2786-178">Under **Recruiting**, select **Candidates**.</span></span>

   ![候補者の表示](./media/hr-recruit-9-candidates.png)

4. <span data-ttu-id="a2786-180">候補者を追加するには、**新規** を選択します。</span><span class="sxs-lookup"><span data-stu-id="a2786-180">To add a candidate, select **New**.</span></span> <span data-ttu-id="a2786-181">既存の候補者を編集するには、リストから候補者を選択し、**編集** を選択します。</span><span class="sxs-lookup"><span data-stu-id="a2786-181">To edit an existing candidate, select the candidate from the list and then select **Edit**.</span></span> <span data-ttu-id="a2786-182">候補者のプロファイルが表示されます。</span><span class="sxs-lookup"><span data-stu-id="a2786-182">The candidate profile appears.</span></span>

5. <span data-ttu-id="a2786-183">**候補者の概要** で、必要に応じて候補者情報を入力または編集します。</span><span class="sxs-lookup"><span data-stu-id="a2786-183">Under **Candidate summary**, enter or edit the candidate information as necessary.</span></span>

6. <span data-ttu-id="a2786-184">**採用要求** で、候補者にリンクする採用要求を選択します。</span><span class="sxs-lookup"><span data-stu-id="a2786-184">Under **Recruiting request**, select a recruiting request to link the candidate to.</span></span> <span data-ttu-id="a2786-185">**開始予定日**、**採用マネージャー**、**職位**、**フィールド説明** に適当な情報を入力します。</span><span class="sxs-lookup"><span data-stu-id="a2786-185">Then complete the **Estimated start date**, **Hiring manager**, **Position**, and **Description fields** as appropriate.</span></span>

   ![採用要求へのリンク](./media/hr-recruit-10-link-to-recruiting-request.png)

7. <span data-ttu-id="a2786-187">候補者のレコードに含める次の領域のすべての情報を入力します。</span><span class="sxs-lookup"><span data-stu-id="a2786-187">Complete all the information in the following areas that you want to include in the candidate's record:</span></span>
   - <span data-ttu-id="a2786-188">**備考**</span><span class="sxs-lookup"><span data-stu-id="a2786-188">**Comments**</span></span>
   - <span data-ttu-id="a2786-189">**職務経験**</span><span class="sxs-lookup"><span data-stu-id="a2786-189">**Professional experience**</span></span>
   - <span data-ttu-id="a2786-190">**連絡先情報**</span><span class="sxs-lookup"><span data-stu-id="a2786-190">**Contact information**</span></span>
   - <span data-ttu-id="a2786-191">**教育**</span><span class="sxs-lookup"><span data-stu-id="a2786-191">**Education**</span></span>
   - <span data-ttu-id="a2786-192">**スキル**</span><span class="sxs-lookup"><span data-stu-id="a2786-192">**Skills**</span></span>
   - <span data-ttu-id="a2786-193">**証明書**</span><span class="sxs-lookup"><span data-stu-id="a2786-193">**Certificates**</span></span>
   - <span data-ttu-id="a2786-194">**審査**</span><span class="sxs-lookup"><span data-stu-id="a2786-194">**Screenings**</span></span>

8. <span data-ttu-id="a2786-195">**保存** を選択します。</span><span class="sxs-lookup"><span data-stu-id="a2786-195">Select **Save**.</span></span>

## <a name="hire-a-candidate"></a><span data-ttu-id="a2786-196">候補者の採用</span><span class="sxs-lookup"><span data-stu-id="a2786-196">Hire a candidate</span></span>

<span data-ttu-id="a2786-197">候補者を採用する準備ができたら、次の手順に従って採用者から従業員へ移行します。</span><span class="sxs-lookup"><span data-stu-id="a2786-197">When you're ready to hire a candidate, follow this procedure to transition the candidate to an employee.</span></span>

1. <span data-ttu-id="a2786-198">候補者フォームで、**採用** を選択します。</span><span class="sxs-lookup"><span data-stu-id="a2786-198">On the candidate form, select **Hire**.</span></span>

   ![候補者の採用](./media/hr-recruit-11-hire.png)

2. <span data-ttu-id="a2786-200">**新規採用** フォームにある **詳細** で、すべてのフィールドに入力します。</span><span class="sxs-lookup"><span data-stu-id="a2786-200">On the **Hire new worker** form, under **Details**, complete all the fields.</span></span>

   ![新入社員の詳細の入力](./media/hr-recruit-12-hire-new-worker.png)

3. <span data-ttu-id="a2786-202">**職位の詳細** で、必要に応じて情報を確認および変更します。</span><span class="sxs-lookup"><span data-stu-id="a2786-202">Under **Position details**, verify and change information as necessary.</span></span>

4. <span data-ttu-id="a2786-203">**オンボード チェックリスト** で、この従業員に関連するオンボード チェックリストを選択します。</span><span class="sxs-lookup"><span data-stu-id="a2786-203">Under **Onboarding checklists**, select the relevant onboarding checklists for this employee.</span></span>

5. <span data-ttu-id="a2786-204">**続行** を選択して従業員レコードを作成します。</span><span class="sxs-lookup"><span data-stu-id="a2786-204">Select **Continue** to create the employee record.</span></span>

   >[!NOTE]
   ><span data-ttu-id="a2786-205">組織のワークフローによっては、候補者レコードが従業員レコードに移行する前に他の承認ステップが必要な場合があります。</span><span class="sxs-lookup"><span data-stu-id="a2786-205">Depending on your organization's workflows, the candidate record may go through additional approval steps before becoming an employee record.</span></span>

## <a name="decide-not-to-hire-a-candidate"></a><span data-ttu-id="a2786-206">候補者の不採用</span><span class="sxs-lookup"><span data-stu-id="a2786-206">Decide not to hire a candidate</span></span>

<span data-ttu-id="a2786-207">候補者を採用しない場合は、次の手順に従って、候補者を審査プロセスから削除します。</span><span class="sxs-lookup"><span data-stu-id="a2786-207">If you decide not to hire a candidate, follow this procedure to remove them from the vetting process.</span></span> 

1. <span data-ttu-id="a2786-208">候補者フォームで、**不採用** を選択します。</span><span class="sxs-lookup"><span data-stu-id="a2786-208">On the candidate form, select **Do not hire**.</span></span>

   ![候補者の不採用](./media/hr-recruit-13-do-not-hire.png)

2. <span data-ttu-id="a2786-210">**理由コード** を選択し、コメントを記入します。</span><span class="sxs-lookup"><span data-stu-id="a2786-210">Select a **Reason code** and include any comments.</span></span>

3. <span data-ttu-id="a2786-211">**OK** を選択します。</span><span class="sxs-lookup"><span data-stu-id="a2786-211">Select **OK**.</span></span>

## <a name="dismiss-a-candidate"></a><span data-ttu-id="a2786-212">候補の消去</span><span class="sxs-lookup"><span data-stu-id="a2786-212">Dismiss a candidate</span></span>

<span data-ttu-id="a2786-213">必要に応じて、採用後に候補を消去することができます。</span><span class="sxs-lookup"><span data-stu-id="a2786-213">If needed, you can dismiss a candidate after hiring them.</span></span> <span data-ttu-id="a2786-214">たとえば、候補者が採用を拒否したり、初日に出勤しなかったりする場合です。</span><span class="sxs-lookup"><span data-stu-id="a2786-214">For example, a candidate might reject your offer or not show up on their first day.</span></span>

- <span data-ttu-id="a2786-215">候補者フォームで、**候補を消去** を選択します。</span><span class="sxs-lookup"><span data-stu-id="a2786-215">On the candidate form, select **Dismiss candidate**.</span></span>

  ![候補の消去](./media/hr-recruit-14-dismiss-candidate.png)

## <a name="see-also"></a><span data-ttu-id="a2786-217">参照</span><span class="sxs-lookup"><span data-stu-id="a2786-217">See also</span></span>

[<span data-ttu-id="a2786-218">Common Data Service 仮想エンティティの構成</span><span class="sxs-lookup"><span data-stu-id="a2786-218">Configure Common Data Service virtual entities</span></span>](hr-admin-integration-common-data-service-virtual-entities.md)<br>
[<span data-ttu-id="a2786-219">従業員の編成</span><span class="sxs-lookup"><span data-stu-id="a2786-219">Organize your workforce</span></span>](hr-personnel-departments-jobs-positions.md)<br>
[<span data-ttu-id="a2786-220">職務のコンポーネントの設定</span><span class="sxs-lookup"><span data-stu-id="a2786-220">Set up the components of a job</span></span>](hr-personnel-jobs.md)