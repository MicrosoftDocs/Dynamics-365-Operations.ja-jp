---
title: 初期同期に関する考慮事項
description: このトピックでは、制約、既知の問題、およびデュアル書き込みの初期同期に関するガイダンスについて説明します。
author: RamaKrishnamoorthy
ms.date: 10/12/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Developer
ms.reviewer: rhaertle
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: ramasri
ms.search.validFrom: 2020-10-12
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 0d0272e1d895c5b1abee6add1bda2f89d97db4aa
ms.sourcegitcommit: a202bf67c3c2c054e2a47cb7b3145cb7c0ee635e
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/25/2021
ms.locfileid: "5941210"
---
# <a name="considerations-for-initial-synchronization"></a><span data-ttu-id="cd315-103">初期同期に関する考慮事項</span><span class="sxs-lookup"><span data-stu-id="cd315-103">Considerations for initial synchronization</span></span>

[!include [banner](../../includes/banner.md)]

[!include [rename-banner](~/includes/cc-data-platform-banner.md)]

<span data-ttu-id="cd315-104">テーブルで二重書き込みを開始する前に、最初の同期を実行して、Finance and Operations アプリと Customer Engagement アプリの両面で既存のデータを処理することができます。</span><span class="sxs-lookup"><span data-stu-id="cd315-104">Before you start dual-write on a table, you can run an initial synchronization to handle existing data on both sides: Finance and Operations apps and customer engagement apps.</span></span> <span data-ttu-id="cd315-105">2 つの環境間でデータを同期する必要がない場合は、初期同期を省略できます。</span><span class="sxs-lookup"><span data-stu-id="cd315-105">You can skip the initial synchronization if you don't have to sync data between the two environments.</span></span>

<span data-ttu-id="cd315-106">初期同期では、既存のデータを 1 つのアプリから別のアプリに双方向でコピーできます。また、実行する際には、いくつかの考慮事項があります。</span><span class="sxs-lookup"><span data-stu-id="cd315-106">The initial synchronization lets you copy existing data from one app to another bidirectionally, and there are several considerations when you run it.</span></span> <span data-ttu-id="cd315-107">たとえば、Go-Live 前にデータ移行が必要な場合があります。</span><span class="sxs-lookup"><span data-stu-id="cd315-107">For example, you might have to migrate data before your go-live.</span></span> <span data-ttu-id="cd315-108">この場合、データはデータ移行によって一方の側に読み込まれ、初期同期によってもう一方の側に同期されます。</span><span class="sxs-lookup"><span data-stu-id="cd315-108">In this case, data can be loaded into one side through data migration and then synced to the other side through the initial synchronization.</span></span>

<span data-ttu-id="cd315-109">初期同期には、次の方法を使用することをお勧めします。</span><span class="sxs-lookup"><span data-stu-id="cd315-109">We recommend that you use the following approach for the initial synchronization:</span></span>

+ <span data-ttu-id="cd315-110">**[単一スレッド テーブル](#single-threaded-entities):** まずデータを Finance and Operations アプリに移行し、次に初期同期をトリガーしてデータを Dataverse に移動します。</span><span class="sxs-lookup"><span data-stu-id="cd315-110">**[Single-threaded tables](#single-threaded-entities):** First migrate data into the Finance and Operations app, and then trigger the initial synchronization to move the data over to Dataverse.</span></span> <span data-ttu-id="cd315-111">Microsoft が実行したラボ テストによると、このシーケンスは、Dataverse から Finance and Operations アプリへの同期よりもパフォーマンスが高いです。</span><span class="sxs-lookup"><span data-stu-id="cd315-111">Based on lab testing that Microsoft has done, this sequence has better performance than synchronization from Dataverse to Finance and Operations apps.</span></span>
+ <span data-ttu-id="cd315-112">**マルチスレッド テーブル:** 最初にデータを Dataverse に移行し、次に初期同期をトリガーしてデータを Finance and Operations アプリに移動します。</span><span class="sxs-lookup"><span data-stu-id="cd315-112">**Multi-threaded tables:** First migrate data into Dataverse, and then trigger the initial synchronization to move the data over to the Finance and Operations app.</span></span>

## <a name="constraints"></a><span data-ttu-id="cd315-113">制約</span><span class="sxs-lookup"><span data-stu-id="cd315-113">Constraints</span></span>

### <a name="data-migration-slow-down-with-enabled-dual-write"></a><span data-ttu-id="cd315-114">二重書き込みの有効化によるデータ移行速度の低下</span><span class="sxs-lookup"><span data-stu-id="cd315-114">Data migration slow-down with enabled dual-write</span></span>

<span data-ttu-id="cd315-115">最初にデュアル書き込みでマップを有効にしてからデータのインポートを開始すると、移行のパフォーマンスが低下します。</span><span class="sxs-lookup"><span data-stu-id="cd315-115">If you first activate the map in dual-write and then start to import data, migration performance will be poor.</span></span> <span data-ttu-id="cd315-116">データの移行が完了するまでは、実行中のマップをデュアル書き込みで有効にしないことをお勧めします。</span><span class="sxs-lookup"><span data-stu-id="cd315-116">We recommend that you not activate running maps in dual-write until the data migration is completed.</span></span>

### <a name="limit-of-500000-rows-per-run"></a><span data-ttu-id="cd315-117">実行ごとに 500,000 の行制限</span><span class="sxs-lookup"><span data-stu-id="cd315-117">Limit of 500,000 rows per run</span></span>

<span data-ttu-id="cd315-118">初期同期によって許可される行の最大数は、1 回の実行ごとに 500,000 です。</span><span class="sxs-lookup"><span data-stu-id="cd315-118">The maximum number of rows that is allowed through initial synchronization is 500,000 per run.</span></span> <span data-ttu-id="cd315-119">各リーガル テーブルが個別に実行するため、各リーガル テーブルに 500,000 の行制限が適用されます。</span><span class="sxs-lookup"><span data-stu-id="cd315-119">The limit of 500,000 rows applies to each legal table, because each legal entity runs separately.</span></span> <span data-ttu-id="cd315-120">詳細については、[Dataverse へデータを統合](/power-platform/admin/data-integrator) を参照してください。</span><span class="sxs-lookup"><span data-stu-id="cd315-120">For more information, see [Integrate data into Dataverse](/power-platform/admin/data-integrator).</span></span> <span data-ttu-id="cd315-121">特に、「パフォーマンスを最適化し、アプリケーションに過負荷をかけないために、現在プロジェクトの実行数を 500K 行に制限しています」という通知に注意してください。</span><span class="sxs-lookup"><span data-stu-id="cd315-121">In particular, pay attention to the note that states, "To optimize performance and not overload the apps, we currently limit project executions to 500k rows per execution per project."</span></span>

<span data-ttu-id="cd315-122">初期同期時に、1 回の実行に 500,000 行以上の行が存在する場合は、データを Finance and Operations アプリと Dataverse に個別に移行し、初期同期をスキップすることをお勧めします。</span><span class="sxs-lookup"><span data-stu-id="cd315-122">If there must be more than 500,000 rows in a run when you the initial synchronization, we recommend that you migrate data into the Finance and Operations app and Dataverse separately, and skip the initial synchronization.</span></span>

### <a name="twenty-four-hour-limit"></a><span data-ttu-id="cd315-123">24 時間制限</span><span class="sxs-lookup"><span data-stu-id="cd315-123">Twenty-four-hour limit</span></span>

<span data-ttu-id="cd315-124">Dataverse から Finance and Operations アプリへの初期同期を実行している場合、24 時間以内にインポートの結果を Finance and Operations アプリから受け取る必要があります。</span><span class="sxs-lookup"><span data-stu-id="cd315-124">If you're running the initial synchronization from Dataverse to the Finance and Operations app, the import result must be received back from the Finance and Operations app within 24 hours.</span></span> <span data-ttu-id="cd315-125">そうしない場合、タイムアウトが発生します。</span><span class="sxs-lookup"><span data-stu-id="cd315-125">Otherwise, a time-out occurs.</span></span> <span data-ttu-id="cd315-126">したがって、大量のデータを同期していて、1 回の実行に 24 時間以上かかる場合、タイムアウトが原因で初期同期が失敗する可能性があります。たとえば、**顧客/アカウント** テーブルの Dataverse から Finance and Operations アプリへの初期同期には、70,000 行が含まれます。</span><span class="sxs-lookup"><span data-stu-id="cd315-126">Therefore, if you're syncing lots of data, and the single run takes more than 24 hours, the initial synchronization might fail because of a time-out. For example, an initial synchronization from Dataverse to a Finance and Operations app for the **Customer/Account** table involves 70,000 rows.</span></span> <span data-ttu-id="cd315-127">したがって、実行には 24 時間以上の時間がかかる場合があります。</span><span class="sxs-lookup"><span data-stu-id="cd315-127">Therefore, the run might take more than 24 hours and time out.</span></span>

<span data-ttu-id="cd315-128">データ量が 70,000 行を超える場合は、[単一スレッド テーブル](#single-threaded-entities) に対して Dataverse から Finance and Operations アプリへの初期同期を実行しないでください。</span><span class="sxs-lookup"><span data-stu-id="cd315-128">Don't run the initial synchronization from Dataverse to a Finance and Operations app for [single-threaded tables](#single-threaded-entities) if the data volume is more than 70,000 rows.</span></span> <span data-ttu-id="cd315-129">これらのテーブルは、インポート時にマルチスレッドをサポートしていないので、ボリュームが 70,000 行を超えると、タイムアウトが発生する可能性があります。</span><span class="sxs-lookup"><span data-stu-id="cd315-129">Because these tables don't support multi-threading during import, a time-out might occur if the volume is more 70,000 rows.</span></span> <span data-ttu-id="cd315-130">この場合、データを Finance and Operations アプリと Dataverse に別々に移行し、初期同期をスキップする必要があります。</span><span class="sxs-lookup"><span data-stu-id="cd315-130">In this situation, you should migrate data into the Finance and Operations app and Dataverse separately, and skip the initial synchronization.</span></span>

### <a name="limit-of-40-legal-entities-while-the-environments-are-being-linked"></a><span data-ttu-id="cd315-131">環境がリンクされている場合の 40 の法人制限</span><span class="sxs-lookup"><span data-stu-id="cd315-131">Limit of 40 legal entities while the environments are being linked</span></span>

<span data-ttu-id="cd315-132">現在、環境がリンクされている場合には法人は 40 までという制限があります。</span><span class="sxs-lookup"><span data-stu-id="cd315-132">Currently, there is a limit of 40 legal entities while the environments are being linked.</span></span> <span data-ttu-id="cd315-133">40 を超える法人が環境間でリンクされているマップを有効にしようとすると、次のエラー メッセージが表示されます。</span><span class="sxs-lookup"><span data-stu-id="cd315-133">If you try to enable maps where more than 40 legal entities are linked between the environments, you will receive the following error message:</span></span>

```console
Dual-write failure - Plugin registration failed: [(Unable to get partition map for project DWM-1ae35e60-4bc2-4905-88ea-XXXXX. Error Exceeds the maximum partitions allowed for mapping DWM-1ae35e60-4bc2-4905-88ea- XXXXX)], One or more errors occurred.
```

### <a name="initial-synchronization-isnt-currently-supported-for-table-maps-that-have-10-or-more-lookups"></a><span data-ttu-id="cd315-134">現在、初期同期は 10 以上のルックアップを含むテーブル マップではサポートされていません</span><span class="sxs-lookup"><span data-stu-id="cd315-134">Initial synchronization isn't currently supported for table maps that have 10 or more lookups</span></span>

<span data-ttu-id="cd315-135">この制限は、ルックアップが 10 以上あるテーブル マップの Dataverse からの初期同期にのみ適用されます。</span><span class="sxs-lookup"><span data-stu-id="cd315-135">This limitation applies only to the initial synchronization from Dataverse for table maps that have 10 or more lookups.</span></span> <span data-ttu-id="cd315-136">10 以上のルックアップを含むテーブル マップに対して初期同期を実行すると、次のエラー メッセージが表示される場合があります。</span><span class="sxs-lookup"><span data-stu-id="cd315-136">If you run the initial synchronization against a table map that has 10 or more lookups, you might receive the following error message:</span></span>

```console
5 Attempts to get data from https://XXXX.azure-apim.net/apim... Failed
```

<span data-ttu-id="cd315-137">回避策として、初期同期を次の手順に分けることができます。</span><span class="sxs-lookup"><span data-stu-id="cd315-137">As a workaround you can split the initial sync into these steps:</span></span>

1. <span data-ttu-id="cd315-138">二重書き込みテーブル マップから必須ではないルックアップ列をいくつか削除し、ルックアップの数を 10 にします。</span><span class="sxs-lookup"><span data-stu-id="cd315-138">Remove some of the lookup columns that are not mandatory from the dual-write table map and bring the number of lookups to 10.</span></span> 
2. <span data-ttu-id="cd315-139">ルックアップ列が削除されたら、マップを保存し、初期同期を行います。</span><span class="sxs-lookup"><span data-stu-id="cd315-139">After the lookup columns are removed, save the map and do the initial sync.</span></span> 
3. <span data-ttu-id="cd315-140">最初の手順の初期同期が正常に完了したら、残りのルックアップ列を追加し、最初の手順で同期されたルックアップ列を削除します。</span><span class="sxs-lookup"><span data-stu-id="cd315-140">After the initial sync for the first step is successful, add the remaining lookup columns and remove the lookup columns that were synced in first step.</span></span> <span data-ttu-id="cd315-141">ルックアップ列の数が 10 であることを再度確認します。</span><span class="sxs-lookup"><span data-stu-id="cd315-141">Once again make sure the number of lookup columns is 10.</span></span> <span data-ttu-id="cd315-142">マップを保存し、初期同期を実行します。これらの手順を繰り返して、すべてのルックアップ列が同期されていることを確認します。</span><span class="sxs-lookup"><span data-stu-id="cd315-142">Save the map and run the initial sync. Repeat these steps to make sure all the lookup columns are synced.</span></span> 
4. <span data-ttu-id="cd315-143">すべてのルックアップ列をマップに戻し、マップを保存して、初期同期をスキップしてマップを実行します。これにより、マップでライブ同期モードが有効になります。</span><span class="sxs-lookup"><span data-stu-id="cd315-143">Add all the lookup columns back to the map, save the map and run the map with skip initial sync. This will enable the map for live sync mode.</span></span>

### <a name="five-minute-limit-for-finance-and-operations-data-export"></a><span data-ttu-id="cd315-144">Finance and Operations データ エクスポートの 5 分間の制限</span><span class="sxs-lookup"><span data-stu-id="cd315-144">Five-minute limit for Finance and Operations data export</span></span>

<span data-ttu-id="cd315-145">Finance and Operations アプリから Dataverse への初期同期を実行し、Finance and Operations のデータのエクスポートに 5 分以上かかる場合、初期同期がタイムアウトすることがあります。タイムアウトは、データ テーブルに `postLoad` メソッドの仮想列がある場合、またはエクスポート クエリが最適化されていない (たとえば、インデックスが存在しない) 場合に発生する可能性があります。</span><span class="sxs-lookup"><span data-stu-id="cd315-145">If you're running the initial synchronization from the Finance and Operations app to Dataverse and the Finance and Operations data export takes more than five minutes, then the initial sync might time out. The time-out can happen if the data table has virtual columns with the `postLoad` method, or the export query isn't optimized (for example, if it has missing indexes).</span></span>

<span data-ttu-id="cd315-146">このタイプの同期は、Platform update 37 (PU37) 以降でサポートされます。</span><span class="sxs-lookup"><span data-stu-id="cd315-146">This type of synchronization is supported in Platform update 37 (PU37) and later.</span></span> <span data-ttu-id="cd315-147">したがって、Finance and Operations アプリを PU37 またはそれ以降のバージョンに更新する必要があります。</span><span class="sxs-lookup"><span data-stu-id="cd315-147">Therefore, you should update your Finance and Operations app to PU37 or later.</span></span>

### <a name="error-handling-capabilities"></a><span data-ttu-id="cd315-148">エラー処理機能</span><span class="sxs-lookup"><span data-stu-id="cd315-148">Error handling capabilities</span></span>

#### <a name="initial-synchronization-is-always-a-full-push"></a><span data-ttu-id="cd315-149">初期同期は常にフル プッシュ</span><span class="sxs-lookup"><span data-stu-id="cd315-149">Initial synchronization is always a full push</span></span>

<span data-ttu-id="cd315-150">個別の行の同期が失敗した場合は、その個別の行だけを再同期することはできません。</span><span class="sxs-lookup"><span data-stu-id="cd315-150">If an individual row fails to be synced, you can't resync only that individual row.</span></span> <span data-ttu-id="cd315-151">初期同期では、常にデータ セット全体がプッシュされます。</span><span class="sxs-lookup"><span data-stu-id="cd315-151">The initial synchronization always pushes the whole data set.</span></span> <span data-ttu-id="cd315-152">この動作は、*フル プッシュ* と呼ばれます。</span><span class="sxs-lookup"><span data-stu-id="cd315-152">This behavior is known as a *full push*.</span></span> <span data-ttu-id="cd315-153">初期同期が部分的にしか成功しなかった場合、初期同期に失敗した行だけでなく、すべての行に対して 2 回目の同期が実行されます。</span><span class="sxs-lookup"><span data-stu-id="cd315-153">If the initial synchronization only partially succeeds, a second synchronization runs for all the rows, not just the rows that failed to be synced during the initial synchronization.</span></span>

#### <a name="only-the-top-five-errors-can-be-viewed"></a><span data-ttu-id="cd315-154">上位 5 つのエラーのみ表示可能</span><span class="sxs-lookup"><span data-stu-id="cd315-154">Only the top five errors can be viewed</span></span>

<span data-ttu-id="cd315-155">初期同期のエラー ログに記録された上位 5 つのエラーのみを表示できます。</span><span class="sxs-lookup"><span data-stu-id="cd315-155">You can view only the top five errors from the initial synchronization error log.</span></span>

## <a name="known-issues"></a><span data-ttu-id="cd315-156">既知の問題</span><span class="sxs-lookup"><span data-stu-id="cd315-156">Known issues</span></span>

<span data-ttu-id="cd315-157">既知の問題の詳細については、[初期同期中の問題のトラブルシューティング](dual-write-troubleshooting-initial-sync.md)を参照してください。</span><span class="sxs-lookup"><span data-stu-id="cd315-157">For information about known issues, see [Troubleshoot issues during initial synchronization](dual-write-troubleshooting-initial-sync.md).</span></span>

## <a name="guidance-matrix"></a><span data-ttu-id="cd315-158">ガイダンス マトリックス</span><span class="sxs-lookup"><span data-stu-id="cd315-158">Guidance matrix</span></span>

<table>
<thead>
<tr>
<th><span data-ttu-id="cd315-159">Finance and Operations アプリ インスタンス</span><span class="sxs-lookup"><span data-stu-id="cd315-159">Finance and Operations app instance</span></span></th>
<th><span data-ttu-id="cd315-160">Dataverse インスタンス</span><span class="sxs-lookup"><span data-stu-id="cd315-160">Dataverse instance</span></span></th>
<th><span data-ttu-id="cd315-161">初期同期を実行するデータの有無</span><span class="sxs-lookup"><span data-stu-id="cd315-161">Has data to run the initial synchronization</span></span></th>
<th><span data-ttu-id="cd315-162">説明</span><span class="sxs-lookup"><span data-stu-id="cd315-162">Description</span></span></th>
<th><span data-ttu-id="cd315-163">テーブルの最大ボリューム</span><span class="sxs-lookup"><span data-stu-id="cd315-163">Maximum volume in a table</span></span></th>
<th><span data-ttu-id="cd315-164">単一スレッドまたはマルチスレッド</span><span class="sxs-lookup"><span data-stu-id="cd315-164">Single-threaded or multi-threaded</span></span></th>
<th><span data-ttu-id="cd315-165">アプローチ</span><span class="sxs-lookup"><span data-stu-id="cd315-165">Approach</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="cd315-166">新規</span><span class="sxs-lookup"><span data-stu-id="cd315-166">New</span></span></td>
<td><span data-ttu-id="cd315-167">新規</span><span class="sxs-lookup"><span data-stu-id="cd315-167">New</span></span></td>
<td><span data-ttu-id="cd315-168">なし</span><span class="sxs-lookup"><span data-stu-id="cd315-168">No</span></span></td>
<td><span data-ttu-id="cd315-169">Finance and Operations アプリ インスタンスと新しい Customer Engagement アプリ インスタンス。どちらのアプリにも初期データがない場合</span><span class="sxs-lookup"><span data-stu-id="cd315-169">A new Finance and Operations app instance and a new customer engagement app instance, where neither app has initial data</span></span></td>
<td><span data-ttu-id="cd315-170">適用できません</span><span class="sxs-lookup"><span data-stu-id="cd315-170">Not applicable</span></span></td>
<td><span data-ttu-id="cd315-171">任意</span><span class="sxs-lookup"><span data-stu-id="cd315-171">Any</span></span></td>
<td>
<ul>
<li><span data-ttu-id="cd315-172">二重書き込みを有効にし、初期同期をスキップします。</span><span class="sxs-lookup"><span data-stu-id="cd315-172">Activate dual-write, and skip the initial synchronization.</span></span></li>
</ul>
</td>
</tr>
<tr>
<td rowspan='3'><span data-ttu-id="cd315-173">新規</span><span class="sxs-lookup"><span data-stu-id="cd315-173">New</span></span></td>
<td rowspan='3'><span data-ttu-id="cd315-174">新規</span><span class="sxs-lookup"><span data-stu-id="cd315-174">New</span></span></td>
<td rowspan='3'><span data-ttu-id="cd315-175">あり</span><span class="sxs-lookup"><span data-stu-id="cd315-175">Yes</span></span></td>
<td rowspan='3'><span data-ttu-id="cd315-176">Finance and Operations アプリ インスタンスと新しい Customer Engagement アプリ インスタンス。どちらかのアプリに移行されたデータがある場合</span><span class="sxs-lookup"><span data-stu-id="cd315-176">A new Finance and Operations app instance and a new customer engagement app instance, where one of the apps has migrated data</span></span></td>
<td><span data-ttu-id="cd315-177">&lt;500,000</span><span class="sxs-lookup"><span data-stu-id="cd315-177">&lt; 500,000</span></span></td>
<td><span data-ttu-id="cd315-178"><a href='#single-threaded-entities'>単一スレッド</a></span><span class="sxs-lookup"><span data-stu-id="cd315-178"><a href='#single-threaded-entities'>Single-threaded</a></span></span></td>
<td>
<ol>
<li><span data-ttu-id="cd315-179">Finance and Operations アプリにデータを移行します。</span><span class="sxs-lookup"><span data-stu-id="cd315-179">Migrate data to the Finance and Operations app.</span></span></li>
<li><span data-ttu-id="cd315-180">初期同期を実行します。</span><span class="sxs-lookup"><span data-stu-id="cd315-180">Run the initial synchronization.</span></span></li>
</ol>
</td>
</tr>
<tr>
<td><span data-ttu-id="cd315-181">&lt;500,000</span><span class="sxs-lookup"><span data-stu-id="cd315-181">&lt; 500,000</span></span></td>
<td><span data-ttu-id="cd315-182">マルチスレッド</span><span class="sxs-lookup"><span data-stu-id="cd315-182">Multi-threaded</span></span></td>
<td>
<ol>
<li><span data-ttu-id="cd315-183">Dataverse にデータを移行します。</span><span class="sxs-lookup"><span data-stu-id="cd315-183">Migrate data to Dataverse.</span></span></li>
<li><span data-ttu-id="cd315-184">初期同期を実行します。</span><span class="sxs-lookup"><span data-stu-id="cd315-184">Run the initial synchronization.</span></span></li>
</ol>
</td>
</tr>
<tr>
<td><span data-ttu-id="cd315-185">&gt;500,000</span><span class="sxs-lookup"><span data-stu-id="cd315-185">&gt; 500,000</span></span></td>
<td><span data-ttu-id="cd315-186">任意</span><span class="sxs-lookup"><span data-stu-id="cd315-186">Any</span></span></td>
<td>
<ol>
<li><span data-ttu-id="cd315-187">初期同期の範囲外で、各アプリにデータを移行します。</span><span class="sxs-lookup"><span data-stu-id="cd315-187">Migrate data to each app outside the initial synchronization.</span></span></li>
<li><span data-ttu-id="cd315-188">二重書き込みを有効にし、初期同期をスキップします。</span><span class="sxs-lookup"><span data-stu-id="cd315-188">Activate dual-write, and skip the initial synchronization.</span></span></li>
</ol>
</td>
</tr>
<tr>
<td rowspan='4'><span data-ttu-id="cd315-189">新規</span><span class="sxs-lookup"><span data-stu-id="cd315-189">New</span></span></td>
<td rowspan='4'><span data-ttu-id="cd315-190">既存</span><span class="sxs-lookup"><span data-stu-id="cd315-190">Existing</span></span></td>
<td rowspan='4'><span data-ttu-id="cd315-191">あり</span><span class="sxs-lookup"><span data-stu-id="cd315-191">Yes</span></span></td>
<td rowspan='4'><span data-ttu-id="cd315-192">新しい Finance and Operations アプリ インスタンスと既存の Customer Engagement アプリ インスタンス</span><span class="sxs-lookup"><span data-stu-id="cd315-192">A new Finance and Operations app instance and an existing customer engagement app instance</span></span></td>
<td><span data-ttu-id="cd315-193">&lt;70,000</span><span class="sxs-lookup"><span data-stu-id="cd315-193">&lt; 70,000</span></span></td>
<td><span data-ttu-id="cd315-194"><a href='#single-threaded-entities'>単一スレッド</a></span><span class="sxs-lookup"><span data-stu-id="cd315-194"><a href='#single-threaded-entities'>Single-threaded</a></span></span></td>
<td>
<ol>
<li><span data-ttu-id="cd315-195">Finance and Operations アプリに新しい会社を作成します。</span><span class="sxs-lookup"><span data-stu-id="cd315-195">Create a new company in the Finance and Operations app.</span></span></li>
<li><span data-ttu-id="cd315-196">会社コードのブートストラップ Dataverse。</span><span class="sxs-lookup"><span data-stu-id="cd315-196">Bootstrap Dataverse for the company code.</span></span></li
><li><span data-ttu-id="cd315-197">初期同期を実行します。</span><span class="sxs-lookup"><span data-stu-id="cd315-197">Run the initial synchronization.</span></span></li>
</ol>
</td>
</tr>
<tr>
<td><span data-ttu-id="cd315-198">&gt;70,000</span><span class="sxs-lookup"><span data-stu-id="cd315-198">&gt; 70,000</span></span></td>
<td><span data-ttu-id="cd315-199"><a href='#single-threaded-entities'>単一スレッド</a></span><span class="sxs-lookup"><span data-stu-id="cd315-199"><a href='#single-threaded-entities'>Single-threaded</a></span></span></td>
<td>
<ol>
<li><span data-ttu-id="cd315-200">Finance and Operations アプリに新しい会社を作成します。</span><span class="sxs-lookup"><span data-stu-id="cd315-200">Create a new company in the Finance and Operations app.</span></span></li>
<li><span data-ttu-id="cd315-201">会社コードのブートストラップ Dataverse。</span><span class="sxs-lookup"><span data-stu-id="cd315-201">Bootstrap Dataverse for the company code.</span></span></li>
<li><span data-ttu-id="cd315-202">初期同期の範囲外で、各アプリにデータを移行します。</span><span class="sxs-lookup"><span data-stu-id="cd315-202">Migrate data to each app outside the initial synchronization.</span></span></li>
<li><span data-ttu-id="cd315-203">二重書き込みを有効にし、初期同期をスキップします。</span><span class="sxs-lookup"><span data-stu-id="cd315-203">Activate dual-write, and skip the initial synchronization.</span></span></li>
</ol>
</td>
</tr>
<tr>
<td><span data-ttu-id="cd315-204">&lt;500,000</span><span class="sxs-lookup"><span data-stu-id="cd315-204">&lt; 500,000</span></span></td>
<td><span data-ttu-id="cd315-205">マルチスレッド</span><span class="sxs-lookup"><span data-stu-id="cd315-205">Multi-threaded</span></span></td>
<td>
<ol>
<li><span data-ttu-id="cd315-206">Finance and Operations アプリに新しい会社を作成します。</span><span class="sxs-lookup"><span data-stu-id="cd315-206">Create a new company in the Finance and Operations app.</span></span></li>
<li><span data-ttu-id="cd315-207">会社コードのブートストラップ Dataverse。</span><span class="sxs-lookup"><span data-stu-id="cd315-207">Bootstrap Dataverse for the company code.</span></span></li>
<li><span data-ttu-id="cd315-208">初期同期を実行します。</span><span class="sxs-lookup"><span data-stu-id="cd315-208">Run the initial synchronization.</span></span></li>
</ol>
</td>
</tr>
<tr>
<td><span data-ttu-id="cd315-209">&gt;500,000</span><span class="sxs-lookup"><span data-stu-id="cd315-209">&gt; 500,000</span></span></td>
<td><span data-ttu-id="cd315-210">任意</span><span class="sxs-lookup"><span data-stu-id="cd315-210">Any</span></span></td>
<td>
<ol>
<li><span data-ttu-id="cd315-211">Finance and Operations アプリに新しい会社を作成します。</span><span class="sxs-lookup"><span data-stu-id="cd315-211">Create a new company in the Finance and Operations app.</span></span></li>
<li><span data-ttu-id="cd315-212">会社コードのブートストラップ Dataverse。</span><span class="sxs-lookup"><span data-stu-id="cd315-212">Bootstrap Dataverse for the company code.</span></span></li>
<li><span data-ttu-id="cd315-213">初期同期の範囲外で、各アプリにデータを移行します。</span><span class="sxs-lookup"><span data-stu-id="cd315-213">Migrate data to each app outside the initial synchronization.</span></span></li>
<li><span data-ttu-id="cd315-214">二重書き込みを有効にし、初期同期をスキップします。</span><span class="sxs-lookup"><span data-stu-id="cd315-214">Activate dual-write, and skip the initial synchronization.</span></span></li>
</ol>
</td>
</tr>
<tr>
<td rowspan='2'><span data-ttu-id="cd315-215">既存</span><span class="sxs-lookup"><span data-stu-id="cd315-215">Existing</span></span></td>
<td rowspan='2'><span data-ttu-id="cd315-216">新規</span><span class="sxs-lookup"><span data-stu-id="cd315-216">New</span></span></td>
<td rowspan='2'><span data-ttu-id="cd315-217">あり</span><span class="sxs-lookup"><span data-stu-id="cd315-217">Yes</span></span></td>
<td rowspan='2'><span data-ttu-id="cd315-218">既存の Finance and Operations アプリ インスタンスと新しい Customer Engagement アプリ インスタンス</span><span class="sxs-lookup"><span data-stu-id="cd315-218">An existing Finance and Operations app instance and a new customer engagement app instance</span></span></td>
<td><span data-ttu-id="cd315-219">&lt;500,000</span><span class="sxs-lookup"><span data-stu-id="cd315-219">&lt; 500,000</span></span></td>
<td><span data-ttu-id="cd315-220">任意</span><span class="sxs-lookup"><span data-stu-id="cd315-220">Any</span></span></td>
<td>
<ul>
<li><span data-ttu-id="cd315-221">初期同期を実行します。</span><span class="sxs-lookup"><span data-stu-id="cd315-221">Run the initial synchronization.</span></span></li>
</ul>
</td>
</tr>
<tr>
<td><span data-ttu-id="cd315-222">&gt;500,000</span><span class="sxs-lookup"><span data-stu-id="cd315-222">&gt; 500,000</span></span></td>
<td><span data-ttu-id="cd315-223">任意</span><span class="sxs-lookup"><span data-stu-id="cd315-223">Any</span></span></td>
<td>
<ol>
<li><span data-ttu-id="cd315-224">各アプリにデータを移行します。</span><span class="sxs-lookup"><span data-stu-id="cd315-224">Migrate data to each app.</span></span></li>
<li><span data-ttu-id="cd315-225">二重書き込みを有効にし、初期同期をスキップします。</span><span class="sxs-lookup"><span data-stu-id="cd315-225">Activate dual-write, and skip the initial synchronization.</span></span></li>
</ol>
</td>
</tr>
<tr>
<td rowspan='4'><span data-ttu-id="cd315-226">既存</span><span class="sxs-lookup"><span data-stu-id="cd315-226">Existing</span></span></td>
<td rowspan='4'><span data-ttu-id="cd315-227">既存</span><span class="sxs-lookup"><span data-stu-id="cd315-227">Existing</span></span></td>
<td rowspan='4'><span data-ttu-id="cd315-228">あり</span><span class="sxs-lookup"><span data-stu-id="cd315-228">Yes</span></span></td>
<td rowspan='4'><span data-ttu-id="cd315-229">既存の Finance and Operations アプリ インスタンスと既存の Customer Engagement アプリ インスタンス</span><span class="sxs-lookup"><span data-stu-id="cd315-229">An existing Finance and Operations app instance and an existing customer engagement app instance</span></span></td>
<td><span data-ttu-id="cd315-230">&lt;70,000</span><span class="sxs-lookup"><span data-stu-id="cd315-230">&lt; 70,000</span></span></td>
<td><span data-ttu-id="cd315-231"><a href='#single-threaded-entities'>単一スレッド</a></span><span class="sxs-lookup"><span data-stu-id="cd315-231"><a href='#single-threaded-entities'>Single-threaded</a></span></span></td>
<td>
<ol>
<li><span data-ttu-id="cd315-232">会社コードのブートストラップ Dataverse。</span><span class="sxs-lookup"><span data-stu-id="cd315-232">Bootstrap Dataverse for the company code.</span></span></li>
<li><span data-ttu-id="cd315-233">初期同期を実行します。</span><span class="sxs-lookup"><span data-stu-id="cd315-233">Run the initial synchronization.</span></span></li>
</ol>
</td>
</tr>
<tr>
<td><span data-ttu-id="cd315-234">&gt;70,000</span><span class="sxs-lookup"><span data-stu-id="cd315-234">&gt; 70,000</span></span></td>
<td><span data-ttu-id="cd315-235"><a href='#single-threaded-entities'>単一スレッド</a></span><span class="sxs-lookup"><span data-stu-id="cd315-235"><a href='#single-threaded-entities'>Single-threaded</a></span></span></td>
<td>
<ol>
<li><span data-ttu-id="cd315-236">会社コードのブートストラップ Dataverse。</span><span class="sxs-lookup"><span data-stu-id="cd315-236">Bootstrap Dataverse for the company code.</span></span></li>
<li><span data-ttu-id="cd315-237">初期同期の範囲外で、各アプリにデータを移行します。</span><span class="sxs-lookup"><span data-stu-id="cd315-237">Migrate data to each app outside the initial synchronization.</span></span></li>
<li><span data-ttu-id="cd315-238">二重書き込みを有効にし、初期同期をスキップします。</span><span class="sxs-lookup"><span data-stu-id="cd315-238">Activate dual-write, and skip the initial synchronization.</span></span></li>
</ol>
</td>
</tr>
<tr>
<td><span data-ttu-id="cd315-239">&lt;500,000</span><span class="sxs-lookup"><span data-stu-id="cd315-239">&lt; 500,000</span></span></td>
<td><span data-ttu-id="cd315-240">マルチスレッド</span><span class="sxs-lookup"><span data-stu-id="cd315-240">Multi-threaded</span></span></td>
<td>
<ol>
<li><span data-ttu-id="cd315-241">会社コードのブートストラップ Dataverse。</span><span class="sxs-lookup"><span data-stu-id="cd315-241">Bootstrap Dataverse for the company code.</span></span></li>
<li><span data-ttu-id="cd315-242">初期同期を実行します。</span><span class="sxs-lookup"><span data-stu-id="cd315-242">Run the initial synchronization.</span></span></li>
</ol>
</td>
</tr>
<tr>
<td><span data-ttu-id="cd315-243">&gt;500,000</span><span class="sxs-lookup"><span data-stu-id="cd315-243">&gt; 500,000</span></span></td>
<td><span data-ttu-id="cd315-244">任意</span><span class="sxs-lookup"><span data-stu-id="cd315-244">Any</span></span></td>
<td>
<ol>
<li><span data-ttu-id="cd315-245">会社コードのブートストラップ Dataverse。</span><span class="sxs-lookup"><span data-stu-id="cd315-245">Bootstrap Dataverse for the company code.</span></span></li>
<li><span data-ttu-id="cd315-246">初期同期の範囲外で、各アプリにデータを移行します。</span><span class="sxs-lookup"><span data-stu-id="cd315-246">Migrate data to each app outside the initial synchronization.</span></span></li>
<li><span data-ttu-id="cd315-247">二重書き込みを有効にし、初期同期をスキップします。</span><span class="sxs-lookup"><span data-stu-id="cd315-247">Activate dual-write, and skip the initial synchronization.</span></span></li>
</ol>
</td>
</tr>
</tbody>
</table>

## <a name="single-threaded-tables"></a><a id="single-threaded-entities"></a><span data-ttu-id="cd315-248">単一スレッド テーブル</span><span class="sxs-lookup"><span data-stu-id="cd315-248">Single-threaded tables</span></span>

- <span data-ttu-id="cd315-249">消費税コード (msdyn\_taxcodes)</span><span class="sxs-lookup"><span data-stu-id="cd315-249">Sales tax codes (msdyn\_taxcodes)</span></span>
- <span data-ttu-id="cd315-250">顧客 V3 (アカウント)</span><span class="sxs-lookup"><span data-stu-id="cd315-250">Customers V3 (accounts)</span></span>
- <span data-ttu-id="cd315-251">仕入先 V2 (msdyn\_vendors)</span><span class="sxs-lookup"><span data-stu-id="cd315-251">Vendors V2 (msdyn\_vendors)</span></span>
- <span data-ttu-id="cd315-252">倉庫 (msdyn\_warehouses)</span><span class="sxs-lookup"><span data-stu-id="cd315-252">Warehouses (msdyn\_warehouses)</span></span>
- <span data-ttu-id="cd315-253">製品カテゴリ (msdyn\_productcategories)</span><span class="sxs-lookup"><span data-stu-id="cd315-253">Product categories (msdyn\_productcategories)</span></span>
- <span data-ttu-id="cd315-254">雇用 (cdm\_employments)</span><span class="sxs-lookup"><span data-stu-id="cd315-254">Employment (cdm\_employments)</span></span>
- <span data-ttu-id="cd315-255">職位作業者割り当て (cdm\_positionworkerassignmentmaps)</span><span class="sxs-lookup"><span data-stu-id="cd315-255">Position worker assignments (cdm\_positionworkerassignmentmaps)</span></span>
- <span data-ttu-id="cd315-256">倉庫の場所 (msdyn\_inventorylocations)</span><span class="sxs-lookup"><span data-stu-id="cd315-256">Warehouse locations (msdyn\_inventorylocations)</span></span>
- <span data-ttu-id="cd315-257">配送モード (msdyn\_shipvias)</span><span class="sxs-lookup"><span data-stu-id="cd315-257">Modes of delivery (msdyn\_shipvias)</span></span>


[!INCLUDE[footer-include](../../../../includes/footer-banner.md)]