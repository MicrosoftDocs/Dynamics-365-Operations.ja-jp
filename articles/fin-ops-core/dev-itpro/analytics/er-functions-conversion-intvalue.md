---
title: INTVALUE ER 関数
description: この記事では、INTVALUE 電子申告 (ER) 関数の使用方法についての情報を提供します。
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
ms.openlocfilehash: eccee60c40bfc96f1fd93e7177207a1dd1888dc6
ms.sourcegitcommit: 87e727005399c82cbb6509f5ce9fb33d18928d30
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 08/12/2022
ms.locfileid: "9282624"
---
# <a name="intvalue-er-function"></a>INTVALUE ER 関数

[!include [banner](../includes/banner.md)]

`INTVALUE` 関数は、指定された文字列を表す *Int* 値を返します。

## <a name="syntax-1"></a>構文 1

```vb
INTVALUE (text)
```

## <a name="syntax-2"></a>構文 2

```vb
INTVALUE (number)
```

## <a name="arguments"></a>引数

`text`: *文字列*

*Int* 数に変換する必要があるテキスト値。

`number`: *実数* または *整数*

*Int* 数に変換する必要がある数値の *実数* または *整数* 値。

## <a name="return-values"></a>戻り値

*Int*

結果数値。

## <a name="usage-notes"></a>使用上の注意

任意の小数点以下の桁数が切り捨てられます。

## <a name="example-1"></a>例 1

`INTVALUE ("100.77")` は、*Int* の値 **100** を返します。

## <a name="example-2"></a>例 2

`INTVALUE (-100.77)` は、*Int* の値 **-100** を返します。

## <a name="additional-resources"></a>追加リソース

[型変換関数](er-functions-category-type-conversion.md)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
