---
title: DAYS ER 関数
description: この記事では、DAYS 電子申告 (ER) 関数がどのように使用されるかについての情報を提供します。
author: kfend
ms.date: 12/04/2019
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
ms.openlocfilehash: a0c50e36bbf0c2bd999a17631e3e00d2feb162fd
ms.sourcegitcommit: 87e727005399c82cbb6509f5ce9fb33d18928d30
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 08/12/2022
ms.locfileid: "9268728"
---
# <a name="days-er-function"></a>DAYS ER 関数

[!include [banner](../includes/banner.md)]

`DAYS` 関数は、ある指定された日付から 2 番目の指定された日付までの日数を表す *整数* 値を返します。

## <a name="syntax"></a>構文

```vb
DAYS (date 1, date 2) as Integer
```

## <a name="arguments"></a>引数

`date 1`: *日付*

日数の計算の開始日を表す日付値。

`date 2`: *日付*

日数の計算の終了日を表す日付値。

## <a name="return-values"></a>戻り値

*整数*

結果数値。

## <a name="usage-notes"></a>使用上の注意

`DAYS` 関数は、最初の日付が 2 番目の日付より遅い場合は正の値を返し、最初の日付が 2 番目の日付と同じである場合は **0** (ゼロ) を返します。最初の日付が 2 番目の日付より早い場合は、負の値を返します。

## <a name="example"></a>例

`DAYS (TODAY (), DATEVALUE( DATETIMEFORMAT( ADDDAYS ( NOW(), 1), "yyyyMMdd"), "yyyyMMdd"))` は、**-1** を返します。

## <a name="additional-resources"></a>追加リソース

[日時の関数](er-functions-category-datetime.md)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
