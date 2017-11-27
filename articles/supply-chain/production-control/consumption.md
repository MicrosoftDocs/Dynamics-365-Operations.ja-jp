---
title: "材料消費の計算"
description: "この記事は、材料消費の計算に関するさまざまなオプションについての情報を提供します。"
author: johanhoffmann
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: BOMDesignerEditBOM, BOMTable, ProdBOM
audience: Application User
ms.reviewer: yuyus
ms.search.scope: Core, Operations
ms.custom: 53401
ms.assetid: 9cff88e4-0425-4707-9178-3c2cb10df7c2
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: johanho
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 2771a31b5a4d418a27de0ebe1945d1fed2d8d6d6
ms.openlocfilehash: f674a1f0051ee4b228b8a92f717ef5348a452bed
ms.contentlocale: ja-jp
ms.lasthandoff: 11/03/2017

---

# <a name="calculate-material-consumption"></a><span data-ttu-id="7e31f-103">材料消費の計算</span><span class="sxs-lookup"><span data-stu-id="7e31f-103">Calculate material consumption</span></span>

[!include[banner](../includes/banner.md)]


<span data-ttu-id="7e31f-104">この記事は、材料消費の計算に関するさまざまなオプションについての情報を提供します。</span><span class="sxs-lookup"><span data-stu-id="7e31f-104">This article provides information about various options that are related to the calculation of material consumption.</span></span> 

<span data-ttu-id="7e31f-105">材料消費の計算に関連付けられる次のオプションは、**部品表**ページの**明細行の詳細**クイック タブの**設定**タブおよび**ステップ消費**タブで使用することができます。</span><span class="sxs-lookup"><span data-stu-id="7e31f-105">The following options that are related to the calculation of material consumption are available on the **Setup** and **Step consumption** tabs on the **Line details** FastTab of the **Bill of materials** page.</span></span>

## <a name="variable-and-constant-consumption"></a><span data-ttu-id="7e31f-106">変動消費と定量消費</span><span class="sxs-lookup"><span data-stu-id="7e31f-106">Variable and constant consumption</span></span>
<span data-ttu-id="7e31f-107">[**消費量**] フィールドで、消費を定数数量または変動数量として計算するかどうかを選択できます。</span><span class="sxs-lookup"><span data-stu-id="7e31f-107">In the **Consumption is** field, you can select whether consumption should be calculated as a constant quantity or a variable quantity.</span></span> <span data-ttu-id="7e31f-108">生産する数量に関係なく、固定の数量や量が生産に必要な場合は、[**定量**] を選択します。</span><span class="sxs-lookup"><span data-stu-id="7e31f-108">Select **Constant** if a fixed quantity or volume is required for the production, regardless of the quantity that is produced.</span></span> <span data-ttu-id="7e31f-109">完成品での材料の要求数量が生産される完成品の数に比例する場合は、**変動**を選択します。これが既定の設定です。</span><span class="sxs-lookup"><span data-stu-id="7e31f-109">Select **Variable**, which is the default setting, if the required amount of material in the finished goods is proportional to the number of finished goods that are produced.</span></span>

## <a name="calculating-consumption-from-a-formula"></a><span data-ttu-id="7e31f-110">計算式から消費量を計算</span><span class="sxs-lookup"><span data-stu-id="7e31f-110">Calculating consumption from a formula</span></span>
<span data-ttu-id="7e31f-111">**式**フィールドで、材料消費の計算のさまざまな式を設定できます。</span><span class="sxs-lookup"><span data-stu-id="7e31f-111">In the **Formula** field, you can set up various formulas for calculating material consumption.</span></span> <span data-ttu-id="7e31f-112">既定値の**標準**を使用する場合、消費は式からは計算されません。</span><span class="sxs-lookup"><span data-stu-id="7e31f-112">If you use the default value, **Standard**, the consumption isn't calculated from a formula.</span></span> <span data-ttu-id="7e31f-113">次の式は、**高さ**、**幅**、**奥行き**、**密度**、**定数**の各フィールドとともに使用します。</span><span class="sxs-lookup"><span data-stu-id="7e31f-113">The following formulas work together with the **Height**, **Width**, **Depth**, **Density**, and **Constant** fields:</span></span>

-   <span data-ttu-id="7e31f-114">高さ \* 定数</span><span class="sxs-lookup"><span data-stu-id="7e31f-114">Height \* Constant</span></span>
-   <span data-ttu-id="7e31f-115">高さ \* 幅 \* 定数</span><span class="sxs-lookup"><span data-stu-id="7e31f-115">Height \* Width \* Constant</span></span>
-   <span data-ttu-id="7e31f-116">高さ \* 幅 \* 奥行き \* 定数</span><span class="sxs-lookup"><span data-stu-id="7e31f-116">Height \* Width \* Depth \* Constant</span></span>
-   <span data-ttu-id="7e31f-117">(高さ \* 幅 \* 奥行き/密度) \* 定数</span><span class="sxs-lookup"><span data-stu-id="7e31f-117">(Height \* Width \* Depth / Density) \* Constant</span></span>

## <a name="rounding-up-and-multiples"></a><span data-ttu-id="7e31f-118">切り上げと倍数</span><span class="sxs-lookup"><span data-stu-id="7e31f-118">Rounding up and multiples</span></span>
<span data-ttu-id="7e31f-119">また、**切り上げ**と**倍数**のフィールドで、材料消費の値を切り上げることができます。</span><span class="sxs-lookup"><span data-stu-id="7e31f-119">Together, the **Rounding up** and **Multiples** fields let you round up the material consumption value.</span></span> <span data-ttu-id="7e31f-120">たとえば、生産に対して原材料がピッキングされる材料取り扱い単位に応じて、値を切り上げることができます。</span><span class="sxs-lookup"><span data-stu-id="7e31f-120">For example, you can round up the value according to the handling unit in which the raw material is picked for production.</span></span> <span data-ttu-id="7e31f-121">**切り上げ**フィールドでは、次のオプションを使用できます: **数量**、**測定**、**消費**。</span><span class="sxs-lookup"><span data-stu-id="7e31f-121">The following options are available in the **Rounding up** field: **Quantity**, **Measurement**, and **Consumption**.</span></span>

### <a name="quantity"></a><span data-ttu-id="7e31f-122">件数</span><span class="sxs-lookup"><span data-stu-id="7e31f-122">Quantity</span></span>

<span data-ttu-id="7e31f-123">丸め方法として**数量**を選択した場合、数量は指定した数量の倍数である必要があります。</span><span class="sxs-lookup"><span data-stu-id="7e31f-123">If you select **Quantity** as the rounding-up mechanism, the quantity must be a multiple of the specified quantity.</span></span> <span data-ttu-id="7e31f-124">たとえば、数量を自然数にする場合は、**倍数**フィールドに「**1**」を指定します。</span><span class="sxs-lookup"><span data-stu-id="7e31f-124">For example, if whole numbers are required, select **1** in the **Multiples** field.</span></span> <span data-ttu-id="7e31f-125">そうすることで、番号は 1 で割り切れる数量に切り上げられます。</span><span class="sxs-lookup"><span data-stu-id="7e31f-125">Numbers are then rounded up to a quantity that is divisible by 1.</span></span>

### <a name="measurement"></a><span data-ttu-id="7e31f-126">測定</span><span class="sxs-lookup"><span data-stu-id="7e31f-126">Measurement</span></span>

<span data-ttu-id="7e31f-127">原材料が特定のサイズで入荷される場合、通常、丸め方法として**測定**を選択します。</span><span class="sxs-lookup"><span data-stu-id="7e31f-127">Typically, you select **Measurement** as the rounding-up mechanism when the raw material comes in specific dimensions.</span></span> <span data-ttu-id="7e31f-128">たとえば、2 メートルの金属管が完成品に要求され、4.5 メートルの長さで金属管が保存されるとします。</span><span class="sxs-lookup"><span data-stu-id="7e31f-128">For example, a piece of 2-meter metal tube is required for a finished good, and the metal tube is stored in 4.5-meter lengths.</span></span> <span data-ttu-id="7e31f-129">この場合、**測定**の切り上げ方法は、特定の数量の完成品を生産するために必要な金属管の数量を計算するために使用できます。</span><span class="sxs-lookup"><span data-stu-id="7e31f-129">In this case, the **Measurement** rounding-up mechanism can be used to calculate how many metal tubes are required to produce a specific number of pieces of the finished good.</span></span> <span data-ttu-id="7e31f-130">この例では、[**式**] フィールドは [**高さ \* 定数**] に設定されています。</span><span class="sxs-lookup"><span data-stu-id="7e31f-130">For this example, the **Formula** field is set to **Height \* Constant**.</span></span> <span data-ttu-id="7e31f-131">[**高さ**] フィールドには **2** が設定され、これが完成品に必要な管の長さを示します。</span><span class="sxs-lookup"><span data-stu-id="7e31f-131">The **Height** field is set to **2** to indicate the length of the tube that is required for the finished good.</span></span> <span data-ttu-id="7e31f-132">**倍数**フィールドには **4.5** が設定され、4.5 メートルの長さで管がピッキングされることを示します。</span><span class="sxs-lookup"><span data-stu-id="7e31f-132">The **Multiple** field is set to **4.5** to indicate that the tube is picked in lengths of 4.5 meters.</span></span> <span data-ttu-id="7e31f-133">計算を次に示します。</span><span class="sxs-lookup"><span data-stu-id="7e31f-133">Here is the calculation:</span></span>

1.  <span data-ttu-id="7e31f-134">完成品 10 個あたりに必要な倍数: 10 ÷ 2 = 5 個</span><span class="sxs-lookup"><span data-stu-id="7e31f-134">Number of multiples that are required for 10 pieces of the finished good: 10 ÷ 2 = 5 pieces</span></span>
2.  <span data-ttu-id="7e31f-135">消費合計: 4.5 × 5 = 22.5 メートルの金属管</span><span class="sxs-lookup"><span data-stu-id="7e31f-135">Total consumption:  4.5 × 5 = 22.5 meters of metal tube</span></span>

<span data-ttu-id="7e31f-136">消費される管 5 個あたり 0.5 メートルの管が仕損されると仮定します。</span><span class="sxs-lookup"><span data-stu-id="7e31f-136">It's assumed that 0.5 meter of tube is scrapped for every five pieces of tube that are consumed.</span></span>

### <a name="consumption"></a><span data-ttu-id="7e31f-137">消耗</span><span class="sxs-lookup"><span data-stu-id="7e31f-137">Consumption</span></span>

<span data-ttu-id="7e31f-138">原材料を、製品の取り扱い単位の整数倍でピッキングする必要がある場合、通常、丸め方法として**消費**を選択します。</span><span class="sxs-lookup"><span data-stu-id="7e31f-138">Typically, you select **Consumption** as the rounding-up mechanism when raw material must be picked in whole quantities of a specific handling unit of the product.</span></span> <span data-ttu-id="7e31f-139">たとえば、完成品 1 つあたり 2 クオートの塗料が使用され、塗料は 25 クオート缶でピッキングされるとします。</span><span class="sxs-lookup"><span data-stu-id="7e31f-139">For example, 2 quarts of paint are used to produce one piece of a finished good, and the paint is picked in 25-quart cans.</span></span> <span data-ttu-id="7e31f-140">この場合、**消費**の切り上げ方法を使用すると、25 クオート缶の整数倍に消費を切り上げることができます。</span><span class="sxs-lookup"><span data-stu-id="7e31f-140">In this case, the **Consumption** rounding-up mechanism can be used to round up consumption to whole numbers of 25-quart cans.</span></span> <span data-ttu-id="7e31f-141">完成品を 180 個生産する場合に必要な塗料の数量の計算を次に示します。</span><span class="sxs-lookup"><span data-stu-id="7e31f-141">Here is the calculation for the amount of paint that is required if 180 pieces of the finished good must be produced:</span></span>

1.  <span data-ttu-id="7e31f-142">必要な塗料 (仕損を除く): 180 × 2 = 360 クオート</span><span class="sxs-lookup"><span data-stu-id="7e31f-142">Paint that is required, excluding scrap: 180 × 2 = 360 quarts</span></span>
2.  <span data-ttu-id="7e31f-143">缶の数量: 360 ÷ 25 = 14.4、これは 15 に切り上げられます</span><span class="sxs-lookup"><span data-stu-id="7e31f-143">Number of cans: 360 ÷ 25 = 14.4, which is rounded up to 15</span></span>
3.  <span data-ttu-id="7e31f-144">必要な塗料 (仕損を含む): 15 × 25 = 375 クオート</span><span class="sxs-lookup"><span data-stu-id="7e31f-144">Paint that is required, including scrap: 15 × 25 = 375 quarts</span></span>

## <a name="step-consumption"></a><span data-ttu-id="7e31f-145">ステップ消費</span><span class="sxs-lookup"><span data-stu-id="7e31f-145">Step consumption</span></span>
<span data-ttu-id="7e31f-146">ステップ消費を使用すると、数量間隔で定量消費を計算できます。</span><span class="sxs-lookup"><span data-stu-id="7e31f-146">Step consumption is used to calculate constant consumption in quantity intervals.</span></span> <span data-ttu-id="7e31f-147">[**設定**] タブの [**式**] フィールドで [**ステップ消費**] を選択すると、[**ステップ消費**] タブでステップに関する情報を追加できます。固定消費数量は、生産数量の間隔に設定できます。</span><span class="sxs-lookup"><span data-stu-id="7e31f-147">If you select **Step consumption** in the **Formula** field on the **Setup** tab, you can add information about the steps on the **Step consumption** tab. The fixed consumed quantity can be set up in intervals of the produced quantity.</span></span> <span data-ttu-id="7e31f-148">たとえば、ステップ消費は次の表のように設定します。</span><span class="sxs-lookup"><span data-stu-id="7e31f-148">For example, step consumption is set up as shown in the following table.</span></span>

| <span data-ttu-id="7e31f-149">シリーズの開始</span><span class="sxs-lookup"><span data-stu-id="7e31f-149">From series</span></span> | <span data-ttu-id="7e31f-150">件数</span><span class="sxs-lookup"><span data-stu-id="7e31f-150">Quantity</span></span> |
|-------------|----------|
| <span data-ttu-id="7e31f-151">0.00</span><span class="sxs-lookup"><span data-stu-id="7e31f-151">0.00</span></span>        | <span data-ttu-id="7e31f-152">10.0000</span><span class="sxs-lookup"><span data-stu-id="7e31f-152">10.0000</span></span>  |
| <span data-ttu-id="7e31f-153">100.00</span><span class="sxs-lookup"><span data-stu-id="7e31f-153">100.00</span></span>      | <span data-ttu-id="7e31f-154">20.0000</span><span class="sxs-lookup"><span data-stu-id="7e31f-154">20.0000</span></span>  |
| <span data-ttu-id="7e31f-155">200.00</span><span class="sxs-lookup"><span data-stu-id="7e31f-155">200.00</span></span>      | <span data-ttu-id="7e31f-156">40.0000</span><span class="sxs-lookup"><span data-stu-id="7e31f-156">40.0000</span></span>  |

<span data-ttu-id="7e31f-157">部品表 (BOM) の数量が 1 で、生産数量は 110 です。</span><span class="sxs-lookup"><span data-stu-id="7e31f-157">The bill of materials (BOM) quantity is 1, and the production quantity is 110.</span></span> <span data-ttu-id="7e31f-158">消費の式は、[シリーズの開始 (数量)] = [消費] です。</span><span class="sxs-lookup"><span data-stu-id="7e31f-158">The formula for the consumption is From series (Quantity) = Consumption.</span></span> <span data-ttu-id="7e31f-159">生産数量が 110 のため、「100 シリーズから」になります。</span><span class="sxs-lookup"><span data-stu-id="7e31f-159">Because the production quantity is 110, it falls into the "From 100 series."</span></span> <span data-ttu-id="7e31f-160">このため、数量は 20 です。</span><span class="sxs-lookup"><span data-stu-id="7e31f-160">Therefore, the quantity is 20.</span></span>




