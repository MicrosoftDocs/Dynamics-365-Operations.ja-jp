---
title: NUMBERVALUE ER 機能
description: この記事では、NUMBERVALUE 電子申告 (ER) 関数の使用方法についての情報を提供します。
author: NickSelin
ms.date: 12/05/2019
ms.prod: ''
ms.technology: ''
ms.search.form: ERDataModelDesigner, ERExpressionDesignerFormula, ERMappedFormatDesigner, ERModelMappingDesigner
audience: Application User, IT Pro
ms.reviewer: kfend
ms.custom: 58771
ms.assetid: 24223e13-727a-4be6-a22d-4d427f504ac9
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 9701fe7a1ce2a96fa5fa8df8aeda125c861a117a
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/03/2022
ms.locfileid: "8871530"
---
# <a name="numbervalue-er-function"></a>NUMBERVALUE ER 機能

[!include [banner](../includes/banner.md)]

`NUMBERVALUE` 関数は、指定された *文字列* 値から変換された *実数* 値を返します。 変換時に、指定された 10 進と桁区切り記号が考慮されます。

## <a name="syntax"></a>構文

```vb
NUMBERVALUE (text, decimal separator, digit grouping separator)
```

## <a name="arguments"></a>引数

`text`: *文字列*

*実数* の数に変換する必要があるテキスト値。

`decimal separator`: 文字列

少数桁の区切り文字。 10 進数の整数部と小数点以下を区切るのに使用されます。

`digit grouping separator`: *文字列*

桁区切り記号。 千の位の区切り記号として使用されます。

## <a name="return-values"></a>戻り値

*実績*

結果数値。

## <a name="example"></a>例

`NUMBERVALUE( "1 234,56", ",", " ")` は、**1234.56** を返します。

## <a name="additional-resources"></a>追加リソース

[型変換関数](er-functions-category-type-conversion.md)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]