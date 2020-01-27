---
title: ROUND ER 関数
description: このトピックでは、ROUND 電子申告 (ER) 関数の使用方法についての情報を提供します。
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
ms.search.scope: Core, Operations
ms.custom: 58771
ms.assetid: 24223e13-727a-4be6-a22d-4d427f504ac9
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: c9384d5975e4a25d18ff741f87431daa4b0bbd7e
ms.sourcegitcommit: 36857283d70664742c8c04f426b231c42daf4ceb
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 12/20/2019
ms.locfileid: "2917077"
---
# <a name="ROUND">ROUND ER 関数</a>

[!include [banner](../includes/banner.md)]

`ROUND` 関数は、指定された数を指定された小数点以下の桁数に丸めてから、*実数*値として返します。

## <a name="syntax"></a>構文

```
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

`decimals` 引数の値が **0** (ゼロ) の場合、指定された数字は最も近い整数に丸められます。

`decimals` 引数の値が 0 (ゼロ) より小さい場合、指定された数字は小数点より左で丸められます。

## <a name="example-1"></a>例 1

`ROUND (1200.767, 2)` は、小数点第 2 位で四捨五入され、**1200.77** を返します。

## <a name="example-2"></a>例 2

`ROUND (1200.767, -3)` は、1,000 の最も近い倍数に四捨五入され、**1000** を返します。

## <a name="additional-resources"></a>追加リソース

[算術関数](er-functions-category-mathematical.md)
