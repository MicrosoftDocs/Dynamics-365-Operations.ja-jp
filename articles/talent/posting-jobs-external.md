---
title: Attract から外部キャリア サイトにジョブを転記
description: このトピックでは、外部採用サイトにジョブを転記するための Dynamics 365 for Talent - Attract の使用方法について説明します。
author: pganapmsft
manager: AnnBe
ms.date: 05/16/2019
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
ms.search.validFrom: 2019-03-19
ms.dyn365.ops.version: Platform update 24
ms.openlocfilehash: 9c27d1810a89ed7d7a7745e41c5f118dbdfe5dda
ms.sourcegitcommit: cadce85ca3004d53caf6bc49147a524c1bfd421f
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 05/16/2019
ms.locfileid: "1590485"
---
# <a name="post-jobs-to-external-career-sites-from-attract"></a><span data-ttu-id="a0fbf-103">Attract から外部キャリア サイトにジョブを転記</span><span class="sxs-lookup"><span data-stu-id="a0fbf-103">Post jobs to external career sites from Attract</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="a0fbf-104">できるだけ多くの資格のある候補者の前で、空いている職位を獲得する必要があります。</span><span class="sxs-lookup"><span data-stu-id="a0fbf-104">You want to get your open positions in front of as many qualified candidates as possible.</span></span> <span data-ttu-id="a0fbf-105">Broadbean などの採用サイトは、この目標を達成するのに役立ちます。</span><span class="sxs-lookup"><span data-stu-id="a0fbf-105">Recruiting sites such as Broadbean help you accomplish this goal.</span></span> <span data-ttu-id="a0fbf-106">Microsoft Dynamics 365 Talent: Attract では Broadbean にジョブを転記し、Microsoft がこの領域で新製品を常に提供できるようにします。</span><span class="sxs-lookup"><span data-stu-id="a0fbf-106">Microsoft Dynamics 365 Talent: Attract now lets you post jobs to Broadbean, and Microsoft is constantly providing new offerings in this area.</span></span>

## <a name="post-jobs-to-broadbean"></a><span data-ttu-id="a0fbf-107">Broadbean へのジョブの転記</span><span class="sxs-lookup"><span data-stu-id="a0fbf-107">Post jobs to Broadbean</span></span>

<span data-ttu-id="a0fbf-108">Broadbean にジョブを転記する前に、Broadbean との統合をコンフィギュレーションする必要があります。</span><span class="sxs-lookup"><span data-stu-id="a0fbf-108">Before you can post jobs to Broadbean, you must configure the Broadbean integration.</span></span>

> [!NOTE]
> - <span data-ttu-id="a0fbf-109">外部サイトへジョブを転記するには、[包括採用アドオン](https://docs.microsoft.com/dynamics365/unified-operations/talent/attract-comprehensive-hiring) が必要です。</span><span class="sxs-lookup"><span data-stu-id="a0fbf-109">To post jobs to external sites, you must have the [Comprehensive hiring add-on](https://docs.microsoft.com/dynamics365/unified-operations/talent/attract-comprehensive-hiring).</span></span>
> - <span data-ttu-id="a0fbf-110">Attract から Broadbean にジョブを転記するには、Broadbean サブスクリプションが必要です。</span><span class="sxs-lookup"><span data-stu-id="a0fbf-110">To post jobs to Broadbean through Attract, you must have a Broadbean subscription.</span></span>
> - <span data-ttu-id="a0fbf-111">現在プレビューにある機能です。</span><span class="sxs-lookup"><span data-stu-id="a0fbf-111">This feature is currently in preview.</span></span> <span data-ttu-id="a0fbf-112">試行する場合は、[Attract 管理者の設定で有効にする](https://docs.microsoft.com/dynamics365/unified-operations/talent/access-preview-feature) を実行します。</span><span class="sxs-lookup"><span data-stu-id="a0fbf-112">If you want to try it, you must [turn it on in the Attract admin settings](https://docs.microsoft.com/dynamics365/unified-operations/talent/access-preview-feature).</span></span>

### <a name="configure-broadbean-integration"></a><span data-ttu-id="a0fbf-113">Broadbean との統合をコンフィギュレーションする</span><span class="sxs-lookup"><span data-stu-id="a0fbf-113">Configure Broadbean integration</span></span>

1. <span data-ttu-id="a0fbf-114">Attract に管理者としてサインインします。</span><span class="sxs-lookup"><span data-stu-id="a0fbf-114">Sign in to Attract as an admin.</span></span>
2. <span data-ttu-id="a0fbf-115">ページの右上隅にある**設定**ボタン (ギヤ記号) を選択して、**管理者センター**を選択します。</span><span class="sxs-lookup"><span data-stu-id="a0fbf-115">Select the **Settings** button (the gear symbol) in the upper-right corner of the page, and then select **Admin center**.</span></span>
3. <span data-ttu-id="a0fbf-116">**職務ボードの設定**タブの **Broadbean との統合を有効にする**セクションで、統合を有効にします。</span><span class="sxs-lookup"><span data-stu-id="a0fbf-116">On the **Job board settings** tab, in the **Enable Broadbean integration** section, turn on the integration.</span></span>
4. <span data-ttu-id="a0fbf-117">Broadbean に連絡し、**ユーザー名、クライアント ID、暗号化トークン**の情報を入力します。</span><span class="sxs-lookup"><span data-stu-id="a0fbf-117">Contact Broadbean, and enter your information in **Username, Client ID, Encryption Token**.</span></span>

> [!WARNING]
> <span data-ttu-id="a0fbf-118">Broadbean の資格情報は機密性が高いものです。</span><span class="sxs-lookup"><span data-stu-id="a0fbf-118">Your Broadbean credentials are sensitive and confidential.</span></span> <span data-ttu-id="a0fbf-119">したがって、責任を持ってそれらを格納および共有します。</span><span class="sxs-lookup"><span data-stu-id="a0fbf-119">Therefore, store and share them responsibly.</span></span> <span data-ttu-id="a0fbf-120">Attract の管理者ロールを持つすべてのユーザーは、これらの資格情報を表示できます。</span><span class="sxs-lookup"><span data-stu-id="a0fbf-120">Anyone who has an Administrator role in Attract can view these credentials.</span></span>

> [!NOTE]
> <span data-ttu-id="a0fbf-121">Microsoft と Attract は、これらの値を作成し管理することには関与していません。</span><span class="sxs-lookup"><span data-stu-id="a0fbf-121">Microsoft and Attract aren't involved in creating and maintaining these values.</span></span> <span data-ttu-id="a0fbf-122">Attract でそれらを最新の状態に保ち、Broadbean と協力してユーザーの資格情報に関連する問題を解決するのはユーザー個人の責任となりす。</span><span class="sxs-lookup"><span data-stu-id="a0fbf-122">It's your responsibility to keep them up to date in Attract and to work with Broadbean to resolve any issues that involve your credentials.</span></span>

### <a name="post-a-job-to-broadbean"></a><span data-ttu-id="a0fbf-123">Broadbean へのジョブの転記</span><span class="sxs-lookup"><span data-stu-id="a0fbf-123">Post a job to Broadbean</span></span>

<span data-ttu-id="a0fbf-124">Broadbean を有効にした後、採用担当者および管理者はジョブを転記できます。</span><span class="sxs-lookup"><span data-stu-id="a0fbf-124">After Broadbean has been turned on, recruiters and admins can post a job to it.</span></span> <span data-ttu-id="a0fbf-125">職務の応募 URL が必要です。</span><span class="sxs-lookup"><span data-stu-id="a0fbf-125">You must have an apply URL for the job.</span></span>

1. <span data-ttu-id="a0fbf-126">Attract で、Broadbean に転記する職務を開きます。</span><span class="sxs-lookup"><span data-stu-id="a0fbf-126">In Attract, open the job that you want to post to Broadbean.</span></span>
2. <span data-ttu-id="a0fbf-127">**転記**セクションで、Broadbean に対応する**今すぐ転記**ボタンを選択します。</span><span class="sxs-lookup"><span data-stu-id="a0fbf-127">In the **Postings** section, select the **Post Now** button that corresponds to Broadbean.</span></span>
3. <span data-ttu-id="a0fbf-128">Broadbean ウィンドウの指示に従います。</span><span class="sxs-lookup"><span data-stu-id="a0fbf-128">Follow the instructions in the Broadbean window.</span></span>

<span data-ttu-id="a0fbf-129">Attract から Broadbean に渡される情報は次の通りです。</span><span class="sxs-lookup"><span data-stu-id="a0fbf-129">Attract passes the following information to Broadbean:</span></span>

- <span data-ttu-id="a0fbf-130">要求 ID</span><span class="sxs-lookup"><span data-stu-id="a0fbf-130">Request ID</span></span>
- <span data-ttu-id="a0fbf-131">職位</span><span class="sxs-lookup"><span data-stu-id="a0fbf-131">Job title</span></span>
- <span data-ttu-id="a0fbf-132">ジョブの説明</span><span class="sxs-lookup"><span data-stu-id="a0fbf-132">Job description</span></span>
- <span data-ttu-id="a0fbf-133">勤務地</span><span class="sxs-lookup"><span data-stu-id="a0fbf-133">Job location</span></span>
- <span data-ttu-id="a0fbf-134">応募 URL</span><span class="sxs-lookup"><span data-stu-id="a0fbf-134">Apply URL</span></span>
- <span data-ttu-id="a0fbf-135">リクルーター情報</span><span class="sxs-lookup"><span data-stu-id="a0fbf-135">Recruiter information</span></span>

<span data-ttu-id="a0fbf-136">Broadbean が正常に転記を完了した後、Attract の**転記**セクションでは Broadbean のステータスが**転記済**として表示されます。</span><span class="sxs-lookup"><span data-stu-id="a0fbf-136">After Broadbean successfully completes the posting, the **Postings** section of the job in Attract shows the Broadbean status as **Posted**.</span></span>

> [!NOTE]
> - <span data-ttu-id="a0fbf-137">Broadbean には**業界**フィールドが必要です。</span><span class="sxs-lookup"><span data-stu-id="a0fbf-137">Broadbean requires the **Industry** field.</span></span> <span data-ttu-id="a0fbf-138">現時点では、このフィールドは既定で **IT** に設定されています。</span><span class="sxs-lookup"><span data-stu-id="a0fbf-138">Currently, this field is set to **IT** by default.</span></span> <span data-ttu-id="a0fbf-139">ただし、Broadbean ジョブ転記のウィンドウで適切な業界に値を変更できます。</span><span class="sxs-lookup"><span data-stu-id="a0fbf-139">However, you can change the value to the correct industry in the window for Broadbean job posting.</span></span>
> - <span data-ttu-id="a0fbf-140">Broadbean が、選択したすべての職務ボードにユーザーのジョブ転記を完了するまでには少し時間がかかります。</span><span class="sxs-lookup"><span data-stu-id="a0fbf-140">It takes some time for Broadbean to finish posting your job to all the job boards that you selected.</span></span> <span data-ttu-id="a0fbf-141">したがって、Attract では職務の状態更新を提供するまでに、わずかな遅れがある可能性があります。</span><span class="sxs-lookup"><span data-stu-id="a0fbf-141">Therefore, there might be a slight delay before Attract provides a status update for the job.</span></span>

### <a name="view-a-broadbean-job-posting"></a><span data-ttu-id="a0fbf-142">Broadbean のジョブ転記を表示する</span><span class="sxs-lookup"><span data-stu-id="a0fbf-142">View a Broadbean job posting</span></span>

<span data-ttu-id="a0fbf-143">ジョブを Broadbean に転記した後は、Attract から表示できます。</span><span class="sxs-lookup"><span data-stu-id="a0fbf-143">After you post a job to Broadbean, you can view it from Attract.</span></span>

1. <span data-ttu-id="a0fbf-144">Attract で、Broadbean で表示する職務を開きます。</span><span class="sxs-lookup"><span data-stu-id="a0fbf-144">In Attract, open the job that you want to view on Broadbean.</span></span>
2. <span data-ttu-id="a0fbf-145">**転記**セクションで、Broadbean に対応する省略記号ボタン (**...**) を選択し、**表示**を選択します。</span><span class="sxs-lookup"><span data-stu-id="a0fbf-145">In the **Postings** section, select the ellipsis button (**...**) that corresponds to Broadbean, and then select **View**.</span></span>

<span data-ttu-id="a0fbf-146">Broadbean のジョブ転記は、新しいウィンドウに表示されます。</span><span class="sxs-lookup"><span data-stu-id="a0fbf-146">The Broadbean job posting appears in a new window.</span></span>

### <a name="update-a-broadbean-job-posting"></a><span data-ttu-id="a0fbf-147">Broadbean のジョブ転記を更新する</span><span class="sxs-lookup"><span data-stu-id="a0fbf-147">Update a Broadbean job posting</span></span>

<span data-ttu-id="a0fbf-148">Broadbean のジョブ転記は 2 通りの方法で更新できます。</span><span class="sxs-lookup"><span data-stu-id="a0fbf-148">You can update a Broadbean job posting in two ways.</span></span>

1. <span data-ttu-id="a0fbf-149">Attract で、更新する職務を開きます。</span><span class="sxs-lookup"><span data-stu-id="a0fbf-149">In Attract, open the job that you want to update.</span></span>
2. <span data-ttu-id="a0fbf-150">**転記**セクションで、Broadbean に対応する**転記を更新**ボタンを選択します。</span><span class="sxs-lookup"><span data-stu-id="a0fbf-150">In the **Postings** section, select the **Update Post** button that corresponds to Broadbean.</span></span>
3. <span data-ttu-id="a0fbf-151">Broadbean ウィンドウで、転記を編集します。</span><span class="sxs-lookup"><span data-stu-id="a0fbf-151">Edit the posting in the Broadbean window.</span></span>

<span data-ttu-id="a0fbf-152">- または -</span><span class="sxs-lookup"><span data-stu-id="a0fbf-152">–or–</span></span>

1. <span data-ttu-id="a0fbf-153">Attract で、Broadbean で表示する職務を開きます。</span><span class="sxs-lookup"><span data-stu-id="a0fbf-153">In Attract, open the job that you want to view on Broadbean.</span></span>
2. <span data-ttu-id="a0fbf-154">**転記**セクションで、Broadbean に対応する省略記号ボタン (**...**) を選択し、**表示**を選択します。</span><span class="sxs-lookup"><span data-stu-id="a0fbf-154">In the **Postings** section, select the ellipsis button (**...**) that corresponds to Broadbean, and then select **View**.</span></span>
3. <span data-ttu-id="a0fbf-155">Broadbean ウィンドウで職務の詳細を編集してから、ジョブを再転記します。</span><span class="sxs-lookup"><span data-stu-id="a0fbf-155">In the Broadbean window, edit the job details, and then repost the job.</span></span> <span data-ttu-id="a0fbf-156">Attract では職務の詳細は変更されません。</span><span class="sxs-lookup"><span data-stu-id="a0fbf-156">The job details in Attract aren't changed.</span></span>

### <a name="remove-a-broadbean-job-posting"></a><span data-ttu-id="a0fbf-157">Broadbean のジョブ転記を削除する</span><span class="sxs-lookup"><span data-stu-id="a0fbf-157">Remove a Broadbean job posting</span></span>

<span data-ttu-id="a0fbf-158">必要に応じて Broadbean からジョブ転記を削除できます。</span><span class="sxs-lookup"><span data-stu-id="a0fbf-158">You can remove a job posting from Broadbean as you require.</span></span>

1. <span data-ttu-id="a0fbf-159">Attract で、削除する職務を開きます。</span><span class="sxs-lookup"><span data-stu-id="a0fbf-159">In Attract, open the job that you want to remove.</span></span>
2. <span data-ttu-id="a0fbf-160">**転記**セクションで、Broadbean に対応する省略記号ボタン (**...**) を選択し、**転記を削除**を選択します。</span><span class="sxs-lookup"><span data-stu-id="a0fbf-160">In the **Postings** section, select the ellipsis button (**...**) that corresponds to Broadbean, and then select **Remove Post**.</span></span>

<span data-ttu-id="a0fbf-161">Broadbean でジョブが削除された後、Attract の Broadbean 項目には**今すぐ転記**ボタンが表示されます。</span><span class="sxs-lookup"><span data-stu-id="a0fbf-161">After Broadbean removes the job, the Broadbean item in Attract has a **Post Now** button.</span></span> <span data-ttu-id="a0fbf-162">このボタンが存在するということは、職務が削除されており、もう一度転記できることを示します。</span><span class="sxs-lookup"><span data-stu-id="a0fbf-162">The presence of this button indicates that the job has been removed and can be posted again.</span></span>

### <a name="troubleshoot-the-broadbean-integration"></a><span data-ttu-id="a0fbf-163">Broadbean との統合のトラブルシューティング</span><span class="sxs-lookup"><span data-stu-id="a0fbf-163">Troubleshoot the Broadbean integration</span></span>

<span data-ttu-id="a0fbf-164">Broadbean にジョブを転記できない場合は、これらの手順を実行します。</span><span class="sxs-lookup"><span data-stu-id="a0fbf-164">If you're having trouble posting a job to Broadbean, try these steps.</span></span>

1. <span data-ttu-id="a0fbf-165">Attract で入力した Broadbean の資格情報が有効で正しいことを確認します。</span><span class="sxs-lookup"><span data-stu-id="a0fbf-165">Verify that the Broadbean credentials that you entered in Attract are valid and correct.</span></span>
2. <span data-ttu-id="a0fbf-166">資格情報が有効で正しい場合、[Broadbean サポート](https://www.broadbean.com/resources/support/) にお問い合わせください。</span><span class="sxs-lookup"><span data-stu-id="a0fbf-166">If the credentials are valid and correct, contact [Broadbean support](https://www.broadbean.com/resources/support/).</span></span>
3. <span data-ttu-id="a0fbf-167">問題が解消しない場合は、[Microsoft サポート](./talent-support.md) にお問い合わせください。</span><span class="sxs-lookup"><span data-stu-id="a0fbf-167">If the issue persists, contact [Microsoft support](./talent-support.md).</span></span>
