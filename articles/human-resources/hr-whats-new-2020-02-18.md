---
title: Dynamics 365 Human Resources の新機能および変更された機能 (2020 年 2 月 18 日)
description: この記事では、2020 年 2 月 18 日に更新された Microsoft Dynamics 365 Human Resources の新機能、または変更された機能について説明します。
author: andreabichsel
manager: tfehr
ms.date: 02/18/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-human-resources
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Human Resources
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: jaredha
ms.search.validFrom: 2020-02-18
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: 66ffd9d0ffcf0e8466be785274ef5fb0fceda7a9
ms.sourcegitcommit: 6affb3316be757c99e1fe9c7c7b312b93c483408
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 02/17/2021
ms.locfileid: "5463793"
---
# <a name="whats-new-or-changed-in-dynamics-365-human-resources-february-18-2020"></a><span data-ttu-id="01b79-103">Dynamics 365 Human Resources の新機能および変更された機能 (2020 年 2 月 18 日)</span><span class="sxs-lookup"><span data-stu-id="01b79-103">What's new or changed in Dynamics 365 Human Resources (February 18, 2020)</span></span>

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

[!include [rename-banner](~/includes/cc-data-platform-banner.md)]

<span data-ttu-id="01b79-104">この記事では、Dynamics 365 Human Resources の新機能および変更された機能について説明します。</span><span class="sxs-lookup"><span data-stu-id="01b79-104">This article describes features that are either new or changed in Dynamics 365 Human Resources.</span></span> <span data-ttu-id="01b79-105">変更は、ビルド番号 8.1.2903 に適用されます。</span><span class="sxs-lookup"><span data-stu-id="01b79-105">Changes apply to build number 8.1.2903.</span></span> <span data-ttu-id="01b79-106">ヘッダーにあるかっこ内の数字は、参照用の LCS のサポート番号を参照していることがあります。</span><span class="sxs-lookup"><span data-stu-id="01b79-106">The numbers in parentheses in some headings refer to LCS support numbers for reference.</span></span>

## <a name="platform-update-32"></a><span data-ttu-id="01b79-107">プラットフォーム update 32</span><span class="sxs-lookup"><span data-stu-id="01b79-107">Platform update 32</span></span> 

<span data-ttu-id="01b79-108">プラットフォーム更新プログラム 32 が使用できるようになりました。</span><span class="sxs-lookup"><span data-stu-id="01b79-108">Platform update 32 is now available.</span></span> <span data-ttu-id="01b79-109">詳細については、[Finance and Operations アプリのプラットフォーム更新プログラム 32 (2020 年 2 月) の新機能および変更された機能](https://docs.microsoft.com/dynamics365/fin-ops-core/dev-itpro/get-started/whats-new-platform-update-32) を参照してください。</span><span class="sxs-lookup"><span data-stu-id="01b79-109">For more information, see [What's new or changed in Platform update 32 for Finance and Operations (February 2020)](https://docs.microsoft.com/dynamics365/fin-ops-core/dev-itpro/get-started/whats-new-platform-update-32).</span></span>

## <a name="search-values-are-remembered-when-changing-view-options-in-streamlined-employee-form-383833"></a><span data-ttu-id="01b79-110">合理化された従業員フォームで表示オプションを変更すると、検索値が記憶される (383833)</span><span class="sxs-lookup"><span data-stu-id="01b79-110">Search values are remembered when changing view options in streamlined employee form (383833)</span></span>

<span data-ttu-id="01b79-111">新しい **作業者** フォームでは、表示オプションを変更して変更を適用したときに検索値が記憶されるようになりました。</span><span class="sxs-lookup"><span data-stu-id="01b79-111">The new **Worker** form now remembers  search values when you change the view options and apply changes.</span></span>

## <a name="compensation-management-summary-tiles-in-preview-feature-redirect-to-wrong-form-401861"></a><span data-ttu-id="01b79-112">プレビュー機能で報酬管理の概要タイルが間違ったフォームにリダイレクトされる (401861)</span><span class="sxs-lookup"><span data-stu-id="01b79-112">Compensation management summary tiles in preview feature redirect to wrong form (401861)</span></span>

<span data-ttu-id="01b79-113">固定および変動報酬管理タイルでは、新しい **作業者** フォームに正しいレコードが表示されるようになりました。</span><span class="sxs-lookup"><span data-stu-id="01b79-113">Fixed and variable compensation management tiles now display the correct records in the new **Worker** form.</span></span> <span data-ttu-id="01b79-114">合理化された従業員フォームのプレビュー機能にのみ適用されます。</span><span class="sxs-lookup"><span data-stu-id="01b79-114">Applies only to the streamlined employee form preview feature.</span></span> <span data-ttu-id="01b79-115">このプレビュー機能は、**機能管理** で有効にすることができます。</span><span class="sxs-lookup"><span data-stu-id="01b79-115">You can enable this preview feature in **Feature management**.</span></span> <span data-ttu-id="01b79-116">詳細については [機能の管理](hr-admin-manage-features.md) を参照してください。</span><span class="sxs-lookup"><span data-stu-id="01b79-116">For more information, see [Manage features](hr-admin-manage-features.md).</span></span>

## <a name="empty-status-field-for-some-leave-request-records-in-dataverse-414915"></a><span data-ttu-id="01b79-117">Dataverse の一部の休暇申請レコードの空のステータス フィールド (414915)</span><span class="sxs-lookup"><span data-stu-id="01b79-117">Empty Status field for some leave request records in Dataverse (414915)</span></span>

<span data-ttu-id="01b79-118">この変更により、休暇申請の **ステータス** フィールドが **確認** に設定されている場合の Dataverse の問題が修正されます。</span><span class="sxs-lookup"><span data-stu-id="01b79-118">This change corrects an issue in Dataverse when the **Status** field in a leave request is set to **Review**.</span></span> <span data-ttu-id="01b79-119">Dataverse でステータスが反映されるようになりました。</span><span class="sxs-lookup"><span data-stu-id="01b79-119">Dataverse now reflects the status.</span></span>

## <a name="skill-gap-analysis-only-possible-for-assigned-job-411390"></a><span data-ttu-id="01b79-120">割り当てられた職務でのみ使用可能なスキル ギャップ分析 (411390)</span><span class="sxs-lookup"><span data-stu-id="01b79-120">Skill gap analysis only possible for assigned job (411390)</span></span>

<span data-ttu-id="01b79-121">Human Resources で定義されているすべての職務に対してスキル ギャップ分析を行うことができるようになりました。</span><span class="sxs-lookup"><span data-stu-id="01b79-121">You can now do a skill gap analysis on any job defined in Human Resources.</span></span>

## <a name="system-currency-doesnt-sync-from-dataverse-to-human-resources-in-new-environments-418011"></a><span data-ttu-id="01b79-122">新しい環境で、システム通貨が Dataverse から Human Resources に同期しない (418011)</span><span class="sxs-lookup"><span data-stu-id="01b79-122">System currency doesn't sync from Dataverse to Human Resources in new environments (418011)</span></span>

<span data-ttu-id="01b79-123">Dataverse のシステム通貨を Human Resources に同期できるようになりました。</span><span class="sxs-lookup"><span data-stu-id="01b79-123">The system currency in Dataverse can now sync to Human Resources.</span></span>

## <a name="in-preview"></a><span data-ttu-id="01b79-124">プレビュー</span><span class="sxs-lookup"><span data-stu-id="01b79-124">In preview</span></span>

- [<span data-ttu-id="01b79-125">休暇のプレビュー機能</span><span class="sxs-lookup"><span data-stu-id="01b79-125">Leave and absence preview features</span></span>](hr-leave-and-absence-overview.md?leave-and-absence-preview-features)

- [<span data-ttu-id="01b79-126">福利厚生管理のプレビュー機能</span><span class="sxs-lookup"><span data-stu-id="01b79-126">Benefits management preview features</span></span>](hr-benefits-management-overview.md)

## <a name="coming-soon"></a><span data-ttu-id="01b79-127">間もなく公開</span><span class="sxs-lookup"><span data-stu-id="01b79-127">Coming soon</span></span>

### <a name="updated-dataverse-solution"></a><span data-ttu-id="01b79-128">更新された Dataverse ソリューション</span><span class="sxs-lookup"><span data-stu-id="01b79-128">Updated Dataverse solution</span></span>

<span data-ttu-id="01b79-129">次の変更により、新しい Dataverse ソリューションがまもなく利用可能になります。</span><span class="sxs-lookup"><span data-stu-id="01b79-129">A new Dataverse solution will be available soon with the following changes:</span></span>

| <span data-ttu-id="01b79-130">説明</span><span class="sxs-lookup"><span data-stu-id="01b79-130">Description</span></span> | <span data-ttu-id="01b79-131">計上額</span><span class="sxs-lookup"><span data-stu-id="01b79-131">Change</span></span> |
| ----------------------------------------- | --- |
| <span data-ttu-id="01b79-132">**職務/職位** エンティティの変更</span><span class="sxs-lookup"><span data-stu-id="01b79-132">**Job/Position** entity changes</span></span> | <span data-ttu-id="01b79-133">追加された **報酬地域**</span><span class="sxs-lookup"><span data-stu-id="01b79-133">**Compensation region** added</span></span></br><span data-ttu-id="01b79-134">追加された **財務分析コード**</span><span class="sxs-lookup"><span data-stu-id="01b79-134">**Financial dimensions** added</span></span> |
| <span data-ttu-id="01b79-135">**作業者** エンティティの変更</span><span class="sxs-lookup"><span data-stu-id="01b79-135">**Worker** entity changes</span></span> | <span data-ttu-id="01b79-136">追加された **名前の順序**</span><span class="sxs-lookup"><span data-stu-id="01b79-136">**Name sequence** added</span></span></br><span data-ttu-id="01b79-137">追加された **自宅から作業**</span><span class="sxs-lookup"><span data-stu-id="01b79-137">**Works from home** added</span></span></br><span data-ttu-id="01b79-138">追加された **言語**</span><span class="sxs-lookup"><span data-stu-id="01b79-138">**Language** added</span></span></br><span data-ttu-id="01b79-139">追加された **勤続日数**</span><span class="sxs-lookup"><span data-stu-id="01b79-139">**Seniority date** added</span></span></br><span data-ttu-id="01b79-140">追加された **記念日**</span><span class="sxs-lookup"><span data-stu-id="01b79-140">**Anniversary date** added</span></span></br><span data-ttu-id="01b79-141">追加された **元の採用日付**</span><span class="sxs-lookup"><span data-stu-id="01b79-141">**Original hire date** added</span></span> |
| <span data-ttu-id="01b79-142">**雇用** エンティティの変更</span><span class="sxs-lookup"><span data-stu-id="01b79-142">**Employment** entity changes</span></span> | <span data-ttu-id="01b79-143">追加された **財務分析コード**</span><span class="sxs-lookup"><span data-stu-id="01b79-143">**Financial dimensions** added</span></span></br><span data-ttu-id="01b79-144">追加された **退職理由**</span><span class="sxs-lookup"><span data-stu-id="01b79-144">**Termination reason** added</span></span></br><span data-ttu-id="01b79-145">**移行日** から名前変更された **退職日**</span><span class="sxs-lookup"><span data-stu-id="01b79-145">**Termination date** renamed from **Transition date**</span></span></br><span data-ttu-id="01b79-146">追加された **猶予期間**</span><span class="sxs-lookup"><span data-stu-id="01b79-146">**Probation date** added</span></span> |
| <span data-ttu-id="01b79-147">**作業者住所** エンティティの変更</span><span class="sxs-lookup"><span data-stu-id="01b79-147">**Worker address** entity changes</span></span> | <span data-ttu-id="01b79-148">追加された **番地**</span><span class="sxs-lookup"><span data-stu-id="01b79-148">**Street address** added</span></span></br><span data-ttu-id="01b79-149">廃止としてマークされた **住所行 1**、**住所行 2**、および **住所行 3**</span><span class="sxs-lookup"><span data-stu-id="01b79-149">**Address line 1**, **Address line 2**, and **Address line 3** marked for deprecation</span></span> |
| <span data-ttu-id="01b79-150">新しい変動報酬の設定エンティティ</span><span class="sxs-lookup"><span data-stu-id="01b79-150">New variable compensation setup entities</span></span> | <span data-ttu-id="01b79-151">**変動報酬プラン タイプ**</span><span class="sxs-lookup"><span data-stu-id="01b79-151">**Compensation variable plan type**</span></span></br><span data-ttu-id="01b79-152">**変動報酬プラン**</span><span class="sxs-lookup"><span data-stu-id="01b79-152">**Compensation variable plan**</span></span></br><span data-ttu-id="01b79-153">**給付ルール**</span><span class="sxs-lookup"><span data-stu-id="01b79-153">**Vesting rules**</span></span></br><span data-ttu-id="01b79-154">**変動報酬プラン レベル**</span><span class="sxs-lookup"><span data-stu-id="01b79-154">**Compensation variable plan level**</span></span> |
| <span data-ttu-id="01b79-155">新しい **作業者カレンダー雇用** エンティティ</span><span class="sxs-lookup"><span data-stu-id="01b79-155">New **Worker calendar employment** entity</span></span> | <span data-ttu-id="01b79-156">追加された **作業カレンダー エンティティ**</span><span class="sxs-lookup"><span data-stu-id="01b79-156">**Work calendar entity** added</span></span> |
| <span data-ttu-id="01b79-157">新しい **給与職位詳細** エンティティ</span><span class="sxs-lookup"><span data-stu-id="01b79-157">New **Payroll position detail** entity</span></span> | <span data-ttu-id="01b79-158">追加された **給与職位詳細**</span><span class="sxs-lookup"><span data-stu-id="01b79-158">**Payroll position detail** added</span></span> |
| <span data-ttu-id="01b79-159">新しい **肩書** エンティティ</span><span class="sxs-lookup"><span data-stu-id="01b79-159">New **Title** entity</span></span> | <span data-ttu-id="01b79-160">追加済み **タイトル**。</span><span class="sxs-lookup"><span data-stu-id="01b79-160">**Title** added.</span></span> <span data-ttu-id="01b79-161">新しい **タイトル** エンティティが、Human Resources と Dataverse の間の同期プロセスに含まれます。</span><span class="sxs-lookup"><span data-stu-id="01b79-161">The new **Title** entity will be included in the sync process between Human Resources and Dataverse.</span></span> <span data-ttu-id="01b79-162">**職位** または **ジョブ** エンティティから最初に参照されることはありません。</span><span class="sxs-lookup"><span data-stu-id="01b79-162">It won't be initially referenced from **Job Position** or **Job** entities.</span></span> |

## <a name="see-also"></a><span data-ttu-id="01b79-163">参照</span><span class="sxs-lookup"><span data-stu-id="01b79-163">See also</span></span>

[<span data-ttu-id="01b79-164">Human Resources の新機能および変更された機能</span><span class="sxs-lookup"><span data-stu-id="01b79-164">What's new or changed in Human Resources</span></span>](hr-admin-whats-new.md)</br>
[<span data-ttu-id="01b79-165">Dynamics 365 Human Resources 2019 のリリース ウェーブ 2 の概要</span><span class="sxs-lookup"><span data-stu-id="01b79-165">Overview of Dynamics 365 Human Resources 2019 release wave 2</span></span>](https://docs.microsoft.com/dynamics365-release-plan/2019wave2/dynamics365-human-resources/)</br>
[<span data-ttu-id="01b79-166">更新プロセス</span><span class="sxs-lookup"><span data-stu-id="01b79-166">Update process</span></span>](hr-admin-setup-update-process.md)</br>
[<span data-ttu-id="01b79-167">機能の管理</span><span class="sxs-lookup"><span data-stu-id="01b79-167">Manage features</span></span>](hr-admin-manage-features.md)

[!INCLUDE[footer-include](../includes/footer-banner.md)]