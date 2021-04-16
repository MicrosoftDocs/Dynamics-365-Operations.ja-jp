---
title: ライフ イベントのプロセス
description: Microsoft Dynamics 365 Human Resources の従業員のライフサイクル中に、各従業員に対してさまざまなイベントの変化が発生する可能性があります。
author: andreabichsel
ms.date: 04/06/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: BenefitWorkspace, HcmBenefitSummaryPart, BenefitLifeEventTypes, BenefitEligibilityProcessResultViewer
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Human Resources
ms.custom: 7521
ms.assetid: ''
ms.search.region: Global
ms.author: anbichse
ms.search.validFrom: 2020-02-03
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: 461f90c3da8fa5b2db14b6dd67a0c19f7eabe867
ms.sourcegitcommit: 3cdc42346bb653c13ab33a7142dbb7969f1f6dda
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 03/31/2021
ms.locfileid: "5793804"
---
# <a name="process-life-events"></a><span data-ttu-id="cdf59-103">ライフ イベントのプロセス</span><span class="sxs-lookup"><span data-stu-id="cdf59-103">Process life events</span></span>

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

<span data-ttu-id="cdf59-104">Microsoft Dynamics 365 Human Resources の従業員のライフサイクル中に、各従業員に対してさまざまなイベントの変化が発生する可能性があります。</span><span class="sxs-lookup"><span data-stu-id="cdf59-104">During the employee lifecycle in Microsoft Dynamics 365 Human Resources, each employee may encounter various life event changes.</span></span> <span data-ttu-id="cdf59-105">たとえば、結婚、雇用の変更、または被扶養/受益者の変更などです。</span><span class="sxs-lookup"><span data-stu-id="cdf59-105">For example, marriage, change in employment, or dependent/beneficiary change.</span></span> <span data-ttu-id="cdf59-106">ライフ イベントを使用するには、給付金パラメータ フォームのライフ イベントを有効にし、ライフ イベント タイプを設定し、さらにプラン タイプのライフ イベント オプションを設定する必要があります。</span><span class="sxs-lookup"><span data-stu-id="cdf59-106">To use life events, you must enable life events in the benefits parameters form, set up life event types, and set up life event options for plan types.</span></span>

<span data-ttu-id="cdf59-107">ライフ イベントを処理するには、採用期間中に、少なくとも一度はオープン登録を実行しておく必要があります。</span><span class="sxs-lookup"><span data-stu-id="cdf59-107">Before you can process life events, you must have already run open enrollment at least once during a hiring time frame.</span></span> <span data-ttu-id="cdf59-108">米国では、オープン登録を通常年に 1 回行います。</span><span class="sxs-lookup"><span data-stu-id="cdf59-108">In the United States, open enrollment is typically once per year.</span></span> <span data-ttu-id="cdf59-109">米国以外では、オープン登録は入社時に実行されます。</span><span class="sxs-lookup"><span data-stu-id="cdf59-109">Outside the United States, open enrollment may be run at the time of hire.</span></span> <span data-ttu-id="cdf59-110">作業者は、処理するべきライフ イベントのために給付金プランを選択する必要はありませんが、オープン登録処理に含まれている必要があります。</span><span class="sxs-lookup"><span data-stu-id="cdf59-110">A worker does not need to select a benefit plan in order for life events to be processed, but they need to have been included in open enrollment processing.</span></span> 

<span data-ttu-id="cdf59-111">将来の日付で発生するライフ イベントをもつ作業者が存在する場合は、ライフ イベント処理を使用します。</span><span class="sxs-lookup"><span data-stu-id="cdf59-111">Use life event processing when you have workers who have life events that take place on a future date.</span></span> <span data-ttu-id="cdf59-112">このイベントは、処理されていないすべてのライフ イベント (将来のライフ イベント、またはいずれかの作業者に固有ではない追加されたライフ イベント – 1 つの例は、新しい給付金) を処理します。</span><span class="sxs-lookup"><span data-stu-id="cdf59-112">This event will process all life events that have not been processed (like future life events, or life events that have been added that are not specific to any one worker – one example is a new benefit).</span></span> <span data-ttu-id="cdf59-113">リアル タイムのライフ イベントは表示されません。</span><span class="sxs-lookup"><span data-stu-id="cdf59-113">Real-time life events are hidden.</span></span>

<span data-ttu-id="cdf59-114">たとえば、今日が 2 月 1 日で、2 月 14 日に作業者である Joe Smith が法人を変更する予定である場合、2 月 15 日にライフ イベント処理を実行すると、2 月 15 日までのすべてのイベントが処理されます。</span><span class="sxs-lookup"><span data-stu-id="cdf59-114">For example, if today is February 1, and on February 14 worker Joe Smith is scheduled to change legal entities, if you run life event processing for February 15, the system processes all events up until February 15.</span></span> 

1. <span data-ttu-id="cdf59-115">**給付金管理** ワークスペースにて、**処理** の下の **ライフ イベントの処理** を選択します。</span><span class="sxs-lookup"><span data-stu-id="cdf59-115">In the **Benefits management** workspace, under **Processing**, select **Life event processing**.</span></span>

2. <span data-ttu-id="cdf59-116">**ライフ イベントの処理を実行** ダイアログ ボックスで、次のフィールドの値を指定します。</span><span class="sxs-lookup"><span data-stu-id="cdf59-116">In the **Run life event process** dialog box, specify values for the following fields:</span></span>

   | <span data-ttu-id="cdf59-117">フィールド</span><span class="sxs-lookup"><span data-stu-id="cdf59-117">Field</span></span> | <span data-ttu-id="cdf59-118">説明</span><span class="sxs-lookup"><span data-stu-id="cdf59-118">Description</span></span> |
   | --- | --- |
   | <span data-ttu-id="cdf59-119">**登録期間**</span><span class="sxs-lookup"><span data-stu-id="cdf59-119">**Enrollment period**</span></span> | <span data-ttu-id="cdf59-120">ライフ イベントを処理する登録期間。</span><span class="sxs-lookup"><span data-stu-id="cdf59-120">The enrollment period to process life events for.</span></span> |
   | <span data-ttu-id="cdf59-121">**法人エンティティ**</span><span class="sxs-lookup"><span data-stu-id="cdf59-121">**Legal entity**</span></span> | <span data-ttu-id="cdf59-122">ライフ イベントを処理する法人。</span><span class="sxs-lookup"><span data-stu-id="cdf59-122">The legal entity to process life events for.</span></span> |
   | <span data-ttu-id="cdf59-123">**ライフ イベント日付**</span><span class="sxs-lookup"><span data-stu-id="cdf59-123">**Life event date**</span></span> | <span data-ttu-id="cdf59-124">システムによって登録期間中に、この日付までのすべてのイベントが処理されます。</span><span class="sxs-lookup"><span data-stu-id="cdf59-124">The system processes all events during the enrollment period that occur up until this date.</span></span> |
   | <span data-ttu-id="cdf59-125">**ワーカー**</span><span class="sxs-lookup"><span data-stu-id="cdf59-125">**Worker**</span></span> | <span data-ttu-id="cdf59-126">ライフ イベントを処理する作業者。</span><span class="sxs-lookup"><span data-stu-id="cdf59-126">The worker to process life events for.</span></span> <span data-ttu-id="cdf59-127">このフィールドを空白のままにすると、ライフ イベントがすべての作業者に対して処理されます。</span><span class="sxs-lookup"><span data-stu-id="cdf59-127">If you leave this field blank, life events will be processed for all workers.</span></span> |

3. <span data-ttu-id="cdf59-128">バックグラウンドで処理を実行する場合は、**バックグラウンドで実行** を選択し、次のタスクを実行します。</span><span class="sxs-lookup"><span data-stu-id="cdf59-128">If you want to run the process in the background, select **Run in the background** and do the following tasks:</span></span>

   1. <span data-ttu-id="cdf59-129">処理情報を入力します。</span><span class="sxs-lookup"><span data-stu-id="cdf59-129">Enter information for the process.</span></span>

   2. <span data-ttu-id="cdf59-130">定期的なジョブを設定するには、**再実行** を選び、繰り返しの情報を入植し、**OK** を選択します。</span><span class="sxs-lookup"><span data-stu-id="cdf59-130">To set up a recurring job, select **Recurrence**, enter the recurrence information, and the select **OK**.</span></span>

   3. <span data-ttu-id="cdf59-131">ジョブ警告を設定するには、**警告** を選び、入庫する警告を選択し、**OK** を選択します。</span><span class="sxs-lookup"><span data-stu-id="cdf59-131">To set up a job alert, select **Alerts**, select the alerts to receive, and then select **OK**.</span></span>

   4. <span data-ttu-id="cdf59-132">**OK** を選択します。</span><span class="sxs-lookup"><span data-stu-id="cdf59-132">Select **OK**.</span></span> <span data-ttu-id="cdf59-133">設定したパラメータで処理が実行されます。</span><span class="sxs-lookup"><span data-stu-id="cdf59-133">The process will run with the parameters you set.</span></span>

4. <span data-ttu-id="cdf59-134">**OK** を選択します。</span><span class="sxs-lookup"><span data-stu-id="cdf59-134">Select **OK**.</span></span>


[!INCLUDE[footer-include](../includes/footer-banner.md)]