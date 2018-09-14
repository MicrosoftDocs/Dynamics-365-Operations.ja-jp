--- 
title: "販売見積の一括作成"
description: "この手順は、複数の顧客に送付する、一連の製品またはサービスの提供の見積書を効率的に作成する方法を示します。"
author: omulvad
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: SalesQuotationTemplateGroup, SalesQuotationListPage, SalesCreateQuotation, SalesQuotationTable, SysQueryForm
audience: Application User
ms.reviewer: kfend
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: omulvad
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 0312b8cfadd45f8e59225e9daba78b9e216cff51
ms.openlocfilehash: e0e9ddf38106fce3ed6a6f908826f2196c97a45a
ms.contentlocale: ja-jp
ms.lasthandoff: 09/14/2018

---
# <a name="mass-create-sales-quotations"></a><span data-ttu-id="166f3-103">販売見積の一括作成</span><span class="sxs-lookup"><span data-stu-id="166f3-103">Mass create sales quotations</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="166f3-104">この手順は、複数の顧客に送付する、一連の製品またはサービスの提供の見積書を効率的に作成する方法を示します。</span><span class="sxs-lookup"><span data-stu-id="166f3-104">This procedure demonstrates how to efficiently create quotations offering a set of products or services that are to be sent to multiple customers.</span></span> <span data-ttu-id="166f3-105">この一括見積作成は、見積テンプレートに基づきます。</span><span class="sxs-lookup"><span data-stu-id="166f3-105">This mass quotation creation is based on quotation templates.</span></span> <span data-ttu-id="166f3-106">この手順は、独自のデータで、またはデモ データの会社 USMF のデータで実行できます。</span><span class="sxs-lookup"><span data-stu-id="166f3-106">You can run this procedure on your own data or in demo data company USMF.</span></span>


## <a name="create-a-quotation-template"></a><span data-ttu-id="166f3-107">見積テンプレートの作成</span><span class="sxs-lookup"><span data-stu-id="166f3-107">Create a quotation template</span></span>
1. <span data-ttu-id="166f3-108">[販売とマーケティング] > [設定] > [見積] > [テンプレート グループ] に移動する。</span><span class="sxs-lookup"><span data-stu-id="166f3-108">Go to Sales and marketing > Setup > Quotations > Template groups.</span></span>
2. <span data-ttu-id="166f3-109">[新規] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="166f3-109">Click New.</span></span>
3. <span data-ttu-id="166f3-110">[グループ ID] フィールドで、選択した ID を入力します。</span><span class="sxs-lookup"><span data-stu-id="166f3-110">In the Group ID field, type an ID of your choice.</span></span>
4. <span data-ttu-id="166f3-111">[説明] フィールドに値を入力します。</span><span class="sxs-lookup"><span data-stu-id="166f3-111">In the Description field, type a value.</span></span>
5. <span data-ttu-id="166f3-112">[保存] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="166f3-112">Click Save.</span></span>
6. <span data-ttu-id="166f3-113">ページを閉じます。</span><span class="sxs-lookup"><span data-stu-id="166f3-113">Close the page.</span></span>
7. <span data-ttu-id="166f3-114">[販売とマーケティング] > [販売見積] > [すべての見積] に移動する。</span><span class="sxs-lookup"><span data-stu-id="166f3-114">Go to Sales and marketing > Sales quotations > All quotations.</span></span>
8. <span data-ttu-id="166f3-115">[新規] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="166f3-115">Click New.</span></span>
9. <span data-ttu-id="166f3-116">[勘定タイプ] フィールドで、「顧客」を選択します。</span><span class="sxs-lookup"><span data-stu-id="166f3-116">In the Account type field, select 'Customer'.</span></span>
10. <span data-ttu-id="166f3-117">[顧客口座] フィールドで値を入力または選択します。</span><span class="sxs-lookup"><span data-stu-id="166f3-117">In the Customer account field, enter or select a value.</span></span>
11. <span data-ttu-id="166f3-118">[OK] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="166f3-118">Click OK.</span></span>
    * <span data-ttu-id="166f3-119">見積書をテンプレートにするには、見積ヘッダーの設定手順を実行する必要があります。</span><span class="sxs-lookup"><span data-stu-id="166f3-119">For a quotation to become a template you must carry out  setup steps on the quotation header.</span></span> <span data-ttu-id="166f3-120">これは、見積に明細行を追加する前にする必要があります。</span><span class="sxs-lookup"><span data-stu-id="166f3-120">This must be done before you add lines to the quotation.</span></span>   
12. <span data-ttu-id="166f3-121">[アクション] ウィンドウで、[オプション] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="166f3-121">On the Action Pane, click Options.</span></span>
13. <span data-ttu-id="166f3-122">[ビューの変更] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="166f3-122">Click Change view.</span></span>
14. <span data-ttu-id="166f3-123">[ヘッダーの表示] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="166f3-123">Click Header view.</span></span>
15. <span data-ttu-id="166f3-124">[設定] セクションを展開します。</span><span class="sxs-lookup"><span data-stu-id="166f3-124">Expand the Setup section.</span></span>
16. <span data-ttu-id="166f3-125">[グループ ID] フィールドで、値を入力または選択します。</span><span class="sxs-lookup"><span data-stu-id="166f3-125">In the Group ID field, enter or select a value.</span></span>
17. <span data-ttu-id="166f3-126">[テンプレート名] フィールドに値を入力します。</span><span class="sxs-lookup"><span data-stu-id="166f3-126">In the Template name field, type a value.</span></span>
18. <span data-ttu-id="166f3-127">[アクティブ] フィールドで、[はい] を選択します。</span><span class="sxs-lookup"><span data-stu-id="166f3-127">Select Yes in the Active field.</span></span>
    * <span data-ttu-id="166f3-128">新しい販売見積にテンプレートを適用する場合、有効なテンプレートのみ使用できます。</span><span class="sxs-lookup"><span data-stu-id="166f3-128">Only active templates can be used when you apply a template to a new sales quotation.</span></span>  
19. <span data-ttu-id="166f3-129">[アクション] ウィンドウで、[オプション] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="166f3-129">On the Action Pane, click Options.</span></span>
20. <span data-ttu-id="166f3-130">[ビューの変更] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="166f3-130">Click Change view.</span></span>
21. <span data-ttu-id="166f3-131">[明細行の表示] ] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="166f3-131">Click Line view.</span></span>
22. <span data-ttu-id="166f3-132">[品目] フィールドで、値を入力または選択します。</span><span class="sxs-lookup"><span data-stu-id="166f3-132">In the Item field, enter or select a value.</span></span>
23. <span data-ttu-id="166f3-133">[品目] フィールドに値を入力します。</span><span class="sxs-lookup"><span data-stu-id="166f3-133">In the Item field, type a value.</span></span>
24. <span data-ttu-id="166f3-134">ページを閉じます。</span><span class="sxs-lookup"><span data-stu-id="166f3-134">Close the page.</span></span>
25. <span data-ttu-id="166f3-135">[割引率] フィールドに数値を入力します。</span><span class="sxs-lookup"><span data-stu-id="166f3-135">In the Discount percent field, enter a number.</span></span>
26. <span data-ttu-id="166f3-136">[行の追加] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="166f3-136">Click Add line.</span></span>
27. <span data-ttu-id="166f3-137">[品目] フィールドで、値を入力または選択します。</span><span class="sxs-lookup"><span data-stu-id="166f3-137">In the Item field, enter or select a value.</span></span>
28. <span data-ttu-id="166f3-138">[品目] フィールドに値を入力します。</span><span class="sxs-lookup"><span data-stu-id="166f3-138">In the Item field, type a value.</span></span>
29. <span data-ttu-id="166f3-139">ページを閉じます。</span><span class="sxs-lookup"><span data-stu-id="166f3-139">Close the page.</span></span>
30. <span data-ttu-id="166f3-140">[単価] フィールドで、新しい価格を入力するか、または現在の価格を変更します。</span><span class="sxs-lookup"><span data-stu-id="166f3-140">In the Unit price field, enter a new price or change the current one.</span></span>
31. <span data-ttu-id="166f3-141">[行の追加] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="166f3-141">Click Add line.</span></span>
32. <span data-ttu-id="166f3-142">[品目] フィールドで、値を入力または選択します。</span><span class="sxs-lookup"><span data-stu-id="166f3-142">In the Item field, enter or select a value.</span></span>
33. <span data-ttu-id="166f3-143">[品目] フィールドに値を入力します。</span><span class="sxs-lookup"><span data-stu-id="166f3-143">In the Item field, type a value.</span></span>
34. <span data-ttu-id="166f3-144">ページを閉じます。</span><span class="sxs-lookup"><span data-stu-id="166f3-144">Close the page.</span></span>
35. <span data-ttu-id="166f3-145">[数量] フィールドに数値を入力します。</span><span class="sxs-lookup"><span data-stu-id="166f3-145">In the Quantity field, enter a number.</span></span>
36. <span data-ttu-id="166f3-146">[割引] フィールドに数値を入力します。</span><span class="sxs-lookup"><span data-stu-id="166f3-146">In the Discount field, enter a number.</span></span>
37. <span data-ttu-id="166f3-147">[保存] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="166f3-147">Click Save.</span></span>

## <a name="apply-the-template-to-create-a-single-quotation"></a><span data-ttu-id="166f3-148">単一の見積を作成する場合、テンプレートを適用します。</span><span class="sxs-lookup"><span data-stu-id="166f3-148">Apply the template to create a single quotation</span></span>
1. <span data-ttu-id="166f3-149">[販売とマーケティング] > [販売見積] > [すべての見積] に移動する。</span><span class="sxs-lookup"><span data-stu-id="166f3-149">Go to Sales and marketing > Sales quotations > All quotations.</span></span>
    * <span data-ttu-id="166f3-150">作成した見積がテンプレートとしてマークされていることに注意してください。</span><span class="sxs-lookup"><span data-stu-id="166f3-150">Note that the quotation you have just created is marked as template.</span></span>  
2. <span data-ttu-id="166f3-151">[新規] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="166f3-151">Click New.</span></span>
3. <span data-ttu-id="166f3-152">[勘定タイプ] フィールドで、「顧客」を選択します。</span><span class="sxs-lookup"><span data-stu-id="166f3-152">In the Account type field, select 'Customer'.</span></span>
4. <span data-ttu-id="166f3-153">[顧客口座] フィールドで値を入力または選択します。</span><span class="sxs-lookup"><span data-stu-id="166f3-153">In the Customer account field, enter or select a value.</span></span>
5. <span data-ttu-id="166f3-154">[テンプレート] セクションを展開します。</span><span class="sxs-lookup"><span data-stu-id="166f3-154">Expand the Template section.</span></span>
6. <span data-ttu-id="166f3-155">[グループ ID] フィールドで、値を入力または選択します。</span><span class="sxs-lookup"><span data-stu-id="166f3-155">In the Group ID field, enter or select a value.</span></span>
7. <span data-ttu-id="166f3-156">[テンプレート名] フィールドで、値を入力または選択します。</span><span class="sxs-lookup"><span data-stu-id="166f3-156">In the Template name field, enter or select a value.</span></span>
8. <span data-ttu-id="166f3-157">[計算方法] フィールドで、「テンプレート値に基づく」を選択します。</span><span class="sxs-lookup"><span data-stu-id="166f3-157">In the Calculation method field, select 'Based on template values'.</span></span>
9. <span data-ttu-id="166f3-158">[OK] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="166f3-158">Click OK.</span></span>
    * <span data-ttu-id="166f3-159">新しい見積書は、テンプレートのデータと条件に基づいて、作成されています。</span><span class="sxs-lookup"><span data-stu-id="166f3-159">The new quotation has now been created, based on the data and terms of the template.</span></span>  
10. <span data-ttu-id="166f3-160">ページを閉じます。</span><span class="sxs-lookup"><span data-stu-id="166f3-160">Close the page.</span></span>
11. <span data-ttu-id="166f3-161">ページを閉じます。</span><span class="sxs-lookup"><span data-stu-id="166f3-161">Close the page.</span></span>

## <a name="apply-the-template-to-mass-create-quotations"></a><span data-ttu-id="166f3-162">一括で見積書を作成するため、テンプレートを適用します。</span><span class="sxs-lookup"><span data-stu-id="166f3-162">Apply the template to mass create quotations</span></span>
1. <span data-ttu-id="166f3-163">[販売とマーケティング] > [販売見積] > [見積の更新] > [見積の一括作成] に移動します。</span><span class="sxs-lookup"><span data-stu-id="166f3-163">Go to Sales and marketing > Sales quotations > Quotation update > Mass create quotations.</span></span>
2. <span data-ttu-id="166f3-164">[勘定タイプ] フィールドで、「顧客」を選択します。</span><span class="sxs-lookup"><span data-stu-id="166f3-164">In the Account type field, select 'Customer'.</span></span>
3. <span data-ttu-id="166f3-165">[グループ ID] フィールドで、値を入力または選択します。</span><span class="sxs-lookup"><span data-stu-id="166f3-165">In the Group ID field, enter or select a value.</span></span>
4. <span data-ttu-id="166f3-166">[テンプレート名] フィールドで、値を入力または選択します。</span><span class="sxs-lookup"><span data-stu-id="166f3-166">In the Template name field, enter or select a value.</span></span>
5. <span data-ttu-id="166f3-167">[計算方法] フィールドで、「テンプレート値に基づく」を選択します。</span><span class="sxs-lookup"><span data-stu-id="166f3-167">In the Calculation method field, select 'Based on template values'.</span></span>
6. <span data-ttu-id="166f3-168">[対象に含めるレコード] セクションを展開します。</span><span class="sxs-lookup"><span data-stu-id="166f3-168">Expand the Records to include section.</span></span>
7. <span data-ttu-id="166f3-169">[フィルター] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="166f3-169">Click Filter.</span></span>
8. <span data-ttu-id="166f3-170">[基準] フィールドでは、この一括見積作成に含める顧客の範囲をカバーするためのフィルターを設定します。</span><span class="sxs-lookup"><span data-stu-id="166f3-170">In the Criteria field, set the filter to cover a range of customers you want to include in this mass quotation creation.</span></span> <span data-ttu-id="166f3-171">次の形式「Customer1..CustomerN」を使用します。</span><span class="sxs-lookup"><span data-stu-id="166f3-171">Use the following format "Customer1..CustomerN.</span></span>
    * <span data-ttu-id="166f3-172">たとえば、フィルタを US-001. .US-004 に設定できます。</span><span class="sxs-lookup"><span data-stu-id="166f3-172">For example, you could set the filter to: US-001..US-004</span></span>  
9. <span data-ttu-id="166f3-173">[OK] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="166f3-173">Click OK.</span></span>
10. <span data-ttu-id="166f3-174">[OK] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="166f3-174">Click OK.</span></span>
11. <span data-ttu-id="166f3-175">[販売とマーケティング] > [販売見積] > [すべての見積] に移動する。</span><span class="sxs-lookup"><span data-stu-id="166f3-175">Go to Sales and marketing > Sales quotations > All quotations.</span></span>
    * <span data-ttu-id="166f3-176">選択したテンプレートに基づいて一括定期更新で指定されたすべての顧客に対して見積書が作成されたことを確認します。</span><span class="sxs-lookup"><span data-stu-id="166f3-176">Verify that quotations have been created for all the customers specified in the mass update routine, as based on the selected template.</span></span>  


