---
title: Dynamics 365 Human Resources の新機能または変更された機能 (2020 年 4 月 13 日)
description: この記事では、Microsoft Dynamics 365 Human Resources の新機能または変更された機能について説明します。
author: Darinkramer
manager: AnnBe
ms.date: 4/13/2020
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
ms.search.validFrom: 2020-04-13
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: 711cc4491024e647429b108438ce1d88483ea63c
ms.sourcegitcommit: dbff1c6bb371a443a0cd2a310f5a48d5c21b08ca
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/13/2020
ms.locfileid: "3259820"
---
# <a name="whats-new-or-changed-in-dynamics-365-human-resources-april-13-2020"></a><span data-ttu-id="12321-103">Dynamics 365 Human Resources の新機能または変更された機能 (2020 年 4 月 13 日)</span><span class="sxs-lookup"><span data-stu-id="12321-103">What's new or changed in Dynamics 365 Human Resources (April 13, 2020)</span></span>

<span data-ttu-id="12321-104">この記事では、Dynamics 365 Human Resources の新機能および変更された機能について説明します。</span><span class="sxs-lookup"><span data-stu-id="12321-104">This article describes features that are either new or changed in Dynamics 365 Human Resources.</span></span> <span data-ttu-id="12321-105">変更は、ビルド番号 8.1.3136 に適用されます。</span><span class="sxs-lookup"><span data-stu-id="12321-105">Changes apply to build number 8.1.3136.</span></span> <span data-ttu-id="12321-106">ヘッダーにあるかっこ内の数字は、参照用の LCS のサポート番号を参照していることがあります。</span><span class="sxs-lookup"><span data-stu-id="12321-106">The numbers in parentheses in some headings refer to LCS support numbers for reference.</span></span>

## <a name="new-production-release-cadence"></a><span data-ttu-id="12321-107">新しい生産リリース リズム</span><span class="sxs-lookup"><span data-stu-id="12321-107">New production release cadence</span></span>

<span data-ttu-id="12321-108">今週のリリースでは、Human Resources のリリース頻度が毎週更新から隔週の更新に移行します。</span><span class="sxs-lookup"><span data-stu-id="12321-108">With this week's release, the release cadence for Human Resources shifts from a weekly update to a biweekly update.</span></span> <span data-ttu-id="12321-109">安全な展開プラクティスとの整合性を確保し、サービスの安定性と信頼性の高い標準を維持するために、すべての地域にサービス更新を展開するプロセスは 2 週間のロールアウトになります。</span><span class="sxs-lookup"><span data-stu-id="12321-109">To ensure alignment with safe deployment practices, and maintain high standards of stability and reliability in the service, the process of deploying service updates to all regions is now a two-week rollout.</span></span> <span data-ttu-id="12321-110">プロセスの各ステージで展開が成功したことを確認するために、追加のテストとモニターが実行されます。</span><span class="sxs-lookup"><span data-stu-id="12321-110">Additional testing and monitors are in place to verify successful deployment at each stage of the process.</span></span> <span data-ttu-id="12321-111">リリース頻度の詳細については、[更新プロセス](hr-admin-setup-update-process.md) を参照してください。</span><span class="sxs-lookup"><span data-stu-id="12321-111">For more information on the release cadence, see [Update process](hr-admin-setup-update-process.md).</span></span>

## <a name="rounding-precision-field-isnt-editable-after-specifying-a-rounding-type-435616"></a><span data-ttu-id="12321-112">丸めタイプを指定した後に丸め精度フィールドを編集できない (435616)</span><span class="sxs-lookup"><span data-stu-id="12321-112">Rounding precision field isn't editable after specifying a Rounding type (435616)</span></span>

<span data-ttu-id="12321-113">この変更により、**丸めタイプ** フィールドを更新した後に **丸め精度** フィールドが使用できるようになりました。</span><span class="sxs-lookup"><span data-stu-id="12321-113">With this change, the **Rounding precision** field is now available after you update the **Rounding type** field.</span></span>

## <a name="cant-edit-leave-enrollment-end-date-when-the-leave-plan-doesnt-have-accrual-periods-413628"></a><span data-ttu-id="12321-114">休暇計画に対して見越計上期間がない場合、休暇登録の終了日を編集できない (413628)</span><span class="sxs-lookup"><span data-stu-id="12321-114">Can't edit leave enrollment end date when the leave plan doesn't have accrual periods (413628)</span></span>

<span data-ttu-id="12321-115">"フィールド 見越計上日の基準を入力する必要があります" というエラーを発生させることなく、登録終了日を編集できるようになりました。</span><span class="sxs-lookup"><span data-stu-id="12321-115">You can now edit the enrollment end date without getting the error "Field Accrual date basis must be filled in."</span></span>

## <a name="employment-entity-doesnt-sync-to-common-data-service-430834"></a><span data-ttu-id="12321-116">雇用エンティティが Common Data Service に同期されない (430834)</span><span class="sxs-lookup"><span data-stu-id="12321-116">Employment entity doesn't sync to Common Data Service (430834)</span></span>

<span data-ttu-id="12321-117">この変更により、財務分析コードを追加した後、雇用データが Common Data Service に同期されなかった問題が修正されます。</span><span class="sxs-lookup"><span data-stu-id="12321-117">This change corrects an issue where the employment data wasn't syncing to Common Data Service after adding financial dimensions.</span></span> 

## <a name="remove-multi-parenting-for-work-calendar-time-interval-entity-431775"></a><span data-ttu-id="12321-118">作業カレンダー時間間隔エンティティのマルチ ペアレンティングの削除 (431775)</span><span class="sxs-lookup"><span data-stu-id="12321-118">Remove multi-parenting for Work Calendar Time Interval entity (431775)</span></span>

<span data-ttu-id="12321-119">この変更により、**作業カレンダー時間間隔** エンティティのマルチ ペアレンティングが削除されます。</span><span class="sxs-lookup"><span data-stu-id="12321-119">This change removes multi-parenting for the **Work Calendar Time Interval** entity.</span></span>

## <a name="filter-with-cast-function-doesnt-work-on-odata-call-position-worker-assignment-entity-431699"></a><span data-ttu-id="12321-120">CAST 関数を使用したフィルターは OData 呼び出し職位作業者割り当てエンティティでは機能しません (431699)</span><span class="sxs-lookup"><span data-stu-id="12321-120">Filter with CAST function doesn't work on OData call Position Worker Assignment entity (431699)</span></span>

<span data-ttu-id="12321-121">この更新には、**職位作業者割り当て** エンティティに対して OData 内で CAST 関数を使用したフィルターを許可する変更が含まれています。</span><span class="sxs-lookup"><span data-stu-id="12321-121">This update includes a change to allow  filter with CAST function within OData for the **Position Worker Assignment** entity.</span></span>

## <a name="in-preview"></a><span data-ttu-id="12321-122">プレビュー</span><span class="sxs-lookup"><span data-stu-id="12321-122">In Preview</span></span>

## <a name="leave-suspension"></a><span data-ttu-id="12321-123">休暇の停止</span><span class="sxs-lookup"><span data-stu-id="12321-123">Leave suspension</span></span>

<span data-ttu-id="12321-124">従業員に対し Human Resources で休暇および欠勤を中断できます。</span><span class="sxs-lookup"><span data-stu-id="12321-124">You can suspend leave and absence in Human Resources for an employee.</span></span> <span data-ttu-id="12321-125">休暇を中断すると、選択した休暇タイプの休暇の発生が停止します。</span><span class="sxs-lookup"><span data-stu-id="12321-125">Suspending leave stops the leave accruals for selected leave types.</span></span> <span data-ttu-id="12321-126">一時停止が見越計上プロセス後に発生した場合、休暇の一時停止により、従業員の休暇残日数が比例配分調整されます。</span><span class="sxs-lookup"><span data-stu-id="12321-126">If the suspension occurs after an accrual has been processed, suspending leave creates a prorated adjustment to the employee's leave balance.</span></span> <span data-ttu-id="12321-127">詳細については、[休暇の中断](hr-leave-and-absence-suspend-leave.md) を参照してください。</span><span class="sxs-lookup"><span data-stu-id="12321-127">For more information, see [Suspend leave](hr-leave-and-absence-suspend-leave.md).</span></span>

## <a name="carry-forward-rules"></a><span data-ttu-id="12321-128">繰越ルール</span><span class="sxs-lookup"><span data-stu-id="12321-128">Carry forward rules</span></span>

<span data-ttu-id="12321-129">繰越調整を転送する繰越残日数に対して、繰越休暇タイプを指定できます。</span><span class="sxs-lookup"><span data-stu-id="12321-129">You can specify a carry forward leave type for carry forward balances where carry forward adjustments are transferred.</span></span> <span data-ttu-id="12321-130">たとえば、従業員が 10 日間繰り越す場合、その 10 日間に別の休暇タイプを選択できます。</span><span class="sxs-lookup"><span data-stu-id="12321-130">For example, if an employee carries forward 10 days, you can pick a different leave type for those 10 days.</span></span> <span data-ttu-id="12321-131">詳細については、[休暇および欠勤タイプのコンフィギュレーション](hr-leave-and-absence-types.md) を参照してください。</span><span class="sxs-lookup"><span data-stu-id="12321-131">For more information, see [Configure leave and absence types](hr-leave-and-absence-types.md).</span></span>

## <a name="known-issues"></a><span data-ttu-id="12321-132">既知の問題</span><span class="sxs-lookup"><span data-stu-id="12321-132">Known issues</span></span>

## <a name="employment-details-entity"></a><span data-ttu-id="12321-133">雇用の詳細エンティティ</span><span class="sxs-lookup"><span data-stu-id="12321-133">Employment Details entity</span></span>

<span data-ttu-id="12321-134">**雇用の詳細** エンティティが次のフィールドで更新されました:</span><span class="sxs-lookup"><span data-stu-id="12321-134">The **Employment Detail** entity has been updated with the following fields:</span></span>

- <span data-ttu-id="12321-135">**PayFrequency**</span><span class="sxs-lookup"><span data-stu-id="12321-135">**PayFrequency**</span></span>
- <span data-ttu-id="12321-136">**雇用カテゴリ ID**</span><span class="sxs-lookup"><span data-stu-id="12321-136">**Employment Category ID**</span></span>
- <span data-ttu-id="12321-137">**雇用タイプ**</span><span class="sxs-lookup"><span data-stu-id="12321-137">**Employment Type**</span></span>
- <span data-ttu-id="12321-138">**EmploymentType ID**</span><span class="sxs-lookup"><span data-stu-id="12321-138">**EmploymentType ID**</span></span>
- <span data-ttu-id="12321-139">**福利厚生の雇用状況**</span><span class="sxs-lookup"><span data-stu-id="12321-139">**Benefit Employment Status**</span></span>

<span data-ttu-id="12321-140">これらのフィールドの設定データは、**機能管理** ワークスペースで有効になっている福利厚生の管理に依存します。</span><span class="sxs-lookup"><span data-stu-id="12321-140">The setup data for these fields rely on benefits management being enabled in the **Feature management** workspace.</span></span> <span data-ttu-id="12321-141">インポート中にエラーが発生するため、**雇用の詳細** エンティティのこれらのフィールドを入力または更新しないでください。</span><span class="sxs-lookup"><span data-stu-id="12321-141">Don't populate or update these fields in the **Employment Detail** entity, because it will result in errors during import.</span></span>

## <a name="sharepoint-preview-doesnt-work-in-some-environments"></a><span data-ttu-id="12321-142">一部の環境で、SharePoint プレビューが機能しない</span><span class="sxs-lookup"><span data-stu-id="12321-142">SharePoint preview doesn't work in some environments</span></span>

<span data-ttu-id="12321-143">SharePoint で保存されているドキュメントのドキュメント プレビューが機能しない場合は、次の手順を実行します。</span><span class="sxs-lookup"><span data-stu-id="12321-143">If document preview for documents stored in SharePoint doesn't work, try the following procedure:</span></span>

1. <span data-ttu-id="12321-144">管理者のユーザー アカウントにユーザー レコードに関連付けられたメールがあることを確認します。</span><span class="sxs-lookup"><span data-stu-id="12321-144">Verify the Admin user account has an email associated with the user record.</span></span> <span data-ttu-id="12321-145">この情報は、**ユーザー** ページで確認できます。</span><span class="sxs-lookup"><span data-stu-id="12321-145">You can view this information in the **User** page.</span></span> <span data-ttu-id="12321-146">メールが設定されていない場合は、OData Excel アドインを使用してメールとプロバイダーを追加する必要があります。</span><span class="sxs-lookup"><span data-stu-id="12321-146">If email isn't set up, you need to add the email and provider with the OData Excel add-in.</span></span> <span data-ttu-id="12321-147">既定では、Excel デザインにメール アドレスは表示されません。</span><span class="sxs-lookup"><span data-stu-id="12321-147">By default, the email address isn't present in the Excel design.</span></span> <span data-ttu-id="12321-148">Excel デザインを編集し、すべてのフィールドを追加し、適用して更新する必要があります。</span><span class="sxs-lookup"><span data-stu-id="12321-148">You'll need to edit the Excel design, add all fields, apply, and refresh.</span></span> <span data-ttu-id="12321-149">これらのステップを完了すると、管理者アカウントを更新できます。</span><span class="sxs-lookup"><span data-stu-id="12321-149">Once you've completed those steps, you can update the admin account.</span></span>

2. <span data-ttu-id="12321-150">管理者アカウントにメール アカウントが関連付けられたら、人事管理に管理者としてサインインします。</span><span class="sxs-lookup"><span data-stu-id="12321-150">After the Admin account has an associated email account, sign in to Human Resources with Admin credentials.</span></span>

3. <span data-ttu-id="12321-151">SharePoint で添付ファイルにアクセスして、ドキュメントのプレビューを開始します。</span><span class="sxs-lookup"><span data-stu-id="12321-151">Access an attachment in SharePoint to start the document preview.</span></span>

4. <span data-ttu-id="12321-152">添付ファイルにアクセスできる他のユーザー アカウントでサインインし、適切にプレビューが機能することを確認します。</span><span class="sxs-lookup"><span data-stu-id="12321-152">Sign in with another user account that has access to attachments and verify that the preview works as expected.</span></span>
