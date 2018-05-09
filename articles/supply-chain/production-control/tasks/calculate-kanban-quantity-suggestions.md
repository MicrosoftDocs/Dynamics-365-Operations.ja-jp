--- 
title: "かんばん数量修正候補の計算"
description: "この手順では、かんばん数量計算を使用して、特定のかんばんルールに対してかんばんのサイズおよび数量を最適化することに焦点をあてます。"
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
ms.search.industry: Manufacturing
ms.author: crytt
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: efcb77ff883b29a4bbaba27551e02311742afbbd
ms.openlocfilehash: 8c9a7d7e4e2d751722dac8089bc2056334fa96a3
ms.contentlocale: ja-jp
ms.lasthandoff: 05/08/2018

---
# <a name="calculate-kanban-quantity-suggestions"></a><span data-ttu-id="8d1aa-103">かんばん数量修正候補の計算</span><span class="sxs-lookup"><span data-stu-id="8d1aa-103">Calculate kanban quantity suggestions</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="8d1aa-104">この手順では、かんばん数量計算を使用して、特定のかんばんルールに対してかんばんのサイズおよび数量を最適化することに焦点をあてます。</span><span class="sxs-lookup"><span data-stu-id="8d1aa-104">This procedure focuses on optimizing the kanban size and quantities for a specific kanban rule by using the kanban quantity calculation.</span></span> <span data-ttu-id="8d1aa-105">この手順の作成に使用するデモ データの会社は USMF です。</span><span class="sxs-lookup"><span data-stu-id="8d1aa-105">The demo data company used to create this procedure is USMF.</span></span> <span data-ttu-id="8d1aa-106">この手順は、バリュー ストリーム マネージャーを対象としています。</span><span class="sxs-lookup"><span data-stu-id="8d1aa-106">This procedure is intended for the value stream manager.</span></span> <span data-ttu-id="8d1aa-107">「かんばん数量計算ポリシーをかんばんルールへ追加する」という手順を事前に完了しておく必要があります。</span><span class="sxs-lookup"><span data-stu-id="8d1aa-107">It is a prerequisite that you have completed the procedure Add a new kanban quantity calculation policy to a kanban rule.</span></span>


## <a name="create-a-kanban-quantity-calculation"></a><span data-ttu-id="8d1aa-108">かんばん数量計算の作成</span><span class="sxs-lookup"><span data-stu-id="8d1aa-108">Create a kanban quantity calculation</span></span>
1. <span data-ttu-id="8d1aa-109">[生産管理] > [定期処理タスク] > [かんばん数量の計算] > [かんばん数量の計算] の順に移動します。</span><span class="sxs-lookup"><span data-stu-id="8d1aa-109">Go to Production control > Periodic tasks > Kanban quantity calculation > Calculate kanban quantity.</span></span>
2. <span data-ttu-id="8d1aa-110">[新規] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="8d1aa-110">Click New.</span></span>
3. <span data-ttu-id="8d1aa-111">[名前] フィールドに、「Speaker2016」と入力します。</span><span class="sxs-lookup"><span data-stu-id="8d1aa-111">In the Name field, type 'Speaker2016'.</span></span>
4. <span data-ttu-id="8d1aa-112">[名前] フィールドで、ドロップ ダウン ボタンをクリックし、ルックアップを開きます。</span><span class="sxs-lookup"><span data-stu-id="8d1aa-112">In the Name field, click the drop-down button to open the lookup.</span></span>
    * <span data-ttu-id="8d1aa-113">「かんばん数量計算ポリシーをかんばんルールへ追加する」という手順に基づいて作成されたポリシーを選択します。</span><span class="sxs-lookup"><span data-stu-id="8d1aa-113">Select the policy that you have created in the procedure Add a new kanban quantity calculation policy to a kanban rule.</span></span> <span data-ttu-id="8d1aa-114">たとえば、「Speaker2016」です。</span><span class="sxs-lookup"><span data-stu-id="8d1aa-114">For example, Speaker2016.</span></span>  
5. <span data-ttu-id="8d1aa-115">一覧で、選択された行のリンクをクリックします。</span><span class="sxs-lookup"><span data-stu-id="8d1aa-115">In the list, click the link in the selected row.</span></span>
6. <span data-ttu-id="8d1aa-116">[現在の日付で有効なルール] フィールドで、日時を「2012-12-17T08:00:00」と設定します</span><span class="sxs-lookup"><span data-stu-id="8d1aa-116">In the Rule active as of date field, set the date and time to '2012-12-17T08:00:00'.</span></span>
    * <span data-ttu-id="8d1aa-117">この日付は、かんばん数量計算に含まれている固定かんばんルールを特定する基準として使用されます。</span><span class="sxs-lookup"><span data-stu-id="8d1aa-117">This date serves as the basis for determining which fixed kanban rules are included in the kanban quantity calculation.</span></span>  
7. <span data-ttu-id="8d1aa-118">[履行済需要期間の開始日] フィールドで、日時を「2012-11-17T09:00:00」と設定します</span><span class="sxs-lookup"><span data-stu-id="8d1aa-118">In the Fulfilled demand period start date field, set the date and time to '2012-11-17T09:00:00'.</span></span>
    * <span data-ttu-id="8d1aa-119">過去の需要トランザクションを含めてかんばん数量を計算する開始日です。</span><span class="sxs-lookup"><span data-stu-id="8d1aa-119">The date from when past demand transactions are included to calculate the kanban quantity.</span></span>  
8. <span data-ttu-id="8d1aa-120">[履行済需要期間の終了日] フィールドで、日時を「2012-12-17T07:59:59」と設定します。</span><span class="sxs-lookup"><span data-stu-id="8d1aa-120">In the Fulfilled demand period end date field, set the date and time to '2012-12-17T07:59:59'.</span></span>
    * <span data-ttu-id="8d1aa-121">過去の需要トランザクションを含めてかんばん数量を計算する最終日です。</span><span class="sxs-lookup"><span data-stu-id="8d1aa-121">The date until when past demand transactions are included to calculate the kanban quantity.</span></span>  
9. <span data-ttu-id="8d1aa-122">[需要期間の開始日] フィールドで、日時を「2012-12-17T08:00:00」と設定します</span><span class="sxs-lookup"><span data-stu-id="8d1aa-122">In the Demand period start date field, set the date and time to '2012-12-17T08:00:00'.</span></span>
    * <span data-ttu-id="8d1aa-123">現在の需要トランザクションを含めてかんばん数量を計算する開始日です。</span><span class="sxs-lookup"><span data-stu-id="8d1aa-123">The date from when current demand transactions are included to calculate the kanban quantity.</span></span>  
10. <span data-ttu-id="8d1aa-124">[需要期間の最終日] フィールドで、日時を「2013-01-16T07:59:59」と設定します</span><span class="sxs-lookup"><span data-stu-id="8d1aa-124">In the Demand period end date field, set the date and time to '2013-01-16T07:59:59'.</span></span>
    * <span data-ttu-id="8d1aa-125">現在の需要トランザクションを含めてかんばん数量を計算する最終日です。</span><span class="sxs-lookup"><span data-stu-id="8d1aa-125">The date until when current demand transactions are included to calculate the kanban quantity.</span></span>  

## <a name="generate-kanban-quantity-proposal"></a><span data-ttu-id="8d1aa-126">かんばん数量提案に生成</span><span class="sxs-lookup"><span data-stu-id="8d1aa-126">Generate kanban quantity proposal</span></span>
1. <span data-ttu-id="8d1aa-127">[保存] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="8d1aa-127">Click Save.</span></span>
2. <span data-ttu-id="8d1aa-128">[生成] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="8d1aa-128">Click Generate.</span></span>
    * <span data-ttu-id="8d1aa-129">これにより、かんばんルール 000020 のかんばん数量提案明細行が生成されます。</span><span class="sxs-lookup"><span data-stu-id="8d1aa-129">This generates a kanban quantity proposal line for the kanban rule 000020.</span></span>  

## <a name="run-kanban-quantity-calculation"></a><span data-ttu-id="8d1aa-130">かんばん数量計算の実行</span><span class="sxs-lookup"><span data-stu-id="8d1aa-130">Run kanban quantity calculation</span></span>
1. <span data-ttu-id="8d1aa-131">[計算] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="8d1aa-131">Click Calculate.</span></span>
    * <span data-ttu-id="8d1aa-132">これにより、かんばん数量の提案が計算されます。</span><span class="sxs-lookup"><span data-stu-id="8d1aa-132">This calculates the kanban quantity proposal.</span></span>  
2. <span data-ttu-id="8d1aa-133">[OK] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="8d1aa-133">Click OK.</span></span>
3. <span data-ttu-id="8d1aa-134">一覧で、選択された行をマークします。</span><span class="sxs-lookup"><span data-stu-id="8d1aa-134">In the list, mark the selected row.</span></span>
    * <span data-ttu-id="8d1aa-135">提案されたかんばん数量が 2.であることに注意します。</span><span class="sxs-lookup"><span data-stu-id="8d1aa-135">Notice the suggested kanban quantity is 2.</span></span>  

## <a name="change-product-quantity-and-calculate-again"></a><span data-ttu-id="8d1aa-136">製品数量および再計算の変更</span><span class="sxs-lookup"><span data-stu-id="8d1aa-136">Change product quantity and calculate again</span></span>
1. <span data-ttu-id="8d1aa-137">製品数量を「5」と設定します。</span><span class="sxs-lookup"><span data-stu-id="8d1aa-137">Set Product quantity to '5'.</span></span>
2. <span data-ttu-id="8d1aa-138">[計算] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="8d1aa-138">Click Calculate.</span></span>
3. <span data-ttu-id="8d1aa-139">[OK] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="8d1aa-139">Click OK.</span></span>
    * <span data-ttu-id="8d1aa-140">かんばん数量 5 からかんばん数量 4 に変更することが推奨されています。</span><span class="sxs-lookup"><span data-stu-id="8d1aa-140">Notice that with a kanban quantity of 5, the suggestion is changed to a kanban quantity of 4.</span></span>  
    * <span data-ttu-id="8d1aa-141">これは、より少ない製品数量においては、その需要を満たすためにさらなるかんばんが必要となることが原因です。</span><span class="sxs-lookup"><span data-stu-id="8d1aa-141">This is caused by the fact that with a lower product quantity, we need more kanbans to fulfill the demand.</span></span>  

## <a name="update-kanban-rule"></a><span data-ttu-id="8d1aa-142">かんばんルールの更新</span><span class="sxs-lookup"><span data-stu-id="8d1aa-142">Update kanban rule</span></span>
1. <span data-ttu-id="8d1aa-143">[ルールの有効日] フィールドに日時を入力します。</span><span class="sxs-lookup"><span data-stu-id="8d1aa-143">In the Rule effective date field, enter a date and time.</span></span>
    * <span data-ttu-id="8d1aa-144">「現在の日付で有効なルール」を将来の日付に設定します。</span><span class="sxs-lookup"><span data-stu-id="8d1aa-144">Set the 'Rule active as of date' to a date in the future.</span></span> <span data-ttu-id="8d1aa-145">たとえば、今日 + 1 年です。</span><span class="sxs-lookup"><span data-stu-id="8d1aa-145">For example, today + one year.</span></span>  
2. <span data-ttu-id="8d1aa-146">[更新] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="8d1aa-146">Click Update.</span></span>
3. <span data-ttu-id="8d1aa-147">[OK] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="8d1aa-147">Click OK.</span></span>
4. <span data-ttu-id="8d1aa-148">ページを閉じます。</span><span class="sxs-lookup"><span data-stu-id="8d1aa-148">Close the page.</span></span>

## <a name="validate-change-on-kanban-rule"></a><span data-ttu-id="8d1aa-149">かんばんルールの変更の検証</span><span class="sxs-lookup"><span data-stu-id="8d1aa-149">Validate change on kanban rule</span></span>
1. <span data-ttu-id="8d1aa-150">[製品情報管理] > [リーン生産] > [かんばんルール] の順に移動します。</span><span class="sxs-lookup"><span data-stu-id="8d1aa-150">Go to Product information management > Lean manufacturing > Kanban rules.</span></span>
2. <span data-ttu-id="8d1aa-151">一覧で、選択された行のリンクをクリックします。</span><span class="sxs-lookup"><span data-stu-id="8d1aa-151">In the list, click the link in the selected row.</span></span>
    * <span data-ttu-id="8d1aa-152">以前のサブタスクで作成されたかんばんルールを選択します。</span><span class="sxs-lookup"><span data-stu-id="8d1aa-152">Select the kanban rule that was created in the previous sub-task.</span></span> <span data-ttu-id="8d1aa-153">これは、数字で並べ替えた一覧にある最初のかんばんルールです。</span><span class="sxs-lookup"><span data-stu-id="8d1aa-153">This should be the first kanban rule in the list sorted by number.</span></span>  
3. <span data-ttu-id="8d1aa-154">[詳細] セクションの展開を切り替えます。</span><span class="sxs-lookup"><span data-stu-id="8d1aa-154">Toggle the expansion of the Details section.</span></span>
    * <span data-ttu-id="8d1aa-155">有効日に注意します。この日付までこのルールが有効化されないことを意味します。</span><span class="sxs-lookup"><span data-stu-id="8d1aa-155">Notice the effective date, which means that this rule is not activated until this date.</span></span>  
4. <span data-ttu-id="8d1aa-156">[数量] セクションの展開を切り替えます。</span><span class="sxs-lookup"><span data-stu-id="8d1aa-156">Toggle the expansion of the Quantities section.</span></span>
    * <span data-ttu-id="8d1aa-157">これはかんばん数量計算に入力した既定の数量であることを確認します。</span><span class="sxs-lookup"><span data-stu-id="8d1aa-157">Notice this is the default quantity that you entered on the kanban quantity calculation.</span></span>  
    * <span data-ttu-id="8d1aa-158">これは、かんばん数量計算から算出した固定かんばん数量 4 です。</span><span class="sxs-lookup"><span data-stu-id="8d1aa-158">Notice this is the fixed kanban quantity of 4 from the kanban quantity calculation.</span></span>  
5. <span data-ttu-id="8d1aa-159">[ListPanel] タブをクリックします。</span><span class="sxs-lookup"><span data-stu-id="8d1aa-159">Click the ListPanel tab.</span></span>


