---
title: Attract のキャリア サイト機能
description: このトピックでは、Attract の候補者向けキャリア サイト機能の概要について説明します。
author: josaw1
manager: AnnBe
ms.date: 02/12/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-talent
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: josaw
ms.search.scope: Talent, Core
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: josaw
ms.search.validFrom: 2019-02-12
ms.dyn365.ops.version: AX 7.1.0, Talent April 2018 update
ms.openlocfilehash: 087ab4034a1e601e7f3514c77d56ef54b0c5c52d
ms.sourcegitcommit: 1ee613a88edddab036d145f27f19d071a4b8ad24
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 02/13/2019
ms.locfileid: "389972"
---
# <a name="career-site-functionality-in-attract"></a><span data-ttu-id="64f65-103">Attract のキャリア サイト機能</span><span class="sxs-lookup"><span data-stu-id="64f65-103">Career site functionality in Attract</span></span>

[!include[banner](../includes/banner.md)]

<span data-ttu-id="64f65-104">このトピックでは、Microsoft Dynamics 365 for Talent: Attract の候補者向けキャリア サイト機能の概要について説明します。</span><span class="sxs-lookup"><span data-stu-id="64f65-104">This topic provides an overview of the candidate-facing career site functionality in Microsoft Dynamics 365 for Talent: Attract.</span></span> <span data-ttu-id="64f65-105">さらに、この機能の設定方法についても説明します。</span><span class="sxs-lookup"><span data-stu-id="64f65-105">It also explains how to set up this functionality.</span></span>

<span data-ttu-id="64f65-106">Attract ではテナントの環境ごとに 1 つのキャリア サイトが提供されます。</span><span class="sxs-lookup"><span data-stu-id="64f65-106">Attract provides one career site for each environment in a tenant.</span></span> <span data-ttu-id="64f65-107">たとえば、組織に開発環境およびテスト環境がある場合、1 つのキャリア サイトが開発環境に対してプロビジョニングされ、別のキャリア サイトがテスト環境に対してプロビジョニングされます。</span><span class="sxs-lookup"><span data-stu-id="64f65-107">For example, if an organization has a development environment and a test environment, one career site is provisioned for the development environment, and another career site is provisioned for the test environment.</span></span> <span data-ttu-id="64f65-108">各キャリア サイトは完全に独立しており、独自の認証メカニズムがあります。</span><span class="sxs-lookup"><span data-stu-id="64f65-108">Each career site is completely isolated and has its own authentication mechanism.</span></span> <span data-ttu-id="64f65-109">ジョブおよび候補者プロファイルは、キャリア サイト間では共有されません。</span><span class="sxs-lookup"><span data-stu-id="64f65-109">Jobs and candidate profiles aren't shared between career sites.</span></span>

<span data-ttu-id="64f65-110">既定では、キャリア サイトは公開されます。</span><span class="sxs-lookup"><span data-stu-id="64f65-110">By default, the career site is public.</span></span> <span data-ttu-id="64f65-111">したがって、候補者はサインインすることなく外部用としてマークされているすべてのジョブを表示できます。</span><span class="sxs-lookup"><span data-stu-id="64f65-111">Therefore, candidates can view all jobs that are marked as external without having to sign in.</span></span> <span data-ttu-id="64f65-112">ただし、他のすべてのアクションでは、候補者がサインインする必要があります。</span><span class="sxs-lookup"><span data-stu-id="64f65-112">However, all other actions require that candidates sign in.</span></span>

## <a name="career-site-management"></a><span data-ttu-id="64f65-113">キャリア サイトの管理</span><span class="sxs-lookup"><span data-stu-id="64f65-113">Career site management</span></span>

<span data-ttu-id="64f65-114">以下の項目の値を設定するには、管理者として Attract にサインインし、**設定**メニュー (ギヤ記号) で**管理センター**を選択してから、**会社情報**タブを選択します。</span><span class="sxs-lookup"><span data-stu-id="64f65-114">To set the values for the following items, sign in to Attract as an administrator, select **Admin center** on the **Settings** menu (the gear symbol), and then select the **Company information** tab.</span></span>

-   <span data-ttu-id="64f65-115">**組織名** - キャリア サイトの上部のナビゲーション バーに組織名が表示されます。</span><span class="sxs-lookup"><span data-stu-id="64f65-115">**Organization name** - The organization name appears on the navigation bar at the top of the career site.</span></span> <span data-ttu-id="64f65-116">組織名を選択すると、候補者は開いているすべてのジョブを一覧表示するページに移動します。</span><span class="sxs-lookup"><span data-stu-id="64f65-116">By selecting the organization name, candidates go to a page that lists all open jobs.</span></span>

-   <span data-ttu-id="64f65-117">**組織ロゴ** - 組織ロゴの画像がキャリア サイトの左上部に表示されます。</span><span class="sxs-lookup"><span data-stu-id="64f65-117">**Organization logo** - An image of the organization's logo appears in the upper left of the career site.</span></span> <span data-ttu-id="64f65-118">ロゴ画像を選択すると、候補者は開いているすべてのジョブを一覧表示するページに移動します。</span><span class="sxs-lookup"><span data-stu-id="64f65-118">By selecting the logo image, candidates go to a page that lists all open jobs.</span></span>

    >   [!NOTE] 
    >   <span data-ttu-id="64f65-119">キャリア サイトに表示されるロゴ画像の固定の高さは、20 ピクセル (px) です。</span><span class="sxs-lookup"><span data-stu-id="64f65-119">The logo image that appears on the career site has a fixed height of 20 pixels (px).</span></span> <span data-ttu-id="64f65-120">管理センターで追加する画像の大きさが調整されます。</span><span class="sxs-lookup"><span data-stu-id="64f65-120">The image that you add in the Admin center is scaled to fit.</span></span> <span data-ttu-id="64f65-121">したがって、画像に応じて幅が変更する可能性があります。</span><span class="sxs-lookup"><span data-stu-id="64f65-121">Therefore, depending on the image, the width might change.</span></span>
 
<span data-ttu-id="64f65-122">以下の項目の値を設定するには、管理者として Attract にサインインし、**設定**メニューで**管理センター**を選択してから、**キャリア サイトの管理**タブを選択します。</span><span class="sxs-lookup"><span data-stu-id="64f65-122">To set the values for the following items, sign in to Attract as an administrator, select **Admin center** on the **Settings** menu, and then select the **Career site management** tab.</span></span>

-   <span data-ttu-id="64f65-123">**検索エンジンの最適化** - 有効にすると、Attract キャリア サイトに募集されているすべてのジョブは、Bing や Google などの検索エンジンを使用して検索可能になります。</span><span class="sxs-lookup"><span data-stu-id="64f65-123">**Search Engine Optimization** - When enabled, all public jobs posted to Attract career site will be searchable using search engines like Bing and Google.</span></span>

    >   [!NOTE] 
    >   <span data-ttu-id="64f65-124">使用している検索エンジンによって、この設定をオンにしてから検索結果が表示されるまでに時間がかかることがあります。</span><span class="sxs-lookup"><span data-stu-id="64f65-124">There might be a delay between turning this setting on and search results appearing, depending on the search engine that you are using.</span></span>
         
## <a name="career-site-urls"></a><span data-ttu-id="64f65-125">キャリア サイトの URL</span><span class="sxs-lookup"><span data-stu-id="64f65-125">Career site URLs</span></span>

<span data-ttu-id="64f65-126">次の一覧には、一般的に使用されるキャリア サイトの URL およびそのアクセス方法が含まれています。</span><span class="sxs-lookup"><span data-stu-id="64f65-126">The following list contains the commonly used career site URLs and how to access them.</span></span>

-   <span data-ttu-id="64f65-127">**キャリア サイトのホーム ページの URL** - キャリア サイトのホームページの URL を表示するには、管理者として Attract にサインインし、**設定**メニューで**管理センター**を選択してから、**キャリア サイトの管理** タブを選択します。</span><span class="sxs-lookup"><span data-stu-id="64f65-127">**Career site home page URL** - To view the career site home page URL, sign in to Attract as an administrator, select **Admin center** on the **Settings** menu, and then select the **Career site management** tab.</span></span>

-   <span data-ttu-id="64f65-128">**個別の人材募集 応募 URL** - 初めて[外部の人材募集](Creating-jobs-Attract.md#postings) をする場合、Attract アプリケーションから**応募**リンクをコピーできます。</span><span class="sxs-lookup"><span data-stu-id="64f65-128">**Individual job post apply URL** - When you [post an external job](Creating-jobs-Attract.md#postings) for the first time, you can copy the **Apply** link from the Attract application.</span></span> <span data-ttu-id="64f65-129">このリンクの URL は、次の形式になります: [https://jobs.talent.dynamics.com/jobs/\<company_name\>/\<environment_number\>/\<job_number\>/apply](https://jobs.talent.dynamics.com/jobs/%3ccompany_name%3e/%3cenvironment_number%3e/%3cjob_number%3e/apply)</span><span class="sxs-lookup"><span data-stu-id="64f65-129">The URL for this link will be in the following format: [https://jobs.talent.dynamics.com/jobs/\<company_name\>/\<environment_number\>/\<job_number\>/apply](https://jobs.talent.dynamics.com/jobs/%3ccompany_name%3e/%3cenvironment_number%3e/%3cjob_number%3e/apply)</span></span>

-   <span data-ttu-id="64f65-130">**個別の人材募集 URL** - 人材募集の URL は、応募 URL のサブ文字列です。</span><span class="sxs-lookup"><span data-stu-id="64f65-130">**Individual job post URL** - The URL of the job post is a substring of the Apply URL.</span></span> <span data-ttu-id="64f65-131">ジョブ番号に至るまですべてから構成されています。</span><span class="sxs-lookup"><span data-stu-id="64f65-131">It consists of everything up through the job number.</span></span> <span data-ttu-id="64f65-132">したがって、前の応募 URL に関しては、人材募集は [https://jobs.talent.dynamics.com/jobs/\<company_name\>/\<environment_number\>/\<job_number\>](https://jobs.talent.dynamics.com/jobs/%3ccompany_name%3e/%3cenvironment_number%3e/%3cjob_number%3e) です。</span><span class="sxs-lookup"><span data-stu-id="64f65-132">Therefore, for the preceding Apply URL, the job post URL is [https://jobs.talent.dynamics.com/jobs/\<company_name\>/\<environment_number\>/\<job_number\>](https://jobs.talent.dynamics.com/jobs/%3ccompany_name%3e/%3cenvironment_number%3e/%3cjob_number%3e)</span></span>

## <a name="authentication-options"></a><span data-ttu-id="64f65-133">認証オプション</span><span class="sxs-lookup"><span data-stu-id="64f65-133">Authentication options</span></span>

<span data-ttu-id="64f65-134">候補者には、Attract キャリア サイトへの次のサインイン オプションがあります。</span><span class="sxs-lookup"><span data-stu-id="64f65-134">Candidates have the following sign-in options for an Attract career site:</span></span>

-   <span data-ttu-id="64f65-135">個人のアカウント:</span><span class="sxs-lookup"><span data-stu-id="64f65-135">Personal account:</span></span>

    -   <span data-ttu-id="64f65-136">LinkedIn</span><span class="sxs-lookup"><span data-stu-id="64f65-136">LinkedIn</span></span>

    -   <span data-ttu-id="64f65-137">Microsoft</span><span class="sxs-lookup"><span data-stu-id="64f65-137">Microsoft</span></span>

    -   <span data-ttu-id="64f65-138">Google</span><span class="sxs-lookup"><span data-stu-id="64f65-138">Google</span></span>

    -   <span data-ttu-id="64f65-139">Facebook</span><span class="sxs-lookup"><span data-stu-id="64f65-139">Facebook</span></span>

-   <span data-ttu-id="64f65-140">勤務先または学校アカウント:</span><span class="sxs-lookup"><span data-stu-id="64f65-140">Work or school account:</span></span>

    -   <span data-ttu-id="64f65-141">Microsoft Azure Active Directory (Azure AD)</span><span class="sxs-lookup"><span data-stu-id="64f65-141">Microsoft Azure Active Directory (Azure AD)</span></span>

<span data-ttu-id="64f65-142">Azure AD サインインは内部の候補者のみを対象としています。</span><span class="sxs-lookup"><span data-stu-id="64f65-142">Azure AD sign-in is intended only for internal candidates.</span></span> <span data-ttu-id="64f65-143">したがって、これはその会社 Azure AD 資格情報を使用する内部の候補者に対してのみ機能します。</span><span class="sxs-lookup"><span data-stu-id="64f65-143">Therefore, it works only for internal candidates who use their company Azure AD credentials.</span></span> <span data-ttu-id="64f65-144">たとえば、現在 Contoso Ltd の従業員である候補者は、関連会社ではない Alpine Ski House でのジョブに応募するとします。</span><span class="sxs-lookup"><span data-stu-id="64f65-144">For example, a candidate who is currently an employee of Contoso Ltd wants to apply for a job in an unrelated company, Alpine Ski House.</span></span> <span data-ttu-id="64f65-145">この場合、従業員が Contoso Ltd から自分の Azure AD 資格情報を使用しようとする場合、サインインが失敗します。</span><span class="sxs-lookup"><span data-stu-id="64f65-145">In this case, the sign-in will be unsuccessful if the employee tries to use Azure AD credentials from Contoso Ltd.</span></span>

## <a name="create-and-maintain-a-profile"></a><span data-ttu-id="64f65-146">プロファイルの作成と管理</span><span class="sxs-lookup"><span data-stu-id="64f65-146">Create and maintain a profile</span></span>

<span data-ttu-id="64f65-147">候補者がキャリア サイトにサインインした後、ページの上部にあるナビゲーション バーで**自分のプロファイル**を選択して自分のプロファイルを作成および管理できます。</span><span class="sxs-lookup"><span data-stu-id="64f65-147">After candidates sign in to the career site, they can select **My profile** on the navigation bar at the top of the page to create and maintain their profile.</span></span>
<span data-ttu-id="64f65-148">プロファイルには、個人情報、業務経験、教育の詳細、ドキュメント、リンク、およびスキル セットに関する情報が含まれています。</span><span class="sxs-lookup"><span data-stu-id="64f65-148">The profile includes personal information, information about work experience, education details, documents, links, and information about skill sets.</span></span> <span data-ttu-id="64f65-149">プロファイルを作成した後、候補者は興味があるジョブ求人への応募にそれを使用できます。</span><span class="sxs-lookup"><span data-stu-id="64f65-149">After a profile is created, it can be used to apply for jobs that the candidate is interested in.</span></span> <span data-ttu-id="64f65-150">プロファイルは、Attract が候補者に適切なジョブを推奨するのにも役立ちます。</span><span class="sxs-lookup"><span data-stu-id="64f65-150">Profiles also help Attract recommend the right jobs to candidates.</span></span>

>   [!NOTE]
>   <span data-ttu-id="64f65-151">候補者が上記の認証プロバイダーのいずれかを使用してサインインするために電子メール ID を使用する場合、その電子メール ID はデフォルトでプロファイルに関連付けられた連絡先電子メール ID になります。</span><span class="sxs-lookup"><span data-stu-id="64f65-151">If a candidate uses an email ID to sign in using one of the authentication providers listed above, that email ID will default to the contact email ID associated with the profile.</span></span> <span data-ttu-id="64f65-152">しかしながら、後者はいつでも変更することができ、前者から完全に独立しています。</span><span class="sxs-lookup"><span data-stu-id="64f65-152">However, the latter can be changed at any time and is completely independent of the former.</span></span> <span data-ttu-id="64f65-153">Attract は、連絡先の電子メール ID を常に使用して、すべての電子メール通信のためにユーザーのプロフィールに関連付けます。</span><span class="sxs-lookup"><span data-stu-id="64f65-153">Attract will always use the contact email ID to associate with your profile for all email communications.</span></span>

## <a name="find-the-right-job"></a><span data-ttu-id="64f65-154">適切なジョブの検索</span><span class="sxs-lookup"><span data-stu-id="64f65-154">Find the right job</span></span>

<span data-ttu-id="64f65-155">ジョブ リスト ページで、候補者は検索条件を入力することにより特定のジョブを検索できます。</span><span class="sxs-lookup"><span data-stu-id="64f65-155">On the job list page, candidates can search for a specific job by entering search terms.</span></span> <span data-ttu-id="64f65-156">検索機能は職位およびジョブの説明での検索条件を検索し、結果として該当するジョブを表示します。</span><span class="sxs-lookup"><span data-stu-id="64f65-156">The search functionality looks for the search terms in job titles and job descriptions, and shows relevant jobs as results.</span></span> <span data-ttu-id="64f65-157">勤務地や職務権限に基づいて、候補者はいつでも結果をフィルター処理できます。</span><span class="sxs-lookup"><span data-stu-id="64f65-157">Candidates can filter the results at any time, based on the job location or job function.</span></span>

<span data-ttu-id="64f65-158">候補者は、キャリア サイト上で推奨される一連のジョブも表示できます。</span><span class="sxs-lookup"><span data-stu-id="64f65-158">Candidates can also view a set of recommended jobs on the career site.</span></span> <span data-ttu-id="64f65-159">候補者に推奨されるジョブは、候補者の過去のアプリケーション、プロファイル、および経歴に基づいています。</span><span class="sxs-lookup"><span data-stu-id="64f65-159">The jobs that are recommended to a candidate are based on the candidate's past applications, profile, and resumes.</span></span>

>   [!NOTE] 
>   <span data-ttu-id="64f65-160">少なくとも 10 のジョブ求人がキャリア サイトに掲載されている場合および候補者がプロファイルを完了した場合にのみ、職務の推奨事項が表示されます。</span><span class="sxs-lookup"><span data-stu-id="64f65-160">Job recommendations are shown only if at least 10 jobs are posted on the career site, and if the candidate has completed a profile.</span></span>

## <a name="apply-for-jobs"></a><span data-ttu-id="64f65-161">ジョブへの応募</span><span class="sxs-lookup"><span data-stu-id="64f65-161">Apply for jobs</span></span>

<span data-ttu-id="64f65-162">候補者が適切なジョブを検索した後、**職務詳細情報**ページで**応募**ボタンを使用して応募できます。</span><span class="sxs-lookup"><span data-stu-id="64f65-162">After candidates find the right job, they can apply by using the **Apply** button on the **Job details** page.</span></span> <span data-ttu-id="64f65-163">この時点で、候補者は新しいプロファイルを作成するか、または本人の既存のプロファイルで情報を確認するかのいずれかができます。</span><span class="sxs-lookup"><span data-stu-id="64f65-163">At this point, candidates can either create a new profile or review the information in their existing profile.</span></span>
<span data-ttu-id="64f65-164">候補者は、必要に応じて経歴書をアップロードでき、ジョブ求人への応募を送信できます。</span><span class="sxs-lookup"><span data-stu-id="64f65-164">Candidates can also upload a resume, as required, and then submit the job application.</span></span>

## <a name="check-application-status"></a><span data-ttu-id="64f65-165">申請状態の確認</span><span class="sxs-lookup"><span data-stu-id="64f65-165">Check application status</span></span>

<span data-ttu-id="64f65-166">候補者が 1 つまたは複数のジョブ求人に応募した後、ページの上部にあるナビゲーション バーの**申請**を選択して、オープンおよびクローズされた申請を表示できます。</span><span class="sxs-lookup"><span data-stu-id="64f65-166">After candidates apply for one or more jobs, they can select **Applications** on the navigation bar at the top of the page to view their open and closed applications.</span></span> <span data-ttu-id="64f65-167">候補者が申請のいずれかを開く場合、完了する必要のある現在のステージおよび保留中のアクション品目のいずれかが表示されます。</span><span class="sxs-lookup"><span data-stu-id="64f65-167">When candidates open one of their applications, they see the current stage and any pending action items that they must complete.</span></span> <span data-ttu-id="64f65-168">たとえば、候補者が個人面接が可能な日付を入力する必要がある場合、ページには可能なオプションが表示されます。</span><span class="sxs-lookup"><span data-stu-id="64f65-168">For example, if a candidate must provide potential dates for an in-person interview, the page shows the available options.</span></span>

## <a name="internal-jobs"></a><span data-ttu-id="64f65-169">内部のジョブ求人</span><span class="sxs-lookup"><span data-stu-id="64f65-169">Internal jobs</span></span>

<span data-ttu-id="64f65-170">現時点では、内部求人としてマークされ Attract キャリア サイトに募集されているジョブは、キャリア サイトに表示されません。</span><span class="sxs-lookup"><span data-stu-id="64f65-170">Currently, jobs that are marked as internal and posted to the Attract career site don't appear on the career site.</span></span> <span data-ttu-id="64f65-171">Attract アプリケーションからコピーできる直接**応募** URL を使用してのみアクセスできます。</span><span class="sxs-lookup"><span data-stu-id="64f65-171">They are only accessible using the direct **Apply** URL that can be copied from the Attract application.</span></span>
