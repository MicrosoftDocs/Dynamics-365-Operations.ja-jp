--- 
title: "かんばん作業状態を元に戻す"
description: "この手順は、間違ったかんばん作業ステータスを元に戻すことに焦点をあてます。"
author: YuyuScheller
manager: AnnBe
ms.date: 03/02/2016
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: yuyus
ms.search.scope: Operations
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: yuyus
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 663da58ef01b705c0c984fbfd3fce8bc31be04c6
ms.openlocfilehash: 55d359232da5f3087b1e6baed182a20da09aeff7
ms.contentlocale: ja-jp
ms.lasthandoff: 08/29/2017

---
# <a name="revert-kanban-job-status"></a><span data-ttu-id="61e46-103">かんばん作業状態を元に戻す</span><span class="sxs-lookup"><span data-stu-id="61e46-103">Revert kanban job status</span></span>

[!include[task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="61e46-104">この手順は、間違ったかんばん作業ステータスを元に戻すことに焦点をあてます。</span><span class="sxs-lookup"><span data-stu-id="61e46-104">This procedure focuses on reverting an incorrect kanban job status.</span></span> <span data-ttu-id="61e46-105">これは機械オペレーターが間違ったジョブを更新してしまった場合に、または誤って間違ったステータスを設定してしまった場合に役立ちます。</span><span class="sxs-lookup"><span data-stu-id="61e46-105">This is useful in case the machine operator updates the wrong job, or sets the wrong status by mistake.</span></span> <span data-ttu-id="61e46-106">この手順によって、かんばん作業が誤って作成時に登録された時に、ステータスが元に戻されます。</span><span class="sxs-lookup"><span data-stu-id="61e46-106">In this procedure, a kanban job is registered as prepared by mistake, and the status is reverted.</span></span> <span data-ttu-id="61e46-107">この手順の作成に使用するデモ データの会社は USMF です。</span><span class="sxs-lookup"><span data-stu-id="61e46-107">The demo data company used to create this procedure is USMF.</span></span> <span data-ttu-id="61e46-108">この手順は、リーン生産会社で働いている現場監督または機械オペレーターを対象としています。</span><span class="sxs-lookup"><span data-stu-id="61e46-108">This procedure is intended for the shop supervisor or machine operator working in a lean manufacturing company.</span></span>


## <a name="open-process-board-for-the-work-cell"></a><span data-ttu-id="61e46-109">作業セルのプロセス ボードを開く</span><span class="sxs-lookup"><span data-stu-id="61e46-109">Open process board for the work cell</span></span>
1. <span data-ttu-id="61e46-110">[プロセス ジョブのかんばんボード] に移動します。</span><span class="sxs-lookup"><span data-stu-id="61e46-110">Go to Kanban board for process jobs.</span></span>
2. <span data-ttu-id="61e46-111">[作業セル] フィールドで、値を入力または選択します。</span><span class="sxs-lookup"><span data-stu-id="61e46-111">In the Work cell field, enter or select a value.</span></span>
    * <span data-ttu-id="61e46-112">作業セル 1260 を選択します。</span><span class="sxs-lookup"><span data-stu-id="61e46-112">Select work cell 1260.</span></span>  

## <a name="prepare-kanban-job"></a><span data-ttu-id="61e46-113">かんばん作業の準備</span><span class="sxs-lookup"><span data-stu-id="61e46-113">Prepare kanban job</span></span>
1. <span data-ttu-id="61e46-114">[準備] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="61e46-114">Click Prepare.</span></span>
    * <span data-ttu-id="61e46-115">灰色表示であるために [準備] をクリックできない場合、選択したかんばん作業が、空のかんばんアイコンによって示される [計画済] ステータスになっていることを確認します。</span><span class="sxs-lookup"><span data-stu-id="61e46-115">If you can't click Prepare because it is grayed out, make sure that the selected kanban job has status Planned, which is indicated by the empty kanban icon.</span></span> <span data-ttu-id="61e46-116">[準備] が失敗した場合、[ピッキング リスト] のすべての材料が使用可能であることを確認します。</span><span class="sxs-lookup"><span data-stu-id="61e46-116">If Prepare fails, make sure that all materials in the Picking list are available.</span></span>  
2. <span data-ttu-id="61e46-117">リストから準備済のジョブを選択します。</span><span class="sxs-lookup"><span data-stu-id="61e46-117">In the list, select the prepared job.</span></span>
    * <span data-ttu-id="61e46-118">準備した最初のジョブを選択します。</span><span class="sxs-lookup"><span data-stu-id="61e46-118">Select the first job that you have just prepared.</span></span>  
    * <span data-ttu-id="61e46-119">内側が三角になっているかんばんアイコンが表示されることによって、ジョブのステータスが準備されていることを確認してください。</span><span class="sxs-lookup"><span data-stu-id="61e46-119">Notice that the jobs status is prepared, which is indicated with a triangle inside the kanban icon.</span></span>  

## <a name="revert-the-status-of-the-prepared-kanban-job"></a><span data-ttu-id="61e46-120">準備済かんばん作業の状態を元に戻す</span><span class="sxs-lookup"><span data-stu-id="61e46-120">Revert the status of the prepared kanban job</span></span>
1. <span data-ttu-id="61e46-121">一覧で、選択された行をマークします。</span><span class="sxs-lookup"><span data-stu-id="61e46-121">In the list, mark the selected row.</span></span>
    * <span data-ttu-id="61e46-122">準備した最初のジョブを選択します。</span><span class="sxs-lookup"><span data-stu-id="61e46-122">Select the first job that was prepared.</span></span>  
2. <span data-ttu-id="61e46-123">[アクション ペイン] 上で、[製造] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="61e46-123">On the Action Pane, click Manufacture.</span></span>
3. <span data-ttu-id="61e46-124">[状態を元に戻す] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="61e46-124">Click Revert status.</span></span>
    * <span data-ttu-id="61e46-125">次の条件があてはまる場合、代替かんばんルールを使用できます: - 補充方法は両方のルールとも同じです。</span><span class="sxs-lookup"><span data-stu-id="61e46-125">You can use an alternative kanban rule when the following conditions are true:  - The replenishment strategy is the same for both rules.</span></span>  <span data-ttu-id="61e46-126">- 生産フローのバージョンは両方のルールとも同じです。</span><span class="sxs-lookup"><span data-stu-id="61e46-126">- The version of the production flow is the same for both rules.</span></span>  <span data-ttu-id="61e46-127">- 供給製品は両方のルールとも同じです。</span><span class="sxs-lookup"><span data-stu-id="61e46-127">- The product that is supplied is the same for both rules.</span></span>  <span data-ttu-id="61e46-128">- かんばんルールの最終活動のように構成されている下流活動は、両方のルールとも同じである必要があります。</span><span class="sxs-lookup"><span data-stu-id="61e46-128">- Any downstream activities that are configured for the last activity of the kanban rules must be the same for both rules.</span></span>  <span data-ttu-id="61e46-129">- 同じ支給された在庫分析コードは両方のルール用に構成する必要があります。</span><span class="sxs-lookup"><span data-stu-id="61e46-129">- The same supplied inventory dimensions must be configured for both rules.</span></span>  <span data-ttu-id="61e46-130">- 材料取り扱い単位のステータスは [未割当] になっている必要があります。</span><span class="sxs-lookup"><span data-stu-id="61e46-130">- The status of the handling unit must be Not assigned.</span></span>  <span data-ttu-id="61e46-131">- イベントかんばんの構成が同じである必要があります。</span><span class="sxs-lookup"><span data-stu-id="61e46-131">- The configuration for event kanbans must be the same.</span></span>  
    * <span data-ttu-id="61e46-132">新しいステータスが [計画済] になっていることを確認します。</span><span class="sxs-lookup"><span data-stu-id="61e46-132">Ensure that the new status is Planned.</span></span>  
4. <span data-ttu-id="61e46-133">[OK] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="61e46-133">Click OK.</span></span>
5. <span data-ttu-id="61e46-134">一覧で、選択された行のマークを解除します。</span><span class="sxs-lookup"><span data-stu-id="61e46-134">In the list, unmark the selected row.</span></span>
    * <span data-ttu-id="61e46-135">同じジョブを選択します。</span><span class="sxs-lookup"><span data-stu-id="61e46-135">Select the same job.</span></span>  
    * <span data-ttu-id="61e46-136">空のかんばんアイコンによって示される、かんばん作業のジョブ ステータスが [計画済] に戻されていることを確認してください。</span><span class="sxs-lookup"><span data-stu-id="61e46-136">Notice that the job status for the kanban job is reverted to Planned, which is indicated by an empty kanban icon.</span></span>  

