--- 
title: "報酬グリッドの設定"
description: "[報酬] グリッドは、固定報酬プランの支払構造を定義または維持するために使用します。"
author: kherr75
manager: AnnBe
ms.date: 03/02/2016
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: rschloma
ms.search.scope: Operations
ms.search.region: Global
ms.author: kherr
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 663da58ef01b705c0c984fbfd3fce8bc31be04c6
ms.openlocfilehash: 258149dbd610dafb8daacaf54c61e69898ca35d6
ms.contentlocale: ja-jp
ms.lasthandoff: 08/29/2017

---
# <a name="set-up-compensation-grids"></a><span data-ttu-id="43080-103">報酬グリッドの設定</span><span class="sxs-lookup"><span data-stu-id="43080-103">Set up compensation grids</span></span>

[!include[task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="43080-104">[報酬] グリッドは、固定報酬プランの支払構造を定義または維持するために使用します。</span><span class="sxs-lookup"><span data-stu-id="43080-104">Compensation grids are used to define and maintain the pay structures for fixed compensation plans.</span></span> <span data-ttu-id="43080-105">[報酬] グリッドは、複数のプラン間で共有または新しい報酬プランの作成時にコピーすることができます。</span><span class="sxs-lookup"><span data-stu-id="43080-105">Compensation grids can be shared between multiple plans or copied when creating a new compensation plan.</span></span>  <span data-ttu-id="43080-106">報酬グリッドを作成する前に、[レベル] と [基準] ポイントを設定する必要があります。</span><span class="sxs-lookup"><span data-stu-id="43080-106">Before creating a compensation grid, Levels and Reference points must be set up.</span></span> <span data-ttu-id="43080-107">この例では、[レベル] と [基準] ポイントのデモ データを使用して、報酬グリッドの新しい [等級] タイプを作成します。</span><span class="sxs-lookup"><span data-stu-id="43080-107">This example will create a new Grade type of compensation grid using demo data for the Levels and Reference points.</span></span> <span data-ttu-id="43080-108">この手順の作成に使用するデモ データの会社は USMF です。</span><span class="sxs-lookup"><span data-stu-id="43080-108">The demo data company used to create this procedure is USMF.</span></span>


## <a name="set-up-information-about-the-compensation-grid"></a><span data-ttu-id="43080-109">報酬グリッドに関する情報の設定</span><span class="sxs-lookup"><span data-stu-id="43080-109">Set up information about the compensation grid</span></span>
1. <span data-ttu-id="43080-110">[人事管理] > [報酬] > [固定報酬] > [報酬グリッド] の順に移動します。</span><span class="sxs-lookup"><span data-stu-id="43080-110">Go to Human resources > Compensation > Fixed compensation > Compensation grids.</span></span>
2. <span data-ttu-id="43080-111">[新規] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="43080-111">Click New.</span></span>
3. <span data-ttu-id="43080-112">[グリッド] フィールドに値を入力します。</span><span class="sxs-lookup"><span data-stu-id="43080-112">In the Grid field, type a value.</span></span>
4. <span data-ttu-id="43080-113">[説明] フィールドに値を入力します。</span><span class="sxs-lookup"><span data-stu-id="43080-113">In the Description field, type a value.</span></span>
5. <span data-ttu-id="43080-114">[タイプ] フィールドで、オプションを選択します。</span><span class="sxs-lookup"><span data-stu-id="43080-114">In the Type field, select an option.</span></span>
6. <span data-ttu-id="43080-115">[参照設定] フィールドで、値を入力または選択します。</span><span class="sxs-lookup"><span data-stu-id="43080-115">In the Reference setup field, enter or select a value.</span></span>
7. <span data-ttu-id="43080-116">[通貨] フィールドで値を入力または選択します。</span><span class="sxs-lookup"><span data-stu-id="43080-116">In the Currency field, enter or select a value.</span></span>
8. <span data-ttu-id="43080-117">[通貨] フィールドに値を入力します。</span><span class="sxs-lookup"><span data-stu-id="43080-117">In the Currency field, type a value.</span></span>
9. <span data-ttu-id="43080-118">[有効日] フィールドに日付を入力します。</span><span class="sxs-lookup"><span data-stu-id="43080-118">In the Effective date field, enter a date.</span></span>

## <a name="add-levels-to-the-compensation-structure"></a><span data-ttu-id="43080-119">報酬構造にレベルを追加</span><span class="sxs-lookup"><span data-stu-id="43080-119">Add levels to the compensation structure</span></span>
1. <span data-ttu-id="43080-120">[報酬構造] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="43080-120">Click Compensation structure.</span></span>
2. <span data-ttu-id="43080-121">一覧で、選択された行をマークします。</span><span class="sxs-lookup"><span data-stu-id="43080-121">In the list, mark the selected row.</span></span>
3. <span data-ttu-id="43080-122">[レベル] フィールドで、値を入力または選択します。</span><span class="sxs-lookup"><span data-stu-id="43080-122">In the Level field, enter or select a value.</span></span>
4. <span data-ttu-id="43080-123">[新規] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="43080-123">Click New.</span></span>
5. <span data-ttu-id="43080-124">一覧で、選択された行をマークします。</span><span class="sxs-lookup"><span data-stu-id="43080-124">In the list, mark the selected row.</span></span>
6. <span data-ttu-id="43080-125">[レベル] フィールドで、値を入力または選択します。</span><span class="sxs-lookup"><span data-stu-id="43080-125">In the Level field, enter or select a value.</span></span>
7. <span data-ttu-id="43080-126">[新規] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="43080-126">Click New.</span></span>
8. <span data-ttu-id="43080-127">一覧で、選択された行をマークします。</span><span class="sxs-lookup"><span data-stu-id="43080-127">In the list, mark the selected row.</span></span>
9. <span data-ttu-id="43080-128">[レベル] フィールドで、値を入力または選択します。</span><span class="sxs-lookup"><span data-stu-id="43080-128">In the Level field, enter or select a value.</span></span>
10. <span data-ttu-id="43080-129">[新規] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="43080-129">Click New.</span></span>
11. <span data-ttu-id="43080-130">一覧で、選択された行をマークします。</span><span class="sxs-lookup"><span data-stu-id="43080-130">In the list, mark the selected row.</span></span>
12. <span data-ttu-id="43080-131">[レベル] フィールドで、値を入力または選択します。</span><span class="sxs-lookup"><span data-stu-id="43080-131">In the Level field, enter or select a value.</span></span>
13. <span data-ttu-id="43080-132">[新規] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="43080-132">Click New.</span></span>
14. <span data-ttu-id="43080-133">一覧で、選択された行をマークします。</span><span class="sxs-lookup"><span data-stu-id="43080-133">In the list, mark the selected row.</span></span>
15. <span data-ttu-id="43080-134">[レベル] フィールドで、値を入力または選択します。</span><span class="sxs-lookup"><span data-stu-id="43080-134">In the Level field, enter or select a value.</span></span>

## <a name="fill-in-the-compensation-structure-with-values"></a><span data-ttu-id="43080-135">値を含む報酬構造の入力</span><span class="sxs-lookup"><span data-stu-id="43080-135">Fill in the compensation structure with values</span></span>
1. <span data-ttu-id="43080-136">一覧で、選択された行をマークします。</span><span class="sxs-lookup"><span data-stu-id="43080-136">In the list, mark the selected row.</span></span>
    * <span data-ttu-id="43080-137">この時点で、報酬の値は、テーブルの各フィールドに手動で入力できます。または、複数のフィールドに簡単に入力して、基本的な計算を実行するのに、[一括変更] 機能を使用できます。</span><span class="sxs-lookup"><span data-stu-id="43080-137">At this point, compensation values can manually be entered into each field in the table, or the Mass change functionality can be used to easily fill in multiple fields and perform basic calculations.</span></span>  
2. <span data-ttu-id="43080-138">[一括変更] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="43080-138">Click Mass change.</span></span>
    * <span data-ttu-id="43080-139">このグリッドでは、まず最初のレベルの平均支給額をテーブルのすべてのフィールドに適用します。</span><span class="sxs-lookup"><span data-stu-id="43080-139">For this grid, we'll first apply the value for the midpoint of the first level's to all the fields in the table.</span></span> <span data-ttu-id="43080-140">これは、報酬マトリックスの基準になります。</span><span class="sxs-lookup"><span data-stu-id="43080-140">This will be the basis for the compensation matrix.</span></span>  
3. <span data-ttu-id="43080-141">[調整のタイプ] フィールドでオプションを選択します。</span><span class="sxs-lookup"><span data-stu-id="43080-141">In the Adjustment type field, select an option.</span></span>
4. <span data-ttu-id="43080-142">[調整金額] フィールドで、数値を入力します。</span><span class="sxs-lookup"><span data-stu-id="43080-142">In the Adjustment amount field, enter a number.</span></span>
5. <span data-ttu-id="43080-143">一覧で、すべての行のマークを設定または解除します。</span><span class="sxs-lookup"><span data-stu-id="43080-143">In the list, mark or unmark all rows.</span></span>
6. <span data-ttu-id="43080-144">[グリッドに適用] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="43080-144">Click Apply to grid.</span></span>
    * <span data-ttu-id="43080-145">ここで、一定の割合または金額で、後続の各レベルの金額を増加させるために一括変更機能を使用します。</span><span class="sxs-lookup"><span data-stu-id="43080-145">Now we'll use the mass change function to increment the amounts in each subsequent level by a certain percentage or amount.</span></span> <span data-ttu-id="43080-146">この例では、各段階の平均間で 12.5% の分散があります。</span><span class="sxs-lookup"><span data-stu-id="43080-146">In this example, each grade will have a 12.5% spread between their midpoints.</span></span>  
7. <span data-ttu-id="43080-147">[調整のタイプ] フィールドでオプションを選択します。</span><span class="sxs-lookup"><span data-stu-id="43080-147">In the Adjustment type field, select an option.</span></span>
8. <span data-ttu-id="43080-148">[調整金額] フィールドで、数値を入力します。</span><span class="sxs-lookup"><span data-stu-id="43080-148">In the Adjustment amount field, enter a number.</span></span>
9. <span data-ttu-id="43080-149">一覧で、目的のレコードを見つけ、選択します。</span><span class="sxs-lookup"><span data-stu-id="43080-149">In the list, find and select the desired record.</span></span>
10. <span data-ttu-id="43080-150">一覧で、目的のレコードを見つけ、選択します。</span><span class="sxs-lookup"><span data-stu-id="43080-150">In the list, find and select the desired record.</span></span>
11. <span data-ttu-id="43080-151">一覧で、目的のレコードを見つけ、選択します。</span><span class="sxs-lookup"><span data-stu-id="43080-151">In the list, find and select the desired record.</span></span>
12. <span data-ttu-id="43080-152">一覧で、目的のレコードを見つけ、選択します。</span><span class="sxs-lookup"><span data-stu-id="43080-152">In the list, find and select the desired record.</span></span>
13. <span data-ttu-id="43080-153">[グリッドに適用] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="43080-153">Click Apply to grid.</span></span>
14. <span data-ttu-id="43080-154">一覧で、目的のレコードを見つけ、選択します。</span><span class="sxs-lookup"><span data-stu-id="43080-154">In the list, find and select the desired record.</span></span>
15. <span data-ttu-id="43080-155">一覧で、目的のレコードを見つけ、選択します。</span><span class="sxs-lookup"><span data-stu-id="43080-155">In the list, find and select the desired record.</span></span>
16. <span data-ttu-id="43080-156">一覧で、目的のレコードを見つけ、選択します。</span><span class="sxs-lookup"><span data-stu-id="43080-156">In the list, find and select the desired record.</span></span>
17. <span data-ttu-id="43080-157">[グリッドに適用] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="43080-157">Click Apply to grid.</span></span>
18. <span data-ttu-id="43080-158">一覧で、目的のレコードを見つけ、選択します。</span><span class="sxs-lookup"><span data-stu-id="43080-158">In the list, find and select the desired record.</span></span>
19. <span data-ttu-id="43080-159">一覧で、目的のレコードを見つけ、選択します。</span><span class="sxs-lookup"><span data-stu-id="43080-159">In the list, find and select the desired record.</span></span>
20. <span data-ttu-id="43080-160">[グリッドに適用] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="43080-160">Click Apply to grid.</span></span>
21. <span data-ttu-id="43080-161">一覧で、目的のレコードを見つけ、選択します。</span><span class="sxs-lookup"><span data-stu-id="43080-161">In the list, find and select the desired record.</span></span>
22. <span data-ttu-id="43080-162">[グリッドに適用] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="43080-162">Click Apply to grid.</span></span>
    * <span data-ttu-id="43080-163">ここで、各レベルの最小基準点と最大基準点を調整するために、一括変更機能を使用します。</span><span class="sxs-lookup"><span data-stu-id="43080-163">Now we'll use the mass change function to adjust the Minimum and Maximum reference points for each level.</span></span> <span data-ttu-id="43080-164">この例では、50% 分散を使用し、最小基準点は -20%、 最大基準点は +20% 調整されます。</span><span class="sxs-lookup"><span data-stu-id="43080-164">This example will use a 50% spread so the Minimum reference point will be adjusted -20% and the Maximum will be adjusted +20%.</span></span>  
23. <span data-ttu-id="43080-165">[調整金額] フィールドで、数値を入力します。</span><span class="sxs-lookup"><span data-stu-id="43080-165">In the Adjustment amount field, enter a number.</span></span>
24. <span data-ttu-id="43080-166">[基準点] フィールドで、値を入力または選択します。</span><span class="sxs-lookup"><span data-stu-id="43080-166">In the Reference point field, enter or select a value.</span></span>
25. <span data-ttu-id="43080-167">一覧で、すべての行のマークを設定または解除します。</span><span class="sxs-lookup"><span data-stu-id="43080-167">In the list, mark or unmark all rows.</span></span>
26. <span data-ttu-id="43080-168">[グリッドに適用] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="43080-168">Click Apply to grid.</span></span>
27. <span data-ttu-id="43080-169">[調整金額] フィールドで、数値を入力します。</span><span class="sxs-lookup"><span data-stu-id="43080-169">In the Adjustment amount field, enter a number.</span></span>
28. <span data-ttu-id="43080-170">[基準点] フィールドで、値を入力または選択します。</span><span class="sxs-lookup"><span data-stu-id="43080-170">In the Reference point field, enter or select a value.</span></span>
29. <span data-ttu-id="43080-171">一覧で、すべての行のマークを設定または解除します。</span><span class="sxs-lookup"><span data-stu-id="43080-171">In the list, mark or unmark all rows.</span></span>
30. <span data-ttu-id="43080-172">[グリッドに適用] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="43080-172">Click Apply to grid.</span></span>

