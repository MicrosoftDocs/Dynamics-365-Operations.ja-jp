---
title: 優先順位に基づくバッチスケジューリング
description: このトピックでは、優先順位に基づくバッチスケジューリングの機能について説明します。
author: peakerbl
manager: AnnBe
ms.date: 11/07/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-platform
ms.technology: ''
audience: IT Pro
ms.reviewer: kfend
ms.search.scope: Core, Operations
ms.custom: 62333
ms.assetid: ''
ms.search.region: Global
ms.author: hasaid
ms.search.validFrom: 2019-10-29
ms.dyn365.ops.version: Platform Update31
ms.openlocfilehash: 0e9a69fc5be52801d7a763ac12dfa84074d1dd03
ms.sourcegitcommit: ddaa4bcfaee503e883efc710fd444fba8db4c2fb
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 11/07/2019
ms.locfileid: "2775013"
---
# <a name="priority-based-batch-scheduling"></a><span data-ttu-id="621c6-103">優先順位に基づくバッチスケジューリング</span><span class="sxs-lookup"><span data-stu-id="621c6-103">Priority-based batch scheduling</span></span> 

[!include [banner](../includes/banner.md)]
[!include [banner](../includes/preview-banner.md)]

<span data-ttu-id="621c6-104">プラットフォーム アップデート 31 では、[機能管理](../../fin-ops/get-started/feature-management/feature-management-overview.md) の **バッチ優先順位に基づくスケジューリング** 機能を有効にすることができます。</span><span class="sxs-lookup"><span data-stu-id="621c6-104">In Platform update 31, you can turn on the **Batch priority-based scheduling** feature in [Feature management](../../fin-ops/get-started/feature-management/feature-management-overview.md).</span></span> <span data-ttu-id="621c6-105">優先順位に基づくスケジューリングでは、バッチグループをバッチサーバーから切り離します。</span><span class="sxs-lookup"><span data-stu-id="621c6-105">Priority-based scheduling decouples batch groups from the batch server.</span></span> <span data-ttu-id="621c6-106">代わりに、使用可能なバッチサーバー間でタスクが実行される順序を決定するために、相対的なスケジューリング優先順位が使用されます。</span><span class="sxs-lookup"><span data-stu-id="621c6-106">Instead, relative scheduling priorities are used to determine the order that tasks are run in across available batch servers.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="621c6-107">この機能は、プラットフォーム アップデート 31 の一部として、制限されたプレビューでのみ使用できます。</span><span class="sxs-lookup"><span data-stu-id="621c6-107">This feature is available only in a restricted preview as part of Platform update 31.</span></span>

<span data-ttu-id="621c6-108">スケジューリング優先順位はバッチ グループに対して定義されますが、特定のバッチ ジョブに対して上書きすることができます。</span><span class="sxs-lookup"><span data-stu-id="621c6-108">A scheduling priority is defined for batch groups, but it can be overridden for specific batch jobs.</span></span> <span data-ttu-id="621c6-109">スケジュールの優先順位の分類は、相対的な優先順位を宣言したり、ジョブおよび業務プロセスの処理順序を決定するために使用されます。</span><span class="sxs-lookup"><span data-stu-id="621c6-109">The scheduling priority classifications are used to declare relative priorities and to determine the processing order of jobs and business processes.</span></span> <span data-ttu-id="621c6-110">スケジューリング優先順位に使用できる値は、**低**、**通常**、**高**、**重大**、**予約済みキャパシティ** です。</span><span class="sxs-lookup"><span data-stu-id="621c6-110">The available values for the scheduling priority are **Low**, **Normal**, **High**, **Critical**, and **Reserved capacity**.</span></span> <span data-ttu-id="621c6-111">**予約済キャパシティ** は、最も高い優先順位を表します。</span><span class="sxs-lookup"><span data-stu-id="621c6-111">**Reserved capacity** represents the highest priority.</span></span>

<span data-ttu-id="621c6-112">今後の更新に対して追加の機能が計画されています。</span><span class="sxs-lookup"><span data-stu-id="621c6-112">Additional functionality is planned for future updates.</span></span>

<span data-ttu-id="621c6-113">優先順位に基づくバッチ スケジューリングでは、機能管理での **バッチ フレームワークの競合軽減**機能を有効にする必要があります。</span><span class="sxs-lookup"><span data-stu-id="621c6-113">Priority-based batch scheduling requires that you turn on the **Batch framework contention reduction** feature in Feature management.</span></span>

<span data-ttu-id="621c6-114">次の手順では、**優先順位に基づくバッチ スケジューリング**機能が有効になっている場合に、バッチ グループ、ジョブ、およびタスクと作業する方法について説明します。</span><span class="sxs-lookup"><span data-stu-id="621c6-114">The following procedures explain how to work with batch groups, jobs, and tasks, when the **Priority based batch scheduling** feature is turned on.</span></span>

## <a name="batch-groups"></a><span data-ttu-id="621c6-115">バッチ グループ</span><span class="sxs-lookup"><span data-stu-id="621c6-115">Batch groups</span></span>

<span data-ttu-id="621c6-116">バッチ グループは、ジョブを論理的にグループ化し、既定のスケジューリング優先順位を設定するためにのみ使用されるようになりました。</span><span class="sxs-lookup"><span data-stu-id="621c6-116">Batch groups are now used only to logically group jobs and to set the default scheduling priority.</span></span> <span data-ttu-id="621c6-117">バッチ グループの例を次に示します:</span><span class="sxs-lookup"><span data-stu-id="621c6-117">Here are some examples of batch groups:</span></span>

- <span data-ttu-id="621c6-118">特定の業務プロセスに属するジョブ</span><span class="sxs-lookup"><span data-stu-id="621c6-118">Jobs that belong to a specific business process</span></span>
- <span data-ttu-id="621c6-119">同じ実行の繰り返しが設定されているジョブ (たとえば、毎晩、毎週、毎月など)</span><span class="sxs-lookup"><span data-stu-id="621c6-119">Jobs that have the same execution recurrence (for example every night, every week, or every month)</span></span>
- <span data-ttu-id="621c6-120">優先順位が同じジョブ</span><span class="sxs-lookup"><span data-stu-id="621c6-120">Jobs that have the same priority</span></span>

### <a name="create-a-batch-group"></a><span data-ttu-id="621c6-121">バッチ グループの作成</span><span class="sxs-lookup"><span data-stu-id="621c6-121">Create a batch group</span></span>

1. <span data-ttu-id="621c6-122">**システム管理** \> **設定** \> **バッチ グループ** の順に移動します。</span><span class="sxs-lookup"><span data-stu-id="621c6-122">Go to **System administration** \> **Setup** \> **Batch group**.</span></span>
2. <span data-ttu-id="621c6-123">**新規** を選択して、新しいバッチ グループを作成します。</span><span class="sxs-lookup"><span data-stu-id="621c6-123">Select **New** to create a batch group.</span></span>
3. <span data-ttu-id="621c6-124">**グループ** フィールドで、そのバッチ グループに対して固有の名前を入力します。</span><span class="sxs-lookup"><span data-stu-id="621c6-124">In the **Group** field, enter a unique name for the batch group.</span></span>
4. <span data-ttu-id="621c6-125">**説明**フィールドで値を入力します。</span><span class="sxs-lookup"><span data-stu-id="621c6-125">In the **Description** field, enter a value.</span></span>
5. <span data-ttu-id="621c6-126"> **スケジューリング優先順位** フィールドで、バッチ グループ内のバッチ ジョブの既定のスケジューリング優先順位を選択します。</span><span class="sxs-lookup"><span data-stu-id="621c6-126">In the **Scheduling priority** field, select the default scheduling priority for the batch jobs in the batch group.</span></span>
6. <span data-ttu-id="621c6-127">**保存** を選択します。</span><span class="sxs-lookup"><span data-stu-id="621c6-127">Select **Save**.</span></span>

## <a name="batch-jobs"></a><span data-ttu-id="621c6-128">バッチ ジョブ</span><span class="sxs-lookup"><span data-stu-id="621c6-128">Batch jobs</span></span>

<span data-ttu-id="621c6-129">バッチ ジョブは、自動処理のために送信されるタスクのグループです。</span><span class="sxs-lookup"><span data-stu-id="621c6-129">A batch job is a group of tasks that are submitted for automatic processing.</span></span> <span data-ttu-id="621c6-130">バッチ ジョブは、**実行者** フィールドで選択されたユーザーのセキュリティ資格情報を使用して実行されます。</span><span class="sxs-lookup"><span data-stu-id="621c6-130">Batch jobs are run by using the security credentials of the user who is selected in **Run by** field.</span></span> <span data-ttu-id="621c6-131">バッチ ジョブを作成するには、次の手順に従います。</span><span class="sxs-lookup"><span data-stu-id="621c6-131">Use the following procedure to create a batch job.</span></span>

### <a name="create-a-batch-job"></a><span data-ttu-id="621c6-132">バッチ ジョブの作成</span><span class="sxs-lookup"><span data-stu-id="621c6-132">Create a batch job</span></span>

1. <span data-ttu-id="621c6-133">**システム管理** \> **照会** \> **バッチ ジョブ** の順に移動します。</span><span class="sxs-lookup"><span data-stu-id="621c6-133">Go to **System administration** \> **Inquiries** \> **Batch jobs**.</span></span>
2. <span data-ttu-id="621c6-134">**新規** を選択して、新しいバッチ ジョブを作成します。</span><span class="sxs-lookup"><span data-stu-id="621c6-134">Select **New** to create a batch job.</span></span>
3. <span data-ttu-id="621c6-135">**職務明細書**フィールドに値を入力します。</span><span class="sxs-lookup"><span data-stu-id="621c6-135">In the **Job description** field, enter a value.</span></span>
4. <span data-ttu-id="621c6-136">**開始予定日時**フィールドに、日時を入力します。</span><span class="sxs-lookup"><span data-stu-id="621c6-136">In the **Scheduled start date/time** field, enter a date and time.</span></span>
5. <span data-ttu-id="621c6-137">**実行者** フィールドで、バッチジョブの実行時に使用するセキュリティ資格情報を持つユーザーを選択します。</span><span class="sxs-lookup"><span data-stu-id="621c6-137">In the **Run by** field, select the users whose security credentials will be used when the batch job is run.</span></span> <span data-ttu-id="621c6-138">詳細については、[バッチ管理者のセキュリティ ロール](runby.md) を参照してください。</span><span class="sxs-lookup"><span data-stu-id="621c6-138">For more information, see [Batch manager security role](runby.md).</span></span>
6. <span data-ttu-id="621c6-139">オプション: **監視カテゴリ** フィールドで、監視中にジョブのタイプを容易に識別できるように値を選択します。</span><span class="sxs-lookup"><span data-stu-id="621c6-139">Optional: In the **Monitoring category** field, select a value to make it easier to identify the types of jobs during monitoring.</span></span>
7. <span data-ttu-id="621c6-140">オプション: **重要なジョブ**　オプションを **はい** に設定します。</span><span class="sxs-lookup"><span data-stu-id="621c6-140">Optional: Set the **Critical job** option to **Yes**.</span></span> <span data-ttu-id="621c6-141">詳細については、[ユーザーを一括でインポートする](tasks/import-bulk-users.md) または [重大としてバッチ ジョブを処理するときのワークフロー メッセージを構成する](../../fin-ops/organization-administration/workflow-batch-job-critical.md) を参照してください。</span><span class="sxs-lookup"><span data-stu-id="621c6-141">For more information, see [Import users in bulk](tasks/import-bulk-users.md) or [Configure the Workflow message processing batch job as critical](../../fin-ops/organization-administration/workflow-batch-job-critical.md).</span></span>
8. <span data-ttu-id="621c6-142">**バッチ グループ** フィールドで、ジョブのバッチ グループを選択します。</span><span class="sxs-lookup"><span data-stu-id="621c6-142">In the **Batch group** field, select the batch group for the job.</span></span>
9. <span data-ttu-id="621c6-143">オプション: **スケジューリング優性順位が上書きされました** オプションを **はい** に設定し、**ジョブのスケジューリング優先順位** フィールドを使用可能にします。</span><span class="sxs-lookup"><span data-stu-id="621c6-143">Optional: Set the **Scheduling priority is overridden** option to **Yes**, to make the **Job scheduling priority** field available.</span></span>
10. <span data-ttu-id="621c6-144">オプション: **ジョブのスケジューリング優先順位** フィールドで、バッチ グループに対して定義されている既定の優先順位とは異なる既定の優先順位を選択します。</span><span class="sxs-lookup"><span data-stu-id="621c6-144">Optional: In the **Job scheduling priority** field, select a default priority that differs from the default priority that is defined for the batch group.</span></span>
11. <span data-ttu-id="621c6-145">オプション: **有効な期間** フィールドで、バッチ ジョブを実行できる時間の範囲を選択します。</span><span class="sxs-lookup"><span data-stu-id="621c6-145">Optional: In the **Active period** field, select the time range when the batch job can be run.</span></span> <span data-ttu-id="621c6-146">詳細については、[有効なバッチ期間](activeperiod.md) を参照してください。</span><span class="sxs-lookup"><span data-stu-id="621c6-146">For more information, see [Active batch periods](activeperiod.md).</span></span>
12. <span data-ttu-id="621c6-147">**保存** を選択します。</span><span class="sxs-lookup"><span data-stu-id="621c6-147">Select **Save**.</span></span>

### <a name="add-a-task-to-a-batch-job"></a><span data-ttu-id="621c6-148">バッチ ジョブへのタスクの追加</span><span class="sxs-lookup"><span data-stu-id="621c6-148">Add a task to a batch job</span></span>

1. <span data-ttu-id="621c6-149">**バッチ ジョブ** ページの **バッチ タスク** セクションで、**新規** を選択します。</span><span class="sxs-lookup"><span data-stu-id="621c6-149">On the **Batch job** page, in the **Batch tasks** section, select **New**.</span></span>
2. <span data-ttu-id="621c6-150">**タスク明細書**フィールドに値を入力します。</span><span class="sxs-lookup"><span data-stu-id="621c6-150">In the **Task description** field, enter a value.</span></span>
3. <span data-ttu-id="621c6-151">**会社アカウント** フィールドで、タスクが実行される会社を選択します。</span><span class="sxs-lookup"><span data-stu-id="621c6-151">In the **Company accounts** field, select the company that the task will be run in.</span></span>
4. <span data-ttu-id="621c6-152">**クラス名** フィールドで、実行するプロセスを選択します。</span><span class="sxs-lookup"><span data-stu-id="621c6-152">In the **Class name** field, select the process to run.</span></span>
5. <span data-ttu-id="621c6-153">**保存** を選択します。</span><span class="sxs-lookup"><span data-stu-id="621c6-153">Select **Save**.</span></span>
6. <span data-ttu-id="621c6-154">**バッチ タスクの詳細** クイックタブを展開して、バッチ タスクの設定をさらに追加するか、制約を追加します。</span><span class="sxs-lookup"><span data-stu-id="621c6-154">Expand the **Batch task detail** FastTab to add more settings for the batch task, or to add constraints.</span></span>
7. <span data-ttu-id="621c6-155">**全般** タブで、**タスクの失敗を無視する** オプションを **はい** に設定して、タスクの失敗によってジョブが失敗しないように指定します。</span><span class="sxs-lookup"><span data-stu-id="621c6-155">On the **General** tab, set the **Ignore task failure** option to **Yes** to specify that failure of the task should not cause the job to fail.</span></span>
8. <span data-ttu-id="621c6-156">**最大再試行回数** フィールドで、試行が何回失敗した場合にタスクが失敗したと見なされるかを指定します。</span><span class="sxs-lookup"><span data-stu-id="621c6-156">In the **Maximum retries** field, specify the number of times that a task should be retried before it's considered to have failed.</span></span>
9. <span data-ttu-id="621c6-157">そのジョブを作成したユーザーのみがタスクを実行する場合は、**プライベート** オプションを **はい** に設定します。</span><span class="sxs-lookup"><span data-stu-id="621c6-157">Set the **Private** option to **Yes** if the task should be run only by the user who created the job.</span></span> <span data-ttu-id="621c6-158">このオプションは、クライアントタスクにのみ適用されます。</span><span class="sxs-lookup"><span data-stu-id="621c6-158">This option is applicable only to client tasks.</span></span>
10. <span data-ttu-id="621c6-159">選択したタスクの実行がそのジョブの先行タスクのステータスに依存すべき場合は、**制約** タブで、**新規** を選択します。</span><span class="sxs-lookup"><span data-stu-id="621c6-159">On the **Constraints** tab, select **New** if the execution of the selected task should be dependent on the status of a preceding task for the job.</span></span>
11. <span data-ttu-id="621c6-160">**タスク ID** フィールドで、先行タスクを選択します。</span><span class="sxs-lookup"><span data-stu-id="621c6-160">In the **Task ID** field, select the preceding task.</span></span>
12. <span data-ttu-id="621c6-161">**予定されたステータス** フィールドで、現在のタスクを実行する前に先行タスクが到達する必要があるステータスを選択します。</span><span class="sxs-lookup"><span data-stu-id="621c6-161">In the **Expected status** field, select the status that the preceding task must reach before the current task can run.</span></span>
13. <span data-ttu-id="621c6-162">**保存** を選択します。</span><span class="sxs-lookup"><span data-stu-id="621c6-162">Select **Save**.</span></span>

> [!NOTE]
> <span data-ttu-id="621c6-163">複数の条件 / 制約を入力した場合、依存タスクが実行できる前にすべての条件が満たされている必要がある場合は、条件タイプとして **すべて** を選択します。</span><span class="sxs-lookup"><span data-stu-id="621c6-163">If you enter more than one condition/constraint, and if all conditions must be met before the dependent task can run, select **All** as the condition type.</span></span> <span data-ttu-id="621c6-164">いずれかの条件が満たされた後で依存タスクを実行できる場合は、条件タイプとして **任意** を選択します。</span><span class="sxs-lookup"><span data-stu-id="621c6-164">If the dependent task can run after any of the conditions has been met, select **Any** as the condition type.</span></span>
