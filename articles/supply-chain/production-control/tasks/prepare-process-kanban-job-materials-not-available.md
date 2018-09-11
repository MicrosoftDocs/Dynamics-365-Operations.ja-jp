--- 
title: "作業セルで材料が利用不可の場合にプロセスかんばん作業を準備"
description: "この手順では、作業セルで材料が利用不可能な場合にプロセスかんばん作業を準備することに焦点をあてるため、倉庫からの材料をピッキングすることが必要です。"
author: ChristianRytt
manager: AnnBe
ms.date: 8/29/2018
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: KanbanBoardWorkCell
audience: Application User
ms.reviewer: shylaw
ms.search.scope: Core, Operations
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: crytt
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 32d71167fdad65cb1dec37671999a497759ca484
ms.openlocfilehash: 80bd786b1c891be1ae8d0f1ea0670133313e8991
ms.contentlocale: ja-jp
ms.lasthandoff: 09/11/2018

---
# <a name="prepare-a-process-kanban-job-when-materials-are-not-available-for-the-work-cell"></a><span data-ttu-id="74e1a-103">作業セルで材料が利用不可の場合にプロセスかんばん作業を準備</span><span class="sxs-lookup"><span data-stu-id="74e1a-103">Prepare a process kanban job when materials are not available for the work cell</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="74e1a-104">この手順では、作業セルで材料が利用不可能な場合にプロセスかんばん作業を準備することに焦点をあてるため、倉庫からの材料をピッキングすることが必要です。</span><span class="sxs-lookup"><span data-stu-id="74e1a-104">This procedure focuses on preparing a process kanban job when some materials are not available for the work cell, therefore it's necessary to pick materials from the warehouse.</span></span> <span data-ttu-id="74e1a-105">「材料が利用可能な場合にプロセスかんばん作業を準備する」という手順は、この手順を作成するための前提条件です。</span><span class="sxs-lookup"><span data-stu-id="74e1a-105">The procedure "Prepare a process kanban job when materials are available" is a prerequisite for creating this procedure.</span></span> <span data-ttu-id="74e1a-106">この手順は、機械オペレーターを対象としています。</span><span class="sxs-lookup"><span data-stu-id="74e1a-106">This procedure is intended for the machine operator.</span></span> <span data-ttu-id="74e1a-107">この手順の作成に使用するデモ データの会社は USMF です。</span><span class="sxs-lookup"><span data-stu-id="74e1a-107">The demo data company used to create this procedure is USMF.</span></span>

1. <span data-ttu-id="74e1a-108">[生産管理] > [かんばん] > [プロセス ジョブのかんばんボード] の順に移動します。</span><span class="sxs-lookup"><span data-stu-id="74e1a-108">Go to Production control > Kanban > Kanban board for process jobs.</span></span>
2. <span data-ttu-id="74e1a-109">[作業セル] フィールドで、ドロップ ダウン ボタンをクリックし、ルックアップを開きます。</span><span class="sxs-lookup"><span data-stu-id="74e1a-109">In the Work cell field, click the drop-down button to open the lookup.</span></span>
3. <span data-ttu-id="74e1a-110">一覧で、選択された行のリンクをクリックします。</span><span class="sxs-lookup"><span data-stu-id="74e1a-110">In the list, click the link in the selected row.</span></span>
    * <span data-ttu-id="74e1a-111">作業セル 1250 を選択します。</span><span class="sxs-lookup"><span data-stu-id="74e1a-111">Select work cell 1250.</span></span>  
4. <span data-ttu-id="74e1a-112">一覧で、目的のレコードを見つけ、選択します。</span><span class="sxs-lookup"><span data-stu-id="74e1a-112">In the list, find and select the desired record.</span></span>
    * <span data-ttu-id="74e1a-113">「かんばん 000356」を選択します。</span><span class="sxs-lookup"><span data-stu-id="74e1a-113">Select Kanban 000356.</span></span>  
5. <span data-ttu-id="74e1a-114">一覧で、目的のレコードを見つけ、選択します。</span><span class="sxs-lookup"><span data-stu-id="74e1a-114">In the list, find and select the desired record.</span></span>
    * <span data-ttu-id="74e1a-115">一覧で、行 4 を選択解除します。</span><span class="sxs-lookup"><span data-stu-id="74e1a-115">In the list, deselect row 4.</span></span> <span data-ttu-id="74e1a-116">または、「材料が利用可能な場合にプロセスかんばん作業を準備する」というタスクが完了していない場合は、行 4 を選択します。</span><span class="sxs-lookup"><span data-stu-id="74e1a-116">or Select row 4 if you haven't completed the task "Prepare a process kanban job when materials are available."</span></span>  
6. <span data-ttu-id="74e1a-117">[ピッキング リスト] セクションの展開を切り替えます。</span><span class="sxs-lookup"><span data-stu-id="74e1a-117">Toggle the expansion of the Picking list section.</span></span>
    * <span data-ttu-id="74e1a-118">供給のステータスにエントリー アイコンがないということは、品目「P0002」の 48 ea が作業セルに存在しないことを示します。</span><span class="sxs-lookup"><span data-stu-id="74e1a-118">The No entry icon in the supply status indicates that 48 ea of item P0002 are missing for the work cell.</span></span>  

## <a name="transfer-materials-to-work-cell"></a><span data-ttu-id="74e1a-119">材料を作業セルに移動する</span><span class="sxs-lookup"><span data-stu-id="74e1a-119">Transfer materials to work cell</span></span>
1. <span data-ttu-id="74e1a-120">[転送ジョブ] セクションの展開を切り替えます。</span><span class="sxs-lookup"><span data-stu-id="74e1a-120">Toggle the expansion of the Transfer jobs section.</span></span>
2. <span data-ttu-id="74e1a-121">クイック フィルターを使用して、'P0002' の値で品目番号フィールドにフィルターを適用します。</span><span class="sxs-lookup"><span data-stu-id="74e1a-121">Use the Quick Filter to filter on the Item number field with a value of 'P0002'.</span></span>
3. <span data-ttu-id="74e1a-122">一覧で、目的のレコードを見つけ、選択します。</span><span class="sxs-lookup"><span data-stu-id="74e1a-122">In the list, find and select the desired record.</span></span>
4. <span data-ttu-id="74e1a-123">[開始] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="74e1a-123">Click Start.</span></span>
    * <span data-ttu-id="74e1a-124">転送処理中です。</span><span class="sxs-lookup"><span data-stu-id="74e1a-124">Transfer is in progress.</span></span>  
5. <span data-ttu-id="74e1a-125">[完了] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="74e1a-125">Click Complete.</span></span>
    * <span data-ttu-id="74e1a-126">品目「P0002」は、かんばん作業のピッキング リストから使用可能です。</span><span class="sxs-lookup"><span data-stu-id="74e1a-126">Item P0002 is now available in the picking list for the kanban job.</span></span> <span data-ttu-id="74e1a-127">これは、必要なすべての材料でかんばんを準備することを意味します。</span><span class="sxs-lookup"><span data-stu-id="74e1a-127">This means that we can prepare the kanban with all the needed materials.</span></span>  
6. <span data-ttu-id="74e1a-128">[準備] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="74e1a-128">Click Prepare.</span></span>
    * <span data-ttu-id="74e1a-129">[ジョブ ステータス] にアイコンがあるということは、ジョブが準備が整っていることを意味します。</span><span class="sxs-lookup"><span data-stu-id="74e1a-129">Notice that an icon in the Job status indicates that the job is now ready.</span></span>  


