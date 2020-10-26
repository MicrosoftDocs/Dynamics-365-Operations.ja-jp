---
title: 倉庫アプリ イベント
description: このトピックでは、倉庫アプリ イベントのメッセージをバッチ ジョブの一部として処理するために使用される、倉庫アプリのイベント処理について説明します。
author: perlynne
manager: tfehr
ms.date: 09/02/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: WHSMobileDeviceQueueEvent
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: perlynne
ms.search.validFrom: 2020-10-09
ms.dyn365.ops.version: 10.0.15
ms.openlocfilehash: 210008c4a1366773f465c59b38eca30f11f0b38c
ms.sourcegitcommit: 286786445f72db20e993d37a63df0b886f8f5e99
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 10/12/2020
ms.locfileid: "3988386"
---
# <a name="warehouse-app-event-processing"></a><span data-ttu-id="8fa7d-103">倉庫アプリのイベント処理</span><span class="sxs-lookup"><span data-stu-id="8fa7d-103">Warehouse app event processing</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="8fa7d-104">Supply Chain Management で実行されるバッチ ジョブでは、キューのデータを使用して、倉庫アプリによって発行されたイベントを処理し、必要に応じて通知されたイベントに対応することができます。</span><span class="sxs-lookup"><span data-stu-id="8fa7d-104">Batch jobs running in Supply Chain Management can use data from a queue for processing events issued by the warehouse app to react as needed to the signaled events.</span></span> <span data-ttu-id="8fa7d-105">この機能は、アプリを使用しているユーザーが実行する特定のタイプのアクションに応じて、関連するイベントをキューに追加します。</span><span class="sxs-lookup"><span data-stu-id="8fa7d-105">This feature add relevant events to the queue in response to certain types of actions taken by workers using the app.</span></span> <span data-ttu-id="8fa7d-106">たとえば、**倉庫アプリから作成および処理される移動オーダー**機能を使用する場合は、システムで**倉庫アプリのイベント処理**バッチ ジョブを実行しているときに、移動オーダー ヘッダーと明細行がバック エンドで作成および更新されます。</span><span class="sxs-lookup"><span data-stu-id="8fa7d-106">An example is when using the **Create and process transfer orders from the warehouse app** feature, the transfer order header and lines get created and updated in the back end when the system is running the **Process warehouse app events** batch job.</span></span>

## <a name="enable-the-process-warehouse-app-events-feature"></a><span data-ttu-id="8fa7d-107">倉庫アプリのイベント処理機能を有効にする</span><span class="sxs-lookup"><span data-stu-id="8fa7d-107">Enable the Process warehouse app events feature</span></span>

<span data-ttu-id="8fa7d-108">この機能を使用する前に、システム上で有効にする必要があります。</span><span class="sxs-lookup"><span data-stu-id="8fa7d-108">Before you can use this feature, it must be enabled on your system.</span></span> <span data-ttu-id="8fa7d-109">管理者は、[機能管理](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) ページを使用して、機能状態を確認し、必要に応じてそれを有効にすることができます。</span><span class="sxs-lookup"><span data-stu-id="8fa7d-109">Administrators can use the [feature management](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) page to check the feature status and enable it if needed.</span></span> <span data-ttu-id="8fa7d-110">倉庫アプリのイベント処理機能は次のように一覧表示されます。</span><span class="sxs-lookup"><span data-stu-id="8fa7d-110">The Process warehouse app events feature is listed as:</span></span>

- <span data-ttu-id="8fa7d-111">**モジュール** - 倉庫管理</span><span class="sxs-lookup"><span data-stu-id="8fa7d-111">**Module** - Warehouse management</span></span>
- <span data-ttu-id="8fa7d-112">**機能名** - 倉庫アプリのイベント処理</span><span class="sxs-lookup"><span data-stu-id="8fa7d-112">**Feature name** - Process warehouse app events</span></span>

## <a name="set-up-a-batch-job-to-process-warehouse-app-events"></a><span data-ttu-id="8fa7d-113">倉庫アプリのイベントを処理するためのバッチ ジョブを設定する</span><span class="sxs-lookup"><span data-stu-id="8fa7d-113">Set up a batch job to process warehouse app events</span></span>

### <a name="process-warehouse-app-events"></a><span data-ttu-id="8fa7d-114">倉庫アプリ イベントの処理</span><span class="sxs-lookup"><span data-stu-id="8fa7d-114">Process warehouse app events</span></span>

<span data-ttu-id="8fa7d-115">移動オーダーの作成と行の更新のための倉庫アプリ イベントを処理するために、スケジュールされたバッチ ジョブを設定します。</span><span class="sxs-lookup"><span data-stu-id="8fa7d-115">Set up a scheduled batch job to process the warehouse app events for the transfer order creation and line updates.</span></span>

1. <span data-ttu-id="8fa7d-116">**倉庫管理 \> 定期タスク \> 倉庫アプリのイベント処理**の順に移動します。</span><span class="sxs-lookup"><span data-stu-id="8fa7d-116">Go to **Warehouse management \> Periodic tasks \> Process warehouse app events**.</span></span>
1. <span data-ttu-id="8fa7d-117">倉庫アプリのイベント処理ダイアログ ボックスが開きます。</span><span class="sxs-lookup"><span data-stu-id="8fa7d-117">The Process warehouse app events dialog box opens.</span></span> <span data-ttu-id="8fa7d-118">**バックグラウンドで実行**クイックタブを展開し、**バッチ処理**を**はい**に設定します。</span><span class="sxs-lookup"><span data-stu-id="8fa7d-118">Expand the **Run in background** FastTab and set **Batch processing** to **Yes**.</span></span>
1. <span data-ttu-id="8fa7d-119">**バックグラウンドで実行**クイックタブで、**繰り返し**を選択します。</span><span class="sxs-lookup"><span data-stu-id="8fa7d-119">On the **Run in the background** FastTab, select **Recurrence**.</span></span>
1. <span data-ttu-id="8fa7d-120">**繰り返しの定義**ダイアログ ボックスが開きます。</span><span class="sxs-lookup"><span data-stu-id="8fa7d-120">The **Define recurrence** dialog box opens.</span></span> <span data-ttu-id="8fa7d-121">業務の要件に応じて実行スケジュールを設定します。</span><span class="sxs-lookup"><span data-stu-id="8fa7d-121">Set the run schedule as needed for your business.</span></span>
1. <span data-ttu-id="8fa7d-122">**OK** をクリックし、**倉庫アプリのイベント処理**ダイアログ ボックスに戻ります。</span><span class="sxs-lookup"><span data-stu-id="8fa7d-122">Select **OK** to return to the **Process warehouse app events** dialog box.</span></span>
1. <span data-ttu-id="8fa7d-123">**倉庫アプリのイベント処理**ダイアログ ボックスで **OK** を選択し、バッチ ジョブをバッチ キューに追加します。</span><span class="sxs-lookup"><span data-stu-id="8fa7d-123">Select **OK** in the **Process warehouse app events** dialog box to add the batch job to the batch queue.</span></span>

## <a name="query-warehouse-app-events"></a><span data-ttu-id="8fa7d-124">倉庫アプリ イベントのクエリ</span><span class="sxs-lookup"><span data-stu-id="8fa7d-124">Query warehouse app events</span></span>

<span data-ttu-id="8fa7d-125">倉庫アプリによって生成されたイベント キューとイベント メッセージを表示するには、**倉庫管理 \> 照会およびレポート \> モバイル デバイスのログ \> 倉庫アプリのイベント**の順に移動します。</span><span class="sxs-lookup"><span data-stu-id="8fa7d-125">You can view the event queue and events messages generated by the warehouse app by going to **Warehouse management \> Inquiries and reports \> Mobile device logs \> Warehouse app events**.</span></span>

## <a name="the-standard-event-queue-process"></a><span data-ttu-id="8fa7d-126">標準のイベント キュー プロセス</span><span class="sxs-lookup"><span data-stu-id="8fa7d-126">The standard event queue process</span></span>

<span data-ttu-id="8fa7d-127">倉庫アプリのイベント キューは、通常、次の説明のフローで使用されます。</span><span class="sxs-lookup"><span data-stu-id="8fa7d-127">The warehouse apps events queue will typically be used with the following described flow:</span></span>

1. <span data-ttu-id="8fa7d-128">イベント メッセージを使用して、イベントがキューに追加されます。</span><span class="sxs-lookup"><span data-stu-id="8fa7d-128">An event gets added to the queue  with an event message.</span></span> <span data-ttu-id="8fa7d-129">新しいメッセージには最初、**待機中**のイベントの状態が含まれます。このメッセージは、**倉庫アプリのイベント処理**バッチ ジョブによって取得および処理されることはありません。</span><span class="sxs-lookup"><span data-stu-id="8fa7d-129">The new message initially has an Event state of **Waiting**, which means that the **Process warehouse app events** batch job will not pick up and process this message.</span></span>
1. <span data-ttu-id="8fa7d-130">メッセージの状態が**キューに設定**に更新されるとすぐに、**倉庫アプリの処理**イベント バッチ ジョブによってイベントが取得および処理されます。</span><span class="sxs-lookup"><span data-stu-id="8fa7d-130">As soon as the message state is updated to **Queued**, the **Process warehouse app** events batch job will pick up and process the event.</span></span>
1. <span data-ttu-id="8fa7d-131">バッチ ジョブは、要求された処理が可能かどうかに応じて、イベントの状態を**完了**または**失敗**に更新します。</span><span class="sxs-lookup"><span data-stu-id="8fa7d-131">The batch job updates the event states to either **Completed** or **Failed**, depending on whether the requested process was possible.</span></span>
1. <span data-ttu-id="8fa7d-132">すべての関連するイベント メッセージが**完了**になると、そのイベントがキューから削除されます。</span><span class="sxs-lookup"><span data-stu-id="8fa7d-132">When all the related event messages are **Completed**, the event is deleted from the queue.</span></span>

 <span data-ttu-id="8fa7d-133">詳細な例については、「[倉庫アプリから移動オーダーを作成のプロセス](create-transfer-order-from-warehouse-app.md)」を参照してください。</span><span class="sxs-lookup"><span data-stu-id="8fa7d-133">For a detailed example, see [Create transfer order from warehouse app process](create-transfer-order-from-warehouse-app.md).</span></span>

## <a name="handle-event-errors"></a><span data-ttu-id="8fa7d-134">イベント エラーの処理</span><span class="sxs-lookup"><span data-stu-id="8fa7d-134">Handle event errors</span></span>

<span data-ttu-id="8fa7d-135">倉庫イベント処理の一部として、要求されたメッセージ活動がバッチ ジョブからプロセスを受け取らないことがあります。</span><span class="sxs-lookup"><span data-stu-id="8fa7d-135">As part of the warehouse event processing, the requested message activity may not receive processes from the batch job.</span></span> <span data-ttu-id="8fa7d-136">この場合、イベント メッセージは**失敗**に変更されます。</span><span class="sxs-lookup"><span data-stu-id="8fa7d-136">In this case, the event message will change to **Failed**.</span></span> <span data-ttu-id="8fa7d-137">**バッチ ログ**情報を使用して理由を確認し、問題を修正するために必要なアクションを実行できます。</span><span class="sxs-lookup"><span data-stu-id="8fa7d-137">You can use the **Batch log** information to learn why and take needed action to correct any problems.</span></span>

<span data-ttu-id="8fa7d-138">詳細な例については、「[倉庫アプリから移動オーダーを作成](create-transfer-order-from-warehouse-app.md)」を参照してください。</span><span class="sxs-lookup"><span data-stu-id="8fa7d-138">For a detailed example, see [Create transfer order from warehouse app](create-transfer-order-from-warehouse-app.md).</span></span>

<span data-ttu-id="8fa7d-139">失敗した倉庫アプリのイベント メッセージをリセットするには、次の操作を行います。</span><span class="sxs-lookup"><span data-stu-id="8fa7d-139">To reset a failed warehouse app event message:</span></span>

1. <span data-ttu-id="8fa7d-140">**倉庫管理 \> 照会およびレポート \> モバイル デバイスのログ \> 倉庫アプリのイベント**の順に移動します。</span><span class="sxs-lookup"><span data-stu-id="8fa7d-140">Go to **Warehouse management \> Inquiries and reports \> Mobile device logs \> Warehouse app events**.</span></span>
1. <span data-ttu-id="8fa7d-141">**倉庫アプリ イベントのメッセージ** クイックタブで、**イベントの状態**列で**失敗**を表示している関連イベントを見つけて選択します。</span><span class="sxs-lookup"><span data-stu-id="8fa7d-141">On the **Warehouse app event messages** FastTab, find and select a relevant event that is showing **Failed** in the **Event state** column.</span></span>
1. <span data-ttu-id="8fa7d-142">**倉庫アプリ イベントのメッセージ** ツールバーで**リセット**を選択します。</span><span class="sxs-lookup"><span data-stu-id="8fa7d-142">Select **Reset** from the **Warehouse app event messages** toolbar.</span></span>
1. <span data-ttu-id="8fa7d-143">該当するすべてのメッセージがリセットされるまで作業を続行します。</span><span class="sxs-lookup"><span data-stu-id="8fa7d-143">Continue working until all relevant messages are reset.</span></span>

<span data-ttu-id="8fa7d-144">また、**倉庫アプリ イベントのメッセージ** ツールバーの**削除**オプションを使用して、**失敗**したイベント メッセージを削除することもできます。</span><span class="sxs-lookup"><span data-stu-id="8fa7d-144">You can also remove a **Failed** event message by using the **Delete** option on the **Warehouse app event messages** toolbar.</span></span>
