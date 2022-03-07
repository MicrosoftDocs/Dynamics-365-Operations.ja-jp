---
title: WEEKNUM ER 関数
description: このトピックでは、WEEKNUM 電子申告 (ER) 関数の使用方法についての情報を提供します。
author: NickSelin
ms.date: 12/03/2021
ms.prod: ''
ms.technology: ''
ms.search.form: ERDataModelDesigner, ERExpressionDesignerFormula, ERMappedFormatDesigner, ERModelMappingDesigner
audience: Application User, IT Pro
ms.reviewer: kfend
ms.custom: 58771
ms.assetid: ''
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2021-12-03
ms.dyn365.ops.version: AX 10.0.24
ms.openlocfilehash: fe36d4142b6e4922e2cbca09bb0ca9f68f6680a0
ms.sourcegitcommit: c85eac17fbfbd311288b50664f9e2bae101c1fe6
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 12/03/2021
ms.locfileid: "7891344"
---
# <a name="weeknum-er-function"></a>WEEKNUM ER 関数

[!include [banner](../includes/banner.md)]
[!include [banner](../includes/preview-banner.md)]

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
