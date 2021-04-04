---
title: コンフィギュレーション済みの製品バリアントの製品番号の分類の作成
description: この手順では、コンフィギュレーション済製品バリアントにおける製品番号の分類を設定する方法、およびそれをコンフィギュレーション可能な製品マスターに関連付ける方法を示します。
author: ShylaThompson
manager: tfehr
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: DefaultDashboard, EcoResProductVariantMaintainWorkspace, EcoResNomenclature, EcoResProductListPage, EcoResProductDetails, PCProductConfigurationModelListPage, PCProductConfigurationModelDetails
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: kamaybac
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 07922a20d5c99640f32bb28ddddaffe846440667
ms.sourcegitcommit: eaf330dbee1db96c20d5ac479f007747bea079eb
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 02/15/2021
ms.locfileid: "5258878"
---
# <a name="create-a-product-number-nomenclature-for-configured-product-variants"></a><span data-ttu-id="500a3-103">コンフィギュレーション済みの製品バリアントの製品番号の分類の作成</span><span class="sxs-lookup"><span data-stu-id="500a3-103">Create a product number nomenclature for configured product variants</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="500a3-104">この手順では、コンフィギュレーション済製品バリアントにおける製品番号の分類を設定する方法、およびそれをコンフィギュレーション可能な製品マスターに関連付ける方法を示します。</span><span class="sxs-lookup"><span data-stu-id="500a3-104">This procedure shows you how to set up a product number nomenclature for configured product variants, and how it can be attached to a configurable product master.</span></span> <span data-ttu-id="500a3-105">この手順では、製品コンフィギュレーション モデル コンポーネントのコンフィギュレーションに関する用語をどのように作成するかを示します。</span><span class="sxs-lookup"><span data-stu-id="500a3-105">This procedure also demonstrates how you can build a configuration nomenclature for a product configuration model component.</span></span> <span data-ttu-id="500a3-106">この手順の作成に使用するデモ データの会社は USMF です。</span><span class="sxs-lookup"><span data-stu-id="500a3-106">The demo data company used to create this procedure is USMF.</span></span> <span data-ttu-id="500a3-107">新しい製品番号の分類は、「D0004」製品マスターに割り当てられます。</span><span class="sxs-lookup"><span data-stu-id="500a3-107">The new product number nomenclature is assigned to the D0004 product master.</span></span> <span data-ttu-id="500a3-108">このタスクは、通常、製品デザイナーが行います。</span><span class="sxs-lookup"><span data-stu-id="500a3-108">This task would typically be done by a product designer.</span></span>


## <a name="create-a-product-number-nomenclature"></a><span data-ttu-id="500a3-109">[製品番号の分類] を作成します。</span><span class="sxs-lookup"><span data-stu-id="500a3-109">Create a product number nomenclature</span></span>
1. <span data-ttu-id="500a3-110">[製品バリアント モデルの定義] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="500a3-110">Click Product variant model definition.</span></span>
2. <span data-ttu-id="500a3-111">[製品の分類] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="500a3-111">Click Product nomenclature.</span></span>
3. <span data-ttu-id="500a3-112">[新規] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="500a3-112">Click New.</span></span>
4. <span data-ttu-id="500a3-113">[名前] フィールドに値を入力します。</span><span class="sxs-lookup"><span data-stu-id="500a3-113">In the Name field, type a value.</span></span>
5. <span data-ttu-id="500a3-114">[説明] フィールドに値を入力します。</span><span class="sxs-lookup"><span data-stu-id="500a3-114">In the Description field, type a value.</span></span>
6. <span data-ttu-id="500a3-115">[追加] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="500a3-115">Click Add.</span></span>
7. <span data-ttu-id="500a3-116">[製品マスター番号] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="500a3-116">Click Product master number.</span></span>
8. <span data-ttu-id="500a3-117">[追加] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="500a3-117">Click Add.</span></span>
9. <span data-ttu-id="500a3-118">[テキスト定数] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="500a3-118">Click Text constant.</span></span>
10. <span data-ttu-id="500a3-119">一覧で、選択された行をマークします。</span><span class="sxs-lookup"><span data-stu-id="500a3-119">In the list, mark the selected row.</span></span>
11. <span data-ttu-id="500a3-120">[テキスト] フィールドに値を入力します。</span><span class="sxs-lookup"><span data-stu-id="500a3-120">In the Text field, type a value.</span></span>
12. <span data-ttu-id="500a3-121">[追加] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="500a3-121">Click Add.</span></span>
13. <span data-ttu-id="500a3-122">[コンフィギュレーション] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="500a3-122">Click Configuration.</span></span>
14. <span data-ttu-id="500a3-123">ページを閉じます。</span><span class="sxs-lookup"><span data-stu-id="500a3-123">Close the page.</span></span>

## <a name="assign-the-product-number-nomenclature-to-a-product-master"></a><span data-ttu-id="500a3-124">製品番号の分類を製品マスターに割り当てる</span><span class="sxs-lookup"><span data-stu-id="500a3-124">Assign the product number nomenclature to a product master</span></span>
1. <span data-ttu-id="500a3-125">[製品マスター] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="500a3-125">Click Product masters.</span></span>
2. <span data-ttu-id="500a3-126">クイック フィルターを使用して、レコードを見つけます。</span><span class="sxs-lookup"><span data-stu-id="500a3-126">Use the Quick Filter to find records.</span></span> <span data-ttu-id="500a3-127">たとえば、「D」という値を含む [製品番号] フィールドをフィルターします。</span><span class="sxs-lookup"><span data-stu-id="500a3-127">For example, filter on the Product number field with a value of 'D'.</span></span>
3. <span data-ttu-id="500a3-128">一覧で、選択された行のリンクをクリックします。</span><span class="sxs-lookup"><span data-stu-id="500a3-128">In the list, click the link in the selected row.</span></span>
4. <span data-ttu-id="500a3-129">[編集] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="500a3-129">Click Edit.</span></span>
5. <span data-ttu-id="500a3-130">[分類の使用] フィールドで、[はい] を選択します。</span><span class="sxs-lookup"><span data-stu-id="500a3-130">Select Yes in the Use nomenclature field.</span></span>
6. <span data-ttu-id="500a3-131">[製品バリアント番号の分類] フィールドに、値を入力または選択します。</span><span class="sxs-lookup"><span data-stu-id="500a3-131">In the Product variant number nomenclature field, enter or select a value.</span></span>
7. <span data-ttu-id="500a3-132">ページを閉じます。</span><span class="sxs-lookup"><span data-stu-id="500a3-132">Close the page.</span></span>
8. <span data-ttu-id="500a3-133">ページを閉じます。</span><span class="sxs-lookup"><span data-stu-id="500a3-133">Close the page.</span></span>

## <a name="create-nomenclature-for-a-product-configuration-model-component"></a><span data-ttu-id="500a3-134">製品コンフィギュレーション モデル コンポーネントの分類の作成</span><span class="sxs-lookup"><span data-stu-id="500a3-134">Create nomenclature for a product configuration model component</span></span>
1. <span data-ttu-id="500a3-135">[製品コンフィギュレーション モデル] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="500a3-135">Click Product configuration models.</span></span>
2. <span data-ttu-id="500a3-136">一覧で、目的のレコードを見つけ、選択します。</span><span class="sxs-lookup"><span data-stu-id="500a3-136">In the list, find and select the desired record.</span></span>
3. <span data-ttu-id="500a3-137">一覧で、選択された行のリンクをクリックします。</span><span class="sxs-lookup"><span data-stu-id="500a3-137">In the list, click the link in the selected row.</span></span>
4. <span data-ttu-id="500a3-138">[編集] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="500a3-138">Click Edit.</span></span>
5. <span data-ttu-id="500a3-139">[コンフィギュレーションの分類の使用] フィールドで、[はい] を選択します。</span><span class="sxs-lookup"><span data-stu-id="500a3-139">Select Yes in the Use configuration nomenclature field.</span></span>
6. <span data-ttu-id="500a3-140">[追加] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="500a3-140">Click Add.</span></span>
7. <span data-ttu-id="500a3-141">[属性値] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="500a3-141">Click Attribute value.</span></span>
8. <span data-ttu-id="500a3-142">一覧で、選択された行をマークします。</span><span class="sxs-lookup"><span data-stu-id="500a3-142">In the list, mark the selected row.</span></span>
9. <span data-ttu-id="500a3-143">[属性] フィールドに、値を入力または選択します。</span><span class="sxs-lookup"><span data-stu-id="500a3-143">In the Attribute field, enter or select a value.</span></span>
10. <span data-ttu-id="500a3-144">[追加] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="500a3-144">Click Add.</span></span>
11. <span data-ttu-id="500a3-145">[テキスト定数] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="500a3-145">Click Text constant.</span></span>
12. <span data-ttu-id="500a3-146">一覧で、選択された行をマークします。</span><span class="sxs-lookup"><span data-stu-id="500a3-146">In the list, mark the selected row.</span></span>
13. <span data-ttu-id="500a3-147">[テキスト] フィールドに値を入力します。</span><span class="sxs-lookup"><span data-stu-id="500a3-147">In the Text field, type a value.</span></span>
14. <span data-ttu-id="500a3-148">[追加] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="500a3-148">Click Add.</span></span>
15. <span data-ttu-id="500a3-149">[属性値] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="500a3-149">Click Attribute value.</span></span>
16. <span data-ttu-id="500a3-150">一覧で、選択された行をマークします。</span><span class="sxs-lookup"><span data-stu-id="500a3-150">In the list, mark the selected row.</span></span>
17. <span data-ttu-id="500a3-151">[属性] フィールドに、値を入力または選択します。</span><span class="sxs-lookup"><span data-stu-id="500a3-151">In the Attribute field, enter or select a value.</span></span>
18. <span data-ttu-id="500a3-152">[追加] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="500a3-152">Click Add.</span></span>
19. <span data-ttu-id="500a3-153">[テキスト定数] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="500a3-153">Click Text constant.</span></span>
20. <span data-ttu-id="500a3-154">一覧で、選択された行をマークします。</span><span class="sxs-lookup"><span data-stu-id="500a3-154">In the list, mark the selected row.</span></span>
21. <span data-ttu-id="500a3-155">[テキスト] フィールドに値を入力します。</span><span class="sxs-lookup"><span data-stu-id="500a3-155">In the Text field, type a value.</span></span>
22. <span data-ttu-id="500a3-156">[追加] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="500a3-156">Click Add.</span></span>
23. <span data-ttu-id="500a3-157">[属性値] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="500a3-157">Click Attribute value.</span></span>
24. <span data-ttu-id="500a3-158">一覧で、選択された行をマークします。</span><span class="sxs-lookup"><span data-stu-id="500a3-158">In the list, mark the selected row.</span></span>
25. <span data-ttu-id="500a3-159">[属性] フィールドに、値を入力または選択します。</span><span class="sxs-lookup"><span data-stu-id="500a3-159">In the Attribute field, enter or select a value.</span></span>
26. <span data-ttu-id="500a3-160">[追加] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="500a3-160">Click Add.</span></span>
27. <span data-ttu-id="500a3-161">[テキスト定数] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="500a3-161">Click Text constant.</span></span>
28. <span data-ttu-id="500a3-162">一覧で、選択された行をマークします。</span><span class="sxs-lookup"><span data-stu-id="500a3-162">In the list, mark the selected row.</span></span>
29. <span data-ttu-id="500a3-163">[テキスト] フィールドに値を入力します。</span><span class="sxs-lookup"><span data-stu-id="500a3-163">In the Text field, type a value.</span></span>
30. <span data-ttu-id="500a3-164">[追加] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="500a3-164">Click Add.</span></span>
31. <span data-ttu-id="500a3-165">[属性値] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="500a3-165">Click Attribute value.</span></span>
32. <span data-ttu-id="500a3-166">一覧で、選択された行をマークします。</span><span class="sxs-lookup"><span data-stu-id="500a3-166">In the list, mark the selected row.</span></span>
33. <span data-ttu-id="500a3-167">[属性] フィールドに、値を入力または選択します。</span><span class="sxs-lookup"><span data-stu-id="500a3-167">In the Attribute field, enter or select a value.</span></span>
34. <span data-ttu-id="500a3-168">[追加] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="500a3-168">Click Add.</span></span>
35. <span data-ttu-id="500a3-169">[テキスト定数] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="500a3-169">Click Text constant.</span></span>
36. <span data-ttu-id="500a3-170">一覧で、選択された行をマークします。</span><span class="sxs-lookup"><span data-stu-id="500a3-170">In the list, mark the selected row.</span></span>
37. <span data-ttu-id="500a3-171">[テキスト] フィールドに値を入力します。</span><span class="sxs-lookup"><span data-stu-id="500a3-171">In the Text field, type a value.</span></span>
38. <span data-ttu-id="500a3-172">[追加] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="500a3-172">Click Add.</span></span>
39. <span data-ttu-id="500a3-173">[番号順序値] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="500a3-173">Click Number sequence value.</span></span>
40. <span data-ttu-id="500a3-174">一覧で、選択された行をマークします。</span><span class="sxs-lookup"><span data-stu-id="500a3-174">In the list, mark the selected row.</span></span>
41. <span data-ttu-id="500a3-175">[番号順序] フィールドに、値を入力または選択します。</span><span class="sxs-lookup"><span data-stu-id="500a3-175">In the Number sequence field, enter or select a value.</span></span>
42. <span data-ttu-id="500a3-176">ページを閉じます。</span><span class="sxs-lookup"><span data-stu-id="500a3-176">Close the page.</span></span>
43. <span data-ttu-id="500a3-177">ページを閉じます。</span><span class="sxs-lookup"><span data-stu-id="500a3-177">Close the page.</span></span>
44. <span data-ttu-id="500a3-178">ページを閉じます。</span><span class="sxs-lookup"><span data-stu-id="500a3-178">Close the page.</span></span>



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]