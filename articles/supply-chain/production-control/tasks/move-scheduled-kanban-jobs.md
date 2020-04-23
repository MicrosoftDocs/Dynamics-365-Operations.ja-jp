---
title: スケジュール済みかんばん作業の移動
description: この手順は、計画済のプロセスかんばんジョブを別の期間に移動することに焦点をあてます。
author: ChristianRytt
manager: tfehr
ms.date: 11/07/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: KanbanJobSchedulingListPage
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: crytt
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: bb95bab2173cb45300560f59c394cd2d558fe69f
ms.sourcegitcommit: 4f9912439ff78acf0c754d5bff972c4b85763093
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/02/2020
ms.locfileid: "3206982"
---
# <a name="move-scheduled-kanban-jobs"></a><span data-ttu-id="12a19-103">スケジュール済みかんばん作業の移動</span><span class="sxs-lookup"><span data-stu-id="12a19-103">Move scheduled kanban jobs</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="12a19-104">この手順は、計画済のプロセスかんばんジョブを別の期間に移動することに焦点をあてます。</span><span class="sxs-lookup"><span data-stu-id="12a19-104">This procedure focuses on moving planned process kanban jobs to a different period.</span></span> <span data-ttu-id="12a19-105">この手順の作成に使用するデモ データの会社は USMF です。</span><span class="sxs-lookup"><span data-stu-id="12a19-105">The demo data company used to create this procedure is USMF.</span></span> <span data-ttu-id="12a19-106">この手順は、かんばんを処理する作業現場の監督または生産計画担当者を対象としています。</span><span class="sxs-lookup"><span data-stu-id="12a19-106">This procedure is intended for the shop floor supervisor or production planner working with kanbans.</span></span>

## <a name="select-scheduled-kanban-jobs"></a><span data-ttu-id="12a19-107">スケジュール済みかんばん作業を選択します。</span><span class="sxs-lookup"><span data-stu-id="12a19-107">Select scheduled kanban jobs.</span></span> 

1. <span data-ttu-id="12a19-108">**生産管理 > かんばん > かんばん作業スケジューリング**の順に移動します。</span><span class="sxs-lookup"><span data-stu-id="12a19-108">Go to **Production control > Kanban > Kanban job scheduling**.</span></span> 

2. <span data-ttu-id="12a19-109">**作業セル**フィールドで、ドロップ ダウン ボタンをクリックし、ルックアップを開きます。</span><span class="sxs-lookup"><span data-stu-id="12a19-109">In the **Work cell** field, click the drop-down button to open the lookup.</span></span> 

3. <span data-ttu-id="12a19-110">一覧で、選択された行をマークします。</span><span class="sxs-lookup"><span data-stu-id="12a19-110">In the list, mark the selected row.</span></span> 
   - <span data-ttu-id="12a19-111">作業セル 1250 を選択します。</span><span class="sxs-lookup"><span data-stu-id="12a19-111">Select work cell 1250.</span></span> 
4. <span data-ttu-id="12a19-112">**選択** をクリックします。</span><span class="sxs-lookup"><span data-stu-id="12a19-112">Click **Select**.</span></span> 

5. <span data-ttu-id="12a19-113">**ジョブ ステータスの表示**フィールドでは、**スケジュール済み**を選択します。</span><span class="sxs-lookup"><span data-stu-id="12a19-113">In the **Display job status** field, select **Scheduled**.</span></span> <span data-ttu-id="12a19-114">これは、スケジュール済のかんばんジョブのみを表示するジョブ一覧をフィルタ処理します。</span><span class="sxs-lookup"><span data-stu-id="12a19-114">This filters the job list to display only the scheduled kanban jobs.</span></span> 

## <a name="move-kanban-jobs-to-a-different-period"></a><span data-ttu-id="12a19-115">かんばん作業を別の期間へ移動します。</span><span class="sxs-lookup"><span data-stu-id="12a19-115">Move kanban jobs to a different period.</span></span> 

1. <span data-ttu-id="12a19-116">一覧で、目的のレコードを見つけ、選択します。</span><span class="sxs-lookup"><span data-stu-id="12a19-116">In the list, find and select the desired record.</span></span> <span data-ttu-id="12a19-117">たとえば、**計画期間**フィールドにある 2012 年 12 月 20 日にスケジュールされたジョブなど、ジョブ ステータスが**計画済み**となっているジョブを選択します。</span><span class="sxs-lookup"><span data-stu-id="12a19-117">Select a job that has the **Planned job** status, for example, a job scheduled on December 20, 2012 in the **Planned period** field.</span></span> <span data-ttu-id="12a19-118">その後、ジョブを以前の期間に移動します。</span><span class="sxs-lookup"><span data-stu-id="12a19-118">Then move the job to the previous period.</span></span> 

2. <span data-ttu-id="12a19-119">**前期**をクリックします。</span><span class="sxs-lookup"><span data-stu-id="12a19-119">Click **Previous period**.</span></span> 

3. <span data-ttu-id="12a19-120">**終了**をクリックすると、前期の最後のジョブとしてジョブ リストの最後にジョブが移動されます。</span><span class="sxs-lookup"><span data-stu-id="12a19-120">Click **End** to move the job to the end of the job list as the last job in the previous period.</span></span> 

4. <span data-ttu-id="12a19-121">一覧で、目的のレコードを見つけ、選択します。</span><span class="sxs-lookup"><span data-stu-id="12a19-121">In the list, find and select the desired record.</span></span> <span data-ttu-id="12a19-122">たとえば、**計画期間**フィールドにある 2012 年 12 月 18 日にスケジュールされたジョブなど、ジョブ ステータスが**計画済み**となっているジョブを選択します。</span><span class="sxs-lookup"><span data-stu-id="12a19-122">Select a job that has the **Planned job** status, for example, a job scheduled on December 18, 2012 in the **Planned period** field.</span></span> <span data-ttu-id="12a19-123">その後、ジョブを次の期間に移動します。</span><span class="sxs-lookup"><span data-stu-id="12a19-123">Then move the job to the next period.</span></span> 

5. <span data-ttu-id="12a19-124">**次の期間**をクリックします。</span><span class="sxs-lookup"><span data-stu-id="12a19-124">Click **Next period**.</span></span> 

6. <span data-ttu-id="12a19-125">**開始**をクリックすると、前期の最初のジョブとしてジョブ リストの最初にジョブが移動されます。</span><span class="sxs-lookup"><span data-stu-id="12a19-125">Click **Start** to move the job to the start of the job list as the first job in the previous period.</span></span> 

## <a name="move-a-job-within-a-period"></a><span data-ttu-id="12a19-126">期間内へジョブを移動します。</span><span class="sxs-lookup"><span data-stu-id="12a19-126">Move a job within a period.</span></span> 

1. <span data-ttu-id="12a19-127">一覧で、目的のレコードを見つけ、選択します。</span><span class="sxs-lookup"><span data-stu-id="12a19-127">In the list, find and select the desired record.</span></span> <span data-ttu-id="12a19-128">たとえば、**計画期間**フィールドにある 2012 年 12 月 19 日にスケジュールされた 2 番目のジョブなど、ジョブ ステータスが計画済みとなっているジョブを選択します。</span><span class="sxs-lookup"><span data-stu-id="12a19-128">Select a job that has the Planned job status, for example, the second job scheduled on December 19, 2012 in the **Planned period** field.</span></span> <span data-ttu-id="12a19-129">その後、計画期間内にジョブを移動します。</span><span class="sxs-lookup"><span data-stu-id="12a19-129">Then move the job within the planned period.</span></span> 

2. <span data-ttu-id="12a19-130">**次**をクリックします。</span><span class="sxs-lookup"><span data-stu-id="12a19-130">Click **Forward**.</span></span> <span data-ttu-id="12a19-131">一覧でジョブが 1 行下へ移動することを確認します。</span><span class="sxs-lookup"><span data-stu-id="12a19-131">Notice that the job is moved one line down on the list.</span></span> 

3. <span data-ttu-id="12a19-132">**前**をクリックします。</span><span class="sxs-lookup"><span data-stu-id="12a19-132">Click **Backward**.</span></span> <span data-ttu-id="12a19-133">一覧でジョブが 1 行上へ移動することを確認します。</span><span class="sxs-lookup"><span data-stu-id="12a19-133">Notice that the job is moved one line up on the list.</span></span>
