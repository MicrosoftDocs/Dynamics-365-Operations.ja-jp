--- 
title: "販売見積の一括作成"
description: "この手順は、複数の顧客に送付する、一連の製品またはサービスの提供の見積書を効率的に作成する方法を示します。"
author: omulvad
manager: AnnBe
ms.date: 11/10/2016
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: kfend
ms.search.scope: Operations
ms.search.region: Global
ms.author: omulvad
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 663da58ef01b705c0c984fbfd3fce8bc31be04c6
ms.openlocfilehash: 1fcb2c4d47f0c8e701be025e0554ed476693d732
ms.contentlocale: ja-jp
ms.lasthandoff: 08/29/2017

---
# <a name="mass-create-sales-quotations"></a><span data-ttu-id="200db-103">販売見積の一括作成</span><span class="sxs-lookup"><span data-stu-id="200db-103">Mass create sales quotations</span></span>

[!include[task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="200db-104">この手順は、複数の顧客に送付する、一連の製品またはサービスの提供の見積書を効率的に作成する方法を示します。</span><span class="sxs-lookup"><span data-stu-id="200db-104">This procedure demonstrates how to efficiently create quotations offering a set of products or services that are to be sent to multiple customers.</span></span> <span data-ttu-id="200db-105">この一括見積作成は、見積テンプレートに基づきます。</span><span class="sxs-lookup"><span data-stu-id="200db-105">This mass quotation creation is based on quotation templates.</span></span> <span data-ttu-id="200db-106">この手順は、独自のデータで、またはデモ データの会社 USMF のデータで実行できます。</span><span class="sxs-lookup"><span data-stu-id="200db-106">You can run this procedure on your own data or in demo data company USMF.</span></span>


## <a name="create-a-quotation-template"></a><span data-ttu-id="200db-107">見積テンプレートの作成</span><span class="sxs-lookup"><span data-stu-id="200db-107">Create a quotation template</span></span>
1. <span data-ttu-id="200db-108">[販売とマーケティング] > [設定] > [見積] > [テンプレート グループ] に移動する。</span><span class="sxs-lookup"><span data-stu-id="200db-108">Go to Sales and marketing > Setup > Quotations > Template groups.</span></span>
2. <span data-ttu-id="200db-109">[新規] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="200db-109">Click New.</span></span>
3. <span data-ttu-id="200db-110">[グループ ID] フィールドで、選択した ID を入力します。</span><span class="sxs-lookup"><span data-stu-id="200db-110">In the Group ID field, type an ID of your choice.</span></span>
4. <span data-ttu-id="200db-111">[説明] フィールドに値を入力します。</span><span class="sxs-lookup"><span data-stu-id="200db-111">In the Description field, type a value.</span></span>
5. <span data-ttu-id="200db-112">[保存] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="200db-112">Click Save.</span></span>
6. <span data-ttu-id="200db-113">ページを閉じます。</span><span class="sxs-lookup"><span data-stu-id="200db-113">Close the page.</span></span>
7. <span data-ttu-id="200db-114">[販売とマーケティング] > [販売見積] > [すべての見積] に移動する。</span><span class="sxs-lookup"><span data-stu-id="200db-114">Go to Sales and marketing > Sales quotations > All quotations.</span></span>
8. <span data-ttu-id="200db-115">[新規] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="200db-115">Click New.</span></span>
9. <span data-ttu-id="200db-116">[勘定タイプ] フィールドで、「顧客」を選択します。</span><span class="sxs-lookup"><span data-stu-id="200db-116">In the Account type field, select 'Customer'.</span></span>
10. <span data-ttu-id="200db-117">[顧客口座] フィールドで値を入力または選択します。</span><span class="sxs-lookup"><span data-stu-id="200db-117">In the Customer account field, enter or select a value.</span></span>
11. <span data-ttu-id="200db-118">[OK] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="200db-118">Click OK.</span></span>
    * <span data-ttu-id="200db-119">見積書をテンプレートにするには、見積ヘッダーの設定手順を実行する必要があります。</span><span class="sxs-lookup"><span data-stu-id="200db-119">For a quotation to become a template you must carry out  setup steps on the quotation header.</span></span> <span data-ttu-id="200db-120">これは、見積に明細行を追加する前にする必要があります。</span><span class="sxs-lookup"><span data-stu-id="200db-120">This must be done before you add lines to the quotation.</span></span>   
12. <span data-ttu-id="200db-121">[アクション] ウィンドウで、[オプション] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="200db-121">On the Action Pane, click Options.</span></span>
13. <span data-ttu-id="200db-122">[ビューの変更] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="200db-122">Click Change view.</span></span>
14. <span data-ttu-id="200db-123">[ヘッダーの表示] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="200db-123">Click Header view.</span></span>
15. <span data-ttu-id="200db-124">[設定] セクションを展開します。</span><span class="sxs-lookup"><span data-stu-id="200db-124">Expand the Setup section.</span></span>
16. <span data-ttu-id="200db-125">[グループ ID] フィールドで、値を入力または選択します。</span><span class="sxs-lookup"><span data-stu-id="200db-125">In the Group ID field, enter or select a value.</span></span>
17. <span data-ttu-id="200db-126">[テンプレート名] フィールドに値を入力します。</span><span class="sxs-lookup"><span data-stu-id="200db-126">In the Template name field, type a value.</span></span>
18. <span data-ttu-id="200db-127">[アクティブ] フィールドで、[はい] を選択します。</span><span class="sxs-lookup"><span data-stu-id="200db-127">Select Yes in the Active field.</span></span>
    * <span data-ttu-id="200db-128">新しい販売見積にテンプレートを適用する場合、有効なテンプレートのみ使用できます。</span><span class="sxs-lookup"><span data-stu-id="200db-128">Only active templates can be used when you apply a template to a new sales quotation.</span></span>  
19. <span data-ttu-id="200db-129">[アクション] ウィンドウで、[オプション] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="200db-129">On the Action Pane, click Options.</span></span>
20. <span data-ttu-id="200db-130">[ビューの変更] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="200db-130">Click Change view.</span></span>
21. <span data-ttu-id="200db-131">[明細行の表示] ] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="200db-131">Click Line view.</span></span>
22. <span data-ttu-id="200db-132">[品目] フィールドで、値を入力または選択します。</span><span class="sxs-lookup"><span data-stu-id="200db-132">In the Item field, enter or select a value.</span></span>
23. <span data-ttu-id="200db-133">[品目] フィールドに値を入力します。</span><span class="sxs-lookup"><span data-stu-id="200db-133">In the Item field, type a value.</span></span>
24. <span data-ttu-id="200db-134">ページを閉じます。</span><span class="sxs-lookup"><span data-stu-id="200db-134">Close the page.</span></span>
25. <span data-ttu-id="200db-135">[割引率] フィールドに数値を入力します。</span><span class="sxs-lookup"><span data-stu-id="200db-135">In the Discount percent field, enter a number.</span></span>
26. <span data-ttu-id="200db-136">[行の追加] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="200db-136">Click Add line.</span></span>
27. <span data-ttu-id="200db-137">[品目] フィールドで、値を入力または選択します。</span><span class="sxs-lookup"><span data-stu-id="200db-137">In the Item field, enter or select a value.</span></span>
28. <span data-ttu-id="200db-138">[品目] フィールドに値を入力します。</span><span class="sxs-lookup"><span data-stu-id="200db-138">In the Item field, type a value.</span></span>
29. <span data-ttu-id="200db-139">ページを閉じます。</span><span class="sxs-lookup"><span data-stu-id="200db-139">Close the page.</span></span>
30. <span data-ttu-id="200db-140">[単価] フィールドで、新しい価格を入力するか、または現在の価格を変更します。</span><span class="sxs-lookup"><span data-stu-id="200db-140">In the Unit price field, enter a new price or change the current one.</span></span>
31. <span data-ttu-id="200db-141">[行の追加] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="200db-141">Click Add line.</span></span>
32. <span data-ttu-id="200db-142">[品目] フィールドで、値を入力または選択します。</span><span class="sxs-lookup"><span data-stu-id="200db-142">In the Item field, enter or select a value.</span></span>
33. <span data-ttu-id="200db-143">[品目] フィールドに値を入力します。</span><span class="sxs-lookup"><span data-stu-id="200db-143">In the Item field, type a value.</span></span>
34. <span data-ttu-id="200db-144">ページを閉じます。</span><span class="sxs-lookup"><span data-stu-id="200db-144">Close the page.</span></span>
35. <span data-ttu-id="200db-145">[数量] フィールドに数値を入力します。</span><span class="sxs-lookup"><span data-stu-id="200db-145">In the Quantity field, enter a number.</span></span>
36. <span data-ttu-id="200db-146">[割引] フィールドに数値を入力します。</span><span class="sxs-lookup"><span data-stu-id="200db-146">In the Discount field, enter a number.</span></span>
37. <span data-ttu-id="200db-147">[保存] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="200db-147">Click Save.</span></span>

## <a name="apply-the-template-to-create-a-single-quotation"></a><span data-ttu-id="200db-148">単一の見積を作成する場合、テンプレートを適用します。</span><span class="sxs-lookup"><span data-stu-id="200db-148">Apply the template to create a single quotation</span></span>
1. <span data-ttu-id="200db-149">[販売とマーケティング] > [販売見積] > [すべての見積] に移動する。</span><span class="sxs-lookup"><span data-stu-id="200db-149">Go to Sales and marketing > Sales quotations > All quotations.</span></span>
    * <span data-ttu-id="200db-150">作成した見積がテンプレートとしてマークされていることに注意してください。</span><span class="sxs-lookup"><span data-stu-id="200db-150">Note that the quotation you have just created is marked as template.</span></span>  
2. <span data-ttu-id="200db-151">[新規] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="200db-151">Click New.</span></span>
3. <span data-ttu-id="200db-152">[勘定タイプ] フィールドで、「顧客」を選択します。</span><span class="sxs-lookup"><span data-stu-id="200db-152">In the Account type field, select 'Customer'.</span></span>
4. <span data-ttu-id="200db-153">[顧客口座] フィールドで値を入力または選択します。</span><span class="sxs-lookup"><span data-stu-id="200db-153">In the Customer account field, enter or select a value.</span></span>
5. <span data-ttu-id="200db-154">[テンプレート] セクションを展開します。</span><span class="sxs-lookup"><span data-stu-id="200db-154">Expand the Template section.</span></span>
6. <span data-ttu-id="200db-155">[グループ ID] フィールドで、値を入力または選択します。</span><span class="sxs-lookup"><span data-stu-id="200db-155">In the Group ID field, enter or select a value.</span></span>
7. <span data-ttu-id="200db-156">[テンプレート名] フィールドで、値を入力または選択します。</span><span class="sxs-lookup"><span data-stu-id="200db-156">In the Template name field, enter or select a value.</span></span>
8. <span data-ttu-id="200db-157">[計算方法] フィールドで、「テンプレート値に基づく」を選択します。</span><span class="sxs-lookup"><span data-stu-id="200db-157">In the Calculation method field, select 'Based on template values'.</span></span>
9. <span data-ttu-id="200db-158">[OK] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="200db-158">Click OK.</span></span>
    * <span data-ttu-id="200db-159">新しい見積書は、テンプレートのデータと条件に基づいて、作成されています。</span><span class="sxs-lookup"><span data-stu-id="200db-159">The new quotation has now been created, based on the data and terms of the template.</span></span>  
10. <span data-ttu-id="200db-160">ページを閉じます。</span><span class="sxs-lookup"><span data-stu-id="200db-160">Close the page.</span></span>
11. <span data-ttu-id="200db-161">ページを閉じます。</span><span class="sxs-lookup"><span data-stu-id="200db-161">Close the page.</span></span>

## <a name="apply-the-template-to-mass-create-quotations"></a><span data-ttu-id="200db-162">一括で見積書を作成するため、テンプレートを適用します。</span><span class="sxs-lookup"><span data-stu-id="200db-162">Apply the template to mass create quotations</span></span>
1. <span data-ttu-id="200db-163">[販売とマーケティング] > [販売見積] > [見積の更新] > [見積の一括作成] に移動します。</span><span class="sxs-lookup"><span data-stu-id="200db-163">Go to Sales and marketing > Sales quotations > Quotation update > Mass create quotations.</span></span>
2. <span data-ttu-id="200db-164">[勘定タイプ] フィールドで、「顧客」を選択します。</span><span class="sxs-lookup"><span data-stu-id="200db-164">In the Account type field, select 'Customer'.</span></span>
3. <span data-ttu-id="200db-165">[グループ ID] フィールドで、値を入力または選択します。</span><span class="sxs-lookup"><span data-stu-id="200db-165">In the Group ID field, enter or select a value.</span></span>
4. <span data-ttu-id="200db-166">[テンプレート名] フィールドで、値を入力または選択します。</span><span class="sxs-lookup"><span data-stu-id="200db-166">In the Template name field, enter or select a value.</span></span>
5. <span data-ttu-id="200db-167">[計算方法] フィールドで、「テンプレート値に基づく」を選択します。</span><span class="sxs-lookup"><span data-stu-id="200db-167">In the Calculation method field, select 'Based on template values'.</span></span>
6. <span data-ttu-id="200db-168">[対象に含めるレコード] セクションを展開します。</span><span class="sxs-lookup"><span data-stu-id="200db-168">Expand the Records to include section.</span></span>
7. <span data-ttu-id="200db-169">[フィルター] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="200db-169">Click Filter.</span></span>
8. <span data-ttu-id="200db-170">[基準] フィールドでは、この一括見積作成に含める顧客の範囲をカバーするためのフィルターを設定します。</span><span class="sxs-lookup"><span data-stu-id="200db-170">In the Criteria field, set the filter to cover a range of customers you want to include in this mass quotation creation.</span></span> <span data-ttu-id="200db-171">次の形式「Customer1..CustomerN」を使用します。</span><span class="sxs-lookup"><span data-stu-id="200db-171">Use the following format "Customer1..CustomerN.</span></span>
    * <span data-ttu-id="200db-172">たとえば、フィルタを US-001. .US-004 に設定できます。</span><span class="sxs-lookup"><span data-stu-id="200db-172">For example, you could set the filter to: US-001..US-004</span></span>  
9. <span data-ttu-id="200db-173">[OK] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="200db-173">Click OK.</span></span>
10. <span data-ttu-id="200db-174">[OK] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="200db-174">Click OK.</span></span>
11. <span data-ttu-id="200db-175">[販売とマーケティング] > [販売見積] > [すべての見積] に移動する。</span><span class="sxs-lookup"><span data-stu-id="200db-175">Go to Sales and marketing > Sales quotations > All quotations.</span></span>
    * <span data-ttu-id="200db-176">選択したテンプレートに基づいて一括定期更新で指定されたすべての顧客に対して見積書が作成されたことを確認します。</span><span class="sxs-lookup"><span data-stu-id="200db-176">Verify that quotations have been created for all the customers specified in the mass update routine, as based on the selected template.</span></span>  

