---
title: 初期同期に関する考慮事項
description: このトピックでは、制約、既知の問題、およびデュアル書き込みの初期同期に関するガイダンスについて説明します。
author: RamaKrishnamoorthy
manager: AnnBe
ms.date: 10/12/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
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
ms.openlocfilehash: 7a4336dcc94fd3db8a21bda11d7f25c94ca144cf
ms.sourcegitcommit: 659375c4cc7f5524cbf91cf6160f6a410960ac16
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 12/05/2020
ms.locfileid: "4687330"
---
# <a name="considerations-for-initial-synchronization"></a><span data-ttu-id="d97ea-103">初期同期に関する考慮事項</span><span class="sxs-lookup"><span data-stu-id="d97ea-103">Considerations for initial synchronization</span></span>

[!include [banner](../../includes/banner.md)]

[!include [rename-banner](~/includes/cc-data-platform-banner.md)]

<span data-ttu-id="d97ea-104">エンティティでデュアル書き込みを開始する前に、最初の同期を実行して、Finance and Operations アプリと Customer Engagement アプリの両面で既存のデータを処理することができます。</span><span class="sxs-lookup"><span data-stu-id="d97ea-104">Before you start dual-write on an entity, you can run an initial synchronization to handle existing data on both sides: Finance and Operations apps and customer engagement apps.</span></span> <span data-ttu-id="d97ea-105">2 つの環境間でデータを同期する必要がない場合は、初期同期を省略できます。</span><span class="sxs-lookup"><span data-stu-id="d97ea-105">You can skip the initial synchronization if you don't have to sync data between the two environments.</span></span>

<span data-ttu-id="d97ea-106">初期同期では、既存のデータを 1 つのアプリから別のアプリに双方向でコピーできます。また、実行する際には、いくつかの考慮事項があります。</span><span class="sxs-lookup"><span data-stu-id="d97ea-106">The initial synchronization lets you copy existing data from one app to another bidirectionally, and there are several considerations when you run it.</span></span> <span data-ttu-id="d97ea-107">たとえば、Go-Live 前にデータ移行が必要な場合があります。</span><span class="sxs-lookup"><span data-stu-id="d97ea-107">For example, you might have to migrate data before your go-live.</span></span> <span data-ttu-id="d97ea-108">この場合、データはデータ移行によって一方の側に読み込まれ、初期同期によってもう一方の側に同期されます。</span><span class="sxs-lookup"><span data-stu-id="d97ea-108">In this case, data can be loaded into one side through data migration and then synced to the other side through the initial synchronization.</span></span>

<span data-ttu-id="d97ea-109">初期同期には、次の方法を使用することをお勧めします。</span><span class="sxs-lookup"><span data-stu-id="d97ea-109">We recommend that you use the following approach for the initial synchronization:</span></span>

+ <span data-ttu-id="d97ea-110">**[単一スレッド テーブル](#single-threaded-entities):** まずデータを Finance and Operations アプリに移行し、次に初期同期をトリガーしてデータを Dataverse に移動します。</span><span class="sxs-lookup"><span data-stu-id="d97ea-110">**[Single-threaded tables](#single-threaded-entities):** First migrate data into the Finance and Operations app, and then trigger the initial synchronization to move the data over to Dataverse.</span></span> <span data-ttu-id="d97ea-111">Microsoft が実行したラボ テストによると、このシーケンスは、Dataverse から Finance and Operations アプリへの同期よりもパフォーマンスが高いです。</span><span class="sxs-lookup"><span data-stu-id="d97ea-111">Based on lab testing that Microsoft has done, this sequence has better performance than synchronization from Dataverse to Finance and Operations apps.</span></span>
+ <span data-ttu-id="d97ea-112">**マルチスレッド テーブル:** 最初にデータを Dataverse に移行し、次に初期同期をトリガーしてデータを Finance and Operations アプリに移動します。</span><span class="sxs-lookup"><span data-stu-id="d97ea-112">**Multi-threaded tables:** First migrate data into Dataverse, and then trigger the initial synchronization to move the data over to the Finance and Operations app.</span></span>

## <a name="constraints"></a><span data-ttu-id="d97ea-113">制約</span><span class="sxs-lookup"><span data-stu-id="d97ea-113">Constraints</span></span>

### <a name="data-migration-slow-down-with-enabled-dual-write"></a><span data-ttu-id="d97ea-114">二重書き込みの有効化によるデータ移行速度の低下</span><span class="sxs-lookup"><span data-stu-id="d97ea-114">Data migration slow-down with enabled dual-write</span></span>

<span data-ttu-id="d97ea-115">最初にデュアル書き込みでマップを有効にしてからデータのインポートを開始すると、移行のパフォーマンスが低下します。</span><span class="sxs-lookup"><span data-stu-id="d97ea-115">If you first activate the map in dual-write and then start to import data, migration performance will be poor.</span></span> <span data-ttu-id="d97ea-116">データの移行が完了するまでは、実行中のマップをデュアル書き込みで有効にしないことをお勧めします。</span><span class="sxs-lookup"><span data-stu-id="d97ea-116">We recommend that you not activate running maps in dual-write until the data migration is completed.</span></span>

### <a name="limit-of-500000-records-per-run"></a><span data-ttu-id="d97ea-117">実行ごとに 500,000 のレコード制限</span><span class="sxs-lookup"><span data-stu-id="d97ea-117">Limit of 500,000 records per run</span></span>

<span data-ttu-id="d97ea-118">初期同期によって許可されるレコードの最大数は、1 つの実行ごとに 500,000 です。</span><span class="sxs-lookup"><span data-stu-id="d97ea-118">The maximum number of records that is allowed through initial synchronization is 500,000 per run.</span></span> <span data-ttu-id="d97ea-119">各法人が個別に実行するため、各法人に 500,000 のレコード制限が適用されます。</span><span class="sxs-lookup"><span data-stu-id="d97ea-119">The limit of 500,000 records applies to each legal entity, because each legal entity runs separately.</span></span> <span data-ttu-id="d97ea-120">詳細については、[Dataverse へデータを統合](https://docs.microsoft.com/power-platform/admin/data-integrator) を参照してください。</span><span class="sxs-lookup"><span data-stu-id="d97ea-120">For more information, see [Integrate data into Dataverse](https://docs.microsoft.com/power-platform/admin/data-integrator).</span></span> <span data-ttu-id="d97ea-121">特に、「パフォーマンスを最適化し、アプリケーションに過負荷をかけないために、現在プロジェクトの実行数を 500K 行に制限しています」という通知に注意してください。</span><span class="sxs-lookup"><span data-stu-id="d97ea-121">In particular, pay attention to the note that states, "To optimize performance and not overload the apps, we currently limit project executions to 500k rows per execution per project."</span></span>

<span data-ttu-id="d97ea-122">初期同期時に、1 回の実行に 500,000 レコード以上のレコードが存在する場合は、データを Finance and Operations アプリと Dataverse に個別に移行し、初期同期をスキップすることをお勧めします。</span><span class="sxs-lookup"><span data-stu-id="d97ea-122">If there must be more than 500,000 records in a run when you the initial synchronization, we recommend that you migrate data into the Finance and Operations app and Dataverse separately, and skip the initial synchronization.</span></span>

### <a name="twenty-four-hour-limit"></a><span data-ttu-id="d97ea-123">24 時間制限</span><span class="sxs-lookup"><span data-stu-id="d97ea-123">Twenty-four-hour limit</span></span>

<span data-ttu-id="d97ea-124">Dataverse から Finance and Operations アプリへの初期同期を実行している場合、24 時間以内にインポートの結果を Finance and Operations アプリから受け取る必要があります。</span><span class="sxs-lookup"><span data-stu-id="d97ea-124">If you're running the initial synchronization from Dataverse to the Finance and Operations app, the import result must be received back from the Finance and Operations app within 24 hours.</span></span> <span data-ttu-id="d97ea-125">そうしない場合、タイムアウトが発生します。</span><span class="sxs-lookup"><span data-stu-id="d97ea-125">Otherwise, a time-out occurs.</span></span> <span data-ttu-id="d97ea-126">したがって、大量のデータを同期していて、1 回の実行に 24 時間以上かかる場合、タイムアウトが原因で初期同期が失敗する可能性があります。たとえば、**顧客/アカウント** エンティティの Dataverse から Finance and Operations アプリへの初期同期には、70,000 レコードが含まれます。</span><span class="sxs-lookup"><span data-stu-id="d97ea-126">Therefore, if you're syncing lots of data, and the single run takes more than 24 hours, the initial synchronization might fail because of a time-out. For example, an initial synchronization from Dataverse to a Finance and Operations app for the **Customer/Account** entity involves 70,000 records.</span></span> <span data-ttu-id="d97ea-127">したがって、実行には 24 時間以上の時間がかかる場合があります。</span><span class="sxs-lookup"><span data-stu-id="d97ea-127">Therefore, the run might take more than 24 hours and time out.</span></span>

<span data-ttu-id="d97ea-128">データ量が 70,000 レコードを超える場合は、[単一スレッド テーブル](#single-threaded-entities)に対して Dataverse から Finance and Operations アプリへの初期同期を実行しないでください。</span><span class="sxs-lookup"><span data-stu-id="d97ea-128">Don't run the initial synchronization from Dataverse to a Finance and Operations app for [single-threaded tables](#single-threaded-entities) if the data volume is more than 70,000 records.</span></span> <span data-ttu-id="d97ea-129">これらのテーブルは、インポート時にマルチスレッドをサポートしていないので、ボリュームが 70,000 レコードを超えると、タイムアウトが発生する可能性があります。</span><span class="sxs-lookup"><span data-stu-id="d97ea-129">Because these tables don't support multi-threading during import, a time-out might occur if the volume is more 70,000 records.</span></span> <span data-ttu-id="d97ea-130">この場合、データを Finance and Operations アプリと Dataverse に別々に移行し、初期同期をスキップする必要があります。</span><span class="sxs-lookup"><span data-stu-id="d97ea-130">In this situation, you should migrate data into the Finance and Operations app and Dataverse separately, and skip the initial synchronization.</span></span>

### <a name="limit-of-40-legal-entities-while-the-environments-are-being-linked"></a><span data-ttu-id="d97ea-131">環境がリンクされている場合の 40 の法人制限</span><span class="sxs-lookup"><span data-stu-id="d97ea-131">Limit of 40 legal entities while the environments are being linked</span></span>

<span data-ttu-id="d97ea-132">現在、環境がリンクされている場合には法人は 40 までという制限があります。</span><span class="sxs-lookup"><span data-stu-id="d97ea-132">Currently, there is a limit of 40 legal entities while the environments are being linked.</span></span> <span data-ttu-id="d97ea-133">40 を超える法人が環境間でリンクされているマップを有効にしようとすると、次のエラー メッセージが表示されます。</span><span class="sxs-lookup"><span data-stu-id="d97ea-133">If you try to enable maps where more than 40 legal entities are linked between the environments, you will receive the following error message:</span></span>

```console
Dual-write failure - Plugin registration failed: [(Unable to get partition map for project DWM-1ae35e60-4bc2-4905-88ea-XXXXX. Error Exceeds the maximum partitions allowed for mapping DWM-1ae35e60-4bc2-4905-88ea- XXXXX)], One or more errors occurred.
```

### <a name="initial-synchronization-isnt-currently-supported-for-table-maps-that-have-10-or-more-lookups"></a><span data-ttu-id="d97ea-134">現在、初期同期は 10 以上のルックアップを含むテーブル マップではサポートされていません</span><span class="sxs-lookup"><span data-stu-id="d97ea-134">Initial synchronization isn't currently supported for table maps that have 10 or more lookups</span></span>

<span data-ttu-id="d97ea-135">この制限は、ルックアップが 10 以上あるテーブル マップの Dataverse からの初期同期にのみ適用されます。</span><span class="sxs-lookup"><span data-stu-id="d97ea-135">This limitation applies only to the initial synchronization from Dataverse for table maps that have 10 or more lookups.</span></span> <span data-ttu-id="d97ea-136">10 以上のルックアップを含むテーブル マップに対して初期同期を実行すると、次のエラー メッセージが表示される場合があります。</span><span class="sxs-lookup"><span data-stu-id="d97ea-136">If you run the initial synchronization against an table map that has 10 or more lookups, you might receive the following error message:</span></span>

```console
5 Attempts to get data from https://XXXX.azure-apim.net/apim... Failed
```

<span data-ttu-id="d97ea-137">回避策として、初期同期を次の手順に分けることができます。</span><span class="sxs-lookup"><span data-stu-id="d97ea-137">As a workaround you can split the initial sync into these steps:</span></span>

1. <span data-ttu-id="d97ea-138">二重書き込みテーブル マップから必須ではないルックアップ フィールドをいくつか削除し、ルックアップの数を 10 にします。</span><span class="sxs-lookup"><span data-stu-id="d97ea-138">Remove some of the lookup fields that are not mandatory from the dual-write table map and bring the number of lookups to 10.</span></span> 
2. <span data-ttu-id="d97ea-139">ルックアップ フィールドが削除されたら、マップを保存し、初期同期を行います。</span><span class="sxs-lookup"><span data-stu-id="d97ea-139">After the lookup fields are removed, save the map and do the initial sync.</span></span> 
3. <span data-ttu-id="d97ea-140">最初の手順の初期同期が正常に完了したら、残りのルックアップ フィールドを追加し、最初の手順で同期されたルックアップ フィールドを削除します。</span><span class="sxs-lookup"><span data-stu-id="d97ea-140">After the initial sync for the first step is successful, add the remaining lookup fields and remove the lookup fields that were synced in first step.</span></span> <span data-ttu-id="d97ea-141">ルックアップ フィールドの数が 10 であることを再度確認します。</span><span class="sxs-lookup"><span data-stu-id="d97ea-141">Once again make sure the number of lookup fields is 10.</span></span> <span data-ttu-id="d97ea-142">マップを保存し、初期同期を実行します。これらの手順を繰り返して、すべてのルックアップ フィールドが同期されていることを確認します。</span><span class="sxs-lookup"><span data-stu-id="d97ea-142">Save the map and run the initial sync. Repeat these steps to make sure all the lookup fields are synced.</span></span> 
4. <span data-ttu-id="d97ea-143">すべてのルックアップ フィールドをマップに戻し、マップを保存して、初期同期をスキップしてマップを実行します。これにより、マップでライブ同期モードが有効になります。</span><span class="sxs-lookup"><span data-stu-id="d97ea-143">Add all the lookup fields back to the map, save the map and run the map with skip initial sync. This will enable the map for live sync mode.</span></span>

### <a name="five-minute-limit-for-finance-and-operations-data-export"></a><span data-ttu-id="d97ea-144">Finance and Operations データ エクスポートの 5 分間の制限</span><span class="sxs-lookup"><span data-stu-id="d97ea-144">Five-minute limit for Finance and Operations data export</span></span>

<span data-ttu-id="d97ea-145">Finance and Operations アプリから Dataverse への初期同期を実行し、Finance and Operations のデータのエクスポートに 5 分以上かかる場合、初期同期がタイムアウトすることがあります。タイムアウトは、データ エンティティに `postLoad` メソッドの仮想フィールドがある場合、またはエクスポート クエリが最適化されていない (たとえば、インデックスが存在しない) 場合に発生する可能性があります。</span><span class="sxs-lookup"><span data-stu-id="d97ea-145">If you're running the initial synchronization from the Finance and Operations app to Dataverse and the Finance and Operations data export takes more than five minutes, then the initial sync might time out. The time-out can happen if the data entity has virtual fields with the `postLoad` method, or the export query isn't optimized (for example, if it has missing indexes).</span></span>

<span data-ttu-id="d97ea-146">このタイプの同期は、Platform update 37 (PU37) 以降でサポートされます。</span><span class="sxs-lookup"><span data-stu-id="d97ea-146">This type of synchronization is supported in Platform update 37 (PU37) and later.</span></span> <span data-ttu-id="d97ea-147">したがって、Finance and Operations アプリを PU37 またはそれ以降のバージョンに更新する必要があります。</span><span class="sxs-lookup"><span data-stu-id="d97ea-147">Therefore, you should update your Finance and Operations app to PU37 or later.</span></span>

### <a name="error-handling-capabilities"></a><span data-ttu-id="d97ea-148">エラー処理機能</span><span class="sxs-lookup"><span data-stu-id="d97ea-148">Error handling capabilities</span></span>

#### <a name="initial-synchronization-is-always-a-full-push"></a><span data-ttu-id="d97ea-149">初期同期は常にフル プッシュ</span><span class="sxs-lookup"><span data-stu-id="d97ea-149">Initial synchronization is always a full push</span></span>

<span data-ttu-id="d97ea-150">個別のレコードの同期が失敗した場合は、その個別のレコードだけを再同期することはできません。</span><span class="sxs-lookup"><span data-stu-id="d97ea-150">If an individual record fails to be synced, you can't resync only that individual record.</span></span> <span data-ttu-id="d97ea-151">初期同期では、常にデータ セット全体がプッシュされます。</span><span class="sxs-lookup"><span data-stu-id="d97ea-151">The initial synchronization always pushes the whole data set.</span></span> <span data-ttu-id="d97ea-152">この動作は、*フル プッシュ* と呼ばれます。</span><span class="sxs-lookup"><span data-stu-id="d97ea-152">This behavior is known as a *full push*.</span></span> <span data-ttu-id="d97ea-153">初期同期が部分的にしか成功しなかった場合、初期同期に失敗したレコードだけでなく、すべてのレコードに対して 2 回目の同期が実行されます。</span><span class="sxs-lookup"><span data-stu-id="d97ea-153">If the initial synchronization only partially succeeds, a second synchronization runs for all the records, not just the records that failed to be synced during the initial synchronization.</span></span>

#### <a name="only-the-top-five-errors-can-be-viewed"></a><span data-ttu-id="d97ea-154">上位 5 つのエラーのみ表示可能</span><span class="sxs-lookup"><span data-stu-id="d97ea-154">Only the top five errors can be viewed</span></span>

<span data-ttu-id="d97ea-155">初期同期のエラー ログに記録された上位 5 つのエラーのみを表示できます。</span><span class="sxs-lookup"><span data-stu-id="d97ea-155">You can view only the top five errors from the initial synchronization error log.</span></span>

## <a name="known-issues"></a><span data-ttu-id="d97ea-156">既知の問題</span><span class="sxs-lookup"><span data-stu-id="d97ea-156">Known issues</span></span>

<span data-ttu-id="d97ea-157">既知の問題の詳細については、[初期同期中の問題のトラブルシューティング](dual-write-troubleshooting-initial-sync.md)を参照してください。</span><span class="sxs-lookup"><span data-stu-id="d97ea-157">For information about known issues, see [Troubleshoot issues during initial synchronization](dual-write-troubleshooting-initial-sync.md).</span></span>

## <a name="guidance-matrix"></a><span data-ttu-id="d97ea-158">ガイダンス マトリックス</span><span class="sxs-lookup"><span data-stu-id="d97ea-158">Guidance matrix</span></span>

<table>
<thead>
<tr>
<th><span data-ttu-id="d97ea-159">Finance and Operations アプリ インスタンス</span><span class="sxs-lookup"><span data-stu-id="d97ea-159">Finance and Operations app instance</span></span></th>
<th><span data-ttu-id="d97ea-160">Dataverse インスタンス</span><span class="sxs-lookup"><span data-stu-id="d97ea-160">Dataverse instance</span></span></th>
<th><span data-ttu-id="d97ea-161">初期同期を実行するデータの有無</span><span class="sxs-lookup"><span data-stu-id="d97ea-161">Has data to run the initial synchronization</span></span></th>
<th><span data-ttu-id="d97ea-162">説明</span><span class="sxs-lookup"><span data-stu-id="d97ea-162">Description</span></span></th>
<th><span data-ttu-id="d97ea-163">エンティティの最大ボリューム</span><span class="sxs-lookup"><span data-stu-id="d97ea-163">Maximum volume in an entity</span></span></th>
<th><span data-ttu-id="d97ea-164">単一スレッドまたはマルチスレッド</span><span class="sxs-lookup"><span data-stu-id="d97ea-164">Single-threaded or multi-threaded</span></span></th>
<th><span data-ttu-id="d97ea-165">アプローチ</span><span class="sxs-lookup"><span data-stu-id="d97ea-165">Approach</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="d97ea-166">新規</span><span class="sxs-lookup"><span data-stu-id="d97ea-166">New</span></span></td>
<td><span data-ttu-id="d97ea-167">新規</span><span class="sxs-lookup"><span data-stu-id="d97ea-167">New</span></span></td>
<td><span data-ttu-id="d97ea-168">なし</span><span class="sxs-lookup"><span data-stu-id="d97ea-168">No</span></span></td>
<td><span data-ttu-id="d97ea-169">Finance and Operations アプリ インスタンスと新しい Customer Engagement アプリ インスタンス。どちらのアプリにも初期データがない場合</span><span class="sxs-lookup"><span data-stu-id="d97ea-169">A new Finance and Operations app instance and a new customer engagement app instance, where neither app has initial data</span></span></td>
<td><span data-ttu-id="d97ea-170">適用できません</span><span class="sxs-lookup"><span data-stu-id="d97ea-170">Not applicable</span></span></td>
<td><span data-ttu-id="d97ea-171">任意</span><span class="sxs-lookup"><span data-stu-id="d97ea-171">Any</span></span></td>
<td>
<ul>
<li><span data-ttu-id="d97ea-172">二重書き込みを有効にし、初期同期をスキップします。</span><span class="sxs-lookup"><span data-stu-id="d97ea-172">Activate dual-write, and skip the initial synchronization.</span></span></li>
</ul>
</td>
</tr>
<tr>
<td rowspan='3'><span data-ttu-id="d97ea-173">新規</span><span class="sxs-lookup"><span data-stu-id="d97ea-173">New</span></span></td>
<td rowspan='3'><span data-ttu-id="d97ea-174">新規</span><span class="sxs-lookup"><span data-stu-id="d97ea-174">New</span></span></td>
<td rowspan='3'><span data-ttu-id="d97ea-175">あり</span><span class="sxs-lookup"><span data-stu-id="d97ea-175">Yes</span></span></td>
<td rowspan='3'><span data-ttu-id="d97ea-176">Finance and Operations アプリ インスタンスと新しい Customer Engagement アプリ インスタンス。どちらかのアプリに移行されたデータがある場合</span><span class="sxs-lookup"><span data-stu-id="d97ea-176">A new Finance and Operations app instance and a new customer engagement app instance, where one of the apps has migrated data</span></span></td>
<td><span data-ttu-id="d97ea-177">&lt;500,000</span><span class="sxs-lookup"><span data-stu-id="d97ea-177">&lt; 500,000</span></span></td>
<td><span data-ttu-id="d97ea-178"><a href='#single-threaded-entities'>単一スレッド</a></span><span class="sxs-lookup"><span data-stu-id="d97ea-178"><a href='#single-threaded-entities'>Single-threaded</a></span></span></td>
<td>
<ol>
<li><span data-ttu-id="d97ea-179">Finance and Operations アプリにデータを移行します。</span><span class="sxs-lookup"><span data-stu-id="d97ea-179">Migrate data to the Finance and Operations app.</span></span></li>
<li><span data-ttu-id="d97ea-180">初期同期を実行します。</span><span class="sxs-lookup"><span data-stu-id="d97ea-180">Run the initial synchronization.</span></span></li>
</ol>
</td>
</tr>
<tr>
<td><span data-ttu-id="d97ea-181">&lt;500,000</span><span class="sxs-lookup"><span data-stu-id="d97ea-181">&lt; 500,000</span></span></td>
<td><span data-ttu-id="d97ea-182">マルチスレッド</span><span class="sxs-lookup"><span data-stu-id="d97ea-182">Multi-threaded</span></span></td>
<td>
<ol>
<li><span data-ttu-id="d97ea-183">Dataverse にデータを移行します。</span><span class="sxs-lookup"><span data-stu-id="d97ea-183">Migrate data to Dataverse.</span></span></li>
<li><span data-ttu-id="d97ea-184">初期同期を実行します。</span><span class="sxs-lookup"><span data-stu-id="d97ea-184">Run the initial synchronization.</span></span></li>
</ol>
</td>
</tr>
<tr>
<td><span data-ttu-id="d97ea-185">&gt;500,000</span><span class="sxs-lookup"><span data-stu-id="d97ea-185">&gt; 500,000</span></span></td>
<td><span data-ttu-id="d97ea-186">任意</span><span class="sxs-lookup"><span data-stu-id="d97ea-186">Any</span></span></td>
<td>
<ol>
<li><span data-ttu-id="d97ea-187">初期同期の範囲外で、各アプリにデータを移行します。</span><span class="sxs-lookup"><span data-stu-id="d97ea-187">Migrate data to each app outside the initial synchronization.</span></span></li>
<li><span data-ttu-id="d97ea-188">二重書き込みを有効にし、初期同期をスキップします。</span><span class="sxs-lookup"><span data-stu-id="d97ea-188">Activate dual-write, and skip the initial synchronization.</span></span></li>
</ol>
</td>
</tr>
<tr>
<td rowspan='4'><span data-ttu-id="d97ea-189">新規</span><span class="sxs-lookup"><span data-stu-id="d97ea-189">New</span></span></td>
<td rowspan='4'><span data-ttu-id="d97ea-190">既存</span><span class="sxs-lookup"><span data-stu-id="d97ea-190">Existing</span></span></td>
<td rowspan='4'><span data-ttu-id="d97ea-191">あり</span><span class="sxs-lookup"><span data-stu-id="d97ea-191">Yes</span></span></td>
<td rowspan='4'><span data-ttu-id="d97ea-192">新しい Finance and Operations アプリ インスタンスと既存の Customer Engagement アプリ インスタンス</span><span class="sxs-lookup"><span data-stu-id="d97ea-192">A new Finance and Operations app instance and an existing customer engagement app instance</span></span></td>
<td><span data-ttu-id="d97ea-193">&lt;70,000</span><span class="sxs-lookup"><span data-stu-id="d97ea-193">&lt; 70,000</span></span></td>
<td><span data-ttu-id="d97ea-194"><a href='#single-threaded-entities'>単一スレッド</a></span><span class="sxs-lookup"><span data-stu-id="d97ea-194"><a href='#single-threaded-entities'>Single-threaded</a></span></span></td>
<td>
<ol>
<li><span data-ttu-id="d97ea-195">Finance and Operations アプリに新しい会社を作成します。</span><span class="sxs-lookup"><span data-stu-id="d97ea-195">Create a new company in the Finance and Operations app.</span></span></li>
<li><span data-ttu-id="d97ea-196">会社コードのブートストラップ Dataverse。</span><span class="sxs-lookup"><span data-stu-id="d97ea-196">Bootstrap Dataverse for the company code.</span></span></li
><li><span data-ttu-id="d97ea-197">初期同期を実行します。</span><span class="sxs-lookup"><span data-stu-id="d97ea-197">Run the initial synchronization.</span></span></li>
</ol>
</td>
</tr>
<tr>
<td><span data-ttu-id="d97ea-198">&gt;70,000</span><span class="sxs-lookup"><span data-stu-id="d97ea-198">&gt; 70,000</span></span></td>
<td><span data-ttu-id="d97ea-199"><a href='#single-threaded-entities'>単一スレッド</a></span><span class="sxs-lookup"><span data-stu-id="d97ea-199"><a href='#single-threaded-entities'>Single-threaded</a></span></span></td>
<td>
<ol>
<li><span data-ttu-id="d97ea-200">Finance and Operations アプリに新しい会社を作成します。</span><span class="sxs-lookup"><span data-stu-id="d97ea-200">Create a new company in the Finance and Operations app.</span></span></li>
<li><span data-ttu-id="d97ea-201">会社コードのブートストラップ Dataverse。</span><span class="sxs-lookup"><span data-stu-id="d97ea-201">Bootstrap Dataverse for the company code.</span></span></li>
<li><span data-ttu-id="d97ea-202">初期同期の範囲外で、各アプリにデータを移行します。</span><span class="sxs-lookup"><span data-stu-id="d97ea-202">Migrate data to each app outside the initial synchronization.</span></span></li>
<li><span data-ttu-id="d97ea-203">二重書き込みを有効にし、初期同期をスキップします。</span><span class="sxs-lookup"><span data-stu-id="d97ea-203">Activate dual-write, and skip the initial synchronization.</span></span></li>
</ol>
</td>
</tr>
<tr>
<td><span data-ttu-id="d97ea-204">&lt;500,000</span><span class="sxs-lookup"><span data-stu-id="d97ea-204">&lt; 500,000</span></span></td>
<td><span data-ttu-id="d97ea-205">マルチスレッド</span><span class="sxs-lookup"><span data-stu-id="d97ea-205">Multi-threaded</span></span></td>
<td>
<ol>
<li><span data-ttu-id="d97ea-206">Finance and Operations アプリに新しい会社を作成します。</span><span class="sxs-lookup"><span data-stu-id="d97ea-206">Create a new company in the Finance and Operations app.</span></span></li>
<li><span data-ttu-id="d97ea-207">会社コードのブートストラップ Dataverse。</span><span class="sxs-lookup"><span data-stu-id="d97ea-207">Bootstrap Dataverse for the company code.</span></span></li>
<li><span data-ttu-id="d97ea-208">初期同期を実行します。</span><span class="sxs-lookup"><span data-stu-id="d97ea-208">Run the initial synchronization.</span></span></li>
</ol>
</td>
</tr>
<tr>
<td><span data-ttu-id="d97ea-209">&gt;500,000</span><span class="sxs-lookup"><span data-stu-id="d97ea-209">&gt; 500,000</span></span></td>
<td><span data-ttu-id="d97ea-210">任意</span><span class="sxs-lookup"><span data-stu-id="d97ea-210">Any</span></span></td>
<td>
<ol>
<li><span data-ttu-id="d97ea-211">Finance and Operations アプリに新しい会社を作成します。</span><span class="sxs-lookup"><span data-stu-id="d97ea-211">Create a new company in the Finance and Operations app.</span></span></li>
<li><span data-ttu-id="d97ea-212">会社コードのブートストラップ Dataverse。</span><span class="sxs-lookup"><span data-stu-id="d97ea-212">Bootstrap Dataverse for the company code.</span></span></li>
<li><span data-ttu-id="d97ea-213">初期同期の範囲外で、各アプリにデータを移行します。</span><span class="sxs-lookup"><span data-stu-id="d97ea-213">Migrate data to each app outside the initial synchronization.</span></span></li>
<li><span data-ttu-id="d97ea-214">二重書き込みを有効にし、初期同期をスキップします。</span><span class="sxs-lookup"><span data-stu-id="d97ea-214">Activate dual-write, and skip the initial synchronization.</span></span></li>
</ol>
</td>
</tr>
<tr>
<td rowspan='2'><span data-ttu-id="d97ea-215">既存</span><span class="sxs-lookup"><span data-stu-id="d97ea-215">Existing</span></span></td>
<td rowspan='2'><span data-ttu-id="d97ea-216">新規</span><span class="sxs-lookup"><span data-stu-id="d97ea-216">New</span></span></td>
<td rowspan='2'><span data-ttu-id="d97ea-217">あり</span><span class="sxs-lookup"><span data-stu-id="d97ea-217">Yes</span></span></td>
<td rowspan='2'><span data-ttu-id="d97ea-218">既存の Finance and Operations アプリ インスタンスと新しい Customer Engagement アプリ インスタンス</span><span class="sxs-lookup"><span data-stu-id="d97ea-218">An existing Finance and Operations app instance and a new customer engagement app instance</span></span></td>
<td><span data-ttu-id="d97ea-219">&lt;500,000</span><span class="sxs-lookup"><span data-stu-id="d97ea-219">&lt; 500,000</span></span></td>
<td><span data-ttu-id="d97ea-220">任意</span><span class="sxs-lookup"><span data-stu-id="d97ea-220">Any</span></span></td>
<td>
<ul>
<li><span data-ttu-id="d97ea-221">初期同期を実行します。</span><span class="sxs-lookup"><span data-stu-id="d97ea-221">Run the initial synchronization.</span></span></li>
</ul>
</td>
</tr>
<tr>
<td><span data-ttu-id="d97ea-222">&gt;500,000</span><span class="sxs-lookup"><span data-stu-id="d97ea-222">&gt; 500,000</span></span></td>
<td><span data-ttu-id="d97ea-223">任意</span><span class="sxs-lookup"><span data-stu-id="d97ea-223">Any</span></span></td>
<td>
<ol>
<li><span data-ttu-id="d97ea-224">各アプリにデータを移行します。</span><span class="sxs-lookup"><span data-stu-id="d97ea-224">Migrate data to each app.</span></span></li>
<li><span data-ttu-id="d97ea-225">二重書き込みを有効にし、初期同期をスキップします。</span><span class="sxs-lookup"><span data-stu-id="d97ea-225">Activate dual-write, and skip the initial synchronization.</span></span></li>
</ol>
</td>
</tr>
<tr>
<td rowspan='4'><span data-ttu-id="d97ea-226">既存</span><span class="sxs-lookup"><span data-stu-id="d97ea-226">Existing</span></span></td>
<td rowspan='4'><span data-ttu-id="d97ea-227">既存</span><span class="sxs-lookup"><span data-stu-id="d97ea-227">Existing</span></span></td>
<td rowspan='4'><span data-ttu-id="d97ea-228">あり</span><span class="sxs-lookup"><span data-stu-id="d97ea-228">Yes</span></span></td>
<td rowspan='4'><span data-ttu-id="d97ea-229">既存の Finance and Operations アプリ インスタンスと既存の Customer Engagement アプリ インスタンス</span><span class="sxs-lookup"><span data-stu-id="d97ea-229">An existing Finance and Operations app instance and an existing customer engagement app instance</span></span></td>
<td><span data-ttu-id="d97ea-230">&lt;70,000</span><span class="sxs-lookup"><span data-stu-id="d97ea-230">&lt; 70,000</span></span></td>
<td><span data-ttu-id="d97ea-231"><a href='#single-threaded-entities'>単一スレッド</a></span><span class="sxs-lookup"><span data-stu-id="d97ea-231"><a href='#single-threaded-entities'>Single-threaded</a></span></span></td>
<td>
<ol>
<li><span data-ttu-id="d97ea-232">会社コードのブートストラップ Dataverse。</span><span class="sxs-lookup"><span data-stu-id="d97ea-232">Bootstrap Dataverse for the company code.</span></span></li>
<li><span data-ttu-id="d97ea-233">初期同期を実行します。</span><span class="sxs-lookup"><span data-stu-id="d97ea-233">Run the initial synchronization.</span></span></li>
</ol>
</td>
</tr>
<tr>
<td><span data-ttu-id="d97ea-234">&gt;70,000</span><span class="sxs-lookup"><span data-stu-id="d97ea-234">&gt; 70,000</span></span></td>
<td><span data-ttu-id="d97ea-235"><a href='#single-threaded-entities'>単一スレッド</a></span><span class="sxs-lookup"><span data-stu-id="d97ea-235"><a href='#single-threaded-entities'>Single-threaded</a></span></span></td>
<td>
<ol>
<li><span data-ttu-id="d97ea-236">会社コードのブートストラップ Dataverse。</span><span class="sxs-lookup"><span data-stu-id="d97ea-236">Bootstrap Dataverse for the company code.</span></span></li>
<li><span data-ttu-id="d97ea-237">初期同期の範囲外で、各アプリにデータを移行します。</span><span class="sxs-lookup"><span data-stu-id="d97ea-237">Migrate data to each app outside the initial synchronization.</span></span></li>
<li><span data-ttu-id="d97ea-238">二重書き込みを有効にし、初期同期をスキップします。</span><span class="sxs-lookup"><span data-stu-id="d97ea-238">Activate dual-write, and skip the initial synchronization.</span></span></li>
</ol>
</td>
</tr>
<tr>
<td><span data-ttu-id="d97ea-239">&lt;500,000</span><span class="sxs-lookup"><span data-stu-id="d97ea-239">&lt; 500,000</span></span></td>
<td><span data-ttu-id="d97ea-240">マルチスレッド</span><span class="sxs-lookup"><span data-stu-id="d97ea-240">Multi-threaded</span></span></td>
<td>
<ol>
<li><span data-ttu-id="d97ea-241">会社コードのブートストラップ Dataverse。</span><span class="sxs-lookup"><span data-stu-id="d97ea-241">Bootstrap Dataverse for the company code.</span></span></li>
<li><span data-ttu-id="d97ea-242">初期同期を実行します。</span><span class="sxs-lookup"><span data-stu-id="d97ea-242">Run the initial synchronization.</span></span></li>
</ol>
</td>
</tr>
<tr>
<td><span data-ttu-id="d97ea-243">&gt;500,000</span><span class="sxs-lookup"><span data-stu-id="d97ea-243">&gt; 500,000</span></span></td>
<td><span data-ttu-id="d97ea-244">任意</span><span class="sxs-lookup"><span data-stu-id="d97ea-244">Any</span></span></td>
<td>
<ol>
<li><span data-ttu-id="d97ea-245">会社コードのブートストラップ Dataverse。</span><span class="sxs-lookup"><span data-stu-id="d97ea-245">Bootstrap Dataverse for the company code.</span></span></li>
<li><span data-ttu-id="d97ea-246">初期同期の範囲外で、各アプリにデータを移行します。</span><span class="sxs-lookup"><span data-stu-id="d97ea-246">Migrate data to each app outside the initial synchronization.</span></span></li>
<li><span data-ttu-id="d97ea-247">二重書き込みを有効にし、初期同期をスキップします。</span><span class="sxs-lookup"><span data-stu-id="d97ea-247">Activate dual-write, and skip the initial synchronization.</span></span></li>
</ol>
</td>
</tr>
</tbody>
</table>

## <a name="single-threaded-tables"></a><a id="single-threaded-entities"></a><span data-ttu-id="d97ea-248">単一スレッド テーブル</span><span class="sxs-lookup"><span data-stu-id="d97ea-248">Single-threaded tables</span></span>

- <span data-ttu-id="d97ea-249">消費税コード (msdyn\_taxcodes)</span><span class="sxs-lookup"><span data-stu-id="d97ea-249">Sales tax codes (msdyn\_taxcodes)</span></span>
- <span data-ttu-id="d97ea-250">顧客 V3 (アカウント)</span><span class="sxs-lookup"><span data-stu-id="d97ea-250">Customers V3 (accounts)</span></span>
- <span data-ttu-id="d97ea-251">仕入先 V2 (msdyn\_vendors)</span><span class="sxs-lookup"><span data-stu-id="d97ea-251">Vendors V2 (msdyn\_vendors)</span></span>
- <span data-ttu-id="d97ea-252">倉庫 (msdyn\_warehouses)</span><span class="sxs-lookup"><span data-stu-id="d97ea-252">Warehouses (msdyn\_warehouses)</span></span>
- <span data-ttu-id="d97ea-253">製品カテゴリ (msdyn\_productcategories)</span><span class="sxs-lookup"><span data-stu-id="d97ea-253">Product categories (msdyn\_productcategories)</span></span>
- <span data-ttu-id="d97ea-254">雇用 (cdm\_employments)</span><span class="sxs-lookup"><span data-stu-id="d97ea-254">Employment (cdm\_employments)</span></span>
- <span data-ttu-id="d97ea-255">職位作業者割り当て (cdm\_positionworkerassignmentmaps)</span><span class="sxs-lookup"><span data-stu-id="d97ea-255">Position worker assignments (cdm\_positionworkerassignmentmaps)</span></span>
- <span data-ttu-id="d97ea-256">倉庫の場所 (msdyn\_inventorylocations)</span><span class="sxs-lookup"><span data-stu-id="d97ea-256">Warehouse locations (msdyn\_inventorylocations)</span></span>
- <span data-ttu-id="d97ea-257">配送モード (msdyn\_shipvias)</span><span class="sxs-lookup"><span data-stu-id="d97ea-257">Modes of delivery (msdyn\_shipvias)</span></span>
