---
title: 最小の在庫イベントを使用したかんばんルールの作成
description: この手順では、特定の製品が特定の場所で常に使用できるようにするために、最小在庫のイベントを使用してかんばんルールを作成するのに必要な設定を中心に説明します。
author: ChristianRytt
manager: tfehr
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: KanbanRules, LeanProductionFlowActivityLookup, InventItemIdLookupSimple, EcoResProductInformationDialog, EcoResProductDetailsExtended, ReqItemTable, InventLocationIdLookup
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: crytt
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: b295000e132b8551045520df1af55a37673f131d
ms.sourcegitcommit: 199848e78df5cb7c439b001bdbe1ece963593cdb
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 10/13/2020
ms.locfileid: "4431684"
---
# <a name="create-a-kanban-rule-using-a-minimum-stock-event"></a><span data-ttu-id="619ca-103">最小の在庫イベントを使用したかんばんルールの作成</span><span class="sxs-lookup"><span data-stu-id="619ca-103">Create a kanban rule using a minimum stock event</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="619ca-104">この手順では、特定の製品が特定の場所で常に使用できるようにするために、最小在庫のイベントを使用してかんばんルールを作成するのに必要な設定を中心に説明します。</span><span class="sxs-lookup"><span data-stu-id="619ca-104">This procedure focuses on the setup needed to create a kanban rule using a minimum stock event to ensure that a specific product is always available at a specific location.</span></span> <span data-ttu-id="619ca-105">かんばんルールは、在庫レベルが 200 個を下回ったときに材料をその場所に転送するために作成されます。</span><span class="sxs-lookup"><span data-stu-id="619ca-105">A kanban rule is created to transfer material to the location when the inventory level drops below 200 pieces.</span></span> <span data-ttu-id="619ca-106">ペギング イベント処理を実行することによって、必要なかんばんが作成されます。</span><span class="sxs-lookup"><span data-stu-id="619ca-106">By running the Pegging event processing, the needed kanbans are created.</span></span> <span data-ttu-id="619ca-107">このタスクの作成に使用するデモ データの会社は USMF です。</span><span class="sxs-lookup"><span data-stu-id="619ca-107">The demo data company used to create this task is USMF.</span></span> <span data-ttu-id="619ca-108">このタスクは、リーン環境で新しい製品または変更された製品の生産を準備している、プロセス エンジニアまたはバリュー ストリームのマネージャーを対象としています。</span><span class="sxs-lookup"><span data-stu-id="619ca-108">This task is intended for the process engineer or the value stream manager, as they prepare production of a new or modified product in a lean environment.</span></span>


## <a name="create-a-new-kanban-rule"></a><span data-ttu-id="619ca-109">新しいかんばんルールの作成</span><span class="sxs-lookup"><span data-stu-id="619ca-109">Create a new kanban rule</span></span>
1. <span data-ttu-id="619ca-110">[製品情報管理] > [リーン生産] > [かんばんルール] の順に移動します。</span><span class="sxs-lookup"><span data-stu-id="619ca-110">Go to Product information management > Lean manufacturing > Kanban rules.</span></span>
2. <span data-ttu-id="619ca-111">[新規] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="619ca-111">Click New.</span></span>
3. <span data-ttu-id="619ca-112">[タイプ] フィールドで、「引き取り」を選択します。</span><span class="sxs-lookup"><span data-stu-id="619ca-112">In the Type field, select 'Withdrawal'.</span></span>
    * <span data-ttu-id="619ca-113">このタイプは転送かんばんの作成に使用されます。</span><span class="sxs-lookup"><span data-stu-id="619ca-113">This type is used to create transfer kanbans.</span></span>  
4. <span data-ttu-id="619ca-114">[補充方法] フィールドで、「イベント」を選択します。</span><span class="sxs-lookup"><span data-stu-id="619ca-114">In the Replenishment strategy field, select 'Event'.</span></span>
    * <span data-ttu-id="619ca-115">イベント戦略は、イベントに基づくかんばんの転送を作成するために使用されます。</span><span class="sxs-lookup"><span data-stu-id="619ca-115">The Event strategy is used to create the transfer kanbans based on an event.</span></span> <span data-ttu-id="619ca-116">後の手順で、在庫補充を使用して転送かんばんをトリガーします。</span><span class="sxs-lookup"><span data-stu-id="619ca-116">Later in the procedure, you will trigger transfer kanbans by using stock replenishment.</span></span>  
5. <span data-ttu-id="619ca-117">[最初の計画活動] フィールドで、値を入力または選択します。</span><span class="sxs-lookup"><span data-stu-id="619ca-117">In the First plan activity field, enter or select a value.</span></span>
    * <span data-ttu-id="619ca-118">ReplenishSpeakerComponents を入力または選択します。</span><span class="sxs-lookup"><span data-stu-id="619ca-118">Enter or select ReplenishSpeakerComponents.</span></span> <span data-ttu-id="619ca-119">この転送活動には入庫 (出荷) 倉庫と場所 12 があるので、材料は倉庫 12 のロケーション 12 に移動されます。</span><span class="sxs-lookup"><span data-stu-id="619ca-119">This transfer activity has receipt (output) warehouse and location 12, which means that materials will be moved to location 12 in warehouse 12.</span></span>  
6. <span data-ttu-id="619ca-120">[詳細] セクションを展開します。</span><span class="sxs-lookup"><span data-stu-id="619ca-120">Expand the Details section.</span></span>
7. <span data-ttu-id="619ca-121">[製品] フィールドで、値を入力または選択します。</span><span class="sxs-lookup"><span data-stu-id="619ca-121">In the Product field, enter or select a value.</span></span>
    * <span data-ttu-id="619ca-122">M0007 を選択します。</span><span class="sxs-lookup"><span data-stu-id="619ca-122">Select M0007.</span></span>  
8. <span data-ttu-id="619ca-123">[イベント] セクションを展開します。</span><span class="sxs-lookup"><span data-stu-id="619ca-123">Expand the Events section.</span></span>
9. <span data-ttu-id="619ca-124">[在庫補充イベント] フィールドで、「バッチ」を選択します。</span><span class="sxs-lookup"><span data-stu-id="619ca-124">In the Stock replenishment event field, select 'Batch'.</span></span>
    * <span data-ttu-id="619ca-125">これにより、ペギング イベント処理中に関連する場所へ材料ニーズを満たすかんばんを作成します。</span><span class="sxs-lookup"><span data-stu-id="619ca-125">This creates kanbans to fulfill material needs at the related location during Pegging event processing.</span></span>  

## <a name="set-the-minimum-quantity-for-the-item"></a><span data-ttu-id="619ca-126">品目の最小数量の設定</span><span class="sxs-lookup"><span data-stu-id="619ca-126">Set the minimum quantity for the item</span></span>
1. <span data-ttu-id="619ca-127">クリックして、[製品] フィールドのリンク先を表示します。</span><span class="sxs-lookup"><span data-stu-id="619ca-127">Click to follow the link in the Product field.</span></span>
2. <span data-ttu-id="619ca-128">クリックして、[品目番号] フィールドのリンク先を表示します。</span><span class="sxs-lookup"><span data-stu-id="619ca-128">Click to follow the link in the Item number field.</span></span>
3. <span data-ttu-id="619ca-129">製品画像の情報ボックスを展開します。</span><span class="sxs-lookup"><span data-stu-id="619ca-129">Expand the Product image FactBox.</span></span>
4. <span data-ttu-id="619ca-130">アクション ウィンドウで、[計画] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="619ca-130">On the Action Pane, click Plan.</span></span>
5. <span data-ttu-id="619ca-131">[品目補充] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="619ca-131">Click Item coverage.</span></span>
6. <span data-ttu-id="619ca-132">[新規] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="619ca-132">Click New.</span></span>
7. <span data-ttu-id="619ca-133">一覧で、選択された行をマークします。</span><span class="sxs-lookup"><span data-stu-id="619ca-133">In the list, mark the selected row.</span></span>
8. <span data-ttu-id="619ca-134">[倉庫] フィールドで、値を入力または選択します。</span><span class="sxs-lookup"><span data-stu-id="619ca-134">In the Warehouse field, enter or select a value.</span></span>
    * <span data-ttu-id="619ca-135">[倉庫] を 12 に設定します。</span><span class="sxs-lookup"><span data-stu-id="619ca-135">Set Warehouse to 12.</span></span>  
9. <span data-ttu-id="619ca-136">最小を「200」に設定します。</span><span class="sxs-lookup"><span data-stu-id="619ca-136">Set Minimum to '200'.</span></span>

## <a name="run-the-batch-event-creation-job"></a><span data-ttu-id="619ca-137">バッチ イベント作成ジョブの実行</span><span class="sxs-lookup"><span data-stu-id="619ca-137">Run the batch event creation job</span></span>
1. <span data-ttu-id="619ca-138">[生産管理] > [定期処理のタスク] > [かんばん作業のバッチ処理] > [ペギング イベント処理] の順に移動します。</span><span class="sxs-lookup"><span data-stu-id="619ca-138">Go to Production control > Periodic tasks > Kanban job batch processing > Pegging event processing.</span></span>
2. <span data-ttu-id="619ca-139">[OK] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="619ca-139">Click OK.</span></span>
3. <span data-ttu-id="619ca-140">[製品情報管理] > [リーン生産] > [かんばんルール] の順に移動します。</span><span class="sxs-lookup"><span data-stu-id="619ca-140">Go to Product information management > Lean manufacturing > Kanban rules.</span></span>
4. <span data-ttu-id="619ca-141">一覧で、選択された行のリンクをクリックします。</span><span class="sxs-lookup"><span data-stu-id="619ca-141">In the list, click the link in the selected row.</span></span>
    * <span data-ttu-id="619ca-142">先に作成されたかんばんルールを選択します。</span><span class="sxs-lookup"><span data-stu-id="619ca-142">Select the kanban rule that you created earlier.</span></span>  
5. <span data-ttu-id="619ca-143">[かんばん] セクションを展開します。</span><span class="sxs-lookup"><span data-stu-id="619ca-143">Expand the Kanbans section.</span></span>
    * <span data-ttu-id="619ca-144">必要な材料を倉庫 12 に転送するためにかんばんが作成されたことを確認します。</span><span class="sxs-lookup"><span data-stu-id="619ca-144">Notice that a kanban was created to transfer the needed material to warehouse 12.</span></span>  

