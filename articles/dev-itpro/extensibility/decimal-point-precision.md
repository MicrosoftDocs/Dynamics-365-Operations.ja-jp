---
title: "選択したデータ型の小数点以下の精度の拡張"
description: "このトピックでは、選択したデータ型の小数点以下の精度の拡張方法について説明します。"
author: LarsBlaaberg
manager: 
ms.date: 10/10/2018
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-platform
ms.technology: 
audience: Developer
ms.reviewer: 
ms.search.scope: Operations
ms.custom: 89563
ms.assetid: 8DA4DA85-0C2D-4CAF-B350-DAC9C1BE4DF9
ms.search.region: Global
ms.author: lolsen
ms.search.validFrom: 2018-10-10
ms.dyn365.ops.version: Platform update 21
ms.translationtype: HT
ms.sourcegitcommit: 3b7c2b72d97c42076e1f759e9c11c74cb17476c1
ms.openlocfilehash: 8eef5c18b6cde5053bd16827dca3019dcd7cf607
ms.contentlocale: ja-jp
ms.lasthandoff: 10/17/2018

---

# <a name="extending-decimal-point-precision-for-selected-data-types"></a><span data-ttu-id="4f4a9-103">選択したデータ型の小数点以下の精度の拡張</span><span class="sxs-lookup"><span data-stu-id="4f4a9-103">Extending decimal point precision for selected data types</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="4f4a9-104">このトピックでは、選択したデータ型の小数点以下の精度の拡張方法について説明します。</span><span class="sxs-lookup"><span data-stu-id="4f4a9-104">This topic describes how to extend decimal point precision for selected data types.</span></span> <span data-ttu-id="4f4a9-105">特定のシナリオの小数点精度を変更するため、Real 型の特定の拡張データ型の拡張機能を作成することができます。</span><span class="sxs-lookup"><span data-stu-id="4f4a9-105">You can create extensions of specific extended data types of the type Real, to change the decimal point precision for certain scenarios.</span></span>

## <a name="weight"></a><span data-ttu-id="4f4a9-106">太さ</span><span class="sxs-lookup"><span data-stu-id="4f4a9-106">Weight</span></span>
<span data-ttu-id="4f4a9-107">既定では、小数点以下最大 2 桁の重量データを維持できます。</span><span class="sxs-lookup"><span data-stu-id="4f4a9-107">Weight data can be maintained with a maximum of two decimals by default.</span></span> <span data-ttu-id="4f4a9-108">小数点以下精度が最大 6 桁の重量データを入力、管理、および表示する必要がある場合、**WeightBase** 拡張データ型の小数点の精度を拡張する必要があります。</span><span class="sxs-lookup"><span data-stu-id="4f4a9-108">If you require the ability to enter, maintain, and view weight data with a maximum precision of six decimals, you must extend the decimal point precision for the **WeightBase** extended data type.</span></span>

## <a name="product-quantity"></a><span data-ttu-id="4f4a9-109">製品数量</span><span class="sxs-lookup"><span data-stu-id="4f4a9-109">Product quantity</span></span>
<span data-ttu-id="4f4a9-110">既定では、小数点以下最大 2 桁の、製品の調達、消費、生産、保存、および販売に関連する数量データを管理できます。</span><span class="sxs-lookup"><span data-stu-id="4f4a9-110">Quantity data that is related to the procuring, consuming, producing, storing, and selling of products can be maintained with a maximum of two decimals by default.</span></span>
<span data-ttu-id="4f4a9-111">小数点以下精度が最大 6 桁の製品数量を入力、管理、および表示する必要がある場合、**ProductQuantity**、**CostQuantity**、**CAMMagnitude** 拡張データ型の小数点の精度を拡張する必要があります。</span><span class="sxs-lookup"><span data-stu-id="4f4a9-111">If you require the ability to enter, maintain, and view product quantities with a maximum precision of six decimals points, you must extend the decimal point precision of the **ProductQuantity**, **CostQuantity**, and **CAMMagnitude** extended data types.</span></span>

<span data-ttu-id="4f4a9-112">部品表、数式、および製造オーダーでは、既定では、小数点以下 4 桁の数量を管理できます。</span><span class="sxs-lookup"><span data-stu-id="4f4a9-112">Bill of materials, formulas, and production orders allow maintaining quantities with four decimals by default.</span></span> <span data-ttu-id="4f4a9-113">小数点以下 5 桁以上が必要な場合、**BOMProductQuantity** 拡張データ型の小数点の精度を拡張します。</span><span class="sxs-lookup"><span data-stu-id="4f4a9-113">If you require more than four decimals, extend the decimal point precision for the **BOMProductQuantity** extended data type.</span></span>

### <a name="related-data-types"></a><span data-ttu-id="4f4a9-114">関連データ型</span><span class="sxs-lookup"><span data-stu-id="4f4a9-114">Related data types</span></span>
<span data-ttu-id="4f4a9-115">**価格単位**、**価格数量**、および**請求数量データ**は、製品数量とは別に拡張できます。</span><span class="sxs-lookup"><span data-stu-id="4f4a9-115">**Price unit**, **Price quantity**, and **Charge quantity data** can be extended independently from product quantities.</span></span>
<span data-ttu-id="4f4a9-116">**PriceUnit** 拡張データ型を拡張し、小数点の精度を、既定の価格単位 2 以外の値に変更できます。</span><span class="sxs-lookup"><span data-stu-id="4f4a9-116">You can extend the **PriceUnit** extended data type to change the decimal point precision to a value other than the default two for price units.</span></span>

<span data-ttu-id="4f4a9-117">**PriceQty** 拡張データ型を拡張し、小数点の精度を、既定の価格および請求数量 2 以外の値に変更できます。</span><span class="sxs-lookup"><span data-stu-id="4f4a9-117">You can extend the **PriceQty** extended data type to change the decimal point precision to a value other than the default two for price and charge quantities.</span></span>

### <a name="overloaded-data-types"></a><span data-ttu-id="4f4a9-118">オーバーロード拡張データ型</span><span class="sxs-lookup"><span data-stu-id="4f4a9-118">Overloaded data types</span></span>
<span data-ttu-id="4f4a9-119">数量データとその他のデータ型の両方を保管するのに使用される 2 つの拡張データ型があります。</span><span class="sxs-lookup"><span data-stu-id="4f4a9-119">There are two extended data types that are used for storing both quantity data and other types of data.</span></span> <span data-ttu-id="4f4a9-120">これらのデータ型は個別に拡張する必要があります。</span><span class="sxs-lookup"><span data-stu-id="4f4a9-120">These data types must be extended separately.</span></span>

<span data-ttu-id="4f4a9-121">**AmountQty** 拡張データ型は、金額と数量の両方を格納して表示するために使用します。</span><span class="sxs-lookup"><span data-stu-id="4f4a9-121">The **AmountQty** extended data type is used for storing and presenting both amounts and quantities.</span></span> <span data-ttu-id="4f4a9-122">**AmountQty** 拡張データ型は、金額と数量の両方に対して必要な小数点以下の最大金額に拡張する必要があります。</span><span class="sxs-lookup"><span data-stu-id="4f4a9-122">The **AmountQty** extended data type should be extended to the maximum amount of required decimals for both amounts and quantities.</span></span> <span data-ttu-id="4f4a9-123">たとえば、金額は小数点以下 3 で維持する必要があるが、数量は引き続き小数点以下 2 桁で維持する必要がある場合は、小数点以下 3 桁にデータ型を拡張する必要があります。</span><span class="sxs-lookup"><span data-stu-id="4f4a9-123">For example, if amounts need to be maintained with three decimal points, but quantities still need to be maintained with two decimal points, then the data type should be extended to three decimal points.</span></span>

<span data-ttu-id="4f4a9-124">**ProductQuantityHourValue** 拡張データ型は、時間と数量の両方を格納して表示するために使用します。</span><span class="sxs-lookup"><span data-stu-id="4f4a9-124">The **ProductQuantityHourValue** extended data type is used for storing and presenting both hours and quantities.</span></span> <span data-ttu-id="4f4a9-125">**ProductQuantityHourValue** 拡張データ型は、時間と数量の両方に対して必要な小数点以下の最大桁数に拡張する必要があります。</span><span class="sxs-lookup"><span data-stu-id="4f4a9-125">The **ProductQuantityHourValue** extended data type should be extended to the maximum amount of required decimal points for both hours and quantities.</span></span>
<span data-ttu-id="4f4a9-126">たとえば、数量は小数点以下 4 桁で維持する必要があるが、時間は引き続き小数点以下 2 桁で維持する必要がある場合は、小数点以下 4 桁にデータ型を拡張する必要があります。</span><span class="sxs-lookup"><span data-stu-id="4f4a9-126">For example, if quantities need to be maintained with four decimal points, but hours still need to be maintained with two decimal points, then the data type should be extended to four decimal points.</span></span>


## <a name="unit-amounts"></a><span data-ttu-id="4f4a9-127">ユニット金額</span><span class="sxs-lookup"><span data-stu-id="4f4a9-127">Unit amounts</span></span>
<span data-ttu-id="4f4a9-128">既定では、価格、明細行の割引金額、請求金額の明細行の金額を含むユニット金額は、小数点以下最大 2 桁で維持することができます。</span><span class="sxs-lookup"><span data-stu-id="4f4a9-128">By default, unit amounts including prices, line discount amounts, and line charge amounts can be maintained with a maximum of two decimals.</span></span>

<span data-ttu-id="4f4a9-129">小数点以下の精度が最大 6 桁のユニット金額を入力、管理、および表示する必要がある場合、**UnitAmountCur**、**UnitAmountMST**、**CostPriceNonMonetary** 拡張データ型の小数点の精度を拡張する必要があります。</span><span class="sxs-lookup"><span data-stu-id="4f4a9-129">If you require the ability enter, maintain, and view unit amounts with a maximum precision of six decimal points, you must extend the decimal point precision of the **UnitAmountCur**, **UnitAmountMST**, and **CostPriceNonMonetary** extended data types.</span></span>

<span data-ttu-id="4f4a9-130">小数点以下 4 桁以上の精度が必要な場合、PriceRoundOff 拡張データ型も拡張する必要があります。</span><span class="sxs-lookup"><span data-stu-id="4f4a9-130">If you require a decimal point precision of more than four, you should also extend the PriceRoundOff extended data type.</span></span>

### <a name="overloaded-data-types"></a><span data-ttu-id="4f4a9-131">オーバーロード拡張データ型</span><span class="sxs-lookup"><span data-stu-id="4f4a9-131">Overloaded data types</span></span>
<span data-ttu-id="4f4a9-132">ユニット数量データとその他のデータ型の両方を保管するのに使用される 5 つの拡張データ型があります。</span><span class="sxs-lookup"><span data-stu-id="4f4a9-132">There are five extended data types that are used for storing both unit amount data and other types of data.</span></span>

<span data-ttu-id="4f4a9-133">**PriceDiscAmount** 拡張データ型は、金額とユニット数量を格納して表示するために使用します。</span><span class="sxs-lookup"><span data-stu-id="4f4a9-133">The **PriceDiscAmount** extended data type is used for storing and presenting amounts and unit amounts.</span></span> <span data-ttu-id="4f4a9-134">**PriceDiscAmount** 拡張データ型は、金額とユニット数量の両方に対して必要な小数点以下の最大金額に拡張する必要があります。</span><span class="sxs-lookup"><span data-stu-id="4f4a9-134">The **PriceDiscAmount** extended data type should be extended to the maximum amount of required decimals points for both amounts and unit amounts.</span></span>
<span data-ttu-id="4f4a9-135">たとえば、金額は小数点以下 3 桁で維持する必要があるが、ユニット金額は小数点以下 4 桁で維持する必要がある場合は、小数点以下 4 桁にデータ型を拡張する必要があります。</span><span class="sxs-lookup"><span data-stu-id="4f4a9-135">For example, if amounts need to be maintained with three decimal points, but unit amounts need to be maintained with four decimal points, the data type should be extended to four decimal points.</span></span>

<span data-ttu-id="4f4a9-136">**MCRRoyaltyValue**、**PdsRebateValue**、**TAMRebateValue**、および **MarkupValue** 拡張データ型は、金額、ユニット金額、割合を格納して表示するのに使用されます。</span><span class="sxs-lookup"><span data-stu-id="4f4a9-136">The **MCRRoyaltyValue**, **PdsRebateValue**, **TAMRebateValue**, and **MarkupValue** extended data types are used for storing and presenting amounts, unit amounts, and percentages.</span></span>
<span data-ttu-id="4f4a9-137">拡張データ型は、金額、ユニット数量、割合に対して必要な小数点以下の最大金額に拡張する必要があります。</span><span class="sxs-lookup"><span data-stu-id="4f4a9-137">The extended data types should be extended to the maximum amount of required decimal points for amounts, unit amounts, and percentages.</span></span> <span data-ttu-id="4f4a9-138">たとえば、金額は小数点以下 3 桁で維持する必要があるが、ユニット金額は小数点以下 4 桁で維持する必要があり、割合は小数点以下 2 桁で維持する必要がある場合は、小数点以下 4 桁にデータ型を拡張する必要があります。</span><span class="sxs-lookup"><span data-stu-id="4f4a9-138">For example, if amounts need to be maintained with three decimal points, but unit amounts need to be maintained with four decimal points and percentages should remain maintained with two decimal points, then the data type should be extended to four decimal points.</span></span>

## <a name="amounts"></a><span data-ttu-id="4f4a9-139">金額</span><span class="sxs-lookup"><span data-stu-id="4f4a9-139">Amounts</span></span>
<span data-ttu-id="4f4a9-140">既定では、ユニット金額を含む金額は、小数点以下最大 2 桁で管理できます。</span><span class="sxs-lookup"><span data-stu-id="4f4a9-140">Amounts, including unit amounts, can be maintained with a maximum of two decimals by default.</span></span>

<span data-ttu-id="4f4a9-141">小数点以下の精度が最大 6 桁のユニット金額を含む金額を入力、管理、および表示できる必要がある場合、**Amount**、**AmountMST**、**CostAmountNonMonetary** 拡張データ型の小数点の精度を拡張する必要があります。</span><span class="sxs-lookup"><span data-stu-id="4f4a9-141">If you require the ability to enter, maintain, and view amounts including unit amounts with a precision of maximum six decimal points, you must extend the decimal point precision of the **Amount**, **AmountMST**, and **CostAmountNonMonetary** extended data types.</span></span>
<span data-ttu-id="4f4a9-142">金額以外ユニット金額にさまざまな精度が必要な場合は、ユニット金額の小数点以下の精度を拡張する方法の説明に従います。</span><span class="sxs-lookup"><span data-stu-id="4f4a9-142">If you require a different precision for unit amounts other than for amount, follow the description for how to extend the decimal point precision for unit amounts.</span></span>

### <a name="overloaded-data-types"></a><span data-ttu-id="4f4a9-143">オーバーロード拡張データ型</span><span class="sxs-lookup"><span data-stu-id="4f4a9-143">Overloaded data types</span></span>
<span data-ttu-id="4f4a9-144">金額データとその他のデータ型の両方を保管するのに使用される 3 つの拡張データ型があります。</span><span class="sxs-lookup"><span data-stu-id="4f4a9-144">There are three extended data types that are used for storing amount data and other types of data.</span></span> <span data-ttu-id="4f4a9-145">つまり、個別に拡張する必要があります。</span><span class="sxs-lookup"><span data-stu-id="4f4a9-145">This means that they must be extended separately.</span></span>

<span data-ttu-id="4f4a9-146">**AmountQty** 拡張データ型は、金額と数量を格納して表示するために使用します。</span><span class="sxs-lookup"><span data-stu-id="4f4a9-146">The **AmountQty** extended data type is used for storing and presenting amounts and quantities.</span></span> <span data-ttu-id="4f4a9-147">**AmountQty** 拡張データ型は、金額と数量の両方に対して必要な小数点以下の最大金額に拡張する必要があります。</span><span class="sxs-lookup"><span data-stu-id="4f4a9-147">The **AmountQty** extended data type should be extended to the maximum amount of required decimals for both amounts and quantities.</span></span> <span data-ttu-id="4f4a9-148">たとえば、金額は小数点以下 3 桁で維持する必要があるが、数量は引き続き 2 桁で維持する必要がある場合は、小数点以下 3 桁にデータ型を拡張する必要があります。</span><span class="sxs-lookup"><span data-stu-id="4f4a9-148">For example, if amounts need to be maintained with three decimal points, but quantities still need to be maintained with two, then the data type should be extended to three decimal points.</span></span>

<span data-ttu-id="4f4a9-149">**PriceDiscAmount** 拡張データ型は、金額とユニット数量を格納して表示するために使用します。</span><span class="sxs-lookup"><span data-stu-id="4f4a9-149">The **PriceDiscAmount** extended data type is used for storing and presenting amounts and unit amounts.</span></span> <span data-ttu-id="4f4a9-150">**PriceDiscAmount** 拡張データ型は、金額とユニット数量に対して必要な小数点以下の最大金額に拡張する必要があります。</span><span class="sxs-lookup"><span data-stu-id="4f4a9-150">The **PriceDiscAmount** extended data type should be extended to the maximum amount of required decimals points for amounts and unit amounts.</span></span>
<span data-ttu-id="4f4a9-151">たとえば、金額は小数点以下 3 桁で維持する必要があるが、ユニット金額は小数点以下 4 桁で維持する必要がある場合は、小数点以下 4 桁にデータ型を拡張する必要があります。</span><span class="sxs-lookup"><span data-stu-id="4f4a9-151">For example, if amounts need to be maintained with three decimal points, but unit amounts need to be maintained with four decimal points, then the data type should be extended to four decimal points.</span></span>

<span data-ttu-id="4f4a9-152">**MarkupValue** 拡張データ型は、金額、ユニット数量、割合を格納して表示するために使用します。</span><span class="sxs-lookup"><span data-stu-id="4f4a9-152">The **MarkupValue** extended data type is used for storing and presenting amounts, unit amounts, and percentages.</span></span>
<span data-ttu-id="4f4a9-153">拡張データ型は、金額、ユニット数量、割合に対して必要な小数点以下の最大金額に拡張する必要があります。</span><span class="sxs-lookup"><span data-stu-id="4f4a9-153">The extended data types should be extended to the maximum amount of required decimals points for amounts, unit amounts, and percentages.</span></span>
<span data-ttu-id="4f4a9-154">たとえば、金額は小数点以下 3 桁で維持する必要があり、ユニット金額は小数点以下 4 桁で維持する必要があり、割合は小数点以下 2 桁で維持する必要がある場合は、小数点以下 4 桁にデータ型を拡張する必要があります。</span><span class="sxs-lookup"><span data-stu-id="4f4a9-154">For example, if amounts need to be maintained with three decimal points, unit amounts need to be maintained with four decimal points, and percentages should remain with two decimal points, then the data type should be extended to four decimal points.</span></span>

