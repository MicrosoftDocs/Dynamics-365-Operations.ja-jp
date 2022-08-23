---
title: CASE ER 関数
description: この記事では、CASE 電子申告 (ER) 関数がどのように使用されるかについての情報を提供します。
author: kfend
ms.date: 12/17/2019
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
ms.openlocfilehash: 702648e14abe980d246b92b0fe512bba07717e45
ms.sourcegitcommit: 87e727005399c82cbb6509f5ce9fb33d18928d30
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 08/12/2022
ms.locfileid: "9274862"
---
# <a name="case-er-function"></a>CASE ER 関数

[!include [banner](../includes/banner.md)]

`CASE` 関数は、指定された代替オプションに対して指定された式の値を評価し、指定された式の値に等しい最初のオプションの結果を返します。 それ以外の場合は、オプションの前にはない呼び出された関数の最後の引数としてデフォルト結果が指定されている場合、オプションのデフォルト結果を返します。 返される値は、サポートされているいずれかのデータ型の値にすることができます。

## <a name="syntax"></a>構文

```vb
CASE (expression, option 1, result 1[, option 2, result 2, …, option N, result N, default result])
```

## <a name="arguments"></a>引数

`expression`: *プリミティブ データ型* (ブール値、数値、またはテキスト)

プリミティブ データ型の値を返す有効な式。

`option 1`: *プリミティブ データ型* (ブール値、数値、またはテキスト)

呼び出された関数の `expression` 引数と同じプリミティブ データ型の値を返す有効な式。 この引数は必須です。

`result 1`: *サポートされているいずれかのデータ型*

前のオプションに対応する返された結果。 この引数は必須です。

`option N`: *プリミティブ データ型* (ブール値、数値、またはテキスト)

呼び出された関数の `expression` 引数と同じプリミティブ データ型の値を返す有効な式。 この引数はオプションです。

`result N`: *サポートされているいずれかのデータ型*

前のオプションに対応する返された結果。 この引数はオプションです。

`default result`: *サポートされているいずれかのデータ型*

一致がない場合に返される結果。 この引数はオプションです。

## <a name="return-values"></a>戻り値

*サポートされているいずれかのデータ型*

サポートされているいずれかのデータ型の結果値。

## <a name="usage-notes"></a>使用上の注意

実行時に、一致するものがなく、オプションの既定の結果が定義されていない場合は、例外がスローされます。

すべての結果は、同じデータ型を使用して指定する必要があります。 構成された結果のデータ型が一致しない場合は、デザイン時に例外がスローされます。

最初の結果値と *N* 番目の結果値が *コンテナー (レコード)* または *レコード リスト* データ型の値である場合、結果には両方の値に存在するフィールドのみが含まれます。

## <a name="example"></a>例

`CASE( DATETIMEFORMAT( NOW(), "MM"), "10", "WINTER", "11", "WINTER", "12", "WINTER", "")` は、現在のアプリケーション セッションの日付が 10 月から 12 月の場合に文字列 **"WINTER"** を返します。 それ以外の場合は、空白文字列を返します。

## <a name="additional-resources"></a>追加リソース

[論理機能](er-functions-category-logical.md)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
