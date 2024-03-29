---
title: ADDDAYS ER 関数
description: この記事では、ADDDAYS 電子申告 (ER) 関数の使用方法についての情報を提供します。
author: kfend
ms.date: 12/03/2019
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
ms.openlocfilehash: 69273794def0dc52dc8e31615c319ccf5067fa77
ms.sourcegitcommit: 87e727005399c82cbb6509f5ce9fb33d18928d30
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 08/12/2022
ms.locfileid: "9274142"
---
# <a name="adddays-er-function"></a>ADDDAYS ER 関数

[!include [banner](../includes/banner.md)]

`ADDDAYS` 関数は、指定された開始日前後の指定された日数の *日時* 値を計算します。

## <a name="syntax"></a>構文

```vb
ADDDAYS (datetime, days)
```

## <a name="arguments"></a>引数

`datetime`: *日時*

開始日を表す日付/時刻値。

`days`: *整数*

`datetime` の前後の日数。

## <a name="return-values"></a>戻り値

*日時*

結果日時値。

## <a name="usage-notes"></a>使用上の注意

`days` の正の値は、未来の日付になります。 負の値は、過去の日付になります。

## <a name="example-1"></a>例 1

`ADDDAYS (NOW(), 7)` は、7 日後の日付と時刻を返します。

## <a name="example-2"></a>例 2

`ADDDAYS (NOW(), -3)` は、3 日前の日付と時刻を返します。

## <a name="additional-resources"></a>追加リソース

[日時の関数](er-functions-category-datetime.md)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
