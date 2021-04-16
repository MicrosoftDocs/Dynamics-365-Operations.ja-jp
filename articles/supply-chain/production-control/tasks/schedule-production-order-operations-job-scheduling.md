---
title: 工程とジョブのスケジューリングによる製造オーダーのスケジュール
description: このトピックでは、工程のスケジューリングとジョブのスケジューリングで製造オーダーのスケジューリングを行うことに焦点を当てています。
author: ChristianRytt
ms.date: 08/19/2019
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: ProdTableListPage, ProdTableCreate, InventItemIdLookupPurchase, ProdSchedule, ProdTable, ProdRouteJob
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: crytt
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 883a68af78a9d91df089d30d8f1b3d7ba498d577
ms.sourcegitcommit: 0e8db169c3f90bd750826af76709ef5d621fd377
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/01/2021
ms.locfileid: "5841386"
---
# <a name="schedule-a-production-order-with-operations-and-job-scheduling"></a><span data-ttu-id="f7718-103">工程とジョブのスケジューリングによる製造オーダーのスケジュール</span><span class="sxs-lookup"><span data-stu-id="f7718-103">Schedule a production order with operations and job scheduling</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="f7718-104">このトピックでは、工程のスケジューリングとジョブのスケジューリングで製造オーダーのスケジューリングを行うことに焦点を当てています。</span><span class="sxs-lookup"><span data-stu-id="f7718-104">This topic focuses on scheduling a production order with operations scheduling and job scheduling.</span></span> <span data-ttu-id="f7718-105">ジョブは、ジョブのスケジューリングで作成されますが、工程のスケジューリングでは作成されません。</span><span class="sxs-lookup"><span data-stu-id="f7718-105">No jobs are created with operations scheduling whereas jobs are created with job scheduling.</span></span> <span data-ttu-id="f7718-106">このタスクの作成に使用するデモ データの会社は USMF です。</span><span class="sxs-lookup"><span data-stu-id="f7718-106">The demo data company used to create this task is USMF.</span></span> <span data-ttu-id="f7718-107">この手順は、個別の製造環境で作業をしている生産マネージャ、生産計画担当者、または作業現場の監督を対象としています。</span><span class="sxs-lookup"><span data-stu-id="f7718-107">This procedure is intended for the production manager, production planner, or shop floor supervisor working in a discrete manufacturing environment.</span></span>


## <a name="create-a-production-order"></a><span data-ttu-id="f7718-108">製造オーダーの作成</span><span class="sxs-lookup"><span data-stu-id="f7718-108">Create a production order</span></span>
1. <span data-ttu-id="f7718-109">ナビゲーション ウィンドウで、**モジュール > 生産管理 > 製造オーダー > すべての製造オーダー** の順に移動します。</span><span class="sxs-lookup"><span data-stu-id="f7718-109">In the navigation pane, go to **Modules > Production control > Production orders > All production orders**.</span></span>
2. <span data-ttu-id="f7718-110">**新しい製造オーダー** を選択します。</span><span class="sxs-lookup"><span data-stu-id="f7718-110">Select **New production order**.</span></span>
3. <span data-ttu-id="f7718-111">**品目番号グループ** フィールドで、値を入力または選択します。</span><span class="sxs-lookup"><span data-stu-id="f7718-111">In the **Item number** field, enter or select a value.</span></span> <span data-ttu-id="f7718-112">品目番号 **D0001** を選択します。</span><span class="sxs-lookup"><span data-stu-id="f7718-112">Select Item number **D0001**.</span></span>  
4. <span data-ttu-id="f7718-113">**作成** を選択します。</span><span class="sxs-lookup"><span data-stu-id="f7718-113">Select **Create**.</span></span>

## <a name="schedule-operations-for-the-production-order"></a><span data-ttu-id="f7718-114">製造オーダの工程のスケジュール</span><span class="sxs-lookup"><span data-stu-id="f7718-114">Schedule operations for the production order</span></span>
1. <span data-ttu-id="f7718-115">新しく作成された行をマークします。</span><span class="sxs-lookup"><span data-stu-id="f7718-115">Mark the newly created row.</span></span>      
2. <span data-ttu-id="f7718-116">アクション ウィンドウで、**スケジュール** を選択します。</span><span class="sxs-lookup"><span data-stu-id="f7718-116">On the Action Pane, select **Schedule**.</span></span>
3. <span data-ttu-id="f7718-117">**工程のスケジュール** を選択します。</span><span class="sxs-lookup"><span data-stu-id="f7718-117">Select **Schedule operations**.</span></span>
4. <span data-ttu-id="f7718-118">**スケジューリング指示** のフィールドで、**スケジューリングの日付からフォワード** を選択します。</span><span class="sxs-lookup"><span data-stu-id="f7718-118">In the **Scheduling direction** field, select **Forward from scheduling date**.</span></span>
5. <span data-ttu-id="f7718-119">**スケジューリングの日付** フィールドに、日付を入力します。</span><span class="sxs-lookup"><span data-stu-id="f7718-119">In the **Scheduling date** field, enter a date.</span></span> <span data-ttu-id="f7718-120">将来期日、たとえば、今日とさらに 1 週間を選択します。</span><span class="sxs-lookup"><span data-stu-id="f7718-120">Select a future date, for example, today plus one week.</span></span> <span data-ttu-id="f7718-121">選択されたスケジューリング指示で、製造オーダーは、この日付を起点としてスケジューリングされます。</span><span class="sxs-lookup"><span data-stu-id="f7718-121">With the selected Scheduling direction, the production order will be scheduled forward from this date.</span></span>  
6. <span data-ttu-id="f7718-122">**OK** を選択します。</span><span class="sxs-lookup"><span data-stu-id="f7718-122">Select **OK**.</span></span>
7. <span data-ttu-id="f7718-123">一覧で、選択された行をマークします。</span><span class="sxs-lookup"><span data-stu-id="f7718-123">In the list, mark the selected row.</span></span> <span data-ttu-id="f7718-124">ステータスが **スケジュール済** に変わることに注意してください。</span><span class="sxs-lookup"><span data-stu-id="f7718-124">Note that the status is changed to **Scheduled**.</span></span> 
8. <span data-ttu-id="f7718-125">**すべてのジョブ** を選択します。</span><span class="sxs-lookup"><span data-stu-id="f7718-125">Select **All jobs**.</span></span> <span data-ttu-id="f7718-126">ジョブは、工程のスケジューリングで作成されないことに注意してください。</span><span class="sxs-lookup"><span data-stu-id="f7718-126">Note that no jobs are created with operations scheduling.</span></span>  
9. <span data-ttu-id="f7718-127">ページを閉じます。</span><span class="sxs-lookup"><span data-stu-id="f7718-127">Close the page.</span></span>

## <a name="schedule-jobs-for-the-production-order"></a><span data-ttu-id="f7718-128">製造オーダのジョブのスケジュール</span><span class="sxs-lookup"><span data-stu-id="f7718-128">Schedule jobs for the production order</span></span>
1. <span data-ttu-id="f7718-129">アクション ウィンドウで、**スケジュール** を選択します。</span><span class="sxs-lookup"><span data-stu-id="f7718-129">On the Action Pane, select **Schedule**.</span></span>
2. <span data-ttu-id="f7718-130">**ジョブのスケジュール** を選択します。</span><span class="sxs-lookup"><span data-stu-id="f7718-130">Select **Schedule jobs**.</span></span>
3. <span data-ttu-id="f7718-131">**スケジューリング指示** のフィールドで、**スケジューリングの日付からフォワード** を選択します。</span><span class="sxs-lookup"><span data-stu-id="f7718-131">In the **Scheduling direction** field, select **Forward from scheduling date**.</span></span>
4. <span data-ttu-id="f7718-132">**スケジューリングの日付** フィールドに、日付を入力します。</span><span class="sxs-lookup"><span data-stu-id="f7718-132">In the **Scheduling date** field, enter a date.</span></span> <span data-ttu-id="f7718-133">将来の日付、たとえば、今日とさらに 1 週間を選択します。</span><span class="sxs-lookup"><span data-stu-id="f7718-133">Select a date in the future, for example, today plus one week.</span></span> <span data-ttu-id="f7718-134">選択されたスケジューリング指示で、製造オーダーは、この日付を起点としてスケジューリングされます。</span><span class="sxs-lookup"><span data-stu-id="f7718-134">With the selected Scheduling direction, the production order will be scheduled forward from this date.</span></span>  
5. <span data-ttu-id="f7718-135">**OK** を選択します。</span><span class="sxs-lookup"><span data-stu-id="f7718-135">Select **OK**.</span></span>
6. <span data-ttu-id="f7718-136">アクション ウィンドウで、**製造オーダー** をクリックします。</span><span class="sxs-lookup"><span data-stu-id="f7718-136">On the Action Pane, select **Production order**.</span></span>
7. <span data-ttu-id="f7718-137">**すべてのジョブ** を選択します。</span><span class="sxs-lookup"><span data-stu-id="f7718-137">Select **All jobs**.</span></span> <span data-ttu-id="f7718-138">有効な工順に基づいて、ジョブ スケジューリングで5 つのジョブが作成されることに注意してください。</span><span class="sxs-lookup"><span data-stu-id="f7718-138">Note that based on the active route, 5 jobs are created with job scheduling.</span></span>  



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]