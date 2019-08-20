---
title: かんばん数量計算ポリシーのかんばんルールへの追加
description: この手順では、かんばん数量の計算ポリシーを作成し、それをかんばんルールへ追加し、かんばんのサイズおよび数量を最適化することに焦点をあてます。
author: ChristianRytt
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: KanbanQuantityPolicy, KanbanRules
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: crytt
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 401b01a6128babd6ed345342a65705a0262540e8
ms.sourcegitcommit: 8b4b6a9226d4e5f66498ab2a5b4160e26dd112af
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 08/01/2019
ms.locfileid: "1837953"
---
# <a name="add-a-kanban-quantity-calculation-policy-to-a-kanban-rule"></a><span data-ttu-id="968aa-103">かんばん数量計算ポリシーのかんばんルールへの追加</span><span class="sxs-lookup"><span data-stu-id="968aa-103">Add a kanban quantity calculation policy to a kanban rule</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="968aa-104">この手順では、かんばん数量の計算ポリシーを作成し、それをかんばんルールへ追加し、かんばんのサイズおよび数量を最適化することに焦点をあてます。</span><span class="sxs-lookup"><span data-stu-id="968aa-104">This procedure focuses on creating a kanban quantity calculation policy and adding it to a kanban rule to optimize the kanban size and quantities.</span></span> <span data-ttu-id="968aa-105">この手順の作成に使用するデモ データの会社は USMF です。</span><span class="sxs-lookup"><span data-stu-id="968aa-105">The demo data company used to create this procedure is USMF.</span></span> <span data-ttu-id="968aa-106">この手順は、バリュー ストリーム マネージャーを対象としています。</span><span class="sxs-lookup"><span data-stu-id="968aa-106">This procedure is intended for the value stream manager.</span></span> <span data-ttu-id="968aa-107">この手順は、かんばん数量修正候補の計算という手順を作成するための前提条件です。</span><span class="sxs-lookup"><span data-stu-id="968aa-107">This procedure is a prerequisite for creating the procedure Calculate kanban quantity suggestions.</span></span> 


## <a name="create-a-kanban-quantity-calculation-policy"></a><span data-ttu-id="968aa-108">かんばん数量計算ポリシーの作成</span><span class="sxs-lookup"><span data-stu-id="968aa-108">Create a kanban quantity calculation policy</span></span>
1. <span data-ttu-id="968aa-109">[生産管理] > [定期処理タスク] > [かんばん数量の計算] > [かんばん数量の計算ポリシー] の順に移動します。</span><span class="sxs-lookup"><span data-stu-id="968aa-109">Go to Production control > Periodic tasks > Kanban quantity calculation > Kanban quantity calculation policies.</span></span>
2. <span data-ttu-id="968aa-110">[新規] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="968aa-110">Click New.</span></span>
3. <span data-ttu-id="968aa-111">[名前] フィールドに値を入力します。</span><span class="sxs-lookup"><span data-stu-id="968aa-111">In the Name field, type a value.</span></span>
    * <span data-ttu-id="968aa-112">たとえば、「Speaker2016」と入力します。</span><span class="sxs-lookup"><span data-stu-id="968aa-112">For example, type Speaker2016.</span></span>  
4. <span data-ttu-id="968aa-113">[マスター プラン] フィールドで、ドロップ ダウン ボタンをクリックし、ルックアップを開きます。</span><span class="sxs-lookup"><span data-stu-id="968aa-113">In the Master plan field, click the drop-down button to open the lookup.</span></span>
5. <span data-ttu-id="968aa-114">一覧で、目的のレコードを見つけ、選択します。</span><span class="sxs-lookup"><span data-stu-id="968aa-114">In the list, find and select the desired record.</span></span>
    * <span data-ttu-id="968aa-115">StaticPlan を選択して、需要を計算します。</span><span class="sxs-lookup"><span data-stu-id="968aa-115">Select StaticPlan to calculate demand.</span></span>  
6. <span data-ttu-id="968aa-116">一覧で、選択された行のリンクをクリックします。</span><span class="sxs-lookup"><span data-stu-id="968aa-116">In the list, click the link in the selected row.</span></span>
7. <span data-ttu-id="968aa-117">[保存] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="968aa-117">Click Save.</span></span>
8. <span data-ttu-id="968aa-118">[最小かんばん数量] フィールドに、「1」を入力します。</span><span class="sxs-lookup"><span data-stu-id="968aa-118">In the Minimum kanban quantity field, enter '1'.</span></span>
    * <span data-ttu-id="968aa-119">これはかんばん数量計算に含まれる追加のかんばんの数です。</span><span class="sxs-lookup"><span data-stu-id="968aa-119">This is the additional number of kanbans that is included in the kanban quantity calculation.</span></span>  
9. <span data-ttu-id="968aa-120">安全係数に「1」を設定します。</span><span class="sxs-lookup"><span data-stu-id="968aa-120">Set Safety factor to '1'.</span></span>
    * <span data-ttu-id="968aa-121">これは安全在庫の追加数量を計算するのに使用する係数です。</span><span class="sxs-lookup"><span data-stu-id="968aa-121">This is the factor that is used to calculate additional quantity of safety stock.</span></span>  
10. <span data-ttu-id="968aa-122">[進んだ日数] フィールドに「30」を入力します。</span><span class="sxs-lookup"><span data-stu-id="968aa-122">In the Days ahead field, enter '30'.</span></span>
    * <span data-ttu-id="968aa-123">これは需要計算に含まれるかんばん数量計算の日付より前の日数です。</span><span class="sxs-lookup"><span data-stu-id="968aa-123">This is the number of days prior to the kanban quantity calculation date that is included in the demand calculation.</span></span>  
11. <span data-ttu-id="968aa-124">[遅れた日数] フィールドに「30」を入力します。</span><span class="sxs-lookup"><span data-stu-id="968aa-124">In the Days behind field, enter '30'.</span></span>
    * <span data-ttu-id="968aa-125">これは、需要の計算に含まれるかんばん数量の計算の日付からの繰り越し日数です。</span><span class="sxs-lookup"><span data-stu-id="968aa-125">This is the number of days forward from the kanban quantity calculation date that is included in the demand calculation.</span></span>  <span data-ttu-id="968aa-126">計算に使用する式は、実際の値とともに表示されます。</span><span class="sxs-lookup"><span data-stu-id="968aa-126">The formula used for the calculation is shown with the actual values.</span></span> <span data-ttu-id="968aa-127">たとえば、かんばん数量 = ((1 日の平均需要 x リード タイム x 2.00) / 材料取り扱い単位あたりの製品数量) + 1</span><span class="sxs-lookup"><span data-stu-id="968aa-127">For example,  Kanban quantity = ((Average daily demand x lead time x 2.00) / Product quantity per handling unit) + 1</span></span>  
12. <span data-ttu-id="968aa-128">ページを閉じます。</span><span class="sxs-lookup"><span data-stu-id="968aa-128">Close the page.</span></span>

## <a name="add-the-kanban-quantity-calculation-policy-to-a-kanban-rule"></a><span data-ttu-id="968aa-129">かんばん数量計算ポリシーをかんばんルールへ追加する</span><span class="sxs-lookup"><span data-stu-id="968aa-129">Add the kanban quantity calculation policy to a kanban rule</span></span>
1. <span data-ttu-id="968aa-130">[製品情報管理] > [リーン生産] > [かんばんルール] の順に移動します。</span><span class="sxs-lookup"><span data-stu-id="968aa-130">Go to Product information management > Lean manufacturing > Kanban rules.</span></span>
2. <span data-ttu-id="968aa-131">一覧で、目的のレコードを見つけ、選択します。</span><span class="sxs-lookup"><span data-stu-id="968aa-131">In the list, find and select the desired record.</span></span>
    * <span data-ttu-id="968aa-132">この手順では、かんばんルール 000020 を選択します。</span><span class="sxs-lookup"><span data-stu-id="968aa-132">Select kanban rule 000020 for this procedure.</span></span>  
3. <span data-ttu-id="968aa-133">一覧で、選択された行のリンクをクリックします。</span><span class="sxs-lookup"><span data-stu-id="968aa-133">In the list, click the link in the selected row.</span></span>
4. <span data-ttu-id="968aa-134">[かんばん数量計算ポリシー] セクションの展開を切り替えます。</span><span class="sxs-lookup"><span data-stu-id="968aa-134">Toggle the expansion of the Kanban quantity calculation policies section.</span></span>
5. <span data-ttu-id="968aa-135">[追加] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="968aa-135">Click Add.</span></span>
    * <span data-ttu-id="968aa-136">以前のサブタスクで作成したかんばん数量の計算ポリシーを追加します。</span><span class="sxs-lookup"><span data-stu-id="968aa-136">Add the kanban quantity calculation policy that you have just created in the previous sub-task.</span></span>  
6. <span data-ttu-id="968aa-137">一覧で、選択された行をマークします。</span><span class="sxs-lookup"><span data-stu-id="968aa-137">In the list, mark the selected row.</span></span>
7. <span data-ttu-id="968aa-138">[名前] フィールドで、ドロップ ダウン ボタンをクリックし、ルックアップを開きます。</span><span class="sxs-lookup"><span data-stu-id="968aa-138">In the Name field, click the drop-down button to open the lookup.</span></span>
8. <span data-ttu-id="968aa-139">一覧で、選択された行のリンクをクリックします。</span><span class="sxs-lookup"><span data-stu-id="968aa-139">In the list, click the link in the selected row.</span></span>
    * <span data-ttu-id="968aa-140">以前のサブタスクで作成した ポリシー Speaker2016 を追加します。</span><span class="sxs-lookup"><span data-stu-id="968aa-140">Select the policy Speaker2016 that you have just created in the previous sub-task.</span></span>  

