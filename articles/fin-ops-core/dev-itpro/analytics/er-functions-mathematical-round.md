---
title: ROUND ER 関数
description: この記事では、ROUND 電子申告 (ER) 関数の使用方法についての情報を提供します。
author: kfend
ms.date: 10/21/2020
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
ms.openlocfilehash: 57d41ed92a5577fdc5fffeccef2834e9b6fb5197
ms.sourcegitcommit: 87e727005399c82cbb6509f5ce9fb33d18928d30
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 08/12/2022
ms.locfileid: "9286062"
---
# <a name="round-er-function"></a>ROUND ER 関数

[!include [banner](../includes/banner.md)]

`ROUND` 関数は、指定された数を指定された小数点以下の桁数に丸めてから、*実数* 値として返します。

## <a name="syntax"></a>構文

```vb
ROUND (number, decimals)
```

## <a name="arguments"></a>引数

`number`: *実数*

丸める必要のある数値。

`decimals`: *整数*

小数点以下の桁数を表す数値。

## <a name="return-values"></a>戻り値

*実績*

結果数値。

## <a name="usage-notes"></a>使用上の注意

`decimals` 引数の値が 0 (ゼロ) より大きい場合、指定された数字は小数点以下の桁数に丸められます。

`decimals` 引数の値が **0** (ゼロ) の場合、指定された数字は最も近い偶数に丸められます。

`decimals` 引数の値が 0 (ゼロ) より小さい場合、指定された数字は小数点より左で丸められます。

## <a name="example-1"></a>例 1

`ROUND (1200.767, 2)` は、小数点第 2 位で四捨五入され、**1200.77** を返します。

## <a name="example-2"></a>例 2

`ROUND (1200.767, -3)` は、1,000 の最も近い倍数に四捨五入され、**1000** を返します。

## <a name="example-3"></a>例 3

`ROUND (1200.5, 0)` は、最も近い偶数に丸めて **1200** を返しますが、`ROUND (1201.5, 0)` は同じ処理を行って **1202** を返します。

## <a name="additional-resources"></a>追加リソース

[算術関数](er-functions-category-mathematical.md)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
