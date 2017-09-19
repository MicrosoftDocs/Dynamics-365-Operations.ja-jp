--- 
title: "かんばん数量計算ポリシーのかんばんルールへの追加"
description: "この手順では、かんばん数量の計算ポリシーを作成し、それをかんばんルールへ追加し、かんばんのサイズおよび数量を最適化することに焦点をあてます。"
author: ChristianRytt
manager: AnnBe
ms.date: 11/11/2016
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: yuyus
ms.search.scope: Operations
ms.search.region: Global
ms.author: crytt
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 663da58ef01b705c0c984fbfd3fce8bc31be04c6
ms.openlocfilehash: 6a947d4a5302c6ed1848396d50cfbfcb78aabf97
ms.contentlocale: ja-jp
ms.lasthandoff: 08/29/2017

---
# <a name="add-a-kanban-quantity-calculation-policy-to-a-kanban-rule"></a><span data-ttu-id="d0bf3-103">かんばん数量計算ポリシーのかんばんルールへの追加</span><span class="sxs-lookup"><span data-stu-id="d0bf3-103">Add a kanban quantity calculation policy to a kanban rule</span></span>

[!include[task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="d0bf3-104">この手順では、かんばん数量の計算ポリシーを作成し、それをかんばんルールへ追加し、かんばんのサイズおよび数量を最適化することに焦点をあてます。</span><span class="sxs-lookup"><span data-stu-id="d0bf3-104">This procedure focuses on creating a kanban quantity calculation policy and adding it to a kanban rule to optimize the kanban size and quantities.</span></span> <span data-ttu-id="d0bf3-105">この手順の作成に使用するデモ データの会社は USMF です。</span><span class="sxs-lookup"><span data-stu-id="d0bf3-105">The demo data company used to create this procedure is USMF.</span></span> <span data-ttu-id="d0bf3-106">この手順は、バリュー ストリーム マネージャーを対象としています。</span><span class="sxs-lookup"><span data-stu-id="d0bf3-106">This procedure is intended for the value stream manager.</span></span> <span data-ttu-id="d0bf3-107">この手順は、かんばん数量修正候補の計算という手順を作成するための前提条件です。</span><span class="sxs-lookup"><span data-stu-id="d0bf3-107">This procedure is a prerequisite for creating the procedure Calculate kanban quantity suggestions.</span></span> 


## <a name="create-a-kanban-quantity-calculation-policy"></a><span data-ttu-id="d0bf3-108">かんばん数量計算ポリシーの作成</span><span class="sxs-lookup"><span data-stu-id="d0bf3-108">Create a kanban quantity calculation policy</span></span>
1. <span data-ttu-id="d0bf3-109">[生産管理] > [定期処理タスク] > [かんばん数量の計算] > [かんばん数量の計算ポリシー] の順に移動します。</span><span class="sxs-lookup"><span data-stu-id="d0bf3-109">Go to Production control > Periodic tasks > Kanban quantity calculation > Kanban quantity calculation policies.</span></span>
2. <span data-ttu-id="d0bf3-110">[新規] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="d0bf3-110">Click New.</span></span>
3. <span data-ttu-id="d0bf3-111">[名前] フィールドに値を入力します。</span><span class="sxs-lookup"><span data-stu-id="d0bf3-111">In the Name field, type a value.</span></span>
    * <span data-ttu-id="d0bf3-112">たとえば、「Speaker2016」と入力します。</span><span class="sxs-lookup"><span data-stu-id="d0bf3-112">For example, type Speaker2016.</span></span>  
4. <span data-ttu-id="d0bf3-113">[マスター プラン] フィールドで、ドロップ ダウン ボタンをクリックし、ルックアップを開きます。</span><span class="sxs-lookup"><span data-stu-id="d0bf3-113">In the Master plan field, click the drop-down button to open the lookup.</span></span>
5. <span data-ttu-id="d0bf3-114">一覧で、目的のレコードを見つけ、選択します。</span><span class="sxs-lookup"><span data-stu-id="d0bf3-114">In the list, find and select the desired record.</span></span>
    * <span data-ttu-id="d0bf3-115">[StaticPlan] を選択して、需要を計算します。</span><span class="sxs-lookup"><span data-stu-id="d0bf3-115">Select StaticPlan to calculate demand.</span></span>  
6. <span data-ttu-id="d0bf3-116">一覧で、選択された行のリンクをクリックします。</span><span class="sxs-lookup"><span data-stu-id="d0bf3-116">In the list, click the link in the selected row.</span></span>
7. <span data-ttu-id="d0bf3-117">[保存] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="d0bf3-117">Click Save.</span></span>
8. <span data-ttu-id="d0bf3-118">[最小かんばん数量] フィールドに、「1」を入力します。</span><span class="sxs-lookup"><span data-stu-id="d0bf3-118">In the Minimum kanban quantity field, enter '1'.</span></span>
    * <span data-ttu-id="d0bf3-119">これはかんばん数量計算に含まれる追加のかんばんの数です。</span><span class="sxs-lookup"><span data-stu-id="d0bf3-119">This is the additional number of kanbans that is included in the kanban quantity calculation.</span></span>  
9. <span data-ttu-id="d0bf3-120">安全係数に「1」を設定します。</span><span class="sxs-lookup"><span data-stu-id="d0bf3-120">Set Safety factor to '1'.</span></span>
    * <span data-ttu-id="d0bf3-121">これは安全在庫の追加数量を計算するのに使用する係数です。</span><span class="sxs-lookup"><span data-stu-id="d0bf3-121">This is the factor that is used to calculate additional quantity of safety stock.</span></span>  
10. <span data-ttu-id="d0bf3-122">[進んだ日数] フィールドに「30」を入力します。</span><span class="sxs-lookup"><span data-stu-id="d0bf3-122">In the Days ahead field, enter '30'.</span></span>
    * <span data-ttu-id="d0bf3-123">これは需要計算に含まれるかんばん数量計算の日付より前の日数です。</span><span class="sxs-lookup"><span data-stu-id="d0bf3-123">This is the number of days prior to the kanban quantity calculation date that is included in the demand calculation.</span></span>  
11. <span data-ttu-id="d0bf3-124">[遅れた日数] フィールドに「30」を入力します。</span><span class="sxs-lookup"><span data-stu-id="d0bf3-124">In the Days behind field, enter '30'.</span></span>
    * <span data-ttu-id="d0bf3-125">これは、需要の計算に含まれるかんばん数量の計算の日付からの繰り越し日数です。</span><span class="sxs-lookup"><span data-stu-id="d0bf3-125">This is the number of days forward from the kanban quantity calculation date that is included in the demand calculation.</span></span>  <span data-ttu-id="d0bf3-126">計算に使用する式は、実際の値とともに表示されます。</span><span class="sxs-lookup"><span data-stu-id="d0bf3-126">The formula used for the calculation is shown with the actual values.</span></span> <span data-ttu-id="d0bf3-127">たとえば、かんばん数量 = ((1 日の平均需要 x リード タイム x 2.00) / 材料取り扱い単位あたりの製品数量) + 1 </span><span class="sxs-lookup"><span data-stu-id="d0bf3-127">For example,  Kanban quantity = ((Average daily demand x lead time x 2.00) / Product quantity per handling unit) + 1</span></span>  
12. <span data-ttu-id="d0bf3-128">ページを閉じます。</span><span class="sxs-lookup"><span data-stu-id="d0bf3-128">Close the page.</span></span>

## <a name="add-the-kanban-quantity-calculation-policy-to-a-kanban-rule"></a><span data-ttu-id="d0bf3-129">かんばん数量計算ポリシーをかんばんルールへ追加する</span><span class="sxs-lookup"><span data-stu-id="d0bf3-129">Add the kanban quantity calculation policy to a kanban rule</span></span>
1. <span data-ttu-id="d0bf3-130">[製品情報管理] > [リーン生産] > [かんばんルール] の順に移動します。</span><span class="sxs-lookup"><span data-stu-id="d0bf3-130">Go to Product information management > Lean manufacturing > Kanban rules.</span></span>
2. <span data-ttu-id="d0bf3-131">一覧で、目的のレコードを見つけ、選択します。</span><span class="sxs-lookup"><span data-stu-id="d0bf3-131">In the list, find and select the desired record.</span></span>
    * <span data-ttu-id="d0bf3-132">この手順では、かんばんルール 000020 を選択します。</span><span class="sxs-lookup"><span data-stu-id="d0bf3-132">Select kanban rule 000020 for this procedure.</span></span>  
3. <span data-ttu-id="d0bf3-133">一覧で、選択された行のリンクをクリックします。</span><span class="sxs-lookup"><span data-stu-id="d0bf3-133">In the list, click the link in the selected row.</span></span>
4. <span data-ttu-id="d0bf3-134">[かんばん数量計算ポリシー] セクションの展開を切り替えます。</span><span class="sxs-lookup"><span data-stu-id="d0bf3-134">Toggle the expansion of the Kanban quantity calculation policies section.</span></span>
5. <span data-ttu-id="d0bf3-135">[追加] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="d0bf3-135">Click Add.</span></span>
    * <span data-ttu-id="d0bf3-136">以前のサブタスクで作成したかんばん数量の計算ポリシーを追加します。</span><span class="sxs-lookup"><span data-stu-id="d0bf3-136">Add the kanban quantity calculation policy that you have just created in the previous sub-task.</span></span>  
6. <span data-ttu-id="d0bf3-137">一覧で、選択された行をマークします。</span><span class="sxs-lookup"><span data-stu-id="d0bf3-137">In the list, mark the selected row.</span></span>
7. <span data-ttu-id="d0bf3-138">[名前] フィールドで、ドロップ ダウン ボタンをクリックし、ルックアップを開きます。</span><span class="sxs-lookup"><span data-stu-id="d0bf3-138">In the Name field, click the drop-down button to open the lookup.</span></span>
8. <span data-ttu-id="d0bf3-139">一覧で、選択された行のリンクをクリックします。</span><span class="sxs-lookup"><span data-stu-id="d0bf3-139">In the list, click the link in the selected row.</span></span>
    * <span data-ttu-id="d0bf3-140">以前のサブタスクで作成した ポリシー Speaker2016 を追加します。</span><span class="sxs-lookup"><span data-stu-id="d0bf3-140">Select the policy Speaker2016 that you have just created in the previous sub-task.</span></span>  

