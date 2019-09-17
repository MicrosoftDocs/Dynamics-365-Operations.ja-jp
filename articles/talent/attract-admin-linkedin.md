---
title: AMicrosoft Dynamics 365 for Talent - Attract の Linkedln との統合の設定
description: このトピックでは、Attract から Linkedln にジョブを簡単に転記し、採用担当者が候補者の Linkedln プロファイルと採用情報を同期できるように、Microsoft Dynamics 365 for Talent - Attract の Linkedln 統合のコンフィギュレーション方法を説明します。
author: andreabichsel
manager: AnnBe
ms.date: 07/08/2019
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
ms.search.validFrom: 2019-07-08
ms.dyn365.ops.version: Talent October 2018 update
ms.openlocfilehash: 8e42ec7d0bb74089b4e915b5a30277401e694cf9
ms.sourcegitcommit: c62756cb04549b2ff5de9b93d497e964a340335a
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 07/17/2019
ms.locfileid: "1756225"
---
# <a name="set-up-linkedin-integration"></a><span data-ttu-id="2eca6-103">LinkedIn 統合の設定</span><span class="sxs-lookup"><span data-stu-id="2eca6-103">Set up LinkedIn integration</span></span>

[!include[banner](../includes/banner.md)]

<span data-ttu-id="2eca6-104">採用担当者および採用マネージャーが、Microsoft Dynamics 365 for Talent: Attract と LinkedIn 統合をコンフィギュレーション構成して、主なスキルをご提供します。</span><span class="sxs-lookup"><span data-stu-id="2eca6-104">Help your recruiters and hiring managers attract top talent by configuring LinkedIn integration with Microsoft Dynamics 365 for Talent: Attract.</span></span> <span data-ttu-id="2eca6-105">Attract では、ジョブを最大の本格的なオンライン ネットワークである LinkedIn に直接転記できます。</span><span class="sxs-lookup"><span data-stu-id="2eca6-105">Attract lets you post jobs directly to LinkedIn, the largest professional online network.</span></span>

<span data-ttu-id="2eca6-106">Attract を通して LinkedIn に転記したジョブは、制限付き一覧であり、会社に対して追加の費用が発生することはありません。</span><span class="sxs-lookup"><span data-stu-id="2eca6-106">Jobs that you post to LinkedIn through Attract are Limited Listings and are provided at no extra cost to your company.</span></span> <span data-ttu-id="2eca6-107">これらの一覧は、Attract などの LinkedIn ソフトウェア パートナーを通じてのみ利用可能です。</span><span class="sxs-lookup"><span data-stu-id="2eca6-107">These listings are available only through LinkedIn software partners such as Attract.</span></span> <span data-ttu-id="2eca6-108">会社の LinkedIn ページの**キャリア** パネルには有料の一覧しか表示されないため、この一覧は表示されません。</span><span class="sxs-lookup"><span data-stu-id="2eca6-108">They don't appear in the **Careers** panel on your company's LinkedIn page, because only paid listings appear there.</span></span> <span data-ttu-id="2eca6-109">ただし、潜在的な候補者が使用可能なすべての職務を表示する際には表示されます。</span><span class="sxs-lookup"><span data-stu-id="2eca6-109">However, they are shown when potential candidates view all available jobs.</span></span> <span data-ttu-id="2eca6-110">制限付き一覧は、LinkedIn の職務検索でも表示されます。</span><span class="sxs-lookup"><span data-stu-id="2eca6-110">Limited Listings are also shown in LinkedIn job searches.</span></span>

<span data-ttu-id="2eca6-111">Attract では、この人気のあるキャリア サイトからの応募者を探すのに役立つ LinkedIn と統合する方法を 2 とおり用意しています。</span><span class="sxs-lookup"><span data-stu-id="2eca6-111">Attract provides two ways to integrate with LinkedIn to help you source candidates from this popular career site:</span></span>

- <span data-ttu-id="2eca6-112">Attract から LinkedIn へジョブを転記します。</span><span class="sxs-lookup"><span data-stu-id="2eca6-112">Post jobs from Attract to LinkedIn.</span></span>
- <span data-ttu-id="2eca6-113">Attract から LinkedIn へ候補者をソーシングします。</span><span class="sxs-lookup"><span data-stu-id="2eca6-113">Source candidates from LinkedIn to Attract.</span></span>

<span data-ttu-id="2eca6-114">両方のオプションを、管理者センターの **LinkedIn 統合**タブで構成します。</span><span class="sxs-lookup"><span data-stu-id="2eca6-114">You configure both options on the **LinkedIn Integration** tab in the Admin center.</span></span> <span data-ttu-id="2eca6-115">管理センターを開くには、<https://attract.talent.dynamics.com/adminsettings> へ移動します。</span><span class="sxs-lookup"><span data-stu-id="2eca6-115">To open the Admin center, go to <https://attract.talent.dynamics.com/adminsettings>.</span></span>

> [!NOTE]
> <span data-ttu-id="2eca6-116">Attract で LinkedIn Recruiter 統合を使用するには、[包括採用アドオン](https://docs.microsoft.com/dynamics365/unified-operations/talent/attract-comprehensive-hiring) および [LinkedIn Recruiter ライセンス](https://business.linkedin.com/talent-solutions/cx/17/08/recruiter-demo-fs2-k18) が必要です。</span><span class="sxs-lookup"><span data-stu-id="2eca6-116">To use LinkedIn Recruiter integration with Attract, you need the [Comprehensive hiring add-on](https://docs.microsoft.com/dynamics365/unified-operations/talent/attract-comprehensive-hiring) and [LinkedIn Recruiter licenses](https://business.linkedin.com/talent-solutions/cx/17/08/recruiter-demo-fs2-k18).</span></span> <span data-ttu-id="2eca6-117">詳細については、[Attract のバージョンは何ですか](./attract-comprehensive-hiring.md) を参照してください。</span><span class="sxs-lookup"><span data-stu-id="2eca6-117">For more information, see [Which version of Attract?](./attract-comprehensive-hiring.md).</span></span>

<span data-ttu-id="2eca6-118">LinkedIn へのジョブ転記に問題がある場合は、[Linkedln で統合によるトラブルシューティング](./attract-troubleshoot-linkedin.md) を参照してください。</span><span class="sxs-lookup"><span data-stu-id="2eca6-118">If you're having trouble posting jobs to LinkedIn, see [Troubleshoot integration with LinkedIn](./attract-troubleshoot-linkedin.md).</span></span>

<span data-ttu-id="2eca6-119">LinkedIn にジョブ転記するための他の方法については、[Linkedln に関するよく寄せられる質問](./attract-linkedin-faq.md) を参照してください。</span><span class="sxs-lookup"><span data-stu-id="2eca6-119">For information about other ways to post jobs to LinkedIn, see [LinkedIn FAQ](./attract-linkedin-faq.md).</span></span>

## <a name="configure-job-posting-to-linkedin"></a><span data-ttu-id="2eca6-120">LinkedIn へのジョブ転記のコンフィギュレーション</span><span class="sxs-lookup"><span data-stu-id="2eca6-120">Configure job posting to LinkedIn</span></span>

<span data-ttu-id="2eca6-121">Attract から LinkedIn にジョブ転記する前に、[Linkedln 社の ID](https://aka.ms/findID) が必要です。</span><span class="sxs-lookup"><span data-stu-id="2eca6-121">Before you can post jobs from Attract to LinkedIn, you need a [LinkedIn Company ID](https://aka.ms/findID).</span></span> <span data-ttu-id="2eca6-122">LinkedIn 社の ID は、LinkedIn で会社を固有に識別する文字列です。</span><span class="sxs-lookup"><span data-stu-id="2eca6-122">Your LinkedIn Company ID is a string of numbers that uniquely identifies your company in LinkedIn.</span></span> <span data-ttu-id="2eca6-123">詳細については、[Linkedln 社の ID を Linkedln 職務ボードに関連付ける - よく寄せられる質問](https://aka.ms/findID) を参照してください。</span><span class="sxs-lookup"><span data-stu-id="2eca6-123">For more information, see [Associating your LinkedIn Company ID with the LinkedIn Job Board - Frequently Asked Questions](https://aka.ms/findID).</span></span>

<span data-ttu-id="2eca6-124">Attract では、ジョブ転記のフィードが LinkedIn に送信され、1 日に 1 回ほどフィードがチェックされます。</span><span class="sxs-lookup"><span data-stu-id="2eca6-124">Attract sends a feed of your job postings to LinkedIn, and LinkedIn checks for the feed approximately once per day.</span></span> <span data-ttu-id="2eca6-125">ジョブをサイトに転記するのに、最大 48 時間かかります。</span><span class="sxs-lookup"><span data-stu-id="2eca6-125">It can take up to 48 hours for your jobs to be posted to the site.</span></span>

<span data-ttu-id="2eca6-126">LinkedIn に転記された職務は、ライブ LinkedIn サイトに表示されます。</span><span class="sxs-lookup"><span data-stu-id="2eca6-126">Jobs that are posted to LinkedIn appear on the live LinkedIn site.</span></span> <span data-ttu-id="2eca6-127">LinkedIn には職務を転記するためのテスト環境はありません。</span><span class="sxs-lookup"><span data-stu-id="2eca6-127">LinkedIn doesn't have a test environment for posting jobs.</span></span> <span data-ttu-id="2eca6-128">したがって、テスト ジョブを誤って転記しないように注意してください。</span><span class="sxs-lookup"><span data-stu-id="2eca6-128">Therefore, make sure that you don't accidentally post any test jobs.</span></span> 

1. <span data-ttu-id="2eca6-129">右上隅の**設定**メニュー (ギヤ記号) で、**管理センター**を選択します。</span><span class="sxs-lookup"><span data-stu-id="2eca6-129">On the **Setup** menu (the gear symbol) in the upper-right corner, select **Admin center**.</span></span> <span data-ttu-id="2eca6-130">または、<https://attract.talent.dynamics.com/adminsettings> を参照してください。</span><span class="sxs-lookup"><span data-stu-id="2eca6-130">Alternatively, go to <https://attract.talent.dynamics.com/adminsettings>.</span></span>
2. <span data-ttu-id="2eca6-131">**Linkedln 統合**タブを選択します。</span><span class="sxs-lookup"><span data-stu-id="2eca6-131">Select the **LinkedIn Integration** tab.</span></span>
3. <span data-ttu-id="2eca6-132">**会社名**に会社名を入力し、**会社の ID** に LinkedIn 社の ID を入力します。</span><span class="sxs-lookup"><span data-stu-id="2eca6-132">Under **Company name**, enter the name of your company, and under **Company ID**, enter your LinkedIn Company ID.</span></span> <span data-ttu-id="2eca6-133">会社名が、会社の LinkedIn ページに表示される名前と一致していることを確認してください。</span><span class="sxs-lookup"><span data-stu-id="2eca6-133">Make sure that the company name matches the name that appears on your company's LinkedIn page.</span></span> <span data-ttu-id="2eca6-134">LinkedIn 会社 ID の詳細については、[Linkedln 会社 ID を Linkedln 職務ボードに関連付ける - よく寄せられる質問](https://www.linkedin.com/help/linkedin/answer/98972) を参照してください。</span><span class="sxs-lookup"><span data-stu-id="2eca6-134">For more information about LinkedIn Company IDs, see [Associating your LinkedIn Company ID with the LinkedIn Job Board - Frequently Asked Questions](https://www.linkedin.com/help/linkedin/answer/98972).</span></span>

    <span data-ttu-id="2eca6-135">組織に関する情報を変更する必要がある場合は、[組織の住所、技術連絡先などの変更](https://docs.microsoft.com/office365/admin/manage/change-address-contact-and-more) を参照してください。</span><span class="sxs-lookup"><span data-stu-id="2eca6-135">If you need to change any information for your organization, see [Change your organization's address, technical contact, and more](https://docs.microsoft.com/office365/admin/manage/change-address-contact-and-more).</span></span> <span data-ttu-id="2eca6-136">問題が解決しない場合は、[LinkedIn サポート](https://www.linkedin.com/help/linkedin) に連絡してください。</span><span class="sxs-lookup"><span data-stu-id="2eca6-136">If you still have issues, contact [LinkedIn support](https://www.linkedin.com/help/linkedin).</span></span>

4. <span data-ttu-id="2eca6-137">**保存** を選択します。</span><span class="sxs-lookup"><span data-stu-id="2eca6-137">Select **Save**.</span></span>

## <a name="set-up-linkedin-recruiter-with-attract"></a><span data-ttu-id="2eca6-138">Attract で LinkedIn Recruiter を設定</span><span class="sxs-lookup"><span data-stu-id="2eca6-138">Set up LinkedIn Recruiter with Attract</span></span> 

<span data-ttu-id="2eca6-139">採用担当者が LinkedIn Recruiter を介してジョブを調達するには、Attract の LinkedIn Recruiter と統合をコンフィギュレーションする必要があります。</span><span class="sxs-lookup"><span data-stu-id="2eca6-139">To allow recruiters to source jobs through LinkedIn Recruiter, you must configure integration with LinkedIn Recruiter in Attract.</span></span> <span data-ttu-id="2eca6-140">コンフィギュレーション プロセスを完了するには、組織の LinkedIn Recruiter 契約の管理者であるユーザーを処理する必要があります。</span><span class="sxs-lookup"><span data-stu-id="2eca6-140">To complete the configuration process, you must work with the user who is an admin on your organization's LinkedIn Recruiter contract.</span></span>

1. <span data-ttu-id="2eca6-141">右上隅の**設定**メニュー (ギヤ記号) で、**管理センター**を選択します。</span><span class="sxs-lookup"><span data-stu-id="2eca6-141">On the **Setup** menu (the gear symbol) in the upper-right corner, select **Admin center**.</span></span> <span data-ttu-id="2eca6-142">または、<https://attract.talent.dynamics.com/adminsettings> を参照してください。</span><span class="sxs-lookup"><span data-stu-id="2eca6-142">Alternatively, go to <https://attract.talent.dynamics.com/adminsettings>.</span></span>
2. <span data-ttu-id="2eca6-143">**Linkedln 統合**タブを選択します。</span><span class="sxs-lookup"><span data-stu-id="2eca6-143">Select the **LinkedIn Integration** tab.</span></span>

    <span data-ttu-id="2eca6-144">[![ LinkedIn Recruiter 統合を開始する Attract 管理者ビュー](./media/LinkedInConnect.png)](./media/LinkedInConnect.png)</span><span class="sxs-lookup"><span data-stu-id="2eca6-144">[![Attract Admin view to start LinkedIn Recruiter integration](./media/LinkedInConnect.png)](./media/LinkedInConnect.png)</span></span>

3. <span data-ttu-id="2eca6-145">**接続**を選択して、設定を開始します。</span><span class="sxs-lookup"><span data-stu-id="2eca6-145">Select **Connect** to start the setup.</span></span> <span data-ttu-id="2eca6-146">LinkedIn の登録手続きについての案内が表示されます。</span><span class="sxs-lookup"><span data-stu-id="2eca6-146">You will be guided through the LinkedIn sign-in process.</span></span>
4. <span data-ttu-id="2eca6-147">複数の LinkedIn 契約に関する席数を使用する場合は、Attract システムにする契約を選択します。</span><span class="sxs-lookup"><span data-stu-id="2eca6-147">If you have seats on multiple LinkedIn contracts, select the contract that you want to connect to the Attract system.</span></span> <span data-ttu-id="2eca6-148">1 つの LinkedIn 契約のみの場合、この手順をスキップできます。</span><span class="sxs-lookup"><span data-stu-id="2eca6-148">If you have a seat on only one LinkedIn contract, you can skip this step.</span></span>
5. <span data-ttu-id="2eca6-149">**Recruiter System Connect (RSC)** で、**要求**を選択します。</span><span class="sxs-lookup"><span data-stu-id="2eca6-149">Under **Recruiter System Connect (RSC)**, select **Request**.</span></span>

    <span data-ttu-id="2eca6-150">[![ LinkedIn Recruiter 統合を要求する Attract 管理者ビュー](./media/RequestLinkedInRSC.png)](./media/RequestLinkedInRSC.png)</span><span class="sxs-lookup"><span data-stu-id="2eca6-150">[![Attract Admin view to Request LinkedIn Recruiter integration](./media/RequestLinkedInRSC.png)](./media/RequestLinkedInRSC.png)</span></span>

6. <span data-ttu-id="2eca6-151">**Recruiter System Connect (RSC)** 設定は、**パートナー準備完了**として表示されるようになります。</span><span class="sxs-lookup"><span data-stu-id="2eca6-151">The **Recruiter System Connect (RSC)** setting should now appear as **Partner ready**.</span></span> <span data-ttu-id="2eca6-152">このページで**通知パートナー**が表示されたら、しばらく待ち、**通知パートナー**を選択してページを最新の情報に更新します。</span><span class="sxs-lookup"><span data-stu-id="2eca6-152">If you see **Notify partner** on this page, wait a few seconds, select **Notify partner**, and then refresh the page.</span></span> <span data-ttu-id="2eca6-153">これで設定が、**パートナー準備完了**に表示されます。</span><span class="sxs-lookup"><span data-stu-id="2eca6-153">The setting should now appear as **Partner ready**.</span></span>

    <span data-ttu-id="2eca6-154">[![完了した要求の Attract 側を示す Attract 管理者ビュー](./media/PartnerReadyRSC.png)](./media/PartnerReadyRSC.png)</span><span class="sxs-lookup"><span data-stu-id="2eca6-154">[![Attract Admin view to indicate Attract side of requests have been completed](./media/PartnerReadyRSC.png)](./media/PartnerReadyRSC.png)</span></span>

7. <span data-ttu-id="2eca6-155">以下の手順を完了するには、LinkedIn Recruiter 契約に関する管理特権が必要です。</span><span class="sxs-lookup"><span data-stu-id="2eca6-155">To complete the following steps, you must have admin privileges on your LinkedIn Recruiter contract.</span></span>

    1. <span data-ttu-id="2eca6-156">自分の管理者アカウントを使用して LinkedIn にログインし、画面右上の **LinkedIn Recruiter** を選択します。</span><span class="sxs-lookup"><span data-stu-id="2eca6-156">Sign in to LinkedIn by using your admin account, and then select **LinkedIn Recruiter** in the upper right.</span></span> 
    2. <span data-ttu-id="2eca6-157">ページ上部にある**詳細**メニューで、**管理者設定**を選択してから **ATS** タブを選択します。</span><span class="sxs-lookup"><span data-stu-id="2eca6-157">On the **More** menu at the top of the page, select **Admin Settings**, and then select the **ATS** tab.</span></span>
    3. <span data-ttu-id="2eca6-158">1 つの契約に対して 1 回のエクスポートを有効にするには、**契約レベルのアクセス (この契約を使用するすべての座席に対して)** をオンにします。</span><span class="sxs-lookup"><span data-stu-id="2eca6-158">To enable one-click export for just one contract, turn on **Contract Level access (for every seat on this contract**.</span></span> <span data-ttu-id="2eca6-159">会社全体でこの機能を有効にするには、**会社レベルのアクセス (会社内のすべての契約に対して)** をオンにします。</span><span class="sxs-lookup"><span data-stu-id="2eca6-159">To enable it for the whole company, turn on **Company Level access (for every contract in your company**.</span></span>

    <span data-ttu-id="2eca6-160">[![LinkedIn Recruiter の管理者ビューから Attract 統合にオン](./media/EnableRSC.png)](./media/EnableRSC.png)</span><span class="sxs-lookup"><span data-stu-id="2eca6-160">[![Turn on Attract integration from LinkedIn Recruiter Admin view](./media/EnableRSC.png)](./media/EnableRSC.png)</span></span>

8. <span data-ttu-id="2eca6-161">Attract 管理センターで、**LinkedIn 統合**タブを選択します。**Recruiter System Connect (RSC)** の設定が、**有効**と表示されます。</span><span class="sxs-lookup"><span data-stu-id="2eca6-161">In the Attract Admin center, select the **LinkedIn integration** tab. The **Recruiter System Connect (RSC)** setting should now appear as **Enabled**.</span></span>

    <span data-ttu-id="2eca6-162">[![LinkedIn Recruiter 統合の完了](./media/RSCSetupComplete.png)](./media/RSCSetupComplete.png)</span><span class="sxs-lookup"><span data-stu-id="2eca6-162">[![LinkedIn Recruiter integration complete](./media/RSCSetupComplete.png)](./media/RSCSetupComplete.png)</span></span>

## <a name="set-up-apply-with-linkedin-in-attract"></a><span data-ttu-id="2eca6-163">Attract と LinkedIn で適用を設定</span><span class="sxs-lookup"><span data-stu-id="2eca6-163">Set up Apply with LinkedIn in Attract</span></span>

<span data-ttu-id="2eca6-164">自分の LinkedIn プロファイルを使用して、ジョブに応募を許可することができます。</span><span class="sxs-lookup"><span data-stu-id="2eca6-164">You can allow candidates to apply to your jobs by using their LinkedIn profiles.</span></span> <span data-ttu-id="2eca6-165">LinkedIn の適用に関しては、[すべての場所における Linkedln の機能 - Linkedln の適用](https://blog.linkedin.com/2011/07/24/apply-with-linkedin) を参照してください。</span><span class="sxs-lookup"><span data-stu-id="2eca6-165">For more information about Apply with LinkedIn, see [The Power of LinkedIn Everywhere: Apply with LinkedIn](https://blog.linkedin.com/2011/07/24/apply-with-linkedin).</span></span>

<span data-ttu-id="2eca6-166">現在プレビューにある機能です。</span><span class="sxs-lookup"><span data-stu-id="2eca6-166">This feature is currently in preview.</span></span> <span data-ttu-id="2eca6-167">この手順を実行する前に、LinkedIn の適用が有効になっていることを確認してください。</span><span class="sxs-lookup"><span data-stu-id="2eca6-167">Before you follow these steps, make sure that Apply with LinkedIn is enabled.</span></span> <span data-ttu-id="2eca6-168">プレビュー機能の有効化についての詳細は、[Talent のプレビュー機能の利用](./access-preview-feature.md) を参照してください。</span><span class="sxs-lookup"><span data-stu-id="2eca6-168">For more information about how to enable preview features, see [Access preview features in Talent](./access-preview-feature.md).</span></span>

1. <span data-ttu-id="2eca6-169">右上隅の**設定**メニュー (ギヤ記号) で、**管理センター**を選択します。</span><span class="sxs-lookup"><span data-stu-id="2eca6-169">On the **Setup** menu (the gear symbol) in the upper-right corner, select **Admin center**.</span></span> <span data-ttu-id="2eca6-170">または、<https://attract.talent.dynamics.com/adminsettings> を参照してください。</span><span class="sxs-lookup"><span data-stu-id="2eca6-170">Alternatively, go to <https://attract.talent.dynamics.com/adminsettings>.</span></span>
2. <span data-ttu-id="2eca6-171">**Linkedln 統合**タブを選択します。</span><span class="sxs-lookup"><span data-stu-id="2eca6-171">Select the **LinkedIn Integration** tab.</span></span>

    <span data-ttu-id="2eca6-172">[![ LinkedIn Recruiter 統合を開始する Attract 管理者ビュー](./media/LinkedInConnect.png)](./media/LinkedInConnect.png)</span><span class="sxs-lookup"><span data-stu-id="2eca6-172">[![Attract Admin view to start LinkedIn Recruiter integration](./media/LinkedInConnect.png)](./media/LinkedInConnect.png)</span></span>

3. <span data-ttu-id="2eca6-173">**LinkedIn の適用**の横にある**接続**を選択して、設定を開始します。</span><span class="sxs-lookup"><span data-stu-id="2eca6-173">Next to **Apply with LinkedIn**, select **Connect** to start the setup.</span></span> <span data-ttu-id="2eca6-174">LinkedIn の残りのプロセスについての案内が表示されます。</span><span class="sxs-lookup"><span data-stu-id="2eca6-174">You will be guided through the rest of the process with LinkedIn.</span></span>

## <a name="see-also"></a><span data-ttu-id="2eca6-175">参照</span><span class="sxs-lookup"><span data-stu-id="2eca6-175">See also</span></span>

[<span data-ttu-id="2eca6-176">LinkedIn に関するよく寄せられる質問</span><span class="sxs-lookup"><span data-stu-id="2eca6-176">LinkedIn FAQ</span></span>](./attract-linkedin-faq.md)

[<span data-ttu-id="2eca6-177">Attract から外部サイトへの求人の投稿</span><span class="sxs-lookup"><span data-stu-id="2eca6-177">Post jobs to external sites from Attract</span></span>](./posting-jobs-external.md)

[<span data-ttu-id="2eca6-178">LinkedIn Recruiter 候補者のソーシング</span><span class="sxs-lookup"><span data-stu-id="2eca6-178">Source candidates with LinkedIn Recruiter</span></span>](./attract-linkedin-recruiter.md)

[<span data-ttu-id="2eca6-179">ジョブの作成</span><span class="sxs-lookup"><span data-stu-id="2eca6-179">Create jobs</span></span>](./creating-jobs-attract.md)

[<span data-ttu-id="2eca6-180">LinkedIn との統合のトラブルシューティング</span><span class="sxs-lookup"><span data-stu-id="2eca6-180">Troubleshoot integration with LinkedIn</span></span>](./attract-troubleshoot-linkedin.md)
