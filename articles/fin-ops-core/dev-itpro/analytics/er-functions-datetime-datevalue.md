---
title: DATEVALUE ER 関数
description: このトピックでは、DATEVALUE 電子申告 (ER) 関数の使用方法についての情報を提供します。
author: NickSelin
manager: kfend
ms.date: 12/04/2019
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
ms.openlocfilehash: 82feb8284f4b6116a53d174dcdd9b8c09c4fa63a
ms.sourcegitcommit: 6cb174d1ec8b55946dca4db03d6a3c3f4c6fa2df
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 03/09/2021
ms.locfileid: "5563561"
---
# <a name="datevalue-er-function"></a>DATEVALUE ER 関数

[!include [banner](../includes/banner.md)]

`DATEVALUE` 関数は、指定された形式およびオプションで指定された [カルチャ](https://docs.microsoft.com/bingmaps/rest-services/common-parameters-and-types/supported-culture-codes) の、特定のテキスト値から日付値に変換される *日付* 値を返します。 サポートされている形式の詳細については、[標準](https://msdn.microsoft.com/library/az4se3k1(v=vs.110).aspx) と [カスタム](https://msdn.microsoft.com/library/8kb3ddd4(v=vs.110).aspx) を参照してください。

## <a name="syntax-1"></a>構文 1

```vb
DATEVALUE (text, format)
```

## <a name="syntax-2"></a>構文 2

```vb
DATEVALUE (text, format, culture)
```

## <a name="arguments"></a>引数

`text`: *文字列*

書式設定する値を表すテキスト。

`format`: *文字列*

指定されたテキストの形式。

`culture`: *文字列*

指定されたテキストの書式設定に使用されるカルチャ。

## <a name="return-values"></a>戻り値

*日付*

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