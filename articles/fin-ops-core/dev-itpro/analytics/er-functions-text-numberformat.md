---
title: NUMBERFORMAT ER 関数
description: この記事では、NUMBERFORMAT 電子申告 (ER) 関数の使用方法についての情報を提供します。
author: NickSelin
ms.date: 12/10/2019
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
ms.openlocfilehash: 3e6fa4cbdfb2509418a40980aa29894b5e531bbb
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/03/2022
ms.locfileid: "8862193"
---
# <a name="numberformat-er-function"></a>NUMBERFORMAT ER 関数

[!include [banner](../includes/banner.md)]

`NUMBERFORMAT` 関数は、指定された形式およびオプションで指定された [カルチャ](/bingmaps/rest-services/common-parameters-and-types/supported-culture-codes) で、指定された数を表す *文字列* の値を返します。 サポートされている形式の詳細については、[標準](/dotnet/standard/base-types/standard-numeric-format-strings) と [カスタム](/dotnet/standard/base-types/custom-numeric-format-strings) を参照してください。

## <a name="syntax-1"></a>構文 1

```vb
NUMBERFORMAT (number, format)
```

## <a name="syntax-2"></a>構文 2

```vb
NUMBERFORMAT (number, format, culture)
```

## <a name="arguments"></a>引数

`number`: *整数* または *実数*

書式設定する必要がある数値を指定する数値。

`format` : *文字列*

形式を表す *文字列* 値。

`culture`: *文字列*

書式設定に使用するカルチャを表す *文字列* 値。

## <a name="return-values"></a>戻り値

*文字列*

結果テキスト値。

## <a name="usage-notes"></a>使用上の注意

カルチャが呼び出された関数の引数として定義されていない場合は、この関数が実行されるコンテキストによって、数値の書式設定に使用されるカルチャが決まります。

## <a name="example-1"></a>例 1

**EN-US** カルチャの場合、`NUMBERFORMAT (0.45, "p")` は **"45.00 %"** を返し、`NUMBERFORMAT (10.45, "#")` は **"10"** を返します。

## <a name="example-2"></a>例 2

`NUMBERFORMAT (10/3, "F2", "de")` は **3,33** 返すが、一方では、`NUMBERFORMAT (10/3, "F2", "en-us")` は **3.33** を返します。

## <a name="additional-resources"></a>追加リソース

[テキスト関数](er-functions-category-text.md)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]