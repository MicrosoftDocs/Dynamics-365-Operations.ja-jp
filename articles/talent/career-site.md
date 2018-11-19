---
title: "Attract のキャリア サイト機能"
description: "この記事では、Microsoft Dynamics 365 for Talent - Attract での候補者向けのキャリア サイト機能の概要を示します。 さらに、この機能の設定方法についても説明します。"
author: josaw
manager: AnnBe
ms.date: 10/18/2018
ms.topic: article
ms.prod: 
ms.service: dynamics-365-talent
ms.technology: 
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Talent
ms.custom: 
ms.assetid: 
ms.search.region: Global
ms.author: rschloma
ms.search.validFrom: 2018-10-18
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: e890e32049e930b70c2d0aac8aa8206ab999418a
ms.openlocfilehash: 452e3e92ea32ab5f1e3720ab81ff2f7ea18b2a06
ms.contentlocale: ja-jp
ms.lasthandoff: 10/22/2018

---
# <a name="career-site-functionality-in-attract"></a><span data-ttu-id="42541-104">Attract のキャリア サイト機能</span><span class="sxs-lookup"><span data-stu-id="42541-104">Career site functionality in Attract</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="42541-105">この記事は、Microsoft Dynamics 365 for Talent: Attract での候補者向けのキャリア サイト機能の概要を示します。</span><span class="sxs-lookup"><span data-stu-id="42541-105">This article provides an overview of the candidate-facing career site functionality in Microsoft Dynamics 365 for Talent: Attract.</span></span> <span data-ttu-id="42541-106">さらに、この機能の設定方法についても説明します。</span><span class="sxs-lookup"><span data-stu-id="42541-106">It also explains how to set up this functionality.</span></span>

## <a name="overview"></a><span data-ttu-id="42541-107">概要</span><span class="sxs-lookup"><span data-stu-id="42541-107">Overview</span></span>

<span data-ttu-id="42541-108">Attract ではテナントの環境ごとに 1 つのキャリア サイトが提供されます。</span><span class="sxs-lookup"><span data-stu-id="42541-108">Attract provides one career site for each environment in a tenant.</span></span> <span data-ttu-id="42541-109">たとえば、組織に開発環境およびテスト環境がある場合、1 つのキャリア サイトが開発環境に対してプロビジョニングされ、別のキャリア サイトがテスト環境に対してプロビジョニングされます。</span><span class="sxs-lookup"><span data-stu-id="42541-109">For example, if an organization has a development environment and a test environment, one career site is provisioned for the development environment, and another career site is provisioned for the test environment.</span></span> <span data-ttu-id="42541-110">各キャリア サイトは**完全に独立**しており、独自の認証メカニズムがあります。</span><span class="sxs-lookup"><span data-stu-id="42541-110">Each career site is **completely isolated** and has its own authentication mechanism.</span></span> <span data-ttu-id="42541-111">ジョブおよび候補者プロファイルは、キャリア サイト間では共有されません。</span><span class="sxs-lookup"><span data-stu-id="42541-111">Jobs and candidate profiles aren't shared between career sites.</span></span>

<span data-ttu-id="42541-112">既定では、キャリア サイトは公開されます。</span><span class="sxs-lookup"><span data-stu-id="42541-112">By default, the career site is public.</span></span> <span data-ttu-id="42541-113">したがって、候補者はサインインすることなく外部用としてマークされているすべてのジョブを表示できます。</span><span class="sxs-lookup"><span data-stu-id="42541-113">Therefore, candidates can view all jobs that are marked as external without having to sign in.</span></span> <span data-ttu-id="42541-114">ただし、他のすべてのアクションでは、候補者がサインインする必要があります。</span><span class="sxs-lookup"><span data-stu-id="42541-114">However, all other actions require that candidates sign in.</span></span>

## <a name="career-site-management"></a><span data-ttu-id="42541-115">キャリア サイトの管理</span><span class="sxs-lookup"><span data-stu-id="42541-115">Career site management</span></span>

<span data-ttu-id="42541-116">キャリア サイトの次の項目は、設定によって制御されます。</span><span class="sxs-lookup"><span data-stu-id="42541-116">The following items on the career site are controlled by settings:</span></span>

- <span data-ttu-id="42541-117">**組織名:** キャリア サイトの上部のナビゲーション バーに組織名が表示されます。</span><span class="sxs-lookup"><span data-stu-id="42541-117">**Organization name:** The organization name appears on the navigation bar at the top of the career site.</span></span> <span data-ttu-id="42541-118">組織名を選択すると、候補者は開いているすべてのジョブを一覧表示するページに移動します。</span><span class="sxs-lookup"><span data-stu-id="42541-118">By selecting the organization name, candidates go to a page that lists all open jobs.</span></span>
- <span data-ttu-id="42541-119">**組織ロゴ:** 組織ロゴの画像がキャリア サイトの左上部に表示されます。</span><span class="sxs-lookup"><span data-stu-id="42541-119">**Organization logo:** An image of the organization's logo appears in the upper left of the career site.</span></span> <span data-ttu-id="42541-120">ロゴ画像を選択すると、候補者は開いているすべてのジョブを一覧表示するページに移動します。</span><span class="sxs-lookup"><span data-stu-id="42541-120">By selecting the logo image, candidates go to a page that lists all open jobs.</span></span>

<span data-ttu-id="42541-121">組織名と組織ロゴの値を設定するには、管理者として Attract にサインインし、**設定**メニュー (ギヤ記号) で**管理センター**を選択してから、**会社情報**タブを選択します。</span><span class="sxs-lookup"><span data-stu-id="42541-121">To set the values for the organization name and logo, sign in to Attract as an administrator, select **Admin center** on the **Settings** menu (the gear symbol), and then select the **Company information** tab.</span></span>

> [!NOTE]
> <span data-ttu-id="42541-122">キャリア サイトに表示されるロゴ画像の固定の高さは、20 ピクセル (px) です。</span><span class="sxs-lookup"><span data-stu-id="42541-122">The logo image that appears on the career site has a fixed height of 20 pixels (px).</span></span> <span data-ttu-id="42541-123">管理センターで追加する画像の大きさが調整されます。</span><span class="sxs-lookup"><span data-stu-id="42541-123">The image that you add in the Admin center is scaled to fit.</span></span> <span data-ttu-id="42541-124">したがって、画像に応じて幅が変更する可能性があります。</span><span class="sxs-lookup"><span data-stu-id="42541-124">Therefore, depending on the image, the width might change.</span></span>

## <a name="career-site-url"></a><span data-ttu-id="42541-125">キャリア サイトの URL</span><span class="sxs-lookup"><span data-stu-id="42541-125">Career site URL</span></span>

<span data-ttu-id="42541-126">初めて [外部の人材募集](./Creating-jobs-Attract.md#postings) をする場合、Attract アプリケーションから**応募**リンクをコピーできます。</span><span class="sxs-lookup"><span data-stu-id="42541-126">When you [post an external job](./Creating-jobs-Attract.md#postings) for the first time, you can copy the **Apply** link from the Attract application.</span></span> <span data-ttu-id="42541-127">このリンクの URL は、次の形式になります: `https://jobs.talent.dynamics.com/jobs/<company_name>/<environment_number>/<job_number>/apply`</span><span class="sxs-lookup"><span data-stu-id="42541-127">The URL for this link will be in the following format: `https://jobs.talent.dynamics.com/jobs/<company_name>/<environment_number>/<job_number>/apply`</span></span>

<span data-ttu-id="42541-128">キャリア サイトの URL は、**応募** URL のサブ文字列です。</span><span class="sxs-lookup"><span data-stu-id="42541-128">The URL of the career site is a substring of the **Apply** URL.</span></span> <span data-ttu-id="42541-129">会社名に至るまですべてから構成されています。</span><span class="sxs-lookup"><span data-stu-id="42541-129">It consists of everything up through the company name.</span></span> <span data-ttu-id="42541-130">したがって、前の**応募** URL に関しては、キャリア サイト URL は `https://jobs.talent.dynamics.com/jobs/<company_name>/` です。</span><span class="sxs-lookup"><span data-stu-id="42541-130">Therefore, for the preceding **Apply** URL, the career site URL is `https://jobs.talent.dynamics.com/jobs/<company_name>/`.</span></span>

## <a name="authentication-options"></a><span data-ttu-id="42541-131">認証オプション</span><span class="sxs-lookup"><span data-stu-id="42541-131">Authentication options</span></span>

<span data-ttu-id="42541-132">候補者には、Attract キャリア サイトへの次のサインイン オプションがあります。</span><span class="sxs-lookup"><span data-stu-id="42541-132">Candidates have the following sign-in options for an Attract career site:</span></span>

- <span data-ttu-id="42541-133">個人のアカウント:</span><span class="sxs-lookup"><span data-stu-id="42541-133">Personal account:</span></span>

    - <span data-ttu-id="42541-134">LinkedIn</span><span class="sxs-lookup"><span data-stu-id="42541-134">LinkedIn</span></span>
    - <span data-ttu-id="42541-135">Microsoft</span><span class="sxs-lookup"><span data-stu-id="42541-135">Microsoft</span></span>
    - <span data-ttu-id="42541-136">Google</span><span class="sxs-lookup"><span data-stu-id="42541-136">Google</span></span>
    - <span data-ttu-id="42541-137">Facebook</span><span class="sxs-lookup"><span data-stu-id="42541-137">Facebook</span></span>

- <span data-ttu-id="42541-138">勤務先または学校アカウント:</span><span class="sxs-lookup"><span data-stu-id="42541-138">Work or school account:</span></span>

    - <span data-ttu-id="42541-139">Microsoft Azure Active Directory (Azure AD)</span><span class="sxs-lookup"><span data-stu-id="42541-139">Microsoft Azure Active Directory (Azure AD)</span></span>

<span data-ttu-id="42541-140">Azure AD サインインは内部の候補者のみを対象としています。</span><span class="sxs-lookup"><span data-stu-id="42541-140">Azure AD sign-in is intended only for internal candidates.</span></span> <span data-ttu-id="42541-141">したがって、これはその会社 Azure AD 資格情報を使用する内部の候補者に対してのみ機能します。</span><span class="sxs-lookup"><span data-stu-id="42541-141">Therefore, it works only for internal candidates who use their company Azure AD credentials.</span></span> <span data-ttu-id="42541-142">たとえば、現在 Contoso Ltd の従業員である候補者は、関連会社ではない Alpine Ski House でのジョブ募集に応募するとします。</span><span class="sxs-lookup"><span data-stu-id="42541-142">For example, a candidate who is currently an employee of Contoso Ltd wants to apply for a job in an unrelated company, Alpine Ski House.</span></span> <span data-ttu-id="42541-143">この場合、従業員が Contoso Ltd から自分の Azure AD 資格情報を使用しようとする場合、サインインが失敗します。</span><span class="sxs-lookup"><span data-stu-id="42541-143">In this case, the sign-in will be unsuccessful if the employee tries to use his or her Azure AD credentials from Contoso Ltd.</span></span>

## <a name="create-and-maintain-a-profile"></a><span data-ttu-id="42541-144">プロファイルの作成と管理</span><span class="sxs-lookup"><span data-stu-id="42541-144">Create and maintain a profile</span></span>

<span data-ttu-id="42541-145">候補者がキャリア サイトにサインインした後、ページの上部にあるナビゲーション バーで**自分のプロファイル**を選択して自分のプロファイルを作成および管理できます。</span><span class="sxs-lookup"><span data-stu-id="42541-145">After candidates sign in to the career site, they can select **My profile** on the navigation bar at the top of the page to create and maintain their profile.</span></span> <span data-ttu-id="42541-146">プロファイルには、個人情報、業務経験、教育の詳細、ドキュメント、リンク、およびスキル セットに関する情報が含まれています。</span><span class="sxs-lookup"><span data-stu-id="42541-146">The profile includes personal information, information about work experience, education details, documents, links, and information about skill sets.</span></span> <span data-ttu-id="42541-147">プロファイルを作成した後、候補者は興味があるジョブ求人への応募にそれを使用できます。</span><span class="sxs-lookup"><span data-stu-id="42541-147">After a profile is created, it can be used to apply for jobs that the candidate is interested in.</span></span> <span data-ttu-id="42541-148">プロファイルは、Attract が候補者に適切なジョブを推奨するのにも役立ちます。</span><span class="sxs-lookup"><span data-stu-id="42541-148">Profiles also help Attract recommend the right jobs to candidates.</span></span>

## <a name="find-the-right-job"></a><span data-ttu-id="42541-149">適切なジョブの検索</span><span class="sxs-lookup"><span data-stu-id="42541-149">Find the right job</span></span>

<span data-ttu-id="42541-150">ジョブ リスト ページで、候補者は検索条件を入力することにより特定のジョブを検索できます。</span><span class="sxs-lookup"><span data-stu-id="42541-150">On the job list page, candidates can search for a specific job by entering search terms.</span></span> <span data-ttu-id="42541-151">検索機能は職位およびジョブの説明での検索条件を検索し、結果として該当するジョブを表示します。</span><span class="sxs-lookup"><span data-stu-id="42541-151">The search functionality looks for the search terms in job titles and job descriptions, and shows relevant jobs as results.</span></span> <span data-ttu-id="42541-152">勤務地や職務権限に基づいて、候補者はいつでも結果をフィルター処理できます。</span><span class="sxs-lookup"><span data-stu-id="42541-152">Candidates can filter the results at any time, based on the job location or job function.</span></span>

<span data-ttu-id="42541-153">候補者は、キャリア サイト上で推奨される一連のジョブも表示できます。</span><span class="sxs-lookup"><span data-stu-id="42541-153">Candidates can also view a set of recommended jobs on the career site.</span></span> <span data-ttu-id="42541-154">候補者に推奨されるジョブは、候補者の過去のアプリケーション、プロファイル、および経歴に基づいています。</span><span class="sxs-lookup"><span data-stu-id="42541-154">The jobs that are recommended to a candidate are based on the candidate's past applications, profile, and resumes.</span></span>

> [!NOTE]
> <span data-ttu-id="42541-155">少なくとも 10 のジョブ求人がキャリア サイトで投稿される場合にのみ、および候補者が自分のプロファイルを完了した場合にのみ、職務の推奨事項が表示されます。</span><span class="sxs-lookup"><span data-stu-id="42541-155">Job recommendations are shown only if at least 10 jobs are posted on the career site, and if the candidate has completed his or her profile.</span></span>

## <a name="apply-for-jobs"></a><span data-ttu-id="42541-156">ジョブへの応募</span><span class="sxs-lookup"><span data-stu-id="42541-156">Apply for jobs</span></span>

<span data-ttu-id="42541-157">候補者が適切なジョブを検索した後、職務詳細情報ページで**応募**ボタンを使用して応募できます。</span><span class="sxs-lookup"><span data-stu-id="42541-157">After candidates find the right job, they can apply by using the **Apply** button on the job details page.</span></span> <span data-ttu-id="42541-158">この時点で、候補者は新しいプロファイルを作成するか、または既存のプロファイルで情報を確認するかのいずれかができます。</span><span class="sxs-lookup"><span data-stu-id="42541-158">At this point, candidates can either create a brand-new profile or review the information in their existing profile.</span></span> <span data-ttu-id="42541-159">候補者は、必要に応じて経歴書をアップロードでき、ジョブ求人への応募を送信できます。</span><span class="sxs-lookup"><span data-stu-id="42541-159">Candidates can also upload a resume, as required, and then submit the job application.</span></span>

## <a name="check-application-status"></a><span data-ttu-id="42541-160">申請ステータスの確認</span><span class="sxs-lookup"><span data-stu-id="42541-160">Check application status</span></span>

<span data-ttu-id="42541-161">候補者が 1 つまたは複数のジョブ求人に応募した後、ページの上部にあるナビゲーション バーの**申請**を選択して、オープンおよびクローズされた申請を表示できます。</span><span class="sxs-lookup"><span data-stu-id="42541-161">After candidates apply for one or more jobs, they can select **Applications** on the navigation bar at the top of the page to view their open and closed applications.</span></span> <span data-ttu-id="42541-162">候補者が申請のいずれかを開く場合、完了する必要のある現在のステージおよび保留中のアクション品目のいずれかが表示されます。</span><span class="sxs-lookup"><span data-stu-id="42541-162">When candidates open one of their applications, they see the current stage and any pending action items that they must complete.</span></span> <span data-ttu-id="42541-163">たとえば、候補者が個人面接が可能な日付を入力する必要がある場合、ページには自分のオプションが表示されます。</span><span class="sxs-lookup"><span data-stu-id="42541-163">For example, if a candidate must provide potential dates for an in-person interview, the page shows his or her options.</span></span>

## <a name="internal-jobs"></a><span data-ttu-id="42541-164">内部のジョブ求人</span><span class="sxs-lookup"><span data-stu-id="42541-164">Internal jobs</span></span>

<span data-ttu-id="42541-165">現時点では、内部求人としてマークされ Attract キャリア サイトに募集されているジョブは、キャリア サイトに表示されません。</span><span class="sxs-lookup"><span data-stu-id="42541-165">Currently, jobs that are marked as internal and posted to the Attract career site don't appear on the career site.</span></span> <span data-ttu-id="42541-166">Attract アプリケーションからコピーできる直接**応募** URL を通してのみアクセスできます。</span><span class="sxs-lookup"><span data-stu-id="42541-166">They are accessible only via the direct **Apply** URL that can be copied from the Attract application.</span></span>

