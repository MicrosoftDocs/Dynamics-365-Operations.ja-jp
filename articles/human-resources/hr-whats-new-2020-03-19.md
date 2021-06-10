---
title: Dynamics 365 Human Resources の新機能および変更された機能 (2020 年 3 月 19 日)
description: この記事では、2020 年 3 月 19 日に更新された Microsoft Dynamics 365 Human Resources の新機能、または変更された機能について説明します。
author: andreabichsel
ms.date: 03/19/2020
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
ms.search.validFrom: 2020-03-19
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: 2882eca5c0823d413ca3242069c5ba47b985c2a8
ms.sourcegitcommit: 879ee8a10e6158885795dce4b3db5077540eec41
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 05/18/2021
ms.locfileid: "6051164"
---
# <a name="whats-new-or-changed-in-dynamics-365-human-resources-march-19-2020"></a><span data-ttu-id="39324-103">Dynamics 365 Human Resources の新機能および変更された機能 (2020 年 3 月 19 日)</span><span class="sxs-lookup"><span data-stu-id="39324-103">What's new or changed in Dynamics 365 Human Resources (March 19, 2020)</span></span>

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

[!include [rename-banner](~/includes/cc-data-platform-banner.md)]

<span data-ttu-id="39324-104">この記事では、Dynamics 365 Human Resources の新機能および変更された機能について説明します。</span><span class="sxs-lookup"><span data-stu-id="39324-104">This article describes features that are either new or changed in Dynamics 365 Human Resources.</span></span> <span data-ttu-id="39324-105">変更は、ビルド番号 8.1.3014 に適用されます。</span><span class="sxs-lookup"><span data-stu-id="39324-105">Changes apply to build number 8.1.3014.</span></span> <span data-ttu-id="39324-106">一部のヘッダーにあるかっこ内の数字は、参照用に Lifecycle Services (LCS) のサポート番号を参照しています。</span><span class="sxs-lookup"><span data-stu-id="39324-106">The numbers in parentheses in some headings refer to Lifecycle Services (LCS) support numbers for reference.</span></span>

## <a name="human-resources-environment-limits-are-now-based-on-updated-licensing-394595"></a><span data-ttu-id="39324-107">人事管理環境の制限は、現在、更新されたライセンスに基づいている (394595)</span><span class="sxs-lookup"><span data-stu-id="39324-107">Human Resources environment limits are now based on updated licensing (394595)</span></span>

<span data-ttu-id="39324-108">Lifecycle Services (LCS) のプロジェクトあたりの環境数の制限が変更されました。</span><span class="sxs-lookup"><span data-stu-id="39324-108">The limit on the number of environments per project in Lifecycle Services (LCS) has changed.</span></span> <span data-ttu-id="39324-109">以前の制限は 2 つの環境でした。</span><span class="sxs-lookup"><span data-stu-id="39324-109">The previous limit was two environments.</span></span> <span data-ttu-id="39324-110">LCS で人事管理用に作成できる運用環境とサンドボックス環境の数の制限は、更新されたライセンスに基づいています。</span><span class="sxs-lookup"><span data-stu-id="39324-110">The limit on the number of production and sandbox environments you can create for Human Resources in LCS is now based on updated licensing.</span></span> <span data-ttu-id="39324-111">購入したライセンスの数に応じて、LCS プロジェクトごとに必要な数の環境を作成できるようになりました。</span><span class="sxs-lookup"><span data-stu-id="39324-111">You can now create as many environments as needed per LCS project, depending on the number of licenses purchased.</span></span> <span data-ttu-id="39324-112">2020 年 2 月 1 日に更新された新しいライセンスでは、顧客は追加の環境を購入できます。</span><span class="sxs-lookup"><span data-stu-id="39324-112">The new licensing, updated on February 1, 2020, allows customers to purchase additional environments.</span></span> <span data-ttu-id="39324-113">追加の環境のライセンス要件の詳細については、[Dynamics 365 ライセンスガイド](https://dynamics.microsoft.com/pricing/#HumanResources) を参照してください。</span><span class="sxs-lookup"><span data-stu-id="39324-113">For more information about licensing requirements for additional environments, see [Dynamics 365 Licensing Guide](https://dynamics.microsoft.com/pricing/#HumanResources).</span></span>

## <a name="provide-cross-company-viewing-of-compensation-data-for-employees-and-managers-403904"></a><span data-ttu-id="39324-114">従業員とマネージャーの報酬データを会社表示する (403904)</span><span class="sxs-lookup"><span data-stu-id="39324-114">Provide cross company viewing of compensation data for employees and managers (403904)</span></span>

<span data-ttu-id="39324-115">**機能の管理** ワークスペースで、この機能を有効にします。</span><span class="sxs-lookup"><span data-stu-id="39324-115">Turn on this feature in the **Feature management** workspace.</span></span> <span data-ttu-id="39324-116">詳細は、[プレビュー機能を有効または無効にする](hr-admin-manage-features.md#enable-or-disable-preview-features) を参照してください。</span><span class="sxs-lookup"><span data-stu-id="39324-116">For more information, see [Enable or disable preview features](hr-admin-manage-features.md#enable-or-disable-preview-features).</span></span>

<span data-ttu-id="39324-117">この機能を有効にすると、マネージャーは雇用のある会社にログインすることなく、直属の部下および拡張レポートの報酬を表示することができます。</span><span class="sxs-lookup"><span data-stu-id="39324-117">When you enable this feature, managers can see direct and extended reports compensation without having to sign into the company of employment.</span></span> <span data-ttu-id="39324-118">完全な報酬履歴は、マネージャーがアクセスできるログインしている会社から入手できます。</span><span class="sxs-lookup"><span data-stu-id="39324-118">Full compensation history is available from any signed in company the manager can access.</span></span> <span data-ttu-id="39324-119">詳細については、[従業員およびマネージャー セルフサービスの概要](hr-employee-manager-self-service-overview.md) を参照してください。</span><span class="sxs-lookup"><span data-stu-id="39324-119">For more information, see [Employee and Manager self service overview](hr-employee-manager-self-service-overview.md).</span></span>

## <a name="enable-global-address-book-merge-functionality-427189"></a><span data-ttu-id="39324-120">グローバル アドレス帳のマージ機能を有効にする (427189)</span><span class="sxs-lookup"><span data-stu-id="39324-120">Enable global address book merge functionality (427189)</span></span>

<span data-ttu-id="39324-121">重複するアドレス帳エントリをマージするには、重複するレコードを選択して、**グローバル アドレス帳** ページから選択し、**マージ** を選択します。</span><span class="sxs-lookup"><span data-stu-id="39324-121">You can now merge duplicate address book entries by selecting the duplicate records and choosing **Merge** from the **Global address book** page.</span></span>

## <a name="unable-to-adjust-leave-balance-for-a-plan-with-no-accruals-that-was-created-with-the-multiple-leave-type-feature-on-419635"></a><span data-ttu-id="39324-122">複数の休暇タイプ機能を使用して作成された、見越計上のない計画の休暇残高を調整できない (419635)</span><span class="sxs-lookup"><span data-stu-id="39324-122">Unable to adjust leave balance for a plan with no accruals that was created with the Multiple leave type feature on (419635)</span></span>

<span data-ttu-id="39324-123">ここで、機能管理で **複数の休暇タイプ** プレビュー機能を有効にして作成した休暇計画の残高を調整できます。</span><span class="sxs-lookup"><span data-stu-id="39324-123">You can now adjust balances for leave plans that were created with the **Multiple leave type** preview feature enabled in Feature management.</span></span>

## <a name="primary-position-field-in-the-workerpositionassignmententity-when-an-employee-is-terminated-420774"></a><span data-ttu-id="39324-124">従業員が退職したときの WorkerPositionAssignmentEntity の基本職位フィールド (420774)</span><span class="sxs-lookup"><span data-stu-id="39324-124">Primary position field in the WorkerPositionAssignmentEntity when an employee is terminated (420774)</span></span>

<span data-ttu-id="39324-125">雇用が終了した従業員については、退職時にアクティブだった基本職位がエンティティに表示されます。</span><span class="sxs-lookup"><span data-stu-id="39324-125">For employees with a terminated employment, the primary position that was active at the time of termination is displayed in the entity.</span></span> <span data-ttu-id="39324-126">統合の場合は、その従業員の作業者の職位割り当てに対して重複するレコードが作成されなくなります。</span><span class="sxs-lookup"><span data-stu-id="39324-126">For integrations, a duplicate record will no longer be created for the employee’s worker position assignment.</span></span> 

## <a name="dataverse-solution-is-now-available-with-the-following-changes"></a><span data-ttu-id="39324-127">Dataverse ソリューションが、次の変更で利用可能になりました。</span><span class="sxs-lookup"><span data-stu-id="39324-127">Dataverse solution is now available with the following changes:</span></span>

| <span data-ttu-id="39324-128">説明</span><span class="sxs-lookup"><span data-stu-id="39324-128">Description</span></span> | <span data-ttu-id="39324-129">計上額</span><span class="sxs-lookup"><span data-stu-id="39324-129">Change</span></span> |
| --- | --- |
| <span data-ttu-id="39324-130">**職務/職位** エンティティの変更</span><span class="sxs-lookup"><span data-stu-id="39324-130">**Job/Position** entity changes</span></span> | <ul><li><span data-ttu-id="39324-131">追加された **報酬地域**</span><span class="sxs-lookup"><span data-stu-id="39324-131">**Compensation region** added</span></span></li>|
| <span data-ttu-id="39324-132">追加された **職務職位分析** エンティティ</span><span class="sxs-lookup"><span data-stu-id="39324-132">**Job position dimension** entity added</span></span> | <ul><li><span data-ttu-id="39324-133">追加された **財務分析コード**</span><span class="sxs-lookup"><span data-stu-id="39324-133">**Financial dimensions** added</span></span></li>
| <span data-ttu-id="39324-134">**作業者** エンティティの変更</span><span class="sxs-lookup"><span data-stu-id="39324-134">**Worker** entity changes</span></span> | <ul><li><span data-ttu-id="39324-135">追加された **名前の順序**</span><span class="sxs-lookup"><span data-stu-id="39324-135">**Name sequence** added</span></span></li><li><span data-ttu-id="39324-136">追加された **自宅から作業**</span><span class="sxs-lookup"><span data-stu-id="39324-136">**Works from home** added</span></span></li><li><span data-ttu-id="39324-137">追加された **言語**</span><span class="sxs-lookup"><span data-stu-id="39324-137">**Language** added</span></span></li><li><span data-ttu-id="39324-138">追加された **勤続日数**</span><span class="sxs-lookup"><span data-stu-id="39324-138">**Seniority date** added</span></span></li><li><span data-ttu-id="39324-139">追加された **記念日**</span><span class="sxs-lookup"><span data-stu-id="39324-139">**Anniversary date** added</span></span></li><li><span data-ttu-id="39324-140">追加された **元の採用日付**</span><span class="sxs-lookup"><span data-stu-id="39324-140">**Original hire date** added</span></span></li></ul> |
| <span data-ttu-id="39324-141">**雇用** エンティティの変更</span><span class="sxs-lookup"><span data-stu-id="39324-141">**Employment** entity changes</span></span> | <ul><li><span data-ttu-id="39324-142">追加された **財務分析コード**</span><span class="sxs-lookup"><span data-stu-id="39324-142">**Financial dimensions** added</span></span></li><li><span data-ttu-id="39324-143">追加された **退職理由**</span><span class="sxs-lookup"><span data-stu-id="39324-143">**Termination reason** added</span></span></li><li><span data-ttu-id="39324-144">**移行日** から名前変更された **退職日**</span><span class="sxs-lookup"><span data-stu-id="39324-144">**Termination date** renamed from **Transition date**</span></span></li><li><span data-ttu-id="39324-145">追加された **猶予期間**</span><span class="sxs-lookup"><span data-stu-id="39324-145">**Probation date** added</span></span></li></ul> |
| <span data-ttu-id="39324-146">**作業者住所** エンティティの変更</span><span class="sxs-lookup"><span data-stu-id="39324-146">**Worker address** entity changes</span></span> | <ul><li><span data-ttu-id="39324-147">追加された **番地**</span><span class="sxs-lookup"><span data-stu-id="39324-147">**Street address** added</span></span></li><li><span data-ttu-id="39324-148">廃止としてマークされた **住所行 1**、**住所行 2**、および **住所行 3**</span><span class="sxs-lookup"><span data-stu-id="39324-148">**Address line 1**, **Address line 2**, and **Address line 3** marked for deprecation</span></span></li></ul> |
| <span data-ttu-id="39324-149">新しい変動報酬の設定エンティティ</span><span class="sxs-lookup"><span data-stu-id="39324-149">New variable compensation setup entities</span></span> | <ul><li><span data-ttu-id="39324-150">**変動報酬プラン タイプ**</span><span class="sxs-lookup"><span data-stu-id="39324-150">**Compensation variable plan type**</span></span></li><li><span data-ttu-id="39324-151">**変動報酬プラン**</span><span class="sxs-lookup"><span data-stu-id="39324-151">**Compensation variable plan**</span></span></li><li><span data-ttu-id="39324-152">**給付ルール**</span><span class="sxs-lookup"><span data-stu-id="39324-152">**Vesting rules**</span></span></li><li><span data-ttu-id="39324-153">**変動報酬プラン レベル**</span><span class="sxs-lookup"><span data-stu-id="39324-153">**Compensation variable plan level**</span></span></li></ul> |
| <span data-ttu-id="39324-154">新しい **作業者カレンダー雇用** エンティティ</span><span class="sxs-lookup"><span data-stu-id="39324-154">New **Worker calendar employment** entity</span></span> | <ul><li><span data-ttu-id="39324-155">追加された **作業カレンダー エンティティ**</span><span class="sxs-lookup"><span data-stu-id="39324-155">**Work calendar entity** added</span></span></li></ul> |
| <span data-ttu-id="39324-156">新しい **給与職位詳細** エンティティ</span><span class="sxs-lookup"><span data-stu-id="39324-156">New **Payroll position detail** entity</span></span> | <ul><li><span data-ttu-id="39324-157">追加された **給与職位詳細**</span><span class="sxs-lookup"><span data-stu-id="39324-157">**Payroll position detail** added</span></span></li></ul> |
| <span data-ttu-id="39324-158">新しい **肩書** エンティティ</span><span class="sxs-lookup"><span data-stu-id="39324-158">New **Title** entity</span></span> | <ul><li><span data-ttu-id="39324-159">追加された **タイトル**</span><span class="sxs-lookup"><span data-stu-id="39324-159">**Title** added</span></span></li></ul><span data-ttu-id="39324-160">新しい **タイトル** エンティティは Dataverse に含まれますが、この時点では **職位** または **職務** エンティティから参照されません。</span><span class="sxs-lookup"><span data-stu-id="39324-160">The new **Title** entity is included in Dataverse but isn't referenced from the **Job Position** or **Job** entities at this time.</span></span> |

> [!NOTE]
> <span data-ttu-id="39324-161">職位と雇用どちらの財務分析コードは、Human Resources から Dataverse への更新の一方向の統合を提供します。</span><span class="sxs-lookup"><span data-stu-id="39324-161">Financial dimensions for both positions and employment provide one-direction integration for updates from Human Resources to Dataverse.</span></span> <span data-ttu-id="39324-162">財務分析コードの更新は、現在 Dataverse から Human Resources へは同期されません。</span><span class="sxs-lookup"><span data-stu-id="39324-162">Financial dimensions updates don't currently synchronize from Dataverse to Human Resources.</span></span>

<span data-ttu-id="39324-163">今後数週間のうちに、これらのエンティティの変更がすべての環境で使用できるようになります。</span><span class="sxs-lookup"><span data-stu-id="39324-163">Over the next few weeks, these entity changes will be available in all environments.</span></span> <span data-ttu-id="39324-164">Human Resources の最新 Dataverse ソリューションを手動でインストールするには、次の操作を行います。</span><span class="sxs-lookup"><span data-stu-id="39324-164">To manually install the latest Dataverse solution for Human Resources:</span></span>

1.  <span data-ttu-id="39324-165">[Power Platform 管理センター](https://admin.powerplatform.microsoft.com) に移動します。</span><span class="sxs-lookup"><span data-stu-id="39324-165">Go to the [Power Platform Admin Center](https://admin.powerplatform.microsoft.com).</span></span>

2.  <span data-ttu-id="39324-166">**環境** を選択します。</span><span class="sxs-lookup"><span data-stu-id="39324-166">Select **Environments**.</span></span>

3.  <span data-ttu-id="39324-167">アップグレードする環境を検索します。</span><span class="sxs-lookup"><span data-stu-id="39324-167">Find the environment you want to upgrade.</span></span> <span data-ttu-id="39324-168">環境は、Human Resources の **バージョン情報** フォームで、**Common Data Service 情報** セクションの **環境名** に対応している必要があります。</span><span class="sxs-lookup"><span data-stu-id="39324-168">The environment should correspond to **Environment name** in the **Common Data Service information** section in the **About** form in Human Resources.</span></span>

4.  <span data-ttu-id="39324-169">環境の詳細を表示するための環境を選択します。</span><span class="sxs-lookup"><span data-stu-id="39324-169">Select the environment to view the environment details.</span></span>

5.  <span data-ttu-id="39324-170">上部の操作バーで、**ソリューションの管理** を選択します。</span><span class="sxs-lookup"><span data-stu-id="39324-170">In the action bar at the top, select **Manage Solutions**.</span></span> <span data-ttu-id="39324-171">新しいブラウザー ウィンドウが開き、環境のコンテキストで **Dynamics 365 管理センター** に移動します。</span><span class="sxs-lookup"><span data-stu-id="39324-171">A new browser window will open and navigate to **Dynamics 365 Administration Center** in the context of your environment.</span></span>

6.  <span data-ttu-id="39324-172">**ソリューション** リストで、**Dynamics 365 Human Resources アンカー** を選択します。</span><span class="sxs-lookup"><span data-stu-id="39324-172">In the **Solution** list, select **Dynamics 365 Human Resources Anchor**.</span></span>

7.  <span data-ttu-id="39324-173">最新のソリューションを適用するには、**アップグレード** を選択します。</span><span class="sxs-lookup"><span data-stu-id="39324-173">Select **Upgrade** to apply the latest solution.</span></span>

## <a name="sharepoint-preview-doesnt-work-in-some-environments"></a><span data-ttu-id="39324-174">一部の環境で、SharePoint プレビューが機能しない</span><span class="sxs-lookup"><span data-stu-id="39324-174">SharePoint preview doesn't work in some environments</span></span>

<span data-ttu-id="39324-175">SharePoint で保存されているドキュメントのドキュメント プレビューが機能しない場合は、次の手順を実行します。</span><span class="sxs-lookup"><span data-stu-id="39324-175">If document preview for documents stored in SharePoint doesn't work, try the following procedure:</span></span>

1. <span data-ttu-id="39324-176">管理者のユーザー アカウントにユーザー レコードに関連付けられたメールがあることを確認します。</span><span class="sxs-lookup"><span data-stu-id="39324-176">Verify the Admin user account has an email associated with the user record.</span></span> <span data-ttu-id="39324-177">この情報は、**ユーザー** ページで確認できます。</span><span class="sxs-lookup"><span data-stu-id="39324-177">You can view this information in the **User** page.</span></span> <span data-ttu-id="39324-178">メールが設定されていない場合は、OData Excel アドインを使用してメールとプロバイダーを追加する必要があります。</span><span class="sxs-lookup"><span data-stu-id="39324-178">If email isn't set up, you need to add the email and provider with the OData Excel add-in.</span></span> <span data-ttu-id="39324-179">既定では、Excel デザインにメール アドレスは表示されません。</span><span class="sxs-lookup"><span data-stu-id="39324-179">By default, the email address isn't present in the Excel design.</span></span> <span data-ttu-id="39324-180">Excel デザインを編集し、すべてのフィールドを追加し、適用して更新する必要があります。</span><span class="sxs-lookup"><span data-stu-id="39324-180">You'll need to edit the Excel design, add all fields, apply, and refresh.</span></span> <span data-ttu-id="39324-181">これらのステップを完了すると、管理者アカウントを更新できます。</span><span class="sxs-lookup"><span data-stu-id="39324-181">Once you've completed those steps, you can update the admin account.</span></span>

2. <span data-ttu-id="39324-182">管理者アカウントにメール アカウントが関連付けられたら、人事管理に管理者としてサインインします。</span><span class="sxs-lookup"><span data-stu-id="39324-182">After the Admin account has an associated email account, sign in to Human Resources with Admin credentials.</span></span>

3. <span data-ttu-id="39324-183">SharePoint で添付ファイルにアクセスして、ドキュメントのプレビューを開始します。</span><span class="sxs-lookup"><span data-stu-id="39324-183">Access an attachment in SharePoint to start the document preview.</span></span>

4. <span data-ttu-id="39324-184">添付ファイルにアクセスできる他のユーザー アカウントでサインインし、適切にプレビューが機能することを確認します。</span><span class="sxs-lookup"><span data-stu-id="39324-184">Sign in with another user account that has access to attachments and verify that the preview works as expected.</span></span>

## <a name="coming-soon"></a><span data-ttu-id="39324-185">間もなく公開</span><span class="sxs-lookup"><span data-stu-id="39324-185">Coming Soon</span></span>

### <a name="platform-update-33"></a><span data-ttu-id="39324-186">プラットフォーム update 33</span><span class="sxs-lookup"><span data-stu-id="39324-186">Platform update 33</span></span>

- <span data-ttu-id="39324-187">フル ページ アプリ (プレビュー) - このプレビュー機能は、保存されたビュー機能を有効にする必要があり、ダッシュボードから Power Apps とサード パーティー アプリをフルページ エクスペリエンスとして追加できます。</span><span class="sxs-lookup"><span data-stu-id="39324-187">Full page apps (Preview) - This preview feature, which requires you to enable the Saved views feature, allows Power Apps and third-party apps to be added as full-page experiences via the dashboard.</span></span>

- <span data-ttu-id="39324-188">保存されているビュー (プレビュー) - このプレビュー機能はパーソナル化 サブシステムの大幅な拡張を提供する、保存されているビューを有効にします。</span><span class="sxs-lookup"><span data-stu-id="39324-188">Saved views (Preview) - This preview feature enables saved views, which provide a significant enhancement to the personalization subsystem.</span></span> <span data-ttu-id="39324-189">この機能により、ユーザーはページごとに複数の名前を付けた個人用設定を使用できます。</span><span class="sxs-lookup"><span data-stu-id="39324-189">This feature allows users to have multiple named sets of personalizations per page.</span></span> <span data-ttu-id="39324-190">セキュリティ ロールにビューを公開することもできます。</span><span class="sxs-lookup"><span data-stu-id="39324-190">You can also publish views to security roles.</span></span>

- <span data-ttu-id="39324-191">「次の値のいずれか」のフィルタリング結果を最適化 - この機能により、最適化された「いずれか」のフィルタリング結果が可能になり、複数のフィルター値の入力を容易にして、個々またはすべてのフィルター値を削除する簡単なメカニズムを備え、またフィルター値のよりコンパクトで直感的な視覚化を実現します。</span><span class="sxs-lookup"><span data-stu-id="39324-191">Optimized "is one of" filtering experience - This feature enables an optimized "is one of" filtering experience that makes it easier to enter multiple filter values, has a simpler mechanism to remove individual or all filter values, and has a more compact and intuitive visualization of filter values.</span></span>

- <span data-ttu-id="39324-192">推奨されるフィールド - ユーザーは、多くの場合、グリッドまたはページにフィールドを追加する必要があります。</span><span class="sxs-lookup"><span data-stu-id="39324-192">Recommended fields - Users often need to add fields to a grid or page.</span></span> <span data-ttu-id="39324-193">多数の使用可能なフィールドでは、これは困難になることがあります。</span><span class="sxs-lookup"><span data-stu-id="39324-193">This can be difficult with so many available fields.</span></span> <span data-ttu-id="39324-194">この機能により、大きなリストを通じて検索する代わりに、システムは類似のシナリオでほかのユーザーが最も頻繁に追加する内容に基づいて、一連の推奨されるフィールドを表示することが有効になります。</span><span class="sxs-lookup"><span data-stu-id="39324-194">Instead of having to search through a large list, this feature enables the system to surface a set of recommended fields based on what other users most often add in similar scenarios.</span></span>

- <span data-ttu-id="39324-195">グリッド内の既定の付箋アクション - この機能により、グリッド内の既定のアクションは、その列が移動または非表示のどちらであるかに関係なく、グリッド内の特定の列にリンクされます。</span><span class="sxs-lookup"><span data-stu-id="39324-195">Sticky default actions in grids - This feature ensures that the default action in a grid is linked to a specific column in a grid, regardless of whether that column is moved or hidden.</span></span>

## <a name="new-production-release-cadence"></a><span data-ttu-id="39324-196">新しい生産リリース リズム</span><span class="sxs-lookup"><span data-stu-id="39324-196">New production release cadence</span></span>

<span data-ttu-id="39324-197">4 月から、人事管理のリリース リズムは、毎週更新から隔週の更新に移行します。</span><span class="sxs-lookup"><span data-stu-id="39324-197">Beginning in April, the release cadence for Human Resources will shift from a weekly update to a biweekly update.</span></span> <span data-ttu-id="39324-198">これにより、安全な展開プラクティスでアラインメントを行い、サービスの安定性と信頼性の高い基準を維持することができます。</span><span class="sxs-lookup"><span data-stu-id="39324-198">This will ensure alignment with safe deployment practices and maintain high standards of stability and reliability in the service.</span></span> <span data-ttu-id="39324-199">プロセスの各ステージで成功した展開を確認するために、テストとモニターを追加で実行しています。</span><span class="sxs-lookup"><span data-stu-id="39324-199">We're putting additional testing and monitors in place to verify successful deployment at each stage of the process.</span></span> <span data-ttu-id="39324-200">リリース リズムの詳細については、[更新プロセス](hr-admin-setup-update-process.md) を参照してください。</span><span class="sxs-lookup"><span data-stu-id="39324-200">For more information about the release cadence, see [Update process](hr-admin-setup-update-process.md).</span></span>

## <a name="in-preview"></a><span data-ttu-id="39324-201">プレビュー</span><span class="sxs-lookup"><span data-stu-id="39324-201">In preview</span></span>

<span data-ttu-id="39324-202">2020 年 2 月 3 日に次のプレビュー機能が利用可能になります。</span><span class="sxs-lookup"><span data-stu-id="39324-202">The following preview features are available on February 3, 2020:</span></span>

- <span data-ttu-id="39324-203">**休暇および欠勤のプレビュー機能** - 詳細については、[休暇および欠勤のプレビュー機能](hr-leave-and-absence-overview.md?leave-and-absence-preview-features) を参照してください。</span><span class="sxs-lookup"><span data-stu-id="39324-203">**Leave and absence preview features** - For more information, see [Leave and absence preview features](hr-leave-and-absence-overview.md?leave-and-absence-preview-features).</span></span>

- <span data-ttu-id="39324-204">**福利厚生管理プレビュー機能** - 既知の問題など、詳細については[福利厚生管理の概要](hr-benefits-management-overview.md)を参照してください。</span><span class="sxs-lookup"><span data-stu-id="39324-204">**Benefits management preview feature** - For more information, including known issues, see [Benefits management overview](hr-benefits-management-overview.md).</span></span>

## <a name="see-also"></a><span data-ttu-id="39324-205">参照</span><span class="sxs-lookup"><span data-stu-id="39324-205">See also</span></span>

[<span data-ttu-id="39324-206">Human Resources の新機能および変更された機能</span><span class="sxs-lookup"><span data-stu-id="39324-206">What's new or changed in Human Resources</span></span>](hr-admin-whats-new.md)</br>
[<span data-ttu-id="39324-207">Dynamics 365 Human Resources 2019 のリリース ウェーブ 2 の概要</span><span class="sxs-lookup"><span data-stu-id="39324-207">Overview of Dynamics 365 Human Resources 2019 release wave 2</span></span>](/dynamics365-release-plan/2019wave2/dynamics365-human-resources/)</br>
[<span data-ttu-id="39324-208">更新プロセス</span><span class="sxs-lookup"><span data-stu-id="39324-208">Update process</span></span>](hr-admin-setup-update-process.md)</br>
[<span data-ttu-id="39324-209">機能の管理</span><span class="sxs-lookup"><span data-stu-id="39324-209">Manage features</span></span>](hr-admin-manage-features.md)

[!INCLUDE[footer-include](../includes/footer-banner.md)]