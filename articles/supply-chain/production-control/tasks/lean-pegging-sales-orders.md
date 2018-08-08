--- 
title: "販売注文のリーン ペギング"
description: "この手順で、品目がかんばんで生産される販売明細行からペギング ツリーを検証することに集中します。"
author: ChristianRytt
manager: AnnBe
ms.date: 03/02/2016
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: josaw
ms.search.scope: Operations
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: crytt
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: d9747ba144d56c9410846769e5465372c89ea111
ms.openlocfilehash: 4d695ea58c331e9783404bb357edbe2af586ad19
ms.contentlocale: ja-jp
ms.lasthandoff: 08/07/2018

---
# <a name="lean-pegging-from-sales-orders"></a><span data-ttu-id="8a6f6-103">販売注文のリーン ペギング</span><span class="sxs-lookup"><span data-stu-id="8a6f6-103">Lean pegging from sales orders</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="8a6f6-104">この手順で、品目がかんばんで生産される販売明細行からペギング ツリーを検証することに集中します。</span><span class="sxs-lookup"><span data-stu-id="8a6f6-104">This procedure focuses on validating the pegging tree from a sales line where the item is produced with kanbans.</span></span> <span data-ttu-id="8a6f6-105">ペギング ツリーを検証すると、すべてのかんばん作業が計画済になります。</span><span class="sxs-lookup"><span data-stu-id="8a6f6-105">After validating the pegging tree, all the kanban jobs are planned.</span></span> <span data-ttu-id="8a6f6-106">これにより、すぐに生産を始められるようにする必要のある注文受付者の注文のシナリオに役立ちます。</span><span class="sxs-lookup"><span data-stu-id="8a6f6-106">This is useful for order scenarios where the order taker needs to ensure that production can start right away.</span></span> <span data-ttu-id="8a6f6-107">この手順の作成に使用するデモ データの会社は USMF です。</span><span class="sxs-lookup"><span data-stu-id="8a6f6-107">The demo data company used to create this procedure is USMF.</span></span> <span data-ttu-id="8a6f6-108">この手順は、リーン会社で働いている上級の受付者を対象としています。</span><span class="sxs-lookup"><span data-stu-id="8a6f6-108">This procedure is intended for the advanced order taker working in a lean company.</span></span>


## <a name="create-a-sales-order-for-a-kanban-controlled-item"></a><span data-ttu-id="8a6f6-109">かんばんの統制品目の販売注文の作成</span><span class="sxs-lookup"><span data-stu-id="8a6f6-109">Create a sales order for a kanban controlled item</span></span>
1. <span data-ttu-id="8a6f6-110">[すべての販売注文] に移動します。</span><span class="sxs-lookup"><span data-stu-id="8a6f6-110">Go to All sales orders.</span></span>
2. <span data-ttu-id="8a6f6-111">[新規] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="8a6f6-111">Click New.</span></span>
3. <span data-ttu-id="8a6f6-112">[顧客口座] フィールドで値を入力または選択します。</span><span class="sxs-lookup"><span data-stu-id="8a6f6-112">In the Customer account field, enter or select a value.</span></span>
    * <span data-ttu-id="8a6f6-113">US-001 を使用します。</span><span class="sxs-lookup"><span data-stu-id="8a6f6-113">Use US-001.</span></span>  
4. <span data-ttu-id="8a6f6-114">[OK] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="8a6f6-114">Click OK.</span></span>
5. <span data-ttu-id="8a6f6-115">[品目番号] フィールドに、'L0001' を入力します。</span><span class="sxs-lookup"><span data-stu-id="8a6f6-115">In the Item number field, type 'L0001'.</span></span>
6. <span data-ttu-id="8a6f6-116">数量を '30' に設定します。</span><span class="sxs-lookup"><span data-stu-id="8a6f6-116">Set Quantity to '30'.</span></span>
    * <span data-ttu-id="8a6f6-117">イベントかんばんルールをトリガーするためには数量が 24 以上であることが重要です。</span><span class="sxs-lookup"><span data-stu-id="8a6f6-117">It is important that the quantity is higher than 24 in order to trigger the event kanban rule.</span></span>  

## <a name="open-a-pegging-tree"></a><span data-ttu-id="8a6f6-118">ペギング ツリーを開く</span><span class="sxs-lookup"><span data-stu-id="8a6f6-118">Open a pegging tree</span></span> 
1. <span data-ttu-id="8a6f6-119">[製品と供給] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="8a6f6-119">Click Product and supply.</span></span>
2. <span data-ttu-id="8a6f6-120">[ペギング ツリーの表示] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="8a6f6-120">Click View pegging tree.</span></span>
    * <span data-ttu-id="8a6f6-121">ペギング ツリーが販売注文明細行に必要なペギングのすべてのレベルを示すことを確認します。</span><span class="sxs-lookup"><span data-stu-id="8a6f6-121">Notice that the pegging tree shows all levels of the pegging needed for the sales order line.</span></span> <span data-ttu-id="8a6f6-122">この場合、かんばんの 2 つのレベルとすべての必須コンポーネントがあります。</span><span class="sxs-lookup"><span data-stu-id="8a6f6-122">In this case, there are two levels of kanbans and all the required components.</span></span>  

## <a name="plan-the-pegging-tree"></a><span data-ttu-id="8a6f6-123">ペギング ツリーの計画</span><span class="sxs-lookup"><span data-stu-id="8a6f6-123">Plan the pegging tree</span></span>
1. <span data-ttu-id="8a6f6-124">ツリーで、「Sales line 000832\Kanban 000558」を選択します。</span><span class="sxs-lookup"><span data-stu-id="8a6f6-124">In the tree, select 'Sales line 000832\Kanban 000558'.</span></span>
2. <span data-ttu-id="8a6f6-125">[かんばん作業] セクションを展開します。</span><span class="sxs-lookup"><span data-stu-id="8a6f6-125">Expand the Kanban jobs section.</span></span>
    * <span data-ttu-id="8a6f6-126">かんばん作業のジョブ ステータスが [未計画] になっていることを確認します。</span><span class="sxs-lookup"><span data-stu-id="8a6f6-126">Notice that the job status for the kanban job is Not planned.</span></span>  
3. <span data-ttu-id="8a6f6-127">[ペギング ツリー全体の計画] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="8a6f6-127">Click Plan entire pegging tree.</span></span>
    * <span data-ttu-id="8a6f6-128">これがペギング ツリーですべてのかんばん作業を計画し、[ジョブ ステータス] を「未計画」から「計画済」に変更します。</span><span class="sxs-lookup"><span data-stu-id="8a6f6-128">This will plan all kanban jobs in the pegging tree, changing the Job status from Not planned to Planned.</span></span>  
4. <span data-ttu-id="8a6f6-129">ページを更新します。</span><span class="sxs-lookup"><span data-stu-id="8a6f6-129">Refresh the page.</span></span>
    * <span data-ttu-id="8a6f6-130">かんばん作業の状態が「未計画」から「計画済」に変更されていることを確認します。</span><span class="sxs-lookup"><span data-stu-id="8a6f6-130">Notice that the kanban Job status changed from Not planned to Planned.</span></span>  
5. <span data-ttu-id="8a6f6-131">ツリーで、「Sales line 000832\Kanban 000558\Issue for L0001\Kanban 000559」を選択します。</span><span class="sxs-lookup"><span data-stu-id="8a6f6-131">In the tree, select 'Sales line 000832\Kanban 000558\Issue for L0001\Kanban 000559'.</span></span>
    * <span data-ttu-id="8a6f6-132">すべてのペギング ツリーが [計画済] であるため、2 番目のかんばんジョブも計画済になります。</span><span class="sxs-lookup"><span data-stu-id="8a6f6-132">The job for the second kanban is also planned, because the entire pegging tree is planned.</span></span> <span data-ttu-id="8a6f6-133">かんばん作業の状態が [未計画] から [計画済] に変更されていることを確認します。</span><span class="sxs-lookup"><span data-stu-id="8a6f6-133">Notice that the kanban job status is changed from Not planned to Planned.</span></span>  


