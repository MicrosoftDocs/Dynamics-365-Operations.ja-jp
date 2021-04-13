---
title: 優先順位に基づくバッチスケジューリング
description: このトピックでは、優先順位に基づくバッチスケジューリングの機能について説明します。
author: peakerbl
ms.date: 12/05/2019
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: IT Pro
ms.reviewer: kfend
ms.custom: 62333
ms.assetid: ''
ms.search.region: Global
ms.author: peakerbl
ms.search.validFrom: 2019-10-29
ms.dyn365.ops.version: Platform Update31
ms.openlocfilehash: bf1a5532e46daec97280b8f4bef8d4b4076b6ef3
ms.sourcegitcommit: 074b6e212d19dd5d84881d1cdd096611a18c207f
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 03/31/2021
ms.locfileid: "5745939"
---
# <a name="priority-based-batch-scheduling"></a><span data-ttu-id="72237-103">優先順位に基づくバッチスケジューリング</span><span class="sxs-lookup"><span data-stu-id="72237-103">Priority-based batch scheduling</span></span> 

[!include [banner](../includes/banner.md)]

<span data-ttu-id="72237-104">プラットフォーム アップデート 31 では、[機能管理](../../fin-ops/get-started/feature-management/feature-management-overview.md) の **バッチ優先順位に基づくスケジューリング** 機能を有効にすることができます。</span><span class="sxs-lookup"><span data-stu-id="72237-104">In Platform update 31, you can turn on the **Batch priority-based scheduling** feature in [Feature management](../../fin-ops/get-started/feature-management/feature-management-overview.md).</span></span> <span data-ttu-id="72237-105">優先順位に基づくスケジューリングでは、バッチグループをバッチサーバーから切り離します。</span><span class="sxs-lookup"><span data-stu-id="72237-105">Priority-based scheduling decouples batch groups from the batch server.</span></span> <span data-ttu-id="72237-106">代わりに、使用可能なバッチサーバー間でタスクが実行される順序を決定するために、相対的なスケジューリング優先順位が使用されます。</span><span class="sxs-lookup"><span data-stu-id="72237-106">Instead, relative scheduling priorities are used to determine the order that tasks are run in across available batch servers.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="72237-107">この機能は、プラットフォーム アップデート 31 の一部として、制限されたプレビューでのみ使用できます。</span><span class="sxs-lookup"><span data-stu-id="72237-107">This feature is available only in a restricted preview as part of Platform update 31.</span></span>

<span data-ttu-id="72237-108">スケジューリング優先順位はバッチ グループに対して定義されますが、特定のバッチ ジョブに対して上書きすることができます。</span><span class="sxs-lookup"><span data-stu-id="72237-108">A scheduling priority is defined for batch groups, but it can be overridden for specific batch jobs.</span></span> <span data-ttu-id="72237-109">スケジュール設定の優先順位の分類は、相対的な優先順位を宣言し、ジョブとビジネスプロセスの処理順序の決定に使用されます。</span><span class="sxs-lookup"><span data-stu-id="72237-109">The scheduling priority classifications are used to declare relative priorities, and to determine the processing order of jobs and business processes.</span></span> <span data-ttu-id="72237-110">スケジューリング優先順位に使用できる値は、**低**、**通常**、**高**、**重大**、**予約済みキャパシティ** です。</span><span class="sxs-lookup"><span data-stu-id="72237-110">The available values for the scheduling priority are **Low**, **Normal**, **High**, **Critical**, and **Reserved capacity**.</span></span> <span data-ttu-id="72237-111">**標準** は規定の値です。これが有効化されると、すべての既存のバッチグループに適用されます。</span><span class="sxs-lookup"><span data-stu-id="72237-111">**Normal** is the default value and is also applied to all existing batch groups when the feature is turned on.</span></span> <span data-ttu-id="72237-112">**予約済キャパシティ** は、最も高い優先順位を表します。</span><span class="sxs-lookup"><span data-stu-id="72237-112">**Reserved capacity** represents the highest priority.</span></span> <span data-ttu-id="72237-113">プラットフォーム更新プログラム 32 または それ以降のバージョンでは、これをジョブ専用のキャパシティとして使用できます。</span><span class="sxs-lookup"><span data-stu-id="72237-113">In Platform update 32 and later versions, you can use it to dedicate reserved capacity for jobs.</span></span> <span data-ttu-id="72237-114">詳細については、 このトピック後半の <a name="reserved">バッチ専用のキャパシティを設定する</a> セクションを参照してください。</span><span class="sxs-lookup"><span data-stu-id="72237-114">For more information, see the <a name="reserved">Set the batch reserved capacity</a> section later in this topic.</span></span>

> [!NOTE]
> <span data-ttu-id="72237-115">この機能を有効にすると、すべての既存のバッチグループに対するスケジュールの優先度が **標準** に設定されています。それぞれのバッチグループに対してスケジュールの優先度を設定することは、業務要件に応じたバッチジョブと業務プロセスの優先度を表すことにもなります。</span><span class="sxs-lookup"><span data-stu-id="72237-115">Because the schedule priority is set to **Normal** for all existing batch groups when the feature is turned on, it's important that you plan and update the scheduling priority for each batch group so that it represents the relative priorities according to business requirements for the related batch jobs and their related business processes.</span></span>

<span data-ttu-id="72237-116">プラットフォーム更新プログラム 32 には、既存のバッチジョブに対する更新サポートが含まれています。</span><span class="sxs-lookup"><span data-stu-id="72237-116">Platform update 32 includes upgrade support for existing batch jobs.</span></span> <span data-ttu-id="72237-117">詳細については、 このトピック後半の <a name="#automatic">バッチジョブ を バッチグループ へと自動移行する</a> セクションを参照してください。</span><span class="sxs-lookup"><span data-stu-id="72237-117">For more information, see the <a name="#automatic">Automatic batch group migration for batch jobs</a> section later in this topic.</span></span>

<span data-ttu-id="72237-118">優先順位に基づくバッチ スケジューリングでは、機能管理での **バッチ フレームワークの競合軽減** 機能を有効にする必要があります。</span><span class="sxs-lookup"><span data-stu-id="72237-118">Priority-based batch scheduling requires that you turn on the **Batch framework contention reduction** feature in Feature management.</span></span>

<span data-ttu-id="72237-119">次の手順では、**優先順位に基づくバッチ スケジューリング** 機能が有効になっている場合に、バッチ グループ、ジョブ、およびタスクと作業する方法について説明します。</span><span class="sxs-lookup"><span data-stu-id="72237-119">The following procedures explain how to work with batch groups, jobs, and tasks, when the **Priority based batch scheduling** feature is turned on.</span></span>

## <a name="batch-groups"></a><span data-ttu-id="72237-120">バッチ グループ</span><span class="sxs-lookup"><span data-stu-id="72237-120">Batch groups</span></span>

<span data-ttu-id="72237-121">バッチ グループは、ジョブを論理的にグループ化し、既定のスケジューリング優先順位を設定するためにのみ使用されるようになりました。</span><span class="sxs-lookup"><span data-stu-id="72237-121">Batch groups are now used only to logically group jobs and to set the default scheduling priority.</span></span> <span data-ttu-id="72237-122">バッチ グループの例を次に示します:</span><span class="sxs-lookup"><span data-stu-id="72237-122">Here are some examples of batch groups:</span></span>

- <span data-ttu-id="72237-123">特定の業務プロセスに属するジョブ</span><span class="sxs-lookup"><span data-stu-id="72237-123">Jobs that belong to a specific business process</span></span>
- <span data-ttu-id="72237-124">同じ実行の繰り返しが設定されているジョブ (たとえば、毎晩、毎週、毎月など)</span><span class="sxs-lookup"><span data-stu-id="72237-124">Jobs that have the same execution recurrence (for example every night, every week, or every month)</span></span>
- <span data-ttu-id="72237-125">優先順位が同じジョブ</span><span class="sxs-lookup"><span data-stu-id="72237-125">Jobs that have the same priority</span></span>

### <a name="create-a-batch-group"></a><span data-ttu-id="72237-126">バッチ グループの作成</span><span class="sxs-lookup"><span data-stu-id="72237-126">Create a batch group</span></span>

1. <span data-ttu-id="72237-127">**システム管理** \> **設定** \> **バッチ グループ** の順に移動します。</span><span class="sxs-lookup"><span data-stu-id="72237-127">Go to **System administration** \> **Setup** \> **Batch group**.</span></span>
2. <span data-ttu-id="72237-128">**新規** を選択して、新しいバッチ グループを作成します。</span><span class="sxs-lookup"><span data-stu-id="72237-128">Select **New** to create a batch group.</span></span>
3. <span data-ttu-id="72237-129">**グループ** フィールドで、そのバッチ グループに対して固有の名前を入力します。</span><span class="sxs-lookup"><span data-stu-id="72237-129">In the **Group** field, enter a unique name for the batch group.</span></span>
4. <span data-ttu-id="72237-130">**説明** フィールドで値を入力します。</span><span class="sxs-lookup"><span data-stu-id="72237-130">In the **Description** field, enter a value.</span></span>
5. <span data-ttu-id="72237-131"> **スケジューリング優先順位** フィールドで、バッチ グループ内のバッチ ジョブの既定のスケジューリング優先順位を選択します。</span><span class="sxs-lookup"><span data-stu-id="72237-131">In the **Scheduling priority** field, select the default scheduling priority for the batch jobs in the batch group.</span></span>
6. <span data-ttu-id="72237-132">**保存** を選択します。</span><span class="sxs-lookup"><span data-stu-id="72237-132">Select **Save**.</span></span>

## <a name="batch-jobs"></a><span data-ttu-id="72237-133">バッチ ジョブ</span><span class="sxs-lookup"><span data-stu-id="72237-133">Batch jobs</span></span>

<span data-ttu-id="72237-134">バッチ ジョブは、自動処理のために送信されるタスクのグループです。</span><span class="sxs-lookup"><span data-stu-id="72237-134">A batch job is a group of tasks that are submitted for automatic processing.</span></span> <span data-ttu-id="72237-135">バッチ ジョブは、**実行者** フィールドで選択されたユーザーのセキュリティ資格情報を使用して実行されます。</span><span class="sxs-lookup"><span data-stu-id="72237-135">Batch jobs are run by using the security credentials of the user who is selected in **Run by** field.</span></span> <span data-ttu-id="72237-136">バッチ ジョブを作成するには、次の手順に従います。</span><span class="sxs-lookup"><span data-stu-id="72237-136">Use the following procedure to create a batch job.</span></span>

### <a name="create-a-batch-job"></a><span data-ttu-id="72237-137">バッチ ジョブの作成</span><span class="sxs-lookup"><span data-stu-id="72237-137">Create a batch job</span></span>

1. <span data-ttu-id="72237-138">**システム管理** \> **照会** \> **バッチ ジョブ** の順に移動します。</span><span class="sxs-lookup"><span data-stu-id="72237-138">Go to **System administration** \> **Inquiries** \> **Batch jobs**.</span></span>
2. <span data-ttu-id="72237-139">**新規** を選択して、新しいバッチ ジョブを作成します。</span><span class="sxs-lookup"><span data-stu-id="72237-139">Select **New** to create a batch job.</span></span>
3. <span data-ttu-id="72237-140">**職務明細書** フィールドに値を入力します。</span><span class="sxs-lookup"><span data-stu-id="72237-140">In the **Job description** field, enter a value.</span></span>
4. <span data-ttu-id="72237-141">**開始予定日時** フィールドに、日時を入力します。</span><span class="sxs-lookup"><span data-stu-id="72237-141">In the **Scheduled start date/time** field, enter a date and time.</span></span>
5. <span data-ttu-id="72237-142">**実行者** フィールドで、バッチジョブの実行時に使用するセキュリティ資格情報を持つユーザーを選択します。</span><span class="sxs-lookup"><span data-stu-id="72237-142">In the **Run by** field, select the users whose security credentials will be used when the batch job is run.</span></span> <span data-ttu-id="72237-143">詳細については、[バッチ管理者のセキュリティ ロール](runby.md) を参照してください。</span><span class="sxs-lookup"><span data-stu-id="72237-143">For more information, see [Batch manager security role](runby.md).</span></span>
6. <span data-ttu-id="72237-144">オプション: **監視カテゴリ** フィールドで、監視中にジョブのタイプを容易に識別できるように値を選択します。</span><span class="sxs-lookup"><span data-stu-id="72237-144">Optional: In the **Monitoring category** field, select a value to make it easier to identify the types of jobs during monitoring.</span></span>
7. <span data-ttu-id="72237-145">オプション: **重要なジョブ**　オプションを **はい** に設定します。</span><span class="sxs-lookup"><span data-stu-id="72237-145">Optional: Set the **Critical job** option to **Yes**.</span></span> <span data-ttu-id="72237-146">詳細については、[ユーザーを一括でインポートする](tasks/import-bulk-users.md) または [重大としてバッチ ジョブを処理するときのワークフロー メッセージを構成する](../../fin-ops/organization-administration/workflow-batch-job-critical.md) を参照してください。</span><span class="sxs-lookup"><span data-stu-id="72237-146">For more information, see [Import users in bulk](tasks/import-bulk-users.md) or [Configure the Workflow message processing batch job as critical](../../fin-ops/organization-administration/workflow-batch-job-critical.md).</span></span>
8. <span data-ttu-id="72237-147">**バッチ グループ** フィールドで、ジョブのバッチ グループを選択します。</span><span class="sxs-lookup"><span data-stu-id="72237-147">In the **Batch group** field, select the batch group for the job.</span></span>
9. <span data-ttu-id="72237-148">オプション: **スケジューリング優性順位が上書きされました** オプションを **はい** に設定し、**ジョブのスケジューリング優先順位** フィールドを使用可能にします。</span><span class="sxs-lookup"><span data-stu-id="72237-148">Optional: Set the **Scheduling priority is overridden** option to **Yes**, to make the **Job scheduling priority** field available.</span></span>
10. <span data-ttu-id="72237-149">オプション: **ジョブのスケジューリング優先順位** フィールドで、バッチ グループに対して定義されている既定の優先順位とは異なる既定の優先順位を選択します。</span><span class="sxs-lookup"><span data-stu-id="72237-149">Optional: In the **Job scheduling priority** field, select a default priority that differs from the default priority that is defined for the batch group.</span></span>
11. <span data-ttu-id="72237-150">オプション: **有効な期間** フィールドで、バッチ ジョブを実行できる時間の範囲を選択します。</span><span class="sxs-lookup"><span data-stu-id="72237-150">Optional: In the **Active period** field, select the time range when the batch job can be run.</span></span> <span data-ttu-id="72237-151">詳細については、[有効なバッチ期間](activeperiod.md) を参照してください。</span><span class="sxs-lookup"><span data-stu-id="72237-151">For more information, see [Active batch periods](activeperiod.md).</span></span>
12. <span data-ttu-id="72237-152">**保存** を選択します。</span><span class="sxs-lookup"><span data-stu-id="72237-152">Select **Save**.</span></span>

### <a name="add-a-task-to-a-batch-job"></a><span data-ttu-id="72237-153">バッチ ジョブへのタスクの追加</span><span class="sxs-lookup"><span data-stu-id="72237-153">Add a task to a batch job</span></span>

1. <span data-ttu-id="72237-154">**バッチ ジョブ** ページの **バッチ タスク** セクションで、**新規** を選択します。</span><span class="sxs-lookup"><span data-stu-id="72237-154">On the **Batch job** page, in the **Batch tasks** section, select **New**.</span></span>
2. <span data-ttu-id="72237-155">**タスク明細書** フィールドに値を入力します。</span><span class="sxs-lookup"><span data-stu-id="72237-155">In the **Task description** field, enter a value.</span></span>
3. <span data-ttu-id="72237-156">**会社アカウント** フィールドで、タスクが実行される会社を選択します。</span><span class="sxs-lookup"><span data-stu-id="72237-156">In the **Company accounts** field, select the company that the task will be run in.</span></span>
4. <span data-ttu-id="72237-157">**クラス名** フィールドで、実行するプロセスを選択します。</span><span class="sxs-lookup"><span data-stu-id="72237-157">In the **Class name** field, select the process to run.</span></span> <span data-ttu-id="72237-158">**CanGoBatchJournal** プロパティが有効化されていると、クラスがリスト表示されます。</span><span class="sxs-lookup"><span data-stu-id="72237-158">Classes appear in the list only if the **CanGoBatchJournal** property is turned on.</span></span>
5. <span data-ttu-id="72237-159">**保存** を選択します。</span><span class="sxs-lookup"><span data-stu-id="72237-159">Select **Save**.</span></span>
6. <span data-ttu-id="72237-160">**バッチ タスクの詳細** クイックタブを展開して、バッチ タスクの設定をさらに追加するか、制約を追加します。</span><span class="sxs-lookup"><span data-stu-id="72237-160">Expand the **Batch task detail** FastTab to add more settings for the batch task, or to add constraints.</span></span>
7. <span data-ttu-id="72237-161">**全般** タブで、**タスクの失敗を無視する** オプションを **はい** に設定して、タスクの失敗によってジョブが失敗しないように指定します。</span><span class="sxs-lookup"><span data-stu-id="72237-161">On the **General** tab, set the **Ignore task failure** option to **Yes** to specify that failure of the task should not cause the job to fail.</span></span>
8. <span data-ttu-id="72237-162">**最大再試行回数** フィールドで、試行が何回失敗した場合にタスクが失敗したと見なされるかを指定します。</span><span class="sxs-lookup"><span data-stu-id="72237-162">In the **Maximum retries** field, specify the number of times that a task should be retried before it's considered to have failed.</span></span>
9. <span data-ttu-id="72237-163">そのジョブを作成したユーザーのみがタスクを実行する場合は、**プライベート** オプションを **はい** に設定します。</span><span class="sxs-lookup"><span data-stu-id="72237-163">Set the **Private** option to **Yes** if the task should be run only by the user who created the job.</span></span> <span data-ttu-id="72237-164">このオプションは、クライアントタスクにのみ適用されます。</span><span class="sxs-lookup"><span data-stu-id="72237-164">This option is applicable only to client tasks.</span></span>
10. <span data-ttu-id="72237-165">選択したタスクの実行がそのジョブの先行タスクのステータスに依存すべき場合は、**制約** タブで、**新規** を選択します。</span><span class="sxs-lookup"><span data-stu-id="72237-165">On the **Constraints** tab, select **New** if the execution of the selected task should be dependent on the status of a preceding task for the job.</span></span>
11. <span data-ttu-id="72237-166">**タスク ID** フィールドで、先行タスクを選択します。</span><span class="sxs-lookup"><span data-stu-id="72237-166">In the **Task ID** field, select the preceding task.</span></span>
12. <span data-ttu-id="72237-167">**予定されたステータス** フィールドで、現在のタスクを実行する前に先行タスクが到達する必要があるステータスを選択します。</span><span class="sxs-lookup"><span data-stu-id="72237-167">In the **Expected status** field, select the status that the preceding task must reach before the current task can run.</span></span>
13. <span data-ttu-id="72237-168">**保存** を選択します。</span><span class="sxs-lookup"><span data-stu-id="72237-168">Select **Save**.</span></span>

    > [!NOTE]
    > <span data-ttu-id="72237-169">複数の条件 / 制約を入力した場合、依存タスクが実行できる前にすべての条件が満たされている必要がある場合は、条件タイプとして **すべて** を選択します。</span><span class="sxs-lookup"><span data-stu-id="72237-169">If you enter more than one condition/constraint, and if all conditions must be met before the dependent task can run, select **All** as the condition type.</span></span> <span data-ttu-id="72237-170">いずれかの条件が満たされた後で依存タスクを実行できる場合は、条件タイプとして **任意** を選択します。</span><span class="sxs-lookup"><span data-stu-id="72237-170">If the dependent task can run after any of the conditions has been met, select **Any** as the condition type.</span></span>

14. <span data-ttu-id="72237-171">バッチ タスクが入力パラメーターに対応している場合は、 **パラメーター** を選択し、続いてタスク固有のパラメーターを設定します。</span><span class="sxs-lookup"><span data-stu-id="72237-171">If the batch task supports input parameters, select **Parameters**, and then set task-specific parameters.</span></span>
15. <span data-ttu-id="72237-172">**OK** を選択してから、**保存** を選択します。</span><span class="sxs-lookup"><span data-stu-id="72237-172">Select **OK**, and then select **Save**.</span></span>

## <a name=""></a><span data-ttu-id="72237-173"><a name="reserved">バッチに特化したキャパシティ レベルの設定</a></span><span class="sxs-lookup"><span data-stu-id="72237-173"><a name="reserved">Set the batch reserved capacity level</a></span></span>

1. <span data-ttu-id="72237-174">**システム管理** \> **設定** \> **システム パラメーター** に移動します。</span><span class="sxs-lookup"><span data-stu-id="72237-174">Go to **System administration** \> **Setup** \> **System parameters**.</span></span>
2. <span data-ttu-id="72237-175">**バッチ グローバル 設定** タブの **バッチ専用のキャパシティ レベル** フィールドで、 **専用キャパシティ** の優先度を持つバッチジョブ 専用のキャパシティ レベルを選択します。</span><span class="sxs-lookup"><span data-stu-id="72237-175">On the **Batch global settings** tab, in the **Batch reserved capacity level** field, select the reserved capacity level to use for batch jobs that have **Reserved capacity** priority:</span></span>

    - <span data-ttu-id="72237-176">**専用キャパシティなし** – この値が既定の値となります。</span><span class="sxs-lookup"><span data-stu-id="72237-176">**No reserved capacity** – This value is the default value.</span></span>
    - <span data-ttu-id="72237-177">**専用キャパシティ低** – 累積するバッチ スレッドの 10パーセントがバッチ処理に割り当てられます。</span><span class="sxs-lookup"><span data-stu-id="72237-177">**Low reserved capacity** – Ten percent of the cumulative batch threads are reserved.</span></span>
    - <span data-ttu-id="72237-178">**専用キャパシティ中** – 累積するバッチスレッドの 15パーセントがバッチ処理に割り当てられます。</span><span class="sxs-lookup"><span data-stu-id="72237-178">**Medium reserved capacity** – Fifteen percent of the cumulative batch threads are reserved.</span></span>
    - <span data-ttu-id="72237-179">**専用キャパシティ高** – 累積するバッチスレッドの 25パーセントがバッチ処理に割り当てられます。</span><span class="sxs-lookup"><span data-stu-id="72237-179">**High reserved capacity** – Twenty-five percent of the cumulative batch threads are reserved.</span></span>

    > [!NOTE]
    > <span data-ttu-id="72237-180">サンプルの値は、わかりやすい事例を示しています。</span><span class="sxs-lookup"><span data-stu-id="72237-180">Sample values are for the purpose of illustration only.</span></span> <span data-ttu-id="72237-181">実際に割り当てられるキャパシティは、バッチサーバの設定と、任意時点で使用可能となるバッチスレッドの数によって異なります。</span><span class="sxs-lookup"><span data-stu-id="72237-181">The actual reserved capacity depends on the configuration of the batch server and the number of available batch threads at any given point.</span></span>

3. <span data-ttu-id="72237-182">**保存** を選択します。</span><span class="sxs-lookup"><span data-stu-id="72237-182">Select **Save**.</span></span>

> [!NOTE]
> <span data-ttu-id="72237-183">専用キャパシティは、 **専用キャパシティ** 優先度を持つバッチジョブのみに特化しています。</span><span class="sxs-lookup"><span data-stu-id="72237-183">Any reserved capacity is exclusive to batch jobs that have **Reserved capacity** priority.</span></span> <span data-ttu-id="72237-184">専用キャパシティは、未使用の専用キャパシティがあった場合でも、その他の 優先度が割り当てられているバッチジョブには利用できません。</span><span class="sxs-lookup"><span data-stu-id="72237-184">The reserved capacity won't be made available for batch jobs that have other priorities, even if there is idle reserved capacity.</span></span>

<span data-ttu-id="72237-185">**期限切れのバッチレコードを削除するシステムジョブ** は、新規の内部システム向けのバッチジョブで、新たな BatchHeartbeatTable テーブルを削除します。</span><span class="sxs-lookup"><span data-stu-id="72237-185">A new internal system batch job, **System job to clean up expired batch heartbeat records**, cleans up the new BatchHeartbeatTable table.</span></span> <span data-ttu-id="72237-186">このバッチジョブのクラス名は、 **SysCleanupBatchHeartbeatTable** です。</span><span class="sxs-lookup"><span data-stu-id="72237-186">This batch job has the class name **SysCleanupBatchHeartbeatTable**.</span></span> <span data-ttu-id="72237-187">BatchHeartbeatTable は 内部を監視するテーブルで、使用中のノードのスレッドのキャパシティを決定、設定や分配します。</span><span class="sxs-lookup"><span data-stu-id="72237-187">BatchHeartbeatTable is an internal monitoring table that is used to determine, configure, and distribute reserved capacity threads among online nodes.</span></span>

## <a name=""></a><span data-ttu-id="72237-188"><a name="automatic">バッチジョブをバッチグループへ自動移行する</a></span><span class="sxs-lookup"><span data-stu-id="72237-188"><a name="automatic">Automatic batch group migration for batch jobs</a></span></span>

<span data-ttu-id="72237-189">この機能が有効化されると、タスクのバッチ グループ情報は、使用されるジョブへと複製されます。</span><span class="sxs-lookup"><span data-stu-id="72237-189">After the feature is turned on, batch group information on the task is duplicated on the job that will be used.</span></span> <span data-ttu-id="72237-190">ジョブのバッチグループへの割り当ては、ジョブのタスクで最も使用されるバッチグループを基準に決定されます。</span><span class="sxs-lookup"><span data-stu-id="72237-190">The batch group assignment on a job is based on the batch group that is most used for the tasks for the job.</span></span>

<span data-ttu-id="72237-191">新規のバッチジョブ、 **バッチ グループの関連付けをバッチ ジョブに設定するシステム ジョブ** が移行の管理をします。</span><span class="sxs-lookup"><span data-stu-id="72237-191">A new system batch job, **System job to seed batch group associations to batch jobs**, manages the migration.</span></span> <span data-ttu-id="72237-192">このバッチジョブのクラス名は、 **SysMigrateBatchGroupsForPriorityBasedScheduling** です。</span><span class="sxs-lookup"><span data-stu-id="72237-192">This batch job has the class name **SysMigrateBatchGroupsForPriorityBasedScheduling**.</span></span>

<span data-ttu-id="72237-193">このバッチジョブは毎日 1:00 AM に起動し、 **スケジュール設定に基づいたバッチ処理優先度** 機能が無効となっていても起動します。</span><span class="sxs-lookup"><span data-stu-id="72237-193">The batch job is run every day at 1:00 AM, even if the **Batch priority-based scheduling** feature is turned off.</span></span> <span data-ttu-id="72237-194">最終実行時以降の、適用可能となるバッチ ジョブの差分を移行します。</span><span class="sxs-lookup"><span data-stu-id="72237-194">It migrates the delta of applicable batch jobs since the last execution.</span></span>

<span data-ttu-id="72237-195">この機能を有効にすると、バッチジョブが実行され、最終実行時以降のバッチジョブが移行されます。</span><span class="sxs-lookup"><span data-stu-id="72237-195">The batch job is also run when the feature is turned on, to migrate any batch jobs since the last execution.</span></span> <span data-ttu-id="72237-196">この機能を有効にしたユーザーには、移行バッチ ジョブの ID への参照を含む通知が送信されます。</span><span class="sxs-lookup"><span data-stu-id="72237-196">The user who turned on the feature will receive a notification that includes a reference to the ID of the migration batch job.</span></span>

<span data-ttu-id="72237-197">この機能を有効化して移行が完了したら、自動バッチグループへの割り当てを確認することを推奨します。</span><span class="sxs-lookup"><span data-stu-id="72237-197">We recommend that you review the automatic batch group assignment after the feature is turned on and the migration is completed.</span></span> <span data-ttu-id="72237-198">この確認作業を容易にする目的で、タスクの **バッチグループ** フィールドは読み取り専用になっています。</span><span class="sxs-lookup"><span data-stu-id="72237-198">To facilitate this review, the **Batch group** field for tasks is read-only.</span></span> <span data-ttu-id="72237-199">下位互換性に対応するため、このフィールドの値は、新たなバッチタスクが追加された際にジョブから反映されます。</span><span class="sxs-lookup"><span data-stu-id="72237-199">To support backward compatibility, the value of this field will be propagated from the job when new batch tasks are added.</span></span>


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]