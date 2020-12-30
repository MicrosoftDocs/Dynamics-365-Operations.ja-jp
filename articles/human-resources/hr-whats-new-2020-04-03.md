---
title: Dynamics 365 Human Resources の新機能または変更された機能 (2020 年 4 月 3 日)
description: この記事では、2020 年 4 月 3 日に更新された Microsoft Dynamics 365 Human Resources の新機能、または変更された機能について説明します。
author: Darinkramer
manager: AnnBe
ms.date: 04/03/2020
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
ms.search.validFrom: 2020-04-03
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: 8f5d7ab996e0d27f763cd4c3c51e9a2c923d909b
ms.sourcegitcommit: e89bb3e5420a6ece84f4e80c11e360b4a042f59d
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 11/17/2020
ms.locfileid: "4526789"
---
# <a name="whats-new-or-changed-in-dynamics-365-human-resources-april-3-2020"></a><span data-ttu-id="332a6-103">Dynamics 365 Human Resources の新機能または変更された機能 (2020 年 4 月 3 日)</span><span class="sxs-lookup"><span data-stu-id="332a6-103">What's new or changed in Dynamics 365 Human Resources (April 3, 2020)</span></span>

[!include [rename-banner](~/includes/cc-data-platform-banner.md)]

<span data-ttu-id="332a6-104">この記事では、Dynamics 365 Human Resources の新機能および変更された機能について説明します。</span><span class="sxs-lookup"><span data-stu-id="332a6-104">This article describes features that are either new or changed in Dynamics 365 Human Resources.</span></span> <span data-ttu-id="332a6-105">変更は、ビルド番号 8.1.3111 に適用されます。</span><span class="sxs-lookup"><span data-stu-id="332a6-105">Changes apply to build number 8.1.3111.</span></span> <span data-ttu-id="332a6-106">一部のヘッダーにあるかっこ内の数字は、参照用に Lifecycle Services (LCS) のサポート番号を参照しています。</span><span class="sxs-lookup"><span data-stu-id="332a6-106">The numbers in parentheses in some headings refer to Lifecycle Services (LCS) support numbers for reference.</span></span>

## <a name="features-that-are-generally-available-the-week-of-april-6"></a><span data-ttu-id="332a6-107">4 月 6 日の週に一般公開される機能</span><span class="sxs-lookup"><span data-stu-id="332a6-107">Features that are generally available the week of April 6</span></span>

- <span data-ttu-id="332a6-108">**休暇と欠勤の機能** - 詳細については、[休暇と欠勤の概要](hr-leave-and-absence-overview.md) を参照してください。</span><span class="sxs-lookup"><span data-stu-id="332a6-108">**Leave and absence features** - For more information, see [Leave and absence overview](hr-leave-and-absence-overview.md).</span></span>

- <span data-ttu-id="332a6-109">**福利厚生管理の機能** - 詳細については、[福利厚生管理の概要](hr-benefits-management-overview.md) を参照してください。</span><span class="sxs-lookup"><span data-stu-id="332a6-109">**Benefits management features** - For more information, see [Benefits management overview](hr-benefits-management-overview.md).</span></span>

## <a name="human-resources-environment-limits-are-now-based-on-updated-licensing-394595"></a><span data-ttu-id="332a6-110">人事管理環境の制限は、現在、更新されたライセンスに基づいている (394595)</span><span class="sxs-lookup"><span data-stu-id="332a6-110">Human Resources environment limits are now based on updated licensing (394595)</span></span>

<span data-ttu-id="332a6-111">LCS のプロジェクトあたりの環境数の制限が変更されました。</span><span class="sxs-lookup"><span data-stu-id="332a6-111">The limit on the number of environments per project in LCS has changed.</span></span> <span data-ttu-id="332a6-112">以前の制限は 2 つの環境でした。</span><span class="sxs-lookup"><span data-stu-id="332a6-112">The previous limit was two environments.</span></span> <span data-ttu-id="332a6-113">LCS で人事管理用に作成できる運用環境とサンドボックス環境の数の制限は、更新されたライセンスに基づいています。</span><span class="sxs-lookup"><span data-stu-id="332a6-113">The limit on the number of production and sandbox environments you can create for Human Resources in LCS is now based on updated licensing.</span></span> <span data-ttu-id="332a6-114">購入したライセンスの数に応じて、LCS プロジェクトごとに必要な数の環境を作成できるようになりました。</span><span class="sxs-lookup"><span data-stu-id="332a6-114">You can now create as many environments as needed per LCS project, depending on the number of licenses purchased.</span></span> <span data-ttu-id="332a6-115">2020 年 2 月 1 日に更新された新しいライセンスでは、顧客は追加の環境を購入できます。</span><span class="sxs-lookup"><span data-stu-id="332a6-115">The new licensing, updated on February 1, 2020, allows customers to purchase additional environments.</span></span> <span data-ttu-id="332a6-116">追加の環境のライセンス要件の詳細については、[Dynamics 365 ライセンスガイド](https://dynamics.microsoft.com/pricing/#HumanResources) を参照してください。</span><span class="sxs-lookup"><span data-stu-id="332a6-116">For more information about licensing requirements for additional environments, see [Dynamics 365 Licensing Guide](https://dynamics.microsoft.com/pricing/#HumanResources).</span></span>
 
## <a name="error-when-trying-to-delete-a-questionnaire-428603"></a><span data-ttu-id="332a6-117">アンケートを削除しようとするとエラーが発生しました (428603)</span><span class="sxs-lookup"><span data-stu-id="332a6-117">Error when trying to delete a questionnaire (428603)</span></span>

<span data-ttu-id="332a6-118">今週の更新プログラムでは、アンケートを削除しようとすると次のエラーが表示される問題が修正されました:</span><span class="sxs-lookup"><span data-stu-id="332a6-118">This week's update corrects an issue where the following error displays when attempting to delete a questionnaire:</span></span>

<span data-ttu-id="332a6-119">アンバランスな X++ TTSBEGIN/TTSCOMMIT ペアが検出されました。</span><span class="sxs-lookup"><span data-stu-id="332a6-119">An unbalanced X++ TTSBEGIN/TTSCOMMIT pair has been detected.</span></span>

## <a name="performance-journal-and-professional-certificates-security-issue-428499"></a><span data-ttu-id="332a6-120">業績仕訳と専門的な証明書のセキュリティ問題 (428499)</span><span class="sxs-lookup"><span data-stu-id="332a6-120">Performance journal and professional certificates security issue (428499)</span></span>

<span data-ttu-id="332a6-121">この変更により、アクセスできる企業に基づいて、業績仕訳と専門的な証明書の両方の表示が制限されます。</span><span class="sxs-lookup"><span data-stu-id="332a6-121">This change limits the visibility of both performance journals and professional certificates based on the companies they have access to.</span></span> 

## <a name="the-abbreviation-for-quebec-and-manitoba-387510"></a><span data-ttu-id="332a6-122">ケベック州とマニトバ州の略語 (387510)</span><span class="sxs-lookup"><span data-stu-id="332a6-122">The abbreviation for Quebec and Manitoba (387510)</span></span>

<span data-ttu-id="332a6-123">開始データは、マニトバ州とケベック州の正しい略語を反映するように更新されました。</span><span class="sxs-lookup"><span data-stu-id="332a6-123">Starting data has been updated to reflect the correct abbreviation for Manitoba and Quebec.</span></span>

## <a name="new-entities-available-in-data-management-framework"></a><span data-ttu-id="332a6-124">データ管理フレームワークで使用できる新しいエンティティ</span><span class="sxs-lookup"><span data-stu-id="332a6-124">New entities available in Data Management Framework</span></span>

<span data-ttu-id="332a6-125">次のエンティティが利用可能になりました。</span><span class="sxs-lookup"><span data-stu-id="332a6-125">The following entities are now available.</span></span> <span data-ttu-id="332a6-126">エンティティ リストにこれらのエンティティが表示されない場合は、**フレームワーク パラメーター > エンティティ設定 > エンティティ リストの更新** の **エンティティの更新** オプションを使用します。</span><span class="sxs-lookup"><span data-stu-id="332a6-126">If you don't see these entities listed in the entities list, use the **Refresh entities** option in **Framework Parameters > Entity settings > Refresh entity list**.</span></span>

 - <span data-ttu-id="332a6-127">休暇の銀行トランザクション V2</span><span class="sxs-lookup"><span data-stu-id="332a6-127">Leave and absence bank transaction V2</span></span>
 - <span data-ttu-id="332a6-128">休暇の登録 V2</span><span class="sxs-lookup"><span data-stu-id="332a6-128">Leave and absence enrollment V2</span></span>
 - <span data-ttu-id="332a6-129">休暇計画層 V2</span><span class="sxs-lookup"><span data-stu-id="332a6-129">Leave and absence plan tier V2</span></span>
 - <span data-ttu-id="332a6-130">休暇計画 V2</span><span class="sxs-lookup"><span data-stu-id="332a6-130">Leave and absence plan V2</span></span>

## <a name="common-data-service-solution-is-now-available-with-the-following-changes"></a><span data-ttu-id="332a6-131">Common Data Service ソリューションが、次の変更で利用可能になりました。</span><span class="sxs-lookup"><span data-stu-id="332a6-131">Common Data Service solution is now available with the following changes:</span></span>

| <span data-ttu-id="332a6-132">説明</span><span class="sxs-lookup"><span data-stu-id="332a6-132">Description</span></span> | <span data-ttu-id="332a6-133">計上額</span><span class="sxs-lookup"><span data-stu-id="332a6-133">Change</span></span> |
| --- | --- |
| <span data-ttu-id="332a6-134">**職務/職位** エンティティの変更</span><span class="sxs-lookup"><span data-stu-id="332a6-134">**Job/Position** entity changes</span></span> | <ul><li><span data-ttu-id="332a6-135">追加された **報酬地域**</span><span class="sxs-lookup"><span data-stu-id="332a6-135">**Compensation region** added</span></span></li>|
| <span data-ttu-id="332a6-136">追加された **職務職位分析** エンティティ</span><span class="sxs-lookup"><span data-stu-id="332a6-136">**Job position dimension** entity added</span></span> | <ul><li><span data-ttu-id="332a6-137">追加された **財務分析コード**</span><span class="sxs-lookup"><span data-stu-id="332a6-137">**Financial dimensions** added</span></span></li>
| <span data-ttu-id="332a6-138">**作業者** エンティティの変更</span><span class="sxs-lookup"><span data-stu-id="332a6-138">**Worker** entity changes</span></span> | <ul><li><span data-ttu-id="332a6-139">追加された **名前の順序**</span><span class="sxs-lookup"><span data-stu-id="332a6-139">**Name sequence** added</span></span></li><li><span data-ttu-id="332a6-140">追加された **自宅から作業**</span><span class="sxs-lookup"><span data-stu-id="332a6-140">**Works from home** added</span></span></li><li><span data-ttu-id="332a6-141">追加された **言語**</span><span class="sxs-lookup"><span data-stu-id="332a6-141">**Language** added</span></span></li><li><span data-ttu-id="332a6-142">追加された **勤続日数**</span><span class="sxs-lookup"><span data-stu-id="332a6-142">**Seniority date** added</span></span></li><li><span data-ttu-id="332a6-143">追加された **記念日**</span><span class="sxs-lookup"><span data-stu-id="332a6-143">**Anniversary date** added</span></span></li><li><span data-ttu-id="332a6-144">追加された **元の採用日付**</span><span class="sxs-lookup"><span data-stu-id="332a6-144">**Original hire date** added</span></span></li></ul> |
| <span data-ttu-id="332a6-145">**雇用** エンティティの変更</span><span class="sxs-lookup"><span data-stu-id="332a6-145">**Employment** entity changes</span></span> | <ul><li><span data-ttu-id="332a6-146">追加された **財務分析コード**</span><span class="sxs-lookup"><span data-stu-id="332a6-146">**Financial dimensions** added</span></span></li><li><span data-ttu-id="332a6-147">追加された **退職理由**</span><span class="sxs-lookup"><span data-stu-id="332a6-147">**Termination reason** added</span></span></li><li><span data-ttu-id="332a6-148">**移行日** から名前変更された **退職日**</span><span class="sxs-lookup"><span data-stu-id="332a6-148">**Termination date** renamed from **Transition date**</span></span></li><li><span data-ttu-id="332a6-149">追加された **猶予期間**</span><span class="sxs-lookup"><span data-stu-id="332a6-149">**Probation date** added</span></span></li></ul> |
| <span data-ttu-id="332a6-150">**作業者住所** エンティティの変更</span><span class="sxs-lookup"><span data-stu-id="332a6-150">**Worker address** entity changes</span></span> | <ul><li><span data-ttu-id="332a6-151">追加された **番地**</span><span class="sxs-lookup"><span data-stu-id="332a6-151">**Street address** added</span></span></li><li><span data-ttu-id="332a6-152">廃止としてマークされた **住所行 1**、**住所行 2**、および **住所行 3**</span><span class="sxs-lookup"><span data-stu-id="332a6-152">**Address line 1**, **Address line 2**, and **Address line 3** marked for deprecation</span></span></li></ul> |
| <span data-ttu-id="332a6-153">新しい変動報酬の設定エンティティ</span><span class="sxs-lookup"><span data-stu-id="332a6-153">New variable compensation setup entities</span></span> | <ul><li><span data-ttu-id="332a6-154">**変動報酬プラン タイプ**</span><span class="sxs-lookup"><span data-stu-id="332a6-154">**Compensation variable plan type**</span></span></li><li><span data-ttu-id="332a6-155">**変動報酬プラン**</span><span class="sxs-lookup"><span data-stu-id="332a6-155">**Compensation variable plan**</span></span></li><li><span data-ttu-id="332a6-156">**給付ルール**</span><span class="sxs-lookup"><span data-stu-id="332a6-156">**Vesting rules**</span></span></li><li><span data-ttu-id="332a6-157">**変動報酬プラン レベル**</span><span class="sxs-lookup"><span data-stu-id="332a6-157">**Compensation variable plan level**</span></span></li></ul> |
| <span data-ttu-id="332a6-158">新しい **作業者カレンダー雇用** エンティティ</span><span class="sxs-lookup"><span data-stu-id="332a6-158">New **Worker calendar employment** entity</span></span> | <ul><li><span data-ttu-id="332a6-159">追加された **作業カレンダー エンティティ**</span><span class="sxs-lookup"><span data-stu-id="332a6-159">**Work calendar entity** added</span></span></li></ul> |
| <span data-ttu-id="332a6-160">新しい **給与職位詳細** エンティティ</span><span class="sxs-lookup"><span data-stu-id="332a6-160">New **Payroll position detail** entity</span></span> | <ul><li><span data-ttu-id="332a6-161">追加された **給与職位詳細**</span><span class="sxs-lookup"><span data-stu-id="332a6-161">**Payroll position detail** added</span></span></li></ul> |
| <span data-ttu-id="332a6-162">新しい **肩書** エンティティ</span><span class="sxs-lookup"><span data-stu-id="332a6-162">New **Title** entity</span></span> | <ul><li><span data-ttu-id="332a6-163">追加された **タイトル**</span><span class="sxs-lookup"><span data-stu-id="332a6-163">**Title** added</span></span></li></ul><span data-ttu-id="332a6-164">新しい **タイトル** エンティティは Common Data Service に含まれますが、この時点では **職位** または **職務** エンティティから参照されません。</span><span class="sxs-lookup"><span data-stu-id="332a6-164">The new **Title** entity is included in Common Data Service but isn't referenced from the **Job Position** or **Job** entities at this time.</span></span> |

> [!NOTE]
> <span data-ttu-id="332a6-165">職位と雇用どちらの財務分析コードは、Human Resources から Common Data Service への更新の一方向の統合を提供します。</span><span class="sxs-lookup"><span data-stu-id="332a6-165">Financial dimensions for both positions and employment provide one-direction integration for updates from Human Resources to Common Data Service.</span></span> <span data-ttu-id="332a6-166">財務分析コードの更新は、現在 Common Data Service から Human Resources へは同期されません。</span><span class="sxs-lookup"><span data-stu-id="332a6-166">Financial dimensions updates don't currently synchronize from Common Data Service to Human Resources.</span></span>

<span data-ttu-id="332a6-167">今後数週間のうちに、これらのエンティティの変更がすべての環境で使用できるようになります。</span><span class="sxs-lookup"><span data-stu-id="332a6-167">Over the next few weeks, these entity changes will be available in all environments.</span></span> <span data-ttu-id="332a6-168">Human Resources の最新 Common Data Service ソリューションを手動でインストールするには、次の操作を行います。</span><span class="sxs-lookup"><span data-stu-id="332a6-168">To manually install the latest Common Data Service solution for Human Resources:</span></span>

1.  <span data-ttu-id="332a6-169">[Power Platform 管理センター](https://admin.powerplatform.microsoft.com) に移動します。</span><span class="sxs-lookup"><span data-stu-id="332a6-169">Go to the [Power Platform Admin Center](https://admin.powerplatform.microsoft.com).</span></span>

2.  <span data-ttu-id="332a6-170">**環境** を選択します。</span><span class="sxs-lookup"><span data-stu-id="332a6-170">Select **Environments**.</span></span>

3.  <span data-ttu-id="332a6-171">アップグレードする環境を検索します。</span><span class="sxs-lookup"><span data-stu-id="332a6-171">Find the environment you want to upgrade.</span></span> <span data-ttu-id="332a6-172">環境は、Human Resources の **バージョン情報** フォームで、**Common Data Service 情報** セクションの **環境名** に対応している必要があります。</span><span class="sxs-lookup"><span data-stu-id="332a6-172">The environment should correspond to **Environment name** in the **Common Data Service information** section in the **About** form in Human Resources.</span></span>

4.  <span data-ttu-id="332a6-173">環境の詳細を表示するための環境を選択します。</span><span class="sxs-lookup"><span data-stu-id="332a6-173">Select the environment to view the environment details.</span></span>

5.  <span data-ttu-id="332a6-174">上部の操作バーで、**ソリューションの管理** を選択します。</span><span class="sxs-lookup"><span data-stu-id="332a6-174">In the action bar at the top, select **Manage Solutions**.</span></span> <span data-ttu-id="332a6-175">新しいブラウザー ウィンドウが開き、環境のコンテキストで **Dynamics 365 管理センター** に移動します。</span><span class="sxs-lookup"><span data-stu-id="332a6-175">A new browser window will open and navigate to **Dynamics 365 Administration Center** in the context of your environment.</span></span>

6.  <span data-ttu-id="332a6-176">**ソリューション** リストで、**Dynamics 365 Human Resources アンカー** を選択します。</span><span class="sxs-lookup"><span data-stu-id="332a6-176">In the **Solution** list, select **Dynamics 365 Human Resources Anchor**.</span></span>

7.  <span data-ttu-id="332a6-177">最新のソリューションを適用するには、**アップグレード** を選択します。</span><span class="sxs-lookup"><span data-stu-id="332a6-177">Select **Upgrade** to apply the latest solution.</span></span>

## <a name="in-preview"></a><span data-ttu-id="332a6-178">プレビュー</span><span class="sxs-lookup"><span data-stu-id="332a6-178">In Preview</span></span>

## <a name="leave-suspension"></a><span data-ttu-id="332a6-179">休暇の停止</span><span class="sxs-lookup"><span data-stu-id="332a6-179">Leave suspension</span></span>

<span data-ttu-id="332a6-180">従業員に対し Human Resources で休暇および欠勤を中断できます。</span><span class="sxs-lookup"><span data-stu-id="332a6-180">You can suspend leave and absence in Human Resources for an employee.</span></span> <span data-ttu-id="332a6-181">休暇を中断すると、選択した休暇タイプの休暇の発生が停止します。</span><span class="sxs-lookup"><span data-stu-id="332a6-181">Suspending leave stops the leave accruals for selected leave types.</span></span> <span data-ttu-id="332a6-182">一時停止が見越計上プロセス後に発生した場合、休暇の一時停止により、従業員の休暇残日数が比例配分調整されます。</span><span class="sxs-lookup"><span data-stu-id="332a6-182">If the suspension occurs after an accrual has been processed, suspending leave will create a prorated adjustment to the employee's leave balance.</span></span> <span data-ttu-id="332a6-183">詳細については、[休暇の中断](hr-leave-and-absence-suspend-leave.md) を参照してください。</span><span class="sxs-lookup"><span data-stu-id="332a6-183">For more information, see [Suspend leave](hr-leave-and-absence-suspend-leave.md).</span></span>

## <a name="carry-forward-rules"></a><span data-ttu-id="332a6-184">繰越ルール</span><span class="sxs-lookup"><span data-stu-id="332a6-184">Carry forward rules</span></span>

<span data-ttu-id="332a6-185">繰越調整を転送する繰越残日数に対して、繰越休暇タイプを指定できます。</span><span class="sxs-lookup"><span data-stu-id="332a6-185">You can specify a carry forward leave type for carry forward balances where carry forward adjustments are transferred.</span></span> <span data-ttu-id="332a6-186">たとえば、従業員が 10 日間繰り越す場合、その 10 日間に別の休暇タイプを選択できます。</span><span class="sxs-lookup"><span data-stu-id="332a6-186">For example, if an employee carries forward 10 days, you can pick a different leave type for those 10 days.</span></span> <span data-ttu-id="332a6-187">詳細については、[休暇および欠勤タイプのコンフィギュレーション](hr-leave-and-absence-types.md) を参照してください。</span><span class="sxs-lookup"><span data-stu-id="332a6-187">For more information, see [Configure leave and absence types](hr-leave-and-absence-types.md).</span></span>

## <a name="coming-soon"></a><span data-ttu-id="332a6-188">間もなく公開</span><span class="sxs-lookup"><span data-stu-id="332a6-188">Coming Soon</span></span>

## <a name="new-production-release-cadence"></a><span data-ttu-id="332a6-189">新しい生産リリース リズム</span><span class="sxs-lookup"><span data-stu-id="332a6-189">New production release cadence</span></span>

<span data-ttu-id="332a6-190">4 月から、Human Resources のリリース頻度は、毎週更新から隔週更新に移行します。</span><span class="sxs-lookup"><span data-stu-id="332a6-190">Beginning in April, the release cadence for Human Resources will shift from a weekly update to a bi-weekly update.</span></span> <span data-ttu-id="332a6-191">安全な展開プラクティスとの整合性を確保し、サービスの安定性と信頼性の高い標準を維持するために、すべての地域にサービス更新を展開するプロセスは 2 週間で展開されます。</span><span class="sxs-lookup"><span data-stu-id="332a6-191">To ensure alignment with safe deployment practices, and maintain high standards of stability and reliability in the service, the process of deploying service updates to all regions will be a two-week rollout.</span></span> <span data-ttu-id="332a6-192">プロセスの各ステージで展開が成功したことを確認するために、追加のテストとモニターが実行されます。</span><span class="sxs-lookup"><span data-stu-id="332a6-192">Additional testing and monitors will be in place to verify successful deployment at each stage of the process.</span></span> <span data-ttu-id="332a6-193">リリース頻度の詳細については、[更新プロセス](hr-admin-setup-update-process.md) を参照してください。</span><span class="sxs-lookup"><span data-stu-id="332a6-193">For more information on the release cadence, see [Update process](hr-admin-setup-update-process.md).</span></span>

## <a name="known-issues"></a><span data-ttu-id="332a6-194">既知の問題</span><span class="sxs-lookup"><span data-stu-id="332a6-194">Known issues</span></span>

## <a name="employment-detail-entity"></a><span data-ttu-id="332a6-195">雇用の詳細エンティティ</span><span class="sxs-lookup"><span data-stu-id="332a6-195">Employment Detail entity</span></span>

<span data-ttu-id="332a6-196">**雇用の詳細** エンティティが、次のフィールドで更新されました: **PayFrequency**、**雇用カテゴリ ID**、**雇用タイプ**、**EmploymentType ID**、**福利厚生の雇用状況**。</span><span class="sxs-lookup"><span data-stu-id="332a6-196">The **Employment Detail** entity has been updated with the following fields: **PayFrequency**, **Employment Category ID**, **Employment Type**, **EmploymentType ID**, and **Benefit Employment Status**.</span></span> <span data-ttu-id="332a6-197">これらのフィールドの設定データは、機能管理で有効になっている福利厚生の管理に依存します。</span><span class="sxs-lookup"><span data-stu-id="332a6-197">The setup data for these fields rely on benefits management being enabled in Feature management.</span></span> <span data-ttu-id="332a6-198">これらのフィールドは、インポート中にエラーが発生するため、**雇用の詳細** エンティティで入力または更新しないでください。</span><span class="sxs-lookup"><span data-stu-id="332a6-198">These fields shouldn't be populated or updated in the **Employment Detail** entity, because it will result in errors during import.</span></span>

## <a name="sharepoint-preview-doesnt-work-in-some-environments"></a><span data-ttu-id="332a6-199">一部の環境で、SharePoint プレビューが機能しない</span><span class="sxs-lookup"><span data-stu-id="332a6-199">SharePoint preview doesn't work in some environments</span></span>

<span data-ttu-id="332a6-200">SharePoint で保存されているドキュメントのドキュメント プレビューが機能しない場合は、次の手順を実行します。</span><span class="sxs-lookup"><span data-stu-id="332a6-200">If document preview for documents stored in SharePoint doesn't work, try the following procedure:</span></span>

1. <span data-ttu-id="332a6-201">管理者のユーザー アカウントにユーザー レコードに関連付けられたメールがあることを確認します。</span><span class="sxs-lookup"><span data-stu-id="332a6-201">Verify the Admin user account has an email associated with the user record.</span></span> <span data-ttu-id="332a6-202">この情報は、**ユーザー** ページで確認できます。</span><span class="sxs-lookup"><span data-stu-id="332a6-202">You can view this information in the **User** page.</span></span> <span data-ttu-id="332a6-203">メールが設定されていない場合は、OData Excel アドインを使用してメールとプロバイダーを追加する必要があります。</span><span class="sxs-lookup"><span data-stu-id="332a6-203">If email isn't set up, you need to add the email and provider with the OData Excel add-in.</span></span> <span data-ttu-id="332a6-204">既定では、Excel デザインにメール アドレスは表示されません。</span><span class="sxs-lookup"><span data-stu-id="332a6-204">By default, the email address isn't present in the Excel design.</span></span> <span data-ttu-id="332a6-205">Excel デザインを編集し、すべてのフィールドを追加し、適用して更新する必要があります。</span><span class="sxs-lookup"><span data-stu-id="332a6-205">You'll need to edit the Excel design, add all fields, apply, and refresh.</span></span> <span data-ttu-id="332a6-206">これらのステップを完了すると、管理者アカウントを更新できます。</span><span class="sxs-lookup"><span data-stu-id="332a6-206">Once you've completed those steps, you can update the admin account.</span></span>

2. <span data-ttu-id="332a6-207">管理者アカウントにメール アカウントが関連付けられたら、人事管理に管理者としてサインインします。</span><span class="sxs-lookup"><span data-stu-id="332a6-207">After the Admin account has an associated email account, sign in to Human Resources with Admin credentials.</span></span>

3. <span data-ttu-id="332a6-208">SharePoint で添付ファイルにアクセスして、ドキュメントのプレビューを開始します。</span><span class="sxs-lookup"><span data-stu-id="332a6-208">Access an attachment in SharePoint to start the document preview.</span></span>

4. <span data-ttu-id="332a6-209">添付ファイルにアクセスできる他のユーザー アカウントでサインインし、適切にプレビューが機能することを確認します。</span><span class="sxs-lookup"><span data-stu-id="332a6-209">Sign in with another user account that has access to attachments and verify that the preview works as expected.</span></span>

## <a name="see-also"></a><span data-ttu-id="332a6-210">参照</span><span class="sxs-lookup"><span data-stu-id="332a6-210">See also</span></span>

[<span data-ttu-id="332a6-211">Human Resources の新機能および変更された機能</span><span class="sxs-lookup"><span data-stu-id="332a6-211">What's new or changed in Human Resources</span></span>](hr-admin-whats-new.md)</br>
[<span data-ttu-id="332a6-212">Dynamics 365 Human Resources 2019 のリリース ウェーブ 2 の概要</span><span class="sxs-lookup"><span data-stu-id="332a6-212">Overview of Dynamics 365 Human Resources 2019 release wave 2</span></span>](https://docs.microsoft.com/dynamics365-release-plan/2019wave2/dynamics365-human-resources/)</br>
[<span data-ttu-id="332a6-213">更新プロセス</span><span class="sxs-lookup"><span data-stu-id="332a6-213">Update process</span></span>](hr-admin-setup-update-process.md)</br>
[<span data-ttu-id="332a6-214">機能の管理</span><span class="sxs-lookup"><span data-stu-id="332a6-214">Manage features</span></span>](hr-admin-manage-features.md)