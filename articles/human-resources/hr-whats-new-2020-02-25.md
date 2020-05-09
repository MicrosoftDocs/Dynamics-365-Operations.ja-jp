---
title: Dynamics 365 Human Resources の新機能および変更された機能 (2020 年 2 月 25 日)
description: この記事では、Microsoft Dynamics 365 Human Resources の新機能または変更された機能について説明します。
author: Darinkramer
manager: AnnBe
ms.date: 02/25/2020
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
ms.search.validFrom: 2020-02-25
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: 720b4e03549a059c8945bec9d27de9cdcaada488
ms.sourcegitcommit: f38302b9430f2ab3efe91d0a7beff946bc610e8f
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 02/28/2020
ms.locfileid: "3092755"
---
# <a name="whats-new-or-changed-in-dynamics-365-human-resources-february-25-2020"></a><span data-ttu-id="3ca3d-103">Dynamics 365 Human Resources の新機能および変更された機能 (2020 年 2 月 25 日)</span><span class="sxs-lookup"><span data-stu-id="3ca3d-103">What's new or changed in Dynamics 365 Human Resources (February 25, 2020)</span></span>

<span data-ttu-id="3ca3d-104">この記事では、Dynamics 365 Human Resources の新機能および変更された機能について説明します。</span><span class="sxs-lookup"><span data-stu-id="3ca3d-104">This article describes features that are either new or changed in Dynamics 365 Human Resources.</span></span> <span data-ttu-id="3ca3d-105">変更は、ビルド番号 8.1.2927 に適用されます。</span><span class="sxs-lookup"><span data-stu-id="3ca3d-105">Changes apply to build number 8.1.2927.</span></span> <span data-ttu-id="3ca3d-106">ヘッダーにあるかっこ内の数字は、参照用の LCS のサポート番号を参照していることがあります。</span><span class="sxs-lookup"><span data-stu-id="3ca3d-106">The numbers in parentheses in some headings refer to LCS support numbers for reference.</span></span>

## <a name="enable-case-management-navigation-and-data-management-framework-dmf-entity-414754"></a><span data-ttu-id="3ca3d-107">ケース管理ナビゲーションおよびデータ管理フレームワーク (DMF) エンティティを有効にする (414754)</span><span class="sxs-lookup"><span data-stu-id="3ca3d-107">Enable Case Management navigation and data management framework (DMF) entity (414754)</span></span>

<span data-ttu-id="3ca3d-108">このプレビュー機能を使用すると、ケース管理ケースへの追加ナビゲーションができます。</span><span class="sxs-lookup"><span data-stu-id="3ca3d-108">This preview feature enables additional navigation to case management cases.</span></span> <span data-ttu-id="3ca3d-109">このプレビュー機能は、**機能管理**ワークスペースで有効にすることができます。</span><span class="sxs-lookup"><span data-stu-id="3ca3d-109">You can enable this preview feature in the **Feature Management** workspace.</span></span> <span data-ttu-id="3ca3d-110">これらのメニュー項目は、Dynamics 365 Human Resources の**コンプライアンス** ワークスペースに表示されます。</span><span class="sxs-lookup"><span data-stu-id="3ca3d-110">These menu items appear in the **Compliance** workspace of Dynamics 365 Human Resources.</span></span> <span data-ttu-id="3ca3d-111">この変更により、Human Resources は次のような情報にアクセスできます。</span><span class="sxs-lookup"><span data-stu-id="3ca3d-111">With this change, Human Resources can access:</span></span>

- <span data-ttu-id="3ca3d-112">すべてのケース</span><span class="sxs-lookup"><span data-stu-id="3ca3d-112">All cases</span></span>
- <span data-ttu-id="3ca3d-113">自分のケース</span><span class="sxs-lookup"><span data-stu-id="3ca3d-113">My cases</span></span>
- <span data-ttu-id="3ca3d-114">自分のオープンなケース</span><span class="sxs-lookup"><span data-stu-id="3ca3d-114">My open cases</span></span>
- <span data-ttu-id="3ca3d-115">自分の期限を過ぎたケース</span><span class="sxs-lookup"><span data-stu-id="3ca3d-115">My overdue cases</span></span>
- <span data-ttu-id="3ca3d-116">ワークフローを使用して自分に割り当てられたケース</span><span class="sxs-lookup"><span data-stu-id="3ca3d-116">Cases assigned to me through workflow</span></span>

<span data-ttu-id="3ca3d-117">これらの新しいビューと共に、**ケースの詳細** DMF エンティティも使用できます。</span><span class="sxs-lookup"><span data-stu-id="3ca3d-117">Along with these new views into cases, the **Case detail** DMF entity is also available.</span></span>

## <a name="enable-relationship-definitions-in-global-address-bbook-414762"></a><span data-ttu-id="3ca3d-118">グローバル アドレス帳でのリレーションシップの定義を有効にする (414762)</span><span class="sxs-lookup"><span data-stu-id="3ca3d-118">Enable Relationship definitions in global address bBook (414762)</span></span>

<span data-ttu-id="3ca3d-119">グローバル アドレス帳でリレーションシップが有効になりました。</span><span class="sxs-lookup"><span data-stu-id="3ca3d-119">Relationships are now enabled in the global address book.</span></span> <span data-ttu-id="3ca3d-120">今週のリリース前までは、**リレーションシップ**情報ボックスはすべてのシステム定義されたリレーションシップを表示していました。</span><span class="sxs-lookup"><span data-stu-id="3ca3d-120">Prior to this week's release, the **Relationship** fact box displayed any system-defined relationships.</span></span> <span data-ttu-id="3ca3d-121">これで、グローバル アドレス帳ページでこれらのリレーションシップを定義することができます。</span><span class="sxs-lookup"><span data-stu-id="3ca3d-121">Now you can define those relationships within the global address book page.</span></span>

## <a name="a-position-can-be-removed-when-active-compensation-records-exist-for-the-position-414568"></a><span data-ttu-id="3ca3d-122">職位に有効な報酬レコードが存在する場合、その職位を削除できます (414568)</span><span class="sxs-lookup"><span data-stu-id="3ca3d-122">A position can be removed when active compensation records exist for the position (414568)</span></span>

<span data-ttu-id="3ca3d-123">この変更により、職位を削除しようと試みるとき作業者が同じ職位の有効な報酬レコードを持っている場合、警告が表示されます。</span><span class="sxs-lookup"><span data-stu-id="3ca3d-123">With this change, a warning appears when you attempt to delete a position and a worker has an active compensation record for that same position.</span></span> <span data-ttu-id="3ca3d-124">この場合、職位を削除する前に、従業員の固定報酬レコードを更新する必要があります。</span><span class="sxs-lookup"><span data-stu-id="3ca3d-124">When this happens, you must update the employee fixed compensation record before removing the position.</span></span>

## <a name="performance-review-workflow-occasionally-adds-sign-offs-from-people-who-are-not-part-of-the-process-414171"></a><span data-ttu-id="3ca3d-125">業績の確認ワークフローでは、プロセスの一部でない人物からのサイン オフが時折追加されます (414171)</span><span class="sxs-lookup"><span data-stu-id="3ca3d-125">Performance review workflow occasionally adds sign-offs from people who are not part of the process (414171)</span></span>

<span data-ttu-id="3ca3d-126">この変更により、追加のサイン オフ参加者がパフォーマンス レビューに追加される場合に発生する問題を修正します。</span><span class="sxs-lookup"><span data-stu-id="3ca3d-126">This change corrects an issue where additional sign-off participants are added to the performance review.</span></span>

## <a name="worker-position-assignment-not-created-in-common-data-service-when-selected-on-the-new-worker-dialog-413479"></a><span data-ttu-id="3ca3d-127">新しい作業者ダイアログで選択した場合、Common Data Service で作業者の職位割り当てが作成されません (413479)</span><span class="sxs-lookup"><span data-stu-id="3ca3d-127">Worker position assignment not created in Common Data Service when selected on the New Worker dialog (413479)</span></span>

<span data-ttu-id="3ca3d-128">この変更により、新しい作業員を採用して**新しい作業者**ダイアログから新しい採用を職務に割り当てる場合に発生する問題を修正します。</span><span class="sxs-lookup"><span data-stu-id="3ca3d-128">This change corrects an issue when hiring a new worker and assigning the new hire to a position through the **New worker** dialog.</span></span> <span data-ttu-id="3ca3d-129">これで、職位の割り当てが Common Data Service に反映されるようになります。</span><span class="sxs-lookup"><span data-stu-id="3ca3d-129">Now the position assignment is reflected in Common Data Service.</span></span>

## <a name="coming-soon"></a><span data-ttu-id="3ca3d-130">間もなく公開</span><span class="sxs-lookup"><span data-stu-id="3ca3d-130">Coming soon</span></span>

### <a name="updated-common-data-service-solution"></a><span data-ttu-id="3ca3d-131">更新された Common Data Service ソリューション</span><span class="sxs-lookup"><span data-stu-id="3ca3d-131">Updated Common Data Service solution</span></span>

<span data-ttu-id="3ca3d-132">次の変更により、新しい Common Data Service ソリューションがまもなく利用可能になります。</span><span class="sxs-lookup"><span data-stu-id="3ca3d-132">A new Common Data Service solution will be available soon with the following changes:</span></span>

| <span data-ttu-id="3ca3d-133">説明</span><span class="sxs-lookup"><span data-stu-id="3ca3d-133">Description</span></span> | <span data-ttu-id="3ca3d-134">計上額</span><span class="sxs-lookup"><span data-stu-id="3ca3d-134">Change</span></span> |
| ----------------------------------------- | --- |
| <span data-ttu-id="3ca3d-135">**職務/職位**エンティティの変更</span><span class="sxs-lookup"><span data-stu-id="3ca3d-135">**Job/Position** entity changes</span></span> | <span data-ttu-id="3ca3d-136">追加された**報酬地域**</span><span class="sxs-lookup"><span data-stu-id="3ca3d-136">**Compensation region** added</span></span></br><span data-ttu-id="3ca3d-137">追加された**財務分析コード**</span><span class="sxs-lookup"><span data-stu-id="3ca3d-137">**Financial dimensions** added</span></span> |
| <span data-ttu-id="3ca3d-138">**作業者**エンティティの変更</span><span class="sxs-lookup"><span data-stu-id="3ca3d-138">**Worker** entity changes</span></span> | <span data-ttu-id="3ca3d-139">追加された**名前の順序**</span><span class="sxs-lookup"><span data-stu-id="3ca3d-139">**Name sequence** added</span></span></br><span data-ttu-id="3ca3d-140">追加された**自宅から作業**</span><span class="sxs-lookup"><span data-stu-id="3ca3d-140">**Works from home** added</span></span></br><span data-ttu-id="3ca3d-141">追加された**言語**</span><span class="sxs-lookup"><span data-stu-id="3ca3d-141">**Language** added</span></span></br><span data-ttu-id="3ca3d-142">追加された**勤続日数**</span><span class="sxs-lookup"><span data-stu-id="3ca3d-142">**Seniority date** added</span></span></br><span data-ttu-id="3ca3d-143">追加された**記念日**</span><span class="sxs-lookup"><span data-stu-id="3ca3d-143">**Anniversary date** added</span></span></br><span data-ttu-id="3ca3d-144">追加された**元の採用日付**</span><span class="sxs-lookup"><span data-stu-id="3ca3d-144">**Original hire date** added</span></span> |
| <span data-ttu-id="3ca3d-145">**雇用**エンティティの変更</span><span class="sxs-lookup"><span data-stu-id="3ca3d-145">**Employment** entity changes</span></span> | <span data-ttu-id="3ca3d-146">追加された**財務分析コード**</span><span class="sxs-lookup"><span data-stu-id="3ca3d-146">**Financial dimensions** added</span></span></br><span data-ttu-id="3ca3d-147">追加された**退職理由**</span><span class="sxs-lookup"><span data-stu-id="3ca3d-147">**Termination reason** added</span></span></br><span data-ttu-id="3ca3d-148">**移行日**から名前変更された**退職日**</span><span class="sxs-lookup"><span data-stu-id="3ca3d-148">**Termination date** renamed from **Transition date**</span></span></br><span data-ttu-id="3ca3d-149">追加された**猶予期間**</span><span class="sxs-lookup"><span data-stu-id="3ca3d-149">**Probation date** added</span></span> |
| <span data-ttu-id="3ca3d-150">**作業者住所**エンティティの変更</span><span class="sxs-lookup"><span data-stu-id="3ca3d-150">**Worker address** entity changes</span></span> | <span data-ttu-id="3ca3d-151">追加された**番地**</span><span class="sxs-lookup"><span data-stu-id="3ca3d-151">**Street address** added</span></span></br><span data-ttu-id="3ca3d-152">廃止としてマークされた**住所行 1**、**住所行 2**、および**住所行 3**</span><span class="sxs-lookup"><span data-stu-id="3ca3d-152">**Address line 1**, **Address line 2**, and **Address line 3** marked for deprecation</span></span> |
| <span data-ttu-id="3ca3d-153">新しい変動報酬の設定エンティティ</span><span class="sxs-lookup"><span data-stu-id="3ca3d-153">New variable compensation setup entities</span></span> | <span data-ttu-id="3ca3d-154">**変動報酬プラン タイプ**</span><span class="sxs-lookup"><span data-stu-id="3ca3d-154">**Compensation variable plan type**</span></span></br><span data-ttu-id="3ca3d-155">**変動報酬プラン**</span><span class="sxs-lookup"><span data-stu-id="3ca3d-155">**Compensation variable plan**</span></span></br><span data-ttu-id="3ca3d-156">**給付ルール**</span><span class="sxs-lookup"><span data-stu-id="3ca3d-156">**Vesting rules**</span></span></br><span data-ttu-id="3ca3d-157">**変動報酬プラン レベル**</span><span class="sxs-lookup"><span data-stu-id="3ca3d-157">**Compensation variable plan level**</span></span> |
| <span data-ttu-id="3ca3d-158">新しい**作業者カレンダー雇用**エンティティ</span><span class="sxs-lookup"><span data-stu-id="3ca3d-158">New **Worker calendar employment** entity</span></span> | <span data-ttu-id="3ca3d-159">追加された**作業カレンダー エンティティ**</span><span class="sxs-lookup"><span data-stu-id="3ca3d-159">**Work calendar entity** added</span></span> |
| <span data-ttu-id="3ca3d-160">新しい**給与職位詳細**エンティティ</span><span class="sxs-lookup"><span data-stu-id="3ca3d-160">New **Payroll position detail** entity</span></span> | <span data-ttu-id="3ca3d-161">追加された**給与職位詳細**</span><span class="sxs-lookup"><span data-stu-id="3ca3d-161">**Payroll position detail** added</span></span> |
| <span data-ttu-id="3ca3d-162">新しい**肩書**エンティティ</span><span class="sxs-lookup"><span data-stu-id="3ca3d-162">New **Title** entity</span></span> | <span data-ttu-id="3ca3d-163">追加済み**タイトル**。</span><span class="sxs-lookup"><span data-stu-id="3ca3d-163">**Title** added.</span></span> <span data-ttu-id="3ca3d-164">新しい**タイトル** エンティティが、Human Resources と Common Data Service の間の同期プロセスに含まれます。</span><span class="sxs-lookup"><span data-stu-id="3ca3d-164">The new **Title** entity will be included in the sync process between Human Resources and Common Data Service.</span></span> <span data-ttu-id="3ca3d-165">**職位**または**ジョブ** エンティティから最初に参照されることはありません。</span><span class="sxs-lookup"><span data-stu-id="3ca3d-165">It won't be initially referenced from **Job Position** or **Job** entities.</span></span> |

<span data-ttu-id="3ca3d-166">今後数週間のうちに、これらのエンティティの変更がすべての環境で使用できるようになります。</span><span class="sxs-lookup"><span data-stu-id="3ca3d-166">Over the next few weeks, these entity changes will be available in all environments.</span></span> <span data-ttu-id="3ca3d-167">Human Resources の最新 Common Data Service ソリューションを手動でインストールするには、次の操作を行います。</span><span class="sxs-lookup"><span data-stu-id="3ca3d-167">To manually install the latest Common Data Service solution for Human Resources:</span></span>

1.  <span data-ttu-id="3ca3d-168">[Power Platform 管理センター](https://admin.powerplatform.microsoft.com) に移動します。</span><span class="sxs-lookup"><span data-stu-id="3ca3d-168">Go to the [Power Platform Admin Center](https://admin.powerplatform.microsoft.com).</span></span>

2.  <span data-ttu-id="3ca3d-169">**環境**を選択します。</span><span class="sxs-lookup"><span data-stu-id="3ca3d-169">Select **Environments**.</span></span>

3.  <span data-ttu-id="3ca3d-170">アップグレードする環境を検索します。</span><span class="sxs-lookup"><span data-stu-id="3ca3d-170">Find the environment you want to upgrade.</span></span> <span data-ttu-id="3ca3d-171">これは、Human Resources の**バージョン情報**フォームで、**Common Data Service 情報**セクションの**環境名**に対応している必要があります。</span><span class="sxs-lookup"><span data-stu-id="3ca3d-171">This should correspond to **Environment name** in the **Common Data Service information** section in the **About** form in Human Resources.</span></span>

4.  <span data-ttu-id="3ca3d-172">環境の詳細を表示するための環境を選択します。</span><span class="sxs-lookup"><span data-stu-id="3ca3d-172">Select the environment to view the environment details.</span></span>

5.  <span data-ttu-id="3ca3d-173">上部の操作バーで、**ソリューションの管理**を選択します。</span><span class="sxs-lookup"><span data-stu-id="3ca3d-173">In the action bar at the top, select **Manage Solutions**.</span></span> <span data-ttu-id="3ca3d-174">新しいブラウザー ウィンドウが開き、環境のコンテキストで**Dynamics 365 管理センター**に移動します。</span><span class="sxs-lookup"><span data-stu-id="3ca3d-174">A new browser window will open and navigate to **Dynamics 365 Administration Center** in the context of your environment.</span></span>

6.  <span data-ttu-id="3ca3d-175">**ソリューション** リストで、**Dynamics 365 Human Resources アンカー**を選択します。</span><span class="sxs-lookup"><span data-stu-id="3ca3d-175">In the **Solution** list, select **Dynamics 365 Human Resources Anchor**.</span></span>

7.  <span data-ttu-id="3ca3d-176">最新のソリューションを適用するには、**アップグレード**を選択します。</span><span class="sxs-lookup"><span data-stu-id="3ca3d-176">Select **Upgrade** to apply the latest solution.</span></span>

## <a name="in-preview"></a><span data-ttu-id="3ca3d-177">プレビュー</span><span class="sxs-lookup"><span data-stu-id="3ca3d-177">In preview</span></span>

<span data-ttu-id="3ca3d-178">次のプレビュー機能が 2020 年 2 月 3 日に利用可能になります。</span><span class="sxs-lookup"><span data-stu-id="3ca3d-178">The following preview features became available on February 3, 2020:</span></span>

- <span data-ttu-id="3ca3d-179">**休暇および欠勤のプレビュー機能** - 詳細については、[休暇および欠勤のプレビュー機能](hr-leave-and-absence-overview.md?leave-and-absence-preview-features) を参照してください。</span><span class="sxs-lookup"><span data-stu-id="3ca3d-179">**Leave and absence preview features** - For more information, see [Leave and absence preview features](hr-leave-and-absence-overview.md?leave-and-absence-preview-features).</span></span>

- <span data-ttu-id="3ca3d-180">**福利厚生管理プレビュー機能** - 既知の問題など、詳細については[福利厚生管理の概要](hr-benefits-management-overview.md)を参照してください。</span><span class="sxs-lookup"><span data-stu-id="3ca3d-180">**Benefits management preview feature** - For more information, including known issues, see [Benefits management overview](hr-benefits-management-overview.md).</span></span>