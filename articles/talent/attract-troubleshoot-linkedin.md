---
title: LinkedIn と Microsoft Dynamics 365 Talent - Attract との統合のトラブルシューティング
description: このトピックでは、Microsoft Dynamics 365 Talent - Attract から LinkedIn に職務を転記する際の問題をトラブルシューティングする方法について説明します。
author: andreabichsel
manager: AnnBe
ms.date: 06/04/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-talent
ms.technology: ''
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Core, Talent
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: anbichse
ms.search.validFrom: 2019-06-04
ms.dyn365.ops.version: Platform update 24
ms.openlocfilehash: 79f138ad9aeb203bce19cc93237fca96bffd015f
ms.sourcegitcommit: 434dd21450bddcd891aba0555b9853d9ba0afb6f
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 09/23/2019
ms.locfileid: "2008223"
---
# <a name="troubleshoot-integration-with-linkedin"></a><span data-ttu-id="c45f8-103">LinkedIn との統合のトラブルシューティング</span><span class="sxs-lookup"><span data-stu-id="c45f8-103">Troubleshoot integration with LinkedIn</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="c45f8-104">次の情報は、Microsoft Dynamics 365 Talent: Attract から LinkedIn に職務を転記する際に発生する可能性のある問題のトラブルシューティングに役立ちます。</span><span class="sxs-lookup"><span data-stu-id="c45f8-104">Use the following information to help troubleshoot issues that you might have when you try to post jobs to LinkedIn from Microsoft Dynamics 365 Talent: Attract.</span></span>

## <a name="you-cant-sign-in-to-linkedin-from-attract"></a><span data-ttu-id="c45f8-105">Attract から LinkedIn にサイン インできない</span><span class="sxs-lookup"><span data-stu-id="c45f8-105">You can't sign in to LinkedIn from Attract</span></span>

<span data-ttu-id="c45f8-106">Attract から LinkedIn にサイン インできない場合は、次の手順をお試しください。</span><span class="sxs-lookup"><span data-stu-id="c45f8-106">If you're having trouble signing in to LinkedIn from Attract, try these steps:</span></span>

1. <span data-ttu-id="c45f8-107">Attract で入力した LinkedIn の資格情報が有効で正しいことを確認します。</span><span class="sxs-lookup"><span data-stu-id="c45f8-107">Verify that the LinkedIn credentials that you entered in Attract are valid and correct.</span></span>
2. <span data-ttu-id="c45f8-108">資格情報が有効で正しい場合、[LinkedIn サポート](https://www.linkedin.com/help/linkedin) にお問い合わせください。</span><span class="sxs-lookup"><span data-stu-id="c45f8-108">If the credentials are valid and correct, contact [LinkedIn support](https://www.linkedin.com/help/linkedin).</span></span>
3. <span data-ttu-id="c45f8-109">問題が解消しない場合は、[Microsoft サポート](./talent-support.md) にお問い合わせください。</span><span class="sxs-lookup"><span data-stu-id="c45f8-109">If the issue persists, contact [Microsoft support](./talent-support.md).</span></span>

## <a name="job-posts-from-attract-dont-appear-on-linkedin"></a><span data-ttu-id="c45f8-110">Attract からの職務の転記が LinkedIn に表示されない</span><span class="sxs-lookup"><span data-stu-id="c45f8-110">Job posts from Attract don't appear on LinkedIn</span></span>

<span data-ttu-id="c45f8-111">24 時間経過後も LinkedIn に職務が表示されていない場合は、次の手順をお試しください。</span><span class="sxs-lookup"><span data-stu-id="c45f8-111">If your job hasn't appeared on LinkedIn after 24 hours, try these steps:</span></span>

1. <span data-ttu-id="c45f8-112">LinkedIn 会社 ID が LinkedIn 会社ページにマップされ、Attract 管理センターに正しく入力されていることを確認します。</span><span class="sxs-lookup"><span data-stu-id="c45f8-112">Make sure that your LinkedIn Company ID maps to your LinkedIn company page and is correctly entered in the Attract Admin center.</span></span> <span data-ttu-id="c45f8-113">管理センターで LinkedIn 設定を変更する方法の詳細については、[LinkedIn との統合を設定する](attract-admin-linkedin.md) を参照してください。</span><span class="sxs-lookup"><span data-stu-id="c45f8-113">For more information about how to change LinkedIn settings in the Admin center, see [Set up integration with LinkedIn](attract-admin-linkedin.md).</span></span> <span data-ttu-id="c45f8-114">LinkedIn 会社 ID の詳細については、[Linkedln 会社 ID を Linkedln 職務ボードに関連付ける - よく寄せられる質問](https://www.linkedin.com/help/linkedin/answer/98972) を参照してください。</span><span class="sxs-lookup"><span data-stu-id="c45f8-114">For more information about LinkedIn Company IDs, see [Associating your LinkedIn Company ID with the LinkedIn Job Board - Frequently Asked Questions](https://www.linkedin.com/help/linkedin/answer/98972).</span></span>
2. <span data-ttu-id="c45f8-115">LinkedIn の職務の詳細を確認して、アドレスが完全であることを確認します。</span><span class="sxs-lookup"><span data-stu-id="c45f8-115">Check the job details on LinkedIn to make sure that the address is complete.</span></span> <span data-ttu-id="c45f8-116">LinkedIn が職務を正常に転記するには、少なくともその職務の都市と国または地域が必要です。</span><span class="sxs-lookup"><span data-stu-id="c45f8-116">To post a job successfully, LinkedIn needs at least the city and country or region of the job.</span></span>
3. <span data-ttu-id="c45f8-117">職務が LinkedIn に転記されている別の職務と重複していないことを確認します。</span><span class="sxs-lookup"><span data-stu-id="c45f8-117">Make sure that the job doesn't duplicate another job that has been posted on LinkedIn.</span></span> <span data-ttu-id="c45f8-118">LinkedInは、LinkedIn プレミアム ジョブ スロットまたは別のソースからの限定付き一覧のいずれかと重複する職務を投稿しません。</span><span class="sxs-lookup"><span data-stu-id="c45f8-118">LinkedIn won't post jobs that are duplicates of either LinkedIn Premium Job Slots or Limited Listings from another source.</span></span> <span data-ttu-id="c45f8-119">会社の別のユーザーが、まだ手動で職務を転記していないことを確認します。</span><span class="sxs-lookup"><span data-stu-id="c45f8-119">Verify that another person at your company didn't already post the job manually.</span></span>

## <a name="see-also"></a><span data-ttu-id="c45f8-120">参照</span><span class="sxs-lookup"><span data-stu-id="c45f8-120">See also</span></span>

[<span data-ttu-id="c45f8-121">LinkedIn に関するよく寄せられる質問</span><span class="sxs-lookup"><span data-stu-id="c45f8-121">LinkedIn FAQ</span></span>](./attract-linkedin-faq.md)

[<span data-ttu-id="c45f8-122">Attract から LinkedIn への職務の投稿</span><span class="sxs-lookup"><span data-stu-id="c45f8-122">Post jobs to LinkedIn from Attract</span></span>](./attract-post-jobs-to-linkedin.md)

[<span data-ttu-id="c45f8-123">LinkedIn Recruiter での候補者のソーシング</span><span class="sxs-lookup"><span data-stu-id="c45f8-123">Source candidates with LinkedIn Recruiter</span></span>](./attract-linkedin-recruiter.md)

[<span data-ttu-id="c45f8-124">職務の作成</span><span class="sxs-lookup"><span data-stu-id="c45f8-124">Create jobs</span></span>](./creating-jobs-attract.md)

[<span data-ttu-id="c45f8-125">LinkedIn との統合のトラブルシューティング</span><span class="sxs-lookup"><span data-stu-id="c45f8-125">Troubleshoot integration with LinkedIn</span></span>](./attract-troubleshoot-linkedin.md)
