---
title: SESSIONTODAY ER 関数
description: この記事では、SESSIONTODAY 電子申告 (ER) 関数の使用方法についての情報を提供します。
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
ms.openlocfilehash: 0eeb4fcc449b565774cc79b767a2d157557d5b98
ms.sourcegitcommit: 87e727005399c82cbb6509f5ce9fb33d18928d30
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 08/12/2022
ms.locfileid: "9274892"
---
# <a name="sessiontoday-er-function"></a>SESSIONTODAY ER 関数

[!include [banner](../includes/banner.md)]

`SESSIONTODAY` 関数は、現在のアプリケーション セッションの日付を表す *日付* 値を返します。

## <a name="syntax"></a>構文

```vb
SESSIONTODAY ()
```

## <a name="return-values"></a>戻り値

*日付*

結果日付値。

## <a name="example"></a>例

`DATEFORMAT (SESSIONTODAY (), "d", "DE")` は、選択されたドイツのカルチャおよび指定された形式に基づいて、現在のアプリケーション セッションの日付 2015 年 12 月 24 日を、文字列 **"24-12-2015"** として返します。

## <a name="additional-resources"></a>追加リソース

[日時の関数](er-functions-category-datetime.md)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
