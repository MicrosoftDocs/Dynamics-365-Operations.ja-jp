---
title: 選択したデータ型の小数点以下の精度の拡張
description: このトピックでは、選択したデータ型の小数点以下の精度の拡張方法について説明します。
author: LarsBlaaberg
ms.date: 09/24/2019
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Developer
ms.reviewer: rhaertle
ms.custom: 89563
ms.assetid: 8DA4DA85-0C2D-4CAF-B350-DAC9C1BE4DF9
ms.search.region: Global
ms.author: lolsen
ms.search.validFrom: 2018-10-10
ms.dyn365.ops.version: Platform update 21
ms.openlocfilehash: 986282f4fe21ddf56d30e473afa516dd98599017
ms.sourcegitcommit: 074b6e212d19dd5d84881d1cdd096611a18c207f
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 03/31/2021
ms.locfileid: "5749652"
---
# <a name="extending-decimal-point-precision-for-selected-data-types"></a><span data-ttu-id="fbc33-103">選択したデータ型の小数点以下の精度の拡張</span><span class="sxs-lookup"><span data-stu-id="fbc33-103">Extending decimal point precision for selected data types</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="fbc33-104">このトピックでは、選択したデータ型の小数点以下の精度の拡張方法について説明します。</span><span class="sxs-lookup"><span data-stu-id="fbc33-104">This topic describes how to extend decimal point precision for selected data types.</span></span> <span data-ttu-id="fbc33-105">特定のシナリオの小数点精度を変更するため、Real 型の特定の拡張データ型の拡張機能を作成することができます。</span><span class="sxs-lookup"><span data-stu-id="fbc33-105">You can create extensions of specific extended data types of the type Real, to change the decimal point precision for certain scenarios.</span></span> <span data-ttu-id="fbc33-106">小数点以下の桁数を変更するには、必要に応じて **NoOfDecimals** プロパティを変更します。</span><span class="sxs-lookup"><span data-stu-id="fbc33-106">To change the decimal point precision, change the **NoOfDecimals** property as needed.</span></span>

<span data-ttu-id="fbc33-107">拡張データ型は階層型になっており、拡張されたデータ型から動作を継承します。</span><span class="sxs-lookup"><span data-stu-id="fbc33-107">Extended data types are hierarchical and inherit behavior from the data type they extend.</span></span> <span data-ttu-id="fbc33-108">1 つの拡張データ型の小数点以下の桁数を変更すると、すべての派生した拡張データ型の小数点以下の桁数に適用されます。</span><span class="sxs-lookup"><span data-stu-id="fbc33-108">When changing the number of decimals for one extended data type, the number of decimals on all derived extended data types will follow.</span></span> <span data-ttu-id="fbc33-109">つまり、**NoOfDecimalsIsExtensible** が False である拡張データ型が見つかった場合、小数点以下の桁数が広範囲に拡張される場合があるため、親拡張データ型を確認します。</span><span class="sxs-lookup"><span data-stu-id="fbc33-109">In other words, if you find an extended data type where **NoOfDecimalsIsExtensible** is false, then check the parent extended data type, as the number of decimals might be extensible in this wider scope.</span></span>

## <a name="weight"></a><span data-ttu-id="fbc33-110">太さ</span><span class="sxs-lookup"><span data-stu-id="fbc33-110">Weight</span></span>
<span data-ttu-id="fbc33-111">既定では、小数点以下最大 2 桁の重量データを維持できます。</span><span class="sxs-lookup"><span data-stu-id="fbc33-111">Weight data can be maintained with a maximum of two decimals by default.</span></span> <span data-ttu-id="fbc33-112">小数点以下精度が最大 6 桁の重量データを入力、管理、および表示する必要がある場合、**WeightBase** 拡張データ型の小数点の精度を拡張する必要があります。</span><span class="sxs-lookup"><span data-stu-id="fbc33-112">If you require the ability to enter, maintain, and view weight data with a maximum precision of six decimals, you must extend the decimal point precision for the **WeightBase** extended data type.</span></span>

## <a name="product-width-height-and-depth"></a><span data-ttu-id="fbc33-113">製品の幅、高さ、および奥行き</span><span class="sxs-lookup"><span data-stu-id="fbc33-113">Product width, height and depth</span></span>
<span data-ttu-id="fbc33-114">既定では、小数点以下最大 2 桁の現物分析コードを維持することができます。</span><span class="sxs-lookup"><span data-stu-id="fbc33-114">These physical dimensions can be maintained with a maximum of two decimals by default.</span></span> <span data-ttu-id="fbc33-115">小数点以下精度が最大 6 桁のデータを入力、管理、および表示する必要がある場合、**InventWidth**、**InventHeight**、および **InventDepth** 拡張データ型の小数点の精度をそれぞれ拡張する必要があります。</span><span class="sxs-lookup"><span data-stu-id="fbc33-115">If you require the ability to enter, maintain, and view this data with a maximum precision of six decimals, you must extend the decimal point precision for the **InventWidth**, **InventHeight**, and **InventDepth** extended data types respectively.</span></span>

## <a name="product-quantity"></a><span data-ttu-id="fbc33-116">製品数量</span><span class="sxs-lookup"><span data-stu-id="fbc33-116">Product quantity</span></span>
<span data-ttu-id="fbc33-117">既定では、小数点以下最大 2 桁の、製品の調達、消費、生産、保存、および販売に関連する数量データを管理できます。</span><span class="sxs-lookup"><span data-stu-id="fbc33-117">Quantity data that is related to the procuring, consuming, producing, storing, and selling of products can be maintained with a maximum of two decimals by default.</span></span>
<span data-ttu-id="fbc33-118">小数点以下精度が最大 6 桁の製品数量を入力、管理、および表示する必要がある場合、**ProductQuantity**、**CostQuantity**、**CAMMagnitude** 拡張データ型の小数点の精度を拡張する必要があります。</span><span class="sxs-lookup"><span data-stu-id="fbc33-118">If you require the ability to enter, maintain, and view product quantities with a maximum precision of six decimals points, you must extend the decimal point precision of the **ProductQuantity**, **CostQuantity**, and **CAMMagnitude** extended data types.</span></span>

<span data-ttu-id="fbc33-119">部品表、数式、および製造オーダーでは、既定では、小数点以下 4 桁の数量を管理できます。</span><span class="sxs-lookup"><span data-stu-id="fbc33-119">Bill of materials, formulas, and production orders allow maintaining quantities with four decimals by default.</span></span> <span data-ttu-id="fbc33-120">小数点以下 5 桁以上が必要な場合、**BOMProductQuantity** 拡張データ型の小数点の精度を拡張します。</span><span class="sxs-lookup"><span data-stu-id="fbc33-120">If you require more than four decimals, extend the decimal point precision for the **BOMProductQuantity** extended data type.</span></span>

### <a name="related-data-types"></a><span data-ttu-id="fbc33-121">関連データ型</span><span class="sxs-lookup"><span data-stu-id="fbc33-121">Related data types</span></span>
<span data-ttu-id="fbc33-122">**価格単位**、**価格数量**、および **請求数量データ** は、製品数量とは別に拡張できます。</span><span class="sxs-lookup"><span data-stu-id="fbc33-122">**Price unit**, **Price quantity**, and **Charge quantity data** can be extended independently from product quantities.</span></span>
<span data-ttu-id="fbc33-123">**PriceUnit** 拡張データ型を拡張し、小数点の精度を、既定の価格単位 2 以外の値に変更できます。</span><span class="sxs-lookup"><span data-stu-id="fbc33-123">You can extend the **PriceUnit** extended data type to change the decimal point precision to a value other than the default two for price units.</span></span>

<span data-ttu-id="fbc33-124">**PriceQty** 拡張データ型を拡張し、小数点の精度を、既定の価格および請求数量 2 以外の値に変更できます。</span><span class="sxs-lookup"><span data-stu-id="fbc33-124">You can extend the **PriceQty** extended data type to change the decimal point precision to a value other than the default two for price and charge quantities.</span></span>

### <a name="overloaded-data-types"></a><span data-ttu-id="fbc33-125">オーバーロード拡張データ型</span><span class="sxs-lookup"><span data-stu-id="fbc33-125">Overloaded data types</span></span>
<span data-ttu-id="fbc33-126">数量データとその他のデータ型の両方を保管するのに使用される 2 つの拡張データ型があります。</span><span class="sxs-lookup"><span data-stu-id="fbc33-126">There are two extended data types that are used for storing both quantity data and other types of data.</span></span> <span data-ttu-id="fbc33-127">これらのデータ型は個別に拡張する必要があります。</span><span class="sxs-lookup"><span data-stu-id="fbc33-127">These data types must be extended separately.</span></span>

<span data-ttu-id="fbc33-128">**AmountQty** 拡張データ型は、金額と数量の両方を格納して表示するために使用します。</span><span class="sxs-lookup"><span data-stu-id="fbc33-128">The **AmountQty** extended data type is used for storing and presenting both amounts and quantities.</span></span> <span data-ttu-id="fbc33-129">**AmountQty** 拡張データ型は、金額と数量の両方に対して必要な小数点以下の最大金額に拡張する必要があります。</span><span class="sxs-lookup"><span data-stu-id="fbc33-129">The **AmountQty** extended data type should be extended to the maximum amount of required decimals for both amounts and quantities.</span></span> <span data-ttu-id="fbc33-130">たとえば、金額は小数点以下 3 で維持する必要があるが、数量は引き続き小数点以下 2 桁で維持する必要がある場合は、小数点以下 3 桁にデータ型を拡張する必要があります。</span><span class="sxs-lookup"><span data-stu-id="fbc33-130">For example, if amounts need to be maintained with three decimal points, but quantities still need to be maintained with two decimal points, then the data type should be extended to three decimal points.</span></span>

<span data-ttu-id="fbc33-131">**ProductQuantityHourValue** 拡張データ型は、時間と数量の両方を格納して表示するために使用します。</span><span class="sxs-lookup"><span data-stu-id="fbc33-131">The **ProductQuantityHourValue** extended data type is used for storing and presenting both hours and quantities.</span></span> <span data-ttu-id="fbc33-132">**ProductQuantityHourValue** 拡張データ型は、時間と数量の両方に対して必要な小数点以下の最大桁数に拡張する必要があります。</span><span class="sxs-lookup"><span data-stu-id="fbc33-132">The **ProductQuantityHourValue** extended data type should be extended to the maximum amount of required decimal points for both hours and quantities.</span></span>
<span data-ttu-id="fbc33-133">たとえば、数量は小数点以下 4 桁で維持する必要があるが、時間は引き続き小数点以下 2 桁で維持する必要がある場合は、小数点以下 4 桁にデータ型を拡張する必要があります。</span><span class="sxs-lookup"><span data-stu-id="fbc33-133">For example, if quantities need to be maintained with four decimal points, but hours still need to be maintained with two decimal points, then the data type should be extended to four decimal points.</span></span>


## <a name="unit-amounts"></a><span data-ttu-id="fbc33-134">ユニット金額</span><span class="sxs-lookup"><span data-stu-id="fbc33-134">Unit amounts</span></span>
<span data-ttu-id="fbc33-135">既定では、価格、明細行の割引金額、請求金額の明細行の金額を含むユニット金額は、小数点以下最大 2 桁で維持することができます。</span><span class="sxs-lookup"><span data-stu-id="fbc33-135">By default, unit amounts including prices, line discount amounts, and line charge amounts can be maintained with a maximum of two decimals.</span></span>

<span data-ttu-id="fbc33-136">小数点以下の精度が最大 6 桁のユニット金額を入力、管理、および表示する必要がある場合、**UnitAmountCur**、**UnitAmountMST**、**CostPriceNonMonetary** 拡張データ型の小数点の精度を拡張する必要があります。</span><span class="sxs-lookup"><span data-stu-id="fbc33-136">If you require the ability enter, maintain, and view unit amounts with a maximum precision of six decimal points, you must extend the decimal point precision of the **UnitAmountCur**, **UnitAmountMST**, and **CostPriceNonMonetary** extended data types.</span></span>

<span data-ttu-id="fbc33-137">小数点以下 4 桁以上の精度が必要な場合、PriceRoundOff 拡張データ型も拡張する必要があります。</span><span class="sxs-lookup"><span data-stu-id="fbc33-137">If you require a decimal point precision of more than four, you should also extend the PriceRoundOff extended data type.</span></span>

### <a name="overloaded-data-types"></a><span data-ttu-id="fbc33-138">オーバーロード拡張データ型</span><span class="sxs-lookup"><span data-stu-id="fbc33-138">Overloaded data types</span></span>
<span data-ttu-id="fbc33-139">ユニット数量データとその他のデータ型の両方を保管するのに使用される 5 つの拡張データ型があります。</span><span class="sxs-lookup"><span data-stu-id="fbc33-139">There are five extended data types that are used for storing both unit amount data and other types of data.</span></span>

<span data-ttu-id="fbc33-140">**PriceDiscAmount** 拡張データ型は、金額とユニット数量を格納して表示するために使用します。</span><span class="sxs-lookup"><span data-stu-id="fbc33-140">The **PriceDiscAmount** extended data type is used for storing and presenting amounts and unit amounts.</span></span> <span data-ttu-id="fbc33-141">**PriceDiscAmount** 拡張データ型は、金額とユニット数量の両方に対して必要な小数点以下の最大金額に拡張する必要があります。</span><span class="sxs-lookup"><span data-stu-id="fbc33-141">The **PriceDiscAmount** extended data type should be extended to the maximum amount of required decimals points for both amounts and unit amounts.</span></span>
<span data-ttu-id="fbc33-142">たとえば、金額は小数点以下 3 桁で維持する必要があるが、ユニット金額は小数点以下 4 桁で維持する必要がある場合は、小数点以下 4 桁にデータ型を拡張する必要があります。</span><span class="sxs-lookup"><span data-stu-id="fbc33-142">For example, if amounts need to be maintained with three decimal points, but unit amounts need to be maintained with four decimal points, the data type should be extended to four decimal points.</span></span>

<span data-ttu-id="fbc33-143">**MCRRoyaltyValue**、**PdsRebateValue**、**TAMRebateValue**、および **MarkupValue** 拡張データ型は、金額、ユニット金額、割合を格納して表示するのに使用されます。</span><span class="sxs-lookup"><span data-stu-id="fbc33-143">The **MCRRoyaltyValue**, **PdsRebateValue**, **TAMRebateValue**, and **MarkupValue** extended data types are used for storing and presenting amounts, unit amounts, and percentages.</span></span>
<span data-ttu-id="fbc33-144">拡張データ型は、金額、ユニット数量、割合に対して必要な小数点以下の最大金額に拡張する必要があります。</span><span class="sxs-lookup"><span data-stu-id="fbc33-144">The extended data types should be extended to the maximum amount of required decimal points for amounts, unit amounts, and percentages.</span></span> <span data-ttu-id="fbc33-145">たとえば、金額は小数点以下 3 桁で維持する必要があるが、ユニット金額は小数点以下 4 桁で維持する必要があり、割合は小数点以下 2 桁で維持する必要がある場合は、小数点以下 4 桁にデータ型を拡張する必要があります。</span><span class="sxs-lookup"><span data-stu-id="fbc33-145">For example, if amounts need to be maintained with three decimal points, but unit amounts need to be maintained with four decimal points and percentages should remain maintained with two decimal points, then the data type should be extended to four decimal points.</span></span>

## <a name="amounts"></a><span data-ttu-id="fbc33-146">金額</span><span class="sxs-lookup"><span data-stu-id="fbc33-146">Amounts</span></span>
<span data-ttu-id="fbc33-147">既定では、ユニット金額を含む金額は、小数点以下最大 2 桁で管理できます。</span><span class="sxs-lookup"><span data-stu-id="fbc33-147">Amounts, including unit amounts, can be maintained with a maximum of two decimals by default.</span></span>

<span data-ttu-id="fbc33-148">小数点以下の精度が最大 6 桁のユニット金額を含む金額を入力、管理、および表示できる必要がある場合、**Amount**、**AmountMST**、**CostAmountNonMonetary** 拡張データ型の小数点の精度を拡張する必要があります。</span><span class="sxs-lookup"><span data-stu-id="fbc33-148">If you require the ability to enter, maintain, and view amounts including unit amounts with a precision of maximum six decimal points, you must extend the decimal point precision of the **Amount**, **AmountMST**, and **CostAmountNonMonetary** extended data types.</span></span>
<span data-ttu-id="fbc33-149">金額以外ユニット金額にさまざまな精度が必要な場合は、ユニット金額の小数点以下の精度を拡張する方法の説明に従います。</span><span class="sxs-lookup"><span data-stu-id="fbc33-149">If you require a different precision for unit amounts other than for amount, follow the description for how to extend the decimal point precision for unit amounts.</span></span>

### <a name="overloaded-data-types"></a><span data-ttu-id="fbc33-150">オーバーロード拡張データ型</span><span class="sxs-lookup"><span data-stu-id="fbc33-150">Overloaded data types</span></span>
<span data-ttu-id="fbc33-151">金額データとその他のデータ型の両方を保管するのに使用される 3 つの拡張データ型があります。</span><span class="sxs-lookup"><span data-stu-id="fbc33-151">There are three extended data types that are used for storing amount data and other types of data.</span></span> <span data-ttu-id="fbc33-152">つまり、個別に拡張する必要があります。</span><span class="sxs-lookup"><span data-stu-id="fbc33-152">This means that they must be extended separately.</span></span>

<span data-ttu-id="fbc33-153">**AmountQty** 拡張データ型は、金額と数量を格納して表示するために使用します。</span><span class="sxs-lookup"><span data-stu-id="fbc33-153">The **AmountQty** extended data type is used for storing and presenting amounts and quantities.</span></span> <span data-ttu-id="fbc33-154">**AmountQty** 拡張データ型は、金額と数量の両方に対して必要な小数点以下の最大金額に拡張する必要があります。</span><span class="sxs-lookup"><span data-stu-id="fbc33-154">The **AmountQty** extended data type should be extended to the maximum amount of required decimals for both amounts and quantities.</span></span> <span data-ttu-id="fbc33-155">たとえば、金額は小数点以下 3 桁で維持する必要があるが、数量は引き続き 2 桁で維持する必要がある場合は、小数点以下 3 桁にデータ型を拡張する必要があります。</span><span class="sxs-lookup"><span data-stu-id="fbc33-155">For example, if amounts need to be maintained with three decimal points, but quantities still need to be maintained with two, then the data type should be extended to three decimal points.</span></span>

<span data-ttu-id="fbc33-156">**PriceDiscAmount** 拡張データ型は、金額とユニット数量を格納して表示するために使用します。</span><span class="sxs-lookup"><span data-stu-id="fbc33-156">The **PriceDiscAmount** extended data type is used for storing and presenting amounts and unit amounts.</span></span> <span data-ttu-id="fbc33-157">**PriceDiscAmount** 拡張データ型は、金額とユニット数量に対して必要な小数点以下の最大金額に拡張する必要があります。</span><span class="sxs-lookup"><span data-stu-id="fbc33-157">The **PriceDiscAmount** extended data type should be extended to the maximum amount of required decimals points for amounts and unit amounts.</span></span>
<span data-ttu-id="fbc33-158">たとえば、金額は小数点以下 3 桁で維持する必要があるが、ユニット金額は小数点以下 4 桁で維持する必要がある場合は、小数点以下 4 桁にデータ型を拡張する必要があります。</span><span class="sxs-lookup"><span data-stu-id="fbc33-158">For example, if amounts need to be maintained with three decimal points, but unit amounts need to be maintained with four decimal points, then the data type should be extended to four decimal points.</span></span>

<span data-ttu-id="fbc33-159">**MarkupValue** 拡張データ型は、金額、ユニット数量、割合を格納して表示するために使用します。</span><span class="sxs-lookup"><span data-stu-id="fbc33-159">The **MarkupValue** extended data type is used for storing and presenting amounts, unit amounts, and percentages.</span></span>
<span data-ttu-id="fbc33-160">拡張データ型は、金額、ユニット数量、割合に対して必要な小数点以下の最大金額に拡張する必要があります。</span><span class="sxs-lookup"><span data-stu-id="fbc33-160">The extended data types should be extended to the maximum amount of required decimals points for amounts, unit amounts, and percentages.</span></span>
<span data-ttu-id="fbc33-161">たとえば、金額は小数点以下 3 桁で維持する必要があり、ユニット金額は小数点以下 4 桁で維持する必要があり、割合は小数点以下 2 桁で維持する必要がある場合は、小数点以下 4 桁にデータ型を拡張する必要があります。</span><span class="sxs-lookup"><span data-stu-id="fbc33-161">For example, if amounts need to be maintained with three decimal points, unit amounts need to be maintained with four decimal points, and percentages should remain with two decimal points, then the data type should be extended to four decimal points.</span></span>


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]