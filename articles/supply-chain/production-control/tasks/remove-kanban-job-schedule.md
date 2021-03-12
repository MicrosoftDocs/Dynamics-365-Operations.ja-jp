---
title: かんばん作業をスケジュールから削除する
description: この手順では、ジョブ ステータスを未定に戻すことによって、計画済みプロセスかんばんジョブをスケジュールから削除することに焦点をあてます。
author: ChristianRytt
manager: tfehr
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: KanbanJobSchedulingListPage, SysLookupMultiSelectGrid, KanbanJobStatusUpdate
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: crytt
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: fcd9247e24323ba606377d7e51bd4447ab51c905
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 01/15/2021
ms.locfileid: "4961618"
---
# <a name="remove-a-kanban-job-from-the-schedule"></a><span data-ttu-id="9ca01-103">かんばん作業をスケジュールから削除する</span><span class="sxs-lookup"><span data-stu-id="9ca01-103">Remove a kanban job from the schedule</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="9ca01-104">この手順では、ジョブ ステータスを未定に戻すことによって、計画済みプロセスかんばんジョブをスケジュールから削除することに焦点をあてます。</span><span class="sxs-lookup"><span data-stu-id="9ca01-104">This procedure focuses on removing a planned process kanban job from the schedule by reverting the job status to Not planned.</span></span> <span data-ttu-id="9ca01-105">この手順の作成に使用するデモ データの会社は USMF です。</span><span class="sxs-lookup"><span data-stu-id="9ca01-105">The demo data company used to create this procedure is USMF.</span></span> <span data-ttu-id="9ca01-106">この手順は、作業現場の監督または生産計画担当者を対象としています。</span><span class="sxs-lookup"><span data-stu-id="9ca01-106">This procedure is intended for the shop floor supervisor or production planner.</span></span>


## <a name="find-a-planned-kanban-job"></a><span data-ttu-id="9ca01-107">計画済かんばん作業を見つける</span><span class="sxs-lookup"><span data-stu-id="9ca01-107">Find a planned kanban job</span></span>
1. <span data-ttu-id="9ca01-108">[生産管理] > [かんばん] > [かんばん作業スケジューリング] の順に移動します。</span><span class="sxs-lookup"><span data-stu-id="9ca01-108">Go to Production control > Kanban > Kanban job scheduling.</span></span>
2. <span data-ttu-id="9ca01-109">[作業セル] フィールドで、ドロップ ダウン ボタンをクリックし、ルックアップを開きます。</span><span class="sxs-lookup"><span data-stu-id="9ca01-109">In the Work cell field, click the drop-down button to open the lookup.</span></span>
3. <span data-ttu-id="9ca01-110">一覧で、選択された行のリンクをクリックします。</span><span class="sxs-lookup"><span data-stu-id="9ca01-110">In the list, click the link in the selected row.</span></span>
    * <span data-ttu-id="9ca01-111">作業セル 1250 を選択します。</span><span class="sxs-lookup"><span data-stu-id="9ca01-111">Select work cell 1250.</span></span>  
4. <span data-ttu-id="9ca01-112">[選択] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="9ca01-112">Click Select.</span></span>
5. <span data-ttu-id="9ca01-113">[ジョブ ステータスの表示] フィールドでは、「スケジュール済み」を選択します。</span><span class="sxs-lookup"><span data-stu-id="9ca01-113">In the Display job status field, select 'Scheduled'.</span></span>

## <a name="remove-the-planned-kanban-job-from-the-schedule"></a><span data-ttu-id="9ca01-114">計画済かんばん作業をスケジュールから削除する</span><span class="sxs-lookup"><span data-stu-id="9ca01-114">Remove the planned kanban job from the schedule</span></span>
1. <span data-ttu-id="9ca01-115">一覧で、目的のレコードを見つけ、選択します。</span><span class="sxs-lookup"><span data-stu-id="9ca01-115">In the list, find and select the desired record.</span></span>
    * <span data-ttu-id="9ca01-116">たとえば、2012 年 12 月 19 日付のジョブなど、ステータスが計画済みとなっているジョブを選択します。</span><span class="sxs-lookup"><span data-stu-id="9ca01-116">Select a job that has the Planned status, for example, a job from December 19, 2012.</span></span>  
2. <span data-ttu-id="9ca01-117">アクション ウィンドウで、[計画] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="9ca01-117">On the Action Pane, click Plan.</span></span>
3. <span data-ttu-id="9ca01-118">[ジョブ ステータスを元に戻す] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="9ca01-118">Click Revert job status.</span></span>
4. <span data-ttu-id="9ca01-119">[OK] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="9ca01-119">Click OK.</span></span>
    * <span data-ttu-id="9ca01-120">これは、現在のジョブ ステータスを「計画済み」から「未定」に戻し、プロセス表から削除します。</span><span class="sxs-lookup"><span data-stu-id="9ca01-120">This will revert the current job status from 'Planned' to 'Not planned' and remove it from the process board.</span></span>   

