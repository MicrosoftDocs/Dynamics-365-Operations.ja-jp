---
title: DATEVALUE ER 関数
description: このトピックでは、DATEVALUE 電子申告 (ER) 関数の使用方法についての情報を提供します。
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
ms.openlocfilehash: 446f1357e54342073e73f86ef36e6467e029ebc4
ms.sourcegitcommit: e7eeca05d738e9e46d6185d1ba349836ebafc1a4
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 09/09/2021
ms.locfileid: "7485577"
---
# <a name="datevalue-er-function"></a>DATEVALUE ER 関数

[!include [banner](../includes/banner.md)]

`DATEVALUE` 関数は、指定されたテキスト値を、指定された形式とオプションで指定された [カルチャ](/bingmaps/rest-services/common-parameters-and-types/supported-culture-codes)で、日付値に変換した *[Date](er-formula-supported-data-types-primitive.md#date)* 値を返します。 サポートされている形式の詳細については、[標準](/dotnet/standard/base-types/standard-date-and-time-format-strings) と [カスタム](/dotnet/standard/base-types/custom-date-and-time-format-strings) を参照してください。

## <a name="syntax-1"></a>構文 1

```vb
DATEVALUE (text, format)
```

## <a name="syntax-2"></a>構文 2

```vb
DATEVALUE (text, format, culture)
```

## <a name="arguments"></a>引数

`text`: *[文字列](er-formula-supported-data-types-primitive.md#string)*

書式設定する値を表すテキスト。

`format`: *文字列*

指定されたテキストの形式。 サポートされている形式の詳細については、[標準](/dotnet/standard/base-types/standard-date-and-time-format-strings) と [カスタム](/dotnet/standard/base-types/custom-date-and-time-format-strings) を参照してください。

`culture`: *文字列*

指定されたテキストの書式設定に使用されるカルチャ。 サポートされているカルチャの詳細については、[カルチャ](/bingmaps/rest-services/common-parameters-and-types/supported-culture-codes)を参照してください。

## <a name="return-values"></a>戻り値

*日*

結果日付値。

## <a name="usage-notes"></a>使用上の注意

呼び出された関数の引数としてカルチャが定義されていない場合、`culture` の値は、呼び出し元のコンテキストによって定義されます。 たとえば、ドイツのカルチャを使用するように構成された **FILE** 要素に対して、電子申告 (ER) 形式の構文 1 を使用して `DATEVALUE` 関数が呼び出された場合、変換はドイツのカルチャを使用して行われます。 既定の `culture` の値は **EN-US** です。

## <a name="example-1"></a>例 1

`DATEVALUE ("21-Dec-2016", "dd-MMM-yyyy")`は、指定されたカスタム形式と既定のアプリケーションの **EN-US** カルチャに基づいて、日付値 **2016 年 12 月 21 日** を返します。

## <a name="example-2"></a>例 2

`DATEVALUE ("21-Gen-2016", "dd-MMM-yyyy", "IT")` は、指定されたカスタム形式とカルチャに基づいて、日付値 **2016 年 1 月 21 日** を返します。

ただし、`DATEVALUE ("21-Gen-2016", "dd-MMM-yyyy", "EN-US")` は、指定した文字列が、指定したカルチャに対する有効な日付として認識されていないことをユーザーに通知するための例外をスローします。

## <a name="additional-resources"></a>追加リソース

[日時の関数](er-functions-category-datetime.md)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
