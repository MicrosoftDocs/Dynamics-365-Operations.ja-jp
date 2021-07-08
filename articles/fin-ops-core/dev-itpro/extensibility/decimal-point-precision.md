---
title: 選択したデータ型の小数点以下の精度の拡張
description: このトピックでは、選択したデータ型の小数点以下の精度の拡張方法について説明します。
author: MichaelFruergaardPontoppidan
ms.date: 09/24/2019
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Developer
ms.reviewer: rhaertle
ms.custom: 89563
ms.assetid: 8DA4DA85-0C2D-4CAF-B350-DAC9C1BE4DF9
ms.search.region: Global
ms.author: mfp
ms.search.validFrom: 2018-10-10
ms.dyn365.ops.version: Platform update 21
ms.openlocfilehash: abed458980fe19d68e0cf65323c3ba1ff5bd5104
ms.sourcegitcommit: 15aacd0e109b05c7281407b5bba4e6cd99116c28
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/10/2021
ms.locfileid: "6224048"
---
# <a name="extending-decimal-point-precision-for-selected-data-types"></a><span data-ttu-id="3c9e5-103">選択したデータ型の小数点以下の精度の拡張</span><span class="sxs-lookup"><span data-stu-id="3c9e5-103">Extending decimal point precision for selected data types</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="3c9e5-104">このトピックでは、選択したデータ型の小数点以下の精度の拡張方法について説明します。</span><span class="sxs-lookup"><span data-stu-id="3c9e5-104">This topic describes how to extend decimal point precision for selected data types.</span></span> <span data-ttu-id="3c9e5-105">特定のシナリオの小数点精度を変更するため、Real 型の特定の拡張データ型の拡張機能を作成することができます。</span><span class="sxs-lookup"><span data-stu-id="3c9e5-105">You can create extensions of specific extended data types of the type Real, to change the decimal point precision for certain scenarios.</span></span> <span data-ttu-id="3c9e5-106">小数点以下の桁数を変更するには、必要に応じて **NoOfDecimals** プロパティを変更します。</span><span class="sxs-lookup"><span data-stu-id="3c9e5-106">To change the decimal point precision, change the **NoOfDecimals** property as needed.</span></span>

<span data-ttu-id="3c9e5-107">拡張データ型は階層型になっており、拡張されたデータ型から動作を継承します。</span><span class="sxs-lookup"><span data-stu-id="3c9e5-107">Extended data types are hierarchical and inherit behavior from the data type they extend.</span></span> <span data-ttu-id="3c9e5-108">1 つの拡張データ型の小数点以下の桁数を変更すると、すべての派生した拡張データ型の小数点以下の桁数に適用されます。</span><span class="sxs-lookup"><span data-stu-id="3c9e5-108">When changing the number of decimal places for one extended data type, the number of decimal places on all derived extended data types will follow.</span></span> <span data-ttu-id="3c9e5-109">つまり、**NoOfDecimalsIsExtensible** が False である拡張データ型が見つかった場合、小数点以下の桁数が広範囲に拡張される場合があるため、親拡張データ型を確認します。</span><span class="sxs-lookup"><span data-stu-id="3c9e5-109">In other words, if you find an extended data type where **NoOfDecimalsIsExtensible** is false, then check the parent extended data type, as the number of decimal places might be extensible in this wider scope.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="3c9e5-110">データベースの制約により、このトピックで説明する各データ型の小数点以下の精度は最大 6 桁です。</span><span class="sxs-lookup"><span data-stu-id="3c9e5-110">Due to database constraints, each of the data types described in this topic can have a maximum precision of six decimal places.</span></span>

## <a name="weight"></a><span data-ttu-id="3c9e5-111">太さ</span><span class="sxs-lookup"><span data-stu-id="3c9e5-111">Weight</span></span>

<span data-ttu-id="3c9e5-112">既定では、小数点以下最大 2 桁の重量データを維持できます。</span><span class="sxs-lookup"><span data-stu-id="3c9e5-112">Weight data can be maintained with a maximum of two decimal places by default.</span></span>

<span data-ttu-id="3c9e5-113">小数点以下の精度が最大 6 桁の重量データを入力、管理、および表示する必要がある場合、**WeightBase** 拡張データ型の小数点の精度を拡張する必要があります。</span><span class="sxs-lookup"><span data-stu-id="3c9e5-113">If you require the ability to enter, maintain, and view weight data with a maximum precision of six decimal places, you must extend the decimal point precision for the **WeightBase** extended data type.</span></span>

## <a name="product-width-height-and-depth"></a><span data-ttu-id="3c9e5-114">製品の幅、高さ、および奥行き</span><span class="sxs-lookup"><span data-stu-id="3c9e5-114">Product width, height and depth</span></span>

<span data-ttu-id="3c9e5-115">既定では、小数点以下最大 2 桁の現物分析コードを維持することができます。</span><span class="sxs-lookup"><span data-stu-id="3c9e5-115">These physical dimensions can be maintained with a maximum of two decimal places by default.</span></span>

<span data-ttu-id="3c9e5-116">小数点以下の精度が最大 6 桁のデータを入力、管理、および表示する必要がある場合、**InventWidth**、**InventHeight**、および **InventDepth** 拡張データ型の小数点の精度をそれぞれ拡張する必要があります。</span><span class="sxs-lookup"><span data-stu-id="3c9e5-116">If you require the ability to enter, maintain, and view this data with a maximum precision of six decimal places, you must extend the decimal point precision for the **InventWidth**, **InventHeight**, and **InventDepth** extended data types respectively.</span></span>

## <a name="product-quantity"></a><span data-ttu-id="3c9e5-117">製品数量</span><span class="sxs-lookup"><span data-stu-id="3c9e5-117">Product quantity</span></span>

<span data-ttu-id="3c9e5-118">既定では、小数点以下最大 2 桁の、製品の調達、消費、生産、保存、および販売に関連する数量データを管理できます。</span><span class="sxs-lookup"><span data-stu-id="3c9e5-118">Quantity data that is related to the procuring, consuming, producing, storing, and selling of products can be maintained with a maximum of two decimal places by default.</span></span>

<span data-ttu-id="3c9e5-119">小数点以下の精度が最大 6 桁の製品数量を入力、管理、および表示する必要がある場合、**ProductQuantity**、**CostQuantity**、**CAMMagnitude** 拡張データ型の小数点以下の精度を拡張する必要があります。</span><span class="sxs-lookup"><span data-stu-id="3c9e5-119">If you require the ability to enter, maintain, and view product quantities with a maximum precision of six decimal places, you must extend the decimal point precision of the **ProductQuantity**, **CostQuantity**, and **CAMMagnitude** extended data types.</span></span>

<span data-ttu-id="3c9e5-120">部品表、数式、および製造オーダーでは、既定では、小数点以下 4 桁の数量を管理できます。</span><span class="sxs-lookup"><span data-stu-id="3c9e5-120">Bill of materials, formulas, and production orders allow maintaining quantities with four decimal places by default.</span></span>

<span data-ttu-id="3c9e5-121">小数点以下 4 桁以上が必要な場合、**BOMProductQuantity** 拡張データ型の小数点以下の精度を拡張します。</span><span class="sxs-lookup"><span data-stu-id="3c9e5-121">If you require more than four decimal places, extend the decimal point precision for the **BOMProductQuantity** extended data type.</span></span>

### <a name="related-data-types"></a><span data-ttu-id="3c9e5-122">関連データ型</span><span class="sxs-lookup"><span data-stu-id="3c9e5-122">Related data types</span></span>

<span data-ttu-id="3c9e5-123">**価格単位**、**価格数量**、および **請求数量データ** は、製品数量とは別に拡張できます。</span><span class="sxs-lookup"><span data-stu-id="3c9e5-123">**Price unit**, **Price quantity**, and **Charge quantity data** can be extended independently from product quantities.</span></span>

<span data-ttu-id="3c9e5-124">**PriceUnit** 拡張データ型を拡張し、小数点の精度を、既定の価格単位 2 以外の値に変更できます。</span><span class="sxs-lookup"><span data-stu-id="3c9e5-124">You can extend the **PriceUnit** extended data type to change the decimal point precision to a value other than the default two for price units.</span></span>

<span data-ttu-id="3c9e5-125">**PriceQty** 拡張データ型を拡張し、小数点の精度を、既定の価格および請求数量 2 以外の値に変更できます。</span><span class="sxs-lookup"><span data-stu-id="3c9e5-125">You can extend the **PriceQty** extended data type to change the decimal point precision to a value other than the default two for price and charge quantities.</span></span>

### <a name="overloaded-data-types"></a><span data-ttu-id="3c9e5-126">オーバーロード拡張データ型</span><span class="sxs-lookup"><span data-stu-id="3c9e5-126">Overloaded data types</span></span>

<span data-ttu-id="3c9e5-127">数量データとその他のデータ型の両方を保管するのに使用される 2 つの拡張データ型があります。</span><span class="sxs-lookup"><span data-stu-id="3c9e5-127">There are two extended data types that are used for storing both quantity data and other types of data.</span></span> <span data-ttu-id="3c9e5-128">これらのデータ型は個別に拡張する必要があります。</span><span class="sxs-lookup"><span data-stu-id="3c9e5-128">These data types must be extended separately.</span></span>

<span data-ttu-id="3c9e5-129">**AmountQty** 拡張データ型は、金額と数量の両方を格納して表示するために使用します。</span><span class="sxs-lookup"><span data-stu-id="3c9e5-129">The **AmountQty** extended data type is used for storing and presenting both amounts and quantities.</span></span> <span data-ttu-id="3c9e5-130">**AmountQty** 拡張データ型は、金額と数量の両方に対して必要な小数点以下の最大桁数に拡張する必要があります。</span><span class="sxs-lookup"><span data-stu-id="3c9e5-130">The **AmountQty** extended data type should be extended to the maximum amount of required decimal places for both amounts and quantities.</span></span>

<span data-ttu-id="3c9e5-131">たとえば、金額は小数点以下 3 桁で管理する必要があるが、数量は引き続き小数点以下 2 桁で管理する必要がある場合は、小数点以下 3 桁にデータ型を拡張する必要があります。</span><span class="sxs-lookup"><span data-stu-id="3c9e5-131">For example, if amounts need to be maintained with three decimal places, but quantities still need to be maintained with two decimal places, then the data type should be extended to three decimal places.</span></span>

<span data-ttu-id="3c9e5-132">**ProductQuantityHourValue** 拡張データ型は、時間と数量の両方を格納して表示するために使用します。</span><span class="sxs-lookup"><span data-stu-id="3c9e5-132">The **ProductQuantityHourValue** extended data type is used for storing and presenting both hours and quantities.</span></span> <span data-ttu-id="3c9e5-133">**ProductQuantityHourValue** 拡張データ型は、時間と数量の両方に対して必要な小数点以下の最大桁数に拡張する必要があります。</span><span class="sxs-lookup"><span data-stu-id="3c9e5-133">The **ProductQuantityHourValue** extended data type should be extended to the maximum amount of required decimal places for both hours and quantities.</span></span>

<span data-ttu-id="3c9e5-134">たとえば、数量は小数点以下 4 桁で管理する必要があるが、時間は引き続き小数点以下 2 桁で管理する必要がある場合は、小数点以下 4 桁にデータ型を拡張する必要があります。</span><span class="sxs-lookup"><span data-stu-id="3c9e5-134">For example, if quantities need to be maintained with four decimal places, but hours still need to be maintained with two decimal places, then the data type should be extended to four decimal places.</span></span>

## <a name="unit-amounts"></a><span data-ttu-id="3c9e5-135">ユニット金額</span><span class="sxs-lookup"><span data-stu-id="3c9e5-135">Unit amounts</span></span>

<span data-ttu-id="3c9e5-136">既定では、価格、明細行の割引金額、請求金額の明細行の金額を含むユニット金額は、小数点以下最大 2 桁で管理することができます。</span><span class="sxs-lookup"><span data-stu-id="3c9e5-136">By default, unit amounts including prices, line discount amounts, and line charge amounts can be maintained with a maximum of two decimal places.</span></span>

<span data-ttu-id="3c9e5-137">小数点以下の精度が最大 6 桁のユニット金額を入力、管理、および表示する必要がある場合、**UnitAmountCur**、**UnitAmountMST**、**CostPriceNonMonetary** 拡張データ型の小数点の精度を拡張する必要があります。</span><span class="sxs-lookup"><span data-stu-id="3c9e5-137">If you require the ability enter, maintain, and view unit amounts with a maximum precision of six decimal places, you must extend the decimal point precision of the **UnitAmountCur**, **UnitAmountMST**, and **CostPriceNonMonetary** extended data types.</span></span>

<span data-ttu-id="3c9e5-138">小数点以下 4 桁以上の精度が必要な場合、PriceRoundOff 拡張データ型も拡張する必要があります。</span><span class="sxs-lookup"><span data-stu-id="3c9e5-138">If you require a decimal point precision of more than four, you should also extend the PriceRoundOff extended data type.</span></span>

### <a name="overloaded-data-types"></a><span data-ttu-id="3c9e5-139">オーバーロード拡張データ型</span><span class="sxs-lookup"><span data-stu-id="3c9e5-139">Overloaded data types</span></span>

<span data-ttu-id="3c9e5-140">ユニット数量データとその他のデータ型の両方を保管するのに使用される 5 つの拡張データ型があります。</span><span class="sxs-lookup"><span data-stu-id="3c9e5-140">There are five extended data types that are used for storing both unit amount data and other types of data.</span></span>

<span data-ttu-id="3c9e5-141">**PriceDiscAmount** 拡張データ型は、金額とユニット数量を格納して表示するために使用します。</span><span class="sxs-lookup"><span data-stu-id="3c9e5-141">The **PriceDiscAmount** extended data type is used for storing and presenting amounts and unit amounts.</span></span> <span data-ttu-id="3c9e5-142">**PriceDiscAmount** 拡張データ型は、金額とユニット数量の両方に対して必要な小数点以下の最大金額に拡張する必要があります。</span><span class="sxs-lookup"><span data-stu-id="3c9e5-142">The **PriceDiscAmount** extended data type should be extended to the maximum amount of required decimal places for both amounts and unit amounts.</span></span>

<span data-ttu-id="3c9e5-143">たとえば、金額は小数点以下 3 桁で管理する必要があるが、ユニット金額は小数点以下 4 桁で管理する必要がある場合は、小数点以下 4 桁にデータ型を拡張する必要があります。</span><span class="sxs-lookup"><span data-stu-id="3c9e5-143">For example, if amounts need to be maintained with three decimal places, but unit amounts need to be maintained with four decimal places, the data type should be extended to four decimal places.</span></span>

<span data-ttu-id="3c9e5-144">**MCRRoyaltyValue**、**PdsRebateValue**、**TAMRebateValue**、および **MarkupValue** 拡張データ型は、金額、ユニット金額、割合を格納して表示するのに使用されます。</span><span class="sxs-lookup"><span data-stu-id="3c9e5-144">The **MCRRoyaltyValue**, **PdsRebateValue**, **TAMRebateValue**, and **MarkupValue** extended data types are used for storing and presenting amounts, unit amounts, and percentages.</span></span>

<span data-ttu-id="3c9e5-145">拡張データ型は、金額、ユニット数量、割合に対して必要な小数点以下の最大金額に拡張する必要があります。</span><span class="sxs-lookup"><span data-stu-id="3c9e5-145">The extended data types should be extended to the maximum amount of required decimal places for amounts, unit amounts, and percentages.</span></span> <span data-ttu-id="3c9e5-146">たとえば、金額は小数点以下 3 桁で管理する必要があるが、ユニット金額は小数点以下 4 桁で管理する必要があり、割合は小数点以下 2 桁で管理する必要がある場合は、小数点以下 4 桁にデータ型を拡張する必要があります。</span><span class="sxs-lookup"><span data-stu-id="3c9e5-146">For example, if amounts need to be maintained with three decimal places, but unit amounts need to be maintained with four decimal places and percentages should remain maintained with two decimal places, then the data type should be extended to four decimal places.</span></span>

## <a name="amounts"></a><span data-ttu-id="3c9e5-147">金額</span><span class="sxs-lookup"><span data-stu-id="3c9e5-147">Amounts</span></span>

<span data-ttu-id="3c9e5-148">既定では、ユニット金額を含む金額は、小数点以下最大 2 桁で管理できます。</span><span class="sxs-lookup"><span data-stu-id="3c9e5-148">Amounts, including unit amounts, can be maintained with a maximum of two decimal places by default.</span></span>

<span data-ttu-id="3c9e5-149">小数点以下の精度が最大 6 桁のユニット金額を含む金額を入力、管理、および表示する必要がある場合、**Amount**、**AmountMST**、**CostAmountNonMonetary** 拡張データ型の小数点の精度を拡張する必要があります。</span><span class="sxs-lookup"><span data-stu-id="3c9e5-149">If you require the ability to enter, maintain, and view amounts including unit amounts with a precision of maximum six decimal places, you must extend the decimal point precision of the **Amount**, **AmountMST**, and **CostAmountNonMonetary** extended data types.</span></span>

<span data-ttu-id="3c9e5-150">金額以外ユニット金額にさまざまな精度が必要な場合は、ユニット金額の小数点以下の精度を拡張する方法の説明に従います。</span><span class="sxs-lookup"><span data-stu-id="3c9e5-150">If you require a different precision for unit amounts other than for amount, follow the description for how to extend the decimal point precision for unit amounts.</span></span>

### <a name="overloaded-data-types"></a><span data-ttu-id="3c9e5-151">オーバーロード拡張データ型</span><span class="sxs-lookup"><span data-stu-id="3c9e5-151">Overloaded data types</span></span>

<span data-ttu-id="3c9e5-152">金額データとその他のデータ型の両方を保管するのに使用される 3 つの拡張データ型があります。</span><span class="sxs-lookup"><span data-stu-id="3c9e5-152">There are three extended data types that are used for storing amount data and other types of data.</span></span> <span data-ttu-id="3c9e5-153">つまり、個別に拡張する必要があります。</span><span class="sxs-lookup"><span data-stu-id="3c9e5-153">This means that they must be extended separately.</span></span>

<span data-ttu-id="3c9e5-154">**AmountQty** 拡張データ型は、金額と数量を格納して表示するために使用します。</span><span class="sxs-lookup"><span data-stu-id="3c9e5-154">The **AmountQty** extended data type is used for storing and presenting amounts and quantities.</span></span> <span data-ttu-id="3c9e5-155">**AmountQty** 拡張データ型は、金額と数量の両方に対して必要な小数点以下の最大桁数に拡張する必要があります。</span><span class="sxs-lookup"><span data-stu-id="3c9e5-155">The **AmountQty** extended data type should be extended to the maximum amount of required decimal places for both amounts and quantities.</span></span>

<span data-ttu-id="3c9e5-156">たとえば、金額は小数点以下 3 桁で管理する必要があるが、数量は引き続き 2 桁で管理する必要がある場合は、小数点以下 3 桁にデータ型を拡張する必要があります。</span><span class="sxs-lookup"><span data-stu-id="3c9e5-156">For example, if amounts need to be maintained with three decimal places, but quantities still need to be maintained with two, then the data type should be extended to three decimal places.</span></span>

<span data-ttu-id="3c9e5-157">**PriceDiscAmount** 拡張データ型は、金額とユニット数量を格納して表示するために使用します。</span><span class="sxs-lookup"><span data-stu-id="3c9e5-157">The **PriceDiscAmount** extended data type is used for storing and presenting amounts and unit amounts.</span></span> <span data-ttu-id="3c9e5-158">**PriceDiscAmount** 拡張データ型は、金額とユニット数量の両方に対して必要な小数点以下の最大桁数に拡張する必要があります。</span><span class="sxs-lookup"><span data-stu-id="3c9e5-158">The **PriceDiscAmount** extended data type should be extended to the maximum amount of required decimal places for amounts and unit amounts.</span></span>

<span data-ttu-id="3c9e5-159">たとえば、金額は小数点以下 3 桁で管理する必要があるが、ユニット金額は小数点以下 4 桁で管理する必要がある場合は、小数点以下 4 桁にデータ型を拡張する必要があります。</span><span class="sxs-lookup"><span data-stu-id="3c9e5-159">For example, if amounts need to be maintained with three decimal places, but unit amounts need to be maintained with four decimal places, then the data type should be extended to four decimal places.</span></span>

<span data-ttu-id="3c9e5-160">**MarkupValue** 拡張データ型は、金額、ユニット数量、割合を格納して表示するために使用します。</span><span class="sxs-lookup"><span data-stu-id="3c9e5-160">The **MarkupValue** extended data type is used for storing and presenting amounts, unit amounts, and percentages.</span></span>

<span data-ttu-id="3c9e5-161">拡張データ型は、金額、ユニット数量、割合に対して必要な小数点以下の最大金額に拡張する必要があります。</span><span class="sxs-lookup"><span data-stu-id="3c9e5-161">The extended data types should be extended to the maximum amount of required decimal places for amounts, unit amounts, and percentages.</span></span>

<span data-ttu-id="3c9e5-162">たとえば、金額は小数点以下 3 桁で管理する必要があるが、ユニット金額は小数点以下 4 桁で管理する必要があり、割合は小数点以下 2 桁で管理する必要がある場合は、小数点以下 4 桁にデータ型を拡張する必要があります。</span><span class="sxs-lookup"><span data-stu-id="3c9e5-162">For example, if amounts need to be maintained with three decimal places, unit amounts need to be maintained with four decimal places, and percentages should remain with two decimal places, then the data type should be extended to four decimal places.</span></span>


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
