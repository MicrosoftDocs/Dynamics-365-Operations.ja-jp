---
title: 予定された保守ウィンドウのよく寄せられる質問
description: このトピックでは、Microsoft の計画されたメンテナンス ウィンドウに関するよくある質問に対する回答を示します。
author: angelmarshall
manager: AnnBe
ms.date: 10/15/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Developer, IT Pro
ms.reviewer: sericks
ms.custom: 6154
ms.search.region: Global
ms.author: tsmarsha
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 1b98c5bb6a08740ac367974d98e852f0250ee254
ms.sourcegitcommit: 659375c4cc7f5524cbf91cf6160f6a410960ac16
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 12/05/2020
ms.locfileid: "4687894"
---
# <a name="planned-maintenance-window-faq"></a><span data-ttu-id="4cf36-103">予定された保守ウィンドウのよく寄せられる質問</span><span class="sxs-lookup"><span data-stu-id="4cf36-103">Planned maintenance window FAQ</span></span>
[!include [banner](../includes/banner.md)]

### <a name="what-is-a-planned-maintenance-window"></a><span data-ttu-id="4cf36-104">計画されているメンテナンス期間とは何ですか ?</span><span class="sxs-lookup"><span data-stu-id="4cf36-104">What is a planned maintenance window?</span></span>
<span data-ttu-id="4cf36-105">メンテナンス予定期間は、機器設備や [サービス](../../fin-ops/get-started/one-version.md) に関する重要な更新を適用するために Microsoft がスケジュール設定をした時間枠です。</span><span class="sxs-lookup"><span data-stu-id="4cf36-105">A planned maintenance window is the timeframe that Microsoft has scheduled to apply infrastructure or [service updates](../../fin-ops/get-started/one-version.md) to your cloud service.</span></span>

### <a name="how-does-a-planned-maintenance-window-work"></a><span data-ttu-id="4cf36-106">計画されているメンテナンス ウィンドウはどのように機能しますか。</span><span class="sxs-lookup"><span data-stu-id="4cf36-106">How does a planned maintenance window work?</span></span>
<span data-ttu-id="4cf36-107">レベル 2 からレベル 5 のサンドボックス環境および実稼働環境でスケジュールされた計画的保守については、パッチ適用を開始する **5 日前** に Microsoft がすべての利害関係者に通知を送信します。</span><span class="sxs-lookup"><span data-stu-id="4cf36-107">For planned maintenance scheduled on your Tier 2 through Tier 5 sandbox environments and production environments, Microsoft will send a notification to all stakeholders **five business days** before the start of the patching window.</span></span> <span data-ttu-id="4cf36-108">パッチ適用枠は環境にパッチが適用される期間です。</span><span class="sxs-lookup"><span data-stu-id="4cf36-108">The patching window is the period when the environment is patched.</span></span> <span data-ttu-id="4cf36-109">それは地理的な地域によって定義されます。</span><span class="sxs-lookup"><span data-stu-id="4cf36-109">It's defined by geographic region.</span></span> <span data-ttu-id="4cf36-110">保守活動に関する詳細は、関係者に送信される通知に含まれます。</span><span class="sxs-lookup"><span data-stu-id="4cf36-110">Details about the maintenance activity will be included in the notification that is sent to stakeholders.</span></span> <span data-ttu-id="4cf36-111">Microsoft が管理するレベル 1 の環境では、更新前に通知は送信されません。</span><span class="sxs-lookup"><span data-stu-id="4cf36-111">For Microsoft-managed Tier 1 environments, we will not send any notifications before the update.</span></span> 

### <a name="when-is-this-planned-maintenance-window-taken"></a><span data-ttu-id="4cf36-112">この計画済みメンテナンス ウィンドウはいつ使用されますか ?</span><span class="sxs-lookup"><span data-stu-id="4cf36-112">When is this planned maintenance window taken?</span></span>
<span data-ttu-id="4cf36-113">ユーザーへの影響を制限するため、環境が配置されている地域に応じてメンテナンス ウィンドウが予定されています。</span><span class="sxs-lookup"><span data-stu-id="4cf36-113">To limit the impact on users, the maintenance window is planned according to the region where environments are deployed.</span></span> <span data-ttu-id="4cf36-114">次のリストは、各地域のメンテナンス ウィンドウを示しています。</span><span class="sxs-lookup"><span data-stu-id="4cf36-114">The following list shows the maintenance window for each region.</span></span> <span data-ttu-id="4cf36-115">すべての環境は、これら 3 つの地域のいずれかに分類されます。</span><span class="sxs-lookup"><span data-stu-id="4cf36-115">All environments fall into one of these three regions.</span></span> <span data-ttu-id="4cf36-116">時間は協定世界時 (UTC、グリニッジ標準時) で表示されます。</span><span class="sxs-lookup"><span data-stu-id="4cf36-116">The times are shown in Coordinated Universal Time (UTC, which is also known as Greenwich Mean Time).</span></span>

- <span data-ttu-id="4cf36-117">**NAM:** 午前 2 時から午前 10 時</span><span class="sxs-lookup"><span data-stu-id="4cf36-117">**NAM:** 2 AM to 10 AM</span></span>
- <span data-ttu-id="4cf36-118">**EMEA:** 午後 10 時から午前 6 時</span><span class="sxs-lookup"><span data-stu-id="4cf36-118">**EMEA:** 10 PM to 6 AM</span></span>
- <span data-ttu-id="4cf36-119">**APAC:** 午後 12 時から午後 9 時</span><span class="sxs-lookup"><span data-stu-id="4cf36-119">**APAC:** 12 PM to 9 PM</span></span>

### <a name="will-the-maintenance-from-microsoft-require-any-uptake"></a><span data-ttu-id="4cf36-120">Microsoft からの保守では何かを取得することが必要ですか。</span><span class="sxs-lookup"><span data-stu-id="4cf36-120">Will the maintenance from Microsoft require any uptake?</span></span>
<span data-ttu-id="4cf36-121">ほとんどの保守作業でユーザー側のアクションは不要です。</span><span class="sxs-lookup"><span data-stu-id="4cf36-121">Most of the maintenance operations require no action on your end.</span></span> <span data-ttu-id="4cf36-122">取得が必要な重要なセキュリティ更新プログラムがある場合は、通知されます。</span><span class="sxs-lookup"><span data-stu-id="4cf36-122">If there is a critical security update that requires uptake, you will be notified.</span></span>

### <a name="who-will-be-notified-about-the-upcoming-planned-maintenance"></a><span data-ttu-id="4cf36-123">将来の計画的なメンテナンスはだれに通知されますか。</span><span class="sxs-lookup"><span data-stu-id="4cf36-123">Who will be notified about the upcoming planned maintenance?</span></span>
<span data-ttu-id="4cf36-124">次の利害関係者には、今後のメンテナンスについて通知されます。</span><span class="sxs-lookup"><span data-stu-id="4cf36-124">The following stakeholders will be notified about the upcoming maintenance:</span></span>

- <span data-ttu-id="4cf36-125">プロジェクト所有者</span><span class="sxs-lookup"><span data-stu-id="4cf36-125">Project owners</span></span>
- <span data-ttu-id="4cf36-126">組織の管理者</span><span class="sxs-lookup"><span data-stu-id="4cf36-126">Organization admins</span></span>
- <span data-ttu-id="4cf36-127">環境管理者</span><span class="sxs-lookup"><span data-stu-id="4cf36-127">Environment admins</span></span>
- <span data-ttu-id="4cf36-128">デプロイ中または Microsoft Dynamics Lifecycle Services (LCS) で環境の詳細ページにある **通知する** ボタンによりリストに指定されたその他のユーザー。</span><span class="sxs-lookup"><span data-stu-id="4cf36-128">Other people who are specified in the list during deployment or through the **Notify** button on the environment details page in Microsoft Dynamics Lifecycle Services (LCS)</span></span>

### <a name="how-do-i-sign-up-to-be-notified-about-the-maintenance-window"></a><span data-ttu-id="4cf36-129">メンテナンス ウィンドウに関して通知を受け取るよう登録するにはどうすればよいですか。</span><span class="sxs-lookup"><span data-stu-id="4cf36-129">How do I sign up to be notified about the maintenance window?</span></span>
<span data-ttu-id="4cf36-130">任意のパートナー、独立系ソフトウェア仕入先 (ISV)、および次回の更新プログラムについて通知を受けたいその他の関係者は、関連する利害関係者 (プロジェクト所有者、環境管理者、または追加の関係者) として LCS プロジェクトに追加するよう依頼できます。</span><span class="sxs-lookup"><span data-stu-id="4cf36-130">Any partner, independent software vendor (ISV), and other interested party who wants to be notified about upcoming updates can request to be added to the LCS project as a relevant stakeholder (project owner, environment admin, or additional stakeholder).</span></span>

### <a name="why-cant-these-updates-be-applied-in-zero-downtime"></a><span data-ttu-id="4cf36-131">これらの更新プログラムがゼロ ダウンタイムで適用できないのはなぜですか。</span><span class="sxs-lookup"><span data-stu-id="4cf36-131">Why can't these updates be applied in zero downtime?</span></span>
<span data-ttu-id="4cf36-132">Microsoft はサービスのダウンタイムの必要性を減らすよう継続的に努力しており、多くの定期的な保守作業ではダウンタイムを発生しません。</span><span class="sxs-lookup"><span data-stu-id="4cf36-132">Microsoft is continually working to reduce the necessity of downtime for the service, and many regular maintenance tasks don't incur downtime.</span></span> <span data-ttu-id="4cf36-133">しかし、予測可能性を保証するため、Microsoft はゼロ ダウンタイムですべてのパッチを実行することはまだできません。</span><span class="sxs-lookup"><span data-stu-id="4cf36-133">However, to help guarantee the most predictability, Microsoft can't yet do all patching in zero downtime.</span></span>

## <a name="microsoft-service-updates"></a><span data-ttu-id="4cf36-134">Microsoft のサービス更新プログラム</span><span class="sxs-lookup"><span data-stu-id="4cf36-134">Microsoft service updates</span></span> 
<span data-ttu-id="4cf36-135">別のよく寄せられる質問 (FAQ) に Microsoft によって行われるサービス更新プログラムに関する詳細が記載されています。</span><span class="sxs-lookup"><span data-stu-id="4cf36-135">A separate set of frequently asked questions (FAQ) provides details about service updates that are done by Microsoft.</span></span> <span data-ttu-id="4cf36-136">[1 つのバージョンのサービス更新プログラムに関してよく寄せられる質問](../../fin-ops/get-started/one-version.md) を参照してください。</span><span class="sxs-lookup"><span data-stu-id="4cf36-136">See [One Version service updates FAQ](../../fin-ops/get-started/one-version.md).</span></span>

## <a name="infrastructure-updates"></a><span data-ttu-id="4cf36-137">機器設備の更新</span><span class="sxs-lookup"><span data-stu-id="4cf36-137">Infrastructure updates</span></span> 

### <a name="how-long-is-the-maintenance-window"></a><span data-ttu-id="4cf36-138">メンテナンス ウィンドウの長さはどの程度ですか。</span><span class="sxs-lookup"><span data-stu-id="4cf36-138">How long is the maintenance window?</span></span>
<span data-ttu-id="4cf36-139">ほとんどのオペレーティング システム レベルの更新は約 1 時間で完了します。</span><span class="sxs-lookup"><span data-stu-id="4cf36-139">Most operating system–level updates are completed in approximately one hour.</span></span> <span data-ttu-id="4cf36-140">ただし、障害を処理してシステムを正常な状態に戻す時間があるため、Microsoft は 3 時間の時間枠を要求しています。</span><span class="sxs-lookup"><span data-stu-id="4cf36-140">However, Microsoft asks for a three-hour window, so that there is time to handle any failures and to bring the system back to a healthy state.</span></span> 

<span data-ttu-id="4cf36-141">すべてのアップデートの正確なダウンタイムは、アップデート開始前に通知されるメンテナンス ウィンドウ通知電子メールに含まれます。</span><span class="sxs-lookup"><span data-stu-id="4cf36-141">The exact downtime for all updates will be included in the maintenance window notification email that is sent to you before the start of the update.</span></span>

### <a name="how-frequent-are-the-updates"></a><span data-ttu-id="4cf36-142">更新の頻度を選択してください。</span><span class="sxs-lookup"><span data-stu-id="4cf36-142">How frequent are the updates?</span></span>
<span data-ttu-id="4cf36-143">オペレーティング システムレベルの更新は、Microsoft が管理するレベル 2 からレベル 5 のサンドボックス環境と実稼働環境に毎月適用されます。</span><span class="sxs-lookup"><span data-stu-id="4cf36-143">Operating system–level updates are applied monthly to your Microsoft-managed Tier 2 through Tier 5 sandbox environments and to the production environments.</span></span> <span data-ttu-id="4cf36-144">ただし、Microsoft が管理するレベル 1 環境は、地域ごとに定義されたメンテナンス期間に毎週更新されます。</span><span class="sxs-lookup"><span data-stu-id="4cf36-144">However, Microsoft-managed Tier 1 environments are updated weekly in the maintenance windows defined per region.</span></span>

### <a name="where-can-i-learn-more-about-what-is-applied"></a><span data-ttu-id="4cf36-145">何が適用されたかについての詳細はどこですか。</span><span class="sxs-lookup"><span data-stu-id="4cf36-145">Where can I learn more about what is applied?</span></span>
<span data-ttu-id="4cf36-146">適用される更新プログラムの詳細については、[Microsoft セキュリティ速報](https://technet.microsoft.com/security/bulletins.aspx) を参照してください。</span><span class="sxs-lookup"><span data-stu-id="4cf36-146">For more information about the updates that will be applied, see [Microsoft Security Bulletins](https://technet.microsoft.com/security/bulletins.aspx).</span></span>

### <a name="where-can-i-track-progress-of-the-update"></a><span data-ttu-id="4cf36-147">更新プログラムの進捗はどのように追跡できますか。</span><span class="sxs-lookup"><span data-stu-id="4cf36-147">Where can I track progress of the update?</span></span>
<span data-ttu-id="4cf36-148">オペレーティング システム レベルの更新中に、LCS は現在どのパッチ適用が進行中であるかを示しません。</span><span class="sxs-lookup"><span data-stu-id="4cf36-148">During operating system–level updates, LCS doesn't currently indicate that any patching is in progress.</span></span> <span data-ttu-id="4cf36-149">ただし、Microsoft はこの機能をある時点で追加する予定です。</span><span class="sxs-lookup"><span data-stu-id="4cf36-149">However, Microsoft plans to add this functionality at some point.</span></span>

### <a name="what-environments-are-updated"></a><span data-ttu-id="4cf36-150">なんの環境が更新されるか。</span><span class="sxs-lookup"><span data-stu-id="4cf36-150">What environments are updated?</span></span>
<span data-ttu-id="4cf36-151">オペレーティング システム レベルの更新は、Microsoft の基本サービスの一部として含まれているすべての Microsoft が管理する環境に適用されます。</span><span class="sxs-lookup"><span data-stu-id="4cf36-151">Operating system–level updates are applied to all Microsoft-managed environments that are included as part of the Microsoft base offer.</span></span> <span data-ttu-id="4cf36-152">これには、レベル 1、レベル 2 からレベル 5、および実稼働環境が含まれます。</span><span class="sxs-lookup"><span data-stu-id="4cf36-152">This includes your Tier 1, Tier 2 through Tier 5, and Production environments.</span></span> <span data-ttu-id="4cf36-153">購入済のアドオンにも適用されます。</span><span class="sxs-lookup"><span data-stu-id="4cf36-153">They are also applied to add-ons that have been purchased.</span></span> <span data-ttu-id="4cf36-154">ただし、サブスクリプションでホストされている他の環境 (クラウド ホスト環境など) は、顧客またはパートナーが責任を負います。</span><span class="sxs-lookup"><span data-stu-id="4cf36-154">However, other environments, such as environments hosted in your subscription (known as Cloud hosted environments), are the responsibility of the customer or partner.</span></span>

### <a name="what-notifications-will-i-receive-about-upcoming-planned-maintenance"></a><span data-ttu-id="4cf36-155">次回の計画済みメンテナンスに関してどのような通知を受け取りますか ?</span><span class="sxs-lookup"><span data-stu-id="4cf36-155">What notifications will I receive about upcoming planned maintenance?</span></span>
<span data-ttu-id="4cf36-156">更新が予定されている 5 日前に、レベル 2 からレベル 5 のサンドボックス環境および実稼動環境でスケジュールされた更新の通知電子メールが届きます。</span><span class="sxs-lookup"><span data-stu-id="4cf36-156">You will receive a notification email for the scheduled update on your Tier 2 to Tier 5 sandbox environment and production environment, five days before the update is scheduled to occur.</span></span> <span data-ttu-id="4cf36-157">この電子メールには、更新される環境、更新の種類、更新が実行する見積もり時間、および実行する必要のある操作に関する情報が含まれます。</span><span class="sxs-lookup"><span data-stu-id="4cf36-157">This email will include information about the environments that will be updated, the update type, the estimated amount of time that the update will take, and any action that you might have to take.</span></span> <span data-ttu-id="4cf36-158">Microsoft が管理するレベル 1 環境の通知は送信されません。</span><span class="sxs-lookup"><span data-stu-id="4cf36-158">We do not send notifications for Microsoft-managed Tier 1 environments.</span></span> 

### <a name="will-i-be-notified-when-the-update-is-completed"></a><span data-ttu-id="4cf36-159">更新プログラムの完了時に通知されますか。</span><span class="sxs-lookup"><span data-stu-id="4cf36-159">Will I be notified when the update is completed?</span></span>
<span data-ttu-id="4cf36-160">定義された保守時間枠で更新が完了する場合、更新が完了したときに通知を受信しません。</span><span class="sxs-lookup"><span data-stu-id="4cf36-160">If your update is completed within the defined maintenance window, you won't receive any notification when the update is completed.</span></span> 

### <a name="how-do-i-report-an-issue-that-is-identified-during-validation-of-the-updates-that-were-applied-to-the-environment"></a><span data-ttu-id="4cf36-161">環境に適用された更新の検証時に識別される問題をレポートするにはどうすればよいですか。</span><span class="sxs-lookup"><span data-stu-id="4cf36-161">How do I report an issue that is identified during validation of the updates that were applied to the environment?</span></span>
<span data-ttu-id="4cf36-162">更新の検証中に特定された問題を報告するには、Microsoft にサポート チケットを提出し、タイトルに '予定された保守時間枠' を追加します。</span><span class="sxs-lookup"><span data-stu-id="4cf36-162">To report an issue that is identified during update validation, file a support ticket with Microsoft and append the title with 'Planned Maintenance Window'.</span></span>

### <a name="what-happens-if-the-patching-fails"></a><span data-ttu-id="4cf36-163">ファイルの修正に失敗した場合はどうなるでしょうか ?</span><span class="sxs-lookup"><span data-stu-id="4cf36-163">What happens if the patching fails?</span></span>
<span data-ttu-id="4cf36-164">修正が、オペレーティング システム レベル更新中に失敗すると、特定の修正プログラムはスキップされ、次の更新サイクルで適用されます。</span><span class="sxs-lookup"><span data-stu-id="4cf36-164">If the patching fails during an operating system–level update, the specific patch is skipped and will be applied in the next update cycle.</span></span>

### <a name="will-i-be-compensated-if-the-update-takes-longer-than-the-scheduled-maintenance-window"></a><span data-ttu-id="4cf36-165">更新プログラムが予定メンテナンス ウインドウより時間がかかる場合は補償されますか。</span><span class="sxs-lookup"><span data-stu-id="4cf36-165">Will I be compensated if the update takes longer than the scheduled maintenance window?</span></span>
<span data-ttu-id="4cf36-166">更新が予定された保守ウィンドウよりも長い場合は、余分な時間は予定外のダウンタイムと見なされ、一般的なサービス レベル アグリーメント (SLA) の対象となります。</span><span class="sxs-lookup"><span data-stu-id="4cf36-166">If the update takes longer than the scheduled maintenance window, the extra time is considered unplanned downtime and is subject to the general service level agreement (SLA).</span></span>

### <a name="how-do-i-reschedule-security-maintenance-activities"></a><span data-ttu-id="4cf36-167">セキュリティ管理活動を再スケジュールする方法</span><span class="sxs-lookup"><span data-stu-id="4cf36-167">How do I reschedule security maintenance activities?</span></span>
<span data-ttu-id="4cf36-168">セキュリティ メンテナンスは、安全な環境の確保するのに役立ちます。メンテナンスを行わないと、回避可能なセキュリティ リスクを招く可能性があります。</span><span class="sxs-lookup"><span data-stu-id="4cf36-168">Security maintenance helps ensure a secure environment, and not doing the maintenance could potentially introduce an avoidable security risk.</span></span> 

<span data-ttu-id="4cf36-169">絶対的なビジネス ニーズがあり、上記の期間中にこのメンテナンスを行うことができない場合は、Microsoft にサポート チケットを提出することにより、第 2 層から第 5 層のサンドボックス環境と実稼働環境の現在のメンテナンス活動の再スケジュールを要求できます。</span><span class="sxs-lookup"><span data-stu-id="4cf36-169">If there is an absolute business need and you are unable to move forward with this maintenance during the timeframe listed above, you can request to reschedule the current maintenance activity for Tier 2 through Tier 5 sandbox environments and production environments by filing a support ticket with Microsoft.</span></span> <span data-ttu-id="4cf36-170">再スケジュール要求をするサポート チケットの提出期限は、通知メールに記載されています。</span><span class="sxs-lookup"><span data-stu-id="4cf36-170">The deadline for filing the support ticket to request a reschedule will be included in your notification email.</span></span> <span data-ttu-id="4cf36-171">どんな要求も、締め切りを過ぎて送信された場合には受け付けられません。</span><span class="sxs-lookup"><span data-stu-id="4cf36-171">Any request submitted after that deadline will not be honored.</span></span> 

<span data-ttu-id="4cf36-172">Microsoft が管理する第 1 層の環境では、セキュリティ管理活動を再スケジューリングすることはできません。</span><span class="sxs-lookup"><span data-stu-id="4cf36-172">We do not offer rescheduling of security maintenance activities on Microsoft-managed Tier 1 environments.</span></span>
