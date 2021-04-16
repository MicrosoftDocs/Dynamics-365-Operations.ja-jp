---
title: ウェーブ中の作業作成のスケジュール
description: このトピックでは、作業作成のスケジュールのウェーブ処理メソッドを設定および使用する方法について説明します。
author: perlynne
ms.date: 01/14/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: WHSPostMethod, WHSWavePostMethodTaskConfig, WHSWaveTemplateTable, WHSParameters, WHSWaveTableListPage, WHSWorkTableListPage, WHSWorkTable, BatchJobEnhanced, WHSPlannedWorkOrder
audience: Application User
ms.reviewer: ''
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: kamaybac
ms.search.validFrom: 2021-01-14
ms.dyn365.ops.version: 10.0.17
ms.openlocfilehash: e4258c03b12a80a5bd81328ae7418835d68f82e7
ms.sourcegitcommit: 0e8db169c3f90bd750826af76709ef5d621fd377
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/01/2021
ms.locfileid: "5835705"
---
# <a name="schedule-work-creation-during-wave"></a><span data-ttu-id="eab73-103">ウェーブ中の作業作成のスケジュール</span><span class="sxs-lookup"><span data-stu-id="eab73-103">Schedule work creation during wave</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="eab73-104">ウェーブ プロセスの一部として *作業作成のスケジュール* 機能を使用すると、並行処理を使用してシステムに作業を作成させることにより、ウェーブ処理のスループットを向上させることができます。</span><span class="sxs-lookup"><span data-stu-id="eab73-104">Use the *Schedule work creation* feature as part of your waving process to help increase wave processing throughput by having the system create work using parallel processing.</span></span>

<span data-ttu-id="eab73-105">この機能を有効にすると、計画作業が自動的に作成され、最終的にシステムが実際の作業の作成を処理します。</span><span class="sxs-lookup"><span data-stu-id="eab73-105">When the functionality is enabled, planned work will automatically get created, which the system will eventually process to create actual work.</span></span> <span data-ttu-id="eab73-106">ウェーブ積荷の数が所定のしきい値に達すると、システムは並列の非同期処理を適用することで、より迅速に実際の作業を作成します。</span><span class="sxs-lookup"><span data-stu-id="eab73-106">If the number of wave load lines reaches a predetermined threshold, the system will create actual work more quickly by applying parallel, asynchronous processing.</span></span>

## <a name="turn-on-the-scheduled-work-creation-features-in-feature-management"></a><span data-ttu-id="eab73-107">機能管理でスケジュールされた作業作成機能を有効にする</span><span class="sxs-lookup"><span data-stu-id="eab73-107">Turn on the scheduled work creation features in feature management</span></span>

<span data-ttu-id="eab73-108">このトピックで説明する機能を使用するには、システムでこれら機能を有効にする必要があります。</span><span class="sxs-lookup"><span data-stu-id="eab73-108">To use the features described in this topic, they must be turned on for your system.</span></span> <span data-ttu-id="eab73-109">[機能の管理](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md)ワークスペースを使用して、次の機能を次に示す順番で有効にします :</span><span class="sxs-lookup"><span data-stu-id="eab73-109">Use [Feature management](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) workspace to turn on the following features in the following order:</span></span>

1. <span data-ttu-id="eab73-110">**組織全体の作業のブロック** - スケジュールされた作業作成の手動/自動の両方の構成に必要です。</span><span class="sxs-lookup"><span data-stu-id="eab73-110">**Organization-wide work blocking** - Required for both manual and automatic configuration of scheduled work creation.</span></span>
1. <span data-ttu-id="eab73-111">**作業作成のスケジュール** - スケジュールされた作業作成の手動/自動の両方の構成に必要です。</span><span class="sxs-lookup"><span data-stu-id="eab73-111">**Schedule work creation** - Required for both manual and automatic configuration of scheduled work creation.</span></span>
1. <span data-ttu-id="eab73-112">**組織全体の 「作業作成のスケジュール」 ウェーブメソッド** - スケジュールされた作業作成の自動設定に必要です。</span><span class="sxs-lookup"><span data-stu-id="eab73-112">**Organization-wide "Schedule work creation" wave method** - Required for automatic configuration of scheduled work creation.</span></span> <span data-ttu-id="eab73-113">手動での構成のみを使用する場合は、この機能は不要です。</span><span class="sxs-lookup"><span data-stu-id="eab73-113">You don't need this feature if you will only use manual configuration.</span></span>

<a name="Auto-enable-schedule-work-creation"></a>

## <a name="automatically-configure-scheduled-work-creation"></a><span data-ttu-id="eab73-114">スケジュールされた作業の作成を自動的に設定する</span><span class="sxs-lookup"><span data-stu-id="eab73-114">Automatically configure scheduled work creation</span></span>

<span data-ttu-id="eab73-115">*組織全体の 「作業作成のスケジュール」 ウェーブメソッド* 機能を有効にすると、ご利用のシステムでは自動的に次のようになります :</span><span class="sxs-lookup"><span data-stu-id="eab73-115">If you enable the *Organization-wide "Schedule work creation" wave method* feature, the following automatically occurs on your system:</span></span>

- <span data-ttu-id="eab73-116">ウェーブ メソッド(`WHSScheduleWorkCreationWaveStepMethod`) *作業作成のスケジュール* は、すべての法人に並行して実行されるように追加・設定されています。</span><span class="sxs-lookup"><span data-stu-id="eab73-116">The *Schedule work creation* wave method (`WHSScheduleWorkCreationWaveStepMethod`) is added and configured to run in parallel across all legal entities.</span></span>
- <span data-ttu-id="eab73-117">**ウェーブ テンプレートのタイプ** を *出荷* に設定し、**テンプレートの状態** を *有効* に設定したすべての法人のウェーブ テンプレートでは、*作業の作成* というメソッドが *作業作成のスケジュール* メソッドに変更されます。</span><span class="sxs-lookup"><span data-stu-id="eab73-117">Wave templates from all legal entities that have **Wave template type** set to *Shipping* and **Template status** set to *Valid* will have the *Create work* method replaced by the *Schedule work creation* method.</span></span> <span data-ttu-id="eab73-118">ただし、*作業の作成* メソッドが反復可能であると認められている法人のウェーブ テンプレートは修正されません。</span><span class="sxs-lookup"><span data-stu-id="eab73-118">However, wave templates from legal entities where the *Create work* method is allowed to be repeatable will not be modified.</span></span>
- <span data-ttu-id="eab73-119">*作業作成のスケジュール* メソッドのタスク構成は、**倉庫管理プロセスの使用** を有効にしているすべての法人のすべての倉庫に対して作成されます。</span><span class="sxs-lookup"><span data-stu-id="eab73-119">Task configurations for the *Schedule work creation* method will be created for all warehouses from all legal entities that have **Use warehouse management processes** enabled.</span></span> <span data-ttu-id="eab73-120">これにより、*作業作成のスケジュール* メソッドが既定で並列して実行されます。</span><span class="sxs-lookup"><span data-stu-id="eab73-120">This means that the *Schedule work creation* method will now run in parallel by default.</span></span> <span data-ttu-id="eab73-121">**倉庫管理プロセスを使用** を *いいえ* から *はい* に変更した既存の倉庫でも、この方法が既定で並行して実行されます。</span><span class="sxs-lookup"><span data-stu-id="eab73-121">Existing warehouses for which you change **Use warehouse management processes** from *No* to *Yes* will also run this method in parallel by default.</span></span>
- <span data-ttu-id="eab73-122">すべての法人はウェーブを一括して処理し、**ロックの待機 (ms)** は、これまで *0* ms に設定されていたものが、既定の *60,000* ms に設定されます。</span><span class="sxs-lookup"><span data-stu-id="eab73-122">All legal entities will process waves in batches and **Wait for lock (ms)** will be set to a default value of *60,000* ms if it was previously set to *0* ms.</span></span>
- <span data-ttu-id="eab73-123">新たに作成したすべてのウェーブ テンプレートには、*作業の作成* メソッドではなく  *作業作成のスケジュール* というウェーブ メソッドが採用されます。</span><span class="sxs-lookup"><span data-stu-id="eab73-123">All the new wave templates that you create will have the *Schedule work creation* wave method instead of the *Create Work* method.</span></span>

<span data-ttu-id="eab73-124">また、ウェーブを一括して処理するように設定されているすべての法人、および *作業作成のスケジュール* メソッドを並行して使用するように設定されているすべての倉庫については、既存のタスクおよびウェーブ処理の設定が維持されます。</span><span class="sxs-lookup"><span data-stu-id="eab73-124">The existing task and wave processing configurations will also be kept for all legal entities that are already configured to process waves in batches, and for all warehouses that are already configured to use the *Schedule work creation* method in parallel.</span></span>

<span data-ttu-id="eab73-125">必要に応じて、以下のように、*組織全体の 「作業作成のスケジュール」 ウェーブメソッド* 機能を有効にしたときに自動的に行われた設定の一部、またはすべてを手動で元に戻すことができます :</span><span class="sxs-lookup"><span data-stu-id="eab73-125">If necessary, you can manually revert any or all of the settings made automatically when you enabled the *Organization-wide Schedule work creation wave method* feature by doing the following:</span></span>

- <span data-ttu-id="eab73-126">ウェーブ テンプレートに対しては、**倉庫管理 \> 設定 \> ウェーブ \> ウェーブ テンプレート** にアクセスしてください。</span><span class="sxs-lookup"><span data-stu-id="eab73-126">For wave templates, go to **Warehouse management \> Setup \> Waves \> Wave templates**.</span></span> <span data-ttu-id="eab73-127">*作業作成のスケジュール* メソッドを *作業の作成* と置き換えます。</span><span class="sxs-lookup"><span data-stu-id="eab73-127">Replace *Schedule work creation* method with *Create work*.</span></span>
- <span data-ttu-id="eab73-128">倉庫のパラメーターに対しては、 **倉庫管理 \> 設定 \> 倉庫管理パラメーター** にアクセスしてください。</span><span class="sxs-lookup"><span data-stu-id="eab73-128">For warehouse parameters, go to **Warehouse management \> Setup \> Warehouse management parameters**.</span></span> <span data-ttu-id="eab73-129">**制御処理** タブで、**バッチの処理** と **ロックを待機 (ミリ秒)** の値 を適用します 。</span><span class="sxs-lookup"><span data-stu-id="eab73-129">On the **Wave processing** tab, apply your preferred values for **Process waves in batch** and **Wait for lock (ms)**.</span></span>
- <span data-ttu-id="eab73-130">ウェーブ メソッドに対すしては、**倉庫管理 \> 設定 \> ウェーブ \> ウェーブ プロセスのメソッド** にアクセスしてください。</span><span class="sxs-lookup"><span data-stu-id="eab73-130">For the wave methods, go to **Warehouse management \> Setup \> Waves \> Wave process methods**.</span></span> <span data-ttu-id="eab73-131">`WHSScheduleWorkCreationWaveStepMethod` を選択し、アクション ペインで、**タスクの構成** を選択します。</span><span class="sxs-lookup"><span data-stu-id="eab73-131">Select `WHSScheduleWorkCreationWaveStepMethod` and, on the Action Pane, select **Task configuration**.</span></span> <span data-ttu-id="eab73-132">必要に応じて、バッチ タスクの数と、リストされている各倉庫に割り当てられている複数のグループを変更または削除します。</span><span class="sxs-lookup"><span data-stu-id="eab73-132">Modify or delete the number of batch tasks and the assigned wave group for each listed warehouse as needed.</span></span>

## <a name="manually-configure-scheduled-work-creation"></a><span data-ttu-id="eab73-133">スケジュールされた作業の作成を手動で設定する</span><span class="sxs-lookup"><span data-stu-id="eab73-133">Manually configure scheduled work creation</span></span>

<span data-ttu-id="eab73-134">[*組織全体の 「作業作成のスケジュール」 ウェーブ メソッド* 機能](#Auto-enable-schedule-work-creation) を有効にしていない場合は、このセクションで説明する手順で、必要に応じてスケジュールされた仕事の作成を手動で設定することができます。</span><span class="sxs-lookup"><span data-stu-id="eab73-134">If you didn't enable the [*Organization-wide "Schedule work creation" wave method* feature](#Auto-enable-schedule-work-creation), then you can use the procedures provided in this section to manually configure scheduled work creation as needed.</span></span>

### <a name="manually-enable-batch-processing-of-waves"></a><span data-ttu-id="eab73-135">ウェーブのバッチ処理を手動で有効にする</span><span class="sxs-lookup"><span data-stu-id="eab73-135">Manually enable batch processing of waves</span></span>

<span data-ttu-id="eab73-136">並列非同期メソッドを利用して倉庫作業を作成するには、ウェーブ プロセスをバッチで実行する必要があります。</span><span class="sxs-lookup"><span data-stu-id="eab73-136">To take advantage of a parallel asynchronous method to create warehouse work, your wave process must be running in batch.</span></span> <span data-ttu-id="eab73-137">これを設定するには:</span><span class="sxs-lookup"><span data-stu-id="eab73-137">To set this up:</span></span>

1. <span data-ttu-id="eab73-138"> *\*倉庫管理 \> 設定 \> 倉庫管理パラメーター** の順に移動します。</span><span class="sxs-lookup"><span data-stu-id="eab73-138">Go to **Warehouse management \> Setup \> Warehouse management parameters**.</span></span>
1. <span data-ttu-id="eab73-139">**全般** タブで **ウェーブのバッチ処理** を *はい* に設定します。</span><span class="sxs-lookup"><span data-stu-id="eab73-139">On the **General** tab, set **Process waves in batch** to *Yes*.</span></span> <span data-ttu-id="eab73-140">必要に応じて、専用の **ウェーブを処理するバッチ グループ** を選択して、バッチ キューの処理が他のプロセスと同時に実行されないようにすることもできます。</span><span class="sxs-lookup"><span data-stu-id="eab73-140">Optionally, you can also select a dedicated **Wave processing batch group** to prevent your batch queue processing from running at the same time as other processes.</span></span>
1. <span data-ttu-id="eab73-141">システムが複数のウェーブを同時に処理する場合に適用される、**ロック待機 (ミリ秒) 時間** を設定します。</span><span class="sxs-lookup"><span data-stu-id="eab73-141">Set the **Wait for lock (ms) time**, which applies when the system is processing several waves at the same time.</span></span> <span data-ttu-id="eab73-142">大規模なウェーブ プロセスの場合は、値を *60000* にすることをお勧めします。</span><span class="sxs-lookup"><span data-stu-id="eab73-142">For most larger waving processes, we recommend a value of *60000*.</span></span>

### <a name="manually-enable-the-new-wave-step-method-for-existing-wave-templates"></a><span data-ttu-id="eab73-143">既存のウェーブ テンプレートに対して新しいウェーブ ステップ メソッドを手動で有効にする</span><span class="sxs-lookup"><span data-stu-id="eab73-143">Manually enable the new wave step method for existing wave templates</span></span>

<span data-ttu-id="eab73-144">最初に、新しいウェーブ ステップ メソッドを作成し、並列非同期タスク処理を有効にします。</span><span class="sxs-lookup"><span data-stu-id="eab73-144">Start by creating the new wave step method and enabling it for parallel asynchronous task processing.</span></span>

1. <span data-ttu-id="eab73-145"> *\*倉庫管理 \> 設定 \> ウェーブ \> ウェーブのプロセス メソッド** に移動します。</span><span class="sxs-lookup"><span data-stu-id="eab73-145">Go to **Warehouse management \> Setup \> Waves \> Wave process methods**.</span></span>
1. <span data-ttu-id="eab73-146"> *\*メソッドの再生成** を選択して、\*WHSScheduleWorkCreationWaveStepMethod* が出荷ウェーブ テンプレートで使用できるウェーブ プロセス メソッドの一覧に追加されていることに注意してください。</span><span class="sxs-lookup"><span data-stu-id="eab73-146">Select  **Regenerate method** and note that *WHSScheduleWorkCreationWaveStepMethod* has been added to the list of wave process methods you can use in your shipping wave templates.</span></span>
1. <span data-ttu-id="eab73-147">**メソッド名** *WHSScheduleWorkCreationWaveStepMethod* を含むレコードを選択し、**タスク構成** を選択します。</span><span class="sxs-lookup"><span data-stu-id="eab73-147">Select the record with the **Method name** *WHSScheduleWorkCreationWaveStepMethod* and select **Task configuration**.</span></span>
1. <span data-ttu-id="eab73-148">グリッドに新しい行を追加するには、アクション ウィンドウで **新規** を選択して、次の設定を使用します:</span><span class="sxs-lookup"><span data-stu-id="eab73-148">To add a new row to the grid, select **New** on the Action Pane and use the following settings:</span></span>

    - <span data-ttu-id="eab73-149">**倉庫** - 作業作成処理をスケジュールするために使用する倉庫を選択します。</span><span class="sxs-lookup"><span data-stu-id="eab73-149">**Warehouse** - Select the warehouse you will use to schedule work creation processing.</span></span>
    - <span data-ttu-id="eab73-150">**バッチ タスクの最大数** - バッチ タスクの最大数を指定します。</span><span class="sxs-lookup"><span data-stu-id="eab73-150">**Maximum number of batch tasks** - Specify a maximum number of batch tasks.</span></span> <span data-ttu-id="eab73-151">ほとんどの場合、この値は 8-16 の範囲にする必要がありますが、シナリオに基づいて最適な設定を試することをお勧めします。</span><span class="sxs-lookup"><span data-stu-id="eab73-151">In most cases, this value should be in the range from 8-16, however we recommend that you experiment with the optimal setting based on your scenarios.</span></span>
    - <span data-ttu-id="eab73-152">**ウェーブを処理するバッチ グループ** - 専用のウェーブを処理するバッチ グループを選択して、バッチ キュー処理を最適化します。</span><span class="sxs-lookup"><span data-stu-id="eab73-152">**Wave processing batch group** - Select a dedicated wave processing batch group to optimize your batch queue processing.</span></span>

<span data-ttu-id="eab73-153">これで、既存のウェーブ テンプレートを更新 (または新しいテンプレートを作成) して、*作業作成のスケジュール* ウェーブ処理メソッドを使用する準備が整いました。</span><span class="sxs-lookup"><span data-stu-id="eab73-153">Now you are ready to update an existing wave template (or create a new one) to use the *Schedule work creation* wave processing method.</span></span>

1. <span data-ttu-id="eab73-154"> *\*倉庫管理 \> 設定 \> ウェーブ \> ウェーブ テンプレート** の順に移動します。</span><span class="sxs-lookup"><span data-stu-id="eab73-154">Go to **Warehouse management \> Setup \> Waves \> Wave templates**.</span></span>
1. <span data-ttu-id="eab73-155">アクション ペインで **編集** を選択します。</span><span class="sxs-lookup"><span data-stu-id="eab73-155">Select **Edit** on the Action Pane.</span></span>
1. <span data-ttu-id="eab73-156">リスト ペインで、更新するウェーブ テンプレートを選択します (デモ データを使用してテストを行っている場合は、*24 出荷の既定* を使用できます)。</span><span class="sxs-lookup"><span data-stu-id="eab73-156">In the list pane, select the wave template you would like to update (if you are testing using demo data, then you could use *24 Shipping default*).</span></span>
1. <span data-ttu-id="eab73-157">**メソッド** クイック タブを展開し、**残りのメソッド** グリッドで **名前** *作業作成のスケジュール* の行を選択します。</span><span class="sxs-lookup"><span data-stu-id="eab73-157">Expand the **Methods** FastTab and select the row with the **Name** *Schedule work creation* in the **Remaining methods** grid.</span></span>
1. <span data-ttu-id="eab73-158">**選択されたメソッド** 列を指す矢印を選択して、選択した行をその列に移動します。</span><span class="sxs-lookup"><span data-stu-id="eab73-158">Select the arrow pointing to the **Selected methods** column to move the selected row to that column.</span></span> <span data-ttu-id="eab73-159">`WHSScheduleWorkCreationWaveStepMethod` または `createWork` を使用する選択済みのメソッドは一度にひとつしかないため、**メソッド名** `createWork` の既存の行は自動的に **残りのメソッド** グリッドに移動します。</span><span class="sxs-lookup"><span data-stu-id="eab73-159">(You can only have one selected method at a time that uses either `WHSScheduleWorkCreationWaveStepMethod` or `createWork`, so the existing row with **Method name** `createWork` is automatically moved to the **Remaining methods** grid.)</span></span>

## <a name="set-wave-task-processing-threshold-data"></a><span data-ttu-id="eab73-160">ウェーブ タスク処理のしきい値データの設定</span><span class="sxs-lookup"><span data-stu-id="eab73-160">Set wave task processing threshold data</span></span>

<span data-ttu-id="eab73-161">システムは、タスク ベースの処理を使用してウェーブ プロセスを初めて実行するときに、既定のウェーブ タスク処理のしきい値データを作成します。</span><span class="sxs-lookup"><span data-stu-id="eab73-161">The system will create default wave task processing threshold data the first time a wave process runs using any task-based processing.</span></span> <span data-ttu-id="eab73-162">データは、ウェーブ処理を非同期に実行し、タスク ベースにするタイミングを制御するために使用されます。これにより、ウェーブ処理を並行して処理し、作業を作成できます。</span><span class="sxs-lookup"><span data-stu-id="eab73-162">The data is used to control when wave processing will run asynchronously and be task-based, which enables it to process and create work in parallel.</span></span>

<span data-ttu-id="eab73-163">既定のデータでは、最初に、最小積荷明細行数 (`MINIMUMWAVELOADLINES`) に対してしきい値 15 が使用されます。</span><span class="sxs-lookup"><span data-stu-id="eab73-163">The default data will initially use a threshold value of 15 for the minimum number of load lines (`MINIMUMWAVELOADLINES`).</span></span> <span data-ttu-id="eab73-164">つまり、システムが、15 より多い積荷明細行を含むウェーブを処理すると、非同期タスク処理を使用します。</span><span class="sxs-lookup"><span data-stu-id="eab73-164">This means that when the system processes a wave with more than 15 loads lines, it will use asynchronous task processing.</span></span> <span data-ttu-id="eab73-165">テスト環境では、このデータを `WHSWaveTaskProcessingThresholdParameters` テーブルに手動で挿入/更新することができます。</span><span class="sxs-lookup"><span data-stu-id="eab73-165">You can manually insert/update this data in the `WHSWaveTaskProcessingThresholdParameters` table in your test environments.</span></span> <span data-ttu-id="eab73-166">運用環境でこの設定を変更する必要がある場合は、マイクロソフトのサポートに連絡してアップデートを依頼する必要があります。</span><span class="sxs-lookup"><span data-stu-id="eab73-166">If you need to change this setting in a production environment, you must contact Microsoft Support to request the update.</span></span>

## <a name="work-with-the-scheduled-work-creation"></a><span data-ttu-id="eab73-167">スケジュールされた作業の作成に関する作業</span><span class="sxs-lookup"><span data-stu-id="eab73-167">Work with the scheduled work creation</span></span>

<span data-ttu-id="eab73-168">スケジュールされた作業の作成を使用する方法の詳細については、[ウェーブの作成と処理](wave-processing.md) を参照してください。</span><span class="sxs-lookup"><span data-stu-id="eab73-168">For details about how to work with scheduled work creation, see [Wave creation and processing](wave-processing.md).</span></span> 


[!INCLUDE[footer-include](../../includes/footer-banner.md)]
