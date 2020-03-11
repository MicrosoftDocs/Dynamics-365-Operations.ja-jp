---
title: ABS ER 関数
description: このトピックでは、ABS 電子申告 (ER) 関数の使用方法についての情報を提供します。
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
ms.openlocfilehash: 214fb2808f024487795f27de45de1d4de8cead2d
ms.sourcegitcommit: 3c1eb3d89c6ab9bd70b806ca42ef9df74cf850bc
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 02/12/2020
ms.locfileid: "3041656"
---
# <a name="ABS">ABS ER 関数</a>

[!include [banner](../includes/banner.md)]

`ABS` 関数は、指定された数の絶対値 (係数) を*実数*値として返します。 つまり、符号のない数値を返します。

## <a name="syntax"></a>構文

```vb
ABS (number)
```

## <a name="arguments"></a>引数

`number`: *実数*

係数を求める数値。

## <a name="return-values"></a>戻り値

*実績*

結果数値。

## <a name="example"></a>例

`ABS (-1)` は、**1** を返します。

## <a name="additional-resources"></a>追加リソース

[算術関数](er-functions-category-mathematical.md)
