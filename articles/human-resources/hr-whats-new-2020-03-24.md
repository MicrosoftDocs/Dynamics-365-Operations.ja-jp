---
title: Dynamics 365 Human Resources の新機能および変更された機能 (2020 年 3 月 24 日)
description: この記事では、2020 年 3 月 24 日に更新された Microsoft Dynamics 365 Human Resources の新機能、または変更された機能について説明します。
author: andreabichsel
manager: tfehr
ms.date: 03/24/2020
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
ms.search.validFrom: 2020-03-24
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: d3f9595bd19026e0dad0a2a2ad3708bd4f8ca1ba
ms.sourcegitcommit: f8bac7ca2803913fd236adbc3806259a17a110f4
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 02/06/2021
ms.locfileid: "5127948"
---
# <a name="whats-new-or-changed-in-dynamics-365-human-resources-march-24-2020"></a><span data-ttu-id="0ad56-103">Dynamics 365 Human Resources の新機能および変更された機能 (2020 年 3 月 24 日)</span><span class="sxs-lookup"><span data-stu-id="0ad56-103">What's new or changed in Dynamics 365 Human Resources (March 24, 2020)</span></span>

[!include [rename-banner](~/includes/cc-data-platform-banner.md)]

<span data-ttu-id="0ad56-104">この記事では、Dynamics 365 Human Resources の新機能および変更された機能について説明します。</span><span class="sxs-lookup"><span data-stu-id="0ad56-104">This article describes features that are either new or changed in Dynamics 365 Human Resources.</span></span> <span data-ttu-id="0ad56-105">変更は、ビルド番号 8.1.3073 に適用されます。</span><span class="sxs-lookup"><span data-stu-id="0ad56-105">Changes apply to build number 8.1.3073.</span></span> <span data-ttu-id="0ad56-106">一部のヘッダーにあるかっこ内の数字は、参照用に Lifecycle Services (LCS) のサポート番号を参照しています。</span><span class="sxs-lookup"><span data-stu-id="0ad56-106">The numbers in parentheses in some headings refer to Lifecycle Services (LCS) support numbers for reference.</span></span>

## <a name="human-resources-environment-limits-are-now-based-on-updated-licensing-394595"></a><span data-ttu-id="0ad56-107">人事管理環境の制限は、現在、更新されたライセンスに基づいている (394595)</span><span class="sxs-lookup"><span data-stu-id="0ad56-107">Human Resources environment limits are now based on updated licensing (394595)</span></span>

<span data-ttu-id="0ad56-108">Lifecycle Services (LCS) のプロジェクトあたりの環境数の制限が変更されました。</span><span class="sxs-lookup"><span data-stu-id="0ad56-108">The limit on the number of environments per project in Lifecycle Services (LCS) has changed.</span></span> <span data-ttu-id="0ad56-109">以前の制限は 2 つの環境でした。</span><span class="sxs-lookup"><span data-stu-id="0ad56-109">The previous limit was two environments.</span></span> <span data-ttu-id="0ad56-110">LCS で人事管理用に作成できる運用環境とサンドボックス環境の数の制限は、更新されたライセンスに基づいています。</span><span class="sxs-lookup"><span data-stu-id="0ad56-110">The limit on the number of production and sandbox environments you can create for Human Resources in LCS is now based on updated licensing.</span></span> <span data-ttu-id="0ad56-111">購入したライセンスの数に応じて、LCS プロジェクトごとに必要な数の環境を作成できるようになりました。</span><span class="sxs-lookup"><span data-stu-id="0ad56-111">You can now create as many environments as needed per LCS project, depending on the number of licenses purchased.</span></span> <span data-ttu-id="0ad56-112">2020 年 2 月 1 日に更新された新しいライセンスでは、顧客は追加の環境を購入できます。</span><span class="sxs-lookup"><span data-stu-id="0ad56-112">The new licensing, updated on February 1, 2020, allows customers to purchase additional environments.</span></span> <span data-ttu-id="0ad56-113">追加の環境のライセンス要件の詳細については、[Dynamics 365 ライセンスガイド](https://dynamics.microsoft.com/pricing/#HumanResources) を参照してください。</span><span class="sxs-lookup"><span data-stu-id="0ad56-113">For more information about licensing requirements for additional environments, see [Dynamics 365 Licensing Guide](https://dynamics.microsoft.com/pricing/#HumanResources).</span></span>

## <a name="platform-changes"></a><span data-ttu-id="0ad56-114">プラットフォームの変更</span><span class="sxs-lookup"><span data-stu-id="0ad56-114">Platform changes</span></span>

- <span data-ttu-id="0ad56-115">フル ページ アプリ (プレビュー) - このプレビュー機能は、保存されたビュー機能を有効にする必要があり、ダッシュボードから Power Apps とサード パーティー アプリをフルページ エクスペリエンスとして追加できます。</span><span class="sxs-lookup"><span data-stu-id="0ad56-115">Full page apps (Preview) - This preview feature, which requires you to enable the Saved views feature, allows Power Apps and third-party apps to be added as full-page experiences via the dashboard.</span></span>

- <span data-ttu-id="0ad56-116">保存されているビュー (プレビュー) - このプレビュー機能はパーソナル化 サブシステムの大幅な拡張を提供する、保存されているビューを有効にします。</span><span class="sxs-lookup"><span data-stu-id="0ad56-116">Saved views (Preview) - This preview feature enables saved views, which provide a significant enhancement to the personalization subsystem.</span></span> <span data-ttu-id="0ad56-117">この機能により、ユーザーはページごとに複数の名前を付けた個人用設定を使用できます。</span><span class="sxs-lookup"><span data-stu-id="0ad56-117">This feature allows users to have multiple named sets of personalizations per page.</span></span> <span data-ttu-id="0ad56-118">セキュリティ ロールにビューを公開することもできます。</span><span class="sxs-lookup"><span data-stu-id="0ad56-118">You can also publish views to security roles.</span></span>

- <span data-ttu-id="0ad56-119">「次の値のいずれか」のフィルタリング結果を最適化 - この機能により、最適化された「いずれか」のフィルタリング結果が可能になり、複数のフィルター値の入力を容易にして、個々またはすべてのフィルター値を削除する簡単なメカニズムを備え、またフィルター値のよりコンパクトで直感的な視覚化を実現します。</span><span class="sxs-lookup"><span data-stu-id="0ad56-119">Optimized "is one of" filtering experience - This feature enables an optimized "is one of" filtering experience that makes it easier to enter multiple filter values, has a simpler mechanism to remove individual or all filter values, and has a more compact and intuitive visualization of filter values.</span></span>

- <span data-ttu-id="0ad56-120">推奨されるフィールド - ユーザーは、多くの場合、グリッドまたはページにフィールドを追加する必要があります。</span><span class="sxs-lookup"><span data-stu-id="0ad56-120">Recommended fields - Users often need to add fields to a grid or page.</span></span> <span data-ttu-id="0ad56-121">多数の使用可能なフィールドでは、これは困難になることがあります。</span><span class="sxs-lookup"><span data-stu-id="0ad56-121">This can be difficult with so many available fields.</span></span> <span data-ttu-id="0ad56-122">この機能により、大きなリストを通じて検索する代わりに、システムは類似のシナリオでほかのユーザーが最も頻繁に追加する内容に基づいて、一連の推奨されるフィールドを表示することが有効になります。</span><span class="sxs-lookup"><span data-stu-id="0ad56-122">Instead of having to search through a large list, this feature enables the system to surface a set of recommended fields based on what other users most often add in similar scenarios.</span></span>

- <span data-ttu-id="0ad56-123">グリッド内の既定の付箋アクション - この機能により、グリッド内の既定のアクションは、その列が移動または非表示のどちらであるかに関係なく、グリッド内の特定の列にリンクされます。</span><span class="sxs-lookup"><span data-stu-id="0ad56-123">Sticky default actions in grids - This feature ensures that the default action in a grid is linked to a specific column in a grid, regardless of whether that column is moved or hidden.</span></span>

## <a name="unable-to-adjust-leave-balance-for-a-plan-with-no-accruals-that-was-created-with-multiple-leave-type-feature-on-419635"></a><span data-ttu-id="0ad56-124">"複数の休暇タイプ" 機能を使用して作成された、見越計上のない計画の休暇残日数を調整できない (419635)</span><span class="sxs-lookup"><span data-stu-id="0ad56-124">Unable to adjust leave balance for a plan with no accruals that was created with "multiple leave type" feature on (419635)</span></span>

<span data-ttu-id="0ad56-125">この変更により、機能管理で 複数の休暇タイプ (プレビュー) 機能を有効にして作成した休暇計画の残日数を調整できます。</span><span class="sxs-lookup"><span data-stu-id="0ad56-125">With this change, you can adjust balances for leave plans that have been created with the Multiple leave type (Preview) feature enabled in feature management.</span></span>

## <a name="in-preview"></a><span data-ttu-id="0ad56-126">プレビュー</span><span class="sxs-lookup"><span data-stu-id="0ad56-126">In preview</span></span>

<span data-ttu-id="0ad56-127">次のプレビュー機能が 2020 年 2 月 3 日に利用可能になります。</span><span class="sxs-lookup"><span data-stu-id="0ad56-127">The following preview features became available on February 3, 2020:</span></span>

- <span data-ttu-id="0ad56-128">**休暇および欠勤のプレビュー機能** - 詳細については、[休暇および欠勤のプレビュー機能](hr-leave-and-absence-overview.md?leave-and-absence-preview-features) を参照してください。</span><span class="sxs-lookup"><span data-stu-id="0ad56-128">**Leave and absence preview features** - For more information, see [Leave and absence preview features](hr-leave-and-absence-overview.md?leave-and-absence-preview-features).</span></span>

- <span data-ttu-id="0ad56-129">**福利厚生管理プレビュー機能** - 既知の問題など、詳細については[福利厚生管理の概要](hr-benefits-management-overview.md)を参照してください。</span><span class="sxs-lookup"><span data-stu-id="0ad56-129">**Benefits management preview feature** - For more information, including known issues, see [Benefits management overview](hr-benefits-management-overview.md).</span></span>

## <a name="dataverse-solution-is-now-available-with-the-following-changes"></a><span data-ttu-id="0ad56-130">Dataverse ソリューションが、次の変更で利用可能になりました。</span><span class="sxs-lookup"><span data-stu-id="0ad56-130">Dataverse solution is now available with the following changes:</span></span>

| <span data-ttu-id="0ad56-131">説明</span><span class="sxs-lookup"><span data-stu-id="0ad56-131">Description</span></span> | <span data-ttu-id="0ad56-132">計上額</span><span class="sxs-lookup"><span data-stu-id="0ad56-132">Change</span></span> |
| --- | --- |
| <span data-ttu-id="0ad56-133">**職務/職位** エンティティの変更</span><span class="sxs-lookup"><span data-stu-id="0ad56-133">**Job/Position** entity changes</span></span> | <ul><li><span data-ttu-id="0ad56-134">追加された **報酬地域**</span><span class="sxs-lookup"><span data-stu-id="0ad56-134">**Compensation region** added</span></span></li>|
| <span data-ttu-id="0ad56-135">追加された **職務職位分析** エンティティ</span><span class="sxs-lookup"><span data-stu-id="0ad56-135">**Job position dimension** entity added</span></span> | <ul><li><span data-ttu-id="0ad56-136">追加された **財務分析コード**</span><span class="sxs-lookup"><span data-stu-id="0ad56-136">**Financial dimensions** added</span></span></li>
| <span data-ttu-id="0ad56-137">**作業者** エンティティの変更</span><span class="sxs-lookup"><span data-stu-id="0ad56-137">**Worker** entity changes</span></span> | <ul><li><span data-ttu-id="0ad56-138">追加された **名前の順序**</span><span class="sxs-lookup"><span data-stu-id="0ad56-138">**Name sequence** added</span></span></li><li><span data-ttu-id="0ad56-139">追加された **自宅から作業**</span><span class="sxs-lookup"><span data-stu-id="0ad56-139">**Works from home** added</span></span></li><li><span data-ttu-id="0ad56-140">追加された **言語**</span><span class="sxs-lookup"><span data-stu-id="0ad56-140">**Language** added</span></span></li><li><span data-ttu-id="0ad56-141">追加された **勤続日数**</span><span class="sxs-lookup"><span data-stu-id="0ad56-141">**Seniority date** added</span></span></li><li><span data-ttu-id="0ad56-142">追加された **記念日**</span><span class="sxs-lookup"><span data-stu-id="0ad56-142">**Anniversary date** added</span></span></li><li><span data-ttu-id="0ad56-143">追加された **元の採用日付**</span><span class="sxs-lookup"><span data-stu-id="0ad56-143">**Original hire date** added</span></span></li></ul> |
| <span data-ttu-id="0ad56-144">**雇用** エンティティの変更</span><span class="sxs-lookup"><span data-stu-id="0ad56-144">**Employment** entity changes</span></span> | <ul><li><span data-ttu-id="0ad56-145">追加された **財務分析コード**</span><span class="sxs-lookup"><span data-stu-id="0ad56-145">**Financial dimensions** added</span></span></li><li><span data-ttu-id="0ad56-146">追加された **退職理由**</span><span class="sxs-lookup"><span data-stu-id="0ad56-146">**Termination reason** added</span></span></li><li><span data-ttu-id="0ad56-147">**移行日** から名前変更された **退職日**</span><span class="sxs-lookup"><span data-stu-id="0ad56-147">**Termination date** renamed from **Transition date**</span></span></li><li><span data-ttu-id="0ad56-148">追加された **猶予期間**</span><span class="sxs-lookup"><span data-stu-id="0ad56-148">**Probation date** added</span></span></li></ul> |
| <span data-ttu-id="0ad56-149">**作業者住所** エンティティの変更</span><span class="sxs-lookup"><span data-stu-id="0ad56-149">**Worker address** entity changes</span></span> | <ul><li><span data-ttu-id="0ad56-150">追加された **番地**</span><span class="sxs-lookup"><span data-stu-id="0ad56-150">**Street address** added</span></span></li><li><span data-ttu-id="0ad56-151">廃止としてマークされた **住所行 1**、**住所行 2**、および **住所行 3**</span><span class="sxs-lookup"><span data-stu-id="0ad56-151">**Address line 1**, **Address line 2**, and **Address line 3** marked for deprecation</span></span></li></ul> |
| <span data-ttu-id="0ad56-152">新しい変動報酬の設定エンティティ</span><span class="sxs-lookup"><span data-stu-id="0ad56-152">New variable compensation setup entities</span></span> | <ul><li><span data-ttu-id="0ad56-153">**変動報酬プラン タイプ**</span><span class="sxs-lookup"><span data-stu-id="0ad56-153">**Compensation variable plan type**</span></span></li><li><span data-ttu-id="0ad56-154">**変動報酬プラン**</span><span class="sxs-lookup"><span data-stu-id="0ad56-154">**Compensation variable plan**</span></span></li><li><span data-ttu-id="0ad56-155">**給付ルール**</span><span class="sxs-lookup"><span data-stu-id="0ad56-155">**Vesting rules**</span></span></li><li><span data-ttu-id="0ad56-156">**変動報酬プラン レベル**</span><span class="sxs-lookup"><span data-stu-id="0ad56-156">**Compensation variable plan level**</span></span></li></ul> |
| <span data-ttu-id="0ad56-157">新しい **作業者カレンダー雇用** エンティティ</span><span class="sxs-lookup"><span data-stu-id="0ad56-157">New **Worker calendar employment** entity</span></span> | <ul><li><span data-ttu-id="0ad56-158">追加された **作業カレンダー エンティティ**</span><span class="sxs-lookup"><span data-stu-id="0ad56-158">**Work calendar entity** added</span></span></li></ul> |
| <span data-ttu-id="0ad56-159">新しい **給与職位詳細** エンティティ</span><span class="sxs-lookup"><span data-stu-id="0ad56-159">New **Payroll position detail** entity</span></span> | <ul><li><span data-ttu-id="0ad56-160">追加された **給与職位詳細**</span><span class="sxs-lookup"><span data-stu-id="0ad56-160">**Payroll position detail** added</span></span></li></ul> |
| <span data-ttu-id="0ad56-161">新しい **肩書** エンティティ</span><span class="sxs-lookup"><span data-stu-id="0ad56-161">New **Title** entity</span></span> | <ul><li><span data-ttu-id="0ad56-162">追加された **タイトル**</span><span class="sxs-lookup"><span data-stu-id="0ad56-162">**Title** added</span></span></li></ul><span data-ttu-id="0ad56-163">新しい **タイトル** エンティティは Dataverse に含まれますが、この時点では **職位** または **職務** エンティティから参照されません。</span><span class="sxs-lookup"><span data-stu-id="0ad56-163">The new **Title** entity is included in Dataverse but isn't referenced from the **Job Position** or **Job** entities at this time.</span></span> |

> [!NOTE]
> <span data-ttu-id="0ad56-164">職位と雇用どちらの財務分析コードは、Human Resources から Dataverse への更新の一方向の統合を提供します。</span><span class="sxs-lookup"><span data-stu-id="0ad56-164">Financial dimensions for both positions and employment provide one-direction integration for updates from Human Resources to Dataverse.</span></span> <span data-ttu-id="0ad56-165">財務分析コードの更新は、現在 Dataverse から Human Resources へは同期されません。</span><span class="sxs-lookup"><span data-stu-id="0ad56-165">Financial dimensions updates don't currently synchronize from Dataverse to Human Resources.</span></span>

<span data-ttu-id="0ad56-166">今後数週間のうちに、これらのエンティティの変更がすべての環境で使用できるようになります。</span><span class="sxs-lookup"><span data-stu-id="0ad56-166">Over the next few weeks, these entity changes will be available in all environments.</span></span> <span data-ttu-id="0ad56-167">Human Resources の最新 Dataverse ソリューションを手動でインストールするには、次の操作を行います。</span><span class="sxs-lookup"><span data-stu-id="0ad56-167">To manually install the latest Dataverse solution for Human Resources:</span></span>

1.  <span data-ttu-id="0ad56-168">[Power Platform 管理センター](https://admin.powerplatform.microsoft.com) に移動します。</span><span class="sxs-lookup"><span data-stu-id="0ad56-168">Go to the [Power Platform Admin Center](https://admin.powerplatform.microsoft.com).</span></span>

2.  <span data-ttu-id="0ad56-169">**環境** を選択します。</span><span class="sxs-lookup"><span data-stu-id="0ad56-169">Select **Environments**.</span></span>

3.  <span data-ttu-id="0ad56-170">アップグレードする環境を検索します。</span><span class="sxs-lookup"><span data-stu-id="0ad56-170">Find the environment you want to upgrade.</span></span> <span data-ttu-id="0ad56-171">環境は、Human Resources の **バージョン情報** フォームで、**Common Data Service 情報** セクションの **環境名** に対応している必要があります。</span><span class="sxs-lookup"><span data-stu-id="0ad56-171">The environment should correspond to **Environment name** in the **Common Data Service information** section in the **About** form in Human Resources.</span></span>

4.  <span data-ttu-id="0ad56-172">環境の詳細を表示するための環境を選択します。</span><span class="sxs-lookup"><span data-stu-id="0ad56-172">Select the environment to view the environment details.</span></span>

5.  <span data-ttu-id="0ad56-173">上部の操作バーで、**ソリューションの管理** を選択します。</span><span class="sxs-lookup"><span data-stu-id="0ad56-173">In the action bar at the top, select **Manage Solutions**.</span></span> <span data-ttu-id="0ad56-174">新しいブラウザー ウィンドウが開き、環境のコンテキストで **Dynamics 365 管理センター** に移動します。</span><span class="sxs-lookup"><span data-stu-id="0ad56-174">A new browser window will open and navigate to **Dynamics 365 Administration Center** in the context of your environment.</span></span>

6.  <span data-ttu-id="0ad56-175">**ソリューション** リストで、**Dynamics 365 Human Resources アンカー** を選択します。</span><span class="sxs-lookup"><span data-stu-id="0ad56-175">In the **Solution** list, select **Dynamics 365 Human Resources Anchor**.</span></span>

7.  <span data-ttu-id="0ad56-176">最新のソリューションを適用するには、**アップグレード** を選択します。</span><span class="sxs-lookup"><span data-stu-id="0ad56-176">Select **Upgrade** to apply the latest solution.</span></span>

## <a name="sharepoint-preview-doesnt-work-in-some-environments"></a><span data-ttu-id="0ad56-177">一部の環境で、SharePoint プレビューが機能しない</span><span class="sxs-lookup"><span data-stu-id="0ad56-177">SharePoint preview doesn't work in some environments</span></span>

<span data-ttu-id="0ad56-178">SharePoint で保存されているドキュメントのドキュメント プレビューが機能しない場合は、次の手順を実行します。</span><span class="sxs-lookup"><span data-stu-id="0ad56-178">If document preview for documents stored in SharePoint doesn't work, try the following procedure:</span></span>

1. <span data-ttu-id="0ad56-179">管理者のユーザー アカウントにユーザー レコードに関連付けられたメールがあることを確認します。</span><span class="sxs-lookup"><span data-stu-id="0ad56-179">Verify the Admin user account has an email associated with the user record.</span></span> <span data-ttu-id="0ad56-180">この情報は、**ユーザー** ページで確認できます。</span><span class="sxs-lookup"><span data-stu-id="0ad56-180">You can view this information in the **User** page.</span></span> <span data-ttu-id="0ad56-181">メールが設定されていない場合は、OData Excel アドインを使用してメールとプロバイダーを追加する必要があります。</span><span class="sxs-lookup"><span data-stu-id="0ad56-181">If email isn't set up, you need to add the email and provider with the OData Excel add-in.</span></span> <span data-ttu-id="0ad56-182">既定では、Excel デザインにメール アドレスは表示されません。</span><span class="sxs-lookup"><span data-stu-id="0ad56-182">By default, the email address isn't present in the Excel design.</span></span> <span data-ttu-id="0ad56-183">Excel デザインを編集し、すべてのフィールドを追加し、適用して更新する必要があります。</span><span class="sxs-lookup"><span data-stu-id="0ad56-183">You'll need to edit the Excel design, add all fields, apply, and refresh.</span></span> <span data-ttu-id="0ad56-184">これらのステップを完了すると、管理者アカウントを更新できます。</span><span class="sxs-lookup"><span data-stu-id="0ad56-184">Once you've completed those steps, you can update the admin account.</span></span>

2. <span data-ttu-id="0ad56-185">管理者アカウントにメール アカウントが関連付けられたら、人事管理に管理者としてサインインします。</span><span class="sxs-lookup"><span data-stu-id="0ad56-185">After the Admin account has an associated email account, sign in to Human Resources with Admin credentials.</span></span>

3. <span data-ttu-id="0ad56-186">SharePoint で添付ファイルにアクセスして、ドキュメントのプレビューを開始します。</span><span class="sxs-lookup"><span data-stu-id="0ad56-186">Access an attachment in SharePoint to start the document preview.</span></span>

4. <span data-ttu-id="0ad56-187">添付ファイルにアクセスできる他のユーザー アカウントでサインインし、適切にプレビューが機能することを確認します。</span><span class="sxs-lookup"><span data-stu-id="0ad56-187">Sign in with another user account that has access to attachments and verify that the preview works as expected.</span></span>

## <a name="coming-soon"></a><span data-ttu-id="0ad56-188">間もなく公開</span><span class="sxs-lookup"><span data-stu-id="0ad56-188">Coming Soon</span></span>

## <a name="new-production-release-cadence"></a><span data-ttu-id="0ad56-189">新しい生産リリース リズム</span><span class="sxs-lookup"><span data-stu-id="0ad56-189">New production release cadence</span></span>

<span data-ttu-id="0ad56-190">4 月から、Human Resources のリリース頻度は、毎週更新から隔週更新に移行します。</span><span class="sxs-lookup"><span data-stu-id="0ad56-190">Beginning in April, the release cadence for Human Resources will shift from a weekly update to a bi-weekly update.</span></span> <span data-ttu-id="0ad56-191">安全な展開プラクティスとの整合性を確保し、サービスの安定性と信頼性の高い標準を維持するために、すべての地域にサービス更新を展開するプロセスは 2 週間で展開されます。</span><span class="sxs-lookup"><span data-stu-id="0ad56-191">To ensure alignment with safe deployment practices, and maintain high standards of stability and reliability in the service, the process of deploying service updates to all regions will be a two-week rollout.</span></span> <span data-ttu-id="0ad56-192">プロセスの各ステージで展開が成功したことを確認するために、追加のテストとモニターが実行されます。</span><span class="sxs-lookup"><span data-stu-id="0ad56-192">Additional testing and monitors will be in place to verify successful deployment at each stage of the process.</span></span> <span data-ttu-id="0ad56-193">リリース頻度の詳細については、[更新プロセス](hr-admin-setup-update-process.md) を参照してください。</span><span class="sxs-lookup"><span data-stu-id="0ad56-193">For more information on the release cadence, see [Update process](hr-admin-setup-update-process.md).</span></span>

## <a name="known-issues"></a><span data-ttu-id="0ad56-194">既知の問題</span><span class="sxs-lookup"><span data-stu-id="0ad56-194">Known issues</span></span>

## <a name="employment-detail-entity"></a><span data-ttu-id="0ad56-195">雇用の詳細エンティティ</span><span class="sxs-lookup"><span data-stu-id="0ad56-195">Employment Detail entity</span></span>

<span data-ttu-id="0ad56-196">**雇用の詳細** エンティティが、次のフィールドで更新されました: **PayFrequency**、**雇用カテゴリ ID**、**雇用タイプ**、**EmploymentType ID**、**福利厚生の雇用状況**。</span><span class="sxs-lookup"><span data-stu-id="0ad56-196">The **Employment Detail** entity has been updated with the following fields: **PayFrequency**, **Employment Category ID**, **Employment Type**, **EmploymentType ID**, and **Benefit Employment Status**.</span></span> <span data-ttu-id="0ad56-197">これらのフィールドの設定データは、機能管理で有効になっている福利厚生の管理に依存します。</span><span class="sxs-lookup"><span data-stu-id="0ad56-197">The setup data for these fields rely on benefits management being enabled in Feature management.</span></span> <span data-ttu-id="0ad56-198">これらのフィールドは、インポート中にエラーが発生するため、**雇用の詳細** エンティティで入力または更新しないでください。</span><span class="sxs-lookup"><span data-stu-id="0ad56-198">These fields shouldn't be populated or updated in the **Employment Detail** entity, because it will result in errors during import.</span></span>

## <a name="see-also"></a><span data-ttu-id="0ad56-199">参照</span><span class="sxs-lookup"><span data-stu-id="0ad56-199">See also</span></span>

[<span data-ttu-id="0ad56-200">Human Resources の新機能および変更された機能</span><span class="sxs-lookup"><span data-stu-id="0ad56-200">What's new or changed in Human Resources</span></span>](hr-admin-whats-new.md)</br>
[<span data-ttu-id="0ad56-201">Dynamics 365 Human Resources 2019 のリリース ウェーブ 2 の概要</span><span class="sxs-lookup"><span data-stu-id="0ad56-201">Overview of Dynamics 365 Human Resources 2019 release wave 2</span></span>](https://docs.microsoft.com/dynamics365-release-plan/2019wave2/dynamics365-human-resources/)</br>
[<span data-ttu-id="0ad56-202">更新プロセス</span><span class="sxs-lookup"><span data-stu-id="0ad56-202">Update process</span></span>](hr-admin-setup-update-process.md)</br>
[<span data-ttu-id="0ad56-203">機能の管理</span><span class="sxs-lookup"><span data-stu-id="0ad56-203">Manage features</span></span>](hr-admin-manage-features.md)