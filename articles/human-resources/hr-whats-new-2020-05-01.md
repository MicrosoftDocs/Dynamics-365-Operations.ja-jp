---
title: Dynamics 365 Human Resources（2020 年 5 月 1 日）の新機能と変更された機能
description: この記事では、2020 年 5 月 1 日に更新された Microsoft Dynamics 365 Human Resources の新機能、または変更された機能について説明します。
author: andreabichsel
manager: tfehr
ms.date: 05/01/2020
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
ms.author: jaredha
ms.search.validFrom: 2020-05-01
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: 71fb3b6cb28abbd5d373103205c3360b7e64464e
ms.sourcegitcommit: 6affb3316be757c99e1fe9c7c7b312b93c483408
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 02/17/2021
ms.locfileid: "5465321"
---
# <a name="whats-new-or-changed-in-dynamics-365-human-resources-may-1-2020"></a><span data-ttu-id="ea23b-103">Dynamics 365 Human Resources（2020 年 5 月 1 日）の新機能と変更された機能</span><span class="sxs-lookup"><span data-stu-id="ea23b-103">What's new or changed in Dynamics 365 Human Resources (May 1, 2020)</span></span>

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

<span data-ttu-id="ea23b-104">この記事では、Dynamics 365 Human Resources の新機能および変更された機能について説明します。</span><span class="sxs-lookup"><span data-stu-id="ea23b-104">This article describes features that are either new or changed in Dynamics 365 Human Resources.</span></span> <span data-ttu-id="ea23b-105">変更は、ビルド番号 8.1.3196 に適用されます。</span><span class="sxs-lookup"><span data-stu-id="ea23b-105">Changes apply to build number 8.1.3196.</span></span> <span data-ttu-id="ea23b-106">ヘッダーにあるかっこ内の数字は、参照用の LCS のサポート番号を参照していることがあります。</span><span class="sxs-lookup"><span data-stu-id="ea23b-106">The numbers in parentheses in some headings refer to LCS support numbers for reference.</span></span>

## <a name="new-performance-management-entities-available-in-data-management-framework-dmf"></a><span data-ttu-id="ea23b-107">データ管理フレームワーク (DMF) で使用できる新しいパフォーマンス管理エンティティ</span><span class="sxs-lookup"><span data-stu-id="ea23b-107">New Performance Management entities available in Data Management Framework (DMF)</span></span>

<span data-ttu-id="ea23b-108">次のエンティティが利用可能になりました。</span><span class="sxs-lookup"><span data-stu-id="ea23b-108">The following entities are now available.</span></span> <span data-ttu-id="ea23b-109">エンティティ リストにこれらのエンティティが表示されない場合は、**フレームワーク パラメーター > エンティティ設定 > エンティティ リストの更新** の **エンティティの更新** オプションを使用します。</span><span class="sxs-lookup"><span data-stu-id="ea23b-109">If you don't see these entities listed in the entities list, use the **Refresh entities** option in **Framework Parameters > Entity settings > Refresh entity list**.</span></span>

- <span data-ttu-id="ea23b-110">**ディスカッションのコンピテンシー**</span><span class="sxs-lookup"><span data-stu-id="ea23b-110">**Discussion Competency**</span></span>
- <span data-ttu-id="ea23b-111">**ディスカッションの目標**</span><span class="sxs-lookup"><span data-stu-id="ea23b-111">**Discussion Goals**</span></span>
- <span data-ttu-id="ea23b-112">**ディスカッションの測定**</span><span class="sxs-lookup"><span data-stu-id="ea23b-112">**Discussion Measurement**</span></span>
- <span data-ttu-id="ea23b-113">**ディスカッションのトピック**</span><span class="sxs-lookup"><span data-stu-id="ea23b-113">**Discussion Topic**</span></span>
- <span data-ttu-id="ea23b-114">**業績履歴**</span><span class="sxs-lookup"><span data-stu-id="ea23b-114">**Performance Journal**</span></span>
- <span data-ttu-id="ea23b-115">**測定**</span><span class="sxs-lookup"><span data-stu-id="ea23b-115">**Measurement**</span></span>
- <span data-ttu-id="ea23b-116">**目標の測定**</span><span class="sxs-lookup"><span data-stu-id="ea23b-116">**Goal Measurement**</span></span>

<span data-ttu-id="ea23b-117">さらに、**合計スコア** と **平均スコア** が **ディスカッション** エンティティに追加されました。</span><span class="sxs-lookup"><span data-stu-id="ea23b-117">In addition, **Total score** and **Average score** were added to the **Discussion** entity.</span></span>

## <a name="increase-length-of-leave-request-comments-275641"></a><span data-ttu-id="ea23b-118">休暇要求のコメントの文字数の増加 (275641)</span><span class="sxs-lookup"><span data-stu-id="ea23b-118">Increase length of leave request comments (275641)</span></span>

<span data-ttu-id="ea23b-119">休暇に対するコメントで、100 文字を超えた入力が許可されます。</span><span class="sxs-lookup"><span data-stu-id="ea23b-119">Comments on leave requests now allow more than 100 characters.</span></span>

## <a name="final-comments-on-reviews-dont-appear-when-the-manager-or-employee-is-signed-into-a-different-company-431688"></a><span data-ttu-id="ea23b-120">マネージャーや従業員が別の会社にサイン インしている場合、レビューの最終コメントは表示されません (431688)</span><span class="sxs-lookup"><span data-stu-id="ea23b-120">Final comments on reviews don't appear when the manager or employee is signed into a different company (431688)</span></span>

<span data-ttu-id="ea23b-121">レビューを表示すると、すべてのコメントが表示されるようになります。</span><span class="sxs-lookup"><span data-stu-id="ea23b-121">All comments will now appear when viewing reviews.</span></span>

## <a name="user-defined-links-arent-supported-on-new-worker-form-390374"></a><span data-ttu-id="ea23b-122">新しい作業者フォームでユーザー定義のリンクに対応していない (390374)</span><span class="sxs-lookup"><span data-stu-id="ea23b-122">User-defined links aren't supported on new Worker form (390374)</span></span>

<span data-ttu-id="ea23b-123">合理化された **作業者** フォームで、ユーザー定義のリンクを有効にすることができます。</span><span class="sxs-lookup"><span data-stu-id="ea23b-123">User-defined links are now enabled on the streamlined **Worker** form.</span></span>

## <a name="hcmratinglevelentity-causes-odata-api-crash-439476"></a><span data-ttu-id="ea23b-124">HcmRatingLevelEntity により、OData API がクラッシュする (439476)</span><span class="sxs-lookup"><span data-stu-id="ea23b-124">HcmRatingLevelEntity causes OData API crash (439476)</span></span>

<span data-ttu-id="ea23b-125">この変更により、API のクラッシュが修正されます。</span><span class="sxs-lookup"><span data-stu-id="ea23b-125">This change corrects the API crash.</span></span> <span data-ttu-id="ea23b-126">重複した名称がこのエラーの原因となりました。</span><span class="sxs-lookup"><span data-stu-id="ea23b-126">A duplicate name cased this error.</span></span>

## <a name="in-preview"></a><span data-ttu-id="ea23b-127">プレビュー</span><span class="sxs-lookup"><span data-stu-id="ea23b-127">In preview</span></span>

## <a name="leave-suspension"></a><span data-ttu-id="ea23b-128">休暇の停止</span><span class="sxs-lookup"><span data-stu-id="ea23b-128">Leave suspension</span></span>

<span data-ttu-id="ea23b-129">従業員に対し Human Resources で休暇および欠勤を中断できます。</span><span class="sxs-lookup"><span data-stu-id="ea23b-129">You can suspend leave and absence in Human Resources for an employee.</span></span> <span data-ttu-id="ea23b-130">休暇を中断すると、選択した休暇タイプの休暇の発生が停止します。</span><span class="sxs-lookup"><span data-stu-id="ea23b-130">Suspending leave stops the leave accruals for selected leave types.</span></span> <span data-ttu-id="ea23b-131">一時停止が見越計上プロセス後に発生した場合、休暇の一時停止により、従業員の休暇残日数が比例配分調整されます。</span><span class="sxs-lookup"><span data-stu-id="ea23b-131">If the suspension occurs after an accrual has been processed, suspending leave creates a prorated adjustment to the employee's leave balance.</span></span> <span data-ttu-id="ea23b-132">詳細については、[休暇の中断](hr-leave-and-absence-suspend-leave.md) を参照してください。</span><span class="sxs-lookup"><span data-stu-id="ea23b-132">For more information, see [Suspend leave](hr-leave-and-absence-suspend-leave.md).</span></span>

## <a name="update-user-experience-to-indicate-that-accrual-is-suspended-429550"></a><span data-ttu-id="ea23b-133">ユーザー エクスペリエンスを更新し、見越計上の中断が表示されるようになりました (429550)</span><span class="sxs-lookup"><span data-stu-id="ea23b-133">Update user experience to indicate that accrual is suspended (429550)</span></span>

<span data-ttu-id="ea23b-134">ユーザー エクスペリエンスは、計画に対して見越計上が中断されたことを示します。</span><span class="sxs-lookup"><span data-stu-id="ea23b-134">The user experience now indicates that the accrual has been suspended for a plan.</span></span>

## <a name="suspend-leave-accrual-for-specified-leave-types-272447"></a><span data-ttu-id="ea23b-135">指定した休暇タイプの休暇取得を一時停止する (272447)</span><span class="sxs-lookup"><span data-stu-id="ea23b-135">Suspend leave accrual for specified leave types (272447)</span></span>

<span data-ttu-id="ea23b-136">今回のリリースでは、人事部は無給休暇の休暇申請を入力した従業員に対して、休暇の発生を停止するルールを作成することができます。</span><span class="sxs-lookup"><span data-stu-id="ea23b-136">In this release, HR can create a rule to suspend leave accruals for employees with leave requests entered for unpaid leave.</span></span> <span data-ttu-id="ea23b-137">無給休暇のタイプを指定できますが、必須ではあります。</span><span class="sxs-lookup"><span data-stu-id="ea23b-137">Unpaid leave can be a type, but doesn't have to be.</span></span> <span data-ttu-id="ea23b-138">他の休暇種類に基づいて、任意の休暇を停止することができます。</span><span class="sxs-lookup"><span data-stu-id="ea23b-138">You can suspend any leave based on another leave type.</span></span>

## <a name="dmf-entity-available-for-accrual-suspensions-429549"></a><span data-ttu-id="ea23b-139">DMF エンティティが見越し計上の停止に使用可能 (429549)</span><span class="sxs-lookup"><span data-stu-id="ea23b-139">DMF entity available for accrual suspensions (429549)</span></span>

<span data-ttu-id="ea23b-140">DMF エンティティが見越し計上の停止に使用できるようになりました 。</span><span class="sxs-lookup"><span data-stu-id="ea23b-140">A DMF entity is now available for accrual suspensions.</span></span>

## <a name="add-reason-code-to-accrual-suspensions-429547"></a><span data-ttu-id="ea23b-141">見越計上の停止に理由コードが追加されました (429547)</span><span class="sxs-lookup"><span data-stu-id="ea23b-141">Add reason code to accrual suspensions (429547)</span></span>

<span data-ttu-id="ea23b-142">見越計上の中断に理由コードが追加されました。</span><span class="sxs-lookup"><span data-stu-id="ea23b-142">Reason codes have been added to the accrual suspension.</span></span>

## <a name="begin-transitioning-from-human-resources-parameters-to-leave-and-absence-parameters"></a><span data-ttu-id="ea23b-143">人事パラメータから休職,、欠勤パラメータへの移行を開始</span><span class="sxs-lookup"><span data-stu-id="ea23b-143">Begin transitioning from Human Resources parameters to leave and absence parameters</span></span>

<span data-ttu-id="ea23b-144">このリリースでは、人事管理パラメータと休暇・欠勤のパラメータの組み合わせに対応しています。</span><span class="sxs-lookup"><span data-stu-id="ea23b-144">This release starts to combine Human Resources parameters with Leave and absence parameters.</span></span>

## <a name="carry-forward-rules"></a><span data-ttu-id="ea23b-145">繰越ルール</span><span class="sxs-lookup"><span data-stu-id="ea23b-145">Carry forward rules</span></span>

<span data-ttu-id="ea23b-146">繰越調整を転送する繰越残日数に対して、繰越休暇タイプを指定できます。</span><span class="sxs-lookup"><span data-stu-id="ea23b-146">You can specify a carry forward leave type for carry forward balances where carry forward adjustments are transferred.</span></span> <span data-ttu-id="ea23b-147">たとえば、従業員が 10 日間繰り越す場合、その 10 日間に別の休暇タイプを選択できます。</span><span class="sxs-lookup"><span data-stu-id="ea23b-147">For example, if an employee carries forward 10 days, you can pick a different leave type for those 10 days.</span></span> <span data-ttu-id="ea23b-148">詳細については、[休暇および欠勤タイプのコンフィギュレーション](hr-leave-and-absence-types.md) を参照してください。</span><span class="sxs-lookup"><span data-stu-id="ea23b-148">For more information, see [Configure leave and absence types](hr-leave-and-absence-types.md).</span></span>

## <a name="known-issues"></a><span data-ttu-id="ea23b-149">既知の問題</span><span class="sxs-lookup"><span data-stu-id="ea23b-149">Known issues</span></span>

## <a name="sharepoint-preview-doesnt-work-in-some-environments"></a><span data-ttu-id="ea23b-150">一部の環境で、SharePoint プレビューが機能しない</span><span class="sxs-lookup"><span data-stu-id="ea23b-150">SharePoint preview doesn't work in some environments</span></span>

<span data-ttu-id="ea23b-151">SharePoint で保存されているドキュメントのドキュメント プレビューが機能しない場合は、次の手順を実行します。</span><span class="sxs-lookup"><span data-stu-id="ea23b-151">If document preview for documents stored in SharePoint doesn't work, try the following procedure:</span></span>

1. <span data-ttu-id="ea23b-152">管理者のユーザー アカウントにユーザー レコードに関連付けられたメールがあることを確認します。</span><span class="sxs-lookup"><span data-stu-id="ea23b-152">Verify the Admin user account has an email associated with the user record.</span></span> <span data-ttu-id="ea23b-153">この情報は、**ユーザー** ページで確認できます。</span><span class="sxs-lookup"><span data-stu-id="ea23b-153">You can view this information in the **User** page.</span></span> <span data-ttu-id="ea23b-154">メールが設定されていない場合は、OData Excel アドインを使用してメールとプロバイダーを追加する必要があります。</span><span class="sxs-lookup"><span data-stu-id="ea23b-154">If email isn't set up, you need to add the email and provider with the OData Excel add-in.</span></span> <span data-ttu-id="ea23b-155">既定では、Excel デザインにメール アドレスは表示されません。</span><span class="sxs-lookup"><span data-stu-id="ea23b-155">By default, the email address isn't present in the Excel design.</span></span> <span data-ttu-id="ea23b-156">Excel デザインを編集し、すべてのフィールドを追加し、適用して更新する必要があります。</span><span class="sxs-lookup"><span data-stu-id="ea23b-156">You'll need to edit the Excel design, add all fields, apply, and refresh.</span></span> <span data-ttu-id="ea23b-157">これらのステップを完了すると、管理者アカウントを更新できます。</span><span class="sxs-lookup"><span data-stu-id="ea23b-157">Once you've completed those steps, you can update the admin account.</span></span>

2. <span data-ttu-id="ea23b-158">管理者アカウントにメール アカウントが関連付けられたら、人事管理に管理者としてサインインします。</span><span class="sxs-lookup"><span data-stu-id="ea23b-158">After the Admin account has an associated email account, sign in to Human Resources with Admin credentials.</span></span>

3. <span data-ttu-id="ea23b-159">SharePoint で添付ファイルにアクセスして、ドキュメントのプレビューを開始します。</span><span class="sxs-lookup"><span data-stu-id="ea23b-159">Access an attachment in SharePoint to start the document preview.</span></span>

4. <span data-ttu-id="ea23b-160">添付ファイルにアクセスできる他のユーザー アカウントでサインインし、適切にプレビューが機能することを確認します。</span><span class="sxs-lookup"><span data-stu-id="ea23b-160">Sign in with another user account that has access to attachments and verify that the preview works as expected.</span></span>

## <a name="see-also"></a><span data-ttu-id="ea23b-161">参照</span><span class="sxs-lookup"><span data-stu-id="ea23b-161">See also</span></span>

[<span data-ttu-id="ea23b-162">Human Resources の新機能および変更された機能</span><span class="sxs-lookup"><span data-stu-id="ea23b-162">What's new or changed in Human Resources</span></span>](hr-admin-whats-new.md)</br>
[<span data-ttu-id="ea23b-163">Dynamics 365 Human Resources 2019 のリリース ウェーブ 2 の概要</span><span class="sxs-lookup"><span data-stu-id="ea23b-163">Overview of Dynamics 365 Human Resources 2019 release wave 2</span></span>](https://docs.microsoft.com/dynamics365-release-plan/2019wave2/dynamics365-human-resources/)</br>
[<span data-ttu-id="ea23b-164">更新プロセス</span><span class="sxs-lookup"><span data-stu-id="ea23b-164">Update process</span></span>](hr-admin-setup-update-process.md)</br>
[<span data-ttu-id="ea23b-165">機能の管理</span><span class="sxs-lookup"><span data-stu-id="ea23b-165">Manage features</span></span>](hr-admin-manage-features.md)

[!INCLUDE[footer-include](../includes/footer-banner.md)]