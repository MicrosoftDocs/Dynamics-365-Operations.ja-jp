---
title: POWER ER 関数
description: このトピックでは、POWER 電子申告 (ER) 関数使用方法についての情報を提供します。
author: NickSelin
ms.date: 12/17/2019
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
ms.openlocfilehash: ce1f4c735f815c46003ded35156bb47febf177a3
ms.sourcegitcommit: 074b6e212d19dd5d84881d1cdd096611a18c207f
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 03/31/2021
ms.locfileid: "5750159"
---
# <a name="power-er-function"></a>POWER ER 関数

[!include [banner](../includes/banner.md)]

`POWER` 関数は、指定された正の数に指定された累乗をした結果を表す *実数* 値を返します。

## <a name="syntax"></a>構文

```vb
POWER (number, power)
```

## <a name="arguments"></a>引数

`number`: *実数* または *整数*

指定された累乗をする必要がある数値。

`power`: *実数* または *整数*

指定され累乗を表す数値。

## <a name="return-values"></a>戻り値

*実績*

結果数値。

## <a name="example-1"></a>例 1

`POWER (10, 2)` は、**100** を返します。

## <a name="example-2"></a>例 2

`POWER (4, 0.5)` は、**2** を返します。

## <a name="additional-resources"></a>追加リソース

[算術関数](er-functions-category-mathematical.md)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]