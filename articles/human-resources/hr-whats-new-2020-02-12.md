---
title: Dynamics 365 Human Resources の新機能および変更された機能 (2020 年 2 月 12 日)
description: この記事では、2020 年 2 月 12 日に更新された Microsoft Dynamics 365 Human Resources の新機能、または変更された機能について説明します。
author: andreabichsel
ms.date: 02/07/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.search.scope: Human Resources
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: jaredha
ms.search.validFrom: 2020-02-07
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: 6cae0d3f59b1b0d01f3b2f6cf3469520e35d2f91
ms.sourcegitcommit: 879ee8a10e6158885795dce4b3db5077540eec41
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 05/18/2021
ms.locfileid: "6051215"
---
# <a name="whats-new-or-changed-in-dynamics-365-human-resources-february-12-2020"></a><span data-ttu-id="e4cf9-103">Dynamics 365 Human Resources の新機能および変更された機能 (2020 年 2 月 12 日)</span><span class="sxs-lookup"><span data-stu-id="e4cf9-103">What's new or changed in Dynamics 365 Human Resources (February 12, 2020)</span></span>

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

[!include [rename-banner](~/includes/cc-data-platform-banner.md)]

<span data-ttu-id="e4cf9-104">この記事では、Dynamics 365 Human Resources の新機能および変更された機能について説明します。</span><span class="sxs-lookup"><span data-stu-id="e4cf9-104">This article describes features that are either new or changed in Dynamics 365 Human Resources.</span></span> <span data-ttu-id="e4cf9-105">変更は、ビルド番号 8.1.2867 に適用されます。</span><span class="sxs-lookup"><span data-stu-id="e4cf9-105">Changes apply to build number 8.1.2867.</span></span> <span data-ttu-id="e4cf9-106">ヘッダーにあるかっこ内の数字は、Microsoft Dynamics Lifecycle Services (LCS) のサポート番号を参照していることがあります。</span><span class="sxs-lookup"><span data-stu-id="e4cf9-106">The numbers in parentheses in some headings refer to support numbers in Microsoft Dynamics Lifecycle Services (LCS).</span></span>

## <a name="existing-entities-compfixedempls-and-hcmpersonimage-should-be-accessible-from-odata-414178"></a><span data-ttu-id="e4cf9-107">既存のエンティティ CompFixedEmpls および HcmPersonImage は、OData からアクセス可能である必要がある (414178)</span><span class="sxs-lookup"><span data-stu-id="e4cf9-107">Existing entities CompFixedEmpls and HcmPersonImage should be accessible from OData (414178)</span></span>

<span data-ttu-id="e4cf9-108">今週のリリースにより、**CompFixedEmpls** と **HcmPersonImage** エンティティはパブリックになり、ODAta を介して使用できるようになりました。</span><span class="sxs-lookup"><span data-stu-id="e4cf9-108">With this week's release, the **CompFixedEmpls** and **HcmPersonImage** entities are now public and available via ODAta.</span></span>

## <a name="delete-employment-from-dataverse-doesnt-work-when-employment-details-arent-active-403193"></a><span data-ttu-id="e4cf9-109">雇用の詳細が有効でない場合、Dataverse からの雇用の削除は機能しない (403193)</span><span class="sxs-lookup"><span data-stu-id="e4cf9-109">Delete employment from Dataverse doesn't work when employment details aren't active (403193)</span></span>

<span data-ttu-id="e4cf9-110">この変更により、有効な雇用の詳細が存在しない場合でも、Dataverse 経由で雇用を削除できるようになります。</span><span class="sxs-lookup"><span data-stu-id="e4cf9-110">This change now allows for deleting employment via Dataverse when no active employment details exist.</span></span>

## <a name="course-registration-workflow-changes-status-to-complete-and-errors-after-second-approval-409749"></a><span data-ttu-id="e4cf9-111">コース登録ワークフローは、2 回目の承認後に完了およびエラーにステータスを変更する (409749)</span><span class="sxs-lookup"><span data-stu-id="e4cf9-111">Course registration workflow changes status to complete and errors after second approval (409749)</span></span>

<span data-ttu-id="e4cf9-112">コース登録ワークフローは、複数の承認者が使用できるように更新されました。</span><span class="sxs-lookup"><span data-stu-id="e4cf9-112">Course registration workflow has been updated to allow for multiple approvers.</span></span>

## <a name="in-preview"></a><span data-ttu-id="e4cf9-113">プレビュー</span><span class="sxs-lookup"><span data-stu-id="e4cf9-113">In preview</span></span>

<span data-ttu-id="e4cf9-114">2020 年 2 月 3 日に次のプレビュー機能が利用可能になります。</span><span class="sxs-lookup"><span data-stu-id="e4cf9-114">The following preview features are available on February 3, 2020:</span></span>

- <span data-ttu-id="e4cf9-115">**休暇および欠勤のプレビュー機能** - 詳細については、[休暇および欠勤のプレビュー機能](hr-leave-and-absence-overview.md?leave-and-absence-preview-features) を参照してください。</span><span class="sxs-lookup"><span data-stu-id="e4cf9-115">**Leave and absence preview features** - For more information, see [Leave and absence preview features](hr-leave-and-absence-overview.md?leave-and-absence-preview-features).</span></span>

- <span data-ttu-id="e4cf9-116">**福利厚生管理プレビュー機能** - 既知の問題など、詳細については[福利厚生管理の概要](hr-benefits-management-overview.md)を参照してください。</span><span class="sxs-lookup"><span data-stu-id="e4cf9-116">**Benefits management preview feature** - For more information, including known issues, see [Benefits management overview](hr-benefits-management-overview.md).</span></span>

## <a name="coming-soon"></a><span data-ttu-id="e4cf9-117">間もなく公開</span><span class="sxs-lookup"><span data-stu-id="e4cf9-117">Coming soon</span></span>

### <a name="platform-update-32"></a><span data-ttu-id="e4cf9-118">プラットフォーム update 32</span><span class="sxs-lookup"><span data-stu-id="e4cf9-118">Platform update 32</span></span> 

<span data-ttu-id="e4cf9-119">プラットフォームの更新 32 はまもなく使用可能になります。</span><span class="sxs-lookup"><span data-stu-id="e4cf9-119">Platform update 32 will be available soon.</span></span> <span data-ttu-id="e4cf9-120">[プラットフォームの更新 32 に関する詳細情報はこちらを参照してください](../fin-ops-core/dev-itpro/get-started/whats-new-platform-update-32.md)。</span><span class="sxs-lookup"><span data-stu-id="e4cf9-120">[Find out more information about Platform update 32 here](../fin-ops-core/dev-itpro/get-started/whats-new-platform-update-32.md).</span></span>

### <a name="updated-dataverse-solution"></a><span data-ttu-id="e4cf9-121">更新された Dataverse ソリューション</span><span class="sxs-lookup"><span data-stu-id="e4cf9-121">Updated Dataverse Solution</span></span>

<span data-ttu-id="e4cf9-122">次の変更により、新しい Dataverse ソリューションがまもなく利用可能になります。</span><span class="sxs-lookup"><span data-stu-id="e4cf9-122">A new Dataverse solution will be available soon with the following changes:</span></span>

| <span data-ttu-id="e4cf9-123">説明</span><span class="sxs-lookup"><span data-stu-id="e4cf9-123">Description</span></span> | <span data-ttu-id="e4cf9-124">計上額</span><span class="sxs-lookup"><span data-stu-id="e4cf9-124">Change</span></span> |
| ----------------------------------------- | --- |
| <span data-ttu-id="e4cf9-125">**職務/職位** エンティティの変更</span><span class="sxs-lookup"><span data-stu-id="e4cf9-125">**Job/Position** entity changes</span></span> | <span data-ttu-id="e4cf9-126">追加された **報酬地域**</span><span class="sxs-lookup"><span data-stu-id="e4cf9-126">**Compensation region** added</span></span></br><span data-ttu-id="e4cf9-127">追加された **財務分析コード**</span><span class="sxs-lookup"><span data-stu-id="e4cf9-127">**Financial dimensions** added</span></span> |
| <span data-ttu-id="e4cf9-128">**作業者** エンティティの変更</span><span class="sxs-lookup"><span data-stu-id="e4cf9-128">**Worker** entity changes</span></span> | <span data-ttu-id="e4cf9-129">追加された **名前の順序**</span><span class="sxs-lookup"><span data-stu-id="e4cf9-129">**Name sequence** added</span></span></br><span data-ttu-id="e4cf9-130">追加された **自宅から作業**</span><span class="sxs-lookup"><span data-stu-id="e4cf9-130">**Works from home** added</span></span></br><span data-ttu-id="e4cf9-131">追加された **言語**</span><span class="sxs-lookup"><span data-stu-id="e4cf9-131">**Language** added</span></span></br><span data-ttu-id="e4cf9-132">追加された **勤続日数**</span><span class="sxs-lookup"><span data-stu-id="e4cf9-132">**Seniority date** added</span></span></br><span data-ttu-id="e4cf9-133">追加された **記念日**</span><span class="sxs-lookup"><span data-stu-id="e4cf9-133">**Anniversary date** added</span></span></br><span data-ttu-id="e4cf9-134">追加された **元の採用日付**</span><span class="sxs-lookup"><span data-stu-id="e4cf9-134">**Original hire date** added</span></span> |
| <span data-ttu-id="e4cf9-135">**雇用** エンティティの変更</span><span class="sxs-lookup"><span data-stu-id="e4cf9-135">**Employment** entity changes</span></span> | <span data-ttu-id="e4cf9-136">追加された **財務分析コード**</span><span class="sxs-lookup"><span data-stu-id="e4cf9-136">**Financial dimensions** added</span></span></br><span data-ttu-id="e4cf9-137">追加された **退職理由**</span><span class="sxs-lookup"><span data-stu-id="e4cf9-137">**Termination reason** added</span></span></br><span data-ttu-id="e4cf9-138">**移行日** から名前変更された **退職日**</span><span class="sxs-lookup"><span data-stu-id="e4cf9-138">**Termination date** renamed from **Transition date**</span></span></br><span data-ttu-id="e4cf9-139">追加された **猶予期間**</span><span class="sxs-lookup"><span data-stu-id="e4cf9-139">**Probation date** added</span></span> |
| <span data-ttu-id="e4cf9-140">**作業者住所** エンティティの変更</span><span class="sxs-lookup"><span data-stu-id="e4cf9-140">**Worker address** entity changes</span></span> | <span data-ttu-id="e4cf9-141">追加された **番地**</span><span class="sxs-lookup"><span data-stu-id="e4cf9-141">**Street address** added</span></span></br><span data-ttu-id="e4cf9-142">廃止としてマークされた **住所行 1**、**住所行 2**、および **住所行 3**</span><span class="sxs-lookup"><span data-stu-id="e4cf9-142">**Address line 1**, **Address line 2**, and **Address line 3** marked for deprecation</span></span> |
| <span data-ttu-id="e4cf9-143">新しい変動報酬の設定エンティティ</span><span class="sxs-lookup"><span data-stu-id="e4cf9-143">New variable compensation setup entities</span></span> | <span data-ttu-id="e4cf9-144">**変動報酬プラン タイプ**</span><span class="sxs-lookup"><span data-stu-id="e4cf9-144">**Compensation variable plan type**</span></span></br><span data-ttu-id="e4cf9-145">**変動報酬プラン**</span><span class="sxs-lookup"><span data-stu-id="e4cf9-145">**Compensation variable plan**</span></span></br><span data-ttu-id="e4cf9-146">**給付ルール**</span><span class="sxs-lookup"><span data-stu-id="e4cf9-146">**Vesting rules**</span></span></br><span data-ttu-id="e4cf9-147">**変動報酬プラン レベル**</span><span class="sxs-lookup"><span data-stu-id="e4cf9-147">**Compensation variable plan level**</span></span> |
| <span data-ttu-id="e4cf9-148">新しい **作業者カレンダー雇用** エンティティ</span><span class="sxs-lookup"><span data-stu-id="e4cf9-148">New **Worker calendar employment** entity</span></span> | <span data-ttu-id="e4cf9-149">追加された **作業カレンダー エンティティ**</span><span class="sxs-lookup"><span data-stu-id="e4cf9-149">**Work calendar entity** added</span></span> |
| <span data-ttu-id="e4cf9-150">新しい **給与職位詳細** エンティティ</span><span class="sxs-lookup"><span data-stu-id="e4cf9-150">New **Payroll position detail** entity</span></span> | <span data-ttu-id="e4cf9-151">追加された **給与職位詳細**</span><span class="sxs-lookup"><span data-stu-id="e4cf9-151">**Payroll position detail** added</span></span> |
| <span data-ttu-id="e4cf9-152">新しい **肩書** エンティティ</span><span class="sxs-lookup"><span data-stu-id="e4cf9-152">New **Title** entity</span></span> | <span data-ttu-id="e4cf9-153">追加済み **タイトル**。</span><span class="sxs-lookup"><span data-stu-id="e4cf9-153">**Title** added.</span></span> <span data-ttu-id="e4cf9-154">新しい **タイトル** エンティティが、Human Resources と Dataverse の間の同期プロセスに含まれます。</span><span class="sxs-lookup"><span data-stu-id="e4cf9-154">The new **Title** entity will be included in the sync process between Human Resources and Dataverse.</span></span> <span data-ttu-id="e4cf9-155">**職位** または **ジョブ** エンティティから最初に参照されることはありません。</span><span class="sxs-lookup"><span data-stu-id="e4cf9-155">It won't be initially referenced from **Job Position** or **Job** entities.</span></span> |

## <a name="see-also"></a><span data-ttu-id="e4cf9-156">参照</span><span class="sxs-lookup"><span data-stu-id="e4cf9-156">See also</span></span>

[<span data-ttu-id="e4cf9-157">Human Resources の新機能および変更された機能</span><span class="sxs-lookup"><span data-stu-id="e4cf9-157">What's new or changed in Human Resources</span></span>](hr-admin-whats-new.md)</br>
[<span data-ttu-id="e4cf9-158">Dynamics 365 Human Resources 2019 のリリース ウェーブ 2 の概要</span><span class="sxs-lookup"><span data-stu-id="e4cf9-158">Overview of Dynamics 365 Human Resources 2019 release wave 2</span></span>](/dynamics365-release-plan/2019wave2/dynamics365-human-resources/)</br>
[<span data-ttu-id="e4cf9-159">更新プロセス</span><span class="sxs-lookup"><span data-stu-id="e4cf9-159">Update process</span></span>](hr-admin-setup-update-process.md)</br>
[<span data-ttu-id="e4cf9-160">機能の管理</span><span class="sxs-lookup"><span data-stu-id="e4cf9-160">Manage features</span></span>](hr-admin-manage-features.md)

[!INCLUDE[footer-include](../includes/footer-banner.md)]