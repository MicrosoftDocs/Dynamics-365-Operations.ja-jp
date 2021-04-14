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
ms.reviewer: anbichse
ms.search.scope: Human Resources
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: jaredha
ms.search.validFrom: 2020-02-07
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: c4453b5507f9972a4bfbc18a92f98b90b8e9c983
ms.sourcegitcommit: 3cdc42346bb653c13ab33a7142dbb7969f1f6dda
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 03/31/2021
ms.locfileid: "5790479"
---
# <a name="whats-new-or-changed-in-dynamics-365-human-resources-february-12-2020"></a><span data-ttu-id="73b92-103">Dynamics 365 Human Resources の新機能および変更された機能 (2020 年 2 月 12 日)</span><span class="sxs-lookup"><span data-stu-id="73b92-103">What's new or changed in Dynamics 365 Human Resources (February 12, 2020)</span></span>

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

[!include [rename-banner](~/includes/cc-data-platform-banner.md)]

<span data-ttu-id="73b92-104">この記事では、Dynamics 365 Human Resources の新機能および変更された機能について説明します。</span><span class="sxs-lookup"><span data-stu-id="73b92-104">This article describes features that are either new or changed in Dynamics 365 Human Resources.</span></span> <span data-ttu-id="73b92-105">変更は、ビルド番号 8.1.2867 に適用されます。</span><span class="sxs-lookup"><span data-stu-id="73b92-105">Changes apply to build number 8.1.2867.</span></span> <span data-ttu-id="73b92-106">ヘッダーにあるかっこ内の数字は、Microsoft Dynamics Lifecycle Services (LCS) のサポート番号を参照していることがあります。</span><span class="sxs-lookup"><span data-stu-id="73b92-106">The numbers in parentheses in some headings refer to support numbers in Microsoft Dynamics Lifecycle Services (LCS).</span></span>

## <a name="existing-entities-compfixedempls-and-hcmpersonimage-should-be-accessible-from-odata-414178"></a><span data-ttu-id="73b92-107">既存のエンティティ CompFixedEmpls および HcmPersonImage は、OData からアクセス可能である必要がある (414178)</span><span class="sxs-lookup"><span data-stu-id="73b92-107">Existing entities CompFixedEmpls and HcmPersonImage should be accessible from OData (414178)</span></span>

<span data-ttu-id="73b92-108">今週のリリースにより、**CompFixedEmpls** と **HcmPersonImage** エンティティはパブリックになり、ODAta を介して使用できるようになりました。</span><span class="sxs-lookup"><span data-stu-id="73b92-108">With this week's release, the **CompFixedEmpls** and **HcmPersonImage** entities are now public and available via ODAta.</span></span>

## <a name="delete-employment-from-dataverse-doesnt-work-when-employment-details-arent-active-403193"></a><span data-ttu-id="73b92-109">雇用の詳細が有効でない場合、Dataverse からの雇用の削除は機能しない (403193)</span><span class="sxs-lookup"><span data-stu-id="73b92-109">Delete employment from Dataverse doesn't work when employment details aren't active (403193)</span></span>

<span data-ttu-id="73b92-110">この変更により、有効な雇用の詳細が存在しない場合でも、Dataverse 経由で雇用を削除できるようになります。</span><span class="sxs-lookup"><span data-stu-id="73b92-110">This change now allows for deleting employment via Dataverse when no active employment details exist.</span></span>

## <a name="course-registration-workflow-changes-status-to-complete-and-errors-after-second-approval-409749"></a><span data-ttu-id="73b92-111">コース登録ワークフローは、2 回目の承認後に完了およびエラーにステータスを変更する (409749)</span><span class="sxs-lookup"><span data-stu-id="73b92-111">Course registration workflow changes status to complete and errors after second approval (409749)</span></span>

<span data-ttu-id="73b92-112">コース登録ワークフローは、複数の承認者が使用できるように更新されました。</span><span class="sxs-lookup"><span data-stu-id="73b92-112">Course registration workflow has been updated to allow for multiple approvers.</span></span>

## <a name="in-preview"></a><span data-ttu-id="73b92-113">プレビュー</span><span class="sxs-lookup"><span data-stu-id="73b92-113">In preview</span></span>

<span data-ttu-id="73b92-114">2020 年 2 月 3 日に次のプレビュー機能が利用可能になります。</span><span class="sxs-lookup"><span data-stu-id="73b92-114">The following preview features are available on February 3, 2020:</span></span>

- <span data-ttu-id="73b92-115">**休暇および欠勤のプレビュー機能** - 詳細については、[休暇および欠勤のプレビュー機能](hr-leave-and-absence-overview.md?leave-and-absence-preview-features) を参照してください。</span><span class="sxs-lookup"><span data-stu-id="73b92-115">**Leave and absence preview features** - For more information, see [Leave and absence preview features](hr-leave-and-absence-overview.md?leave-and-absence-preview-features).</span></span>

- <span data-ttu-id="73b92-116">**福利厚生管理プレビュー機能** - 既知の問題など、詳細については[福利厚生管理の概要](hr-benefits-management-overview.md)を参照してください。</span><span class="sxs-lookup"><span data-stu-id="73b92-116">**Benefits management preview feature** - For more information, including known issues, see [Benefits management overview](hr-benefits-management-overview.md).</span></span>

## <a name="coming-soon"></a><span data-ttu-id="73b92-117">間もなく公開</span><span class="sxs-lookup"><span data-stu-id="73b92-117">Coming soon</span></span>

### <a name="platform-update-32"></a><span data-ttu-id="73b92-118">プラットフォーム update 32</span><span class="sxs-lookup"><span data-stu-id="73b92-118">Platform update 32</span></span> 

<span data-ttu-id="73b92-119">プラットフォームの更新 32 はまもなく使用可能になります。</span><span class="sxs-lookup"><span data-stu-id="73b92-119">Platform update 32 will be available soon.</span></span> <span data-ttu-id="73b92-120">[プラットフォームの更新 32 に関する詳細情報はこちらを参照してください](https://docs.microsoft.com/dynamics365/fin-ops-core/dev-itpro/get-started/whats-new-platform-update-32)。</span><span class="sxs-lookup"><span data-stu-id="73b92-120">[Find out more information about Platform update 32 here](https://docs.microsoft.com/dynamics365/fin-ops-core/dev-itpro/get-started/whats-new-platform-update-32).</span></span>

### <a name="updated-dataverse-solution"></a><span data-ttu-id="73b92-121">更新された Dataverse ソリューション</span><span class="sxs-lookup"><span data-stu-id="73b92-121">Updated Dataverse Solution</span></span>

<span data-ttu-id="73b92-122">次の変更により、新しい Dataverse ソリューションがまもなく利用可能になります。</span><span class="sxs-lookup"><span data-stu-id="73b92-122">A new Dataverse solution will be available soon with the following changes:</span></span>

| <span data-ttu-id="73b92-123">説明</span><span class="sxs-lookup"><span data-stu-id="73b92-123">Description</span></span> | <span data-ttu-id="73b92-124">計上額</span><span class="sxs-lookup"><span data-stu-id="73b92-124">Change</span></span> |
| ----------------------------------------- | --- |
| <span data-ttu-id="73b92-125">**職務/職位** エンティティの変更</span><span class="sxs-lookup"><span data-stu-id="73b92-125">**Job/Position** entity changes</span></span> | <span data-ttu-id="73b92-126">追加された **報酬地域**</span><span class="sxs-lookup"><span data-stu-id="73b92-126">**Compensation region** added</span></span></br><span data-ttu-id="73b92-127">追加された **財務分析コード**</span><span class="sxs-lookup"><span data-stu-id="73b92-127">**Financial dimensions** added</span></span> |
| <span data-ttu-id="73b92-128">**作業者** エンティティの変更</span><span class="sxs-lookup"><span data-stu-id="73b92-128">**Worker** entity changes</span></span> | <span data-ttu-id="73b92-129">追加された **名前の順序**</span><span class="sxs-lookup"><span data-stu-id="73b92-129">**Name sequence** added</span></span></br><span data-ttu-id="73b92-130">追加された **自宅から作業**</span><span class="sxs-lookup"><span data-stu-id="73b92-130">**Works from home** added</span></span></br><span data-ttu-id="73b92-131">追加された **言語**</span><span class="sxs-lookup"><span data-stu-id="73b92-131">**Language** added</span></span></br><span data-ttu-id="73b92-132">追加された **勤続日数**</span><span class="sxs-lookup"><span data-stu-id="73b92-132">**Seniority date** added</span></span></br><span data-ttu-id="73b92-133">追加された **記念日**</span><span class="sxs-lookup"><span data-stu-id="73b92-133">**Anniversary date** added</span></span></br><span data-ttu-id="73b92-134">追加された **元の採用日付**</span><span class="sxs-lookup"><span data-stu-id="73b92-134">**Original hire date** added</span></span> |
| <span data-ttu-id="73b92-135">**雇用** エンティティの変更</span><span class="sxs-lookup"><span data-stu-id="73b92-135">**Employment** entity changes</span></span> | <span data-ttu-id="73b92-136">追加された **財務分析コード**</span><span class="sxs-lookup"><span data-stu-id="73b92-136">**Financial dimensions** added</span></span></br><span data-ttu-id="73b92-137">追加された **退職理由**</span><span class="sxs-lookup"><span data-stu-id="73b92-137">**Termination reason** added</span></span></br><span data-ttu-id="73b92-138">**移行日** から名前変更された **退職日**</span><span class="sxs-lookup"><span data-stu-id="73b92-138">**Termination date** renamed from **Transition date**</span></span></br><span data-ttu-id="73b92-139">追加された **猶予期間**</span><span class="sxs-lookup"><span data-stu-id="73b92-139">**Probation date** added</span></span> |
| <span data-ttu-id="73b92-140">**作業者住所** エンティティの変更</span><span class="sxs-lookup"><span data-stu-id="73b92-140">**Worker address** entity changes</span></span> | <span data-ttu-id="73b92-141">追加された **番地**</span><span class="sxs-lookup"><span data-stu-id="73b92-141">**Street address** added</span></span></br><span data-ttu-id="73b92-142">廃止としてマークされた **住所行 1**、**住所行 2**、および **住所行 3**</span><span class="sxs-lookup"><span data-stu-id="73b92-142">**Address line 1**, **Address line 2**, and **Address line 3** marked for deprecation</span></span> |
| <span data-ttu-id="73b92-143">新しい変動報酬の設定エンティティ</span><span class="sxs-lookup"><span data-stu-id="73b92-143">New variable compensation setup entities</span></span> | <span data-ttu-id="73b92-144">**変動報酬プラン タイプ**</span><span class="sxs-lookup"><span data-stu-id="73b92-144">**Compensation variable plan type**</span></span></br><span data-ttu-id="73b92-145">**変動報酬プラン**</span><span class="sxs-lookup"><span data-stu-id="73b92-145">**Compensation variable plan**</span></span></br><span data-ttu-id="73b92-146">**給付ルール**</span><span class="sxs-lookup"><span data-stu-id="73b92-146">**Vesting rules**</span></span></br><span data-ttu-id="73b92-147">**変動報酬プラン レベル**</span><span class="sxs-lookup"><span data-stu-id="73b92-147">**Compensation variable plan level**</span></span> |
| <span data-ttu-id="73b92-148">新しい **作業者カレンダー雇用** エンティティ</span><span class="sxs-lookup"><span data-stu-id="73b92-148">New **Worker calendar employment** entity</span></span> | <span data-ttu-id="73b92-149">追加された **作業カレンダー エンティティ**</span><span class="sxs-lookup"><span data-stu-id="73b92-149">**Work calendar entity** added</span></span> |
| <span data-ttu-id="73b92-150">新しい **給与職位詳細** エンティティ</span><span class="sxs-lookup"><span data-stu-id="73b92-150">New **Payroll position detail** entity</span></span> | <span data-ttu-id="73b92-151">追加された **給与職位詳細**</span><span class="sxs-lookup"><span data-stu-id="73b92-151">**Payroll position detail** added</span></span> |
| <span data-ttu-id="73b92-152">新しい **肩書** エンティティ</span><span class="sxs-lookup"><span data-stu-id="73b92-152">New **Title** entity</span></span> | <span data-ttu-id="73b92-153">追加済み **タイトル**。</span><span class="sxs-lookup"><span data-stu-id="73b92-153">**Title** added.</span></span> <span data-ttu-id="73b92-154">新しい **タイトル** エンティティが、Human Resources と Dataverse の間の同期プロセスに含まれます。</span><span class="sxs-lookup"><span data-stu-id="73b92-154">The new **Title** entity will be included in the sync process between Human Resources and Dataverse.</span></span> <span data-ttu-id="73b92-155">**職位** または **ジョブ** エンティティから最初に参照されることはありません。</span><span class="sxs-lookup"><span data-stu-id="73b92-155">It won't be initially referenced from **Job Position** or **Job** entities.</span></span> |

## <a name="see-also"></a><span data-ttu-id="73b92-156">参照</span><span class="sxs-lookup"><span data-stu-id="73b92-156">See also</span></span>

[<span data-ttu-id="73b92-157">Human Resources の新機能および変更された機能</span><span class="sxs-lookup"><span data-stu-id="73b92-157">What's new or changed in Human Resources</span></span>](hr-admin-whats-new.md)</br>
[<span data-ttu-id="73b92-158">Dynamics 365 Human Resources 2019 のリリース ウェーブ 2 の概要</span><span class="sxs-lookup"><span data-stu-id="73b92-158">Overview of Dynamics 365 Human Resources 2019 release wave 2</span></span>](https://docs.microsoft.com/dynamics365-release-plan/2019wave2/dynamics365-human-resources/)</br>
[<span data-ttu-id="73b92-159">更新プロセス</span><span class="sxs-lookup"><span data-stu-id="73b92-159">Update process</span></span>](hr-admin-setup-update-process.md)</br>
[<span data-ttu-id="73b92-160">機能の管理</span><span class="sxs-lookup"><span data-stu-id="73b92-160">Manage features</span></span>](hr-admin-manage-features.md)

[!INCLUDE[footer-include](../includes/footer-banner.md)]