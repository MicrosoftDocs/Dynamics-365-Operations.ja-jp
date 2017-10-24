--- 
title: "ロイヤルティ プログラムの定義"
description: "この手順は、二つのロイヤルティ層でのロイヤルティ プログラムの設定方法を示します。"
author: jashanno
manager: AnnBe
ms.date: 11/14/2016
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: josaw
ms.search.scope: Operations
ms.search.region: Global
ms.search.industry: Retail
ms.author: jashanno
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 7e0a5d044133b917a3eb9386773205218e5c1b40
ms.openlocfilehash: 7a949d5cb4f01518b46bc4b1769de34196109050
ms.contentlocale: ja-jp
ms.lasthandoff: 09/29/2017

---
# <a name="define-loyalty-programs"></a><span data-ttu-id="b3194-103">ロイヤルティ プログラムの定義</span><span class="sxs-lookup"><span data-stu-id="b3194-103">Define loyalty programs</span></span>

[!include[task guide banner](../includes/task-guide-banner.md)]

<span data-ttu-id="b3194-104">この手順は、二つのロイヤルティ層でのロイヤルティ プログラムの設定方法を示します。</span><span class="sxs-lookup"><span data-stu-id="b3194-104">This procedure shows how to set up a loyalty program with two loyalty tiers.</span></span> <span data-ttu-id="b3194-105">この手順では、デモ データの会社 USRT を使用します。</span><span class="sxs-lookup"><span data-stu-id="b3194-105">This procedure uses the USRT demo data company.</span></span>

1. <span data-ttu-id="b3194-106">Retail と Commerce > .. に移動します</span><span class="sxs-lookup"><span data-stu-id="b3194-106">Go to Retail and commerce > ..</span></span> <span data-ttu-id="b3194-107">> ロイヤルティ プログラム。</span><span class="sxs-lookup"><span data-stu-id="b3194-107">> Loyalty programs.</span></span>
2. <span data-ttu-id="b3194-108">[新規] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="b3194-108">Click New.</span></span>
3. <span data-ttu-id="b3194-109">[名前] フィールドに値を入力します。</span><span class="sxs-lookup"><span data-stu-id="b3194-109">In the Name field, type a value.</span></span>
4. <span data-ttu-id="b3194-110">[説明] フィールドに値を入力します。</span><span class="sxs-lookup"><span data-stu-id="b3194-110">In the Description field, type a value.</span></span>
5. <span data-ttu-id="b3194-111">[行の追加] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="b3194-111">Click Add line.</span></span>
6. <span data-ttu-id="b3194-112">[レベル] フィールドに数値を入力します。</span><span class="sxs-lookup"><span data-stu-id="b3194-112">In the Level field, enter a number.</span></span>
7. <span data-ttu-id="b3194-113">[層] フィールドに、ロイヤルティ層の名前を入力します。</span><span class="sxs-lookup"><span data-stu-id="b3194-113">In the Tier field, enter a name for the loyalty tier.</span></span>
8. <span data-ttu-id="b3194-114">[説明] フィールドで値を入力します。</span><span class="sxs-lookup"><span data-stu-id="b3194-114">In the Description field, type a value.</span></span>
9. <span data-ttu-id="b3194-115">[日付範囲] フィールドで、ドロップ ダウン ボタンをクリックし、ルックアップを開きます。</span><span class="sxs-lookup"><span data-stu-id="b3194-115">In the Date interval field, click the drop-down button to open the lookup.</span></span>
    * <span data-ttu-id="b3194-116">この日付範囲は、延長する必要があります。</span><span class="sxs-lookup"><span data-stu-id="b3194-116">This date interval should extend into the future.</span></span> <span data-ttu-id="b3194-117">たとえば、ゴールド層に対して選択された日付範囲が 1 年の期間の場合、ゴールド層を利用する顧客は、1 年間、ゴールド層に割り当てられている報酬を受け取ることができます。</span><span class="sxs-lookup"><span data-stu-id="b3194-117">For example, if the date interval that is selected for gold tier is a one-year period, any customer who qualifies for the gold tier can receive the rewards that are assigned to the gold tier for one year.</span></span> <span data-ttu-id="b3194-118">顧客がゴールド層にいる間にその層を利用する資格を再取得した場合、再取得した日付からもう 1 年、ゴールド層の有効期限が切れる日付が延長されます。</span><span class="sxs-lookup"><span data-stu-id="b3194-118">If the customer re-qualifies for the gold tier while they are in the tier, the date that the tier expires is extended by another year from the date when they re-qualify.</span></span>  
10. <span data-ttu-id="b3194-119">一覧で、選択された行のリンクをクリックします。</span><span class="sxs-lookup"><span data-stu-id="b3194-119">In the list, click the link in the selected row.</span></span>
11. <span data-ttu-id="b3194-120">[明細行の追加] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="b3194-120">Click Add line.</span></span>
12. <span data-ttu-id="b3194-121">[レベル] フィールドに数値を入力します。</span><span class="sxs-lookup"><span data-stu-id="b3194-121">In the Level field, enter a number.</span></span>
13. <span data-ttu-id="b3194-122">[層] フィールドに、ロイヤルティ層の名前を入力します。</span><span class="sxs-lookup"><span data-stu-id="b3194-122">In the Tier field, enter a name for the loyalty tier.</span></span>
14. <span data-ttu-id="b3194-123">[説明] フィールドで値を入力します。</span><span class="sxs-lookup"><span data-stu-id="b3194-123">In the Description field, type a value.</span></span>
15. <span data-ttu-id="b3194-124">[日付範囲] フィールドで、ドロップ ダウン ボタンをクリックし、ルックアップを開きます。</span><span class="sxs-lookup"><span data-stu-id="b3194-124">In the Date interval field, click the drop-down button to open the lookup.</span></span>
16. <span data-ttu-id="b3194-125">一覧で、選択された行のリンクをクリックします。</span><span class="sxs-lookup"><span data-stu-id="b3194-125">In the list, click the link in the selected row.</span></span>
17. <span data-ttu-id="b3194-126">[保存] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="b3194-126">Click Save.</span></span>
18. <span data-ttu-id="b3194-127">一覧で、目的のレコードを見つけ、選択します。</span><span class="sxs-lookup"><span data-stu-id="b3194-127">In the list, find and select the desired record.</span></span>
    * <span data-ttu-id="b3194-128">層ルールは、層を利用するために期間中に最低限必要となる報酬ポイントを定義します。</span><span class="sxs-lookup"><span data-stu-id="b3194-128">Tier rules define the minimum number of a reward point needed to be earned during a time period to qualify for the tier.</span></span>  
19. <span data-ttu-id="b3194-129">[層ルール] セクションの展開を切り替えます。</span><span class="sxs-lookup"><span data-stu-id="b3194-129">Toggle the expansion of the Tier rules section.</span></span>
20. <span data-ttu-id="b3194-130">[新規] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="b3194-130">Click New.</span></span>
    * <span data-ttu-id="b3194-131">1 つの層で複数の層ルールを使用できます。</span><span class="sxs-lookup"><span data-stu-id="b3194-131">You can have more than one tier rule per tier.</span></span> <span data-ttu-id="b3194-132">たとえば、層を取得するためには、1 か月で 500 ドルの金額を購入している、1 年間で 1,000 ドルの金額を購入している、1 年間に 20 のトランザクションがあるという 3 つの異なる基準があるとします。</span><span class="sxs-lookup"><span data-stu-id="b3194-132">For example, you could have three different criteria to earn a tier; by spending $500 in one month, by spending $1000 over one year, and by having 20 transactions in one year.</span></span> <span data-ttu-id="b3194-133">そのためには、3 つの層ルールを作成する必要があります。</span><span class="sxs-lookup"><span data-stu-id="b3194-133">To do this, you would need to create three tier rules.</span></span>  
21. <span data-ttu-id="b3194-134">[報酬ポイント] フィールドで、ドロップ ダウン ボタンをクリックし、ルックアップを開きます。</span><span class="sxs-lookup"><span data-stu-id="b3194-134">In the Reward point field, click the drop-down button to open the lookup.</span></span>
    * <span data-ttu-id="b3194-135">これは、償還不可能なロイヤルティ報酬ポイントであることが必要です。</span><span class="sxs-lookup"><span data-stu-id="b3194-135">This should be a non-redeemable loyalty reward point.</span></span>  
22. <span data-ttu-id="b3194-136">一覧で、選択された行のリンクをクリックします。</span><span class="sxs-lookup"><span data-stu-id="b3194-136">In the list, click the link in the selected row.</span></span>
23. <span data-ttu-id="b3194-137">[発行済み最小ポイント] フィールドに数値を入力します。</span><span class="sxs-lookup"><span data-stu-id="b3194-137">In the Minimum issued points field, enter a number.</span></span>
    * <span data-ttu-id="b3194-138">最下位レベル層の場合、すべての顧客がプログラムに参加するだけで利用できるようにするには、「0」を入力します。</span><span class="sxs-lookup"><span data-stu-id="b3194-138">For the lowest level tier, if all customers qualify simply by participating in the program, enter '0'.</span></span>  
24. <span data-ttu-id="b3194-139">[日付範囲の評価] フィールドで、ドロップ ダウン ボタンをクリックし、ルックアップを開きます。</span><span class="sxs-lookup"><span data-stu-id="b3194-139">In the Evaluation date interval field, click the drop-down button to open the lookup.</span></span>
    * <span data-ttu-id="b3194-140">この日付範囲は、過去に遡る必要があります。</span><span class="sxs-lookup"><span data-stu-id="b3194-140">This date interval should extend into the past.</span></span> <span data-ttu-id="b3194-141">この日付期間中に取得したポイントのみ、発行済み最小ポイントの値にカウントされます。</span><span class="sxs-lookup"><span data-stu-id="b3194-141">Only points earned during this date interval will be counted towards reaching the minimum issued points value.</span></span>  
25. <span data-ttu-id="b3194-142">一覧で、選択された行のリンクをクリックします。</span><span class="sxs-lookup"><span data-stu-id="b3194-142">In the list, click the link in the selected row.</span></span>
26. <span data-ttu-id="b3194-143">[保存] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="b3194-143">Click Save.</span></span>
27. <span data-ttu-id="b3194-144">一覧で、目的のレコードを見つけ、選択します。</span><span class="sxs-lookup"><span data-stu-id="b3194-144">In the list, find and select the desired record.</span></span>
28. <span data-ttu-id="b3194-145">[新規] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="b3194-145">Click New.</span></span>
29. <span data-ttu-id="b3194-146">[報酬ポイント] フィールドで、ドロップ ダウン ボタンをクリックし、ルックアップを開きます。</span><span class="sxs-lookup"><span data-stu-id="b3194-146">In the Reward point field, click the drop-down button to open the lookup.</span></span>
30. <span data-ttu-id="b3194-147">一覧で、選択された行のリンクをクリックします。</span><span class="sxs-lookup"><span data-stu-id="b3194-147">In the list, click the link in the selected row.</span></span>
31. <span data-ttu-id="b3194-148">[発行済み最小ポイント] フィールドに数値を入力します。</span><span class="sxs-lookup"><span data-stu-id="b3194-148">In the Minimum issued points field, enter a number.</span></span>
32. <span data-ttu-id="b3194-149">[日付範囲の評価] フィールドで、ドロップ ダウン ボタンをクリックし、ルックアップを開きます。</span><span class="sxs-lookup"><span data-stu-id="b3194-149">In the Evaluation date interval field, click the drop-down button to open the lookup.</span></span>
    * <span data-ttu-id="b3194-150">この日付範囲は、過去に遡る必要があります。</span><span class="sxs-lookup"><span data-stu-id="b3194-150">This date interval should extend into the past.</span></span>  
33. <span data-ttu-id="b3194-151">一覧で、選択された行のリンクをクリックします。</span><span class="sxs-lookup"><span data-stu-id="b3194-151">In the list, click the link in the selected row.</span></span>
34. <span data-ttu-id="b3194-152">[保存] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="b3194-152">Click Save.</span></span>
35. <span data-ttu-id="b3194-153">[価格グループ] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="b3194-153">Click Price groups.</span></span>
    * <span data-ttu-id="b3194-154">ロイヤルティ顧客に割引を表示します。</span><span class="sxs-lookup"><span data-stu-id="b3194-154">If you want to give loyalty customers discounts.</span></span> <span data-ttu-id="b3194-155">1 つ以上の価格グループをロイヤルティ プログラムに割り当て、割引に価格グループを割り当てる必要があります。</span><span class="sxs-lookup"><span data-stu-id="b3194-155">you'll need to assign one or more price groups to the loyalty program and assign the price groups to discounts.</span></span> <span data-ttu-id="b3194-156">ベスト プラクティスは、さまざまな割引エンティティ タイプの間で価格グループを混用しないことです。</span><span class="sxs-lookup"><span data-stu-id="b3194-156">It is a best practise to not mix price groups across different types of discounting entities.</span></span>  <span data-ttu-id="b3194-157">たとえば、ロイヤルティの割引およびチャネル割引に対して同じ価格グループを使用しないでください。</span><span class="sxs-lookup"><span data-stu-id="b3194-157">For example, don't use the same price group for a loyalty discount and a channel discount.</span></span>  
36. <span data-ttu-id="b3194-158">[価格グループ] フィールドで、ドロップ ダウン ボタンをクリックし、ルックアップを開きます。</span><span class="sxs-lookup"><span data-stu-id="b3194-158">In the Price group field, click the drop-down button to open the lookup.</span></span>
    * <span data-ttu-id="b3194-159">ページ上部にある価格グループのリンクはロイヤルティ プログラムのためのものです。</span><span class="sxs-lookup"><span data-stu-id="b3194-159">The Price groups link at the top of the page is for the loyalty program.</span></span> <span data-ttu-id="b3194-160">プログラム層クイック タブの価格グループのリンクは特定のロイヤルティ層専用です。</span><span class="sxs-lookup"><span data-stu-id="b3194-160">The Price groups link in the Program tiers fasttab is for a specific loyalty tier only.</span></span>  
37. <span data-ttu-id="b3194-161">一覧で、選択された行のリンクをクリックします。</span><span class="sxs-lookup"><span data-stu-id="b3194-161">In the list, click the link in the selected row.</span></span>
38. <span data-ttu-id="b3194-162">[保存] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="b3194-162">Click Save.</span></span>
39. <span data-ttu-id="b3194-163">ページを閉じます。</span><span class="sxs-lookup"><span data-stu-id="b3194-163">Close the page.</span></span>
40. <span data-ttu-id="b3194-164">[保存] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="b3194-164">Click Save.</span></span>


