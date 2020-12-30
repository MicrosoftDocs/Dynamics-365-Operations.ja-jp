---
title: BYOD でスケジュール設定されたバッチ ジョブを最適化する
description: このトピックでは、Microsoft Dynamics 365 Human Resources でデータベースの持ち込み (BYOD) 機能を使用している場合のパフォーマンスの最適化方法について説明します。
author: andreabichsel
manager: AnnBe
ms.date: 08/17/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-human-resources
ms.technology: ''
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Core, Human Resources
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: anbichse
ms.search.validFrom: 2020-08-10
ms.dyn365.ops.version: Platform update 36
ms.openlocfilehash: d08762ff40b4da8264bd5bc4a1c16fd2afc4d610
ms.sourcegitcommit: 199848e78df5cb7c439b001bdbe1ece963593cdb
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 10/13/2020
ms.locfileid: "4419353"
---
# <a name="optimize-byod-scheduled-batch-jobs"></a><span data-ttu-id="a6d76-103">BYOD でスケジュール設定されたバッチ ジョブを最適化する</span><span class="sxs-lookup"><span data-stu-id="a6d76-103">Optimize BYOD scheduled batch jobs</span></span>

<span data-ttu-id="a6d76-104">このトピックでは、データベースの持ち込み (BYOD) 機能を使用している場合のパフォーマンスの最適化方法について説明します。</span><span class="sxs-lookup"><span data-stu-id="a6d76-104">This topic explains how to optimize performance when you're using the bring your own database (BYOD) feature.</span></span> <span data-ttu-id="a6d76-105">詳細については、[自分のデータベースの持ち込み (BYOD)](https://docs.microsoft.com/dynamics365/fin-ops-core/dev-itpro/analytics/export-entities-to-your-own-database?toc=/dynamics365/human-resources/toc.json)を参照してください。</span><span class="sxs-lookup"><span data-stu-id="a6d76-105">For more information about BYOD, see [Bring your own database (BYOD)](https://docs.microsoft.com/dynamics365/fin-ops-core/dev-itpro/analytics/export-entities-to-your-own-database?toc=/dynamics365/human-resources/toc.json).</span></span>

## <a name="performance-considerations-for-data-export"></a><span data-ttu-id="a6d76-106">データ エクスポートのパフォーマンスに関する考慮事項</span><span class="sxs-lookup"><span data-stu-id="a6d76-106">Performance considerations for data export</span></span>

<span data-ttu-id="a6d76-107">エンティティが宛先データベースに公開された後、**データ管理** ワークスペースのエクスポート機能を使用してデータを移動することができます。</span><span class="sxs-lookup"><span data-stu-id="a6d76-107">After entities are published to the destination database, you can use the Export function in the **Data management** workspace to move data.</span></span> <span data-ttu-id="a6d76-108">エクスポート関数を使用すると、1 つまたは複数のエンティティが含まれるデータ移動ジョブを定義できます。</span><span class="sxs-lookup"><span data-stu-id="a6d76-108">The Export function lets you define a Data movement job that contains one or more entities.</span></span> <span data-ttu-id="a6d76-109">データのエクスポートについての詳細情報は、[データのインポート ジョブとエクスポート ジョブの概要](https://docs.microsoft.com/dynamics365/fin-ops-core/dev-itpro/data-entities/data-import-export-job?toc=/dynamics365/human-resources/toc.json) を参照してください。</span><span class="sxs-lookup"><span data-stu-id="a6d76-109">For more information about data export, see [Data import and export jobs overview](https://docs.microsoft.com/dynamics365/fin-ops-core/dev-itpro/data-entities/data-import-export-job?toc=/dynamics365/human-resources/toc.json).</span></span>

<span data-ttu-id="a6d76-110">**エクスポート** ページを使用すると、データをコンマ区切り値 (CSV) ファイルなどの様々なターゲットのデータ書式にエクスポートすることができます。</span><span class="sxs-lookup"><span data-stu-id="a6d76-110">You can use the **Export** page to export data into different target data formats, such as a comma-separated values (CSV) file.</span></span> <span data-ttu-id="a6d76-111">このページは、別の宛先として SQL データベースもサポートしています。</span><span class="sxs-lookup"><span data-stu-id="a6d76-111">This page also supports SQL databases as another destination.</span></span>

<span data-ttu-id="a6d76-112">複数のエンティティを持つデータ プロジェクトを作成し、バッチジョブを使用してそのデータ プロジェクトの実行をスケジュールすることができます。</span><span class="sxs-lookup"><span data-stu-id="a6d76-112">You can create a data project that has multiple entities and use a batch job to schedule that data project to run.</span></span> <span data-ttu-id="a6d76-113">また、**バッチ処理でエクスポート** オプションを選択することにより、データ エクスポート ジョブを定期的に実行することができます。</span><span class="sxs-lookup"><span data-stu-id="a6d76-113">If you select the **Export in batch** option, you can schedule the data export job to run periodically.</span></span>

<span data-ttu-id="a6d76-114">BYOD エクスポートの全体的な信頼性を維持するために、エクスポート プロジェクトに複数のエンティティを追加する場合は注意する必要があります。</span><span class="sxs-lookup"><span data-stu-id="a6d76-114">To help preserve the overall reliability of the BYOD export, you must be careful when you add multiple entities to an export project.</span></span> <span data-ttu-id="a6d76-115">同じプロジェクトに追加するエンティティの数を決定する際には、以下のパラメーターを考慮してください。</span><span class="sxs-lookup"><span data-stu-id="a6d76-115">When you're determining the number of entities to add to the same project, consider the following parameters:</span></span>

- <span data-ttu-id="a6d76-116">エンティティの複雑性</span><span class="sxs-lookup"><span data-stu-id="a6d76-116">The complexity of the entities</span></span>
- <span data-ttu-id="a6d76-117">エンティティごとの予想されるデータ量</span><span class="sxs-lookup"><span data-stu-id="a6d76-117">The expected data volume per entity</span></span>
- <span data-ttu-id="a6d76-118">ジョブ レベルでエクスポートを完了するにあたって必要となる全体的な時間</span><span class="sxs-lookup"><span data-stu-id="a6d76-118">The overall time that will be required to complete the export at the job level</span></span>

<span data-ttu-id="a6d76-119">最高のパフォーマンスを得るには、1つのプロジェクトにたくさんののエンティティを追加しないでください。</span><span class="sxs-lookup"><span data-stu-id="a6d76-119">For the best performance, avoid adding hundreds of entities to a single project.</span></span> <span data-ttu-id="a6d76-120">複数のジョブを作成し、各ジョブに含まれるエンティティ数を削減することをお勧めします。</span><span class="sxs-lookup"><span data-stu-id="a6d76-120">We recommend that you create multiple jobs, each of which contains fewer entities.</span></span>

## <a name="scheduling-byod-batch-jobs"></a><span data-ttu-id="a6d76-121">BYOD バッチ バッチジョブのスケジュール設定</span><span class="sxs-lookup"><span data-stu-id="a6d76-121">Scheduling BYOD batch jobs</span></span>

<span data-ttu-id="a6d76-122">Microsoft Dynamics 365 Human Resources のユーザーへの影響を軽減するには、夜間または業務時間外に BYOD バッチジョブを実行してください。</span><span class="sxs-lookup"><span data-stu-id="a6d76-122">To help reduce the impact on users of Microsoft Dynamics 365 Human Resources, run BYOD batch jobs at night or after hours.</span></span> <span data-ttu-id="a6d76-123">これらの定期的なバッチ ジョブを実行するタイム ゾーンを確認してください。</span><span class="sxs-lookup"><span data-stu-id="a6d76-123">Be sure to check the time zone for recurring batch jobs.</span></span> <span data-ttu-id="a6d76-124">一部のバッチ ジョブは、太平洋標準時 (PST) を使用している場合があります。</span><span class="sxs-lookup"><span data-stu-id="a6d76-124">Some batch jobs might use Pacific Standard Time (PST).</span></span>

<span data-ttu-id="a6d76-125">パフォーマンスの問題を回避するために、BYOD バッチジョブのスケジューリング頻度を公正する際は、次の要素を考慮してください :</span><span class="sxs-lookup"><span data-stu-id="a6d76-125">To help avoid performance issues, consider the following factors when you configure the scheduling frequency for BYOD batch jobs:</span></span>

- <span data-ttu-id="a6d76-126">各バッチジョブの完了までに必要となる時間</span><span class="sxs-lookup"><span data-stu-id="a6d76-126">The time that is required to complete each batch job</span></span>
- <span data-ttu-id="a6d76-127">BYOD のデータに対する業務上のニーズ</span><span class="sxs-lookup"><span data-stu-id="a6d76-127">The business need for the data in BYOD</span></span>

<span data-ttu-id="a6d76-128">各バッチジョブの頻度を設定して、次にスケジュール設定された実行時間よりも前にジョブを完了できるようにしてください。</span><span class="sxs-lookup"><span data-stu-id="a6d76-128">Set the frequency for each batch job to a value that ensures that the job can be completed well before its next scheduled run time.</span></span> <span data-ttu-id="a6d76-129">この方法は、Human Resources のパフォーマンスに悪影響を及ぼす可能性があるため、複数のジョブを並行して実行しないようにしてください。</span><span class="sxs-lookup"><span data-stu-id="a6d76-129">Avoid running multiple jobs in parallel, because this approach can negatively affect the performance of Human Resources.</span></span>

<span data-ttu-id="a6d76-130">最高のパフォーマンスを得るためには、**エクスポート** ページの **バッチ処理でエクスポート** オプションを使用して、BYOD バッチジョブをスケジュール設定してください。</span><span class="sxs-lookup"><span data-stu-id="a6d76-130">For the best performance, always use the **Export in batch** option on the **Export** page to schedule BYOD batch jobs.</span></span> <span data-ttu-id="a6d76-131">**管理 \> 定期データ ジョブの管理** にて定期的なスケジュール設定されたエクスポートを回避します。</span><span class="sxs-lookup"><span data-stu-id="a6d76-131">Avoid scheduling recurring exports at **Manage \> Manage recurring data jobs**.</span></span>

## <a name="incremental-export"></a><span data-ttu-id="a6d76-132">差分エクスポート</span><span class="sxs-lookup"><span data-stu-id="a6d76-132">Incremental export</span></span>

<span data-ttu-id="a6d76-133">データ エクスポートにエンティティを追加する場合は、増分プッシュ (エクスポート) またはフル プッシュのいずれかを行うことができます。</span><span class="sxs-lookup"><span data-stu-id="a6d76-133">When you add an entity for data export, you can do either an incremental push (export) or a full push.</span></span> <span data-ttu-id="a6d76-134">フル プッシュは、BYOD データベースのエンティティから既存のレコードをすべて削除します。</span><span class="sxs-lookup"><span data-stu-id="a6d76-134">A full push deletes all existing records from an entity in the BYOD database.</span></span> <span data-ttu-id="a6d76-135">続いて、Human Resources エンティティから現在のレコードセットを挿入します。</span><span class="sxs-lookup"><span data-stu-id="a6d76-135">It then inserts the current set of records from the Human Resources entity.</span></span>

<span data-ttu-id="a6d76-136">増分プッシュを実行するには、**エンティティ** ページで各エンティティの変更の追跡を有効にする必要があります。</span><span class="sxs-lookup"><span data-stu-id="a6d76-136">To do an incremental push, you must turn on change tracking for each entity on the **Entities** page.</span></span> <span data-ttu-id="a6d76-137">詳細については、 [エンティティへの変更の追跡を有効化する](https://docs.microsoft.com/dynamics365/fin-ops-core/dev-itpro/data-entities/entity-change-track?toc=/dynamics365/human-resources/toc.json)を参照してください。</span><span class="sxs-lookup"><span data-stu-id="a6d76-137">For more information, see [Enable change tracking for entities](https://docs.microsoft.com/dynamics365/fin-ops-core/dev-itpro/data-entities/entity-change-track?toc=/dynamics365/human-resources/toc.json).</span></span>

<span data-ttu-id="a6d76-138">増分プッシュを選択した場合、最初のプッシュは常に完全なプッシュになります。</span><span class="sxs-lookup"><span data-stu-id="a6d76-138">If you select an incremental push, the first push is always a full push.</span></span> <span data-ttu-id="a6d76-139">SQL は、この最初の完全プッシュからの変更を追跡します。</span><span class="sxs-lookup"><span data-stu-id="a6d76-139">SQL tracks changes from this first full push.</span></span> <span data-ttu-id="a6d76-140">新しいレコードが挿入される、またはレコードが追加または削除されるたびに、これら変更が宛先エンティティに反映されます。</span><span class="sxs-lookup"><span data-stu-id="a6d76-140">When a new record is inserted, or when a record is updated or deleted, the change is reflected in the destination entity.</span></span>

## <a name="time-outs"></a><span data-ttu-id="a6d76-141">タイムアウト</span><span class="sxs-lookup"><span data-stu-id="a6d76-141">Time-outs</span></span>

<span data-ttu-id="a6d76-142">BYOD エクスポートの既定のタイムアウトを示します :</span><span class="sxs-lookup"><span data-stu-id="a6d76-142">Here are the default time-outs for BYOD exports:</span></span>

- <span data-ttu-id="a6d76-143">トランケート処理では 10分間</span><span class="sxs-lookup"><span data-stu-id="a6d76-143">Ten minutes for truncation operations</span></span>
- <span data-ttu-id="a6d76-144">一括挿入処理では 1 時間</span><span class="sxs-lookup"><span data-stu-id="a6d76-144">One hour for bulk insert operations</span></span>

<span data-ttu-id="a6d76-145">ボリュームが多い場合、これらのタイムアウト設定の時間内に処理が完了しない場合があります。</span><span class="sxs-lookup"><span data-stu-id="a6d76-145">When volumes are high, these time-out settings might not be sufficient.</span></span> <span data-ttu-id="a6d76-146">これらを変更するには、**データ管理 \> フレームワークパラメータ \> 独自のデータベース** に移動します。</span><span class="sxs-lookup"><span data-stu-id="a6d76-146">To update them, go to **Data management \> Framework parameters \> Bring your own database**.</span></span> <span data-ttu-id="a6d76-147">タイムアウトは会社ごとに固有の設定となるため、それぞれの会社ごとに個別に設定する必要があります。</span><span class="sxs-lookup"><span data-stu-id="a6d76-147">These time-outs are company-specific and must be set separately for each company.</span></span>

## <a name="known-limitations"></a><span data-ttu-id="a6d76-148">既知の制限</span><span class="sxs-lookup"><span data-stu-id="a6d76-148">Known limitations</span></span>

<span data-ttu-id="a6d76-149">BYOD 機能には、次の制限があります :</span><span class="sxs-lookup"><span data-stu-id="a6d76-149">The BYOD feature has the following limitations:</span></span>

- <span data-ttu-id="a6d76-150">同期中のデータベースにはアクティブなロックが存在してはいけません。</span><span class="sxs-lookup"><span data-stu-id="a6d76-150">There should be no active locks on your database during synchronization.</span></span> <span data-ttu-id="a6d76-151">アクティブなロックが存在すると、Azure SQL database へのデータのエクスポート時に、書き込速度の低下や失敗が発生する場合があります。</span><span class="sxs-lookup"><span data-stu-id="a6d76-151">Active locks can cause slow writes or even failure to export data to your Azure SQL database.</span></span>
- <span data-ttu-id="a6d76-152">独自のデータベースには、複合のエンティティをエクスポートすることはできません。</span><span class="sxs-lookup"><span data-stu-id="a6d76-152">You can't export composite entities into your own database.</span></span> <span data-ttu-id="a6d76-153">現在、複合エンティティがサポートされていません。</span><span class="sxs-lookup"><span data-stu-id="a6d76-153">Currently, composite entities aren't supported.</span></span> <span data-ttu-id="a6d76-154">複合エンティティを構成する個々 のエンティティをエクスポートする必要があります。</span><span class="sxs-lookup"><span data-stu-id="a6d76-154">You must export individual entities that make up the composite entity.</span></span> <span data-ttu-id="a6d76-155">ただし、同じデータ プロジェクト内では両方のエンティティをエクスポートすることができます。</span><span class="sxs-lookup"><span data-stu-id="a6d76-155">However, you can export both entities in the same data project.</span></span>
- <span data-ttu-id="a6d76-156">固有のキーを持たないエンティティは、増分プッシュを使用してのエクスポートはできません。</span><span class="sxs-lookup"><span data-stu-id="a6d76-156">Entities that don't have unique keys can't be exported by using incremental push.</span></span> <span data-ttu-id="a6d76-157">この制限は特に、数個の既製エンティティからレコードを段階的にエクスポートする場合に直面する可能性があります。</span><span class="sxs-lookup"><span data-stu-id="a6d76-157">You might face this limitation especially when you try to incrementally export records from a few ready-made entities.</span></span> <span data-ttu-id="a6d76-158">これらのエンティティはデータをインポートできるように設計されているため、固有のキーはありません。</span><span class="sxs-lookup"><span data-stu-id="a6d76-158">Because these entities were designed to enable the import of data, they don't have a unique key.</span></span>

## <a name="troubleshooting"></a><span data-ttu-id="a6d76-159">トラブルシューティング</span><span class="sxs-lookup"><span data-stu-id="a6d76-159">Troubleshooting</span></span>

### <a name="incremental-push-doesnt-work-correctly"></a><span data-ttu-id="a6d76-160">増分プッシュが正常に機能しない</span><span class="sxs-lookup"><span data-stu-id="a6d76-160">Incremental push doesn't work correctly</span></span>

<span data-ttu-id="a6d76-161">**問題 :** あるエンティティに対してフルプッシュが実行された場合、**セレクト** 文を使用すると BYOD で大量のレコードセットが表示されます。</span><span class="sxs-lookup"><span data-stu-id="a6d76-161">**Issue:** When a full push occurs for an entity, you see a large set of records in BYOD when you use a **select** statement.</span></span> <span data-ttu-id="a6d76-162">しかし、増分プッシュを行うと、BYOD では数件のレコードしか表示されません。</span><span class="sxs-lookup"><span data-stu-id="a6d76-162">However, when you do an incremental push, you see only a few records in BYOD.</span></span> <span data-ttu-id="a6d76-163">増分プッシュですべてのレコードが削除され、BYOD で変更したレコードだけが追加されたように見えます。</span><span class="sxs-lookup"><span data-stu-id="a6d76-163">It seems as though the incremental push deleted all the records and added only the changed records in BYOD.</span></span>

<span data-ttu-id="a6d76-164">**解決策 :** SQLの変更追跡テーブルがしかるべき状態になっていない可能性があります。</span><span class="sxs-lookup"><span data-stu-id="a6d76-164">**Solution:** The SQL change tracking tables might not be in the expected state.</span></span> <span data-ttu-id="a6d76-165">このような場合は、エンティティの変更の追跡をオフにしてからオンに戻すことをお勧めします。</span><span class="sxs-lookup"><span data-stu-id="a6d76-165">In cases of this type, we recommend that you turn off change tracking for the entity and then turn it back on.</span></span> <span data-ttu-id="a6d76-166">詳細については、 [エンティティへの変更の追跡を有効化する](https://docs.microsoft.com/dynamics365/fin-ops-core/dev-itpro/data-entities/entity-change-track?toc=/dynamics365/human-resources/toc.json)を参照してください。</span><span class="sxs-lookup"><span data-stu-id="a6d76-166">For more information, see [Enable change tracking for entities](https://docs.microsoft.com/dynamics365/fin-ops-core/dev-itpro/data-entities/entity-change-track?toc=/dynamics365/human-resources/toc.json).</span></span>

## <a name="see-also"></a><span data-ttu-id="a6d76-167">参照</span><span class="sxs-lookup"><span data-stu-id="a6d76-167">See also</span></span>

[<span data-ttu-id="a6d76-168">データ管理の概要</span><span class="sxs-lookup"><span data-stu-id="a6d76-168">Data management overview</span></span>](https://docs.microsoft.com/dynamics365/fin-ops-core/dev-itpro/data-entities/data-entities-data-packages?toc=/dynamics365/human-resources/toc.json)<br>
[<span data-ttu-id="a6d76-169">自分のデータベースの持ち込み (BYOD)</span><span class="sxs-lookup"><span data-stu-id="a6d76-169">Bring your own database (BYOD)</span></span>](https://docs.microsoft.com/dynamics365/fin-ops-core/dev-itpro/analytics/export-entities-to-your-own-database?toc=/dynamics365/human-resources/toc.json)<br>
[<span data-ttu-id="a6d76-170">データ インポート/エクスポート ジョブの概要</span><span class="sxs-lookup"><span data-stu-id="a6d76-170">Data import and export jobs overview</span></span>](https://docs.microsoft.com/dynamics365/fin-ops-core/dev-itpro/data-entities/data-import-export-job?toc=/dynamics365/human-resources/toc.json)<br>
[<span data-ttu-id="a6d76-171">エンティティの変更追跡の有効化</span><span class="sxs-lookup"><span data-stu-id="a6d76-171">Enable change tracking for entities</span></span>](https://docs.microsoft.com/dynamics365/fin-ops-core/dev-itpro/data-entities/entity-change-track?toc=/dynamics365/human-resources/toc.json)
