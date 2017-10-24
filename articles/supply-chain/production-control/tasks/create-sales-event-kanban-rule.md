--- 
title: "販売イベントかんばんルールの作成"
description: "この手順は、販売注文の作成時に発生するかんばんルールを作成するのに必要な設定を対象としています。"
author: ChristianRytt
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
ms.author: crytt
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: f827b4787506cfdec8b9a91c4a68f3293190158a
ms.openlocfilehash: f1f66157b2e74ad1b490e10112cbc121ac9826fb
ms.contentlocale: ja-jp
ms.lasthandoff: 09/29/2017

---
# <a name="create-a-sales-event-kanban-rule"></a><span data-ttu-id="95972-103">販売イベントかんばんルールの作成</span><span class="sxs-lookup"><span data-stu-id="95972-103">Create a sales event kanban rule</span></span>

[!include[task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="95972-104">この手順は、販売注文の作成時に発生するかんばんルールを作成するのに必要な設定を対象としています。</span><span class="sxs-lookup"><span data-stu-id="95972-104">This procedure focuses on the setup needed to create a kanban rule that is triggered during sales order creation.</span></span> <span data-ttu-id="95972-105">かんばんルールのイベントは、販売注文明細行に基づいて必要量を補充します。</span><span class="sxs-lookup"><span data-stu-id="95972-105">The event kanban rule replenishes requirements that originate from sales order lines.</span></span> <span data-ttu-id="95972-106">この手順の作成に使用するデモ データの会社は USMF です。</span><span class="sxs-lookup"><span data-stu-id="95972-106">The demo data company used to create this procedure is USMF.</span></span> <span data-ttu-id="95972-107">これは、新しい製品または変更された製品の生産を準備している、プロセス エンジニアまたはバリュー ストリームのマネージャーを対象としています。</span><span class="sxs-lookup"><span data-stu-id="95972-107">It is intended for the process engineer or the value stream manager as they prepare production of a new or modified product.</span></span>




## <a name="create-a-new-kanban-rule"></a><span data-ttu-id="95972-108">新しいかんばんルールの作成</span><span class="sxs-lookup"><span data-stu-id="95972-108">Create a new kanban rule</span></span>
1. <span data-ttu-id="95972-109">[かんばんルール] に移動します。</span><span class="sxs-lookup"><span data-stu-id="95972-109">Go to Kanban rules.</span></span>
2. <span data-ttu-id="95972-110">[新規] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="95972-110">Click New.</span></span>
3. <span data-ttu-id="95972-111">[補充方法] フィールドで、「イベント」を選択します。</span><span class="sxs-lookup"><span data-stu-id="95972-111">In the Replenishment strategy field, select 'Event'.</span></span>
    * <span data-ttu-id="95972-112">[イベント] を選択すると、かんばんルールは、たとえば販売注文明細行の作成といったイベントによってトリガーされることになります。</span><span class="sxs-lookup"><span data-stu-id="95972-112">Selecting Event means that the kanban rule is triggered by an event, for example, creation of a sales order line.</span></span>   <span data-ttu-id="95972-113">これは、各かんばんが特定の需要を満たす必要がある領域に適用されます。</span><span class="sxs-lookup"><span data-stu-id="95972-113">This is applied to areas where each kanban should cover a specific demand.</span></span>  
4. <span data-ttu-id="95972-114">[最初の計画活動] フィールドで、値を入力または選択します。</span><span class="sxs-lookup"><span data-stu-id="95972-114">In the First plan activity field, enter or select a value.</span></span>
    * <span data-ttu-id="95972-115">[最終アセンブリ] を選択します。</span><span class="sxs-lookup"><span data-stu-id="95972-115">Select Final assembly.</span></span>  
5. <span data-ttu-id="95972-116">[詳細] セクションを展開します。</span><span class="sxs-lookup"><span data-stu-id="95972-116">Expand the Details section.</span></span>
6. <span data-ttu-id="95972-117">[製品] フィールドで、値を入力または選択します。</span><span class="sxs-lookup"><span data-stu-id="95972-117">In the Product field, enter or select a value.</span></span>
    * <span data-ttu-id="95972-118">[L0050] を選択します。</span><span class="sxs-lookup"><span data-stu-id="95972-118">Select L0050.</span></span>  

## <a name="define-an-event"></a><span data-ttu-id="95972-119">イベントの定義</span><span class="sxs-lookup"><span data-stu-id="95972-119">Define an event</span></span>
1. <span data-ttu-id="95972-120">[イベント] セクションを展開します。</span><span class="sxs-lookup"><span data-stu-id="95972-120">Expand the Events section.</span></span>
2. <span data-ttu-id="95972-121">[販売イベント] フィールドで、「自動」を選択します。</span><span class="sxs-lookup"><span data-stu-id="95972-121">In the Sales event field, select 'Automatic'.</span></span>
    * <span data-ttu-id="95972-122">販売イベントの [自動] を選択すると、このかんばんルールは、販売明細行が製品および受入場所に一致すると自動的に発生します。</span><span class="sxs-lookup"><span data-stu-id="95972-122">By selecting the sales event Automatic, this kanban rule will be triggered automatically when a sales line matches the product and receipt location.</span></span> <span data-ttu-id="95972-123">この手順では、倉庫 13 の製品 L0050 です。</span><span class="sxs-lookup"><span data-stu-id="95972-123">In this procedure, it is product L0050 on warehouse 13.</span></span>  
3. <span data-ttu-id="95972-124">[最小イベント数量] を「50」に設定します。</span><span class="sxs-lookup"><span data-stu-id="95972-124">Set Minimum event quantity to '50'.</span></span>
    * <span data-ttu-id="95972-125">最小イベント数量が 50 の場合、かんばんルールは、イベントが 50 またはそれ以上の数量の場合にだけ発生します。</span><span class="sxs-lookup"><span data-stu-id="95972-125">With a minimum event quantity of 50, the kanban rule will only be triggered by events with a quantity of 50 or more.</span></span>  
4. <span data-ttu-id="95972-126">[生産フロー] セクションを展開します。</span><span class="sxs-lookup"><span data-stu-id="95972-126">Expand the Production flow section.</span></span>
    * <span data-ttu-id="95972-127">受入場所が倉庫 13 であることに注目してください。</span><span class="sxs-lookup"><span data-stu-id="95972-127">Notice that the Receipt location is warehouse 13.</span></span> <span data-ttu-id="95972-128">これは、このかんばんルールがこの場所に対して発生されることを意味します。</span><span class="sxs-lookup"><span data-stu-id="95972-128">This means that this kanban rule will be triggered for this location.</span></span>  
    * <span data-ttu-id="95972-129">この例では、製品 L0050 の販売明細行、数量 50 以上、倉庫 13、によりこのかんばんルールが発生します。</span><span class="sxs-lookup"><span data-stu-id="95972-129">In this example, a sales line for product L0050, with a quantity of 50 or more, on warehouse 13, will trigger this kanban rule.</span></span>  

## <a name="create-sales-line-to-trigger-event-kanban-rule"></a><span data-ttu-id="95972-130">イベントかんばんルールをトリガーする販売明細行の作成</span><span class="sxs-lookup"><span data-stu-id="95972-130">Create sales line to trigger event kanban rule</span></span>
1. <span data-ttu-id="95972-131">[すべての販売注文] に移動します。</span><span class="sxs-lookup"><span data-stu-id="95972-131">Go to All sales orders.</span></span>
    * <span data-ttu-id="95972-132">かんばんルールが保存されたときに警告が表示されます。これは販売注文作成中にリアルタイムでかんばんが作成されることを意味します。</span><span class="sxs-lookup"><span data-stu-id="95972-132">A warning is shown when the kanban rule is saved, which means that kanbans will be created in real-time during sales order creation.</span></span>  
2. <span data-ttu-id="95972-133">[新規] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="95972-133">Click New.</span></span>
3. <span data-ttu-id="95972-134">[顧客口座] フィールドで値を入力または選択します。</span><span class="sxs-lookup"><span data-stu-id="95972-134">In the Customer account field, enter or select a value.</span></span>
    * <span data-ttu-id="95972-135">たとえば、[US-003] を選択します。</span><span class="sxs-lookup"><span data-stu-id="95972-135">For example, select US-003.</span></span>  
4. <span data-ttu-id="95972-136">[OK] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="95972-136">Click OK.</span></span>
5. <span data-ttu-id="95972-137">[品目番号] フィールドに、'L0050' を入力します。</span><span class="sxs-lookup"><span data-stu-id="95972-137">In the Item number field, type 'L0050'.</span></span>
6. <span data-ttu-id="95972-138">[サイト] フィールドで、「1」と入力します。</span><span class="sxs-lookup"><span data-stu-id="95972-138">In the Site field, type '1'.</span></span>
    * <span data-ttu-id="95972-139">[倉庫 13] が [サイト 1] にあるために、[サイト 1] を選択します。</span><span class="sxs-lookup"><span data-stu-id="95972-139">Select Site 1 because Warehouse 13 is on Site 1.</span></span>  
7. <span data-ttu-id="95972-140">[倉庫] フィールドで、値を入力または選択します。</span><span class="sxs-lookup"><span data-stu-id="95972-140">In the Warehouse field, enter or select a value.</span></span>
    * <span data-ttu-id="95972-141">[倉庫] を 13 に設定します。</span><span class="sxs-lookup"><span data-stu-id="95972-141">Set Warehouse to 13.</span></span>  
8. <span data-ttu-id="95972-142">数量を '75' に設定します。</span><span class="sxs-lookup"><span data-stu-id="95972-142">Set Quantity to '75'.</span></span>
    * <span data-ttu-id="95972-143">作成されたかんばんルールを発生させるために、50 以上の数量を入力します。</span><span class="sxs-lookup"><span data-stu-id="95972-143">Enter a quantity of 50 or greater, to trigger the created kanban rule.</span></span>  

## <a name="verify-that-kanban-is-created"></a><span data-ttu-id="95972-144">かんばんが作成されていることの確認</span><span class="sxs-lookup"><span data-stu-id="95972-144">Verify that kanban is created</span></span>
1. <span data-ttu-id="95972-145">[製品と供給] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="95972-145">Click Product and supply.</span></span>
2. <span data-ttu-id="95972-146">[ペギング ツリーの表示] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="95972-146">Click View pegging tree.</span></span>
    * <span data-ttu-id="95972-147">販売明細行と同じ数量のかんばんが作成されることを確認します。</span><span class="sxs-lookup"><span data-stu-id="95972-147">Notice that a kanban with the same quantity as the sales line is created.</span></span> <span data-ttu-id="95972-148">製品 L0050 を生産するのに必要な原材料の問題も確認できます。</span><span class="sxs-lookup"><span data-stu-id="95972-148">You can also see the material issues needed to produce L0050.</span></span> <span data-ttu-id="95972-149">これは、この手順の最後のステップです。</span><span class="sxs-lookup"><span data-stu-id="95972-149">This is the last step in this procedure.</span></span>  


