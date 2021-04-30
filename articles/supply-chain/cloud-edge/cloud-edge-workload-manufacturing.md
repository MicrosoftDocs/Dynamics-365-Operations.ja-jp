---
title: クラウドおよびエッジのスケール ユニットの製造実行ワークロード
description: このトピックでは、製造実行ワークロードが クラウドおよびエッジのスケール ユニットと機能する方法について説明します。
author: cabeln
ms.date: 10/06/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: kamaybac
ms.custom: ''
ms.assetid: ''
ms.search.region: global
ms.search.industry: SCM
ms.author: cabeln
ms.search.validFrom: 2020-10-06
ms.dyn365.ops.version: 10.0.15
ms.openlocfilehash: a6d6979093c67d2d89b88678712f4c0205c63194
ms.sourcegitcommit: 639175a39da38edd13e21eeb5a1a5ca62fa44d99
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/15/2021
ms.locfileid: "5899098"
---
# <a name="manufacturing-execution-workloads-for-cloud-and-edge-scale-units"></a><span data-ttu-id="b865a-103">クラウドおよびエッジのスケール ユニットに対する製造実行ワークロード</span><span class="sxs-lookup"><span data-stu-id="b865a-103">Manufacturing execution workloads for cloud and edge scale units</span></span>

[!include [banner](../includes/banner.md)]
[!include [preview banner](../includes/preview-banner.md)]

> [!WARNING]
> <span data-ttu-id="b865a-104">製造実行ワークロードは、現時点ではプレビューで使用できます。</span><span class="sxs-lookup"><span data-stu-id="b865a-104">The manufacturing execution workload is available in preview at this point in time.</span></span>
> <span data-ttu-id="b865a-105">ワークロード スケール ユニットで使用されている場合は、すべてのビジネス機能がパブリック プレビューで完全にサポートされているわけではありません。</span><span class="sxs-lookup"><span data-stu-id="b865a-105">Some business functionality isn't fully supported in the public preview when workload scale units are used.</span></span>

<span data-ttu-id="b865a-106">製造実行では、スケール ユニットは以下の機能を提供します。</span><span class="sxs-lookup"><span data-stu-id="b865a-106">In manufacturing execution, scale units deliver the following capabilities:</span></span>

- <span data-ttu-id="b865a-107">機械オペレーターと作業現場監督は、運用生産計画にアクセスできます。</span><span class="sxs-lookup"><span data-stu-id="b865a-107">Machine operators and shop floor supervisors can access the operational production plan.</span></span>
- <span data-ttu-id="b865a-108">機械オペレーターは、個々の製造ジョブを実行することによって、計画を最新の状態に保つことができます。</span><span class="sxs-lookup"><span data-stu-id="b865a-108">Machine operators can keep the plan up to date by running discrete and process manufacturing jobs.</span></span>
- <span data-ttu-id="b865a-109">作業現場の監修者は、運用計画を調整できます。</span><span class="sxs-lookup"><span data-stu-id="b865a-109">The shop floor supervisor can adjust the operational plan.</span></span>
- <span data-ttu-id="b865a-110">作業者は、出勤と出勤の出勤と退勤をエッジで確認して、作業者の支払計算を正しく行うことができます。</span><span class="sxs-lookup"><span data-stu-id="b865a-110">Workers can access time and attendance for clock-in and clock-out on the edge, to ensure correct worker pay calculation.</span></span>

<span data-ttu-id="b865a-111">このトピックでは、製造実行ワークロードが クラウドおよびエッジのスケール ユニットと機能する方法について説明します。</span><span class="sxs-lookup"><span data-stu-id="b865a-111">This topic describes how manufacturing execution workloads work with cloud and edge scale units.</span></span>

## <a name="the-manufacturing-lifecycle"></a><span data-ttu-id="b865a-112">製造ライフサイクル</span><span class="sxs-lookup"><span data-stu-id="b865a-112">The manufacturing lifecycle</span></span>

<span data-ttu-id="b865a-113">次の図に示すように、製造ライフサイクルは、*計画*、*実行*、*確定* の 3 つのフェーズに分かれています。</span><span class="sxs-lookup"><span data-stu-id="b865a-113">As the following illustration shows, the manufacturing lifecycle is divided into three phases: *Plan*, *Execute*, and *Finalize*.</span></span>

<span data-ttu-id="b865a-114">[![単一の環境を使用する場合の製造実行フェーズ](media/mes-phases.png "単一の環境を使用する場合の製造実行フェーズ")](media/mes-phases-large.png)</span><span class="sxs-lookup"><span data-stu-id="b865a-114">[![Manufacturing execution phases when a single environment is used](media/mes-phases.png "Manufacturing execution phases when a single environment is used")](media/mes-phases-large.png)</span></span>

<span data-ttu-id="b865a-115">_計画_ フェーズには、製品定義、計画、注文の作成、スケジューリング、リリースが含まれます。</span><span class="sxs-lookup"><span data-stu-id="b865a-115">The _Plan_ phase includes product definition, planning, order creation and scheduling, and release.</span></span> <span data-ttu-id="b865a-116">このリリース手順は、_計画_ フェーズから _実行_ フェーズへの移行を示します。</span><span class="sxs-lookup"><span data-stu-id="b865a-116">The release step indicates the transition from the _Plan_ phase to the _Execute_ phase.</span></span> <span data-ttu-id="b865a-117">製造オーダーをリリースすると、製造オーダー ジョブが生産現場に表示され、実行できるようになります。</span><span class="sxs-lookup"><span data-stu-id="b865a-117">When a production order is released, the production order jobs will be visible on the production floor and ready for execution.</span></span>

<span data-ttu-id="b865a-118">生産ジョブが完了とマークされている場合は、_実行_ フェーズから _確定_ フェーズに進みます。</span><span class="sxs-lookup"><span data-stu-id="b865a-118">When a production job is marked as completed, it moves from the _Execute_ phase to the _Finalize_ phase.</span></span> <span data-ttu-id="b865a-119">_確定_ フェーズでは、*実行* フェーズからの登録は、計算、承認、転送される承認ワークフローを通過します。</span><span class="sxs-lookup"><span data-stu-id="b865a-119">In the _Finalize_ phase, the registrations from the *Execute* phase go through an approval workflow, where they are calculated, approved, and transferred.</span></span> <span data-ttu-id="b865a-120">その時点で、製造オーダーが完了します。</span><span class="sxs-lookup"><span data-stu-id="b865a-120">At that point, the production order is completed.</span></span> <span data-ttu-id="b865a-121">したがって、作業者の支払の基礎が生成されます。</span><span class="sxs-lookup"><span data-stu-id="b865a-121">Therefore, the basis for the workers' pay is generated.</span></span>

## <a name="splitting-the-execute-phase-into-a-separate-workload"></a><span data-ttu-id="b865a-122">実行フェーズの別のワークロードへの分割</span><span class="sxs-lookup"><span data-stu-id="b865a-122">Splitting the Execute phase into a separate workload</span></span>

<span data-ttu-id="b865a-123">次の図に示すように、スケール ユニットを使用すると、_実行_ フェーズが別のワークロードとして分割されます。</span><span class="sxs-lookup"><span data-stu-id="b865a-123">As the following illustration shows, when scale units are used, the _Execute_ phase is split out as a separate workload.</span></span>

<span data-ttu-id="b865a-124">[![スケール ユニットが使用されている場合の製造実行フェーズ](media/mes-phases-workloads.png "スケール ユニットが使用されている場合の製造実行フェーズ")](media/mes-phases-workloads-large.png)</span><span class="sxs-lookup"><span data-stu-id="b865a-124">[![Manufacturing execution phases when scale units are used](media/mes-phases-workloads.png "Manufacturing execution phases when scale units are used")](media/mes-phases-workloads-large.png)</span></span>

<span data-ttu-id="b865a-125">このモデルでは、シングル インスタンス インストールから、ハブとスケール ユニットに基づくモデルに移動します。</span><span class="sxs-lookup"><span data-stu-id="b865a-125">The model now goes from a single-instance installation to a model that is based on the hub and scale units.</span></span> <span data-ttu-id="b865a-126">_計画_ フェーズと _確定_ フェーズは、ハブ上のバックオフィス動作として実行し、製造実行ワークロードはスケール ユニット上で実行します。</span><span class="sxs-lookup"><span data-stu-id="b865a-126">The _Plan_ and _Finalize_ phases run as back-office operations on the hub, and the manufacturing execution workload runs on the scale units.</span></span> <span data-ttu-id="b865a-127">データは、ハブとスケール ユニットの間で非同期に転送されます。</span><span class="sxs-lookup"><span data-stu-id="b865a-127">Data is transferred asynchronously between the hub and scale units.</span></span>

<span data-ttu-id="b865a-128">製造オーダーがハブでリリースされると、生産ジョブを処理するために必要なすべてのデータがスケール ユニットに転送されます。</span><span class="sxs-lookup"><span data-stu-id="b865a-128">When a production order is released on the hub, all data that is required to process production jobs is transferred to the scale unit.</span></span> <span data-ttu-id="b865a-129">このデータには、製造オーダー、生産工順、部品表、製品が含まれます。</span><span class="sxs-lookup"><span data-stu-id="b865a-129">This data includes production orders, production routes, bills of materials, and products.</span></span> <span data-ttu-id="b865a-130">製造オーダーに関連しないデータ (間接活動、休暇コード、生産パラメータなど) も、ハブからスケール ユニットに転送されます。</span><span class="sxs-lookup"><span data-stu-id="b865a-130">Data that isn't related to a production order (such as indirect activities, absence codes, and production parameters) is also transferred from the hub to the scale unit.</span></span> <span data-ttu-id="b865a-131">原則として、ハブから取得され、スケール ユニットに転送されたデータは、ハブでのみ作成または更新できます。</span><span class="sxs-lookup"><span data-stu-id="b865a-131">As a rule, data that originates from the hub and that is transferred to the scale unit can be created or updated only on the hub.</span></span> <span data-ttu-id="b865a-132">たとえば、新しい休暇コードや間接活動をスケール ユニットで作成することはできず、&mdash;これは登録に対してのみ使用できます。</span><span class="sxs-lookup"><span data-stu-id="b865a-132">For example, a new absence code or indirect activity can't be created on the scale unit&mdash;they can be used only for registration.</span></span> <span data-ttu-id="b865a-133">実行時にスケール ユニットで行われた登録がハブに転送され、その後、時刻と出勤の承認、在庫、財務の更新が処理されます。</span><span class="sxs-lookup"><span data-stu-id="b865a-133">The registrations that are made on the scale unit during execution are then transferred to the hub, where time and attendance approval, inventory, and financial updates are processed.</span></span>

## <a name="manufacturing-execution-tasks-that-can-be-run-on-workloads"></a><span data-ttu-id="b865a-134">ワークロードに対して実行できる製造実行タスク</span><span class="sxs-lookup"><span data-stu-id="b865a-134">Manufacturing execution tasks that can be run on workloads</span></span>

<span data-ttu-id="b865a-135">スケール ユニットが使用されている場合、次の製造実行タスクをワークロードで実行できます。</span><span class="sxs-lookup"><span data-stu-id="b865a-135">The following manufacturing execution tasks can currently be run on workloads when scale units are used:</span></span>

- <span data-ttu-id="b865a-136">出勤、ログイン、退勤、および休暇</span><span class="sxs-lookup"><span data-stu-id="b865a-136">Clock-in, log-in, clock-out, and absence</span></span>
- <span data-ttu-id="b865a-137">ジョブの開始</span><span class="sxs-lookup"><span data-stu-id="b865a-137">Start job</span></span>
- <span data-ttu-id="b865a-138">ジョブのバンドル</span><span class="sxs-lookup"><span data-stu-id="b865a-138">Bundle jobs</span></span>
- <span data-ttu-id="b865a-139">進捗状況のレポート</span><span class="sxs-lookup"><span data-stu-id="b865a-139">Report progress</span></span>
- <span data-ttu-id="b865a-140">仕損のレポート</span><span class="sxs-lookup"><span data-stu-id="b865a-140">Report scrap</span></span>
- <span data-ttu-id="b865a-141">間接活動</span><span class="sxs-lookup"><span data-stu-id="b865a-141">Indirect activity</span></span>
- <span data-ttu-id="b865a-142">分割</span><span class="sxs-lookup"><span data-stu-id="b865a-142">Break</span></span>

## <a name="working-with-manufacturing-execution-workloads-on-the-hub"></a><span data-ttu-id="b865a-143">ハブでの製造実行ワークロードで作業します</span><span class="sxs-lookup"><span data-stu-id="b865a-143">Working with manufacturing execution workloads on the hub</span></span>

<span data-ttu-id="b865a-144">通常、製造実行ワークロードの実行に必要なプロセスは、ハブとすべてのスケール ユニットを必要に応じて同期するように自動的に実行されます。</span><span class="sxs-lookup"><span data-stu-id="b865a-144">Usually, the processes that are required to run manufacturing execution workloads run automatically to keep the hub and all the scale units in sync, as needed.</span></span> <span data-ttu-id="b865a-145">ただし、問題が発生した場合は、ワークロードから受信した作業登録の処理を手動でトリガーするか、登録処理ログを確認することができます。</span><span class="sxs-lookup"><span data-stu-id="b865a-145">However, if you're having trouble, you can manually trigger the processing of raw registrations that are received from workloads and/or check the registration processing log.</span></span>

### <a name="manually-process-raw-registrations"></a><span data-ttu-id="b865a-146">作業登録の手動処理</span><span class="sxs-lookup"><span data-stu-id="b865a-146">Manually process raw registrations</span></span>

<span data-ttu-id="b865a-147">Supply Chain Management のバッチ ジョブは、ワークロードから受信したすべての登録を処理するために自動的に実行されます。</span><span class="sxs-lookup"><span data-stu-id="b865a-147">A batch job in Supply Chain Management runs automatically to process all the registrations that have been received from the workloads.</span></span> <span data-ttu-id="b865a-148">このジョブでは、ワークロードで完了したジョブに対して登録が処理されるときに、必要な生産仕訳帳とログ ブックのエントリが作成されます。</span><span class="sxs-lookup"><span data-stu-id="b865a-148">This job creates the required production journals and logbook entries when a registration is processed for a completed job on the workload.</span></span>

<span data-ttu-id="b865a-149">通常、ジョブは自動的に実行されますが、ハブにログインして、**生産制御 \> 定期タスク \> バックオフィスのワークロード管理 \> プロセス作業登録** に移動することで、いつでも手動で実行することができます。</span><span class="sxs-lookup"><span data-stu-id="b865a-149">Although the job usually runs automatically, you can run it manually at any time by signing in to the hub and going to **Production control \> Periodic tasks \> Backoffice workload management \> Process raw registrations**.</span></span>

### <a name="check-the-raw-registration-processing-log"></a><span data-ttu-id="b865a-150">未処理の登録処理ログの確認</span><span class="sxs-lookup"><span data-stu-id="b865a-150">Check the raw registration processing log</span></span>

<span data-ttu-id="b865a-151">登録処理のログを確認するには、ハブにログインし、**生産管理 \> 定期タスク \> バックオフィス ワークロード管理 \> 作業登録処理ログ** に移動します。</span><span class="sxs-lookup"><span data-stu-id="b865a-151">To review the registration processing log, sign in to the hub, and go to **Production control \> Periodic tasks \> Backoffice workload management \> Raw registration processing log**.</span></span> <span data-ttu-id="b865a-152">**作業登録処理ログ** ページには、処理済の作業登録の一覧と各登録のステータスが表示されます。</span><span class="sxs-lookup"><span data-stu-id="b865a-152">The **Raw registration processing log** page shows a list of processed raw registrations and the status of each registration.</span></span>

<span data-ttu-id="b865a-153">![作業登録処理のログ ページ](media/mes-processing-log.png "作業登録処理のログ ページ")</span><span class="sxs-lookup"><span data-stu-id="b865a-153">![Raw registration processing log page](media/mes-processing-log.png "Raw registration processing log page")</span></span>

<span data-ttu-id="b865a-154">一覧で登録を選択し、アクション ペインで次のいずれかのボタンを選択することによって、登録を行うことができます。</span><span class="sxs-lookup"><span data-stu-id="b865a-154">You can work on any registration in the list by selecting it and then selecting one of the following buttons on the Action Pane:</span></span>

- <span data-ttu-id="b865a-155">**プロセス** - 選択した登録を手動で処理します。</span><span class="sxs-lookup"><span data-stu-id="b865a-155">**Process** – Manually process the selected registration.</span></span> <span data-ttu-id="b865a-156">このアクションは、_作業登録の処理_ ジョブが実行されていないか、ジョブが失敗した場合に役立ちます。</span><span class="sxs-lookup"><span data-stu-id="b865a-156">This action can be useful if the _Process raw registrations_ job hasn't run, or if it failed.</span></span>
- <span data-ttu-id="b865a-157">**キャンセル** - 選択した登録をキャンセルします。</span><span class="sxs-lookup"><span data-stu-id="b865a-157">**Cancel** – Cancel the selected registration.</span></span>

## <a name="working-with-manufacturing-execution-workloads-on-a-scale-unit"></a><span data-ttu-id="b865a-158">スケール ユニットでの製造実行ワークロードの作業</span><span class="sxs-lookup"><span data-stu-id="b865a-158">Working with manufacturing execution workloads on a scale unit</span></span>

<span data-ttu-id="b865a-159">通常、製造実行ワークロードの実行に必要なプロセスは、ハブとすべてのスケール ユニットを必要に応じて同期するように自動的に実行されます。</span><span class="sxs-lookup"><span data-stu-id="b865a-159">Usually, the processes that are required to run manufacturing execution workloads run automatically to keep the hub and all the scale units in sync, as needed.</span></span> <span data-ttu-id="b865a-160">ただし、問題が発生した場合は、スケール ユニットで処理された注文の履歴を確認するか、手動で _製造ハブからスケール ユニットへのメッセージ プロセッサ_ ジョブに実行します。</span><span class="sxs-lookup"><span data-stu-id="b865a-160">However, if you're having trouble, you can check the history of orders that have been processed on a scale unit or manually run the _Manufacturing hub to scale unit message processor_ job.</span></span>

### <a name="view-the-history-of-manufacturing-jobs-that-have-been-processed-on-a-scale-unit"></a><span data-ttu-id="b865a-161">スケール ユニットで処理された製造ジョブの履歴を表示します</span><span class="sxs-lookup"><span data-stu-id="b865a-161">View the history of manufacturing jobs that have been processed on a scale unit</span></span>

<span data-ttu-id="b865a-162">スケール ユニットで処理された製造ジョブの履歴を確認するには、スケール ユニット マシンにログインして、**生産管理 \> 定期タスク \> バックオフィスのワークロード管理 \> 製造ジョブの処理履歴** に移動します。</span><span class="sxs-lookup"><span data-stu-id="b865a-162">To review the history of manufacturing jobs that have been processed on a scale unit, sign in to the scale unit machine, and go to **Production control \> Periodic tasks \> Backoffice workload management \> Manufacturing jobs processing history**.</span></span> <span data-ttu-id="b865a-163">**製造ジョブ処理履歴** ページには、スケール ユニットでの製造オーダーの処理履歴が表示されます。</span><span class="sxs-lookup"><span data-stu-id="b865a-163">The **Manufacturing jobs processing history** page shows the processing history of the production orders on the scale unit.</span></span> <span data-ttu-id="b865a-164">一覧からそれを選択して、その後アクション ペインで次のいずれかのボタンを選択することによって、製造オーダー上で作業できます。</span><span class="sxs-lookup"><span data-stu-id="b865a-164">You can work on any production order in the list by selecting it and then selecting one of the following buttons on the Action Pane:</span></span>

- <span data-ttu-id="b865a-165">**プロセス** - 選択した製造オーダーを手動で処理します。</span><span class="sxs-lookup"><span data-stu-id="b865a-165">**Process** – Manually process the selected production order.</span></span>
- <span data-ttu-id="b865a-166">**キャンセル** - 選択した製造オーダーをキャンセルします。</span><span class="sxs-lookup"><span data-stu-id="b865a-166">**Cancel** – Cancel the selected production order.</span></span>

### <a name="manufacturing-hub-to-scale-unit-message-processor-job"></a><span data-ttu-id="b865a-167">製造ハブからスケール ユニットへのメッセージ プロセッサ ジョブ</span><span class="sxs-lookup"><span data-stu-id="b865a-167">Manufacturing hub to scale unit message processor job</span></span>

<span data-ttu-id="b865a-168">_製造ハブからスケール ユニットへのメッセージ プロセッサ_ ジョブは、ハブのデータをスケール ユニットに処理します。</span><span class="sxs-lookup"><span data-stu-id="b865a-168">The _Manufacturing hub to scale unit message processor_ job processes data from the hub to the scale unit.</span></span> <span data-ttu-id="b865a-169">このジョブは、製造実行ワークロードがデプロイされると自動的に開始されます。</span><span class="sxs-lookup"><span data-stu-id="b865a-169">This job is automatically started when the manufacturing execution workload is deployed.</span></span> <span data-ttu-id="b865a-170">ただし、これは、**生産管理 \> 定期タスク \> バックオフィス ワークロード管理 \> 製造ハブからスケール ユニットへのメッセージ プロセッサ** に移動することで、いつでも手動で実行できます。</span><span class="sxs-lookup"><span data-stu-id="b865a-170">However, you can run it manually at any time by going to **Production control \> Periodic tasks \> Backoffice workload management \> Manufacturing hub to scale unit message processor**.</span></span>

[!INCLUDE [cloud-edge-privacy-notice](../../includes/cloud-edge-privacy-notice.md)]

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
