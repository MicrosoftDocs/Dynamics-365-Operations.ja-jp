---
title: ウェーブ中の作業作成のスケジュール
description: このトピックでは、作業作成のスケジュールのウェーブ処理メソッドを設定および使用する方法について説明します。
author: perlynne
manager: mirzaab
ms.date: 01/14/2021
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: WHSPostMethod, WHSWavePostMethodTaskConfig, WHSWaveTemplateTable, WHSParameters, WHSWaveTableListPage, WHSWorkTableListPage, WHSWorkTable, BatchJobEnhanced, WHSPlannedWorkOrder
audience: Application User
ms.reviewer: ''
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: kamaybac
ms.search.validFrom: 2021-01-14
ms.dyn365.ops.version: 10.0.17
ms.openlocfilehash: 36a450f78695f617056875f8d236fe46bc66aaaf
ms.sourcegitcommit: 2b4809e60974e72df9476ffd62706b1bfc8da4a7
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 03/04/2021
ms.locfileid: "5501225"
---
# <a name="schedule-work-creation-during-wave"></a><span data-ttu-id="cb509-103">ウェーブ中の作業作成のスケジュール</span><span class="sxs-lookup"><span data-stu-id="cb509-103">Schedule work creation during wave</span></span>

[!include [banner](../../includes/banner.md)]
[!include [preview banner](../includes/preview-banner.md)]

<span data-ttu-id="cb509-104">ウェーブ プロセスの一部として *作業作成のスケジュール* 機能を使用すると、並行処理を使用してシステムに作業を作成させることにより、ウェーブ処理のスループットを向上させることができます。</span><span class="sxs-lookup"><span data-stu-id="cb509-104">Use the *Schedule work creation* feature as part of your waving process to help increase wave processing throughput by having the system create work using parallel processing.</span></span>

<span data-ttu-id="cb509-105">この機能を有効にすると、計画作業が自動的に作成され、最終的にシステムが実際の作業の作成を処理します。</span><span class="sxs-lookup"><span data-stu-id="cb509-105">When the functionality is enabled, planned work will automatically get created, which the system will eventually process to create actual work.</span></span> <span data-ttu-id="cb509-106">ウェーブ積荷の数が所定のしきい値に達すると、システムは並列の非同期処理を適用することで、より迅速に実際の作業を作成します。</span><span class="sxs-lookup"><span data-stu-id="cb509-106">If the number of wave load lines reaches a predetermined threshold, the system will create actual work more quickly by applying parallel, asynchronous processing.</span></span>

## <a name="enable-the-schedule-work-creation-feature"></a><span data-ttu-id="cb509-107">作業作成のスケジュール機能を有効にする</span><span class="sxs-lookup"><span data-stu-id="cb509-107">Enable the Schedule work creation feature</span></span>

### <a name="enable-the-feature-in-feature-management"></a><span data-ttu-id="cb509-108">機能管理で機能を有効にする</span><span class="sxs-lookup"><span data-stu-id="cb509-108">Enable the feature in feature management</span></span>

<span data-ttu-id="cb509-109">*作業作成のスケジュール* 機能を使用するには、システム上で有効にする必要があります。</span><span class="sxs-lookup"><span data-stu-id="cb509-109">Before you can use the *Schedule work creation* feature, it must be turned on in your system.</span></span> <span data-ttu-id="cb509-110">管理者は、[機能の管理](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) ワークスペースを使用して、機能の状態を確認し、必要に応じて有効にすることができます。</span><span class="sxs-lookup"><span data-stu-id="cb509-110">Admins can use the [Feature management](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) workspace to check the status of the feature and turn it on if it's required.</span></span> <span data-ttu-id="cb509-111">この機能は、次のようにして表示されます。</span><span class="sxs-lookup"><span data-stu-id="cb509-111">There, the feature is listed in the following way:</span></span>

- <span data-ttu-id="cb509-112">**モジュール:** *倉庫管理*</span><span class="sxs-lookup"><span data-stu-id="cb509-112">**Module:** *Warehouse management*</span></span>
- <span data-ttu-id="cb509-113">**機能名:** *作業作成のスケジュール*</span><span class="sxs-lookup"><span data-stu-id="cb509-113">**Feature name:** *Schedule work creation*</span></span>

> [!NOTE]
> <span data-ttu-id="cb509-114">*組織全体の作業のブロック* 機能は、*作業作成のスケジュール* を有効にする前に、有効にする必要があります。</span><span class="sxs-lookup"><span data-stu-id="cb509-114">The *Organization-wide work blocking* feature must be enabled before you can enable *Schedule work creation*.</span></span>

### <a name="manually-enable-batch-processing-of-waves"></a><span data-ttu-id="cb509-115">ウェーブのバッチ処理を手動で有効にする</span><span class="sxs-lookup"><span data-stu-id="cb509-115">Manually enable batch processing of waves</span></span>

<span data-ttu-id="cb509-116">並列非同期メソッドを利用して倉庫作業を作成するには、ウェーブ プロセスをバッチで実行する必要があります。</span><span class="sxs-lookup"><span data-stu-id="cb509-116">To take advantage of a parallel asynchronous method to create warehouse work, your wave process must be running in batch.</span></span> <span data-ttu-id="cb509-117">これを設定するには:</span><span class="sxs-lookup"><span data-stu-id="cb509-117">To set this up:</span></span>

1. <span data-ttu-id="cb509-118"> *\*倉庫管理 \> 設定 \> 倉庫管理パラメーター** の順に移動します。</span><span class="sxs-lookup"><span data-stu-id="cb509-118">Go to **Warehouse management \> Setup \> Warehouse management parameters**.</span></span>

1. <span data-ttu-id="cb509-119">**全般** タブで **ウェーブのバッチ処理** を *はい* に設定します。</span><span class="sxs-lookup"><span data-stu-id="cb509-119">On the **General** tab, set **Process waves in batch** to *Yes*.</span></span> <span data-ttu-id="cb509-120">必要に応じて、専用の **ウェーブを処理するバッチ グループ** を選択して、バッチ キューの処理が他のプロセスと同時に実行されないようにすることもできます。</span><span class="sxs-lookup"><span data-stu-id="cb509-120">Optionally, you can also select a dedicated **Wave processing batch group** to prevent your batch queue processing from running at the same time as other processes.</span></span>

1. <span data-ttu-id="cb509-121">システムが複数のウェーブを同時に処理する場合に適用される、**ロック待機 (ミリ秒) 時間** を設定します。</span><span class="sxs-lookup"><span data-stu-id="cb509-121">Set the **Wait for lock (ms) time**, which applies when the system is processing several waves at the same time.</span></span> <span data-ttu-id="cb509-122">大規模なウェーブ プロセスの場合は、値を *60000* にすることをお勧めします。</span><span class="sxs-lookup"><span data-stu-id="cb509-122">For most larger waving processes, we recommend a value of *60000*.</span></span>

### <a name="manually-enable-the-new-wave-step-method-for-existing-wave-templates"></a><span data-ttu-id="cb509-123">既存のウェーブ テンプレートに対して新しいウェーブ ステップ メソッドを手動で有効にする</span><span class="sxs-lookup"><span data-stu-id="cb509-123">Manually enable the new wave step method for existing wave templates</span></span>

<span data-ttu-id="cb509-124">最初に、新しいウェーブ ステップ メソッドを作成し、並列非同期タスク処理を有効にします。</span><span class="sxs-lookup"><span data-stu-id="cb509-124">Start by creating the new wave step method and enabling it for parallel asynchronous task processing.</span></span>

1. <span data-ttu-id="cb509-125"> *\*倉庫管理 \> 設定 \> ウェーブ \> ウェーブのプロセス メソッド** に移動します。</span><span class="sxs-lookup"><span data-stu-id="cb509-125">Go to **Warehouse management \> Setup \> Waves \> Wave process methods**.</span></span>

1. <span data-ttu-id="cb509-126"> *\*メソッドの再生成** を選択して、\*WHSScheduleWorkCreationWaveStepMethod* が出荷ウェーブ テンプレートで使用できるウェーブ プロセス メソッドの一覧に追加されていることに注意してください。</span><span class="sxs-lookup"><span data-stu-id="cb509-126">Select  **Regenerate method** and note that *WHSScheduleWorkCreationWaveStepMethod* has been added to the list of wave process methods you can use in your shipping wave templates.</span></span>

1. <span data-ttu-id="cb509-127">**メソッド名** *WHSScheduleWorkCreationWaveStepMethod* を含むレコードを選択し、**タスク構成** を選択します。</span><span class="sxs-lookup"><span data-stu-id="cb509-127">Select the record with the **Method name** *WHSScheduleWorkCreationWaveStepMethod* and select **Task configuration**.</span></span>

1. <span data-ttu-id="cb509-128">グリッドに新しい行を追加するには、アクション ウィンドウで **新規** を選択して、次の設定を使用します:</span><span class="sxs-lookup"><span data-stu-id="cb509-128">To add a new row to the grid, select **New** on the Action Pane and use the following settings:</span></span>

    - <span data-ttu-id="cb509-129">**倉庫** - 作業作成処理をスケジュールするために使用する倉庫を選択します。</span><span class="sxs-lookup"><span data-stu-id="cb509-129">**Warehouse** - Select the warehouse you will use to schedule work creation processing.</span></span>

    - <span data-ttu-id="cb509-130">**バッチ タスクの最大数** - バッチ タスクの最大数を指定します。</span><span class="sxs-lookup"><span data-stu-id="cb509-130">**Maximum number of batch tasks** - Specify a maximum number of batch tasks.</span></span> <span data-ttu-id="cb509-131">ほとんどの場合、この値は 8-16 の範囲にする必要がありますが、シナリオに基づいて最適な設定を試することをお勧めします。</span><span class="sxs-lookup"><span data-stu-id="cb509-131">In most cases, this value should be in the range from 8-16, however we recommend that you experiment with the optimal setting based on your scenarios.</span></span>

    - <span data-ttu-id="cb509-132">**ウェーブを処理するバッチ グループ** - 専用のウェーブを処理するバッチ グループを選択して、バッチ キュー処理を最適化します。</span><span class="sxs-lookup"><span data-stu-id="cb509-132">**Wave processing batch group** - Select a dedicated wave processing batch group to optimize your batch queue processing.</span></span>

<span data-ttu-id="cb509-133">これで、既存のウェーブ テンプレートを更新 (または新しいテンプレートを作成) して、*作業作成のスケジュール* ウェーブ処理メソッドを使用する準備が整いました。</span><span class="sxs-lookup"><span data-stu-id="cb509-133">Now you are ready to update an existing wave template (or create a new one) to use the *Schedule work creation* wave processing method.</span></span>

1. <span data-ttu-id="cb509-134"> *\*倉庫管理 \> 設定 \> ウェーブ \> ウェーブ テンプレート** の順に移動します。</span><span class="sxs-lookup"><span data-stu-id="cb509-134">Go to **Warehouse management \> Setup \> Waves \> Wave templates**.</span></span>

1. <span data-ttu-id="cb509-135">アクション ペインで **編集** を選択します。</span><span class="sxs-lookup"><span data-stu-id="cb509-135">Select **Edit** on the Action Pane.</span></span>

1. <span data-ttu-id="cb509-136">リスト ペインで、更新するウェーブ テンプレートを選択します (デモ データを使用してテストを行っている場合は、*24 出荷の既定* を使用できます)。</span><span class="sxs-lookup"><span data-stu-id="cb509-136">In the list pane, select the wave template you would like to update (if you are testing using demo data, then you could use *24 Shipping default*).</span></span>

1. <span data-ttu-id="cb509-137">**メソッド** クイック タブを展開し、**残りのメソッド** グリッドで **名前** *作業作成のスケジュール* の行を選択します。</span><span class="sxs-lookup"><span data-stu-id="cb509-137">Expand the **Methods** FastTab and select the row with the **Name** *Schedule work creation* in the **Remaining methods** grid.</span></span>

1. <span data-ttu-id="cb509-138">**選択されたメソッド** 列を指す矢印を選択して、選択した行をその列に移動します。</span><span class="sxs-lookup"><span data-stu-id="cb509-138">Select the arrow pointing to the **Selected methods** column to move the selected row to that column.</span></span> <span data-ttu-id="cb509-139">(*WHSScheduleWorkCreationWaveStepMethod* または *createWork* を使用するメソッドは、一度に 1 つしか選択できないため、**メソッド名** *createWork* を持つ既存の行は、自動的に **残りのメソッド** グリッドに移動されます。)</span><span class="sxs-lookup"><span data-stu-id="cb509-139">(You can only have one selected method at a time that uses either *WHSScheduleWorkCreationWaveStepMethod* or *createWork*, so the existing row with **Method name** *createWork* is automatically moved to the **Remaining methods** grid.)</span></span>

## <a name="set-wave-task-processing-threshold-data"></a><span data-ttu-id="cb509-140">ウェーブ タスク処理のしきい値データの設定</span><span class="sxs-lookup"><span data-stu-id="cb509-140">Set wave task processing threshold data</span></span>

<span data-ttu-id="cb509-141">システムは、タスク ベースの処理を使用してウェーブ プロセスを初めて実行するときに、既定のウェーブ タスク処理のしきい値データを作成します。</span><span class="sxs-lookup"><span data-stu-id="cb509-141">The system will create default wave task processing threshold data the first time a wave process runs using any task-based processing.</span></span> <span data-ttu-id="cb509-142">データは、ウェーブ処理を非同期に実行し、タスク ベースにするタイミングを制御するために使用されます。これにより、ウェーブ処理を並行して処理し、作業を作成できます。</span><span class="sxs-lookup"><span data-stu-id="cb509-142">The data is used to control when wave processing will run asynchronously and be task-based, which enables it to process and create work in parallel.</span></span>

<span data-ttu-id="cb509-143">既定のデータでは、最初に、最小積荷明細行数 (MINIMUMWAVELOADLINES) に対してしきい値 15 が使用されます。</span><span class="sxs-lookup"><span data-stu-id="cb509-143">The default data will initially use a threshold value of 15 for the minimum number of load lines (MINIMUMWAVELOADLINES).</span></span> <span data-ttu-id="cb509-144">つまり、システムが、15 より多い積荷明細行を含むウェーブを処理すると、非同期タスク処理を使用します。</span><span class="sxs-lookup"><span data-stu-id="cb509-144">This means that when the system processes a wave with more than 15 loads lines, it will use asynchronous task processing.</span></span> <span data-ttu-id="cb509-145">このデータは、テスト環境の **WHSWaveTaskProcessingThresholdParameters** テーブルに手動で挿入または更新できますが、運用環境でこの設定を変更する必要がある場合は、Microsoft サポートに連絡して、更新を依頼する必要があります。</span><span class="sxs-lookup"><span data-stu-id="cb509-145">You can manually insert/update this data in the **WHSWaveTaskProcessingThresholdParameters** table in your test environments, but if you need to change this setting in a production environment, you must contact Microsoft Support to request the update.</span></span>

## <a name="work-with-the-feature"></a><span data-ttu-id="cb509-146">機能の使用</span><span class="sxs-lookup"><span data-stu-id="cb509-146">Work with the feature</span></span>

<span data-ttu-id="cb509-147">*作業作成のスケジュール* 機能を有効にすると、ウェーブ処理は計画作業を作成し、最終的には新しい作業作成プロセスで使用されます。</span><span class="sxs-lookup"><span data-stu-id="cb509-147">When the *Schedule work creation* functionality is enabled, wave processing will create planned work, which will eventually be used by the new work creation process.</span></span> <span data-ttu-id="cb509-148">作業の作成中は、*組織全体の作業のブロック* 機能を使用して作業がブロックされます。</span><span class="sxs-lookup"><span data-stu-id="cb509-148">During work creation, the work will be blocked using the *Organization-wide work blocking* feature.</span></span>

<span data-ttu-id="cb509-149">次のフローチャートは、ウェーブ処理中に計画作業がどのように作成されるかを示しています。</span><span class="sxs-lookup"><span data-stu-id="cb509-149">The following flowchart shows how planned work is created during wave processing.</span></span>

![作業作成のスケジュール](media/schedule-work-creation-process.png)

### <a name="planned-work"></a><span data-ttu-id="cb509-151">計画作業</span><span class="sxs-lookup"><span data-stu-id="cb509-151">Planned work</span></span>

<span data-ttu-id="cb509-152">**計画作業の詳細** ページ (**倉庫管理 \> 作業 \> 計画作業の詳細**) には、ウェーブ処理中に最初に作成された計画作業に関する情報が表示されます。</span><span class="sxs-lookup"><span data-stu-id="cb509-152">The **Planned work details** page (**Warehouse management \> Work \> Planned work details**) shows information about the planned work, which is initially created during wave processing.</span></span> <span data-ttu-id="cb509-153">以下の **プロセス状態** 値を使用できます:</span><span class="sxs-lookup"><span data-stu-id="cb509-153">The following **Process status** values are available:</span></span>

- <span data-ttu-id="cb509-154">**キューに設定** - 計画作業は、作業の作成に使用されるまで待機しています。</span><span class="sxs-lookup"><span data-stu-id="cb509-154">**Queued** - The planned work is waiting to be used to create work.</span></span>
- <span data-ttu-id="cb509-155">**完了** - 計画作業が作業の作成に使用されました。</span><span class="sxs-lookup"><span data-stu-id="cb509-155">**Completed** - The planned work has been used to create work.</span></span>
- <span data-ttu-id="cb509-156">**失敗** – ウェーブ処理が失敗しました。</span><span class="sxs-lookup"><span data-stu-id="cb509-156">**Failed** – The wave processing has failed.</span></span> <span data-ttu-id="cb509-157">計画作業は、関連する実際の作業の有無にかかわらず、**失敗** した状態になることがあります。</span><span class="sxs-lookup"><span data-stu-id="cb509-157">Note that the planned work can be in a **Failed** state with or without related actual work.</span></span> <span data-ttu-id="cb509-158">実際の作業作成プロセスが失敗すると、実際の作業は *キャンセル済* 状態のままになります。</span><span class="sxs-lookup"><span data-stu-id="cb509-158">When the actual work creation process fails, the actual work remains in status *Cancelled*.</span></span>

### <a name="batch-job-for-the-work-creation-process"></a><span data-ttu-id="cb509-159">作業作成プロセスのバッチ ジョブ</span><span class="sxs-lookup"><span data-stu-id="cb509-159">Batch job for the work creation process</span></span>

<span data-ttu-id="cb509-160">ウェーブを処理するバッチ ジョブを表示するには、**すべてのウェーブ** ページのアクション ペインで **バッチ ジョブ** を選択 します。</span><span class="sxs-lookup"><span data-stu-id="cb509-160">To view the batch jobs for processing waves, select **Batch jobs** on the Action Pane on the **All waves** page.</span></span>

<span data-ttu-id="cb509-161">ここから、各バッチ ジョブ ID のすべてのバッチ タスクの詳細を表示できます。</span><span class="sxs-lookup"><span data-stu-id="cb509-161">From here, you can view all the batch task details for each of the batch job IDs.</span></span>


[!INCLUDE[footer-include](../../includes/footer-banner.md)]