---
title: PADLEFT ER 関数
description: この記事では、PADLEFT 電子申告 (ER) 関数の使用方法についての情報を提供します。
author: kfend
ms.date: 12/10/2019
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
ms.openlocfilehash: dac1f9142a381238bf116c4bce65958da8afc4db
ms.sourcegitcommit: 87e727005399c82cbb6509f5ce9fb33d18928d30
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 08/12/2022
ms.locfileid: "9278891"
---
# <a name="padleft-er-function"></a>PADLEFT ER 関数

[!include [banner](../includes/banner.md)]

`PADLEFT` 関数は、指定の文字列から始まる指定の文字でパディングされた指定の長さの *文字列* 値を返します。

## <a name="syntax"></a>構文

```vb
PADLEFT (text, length, padding chars)
```

## <a name="arguments"></a>引数

`text`: *文字列*

オリジナルのテキストを表す *文字列* 値。

`length`: *整数*

パディングされた文字列の最終文字数を表す *整数* 値。

`padding chars`: *文字列*

パディングに使用する文字。

## <a name="return-values"></a>戻り値

*文字列*

結果テキスト値。

## <a name="example"></a>例

`PADLEFT ("1234", 10, "`&nbsp;`")` は、テキスト文字列の **"&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;1234"** を返します。

## <a name="additional-resources"></a>追加リソース

[テキスト関数](er-functions-category-text.md)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
