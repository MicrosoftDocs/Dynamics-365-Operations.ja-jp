---
title: 実行中のバッチ ジョブのキャンセル
description: このトピックでは、実行中のバッチ ジョブをキャンセルする方法について説明します。
author: karimelazzouni
ms.date: 03/26/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: IT Pro
ms.reviewer: sericks
ms.custom: 62333
ms.assetid: 6135bcf7-bf8f-42ae-b2c6-458f6538e6a4
ms.search.region: Global
ms.author: kaelazzo
ms.search.validFrom: 2019-05-08
ms.dyn365.ops.version: Platform update 27
ms.openlocfilehash: 5626383f3cb47a89a62e79665c0d43e8fb6ccb3f
ms.sourcegitcommit: 074b6e212d19dd5d84881d1cdd096611a18c207f
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 03/31/2021
ms.locfileid: "5751338"
---
# <a name="cancel-an-executing-batch-job"></a><a id="legacy-abort"></a><span data-ttu-id="5424b-103">実行中のバッチ ジョブのキャンセル</span><span class="sxs-lookup"><span data-stu-id="5424b-103">Cancel an executing batch job</span></span>
[!include [banner](../includes/banner.md)]

> [!NOTE] 
> <span data-ttu-id="5424b-104">この機能は、Platform update 27 以降で利用できます。</span><span class="sxs-lookup"><span data-stu-id="5424b-104">This feature is available as of Platform update 27.</span></span>

<span data-ttu-id="5424b-105">すでに実行中のタスクが完了するのに長い時間がかかる場合、バッチ ジョブのキャンセルに長い時間がかかる場合があります。</span><span class="sxs-lookup"><span data-stu-id="5424b-105">Sometimes canceling a batch job can take a long time if already executing tasks will take a long time to finish.</span></span> <span data-ttu-id="5424b-106">このオプションを使用すると、システム管理者やバッチ ジョブ マネージャーは、キャンセル処理中のジョブに対してすでに実行されているタスクをキャンセルできます。</span><span class="sxs-lookup"><span data-stu-id="5424b-106">This option provides a system administrator or batch job manager with the ability to cancel already executing tasks for jobs that are in the process of being canceled.</span></span> <span data-ttu-id="5424b-107">これは他の場所でシステムの使用に影響を与えている長時間実行中のジョブをキャンセルするはるかに高速なメカニズムを提供します。</span><span class="sxs-lookup"><span data-stu-id="5424b-107">This provides a much faster mechanism to cancel a long running job that is impacting system usage elsewhere.</span></span>

>[!NOTE]
> <span data-ttu-id="5424b-108">この機能は注意して使用する必要があることが重要です。</span><span class="sxs-lookup"><span data-stu-id="5424b-108">It is important to note that this feature should be used with caution.</span></span> <span data-ttu-id="5424b-109">実行中のプロセスをキャンセルすると、本質的に安全でないアクションのため、データが破損したり孤立したデータまたは不完全なデータが生成される可能性があります。</span><span class="sxs-lookup"><span data-stu-id="5424b-109">When you cancel a running process, it is an inherently unsafe action that can lead to data corruption, resulting in either orphaned or incomplete data.</span></span> <span data-ttu-id="5424b-110">このアクションは、実行中のタスクによって引き起こされる他の問題を軽減するためにのみ使用するべきです。</span><span class="sxs-lookup"><span data-stu-id="5424b-110">This action should only be used to mitigate other issues caused by the running tasks.</span></span>

<span data-ttu-id="5424b-111">実行中のタスクを直ちにキャンセルするには、次の手順を実行します。</span><span class="sxs-lookup"><span data-stu-id="5424b-111">Complete the following steps to immediately cancel the running task.</span></span>

1. <span data-ttu-id="5424b-112">**システム管理** \> **照会** \> **バッチ ジョブ** の順に移動します。</span><span class="sxs-lookup"><span data-stu-id="5424b-112">Go to **System administration** \> **Inquiries** \> **Batch jobs**.</span></span>
2. <span data-ttu-id="5424b-113">**状態** が **キャンセル** のバッチ ジョブを選択します。</span><span class="sxs-lookup"><span data-stu-id="5424b-113">Select a batch job that has a **Status** of **Canceling**.</span></span>
3. <span data-ttu-id="5424b-114">**バッチ タスク** タブでタスク上の **中止** を選択し、**OK** を選択します。</span><span class="sxs-lookup"><span data-stu-id="5424b-114">On the **Batch tasks** tab, select **Abort** on the task, and then select **OK**.</span></span>

## <a name="enhanced-cancellation-feature"></a><span data-ttu-id="5424b-115">取消機能の強化</span><span class="sxs-lookup"><span data-stu-id="5424b-115">Enhanced cancellation feature</span></span>
<span data-ttu-id="5424b-116">バージョン 10.0.16 から、バッチの取消機能の拡張機能が導入されました。</span><span class="sxs-lookup"><span data-stu-id="5424b-116">Starting in version 10.0.16, an enhancement to the batch cancellation functionality has been introduced.</span></span> <span data-ttu-id="5424b-117">確認すると、キャンセルしようとするバッチ タスクを現在実行しているバッチ サーバーが再起動します。</span><span class="sxs-lookup"><span data-stu-id="5424b-117">Upon confirmation, this will restart the batch server currently running the batch tasks that you are attempting to cancel.</span></span> <span data-ttu-id="5424b-118">これにより、機能は制限に大きな影響を与えるので、キャンセルしようとするジョブのタスクが適用される前の設定が解除されます。</span><span class="sxs-lookup"><span data-stu-id="5424b-118">This makes the functionality more resilient to limitations, and ensures that tasks of the job you are trying to cancel are truly preempted.</span></span>

<span data-ttu-id="5424b-119">新しい機能を使用するには、次の手順を参照してください。</span><span class="sxs-lookup"><span data-stu-id="5424b-119">To use the new functionality, refer to the following steps:</span></span>

1. <span data-ttu-id="5424b-120">バージョン 10.0.16 以降を実行するか、または必要な品質パッケージをインストールしてください。</span><span class="sxs-lookup"><span data-stu-id="5424b-120">Make sure you are running version 10.0.16 or later, or have the necessary quality package installed.</span></span>
2. <span data-ttu-id="5424b-121">[機能管理](https://docs.microsoft.com/dynamics365/fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview) ワークスペースの **バッチ中止の強化** 機能を有効にします。</span><span class="sxs-lookup"><span data-stu-id="5424b-121">Enable the **Enhanced batch abort** feature in the [Feature management](https://docs.microsoft.com/dynamics365/fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview) workspace.</span></span>
3. <span data-ttu-id="5424b-122">同じ指示に従い、[実行しているバッチ ジョブをキャンセル](#legacy-abort) を実行します。</span><span class="sxs-lookup"><span data-stu-id="5424b-122">Follow the same instructions to [cancel an executing batch job](#legacy-abort).</span></span>
 
<span data-ttu-id="5424b-123">キャンセル タスクを実行しているバッチ サーバーを再起動するように求めるメッセージが表示されます。</span><span class="sxs-lookup"><span data-stu-id="5424b-123">You will be prompted that the batch server, which is running the canceling tasks, will be restarted.</span></span> <span data-ttu-id="5424b-124">これにより、他のバッチ ジョブの一覧が混乱する可能性があります。</span><span class="sxs-lookup"><span data-stu-id="5424b-124">This can potentially disrupt a list of other batch jobs.</span></span> <span data-ttu-id="5424b-125">キャンセル タスクを終了するには、次の手順に進む必要があります。</span><span class="sxs-lookup"><span data-stu-id="5424b-125">You must proceed in order to end the canceling tasks.</span></span>

![キャンセル タスクを終了することを確認します。](https://user-images.githubusercontent.com/7556912/112464897-ba820680-8d6c-11eb-871a-e1aff1d82665.png)

<span data-ttu-id="5424b-127">サーバーで他の実行中のバッチ ジョブをキャンセルしたくない、実行中のすべてのジョブではなく単一タスクをキャンセルする古い動作を好む場合は、機能管理ワークスペースの **バッチ中止の強化** 機能をオフにし、再度[実行しているバッチ ジョブをキャンセル](#legacy-abort) を行えます。</span><span class="sxs-lookup"><span data-stu-id="5424b-127">If you do not want to cancel other running batch jobs on the server and would prefer the old behavior of canceling a single task and not all the jobs running, you can turn off the **Enhanced batch abort** feature in the Feature management workspace and try to [cancel the executing batch job](#legacy-abort) again.</span></span>


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
