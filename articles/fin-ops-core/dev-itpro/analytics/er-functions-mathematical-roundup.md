---
title: ROUNDUP ER 関数
description: このトピックでは、ROUNDUP 電子申告 (ER) 関数の使用方法についての情報を提供します。
author: NickSelin
ms.date: 12/17/2019
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
ms.openlocfilehash: 0d397a43712b349bc6eb5e88f38dbc7d8a5231a909f38608d45b4e08861b6b7b
ms.sourcegitcommit: 42fe9790ddf0bdad911544deaa82123a396712fb
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 08/05/2021
ms.locfileid: "6743242"
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