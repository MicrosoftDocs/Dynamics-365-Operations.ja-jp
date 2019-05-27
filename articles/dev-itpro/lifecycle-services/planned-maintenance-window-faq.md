---
title: 予定された保守ウィンドウのよく寄せられる質問
description: このトピックでは、Microsoft の計画されたメンテナンス ウィンドウに関するよくある質問に対する回答を示します。
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
ms.custom: 6154
ms.search.region: Global
ms.author: manado
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 8eeee27b964fa4412ecb008836f4f1ef30c2b942
ms.sourcegitcommit: f7a1e74a639dfbe470f7d57d4fc55e3bf4c6a74a
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 05/13/2019
ms.locfileid: "1540876"
---
# <a name="planned-maintenance-window-faq"></a><span data-ttu-id="743b4-103">予定された保守ウィンドウのよく寄せられる質問</span><span class="sxs-lookup"><span data-stu-id="743b4-103">Planned maintenance window FAQ</span></span>
[!include [banner](../includes/banner.md)]

### <a name="what-is-a-planned-maintenance-window"></a><span data-ttu-id="743b4-104">計画されているメンテナンス期間とは何ですか ?</span><span class="sxs-lookup"><span data-stu-id="743b4-104">What is a planned maintenance window?</span></span>
<span data-ttu-id="743b4-105">メンテナンス予定期間は、機器設備や [サービス](../../fin-and-ops/get-started/one-version.md) に関する重要な更新を適用するために Microsoft がスケジュール設定をした時間枠です。</span><span class="sxs-lookup"><span data-stu-id="743b4-105">A planned maintenance window is the timeframe that Microsoft has scheduled to apply infrastructure or [service updates](../../fin-and-ops/get-started/one-version.md) to your cloud service.</span></span>

### <a name="how-does-a-planned-maintenance-window-work"></a><span data-ttu-id="743b4-106">計画されているメンテナンス ウィンドウはどのように機能しますか。</span><span class="sxs-lookup"><span data-stu-id="743b4-106">How does a planned maintenance window work?</span></span>
<span data-ttu-id="743b4-107">すべての計画されたメンテナンスにつきましては、パッチ適用枠が開始する **5営業日** 前に Microsoft からすべての関係者にお知らせを送信します。</span><span class="sxs-lookup"><span data-stu-id="743b4-107">For all planned maintenance, Microsoft will send a notification to all stakeholders **five business days** before the start of the patching window.</span></span> <span data-ttu-id="743b4-108">パッチ適用枠は環境にパッチが適用される期間です。</span><span class="sxs-lookup"><span data-stu-id="743b4-108">The patching window is the period when the environment is patched.</span></span> <span data-ttu-id="743b4-109">それは地理的な地域によって定義されます。</span><span class="sxs-lookup"><span data-stu-id="743b4-109">It's defined by geographic region.</span></span> <span data-ttu-id="743b4-110">保守活動に関する詳細は、関係者に送信される通知に含まれます。</span><span class="sxs-lookup"><span data-stu-id="743b4-110">Details about the maintenance activity will be included in the notification that is sent to stakeholders.</span></span>

### <a name="when-is-this-planned-maintenance-window-taken"></a><span data-ttu-id="743b4-111">この計画済みメンテナンス ウィンドウはいつ使用されますか ?</span><span class="sxs-lookup"><span data-stu-id="743b4-111">When is this planned maintenance window taken?</span></span>
<span data-ttu-id="743b4-112">ユーザーへの影響を制限するため、環境が配置されている地域に応じてメンテナンス ウィンドウが予定されています。</span><span class="sxs-lookup"><span data-stu-id="743b4-112">To limit the impact on users, the maintenance window is planned according to the region where environments are deployed.</span></span> <span data-ttu-id="743b4-113">次のリストは、各地域のメンテナンス ウィンドウを示しています。</span><span class="sxs-lookup"><span data-stu-id="743b4-113">The following list shows the maintenance window for each region.</span></span> <span data-ttu-id="743b4-114">すべての環境は、これら 3 つの地域のいずれかに分類されます。</span><span class="sxs-lookup"><span data-stu-id="743b4-114">All environments fall into one of these three regions.</span></span> <span data-ttu-id="743b4-115">時間は協定世界時 (UTC、グリニッジ標準時) で表示されます。</span><span class="sxs-lookup"><span data-stu-id="743b4-115">The times are shown in Coordinated Universal Time (UTC, which is also known as Greenwich Mean Time).</span></span>

- <span data-ttu-id="743b4-116">**NAM:** 午前 2 時から午前 10 時</span><span class="sxs-lookup"><span data-stu-id="743b4-116">**NAM:** 2 AM to 10 AM</span></span>
- <span data-ttu-id="743b4-117">**EMEA:** 午後 10 時から午前 6 時</span><span class="sxs-lookup"><span data-stu-id="743b4-117">**EMEA:** 10 PM to 6 AM</span></span>
- <span data-ttu-id="743b4-118">**APAC:** 午後 12 時から午後 9 時</span><span class="sxs-lookup"><span data-stu-id="743b4-118">**APAC:** 12 PM to 9 PM</span></span>

### <a name="will-the-maintenance-from-microsoft-require-any-uptake"></a><span data-ttu-id="743b4-119">Microsoft からの保守では何かを取得することが必要ですか。</span><span class="sxs-lookup"><span data-stu-id="743b4-119">Will the maintenance from Microsoft require any uptake?</span></span>
<span data-ttu-id="743b4-120">ほとんどの保守作業でユーザー側のアクションは不要です。</span><span class="sxs-lookup"><span data-stu-id="743b4-120">Most of the maintenance operations require no action on your end.</span></span> <span data-ttu-id="743b4-121">取得が必要な重要なセキュリティ更新プログラムがある場合は、通知されます。</span><span class="sxs-lookup"><span data-stu-id="743b4-121">If there is a critical security update that requires uptake, you will be notified.</span></span>

### <a name="who-will-be-notified-about-the-upcoming-planned-maintenance"></a><span data-ttu-id="743b4-122">将来の計画的なメンテナンスはだれに通知されますか。</span><span class="sxs-lookup"><span data-stu-id="743b4-122">Who will be notified about the upcoming planned maintenance?</span></span>
<span data-ttu-id="743b4-123">次の利害関係者には、今後のメンテナンスについて通知されます。</span><span class="sxs-lookup"><span data-stu-id="743b4-123">The following stakeholders will be notified about the upcoming maintenance:</span></span>

- <span data-ttu-id="743b4-124">プロジェクト所有者</span><span class="sxs-lookup"><span data-stu-id="743b4-124">Project owners</span></span>
- <span data-ttu-id="743b4-125">組織の管理者</span><span class="sxs-lookup"><span data-stu-id="743b4-125">Organization admins</span></span>
- <span data-ttu-id="743b4-126">環境管理者</span><span class="sxs-lookup"><span data-stu-id="743b4-126">Environment admins</span></span>
- <span data-ttu-id="743b4-127">デプロイ中または Microsoft Dynamics Lifecycle Services (LCS) で環境の詳細ページにある **通知する** ボタンによりリストに指定されたその他のユーザー。</span><span class="sxs-lookup"><span data-stu-id="743b4-127">Other people who are specified in the list during deployment or through the **Notify** button on the environment details page in Microsoft Dynamics Lifecycle Services (LCS)</span></span>

### <a name="how-do-i-sign-up-to-be-notified-about-the-maintenance-window"></a><span data-ttu-id="743b4-128">メンテナンス ウィンドウに関して通知を受け取るよう登録するにはどうすればよいですか。</span><span class="sxs-lookup"><span data-stu-id="743b4-128">How do I sign up to be notified about the maintenance window?</span></span>
<span data-ttu-id="743b4-129">任意のパートナー、独立系ソフトウェア仕入先 (ISV)、および次回の更新プログラムについて通知を受けたいその他の関係者は、関連する利害関係者 (プロジェクト所有者、環境管理者、または追加の関係者) として LCS プロジェクトに追加するよう依頼できます。</span><span class="sxs-lookup"><span data-stu-id="743b4-129">Any partner, independent software vendor (ISV), and other interested party who wants to be notified about upcoming updates can request to be added to the LCS project as a relevant stakeholder (project owner, environment admin, or additional stakeholder).</span></span>

### <a name="why-cant-these-updates-be-applied-in-zero-downtime"></a><span data-ttu-id="743b4-130">これらの更新プログラムがゼロ ダウンタイムで適用できないのはなぜですか。</span><span class="sxs-lookup"><span data-stu-id="743b4-130">Why can't these updates be applied in zero downtime?</span></span>
<span data-ttu-id="743b4-131">Microsoft はサービスのダウンタイムの必要性を減らすよう継続的に努力しており、多くの定期的な保守作業ではダウンタイムを発生しません。</span><span class="sxs-lookup"><span data-stu-id="743b4-131">Microsoft is continually working to reduce the necessity of downtime for the service, and many regular maintenance tasks don't incur downtime.</span></span> <span data-ttu-id="743b4-132">しかし、予測可能性を保証するため、Microsoft はゼロ ダウンタイムですべてのパッチを実行することはまだできません。</span><span class="sxs-lookup"><span data-stu-id="743b4-132">However, to help guarantee the most predictability, Microsoft can't yet do all patching in zero downtime.</span></span>

## <a name="microsoft-service-updates"></a><span data-ttu-id="743b4-133">Microsoft のサービス更新プログラム</span><span class="sxs-lookup"><span data-stu-id="743b4-133">Microsoft service updates</span></span> 
<span data-ttu-id="743b4-134">別のよく寄せられる質問 (FAQ) に Microsoft によって行われるサービス更新プログラムに関する詳細が記載されています。</span><span class="sxs-lookup"><span data-stu-id="743b4-134">A separate set of frequently asked questions (FAQ) provides details about service updates that are done by Microsoft.</span></span> <span data-ttu-id="743b4-135">[1 つのバージョンのサービス更新プログラムに関してよく寄せられる質問](../../fin-and-ops/get-started/one-version.md) を参照してください。</span><span class="sxs-lookup"><span data-stu-id="743b4-135">See [One Version service updates FAQ](../../fin-and-ops/get-started/one-version.md).</span></span>

## <a name="infrastructure-updates"></a><span data-ttu-id="743b4-136">機器設備の更新</span><span class="sxs-lookup"><span data-stu-id="743b4-136">Infrastructure updates</span></span> 

### <a name="how-long-is-the-maintenance-window"></a><span data-ttu-id="743b4-137">メンテナンス ウィンドウの長さはどの程度ですか。</span><span class="sxs-lookup"><span data-stu-id="743b4-137">How long is the maintenance window?</span></span>
<span data-ttu-id="743b4-138">ほとんどのオペレーティング システム レベルの更新は約 1 時間で完了します。</span><span class="sxs-lookup"><span data-stu-id="743b4-138">Most operating system–level updates are completed in approximately one hour.</span></span> <span data-ttu-id="743b4-139">ただし、障害を処理してシステムを正常な状態に戻す時間があるため、Microsoft は 3 時間の時間枠を要求しています。</span><span class="sxs-lookup"><span data-stu-id="743b4-139">However, Microsoft asks for a three-hour window, so that there is time to handle any failures and to bring the system back to a healthy state.</span></span> 

<span data-ttu-id="743b4-140">すべてのアップデートの正確なダウンタイムは、アップデート開始前に通知されるメンテナンス ウィンドウ通知電子メールに含まれます。</span><span class="sxs-lookup"><span data-stu-id="743b4-140">The exact downtime for all updates will be included in the maintenance window notification email that is sent to you before the start of the update.</span></span>

### <a name="where-can-i-learn-more-about-what-is-applied"></a><span data-ttu-id="743b4-141">何が適用されたかについての詳細はどこですか。</span><span class="sxs-lookup"><span data-stu-id="743b4-141">Where can I learn more about what is applied?</span></span>
<span data-ttu-id="743b4-142">適用される更新プログラムの詳細については、[Microsoft セキュリティ速報](https://technet.microsoft.com/security/bulletins.aspx) を参照してください。</span><span class="sxs-lookup"><span data-stu-id="743b4-142">For more information about the updates that will be applied, see [Microsoft Security Bulletins](https://technet.microsoft.com/security/bulletins.aspx).</span></span>

### <a name="where-can-i-track-progress-of-the-update"></a><span data-ttu-id="743b4-143">更新プログラムの進捗はどのように追跡できますか。</span><span class="sxs-lookup"><span data-stu-id="743b4-143">Where can I track progress of the update?</span></span>
<span data-ttu-id="743b4-144">オペレーティング システム レベルの更新中に、LCS は現在どのパッチ適用が進行中であるかを示しません。</span><span class="sxs-lookup"><span data-stu-id="743b4-144">During operating system–level updates, LCS doesn't currently indicate that any patching is in progress.</span></span> <span data-ttu-id="743b4-145">ただし、Microsoft はこの機能をある時点で追加する予定です。</span><span class="sxs-lookup"><span data-stu-id="743b4-145">However, Microsoft plans to add this functionality at some point.</span></span>

### <a name="what-environments-are-updated"></a><span data-ttu-id="743b4-146">なんの環境が更新されるか。</span><span class="sxs-lookup"><span data-stu-id="743b4-146">What environments are updated?</span></span>
<span data-ttu-id="743b4-147">オペレーティング システム レベルの更新は、Microsoft の基本サービスの一部として含まれているすべての第 2 層のサンドボックス環境に適用されます。</span><span class="sxs-lookup"><span data-stu-id="743b4-147">Operating system–level updates are applied to all Tier-2 sandbox environments that are included as part of the Microsoft base offer.</span></span> <span data-ttu-id="743b4-148">購入済のアドオンにも適用されます。</span><span class="sxs-lookup"><span data-stu-id="743b4-148">They are also applied to add-ons that have been purchased.</span></span> <span data-ttu-id="743b4-149">ただし、第 1 層サンドボックスおよびデモ環境など、他のすべての環境は顧客やパートナーの担当であることに注意してください。</span><span class="sxs-lookup"><span data-stu-id="743b4-149">However, other environments, such as Tier-1 sandbox and demo environments, are the responsibility of the customer or partner.</span></span>

### <a name="what-notifications-will-i-receive-about-upcoming-planned-maintenance"></a><span data-ttu-id="743b4-150">次回の計画済みメンテナンスに関してどのような通知を受け取りますか ?</span><span class="sxs-lookup"><span data-stu-id="743b4-150">What notifications will I receive about upcoming planned maintenance?</span></span>
<span data-ttu-id="743b4-151">更新が予定されている 5 日前に、電子メール通知を受け取ります。</span><span class="sxs-lookup"><span data-stu-id="743b4-151">You will receive a notification email five days before the update is scheduled to occur.</span></span> <span data-ttu-id="743b4-152">この電子メールには、更新される環境、更新の種類、更新が実行する見積もり時間、および実行する必要のある操作に関する情報が含まれます。</span><span class="sxs-lookup"><span data-stu-id="743b4-152">This email will include information about the environments that will be updated, the update type, the estimated amount of time that the update will take, and any action that you might have to take.</span></span>

### <a name="will-i-be-notified-when-the-update-is-completed"></a><span data-ttu-id="743b4-153">更新プログラムの完了時に通知されますか。</span><span class="sxs-lookup"><span data-stu-id="743b4-153">Will I be notified when the update is completed?</span></span>
<span data-ttu-id="743b4-154">定義された保守時間枠で更新が完了する場合、更新が完了したときに通知を受信しません。</span><span class="sxs-lookup"><span data-stu-id="743b4-154">If your update is completed within the defined maintenance window, you won't receive any notification when the update is completed.</span></span> 

### <a name="how-do-i-report-an-issue-that-is-identified-during-validation-of-the-updates-that-were-applied-to-the-environment"></a><span data-ttu-id="743b4-155">環境に適用された更新の検証時に識別される問題をレポートするにはどうすればよいですか。</span><span class="sxs-lookup"><span data-stu-id="743b4-155">How do I report an issue that is identified during validation of the updates that were applied to the environment?</span></span>
<span data-ttu-id="743b4-156">更新の検証中に特定された問題を報告するには、Microsoft にサポート チケットを提出し、タイトルに '予定された保守時間枠' を追加します。</span><span class="sxs-lookup"><span data-stu-id="743b4-156">To report an issue that is identified during update validation, file a support ticket with Microsoft and append the title with 'Planned Maintenance Window'.</span></span>

### <a name="what-happens-if-the-patching-fails"></a><span data-ttu-id="743b4-157">ファイルの修正に失敗した場合はどうなるでしょうか ?</span><span class="sxs-lookup"><span data-stu-id="743b4-157">What happens if the patching fails?</span></span>
<span data-ttu-id="743b4-158">修正が、オペレーティング システム レベル更新中に失敗すると、特定の修正プログラムはスキップされ、次の更新サイクルで適用されます。</span><span class="sxs-lookup"><span data-stu-id="743b4-158">If the patching fails during an operating system–level update, the specific patch is skipped and will be applied in the next update cycle.</span></span>

### <a name="will-i-be-compensated-if-the-update-takes-longer-than-the-scheduled-maintenance-window"></a><span data-ttu-id="743b4-159">更新プログラムが予定メンテナンス ウインドウより時間がかかる場合は補償されますか。</span><span class="sxs-lookup"><span data-stu-id="743b4-159">Will I be compensated if the update takes longer than the scheduled maintenance window?</span></span>
<span data-ttu-id="743b4-160">更新が予定された保守ウィンドウよりも長い場合は、余分な時間は予定外のダウンタイムと見なされ、一般的なサービス レベル アグリーメント (SLA) の対象となります。</span><span class="sxs-lookup"><span data-stu-id="743b4-160">If the update takes longer than the scheduled maintenance window, the extra time is considered unplanned downtime and is subject to the general service level agreement (SLA).</span></span>

### <a name="can-i-reschedule-the-planned-maintenance"></a><span data-ttu-id="743b4-161">計画的なメンテナンスを再スケジューリングできますか。</span><span class="sxs-lookup"><span data-stu-id="743b4-161">Can I reschedule the planned maintenance?</span></span>
<span data-ttu-id="743b4-162">Microsoft は計画的なメンテナンスを再スケジュールするためのオプションを提供していません。</span><span class="sxs-lookup"><span data-stu-id="743b4-162">Microsoft doesn't offer an option to reschedule a planned maintenance.</span></span> <span data-ttu-id="743b4-163">ただし、現在の月の保守サイクルから除外するように選択できます。</span><span class="sxs-lookup"><span data-stu-id="743b4-163">However, you can select to be excluded from the maintenance cycle for the current month.</span></span> 

### <a name="how-do-i-opt-out-of-the-current-maintenance-cycle"></a><span data-ttu-id="743b4-164">現在のメンテナンス サイクルを停止するにはどうすればよいですか。</span><span class="sxs-lookup"><span data-stu-id="743b4-164">How do I opt out of the current maintenance cycle?</span></span>
<span data-ttu-id="743b4-165">現在のメンテナンス サイクルを無効にするには、Microsoft にサポート チケットを提出してください。</span><span class="sxs-lookup"><span data-stu-id="743b4-165">To opt out of the current maintenance cycle, file a support ticket with Microsoft.</span></span> <span data-ttu-id="743b4-166">無効化の要求をするサポートチケットの提出期限は、通知メールに記載されています。</span><span class="sxs-lookup"><span data-stu-id="743b4-166">The deadline for filing the support ticket to request an opt-out will be included in your notification email.</span></span> <span data-ttu-id="743b4-167">無効化の要求は、締め切りを過ぎて送信された場合には受け付けられません。</span><span class="sxs-lookup"><span data-stu-id="743b4-167">Any opt-out submitted after that deadline will not be honored.</span></span> <span data-ttu-id="743b4-168">ご利用の環境は当月のメンテナンスサイクルの対象から除外されますが、翌月には再度更新されます。</span><span class="sxs-lookup"><span data-stu-id="743b4-168">Your environment will be excluded from the maintenance cycle for the current month, however your environment will be updated in the next month.</span></span>
