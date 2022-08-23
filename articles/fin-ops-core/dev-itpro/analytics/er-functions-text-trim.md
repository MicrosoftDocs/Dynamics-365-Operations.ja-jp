---
title: TRIM ER 関数
description: この記事では、TRIM 電子申告 (ER) 関数がどのように使用されるかについての情報を提供します。
author: kfend
ms.date: 02/28/2022
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
ms.openlocfilehash: 95b8d2989d705c4998da0af8e683adf567edfe92
ms.sourcegitcommit: 87e727005399c82cbb6509f5ce9fb33d18928d30
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 08/12/2022
ms.locfileid: "9273101"
---
# <a name="trim-er-function"></a>TRIM ER 関数

[!include [banner](../includes/banner.md)]

`TRIM`関数は、タブ、改行、改行、フォーム フィードの文字が単一スペース文字で置き換えられた後、先行するスペースと末尾のスペースが切り詰められて、語間の複数のスペースが削除された後で、*文字列* の値として指定した文字列を返します。

## <a name="syntax"></a>構文

```vb
TRIM (text)
```

## <a name="arguments"></a>引数

`text`: *文字列*

*文字列* 型のデータ ソースの有効なパス。

## <a name="return-values"></a>戻り値

*文字列*

結果テキスト値。

## <a name="usage-notes"></a>使用上の注意

場合によっては、先頭のスペースと末尾のスペースを切り詰め、指定したテキストの書式設定を維持する方が望ましい場合があります。 たとえば、このテキストが複数行のテキスト ボックスに入力できる住所を表し、改行と改行形式を含む場合があります。 この場合、次の式: `REPLACE(text,"^[ \t]+|[ \t]+$","", true)` を使用し、`text` は、指定したテキスト文字列を参照 する引数です。

## <a name="example-1"></a>例 1

`TRIM ("`&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;`Sample`&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;`text`&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;`")` は、**"Sample text"** を返します。

## <a name="example-2"></a>例 2

`TRIM (CONCATENATE (CHAR(10), "`&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;`Sample`&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;`", CHAR(9),"`&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;`text`&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;`", CHAR(13)))` は、**"サンプル テキスト"** を返します。

## <a name="additional-resources"></a>追加リソース

[テキスト関数](er-functions-category-text.md)

[REPLACE ER 関数](er-functions-text-replace.md)

[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
