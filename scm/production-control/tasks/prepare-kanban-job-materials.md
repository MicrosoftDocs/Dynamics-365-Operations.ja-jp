--- 
title: "作業セルで材料が利用可能な場合にプロセスかんばん作業を準備"
description: "このタスクでは、作業セルですべての材料が利用可能な場合にプロセスかんばん作業を準備することに焦点をあてます。"
author: johanhoffmann
manager: AnnBe
ms.date: 11/11/2016
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: bis
ms.search.scope: Operations
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: johanho
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 663da58ef01b705c0c984fbfd3fce8bc31be04c6
ms.openlocfilehash: 62f3f71cc5e47f0fb027211a911e61673ca2e375
ms.contentlocale: ja-jp
ms.lasthandoff: 08/29/2017

---
# <a name="prepare-a-process-kanban-job-when-materials-are-available-for-the-work-cell"></a><span data-ttu-id="6cfd4-103">作業セルで材料が利用可能な場合にプロセスかんばん作業を準備</span><span class="sxs-lookup"><span data-stu-id="6cfd4-103">Prepare a process kanban job when materials are available for the work cell</span></span>

[!include[task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="6cfd4-104">このタスクでは、作業セルですべての材料が利用可能な場合にプロセスかんばん作業を準備することに焦点をあてます。</span><span class="sxs-lookup"><span data-stu-id="6cfd4-104">This task focuses on preparing a process kanban job when all materials are available for the work cell.</span></span> <span data-ttu-id="6cfd4-105">このタスクの作成に使用するデモ データの会社は USMF です。</span><span class="sxs-lookup"><span data-stu-id="6cfd4-105">The demo data company used to create this task is USMF.</span></span> <span data-ttu-id="6cfd4-106">このタスクは、機械オペレーターを対象としています。</span><span class="sxs-lookup"><span data-stu-id="6cfd4-106">This task is intended for the machine operator.</span></span>

1. <span data-ttu-id="6cfd4-107">[プロセス ジョブのかんばんボード] に移動します。</span><span class="sxs-lookup"><span data-stu-id="6cfd4-107">Go to Kanban board for process jobs.</span></span>
2. <span data-ttu-id="6cfd4-108">[作業セル] フィールドで、ドロップ ダウン ボタンをクリックし、ルックアップを開きます。</span><span class="sxs-lookup"><span data-stu-id="6cfd4-108">In the Work cell field, click the drop-down button to open the lookup.</span></span>
3. <span data-ttu-id="6cfd4-109">一覧で、選択された行のリンクをクリックします。</span><span class="sxs-lookup"><span data-stu-id="6cfd4-109">In the list, click the link in the selected row.</span></span>
    * <span data-ttu-id="6cfd4-110">作業セル 1250 を選択し、[OK] をクリックします</span><span class="sxs-lookup"><span data-stu-id="6cfd4-110">Select work cell 1250 and click OK.</span></span>  
4. <span data-ttu-id="6cfd4-111">一覧で行 4 を選択します。</span><span class="sxs-lookup"><span data-stu-id="6cfd4-111">In the list, select row 4.</span></span>
    * <span data-ttu-id="6cfd4-112">クリーンなデモ会社では、4 行目のかんばん「000329」はまだ完了していない最初のジョブです。</span><span class="sxs-lookup"><span data-stu-id="6cfd4-112">In the clean demo company, Kanban 000329 in row 4 is the first job that is not completed yet.</span></span>  
5. <span data-ttu-id="6cfd4-113">[ピッキング リスト] セクションの展開を切り替えます。</span><span class="sxs-lookup"><span data-stu-id="6cfd4-113">Toggle the expansion of the Picking list section.</span></span>
    * <span data-ttu-id="6cfd4-114">供給のステータスがピッキング リストのすべての品目に対して使用できることを確認します。</span><span class="sxs-lookup"><span data-stu-id="6cfd4-114">Verify that the supply status is available for all items in the picking list.</span></span>  
    * <span data-ttu-id="6cfd4-115">複数のジョブが選択されている場合、ピッキング リストには、選択したジョブに必要なすべての品目の合計が表示されます。</span><span class="sxs-lookup"><span data-stu-id="6cfd4-115">If multiple jobs are selected, the picking list will show the sum of all items needed for the selected jobs.</span></span>  
6. <span data-ttu-id="6cfd4-116">[準備] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="6cfd4-116">Click Prepare.</span></span>
    * <span data-ttu-id="6cfd4-117">準備プロセスは完了です。</span><span class="sxs-lookup"><span data-stu-id="6cfd4-117">The preparation process is now completed.</span></span> <span data-ttu-id="6cfd4-118">ピッキング リストのすべての行に関連する選択済みのチェック ボックスは、供給のステータスがピッキングされていることを示します。</span><span class="sxs-lookup"><span data-stu-id="6cfd4-118">The selected check box for all rows in the picking list indicates that the supply status is picked.</span></span>  

