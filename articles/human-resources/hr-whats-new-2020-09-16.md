---
title: Dynamics 365 Human Resources の新機能または変更された機能 (2020 年 9 月 16 日)
description: このトピックでは、2020 年 9 月 16 日に更新された、Microsoft Dynamics 365 Human Resources の新機能または変更された機能について説明します。
author: jcart1106
ms.date: 09/16/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.search.scope: Human Resources
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: jcart
ms.search.validFrom: 2020-09-16
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: 0fe3ac2393e66a00e070d8cb6862c29625d39b53
ms.sourcegitcommit: 879ee8a10e6158885795dce4b3db5077540eec41
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 05/18/2021
ms.locfileid: "6057167"
---
# <a name="whats-new-or-changed-in-dynamics-365-human-resources-september-16-2020"></a><span data-ttu-id="2eece-103">Dynamics 365 Human Resources の新機能または変更された機能 (2020 年 9 月 16 日)</span><span class="sxs-lookup"><span data-stu-id="2eece-103">What's new or changed in Dynamics 365 Human Resources (September 16, 2020)</span></span>

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

[!include [rename-banner](~/includes/cc-data-platform-banner.md)]

<span data-ttu-id="2eece-104">このトピックでは、Dynamics 365 Human Resources の新機能または変更された機能について説明します。</span><span class="sxs-lookup"><span data-stu-id="2eece-104">This topic describes features that are either new or changed in Dynamics 365 Human Resources.</span></span> <span data-ttu-id="2eece-105">変更は、ビルド番号 8.1.3557 に適用されます。</span><span class="sxs-lookup"><span data-stu-id="2eece-105">Changes apply to build number 8.1.3557.</span></span> <span data-ttu-id="2eece-106">一部の機能の横にあるかっこ内の数字は、参照用に Lifecycle Services (LCS) サポート番号を示しています。</span><span class="sxs-lookup"><span data-stu-id="2eece-106">The numbers in parentheses next to some features refer to Lifecycle Services (LCS) support numbers for reference.</span></span>

## <a name="included-in-this-release"></a><span data-ttu-id="2eece-107">このリリースに含まれる</span><span class="sxs-lookup"><span data-stu-id="2eece-107">Included in this release</span></span>

-  [<span data-ttu-id="2eece-108">保存されているビュー - 一般提供</span><span class="sxs-lookup"><span data-stu-id="2eece-108">Saved views - general availability</span></span>](/dynamics365-release-plan/2020wave2/finance-operations/finance-operations-crossapp-capabilities/saved-views--general-availability)<br><span data-ttu-id="2eece-109">- 詳細については、[保存されているビュー](../fin-ops-core/fin-ops/get-started/saved-views.md) を参照してください。</span><span class="sxs-lookup"><span data-stu-id="2eece-109">- For more information, see [Saved views](../fin-ops-core/fin-ops/get-started/saved-views.md).</span></span> 

- <span data-ttu-id="2eece-110">**職位アクション** フォームには、更新された分析コード グリッドと新しいダイアログがあります (469495)。</span><span class="sxs-lookup"><span data-stu-id="2eece-110">The **Position actions** form has an updated dimensions grid and new dialogue (469495).</span></span>

- <span data-ttu-id="2eece-111">**Human Resources 共有パラメーター** の **詳細なアクセス** で **作業者情報へのアクセス制限** を "はい" に設定すると、福利厚生フォームには適切な作業者のみが表示されるようになりました (393384)。</span><span class="sxs-lookup"><span data-stu-id="2eece-111">If you set **Restrict access to worker information** to yes in **Advanced access** in **Human Resources Shared parameters**, benefits forms now show only the appropriate workers (393384).</span></span>

- <span data-ttu-id="2eece-112">**WorkCalendar** エンティティの新しいカレンダー生成オプション (477055):</span><span class="sxs-lookup"><span data-stu-id="2eece-112">New calendar generation options in the **WorkCalendar** entity (477055):</span></span><br><span data-ttu-id="2eece-113">- 既定の終了時刻</span><span class="sxs-lookup"><span data-stu-id="2eece-113">- Default ending time</span></span><br><span data-ttu-id="2eece-114">- 既定の開始時刻</span><span class="sxs-lookup"><span data-stu-id="2eece-114">-    Default starting time</span></span><br><span data-ttu-id="2eece-115">- 金曜日は就業日ですか</span><span class="sxs-lookup"><span data-stu-id="2eece-115">-  Is Friday working day</span></span><br><span data-ttu-id="2eece-116">- 月曜日は就業日ですか</span><span class="sxs-lookup"><span data-stu-id="2eece-116">-  Is Monday working day</span></span><br><span data-ttu-id="2eece-117">- 土曜日は就業日ですか</span><span class="sxs-lookup"><span data-stu-id="2eece-117">-  Is Saturday working day</span></span><br><span data-ttu-id="2eece-118">- 日曜日は就業日ですか</span><span class="sxs-lookup"><span data-stu-id="2eece-118">- Is Sunday working day</span></span><br><span data-ttu-id="2eece-119">- 木曜日は就業日ですか</span><span class="sxs-lookup"><span data-stu-id="2eece-119">- Is Thursday working day</span></span><br><span data-ttu-id="2eece-120">- 火曜日は就業日ですか</span><span class="sxs-lookup"><span data-stu-id="2eece-120">- Is Tuesday working day</span></span><br><span data-ttu-id="2eece-121">- 水曜日は就業日ですか</span><span class="sxs-lookup"><span data-stu-id="2eece-121">- Is Wednesday working day</span></span><br><span data-ttu-id="2eece-122">- 作業カレンダーの休日 ID</span><span class="sxs-lookup"><span data-stu-id="2eece-122">- Work calendar holiday ID</span></span>

- <span data-ttu-id="2eece-123">**LeaveBankTransactionV1** エンティティには、理由コードが含まれるようになりました (477823)。</span><span class="sxs-lookup"><span data-stu-id="2eece-123">The **LeaveBankTransactionV1** entity now includes the reason code (477823).</span></span>

- <span data-ttu-id="2eece-124">タスク記録を保存できるようになりました (492923)。</span><span class="sxs-lookup"><span data-stu-id="2eece-124">You can now save task recordings (492923).</span></span>

- <span data-ttu-id="2eece-125">データが **HCMWorkerContactEntity** から正常に公開されるようになりました (427620)。</span><span class="sxs-lookup"><span data-stu-id="2eece-125">Data is now published successfully from **HCMWorkerContactEntity** (427620).</span></span>

- <span data-ttu-id="2eece-126">契約社員作業者タイプの **報酬** クイック タブが、**作業者アクション** フォームに表示されるようになりました (482494)。</span><span class="sxs-lookup"><span data-stu-id="2eece-126">The **Compensation** fast tab now displays for the contractor worker type in the **Worker actions** form (482494).</span></span>

- <span data-ttu-id="2eece-127">**固定報酬** を設定した場合、**レベル** と **プラン** フィールドが必須になりました。</span><span class="sxs-lookup"><span data-stu-id="2eece-127">The **Level** and **Plan** fields are now mandatory if you set **Fixed compensation**.</span></span> <span data-ttu-id="2eece-128">これらのフィールドを空白のままにすると、エラー メッセージが表示されます (482497)。</span><span class="sxs-lookup"><span data-stu-id="2eece-128">An error message displays if you leave these fields blank (482497).</span></span>

- <span data-ttu-id="2eece-129">**福利厚生** の **プラン タイプ** フィールドがドロップ ダウンリストになりました (488768)。</span><span class="sxs-lookup"><span data-stu-id="2eece-129">The **Plan type** field in **Benefits** is now a dropdown list (488768).</span></span>

- <span data-ttu-id="2eece-130">システム管理者は、カスタム フィールドが Human Resources から削除された場合に、通知を受け取るようになりました (481408)。</span><span class="sxs-lookup"><span data-stu-id="2eece-130">System administrators now receive a notification if a custom field is deleted from Human Resources (481408).</span></span>

- <span data-ttu-id="2eece-131">従業員のプロセスを終了する間、ロックされているように見えた後、Human Resources は期待どおりに動作し、選択した会社を変更しません (479877)。</span><span class="sxs-lookup"><span data-stu-id="2eece-131">During the terminate employee process, Human Resources behaves as expected and doesn't change the selected company after appearing to lock (479877).</span></span> 

- <span data-ttu-id="2eece-132">マネージャーは、個人用設定を使用して数値列を追加できなくなりました (485317)。</span><span class="sxs-lookup"><span data-stu-id="2eece-132">Managers can no longer add a number column through personalization (485317).</span></span>

- <span data-ttu-id="2eece-133">マネージャーは、有効期限切れ ID 番号からデータ範囲フィルターを削除できなくなりました (485321)。</span><span class="sxs-lookup"><span data-stu-id="2eece-133">Managers can no longer remove the data range filter from identification numbers expiring (485321).</span></span>

- <span data-ttu-id="2eece-134">**報告先** フィールドが空の場合でも、職位にカーソルを合わせると職位の詳細が表示されます (433328)。</span><span class="sxs-lookup"><span data-stu-id="2eece-134">When the **Reports to** field is empty, position details still display when hovering over the position (433328).</span></span>

- <span data-ttu-id="2eece-135">従業員が、従業員セルフ サービスで福利厚生プラン情報を表示できるようになりました (481676)。</span><span class="sxs-lookup"><span data-stu-id="2eece-135">Employees can now view benefit plan information in Employee self service (481676).</span></span>

- <span data-ttu-id="2eece-136">従業員は、すべての登録済コースを表示できるようになりました (429048)。</span><span class="sxs-lookup"><span data-stu-id="2eece-136">Employees can now see all registered courses (429048).</span></span>

- <span data-ttu-id="2eece-137">**プロフェッショナル証明書** ページの表示オプションを制限できるようになりました。</span><span class="sxs-lookup"><span data-stu-id="2eece-137">You can now restrict viewing options for the **Professional certificates** page.</span></span> <span data-ttu-id="2eece-138">表示オプションを現在の法人、作業者ステータス別、および作業者タイプ別に制限できます (451501)。</span><span class="sxs-lookup"><span data-stu-id="2eece-138">You can restrict viewing options to the current legal entity, by worker status, and by worker type (451501).</span></span> 


## <a name="in-preview"></a><span data-ttu-id="2eece-139">プレビュー</span><span class="sxs-lookup"><span data-stu-id="2eece-139">In Preview</span></span>

### <a name="human-resources-app-in-teams"></a><span data-ttu-id="2eece-140">Teams の Human Resources アプリ</span><span class="sxs-lookup"><span data-stu-id="2eece-140">Human Resources app in Teams</span></span>

<span data-ttu-id="2eece-141">従業員は、Microsoft Teams 内で休暇の表示および申請ができます。</span><span class="sxs-lookup"><span data-stu-id="2eece-141">Employees can view and request time away from work within Microsoft Teams.</span></span> <span data-ttu-id="2eece-142">ボットと対話して、休暇申請を作成できます。</span><span class="sxs-lookup"><span data-stu-id="2eece-142">They can interact with a bot to create leave requests.</span></span> <span data-ttu-id="2eece-143">詳細については、以下を参照してください。</span><span class="sxs-lookup"><span data-stu-id="2eece-143">For more information, see:</span></span>

- <span data-ttu-id="2eece-144">Dynamics 365 2020 リリース ウェーブ 1 プランでの [Microsoft Teams の従業員の休暇および欠勤体験](/dynamics365-release-plan/2020wave1/dynamics365-human-resources/employee-leave-absence-experience-teams)</span><span class="sxs-lookup"><span data-stu-id="2eece-144">[Employee leave and absence experience in Microsoft Teams](/dynamics365-release-plan/2020wave1/dynamics365-human-resources/employee-leave-absence-experience-teams) in the Dynamics 365 2020 release wave 1 plan</span></span>
- <span data-ttu-id="2eece-145">Human Resources ドキュメントの [Teams の Human Resources アプリ](./hr-admin-teams-leave-app.md)</span><span class="sxs-lookup"><span data-stu-id="2eece-145">[Human Resources app in Teams](./hr-admin-teams-leave-app.md) in Human Resources documentation</span></span>

### <a name="human-resources-app-in-teams-preview-features"></a><span data-ttu-id="2eece-146">Teams の Human Resources アプリにおけるプレビュー機能</span><span class="sxs-lookup"><span data-stu-id="2eece-146">Human Resources app in Teams preview features</span></span>
 
-  <span data-ttu-id="2eece-147">**通知** : 休暇申請の提出者と承認者は、Teams の人事アプリで通知されます。</span><span class="sxs-lookup"><span data-stu-id="2eece-147">**Notifications**: Submitters and approvers of time-off requests will be notified in the Human Resources app in Teams.</span></span> <span data-ttu-id="2eece-148">承認者は、休暇申請を承認または拒否できます。</span><span class="sxs-lookup"><span data-stu-id="2eece-148">Approvers can approve or deny time-off requests.</span></span> <span data-ttu-id="2eece-149">申請が承認または拒否された場合は、送信者に通知されます。</span><span class="sxs-lookup"><span data-stu-id="2eece-149">Submitters will be notified if the request was approved or denied.</span></span> <span data-ttu-id="2eece-150">詳細については、以下を参照してください。</span><span class="sxs-lookup"><span data-stu-id="2eece-150">For more information, see:</span></span>
   - <span data-ttu-id="2eece-151">Dynamics 365 2020 リリース ウェーブ 2 プランでの [Microsoft Teams の従業員の休暇および欠勤体験](/dynamics365-release-plan/2020wave2/human-resources/dynamics365-human-resources/employee-leave-absence-experience-teams)</span><span class="sxs-lookup"><span data-stu-id="2eece-151">[Employee leave and absence experience in Microsoft Teams](/dynamics365-release-plan/2020wave2/human-resources/dynamics365-human-resources/employee-leave-absence-experience-teams) in the Dynamics 365 2020 release wave 2 plan</span></span>
   - <span data-ttu-id="2eece-152">Human Resources ドキュメントの [Teams の Human Resources アプリの通知を有効にする](./hr-admin-teams-leave-app.md#enable-notifications-for-the-human-resources-app-in-teams)</span><span class="sxs-lookup"><span data-stu-id="2eece-152">[Enable notifications for the Human Resources app in Teams](./hr-admin-teams-leave-app.md#enable-notifications-for-the-human-resources-app-in-teams) in Human Resources documentation</span></span>
   - <span data-ttu-id="2eece-153">Human Resources ドキュメントの [個々のユーザーの Teams の通知をオンまたはオフにする](./hr-admin-teams-leave-app.md#turn-teams-notifications-on-or-off-for-individual-users)</span><span class="sxs-lookup"><span data-stu-id="2eece-153">[Turn Teams notifications on or off for individual users](./hr-admin-teams-leave-app.md#turn-teams-notifications-on-or-off-for-individual-users) in Human Resources documentation</span></span>
   - <span data-ttu-id="2eece-154">Human Resources ドキュメントの [Teams の通知](./hr-teams-leave-app.md#respond-to-teams-notifications)</span><span class="sxs-lookup"><span data-stu-id="2eece-154">[Teams notifications](./hr-teams-leave-app.md#respond-to-teams-notifications) in Human Resources documentation</span></span>
   - <span data-ttu-id="2eece-155">Human Resources ドキュメントの [チームの休暇カレンダーの表示](./hr-teams-leave-app.md#view-your-teams-leave-calendar)</span><span class="sxs-lookup"><span data-stu-id="2eece-155">[View your team's leave calendar](./hr-teams-leave-app.md#view-your-teams-leave-calendar) in Human Resources documentation</span></span>
 
- <span data-ttu-id="2eece-156">**マネージャーの休暇カレンダー**: マネージャーは、直属の部下の承認済みおよび保留中の休暇をカレンダー表示で確認できます。</span><span class="sxs-lookup"><span data-stu-id="2eece-156">**Manager time-off calendar**: Managers can see approved and pending time off for their direct reports in a calendar view.</span></span> <span data-ttu-id="2eece-157">このビューを使用すると、チームのメンバーの休暇を簡単に把握することができます。</span><span class="sxs-lookup"><span data-stu-id="2eece-157">This view provides an easy understanding of when their team members are away from work.</span></span> <span data-ttu-id="2eece-158">詳細については、以下を参照してください。</span><span class="sxs-lookup"><span data-stu-id="2eece-158">For more information, see:</span></span>
   - <span data-ttu-id="2eece-159">Dynamics 365 2020 リリース ウェーブ 2 プランでの [Microsoft Teams の従業員の休暇および欠勤体験](/dynamics365-release-plan/2020wave2/human-resources/dynamics365-human-resources/employee-leave-absence-experience-teams)</span><span class="sxs-lookup"><span data-stu-id="2eece-159">[Employee leave and absence experience in Microsoft Teams](/dynamics365-release-plan/2020wave2/human-resources/dynamics365-human-resources/employee-leave-absence-experience-teams) in the Dynamics 365 2020 release wave 2 plan</span></span>
   - <span data-ttu-id="2eece-160">Human Resources ドキュメントの [チームの休暇カレンダーの表示](./hr-teams-leave-app.md#view-your-teams-leave-calendar)</span><span class="sxs-lookup"><span data-stu-id="2eece-160">[View your team's leave calendar](./hr-teams-leave-app.md#view-your-teams-leave-calendar) in Human Resources documentation</span></span>

### <a name="configuration-option-to-position-work-items-assigned-to-me-list-477004"></a><span data-ttu-id="2eece-161">自分のリストに割り当てられた作業項目を配置するコンフィギュレーション オプション (477004)</span><span class="sxs-lookup"><span data-stu-id="2eece-161">Configuration option to position Work items assigned to me list (477004)</span></span>

<span data-ttu-id="2eece-162">ダッシュボードの右側の列に、**自分に割り当てられた作業項目** リストを配置するための新しいオプションが使用可能になりました。</span><span class="sxs-lookup"><span data-stu-id="2eece-162">A new option is now available to position the **Work items assigned to me** list in the right-hand column of the dashboard.</span></span> <span data-ttu-id="2eece-163">この変更により、すべての作業項目とタスク一覧が同じ領域に表示されます。</span><span class="sxs-lookup"><span data-stu-id="2eece-163">With this change, all work items and to do lists display in the same area.</span></span> <span data-ttu-id="2eece-164">この機能を有効にするには、機能管理で **プレビュー - ワークフロー エクスペリエンスの拡張機能** をオンにします。</span><span class="sxs-lookup"><span data-stu-id="2eece-164">Enable this functionality by turning on **Preview - Workflow experience enhancements** in Feature management.</span></span> <span data-ttu-id="2eece-165">プレビュー機能をオンにする方法の詳細については、[機能の管理](hr-admin-manage-features.md) を参照してください。</span><span class="sxs-lookup"><span data-stu-id="2eece-165">For more information about turning on preview features, see [Manage features](hr-admin-manage-features.md).</span></span>

<span data-ttu-id="2eece-166">この機能は、人事アクション フォームに表示されるワークフロー オプションも促進します。</span><span class="sxs-lookup"><span data-stu-id="2eece-166">This feature also promotes the workflow options that appear in the personnel actions forms.</span></span> <span data-ttu-id="2eece-167">すばやくアクセスできるように、アクション クイック タブ上にも、ワークフロー オプションは表示されます。</span><span class="sxs-lookup"><span data-stu-id="2eece-167">Workflow options also appear above the action fast tab for quick access.</span></span> <span data-ttu-id="2eece-168">詳細については、以下を参照してください。</span><span class="sxs-lookup"><span data-stu-id="2eece-168">For more information, see:</span></span> 

- <span data-ttu-id="2eece-169">Dynamics 365 2020 のリリース ウェーブ 2 プランの [組織および人事管理ワークフロー エクスペリエンスの機能強化](/dynamics365-release-plan/2020wave2/human-resources/dynamics365-human-resources/organization-personnel-management-workflow-experience-enhancements)</span><span class="sxs-lookup"><span data-stu-id="2eece-169">[Organization and personnel management workflow experience enhancements](/dynamics365-release-plan/2020wave2/human-resources/dynamics365-human-resources/organization-personnel-management-workflow-experience-enhancements) in the Dynamics 365 2020 release wave 2 plan</span></span>

![自分自身に割り当てられた作業項目](./media/hr-workflow-work-items-assigned-to-me.png)

![ワークフロー項目のクイックアクセス](./media/hr-workflow-quick-access.png)

### <a name="leave-and-absence-calendar"></a><span data-ttu-id="2eece-172">休暇および欠勤カレンダー</span><span class="sxs-lookup"><span data-stu-id="2eece-172">Leave and absence calendar</span></span>

<span data-ttu-id="2eece-173">このリリースには、休暇および欠勤カレンダーの追加カレンダー オプションが含まれています。</span><span class="sxs-lookup"><span data-stu-id="2eece-173">This release includes additional calendar options for leave and absence calendars.</span></span> <span data-ttu-id="2eece-174">詳細については、[チームおよび会社カレンダーの表示](./hr-employee-self-service-calendar.md) を参照してください。</span><span class="sxs-lookup"><span data-stu-id="2eece-174">For more information, see [View team and company calendars](./hr-employee-self-service-calendar.md).</span></span>

## <a name="coming-soon"></a><span data-ttu-id="2eece-175">間もなく公開</span><span class="sxs-lookup"><span data-stu-id="2eece-175">Coming Soon</span></span>

### <a name="checklist-entities-included-in-dataverse"></a><span data-ttu-id="2eece-176">Dataverse に含まれるチェックリスト エンティティ</span><span class="sxs-lookup"><span data-stu-id="2eece-176">Checklist entities included in Dataverse</span></span>

<span data-ttu-id="2eece-177">オンボード、オフボード、転送、および業務プロセスのチェックリスト エンティティは、Dataverse ですぐに使用可能になります。</span><span class="sxs-lookup"><span data-stu-id="2eece-177">Checklist entities for Onboarding, Offboarding, Transfers, and Business processes will be available soon in Dataverse.</span></span>

### <a name="benefits-management-reason-codes"></a><span data-ttu-id="2eece-178">福利厚生管理の理由コード</span><span class="sxs-lookup"><span data-stu-id="2eece-178">Benefits management reason codes</span></span>

<span data-ttu-id="2eece-179">福利厚生管理の理由コードは、Human Resources の既存の理由コードと間もなく結合されます。</span><span class="sxs-lookup"><span data-stu-id="2eece-179">Benefits management reason codes will soon be combined with existing reason codes in Human Resources.</span></span> <span data-ttu-id="2eece-180">福利厚生管理で 15 文字を超える理由コードを作成した場合は、福利厚生管理の **理由コード** フォームで理由コードの名前を 15 文字以下に変更する必要があります。</span><span class="sxs-lookup"><span data-stu-id="2eece-180">If you created reason codes in Benefits management that are over 15 characters, you must change the name of the reason code in the Benefits management **Reason codes** form to be 15 characters or less.</span></span> <span data-ttu-id="2eece-181">名前を更新すると、理由コードが人事管理の既存の理由コード フォームの下に表示されます。</span><span class="sxs-lookup"><span data-stu-id="2eece-181">After you update the name, the reason code will appear under the existing reason code form in Personnel management.</span></span> <span data-ttu-id="2eece-182">この変更は将来使用可能になり、既存の機能には影響しません。</span><span class="sxs-lookup"><span data-stu-id="2eece-182">This change will be available in the future and won't affect existing functionality.</span></span>

## <a name="see-also"></a><span data-ttu-id="2eece-183">参照</span><span class="sxs-lookup"><span data-stu-id="2eece-183">See also</span></span>

[<span data-ttu-id="2eece-184">Human Resources の新機能および変更された機能</span><span class="sxs-lookup"><span data-stu-id="2eece-184">What's new or changed in Human Resources</span></span>](hr-admin-whats-new.md)</br>
[<span data-ttu-id="2eece-185">Dynamics 365 Human Resources 2019 のリリース ウェーブ 2 の概要</span><span class="sxs-lookup"><span data-stu-id="2eece-185">Overview of Dynamics 365 Human Resources 2019 release wave 2</span></span>](/dynamics365-release-plan/2019wave2/dynamics365-human-resources/)</br>
[<span data-ttu-id="2eece-186">更新プロセス</span><span class="sxs-lookup"><span data-stu-id="2eece-186">Update process</span></span>](hr-admin-setup-update-process.md)</br>
[<span data-ttu-id="2eece-187">機能の管理</span><span class="sxs-lookup"><span data-stu-id="2eece-187">Manage features</span></span>](hr-admin-manage-features.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]
