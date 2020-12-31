---
title: DATETIMEVALUE ER 関数
description: このトピックでは、DATETIMEVALUE 電子申告 (ER) 関数の使用方法についての情報を提供します。
author: NickSelin
manager: kfend
ms.date: 12/03/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-platform
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
ms.openlocfilehash: 30879796b483752a578e516d8afd75f5a690cabc
ms.sourcegitcommit: 659375c4cc7f5524cbf91cf6160f6a410960ac16
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 12/05/2020
ms.locfileid: "4684910"
---
# <a name="datetimevalue-er-function"></a>DATETIMEVALUE ER 関数

[!include [banner](../includes/banner.md)]

`DATETIMEVALUE` 関数は、指定された形式およびオプションで指定された [カルチャ](https://docs.microsoft.com/bingmaps/rest-services/common-parameters-and-types/supported-culture-codes) の、特定のテキスト値から日時値に変換される *DateTime* 値を返します。 サポートされている形式の詳細については、[標準](https://msdn.microsoft.com/library/az4se3k1(v=vs.110).aspx) と [カスタム](https://msdn.microsoft.com/library/8kb3ddd4(v=vs.110).aspx) を参照してください。

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
