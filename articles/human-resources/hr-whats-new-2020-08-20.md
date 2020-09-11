---
title: Dynamics 365 Human Resources の新機能、または変更された機能 (2020 年 8 月 20 日)
description: このトピックでは、2020 年 8 月 20 日に更新された、Microsoft Dynamics 365 Human Resources の新機能、または変更された機能について説明します。
author: Darinkramer
manager: AnnBe
ms.date: 8/20/2020
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
ms.search.validFrom: 2020-08-20
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: 11a1f166080b96760cb10f4d0cdc627979c2709e
ms.sourcegitcommit: e0bf7a81ead351f5b109061c401589295058f808
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 08/26/2020
ms.locfileid: "3726310"
---
# <a name="whats-new-or-changed-in-dynamics-365-human-resources-august-20-2020"></a><span data-ttu-id="7aac9-103">Dynamics 365 Human Resources の新機能、または変更された機能 (2020 年 8 月 20 日)</span><span class="sxs-lookup"><span data-stu-id="7aac9-103">What's new or changed in Dynamics 365 Human Resources (August 20, 2020)</span></span>

<span data-ttu-id="7aac9-104">このトピックでは、Dynamics 365 Human Resources の新機能または変更された機能について説明します。</span><span class="sxs-lookup"><span data-stu-id="7aac9-104">This topic describes features that are either new or changed in Dynamics 365 Human Resources.</span></span> <span data-ttu-id="7aac9-105">変更は、ビルド番号 8.1.3478 に適用されます。</span><span class="sxs-lookup"><span data-stu-id="7aac9-105">Changes apply to build number 8.1.3478.</span></span> <span data-ttu-id="7aac9-106">一部のヘッダーにあるかっこ内の数字は、参照用に Lifecycle Services (LCS) のサポート番号を参照しています。</span><span class="sxs-lookup"><span data-stu-id="7aac9-106">The numbers in parentheses in some headings refer to Lifecycle Services (LCS) support numbers for reference.</span></span>

## <a name="show-upcoming-and-pending-leave-of-absence-information-to-cards-in-people-workspace"></a><span data-ttu-id="7aac9-107">休暇の予定と保留中の休暇情報を、プープル ワークスペースのカードに表示する</span><span class="sxs-lookup"><span data-stu-id="7aac9-107">Show upcoming and pending leave of absence information to cards in People workspace</span></span>

<span data-ttu-id="7aac9-108">**ピープル** ワークスペースの休暇カードと欠勤カードで、休暇の予定と保留中の休暇申請オプションが使用できるようになりました。</span><span class="sxs-lookup"><span data-stu-id="7aac9-108">Pending and upcoming leave request options are now available on the Leave and absence cards in the **People** workspace.</span></span>

## <a name="private-field-isnt-yes-by-default-for-employee-role-in-employee-self-service-477106"></a><span data-ttu-id="7aac9-109">従業員セルフサービスの従業員ロールの場合、プライベート フィールドは既定で [はい] になっていません (477106)</span><span class="sxs-lookup"><span data-stu-id="7aac9-109">Private field isn't Yes by default for Employee role in Employee self service (477106)</span></span>

<span data-ttu-id="7aac9-110">従業員が従業員セルフサービスの **個人情報** ページを使用して新しい住所レコードを追加すると、**プライベート フィールド**の既定値が**はい**になります。</span><span class="sxs-lookup"><span data-stu-id="7aac9-110">The **Private** field now defaults to **Yes** when employees add new address records through the **Personal information** page in Employee self service.</span></span> 

## <a name="candidates-to-hire-fasttab-in-personnel-management-shows-an-incorrect-count-of-candidates-470110"></a><span data-ttu-id="7aac9-111">従業員管理の採用候補クイックタブで、表示される候補の数が誤って表示される (470110)</span><span class="sxs-lookup"><span data-stu-id="7aac9-111">Candidates to hire FastTab in Personnel management shows an incorrect count of candidates (470110)</span></span>

<span data-ttu-id="7aac9-112">**人事管理** ページで、採用候補者の数を正確に表示するようになりました。</span><span class="sxs-lookup"><span data-stu-id="7aac9-112">The **Personnel management** page now accurately displays the number of candidates to hire.</span></span> 

## <a name="cant-enter-sickness-for-terminated-employee-when-accrual-is-set-to-zero-446195"></a><span data-ttu-id="7aac9-113">見越計上がゼロに設定されていると、退職した従業員の病欠を入力できない (446195)</span><span class="sxs-lookup"><span data-stu-id="7aac9-113">Can’t enter sickness for terminated employee when accrual is set to zero (446195)</span></span>

<span data-ttu-id="7aac9-114">休暇トランザクションは、将来的に退職する従業員に対しても認められるようになりましたが、見越計上はゼロに設定されます。</span><span class="sxs-lookup"><span data-stu-id="7aac9-114">Leave transactions are now allowed for employees that have been terminated in the future and the accrual is set to zero.</span></span> <span data-ttu-id="7aac9-115">休暇トランザクションは、従業員の退職日まで入力可能です。</span><span class="sxs-lookup"><span data-stu-id="7aac9-115">Leave transactions can be entered up to the termination date of the employee.</span></span> 

## <a name="adding-custom-fields-to-the-new-worker-form-disables-the-fields-in-the-action-pane-for-manage-leave-473314"></a><span data-ttu-id="7aac9-116">新しい作業者のフォームにカスタム フィールドを追加すると、休暇管理のアクション ペインのフィールドが無効になる (473314)</span><span class="sxs-lookup"><span data-stu-id="7aac9-116">Adding custom fields to the new Worker form disables the fields in the action pane for Manage leave (473314)</span></span>

<span data-ttu-id="7aac9-117">新しい**作業者** フォームにカスタム フィールドが追加されている場合は、**休暇管理**の新規**作業者**フォーム上のアクション ペインのオプションは無効化されます。</span><span class="sxs-lookup"><span data-stu-id="7aac9-117">Action pane options on the new **Worker** form in **Manage leave** will no longer be disabled if custom fields have been added to the new **Worker** form.</span></span>

## <a name="making-the-leave-comment-field-mandatory-allows-a-leave-request-to-be-submitted-when-no-comment-is-entered-473543"></a><span data-ttu-id="7aac9-118">休暇のコメント フィールドを必須にしても、コメントが未入力のままで休暇申請ができてしまう (473543)</span><span class="sxs-lookup"><span data-stu-id="7aac9-118">Making the Leave comment field mandatory allows a leave request to be submitted when no comment is entered (473543)</span></span>

<span data-ttu-id="7aac9-119">コメント フィールドは必須になり、休暇の申請時にはこの設定に従うようになりました。</span><span class="sxs-lookup"><span data-stu-id="7aac9-119">Comment fields can now be mandatory, and leave requests honor this setting.</span></span> <span data-ttu-id="7aac9-120">必須フィールドはプレビュー機能です。</span><span class="sxs-lookup"><span data-stu-id="7aac9-120">Mandatory fields is a preview feature.</span></span>

### <a name="dmf-entity-available-for-accrual-suspensions"></a><span data-ttu-id="7aac9-121">DMF エンティティで休暇付与の一時停止が可能</span><span class="sxs-lookup"><span data-stu-id="7aac9-121">DMF entity available for accrual suspensions</span></span>

<span data-ttu-id="7aac9-122">DMF エンティティが見越し計上の停止に使用できるようになりました 。</span><span class="sxs-lookup"><span data-stu-id="7aac9-122">A DMF entity is now available for accrual suspensions.</span></span>

## <a name="in-preview"></a><span data-ttu-id="7aac9-123">プレビュー</span><span class="sxs-lookup"><span data-stu-id="7aac9-123">In preview</span></span>

### <a name="mandatory-fields"></a><span data-ttu-id="7aac9-124">必須項目</span><span class="sxs-lookup"><span data-stu-id="7aac9-124">Mandatory fields</span></span>

<span data-ttu-id="7aac9-125">人事管理のパーソナル化機能を使用することにより、フィールドを必須にすることができます。</span><span class="sxs-lookup"><span data-stu-id="7aac9-125">You can make fields mandatory by using Human Resources personalization capabilities.</span></span> <span data-ttu-id="7aac9-126">この機能には**保存されたビュー**が必要です。</span><span class="sxs-lookup"><span data-stu-id="7aac9-126">This feature requires **Saved views**.</span></span> <span data-ttu-id="7aac9-127">保存されたビューに関する詳細については、次を参照してください。</span><span class="sxs-lookup"><span data-stu-id="7aac9-127">For more information about saved views, see:</span></span>

- <span data-ttu-id="7aac9-128">[保存ビュー - Dynamics 365 2020 リリース ウェーブ 2 プランの一般提供](https://docs.microsoft.com/dynamics365-release-plan/2020wave2/finance-operations/finance-operations-crossapp-capabilities/saved-views--general-availability) </span><span class="sxs-lookup"><span data-stu-id="7aac9-128">[Saved views - general availability](https://docs.microsoft.com/dynamics365-release-plan/2020wave2/finance-operations/finance-operations-crossapp-capabilities/saved-views--general-availability) in the Dynamics 365 2020 release wave 2 plan</span></span>
- [<span data-ttu-id="7aac9-129">保存されたビューを十分に活用するフォームの作成</span><span class="sxs-lookup"><span data-stu-id="7aac9-129">Build forms that fully utilize saved views</span></span>](https://docs.microsoft.com/dynamics365/fin-ops-core/dev-itpro/user-interface/understanding-saved-views)

### <a name="human-resources-application-in-teams"></a><span data-ttu-id="7aac9-130">Teams の Human Resources アプリケーション</span><span class="sxs-lookup"><span data-stu-id="7aac9-130">Human Resources application in Teams</span></span>

<span data-ttu-id="7aac9-131">従業員は、Microsoft Teams 内で休暇の表示および申請ができます。</span><span class="sxs-lookup"><span data-stu-id="7aac9-131">Employees can view and request time away from work within Microsoft Teams.</span></span> <span data-ttu-id="7aac9-132">ボットと対話して、休暇申請を作成できます。</span><span class="sxs-lookup"><span data-stu-id="7aac9-132">They can interact with a bot to create leave requests.</span></span> <span data-ttu-id="7aac9-133">詳細については、以下を参照してください。</span><span class="sxs-lookup"><span data-stu-id="7aac9-133">For more information, see:</span></span>

- <span data-ttu-id="7aac9-134">Dynamics 365 2020 リリース ウェーブ 1 プランでの [Microsoft Teams の従業員の休暇および欠勤体験](https://docs.microsoft.com/dynamics365-release-plan/2020wave1/dynamics365-human-resources/employee-leave-absence-experience-teams)</span><span class="sxs-lookup"><span data-stu-id="7aac9-134">[Employee leave and absence experience in Microsoft Teams](https://docs.microsoft.com/dynamics365-release-plan/2020wave1/dynamics365-human-resources/employee-leave-absence-experience-teams) in the Dynamics 365 2020 release wave 1 plan</span></span>
- [<span data-ttu-id="7aac9-135">Teams の Human Resources アプリ</span><span class="sxs-lookup"><span data-stu-id="7aac9-135">Human Resources app in Teams</span></span>](https://go.microsoft.com/fwlink/?linkid=2127841)

## <a name="coming-soon"></a><span data-ttu-id="7aac9-136">間もなく公開</span><span class="sxs-lookup"><span data-stu-id="7aac9-136">Coming soon</span></span>

### <a name="human-resources-app-in-teams-preview-features"></a><span data-ttu-id="7aac9-137">Teams の Human Resources アプリにおけるプレビュー機能</span><span class="sxs-lookup"><span data-stu-id="7aac9-137">Human Resources app in Teams preview features</span></span>
 
-  <span data-ttu-id="7aac9-138">**通知** : 休暇申請の提出者と承認者は、Teams の人事アプリで通知されます。</span><span class="sxs-lookup"><span data-stu-id="7aac9-138">**Notifications**: Submitters and approvers of time-off requests will be notified in the Human Resources app in Teams.</span></span> <span data-ttu-id="7aac9-139">承認者は休暇申請を承認、または拒否することができ、申請が承認または拒否された場合は送信者に通知されます。</span><span class="sxs-lookup"><span data-stu-id="7aac9-139">Approvers will be able to approve or deny time-off requests, and submitters will be notified if the request was approved or denied.</span></span>
 
- <span data-ttu-id="7aac9-140">**マネージャーの休暇カレンダー** : マネージャーは、直属の部下の承認済み休暇、および保留中の休暇をカレンダーで確認することができます。</span><span class="sxs-lookup"><span data-stu-id="7aac9-140">**Manager time-off calendar**: Managers will be able to see approved and pending time off for their direct reports in a calendar view.</span></span> <span data-ttu-id="7aac9-141">このビューを使用すると、チームのメンバーの休暇を簡単に把握することができます。</span><span class="sxs-lookup"><span data-stu-id="7aac9-141">This view provides an easy understanding of when their team members are away from work.</span></span>

### <a name="checklist-entities-included-in-common-data-service"></a><span data-ttu-id="7aac9-142">Common Data Service に含まれるチェックリスト エンティティ</span><span class="sxs-lookup"><span data-stu-id="7aac9-142">Checklist entities included in Common Data Service</span></span>

<span data-ttu-id="7aac9-143">オンボード、オフボード、転送、および業務プロセスのチェックリスト エンティティは、Common Data Service ですぐに使用可能になります。</span><span class="sxs-lookup"><span data-stu-id="7aac9-143">Checklist entities for Onboarding, Offboarding, Transfers, and Business processes will be available soon in Common Data Service.</span></span>

## <a name="known-issues"></a><span data-ttu-id="7aac9-144">既知の問題</span><span class="sxs-lookup"><span data-stu-id="7aac9-144">Known issues</span></span>

<span data-ttu-id="7aac9-145">**機能管理** ワークスペースには、通常使用可能な場合にプレビュー機能として無効になっている機能が表示される場合があります。</span><span class="sxs-lookup"><span data-stu-id="7aac9-145">The **Feature management** workspace may be displaying features that are disabled as preview features when they are generally available.</span></span> <span data-ttu-id="7aac9-146">正しくないステータスを示す一般的な機能を以下に示します。</span><span class="sxs-lookup"><span data-stu-id="7aac9-146">Below is a list of generally available features that show an incorrect status.</span></span> 

- <span data-ttu-id="7aac9-147">給付金管理</span><span class="sxs-lookup"><span data-stu-id="7aac9-147">Benefits management</span></span>
- <span data-ttu-id="7aac9-148">ケース管理</span><span class="sxs-lookup"><span data-stu-id="7aac9-148">Case management</span></span>
- <span data-ttu-id="7aac9-149">データベースのログ記録 (監査)</span><span class="sxs-lookup"><span data-stu-id="7aac9-149">Database logging (Auditing)</span></span>
- <span data-ttu-id="7aac9-150">1 つの会社または 1 つの計画の休暇の見越計上</span><span class="sxs-lookup"><span data-stu-id="7aac9-150">Leave accrual for a single company or a single plan</span></span>
- <span data-ttu-id="7aac9-151">休暇の見越計上の中断</span><span class="sxs-lookup"><span data-stu-id="7aac9-151">Leave and absence accrual suspension</span></span>
- <span data-ttu-id="7aac9-152">残高調整の理由コードとコメント</span><span class="sxs-lookup"><span data-stu-id="7aac9-152">Balance adjustment reason code and comment</span></span>
- <span data-ttu-id="7aac9-153">休暇の売買</span><span class="sxs-lookup"><span data-stu-id="7aac9-153">Buy and sell leave</span></span>
- <span data-ttu-id="7aac9-154">休暇および欠勤カレンダー</span><span class="sxs-lookup"><span data-stu-id="7aac9-154">Leave and absence calendar</span></span>
- <span data-ttu-id="7aac9-155">休暇繰越ルール</span><span class="sxs-lookup"><span data-stu-id="7aac9-155">Leave carry-forward rules</span></span>
- <span data-ttu-id="7aac9-156">休暇の見越計上の監査</span><span class="sxs-lookup"><span data-stu-id="7aac9-156">Leave accrual auditing</span></span>
- <span data-ttu-id="7aac9-157">休暇の見越計上の削除</span><span class="sxs-lookup"><span data-stu-id="7aac9-157">Leave accrual deletion</span></span>
- <span data-ttu-id="7aac9-158">休暇の見越計上の丸め</span><span class="sxs-lookup"><span data-stu-id="7aac9-158">Leave accrual rounding</span></span>
- <span data-ttu-id="7aac9-159">1 つの休暇計画で複数の休暇タイプを構成</span><span class="sxs-lookup"><span data-stu-id="7aac9-159">Configure multiple leave types on a single leave plan</span></span>
- <span data-ttu-id="7aac9-160">短期休暇の更新</span><span class="sxs-lookup"><span data-stu-id="7aac9-160">Update time-off enhancements</span></span>
- <span data-ttu-id="7aac9-161">見越計上に従業員の FTE を使用する</span><span class="sxs-lookup"><span data-stu-id="7aac9-161">Use an employee's FTE for accruals</span></span>
- <span data-ttu-id="7aac9-162">会社間報酬ビュー</span><span class="sxs-lookup"><span data-stu-id="7aac9-162">Cross company compensation view</span></span>
- <span data-ttu-id="7aac9-163">業績の確認の印刷</span><span class="sxs-lookup"><span data-stu-id="7aac9-163">Print performance reviews</span></span>
- <span data-ttu-id="7aac9-164">休暇の見越計上における休日の修正</span><span class="sxs-lookup"><span data-stu-id="7aac9-164">Leave accrual holiday corrections</span></span>

### <a name="benefit-plan-employee-entity"></a><span data-ttu-id="7aac9-165">福利厚生プランの従業員エンティティ</span><span class="sxs-lookup"><span data-stu-id="7aac9-165">Benefit plan employee entity</span></span> 

<span data-ttu-id="7aac9-166">**BenefitsPlanEmployee** エンティティに関する2つの問題が発見されました。</span><span class="sxs-lookup"><span data-stu-id="7aac9-166">We have recently discovered two issues regarding the **BenefitsPlanEmployee** entity.</span></span> <span data-ttu-id="7aac9-167">作業者の登録をインポートする際に、**補充コード**と **計画タイプ コード**が正しく設定されません。</span><span class="sxs-lookup"><span data-stu-id="7aac9-167">When importing worker enrollments, the **Coverage code** and the **Plan type code** are being set incorrectly.</span></span> <span data-ttu-id="7aac9-168">この問題が発生すると、従業員の福利厚生プランが **作業者の福利厚生プラン**フォームと、従業員セルフサービスの**オープン登録**フォームに正しく表示されません。</span><span class="sxs-lookup"><span data-stu-id="7aac9-168">This issue causes employee benefit plans to display incorrectly in the **Worker benefits plan** form and in the **Open enrollment** form in Employee self service.</span></span> <span data-ttu-id="7aac9-169">この問題は、従業員セルフ サービスでプランを選択する機能にも影響します。</span><span class="sxs-lookup"><span data-stu-id="7aac9-169">This issue can also impact the employee's ability to select plans in Employee self service.</span></span> <span data-ttu-id="7aac9-170">現時点では回避策はありません。</span><span class="sxs-lookup"><span data-stu-id="7aac9-170">Currently there isn't a workaround.</span></span> <span data-ttu-id="7aac9-171">この問題については優先度を挙げて取り組み、次のリリースで修正を展開していきます。</span><span class="sxs-lookup"><span data-stu-id="7aac9-171">We're treating this as a high-priority fix and will roll out the fix with our next release.</span></span>

## <a name="see-also"></a><span data-ttu-id="7aac9-172">参照</span><span class="sxs-lookup"><span data-stu-id="7aac9-172">See also</span></span>

[<span data-ttu-id="7aac9-173">Human Resources の新機能および変更された機能</span><span class="sxs-lookup"><span data-stu-id="7aac9-173">What's new or changed in Human Resources</span></span>](hr-admin-whats-new.md)</br>
[<span data-ttu-id="7aac9-174">Dynamics 365 Human Resources 2019 のリリース ウェーブ 2 の概要</span><span class="sxs-lookup"><span data-stu-id="7aac9-174">Overview of Dynamics 365 Human Resources 2019 release wave 2</span></span>](https://docs.microsoft.com/dynamics365-release-plan/2019wave2/dynamics365-human-resources/)</br>
[<span data-ttu-id="7aac9-175">更新プロセス</span><span class="sxs-lookup"><span data-stu-id="7aac9-175">Update process</span></span>](hr-admin-setup-update-process.md)</br>
[<span data-ttu-id="7aac9-176">機能の管理</span><span class="sxs-lookup"><span data-stu-id="7aac9-176">Manage features</span></span>](hr-admin-manage-features.md)
