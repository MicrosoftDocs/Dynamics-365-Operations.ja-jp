---
title: 日付と時刻のカテゴリ内の ER 関数のリスト
description: この記事では、電子申告 (ER) でサポートされる日時の関数について説明します。
author: kfend
ms.date: 09/09/2021
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
ms.openlocfilehash: d77f41e10d927a9aae06b9ba0fc58ca237c071cd
ms.sourcegitcommit: 87e727005399c82cbb6509f5ce9fb33d18928d30
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 08/12/2022
ms.locfileid: "9291327"
---
# <a name="list-of-er-functions-in-the-date-and-time-category"></a>日付と時刻のカテゴリ内の ER 関数のリスト

[!include [banner](../includes/banner.md)]

電子報告 (ER) 日時の関数を使用して、日付と時刻の値から情報を抽出し、操作を実行できます。 この記事では、これらの関数の概要を示します。

## <a name="list-of-supported-functions"></a>サポートされている関数のリスト

| 職務 | 説明 |
|----------|-------------|
| [AddDays](er-functions-datetime-adddays.md) | この関数は、指定された開始日の前または後の指定された日数分の *[DateTime](er-formula-supported-data-types-primitive.md#datetime)* 値を返します。 |
| [ChangeTimeZone](er-functions-datetime-changetimezone.md) | この関数は、他のタイムゾーンの指定された日付/時刻の値を別のタイムゾーンの日付/時刻の値に変換した *DateTime* 値を返します。 |
| [DateFormat](er-functions-datetime-dateformat.md) | この関数は、指定された日付の値を、指定された書式と任意に指定された文化でテキストとして表示する *[文字列](er-formula-supported-data-types-primitive.md#string)* 値を返します。 |
| [DateTimeFormat](er-functions-datetime-datetimeformat.md) | この関数は、特定の日付/時刻値を指定された形式およびオプションで指定されたカルチャのテキストとして表す *文字列* の値を返します。 |
| [DateTimeValue](er-functions-datetime-datetimevalue.md) | この関数は、指定された形式およびオプションで指定されたカルチャの特定のテキスト値から日付/時刻値に変換される *日時* 値を返します。 |
| [DateToDateTime](er-functions-datetime-datetodatetime.md) | この関数は、特定の日付値から協定世界時 (グリニッジ標準時 \[GMT\]) の日付/時刻値に変換された *日時* 値を返します。 |
| [DateValue](er-functions-datetime-datevalue.md) | この関数は、指定された形式およびオプションで指定されたカルチャの特定のテキスト値から日付値に変換される *[日付](er-formula-supported-data-types-primitive.md#date)* 値を返します。 |
| [DayOfYear](er-functions-datetime-dayofyear.md) | この関数は、1 月 1 日から指定された日付までの日数を表す *[整数](er-formula-supported-data-types-primitive.md#integer)* 値を返します。 |
| [日数](er-functions-datetime-days.md) | この関数は、ある指定された日付から 2 番目の指定された日付までの日数を表す *整数* 値を返します。 |
| [Now](er-functions-datetime-now.md) | この関数は、現在のアプリケーション サーバーの日付と時刻を表す *日時* 値を返します。 |
| [NullDate](er-functions-datetime-nulldate.md) | この関数は、**null** の日付 (1900 年 1 月 1 日) を表す *日付* 値を返します。 |
| [NullDateTime](er-functions-datetime-nulldatetime.md) | この関数は、協定世界時の **null** の日付/時刻値 (1900 年 1 月 1 日) を表す *日時* 値を返します。 |
| [SessionNow](er-functions-datetime-sessionnow.md) | この関数は、現在のアプリケーション セッションの日付と時刻を表す *日時* 値を返します。 |
| [SessionToday](er-functions-datetime-sessiontoday.md) | この関数は、現在のアプリケーション セッションの日付を表す *日付* 値を返します。 |
| [今日](er-functions-datetime-today.md) | この関数は、現在のアプリケーション サーバーの日付を表す *日付* 値を返します。 |
| [WeekNum](er-functions-datetime-weeknum.md) | この関数は、年の週を表す *整数* 値を返します。 |

## <a name="additional-resources"></a>追加リソース

[電子申告の概要](general-electronic-reporting.md)

[電子申告のフォーミュラ デザイナー](general-electronic-reporting-formula-designer.md)

[電子報告のフォーミュラ言語](er-formula-language.md)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
