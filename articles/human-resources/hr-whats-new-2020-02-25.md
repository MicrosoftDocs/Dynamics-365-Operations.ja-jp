---
title: Dynamics 365 Human Resources の新機能および変更された機能 (2020 年 2 月 25 日)
description: この記事では、2020 年 2 月 25 日に更新された Microsoft Dynamics 365 Human Resources の新機能、または変更された機能について説明します。
author: andreabichsel
ms.date: 02/25/2020
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
ms.search.validFrom: 2020-02-25
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: 9d9ff9b524a5812bd309fc33d6aa4ba4a92d687b
ms.sourcegitcommit: 879ee8a10e6158885795dce4b3db5077540eec41
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 05/18/2021
ms.locfileid: "6051188"
---
# <a name="whats-new-or-changed-in-dynamics-365-human-resources-february-25-2020"></a><span data-ttu-id="91346-103">Dynamics 365 Human Resources の新機能および変更された機能 (2020 年 2 月 25 日)</span><span class="sxs-lookup"><span data-stu-id="91346-103">What's new or changed in Dynamics 365 Human Resources (February 25, 2020)</span></span>

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

[!include [rename-banner](~/includes/cc-data-platform-banner.md)]

<span data-ttu-id="91346-104">この記事では、Dynamics 365 Human Resources の新機能および変更された機能について説明します。</span><span class="sxs-lookup"><span data-stu-id="91346-104">This article describes features that are either new or changed in Dynamics 365 Human Resources.</span></span> <span data-ttu-id="91346-105">変更は、ビルド番号 8.1.2927 に適用されます。</span><span class="sxs-lookup"><span data-stu-id="91346-105">Changes apply to build number 8.1.2927.</span></span> <span data-ttu-id="91346-106">ヘッダーにあるかっこ内の数字は、参照用の LCS のサポート番号を参照していることがあります。</span><span class="sxs-lookup"><span data-stu-id="91346-106">The numbers in parentheses in some headings refer to LCS support numbers for reference.</span></span>

## <a name="enable-case-management-navigation-and-data-management-framework-dmf-entity-414754"></a><span data-ttu-id="91346-107">ケース管理ナビゲーションおよびデータ管理フレームワーク (DMF) エンティティを有効にする (414754)</span><span class="sxs-lookup"><span data-stu-id="91346-107">Enable Case Management navigation and data management framework (DMF) entity (414754)</span></span>

<span data-ttu-id="91346-108">このプレビュー機能を使用すると、ケース管理ケースへの追加ナビゲーションができます。</span><span class="sxs-lookup"><span data-stu-id="91346-108">This preview feature enables additional navigation to case management cases.</span></span> <span data-ttu-id="91346-109">このプレビュー機能は、**機能管理** ワークスペースで有効にすることができます。</span><span class="sxs-lookup"><span data-stu-id="91346-109">You can enable this preview feature in the **Feature Management** workspace.</span></span> <span data-ttu-id="91346-110">これらのメニュー項目は、Dynamics 365 Human Resources の **コンプライアンス** ワークスペースに表示されます。</span><span class="sxs-lookup"><span data-stu-id="91346-110">These menu items appear in the **Compliance** workspace of Dynamics 365 Human Resources.</span></span> <span data-ttu-id="91346-111">この変更により、Human Resources は次のような情報にアクセスできます。</span><span class="sxs-lookup"><span data-stu-id="91346-111">With this change, Human Resources can access:</span></span>

- <span data-ttu-id="91346-112">すべてのケース</span><span class="sxs-lookup"><span data-stu-id="91346-112">All cases</span></span>
- <span data-ttu-id="91346-113">自分のケース</span><span class="sxs-lookup"><span data-stu-id="91346-113">My cases</span></span>
- <span data-ttu-id="91346-114">自分のオープンなケース</span><span class="sxs-lookup"><span data-stu-id="91346-114">My open cases</span></span>
- <span data-ttu-id="91346-115">自分の期限を過ぎたケース</span><span class="sxs-lookup"><span data-stu-id="91346-115">My overdue cases</span></span>
- <span data-ttu-id="91346-116">ワークフローを使用して自分に割り当てられたケース</span><span class="sxs-lookup"><span data-stu-id="91346-116">Cases assigned to me through workflow</span></span>

<span data-ttu-id="91346-117">これらの新しいビューと共に、**ケースの詳細** DMF エンティティも使用できます。</span><span class="sxs-lookup"><span data-stu-id="91346-117">Along with these new views into cases, the **Case detail** DMF entity is also available.</span></span>

## <a name="enable-relationship-definitions-in-global-address-bbook-414762"></a><span data-ttu-id="91346-118">グローバル アドレス帳でのリレーションシップの定義を有効にする (414762)</span><span class="sxs-lookup"><span data-stu-id="91346-118">Enable Relationship definitions in global address bBook (414762)</span></span>

<span data-ttu-id="91346-119">グローバル アドレス帳でリレーションシップが有効になりました。</span><span class="sxs-lookup"><span data-stu-id="91346-119">Relationships are now enabled in the global address book.</span></span> <span data-ttu-id="91346-120">今週のリリース前までは、**リレーションシップ** 情報ボックスはすべてのシステム定義されたリレーションシップを表示していました。</span><span class="sxs-lookup"><span data-stu-id="91346-120">Prior to this week's release, the **Relationship** fact box displayed any system-defined relationships.</span></span> <span data-ttu-id="91346-121">これで、グローバル アドレス帳ページでこれらのリレーションシップを定義することができます。</span><span class="sxs-lookup"><span data-stu-id="91346-121">Now you can define those relationships within the global address book page.</span></span>

## <a name="a-position-can-be-removed-when-active-compensation-records-exist-for-the-position-414568"></a><span data-ttu-id="91346-122">職位に有効な報酬レコードが存在する場合、その職位を削除できます (414568)</span><span class="sxs-lookup"><span data-stu-id="91346-122">A position can be removed when active compensation records exist for the position (414568)</span></span>

<span data-ttu-id="91346-123">この変更により、職位を削除しようと試みるとき作業者が同じ職位の有効な報酬レコードを持っている場合、警告が表示されます。</span><span class="sxs-lookup"><span data-stu-id="91346-123">With this change, a warning appears when you attempt to delete a position and a worker has an active compensation record for that same position.</span></span> <span data-ttu-id="91346-124">この場合、職位を削除する前に、従業員の固定報酬レコードを更新する必要があります。</span><span class="sxs-lookup"><span data-stu-id="91346-124">When this happens, you must update the employee fixed compensation record before removing the position.</span></span>

## <a name="performance-review-workflow-occasionally-adds-sign-offs-from-people-who-are-not-part-of-the-process-414171"></a><span data-ttu-id="91346-125">業績の確認ワークフローでは、プロセスの一部でない人物からのサイン オフが時折追加されます (414171)</span><span class="sxs-lookup"><span data-stu-id="91346-125">Performance review workflow occasionally adds sign-offs from people who are not part of the process (414171)</span></span>

<span data-ttu-id="91346-126">この変更により、追加のサイン オフ参加者がパフォーマンス レビューに追加される場合に発生する問題を修正します。</span><span class="sxs-lookup"><span data-stu-id="91346-126">This change corrects an issue where additional sign-off participants are added to the performance review.</span></span>

## <a name="worker-position-assignment-not-created-in-dataverse-when-selected-on-the-new-worker-dialog-413479"></a><span data-ttu-id="91346-127">新しい作業者ダイアログで選択した場合、Dataverse で作業者の職位割り当てが作成されません (413479)</span><span class="sxs-lookup"><span data-stu-id="91346-127">Worker position assignment not created in Dataverse when selected on the New Worker dialog (413479)</span></span>

<span data-ttu-id="91346-128">この変更により、新しい作業員を採用して **新しい作業者** ダイアログから新しい採用を職務に割り当てる場合に発生する問題を修正します。</span><span class="sxs-lookup"><span data-stu-id="91346-128">This change corrects an issue when hiring a new worker and assigning the new hire to a position through the **New worker** dialog.</span></span> <span data-ttu-id="91346-129">これで、職位の割り当てが Dataverse に反映されるようになります。</span><span class="sxs-lookup"><span data-stu-id="91346-129">Now the position assignment is reflected in Dataverse.</span></span>

## <a name="coming-soon"></a><span data-ttu-id="91346-130">間もなく公開</span><span class="sxs-lookup"><span data-stu-id="91346-130">Coming soon</span></span>

### <a name="updated-dataverse-solution"></a><span data-ttu-id="91346-131">更新された Dataverse ソリューション</span><span class="sxs-lookup"><span data-stu-id="91346-131">Updated Dataverse solution</span></span>

<span data-ttu-id="91346-132">次の変更により、新しい Dataverse ソリューションがまもなく利用可能になります。</span><span class="sxs-lookup"><span data-stu-id="91346-132">A new Dataverse solution will be available soon with the following changes:</span></span>

| <span data-ttu-id="91346-133">説明</span><span class="sxs-lookup"><span data-stu-id="91346-133">Description</span></span> | <span data-ttu-id="91346-134">計上額</span><span class="sxs-lookup"><span data-stu-id="91346-134">Change</span></span> |
| ----------------------------------------- | --- |
| <span data-ttu-id="91346-135">**職務/職位** エンティティの変更</span><span class="sxs-lookup"><span data-stu-id="91346-135">**Job/Position** entity changes</span></span> | <span data-ttu-id="91346-136">追加された **報酬地域**</span><span class="sxs-lookup"><span data-stu-id="91346-136">**Compensation region** added</span></span></br><span data-ttu-id="91346-137">追加された **財務分析コード**</span><span class="sxs-lookup"><span data-stu-id="91346-137">**Financial dimensions** added</span></span> |
| <span data-ttu-id="91346-138">**作業者** エンティティの変更</span><span class="sxs-lookup"><span data-stu-id="91346-138">**Worker** entity changes</span></span> | <span data-ttu-id="91346-139">追加された **名前の順序**</span><span class="sxs-lookup"><span data-stu-id="91346-139">**Name sequence** added</span></span></br><span data-ttu-id="91346-140">追加された **自宅から作業**</span><span class="sxs-lookup"><span data-stu-id="91346-140">**Works from home** added</span></span></br><span data-ttu-id="91346-141">追加された **言語**</span><span class="sxs-lookup"><span data-stu-id="91346-141">**Language** added</span></span></br><span data-ttu-id="91346-142">追加された **勤続日数**</span><span class="sxs-lookup"><span data-stu-id="91346-142">**Seniority date** added</span></span></br><span data-ttu-id="91346-143">追加された **記念日**</span><span class="sxs-lookup"><span data-stu-id="91346-143">**Anniversary date** added</span></span></br><span data-ttu-id="91346-144">追加された **元の採用日付**</span><span class="sxs-lookup"><span data-stu-id="91346-144">**Original hire date** added</span></span> |
| <span data-ttu-id="91346-145">**雇用** エンティティの変更</span><span class="sxs-lookup"><span data-stu-id="91346-145">**Employment** entity changes</span></span> | <span data-ttu-id="91346-146">追加された **財務分析コード**</span><span class="sxs-lookup"><span data-stu-id="91346-146">**Financial dimensions** added</span></span></br><span data-ttu-id="91346-147">追加された **退職理由**</span><span class="sxs-lookup"><span data-stu-id="91346-147">**Termination reason** added</span></span></br><span data-ttu-id="91346-148">**移行日** から名前変更された **退職日**</span><span class="sxs-lookup"><span data-stu-id="91346-148">**Termination date** renamed from **Transition date**</span></span></br><span data-ttu-id="91346-149">追加された **猶予期間**</span><span class="sxs-lookup"><span data-stu-id="91346-149">**Probation date** added</span></span> |
| <span data-ttu-id="91346-150">**作業者住所** エンティティの変更</span><span class="sxs-lookup"><span data-stu-id="91346-150">**Worker address** entity changes</span></span> | <span data-ttu-id="91346-151">追加された **番地**</span><span class="sxs-lookup"><span data-stu-id="91346-151">**Street address** added</span></span></br><span data-ttu-id="91346-152">廃止としてマークされた **住所行 1**、**住所行 2**、および **住所行 3**</span><span class="sxs-lookup"><span data-stu-id="91346-152">**Address line 1**, **Address line 2**, and **Address line 3** marked for deprecation</span></span> |
| <span data-ttu-id="91346-153">新しい変動報酬の設定エンティティ</span><span class="sxs-lookup"><span data-stu-id="91346-153">New variable compensation setup entities</span></span> | <span data-ttu-id="91346-154">**変動報酬プラン タイプ**</span><span class="sxs-lookup"><span data-stu-id="91346-154">**Compensation variable plan type**</span></span></br><span data-ttu-id="91346-155">**変動報酬プラン**</span><span class="sxs-lookup"><span data-stu-id="91346-155">**Compensation variable plan**</span></span></br><span data-ttu-id="91346-156">**給付ルール**</span><span class="sxs-lookup"><span data-stu-id="91346-156">**Vesting rules**</span></span></br><span data-ttu-id="91346-157">**変動報酬プラン レベル**</span><span class="sxs-lookup"><span data-stu-id="91346-157">**Compensation variable plan level**</span></span> |
| <span data-ttu-id="91346-158">新しい **作業者カレンダー雇用** エンティティ</span><span class="sxs-lookup"><span data-stu-id="91346-158">New **Worker calendar employment** entity</span></span> | <span data-ttu-id="91346-159">追加された **作業カレンダー エンティティ**</span><span class="sxs-lookup"><span data-stu-id="91346-159">**Work calendar entity** added</span></span> |
| <span data-ttu-id="91346-160">新しい **給与職位詳細** エンティティ</span><span class="sxs-lookup"><span data-stu-id="91346-160">New **Payroll position detail** entity</span></span> | <span data-ttu-id="91346-161">追加された **給与職位詳細**</span><span class="sxs-lookup"><span data-stu-id="91346-161">**Payroll position detail** added</span></span> |
| <span data-ttu-id="91346-162">新しい **肩書** エンティティ</span><span class="sxs-lookup"><span data-stu-id="91346-162">New **Title** entity</span></span> | <span data-ttu-id="91346-163">追加済み **タイトル**。</span><span class="sxs-lookup"><span data-stu-id="91346-163">**Title** added.</span></span> <span data-ttu-id="91346-164">新しい **タイトル** エンティティが、Human Resources と Dataverse の間の同期プロセスに含まれます。</span><span class="sxs-lookup"><span data-stu-id="91346-164">The new **Title** entity will be included in the sync process between Human Resources and Dataverse.</span></span> <span data-ttu-id="91346-165">**職位** または **ジョブ** エンティティから最初に参照されることはありません。</span><span class="sxs-lookup"><span data-stu-id="91346-165">It won't be initially referenced from **Job Position** or **Job** entities.</span></span> |

<span data-ttu-id="91346-166">今後数週間のうちに、これらのエンティティの変更がすべての環境で使用できるようになります。</span><span class="sxs-lookup"><span data-stu-id="91346-166">Over the next few weeks, these entity changes will be available in all environments.</span></span> <span data-ttu-id="91346-167">Human Resources の最新 Dataverse ソリューションを手動でインストールするには、次の操作を行います。</span><span class="sxs-lookup"><span data-stu-id="91346-167">To manually install the latest Dataverse solution for Human Resources:</span></span>

1.  <span data-ttu-id="91346-168">[Power Platform 管理センター](https://admin.powerplatform.microsoft.com) に移動します。</span><span class="sxs-lookup"><span data-stu-id="91346-168">Go to the [Power Platform Admin Center](https://admin.powerplatform.microsoft.com).</span></span>

2.  <span data-ttu-id="91346-169">**環境** を選択します。</span><span class="sxs-lookup"><span data-stu-id="91346-169">Select **Environments**.</span></span>

3.  <span data-ttu-id="91346-170">アップグレードする環境を検索します。</span><span class="sxs-lookup"><span data-stu-id="91346-170">Find the environment you want to upgrade.</span></span> <span data-ttu-id="91346-171">これは、Human Resources の **バージョン情報** フォームで、**Common Data Service 情報** セクションの **環境名** に対応している必要があります。</span><span class="sxs-lookup"><span data-stu-id="91346-171">This should correspond to **Environment name** in the **Common Data Service information** section in the **About** form in Human Resources.</span></span>

4.  <span data-ttu-id="91346-172">環境の詳細を表示するための環境を選択します。</span><span class="sxs-lookup"><span data-stu-id="91346-172">Select the environment to view the environment details.</span></span>

5.  <span data-ttu-id="91346-173">上部の操作バーで、**ソリューションの管理** を選択します。</span><span class="sxs-lookup"><span data-stu-id="91346-173">In the action bar at the top, select **Manage Solutions**.</span></span> <span data-ttu-id="91346-174">新しいブラウザー ウィンドウが開き、環境のコンテキストで **Dynamics 365 管理センター** に移動します。</span><span class="sxs-lookup"><span data-stu-id="91346-174">A new browser window will open and navigate to **Dynamics 365 Administration Center** in the context of your environment.</span></span>

6.  <span data-ttu-id="91346-175">**ソリューション** リストで、**Dynamics 365 Human Resources アンカー** を選択します。</span><span class="sxs-lookup"><span data-stu-id="91346-175">In the **Solution** list, select **Dynamics 365 Human Resources Anchor**.</span></span>

7.  <span data-ttu-id="91346-176">最新のソリューションを適用するには、**アップグレード** を選択します。</span><span class="sxs-lookup"><span data-stu-id="91346-176">Select **Upgrade** to apply the latest solution.</span></span>

## <a name="in-preview"></a><span data-ttu-id="91346-177">プレビュー</span><span class="sxs-lookup"><span data-stu-id="91346-177">In preview</span></span>

<span data-ttu-id="91346-178">次のプレビュー機能が 2020 年 2 月 3 日に利用可能になります。</span><span class="sxs-lookup"><span data-stu-id="91346-178">The following preview features became available on February 3, 2020:</span></span>

- <span data-ttu-id="91346-179">**休暇および欠勤のプレビュー機能** - 詳細については、[休暇および欠勤のプレビュー機能](hr-leave-and-absence-overview.md?leave-and-absence-preview-features) を参照してください。</span><span class="sxs-lookup"><span data-stu-id="91346-179">**Leave and absence preview features** - For more information, see [Leave and absence preview features](hr-leave-and-absence-overview.md?leave-and-absence-preview-features).</span></span>

- <span data-ttu-id="91346-180">**福利厚生管理プレビュー機能** - 既知の問題など、詳細については[福利厚生管理の概要](hr-benefits-management-overview.md)を参照してください。</span><span class="sxs-lookup"><span data-stu-id="91346-180">**Benefits management preview feature** - For more information, including known issues, see [Benefits management overview](hr-benefits-management-overview.md).</span></span>

## <a name="see-also"></a><span data-ttu-id="91346-181">参照</span><span class="sxs-lookup"><span data-stu-id="91346-181">See also</span></span>

[<span data-ttu-id="91346-182">Human Resources の新機能および変更された機能</span><span class="sxs-lookup"><span data-stu-id="91346-182">What's new or changed in Human Resources</span></span>](hr-admin-whats-new.md)</br>
[<span data-ttu-id="91346-183">Dynamics 365 Human Resources 2019 のリリース ウェーブ 2 の概要</span><span class="sxs-lookup"><span data-stu-id="91346-183">Overview of Dynamics 365 Human Resources 2019 release wave 2</span></span>](/dynamics365-release-plan/2019wave2/dynamics365-human-resources/)</br>
[<span data-ttu-id="91346-184">更新プロセス</span><span class="sxs-lookup"><span data-stu-id="91346-184">Update process</span></span>](hr-admin-setup-update-process.md)</br>
[<span data-ttu-id="91346-185">機能の管理</span><span class="sxs-lookup"><span data-stu-id="91346-185">Manage features</span></span>](hr-admin-manage-features.md)

[!INCLUDE[footer-include](../includes/footer-banner.md)]