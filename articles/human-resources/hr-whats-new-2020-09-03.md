---
title: Dynamics 365 Human Resources (2020 年 9 月 3 日) の新機能および変更された機能
description: このトピックでは、2020 年 9 月 3 日に更新された、Microsoft Dynamics 365 Human Resources の新機能または変更された機能について説明します。
author: andreabichsel
ms.date: 09/03/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Human Resources
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: jaredha
ms.search.validFrom: 2020-09-03
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: 965f3ca859c601d26470038a889b0f21d2bdff5f
ms.sourcegitcommit: 3cdc42346bb653c13ab33a7142dbb7969f1f6dda
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 03/31/2021
ms.locfileid: "5800120"
---
# <a name="whats-new-or-changed-in-dynamics-365-human-resources-september-3-2020"></a><span data-ttu-id="5b25e-103">Dynamics 365 Human Resources (2020 年 9 月 3 日) の新機能および変更された機能</span><span class="sxs-lookup"><span data-stu-id="5b25e-103">What's new or changed in Dynamics 365 Human Resources (September 3, 2020)</span></span>

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

[!include [rename-banner](~/includes/cc-data-platform-banner.md)]

<span data-ttu-id="5b25e-104">このトピックでは、Dynamics 365 Human Resources の新機能または変更された機能について説明します。</span><span class="sxs-lookup"><span data-stu-id="5b25e-104">This topic describes features that are either new or changed in Dynamics 365 Human Resources.</span></span> <span data-ttu-id="5b25e-105">変更は、ビルド番号 8.1.3504 に適用されます。</span><span class="sxs-lookup"><span data-stu-id="5b25e-105">Changes apply to build number 8.1.3504.</span></span> <span data-ttu-id="5b25e-106">一部のヘッダーにあるかっこ内の数字は、参照用に Lifecycle Services (LCS) のサポート番号を参照しています。</span><span class="sxs-lookup"><span data-stu-id="5b25e-106">The numbers in parentheses in some headings refer to Lifecycle Services (LCS) support numbers for reference.</span></span>

<span data-ttu-id="5b25e-107">Human Resources の今後の機能の詳細については、[Dynamics 365 Human Resources 2019 のリリース ウェーブ 2 の概要](https://docs.microsoft.com/dynamics365-release-plan/2019wave2/dynamics365-human-resources/) を参照してください。</span><span class="sxs-lookup"><span data-stu-id="5b25e-107">For more information about upcoming features in Human Resources, see [Overview of Dynamics 365 Human Resources 2019 release wave 2](https://docs.microsoft.com/dynamics365-release-plan/2019wave2/dynamics365-human-resources/).</span></span> <span data-ttu-id="5b25e-108">Human Resources の更新プロセスの詳細については、[更新プロセス](hr-admin-setup-update-process.md) を参照してください。</span><span class="sxs-lookup"><span data-stu-id="5b25e-108">For more information about the update process for Human Resources, see [Update process](hr-admin-setup-update-process.md).</span></span>

## <a name="in-this-release"></a><span data-ttu-id="5b25e-109">今回のリリース</span><span class="sxs-lookup"><span data-stu-id="5b25e-109">In this release</span></span>

### <a name="new-default-financial-dimensions-grid-and-dialog-pattern-throughout-human-resources-469495"></a><span data-ttu-id="5b25e-110">Human Resources 全体の新しい既定の財務分析コード グリッドとダイアログ パターン (469495)</span><span class="sxs-lookup"><span data-stu-id="5b25e-110">New default financial dimensions grid and dialog pattern throughout Human Resources (469495)</span></span>

<span data-ttu-id="5b25e-111">財務分析コードの新しいパターンが、次の領域で使用できるようになりました:</span><span class="sxs-lookup"><span data-stu-id="5b25e-111">The new pattern for financial dimensions is now available in the following areas:</span></span>

- <span data-ttu-id="5b25e-112">職位アクション (フォーム: **HcmPositionActionDetail**)</span><span class="sxs-lookup"><span data-stu-id="5b25e-112">Position actions  (Form: **HcmPositionActionDetail**)</span></span>
- <span data-ttu-id="5b25e-113">給与所得コード (フォーム: **PayrollEarningCode**)</span><span class="sxs-lookup"><span data-stu-id="5b25e-113">Payroll earning codes  (Form: **PayrollEarningCode**)</span></span>

### <a name="entries-dont-appear-in-company-leave-calendar-if-leave-and-absence-calendar-enhancements-arent-enabled-484406"></a><span data-ttu-id="5b25e-114">休暇および欠勤カレンダーの機能拡張が有効になっていない場合、会社の休暇カレンダーにエントリが表示されない (484406)</span><span class="sxs-lookup"><span data-stu-id="5b25e-114">Entries don't appear in company leave calendar if Leave and absence calendar enhancements aren't enabled (484406)</span></span>

<span data-ttu-id="5b25e-115">今回のリリースでは、会社の休暇カレンダーに休暇エントリが表示されない問題が修正されています。</span><span class="sxs-lookup"><span data-stu-id="5b25e-115">This release corrects an issue where leave entries aren't displayed in the company leave calendar.</span></span> <span data-ttu-id="5b25e-116">この問題は、機能管理オプション **休暇および欠勤カレンダーの機能拡張** が有効になっていない場合にのみ発生します。</span><span class="sxs-lookup"><span data-stu-id="5b25e-116">This issue only occurs when the Feature management option **Leave and absence calendar enhancements** isn't enabled.</span></span>

### <a name="benefitplanemployeeentity-issue-467597"></a><span data-ttu-id="5b25e-117">BenefitPlanEmployeeEntity の問題 (467597)</span><span class="sxs-lookup"><span data-stu-id="5b25e-117">BenefitPlanEmployeeEntity issue (467597)</span></span>

<span data-ttu-id="5b25e-118">今回のリリースでは、**BenefitsPlanEmployee** エンティティに関する問題が修正されています。</span><span class="sxs-lookup"><span data-stu-id="5b25e-118">This release corrects an issue with the **BenefitsPlanEmployee** entity.</span></span> <span data-ttu-id="5b25e-119">作業者の登録をインポートする際に、**補充コード** と **計画タイプ コード** が正しく設定されるようになりました。</span><span class="sxs-lookup"><span data-stu-id="5b25e-119">When importing worker enrollments, the **Coverage code** and the **Plan type code** are now set correctly.</span></span> <span data-ttu-id="5b25e-120">この問題により、従業員の福利厚生プランが **作業者の福利厚生プラン** フォームと、従業員セルフ サービスの **オープン登録** フォームに正しく表示されませんでした。</span><span class="sxs-lookup"><span data-stu-id="5b25e-120">This issue caused employee benefit plans to display incorrectly in the **Worker benefits plan** and **Open enrollment** forms in Employee self service.</span></span>

### <a name="electronic-file-1094-c-output-missing-letter-in-xml-435190"></a><span data-ttu-id="5b25e-121">電子ファイル 1094-C の出力で XML に文字がない (435190)</span><span class="sxs-lookup"><span data-stu-id="5b25e-121">Electronic file 1094-C output missing letter in XML (435190)</span></span>

<span data-ttu-id="5b25e-122">この変更により、IRS への送信時に必要な文字が 1094-C 出力ファイルにないという問題が修正されています。</span><span class="sxs-lookup"><span data-stu-id="5b25e-122">This change corrects an issue with the 1094-C output file missing a character needed when submitting to the IRS.</span></span>

### <a name="employee-variable-compensation-table-mapped-to-fixed-compensation-form-476117"></a><span data-ttu-id="5b25e-123">固定報酬フォームにマップされた従業員の変動報酬テーブル (476117)</span><span class="sxs-lookup"><span data-stu-id="5b25e-123">Employee variable compensation table mapped to fixed compensation form (476117)</span></span>

<span data-ttu-id="5b25e-124">この変更により、固定報酬フィールドが固定報酬フォームと連携します。</span><span class="sxs-lookup"><span data-stu-id="5b25e-124">This change aligns the fixed compensation fields with the fixed compensation form.</span></span> <span data-ttu-id="5b25e-125">現在、変動報酬フィールドは、変動報酬フォームでのみ使用できます。</span><span class="sxs-lookup"><span data-stu-id="5b25e-125">Variable compensation fields are now only available with the variable compensation form.</span></span>

### <a name="leave-requests-allowed-before-enrollment-if-that-leave-type-has-a-negative-minimum-balance-469917"></a><span data-ttu-id="5b25e-126">休暇タイプにマイナスの最小残高がある場合に、登録前に休暇申請を許可する (469917)</span><span class="sxs-lookup"><span data-stu-id="5b25e-126">Leave requests allowed before enrollment if that leave type has a negative minimum balance (469917)</span></span>

<span data-ttu-id="5b25e-127">この変更により、登録にマイナスの最小残高があっても、プランに登録する前に休暇申請を入力することは禁止されます。</span><span class="sxs-lookup"><span data-stu-id="5b25e-127">This change prohibits entering leave requests before being enrolled in the plan, even if the enrollment has a negative minimum balance.</span></span> <span data-ttu-id="5b25e-128">申請は、プランが有効な場合にのみ入力または送信できます。</span><span class="sxs-lookup"><span data-stu-id="5b25e-128">You can only enter or submit requests when the plan is active.</span></span>

### <a name="document-templates-dont-download-457279"></a><span data-ttu-id="5b25e-129">ドキュメント テンプレートがダウンロードされない (457279)</span><span class="sxs-lookup"><span data-stu-id="5b25e-129">Document templates don't download (457279)</span></span>

<span data-ttu-id="5b25e-130">この変更により、すべてのドキュメント テンプレートをダウンロードできるようになりました。</span><span class="sxs-lookup"><span data-stu-id="5b25e-130">With this change, you can now download all document templates.</span></span> 

### <a name="data-displays-as-column-headers-instead-of-rows-for-the-pay-rate-field-in-the-compensation-plan-report-476077"></a><span data-ttu-id="5b25e-131">データが、報酬プラン レポートの支払レート フィールドに行ではなく、列ヘッダーとして表示される (476077)</span><span class="sxs-lookup"><span data-stu-id="5b25e-131">Data displays as column headers instead of rows for the Pay rate field in the compensation plan report (476077)</span></span>

<span data-ttu-id="5b25e-132">分析レポートに、**支払レート** の正しい情報が表示されるようになりました。</span><span class="sxs-lookup"><span data-stu-id="5b25e-132">The analytics report now displays the correct information for **Pay rate**.</span></span>

## <a name="in-preview"></a><span data-ttu-id="5b25e-133">プレビュー</span><span class="sxs-lookup"><span data-stu-id="5b25e-133">In preview</span></span>

### <a name="human-resources-application-in-teams"></a><span data-ttu-id="5b25e-134">Teams の Human Resources アプリケーション</span><span class="sxs-lookup"><span data-stu-id="5b25e-134">Human Resources application in Teams</span></span>

<span data-ttu-id="5b25e-135">従業員は、Microsoft Teams 内で休暇の表示および申請ができます。</span><span class="sxs-lookup"><span data-stu-id="5b25e-135">Employees can view and request time away from work within Microsoft Teams.</span></span> <span data-ttu-id="5b25e-136">ボットと対話して、休暇申請を作成できます。</span><span class="sxs-lookup"><span data-stu-id="5b25e-136">They can interact with a bot to create leave requests.</span></span> <span data-ttu-id="5b25e-137">詳細については、以下を参照してください。</span><span class="sxs-lookup"><span data-stu-id="5b25e-137">For more information, see:</span></span>

- <span data-ttu-id="5b25e-138">Dynamics 365 2020 リリース ウェーブ 1 プランでの [Microsoft Teams の従業員の休暇および欠勤体験](https://docs.microsoft.com/dynamics365-release-plan/2020wave1/dynamics365-human-resources/employee-leave-absence-experience-teams)</span><span class="sxs-lookup"><span data-stu-id="5b25e-138">[Employee leave and absence experience in Microsoft Teams](https://docs.microsoft.com/dynamics365-release-plan/2020wave1/dynamics365-human-resources/employee-leave-absence-experience-teams) in the Dynamics 365 2020 release wave 1 plan</span></span>
- <span data-ttu-id="5b25e-139">Human Resources ドキュメントの [Teams の Human Resources アプリ](https://go.microsoft.com/fwlink/?linkid=2127841)</span><span class="sxs-lookup"><span data-stu-id="5b25e-139">[Human Resources app in Teams](https://go.microsoft.com/fwlink/?linkid=2127841) in Human Resources documentation</span></span>

### <a name="human-resources-app-in-teams-preview-features"></a><span data-ttu-id="5b25e-140">Teams の Human Resources アプリにおけるプレビュー機能</span><span class="sxs-lookup"><span data-stu-id="5b25e-140">Human Resources app in Teams preview features</span></span>
 
-  <span data-ttu-id="5b25e-141">**通知** : 休暇申請の提出者と承認者は、Teams の人事アプリで通知されます。</span><span class="sxs-lookup"><span data-stu-id="5b25e-141">**Notifications**: Submitters and approvers of time-off requests will be notified in the Human Resources app in Teams.</span></span> <span data-ttu-id="5b25e-142">承認者は、休暇申請を承認または拒否することができます。</span><span class="sxs-lookup"><span data-stu-id="5b25e-142">Approvers will be able to approve or deny time-off requests.</span></span> <span data-ttu-id="5b25e-143">申請が承認または拒否された場合は、送信者に通知されます。</span><span class="sxs-lookup"><span data-stu-id="5b25e-143">Submitters will be notified if the request was approved or denied.</span></span> <span data-ttu-id="5b25e-144">詳細については、以下を参照してください。</span><span class="sxs-lookup"><span data-stu-id="5b25e-144">For more information, see:</span></span>
   - <span data-ttu-id="5b25e-145">Dynamics 365 2020 リリース ウェーブ 2 プランでの [Microsoft Teams の従業員の休暇および欠勤体験](https://docs.microsoft.com/dynamics365-release-plan/2020wave2/human-resources/dynamics365-human-resources/employee-leave-absence-experience-teams)</span><span class="sxs-lookup"><span data-stu-id="5b25e-145">[Employee leave and absence experience in Microsoft Teams](https://docs.microsoft.com/dynamics365-release-plan/2020wave2/human-resources/dynamics365-human-resources/employee-leave-absence-experience-teams) in the Dynamics 365 2020 release wave 2 plan</span></span>
   - <span data-ttu-id="5b25e-146">Human Resources ドキュメントの [Teams の Human Resources アプリの通知を有効にする](https://docs.microsoft.com/dynamics365/human-resources/hr-admin-teams-leave-app#enable-notifications-for-the-human-resources-app-in-teams)</span><span class="sxs-lookup"><span data-stu-id="5b25e-146">[Enable notifications for the Human Resources app in Teams](https://docs.microsoft.com/dynamics365/human-resources/hr-admin-teams-leave-app#enable-notifications-for-the-human-resources-app-in-teams) in Human Resources documentation</span></span>
   - <span data-ttu-id="5b25e-147">Human Resources ドキュメントの [個々のユーザーの Teams の通知をオンまたはオフにする](https://docs.microsoft.com/dynamics365/human-resources/hr-admin-teams-leave-app#turn-teams-notifications-on-or-off-for-individual-users)</span><span class="sxs-lookup"><span data-stu-id="5b25e-147">[Turn Teams notifications on or off for individual users](https://docs.microsoft.com/dynamics365/human-resources/hr-admin-teams-leave-app#turn-teams-notifications-on-or-off-for-individual-users) in Human Resources documentation</span></span>
   - <span data-ttu-id="5b25e-148">Human Resources ドキュメントの [Teams の通知](https://docs.microsoft.com/dynamics365/human-resources/hr-teams-leave-app#teams-notifications)</span><span class="sxs-lookup"><span data-stu-id="5b25e-148">[Teams notifications](https://docs.microsoft.com/dynamics365/human-resources/hr-teams-leave-app#teams-notifications) in Human Resources documentation</span></span>
   - <span data-ttu-id="5b25e-149">Human Resources ドキュメントの [チームの休暇カレンダーの表示](https://docs.microsoft.com/dynamics365/human-resources/hr-teams-leave-app#view-your-teams-leave-calendar)</span><span class="sxs-lookup"><span data-stu-id="5b25e-149">[View your team's leave calendar](https://docs.microsoft.com/dynamics365/human-resources/hr-teams-leave-app#view-your-teams-leave-calendar) in Human Resources documentation</span></span>
 
- <span data-ttu-id="5b25e-150">**マネージャーの休暇カレンダー** : マネージャーは、直属の部下の承認済み休暇、および保留中の休暇をカレンダーで確認することができます。</span><span class="sxs-lookup"><span data-stu-id="5b25e-150">**Manager time-off calendar**: Managers will be able to see approved and pending time off for their direct reports in a calendar view.</span></span> <span data-ttu-id="5b25e-151">このビューを使用すると、チームのメンバーの休暇を簡単に把握することができます。</span><span class="sxs-lookup"><span data-stu-id="5b25e-151">This view provides an easy understanding of when their team members are away from work.</span></span> <span data-ttu-id="5b25e-152">詳細については、以下を参照してください。</span><span class="sxs-lookup"><span data-stu-id="5b25e-152">For more information, see:</span></span>
   - <span data-ttu-id="5b25e-153">Dynamics 365 2020 リリース ウェーブ 2 プランでの [Microsoft Teams の従業員の休暇および欠勤体験](https://docs.microsoft.com/dynamics365-release-plan/2020wave2/human-resources/dynamics365-human-resources/employee-leave-absence-experience-teams)</span><span class="sxs-lookup"><span data-stu-id="5b25e-153">[Employee leave and absence experience in Microsoft Teams](https://docs.microsoft.com/dynamics365-release-plan/2020wave2/human-resources/dynamics365-human-resources/employee-leave-absence-experience-teams) in the Dynamics 365 2020 release wave 2 plan</span></span>
   - <span data-ttu-id="5b25e-154">Human Resources ドキュメントの [チームの休暇カレンダーの表示](https://docs.microsoft.com/dynamics365/human-resources/hr-teams-leave-app#view-your-teams-leave-calendar)</span><span class="sxs-lookup"><span data-stu-id="5b25e-154">[View your team's leave calendar](https://docs.microsoft.com/dynamics365/human-resources/hr-teams-leave-app#view-your-teams-leave-calendar) in Human Resources documentation</span></span>

### <a name="configuration-option-to-position-work-items-assigned-to-me-list-477004"></a><span data-ttu-id="5b25e-155">自分のリストに割り当てられた作業項目を配置するコンフィギュレーション オプション (477004)</span><span class="sxs-lookup"><span data-stu-id="5b25e-155">Configuration option to position Work items assigned to me list (477004)</span></span>

<span data-ttu-id="5b25e-156">ダッシュボードの右側の列に、**自分に割り当てられた作業項目** リストを配置するための新しいオプションが使用可能になりました。</span><span class="sxs-lookup"><span data-stu-id="5b25e-156">A new option is now available to position the **Work items assigned to me** list in the right-hand column of the dashboard.</span></span> <span data-ttu-id="5b25e-157">この変更により、すべての作業項目とタスク一覧が同じ領域に表示されます。</span><span class="sxs-lookup"><span data-stu-id="5b25e-157">With this change, all work items and to do lists display in the same area.</span></span> <span data-ttu-id="5b25e-158">この機能を有効にするには、機能管理で **プレビュー - ワークフロー エクスペリエンスの拡張機能** をオンにします。</span><span class="sxs-lookup"><span data-stu-id="5b25e-158">Enable this functionality by turning on **Preview - Workflow experience enhancements** in Feature management.</span></span> <span data-ttu-id="5b25e-159">プレビュー機能をオンにする方法の詳細については、[機能の管理](hr-admin-manage-features.md) を参照してください。</span><span class="sxs-lookup"><span data-stu-id="5b25e-159">For more information about turning on preview features, see [Manage features](hr-admin-manage-features.md).</span></span>

<span data-ttu-id="5b25e-160">この機能は、人事アクション フォームに表示されるワークフロー オプションも促進します。</span><span class="sxs-lookup"><span data-stu-id="5b25e-160">This feature also promotes the workflow options that appear in the personnel actions forms.</span></span> <span data-ttu-id="5b25e-161">すばやくアクセスできるように、アクション クイック タブ上にも、ワークフロー オプションは表示されます。</span><span class="sxs-lookup"><span data-stu-id="5b25e-161">Workflow options also appear above the action fast tab for quick access.</span></span> <span data-ttu-id="5b25e-162">詳細については、以下を参照してください。</span><span class="sxs-lookup"><span data-stu-id="5b25e-162">For more information, see:</span></span> 

- <span data-ttu-id="5b25e-163">Dynamics 365 2020 のリリース ウェーブ 2 プランの [組織および人事管理ワークフロー エクスペリエンスの機能強化](https://docs.microsoft.com/dynamics365-release-plan/2020wave2/human-resources/dynamics365-human-resources/organization-personnel-management-workflow-experience-enhancements)</span><span class="sxs-lookup"><span data-stu-id="5b25e-163">[Organization and personnel management workflow experience enhancements](https://docs.microsoft.com/dynamics365-release-plan/2020wave2/human-resources/dynamics365-human-resources/organization-personnel-management-workflow-experience-enhancements) in the Dynamics 365 2020 release wave 2 plan</span></span>

![自分自身に割り当てられた作業項目](./media/hr-workflow-work-items-assigned-to-me.png)

![ワークフロー項目のクイックアクセス](./media/hr-workflow-quick-access.png)

## <a name="coming-soon"></a><span data-ttu-id="5b25e-166">間もなく公開</span><span class="sxs-lookup"><span data-stu-id="5b25e-166">Coming Soon</span></span>

### <a name="checklist-entities-included-in-dataverse"></a><span data-ttu-id="5b25e-167">Dataverse に含まれるチェックリスト エンティティ</span><span class="sxs-lookup"><span data-stu-id="5b25e-167">Checklist entities included in Dataverse</span></span>

<span data-ttu-id="5b25e-168">オンボード、オフボード、転送、および業務プロセスのチェックリスト エンティティは、Dataverse ですぐに使用可能になります。</span><span class="sxs-lookup"><span data-stu-id="5b25e-168">Checklist entities for Onboarding, Offboarding, Transfers, and Business processes will be available soon in Dataverse.</span></span>

### <a name="benefits-management-reason-codes"></a><span data-ttu-id="5b25e-169">福利厚生管理の理由コード</span><span class="sxs-lookup"><span data-stu-id="5b25e-169">Benefits management reason codes</span></span>

<span data-ttu-id="5b25e-170">福利厚生管理の理由コードは、Human Resources の既存の理由コードと間もなく結合されます。</span><span class="sxs-lookup"><span data-stu-id="5b25e-170">Benefits management reason codes will soon be combined with existing reason codes in Human Resources.</span></span> <span data-ttu-id="5b25e-171">福利厚生管理で 15 文字を超える理由コードを作成した場合は、福利厚生管理の **理由コード** フォームで理由コードの名前を 15 文字以下に変更する必要があります。</span><span class="sxs-lookup"><span data-stu-id="5b25e-171">If you created reason codes in Benefits management that are over 15 characters, you must change the name of the reason code in the Benefits management **Reason codes** form to be 15 characters or less.</span></span> <span data-ttu-id="5b25e-172">名前を更新すると、理由コードが人事管理の既存の理由コード フォームの下に表示されます。</span><span class="sxs-lookup"><span data-stu-id="5b25e-172">After you update the name, the reason code will appear under the existing reason code form in Personnel management.</span></span> <span data-ttu-id="5b25e-173">この変更は将来使用可能になり、既存の機能には影響しません。</span><span class="sxs-lookup"><span data-stu-id="5b25e-173">This change will be available in the future and won't affect existing functionally.</span></span>

## <a name="see-also"></a><span data-ttu-id="5b25e-174">参照</span><span class="sxs-lookup"><span data-stu-id="5b25e-174">See also</span></span>

[<span data-ttu-id="5b25e-175">Human Resources の新機能および変更された機能</span><span class="sxs-lookup"><span data-stu-id="5b25e-175">What's new or changed in Human Resources</span></span>](hr-admin-whats-new.md)</br>
[<span data-ttu-id="5b25e-176">Dynamics 365 Human Resources 2019 のリリース ウェーブ 2 の概要</span><span class="sxs-lookup"><span data-stu-id="5b25e-176">Overview of Dynamics 365 Human Resources 2019 release wave 2</span></span>](https://docs.microsoft.com/dynamics365-release-plan/2019wave2/dynamics365-human-resources/)</br>
[<span data-ttu-id="5b25e-177">更新プロセス</span><span class="sxs-lookup"><span data-stu-id="5b25e-177">Update process</span></span>](hr-admin-setup-update-process.md)</br>
[<span data-ttu-id="5b25e-178">機能の管理</span><span class="sxs-lookup"><span data-stu-id="5b25e-178">Manage features</span></span>](hr-admin-manage-features.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]