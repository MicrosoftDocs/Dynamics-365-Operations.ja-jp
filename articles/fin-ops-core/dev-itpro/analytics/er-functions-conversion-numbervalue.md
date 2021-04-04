---
title: NUMBERVALUE ER 機能
description: このトピックでは、NUMBERVALUE 電子申告 (ER) 関数の使用方法についての情報を提供します。
author: NickSelin
manager: kfend
ms.date: 12/05/2019
ms.topic: article
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
ms.openlocfilehash: f542621c4bcc29e03d8c92b0c700e2c80c9846f6
ms.sourcegitcommit: 6cb174d1ec8b55946dca4db03d6a3c3f4c6fa2df
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 03/09/2021
ms.locfileid: "5561425"
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