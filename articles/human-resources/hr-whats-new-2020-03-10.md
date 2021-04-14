---
title: Dynamics 365 Human Resources の新機能および変更された機能 (2020 年 3 月 10 日)
description: この記事では、2020 年 3 月 10 日に更新された Microsoft Dynamics 365 Human Resources の新機能、または変更された機能について説明します。
author: andreabichsel
ms.date: 03/10/2020
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
ms.search.validFrom: 2020-03-10
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: 27d9aead663da63b98cba249ef57f1324a145c34
ms.sourcegitcommit: 3cdc42346bb653c13ab33a7142dbb7969f1f6dda
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 03/31/2021
ms.locfileid: "5790383"
---
# <a name="whats-new-or-changed-in-dynamics-365-human-resources-march-10-2020"></a><span data-ttu-id="8c998-103">Dynamics 365 Human Resources の新機能および変更された機能 (2020 年 3 月 10 日)</span><span class="sxs-lookup"><span data-stu-id="8c998-103">What's new or changed in Dynamics 365 Human Resources (March 10, 2020)</span></span>

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

[!include [rename-banner](~/includes/cc-data-platform-banner.md)]

<span data-ttu-id="8c998-104">この記事では、Dynamics 365 Human Resources の新機能および変更された機能について説明します。</span><span class="sxs-lookup"><span data-stu-id="8c998-104">This article describes features that are either new or changed in Dynamics 365 Human Resources.</span></span> <span data-ttu-id="8c998-105">変更は、ビルド番号 8.1.2985 に適用されます。</span><span class="sxs-lookup"><span data-stu-id="8c998-105">Changes apply to build number 8.1.2985.</span></span> <span data-ttu-id="8c998-106">ヘッダーにあるかっこ内の数字は、参照用の LCS のサポート番号を参照していることがあります。</span><span class="sxs-lookup"><span data-stu-id="8c998-106">The numbers in parentheses in some headings refer to LCS support numbers for reference.</span></span>

## <a name="cant-access-skill-gap-analysis-report-394460"></a><span data-ttu-id="8c998-107">スキル ギャップ分析レポートにアクセスできません (394460)</span><span class="sxs-lookup"><span data-stu-id="8c998-107">Can't access skill gap analysis report (394460)</span></span>

<span data-ttu-id="8c998-108">このレポートは Dynamics 365 Human Resources ではサポートされていません。</span><span class="sxs-lookup"><span data-stu-id="8c998-108">This report isn't supported in Dynamics 365 Human Resources.</span></span> <span data-ttu-id="8c998-109">SSRS レポートを印刷するためのメニュー項目が削除されます。</span><span class="sxs-lookup"><span data-stu-id="8c998-109">The menu item to print the SSRS report is removed.</span></span>

## <a name="incorrect-message-accessing-the-getting-started-page-417950"></a><span data-ttu-id="8c998-110">はじめにページにアクセスするメッセージが正しくありません (417950)</span><span class="sxs-lookup"><span data-stu-id="8c998-110">Incorrect message accessing the Getting Started page (417950)</span></span>

<span data-ttu-id="8c998-111">この変更により、フォームへのアクセス許可がない場合は、セキュリティによってこのメニュー項目が非表示になります。</span><span class="sxs-lookup"><span data-stu-id="8c998-111">With this change, security hides this menu item if you don't have access to the form.</span></span>

## <a name="streamlined-task-maintenance-for-employees-380538"></a><span data-ttu-id="8c998-112">従業員のタスク メンテナンスの合理化 (380538)</span><span class="sxs-lookup"><span data-stu-id="8c998-112">Streamlined task maintenance for employees (380538)</span></span>

<span data-ttu-id="8c998-113">作業者タスク メンテナンス フォームには、オンボード、オフボード、移動、および業務プロセスのすべてのタスクが表示されます。</span><span class="sxs-lookup"><span data-stu-id="8c998-113">The worker task maintenance form lists all tasks for an employee across onboarding, offboarding, transitions, and business processes.</span></span> <span data-ttu-id="8c998-114">タスクの状態を削除、再割り当て、または更新できるようになりました。</span><span class="sxs-lookup"><span data-stu-id="8c998-114">You can delete, reassign, or update the status of tasks.</span></span>

<span data-ttu-id="8c998-115">例: ベンジャミン マーティンは福利厚生管理者です。</span><span class="sxs-lookup"><span data-stu-id="8c998-115">Example: Benjamin Martin is a benefits administrator.</span></span> <span data-ttu-id="8c998-116">従業員のオンボードでは、ベンジャミンに対してタスクが作成され、新しい従業員の給付金の選択が確認されます。</span><span class="sxs-lookup"><span data-stu-id="8c998-116">During employee onboarding, tasks are created for Benjamin to review the new employee’s benefit selection.</span></span> <span data-ttu-id="8c998-117">ベンジャミンには、完了した過去のタスクと、完了する必要がある将来のタスクがあります。</span><span class="sxs-lookup"><span data-stu-id="8c998-117">Benjamin has past tasks that he's completed, and future tasks that he needs to complete.</span></span> <span data-ttu-id="8c998-118">ベンジャミンが会社を退職することを決定したので、タスクを再割り当てまたは削除する必要があります。</span><span class="sxs-lookup"><span data-stu-id="8c998-118">Benjamin decides to leave the company, so his tasks need to be either re-assigned or removed.</span></span> <span data-ttu-id="8c998-119">タスクのメンテナンス フォーム (**作業者** フォームのアクション ウィンドウ) では、ベンジャミンのすべてのタスクが別の作業者に再割り当てされるかまたは削除されます。</span><span class="sxs-lookup"><span data-stu-id="8c998-119">The task maintenance form (in the action pane of the **Worker** form) allows all of Benjamin’s tasks to be re-assigned to another worker or removed.</span></span>  

## <a name="dataverse-solution-is-now-available-with-the-following-changes"></a><span data-ttu-id="8c998-120">Dataverse ソリューションが、次の変更で利用可能になりました。</span><span class="sxs-lookup"><span data-stu-id="8c998-120">Dataverse solution is now available with the following changes:</span></span>

| <span data-ttu-id="8c998-121">説明</span><span class="sxs-lookup"><span data-stu-id="8c998-121">Description</span></span> | <span data-ttu-id="8c998-122">計上額</span><span class="sxs-lookup"><span data-stu-id="8c998-122">Change</span></span> |
| --- | --- |
| <span data-ttu-id="8c998-123">**職務/職位** エンティティの変更</span><span class="sxs-lookup"><span data-stu-id="8c998-123">**Job/Position** entity changes</span></span> | <ul><li><span data-ttu-id="8c998-124">追加された **報酬地域**</span><span class="sxs-lookup"><span data-stu-id="8c998-124">**Compensation region** added</span></span></li>|
| <span data-ttu-id="8c998-125">追加された **職務職位分析** エンティティ</span><span class="sxs-lookup"><span data-stu-id="8c998-125">**Job position dimension** entity added</span></span> | <ul><li><span data-ttu-id="8c998-126">追加された **財務分析コード**</span><span class="sxs-lookup"><span data-stu-id="8c998-126">**Financial dimensions** added</span></span></li>
| <span data-ttu-id="8c998-127">**作業者** エンティティの変更</span><span class="sxs-lookup"><span data-stu-id="8c998-127">**Worker** entity changes</span></span> | <ul><li><span data-ttu-id="8c998-128">追加された **名前の順序**</span><span class="sxs-lookup"><span data-stu-id="8c998-128">**Name sequence** added</span></span></li><li><span data-ttu-id="8c998-129">追加された **自宅から作業**</span><span class="sxs-lookup"><span data-stu-id="8c998-129">**Works from home** added</span></span></li><li><span data-ttu-id="8c998-130">追加された **言語**</span><span class="sxs-lookup"><span data-stu-id="8c998-130">**Language** added</span></span></li><li><span data-ttu-id="8c998-131">追加された **勤続日数**</span><span class="sxs-lookup"><span data-stu-id="8c998-131">**Seniority date** added</span></span></li><li><span data-ttu-id="8c998-132">追加された **記念日**</span><span class="sxs-lookup"><span data-stu-id="8c998-132">**Anniversary date** added</span></span></li><li><span data-ttu-id="8c998-133">追加された **元の採用日付**</span><span class="sxs-lookup"><span data-stu-id="8c998-133">**Original hire date** added</span></span></li></ul> |
| <span data-ttu-id="8c998-134">**雇用** エンティティの変更</span><span class="sxs-lookup"><span data-stu-id="8c998-134">**Employment** entity changes</span></span> | <ul><li><span data-ttu-id="8c998-135">追加された **財務分析コード**</span><span class="sxs-lookup"><span data-stu-id="8c998-135">**Financial dimensions** added</span></span></li><li><span data-ttu-id="8c998-136">追加された **退職理由**</span><span class="sxs-lookup"><span data-stu-id="8c998-136">**Termination reason** added</span></span></li><li><span data-ttu-id="8c998-137">**移行日** から名前変更された **退職日**</span><span class="sxs-lookup"><span data-stu-id="8c998-137">**Termination date** renamed from **Transition date**</span></span></li><li><span data-ttu-id="8c998-138">追加された **猶予期間**</span><span class="sxs-lookup"><span data-stu-id="8c998-138">**Probation date** added</span></span></li></ul> |
| <span data-ttu-id="8c998-139">**作業者住所** エンティティの変更</span><span class="sxs-lookup"><span data-stu-id="8c998-139">**Worker address** entity changes</span></span> | <ul><li><span data-ttu-id="8c998-140">追加された **番地**</span><span class="sxs-lookup"><span data-stu-id="8c998-140">**Street address** added</span></span></li><li><span data-ttu-id="8c998-141">廃止としてマークされた **住所行 1**、**住所行 2**、および **住所行 3**</span><span class="sxs-lookup"><span data-stu-id="8c998-141">**Address line 1**, **Address line 2**, and **Address line 3** marked for deprecation</span></span></li></ul> |
| <span data-ttu-id="8c998-142">新しい変動報酬の設定エンティティ</span><span class="sxs-lookup"><span data-stu-id="8c998-142">New variable compensation setup entities</span></span> | <ul><li><span data-ttu-id="8c998-143">**変動報酬プラン タイプ**</span><span class="sxs-lookup"><span data-stu-id="8c998-143">**Compensation variable plan type**</span></span></li><li><span data-ttu-id="8c998-144">**変動報酬プラン**</span><span class="sxs-lookup"><span data-stu-id="8c998-144">**Compensation variable plan**</span></span></li><li><span data-ttu-id="8c998-145">**給付ルール**</span><span class="sxs-lookup"><span data-stu-id="8c998-145">**Vesting rules**</span></span></li><li><span data-ttu-id="8c998-146">**変動報酬プラン レベル**</span><span class="sxs-lookup"><span data-stu-id="8c998-146">**Compensation variable plan level**</span></span></li></ul> |
| <span data-ttu-id="8c998-147">新しい **作業者カレンダー雇用** エンティティ</span><span class="sxs-lookup"><span data-stu-id="8c998-147">New **Worker calendar employment** entity</span></span> | <ul><li><span data-ttu-id="8c998-148">追加された **作業カレンダー エンティティ**</span><span class="sxs-lookup"><span data-stu-id="8c998-148">**Work calendar entity** added</span></span></li></ul> |
| <span data-ttu-id="8c998-149">新しい **給与職位詳細** エンティティ</span><span class="sxs-lookup"><span data-stu-id="8c998-149">New **Payroll position detail** entity</span></span> | <ul><li><span data-ttu-id="8c998-150">追加された **給与職位詳細**</span><span class="sxs-lookup"><span data-stu-id="8c998-150">**Payroll position detail** added</span></span></li></ul> |
| <span data-ttu-id="8c998-151">新しい **肩書** エンティティ</span><span class="sxs-lookup"><span data-stu-id="8c998-151">New **Title** entity</span></span> | <ul><li><span data-ttu-id="8c998-152">追加された **タイトル**</span><span class="sxs-lookup"><span data-stu-id="8c998-152">**Title** added</span></span></li></ul> <span data-ttu-id="8c998-153">新しい **タイトル** エンティティは Dataverse に含まれますが、この時点では **職位** または **職務** エンティティから参照されません。</span><span class="sxs-lookup"><span data-stu-id="8c998-153">The new **Title** entity is included in Dataverse but isn't referenced from the **Job Position** or **Job** entities at this time.</span></span> |

> [!NOTE]
> <span data-ttu-id="8c998-154">職位と雇用どちらの財務分析コードは、Human Resources から Dataverse への更新の一方向の統合を提供します。</span><span class="sxs-lookup"><span data-stu-id="8c998-154">Financial dimensions for both positions and employment provide one-direction integration for updates from Human Resources to Dataverse.</span></span> <span data-ttu-id="8c998-155">財務分析コードの更新は、現在 Dataverse から Human Resources へは同期されません。</span><span class="sxs-lookup"><span data-stu-id="8c998-155">Financial dimensions updates don't currently synchronize from Dataverse to Human Resources.</span></span>

<span data-ttu-id="8c998-156">今後数週間のうちに、これらのエンティティの変更がすべての環境で使用できるようになります。</span><span class="sxs-lookup"><span data-stu-id="8c998-156">Over the next few weeks, these entity changes will be available in all environments.</span></span> <span data-ttu-id="8c998-157">Human Resources の最新 Dataverse ソリューションを手動でインストールするには、次の操作を行います。</span><span class="sxs-lookup"><span data-stu-id="8c998-157">To manually install the latest Dataverse solution for Human Resources:</span></span>

1.  <span data-ttu-id="8c998-158">[Power Platform 管理センター](https://admin.powerplatform.microsoft.com) に移動します。</span><span class="sxs-lookup"><span data-stu-id="8c998-158">Go to the [Power Platform Admin Center](https://admin.powerplatform.microsoft.com).</span></span>

2.  <span data-ttu-id="8c998-159">**環境** を選択します。</span><span class="sxs-lookup"><span data-stu-id="8c998-159">Select **Environments**.</span></span>

3.  <span data-ttu-id="8c998-160">アップグレードする環境を検索します。</span><span class="sxs-lookup"><span data-stu-id="8c998-160">Find the environment you want to upgrade.</span></span> <span data-ttu-id="8c998-161">環境は、Human Resources の **バージョン情報** フォームで、**Dataverse 情報** セクションの **環境名** に対応している必要があります。</span><span class="sxs-lookup"><span data-stu-id="8c998-161">The environment should correspond to **Environment name** in the **Dataverse information** section in the **About** form in Human Resources.</span></span>

4.  <span data-ttu-id="8c998-162">環境の詳細を表示するための環境を選択します。</span><span class="sxs-lookup"><span data-stu-id="8c998-162">Select the environment to view the environment details.</span></span>

5.  <span data-ttu-id="8c998-163">上部の操作バーで、**ソリューションの管理** を選択します。</span><span class="sxs-lookup"><span data-stu-id="8c998-163">In the action bar at the top, select **Manage Solutions**.</span></span> <span data-ttu-id="8c998-164">新しいブラウザー ウィンドウが開き、環境のコンテキストで **Dynamics 365 管理センター** に移動します。</span><span class="sxs-lookup"><span data-stu-id="8c998-164">A new browser window will open and navigate to **Dynamics 365 Administration Center** in the context of your environment.</span></span>

6.  <span data-ttu-id="8c998-165">**ソリューション** リストで、**Dynamics 365 Human Resources アンカー** を選択します。</span><span class="sxs-lookup"><span data-stu-id="8c998-165">In the **Solution** list, select **Dynamics 365 Human Resources Anchor**.</span></span>

7.  <span data-ttu-id="8c998-166">最新のソリューションを適用するには、**アップグレード** を選択します。</span><span class="sxs-lookup"><span data-stu-id="8c998-166">Select **Upgrade** to apply the latest solution.</span></span>

## <a name="in-preview"></a><span data-ttu-id="8c998-167">プレビュー</span><span class="sxs-lookup"><span data-stu-id="8c998-167">In preview</span></span>

<span data-ttu-id="8c998-168">2020 年 2 月 3 日に次のプレビュー機能が利用可能になります。</span><span class="sxs-lookup"><span data-stu-id="8c998-168">The following preview features are available on February 3, 2020:</span></span>

- <span data-ttu-id="8c998-169">**休暇および欠勤のプレビュー機能** - 詳細については、[休暇および欠勤のプレビュー機能](hr-leave-and-absence-overview.md?leave-and-absence-preview-features) を参照してください。</span><span class="sxs-lookup"><span data-stu-id="8c998-169">**Leave and absence preview features** - For more information, see [Leave and absence preview features](hr-leave-and-absence-overview.md?leave-and-absence-preview-features).</span></span>

- <span data-ttu-id="8c998-170">**福利厚生管理プレビュー機能** - 既知の問題など、詳細については[福利厚生管理の概要](hr-benefits-management-overview.md)を参照してください。</span><span class="sxs-lookup"><span data-stu-id="8c998-170">**Benefits management preview feature** - For more information, including known issues, see [Benefits management overview](hr-benefits-management-overview.md).</span></span>

## <a name="coming-soon"></a><span data-ttu-id="8c998-171">間もなく公開</span><span class="sxs-lookup"><span data-stu-id="8c998-171">Coming Soon</span></span>

### <a name="platform-update-33"></a><span data-ttu-id="8c998-172">プラットフォーム update 33</span><span class="sxs-lookup"><span data-stu-id="8c998-172">Platform update 33</span></span>

- <span data-ttu-id="8c998-173">フル ページ アプリ (プレビュー) - このプレビュー機能は、保存されたビュー機能を有効にする必要があり、ダッシュボードから Power Apps とサード パーティー アプリをフルページ エクスペリエンスとして追加できます。</span><span class="sxs-lookup"><span data-stu-id="8c998-173">Full page apps (Preview) - This preview feature, which requires you to enable the Saved views feature, allows Power Apps and third-party apps to be added as full-page experiences via the dashboard.</span></span>

- <span data-ttu-id="8c998-174">保存されているビュー (プレビュー) - このプレビュー機能は個人用設定サブシステムの大幅な拡張で、保存されているビューを有効にします。</span><span class="sxs-lookup"><span data-stu-id="8c998-174">Saved views (Preview) - This preview feature enables saved views, which is a significant enhancement to the personalization subsystem.</span></span> <span data-ttu-id="8c998-175">この機能により、ユーザーはページごとに複数の名前を付けた個人用設定を使用できます。</span><span class="sxs-lookup"><span data-stu-id="8c998-175">This feature allows users to have multiple named sets of personalizations per page.</span></span> <span data-ttu-id="8c998-176">セキュリティ ロールにビューを公開することもできます。</span><span class="sxs-lookup"><span data-stu-id="8c998-176">You can also publish views to security roles.</span></span>

- <span data-ttu-id="8c998-177">「次の値のいずれか」のフィルタリング結果を最適化 - この機能により、最適化された「いずれか」のフィルタリング結果が可能になり、複数のフィルター値の入力を容易にして、個々またはすべてのフィルター値を削除する簡単なメカニズムを備え、またフィルター値のよりコンパクトで直感的な視覚化を実現します。</span><span class="sxs-lookup"><span data-stu-id="8c998-177">Optimized "is one of" filtering experience - This feature enables an optimized "is one of" filtering experience that makes it easier to enter multiple filter values, has a simpler mechanism to remove individual or all filter values, and has a more compact and intuitive visualization of filter values.</span></span>

- <span data-ttu-id="8c998-178">推奨されるフィールド - ユーザーは、多くの場合、グリッドまたはページにフィールドを追加する必要があります。</span><span class="sxs-lookup"><span data-stu-id="8c998-178">Recommended fields - Users often need to add fields to a grid or page.</span></span> <span data-ttu-id="8c998-179">多数の使用可能なフィールドでは、これは困難になることがあります。</span><span class="sxs-lookup"><span data-stu-id="8c998-179">This can be difficult with so many available fields.</span></span> <span data-ttu-id="8c998-180">この機能により、大きなリストを通じて検索する代わりに、システムは類似のシナリオでほかのユーザーが最も頻繁に追加する内容に基づいて、一連の推奨されるフィールドを表示することが有効になります。</span><span class="sxs-lookup"><span data-stu-id="8c998-180">Instead of having to search through a large list, this feature enables the system to surface a set of recommended fields based on what other users most often add in similar scenarios.</span></span>

- <span data-ttu-id="8c998-181">グリッド内の既定の付箋アクション - この機能により、グリッド内の既定のアクションは、その列が移動または非表示のどちらであるかに関係なく、グリッド内の特定の列にリンクされます。</span><span class="sxs-lookup"><span data-stu-id="8c998-181">Sticky default actions in grids - This feature ensures that the default action in a grid is linked to a specific column in a grid, regardless of whether that column is moved or hidden.</span></span>

## <a name="see-also"></a><span data-ttu-id="8c998-182">参照</span><span class="sxs-lookup"><span data-stu-id="8c998-182">See also</span></span>

[<span data-ttu-id="8c998-183">Human Resources の新機能および変更された機能</span><span class="sxs-lookup"><span data-stu-id="8c998-183">What's new or changed in Human Resources</span></span>](hr-admin-whats-new.md)</br>
[<span data-ttu-id="8c998-184">Dynamics 365 Human Resources 2019 のリリース ウェーブ 2 の概要</span><span class="sxs-lookup"><span data-stu-id="8c998-184">Overview of Dynamics 365 Human Resources 2019 release wave 2</span></span>](https://docs.microsoft.com/dynamics365-release-plan/2019wave2/dynamics365-human-resources/)</br>
[<span data-ttu-id="8c998-185">更新プロセス</span><span class="sxs-lookup"><span data-stu-id="8c998-185">Update process</span></span>](hr-admin-setup-update-process.md)</br>
[<span data-ttu-id="8c998-186">機能の管理</span><span class="sxs-lookup"><span data-stu-id="8c998-186">Manage features</span></span>](hr-admin-manage-features.md)

[!INCLUDE[footer-include](../includes/footer-banner.md)]