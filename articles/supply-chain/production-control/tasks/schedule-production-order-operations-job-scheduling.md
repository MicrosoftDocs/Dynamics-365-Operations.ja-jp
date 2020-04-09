---
title: 工程とジョブのスケジューリングによる製造オーダーのスケジュール
description: このトピックでは、工程のスケジューリングとジョブのスケジューリングで製造オーダーのスケジューリングを行うことに焦点を当てています。
author: ChristianRytt
manager: AnnBe
ms.date: 08/19/2019
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ProdTableListPage, ProdTableCreate, InventItemIdLookupPurchase, ProdSchedule, ProdTable, ProdRouteJob
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: crytt
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 2181a84aea08aac0ddb202f7211dbda6330a3d49
ms.sourcegitcommit: fcb27d6a46cd544feef34f6ec7607bdd46b0c12b
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 03/18/2020
ms.locfileid: "3148840"
---
# <a name="schedule-a-production-order-with-operations-and-job-scheduling"></a><span data-ttu-id="c7dc8-103">工程とジョブのスケジューリングによる製造オーダーのスケジュール</span><span class="sxs-lookup"><span data-stu-id="c7dc8-103">Schedule a production order with operations and job scheduling</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="c7dc8-104">このトピックでは、工程のスケジューリングとジョブのスケジューリングで製造オーダーのスケジューリングを行うことに焦点を当てています。</span><span class="sxs-lookup"><span data-stu-id="c7dc8-104">This topic focuses on scheduling a production order with operations scheduling and job scheduling.</span></span> <span data-ttu-id="c7dc8-105">ジョブは、ジョブのスケジューリングで作成されますが、工程のスケジューリングでは作成されません。</span><span class="sxs-lookup"><span data-stu-id="c7dc8-105">No jobs are created with operations scheduling whereas jobs are created with job scheduling.</span></span> <span data-ttu-id="c7dc8-106">このタスクの作成に使用するデモ データの会社は USMF です。</span><span class="sxs-lookup"><span data-stu-id="c7dc8-106">The demo data company used to create this task is USMF.</span></span> <span data-ttu-id="c7dc8-107">この手順は、個別の製造環境で作業をしている生産マネージャ、生産計画担当者、または作業現場の監督を対象としています。</span><span class="sxs-lookup"><span data-stu-id="c7dc8-107">This procedure is intended for the production manager, production planner, or shop floor supervisor working in a discrete manufacturing environment.</span></span>


## <a name="create-a-production-order"></a><span data-ttu-id="c7dc8-108">製造オーダーの作成</span><span class="sxs-lookup"><span data-stu-id="c7dc8-108">Create a production order</span></span>
1. <span data-ttu-id="c7dc8-109">ナビゲーション ウィンドウで、**モジュール > 生産管理 > 製造オーダー > すべての製造オーダー**の順に移動します。</span><span class="sxs-lookup"><span data-stu-id="c7dc8-109">In the navigation pane, go to **Modules > Production control > Production orders > All production orders**.</span></span>
2. <span data-ttu-id="c7dc8-110">**新しい製造オーダー**を選択します。</span><span class="sxs-lookup"><span data-stu-id="c7dc8-110">Select **New production order**.</span></span>
3. <span data-ttu-id="c7dc8-111">**品目番号グループ** フィールドで、値を入力または選択します。</span><span class="sxs-lookup"><span data-stu-id="c7dc8-111">In the **Item number** field, enter or select a value.</span></span> <span data-ttu-id="c7dc8-112">品目番号 **D0001** を選択します。</span><span class="sxs-lookup"><span data-stu-id="c7dc8-112">Select Item number **D0001**.</span></span>  
4. <span data-ttu-id="c7dc8-113">**作成**を選択します。</span><span class="sxs-lookup"><span data-stu-id="c7dc8-113">Select **Create**.</span></span>

## <a name="schedule-operations-for-the-production-order"></a><span data-ttu-id="c7dc8-114">製造オーダの工程のスケジュール</span><span class="sxs-lookup"><span data-stu-id="c7dc8-114">Schedule operations for the production order</span></span>
1. <span data-ttu-id="c7dc8-115">新しく作成された行をマークします。</span><span class="sxs-lookup"><span data-stu-id="c7dc8-115">Mark the newly created row.</span></span>      
2. <span data-ttu-id="c7dc8-116">アクション ウィンドウで、**スケジュール**を選択します。</span><span class="sxs-lookup"><span data-stu-id="c7dc8-116">On the Action Pane, select **Schedule**.</span></span>
3. <span data-ttu-id="c7dc8-117">**工程のスケジュール**を選択します。</span><span class="sxs-lookup"><span data-stu-id="c7dc8-117">Select **Schedule operations**.</span></span>
4. <span data-ttu-id="c7dc8-118">**スケジューリング指示**のフィールドで、**スケジューリングの日付からフォワード**を選択します。</span><span class="sxs-lookup"><span data-stu-id="c7dc8-118">In the **Scheduling direction** field, select **Forward from scheduling date**.</span></span>
5. <span data-ttu-id="c7dc8-119">**スケジューリングの日付**フィールドに、日付を入力します。</span><span class="sxs-lookup"><span data-stu-id="c7dc8-119">In the **Scheduling date** field, enter a date.</span></span> <span data-ttu-id="c7dc8-120">将来期日、たとえば、今日とさらに 1 週間を選択します。</span><span class="sxs-lookup"><span data-stu-id="c7dc8-120">Select a future date, for example, today plus one week.</span></span> <span data-ttu-id="c7dc8-121">選択されたスケジューリング指示で、製造オーダーは、この日付を起点としてスケジューリングされます。</span><span class="sxs-lookup"><span data-stu-id="c7dc8-121">With the selected Scheduling direction, the production order will be scheduled forward from this date.</span></span>  
6. <span data-ttu-id="c7dc8-122">**OK** を選択します。</span><span class="sxs-lookup"><span data-stu-id="c7dc8-122">Select **OK**.</span></span>
7. <span data-ttu-id="c7dc8-123">一覧で、選択された行をマークします。</span><span class="sxs-lookup"><span data-stu-id="c7dc8-123">In the list, mark the selected row.</span></span> <span data-ttu-id="c7dc8-124">ステータスが**スケジュール済**に変わることに注意してください。</span><span class="sxs-lookup"><span data-stu-id="c7dc8-124">Note that the status is changed to **Scheduled**.</span></span> 
8. <span data-ttu-id="c7dc8-125">**すべてのジョブ**を選択します。</span><span class="sxs-lookup"><span data-stu-id="c7dc8-125">Select **All jobs**.</span></span> <span data-ttu-id="c7dc8-126">ジョブは、工程のスケジューリングで作成されないことに注意してください。</span><span class="sxs-lookup"><span data-stu-id="c7dc8-126">Note that no jobs are created with operations scheduling.</span></span>  
9. <span data-ttu-id="c7dc8-127">ページを閉じます。</span><span class="sxs-lookup"><span data-stu-id="c7dc8-127">Close the page.</span></span>

## <a name="schedule-jobs-for-the-production-order"></a><span data-ttu-id="c7dc8-128">製造オーダのジョブのスケジュール</span><span class="sxs-lookup"><span data-stu-id="c7dc8-128">Schedule jobs for the production order</span></span>
1. <span data-ttu-id="c7dc8-129">アクション ウィンドウで、**スケジュール**を選択します。</span><span class="sxs-lookup"><span data-stu-id="c7dc8-129">On the Action Pane, select **Schedule**.</span></span>
2. <span data-ttu-id="c7dc8-130">**ジョブのスケジュール**を選択します。</span><span class="sxs-lookup"><span data-stu-id="c7dc8-130">Select **Schedule jobs**.</span></span>
3. <span data-ttu-id="c7dc8-131">**スケジューリング指示**のフィールドで、**スケジューリングの日付からフォワード**を選択します。</span><span class="sxs-lookup"><span data-stu-id="c7dc8-131">In the **Scheduling direction** field, select **Forward from scheduling date**.</span></span>
4. <span data-ttu-id="c7dc8-132">**スケジューリングの日付**フィールドに、日付を入力します。</span><span class="sxs-lookup"><span data-stu-id="c7dc8-132">In the **Scheduling date** field, enter a date.</span></span> <span data-ttu-id="c7dc8-133">将来の日付、たとえば、今日とさらに 1 週間を選択します。</span><span class="sxs-lookup"><span data-stu-id="c7dc8-133">Select a date in the future, for example, today plus one week.</span></span> <span data-ttu-id="c7dc8-134">選択されたスケジューリング指示で、製造オーダーは、この日付を起点としてスケジューリングされます。</span><span class="sxs-lookup"><span data-stu-id="c7dc8-134">With the selected Scheduling direction, the production order will be scheduled forward from this date.</span></span>  
5. <span data-ttu-id="c7dc8-135">**OK** を選択します。</span><span class="sxs-lookup"><span data-stu-id="c7dc8-135">Select **OK**.</span></span>
6. <span data-ttu-id="c7dc8-136">アクション ウィンドウで、**製造オーダー**をクリックします。</span><span class="sxs-lookup"><span data-stu-id="c7dc8-136">On the Action Pane, select **Production order**.</span></span>
7. <span data-ttu-id="c7dc8-137">**すべてのジョブ**を選択します。</span><span class="sxs-lookup"><span data-stu-id="c7dc8-137">Select **All jobs**.</span></span> <span data-ttu-id="c7dc8-138">有効な工順に基づいて、ジョブ スケジューリングで5 つのジョブが作成されることに注意してください。</span><span class="sxs-lookup"><span data-stu-id="c7dc8-138">Note that based on the active route, 5 jobs are created with job scheduling.</span></span>  

