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
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: kamaybac
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 5f75d7e493255b9c09c10b121f388854861cb0fc
ms.sourcegitcommit: 199848e78df5cb7c439b001bdbe1ece963593cdb
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 10/13/2020
ms.locfileid: "4431960"
---
# <a name="create-a-product-number-nomenclature-for-configured-product-variants"></a><span data-ttu-id="d85d1-103">コンフィギュレーション済みの製品バリアントの製品番号の分類の作成</span><span class="sxs-lookup"><span data-stu-id="d85d1-103">Create a product number nomenclature for configured product variants</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="d85d1-104">この手順では、コンフィギュレーション済製品バリアントにおける製品番号の分類を設定する方法、およびそれをコンフィギュレーション可能な製品マスターに関連付ける方法を示します。</span><span class="sxs-lookup"><span data-stu-id="d85d1-104">This procedure shows you how to set up a product number nomenclature for configured product variants, and how it can be attached to a configurable product master.</span></span> <span data-ttu-id="d85d1-105">この手順では、製品コンフィギュレーション モデル コンポーネントのコンフィギュレーションに関する用語をどのように作成するかを示します。</span><span class="sxs-lookup"><span data-stu-id="d85d1-105">This procedure also demonstrates how you can build a configuration nomenclature for a product configuration model component.</span></span> <span data-ttu-id="d85d1-106">この手順の作成に使用するデモ データの会社は USMF です。</span><span class="sxs-lookup"><span data-stu-id="d85d1-106">The demo data company used to create this procedure is USMF.</span></span> <span data-ttu-id="d85d1-107">新しい製品番号の分類は、「D0004」製品マスターに割り当てられます。</span><span class="sxs-lookup"><span data-stu-id="d85d1-107">The new product number nomenclature is assigned to the D0004 product master.</span></span> <span data-ttu-id="d85d1-108">このタスクは、通常、製品デザイナーが行います。</span><span class="sxs-lookup"><span data-stu-id="d85d1-108">This task would typically be done by a product designer.</span></span>


## <a name="create-a-product-number-nomenclature"></a><span data-ttu-id="d85d1-109">[製品番号の分類] を作成します。</span><span class="sxs-lookup"><span data-stu-id="d85d1-109">Create a product number nomenclature</span></span>
1. <span data-ttu-id="d85d1-110">[製品バリアント モデルの定義] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="d85d1-110">Click Product variant model definition.</span></span>
2. <span data-ttu-id="d85d1-111">[製品の分類] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="d85d1-111">Click Product nomenclature.</span></span>
3. <span data-ttu-id="d85d1-112">[新規] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="d85d1-112">Click New.</span></span>
4. <span data-ttu-id="d85d1-113">[名前] フィールドに値を入力します。</span><span class="sxs-lookup"><span data-stu-id="d85d1-113">In the Name field, type a value.</span></span>
5. <span data-ttu-id="d85d1-114">[説明] フィールドに値を入力します。</span><span class="sxs-lookup"><span data-stu-id="d85d1-114">In the Description field, type a value.</span></span>
6. <span data-ttu-id="d85d1-115">[追加] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="d85d1-115">Click Add.</span></span>
7. <span data-ttu-id="d85d1-116">[製品マスター番号] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="d85d1-116">Click Product master number.</span></span>
8. <span data-ttu-id="d85d1-117">[追加] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="d85d1-117">Click Add.</span></span>
9. <span data-ttu-id="d85d1-118">[テキスト定数] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="d85d1-118">Click Text constant.</span></span>
10. <span data-ttu-id="d85d1-119">一覧で、選択された行をマークします。</span><span class="sxs-lookup"><span data-stu-id="d85d1-119">In the list, mark the selected row.</span></span>
11. <span data-ttu-id="d85d1-120">[テキスト] フィールドに値を入力します。</span><span class="sxs-lookup"><span data-stu-id="d85d1-120">In the Text field, type a value.</span></span>
12. <span data-ttu-id="d85d1-121">[追加] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="d85d1-121">Click Add.</span></span>
13. <span data-ttu-id="d85d1-122">[コンフィギュレーション] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="d85d1-122">Click Configuration.</span></span>
14. <span data-ttu-id="d85d1-123">ページを閉じます。</span><span class="sxs-lookup"><span data-stu-id="d85d1-123">Close the page.</span></span>

## <a name="assign-the-product-number-nomenclature-to-a-product-master"></a><span data-ttu-id="d85d1-124">製品番号の分類を製品マスターに割り当てる</span><span class="sxs-lookup"><span data-stu-id="d85d1-124">Assign the product number nomenclature to a product master</span></span>
1. <span data-ttu-id="d85d1-125">[製品マスター] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="d85d1-125">Click Product masters.</span></span>
2. <span data-ttu-id="d85d1-126">クイック フィルターを使用して、レコードを見つけます。</span><span class="sxs-lookup"><span data-stu-id="d85d1-126">Use the Quick Filter to find records.</span></span> <span data-ttu-id="d85d1-127">たとえば、「D」という値を含む [製品番号] フィールドをフィルターします。</span><span class="sxs-lookup"><span data-stu-id="d85d1-127">For example, filter on the Product number field with a value of 'D'.</span></span>
3. <span data-ttu-id="d85d1-128">一覧で、選択された行のリンクをクリックします。</span><span class="sxs-lookup"><span data-stu-id="d85d1-128">In the list, click the link in the selected row.</span></span>
4. <span data-ttu-id="d85d1-129">[編集] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="d85d1-129">Click Edit.</span></span>
5. <span data-ttu-id="d85d1-130">[分類の使用] フィールドで、[はい] を選択します。</span><span class="sxs-lookup"><span data-stu-id="d85d1-130">Select Yes in the Use nomenclature field.</span></span>
6. <span data-ttu-id="d85d1-131">[製品バリアント番号の分類] フィールドに、値を入力または選択します。</span><span class="sxs-lookup"><span data-stu-id="d85d1-131">In the Product variant number nomenclature field, enter or select a value.</span></span>
7. <span data-ttu-id="d85d1-132">ページを閉じます。</span><span class="sxs-lookup"><span data-stu-id="d85d1-132">Close the page.</span></span>
8. <span data-ttu-id="d85d1-133">ページを閉じます。</span><span class="sxs-lookup"><span data-stu-id="d85d1-133">Close the page.</span></span>

## <a name="create-nomenclature-for-a-product-configuration-model-component"></a><span data-ttu-id="d85d1-134">製品コンフィギュレーション モデル コンポーネントの分類の作成</span><span class="sxs-lookup"><span data-stu-id="d85d1-134">Create nomenclature for a product configuration model component</span></span>
1. <span data-ttu-id="d85d1-135">[製品コンフィギュレーション モデル] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="d85d1-135">Click Product configuration models.</span></span>
2. <span data-ttu-id="d85d1-136">一覧で、目的のレコードを見つけ、選択します。</span><span class="sxs-lookup"><span data-stu-id="d85d1-136">In the list, find and select the desired record.</span></span>
3. <span data-ttu-id="d85d1-137">一覧で、選択された行のリンクをクリックします。</span><span class="sxs-lookup"><span data-stu-id="d85d1-137">In the list, click the link in the selected row.</span></span>
4. <span data-ttu-id="d85d1-138">[編集] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="d85d1-138">Click Edit.</span></span>
5. <span data-ttu-id="d85d1-139">[コンフィギュレーションの分類の使用] フィールドで、[はい] を選択します。</span><span class="sxs-lookup"><span data-stu-id="d85d1-139">Select Yes in the Use configuration nomenclature field.</span></span>
6. <span data-ttu-id="d85d1-140">[追加] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="d85d1-140">Click Add.</span></span>
7. <span data-ttu-id="d85d1-141">[属性値] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="d85d1-141">Click Attribute value.</span></span>
8. <span data-ttu-id="d85d1-142">一覧で、選択された行をマークします。</span><span class="sxs-lookup"><span data-stu-id="d85d1-142">In the list, mark the selected row.</span></span>
9. <span data-ttu-id="d85d1-143">[属性] フィールドに、値を入力または選択します。</span><span class="sxs-lookup"><span data-stu-id="d85d1-143">In the Attribute field, enter or select a value.</span></span>
10. <span data-ttu-id="d85d1-144">[追加] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="d85d1-144">Click Add.</span></span>
11. <span data-ttu-id="d85d1-145">[テキスト定数] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="d85d1-145">Click Text constant.</span></span>
12. <span data-ttu-id="d85d1-146">一覧で、選択された行をマークします。</span><span class="sxs-lookup"><span data-stu-id="d85d1-146">In the list, mark the selected row.</span></span>
13. <span data-ttu-id="d85d1-147">[テキスト] フィールドに値を入力します。</span><span class="sxs-lookup"><span data-stu-id="d85d1-147">In the Text field, type a value.</span></span>
14. <span data-ttu-id="d85d1-148">[追加] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="d85d1-148">Click Add.</span></span>
15. <span data-ttu-id="d85d1-149">[属性値] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="d85d1-149">Click Attribute value.</span></span>
16. <span data-ttu-id="d85d1-150">一覧で、選択された行をマークします。</span><span class="sxs-lookup"><span data-stu-id="d85d1-150">In the list, mark the selected row.</span></span>
17. <span data-ttu-id="d85d1-151">[属性] フィールドに、値を入力または選択します。</span><span class="sxs-lookup"><span data-stu-id="d85d1-151">In the Attribute field, enter or select a value.</span></span>
18. <span data-ttu-id="d85d1-152">[追加] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="d85d1-152">Click Add.</span></span>
19. <span data-ttu-id="d85d1-153">[テキスト定数] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="d85d1-153">Click Text constant.</span></span>
20. <span data-ttu-id="d85d1-154">一覧で、選択された行をマークします。</span><span class="sxs-lookup"><span data-stu-id="d85d1-154">In the list, mark the selected row.</span></span>
21. <span data-ttu-id="d85d1-155">[テキスト] フィールドに値を入力します。</span><span class="sxs-lookup"><span data-stu-id="d85d1-155">In the Text field, type a value.</span></span>
22. <span data-ttu-id="d85d1-156">[追加] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="d85d1-156">Click Add.</span></span>
23. <span data-ttu-id="d85d1-157">[属性値] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="d85d1-157">Click Attribute value.</span></span>
24. <span data-ttu-id="d85d1-158">一覧で、選択された行をマークします。</span><span class="sxs-lookup"><span data-stu-id="d85d1-158">In the list, mark the selected row.</span></span>
25. <span data-ttu-id="d85d1-159">[属性] フィールドに、値を入力または選択します。</span><span class="sxs-lookup"><span data-stu-id="d85d1-159">In the Attribute field, enter or select a value.</span></span>
26. <span data-ttu-id="d85d1-160">[追加] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="d85d1-160">Click Add.</span></span>
27. <span data-ttu-id="d85d1-161">[テキスト定数] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="d85d1-161">Click Text constant.</span></span>
28. <span data-ttu-id="d85d1-162">一覧で、選択された行をマークします。</span><span class="sxs-lookup"><span data-stu-id="d85d1-162">In the list, mark the selected row.</span></span>
29. <span data-ttu-id="d85d1-163">[テキスト] フィールドに値を入力します。</span><span class="sxs-lookup"><span data-stu-id="d85d1-163">In the Text field, type a value.</span></span>
30. <span data-ttu-id="d85d1-164">[追加] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="d85d1-164">Click Add.</span></span>
31. <span data-ttu-id="d85d1-165">[属性値] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="d85d1-165">Click Attribute value.</span></span>
32. <span data-ttu-id="d85d1-166">一覧で、選択された行をマークします。</span><span class="sxs-lookup"><span data-stu-id="d85d1-166">In the list, mark the selected row.</span></span>
33. <span data-ttu-id="d85d1-167">[属性] フィールドに、値を入力または選択します。</span><span class="sxs-lookup"><span data-stu-id="d85d1-167">In the Attribute field, enter or select a value.</span></span>
34. <span data-ttu-id="d85d1-168">[追加] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="d85d1-168">Click Add.</span></span>
35. <span data-ttu-id="d85d1-169">[テキスト定数] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="d85d1-169">Click Text constant.</span></span>
36. <span data-ttu-id="d85d1-170">一覧で、選択された行をマークします。</span><span class="sxs-lookup"><span data-stu-id="d85d1-170">In the list, mark the selected row.</span></span>
37. <span data-ttu-id="d85d1-171">[テキスト] フィールドに値を入力します。</span><span class="sxs-lookup"><span data-stu-id="d85d1-171">In the Text field, type a value.</span></span>
38. <span data-ttu-id="d85d1-172">[追加] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="d85d1-172">Click Add.</span></span>
39. <span data-ttu-id="d85d1-173">[番号順序値] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="d85d1-173">Click Number sequence value.</span></span>
40. <span data-ttu-id="d85d1-174">一覧で、選択された行をマークします。</span><span class="sxs-lookup"><span data-stu-id="d85d1-174">In the list, mark the selected row.</span></span>
41. <span data-ttu-id="d85d1-175">[番号順序] フィールドに、値を入力または選択します。</span><span class="sxs-lookup"><span data-stu-id="d85d1-175">In the Number sequence field, enter or select a value.</span></span>
42. <span data-ttu-id="d85d1-176">ページを閉じます。</span><span class="sxs-lookup"><span data-stu-id="d85d1-176">Close the page.</span></span>
43. <span data-ttu-id="d85d1-177">ページを閉じます。</span><span class="sxs-lookup"><span data-stu-id="d85d1-177">Close the page.</span></span>
44. <span data-ttu-id="d85d1-178">ページを閉じます。</span><span class="sxs-lookup"><span data-stu-id="d85d1-178">Close the page.</span></span>

