---
title: DATETIMEVALUE ER 関数
description: このトピックでは、DATETIMEVALUE 電子申告 (ER) 関数の使用方法についての情報を提供します。
author: NickSelin
ms.date: 12/03/2019
ms.topic: article
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
ms.openlocfilehash: db5b2c56f0c6dcc019419801821d7a6eae8a0e91
ms.sourcegitcommit: 951393b05bf409333cb3c7ad977bcaa804aa801b
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/13/2021
ms.locfileid: "5891284"
---
# <a name="datetimevalue-er-function"></a>DATETIMEVALUE ER 関数

[!include [banner](../includes/banner.md)]

`DATETIMEVALUE` 関数は、指定された形式およびオプションで指定された [カルチャ](/bingmaps/rest-services/common-parameters-and-types/supported-culture-codes) の、特定のテキスト値から日時値に変換される *DateTime* 値を返します。 サポートされている形式の詳細については、[標準](/dotnet/standard/base-types/standard-date-and-time-format-strings) と [カスタム](/dotnet/standard/base-types/custom-date-and-time-format-strings) を参照してください。

## <a name="syntax-1"></a>構文 1

```vb
DATETIMEVALUE (text, format)
```

## <a name="syntax-2"></a>構文 2

```vb
DATETIMEVALUE (text, format, culture)
```

## <a name="arguments"></a>引数

`text`: *文字列*

書式設定する値を表すテキスト。

`format`: *文字列*

指定されたテキストの形式。

`culture`: *文字列*

指定されたテキストの書式設定に使用されるカルチャ。

## <a name="return-values"></a>戻り値

*日時*

結果日時値。

## <a name="usage-notes"></a>使用上の注意

呼び出された関数の引数としてカルチャが定義されていない場合、`culture` の値は、呼び出し元のコンテキストによって定義されます。 たとえば、ドイツのカルチャを使用するように構成された **FILE** 要素に対して、電子申告 (ER) 形式の構文 1 を使用して `DATETIMEVALUE` 関数が呼び出された場合、変換はドイツのカルチャを使用して行われます。 既定の `culture` の値は **EN-US** です。

## <a name="example-1"></a>例 1

`DATETIMEVALUE ("21-Dec-2016 02:55:00", "dd-MMM-yyyy hh:mm:ss")`は、指定されたカスタム形式と既定のアプリケーションの **EN-US** カルチャに基づいて **2016 年 12 月 21 日 2 時 55 分 00 秒** を返します。

## <a name="example-2"></a>例 2

`DATETIMEVALUE ("21-Gen-2016 02:55:00", "dd-MMM-yyyy hh:mm:ss", "IT")` は、指定されたカスタム形式およびカルチャに基づいて、**2016 年 12 月 21 日 2 時 55 分 00 秒** を返します。

ただし、`DATETIMEVALUE ("21-Gen-2016 02:55:00", "dd-MMM-yyyy hh:mm:ss", "EN-US")` は、指定した文字列が、指定したカルチャに対する有効な日時値として認識されていないことをユーザーに通知するための例外をスローします。

## <a name="additional-resources"></a>追加リソース

[日時の関数](er-functions-category-datetime.md)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]