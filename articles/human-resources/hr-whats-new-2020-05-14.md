---
title: Dynamics 365 Human Resources (2020年5月14日) の新機能と変更された機能
description: このトピックでは、2020 年 5 月 14 日に更新された、Microsoft Dynamics 365 Human Resources の新機能、または変更された機能について説明します。
author: Darinkramer
manager: AnnBe
ms.date: 05/14/2020
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
ms.author: dkrame
ms.search.validFrom: 2020-05-14
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: 76ca497cc7fabf737c8a0ee71363f22fd4201ea8
ms.sourcegitcommit: e89bb3e5420a6ece84f4e80c11e360b4a042f59d
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 11/17/2020
ms.locfileid: "4528500"
---
# <a name="whats-new-or-changed-in-dynamics-365-human-resources-may-14-2020"></a><span data-ttu-id="54323-103">Dynamics 365 Human Resources (2020年5月14日) の新機能と変更された機能</span><span class="sxs-lookup"><span data-stu-id="54323-103">What's new or changed in Dynamics 365 Human Resources (May 14, 2020)</span></span>

[!include [rename-banner](~/includes/cc-data-platform-banner.md)]

<span data-ttu-id="54323-104">このトピックでは、Dynamics 365 Human Resources の新機能または変更された機能について説明します。</span><span class="sxs-lookup"><span data-stu-id="54323-104">This topic describes features that are either new or changed in Dynamics 365 Human Resources.</span></span> <span data-ttu-id="54323-105">変更は、ビルド番号 8.1.3244 に適用されます。</span><span class="sxs-lookup"><span data-stu-id="54323-105">Changes apply to build number 8.1.3244.</span></span> <span data-ttu-id="54323-106">一部のヘッダーにあるかっこ内の数字は、参照用に Lifecycle Services (LCS) のサポート番号を参照しています。</span><span class="sxs-lookup"><span data-stu-id="54323-106">The numbers in parentheses in some headings refer to Lifecycle Services (LCS) support numbers for reference.</span></span>

## <a name="platform-changes"></a><span data-ttu-id="54323-107">プラットフォームの変更</span><span class="sxs-lookup"><span data-stu-id="54323-107">Platform changes</span></span>

<span data-ttu-id="54323-108">プラットフォームの変更は今週のリリースに含まれています。</span><span class="sxs-lookup"><span data-stu-id="54323-108">Platform changes are included in this week's release.</span></span> <span data-ttu-id="54323-109">詳細については、[Finance and Operations アプリのバージョン 10.0.10 のプラットフォーム更新プログラム (2020年5月) ](https://docs.microsoft.com/dynamics365/fin-ops-core/dev-itpro/get-started/whats-new-platform-update-34) を参照してください。</span><span class="sxs-lookup"><span data-stu-id="54323-109">For more information, see [Platform updates for version 10.0.10 of Finance and Operations apps (May 2020)](https://docs.microsoft.com/dynamics365/fin-ops-core/dev-itpro/get-started/whats-new-platform-update-34).</span></span> <span data-ttu-id="54323-110">このリリースには、バグ修正や保存されたビューへの変更が含まれています。</span><span class="sxs-lookup"><span data-stu-id="54323-110">This release includes bug fixes and changes to saved views.</span></span>
 
## <a name="ensure-common-data-service-picklists-are-consistent-with-leave-enums-436343"></a><span data-ttu-id="54323-111">Common Data Service の候補リストがすべての列挙と一致することを保証する (436343)</span><span class="sxs-lookup"><span data-stu-id="54323-111">Ensure Common Data Service picklists are consistent with Leave enums (436343)</span></span>

<span data-ttu-id="54323-112">Common Data Service の候補リストがすべての列挙と一致するようになっています。</span><span class="sxs-lookup"><span data-stu-id="54323-112">Common Data Service picklists are now consistent with Leave enums.</span></span>

## <a name="allow-users-to-configure-leave-request-workflow-based-on-the-request-amount-300044"></a><span data-ttu-id="54323-113">申請の量に応じた休暇申請のワークフローを構成できるようにする (300044)</span><span class="sxs-lookup"><span data-stu-id="54323-113">Allow users to configure leave request workflow based on the request amount (300044)</span></span>

<span data-ttu-id="54323-114">申請の量に応じて休暇申請のワークフローを設定することができます。</span><span class="sxs-lookup"><span data-stu-id="54323-114">Users can configure leave requests workflows based on request amounts.</span></span>
 
## <a name="new-worker-form-exposes-data-through-the-view-menu-when-advanced-security-is-enabled-403185"></a><span data-ttu-id="54323-115">高度なセキュリティが有効になっている場合、新しい作業者フォームにて[表示] メニューを使用してデータが公開されます (403185)</span><span class="sxs-lookup"><span data-stu-id="54323-115">New worker form exposes data through the View menu when advanced security is enabled (403185)</span></span>

<span data-ttu-id="54323-116">このリリースでは、高度なアクセスが有効になっており、他社の作業者がアクセスできるように設定されている場合に、法人間での作業者の閲覧方法が修正されます。</span><span class="sxs-lookup"><span data-stu-id="54323-116">This release corrects how viewing workers across legal entities functions when advanced access is enabled and workers in other companies are accessible.</span></span>

## <a name="allow-running-leave-accruals-for-a-single-plan-or-a-single-company-318844"></a><span data-ttu-id="54323-117">単体のプランまたは単一の会社ので連続した休暇取得を可能にする (318844)</span><span class="sxs-lookup"><span data-stu-id="54323-117">Allow running leave accruals for a single plan or a single company (318844)</span></span>

<span data-ttu-id="54323-118">この変更により、会社やプランの見越し計上を実行できます。</span><span class="sxs-lookup"><span data-stu-id="54323-118">With this change, you can run accruals for a company or a plan.</span></span>
 
## <a name="show-the-positions-full-time-equivalent-fte-in-the-enrolled-workers-form-414658"></a><span data-ttu-id="54323-119">登録された作業者フォームに該当する職位のフルタイム換算 (FTE) を表示する (414658)</span><span class="sxs-lookup"><span data-stu-id="54323-119">Show the position's full-time equivalent (FTE) in the Enrolled workers form (414658)</span></span>

<span data-ttu-id="54323-120">休暇タイプで [FTE] オプションが有効になっている場合は、作業者の職位の FTE 値によって作業者の見越計上率が決まります。</span><span class="sxs-lookup"><span data-stu-id="54323-120">The FTE value from a worker's position determines a worker's accrual rate when the FTE option is enabled on the leave type.</span></span> <span data-ttu-id="54323-121">このフィールドは、 **登録された作業者** フォームと **一括登録** ダイアログに含まれるようになりました。</span><span class="sxs-lookup"><span data-stu-id="54323-121">This field is now included in **Enrolled workers** form and the **Mass enrollment** dialog.</span></span>

## <a name="add-leave-balance-expiration-batch-job-431266"></a><span data-ttu-id="54323-122">休暇残数の有効期限バッチジョブの追加 (431266)</span><span class="sxs-lookup"><span data-stu-id="54323-122">Add leave balance expiration batch job (431266)</span></span>

<span data-ttu-id="54323-123">新しいバッチジョブを日次で実行できるようになりました。</span><span class="sxs-lookup"><span data-stu-id="54323-123">A new batch job is now available that runs daily.</span></span> <span data-ttu-id="54323-124">これにより、有効期限が当日になると、残日数が減少します。</span><span class="sxs-lookup"><span data-stu-id="54323-124">It decreases the remaining leave balance when expiration dates become current.</span></span>

## <a name="exporting-personal-contacts-for-an-employee-using-the-worker-personal-contact-person-entity-doesnt-export-personal-contacts-with-the-parent-relationship-type-345893"></a><span data-ttu-id="54323-125">作業者の個人連絡担当者を使用して、従業員の個人の連絡先をエクスポートしても、親関係タイプの個人連絡先がエクスポートされない (345893)</span><span class="sxs-lookup"><span data-stu-id="54323-125">Exporting personal contacts for an employee using the Worker personal contact person entity doesn't export personal contacts with the Parent relationship type (345893)</span></span>

<span data-ttu-id="54323-126">**作業者の個人連絡担当者** データ エンティティ ( DMF の **HcmPersonalContactPersonEntity** と OData の **PersonalContactPerson**) は、**親** のリレーションシップ タイプが設定されている個人の連絡先をエクスポートできませんでした。</span><span class="sxs-lookup"><span data-stu-id="54323-126">The **Worker personal contact person** data entity (**HcmPersonalContactPersonEntity** in DMF and **PersonalContactPerson** in OData) couldn't export personal contacts that have a relationship type of **Parent**.</span></span> <span data-ttu-id="54323-127">この問題は、この変更後に作成される個人の連絡先に対して修正されています。</span><span class="sxs-lookup"><span data-stu-id="54323-127">This issue is fixed for personal contacts that are created after this change.</span></span> <span data-ttu-id="54323-128">**親** タイプの既存の個人連絡先 は、将来的なリリースで修正されます。</span><span class="sxs-lookup"><span data-stu-id="54323-128">Existing personal contacts of type **Parent** will be fixed in a later release.</span></span>

## <a name="reason-codes-display-across-different-scenarios-when-theyre-marked-as-leave-and-absence-and-the-streamlined-employee-form-is-enabled-434163"></a><span data-ttu-id="54323-129">休暇と欠勤の両方としてマークされている場合に、理由コードに異なるシナリオのものが表示される (434163)</span><span class="sxs-lookup"><span data-stu-id="54323-129">Reason codes display across different scenarios when they're marked as Leave and absence and the streamlined employee form is enabled (434163)</span></span>

<span data-ttu-id="54323-130">この変更により、合理化された従業員入力を有効にすると、理由コードが休暇および欠勤コードのみに制限されます。</span><span class="sxs-lookup"><span data-stu-id="54323-130">This change restricts the reason codes to only Leave and absence codes when you enable streamlined employee entry.</span></span>

## <a name="the-preview-feature-assign-a-leave-plan-to-employees-in-the-future-displays-error-433555"></a><span data-ttu-id="54323-131">プレビュー機能で、従業員に未来日付の休暇を割り当てるとエラーが表示される (433555)</span><span class="sxs-lookup"><span data-stu-id="54323-131">The preview feature Assign a leave plan to employees in the future displays error (433555)</span></span>

<span data-ttu-id="54323-132">この変更により、休暇計画に2つの休暇タイプが割り当てられていて、従業員を割り当てようとした場合のエラーが修正されます。</span><span class="sxs-lookup"><span data-stu-id="54323-132">This change corrects an error when a leave plan has two leave types assigned and you attempt to assign an employee.</span></span>

## <a name="getting-started-banner-appears-for-all-users-441731"></a><span data-ttu-id="54323-133">全ユーザーに "はじめに" バナーが表示される (441731)</span><span class="sxs-lookup"><span data-stu-id="54323-133">Getting started banner appears for all users (441731)</span></span>

<span data-ttu-id="54323-134">この変更により、システム管理者やデータ管理者以外のユーザーに対して、[はじめに] のバナーが表示されなくなります。</span><span class="sxs-lookup"><span data-stu-id="54323-134">With this change, the Getting started banner is hidden for users that aren't System administrators or Data management administrators.</span></span> 

## <a name="the-common-data-service-worker-address-entity-works-differently-in-terms-of-date-time-effective-dates-in-human-resources-425071"></a><span data-ttu-id="54323-135">Common Data Service 作業者の住所エンティティの勤務時間の発効日が、Human Resources とは異なる (425071)</span><span class="sxs-lookup"><span data-stu-id="54323-135">The Common Data Service Worker Address entity works differently in terms of date time effective dates in Human Resources (425071)</span></span>

<span data-ttu-id="54323-136">この変更により、特定のシナリオでは、住所の日付に基づいて住所情報の整合性が保たれます。</span><span class="sxs-lookup"><span data-stu-id="54323-136">This change keeps address information aligned in certain scenarios, based on the dates of the address.</span></span>

## <a name="unable-to-add-an-attachment-to-an-approved-leave-request-425407"></a><span data-ttu-id="54323-137">承認済の休暇申請に添付ファイルを追加できない (425407)</span><span class="sxs-lookup"><span data-stu-id="54323-137">Unable to add an attachment to an approved leave request (425407)</span></span>

<span data-ttu-id="54323-138">今週のリリースでは、休暇申請を変更することなく、承認された休暇申請に添付ファイルを追加することができます。</span><span class="sxs-lookup"><span data-stu-id="54323-138">With this week's release, you can add attachments to approved leave requests without changing the leave request.</span></span>

## <a name="in-preview"></a><span data-ttu-id="54323-139">プレビュー</span><span class="sxs-lookup"><span data-stu-id="54323-139">In preview</span></span>

## <a name="leave-suspension"></a><span data-ttu-id="54323-140">休暇の停止</span><span class="sxs-lookup"><span data-stu-id="54323-140">Leave suspension</span></span>

<span data-ttu-id="54323-141">従業員に対し Human Resources で休暇および欠勤を中断できます。</span><span class="sxs-lookup"><span data-stu-id="54323-141">You can suspend leave and absence in Human Resources for an employee.</span></span> <span data-ttu-id="54323-142">休暇を中断すると、選択した休暇タイプの休暇の発生が停止します。</span><span class="sxs-lookup"><span data-stu-id="54323-142">Suspending leave stops the leave accruals for selected leave types.</span></span> <span data-ttu-id="54323-143">一時停止が見越計上プロセス後に発生した場合、休暇の一時停止により、従業員の休暇残日数が比例配分調整されます。</span><span class="sxs-lookup"><span data-stu-id="54323-143">If the suspension occurs after an accrual has been processed, suspending leave creates a prorated adjustment to the employee's leave balance.</span></span> <span data-ttu-id="54323-144">詳細については、[休暇の中断](hr-leave-and-absence-suspend-leave.md) を参照してください。</span><span class="sxs-lookup"><span data-stu-id="54323-144">For more information, see [Suspend leave](hr-leave-and-absence-suspend-leave.md).</span></span>

## <a name="update-user-experience-to-indicate-that-accrual-is-suspended-429550"></a><span data-ttu-id="54323-145">ユーザー エクスペリエンスを更新し、見越計上の中断が表示されるようになりました (429550)</span><span class="sxs-lookup"><span data-stu-id="54323-145">Update user experience to indicate that accrual is suspended (429550)</span></span>

<span data-ttu-id="54323-146">ユーザー エクスペリエンスは、計画に対して見越計上が中断されたことを示します。</span><span class="sxs-lookup"><span data-stu-id="54323-146">The user experience now indicates that the accrual has been suspended for a plan.</span></span>

## <a name="suspend-leave-accrual-for-specified-leave-types-272447"></a><span data-ttu-id="54323-147">指定した休暇タイプの休暇取得を一時停止する (272447)</span><span class="sxs-lookup"><span data-stu-id="54323-147">Suspend leave accrual for specified leave types (272447)</span></span>

<span data-ttu-id="54323-148">今回のリリースでは、人事部は無給休暇の休暇申請を入力した従業員に対して、休暇の発生を停止するルールを作成することができます。</span><span class="sxs-lookup"><span data-stu-id="54323-148">In this release, HR can create a rule to suspend leave accruals for employees with leave requests entered for unpaid leave.</span></span> <span data-ttu-id="54323-149">無給休暇のタイプを指定できますが、必須ではあります。</span><span class="sxs-lookup"><span data-stu-id="54323-149">Unpaid leave can be a type, but doesn't have to be.</span></span> <span data-ttu-id="54323-150">他の休暇種類に基づいて、任意の休暇を停止することができます。</span><span class="sxs-lookup"><span data-stu-id="54323-150">You can suspend any leave based on another leave type.</span></span>

## <a name="dmf-entity-available-for-accrual-suspensions-429549"></a><span data-ttu-id="54323-151">DMF エンティティが見越し計上の停止に使用可能 (429549)</span><span class="sxs-lookup"><span data-stu-id="54323-151">DMF entity available for accrual suspensions (429549)</span></span>

<span data-ttu-id="54323-152">DMF エンティティが見越し計上の停止に使用できるようになりました 。</span><span class="sxs-lookup"><span data-stu-id="54323-152">A DMF entity is now available for accrual suspensions.</span></span>

## <a name="add-reason-code-to-accrual-suspensions-429547"></a><span data-ttu-id="54323-153">見越計上の停止に理由コードが追加されました (429547)</span><span class="sxs-lookup"><span data-stu-id="54323-153">Add reason code to accrual suspensions (429547)</span></span>

<span data-ttu-id="54323-154">見越計上の中断に理由コードが追加されました。</span><span class="sxs-lookup"><span data-stu-id="54323-154">Reason codes have been added to the accrual suspension.</span></span>

## <a name="begin-transitioning-from-human-resources-parameters-to-leave-and-absence-parameters"></a><span data-ttu-id="54323-155">人事パラメータから休職,、欠勤パラメータへの移行を開始</span><span class="sxs-lookup"><span data-stu-id="54323-155">Begin transitioning from Human Resources parameters to leave and absence parameters</span></span>

<span data-ttu-id="54323-156">このリリースでは、人事管理パラメータと休暇・欠勤のパラメータの組み合わせに対応しています。</span><span class="sxs-lookup"><span data-stu-id="54323-156">This release starts to combine Human Resources parameters with Leave and absence parameters.</span></span>

## <a name="carry-forward-rules"></a><span data-ttu-id="54323-157">繰越ルール</span><span class="sxs-lookup"><span data-stu-id="54323-157">Carry forward rules</span></span>

<span data-ttu-id="54323-158">繰越調整を転送する繰越残日数に対して、繰越休暇タイプを指定できます。</span><span class="sxs-lookup"><span data-stu-id="54323-158">You can specify a carry forward leave type for carry forward balances where carry forward adjustments are transferred.</span></span> <span data-ttu-id="54323-159">たとえば、従業員が 10 日間繰り越す場合、その 10 日間に別の休暇タイプを選択できます。</span><span class="sxs-lookup"><span data-stu-id="54323-159">For example, if an employee carries forward 10 days, you can pick a different leave type for those 10 days.</span></span> <span data-ttu-id="54323-160">詳細については、[休暇および欠勤タイプのコンフィギュレーション](hr-leave-and-absence-types.md) を参照してください。</span><span class="sxs-lookup"><span data-stu-id="54323-160">For more information, see [Configure leave and absence types](hr-leave-and-absence-types.md).</span></span>

## <a name="see-also"></a><span data-ttu-id="54323-161">参照</span><span class="sxs-lookup"><span data-stu-id="54323-161">See also</span></span>

[<span data-ttu-id="54323-162">Human Resources の新機能および変更された機能</span><span class="sxs-lookup"><span data-stu-id="54323-162">What's new or changed in Human Resources</span></span>](hr-admin-whats-new.md)</br>
[<span data-ttu-id="54323-163">Dynamics 365 Human Resources 2019 のリリース ウェーブ 2 の概要</span><span class="sxs-lookup"><span data-stu-id="54323-163">Overview of Dynamics 365 Human Resources 2019 release wave 2</span></span>](https://docs.microsoft.com/dynamics365-release-plan/2019wave2/dynamics365-human-resources/)</br>
[<span data-ttu-id="54323-164">更新プロセス</span><span class="sxs-lookup"><span data-stu-id="54323-164">Update process</span></span>](hr-admin-setup-update-process.md)</br>
[<span data-ttu-id="54323-165">機能の管理</span><span class="sxs-lookup"><span data-stu-id="54323-165">Manage features</span></span>](hr-admin-manage-features.md)