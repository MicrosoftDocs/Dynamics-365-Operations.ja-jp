---
title: Attract でジョブ求人の作成、承認、および転記
description: このトピックでは、Attract でのジョブ求人の要素について説明します。 ジョブ求人を作成する方法についても説明します。
author: josaw
manager: AnnBe
ms.date: 02/26/2019
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
ms.search.industry: ''
ms.author: josaw
ms.search.validFrom: 2018-10-24
ms.dyn365.ops.version: Talent October 2018 update
ms.openlocfilehash: 2f7e0ec7d33579f213909ff9ad911d26800c2b76
ms.sourcegitcommit: ceef0ee77ffc245e57637e2ea84e1a71a214b3d7
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 03/01/2019
ms.locfileid: "772814"
---
# <a name="create-approve-and-post-jobs-in-attract"></a><span data-ttu-id="cdc49-104">Attract でジョブ求人の作成、承認、および転記</span><span class="sxs-lookup"><span data-stu-id="cdc49-104">Create, approve, and post jobs in Attract</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="cdc49-105">このトピックでは、Microsoft Dynamics 365 for Talent: Attract でのジョブ求人の要素について説明します。</span><span class="sxs-lookup"><span data-stu-id="cdc49-105">This topic describes the elements of a job in Microsoft Dynamics 365 for Talent: Attract.</span></span> <span data-ttu-id="cdc49-106">ジョブ求人を作成する方法についても説明します。</span><span class="sxs-lookup"><span data-stu-id="cdc49-106">It also explains how to create a job.</span></span>

## <a name="job-creation"></a><span data-ttu-id="cdc49-107">職務の作成</span><span class="sxs-lookup"><span data-stu-id="cdc49-107">Job creation</span></span>

<span data-ttu-id="cdc49-108">管理者、採用担当者、および採用マネージャーがジョブ求人を作成できます。</span><span class="sxs-lookup"><span data-stu-id="cdc49-108">Admins, recruiters, and hiring managers can create jobs.</span></span> <span data-ttu-id="cdc49-109">ジョブ求人を作成するときに、プロセスでのロールを選択するよう求められます: 採用マネージャーまたは採用担当者。</span><span class="sxs-lookup"><span data-stu-id="cdc49-109">When you create a job, you're prompted to select your role in the process: hiring manager or recruiter.</span></span> <span data-ttu-id="cdc49-110">ロールを選択した後、プロセス テンプレートを選択するよう求められます。</span><span class="sxs-lookup"><span data-stu-id="cdc49-110">After you select a role, you're prompted to select a process template.</span></span> <span data-ttu-id="cdc49-111">**スキップ**を選択すると、既定のテンプレートが使用されます。</span><span class="sxs-lookup"><span data-stu-id="cdc49-111">If you select **Skip**, the default template is used.</span></span> <span data-ttu-id="cdc49-112">プロセス テンプレートの詳細については、[Attract でプロセス テンプレートの作成](./process-templates-attract.md) を参照してください。</span><span class="sxs-lookup"><span data-stu-id="cdc49-112">For more information about process templates, see [Create a process template in Attract](./process-templates-attract.md).</span></span>

<span data-ttu-id="cdc49-113">Attract でのジョブ求人には、職務の詳細、採用チーム、採用プロセス、人材募集、および分析が含まれます。</span><span class="sxs-lookup"><span data-stu-id="cdc49-113">A job in Attract has job details, a hiring team, a hiring process, job postings, and analytics.</span></span>

## <a name="job-details"></a><span data-ttu-id="cdc49-114">職務の詳細</span><span class="sxs-lookup"><span data-stu-id="cdc49-114">Job details</span></span>

<span data-ttu-id="cdc49-115">**職務の詳細**タブには、職務の職責と属性に関する詳細が含まれています。</span><span class="sxs-lookup"><span data-stu-id="cdc49-115">The **Job details** tab contains details about the job's responsibilities and attributes.</span></span> <span data-ttu-id="cdc49-116">職位、職務明細書、および勤務地のフィールドが必須です。</span><span class="sxs-lookup"><span data-stu-id="cdc49-116">The fields for the job title, job description, and job location are required.</span></span> <span data-ttu-id="cdc49-117">他のフィールドはオプションです。</span><span class="sxs-lookup"><span data-stu-id="cdc49-117">The other fields are optional.</span></span>

<span data-ttu-id="cdc49-118">既定では、**求人数**フィールドが **1** に設定されています。</span><span class="sxs-lookup"><span data-stu-id="cdc49-118">By default, the **Number of openings** field is set to **1**.</span></span> <span data-ttu-id="cdc49-119">ただし、その値は変更できます。</span><span class="sxs-lookup"><span data-stu-id="cdc49-119">However, you can change the value.</span></span> <span data-ttu-id="cdc49-120">ジョブのオファーが準備された場合、**空いている求人数**フィールドは減少します。</span><span class="sxs-lookup"><span data-stu-id="cdc49-120">When an offer has been prepared for a job, the value of the **Number of openings available** field is decremented.</span></span>

<span data-ttu-id="cdc49-121">職位管理が管理センターで有効になった場合、**職位の更新**ルックアップが使用できます。</span><span class="sxs-lookup"><span data-stu-id="cdc49-121">If position management has been turned on in the Admin Center, the **Update positions** lookup is available.</span></span> <span data-ttu-id="cdc49-122">このルックアップは Common Data Service for Apps の JobPosition エンティティを読み込み、職務に対して選択可能な職位の一覧を返します。</span><span class="sxs-lookup"><span data-stu-id="cdc49-122">This lookup reads the JobPosition entity in Common Data Service for Apps and returns a list of positions that can be selected for the job.</span></span> <span data-ttu-id="cdc49-123">選択する求人数が職位の求人数を超える場合、警告が表示されます。</span><span class="sxs-lookup"><span data-stu-id="cdc49-123">If the number of positions that you select exceeds the number of open positions, you receive a warning.</span></span> <span data-ttu-id="cdc49-124">職位が複数の職務に使用される場合にも、警告が表示されます。</span><span class="sxs-lookup"><span data-stu-id="cdc49-124">You also receive a warning if a position is used on multiple jobs.</span></span>

> [!NOTE]
> <span data-ttu-id="cdc49-125">職位管理は、 包括採用アドオンで使用できます。</span><span class="sxs-lookup"><span data-stu-id="cdc49-125">Position management is available with the Comprehensive Hiring Add-on.</span></span>

<span data-ttu-id="cdc49-126">採用プロセスのオファー アクティビティでの設定に応じて、職位数は 1 つのオファーに対して 2 回使用できます。</span><span class="sxs-lookup"><span data-stu-id="cdc49-126">Depending on the settings in the Offer activity of the hiring process, a position number can be used twice in an offer.</span></span> <span data-ttu-id="cdc49-127">詳細については、[採用プロセス](./activities-attract.md) を参照してください。</span><span class="sxs-lookup"><span data-stu-id="cdc49-127">For more information, see [Hiring process](./activities-attract.md).</span></span>

<span data-ttu-id="cdc49-128">Attract には、既定の一連の**スキル**が含まれます。</span><span class="sxs-lookup"><span data-stu-id="cdc49-128">Attract includes a default set of **Skills**.</span></span> <span data-ttu-id="cdc49-129">これらのスキルは、入力する際の提案として表示されます。</span><span class="sxs-lookup"><span data-stu-id="cdc49-129">These skills appear as suggestions as you type.</span></span> <span data-ttu-id="cdc49-130">フィールドに新しいスキル テキストを入力し、Enter キーを押して、スキルをさらに追加できます。</span><span class="sxs-lookup"><span data-stu-id="cdc49-130">You can add more skills by entering the new skill text in the field and then pressing Enter.</span></span>

<span data-ttu-id="cdc49-131">Attract には、既定の一連の**職務権限**が含まれます。</span><span class="sxs-lookup"><span data-stu-id="cdc49-131">Attract includes a default set of **Job functions**.</span></span> <span data-ttu-id="cdc49-132">フィールドに新しい職務権限を入力し、Enter キーを押して、3 つまでさらに職務権限を追加できます。</span><span class="sxs-lookup"><span data-stu-id="cdc49-132">You can add up to three more job functions by entering the new job function in the field and then pressing Enter.</span></span>

<span data-ttu-id="cdc49-133">Attract には、既定の一連の**会社の業種**が含まれます。</span><span class="sxs-lookup"><span data-stu-id="cdc49-133">Attract includes a default set of **Company industry**.</span></span> <span data-ttu-id="cdc49-134">フィールドに新しい会社の業種を入力し、Enter キーを押して、3 つまでさらに会社の業種を追加できます。</span><span class="sxs-lookup"><span data-stu-id="cdc49-134">You can add up to three more company industries by entering the new company industry in the field and then pressing Enter.</span></span>

## <a name="hiring-team"></a><span data-ttu-id="cdc49-135">採用チーム</span><span class="sxs-lookup"><span data-stu-id="cdc49-135">Hiring team</span></span>

<span data-ttu-id="cdc49-136">**採用チーム**タブには、ジョブ求人に関与する個人の一覧が含まれます。</span><span class="sxs-lookup"><span data-stu-id="cdc49-136">The **Hiring team** tab contains the list of individuals who will be involved in the job.</span></span> <span data-ttu-id="cdc49-137">ユーザーが採用チームに追加される場合、採用チームでのロールが割り当てられる必要があります。</span><span class="sxs-lookup"><span data-stu-id="cdc49-137">When users are added to a hiring team, they must be assigned a role on the hiring team.</span></span> <span data-ttu-id="cdc49-138">ロールは、ユーザーのアクセス先および受信する通知のデータを決定します。</span><span class="sxs-lookup"><span data-stu-id="cdc49-138">The role determines the data that the users have access to and the notifications that they receive.</span></span> <span data-ttu-id="cdc49-139">選択できるロールは、**採用担当者**、**採用マネージャー**、**代理人**、および**面接者**です。</span><span class="sxs-lookup"><span data-stu-id="cdc49-139">The roles that can be selected are **Recruiter**, **Hiring manager**, **Delegate**, and **Interviewer**.</span></span> <span data-ttu-id="cdc49-140">ロール権限の詳細については、"ロール管理" ドキュメントを参照してください。</span><span class="sxs-lookup"><span data-stu-id="cdc49-140">For more information about role privileges, see the "Role management" document.</span></span> <span data-ttu-id="cdc49-141">採用担当者および採用マネージャーは、代わりに 1 名以上の複数の代理人を指名できます。</span><span class="sxs-lookup"><span data-stu-id="cdc49-141">Recruiters and hiring managers can appoint one or more delegates to work on their behalf.</span></span> <span data-ttu-id="cdc49-142">代理人の詳細については、[Attract でのセキュリティおよびロールの管理](./security-attract.md) を参照してください。</span><span class="sxs-lookup"><span data-stu-id="cdc49-142">For more information about delegates, see [Security and role management in Attract](./security-attract.md).</span></span>

<span data-ttu-id="cdc49-143">ジョブ求人が有効になった後、採用チームを更新できます。</span><span class="sxs-lookup"><span data-stu-id="cdc49-143">The hiring team can be updated after the job is activated.</span></span>

## <a name="process"></a><span data-ttu-id="cdc49-144">プロセス</span><span class="sxs-lookup"><span data-stu-id="cdc49-144">Process</span></span>

<span data-ttu-id="cdc49-145">採用プロセスに関する既定の情報は、ジョブ求人が作成されたときに選択されたプロセス テンプレートに基づきます。</span><span class="sxs-lookup"><span data-stu-id="cdc49-145">Default information about the hiring process is based on the process template that was selected when the job was created.</span></span> <span data-ttu-id="cdc49-146">その時点で特定のテンプレートが選択されなかった場合には、既定のテンプレートが使用されます。</span><span class="sxs-lookup"><span data-stu-id="cdc49-146">If a specific template wasn't selected at that time, the default template is used.</span></span> <span data-ttu-id="cdc49-147">採用プロセスを定義する場合、候補者、応募、およびオファー ステージ以外のさまざまなステージを追加または削除できます。</span><span class="sxs-lookup"><span data-stu-id="cdc49-147">When you define the hiring process, you can add or remove various stages, except the Prospect, Application, and Offer stages.</span></span> <span data-ttu-id="cdc49-148">候補者のステージを削除できませんが、無効にはできます。</span><span class="sxs-lookup"><span data-stu-id="cdc49-148">Although the Prospect stage can't be removed, it can be turned off.</span></span> <span data-ttu-id="cdc49-149">各ステージ内では、1 つまたは複数の事前に定義された活動を追加または削除できます。</span><span class="sxs-lookup"><span data-stu-id="cdc49-149">Within each stage, you can add or remove one or more predefined activities.</span></span>

<span data-ttu-id="cdc49-150">採用プロセスに追加できる活動に関する詳細については、[Attract での採用プロセス活動](./activities-attract.md) を参照してください。</span><span class="sxs-lookup"><span data-stu-id="cdc49-150">For more information about activities that can be added to the hiring process, see [Hiring process activities in Attract](./activities-attract.md).</span></span>

> [!NOTE]
> <span data-ttu-id="cdc49-151">ジョブ求人が有効になった後は、採用のプロセスを更新できません。</span><span class="sxs-lookup"><span data-stu-id="cdc49-151">The process hiring can't be updated after a job is activated.</span></span>

## <a name="postings"></a><span data-ttu-id="cdc49-152">転記</span><span class="sxs-lookup"><span data-stu-id="cdc49-152">Postings</span></span>

<span data-ttu-id="cdc49-153">ジョブ求人が有効になった後に、転記できます。</span><span class="sxs-lookup"><span data-stu-id="cdc49-153">After a job is activated, it can be posted.</span></span> <span data-ttu-id="cdc49-154">採用担当者と管理者だけが、ジョブ求人を転記できます。</span><span class="sxs-lookup"><span data-stu-id="cdc49-154">Only recruiters and admins can post jobs.</span></span> <span data-ttu-id="cdc49-155">ジョブ求人は、Talent Careers (Microsoft Dynamics 365 for Talent キャリア サイト) または LinkedIn のいずれかに転記できます。</span><span class="sxs-lookup"><span data-stu-id="cdc49-155">The job can be posted to either Talent Careers (a Microsoft Dynamics 365 for Talent career site) or LinkedIn.</span></span> 

<span data-ttu-id="cdc49-156">Attract チームは、継続的にジョブ ボード アグリゲーターと提携していきます。</span><span class="sxs-lookup"><span data-stu-id="cdc49-156">The Attract team is continually working to partner with job board aggregators.</span></span> <span data-ttu-id="cdc49-157">このリストは時間の経過に伴い展開されます。</span><span class="sxs-lookup"><span data-stu-id="cdc49-157">This list will expand over time.</span></span>

<span data-ttu-id="cdc49-158">ジョブ求人の転記の詳細については、[Attractでキャリア サイト機能](career-site.md) を参照してください。</span><span class="sxs-lookup"><span data-stu-id="cdc49-158">For more information about job postings, see [Career site functionality in Attract](career-site.md).</span></span>

> [!NOTE]
> <span data-ttu-id="cdc49-159">ジョブ求人の転記機能は、Attract の包括採用アドオンでのみ使用できます。</span><span class="sxs-lookup"><span data-stu-id="cdc49-159">The job posting functionality is available only with the Comprehensive Hiring Add-on for Attract.</span></span>

### <a name="posting-jobs-to-linkedin"></a><span data-ttu-id="cdc49-160">LinkedIn へのジョブ求人の転記</span><span class="sxs-lookup"><span data-stu-id="cdc49-160">Posting jobs to LinkedIn</span></span> 

<span data-ttu-id="cdc49-161">Attract から LinkedIn にジョブを転記する前に、管理者は**管理者設定**に LinkedIn Company ID および LinkedIn Company 名を追加する必要があります。</span><span class="sxs-lookup"><span data-stu-id="cdc49-161">Before posting a job from Attract to LinkedIn, the administrator must add the LinkedIn Company ID and LinkedIn Company name in the **Admin Settings**.</span></span> <span data-ttu-id="cdc49-162">LinkedIn Company ID は、Attract からのジョブ求人が正しい会社ページにマップされていることを確認するために必要です。</span><span class="sxs-lookup"><span data-stu-id="cdc49-162">The LinkedIn Company ID is required to ensure your jobs posted from Attract are mapped to the correct company page.</span></span>

<span data-ttu-id="cdc49-163">LinkedIn Company ID は、LinkedIn 内で会社を固有に識別する文字列です。</span><span class="sxs-lookup"><span data-stu-id="cdc49-163">Your LinkedIn Company ID is a string of numbers that uniquely identifies your company within LinkedIn.</span></span> <span data-ttu-id="cdc49-164">LinkedIn company ID を確認する方法の詳細については、[LinkedIn のサイト](https://aka.ms/findID) を参照してください。</span><span class="sxs-lookup"><span data-stu-id="cdc49-164">For more information on how to find your LinkedIn company ID, please visit the [LinkedIn site](https://aka.ms/findID).</span></span>

<span data-ttu-id="cdc49-165">LinkedIn の会社を更新するには、 **設定** メニュー (ギア記号) で **管理センター** を選択してから、 **LinkedIn の統合** タブを選択します。</span><span class="sxs-lookup"><span data-stu-id="cdc49-165">To update your LinkedIn company, select **Admin center** on the **Settings** menu (the gear symbol), and then select the **LinkedIn Integration** tab.</span></span> <span data-ttu-id="cdc49-166">**LinkedIn に接続**セクションで、LinkedIn 会社名 および 会社 ID を入力してから設定を保存します。</span><span class="sxs-lookup"><span data-stu-id="cdc49-166">Under the **Connect to LinkedIn** section, enter your LinkedIn Company Name and Company ID, and then save the settings.</span></span>

> [!NOTE]
> <span data-ttu-id="cdc49-167">LinkedIn へのジョブ求人転記プロセスについての重要な注意事項が 4 つあります。</span><span class="sxs-lookup"><span data-stu-id="cdc49-167">There are four important things to note about job posting process to LinkedIn.</span></span>
> 1. <span data-ttu-id="cdc49-168">LinkedIn に転記されたジョブ求人は、「制限付きリスト」ジョブ求人として投稿されます。</span><span class="sxs-lookup"><span data-stu-id="cdc49-168">Jobs posted to LinkedIn are posted as "Limited Listings" jobs.</span></span> <span data-ttu-id="cdc49-169">制限付きリストのジョブ求人を LinkedIn のサイト全体で宣伝することはできません。</span><span class="sxs-lookup"><span data-stu-id="cdc49-169">Limited listing jobs cannot be promoted across the LinkedIn site.</span></span> <span data-ttu-id="cdc49-170">Attract から LinkedIn へ転記された制限付きリストのジョブ求人を宣伝したい場合は、LinkedIn と連携して「求人ラッピング」を有効にする必要があります。</span><span class="sxs-lookup"><span data-stu-id="cdc49-170">If you want to promote limited listing jobs posted to LinkedIn from Attract, you should work with LinkedIn to enable "Job Wrapping".</span></span> <span data-ttu-id="cdc49-171">詳細については、次のリンクを参照して LinkedIn サポートにご連絡ください。</span><span class="sxs-lookup"><span data-stu-id="cdc49-171">Please refer to links below and contact LinkedIn support for more details.</span></span>
>
>    [<span data-ttu-id="cdc49-172">制限付きリストと Job Wrapping のプレミアム求人枠</span><span class="sxs-lookup"><span data-stu-id="cdc49-172">Limited Listings vs Premium Job Slots for Job Wrapping</span></span>](https://www.linkedin.com/help/recruiter/answer/79049/limited-listings-vs-premium-job-slots-for-job-wrapping)
>
>    [<span data-ttu-id="cdc49-173">求人ラッピングよくある質問</span><span class="sxs-lookup"><span data-stu-id="cdc49-173">Job Wrapping FAQ</span></span>](https://www.linkedin.com/help/recruiter/answer/79050/job-wrapping-frequently-asked-questions)
>
> 1. <span data-ttu-id="cdc49-174">LinkedIn にジョブ求人を転記する際、Attractは、ジョブ求人に対して Microsoft 365 組織名を渡します。</span><span class="sxs-lookup"><span data-stu-id="cdc49-174">When posting jobs to LinkedIn, Attract passes the Microsoft 365 Organization name against the job.</span></span> <span data-ttu-id="cdc49-175">LinkedIn は、渡された組織名に基づいてジョブ求人を LinkedIn 側の会社にリンクします。</span><span class="sxs-lookup"><span data-stu-id="cdc49-175">LinkedIn links the jobs to a company on the LinkedIn side based on the organization name that is passed.</span></span> <span data-ttu-id="cdc49-176">仕事が LinkedIn で間違った会社に対してリストされている場合は、Microsoft 365 の組織名が LinkedIn の会社名と一致することを確認してください。</span><span class="sxs-lookup"><span data-stu-id="cdc49-176">If your job is listed against the wrong company on LinkedIn, check that your Microsoft 365 Organization name matches the company name on LinkedIn.</span></span>  
>
>    [<span data-ttu-id="cdc49-177">住所や連絡先などの変更</span><span class="sxs-lookup"><span data-stu-id="cdc49-177">Change Address Contact and more</span></span>](https://docs.microsoft.com/en-us/office365/admin/manage/change-address-contact-and-more)
>
>    <span data-ttu-id="cdc49-178">この手順の後に問題がある場合は、LinkedIn サポートにお問い合わせください。</span><span class="sxs-lookup"><span data-stu-id="cdc49-178">If you have problems after this step, please contact LinkedIn support.</span></span> 
> 
> 1. <span data-ttu-id="cdc49-179">LinkedIn に転記されたジョブは、ライブ LinkedIn サイトに表示されます。</span><span class="sxs-lookup"><span data-stu-id="cdc49-179">Jobs posted to LinkedIn appear on the live LinkedIn site.</span></span> <span data-ttu-id="cdc49-180">LinkedIn にジョブを転記するためのテスト環境ではありません。</span><span class="sxs-lookup"><span data-stu-id="cdc49-180">There is no test environment for posting jobs to LinkedIn.</span></span> 
>
> 1. <span data-ttu-id="cdc49-181">現在の LinkedIn バッチ ジョブ求人転記プロセスのため、LinkedIn に転記されたジョブ求人が LinkedIn 内から求職者に表示されるまでには、最大 24 時間かかることがあります。</span><span class="sxs-lookup"><span data-stu-id="cdc49-181">It may take up to 24 hours for jobs posted to LinkedIn to be visible to candidates from within in LinkedIn, due to the current LinkedIn batch job posting process.</span></span>


## <a name="activate"></a><span data-ttu-id="cdc49-182">有効化する</span><span class="sxs-lookup"><span data-stu-id="cdc49-182">Activate</span></span>

<span data-ttu-id="cdc49-183">ジョブ求人が有効になった後、転記でき、候補者および申請者を追加できます。</span><span class="sxs-lookup"><span data-stu-id="cdc49-183">After a job is activated, it can be posted, and prospects and applicants can be added to it.</span></span> <span data-ttu-id="cdc49-184">ジョブ求人に候補者を追加するオプションは、採用プロセスの候補者活動で設定されます。</span><span class="sxs-lookup"><span data-stu-id="cdc49-184">The option to add prospects to a job is set in the Prospect activity in the hiring process.</span></span>

> [!NOTE]
> <span data-ttu-id="cdc49-185">ジョブ求人が有効になった後は、採用のプロセスを更新できません。</span><span class="sxs-lookup"><span data-stu-id="cdc49-185">The process hiring can't be updated after a job is activated.</span></span>

## <a name="prospects-and-applicants"></a><span data-ttu-id="cdc49-186">候補者および申請者</span><span class="sxs-lookup"><span data-stu-id="cdc49-186">Prospects and applicants</span></span>

<span data-ttu-id="cdc49-187">ジョブ求人に候補者を追加するオプションは、採用プロセスの [候補者活動](./activities-attract.md#prospect-activity) で設定されます。</span><span class="sxs-lookup"><span data-stu-id="cdc49-187">The option to add prospects to a job is set in the [Prospect activity](./activities-attract.md#prospect-activity) in the hiring process.</span></span> <span data-ttu-id="cdc49-188">ジョブ求人を有効にする前に、このオプションを設定する必要があります。</span><span class="sxs-lookup"><span data-stu-id="cdc49-188">This option should be set before you activate the job.</span></span> <span data-ttu-id="cdc49-189">ジョブ求人が有効になった後、候補者および申請者を追加できます。</span><span class="sxs-lookup"><span data-stu-id="cdc49-189">After a job is activated, prospects and applicants can be added to it.</span></span>

## <a name="approvals"></a><span data-ttu-id="cdc49-190">承認</span><span class="sxs-lookup"><span data-stu-id="cdc49-190">Approvals</span></span>

<span data-ttu-id="cdc49-191">Attract のジョブ求人は、承認用に申請できます。</span><span class="sxs-lookup"><span data-stu-id="cdc49-191">Attract jobs can be submitted for approval.</span></span> <span data-ttu-id="cdc49-192">すべてのジョブ求人に、承認が必要ではありません。</span><span class="sxs-lookup"><span data-stu-id="cdc49-192">Not all jobs require approval.</span></span> <span data-ttu-id="cdc49-193">要件は、テンプレート レベルで設定されます。</span><span class="sxs-lookup"><span data-stu-id="cdc49-193">The requirement is set at the template level.</span></span> <span data-ttu-id="cdc49-194">既定では、テンプレートで承認が無効になっています。</span><span class="sxs-lookup"><span data-stu-id="cdc49-194">By default, approvals are turned off on the template.</span></span> <span data-ttu-id="cdc49-195">承認を設定するには、プロセス テンプレートに移動し、**承認**フィールドを既定値に設定します。</span><span class="sxs-lookup"><span data-stu-id="cdc49-195">To set up approvals, go to a process template, and set the **Approval** field to Default.</span></span> <span data-ttu-id="cdc49-196">それから、ジョブ求人を作成するときにそのテンプレートを選択します。</span><span class="sxs-lookup"><span data-stu-id="cdc49-196">Then select that template when you create the job.</span></span>

<span data-ttu-id="cdc49-197">ジョブ求人を保存した後、承認用に申請できます。</span><span class="sxs-lookup"><span data-stu-id="cdc49-197">After a job is saved, it can be submitted for approval.</span></span> <span data-ttu-id="cdc49-198">次の表では、承認を使用するドキュメントのステータスが一覧表示されます。</span><span class="sxs-lookup"><span data-stu-id="cdc49-198">The following table lists the statuses of a document that uses approvals.</span></span>

| <span data-ttu-id="cdc49-199">ステータス</span><span class="sxs-lookup"><span data-stu-id="cdc49-199">Status</span></span>   | <span data-ttu-id="cdc49-200">行政単位 (区画)</span><span class="sxs-lookup"><span data-stu-id="cdc49-200">State</span></span>                                                               |
|----------|---------------------------------------------------------------------|
| <span data-ttu-id="cdc49-201">ドラフト</span><span class="sxs-lookup"><span data-stu-id="cdc49-201">Draft</span></span>    | <span data-ttu-id="cdc49-202">ジョブ求人が保存されたが、まだワークフローに送信されていません。</span><span class="sxs-lookup"><span data-stu-id="cdc49-202">The job has been saved, but it hasn't been submitted to a workflow.</span></span> |
| <span data-ttu-id="cdc49-203">保留中</span><span class="sxs-lookup"><span data-stu-id="cdc49-203">Pending</span></span>  | <span data-ttu-id="cdc49-204">ジョブ求人を承認者に送信しました。</span><span class="sxs-lookup"><span data-stu-id="cdc49-204">The job has been submitted to approvers.</span></span>                            |
| <span data-ttu-id="cdc49-205">承認済</span><span class="sxs-lookup"><span data-stu-id="cdc49-205">Approved</span></span> | <span data-ttu-id="cdc49-206">ジョブ求人が承認されたが、まだ有効になっていません。</span><span class="sxs-lookup"><span data-stu-id="cdc49-206">The job has been approved, but it hasn't been activated.</span></span>            |
| <span data-ttu-id="cdc49-207">拒否済</span><span class="sxs-lookup"><span data-stu-id="cdc49-207">Rejected</span></span> | <span data-ttu-id="cdc49-208">ジョブ求人が拒否されると、有効化はできません。</span><span class="sxs-lookup"><span data-stu-id="cdc49-208">The job has been rejected, and it can't be activated.</span></span>               |
| <span data-ttu-id="cdc49-209">使用可能</span><span class="sxs-lookup"><span data-stu-id="cdc49-209">Active</span></span>   | <span data-ttu-id="cdc49-210">ジョブ求人が承認され、有効化されました。</span><span class="sxs-lookup"><span data-stu-id="cdc49-210">The job has been approved and activated.</span></span>                            |

<span data-ttu-id="cdc49-211">ジョブ求人の一覧で、ジョブ ステータスでフィルター処理できます。</span><span class="sxs-lookup"><span data-stu-id="cdc49-211">In the job list, you can filter on the job statuses.</span></span>

<span data-ttu-id="cdc49-212">承認は、会社内の任意の Microsoft Azure Active Directory(Azure AD) ユーザーに送信できます。</span><span class="sxs-lookup"><span data-stu-id="cdc49-212">Approvals can be sent to any Microsoft Azure Active Directory (Azure AD) user in the company.</span></span> <span data-ttu-id="cdc49-213">承認は、承認者として一覧表示されているすべての人に同時に送信されます。</span><span class="sxs-lookup"><span data-stu-id="cdc49-213">The approvals are sent in parallel to all the people who are listed as approvers.</span></span> <span data-ttu-id="cdc49-214">ジョブ求人が承認された後に、有効になります。</span><span class="sxs-lookup"><span data-stu-id="cdc49-214">After a job is approved, it can be activated.</span></span>

<span data-ttu-id="cdc49-215">承認者として一覧表示されている人は、Attract で承認する項目があるという通知を受け取ります。</span><span class="sxs-lookup"><span data-stu-id="cdc49-215">The people who are listed as approvers will receive a notification in Attract to inform them that they have an item to approve.</span></span> <span data-ttu-id="cdc49-216">承認項目は、ダッシュボードの**自分に割り当て済み**セクションにも表示されます。</span><span class="sxs-lookup"><span data-stu-id="cdc49-216">An approval item will also appear in the **Assigned to you** section on the dashboard.</span></span> <span data-ttu-id="cdc49-217">誰かがジョブ求人を受け入れまたは承認した後に、採用チームが通知を受け取ります。</span><span class="sxs-lookup"><span data-stu-id="cdc49-217">After someone accepts or approves a job, the hiring team will receive a notification.</span></span> <span data-ttu-id="cdc49-218">最後に、採用チームはジョブ求人が承認されたときに通知を受け取ります。</span><span class="sxs-lookup"><span data-stu-id="cdc49-218">Finally, the hiring team will receive a notification when the job is approved.</span></span>

## <a name="create-a-job"></a><span data-ttu-id="cdc49-219">職務の作成</span><span class="sxs-lookup"><span data-stu-id="cdc49-219">Create a job</span></span>

<span data-ttu-id="cdc49-220">職務を作成するには、これらの手順に従います。</span><span class="sxs-lookup"><span data-stu-id="cdc49-220">Follow these steps to create a job.</span></span>

1. <span data-ttu-id="cdc49-221">**職務**に移動します。</span><span class="sxs-lookup"><span data-stu-id="cdc49-221">Go to **Jobs**.</span></span>
2. <span data-ttu-id="cdc49-222">**新規** を選択します。</span><span class="sxs-lookup"><span data-stu-id="cdc49-222">Select **New**.</span></span>
3. <span data-ttu-id="cdc49-223">**職位**フィールドに、職位を入力します。</span><span class="sxs-lookup"><span data-stu-id="cdc49-223">In the **Job title** field, enter the job title.</span></span> <span data-ttu-id="cdc49-224">**ロール**フィールドに、ロールを入力します。</span><span class="sxs-lookup"><span data-stu-id="cdc49-224">In the **Role** field, enter your role.</span></span>
4. <span data-ttu-id="cdc49-225">**テンプレート** フィールドで、テンプレートを選択します。</span><span class="sxs-lookup"><span data-stu-id="cdc49-225">In the **Template** field, select a template.</span></span> <span data-ttu-id="cdc49-226">または、**スキップ**を選択します。</span><span class="sxs-lookup"><span data-stu-id="cdc49-226">Alternatively, select **Skip**.</span></span> <span data-ttu-id="cdc49-227">**スキップ**を選択した場合、既定のテンプレートとしてマークされているテンプレートが使用されます。</span><span class="sxs-lookup"><span data-stu-id="cdc49-227">If you select **Skip**, the template that is marked as the default template is used.</span></span>

    <span data-ttu-id="cdc49-228">ドキュメントが承認プロセスを経由する必要がある場合、**承認プロセス**フィールドを**既定値**に設定しているテンプレートを選択します。</span><span class="sxs-lookup"><span data-stu-id="cdc49-228">If the document should go through an approval process, select a template where the **Approval process** field is set to **Default**.</span></span>

5. <span data-ttu-id="cdc49-229">**詳細**タブで、職務の詳細を入力します。</span><span class="sxs-lookup"><span data-stu-id="cdc49-229">On the **Details** tab, enter the details of the job.</span></span> <span data-ttu-id="cdc49-230">**肩書き**、**職務明細書**、および**勤務地**フィールドが必須です。</span><span class="sxs-lookup"><span data-stu-id="cdc49-230">The **Title**, **Job description**, and **Location** fields are required.</span></span>
6. <span data-ttu-id="cdc49-231">**保存** を選択します。</span><span class="sxs-lookup"><span data-stu-id="cdc49-231">Select **Save**.</span></span>
7. <span data-ttu-id="cdc49-232">**採用チーム**タブで、採用マネージャー、採用担当者、または面接者を追加します。</span><span class="sxs-lookup"><span data-stu-id="cdc49-232">On the **Hiring team** tab, add a hiring manager, recruiter, or interviewer.</span></span>
8. <span data-ttu-id="cdc49-233">**保存** を選択します。</span><span class="sxs-lookup"><span data-stu-id="cdc49-233">Select **Save**.</span></span>
9. <span data-ttu-id="cdc49-234">**プロセス**タブで、必要なステージを追加または削除します。</span><span class="sxs-lookup"><span data-stu-id="cdc49-234">On the **Process** tab, add or remove stages as you require:</span></span>

    - <span data-ttu-id="cdc49-235">ステージを追加するには、**+ 新規ステージ**を選択します。</span><span class="sxs-lookup"><span data-stu-id="cdc49-235">To add a stage, select **+ New Stage**.</span></span>
    - <span data-ttu-id="cdc49-236">ステージを削除するには、ポインターをステージに移動して削除し、表示されるごみ箱ボタンを選択します。</span><span class="sxs-lookup"><span data-stu-id="cdc49-236">To remove a stage, hover the pointer over the stage to remove, and then select the trash can button that appears.</span></span>

        > [!NOTE]
        > <span data-ttu-id="cdc49-237">候補者、申請、およびオファー ステージを削除することはできません。</span><span class="sxs-lookup"><span data-stu-id="cdc49-237">The Prospect, Application, and Offer stages can't be removed.</span></span>

10. <span data-ttu-id="cdc49-238">必要に応じて、活動を追加または削除します。</span><span class="sxs-lookup"><span data-stu-id="cdc49-238">Add or remove activities as you require:</span></span>

    - <span data-ttu-id="cdc49-239">活動を追加するには、右の一覧から適切なステージにドラッグします。</span><span class="sxs-lookup"><span data-stu-id="cdc49-239">To add an activity, drag it from the list on the right to the appropriate stage.</span></span> <span data-ttu-id="cdc49-240">または、活動をダブルクリックし、それを追加するステージを選択します。</span><span class="sxs-lookup"><span data-stu-id="cdc49-240">Alternatively, double-click the activity, and then select the stage to add it to.</span></span>
    - <span data-ttu-id="cdc49-241">活動を削除するには、活動を展開し、活動ヘッダーのごみ箱ボタンを選択します。</span><span class="sxs-lookup"><span data-stu-id="cdc49-241">To remove an activity, expand the activity, and then select the trash can button on the activity header.</span></span>

11. <span data-ttu-id="cdc49-242">**保存** を選択します。</span><span class="sxs-lookup"><span data-stu-id="cdc49-242">Select **Save**.</span></span>
12. <span data-ttu-id="cdc49-243">承認プロセスを使用する選択をした場合は、次の手順に従います。</span><span class="sxs-lookup"><span data-stu-id="cdc49-243">If you selected to use an approval process, follow these steps:</span></span>

    1. <span data-ttu-id="cdc49-244">**+ 承認者の追加**を選択し、Azure AD アカウントを持つユーザーを入力します。</span><span class="sxs-lookup"><span data-stu-id="cdc49-244">Select **+ Add approver**, and then enter a user who has an Azure AD account.</span></span> <span data-ttu-id="cdc49-245">複数の承認者を追加できます。</span><span class="sxs-lookup"><span data-stu-id="cdc49-245">You can add multiple approvers.</span></span>
    2. <span data-ttu-id="cdc49-246">**承認者に送信**を選択します。</span><span class="sxs-lookup"><span data-stu-id="cdc49-246">Select **Send to approvers**.</span></span>

    <span data-ttu-id="cdc49-247">職務の**ジョブ ステータス**フィールドを**保留中**に設定します。</span><span class="sxs-lookup"><span data-stu-id="cdc49-247">The **Job status** field of the job is set to **Pending**.</span></span> <span data-ttu-id="cdc49-248">**ジョブ ステータス**フィールドの値が**承認済**に変更した後、ジョブ求人を有効化できます。</span><span class="sxs-lookup"><span data-stu-id="cdc49-248">After the value of the **Job status** field changes to **Approved**, the job can be activated.</span></span>

13. <span data-ttu-id="cdc49-249">ジョブ求人を有効にするには、**有効化**を選択します。</span><span class="sxs-lookup"><span data-stu-id="cdc49-249">To activate the job, select **Activate**.</span></span>
14. <span data-ttu-id="cdc49-250">ジョブ求人を転記するには、**転記**に移動し、Talent Careers サイトまたは LinkedIn で**今すぐ転記**を選択します。</span><span class="sxs-lookup"><span data-stu-id="cdc49-250">To post the job, go to **Postings**, and then select **Post Now** under the Talent Careers site or LinkedIn.</span></span>
