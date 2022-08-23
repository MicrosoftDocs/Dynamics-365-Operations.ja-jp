---
title: WEEKNUM ER 関数
description: この記事では、WEEKNUM 電子申告 (ER) 関数の使用方法についての情報を提供します。
author: kfend
ms.date: 01/15/2022
ms.prod: ''
ms.technology: ''
audience: Application User, IT Pro
ms.reviewer: kfend
ms.search.region: Global
ms.author: filatovm
ms.search.validFrom: 2021-12-03
ms.dyn365.ops.version: AX 10.0.24
ms.custom: 58771
ms.assetid: ''
ms.search.form: ERDataModelDesigner, ERExpressionDesignerFormula, ERMappedFormatDesigner, ERModelMappingDesigner
ms.openlocfilehash: 4658f88b7e353e651177fad0c8636c5403be1256
ms.sourcegitcommit: 87e727005399c82cbb6509f5ce9fb33d18928d30
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 08/12/2022
ms.locfileid: "9268149"
---
# <a name="weeknum-er-function"></a>WEEKNUM ER 関数

[!include [banner](../includes/banner.md)]

`WEEKNUM` 関数は、指定された *[日付](er-formula-supported-data-types-primitive.md#date)* 値を含む 1 年のうちの週を表す *[整数](er-formula-supported-data-types-primitive.md#integer)* 値を返します。 この計算は、カレンダーの週と週の最初の日を定義するカルチャに依存したルールに基づいています。

## <a name="syntax"></a>構文

```vb
WEEKNUM (date, culture) as Integer
```

## <a name=""></a><a name="arguments">引数</a>

`date`: *日付*

年の週の計算に使用する日付を表す値です。

`culture`: *[文字列](er-formula-supported-data-types-primitive.md#string)*

計算に使用するカルチャ。 .NET [標準](/dotnet/api/system.globalization.cultureinfo.getcultures?view=net-5.0)でサポートされているカルチャ コードを使用することができます。

## <a name="return-values"></a>戻り値

*整数*

結果数値。

## <a name="usage-notes"></a>使用上の注意

年の週は、[ISO 8601](https://www.iso.org/iso-8601-date-and-time-format.html) 標準に基づいて計算されますが、この規格が国や地域で採用されている場合は、実行時にロケールが提供されます。 それ以外の場合は、国/地域固有の国の基準に基づいて計算されます。

サポート対象外の[カルチャ](#arguments) コードが実行時に `WEEKNUM` 関数の引数として指定されている場合、例外は分別されます。 カルチャ コードとして空白文字列が指定された場合は、英語のカントリーニュートラル カレンダーを使用して週番号が計算されます。

## <a name="examples"></a>例

`WEEKNUM (DATEVALUE ("01-01-2020", "de"))` は、**1** を返します。

`WEEKNUM (DATEVALUE ("01-01-2021", "de"))` は、**53** を返します。

`WEEKNUM (DATEVALUE ("01-01-2022", "de"))` は、**52** を返します。

`WEEKNUM (DATEVALUE ("01-01-2022", "ar"))` は、**21** を返します。

## <a name="additional-resources"></a>追加リソース

[日時の関数](er-functions-category-datetime.md)

[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
