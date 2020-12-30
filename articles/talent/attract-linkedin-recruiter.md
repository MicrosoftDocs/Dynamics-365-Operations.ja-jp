---
title: Attract の LinkedIn Recruiter を使用した候補者のソーシング
description: Microsoft Dynamics 365 Talent - Attract が提供する LinkedIn 統合を使用して、LinkedIn Recruiter から職務候補者をソース化します。
author: andreabichsel
manager: AnnBe
ms.date: 08/31/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-talent
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Talent, Core
ms.custom: 7521
ms.assetid: 3b953d5f-6325-4c9e-8b9b-6ab0458a73f8
ms.search.region: Global
ms.search.industry: ''
ms.author: anbichse
ms.search.validFrom: 2018-10-15
ms.dyn365.ops.version: Talent October 2018 update
ms.openlocfilehash: 96e4660c4958bf5f2a0910bfad770e1e713f800f
ms.sourcegitcommit: e89bb3e5420a6ece84f4e80c11e360b4a042f59d
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 11/17/2020
ms.locfileid: "4528272"
---
# <a name="source-candidates-with-linkedin-recruiter-in-attract"></a><span data-ttu-id="5bcb2-103">Attract の LinkedIn Recruiter を使用した候補者のソーシング</span><span class="sxs-lookup"><span data-stu-id="5bcb2-103">Source candidates with LinkedIn Recruiter in Attract</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="5bcb2-104">LinkedIn は世界最大のオンライン プロフェッショナル ネットワークで、世界の最高の人材へのアクセスを提供します。</span><span class="sxs-lookup"><span data-stu-id="5bcb2-104">LinkedIn is the world's largest online professional network, giving you access to the world's top talent.</span></span> <span data-ttu-id="5bcb2-105">Microsoft Dynamics 365 Talent: Attract では LinkedIn から直接候補者をソース化できます。</span><span class="sxs-lookup"><span data-stu-id="5bcb2-105">Microsoft Dynamics 365 Talent: Attract lets you source candidates directly from LinkedIn.</span></span> <span data-ttu-id="5bcb2-106">したがって、空いている職位を埋めるために必要な人材を見つけるのはこれまで以上に簡単です。</span><span class="sxs-lookup"><span data-stu-id="5bcb2-106">Therefore, it's easier than ever to find the talent that you need to fill your open positions.</span></span> <span data-ttu-id="5bcb2-107">Attract を通じて LinkedIn との接続を設定した後、ワンクリックで職位の LinkedIn 候補者を表示し、Attract にエクスポートできます。</span><span class="sxs-lookup"><span data-stu-id="5bcb2-107">After you set up your connection with LinkedIn through Attract, you can view potential LinkedIn candidates for your positions and export them into Attract with just one click.</span></span>

<span data-ttu-id="5bcb2-108">この機能がないようであれば、管理者にお問い合わせください。Attract から LinkedIn Recruiter を利用する前に、管理者は [LinkedIn との統合を設定](./attract-admin-linkedin.md) する必要があります。</span><span class="sxs-lookup"><span data-stu-id="5bcb2-108">If you don't seem to have this capability, contact your admin. Before you can take advantage of LinkedIn Recruiter from Attract, your admin must [set up integration with LinkedIn](./attract-admin-linkedin.md).</span></span> <span data-ttu-id="5bcb2-109">その後、LinkedIn Recruiter との接続を設定し、候補者の検索を開始できます。</span><span class="sxs-lookup"><span data-stu-id="5bcb2-109">You can then set up your connection with LinkedIn Recruiter and start finding candidates.</span></span>

>[!IMPORTANT]
><span data-ttu-id="5bcb2-110">2020 年 7 月 1 日現在、LinkedIn は Internet Explorer 11 をサポートしていません。</span><span class="sxs-lookup"><span data-stu-id="5bcb2-110">As of July 1, 2020, LinkedIn no longer supports Internet Explorer 11.</span></span> <span data-ttu-id="5bcb2-111">ユーザーはまだ Internet Explorer 11 を使用して LinkedIn にアクセスできますが、アップグレードするか別のブラウザーを使用するかを確認するメッセージが表示されます。</span><span class="sxs-lookup"><span data-stu-id="5bcb2-111">Users can still access LinkedIn with Internet Explorer 11, but will be prompted to upgrade or use a different browser.</span></span> <span data-ttu-id="5bcb2-112">詳細については、[サポートされている LinkedIn 用インターネット ブラウザー](https://www.linkedin.com/help/linkedin/answer/4135/supported-internet-browsers-for-linkedin) を参照してください。</span><span class="sxs-lookup"><span data-stu-id="5bcb2-112">For more information, see [Supported Internet Browsers for LinkedIn](https://www.linkedin.com/help/linkedin/answer/4135/supported-internet-browsers-for-linkedin).</span></span>

## <a name="set-up-your-connection-with-linkedin-recruiter"></a><span data-ttu-id="5bcb2-113">LinkedIn Recruiter との接続の設定</span><span class="sxs-lookup"><span data-stu-id="5bcb2-113">Set up your connection with LinkedIn Recruiter</span></span>

<span data-ttu-id="5bcb2-114">Attract を通じて LinkedIn Recruiter で作業を開始する前に、LinkedIn Recruiter との接続を設定する必要があります。</span><span class="sxs-lookup"><span data-stu-id="5bcb2-114">Before you can start working with LinkedIn Recruiter through Attract, you must set up your connection with LinkedIn Recruiter.</span></span> <span data-ttu-id="5bcb2-115">このステップでは、LinkedIn Recruiter の資格情報が必要です。</span><span class="sxs-lookup"><span data-stu-id="5bcb2-115">For this step, you need your LinkedIn Recruiter credentials.</span></span>

1. <span data-ttu-id="5bcb2-116">ページの右上隅にある **設定** ボタン (ギア アイコン) を選択します。</span><span class="sxs-lookup"><span data-stu-id="5bcb2-116">Select the **Settings** button (gear icon) in the upper-right corner of the page.</span></span>
2. <span data-ttu-id="5bcb2-117">**ユーザー設定** を選択します。</span><span class="sxs-lookup"><span data-stu-id="5bcb2-117">Select **User settings**.</span></span>
3. <span data-ttu-id="5bcb2-118">**接続** タブで、**LinkedIn** の横にある **接続** を選択します。</span><span class="sxs-lookup"><span data-stu-id="5bcb2-118">On the **Connections** tab, select **Connect** next to **LinkedIn**.</span></span> <span data-ttu-id="5bcb2-119">LinkedIn が提供する指示に従ってください。</span><span class="sxs-lookup"><span data-stu-id="5bcb2-119">Follow the instructions that are provided by LinkedIn.</span></span>

    ![[<span data-ttu-id="5bcb2-120">Attract から LinkedIn Recruiter への接続の設定</span><span class="sxs-lookup"><span data-stu-id="5bcb2-120">Set up connection to LinkedIn Recruiter from Attract</span></span>](./media/attract-set-up-linkedin-recruiter-connection.png)](./media/attract-set-up-linkedin-recruiter-connection.png)

## <a name="view-linkedin-candidates-in-attract"></a><span data-ttu-id="5bcb2-121">LinkedIn の候補者を Attract で表示する</span><span class="sxs-lookup"><span data-stu-id="5bcb2-121">View LinkedIn candidates in Attract</span></span>

<span data-ttu-id="5bcb2-122">LinkedIn Recruiter に接続すると、候補者の LinkedIn プロファイルを Attract で表示できます。</span><span class="sxs-lookup"><span data-stu-id="5bcb2-122">After you're connected to LinkedIn Recruiter, you can view candidates' LinkedIn profiles in Attract.</span></span>

>[!NOTE]
><span data-ttu-id="5bcb2-123">採用者のシートが割り当てられている場合は、完全な情報を閲覧することができます。</span><span class="sxs-lookup"><span data-stu-id="5bcb2-123">If you have a Recruiter seat assigned to you, you can see the candidates' full information.</span></span><br><br>
><span data-ttu-id="5bcb2-124">採用マネージャーのシートを所有している場合や、何もシートが割り当てられていない場合は、Attract で候補者の LinkedIn タブに移動する前に必ず LinkedIn または LinkedIn Recruiter からサインアウトしてください。</span><span class="sxs-lookup"><span data-stu-id="5bcb2-124">If you have a Hiring Manager seat or no seat assigned to you, be sure to sign out of LinkedIn or LinkedIn Recruiter before navigating to the LinkedIn tab for a candidate in Attract.</span></span> <span data-ttu-id="5bcb2-125">候補者の基本のパブリック プロファイル データ (姓、名など) を確認できるようになります。</span><span class="sxs-lookup"><span data-stu-id="5bcb2-125">You'll be able to see the candidate's basic public profile data, such as their first and last name.</span></span>

1. <span data-ttu-id="5bcb2-126">Attract で、左側にある **職務** または **人材プール** を選択してから、申請者を選択します。</span><span class="sxs-lookup"><span data-stu-id="5bcb2-126">In Attract, select **Jobs** or **Talent pools** on the left, and then select an applicant.</span></span>

    ![[<span data-ttu-id="5bcb2-127">LinkedIn の候補者を Attract で表示する</span><span class="sxs-lookup"><span data-stu-id="5bcb2-127">View LinkedIn candidates in Attract</span></span>](./media/attract-view-linkedin-candidates.png)](./media/attract-view-linkedin-candidates.png)

2. <span data-ttu-id="5bcb2-128">候補者のプロファイルで、**LinkedIn** タブを選択します。候補者のプロファイルと InMail 履歴を表示できます。</span><span class="sxs-lookup"><span data-stu-id="5bcb2-128">In the candidate's profile, select the **LinkedIn** tab. You can view the candidate's profile and InMail history.</span></span>

   ![候補者の LinkedIn 情報の表示](./media/attract-candidate-linkedin-tab.png)

<span data-ttu-id="5bcb2-130">ここでは、実行できるアクションは次のとおりです。</span><span class="sxs-lookup"><span data-stu-id="5bcb2-130">From here, you can perform the following actions:</span></span>

- <span data-ttu-id="5bcb2-131">**採用活動** タブを選択して、次の情報を表示します。</span><span class="sxs-lookup"><span data-stu-id="5bcb2-131">Select the **Recruiting activities** tab to view:</span></span>
   
   - <span data-ttu-id="5bcb2-132">採用担当者メモ (パブリックとプライベートの両方)。</span><span class="sxs-lookup"><span data-stu-id="5bcb2-132">Recruiter notes (both public and private).</span></span> <span data-ttu-id="5bcb2-133">既定では、メモはプライベートになり、メモの所有者にのみ表示されます。</span><span class="sxs-lookup"><span data-stu-id="5bcb2-133">By default, notes are private and only visible to the owner of the notes.</span></span>
   - <span data-ttu-id="5bcb2-134">InMail 活動 (InMail コンテンツは除く)。</span><span class="sxs-lookup"><span data-stu-id="5bcb2-134">InMail activity (but not the InMail content).</span></span> <span data-ttu-id="5bcb2-135">ページの下部までスクロールして、見込顧客との InMail のやり取りを表示し、見込顧客とやり取りしている組織内の他のユーザーを表示します。</span><span class="sxs-lookup"><span data-stu-id="5bcb2-135">Scroll to the bottom of the page to view the InMail exchange with your prospect and view other users in your organization who are interacting with your prospect.</span></span>
   - <span data-ttu-id="5bcb2-136">候補者の拒否活動</span><span class="sxs-lookup"><span data-stu-id="5bcb2-136">Candidate rejection activity</span></span>

- <span data-ttu-id="5bcb2-137">**InMail を送信** を選択して、Attract を離れずに InMail を送信します。</span><span class="sxs-lookup"><span data-stu-id="5bcb2-137">Select **Send InMail** to send InMail without having to leave Attract.</span></span>

- <span data-ttu-id="5bcb2-138">**ジョブに保存** を選択すると、Attract を離れずにジョブを保存することができます。</span><span class="sxs-lookup"><span data-stu-id="5bcb2-138">Select **Save to a job** to save the job without leaving Attract.</span></span>

> [!NOTE]
> <span data-ttu-id="5bcb2-139">候補者の Attract 情報が LinkedIn の情報と一致すると、候補者の LinkedIn プロファイルが Attract に表示されます。</span><span class="sxs-lookup"><span data-stu-id="5bcb2-139">A candidate's LinkedIn profile will display in Attract when the candidate's Attract information matches the LinkedIn information.</span></span> <span data-ttu-id="5bcb2-140">使用される照合ルールは次のとおりです。</span><span class="sxs-lookup"><span data-stu-id="5bcb2-140">Here are the matching rules that are used:</span></span>
> 
> 1. <span data-ttu-id="5bcb2-141">電子メール アドレスと LinkedIn メンバーID が Attract と LinkedIn で一致すると、候補者のプロファイルが表示されます。</span><span class="sxs-lookup"><span data-stu-id="5bcb2-141">If the email address and LinkedIn member ID match in Attract and LinkedIn, the candidate's profile is shown.</span></span> <span data-ttu-id="5bcb2-142">候補者は、LinkedIn プロファイルを Attract からリンクまたはリンク解除するオプションを引き続き使用できます。</span><span class="sxs-lookup"><span data-stu-id="5bcb2-142">Candidates still have the option to link or unlink their LinkedIn profile from Attract.</span></span>
> 2. <span data-ttu-id="5bcb2-143">電子メール アドレスまたは LinkedIn メンバー ID が一致しない場合は、可能性のある候補者の一覧が表示されます。</span><span class="sxs-lookup"><span data-stu-id="5bcb2-143">If the email address or LinkedIn member ID doesn't match, you see a list of possible candidates.</span></span> <span data-ttu-id="5bcb2-144">その後、リスト内の候補を選択し、プロファイルをリンクできます。</span><span class="sxs-lookup"><span data-stu-id="5bcb2-144">You can then select a candidate in the list and link the profile.</span></span>
> 3. <span data-ttu-id="5bcb2-145">良好な一致がない場合は、一致が見つからなかったことが通知されます。</span><span class="sxs-lookup"><span data-stu-id="5bcb2-145">If there are no good matches, you're notified that no match was found.</span></span>

## <a name="export-linkedin-candidates-to-attract-with-one-click"></a><span data-ttu-id="5bcb2-146">LinkedIn 候補者をワンクリックで Attract にエクスポートする</span><span class="sxs-lookup"><span data-stu-id="5bcb2-146">Export LinkedIn candidates to Attract with one click</span></span>

<span data-ttu-id="5bcb2-147">LinkedIn Recruiter で候補者を確認している間は、現在 Attract で開いている職務に候補者をエクスポートできます。</span><span class="sxs-lookup"><span data-stu-id="5bcb2-147">While you're reviewing candidates in LinkedIn Recruiter, you can export them to jobs that you currently have open in Attract.</span></span> <span data-ttu-id="5bcb2-148">このステップでは、Attract の採用担当者または採用マネージャーのアクセス許可が必要です。</span><span class="sxs-lookup"><span data-stu-id="5bcb2-148">For this step, you need Recruiter or Hiring Manager permissions in Attract.</span></span> <span data-ttu-id="5bcb2-149">Attract でのロールの詳細については、[Attract でのセキュリティおよびロールの管理](https://docs.microsoft.com/dynamics365/unified-operations/talent/security-attract) を参照してください。</span><span class="sxs-lookup"><span data-stu-id="5bcb2-149">For more information about roles in Attract, see [Security and role management in Attract](https://docs.microsoft.com/dynamics365/unified-operations/talent/security-attract).</span></span>

<span data-ttu-id="5bcb2-150">また、職務に候補者ステージがあることを確認する必要があります。</span><span class="sxs-lookup"><span data-stu-id="5bcb2-150">You must also make sure that the job has a Prospect stage.</span></span> <span data-ttu-id="5bcb2-151">詳細については、[候補者活動](./activities-attract.md#prospect-activity) を参照してください。</span><span class="sxs-lookup"><span data-stu-id="5bcb2-151">For more information, see [Prospect activity](./activities-attract.md#prospect-activity).</span></span>

1. <span data-ttu-id="5bcb2-152">Attract で職務を作成し、適切なロールを割り当てた後、職務をアクティブにします。</span><span class="sxs-lookup"><span data-stu-id="5bcb2-152">In Attract, create a job, assign the appropriate roles, and activate the job.</span></span>
2. <span data-ttu-id="5bcb2-153">LinkedIn Recruiter で、その職務に適した候補者を見つけ、候補者のプロファイルに移動します。</span><span class="sxs-lookup"><span data-stu-id="5bcb2-153">In LinkedIn Recruiter, find a good candidate for the job, and go to the candidate's profile.</span></span>
3. <span data-ttu-id="5bcb2-154">連絡先カードの職務検索ボックスで、タイトルまたは Attract で有効の職務 ID を使い職務を検索します。</span><span class="sxs-lookup"><span data-stu-id="5bcb2-154">In the job search box in the contact card, find the job by using the title or the Job ID that was activated in Attract.</span></span> <span data-ttu-id="5bcb2-155">職務が見つからない場合は、**変更 ATS** を選択して正しい Attract インスタンスを検索します。</span><span class="sxs-lookup"><span data-stu-id="5bcb2-155">If you can't find the job, select **Change ATS** to find the correct Attract instance.</span></span>
4. <span data-ttu-id="5bcb2-156">職務を選択してから、**エクスポート** を選択します。</span><span class="sxs-lookup"><span data-stu-id="5bcb2-156">Select the job, and then select **Export**.</span></span>
5. <span data-ttu-id="5bcb2-157">Attract で、職務を開きます。</span><span class="sxs-lookup"><span data-stu-id="5bcb2-157">In Attract, open the job.</span></span> <span data-ttu-id="5bcb2-158">エクスポートされた候補者は、職務の **候補者** タブに表示されます。</span><span class="sxs-lookup"><span data-stu-id="5bcb2-158">The exported candidate will appear on the **Prospect** tab of the job.</span></span>

## <a name="view-attract-information-in-linkedin-recruiter"></a><span data-ttu-id="5bcb2-159">LinkedIn Recruiter で Attract の情報を表示する</span><span class="sxs-lookup"><span data-stu-id="5bcb2-159">View Attract information in LinkedIn Recruiter</span></span>

<span data-ttu-id="5bcb2-160">LinkedIn Recruiter では、候補者が組織内の他の職務に応募したかどうか追跡し、候補者が求人応募のさまざまなステージでどこにいるかを確認し、Attract からのフィードバックとコメントを表示できます。</span><span class="sxs-lookup"><span data-stu-id="5bcb2-160">In LinkedIn Recruiter, you can track whether a candidate applied to other jobs in your organization, see where the candidate is in the various stages for job applications, and view feedback and comments from Attract.</span></span>

1. <span data-ttu-id="5bcb2-161">LinkedIn Recruiter を開いて、候補者プロファイルを選択します。</span><span class="sxs-lookup"><span data-stu-id="5bcb2-161">Open LinkedIn Recruiter, and select a candidate profile.</span></span>
2. <span data-ttu-id="5bcb2-162">**In ATS** をポイントします。</span><span class="sxs-lookup"><span data-stu-id="5bcb2-162">Hover over **In ATS**.</span></span>
3. <span data-ttu-id="5bcb2-163">Attract に格納されている候補者情報を表示するには、次のいずれかのオプションを選択します。</span><span class="sxs-lookup"><span data-stu-id="5bcb2-163">Select any of the following options to view the candidate information that is stored in Attract:</span></span>

    - <span data-ttu-id="5bcb2-164">**Jobs & Statuses** – 候補者が所属する職務、最新の状態、および各職務における候補者の進捗状況を確認します。</span><span class="sxs-lookup"><span data-stu-id="5bcb2-164">**Jobs & Statuses** – See jobs that the candidate is part of, the latest status, and how the candidate is progressing for each job.</span></span>
    - <span data-ttu-id="5bcb2-165">**面接フィードバック** – 面接者が Attract で送信したフィードバックを参照します。</span><span class="sxs-lookup"><span data-stu-id="5bcb2-165">**Interview Feedback** – See feedback that interviewers have submitted in Attract.</span></span>
    - <span data-ttu-id="5bcb2-166">**注記** – Attract でこの候補者に対して入力されたメモを確認します。</span><span class="sxs-lookup"><span data-stu-id="5bcb2-166">**Notes** – See any notes that have been entered for this candidate in Attract.</span></span>

    ![[<span data-ttu-id="5bcb2-167">LinkedIn Recruiter から Attract 情報を表示する</span><span class="sxs-lookup"><span data-stu-id="5bcb2-167">View Attract information from LinkedIn Recruiter</span></span>](./media/attract-view-information-from-linkedin-recruiter.png)](./media/attract-view-information-from-linkedin-recruiter.png)

> [!NOTE]
> <span data-ttu-id="5bcb2-168">候補者が過去の候補者のステージに移動していない場合、候補者と応募のデータは LinkedIn Recruiter とは同期されません。</span><span class="sxs-lookup"><span data-stu-id="5bcb2-168">Candidate and application data won't be synced with LinkedIn Recruiter if the candidate hasn't moved past the Prospect stage.</span></span>

## <a name="view-linkedin-talent-pools"></a><span data-ttu-id="5bcb2-169">LinkedIn 人材プールの表示</span><span class="sxs-lookup"><span data-stu-id="5bcb2-169">View LinkedIn talent pools</span></span>

<span data-ttu-id="5bcb2-170">候補者が LinkedIn プロファイルを組織内の任意のユーザーと共有することに同意した場合、新しい候補者レコードが Attract に作成されます。</span><span class="sxs-lookup"><span data-stu-id="5bcb2-170">If candidates agree to share their LinkedIn profiles with any user in your organization, a new candidate record is created in Attract.</span></span> <span data-ttu-id="5bcb2-171">これらの候補者は、システムで作成された LinkedIn 人材プールに表示されます。</span><span class="sxs-lookup"><span data-stu-id="5bcb2-171">These candidates then appear in a system-created LinkedIn talent pool.</span></span>

1. <span data-ttu-id="5bcb2-172">Attract で、左側にある **人材プール** を選択します。</span><span class="sxs-lookup"><span data-stu-id="5bcb2-172">In Attract, select **Talent pools** on the left.</span></span>
2. <span data-ttu-id="5bcb2-173">LinkedIn 人材プールを選択します。</span><span class="sxs-lookup"><span data-stu-id="5bcb2-173">Select the LinkedIn talent pool.</span></span> <span data-ttu-id="5bcb2-174">LinkedIn から候補者とそのスタブ プロファイルの一覧が表示されます。</span><span class="sxs-lookup"><span data-stu-id="5bcb2-174">You will see a list of candidates and their stub profiles from LinkedIn.</span></span> <span data-ttu-id="5bcb2-175">候補者が共有することを選択した場合、スタブ プロファイルには候補者の姓名と電子メール アドレスが含まれます。</span><span class="sxs-lookup"><span data-stu-id="5bcb2-175">Stub profiles contain the candidate's first and last names and email address, if the candidate chose to share it.</span></span>

## <a name="see-also"></a><span data-ttu-id="5bcb2-176">参照</span><span class="sxs-lookup"><span data-stu-id="5bcb2-176">See also</span></span>

[<span data-ttu-id="5bcb2-177">LinkedIn に関するよく寄せられる質問との Attract 統合</span><span class="sxs-lookup"><span data-stu-id="5bcb2-177">Attract integration with LinkedIn FAQ</span></span>](./attract-linkedin-faq.md)

[<span data-ttu-id="5bcb2-178">Microsoft Dynamics 365 Talent - Attract の LinkedIn との統合の設定</span><span class="sxs-lookup"><span data-stu-id="5bcb2-178">Set up integration with LinkedIn for Microsoft Dynamics 365 Talent - Attract</span></span>](./attract-admin-linkedin.md)

[<span data-ttu-id="5bcb2-179">Attract でジョブ求人の作成、承認、および投稿</span><span class="sxs-lookup"><span data-stu-id="5bcb2-179">Create, approve, and post jobs in Attract</span></span>](./creating-jobs-attract.md)

[<span data-ttu-id="5bcb2-180">Microsoft Dynamics 365 Talent - Attract から LinkedIn への職務の投稿</span><span class="sxs-lookup"><span data-stu-id="5bcb2-180">Post jobs to LinkedIn from Microsoft Dynamics 365 Talent - Attract</span></span>](./attract-post-jobs-to-linkedin.md)

[<span data-ttu-id="5bcb2-181">LinkedIn と Microsoft Dynamics 365 Talent - Attract との統合のトラブルシューティング</span><span class="sxs-lookup"><span data-stu-id="5bcb2-181">Troubleshooting integration with LinkedIn and Microsoft Dynamics 365 Talent - Attract</span></span>](./attract-troubleshoot-linkedin.md)
