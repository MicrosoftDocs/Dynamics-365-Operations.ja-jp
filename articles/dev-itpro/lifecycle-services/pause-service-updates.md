---
title: Lifecycle Services (LCS) によるサービスの更新の一時停止
description: このトピックは環境に応じてサービスの更新を一時停止する方法を説明します。
author: manalidongre
manager: AnnBe
ms.date: 05/10/2019
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
ms.openlocfilehash: 9d8573b915f62d8bd0eb796fadf46973843899b2
ms.sourcegitcommit: f7a1e74a639dfbe470f7d57d4fc55e3bf4c6a74a
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 05/13/2019
ms.locfileid: "1540877"
---
# <a name="pause-service-updates-through-lifecycle-services-lcs"></a><span data-ttu-id="8b6e6-103">Lifecycle Services (LCS) によるサービスの更新の一時停止</span><span class="sxs-lookup"><span data-stu-id="8b6e6-103">Pause service updates through Lifecycle Services (LCS)</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="8b6e6-104">このトピックでは Microsoft Dynamics Lifecycle Services (LCS) を使用して、サンドボックスおよび運用環境の更新を一時停止する方法を説明します。</span><span class="sxs-lookup"><span data-stu-id="8b6e6-104">This topic explains how to pause updates to your sandbox and production environments by using Microsoft Dynamics Lifecycle Services (LCS).</span></span>

> [!IMPORTANT]
> <span data-ttu-id="8b6e6-105">この機能は **バージョン 8.1 以降** を使用しているお客様、または **バージョン 7.3** を使用していて、[初回リリース](../../fin-and-ops/get-started/public-preview-releases.md) プログラムに参加して **いない** お客様だけが利用できます。</span><span class="sxs-lookup"><span data-stu-id="8b6e6-105">This feature is available only to customers who are using **version 8.1 and later** or are using **version 7.3**, and who are **not** part of the [First release](../../fin-and-ops/get-started/public-preview-releases.md) program.</span></span> <span data-ttu-id="8b6e6-106">Microsoft はこの機能を初回リリースのお客様が利用できるようにすることを目指しています。</span><span class="sxs-lookup"><span data-stu-id="8b6e6-106">Microsoft is working to make the feature available to First release customers.</span></span> <span data-ttu-id="8b6e6-107">バージョン 7.1、7.2、または 8.0 のお客様は、通常のサービス フローを使用して手動で更新を行うことができます。</span><span class="sxs-lookup"><span data-stu-id="8b6e6-107">For customers who are on version 7.1, 7.2, or 8.0, you can take the update manually using the regular servicing flows.</span></span>

<span data-ttu-id="8b6e6-108">Microsoft は構成したサンドボックスおよび運用環境を、Microsoft がリリースした最新のサービス更新プログラムに更新します。</span><span class="sxs-lookup"><span data-stu-id="8b6e6-108">Microsoft updates your configured sandbox and production environments to the latest service update that Microsoft has released.</span></span> <span data-ttu-id="8b6e6-109">Microsoft はお客様の環境に対する今後の更新プログラムについて、電子メールまたは LCS の通知でお知らせします。</span><span class="sxs-lookup"><span data-stu-id="8b6e6-109">Microsoft notifies you about upcoming updates to your environments via email and through notifications in LCS.</span></span> <span data-ttu-id="8b6e6-110">その時点で何らかの理由で更新プログラムを続行できない場合は、LCS を介して一時停止できます。</span><span class="sxs-lookup"><span data-stu-id="8b6e6-110">At that point, if you can't proceed with the update for some reason, you can pause it through LCS.</span></span>

<span data-ttu-id="8b6e6-111">構成されたサンドボックス環境を変更して実稼働の更新頻度を設定する方法の詳細は、[Lifecycle Services (LCS) でサービス更新を構成する](configure-service-updates.md) を参照してください。</span><span class="sxs-lookup"><span data-stu-id="8b6e6-111">For more information about how to change the configured sandbox environment and set the production update cadence, see [Configure service updates through Lifecycle Services (LCS)](configure-service-updates.md).</span></span>

## <a name="who-can-pause-service-updates"></a><span data-ttu-id="8b6e6-112">誰がサービスの更新を一時停止できますか。</span><span class="sxs-lookup"><span data-stu-id="8b6e6-112">Who can pause service updates?</span></span>

<span data-ttu-id="8b6e6-113">LCS で **プロジェクト所有者** ロールが割り当てられているユーザー (顧客またはパートナー) のみが更新を一時停止できます。</span><span class="sxs-lookup"><span data-stu-id="8b6e6-113">Only users (customers or partners) who are assigned to the **project owner** role in LCS can pause updates.</span></span> <span data-ttu-id="8b6e6-114">さらに、更新は **実装プロジェクト** に対してのみ一時停止できます。</span><span class="sxs-lookup"><span data-stu-id="8b6e6-114">Additionally, updates can be paused only for **implementation projects**.</span></span>

<span data-ttu-id="8b6e6-115">サービスの更新プログラムを最新の状態に保つことで Microsoft がリリースした一連の修正を常にお客様に実行し、最高のサービス エクスペリエンスを提供します。</span><span class="sxs-lookup"><span data-stu-id="8b6e6-115">Staying current with service updates helps guarantee that customers always run on the latest set of fixes that Microsoft has released, so that they have the best service experience.</span></span> <span data-ttu-id="8b6e6-116">したがって、Microsoft は更新プログラムを無期限に停止することを許可しません。</span><span class="sxs-lookup"><span data-stu-id="8b6e6-116">Therefore, Microsoft doesn't allow updates to be paused indefinitely.</span></span>

<span data-ttu-id="8b6e6-117">Microsoft がリリースした最新の更新プログラムから 2 つ前よりも更新が遅れている場合、LCS で更新プログラムを一時停止できません。</span><span class="sxs-lookup"><span data-stu-id="8b6e6-117">You can't pause updates through LCS if you're more than two updates behind the latest update that Microsoft has released.</span></span> <span data-ttu-id="8b6e6-118">たとえば、バージョン8.1以降を利用している環境で、Microsoftが最後にリリースした更新プログラムがバージョン8.1.3であった場合、バージョン 8.1.2 または バージョン 8.1.1 を利用しているユーザーは更新プログラムを一時停止 **することができます** 。</span><span class="sxs-lookup"><span data-stu-id="8b6e6-118">For example, if you are on version 8.1 and higher, if the last update that Microsoft released is version 8.1.3, customers who are using version 8.1.2 and version 8.1.1 **can** pause updates.</span></span> <span data-ttu-id="8b6e6-119">しかし、バージョン 8.1.0 を使用しているユーザーは更新が必要なプログラムが2つ以上残っているため更新プログラムを一時停止 **できません** 。</span><span class="sxs-lookup"><span data-stu-id="8b6e6-119">However, a customer who is using version 8.1.0 **cannot** ppause updates, because they are more than two updates behind.</span></span> <span data-ttu-id="8b6e6-120">バージョン7.3を使用している場合は、プラットフォームの更新のみが適用されます。</span><span class="sxs-lookup"><span data-stu-id="8b6e6-120">For customers who are on version 7.3, you get platform updates only.</span></span> <span data-ttu-id="8b6e6-121">たとえば、Microsoftがリリースした最新のプラットフォーム更新が 24の場合、プラットフォーム更新プログラム 23 と更新 22 **のユーザーは** 一時停止することができます。</span><span class="sxs-lookup"><span data-stu-id="8b6e6-121">For example, if the last platform update that Microsoft released is Platform update 24, then customers who are on Platform update 23 and update 22 **can** pause.</span></span> <span data-ttu-id="8b6e6-122">ただし、プラットフォーム更新プログラム21を使用している場合は、一時停止することは **できません** 。</span><span class="sxs-lookup"><span data-stu-id="8b6e6-122">However, if you are on Platform update 21, then you **cannot** pause.</span></span> 

## <a name="what-can-i-pause"></a><span data-ttu-id="8b6e6-123">何を一時停止できますか。</span><span class="sxs-lookup"><span data-stu-id="8b6e6-123">What can I pause?</span></span>

<span data-ttu-id="8b6e6-124">更新を一時停止する場合はオプションが 2 つあります:</span><span class="sxs-lookup"><span data-stu-id="8b6e6-124">If you decide to pause updates, you have two options:</span></span>

- <span data-ttu-id="8b6e6-125">実稼働環境に対してのみ更新プログラムを一時停止します。</span><span class="sxs-lookup"><span data-stu-id="8b6e6-125">Pause updates only to your production environment.</span></span>
- <span data-ttu-id="8b6e6-126">サンドボックスと実稼働環境の両方の更新プログラムを一時停止します。</span><span class="sxs-lookup"><span data-stu-id="8b6e6-126">Pause updates to both your sandbox environment and your production environment.</span></span>

<span data-ttu-id="8b6e6-127">最大 2 つの連続する更新プログラムを一度に一時停止できます。</span><span class="sxs-lookup"><span data-stu-id="8b6e6-127">You can pause a maximum of two continuous updates at a time.</span></span> <span data-ttu-id="8b6e6-128">付加情報として、最大で 3 ヶ月間更新プログラムを一時停止できます。</span><span class="sxs-lookup"><span data-stu-id="8b6e6-128">(According to other information that may have been communicated to you, you can pause updates for up to three months.</span></span> <span data-ttu-id="8b6e6-129">3か月間で2つの更新が入るため、これら2つの制約には整合性があります。 たとえば、バージョン 8.1.3 を使用している場合は、更新プログラム バージョン 10.0.0 と更新プログラム バージョン 10.0.1 を一時停止できます。</span><span class="sxs-lookup"><span data-stu-id="8b6e6-129">These two statements are consistent, because three months corresponds to two updates.) For example, if you're using version 8.1.3, you can pause update version 10.0.0 and update version 10.0.1.</span></span> <span data-ttu-id="8b6e6-130">ただし、更新プログラムのバージョン 10.0.2 を一時停止することはできません。</span><span class="sxs-lookup"><span data-stu-id="8b6e6-130">However, you can't pause update version 10.0.2.</span></span> <span data-ttu-id="8b6e6-131">さらに、4月には次に控えている2つの更新プログラムまで一時停止できます。</span><span class="sxs-lookup"><span data-stu-id="8b6e6-131">In addition, in the month of April, you can pause the next two updates.</span></span> <span data-ttu-id="8b6e6-132">しかし、7月と8月以降に予定されている更新プログラムを一時停止することはできません。</span><span class="sxs-lookup"><span data-stu-id="8b6e6-132">However, you will not be able to pause updates scheduled for July, August, and later.</span></span> <span data-ttu-id="8b6e6-133">同様に、7.3を利用しているユーザーにはプラットフォームの更新のみが適用されますが、プラットフォーム23を使用している場合は24と25の更新を一時停止することはできますが、プラットフォーム26を一時停止することはできません。</span><span class="sxs-lookup"><span data-stu-id="8b6e6-133">Similarly, for customers on version 7.3 for platform only updates, if you’re using Platform update 23 then you can pause update 24 and update 25, but you cannot pause update 26.</span></span>

> [!IMPORTANT]
>  <span data-ttu-id="8b6e6-134">業界または業務上のスケジュールを問わず、2つ以上の更新を停止することはできません。</span><span class="sxs-lookup"><span data-stu-id="8b6e6-134">There is no way to pause more than two updates, regardless of your industry or business schedule.</span></span> <span data-ttu-id="8b6e6-135">2つ以上の更新が控えている状態で、更新完了後の検証の段階でサンドボックス環境内に致命的な問題を発見した場合は、Microsoftサポートにご連絡の上Production環境の更新停止を依頼してください。</span><span class="sxs-lookup"><span data-stu-id="8b6e6-135">If you are more than 2 updates behind and you find a critical issue during validations in your sandbox environment after the update, you can contact Microsoft Support to pause the update to your production environment.</span></span> <span data-ttu-id="8b6e6-136">2つ以上の更新が控えている状態で、かつLCSに実装されている更新の停止機能を使ってProductionの更新停止を実行できない場合にのみ必要となります。</span><span class="sxs-lookup"><span data-stu-id="8b6e6-136">This is only required if you are more than two updates behind and you are unable to use the pause updates functionality available in LCS to pause the update to production.</span></span>

> <span data-ttu-id="8b6e6-137">サンドボックス環境への更新を一時停止する場合は、実稼働環境への更新も自動的に一時停止されます。これは、Microdoftが常に実稼働環境よりも先にに構成済みのサンドボックス環境を更新するためです。</span><span class="sxs-lookup"><span data-stu-id="8b6e6-137">If you pause updates to your sandbox environment, updates are automatically also paused for your production environment, because Microsoft always updates configured sandbox environments before production environments.</span></span>

## <a name="how-do-i-pause-updates"></a><span data-ttu-id="8b6e6-138">更新プログラムを一時停止する方法。</span><span class="sxs-lookup"><span data-stu-id="8b6e6-138">How do I pause updates?</span></span>

<span data-ttu-id="8b6e6-139">更新プログラムを一時停止するには、以下の手順を実行します。</span><span class="sxs-lookup"><span data-stu-id="8b6e6-139">To pause updates, follow these steps.</span></span>

1. <span data-ttu-id="8b6e6-140">実装プロジェクトの LCS で **プロジェクト設定** ページを開きます。</span><span class="sxs-lookup"><span data-stu-id="8b6e6-140">In LCS, in your implementation project, open the **Project settings** page.</span></span>

    <span data-ttu-id="8b6e6-141">このページには **更新プログラムの設定** という名前の新しいタブがあります。</span><span class="sxs-lookup"><span data-stu-id="8b6e6-141">This page has a new tab that is named **Update settings**.</span></span>

2. <span data-ttu-id="8b6e6-142">**更新プログラムの設定** タブで、**更新プログラムの一時停止** オプションを **オン** に設定します。</span><span class="sxs-lookup"><span data-stu-id="8b6e6-142">On the **Update settings** tab, set the **Pause updates** option to **ON**.</span></span>
3. <span data-ttu-id="8b6e6-143">**設定の編集** を選択します。</span><span class="sxs-lookup"><span data-stu-id="8b6e6-143">Select **Edit settings**.</span></span>
4. <span data-ttu-id="8b6e6-144">表示されるダイアログ ボックスで、実稼働環境の更新プログラムのみを一時停止するか、またはサンドボックス環境と実稼働環境の両方で更新を一時停止するかを選択します。</span><span class="sxs-lookup"><span data-stu-id="8b6e6-144">In the dialog box that appears, select whether you want to pause updates to your production environment only, or to both your sandbox environment and your production environment.</span></span>
5. <span data-ttu-id="8b6e6-145">**次へ** を選択します。</span><span class="sxs-lookup"><span data-stu-id="8b6e6-145">Select **Next**.</span></span>
6. <span data-ttu-id="8b6e6-146">更新プログラムを一時停止する理由を選択してください。</span><span class="sxs-lookup"><span data-stu-id="8b6e6-146">Select your reason for pausing updates.</span></span> <span data-ttu-id="8b6e6-147">**検証中に問題が見つかりました** を選択した場合は、有効なサポート チケット番号を入力する必要があります。</span><span class="sxs-lookup"><span data-stu-id="8b6e6-147">If you select **Issue found during validations**, you must enter a valid support ticket number.</span></span> <span data-ttu-id="8b6e6-148">更新プログラムを一時停止する理由を Microsoft が理解するためにさらに詳細情報を追加できます。</span><span class="sxs-lookup"><span data-stu-id="8b6e6-148">You can add any additional details that will help Microsoft understand why you want to pause updates.</span></span>
7. <span data-ttu-id="8b6e6-149">完了したら、**確定** を選択します。</span><span class="sxs-lookup"><span data-stu-id="8b6e6-149">When you've finished, select **Confirm**.</span></span>

<span data-ttu-id="8b6e6-150">既存の一時停止を編集することもできます。</span><span class="sxs-lookup"><span data-stu-id="8b6e6-150">You can also edit an existing pause.</span></span> <span data-ttu-id="8b6e6-151">一時停止の期間を延長して更新プログラムをより長い時間停止するか、キャンセルして更新プログラムを再開することができます。</span><span class="sxs-lookup"><span data-stu-id="8b6e6-151">You can either extend the duration of the pause, so that updates are paused for a longer time, or cancel it, so that updates are resumed.</span></span> <span data-ttu-id="8b6e6-152">一時停止を編集するには、**設定を編集** を選択します。</span><span class="sxs-lookup"><span data-stu-id="8b6e6-152">To edit a pause, select **Edit settings**.</span></span> <span data-ttu-id="8b6e6-153">一時停止できる更新プログラムの数に関する制限がまだ適用されます。</span><span class="sxs-lookup"><span data-stu-id="8b6e6-153">The limitations about the number of updates that you can pause still apply.</span></span>

<span data-ttu-id="8b6e6-154">一時停止をキャンセルして環境に対する更新プログラムを再開するには、**更新プログラムを一時停止** オプションを **オフ** に設定します。</span><span class="sxs-lookup"><span data-stu-id="8b6e6-154">To cancel a pause and resume updates to your environments, set the **Pause updates** option to **OFF**.</span></span>

<span data-ttu-id="8b6e6-155">更新プログラムの一時停止や既存の一時停止を編集をしたときは、**設定の更新** タブの上部に通知が表示されます。この通知は一時停止された内容を示します。</span><span class="sxs-lookup"><span data-stu-id="8b6e6-155">Any time that you pause updates or edit an existing pause, a notification appears at the top of the **Update settings** tab. This notification shows what has been paused.</span></span> <span data-ttu-id="8b6e6-156">選択した環境のサービス更新プログラムの一時停止を通知するために、すべての関係者 (プロジェクト所有者および環境管理者) にも電子メールが送信されます。</span><span class="sxs-lookup"><span data-stu-id="8b6e6-156">An email is also sent to all stakeholders (the project owner and environment manager), to notify them that service updates for the selected environments have been paused.</span></span> <span data-ttu-id="8b6e6-157">誰かが既存の一時停止をキャンセルして更新プログラムを再開すると、通知が消えて更新プログラムの再開を関係者に通知する電子メールが送信されます。</span><span class="sxs-lookup"><span data-stu-id="8b6e6-157">If someone cancels an existing pause and resumes updates, the notification disappears, and an email is sent to inform the stakeholders that updates have resumed.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="8b6e6-158">ダウンタイム時間枠が始まる 4 時間前まで LCS から更新プログラムを一時停止できます。</span><span class="sxs-lookup"><span data-stu-id="8b6e6-158">You can pause updates through LCS until four hours before the start of the downtime window.</span></span>

> <span data-ttu-id="8b6e6-159">一時停止をキャンセルし、更新予定の7日前までの期間で更新を再開するように選択できます。</span><span class="sxs-lookup"><span data-stu-id="8b6e6-159">You can cancel a pause and choose to resume updates only 7 days prior to the start of the downtime date.</span></span> <span data-ttu-id="8b6e6-160">この日付を過ぎている場合、一時停止をキャンセルすることはできません。</span><span class="sxs-lookup"><span data-stu-id="8b6e6-160">If you are past that date then you will not be able to cancel a pause.</span></span>

## <a name="what-happens-after-the-pause-duration-expires"></a><span data-ttu-id="8b6e6-161">一時停止の期間を超えた後はどうなりますか。</span><span class="sxs-lookup"><span data-stu-id="8b6e6-161">What happens after the pause duration expires?</span></span>

<span data-ttu-id="8b6e6-162">サービス更新プログラムの積み重ねにより Microsoft がリリースした一連の修正を常にお客様に実行し、最高のサービス エクスペリエンスを提供します。</span><span class="sxs-lookup"><span data-stu-id="8b6e6-162">Cumulative service updates help guarantee that customers always run on the latest set of fixes that Microsoft has released, so that they have the best service experience.</span></span> <span data-ttu-id="8b6e6-163">したがって、Microsoft は更新プログラムを無期限に停止することを許可しません。</span><span class="sxs-lookup"><span data-stu-id="8b6e6-163">Therefore, Microsoft doesn't allow updates to be paused indefinitely.</span></span>

<span data-ttu-id="8b6e6-164">更新プログラムを再開するために一時停止をキャンセルする方法が 2 つあります。</span><span class="sxs-lookup"><span data-stu-id="8b6e6-164">There are two ways to cancel pauses, so that updates are resumed:</span></span>

- <span data-ttu-id="8b6e6-165">前のセクションで説明したように、誰かが継続中の一時停止を手動でキャンセルします。</span><span class="sxs-lookup"><span data-stu-id="8b6e6-165">Someone manually cancels an ongoing pause, as explained in the previous section.</span></span>
- <span data-ttu-id="8b6e6-166">一時停止に設定された期間が過ぎると、構成された環境への更新プログラムが自動的に再開します。</span><span class="sxs-lookup"><span data-stu-id="8b6e6-166">The duration that was set for the pause expires, and updates to the configured environments are automatically resumed.</span></span>

<span data-ttu-id="8b6e6-167">どちらの場合も、関係者に通知するために電子メールが送信されます。</span><span class="sxs-lookup"><span data-stu-id="8b6e6-167">In both cases, an email is sent to inform the stakeholders.</span></span>

<span data-ttu-id="8b6e6-168">サービス更新プログラムに関する詳細は [1 つのバージョンのサービス更新に関するよく寄せられる質問](../../fin-and-ops/get-started/one-version.md) を参照してください。</span><span class="sxs-lookup"><span data-stu-id="8b6e6-168">For more information about service updates, see [One Version service updates FAQ](../../fin-and-ops/get-started/one-version.md).</span></span>
