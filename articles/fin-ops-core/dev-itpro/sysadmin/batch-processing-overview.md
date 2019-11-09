---
title: バッチ処理の概要
description: このトピックでは、バッチ処理の概要を示します。
author: hasaid
manager: AnnBe
ms.date: 07/23/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-platform
ms.technology: ''
audience: IT Pro
ms.reviewer: sericks
ms.search.scope: Core, Operations
ms.custom: 62333
ms.assetid: 6135bcf7-bf8f-42ae-b2c6-458f6538e6a4
ms.search.region: Global
ms.author: hasaid
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 365d35ebf6f7a935aa5a4b6e42e072d6eb26319c
ms.sourcegitcommit: 3ba95d50b8262fa0f43d4faad76adac4d05eb3ea
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 09/27/2019
ms.locfileid: "2183079"
---
# <a name="batch-processing-overview"></a><span data-ttu-id="95f41-103">バッチ処理の概要</span><span class="sxs-lookup"><span data-stu-id="95f41-103">Batch processing overview</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="95f41-104">このトピックでは、バッチ処理の概要を示します。</span><span class="sxs-lookup"><span data-stu-id="95f41-104">This topic provides an overview of batch processing.</span></span>

<span data-ttu-id="95f41-105">Finance and Operations では、多くのタスクをバッチ ジョブの一部として実行できます。</span><span class="sxs-lookup"><span data-stu-id="95f41-105">Many tasks in Finance and Operations can be run as part of batch jobs.</span></span> <span data-ttu-id="95f41-106">たとえば、バッチ ジョブには、レポートの印刷、管理の実行、電子ドキュメントの送信などのタスクを含めることができます。</span><span class="sxs-lookup"><span data-stu-id="95f41-106">For example, batch jobs can include tasks for printing reports, performing maintenance, or sending electronic documents.</span></span> <span data-ttu-id="95f41-107">バッチ ジョブを使用すると、通常の就業時間内におけるコンピュータまたはサーバーの処理速度の低下を回避できます。</span><span class="sxs-lookup"><span data-stu-id="95f41-107">By using batch jobs, you can avoid slowing down your computer or the server during typical working hours.</span></span> 

<span data-ttu-id="95f41-108">バッチ ジョブ内のタスクは、順次または同時のいずれかに実行できます。</span><span class="sxs-lookup"><span data-stu-id="95f41-108">The tasks in a batch job can run either sequentially or at the same time.</span></span> <span data-ttu-id="95f41-109">また、タスク間に依存関係を作成できます。</span><span class="sxs-lookup"><span data-stu-id="95f41-109">Additionally, you can create dependencies between tasks.</span></span> <span data-ttu-id="95f41-110">つまり、前のタスクが成功したか失敗したかによってタスク順序が変わります。</span><span class="sxs-lookup"><span data-stu-id="95f41-110">In other words, the sequence of tasks can differ, depending on whether an earlier task succeeds or fails.</span></span> 

<span data-ttu-id="95f41-111">バッチ ジョブの再実行回数を設定できます。</span><span class="sxs-lookup"><span data-stu-id="95f41-111">You can set up recurrence patterns for batch jobs.</span></span> <span data-ttu-id="95f41-112">たとえば、毎月、月末に請求書を自動処理するジョブを設定できます。</span><span class="sxs-lookup"><span data-stu-id="95f41-112">For example, you can set up a job to process invoices automatically at the end of every month.</span></span> 

<span data-ttu-id="95f41-113">バッチ ジョブを監視するために、警告を設定できます。</span><span class="sxs-lookup"><span data-stu-id="95f41-113">To monitor batch jobs, you can set up alerts.</span></span> <span data-ttu-id="95f41-114">バッチジョブが成功した場合、失敗した場合、または実行が完了した場合に警告を送信できます。</span><span class="sxs-lookup"><span data-stu-id="95f41-114">Alerts can be sent when the batch job succeeds, fails, or has finished running.</span></span> 

<span data-ttu-id="95f41-115">バッチ ジョブの処理後、履歴を表示できます。</span><span class="sxs-lookup"><span data-stu-id="95f41-115">After a batch job has been processed, you can view the history.</span></span> <span data-ttu-id="95f41-116">履歴には、ジョブの実行中に発生したメッセージが含まれています。</span><span class="sxs-lookup"><span data-stu-id="95f41-116">The history includes any messages that were encountered while the job was running.</span></span> 

<span data-ttu-id="95f41-117">バッチ グループを使用してバッチ タスクをカテゴリ化し、特定のサーバーで実行します。</span><span class="sxs-lookup"><span data-stu-id="95f41-117">Use batch groups to categorize batch tasks and run them on specific servers.</span></span> <span data-ttu-id="95f41-118">作業環境のサーバーには、別のソフトウェアがインストールされているサーバーや、1 日の内で使用できる時間が異なるサーバーがあります。</span><span class="sxs-lookup"><span data-stu-id="95f41-118">The servers in your environment might have different software installed, or they might be available at different times of the day.</span></span> <span data-ttu-id="95f41-119">バッチ グループを使用すると、最も適したサーバーにバッチ タスクを割り当てることができます。</span><span class="sxs-lookup"><span data-stu-id="95f41-119">Batch groups are used to direct batch tasks to the most appropriate server.</span></span> <span data-ttu-id="95f41-120">同じバッチ ジョブ内のタスクは、別の複数のバッチ グループに含めることもできます。</span><span class="sxs-lookup"><span data-stu-id="95f41-120">Tasks in the same batch job can belong to different batch groups.</span></span> 

<span data-ttu-id="95f41-121">たとえば、サーバー A がレポートを印刷するよう設定され、サーバー B が電子ドキュメントを送信するよう設定されます。</span><span class="sxs-lookup"><span data-stu-id="95f41-121">For example, server A is set up to print reports, and server B is set up to send electronic documents.</span></span> <span data-ttu-id="95f41-122">バッチ グループを使用することで、レポート タスクがサーバー A で実行され、電子ドキュメントがサーバー B で処理されることを保証することができます。</span><span class="sxs-lookup"><span data-stu-id="95f41-122">You can use batch groups to make sure that reporting tasks are run on server A and electronic documents are processed by server B.</span></span>

<span data-ttu-id="95f41-123">詳細については、[バッチ処理とバッチ サーバー](batch-server-overview.md) を参照してください。</span><span class="sxs-lookup"><span data-stu-id="95f41-123">For more information, see [Batch processing and batch servers](batch-server-overview.md).</span></span>


## <a name="batch-functions"></a><span data-ttu-id="95f41-124">バッチ関数</span><span class="sxs-lookup"><span data-stu-id="95f41-124">Batch functions</span></span>

<span data-ttu-id="95f41-125">管理者およびバッチ マネージャーは、バッチ ジョブの作成とコピー、バッチ ジョブ ユーザーの変更、ジョブを実行しない期間の指定などの一般的なタスクを実行できます。</span><span class="sxs-lookup"><span data-stu-id="95f41-125">Administrators and Batch managers can perform common tasks including creating and copying batch jobs, changing a batch job user, and specifying a time period in which a job should not execute.</span></span> <span data-ttu-id="95f41-126">これらのタスクの詳細については、次のトピックを参照してください。</span><span class="sxs-lookup"><span data-stu-id="95f41-126">For more information about these tasks, see the following topics:</span></span>

-  [<span data-ttu-id="95f41-127">バッチ ジョブの作成</span><span class="sxs-lookup"><span data-stu-id="95f41-127">Create a batch job</span></span>](tasks/create-batch-job.md)
-  [<span data-ttu-id="95f41-128">バッチ マネージャー ロール</span><span class="sxs-lookup"><span data-stu-id="95f41-128">Batch manager role</span></span>](runby.md)
-  [<span data-ttu-id="95f41-129">バッチ アクティブ期間</span><span class="sxs-lookup"><span data-stu-id="95f41-129">Batch active period</span></span>](activeperiod.md)
-  [<span data-ttu-id="95f41-130">バッチ ジョブのコピー</span><span class="sxs-lookup"><span data-stu-id="95f41-130">Copy a batch job</span></span>](copy-batch-job.md)
-  [<span data-ttu-id="95f41-131">バッチ警告のコンフィギュレーション</span><span class="sxs-lookup"><span data-stu-id="95f41-131">Configure batch alerts</span></span>](alerts.md)
-  [<span data-ttu-id="95f41-132">バッチ化された フォーム</span><span class="sxs-lookup"><span data-stu-id="95f41-132">Batch enhanced forms</span></span>](enhanced-forms.md)
-  [<span data-ttu-id="95f41-133">バッチ履歴のクリーンアップ</span><span class="sxs-lookup"><span data-stu-id="95f41-133">Batch history cleanup</span></span>](batch-history-cleanup.md)
-  [<span data-ttu-id="95f41-134">実行中のバッチ ジョブの中止</span><span class="sxs-lookup"><span data-stu-id="95f41-134">Abort an executing batch job</span></span>](batch-abort.md)
