---
title: ROUNDUP ER 関数
description: この記事では、ROUNDUP 電子申告 (ER) 関数の使用方法についての情報を提供します。
author: kfend
ms.date: 12/17/2019
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
ms.openlocfilehash: 5266b0f74f348d936bde8948770e48dbbf9bb4f5
ms.sourcegitcommit: 87e727005399c82cbb6509f5ce9fb33d18928d30
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 08/12/2022
ms.locfileid: "9268029"
---
# <a name="roundup-er-function"></a>ROUNDUP ER 関数

[!include [banner](../includes/banner.md)]

`ROUNDUP` 関数は、指定された数を指定された小数点以下の桁数に切り上げてから、*実数* 値として返します。

## <a name="syntax"></a>構文

```vb
ROUNDDOWN (number, decimals)
```

## <a name="arguments"></a>引数

`number`: *実数*

切り上げる必要のある数値。

`decimals`: *整数*

小数点以下の桁数を表す数値。

## <a name="return-values"></a>戻り値

*実績*

結果数値。

## <a name="usage-notes"></a>使用上の注意

この関数は、[ROUND](er-functions-mathematical-round.md) のように機能しますが、常に指定した数字を (ゼロとは逆方向に) 切り上げます。

## <a name="example-1"></a>例 1

`ROUNDUP (1200.763, 2)` は、小数点第 2 位で切り上げられ、**1200.77** を返します。

## <a name="example-2"></a>例 2

`ROUNDUP (1200.767, -3)` は、1,000 の最も近い倍数に切り上げられ、**2000** を返します。

## <a name="additional-resources"></a>追加リソース

[算術関数](er-functions-category-mathematical.md)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
