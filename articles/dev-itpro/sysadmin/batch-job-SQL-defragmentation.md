---
title: SQL インデックスの最適化を処理するバッチ ジョブ
description: このトピックでは、分割されたインデックスを再構築するために使用するシステム バッチ ジョブを説明します。
author: sericks
manager: AnnBe
ms.date: 02/25/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: IT Pro
ms.reviewer: sericks
ms.search.scope: Operations
ms.search.region: Global
ms.author: ganas
ms.search.validFrom: 2018-12-31
ms.dyn365.ops.version: Platform update 22
ms.openlocfilehash: c02a91b9c8d2e5943b2c4945769e86a6abdda0a6
ms.sourcegitcommit: 2bced4ab07ac29dbbb6ee87398c5915d58466004
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 02/25/2019
ms.locfileid: "759718"
---
# <a name="batch-job-to-handle-sql-index-defragmentation"></a><span data-ttu-id="910e0-103">SQL インデックスの最適化を処理するバッチ ジョブ</span><span class="sxs-lookup"><span data-stu-id="910e0-103">Batch job to handle SQL index defragmentation</span></span>

[!include[banner](../includes/banner.md)]


<span data-ttu-id="910e0-104">プラットフォーム更新プログラム 22 では、断片化したインデックスを再構築する新しいシステム バッチ ジョブが導入されました。</span><span class="sxs-lookup"><span data-stu-id="910e0-104">In Platform update 22, a new system batch job has been introduced to rebuild fragmented indexes.</span></span> <span data-ttu-id="910e0-105">インデックスの断片化により、固有のシナリオでパフォーマンスが著しく低下します。</span><span class="sxs-lookup"><span data-stu-id="910e0-105">Index fragmentation results in notable performance degradation in specific scenarios.</span></span> <span data-ttu-id="910e0-106">断片化の問題に対処し、データベースを最高のパフォーマンス状態に維持するため、このバッチ ジョブはスケジュールされた時間に定期的に激しく断片化したインデックスを再構築します。</span><span class="sxs-lookup"><span data-stu-id="910e0-106">To address fragmentation issues and keep the database in a top-performing state, this batch job will rebuild highly fragmented indexes periodically at a scheduled time.</span></span> <span data-ttu-id="910e0-107">既定では、そのジョブは毎日現地時間の午前 3:00 に最大 2 時間実行されるようにスケジュールされます。</span><span class="sxs-lookup"><span data-stu-id="910e0-107">By default, the job scheduled to run at 3:00 AM local time every day for a maximum of 2 hours.</span></span> <span data-ttu-id="910e0-108">再構築する必要がある断片化されたインデックスが多くないとバッチ ジョブが判断した場合は早期に完了します。</span><span class="sxs-lookup"><span data-stu-id="910e0-108">If the batch job finds that not many fragmented indexes need to be rebuilt, it will complete early.</span></span>  

<span data-ttu-id="910e0-109">このシステム ジョブは変更できません</span><span class="sxs-lookup"><span data-stu-id="910e0-109">This system job cannot be canceled.</span></span> <span data-ttu-id="910e0-110">週 1 回実行する場合は、スケジュールと頻度を変更できます。</span><span class="sxs-lookup"><span data-stu-id="910e0-110">You can change the schedule and its recurrence if you want to run it weekly.</span></span> <span data-ttu-id="910e0-111">システム ジョブは、週 1 回以上実行する必要があります。</span><span class="sxs-lookup"><span data-stu-id="910e0-111">System jobs are expected to run at least once a week.</span></span> 

<span data-ttu-id="910e0-112">**システム ジョブ パラメーターを調整** ページでパラメータの値を変更し、ジョブを実行できる期間とターゲットとできるインデックスの数を最大値で指定できます。</span><span class="sxs-lookup"><span data-stu-id="910e0-112">You can change the parameter values on the **Adjust system job parameters** page to denote how long the job can run and how many indexes it should target, at a maximum.</span></span> <span data-ttu-id="910e0-113">DTU しきい値は、システムがビジー状態のときにこのジョブが開始するのを防ぎます。</span><span class="sxs-lookup"><span data-stu-id="910e0-113">The DTU threshold is to prevent this job from starting when the system is busy.</span></span> <span data-ttu-id="910e0-114">既定の DTU しきい値が 50 の場合、つまりインデックスがジョブの再構築をスケジュールされているときにシステムが 50% 以上の DTU を使用している場合、ジョブはインデックスを再構築しないで早期に終了します。</span><span class="sxs-lookup"><span data-stu-id="910e0-114">The default DTU threshold is 50,  which means that if the system is using 50 percent or more DTU during the time that the index rebuild job is scheduled to run, the job exit early without rebuilding any indexes.</span></span>
 
<span data-ttu-id="910e0-115">![システム ジョブ調整パラメータ ページのスクリーンショット](media/SystemJobParameters.PNG "システム ジョブ調整パラメータ ページのスクリーンショット")</span><span class="sxs-lookup"><span data-stu-id="910e0-115">![Screenshot of Adjust system job parameters page](media/SystemJobParameters.PNG "Screenshot of Adjust system job parameters page")</span></span>
 
<span data-ttu-id="910e0-116">このジョブを実行すると、以下に影響を与える可能性があります。</span><span class="sxs-lookup"><span data-stu-id="910e0-116">When this job is executing, there could be some impact on the following:</span></span>
-   <span data-ttu-id="910e0-117">SQL リソースの処理にかかる時間。</span><span class="sxs-lookup"><span data-stu-id="910e0-117">The time that it takes SQL resources to process.</span></span>
- <span data-ttu-id="910e0-118">ブロックされる場合があります。</span><span class="sxs-lookup"><span data-stu-id="910e0-118">There may be blocking,</span></span>

## <a name="change-the-default-scheduled-timerecurrence"></a><span data-ttu-id="910e0-119">スケジュールされた既定の時間/頻度の変更</span><span class="sxs-lookup"><span data-stu-id="910e0-119">Change the default scheduled time/recurrence</span></span>
1. <span data-ttu-id="910e0-120">**システム管理 > 照会 > バッチ ジョブ** の順に移動します。</span><span class="sxs-lookup"><span data-stu-id="910e0-120">Go to **System administration > Inquiries > Batch Jobs**.</span></span>
2. <span data-ttu-id="910e0-121">*インデックスの再構築*を含むジョブの説明を検索します。</span><span class="sxs-lookup"><span data-stu-id="910e0-121">Search for a job description that contains *index rebuild*.</span></span>   
3. <span data-ttu-id="910e0-122">レコードを選択します。</span><span class="sxs-lookup"><span data-stu-id="910e0-122">Select the record.</span></span>  
4. <span data-ttu-id="910e0-123">メニュー項目**バッチ ジョブ > 再実行**をクリックします。</span><span class="sxs-lookup"><span data-stu-id="910e0-123">Click the menu item **Batch Job > Recurrence**.</span></span>  
5. <span data-ttu-id="910e0-124">スケジュールに合うようにスケジュール時間と頻度を変更します。</span><span class="sxs-lookup"><span data-stu-id="910e0-124">Change the schedule time and recurrence to suit your schedule.</span></span>

<span data-ttu-id="910e0-125">インデックス再構築の結果は、**システム管理 > 照会 > データベース > SQLインデックスの断片化の詳細**にあります。</span><span class="sxs-lookup"><span data-stu-id="910e0-125">The results of index rebuild can be found by going to **System administration > Inquiries > Database > SQL index fragmentation details**.</span></span> 

> [!Note]
> <span data-ttu-id="910e0-126">場合によっては、断片化の前後で番号が同じであるかそれ以上であることがあります。</span><span class="sxs-lookup"><span data-stu-id="910e0-126">In some cases, you may find that the before and after fragmentation number is the same or even higher.</span></span> <span data-ttu-id="910e0-127">これは、Microsoft が侵入型オンライン再構築オプションを使用しているため通常です。</span><span class="sxs-lookup"><span data-stu-id="910e0-127">This is typical because Microsoft uses a less intrusive online rebuild option.</span></span> <span data-ttu-id="910e0-128">今後、オプションのオフライン再構築オプションの導入を計画しています。</span><span class="sxs-lookup"><span data-stu-id="910e0-128">In the future, we plan to introduce an optional offline rebuild option.</span></span>
