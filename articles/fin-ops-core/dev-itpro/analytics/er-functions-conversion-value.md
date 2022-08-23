---
title: VALUE ER 関数
description: この記事では、VALUE 電子申告 (ER) 関数の使用方法についての情報を提供します。
author: kfend
ms.date: 12/05/2019
ms.prod: ''
ms.technology: ''
audience: Application User, IT Pro
ms.reviewer: kfend
ms.search.region: Global
ms.author: filatovm
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.custom: 58771
ms.assetid: 24223e13-727a-4be6-a22d-4d427f504ac9
ms.search.form: ERDataModelDesigner, ERExpressionDesignerFormula, ERMappedFormatDesigner, ERModelMappingDesigner
ms.openlocfilehash: 0a47637c47ca6c947451efa1230191779401b4e1
ms.sourcegitcommit: 87e727005399c82cbb6509f5ce9fb33d18928d30
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 08/12/2022
ms.locfileid: "9277665"
---
# <a name="value-er-function"></a>VALUE ER 関数

[!include [banner](../includes/banner.md)]

`VALUE` 関数は、指定された文字列から変換された *実数* 値を返します。

## <a name="syntax"></a>構文

```vb
VALUE (text)
```

## <a name="arguments"></a>引数

`text`: *文字列*

数値に変換する必要がある文字列値。

## <a name="return-values"></a>戻り値

*実績*

結果数値。

## <a name="usage-notes"></a>使用上の注意

コンマとドット (.) が小数点の区切り記号とみなされ、先頭のハイフン (-) は負の記号として使用されます。 他の数値以外の文字が指定された文字列に含まれている場合、実行時に例外がスローされます。

## <a name="example-1"></a>例 1

`VALUE ("1 234,56")` で例外がスローされました。

## <a name="example-2"></a>例 2

`VALUE ("1234,56")` は、**1234.56** を返します。

## <a name="additional-resources"></a>追加リソース

[型変換関数](er-functions-category-type-conversion.md)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
