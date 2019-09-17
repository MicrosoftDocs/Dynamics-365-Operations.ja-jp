---
title: インテリジェントな推奨
description: このトピックでは、機械学習を使用して、職務および職務候補者の推奨事項を提供する方法について説明します。
author: andreabichsel
manager: AnnBe
ms.date: 05/16/2019
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
ms.author: anbichse
ms.search.validFrom: 2018-10-15
ms.dyn365.ops.version: Talent October 2018 update
ms.openlocfilehash: beb54753c50e398197353f86c2a1239a96b879eb
ms.sourcegitcommit: 45f8cea6ac75bd2f4187380546a201c056072c59
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 07/12/2019
ms.locfileid: "1741755"
---
# <a name="intelligent-recommendations"></a><span data-ttu-id="b77d2-103">インテリジェントな推奨</span><span class="sxs-lookup"><span data-stu-id="b77d2-103">Intelligent recommendations</span></span>

[!include[banner](../includes/banner.md)]

<span data-ttu-id="b77d2-104">機械学習は、採用担当者および雇用責任者がすばやく職位のトップ候補者を特定するのに役立ちます。</span><span class="sxs-lookup"><span data-stu-id="b77d2-104">Machine learning can help recruiters and hiring managers quickly identify top candidates for a position.</span></span> <span data-ttu-id="b77d2-105">候補者が自分のプロファイルや関心事項に最も適した職位を見つけることにも役立ちます。</span><span class="sxs-lookup"><span data-stu-id="b77d2-105">It can also help prospects find the position that best suits their profile and interests.</span></span> <span data-ttu-id="b77d2-106">これらの機能が使用され、フィードバックが提供されると、推奨事項が改善されます。</span><span class="sxs-lookup"><span data-stu-id="b77d2-106">As these features are used, and feedback is provided, recommendations will improve.</span></span>

> [!NOTE] 
> - <span data-ttu-id="b77d2-107">インテリジェントな推奨機能は、[包括採用アドオン](https://docs.microsoft.com/dynamics365/unified-operations/talent/attract-comprehensive-hiring) でのみ使用できます。</span><span class="sxs-lookup"><span data-stu-id="b77d2-107">The intelligent recommendation features are available only with the [Comprehensive hiring add-on](https://docs.microsoft.com/dynamics365/unified-operations/talent/attract-comprehensive-hiring).</span></span>
> - <span data-ttu-id="b77d2-108">このトピックに記載されている機能は、プレビュー レビュー リリースの一部として、対象とするユーザーが使用可能です。</span><span class="sxs-lookup"><span data-stu-id="b77d2-108">Functionality noted in this topic is available as part of a preview review release.</span></span> <span data-ttu-id="b77d2-109">コンテンツおよび機能は、変更されることがあります。</span><span class="sxs-lookup"><span data-stu-id="b77d2-109">The content and the functionality are subject to change.</span></span> <span data-ttu-id="b77d2-110">この機能を使用するには、Attract の**管理者センター**を使用して有効にするよう管理者に依頼してください。</span><span class="sxs-lookup"><span data-stu-id="b77d2-110">To use this feature, ask an administrator to enable it using the **Admin center** in Attract.</span></span> <span data-ttu-id="b77d2-111">**推奨候補者**、**推奨職務**、および**候補者の推奨事項**を**オン**に設定します。</span><span class="sxs-lookup"><span data-stu-id="b77d2-111">Set **Candidate recommendation**, **Job recommendation**, and **Prospect recommendation** to **On**.</span></span> <span data-ttu-id="b77d2-112">詳細については、[Talent のプレビュー機能の利用](./access-preview-feature.md) を参照してください。</span><span class="sxs-lookup"><span data-stu-id="b77d2-112">For more information, see [Access preview features in Talent](./access-preview-feature.md).</span></span> 


## <a name="candidate-recommendations"></a><span data-ttu-id="b77d2-113">推奨候補者</span><span class="sxs-lookup"><span data-stu-id="b77d2-113">Candidate recommendations</span></span>

<span data-ttu-id="b77d2-114">ジョブ求人には数百人の応募があるかもしれないので、スキルと背景がその職務に最も合致する候補者を見つけることは、採用担当者および雇用責任者にとって難しいかもしれません。</span><span class="sxs-lookup"><span data-stu-id="b77d2-114">Because job postings might attract hundreds of applicants, it can be difficult for recruiters and hiring managers to find the candidates whose skills and background best match the position.</span></span> <span data-ttu-id="b77d2-115">職務明細書と要件、および候補者の履歴書とプロファイルとの間の相関関係を分析することにより、機械学習を用いて推奨候補者を生成することができます。</span><span class="sxs-lookup"><span data-stu-id="b77d2-115">By analyzing the correlation between the job description and requirements, and data from the candidates' resumes and profiles, machine learning can be used to produce candidate recommendations.</span></span> <span data-ttu-id="b77d2-116">候補者の推奨は、採用担当者と雇用責任者が最高の人材を特定し、面接段階にすばやく移行するのに役立ちます。</span><span class="sxs-lookup"><span data-stu-id="b77d2-116">Candidate recommendations can help recruiters and hiring managers identify the top talent and move them to the interview stage faster.</span></span> <span data-ttu-id="b77d2-117">どの職種でも、10 名以上の候補者が履歴書やプロファイルを持っている場合は、仕事の要件を最も満たす候補者が**ジョブ**ページの**考慮する応募者**セクションに表示されます。</span><span class="sxs-lookup"><span data-stu-id="b77d2-117">For any job, if there are more than ten candidates or prospects who have resumes or complete profiles, the candidates or prospects who most closely meet the job's requirements appear in the **Applicants to consider** section on the **Job** page.</span></span>

<span data-ttu-id="b77d2-118">推奨候補者の場合は、候補者カードで**候補者の表示**を選択して、候補者のプロファイルを確認したり、候補者の応募に対する処理を行うことができます。</span><span class="sxs-lookup"><span data-stu-id="b77d2-118">For any recommended candidate, you can select **View candidate** on the candidate card to review the candidate's profile and take action on his or her application.</span></span> <span data-ttu-id="b77d2-119">省略記号ボタン (**...**) を使用して、新しいタブに候補者のプロファイルを開きます。省略記号ボタンを使用して推奨事項についてのフィードバックを提供することもできます。</span><span class="sxs-lookup"><span data-stu-id="b77d2-119">You can use the ellipsis button (**...**) to open the candidate's profile on a new tab. You can also use the ellipsis button to provide feedback about the recommendation.</span></span> <span data-ttu-id="b77d2-120">この方法によって、推薦エンジンを微調整して、将来の推奨事項を改善することができます。</span><span class="sxs-lookup"><span data-stu-id="b77d2-120">In this way, you help fine-tune the recommendation engine and improve future recommendations.</span></span> <span data-ttu-id="b77d2-121">気に入らない推奨事項は、**ジョブ**ページを更新するときに**考慮する応募者**から削除されます。</span><span class="sxs-lookup"><span data-stu-id="b77d2-121">Any recommendations that you don't like are removed from the **Applicants to consider** section when you refresh the **Job** page.</span></span> <span data-ttu-id="b77d2-122">フィードバック カードを使用して、推奨事項が役に立たなかった理由を示すことができます。</span><span class="sxs-lookup"><span data-stu-id="b77d2-122">You can use the feedback card to indicate why you didn't find the recommendation useful.</span></span>

## <a name="job-recommendations"></a><span data-ttu-id="b77d2-123">推奨職務</span><span class="sxs-lookup"><span data-stu-id="b77d2-123">Job recommendations</span></span> 

<span data-ttu-id="b77d2-124">候補者がキャリア サイトを使用して求人に応募する場合は、Attract が組織の他の空いている職位が推奨します。</span><span class="sxs-lookup"><span data-stu-id="b77d2-124">When a prospective employee uses the career site to apply to a job, Attract recommends other open positions at the organization.</span></span> <span data-ttu-id="b77d2-125">これらの推奨事項は、過去の応募、および候補者の経歴書または候補プロファイルに基づいています。</span><span class="sxs-lookup"><span data-stu-id="b77d2-125">These recommendations are based on past applications and the resume or candidate profile of the prospect.</span></span> <span data-ttu-id="b77d2-126">そのため、推奨職務は、候補者が自分に最も適した職務をすばやく見つけるのに役立ちます。</span><span class="sxs-lookup"><span data-stu-id="b77d2-126">Therefore, job recommendations help prospects quickly identify the jobs that are the best fit for them.</span></span> <span data-ttu-id="b77d2-127">推奨職務は、10 以上のジョブ求人がキャリア サイトで投稿される場合に候補者に提供されます。</span><span class="sxs-lookup"><span data-stu-id="b77d2-127">Job recommendations are provided to prospects if more than ten jobs are posted on the career site.</span></span> <span data-ttu-id="b77d2-128">候補者は、推奨事項カードから人材募集の詳細を開くことができます。</span><span class="sxs-lookup"><span data-stu-id="b77d2-128">Prospects can open the details of a job posting from the recommendation card.</span></span> <span data-ttu-id="b77d2-129">将来の推奨事項を改善するために、候補者が推奨事項に関するフィードバックを提供することもできます。</span><span class="sxs-lookup"><span data-stu-id="b77d2-129">They can also provide feedback about a recommendation to help improve future recommendations.</span></span>

## <a name="prospect-recommendations"></a><span data-ttu-id="b77d2-130">候補者の推奨事項</span><span class="sxs-lookup"><span data-stu-id="b77d2-130">Prospect recommendations</span></span> 

<span data-ttu-id="b77d2-131">新しい職位が使用可能になると、過去の申請者全員と人材ネットワーク全体を見るのに時間がかかることがあります。</span><span class="sxs-lookup"><span data-stu-id="b77d2-131">When a new position becomes available, looking through all your past applicants and your entire talent network can take a while.</span></span> <span data-ttu-id="b77d2-132">これを行うために Attract を利用するには、インテリジェントな機械学習アルゴリズムを使用できます。</span><span class="sxs-lookup"><span data-stu-id="b77d2-132">To have Attract help you do this, you can use intelligent machine learning algorithms.</span></span> <span data-ttu-id="b77d2-133">これは、ジョブ求人を作成するとすぐに Attract がすべての候補者をレビューし、よく一致する候補者を提案することを意味します。</span><span class="sxs-lookup"><span data-stu-id="b77d2-133">This means that Attract reviews all the candidates and suggests those who are a good match as soon as you create the job.</span></span> <span data-ttu-id="b77d2-134">これらの推奨事項を表示するには、職務の**候補者**ステージを有効にします。</span><span class="sxs-lookup"><span data-stu-id="b77d2-134">To view these recommendations, enable the **Prospect** stage for the job.</span></span> <span data-ttu-id="b77d2-135">Attract が候補者データベース全体をスキャンして推奨事項を作成するまでに最大 1 分かかる場合があります。</span><span class="sxs-lookup"><span data-stu-id="b77d2-135">It may take up to a minute for Attract to scan your entire candidate database to make recommendations.</span></span>

<span data-ttu-id="b77d2-136">推奨事項は、**候補者**ステージが有効である任意の職務の**候補者**タブにカードとして表示されます。</span><span class="sxs-lookup"><span data-stu-id="b77d2-136">The recommendations appear as cards in the **Prospects** tab of any job that has the **Prospect** stage enabled.</span></span> <span data-ttu-id="b77d2-137">これらのカードには候補者のプロファイルにあるスキルと、教育資格情報がリストされています。</span><span class="sxs-lookup"><span data-stu-id="b77d2-137">These cards list the skills found in the prospect's profile, as well as any education qualification information.</span></span> <span data-ttu-id="b77d2-138">必要な推薦事項を見つけた場合は、その職務の候補者として候補者を追加することができます。</span><span class="sxs-lookup"><span data-stu-id="b77d2-138">If you find a recommendation that you like, you can add the candidate as a prospect for that job.</span></span>

> [!NOTE]
> <span data-ttu-id="b77d2-139">最近 Attract を使用し始めた場合は、この機能を使用する前に、完全なプロファイルまたは履歴書を持つ 10 人以上の申請者ができるまで待つ必要があります。</span><span class="sxs-lookup"><span data-stu-id="b77d2-139">If you recently started using Attract, you’ll need to wait until you have 10 or more applicants who have full profiles or resumes before you can use this capability.</span></span>

<span data-ttu-id="b77d2-140">推奨事項の潜在的な偏りを避けるために、Attract はスキル、資格、および職務記述説明に一致するその他のキーワードに対する候補者プロファイルのみをスキャンします。</span><span class="sxs-lookup"><span data-stu-id="b77d2-140">To avoid potential bias in the recommendations, Attract only scans candidate profiles for skills, qualifications, and other keywords that match the job description.</span></span> <span data-ttu-id="b77d2-141">さらに、Attract は、評価前に候補者プロファイルから個人を特定する情報を削除します。</span><span class="sxs-lookup"><span data-stu-id="b77d2-141">In addition, Attract removes personally identifying information from candidate profiles prior to evaluation.</span></span>
