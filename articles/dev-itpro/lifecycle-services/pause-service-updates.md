---
title: Lifecycle Services (LCS) によるサービスの更新の一時停止
description: このトピックは環境に応じてサービスの更新を一時停止する方法を説明します。
author: manalidongre
manager: AnnBe
ms.date: 03/22/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Developer, IT Pro
ms.reviewer: sericks
ms.search.scope: Operations
ms.search.region: Global
ms.author: manado
ms.search.validFrom: 2019-3-31
ms.dyn365.ops.version: Platform update 24
ms.openlocfilehash: 69d4c9c6d05f6e541f017f4cfc5742d27aa87cc4
ms.sourcegitcommit: c131672b02407a99aafd38957d04816a82997264
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 03/22/2019
ms.locfileid: "892421"
---
# <a name="pause-service-updates-through-lifecycle-services-lcs"></a><span data-ttu-id="8875f-103">Lifecycle Services (LCS) によるサービスの更新の一時停止</span><span class="sxs-lookup"><span data-stu-id="8875f-103">Pause service updates through Lifecycle Services (LCS)</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="8875f-104">このトピックでは Microsoft Dynamics Lifecycle Services (LCS) を使用して、サンドボックスおよび運用環境の更新を一時停止する方法を説明します。</span><span class="sxs-lookup"><span data-stu-id="8875f-104">This topic explains how to pause updates to your sandbox and production environments by using Microsoft Dynamics Lifecycle Services (LCS).</span></span>

> [!IMPORTANT]
> <span data-ttu-id="8875f-105">この機能は **バージョン 8.1 以降** を使用していて [最初のリリース](../../fin-and-ops/get-started/public-preview-releases.md) プログラムの一部で **ない** 顧客だけが利用できます。</span><span class="sxs-lookup"><span data-stu-id="8875f-105">This feature is available only to customers who are using **version 8.1 and later**, and who are **not** part of the [First release](../../fin-and-ops/get-started/public-preview-releases.md) program.</span></span> <span data-ttu-id="8875f-106">Microsoft はこの機能を最初のリリースのお客様、および古いバージョンの製品を使用しているお客様もご利用いただけるよう努めています。</span><span class="sxs-lookup"><span data-stu-id="8875f-106">Microsoft is working to make the feature available to First release customers and customers who use older versions of the product.</span></span> 

<span data-ttu-id="8875f-107">Microsoft は構成したサンドボックスおよび運用環境を、Microsoft がリリースした最新のサービス更新プログラムに更新します。</span><span class="sxs-lookup"><span data-stu-id="8875f-107">Microsoft updates your configured sandbox and production environments to the latest service update that Microsoft has released.</span></span> <span data-ttu-id="8875f-108">Microsoft はお客様の環境に対する今後の更新プログラムについて、電子メールまたは LCS の通知でお知らせします。</span><span class="sxs-lookup"><span data-stu-id="8875f-108">Microsoft notifies you about upcoming updates to your environments via email and through notifications in LCS.</span></span> <span data-ttu-id="8875f-109">その時点で何らかの理由で更新プログラムを続行できない場合は、LCS を介して一時停止できます。</span><span class="sxs-lookup"><span data-stu-id="8875f-109">At that point, if you can't proceed with the update for some reason, you can pause it through LCS.</span></span>

<span data-ttu-id="8875f-110">構成されたサンドボックス環境を変更して実稼働の更新頻度を設定する方法の詳細は、[Lifecycle Services (LCS) でサービス更新を構成する](configure-service-updates.md) を参照してください。</span><span class="sxs-lookup"><span data-stu-id="8875f-110">For more information about how to change the configured sandbox environment and set the production update cadence, see [Configure service updates through Lifecycle Services (LCS)](configure-service-updates.md).</span></span>

## <a name="who-can-pause-service-updates"></a><span data-ttu-id="8875f-111">誰がサービスの更新を一時停止できますか。</span><span class="sxs-lookup"><span data-stu-id="8875f-111">Who can pause service updates?</span></span>

<span data-ttu-id="8875f-112">LCS で **プロジェクト所有者** ロールが割り当てられているユーザー (顧客またはパートナー) のみが更新を一時停止できます。</span><span class="sxs-lookup"><span data-stu-id="8875f-112">Only users (customers or partners) who are assigned to the **project owner** role in LCS can pause updates.</span></span> <span data-ttu-id="8875f-113">さらに、更新は **実装プロジェクト** に対してのみ一時停止できます。</span><span class="sxs-lookup"><span data-stu-id="8875f-113">Additionally, updates can be paused only for **implementation projects**.</span></span>

<span data-ttu-id="8875f-114">サービスの更新プログラムを最新の状態に保つことで Microsoft がリリースした一連の修正を常にお客様に実行し、最高のサービス エクスペリエンスを提供します。</span><span class="sxs-lookup"><span data-stu-id="8875f-114">Staying current with service updates helps guarantee that customers always run on the latest set of fixes that Microsoft has released, so that they have the best service experience.</span></span> <span data-ttu-id="8875f-115">したがって、Microsoft は更新プログラムを無期限に停止することを許可しません。</span><span class="sxs-lookup"><span data-stu-id="8875f-115">Therefore, Microsoft doesn't allow updates to be paused indefinitely.</span></span>

<span data-ttu-id="8875f-116">Microsoft がリリースした最新の更新プログラムから 2 つ前よりも更新が遅れている場合、LCS で更新プログラムを一時停止できません。</span><span class="sxs-lookup"><span data-stu-id="8875f-116">You can't pause updates through LCS if you're more than two updates behind the latest update that Microsoft has released.</span></span> <span data-ttu-id="8875f-117">たとえば Microsoft が最後にリリースした更新プログラムがバージョン 8.1.3 である場合、バージョン 8.1.2 およびバージョン 8.1.1 を使用しているお客様は更新プログラムを一時停止 **できます**。</span><span class="sxs-lookup"><span data-stu-id="8875f-117">For example, if the last update that Microsoft released is version 8.1.3, customers who are using version 8.1.2 and version 8.1.1 **can** pause updates.</span></span> <span data-ttu-id="8875f-118">しかしバージョン 8.1.0 を使用しているお客様は更新プログラムが 2 つよりさらに遅れているため更新プログラムを一時停止 **できません**。</span><span class="sxs-lookup"><span data-stu-id="8875f-118">However, a customer who is using version 8.1.0 **cannot** pause updates, because they are more than two updates behind.</span></span>

## <a name="what-can-i-pause"></a><span data-ttu-id="8875f-119">何を一時停止できますか。</span><span class="sxs-lookup"><span data-stu-id="8875f-119">What can I pause?</span></span>

<span data-ttu-id="8875f-120">更新を一時停止する場合はオプションが 2 つあります:</span><span class="sxs-lookup"><span data-stu-id="8875f-120">If you decide to pause updates, you have two options:</span></span>

- <span data-ttu-id="8875f-121">実稼働環境に対してのみ更新プログラムを一時停止します。</span><span class="sxs-lookup"><span data-stu-id="8875f-121">Pause updates only to your production environment.</span></span>
- <span data-ttu-id="8875f-122">サンドボックスと実稼働環境の両方の更新プログラムを一時停止します。</span><span class="sxs-lookup"><span data-stu-id="8875f-122">Pause updates to both your sandbox environment and your production environment.</span></span>

<span data-ttu-id="8875f-123">最大 2 つの連続する更新プログラムを一度に一時停止できます。</span><span class="sxs-lookup"><span data-stu-id="8875f-123">You can pause a maximum of two continuous updates at a time.</span></span> <span data-ttu-id="8875f-124">(お伝えできる他の情報として、最大で 3 ヶ月間更新プログラムを一時停止できます。</span><span class="sxs-lookup"><span data-stu-id="8875f-124">(According to other information that is communicated to you, you can pause updates for up to three months.</span></span> <span data-ttu-id="8875f-125">3 か月が 2 つの更新プログラムに対応するため、これら2つの文は一貫しています。) たとえばバージョン 8.1.3 を使用している場合は、更新プログラム バージョン 10.0.0 と更新プログラム バージョン 10.0.1 を一時停止できます。</span><span class="sxs-lookup"><span data-stu-id="8875f-125">These two statements are consistent, because three months correspond to two updates.) For example, if you're using version 8.1.3, you can pause update version 10.0.0 and update version 10.0.1.</span></span> <span data-ttu-id="8875f-126">ただし、更新プログラムのバージョン 10.0.2 を一時停止することはできません。</span><span class="sxs-lookup"><span data-stu-id="8875f-126">However, you can't pause update version 10.0.2.</span></span> <span data-ttu-id="8875f-127">さらに 4 月には次の 2 つの更新プログラムまで一時停止できます。</span><span class="sxs-lookup"><span data-stu-id="8875f-127">In addition, in the month of April, you can pause up to next two updates.</span></span> <span data-ttu-id="8875f-128">7 月、8 月、そしてそれ以降に予定されている更新プログラムを一時停止することはできません。</span><span class="sxs-lookup"><span data-stu-id="8875f-128">However, you will not be able to pause updates scheduled for July, August and later.</span></span> 

> [!IMPORTANT]
>  <span data-ttu-id="8875f-129">業界または業務上のスケジュールを問わず、2つ以上の更新を停止することはできません。</span><span class="sxs-lookup"><span data-stu-id="8875f-129">There is no way to pause more than two updates, regardless of your industry or business schedule.</span></span> <span data-ttu-id="8875f-130">2つ以上の更新が控えている状態で、更新完了後の検証の段階でサンドボックス環境内に致命的な問題を発見した場合は、Microsoftサポートにご連絡の上Production環境の更新停止を依頼してください。</span><span class="sxs-lookup"><span data-stu-id="8875f-130">If you are more than 2 updates behind and you find a critical issue during validations in your sandbox environment after the update, you can contact Microsoft Support to pause the update to your production environment.</span></span> <span data-ttu-id="8875f-131">2つ以上の更新が控えている状態で、かつLCSに実装されている更新の停止機能を使ってProductionの更新停止を実行できない場合にのみ必要となります。</span><span class="sxs-lookup"><span data-stu-id="8875f-131">This is only required if you are more than two updates behind and you are unable to use the pause updates functionality available in LCS to pause the update to production.</span></span>

> <span data-ttu-id="8875f-132">Microsoft は常に実稼働環境よりも前に構成済みのサンドボックス環境を更新するため、サンドボックス環境への更新を一時停止すると実稼働環境でも更新が自動的に一時停止されます。</span><span class="sxs-lookup"><span data-stu-id="8875f-132">If you pause updates to your sandbox environment, updates are automatically paused for your production environment too, because Microsoft always updates configured sandbox environments before production environments.</span></span>

## <a name="how-do-i-pause-updates"></a><span data-ttu-id="8875f-133">更新プログラムを一時停止する方法。</span><span class="sxs-lookup"><span data-stu-id="8875f-133">How do I pause updates?</span></span>

<span data-ttu-id="8875f-134">更新プログラムを一時停止するには、以下の手順を実行します。</span><span class="sxs-lookup"><span data-stu-id="8875f-134">To pause updates, follow these steps.</span></span>

1. <span data-ttu-id="8875f-135">実装プロジェクトの LCS で **プロジェクト設定** ページを開きます。</span><span class="sxs-lookup"><span data-stu-id="8875f-135">In LCS, in your implementation project, open the **Project settings** page.</span></span>

    <span data-ttu-id="8875f-136">このページには **更新プログラムの設定** という名前の新しいタブがあります。</span><span class="sxs-lookup"><span data-stu-id="8875f-136">This page has a new tab that is named **Update settings**.</span></span>

2. <span data-ttu-id="8875f-137">**更新プログラムの設定** タブで、**更新プログラムの一時停止** オプションを **オン** に設定します。</span><span class="sxs-lookup"><span data-stu-id="8875f-137">On the **Update settings** tab, set the **Pause updates** option to **ON**.</span></span>
3. <span data-ttu-id="8875f-138">**設定の編集** を選択します。</span><span class="sxs-lookup"><span data-stu-id="8875f-138">Select **Edit settings**.</span></span>
4. <span data-ttu-id="8875f-139">表示されるダイアログ ボックスで、実稼働環境の更新プログラムのみを一時停止するか、またはサンドボックス環境と実稼働環境の両方で更新を一時停止するかを選択します。</span><span class="sxs-lookup"><span data-stu-id="8875f-139">In the dialog box that appears, select whether you want to pause updates to your production environment only, or to both your sandbox environment and your production environment.</span></span>
5. <span data-ttu-id="8875f-140">**次へ** を選択します。</span><span class="sxs-lookup"><span data-stu-id="8875f-140">Select **Next**.</span></span>
6. <span data-ttu-id="8875f-141">更新プログラムを一時停止する理由を選択してください。</span><span class="sxs-lookup"><span data-stu-id="8875f-141">Select your reason for pausing updates.</span></span> <span data-ttu-id="8875f-142">**検証中に問題が見つかりました** を選択した場合は、有効なサポート チケット番号を入力する必要があります。</span><span class="sxs-lookup"><span data-stu-id="8875f-142">If you select **Issue found during validations**, you must enter a valid support ticket number.</span></span> <span data-ttu-id="8875f-143">更新プログラムを一時停止する理由を Microsoft が理解するためにさらに詳細情報を追加できます。</span><span class="sxs-lookup"><span data-stu-id="8875f-143">You can add any additional details that will help Microsoft understand why you want to pause updates.</span></span>
7. <span data-ttu-id="8875f-144">完了したら、**確定** を選択します。</span><span class="sxs-lookup"><span data-stu-id="8875f-144">When you've finished, select **Confirm**.</span></span>

<span data-ttu-id="8875f-145">既存の一時停止を編集することもできます。</span><span class="sxs-lookup"><span data-stu-id="8875f-145">You can also edit an existing pause.</span></span> <span data-ttu-id="8875f-146">一時停止の期間を延長して更新プログラムをより長い時間停止するか、キャンセルして更新プログラムを再開することができます。</span><span class="sxs-lookup"><span data-stu-id="8875f-146">You can either extend the duration of the pause, so that updates are paused for a longer time, or cancel it, so that updates are resumed.</span></span> <span data-ttu-id="8875f-147">一時停止を編集するには、**設定を編集** を選択します。</span><span class="sxs-lookup"><span data-stu-id="8875f-147">To edit a pause, select **Edit settings**.</span></span> <span data-ttu-id="8875f-148">一時停止できる更新プログラムの数に関する制限がまだ適用されます。</span><span class="sxs-lookup"><span data-stu-id="8875f-148">The limitations about the number of updates that you can pause still apply.</span></span>

<span data-ttu-id="8875f-149">一時停止をキャンセルして環境に対する更新プログラムを再開するには、**更新プログラムを一時停止** オプションを **オフ** に設定します。</span><span class="sxs-lookup"><span data-stu-id="8875f-149">To cancel a pause and resume updates to your environments, set the **Pause updates** option to **OFF**.</span></span>

<span data-ttu-id="8875f-150">更新プログラムの一時停止や既存の一時停止を編集をしたときは、**設定の更新** タブの上部に通知が表示されます。この通知は一時停止された内容を示します。</span><span class="sxs-lookup"><span data-stu-id="8875f-150">Any time that you pause updates or edit an existing pause, a notification appears at the top of the **Update settings** tab. This notification shows what has been paused.</span></span> <span data-ttu-id="8875f-151">選択した環境のサービス更新プログラムの一時停止を通知するために、すべての関係者 (プロジェクト所有者および環境管理者) にも電子メールが送信されます。</span><span class="sxs-lookup"><span data-stu-id="8875f-151">An email is also sent to all stakeholders (the project owner and environment manager), to notify them that service updates for the selected environments have been paused.</span></span> <span data-ttu-id="8875f-152">誰かが既存の一時停止をキャンセルして更新プログラムを再開すると、通知が消えて更新プログラムの再開を関係者に通知する電子メールが送信されます。</span><span class="sxs-lookup"><span data-stu-id="8875f-152">If someone cancels an existing pause and resumes updates, the notification disappears, and an email is sent to inform the stakeholders that updates have resumed.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="8875f-153">ダウンタイム時間枠が始まる 4 時間前まで LCS から更新プログラムを一時停止できます。</span><span class="sxs-lookup"><span data-stu-id="8875f-153">You can pause updates through LCS until four hours before the start of the downtime window.</span></span>

## <a name="what-happens-after-the-pause-duration-expires"></a><span data-ttu-id="8875f-154">一時停止の期間を超えた後はどうなりますか。</span><span class="sxs-lookup"><span data-stu-id="8875f-154">What happens after the pause duration expires?</span></span>

<span data-ttu-id="8875f-155">サービス更新プログラムの積み重ねにより Microsoft がリリースした一連の修正を常にお客様に実行し、最高のサービス エクスペリエンスを提供します。</span><span class="sxs-lookup"><span data-stu-id="8875f-155">Cumulative service updates help guarantee that customers always run on the latest set of fixes that Microsoft has released, so that they have the best service experience.</span></span> <span data-ttu-id="8875f-156">したがって、Microsoft は更新プログラムを無期限に停止することを許可しません。</span><span class="sxs-lookup"><span data-stu-id="8875f-156">Therefore, Microsoft doesn't allow updates to be paused indefinitely.</span></span>

<span data-ttu-id="8875f-157">更新プログラムを再開するために一時停止をキャンセルする方法が 2 つあります。</span><span class="sxs-lookup"><span data-stu-id="8875f-157">There are two ways to cancel pauses, so that updates are resumed:</span></span>

- <span data-ttu-id="8875f-158">前のセクションで説明したように、誰かが継続中の一時停止を手動でキャンセルします。</span><span class="sxs-lookup"><span data-stu-id="8875f-158">Someone manually cancels an ongoing pause, as explained in the previous section.</span></span>
- <span data-ttu-id="8875f-159">一時停止に設定された期間が過ぎると、構成された環境への更新プログラムが自動的に再開します。</span><span class="sxs-lookup"><span data-stu-id="8875f-159">The duration that was set for the pause expires, and updates to the configured environments are automatically resumed.</span></span>

<span data-ttu-id="8875f-160">どちらの場合も、関係者に通知するために電子メールが送信されます。</span><span class="sxs-lookup"><span data-stu-id="8875f-160">In both cases, an email is sent to inform the stakeholders.</span></span>

<span data-ttu-id="8875f-161">サービス更新プログラムに関する詳細は [1 つのバージョンのサービス更新に関するよく寄せられる質問](../../fin-and-ops/get-started/one-version.md) を参照してください。</span><span class="sxs-lookup"><span data-stu-id="8875f-161">For more information about service updates, see [One Version service updates FAQ](../../fin-and-ops/get-started/one-version.md).</span></span>
