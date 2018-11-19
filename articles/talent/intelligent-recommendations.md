---
title: "インテリジェントな推奨"
description: "このトピックでは、機械学習を使用して、職務および職務候補者の推奨事項を提供する方法について説明します。"
author: josaw
manager: AnnBe
ms.date: 10/15/2018
ms.topic: article
ms.prod: 
ms.service: dynamics-365-talent
ms.technology: 
ms.search.form: 
audience: Application User
ms.reviewer: josaw
ms.search.scope: Talent, Core
ms.custom: 7521
ms.assetid: 3b953d5f-6325-4c9e-8b9b-6ab0458a73f8
ms.search.region: Global
ms.author: rschloma
ms.search.validFrom: 2018-10-15
ms.dyn365.ops.version: Talent October 2018 update
ms.translationtype: HT
ms.sourcegitcommit: b589a6ce02cdc02436e256f9e81346fe8b766687
ms.openlocfilehash: c6225a311f5ba0b65b45092a1f626b9d6aff3f5e
ms.contentlocale: ja-jp
ms.lasthandoff: 11/12/2018

---

# <a name="intelligent-recommendations"></a><span data-ttu-id="65e8d-103">インテリジェントな推奨</span><span class="sxs-lookup"><span data-stu-id="65e8d-103">Intelligent recommendations</span></span>

[!include[banner](../includes/banner.md)]

<span data-ttu-id="65e8d-104">機械学習は、採用担当者および雇用責任者がすばやく職位のトップ候補者を特定するのに役立ちます。</span><span class="sxs-lookup"><span data-stu-id="65e8d-104">Machine learning can help recruiters and hiring managers quickly identify top candidates for a position.</span></span> <span data-ttu-id="65e8d-105">候補者が自分のプロファイルや関心事項に最も適した職位を見つけることにも役立ちます。</span><span class="sxs-lookup"><span data-stu-id="65e8d-105">It can also help prospects find the position that best suits their profile and interests.</span></span> <span data-ttu-id="65e8d-106">これらの機能が使用され、フィードバックが提供されると、推奨事項が改善されます。</span><span class="sxs-lookup"><span data-stu-id="65e8d-106">As these features are used, and feedback is provided, recommendations will improve.</span></span>

> [!NOTE] 
> - <span data-ttu-id="65e8d-107">インテリジェントな推奨機能は、包括採用アドオンでのみ使用できます。</span><span class="sxs-lookup"><span data-stu-id="65e8d-107">The intelligent recommendation features are available only with the Comprehensive hiring add-on.</span></span>
> - <span data-ttu-id="65e8d-108">候補者と職務の推奨事項の機能を有効にするには、管理者がそれらのプレビュー オプションをオンにする必要があります。</span><span class="sxs-lookup"><span data-stu-id="65e8d-108">To enable the candidate and job recommendation features, an admin must turn on the preview options for them.</span></span> <span data-ttu-id="65e8d-109">管理者センターの**機能の管理**タブで、**プレビュー機能**オプションが**オン**に設定されていることを確認します。</span><span class="sxs-lookup"><span data-stu-id="65e8d-109">In the Admin center, on the **Feature management** tab, make sure that the **Preview features** option is set to **On**.</span></span> <span data-ttu-id="65e8d-110">個々の**推奨候補者**および**推奨職務**オプションが**オン**に設定されていることを確認します。</span><span class="sxs-lookup"><span data-stu-id="65e8d-110">Then make sure that the individual **Candidate recommendation** and **Job recommendation** options are set to **On**.</span></span>

## <a name="candidate-recommendations"></a><span data-ttu-id="65e8d-111">推奨候補者</span><span class="sxs-lookup"><span data-stu-id="65e8d-111">Candidate recommendations</span></span>

<span data-ttu-id="65e8d-112">ジョブ求人には数百人の応募があるかもしれないので、スキルと背景がその職務に最も合致する候補者を見つけることは、採用担当者および雇用責任者にとって難しいかもしれません。</span><span class="sxs-lookup"><span data-stu-id="65e8d-112">Because job postings might attract hundreds of applicants, it can be difficult for recruiters and hiring managers to find the candidates whose skills and background best match the position.</span></span> <span data-ttu-id="65e8d-113">職務明細書と要件、および候補者の履歴書とプロファイルとの間の相関関係を分析することにより、機械学習を用いて推奨候補者を生成することができます。</span><span class="sxs-lookup"><span data-stu-id="65e8d-113">By analyzing the correlation between the job description and requirements, and data from the candidates' resumes and profiles, machine learning can be used to produce candidate recommendations.</span></span> <span data-ttu-id="65e8d-114">候補者の推奨は、採用担当者と雇用責任者が最高の人材を特定し、面接段階にすばやく移行するのに役立ちます。</span><span class="sxs-lookup"><span data-stu-id="65e8d-114">Candidate recommendations can help recruiters and hiring managers identify the top talent and move them to the interview stage faster.</span></span> <span data-ttu-id="65e8d-115">どの職種でも、10 名以上の候補者が履歴書やプロファイルを持っている場合は、仕事の要件を最も満たす候補者が**ジョブ**ページの**考慮する応募者**セクションに表示されます。</span><span class="sxs-lookup"><span data-stu-id="65e8d-115">For any job, if there are more than ten candidates or prospects who have resumes or complete profiles, the candidates or prospects who most closely meet the job's requirements appear in the **Applicants to consider** section on the **Job** page.</span></span>

<span data-ttu-id="65e8d-116">推奨候補者の場合は、候補者カードで**候補者の表示**を選択して、候補者のプロファイルを確認したり、候補者の応募に対する処理を行うことができます。</span><span class="sxs-lookup"><span data-stu-id="65e8d-116">For any recommended candidate, you can select **View candidate** on the candidate card to review the candidate's profile and take action on his or her application.</span></span> <span data-ttu-id="65e8d-117">省略記号ボタン (**...**) を使用して、新しいタブに候補者のプロファイルを開きます。省略記号ボタンを使用して推奨事項についてのフィードバックを提供することもできます。</span><span class="sxs-lookup"><span data-stu-id="65e8d-117">You can use the ellipsis button (**...**) to open the candidate's profile on a new tab. You can also use the ellipsis button to provide feedback about the recommendation.</span></span> <span data-ttu-id="65e8d-118">この方法によって、推薦エンジンを微調整して、将来の推奨事項を改善することができます。</span><span class="sxs-lookup"><span data-stu-id="65e8d-118">In this way, you help fine-tune the recommendation engine and improve future recommendations.</span></span> <span data-ttu-id="65e8d-119">気に入らない推奨事項は、**ジョブ**ページを更新するときに**考慮する応募者**から削除されます。</span><span class="sxs-lookup"><span data-stu-id="65e8d-119">Any recommendations that you don't like are removed from the **Applicants to consider** section when you refresh the **Job** page.</span></span> <span data-ttu-id="65e8d-120">フィードバック カードを使用して、推奨事項が役に立たなかった理由を示すことができます。</span><span class="sxs-lookup"><span data-stu-id="65e8d-120">You can use the feedback card to indicate why you didn't find the recommendation useful.</span></span>

## <a name="job-recommendations"></a><span data-ttu-id="65e8d-121">推奨職務</span><span class="sxs-lookup"><span data-stu-id="65e8d-121">Job recommendations</span></span> 

<span data-ttu-id="65e8d-122">候補者がキャリア サイトを使用して求人に応募する場合は、組織の他の空いている職位が推奨されます。</span><span class="sxs-lookup"><span data-stu-id="65e8d-122">When a prospective employee uses the career site to apply to a job, other open positions at the organization are recommended.</span></span> <span data-ttu-id="65e8d-123">これらの推奨事項は、候補者の過去の応募、および経歴書、または候補プロファイルに基づいています。</span><span class="sxs-lookup"><span data-stu-id="65e8d-123">These recommendations are based on the prospect's past applications, and on his or her resume or candidate profile.</span></span> <span data-ttu-id="65e8d-124">そのため、推奨職務は、候補者が自分に最も適した職務をすばやく見つけるのに役立ちます。</span><span class="sxs-lookup"><span data-stu-id="65e8d-124">Therefore, job recommendations help prospects quickly identify the jobs that are the best fit for them.</span></span> <span data-ttu-id="65e8d-125">推奨職務は、10 以上のジョブ求人がキャリア サイトで投稿される場合に候補者に提供されます。</span><span class="sxs-lookup"><span data-stu-id="65e8d-125">Job recommendations are provided to prospects if more than ten jobs are posted on the career site.</span></span> <span data-ttu-id="65e8d-126">候補者は、推奨事項カードから人材募集の詳細を開くことができます。</span><span class="sxs-lookup"><span data-stu-id="65e8d-126">Prospects can open the details of a job posting from the recommendation card.</span></span> <span data-ttu-id="65e8d-127">将来の推奨事項を改善するために、候補者が推奨事項に関するフィードバックを提供することもできます。</span><span class="sxs-lookup"><span data-stu-id="65e8d-127">They can also provide feedback about a recommendation to help improve future recommendations.</span></span>

