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
ms.openlocfilehash: e52b7a5aff3e86e845484e1e84b4003cc4a52c95
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 01/15/2021
ms.locfileid: "4992373"
---
# <a name="create-a-product-number-nomenclature-for-configured-product-variants"></a><span data-ttu-id="731b9-103">コンフィギュレーション済みの製品バリアントの製品番号の分類の作成</span><span class="sxs-lookup"><span data-stu-id="731b9-103">Create a product number nomenclature for configured product variants</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="731b9-104">この手順では、コンフィギュレーション済製品バリアントにおける製品番号の分類を設定する方法、およびそれをコンフィギュレーション可能な製品マスターに関連付ける方法を示します。</span><span class="sxs-lookup"><span data-stu-id="731b9-104">This procedure shows you how to set up a product number nomenclature for configured product variants, and how it can be attached to a configurable product master.</span></span> <span data-ttu-id="731b9-105">この手順では、製品コンフィギュレーション モデル コンポーネントのコンフィギュレーションに関する用語をどのように作成するかを示します。</span><span class="sxs-lookup"><span data-stu-id="731b9-105">This procedure also demonstrates how you can build a configuration nomenclature for a product configuration model component.</span></span> <span data-ttu-id="731b9-106">この手順の作成に使用するデモ データの会社は USMF です。</span><span class="sxs-lookup"><span data-stu-id="731b9-106">The demo data company used to create this procedure is USMF.</span></span> <span data-ttu-id="731b9-107">新しい製品番号の分類は、「D0004」製品マスターに割り当てられます。</span><span class="sxs-lookup"><span data-stu-id="731b9-107">The new product number nomenclature is assigned to the D0004 product master.</span></span> <span data-ttu-id="731b9-108">このタスクは、通常、製品デザイナーが行います。</span><span class="sxs-lookup"><span data-stu-id="731b9-108">This task would typically be done by a product designer.</span></span>


## <a name="create-a-product-number-nomenclature"></a><span data-ttu-id="731b9-109">[製品番号の分類] を作成します。</span><span class="sxs-lookup"><span data-stu-id="731b9-109">Create a product number nomenclature</span></span>
1. <span data-ttu-id="731b9-110">[製品バリアント モデルの定義] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="731b9-110">Click Product variant model definition.</span></span>
2. <span data-ttu-id="731b9-111">[製品の分類] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="731b9-111">Click Product nomenclature.</span></span>
3. <span data-ttu-id="731b9-112">[新規] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="731b9-112">Click New.</span></span>
4. <span data-ttu-id="731b9-113">[名前] フィールドに値を入力します。</span><span class="sxs-lookup"><span data-stu-id="731b9-113">In the Name field, type a value.</span></span>
5. <span data-ttu-id="731b9-114">[説明] フィールドに値を入力します。</span><span class="sxs-lookup"><span data-stu-id="731b9-114">In the Description field, type a value.</span></span>
6. <span data-ttu-id="731b9-115">[追加] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="731b9-115">Click Add.</span></span>
7. <span data-ttu-id="731b9-116">[製品マスター番号] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="731b9-116">Click Product master number.</span></span>
8. <span data-ttu-id="731b9-117">[追加] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="731b9-117">Click Add.</span></span>
9. <span data-ttu-id="731b9-118">[テキスト定数] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="731b9-118">Click Text constant.</span></span>
10. <span data-ttu-id="731b9-119">一覧で、選択された行をマークします。</span><span class="sxs-lookup"><span data-stu-id="731b9-119">In the list, mark the selected row.</span></span>
11. <span data-ttu-id="731b9-120">[テキスト] フィールドに値を入力します。</span><span class="sxs-lookup"><span data-stu-id="731b9-120">In the Text field, type a value.</span></span>
12. <span data-ttu-id="731b9-121">[追加] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="731b9-121">Click Add.</span></span>
13. <span data-ttu-id="731b9-122">[コンフィギュレーション] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="731b9-122">Click Configuration.</span></span>
14. <span data-ttu-id="731b9-123">ページを閉じます。</span><span class="sxs-lookup"><span data-stu-id="731b9-123">Close the page.</span></span>

## <a name="assign-the-product-number-nomenclature-to-a-product-master"></a><span data-ttu-id="731b9-124">製品番号の分類を製品マスターに割り当てる</span><span class="sxs-lookup"><span data-stu-id="731b9-124">Assign the product number nomenclature to a product master</span></span>
1. <span data-ttu-id="731b9-125">[製品マスター] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="731b9-125">Click Product masters.</span></span>
2. <span data-ttu-id="731b9-126">クイック フィルターを使用して、レコードを見つけます。</span><span class="sxs-lookup"><span data-stu-id="731b9-126">Use the Quick Filter to find records.</span></span> <span data-ttu-id="731b9-127">たとえば、「D」という値を含む [製品番号] フィールドをフィルターします。</span><span class="sxs-lookup"><span data-stu-id="731b9-127">For example, filter on the Product number field with a value of 'D'.</span></span>
3. <span data-ttu-id="731b9-128">一覧で、選択された行のリンクをクリックします。</span><span class="sxs-lookup"><span data-stu-id="731b9-128">In the list, click the link in the selected row.</span></span>
4. <span data-ttu-id="731b9-129">[編集] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="731b9-129">Click Edit.</span></span>
5. <span data-ttu-id="731b9-130">[分類の使用] フィールドで、[はい] を選択します。</span><span class="sxs-lookup"><span data-stu-id="731b9-130">Select Yes in the Use nomenclature field.</span></span>
6. <span data-ttu-id="731b9-131">[製品バリアント番号の分類] フィールドに、値を入力または選択します。</span><span class="sxs-lookup"><span data-stu-id="731b9-131">In the Product variant number nomenclature field, enter or select a value.</span></span>
7. <span data-ttu-id="731b9-132">ページを閉じます。</span><span class="sxs-lookup"><span data-stu-id="731b9-132">Close the page.</span></span>
8. <span data-ttu-id="731b9-133">ページを閉じます。</span><span class="sxs-lookup"><span data-stu-id="731b9-133">Close the page.</span></span>

## <a name="create-nomenclature-for-a-product-configuration-model-component"></a><span data-ttu-id="731b9-134">製品コンフィギュレーション モデル コンポーネントの分類の作成</span><span class="sxs-lookup"><span data-stu-id="731b9-134">Create nomenclature for a product configuration model component</span></span>
1. <span data-ttu-id="731b9-135">[製品コンフィギュレーション モデル] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="731b9-135">Click Product configuration models.</span></span>
2. <span data-ttu-id="731b9-136">一覧で、目的のレコードを見つけ、選択します。</span><span class="sxs-lookup"><span data-stu-id="731b9-136">In the list, find and select the desired record.</span></span>
3. <span data-ttu-id="731b9-137">一覧で、選択された行のリンクをクリックします。</span><span class="sxs-lookup"><span data-stu-id="731b9-137">In the list, click the link in the selected row.</span></span>
4. <span data-ttu-id="731b9-138">[編集] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="731b9-138">Click Edit.</span></span>
5. <span data-ttu-id="731b9-139">[コンフィギュレーションの分類の使用] フィールドで、[はい] を選択します。</span><span class="sxs-lookup"><span data-stu-id="731b9-139">Select Yes in the Use configuration nomenclature field.</span></span>
6. <span data-ttu-id="731b9-140">[追加] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="731b9-140">Click Add.</span></span>
7. <span data-ttu-id="731b9-141">[属性値] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="731b9-141">Click Attribute value.</span></span>
8. <span data-ttu-id="731b9-142">一覧で、選択された行をマークします。</span><span class="sxs-lookup"><span data-stu-id="731b9-142">In the list, mark the selected row.</span></span>
9. <span data-ttu-id="731b9-143">[属性] フィールドに、値を入力または選択します。</span><span class="sxs-lookup"><span data-stu-id="731b9-143">In the Attribute field, enter or select a value.</span></span>
10. <span data-ttu-id="731b9-144">[追加] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="731b9-144">Click Add.</span></span>
11. <span data-ttu-id="731b9-145">[テキスト定数] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="731b9-145">Click Text constant.</span></span>
12. <span data-ttu-id="731b9-146">一覧で、選択された行をマークします。</span><span class="sxs-lookup"><span data-stu-id="731b9-146">In the list, mark the selected row.</span></span>
13. <span data-ttu-id="731b9-147">[テキスト] フィールドに値を入力します。</span><span class="sxs-lookup"><span data-stu-id="731b9-147">In the Text field, type a value.</span></span>
14. <span data-ttu-id="731b9-148">[追加] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="731b9-148">Click Add.</span></span>
15. <span data-ttu-id="731b9-149">[属性値] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="731b9-149">Click Attribute value.</span></span>
16. <span data-ttu-id="731b9-150">一覧で、選択された行をマークします。</span><span class="sxs-lookup"><span data-stu-id="731b9-150">In the list, mark the selected row.</span></span>
17. <span data-ttu-id="731b9-151">[属性] フィールドに、値を入力または選択します。</span><span class="sxs-lookup"><span data-stu-id="731b9-151">In the Attribute field, enter or select a value.</span></span>
18. <span data-ttu-id="731b9-152">[追加] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="731b9-152">Click Add.</span></span>
19. <span data-ttu-id="731b9-153">[テキスト定数] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="731b9-153">Click Text constant.</span></span>
20. <span data-ttu-id="731b9-154">一覧で、選択された行をマークします。</span><span class="sxs-lookup"><span data-stu-id="731b9-154">In the list, mark the selected row.</span></span>
21. <span data-ttu-id="731b9-155">[テキスト] フィールドに値を入力します。</span><span class="sxs-lookup"><span data-stu-id="731b9-155">In the Text field, type a value.</span></span>
22. <span data-ttu-id="731b9-156">[追加] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="731b9-156">Click Add.</span></span>
23. <span data-ttu-id="731b9-157">[属性値] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="731b9-157">Click Attribute value.</span></span>
24. <span data-ttu-id="731b9-158">一覧で、選択された行をマークします。</span><span class="sxs-lookup"><span data-stu-id="731b9-158">In the list, mark the selected row.</span></span>
25. <span data-ttu-id="731b9-159">[属性] フィールドに、値を入力または選択します。</span><span class="sxs-lookup"><span data-stu-id="731b9-159">In the Attribute field, enter or select a value.</span></span>
26. <span data-ttu-id="731b9-160">[追加] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="731b9-160">Click Add.</span></span>
27. <span data-ttu-id="731b9-161">[テキスト定数] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="731b9-161">Click Text constant.</span></span>
28. <span data-ttu-id="731b9-162">一覧で、選択された行をマークします。</span><span class="sxs-lookup"><span data-stu-id="731b9-162">In the list, mark the selected row.</span></span>
29. <span data-ttu-id="731b9-163">[テキスト] フィールドに値を入力します。</span><span class="sxs-lookup"><span data-stu-id="731b9-163">In the Text field, type a value.</span></span>
30. <span data-ttu-id="731b9-164">[追加] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="731b9-164">Click Add.</span></span>
31. <span data-ttu-id="731b9-165">[属性値] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="731b9-165">Click Attribute value.</span></span>
32. <span data-ttu-id="731b9-166">一覧で、選択された行をマークします。</span><span class="sxs-lookup"><span data-stu-id="731b9-166">In the list, mark the selected row.</span></span>
33. <span data-ttu-id="731b9-167">[属性] フィールドに、値を入力または選択します。</span><span class="sxs-lookup"><span data-stu-id="731b9-167">In the Attribute field, enter or select a value.</span></span>
34. <span data-ttu-id="731b9-168">[追加] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="731b9-168">Click Add.</span></span>
35. <span data-ttu-id="731b9-169">[テキスト定数] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="731b9-169">Click Text constant.</span></span>
36. <span data-ttu-id="731b9-170">一覧で、選択された行をマークします。</span><span class="sxs-lookup"><span data-stu-id="731b9-170">In the list, mark the selected row.</span></span>
37. <span data-ttu-id="731b9-171">[テキスト] フィールドに値を入力します。</span><span class="sxs-lookup"><span data-stu-id="731b9-171">In the Text field, type a value.</span></span>
38. <span data-ttu-id="731b9-172">[追加] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="731b9-172">Click Add.</span></span>
39. <span data-ttu-id="731b9-173">[番号順序値] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="731b9-173">Click Number sequence value.</span></span>
40. <span data-ttu-id="731b9-174">一覧で、選択された行をマークします。</span><span class="sxs-lookup"><span data-stu-id="731b9-174">In the list, mark the selected row.</span></span>
41. <span data-ttu-id="731b9-175">[番号順序] フィールドに、値を入力または選択します。</span><span class="sxs-lookup"><span data-stu-id="731b9-175">In the Number sequence field, enter or select a value.</span></span>
42. <span data-ttu-id="731b9-176">ページを閉じます。</span><span class="sxs-lookup"><span data-stu-id="731b9-176">Close the page.</span></span>
43. <span data-ttu-id="731b9-177">ページを閉じます。</span><span class="sxs-lookup"><span data-stu-id="731b9-177">Close the page.</span></span>
44. <span data-ttu-id="731b9-178">ページを閉じます。</span><span class="sxs-lookup"><span data-stu-id="731b9-178">Close the page.</span></span>

