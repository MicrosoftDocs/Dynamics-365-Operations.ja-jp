---
title: Dynamics 365 Human Resources の新機能または変更された機能 (2020 年 9 月 16 日)
description: このトピックでは、2020 年 9 月 16 日に更新された、Microsoft Dynamics 365 Human Resources の新機能または変更された機能について説明します。
author: jcart1106
manager: tfehr
ms.date: 09/16/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-talent
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Human Resources
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: jcart
ms.search.validFrom: 2020-09-16
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: 74a87ddb4ed14042dd4e716ad64bc844a800a0a0
ms.sourcegitcommit: ea2d652867b9b83ce6e5e8d6a97d2f9460a84c52
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 02/03/2021
ms.locfileid: "5113321"
---
# <a name="whats-new-or-changed-in-dynamics-365-human-resources-september-16-2020"></a><span data-ttu-id="529a7-103">Dynamics 365 Human Resources の新機能または変更された機能 (2020 年 9 月 16 日)</span><span class="sxs-lookup"><span data-stu-id="529a7-103">What's new or changed in Dynamics 365 Human Resources (September 16, 2020)</span></span>

[!include [rename-banner](~/includes/cc-data-platform-banner.md)]

<span data-ttu-id="529a7-104">このトピックでは、Dynamics 365 Human Resources の新機能または変更された機能について説明します。</span><span class="sxs-lookup"><span data-stu-id="529a7-104">This topic describes features that are either new or changed in Dynamics 365 Human Resources.</span></span> <span data-ttu-id="529a7-105">変更は、ビルド番号 8.1.3557 に適用されます。</span><span class="sxs-lookup"><span data-stu-id="529a7-105">Changes apply to build number 8.1.3557.</span></span> <span data-ttu-id="529a7-106">一部の機能の横にあるかっこ内の数字は、参照用に Lifecycle Services (LCS) サポート番号を示しています。</span><span class="sxs-lookup"><span data-stu-id="529a7-106">The numbers in parentheses next to some features refer to Lifecycle Services (LCS) support numbers for reference.</span></span>

## <a name="included-in-this-release"></a><span data-ttu-id="529a7-107">このリリースに含まれる</span><span class="sxs-lookup"><span data-stu-id="529a7-107">Included in this release</span></span>

-  [<span data-ttu-id="529a7-108">保存されているビュー - 一般提供</span><span class="sxs-lookup"><span data-stu-id="529a7-108">Saved views - general availability</span></span>](https://docs.microsoft.com/dynamics365-release-plan/2020wave2/finance-operations/finance-operations-crossapp-capabilities/saved-views--general-availability)<br><span data-ttu-id="529a7-109">- 詳細については、[保存されているビュー](https://docs.microsoft.com/dynamics365/fin-ops-core/fin-ops/get-started/saved-views) を参照してください。</span><span class="sxs-lookup"><span data-stu-id="529a7-109">- For more information, see [Saved views](https://docs.microsoft.com/dynamics365/fin-ops-core/fin-ops/get-started/saved-views).</span></span> 

- <span data-ttu-id="529a7-110">**職位アクション** フォームには、更新された分析コード グリッドと新しいダイアログがあります (469495)。</span><span class="sxs-lookup"><span data-stu-id="529a7-110">The **Position actions** form has an updated dimensions grid and new dialogue (469495).</span></span>

- <span data-ttu-id="529a7-111">**Human Resources 共有パラメーター** の **詳細なアクセス** で **作業者情報へのアクセス制限** を "はい" に設定すると、福利厚生フォームには適切な作業者のみが表示されるようになりました (393384)。</span><span class="sxs-lookup"><span data-stu-id="529a7-111">If you set **Restrict access to worker information** to yes in **Advanced access** in **Human Resources Shared parameters**, benefits forms now show only the appropriate workers (393384).</span></span>

- <span data-ttu-id="529a7-112">**WorkCalendar** エンティティの新しいカレンダー生成オプション (477055):</span><span class="sxs-lookup"><span data-stu-id="529a7-112">New calendar generation options in the **WorkCalendar** entity (477055):</span></span><br><span data-ttu-id="529a7-113">- 既定の終了時刻</span><span class="sxs-lookup"><span data-stu-id="529a7-113">- Default ending time</span></span><br><span data-ttu-id="529a7-114">- 既定の開始時刻</span><span class="sxs-lookup"><span data-stu-id="529a7-114">-    Default starting time</span></span><br><span data-ttu-id="529a7-115">- 金曜日は就業日ですか</span><span class="sxs-lookup"><span data-stu-id="529a7-115">-  Is Friday working day</span></span><br><span data-ttu-id="529a7-116">- 月曜日は就業日ですか</span><span class="sxs-lookup"><span data-stu-id="529a7-116">-  Is Monday working day</span></span><br><span data-ttu-id="529a7-117">- 土曜日は就業日ですか</span><span class="sxs-lookup"><span data-stu-id="529a7-117">-  Is Saturday working day</span></span><br><span data-ttu-id="529a7-118">- 日曜日は就業日ですか</span><span class="sxs-lookup"><span data-stu-id="529a7-118">- Is Sunday working day</span></span><br><span data-ttu-id="529a7-119">- 木曜日は就業日ですか</span><span class="sxs-lookup"><span data-stu-id="529a7-119">- Is Thursday working day</span></span><br><span data-ttu-id="529a7-120">- 火曜日は就業日ですか</span><span class="sxs-lookup"><span data-stu-id="529a7-120">- Is Tuesday working day</span></span><br><span data-ttu-id="529a7-121">- 水曜日は就業日ですか</span><span class="sxs-lookup"><span data-stu-id="529a7-121">- Is Wednesday working day</span></span><br><span data-ttu-id="529a7-122">- 作業カレンダーの休日 ID</span><span class="sxs-lookup"><span data-stu-id="529a7-122">- Work calendar holiday ID</span></span>

- <span data-ttu-id="529a7-123">**LeaveBankTransactionV1** エンティティには、理由コードが含まれるようになりました (477823)。</span><span class="sxs-lookup"><span data-stu-id="529a7-123">The **LeaveBankTransactionV1** entity now includes the reason code (477823).</span></span>

- <span data-ttu-id="529a7-124">タスク記録を保存できるようになりました (492923)。</span><span class="sxs-lookup"><span data-stu-id="529a7-124">You can now save task recordings (492923).</span></span>

- <span data-ttu-id="529a7-125">データが **HCMWorkerContactEntity** から正常に公開されるようになりました (427620)。</span><span class="sxs-lookup"><span data-stu-id="529a7-125">Data is now published successfully from **HCMWorkerContactEntity** (427620).</span></span>

- <span data-ttu-id="529a7-126">契約社員作業者タイプの **報酬** クイック タブが、**作業者アクション** フォームに表示されるようになりました (482494)。</span><span class="sxs-lookup"><span data-stu-id="529a7-126">The **Compensation** fast tab now displays for the contractor worker type in the **Worker actions** form (482494).</span></span>

- <span data-ttu-id="529a7-127">**固定報酬** を設定した場合、**レベル** と **プラン** フィールドが必須になりました。</span><span class="sxs-lookup"><span data-stu-id="529a7-127">The **Level** and **Plan** fields are now mandatory if you set **Fixed compensation**.</span></span> <span data-ttu-id="529a7-128">これらのフィールドを空白のままにすると、エラー メッセージが表示されます (482497)。</span><span class="sxs-lookup"><span data-stu-id="529a7-128">An error message displays if you leave these fields blank (482497).</span></span>

- <span data-ttu-id="529a7-129">**福利厚生** の **プラン タイプ** フィールドがドロップ ダウンリストになりました (488768)。</span><span class="sxs-lookup"><span data-stu-id="529a7-129">The **Plan type** field in **Benefits** is now a dropdown list (488768).</span></span>

- <span data-ttu-id="529a7-130">システム管理者は、カスタム フィールドが Human Resources から削除された場合に、通知を受け取るようになりました (481408)。</span><span class="sxs-lookup"><span data-stu-id="529a7-130">System administrators now receive a notification if a custom field is deleted from Human Resources (481408).</span></span>

- <span data-ttu-id="529a7-131">従業員のプロセスを終了する間、ロックされているように見えた後、Human Resources は期待どおりに動作し、選択した会社を変更しません (479877)。</span><span class="sxs-lookup"><span data-stu-id="529a7-131">During the terminate employee process, Human Resources behaves as expected and doesn't change the selected company after appearing to lock (479877).</span></span> 

- <span data-ttu-id="529a7-132">マネージャーは、個人用設定を使用して数値列を追加できなくなりました (485317)。</span><span class="sxs-lookup"><span data-stu-id="529a7-132">Managers can no longer add a number column through personalization (485317).</span></span>

- <span data-ttu-id="529a7-133">マネージャーは、有効期限切れ ID 番号からデータ範囲フィルターを削除できなくなりました (485321)。</span><span class="sxs-lookup"><span data-stu-id="529a7-133">Managers can no longer remove the data range filter from identification numbers expiring (485321).</span></span>

- <span data-ttu-id="529a7-134">**報告先** フィールドが空の場合でも、職位にカーソルを合わせると職位の詳細が表示されます (433328)。</span><span class="sxs-lookup"><span data-stu-id="529a7-134">When the **Reports to** field is empty, position details still display when hovering over the position (433328).</span></span>

- <span data-ttu-id="529a7-135">従業員が、従業員セルフ サービスで福利厚生プラン情報を表示できるようになりました (481676)。</span><span class="sxs-lookup"><span data-stu-id="529a7-135">Employees can now view benefit plan information in Employee self service (481676).</span></span>

- <span data-ttu-id="529a7-136">従業員は、すべての登録済コースを表示できるようになりました (429048)。</span><span class="sxs-lookup"><span data-stu-id="529a7-136">Employees can now see all registered courses (429048).</span></span>

- <span data-ttu-id="529a7-137">**プロフェッショナル証明書** ページの表示オプションを制限できるようになりました。</span><span class="sxs-lookup"><span data-stu-id="529a7-137">You can now restrict viewing options for the **Professional certificates** page.</span></span> <span data-ttu-id="529a7-138">表示オプションを現在の法人、作業者ステータス別、および作業者タイプ別に制限できます (451501)。</span><span class="sxs-lookup"><span data-stu-id="529a7-138">You can restrict viewing options to the current legal entity, by worker status, and by worker type (451501).</span></span> 


## <a name="in-preview"></a><span data-ttu-id="529a7-139">プレビュー</span><span class="sxs-lookup"><span data-stu-id="529a7-139">In Preview</span></span>

### <a name="human-resources-app-in-teams"></a><span data-ttu-id="529a7-140">Teams の Human Resources アプリ</span><span class="sxs-lookup"><span data-stu-id="529a7-140">Human Resources app in Teams</span></span>

<span data-ttu-id="529a7-141">従業員は、Microsoft Teams 内で休暇の表示および申請ができます。</span><span class="sxs-lookup"><span data-stu-id="529a7-141">Employees can view and request time away from work within Microsoft Teams.</span></span> <span data-ttu-id="529a7-142">ボットと対話して、休暇申請を作成できます。</span><span class="sxs-lookup"><span data-stu-id="529a7-142">They can interact with a bot to create leave requests.</span></span> <span data-ttu-id="529a7-143">詳細については、以下を参照してください。</span><span class="sxs-lookup"><span data-stu-id="529a7-143">For more information, see:</span></span>

- <span data-ttu-id="529a7-144">Dynamics 365 2020 リリース ウェーブ 1 プランでの [Microsoft Teams の従業員の休暇および欠勤体験](https://docs.microsoft.com/dynamics365-release-plan/2020wave1/dynamics365-human-resources/employee-leave-absence-experience-teams)</span><span class="sxs-lookup"><span data-stu-id="529a7-144">[Employee leave and absence experience in Microsoft Teams](https://docs.microsoft.com/dynamics365-release-plan/2020wave1/dynamics365-human-resources/employee-leave-absence-experience-teams) in the Dynamics 365 2020 release wave 1 plan</span></span>
- <span data-ttu-id="529a7-145">Human Resources ドキュメントの [Teams の Human Resources アプリ](https://go.microsoft.com/fwlink/?linkid=2127841)</span><span class="sxs-lookup"><span data-stu-id="529a7-145">[Human Resources app in Teams](https://go.microsoft.com/fwlink/?linkid=2127841) in Human Resources documentation</span></span>

### <a name="human-resources-app-in-teams-preview-features"></a><span data-ttu-id="529a7-146">Teams の Human Resources アプリにおけるプレビュー機能</span><span class="sxs-lookup"><span data-stu-id="529a7-146">Human Resources app in Teams preview features</span></span>
 
-  <span data-ttu-id="529a7-147">**通知** : 休暇申請の提出者と承認者は、Teams の人事アプリで通知されます。</span><span class="sxs-lookup"><span data-stu-id="529a7-147">**Notifications**: Submitters and approvers of time-off requests will be notified in the Human Resources app in Teams.</span></span> <span data-ttu-id="529a7-148">承認者は、休暇申請を承認または拒否できます。</span><span class="sxs-lookup"><span data-stu-id="529a7-148">Approvers can approve or deny time-off requests.</span></span> <span data-ttu-id="529a7-149">申請が承認または拒否された場合は、送信者に通知されます。</span><span class="sxs-lookup"><span data-stu-id="529a7-149">Submitters will be notified if the request was approved or denied.</span></span> <span data-ttu-id="529a7-150">詳細については、以下を参照してください。</span><span class="sxs-lookup"><span data-stu-id="529a7-150">For more information, see:</span></span>
   - <span data-ttu-id="529a7-151">Dynamics 365 2020 リリース ウェーブ 2 プランでの [Microsoft Teams の従業員の休暇および欠勤体験](https://docs.microsoft.com/dynamics365-release-plan/2020wave2/human-resources/dynamics365-human-resources/employee-leave-absence-experience-teams)</span><span class="sxs-lookup"><span data-stu-id="529a7-151">[Employee leave and absence experience in Microsoft Teams](https://docs.microsoft.com/dynamics365-release-plan/2020wave2/human-resources/dynamics365-human-resources/employee-leave-absence-experience-teams) in the Dynamics 365 2020 release wave 2 plan</span></span>
   - <span data-ttu-id="529a7-152">Human Resources ドキュメントの [Teams の Human Resources アプリの通知を有効にする](https://docs.microsoft.com/dynamics365/human-resources/hr-admin-teams-leave-app#enable-notifications-for-the-human-resources-app-in-teams)</span><span class="sxs-lookup"><span data-stu-id="529a7-152">[Enable notifications for the Human Resources app in Teams](https://docs.microsoft.com/dynamics365/human-resources/hr-admin-teams-leave-app#enable-notifications-for-the-human-resources-app-in-teams) in Human Resources documentation</span></span>
   - <span data-ttu-id="529a7-153">Human Resources ドキュメントの [個々のユーザーの Teams の通知をオンまたはオフにする](https://docs.microsoft.com/dynamics365/human-resources/hr-admin-teams-leave-app#turn-teams-notifications-on-or-off-for-individual-users)</span><span class="sxs-lookup"><span data-stu-id="529a7-153">[Turn Teams notifications on or off for individual users](https://docs.microsoft.com/dynamics365/human-resources/hr-admin-teams-leave-app#turn-teams-notifications-on-or-off-for-individual-users) in Human Resources documentation</span></span>
   - <span data-ttu-id="529a7-154">Human Resources ドキュメントの [Teams の通知](https://docs.microsoft.com/dynamics365/human-resources/hr-teams-leave-app#teams-notifications)</span><span class="sxs-lookup"><span data-stu-id="529a7-154">[Teams notifications](https://docs.microsoft.com/dynamics365/human-resources/hr-teams-leave-app#teams-notifications) in Human Resources documentation</span></span>
   - <span data-ttu-id="529a7-155">Human Resources ドキュメントの [チームの休暇カレンダーの表示](https://docs.microsoft.com/dynamics365/human-resources/hr-teams-leave-app#view-your-teams-leave-calendar)</span><span class="sxs-lookup"><span data-stu-id="529a7-155">[View your team's leave calendar](https://docs.microsoft.com/dynamics365/human-resources/hr-teams-leave-app#view-your-teams-leave-calendar) in Human Resources documentation</span></span>
 
- <span data-ttu-id="529a7-156">**マネージャーの休暇カレンダー**: マネージャーは、直属の部下の承認済みおよび保留中の休暇をカレンダー表示で確認できます。</span><span class="sxs-lookup"><span data-stu-id="529a7-156">**Manager time-off calendar**: Managers can see approved and pending time off for their direct reports in a calendar view.</span></span> <span data-ttu-id="529a7-157">このビューを使用すると、チームのメンバーの休暇を簡単に把握することができます。</span><span class="sxs-lookup"><span data-stu-id="529a7-157">This view provides an easy understanding of when their team members are away from work.</span></span> <span data-ttu-id="529a7-158">詳細については、以下を参照してください。</span><span class="sxs-lookup"><span data-stu-id="529a7-158">For more information, see:</span></span>
   - <span data-ttu-id="529a7-159">Dynamics 365 2020 リリース ウェーブ 2 プランでの [Microsoft Teams の従業員の休暇および欠勤体験](https://docs.microsoft.com/dynamics365-release-plan/2020wave2/human-resources/dynamics365-human-resources/employee-leave-absence-experience-teams)</span><span class="sxs-lookup"><span data-stu-id="529a7-159">[Employee leave and absence experience in Microsoft Teams](https://docs.microsoft.com/dynamics365-release-plan/2020wave2/human-resources/dynamics365-human-resources/employee-leave-absence-experience-teams) in the Dynamics 365 2020 release wave 2 plan</span></span>
   - <span data-ttu-id="529a7-160">Human Resources ドキュメントの [チームの休暇カレンダーの表示](https://docs.microsoft.com/dynamics365/human-resources/hr-teams-leave-app#view-your-teams-leave-calendar)</span><span class="sxs-lookup"><span data-stu-id="529a7-160">[View your team's leave calendar](https://docs.microsoft.com/dynamics365/human-resources/hr-teams-leave-app#view-your-teams-leave-calendar) in Human Resources documentation</span></span>

### <a name="configuration-option-to-position-work-items-assigned-to-me-list-477004"></a><span data-ttu-id="529a7-161">自分のリストに割り当てられた作業項目を配置するコンフィギュレーション オプション (477004)</span><span class="sxs-lookup"><span data-stu-id="529a7-161">Configuration option to position Work items assigned to me list (477004)</span></span>

<span data-ttu-id="529a7-162">ダッシュボードの右側の列に、**自分に割り当てられた作業項目** リストを配置するための新しいオプションが使用可能になりました。</span><span class="sxs-lookup"><span data-stu-id="529a7-162">A new option is now available to position the **Work items assigned to me** list in the right-hand column of the dashboard.</span></span> <span data-ttu-id="529a7-163">この変更により、すべての作業項目とタスク一覧が同じ領域に表示されます。</span><span class="sxs-lookup"><span data-stu-id="529a7-163">With this change, all work items and to do lists display in the same area.</span></span> <span data-ttu-id="529a7-164">この機能を有効にするには、機能管理で **プレビュー - ワークフロー エクスペリエンスの拡張機能** をオンにします。</span><span class="sxs-lookup"><span data-stu-id="529a7-164">Enable this functionality by turning on **Preview - Workflow experience enhancements** in Feature management.</span></span> <span data-ttu-id="529a7-165">プレビュー機能をオンにする方法の詳細については、[機能の管理](hr-admin-manage-features.md) を参照してください。</span><span class="sxs-lookup"><span data-stu-id="529a7-165">For more information about turning on preview features, see [Manage features](hr-admin-manage-features.md).</span></span>

<span data-ttu-id="529a7-166">この機能は、人事アクション フォームに表示されるワークフロー オプションも促進します。</span><span class="sxs-lookup"><span data-stu-id="529a7-166">This feature also promotes the workflow options that appear in the personnel actions forms.</span></span> <span data-ttu-id="529a7-167">すばやくアクセスできるように、アクション クイック タブ上にも、ワークフロー オプションは表示されます。</span><span class="sxs-lookup"><span data-stu-id="529a7-167">Workflow options also appear above the action fast tab for quick access.</span></span> <span data-ttu-id="529a7-168">詳細については、以下を参照してください。</span><span class="sxs-lookup"><span data-stu-id="529a7-168">For more information, see:</span></span> 

- <span data-ttu-id="529a7-169">Dynamics 365 2020 のリリース ウェーブ 2 プランの [組織および人事管理ワークフロー エクスペリエンスの機能強化](https://docs.microsoft.com/dynamics365-release-plan/2020wave2/human-resources/dynamics365-human-resources/organization-personnel-management-workflow-experience-enhancements)</span><span class="sxs-lookup"><span data-stu-id="529a7-169">[Organization and personnel management workflow experience enhancements](https://docs.microsoft.com/dynamics365-release-plan/2020wave2/human-resources/dynamics365-human-resources/organization-personnel-management-workflow-experience-enhancements) in the Dynamics 365 2020 release wave 2 plan</span></span>

![自分自身に割り当てられた作業項目](./media/hr-workflow-work-items-assigned-to-me.png)

![ワークフロー項目のクイックアクセス](./media/hr-workflow-quick-access.png)

### <a name="leave-and-absence-calendar"></a><span data-ttu-id="529a7-172">休暇および欠勤カレンダー</span><span class="sxs-lookup"><span data-stu-id="529a7-172">Leave and absence calendar</span></span>

<span data-ttu-id="529a7-173">このリリースには、休暇および欠勤カレンダーの追加カレンダー オプションが含まれています。</span><span class="sxs-lookup"><span data-stu-id="529a7-173">This release includes additional calendar options for leave and absence calendars.</span></span> <span data-ttu-id="529a7-174">詳細については、[チームおよび会社カレンダーの表示](https://docs.microsoft.com/dynamics365/human-resources/hr-employee-self-service-calendar) を参照してください。</span><span class="sxs-lookup"><span data-stu-id="529a7-174">For more information, see [View team and company calendars](https://docs.microsoft.com/dynamics365/human-resources/hr-employee-self-service-calendar).</span></span>

## <a name="coming-soon"></a><span data-ttu-id="529a7-175">間もなく公開</span><span class="sxs-lookup"><span data-stu-id="529a7-175">Coming Soon</span></span>

### <a name="checklist-entities-included-in-dataverse"></a><span data-ttu-id="529a7-176">Dataverse に含まれるチェックリスト エンティティ</span><span class="sxs-lookup"><span data-stu-id="529a7-176">Checklist entities included in Dataverse</span></span>

<span data-ttu-id="529a7-177">オンボード、オフボード、転送、および業務プロセスのチェックリスト エンティティは、Dataverse ですぐに使用可能になります。</span><span class="sxs-lookup"><span data-stu-id="529a7-177">Checklist entities for Onboarding, Offboarding, Transfers, and Business processes will be available soon in Dataverse.</span></span>

### <a name="benefits-management-reason-codes"></a><span data-ttu-id="529a7-178">福利厚生管理の理由コード</span><span class="sxs-lookup"><span data-stu-id="529a7-178">Benefits management reason codes</span></span>

<span data-ttu-id="529a7-179">福利厚生管理の理由コードは、Human Resources の既存の理由コードと間もなく結合されます。</span><span class="sxs-lookup"><span data-stu-id="529a7-179">Benefits management reason codes will soon be combined with existing reason codes in Human Resources.</span></span> <span data-ttu-id="529a7-180">福利厚生管理で 15 文字を超える理由コードを作成した場合は、福利厚生管理の **理由コード** フォームで理由コードの名前を 15 文字以下に変更する必要があります。</span><span class="sxs-lookup"><span data-stu-id="529a7-180">If you created reason codes in Benefits management that are over 15 characters, you must change the name of the reason code in the Benefits management **Reason codes** form to be 15 characters or less.</span></span> <span data-ttu-id="529a7-181">名前を更新すると、理由コードが人事管理の既存の理由コード フォームの下に表示されます。</span><span class="sxs-lookup"><span data-stu-id="529a7-181">After you update the name, the reason code will appear under the existing reason code form in Personnel management.</span></span> <span data-ttu-id="529a7-182">この変更は将来使用可能になり、既存の機能には影響しません。</span><span class="sxs-lookup"><span data-stu-id="529a7-182">This change will be available in the future and won't affect existing functionality.</span></span>

## <a name="see-also"></a><span data-ttu-id="529a7-183">参照</span><span class="sxs-lookup"><span data-stu-id="529a7-183">See also</span></span>

[<span data-ttu-id="529a7-184">Human Resources の新機能および変更された機能</span><span class="sxs-lookup"><span data-stu-id="529a7-184">What's new or changed in Human Resources</span></span>](hr-admin-whats-new.md)</br>
[<span data-ttu-id="529a7-185">Dynamics 365 Human Resources 2019 のリリース ウェーブ 2 の概要</span><span class="sxs-lookup"><span data-stu-id="529a7-185">Overview of Dynamics 365 Human Resources 2019 release wave 2</span></span>](https://docs.microsoft.com/dynamics365-release-plan/2019wave2/dynamics365-human-resources/)</br>
[<span data-ttu-id="529a7-186">更新プロセス</span><span class="sxs-lookup"><span data-stu-id="529a7-186">Update process</span></span>](hr-admin-setup-update-process.md)</br>
[<span data-ttu-id="529a7-187">機能の管理</span><span class="sxs-lookup"><span data-stu-id="529a7-187">Manage features</span></span>](hr-admin-manage-features.md)
