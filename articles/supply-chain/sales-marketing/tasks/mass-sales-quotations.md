---
title: 販売見積の一括作成
description: この手順は、複数の顧客に送付する、一連の製品またはサービスの提供の見積書を効率的に作成する方法を示します。
author: omulvad
manager: tfehr
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: SalesQuotationTemplateGroup, SalesQuotationListPage, SalesCreateQuotation, SalesQuotationTable, SysQueryForm, SalesQuickQuote
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: kamaybac
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: f7aaa4e1fee12092be0389f0641e64712e869e6a
ms.sourcegitcommit: eaf330dbee1db96c20d5ac479f007747bea079eb
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 02/15/2021
ms.locfileid: "5260362"
---
# <a name="mass-create-sales-quotations"></a><span data-ttu-id="27645-103">販売見積の一括作成</span><span class="sxs-lookup"><span data-stu-id="27645-103">Mass create sales quotations</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="27645-104">この手順は、複数の顧客に送付する、一連の製品またはサービスの提供の見積書を効率的に作成する方法を示します。</span><span class="sxs-lookup"><span data-stu-id="27645-104">This procedure demonstrates how to efficiently create quotations offering a set of products or services that are to be sent to multiple customers.</span></span> <span data-ttu-id="27645-105">この一括見積作成は、見積テンプレートに基づきます。</span><span class="sxs-lookup"><span data-stu-id="27645-105">This mass quotation creation is based on quotation templates.</span></span> <span data-ttu-id="27645-106">この手順は、独自のデータで、またはデモ データの会社 USMF のデータで実行できます。</span><span class="sxs-lookup"><span data-stu-id="27645-106">You can run this procedure on your own data or in demo data company USMF.</span></span>


## <a name="create-a-quotation-template"></a><span data-ttu-id="27645-107">見積テンプレートの作成</span><span class="sxs-lookup"><span data-stu-id="27645-107">Create a quotation template</span></span>
1. <span data-ttu-id="27645-108">[販売とマーケティング] > [設定] > [見積] > [テンプレート グループ] に移動する。</span><span class="sxs-lookup"><span data-stu-id="27645-108">Go to Sales and marketing > Setup > Quotations > Template groups.</span></span>
2. <span data-ttu-id="27645-109">[新規] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="27645-109">Click New.</span></span>
3. <span data-ttu-id="27645-110">[グループ ID] フィールドで、選択した ID を入力します。</span><span class="sxs-lookup"><span data-stu-id="27645-110">In the Group ID field, type an ID of your choice.</span></span>
4. <span data-ttu-id="27645-111">[説明] フィールドに値を入力します。</span><span class="sxs-lookup"><span data-stu-id="27645-111">In the Description field, type a value.</span></span>
5. <span data-ttu-id="27645-112">[保存] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="27645-112">Click Save.</span></span>
6. <span data-ttu-id="27645-113">ページを閉じます。</span><span class="sxs-lookup"><span data-stu-id="27645-113">Close the page.</span></span>
7. <span data-ttu-id="27645-114">[販売とマーケティング] > [販売見積] > [すべての見積] に移動する。</span><span class="sxs-lookup"><span data-stu-id="27645-114">Go to Sales and marketing > Sales quotations > All quotations.</span></span>
8. <span data-ttu-id="27645-115">[新規] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="27645-115">Click New.</span></span>
9. <span data-ttu-id="27645-116">[勘定タイプ] フィールドで、「顧客」を選択します。</span><span class="sxs-lookup"><span data-stu-id="27645-116">In the Account type field, select 'Customer'.</span></span>
10. <span data-ttu-id="27645-117">[顧客口座] フィールドで値を入力または選択します。</span><span class="sxs-lookup"><span data-stu-id="27645-117">In the Customer account field, enter or select a value.</span></span>
11. <span data-ttu-id="27645-118">[OK] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="27645-118">Click OK.</span></span>
    * <span data-ttu-id="27645-119">見積書をテンプレートにするには、見積ヘッダーの設定手順を実行する必要があります。</span><span class="sxs-lookup"><span data-stu-id="27645-119">For a quotation to become a template you must carry out  setup steps on the quotation header.</span></span> <span data-ttu-id="27645-120">これは、見積に明細行を追加する前にする必要があります。</span><span class="sxs-lookup"><span data-stu-id="27645-120">This must be done before you add lines to the quotation.</span></span>   
12. <span data-ttu-id="27645-121">[アクション] ウィンドウで、[オプション] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="27645-121">On the Action Pane, click Options.</span></span>
13. <span data-ttu-id="27645-122">[ビューの変更] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="27645-122">Click Change view.</span></span>
14. <span data-ttu-id="27645-123">[ヘッダーの表示] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="27645-123">Click Header view.</span></span>
15. <span data-ttu-id="27645-124">[設定] セクションを展開します。</span><span class="sxs-lookup"><span data-stu-id="27645-124">Expand the Setup section.</span></span>
16. <span data-ttu-id="27645-125">[グループ ID] フィールドで、値を入力または選択します。</span><span class="sxs-lookup"><span data-stu-id="27645-125">In the Group ID field, enter or select a value.</span></span>
17. <span data-ttu-id="27645-126">[テンプレート名] フィールドに値を入力します。</span><span class="sxs-lookup"><span data-stu-id="27645-126">In the Template name field, type a value.</span></span>
18. <span data-ttu-id="27645-127">[アクティブ] フィールドで、[はい] を選択します。</span><span class="sxs-lookup"><span data-stu-id="27645-127">Select Yes in the Active field.</span></span>
    * <span data-ttu-id="27645-128">新しい販売見積にテンプレートを適用する場合、有効なテンプレートのみ使用できます。</span><span class="sxs-lookup"><span data-stu-id="27645-128">Only active templates can be used when you apply a template to a new sales quotation.</span></span>  
19. <span data-ttu-id="27645-129">[アクション] ウィンドウで、[オプション] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="27645-129">On the Action Pane, click Options.</span></span>
20. <span data-ttu-id="27645-130">[ビューの変更] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="27645-130">Click Change view.</span></span>
21. <span data-ttu-id="27645-131">[明細行の表示] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="27645-131">Click Line view.</span></span>
22. <span data-ttu-id="27645-132">[品目] フィールドで、値を入力または選択します。</span><span class="sxs-lookup"><span data-stu-id="27645-132">In the Item field, enter or select a value.</span></span>
23. <span data-ttu-id="27645-133">[品目] フィールドに値を入力します。</span><span class="sxs-lookup"><span data-stu-id="27645-133">In the Item field, type a value.</span></span>
24. <span data-ttu-id="27645-134">ページを閉じます。</span><span class="sxs-lookup"><span data-stu-id="27645-134">Close the page.</span></span>
25. <span data-ttu-id="27645-135">[割引率] フィールドに数値を入力します。</span><span class="sxs-lookup"><span data-stu-id="27645-135">In the Discount percent field, enter a number.</span></span>
26. <span data-ttu-id="27645-136">[行の追加] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="27645-136">Click Add line.</span></span>
27. <span data-ttu-id="27645-137">[品目] フィールドで、値を入力または選択します。</span><span class="sxs-lookup"><span data-stu-id="27645-137">In the Item field, enter or select a value.</span></span>
28. <span data-ttu-id="27645-138">[品目] フィールドに値を入力します。</span><span class="sxs-lookup"><span data-stu-id="27645-138">In the Item field, type a value.</span></span>
29. <span data-ttu-id="27645-139">ページを閉じます。</span><span class="sxs-lookup"><span data-stu-id="27645-139">Close the page.</span></span>
30. <span data-ttu-id="27645-140">[単価] フィールドで、新しい価格を入力するか、または現在の価格を変更します。</span><span class="sxs-lookup"><span data-stu-id="27645-140">In the Unit price field, enter a new price or change the current one.</span></span>
31. <span data-ttu-id="27645-141">[行の追加] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="27645-141">Click Add line.</span></span>
32. <span data-ttu-id="27645-142">[品目] フィールドで、値を入力または選択します。</span><span class="sxs-lookup"><span data-stu-id="27645-142">In the Item field, enter or select a value.</span></span>
33. <span data-ttu-id="27645-143">[品目] フィールドに値を入力します。</span><span class="sxs-lookup"><span data-stu-id="27645-143">In the Item field, type a value.</span></span>
34. <span data-ttu-id="27645-144">ページを閉じます。</span><span class="sxs-lookup"><span data-stu-id="27645-144">Close the page.</span></span>
35. <span data-ttu-id="27645-145">[数量] フィールドに数値を入力します。</span><span class="sxs-lookup"><span data-stu-id="27645-145">In the Quantity field, enter a number.</span></span>
36. <span data-ttu-id="27645-146">[割引] フィールドに数値を入力します。</span><span class="sxs-lookup"><span data-stu-id="27645-146">In the Discount field, enter a number.</span></span>
37. <span data-ttu-id="27645-147">[保存] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="27645-147">Click Save.</span></span>

## <a name="apply-the-template-to-create-a-single-quotation"></a><span data-ttu-id="27645-148">単一の見積を作成する場合、テンプレートを適用します。</span><span class="sxs-lookup"><span data-stu-id="27645-148">Apply the template to create a single quotation</span></span>
1. <span data-ttu-id="27645-149">[販売とマーケティング] > [販売見積] > [すべての見積] に移動する。</span><span class="sxs-lookup"><span data-stu-id="27645-149">Go to Sales and marketing > Sales quotations > All quotations.</span></span>
    * <span data-ttu-id="27645-150">作成した見積がテンプレートとしてマークされていることに注意してください。</span><span class="sxs-lookup"><span data-stu-id="27645-150">Note that the quotation you have just created is marked as template.</span></span>  
2. <span data-ttu-id="27645-151">[新規] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="27645-151">Click New.</span></span>
3. <span data-ttu-id="27645-152">[勘定タイプ] フィールドで、「顧客」を選択します。</span><span class="sxs-lookup"><span data-stu-id="27645-152">In the Account type field, select 'Customer'.</span></span>
4. <span data-ttu-id="27645-153">[顧客口座] フィールドで値を入力または選択します。</span><span class="sxs-lookup"><span data-stu-id="27645-153">In the Customer account field, enter or select a value.</span></span>
5. <span data-ttu-id="27645-154">[テンプレート] セクションを展開します。</span><span class="sxs-lookup"><span data-stu-id="27645-154">Expand the Template section.</span></span>
6. <span data-ttu-id="27645-155">[グループ ID] フィールドで、値を入力または選択します。</span><span class="sxs-lookup"><span data-stu-id="27645-155">In the Group ID field, enter or select a value.</span></span>
7. <span data-ttu-id="27645-156">[テンプレート名] フィールドで、値を入力または選択します。</span><span class="sxs-lookup"><span data-stu-id="27645-156">In the Template name field, enter or select a value.</span></span>
8. <span data-ttu-id="27645-157">[計算方法] フィールドで、「テンプレート値に基づく」を選択します。</span><span class="sxs-lookup"><span data-stu-id="27645-157">In the Calculation method field, select 'Based on template values'.</span></span>
9. <span data-ttu-id="27645-158">[OK] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="27645-158">Click OK.</span></span>
    * <span data-ttu-id="27645-159">新しい見積書は、テンプレートのデータと条件に基づいて、作成されています。</span><span class="sxs-lookup"><span data-stu-id="27645-159">The new quotation has now been created, based on the data and terms of the template.</span></span>  
10. <span data-ttu-id="27645-160">ページを閉じます。</span><span class="sxs-lookup"><span data-stu-id="27645-160">Close the page.</span></span>
11. <span data-ttu-id="27645-161">ページを閉じます。</span><span class="sxs-lookup"><span data-stu-id="27645-161">Close the page.</span></span>

## <a name="apply-the-template-to-mass-create-quotations"></a><span data-ttu-id="27645-162">一括で見積書を作成するため、テンプレートを適用します。</span><span class="sxs-lookup"><span data-stu-id="27645-162">Apply the template to mass create quotations</span></span>
1. <span data-ttu-id="27645-163">[販売とマーケティング] > [販売見積] > [見積の更新] > [見積の一括作成] に移動します。</span><span class="sxs-lookup"><span data-stu-id="27645-163">Go to Sales and marketing > Sales quotations > Quotation update > Mass create quotations.</span></span>
2. <span data-ttu-id="27645-164">[勘定タイプ] フィールドで、「顧客」を選択します。</span><span class="sxs-lookup"><span data-stu-id="27645-164">In the Account type field, select 'Customer'.</span></span>
3. <span data-ttu-id="27645-165">[グループ ID] フィールドで、値を入力または選択します。</span><span class="sxs-lookup"><span data-stu-id="27645-165">In the Group ID field, enter or select a value.</span></span>
4. <span data-ttu-id="27645-166">[テンプレート名] フィールドで、値を入力または選択します。</span><span class="sxs-lookup"><span data-stu-id="27645-166">In the Template name field, enter or select a value.</span></span>
5. <span data-ttu-id="27645-167">[計算方法] フィールドで、「テンプレート値に基づく」を選択します。</span><span class="sxs-lookup"><span data-stu-id="27645-167">In the Calculation method field, select 'Based on template values'.</span></span>
6. <span data-ttu-id="27645-168">[対象に含めるレコード] セクションを展開します。</span><span class="sxs-lookup"><span data-stu-id="27645-168">Expand the Records to include section.</span></span>
7. <span data-ttu-id="27645-169">[フィルター] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="27645-169">Click Filter.</span></span>
8. <span data-ttu-id="27645-170">[基準] フィールドでは、この一括見積作成に含める顧客の範囲をカバーするためのフィルターを設定します。</span><span class="sxs-lookup"><span data-stu-id="27645-170">In the Criteria field, set the filter to cover a range of customers you want to include in this mass quotation creation.</span></span> <span data-ttu-id="27645-171">次の形式「Customer1..CustomerN」を使用します。</span><span class="sxs-lookup"><span data-stu-id="27645-171">Use the following format "Customer1..CustomerN.</span></span>
    * <span data-ttu-id="27645-172">たとえば、フィルタを US-001. .US-004 に設定できます。</span><span class="sxs-lookup"><span data-stu-id="27645-172">For example, you could set the filter to: US-001..US-004</span></span>  
9. <span data-ttu-id="27645-173">[OK] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="27645-173">Click OK.</span></span>
10. <span data-ttu-id="27645-174">[OK] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="27645-174">Click OK.</span></span>
11. <span data-ttu-id="27645-175">[販売とマーケティング] > [販売見積] > [すべての見積] に移動する。</span><span class="sxs-lookup"><span data-stu-id="27645-175">Go to Sales and marketing > Sales quotations > All quotations.</span></span>
    * <span data-ttu-id="27645-176">選択したテンプレートに基づいて一括定期更新で指定されたすべての顧客に対して見積書が作成されたことを確認します。</span><span class="sxs-lookup"><span data-stu-id="27645-176">Verify that quotations have been created for all the customers specified in the mass update routine, as based on the selected template.</span></span>  



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]