---
title: INT64VALUE ER 関数
description: このトピックでは、INT64VALUE 電子申告 (ER) 関数の使用方法についての情報を提供します。
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
ms.openlocfilehash: 89a26e867579bcb34a9bae33fa0b98e1ecfe9995
ms.sourcegitcommit: 074b6e212d19dd5d84881d1cdd096611a18c207f
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 03/31/2021
ms.locfileid: "5755399"
---
# <a name="int64value-er-function"></a>INT64VALUE ER 関数

[!include [banner](../includes/banner.md)]

`INT64VALUE` 関数は、指定された文字列を表す *Int64* 値を返します。

## <a name="syntax-1"></a>構文 1

```vb
INT64VALUE (text)
```

## <a name="syntax-2"></a>構文 2

```vb
INT64VALUE (number)
```

## <a name="arguments"></a>引数

`text`: *文字列*

*Int64* 数に変換する必要があるテキスト値。

`number`: *実数* または *整数*

*Int64* 数に変換する必要がある数値の *実数* または *整数* 値。

## <a name="return-values"></a>戻り値

*Int64*

結果数値。

## <a name="usage-notes"></a>使用上の注意

任意の小数点以下の桁数が切り捨てられます。

## <a name="example-1"></a>例 1

`INT64VALUE ("22565422744")` は、*Int64* の値 **22565422744** を返します。

## <a name="example-2"></a>例 2

`INT64VALUE ( VALUE("22565422744.77"))` は、*Int64* の値 **22565422744** を返します。

## <a name="additional-resources"></a>追加リソース

[型変換関数](er-functions-category-type-conversion.md)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]