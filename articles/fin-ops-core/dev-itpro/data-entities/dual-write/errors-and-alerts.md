---
title: エラー管理と警告通知
description: このトピックでは、問題のトラブルシューティングに役立つエラー ログと警告通知について説明します。
author: sabinn-msft
ms.date: 03/20/2020
ms.topic: article
audience: Developer
ms.reviewer: v-douklo
ms.search.region: Global
ms.author: sabinn
ms.search.validFrom: 2020-03-20
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 760f7253e870a22d732c04633815a521b37f061d
ms.sourcegitcommit: d13c0ff34f52ea0453d281fed643bc9a983fb7e8
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 05/14/2021
ms.locfileid: "6033283"
---
# <a name="error-management-and-alert-notifications"></a><span data-ttu-id="29a00-103">エラー管理と警告通知</span><span class="sxs-lookup"><span data-stu-id="29a00-103">Error management and alert notifications</span></span>

[!include [banner](../../includes/banner.md)]

[!include [rename-banner](~/includes/cc-data-platform-banner.md)]

<span data-ttu-id="29a00-104">Microsoft は、エラーに強い二重書き込みを実現するために、多くの時間と労力を費やしてきました。</span><span class="sxs-lookup"><span data-stu-id="29a00-104">Microsoft has invested lots of time and effort into making dual-write resilient to errors.</span></span> <span data-ttu-id="29a00-105">ただし、二重書き込み用のテーブル マップを有効にしている間または後に、問題が発生した場合は、特定のテーブル マップを選択して、それらのすべてのアクティビティとエラーの統合ビューを取得できます。</span><span class="sxs-lookup"><span data-stu-id="29a00-105">However, if you encounter an issue while or after you enable table maps for dual-write, you can select specific table maps to get a consolidated view of all the activities and errors for them.</span></span> <span data-ttu-id="29a00-106">この統合ビューには、エラー ログが含まれています。</span><span class="sxs-lookup"><span data-stu-id="29a00-106">This consolidated view includes error logs.</span></span> <span data-ttu-id="29a00-107">目標は、テーブル マップのアクティビティの単一ビューを提供することにより、トラブルシューティングを支援することです。</span><span class="sxs-lookup"><span data-stu-id="29a00-107">The goal is to help you during troubleshooting by providing a single view of the activities for a table map.</span></span>

## <a name="consolidated-error-management"></a><span data-ttu-id="29a00-108">統合されたエラー管理</span><span class="sxs-lookup"><span data-stu-id="29a00-108">Consolidated error management</span></span>

<span data-ttu-id="29a00-109">アクティビティ ログは、特定のテーブル マップが **実行していません** の状態から **実行中** 状態に移行するイベントの時系列一覧を提供します。</span><span class="sxs-lookup"><span data-stu-id="29a00-109">The activity log provides a chronological list of events that a specific table map goes through from the **Not Running** status to the **Running** status.</span></span> <span data-ttu-id="29a00-110">たとえば、一覧には、作成されたマッピング、列マッピングの更新、実行されたマッピングを含めることができます。</span><span class="sxs-lookup"><span data-stu-id="29a00-110">For example, the list can include mappings that are created, updates of column mappings, and mappings that are run.</span></span> <span data-ttu-id="29a00-111">さらに、エラーが発生した場合は、ログをダウンロードして、次のレベルの詳細を取得できます。</span><span class="sxs-lookup"><span data-stu-id="29a00-111">Additionally, if errors occur, you can download the logs to get the next level of details.</span></span>

![アクティビティ ログの表示](media/activity-log.png)

## <a name="re-running-execution-for-initial-sync"></a><span data-ttu-id="29a00-113">初期同期の実行の再実行</span><span class="sxs-lookup"><span data-stu-id="29a00-113">Re-running execution for Initial sync</span></span>

<span data-ttu-id="29a00-114">Finance and Operations アプリ と Dataverse の間で既存のデータをコピーしているときに問題が発生した場合、**初回同期の詳細** タブにエラー数が表示されます。</span><span class="sxs-lookup"><span data-stu-id="29a00-114">If you encounter issues while you copy pre-existing data between Finance and Operations apps and Dataverse, the **Initial sync details** tab provides a count of the errors.</span></span> 

![初期同期エラー](media/Initial-sync-rerun-1.png)

<span data-ttu-id="29a00-116">個々のプロジェクトをクリックすると、同期が失敗した方向 (Finance and Operations アプリから Dataverse またはその逆) と、失敗した理由の詳細が表示されます。</span><span class="sxs-lookup"><span data-stu-id="29a00-116">Clicking on the individual project will show you the direction in which the sync failed (Finance and Operations app to Dataverse or vice-versa) and details of why it failed.</span></span> <span data-ttu-id="29a00-117">基になる問題を修正することを選択してから、最後の同期で失敗またはエラーが発生したレコードとともに、に実行全体を再試行する **実行の再実行** を選択できます。これが完了すると、初期同期が完了し、テーブルは **実行中** の状態に戻ります。</span><span class="sxs-lookup"><span data-stu-id="29a00-117">You can choose to fix the underlying issues and then select **Re-run execution** which retries the entire execution, along with the records that failed or errored out in the last sync. Once this completes, initial sync is completed and the table returns to the **Running** state.</span></span> <span data-ttu-id="29a00-118">エラーを無視して新しい増分データを追加する場合があります。</span><span class="sxs-lookup"><span data-stu-id="29a00-118">There may be cases where you want to ignore the errors and add new incremental data.</span></span> <span data-ttu-id="29a00-119">この場合は、**エラーなしで再実行** を選択できます。これにより、新しいデータを追加し、エラーが発生したレコードを再試行する必要がなくなります。</span><span class="sxs-lookup"><span data-stu-id="29a00-119">In these cases, you can select **Rerun execution without errors**, which lets you add new data and not retry the errored records.</span></span> 

![エラーのある初期同期再試行](media/Initial-sync-rerun-3.png)

<span data-ttu-id="29a00-121">完了すると、状態が **完了** とマークされ、テーブルを **実行中** の状態に変更できます。</span><span class="sxs-lookup"><span data-stu-id="29a00-121">Once it is done, the status is marked **Completed** and then you can change the table to the **Running** state.</span></span> 

![エラーのない初期同期再試行](media/Initial-sync-rerun-4.png)

## <a name="queued-records-insights-and-error-management&quot;></a><span data-ttu-id=&quot;29a00-123&quot;>キューに入れられたレコードのインサイトとエラー管理</span><span class=&quot;sxs-lookup&quot;><span data-stu-id=&quot;29a00-123&quot;>Queued records insights and error management</span></span>

<span data-ttu-id=&quot;29a00-124&quot;>テーブル マップを一時停止する機能は、計画的または計画外のメンテナンスに対処するように設計されました。</span><span class=&quot;sxs-lookup&quot;><span data-stu-id=&quot;29a00-124&quot;>The ability to pause a table map was designed to address planned or unplanned maintenance.</span></span> <span data-ttu-id=&quot;29a00-125&quot;>特に計画的または計画外のメンテナンス中にビジネスの継続性を確保するために、ルールを介して手動または自動でテーブル マップを一時停止できます。</span><span class=&quot;sxs-lookup&quot;><span data-stu-id=&quot;29a00-125&quot;>To ensure business continuity, especially during planned or unplanned maintenance, you can pause table maps, manually or automatically via rules.</span></span> <span data-ttu-id=&quot;29a00-126&quot;>これにより、ユーザーは引き続き作業を行い、アプリがメンテナンスから復元中でもレコードを作成できます。</span><span class=&quot;sxs-lookup&quot;><span data-stu-id=&quot;29a00-126&quot;>This lets users continue to do their work and create records while the app is being recovered from maintenance.</span></span>

<span data-ttu-id=&quot;29a00-127&quot;>**実行中** の状態のテーブル マップを一時停止すると、テーブル マップを再開するまで、作成または更新されたすべてのレコードがキューに入れられます。</span><span class=&quot;sxs-lookup&quot;><span data-stu-id=&quot;29a00-127&quot;>When you pause a table map that is in the **Running** state, all records created or updated are queued until you resume the table map.</span></span> <span data-ttu-id=&quot;29a00-128&quot;>キューに入れたレコードはセキュリティで保護された Azure ストレージに格納され、再開してテーブル マップを **実行中** の状態に戻すと再生されます。</span><span class=&quot;sxs-lookup&quot;><span data-stu-id=&quot;29a00-128&quot;>The queued records are stored in secure Azure storage and replayed back when you resume and put the table map back into **Running** state.</span></span>

> [!NOTE]
> <span data-ttu-id=&quot;29a00-129&quot;>テーブル マップが **一時停止** の状態の場合、レコードの数とレコードをキューに入れることができる時間には制限があります。</span><span class=&quot;sxs-lookup&quot;><span data-stu-id=&quot;29a00-129&quot;>When a table map is in the **Paused** state, there are limits to the number of records and amount of time you can queue the records.</span></span> <span data-ttu-id=&quot;29a00-130&quot;>最初に発生した制限が適用されます。</span><span class=&quot;sxs-lookup&quot;><span data-stu-id=&quot;29a00-130&quot;>Whichever limits occurs first will apply.</span></span> <span data-ttu-id=&quot;29a00-131&quot;>最初はソフト制限から開始し、最終的にはハード制限を適用して、ストレージ制限を超えないようにします。</span><span class=&quot;sxs-lookup&quot;><span data-stu-id=&quot;29a00-131&quot;>We will start with soft limits and eventually enforce harder limits to protect you from exceeding the storage limits.</span></span>

<span data-ttu-id=&quot;29a00-132&quot;>**一時停止** 状態のテーブル マップ用に作成または更新されたレコードは、テーブル マップの **キューに入れられたレコード** で表示できます。</span><span class=&quot;sxs-lookup&quot;><span data-stu-id=&quot;29a00-132&quot;>Records created or updated for a table map in the **Paused** state can be viewed under **Queued records** for each table map.</span></span>

<span data-ttu-id=&quot;29a00-133&quot;>![キューに入れられたレコードのインサイト](media/Queued-Insights1.png &quot;キューに入れられたレコードのインサイト")</span><span class="sxs-lookup"><span data-stu-id="29a00-133">![Queued records insights](media/Queued-Insights1.png "Queued records insights")</span></span>

<span data-ttu-id="29a00-134">**キューに入れられたレコード数の合計** は、特定のテーブル マップに対してキューに入れられているレコードの合計数を示します。</span><span class="sxs-lookup"><span data-stu-id="29a00-134">The **Total queued record count** shows the total number of records queued for a given table map.</span></span> <span data-ttu-id="29a00-135">**さらに読み込む** をクリックすると、ページ設定された表示内で追加のレコードを表示できます。</span><span class="sxs-lookup"><span data-stu-id="29a00-135">You can click on **Load more** to see additional records in the paginated view.</span></span> <span data-ttu-id="29a00-136">統合キーでレコードのフィルタ処理もできます。</span><span class="sxs-lookup"><span data-stu-id="29a00-136">You can also filter the records on the integration key.</span></span>

<span data-ttu-id="29a00-137">テーブル マップを再開すると、**一時停止** 状態から **実行中** の状態に切り替わり、キューから送信先アプリケーションにレコードが書き込まれます。</span><span class="sxs-lookup"><span data-stu-id="29a00-137">When you resume the table map, it switches from the **Pause** state to the **Running** state and writes the records from the queue to the destination application.</span></span> <span data-ttu-id="29a00-138">送信先アプリでのビジネス検証など、さまざまな理由により、一部のレコードがエラーが発生し、書き込みに失敗する可能性があります。</span><span class="sxs-lookup"><span data-stu-id="29a00-138">It is possible that some records error out and fail to write due to various reasons including business validations on destination app.</span></span> <span data-ttu-id="29a00-139">このような場合、レコードは引き続きキューに残り、**キャッチ アップ エラー** タブに表示されます。</span><span class="sxs-lookup"><span data-stu-id="29a00-139">In these cases, the records will continue to remain in the queue and can be viewed under the **Catch-up errors** tab.</span></span>

<span data-ttu-id="29a00-140">![キューに入れられたレコードの再試行を選択](media/Queued-Insights-retry-selected3.png "キューに入れられたレコードの再試行を選択")</span><span class="sxs-lookup"><span data-stu-id="29a00-140">![Queued records retry selected](media/Queued-Insights-retry-selected3.png "Queued records retry selected")</span></span>

<span data-ttu-id="29a00-141">詳細なエラー メッセージは、基になる問題を修正するのに役立ちます。その後、**再試行の選択** レコードまたは **すべて再試行** レコードを選択できます。</span><span class="sxs-lookup"><span data-stu-id="29a00-141">The detailed Error message will help you fix the underlying issue after which you could **Retry selected** records or **Retry All** records.</span></span> <span data-ttu-id="29a00-142">再試行が成功すると、**再試行の状態** が **完了** とマークされます。</span><span class="sxs-lookup"><span data-stu-id="29a00-142">Once the retry is successful, **Retry status** will be marked as **Completed**.</span></span>

<span data-ttu-id="29a00-143">![キューに入れられたレコードが完了](media/Queued-Insights-retry-selected4.png "キューに入れられたレコードの再試行を選択")</span><span class="sxs-lookup"><span data-stu-id="29a00-143">![Queued records completed](media/Queued-Insights-retry-selected4.png "Queued records retry selected")</span></span>

> [!NOTE]
> <span data-ttu-id="29a00-144">エラーが発生したレコードは、7 日間キューで使用可能になり、その後キューは削除されます。</span><span class="sxs-lookup"><span data-stu-id="29a00-144">Errored records will be available in the queue for 7 days after which will the queue will be purged.</span></span> <span data-ttu-id="29a00-145">場合によっては、これらのレコードが不要になり、キューから削除できることがあります。</span><span class="sxs-lookup"><span data-stu-id="29a00-145">In some cases, you may no longer need these records and they can be deleted from the queue.</span></span>

## <a name="alert-notifications"></a><span data-ttu-id="29a00-146">警告の通知</span><span class="sxs-lookup"><span data-stu-id="29a00-146">Alert notifications</span></span>

<span data-ttu-id="29a00-147">管理者は、1 つ以上の警告設定を作成して、計画的または計画外のメンテナンスのケースを処理することができます。</span><span class="sxs-lookup"><span data-stu-id="29a00-147">As an admin, you can create one or more alert settings to handle cases of planned or unplanned maintenance.</span></span> <span data-ttu-id="29a00-148">たとえば、ネットワーク エラーなどが原因で特定のエラーしきい値に達した場合に、電子メールで通知するように、二重書き込みシステムを設定できます。</span><span class="sxs-lookup"><span data-stu-id="29a00-148">For example, you can set up the dual-write system to notify you by email if a specific error threshold is reached because of, for example, network errors.</span></span> <span data-ttu-id="29a00-149">二重書き込みシステムは、ユーザーの代わりにアクションを実行することもできます。</span><span class="sxs-lookup"><span data-stu-id="29a00-149">The dual-write system can also take action on your behalf.</span></span> <span data-ttu-id="29a00-150">たとえば、二重書き込みを一時停止または停止することができます。</span><span class="sxs-lookup"><span data-stu-id="29a00-150">For example, it can pause or stop dual-write.</span></span>

<span data-ttu-id="29a00-151">次の図は、**アプリケーション エラー** タイプのエラーが 15 分以内に 10 回発生した場合に、二重書き込みが一時停止する例を示しています。</span><span class="sxs-lookup"><span data-stu-id="29a00-151">The following illustration shows an example where dual-write will be paused if 10 errors of the **Application error** type occur within 15 minutes.</span></span>

![1 つ以上の警告設定の作成](media/create-alert-settings.png)

<span data-ttu-id="29a00-153">**警告設定の作成** を選択することにより、追加の警告を作成できます。</span><span class="sxs-lookup"><span data-stu-id="29a00-153">By selecting **Create alert settings**, you can create more alerts.</span></span> <span data-ttu-id="29a00-154">また、個人またはグループのどちらに通知を送信するかを選択したり、二重書き込みシステムがユーザーに代わりにアクションを実行するかどうかを選択することもできます。</span><span class="sxs-lookup"><span data-stu-id="29a00-154">You can also select whether notifications should be sent to an individual or a group, and whether the dual-write system should take any action on your behalf.</span></span> <span data-ttu-id="29a00-155">警告をグループに送信するには、コンマで区切られた値、例えば "id1@contoso.com, id2@contoso.com" を入力します。</span><span class="sxs-lookup"><span data-stu-id="29a00-155">To send alerts to a group, enter the values separated by commas, for example, "id1@contoso.com, id2@contoso.com".</span></span>

![警告の作成と通知の送信](media/create-alert-notification.png)

> [!NOTE]
> <span data-ttu-id="29a00-157">警告を有効にするには、テーブル マップを再起動する必要があります</span><span class="sxs-lookup"><span data-stu-id="29a00-157">In order for your alerts to take effect, you need to restart your table maps</span></span>

<span data-ttu-id="29a00-158">この機能は、計画外のメンテナンスがある場合に特に便利です。</span><span class="sxs-lookup"><span data-stu-id="29a00-158">This feature is especially useful if there is unplanned maintenance.</span></span> <span data-ttu-id="29a00-159">たとえば、アプリの 1 つが使用できなくなり、定義したしきい値に基づいて、二重書き込みが一時停止状態になり、すべての新しい要求がキューに入れられるます (つまり、それらは失われません)。</span><span class="sxs-lookup"><span data-stu-id="29a00-159">For example, one of the apps becomes unavailable and, based on your defined thresholds, dual-write goes into a paused state where all new requests are queued (that is, they aren't lost).</span></span> <span data-ttu-id="29a00-160">基になる問題を修正し、両方のアプリが正常に実行されたら、一時停止状態から再開できます。</span><span class="sxs-lookup"><span data-stu-id="29a00-160">After you fix the underlying issue, and both apps are running smoothly, you can resume from the paused state.</span></span> <span data-ttu-id="29a00-161">更新はキューから読み戻され、復元されたアプリに書き込まれます。</span><span class="sxs-lookup"><span data-stu-id="29a00-161">The updates will then be read back from the queue and written to the recovered app.</span></span>

## <a name="next-steps"></a><span data-ttu-id="29a00-162">次のステップ</span><span class="sxs-lookup"><span data-stu-id="29a00-162">Next steps</span></span>

[<span data-ttu-id="29a00-163">アプリケーション ライフサイクル管理</span><span class="sxs-lookup"><span data-stu-id="29a00-163">Application lifecycle management</span></span>](app-lifecycle-management.md)


[!INCLUDE[footer-include](../../../../includes/footer-banner.md)]
