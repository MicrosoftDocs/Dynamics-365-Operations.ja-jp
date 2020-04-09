---
title: 製造のための固定数量かんばんルールの作成
description: この手順は、リーン環境の作業セルで、変換する活動をトリガーする固定の製造かんばんルールを作成するのに必要な設定を対象としています。
author: ChristianRytt
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: KanbanRules, LeanProductionFlowActivityLookup, InventItemIdLookupSimple, UnitOfMeasureLookup, KanbanCreate
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: crytt
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: ff38ba2ed1d513d6b64cf5a64e021cbb08d69b21
ms.sourcegitcommit: 34e543e807ac8790597f522fe3b4f0266cf4ee56
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 03/24/2020
ms.locfileid: "3161757"
---
# <a name="create-a-fixed-quantity-kanban-rule-for-manufacturing"></a><span data-ttu-id="7b5a1-103">製造のための固定数量かんばんルールの作成</span><span class="sxs-lookup"><span data-stu-id="7b5a1-103">Create a fixed quantity kanban rule for manufacturing</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="7b5a1-104">この手順は、リーン環境の作業セルで、変換する活動をトリガーする固定の製造かんばんルールを作成するのに必要な設定を対象としています。</span><span class="sxs-lookup"><span data-stu-id="7b5a1-104">This procedure focuses on the setup needed to create a fixed manufacturing kanban rule for triggering transforming activities, at a work cell, in a lean environment.</span></span> <span data-ttu-id="7b5a1-105">この手順の作成に使用するデモ データの会社は USMF です。</span><span class="sxs-lookup"><span data-stu-id="7b5a1-105">The demo data company used to create this procedure is USMF.</span></span> <span data-ttu-id="7b5a1-106">この手順は、新しい製品または変更された製品の生産を準備している、プロセス エンジニアまたはバリュー ストリームのマネージャーを対象としています。</span><span class="sxs-lookup"><span data-stu-id="7b5a1-106">This procedure is intended for the Process Engineer or the Value Stream Manager, as they prepare production of a new or modified product.</span></span>


## <a name="create-new-kanban-rule"></a><span data-ttu-id="7b5a1-107">新しいかんばんルールの作成</span><span class="sxs-lookup"><span data-stu-id="7b5a1-107">Create new kanban rule</span></span>
1. <span data-ttu-id="7b5a1-108">[かんばんルール] に移動します。</span><span class="sxs-lookup"><span data-stu-id="7b5a1-108">Go to Kanban rules.</span></span>
2. <span data-ttu-id="7b5a1-109">[新規] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="7b5a1-109">Click New.</span></span>
    * <span data-ttu-id="7b5a1-110">既定のタイプが製造、また補充方法が固定になっていることに注目してください。</span><span class="sxs-lookup"><span data-stu-id="7b5a1-110">Notice that the default Type is Manufacturing and Replenishment strategy is Fixed.</span></span> <span data-ttu-id="7b5a1-111">これらのパラメーターを変更する必要はありません。</span><span class="sxs-lookup"><span data-stu-id="7b5a1-111">You do not have to change these parameters.</span></span>  
3. <span data-ttu-id="7b5a1-112">[最初の計画活動] フィールドで、値を入力または選択します。</span><span class="sxs-lookup"><span data-stu-id="7b5a1-112">In the First plan activity field, enter or select a value.</span></span>
    * <span data-ttu-id="7b5a1-113">これはこのかんばんルールに基づいて作成されたかんばんに対して実行される活動です。</span><span class="sxs-lookup"><span data-stu-id="7b5a1-113">This is the activity that will be performed for kanbans created based on this kanban rule.</span></span>  <span data-ttu-id="7b5a1-114">「SpeakerTestAndPackaging」を選択します。</span><span class="sxs-lookup"><span data-stu-id="7b5a1-114">Select 'SpeakerTestAndPackaging'.</span></span>  
4. <span data-ttu-id="7b5a1-115">[詳細] セクションを展開します。</span><span class="sxs-lookup"><span data-stu-id="7b5a1-115">Expand the Details section.</span></span>
5. <span data-ttu-id="7b5a1-116">[製品] フィールドで、値を入力または選択します。</span><span class="sxs-lookup"><span data-stu-id="7b5a1-116">In the Product field, enter or select a value.</span></span>
    * <span data-ttu-id="7b5a1-117">[L0050] を選択します。</span><span class="sxs-lookup"><span data-stu-id="7b5a1-117">Select L0050.</span></span>  
6. <span data-ttu-id="7b5a1-118">[計量単位] フィールドで、値を入力または選択します。</span><span class="sxs-lookup"><span data-stu-id="7b5a1-118">In the Unit of measure field, enter or select a value.</span></span>
    * <span data-ttu-id="7b5a1-119">分を選択します。</span><span class="sxs-lookup"><span data-stu-id="7b5a1-119">Select minutes.</span></span>  
7. <span data-ttu-id="7b5a1-120">[リード タイム] フィールドで、数値を入力します。</span><span class="sxs-lookup"><span data-stu-id="7b5a1-120">In the Lead time field, enter a number.</span></span>
    * <span data-ttu-id="7b5a1-121">5 を入力します。</span><span class="sxs-lookup"><span data-stu-id="7b5a1-121">Enter 5.</span></span>  

## <a name="set-quantities"></a><span data-ttu-id="7b5a1-122">数量の設定</span><span class="sxs-lookup"><span data-stu-id="7b5a1-122">Set quantities</span></span>
1. <span data-ttu-id="7b5a1-123">[数量] セクションを展開します。</span><span class="sxs-lookup"><span data-stu-id="7b5a1-123">Expand the Quantities section.</span></span>
2. <span data-ttu-id="7b5a1-124">[既定の数量] を「10」に設定します。</span><span class="sxs-lookup"><span data-stu-id="7b5a1-124">Set Default quantity to '10'.</span></span>
    * <span data-ttu-id="7b5a1-125">これは、かんばんごとに転送される数量です。</span><span class="sxs-lookup"><span data-stu-id="7b5a1-125">This is the quantity that will be transferred for each kanban.</span></span>  
3. <span data-ttu-id="7b5a1-126">[製品数量の差異] チェック ボックスを選択します。</span><span class="sxs-lookup"><span data-stu-id="7b5a1-126">Select the Product quantity variance check box.</span></span>
    * <span data-ttu-id="7b5a1-127">これを使用すると、選択されたかんばんが既定の数量との差異で完了できます。</span><span class="sxs-lookup"><span data-stu-id="7b5a1-127">With this, selected kanbans can be completed with a variance from the default quantity.</span></span>  <span data-ttu-id="7b5a1-128">かんばんが 8 から 12 の数量で完了するようにするには、両方の差異を 2 に設定します。</span><span class="sxs-lookup"><span data-stu-id="7b5a1-128">To allow kanbans to be completed with a quantity from 8 to 12, set both variances to 2.</span></span>  
4. <span data-ttu-id="7b5a1-129">[差異の上限] を「2」に設定します。</span><span class="sxs-lookup"><span data-stu-id="7b5a1-129">Set Variance below to '2'.</span></span>
    * <span data-ttu-id="7b5a1-130">これにより、数量が減って 10 - 2 = 8 完了することになります。</span><span class="sxs-lookup"><span data-stu-id="7b5a1-130">This will allow completing down to 10 - 2 = 8</span></span>  
5. <span data-ttu-id="7b5a1-131">[差異の下限] を「2」に設定します。</span><span class="sxs-lookup"><span data-stu-id="7b5a1-131">Set Variance above to '2'.</span></span>
    * <span data-ttu-id="7b5a1-132">これにより、数量が増えて 10 + 2 = 12 完了することになります。</span><span class="sxs-lookup"><span data-stu-id="7b5a1-132">This will allow completing up to 10 + 2 = 12</span></span>  
6. <span data-ttu-id="7b5a1-133">[固定かんばん数量] フィールドで、数値を入力します。</span><span class="sxs-lookup"><span data-stu-id="7b5a1-133">In the Fixed kanban quantity field, enter a number.</span></span>
    * <span data-ttu-id="7b5a1-134">これは有効にするかんばんの量です。</span><span class="sxs-lookup"><span data-stu-id="7b5a1-134">This is the amount of kanbans that should be active.</span></span> <span data-ttu-id="7b5a1-135">この場合、5 つのかんばんが 、それぞれ 10 処理します。</span><span class="sxs-lookup"><span data-stu-id="7b5a1-135">In this case, 5 kanbans processing 10 each.</span></span>  
7. <span data-ttu-id="7b5a1-136">[下限値に対する警告] フィールドで、「2」を入力します。</span><span class="sxs-lookup"><span data-stu-id="7b5a1-136">In the Alert boundary minimum field, enter '2'.</span></span>
    * <span data-ttu-id="7b5a1-137">出荷先にあるべきすべてのかんばんの最小数量を追跡するために使用されます。</span><span class="sxs-lookup"><span data-stu-id="7b5a1-137">Used to keep track of the minimum amount of full kanbans that should be at the destination.</span></span> <span data-ttu-id="7b5a1-138">たとえば、これはかんばんの数量の概要に使用されます。</span><span class="sxs-lookup"><span data-stu-id="7b5a1-138">For example, this is used on the kanban quantity overview.</span></span>  
8. <span data-ttu-id="7b5a1-139">[上限値に対する警告] フィールドで、「4」を入力します。</span><span class="sxs-lookup"><span data-stu-id="7b5a1-139">In the Alert boundary maximum field, enter '4'.</span></span>
    * <span data-ttu-id="7b5a1-140">出荷先にあるべきすべてのかんばんの最大数量を追跡するために使用されます。</span><span class="sxs-lookup"><span data-stu-id="7b5a1-140">Used to keep track of the maximum amount of full kanbans that should be at the destination.</span></span> <span data-ttu-id="7b5a1-141">たとえば、これはかんばんの数量の概要に使用されます。</span><span class="sxs-lookup"><span data-stu-id="7b5a1-141">For example, this is used on the kanban quantity overview.</span></span>  
9. <span data-ttu-id="7b5a1-142">[自動計画数量] フィールドで、「1」を入力します。</span><span class="sxs-lookup"><span data-stu-id="7b5a1-142">In the Automatic planning quantity field, enter '1'.</span></span>
    * <span data-ttu-id="7b5a1-143">これを 1 に設定すると、すべてのかんばんが自動的に計画されることになります。</span><span class="sxs-lookup"><span data-stu-id="7b5a1-143">Setting this to 1 means that every kanban will be automatically planned.</span></span>   <span data-ttu-id="7b5a1-144">3 を入力してしまうと、3 つの空のかんばんに計画の準備が整うまで、そのかんばんは計画されないことになります。</span><span class="sxs-lookup"><span data-stu-id="7b5a1-144">If we entered 3, the kanbans would not be planned until 3 empty kanbans are ready for planning.</span></span> <span data-ttu-id="7b5a1-145">これは、作業をグループ化し、余計な設定を回避するのに役立ちます。</span><span class="sxs-lookup"><span data-stu-id="7b5a1-145">This is useful for grouping work and avoiding too much setup.</span></span>  

## <a name="create-kanbans"></a><span data-ttu-id="7b5a1-146">かんばんの作成</span><span class="sxs-lookup"><span data-stu-id="7b5a1-146">Create Kanbans</span></span>
1. <span data-ttu-id="7b5a1-147">[かんばん] セクションを展開します。</span><span class="sxs-lookup"><span data-stu-id="7b5a1-147">Expand the Kanbans section.</span></span>
2. <span data-ttu-id="7b5a1-148">[保存] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="7b5a1-148">Click Save.</span></span>
    * <span data-ttu-id="7b5a1-149">かんばんルールは、かんばんを作成する前に保存する必要があります。</span><span class="sxs-lookup"><span data-stu-id="7b5a1-149">The kanban rule needs to be saved before kanbans can be created.</span></span>  
3. <span data-ttu-id="7b5a1-150">[追加] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="7b5a1-150">Click Add.</span></span>
    * <span data-ttu-id="7b5a1-151">この提案されている [新しいかんばんの数] が 5 であるため、有効なかんばんが存在しないことに注意してください。。</span><span class="sxs-lookup"><span data-stu-id="7b5a1-151">Note that there are no active kanbans, due to this the suggested 'Number of new kanbans' are 5.</span></span> <span data-ttu-id="7b5a1-152">これは、[固定かんばん数量] と等しくなります。</span><span class="sxs-lookup"><span data-stu-id="7b5a1-152">This is equal to the 'Fixed kanban quantity'.</span></span>  
4. <span data-ttu-id="7b5a1-153">[作成] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="7b5a1-153">Click Create.</span></span>
    * <span data-ttu-id="7b5a1-154">これは、5 つのかんばんを作成します。</span><span class="sxs-lookup"><span data-stu-id="7b5a1-154">This will create 5 kanbans.</span></span>  
    * <span data-ttu-id="7b5a1-155">この製造かんばんルールのために、10 それぞれに対して 5 のかんばんが作成されたことに注目してください。</span><span class="sxs-lookup"><span data-stu-id="7b5a1-155">Note that 5 kanbans, for 10 each, was created for this manufacturing kanban rule.</span></span> <span data-ttu-id="7b5a1-156">これは、この手順の最後のステップです。</span><span class="sxs-lookup"><span data-stu-id="7b5a1-156">This is the last step in this procedure.</span></span>  

