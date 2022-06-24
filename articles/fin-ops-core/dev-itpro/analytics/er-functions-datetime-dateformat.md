---
title: DATEFORMAT ER 関数
description: この記事では、DATEFORMAT 電子申告 (ER) 関数の使用方法についての情報を提供します。
author: NickSelin
ms.date: 09/08/2021
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
ms.openlocfilehash: e48797def54150d259dd5e0a9a4206722c168bf4
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/03/2022
ms.locfileid: "8852665"
---
# <a name="dateformat-er-function"></a>DATEFORMAT ER 関数

[!include [banner](../includes/banner.md)]

`DATEFORMAT` 関数は、指定された日付の値を、指定されたフォーマットと任意に指定された [カルチャ](/bingmaps/rest-services/common-parameters-and-types/supported-culture-codes)でテキストとして表示する *[文字列](er-formula-supported-data-types-primitive.md#string)* 値を返します。 サポートされている形式の詳細については、[標準](/dotnet/standard/base-types/standard-date-and-time-format-strings) と [カスタム](/dotnet/standard/base-types/custom-date-and-time-format-strings) を参照してください。

## <a name="syntax-1"></a>構文 1

```vb
DATEFORMAT (date, format)
```

## <a name="syntax-2"></a>構文 2

```vb
DATEFORMAT (date, format, culture)
```

## <a name="arguments"></a>引数

`date`: *[日付](er-formula-supported-data-types-primitive.md#date)*

書式設定する日付を表す日付値。

`format`: *文字列*

出力文字列の形式。 サポートされている形式の詳細については、[標準](/dotnet/standard/base-types/standard-date-and-time-format-strings) と [カスタム](/dotnet/standard/base-types/custom-date-and-time-format-strings) を参照してください。

> [!NOTE]
> 書式文字列では、標準形式またはカスタム形式を使用する場合、大文字と小文字が区別されます。 たとえば、[標準](/dotnet/standard/base-types/standard-date-and-time-format-strings) "d" 書式指定子は短い日付パターンを使用して日付を返し、標準 "D" 書式指定子は長い日付パターンを使用して日付を返します。 また、[カスタム](/dotnet/standard/base-types/custom-date-and-time-format-strings) "M" 書式指定子は月を 1 から 12 の値で返しますが、カスタム "m" 書式指定子は 0 から 59 の分を返します。

`culture`: *文字列*

書式設定に使用するカルチャ。 サポートされているカルチャの詳細については、[カルチャ](/bingmaps/rest-services/common-parameters-and-types/supported-culture-codes)を参照してください。

## <a name="return-values"></a>戻り値

*文字列*

結果文字列値。

## <a name="usage-notes"></a>使用上の注意

呼び出された関数の引数としてカルチャが定義されていない場合、`culture` の値は、呼び出し元のコンテキストによって定義されます。 たとえば、ドイツのカルチャを使用するように構成された **FILE** 要素に対して、電子申告 (ER) 形式の構文 1 を使用して `DATEFORMAT` 関数が呼び出された場合、変換はドイツのカルチャを使用して行われます。 既定の `culture` の値は **EN-US** です。

## <a name="example-1"></a>例 1

`DATEFORMAT (TODAY (), "dd-MM-yyyy")` は、指定されたカスタム形式に基づいて、現在のアプリケーション サーバーの日付 2015 年 12 月 24 日を、文字列 **"24-12-2015"** として返します。

## <a name="example-2"></a>例 2

`DATEFORMAT (SESSIONTODAY (), "d", "DE")` は、選択されたドイツのカルチャおよび指定された形式に基づいて、現在のアプリケーション セッションの日付 2015 年 12 月 24 日を、文字列 **"24-12-2015"** として返します。

## <a name="additional-resources"></a>追加リソース

[日時の関数](er-functions-category-datetime.md)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
