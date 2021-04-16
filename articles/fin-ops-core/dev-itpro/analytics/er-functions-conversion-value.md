---
title: VALUE ER 関数
description: このトピックでは、VALUE 電子申告 (ER) 関数の使用方法についての情報を提供します。
author: NickSelin
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
ms.openlocfilehash: 2252823d98b63d36d9bb195696abef34ac9c98b6
ms.sourcegitcommit: 074b6e212d19dd5d84881d1cdd096611a18c207f
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 03/31/2021
ms.locfileid: "5752583"
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