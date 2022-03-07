---
title: RIGHT ER 関数
description: このトピックでは、RIGHT 電子申告 (ER) 関数がどのように使用されるかについての情報を提供します。
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
ms.openlocfilehash: 45696d0498f712218126af8557521a2317d584eea5059ac3b588d3792d42495c
ms.sourcegitcommit: 42fe9790ddf0bdad911544deaa82123a396712fb
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 08/05/2021
ms.locfileid: "6740290"
---
# <a name="right-er-function"></a>RIGHT ER 関数

[!include [banner](../includes/banner.md)]

この `RIGHT` 関数は、指定された文字列の末尾から指定された数の文字を表す *文字列* 値を返します。

## <a name="syntax"></a>構文

```vb
RIGHT (text, number)
```

## <a name="arguments"></a>引数

`text`: *文字列*

オリジナルのテキストを表す *文字列* 値。

`number`: *整数*

元のテキストの末尾から戻される必要がある文字数。

## <a name="return-values"></a>戻り値

*文字列*

結果テキスト値。

## <a name="example"></a>例

`RIGHT ("Sample", 3)` は、**"ple"** を返します。

## <a name="additional-resources"></a>追加リソース

[テキスト関数](er-functions-category-text.md)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]