---
title: バッチ処理とバッチ サーバー
description: このトピックでは、バッチ処理とバッチ サーバー、およびその使用を計画する方法について説明します。
author: maertenm
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-platform
ms.technology: ''
audience: IT Pro
ms.reviewer: sericks
ms.search.scope: Core, Operations
ms.custom: 57201
ms.assetid: 22a56b7d-4e07-4161-8416-0cac4a0b65a2
ms.search.region: Global
ms.author: maertenm
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 12bdb89602793d1fa2bd22585f0c33270b57c3c3
ms.sourcegitcommit: 3ba95d50b8262fa0f43d4faad76adac4d05eb3ea
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 09/27/2019
ms.locfileid: "2191799"
---
# <a name="batch-processing-and-batch-servers"></a><span data-ttu-id="6c6a7-103">バッチ処理とバッチ サーバー</span><span class="sxs-lookup"><span data-stu-id="6c6a7-103">Batch processing and batch servers</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="6c6a7-104">このトピックでは、バッチ処理とバッチ サーバー、およびその使用を計画する方法について説明します。</span><span class="sxs-lookup"><span data-stu-id="6c6a7-104">This topic describes batch processing and batch servers, and how to plan for their use.</span></span>

<span data-ttu-id="6c6a7-105">バッチ フレームワークは、Application Object Server (AOS) の複数のインスタンスにわたるタスクを処理できるサーバー ベースの非同期バッチ処理環境を提供します。</span><span class="sxs-lookup"><span data-stu-id="6c6a7-105">The batch framework provides an asynchronous, server-based batch processing environment that can process tasks across multiple instances of Application Object Server (AOS).</span></span> 

<span data-ttu-id="6c6a7-106">バッチ フレームワークの次のような側面について、よく理解しておく必要があります。</span><span class="sxs-lookup"><span data-stu-id="6c6a7-106">You should become familiar with the following aspects of the batch framework:</span></span>

-   <span data-ttu-id="6c6a7-107">**バッチ ジョブ**は、特定の目標を達成するために使用されるプロセスです。</span><span class="sxs-lookup"><span data-stu-id="6c6a7-107">A **batch job** is a process that is used to achieve a specific goal.</span></span> <span data-ttu-id="6c6a7-108">バッチ ジョブは、1 つまたは複数のバッチ タスクで構成されます。</span><span class="sxs-lookup"><span data-stu-id="6c6a7-108">A batch job consists of one or more batch tasks.</span></span>
-   <span data-ttu-id="6c6a7-109">**バッチ タスク**は、バッチ ジョブによって実行される活動です。</span><span class="sxs-lookup"><span data-stu-id="6c6a7-109">A **batch task** is an activity that is run by a batch job.</span></span> <span data-ttu-id="6c6a7-110">複数の種類の依存関係を持つバッチ タスクをバッチ ジョブに追加することができます。</span><span class="sxs-lookup"><span data-stu-id="6c6a7-110">You can add batch tasks that have multiple types of dependencies to a batch job.</span></span> <span data-ttu-id="6c6a7-111">また、それぞれがタスクを実行する、複数のスレッドを実行するように AOS インスタンスを構成することができます。</span><span class="sxs-lookup"><span data-stu-id="6c6a7-111">You can also configure AOS instances to run multiple threads, each of which runs a task.</span></span> <span data-ttu-id="6c6a7-112">実行を待機しているすべてのバッチ タスクはバッチ サーバーとしてコンフィギュレーションされている使用可能なすべての AOS インスタンスによって実行できます。</span><span class="sxs-lookup"><span data-stu-id="6c6a7-112">All batch tasks that are waiting to be run can be run by any available AOS instance that is configured as a batch server.</span></span> <span data-ttu-id="6c6a7-113">スループットを向上させ、全体の実行時間を短縮するには、バッチ ジョブを多数のタスクとして定義し、バッチ サーバーを使用して使用可能なすべての AOS インスタンスに対してタスクを実行します。</span><span class="sxs-lookup"><span data-stu-id="6c6a7-113">To improve throughput and reduce overall execution time, you can define a batch job as many tasks and then use a batch server to run the tasks against all available AOS instances.</span></span>
-   <span data-ttu-id="6c6a7-114">**バッチ グループ**は、バッチ タスクの属性です。</span><span class="sxs-lookup"><span data-stu-id="6c6a7-114">A **batch group** is an attribute of a batch task.</span></span> <span data-ttu-id="6c6a7-115">バッチ グループは、管理者がタスクを実行する AOS インスタンスを決定または指定することを可能にします。</span><span class="sxs-lookup"><span data-stu-id="6c6a7-115">A batch group lets the administrator determine or specify which AOS instance runs the task.</span></span> <span data-ttu-id="6c6a7-116">新しいタスクを作成するとき、そのタスクは既定のバッチ グループに配置されます。</span><span class="sxs-lookup"><span data-stu-id="6c6a7-116">When you create a new task, it's put in the default batch group.</span></span> <span data-ttu-id="6c6a7-117">すべてのバッチ サーバーは、任意のジョブから既定のバッチ グループおよび待機中のタスクをプロセスするためにコンフィギュレーションされています。</span><span class="sxs-lookup"><span data-stu-id="6c6a7-117">All batch servers are configured to process the default batch group and the waiting tasks from any job.</span></span> <span data-ttu-id="6c6a7-118">また、名前付きバッチ グループを作成して、そのバッチ グループと特定の AOS インスタンスの間のアフィニティを設定できます。</span><span class="sxs-lookup"><span data-stu-id="6c6a7-118">Additionally, you can create a named batch group, and then set an affinity between that batch group and specific AOS instances.</span></span> <span data-ttu-id="6c6a7-119">アフィニティを作成した後は、指定された AOS インスタンスのみが名前付きバッチ グループのタスクを処理することができ、 AOS インスタンスは指定された名前付きバッチ グループからのみタスクを処理することができます。</span><span class="sxs-lookup"><span data-stu-id="6c6a7-119">After you create this affinity, only the specified AOS instances will process tasks from the named batch group, and those AOS instances will process tasks from the named batch group only.</span></span> <span data-ttu-id="6c6a7-120">また、バッチ グループが必要な場合、既定のバッチ グループを構成済みサーバーに追加することができます。</span><span class="sxs-lookup"><span data-stu-id="6c6a7-120">You can also add the default batch group to the configured servers, if that batch group is required.</span></span>

## <a name="batch-server-topology-planning"></a><span data-ttu-id="6c6a7-121">バッチ サーバーのトポロジ計画</span><span class="sxs-lookup"><span data-stu-id="6c6a7-121">Batch server topology planning</span></span>
<span data-ttu-id="6c6a7-122">バッチ サーバーの能力は、AOS インスタンスで同時に実行できるスレッドの最大数に基づいています。</span><span class="sxs-lookup"><span data-stu-id="6c6a7-122">The capacity of a batch server is based on the maximum number of threads that can run concurrently on the AOS instance.</span></span> <span data-ttu-id="6c6a7-123">各スレッドは、1 つのバッチ タスクを実行します。</span><span class="sxs-lookup"><span data-stu-id="6c6a7-123">Each thread runs one batch task.</span></span> <span data-ttu-id="6c6a7-124">タスク間またはタスク内に複雑な依存関係を追加することができます。</span><span class="sxs-lookup"><span data-stu-id="6c6a7-124">You can add complex dependencies between or among tasks.</span></span> <span data-ttu-id="6c6a7-125">これらのタスクは、ビジネス ロジックおよび要件に基づき、シリアル ステップまたはパラレル ステップで実行することができます。</span><span class="sxs-lookup"><span data-stu-id="6c6a7-125">You can run these tasks in serial steps or parallel steps, depending on the business logic and requirements.</span></span> <span data-ttu-id="6c6a7-126">依存関係を持っていないすべてのタスクは並列タスクと見なされます。</span><span class="sxs-lookup"><span data-stu-id="6c6a7-126">All tasks that don't have any dependencies are considered parallel tasks.</span></span> <span data-ttu-id="6c6a7-127">バッチ サーバーとしてコンフィギュレーションされている AOS インスタンスは、処理を待機しているタスクを定期的に確認します。</span><span class="sxs-lookup"><span data-stu-id="6c6a7-127">AOS instances that are configured as batch servers periodically check for tasks that are waiting to be processed.</span></span> <span data-ttu-id="6c6a7-128">バッチ サーバーは、各並列タスクをスレッドに割り当て、そのスレッドの処理を開始します。</span><span class="sxs-lookup"><span data-stu-id="6c6a7-128">The batch server assigns each parallel task to a thread and starts to process the thread.</span></span> 

<span data-ttu-id="6c6a7-129">複数の AOS インスタンス間で複数のスレッドを実行することができます。</span><span class="sxs-lookup"><span data-stu-id="6c6a7-129">You can run multiple threads across multiple AOS instances.</span></span> <span data-ttu-id="6c6a7-130">各 AOS インスタンスは、構成設定で定義されているキャパシティに応じて、複数のスレッドを自動的に実行します。</span><span class="sxs-lookup"><span data-stu-id="6c6a7-130">Each AOS instance automatically runs multiple threads, depending on that capacity that is defined in the configuration settings.</span></span> <span data-ttu-id="6c6a7-131">したがって、ジョブからの並列タスクは、複数の AOS インスタンスにわたって複数のスレッドで実行できます。</span><span class="sxs-lookup"><span data-stu-id="6c6a7-131">Therefore, parallel tasks from a job can be run on multiple threads across multiple AOS instances.</span></span>

<span data-ttu-id="6c6a7-132">バッチ サーバーは、1 分間に 1 回使用可能なスレッドをチェックします。</span><span class="sxs-lookup"><span data-stu-id="6c6a7-132">A batch server checks for available threads one time per minute.</span></span> <span data-ttu-id="6c6a7-133">したがって、待機中のタスクが使用可能なスレッドで処理されるのを確認するまで、少し待たなければならない場合があります。</span><span class="sxs-lookup"><span data-stu-id="6c6a7-133">Therefore, you might have to wait for a minute before you see that a waiting task is picked up for processing by an available thread.</span></span>

## <a name="batch-server-management-planning"></a><span data-ttu-id="6c6a7-134">バッチ サーバーの管理計画</span><span class="sxs-lookup"><span data-stu-id="6c6a7-134">Batch server management planning</span></span>
<span data-ttu-id="6c6a7-135">すべてのバッチ サーバーは単一の場所から管理することができます。</span><span class="sxs-lookup"><span data-stu-id="6c6a7-135">All batch servers can be managed from a single location.</span></span> 

<span data-ttu-id="6c6a7-136">バッチ サーバーの 1 つの一般的な使用方法は、複数のサーバー間でジョブの負荷分散を行うことです。</span><span class="sxs-lookup"><span data-stu-id="6c6a7-136">One typical use of batch servers is to load balance jobs across multiple servers.</span></span> <span data-ttu-id="6c6a7-137">バッチ サーバーが処理するスレッド数をセットすることができます。</span><span class="sxs-lookup"><span data-stu-id="6c6a7-137">You can set the number of threads that the batch server will process.</span></span> 

<span data-ttu-id="6c6a7-138">バッチ サーバーは、クライアントおよびその他の関連付けられたコンポーネントからサービスが要求する有効な AOS インスタンスでもあるため、AOS インスタンスがバッチ処理に利用できるようにする場合は慎重に決定する必要があります。</span><span class="sxs-lookup"><span data-stu-id="6c6a7-138">Because batch servers are also active AOS instances that service requests from the client and other associated components, you must carefully determine when an AOS instance should be available to process batches.</span></span> 


## <a name="walkthroughs"></a><span data-ttu-id="6c6a7-139">チュートリアル</span><span class="sxs-lookup"><span data-stu-id="6c6a7-139">Walkthroughs</span></span>
<span data-ttu-id="6c6a7-140">次のチュートリアルでは、タスクの処理方法と、バッチ グループを使用してバッチ ジョブをバッチ ・サーバーに関連付ける方法について説明します。</span><span class="sxs-lookup"><span data-stu-id="6c6a7-140">The following walkthroughs describe how tasks are processed, and how batch groups can be used to associate batch jobs with batch servers.</span></span>

### <a name="batch-processing-of-dependent-tasks"></a><span data-ttu-id="6c6a7-141">従属タスクのバッチ処理</span><span class="sxs-lookup"><span data-stu-id="6c6a7-141">Batch processing of dependent tasks</span></span>

<span data-ttu-id="6c6a7-142">この例では、ジョブ 1 と呼ばれるジョブを作成しました。</span><span class="sxs-lookup"><span data-stu-id="6c6a7-142">For this example, you've created a job that is called JOB 1.</span></span> <span data-ttu-id="6c6a7-143">次の図に示すように、職務には 7 つのタスクがあります。タスク 1、タスク 2、タスク 3、タスク 4、タスク 5、タスク 6、およびタスク 7 です。</span><span class="sxs-lookup"><span data-stu-id="6c6a7-143">As the following diagram shows, the job has seven tasks: TASK 1, TASK 2, TASK 3, TASK 4, TASK 5, TASK 6, and TASK 7.</span></span> 

![依存タスクのジョブ](./media/batch_framework_programmability.gif) 

<span data-ttu-id="6c6a7-145">タスクには次の依存関係があります。</span><span class="sxs-lookup"><span data-stu-id="6c6a7-145">The tasks have the following dependencies:</span></span>

-   <span data-ttu-id="6c6a7-146">タスク 1 は、最初のタスクです。</span><span class="sxs-lookup"><span data-stu-id="6c6a7-146">TASK 1 is the first task.</span></span>
-   <span data-ttu-id="6c6a7-147">タスク 2 は、タスク 1 が完了すると実行されます (タスク 1 が成功したか失敗したかに関係ありません)。</span><span class="sxs-lookup"><span data-stu-id="6c6a7-147">TASK 2 runs when TASK 1 is completed (regardless of the success or failure of TASK 1).</span></span>
-   <span data-ttu-id="6c6a7-148">タスク 3 は、タスク 2 が正常に行われた場合に実行されます。</span><span class="sxs-lookup"><span data-stu-id="6c6a7-148">TASK 3 runs when TASK 2 is successful.</span></span>
-   <span data-ttu-id="6c6a7-149">タスク 4 は、タスク 2 が正常に行われた場合に実行されます。</span><span class="sxs-lookup"><span data-stu-id="6c6a7-149">TASK 4 runs when TASK 2 is successful.</span></span>
-   <span data-ttu-id="6c6a7-150">タスク 5 は、タスク 2 が失敗したときに実行されます。</span><span class="sxs-lookup"><span data-stu-id="6c6a7-150">TASK 5 runs when TASK 2 fails.</span></span>
-   <span data-ttu-id="6c6a7-151">タスク 6 は、タスク 3 が失敗したときに実行されます。</span><span class="sxs-lookup"><span data-stu-id="6c6a7-151">TASK 6 runs when TASK 3 fails.</span></span>
-   <span data-ttu-id="6c6a7-152">タスク 7 は、タスク 3 とタスク 4 の両方が正常に行われたときに実行されます。</span><span class="sxs-lookup"><span data-stu-id="6c6a7-152">TASK 7 runs when both TASK 3 and TASK 4 are successful.</span></span>

<span data-ttu-id="6c6a7-153">2 つのバッチ・サーバー、Batch1 と Batch2 が構成されています。</span><span class="sxs-lookup"><span data-stu-id="6c6a7-153">Two batch servers, Batch1 and Batch2, are configured.</span></span> <span data-ttu-id="6c6a7-154">各サーバーには、1 つのスレッドの容量があります。</span><span class="sxs-lookup"><span data-stu-id="6c6a7-154">Each server has a capacity of one thread.</span></span> 

<span data-ttu-id="6c6a7-155">Batch1 が待機中のタスクをチェックし、そのスレッドにタスク 1 を割り当て、タスク 1 の実行を開始するとします。</span><span class="sxs-lookup"><span data-stu-id="6c6a7-155">Imagine that Batch1 checks for waiting tasks, assigns TASK 1 to its thread, and starts to run TASK 1.</span></span> <span data-ttu-id="6c6a7-156">Batch2 とその単一スレッドも使用可能ですが、タスク 2 はタスク 1 が完了するまで待機し続けます。</span><span class="sxs-lookup"><span data-stu-id="6c6a7-156">Although Batch2 and its single thread are also available, TASK 2 continues to wait until TASK 1 is completed.</span></span> 

<span data-ttu-id="6c6a7-157">タスク 1 が完了するとすぐに、タスク 2 は実行する準備ができています。</span><span class="sxs-lookup"><span data-stu-id="6c6a7-157">As soon as TASK 1 is completed, TASK 2 is ready to be run.</span></span> <span data-ttu-id="6c6a7-158">ここでは、Batch2 が待機中のタスクをチェックし、そのスレッドにタスク 2 を割り当て、タスク 2 の実行を開始するものとします。</span><span class="sxs-lookup"><span data-stu-id="6c6a7-158">This time, imagine that Batch2 checks for waiting tasks, assigns TASK 2 to its thread, and starts to run TASK 2.</span></span> 

<span data-ttu-id="6c6a7-159">タスク 2 が正常に行われた場合は、タスク 3 およびタスク 4 の実行準備が整います。</span><span class="sxs-lookup"><span data-stu-id="6c6a7-159">If TASK 2 is successful, TASK 3 and TASK 4 are ready to be run.</span></span> <span data-ttu-id="6c6a7-160">ここでは、Batch2 が待機中のタスクをチェックし、そのスレッドにタスク 3 を割り当て、タスク 3 の実行を開始するものとします。</span><span class="sxs-lookup"><span data-stu-id="6c6a7-160">This time, imagine that Batch2 checks for waiting tasks, assigns TASK 3 to its thread, and starts to run TASK 3.</span></span> <span data-ttu-id="6c6a7-161">Batch1 も待機中のタスクをチェックし、そのスレッドにタスク 4 を割り当て、タスク 4 の実行を開始します。</span><span class="sxs-lookup"><span data-stu-id="6c6a7-161">Batch1 also checks for waiting tasks, assigns TASK 4 to its thread, and starts to run TASK 4.</span></span> 

<span data-ttu-id="6c6a7-162">タスク 3 とタスク 4 が成功した場合は、バッチ サーバーのいずれかがタスク 7 を実行します。</span><span class="sxs-lookup"><span data-stu-id="6c6a7-162">If TASK 3 and TASK 4 are successful, one of the batch servers runs TASK 7.</span></span> 

<span data-ttu-id="6c6a7-163">タスク 2 が失敗すると、バッチ サーバーのいずれかがタスク 5 を実行します。</span><span class="sxs-lookup"><span data-stu-id="6c6a7-163">If TASK 2 fails, one of the batch servers runs TASK 5.</span></span> 

<span data-ttu-id="6c6a7-164">タスク 3 が失敗すると、利用可能なバッチ サーバーのいずれかがタスク 6 を実行します。</span><span class="sxs-lookup"><span data-stu-id="6c6a7-164">If TASK 3 fails, one of the available batch servers runs TASK 6.</span></span> 

<span data-ttu-id="6c6a7-165">**注記:** このチュートリアルでは、概念を説明するために Batch1 と Batch2 を使用します。</span><span class="sxs-lookup"><span data-stu-id="6c6a7-165">**Note:** For this walkthrough, we are using Batch1 and Batch2 to explain the concept.</span></span> <span data-ttu-id="6c6a7-166">使用可能なスレッドを持つすべてのバッチ サーバーは、待機中のタスクの実行を開始します。</span><span class="sxs-lookup"><span data-stu-id="6c6a7-166">Any batch server that has available threads will start to run a waiting task.</span></span> <span data-ttu-id="6c6a7-167">サーバー上で実行するバッチ ジョブを決定または指定するには、バッチ グループを作成する必要があります。</span><span class="sxs-lookup"><span data-stu-id="6c6a7-167">You must create a batch group to determine or specify which batch job runs on which server.</span></span>

### <a name="batch-processing-that-uses-batch-groups"></a><span data-ttu-id="6c6a7-168">バッチ グループを使用するバッチ処理</span><span class="sxs-lookup"><span data-stu-id="6c6a7-168">Batch processing that uses batch groups</span></span>

<span data-ttu-id="6c6a7-169">この例は、特定のバッチ サーバーでバッチ ジョブを処理する方法を示しています。</span><span class="sxs-lookup"><span data-stu-id="6c6a7-169">This example shows how batch jobs can be processed on specific batch servers.</span></span> 

<span data-ttu-id="6c6a7-170">次の 3 つのバッチ サーバー、AOS1、AOS2、および AOS3 があります。</span><span class="sxs-lookup"><span data-stu-id="6c6a7-170">You have three batch servers: AOS1, AOS2, and AOS3.</span></span> <span data-ttu-id="6c6a7-171">既定では、すべてのバッチ サーバーは使用可能なスレッドの数に応じて、すべてのバッチ ジョブのタスクを処理します。</span><span class="sxs-lookup"><span data-stu-id="6c6a7-171">By default, all the batch servers process tasks from all batch jobs, depending on the number of available threads.</span></span> 

<span data-ttu-id="6c6a7-172">名前付きバッチ グループ、BG1 を作成し、AOS2 および AOS3 で実行するように構成します。</span><span class="sxs-lookup"><span data-stu-id="6c6a7-172">You create a named batch group, BG1, and configure it to run on AOS2 and AOS3.</span></span> <span data-ttu-id="6c6a7-173">したがって、BG1 のジョブからのタスクは、使用可能なスレッドの数に応じて、AOS2 または AOS3 でのみ実行されます。</span><span class="sxs-lookup"><span data-stu-id="6c6a7-173">Therefore, tasks from jobs in BG1 will run only on AOS2 or AOS3, depending on the number available threads.</span></span> <span data-ttu-id="6c6a7-174">AOS1 は、BG1 のジョブのタスクを処理しません。</span><span class="sxs-lookup"><span data-stu-id="6c6a7-174">AOS1 won't process tasks from jobs in BG1.</span></span> <span data-ttu-id="6c6a7-175">同様に、AOS2 および AOS3 は BG1 からのみタスクを処理します。</span><span class="sxs-lookup"><span data-stu-id="6c6a7-175">Likewise, AOS2 and AOS3 will process tasks from BG1 only.</span></span> 

<span data-ttu-id="6c6a7-176">AOS2 および AOS3 を構成して他のバッチ グループからタスクを処理することができます。</span><span class="sxs-lookup"><span data-stu-id="6c6a7-176">You can configure AOS2 and AOS3 to process tasks from other batch groups.</span></span> <span data-ttu-id="6c6a7-177">これらのバッチ グループには、既定のバッチ グループが含まれています。</span><span class="sxs-lookup"><span data-stu-id="6c6a7-177">These batch groups include the default batch group.</span></span>


