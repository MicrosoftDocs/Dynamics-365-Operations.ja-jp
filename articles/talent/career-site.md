---
title: Attract のキャリア サイトの設定
description: このトピックでは、Microsoft Dynamics 365 Talent - Attract の候補者向けキャリア サイト機能の概要について説明します。
author: hasrivas
manager: AnnBe
ms.date: 03/20/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-talent
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Talent, Core
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: hasrivas
ms.search.validFrom: 2019-02-12
ms.dyn365.ops.version: AX 7.1.0, Talent April 2018 update
ms.openlocfilehash: d4a1e7c19ccec6ae32e46ec7d58604b162418953
ms.sourcegitcommit: 199848e78df5cb7c439b001bdbe1ece963593cdb
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 10/13/2020
ms.locfileid: "4461721"
---
# <a name="set-up-your-career-site-in-attract"></a><span data-ttu-id="eb91b-103">Attract のキャリア サイトの設定</span><span class="sxs-lookup"><span data-stu-id="eb91b-103">Set up your career site in Attract</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="eb91b-104">このトピックでは、Microsoft Dynamics 365 Talent: Attract の候補者向けキャリア サイト機能の概要について説明します。</span><span class="sxs-lookup"><span data-stu-id="eb91b-104">This topic provides an overview of the candidate-facing career site functionality in Microsoft Dynamics 365 Talent: Attract.</span></span> <span data-ttu-id="eb91b-105">さらに、この機能の設定方法についても説明します。</span><span class="sxs-lookup"><span data-stu-id="eb91b-105">It also explains how to set up this functionality.</span></span>

<span data-ttu-id="eb91b-106">Attract ではテナントの環境ごとに 1 つのキャリア サイトが提供されます。</span><span class="sxs-lookup"><span data-stu-id="eb91b-106">Attract provides one career site for each environment in a tenant.</span></span> <span data-ttu-id="eb91b-107">たとえば、組織に開発環境およびテスト環境がある場合、1 つのキャリア サイトが開発環境に対してプロビジョニングされ、別のキャリア サイトがテスト環境に対してプロビジョニングされます。</span><span class="sxs-lookup"><span data-stu-id="eb91b-107">For example, if an organization has a development environment and a test environment, one career site is provisioned for the development environment, and another career site is provisioned for the test environment.</span></span> <span data-ttu-id="eb91b-108">各キャリア サイトは完全に独立しており、独自の認証メカニズムがあります。</span><span class="sxs-lookup"><span data-stu-id="eb91b-108">Each career site is completely isolated and has its own authentication mechanism.</span></span> <span data-ttu-id="eb91b-109">ジョブおよび候補者プロファイルは、キャリア サイト間では共有されません。</span><span class="sxs-lookup"><span data-stu-id="eb91b-109">Jobs and candidate profiles aren't shared between career sites.</span></span>

<span data-ttu-id="eb91b-110">既定では、キャリア サイトは公開されます。</span><span class="sxs-lookup"><span data-stu-id="eb91b-110">By default, the career site is public.</span></span> <span data-ttu-id="eb91b-111">したがって、候補者はサインインすることなく外部用としてマークされているすべてのジョブを表示できます。</span><span class="sxs-lookup"><span data-stu-id="eb91b-111">Therefore, candidates can view all jobs that are marked as external without having to sign in.</span></span> <span data-ttu-id="eb91b-112">ただし、他のすべてのアクションでは、候補者がサインインする必要があります。</span><span class="sxs-lookup"><span data-stu-id="eb91b-112">However, all other actions require that candidates sign in.</span></span>

## <a name="career-site-management"></a><span data-ttu-id="eb91b-113">キャリア サイトの管理</span><span class="sxs-lookup"><span data-stu-id="eb91b-113">Career site management</span></span>

<span data-ttu-id="eb91b-114">以下の項目の値を設定するには、管理者として Attract にサインインし、**設定** メニュー (ギヤ記号) で **管理センター** を選択してから、**会社情報** タブを選択します。</span><span class="sxs-lookup"><span data-stu-id="eb91b-114">To set the values for the following items, sign in to Attract as an administrator, select **Admin center** on the **Settings** menu (the gear symbol), and then select the **Company information** tab.</span></span>

-   <span data-ttu-id="eb91b-115">**組織名** - キャリア サイトの上部のナビゲーション バーに組織名が表示されます。</span><span class="sxs-lookup"><span data-stu-id="eb91b-115">**Organization name** - The organization name appears on the navigation bar at the top of the career site.</span></span> <span data-ttu-id="eb91b-116">組織名を選択すると、候補者は開いているすべてのジョブを一覧表示するページに移動します。</span><span class="sxs-lookup"><span data-stu-id="eb91b-116">By selecting the organization name, candidates go to a page that lists all open jobs.</span></span>

-   <span data-ttu-id="eb91b-117">**組織ロゴ** - 組織ロゴの画像がキャリア サイトの左上部に表示されます。</span><span class="sxs-lookup"><span data-stu-id="eb91b-117">**Organization logo** - An image of the organization's logo appears in the upper left of the career site.</span></span> <span data-ttu-id="eb91b-118">ロゴ画像を選択すると、候補者は開いているすべてのジョブを一覧表示するページに移動します。</span><span class="sxs-lookup"><span data-stu-id="eb91b-118">By selecting the logo image, candidates go to a page that lists all open jobs.</span></span>

    > [!NOTE] 
    > <span data-ttu-id="eb91b-119">キャリア サイトに表示されるロゴ画像の固定の高さは、20 ピクセル (px) です。</span><span class="sxs-lookup"><span data-stu-id="eb91b-119">The logo image that appears on the career site has a fixed height of 20 pixels (px).</span></span> <span data-ttu-id="eb91b-120">管理センターで追加する画像の大きさが調整されます。</span><span class="sxs-lookup"><span data-stu-id="eb91b-120">The image that you add in the Admin center is  scaled to fit.</span></span> <span data-ttu-id="eb91b-121">したがって、画像に応じて幅が変更する可能性があります。</span><span class="sxs-lookup"><span data-stu-id="eb91b-121">Therefore, depending on the image, the width might change.</span></span>
 
<span data-ttu-id="eb91b-122">以下の項目の値を設定するには、管理者として Attract にサインインし、**設定** メニューで **管理センター** を選択してから、**キャリア サイトの管理** タブを選択します。</span><span class="sxs-lookup"><span data-stu-id="eb91b-122">To set the values for the following items, sign in to Attract as an administrator, select **Admin center** on the **Settings** menu, and then select the **Career site management** tab.</span></span>

-   <span data-ttu-id="eb91b-123">**検索エンジンの最適化** - 有効にすると、Attract キャリア サイトに募集されているすべてのジョブは、Bing や Google などの検索エンジンを使用して検索可能になります。</span><span class="sxs-lookup"><span data-stu-id="eb91b-123">**Search Engine Optimization** - When enabled, all public jobs posted to Attract career site will be searchable using search engines like Bing and Google.</span></span> 

    > [!NOTE] 
    > <span data-ttu-id="eb91b-124">使用している検索エンジンによって、この設定をオンにしてから検索結果が表示されるまでに時間がかかることがあります。</span><span class="sxs-lookup"><span data-stu-id="eb91b-124">There might be a delay between turning this setting on and search results appearing, depending on the search engine that you are using.</span></span>
    
-   <span data-ttu-id="eb91b-125">**契約条件** - 有効になっている場合、すべての候補者はジョブに応募する際に、組織の契約条件に同意する必要があります。</span><span class="sxs-lookup"><span data-stu-id="eb91b-125">**Terms and Conditions** - When enabled, all candidates must consent to the organization's terms and conditions when applying for any job.</span></span> <span data-ttu-id="eb91b-126">Attract 管理者は、独自の同意テキストと、その契約条件ページへのリンクをコンフィギュレーションすることができます。</span><span class="sxs-lookup"><span data-stu-id="eb91b-126">The Attract Administrator is able to configure their own Consent text as well as the link to their Terms and Conditions page.</span></span> 

        
## <a name="career-site-urls"></a><span data-ttu-id="eb91b-127">キャリア サイトの URL</span><span class="sxs-lookup"><span data-stu-id="eb91b-127">Career site URLs</span></span>

<span data-ttu-id="eb91b-128">次の一覧には、一般的に使用されるキャリア サイトの URL およびそのアクセス方法が含まれています。</span><span class="sxs-lookup"><span data-stu-id="eb91b-128">The following list contains the commonly used career site URLs and how to access them.</span></span>

-   <span data-ttu-id="eb91b-129">**キャリア サイトのホーム ページの URL** - キャリア サイトのホームページの URL を表示するには、管理者として Attract にサインインし、**設定** メニューで **管理センター** を選択してから、**キャリア サイトの管理** タブを選択します。</span><span class="sxs-lookup"><span data-stu-id="eb91b-129">**Career site home page URL** - To view the career site home page URL, sign in to Attract as an administrator, select **Admin center** on the **Settings** menu, and then select the **Career site management** tab.</span></span>

-   <span data-ttu-id="eb91b-130">**個別の人材募集 応募 URL** - 初めて [外部の人材募集](Creating-jobs-Attract.md#postings) をする場合、Attract から **応募** リンクをコピーできます。</span><span class="sxs-lookup"><span data-stu-id="eb91b-130">**Individual job post apply URL** - When you [post an external job](Creating-jobs-Attract.md#postings) for the first time, you can copy the **Apply** link from Attract.</span></span> <span data-ttu-id="eb91b-131">このリンクの URL は、次の形式になります: [https://jobs.talent.dynamics.com/jobs/\<company_name\>/\<environment_number\>/\<job_number\>/応募](https://jobs.talent.dynamics.com/jobs/%3ccompany_name%3e/%3cenvironment_number%3e/%3cjob_number%3e/apply)</span><span class="sxs-lookup"><span data-stu-id="eb91b-131">The URL for this link will be in the following format: [https://jobs.talent.dynamics.com/jobs/\<company_name\>/\<environment_number\>/\<job_number\>/apply](https://jobs.talent.dynamics.com/jobs/%3ccompany_name%3e/%3cenvironment_number%3e/%3cjob_number%3e/apply)</span></span>

-   <span data-ttu-id="eb91b-132">**個別の人材募集 URL** - 人材募集の URL は、応募 URL のサブ文字列です。</span><span class="sxs-lookup"><span data-stu-id="eb91b-132">**Individual job post URL** - The URL of the job post is a substring of the Apply URL.</span></span> <span data-ttu-id="eb91b-133">ジョブ番号に至るまですべてから構成されています。</span><span class="sxs-lookup"><span data-stu-id="eb91b-133">It consists of everything up through the job number.</span></span> <span data-ttu-id="eb91b-134">したがって、前の応募 URL に関しては、人材募集は [https://jobs.talent.dynamics.com/jobs/\<company_name\>/\<environment_number\>/\<job_number\>](https://jobs.talent.dynamics.com/jobs/%3ccompany_name%3e/%3cenvironment_number%3e/%3cjob_number%3e) です。</span><span class="sxs-lookup"><span data-stu-id="eb91b-134">Therefore, for the preceding Apply URL, the job post URL is [https://jobs.talent.dynamics.com/jobs/\<company_name\>/\<environment_number\>/\<job_number\>](https://jobs.talent.dynamics.com/jobs/%3ccompany_name%3e/%3cenvironment_number%3e/%3cjob_number%3e)</span></span>

## <a name="authentication-options"></a><span data-ttu-id="eb91b-135">認証オプション</span><span class="sxs-lookup"><span data-stu-id="eb91b-135">Authentication options</span></span>

<span data-ttu-id="eb91b-136">候補者には、Attract キャリア サイトへの次のサインイン オプションがあります。</span><span class="sxs-lookup"><span data-stu-id="eb91b-136">Candidates have the following sign-in options for an Attract career site:</span></span>

-   <span data-ttu-id="eb91b-137">個人のアカウント:</span><span class="sxs-lookup"><span data-stu-id="eb91b-137">Personal account:</span></span>

    -   <span data-ttu-id="eb91b-138">LinkedIn</span><span class="sxs-lookup"><span data-stu-id="eb91b-138">LinkedIn</span></span>

    -   <span data-ttu-id="eb91b-139">Microsoft</span><span class="sxs-lookup"><span data-stu-id="eb91b-139">Microsoft</span></span>

    -   <span data-ttu-id="eb91b-140">Google</span><span class="sxs-lookup"><span data-stu-id="eb91b-140">Google</span></span>

    -   <span data-ttu-id="eb91b-141">Facebook</span><span class="sxs-lookup"><span data-stu-id="eb91b-141">Facebook</span></span>

-   <span data-ttu-id="eb91b-142">勤務先または学校アカウント:</span><span class="sxs-lookup"><span data-stu-id="eb91b-142">Work or school account:</span></span>

    -   <span data-ttu-id="eb91b-143">Microsoft Azure Active Directory (Azure AD)</span><span class="sxs-lookup"><span data-stu-id="eb91b-143">Microsoft Azure Active Directory (Azure AD)</span></span>

<span data-ttu-id="eb91b-144">Azure AD サインインは内部の候補者のみを対象としています。</span><span class="sxs-lookup"><span data-stu-id="eb91b-144">Azure AD sign-in is intended only for internal candidates.</span></span> <span data-ttu-id="eb91b-145">したがって、これはその会社 Azure AD 資格情報を使用する内部の候補者に対してのみ機能します。</span><span class="sxs-lookup"><span data-stu-id="eb91b-145">Therefore, it works only for internal candidates who use their company Azure AD credentials.</span></span> <span data-ttu-id="eb91b-146">たとえば、現在 Contoso Ltd の従業員である候補者は、関連会社ではない Alpine Ski House でのジョブに応募するとします。</span><span class="sxs-lookup"><span data-stu-id="eb91b-146">For example, a candidate who is currently an employee of Contoso Ltd wants to apply for a job in an unrelated company, Alpine Ski House.</span></span> <span data-ttu-id="eb91b-147">この場合、従業員が Contoso Ltd から自分の Azure AD 資格情報を使用しようとする場合、サインインが失敗します。</span><span class="sxs-lookup"><span data-stu-id="eb91b-147">In this case, the sign-in will be unsuccessful if the employee tries to use Azure AD credentials from Contoso Ltd.</span></span> 

<span data-ttu-id="eb91b-148">閲覧または申請しているジョブが内部のみと表示される場合、候補者は Azure AD を使用してログインする必要があります。</span><span class="sxs-lookup"><span data-stu-id="eb91b-148">Candidates must sign in by using Azure AD if the job that they are viewing or applying for is listed as internal only.</span></span>

## <a name="create-and-maintain-a-profile"></a><span data-ttu-id="eb91b-149">プロファイルの作成と管理</span><span class="sxs-lookup"><span data-stu-id="eb91b-149">Create and maintain a profile</span></span>

<span data-ttu-id="eb91b-150">候補者がキャリア サイトにサインインした後、ページの上部にあるナビゲーション バーで **自分のプロファイル** を選択して自分のプロファイルを作成および管理できます。</span><span class="sxs-lookup"><span data-stu-id="eb91b-150">After candidates sign in to the career site, they can select **My profile** on the navigation bar at the top of the page to create and maintain their profile.</span></span>
<span data-ttu-id="eb91b-151">プロファイルには、個人情報、業務経験、教育の詳細、ドキュメント、リンク、およびスキル セットに関する情報が含まれています。</span><span class="sxs-lookup"><span data-stu-id="eb91b-151">The profile includes personal information, information about work experience, education details, documents, links, and information about skill sets.</span></span> <span data-ttu-id="eb91b-152">プロファイルを作成した後、候補者は興味があるジョブ求人への応募にそれを使用できます。</span><span class="sxs-lookup"><span data-stu-id="eb91b-152">After a profile is created, it can be used to apply for jobs that the candidate is interested in.</span></span> <span data-ttu-id="eb91b-153">プロファイルは、Attract が候補者に適切なジョブを推奨するのにも役立ちます。</span><span class="sxs-lookup"><span data-stu-id="eb91b-153">Profiles also help Attract recommend the right jobs to candidates.</span></span>

> [!NOTE]
> <span data-ttu-id="eb91b-154">候補者が上記の認証プロバイダーのいずれかを使用してサインインするために電子メール ID を使用する場合、その電子メール ID はデフォルトでプロファイルに関連付けられた連絡先電子メール ID になります。</span><span class="sxs-lookup"><span data-stu-id="eb91b-154">If a candidate uses an email ID to sign in using one of the authentication providers listed above, that email ID will default to the contact email ID associated with the profile.</span></span> <span data-ttu-id="eb91b-155">しかしながら、後者はいつでも変更することができ、前者から完全に独立しています。</span><span class="sxs-lookup"><span data-stu-id="eb91b-155">However, the latter can be changed at any time and is completely independent of the former.</span></span> <span data-ttu-id="eb91b-156">Attract は、連絡先の電子メール ID を常に使用して、すべての電子メール通信のためにユーザーのプロフィールに関連付けます。</span><span class="sxs-lookup"><span data-stu-id="eb91b-156">Attract will always use the contact email ID to associate with your profile for all email communications.</span></span>

## <a name="find-the-right-job"></a><span data-ttu-id="eb91b-157">適切なジョブの検索</span><span class="sxs-lookup"><span data-stu-id="eb91b-157">Find the right job</span></span>

<span data-ttu-id="eb91b-158">ジョブ リスト ページで、候補者は検索条件を入力することにより特定のジョブを検索できます。</span><span class="sxs-lookup"><span data-stu-id="eb91b-158">On the job list page, candidates can search for a specific job by entering search terms.</span></span> <span data-ttu-id="eb91b-159">検索機能は職位およびジョブの説明での検索条件を検索し、結果として該当するジョブを表示します。</span><span class="sxs-lookup"><span data-stu-id="eb91b-159">The search functionality looks for the search terms in job titles and job descriptions, and shows relevant jobs as results.</span></span> <span data-ttu-id="eb91b-160">勤務地や職務権限に基づいて、候補者はいつでも結果をフィルター処理できます。</span><span class="sxs-lookup"><span data-stu-id="eb91b-160">Candidates can filter the results at any time, based on the job location or job function.</span></span>

<span data-ttu-id="eb91b-161">候補者は、キャリア サイト上で推奨される一連のジョブも表示できます。</span><span class="sxs-lookup"><span data-stu-id="eb91b-161">Candidates can also view a set of recommended jobs on the career site.</span></span> <span data-ttu-id="eb91b-162">候補者に推奨されるジョブは、候補者の過去のアプリケーション、プロファイル、および経歴に基づいています。</span><span class="sxs-lookup"><span data-stu-id="eb91b-162">The jobs that are recommended to a candidate are based on the candidate's past applications, profile, and resumes.</span></span>

> [!NOTE] 
> <span data-ttu-id="eb91b-163">少なくとも 10 のジョブ求人がキャリア サイトに掲載されている場合および候補者がプロファイルを完了した場合にのみ、職務の推奨事項が表示されます。</span><span class="sxs-lookup"><span data-stu-id="eb91b-163">Job recommendations are shown only if at least 10 jobs are posted on the career site, and if the candidate has completed a profile.</span></span>

<span data-ttu-id="eb91b-164">採用チームのメンバーに連絡したい場合、内部候補者はジョブの採用マネージャーならびに採用担当者が誰であるかもわかります。</span><span class="sxs-lookup"><span data-stu-id="eb91b-164">Internal candidates can also see who the hiring manager and/or recruiter for a job is, in case they want to contact those members of the hiring team.</span></span> <span data-ttu-id="eb91b-165">ただし、外部の候補者はどんなジョブの採用チーム メンバーも閲覧できません。</span><span class="sxs-lookup"><span data-stu-id="eb91b-165">However, external candidates have no visibility into the members of the hiring team for any job.</span></span>

## <a name="contact-the-hiring-team"></a><span data-ttu-id="eb91b-166">採用チームに連絡してください</span><span class="sxs-lookup"><span data-stu-id="eb91b-166">Contact the hiring team</span></span>
<span data-ttu-id="eb91b-167">内部候補者のみが採用チームと連絡できます。</span><span class="sxs-lookup"><span data-stu-id="eb91b-167">Only internal candidates can contact the hiring team.</span></span> <span data-ttu-id="eb91b-168">この制限は、内部のみまたは公開が転記されたかどうかに関係なく、すべてのジョブに適用されます。</span><span class="sxs-lookup"><span data-stu-id="eb91b-168">This limitation applies to all jobs, regardless of whether they are internal only or were publicly posted.</span></span>

<span data-ttu-id="eb91b-169">候補者は、転記されたジョブに関心を示したり、詳細を知りたい場合は、採用チームに連絡してください。</span><span class="sxs-lookup"><span data-stu-id="eb91b-169">Candidates might want to contact the hiring team to express interest in a job that was posted or learn more about it.</span></span> <span data-ttu-id="eb91b-170">一覧にある採用チームのメンバーのいずれかに連絡できます (採用マネージャまたは採用担当者)。</span><span class="sxs-lookup"><span data-stu-id="eb91b-170">They can contact any of the hiring team members who are listed (hiring manager or recruiters).</span></span> <span data-ttu-id="eb91b-171">オプションでメッセージに履歴書を添付できます。また、以前にプロファイルの一部をアップロードした既存の履歴書を選択できます。</span><span class="sxs-lookup"><span data-stu-id="eb91b-171">They can also optionally attach a resume to the message, or they can select an existing resume they previously uploaded as part of their profile.</span></span>

<span data-ttu-id="eb91b-172">内部の候補者が連絡をするため採用チームのメンバーを選択した後、Attract は候補者代わりにユーザーへ電子メールを送信します。</span><span class="sxs-lookup"><span data-stu-id="eb91b-172">After an internal candidate selects the hiring team members to contact, Attract sends an email to those people on the candidate's behalf.</span></span> <span data-ttu-id="eb91b-173">同時に、そのステージがジョブに対応する場合、候補者のプロファイルが **見込顧客** ステージに追加されます。　</span><span class="sxs-lookup"><span data-stu-id="eb91b-173">At the same time, the candidate's profile is added to the **Prospect** stage, if that stage is available for the job.</span></span> <span data-ttu-id="eb91b-174">**見込顧客** ステージの下で、採用担当者または採用マネージャーは連絡を取った候補者を閲覧できます。</span><span class="sxs-lookup"><span data-stu-id="eb91b-174">Under the **Prospect** stage, recruiters or hiring managers can view the candidates who have contacted them.</span></span> <span data-ttu-id="eb91b-175">また、候補者のプロファイルをレビューし、候補者を招待して適用することも可能です。</span><span class="sxs-lookup"><span data-stu-id="eb91b-175">They can also review candidate profiles and invite potential candidates to apply.</span></span>

<span data-ttu-id="eb91b-176">候補者は、すでに採用のチーム メンバーに連絡したことのあるジョブに応募できます。</span><span class="sxs-lookup"><span data-stu-id="eb91b-176">Candidates can apply for a job that they have already contacted hiring team members about.</span></span> <span data-ttu-id="eb91b-177">適用後、候補者はキャリア サイトを通じて採用チームに連絡することはもうできません。</span><span class="sxs-lookup"><span data-stu-id="eb91b-177">After they apply, candidates can no longer contact the hiring team through the career site.</span></span>

## <a name="apply-for-jobs"></a><span data-ttu-id="eb91b-178">ジョブへの応募</span><span class="sxs-lookup"><span data-stu-id="eb91b-178">Apply for jobs</span></span>

<span data-ttu-id="eb91b-179">候補者が適切なジョブを検索した後、 **職務詳細情報** ページで **適用** ボタンを使用して応募できます。</span><span class="sxs-lookup"><span data-stu-id="eb91b-179">After candidates find the right job, they can apply by using the **Apply** button on the **Job details** page.</span></span> <span data-ttu-id="eb91b-180">この時点で、候補者は新しいプロファイルを作成するか、または本人の既存のプロファイルで情報を確認するかのいずれかができます。</span><span class="sxs-lookup"><span data-stu-id="eb91b-180">At this point, candidates can either create a new profile or review the information in their existing profile.</span></span>
<span data-ttu-id="eb91b-181">候補者は、必要に応じて経歴書をアップロードでき、ジョブ求人への応募を送信できます。</span><span class="sxs-lookup"><span data-stu-id="eb91b-181">Candidates can also upload a resume, as required, and then submit the job application.</span></span>

### <a name="enable-applying-for-jobs-with-linkedin-profiles"></a><span data-ttu-id="eb91b-182">LinkedIn プロファイルを使用して、ジョブの適用を有効</span><span class="sxs-lookup"><span data-stu-id="eb91b-182">Enable applying for jobs with LinkedIn profiles</span></span>

<span data-ttu-id="eb91b-183">LinkedIn を通じて適用を許可するよう Attract を構成することによって、候補者が職位に応募することを簡単にします。</span><span class="sxs-lookup"><span data-stu-id="eb91b-183">You can make it easy for candidates to apply for your positions by configuring Attract to allow them to apply through LinkedIn.</span></span>

> [!NOTE] 
> <span data-ttu-id="eb91b-184">LinkedIn に適用する候補者を許可する前に、LinkedIn からの 1 つまたは複数の採用ライセンスを持つ必要があります。</span><span class="sxs-lookup"><span data-stu-id="eb91b-184">You need to have one or more recruiter licenses from LinkedIn before you can allow candidates to apply with LinkedIn.</span></span>

1. <span data-ttu-id="eb91b-185">Attract に管理者としてサインインします。</span><span class="sxs-lookup"><span data-stu-id="eb91b-185">Sign in to Attract as an admin.</span></span>
2. <span data-ttu-id="eb91b-186">ページの右上隅にある **設定** ボタン (ギヤ記号) を選択して、**管理者センター** を選択します。</span><span class="sxs-lookup"><span data-stu-id="eb91b-186">Select the **Settings** button (the gear symbol) in the upper-right corner of the page, and then select **Admin center**.</span></span>
3. <span data-ttu-id="eb91b-187">**LinkedIn 統合** タブを選び、LinkedIn Recruiter アカウントに接続します。</span><span class="sxs-lookup"><span data-stu-id="eb91b-187">Select the **LinkedIn Integration** tab and connect with a LinkedIn recruiter account.</span></span>
4. <span data-ttu-id="eb91b-188">**LinkedIn Recruiter System Connect統合** セクションで、**LinkedIn を適用** 設定の **有効** を選択します。</span><span class="sxs-lookup"><span data-stu-id="eb91b-188">In the **LinkedIn Recruiter System Connect Integration** section, select **Enabled** for the **Apply with LinkedIn** setting.</span></span>

<span data-ttu-id="eb91b-189">設定を有効にした後、候補者は既存の LinkedIn プロファイル データを使用して応募できます。</span><span class="sxs-lookup"><span data-stu-id="eb91b-189">After you've enabled the setting, candidates can apply using their existing LinkedIn profile data.</span></span> <span data-ttu-id="eb91b-190">候補者が **LinkedIn に適用** ボタンをえらび応募するとき、まだログインしていないと、LinkedIn で認証を行うよう求められます。</span><span class="sxs-lookup"><span data-stu-id="eb91b-190">When candidates apply by choosing the **Apply with LinkedIn** button, they are asked to authenticate with LinkedIn if they're not already signed in.</span></span> <span data-ttu-id="eb91b-191">認証後、LinkedIn プロファイルはアプリケーション ページに表示される既存プロファイル データに置き換えられます。</span><span class="sxs-lookup"><span data-stu-id="eb91b-191">After they've authenticated, their LinkedIn profile replaces any existing profile data shown in the application page.</span></span> <span data-ttu-id="eb91b-192">候補者は、必要に応じて情報を編集して、申請を送信することができます。</span><span class="sxs-lookup"><span data-stu-id="eb91b-192">Candidates can edit the information as needed and then submit the application.</span></span> <span data-ttu-id="eb91b-193">ジョブを申請せずにページから移動した場合、自分のプロファイル データを Attract で更新することはできません。</span><span class="sxs-lookup"><span data-stu-id="eb91b-193">If a candidate navigates away from the page without applying for the job, their profile data is not updated in Attract.</span></span>

## <a name="check-application-status"></a><span data-ttu-id="eb91b-194">申請状態の確認</span><span class="sxs-lookup"><span data-stu-id="eb91b-194">Check application status</span></span>

<span data-ttu-id="eb91b-195">候補者が 1 つまたは複数のジョブ求人に応募した後、ページの上部にあるナビゲーション バーの **申請** を選択して、オープンおよびクローズされた申請を表示できます。</span><span class="sxs-lookup"><span data-stu-id="eb91b-195">After candidates apply for one or more jobs, they can select **Applications** on the navigation bar at the top of the page to view their open and closed applications.</span></span> <span data-ttu-id="eb91b-196">候補者が申請のいずれかを開く場合、完了する必要のある現在のステージおよび保留中のアクション品目のいずれかが表示されます。</span><span class="sxs-lookup"><span data-stu-id="eb91b-196">When candidates open one of their applications, they see the current stage and any pending action items that they must complete.</span></span> <span data-ttu-id="eb91b-197">たとえば、候補者が個人面接が可能な日付を入力する必要がある場合、ページには可能なオプションが表示されます。</span><span class="sxs-lookup"><span data-stu-id="eb91b-197">For example, if a candidate must provide potential dates for an in-person interview, the page shows the available options.</span></span>

## <a name="internal-jobs"></a><span data-ttu-id="eb91b-198">内部のジョブ求人</span><span class="sxs-lookup"><span data-stu-id="eb91b-198">Internal jobs</span></span>

<span data-ttu-id="eb91b-199">現時点では、内部求人としてマークされ Attract キャリア サイトに募集されているジョブは、キャリア サイトに表示されません。</span><span class="sxs-lookup"><span data-stu-id="eb91b-199">Currently, jobs that are marked as internal and posted to the Attract career site don't appear on the career site.</span></span> <span data-ttu-id="eb91b-200">Attract アプリケーションからコピーできる直接 **応募** URL を使用してのみアクセスできます。</span><span class="sxs-lookup"><span data-stu-id="eb91b-200">They are only accessible using the direct **Apply** URL that can be copied from the Attract application.</span></span>
