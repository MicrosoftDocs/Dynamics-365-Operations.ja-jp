---
title: Attract から LinkedIn への職務の投稿
description: このトピックでは、Dynamics 365 Talent - Attract を使用して LinkedIn に職務を転記する方法について説明します。
author: andreabichsel
manager: AnnBe
ms.date: 07/08/2019
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
ms.search.validFrom: 2019-07-08
ms.dyn365.ops.version: Platform update 24
ms.openlocfilehash: 782a2e5de6edf0e85c4d32a0910f5f3c01981a01
ms.sourcegitcommit: 9cc6a011bfdd1b0fe505760b6bf429eb6c65862a
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 11/25/2019
ms.locfileid: "2833005"
---
# <a name="post-jobs-to-linkedin-from-attract"></a><span data-ttu-id="9a465-103">Attract から LinkedIn への職務の投稿</span><span class="sxs-lookup"><span data-stu-id="9a465-103">Post jobs to LinkedIn from Attract</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="9a465-104">LinkedIn は最大のオンライン プロフェッショナル ネットワークで、世界の最高の人材へのアクセスを提供します。</span><span class="sxs-lookup"><span data-stu-id="9a465-104">LinkedIn is the largest online professional network, giving you access to the world's top talent.</span></span> <span data-ttu-id="9a465-105">Microsoft Dynamics 365 Talent: Attract では、Attract から LinkedIn に職務を直接転記できるため、必要な人材を獲得するのに役立ちます。</span><span class="sxs-lookup"><span data-stu-id="9a465-105">Microsoft Dynamics 365 Talent: Attract helps you get the talent that you need by letting you post your jobs directly from Attract to LinkedIn.</span></span>

<span data-ttu-id="9a465-106">Attract を使用すると、追加料金なしで LinkedIn に制限付き一覧を転記できます。</span><span class="sxs-lookup"><span data-stu-id="9a465-106">Attract lets you post Limited Listings to LinkedIn at no extra cost.</span></span> <span data-ttu-id="9a465-107">これらの一覧は、Attract などの LinkedIn ソフトウェア パートナーを通じてのみ利用可能です。</span><span class="sxs-lookup"><span data-stu-id="9a465-107">These listings are available only through LinkedIn software partners such as Attract.</span></span> <span data-ttu-id="9a465-108">会社の LinkedIn ページの**キャリア** パネルには有料の一覧しか表示されないため、この一覧は表示されません。</span><span class="sxs-lookup"><span data-stu-id="9a465-108">They don't appear in the **Careers** panel on your company's LinkedIn page, because only paid listings appear there.</span></span> <span data-ttu-id="9a465-109">ただし、潜在的な候補者が使用可能なすべての職務を表示する際には表示されます。</span><span class="sxs-lookup"><span data-stu-id="9a465-109">However, they are shown when potential candidates view all available jobs.</span></span> <span data-ttu-id="9a465-110">制限付き一覧は、LinkedIn の職務検索でも表示されます。</span><span class="sxs-lookup"><span data-stu-id="9a465-110">Limited Listings are also shown in LinkedIn job searches.</span></span>

<span data-ttu-id="9a465-111">Attract で[職務を作成](./creating-jobs-attract.md) した後は、ボタンを選択するだけで LinkedIn 上の何千もの潜在的な候補者の前に職務を配置することができます。</span><span class="sxs-lookup"><span data-stu-id="9a465-111">After you [create a job](./creating-jobs-attract.md) in Attract, you just have to select a button to put your job in front of thousands of potential candidates on LinkedIn.</span></span>

<span data-ttu-id="9a465-112">次の表に、ユーザー ロールに応じて LinkedIn で実行できるアクションを示します。</span><span class="sxs-lookup"><span data-stu-id="9a465-112">The following table shows the actions that you can perform on LinkedIn, depending on your user role.</span></span>

| <span data-ttu-id="9a465-113">役割</span><span class="sxs-lookup"><span data-stu-id="9a465-113">Role</span></span> | <span data-ttu-id="9a465-114">実行できるアクション</span><span class="sxs-lookup"><span data-stu-id="9a465-114">Actions that you can take</span></span> |
|---|---|
| <span data-ttu-id="9a465-115">管理者</span><span class="sxs-lookup"><span data-stu-id="9a465-115">Admin</span></span> | <span data-ttu-id="9a465-116">転記、再転記、および転記の削除</span><span class="sxs-lookup"><span data-stu-id="9a465-116">Post, repost, and unpost</span></span> |
| <span data-ttu-id="9a465-117">採用マネージャー</span><span class="sxs-lookup"><span data-stu-id="9a465-117">Hiring manager</span></span> | <span data-ttu-id="9a465-118">読み取り専用</span><span class="sxs-lookup"><span data-stu-id="9a465-118">Read only</span></span> |
| <span data-ttu-id="9a465-119">採用担当者</span><span class="sxs-lookup"><span data-stu-id="9a465-119">Recruiter</span></span> | <span data-ttu-id="9a465-120">転記、再転記、および転記の削除</span><span class="sxs-lookup"><span data-stu-id="9a465-120">Post, repost, and unpost</span></span> |
| <span data-ttu-id="9a465-121">面接者</span><span class="sxs-lookup"><span data-stu-id="9a465-121">Interviewer</span></span> | <span data-ttu-id="9a465-122">アクセス許可なし</span><span class="sxs-lookup"><span data-stu-id="9a465-122">No access</span></span> |
| <span data-ttu-id="9a465-123">読み取り専用</span><span class="sxs-lookup"><span data-stu-id="9a465-123">Read-only</span></span> | <span data-ttu-id="9a465-124">読み取り専用</span><span class="sxs-lookup"><span data-stu-id="9a465-124">Read only</span></span> |

<span data-ttu-id="9a465-125">Attract でのユーザー ロールの詳細については、[Attract でのセキュリティおよびロールの管理](./security-attract.md) を参照してください。</span><span class="sxs-lookup"><span data-stu-id="9a465-125">For more information about user roles in Attract, see [Security and role management in Attract](./security-attract.md).</span></span>

<span data-ttu-id="9a465-126">管理者として、LinkedIn と Attract の統合を構成する方法の詳細が必要な場合は、[Microsoft Dynamics 365 Talent - Attract での、LinkedIn との統合の設定](./attract-admin-linkedin.md) を参照してください。</span><span class="sxs-lookup"><span data-stu-id="9a465-126">If you're an admin and need more information about how to configure LinkedIn integration with Attract, see [Set up integration with LinkedIn for Microsoft Dynamics 365 Talent - Attract](./attract-admin-linkedin.md).</span></span>

<span data-ttu-id="9a465-127">LinkedIn に転記された職務は、ライブ LinkedIn サイトに表示されます。</span><span class="sxs-lookup"><span data-stu-id="9a465-127">Jobs that are posted to LinkedIn appear on the live LinkedIn site.</span></span> <span data-ttu-id="9a465-128">LinkedIn には職務を転記するためのテスト環境はありません。</span><span class="sxs-lookup"><span data-stu-id="9a465-128">LinkedIn doesn't have a test environment for posting jobs.</span></span> <span data-ttu-id="9a465-129">したがって、テスト ジョブを誤って転記しないように注意してください。</span><span class="sxs-lookup"><span data-stu-id="9a465-129">Therefore, make sure that you don't accidentally post any test jobs.</span></span>

## <a name="post-jobs-to-linkedin"></a><span data-ttu-id="9a465-130">LinkedIn への職務の投稿</span><span class="sxs-lookup"><span data-stu-id="9a465-130">Post jobs to LinkedIn</span></span>

1. <span data-ttu-id="9a465-131">Attract で、LinkedIn に転記する職務を開きます。</span><span class="sxs-lookup"><span data-stu-id="9a465-131">In Attract, open the job that you want to post to LinkedIn.</span></span>
2. <span data-ttu-id="9a465-132">**転記**タブで、LinkedIn に対応する**今すぐ転記**ボタンを選択します。</span><span class="sxs-lookup"><span data-stu-id="9a465-132">On the **Postings** tab, select the **Post Now** button that corresponds to LinkedIn.</span></span>

    <span data-ttu-id="9a465-133">[![Attract から LinkedIn への職務の投稿](./media/attract-post-job-to-linkedin.png)](./media/attract-post-job-to-linkedin.png)</span><span class="sxs-lookup"><span data-stu-id="9a465-133">[![Attract post job to LinkedIn](./media/attract-post-job-to-linkedin.png)](./media/attract-post-job-to-linkedin.png)</span></span>

3. <span data-ttu-id="9a465-134">**"今すぐ応募" Web アドレスの作成**ダイアログ ボックスで、**候補者は次の URL を使用して応募できます**の下にあるオプションを選択します。</span><span class="sxs-lookup"><span data-stu-id="9a465-134">In the **Create an "Apply now" web address** dialog box, select an option under **Candidates can apply using a**.</span></span> <span data-ttu-id="9a465-135">**Attract 内のリンク**を選択することをお勧めします。</span><span class="sxs-lookup"><span data-stu-id="9a465-135">We recommend that you select **Link in Attract**.</span></span>
4. <span data-ttu-id="9a465-136">**完了** を選択します。</span><span class="sxs-lookup"><span data-stu-id="9a465-136">Select **Done**.</span></span>
5. <span data-ttu-id="9a465-137">**転記を送信**メッセージ ボックスで、**確認**を選択します。</span><span class="sxs-lookup"><span data-stu-id="9a465-137">In the **Submit for posting** message box, select **Confirm**.</span></span>

<span data-ttu-id="9a465-138">LinkedIn が正常に転記を完了した後、Attract の**転記**セクションでは LinkedIn のステータスが**転記済**として表示されます。</span><span class="sxs-lookup"><span data-stu-id="9a465-138">After LinkedIn successfully completes the posting, the **Postings** section of the job in Attract shows the LinkedIn status as **Posted**.</span></span> <span data-ttu-id="9a465-139">職務が LinkedIn に表示されるまでに、最大 48 時間かかることがあります。</span><span class="sxs-lookup"><span data-stu-id="9a465-139">It can take up to 48 hours for your job to appear in LinkedIn.</span></span>

<span data-ttu-id="9a465-140">興味のある候補者が一覧の横にある**表示**を選択すると、職務の詳細と応募方法に関する情報が表示されます。</span><span class="sxs-lookup"><span data-stu-id="9a465-140">When interested candidates select **View** next to your listing, they will see the full job details, together with your information about how to apply.</span></span>

<span data-ttu-id="9a465-141">Attract を介したすべての職務の転記は、制限付き一覧です。</span><span class="sxs-lookup"><span data-stu-id="9a465-141">All job postings that are done through Attract are Limited Listings.</span></span> <span data-ttu-id="9a465-142">LinkedIn での制限付き一覧の詳細については、[求人ラッピングにおける制限付き一覧対プレミアム ジョブ スロット](https://www.linkedin.com/help/recruiter/answer/79049) を参照してください。</span><span class="sxs-lookup"><span data-stu-id="9a465-142">For more information about Limited Listings on LinkedIn, see [Limited Listings vs Premium Job Slots for Job Wrapping](https://www.linkedin.com/help/recruiter/answer/79049).</span></span>

<span data-ttu-id="9a465-143">LinkedIn へのジョブ転記に問題がある場合は、[LinkedIn と Microsoft Dynamics 365 Talent - Attract の統合に関するトラブルシューティング](./attract-troubleshoot-linkedin.md) を参照してください。</span><span class="sxs-lookup"><span data-stu-id="9a465-143">If you're having trouble posting jobs to LinkedIn, see [Troubleshooting integration with LinkedIn and Microsoft Dynamics 365 Talent - Attract](./attract-troubleshoot-linkedin.md).</span></span>

## <a name="see-also"></a><span data-ttu-id="9a465-144">参照</span><span class="sxs-lookup"><span data-stu-id="9a465-144">See also</span></span>

[<span data-ttu-id="9a465-145">LinkedIn に関するよく寄せられる質問との Attract 統合</span><span class="sxs-lookup"><span data-stu-id="9a465-145">Attract integration with LinkedIn FAQ</span></span>](./attract-linkedin-faq.md)

[<span data-ttu-id="9a465-146">Microsoft Dynamics 365 Talent - Attract の LinkedIn との統合の設定</span><span class="sxs-lookup"><span data-stu-id="9a465-146">Set up integration with LinkedIn for Microsoft Dynamics 365 Talent - Attract</span></span>](./attract-admin-linkedin.md)

[<span data-ttu-id="9a465-147">Attract でジョブ求人の作成、承認、および投稿</span><span class="sxs-lookup"><span data-stu-id="9a465-147">Create, approve, and post jobs in Attract</span></span>](./creating-jobs-attract.md)

[<span data-ttu-id="9a465-148">LinkedIn Recruiter 候補者のソーシング</span><span class="sxs-lookup"><span data-stu-id="9a465-148">Source candidates with LinkedIn Recruiter</span></span>](./attract-linkedin-recruiter.md)

[<span data-ttu-id="9a465-149">LinkedIn との統合のトラブルシューティング</span><span class="sxs-lookup"><span data-stu-id="9a465-149">Troubleshoot integration with LinkedIn</span></span>](./attract-troubleshoot-linkedin.md)
