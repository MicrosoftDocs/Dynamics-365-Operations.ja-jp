---
title: 型変換カテゴリ内の ER 関数のリスト
description: この記事では、電子申告 (ER) でサポートされる変換関数について説明します。
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
ms.openlocfilehash: 00fe8c5bce40a59580509a719212f163238815be
ms.sourcegitcommit: 87e727005399c82cbb6509f5ce9fb33d18928d30
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 08/12/2022
ms.locfileid: "9292619"
---
# <a name="list-of-er-functions-in-the-type-conversion-category"></a>型変換カテゴリ内の ER 関数のリスト

[!include [banner](../includes/banner.md)]

電子レポート (ER) 型変換関数を使用して、タイプ間で値を変換できます。 この記事では、これらの関数の概要を示します。

## <a name="type-conversion-functions"></a>型変換関数

| 職務 | 説明 |
|----------|-------------|
| [Int64Value](er-functions-conversion-int64value.md)   | この関数は、指定された文字列を表す *Int64* 値を返します。 |
| [IntValue](er-functions-conversion-intvalue.md)       | この関数は、指定された文字列を表す *Int* 値を返します。 |
| [NumberValue](er-functions-conversion-numbervalue.md) | この関数は、指定された *文字列* 値から変換された *実数* 値を返します。 変換時に、指定された 10 進と桁区切り記号が考慮されます。 |
| [金額](er-functions-conversion-value.md)             | この関数は、指定された *文字列* 値から変換された *実数* 値を返します。 |

## <a name="type-conversion-functions-in-the-container-category"></a>コンテナー カテゴリ内の型変換関数

次の表では、[コンテナー](er-functions-category-container.md) カテゴリにおける型変換関数について説明します。

| 関数 | 説明 |
|----------|-------------|
| [Base64StringToContainer](er-functions-container-base64stringtocontainer.md) | この関数は、指定された *文字列* 型の入力を *コンテナー* 型のデータ項目に変換します。 |

## <a name="type-conversion-functions-in-the-date-and-time-category"></a>日付と時刻のカテゴリ内の型変換関数のリスト

次の表では、[日付と時刻のカテゴリ](er-functions-category-datetime.md) における型変換関数について説明します。

| 職務 | 説明 |
|----------|-------------|
| [DateTimeValue](er-functions-datetime-datetimevalue.md)   | この関数は、指定された形式およびオプションで指定されたカルチャの特定の *文字列* 値から、日付/時刻値に変換される *日時* 値を返します。 |
| [DateToDateTime](er-functions-datetime-datetodatetime.md) | この関数は、特定の *日付* 値から協定世界時 (グリニッジ標準時 \[GMT\]) の日付/時刻値に変換された *日時* 値を返します。 |
| [DateValue](er-functions-datetime-datevalue.md)           | この関数は、指定された形式およびオプションで指定されたカルチャの特定の *文字列* 値から、日付値に変換される *日付* 値を返します。 |

## <a name="type-conversion-functions-in-the-list-category"></a>リスト カテゴリ内の型変換関数

次の表では、[リスト カテゴリ](er-functions-category-list.md) における型変換関数について説明します。

| 職務 | 説明 |
|----------|-------------|
| [リスト](er-functions-list-list.md)                 | この関数は、*コンテナー (レコード)* タイプの指定された引数から作成された新しいリストとして *レコード リスト* 値を返します。 |
| [ListOfFields](er-functions-list-listoffields.md) | この関数は、*列挙* または *コンテナー (レコード)* タイプの特定の引数の構造に基づいて作成された *レコード リスト* 値を返します。 |
| [分割](er-functions-list-split.md)               | この関数は、指定された *文字列* 値をサブ文字列に分割し、新しい *レコード リスト* 値として結果を返します。 |
| [StringJoin](er-functions-list-stringjoin.md)     | この関数は、指定された *レコード リスト* 値から指定したフィールドの連結された値で構成される *文字列* 値を返します。 値は、指定した区切り記号で区切ることができます。 |

## <a name="type-conversion-functions-in-the-text-category"></a>テキスト カテゴリ内の型変換関数

次の表では、[テキスト カテゴリ](er-functions-category-text.md) における型変換関数について説明します。

| 職務 | 説明 |
|----------|-------------|
| [Char](er-functions-text-char.md)                 | この関数は、指定された Unicode 番号で参照される単一文字を表す *文字列* 値を返します。 |
| [GuidValue](er-functions-text-guidvalue.md)       | この関数は、指定された *文字列* 型の入力を *GUID* 型のデータ品目に変換します。 |
| [NumberFormat](er-functions-text-numberformat.md) | この関数は、指定された形式およびオプションで指定されたカルチャで指定された数を表す、*文字列* 値を返します。 |
| [QrCode](er-functions-text-qrcode.md)             | この関数は、バイナリ形式の指定された文字列に対して、クイック応答コード (QR コード) イメージを表示する *コンテナー* 値を返します。 |
| [テキスト](er-functions-text-text.md)                 | この関数は、現在のアプリケーション インスタンスのサーバー ロケール設定に従って書式設定されるテキスト文字列に変換した後に、指定された数を表す *文字列* 値を返します。 |

## <a name="additional-resources"></a>追加リソース

[電子申告の概要](general-electronic-reporting.md)

[電子申告のフォーミュラ デザイナー](general-electronic-reporting-formula-designer.md)

[電子報告のフォーミュラ言語](er-formula-language.md)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
