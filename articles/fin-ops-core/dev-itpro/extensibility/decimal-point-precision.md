---
title: 選択したデータ型の小数点以下の精度の拡張
description: この記事では、選択したデータ型の小数点以下の精度の拡張方法について説明します。
author: MichaelFruergaardPontoppidan
ms.date: 09/24/2019
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Developer
ms.reviewer: josaw
ms.search.region: Global
ms.author: mfp
ms.search.validFrom: 2018-10-10
ms.dyn365.ops.version: Platform update 21
ms.custom: 89563
ms.assetid: 8DA4DA85-0C2D-4CAF-B350-DAC9C1BE4DF9
ms.openlocfilehash: c9265557c99a9efa5a3b290065e6abe43d22e502
ms.sourcegitcommit: 87e727005399c82cbb6509f5ce9fb33d18928d30
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 08/12/2022
ms.locfileid: "9270943"
---
# <a name="extending-number-of-decimals-for-selected-data-types"></a>選択したデータ型の小数点以下桁数の拡張

[!include [banner](../includes/banner.md)]

この記事では、選択したデータ型の小数点以下桁数の拡張方法について説明します。 特定のシナリオの小数点以下桁数を変更するため、Real 型の特定の拡張データ型の拡張機能を作成することができます。 小数点以下の桁数を変更するには、必要に応じて **NoOfDecimals** プロパティを変更します。

拡張データ型は階層型になっており、拡張されたデータ型から動作を継承します。 1 つの拡張データ型の小数点以下の桁数を変更すると、すべての派生した拡張データ型の小数点以下の桁数に適用されます。 つまり、**NoOfDecimalsIsExtensible** が False である拡張データ型が見つかった場合、小数点以下の桁数が広範囲に拡張される場合があるため、親拡張データ型を確認します。

> [!IMPORTANT]
> データベースの制約により、この記事で説明する各データ型の小数点以下の精度は最大 6 桁です。

## <a name="weight"></a>重量

既定では、小数点以下最大 2 桁の重量データを維持できます。

小数点以下が最大 6 桁の重量データを入力、管理、および表示する必要がある場合、**WeightBase** 拡張データ型の小数点以下桁数を拡張する必要があります。

## <a name="product-width-height-and-depth"></a>製品の幅、高さ、および奥行き

既定では、小数点以下最大 2 桁の現物分析コードを維持することができます。

小数点以下が最大 6 桁のデータを入力、管理、および表示する必要がある場合、**InventWidth**、**InventHeight**、および **InventDepth** 拡張データ型の小数点以下桁数をそれぞれ拡張する必要があります。

## <a name="product-quantity"></a>製品数量

既定では、小数点以下最大 2 桁の、製品の調達、消費、生産、保存、および販売に関連する数量データを管理できます。

小数点以下が最大 6 桁の製品数量を入力、管理、および表示する必要がある場合、**ProductQuantity**、**CostQuantity**、**CAMMagnitude** 拡張データ型の小数点以下桁数を拡張する必要があります。

部品表、数式、および製造オーダーでは、既定では、小数点以下 4 桁の数量を管理できます。

小数点以下 4 桁以上が必要な場合、**BOMProductQuantity** 拡張データ型の小数点以下桁数を拡張します。

### <a name="related-data-types"></a>関連データ型

**価格単位**、**価格数量**、および **請求数量データ** は、製品数量とは別に拡張できます。

**PriceUnit** 拡張データ型を拡張し、小数点以下桁数を、既定の価格単位 2 以外の値に変更できます。

**PriceQty** 拡張データ型を拡張し、小数点以下桁数を、既定の価格および請求数量 2 以外の値に変更できます。

### <a name="overloaded-data-types"></a>オーバーロード拡張データ型

数量データとその他のデータ型の両方を保管するのに使用される 2 つの拡張データ型があります。 これらのデータ型は個別に拡張する必要があります。

**AmountQty** 拡張データ型は、金額と数量の両方を格納して表示するために使用します。 **AmountQty** 拡張データ型は、金額と数量の両方に対して必要な小数点以下の最大桁数に拡張する必要があります。

たとえば、金額は小数点以下 3 桁で管理する必要があるが、数量は引き続き 2 桁で管理する必要がある場合は、小数点以下 3 桁にデータ型を拡張する必要があります。

**ProductQuantityHourValue** 拡張データ型は、時間と数量の両方を格納して表示するために使用します。 **ProductQuantityHourValue** 拡張データ型は、時間と数量の両方に対して必要な小数点以下の最大桁数に拡張する必要があります。

たとえば、数量は小数点以下 4 桁で管理する必要があるが、時間は引き続き 2 桁で管理する必要がある場合は、小数点以下 4 桁にデータ型を拡張する必要があります。

## <a name="unit-amounts"></a>ユニット金額

既定では、価格、明細行の割引金額、請求金額の明細行の金額を含むユニット金額は、小数点以下最大 2 桁で維持することができます。

小数点以下が最大 6 桁のユニット金額を入力、管理、および表示する必要がある場合、**UnitAmountCur**、**UnitAmountMST**、**CostPriceNonMonetary** 拡張データ型の小数点以下桁数を拡張する必要があります。

小数点以下 4 桁以上が必要な場合、PriceRoundOff 拡張データ型も拡張する必要があります。

### <a name="overloaded-data-types"></a>オーバーロード拡張データ型

ユニット数量データとその他のデータ型の両方を保管するのに使用される 5 つの拡張データ型があります。

**PriceDiscAmount** 拡張データ型は、金額とユニット数量を格納して表示するために使用します。 **PriceDiscAmount** 拡張データ型は、金額とユニット数量に対して必要な小数点以下の最大桁数に拡張する必要があります。

たとえば、金額は小数点以下 3 桁で管理する必要があるが、ユニット金額は小数点以下 4 桁で管理する必要がある場合は、小数点以下 4 桁にデータ型を拡張する必要があります。

**MCRRoyaltyValue**、**PdsRebateValue**、**TAMRebateValue**、および **MarkupValue** 拡張データ型は、金額、ユニット金額、割合を格納して表示するのに使用されます。

拡張データ型は、金額、ユニット数量、割合に対して必要な小数点以下の最大桁数に拡張する必要があります。 たとえば、金額は小数点以下 3 桁で管理する必要があるが、ユニット金額は小数点以下 4 桁で管理する必要があり、割合は小数点以下 2 桁で管理する必要がある場合は、小数点以下 4 桁にデータ型を拡張する必要があります。

## <a name="amounts"></a>金額

既定では、ユニット金額を含む金額は、小数点以下最大 2 桁で管理できます。

小数点以下の桁数が最大 6 桁のユニット金額を含む金額を入力、管理、および表示する必要がある場合、**Amount**、**AmountMST**、**CostAmountNonMonetary** 拡張データ型の小数点以下桁数を拡張する必要があります。

金額以外ユニット金額にさまざまな小数点以下桁数が必要な場合は、ユニット金額の小数点以下の桁数を拡張する方法の説明に従います。

### <a name="overloaded-data-types"></a>オーバーロード拡張データ型

金額データとその他のデータ型の両方を保管するのに使用される 3 つの拡張データ型があります。 つまり、個別に拡張する必要があります。

**AmountQty** 拡張データ型は、金額と数量を格納して表示するために使用します。 **AmountQty** 拡張データ型は、金額と数量の両方に対して必要な小数点以下の最大桁数に拡張する必要があります。

たとえば、金額は小数点以下 3 桁で管理する必要があるが、数量は引き続き 2 桁で管理する必要がある場合は、小数点以下 3 桁にデータ型を拡張する必要があります。

**PriceDiscAmount** 拡張データ型は、金額とユニット数量を格納して表示するために使用します。 **PriceDiscAmount** 拡張データ型は、金額とユニット数量の両方に対して必要な小数点以下の最大桁数に拡張する必要があります。

たとえば、金額は小数点以下 3 桁で管理する必要があるが、ユニット金額は小数点以下 4 桁で管理する必要がある場合は、小数点以下 4 桁にデータ型を拡張する必要があります。

**MarkupValue** 拡張データ型は、金額、ユニット数量、割合を格納して表示するために使用します。

拡張データ型は、金額、ユニット数量、割合に対して必要な小数点以下の最大桁数に拡張する必要があります。

たとえば、金額は小数点以下 3 桁で管理する必要があるが、ユニット金額は小数点以下 4 桁で管理する必要があり、割合は小数点以下 2 桁で管理する必要がある場合は、小数点以下 4 桁にデータ型を拡張する必要があります。


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
