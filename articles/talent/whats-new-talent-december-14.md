---
title: Dynamics 365 for Talent Core HR の新機能および変更された機能 (2018 年 12 月 14 日)
description: このトピックでは、Microsoft Dynamics 365 for Talent Core HR の新機能または変更された機能について説明します。
author: Darinkramer
manager: AnnBe
ms.date: 12/14/2018
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-talent
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: josaw
ms.search.scope: Talent
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: dkrame
ms.search.validFrom: 2018-12-14
ms.dyn365.ops.version: Talent
ms.openlocfilehash: 7d2866923efd7f115ad5290f35ed4fcac5e47573
ms.sourcegitcommit: 0f530e5f72a40f383868957a6b5cb0e446e4c795
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 01/29/2019
ms.locfileid: "305084"
---
# <a name="whats-new-or-changed-in-dynamics-365-for-talent-core-hr-december-14-2018"></a><span data-ttu-id="d1054-103">Dynamics 365 for Talent Core HR の新機能および変更された機能 (2018 年 12 月 14 日)</span><span class="sxs-lookup"><span data-stu-id="d1054-103">What's new or changed in Dynamics 365 for Talent Core HR (December 14, 2018)</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="d1054-104">**ビルド 8.1.2085**</span><span class="sxs-lookup"><span data-stu-id="d1054-104">**Build 8.1.2085**</span></span>

<span data-ttu-id="d1054-105">このトピックでは、Core HR の新機能または変更された機能について説明します。</span><span class="sxs-lookup"><span data-stu-id="d1054-105">This topic describes features that are either new or changed in Core HR.</span></span>

## <a name="changes"></a><span data-ttu-id="d1054-106">変更</span><span class="sxs-lookup"><span data-stu-id="d1054-106">Changes</span></span>

### <a name="us---aca-affordable-care-act-support-for-tax-year-2018-1095-b-and-1095-c-forms"></a><span data-ttu-id="d1054-107">米国 – ACA (Affordable Care Act) が 2018 税年度 の 1095 B および 1095-C フォームをサポート</span><span class="sxs-lookup"><span data-stu-id="d1054-107">US - ACA (Affordable Care Act) support for tax year 2018 1095-B and 1095-C forms</span></span>

<span data-ttu-id="d1054-108">毎年、該当する大規模雇用者 (ALE) は各フルタイム従業員に 1095-C を提供する必要があります。</span><span class="sxs-lookup"><span data-stu-id="d1054-108">Each year, Applicable Large Employers (ALEs) must provide each full-time employees with a 1095-C.</span></span> <span data-ttu-id="d1054-109">また、雇用主が自家保険を提供する場合、1095-C (ALE の場合) および 1095-B (小規模の雇用者の場合) を、提供される健康プログラムの対象となるフルタイムまたはパートタイム従業員に提供する必要があります。</span><span class="sxs-lookup"><span data-stu-id="d1054-109">In addition, if the employer provides self-insured coverage they must provide the 1095-C (if they are an ALE) and a 1095-B (if they are a small employer) to any employee, full-time or part-time, covered under one of their offered health plans.</span></span> <span data-ttu-id="d1054-110">この機能には、1095-C および 1095-B の両方の印刷可能なフォームが用意されています。</span><span class="sxs-lookup"><span data-stu-id="d1054-110">This feature provides printable forms for both the 1095-C and 1095-B.</span></span>

### <a name="during-import-submittedbypersonid-field-on-hcmperfjournalentity-is-ignored"></a><span data-ttu-id="d1054-111">インポート中は HcmPerfJournalEntity の SubmittedByPersonId フィールドが無視されます。</span><span class="sxs-lookup"><span data-stu-id="d1054-111">During import SubmittedByPersonId field on HcmPerfJournalEntity is ignored</span></span>

<span data-ttu-id="d1054-112">業績仕訳帳入力のインポート中およびエクスポート中に、**送信者**フィールドは無視されます。</span><span class="sxs-lookup"><span data-stu-id="d1054-112">When importing/exporting performance journal entries, the **Submitted by** field is ignored.</span></span> <span data-ttu-id="d1054-113">この変更によって、**インポート/エクスポート**値がエクスポート中のテーブルの値に反映され、インポート時にインポート ファイルで指定された値にシステムが更新されます。</span><span class="sxs-lookup"><span data-stu-id="d1054-113">With this change, the value **imported/exported** will reflect the value in the table during the export, when importing the system will be updated with the value supplied in the import file.</span></span>

### <a name="analytics-tab-on-leave-and-absence-workspace-displays-openconnectionerror-error-for-non-system-admin-roles"></a><span data-ttu-id="d1054-114">[休暇と欠勤] ワークスペースの分析タブで、非システム管理者ロールの "OpenConnectionError" エラーを表示</span><span class="sxs-lookup"><span data-stu-id="d1054-114">Analytics tab on 'Leave and absence' workspace displays "OpenConnectionError" error for non-system Admin roles</span></span>

<span data-ttu-id="d1054-115">この更新により、**休暇と欠勤**ワークスペースの**分析**タブを開いた時のエラーが表示されなくなりました。</span><span class="sxs-lookup"><span data-stu-id="d1054-115">With this update, no errors will be issued when opening the **Analytics** tab on the **Leave and Absence** workspace.</span></span>

### <a name="employee-self-service-position-hierarchy-drill-down-from-tile-fails-to-get-parent-node"></a><span data-ttu-id="d1054-116">従業員セルフ サービス、タイルの失敗から親ノードを取得する職位階層のドリルダウン</span><span class="sxs-lookup"><span data-stu-id="d1054-116">Employee self-service, Position Hierarchy drill-down from tile fails to get parent node</span></span>

<span data-ttu-id="d1054-117">職位階層が既存のワークスペースに表示されるよう個人用に設定された時の「親ノード取得の失敗」エラーを修正する変更が行われ、職位が階層内で選択されるようになりました。</span><span class="sxs-lookup"><span data-stu-id="d1054-117">A change has been made to correct the error "Getting the parent node failed" when the position hierarchy has been personalized to appear on an existing workspace and a position is selected in the hierarchy.</span></span>  

### <a name="must-be-system-admin-to-see-the-payroll-tab-in-the-position-page"></a><span data-ttu-id="d1054-118">システム管理者は職位ページの給与タブを確認する必要があります</span><span class="sxs-lookup"><span data-stu-id="d1054-118">Must be System Admin to see the Payroll tab in the Position page</span></span>

<span data-ttu-id="d1054-119">「給与作業者と職位詳細を管理」の既存の権限に正しいセキュリティ要素を加える変更が行われました。</span><span class="sxs-lookup"><span data-stu-id="d1054-119">A change has been made to include the correct security elements in the existing privilege: "Maintain payroll worker and position detail".</span></span> <span data-ttu-id="d1054-120">この変更により、既定では、給与管理者が職位ページ上の給与フィールドにアクセスできます。</span><span class="sxs-lookup"><span data-stu-id="d1054-120">With this change, by default, the Payroll Administrator will have access to the Payroll fields on the Position page.</span></span>

### <a name="error-when-submitting-performance-review-to-manager-and-the-reviewsperfperiod-placeholder-is-used-in-the-submission-instructions"></a><span data-ttu-id="d1054-121">業務の確認をマネージャーに送信しているとき、および %Reviews.PerfPeriod% プレースホルダ―を送信指示で使用しているときのエラー</span><span class="sxs-lookup"><span data-stu-id="d1054-121">Error when submitting performance review to manager and the %Reviews.PerfPeriod% placeholder is used in the Submission instructions</span></span>

<span data-ttu-id="d1054-122">送信指示で ％Reviews.PerfPeriod％ プレースホルダーを使用する場合に「null 参照」エラーを修正する変更が行われました。</span><span class="sxs-lookup"><span data-stu-id="d1054-122">A change has been made that corrects the "Null Reference" error when using the %Reviews.PerfPeriod% placeholder in the Submission instructions.</span></span>

### <a name="workforce-power-bi-report-shows-error-when-worker-seniority-date-is-a-leap-day"></a><span data-ttu-id="d1054-123">作業者の勤続日数がうるう日の場合、要員指標 Power BI レポートにエラーが表示されます</span><span class="sxs-lookup"><span data-stu-id="d1054-123">Workforce Power BI report shows error when worker seniority date is a leap day</span></span>

<span data-ttu-id="d1054-124">この変更により、うるう日は Power BI でサポートされます。</span><span class="sxs-lookup"><span data-stu-id="d1054-124">With this change, leap days are now supported in Power BI.</span></span>

### <a name="integration-between-core-hr-and-attract"></a><span data-ttu-id="d1054-125">Core HR と Attract 間の統合</span><span class="sxs-lookup"><span data-stu-id="d1054-125">Integration between Core HR and Attract</span></span>

<span data-ttu-id="d1054-126">採用候補者に関連する Core HR と Attract の統合を更新するための変更が行われました。</span><span class="sxs-lookup"><span data-stu-id="d1054-126">A change has been made to update the integration between Core HR and Attract related to candidates to hire.</span></span> <span data-ttu-id="d1054-127">採用候補者を**人事管理**ワークスペースに表示するため、次の CDS for Apps (CDS 2.0) エンティティが使用されます。</span><span class="sxs-lookup"><span data-stu-id="d1054-127">For candidates to hire to be visible in the **Personnel Management** workspace, the following CDS for Apps (CDS 2.0) entities are used:</span></span>

<span data-ttu-id="d1054-128">求人応募</span><span class="sxs-lookup"><span data-stu-id="d1054-128">Job Application</span></span>
- <span data-ttu-id="d1054-129">状態理由はオファー承諾済に設定する必要があります。</span><span class="sxs-lookup"><span data-stu-id="d1054-129">Status Reason needs to be set to Offer Accepted</span></span>
-   <span data-ttu-id="d1054-130">候補者および求人の提供</span><span class="sxs-lookup"><span data-stu-id="d1054-130">Provides Candidate and Job Opening</span></span>

<span data-ttu-id="d1054-131">候補者</span><span class="sxs-lookup"><span data-stu-id="d1054-131">Candidate</span></span>
-   <span data-ttu-id="d1054-132">候補者情報の提供</span><span class="sxs-lookup"><span data-stu-id="d1054-132">Provides Candidate information</span></span>

<span data-ttu-id="d1054-133">求人</span><span class="sxs-lookup"><span data-stu-id="d1054-133">Job Opening</span></span>
-   <span data-ttu-id="d1054-134">求人 ID および求人参加者の提供</span><span class="sxs-lookup"><span data-stu-id="d1054-134">Provides Job Opening ID and Job Opening Participants</span></span>

<span data-ttu-id="d1054-135">求人参加者</span><span class="sxs-lookup"><span data-stu-id="d1054-135">Job Opening Participants</span></span>
-   <span data-ttu-id="d1054-136">採用マネージャーへの提供</span><span class="sxs-lookup"><span data-stu-id="d1054-136">Provides Hiring Manager</span></span>

<span data-ttu-id="d1054-137">候補者が人事管理に追加されると、候補者カードで利用可能な新しいオプションを使用して候補者を消去することもできるようになりました。</span><span class="sxs-lookup"><span data-stu-id="d1054-137">When a candidate is added to Personnel Management, the candidate can now also be dismissed using a new option available on the candidate card.</span></span>

## <a name="coming-soon"></a><span data-ttu-id="d1054-138">間もなく公開</span><span class="sxs-lookup"><span data-stu-id="d1054-138">Coming soon</span></span>

### <a name="leave-and-absence-future-leave-and-forecasting-leave-balances"></a><span data-ttu-id="d1054-139">休暇と欠勤: 未来の休暇と休暇残高の予測</span><span class="sxs-lookup"><span data-stu-id="d1054-139">Leave and absence: Future leave and forecasting leave balances</span></span>

<span data-ttu-id="d1054-140">従業員が休暇を予測し、現在の休暇残高に影響を与えずに将来の休暇時間要求ができるようにするための変更が行われたため、休暇残高の表示方法も変更されました。</span><span class="sxs-lookup"><span data-stu-id="d1054-140">With the changes being made to allow for employees to forecast time off and request future time off requests without impacting their current time off balances, the way the time off balances are displayed is also changing.</span></span> 

<span data-ttu-id="d1054-141">現在表示されている使用可能な残高は、現在までの見越しおよび承認されたすべての休暇申請を含む申請に対して利用可能な休暇の量です。</span><span class="sxs-lookup"><span data-stu-id="d1054-141">The available balance currently displayed is the amount of time off available for requests including accruals through today and all approved leave requests to the end of time.</span></span> 

<span data-ttu-id="d1054-142">予測機能がリリースされると、表示されている残高は、現在までの見越額および申請を含めて、現在の休暇の残高に変更されます。</span><span class="sxs-lookup"><span data-stu-id="d1054-142">When the ability to forecast is released, the balance displayed changes to  be the current balance of time off including accruals through today and requests through today.</span></span> <span data-ttu-id="d1054-143">従業員およびマネージャーの両方が、**休暇**カードと**残高休暇**ウィンドウにある従業員およびマネージャー セルフサービスで更新された残高を参照できます。</span><span class="sxs-lookup"><span data-stu-id="d1054-143">Employees and managers will see these updated balances in employee and manager self-service on the **Time off** card and in the **Time off balances** window.</span></span> <span data-ttu-id="d1054-144">**人員**ワークスペースと従業員の**割り当て済の休暇計画**ウィンドウにある更新済みの残高は HR マネージャーが参照できます。</span><span class="sxs-lookup"><span data-stu-id="d1054-144">HR managers will see these updated balances in the **People** workspace and in the employee’s **Assigned leave plans** window.</span></span>

## <a name="known-issue"></a><span data-ttu-id="d1054-145">既知の問題</span><span class="sxs-lookup"><span data-stu-id="d1054-145">Known issue</span></span>

### <a name="mapping-errors-in-the-integration-with-finance-and-operations"></a><span data-ttu-id="d1054-146">Finance and Operations との統合のマッピング エラー</span><span class="sxs-lookup"><span data-stu-id="d1054-146">Mapping errors in the integration with Finance and Operations</span></span>

<span data-ttu-id="d1054-147">次の問題は、Dynamics 365 for Finance and Operations を統合するための現在のテンプレートで識別されています。</span><span class="sxs-lookup"><span data-stu-id="d1054-147">The following issues have been identified in the current template for integrating Talent with Dynamics 365 for Finance and Operations.</span></span> <span data-ttu-id="d1054-148">新しいテンプレートは、間もなく公開され、作成されたすべての新しい統合プロジェクトに適用されます。</span><span class="sxs-lookup"><span data-stu-id="d1054-148">A new template will be published soon and will be applied to all new integration projects that are created.</span></span> <span data-ttu-id="d1054-149">既存の統合プロジェクトのために、タスク マッピングを更新できます。</span><span class="sxs-lookup"><span data-stu-id="d1054-149">For existing integration projects, the task mappings can be updated.</span></span> <span data-ttu-id="d1054-150">更新されたマッピングについては、次の表を参照してください。</span><span class="sxs-lookup"><span data-stu-id="d1054-150">Refer to the following table for updated mappings.</span></span> 

>[!NOTE]
> <span data-ttu-id="d1054-151">ジョブ職位から職位親ジョブ割り当てタスクはデータが統合されていません。</span><span class="sxs-lookup"><span data-stu-id="d1054-151">The Job Positions to Positions Parent Job Assignment task does not integrate data.</span></span> <span data-ttu-id="d1054-152">この問題は現在調査中です。</span><span class="sxs-lookup"><span data-stu-id="d1054-152">This is an issue that is currently being researched.</span></span> <span data-ttu-id="d1054-153">現在のマッピングに回避策はありません。</span><span class="sxs-lookup"><span data-stu-id="d1054-153">There is no workaround in the current mapping.</span></span> 

<span data-ttu-id="d1054-154">部門から作業単位タスクは、次のマッピングの更新が必要です。</span><span class="sxs-lookup"><span data-stu-id="d1054-154">The Departments to Operating unit task needs the following mappings updated.</span></span>

| <span data-ttu-id="d1054-155">既存のソース フィールド</span><span class="sxs-lookup"><span data-stu-id="d1054-155">Existing source field</span></span>          | <span data-ttu-id="d1054-156">新規ソース フィールド</span><span class="sxs-lookup"><span data-stu-id="d1054-156">New source field</span></span> |
| -------------------------------|------------------|
| <span data-ttu-id="d1054-157">cdm_description (説明)</span><span class="sxs-lookup"><span data-stu-id="d1054-157">cdm_description (Description)</span></span>  | <span data-ttu-id="d1054-158">cdm_name (名前)</span><span class="sxs-lookup"><span data-stu-id="d1054-158">cdm_name (Name)</span></span>  |

<span data-ttu-id="d1054-159">追加のマッピングも追加する必要があります。</span><span class="sxs-lookup"><span data-stu-id="d1054-159">An additional mapping also needs to be added.</span></span> <span data-ttu-id="d1054-160">最後の**なし**フィールドを選択して、次のマッピングを追加します。</span><span class="sxs-lookup"><span data-stu-id="d1054-160">Select the last **None** field to add the following mapping.</span></span>

| <span data-ttu-id="d1054-161">ソース フィールド</span><span class="sxs-lookup"><span data-stu-id="d1054-161">Source field</span></span>                   | <span data-ttu-id="d1054-162">出力先フィールド</span><span class="sxs-lookup"><span data-stu-id="d1054-162">Destination field</span></span>    |
| -------------------------------|----------------------|
| <span data-ttu-id="d1054-163">cdm_description (説明)</span><span class="sxs-lookup"><span data-stu-id="d1054-163">cdm_description (Description)</span></span>  | <span data-ttu-id="d1054-164">NAMEALIAS (NAMEALIAS)</span><span class="sxs-lookup"><span data-stu-id="d1054-164">NAMEALIAS (NAMEALIAS)</span></span>|

<span data-ttu-id="d1054-165">更新されたマッピングは、次の画像のようになります。</span><span class="sxs-lookup"><span data-stu-id="d1054-165">The updated mappings should look like the following image.</span></span>

![部門から作業単位タスク](./media/DepartmentMapping.png)


<span data-ttu-id="d1054-167">ジョブからジョブ詳細タスクへは、次のマッピングの更新が必要です。</span><span class="sxs-lookup"><span data-stu-id="d1054-167">The Jobs to Job Detail task needs the following mappings updated.</span></span>

| <span data-ttu-id="d1054-168">既存のソース フィールド</span><span class="sxs-lookup"><span data-stu-id="d1054-168">Existing source field</span></span>          | <span data-ttu-id="d1054-169">新規ソース フィールド</span><span class="sxs-lookup"><span data-stu-id="d1054-169">New source field</span></span>                   |
| -------------------------------|------------------------------------|
| <span data-ttu-id="d1054-170">cdm_name (名前)</span><span class="sxs-lookup"><span data-stu-id="d1054-170">cdm_name (Name)</span></span>                | <span data-ttu-id="d1054-171">cdm_description (説明)</span><span class="sxs-lookup"><span data-stu-id="d1054-171">cdm_description (Description)</span></span>      |
| <span data-ttu-id="d1054-172">cdm_name (名前)</span><span class="sxs-lookup"><span data-stu-id="d1054-172">cdm_name (Description)</span></span>         | <span data-ttu-id="d1054-173">cdm_jobdescription (職務明細書)</span><span class="sxs-lookup"><span data-stu-id="d1054-173">cdm_jobdescription(Job Description)</span></span>|


<span data-ttu-id="d1054-174">更新されたマッピングは、以下の画像のようになります。</span><span class="sxs-lookup"><span data-stu-id="d1054-174">The updated mappings should look like the image below.</span></span>

![ジョブからジョブ詳細タスク](./media/JobMapping.png)

<span data-ttu-id="d1054-176">作業者から作業タスクへは、次のマッピングの更新が必要です。</span><span class="sxs-lookup"><span data-stu-id="d1054-176">The Workers to Work task needs the following mappings updated.</span></span>

| <span data-ttu-id="d1054-177">既存のソース フィールド</span><span class="sxs-lookup"><span data-stu-id="d1054-177">Existing source field</span></span>                 | <span data-ttu-id="d1054-178">新規ソース フィールド</span><span class="sxs-lookup"><span data-stu-id="d1054-178">New source field</span></span>                               |
| --------------------------------------|------------------------------------------------|
| <span data-ttu-id="d1054-179">cdm_emailaddress1 (電子メール アドレス 1)</span><span class="sxs-lookup"><span data-stu-id="d1054-179">cdm_emailaddress1 (Email Address 1)</span></span>   | <span data-ttu-id="d1054-180">cdm_primaryemailaddress (主要な電子メール アドレス</span><span class="sxs-lookup"><span data-stu-id="d1054-180">cdm_primaryemailaddress (Primary Email Address</span></span> |
| <span data-ttu-id="d1054-181">cdm_telephone1 (電話1)</span><span class="sxs-lookup"><span data-stu-id="d1054-181">cdm_telephone1 (Telephone 1)</span></span>          | <span data-ttu-id="d1054-182">cdm_primarytelephone (代表電話)</span><span class="sxs-lookup"><span data-stu-id="d1054-182">cdm_primarytelephone (Primary Telephone)</span></span>       |

<span data-ttu-id="d1054-183">性別フィールドの変換は、更新する必要があります。</span><span class="sxs-lookup"><span data-stu-id="d1054-183">The Gender field transform also needs to be updated.</span></span> <span data-ttu-id="d1054-184">性別の**fn** (機能) マップを選択し、次の値のマッピングを更新します。</span><span class="sxs-lookup"><span data-stu-id="d1054-184">Select the **fn** (function) map type for Gender and update the following value mappings.</span></span>

| <span data-ttu-id="d1054-185">CDS 値</span><span class="sxs-lookup"><span data-stu-id="d1054-185">CDS value</span></span>                   | <span data-ttu-id="d1054-186">Finance and Operations 値</span><span class="sxs-lookup"><span data-stu-id="d1054-186">Finance and Operations value</span></span>                     |
| ----------------------------|--------------------------------------------------|
| <span data-ttu-id="d1054-187">75440000</span><span class="sxs-lookup"><span data-stu-id="d1054-187">75440000</span></span>                    | <span data-ttu-id="d1054-188">男性</span><span class="sxs-lookup"><span data-stu-id="d1054-188">Male</span></span>                                             |
| <span data-ttu-id="d1054-189">75440001</span><span class="sxs-lookup"><span data-stu-id="d1054-189">75440001</span></span>                    | <span data-ttu-id="d1054-190">女性</span><span class="sxs-lookup"><span data-stu-id="d1054-190">Female</span></span>                                           |
| <span data-ttu-id="d1054-191">75440002</span><span class="sxs-lookup"><span data-stu-id="d1054-191">75440002</span></span>                    | <span data-ttu-id="d1054-192">なし</span><span class="sxs-lookup"><span data-stu-id="d1054-192">None</span></span>                                             | 
| <span data-ttu-id="d1054-193">75440003</span><span class="sxs-lookup"><span data-stu-id="d1054-193">75440003</span></span>                    | <span data-ttu-id="d1054-194">不特定</span><span class="sxs-lookup"><span data-stu-id="d1054-194">NonSpecific</span></span>                                      |

<span data-ttu-id="d1054-195">更新されたマッピングは、次の画像のようになります。</span><span class="sxs-lookup"><span data-stu-id="d1054-195">The updated mappings should look like the following images.</span></span>

![作業者から作業者タスク](./media/WorkerMapping.png)

![性別フィールドの変換](./media/WorkerTransform.png)
