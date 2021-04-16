---
title: CONTAINS ER 関数
description: このトピックでは、CONTAINS 電子申告 (ER) 関数の使用方法についての情報を提供します。
author: NickSelin
ms.date: 02/11/2021
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-platform
ms.technology: ''
ms.search.form: ERDataModelDesigner, ERExpressionDesignerFormula, ERMappedFormatDesigner, ERModelMappingDesigner
audience: Application User, IT Pro
ms.reviewer: kfend
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2021-02-01
ms.dyn365.ops.version: AX 10.0.18
ms.openlocfilehash: c1d2d761a38d0edfb9abd439e0f710b336f54927
ms.sourcegitcommit: 074b6e212d19dd5d84881d1cdd096611a18c207f
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 03/31/2021
ms.locfileid: "5745428"
---
# <a name="contains-er-function"></a>CONTAINS ER 関数

[!include [banner](../includes/banner.md)]

`CONTAINS` 関数は、指定された入力に指定されたテキストが含まれるかどうかを決定します。 指定された入力が指定されたテキストを含む場合、関数は *TRUE* の **ブール値** を返します。 それ以外の場合は、**FALSE** の *ブール* 値が返されます。

## <a name="syntax"></a>構文

```vb
CONTAINS (input, search text)
```

## <a name="arguments"></a>引数

`input`: *文字列*

*文字列* 型または文字列定数のデータ ソースの項目の有効なパスで、2 番目の引数を含む可能性がある値です。

`search text`: *文字列*

*文字列* データ型または文字列定数のデータ ソースの項目の有効なパスで、1 番目の引数を含む可能性がある値です。

## <a name="return-values"></a>戻り値

*ブール値*

結果 *ブール* 値。

## <a name="usage-notes"></a>使用上の注意

この機能は、[Microsoft Dataverse](../data-entities/data-integration-cds.md) にアクセスするための適切なマッピングが [Regulatory Configuration Services](../../../finance/localizations/rcs-globalization-feature.md) で構成されている場合にのみ、[FILTER](er-functions-list-filter.md) 関数の条件式を指定をするのに使用できます。 それ以外の場合は、設計時に例外がスローされます。 受信するメッセージは、効率を向上させるために、`FILTER` 関数の代わりに [WHERE](er-functions-list-where.md) 関数を使用することを推奨しています。

## <a name="example-1"></a>例 1

`CONTAINS ("abc", "d")` 式は **FALSE** を返し、`CONTAINS ("abc", "C")` 式は **TRUE** を返します。

## <a name="example-2"></a>例 2

**モデル** データ ソースの **アドレス** フィールドの値が文字列 **DEU** を含む場合、`CONTAINS (model.InvoiceBase.Customer.PostalAddress.Address, "DEU")` 式は **TRUE** を返します。 それ以外の場合、**FALSE** を返します。

## <a name="additional-resources"></a>追加リソース

[論理関数](er-functions-category-logical.md)
