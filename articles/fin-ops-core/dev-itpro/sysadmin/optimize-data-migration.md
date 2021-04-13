---
title: Finance and Operations アプリのデータ移行の最適化
description: このトピックでは、Finance and Operations アプリのデータ移行を最適化するために使用できる手順とアクションの概要を示します。
author: skaue-ms
ms.date: 02/03/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: IT Pro
ms.reviewer: sericks
ms.search.region: Global
ms.author: toskaue
ms.search.validFrom: 2021-01-31
ms.dyn365.ops.version: 10.0.13
ms.openlocfilehash: 80ff2e6a1ceb0f5df23281c1a935ce2600d0f1ea
ms.sourcegitcommit: 074b6e212d19dd5d84881d1cdd096611a18c207f
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 03/31/2021
ms.locfileid: "5745943"
---
# <a name="optimize-data-migration-for-finance-and-operations-apps"></a><span data-ttu-id="5ef54-103">Finance and Operations アプリのデータ移行の最適化</span><span class="sxs-lookup"><span data-stu-id="5ef54-103">Optimize data migration for Finance and Operations apps</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="5ef54-104">データ移行は、ほとんどすべての実装で重要な成功要因です。</span><span class="sxs-lookup"><span data-stu-id="5ef54-104">Data migration is a key success factor in almost every implementation.</span></span> <span data-ttu-id="5ef54-105">一部の顧客の主な関心事項は、特に大量のデータと小さな切替ウィンドウがある場合の、データ移行の速度です。</span><span class="sxs-lookup"><span data-stu-id="5ef54-105">A primary concern of some customers is the speed that data can be migrated at, especially if there are vast amounts of data and a small cutover window.</span></span> <span data-ttu-id="5ef54-106">[データ移行フレームワーク](../data-entities/data-entities-data-packages.md) は、業務要件や操作の一部としてデータを移動するためにも使用されます。</span><span class="sxs-lookup"><span data-stu-id="5ef54-106">The [Data migration framework](../data-entities/data-entities-data-packages.md) is also used to move data as part of business requirements and operations.</span></span>

<span data-ttu-id="5ef54-107">このトピックの情報は、データ移行のパフォーマンスを最適化するために使用できる一連のステップとアクションを表します。</span><span class="sxs-lookup"><span data-stu-id="5ef54-107">The information in this topic represents a set of steps and actions that you can use to optimize the performance of data migration.</span></span>

> [!NOTE]
> <span data-ttu-id="5ef54-108">レベル 1 環境でのテスト結果を、レベル 2 以上のサンドボックス環境のパフォーマンスと比較または推定しないでください。</span><span class="sxs-lookup"><span data-stu-id="5ef54-108">Testing results in a Tier-1 environment should not be compared or extrapolated to performance in a Tier-2 or higher sandbox environment.</span></span>

<span data-ttu-id="5ef54-109">すべての標準エンティティがデータ移行用に最適化されているわけではありません。</span><span class="sxs-lookup"><span data-stu-id="5ef54-109">Not all standard entities have been optimized for data migration.</span></span> <span data-ttu-id="5ef54-110">一部のエンティティは、Open Data Protocol (OData) との統合に対して最適化されています。また、必要なエンティティをパフォーマンス要件を満たすように最適化できない場合は、[新しい最適化されたエンティティを作成](../data-entities/build-consuming-data-entities.md) することをお勧めします。</span><span class="sxs-lookup"><span data-stu-id="5ef54-110">Some entities have been optimized for integration with Open Data Protocol (OData), and if a required entity can't be optimized to meet the performance requirements, we recommend that you [create a new optimized entity](../data-entities/build-consuming-data-entities.md).</span></span> <span data-ttu-id="5ef54-111">開発者は、既存のエンティティを複製することで、このプロセスを迅速化できます。</span><span class="sxs-lookup"><span data-stu-id="5ef54-111">A developer can accelerate this process by duplicating an existing entity.</span></span>

<span data-ttu-id="5ef54-112">データのサブセットを使用して最適化フェーズを開始します。</span><span class="sxs-lookup"><span data-stu-id="5ef54-112">Begin the optimization phase by using a subset of the data.</span></span> <span data-ttu-id="5ef54-113">たとえば、100 万のレコードをインポートする必要がある場合は、1,000 レコードから始めて、10,000 レコードに増やし、その後 100,000 レコードに増やすことを検討してください。</span><span class="sxs-lookup"><span data-stu-id="5ef54-113">For example, if you must import one million records, consider starting with 1,000 records, then increase the number to 10,000 records, and then increase it to 100,000 records.</span></span>

<span data-ttu-id="5ef54-114">使用するエンティティを特定した後は、次のセクションを実行して最適化の機会を探します。</span><span class="sxs-lookup"><span data-stu-id="5ef54-114">After you've identified the entities that you will use, you should go through the following sections to explore opportunities for optimization.</span></span>

## <a name="disable-change-tracking"></a><span data-ttu-id="5ef54-115">変更追跡を無効にする</span><span class="sxs-lookup"><span data-stu-id="5ef54-115">Disable change tracking</span></span>

<span data-ttu-id="5ef54-116">エンティティの一覧から[変更追跡を有効化または無効化](../data-entities/entity-change-track.md) できます。</span><span class="sxs-lookup"><span data-stu-id="5ef54-116">You can [enable and disable change tracking](../data-entities/entity-change-track.md) from the list of entities.</span></span>

1. <span data-ttu-id="5ef54-117">**データ管理** ワークスペースで、**フレームワーク パラメーター** タイルを選択します。</span><span class="sxs-lookup"><span data-stu-id="5ef54-117">In the **Data management** workspace, select the **Data entities** tile.</span></span>
2. <span data-ttu-id="5ef54-118">**ターゲット エンティティ** ページで、グリッドでエンティティを選択し、アクション ウィンドウの **変更追跡** タブで、**変更追跡を無効にする** を選択します。</span><span class="sxs-lookup"><span data-stu-id="5ef54-118">On the **Target entities** page, select the entity in the grid, and then, on the Action Pane, on the **Change tracking** tab, select **Disable Change Tracking**.</span></span>

## <a name="enable-set-based-processing"></a><span data-ttu-id="5ef54-119">セットベースのプロセスを有効にする</span><span class="sxs-lookup"><span data-stu-id="5ef54-119">Enable set-based processing</span></span>

<span data-ttu-id="5ef54-120">エンティティがセットベースのプロセスをサポートしている場合は、次の手順に従います。</span><span class="sxs-lookup"><span data-stu-id="5ef54-120">Follow these steps to verify that an entity supports set-based processing.</span></span>

1. <span data-ttu-id="5ef54-121">**データ管理** ワークスペースで、**フレームワーク パラメーター** タイルを選択します。</span><span class="sxs-lookup"><span data-stu-id="5ef54-121">In the **Data management** workspace, select the **Data entities** tile.</span></span>
2. <span data-ttu-id="5ef54-122">**ターゲット エンティティ** ページで、グリッドでエンティティを検索し、**セットベースのプロセス** 列の値を確認します。</span><span class="sxs-lookup"><span data-stu-id="5ef54-122">On the **Target entities** page, find the entity in the grid, and review the value in the **Set-based processing** column.</span></span>

<span data-ttu-id="5ef54-123">**一般仕訳帳** エンティティに対してセットベースのプロセスを有効にする方法を示す例については、[一般仕訳帳エンティティを使用して伝票をインポートするためのベスト プラクティス](../data-entities/tips-tricks-import-general-journal-entity.md) を参照してください。</span><span class="sxs-lookup"><span data-stu-id="5ef54-123">For an example that shows how set-based processing can be enabled for the **General Journal** entity, see [Best practices for importing vouchers by using the General journal entity](../data-entities/tips-tricks-import-general-journal-entity.md).</span></span> <span data-ttu-id="5ef54-124">すべてのエンティティがセットベースのプロセスをサポートしているわけではありません。</span><span class="sxs-lookup"><span data-stu-id="5ef54-124">Not all entities support set-based processing.</span></span> <span data-ttu-id="5ef54-125">たとえば、**顧客の定義** (**CustCustomerBaseEntity**) エンティティに対してセットベースのプロセスのサポートを有効にして、変更を保存しようとすると、次の警告メッセージが表示されます。</span><span class="sxs-lookup"><span data-stu-id="5ef54-125">For example, if you try to enable support set-based processing for the **Customer definitions** (**CustCustomerBaseEntity**) entity and save your change, you will receive the following warning message:</span></span>

> <span data-ttu-id="5ef54-126">セット操作は「顧客の定義」エンティティではサポートされていません。</span><span class="sxs-lookup"><span data-stu-id="5ef54-126">Set operations not supported for 'Customer definitions' entity.</span></span>

<span data-ttu-id="5ef54-127">セットベースのプロセスが可能なエンティティを作成する必要がある場合の重要な考慮事項を次に示します。</span><span class="sxs-lookup"><span data-stu-id="5ef54-127">Here are some important considerations if you must create an entity that allows for set-based processing:</span></span>

* <span data-ttu-id="5ef54-128">データ ソースは読み取り専用に設定できません。</span><span class="sxs-lookup"><span data-stu-id="5ef54-128">The data sources can't be read-only.</span></span>
* <span data-ttu-id="5ef54-129">データ エンティティ ビューの [**ValidTimeStateEnabled**](../dev-tools/date-effectivity.md) プロパティは **いいえ** に設定する必要があります。</span><span class="sxs-lookup"><span data-stu-id="5ef54-129">The [**ValidTimeStateEnabled**](../dev-tools/date-effectivity.md) property of the data entity view the must be set to **No**.</span></span>
* <span data-ttu-id="5ef54-130">データ ソース上のすべてのテーブルで、**TableType** プロパティが **通常** に設定されている必要があります 。</span><span class="sxs-lookup"><span data-stu-id="5ef54-130">All tables on the data sources must have **TableType** property set to **Regular**.</span></span>
* <span data-ttu-id="5ef54-131">使用される **クエリ** の [**QueryType**](../dev-ref/application-explorer-aot-properties.md#query-properties-1) を **Union** に設定することはできません。</span><span class="sxs-lookup"><span data-stu-id="5ef54-131">The property [**QueryType**](../dev-ref/application-explorer-aot-properties.md#query-properties-1) on the used **Query** can't be set to **Union**.</span></span>
* <span data-ttu-id="5ef54-132">主要データ ソースは会社間でデータが保存されるのを防ぐことができません。</span><span class="sxs-lookup"><span data-stu-id="5ef54-132">The main data source can't prevent data from being saved across companies.</span></span> <span data-ttu-id="5ef54-133">ただし、埋め込みデータ ソースでは可能です。</span><span class="sxs-lookup"><span data-stu-id="5ef54-133">However, embedded data sources allow it.</span></span>
* <span data-ttu-id="5ef54-134">主要データ ソースはパーティション間でデータが保存されるのを防ぐことができません。</span><span class="sxs-lookup"><span data-stu-id="5ef54-134">The main data source can't prevent data from being saved across partitions.</span></span> <span data-ttu-id="5ef54-135">ただし、埋め込みデータ ソースでは可能です。</span><span class="sxs-lookup"><span data-stu-id="5ef54-135">However, embedded data sources allow it.</span></span>

## <a name="create-a-data-migration-batch-group"></a><span data-ttu-id="5ef54-136">データ移行バッチ グループの作成</span><span class="sxs-lookup"><span data-stu-id="5ef54-136">Create a data migration batch group</span></span>

<span data-ttu-id="5ef54-137">切替中に、他の活動がほとんどまたは全くないト時にデータ移行を実行します。</span><span class="sxs-lookup"><span data-stu-id="5ef54-137">During cutover, run the data migration while there is little or no other activity.</span></span> <span data-ttu-id="5ef54-138">ほとんどまたはすべての計算ノードが割り当てられているバッチ グループを構成して使用すると便利です。</span><span class="sxs-lookup"><span data-stu-id="5ef54-138">It can be helpful to configure and use a batch group where most or all compute nodes are assigned.</span></span>

<span data-ttu-id="5ef54-139">バッチ グループは、**バッチ グループ** ページ (**システム管理 \> 設定 \> バッチ グループ**) で構成できます。</span><span class="sxs-lookup"><span data-stu-id="5ef54-139">You can configure a batch group on the **Batch group** page (**System administration \> Setup \> Batch group**).</span></span>

## <a name="enable-priority-based-batch-scheduling"></a><span data-ttu-id="5ef54-140">優先順位に基づくバッチ スケジューリングを有効にする</span><span class="sxs-lookup"><span data-stu-id="5ef54-140">Enable priority-based batch scheduling</span></span>

<span data-ttu-id="5ef54-141">プラットフォーム更新プログラム 31 では、新しい[優先順位に基づくバッチ スケジューリング](priority-based-batch-scheduling.md) 機能によって、ジョブの実行方法が最適化されます。</span><span class="sxs-lookup"><span data-stu-id="5ef54-141">In Platform update 31, the new [priority-based batch scheduling](priority-based-batch-scheduling.md) feature optimizes how batch jobs are run.</span></span> <span data-ttu-id="5ef54-142">バッチ フレームワークで競合が特定されている場合は、優先順位に基づくバッチ スケジューリングを有効にすることを検討してください。</span><span class="sxs-lookup"><span data-stu-id="5ef54-142">If contention is identified in the batch framework, consider enabling priority-based batch scheduling.</span></span>

## <a name="configure-the-maximum-number-of-batch-threads"></a><span data-ttu-id="5ef54-143">バッチ スレッドの最大数を構成する</span><span class="sxs-lookup"><span data-stu-id="5ef54-143">Configure the maximum number of batch threads</span></span>

<span data-ttu-id="5ef54-144">並列処理とマルチスレッド処理をより有効に利用するために、**サーバーの構成** ページの **バッチ スレッドの最大数** フィールド (**システム管理 \> 設定 \> サーバーの構成**) を設定することにより、Application Object Server (AOS) のインスタンスごとにバッチ スレッドの最大数を構成できます。</span><span class="sxs-lookup"><span data-stu-id="5ef54-144">To better use parallelism and multithreading, you can configure the maximum number of batch threads per instance of Application Object Server (AOS) by setting the **Maximum batch threads** field on the **Server configuration** page (**System administration \> Setup \> Server configuration**).</span></span> <span data-ttu-id="5ef54-145">このフィールドの値の変更には注意が必要です。</span><span class="sxs-lookup"><span data-stu-id="5ef54-145">Be careful about changing the value of this field.</span></span> <span data-ttu-id="5ef54-146">値が高すぎるとパフォーマンスに悪影響が及ぼす可能性があります。</span><span class="sxs-lookup"><span data-stu-id="5ef54-146">A value that is too high can have negative performance implications.</span></span> <span data-ttu-id="5ef54-147">現在、既定値は **4** です。</span><span class="sxs-lookup"><span data-stu-id="5ef54-147">Currently, the default value is **4**.</span></span> <span data-ttu-id="5ef54-148">必要に応じて値を **8** に変更することもできます。</span><span class="sxs-lookup"><span data-stu-id="5ef54-148">You can change the value to **8** as you require.</span></span> <span data-ttu-id="5ef54-149">ただし、大幅なパフォーマンス テストを行わない限り、このフィールドを 8 を超える値に設定しないでください。</span><span class="sxs-lookup"><span data-stu-id="5ef54-149">However, you should not set the field to a value that is more than 8 unless you do significant performance testing.</span></span>

## <a name="import-in-batch-mode"></a><span data-ttu-id="5ef54-150">バッチ モードでのインポート</span><span class="sxs-lookup"><span data-stu-id="5ef54-150">Import in batch mode</span></span>

<span data-ttu-id="5ef54-151">インポート ジョブを実行する際は、必ずバッチ モードで実行します。</span><span class="sxs-lookup"><span data-stu-id="5ef54-151">Whenever you run an import job, make sure that it's run in batch mode.</span></span> <span data-ttu-id="5ef54-152">それ以外の場合は、単一のスレッドがジョブの実行に使用されます。</span><span class="sxs-lookup"><span data-stu-id="5ef54-152">Otherwise, a single thread will be used to run the job.</span></span> <span data-ttu-id="5ef54-153">この場合、システムではこれらの最適化の構成を十分に活用できません。</span><span class="sxs-lookup"><span data-stu-id="5ef54-153">In this case, the system won't be able to take full advantage of these optimization configurations.</span></span>

## <a name="clean-staging-tables"></a><span data-ttu-id="5ef54-154">ステージング テーブルのクリーンアップ</span><span class="sxs-lookup"><span data-stu-id="5ef54-154">Clean staging tables</span></span>

<span data-ttu-id="5ef54-155">ステージング テーブルをクリーンアップすることをお勧めします。</span><span class="sxs-lookup"><span data-stu-id="5ef54-155">We recommend that you clean up the staging tables.</span></span> <span data-ttu-id="5ef54-156">プラットフォーム更新プログラム 29 以降では、[ジョブ履歴のクリーンアップ ジョブ](../data-entities/data-import-export-job.md#job-history-clean-up-available-in-platform-update-29-and-later) をスケジュールすることでこの最適化を実現できます。</span><span class="sxs-lookup"><span data-stu-id="5ef54-156">In Platform update 29 and later, you can achieve this optimization by scheduling the [Job history cleanup job](../data-entities/data-import-export-job.md#job-history-clean-up-available-in-platform-update-29-and-later).</span></span> <span data-ttu-id="5ef54-157">このジョブをスケジュールするには、**データ管理** ワークスペースの **ジョブ履歴クリーンアップ** タスクを選択します。</span><span class="sxs-lookup"><span data-stu-id="5ef54-157">To schedule this job, select the **Job history cleanup** tile in the **Data management** workspace.</span></span>

> [!NOTE]
> <span data-ttu-id="5ef54-158">最初に **機能管理** ワークスペースの **実行履歴のクリーンアップ** 機能を有効にする必要があります。</span><span class="sxs-lookup"><span data-stu-id="5ef54-158">You must first turn on the **Execution history cleanup** feature in the **Feature management** workspace.</span></span>


## <a name="update-statistics"></a><span data-ttu-id="5ef54-159">統計の更新</span><span class="sxs-lookup"><span data-stu-id="5ef54-159">Update statistics</span></span>

<span data-ttu-id="5ef54-160">大量のデータが関係するデータ移行ジョブを実行する前に、関連するテーブルの統計の更新を検討してください。</span><span class="sxs-lookup"><span data-stu-id="5ef54-160">Before you run a data migration job that involves a large volume of data, consider updating the statistics across the associated tables.</span></span> <span data-ttu-id="5ef54-161">この最適化は運用環境で自動的に処理されるので、特にサンドボックス環境に適用されます。</span><span class="sxs-lookup"><span data-stu-id="5ef54-161">This optimization applies specifically to sandbox environments, because it's handled automatically in production environments.</span></span> <span data-ttu-id="5ef54-162">[LCS から特定のテーブルの統計を更新](../lifecycle-services/querycookbook.md) できます。</span><span class="sxs-lookup"><span data-stu-id="5ef54-162">You can [update statistics for a specific table from LCS](../lifecycle-services/querycookbook.md).</span></span> <span data-ttu-id="5ef54-163">または、サンドボックス環境では、直接 SQL を介して **sp\_updatestats** ストアド プロシージャを使用できます。</span><span class="sxs-lookup"><span data-stu-id="5ef54-163">Alternatively, in a sandbox environment, you can use the **sp\_updatestats** stored procedure through direct SQL.</span></span>

## <a name="clean-the-data"></a><span data-ttu-id="5ef54-164">データのクリーンアップ</span><span class="sxs-lookup"><span data-stu-id="5ef54-164">Clean the data</span></span>

<span data-ttu-id="5ef54-165">検証およびエラー報告に費やす時間は、移行の合計時間を増加します。</span><span class="sxs-lookup"><span data-stu-id="5ef54-165">The time that is spent on validations and error reporting will increase the total time of the migration.</span></span> <span data-ttu-id="5ef54-166">量の多い無効または不整合なデータをインポートする場合は、この点を考慮してください。</span><span class="sxs-lookup"><span data-stu-id="5ef54-166">Consider this fact when you import a high volume of invalid or inconsistent data.</span></span> <span data-ttu-id="5ef54-167">データの品質に関連するエラーを修正および削減することをお勧めします。</span><span class="sxs-lookup"><span data-stu-id="5ef54-167">We recommend that you try to fix and reduce errors that are related to data quality.</span></span> <span data-ttu-id="5ef54-168">これにより、検証やエラー処理が不必要に実行されるのを防ぐのに役立ちます。</span><span class="sxs-lookup"><span data-stu-id="5ef54-168">In this way, you help prevent unnecessary executions of validation and error handling.</span></span>

## <a name="configurations-to-test-during-test-runs-of-data-migration"></a><span data-ttu-id="5ef54-169">データ移行のテストの実行中にテストする構成</span><span class="sxs-lookup"><span data-stu-id="5ef54-169">Configurations to test during test runs of data migration</span></span>

<span data-ttu-id="5ef54-170">パフォーマンスに影響を与える可能性がある構成は次のとおりです。</span><span class="sxs-lookup"><span data-stu-id="5ef54-170">The following configurations can affect performance.</span></span> <span data-ttu-id="5ef54-171">したがって、シナリオに適したさまざまな値を使用して変更をテストすることをお勧めします。</span><span class="sxs-lookup"><span data-stu-id="5ef54-171">Therefore, we recommend that you test changes by using different values that are suitable for your scenario.</span></span>

### <a name="configure-entity-execution-parameters"></a><span data-ttu-id="5ef54-172">エンティティの実行パラメーターを構成します</span><span class="sxs-lookup"><span data-stu-id="5ef54-172">Configure entity execution parameters</span></span>

<span data-ttu-id="5ef54-173">すべてのエンティティまたは特定のエンティティの実行パラメーターを変更するには、次の手順に従います。</span><span class="sxs-lookup"><span data-stu-id="5ef54-173">Follow these steps to change the execution parameters for all entities or specific entities.</span></span>

1. <span data-ttu-id="5ef54-174">**データ管理** ワークスペースで、**フレームワーク パラメーター** タイルを選択します。</span><span class="sxs-lookup"><span data-stu-id="5ef54-174">In the **Data management** workspace, select the **Framework parameters** tile.</span></span>
2. <span data-ttu-id="5ef54-175">**エンティティ設定** タブの **データのインポート/エクスポート フレームワーク パラメーター** ページで、**エンティティの実行パラメーターを構成する** を選択します。</span><span class="sxs-lookup"><span data-stu-id="5ef54-175">On the **Data import/export framework parameters** page, on the **Entity settings** tab, select **Configure entity execution parameters**.</span></span>
3. <span data-ttu-id="5ef54-176">**エンティティ インポートの実行パラメーター** ページで、**インポートのしきい値レコード数** および **インポート タスク数** フィールドを目的のエンティティに適切に設定します。</span><span class="sxs-lookup"><span data-stu-id="5ef54-176">On the **Entity import execution parameters** page, set the **Import threshold record count** and **Import task count** fields as appropriate for the desired entities.</span></span>

#### <a name="import-threshold-record-count"></a><span data-ttu-id="5ef54-177">インポートしきい値レコード数</span><span class="sxs-lookup"><span data-stu-id="5ef54-177">Import threshold record count</span></span>

<span data-ttu-id="5ef54-178">この値により、スレッドごとに処理されるレコード数が決まれます。</span><span class="sxs-lookup"><span data-stu-id="5ef54-178">This value determines the number of records to be processed per thread.</span></span> <span data-ttu-id="5ef54-179">[**インポートのしきい値レコード数** を変更](../data-entities/data-import-export-job.md#parallel-imports) することで、インポートを小さいタスクに分割する方法を制御できます。</span><span class="sxs-lookup"><span data-stu-id="5ef54-179">[By modifying the **Import threshold record count**](../data-entities/data-import-export-job.md#parallel-imports) you can control how you want to split the import into smaller tasks.</span></span>

#### <a name="import-task-count"></a><span data-ttu-id="5ef54-180">インポート タスク数</span><span class="sxs-lookup"><span data-stu-id="5ef54-180">Import task count</span></span>

<span data-ttu-id="5ef54-181">このフィールドは、特定のエンティティのデータ移行ジョブに使用されるスレッドの数を定義します。</span><span class="sxs-lookup"><span data-stu-id="5ef54-181">This field defines the number of threads that will be used for the data migration job for a specific entity.</span></span> <span data-ttu-id="5ef54-182">たとえば、各サーバーの **最大バッチ スレッド** フィールドが **8** に設定され、データ移行バッチ グループに 4 つのサーバーが割り当てられます。</span><span class="sxs-lookup"><span data-stu-id="5ef54-182">For example, the **Maximum batch threads** field for each server is set to **8**, and four servers are assigned to the data migration batch group.</span></span> <span data-ttu-id="5ef54-183">この場合、**インポート タスク数** フィールドの合計最大値は **32** (= 8 × 4) になります。</span><span class="sxs-lookup"><span data-stu-id="5ef54-183">In this case, the total maximum value of the **Import task count** field is **32** (= 8 × 4).</span></span>

<span data-ttu-id="5ef54-184">データ エンティティがマルチスレッドをサポートしない場合、エンティティを構成しようとする場合にエラー メッセージが表示されます。</span><span class="sxs-lookup"><span data-stu-id="5ef54-184">If a data entity doesn't support multithreading, you receive an error message when you try to configure the entity.</span></span> <span data-ttu-id="5ef54-185">次に例を示します。</span><span class="sxs-lookup"><span data-stu-id="5ef54-185">Here is an example:</span></span>

> <span data-ttu-id="5ef54-186">カスタム シーケンスはエンティティ「顧客 V3」に対して定義されています。複数のタスクはサポートされていません。</span><span class="sxs-lookup"><span data-stu-id="5ef54-186">Custom sequence is defined for the entity 'Customers V3', more than one task is not supported.</span></span>

### <a name="validations"></a><span data-ttu-id="5ef54-187">検証</span><span class="sxs-lookup"><span data-stu-id="5ef54-187">Validations</span></span>

<span data-ttu-id="5ef54-188">レコードの挿入または更新の検証ロジックがシステムに組み込まれているか、個々のフィールドの検証が行われている場合があります。</span><span class="sxs-lookup"><span data-stu-id="5ef54-188">Validation logic for record insertions or updates might have been incorporated into the system, or there might be validation of individual fields.</span></span> <span data-ttu-id="5ef54-189">データ移行の完成度が十分に高い場合は、この検証を無効にすることで、インポートに費やした時間が大幅に短縮されます (無効にできる場合)。</span><span class="sxs-lookup"><span data-stu-id="5ef54-189">If the data migration is mature enough, the time that is spent on imports can be significantly reduced by disabling this validation, if it can be disabled.</span></span>

<span data-ttu-id="5ef54-190">次の手順に従って、各エンティティの設定を変更します。</span><span class="sxs-lookup"><span data-stu-id="5ef54-190">Follow these steps to change the settings for each entity.</span></span>

1. <span data-ttu-id="5ef54-191">**データ管理** ワークスペースで、**フレームワーク パラメーター** タイルを選択します。</span><span class="sxs-lookup"><span data-stu-id="5ef54-191">In the **Data management** workspace, select the **Data entities** tile.</span></span>
2. <span data-ttu-id="5ef54-192">**ターゲット エンティティ** ページで、グリッドでエンティティを選択し、アクション ウィンドウで **エンティティ構造** を選択します。</span><span class="sxs-lookup"><span data-stu-id="5ef54-192">On the **Target entities** page, select the entity in the grid, and then, on the Action Pane, select **Entity structure**.</span></span>
3. <span data-ttu-id="5ef54-193">**エンティティ構造** ページで、**ビジネス検証** および **挿入または更新メソッドでのビジネス ロジックの実行** フィールドを適切に設定します。</span><span class="sxs-lookup"><span data-stu-id="5ef54-193">On the **Entity structure** page, set the **Run business validations** and **Run business logic in insert or update method** fields as appropriate.</span></span>

#### <a name="run-business-validations"></a><span data-ttu-id="5ef54-194">業務検証の実行</span><span class="sxs-lookup"><span data-stu-id="5ef54-194">Run business validations</span></span>

<span data-ttu-id="5ef54-195">このチェック ボックスがオンの場合、システムはテーブルの **validateWrite()** メソッドに書き込まれるすべてのロジックを実行します。</span><span class="sxs-lookup"><span data-stu-id="5ef54-195">If this check box is selected, the system will run any logic that is written into the **validateWrite()** method on the table.</span></span> <span data-ttu-id="5ef54-196">また、関連するイベント ハンドラーも実行されます。</span><span class="sxs-lookup"><span data-stu-id="5ef54-196">It will also run any related event handlers.</span></span>

#### <a name="run-business-logic-in-insert-or-update-method"></a><span data-ttu-id="5ef54-197">挿入方法または更新方法のビジネス ロジックを実行</span><span class="sxs-lookup"><span data-stu-id="5ef54-197">Run business logic in insert or update method</span></span>

<span data-ttu-id="5ef54-198">このチェック ボックスがオンの場合、システムはテーブルの **挿入 ()** または **更新 ()** メソッドに書き込まれるすべてのロジックを実行します。</span><span class="sxs-lookup"><span data-stu-id="5ef54-198">If this check box is selected, the system will run any logic that is written into the **insert()** or **update()** method on the table.</span></span> <span data-ttu-id="5ef54-199">また、関連するイベント ハンドラーも実行されます。</span><span class="sxs-lookup"><span data-stu-id="5ef54-199">It will also run any related event handlers.</span></span>

#### <a name="call-the-validatefield-method-on-the-target"></a><span data-ttu-id="5ef54-200">ターゲットの validateField メソッドを呼び出す</span><span class="sxs-lookup"><span data-stu-id="5ef54-200">Call the validateField method on the target</span></span>

<span data-ttu-id="5ef54-201">フィールド検証を実行するには、次の手順を実行します。</span><span class="sxs-lookup"><span data-stu-id="5ef54-201">Follow these steps to run field validation.</span></span>

1. <span data-ttu-id="5ef54-202">**データ管理** ワークスペースで、**フレームワーク パラメーター** タイルを選択します。</span><span class="sxs-lookup"><span data-stu-id="5ef54-202">In the **Data management** workspace, select the **Data entities** tile.</span></span>
2. <span data-ttu-id="5ef54-203">**ターゲット エンティティ** ページで、グリッドでエンティティを選択し、アクション ウィンドウで **ターゲット マッピングの変更** を選択します。</span><span class="sxs-lookup"><span data-stu-id="5ef54-203">On the **Target entities** page, select the entity in the grid, and then, on the Action Pane, select **Modify target mapping**.</span></span>
3. <span data-ttu-id="5ef54-204">**ステージングをターゲットにマップ** ページで、検証を実行する必要があるフィールドの **フィールドの検証メソッドの呼び出し** チェック ボックスをオンにします。</span><span class="sxs-lookup"><span data-stu-id="5ef54-204">On the **Map staging to target** page, select the **Call validate Field method** check box for the field that validation should be run for.</span></span> <span data-ttu-id="5ef54-205">その後、そのフィールドに対して **validateField(FieldId p1)** メソッドが呼び出されます。</span><span class="sxs-lookup"><span data-stu-id="5ef54-205">The **validateField(FieldId p1)** method will then be called for that field.</span></span>

### <a name="recommendations-for-optimizing-data-migration-performance"></a><span data-ttu-id="5ef54-206">データ移行のパフォーマンスを最適化するための推奨事項</span><span class="sxs-lookup"><span data-stu-id="5ef54-206">Recommendations for optimizing data migration performance</span></span>

<span data-ttu-id="5ef54-207">データ移行のパフォーマンスを最適化するために使用する方法に関する一般的な推奨事項を次に示します。</span><span class="sxs-lookup"><span data-stu-id="5ef54-207">Here are some general recommendations about the approach that you should use to optimize the performance of data migration:</span></span>

* <span data-ttu-id="5ef54-208">大きなファイルを小さいチャンクに分割します。</span><span class="sxs-lookup"><span data-stu-id="5ef54-208">Break up large files into smaller chunks.</span></span> <span data-ttu-id="5ef54-209">この方法により、SQL オプティマイザは、新しいクエリ プランが最適かどうかを判断するための時間を確保できます。</span><span class="sxs-lookup"><span data-stu-id="5ef54-209">This approach gives the SQL optimizer time to determine whether a new query plan will be optimal.</span></span>
* <span data-ttu-id="5ef54-210">適切なレベル 2 以上の環境でパフォーマンスをテストします。</span><span class="sxs-lookup"><span data-stu-id="5ef54-210">Test performance in an appropriate Tier-2 or higher environment.</span></span>
* <span data-ttu-id="5ef54-211">運用前に、切替モックでのパフォーマンスをテストします。</span><span class="sxs-lookup"><span data-stu-id="5ef54-211">Test performance in a mock cutover before go-live.</span></span>

<span data-ttu-id="5ef54-212">データ移行のパフォーマンスのテストは、反復プロセスです。</span><span class="sxs-lookup"><span data-stu-id="5ef54-212">Testing of data migration performance is an iterative process.</span></span> <span data-ttu-id="5ef54-213">特定のエンティティの最適な構成を決定するために、各テストに関する情報を収集して比較することをお勧めします。</span><span class="sxs-lookup"><span data-stu-id="5ef54-213">We recommend that you collect and compare information about each test to determine the optimal configuration for a specific entity.</span></span> <span data-ttu-id="5ef54-214">次の設定の一部を収集して確認する必要があります。</span><span class="sxs-lookup"><span data-stu-id="5ef54-214">You should collect and verify some of the following settings:</span></span>

* <span data-ttu-id="5ef54-215">使用されるバッチ グループ</span><span class="sxs-lookup"><span data-stu-id="5ef54-215">The batch group that is used</span></span>
* <span data-ttu-id="5ef54-216">各バッチ グループに割り当てられるバッチ サーバーの数</span><span class="sxs-lookup"><span data-stu-id="5ef54-216">The number of batch servers that are assigned to each batch group</span></span>
* <span data-ttu-id="5ef54-217">バッチ サーバーごとのバッチ スレッドの最大数</span><span class="sxs-lookup"><span data-stu-id="5ef54-217">The maximum number of batch threads per batch server</span></span>

<span data-ttu-id="5ef54-218">各エンティティについて収集する情報の例を次に示します。</span><span class="sxs-lookup"><span data-stu-id="5ef54-218">Here is an example of the information that you might collect for each entity.</span></span>

| <span data-ttu-id="5ef54-219">情報</span><span class="sxs-lookup"><span data-stu-id="5ef54-219">Information</span></span> | <span data-ttu-id="5ef54-220">説明</span><span class="sxs-lookup"><span data-stu-id="5ef54-220">Description</span></span> |
|---|---|
| <span data-ttu-id="5ef54-221">エンティティ</span><span class="sxs-lookup"><span data-stu-id="5ef54-221">Entity</span></span> | <span data-ttu-id="5ef54-222">テストされているエンティティの名前</span><span class="sxs-lookup"><span data-stu-id="5ef54-222">The name of the entity that is being tested</span></span> |
| <span data-ttu-id="5ef54-223">レコード数</span><span class="sxs-lookup"><span data-stu-id="5ef54-223">Number of records</span></span> | <span data-ttu-id="5ef54-224">インポートされるレコード数</span><span class="sxs-lookup"><span data-stu-id="5ef54-224">The number of records that are being imported</span></span> |
| <span data-ttu-id="5ef54-225">ソース形式</span><span class="sxs-lookup"><span data-stu-id="5ef54-225">Source format</span></span> | <span data-ttu-id="5ef54-226">インポートされるデータのソース形式</span><span class="sxs-lookup"><span data-stu-id="5ef54-226">The source format of the data that is being imported</span></span> |
| <span data-ttu-id="5ef54-227">無効にされた変更追跡</span><span class="sxs-lookup"><span data-stu-id="5ef54-227">Change tracking disabled</span></span> | <span data-ttu-id="5ef54-228">はい/いいえ</span><span class="sxs-lookup"><span data-stu-id="5ef54-228">Yes/No</span></span> |
| <span data-ttu-id="5ef54-229">セット ベースのプロセス</span><span class="sxs-lookup"><span data-stu-id="5ef54-229">Set-based processing</span></span> | <span data-ttu-id="5ef54-230">はい/いいえ</span><span class="sxs-lookup"><span data-stu-id="5ef54-230">Yes/No</span></span> |
| <span data-ttu-id="5ef54-231">インポートしきい値レコード数</span><span class="sxs-lookup"><span data-stu-id="5ef54-231">Import threshold record count</span></span> | <span data-ttu-id="5ef54-232">レコード数</span><span class="sxs-lookup"><span data-stu-id="5ef54-232">The number of records</span></span> |
| <span data-ttu-id="5ef54-233">インポート タスク数</span><span class="sxs-lookup"><span data-stu-id="5ef54-233">Import task count</span></span> | <span data-ttu-id="5ef54-234">タスク数</span><span class="sxs-lookup"><span data-stu-id="5ef54-234">The number of tasks</span></span> |
| <span data-ttu-id="5ef54-235">業務検証の実行</span><span class="sxs-lookup"><span data-stu-id="5ef54-235">Run business validations</span></span> | <span data-ttu-id="5ef54-236">はい/いいえ</span><span class="sxs-lookup"><span data-stu-id="5ef54-236">Yes/No</span></span> |
| <span data-ttu-id="5ef54-237">挿入方法または更新方法のビジネス ロジックを実行</span><span class="sxs-lookup"><span data-stu-id="5ef54-237">Run business logic in insert or update method</span></span> | <span data-ttu-id="5ef54-238">はい/いいえ</span><span class="sxs-lookup"><span data-stu-id="5ef54-238">Yes/No</span></span> |
| <span data-ttu-id="5ef54-239">"フィールドの検証" メソッドの呼び出し</span><span class="sxs-lookup"><span data-stu-id="5ef54-239">Call validate Field method</span></span> | <span data-ttu-id="5ef54-240">はい/いいえ (潜在的なフィールドのリスト)</span><span class="sxs-lookup"><span data-stu-id="5ef54-240">Yes/No (potential field list)</span></span> |
| <span data-ttu-id="5ef54-241">必要なパフォーマンス</span><span class="sxs-lookup"><span data-stu-id="5ef54-241">Required performance</span></span> | <span data-ttu-id="5ef54-242">切替ウィンドウを達成するためにインポートを完了する必要がある時間</span><span class="sxs-lookup"><span data-stu-id="5ef54-242">The amount of time that the import must be completed within to achieve the cutover window</span></span> |
| <span data-ttu-id="5ef54-243">実際のパフォーマンス</span><span class="sxs-lookup"><span data-stu-id="5ef54-243">Actual performance</span></span> | <span data-ttu-id="5ef54-244">レコードのインポートに必要な実際の時間</span><span class="sxs-lookup"><span data-stu-id="5ef54-244">The actual amount of time that was required to import records</span></span> |

<span data-ttu-id="5ef54-245">パフォーマンスを最適化できる領域は他にもあります。</span><span class="sxs-lookup"><span data-stu-id="5ef54-245">There are more areas where performance can be optimized.</span></span> <span data-ttu-id="5ef54-246">たとえば、特定のクエリおよびクエリ プランを分析できます。</span><span class="sxs-lookup"><span data-stu-id="5ef54-246">For example, you can analyze the specific queries and query plans.</span></span> <span data-ttu-id="5ef54-247">ただし、これらのプロセスについては他のトピックで説明します。</span><span class="sxs-lookup"><span data-stu-id="5ef54-247">However, those processes are covered in other topics.</span></span>

<span data-ttu-id="5ef54-248">パフォーマンスのトラブルシューティングおよび最適化の詳細については、次のトピックを参照してください。</span><span class="sxs-lookup"><span data-stu-id="5ef54-248">For more information about performance troubleshooting and optimization, see the following topics:</span></span>

* [<span data-ttu-id="5ef54-249">Lifecycle Services (LCS) 内のツールを使用した、パフォーマンスのトラブルシューティング</span><span class="sxs-lookup"><span data-stu-id="5ef54-249">Performance troubleshooting using tools in Lifecycle Services (LCS)</span></span>](../lifecycle-services/performancetroubleshooting.md)
* [<span data-ttu-id="5ef54-250">クックブックの照会</span><span class="sxs-lookup"><span data-stu-id="5ef54-250">Query cookbook</span></span>](../lifecycle-services/querycookbook.md)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]