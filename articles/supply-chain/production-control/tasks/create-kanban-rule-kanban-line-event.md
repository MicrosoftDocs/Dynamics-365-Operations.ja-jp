---
title: かんばん明細行イベントを使用したかんばんルールの作成
description: この手順では、プロセス活動からプルをトリガするかんばん明細行イベント設定を使用して、かんばんルールを作成します。
author: ChristianRytt
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: KanbanRules, LeanProductionFlowActivityLookup, SalesTableListPage, SalesCreateOrder, SalesTable
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: crytt
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: fe92336c3f80909e5b0865b461e45d55bf08c4b4
ms.sourcegitcommit: 0e8db169c3f90bd750826af76709ef5d621fd377
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/01/2021
ms.locfileid: "5829141"
---
# <a name="create-a-kanban-rule-using-a-kanban-line-event"></a><span data-ttu-id="f2801-103">かんばん明細行イベントを使用したかんばんルールの作成</span><span class="sxs-lookup"><span data-stu-id="f2801-103">Create a kanban rule using a kanban line event</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="f2801-104">この手順では、プロセス活動からプルをトリガするかんばん明細行イベント設定を使用して、かんばんルールを作成します。</span><span class="sxs-lookup"><span data-stu-id="f2801-104">This procedure creates a kanban rule by using the kanban line event setting to trigger pull from a process activity.</span></span> <span data-ttu-id="f2801-105">かんばんルールは、それぞれの数量が 25 かまたはそれより多くの数量のかんばんのプロセス活動によって発生します。</span><span class="sxs-lookup"><span data-stu-id="f2801-105">The kanban rule is triggered by a kanban process activity, with a quantity equal to or greater than 25 each.</span></span> <span data-ttu-id="f2801-106">このタスクの作成に使用するデモ データの会社は USMF です。</span><span class="sxs-lookup"><span data-stu-id="f2801-106">The demo data company used to create this task is USMF.</span></span> <span data-ttu-id="f2801-107">このタスクは、リーン環境で新しい製品または変更された製品の生産を準備している、プロセス エンジニアまたはバリュー ストリームのマネージャーを対象としています。</span><span class="sxs-lookup"><span data-stu-id="f2801-107">This task is intended for the process engineer or the value stream manager, as they prepare production of a new or modified product in a lean environment.</span></span>


## <a name="create-a-kanban-rule"></a><span data-ttu-id="f2801-108">かんばんルールの作成</span><span class="sxs-lookup"><span data-stu-id="f2801-108">Create a kanban rule</span></span>
1. <span data-ttu-id="f2801-109">[製品情報管理] > [リーン生産] > [かんばんルール] の順に移動します。</span><span class="sxs-lookup"><span data-stu-id="f2801-109">Go to Product information management > Lean manufacturing > Kanban rules.</span></span>
2. <span data-ttu-id="f2801-110">[新規] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="f2801-110">Click New.</span></span>
3. <span data-ttu-id="f2801-111">[補充方法] フィールドで、「イベント」を選択します。</span><span class="sxs-lookup"><span data-stu-id="f2801-111">In the Replenishment strategy field, select 'Event'.</span></span>
    * <span data-ttu-id="f2801-112">これにより、かんばんは需要から直接生成されます。</span><span class="sxs-lookup"><span data-stu-id="f2801-112">This generates kanbans directly from demand.</span></span> <span data-ttu-id="f2801-113">受注生産シナリオを定義するルールを設定するのに使用されます。</span><span class="sxs-lookup"><span data-stu-id="f2801-113">It is used to set up rules that define a make-to-order scenario.</span></span>  
4. <span data-ttu-id="f2801-114">[最初の計画活動] フィールドで、値を入力または選択します。</span><span class="sxs-lookup"><span data-stu-id="f2801-114">In the First plan activity field, enter or select a value.</span></span>
    * <span data-ttu-id="f2801-115">SpeakerAssemblyAndPolish を入力または選択します。</span><span class="sxs-lookup"><span data-stu-id="f2801-115">Enter or select SpeakerAssemblyAndPolish.</span></span> <span data-ttu-id="f2801-116">製造かんばんルールの最初の活動は、生産フローのプロセス活動です。</span><span class="sxs-lookup"><span data-stu-id="f2801-116">The first activity of a manufacturing kanban rule is a process activity in the production flow.</span></span> <span data-ttu-id="f2801-117">活動を選択すると、その活動の有効期間がかんばんルールの有効期間にコピーされます。</span><span class="sxs-lookup"><span data-stu-id="f2801-117">When you select the activity, the validity dates of the activity are copied to the validity dates of the kanban rule.</span></span>  
5. <span data-ttu-id="f2801-118">[詳細] セクションを展開します。</span><span class="sxs-lookup"><span data-stu-id="f2801-118">Expand the Details section.</span></span>
6. <span data-ttu-id="f2801-119">[製品] フィールドに「L0001」を入力します。</span><span class="sxs-lookup"><span data-stu-id="f2801-119">In the Product field, type 'L0001'.</span></span>
7. <span data-ttu-id="f2801-120">[イベント] セクションを展開します。</span><span class="sxs-lookup"><span data-stu-id="f2801-120">Expand the Events section.</span></span>
8. <span data-ttu-id="f2801-121">[かんばん明細行イベント] フィールドで、「自動」を選択します。</span><span class="sxs-lookup"><span data-stu-id="f2801-121">In the Kanban line event field, select 'Automatic'.</span></span>
    * <span data-ttu-id="f2801-122">これにより、必要に応じたイベントのかんばんが生成されます。</span><span class="sxs-lookup"><span data-stu-id="f2801-122">This generates event kanbans on demand.</span></span>  <span data-ttu-id="f2801-123">ダウンストリームのプロセス活動に必要な材料を補充するかんばんルールをコンフィギュレーションするには、このフィールドが使用されます。</span><span class="sxs-lookup"><span data-stu-id="f2801-123">The field is used to configure kanban rules that replenish material that is required for a downstream process activity.</span></span> <span data-ttu-id="f2801-124">「自動」を選択すると、イベントのかんばんが需要と共に作成されます。</span><span class="sxs-lookup"><span data-stu-id="f2801-124">When you select Automatic, the event kanbans are created with the demand.</span></span> <span data-ttu-id="f2801-125">この設定は、同じ日に生産を実行する予定がある場合にお勧めします。</span><span class="sxs-lookup"><span data-stu-id="f2801-125">This setting is recommended if you expect to execute production on the same day.</span></span>  
9. <span data-ttu-id="f2801-126">[最小イベント数量] を「25」に設定します。</span><span class="sxs-lookup"><span data-stu-id="f2801-126">Set Minimum event quantity to '25'.</span></span>
    * <span data-ttu-id="f2801-127">需要数量がこのフィールド以上の場合、イベントのかんばんが生成されます。</span><span class="sxs-lookup"><span data-stu-id="f2801-127">Event kanbans are generated when the demand quantity is equal to or more than this field.</span></span> <span data-ttu-id="f2801-128">ある機械ではこのフィールドより少ない注文数量を生産し、別の機械ではこのフィールドより多くの注文数量を生産する場合に便利です。</span><span class="sxs-lookup"><span data-stu-id="f2801-128">This is useful if you want to produce an order quantity less than this field on one machine and more than this field on another machine.</span></span>  
10. <span data-ttu-id="f2801-129">[保存] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="f2801-129">Click Save.</span></span>

## <a name="create-sales-order-and-trigger-kanban-chain"></a><span data-ttu-id="f2801-130">販売注文を作成し、かんばんチェーンをトリガーします。</span><span class="sxs-lookup"><span data-stu-id="f2801-130">Create sales order and trigger kanban chain</span></span>
1. <span data-ttu-id="f2801-131">[販売とマーケティング] > [販売注文] > [すべての販売注文] の順に移動します。</span><span class="sxs-lookup"><span data-stu-id="f2801-131">Go to Sales and marketing > Sales orders > All sales orders.</span></span>
2. <span data-ttu-id="f2801-132">[新規] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="f2801-132">Click New.</span></span>
3. <span data-ttu-id="f2801-133">[顧客口座] フィールドで値を入力または選択します。</span><span class="sxs-lookup"><span data-stu-id="f2801-133">In the Customer account field, enter or select a value.</span></span>
    * <span data-ttu-id="f2801-134">「顧客口座 US-003、Forest Wholesales」を選択します。</span><span class="sxs-lookup"><span data-stu-id="f2801-134">Select Customer account US-003, Forest Wholesales.</span></span>  
4. <span data-ttu-id="f2801-135">[OK] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="f2801-135">Click OK.</span></span>
5. <span data-ttu-id="f2801-136">[品目番号] フィールドに、'L0001' を入力します。</span><span class="sxs-lookup"><span data-stu-id="f2801-136">In the Item number field, type 'L0001'.</span></span>
    * <span data-ttu-id="f2801-137">L0001 はかんばんルールを作成した品目です。</span><span class="sxs-lookup"><span data-stu-id="f2801-137">L0001 is the item for which you created the kanban rule.</span></span>  
6. <span data-ttu-id="f2801-138">数量を '27' に設定します。</span><span class="sxs-lookup"><span data-stu-id="f2801-138">Set Quantity to '27'.</span></span>
    * <span data-ttu-id="f2801-139">27 はかんばんルールにおける最小数量 25 より多いため、これによりイベントのかんばんが発生します。</span><span class="sxs-lookup"><span data-stu-id="f2801-139">Because 27 is higher than the minimum quantity of 25 on the kanban rule, this will trigger an event kanban.</span></span>  
7. <span data-ttu-id="f2801-140">[サイト] フィールドで、「1」と入力します。</span><span class="sxs-lookup"><span data-stu-id="f2801-140">In the Site field, type '1'.</span></span>
8. <span data-ttu-id="f2801-141">[倉庫] フィールドで、値を入力または選択します。</span><span class="sxs-lookup"><span data-stu-id="f2801-141">In the Warehouse field, enter or select a value.</span></span>
    * <span data-ttu-id="f2801-142">倉庫 13 を選択します。</span><span class="sxs-lookup"><span data-stu-id="f2801-142">Select warehouse 13.</span></span>  
9. <span data-ttu-id="f2801-143">[保存] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="f2801-143">Click Save.</span></span>

## <a name="view-the-kanban-generated-by-the-kanban-rule"></a><span data-ttu-id="f2801-144">かんばんルールによって生成されたかんばんの表示</span><span class="sxs-lookup"><span data-stu-id="f2801-144">View the kanban generated by the kanban rule</span></span>
1. <span data-ttu-id="f2801-145">[製品情報管理] > [リーン生産] > [かんばんルール] の順に移動します。</span><span class="sxs-lookup"><span data-stu-id="f2801-145">Go to Product information management > Lean manufacturing > Kanban rules.</span></span>
2. <span data-ttu-id="f2801-146">一覧で、目的のレコードを見つけ、選択します。</span><span class="sxs-lookup"><span data-stu-id="f2801-146">In the list, find and select the desired record.</span></span>
3. <span data-ttu-id="f2801-147">[かんばん] セクションを展開します。</span><span class="sxs-lookup"><span data-stu-id="f2801-147">Expand the Kanbans section.</span></span>
    * <span data-ttu-id="f2801-148">作成済みのかんばんルールに基づいて活動を処理するために 27 のかんばんが作成されたことを確認します。</span><span class="sxs-lookup"><span data-stu-id="f2801-148">Notice that a kanban for 27 was created to process the  activity based on the created kanban rule.</span></span>  
    * <span data-ttu-id="f2801-149">これは最後のステップです。</span><span class="sxs-lookup"><span data-stu-id="f2801-149">This is the last step.</span></span>  



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]