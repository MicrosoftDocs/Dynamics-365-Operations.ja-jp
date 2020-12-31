---
title: ROUNDDOWN ER 関数
description: このトピックでは、ROUNDDOWN 電子申告 (ER) 関数の使用方法についての情報を提供します。
author: NickSelin
manager: kfend
ms.date: 12/17/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-platform
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
ms.openlocfilehash: 9221476c1c12a7cc3fe2367cdee3ad44e5cbe381
ms.sourcegitcommit: 659375c4cc7f5524cbf91cf6160f6a410960ac16
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 12/05/2020
ms.locfileid: "4686885"
---
# <a name="rounddown-er-function"></a>ROUNDDOWN ER 関数

[!include [banner](../includes/banner.md)]

`ROUNDDOWN` 関数は、指定された数を指定された小数点以下の桁数に切り下げてから、*実数* 値として返します。

## <a name="syntax"></a>構文

```vb
ROUNDDOWN (number, decimals)
```

## <a name="arguments"></a>引数

`number`: *実数*

切り下げる必要のある数値。

`decimals`: *整数*

小数点以下の桁数を表す数値。

## <a name="return-values"></a>戻り値

*実績*

結果数値。

## <a name="usage-notes"></a>使用上の注意

この関数は、[ROUND](er-functions-mathematical-round.md) のように機能しますが、常に指定した数字を (ゼロ方向に) 切り捨てます。

## <a name="example-1"></a>例 1

`ROUNDDOWN (1200.767, 2)` は、小数点第 2 位で切り下げられ、**1200.76** を返します。 

## <a name="example-2"></a>例 2

`ROUNDDOWN (1700.767, -3)` は、1,000 の最も近い倍数に切り下げられ、**1000** を返します。

## <a name="additional-resources"></a>追加リソース

[算術関数](er-functions-category-mathematical.md)
