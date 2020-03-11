---
title: DAYOFYEAR ER 関数
description: このトピックでは、DAYOFYEAR 電子申告 (ER) 関数の使用方法についての情報を提供します。
author: NickSelin
manager: kfend
ms.date: 12/04/2019
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
ms.openlocfilehash: d24aabb582151b0b357b64a988cc932a9c9f3cea
ms.sourcegitcommit: 3dede95a3b17de920bb0adcb33029f990682752b
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 02/18/2020
ms.locfileid: "3070670"
---
# <a name="DAYOFYEAR">DAYOFYEAR ER 関数</a>

[!include [banner](../includes/banner.md)]

`DAYOFYEAR` 関数は、1 月 1 日から指定された日までの日数を表す*整数*値を返します。

## <a name="syntax"></a>構文

```vb
DAYOFYEAR (date) as Integer
```

## <a name="arguments"></a>引数

`date`: *日付*

日数の計算に使用する日付を表す日付値。

## <a name="return-values"></a>戻り値

*整数*

結果数値。

## <a name="example-1"></a>例 1

`DAYOFYEAR (DATEVALUE ("01-03-2016", "dd-MM-yyyy"))` は、**61** を返します。

## <a name="example-2"></a>例 2

`DAYOFYEAR (DATEVALUE ("01-01-2016", "dd-MM-yyyy"))` は、**1** を返します。

## <a name="additional-resources"></a>追加リソース

[日時の関数](er-functions-category-datetime.md)
