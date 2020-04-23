---
title: かんばん作業と材料の転送
description: この手順では、かんばん回収作業を実行し、材料を転送することに焦点をあてます。
author: ChristianRytt
manager: tfehr
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: KanbanBoardTransferJob
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: crytt
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 96cb77b7b37fe6519a812735d9a41749da078cf2
ms.sourcegitcommit: 4f9912439ff78acf0c754d5bff972c4b85763093
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/02/2020
ms.locfileid: "3210367"
---
# <a name="transfer-materials-with-kanban-jobs"></a><span data-ttu-id="6f2bf-103">かんばん作業と材料の転送</span><span class="sxs-lookup"><span data-stu-id="6f2bf-103">Transfer materials with kanban jobs</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="6f2bf-104">この手順では、かんばん回収作業を実行し、材料を転送することに焦点をあてます。</span><span class="sxs-lookup"><span data-stu-id="6f2bf-104">This procedure focuses on executing a withdrawal kanban job to transfer materials.</span></span> <span data-ttu-id="6f2bf-105">この手順の作成に使用するデモ データの会社は USMF です。</span><span class="sxs-lookup"><span data-stu-id="6f2bf-105">The demo data company used to create this procedure is USMF.</span></span> <span data-ttu-id="6f2bf-106">この手順は、倉庫作業者を対象としています。</span><span class="sxs-lookup"><span data-stu-id="6f2bf-106">This procedure is intended for the warehouse worker.</span></span>


## <a name="display-transfer-jobs"></a><span data-ttu-id="6f2bf-107">転送ジョブの表示</span><span class="sxs-lookup"><span data-stu-id="6f2bf-107">Display transfer jobs</span></span>
1. <span data-ttu-id="6f2bf-108">[生産管理] > [かんばん] > [転送ジョブのかんばんボード] の順に移動します。</span><span class="sxs-lookup"><span data-stu-id="6f2bf-108">Go to Production control > Kanban > Kanban board for transfer jobs.</span></span>
2. <span data-ttu-id="6f2bf-109">[フィルター] セクションを展開または折りたたみます。</span><span class="sxs-lookup"><span data-stu-id="6f2bf-109">Expand or collapse the Filters section.</span></span>
    * <span data-ttu-id="6f2bf-110">[フィルター] セクションで、[生産フロー]、[活動名]、[移動元倉庫と移動元場所]、[移動先倉庫と移動先場所] にフィルターを使用すると、表示するジョブを指定できます。</span><span class="sxs-lookup"><span data-stu-id="6f2bf-110">In the Filters section, you can specify what jobs you want to see by filtering on Production flow, Activity name, From warehouse and location, and To warehouse and location.</span></span>  
3. <span data-ttu-id="6f2bf-111">[元倉庫] フィールドに、「11」と入力します。</span><span class="sxs-lookup"><span data-stu-id="6f2bf-111">In the From warehouse field, type '11'.</span></span>
4. <span data-ttu-id="6f2bf-112">[移動先場所] フィールドに、「12」と入力します。</span><span class="sxs-lookup"><span data-stu-id="6f2bf-112">In the To location field, type '12'.</span></span>

## <a name="start-a-transfer-job"></a><span data-ttu-id="6f2bf-113">転送ジョブの開始</span><span class="sxs-lookup"><span data-stu-id="6f2bf-113">Start a transfer job</span></span>
1. <span data-ttu-id="6f2bf-114">一覧で、選択された行 (ある場合) を選択解除します。</span><span class="sxs-lookup"><span data-stu-id="6f2bf-114">In the list, deselect the selected row - if any.</span></span>
2. <span data-ttu-id="6f2bf-115">一覧で行 4 を選択します。</span><span class="sxs-lookup"><span data-stu-id="6f2bf-115">In the list, select row 4.</span></span>
    * <span data-ttu-id="6f2bf-116">ステータスが [未定] である最初のジョブを選択します。</span><span class="sxs-lookup"><span data-stu-id="6f2bf-116">Select the first job with status Not planned.</span></span> <span data-ttu-id="6f2bf-117">これが選択した唯一のジョブであることを確認します。</span><span class="sxs-lookup"><span data-stu-id="6f2bf-117">Make sure this is the only job selected.</span></span>  
3. <span data-ttu-id="6f2bf-118">[開始] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="6f2bf-118">Click Start.</span></span>
    * <span data-ttu-id="6f2bf-119">アイコンはジョブが開始されることを示します。</span><span class="sxs-lookup"><span data-stu-id="6f2bf-119">Notice that an icon indicates that the job is started.</span></span>  

## <a name="select-a-second-transfer-job-and-change-quantity"></a><span data-ttu-id="6f2bf-120">2 番目の配送ジョブを選択して数量を変更する</span><span class="sxs-lookup"><span data-stu-id="6f2bf-120">Select a second transfer job and change quantity</span></span>
1. <span data-ttu-id="6f2bf-121">一覧で、目的のレコードを見つけ、選択します。</span><span class="sxs-lookup"><span data-stu-id="6f2bf-121">In the list, find and select the desired record.</span></span>
    * <span data-ttu-id="6f2bf-122">複数のジョブを選択できますが、とりあえず 5 行目を選択します。</span><span class="sxs-lookup"><span data-stu-id="6f2bf-122">You can have multiple jobs selected, but for now select row 5.</span></span>  
2. <span data-ttu-id="6f2bf-123">一覧で、目的のレコードを見つけ、選択します。</span><span class="sxs-lookup"><span data-stu-id="6f2bf-123">In the list, find and select the desired record.</span></span>
    * <span data-ttu-id="6f2bf-124">以前の手順でジョブ 1 つのみが選択されたことを確認します。</span><span class="sxs-lookup"><span data-stu-id="6f2bf-124">Make sure the job in the previous step is the only one selected.</span></span> <span data-ttu-id="6f2bf-125">他のすべてのジョブを選択解除します。</span><span class="sxs-lookup"><span data-stu-id="6f2bf-125">Deselect all other jobs.</span></span>  
3. <span data-ttu-id="6f2bf-126">後で参照するために、ジョブ数量フィールドの値をメモする</span><span class="sxs-lookup"><span data-stu-id="6f2bf-126">Note the value in the Job quantity field to reference later</span></span>
4. <span data-ttu-id="6f2bf-127">[ジョブ数量] を「30」に設定します。</span><span class="sxs-lookup"><span data-stu-id="6f2bf-127">Set Job quantity to '30'.</span></span>
    * <span data-ttu-id="6f2bf-128">警告です!</span><span class="sxs-lookup"><span data-stu-id="6f2bf-128">Notice the warning!</span></span> <span data-ttu-id="6f2bf-129">30 を転送することはできません。</span><span class="sxs-lookup"><span data-stu-id="6f2bf-129">You are not allowed to transfer 30.</span></span> <span data-ttu-id="6f2bf-130">かんばんルールの設定に従って、元の数量のみを転送できます。</span><span class="sxs-lookup"><span data-stu-id="6f2bf-130">According to the setup of the kanban rule, you can only transfer the original quantity.</span></span>  
5. <span data-ttu-id="6f2bf-131">ジョブ数量フィールドに以前にメモした値を使用する</span><span class="sxs-lookup"><span data-stu-id="6f2bf-131">Use the value noted previously in the Job quantity field</span></span>
    * <span data-ttu-id="6f2bf-132">以前の値にジョブ数量を設定します。</span><span class="sxs-lookup"><span data-stu-id="6f2bf-132">Set the Job quantity to the previous value.</span></span>  

## <a name="start-the-second-transfer-job"></a><span data-ttu-id="6f2bf-133">2 番目の配送ジョブの開始</span><span class="sxs-lookup"><span data-stu-id="6f2bf-133">Start the second transfer job</span></span>
1. <span data-ttu-id="6f2bf-134">[開始] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="6f2bf-134">Click Start.</span></span>
    * <span data-ttu-id="6f2bf-135">これにより、5 行目のジョブの転送が開始されます。</span><span class="sxs-lookup"><span data-stu-id="6f2bf-135">This will start the transfer of the job in row 5.</span></span>  

## <a name="complete-both-transfer-jobs"></a><span data-ttu-id="6f2bf-136">両方の転送ジョブの完了</span><span class="sxs-lookup"><span data-stu-id="6f2bf-136">Complete both transfer jobs</span></span>
1. <span data-ttu-id="6f2bf-137">一覧で行 4 を選択します。</span><span class="sxs-lookup"><span data-stu-id="6f2bf-137">In the list, select row 4.</span></span>
    * <span data-ttu-id="6f2bf-138">2 つの転送ジョブが 4 行目、5 行目で選択されました。</span><span class="sxs-lookup"><span data-stu-id="6f2bf-138">Now two transfer jobs are selected on row 4 and row 5.</span></span>  
2. <span data-ttu-id="6f2bf-139">[完了] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="6f2bf-139">Click Complete.</span></span>
    * <span data-ttu-id="6f2bf-140">これで、両方のジョブの転送が完了します。</span><span class="sxs-lookup"><span data-stu-id="6f2bf-140">This will complete the transfer of both jobs.</span></span>  

