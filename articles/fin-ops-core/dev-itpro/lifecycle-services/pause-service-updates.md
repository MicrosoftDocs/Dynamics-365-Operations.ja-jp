---
title: Lifecycle Services (LCS) によるサービスの更新の一時停止
description: このトピックは環境に応じてサービスの更新を一時停止する方法を説明します。
author: angelmarshall
manager: AnnBe
ms.date: 03/03/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Developer, IT Pro
ms.reviewer: sericks
ms.search.region: Global
ms.author: tsmarsha
ms.search.validFrom: 2019-3-31
ms.dyn365.ops.version: Platform update 24
ms.openlocfilehash: 722b8ae7881fa9cf41aa49d3666998cce07edc77
ms.sourcegitcommit: 659375c4cc7f5524cbf91cf6160f6a410960ac16
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 12/05/2020
ms.locfileid: "4687902"
---
# <a name="pause-service-updates-through-lifecycle-services-lcs"></a><span data-ttu-id="5f957-103">Lifecycle Services (LCS) によるサービスの更新の一時停止</span><span class="sxs-lookup"><span data-stu-id="5f957-103">Pause service updates through Lifecycle Services (LCS)</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="5f957-104">このトピックでは Microsoft Dynamics Lifecycle Services (LCS) を使用して、サンドボックスおよび運用クラウド環境の更新を一時停止する方法を説明します。</span><span class="sxs-lookup"><span data-stu-id="5f957-104">This topic explains how to pause updates to your sandbox and production cloud environments by using Microsoft Dynamics Lifecycle Services (LCS).</span></span> <span data-ttu-id="5f957-105">このトピックは、オンプレミス環境には適用されません。</span><span class="sxs-lookup"><span data-stu-id="5f957-105">This topic does not apply to on-premises environments.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="5f957-106">この機能は **バージョン 8.1 以降** を使用しているお客様、または **バージョン 7.3** を使用していて、[初回リリース](../../../fin-ops-core/fin-ops/get-started/public-preview-releases.md) プログラムに参加して **いない** お客様だけが利用できます。</span><span class="sxs-lookup"><span data-stu-id="5f957-106">This feature is available only to customers who are using **version 8.1 and later** or are using **version 7.3**, and who are **not** part of the [First release](../../../fin-ops-core/fin-ops/get-started/public-preview-releases.md) program.</span></span> <span data-ttu-id="5f957-107">Microsoft はこの機能を初回リリースのお客様が利用できるようにすることを目指しています。</span><span class="sxs-lookup"><span data-stu-id="5f957-107">Microsoft is working to make the feature available to First release customers.</span></span> <span data-ttu-id="5f957-108">バージョン 7.1、7.2、または 8.0 のお客様は、通常のサービス フローを使用して手動で更新を行うことができます。</span><span class="sxs-lookup"><span data-stu-id="5f957-108">For customers who are on version 7.1, 7.2, or 8.0, you can take the update manually using the regular servicing flows.</span></span>

<span data-ttu-id="5f957-109">Microsoft は構成したサンドボックスおよび運用環境を、Microsoft がリリースした最新のサービス更新プログラムに更新します。</span><span class="sxs-lookup"><span data-stu-id="5f957-109">Microsoft updates your configured sandbox and production environments to the latest service update that Microsoft has released.</span></span> <span data-ttu-id="5f957-110">Microsoft はお客様の環境に対する今後の更新プログラムについて、電子メールまたは LCS の通知でお知らせします。</span><span class="sxs-lookup"><span data-stu-id="5f957-110">Microsoft notifies you about upcoming updates to your environments via email and through notifications in LCS.</span></span> <span data-ttu-id="5f957-111">その時点で何らかの理由で更新プログラムを続行できない場合は、LCS を介して一時停止できます。</span><span class="sxs-lookup"><span data-stu-id="5f957-111">At that point, if you can't proceed with the update for some reason, you can pause it through LCS.</span></span>

<span data-ttu-id="5f957-112">構成されたサンドボックス環境を変更して実稼働の更新頻度を設定する方法の詳細は、[Lifecycle Services (LCS) でサービス更新を構成する](configure-service-updates.md) を参照してください。</span><span class="sxs-lookup"><span data-stu-id="5f957-112">For more information about how to change the configured sandbox environment and set the production update cadence, see [Configure service updates through Lifecycle Services (LCS)](configure-service-updates.md).</span></span>

## <a name="who-can-pause-service-updates"></a><span data-ttu-id="5f957-113">誰がサービスの更新を一時停止できますか。</span><span class="sxs-lookup"><span data-stu-id="5f957-113">Who can pause service updates?</span></span>

<span data-ttu-id="5f957-114">LCS で **プロジェクト所有者** ロールが割り当てられているユーザー (顧客またはパートナー) のみが更新を一時停止できます。</span><span class="sxs-lookup"><span data-stu-id="5f957-114">Only users (customers or partners) who are assigned to the **project owner** role in LCS can pause updates.</span></span> <span data-ttu-id="5f957-115">さらに、更新は **実装プロジェクト** に対してのみ一時停止できます。</span><span class="sxs-lookup"><span data-stu-id="5f957-115">Additionally, updates can be paused only for **implementation projects**.</span></span>

<span data-ttu-id="5f957-116">サービスの更新プログラムを最新の状態に保つことで Microsoft がリリースした一連の修正を常にお客様に実行し、最高のサービス エクスペリエンスを提供します。</span><span class="sxs-lookup"><span data-stu-id="5f957-116">Staying current with service updates helps guarantee that customers always run on the latest set of fixes that Microsoft has released, so that they have the best service experience.</span></span> <span data-ttu-id="5f957-117">したがって、Microsoft は更新プログラムを無期限に停止することを許可しません。</span><span class="sxs-lookup"><span data-stu-id="5f957-117">Therefore, Microsoft doesn't allow updates to be paused indefinitely.</span></span>

<span data-ttu-id="5f957-118">Microsoft がリリースしている最新の更新プログラムから 3つ またはそれ以上の未適用の更新がある場合は、LCSを使用して更新の一時停止をすることはできません。</span><span class="sxs-lookup"><span data-stu-id="5f957-118">You can't use LCS to pause updates if you're three or more updates behind the latest update that Microsoft has released.</span></span> <span data-ttu-id="5f957-119">Microsoft がリリースした最新の更新プログラムのバージョンが 10.0.0 であった場合で、ユーザーが使用しているバージョンが 8.1.3 または、8.1.2 または、8.1.1 であった場合に更新プログラムを一時停止 **することが可能です** 。</span><span class="sxs-lookup"><span data-stu-id="5f957-119">For example, if the latest update that Microsoft has released is version 10.0.0, customers who are on version 8.1.3, version 8.1.2, and version 8.1.1 **can** pause updates.</span></span> <span data-ttu-id="5f957-120">しかしバージョン 8.1.0 を使用しているユーザーは更新プログラムが 3つ以上古いものであるため更新プログラムを一時停止することが **できません** 。</span><span class="sxs-lookup"><span data-stu-id="5f957-120">However, customers who are on version 8.1.0 **can't** pause updates, because they are more than three updates behind.</span></span> <span data-ttu-id="5f957-121">バージョン 7.3 を使用している場合は、プラットフォームの更新のみが適用されます。</span><span class="sxs-lookup"><span data-stu-id="5f957-121">Customers who are on version 7.3 can get only platform updates.</span></span> <span data-ttu-id="5f957-122">たとえば、Microsoftがリリースした最新のプラットフォーム更新プログラムが 25 の場合、プラットフォーム更新プログラム 24 と更新 23 と更新 22 を使用しているユーザーは一時停止 **することができます** 。</span><span class="sxs-lookup"><span data-stu-id="5f957-122">For example, if the last platform update that Microsoft has released is Platform update 25, customers who are on Platform update 24, Platform update 23, and Platform update 22 **can** pause updates.</span></span> <span data-ttu-id="5f957-123">ただし、プラットフォーム更新プログラム 21 を利用しているユーザーは、更新を一時停止することが **できません** 。</span><span class="sxs-lookup"><span data-stu-id="5f957-123">However, customers who are on Platform update 21 **can't** pause updates.</span></span>

## <a name="what-can-i-pause"></a><span data-ttu-id="5f957-124">何を一時停止できますか。</span><span class="sxs-lookup"><span data-stu-id="5f957-124">What can I pause?</span></span>

<span data-ttu-id="5f957-125">更新を一時停止する場合はオプションが 2 つあります:</span><span class="sxs-lookup"><span data-stu-id="5f957-125">If you decide to pause updates, you have two options:</span></span>

- <span data-ttu-id="5f957-126">実稼働環境に対してのみ更新プログラムを一時停止します。</span><span class="sxs-lookup"><span data-stu-id="5f957-126">Pause updates only to your production environment.</span></span>
- <span data-ttu-id="5f957-127">サンドボックスと実稼働環境の両方の更新プログラムを一時停止します。</span><span class="sxs-lookup"><span data-stu-id="5f957-127">Pause updates to both your sandbox environment and your production environment.</span></span>

<span data-ttu-id="5f957-128">一度に最大3つまでの連続する更新プログラムを一時停止することができます。</span><span class="sxs-lookup"><span data-stu-id="5f957-128">You can pause a maximum of three continuous updates at a time.</span></span> <span data-ttu-id="5f957-129">たとえば、バージョン8.1.3を使用している場合は、更新バージョン10.0.0、10.0.1、10.0.2を一時停止することができます。</span><span class="sxs-lookup"><span data-stu-id="5f957-129">For example, if you're using version 8.1.3, you can pause update version 10.0.0, 10.0.1 and 10.0.2.</span></span> <span data-ttu-id="5f957-130">ただし、更新プログラムのバージョン 10.0.3 を一時停止することはできません。</span><span class="sxs-lookup"><span data-stu-id="5f957-130">However, you can't pause update version 10.0.3.</span></span> <span data-ttu-id="5f957-131">加えて、6月には次に控えている 3つの更新プログラムまで一時停止できます。</span><span class="sxs-lookup"><span data-stu-id="5f957-131">In addition, in the month of June, you can pause the next three updates.</span></span> <span data-ttu-id="5f957-132">しかし、10月と11月と12月以降に予定されている更新プログラムを一時停止することはできません。</span><span class="sxs-lookup"><span data-stu-id="5f957-132">However, you will not be able to pause updates scheduled for October, November, December and later.</span></span> <span data-ttu-id="5f957-133">同様に、プラットフォームの更新のみを適用する バージョン 7.3 を利用しているユーザーに対しては、プラットフォーム 23 を使用している場合は 24 と 25 と26 の更新を一時停止することはできますが、プラットフォーム 27 を一時停止することはできません。</span><span class="sxs-lookup"><span data-stu-id="5f957-133">Similarly, for customers on version 7.3 for platform only updates, if you’re using Platform update 23 then you can pause update 24, update 25, and update 26, but you cannot pause update 27.</span></span> <span data-ttu-id="5f957-134">1年間に8つの更新プログラムをリリースします。</span><span class="sxs-lookup"><span data-stu-id="5f957-134">We will be releasing 8 updates in a year.</span></span> <span data-ttu-id="5f957-135">1年の間で少なくとも2つの更新を適用する必要があります。</span><span class="sxs-lookup"><span data-stu-id="5f957-135">We require you to take at least two updates in a year.</span></span>

> [!IMPORTANT]
>  <span data-ttu-id="5f957-136">従事する業界またはその業務上のスケジュールを問わず、3つ以上の更新を停止することはできません。</span><span class="sxs-lookup"><span data-stu-id="5f957-136">There is no way to pause more than three updates, regardless of your industry or business schedule.</span></span> <span data-ttu-id="5f957-137">3つ以上の更新が控えている状態で、更新完了後の検証段階でサンドボックス環境内に致命的な問題を発見した場合は、Microsoftサポートにご連絡の上で実稼働環境の更新停止を依頼してください。</span><span class="sxs-lookup"><span data-stu-id="5f957-137">If you are more than three updates behind and you find a critical issue during validations in your sandbox environment after the update, you can contact Microsoft Support to pause the update to your production environment.</span></span> <span data-ttu-id="5f957-138">3つ以上の更新が控えている状態で、かつLCSに実装されている更新の停止機能を使って実稼働環境の更新停止を実行できない場合にのみ必要となります。</span><span class="sxs-lookup"><span data-stu-id="5f957-138">This is only required if you are more than three updates behind and you are unable to use the pause updates functionality available in LCS to pause the update to production.</span></span>

> <span data-ttu-id="5f957-139">サンドボックス環境への更新を一時停止する場合は、実稼働環境への更新も自動的に一時停止されます。これは、Microdoftが常に実稼働環境よりも先にに構成済みのサンドボックス環境を更新するためです。</span><span class="sxs-lookup"><span data-stu-id="5f957-139">If you pause updates to your sandbox environment, updates are automatically also paused for your production environment, because Microsoft always updates configured sandbox environments before production environments.</span></span>

## <a name="how-do-i-pause-updates"></a><span data-ttu-id="5f957-140">更新プログラムを一時停止する方法。</span><span class="sxs-lookup"><span data-stu-id="5f957-140">How do I pause updates?</span></span>

<span data-ttu-id="5f957-141">更新プログラムを一時停止するには、以下の手順を実行します。</span><span class="sxs-lookup"><span data-stu-id="5f957-141">To pause updates, follow these steps.</span></span>

1. <span data-ttu-id="5f957-142">実装プロジェクトの LCS で **プロジェクト設定** ページを開きます。</span><span class="sxs-lookup"><span data-stu-id="5f957-142">In LCS, in your implementation project, open the **Project settings** page.</span></span>

    <span data-ttu-id="5f957-143">このページには **更新プログラムの設定** という名前の新しいタブがあります。</span><span class="sxs-lookup"><span data-stu-id="5f957-143">This page has a new tab that is named **Update settings**.</span></span>

2. <span data-ttu-id="5f957-144">**更新プログラムの設定** タブで、**更新プログラムの一時停止** オプションを **オン** に設定します。</span><span class="sxs-lookup"><span data-stu-id="5f957-144">On the **Update settings** tab, set the **Pause updates** option to **ON**.</span></span>
3. <span data-ttu-id="5f957-145">**設定の編集** を選択します。</span><span class="sxs-lookup"><span data-stu-id="5f957-145">Select **Edit settings**.</span></span>
4. <span data-ttu-id="5f957-146">表示されるダイアログ ボックスで、実稼働環境の更新プログラムのみを一時停止するか、またはサンドボックス環境と実稼働環境の両方で更新を一時停止するかを選択します。</span><span class="sxs-lookup"><span data-stu-id="5f957-146">In the dialog box that appears, select whether you want to pause updates to your production environment only, or to both your sandbox environment and your production environment.</span></span>
5. <span data-ttu-id="5f957-147">**次へ** を選択します。</span><span class="sxs-lookup"><span data-stu-id="5f957-147">Select **Next**.</span></span>
6. <span data-ttu-id="5f957-148">更新プログラムを一時停止する理由を選択してください。</span><span class="sxs-lookup"><span data-stu-id="5f957-148">Select your reason for pausing updates.</span></span> <span data-ttu-id="5f957-149">**検証中に問題が見つかりました** を選択した場合は、有効なサポート チケット番号を入力する必要があります。</span><span class="sxs-lookup"><span data-stu-id="5f957-149">If you select **Issue found during validations**, you must enter a valid support ticket number.</span></span> <span data-ttu-id="5f957-150">更新プログラムを一時停止する理由を Microsoft が理解するためにさらに詳細情報を追加できます。</span><span class="sxs-lookup"><span data-stu-id="5f957-150">You can add any additional details that will help Microsoft understand why you want to pause updates.</span></span>
7. <span data-ttu-id="5f957-151">完了したら、**確定** を選択します。</span><span class="sxs-lookup"><span data-stu-id="5f957-151">When you've finished, select **Confirm**.</span></span>

<span data-ttu-id="5f957-152">既存の一時停止を編集することもできます。</span><span class="sxs-lookup"><span data-stu-id="5f957-152">You can also edit an existing pause.</span></span> <span data-ttu-id="5f957-153">一時停止の期間を延長して更新プログラムをより長い時間停止するか、キャンセルして更新プログラムを再開することができます。</span><span class="sxs-lookup"><span data-stu-id="5f957-153">You can either extend the duration of the pause, so that updates are paused for a longer time, or cancel it, so that updates are resumed.</span></span> <span data-ttu-id="5f957-154">一時停止を編集するには、**設定を編集** を選択します。</span><span class="sxs-lookup"><span data-stu-id="5f957-154">To edit a pause, select **Edit settings**.</span></span> <span data-ttu-id="5f957-155">一時停止できる更新プログラムの数に関する制限がまだ適用されます。</span><span class="sxs-lookup"><span data-stu-id="5f957-155">The limitations about the number of updates that you can pause still apply.</span></span>

<span data-ttu-id="5f957-156">一時停止をキャンセルして環境に対する更新プログラムを再開するには、**更新プログラムを一時停止** オプションを **オフ** に設定します。</span><span class="sxs-lookup"><span data-stu-id="5f957-156">To cancel a pause and resume updates to your environments, set the **Pause updates** option to **OFF**.</span></span>

<span data-ttu-id="5f957-157">更新プログラムの一時停止や既存の一時停止を編集をしたときは、**設定の更新** タブの上部に通知が表示されます。この通知は一時停止された内容を示します。</span><span class="sxs-lookup"><span data-stu-id="5f957-157">Any time that you pause updates or edit an existing pause, a notification appears at the top of the **Update settings** tab. This notification shows what has been paused.</span></span> <span data-ttu-id="5f957-158">選択した環境のサービス更新プログラムの一時停止を通知するために、すべての関係者 (プロジェクト所有者および環境管理者) にも電子メールが送信されます。</span><span class="sxs-lookup"><span data-stu-id="5f957-158">An email is also sent to all stakeholders (the project owner and environment manager), to notify them that service updates for the selected environments have been paused.</span></span> <span data-ttu-id="5f957-159">誰かが既存の一時停止をキャンセルして更新プログラムを再開すると、通知が消えて更新プログラムの再開を関係者に通知する電子メールが送信されます。</span><span class="sxs-lookup"><span data-stu-id="5f957-159">If someone cancels an existing pause and resumes updates, the notification disappears, and an email is sent to inform the stakeholders that updates have resumed.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="5f957-160">ダウンタイム時間枠が始まる 4 時間前まで LCS から更新プログラムを一時停止できます。</span><span class="sxs-lookup"><span data-stu-id="5f957-160">You can pause updates through LCS until four hours before the start of the downtime window.</span></span>

> <span data-ttu-id="5f957-161">一時停止をキャンセルし、更新予定の7日前までの期間で更新を再開するように選択できます。</span><span class="sxs-lookup"><span data-stu-id="5f957-161">You can cancel a pause and choose to resume updates only 7 days prior to the start of the downtime date.</span></span> <span data-ttu-id="5f957-162">この日付を過ぎている場合、一時停止をキャンセルすることはできません。</span><span class="sxs-lookup"><span data-stu-id="5f957-162">If you are past that date then you will not be able to cancel a pause.</span></span>

## <a name="what-happens-after-the-pause-duration-expires"></a><span data-ttu-id="5f957-163">一時停止の期間を超えた後はどうなりますか。</span><span class="sxs-lookup"><span data-stu-id="5f957-163">What happens after the pause duration expires?</span></span>

<span data-ttu-id="5f957-164">サービス更新プログラムの積み重ねにより Microsoft がリリースした一連の修正を常にお客様に実行し、最高のサービス エクスペリエンスを提供します。</span><span class="sxs-lookup"><span data-stu-id="5f957-164">Cumulative service updates help guarantee that customers always run on the latest set of fixes that Microsoft has released, so that they have the best service experience.</span></span> <span data-ttu-id="5f957-165">したがって、Microsoft は更新プログラムを無期限に停止することを許可しません。</span><span class="sxs-lookup"><span data-stu-id="5f957-165">Therefore, Microsoft doesn't allow updates to be paused indefinitely.</span></span>

<span data-ttu-id="5f957-166">更新プログラムを再開するために一時停止をキャンセルする方法が 2 つあります。</span><span class="sxs-lookup"><span data-stu-id="5f957-166">There are two ways to cancel pauses, so that updates are resumed:</span></span>

- <span data-ttu-id="5f957-167">前のセクションで説明したように、誰かが継続中の一時停止を手動でキャンセルします。</span><span class="sxs-lookup"><span data-stu-id="5f957-167">Someone manually cancels an ongoing pause, as explained in the previous section.</span></span>
- <span data-ttu-id="5f957-168">一時停止に設定された期間が過ぎると、構成された環境への更新プログラムが自動的に再開します。</span><span class="sxs-lookup"><span data-stu-id="5f957-168">The duration that was set for the pause expires, and updates to the configured environments are automatically resumed.</span></span>

<span data-ttu-id="5f957-169">どちらの場合も、関係者に通知するために電子メールが送信されます。</span><span class="sxs-lookup"><span data-stu-id="5f957-169">In both cases, an email is sent to inform the stakeholders.</span></span>

<span data-ttu-id="5f957-170">サービス更新プログラムに関する詳細は [1 つのバージョンのサービス更新に関するよく寄せられる質問](../../../fin-ops-core/fin-ops/get-started/one-version.md) を参照してください。</span><span class="sxs-lookup"><span data-stu-id="5f957-170">For more information about service updates, see [One Version service updates FAQ](../../../fin-ops-core/fin-ops/get-started/one-version.md).</span></span>
